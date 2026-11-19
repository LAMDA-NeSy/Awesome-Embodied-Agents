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
5. Sort by the month shown in Venue, newest first within the category. Within the same month, sort by full title in ascending alphabetical order, ignoring case.

```markdown
| Paper | Venue | Task | Links |
| :--- | :---: | :--- | :--- |
| **[Full Paper Title](PAPER_URL)** | ICML<br>2024-07 | Object Manipulation; Indoor Navigation | [💻&nbsp;Code](CODE_URL)<br>[🌐&nbsp;Project&nbsp;Page](PROJECT_URL) |
```

For a preprint with only a paper link:

```markdown
| **[Full Paper Title](PAPER_URL)** | Arxiv<br>YYYY-MM | Minecraft | — |
```

## Column Conventions

- **Paper:** link only the full paper title to the primary paper. Retain names that appear in the official title.
- **Venue:** write the formal venue and month on separate lines using `<br>`. Use the conference month for conference papers and the issue month or publisher's publication month for journal articles. For preprints, use `Arxiv<br>YYYY-MM` with the first public preprint month and link the title to the original source.
- **Task:** capitalize the first letter of each word while preserving acronyms and existing capitalization within names. Separate multiple tasks with semicolons.
- **Links:** include only available official `[💻 Code]` and `[🌐 Project Page]` links, one per line using `<br>`. Keep the icon inside the clickable label and use `&nbsp;` between label words to prevent wrapping. Use `—` when neither link is available. An official survey companion collection can serve as its Project Page; keep other resources and reading-note links in supporting documents.

Verify venues and dates against the publisher, conference, or authors. Record agent setup, environment details, and code artifacts in notes as needed. Label partial releases and third-party code in the notes.

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
- Venue names and verified months appear on separate lines. Preprint rows use `Arxiv<br>YYYY-MM`.
- Rows are sorted newest first by the month shown in Venue, with same-month titles alphabetized case-insensitively.
- Markdown tables, local links, and navigation work in Preview.
- New notes are included in the note index.

Suggested PR titles: `Add: Paper Name`, `Fix: Resource Link`, or `Notes: Paper Name`.
