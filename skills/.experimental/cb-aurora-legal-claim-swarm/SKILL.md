---
name: cb-aurora-legal-claim-swarm
description: Coordinate legal skill workflows, plugins, and agent-swarm execution for the CB x Aurora workspace when preparing Ontario employee-side medical leave, constructive dismissal, WSIB, Canada Life disability, and HRTO claim materials.
metadata:
  short-description: Coordinate Ontario employment claim workflows
---

# CB Aurora Legal Claim Swarm

## Overview

Use this skill to structure claim-preparation work for Ontario employer/employee disputes tied to medical leave, constructive dismissal, disability benefits, and human rights applications. Focus on evidence organization, timeline building, draft generation, and submission readiness for employee-side files.

## Non-Negotiable Guardrails

- Do not present output as legal advice; frame all output as draft support for licensed counsel/paralegal review.
- Do not fabricate facts, dates, medical details, or employer communications.
- Always preserve privacy: redact personal health identifiers unless required for a requested filing draft.
- Cite the source document for every material fact included in a chronology or submission draft.

## Required Workflow

1. Confirm scope: identify whether the request concerns constructive dismissal, WSIB, Canada Life disability, HRTO, or a combined strategy.
2. Build a shared chronology: collect events (leave request, employer response, accommodations, benefit denials, return-to-work attempts) in date order.
3. Map evidence: assign each event to source files (emails, medical notes, policy excerpts, denial letters, witness statements).
4. Run a claim-gap check: flag missing records, unclear causation periods, and limitation-period risks for legal review.
5. Draft outputs by venue:
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

## Plugin and Tool Coordination

Use connected workspace plugins in this order when available:

1. Document/search plugins for policy manuals, correspondence, and claim forms.
2. OCR/PDF plugins for scanned medical notes and insurer letters.
3. Spreadsheet/table plugins for chronology and damages calculations.
4. Form-filling plugins for HRTO/benefit form draft population.

If any plugin is unavailable, continue with manual extraction and explicitly list what could not be validated automatically.

## Standard Deliverables

For each matter, return:

- Issue map: claims in scope and legal theory candidates.
- Evidence matrix: fact-to-document mapping with gaps.
- Chronology: dated events with source references.
- Draft pack: forum-specific draft language and checklist.
- Risk log: limitation concerns, proof weaknesses, and counsel questions.
