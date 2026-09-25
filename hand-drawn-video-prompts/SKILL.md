---
name: hand-drawn-video-prompts-vietnamese
description: Use when a user provides a Vietnamese script, article, or voiceover and needs copy-ready vertical B-roll prompts or an assembled 9:16 hand-drawn video with Vietnamese voiceover and subtitles.
---

# Vietnamese Hand-Drawn Video Prompts

Turn a Vietnamese article, script, or voiceover into executable 9:16 hand-drawn B-roll shots.

The content language is Vietnamese.

Technical image-generation and image-to-video prompts may remain in English when that produces more reliable results with the target generation model, but all narrative content, voiceover, keywords, captions, and subtitles must be Vietnamese.

## Modes

### Prompt mode

Use when the user asks only for prompts.

Output:

1. Vietnamese shot breakdown.
2. Vietnamese voiceover for each shot.
3. Visual metaphor for each shot.
4. Copy-ready image-generation prompt.
5. Copy-ready image-to-video prompt.
6. Vietnamese post-production keyword.
7. Suggested shot duration.

Do not claim that images, videos, audio, subtitles, or an exported MP4 were generated unless an actual generation/export tool returned the result.

### Complete-video mode

Use when the user explicitly asks for a complete video.

Read:

references/automation-workflow.md

Follow the complete workflow:

Vietnamese script
→ shot breakdown
→ still images
→ animated clips
→ Vietnamese voiceover
→ Vietnamese transcription/captions
→ editable timeline
→ MP4 export
→ verification.

An asynchronous generation task must be waited on until completion or explicit failure.

Never claim that a video is complete without an actual successful exported video result.

## Language rules

The default language for the project is Vietnamese.

### Voiceover

Voiceover must be natural Vietnamese.

Use Vietnamese pronunciation and phrasing.

Do not translate Vietnamese source material into Chinese or English for the voiceover.

Do not invent facts, numbers, dates, company names, quotations, or conclusions that are not present in the source script.

The voiceover should preserve the meaning of the user's Vietnamese source.

### Subtitles

Subtitles must be Vietnamese.

Use the actual Vietnamese voiceover as the timing source when transcription is available.

If transcription differs from the source script, use the user's original Vietnamese wording for factual corrections.

Subtitles must be added as a deterministic post-production text layer.

Do not ask the image or video generation model to render subtitles.

### Keywords

Post-production keywords must be Vietnamese.

Examples:

- AI TỐN ĐIỆN
- BẮT ĐẦU TÍNH
- CHI PHÍ TĂNG
- ÁP LỰC
- DOANH THU
- VỐN ĐẦU TƯ
- RỦI RO

Keep keywords short and readable.

When text accuracy matters, put the keyword in the deterministic post-production layer instead of relying on image generation.

## Non-negotiable visual rules

Use:

- vertical 9:16 composition
- solid warm-white canvas
- exact base color #F8F6EF
- extremely subtle low-contrast paper grain
- thick imperfect black hand-drawn marker/crayon outlines
- bold flat wax-crayon blocks
- sunflower yellow
- saturated cobalt blue
- vivid tomato red
- only a small muted-green accent
- natural restrained Q-version proportions
- simple hand-drawn composition
- 2–4 large readable visual groups
- generous breathing room

Do not use:

- photorealism
- glossy rendering
- realistic cinematic lighting
- 3D rendering
- cyber HUD
- complex UI
- vintage newspaper styling
- yellowed old paper
- gray-brown backgrounds
- gradients
- vignettes
- logos unless supplied as approved reference material
- watermarks
- unnecessary decorations
- giant heads
- tiny bodies
- bulging eyes
- distorted faces

## Composition

Use vertical 9:16.

The main visual group should normally occupy approximately 60–70% of the frame width.

Keep generous space above and below.

Reserve the lower area for Vietnamese subtitles.

Do not put important generated text in the subtitle area.

Use 2–4 large visual groups per shot.

The scene should be understandable on a phone within approximately one second.

Describe spatial relationships explicitly:

- left
- center
- right
- foreground
- background
- upper area
- lower area

Do not rely only on abstract emotional descriptions.

## Text inside generated artwork

Generated artwork should normally contain no text.

If a short Vietnamese keyword is explicitly requested, it may be placed directly on the warm-white paper or beside the relevant object.

Keep it:

- short
- readable
- fixed
- small
- away from faces
- away from fast-moving objects
- outside the bottom subtitle zone

Do not use:

- sticky notes
- label cards
- stickers
- rounded text boxes
- title panels
- isolated white cards
- subtitle boxes

For company names, people names, dates, amounts, statistics, quotations, or long Vietnamese sentences, prefer deterministic post-production text.

If text generation accuracy is uncertain, provide both:

1. a recommended Vietnamese text version
2. a text-free safe version

## Real entities

For real companies, products, organizations, public figures, countries, or other identifiable entities:

- use restrained visual identity cues
- do not invent logos
- do not deform official logos
- use supplied reference images when exact identity is important
- prefer deterministic post-production overlays for exact names, logos, dates, and numbers

For public figures, use stylized non-photorealistic Q-version representation rather than photorealistic face cloning.

## Animation rules

Use tactile paper stop-motion language.

Default:

tactile 10–12 fps paper stop-motion

Use:

- locked flat frontal camera
- rigid flat paper cutouts
- small settling bounce
- simple object slides
- short hinge-like hand movement
- subtle wheel rotation
- restrained object motion
- stable final frame

Avoid:

- camera drift
- zoom
- parallax
- smooth 3D motion
- face morphing
- lip sync
- newly appearing characters
- newly appearing logos
- text morphing
- watermark
- audio generated inside the video model

When using first and last frames:

1. First frame = completely blank #F8F6EF warm-white paper.
2. Last frame = supplied completed illustration.
3. Keep the final composition consistent.
4. Hold the exact final frame for approximately the final 0.8 seconds.

If only one completed image is available:

Animate the supplied completed illustration in place while preserving every drawn shape and the exact composition.

## Shot duration

Default shot duration:

4–6 seconds.

Use the voiceover as the main timing reference.

Adjust shot duration around natural Vietnamese speech boundaries.

Do not force every shot to have exactly the same duration when the voiceover requires otherwise.

## Visual metaphor

Use clear visual metaphors.

Examples:

| Vietnamese relationship | Preferred visual metaphor |
|---|---|
| cạnh tranh / chạy đua | race, chase, tug-of-war |
| chi phí / tiêu hao | leaking tank, heavy weight, monster eating coins, meter |
| kiểm chứng / báo cáo | exam, magnifying glass, health check |
| lựa chọn / kết luận | forked road, scale, switch, two doors |
| rủi ro / áp lực | crack, warning, unstable blocks, countdown |
| tăng trưởng | rising arrow, growing stack, expanding object |
| giảm sút | falling blocks, shrinking bar, leaking container |
| đầu tư | carts, coins, machine receiving resources |
| doanh thu | coins, flowing revenue stream |
| công nghệ | machine, chip, gear, circuit-like hand-drawn object |

The metaphor must communicate the meaning of the Vietnamese narration without requiring generated text.

## Required shot output

For each shot provide:

### Cảnh XX

**Lời đọc:**
Vietnamese voiceover.

**Thời lượng:**
Approximately 4–6 seconds.

**Ý tưởng hình ảnh:**
A concise Vietnamese visual metaphor.

**Keyword hậu kỳ:**
Short Vietnamese keyword.

**Flow image prompt:**
Technical prompt, preferably in English for reliable image generation.

**Flow image-to-video prompt:**
Technical prompt, preferably in English for reliable video generation.

## Quality control

Before considering the workflow complete, verify:

- 9:16 aspect ratio
- #F8F6EF warm-white background
- consistent visual style
- consistent character proportions
- no unwanted text
- no malformed logos
- Vietnamese voiceover
- Vietnamese subtitles
- subtitle safe area
- correct narration order
- correct scene order
- no missing scenes
- no audio gaps
- no severe character deformation
- stable final frames
- MP4 export actually exists

A generated prompt is not an exported video.

A generated image is not an exported video.

An asynchronous task that is still running is not a completed video.

Only report completion after the final MP4 export has succeeded and the resulting file is available.
