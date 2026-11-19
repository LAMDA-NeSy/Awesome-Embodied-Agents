# Benchmark Selection and Interpretation

## Reference Basis

The robotics selection draws on two system-level references:

- [Envisioning Agentic Robotics](https://arxiv.org/abs/2611.18359), especially Section 4, Tables 3-6 and 8-9, and the evaluation principles on PDF pp. 29-31. See the [reading note](../notes/2026-envisioning-agentic-robotics.md).
- [Towards Agentic Robots](https://arxiv.org/abs/2610.20442), especially Section 6.3 and Table 12 on PDF pp. 29-31. See the [reading note](../notes/2026-towards-agentic-robots.md).

The game-agent expansion follows [Towards Generalist Game Agents](https://arxiv.org/abs/2605.09965), Section 6 and Table 7. The [game-agent guide](GAME_AGENT_GUIDE.md) records the selected benchmarks, interfaces, primary sources, and hybrid-paper assignments.

Page references identify the supplied v1 PDFs. Paper titles, first-release dates, available official code links, and recorded venues were checked against the original papers or author resources when adding entries.

## Two Roles for Benchmark Entries

**Direct embodied coding evaluation** tests generated programs and their execution, repair, or interaction with robot tools. **Complementary agentic evaluation** tests capabilities needed by these systems, such as memory, exploration, planning, or skill use, possibly through action or skill-call interfaces.

Both can inform code-agent research. Their presence in the catalogue does not mean that every benchmark subject is a coding agent, or that every subtest is closed-loop. The homepage retains Paper, Venue, Task, and Links, with the primary paper linked through its title; this guide supplies interpretation without adding columns.

## Direct Program-Based Evaluation

### Embodied First Exam

- Source: Envisioning, Section 4.2, PDF p. 30; supplemented with the original paper and official repository.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2611.12177) · [💻&nbsp;Code](https://github.com/mll-lab-nu/embodied-first-exam) · [🌐&nbsp;Project](https://www.embodied-first-exam.ai/)
- First Arxiv submission month: 2026-11. The catalogue displays `Arxiv<br>2026-11`.
- Coding agents can choose direct control, executable control programs, or training a policy. Tasks include spatial puzzles, dexterous manipulation, multi-robot interaction, dynamic whole-body control, and sim-to-sim engineering.
- Keep Standard, Realtime, and Privileged results separate: they differ in observable state, reset access, and whether the environment advances while the agent reasons.

### CaP-X / CaP-Bench

- Source: Towards, Section 6.3 and Table 12; Envisioning, Table 4.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2603.22435)
- Generated programs compose perception and control primitives. State access, API abstraction, execution feedback, and visual grounding can change the evaluated difficulty.
- Keep the framework and its benchmark under the same paper entry; do not duplicate CaP-Bench as a second paper.

### EmbodiedSWE

- Source: Towards, Section 6.3 and Table 12.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2609.27308)
- Coding agents use simulator access and execution feedback to solve long-horizon robot tasks. The paper also studies trajectory generation and agent improvement.
- Distinguish the benchmark, solver conditions, and downstream policy-learning components when comparing results.

### CodeActionBench

- Source: Envisioning, Section 4.2, p. 29.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2609.33807)
- Agents write, execute, and revise manipulation programs through a shared robot API; hidden physical-outcome verification supports evaluation.
- Comparisons of complete coding-agent stacks should be identified separately from experiments that hold the harness fixed while changing the model.

## Broader Agentic Evaluation

### RobotWorld

- Source: Towards, Section 6.3 and Table 12; Envisioning, Tables 4, 6, and 8.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2610.10409)
- Tests robot use across manipulation, mobile manipulation, locomotion, driving, and aerial control.
- Record whether a condition uses direct actions or optional code control. Diverse embodiments alone do not establish matched cross-embodiment transfer.

### Embodied Agent Arena

- Source: Towards, Section 6.3 and Table 12.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2610.00854)
- Covers geometry, spatial reasoning, affordance, task planning, and manipulation. Its offline diagnostics and interactive execution components provide different evidence.
- Report the exact component and interface. Error-free code execution and completed task goals are separate outcomes.

### Embodied Skill Bench / EmbodiedSkillBench

- Source: Envisioning, Table 4 and Section 4.2.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2610.16238)
- Compares native control, skill-only execution, and agent-directed reuse of packaged embodied skills.
- Report the skill provisioning and action interface. A native-control condition still has robot control tools; it is not an interface-free system.

### RoboDojo

- Source: Towards, Section 6.3 and Table 12; Envisioning, Tables 3, 8, and 9.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2607.04434)
- A sim-and-real manipulation suite designed for generalist robot policies and also used for agent evaluations.
- Agent performance depends on the adapter, task knowledge, allowed state, feedback, and action budget. The suite name does not identify a unique coding-agent protocol.

### RoboMME

- Source: Envisioning, Table 5 and Section 4.3.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2603.04639)
- Memory-dependent manipulation spans temporal, spatial, object, and procedural memory. The original study evaluates generalist policies.
- An agentic adaptation must disclose its history, memory mechanism, controls, and timing; it should not be described as the original benchmark's native code-agent setting.

### RoboQuest

- Source: Envisioning, Table 3 and Section 4.3.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2610.10388)
- Mobile manipulation requires searching for hidden information, inspecting objects, and testing unfamiliar mechanisms before declaring completion.
- The reported visuomotor interface is broader agentic evaluation, not a program-synthesis-only test. Preserve information-gathering and completion-decision conditions when adapting it.

### EmbodiedBench

- Source: Towards, Section 6.3 and Table 12; Envisioning, Table 4.
- [📄&nbsp;Primary paper](https://arxiv.org/abs/2502.09560)
- Covers household planning, navigation, and manipulation at different abstraction levels.
- Identify the environment and concrete action/skill interface. High-level task planning and low-level motor execution should not be interpreted as the same evaluation.

## Information to Record for Comparisons

Record the following in individual reading notes:

1. The exact environment, task split, simulator version, and robot embodiment.
2. Whether the result tests a model, a harness under a fixed model, or a complete system.
3. The observation and action interface, including privileged state and supplied skills.
4. Whether code is generated before execution, repaired during execution, or improved between attempts.
5. Whether the environment advances while the model reasons.
6. Calls, physical steps, retries, token use, wall-clock time, and human assistance.
7. Independent success verification and whether success signals are visible to the agent.
8. Repetitions and per-task outcomes, rather than only an aggregate success number.

The same considerations apply when adding game benchmarks. The two source references focus on robotics; their benchmark lists should not determine which games belong in the repository.
