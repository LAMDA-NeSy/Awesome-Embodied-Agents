# Contributing

Contributions to the paper catalogue, environment resources, reading notes, and metadata corrections are welcome. Please write repository content in English.

## Check the Scope

Read [docs/TAXONOMY.md](docs/TAXONOMY.md). Include code-generation, code-agent, and embodied harness research grounded in games or robotics, covering both custom frameworks and general-purpose coding agents.

For code-based methods, identify what code the agent creates or modifies, where it is executed, what feedback it receives, and which embodied tasks establish relevance. For tool/skill or action-interface harnesses, describe the runtime, model-facing interface, feedback, and substantive orchestration mechanism; do not assume executable program generation. See the [harness guide](docs/HARNESS_GUIDE.md). Survey entries may cover system-level agentic robotics; benchmark entries may provide broader embodied-agent evaluation. For benchmarks, record the measured capability and tested interface in the [benchmark guide](docs/BENCHMARK_GUIDE.md) or a reading note.

Model Training also includes native game/robot-use models. For these entries, identify the foundation or reasoning model being trained, the objective, the embodied training tasks, and whether deployment outputs code, tool calls, or structured actions. Record these details in a reading note, as in the [PEAR example](notes/2026-pear.md).

## Add a Paper

1. Search [README.md](README.md) for the title or Arxiv identifier to avoid duplicates.
2. Select one category: `Survey`, `Harness`, `Model Training`, or `Benchmark`, in that display order.
3. Insert one row using the four-column format below.
4. Verify publication information, task types, and official links with primary sources.
5. Sort by first paper release month (`YYYY-MM`), newest first within the category; use Arxiv v1 when available, otherwise the first official paper release. Within the same month, sort by the full paper title in ascending, case-insensitive alphabetical order; do not use the day or method alias to break ties.

```markdown
| Paper | Venue | Task | Links |
| :--- | :---: | :--- | :--- |
| **[Full Paper Title](PAPER_URL)** | ICML 2024<br>Arxiv 2024-02 | Manipulation; Navigation | [💻&nbsp;Code](CODE_URL)<br>[🌐&nbsp;Project&nbsp;Page](PROJECT_URL) |
```

For an Arxiv preprint with only a recorded paper link:

```markdown
| **[Full Paper Title](PAPER_URL)** | Arxiv YYYY-MM | Minecraft | — |
```

## Column Conventions

- **Paper:** link the full title directly to the primary paper. Keep an optional method alias outside the title link.
- **Venue:** show the first Arxiv submission month (v1) as `Arxiv YYYY-MM`, for example `Arxiv 2026-11`. For published papers, retain the verified conference/journal and edition year on the first line, followed by the Arxiv month on a second line, for example `ICML 2024<br>Arxiv 2024-02`. For work without Arxiv, record the first official release as `Released YYYY-MM` beneath the venue.
- **Task:** use concrete game names or tasks, such as `Minecraft`, `Manipulation`, `Navigation`, or `Locomotion`. Separate multiple tasks with semicolons.
- **Links:** include only available official `[💻 Code]` and `[🌐 Project Page]` links, one per line using `<br>`. Keep the icon inside the clickable label and use `&nbsp;` between label words to prevent wrapping. Use `—` when neither link is available. An official survey companion collection can serve as its Project Page; keep other resources and reading-note links in supporting documents.

Use a venue year from an official publication page or author announcement. A general coding engine is not necessarily the full embodied experiment release; label partial releases precisely in notes. Clearly mark third-party code as `Unofficial`.

The sorting month is Arxiv v1 when available, even if a later conference/journal venue is recorded. The venue edition year and first release month describe different events; do not combine the edition year with an unrelated Arxiv month. Record agent setup, environment details, and code artifacts in notes as needed.

## Category Boundaries

Use the primary contribution to select a category. Model Training focuses on weight updates to the foundation, reasoning, or code-generation model that serves as the embodied agent. Harness covers code execution and repair, tool/skill orchestration, grounded action interfaces, memory, verification, external harness optimization, and workflows that train a separate downstream robot policy. Follow the main contribution for papers that include both runtime design and model training; do not duplicate rows. See the [boundary examples](docs/TAXONOMY.md#boundary-examples).

## Add Resources or Reading Notes

- Add environment and interface resources to [docs/RESOURCES.md](docs/RESOURCES.md).
- Copy [notes/TEMPLATE.md](notes/TEMPLATE.md) to `notes/YYYY-short-name.md` for a reading note.
- Add the note to [notes/README.md](notes/README.md).
- Distinguish the authors' findings, your interpretation, and unresolved questions.

## Before Submitting

- The contribution fits the code-agent and game/robot scope and is not a duplicate.
- The category follows the paper's primary contribution.
- Every paper row has exactly four columns.
- Venue, task names, and official links are verified; first release months use `YYYY-MM`, with preprints shown as `Arxiv YYYY-MM`.
- Rows are sorted by first release month, using Arxiv v1 when available, newest first; same-month titles are alphabetized case-insensitively.
- Markdown tables, local links, and navigation work in Preview.
- New notes are included in the note index.

Suggested PR titles: `Add: Paper Name`, `Fix: Resource Link`, or `Notes: Paper Name`.
