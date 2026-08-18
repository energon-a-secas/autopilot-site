# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
make serve          # http://localhost:8811
make kill           # stop the server
open index.html     # also works — no ES modules, no server required
```

## Architecture

Single `index.html` (~43 KB) with all CSS and JS embedded. No build step, no dependencies, no framework.

**localStorage key:** `"flow-planner"`

**State variables** (module-level):
- `blocks[]`: array of block objects `{ type: 'active'|'away'|'rest', h: number, m: number }`
- `startHour`, `startMinute`, `startAmpm`: schedule start time
- Three command template strings read live from DOM inputs (`#cmd-active-tpl`, `#cmd-away-tpl`, `#cmd-rest-tpl`)

**Block types:**
- `active`: runs the active command template for its duration
- `away`: runs the away command template for its duration
- `rest`: standalone terminator; no duration, runs rest command once at the very end

**Render strategy** (critical: do not conflate):
- `fullRender()` → `renderChain() + renderTimeline() + renderCommand()`: used after structural changes (add/delete block, blur)
- `partialRender()` → `renderTimeline() + renderCommand()` only: used during `input` events on duration fields to avoid blurring the focused input mid-type

**Command generation** (`generateCommand()`):
- Expands templates using `expandTemplate(tpl, b)` with placeholders `{mins}`, `{secs}`, `{h}`, `{m}`
- Joins segments with `"; "`
- `rest` block uses its template string verbatim (no placeholder expansion)

**Puzzle-piece block shapes:** CSS `clip-path` polygons give blocks interlocking tabs/indents. Position classes (`solo`, `first`, `middle`, `last`) are assigned by `posClass()` among non-`rest` blocks only. Rest blocks are always `solo` and get `margin-left: 8px` instead of the negative overlap margin.

## Design tokens

| Token | Value | Usage |
|---|---|---|
| `--accent` | `#22d3ee` (cyan) | active blocks, focus rings |
| `--away` | `#94a3b8` (slate) | away blocks |
| `--rest` | `#f472b6` (pink) | rest block |
| `--surface-1` | `rgba(255,255,255,.03)` | card backgrounds |
| Background | `#040714` | body |

## Presets

Four built-in presets (`full-day`, `morning`, `afternoon`, `split-day`) defined in the `PRESETS` constant. Presets only set `blocks[]` and start time. They never overwrite command templates.
