# OctoAcme — Release Readiness Checklist

## Purpose
Ensure that every production release meets OctoAcme's quality, safety, and communication standards before the deployment window opens. This checklist is owned by the **Release Manager** and signed off jointly by the **QA Champion** and **Project Manager**.

## How to Use
1. Copy this checklist into the release tracking issue or project board card.
2. Assign each section to the responsible role.
3. No release proceeds until all required items are checked or explicitly waived with a documented rationale.

---

## 1. Code & Build

**Owner: Developers / Release Manager**

- [ ] All planned features and bug fixes are merged to the release branch
- [ ] CI pipeline passes (build, unit tests, integration tests, lint, security scan)
- [ ] No open `P0` / `P1` defects without an approved waiver
- [ ] Release artefact (container image, package, binary) is tagged and stored in the artefact registry
- [ ] Dependency versions are pinned; no unpinned `latest` tags in production manifests

---

## 2. Quality Gate Sign-Off

**Owner: Quality Lead / QA Champion**

- [ ] Test plan reviewed and approved for this release
- [ ] Regression suite executed; results documented and reviewed
- [ ] End-to-end / smoke test scenarios pass in the staging environment
- [ ] Accessibility and performance benchmarks meet acceptance thresholds (if applicable)
- [ ] Quality Gates Checklist completed — see [octoacme-quality-gates-checklist.md](octoacme-quality-gates-checklist.md)
- [ ] QA Champion has provided explicit **go / no-go** recommendation: `____`

---

## 3. Environments & Infrastructure

**Owner: Release Manager / Developers**

- [ ] Staging deployment successful; staging mirrors production configuration
- [ ] Environment-specific configuration and feature flags verified
- [ ] Database migrations tested in staging (if applicable)
- [ ] Backup / snapshot of production data taken (if applicable)
- [ ] Deployment window confirmed with on-call and operations teams

---

## 4. Documentation & Release Notes

**Owner: Release Manager / Product Manager**

- [ ] Release notes drafted and reviewed (see Release Notes Template in [octoacme-release-and-deployment.md](octoacme-release-and-deployment.md))
- [ ] API / integration documentation updated (if applicable)
- [ ] Internal runbooks updated for operational changes
- [ ] User-facing help content updated or scheduled for update

---

## 5. Rollback & Incident Readiness

**Owner: Release Manager / Project Manager**

- [ ] Rollback procedure documented and tested in staging
- [ ] On-call engineer confirmed and briefed on release scope
- [ ] Incident communication template prepared (see [octoacme-risks-and-communication.md](octoacme-risks-and-communication.md))
- [ ] Monitoring / alerting thresholds reviewed and adjusted if needed

---

## 6. Stakeholder Communication

**Owner: Stakeholder Liaison / Release Manager**

- [ ] Stakeholder update prepared using [octoacme-stakeholder-update-template.md](octoacme-stakeholder-update-template.md)
- [ ] Internal announcement (engineering, support, sales) scheduled or sent
- [ ] External release communication approved by Product Manager (if applicable)

---

## 7. Final Go / No-Go Sign-Off

| Role | Name | Decision | Date |
|---|---|---|---|
| Release Manager | | ☐ Go ☐ No-Go | |
| QA Champion | | ☐ Go ☐ No-Go | |
| Project Manager | | ☐ Go ☐ No-Go | |
| Product Manager | | ☐ Go ☐ No-Go | |

**Release proceeds only when all four roles confirm Go, or a named decision-maker approves an explicit waiver for any No-Go item.**

---

## Post-Release Verification

- [ ] Production deployment completed without errors
- [ ] Smoke tests passed in production
- [ ] Key metrics (error rate, latency, usage) reviewed and within expected range
- [ ] Stakeholder announcement sent
- [ ] Release issue / tracking card closed and retrospective notes captured
