# Raza AI Agent (starter v1)

A responsive lead CRM and AI outreach drafting dashboard. Node.js 18+ required.

## Run on Windows 11
1. Install Node.js LTS from https://nodejs.org/.
2. Extract the ZIP and open this folder in VS Code.
3. Open Terminal in VS Code and run `npm install`.
4. Copy `.env.example` to `.env`.
5. To enable AI drafting, add your Groq API key to `GROQ_API_KEY` in `.env`. Keep this file private; never commit it.
6. Run `npm start` and open http://localhost:3000.

## Included
- Responsive dashboard and lead metrics
- SQLite persistent local database
- Create, edit, delete, search, qualify and status-track leads
- CSV import/export
- AI-generated email / WhatsApp / DM drafts through Groq (requires API key)
- Activity log for calls, emails, meetings and follow-ups
- Integration status page

## Not yet live / requires provider setup
- Google Maps Places live lead discovery is not wired yet. Use lawful provider APIs, follow their terms, and avoid harvesting private/personal data.
- Email and WhatsApp sending, incoming reply detection, scheduled automatic follow-ups, and calling are not enabled in this starter. Add official provider APIs, authentication, consent/opt-out handling, rate limits and human approval before sending or calling.
- For deployment, configure persistent storage for `data/raza-agent.db`; ephemeral hosting storage can reset on redeploy.

## API endpoints
- `GET /api/health`
- `GET/POST /api/leads`
- `PATCH/DELETE /api/leads/:id`
- `POST /api/ai/draft`
- `GET/POST /api/activities`
- `GET /api/export.csv`
- `POST /api/import` with `{ "rows": [...] }`
