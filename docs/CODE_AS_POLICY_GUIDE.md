# Code-as-Policy Figure Cross-Check

The supplied figure corresponds to the code-as-policy taxonomy in [Weights or Skills? A Survey of Robot-Learning Techniques: from Action-Predicting Weights to Robots that Write their Own Skills](https://arxiv.org/abs/2608.01851), Section 3.1. It lists **27 works**. The catalogue already contained **8**; this cross-check adds the missing **19**: **16 Harness** papers and **3 Model Training** papers.

The figure's five groups below are retained only as a source cross-reference. The homepage uses Survey, Harness, Model Training, and Benchmark, in that order, with each paper listed once. All paper links below point to primary sources.

## Zero-shot synthesis

The source figure groups these by inference-time synthesis. That does not imply that the underlying model was never trained.

| Figure Label | Paper / Catalogue Category | Native Interface or Role | Check |
| :--- | :--- | :--- | :--- |
| **Code-as-Policies** | [Code as Policies: Language Model Programs for Embodied Control](https://arxiv.org/abs/2209.07753)<br>**Harness** | Custom; robot program generation | Already included |
| **ProgPrompt** | [ProgPrompt: Generating Situated Robot Task Plans using Large Language Models](https://arxiv.org/abs/2209.11302)<br>**Harness** | Custom; situated task programs | Already included |
| **VoxPoser** | [VoxPoser: Composable 3D Value Maps for Robotic Manipulation with Language Models](https://arxiv.org/abs/2307.05973)<br>**Harness** | Custom; generated 3D value-map code | Already included |
| **Instruct2Act** | [Instruct2Act: Mapping Multi-modality Instructions to Robotic Actions with Large Language Model](https://arxiv.org/abs/2305.11176)<br>**Harness** | Custom; Python perception-action programs | Already included |
| **ChatGPT for Robotics** | [ChatGPT for Robotics: Design Principles and Model Abilities](https://arxiv.org/abs/2306.17582)<br>**Harness** | Custom; generated code and function calls | Added |
| **TidyBot** | [TidyBot: Personalized Robot Assistance with Large Language Models](https://arxiv.org/abs/2305.05658)<br>**Harness** | Custom; preference rules and robot skills | Added |
| **RoboCodeX** | [RoboCodeX: Multimodal Code Generation for Robotic Behavior Synthesis](https://arxiv.org/abs/2402.16117)<br>**Model Training** | Trained multimodal code-generation model | Already included |
| **RoboScript** | [RoboScript: Code Generation for Free-Form Manipulation Tasks across Real and Simulation](https://arxiv.org/abs/2402.14623)<br>**Harness** | Custom; executable robot code | Added |
| **Text2Motion** | [Text2Motion: From Natural Language Instructions to Feasible Plans](https://arxiv.org/abs/2303.12153)<br>**Harness** | Custom; skill-sequence planning | Added |
| **Demo2Code** | [Demo2Code: From Summarizing Demonstrations to Synthesizing Code via Extended Chain-of-Thought](https://arxiv.org/abs/2305.16744)<br>**Harness** | Custom; demonstration-to-code synthesis | Added |
| **Statler** | [Statler: State-Maintaining Language Models for Embodied Reasoning](https://arxiv.org/abs/2306.17840)<br>**Harness** | Custom; generated code and explicit state memory | Added |
| **Prompt2Walk** | [Prompt a Robot to Walk with Large Language Models](https://arxiv.org/abs/2309.09969)<br>**Harness** | Custom; joint-target feedback control | Added |
| **RoboPro** | [Robotic Programmer: Video Instructed Policy Code Generation for Robotic Manipulation](https://arxiv.org/abs/2501.04268)<br>**Model Training** | Trained multimodal model; policy code | Added |

## Closed-loop self-repair

These systems use feedback, monitoring, or failure reasoning to revise behavior. Learned failure models are distinguished from orchestration logic.

| Figure Label | Paper / Catalogue Category | Native Interface or Role | Check |
| :--- | :--- | :--- | :--- |
| **Inner Monologue** | [Inner Monologue: Embodied Reasoning through Planning with Language Models](https://arxiv.org/abs/2207.05608)<br>**Harness** | Custom; feedback-conditioned skill planning | Added |
| **DoReMi** | [DoReMi: Grounding Language Model by Detecting and Recovering from Plan-Execution Misalignment](https://arxiv.org/abs/2307.00329)<br>**Harness** | Custom; plan monitoring and skill recovery | Added |
| **REFLECT** | [REFLECT: Summarizing Robot Experiences for Failure Explanation and Correction](https://arxiv.org/abs/2306.15724)<br>**Harness** | Custom; experience summaries and failure feedback | Added |
| **Code-as-Monitor** | [Code-as-Monitor: Constraint-aware Visual Programming for Reactive and Proactive Robotic Failure Detection](https://arxiv.org/abs/2412.04455)<br>**Harness** | Custom; executable monitoring code | Added |
| **AHA** | [AHA: A Vision-Language-Model for Detecting and Reasoning Over Failures in Robotic Manipulation](https://arxiv.org/abs/2410.00371)<br>**Model Training** | Trained VLM; natural-language failure explanations | Added |
| **Introspective Planning** | [Introspective Planning: Aligning Robots' Uncertainty with Inherent Task Ambiguity](https://arxiv.org/abs/2402.06529)<br>**Harness** | Custom; retrieval and plan selection | Added |

## Skill-library accumulation

The main persistent artifacts are executable skills or reusable correction knowledge.

| Figure Label | Paper / Catalogue Category | Native Interface or Role | Check |
| :--- | :--- | :--- | :--- |
| **RoboCoder** | [RoboCoder: Robotic Learning from Basic Skills to General Tasks with Large Language Models](https://arxiv.org/abs/2406.03757)<br>**Harness** | Custom; action-code refinement and skill accumulation | Added |
| **DROC** | [Distilling and Retrieving Generalizable Knowledge for Robot Manipulation via Language Corrections](https://arxiv.org/abs/2311.10678)<br>**Harness** | Custom; code repair and correction memory | Added |

## Evolutionary search

The source figure's grouping is retained for the cross-check. The catalogue separately distinguishes program search, evaluation infrastructure, and model learning.

| Figure Label | Paper / Catalogue Category | Native Interface or Role | Check |
| :--- | :--- | :--- | :--- |
| **CaP-X** | [CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation](https://arxiv.org/abs/2603.22435)<br>**Benchmark** | Code-agent gym and evaluation framework | Already included |
| **RoboEvolve** | [RoboEvolve: Co-Evolving Planner-Simulator for Robotic Manipulation with Limited Data](https://arxiv.org/abs/2605.13775)<br>**Model Training** | Trained planner and simulator; plans and simulated rollouts | Added |
| **GEAR** | [Code Evolution for Control: Synthesizing Policies via LLM-Driven Evolutionary Search](https://arxiv.org/abs/2601.06845)<br>**Harness** | Custom; evolutionary policy-code search | Added |

## Full self-improving loop

These systems connect exploration or experiments, persistent state, and robot-policy improvement in a larger agent loop.

| Figure Label | Paper / Catalogue Category | Native Interface or Role | Check |
| :--- | :--- | :--- | :--- |
| **ASPIRE** | [ASPIRE: Agentic /Skills Discovery for Robotics](https://arxiv.org/abs/2607.00272)<br>**Harness** | Coding-agent skill discovery and persistent library | Already included |
| **ENPIRE** | [ENPIRE: Agentic Robot Policy Self-Improvement in the Real World](https://arxiv.org/abs/2606.19980)<br>**Harness** | Coding-agent and physical-experiment loop | Already included |
| **RoboClaw** | [RoboClaw: An Agentic Framework for Scalable Long-Horizon Robotic Tasks](https://arxiv.org/abs/2603.11558)<br>**Harness** | Custom; VLM-driven policy orchestration | Added |

## Classification and Identity Checks

- **RoboScript:** the figure cites the [2024 code-generation paper](https://arxiv.org/abs/2402.14623). It is distinct from the later same-name [World In-Context Learning for Agentic Robot Manipulation](https://arxiv.org/abs/2611.12885).
- **RoboPro → Model Training:** the robotic foundation model learns policy-code generation from Video2Code supervision. Zero-shot task evaluation does not make the method training-free.
- **AHA → Model Training:** FailGen supplies failure trajectories for instruction-tuning a VLM that explains manipulation failures. This is a learned reasoning/critic component, not an action-generating controller. Its integration into repair loops is a downstream use.
- **RoboEvolve → Model Training:** the planner and simulator learn through a coupled exploration-and-consolidation process, including policy optimization. It should not be described as only evolutionary search over program text.
- **RoboCoder → Harness:** the selected contribution is feedback-driven refinement and accumulation of executable action skills. Its 80-task benchmark is a secondary contribution recorded here; the model name does not establish fine-tuning of the LLM.
- **RoboClaw → Harness:** one VLM controller organizes collection, self-resetting action pairs, downstream policy learning, and deployment. Training those downstream robot policies is distinct from training the controller model.
- **Prompt2Walk → Harness:** a frozen LLM predicts joint targets from observation/action history and few-shot examples. The native output is numeric control, not an executable robot program.
- **GEAR in the source figure:** the cited [paper](https://arxiv.org/abs/2601.06845) is titled *Code Evolution for Control: Synthesizing Policies via LLM-Driven Evolutionary Search*. The official [EvoControl repository](https://github.com/pgg3/EvoControl) uses a different name. The catalogue records the full paper title with the repository name as an alias. Its evaluated task is **LunarLander**, rather than locomotion or physical-robot manipulation.
- **CaP-X → Benchmark:** its code-agent gym and evaluation role remain the primary catalogue contribution; the paper is not duplicated under Harness.
- **Custom versus general-purpose coding agents:** these earlier methods generally use custom prompts, programs, planners, or controllers. Code generation alone is not evidence that Codex or Claude Code was used.

## Newly Added Harness Mechanisms

| Method | Main Persistent or Executed Artifact | Harness Contribution | Task |
| :--- | :--- | :--- | :--- |
| [RoboClaw](https://arxiv.org/abs/2603.11558) | Custom; VLM-driven policy orchestration | One VLM controller orchestrates data collection, downstream policy learning, self-resetting action pairs, and long-horizon execution of learned primitives. | Manipulation |
| [EvoControl (GEAR in figure)](https://arxiv.org/abs/2601.06845) | Custom; evolutionary policy-code search | LLM-driven evolutionary search refines executable Python control policies using fitness and behavioral feedback. The cited paper and official repository use EvoControl; GEAR is the source figure's label. | LunarLander |
| [Code-as-Monitor](https://arxiv.org/abs/2412.04455) | Custom; executable monitoring code | VLM-generated programs check spatial and temporal constraints for reactive and proactive failure monitoring. | Manipulation; Failure detection |
| [RoboCoder](https://arxiv.org/abs/2406.03757) | Custom; action-code refinement and skill accumulation | Environmental feedback repairs and accumulates executable motion primitives to expand the robot's action repertoire; the paper also introduces an 80-task benchmark across seven entities. | Locomotion; Manipulation |
| [RoboScript](https://arxiv.org/abs/2402.14623) | Custom; executable robot code | A deployable code-generation pipeline connects perception, motion planning, and robot execution across simulation and real hardware; it also provides a code-generation benchmark. | Manipulation; Object rearrangement |
| [Introspective Planning](https://arxiv.org/abs/2402.06529) | Custom; retrieval and plan selection | Retrieved introspective examples and uncertainty-aware planning align the robot's plan choices with task ambiguity and user intent. | Mobile manipulation; Instruction following |
| [DROC](https://arxiv.org/abs/2311.10678) | Custom; code repair and correction memory | Language corrections are distilled into reusable knowledge and retrieved by textual and visual similarity to improve later robot programs. | Manipulation; Instruction correction |
| [Prompt2Walk](https://arxiv.org/abs/2309.09969) | Custom; joint-target feedback control | Few-shot observation/action history prompts a frozen LLM to predict low-level joint targets, which a PD controller tracks. The outputs are numeric actions rather than robot programs. | Locomotion |
| [DoReMi](https://arxiv.org/abs/2307.00329) | Custom; plan monitoring and skill recovery | Constraints associated with a high-level plan are monitored during execution to detect misalignment and trigger recovery. | Manipulation; Locomotion |
| [Statler](https://arxiv.org/abs/2306.17840) | Custom; generated code and explicit state memory | World-model reader and writer prompts maintain explicit state while generated programs execute robot tasks. | Manipulation; Object rearrangement |
| [REFLECT](https://arxiv.org/abs/2306.15724) | Custom; experience summaries and failure feedback | Hierarchical summaries of multisensory execution histories support progressive failure explanation and correction. | Manipulation; Failure diagnosis; Task recovery |
| [Demo2Code](https://arxiv.org/abs/2305.16744) | Custom; demonstration-to-code synthesis | Recursive summarization converts demonstrations into task specifications, then recursive synthesis expands them into executable code. | Robotouille; Manipulation; Cooking tasks |
| [TidyBot](https://arxiv.org/abs/2305.05658) | Custom; preference rules and robot skills | An LLM summarizes user preferences into reusable rules and uses them to guide personalized household cleanup. | Mobile manipulation; Household cleanup; Object sorting |
| [Text2Motion](https://arxiv.org/abs/2303.12153) | Custom; skill-sequence planning | Language-model planning is grounded with skill feasibility estimates and task-and-motion checks before executing a sequence of skills. | Manipulation; Object rearrangement |
| [ChatGPT for Robotics](https://arxiv.org/abs/2306.17582) | Custom; generated code and function calls | Prompt design, a high-level function library, generated robot code, and human feedback connect a general LLM to several robot platforms. | Manipulation; Navigation; Aerial control |
| [Inner Monologue](https://arxiv.org/abs/2207.05608) | Custom; feedback-conditioned skill planning | Scene descriptions, success detection, and human feedback are inserted into language-model context to support replanning over robot skills. | Manipulation; Mobile manipulation; Household tasks |

## Venue and Link Verification

The catalogue uses the first release month from the linked Arxiv submission histories. Venue shows `Arxiv YYYY-MM` and retains any verified formal venue and edition year separately. Months sort newest first; full titles within the same month sort alphabetically, ignoring case.

- **ChatGPT for Robotics, IEEE Access 2024:** verified against the publisher-registered [Crossref record](https://api.crossref.org/works/10.1109/ACCESS.2024.3387941) and [DOI](https://doi.org/10.1109/ACCESS.2024.3387941). The earlier [Microsoft report](https://www.microsoft.com/en-us/research/publication/chatgpt-for-robotics-design-principles-and-model-abilities/) was released in 2023.
- **TidyBot, IROS 2023:** the [Arxiv author comments](https://arxiv.org/abs/2305.05658) record IROS 2023 and an Autonomous Robots publication. The catalogue uses the conference entry.
- **Text2Motion, Autonomous Robots 2023:** verified in the [author comments](https://arxiv.org/abs/2303.12153) and [project publication record](https://sites.google.com/stanford.edu/text2motion).
- **Demo2Code, NeurIPS 2023:** [official proceedings](https://proceedings.neurips.cc/paper_files/paper/2023/hash/30699996ff411d48903c9752b782a5c1-Abstract-Conference.html) and [author project](https://portal.cs.cornell.edu/demo2code/).
- **Statler, ICRA 2024:** [author comments](https://arxiv.org/abs/2306.17840) and [project citation](https://statler-lm.github.io/).
- **Prompt2Walk, CDC 2024:** [author comments](https://arxiv.org/abs/2309.09969).
- **Inner Monologue, CoRL 2022:** [official paper](https://proceedings.mlr.press/v205/huang23c.html) and [conference volume](https://proceedings.mlr.press/v205/). The proceedings were published in 2023; the catalogue uses the 2022 conference edition.
- **DoReMi, IROS 2024:** [author comments](https://arxiv.org/abs/2307.00329).
- **REFLECT, CoRL 2023:** [official proceedings](https://proceedings.mlr.press/v229/liu23g.html).
- **Code-as-Monitor, CVPR 2025:** [official proceedings](https://openaccess.thecvf.com/content/CVPR2025/html/Zhou_Code-as-Monitor_Constraint-aware_Visual_Programming_for_Reactive_and_Proactive_Robotic_Failure_CVPR_2025_paper.html).
- **AHA, ICLR 2025:** [author project](https://aha-vlm.github.io/).
- **Introspective Planning, NeurIPS 2024:** [author comments](https://arxiv.org/abs/2402.06529) and [official implementation](https://github.com/kevinliang888/IntroPlan).
- **DROC, ICRA 2024:** [author project publication record](https://sites.google.com/stanford.edu/droc).

RoboPro retains **Arxiv 2025-01**: the [author publication page](https://ustcwhy.github.io/publications/robopro/) lists it as Arxiv, while an ICLR submission alone does not establish acceptance. RoboScript, RoboCoder, RoboEvolve, and EvoControl retain their verified Arxiv first release months. Paper-only entries omit unavailable or unverified code links. PromptCraft is the research tool associated with ChatGPT for Robotics, rather than a claim that every reported experiment is released.

See the [Harness guide](HARNESS_GUIDE.md), [training-method guide](MODEL_TRAINING_GUIDE.md), and [main catalogue](../README.md).
