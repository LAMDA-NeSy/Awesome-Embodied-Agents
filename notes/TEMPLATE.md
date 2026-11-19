# Paper Title

## Metadata

| Field | Value |
| :--- | :--- |
| Paper | Full title and primary-source link |
| Authors / institutions | As reported in the paper |
| Venue | `Arxiv YYYY-MM` using Arxiv v1; retain any verified venue and edition year above it with `<br>` |
| First public release month | YYYY-MM; use Arxiv v1 when applicable |
| Code / project | Official links; use `—` when not recorded |
| Category | Survey / Harness / Model Training / Benchmark |
| Task | Specific game titles or robot tasks |
| Domain | Game / Robot / Game + Robot |
| Agent setup | Custom / General-purpose / Not applicable (native-use model) / Unspecified |
| Reading year / status | YYYY; To read / In progress / Read / Reproduced |

## One-Sentence Summary

What does the agent program or learn, for which embodied task, and with what key mechanism?

## Scope and Classification Evidence

- Generated or edited code artifact:
- Game or robot contribution:
- Evidence for the primary category:
- Evidence for Custom versus General-purpose setup, with a paper section or official implementation link:
- Actual coding-agent harness and language model, recorded separately:
- For Model Training: which foundation/reasoning/code-generation model receives weight updates, and what does it output during deployment?
- For native-use training references without program generation: record the action interface and mark code-specific fields Not applicable.
- For tool/skill or semantic-action harnesses without program generation: describe the runtime and model-facing interface; mark code-generation fields Not applicable.

## Environment and Interface

| Aspect | Details |
| :--- | :--- |
| Environment | Game title / simulator / robot platform |
| Embodiment | Avatar, controllable units, robot arm, mobile robot, or other interface |
| Deployment | Game / robot simulation / physical robot |
| Observations | Screenshots, depth, poses, world-state APIs, proprioception, etc. |
| Privileged information | What information is exposed that a deployed agent or human would not normally observe? |
| Action interface | Game API, keyboard/mouse, skill SDK, Cartesian commands, joint control, etc. |
| World clock | Does the environment advance or pause during model inference? |
| Human-provided scaffolding | Primitive skills, maps, demonstrations, task-specific code, API documentation |
| Reset and verification | How resets and success judgments are implemented; any human involvement |

## Code-Agent Loop

| Component | Details |
| :--- | :--- |
| Program artifact | Task script, callable skill, reward, environment generator, policy repository, etc. |
| Generation / editing | Prompt pipeline, agent tools, file editing, search operator, or other mechanism |
| Execution | Runtime, sandbox, simulator, robot SDK, and execution granularity |
| Feedback | Errors, stdout, images, reward, success predicates, or human feedback |
| Repair | What is revised, when, and under what retry budget? |
| Persistence | Reusable code, skill library, notes, repository, learned weights, or none |
| Agent organization | Single agent, planner/executor, team, or other configuration |

## Adaptation and Deployment

- When is code generated: before deployment, during task execution, or between episodes?
- What is optimized: a program, a skill library, a reward, model weights, or a full codebase?
- What remains fixed during evaluation?
- Does deployment retain the coding agent, run frozen code, or use a learned policy?

### Agent-Model Training

- Trained agent model and initialized checkpoint:
- Parameters updated and parameters kept fixed:
- Training objective: SFT, RL, or other:
- Training data or environments and reward/supervision source:
- Agent output interface: executable code, tool calls, or structured actions:
- Is a separate downstream robot policy trained? How does it relate to the agent model?

## Main Contributions

1. Central method and generated artifact:
2. Difference from the closest code-agent baseline:
3. Ablation or evidence supporting the proposed mechanism:

## Evaluation

| Item | Record |
| :--- | :--- |
| Tasks and exact environment versions | |
| Model and agent-harness configurations | |
| Baselines and matched scaffolding | |
| Success metrics and number of trials | |
| Wall-clock / token / rollout / training budgets | |
| Transfer across tasks, environments, or embodiments | |
| Main results and source table/figure | |
| Failure cases and intervention rate | |

## Interpretation and Open Questions

- Limitations stated by the authors:
- My interpretation, clearly distinguished from reported evidence:
- Unresolved questions:
- Comparability with papers using different observations or action abstractions:

## Connections and Next Steps

- Related Game / Robot papers in the same catalogue category:
- Relevant differences between Custom and General-purpose setups:
- Follow-up reading or reproduction actions:

## References

Add official BibTeX if useful. Cite paper sections, figures, and tables for detailed claims.
