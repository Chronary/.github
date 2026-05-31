# Chronary

**Calendar infrastructure for AI agents.**

Chronary gives AI agents a native way to create, manage, and query calendars — one API key, full calendar CRUD, real-time webhooks, availability queries, and iCal feeds for human consumption. Purpose-built for the agentic era, with an MCP server, REST API, and SDKs in TypeScript, Python, Go, and a Go-based CLI.

[**Get started →**](https://docs.chronary.ai/getting-started/quickstart/)  ·  [**Sign in**](https://console.chronary.ai)  ·  [Documentation](https://docs.chronary.ai)  ·  [chronary.ai](https://chronary.ai)

## Quickstart for AI coding agents

First, grab an API key at [console.chronary.ai/sign-up](https://console.chronary.ai/sign-up) — then pick your tool below.

> **Windows:** replace `curl -fsSL … | bash` with `iwr -useb … | iex` in any block.

**1. Claude Code** — install the plugin from inside the Claude Code REPL:

```text
/plugin marketplace add Chronary/chronary-skills
/plugin install chronary@chronary
/reload-plugins
```

Run `/plugins` to confirm `chronary` is listed. (The doubled `chronary@chronary` is `<plugin>@<marketplace>` — both happen to be named `chronary`.) Installs four skills, three slash commands, and the MCP server config in one bundle.

**2. Any AGENTS.md-aware agent (Codex, Aider, Devin, Gemini CLI, Amazon Q, Copilot, …)** — drop our `AGENTS.md` into your project root:

```bash
curl -fsSL https://raw.githubusercontent.com/Chronary/chronary-skills/main/AGENTS.md -o AGENTS.md
```

Codex also reads `~/.codex/AGENTS.md` for user-wide instructions.

**3. Cursor / VS Code Copilot / Windsurf** — one-liner installer copies the skill files into the right per-editor location:

```bash
curl -fsSL https://raw.githubusercontent.com/Chronary/chronary-skills/main/install.sh | bash -s -- cursor
# targets: cursor | vscode | windsurf | all
```

For live API calls from these editors, also configure the MCP server (block 4 below).

**4. MCP clients (Claude Desktop, Cursor, Windsurf, VS Code)** — add this to your client's MCP config file:

```json
{
  "mcpServers": {
    "chronary": {
      "command": "npx",
      "args": ["-y", "@chronary/mcp"],
      "env": { "CHRONARY_API_KEY": "chr_sk_..." }
    }
  }
}
```

> _VS Code (`.vscode/mcp.json`) uses `servers` instead of `mcpServers`; everything else is identical._

Verify with `npx -y @chronary/mcp --help`. Full per-client setup (file locations, auto-approve patterns, troubleshooting) lives in [chronary-skills](https://github.com/Chronary/chronary-skills).

## Repositories

The published surfaces — open these to install, file bugs, or read the source:

| Repo | What it is |
|------|------------|
| [chronary-node](https://github.com/Chronary/chronary-node) | TypeScript / Node SDK — installable from npm as `@chronary/sdk`. |
| [chronary-python](https://github.com/Chronary/chronary-python) | Python SDK — installable from PyPI as `chronary`. |
| [chronary-mcp](https://github.com/Chronary/chronary-mcp) | MCP server for Claude Desktop, Cursor, VS Code, and Windsurf. |
| [chronary-cli](https://github.com/Chronary/chronary-cli) | Command-line tool for developers and CI — install via Homebrew or a release binary. |
| [chronary-openapi](https://github.com/Chronary/chronary-openapi) | OpenAPI spec, Postman collection, and LLM context files. |
| [chronary-examples](https://github.com/Chronary/chronary-examples) | Example agents and integration patterns across SDKs. |

### Also available

- [chronary-go](https://github.com/Chronary/chronary-go) — Go SDK for native Go services.
- [chronary-schemas](https://github.com/Chronary/chronary-schemas) — Zod schemas and TypeScript types shared by the SDK, webhooks, and OpenAPI spec.
- [chronary-toolkit](https://github.com/Chronary/chronary-toolkit) — Agent-framework adapters that wrap the SDK for popular AI frameworks.
- [chronary-skills](https://github.com/Chronary/chronary-skills) — Full reference for the Quickstart above (installers, plugin manifest, AGENTS.md, all skill files).
- [homebrew-tap](https://github.com/Chronary/homebrew-tap) — Homebrew formula for the `chronary` CLI.

## How Chronary differs

Most calendar APIs were built for human-driven calendar apps and assume an interactive sign-in flow. Chronary is built for agents:

- **One API key, no OAuth dance.** Programmatic agents authenticate with an org-scoped or agent-scoped API key. OAuth is reserved for bridging to user-owned Google or Outlook calendars when an agent needs to act on a human's behalf.
- **Webhook-first event delivery.** Every meaningful change emits an HMAC-signed webhook so downstream agents can react without polling.
- **iCal feeds for humans.** Calendars produced by agents render in any human calendar app via signed iCal subscription URLs — no separate bridging service needed.
- **MCP-native.** The same Worker that serves the REST API also exposes an MCP server, so any MCP-capable client (Claude Desktop, Cursor, Windsurf, VS Code) can drive Chronary directly.

## Community and contact

- **Website** — [chronary.ai](https://chronary.ai)
- **Documentation** — [docs.chronary.ai](https://docs.chronary.ai)
- **Product and account support** — [support@chronary.ai](mailto:support@chronary.ai)
- **Security and responsible disclosure** — [security@chronary.ai](mailto:security@chronary.ai) (see [SECURITY.md](https://github.com/Chronary/.github/blob/main/SECURITY.md))
- **Privacy and DPA requests** — [privacy@chronary.ai](mailto:privacy@chronary.ai)
- **Discord** — [Join the server](https://discord.gg/nukjpejk2)

A note on these repos: most are read-only mirrors of an internal monorepo, populated by an automated release pipeline. **Pull requests are not accepted on the mirrors** — bug reports go to Issues on the surface where the bug surfaced. `chronary-examples` and `chronary-skills` are OSS-native and welcome PRs directly. See [CONTRIBUTING.md](https://github.com/Chronary/.github/blob/main/CONTRIBUTING.md) for the full policy.
