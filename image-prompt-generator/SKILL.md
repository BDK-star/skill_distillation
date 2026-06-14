---
name: "image-prompt-generator"
description: "Generates GPT Image prompts and visual briefs for Xiaohongshu covers, concept posters, typography visuals, city atlas travel posters, portrait/editorial photos, anime character fashion covers, and GPT Image 2 advanced workflows. Use when the user asks for 图片提示词, GPT Image prompt, 小红书封面, 海报, 概念图, 字体美学, 城市海报, 城市地图集, 旅行海报, LUMEN ATLAS, 视觉隐喻, 写真, 人像摄影, 清透人像, 明亮写真, 晴朗记忆感人像, 动漫角色封面, 海贼王人物海报, ONE PIECE fashion cover, image2, gpt-image-2, 分层图, 批量生图, 健身图解, 手绘标注, or social-media visual prompts."
---

# Image Prompt Generator

Create GPT Image-ready visual briefs for four primary modes:

1. **XHS Cover** - 小红书封面、种草封面、知识封面、情绪价值封面。
2. **Concept Poster** - 概念海报、字体美学、视觉隐喻、艺术海报。
3. **Epic Narrative Poster** - 双重曝光、人物剪影、IP/小说/动漫史诗叙事海报。
4. **Portrait Editorial** - 写真、人像、头像、氛围照、商业摄影。

Also support **Product Visual/Edit** prompts when the user asks for product refinement, product replacement, exploded views, natural compositing, product light effects, or industrial line art.

Also support **Anime Character Fashion Cover** prompts when the user asks for anime/pirate-adventure character posters, One Piece-style fan fashion covers, luxury magazine cover variants, or character replacement templates.

Also support **GPT Image 2 Advanced Workflows** for image-model-only tasks: layered posters, batch variants, life milestone narrative posters, personalized fitness infographics, photo doodle annotations, and palm-reading entertainment diagrams.

The skill should behave like an interactive visual creative director: show the available image types when the request is broad, collect only the key missing details for the chosen type, generate a ready-to-use prompt, then ask whether to generate the image with image2 / `gpt-image-2` when an image model is available.

## Quick Workflow

1. Run `🔴 CHECKPOINT 1: Image Type Selection`.
2. Run `🔴 CHECKPOINT 2: Template-Specific Intake`.
3. Load `references/template-index.md`, `references/intake-guide.md`, and only the matching template file.
4. Generate a coherent GPT Image brief, not a tag list.
5. Run `🔴 CHECKPOINT 3: Prompt Approval`.
6. Run `🔴 CHECKPOINT 4: Image2 Generation Offer`.

## 🔴 CHECKPOINT 1: Image Type Selection

If the user request is broad, such as "帮我生成一个图片提示词" or "做一张图", show this image type menu and ask the user to choose one:

1. **XHS Cover** - 小红书封面、种草图、知识卡封面、情绪价值封面。
2. **Concept Poster** - 概念海报、字体美学、视觉隐喻、艺术海报。
3. **City Atlas Poster** - 城市地图集、国家地理风旅行海报、LUMEN ATLAS。
4. **Epic Narrative Poster** - 双重曝光、人物剪影、小说/IP/动漫史诗海报。
5. **Portrait Editorial** - 写真、人像、清透人像、明亮写真、个人品牌照。
6. **Anime Character Fashion Cover** - 动漫角色封面、海贼王人物风格、奢华杂志封面。
7. **Product Visual/Edit** - 产品精修、换背景、合成、结构图、工业线稿。
8. **GPT Image 2 Advanced Workflows** - 分层图、批量生图、人生照片、健身图解、手绘标注、手相娱乐图。

If the user already names a type, template, product, city, person, style, or source image task, skip the menu and continue directly.

## 🔴 CHECKPOINT 2: Template-Specific Intake

Use `references/intake-guide.md` to ask only the missing details required by the selected type.

- Ask at most one compact question at a time.
- If the user's input already includes enough details, infer optional fields and draft immediately.
- For template families with style choices, show the available style variants and wait for a choice unless the user's wording clearly selects one.
- For image-only or upload-dependent workflows, ask for the missing source image or state that the result will be a runnable prompt only.

## 🔴 CHECKPOINT 3: Prompt Approval

After generating the prompt, ask whether the user wants to adjust any of these fields: style, visible text, composition, subject details, color palette, aspect ratio, or negative constraints.

If the user asks for changes, update only the affected prompt sections and keep the selected template family.

## 🔴 CHECKPOINT 4: Image2 Generation Offer

After the prompt is approved, ask: "是否要基于这个提示词调用 image2 / `gpt-image-2` 直接生成图片？"

- If an image-generation tool is available and the user says yes, call it with the approved prompt.
- If no image-generation tool is available, say the prompt is ready to copy into image2 / `gpt-image-2`; do not claim that an image was generated.
- For image-model-only workflows, keep the `Image Model Requirement` section visible.

## Mode Selection

Use **XHS Cover** when the goal is scroll-stopping social content, strong title hierarchy, product seeding, knowledge packaging, or lifestyle advice.

Use **Concept Poster** when the goal is metaphor, typography, a phrase or word as visual subject, city atlas travel posters, brand/art poster logic, or symbolic composition.

Use **Epic Narrative Poster** when the goal is a film-poster-like image, double exposure, a side-profile silhouette filled with story worlds, IP/novel/anime character ensembles, or collectible epic poster visuals.

Use **Portrait Editorial** when the goal is a person, avatar, fashion/lifestyle photo, beauty image, mood portrait, clear translucent portrait, bright summer-air portrait, or realistic editorial photography.

Use **Anime Character Fashion Cover** when the goal is a single anime-style protagonist rendered as a luxury fashion magazine cover, especially pirate-adventure or One Piece-style fan cover prompts. If the user asks to choose a picture style, offer or apply one of the available style variants: Mediterranean Resort Muse, Intellectual Coastal Palace, or Royal Crimson Empress.

Use **Product Visual/Edit** when the user provides or describes a product and asks for product retouching, white-background product renders, internal structure displays, product-to-scene compositing, product replacement, product lighting, or industrial design sketches.

Use **GPT Image 2 Advanced Workflows** only when the request explicitly depends on image-model execution or image editing:

- **Layered Poster / 分层图**: generate one complete poster plus separate recomposable layers such as background, people/scene, hero object, decorative elements, and text/graphics.
- **Batch Variants / 批量生图**: generate multiple variants of the same product, theme, cover, or campaign with controlled differences in scene, angle, palette, copy, and composition.
- **Life Milestone Narrative / 人生照片**: turn a portrait, biography, school, career, family, travel, or milestone story into a collectible narrative poster, usually using Epic Narrative Poster logic.
- **Personalized Fitness Infographic / 健身训练图**: create a non-medical exercise-plan image from body data, goals, and training constraints.
- **Photo Doodle Annotation / 手绘标注**: preserve an uploaded photo while adding hand-drawn outlines, arrows, short notes, recipe/ingredient labels, or social-story annotations.
- **Palm Reading Entertainment / 手相娱乐图解**: create a palm-line diagram for entertainment only, without scientific claims or deterministic predictions.

## Image Model Only Gate

Apply this gate before drafting any **GPT Image 2 Advanced Workflows** output:

- These workflows require `gpt-image-2` or an image-capable model/tool such as the Responses API `image_generation` tool.
- If the current environment is text-only, return a ready-to-copy image prompt and clearly state that execution requires an image model; do not claim that images, layers, edits, or batches have been generated.
- In `Output Settings`, default to `model: gpt-image-2`; for Responses API workflows, write `requires image_generation tool`.
- For upload-dependent workflows, state which source images are required, such as product photo, portrait, food photo, or palm image.
- Never promise exact multi-file layer export unless the actual image tool supports it; phrase layer requests as an image-model prompt requirement: "generate separate recomposable layer images with transparent/no-background layers where supported."
- For health, body, identity, or palm-reading content, include the required boundary statement in the prompt itself.

## Interaction Rules

- Ask only when the core subject is missing or the mode changes the result materially.
- If the user provides a theme, title, product, person, or scene, generate a first draft immediately.
- Infer optional fields from the target mode: style, palette, format, lighting, metaphor, composition, and negative constraints.
- Ask at most one concise clarification before the first draft.
- If the user says "用模板", "套模板", "替换关键词", or provides a reusable prompt pattern, use the template workflow.

## Checkpoint Rules

Stop and ask one concise question only when one of these is true:

- The core subject is missing, such as "帮我生成一张图" with no object, theme, person, product, or text.
- The requested mode materially changes the output and cannot be inferred, such as a phrase that could be either an XHS cover title or a typography poster.
- The user requests image editing but does not specify what must be preserved or changed.
- A portrait request names a real person, private person, or identity-sensitive likeness and the prompt needs consent, source-image, or identity-boundary clarification.
- An advanced image-model-only workflow requires an uploaded source image, but the user has not provided or described the required image.

Proceed without asking when the user gives any usable anchor: title, phrase, product, audience, person type, scene, brand mood, or reference template.

For public figures or celebrity-style portrait requests, default to an "inspired-by mood/style" prompt instead of exact likeness. Do not promise to recreate the person's real face. Ask for a compliant reference image and explicit permission only when the user requests identity-preserving likeness.

## GPT Image Rules

- Write natural-language visual briefs for GPT Image, not Midjourney-style tag soup.
- Make exact visible text short, large, and central when text matters.
- For Chinese text, explicitly request clear, correctly written Chinese characters and avoid dense paragraphs.
- Describe hierarchy and relationships instead of pixel-perfect placement.
- For layout-sensitive images, prefer a simple composition with one main subject and a few supporting details.
- Do not rely on tiny subtitles, microcopy, or complex multi-line typography.
- For image-editing prompts, preserve the source image's required identity, shape, perspective, and material details unless the user asks to change them.
- Suggest output settings when useful: model, size, quality, and format.
- For quick drafts use medium quality; for final XHS covers, posters, and portraits use high quality.
- For image-model-only advanced workflows, include `Image Model Requirement: requires gpt-image-2 or image_generation-capable model`.

## Advanced Workflow Rules

- **Batch variants**: specify the number of images, shared brand/product constraints, and controlled variation axes for each image: scene, angle, palette, composition, copy, props, and mood.
- **Layered posters**: ask for a complete composition plus separate recomposable layers. Each non-background layer should have transparent or no background where supported, preserve exact position/scale, and align without manual repositioning.
- **Image editing and annotation**: lock source-image geometry, subject identity, material, lighting, camera angle, and perspective unless the user explicitly asks to change them.
- **Life milestone posters**: bind every internal symbol to the user's real theme or biography; avoid random fantasy collage, template backgrounds, or unrelated prestige symbols.
- **Fitness infographics**: include "not medical advice" and avoid diagnosis, treatment claims, injury guarantees, or body-shaming language. Use general training guidance and advise professional help for pain, injury, pregnancy, chronic illness, or medical conditions.
- **Palm-reading entertainment**: include "for entertainment only, no scientific basis"; avoid deterministic statements about marriage, lifespan, disease, wealth, or fate. Ask for a palm image without clear fingerprints or other sensitive identity details.

## Failure Modes

| Trigger condition | First-line repair | If still unresolved |
|---|---|---|
| Broad request with no image type, such as "帮我生成一张图" | Run `🔴 CHECKPOINT 1` and show the image type menu | Ask the user to choose one menu item; do not draft a final prompt |
| Selected type lacks a required anchor | Ask the single missing field from `references/intake-guide.md` | Offer one inferred default and ask for confirmation |
| Template mismatch or conflicting template request | Switch to the closest template family and say which composition logic is reused | Ask whether to prioritize the user's subject or the original template structure |
| Public figure or celebrity-style portrait request | Write an inspired-by mood/style prompt and avoid exact likeness claims | Ask for a compliant reference image and explicit permission only if identity-preserving likeness is required |
| Private person or identity-preserving portrait request | Ask for source image/permission and clarify what identity details must be preserved | Produce a generic subject-type prompt instead of identity-preserving output |
| Unreadable text risk | Reduce visible text to the shortest useful phrase, make it large, and request accurate readable characters | Move extra copy into non-visible prompt notes or iteration options |
| Chinese rendering risk | Avoid dense paragraphs, microcopy, complex calligraphy, and multiple text zones; request clear standard Chinese characters | Use fewer Chinese words or switch secondary text to non-visible description |
| Reference image conflict | Preserve identity, geometry, perspective, material, and lighting unless the user asks to alter them | Ask which property wins: source fidelity or requested transformation |
| Overcrowded prompt | Cut secondary props, keep one primary subject, and move optional ideas into iteration notes | Generate a simplified prompt with one focus and one supporting element |
| Generic AI gloss | Specify photographic, print, material, or editorial constraints that make the image art-directed | Switch to the closest template with stronger composition rules |
| Cheap template look | Remove decorative badges, fake UI labels, excessive gradients, stock icons, random sparkles, and Canva-like layout language | Use a restrained editorial, museum, magazine, or product-photography style |
| Image-only overclaim | If no image model/tool is available, provide only the prompt and model requirement | Ask whether to copy the prompt elsewhere or continue refining text |
| Unsafe personalization in fitness, body, palm, or private-person workflows | Add non-medical, entertainment-only, privacy, or consent boundaries | Refuse deterministic medical, biometric, fate, or identity-sensitive claims and offer a safer prompt |

## Size Defaults

- **XHS Cover**: vertical first. Use `1024x1536` for broad compatibility; use `1440x1920` or `2160x2880` for high-detail final assets when supported.
- **Concept Poster**: use `1024x1536` for portrait posters, `1536x1024` for landscape posters, and `1024x1024` for square concept visuals.
- **Portrait Editorial**: use `1024x1536` for half-body or full-body portraits, `1024x1024` for avatar-like portraits, and taller vertical sizes for cinematic full-body images when supported.

## Semantic Rules

Before writing the final prompt, choose a non-cliche visual direction:

- Do not map freedom to blue sky and birds; use dissolving boundaries, loosened structures, expanded space.
- Do not map desire to red fire; use gravity, pull, emptiness, proximity, or irreversible approach.
- Do not map loneliness to one person in a corner; use absence of response, scale imbalance, blank space, or acoustic silence.
- Do not map time to clocks and hourglasses; use afterimages, erosion, repetition, weathering, fading, or irreversibility.

## Anti-Patterns

Avoid these recurring failures:

- Fake Chinese, pseudo-letters, misspellings, unreadable text, or text so small it becomes texture.
- Too many titles, subtitles, stickers, captions, badges, labels, seals, UI chips, or decorative callouts.
- One-note "AI poster" aesthetics: glossy 3D, generic neon, over-saturated gradients, fantasy smoke, random particles, and faceless surrealism.
- Literal cliches: freedom as blue sky, time as clock, desire as fire, loneliness as a person in a corner.
- E-commerce clutter, stock-photo smiles, PPT-cover hierarchy, cheap collage, template-card layouts, and unrelated symbolic props.
- Prompt lists that read like tags instead of a coherent visual brief.

## Template Workflow

Use templates as composition and style skeletons, not rigid fill-in forms.

1. Load `references/template-index.md` to choose the closest template family.
2. Load `references/intake-guide.md` to collect the minimum missing fields for that family.
3. Load only the matching template file:
   - `references/templates-xhs-cover.md`
   - `references/templates-concept-poster.md`
   - `references/templates-epic-narrative-poster.md`
   - `references/templates-product-visual.md`
   - `references/templates-portrait.md`
   - `references/templates-anime-fashion-cover.md`
   - `references/templates-gpt-image-2-advanced.md`
4. Replace placeholders with user-specific content.
5. Rewrite the result as a fluent GPT Image visual brief.
6. Preserve the template's composition logic, but remove details that conflict with the user's subject.
7. Never leave raw placeholders in the final answer.

## Output Format

Return these sections:

```md
## Visual Strategy
[One short paragraph explaining the hook, metaphor, or photographic intent.]

## GPT Image Prompt
[A complete prompt ready to paste into GPT Image.]

## Image Model Requirement
[For advanced image-only workflows only: requires gpt-image-2 or image_generation-capable model. If text-only, this is a prompt to run elsewhere.]

## Variant Plan
[For batch generation only: list each requested variant's scene, angle, palette, composition, and copy direction.]

## Output Settings
- model: gpt-image-2, or Responses API with image_generation tool when execution is requested
- size: [recommended size]
- quality: [medium/high]
- format: [png/webp]

## QA Checklist
- Main subject is clear at first glance.
- Visible text is short, large, and readable when text is required.
- Composition has one primary focus and limited supporting elements.
- Style avoids cheap template aesthetics and generic AI-art gloss.
- For portraits: face, pose, outfit, lighting, and background are coherent.

## Next Step
是否要基于这个提示词调用 image2 / gpt-image-2 直接生成图片？
```

Keep the final prompt in the user's working language unless they ask otherwise.
