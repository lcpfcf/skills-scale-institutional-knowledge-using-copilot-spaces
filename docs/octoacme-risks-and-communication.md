# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Roles in Risk & Communication

| Role | Responsibility |
|---|---|
| **Project Manager** | Maintains the risk register; facilitates risk reviews; owns escalation paths |
| **Stakeholder Liaison** | Translates project risks into stakeholder-appropriate communication; distributes updates |
| **Product Manager** | Provides business impact assessment for risks; approves risk waivers |
| **QA Champion** | Raises quality-related risks; tracks defect trends as leading indicators |
| **Release Manager** | Owns release-specific risks; maintains rollback and incident plans |

> See [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) for full role definitions.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
- The **Stakeholder Liaison** owns the stakeholder communication plan and is responsible for distributing timely updates.
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based) using the [Stakeholder Update Template](octoacme-stakeholder-update-template.md)
- Use a single source of truth (project README or release doc) for status

## Communication Templates
Use the [Stakeholder Update Template](octoacme-stakeholder-update-template.md) for regular project status communications. It covers:
- Executive summary with status indicator (🟢/🟡/🔴)
- Progress this period, upcoming milestones, risks, decisions needed, and next steps

Weekly Status Template (lightweight, for internal team):
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

Incident Communication
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call
