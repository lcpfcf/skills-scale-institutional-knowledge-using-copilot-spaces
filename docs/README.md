# OctoAcme Project Management Docs

This README is the entry point for the OctoAcme project management knowledge base. It provides a high-level summary of our processes and links to all detailed process documents in this folder.

---

## Table of Contents

1. [Summary](#summary)
2. [Core Principles](#core-principles)
3. [Project Lifecycle](#project-lifecycle)
4. [Key Artifacts](#key-artifacts)
5. [Overview of Processes](#overview-of-processes)
6. [Process Documents](#process-documents)

---

## Summary

OctoAcme uses a lightweight, end-to-end project management lifecycle designed to keep delivery iterative, measurable, and clearly owned. Work progresses through five phases — Initiation, Planning, Execution, Release, and Close & Retrospective — with a consistent set of shared artifacts and a defined set of roles ensuring accountability at every stage.

---

## Core Principles

- **Customer-first:** Prioritize customer value and usability in every decision.
- **Iterative delivery:** Deliver small, testable increments to reduce risk and gather feedback early.
- **Clear ownership:** Each project has a named Project Manager (PM) and Product Lead.
- **Data-informed decisions:** Measure impact and iterate based on evidence.
- **Psychological safety:** Encourage open feedback, learning from failure, and continuous improvement.

---

## Project Lifecycle

| Phase | Goal |
|---|---|
| **Initiation** | Validate the business need, define success metrics, and gain approval to proceed. |
| **Planning** | Turn the approved initiative into a prioritized backlog, milestone plan, and resource allocation. |
| **Execution** | Build, test, review, and iterate with a consistent delivery rhythm. |
| **Release** | Deploy with risk controls, verify outcomes, and announce to stakeholders. |
| **Close & Retrospective** | Capture learnings, track improvement actions, and close the project formally. |

---

## Key Artifacts

- **Project Charter / One-pager** — captures the problem statement, goals, and stakeholders.
- **Roadmap and Release Plan** — high-level timeline and milestone commitments.
- **Sprint/Iteration Backlog** — prioritized work items with acceptance criteria.
- **Risk Register** — tracked risks, owners, and mitigation plans.
- **Retrospective Notes and Action Items** — learnings and tracked improvements from each cycle.
- **[Release Readiness Checklist](octoacme-release-readiness-checklist.md)** — go/no-go gate owned by the Release Manager and QA Champion before every production release.
- **[Quality Gates Checklist](octoacme-quality-gates-checklist.md)** — mandatory quality checkpoints from code review through release candidate validation, owned by the QA Champion.
- **[Stakeholder Update Template](octoacme-stakeholder-update-template.md)** — standard format for stakeholder communications owned by the Stakeholder Liaison.

---

## Overview of Processes

OctoAcme's project management approach follows a lightweight, end-to-end lifecycle designed to keep delivery iterative, measurable, and clearly owned. Work progresses through five phases:

- **Initiation** — validate the business need and define success metrics.
- **Planning** — turn the approved initiative into a prioritized backlog and milestone plan.
- **Execution** — build and track progress with a consistent delivery rhythm.
- **Release** — deploy with risk controls and verification.
- **Close & Retrospective** — capture learnings and convert them into improvements.

Across the lifecycle, OctoAcme emphasizes customer value, data-informed decisions, and a single set of shared artifacts: one-pagers/charters, backlogs with acceptance criteria, risk registers, release plans, and retrospective action items.

Roles are defined to reinforce clear accountability while keeping collaboration tight:

- A **Project Manager (PM)** coordinates delivery operations — schedules, risk management, stakeholder communications, and overall execution mechanics.
- The **Product Manager (PdM)/Product Lead** drives outcomes, prioritization, and success measurement.
- **Developers** own implementation quality, contribute to estimation, and help identify technical risks.
- The **Release Manager** owns end-to-end release coordination, go/no-go decisions, and deployment safety.
- The **Quality Lead / QA Champion** drives the quality agenda, coordinates test planning, and provides sign-off at each quality gate.
- The **Stakeholder Liaison** manages external communications and ensures stakeholders receive timely, accurate updates.
- A **Subject Matter Expert (SME)** provides domain or technical depth to validate requirements and solution approaches.
- A **UX Designer** translates product requirements into user-centered workflows and designs.
- **Stakeholders** provide requirements, input, and approvals through explicit communication cadences and decision gates.

See [Roles & Personas](octoacme-roles-and-personas.md) for full definitions, interactions, and a RACI overview.

Execution relies on a steady team rhythm and disciplined workflow management. Teams use a project board with clear work states (Backlog → Ready → In Progress → In Review → QA → Done), supported by daily standups, weekly delivery syncs, and sprint/milestone demos. PM and PdM align weekly; stakeholders receive regular updates (weekly or milestone-based). Risks and dependencies are tracked in a simple risk register and escalated through a defined path — team triage first, then PM to Product Lead/dependent teams, and finally sponsor escalation for business-impacting issues.

Quality assurance is built into both the delivery workflow and the release process:

- During execution, teams favor small PRs, link work to issues and acceptance criteria, and require CI checks (tests, linting, security scans) and at least one peer approval before merge.
- Testing expectations include unit tests for new logic, integration tests where applicable, and end-to-end smoke tests for critical flows prior to release.
- Releases require acceptance criteria to be met, scans passing, release notes prepared, and rollback plans documented, followed by post-deploy verification and stakeholder announcements.
- Incidents or failed deployments trigger rollback and follow-up via blameless retrospective practices with tracked improvement actions.

---

## Process Documents

| Document | Description |
|---|---|
| [Project Management Overview](octoacme-project-management-overview.md) | Introduction to OctoAcme's approach, roles, artifacts, and communication cadence. |
| [Project Initiation](octoacme-project-initiation.md) | How to validate, scope, and gain approval for new projects. |
| [Project Planning](octoacme-project-planning.md) | Backlog creation, milestone planning, and resource allocation. |
| [Execution & Tracking](octoacme-execution-and-tracking.md) | Delivery workflow, standup cadence, and progress tracking. |
| [Risks & Communication](octoacme-risks-and-communication.md) | Risk register process, escalation paths, and stakeholder communication. |
| [Release & Deployment](octoacme-release-and-deployment.md) | Release checklists, deployment process, and post-deploy verification. |
| [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md) | Retrospective format, action item tracking, and improvement cycles. |
| [Roles & Personas](octoacme-roles-and-personas.md) | Detailed role definitions for PM, PdM, Developers, Release Manager, QA Champion, Stakeholder Liaison, UX Designer, and SME — with RACI overview. |
| [Release Readiness Checklist](octoacme-release-readiness-checklist.md) | Go/no-go gate for production releases; owned by Release Manager and QA Champion. |
| [Quality Gates Checklist](octoacme-quality-gates-checklist.md) | Mandatory quality checkpoints from code review through release candidate sign-off; owned by QA Champion. |
| [Stakeholder Update Template](octoacme-stakeholder-update-template.md) | Standard format for stakeholder communications; owned by Stakeholder Liaison. |
