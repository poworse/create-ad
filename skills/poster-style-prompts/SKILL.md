---
name: poster-style-prompts
description: Use when the user wants to analyze reference posters or images and extract reusable visual prompts, lighting/composition notes, subject-background ratios, or ad-style prompt templates for future image generation.
---

# Poster Style Prompts

## Overview

Use this skill to turn one or more reference posters into reusable prompt language for future image generation. Focus on transferable visual patterns instead of copying exact faces, logos, or poster text.

## When to Use

- The user provides poster, ad, KV, or promo images and wants similar atmosphere later.
- The task asks for style analysis, lighting analysis, composition breakdown, or prompt extraction.
- The user specifically cares about character-to-background scale, standing position, framing, or environment relationship.
- The output should be reusable for Midjourney, Flux, SDXL, 即梦, 可灵, or generic image prompting.

Do not use this skill when the task is mainly retouching, OCR, or recreating a poster pixel-for-pixel.

## Workflow

1. Read all reference images as a set first.
2. Separate common traits from image-specific details.
3. Analyze the image in six dimensions:
   - style and mood
   - lighting and time of day
   - composition and aspect ratio
   - subject/background relationship
   - color palette and material cues
   - poster-safe empty space for later typography
4. Convert the analysis into generic prompt language that preserves vibe, not identity.
5. Output clean Markdown the user can reuse directly.

## What To Observe

### Style and Mood

- Is it variety-show, lifestyle commercial, fashion editorial, movie-like, documentary, or e-commerce?
- Is the feeling warm, festive, dreamy, premium, relaxed, youthful, intimate, energetic, or quiet?

### Lighting and Time

- Identify golden hour, blue hour, night market lighting, overcast daylight, studio fill, or mixed lighting.
- Note whether the light is soft or hard, whether highlights bloom, and whether background bokeh is important.
- Pay attention to the color contrast between subject light and ambient light.

### Composition and Size

- State the likely format such as `9:16`, `4:5`, `3:4`, or other vertical-poster ratios.
- Estimate how much of the frame the subject occupies. Use rough percentages when exact measurement is impossible.
- Describe whether the person is full-body, three-quarter, half-body, or close portrait.
- Note where empty space exists for title, logo, or campaign copy.

### Subject and Background Relationship

- Explain whether the person dominates the scene or blends into it.
- Describe distance from camera, standing position, and whether the subject is centered or slightly offset.
- Note how the environment supports the person: framing canopy, booth, trees, grass, lights, props, foreground blur.
- Mention whether the background is only decorative or also narrative.

### Prompt Generalization

- Keep the environment type, lighting scheme, framing, depth, and emotional tone.
- Remove exact brands, celebrity identity, show names, slogans, and visible text.
- Replace specifics with reusable equivalents like `outdoor market booth`, `warm string lights`, `summer dusk`, `commercial celebrity poster`, `wooden stall`, `soft dreamy bokeh`.

## Output Requirements

Always return Markdown. Prefer this structure:

```md
# Reference Poster Analysis

## Shared Visual Traits
- ...

## Key Differences
- ...

## Reusable Prompt Keywords
- ...

## General Prompt
[Chinese version]

## General Prompt (EN)
[English version]

## Optional Negative Prompt
- ...
```

If the user asks for more depth, add sections for:

- `构图与尺寸`
- `人物与环境关系`
- `光影拆解`
- `模型专用版本`

## Prompt Writing Rules

- Write prompts with moderate generality: similar vibe, not literal duplication.
- Preserve camera distance, subject scale, and environmental layering.
- Mention foreground, midground, and background when depth matters.
- Use concrete visual words instead of abstract praise.
- If an observation is inferred rather than certain, say so.

## Common Failure Modes

- Overfitting to text, brand marks, or celebrity identity.
- Listing objects without explaining their compositional role.
- Ignoring how much of the frame the person occupies.
- Describing only the subject and forgetting why the background matters.
- Making prompts too generic and losing the poster's emotional temperature.

## Quick Prompt Formula

Use this pattern when the user wants a compact reusable prompt:

`[poster type], [subject scale], [setting], [lighting], [subject placement], [environment framing], [color palette], [depth cues], [mood], [commercial finish]`

Example:

`vertical commercial lifestyle poster, full-body subject occupying about 70% of the frame, standing at a wooden outdoor market booth, warm dusk string lights, near-center placement with a slight offset, canopy and trees framing the subject, golden and amber palette with blue-hour background, dreamy bokeh and soft foreground blur, relaxed youthful festive mood, polished celebrity-ad photography`
