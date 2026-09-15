<div align="center">

# Claude Watch

### See Inside Your AI Coding Sessions

**Open-source observability dashboard for Claude Code.**<br>
Visualize your project's logic, track changes, and search with AI.

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/nir-diamant-759323134/)
[![Twitter](https://img.shields.io/twitter/follow/NirDiamantAI?label=Follow%20@NirDiamantAI&style=social)](https://twitter.com/NirDiamantAI)
[![Discord](https://img.shields.io/badge/Discord-Join%20community-7289da?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/cA6Aa4uyDX)
[![Sponsor](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=ff69b4)](https://github.com/sponsors/NirDiamant)

</div>

<h2 align="center">🎓 From Claude Code sessions to production</h2>

<div align="center">

**[Prompt to Production](https://europe-west1-rag-techniques-views-tracker.cloudfunctions.net/rag-techniques-tracker?notebook=claude-watch--readme&click=course-free-module-cta&target=https%3A%2F%2Fwww.diamant-ai.com%2Fcourses%3Futm_source%3Dgithub%26utm_medium%3Dreadme%26utm_campaign%3Dclaude-watch&retarget=0&text=course-free-module-cta)** - my full course on building software with AI the way professionals do: the methods and paradigms behind reliable, efficient, modular production systems, taught systematically. 17 modules, each pairing a video lecture with a hands-on lab, from your first structured prompt to a working production system.

**The course is live.** Every module is out, lecture and lab.

### 🎁 Try a full module, free

<table>
<tr>
<td align="center">🎬<br><b>7-minute<br>video lecture</b></td>
<td align="center">🛠️<br><b>Hands-on<br>tutorial</b></td>
<td align="center">🤖<br><b>AI assistant<br>inside Claude Code</b></td>
</tr>
</table>

One `npm install` adds the module's AI assistant to your Claude Code, and it guides you through the tutorial as you build.

<a href="https://europe-west1-rag-techniques-views-tracker.cloudfunctions.net/rag-techniques-tracker?notebook=claude-watch--readme&click=course-free-module-cta&target=https%3A%2F%2Fwww.diamant-ai.com%2Fcourses%3Futm_source%3Dgithub%26utm_medium%3Dreadme%26utm_campaign%3Dclaude-watch&retarget=0&text=course-free-module-cta"><img src="images/free-module-button.svg" alt="Claim your free module" width="420"></a>

### 👉 [**Get the full course**](https://europe-west1-rag-techniques-views-tracker.cloudfunctions.net/rag-techniques-tracker?notebook=claude-watch--readme&click=course-full-cta&target=https%3A%2F%2Fwww.diamant-ai.com%2Fcourses%3Futm_source%3Dgithub%26utm_medium%3Dreadme%26utm_campaign%3Dclaude-watch&retarget=0&text=course-full-cta)

</div>

---

## 📫 Stay Updated

<div align="center">
<table>
<tr>
<td align="center">🚀<br><b>Cutting-edge<br>Updates</b></td>
<td align="center">💡<br><b>Expert<br>Insights</b></td>
<td align="center">🎯<br><b>Top 0.1%<br>Content</b></td>
</tr>
</table>

[![Subscribe to DiamantAI Newsletter](images/subscribe-button.svg)](https://diamantai.substack.com/?r=336pe4&utm_campaign=pub-share-checklist)

*Join over 50,000 AI enthusiasts getting unique cutting-edge insights and free tutorials!*
</div>

[![DiamantAI's newsletter](images/substack_image.png)](https://diamantai.substack.com/?r=336pe4&utm_campaign=pub-share-checklist)

---

## Demo

<div align="center">

![Claude Watch Demo](images/demo.gif)

</div>

---

## What It Does

Claude Watch **auto-discovers** every logic file in your project (system prompts, voice guides, rules, configs, playbooks) and shows them as an **interactive visual map**.

- **Bubble Graph**: your project's brain as a zoomable map. Click to explore.
- **AI Search**: ask natural language questions across all your logic files.
- **Live Changes**: see what Claude Code is doing in real time.
- **Snapshots**: save and restore project state.

## Quick Start

```bash
# Clone and build
git clone https://github.com/NirDiamant/claude-watch.git
cd claude-watch
npm install && cd dashboard && npm install && cd ..
npm run build

# Start the dashboard
node dist/cli.js start

# In your project directory, set up hooks
node /path/to/claude-watch/dist/cli.js init
```

Open **http://localhost:3853** and use Claude Code normally.

### Enable AI Search

```bash
export ANTHROPIC_API_KEY=your-key
node dist/cli.js start
```

## How It Works

`claude-watch init` adds hooks to `.claude/settings.json`. Every Claude Code tool call gets captured, stored in SQLite, and broadcast to the dashboard via WebSocket.

The **brain scanner** auto-classifies your project's files by analyzing filenames and content (detecting patterns like NEVER, ALWAYS, MUST, PRIORITY).

## CLI

| Command | Description |
|---|---|
| `claude-watch start` | Launch dashboard |
| `claude-watch init` | Set up hooks in current project |
| `claude-watch init --global` | Set up hooks for all projects |
| `claude-watch snapshot <name>` | Save project state |
| `claude-watch status` | Show server stats |

## Contributing

PRs welcome! Ideas: timeline view, diff viewer, VS Code extension, export to PDF, notifications on rule changes.

## License

MIT
