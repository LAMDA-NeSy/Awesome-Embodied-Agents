# Towards Agentic Robots: Model, Data, Environment, and Harness

## Source and Reading Focus

- Paper: [Arxiv:2610.20442](https://arxiv.org/abs/2610.20442)
- Resources: [Awesome-Agentic-Robots](https://github.com/chonghanqin/Awesome-Agentic-Robots)
- Venue: Arxiv 2026-10
- First public release: 2026
- Category: Survey
- Task type: Agentic robotics; Manipulation; Navigation
- Reading date: 2026
- Source version: the supplied 79-page v1 PDF.
- Reading focus: Section 3 and Table 1 for the taxonomy, Section 6.3 and Table 12 for benchmarking, and Section 7 for harness functions and code-based skills. The taxonomy and benchmark tables were also inspected visually.

## Main Perspective

The paper defines agentic robots through how agents organize goal-directed execution: using observations and outcomes to select capabilities, monitor progress, revise decisions, and recover. It also covers agents that develop robot capabilities through data, environments, and learning experiments (PDF pp. 8-10).

Its four functional domains are:

- **Model:** training, perception, planning, robot control, and adaptation.
- **Data:** collection, annotation, and refinement.
- **Environment:** reconstruction, task generation, and benchmarking.
- **Harness:** orchestration, memory, monitoring and recovery, skills, infrastructure, and layered systems.

These seventeen functions are non-exclusive. A paper can contribute to several functions. Our four catalogue categories serve a different purpose: Survey, Harness, Model Training, and Benchmark provide compact reading entry points, while notes can capture additional functions.

## Harness and Code Agents

Section 7 treats the harness as the software that coordinates capabilities, supplies retained information, checks execution, exposes tools, and manages reusable behavior. Code agents fit this wider system through task programs, code repair, skill libraries, and evolving software.

The skill discussion (PDF pp. 39-41) connects Code as Policies, ProgPrompt, and VoxPoser with later runtime programming and persistent code skills. It distinguishes improvements to skill implementations and memory from changes to model weights. Section 7.5 also shows why perception services, control interfaces, execution traces, and tool failure semantics affect the measured agent.

This supports a broader Survey scope while retaining an explicit code mechanism for method entries in the main collection.

## Benchmarking Lessons

Section 6.3 (PDF pp. 29-31) treats a benchmark as a task together with an interface, reset procedure, feedback path, and scoring rule. A task suite alone does not specify the tested capability. A fixed program, a program repaired from the current trace, and an agent that calls a policy are different evaluation conditions.

Table 12 distinguishes the tested system's outputs: answers, actions, skill/tool calls, and programs. It also separates **benchmarks**, **systems evaluated on them**, and **evaluation-construction agents**. Code written by an evaluator does not imply that the agent under test uses code as its action interface.

For this catalogue, an entry in Benchmark therefore need not be a code-only benchmark, but its relevance and tested interface must be documented.

## Benchmarks Relevant to This Repository

- **CaP-X and EmbodiedSWE:** explicit program-based robot evaluation.
- **Embodied Agent Arena:** combines offline capability diagnostics with interactive planning and manipulation; its components should be interpreted separately.
- **RobotWorld:** broader multi-embodiment robot use; code control is an optional interface rather than a requirement of every condition.
- **RoboDojo:** a manipulation suite spanning simulation and real hardware, with generalist-policy origins and later agent evaluations.
- **EmbodiedBench:** planning and execution at different action abstractions, including navigation and manipulation.

All appear in Section 6.3 and Table 12. Other useful references there include PARTNR for collaboration, KinDER for physical reasoning, and memory or safety benchmarks. They are discovery leads rather than automatically admitted code-agent methods.

## Consequences for Repository Organization

Keep the requested four paper columns. Use the two supplied system-level papers as the leading Survey references. Expand Benchmark to cover direct code execution and complementary embodied capabilities. Preserve Game and Robot scope, and record exact interfaces and experimental conditions in the [benchmark guide](../docs/BENCHMARK_GUIDE.md) or individual reading notes.
