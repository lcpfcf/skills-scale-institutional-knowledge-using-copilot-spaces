# OctoAcme — Quality Gates Checklist

## Purpose
Define the mandatory quality checkpoints that code and features must pass before advancing through the delivery pipeline. This checklist is owned by the **Quality Lead / QA Champion** and is referenced in the [Release Readiness Checklist](octoacme-release-readiness-checklist.md).

## How to Use
- Complete each gate before the work advances to the next phase.
- Items marked **Required** must be satisfied or explicitly waived with a documented rationale.
- The QA Champion signs off at each gate; Developers are responsible for meeting the criteria.

---

## Gate 1: Code Complete (PR / Code Review)

**Triggered when:** A pull request is opened targeting the main or release branch.
**Owner: Developers (author) + QA Champion (reviewer)**

- [ ] **[Required]** Code compiles without errors or warnings
- [ ] **[Required]** Unit tests added or updated for all changed logic
- [ ] **[Required]** Unit test suite passes locally and in CI
- [ ] **[Required]** Code review approved by at least one peer (or team-defined quorum)
- [ ] **[Required]** No high or critical security findings from automated scan (e.g., CodeQL, Dependabot)
- [ ] Linting and formatting rules pass in CI
- [ ] Inline documentation / comments updated where logic is non-obvious

**Gate Outcome:** PR may be merged when all Required items are checked.

---

## Gate 2: Integration & Feature Acceptance

**Triggered when:** Feature branch is merged and deployed to the integration or staging environment.
**Owner: QA Champion / Developers**

- [ ] **[Required]** Integration tests pass in the staging environment
- [ ] **[Required]** All acceptance criteria in the related issue/ticket are verified
- [ ] **[Required]** No regressions identified in directly related areas
- [ ] End-to-end test scenarios covering the new functionality pass
- [ ] API contracts validated (if applicable)
- [ ] Feature flags configured correctly for the target environment

**Gate Outcome:** Feature may be marked "QA Approved" and included in the release candidate.

---

## Gate 3: Regression & Performance

**Triggered when:** A release candidate is assembled.
**Owner: QA Champion**

- [ ] **[Required]** Full regression suite executed; results documented
- [ ] **[Required]** No new `P0` or `P1` defects introduced
- [ ] **[Required]** Existing `P0` / `P1` defects resolved or waived with Product Manager sign-off
- [ ] Performance benchmarks within accepted thresholds (response time, throughput, error rate)
- [ ] Load / stress tests completed for high-traffic release changes (if applicable)
- [ ] Accessibility testing completed for user-facing changes (if applicable)

**Gate Outcome:** Release candidate is eligible for the release readiness review.

---

## Gate 4: Release Readiness (final quality sign-off)

**Triggered when:** All prior gates pass and the deployment window approaches.
**Owner: QA Champion → Release Manager**

- [ ] **[Required]** Gates 1–3 completed and outcomes documented
- [ ] **[Required]** QA Champion provides explicit **Go / No-Go** for the release
- [ ] **[Required]** Outstanding waived items are documented with owner and follow-up date
- [ ] Smoke test script prepared and ready for post-deploy execution
- [ ] On-call engineer briefed on known edge cases or potential failure modes

**Gate Outcome:** QA Champion sign-off recorded in the [Release Readiness Checklist](octoacme-release-readiness-checklist.md).

---

## Defect Severity Reference

| Severity | Definition | Resolution Requirement |
|---|---|---|
| **P0 — Critical** | Data loss, security breach, or complete feature failure in production | Must fix before release |
| **P1 — High** | Major feature broken with no viable workaround | Fix before release or get explicit PM waiver |
| **P2 — Medium** | Feature degraded; workaround exists | Target current or next release |
| **P3 — Low** | Minor cosmetic or edge-case issue | Scheduled at PM/QA discretion |

---

## Quality Metrics to Track

| Metric | Target | Notes |
|---|---|---|
| Unit test coverage | ≥ 80% on changed files | Measured by CI |
| P0/P1 defects at release | 0 (or all waived) | Waiver logged in release issue |
| Regression suite pass rate | 100% | Failures block release candidate |
| Mean time to resolve defect | < 2 business days (P0/P1) | Tracked in defect backlog |
