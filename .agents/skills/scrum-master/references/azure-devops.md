# Using the azure-devops MCP Server

Tools are exposed as `mcp__azure-devops__*`. Exact names may vary by server version; check the available tools.

## Rules

1. **Real data only.** If a tool fails or returns nothing, show the error; never fill gaps with assumptions.
2. **Confirm before writing.** Before creating, updating, linking, reordering or commenting on work items, creating iterations or test plans, changing capacity, running pipelines, or touching PRs/wiki: show the confirmation table from `templates.md` (or ID, field, current → new value) and wait for an explicit yes.
3. **Default context.** Organization `berand97`, project `Coomunion` (see `organization.md`). If the team is ambiguous, list teams and ask.
4. **Links.** Cite every item as `#ID Title` with URL `https://dev.azure.com/berand97/<project>/_workitems/edit/<ID>`.
5. **Batch reads.** Prefer WIQL and `get_batch` over reading items one by one.

## Key Tools

| Need | Tool (action) |
|---|---|
| Projects / teams / identities | `core_list_projects`, `core_list_project_teams`, `core_get_identity_ids` |
| Current sprint, iterations, settings | `work` (`list_team_iterations`, `get_team_settings`) |
| Capacity | `work` (`get_team_capacity`, `get_iteration_capacities`), `work_capacity_write` |
| Sprint items | `wit_work_item` (`list_for_iteration`, `get_batch`) |
| Queries | `wit_query` (`wiql`, `get_results`) |
| Backlog | `wit_backlog` (`list`, `list_work_items`, `reorder`) |
| Create / edit items | `wit_work_item_write` (`create`, `update`, `update_batch`, `add_child`) |
| Comments and links | `wit_work_item_comment_write`, `wit_work_item_link_write` |
| History | `wit_work_item` (`list_revisions`, `list_comments`) |
| Process types and fields | `wit_work_item` (`get_type`) |
| Test plans | `testplan` (`list_plans`, `list_suites`, `list_cases`), `testplan_test_plan_write`, `testplan_test_suite_write`, `testplan_test_case_write` |
| PRs and builds | `repo_pull_request`, `pipelines_build` |
| Wiki | `wiki`, `wiki_upsert_page` |
| Search | `search_workitem`, `search_wiki`, `search_code` |

## Useful WIQL

```sql
-- Current sprint items for a team
SELECT [System.Id], [System.Title], [System.State], [System.AssignedTo]
FROM WorkItems
WHERE [System.TeamProject] = @project
  AND [System.IterationPath] = @currentIteration('[Coomunion]\<team>')
ORDER BY [Microsoft.VSTS.Common.BacklogPriority]

-- Active items with no changes in 2 days
SELECT [System.Id], [System.Title], [System.AssignedTo], [System.ChangedDate]
FROM WorkItems
WHERE [System.TeamProject] = @project
  AND [System.State] = 'Active'
  AND [System.ChangedDate] < @today - 2

-- Blocked items
SELECT [System.Id], [System.Title], [System.AssignedTo]
FROM WorkItems
WHERE [System.TeamProject] = @project
  AND [System.Tags] CONTAINS 'BLOCKED'
  AND [System.State] <> 'Done'
```

State and type names depend on the process. If a query returns nothing, verify names with `get_type` before concluding there is no data.
