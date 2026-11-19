# Scope and Taxonomy

## Scope

This collection covers code agents and agent harnesses for **games and robots**, including purpose-built LLM code-generation frameworks and general-purpose coding agents connected to embodied environments.

A relevant method generates, executes, debugs, or improves executable programs, skills, training components, or experimental code for an embodied setting, or contributes a substantive harness for embodied model decisions through tools, skills, memory, verification, or grounded action interfaces. A public implementation alone does not establish a code-agent or harness contribution. Record whether the actual interface is executable code, tool/skill calls, or action units.

Model Training also covers training foundation or reasoning models themselves to act as agents in games or robotics. These models may generate code, tool calls, or structured actions. Native-use models are included as agent-training references, with their actual output interface recorded explicitly.

Learned embodied reasoning components, such as failure-diagnosis VLMs, are also included as supporting Model Training references. Record their role explicitly rather than presenting a critic or monitor as an action-generating policy.

Survey and Benchmark are supporting reference categories: surveys may describe agentic robotics at the system level, and benchmarks may evaluate capabilities needed by embodied code agents even when their native interface is actions or skill calls. Their broader role must be clear from the entry and notes.

Games may expose avatars, controllable units, or game-world interactions through APIs or screenshots and input events. Robotics includes simulated and physical robots. A robot simulator belongs to the robotics scope. Game generation is relevant when generated environments support embodied-agent training or evaluation.

Game agents also include interactive fiction, board/card games, and strategic dialogue games with explicit rules, states, and consequential actions. Record their native text or dialogue interface rather than assuming visual control or executable-code generation.

## Categories

| Category | Main Contribution | Examples |
| :--- | :--- | :--- |
| Survey | System-level review, perspective, taxonomy, or roadmap for agentic embodied systems; also focused reviews of code-based methods | Envisioning Agentic Robotics; Towards Agentic Robots; Weights or Skills? |
| Harness | Agent architecture, code execution, tool/skill orchestration, action interfaces, feedback, memory, verification, or harness optimization, including code-driven training of downstream robot policies | Harness VLA; HarnessVLN; uni-robot-agent; Show-Harness; OpenRUA; RoboArchitect; Voyager; Eureka |
| Model Training | Training the foundation, reasoning, or code-generation model serving as the embodied agent, including SFT and RL for game or robot use | PEAR; CaPtain; ZAP; AgenticRoboRL; Guava; CrossHA; VAGEN; JARVIS-VLA; RoboCodeX |
| Benchmark | Direct code-agent evaluation and complementary tests of embodied planning, tool use, memory, exploration, and control | Embodied First Exam, EmbodiedSWE, CaP-X, CodeActionBench, RobotWorld, RoboMME |

These categories describe a paper's primary contribution. Task types, agent setups, and code artifacts are recorded as paper attributes or reading-note details.

## Assignment Rules

Give each paper one primary location:

1. Use **Survey** for a review, perspective, taxonomy, or roadmap. The two supplied agentic-robotics papers establish the intended system-level scope; code-specific reviews are additional references.
2. Use **Harness** when the main contribution is how models, tools, programs, feedback, and persistent state are organized into an embodied agent or experimental workflow.
3. Use **Model Training** when the foundation, reasoning, or code-generation model that serves as the agent is itself trained for embodied behavior. Record the trained parameters, objective, and deployment output interface. Training a separate downstream robot policy through generated rewards or configurations belongs under Harness when the contribution is the code-driven experimental workflow.
4. Use **Benchmark** when evaluation infrastructure or capability measurement is the main contribution, even if the paper also introduces a solver or training pipeline. Include useful broader agentic-robotics benchmarks, but identify whether they measure programs, actions, skill calls, or offline predictions in the [benchmark guide](BENCHMARK_GUIDE.md).

For hybrid papers, follow the contribution emphasized in the method and evaluation. Explain secondary contributions in a reading note rather than duplicating the row.

### Reference Frameworks

[Envisioning Agentic Robotics](../notes/2026-envisioning-agentic-robotics.md) distinguishes the model, the embodied harness, callable skills, and real-time control, and separates model-level evaluation from closed-loop system evaluation. [Towards Agentic Robots](../notes/2026-towards-agentic-robots.md) organizes the field by Model, Data, Environment, and Harness. These functional frameworks inform paper selection; they do not replace this repository's four catalogue categories or its Game and Robot scope.

### Boundary Examples

- **PEAR → Model Training:** robot-use RL updates the reasoning model itself. It is a native robot-use training reference whose deployment outputs are structured end-effector actions; executable program generation is not required for this entry. See the [reading note](../notes/2026-pear.md).
- **RoboCodeX → Model Training:** specialized multimodal pretraining and self-updating supervised fine-tuning update the behavior-code generation model itself.
- **RoboPro / RoboEvolve → Model Training:** the main learning target is the policy-code model or the planner/simulator, rather than only a library of generated programs.
- **AHA → Model Training:** instruction-tuning updates a failure-reasoning VLM used as a critic in embodied systems. Its output is a natural-language diagnosis, not a robot action.
- **CaPtain / AgenticRoboRL → Model Training:** SFT and multi-turn RL update the agent model that generates robot-control code or selects skills.
- **ZAP / Guava → Model Training:** simulation-based training or distillation updates a compact model's robot-use decisions through its action/tool interface.
- **CrossHA / VAGEN / JARVIS-VLA → Model Training:** training updates visual agents for game interaction, action selection, or world-state reasoning. See the [training-method guide](MODEL_TRAINING_GUIDE.md) for their specific interfaces.
- **Werewolf LSPO / GameTalk / MARSHAL / VAM → Model Training:** preference learning or RL updates the language model for strategic moves, communication, or multi-agent interaction. Language can be the native game action.
- **Player-1 / Odysseus / G1 → Model Training:** supervised initialization or RL updates a pretrained VLM for interactive game control; the [game-agent guide](GAME_AGENT_GUIDE.md) records each recipe.
- **Eureka / DrEureka → Harness:** LLM-generated rewards and simulation configurations organize the training of a separate robot policy. Their primary contribution is the code-driven learning workflow.
- **Voyager / Playful Agentic Robot Learning → Harness:** behavior improves through executable skills and memory; skill accumulation alone does not imply model-weight training.
- **RHO → Harness:** the method searches and improves policy repositories. Optimizing code is distinct from training model weights.
- **ENPIRE → Harness:** the primary contribution is the coding-agent and physical-experiment loop. Gradient-based policy learning is one supported component.
- **RoboClaw → Harness:** the VLM controller organizes data collection, downstream policy learning, self-resetting, and task execution; learning downstream primitives does not imply controller-model training.
- **RoboCoder / DROC / Statler → Harness:** feedback, reusable correction knowledge, or explicit world-state memory improve robot programs without establishing weight updates to the foundation model. See the [code-as-policy cross-check](CODE_AS_POLICY_GUIDE.md).
- **Harness VLA / HarnessVLN → Harness:** frozen models are organized through manipulation primitives or navigation tools, memory, and execution checks; their native outputs need not be executable code.
- **uni-robot-agent / Show-Harness → Harness:** a shared robot-use runtime or semantic action interpreter is the primary system contribution. Record coding-agent runtimes and direct action/tool configurations separately.
- **RoboArchitect / EMHO / KPHarness → Harness:** optimization revises external control logic, memory, or probing around a fixed model rather than necessarily updating its weights.
- **Code World Models / GameSense → Harness:** generated simulators or execution modules organize game decisions; code generation and downstream module training do not establish a foundation-model update.
- **Continual Harness → Harness:** online edits refine prompts, subagents, skills, and memory; its additional model co-training experiments are recorded separately.
- **NavGPT / MapGPT / InstructNav / Optimus-1 / JARVIS-1 / GITM → Harness:** custom planning, memory, and action/controller interfaces provide relevant navigation or game-agent architectures without implying general-purpose coding-agent use. See the [harness guide](HARNESS_GUIDE.md).
- **EmbodiedSWE → Benchmark:** its benchmark is the primary catalogue entry; trajectory generation and agent training are additional contributions.
- **Orak / TeamCraft / lmgame-Bench → Benchmark:** evaluation suites remain the primary entries despite supporting datasets, harnesses, and model-training experiments.
- **Gauntlet / AAArena → Benchmark:** evaluation measures coding agents developing executable game policies, with development budgets distinguished from frozen-policy gameplay.

## Four-Column Paper Format

| Column | Convention |
| :--- | :--- |
| Paper | Full title linked directly to the primary paper |
| Venue | Verified venue and month on separate lines, such as `ICML<br>2024-07`. Preprints use `Arxiv<br>YYYY-MM` with their first public preprint month |
| Task | Specific game names or robot tasks with each word capitalized, separated by semicolons |
| Links | Only available official `[💻 Code]` and `[🌐 Project Page]` links, one per line using `<br>`; use `—` if neither is available |

Use `&nbsp;` within link labels to prevent wrapping. Official survey companion collections may be linked as Project Page. Other resources and reading notes belong in supporting documents; the reading-note index has a separate Notes column.

Within each category, sort by the displayed month, newest first. Sort papers in the same month by full title in ascending alphabetical order, ignoring case. See the [column conventions](../CONTRIBUTING.md#column-conventions) for how to determine the month.

Task examples include `Minecraft`, `Red Dead Redemption II`, `Manipulation`, `Navigation`, `Locomotion`, and `Assembly`. A survey can use its covered task family or a description such as `Robot learning`. Record concrete tasks whenever the paper reports them.

## Reading-Note Details

The compact catalogue has four columns. Capture the following details in notes when useful:

- **Agent setup:** Custom, General-purpose, or Unspecified. A custom framework can include repair and memory; a general-purpose setup reuses an existing coding agent, such as Codex or Claude Code.
- **Native-use training references:** use Not applicable for the coding-agent setup when the model directly emits actions without generating executable programs; record that action interface instead.
- **Tool/action harness references:** identify the custom runtime or general-purpose coding agent and its native interface. Mark code-generation fields Not applicable when the agent selects tools or action units without emitting programs.
- **Model versus harness:** record the language model separately from the coding-agent framework. A model name alone does not identify the harness.
- **Environment:** exact game title, simulator, robot platform, and simulation versus real hardware.
- **Code artifact:** task program, skill, reward, environment generator, or repository.
- **Adaptation:** execution-time repair, across-episode code search, weight updates, or a mixture.
- **Training target:** identify which model receives weight updates, the training objective and data, and whether a separate downstream robot policy is learned.
- **Evaluation conditions:** observation privilege, action abstraction, human-provided skills, resets, trial counts, and interaction budgets.

Category assignments are editorial decisions supported by each paper's contribution and evidence, and can be revised as the collection grows.
