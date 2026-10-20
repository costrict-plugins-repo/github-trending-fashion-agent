# Fashion Agent Plugin for Claude

A personal AI fashion stylist plugin that brings outfit recommendations,
style tips, deal negotiation, and real product search directly into Claude.

## What it does

| Skill | Description |
|---|---|
| Outfit Recommendation | Suggests complete outfits for any occasion or season |
| Style Tips | Styling advice for specific clothing items |
| Negotiation | Tactics for getting better prices at boutiques, online, markets |
| Product Search | Real products with buy links from Google Shopping and Amazon |

## Agents included

- **@fashion-agent** — Specialist outfit advisor (Google ADK + Gemini 2.5 Flash)
- **@styledesk-agent (Sofia)** — Conversational stylist with memory and negotiation

## Quick start

Once installed, just ask Claude naturally:
- *"What should I wear to a winter gala?"*
- *"Find me a silk midi dress under $200"*
- *"How do I negotiate the price of a coat at a boutique?"*
- *"Give me style tips for wearing white jeans"*

Claude will automatically invoke the fashion agent and return real advice
and product links.

## Authentication

Both agents use self-service API keys — no signup needed:
```bash
curl -X POST \
  https://fashion-agent-246551819686.us-central1.run.app/request-access \
  -H 'Content-Type: application/json' \
  -d '{"principal":"your-name","name":"Your Name","reason":"fashion advice"}'
```

## Built with

- Google ADK for Java 1.0.0
- Gemini 2.5 Flash via Vertex AI
- Google Cloud Run
- NANDA Index (@fashion-agent)
- NEST Live Network

## Links

- Agent: https://fashion-agent-246551819686.us-central1.run.app
- StyleDesk: https://styledesk-agent-246551819686.us-central1.run.app
- NANDA: https://nest.projectnanda.org/agents
- Agent Card: https://fashion-agent-246551819686.us-central1.run.app/.well-known/agent-card.json
