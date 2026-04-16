# Chronary

**Calendar-as-a-service for AI agents.**

Chronary gives AI agents a native way to create, manage, and query calendars — purpose-built for the agentic era. One API key, full calendar CRUD, real-time webhooks, availability queries, and iCal feeds for human consumption.

## Repositories

| Repo | Description |
|------|-------------|
| [chronary-node](https://github.com/Chronary/chronary-node) | TypeScript/Node SDK — `npm install @chronary/sdk` |
| [chronary-python](https://github.com/Chronary/chronary-python) | Python SDK — `pip install chronary` |
| [chronary-mcp](https://github.com/Chronary/chronary-mcp) | MCP server — `npx chronary-mcp` |
| [chronary-cli](https://github.com/Chronary/chronary-cli) | CLI tool for developers |
| [chronary-openapi](https://github.com/Chronary/chronary-openapi) | OpenAPI spec and Postman collection |
| [chronary-examples](https://github.com/Chronary/chronary-examples) | Example agents and integration patterns |

## Quick start

```bash
npm install @chronary/sdk
```

```typescript
import { Chronary } from '@chronary/sdk';

const client = new Chronary({ apiKey: 'chr_sk_live_...' });

const agent = await client.agents.create({ name: 'My Agent' });
const calendar = await client.calendars.create({ name: 'Meetings', agentId: agent.id });
const event = await client.events.create({
  calendarId: calendar.id,
  title: 'Sync with team',
  startTime: '2026-04-16T10:00:00Z',
  endTime: '2026-04-16T10:30:00Z',
});
```

## Links

- [Documentation](https://docs.chronary.ai)
- [API Console](https://console.chronary.ai)
- [Website](https://chronary.ai)
