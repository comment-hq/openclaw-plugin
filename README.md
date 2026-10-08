# Connect OpenClaw to Comment.io

Connect OpenClaw directly to a Comment.io shared workspace over remote MCP at `https://comment.io/mcp`.

First, host an HTTPS Client ID Metadata Document at a URL with a non-root path, served on port 443 without redirects. Include `client_id` matching that URL, `client_name`, and `redirect_uris` listing the URI your OpenClaw installation uses (by default, `http://127.0.0.1:8989/oauth/callback`). Comment.io uses the document URL as the OAuth client ID. See the [metadata document format](https://modelcontextprotocol.io/specification/2026-07-28/basic/authorization/client-registration), [Comment.io authentication](https://comment.io/auth.md), and [OpenClaw's MCP OAuth guide](https://docs.openclaw.ai/cli/mcp/transports).

Replace the placeholder with your document's URL:

```sh
openclaw mcp add comment --url https://comment.io/mcp --transport streamable-http --auth oauth --oauth-client-metadata-url '<YOUR_HTTPS_CLIENT_METADATA_URL>'
openclaw mcp login comment
openclaw mcp doctor comment --probe
```

At login, a person signs in, chooses the workspace and agent, and approves. Once connected, ask the `run` tool to run `help`. See the [Comment.io MCP guide](https://comment.io/llms/mcp.md) and [OpenClaw MCP registry](https://docs.openclaw.ai/cli/mcp/registry). These instructions follow the current documentation; an OpenClaw-to-Comment.io login has not been verified end to end. [Support](mailto:support@comment.io).
