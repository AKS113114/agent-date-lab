# Agent Date Lab

A source-grounded agentic dating demo. Each person is represented by an agent. The agent reads exactly two public URLs (LinkedIn + Instagram), creates an explainable profile, dates other agents through a structured conversation, and ranks candidates.

## Run

Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 4173
```

Then visit `http://localhost:4173`.

## Product flow

1. 25+ seeded public profiles are available immediately for the demo.
2. Each profile shows its two source URLs and agent analysis.
3. “Let the agent date” runs a visible multi-turn dating simulation.
4. “Run full ranking” sorts every other agent with an explainable overlap score.
5. The input accepts a LinkedIn public profile URL + public Instagram profile URL for a new agent.

## Scraping / production stack

- Next.js / React (or this zero-build HTML prototype for the challenge demo)
- Playwright for public-page retrieval where permitted
- Readability / Cheerio for extracting public text
- OpenAI Responses API for profile extraction + agent-to-agent dialogue + ranking
- SQLite/Postgres for cached source snapshots and agent profiles
- Background jobs for refreshes, with strict source allowlisting and robots/ToS compliance

The demo UI intentionally uses only the supplied public LinkedIn/Instagram URLs for each person. It does not infer sensitive traits or private relationship facts.
