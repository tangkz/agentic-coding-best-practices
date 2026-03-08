# MCP Grounding Rules

## Knowledge Acquisition
- The agent MUST check for relevant Knowledge Items (KIs) or documentation before starting research.
- Hallucinations regarding API names or parameters are strictly forbidden; use MCP tools to verify.

## Tool Usage
- Use MCP servers whenever possible over manual searching.
- Maintain a log of all MCP queries and their results in `.tmp/mcp_log.json`.

## Documentation
- Every code change must include comments citing the source of the logic (e.g., "Field mapping based on BigQuery schema: order_v2").
