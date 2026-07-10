# v8 — THE SKETCH, EXACTLY (2026-07-10) — vertical top-down flow + hero prompt box
Stephane's 2nd product sketch: the canvas is a **scrollable top-down flow**, not horizontal. Build EXACTLY:
- [ ] Canvas hero: "Hi Steph," greeting + report-type dropdown (Daily standup/Cost Report/Fleet heartbeat/Inbox digest/Weekly Review/Model benchmark/Outbound) + big **prompt box** (wavy placeholder, bottom bar: voice mic + ψ + Attach left, send circle right).
- [ ] Framing annotations: Settings (Models·Connectors/Guardrails/Appearance/Lifecycle) top-left; status legend QUEUED/RUNNING/IN REVIEW/DONE; Inbox (Urgent/Needs reply/FYI/Noise) top-right.
- [ ] Flow top→bottom: prompt → **Hook** (intent detected · router+recall) → **Brain** (206 facts/tiles, memory index, code graph, vector recall) ← dashed **Tools** (Plan) fed by counts fan (18 hook scripts/12 connectors/118 skills/11 scheduled/3 machines: macbook·mac mini·iCloud·GitHub; local/cloud) → **Reasoning layer** loop → **Orchestrator** big box (OPEN/PREVIEW/TASK/SAVED) + model list (Harness/llama local/claude Code/OpenAI Codex/X Build/Cursor/lovable +Add) + Model/Stop/Pause → **fork** (+, Quick Action).
- [ ] Fan-out 3 subagents w/ beaded PR chains (green=done/orange=live/hollow=pending): PR185→Review→SUBAGENT1 (Round 1-6) · PR186 (QPA/linter/research/build)→Revamp SUBAGENT2 · local Research→Audit ⚠ SUBAGENT3 (+optimize speed).
- [ ] Converge → **Report** robot node (0000) + deploy cube (Deploys/Artifacts) + verify/Persist · est. 10.00AM → tokens/Cost, Summary, Timeline, NEXT?.
- [ ] Run engine drives subagent states + beads fill. Keep node ids review/revamp/migrate(→Audit) so run/ALEPH/inspector still wire. Drop horizontal drag → clean vertical scroll; click→inspector.
- [ ] HOMEPAGE hero: add a **prompt box** + keep the **code-copy** (curl) concept. go crazy.
- [ ] QA (0 errors, run animates beads, dark+mobile) → ship → verify live.

# v7 — THE PLATFORM (2026-07-10) — "go crazy", full app behind the button
Decisions (Stephane, batched grill): **instant demo workspace** on click · install = **`curl -fsSL https://conductor.build/install | sh`** · **live-streaming cockpit** run fidelity · land on **the canvas**.
Spine: the landing is the trailer; "Get Started — it's free" BOOTS the real platform (full-screen takeover) where every click works on mock data, end-to-end, front-end only.
- [x] Architecture: `#landing` + `#boot` (spin-up loader) + `#app` (full-viewport fixed overlay). Get Started → boot ~1.35s → app; "Exit to site" returns.
- [x] Landing: hero + framed app preview + **one-command install** (`curl … | sh`, copy button) + wall + OSS + CTA + footer. sim.ai-tier polish (light/airy).
- [x] App shell: chrome (browser/desktop, command bar, avatars, live, exit) + collapsible rail (nav + sessions) + stage (6 views) + status bar + inspector + voice orb.
- [x] **Live run engine**: Run → queued→running (progress bars) → done; tokens stream into run console; cost/token/elapsed counters tick; on finish → fresh Report generated + toast + fleet done++. Pause/stop work.
- [x] Canvas: draggable nodes, click→inspector w/ live log + artifacts + actions, model+agent dropdown pickers (relabel), hover quick-actions, add-node "+".
- [x] Sessions swap workflow (WF map relabels fan-out nodes; inbox-triage→inbox view). Views: Fleet kanban, Inbox triage filter, Memory search, Reports gallery + reader modal, Settings toggles — all interactive.
- [x] **⌘K command palette** — 14 actions, keyboard nav.
- [x] Voice orb (particle canvas) listening/thinking/speaking + captions; hoisted to app-level (works from any view). Theme toggle. Reduced-motion + dark + mobile (no h-overflow).
- [x] Charset fix (UTF-8 meta) — killed mojibake. Icon hydration made document-wide.
- [x] Browser QA: 0 console errors across full session; run engine, all views, session-swap, modal, palette, voice, dark, mobile all verified.
- [x] GAUNTLET (code-reviewer + ux-designer sub-agents, 16 findings) → applied 16 fixes → re-verified in browser (0 errors) → committed a1d515b → pushed → **Pages LIVE v7 (HTTP 200, markers confirmed)** → artifact redeployed same URL.
- [x] Updated project_conductor memory to v7.

## v7.1 — DEEP ALEPH PORT (2026-07-10) — "more deeper to alef, go crazy"
- [x] Mined the real ALEPH project (~/Documents/Code/aleph) via Explore agent → full buildable brief.
- [x] Rebuilt voice orb → **ALEPH console** (dark cinematic own-world overlay): fibonacci-sphere breathing brain (900 particles, additive+trail, eased state hues 205/150/265/28) + **constellation** (model-colored satellites per live agent, status pulse) + butler-persona **transcript** (streaming bubbles) + **real TTS** (Web Speech API, graceful fallback).
- [x] **Command grammar** drives the real app (run/pause/stop/views/report/fork/rerun/add/theme/brief/fleet/triage) + fallback.
- [x] **Propose→approve→act plan panel** (LeCun gate): "migrate the site" → 5 risk-badged steps → approve → executes real run engine, steps light up.
- [x] **Capability tray** (9/14 connected meter + Live-now/Connect-more) + quick chips + mute + push-to-talk.
- [x] Browser-QA'd: orb, greeting, plan propose+approve+run, caps, constellation reflects run — **0 console errors**, closes clean.
- [ ] SHIP v7.1 → Pages → verify live. `/portfolio` still HELD for Stephane's explicit go.

---
# Conductor landing — v2 build plan

Goal: the hero **is** the product UI, faithful to Stephane's sketch, interactive.
Positioning: **100% open source** (MIT assumed), self-hostable, BYO Claude key. No paid tiers.

## Decisions (from Stephane, 2026-07-10)
- Name **Conductor** · light editorial · full homepage.
- Hero = interactive, super-detailed reproduction of the sketch UI. Every element visible.
- Logos live **in the hero** (Tools node + connect bar), not only a separate wall.
- Reports = **many types, filterable** (daily/weekly/cost/quarterly/benchmarks/newspaper feed).
- Features = "5 things nobody ships" shown with richer per-feature mini-UIs.
- Fully open source → replace pricing with an OSS/self-host section.
- Assumptions: MIT license; no fabricated star/user counts.

## Sketch inventory → must appear in hero
- [ ] Browser / Desktop app frame toggle
- [ ] Command bar: "Agentic build · Website migration" + ✎ Quickedits
- [ ] Brain (context · memory) node
- [ ] Orchestrator (Claude ✳) node w/ open · stop · pause + record dot + live cost
- [ ] Tools · Connector · Skills · Prompts node = real logo cluster + "+"
- [ ] Beaded-chain edges (dots), with PR labels ON the edges (PR185 / PR186 / v local · GRO-865)
- [ ] Fan-out → Review (Round 1-2-3-4-5-6), Revamp, Migrate (⚠ + fork child v2)
- [ ] Converge → Report node (Claude ✳, eta 10:00 AM)
- [ ] Node-type legend rail: link · document · flag · fork
- [ ] "+" add-node affordance w/ dashed lineage (fork)
- [ ] Consumption / summary / timeline → done&verified / QA / tracking / what's next

## Build tasks
1. [ ] Canvas engine: user-unit coord system (1240×760), locked aspect → round beads.
2. [ ] Draggable nodes (pointer events), edges + labels recompute live, clamp in-bounds.
3. [ ] Beaded edges w/ flow animation on hot edges; dashed lineage for fork.
4. [ ] Chrome bar (browser/desktop toggle, command+pencil, connect+logo avatars, live).
5. [ ] Legend rail + drag hint.
6. [ ] Scroll-reveal draw-in (fade+pop, staggered) on first view; drag after.
7. [ ] Features bento with mini-UIs (triage list, cost meter, preview frame, memory graph, gate).
8. [ ] Reports: pill filter tabs + 6 distinct panels (JS switch), incl. newspaper masthead + cost bars.
9. [ ] Open-source section: self-host terminal snippet, BYO key, MIT badge, star/clone CTAs, contribute.
10. [ ] Slim logo marquee under hero ("works with your stack").
11. [ ] OSS nav/CTAs; drop paid tiers.
12. [ ] Keep both themes + reduced-motion + mobile stack fallback for canvas.

## v3 (2026-07-10) — from Stephane's 2nd sketch pass + ALEPH mining
- [ ] Canvas: add **Prompt + Dataroom** node (user prompt + attached files) as first step → Brain → Orchestrator.
- [ ] Nodes = **sessions with quick actions**: hover reveals open / fork / flag / rerun toolbar on each.
- [ ] Tools node shows **Skills · MCPs · Prompts · Connectors** explicitly (not a generic chip).
- [ ] Improve Report node (consumption·summary·timeline → done&verified·QA·tracking·what's-next) + Review node (rounds + files + comments).
- [ ] Features → a **wall** (16, not 5): 4 featured w/ mini-UIs + 12 compact.
- [ ] Reports enriched from ALEPH: add **Inbox triage** (urgent/needs-reply/fyi/noise + pre-drafted) + **Fleet heartbeat** (services/agents live·idle·down + metrics strip). Keep daily/weekly/cost/quarterly/benchmarks/front-page.
- ALEPH source: ~/Documents/Code/aleph (yalla-brief, inbox-operator, daily-recap, usage meter, atlas home canvas of sessions).

## v6 — SHIPPED + VERIFIED (2026-07-10): multi-view app + upgraded wall
- Rail tabs = full working UIs: Canvas / Fleet (kanban dashboard) / Inbox (triage) / Memory (fact browser) / Reports (gallery) / Settings (keys·connectors·guardrails). View switcher + keyboard.
- Sessions = use-cases that SWAP the canvas workflow (website-migration / blog-batch / seo-pass / benchmark-rerun relabel nodes; inbox-triage → inbox view).
- Wall UPGRADED: 5 categorized color-coded bands (Orchestrate/See/Trust/Memory/Machines), 26 cells, 7 mini-UIs. Killed the flat uniform grid.
- Built 5 views via parallel Sonnet squad; **scrubbed real HAQQ intel** (ARR/raise/investors/strategy) → generic demo data before ship (public repo).
- Verified: 0 console errors, all views + workflow-swap + light interactions, dark + mobile.

## v5 — SHIPPED + VERIFIED + GAUNTLET-HARDENED (2026-07-10). Interactive: collapsible rail, clickable sessions, node inspector w/ live log, ALEPH voice orb, model/agent pickers, run/view controls. Gauntlet (2 adversarial agents) → fixed: hero chop (anchor+edge-fade), feature-wall accent discipline, icon fidelity (SVG marks), --muted contrast (AA), micro-type floor, rail dead-zone (Views), dead CTAs wired (toast), inspector occlusion (scroll-into-view), keyboard access, voice dialog a11y. 0 console errors, dark+mobile pass.

## v5 — RELEASE THE MONSTER (2026-07-10): full interactive demo, everything works
Emotion: "this is a REAL app in the page" → "where's the repo". Spine: the conductor's console.
- [ ] Hero = the canvas: slim the headline, enlarge the app to dominate.
- [ ] **Collapsible sidebar** — chevron toggles rail full ↔ icon-strip, smooth.
- [ ] **Clickable sessions** — click switches active session + updates command bar + status.
- [ ] **Node inspector panel** — click a node → right-docked detail panel (streaming log, files, model, cost, quick actions) with close + click-out. The "it's real" moment.
- [ ] **ALEPH voice orb** — mic FAB → overlay w/ canvas particle orb cycling idle/listening/thinking/speaking + captions ("Hey Aleph…"). Reduced-motion safe. The 1%.
- [ ] **Fix icons** — proper OpenAI/xAI/Gemini marks (no lettermark tiles), consistent stroke/size, pixel-align every card/chip/row.
- [ ] Run controls toggle a real paused state; Browser/Desktop toggle does something.
- [ ] Keep: scroll+drag world, model/agent pickers, in-canvas reports+runtimes.
- [ ] GAUNTLET: spawn parallel adversarial reviewers (design + code/QA + "beats GPT?"), fix, re-verify.
- [ ] Ship: push → Pages rebuilds; verify live 200 + markers.

## v4 — SHIPPED + VERIFIED (browser QA 2026-07-10): app-shell canvas, model/agent pickers, in-canvas reports+runtimes, sessions rail, status bar, 24-cell wall, dark+mobile. Repo pushed (9147a0c). Pages rebuilding.

## v4 (2026-07-10) — "closest validity of the visual" · make the page BE the product
- [ ] Hero = full-scale immersive **app-shell canvas**: chrome + left **sessions rail** + bottom **status bar** (cost/controls/eta/live).
- [ ] Canvas is a **scrollable world** (larger than viewport) + draggable nodes → explore the full flow.
- [ ] Per-node **model + agent toggle** = real clickable dropdown (Claude/GPT/Grok/Gemini/local · Reviewer/Builder/Migrator/Researcher). "change model & agent anytime."
- [ ] Reports move **into the canvas** (a reports window w/ tabs) — remove standalone Reports section.
- [ ] Runtimes move **into the canvas** (a runtimes dock) — remove standalone Runtimes section.
- [ ] Richer nodes: Prompt+Dataroom, Brain = Obsidian+Notion+Slack+Teams+Linear+GitHub+Figma, Report = full anatomy (consumption·summary·timeline·done&verified·QA·tracking·what's next).
- [ ] Bigger **feature wall** (~24) below the canvas.
- [ ] Repo+Pages already up (github.com/sboghossian/conductor); push v4 → Pages rebuilds; /portfolio after.

## Verify — v2 PASSED (browser QA, 2026-07-10)
- [x] 0 console errors; 8 nodes + 9 edges with computed paths + 3 labels + logos render
- [x] reveal fires (stage.drawn, node.pop); report tabs switch (cost/feed panels toggle)
- [x] newspaper front page renders; dark mode holds (canvas + masthead); mobile stack fallback; no h-overflow
- [ ] drag: engine wired + clamped, not exercised headlessly (pointer sim) — verify by hand in browser
