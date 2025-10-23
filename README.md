# ADK Agent Suite — Codelabs & Example Apps

Lightweight collection of ADK agent examples, codelabs, and small apps used for demonstrations and hackathon projects. Each app is self-contained under `agentic-apps/` and includes a short README describing purpose and how to run it.

Highlights
- Focused examples that showcase ADK patterns: agent loops, tools, MCP integration, and domain examples (hotel, personal assistant, renovation).
- Minimal runnable code—each app folder contains startup instructions.
- Secrets and environment variables are intentionally local (`.env`) and are gitignored.

Repository layout (important parts)

  agentic-apps/
    hotel-agent-app/         # Hotel/travel agent example — see its README
    personal_assistant/      # Personal assistant example — see its README
    renovation-agent/        # Renovation/planning agent example — see its README



Quick start (local)

1. Create and activate a Python virtualenv

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -U pip
pip install -r requirements.txt
```

2. Add local secrets

```bash
# copy or create a .env in the app folder you plan to run
cp env.example .env
# or create agentic-apps/<app>/.env with required keys
```

3. Choose an example and follow its README

- agentic-apps/hotel-agent-app/README.md
- agentic-apps/personal_assistant/README.md
- agentic-apps/renovation-agent/README.md

Security and git
- The repository `.gitignore` intentionally excludes `.env` files and Python caches (`__pycache__`, `*.pyc`) so local secrets are not committed. Never add API keys to commits or PR descriptions.

How to contribute
- Add a short README for any new app or notebook explaining purpose, required env vars, and quick run steps.
- Keep secrets out of the repo. Add tests or small examples demonstrating expected usage when adding new agents.

Contact / attribution
- Built by the ADK examples collection. See individual READMEs for credits and references.


agentic-apps/
  hotel-agent-app/          # Hotel agent example (see agentic-apps/hotel-agent-app/README.md)
  personal_assistant/       # Personal assistant example (see agentic-apps/personal_assistant/README.md)
  renovation-agent/         # Renovation agent example (see agentic-apps/renovation-agent/README.md)
```

---


