# Chronary

**Calendar infrastructure for AI agents.**

Chronary gives AI agents a native way to create, manage, and query calendars — one API key, full calendar CRUD, real-time webhooks, availability queries, and iCal feeds for human consumption. Purpose-built for the agentic era, with an MCP server, REST API, and SDKs in TypeScript, Python, Go, and a Go-based CLI.

[**Get started →**](https://docs.chronary.ai/getting-started/quickstart/)  ·  [**Sign in**](https://console.chronary.ai)  ·  [Documentation](https://docs.chronary.ai)  ·  [chronary.ai](https://chronary.ai)

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
- [chronary-skills](https://github.com/Chronary/chronary-skills) — Agent skills and IDE plugins for Claude Code, Cursor, VS Code Copilot, Codex, and Windsurf.
- [homebrew-tap](https://github.com/Chronary/homebrew-tap) — Homebrew formula for the `chronary` CLI.

## How Chronary differs

Most calendar APIs were built for human-driven calendar apps and assume an interactive sign-in flow. Chronary is built for agents:

- **One API key, no OAuth dance.** Programmatic agents authenticate with an org-scoped or agent-scoped API key. OAuth is reserved for bridging to user-owned Google or Outlook calendars when an agent needs to act on a human's behalf.
- **Webhook-first event delivery.** Every meaningful change emits an HMAC-signed webhook so downstream agents can react without polling.
- **iCal feeds for humans.** Calendars produced by agents render in any human calendar app via signed iCal subscription URLs — no separate bridging service needed.
- **MCP-native.** The same Worker that serves the REST API also exposes an MCP server, so any MCP-capable client (Claude Desktop, Cursor, Windsurf, VS Code) can drive Chronary directly.

## Community and contact

- **Documentation** — [docs.chronary.ai](https://docs.chronary.ai)
- **Product and account support** — [support@chronary.ai](mailto:support@chronary.ai)
- **Security and responsible disclosure** — [security@chronary.ai](mailto:security@chronary.ai) (see [SECURITY.md](./SECURITY.md))
- **Privacy and DPA requests** — [privacy@chronary.ai](mailto:privacy@chronary.ai)
- **X / Twitter** — [@chronaryai](https://x.com/chronaryai)
- **Discord** — [Join the server](https://discord.gg/nukjpejk2)

A note on these repos: most are read-only mirrors of an internal monorepo, populated by an automated release pipeline. **Pull requests are not accepted on the mirrors** — bug reports go to Issues on the surface where the bug surfaced. `chronary-examples` and `chronary-skills` are OSS-native and welcome PRs directly. See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full policy.
