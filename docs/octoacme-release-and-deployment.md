# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Ownership

| Role | Responsibility |
|---|---|
| **Release Manager** | Owns end-to-end release coordination, go/no-go decisions, and deployment execution |
| **QA Champion** | Provides quality sign-off and regression validation before release |
| **Project Manager** | Aligns release windows with project schedule; escalation path for blockers |
| **Product Manager** | Confirms feature completeness and approves release scope |
| **Stakeholder Liaison** | Coordinates external communication and stakeholder notifications |

> See [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) for full role definitions.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements

Before entering the deployment window, the **Release Manager** must confirm the [Release Readiness Checklist](octoacme-release-readiness-checklist.md) is complete. At minimum:

- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Quality gates passed — see [octoacme-quality-gates-checklist.md](octoacme-quality-gates-checklist.md)
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist
- [ ] [Release Readiness Checklist](octoacme-release-readiness-checklist.md) completed and signed off by Release Manager, QA Champion, PM, and PdM
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support (Stakeholder Liaison coordinates)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
