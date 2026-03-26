---
name: brainstorming-to-prd
description: Transform a raw brainstorming session or ideation conversation into a structured PRD (Product Requirements Document). Use this skill whenever the user says "turn this into a PRD", "write a PRD from our discussion", "formalize this idea", "create a product document from our brainstorming", or when a conversation contains a raw product idea that needs to be structured. Also trigger when the user has a collection of notes, bullet points, or session transcripts and wants them shaped into a formal product document. Always use this skill instead of improvising a PRD structure — it produces consistent, high-quality output ready for Obsidian, GitHub, or Confluence.
---

# Brainstorming to PRD Skill

Transforms a raw ideation conversation or set of notes into a structured, actionable PRD. Output is Obsidian-ready Markdown with inline Properties.

## Input Sources

This skill accepts input from:
1. A live conversation in the current session
2. Pasted raw notes, bullet points, or session transcripts
3. Uploaded Markdown documents from a previous brainstorming session
4. A combination of the above

## Output Format

Always produce a single Markdown file with Obsidian-style inline Properties at the top.

```
title:: [Product Name] – PRD v[X.Y]
version:: 0.1
status:: draft
created:: [YYYY-MM-DD]
modified:: [YYYY-MM-DD]
tags:: prd, [product-name], [domain-tags]
owner:: [name or team]
```

## PRD Structure

Produce the following sections in order. Skip a section only if there is genuinely no information available and note it as `> TBD`.

### 1. Executive Summary
2–4 sentences. What is the product, who is it for, what problem does it solve, what is the primary value proposition.

### 2. Problem Statement
- The core frustration or gap that triggered the idea
- Why existing solutions are insufficient
- Who experiences this problem most acutely

### 3. Goals & Non-Goals
Two explicit lists:
- Goals: what this product must achieve
- Non-Goals: what this product explicitly does NOT do (prevents scope creep)

### 4. Target Audience
- Primary: who pays or who makes the decision to adopt
- Secondary: who uses it day-to-day
- Anti-audience: who this is NOT for

### 5. Core Features & MVP Scope
Table format:

| # | Feature | Priority | MVP | Notes |
|---|---------|----------|-----|-------|

Priority: Must / Should / Could (MoSCoW lite)
MVP: Ja / Nein

### 6. User Stories (optional, if enough detail available)
Format: `Als [Rolle] möchte ich [Aktion], damit [Ergebnis].`
Or English equivalent. Only include if substantive stories emerged from the session.

### 7. Architecture & Tech Stack
- Platform(s)
- Core technologies
- Key integrations
- Hosting / deployment approach
- Link to separate architecture doc if it exists

### 8. Phased Rollout
| Phase | Name | Description | Key Milestone |
|-------|------|-------------|---------------|

### 9. KPIs & Success Metrics
Split into:
- Awareness KPIs (reach, engagement, views)
- Conversion KPIs (leads, calls booked, mandates)
- Quality KPIs (false positive rate, analysis accuracy)

### 10. Business Model & Monetization
- Primary revenue stream
- Secondary options
- Pricing model (if known)
- What NOT to do (ethical guardrails if stated)

### 11. Open Questions & Decisions Log
Table format:

| # | Topic | Status | Decision / Next Step |
|---|-------|--------|----------------------|

Status: Open / Decided / Deferred

### 12. Out of Scope / Backlog
Ideas that came up but are explicitly not MVP. Don't lose them.

---

## Extraction Guidelines

When working from a conversation or notes:

1. Extract decisions explicitly stated by the user – mark these as Decided
2. Extract ideas mentioned but not resolved – mark as Open or Deferred
3. Infer reasonable structure where gaps exist – but mark inferences clearly with `> [inferred]`
4. Never invent facts – if something is unknown, write `> TBD`
5. Preserve the user's language and framing where possible
6. Capture emotional context (why this matters to the person) in the Problem Statement

## Quality Check Before Output

Before presenting the PRD, verify:
- [ ] Executive Summary can be read in under 30 seconds
- [ ] Goals and Non-Goals are explicit and distinct
- [ ] MVP column is filled for every feature
- [ ] Open Questions table captures everything unresolved
- [ ] No section is empty without a `> TBD` marker
- [ ] Obsidian Properties block is complete

## Output Instructions

Save the file as `/mnt/user-data/outputs/[product-name]-PRD-v[X.Y].md` and present it to the user. Ask: "Soll ich einzelne Sections vertiefen oder fehlt etwas Wesentliches?"
