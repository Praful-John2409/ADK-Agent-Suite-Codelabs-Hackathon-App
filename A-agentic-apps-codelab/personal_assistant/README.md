# Personal Assistant

This folder contains a personal assistant agent implemented with ADK. The agent demonstrates custom functions, integrations with third-party tools, and example custom agents.

Contents:
- `agent.py` — entrypoint for the personal assistant.
- `custom_agents.py` — example agent classes and presets.
- `custom_functions.py` — helper functions exposed to the agents.
- `third_party_tools.py` — integrations and adapters for external services.
- `.env` — environment variables for API keys and secrets. Do not commit this file.

Run / Usage:
1. Create/activate a virtual environment.
2. Add your API keys to `.env`.
3. Inspect `agent.py` to see how the assistant is started and configured.

Demo
----

Watch a short demo of this agent here:

https://youtu.be/FTIL9peodW0

Notes:
- Keep secrets out of source control; `.env` is ignored by the repository-level `.gitignore`.
