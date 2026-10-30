<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7c3aed,35:a855f7,65:db2777,100:f59e0b&height=250&section=header&text=Olegario%20Ram%C3%ADrez&fontSize=58&fontColor=ffffff&fontAlignY=38&desc=Full-stack%20engineer%20%C2%B7%20Real-time%20systems%20%C2%B7%20LLM-agent%20tooling&descAlignY=60&descColor=fde68a&animation=fadeIn" width="100%" alt="Olegario Ramírez, full-stack engineer, real-time systems, LLM-agent tooling"/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=18&pause=1200&color=F472B6&center=true&vCenter=true&width=820&lines=WebSocket+control+plane+used+in+live+broadcasts;SvelteKit+%2B+Supabase%2FPostgreSQL+in+production;Multi-agent+LLM+tooling+with+MCP;300%2B+tests+%C2%B7+CI+on+Linux%2C+Windows+and+macOS;Oaxaca%2C+M%C3%A9xico+%E2%80%94+open+to+remote+roles)](https://git.io/typing-svg)

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ol3rm2@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/oleramirez)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Ol3Ramirez)
![Profile views](https://komarev.com/ghpvc/?username=Ol3Ramirez&style=for-the-badge&color=7c3aed&label=PROFILE+VIEWS)

</div>

I build TypeScript and Python systems where timing and correctness matter: a WebSocket control plane used in live broadcasts, a PostgreSQL operations platform in production, and the multi-agent LLM tooling I use to build both.

<div align="center">

![Playwright E2E](https://img.shields.io/badge/Playwright_E2E-100%2B_cases-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![Test stack](https://img.shields.io/badge/Tests-pytest_%C2%B7_Vitest_%C2%B7_Playwright-7c3aed?style=for-the-badge&logo=vitest&logoColor=white)
![CI](https://img.shields.io/badge/CI-Linux_%C2%B7_Windows_%C2%B7_macOS-db2777?style=for-the-badge&logo=githubactions&logoColor=white)
![Production](https://img.shields.io/badge/In_production-ISP_platform-f59e0b?style=for-the-badge&logo=supabase&logoColor=black)

</div>

---

## Tech stack

<div align="center">

**Languages**

[![Languages](https://skillicons.dev/icons?i=ts,js,py,rust,bash,powershell,html,css&theme=dark)](https://skillicons.dev)

**Frontend**

[![Frontend](https://skillicons.dev/icons?i=svelte,react,nextjs,tailwind,vite,redux&theme=dark)](https://skillicons.dev)

**Backend and data**

[![Backend](https://skillicons.dev/icons?i=nodejs,express,postgres,supabase,sqlite,prisma&theme=dark)](https://skillicons.dev)

**DevOps and testing**

[![DevOps](https://skillicons.dev/icons?i=githubactions,docker,aws,vercel,sentry,vitest,git,linux&theme=dark)](https://skillicons.dev)

![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

**AI, media and networking**

![Claude](https://img.shields.io/badge/Claude_Code-D97706?style=flat-square&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-6d28d9?style=flat-square&logo=modelcontextprotocol&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)
![OBS Studio](https://img.shields.io/badge/OBS_Studio-302E31?style=flat-square&logo=obsstudio&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logo=socketdotio&logoColor=white)
![MikroTik](https://img.shields.io/badge/MikroTik_RouterOS-293239?style=flat-square&logo=mikrotik&logoColor=white)

<br/>

<img src="assets/languages.svg" width="720" alt="Language mix across my repositories by code volume: HTML 26.8%, Python 23.5%, JavaScript 19.1%, TypeScript 10.4%, Jupyter 6.9%, Svelte 4.2%, PowerShell 3.4%, Shell 2.6%, SQL 1.9%."/>

</div>

---

## What I build

### 🔴 Live-broadcast control plane (real-time)

[![Stack](https://skillicons.dev/icons?i=py,js,nodejs,rust,bash,powershell&theme=dark)](https://skillicons.dev)
&nbsp;![OBS](https://img.shields.io/badge/OBS_Studio-302E31?style=flat-square&logo=obsstudio&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)
![Used live](https://img.shields.io/badge/Used_in-live_broadcasts-dc2626?style=flat-square)

**Problem.** Run broadcast graphics (scoreboard, lineups, instant replay) for live sports from the on-site operator's phone, in sync with a video feed that arrives seconds late.

**Built.** A Python asyncio WebSocket relay that fans commands out to browser-source overlays and drives OBS Studio over obs-websocket v5. It keeps per-client outbox queues, replays state on reconnect, checks tokens in constant time and allowlists Origins against cross-site WebSocket hijacking. A "field mode" delays commands to match stream latency, and an FFmpeg pipeline cuts slow-motion replays. One config per event series feeds every overlay.

**Stack.** Python (asyncio, websockets), vanilla JS, OBS Studio, FFmpeg, Node.js (telegraf, Telegram bot for remote OBS control), Rust (tokio, small preflight CLI), PM2, Bash + PowerShell.

**Evidence.** Used in live broadcasts. 100+ Playwright E2E cases across 18 specs, each starting the real relay and HTTP server, run in GitHub Actions on Windows and macOS behind a Linux lint gate. The bot has an integration harness against a fake server that speaks the real obs-websocket protocol. A written threat model ships with the code.

*Diagram: the operator's phone sends authenticated WebSocket commands to a Python relay. The relay broadcasts state to browser-source overlays and controls OBS Studio over obs-websocket v5; OBS feeds replay clips to FFmpeg, and a Telegram bot also controls OBS.*

```mermaid
flowchart TD
  phone["📱 Operator phone<br/>(control panel)"] -->|"WebSocket + token"| relay["⚡ WebSocket relay<br/>Python asyncio"]
  relay -->|"broadcast + state replay"| overlays["🖥️ Browser-source<br/>overlays"]
  relay -->|"obs-websocket v5"| obs["🎥 OBS Studio"]
  obs -->|"replay buffer"| ffmpeg["🎞️ FFmpeg<br/>slow-motion clips"]
  bot["🤖 Telegram bot<br/>Node.js"] -->|"obs-websocket v5"| obs
  classDef core fill:#7c3aed,stroke:#c4b5fd,color:#fff
  classDef edge fill:#1e1033,stroke:#a855f7,color:#f5d0fe
  class relay core
  class phone,overlays,obs,ffmpeg,bot edge
```

### 🌐 Operations platform for an internet service provider

[![Stack](https://skillicons.dev/icons?i=svelte,ts,supabase,postgres,tailwind,sentry,vercel&theme=dark)](https://skillicons.dev)
&nbsp;![PWA](https://img.shields.io/badge/Offline--first-PWA-5A0FC8?style=flat-square&logo=pwa&logoColor=white)
![Production](https://img.shields.io/badge/Deployed-to_production-16a34a?style=flat-square)

**Problem.** Manage customers, plans, payments and receivables, inventory, support tickets and field-technician work, including offline work.

**Built.** A SvelteKit app on Supabase/PostgreSQL. Row Level Security enforces data access in the database, with JWT auth (Supabase Auth) and role-based access on top. An audit log is written by a trigger and by the app, and pg_cron runs scheduled jobs. Hardening: database-persisted rate limiting, security headers, CSRF origin checks, Zod validation on endpoints and forms. Field technicians use an offline-first PWA (IndexedDB + service worker) with an interactive map.

**Stack.** SvelteKit (Svelte 5), TypeScript, Supabase / PostgreSQL, Zod, Chart.js, Leaflet, Tailwind, Sentry, Vercel.

**Evidence.** Deployed to production for an internet service provider. 30+ RLS policies, 10 database triggers, 14 versioned migrations.

### 🧠 LLM agent orchestration framework

[![Stack](https://skillicons.dev/icons?i=py,nodejs,sqlite,githubactions&theme=dark)](https://skillicons.dev)
&nbsp;![MCP](https://img.shields.io/badge/MCP-6d28d9?style=flat-square&logo=modelcontextprotocol&logoColor=white)
![Claude](https://img.shields.io/badge/Claude_Code-D97706?style=flat-square&logo=anthropic&logoColor=white)
![Tests](https://img.shields.io/badge/300%2B_tests-Python_%2B_Node-7c3aed?style=flat-square)

**Problem.** Route engineering and research tasks to the right model and tools, and keep the routing itself tested.

**Built.** A multi-agent framework I use daily. A router classifies each task and delegates it to specialized workers, with a fan-out planner for larger jobs. Tools are reached through MCP, and episodic memory lives in SQLite with idempotent writes. An automated quality gate runs unit tests, lint, spec-conformance and documentation checks.

**Stack.** Python, Node.js (zero runtime deps), SQLite, MCP.

**Evidence.** 300+ automated tests (Python + Node), golden-set routing evals, and CI on Linux, Windows and macOS.

*Diagram: a router sends each task to specialized workers. Workers reach tools through MCP, keep idempotent SQLite memory and are checked by a quality gate; golden-set evals test the router.*

```mermaid
flowchart TD
  evals["🧪 Golden-set<br/>routing evals"] -.-> router["🧭 Router<br/>(classifies each task)"]
  router --> workers["🤖 Specialized workers"]
  workers --> tools["🔌 Tools via MCP"]
  workers --> mem[("💾 Episodic memory<br/>SQLite, idempotent")]
  workers --> gate["✅ Quality gate<br/>tests, lint, spec checks"]
  classDef core fill:#db2777,stroke:#fbcfe8,color:#fff
  classDef edge fill:#1e1033,stroke:#a855f7,color:#f5d0fe
  class router core
  class evals,workers,tools,mem,gate edge
```

### 📣 Content-operations toolkit (alpha)

[![Stack](https://skillicons.dev/icons?i=ts,py,sqlite,vitest,nodejs&theme=dark)](https://skillicons.dev)
&nbsp;![Status](https://img.shields.io/badge/Status-alpha-f59e0b?style=flat-square)
![Tests](https://img.shields.io/badge/500%2B_tests-Vitest_%2B_pytest-7c3aed?style=flat-square)

**Problem.** Run content for several social pages from one place, with per-page config and an approval step before anything is published.

**Built.** A TypeScript monorepo, still in development. A strict-TypeScript core with Zod-validated, inheritable per-page config, SQLite persistence with versioned migrations, platform adapters behind one interface and a content-queue state machine (draft, review, approved, published) designed around a human-only approval step. Also: a text-to-speech service with Python inference isolated behind a process watchdog, and an HTML-to-video wrapper.

**Stack.** TypeScript (strict, `noUncheckedIndexedAccess`), Zod, SQLite (better-sqlite3), Vitest, Python, pytest, pnpm workspaces, FFmpeg.

**Evidence.** 500+ automated tests (Vitest + pytest), including credential-handling and path-traversal tests. 5 written ADRs (API-first design, adapter shape, SQLite driver choice).

### 🎬 Local-AI media pipelines

[![Stack](https://skillicons.dev/icons?i=py&theme=dark)](https://skillicons.dev)
&nbsp;![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Whisper](https://img.shields.io/badge/WhisperX-faster--whisper-0ea5e9?style=flat-square)

**Problem.** Turn long live streams into short captioned clips and written summaries without sending media to a paid cloud API.

**Built.** A pipeline that turns long streams into short vertical clips: word-level transcription (WhisperX), local-LLM highlight detection (Ollama), a face-aware static 9:16 crop (MediaPipe) and burned-in karaoke-style captions (FFmpeg). A second CLI transcribes downloads or live streams in chunks (faster-whisper) and drafts analysis with a local LLM. I compared several local models before picking a default.

**Stack.** Python, WhisperX, faster-whisper, Ollama, MediaPipe, OpenCV, FFmpeg, pytest.

**Evidence.** 50+ CLI tests, including a regression test that blocks reinstalling a media-download dependency version with a known CVE. Written security audit, all findings resolved.

---

## How I work with AI agents

- I build daily with AI coding agents (Claude Code) and treat them as an unreliable dependency: routed, tested and gated.
- Custom guardrail hooks (150+ tests) block secrets, unsafe commands and malformed commits before they land. The Bash and PowerShell bootstrap scripts are equivalent on Windows and macOS.
- Before adopting a new model I run structured experiments (latency, calibration, synthesis quality) and turn the findings into routing rules.
- My tooling is designed so that publishing requires explicit human approval.

## Engineering habits

- Decisions written down: ADRs, threat models, dated security audits.
- Adversarial review of my own fixes: multi-round audits, and a second-model review on race conditions.

## Currently deepening

<div align="center">

![LLM security](https://img.shields.io/badge/OWASP_Top_10_for_LLM_Apps-In_progress-7c3aed?style=for-the-badge&labelColor=1a1a2e)
![Detection engineering](https://img.shields.io/badge/Sigma_%C2%B7_MITRE_ATT%26CK-Studying-db2777?style=for-the-badge&labelColor=1a1a2e)

</div>

---

## GitHub activity

<div align="center">

<img src="https://streak-stats.demolab.com?user=Ol3Ramirez&theme=radical&hide_border=true&date_format=M%20j%5B%2C%20Y%5D" alt="GitHub contribution streak and total contributions, private contributions included" />

</div>

Most of my day-to-day work shows up in this profile's contribution graph. I can walk through the architecture and code of any of these projects in an interview.

Spanish (native). Email: <ol3rm2@gmail.com>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:f59e0b,40:db2777,70:c026d3,100:7c3aed&height=100&section=footer" width="100%" alt=""/>
