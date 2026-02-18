---
name: cb-aurora-legal-claim-swarm
description: Coordinate legal skill workflows, plugins, and agent-swarm execution for the CB x Aurora workspace when preparing Ontario employee-side medical leave, constructive dismissal, WSIB, Canada Life disability, and HRTO claim materials.
metadata:
  short-description: Coordinate Ontario employment claim workflows
---

# CB Aurora Legal Claim Swarm

## Overview

Use this skill to structure claim-preparation work for Ontario employer/employee disputes tied to medical leave, constructive dismissal, disability benefits, and human rights applications. Focus on evidence organization, timeline building, draft generation, and submission readiness for employee-side files.

## Intake Prerequisites

Before drafting, confirm:

- Jurisdiction is Ontario, Canada (or clearly mark assumptions for legal review).
- The worker is requesting employee-side support (not employer-side strategy).
- Any known filing deadlines, denial dates, or hearing dates.
- Which forum(s) are in scope: WSIB, Canada Life appeal, HRTO, civil constructive dismissal, or combined.

## Non-Negotiable Guardrails

- Do not present output as legal advice; frame all output as draft support for licensed counsel/paralegal review.
- Do not fabricate facts, dates, medical details, or employer communications.
- Always preserve privacy: redact personal health identifiers unless required for a requested filing draft.
- Cite the source document for every material fact included in a chronology or submission draft.
- If material facts are missing, state `Unknown` and list exactly what evidence is required to proceed.
- Do not infer a forum-specific legal deadline as final; present it as a candidate date pending licensed legal confirmation.

## Escalate Immediately

Pause drafting and request urgent licensed review if any of the following appear:

- Imminent deadline uncertainty (e.g., filing window may expire within days).
- Threats of self-harm, coercion, retaliation, or immediate safety risk.
- Requests to hide, alter, or destroy records.

## Required Workflow

1. Confirm scope and deadlines: identify whether the request concerns constructive dismissal, WSIB, Canada Life disability, HRTO, or a combined strategy; capture all known limitation-period triggers.
   - If forum fit is uncertain, provide a `Forum Fit Unclear` note and list what facts are needed for licensed review.
2. Build a shared chronology: collect events (leave request, employer response, accommodations, benefit denials, return-to-work attempts) in date order with source citations.
3. Map evidence: assign each event to source files (emails, medical notes, policy excerpts, denial letters, witness statements) and note missing exhibits.
4. Run a claim-gap check: flag missing records, unclear causation periods, inconsistent dates, and limitation-period risks for legal review.
5. Draft outputs by venue using only verified facts:
   - WSIB package notes (injury/illness timeline, work impact, medical corroboration)
   - Canada Life appeal support draft (functional limitations, treating-provider evidence, denial-response matrix)
   - HRTO application draft support (protected ground, adverse treatment, remedy framing)
   - Constructive dismissal brief draft (fundamental change, poisoned environment, resignation nexus)
6. Produce a final handoff bundle with open questions, unresolved risks, and a filing-priority order.

## Agent Swarm Pattern

Split work into parallel specialist tracks and merge only after source checks pass:

- Intake Agent: normalize user facts, parties, and requested forum(s).
- Timeline Agent: maintain master chronology with source citations.
- Evidence Agent: index exhibits, deduplicate files, and track missing proof.
- Drafting Agent: generate venue-specific draft language from verified facts only.
- QA Agent: run contradiction checks, date consistency checks, and privacy redaction review.

## Citation Standard

- For each cited fact, include a stable locator when possible (file name + page/section/email date).
- If multiple records support the same fact, cite the strongest primary source first, then optional corroboration.
- If a source cannot be opened/read, mark it `Unverified Source` and do not rely on it for high-confidence claims.
- If duplicate or revised documents conflict, cite the latest finalized version and list superseded versions in notes.

## Codex macOS Execution Mode

- Keep outputs deterministic and skimmable: prefer short bullets and compact tables over long prose.
- Start with a one-screen executive snapshot (top risks, next deadline candidate, and key missing evidence).
- When data conflicts, present a `Conflict` note with both sources instead of choosing one.
- When information is missing, ask targeted follow-up questions in one batch to reduce user back-and-forth.
- If user requests legal conclusions, provide a draft-analysis frame and route final legal determinations to counsel/paralegal review.

## Plugin and Tool Coordination

Use connected workspace plugins in this order when available:

1. Document/search plugins for policy manuals, correspondence, and claim forms.
2. OCR/PDF plugins for scanned medical notes and insurer letters.
3. Spreadsheet/table plugins for chronology and damages calculations.
4. Form-filling plugins for HRTO/benefit form draft population.

If any plugin is unavailable, continue with manual extraction and explicitly list what could not be validated automatically.

## Output Contract

Return sections in this order:

1. Scope + Deadlines (forum, limitation triggers, assumptions)
2. Chronology (date | event | source | confidence)
3. Evidence Matrix (required element | supporting source | gap)
4. Venue Draft Blocks (WSIB / Canada Life / HRTO / constructive dismissal as applicable)
5. Risk Log + Counsel Questions (highest-risk first)

Formatting rules:

- Use `YYYY-MM-DD` when a full date is known; otherwise label date precision (e.g., `2025-03 (month-only)`).
- Use confidence tags for factual rows: `High` (documented), `Medium` (single-source), `Low` (unverified statement).

## Final QA Gate (run before handoff)

- No uncited material facts in chronology or draft blocks.
- No direct legal-advice phrasing; all conclusions framed as draft support for licensed review.
- No unresolved conflicts left without a `Conflict` note and follow-up request.
- Handoff includes a priority tag on each open item: `Urgent` (deadline/safety risk), `Next` (needed for near-term drafting), or `Monitor` (track until additional evidence arrives).

## Standard Deliverables

For each matter, return:

- Issue map: claims in scope and legal theory candidates.
- Evidence matrix: fact-to-document mapping with gaps.
- Chronology: dated events with source references.
- Draft pack: forum-specific draft language and checklist.
- Risk log: limitation concerns, proof weaknesses, and counsel questions.
