# Sea x OpenAI: project context and proposed direction

This repository is an existing research-informed prototype that can demonstrate the team's starting point. It is not represented as work completed during the hackathon.

## Why this problem

Cancer pain occurs between appointments, where patients and caregivers need to describe episodes clearly and follow a clinician-provided plan. The project draws on Julaluck Tantipaswasin's Medical Technology research, with structured assessment, comfort activities and visit summaries.

## Evidence in this repository

| Review area | Evidence | Limits |
| --- | --- | --- |
| Problem framing | Research-to-feature mapping in the README; patient/caregiver workflow | No clinical outcome study |
| Build quality | Working static app, documented storage boundary, validation and export handling | Not production-ready; no authentication or cloud backend |
| Depth of thinking | Explainable personalization, missing-data handling, medication decisions reserved for clinicians | Current rule is an implementation choice, not a validated clinical model |
| Effective use of Codex | Codex-assisted implementation, UI verification, documentation and targeted logic checks | Assistance is disclosed; the app itself does not invoke an AI model |

## Proposed hackathon direction: Deep Domain AI

A possible substantial new build is a consent-based visit-summary assistant that turns structured pain records into a concise draft for the patient and clinician to review.

This is **not implemented**. A responsible prototype would:

1. Use synthetic records during development and evaluation.
2. Request explicit consent before transmitting any real health information.
3. Ground every summary statement in the provided records, preserve dates and units, and identify missing information.
4. Avoid diagnosis, medication changes, dosing advice and emergency triage.
5. Let the patient inspect the draft before downloading or sharing it.
6. Evaluate factual accuracy, omitted important details, unsupported claims and handling of incomplete records.

No performance, safety or clinical-benefit results are claimed. A model-generated summary would need a separate backend, secure secret management, a reviewed privacy design and further clinical evaluation before real patient use.

## Existing work versus event-day work

The current app and these documents were prepared before the event. If selected, establish an event-start Git tag and build substantial new functionality during the hackathon so the new work is clearly attributable. The current prototype is a foundation, not an event submission disguised as new development.

## Event reference

[Sea x OpenAI Regional Codex Hackathon Thailand](https://luma.com/39zve8ph)

The event lists Autonomous & Adaptive AI, AI-Native Products & Operations, and Deep Domain AI as build directions. Its FAQ says existing projects can be used as a base, but only significant new work completed during the event is judged. Confirm the latest rules with the organizers.
