# 07. Tech lead role

**Purpose:** clarify what a tech lead owns, how it differs from an engineering manager, and how to assess whether it is going well.

## 1. What a tech lead is

A tech lead is a Senior or Staff Engineer who is accountable for the **technical direction and delivery quality** of one team's work. It is a role, not a level and not a management position. The tech lead usually still writes code, spending a meaningful share of time on it.

## 2. Tech lead and engineering manager

| Area | Tech lead | Engineering manager |
|---|---|---|
| Technical direction and architecture | Owns | Challenges and supports |
| Delivery planning and technical risk | Owns the technical plan | Owns capacity, priorities and stakeholders |
| Code and design review standards | Owns | Supports |
| Hiring | Interviews, assesses technical skill | Owns the process and the decision |
| Performance and career growth | Gives input, mentors | Owns |
| Team health and process | Contributes | Owns |

The two roles work as a pair. Agree on who decides what, and write it down.

## 3. Responsibilities

**Technical direction**
- Keeps an architecture view of the team's systems and records significant decisions in ADRs or RFCs
- Breaks down large work into deliverable slices with sound technical sequencing
- Identifies and manages technical risks and dependencies early

**Delivery and quality**
- Sets and upholds standards for design, testing, review and operations
- Ensures the team ships safely: reviews, CI, release readiness, rollback plans
- Takes part in incident response for the team's services and drives follow-up actions

**People and culture**
- Mentors engineers, pairs on hard problems and gives actionable feedback
- Creates room for others to lead designs and decisions, rather than deciding everything
- Helps new joiners become productive quickly

**Collaboration**
- Works with product on feasibility, scope and trade-offs
- Coordinates with other tech leads on shared systems and interfaces
- Communicates technical status clearly to non-technical stakeholders

## 4. What a tech lead is not

- A bottleneck for every decision
- The person who must write the hardest code
- A project manager
- Responsible for HR matters

## 5. Assessing a tech lead

Use team-level outcomes and observable behaviours. Review each half-year.

| Area | Questions | Example evidence |
|---|---|---|
| Technical decisions | Are decisions sound, documented and understood? | ADRs, design reviews, fewer reversals |
| Delivery | Does the team ship predictably and safely? | Lead time and change failure trends, on-time delivery of committed work |
| Quality | Is the team's production health improving? | Incident trend, escaped defects, SLO attainment |
| Growth of others | Are teammates growing and taking more ownership? | Engineers leading designs, promotion evidence, feedback |
| Collaboration | Do product and other teams trust the lead? | Stakeholder feedback, smooth cross-team work |
| Sustainability | Is the pace healthy? | On-call load, team survey results |

## 6. Example goals for a half-year

| Goal | Key results |
|---|---|
| Improve release safety | Change failure rate below an agreed level; automated rollback for the main service |
| Reduce time to restore | Time to restore for SEV2 incidents reduced by a set percentage; runbooks for the top five alerts |
| Raise design quality | Every cross-team change has an RFC; two engineers lead a design for the first time |
| Strengthen onboarding | New joiner ships a first production change within a target number of days |

## 7. Rotation and transition

- Consider rotating the tech lead role every one to two years to spread experience and avoid burnout
- Plan handovers deliberately: overlap, documented decisions and an announced change
- Moving out of the role is not a demotion; say so explicitly

## 8. Changelog

| Date | Change | Reason |
|---|---|---|
| YYYY-MM-DD | Initial version | |
