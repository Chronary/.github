# Security Policy

Chronary stores calendar data and API credentials on behalf of developers and their AI agents. We take security seriously and welcome reports from researchers acting in good faith.

The full security architecture — encryption, authentication, infrastructure, compliance posture, and incident-response runbook — is published at [chronary.ai/security](https://chronary.ai/security). This file covers the disclosure process itself.

## Reporting a vulnerability

Email **[security@chronary.ai](mailto:security@chronary.ai)** with a description of the issue and reproduction steps. Please do not file security reports as GitHub issues or post them publicly.

If you would like to encrypt the report, request our PGP key in your initial email and we will reply with the current key fingerprint.

## What to include

- A clear description of the vulnerability and its potential impact
- Steps to reproduce, including request payloads, URLs, or commands
- The Chronary surface affected (REST API, MCP server, console, SDK, CLI, iCal feed)
- Any artifacts (HTTP captures, screenshots, proof-of-concept code) that help us reproduce
- Your preferred name or handle for acknowledgment, if you would like credit

Please redact any API keys, customer data, or third-party credentials before including artifacts.

## Response timelines

- **Acknowledgment** — we aim to acknowledge receipt within **72 hours**.
- **Triage** — we will provide an initial assessment within **5 business days**, including severity and our intended remediation timeline.
- **Fix targets** — critical vulnerabilities are targeted for fix within **30 days**; lower-severity issues are scheduled on a risk-prioritized basis.
- **Disclosure** — we will coordinate public disclosure with you. Default posture is to publish a write-up once a fix is deployed.

## Scope

**In scope:**

- `api.chronary.ai` (REST API and MCP server)
- `console.chronary.ai` (authenticated dashboard)
- `chronary.ai` (marketing site) — only for vulnerabilities with security impact
- `docs.chronary.ai` (documentation site) — only for vulnerabilities with security impact
- Webhook delivery and signing
- iCal feed generation and subscription handling
- The published SDKs and CLI (TypeScript, Python, Go, MCP server, `chronary` CLI)

**Out of scope:**

- Social engineering of Chronary staff or contractors
- Physical attacks on Chronary infrastructure
- Denial-of-service testing
- Findings that require compromise of a third-party service (e.g., guessing a customer's password elsewhere)
- Missing security headers on marketing pages without a demonstrated impact
- Self-XSS or attacks requiring an already-compromised browser
- Automated scanner output without a working proof-of-concept

## Safe harbor

Good-faith research that

1. respects user privacy,
2. avoids data destruction or service disruption,
3. does not exfiltrate data beyond what is necessary to demonstrate the issue, and
4. gives Chronary reasonable time to remediate before public disclosure

will not result in legal action from Chronary under the Computer Fraud and Abuse Act, DMCA Section 1201, or applicable anti-hacking laws. If a third party initiates legal action against you for activity that complies with this policy, we will make our position on the matter known to them.

## API key compromise

If you suspect an API key has been exposed in source code, logs, or a public repository, rotate it immediately via the [console](https://console.chronary.ai) and notify us at [security@chronary.ai](mailto:security@chronary.ai). We may proactively revoke keys we believe have been compromised — including keys detected through third-party secret-scanning programs — and will notify the account owner when we do so.

## Bug bounty

We do not currently operate a formal bug bounty program. We may introduce one in the future and will acknowledge researchers who report valid issues in our security advisories.
