# Work Item Templates

Use these templates when creating or editing items in Azure DevOps. Apply the naming rules and work item language from `organization.md` (write the content in that language).
Azure DevOps HTML fields (Description, Acceptance Criteria, Repro Steps) accept basic HTML: use `<p>`, `<ul>`, `<ol>`, `<b>`.

## User Story

**Title:** `[MODULE] Verb + goal`

**Description**
```
As a <role>,
I want <action>,
so that <benefit>.

Context:
<why it is needed, relevant business rules>

Out of scope:
<what this story does not include>
```

**Acceptance Criteria** (at least 3 scenarios)
```
Scenario 1: <name>
  Given <context>
  When <action>
  Then <expected result>

Scenario 2: <alternate path>
  ...

Scenario 3: <error case>
  ...
```

**Fields:** Story Points, Priority, Area Path, Iteration Path, Tags (module), parent Feature.

## Task

**Title:** `[DEV|QA|UX|OPS] description`

**Description**
```
Goal: <what is delivered when the task is done>
Technical detail: <components, endpoints, tables affected>
Done when: <how it is verified>
```

**Fields:** Remaining Work (h), Activity, Assigned To, parent story.

## Bug

**Title:** `[BUG][MODULE] what fails`

**Repro Steps**
```
Environment: <DEV | QA | PROD> — version/build <n>
User/role: <...>

Steps:
1. ...
2. ...

Actual result: <...>
Expected result: <...>
Evidence: <screenshot, log, transaction ID>
```

**Fields:** Severity, Priority, Found In (build), parent story or `PROD` tag.

## Test Plan

- **Name:** `TP - Sprint <n> - <Team>`
- **Iteration:** the sprint's iteration.
- **Suites:** one requirement-based suite per sprint user story.

## Test Case

**Title:** `TC - <Story ID> - <scenario>`

**Steps** (one per row):

| # | Action | Expected result |
|---|---|---|
| 1 | <user action> | <what should happen> |
| 2 | ... | ... |

- **Preconditions:** test data, user, environment.
- **Link:** "Tested By" to the story.
- One test case per acceptance-criteria scenario.

## Confirmation Summary (before creating)

Before writing to Azure DevOps, show this table and wait for confirmation:

| # | Type | Title | Parent | Key fields |
|---|---|---|---|---|
| 1 | User Story | ... | Feature #... | SP=5, Tags=... |
| 2 | Task | ... | Story (1) | RW=4h, Activity=Development |
