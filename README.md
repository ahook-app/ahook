# AHOOK

Webhooks designed for agents.

AHOOK is a webhook inbox for AI agents. Create an inbox, get an ingest URL, and your agent can wait for events, list them, and pull fields out of them — all from one hosted endpoint. No install, no server to run.

## MCP server

- Endpoint: `https://ahook.app/mcp` (Streamable HTTP, JSON-RPC 2.0)
- Registry: `app.ahook/ahook` on the official MCP Registry
- Point any MCP client at the endpoint URL — nothing to install.

## Tools

| Tool | What it does |
|---|---|
| `create_inbox` | Create a webhook inbox. Returns its ingest URL and a read token (shown once). |
| `wait_for_event` | Wait for the next event in an inbox after a cursor, up to 30s. |
| `list_events` | List events in an inbox. |
| `get_event` | Get one event by id. |
| `extract_field` | Pull a JSON path out of an event body. |
| `delete_inbox` | Delete an inbox and its events. |

Inbox-scoped tools use an `Authorization: Bearer <read token>` header. `create_inbox` works without one and returns the token.

## Links

- Website: https://ahook.app
- Agent instructions: https://ahook.app/llms.txt
- OpenAPI: https://ahook.app/openapi.json

## Pricing

Free tier, plus Starter $7/mo and Growth $19/mo. Details at https://ahook.app.
