# Copilot Workspace Instructions

## Mandatory Checklist — run before every commit

1. `uv run ruff check .`
2. `uv run pytest`

## Overview

**Soc Ops** — Social Bingo (FastAPI + Jinja2 + HTMX). Pure game logic in `game_logic.py`; state mutations only in `GameSession` (`game_service.py`). Pydantic models with `frozen=True`. Server-side sessions via signed cookies.

## Conventions

- Use `uv`, never `pip` | Ruff (E, F, I, N, W, ANN, RUF100), line-length 88
- Templates: Jinja2 + HTMX (`hx-post`, `hx-target`, `hx-swap`)
- CSS utilities in `app/static/css/app.css` — see [full list](.github/instructions/css-utilities.instructions.md)
- All JS/CSS vendored in `app/static/`, no external CDN

## Design Guide — Cozy Coffee Shop Theme

- **Fonts**: Gaegu (handwritten headings via `.cozy-heading`) + Nunito (body) — vendored in `app/static/fonts/`
- **Palette** (CSS variables in `:root`): cream, linen, cork, espresso, terracotta, sage, mustard — see `app.css` for full list
- **Components**: `.btn-cozy` (primary), `.btn-back` (nav), `.cozy-card`, `.cozy-header`, `.bg-cork` (board wrapper)
- **Board squares**: `.bingo-square` with `.marked` / `.winning` / `.free-space` modifiers, staggered reveal animation, nth-child rotations
- **Animations**: coffee cup with latte art on BINGO win, coffee spill on reset, stamp check marks, page fade-in