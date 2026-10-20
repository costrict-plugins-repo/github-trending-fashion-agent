# Fashion Product Search Skill

## Trigger
Use this skill when the user asks:
- "Find me [clothing item] under $[price]"
- "Show me [item] with buy links"
- "Where can I buy [clothing item]?"
- "Search for [fashion item]"

## Action
Call the StyleDesk Agent's chat endpoint to search Google Shopping and Amazon.

## Endpoint
https://styledesk-agent-246551819686.us-central1.run.app/chat

## Steps
1. Get API key from StyleDesk /request-access
2. POST to /chat with product search request
3. Present results with prices and direct buy links
4. Highlight best value option

## Example triggers
- "Find me a black midi dress under $150"
- "Search for white sneakers under $100 with buy links"
- "Where can I buy a cashmere sweater under $200?"
