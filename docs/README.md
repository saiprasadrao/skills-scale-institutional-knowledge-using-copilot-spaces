# OctoAcme Project Management Docs

This README provides a summary of project management processes and links to all process docs used by OctoAcme.

## Summary of Project Management Processes

OctoAcme follows a structured five-phase project lifecycle—Initiation, Planning, Execution, Release, and Close & Retrospective—with clearly defined deliverables and decision gates. Each phase is designed to validate assumptions early, maintain stakeholder alignment, and reduce rework. During Initiation, teams create a lightweight Project One-pager that establishes success metrics, identifies stakeholders, and estimates resources. Planning transforms approved initiatives into actionable backlogs by decomposing work into shippable increments, estimating scope, and identifying cross-team dependencies. This deliberate gating process ensures that only well-defined work enters execution.

OctoAcme operates with clear role definition and a regular communication cadence. Project Managers coordinate delivery, manage risks and dependencies, and ensure transparent communication; Product Managers define outcomes, prioritize backlogs, and measure success; Developers implement features and participate in design and quality activities; and QA/Testing validates acceptance criteria. The communication rhythm includes daily standups (15 minutes), weekly syncs between PM and Product Manager, twice-weekly standups for delivery teams, and monthly stakeholder updates. Issues escalate systematically—from team-level triage to sponsor-level escalation for business-impacting concerns—enabling rapid resolution and maintaining alignment across the organization.

During Execution, OctoAcme enforces disciplined workflows with small pull requests (≤400 lines), mandatory CI testing and linting, and at least one approval before merging. Quality is embedded through unit tests, integration tests, end-to-end smoke tests, and security scanning. Work progresses through a project board (Backlog → Ready → In Progress → In Review → QA → Done), providing visibility and preventing bottlenecks. Risk management is formalized through a Risk Register that tracks impact, likelihood, mitigation plans, and status, with weekly review during syncs. This integrated approach to execution, quality, and risk management reduces production incidents and technical debt.

Release and Deployment are standardized with clear pre-release requirements (acceptance criteria met, CI passing, security scans clean, release notes drafted, rollback plans documented). After each sprint, release, or incident, teams conduct blameless retrospectives (45–75 minutes) to capture learnings and prioritize 2–3 actionable improvements. Action items are tracked in the project backlog with clear owners and due dates, creating a continuous improvement cycle. This structured approach balances speed with reliability while building organizational learning into the project rhythm.

## Process Docs

- [Project Management Overview](./octoacme-project-management-overview.md)
- [Project Initiation Guide](./octoacme-project-initiation.md)
- [Project Planning](./octoacme-project-planning.md)
- [Execution & Tracking](./octoacme-execution-and-tracking.md)
- [Risk Management & Communication](./octoacme-risks-and-communication.md)
- [Release & Deployment Guide](./octoacme-release-and-deployment.md)
- [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)
- [Roles and Personas](./octoacme-roles-and-personas.md)
