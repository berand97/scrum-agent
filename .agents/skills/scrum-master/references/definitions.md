# Team Definitions

> Maintained by the Scrum Master. Adjust the lists to what the team agreed; items marked *(example)* are suggestions.

## Definition of Ready (DoR)

A user story may enter a sprint only if it meets **all** of these:

- [ ] Title follows the organization's naming rules.
- [ ] Description in "As a / I want / so that" format.
- [ ] At least 3 acceptance criteria in Gherkin.
- [ ] Estimated in story points (≤ 13).
- [ ] Has a parent Feature and a module tag.
- [ ] Dependencies identified (or "none").
- [ ] Design/UX attached when applicable. *(example)*
- [ ] Reviewed by the team in refinement.

When evaluating the DoR, report per story: meets / does not meet, and exactly what is missing.

## Definition of Done (DoD)

A user story moves to Done only if it meets **all** of these:

- [ ] All child tasks closed.
- [ ] Code reviewed (PR approved and merged). *(example)*
- [ ] Unit tests passing. *(example)*
- [ ] All test cases in the test plan are Passed.
- [ ] No open severity 1 or 2 bugs linked.
- [ ] Deployed to `<FILL IN: QA | Staging>`.
- [ ] Accepted by the Product Owner in the review.

If asked to move a story to Done and it does not meet the DoD, do not move it: list what is missing.

## Estimation

- Scale: Fibonacci 1, 2, 3, 5, 8, 13. *(example)*
- Reference story (3 points): `<FILL IN: ID and title>`
- Above 13 points → split before entering the sprint.
- Tasks: max 8 hours each. *(example)*

## Capacity

- Productive hours per person/day: `<FILL IN, e.g. 6>`
- Focus factor: `<FILL IN, e.g. 0.7>`
- Reference velocity: average of the last 3 closed sprints.

## Risk Criteria (for report alerts)

- Active item with no changes for more than 2 days. *(example)*
- Item tagged `BLOCKED`.
- Less than 50% of points closed after the sprint midpoint. *(example)*
- Open severity 1 bug in the sprint.
- Unassigned or unestimated items inside the sprint.
