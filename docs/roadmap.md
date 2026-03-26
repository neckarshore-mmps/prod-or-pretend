# Prod or Pretend — Roadmap

## Development Philosophy

Same as OMNIXIS Documentor: feedback-driven, spec-first, AI-assisted.

1. Build a focused MVP
2. Publish, measure, iterate
3. Develop what the audience actually responds to
4. Repeat

The goal is not perfection — it's a working pipeline from hype detection to published analysis, with measurable results.

## Tech Stack

Shared with OMNIXIS Documentor (see [OMNIXIS Technical Architecture](https://github.com/GmanFooFoo/OMNIXIS-planning/blob/main/docs/architecture/architecture-technical.md)):

| Layer | Technology |
|-------|-----------|
| Runtime | Node.js 24 |
| Backend | NestJS 10, TypeScript 5.9 |
| Database | PostgreSQL 16 |
| ORM | TypeORM |
| Queue | BullMQ + Redis |
| Testing | Jest, Playwright |
| CI/CD | GitHub Actions |
| Container | Docker Compose |
| LLM | OpenAI SDK (BYOLLM-ready) |

No experiments at the stack level. Consistency with OMNIXIS reduces context-switching and enables shared infrastructure.

## MVP Development Sequence

Each step builds on the previous. This is the implementation order from current state to first published analysis.

| # | Step | Depends on | Deliverable |
|---|------|------------|-------------|
| 1 | Project scaffold | - | NestJS app, DB, Docker Compose, CI, CLAUDE.md |
| 2 | Hype Detector | Step 1 | LinkedIn feed scanner (via aggregator API), 12-point checklist scoring, flagged post storage |
| 3 | Watch-list Manager | Step 1 | Profile tracking, interaction history, throttling rules (max 1/week, max 2-3 total) |
| 4 | Repo Analyzer (Path A) | Step 2 | GitHub repo cloning, test coverage scan, dependency health, security check, docs fidelity, CI/CD maturity |
| 5 | No-Repo Mirror (Path B) | Step 2 | Consultant framework generator: security, scaling, monitoring, support, migration, operational transferability |
| 6 | Content Generator | Steps 4 + 5 | Post draft generation for LinkedIn (professional tone) and X (loose tone), template-based |
| 7 | Human Review Dashboard | Step 6 | Web UI: review flagged posts, approve/edit/reject analyses, publish |
| 8 | LinkedIn Publishing | Step 7 | Publish finalized posts to neckarshore.ai LinkedIn (human confirms) |
| 9 | X Publishing | Step 6 | Manual posting initially, automated in Phase 2 |
| 10 | KPI Tracking | Steps 8 + 9 | Funnel metrics: reach → profile visits → contacts → mandates |

## Post-MVP (Phase 2+)

| # | Feature | Depends on | Priority |
|---|---------|------------|----------|
| 11 | Automated X posting | Step 9 + calibration data | High |
| 12 | Hype detection auto-calibration | Step 10 + Phase 1 feedback data | High |
| 13 | Live demo URL analysis | Step 4 | Medium |
| 14 | NPM package analysis | Step 4 | Medium |
| 15 | OMNIXIS integration | OMNIXIS docs review | Medium |
| 16 | Content without repo (pure LinkedIn post analysis) | Step 5 | Medium |
| 17 | CRM integration (HubSpot/Pipedrive) | Step 10 | Low |
| 18 | Additional channels (Instagram, YouTube) | Steps 8 + 9 proven | Low |

## Timeline

> **Note:** No specific dates. Focus is on building the right thing, not hitting deadlines. Same principle as OMNIXIS.

| Phase | Focus | Key Milestone | Status |
|-------|-------|---------------|--------|
| Planning | Product concept, PRD, channel strategy | PRD complete | Done |
| **Now** | MVP development | First published analysis | Not started |
| Next | Calibration + measurement | KPIs validated, detection accuracy >90% | |
| Later | Automation + expansion | Automated X, additional artifact types | |

## Shared Infrastructure with OMNIXIS

Where Prod or Pretend and OMNIXIS Documentor overlap:

| Capability | OMNIXIS | Prod or Pretend | Shared? |
|-----------|---------|-----------------|---------|
| GitHub repo cloning + analysis | Git Connector (Step 5a) | Repo Analyzer (Step 4) | Yes — reuse extraction |
| LLM-based content generation | Document Generator (Step 5e) | Content Generator (Step 6) | Partially — different prompts |
| Queue processing | BullMQ worker (Step 5c-2) | Hype detection pipeline | Yes — same infrastructure |
| Test coverage analysis | Not in OMNIXIS | Path A checkpoint | No — new capability |
| Security scanning | Not in OMNIXIS | Path A checkpoint | No — new capability |

> **Decision needed:** Build Prod or Pretend as a standalone app, or as a module within the OMNIXIS monorepo? Standalone is simpler now, monorepo enables sharing. Deferred until Step 1.

---

*See also: [PRD](prd.md) | [Hype Checklist](hype-checklist.md) | [Channel Strategy](channel-strategy.md) | [Decisions](decisions.md)*
