# Maintaining the Collection

## Add a Paper

1. Check the code-agent and game/robot scope in [TAXONOMY.md](TAXONOMY.md).
2. Open [README.md](../README.md) and choose Survey, Harness, Model Training, or Benchmark according to the primary contribution; keep that section order.
3. Copy the row format from [CONTRIBUTING.md](../CONTRIBUTING.md).
4. Fill Paper, Venue, Task, and Links. Link the full paper title directly to the primary paper. Show the Arxiv v1 month as `Arxiv YYYY-MM`; for published papers, keep the verified venue and edition year above it using `<br>`. For papers without Arxiv, use `Released YYYY-MM` for the first official release. Links contains only official 💻 Code and 🌐 Project Page links, one per line using `<br>`; use `—` if neither is available.
5. Insert the paper by first release month, newest first within its category. Sort titles within the same month in ascending, case-insensitive alphabetical order using the full title, without considering the day or method alias.
6. For detailed reading, copy [notes/TEMPLATE.md](../notes/TEMPLATE.md) and update the [note index](../notes/README.md).
7. When adding or removing papers, update the `papers` badge count and its alt text in `README.md` to match the total number of paper rows across the four categories.

The paper catalogue is maintained directly in Markdown. No build or synchronization step is required.

## Edit on GitHub

Open `README.md` in your repository, choose Edit, make the change, and inspect Preview before committing. Use Add file to create a reading note.

Contributors can suggest papers through **Issues → New issue → Add a paper**, report metadata errors, or submit a PR. The templates request the category, publication, task types, and source links.

## Edit Locally

After editing the relevant files:

```bash
git add README.md CONTRIBUTING.md LICENSE docs/ notes/ .github/ assets/
git commit -m "Add: Paper Name"
git push
```

Stage the paths you actually changed. Update the taxonomy and issue-form category options together if you rename a category.

## Repository and Authentication

The collection is hosted at [LAMDA-NeSy/Awesome-Embodied-Agents](https://github.com/LAMDA-NeSy/Awesome-Embodied-Agents).

Suggested GitHub description:

```text
This project aims to collect and curate research papers on code agents for embodied intelligence in games and robotics, including but not limited to surveys, agent harnesses, model training and post-training methods, and benchmarks.
```

Authenticate the GitHub CLI if necessary:

```bash
gh auth login --hostname github.com --git-protocol https --web
```

For a local checkout without a remote, connect the existing repository:

```bash
git remote add origin https://github.com/LAMDA-NeSy/Awesome-Embodied-Agents.git
```

If `origin` already exists, check `git remote -v` before making changes. Fetch and inspect the remote branch before pushing so that existing contributions are preserved. Push the current branch with `git push -u origin main` after committing the intended changes.

The README's contributors, last commit, Stars, and Forks badges use this repository's live GitHub data. Keep their image and destination URLs in sync if the repository is renamed or transferred. The Papers badge is maintained with the paper catalogue.

Suggested topics: `awesome-list`, `coding-agents`, `code-as-policies`, `embodied-ai`, `game-agents`, `robotics`, `program-synthesis`.

## Expand the Catalogue

Keep the section order Survey, Harness, Model Training, Benchmark and the four-column table format consistent. Use specific game titles and task names in Task. Add formal publication information above `Arxiv YYYY-MM` when verified, retaining the first release month and the same-month alphabetical sorting rule.

Record agent setup, exact environment interfaces, observation privilege, rollout budgets, and adaptation details in reading notes. Keep environment resources in [RESOURCES.md](RESOURCES.md).

For Harness additions, use [HARNESS_GUIDE.md](HARNESS_GUIDE.md) to distinguish executable programs, tool/skill orchestration, semantic actions, and external harness optimization. A model with a code repository is not automatically a coding agent. Verify the evaluated runtime and assign hybrid papers once by their primary contribution.
