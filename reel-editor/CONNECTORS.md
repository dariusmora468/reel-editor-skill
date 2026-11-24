# The two connectors

Optional, but they make the reel editor better:

- **Apify** grabs your reference reels when Instagram blocks your AI from downloading them.
  Server URL: `https://mcp.apify.com` (sign in with an Apify account)
- **Higgsfield** makes any image, graphic or video clip the edit needs.
  Server URL: `https://mcp.higgsfield.ai/mcp` (sign in with a Higgsfield account, needs a paid Higgsfield plan)

## Claude Code (easiest: let it do it)

Paste this into Claude Code:

> Connect the Apify MCP server at https://mcp.apify.com and the Higgsfield MCP server at
> https://mcp.higgsfield.ai/mcp, then walk me through signing in to both.

Or do it yourself in a terminal:

```
claude mcp add --transport http apify https://mcp.apify.com
claude mcp add --transport http higgsfield https://mcp.higgsfield.ai/mcp
```

Then open Claude Code, type `/mcp` and sign in to each.

## Codex (ChatGPT desktop app, CLI or IDE)

Paste the same prompt into Codex and let it do it. Or by hand in the app: Settings > MCP servers > Add server.
Name it Apify, pick Streamable HTTP, paste `https://mcp.apify.com`, save, then Restart and Authenticate.
Do the same for Higgsfield with `https://mcp.higgsfield.ai/mcp`.

Or in a terminal (the app, CLI and IDE share this config):

```
codex mcp add apify --url https://mcp.apify.com
codex mcp add higgsfield --url https://mcp.higgsfield.ai/mcp
codex mcp login apify
codex mcp login higgsfield
```

## Claude app (claude.ai or the desktop app)

Settings > Connectors > Add custom connector. Name it Apify, paste `https://mcp.apify.com`, Connect, sign in.
Do the same for Higgsfield with `https://mcp.higgsfield.ai/mcp`.
