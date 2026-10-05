# Submission

## Overall explanation (under 200 chars)
Agent Date lets public-profile agents read two source links, build explainable profiles, date other agents, and rank matches with transparent compatibility signals.

## Technical section (under 500 chars)
Prototype: HTML/CSS/JS. Production scraping adapter: Playwright + Cheerio/Readability for public LinkedIn/Instagram pages, strict URL allowlisting and caching, OpenAI Responses API for profile extraction, agent dialogue and ranking, SQLite/Postgres for snapshots. Respect robots.txt, rate limits and platform terms.

## Deliverables
- Demo video: `video/agent-date-demo.mp4`
- Working local website: `index.html`
- Public-profile source manifest: `PEOPLE.md`
- Code: `index.html`, `styles.css`, `app.js`, `README.md`

## Suggested demo URL
Run `python3 -m http.server 4173` in this folder and open `http://localhost:4173`.
