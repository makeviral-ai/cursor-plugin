# MakeViral

Cursor plugin and Gemini CLI extension that connect agents to [MakeViral](https://www.makeviral.ai) through its official remote [Model Context Protocol](https://modelcontextprotocol.io/) server.

Find the newest viral AI video trend templates from TikTok and Instagram Reels, and make them from your own photos. Agents can also create AI images and videos from a prompt.

## Install

1. Open **Cursor Settings → Plugins**.
2. Search for **MakeViral**.
3. Click **Install**. Browsing templates works without sign-in; sign in to MakeViral when you start a run.

Or run `/add-plugin makeviral` in chat.

## Gemini CLI

```bash
gemini extensions install https://github.com/makeviral-ai/cursor-plugin
```

The extension adds the MakeViral remote MCP server (`https://www.makeviral.ai/mcp`) and a short `GEMINI.md` context file. Gemini CLI opens the MakeViral sign-in the first time a tool needs your account. Update with `gemini extensions update makeviral`.

## MCP

```json
{
  "mcpServers": {
    "makeviral": {
      "type": "http",
      "url": "https://www.makeviral.ai/mcp"
    }
  }
}
```

Auth is OAuth 2.1 with PKCE and Dynamic Client Registration. Cursor registers itself and opens the MakeViral sign-in when a tool needs your account. There is no API key to configure.

## What agents can do

| Category | Capabilities |
| --- | --- |
| Trend templates | Search and show the newest viral templates, with example clips and credit prices |
| Runs | Run a template with your photos (photo upload link included) |
| Create | Make AI images and videos from a prompt |
| Creations | Check the status of a job and list your creations |
| Account | Show your credit balance |

Runs use credits from your MakeViral account. The hosted server is the source of truth for tool names and schemas.

## Support

support@makeviral.ai
