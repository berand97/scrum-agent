# Azure DevOps Integration

## Current Setup

- MCP server: `@azure-devops/mcp@2.9.0` (pinned: 2.10.0 crashes on Node 24 because of the native `keytar` module).
- Authentication: PAT, loaded from `D:\tech-and-solve\scrum-ia\.env` via `dotenv-cli`.
- Claude Code: `D:\tech-and-solve\scrum-ia\.mcp.json`.
- Claude Desktop (Microsoft Store): `%LOCALAPPDATA%\Packages\Claude_pzs8sxrjxfjjc\LocalCache\Roaming\Claude\claude_desktop_config.json`.

`.env` variables:

| Variable | Value |
|---|---|
| `PERSONAL_ACCESS_TOKEN` | base64 of `<email>:<pat>`, no quotes |
| `ado_mcp_project` | Default project (`Coomunion`) |
| `ado_mcp_team` | Default team (optional) |

## PAT Scopes

| Domain | Scope |
|---|---|
| core, work, work-items | Project and Team (Read), Work Items (Read & write) |
| repositories, search | Code (Read & write) |
| wiki | Wiki (Read & write) |
| pipelines | Build (Read & execute), Release (Read) |
| test-plans | Test Management (Read & write) |
| advanced-security | Advanced Security (Read) |

## Troubleshooting

| Symptom | Likely cause | Fix |
|---|---|---|
| `CONNECTION_CLOSED` on connect | Server crashes at startup (unpinned version, `keytar`) | Make sure the config uses `@azure-devops/mcp@2.9.0` |
| `Failed request: (401)` | PAT expired, not base64, or quoted | Regenerate the PAT and store it base64-encoded without quotes |
| `403` on a tool | PAT is missing that scope | Add the scope from the table above |
| Project or team not found | Different name | `core_list_projects` / `core_list_project_teams` |
