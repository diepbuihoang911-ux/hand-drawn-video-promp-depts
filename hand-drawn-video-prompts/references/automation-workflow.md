# Vietnamese Hand-Drawn Video Automation Workflow

This workflow is for creating complete vertical 9:16 hand-drawn videos from Vietnamese articles, scripts, or voiceover text.

## Goal

Vietnamese article/script
→ Vietnamese voiceover
→ hand-drawn visual scenes
→ animated clips
→ Vietnamese captions
→ editable timeline
→ MP4 export

## Default parameters

- Aspect ratio: 9:16
- Typical shot duration: 4–6 seconds
- Background: exact warm-white #F8F6EF
- Visual style: modern Q-version hand-drawn crayon illustration
- Lines: thick imperfect black hand-drawn lines
- Accent colors: sunflower yellow, cobalt blue, tomato red
- Voiceover: natural Vietnamese
- Captions: Vietnamese
- Subtitle placement: lower safe area
- Generated artwork: normally no text
- Final output: 9:16 MP4

## Execution order

### 1. Prepare Vietnamese script

Preserve the user's Vietnamese source.

Split it into scenes and Vietnamese voiceover segments.

Do not invent facts, dates, amounts, company names, quotations, or conclusions.

### 2. Generate still images

Generate one finished composition per shot.

Use the fixed #F8F6EF warm-white background.

Keep the same visual language across all shots.

Do not rely on image generation for exact:

- names
- numbers
- dates
- company names
- long sentences
- subtitles

If the user already provides visual assets, prefer those assets when appropriate.

### 3. Generate animated clips

Convert each still image into a 4–6 second vertical clip.

Use tactile 10–12 fps paper stop-motion.

Keep:

- locked frontal camera
- consistent character design
- consistent paper texture
- consistent palette
- stable final frame

If a shot fails, retry only that shot when possible.

### 4. Generate Vietnamese voiceover

Generate natural Vietnamese narration from the approved Vietnamese script.

Do not translate the voiceover into Chinese or English.

Do not silently rewrite factual claims.

### 5. Generate Vietnamese captions

Transcribe the Vietnamese voiceover.

Correct transcription against the approved Vietnamese source when needed.

Use deterministic caption text.

Do not ask the image/video generation model to render subtitles.

### 6. Assemble timeline

Place:

- video clips
- Vietnamese voiceover
- Vietnamese subtitles
- post-production keywords

in the correct order.

Voiceover is the primary timing reference.

Adjust shot duration around natural Vietnamese speech boundaries.

### 7. Export

Export a real 9:16 MP4.

Before reporting completion, verify that the exported MP4 exists and is accessible.

## Completion rule

Never say that the video is complete merely because:

- prompts were generated
- images were generated
- clips were requested
- an asynchronous task was started
- a timeline was prepared

An asynchronous task must be awaited until it completes or reports an explicit failure.

The final MP4 export must succeed before saying the video is complete.

## Required delivery

A complete-video workflow should deliver:

- final MP4
- editable project/timeline when supported
- Vietnamese subtitles as burned-in or separate subtitle track
- list of failed shots
- list of manual corrections
- list of unresolved items

If export fails, report the failure and its known cause instead of claiming completion.
