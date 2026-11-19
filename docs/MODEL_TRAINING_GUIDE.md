# Model Training: Search Basis and Method Notes

## Search Basis

The search starts from [PEAR](https://arxiv.org/abs/2611.18562), especially [Section 2, Related Work](https://arxiv.org/html/2611.18562v1#S2), which names CaPtain, AgenticRoboRL, and ZAP as concurrent training methods. Following ZAP's references leads to Guava. A complementary search for visual-agent post-training in games identifies CrossHA, VAGEN, and JARVIS-VLA.

Selection focuses on updates to the foundation, reasoning, or code-generation model serving as the embodied agent. Code generation, skill/tool calls, and direct structured actions are distinct interfaces. The homepage keeps the four bibliographic columns; method and verification details live here.

## Robot Agent Training

### PEAR

Robot-use RL updates the reasoning model itself in simulation. At deployment, it consumes observations and robot state and produces structured end-effector actions. Its [reading note](../notes/2026-pear.md) records the training target and interface.

[📄&nbsp;Paper](https://arxiv.org/abs/2611.18562) · [🌐&nbsp;Project](https://mit-han-lab.github.io/pear-blog/)

### CaPtain

SFT on synthetic interaction trajectories is followed by multi-turn RL. The trained VLM writes Python against low-level robot perception and motion primitives. A privileged-state critic supports credit assignment during training; the deployed agent does not receive that state.

[📄&nbsp;Paper](https://arxiv.org/abs/2610.40799) · [💻&nbsp;Code](https://github.com/waltstephen/CaPtain) · [🌐&nbsp;Project](https://waltstephen.github.io/captain/)

### ZAP

A pretrained VLM learns robot motion through successful simulation trajectories and GRPO. The deployed model selects end-effector and gripper actions through a minimal harness. This is a direct robot-use training analogue, with a different interface from code-as-policy agents. The current Arxiv title is used in the catalogue.

[📄&nbsp;Paper](https://arxiv.org/abs/2610.35817) · [🌐&nbsp;Project](https://zero-real.github.io/)

### AgenticRoboRL

SFT and multi-turn RL update the robot planner while execution components stay fixed. Harness adapters support both skill invocation and robot-control code generation. The paper belongs under Model Training because its learning target is the agent model.

[📄&nbsp;Paper](https://arxiv.org/abs/2610.28589) · [💻&nbsp;Code](https://github.com/xinxinliu-ai/AgenticRoboRL) · [🌐&nbsp;Project](https://xinxinliu-ai.github.io/AgenticRoboRL/)

### Guava

Simulation trajectories from a frontier teacher train a compact VLM to reason and select robot tools through a shared manipulation harness. The released study also reports further GRPO training on selected tasks. This entry covers model distillation and training as well as the supporting harness.

[📄&nbsp;Paper](https://arxiv.org/abs/2606.18363) · [💻&nbsp;Code](https://github.com/hdacnw/guava-release) · [🌐&nbsp;Project](https://guava-harness.github.io/)

## Additional Code-as-Policy and Reasoning References

The [code-as-policy figure cross-check](CODE_AS_POLICY_GUIDE.md) adds three training references and distinguishes them from runtime or program-search contributions.

### RoboEvolve

A VLM planner and a video simulator learn in a coupled exploration-and-consolidation loop. The method uses policy optimization, failure consolidation, and a progressive curriculum; the revised paper also studies low-level world-action-model learning. This is a model-learning reference rather than a fixed-model code-evolution harness.

[📄&nbsp;Paper](https://arxiv.org/abs/2605.13775)

### RoboPro

Video2Code creates policy-code supervision from videos for a robotic foundation model. At deployment the model generates executable manipulation programs. Zero-shot evaluation on new tasks follows model training and should not be confused with a training-free prompting method.

[📄&nbsp;Paper](https://arxiv.org/abs/2501.04268) · [🌐&nbsp;Author publication page](https://ustcwhy.github.io/publications/robopro/)

### AHA

FailGen procedurally perturbs manipulation demonstrations to produce failure trajectories and instruction-tuning examples. The learned VLM detects and explains failures and can supply feedback to planning, verification, and reward-design systems. It is a supporting failure-reasoning model, not an action-generating controller; this role is explicit in its Task and classification notes.

[📄&nbsp;Paper](https://arxiv.org/abs/2410.00371) · [💻&nbsp;Code](https://github.com/NVlabs/AHA) · [🌐&nbsp;Project](https://aha-vlm.github.io/)

## Game and Visual Agent Training

The [game-agent guide](GAME_AGENT_GUIDE.md) records 16 additional LLM/VLM training papers, their training targets and recipes, deployment interfaces, and formal venue sources. These include SFT, preference learning, multi-turn RL, self-play, and related continued game-domain pretraining.

### CrossHA

Mixed-interface SFT, single-turn RL, and multi-turn RL train a Minecraft agent to choose its interaction granularity. Deployment can use motion, grounding, raw, language, or latent action interfaces. The authors' code link points to the shared OpenHA repository; it is not a separately named CrossHA repository.

[📄&nbsp;Paper](https://arxiv.org/abs/2512.09706) · [💻&nbsp;Code](https://github.com/CraftJarvis/OpenHA) · [🌐&nbsp;Project](https://craftjarvis.github.io/CrossHA/)

### VAGEN

Multi-turn RL trains a VLM's visual state estimation and transition reasoning, with world-model rewards and turn-aware credit assignment. Embodied evaluations include Sokoban, FrozenLake, navigation, and robot manipulation. The paper also evaluates SVG generation; the homepage Task cell lists its game/robot tasks.

[📄&nbsp;Paper](https://arxiv.org/abs/2510.16907) · [💻&nbsp;Code](https://github.com/mll-lab-nu/VAGEN) · [🌐&nbsp;Project](https://vagen-ai.github.io/)

### JARVIS-VLA

Environment-specific visual-language post-training improves a foundation VLM before imitation learning for Minecraft keyboard/mouse actions. It is a game-agent training analogue to PEAR, with a different supervision recipe and action representation.

[📄&nbsp;Paper](https://arxiv.org/abs/2503.16365) · [💻&nbsp;Code](https://github.com/CraftJarvis/JarvisVLA) · [🌐&nbsp;Project](https://craftjarvis.github.io/JarvisVLA/)

## Venue and Link Verification

- **ZAP:** the [author project page](https://zero-real.github.io/) reports CoRL 2026 Late Breaking Results. The table retains the LBR qualifier.
- **Guava:** the [accepted-paper list](https://agentic-robotics-workshop.github.io/papers) lists it at the CoRL 2026 Workshop on Agentic Robotics. The table retains the Workshop qualifier.
- **CrossHA:** the [author project page](https://craftjarvis.github.io/CrossHA/) reports CVPR 2026; the paper is also available in the [CVF proceedings](https://openaccess.thecvf.com/content/CVPR2026/papers/He_Training_One_Model_to_Master_Cross-Level_Agentic_Actions_via_Reinforcement_CVPR_2026_paper.pdf).
- **VAGEN:** verified against the [NeurIPS 2025 proceedings](https://papers.nips.cc/paper_files/paper/2025/hash/fc6688d75adde86b9df910769c1d02e3-Abstract-Conference.html).
- **JARVIS-VLA:** verified as Findings of ACL 2025 in the [ACL Anthology](https://aclanthology.org/2025.findings-acl.920/).
- **PEAR, CaPtain, and AgenticRoboRL:** first released as preprints in 2026-11, 2026-10, and 2026-10, respectively. The catalogue sorts by the displayed venue month, then by full title within the same month.
- Missing links are omitted. In particular, the ZAP project did not provide an official code release link when checked.

CaP-X remains under Benchmark because benchmarking is its primary catalogue role; its CaP-RL training contribution can inform this reading list without duplicating the paper row.
