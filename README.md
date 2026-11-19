# engineering-handbook

An open, adaptable engineering handbook for software teams of roughly 5 to 50 engineers: how work flows from idea to production, how incidents are handled, how people grow, and how a team measures itself without gaming the numbers.

Everything is written to be copied into your own wiki and edited. It is deliberately opinionated, because a handbook that lists every option helps nobody on a bad day. Where a choice depends on your context, the text says so.

## Contents

| Document | Use it to |
|---|---|
| [01 Software development lifecycle](handbook/01-sdlc.md) | Agree how work moves from idea to production, with quality gates |
| [02 Code review](handbook/02-code-review.md) | Keep reviews fast, kind and useful |
| [03 Incident response](handbook/03-incident-response.md) | Run incidents with clear severity, roles and communication |
| [04 On-call](handbook/04-on-call.md) | Set up a sustainable on-call rotation |
| [05 Career ladder](handbook/05-career-ladder.md) | Define levels, expectations and promotion evidence |
| [06 Engineering metrics and KPIs](handbook/06-engineering-metrics.md) | Measure delivery, quality and team health, and cascade goals |
| [07 Tech lead role](handbook/07-tech-lead-role.md) | Clarify what a tech lead owns and how to assess one |

Templates are in [templates/](templates/): [RFC](templates/rfc.md), [postmortem](templates/postmortem.md) and [incident status update](templates/incident-status-update.md).

## How to adopt it

1. **Start with one document**, usually incident response or the SDLC, whichever hurts more today.
2. **Fork and edit.** Replace the example thresholds and names with yours.
3. **Run it for a quarter**, then review what people ignored or worked around. Those are the parts to simplify.
4. **Keep a changelog** at the top of each document so people can see what changed and why.

## Principles

- **Defaults over rules.** Set sensible defaults and require a written reason to deviate.
- **Small batches.** Smaller changes ship faster, fail more safely and are easier to review.
- **Blameless by design.** Failures are system problems; we fix the system.
- **Measure to learn, not to rank.** Metrics describe teams and systems, never individuals.
- **Write it down.** Decisions, runbooks and expectations live in documents anyone can find.

## Caveats

These documents are starting points drawn from common industry practice. They are not legal, HR or compliance advice. Review the career ladder and any performance process with your HR and legal advisers before use, and adapt on-call and incident practices to your regulatory environment.

## Contributing

Pull requests that make the documents clearer, shorter or more broadly applicable are welcome. Please keep examples free of employer, customer or personal specifics.

## Working with me

I help engineering leaders structure teams, define levels and metrics, and set up incident and delivery practices. Contact: <your-email-or-booking-link>

## License

MIT. See [LICENSE](LICENSE).
