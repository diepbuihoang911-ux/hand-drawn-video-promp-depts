# Hand-Drawn Video Prompts

[简体中文](README.md) · [English](README.en.md)

Turn a Chinese voiceover script into consistent 9:16 illustrated B-roll prompts for Flow, Nano Banana, and compatible video workflows.

Hand-Drawn Video Prompts is designed for AI explainers, finance commentary, technology analysis, and educational short-form video creators. It provides:

- Semantic shots designed for roughly 4–6 seconds each
- Copy-ready English image prompts for Flow and Nano Banana
- Copy-ready English image-to-video prompts
- Small Chinese keywords embedded directly in the artwork when requested
- Visual metaphors tied to the original narration
- Accuracy notes for flags, companies, logos, public figures, dates, and numbers

## Why it exists

Most AI video workflows break between script analysis and visual generation. A strong argument still needs a clear visual idea every few seconds, and generated images often drift in style, background color, typography, and composition.

This skill standardizes the middle layer: script → visual metaphor → still frame → image-to-video motion.

## Demo

Two vertical examples generated with this visual workflow:

- [Demo 722 — 32 seconds](demo/hand-drawn-video-demo-722.mp4)
- [Demo 723 — 41 seconds](demo/hand-drawn-video-demo-723.mp4)

The files are kept as original 9:16 MP4s so visitors can download or preview the actual output.

The workflow can also turn recognizable technology figures—such as Elon Musk, Jensen Huang, and Mark Zuckerberg—into clearly non-photorealistic Q-version characters using safe identity cues like hairstyle, glasses, clothing, pose, and props.

## Visual baseline

- Modern Q-version hand-drawn crayon illustration
- Vertical 9:16 composition
- Fixed warm-white canvas: `#F8F6EF`
- Extremely subtle, low-contrast paper grain
- Thick imperfect black hand-drawn lines
- Sunflower yellow, cobalt blue, and tomato red
- Natural, restrained Q-version proportions
- Two to four clear visual groups
- Small Chinese keywords written directly on the paper, never as sticky notes or cards
- Clear lower-third space reserved for subtitles

## Quick start

1. Load the skill in Codex.
2. Paste a Chinese voiceover script.
3. Ask for prompt-only output or a complete video workflow.
4. Copy the English prompts into Flow or Nano Banana.
5. Use the finished still as the Last Frame and a fixed `#F8F6EF` paper frame as the First Frame.

Example:

```text
Break this Chinese voiceover into Flow image and image-to-video prompts. Put the small Chinese keyword directly in the illustration, keep the background at #F8F6EF, and reserve the bottom for subtitles:

AI makes ideas cheaper, but real-world validation is still slow.
```

## Output format

Each shot includes:

- Source narration
- Suggested duration
- Visual metaphor
- Chinese on-image keyword
- Flow image prompt
- Flow image-to-video prompt
- Entity accuracy notes

## Entity accuracy

The model can handle Q-version composition and motion, but it should not be trusted to reproduce every logo, flag, public-figure likeness, number, or long sentence exactly.

- Flags: specify official structure, colors, proportions, and symbols; use a reference image or deterministic overlay when exactness matters.
- Logos: use brand cues for generation and add the original logo as a reference or post-production layer when required.
- Public figures: use clearly non-photorealistic Q-version identity cues such as hairstyle, glasses, clothing, pose, and props. Do not bypass safety restrictions or create realistic face clones.
- Numbers, dates, and long text: reserve them for a deterministic subtitle or graphic layer.

## Repository layout

```text
hand-drawn-video-prompts/
├── hand-drawn-video-prompts/
│   ├── SKILL.md                  # English runtime skill
│   ├── SKILL.zh-CN.md            # Chinese skill reference
│   └── references/
├── outputs/                      # Public prompt examples and tests
├── demo/                         # Vertical demonstration videos
├── README.md                     # Chinese documentation (Default)
├── README.en.md                  # English documentation
└── README.zh-CN.md               # 中文文档
```

## Current scope

This is a prompt and visual-decomposition skill. It does not include Flow or Nano Banana API calls, an image/video generation service, complex version management, or pixel-perfect guarantees for generated media.

It can be combined with Flow, Nano Banana, ChatCut, and other compatible tools.

## License

MIT License. Contributions, translations, and new style references are welcome.
