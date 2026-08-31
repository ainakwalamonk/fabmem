# fabMem

**Complete context for you and your agents.** fabMem is a local-first memory and code-intelligence engine. It unifies your code, docs, tickets, decisions, and past AI sessions into one graph on your machine — and serves it to the AI coding tools you already use, over MCP.

> Ask once. fabMem checks everything — your code, Notion, ClickUp, Jira, and your Claude / Codex / Cursor sessions — then answers with where each part came from.

## Why fabMem

- **Automatic** — set it up once, then forget it. It reads your AI sessions (Claude Code, Codex, Cursor…), installs its own hooks + MCP into every agent you use, indexes your code with zero config, and injects only the CLAUDE.md rules a tool is missing.
- **Private** — never leaves your machine. A local Postgres with no network port, on-device embeddings, detect-first access. Zero bytes of your code go out.
- **Portable** — any agent, no lock-in. One MCP server every agent plugs into; leave any tool and your memory stays.
- **Grounded** — answers from your real project, with receipts. A real code index (SCIP) across 10+ languages, and a temporal graph that supersedes old decisions instead of leaving them to contradict.

## Install

```bash
npm install -g fabmem
fabmem setup
```

Or run it without installing:

```bash
npx fabmem setup
```

`setup` builds your first index, walks you through connecting your tools, and opens the dashboard.

## Three steps

1. **Install fabMem** — `npx fabmem setup`. It builds your first index and starts running in the background.
2. **Connect your tools** — approve MCP connectors for Notion, ClickUp and more, so your docs and tickets come in alongside your code.
3. **Open the dashboard** — manage your project spheres, and choose which AI harnesses (Claude Code, Codex, Cursor) use fabMem.

## Commands

| Command | What it does |
|---|---|
| `fabmem setup` | Guided first-run: build + connect tools + open the dashboard |
| `fabmem dashboard [--port=]` | Open the dashboard UI |
| `fabmem index-code <path> [--sphere=]` | Index a repo's code (SCIP) into a space |
| `fabmem ask "<question>" [--sphere=] [--depth=quick/standard/deep]` | Ask your memory (local agent) |
| `fabmem backfill [--days=90]` | Background local build (sessions + docs you've touched) |
| `fabmem consolidate [sphere] [--dry-run]` | Resolve entities, normalize predicates, temporal/dedup |
| `fabmem pg <status/start/stop/uninstall>` | Manage the local embedded Postgres (the local tier) |
| `fabmem status` · `fabmem harvest` · `fabmem recent [sphere]` | Status and session utilities |

## Works with

Claude Code · Codex · Cursor · Gemini · Copilot — over MCP. Connectors: Notion, ClickUp, Jira, and other MCP sources.

## Privacy

fabMem is local-first. Your code, docs, and history are indexed into an embedded Postgres on your own machine — nothing is collected or sent to us. When you use an AI agent or model through fabMem, requests go to the providers you have configured, under their own policies.

## Requirements

- Node.js 20 or newer
- macOS or Linux (Windows support in progress)

## License

Proprietary — all rights reserved. See [LICENSE](LICENSE). fabMem is distributed as a compiled package; no source is included.
