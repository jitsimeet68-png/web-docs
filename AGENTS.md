# Агент-исследователь (без написания кода)

**Репозиторий:** `web-docs`
**Цель:** сформировать план и артефакты исследования по теме:
**«Структурированная и проиндексированная документация по написанию кода в Open WebUI (Tools, Functions, Pipe, Actions, Filters)»**

## Область работ (scope)

**Включает:**

* поиск релевантных источников (документация, гайды, примеры);
* создание файлов документации и индекса знаний.

**Исключает:**

* написание исходного кода, правки кода, рефакторинг.

## Результаты (deliverables)

* `docs/sources.csv` — таблица источников и статусов;
* `docs/notes/<номер>_<краткое-название>.md` — конспекты по каждой ссылке;
* `docs/index.md` — дерево/индекс знаний с перекрёстными ссылками.

## Статусы (status_states)

* `found` — найдено
* `read` — прочитано
* `summarized` — суммаризировано
* `doc_created` — создан док-файл

## Модель данных (data_model)

**Заголовки `docs/sources.csv`:**
`["id","url","title","status","path","updated_at"]`

## Рабочий процесс (workflow)

### 1) Инициализация структуры

* создать папки: `docs/`, `docs/notes/`;
* создать файл `docs/sources.csv` с заголовками.

### 2) Поиск ссылок

* найти 15–30 релевантных ссылок;
* добавить строки в `docs/sources.csv` со статусом `found`.

### 3) Линейная обработка ссылок

**Цикл:** `found → read → summarized → doc_created`
Действия:

* прочитать материал; обновить `status="read"`;
* создать конспект в `docs/notes/...`; обновить `status="summarized"` и `path`;
* добавить выводы/термины/ссылки; обновить `status="doc_created"`.

### 4) Построение индекса знаний

* проанализировать все `docs/notes/*.md`;
* сформировать дерево тем и подтем;
* создать `docs/index.md` с оглавлением и ссылками на конспекты.

## Ограничения (constraints)

* никаких команд исполнения и кода; только файлы документации;
* все операции атомарные с фиксацией статуса в CSV.

## Логирование (logging)

* все изменения статусов логировать, обновляя поле `updated_at` в `docs/sources.csv`.

## Готово, когда (done_when)

* нет записей в `docs/sources.csv` со статусами `found`, `read` или `summarized`.

## Проверки качества (quality_checks)

Каждый конспект содержит:

* краткое резюме;
* ключевые термины;
* исходную ссылку.

---

## Предлагаемые улучшения (опционально)

1. **Добавить фронт-матер (YAML) в каждую заметку**
   В начало каждого `docs/notes/*.md` добавить блок с метаданными: `id`, `source_url`, `source_type`, `tags`, `summary`, `updated_at`. Это упростит построение индекса и фильтрацию. Подход широко используется в экосистеме docs-as-code. ([GitHub Docs][1])

2. **Ввести типы материалов и таксономию по Diátaxis**
   Для будущего индекса помечать материалы как `tutorial`, `how-to`, `reference`, `explanation` — это поможет строить дерево знаний, удобное читателю. ([Diátaxis][2])

3. **Правила стиля и читабельности**
   В `CONTRIBUTING.md` кратко описать стиль (простые формулировки, аудитория, глоссарий, примеры). Основываться на рекомендациях Google Tech Writing / Styleguide. ([google.github.io][3])

4. **Автоматическая проверка ссылок (CI)**
   Добавить шаг CI с `lychee` для проверки битых ссылок в `docs/*.md` и `docs/index.md`. Хранить отчёт и поправлять `sources.csv`. ([Docs][4])

5. **Расширить `sources.csv`**
   Полезные поля: `source_type` (docs/blog/spec), `license` (если указано), `notes` (1–2 строки), `diataxis` (тип). Это облегчит сортировку и построение индекса. Рекомендации по структурированию метаданных и фронт-матера — в источниках выше. ([GitHub Docs][1])

6. **Чек-лист качества для заметок**
   В `quality_checks` добавить критерии: уникальное краткое название, оглавление (если >1000 слов), «что это даёт читателю», дата последней проверки, список связанных заметок. Идея «документация как история кода/продукта» — в гайде Google. ([google.github.io][3])

7. **Ориентир на сканируемость**
   Короткие абзацы, списки, выделения — чтобы заметки легко пробегать глазами. ([Archbee][5])

---

Если хотите, я могу сразу предложить 3–4 варианта **промптов для Codex (AGENTS.md)** на эту задачу (в YAML), с учётом предложенных улучшений.

[1]: https://docs.github.com/en/contributing/writing-for-github-docs/using-yaml-frontmatter?utm_source=chatgpt.com "Using YAML frontmatter"
[2]: https://diataxis.fr/?utm_source=chatgpt.com "Diátaxis"
[3]: https://google.github.io/styleguide/docguide/best_practices.html?utm_source=chatgpt.com "Documentation Best Practices | styleguide - Google"
[4]: https://lychee.cli.rs/?utm_source=chatgpt.com "lychee | Docs"
[5]: https://www.archbee.com/blog/technical-writing-best-practices?utm_source=chatgpt.com "Technical Writing Best Practices to Keep In Mind"
