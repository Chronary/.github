# Contributing to Chronary

Most of Chronary's public repos are read-only mirrors of an internal monorepo, populated by an automated release pipeline. **Pull requests are blocked at the repo level on these mirrors** — they are not a code-collaboration surface. The two exceptions are `chronary-examples` and `chronary-skills`, which are OSS-native and welcome contributions directly.

## Reporting a bug or asking for a change

File an issue on the **repo where the bug surfaced**:

| Surface | Repo |
|---|---|
| TypeScript SDK | [chronary-node](https://github.com/Chronary/chronary-node/issues) |
| Python SDK | [chronary-python](https://github.com/Chronary/chronary-python/issues) |
| Go SDK | [chronary-go](https://github.com/Chronary/chronary-go/issues) |
| CLI | [chronary-cli](https://github.com/Chronary/chronary-cli/issues) |
| MCP server | [chronary-mcp](https://github.com/Chronary/chronary-mcp/issues) |
| Toolkit (framework adapters) | [chronary-toolkit](https://github.com/Chronary/chronary-toolkit/issues) |
| Shared schemas | [chronary-schemas](https://github.com/Chronary/chronary-schemas/issues) |
| OpenAPI / Postman | [chronary-openapi](https://github.com/Chronary/chronary-openapi/issues) |

We triage on the mirror, port the fix in the internal monorepo, and the fix lands on the mirror in the next release.

If you would rather not file in public — for billing, account questions, or anything sensitive — email [support@chronary.ai](mailto:support@chronary.ai). Security issues have a separate disclosure process at [security@chronary.ai](mailto:security@chronary.ai); see [SECURITY.md](./SECURITY.md).

## Contributing to chronary-examples and chronary-skills

These two repos are OSS-native and welcome pull requests directly:

- [chronary-examples](https://github.com/Chronary/chronary-examples) — example agents and integration patterns. Add a new example, fix one that broke, or improve a README.
- [chronary-skills](https://github.com/Chronary/chronary-skills) — agent skills and IDE plugins for Claude Code, Cursor, VS Code Copilot, Codex, and Windsurf. Add a new skill or improve an existing one.

Each repo's own `CONTRIBUTING.md` covers style, testing, and the PR process. Fork, branch, open a PR.

## Code of conduct

Participation in any Chronary repo is governed by the [Code of Conduct](./CODE_OF_CONDUCT.md).

## Security issues

Do **not** file security issues publicly. See [SECURITY.md](./SECURITY.md) for the responsible-disclosure process.
