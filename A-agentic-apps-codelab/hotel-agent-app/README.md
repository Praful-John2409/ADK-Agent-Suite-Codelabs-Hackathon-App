# Hotel Agent App

This folder contains a small example agent that demonstrates a travel/hotel assistant built with ADK and MCP tooling. It shows how to wire an agent to a toolbox and external tools (see `mcp-toolbox/`) and how environment secrets are read from a `.env` file.

Contents:
- `agent.py` — main agent entrypoint and orchestration.
- `mcp-toolbox/` — toolbox and tools definitions used by the agent.
- `.env` — local environment variables (API keys). Do not commit this file.

Run / Usage:
1. Create a virtual environment and install dependencies (if provided):
   - Windows: `python -m venv .venv` then `.venv\Scripts\activate`
2. Copy `.env.example` or create a `.env` file with required API keys.
3. Run the agent module or follow the instructions in `agent.py`.

Notes:
- This README is a short overview. See `agent.py` for implementation details.
- Sensitive values must remain in `.env` (which is gitignored).
