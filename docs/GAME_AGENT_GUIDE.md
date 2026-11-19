# Game Agent Guide

The expansion starts from [Towards Generalist Game Agents: A Survey of Foundation Models in Virtual Worlds](https://arxiv.org/abs/2605.09965), especially Sections 4–6 and Tables 4, 5, and 7. The [author collection](https://github.com/THUSI-Lab/Awesome-LFMs-Play-Games) provides leads; the original papers and official publication pages determine the recorded titles, dates, interfaces, and venues.

This pass adds **16 Model Training**, **12 Harness**, and **26 Benchmark** papers, together with the source survey. It covers visual control, Minecraft, real-time action, strategy, interactive fiction, board/card games, and strategic communication. The homepage retains its four categories and four bibliographic columns.

## Selection and Classification

The reading dimensions below describe how a paper contributes to a game agent. They are curation decisions based on its principal contribution.

- **Model Training:** the pretrained LLM/VLM or its native game-action representation learns from demonstrations, preferences, rewards, or continued game-domain training. The recipe column distinguishes SFT, preference learning, RL, and related foundation training.
- **Harness:** runtime organization, perception scaffolds, executable code, planning, memory, real-time scheduling, or adaptation of prompts and skills. Record separately any trained detector, goal selector, or downstream execution module.
- **Benchmark:** a game environment, task suite, interface, or protocol is the primary evaluation contribution. Training data, fine-tuned baselines, and reference harnesses are documented without duplicating the paper.
- **Survey:** the source paper supplies a field-level reference and a [short reading note](../notes/2026-generalist-game-agents.md).

## LLM/VLM Training and Post-Training

These entries complement the existing CrossHA, VAGEN, and JARVIS-VLA rows. Methods differ in whether deployment emits dialogue, semantic actions, behavior tokens, or low-level controls. Continued pretraining is identified explicitly rather than counted as an RL result.

| Paper / Method | Training Target and Recipe | Deployment Interface | Task |
| :--- | :--- | :--- | :--- |
| [Player-1](https://arxiv.org/abs/2610.20584) | Gameplay SFT; multi-environment PPO. Gameplay-trajectory SFT initializes computer-use models, then PPO on synthetic environments improves control and transfer. | Screenshots; composite keyboard/mouse actions | Minecraft; ViZDoom; Synthetic 2D/3D games |
| [Odysseus](https://arxiv.org/abs/2605.00347) | SFT initialization; PPO with a turn-level critic. Long-horizon PPO uses a lightweight turn-level critic to train a pretrained VLM across more than 100 decisions. | Screenshots; controller-button combinations | Super Mario Land; Super Mario Bros. |
| [VAM](https://arxiv.org/abs/2602.16833) | RL post-training with action masking. Verbalized action masks and iterative pruning control exploration during LLM RL post-training. | Text chess positions; masked move choices | Chess |
| [GameTalk](https://arxiv.org/abs/2601.16276) | GRPO; DPO; STaR. Conversation-level rewards train strategic communication across complete multi-turn interactions. | Dialogue; strategic utterances | Rock-Paper-Scissors; Bertrand competition; Bargaining games |
| [SIMA 2](https://arxiv.org/abs/2512.04797) | Demonstration training; autonomous feedback-driven learning. A Gemini-based agent learns from labeled demonstrations and environment feedback; generated tasks and rewards support further adaptation. | Screenshots and instructions; keyboard/mouse actions | ASKA; Minecraft; Cross-game control |
| [Lumine](https://arxiv.org/abs/2511.08892) | Game-domain multimodal training. Trains an end-to-end visual game agent with adaptive reasoning; evaluates transfer from Genshin Impact to other 3D worlds. | Screenshots; keyboard/mouse actions | Genshin Impact; Wuthering Waves; Honkai: Star Rail |
| [Game-TARS](https://arxiv.org/abs/2510.23691) | Continued pretraining; native action modeling. Continual pretraining on heterogeneous interaction data learns a shared native-control action space with sparse thinking. | Screenshots; unified keyboard/mouse actions | Minecraft; First-person shooters; Web 3D games |
| [MARSHAL](https://arxiv.org/abs/2510.15414) | Multi-agent self-play RL. Self-play RL uses turn-level advantages and agent-specific normalization for cooperative and competitive reasoning. | Text game states; multi-agent actions | Tic-Tac-Toe; Connect Four; Kuhn Poker; Leduc Hold'em |
| [OpenHA](https://arxiv.org/abs/2509.13347) | Hierarchical action-token training; mixed-action SFT. Chain of Action trains a monolithic VLA over mixed action abstractions, using abstract actions as intermediate reasoning. | Images and text; hierarchical behavior/action tokens | Minecraft |
| [Think in Games](https://arxiv.org/abs/2508.21365) | Online RL. Online reinforcement learning updates language-guided policies for strategic decisions in Honor of Kings. | Text state; language-guided game policy | Honor of Kings |
| [MS-GRPO](https://arxiv.org/abs/2508.10839) | Multi-step GRPO. Multi-step GRPO attributes episode rewards across decisions and weights episode sampling for LLM post-training. | Text-mediated state; sequential actions | Snake; FrozenLake |
| [G1](https://arxiv.org/abs/2505.13426) | Teacher cold start; GRPO. A perception-enhanced cold start and RL jointly improve visual recognition and game decisions in VLM-Gym. | Game screenshots; discrete or coordinate actions | 2048; Shisen-Sho; Swap |
| [CombatVLA](https://arxiv.org/abs/2503.09527) | Supervised video-action training. Trains a compact VLA on video-action demonstrations and uses truncated action-of-thought inference for combat. | Video; action-of-thought control sequences | Black Myth: Wukong; Sekiro |
| [Werewolf LSPO](https://arxiv.org/abs/2502.04686) | CFR in latent strategy space; iterative DPO. Alternates latent-strategy optimization with DPO of the LLM, rather than only attaching a fixed strategy scaffold. | Dialogue; strategic utterances | Werewolf |
| [OmniJARVIS](https://arxiv.org/abs/2407.00114) | Multimodal autoregressive training; imitation-learning action decoder. Adds discretized behavior tokens to a pretrained multimodal language model and learns unified reasoning, planning, and action sequences. | Images and text; learned behavior tokens | Minecraft |
| [LLaMA-Rider](https://arxiv.org/abs/2310.08922) | Exploration-data SFT. Fine-tunes the LLM on exploration trajectories with feedback-driven revision and subtask relabeling. | Text state; API calls | Minecraft |

## Harnesses

A custom harness can generate and execute code without using a general-purpose coding-agent runtime. The interface column records this distinction. A performance change from memory, reflection, or prompt revision does not by itself establish a model-weight update.

| Paper / Method | Setup and Interface | Harness Contribution | Task |
| :--- | :--- | :--- | :--- |
| [APEX](https://arxiv.org/abs/2605.21240) | Custom; text actions and strategy-DAG memory | A persistent strategy map discovers unexplored branches and balances exploration against familiar high-reward behavior. | Jericho text adventures |
| [SPIKE](https://arxiv.org/abs/2605.18636) | Custom; event-triggered strategic/reactive controllers | An event trigger escalates fast local control to strategic reasoning; separate memory structures support reuse and recovery. | Stardew Valley |
| [Continual Harness](https://arxiv.org/abs/2605.09998) | Custom harness editing; coding-agent integrations | Online, reset-free refinement edits prompts, subagents, skills, and memory. Model co-training is reported as a separate extension. | Pokémon Red; Pokémon Emerald |
| [AgileThinker](https://arxiv.org/abs/2511.04898) | Custom; concurrent planning and reactive execution | Reactive and planning processes run together to balance reasoning depth against changing game states and time pressure. | Freeway; Snake; Overcooked |
| [Code World Models](https://arxiv.org/abs/2510.04542) | Custom; executable Python world models | An LLM synthesizes transition, legal-action, and inference functions; search planners use the resulting code as a simulator. | Tic-Tac-Toe; Chess variants; Card games |
| [VistaWise](https://arxiv.org/abs/2508.18722) | Custom; cross-modal knowledge graph and desktop skills | Retrieval over a cross-modal knowledge graph supports keyboard/mouse skills; object-detector fine-tuning is a separate component. | Minecraft |
| [GMH](https://arxiv.org/abs/2507.11633) | Custom; modular perception, memory, and reasoning | A reusable harness composes visual scaffolding, memory, reasoning, and prompt optimization around a fixed backbone. | Puzzle games; Arcade games |
| [LPLH](https://arxiv.org/abs/2505.12439) | Custom; text commands and map/experience memory | Map construction, context-aware action learning, and experience analysis support narrative-grounded gameplay. | Interactive fiction; Narrative exploration |
| [GameSense](https://arxiv.org/abs/2503.21263) | Custom; generated execution modules | A VLM develops code and specialized real-time modules; downstream module training is distinct from training the VLM planner. | Flappy Bird; First-person shooters; Action-role-playing combat |
| [Reflection of Episodes](https://arxiv.org/abs/2502.13388) | Custom; TextStarCraft II actions and episodic reflection | Keyframes, expert experience, and post-episode reflection update textual experience used in later decisions. | StarCraft II |
| [VARP](https://arxiv.org/abs/2409.12889) | Custom; screenshots and keyboard/mouse actions | A visual trajectory system and action planner ground control in recorded experience; the paper also provides combat tasks. | Black Myth: Wukong |
| [DEPS](https://arxiv.org/abs/2302.01560) | Custom; text descriptions and skill plans | Descriptions and explanations of execution failures revise plans, while a separate goal selector orders candidate subgoals. | Minecraft |

## Benchmarks

Game names identify representative evaluated settings rather than a claim to list every title in a suite. Keep the exact interface, assistance, timing, and training/evaluation split with any reported score.

| Paper / Method | Tested Interface | Evaluation Role | Task |
| :--- | :--- | :--- | :--- |
| [SpireBench](https://arxiv.org/abs/2610.12596) | Complete-game text state; tools and batched actions | Full runs test tactical versus strategic skill, knowledge dependence, and memory across runs. | Slay the Spire |
| [AAArena](https://arxiv.org/abs/2610.12341) | Coding-agent development; standalone programs | Budgeted competitions test opponent selection, replay analysis, and revisions to executable game policies. | Adversarial games; Game-policy coding |
| [GameHorizon Suite](https://arxiv.org/abs/2609.25001) | Offline video questions; online keyboard/mouse control | Multi-horizon data and evaluation separate offline questions from online Minecraft subtask and whole-task completion. | Minecraft; Multi-game video understanding |
| [Gauntlet](https://arxiv.org/abs/2609.18996) | General-purpose coding agents; frozen executable policies | A develop-freeze-evaluate protocol tests coding agents' research decisions and held-out gameplay with zero model calls during execution. | Roguelike; StarCraft II; Freeciv |
| [AgenticSTS](https://arxiv.org/abs/2607.02255) | Text state; typed retrieval and game tools | A bounded-memory testbed assembles fresh decision contexts and ablates individual memory layers. | Slay the Spire 2 |
| [OmniGameArena](https://arxiv.org/abs/2606.09826) | Screenshots; native game-control primitives | New UE5 games and repeated-round skill-prompt refinement measure cold-start play, improvement dynamics, and variant transfer. | UE5 games; Solo play; PvP; Cooperation |
| [PTCG-Bench](https://arxiv.org/abs/2605.29653) | Partial-state text; game tools | Separates first-run play, accumulated-experience improvement, and modular-harness effects. | Pokémon Trading Card Game |
| [PokeGym](https://arxiv.org/abs/2604.08340) | Visual observations; game-control actions | Repeated-episode evaluation studies joint perception/strategy/action configuration adaptation; G-EvoMAC is the proposed solver. | Pokémon Legends: Z-A |
| [GameWorld](https://arxiv.org/abs/2604.07429) | Screenshots; computer-use or semantic controls | Standardized tasks and state-verifiable metrics compare two action interfaces without treating them as interchangeable. | Browser games; Puzzle games; Action games |
| [PokeAgent Challenge](https://arxiv.org/abs/2603.15563) | Battle state/actions; emulator tools | Distinct battling and speedrunning tracks test adversarial partial observability and long-context sequential decisions. | Pokémon battles; Pokémon RPG speedrunning |
| [GameVerse](https://arxiv.org/abs/2603.06656) | Visual observations; semantic or GUI controls | Reflect-and-retry evaluations compare frozen-model video reflection over failure trajectories and expert tutorials. | Angry Birds; Plants vs. Zombies; Tic-Tac-Toe |
| [BotzoneBench](https://arxiv.org/abs/2602.13214) | Text state; game actions against fixed AI anchors | Skill-graded specialized opponents anchor evaluation rather than relying only on changing LLM-versus-LLM pools. | Board games; Card games; Strategic decision-making |
| [FlashAdventure](https://arxiv.org/abs/2509.01052) | Screenshots; GUI actions | Full story arcs stress clue retention, long-horizon planning, and interaction; COAST is the supporting memory-based solver. | Flash adventure games; Story completion |
| [TextQuests](https://arxiv.org/abs/2507.23701) | Native text observations and commands | Full interactive-fiction sessions test sustained self-contained reasoning and exploration without external tools. | Infocom text adventures |
| [StarDojo](https://arxiv.org/abs/2507.07445) | Multimodal observations; semantic game actions | Open-ended production, exploration, combat, and social tasks are evaluated through a common game interface. | Stardew Valley |
| [Orak](https://arxiv.org/abs/2506.03610) | MCP game tools; text/image observations | Twelve games support benchmark evaluation, modular-harness ablations, and expert-trajectory SFT. The paper appears once under Benchmark. | StarCraft II; Street Fighter III; Stardew Valley; Slay the Spire |
| [VideoGameBench](https://arxiv.org/abs/2505.18134) | Raw screenshots; keyboard/button actions | Full-game visual control is evaluated in real time and in a paused Lite setting; these timing contracts should remain separate. | Retro video games; Navigation; Full-game completion |
| [lmgame-Bench](https://arxiv.org/abs/2505.15146) | Gym-style actions; configurable perception/memory scaffolds | Controls prompt sensitivity and interface effects across platformer, puzzle, and narrative games; also studies training transfer. | Sokoban; Tetris; 2048; Candy Crush; Pokémon Red |
| [KORGym](https://arxiv.org/abs/2505.14552) | Text or images; multi-turn actions | A dynamic multi-game platform supports adjustable reasoning evaluation and interactive training settings. | Logic games; Visual puzzles; Strategic games |
| [TextArena](https://arxiv.org/abs/2504.11442) | Text observations and actions | A collection of competitive text games supports training, human/model online play, and opponent-relative skill evaluation. | Competitive text games; Negotiation; Social reasoning |
| [TeamCraft](https://arxiv.org/abs/2412.05255) | Multimodal task prompts; cooperative actions | Procedurally generated tasks and expert demonstrations test transfer across goals, scenes, and team sizes. | Minecraft; Multi-agent cooperation |
| [BALROG](https://arxiv.org/abs/2411.13543) | Text and/or visual observations; environment actions | A unified interface and fine-grained progress metrics evaluate exploration and long-horizon reasoning across game families. | NetHack; MiniHack; Crafter; TextWorld; BabaIsAI; BabyAI |
| [GameBench](https://arxiv.org/abs/2406.06613) | Text state; game moves | Nine game environments probe different strategic reasoning demands under common agent scaffolds. | Board games; Card games; Strategic decision-making |
| [CivRealm](https://arxiv.org/abs/2401.10568) | Tensor or language state; semantic actions | An open-ended strategy environment evaluates learning, reasoning, diplomacy, and full-game planning. | Freeciv; Civilization-style strategy |
| [TextStarCraft II](https://arxiv.org/abs/2312.11865) | Text state summaries; strategic commands | A textual RTS environment and human/gameplay evaluations test strategic planning; summarization and fine-tuning are additional contributions. | StarCraft II |
| [SmartPlay](https://arxiv.org/abs/2310.01557) | Text observations; semantic game actions | A multi-game benchmark separates agent capabilities such as planning, spatial reasoning, and learning from history. | Rock-Paper-Scissors; Tower of Hanoi; Minecraft |

## Reading the Results

- **Interface and information access:** screenshots, textified simulator state, MCP tools, and semantic skills provide different observation and action contracts. GameWorld, GameVerse, Orak, and lmgame-Bench expose useful comparisons.
- **Timing:** VideoGameBench's real-time and paused Lite settings differ. AgileThinker and SPIKE explicitly organize reasoning around changing states and response cost.
- **Adaptation target:** Continual Harness edits the runtime and also studies a separate model co-training extension. APEX and Reflection of Episodes accumulate strategic evidence or text memory. GameSense develops execution modules; VistaWise separately fine-tunes a detector.
- **Whole-game versus diagnostic success:** GameHorizon has offline video questions and online Minecraft tests. Offline accuracy, subtask completion with resets, and complete long-horizon runs answer different questions.
- **Strategy and communication:** Werewolf LSPO, GameTalk, MARSHAL, VAM, TextArena, PTCG-Bench, BotzoneBench, and SpireBench cover different forms of adversarial, cooperative, or partially observed decisions.
- **Coding-agent development versus runtime play:** Gauntlet and AAArena evaluate agents that develop executable policies. The shipped program's execution and the coding agent's development budget are separate parts of the experiment.
- **Benchmark/model hybrids:** Orak, TeamCraft, and lmgame-Bench also provide training resources or learning experiments. They remain single Benchmark entries under the primary-contribution rule.

## Publication and Identity Checks

The catalogue orders papers by their actual first Arxiv release months, newest first, including cases whose identifiers suggest a different month. Within the same month, full titles sort alphabetically, ignoring case. Venue shows `Arxiv YYYY-MM` alongside any verified formal venue and edition year; the latter does not replace the sorting month.

Primary venue sources include:

- **LLaMA-Rider:** [Findings of NAACL 2024](https://aclanthology.org/2024.findings-naacl.292/).
- **OmniJARVIS:** [NeurIPS 2024 proceedings](https://proceedings.neurips.cc/paper_files/paper/2024/hash/85f1225db986e629289f402c46eff1a4-Abstract-Conference.html).
- **Werewolf LSPO:** [ICML 2025 proceedings](https://proceedings.mlr.press/v267/xu25h.html).
- **CombatVLA:** [ICCV 2025 proceedings](https://openaccess.thecvf.com/content/ICCV2025/html/Chen_CombatVLA_An_Efficient_Vision-Language-Action_Model_for_Combat_Tasks_in_3D_ICCV_2025_paper.html).
- **Odysseus:** [COLM 2026 accepted papers](https://colm.eventhosts.cc/Conferences/2026/AcceptedPapers) and [author publication record](https://wwj-y.github.io/publications/). This is the Mario paper, distinct from similarly named web-agent benchmarks.
- **MARSHAL:** the [official implementation](https://github.com/thu-nics/MARSHAL) records ICLR 2026 acceptance.
- **DEPS:** [NeurIPS 2023 proceedings](https://proceedings.neurips.cc/paper_files/paper/2023/hash/6b8dfb8c0c12e6fafc6c256cb08a5ca7-Abstract-Conference.html).
- **GameSense:** [ACL 2025 proceedings](https://aclanthology.org/2025.acl-long.643/); the catalogue uses the published title, *Cultivating Gaming Sense for Yourself: Making VLMs Gaming Experts*.
- **GMH:** the [author comments](https://arxiv.org/abs/2507.11633) identify the ICML MAS workshop. Venue retains the Workshop qualifier.
- **LPLH:** [Findings of ACL 2025](https://aclanthology.org/2025.findings-acl.531/).
- **Code World Models:** [ICLR 2026 proceedings](https://proceedings.iclr.cc/paper_files/paper/2026/hash/d8a12fde9e72444e1b356e8c37e53753-Abstract-Conference.html).
- **VistaWise:** [EMNLP 2025 proceedings](https://aclanthology.org/2025.emnlp-main.1111/).
- **SmartPlay:** [ICLR 2024 proceedings](https://proceedings.iclr.cc/paper_files/paper/2024/hash/063d1fadbde557466bf5bcffe814a64e-Abstract-Conference.html).
- **TextStarCraft II:** [NeurIPS 2024 proceedings](https://proceedings.neurips.cc/paper_files/paper/2024/hash/f0ebc318e2df08360b2df559e81602e5-Abstract-Conference.html).
- **CivRealm:** [ICLR 2024 proceedings](https://proceedings.iclr.cc/paper_files/paper/2024/hash/76d2f8e328e1081c22a77ca0fa330ca5-Abstract-Conference.html). Its implementation uses Freeciv, a Civilization-inspired environment.
- **BALROG:** [ICLR 2025 proceedings](https://proceedings.iclr.cc/paper_files/paper/2025/hash/f0b1515be276f6ba82b4f2b25e50bef0-Abstract-Conference.html).
- **lmgame-Bench:** [ICLR 2026 proceedings](https://proceedings.iclr.cc/paper_files/paper/2026/hash/83a4ea71b13bc86308a2bd0b5e07fb61-Abstract-Conference.html).
- **Orak:** [ICLR 2026 conference page](https://iclr.cc/virtual/2026/poster/10010438).
- **KORGym:** [NeurIPS 2025 proceedings](https://proceedings.neurips.cc/paper_files/paper/2025/hash/ebfa4297cd6419f64efe86f657ba49d0-Abstract-Conference.html).
- **PokeAgent Challenge:** [author comments](https://arxiv.org/abs/2603.15563) identify the NeurIPS 2025 Competition Track; the 2026 preprint is sorted by its first paper release.
- **GameVerse:** the [official implementation](https://github.com/THUSI-Lab/GameVerse) records ICML 2026.
- **PTCG-Bench:** [Findings of EMNLP 2026](https://aclanthology.org/2026.findings-emnlp.1689/).
- **FlashAdventure:** [EMNLP 2025 proceedings](https://aclanthology.org/2025.emnlp-main.1192/).
- **StarDojo:** [author comments](https://arxiv.org/abs/2507.07445) record ECCV 2026 acceptance.
- **PokeGym:** the current [Arxiv title](https://arxiv.org/abs/2604.08340) is *Mastering PokeGym: Graph-Guided Multimodal Evolution at Test Time*. The same paper introduces the benchmark and G-EvoMAC; the catalogue includes it once.

Other entries retain `Arxiv YYYY-MM` where no formal publication was verified. Paper and official project links do not establish that code, weights, datasets, and benchmark assets are all released. Missing or mismatched implementation links are omitted. In particular, the historical TextStarCraft II repository pointer currently identifies unrelated content, and the old PokeAgent speedrun URL redirects to the separate Continual Harness release; neither is labeled as a complete benchmark-code release here.

Return to the [main catalogue](../README.md).
