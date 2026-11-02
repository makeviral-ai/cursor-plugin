# MakeViral MCP server: install guide for AI agents

MakeViral (https://www.makeviral.ai) finds the newest viral AI video trend templates on TikTok and Instagram Reels and makes them from the user's own photos. It also makes any AI image or video from a prompt.

This is a hosted remote MCP server. There is nothing to clone, build or install, and there is no API key.

- Transport: Streamable HTTP
- URL: `https://www.makeviral.ai/mcp`
- Auth: OAuth 2.1 (dynamic client registration and PKCE). `initialize`, `tools/list` and template browsing work without sign-in. Making videos and photos needs a MakeViral account with credits; the client opens the MakeViral sign-in in the browser when a tool needs the account.

## Cline

Add this entry to `cline_mcp_settings.json` (MCP Servers > Configure > Configure MCP Servers):

```json
{
  "mcpServers": {
    "makeviral": {
      "type": "streamableHttp",
      "url": "https://www.makeviral.ai/mcp",
      "disabled": false
    }
  }
}
```

Or open MCP Servers > Remote Servers, set the name to `makeviral` and the URL to `https://www.makeviral.ai/mcp`, then click Add Server.

## Other MCP clients

```json
{
  "mcpServers": {
    "makeviral": {
      "url": "https://www.makeviral.ai/mcp"
    }
  }
}
```

## Check the setup

Call `search_templates` (no sign-in needed). It returns the newest viral trend templates. Before `run_template`, `create_image` or `create_video`, confirm the template or model, the photos and the credit price with the user, because runs use credits from the user's MakeViral account.

Support: support@makeviral.ai
