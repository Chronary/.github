# Contributing to Chronary

The content of this repo — org profile and community-health files — is generated from the Chronary monorepo's `community/` folder. The rest of Chronary's public repos (SDKs, CLI, MCP server, toolkit, schemas, OpenAPI snapshot, examples) are also generated from that same private monorepo. Pull requests opened on any of these repos are welcome as proof-of-concept but cannot be merged directly — any change would be overwritten on the next generated release. To propose a change, open an Issue and the Chronary team will route it into the monorepo.

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
| Examples | [chronary-examples](https://github.com/Chronary/chronary-examples/issues) |

We triage on the mirror, route the fix into the internal monorepo, and the fix lands on the mirror in the next release.

If you would rather not file in public — for billing, account questions, or anything sensitive — email [support@chronary.ai](mailto:support@chronary.ai). Security issues have a separate disclosure process at [security@chronary.ai](mailto:security@chronary.ai); see [SECURITY.md](./SECURITY.md).

## Code of conduct

Participation in any Chronary repo is governed by the [Code of Conduct](./CODE_OF_CONDUCT.md).

## Security issues

Do **not** file security issues publicly. See [SECURITY.md](./SECURITY.md) for the responsible-disclosure process.
