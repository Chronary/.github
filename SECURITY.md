# Security Policy

Chronary stores calendar data and API credentials for developers and the AI agents they build. We welcome reports from security researchers acting in good faith, and we want to make reporting easy and safe.

This policy covers how to report a vulnerability, what you can expect from us, and the rules for testing. Our general security commitments are at [chronary.ai/security](https://chronary.ai/security). The machine-readable contact file is at [chronary.ai/.well-known/security.txt](https://chronary.ai/.well-known/security.txt).

## How to report

- **Email:** [security@chronary.ai](mailto:security@chronary.ai).
- **GitHub:** on our public SDK and tool repositories you can also use private vulnerability reporting ("Report a vulnerability" on the repository's **Security** tab).

Please do not report security issues in public GitHub issues, discussions, pull requests or social media.

A useful report includes:

- what the issue is and what an attacker could do with it;
- the steps to reproduce it, including the requests, URLs or commands you used;
- which part of Chronary is affected (API, MCP server, console, website, docs, an SDK, the CLI, webhooks or calendar feeds);
- anything else that helps us reproduce it, such as screenshots or a minimal proof of concept;
- the name or handle you'd like us to use if we credit you.

Please remove API keys, personal data and any third-party credentials from what you send.

## What to expect

These are targets, not guarantees, but we will keep you informed either way.

- **Acknowledgement:** within 72 hours of your report.
- **Initial assessment:** within 5 business days, including our view of severity and our plan.
- **Updates:** at least every 14 days until the issue is resolved.
- **Fix:** we aim to fix critical issues within 30 days. Other issues are scheduled by risk.
- **Disclosure:** we'll agree a disclosure date with you. Please give us a reasonable time to fix the issue before you publish anything. With your permission, we'll credit you when we publish.

## Supported versions

| Component | Supported |
| --- | --- |
| Hosted services (`chronary.ai`, `api.chronary.ai`, `console.chronary.ai`, `docs.chronary.ai`) | The current deployment |
| TypeScript SDK, Python SDK, Go SDK, the `chronary` CLI and the MCP server | Each major version for at least 5 years from its first release (see below) |
| The toolkit and the schemas package | The latest released version |

**Support period.** We support each major version of the SDKs, the CLI and the MCP server with security fixes for at least five years from the date its first release was published. Fixes ship in a new release of the same major version, which is free, so please keep up with the latest release of your major version. Until a package reaches version 1.0, its whole 0.x series counts as one major version.

| Product | Major version | First released | Supported until at least |
| --- | --- | --- | --- |
| TypeScript SDK (`@chronary/sdk`) | 0.x | April 2026 | April 2031 |
| Python SDK (`chronary`) | 0.x | April 2026 | April 2031 |
| Go SDK (`chronary-go`) | 0.x | April 2026 | April 2031 |
| `chronary` CLI | 0.x | April 2026 | April 2031 |
| MCP server (`@chronary/mcp`) | 1.x | June 2026 | June 2031 |

When we release a new major version, we'll add it here with its own end date, and we'll announce the end of support for a major version in its changelog before it happens. Earlier major versions not listed here, such as the MCP server's 0.x series, are no longer supported; please upgrade.

## Scope

**In scope:**

- `api.chronary.ai` (REST API and MCP server)
- `console.chronary.ai` (customer dashboard)
- `chronary.ai` and `docs.chronary.ai`, for issues with a real security impact
- Webhook delivery and signing
- Calendar feed (iCal) generation and subscriptions
- Our published SDKs, CLI, MCP server and toolkit

**Out of scope:**

- Denial of service, load or volumetric testing, and anything that degrades the service for others
- Spam, including sending large numbers of emails, invitations or webhook deliveries
- Social engineering or phishing of our staff, contractors or customers
- Physical attacks
- Third-party services, websites and products that we don't own
- Findings that depend on a compromise outside Chronary, such as a stolen password or an already-compromised device or browser
- Self-XSS, and missing security headers or best-practice settings without a demonstrated impact
- Automated scanner output without a working proof of concept

## Rules for testing

- **Use your own account.** Create your own account for testing, and only test against accounts and data you own or have explicit permission to use.
- **Don't access other customers' data.** If you come across data that isn't yours, stop, don't keep or share it, and tell us what you saw in your report.
- **Keep it small.** Use the minimum amount of testing needed to show the issue, at a modest request rate. Don't run high-volume automated scans.
- **Don't cause harm.** Don't modify or delete data that isn't yours, and don't disrupt the service.
- **Keep it confidential** until we've agreed a disclosure date with you.

If you're not sure whether something is allowed, email us and ask before you test.

## Safe harbor

If you make a good-faith effort to follow this policy, we will consider your research authorized, and:

- we won't take legal action against you for that research, including under anti-hacking or anti-circumvention laws, and we won't ask law enforcement to act against you for it;
- we won't treat it as a breach of our Terms of Service, to the extent the research would otherwise break the acceptable-use rules in those terms;
- if a third party takes legal action against you over research that followed this policy, we'll make it known that your work was authorized by us.

This safe harbor covers Chronary's own systems and only the rights that Chronary holds. We can't authorize testing of systems that belong to others, including our service providers and our customers. Good faith means, at a minimum, that you respect user privacy, avoid data destruction and service disruption, don't take data beyond what you need to show the issue, and give us reasonable time to fix the issue before public disclosure.

The safe harbor doesn't cover demands for payment or other conditions in exchange for not disclosing an issue, keeping or using data that isn't yours, or activity that this policy puts out of scope. Nothing in it limits what we're required to do by law.

## Compromised API keys

If you think a Chronary API key has been exposed, for example in source code, logs or a public repository, rotate it right away in the [console](https://console.chronary.ai) and let us know at [security@chronary.ai](mailto:security@chronary.ai). We may revoke keys that we believe have been compromised, and we'll tell the account owner when we do.

## Bug bounty

We don't run a paid bug bounty program at the moment. We're grateful for every valid report, and with your permission we're happy to credit you.
