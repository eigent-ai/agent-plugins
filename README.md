# Agent Plugins

A collection of MCP (Model Context Protocol) plugins for AI coding agents when building Eigent.

Plugins provide tools and integrations—GitHub, Slack, Playwright, and more—that agents can use during development.

## Available Plugins

View all plugins at [eigent.ai/plugins](https://www.eigent.ai/plugins).

## Plugin Structure

Each plugin follows a standard structure:

```
plugin-name/
├── .eigent-plugin/
│   └── plugin.json      # Plugin metadata (required)
├── .mcp.json            # MCP server configuration (optional)
├── commands/            # Slash commands (optional)
├── agents/              # Agent definitions (optional)
├── skills/              # Skill definitions (optional)
└── README.md            # Documentation
```

### Required

- **`.eigent-plugin/plugin.json`** — Plugin metadata: `name`, `description`, `author`, and any other fields required by Eigent.

### Optional

- **`.mcp.json`** — MCP server configuration. Defines how to connect to the plugin's MCP server (HTTP, stdio, or other transports).
- **`commands/`** — Slash commands exposed by the plugin.
- **`agents/`** — Agent definitions.
- **`skills/`** — Skill definitions bundled with the plugin.
- **`README.md`** — Plugin-specific documentation and setup instructions.

## Configuration

Each plugin's `.mcp.json` defines how agents connect to its MCP server. Example configurations:

- **GitHub** — HTTP MCP with `GITHUB_PERSONAL_ACCESS_TOKEN`.
- **Playwright** — Stdio MCP via `npx @playwright/mcp@latest`.
- **Slack** — HTTP MCP with OAuth (client ID and callback port).

Refer to each plugin's documentation for setup and environment variables.

## License

Apache License 2.0. See `LICENSE` for the full text.
