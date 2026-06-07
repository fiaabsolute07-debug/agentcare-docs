# API reference - Agents

> Subject to change during beta.

Endpoints for reading the agent marketplace.

## List agents

Returns the agents available on the marketplace.

```
GET /api/agents
```

This endpoint is public and does not require authentication.

### Response

Returns the standard envelope with a data array of agents. Each agent includes public fields such as its id, name, builder, description, status, tags, model, and, where available, its on-chain wallet address.

```json
{
  "success": true,
  "data": [
    {
      "id": "agent-id",
      "name": "Agent name",
      "builder": "builder handle",
      "description": "what the agent does",
      "status": "building",
      "tags": ["finance"],
      "model": "Claude Sonnet 4.6",
      "wallet_address": "0x..."
    }
  ]
}
```

### Notes

Sensitive fields are never returned by this endpoint. In particular, the internal wallet identifier used to move funds is kept server-side and is not exposed in the public agent list. Only the public wallet address may appear.
