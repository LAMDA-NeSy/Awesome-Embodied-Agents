<h1 align="center">Awesome Embodied Agents</h1>

<p align="center">
  <a href="assets/banner-realistic.png">
    <img src="assets/banner-realistic.png" alt="Embodied agent architecture: a foundation model and harness connect to Game and Robotics environments, with realistic hardware, Minecraft gameplay, and laboratory robot imagery." width="640">
  </a>
</p>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue" alt="License: MIT"></a>
  <a href="#survey"><img src="https://img.shields.io/badge/papers-158-3b82f6" alt="Papers: 158"></a>
  <a href="https://github.com/LAMDA-NeSy/Awesome-Embodied-Agents/graphs/contributors"><img src="https://img.shields.io/github/contributors/LAMDA-NeSy/Awesome-Embodied-Agents" alt="GitHub contributors"></a>
  <a href="https://github.com/LAMDA-NeSy/Awesome-Embodied-Agents/commits/main"><img src="https://img.shields.io/github/last-commit/LAMDA-NeSy/Awesome-Embodied-Agents" alt="GitHub last commit"></a>
  <a href="https://github.com/LAMDA-NeSy/Awesome-Embodied-Agents/stargazers"><img src="https://img.shields.io/github/stars/LAMDA-NeSy/Awesome-Embodied-Agents?style=social&amp;label=Stars" alt="GitHub stars"></a>
  <a href="https://github.com/LAMDA-NeSy/Awesome-Embodied-Agents/forks"><img src="https://img.shields.io/github/forks/LAMDA-NeSy/Awesome-Embodied-Agents?style=social&amp;label=Forks" alt="GitHub forks"></a>
</p>

This list collects research on **code agents and agent harnesses for embodied intelligence in games and robotics**, including custom code-generation frameworks and general-purpose coding agents. It covers **surveys, harness design, model training and post-training, and benchmarks**, from code execution and tool use to planning, memory, feedback, and self-improvement. The collection also includes native LLM/VLM game and robot agents, with tasks spanning video games, interactive fiction, strategic board/card games, manipulation, navigation, and control. Within each category, papers are sorted by the month shown in Venue, newest first, then alphabetically by title.

## Table of Contents

- [Survey](#survey)
- [Harness](#harness)
- [Model Training](#model-training)
- [Benchmark](#benchmark)
- [Contributing](#contributing)
- [License](#license)

<a id="survey"></a>
## Survey

System-level surveys, perspectives, and roadmaps on agents in games and robotics. These references connect foundation models, training, data, environments, harnesses, and evaluation, alongside focused reviews of code-based skills.

| Paper | Venue | Task | Links |
| :--- | :---: | :--- | :--- |
| **[Envisioning Agentic Robotics: A New Era of Robotic Systems](https://arxiv.org/abs/2611.18359)** | Arxiv<br>2026-11 | Agentic Robotics; Manipulation; Navigation | — |
| **[A Survey of Agentic Robotics: Toward Continual Self-Improvement](https://www.alphaxiv.org/abs/2610.rsi-agentic-robotics)** | Arxiv<br>2026-10 | Robot Task Orchestration; Motion Generation; Continual Self-Improvement | [🌐&nbsp;Project&nbsp;Page](https://github.com/jiaming-ai/awesome-agentic-robotics) |
| **[Multimodal Embodied Agents: A Unified Capability-centric Perspective from Computer-Use to Robot-Use](https://arxiv.org/abs/2610.30108)** | Arxiv<br>2026-10 | Computer Use; Robot Use; Embodied Capability Evaluation | [🌐&nbsp;Project&nbsp;Page](https://showlab.github.io/Awesome-Multimodal-Embodied-Agent/) |
| **[Towards Agentic Robots: Model, Data, Environment, and Harness](https://arxiv.org/abs/2610.20442)** | Arxiv<br>2026-10 | Agentic Robotics; Manipulation; Navigation | [🌐&nbsp;Project&nbsp;Page](https://github.com/chonghanqin/Awesome-Agentic-Robots) |
| **[Who Improves the Robot? Toward Physical Recursive Self-Improvement](https://arxiv.org/abs/2610.18842)** | Arxiv<br>2026-10 | Robot Skill Adaptation; Physical Recursive Self-Improvement; Verification | [🌐&nbsp;Project&nbsp;Page](https://github.com/SAIL-Research-Lab/Physical-RSI) |
| **[Embodied Agentic Harnesses for Physical Intelligence: A Survey](https://doi.org/10.31224/8297)** | Arxiv<br>2026-09 | Embodied Execution; Runtime Monitoring; Recovery | [🌐&nbsp;Project&nbsp;Page](https://github.com/yuhuang-ca/Survey-of-Embodied-Agentic-Harness) |
| **[From Language Models to World-Acting Systems: Progress and Limits of Agentic AI across Digital, Social, Virtual, and Physical Environments](https://arxiv.org/abs/2609.04894)** | Arxiv<br>2026-09 | Virtual Environments; Robot Control; Delegation And Recovery | — |
| **[Weights or Skills? A Survey of Robot-Learning Techniques: from Action-Predicting Weights to Robots that Write their Own Skills](https://arxiv.org/abs/2608.01851)** | Arxiv<br>2026-08 | Robot Learning; Code-Based Skill Acquisition | — |
| **[From World Action Models to Embodied Brains: A Roadmap for Open-World Physical Intelligence](https://arxiv.org/abs/2607.11689)** | Arxiv<br>2026-07 | Open-World Robot Control; Action Consequence Prediction; Closed-Loop Learning | — |
| **[Harness Engineering for Physical AI: Robot Middleware Is the Harness Layer](https://arxiv.org/abs/2606.09416)** | Arxiv<br>2026-06 | Robot Control; Real-Time Scheduling; Middleware | — |
| **[Towards Generalist Game Agents: A Survey of Foundation Models in Virtual Worlds](https://arxiv.org/abs/2605.09965)** | Arxiv<br>2026-05 | Game Agents; Virtual Worlds; Cross-Game Generalization | [🌐&nbsp;Project&nbsp;Page](https://thusi-lab.github.io/Awesome-LFMs-Play-Games/) |

<a id="harness"></a>
## Harness

Frameworks that connect models or coding agents to games and robots through code execution, tool or skill calls, action interfaces, feedback, memory, and experiment orchestration. This includes harnesses around frozen VLAs, navigation agents, and code-driven training of downstream robot policies. See the [harness guide](docs/HARNESS_GUIDE.md) for interface distinctions and the search basis.

| Paper | Venue | Task | Links |
| :--- | :---: | :--- | :--- |
| **[Democratizing Robot-Use Agents: A Unified Harness with Open Models](https://arxiv.org/abs/2611.01560)** | Arxiv<br>2026-11 | Manipulation; Bimanual Manipulation | [🌐&nbsp;Project&nbsp;Page](https://openrua.ai/uni-robot-agent) |
| **[ENPIRE: Agentic Robot Policy Self-Improvement in the Real World](https://arxiv.org/abs/2606.19980)** | CoRL<br>2026-11 | Manipulation; Assembly | [💻&nbsp;Code](https://github.com/NVlabs/ENPIRE)<br>[🌐&nbsp;Project&nbsp;Page](https://research.nvidia.com/labs/gear/enpire/) |
| **[Fewer Tokens, Better Action: GPT-6 Astra Robot Agents with 14% Higher Success Rate but 65% Fewer Tokens](https://arxiv.org/abs/2610.01939)** | CoRL Workshop<br>2026-11 | Manipulation; Bimanual Manipulation | [💻&nbsp;Code](https://github.com/DAGroup-PKU/PyRUA-Lean)<br>[🌐&nbsp;Project&nbsp;Page](https://dagroup-pku.github.io/PyRUA-Lean/docs/) |
| **[Playful Agentic Robot Learning](https://arxiv.org/abs/2606.19419)** | CoRL<br>2026-11 | Manipulation; Skill Acquisition | [💻&nbsp;Code](https://github.com/Playful-RATs/rats)<br>[🌐&nbsp;Project&nbsp;Page](https://playful-rats.github.io/) |
| **[Reins: Frontier Multimodal Models Driving Real Robot Arms on Long-Horizon Tasks, Zero-Shot](https://arxiv.org/abs/2611.16632)** | Arxiv<br>2026-11 | Manipulation; Bimanual Manipulation | — |
| **[A team of Gemini 4 Argon agents beats Minecraft](https://arxiv.org/abs/2610.22319)** | Arxiv<br>2026-10 | Minecraft | — |
| **[Auriga Technical Report: A Task-Agnostic Agent Harness for Zero-Shot Embodied Manipulation](https://arxiv.org/abs/2611.01112)** | Arxiv<br>2026-10 | Manipulation; Bimanual Manipulation | [💻&nbsp;Code](https://github.com/lose4578/Auriga)<br>[🌐&nbsp;Project&nbsp;Page](https://auriga.stelledge.com/) |
| **[CarryOn: A Dual-Loop Harness for Personalized and Reliable Robot Assistance](https://arxiv.org/abs/2610.21453)** | Arxiv<br>2026-10 | Personalized Robot Assistance; Manipulation; Failure Recovery | [💻&nbsp;Code](https://github.com/JIA-Lab-research/CarryOn)<br>[🌐&nbsp;Project&nbsp;Page](https://vincent2311.github.io/Projects/CarryOn/) |
| **[Embodied Turing Machines: Stateful Code for Robot Recursive Self-Improvement](https://arxiv.org/abs/2610.12369)** | Arxiv<br>2026-10 | Bimanual Manipulation | — |
| **[EMHO: EMbodied Agent Harness Optimization via Experience Traces](https://arxiv.org/abs/2610.08432)** | Arxiv<br>2026-10 | Navigation; Manipulation | — |
| **[HexaShell: A Universal Harness for Robot Coding Agents in Simulation and the Real World](https://arxiv.org/abs/2610.23479)** | Arxiv<br>2026-10 | Manipulation; Bimanual Manipulation | [💻&nbsp;Code](https://github.com/HexaFuture/HexaShell) |
| **[HiSTEVE 1.0: Harnessing Human-Interface VLA Agents for Open-World Games](https://arxiv.org/abs/2610.31162)** | Arxiv<br>2026-10 | Minecraft | [💻&nbsp;Code](https://github.com/Andytonglove/HiSTEVE-1.0) |
| **[KPHarness: Co-Evolving Knowledge and Probing for Long-Horizon Gaming Harnesses](https://arxiv.org/abs/2610.27417)** | Arxiv<br>2026-10 | Minecraft | [🌐&nbsp;Project&nbsp;Page](https://chenzk202212.github.io/adaptive-gaming-harnesses/) |
| **[OpenRUA: Robot-Use Agents Are Zero-Shot Visuomotor Policies](https://arxiv.org/abs/2610.02459)** | Arxiv<br>2026-10 | Manipulation; Mobile Manipulation | [💻&nbsp;Code](https://github.com/terminalworld/OpenRUA) |
| **[RoboArchitect: Automating the Design of Robotic Agents with Persistent Memory](https://arxiv.org/abs/2610.42141)** | Arxiv<br>2026-10 | Manipulation | [💻&nbsp;Code](https://github.com/roboarchitect-ai/RoboArchitect)<br>[🌐&nbsp;Project&nbsp;Page](https://roboarchitect-ai.github.io/) |
| **[Scaling Online Exploration for Robot Agents](https://arxiv.org/abs/2610.22496)** | Arxiv<br>2026-10 | Manipulation; Mobile Manipulation; Dexterous Manipulation | [💻&nbsp;Code](https://github.com/robot-agent-exploration/rax) |
| **[SuperNav: An Agentic Navigation System for Any Task in Any Scene](https://arxiv.org/abs/2610.12126)** | Arxiv<br>2026-10 | Navigation; Object-Goal Navigation; Multi-Object Navigation | [💻&nbsp;Code](https://github.com/zju3dv/SuperNav)<br>[🌐&nbsp;Project&nbsp;Page](https://zju3dv.github.io/SuperNav/) |
| **[Towards a Systematic Study of Embodied System 2 over Full Task Execution Cycles](https://arxiv.org/abs/2610.17657)** | Arxiv<br>2026-10 | Household Tasks; Navigation; Manipulation | — |
| **[Agent as Policy for Robotic Manipulation](https://arxiv.org/abs/2609.12541)** | Arxiv<br>2026-09 | Manipulation; Assembly; Throwing; Cloth Folding | [💻&nbsp;Code](https://github.com/agent-as-policy-2026/agent-as-policy)<br>[🌐&nbsp;Project&nbsp;Page](https://agent-as-policy-2026.github.io/) |
| **[Coding Agents with Harness for Safe Robot Control](https://arxiv.org/abs/2609.20822)** | Arxiv<br>2026-09 | Manipulation; Obstacle Avoidance | — |
| **[DynaHarness: A Dynamic Physical Harness for Self-Evolving Robot Agents](https://arxiv.org/abs/2609.40306)** | Arxiv<br>2026-09 | Manipulation; Failure Recovery | [🌐&nbsp;Project&nbsp;Page](https://denghaoyuan123.github.io/Dynaharness_page/) |
| **[HarnessPAI: An Evolving Harness for Physical AI](https://arxiv.org/abs/2609.29166)** | Arxiv<br>2026-09 | Manipulation; Household Cleaning; Locomotion | [💻&nbsp;Code](https://github.com/Darwin-Agent/HarnessPAI)<br>[🌐&nbsp;Project&nbsp;Page](https://darwin-agent.github.io/HarnessPAI/) |
| **[HarnessVLN: Unifying Training-Free Embodied Navigation through an Agent Harness](https://arxiv.org/abs/2609.15195)** | Arxiv<br>2026-09 | Navigation; Instruction Following; Object-Goal Navigation | [💻&nbsp;Code](https://github.com/AgibotGeneral/harnessvln)<br>[🌐&nbsp;Project&nbsp;Page](https://agibot-harnessvln.netlify.app/) |
| **[NavHarness: Towards Lifelong Embodied Navigation](https://arxiv.org/abs/2609.34276)** | Arxiv<br>2026-09 | Lifelong Navigation; Object-Goal Navigation; Instruction Following | [💻&nbsp;Code](https://github.com/billzhao1030/NavHarness)<br>[🌐&nbsp;Project&nbsp;Page](https://billzhao1030.github.io/NavHarness/) |
| **[RACaP: Agentic Reasoning, Acting, and Coding as Policies for Evolvable Robot Learning](https://arxiv.org/abs/2609.29394)** | Arxiv<br>2026-09 | Manipulation | [💻&nbsp;Code](https://github.com/Robo-Harness/racap) |
| **[RegenHarness: A Robot Agent Harness with Evidence-Gated Recursive Self-Improvement](https://arxiv.org/abs/2609.27612)** | Arxiv<br>2026-09 | Navigation; Inspection; Message Delivery | — |
| **[Robo-Harness K1: Harnessing Robot-Use Agents via Perception Augmentation](https://arxiv.org/abs/2609.29389)** | Arxiv<br>2026-09 | Manipulation; Bimanual Manipulation | [💻&nbsp;Code](https://github.com/Robo-Harness/k1)<br>[🌐&nbsp;Project&nbsp;Page](https://robo-harness.github.io/k1/) |
| **[RoboHarness: A Simple Harness Outperforms VLA and World Action Models](https://arxiv.org/abs/2610.14018)** | Arxiv<br>2026-09 | Household Tasks; Manipulation | [💻&nbsp;Code](https://github.com/BinceQu/RoboHarness) |
| **[Show-Harness: Just a VLM Agent Can Play Robots](https://arxiv.org/abs/2609.10522)** | Arxiv<br>2026-09 | Manipulation; Bimanual Manipulation | [💻&nbsp;Code](https://github.com/showlab/Show-Harness)<br>[🌐&nbsp;Project&nbsp;Page](https://showlab.github.io/Show-Harness/) |
| **[Transferring the Intelligence of VLMs to Robotic Control](https://arxiv.org/abs/2609.22966)** | Arxiv<br>2026-09 | Manipulation; Bimanual Manipulation | — |
| **[Towards the Harness of Embodied Agents](https://arxiv.org/abs/2608.11246)** | Arxiv<br>2026-08 | Manipulation; Mobile Manipulation; Long-Horizon Task Execution | [💻&nbsp;Code](https://github.com/EIT-HAI/Thea)<br>[🌐&nbsp;Project&nbsp;Page](https://eit-hai.github.io/thea/) |
| **[Zetta ζ: An Efficient Closed-Loop Embodied Harness for Self-Evolving Physical Intelligence](https://arxiv.org/abs/2608.16590)** | Arxiv<br>2026-08 | Manipulation; Household Tasks; Failure Recovery | [💻&nbsp;Code](https://github.com/air-embodied-brain/Zetta-Embodiment)<br>[🌐&nbsp;Project&nbsp;Page](https://air-embodied-brain.github.io/zetta/) |
| **[Harness VLA: Steering Frozen VLAs into Reliable Manipulation Primitives via Memory-Guided Agents](https://arxiv.org/abs/2607.08448)** | Arxiv<br>2026-07 | Manipulation; Household Tasks; Bimanual Manipulation | [💻&nbsp;Code](https://github.com/RLinf/RPent)<br>[🌐&nbsp;Project&nbsp;Page](https://harnessvla.github.io/) |
| **[PhyAgentOS: A Self-Evolving Operating System for Embodied Agents with Decoupled Cognitive Planning and Physical Execution](https://arxiv.org/abs/2607.16636)** | Arxiv<br>2026-07 | Minecraft; Stardew Valley; Don't Starve Together; Manipulation | [💻&nbsp;Code](https://github.com/PhyAgentOS/PhyAgentOS-core)<br>[🌐&nbsp;Project&nbsp;Page](https://phy-agent-os.net) |
| **[ASPIRE: Agentic /Skills Discovery for Robotics](https://arxiv.org/abs/2607.00272)** | Arxiv<br>2026-06 | Manipulation; Bimanual Handover; Household Tasks | [💻&nbsp;Code](https://github.com/NVlabs/ASPIRE) |
| **[RHO: Your Coding Agent is Secretly a Roboticist](https://arxiv.org/abs/2606.16458)** | Arxiv<br>2026-06 | Manipulation | [🌐&nbsp;Project&nbsp;Page](https://rho-robotics.github.io/) |
| **[APEX: Autonomous Policy Exploration for Self-Evolving LLM Agents](https://arxiv.org/abs/2605.21240)** | Arxiv<br>2026-05 | Jericho Text Adventures | [💻&nbsp;Code](https://github.com/liushiliushi/APEX1) |
| **[Continual Harness: Online Adaptation for Self-Improving Foundation Agents](https://arxiv.org/abs/2605.09998)** | Arxiv<br>2026-05 | Pokémon Red; Pokémon Emerald | [💻&nbsp;Code](https://github.com/sethkarten/continual-harness)<br>[🌐&nbsp;Project&nbsp;Page](https://sethkarten.ai/continual-harness/) |
| **[Device Context Protocol: A Compact, Safety-First Architecture for LLM-Driven Control of Constrained Devices](https://arxiv.org/abs/2605.26159)** | Arxiv<br>2026-05 | Embedded Device Control; Runtime Safety | [💻&nbsp;Code](https://github.com/device-context-protocol/dcp) |
| **[SPIKE: An Adaptive Dual Controller Framework for Cost-Efficient Long-Horizon Game Agents](https://arxiv.org/abs/2605.18636)** | Arxiv<br>2026-05 | Stardew Valley | [💻&nbsp;Code](https://github.com/wencanjiang/SPIKE)<br>[🌐&nbsp;Project&nbsp;Page](https://wencanjiang.github.io/projects/SPIKE/) |
| **[Code World Models for General Game Playing](https://arxiv.org/abs/2510.04542)** | ICLR<br>2026-04 | Tic-Tac-Toe; Chess Variants; Card Games | — |
| **[Harnessing Embodied Agents: Runtime Governance for Policy-Constrained Execution](https://arxiv.org/abs/2604.07833)** | Arxiv<br>2026-04 | Policy-Constrained Execution; Runtime Monitoring; Recovery | [💻&nbsp;Code](https://github.com/s20sc/harnessing-embodied-agents) |
| **[RoboClaw: An Agentic Framework for Scalable Long-Horizon Robotic Tasks](https://arxiv.org/abs/2603.11558)** | Arxiv<br>2026-03 | Manipulation | [💻&nbsp;Code](https://github.com/RoboClaw-Robotics/RoboClaw)<br>[🌐&nbsp;Project&nbsp;Page](https://roboclaw-agibot.github.io/) |
| **[Code Evolution for Control: Synthesizing Policies via LLM-Driven Evolutionary Search](https://arxiv.org/abs/2601.06845)** | Arxiv<br>2026-01 | LunarLander | [💻&nbsp;Code](https://github.com/pgg3/EvoControl) |
| **[Real-Time Reasoning Agents in Evolving Environments](https://arxiv.org/abs/2511.04898)** | Arxiv<br>2025-11 | Freeway; Snake; Overcooked | [💻&nbsp;Code](https://github.com/SALT-NLP/RealtimeGym) |
| **[VistaWise: Building Cost-Effective Agent with Cross-Modal Knowledge Graph for Minecraft](https://arxiv.org/abs/2508.18722)** | EMNLP<br>2025-11 | Minecraft | — |
| **[Cultivating Gaming Sense for Yourself: Making VLMs Gaming Experts](https://arxiv.org/abs/2503.21263)** | ACL<br>2025-07 | Flappy Bird; First-Person Shooters; Action-Role-Playing Combat | [💻&nbsp;Code](https://github.com/ipsss2/GameSense) |
| **[General Modular Harness for LLM Agents in Multi-Turn Gaming Environments](https://arxiv.org/abs/2507.11633)** | ICML Workshop<br>2025-07 | Puzzle Games; Arcade Games | — |
| **[Learning to Play Like Humans: A Framework for LLM Adaptation in Interactive Fiction Games](https://arxiv.org/abs/2505.12439)** | Findings of ACL<br>2025-07 | Interactive Fiction; Narrative Exploration | — |
| **[Code-as-Monitor: Constraint-aware Visual Programming for Reactive and Proactive Robotic Failure Detection](https://arxiv.org/abs/2412.04455)** | CVPR<br>2025-06 | Manipulation; Failure Detection | [🌐&nbsp;Project&nbsp;Page](https://zhoues.github.io/Code-as-Monitor/) |
| **[JARVIS-1: Open-World Multi-task Agents with Memory-Augmented Multimodal Language Models](https://arxiv.org/abs/2311.05997)** | TPAMI<br>2025-03 | Minecraft | [💻&nbsp;Code](https://github.com/CraftJarvis/JARVIS-1)<br>[🌐&nbsp;Project&nbsp;Page](https://craftjarvis-jarvis1.github.io/) |
| **[Reflection of Episodes: Learning to Play Game from Expert and Self Experiences](https://arxiv.org/abs/2502.13388)** | Arxiv<br>2025-02 | StarCraft II | — |
| **[Introspective Planning: Aligning Robots' Uncertainty with Inherent Task Ambiguity](https://arxiv.org/abs/2402.06529)** | NeurIPS<br>2024-12 | Mobile Manipulation; Instruction Following | [💻&nbsp;Code](https://github.com/kevinliang888/IntroPlan)<br>[🌐&nbsp;Project&nbsp;Page](https://introplan.github.io/) |
| **[Optimus-1: Hybrid Multimodal Memory Empowered Agents Excel in Long-Horizon Tasks](https://arxiv.org/abs/2408.03615)** | NeurIPS<br>2024-12 | Minecraft | [💻&nbsp;Code](https://github.com/iLearn-Lab/NeurIPS24-Optimus-1)<br>[🌐&nbsp;Project&nbsp;Page](https://cybertronagent.github.io/Optimus-1.github.io/) |
| **[Prompt a Robot to Walk with Large Language Models](https://arxiv.org/abs/2309.09969)** | CDC<br>2024-12 | Locomotion | [💻&nbsp;Code](https://github.com/HybridRobotics/prompt2walk)<br>[🌐&nbsp;Project&nbsp;Page](https://prompt2walk.github.io/) |
| **[InstructNav: Zero-shot System for Generic Instruction Navigation in Unexplored Environment](https://arxiv.org/abs/2406.04882)** | CoRL<br>2024-11 | Navigation; Instruction Following; Object-Goal Navigation | [💻&nbsp;Code](https://github.com/LYX0501/InstructNav) |
| **[ReKep: Spatio-Temporal Reasoning of Relational Keypoint Constraints for Robotic Manipulation](https://arxiv.org/abs/2409.01652)** | CoRL<br>2024-11 | Manipulation; Mobile Manipulation; Bimanual Manipulation | [💻&nbsp;Code](https://github.com/huangwl18/ReKep)<br>[🌐&nbsp;Project&nbsp;Page](https://rekep-robot.github.io/) |
| **[DoReMi: Grounding Language Model by Detecting and Recovering from Plan-Execution Misalignment](https://arxiv.org/abs/2307.00329)** | IROS<br>2024-10 | Manipulation; Locomotion | [🌐&nbsp;Project&nbsp;Page](https://sites.google.com/view/doremi-paper) |
| **[Can VLMs Play Action Role-Playing Games? Take Black Myth Wukong as a Study Case](https://arxiv.org/abs/2409.12889)** | Arxiv<br>2024-09 | Black Myth: Wukong | [🌐&nbsp;Project&nbsp;Page](https://varp-agent.github.io/) |
| **[MapGPT: Map-Guided Prompting with Adaptive Path Planning for Vision-and-Language Navigation](https://arxiv.org/abs/2401.07314)** | ACL<br>2024-08 | Navigation; Instruction Following; Object Grounding | [💻&nbsp;Code](https://github.com/chen-judge/MapGPT)<br>[🌐&nbsp;Project&nbsp;Page](https://chen-judge.github.io/MapGPT/) |
| **[DrEureka: Language Model Guided Sim-To-Real Transfer](https://arxiv.org/abs/2406.01967)** | RSS<br>2024-07 | Locomotion; Dexterous Manipulation | [💻&nbsp;Code](https://github.com/eureka-research/DrEureka)<br>[🌐&nbsp;Project&nbsp;Page](https://eureka-research.github.io/dr-eureka/) |
| **[RoboCoder: Robotic Learning from Basic Skills to General Tasks with Large Language Models](https://arxiv.org/abs/2406.03757)** | Arxiv<br>2024-06 | Locomotion; Manipulation | — |
| **[Distilling and Retrieving Generalizable Knowledge for Robot Manipulation via Language Corrections](https://arxiv.org/abs/2311.10678)** | ICRA<br>2024-05 | Manipulation; Instruction Correction | [💻&nbsp;Code](https://github.com/Stanford-ILIAD/droc)<br>[🌐&nbsp;Project&nbsp;Page](https://sites.google.com/stanford.edu/droc) |
| **[Eureka: Human-Level Reward Design via Coding Large Language Models](https://arxiv.org/abs/2310.12931)** | ICLR<br>2024-05 | Locomotion; Dexterous Manipulation | [💻&nbsp;Code](https://github.com/eureka-research/Eureka)<br>[🌐&nbsp;Project&nbsp;Page](https://eureka-research.github.io/) |
| **[Statler: State-Maintaining Language Models for Embodied Reasoning](https://arxiv.org/abs/2306.17840)** | ICRA<br>2024-05 | Manipulation; Object Rearrangement | [💻&nbsp;Code](https://github.com/ripl/statler)<br>[🌐&nbsp;Project&nbsp;Page](https://statler-lm.github.io/) |
| **[ChatGPT for Robotics: Design Principles and Model Abilities](https://arxiv.org/abs/2306.17582)** | IEEE Access<br>2024-04 | Manipulation; Navigation; Aerial Control | [💻&nbsp;Code](https://github.com/microsoft/PromptCraft-Robotics)<br>[🌐&nbsp;Project&nbsp;Page](https://www.microsoft.com/en-us/research/articles/chatgpt-for-robotics/) |
| **[Cradle: Empowering Foundation Agents Towards General Computer Control](https://arxiv.org/abs/2403.03186)** | Arxiv<br>2024-03 | Red Dead Redemption II; Stardew Valley; Cities: Skylines | [💻&nbsp;Code](https://github.com/BAAI-Agents/Cradle)<br>[🌐&nbsp;Project&nbsp;Page](https://baai-agents.github.io/Cradle/) |
| **[NavGPT: Explicit Reasoning in Vision-and-Language Navigation with Large Language Models](https://arxiv.org/abs/2305.16986)** | AAAI<br>2024-02 | Navigation; Instruction Following | [💻&nbsp;Code](https://github.com/GengzeZhou/NavGPT) |
| **[RoboScript: Code Generation for Free-Form Manipulation Tasks across Real and Simulation](https://arxiv.org/abs/2402.14623)** | Arxiv<br>2024-02 | Manipulation; Object Rearrangement | — |
| **[Demo2Code: From Summarizing Demonstrations to Synthesizing Code via Extended Chain-of-Thought](https://arxiv.org/abs/2305.16744)** | NeurIPS<br>2023-12 | Robotouille; Manipulation; Cooking Tasks | [💻&nbsp;Code](https://github.com/portal-cornell/demo2code)<br>[🌐&nbsp;Project&nbsp;Page](https://portal.cs.cornell.edu/demo2code/) |
| **[Describe, Explain, Plan and Select: Interactive Planning with Large Language Models Enables Open-World Multi-Task Agents](https://arxiv.org/abs/2302.01560)** | NeurIPS<br>2023-12 | Minecraft | [💻&nbsp;Code](https://github.com/CraftJarvis/MC-Planner) |
| **[REFLECT: Summarizing Robot Experiences for Failure Explanation and Correction](https://arxiv.org/abs/2306.15724)** | CoRL<br>2023-11 | Manipulation; Failure Diagnosis; Task Recovery | [💻&nbsp;Code](https://github.com/real-stanford/reflect)<br>[🌐&nbsp;Project&nbsp;Page](https://robot-reflect.github.io/) |
| **[Text2Motion: From Natural Language Instructions to Feasible Plans](https://arxiv.org/abs/2303.12153)** | Autonomous Robots<br>2023-11 | Manipulation; Object Rearrangement | [🌐&nbsp;Project&nbsp;Page](https://sites.google.com/stanford.edu/text2motion) |
| **[VoxPoser: Composable 3D Value Maps for Robotic Manipulation with Language Models](https://arxiv.org/abs/2307.05973)** | CoRL<br>2023-11 | Manipulation | [💻&nbsp;Code](https://github.com/huangwl18/VoxPoser)<br>[🌐&nbsp;Project&nbsp;Page](https://voxposer.github.io/) |
| **[Creative Robot Tool Use with Large Language Models](https://arxiv.org/abs/2310.13065)** | Arxiv<br>2023-10 | Manipulation; Physical Tool Use; Locomotion | [🌐&nbsp;Project&nbsp;Page](https://creative-robotool.github.io/) |
| **[TidyBot: Personalized Robot Assistance with Large Language Models](https://arxiv.org/abs/2305.05658)** | IROS<br>2023-10 | Mobile Manipulation; Household Cleanup; Object Sorting | [🌐&nbsp;Project&nbsp;Page](https://tidybot.cs.princeton.edu/) |
| **[Ghost in the Minecraft: Generally Capable Agents for Open-World Environments via Large Language Models with Text-based Knowledge and Memory](https://arxiv.org/abs/2305.17144)** | Arxiv<br>2023-05 | Minecraft | [💻&nbsp;Code](https://github.com/OpenGVLab/GITM) |
| **[Instruct2Act: Mapping Multi-modality Instructions to Robotic Actions with Large Language Model](https://arxiv.org/abs/2305.11176)** | Arxiv<br>2023-05 | Manipulation | [💻&nbsp;Code](https://github.com/OpenGVLab/Instruct2Act) |
| **[ProgPrompt: Generating Situated Robot Task Plans using Large Language Models](https://arxiv.org/abs/2209.11302)** | ICRA<br>2023-05 | Household Tasks; Manipulation | [💻&nbsp;Code](https://github.com/NVlabs/progprompt-vh)<br>[🌐&nbsp;Project&nbsp;Page](https://progprompt.github.io/) |
| **[Voyager: An Open-Ended Embodied Agent with Large Language Models](https://arxiv.org/abs/2305.16291)** | Arxiv<br>2023-05 | Minecraft | [💻&nbsp;Code](https://github.com/MineDojo/Voyager)<br>[🌐&nbsp;Project&nbsp;Page](https://voyager.minedojo.org/) |
| **[Inner Monologue: Embodied Reasoning through Planning with Language Models](https://arxiv.org/abs/2207.05608)** | CoRL<br>2022-12 | Manipulation; Mobile Manipulation; Household Tasks | [🌐&nbsp;Project&nbsp;Page](https://innermonologue.github.io/) |
| **[Code as Policies: Language Model Programs for Embodied Control](https://arxiv.org/abs/2209.07753)** | Arxiv<br>2022-09 | Manipulation | [💻&nbsp;Code](https://github.com/google-research/google-research/tree/master/code_as_policies)<br>[🌐&nbsp;Project&nbsp;Page](https://code-as-policies.github.io/) |


<a id="model-training"></a>
## Model Training

| Paper | Venue | Task | Links |
| :--- | :---: | :--- | :--- |
| **[Guava: Distilling Frontier VLMs into a Compact Agent through a Robotic Manipulation Harness](https://arxiv.org/abs/2606.18363)** | CoRL Workshop<br>2026-11 | Manipulation; Object Rearrangement | [💻&nbsp;Code](https://github.com/hdacnw/guava-release)<br>[🌐&nbsp;Project&nbsp;Page](https://guava-harness.github.io/) |
| **[Pretraining Knows What, Simulation Teaches How: Compositional Generalization for Agentic Robotics](https://arxiv.org/abs/2610.35817)** | CoRL LBR<br>2026-11 | Manipulation; Bimanual Manipulation | [🌐&nbsp;Project&nbsp;Page](https://zero-real.github.io/) |
| **[Training Reasoning Models in Simulation to Natively Use Real Robots](https://arxiv.org/abs/2611.18562)** | Arxiv<br>2026-11 | Manipulation; Object Pickup; Block Alignment | [💻&nbsp;Code](https://github.com/mit-han-lab/pear)<br>[🌐&nbsp;Project&nbsp;Page](https://mit-han-lab.github.io/pear-blog/) |
| **[AgenticRoboRL: Bringing Coding-Agent Post-Training to Agentic Robotics](https://arxiv.org/abs/2610.28589)** | Arxiv<br>2026-10 | Manipulation | [💻&nbsp;Code](https://github.com/xinxinliu-ai/AgenticRoboRL)<br>[🌐&nbsp;Project&nbsp;Page](https://xinxinliu-ai.github.io/AgenticRoboRL/) |
| **[CaPtain: A Pipeline for Post-Training Code-as-Policy Robot Agents](https://arxiv.org/abs/2610.40799)** | Arxiv<br>2026-10 | Manipulation; Object Rearrangement | [💻&nbsp;Code](https://github.com/waltstephen/CaPtain)<br>[🌐&nbsp;Project&nbsp;Page](https://waltstephen.github.io/captain/) |
| **[Odysseus: Scaling VLMs to 100+ Turn Decision-Making in Games via Reinforcement Learning](https://arxiv.org/abs/2605.00347)** | COLM<br>2026-10 | Super Mario Land; Super Mario Bros. | [💻&nbsp;Code](https://github.com/odysseus-project/odysseus-mario-training)<br>[🌐&nbsp;Project&nbsp;Page](https://odysseus-project.github.io/) |
| **[Player-1: Learning to Play from Synthetic Experience](https://arxiv.org/abs/2610.20584)** | Arxiv<br>2026-10 | Minecraft; ViZDoom; Synthetic 2D/3D Games | [🌐&nbsp;Project&nbsp;Page](https://player-1-project.github.io/) |
| **[Training One Model to Master Cross-Level Agentic Actions via Reinforcement Learning](https://arxiv.org/abs/2512.09706)** | CVPR<br>2026-06 | Minecraft | [💻&nbsp;Code](https://github.com/CraftJarvis/OpenHA)<br>[🌐&nbsp;Project&nbsp;Page](https://craftjarvis.github.io/CrossHA/) |
| **[RoboEvolve: Co-Evolving Planner-Simulator for Robotic Manipulation with Limited Data](https://arxiv.org/abs/2605.13775)** | Arxiv<br>2026-05 | Manipulation | — |
| **[MARSHAL: Incentivizing Multi-Agent Reasoning via Self-Play with Strategic LLMs](https://arxiv.org/abs/2510.15414)** | ICLR<br>2026-04 | Tic-Tac-Toe; Connect Four; Kuhn Poker; Leduc Hold'em | [💻&nbsp;Code](https://github.com/thu-nics/MARSHAL) |
| **[VAM: Verbalized Action Masking for Controllable Exploration in RL Post-Training -- A Chess Case Study](https://arxiv.org/abs/2602.16833)** | Arxiv<br>2026-02 | Chess | — |
| **[GameTalk: Training LLMs for Strategic Conversation](https://arxiv.org/abs/2601.16276)** | Arxiv<br>2026-01 | Rock-Paper-Scissors; Bertrand Competition; Bargaining Games | — |
| **[SIMA 2: A Generalist Embodied Agent for Virtual Worlds](https://arxiv.org/abs/2512.04797)** | Arxiv<br>2025-12 | ASKA; Minecraft; Cross-Game Control | [🌐&nbsp;Project&nbsp;Page](https://deepmind.google/blog/sima-2-an-agent-that-plays-reasons-and-learns-with-you-in-virtual-3d-worlds/) |
| **[VAGEN: Reinforcing World Model Reasoning for Multi-Turn VLM Agents](https://arxiv.org/abs/2510.16907)** | NeurIPS<br>2025-12 | Sokoban; FrozenLake; Navigation; Manipulation | [💻&nbsp;Code](https://github.com/mll-lab-nu/VAGEN)<br>[🌐&nbsp;Project&nbsp;Page](https://vagen-ai.github.io/) |
| **[Lumine: An Open Recipe for Building Generalist Agents in 3D Open Worlds](https://arxiv.org/abs/2511.08892)** | Arxiv<br>2025-11 | Genshin Impact; Wuthering Waves; Honkai: Star Rail | — |
| **[CombatVLA: An Efficient Vision-Language-Action Model for Combat Tasks in 3D Action Role-Playing Games](https://arxiv.org/abs/2503.09527)** | ICCV<br>2025-10 | Black Myth: Wukong; Sekiro | [💻&nbsp;Code](https://github.com/ChenVoid/CombatVLA)<br>[🌐&nbsp;Project&nbsp;Page](https://combatvla.github.io/) |
| **[Game-TARS: Pretrained Foundation Models for Scalable Generalist Multimodal Game Agents](https://arxiv.org/abs/2510.23691)** | Arxiv<br>2025-10 | Minecraft; First-Person Shooters; Web 3D Games | [🌐&nbsp;Project&nbsp;Page](https://seed-tars.com/game-tars/) |
| **[OpenHA: A Series of Open-Source Hierarchical Agentic Models in Minecraft](https://arxiv.org/abs/2509.13347)** | Arxiv<br>2025-09 | Minecraft | [💻&nbsp;Code](https://github.com/CraftJarvis/OpenHA) |
| **[Reinforced Language Models for Sequential Decision Making](https://arxiv.org/abs/2508.10839)** | Arxiv<br>2025-08 | Snake; FrozenLake | — |
| **[Think in Games: Learning to Reason in Games via Reinforcement Learning with Large Language Models](https://arxiv.org/abs/2508.21365)** | Arxiv<br>2025-08 | Honor Of Kings | — |
| **[JARVIS-VLA: Post-Training Large-Scale Vision Language Models to Play Visual Games with Keyboards and Mouse](https://arxiv.org/abs/2503.16365)** | Findings of ACL<br>2025-07 | Minecraft | [💻&nbsp;Code](https://github.com/CraftJarvis/JarvisVLA)<br>[🌐&nbsp;Project&nbsp;Page](https://craftjarvis.github.io/JarvisVLA/) |
| **[Learning Strategic Language Agents in the Werewolf Game with Iterative Latent Space Policy Optimization](https://arxiv.org/abs/2502.04686)** | ICML<br>2025-07 | Werewolf | — |
| **[G1: Bootstrapping Perception and Reasoning Abilities of Vision-Language Model via Reinforcement Learning](https://arxiv.org/abs/2505.13426)** | Arxiv<br>2025-05 | 2048; Shisen-Sho; Swap | [💻&nbsp;Code](https://github.com/chenllliang/G1) |
| **[AHA: A Vision-Language-Model for Detecting and Reasoning Over Failures in Robotic Manipulation](https://arxiv.org/abs/2410.00371)** | ICLR<br>2025-04 | Manipulation; Failure Detection; Failure Diagnosis | [💻&nbsp;Code](https://github.com/NVlabs/AHA)<br>[🌐&nbsp;Project&nbsp;Page](https://aha-vlm.github.io/) |
| **[Robotic Programmer: Video Instructed Policy Code Generation for Robotic Manipulation](https://arxiv.org/abs/2501.04268)** | Arxiv<br>2025-01 | Manipulation | [🌐&nbsp;Project&nbsp;Page](https://ustcwhy.github.io/publications/robopro/) |
| **[OmniJARVIS: Unified Vision-Language-Action Tokenization Enables Open-World Instruction Following Agents](https://arxiv.org/abs/2407.00114)** | NeurIPS<br>2024-12 | Minecraft | [💻&nbsp;Code](https://github.com/CraftJarvis/OmniJARVIS)<br>[🌐&nbsp;Project&nbsp;Page](https://omnijarvis.github.io/) |
| **[RoboCodeX: Multimodal Code Generation for Robotic Behavior Synthesis](https://arxiv.org/abs/2402.16117)** | ICML<br>2024-07 | Manipulation; Navigation | — |
| **[LLaMA-Rider: Spurring Large Language Models to Explore the Open World](https://arxiv.org/abs/2310.08922)** | Findings of NAACL<br>2024-06 | Minecraft | [💻&nbsp;Code](https://github.com/PKU-RL/LLaMA-Rider) |

<a id="benchmark"></a>
## Benchmark

Benchmarks for code agents and for the broader abilities needed by agentic embodied systems, including tool use, planning, memory, exploration, and robot control. Some directly test executable programs; others provide complementary agent-level evaluation under action or skill interfaces.

The selection draws on the robotics and game-agent surveys above. See the [benchmark guide](docs/BENCHMARK_GUIDE.md) and [game-agent guide](docs/GAME_AGENT_GUIDE.md) for interfaces, source checks, and the distinction between offline diagnostics and closed-loop execution.

| Paper | Venue | Task | Links |
| :--- | :---: | :--- | :--- |
| **[Embodied First Exam](https://arxiv.org/abs/2611.12177)** | Arxiv<br>2026-11 | Spatial Puzzles; Dexterous Manipulation; Multi-Robot Interaction; Dynamic Whole-Body Control; Sim-To-Sim Engineering | [💻&nbsp;Code](https://github.com/mll-lab-nu/embodied-first-exam)<br>[🌐&nbsp;Project&nbsp;Page](https://www.embodied-first-exam.ai/) |
| **[Are Frontier VLM Agents Ready to Be Robot Generalists? An Empirical Study with the Embodied Agent Arena](https://arxiv.org/abs/2610.00854)** | Arxiv<br>2026-10 | Geometry; Spatial Reasoning; Affordance; Planning; Manipulation | [💻&nbsp;Code](https://github.com/embodied-agent-arena/embodied-agent-arena)<br>[🌐&nbsp;Project&nbsp;Page](https://embodied-agent-arena.github.io/embodied-agent-arena/) |
| **[Can AI Agents Learn Their Way to the Top? Evaluating Heuristic Learning in a Long-Running Game Agent Competition](https://arxiv.org/abs/2610.12341)** | Arxiv<br>2026-10 | Adversarial Games; Game-Policy Coding | [💻&nbsp;Code](https://github.com/THU-CST-SAST/AAArena) |
| **[Embodied Skill Bench: Benchmarking How Well Agents with Embodied Skills Perform on Physical Tasks](https://arxiv.org/abs/2610.16238)** | Arxiv<br>2026-10 | Manipulation; Skill Reuse | [💻&nbsp;Code](https://github.com/HanZhi306/EmbodiedSkill-Bench) |
| **[PTCG-Bench: Can LLM Agents Master Pokémon Trading Card Game?](https://arxiv.org/abs/2605.29653)** | Findings of EMNLP<br>2026-10 | Pokémon Trading Card Game | [💻&nbsp;Code](https://github.com/zjunet/PTCG-Bench) |
| **[RoboQuest: Generalist Physical Agents that Search, Inspect and Test](https://arxiv.org/abs/2610.10388)** | Arxiv<br>2026-10 | Mobile Manipulation; Search; Inspection; Interactive Testing | [💻&nbsp;Code](https://github.com/declare-lab/RoboQuest)<br>[🌐&nbsp;Project&nbsp;Page](https://declare-lab.github.io/RoboQuest/) |
| **[RobotWorld: Benchmarking Multimodal Agents for Robot Use Across Diverse Tasks and Embodiments](https://arxiv.org/abs/2610.10409)** | Arxiv<br>2026-10 | Manipulation; Mobile Manipulation; Locomotion; Driving; Aerial Control | [💻&nbsp;Code](https://github.com/robotworldai/robotworld)<br>[🌐&nbsp;Project&nbsp;Page](https://robotworldai.github.io/) |
| **[SpireBench: Evaluating Long-Horizon Strategic Play of Agentic Models with Slay the Spire](https://arxiv.org/abs/2610.12596)** | Arxiv<br>2026-10 | Slay The Spire | — |
| **[CodeActionBench: Evaluating Agentic Code-as-Policy for Embodied Manipulation](https://arxiv.org/abs/2609.33807)** | Arxiv<br>2026-09 | Manipulation | [💻&nbsp;Code](https://github.com/lyhkk/CodeActionBench)<br>[🌐&nbsp;Project&nbsp;Page](https://codeactionbench.org/benchmark) |
| **[EmbodiedSWE: Coding Agents for Long Horizon Dexterous Robotics](https://arxiv.org/abs/2609.27308)** | Arxiv<br>2026-09 | Manipulation; Assembly; Locomotion And Manipulation | [💻&nbsp;Code](https://github.com/EmbodiedSWE/EmbodiedSWE)<br>[🌐&nbsp;Project&nbsp;Page](https://embodiedswe.github.io/) |
| **[GameHorizon Suite: Multi-Horizon Data and Evaluation in Gameplay](https://arxiv.org/abs/2609.25001)** | Arxiv<br>2026-09 | Minecraft; Multi-Game Video Understanding | [🌐&nbsp;Project&nbsp;Page](https://gamehorizon-suite.github.io/) |
| **[StarDojo: Benchmarking Open-Ended Behaviors of Agentic Multimodal LLMs in Production-Living Simulations with Stardew Valley](https://arxiv.org/abs/2507.07445)** | ECCV<br>2026-09 | Stardew Valley | [💻&nbsp;Code](https://github.com/StarDojo2025/stardojo) |
| **[AgenticSTS: A Bounded-Memory Testbed for Long-Horizon LLM Agents](https://arxiv.org/abs/2607.02255)** | Arxiv<br>2026-07 | Slay The Spire 2 | [💻&nbsp;Code](https://github.com/AlayaLab/AgenticSTS)<br>[🌐&nbsp;Project&nbsp;Page](https://alayalab.github.io/AgenticSTS/) |
| **[Compiled Agency: Coding Agents as Game AI Researchers -- from a Roguelike to StarCraft II and Civilization](https://arxiv.org/abs/2609.18996)** | Arxiv<br>2026-07 | Roguelike; StarCraft II; Freeciv | — |
| **[GameVerse: Can Vision-Language Models Learn from Video-based Reflection?](https://arxiv.org/abs/2603.06656)** | ICML<br>2026-07 | Angry Birds; Plants Vs. Zombies; Tic-Tac-Toe | [💻&nbsp;Code](https://github.com/THUSI-Lab/GameVerse)<br>[🌐&nbsp;Project&nbsp;Page](https://gameverse-bench.github.io/) |
| **[RoboDojo: A Unified Sim-and-Real Benchmark for Comprehensive Evaluation of Generalist Robot Manipulation Policies](https://arxiv.org/abs/2607.04434)** | Arxiv<br>2026-07 | Manipulation; Long-Horizon Execution | [💻&nbsp;Code](https://github.com/RoboDojo-Benchmark/RoboDojo)<br>[🌐&nbsp;Project&nbsp;Page](https://robodojo-benchmark.com/) |
| **[RoboMME: Benchmarking and Understanding Memory for Robotic Generalist Policies](https://arxiv.org/abs/2603.04639)** | ICML<br>2026-07 | Manipulation; Temporal, Spatial, Object, And Procedural Memory | [💻&nbsp;Code](https://github.com/RoboMME/robomme_benchmark)<br>[🌐&nbsp;Project&nbsp;Page](https://robomme.github.io/) |
| **[OmniGameArena: A Unified UE5 Benchmark for VLM Game Agents with Improvement Dynamics](https://arxiv.org/abs/2606.09826)** | Arxiv<br>2026-06 | UE5 Games; Solo Play; PvP; Cooperation | [💻&nbsp;Code](https://github.com/mxlin043/OmniGameArena)<br>[🌐&nbsp;Project&nbsp;Page](https://mxlin043.github.io/OmniGameArena/) |
| **[GameWorld: Towards Standardized and Verifiable Evaluation of Multimodal Game Agents](https://arxiv.org/abs/2604.07429)** | Arxiv<br>2026-04 | Browser Games; Puzzle Games; Action Games | [💻&nbsp;Code](https://github.com/gameworld-project/gameworld) |
| **[lmgame-Bench: How Good are LLMs at Playing Games?](https://arxiv.org/abs/2505.15146)** | ICLR<br>2026-04 | Sokoban; Tetris; 2048; Candy Crush; Pokémon Red | [💻&nbsp;Code](https://github.com/lmgame-org/GamingAgent) |
| **[Mastering PokeGym: Graph-Guided Multimodal Evolution at Test Time](https://arxiv.org/abs/2604.08340)** | Arxiv<br>2026-04 | Pokémon Legends: Z-A | — |
| **[Orak: A Foundational Benchmark for Training and Evaluating LLM Agents on Diverse Video Games](https://arxiv.org/abs/2506.03610)** | ICLR<br>2026-04 | StarCraft II; Street Fighter III; Stardew Valley; Slay The Spire | [💻&nbsp;Code](https://github.com/krafton-ai/Orak) |
| **[CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation](https://arxiv.org/abs/2603.22435)** | Arxiv<br>2026-03 | Manipulation | [🌐&nbsp;Project&nbsp;Page](https://capgym.github.io/) |
| **[The PokeAgent Challenge: Competitive and Long-Context Learning at Scale](https://arxiv.org/abs/2603.15563)** | Arxiv<br>2026-03 | Pokémon Battles; Pokémon RPG Speedrunning | — |
| **[BotzoneBench: Scalable LLM Evaluation via Graded AI Anchors](https://arxiv.org/abs/2602.13214)** | Arxiv<br>2026-01 | Board Games; Card Games; Strategic Decision-Making | [💻&nbsp;Code](https://github.com/AMysteriousBeing/BotzoneBench) |
| **[KORGym: A Dynamic Game Platform for LLM Reasoning Evaluation](https://arxiv.org/abs/2505.14552)** | NeurIPS<br>2025-12 | Logic Games; Visual Puzzles; Strategic Games | [💻&nbsp;Code](https://github.com/multimodal-art-projection/KORGym) |
| **[FlashAdventure: A Benchmark for GUI Agents Solving Full Story Arcs in Diverse Adventure Games](https://arxiv.org/abs/2509.01052)** | EMNLP<br>2025-11 | Flash Adventure Games; Story Completion | [💻&nbsp;Code](https://github.com/ahnjaewoo/FlashAdventure) |
| **[EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents](https://arxiv.org/abs/2502.09560)** | ICML<br>2025-07 | Household Tasks; Navigation; Manipulation | [💻&nbsp;Code](https://github.com/EmbodiedBench/EmbodiedBench)<br>[🌐&nbsp;Project&nbsp;Page](https://embodiedbench.github.io/) |
| **[TextQuests: How Good are LLMs at Text-Based Video Games?](https://arxiv.org/abs/2507.23701)** | Arxiv<br>2025-07 | Infocom Text Adventures | [💻&nbsp;Code](https://github.com/centerforaisafety/textquests)<br>[🌐&nbsp;Project&nbsp;Page](https://textquests.ai/) |
| **[VideoGameBench: Can Vision-Language Models complete popular video games?](https://arxiv.org/abs/2505.18134)** | Arxiv<br>2025-05 | Retro Video Games; Navigation; Full-Game Completion | [💻&nbsp;Code](https://github.com/alexzhang13/videogamebench) |
| **[BALROG: Benchmarking Agentic LLM and VLM Reasoning On Games](https://arxiv.org/abs/2411.13543)** | ICLR<br>2025-04 | NetHack; MiniHack; Crafter; TextWorld; BabaIsAI; BabyAI | [💻&nbsp;Code](https://github.com/balrog-ai/BALROG)<br>[🌐&nbsp;Project&nbsp;Page](https://balrogai.com/) |
| **[TextArena](https://arxiv.org/abs/2504.11442)** | Arxiv<br>2025-04 | Competitive Text Games; Negotiation; Social Reasoning | [💻&nbsp;Code](https://github.com/TextArena/TextArena)<br>[🌐&nbsp;Project&nbsp;Page](https://www.textarena.ai/) |
| **[Large Language Models Play StarCraft II: Benchmarks and A Chain of Summarization Approach](https://arxiv.org/abs/2312.11865)** | NeurIPS<br>2024-12 | StarCraft II | — |
| **[TeamCraft: A Benchmark for Multi-Modal Multi-Agent Systems in Minecraft](https://arxiv.org/abs/2412.05255)** | Arxiv<br>2024-12 | Minecraft; Multi-Agent Cooperation | [💻&nbsp;Code](https://github.com/teamcraft-bench/teamcraft) |
| **[GameBench: Evaluating Strategic Reasoning Abilities of LLM Agents](https://arxiv.org/abs/2406.06613)** | Arxiv<br>2024-06 | Board Games; Card Games; Strategic Decision-Making | [💻&nbsp;Code](https://github.com/Joshuaclymer/GameBench) |
| **[CivRealm: A Learning and Reasoning Odyssey in Civilization for Decision-Making Agents](https://arxiv.org/abs/2401.10568)** | ICLR<br>2024-05 | Freeciv; Civilization-Style Strategy | [💻&nbsp;Code](https://github.com/bigai-ai/civrealm) |
| **[SmartPlay: A Benchmark for LLMs as Intelligent Agents](https://arxiv.org/abs/2310.01557)** | ICLR<br>2024-05 | Rock-Paper-Scissors; Tower Of Hanoi; Minecraft | [💻&nbsp;Code](https://github.com/microsoft/SmartPlay) |

<a id="contributing"></a>
## Contributing

Follow [CONTRIBUTING.md](CONTRIBUTING.md), use the **Add a paper** issue form, or create a note from [notes/TEMPLATE.md](notes/TEMPLATE.md). All repository content uses English.

The catalogue is maintained directly in Markdown. See [docs/MAINTAINING.md](docs/MAINTAINING.md) for editing and publishing instructions.

<a id="license"></a>

## License

Original curation, notes, and artwork are available under the [MIT License](LICENSE). Linked papers, code, datasets, and other third-party materials retain their respective licenses.
