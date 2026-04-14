# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## Release Manager

### Role Summary
The Release Manager owns the end-to-end coordination of software releases. They ensure that every release is ready, safe to deploy, and observable, acting as the bridge between development, QA, and operations.

### Responsibilities
- Maintain and execute the [Release Readiness Checklist](octoacme-release-readiness-checklist.md)
- Schedule and communicate deployment windows
- Coordinate go/no-go decisions with stakeholders
- Ensure rollback plans are documented and tested
- Track post-release metrics and drive rapid response if issues arise

### Goals
- Ship releases on time with minimal production incidents
- Make release readiness visible and auditable
- Reduce mean time to recovery (MTTR) when issues occur

### Typical Communication
- Release readiness summaries shared with PM, QA Champion, and Product Lead
- Deployment window notifications to engineering and support teams
- Post-release status updates to stakeholders

### Interactions with Existing Roles
| Role | Interaction |
|---|---|
| Project Manager | Aligns release windows with the project schedule; surfaces blockers |
| Product Manager | Confirms feature completeness and communicates release scope |
| Developers | Validates that all PRs are merged, pipelines pass, and artefacts are ready |
| Quality Lead / QA Champion | Coordinates final sign-off via the Release Readiness Checklist |

---

## Subject Matter Expert (SME)

### Role Summary
Subject Matter Experts bring deep domain or technical knowledge to a project. They validate that requirements, designs, and implementations are accurate, feasible, and aligned with business or technical constraints.

### Responsibilities
- Review requirements and acceptance criteria for accuracy and completeness
- Advise on technical or business-domain trade-offs
- Participate in design reviews and planning sessions as needed
- Serve as an escalation point for domain-specific questions

### Goals
- Prevent rework caused by incorrect assumptions about the domain
- Accelerate decision-making by providing authoritative input
- Improve solution quality through expert review

### Typical Communication
- Async reviews of requirements docs, design specs, and acceptance criteria
- On-demand consultation during planning and refinement sessions
- Written sign-off on domain-sensitive deliverables

### Interactions with Existing Roles
| Role | Interaction |
|---|---|
| Product Manager | Validates problem statements, success metrics, and feature requirements |
| Project Manager | Clarifies scope boundaries and flags domain risks for the risk register |
| Developers | Reviews technical design choices and confirms implementation approach |

---

## Stakeholder Liaison

### Role Summary
The Stakeholder Liaison is the primary point of contact between the project team and external stakeholders, partners, or end users. They ensure communication is timely, accurate, and actionable in both directions.

### Responsibilities
- Maintain a stakeholder map and communication plan
- Produce and distribute stakeholder updates using the [Stakeholder Update Template](octoacme-stakeholder-update-template.md)
- Gather feedback and requirements from stakeholders and translate them for the project team
- Manage escalations, expectations, and relationship health

### Goals
- Prevent misalignment between the project team and stakeholders
- Ensure stakeholders have the information they need to make timely decisions
- Reduce escalations through proactive, transparent communication

### Typical Communication
- Regular stakeholder update reports (milestone- or cadence-based)
- Ad-hoc stakeholder feedback summaries shared with PM and PdM
- Escalation memos when decisions or approvals are blocked

### Interactions with Existing Roles
| Role | Interaction |
|---|---|
| Project Manager | Coordinates communication schedules; surfaces stakeholder-raised risks |
| Product Manager | Gathers stakeholder input on priorities, trade-offs, and acceptance criteria |
| Developers | Translates external feedback into actionable requirements or change requests |

---

## UX Designer

### Role Summary
UX Designers create user-centered workflows, wireframes, and prototypes that translate product requirements into intuitive experiences. They bridge user needs and technical implementation.

### Responsibilities
- Conduct user research and usability analysis
- Produce wireframes, mockups, and interactive prototypes
- Define and document interaction patterns and UX standards
- Collaborate in design reviews with engineering and product leads
- Validate usability through testing and iteration

### Goals
- Deliver experiences that are intuitive, accessible, and aligned with user needs
- Reduce design-related rework by involving stakeholders early
- Maintain design system consistency across the product

### Typical Communication
- Design reviews with Product Manager and Developers
- Usability test findings shared with PM and PdM
- Design handoff documentation (e.g., annotated specs, Figma links)

### Interactions with Existing Roles
| Role | Interaction |
|---|---|
| Product Manager | Translates product requirements into user experience goals and validates designs against success metrics |
| Project Manager | Ensures design milestones are reflected in the project plan |
| Developers | Provides design specifications and participates in implementation reviews to ensure fidelity |

---

## Quality Lead / QA Champion

### Role Summary
The Quality Lead (QA Champion) drives the quality agenda across the project lifecycle. They coordinate test planning, ensure adequate test coverage, and champion quality gates that prevent defects from reaching production.

### Responsibilities
- Define and maintain the [Quality Gates Checklist](octoacme-quality-gates-checklist.md)
- Coordinate test planning (unit, integration, end-to-end, regression)
- Track defect trends and test coverage metrics
- Review and sign off on release readiness from a quality perspective
- Promote quality engineering practices (TDD, code review standards, CI gating)

### Goals
- Prevent quality regressions from reaching production
- Build shared ownership of quality across the development team
- Make test results and quality signals visible to the entire team

### Typical Communication
- Quality reports shared with PM, PdM, and Release Manager
- Defect triage sessions with Developers
- Go/no-go input to Release Manager via the Release Readiness Checklist

### Interactions with Existing Roles
| Role | Interaction |
|---|---|
| Project Manager | Surfaces quality risks and test milestone status in project tracking |
| Product Manager | Validates that acceptance criteria are testable and complete |
| Developers | Defines test expectations and reviews coverage; drives defect resolution |
| Release Manager | Provides quality sign-off before each release |

---

## Role Interaction Map

This section provides a high-level view of how all roles interact across the project lifecycle.

### RACI Overview

| Activity | PM | PdM | Dev | Release Mgr | SME | Stakeholder Liaison | UX Designer | QA Champion |
|---|---|---|---|---|---|---|---|---|
| Define problem statement & success metrics | C | **R/A** | I | I | C | C | C | I |
| Prioritize backlog | C | **R/A** | C | I | C | I | C | I |
| Project planning & scheduling | **R/A** | C | C | C | I | I | I | C |
| Requirements validation | C | **R/A** | C | I | **R** | C | C | C |
| UX design & prototype | I | C | C | I | I | I | **R/A** | I |
| Feature implementation | I | C | **R/A** | I | C | I | C | C |
| Test planning & execution | C | C | C | I | I | I | I | **R/A** |
| Release readiness sign-off | C | C | C | **R/A** | I | I | I | R |
| Stakeholder communication | C | C | I | I | I | **R/A** | I | I |
| Risk management | **R/A** | C | C | C | C | C | I | C |
| Post-release review | **R/A** | C | C | R | I | C | I | C |

> **Key:** R = Responsible, A = Accountable, C = Consulted, I = Informed

### Lifecycle Touchpoints

| Phase | Key Roles Active |
|---|---|
| **Initiation** | Project Manager, Product Manager, Stakeholder Liaison, SME |
| **Planning** | Project Manager, Product Manager, Developers, UX Designer, SME, QA Champion |
| **Execution** | Developers, UX Designer, QA Champion, Project Manager, Product Manager |
| **Release** | Release Manager, QA Champion, Developers, Project Manager, Product Manager, Stakeholder Liaison |
| **Close & Retrospective** | All roles |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

