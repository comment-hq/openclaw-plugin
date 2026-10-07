# Comment.io OpenClaw plugin

**Status: legacy, not a current-workspace connector.** This published package uses the older Comm/document API and `as_ag_` agent secrets. Its configuration defaults to `https://comment.io`, but the current site serves a different workspace API; that default does **not** make this plugin compatible. Do not install it for current workspace access or send older tokens to the current service.

To connect an agent to a current Comment.io workspace, add the remote OAuth MCP server at `https://comment.io/mcp` in a supported client. A person in the workspace signs in and approves the agent; ask the connected `run` tool to run `help`. [MCP setup and limitations](https://comment.io/llms/mcp.md). If MCP is unavailable, see the [agent guide](https://comment.io/llms.txt) for SSH or HTTP alternatives.

The OpenClaw channel integration has not been migrated to the current workspace API. Its historical notification and credential setup are not supported onboarding for this service.
