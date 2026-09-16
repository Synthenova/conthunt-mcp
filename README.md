# ContHunt

Public plugin pack for ContHunt. The MCP server is hosted — this repo is the storefront (name, dark logo, skill, and the URL clients install).

```text
https://mcp.conthunt.app/
```

Streamable HTTP + OAuth 2.1 PKCE. No local process. Product: [conthunt.app](https://conthunt.app). Docs: [conthunt.app/docs/integrations/mcp](https://conthunt.app/docs/integrations/mcp).

## Cursor

Add this GitHub repo as a plugin (`Synthenova/conthunt-mcp`). Cursor reads `.cursor-plugin/` plus `mcp.json` and `skills/`.

Or paste the hosted URL into `~/.cursor/mcp.json` (tools work; that path has no marketplace logo):

```json
{
  "mcpServers": {
    "conthunt": {
      "url": "https://mcp.conthunt.app/"
    }
  }
}
```

## Claude Code

```text
/plugin marketplace add Synthenova/conthunt-mcp
/plugin install conthunt@conthunt
```

## Codex

```sh
codex plugin marketplace add Synthenova/conthunt-mcp
codex mcp add conthunt --url https://mcp.conthunt.app/
codex mcp login conthunt
```

## Grok Build

```sh
grok plugin marketplace add Synthenova/conthunt-mcp
```

Grok chat: [grok.com/connectors](https://grok.com/connectors) → Custom → `https://mcp.conthunt.app/`. Grok Bot’s Plugins tab lists **Cursor Marketplace** entries, not this GitHub URL by itself.

## Skill

Same skill as the site:

```sh
npx skills add https://conthunt.app
```

From this repo:

```sh
npx skills add Synthenova/conthunt-mcp --skill conthunt -g
```

## Layout

| Path | For |
| --- | --- |
| `mcp.json` | Hosted MCP pointer |
| `plugin.json` | Agent Plugins (Cursor / Codex / portable) |
| `.cursor-plugin/` | Cursor marketplace |
| `.claude-plugin/` | Claude Code marketplace |
| `.grok-plugin/` | Grok Build marketplace |
| `.agents/plugins/` | Codex marketplace catalog |
| `skills/conthunt/` | Agent skill |
| `assets/logo-dark.png` | Marketplace logo |

CLI binaries stay in [`Synthenova/conthunt-cli`](https://github.com/Synthenova/conthunt-cli). This pack does not ship the CLI.

## License

Plugin and skill files are MIT. The ContHunt service is proprietary.
