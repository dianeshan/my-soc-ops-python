🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# Soc Ops 🎯

> Turn awkward intros into a fast, social game.

**Soc Ops** is a Social Bingo app for in-person mixers, team offsites, and community events.
Players move around the room, find people who match each prompt, and race to complete **5 in a row**.

[![Python 3.13+](https://img.shields.io/badge/python-3.13%2B-3776AB?logo=python&logoColor=white)](pyproject.toml)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115%2B-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Why it works

- ✅ Breaks the ice quickly without forced small talk
- ✅ Keeps everyone moving and interacting
- ✅ Simple rules, instant engagement

## How gameplay works

1. Start a game to generate your bingo board.
2. Find people who match the prompts.
3. Mark matching squares.
4. Get 5 in a row to win.

## Run locally in 60 seconds

```bash
uv sync
uv run uvicorn app.main:app --reload
```

Then open `http://127.0.0.1:8000`.

## For contributors

Mandatory checks before commit:

```bash
uv run ruff check .
uv run pytest
```

## Lab Guide

| Part | Title |
|------|-------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Overview & Checklist |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Setup & Context Engineering |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Design-First Frontend |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Custom Quiz Master |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Multi-Agent Development |

> 📝 Offline versions are available in [`workshop/`](workshop/).
