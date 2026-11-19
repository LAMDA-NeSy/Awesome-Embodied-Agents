# Harness Guide

This guide records the selection basis and interfaces for the expanded Harness catalogue. It covers **Game and Robot** systems: code execution, tool/skill orchestration, semantic action interfaces, memory, verification, and harness optimization. These are reading dimensions within Harness, not additional catalogue categories.

## Search Basis

The 2026 search expansion started with [Harness VLA](https://arxiv.org/abs/2607.08448), [HarnessVLN](https://arxiv.org/abs/2609.15195), [uni-robot-agent](https://arxiv.org/abs/2611.01560), and [Show-Harness](https://arxiv.org/abs/2609.10522), then followed related-work references, author project pages, and official implementations. The search also used the system-level model/harness distinction in [Envisioning Agentic Robotics](../notes/2026-envisioning-agentic-robotics.md) and [Towards Agentic Robots](../notes/2026-towards-agentic-robots.md).

Search directions included:

- VLA harnesses: frozen policies as callable primitives, perception augmentation, action interpreters, and hybrid code/policy control.
- Navigation harnesses: VLN, instruction following, object-goal navigation, spatial memory, recovery, and termination.
- Robot-use coding agents: native terminal/ROS access, Python execution, shared robot gateways, and persistent code skills.
- Harness adaptation: program repair, online exploration, experience traces, memory revision, and external harness optimization.
- Game agents: Minecraft planning, reusable skills, multimodal memory, keyboard/mouse control, and harnesses around game VLAs.
- Earlier foundations: executable robot programs, geometric constraints, map-guided planning, and hierarchical game controllers.

The catalogue admits methods with a substantive embodied agent architecture even when the native output is a tool call, a skill choice, or an action unit. A code repository alone does not make a method a code agent. General-purpose coding agents reuse a runtime such as Codex or Claude Code; custom frameworks may instead organize a model through their own planner, tools, and execution loop.

## Newly Added Papers

Each linked paper is the primary source for its method and task description. The catalogue sorts by the displayed venue month, newest first, then by title within each month. Setup labels describe the evaluated interface; they do not imply that every configuration in a paper uses the same runtime.

| Paper / Method | Setup and Native Interface | Harness Contribution | Task |
| :--- | :--- | :--- | :--- |
| [Reins](https://arxiv.org/abs/2611.16632) | Custom; action tools and feedback | A real-time narrator and grounded atomic action interface support long-horizon control and intervention in dynamic real-robot scenes. | Manipulation; Bimanual manipulation |
| [uni-robot-agent](https://arxiv.org/abs/2611.01560) | General-purpose runtimes and custom tool-use configurations | Shared observation and action tools connect open models and coding-agent runtimes to simulation and real robots, with independently configurable perception and execution. | Manipulation; Bimanual manipulation |
| [Auriga Technical Report](https://arxiv.org/abs/2611.01112) | General-purpose coding agent; code execution | A model-led Codex session uses a robot execution gateway, calibrated perception, trajectory preview, and staged execution feedback. | Manipulation; Bimanual manipulation |
| [RoboArchitect](https://arxiv.org/abs/2610.42141) | Coding-agent harness optimization | A coding model revises control routines and persistent memory around a frozen robot policy using rollout evidence, without updating model weights. | Manipulation |
| [HiSTEVE 1.0](https://arxiv.org/abs/2610.31162) | Custom; planner and native-interface VLA | A high-level harness supplies planning and memory while a low-level VLA operates keyboard and mouse. VLA training is a secondary contribution to the full system. | Minecraft |
| [KPHarness](https://arxiv.org/abs/2610.27417) | External harness optimization around a frozen VLA | Recovery knowledge and diagnostic probing co-evolve to revise an execution harness for long-horizon gaming without updating the actor. | Minecraft |
| [HexaShell](https://arxiv.org/abs/2610.23479) | General-purpose coding agent; code execution | A shared Python-cell execution interface and robot tools connect coding agents to simulation and hardware. | Manipulation; Bimanual manipulation |
| [RAX](https://arxiv.org/abs/2610.22496) | General-purpose coding agent; code execution | Online exploration accumulates and repairs reusable robot programs rather than requiring a new model-weight update for each task. | Manipulation; Mobile manipulation; Dexterous manipulation |
| [COAP](https://arxiv.org/abs/2610.12369) | Coding-agent program search; stateful code | A coding agent recursively improves a persistent stateful policy library. The deployed controller uses code without a VLM in the control loop. | Bimanual manipulation |
| [SuperNav](https://arxiv.org/abs/2610.12126) | Custom; navigation tools and skills | A frozen multimodal model orchestrates reusable navigation tools and skills for object, instance, multi-object, and demand-driven tasks. | Navigation; Object-goal navigation; Multi-object navigation |
| [EMHO](https://arxiv.org/abs/2610.08432) | External harness optimization | Experience traces guide revisions to planning, memory, and tool orchestration while the embodied model remains fixed. | Navigation; Manipulation |
| [OpenRUA](https://arxiv.org/abs/2610.02459) | General-purpose coding agents; terminal and ROS 2 | Claude Code or Codex operates native ROS 2 workspaces through a terminal. This project is separate from the openrua.ai uni-robot-agent project. | Manipulation; Mobile manipulation |
| [PyRUA-Lean](https://arxiv.org/abs/2610.01939) | Custom; interactive Python execution | Python cells compose robot primitives and VLA calls, with local retries and compact feedback. A separate training experiment does not replace its main runtime contribution. | Manipulation; Bimanual manipulation |
| [RoboHarness](https://arxiv.org/abs/2610.14018) | General-purpose coding-agent integrations; perception and action tools | A visual-geometric control panel supplies keypoints, tracking, depth, and geometric constraints for manipulation in BEHAVIOR. | Household tasks; Manipulation |
| [RACaP](https://arxiv.org/abs/2609.29394) | Custom; code evolution followed by tool calls | A coding agent evolves typed policy APIs before deployment; a runtime agent reasons and acts through the resulting fixed APIs. Distillation is secondary. | Manipulation |
| [Robo-Harness K1](https://arxiv.org/abs/2609.29389) | Custom; perception and action tools | Calibrated geometry, tracked anchors, and generic motion tools support observe-measure-act-verify loops. The paper also studies distillation from tool-call traces. | Manipulation; Bimanual manipulation |
| [RegenHarness](https://arxiv.org/abs/2609.27612) | Custom; runtime and verification | A quadruped-agent runtime uses evidence checks, persistent memory, and versioned configuration changes for navigation, inspection, and delivery. | Navigation; Inspection; Message delivery |
| [RoboDawn](https://arxiv.org/abs/2609.22966) | Custom; discrete motion interface | A VLM issues semantically meaningful motion and gripper commands, supported by in-context demonstrations rather than assuming generated executable code. | Manipulation; Bimanual manipulation |
| [SafeHarness](https://arxiv.org/abs/2609.20822) | General-purpose coding agent; guarded code execution | Robot-control code uses obstacle-aware planning and execution checks. This is the robotics paper, distinct from the unrelated agent-security work also named SafeHarness. | Manipulation; Obstacle avoidance |
| [HarnessVLN](https://arxiv.org/abs/2609.15195) | Custom; tool/skill orchestration | A shared navigation runtime combines validated tool execution, hierarchical event memory, spatial evidence, recovery, and termination checks. | Navigation; Instruction following; Object-goal navigation |
| [Show-Harness](https://arxiv.org/abs/2609.10522) | Custom; semantic action units | An embodiment-specific interpreter grounds discrete semantic action units into motion. The paper evaluates both a zero-shot frontier VLM and fine-tuned small VLMs. | Manipulation; Bimanual manipulation |
| [Harness VLA](https://arxiv.org/abs/2607.08448) | Custom; tool/skill orchestration | A memory-guided planner composes a frozen VLA primitive with analytic primitives, verifies outcomes, and retries after re-grounding. | Manipulation; Household tasks; Bimanual manipulation |
| [ASPIRE](https://arxiv.org/abs/2607.00272) | Coding-agent skill discovery | Agents discover, debug, and retain reusable code-based skills across robot tasks; the persistent skill library is distinct from model weights. | Manipulation; Bimanual handover; Household tasks |
| [ReKep](https://arxiv.org/abs/2409.01652) | Custom; generated constraint code | A VLM generates Python functions expressing relational keypoint constraints, which solvers turn into robot motion. | Manipulation; Mobile manipulation; Bimanual manipulation |
| [Optimus-1](https://arxiv.org/abs/2408.03615) | Custom; plans and action controller | A knowledge-guided planner, experience-driven reflector, and hybrid multimodal memory coordinate a game controller; the planner does not need to emit executable programs. | Minecraft |
| [InstructNav](https://arxiv.org/abs/2406.04882) | Custom; navigation planning and value maps | Dynamic Chain-of-Navigation planning and multi-sourced value maps convert diverse instructions into actionable navigation trajectories without navigation training. | Navigation; Instruction following; Object-goal navigation |
| [MapGPT](https://arxiv.org/abs/2401.07314) | Custom; map-guided action selection | An online linguistic map and adaptive path planning organize a frozen model's navigation decisions. | Navigation; Instruction following; Object grounding |
| [JARVIS-1](https://arxiv.org/abs/2311.05997) | Custom; memory-augmented planning and controller | A multimodal planner retrieves experience and composes subgoals for a low-level controller; memory growth is distinct from training the planner. | Minecraft |
| [RoboTool](https://arxiv.org/abs/2310.13065) | Custom; code generation | Analyzer, planner, calculator, and coder modules compose parameterized robot skills for creative physical tool use. | Manipulation; Physical tool use; Locomotion |
| [NavGPT](https://arxiv.org/abs/2305.16986) | Custom; reasoning and action selection | A history buffer, observation descriptions, and explicit reasoning guide sequential viewpoint selection for instruction-following navigation. | Navigation; Instruction following |
| [GITM](https://arxiv.org/abs/2305.17144) | Custom; hierarchical planning and structured actions | Decomposition, text-based knowledge, and action memory organize open-world game interaction; do not assume it uses a general-purpose coding-agent runtime. | Minecraft |
| [Instruct2Act](https://arxiv.org/abs/2305.11176) | Custom; Python program generation | An LLM generates executable Python that connects visual foundation-model perception to robot actions under multimodal instructions. | Manipulation |

## Classification Boundaries

The [game-agent guide](GAME_AGENT_GUIDE.md) adds visual control, strategic games, interactive fiction, real-time scheduling, executable world models, and online harness refinement. It also identifies the separate development and runtime roles in game-policy coding benchmarks.

The [code-as-policy figure cross-check](CODE_AS_POLICY_GUIDE.md) accounts for all 27 works in the supplied taxonomy, including 16 additional Harness papers. It records their native interfaces and explains why RoboPro, AHA, and RoboEvolve are placed in Model Training.

- **Harness VLA:** the VLA is frozen and used as a callable manipulation primitive. The contribution is orchestration, memory, verification, and retries.
- **HarnessVLN / SuperNav / NavGPT / MapGPT / InstructNav:** the agent plans and selects navigation operations through a custom runtime. These are navigation-harness references; their output should not be mislabeled as generated executable code.
- **uni-robot-agent / OpenRUA:** these are different projects. The former is the unified harness presented at [openrua.ai](https://openrua.ai/uni-robot-agent); the latter is the terminal/ROS 2 coding-agent framework in [terminalworld/OpenRUA](https://github.com/terminalworld/OpenRUA).
- **Show-Harness / Robo-Harness K1 / PyRUA-Lean / HiSTEVE 1.0:** these papers also report model-training components. Their catalogue location follows the main system/interface contribution; training details remain secondary rather than creating duplicate rows.
- **RoboArchitect / EMHO / KPHarness / ASPIRE / RAX / COAP:** code, skills, memory, or the external harness can improve while the relevant foundation model or actor remains fixed. This differs from agent-model post-training.
- **PEAR / CaPtain / AgenticRoboRL / Guava:** these remain in Model Training because training the embodied agent model is the central contribution. See the [training-method guide](MODEL_TRAINING_GUIDE.md).
- **Optimus-1 / JARVIS-1 / GITM:** memory, hierarchical planning, and controllers make these relevant game-harness references. Their inclusion does not imply the use of an off-the-shelf coding agent.

These assignments are curation decisions based on the primary contribution, not a claim that the four categories are mutually exclusive research topics.

## Metadata and Link Checks

Check preprint dates against the first public version. Some Arxiv identifiers have a different month from their first submissions. For formal publications, follow the [venue and month conventions](../CONTRIBUTING.md#column-conventions).

Formal venues were checked using primary sources:

- **ReKep, CoRL 2024:** [official proceedings](https://proceedings.mlr.press/v270/huang25g.html) in the [CoRL 2024 volume](https://proceedings.mlr.press/v270/). The proceedings volume was published in 2025; the catalogue uses the conference edition year.
- **InstructNav, CoRL 2024:** [official proceedings](https://proceedings.mlr.press/v270/long25b.html) and [author implementation announcement](https://github.com/LYX0501/InstructNav).
- **Optimus-1, NeurIPS 2024:** [official conference paper](https://proceedings.neurips.cc/paper_files/paper/2024/file/5949a8750a110ce1f0631b1776c500a2-Paper-Conference.pdf) and [author project](https://cybertronagent.github.io/Optimus-1.github.io/).
- **MapGPT, ACL 2024:** [author project and publication record](https://chen-judge.github.io/MapGPT/).
- **NavGPT, AAAI 2024:** [official publication](https://ojs.aaai.org/index.php/AAAI/article/view/28597).
- **JARVIS-1, TPAMI 2025:** [publisher record](https://ieeexplore.ieee.org/document/10778628), volume 47, issue 3.
- **PyRUA-Lean, CoRL Workshop 2026:** [Agentic Robotics workshop accepted-paper list](https://agentic-robotics-workshop.github.io/papers). This is a workshop venue, not a CoRL main-conference acceptance.

Preprints without a verified formal publication use `Arxiv<br>YYYY-MM` in the catalogue.

Code and project links in the catalogue come from author paper pages, official project pages, or matching author repositories. Missing links are omitted. [RPent](https://github.com/RLinf/RPent) is the current infrastructure release linked by the [Harness VLA documentation](https://rpent.readthedocs.io/en/latest/rst_source/resources/harnessvla.html); preserve the documented reproduction branches when reproducing historical results. Link verification does not establish that an experiment has been reproduced.

Return to the [Harness catalogue](../README.md#harness).
