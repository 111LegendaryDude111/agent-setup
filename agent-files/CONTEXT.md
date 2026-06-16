# Project Context

## Purpose

Кратко: зачем существует проект, какую проблему решает, кто пользователь, какой основной бизнес/технический контекст.

## Current State

- Статус проекта:
- Основной стек:
- Основные entrypoints:
- Критичные ограничения:

## Key Decisions

| Date | Decision | Reason | Impact |
|---|---|---|---|
| 2026-06-14 | Example decision | Why | What changed |
| 2026-06-16 | OKF knowledge base rule added to agent contract | Важные знания проекта должны жить в agent-readable markdown, а не только в handoff или комментариях | `AGENTS.md` теперь описывает, когда читать/писать `knowledge/`, а `agent-files/OKF_TEMPLATE.md` задает шаблон concept-файла |

## Implemented Features

| Date | Feature | Summary | Files / Modules | Notes |
|---|---|---|---|---|
| 2026-06-14 | Example feature | What was done | `src/...` | Important details |

## Architecture Notes

- Основные компоненты:
- Потоки данных:
- Интеграции:
- Где нельзя ломать интерфейсы:

## Known Constraints

- Не делать over-engineering.
- Не добавлять Docker/microservices без явной необходимости.
- Предпочитать `uv`, `pyproject.toml`, `pytest`, lightweight MVP stack.
- Все рискованные изменения — маленькими PR/changesets.
- Для задач с кодом обязательны `$karpathy-guidelines`, `$caveman` и `$ponytail`.
- Если проект использует `knowledge/`, агент должен вести его в стиле OKF и обновлять только при появлении переиспользуемого знания.

## Open Questions

| Date | Question | Owner | Status |
|---|---|---|---|
| 2026-06-14 | Example | David | Open |
