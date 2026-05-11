# Support

Chronary is calendar infrastructure for AI agents — REST API, MCP server, iCal feeds, and SDKs for TypeScript, Python, Go, and the Chronary CLI.

## Where to get help

- **Documentation** — [docs.chronary.ai](https://docs.chronary.ai). Quickstart, API reference, MCP setup, examples.
- **Email** — [support@chronary.ai](mailto:support@chronary.ai) for product questions, account issues, and billing.
- **Security issues** — see [SECURITY.md](./SECURITY.md). Do not file security reports as GitHub issues.

## Filing a bug or feature request

File issues on the specific repo where the bug surfaced:

| Surface | Repo |
|---|---|
| TypeScript SDK | [chronary-node](https://github.com/Chronary/chronary-node) |
| Python SDK | [chronary-python](https://github.com/Chronary/chronary-python) |
| MCP server | [chronary-mcp](https://github.com/Chronary/chronary-mcp) |
| CLI | [chronary-cli](https://github.com/Chronary/chronary-cli) |
| OpenAPI / Postman | [chronary-openapi](https://github.com/Chronary/chronary-openapi) |
| Example code | [chronary-examples](https://github.com/Chronary/chronary-examples) |

If the issue spans multiple surfaces or you are not sure where it belongs, email [support@chronary.ai](mailto:support@chronary.ai) and we will route it.

## What to include in a bug report

The faster we can reproduce, the faster we can fix:

- SDK / CLI / MCP version (`chronary --version` for the CLI; check `package.json` / `pyproject.toml` for SDKs)
- The exact request or command that triggered the issue
- The full error message and response body, with API keys redacted
- Operating system and runtime version (Node, Python, Go, etc.) when relevant
