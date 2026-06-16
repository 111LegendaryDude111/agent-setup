# OKF Template

Этот шаблон используется для project knowledge base в каталоге `knowledge/`.

OKF concept: один markdown-файл с YAML frontmatter. Путь файла внутри `knowledge/` является identity concept-а.

## Рекомендуемая структура каталогов

```text
knowledge/
├── index.md
├── data-sources/
├── tables/
├── metrics/
├── features/
├── rules/
├── models/
├── pipelines/
├── apis/
└── playbooks/
```

`index.md` и `log.md` являются зарезервированными именами OKF. Не использовать их как concept-файлы.

## Concept File Template

````md
---
type: "<Concept Type>"
title: "<Human-readable title>"
description: "<One sentence summary>"
owner: "<team/person or TODO>"
tags: ["tag1", "tag2"]
status: "draft"
timestamp: "YYYY-MM-DDTHH:MM:SSZ"
---

# <Title>

## Purpose

Коротко: зачем существует concept и какую проблему решает.

## Source of Truth

Ссылки или пути к источникам: код, SQL, config, dashboard, ticket, внешняя документация.

## Definition

Точное определение concept-а. Не смешивать факты с предположениями.

> Assumption: использовать только если вывод сделан агентом и не подтвержден источником.

> TODO: confirm with owner - использовать, если важная информация неизвестна.

## Inputs / Schema

| Field | Type | Description | Source |
| --- | --- | --- | --- |
| `<field>` | `<type>` | `<description>` | `<path or link>` |

## Business Rules

* `<rule>`

## Usage Examples

```text
<example>
```

## Common Mistakes

* `<mistake>`

## Related Knowledge

* [Related concept](/path/to/concept.md)

## Validation Checks

* `<check>`

## Citations

[1] [Source title](<source-url-or-path>)

## Review Notes

> TODO: requires human review - обязательно для critical knowledge.

## Change Log

| Date | Author | Change |
| --- | --- | --- |
| YYYY-MM-DD | agent | Created draft concept. |
````

## Directory Index Template

```md
# <Knowledge Area>

* [Concept title](concept.md) - one sentence description.
* [Subdirectory](subdir/) - one sentence description.
```

## Directory Log Template

```md
# Directory Update Log

## YYYY-MM-DD

* **Creation**: Created [Concept title](/path/to/concept.md).
* **Update**: Updated definition for [Concept title](/path/to/concept.md).
```

## Writing Rules

* Не выдумывать бизнес-факты, thresholds, owners или source-of-truth.
* Для неподтвержденного вывода использовать `> Assumption: ...`.
* Для неизвестных данных использовать `> TODO: confirm with owner`.
* Для fraud thresholds, billing logic, security rules, model thresholds и production runbooks оставлять `status: "draft"` до human review.
* В `## Change Log` писать только содержательные изменения knowledge, а не команды агента.
