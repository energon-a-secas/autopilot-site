<div align="center">

# Autopilot

Visual time-block schedule builder. Generate cross-platform shell commands, run the schedule in your browser, and share configs with a link.

[![Live][badge-site]][url-site]
[![HTML5][badge-html]][url-html]
[![CSS3][badge-css]][url-css]
[![JavaScript][badge-js]][url-js]
[![Claude Code][badge-claude]][url-claude]
[![License][badge-license]](LICENSE)

[badge-site]:    https://img.shields.io/badge/live_site-0063e5?style=for-the-badge&logo=googlechrome&logoColor=white
[badge-html]:    https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white
[badge-css]:     https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white
[badge-js]:      https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black
[badge-claude]:  https://img.shields.io/badge/Claude_Code-CC785C?style=for-the-badge&logo=anthropic&logoColor=white
[badge-license]: https://img.shields.io/badge/license-MIT-404040?style=for-the-badge

[url-site]:   https://autopilot.neorgon.com/
[url-html]:   #
[url-css]:    #
[url-js]:     #
[url-claude]: https://claude.ai/code

---

</div>

## Overview

Autopilot is a visual schedule builder that lets you chain time blocks (active, away, rest) on a timeline and instantly generate the corresponding shell commands. It now supports macOS, Windows, and Linux templates, runs focus sessions directly in the browser, and can encode an entire schedule into a shareable URL.

No server required — everything runs client-side in a single file.

**Live:** [autopilot.neorgon.com](https://autopilot.neorgon.com/)

> **Note:** State is stored locally in your browser. Schedules can be shared via URL.

## Features

- **Visual block-chain editor** — set start time, duration, and state (active / away / rest) per block.
- **Cross-platform command templates** — switch between macOS, Windows, and Linux defaults in one click.
- **Real-time timeline preview** — see your schedule rendered as a visual timeline as you build it.
- **Live shell command generation** — commands update instantly as blocks change.
- **In-browser runner** — run the schedule locally with live countdowns and browser notifications.
- **Shareable URLs** — the full schedule is encoded in the URL hash so you can send a config to someone else.
- **Export to script** — download the generated command as `.sh`, `.ps1`, or `.bat`.
- **Built-in presets** — Full day, Morning focus, Afternoon slot, Split session, Pomodoro, 52/17, and Meeting buffer.
- **Drag-to-reorder blocks** — rearrange schedule blocks by dragging the handle.
- **Custom presets** — save your own schedules and recall them later.
- **Export .ics** — add the schedule to Google/Outlook Calendar.
- **Session history** — track completed runs, total focus time, and day streak.

## Use cases

- Keep your screen awake during long downloads, presentations, or screen-sharing sessions.
- Run Pomodoro / 52-17 focus sessions with browser notifications.
- Automate lock/sleep at the end of a work block.
- Share a team focus routine via a single link.

## Getting started

No install or build step required. Open the file directly in your browser:

```bash
open index.html
```

Or serve locally:

```bash
python3 -m http.server
```

## Architecture

Single `index.html` (~59 KB) with embedded CSS and JS. No dependencies, no build tools, no framework.

## Tech stack

- Pure HTML + CSS + JavaScript
- Single-file architecture
- Zero dependencies

<div align="center">

---

Part of [Neorgon](https://neorgon.com)

</div>
