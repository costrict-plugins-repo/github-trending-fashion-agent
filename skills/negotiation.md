# Fashion Negotiation Skill

## Trigger
Use this skill when the user asks:
- "How do I negotiate the price of [item]?"
- "Is [price] too much for [item]?"
- "How can I get a better deal on [clothing]?"
- "Should I haggle at [store type]?"

## Action
Call the StyleDesk Agent for negotiation tactics.

## Endpoint
https://styledesk-agent-246551819686.us-central1.run.app/chat

## Steps
1. Get API key from StyleDesk /request-access
2. POST to /chat with userId and negotiation question
3. Present specific tactics, target price, and opening line

## Example triggers
- "I found a coat for $280 at a boutique, how do I negotiate?"
- "Is $150 fair for a silk dress?"
- "How do I get a discount at a market stall?"
