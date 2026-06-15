<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=Olegario%20Ramírez&fontSize=52&fontColor=ffffff&fontAlignY=38&desc=Full%20Stack%20Developer%20%7C%20AI%20Systems%20Builder&descAlignY=62&descColor=a78bfa&animation=fadeIn" width="100%" />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&pause=1200&color=A78BFA&center=true&vCenter=true&width=700&lines=TypeScript+%2B+React+%2B+Node.js;Multi-Agent+Systems+%2B+MCP+Protocol;WISP+Networks+%2B+IoT+Automation;LLM+Security+%2B+AI+Red+Teaming;Building+from+Oaxaca%2C+México)](https://git.io/typing-svg)

</div>

---

## About Me

Full Stack Developer building **production-grade systems** that combine robust backend engineering with AI automation. I don't just use AI tools — I architect multi-agent systems from the ground up.

- Based in **Oaxaca, México** · Available remote
- Focused on **enterprise-critical systems**, real-time infrastructure, and AI pipelines
- Running a private **WISP network** (MikroTik/RouterOS) and building its management tooling
- Active learner in **LLM Security** and AI Red Teaming (OWASP LLM Top10, Prompt Injection, STRIDE-GPT)

<div align="center">

[![Email](https://img.shields.io/badge/ol3rm2@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ol3rm2@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/oleramirez)
[![GitHub](https://img.shields.io/badge/Ol3Ramirez-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Ol3Ramirez)

</div>

---

## Featured Project — OLE Agent Stack

> A production multi-agent AI system built from scratch. Not a wrapper around LangChain — a markdown-driven orchestration architecture with deterministic routing, MCP protocol integration, and executable evals.

```
User Input
    │
    ▼
 ROUTER  ──── decision tree A–R ──→  Claude Direct
    │                               (single-agent, fast)
    ├──────────────────────────────→  CHARLYBOT
    │                                (12 MCP-powered COMBOs)
    └──────────────────────────────→  RICKY
                                     (orchestrator: fan-out → fan-in)
                                          └─ CHARLYBOT COMBO × N (parallel workers)
```

**What makes it different:**

| Aspect | Typical Agent Framework | OLE Agent Stack |
|--------|------------------------|-----------------|
| Routing | LLM decides at runtime | Deterministic tree (A–R nodes) |
| Tools | Per-call tool selection | Pre-composed COMBO recipes |
| Context | Unbounded (hits limits fast) | Managed via LETI checkpoints (~150K budget) |
| Config | Python code | Version-controlled Markdown files |
| Evaluation | Manual | Executable evals (routing, COMBO, RICKY) |
| Resilience | Retry logic | Circuit Breaker (2 failures → OPEN → HALF-OPEN) |

**12 specialized COMBOs** — each a recipe of MCP servers:

`COMBO-01` Web scraping · `COMBO-02` Facebook metrics · `COMBO-03` Library docs (Context7) · `COMBO-04` SQLite/historical data · `COMBO-05` Windows diagnostics · `COMBO-06` GitHub search · `COMBO-07` Price comparison · `COMBO-08` Multi-source research · `COMBO-09` YouTube transcripts · `COMBO-10` Google Sheets sync · `COMBO-11` Image/PDF analysis · `COMBO-12` Stealth browser (anti-bot)

**Academic foundations:** ReAct (Yao et al., ICLR 2023) · Reflexion (Shinn et al., NeurIPS 2023) · Tree of Thoughts (arXiv 2305.10601) · Toolformer (Schick et al., NeurIPS 2024) · LangGraph/Pregel · MCP Protocol (Anthropic 2024)

**Stack:** Markdown-driven · Model Context Protocol · Claude Sonnet/Haiku/Opus · SQLite · Playwright · Node.js scripts

---

## Tech Stack

<div align="center">

### Languages & Core
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![SvelteKit](https://img.shields.io/badge/SvelteKit-FF3E00?style=flat-square&logo=svelte&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Redux](https://img.shields.io/badge/Redux-764ABC?style=flat-square&logo=redux&logoColor=white)

### Backend & Data
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)

### AI & Automation
![Anthropic](https://img.shields.io/badge/Anthropic_Claude-D4A27F?style=flat-square&logo=anthropic&logoColor=black)
![MCP Protocol](https://img.shields.io/badge/MCP_Protocol-8B5CF6?style=flat-square&logo=anthropic&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-FF6600?style=flat-square&logo=langchain&logoColor=white)

### Cloud & DevOps
![AWS](https://img.shields.io/badge/AWS_S3-FF9900?style=flat-square&logo=amazons3&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

### Networking & IoT
![MikroTik](https://img.shields.io/badge/MikroTik-293239?style=flat-square&logo=mikrotik&logoColor=white)
![RouterOS](https://img.shields.io/badge/RouterOS-293239?style=flat-square&logo=mikrotik&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logo=socket.io&logoColor=white)

</div>

---

## What I Build

<table>
<tr>
<td width="50%">

### Full-Stack Systems
- Operational management platforms (TypeScript + React + PostgreSQL)
- Dynamic reporting: PDF/Excel export, Chart.js/Recharts dashboards
- Real-time features via WebSockets (live scores, dashboards)
- AWS S3 integration with presigned URLs and image processing
- Interactive maps with Leaflet

</td>
<td width="50%">

### AI & Automation
- Multi-agent orchestration with MCP Protocol
- Deterministic routing trees replacing probabilistic LLM dispatch
- Executable eval frameworks for agent quality measurement
- Prompt caching strategies (60–75% cost reduction on static context)
- LLM security: prompt injection testing, OWASP LLM Top10 mitigation

</td>
</tr>
<tr>
<td>

### Security Engineering
- JWT + RBAC authentication systems
- Audit logging and rate limiting (Helmet, express-rate-limit)
- Input validation at all system boundaries (Zod schemas)
- AI Red Teaming: adversarial prompt testing, jailbreak resistance

</td>
<td>

### WISP & Networking
- MikroTik RouterOS: QoS, Queue Trees, Firewall rules
- Network management tooling with real-time diagnostics
- IoT sensor integration and Python/PowerShell automation
- Bandwidth monitoring and customer management systems

</td>
</tr>
</table>

---

## AI Security Focus

Studying applied LLM security since November 2025 — motivated by a real incident.

| Area | Resources & Tools |
|------|-------------------|
| **Prompt Injection** | OWASP LLM Top10, Promptfoo adversarial testing |
| **Threat Modeling** | STRIDE-GPT, AI-specific attack surface mapping |
| **Red Teaming AI** | Jailbreak resistance, multi-turn attack chains |
| **Secure Agent Design** | Zero-trust classification, Circuit Breaker patterns, idempotency guards |

> The OLE Agent Stack implements: Zero Trust for unknown classifications · idempotency guards on write operations · anti-loop protection (max 3 delegation levels) · Circuit Breaker state machine per worker.

---

## GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=Ol3Ramirez&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ol3Ramirez&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com?user=Ol3Ramirez&theme=tokyonight&hide_border=true)](https://git.io/streak-stats)

</div>

---

## Specialization Matrix

| Domain | Level | Currently Building |
|--------|-------|--------------------|
| Full-Stack TypeScript | ████████░░ Advanced | SvelteKit + Supabase apps |
| AI Systems / Agents | ███████░░░ Intermediate | Multi-agent orchestration (OLE Stack) |
| LLM Security | ██████░░░░ Active Learning | Red teaming, prompt injection |
| WISP / Networking | ████████░░ Advanced | MikroTik automation tooling |
| Cloud (AWS) | ██████░░░░ Intermediate | S3 integrations, serverless |
| Real-Time Systems | ████████░░ Advanced | WebSocket infrastructure |
| IoT & Automation | ██████░░░░ Intermediate | Sensor networks, Python scripts |

---

<div align="center">

**Open to collaborations on:** full-stack systems · AI automation pipelines · network management tooling · LLM security research

*Building things that actually run in production — from Oaxaca, México*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302b63,100:0f0c29&height=100&section=footer" width="100%" />

</div>
