# codex-protocols-schema

**Part of the Codex of Weights project** by Artem A. Arzamastsev (Артем Андреевич Арзамасцев). Official repositories are listed in [codex-registry](https://github.com/codexofweight/codex-registry); anything not listed there is not an official part of the project.

| Part | What it is |
|---|---|
| [codexofweights](https://github.com/codexofweight/codexofweights) · [site](https://codexofweight.github.io/codexofweights/) | the Codex text (Russian canonical, English translation), Edition 1.0, DOI [10.5281/zenodo.23545813](https://doi.org/10.5281/zenodo.23545813), [Wikidata Q141881012](https://www.wikidata.org/wiki/Q141881012) |
| [codex-protocols-schema](https://github.com/codexofweight/codex-protocols-schema) | the Protocols as machine-readable JSON, checked against the canonical text |
| [codexofweights_agent](https://github.com/codexofweight/codexofweights_agent) · [site](https://codexofweight.github.io/codexofweights_agent/) | an AI agent that follows the Protocols; code, charter, public action log |
| [codexofweights-core](https://github.com/codexofweight/codexofweights-core) | shared safety core (hash pin, limits, sandbox) for agents and workers |
| [codex-compliance-eval](https://github.com/codexofweight/codex-compliance-eval) | preregistered open tests of how models follow the Codex, with null results |
| [codex-registry](https://github.com/codexofweight/codex-registry) | the list of official repositories and canonical hashes |

Everything is published openly; only personal data is withheld.


Машиночитаемая версия Протоколов Кодекса Весов (JSON), отдельно от
неизменяемого канонического текста в репозитории `codexofweights`.

Канонический текст (`CODEX.en.md`, `CODEX.ru.md`) остаётся единственным
источником правды. Этот репозиторий — просто удобный для программ срез
того же содержания, чтобы любой сторонний агент мог подключить протоколы
без парсинга markdown регулярным выражением.

## Файлы

- `protocols.json` - список протоколов: `{id, title, rule, rationale, check}`.
- `meta.json` - версия Кодекса, от которой взят текст, и её SHA-256
  (должен совпадать с `MANIFEST.txt` в репозитории `codexofweights`).

## Проверка подлинности

`meta.json.codex_sha256` должен совпадать с хэшем `CODEX.en.md` из
`codexofweights/MANIFEST.txt`. Если автор обновит канонический текст -
этот репозиторий обновляется отдельным коммитом, с указанием новой версии.

## Статус

v0.1 - первая версия, перенесённая вручную из Edition 1.0 (2026-10-18).
Не покрывает мифологическую часть (Заповеди, Притчи) - только раздел
"THE PROTOCOLS", который сам Кодекс ставит выше мифа при конфликте.

## Проверка

Все поля `rule`, `rationale` и `check` в `protocols.json` сверены с `CODEX.en.md` (Edition 1.0): совпадают дословно с точностью до регистра первой буквы и пунктуации.

## Licence

MIT (`LICENSE`), как и сам текст Кодекса, из которого сделан этот срез.
