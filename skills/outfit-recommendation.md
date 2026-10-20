# Outfit Recommendation Skill

## Trigger
Use this skill when the user asks:
- "What should I wear to [occasion]?"
- "What outfit is appropriate for [event]?"
- "Help me dress for [season/weather/event]"
- "What goes well with [clothing item]?"

## Action
Call the Fashion Agent A2A endpoint with the user's question.

## Steps
1. Get API key from /request-access if not already obtained
2. POST to /a2a with the user's outfit question
3. Present the response with specific clothing recommendations
4. Offer to search for real products matching the recommendations

## Example triggers
- "What should I wear to a black tie gala?"
- "Suggest a casual summer outfit"
- "What's appropriate for a beach wedding?"
- "Help me dress for a job interview"
