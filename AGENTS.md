# scrum-ia

Scrum assistant workspace connected to Azure DevOps (organization `berand97`, project `Coomunion`) through the `azure-devops` MCP server.

- For any Scrum or Azure DevOps request, use the `scrum-master` skill (`.agents/skills/scrum-master/SKILL.md`) and its `references/` files.
- Reply in the user's language (Spanish or English).
- Never read, print or commit `.env`: it holds the Azure DevOps PAT and is only consumed by the MCP server.
- If the `azure-devops` MCP tools are not available, say so; do not call the Azure DevOps REST API with the PAT as a workaround.
