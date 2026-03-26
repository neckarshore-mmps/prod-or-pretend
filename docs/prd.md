# Prod or Pretend — Product Requirements Document

**Version:** 0.1
**Status:** Draft
**Created:** 2026-03-26
**Owner:** German Rauhut

## 1. Executive Summary

Prod or Pretend is a constructive quality mirror that analyzes hyped tech posts on LinkedIn and X against real-world production standards. It targets decision-makers (CTOs, founders, team leads) who are drowning in tech hype and need an independent, fact-based voice to distinguish substance from air. The product serves as an acquisition channel for Neckarshore AI consulting services while establishing brand credibility through transparency and open source.

## 2. Problem Statement

**The core frustration:** LinkedIn has become an echo chamber of recycled tech hype. "Built this in a weekend," "Game changer," "AI-powered" — posted without repos, without tests, without evidence. The algorithm amplifies engagement, not substance.

**Who suffers most:** Decision-makers who budget software development. They cannot assess whether a team or contractor built production-ready software or polished theater. They lack the language and tools to question quality without looking clueless. Many have been burned: expensive projects that went live, then crashed, got hacked, or didn't scale.

**Why existing solutions fail:** Tech content creators either celebrate everything (hype amplifiers) or tear everything down (cynical debunkers). Neither helps decision-makers make better choices. There is no constructive, professional voice that mirrors reality and shows the path forward.

## 3. Goals and Non-Goals

**Goals:**
1. Establish neckarshore.ai as an independent, credible voice on software quality
2. Generate inbound consulting leads through visibility and reputation
3. Provide decision-makers with a framework to evaluate tech claims
4. Demonstrate OMNIXIS analysis capabilities through visible, public use
5. Build a measurable acquisition funnel (LinkedIn reach → mandate)

**Non-Goals:**
1. Building a SaaS product with a paywall (this is a channel, not a product)
2. Becoming a viral meme account (mission before reach — "Fart App Trap")
3. Attacking or shaming individual developers
4. Replacing human judgment with fully automated posting on LinkedIn
5. Competing with existing code review or security scanning tools

## 4. Target Audience

**Primary:** Decision-makers who budget and oversee software development
- CTOs and VP Engineering at mid-size companies
- Founders who outsource development and wonder "what am I actually paying for?"
- Engineering team leads wanting to self-evaluate their team's output
- Product owners in automotive, manufacturing, and compliance-heavy industries

**Secondary:** Technical professionals who share the frustration with hype culture
- Senior developers and architects tired of LinkedIn theater
- Consultants who advise on tech decisions

**Anti-audience:** Individual developers looking for code review tools. This is not a dev tool — it's a decision-maker channel.

## 5. Core Features and MVP Scope

| # | Feature | Priority | MVP | Notes |
|---|---------|----------|-----|-------|
| 1 | Hype-post detection (12-point checklist) | Must | Yes | ~80% accuracy target, calibrated via human feedback |
| 2 | Path A: Repo analysis (tests, security, docs, CI/CD, deps) | Must | Yes | GitHub repos only for MVP |
| 3 | Path B: No-repo qualitative mirror (consultant framework) | Must | Yes | Security, scaling, monitoring, support, migration |
| 4 | LinkedIn post generation (human finalizes) | Must | Yes | neckarshore.ai brand, professional tone |
| 5 | X post generation (manual posting) | Should | Yes | Prod or Pretend brand, looser tone |
| 6 | Watch-list management (profiles to monitor) | Must | Yes | Manual curation initially |
| 7 | Interaction throttling (max 1/week/person, max 2-3 total) | Must | Yes | Brand protection |
| 8 | Analysis result storage and tracking | Should | Yes | PostgreSQL |
| 9 | LinkedIn data aggregation (via third-party: Taplio, Apify) | Should | Yes | No direct API scraping |
| 10 | Automated hype detection (no human trigger) | Could | No | Phase 2, after calibration |
| 11 | Live demo URL analysis | Could | No | Post-MVP artifact type |
| 12 | NPM package analysis | Could | No | Post-MVP artifact type |
| 13 | Anonymous radical channel | Could | No | Deferred — "Fart App Trap" risk |

## 6. User Stories

1. As a **CTO**, I want to see a credible, independent analysis of a hyped tech post, so I can form an informed opinion before my team brings it up in the next sprint planning.

2. As a **founder outsourcing development**, I want to understand what "production-ready" actually means, so I can ask better questions of my contractors.

3. As a **team lead**, I want a quality framework I can reference when my developers show me impressive demos that haven't been tested, so I can push back constructively without seeming like a blocker.

4. As the **Prod or Pretend operator**, I want the system to detect hype posts automatically and suggest analyses, so I only spend time on human review and finalization, not on finding targets.

## 7. Architecture and Tech Stack

**Stack:** TypeScript, PostgreSQL, GitHub, Playwright (consistent with OMNIXIS stack)

**Components:**
1. **Hype Detector** — scans LinkedIn feed (via aggregator API) against 12-point checklist, scores posts
2. **Analyzer** — dual-path engine:
   - Path A: GitHub repo analysis (clone, scan tests, security, docs, deps, CI/CD)
   - Path B: Qualitative mirror generator (consultant framework questions)
3. **Content Generator** — produces post drafts for LinkedIn and X, adapted to channel tone
4. **Watch-list Manager** — tracks profiles, interaction history, throttling rules
5. **Dashboard** — analysis results, interaction history, KPI tracking

**Integration with OMNIXIS:** The analyzer reuses OMNIXIS extraction and analysis capabilities where applicable. Specific integration points deferred until OMNIXIS documentation is reviewed.

**Extensibility:** Artifact types (repos, live demos, NPM packages, LinkedIn posts without repos) are plugin-based from day one.

## 8. Phased Rollout

| Phase | Name | Description | Key Milestone |
|-------|------|-------------|---------------|
| 1 | Calibration | Hype detector runs, human decides. System logs hits. No auto-posting. Goal: train to ~99% accuracy. | Detector accuracy validated |
| 2 | LinkedIn Launch | Human-finalized posts on neckarshore.ai LinkedIn. Measured via KPIs. | First 10 posts published, funnel measured |
| 3 | X Launch | Prod or Pretend brand on X. Looser tone, lower barrier. | X account active, cross-referencing LinkedIn |
| 4 | Automation | Full automation for X. LinkedIn stays human-in-loop. | Automated X posting with quality gate |
| 5 | Expansion | Additional artifact types, additional channels, OMNIXIS integration | Full analysis engine |

## 9. KPIs and Success Metrics

**Awareness KPIs:**
1. Follower growth on LinkedIn and X (monthly)
2. Post reach and impressions (per post)
3. Engagement rate (comments and shares, not just likes)
4. Article views per publication

**Conversion KPIs:**
1. Profile visits after publication
2. Contact requests per month
3. Calendly bookings (who enters the sales funnel?)
4. Conversation → mandate conversion rate

**Quality KPIs:**
1. Hype detection accuracy (false positive rate)
2. Analysis quality (measured via engagement on analysis posts)
3. Brand sentiment (positive/constructive perception vs. "troll" perception)

> **Note:** The gap between LinkedIn activity and actual sales often happens outside LinkedIn (email, phone, in-person). Must be manually linked until CRM automates it.

## 10. Business Model and Monetization

**Primary revenue stream:** Prod or Pretend is an acquisition channel for consulting mandates and services under Neckarshore AI. Content builds reputation → reputation generates inbound leads → leads become mandates.

**Secondary options (open):**
- Paid content channel (if reach justifies it)
- Security-scan self-service offering (long-term)
- Speaking engagements and workshops (driven by visibility)

**What NOT to do:**
- No paywall on the core analysis content (defeats the credibility purpose)
- No sponsored analyses (destroys independence)
- No affiliate/referral income from tools being analyzed (conflict of interest)

**CRM strategy:**
- Current: LinkedIn + Calendly + Outlook (sufficient for MVP)
- Future: HubSpot Free or Pipedrive when contacts start slipping through cracks
- Principle: A CRM that isn't used is worse than no CRM

## 11. Open Questions and Decisions Log

| # | Topic | Status | Decision / Next Step |
|---|-------|--------|----------------------|
| 1 | Brand name | Decided | "Prod or Pretend" — alliteration, instantly understandable |
| 2 | Primary channel | Decided | LinkedIn (neckarshore.ai), then X (Prod or Pretend) |
| 3 | Target audience | Decided | Decision-makers, NOT developers |
| 4 | Monetization | Decided | Acquisition channel for consulting, not paywall |
| 5 | Open source | Decided | Yes — credibility through transparency |
| 6 | Tone | Decided | Constructive-critical, solution-oriented, never confrontational |
| 7 | Interaction limits | Decided | Max 1/week/person, max 2-3 total per person |
| 8 | Human-in-loop for LinkedIn | Decided | Always. No auto-posting on LinkedIn. |
| 9 | OMNIXIS integration point | Deferred | Needs OMNIXIS documentation review |
| 10 | License (MIT/Apache/BSL) | Open | To be decided before going public |
| 11 | X brand sub-name | Open | Prod or Pretend, but visual identity TBD |
| 12 | Link to original post in own posts | Open | Platform-native only, no external links on LinkedIn |
| 13 | Anonymous radical channel | Deferred | Consciously parked — "Fart App Trap" |

## 12. Out of Scope / Backlog

See [backlog/ideas.md](../backlog/ideas.md) for the full list. Key deferred items:

1. **Anonymous channel** — higher reach via provocation, no brand tie. Tempting. Consciously deferred to stay mission-aligned.
2. **Instagram / YouTube** — if LinkedIn/X format works, expand to visual platforms.
3. **OMNIXIS deep integration** — analyzer reuses OMNIXIS capabilities. Deferred until OMNIXIS docs are reviewed.
4. **Live demo URL analysis** — analyze deployed apps, not just repos.
5. **NPM package analysis** — scan published packages for quality signals.
6. **Content paywall** — only if organic reach proves the format has paying-audience potential.
