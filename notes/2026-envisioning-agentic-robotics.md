# Envisioning Agentic Robotics: A New Era of Robotic Systems

## Source and Reading Focus

- Paper: [Arxiv:2611.18359](https://arxiv.org/abs/2611.18359)
- Venue: Arxiv 2026-11
- First public release: 2026
- Category: Survey
- Task type: Agentic robotics; Manipulation; Navigation
- Reading date: 2026
- Source version: the supplied 84-page v1 PDF.
- Reading focus: Sections 2-3 on architecture, Section 4 on evaluation, and Section 5 on digital versus physical agents. Key architecture and benchmark tables were also inspected visually.

## Main Perspective

The paper frames agentic robotics as a complete decision-making system that interprets intent, selects capabilities, checks effects, and revises subsequent decisions. Its proposed architecture separates three functional responsibilities (PDF pp. 6-10; Figure 3 on p. 7):

- **S2:** a foundation model together with an embodied harness handles intent, reasoning, orchestration, and outcome verification.
- **S1:** callable skills and modules provide learned policies, perception, motion planning, or generated programs.
- **S0:** the body interface and local controllers turn targets into real-time execution.

These are responsibilities, not necessarily separate models. The distinction prevents a controller's local feedback from being confused with the agent's planning or improvement process.

## What Harness Means Here

The core harness components are context management, tool interfaces, planning, memory, and verification (PDF pp. 15-17; Table 1). They determine what the model can observe, call, remember, and check. The paper also distinguishes a sensorimotor loop, a planning loop, and an evolution loop. Improvements in executable skills or context rules can occur with frozen model weights.

For this collection, this supports keeping code repair, skill-library growth, and repository optimization within Harness when they organize execution without primarily learning new model weights.

## Evaluation Lessons

Section 4 separates **model-level capability tests** from **closed-loop system evaluation**. Knowledge, spatial understanding, or a correct answer about a scene does not by itself establish successful task execution.

The comparison protocol matters as much as the benchmark name (PDF pp. 29-36). Record the model and harness versions, observation access, available skills, control abstraction, whether the world pauses during inference, interaction budgets, and independent completion checks. A returned tool success or the agent's own completion claim can differ from actual task completion.

These points inform catalogue selection and reading notes; the homepage keeps the requested four-column format and does not aggregate results across incompatible protocols.

## Benchmarks Relevant to This Repository

- **CodeActionBench:** discussed in Section 4.2, p. 29, when distinguishing model comparisons from complete agent-stack comparisons.
- **CaP-Bench / CaP-X:** Table 4, p. 25, for writing and executing robot programs under different interfaces and feedback conditions. They refer to a benchmark and its framework, not two independent paper entries.
- **EmbodiedSkillBench, RobotWorld, and EmbodiedBench:** Table 4, p. 25, for skill reuse, tool-mediated robot use, and embodied task execution.
- **RoboMME:** Table 5, p. 26, for memory-dependent manipulation. The original benchmark targets generalist policies; an agentic adaptation must state its protocol.
- **RoboQuest:** Table 3, p. 24, and the results discussion for active information gathering and exploratory manipulation.
- **RoboDojo:** Table 3, p. 24, and Tables 8-9 for manipulation and the limits of comparing different system configurations.

The [benchmark guide](../docs/BENCHMARK_GUIDE.md) records the selection and primary sources.

## Application to Games and Robots

The paper concerns robotics. Our extension to games is editorial: retain the same questions about observations, executable actions, feedback, memory, verification, and time. A game API exposing world state and a screenshot-driven game agent have different observation contracts. Game and Robot remain first-class settings in this repository.
