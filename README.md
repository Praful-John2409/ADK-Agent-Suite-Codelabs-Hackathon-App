# ADK Agent Suite — Codelabs + Hackathon App

A compact repo implementing:

* **A1**: *From Prototypes to Agents with ADK*
* **A2**: *ADK Agents with Tools*
* **A3**: *Travel Agent using MCP (DB) + ADK*
* **B**: One **hackathon** agent app from `awesome-adk-agents`

Each has runnable code (Colab and/or desktop app) and a short YouTube walkthrough.

---

## Structure

```
notebooks/
  a1_prototypes_to_agents.ipynb
  a2_adk_tools.ipynb
  a3_travel_agent_mcp_db.ipynb
  b_hackathon_<project>.ipynb   # optional

apps/
  a1_prototypes_to_agents/
  a2_adk_tools/
  a3_travel_agent/
  b_hackathon_<project>/

adk/agents/   adk/tools/   mcp/{servers,configs}/   data/   scripts/
env.example   requirements.txt
```

---

## Quick Start

### Run in Colab (zero setup)

Open a notebook under `notebooks/` and run the **Setup** cell, then the **Demo** cell:

* A1 → `a1_prototypes_to_agents.ipynb`
* A2 → `a2_adk_tools.ipynb`
* A3 → `a3_travel_agent_mcp_db.ipynb`
* B  → `b_hackathon_<project>.ipynb` (if provided)

### Run locally (desktop app)

```bash
git clone <repo-url> && cd <repo>
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -U pip && pip install -r requirements.txt
cp env.example .env                                  # add API keys as needed
# Pick an app to run:
streamlit run apps/a3_travel_agent/App.py
# or
uvicorn apps/a2_adk_tools.main:app --reload --port 8000
```

---

## Environment

Copy `env.example` → `.env` and fill what you need:

```
OPENAI_API_KEY=
ANTHROPIC_API_KEY=
GOOGLE_API_KEY=
TAVILY_API_KEY=
GOOGLE_MAPS_API_KEY=
SQLITE_PATH=./data/travel.sqlite
MCP_CONFIG=./mcp/configs/client.json
```

---

## What Each Part Shows

* **A1 – Prototypes → Agents:** ADK agent loop, memory/scratchpad, simple planning.

  * Colab: `notebooks/a1_prototypes_to_agents.ipynb`
* **A2 – Tools with ADK:** Tool schemas, routing/policies, logs.

  * Colab: `notebooks/a2_adk_tools.ipynb`
* **A3 – Travel Agent (MCP + DB):** MCP SQLite, itinerary planning, web/maps lookups.

  * Seed DB: `python scripts/seed_travel_db.py`
  * Colab: `notebooks/a3_travel_agent_mcp_db.ipynb`
  * App: `apps/a3_travel_agent/`
* **B – Hackathon App:** One project from the list, packaged as an app.

  * App: `apps/b_hackathon_<project>/`

---

## Videos (add links)

* A1 Walkthrough: `<YouTube A1>`
* A2 Walkthrough: `<YouTube A2>`
* A3 Walkthrough: `<YouTube A3>`
* B App Walkthrough: `<YouTube B>`

---

## Notes

* Python 3.10+ recommended.
* Do **not** commit real keys; use `.env`.
* If MCP won’t connect, verify `MCP_CONFIG` and that your SQLite file exists.

---

## License

MIT (see `LICENSE`).
