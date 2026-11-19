# Banner Assets

The README uses `banner-realistic.png`, a generated composite with realistic materials and photographic environment references. It is centered at 640 pixels wide and links to the full-resolution image. The current banner has no repository headline, so the README heading appears only once. Architecture labels remain in the image. `banner.svg` retains the earlier editable schematic architecture.

## Reference Media

- **Architecture:** the repository's original Model + Harness + Game/Robot diagram in `banner.svg`.
- **Game:** an actual Minecraft frame from the [Voyager project's house-building demonstration](https://voyager.minedojo.org/assets/videos/gallery/house.mp4). See the [Voyager project page](https://voyager.minedojo.org/). Minecraft imagery belongs to its respective rights holders.
- **Robotics:** the Franka Panda manipulation photograph published on the [DAIR Lab robots page](https://dair.engineering.upenn.edu/robots/), with the [original photo](https://dair.engineering.upenn.edu/assets/img/panda.jpg). Source photography remains subject to its original rights.

The environment panels are generated composites based on these references, rather than unaltered records of this repository's experiments.

## Generation

Created with the built-in `image_gen` tool. Opaque background. Reference inputs: the previous architecture banner, the Voyager gameplay frame, and the DAIR Lab photograph.

### Original Generation Prompt

```text
Use case: infographic-diagram; style-transfer and compositing edit.
Asset type: the main GitHub README banner for "Awesome Embodied Code Agents".

Inputs:
Image 1 is the EDIT TARGET: the existing architecture banner. Preserve its scientific meaning and its clear model + harness + environment organization.
Image 2 is a SUPPORTING GAME INSERT: an actual Minecraft gameplay frame from the Voyager research project. Use this authentic screenshot as the Game environment imagery. Retain the recognizable block-textured terrain, jungle, player, and wooden construction; crop away or remove its "Build House with Human Feedback" caption.
Image 3 is a SUPPORTING ROBOTICS INSERT: a photograph of a real Franka Panda arm grasping a blue bottle in a university robotics lab. Use this actual photograph as the Robotics environment imagery. Keep the white articulated arm, mechanically correct joints and gripper, bottle, and real workbench appearance; crop tightly to make the robot clearly recognizable.

Primary request: replace the flat cartoon/vector treatment with a sophisticated, substantially more REALISTIC research architecture visualization, including photographic environment panels. The entire graphic must feel materially richer and more convincing while remaining a readable diagram.

Style: premium scientific editorial visualization with realistic 3D hardware and photo-composited scene windows. Pale ivory/white and very light sage background; charcoal/forest-green typography; restrained teal, blue, lavender, and warm metallic accents. Realistic diffuse daylight, gentle contact shadows, brushed metal, matte white surfaces, subtly translucent glass layers, credible reflections and depth. Keep the interface readable and the background quiet.

Composition: retain a wide landscape banner at approximately the same 2.15:1 aspect ratio as Image 1. Title across the top. On the left and center, a single boundary labeled "Embodied Agent" contains a learned "Foundation Model" and a distinct "Harness". Give the model a detailed, believable AI processor with a neural-network motif instead of a flat cartoon brain. Present Harness modules as refined physical/interface components with depth: "Perception", "Planning", "Memory", "Code Runtime & Tools", and "Verifier". The code runtime should visibly evoke a real coding terminal, with a small, clean Python program on a dark screen. Increase the visual presence of the two environment windows on the right: Game on top, Robotics below, each filled by the corresponding authentic input imagery rather than a drawn miniature diorama.

Architecture: connect Foundation Model and Harness bidirectionally. From the Harness, a shared "Actions" interface branches to BOTH Game and Robotics. A clean return arrow from BOTH environment windows, labeled "Observations / State / Feedback", closes the loop back to the agent. Include the task/instruction input at the top. Keep arrow directions and hierarchy unambiguous. Foundation Model and Harness must remain separate visible components inside one agent.

Exact English text to render legibly:
"Awesome Embodied Code Agents"
"Embodied Agent"
"Foundation Model"
"Harness"
"Perception"
"Planning"
"Memory"
"Code Runtime & Tools"
"Verifier"
"Actions"
"Game"
"Robotics"
"Task / Instruction"
"Observations / State / Feedback"

Use clean professional sans-serif typography. Prioritize these main labels; omit unnecessary tiny captions or footer badges if they interfere with clarity. The scene panels should look like an actual game screenshot and an actual laboratory photograph, respectively. Do not replace them with toy blocks or cartoon robot illustrations. Do not introduce extra agents, fictional architecture modules, logos, watermarks, or unrelated decorations. Keep the whole banner light, polished, realistic, and suitable as a research repository's cover.
```

### Current Edit: Remove the Repeated Headline

Edited with the built-in `image_gen` tool, using the previous `banner-realistic.png` as the single edit target. The output replaces the README asset at the same path. The page retains its text heading and 640-pixel image width.

Final edit prompt:

```text
Use case: text-localization / precise-object-edit.
Asset: existing GitHub README architecture banner.
Input image is the EDIT TARGET, not a style reference.
Make one narrow edit: remove the large top headline reading "Awesome Embodied Code Agents" completely. Reconstruct the pale ivory/sage background behind that heading naturally. Do not add any replacement headline, title, subtitle, slogan, badge, or watermark.
After removing the headline, tighten the redundant top margin by modestly trimming only the now-empty upper strip, approximately 80–90 pixels from the original 1840×854 image, so the image reads as a compact architecture illustration. Keep the entire Task / Instruction box and all architecture elements and arrowheads fully visible with a small breathing margin; do not crop either side or the bottom.
Preserve all remaining visual content and exact English labels as closely as possible: Embodied Agent, Foundation Model, Harness, Perception, Planning, Memory, Code Runtime & Tools, Verifier, Actions, Game, Robotics, Task / Instruction, Observations / State / Feedback. Preserve the original positions relative to each other, realistic processor and terminal, pastel glass module surfaces, pale background, directional connections, actual Minecraft scene, and actual laboratory robot photograph. Do not redraw or redesign the robot or gameplay panels. Retain the light realistic scientific-architecture style. The only removed text must be the large repository headline at the top.
```
