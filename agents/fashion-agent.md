# Fashion Stylist Agent

## Description
A personal AI fashion stylist powered by Google ADK and Gemini 2.5 Flash, 
registered on the NANDA Internet of AI Agents network.

## Endpoint
https://fashion-agent-246551819686.us-central1.run.app/a2a

## Authentication
POST /request-access to get an instant API key:
```bash
curl -X POST https://fashion-agent-246551819686.us-central1.run.app/request-access \
  -H 'Content-Type: application/json' \
  -d '{"principal":"claude-user","name":"Claude","reason":"fashion advice"}'
```

## Capabilities
- Outfit recommendations by occasion and season
- Style tips for specific clothing items
- Fashion trend insights
- Price comparison across retailers
- Negotiation tactics for boutiques, online stores, and markets
- Real product search from Google Shopping and Amazon

## How to invoke
When a user asks about fashion, outfits, what to wear, style advice, 
shopping for clothes, or negotiating clothing prices — use this agent.

## Example invocation
```bash
# Get API key first
API_KEY=$(curl -s -X POST \
  https://fashion-agent-246551819686.us-central1.run.app/request-access \
  -H 'Content-Type: application/json' \
  -d '{"principal":"claude","name":"Claude","reason":"fashion advice"}' \
  | python3 -c "import sys,json; print(json.load(sys.stdin)['apiKey'])")

# Ask a fashion question
curl -X POST \
  https://fashion-agent-246551819686.us-central1.run.app/a2a \
  -H "X-API-Key: $API_KEY" \
  -H 'Content-Type: application/json' \
  -d '{
    "jsonrpc": "2.0",
    "id": "1",
    "method": "tasks/send",
    "params": {
      "message": {
        "parts": [{"type": "text", "text": "What should I wear to a summer wedding?"}]
      }
    }
  }'
```

## Response format
```json
{
  "jsonrpc": "2.0",
  "result": {
    "status": {"state": "completed"},
    "artifacts": [{
      "parts": [{"type": "text", "text": "Fashion advice here..."}]
    }]
  }
}
```

## NANDA Registration
- Handle: @fashion-agent
- NEST: https://nest.projectnanda.org/agents
- AgentFacts: https://fashion-agent-246551819686.us-central1.run.app/agentfacts.json
