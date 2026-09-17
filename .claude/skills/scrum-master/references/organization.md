# How the Organization Uses Azure DevOps

> Maintained by the Scrum Master. Replace every `<FILL IN>` with the real value.
> While a value says `<FILL IN>`, ask the user instead of assuming.
> Values marked *(example)* are suggestions: confirm or change them.

## Context

- Organization: `berand97` (https://dev.azure.com/berand97)
- Main project: `Coomunion`
- Other projects: `SGFI`
- Azure DevOps process: `<FILL IN: Scrum | Agile | CMMI | custom>`
- Work item language (titles, descriptions, test cases): `<FILL IN: Spanish | English>`
- Teams:

| Team | Area path | Scrum Master | Product Owner |
|---|---|---|---|
| `<FILL IN>` | `Coomunion\<FILL IN>` | `<FILL IN>` | `<FILL IN>` |

## Work Hierarchy

Epic → Feature → User Story → Task *(example)*

- Every user story must have a parent Feature. *(example)*
- Bugs found during the sprint are created as children of the affected story. *(example)*
- Production bugs go to the backlog with the `PROD` tag. *(example)*

## Sprints

- Length: `<FILL IN>` weeks, starting on `<FILL IN: weekday>`.
- Iteration naming: `Coomunion\<FILL IN: format, e.g. 2026\Sprint 18>`.
- Ceremonies:

| Ceremony | Day / time | Duration |
|---|---|---|
| Planning | `<FILL IN>` | `<FILL IN>` |
| Daily | `<FILL IN>` | 15 min |
| Refinement | `<FILL IN>` | `<FILL IN>` |
| Review + Retro | `<FILL IN>` | `<FILL IN>` |

## States and Meaning

| State | Meaning | Who moves it |
|---|---|---|
| New | Created, not refined | PO *(example)* |
| Approved | Meets the DoR | Team during refinement *(example)* |
| Committed | Committed to the sprint | Team during planning *(example)* |
| Done | Meets the DoD | QA *(example)* |

## Required Fields

| Type | Field | Rule |
|---|---|---|
| User Story | Story Points | Fibonacci 1, 2, 3, 5, 8, 13; above 13 must be split *(example)* |
| User Story | Acceptance Criteria | Gherkin, at least 3 scenarios *(example)* |
| User Story | Tags | System module (see allowed tags) *(example)* |
| Task | Remaining Work | Hours, max 8 per task *(example)* |
| Task | Activity | Development / Testing / Design / Deployment *(example)* |
| Bug | Severity | 1 - Critical to 4 - Low *(example)* |
| Bug | Repro Steps | Required, per template *(example)* |

## Naming

- User story: `[MODULE] Verb + goal` → `[LOANS] View member balance` *(example)*
- Task: `[DEV|QA|UX|OPS] description` → `[QA] Balance API integration tests` *(example)*
- Bug: `[BUG][MODULE] what fails` *(example)*
- Test plan: `TP - Sprint <n> - <Team>` *(example)*
- Test case: `TC - <Story ID> - <scenario>` *(example)*
- Branches: `feature/<StoryID>-short-description` *(example)*

## Testing

- One test plan per sprint; one requirement-based suite per user story. *(example)*
- Every acceptance criterion has at least one test case. *(example)*
- Test cases are linked to the story with "Tested By". *(example)*

## Allowed Tags

- Status / type: `PROD`, `BLOCKED`, `TECH-DEBT`, `SPIKE` *(example)*
- Modules: `<FILL IN: list of system modules>`
- No new tags without PO approval. *(example)*

## Never Do

- Do not move items to Done without QA evidence. *(example)*
- Do not change story points after planning. *(example)*
- Do not create items outside the team's area path. *(example)*
- Do not delete work items; close them with reason `Removed`. *(example)*

## Reports

| Report | Audience | When | Content |
|---|---|---|---|
| Weekly status | `<FILL IN>` | `<FILL IN>` | Progress %, risks, blockers, open PROD bugs *(example)* |
| Sprint close | `<FILL IN>` | Last day of sprint | "Sprint Report Template" in SKILL.md *(example)* |

General format: a table plus 3 bullet-point conclusions. *(example)*
