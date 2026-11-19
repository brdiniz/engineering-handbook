# 04. On-call

**Purpose:** make sure someone can respond to production problems at any time, without burning people out.

## 1. Principles

- On-call is a shared responsibility of the engineers who build and run the service.
- It must be sustainable. If on-call is regularly painful, fix the system, not the people.
- Fairness matters: rotate evenly, compensate it, and protect rest.
- Alerts must be actionable. Every page needs a human to do something now.

## 2. Rotation design

| Choice | Default | Notes |
|---|---|---|
| Rotation length | 1 week | Shorter handovers lose context, longer ones tire people |
| Minimum rotation size | 5 engineers | Smaller groups mean on-call too often; consider a shared rotation across teams |
| Roles | Primary and secondary | Secondary is the backup if primary does not acknowledge in time |
| Escalation | Primary, then secondary, then engineering manager | Define time limits (for example 10 minutes) |
| Follow-the-sun | Optional | Use when you have teams in distant time zones; avoids night pages |
| Shadowing | New joiners shadow at least one rotation before taking the pager | |

Check local employment law and contracts for rules on on-call pay, rest periods and working time.

## 3. Expectations

**During a shift, the primary:**
- Keeps their laptop and phone available and can respond within the agreed time
- Acknowledges pages promptly and declares an incident if needed (see [incident response](03-incident-response.md))
- Escalates early when stuck; asking for help is expected
- Keeps notes of anything unusual for the handover

**The team:**
- Does not schedule the on-call engineer for heavy project work during the shift
- Gives time off in lieu or equivalent rest after a night-time incident

## 4. Handover

At the end of each shift, the outgoing and incoming engineers meet for 15 minutes and cover:
- Incidents and near misses
- Open issues and flaky alerts
- Planned changes in the coming week
- Anything unusual about the systems

## 5. Alert hygiene

- Every alert links to a runbook or states the first diagnostic step
- Page only on symptoms that affect customers or are about to (error rate, latency, saturation, failed jobs), not on every cause
- Track pages per shift, pages outside working hours and false-positive rate
- Review them monthly. A healthy target is that a typical shift has few pages and almost no night pages; set your own thresholds and act when they are exceeded
- Delete or downgrade alerts nobody acts on

## 6. Runbooks

Each runbook should have:
- What the alert means and how serious it is
- How to check the situation (commands, dashboards)
- Safe mitigations, in order
- When and whom to escalate to
- Links to relevant architecture notes

Keep runbooks next to the code or in a searchable wiki, and fix them whenever they mislead someone.

## 7. Metrics to review monthly

| Metric | Why it matters |
|---|---|
| Pages per shift | Load on the on-call engineer |
| Pages outside working hours | Sleep and burnout risk |
| Time to acknowledge | Whether the rotation is responsive |
| Repeat alerts | Missing automation or fixes |
| Share of pages with a runbook | Documentation coverage |
