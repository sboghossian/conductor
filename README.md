# Conductor

**The open-source visual editor for agentic work.** You conduct, your agents build, you see everything at a glance.

Conductor is a visual, node-based canvas for running fleets of coding agents. You drop in a prompt and your files, wire them through your memory, tools, and skills, and a fleet of agents ships in parallel — each a session you can open, fork, or gate — while you watch every move, cost, and result. The whole run converges into one scheduled report.

> **Status: concept + landing.** This repo currently hosts the concept and its landing page — a single, self-contained `index.html` (no build step, no dependencies, works offline). The runtime is in design. Watch/star if you want to follow it, or fork it and build.

## The idea

```
Prompt + Dataroom  →  Brain (context · memory)  →  Orchestrator (Claude)  →  Tools (skills · MCPs · prompts)
                                                          │
                                                          ▼   fan out (parallel sessions)
                                            Review · Revamp · Migrate  →  Report (done · verified · cost · what's next)
```

- **Each node is a session** — open it, fork a v2, flag it, rerun it.
- **Any model, any agent** — pick an agent type per session (reviewer / builder / migrator / researcher) and the model that drives it. Swap models or rotate keys mid-run.
- **A cockpit, not a chat box** — attention triage, cost-before-you-run, agent-aware preview, browsable memory, and a human gate on anything irreversible.
- **Reports, your way** — daily standup, inbox triage, fleet heartbeat, cost, benchmarks, quarterly, or a full front page.
- **Runtimes & always-on** — Claude Code leads; GPT, Grok, Gemini, and local Ollama plug into the same canvas. Scheduled runs keep shipping while you sleep, self-healing and watched, on your own hardware.

## Principles

- **100% open source**, MIT. No seats, no lock-in.
- **Bring your own key** — you only pay for the tokens your agents spend.
- **Self-hosted** — runs against your local repos, memory, and MCP servers. Nothing leaves your machine.

## Run the landing

It's a single file. Open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 7777   # then open http://localhost:7777
```

## Lineage

Conductor is the node-canvas evolution of an arc of agent-fleet tools: **Helm → Atlas → Bridge → FlightDeck → Conductor**.

## License

[MIT](./LICENSE) © 2026 Stephane Boghossian
