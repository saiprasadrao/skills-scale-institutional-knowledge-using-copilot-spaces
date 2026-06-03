# Decision Log Template

This template standardizes how OctoAcme documents key project decisions. Using a consistent format improves traceability, onboarding, and retrospective analysis.

## How to Use This Template

1. **Create a decision log** in your project repository or wiki (e.g., `docs/DECISIONS.md`)
2. **Add an entry for each significant decision** during Initiation, Planning, Execution, or Release phases
3. **Update the status** as decisions are implemented or revisited
4. **Reference decisions** in issue descriptions, PR comments, and retrospectives

---

## Decision Log Entry Template

### Decision: [Clear, concise title]

**Date:** YYYY-MM-DD  
**Decision Owner:** [Role/Name]  
**Status:** [Approved | Implemented | Revisited | Superseded]  
**Context:** [Link to related issue, spec, or discussion]  

**Problem / Question:**
What decision needed to be made and why?

**Options Considered:**
1. Option A: [Description] — Pros: [list] | Cons: [list]
2. Option B: [Description] — Pros: [list] | Cons: [list]
3. (Add more options if needed)

**Decision:**
Which option was chosen and why?

**Rationale:**
Key reasoning and trade-offs that led to this decision.

**Stakeholders & Approvals:**
- [ ] Product Manager approval
- [ ] Technical Lead approval
- [ ] Project Manager sign-off
- [ ] Other: ________________

**Implementation Notes:**
- Who is responsible for implementation?
- What is the timeline?
- Are there dependencies or follow-up decisions?

**Reversibility:**
How easily can this decision be reversed or changed?
- **High reversibility:** Can be changed with limited rework
- **Medium reversibility:** Requires some rework or coordination
- **Low reversibility:** Would require significant rework or affect downstream decisions

**Follow-up Review:**
Scheduled review date: [YYYY-MM-DD] (optional)  
Review notes: [Add after review]

---

## Example Decision Log Entry

### Decision: Adopt PostgreSQL for primary database

**Date:** 2024-01-15  
**Decision Owner:** Technical Lead  
**Status:** Implemented  
**Context:** [Link to architecture discussion #42](./architecture-decisions.md)

**Problem / Question:**
Which relational database should we use for the core application? The team needed to align on a database technology that balances performance, cost, and team expertise.

**Options Considered:**
1. PostgreSQL: Industry-standard, open-source, strong ecosystem — Pros: Robust, well-documented, strong JSON support | Cons: Requires infrastructure expertise
2. MySQL: Lightweight, simpler ops — Pros: Easier ops, lower resource overhead | Cons: Less feature-rich, slower for complex queries
3. Cloud-managed (e.g., AWS RDS): Minimal ops overhead — Pros: Managed backup/recovery, scaling | Cons: Vendor lock-in, higher cost

**Decision:**
PostgreSQL with managed hosting (AWS RDS).

**Rationale:**
PostgreSQL offers the feature set and query performance needed for our use cases. AWS RDS eliminates operational overhead while keeping us flexible. The team has prior experience, reducing ramp-up time.

**Stakeholders & Approvals:**
- [x] Product Manager approval (PdM confirmed performance requirements met)
- [x] Technical Lead approval (TL confirmed team readiness)
- [x] Project Manager sign-off (PM confirmed cost and timeline impact)

**Implementation Notes:**
- Technical Lead is responsible for database schema design and optimization
- Timeline: Database provisioned by sprint 2, application integration complete by sprint 4
- Dependency: Must complete security audit of AWS account before production deployment

**Reversibility:**
Medium reversibility. Changing databases mid-project would require schema migration and application refactoring, but is not architecturally blocked.

**Follow-up Review:**
Scheduled review date: 2024-06-15 (post-launch review of performance and cost)  
Review notes: [To be added after launch]

---

## Integration with Other Processes

- **Project Initiation:** Document high-level strategic decisions (tech stack, platform choices)
- **Project Planning:** Document scope, timeline, and resource allocation decisions
- **Execution:** Document design, implementation, and trade-off decisions
- **Release:** Document deployment and release strategy decisions
- **Retrospective:** Review reversibility and impact of decisions; capture lessons learned

## Best Practices

1. **Timely Documentation:** Log decisions when made, not after the fact
2. **Involve Stakeholders:** Ensure all affected parties understand and approve major decisions
3. **Capture Rationale:** Future team members will thank you for clear reasoning
4. **Link to Context:** Always link to related issues, specs, or design docs
5. **Review & Learn:** Use the decision log in retrospectives to evaluate decision quality
6. **Revisit When Needed:** Mark decisions that are revisited or superseded; explain why

## Example Decision Log Format in Project README

```markdown
## Key Decisions

See [DECISIONS.md](./DECISIONS.md) for the full decision log, including:
- Database technology selection
- Authentication and authorization approach
- API design and versioning strategy
- CI/CD pipeline architecture
- Deployment strategy and rollback procedures
```