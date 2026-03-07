<div align="center">

# Autopilot

Visual time-block schedule builder that generates shell commands. No more manual duration math.

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

Autopilot is an internal visual schedule builder that lets you chain time blocks (active, idle, away) on a timeline and instantly generates the corresponding macOS shell commands. No server required — everything runs client-side in a single file.

**Live:** [autopilot.neorgon.com](https://autopilot.neorgon.com/)

> **Note:** This site includes a `noindex, nofollow` meta tag — it is an internal tool.

## Features

- **Visual block-chain editor** — set start time, duration, and state (active / idle / away) per block
- **Real-time timeline preview** — see your schedule rendered as a visual timeline as you build it
- **Live shell command generation** — commands update instantly as blocks change
- **AppleScript source viewer** — inspect the generated AppleScript behind each command

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

Single `index.html` (~43 KB) with embedded CSS and JS. No dependencies, no build tools, no framework.

## Tech stack

- Pure HTML + CSS + JavaScript
- Single-file architecture
- Zero dependencies

<div align="center">

---

Part of [Neorgon](https://neorgon.com)

</div>
