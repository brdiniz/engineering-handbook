# 06. Engineering metrics and KPIs

**Purpose:** give teams and leadership a shared, honest view of delivery, quality and team health, and a way to connect team goals to company goals.

## 1. Rules for using metrics

1. **Measure systems and teams, never individuals.** Individual output metrics (commits, lines, tickets, story points) are easy to game and damage collaboration.
2. **Use metrics to ask questions, not to deliver verdicts.** A change in a number starts a conversation.
3. **Pair metrics so they balance each other.** Speed with quality, output with sustainability.
4. **Track trends, not single points.** Look at the direction over several weeks.
5. **Keep the set small.** A handful of metrics that people understand beats a dashboard nobody reads.
6. **Agree definitions first.** "Deployment", "failure" and "incident" mean the same thing for everyone.

## 2. Delivery metrics (the DORA set)

These four measures of software delivery performance come from the DORA research programme.

| Metric | Definition | Why it matters |
|---|---|---|
| Deployment frequency | How often you deploy to production | A proxy for batch size and flow |
| Lead time for changes | Time from commit to running in production | How quickly you can deliver value or a fix |
| Change failure rate | Share of deployments that cause a failure needing remediation | Quality of the release process |
| Time to restore service | How long it takes to recover from a failure in production | Resilience |

DORA's published guidance evolves, so check its current definitions and any added measures (such as rework rate) before you set targets.

**Setting targets:** start by measuring for a quarter to find your baseline, then aim to improve the trend. External benchmarks give context, but your own trajectory matters more.

## 3. Quality and reliability metrics

| Metric | Definition | Notes |
|---|---|---|
| Availability or SLO attainment | Share of time (or requests) meeting the service level objective | Define per service and tie to customer promises |
| Incident count by severity | Number of SEV1 and SEV2 incidents per period | Look at trend and causes, not just totals |
| Mean time to detect | Time from the start of an incident to detection | Shows monitoring quality |
| Escaped defects | Bugs found by customers versus found internally | Shows test effectiveness |
| Bug backlog age | Age distribution of open bugs by priority | Healthy teams close important bugs fast |
| Postmortem action completion | Share of actions closed on time | Shows whether learning leads to change |

## 4. Team health metrics

| Metric | How to gather it |
|---|---|
| Engagement and satisfaction | Short, regular surveys (quarterly), with questions about clarity, autonomy, workload and tooling |
| Sustainable pace | On-call load, after-hours work, and a team-level view of overtime |
| Onboarding time | Time for a new joiner to ship a first production change |
| Retention | Regretted attrition by team, with exit and stay interviews |
| Developer experience | Build time, CI wait time, flaky test rate and survey feedback |

## 5. Product and outcome metrics

Engineering delivers outcomes, so each team also tracks one or two measures that connect to what customers value, agreed with product: adoption of a feature, task success rate, performance perceived by users, support tickets about an area.

## 6. Cascading goals

Link company goals to team goals so every team can see its contribution.

```text
Company goal            Reduce customer-reported problems by 30%
  Engineering goal      Improve production quality and incident response
    Team goal           Cut escaped defects in the billing service by 40%
      Key results       - Add contract tests for all billing APIs
                        - Reduce time to restore for billing incidents to under 30 minutes
                        - Close all P1 and P2 bugs within agreed time
```

Keep each team to two or three goals per quarter, each with a measurable key result and a named owner.

## 7. A starter scorecard

| Area | Metric | Baseline | Target | Trend |
|---|---|---|---|---|
| Delivery | Deployment frequency | | | |
| Delivery | Lead time for changes | | | |
| Quality | Change failure rate | | | |
| Reliability | Time to restore | | | |
| Reliability | SLO attainment | | | |
| Quality | Escaped defects | | | |
| People | Engagement score | | | |
| People | After-hours pages per shift | | | |

Review monthly with the team, and quarterly with leadership.

## 8. Common anti-patterns

- Comparing teams on raw numbers when their contexts differ
- Using velocity (story points) as a performance target, which inflates estimates and says nothing about value
- Rewarding bug counts or ticket closure, which encourages splitting and hiding work
- Measuring activity (hours, commits) instead of outcomes
- Setting a target and then ignoring the cost to quality or team health
- Collecting metrics nobody uses

## 9. Changelog

| Date | Change | Reason |
|---|---|---|
| YYYY-MM-DD | Initial version | |
