<!--
=============================================================================
  SUSHANT KUMAR — GitHub Profile README
  Single source of truth. All values defined here.
  Toggle sections by setting ENABLED: true / false below.
=============================================================================
  USERNAME:           sushantkumar1807
  PORTFOLIO_URL:      https://sushantkumar.pages.dev
  MEDIUM_URL:         https://medium.com/@sushant18072002
  LINKEDIN_URL:       https://www.linkedin.com/in/sushant-kumar-147ba7190
  EMAIL:              sushant18072002@gmail.com
  STATS_URL:          https://github-readme-stats.vercel.app
  STREAK_URL:         https://streak-stats.demolab.com   ← stable (not herokuapp)
  STATS_ENABLED:      true
  STREAK_ENABLED:     true
  BLOG_ENABLED:       true    ← auto-updated daily via .github/workflows/update-blog-posts.yml
  BLOG_COUNT:         3
  STACK_STYLE:        text    ← options: text | icons
=============================================================================
-->

<div align="center">

# SUSHANT KUMAR

### Full Stack · Mobile · AI/Agentic Engineer

*You envision. I engineer. Translating abstract imagination into autonomous reality.*

<p>
  <a href="https://sushantkumar.pages.dev">
    <img src="https://img.shields.io/badge/Portfolio-sushantkumar.pages.dev-f59e0b?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Portfolio">
  </a>
  <a href="mailto:sushant18072002@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
  <a href="https://www.linkedin.com/in/sushant-kumar-147ba7190">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="https://medium.com/@sushant18072002">
    <img src="https://img.shields.io/badge/Medium-Articles-12100E?style=for-the-badge&logo=medium&logoColor=white" alt="Medium">
  </a>
</p>

<!-- Source: HeroConfig.ts → typography.stats -->
<table>
<tr>
<td align="center"><strong>10,00,000+</strong><br><sub>DAILY ACTIVE USERS</sub></td>
<td align="center"><strong>4</strong><br><sub>YEARS PRODUCTION</sub></td>
<td align="center"><strong>3</strong><br><sub>MCP SERVERS IN PROD</sub></td>
<td align="center"><strong>100%</strong><br><sub>MUTATION BLOCK RATE</sub></td>
</tr>
</table>

</div>

---

## 🔭 Currently Building

<!-- Source: AboutConfig.ts → timeline + ProjectsConfig.ts active projects -->

| Area | What | Signal |
|:---|:---|:---|
| **Agent Infrastructure** | `mcp-sqlserver` · `browser-context-mcp` · Neo4j GraphRAG | Safe AI agents over production databases |
| **Full-Stack Gov Systems** | Flutter + Spring Boot + PostgreSQL · Offline-first · 10 lakh DAU | 99.8% sync success on degrading 2G/3G |
| **Technical Writing** | LinkedIn war stories · Medium architecture deep-dives | Teaching through production failures |

---

## ⚡ Engineering Principle

<!-- Source: HowIBuildConfig.ts → paragraph4 + warStories.ts "The Dead Socket" -->

> *"Architecture should be as minimal as possible, but no simpler. True engineering excellence is invisible — it simply works, instantly and beautifully, leaving the user completely unaware of the orchestration beneath."*

> *I shipped an app that lied to a government teacher about whether her data was safe. Charles Proxy showed a 30,000ms hung TCP socket — the OS killed it silently while the app said Success. Now every system I design writes locally first, syncs asynchronously, and makes data loss structurally impossible.*

---

## 🛠️ Stack

<!-- Source: SkillsConfig.ts → categories -->

```
AI / Agentic      MCP (Model Context Protocol) · LLM Orchestration · RAG Pipelines · Safety Gates · Python
Backend           .NET 10 · Node.js · Spring Boot · Django · FastAPI · SQL Server · GCP · AWS · Microservices
Mobile            Flutter · Dart · Offline-First Sync · Impeller · Performance Profiling
Frontend          React · TypeScript · Angular · Framer Motion · WebGL / Three.js
Databases         PostgreSQL · SQL Server · Neo4j · Firebase · SQLite
DevOps            GitHub Actions · Docker · AWS · Azure · CI/CD · OTA Deployment
```

---

## 🚀 Selected Works

<!-- Source: ProjectsConfig.ts → projects[*].story  (problem → techChoice → impact) -->

---

### `01` — MCP SQL Server &nbsp; · &nbsp; [Protocol / Security Boundary](https://github.com/sushantkumar1807/mcp-sqlserver) &nbsp; `2026`

> *"Autonomous AI agents require direct database access to function as analysts. However, LLMs are inherently non-deterministic and hallucinate destructive mutations — DELETE/DROP — even when instructed otherwise."*

→ **Problem:** Standard RBAC is insufficient for dynamic reasoning engines. A single hallucinated mutation against a production database is a catastrophic, unrecoverable event.

→ **Decision:** Three-layer defense. AST tokenizer (ScriptDom) short-circuits any mutation token in `<1ms` before it reaches the driver. Auto-injected `ApplicationIntent=ReadOnly`. Engine-level `DENY` as the final, inescapable backstop.

→ **Outcome:** 10,000+ simulated malicious injections via Claude and GPT-4. **100% mutation block rate.** 3 AI teams querying production data schemas without a single destructive incident.

`#.NET10` `#ASTParsing` `#SQLServer` `#ZeroTrust` `#MCP`

---

### `02` — browser-context-mcp &nbsp; · &nbsp; [Local IPC / Edge Computing](https://github.com/sushantkumar1807/browser-context-mcp) &nbsp; `2025`

> *"AI coding agents lack real-time visibility into the DOM, network waterfalls, and console outputs of the apps they are building — severely limiting autonomous debugging."*

→ **Problem:** Existing solutions relied on heavy, latency-inducing cloud proxies. Every millisecond of proxy overhead breaks the real-time debugging contract.

→ **Decision:** Chrome DevTools Protocol (CDP) + WebSockets over `localhost`. Chrome Extension (MV3) → Local Node.js MCP Server → AI Agent. Zero network egress. Zero cloud auth. Context streams continuously.

→ **Outcome:** **0ms network overhead.** Stress-tested against highly dynamic SPAs triggering continuous DOM mutations. Distributed via npm + sideloaded extension — zero external dependencies.

`#NodeJS` `#CDP` `#WebSockets` `#LocalIPC` `#MCP`

---

### `03` — Govt. School Platform &nbsp; · &nbsp; [Offline-First Sync / Distributed State](https://sushantkumar.pages.dev) &nbsp; `2024`

> *"1,000,000+ users operating on degrading 2G/3G across rural India. Standard network-first REST caused catastrophic UI blocking and massive data loss during sync failures."*

→ **Problem:** A teacher's form submission — 20 minutes of data — silently deleted by a hung TCP socket. The app said Success. The server never received the data.

→ **Decision:** Flutter UI → Local SQLite (Source of Truth) → Background Dart Isolate (Sync Queue with exponential backoff) → AWS Gateway. **The UI never awaits a network request.**

→ **Outcome:** **99.8% sync success rate** across wildly unstable networks. 188 → 0 skipped frames. 10,00,000+ Daily Active Users. Zero perceived latency.

`#Flutter` `#SQLite` `#DartIsolates` `#CRDTs` `#AWS` `#OfflineFirst`

---

### `04` — TrunTapTravel &nbsp; · &nbsp; [State Machines / Concurrency](https://github.com/sushantkumar1807/truntaptravel) &nbsp; `2023`

> *"Complex multi-step booking flows with concurrent filter mutations lead to race conditions, unhandled runtime exceptions, and desynced UI states."*

→ **Problem:** A 7-step booking state machine that had to survive browser refreshes, network drops, and aggressive navigation without corrupting the transaction payload.

→ **Decision:** OpenAPI Spec → Zod validation → React Query cache → Zustand state → React Suspense boundaries. Unidirectional, strictly typed. React 18 Concurrent Mode for deterministic rendering under load.

→ **Outcome:** **100% of runtime type exceptions eliminated.** 95+ Lighthouse score. Sub-50ms TTFB via Vercel Edge.

`#React18` `#TypeScript` `#Zod` `#StaleWhileRevalidate` `#E2ETesting`

---

## ✍️ Latest Writing

<!-- BLOG-POST-LIST:START -->
<!-- Auto-updated daily at 11:30 AM IST via .github/workflows/update-blog-posts.yml -->
- [The Death of Micro-Optimizations: Why Senior Flutter Developers Prioritize State Ownership in 2026](https://medium.com/@sushant18072002/the-death-of-micro-optimizations-why-senior-flutter-developers-prioritize-state-ownership-in-2026-a14078a8c7f0)
- [Seamless Integration: Connecting Rasa NLU Chatbot with Flutter using WebSockets](https://medium.com/@sushant18072002/seamless-integration-connecting-rasa-nlu-chatbot-with-flutter-using-websockets-f7ca66623c0d)
<!-- BLOG-POST-LIST:END -->

➡️ [All articles on Medium →](https://medium.com/@sushant18072002)

---

## 📈 GitHub Activity

<!--
  STATS_ENABLED: true
  Stats: github-readme-stats.vercel.app with cache_seconds=86400 to reduce rate limit hits.
  Streak: streak-stats.demolab.com — community-maintained stable host (replaces defunct herokuapp URL).
  Both wrapped in <picture> for dark/light mode support.
  To disable: set STATS_ENABLED: false above — remove this entire section.
-->

<div align="center">

<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="https://github-readme-stats.vercel.app/api?username=sushantkumar1807&show_icons=true&theme=dark&hide_border=true&cache_seconds=86400"
  >
  <source
    media="(prefers-color-scheme: light)"
    srcset="https://github-readme-stats.vercel.app/api?username=sushantkumar1807&show_icons=true&theme=default&hide_border=true&cache_seconds=86400"
  >
  <img src="https://github-readme-stats.vercel.app/api?username=sushantkumar1807&show_icons=true&theme=dark&hide_border=true&cache_seconds=86400" alt="GitHub Stats" height="150" />
</picture>

&nbsp;

<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="https://streak-stats.demolab.com?user=sushantkumar1807&theme=dark&hide_border=true"
  >
  <source
    media="(prefers-color-scheme: light)"
    srcset="https://streak-stats.demolab.com?user=sushantkumar1807&theme=default&hide_border=true"
  >
  <img src="https://streak-stats.demolab.com?user=sushantkumar1807&theme=dark&hide_border=true" alt="GitHub Streak" height="150" />
</picture>

</div>

---

<div align="center">

**Building at the intersection of full-stack systems, mobile at scale, and autonomous agent infrastructure.**

*Open to: senior engineering roles · technical architecture consulting · writing collaborations*

<br>

<a href="https://sushantkumar.pages.dev">
  <img src="https://img.shields.io/badge/Full_Portfolio-sushantkumar.pages.dev-f59e0b?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Portfolio">
</a>
&nbsp;
<a href="mailto:sushant18072002@gmail.com">
  <img src="https://img.shields.io/badge/Send_a_Proposal-sushant18072002%40gmail.com-000?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
</a>

</div>
