# GPT Image 2 Advanced Workflow Templates

These templates are only for `gpt-image-2` or image-generation-capable workflows. In a text-only environment, use them to produce a ready-to-run prompt and clearly state the model requirement. Do not claim that images, edits, layers, or batches have been generated unless an image model/tool actually ran.

Sources distilled and rewritten from a WeChat article on GPT Image 2 workflows plus OpenAI image-generation guidance. Do not copy source article wording verbatim.

## Shared Variables

- `{source_images}`: required uploaded images, if any
- `{subject}`: product, person, scene, food, palm, or theme
- `{visible_text}`: exact visible title or labels
- `{audience}`: target viewer or platform
- `{style}`: visual style
- `{composition}`: layout and hierarchy
- `{variant_count}`: number of requested outputs
- `{variation_axes}`: scene, angle, palette, props, copy, composition, lighting, or mood differences
- `{preserve}`: source-image details that must not change
- `{constraints}`: safety, privacy, text, brand, and format constraints

## Template: Layered Poster

Use when the user asks for 分层图, layered poster, editable poster, separate layers, or recomposable design assets.

Required input: poster subject or campaign idea; visible text if text matters.

Prompt skeleton:

```md
Create a complete poster for {subject}, then generate separate recomposable layer images for the same composition.

Complete poster:
{composition}. Visible text: "{visible_text}". Style: {style}. The full image should look finished, coherent, and ready for social or campaign use.

Layer output requirement:
Produce separate layers for: background/environment, people or scene elements, main hero object, decorative supporting elements, and text/graphic elements. Each non-background layer should have transparent or no background where supported. Preserve each layer's exact scale, position, perspective, and lighting so the layers can be stacked back into the complete poster without manual repositioning.

Constraints:
Keep text large and readable. Do not shift objects between layers. Do not add unrelated decorative elements. Do not flatten all content into one layer only if layer output is supported by the image tool. {constraints}
```

Output settings: `model: gpt-image-2`, `size: 1024x1536` or campaign-specific ratio, `quality: high`, `format: png`.

Risk constraints: do not promise actual PSD export or guaranteed transparent files unless the runtime supports those outputs.

## Template: Batch Product Variants

Use when the user asks for 批量生图, multiple product posters, XHS seeding variants, ad concepts, or "generate 8 images".

Required input: product photo or product description, platform/audience, number of variants.

Prompt skeleton:

```md
Using {source_images}, create {variant_count} distinct product-promotion image variants for {subject}.

Shared constraints:
Preserve the product's identity, packaging shape, logo placement, color, material, label structure, and perspective unless explicitly changed. Keep a coherent premium product-ad feel for {audience}. Do not invent different packaging or unreadable fake label text.

Variant plan:
Vary these axes: {variation_axes}. Each variant should have a different scene, camera angle, color mood, supporting props, composition, and short ad-copy direction while keeping the same product and brand identity.

For each variant:
1. Define scene and background.
2. Define product placement and angle.
3. Define lighting and color palette.
4. Define one short readable headline or no text if text would reduce quality.
5. Avoid clutter, fake UI stickers, and template-like badges.
```

Output settings: `model: gpt-image-2`, size `1024x1536`, `3:4`, or platform-specific ratio; `quality: high` for final assets.

Risk constraints: require source product image for product-identity preservation; if none is provided, state that the prompt is for concept variants only.

## Template: Life Milestone Narrative Poster

Use for 人生照片, graduation poster, career poster, personal-memory image, biography poster, or portrait-based collectible narrative art.

Required input: portrait or person description, milestone theme, key places/objects/symbols.

Prompt skeleton:

```md
Create a collectible narrative poster for {subject} around this milestone: {visible_text}.

Use a large side-profile silhouette, calm portrait outline, or elegant central figure as the main container. Inside or around the silhouette, build a coherent world of milestone symbols: {composition}. Every symbol must be directly tied to the person's real story, school, work, family, place, identity, or achievement.

Visual direction:
{style}. Use cinematic poster structure, soft atmospheric depth, refined paper or print texture, controlled negative space, and a quiet epic mood. If text is needed, keep it short, readable, and secondary to the portrait narrative.

Constraints:
Avoid random fantasy collage, unrelated prestige symbols, fake school marks, messy detail density, full-face identity changes, and template backgrounds. Preserve the person's identity if a portrait is supplied. {constraints}
```

Output settings: `model: gpt-image-2`, `size: 1024x1536` or `2160x3840`, `quality: high`, `format: png`.

Risk constraints: for private people, use provided images or user-supplied descriptions; avoid implying verified biography beyond user input.

## Template: Personalized Fitness Infographic

Use for personalized yoga, weekly workout chart, training poster, exercise action diagram, or follow-along fitness image.

Required input: fitness goal, training level, constraints, preferred style. Body metrics are optional and should be handled neutrally.

Prompt skeleton:

```md
Create a non-medical personalized fitness infographic for {subject}.

Important disclaimer:
This is general fitness guidance, not medical advice. Stop if there is pain, and consult a qualified professional for injury, pregnancy, chronic illness, or medical concerns.

Content:
Show a clear training plan for {visible_text}. Include illustrated exercise poses or action panels, simple labels, recommended sets/reps/rest ranges, and short form cues. Keep the layout readable enough to follow during training.

Visual direction:
{composition}. Style: {style}. Use clean hierarchy, large title, consistent icons or illustrated figures, enough spacing, and limited color accents.

Constraints:
Avoid diagnosis, treatment promises, body-shaming language, extreme transformations, unsafe exercises, tiny dense text, and medical claims. {constraints}
```

Output settings: `model: gpt-image-2`, landscape `1536x1024` or `16:9`, `quality: high` when labels are important.

Risk constraints: treat body data as context for general difficulty and emphasis, not as a medical assessment.

## Template: Photo Doodle Annotation

Use for food photo annotation, lifestyle photo doodle, hand-drawn labels, recipe notes, ingredient callouts, or story-style markup.

Required input: uploaded photo plus desired annotation tone.

Prompt skeleton:

```md
Edit {source_images} into a warm hand-drawn annotated social image.

Preserve:
{preserve}. Keep the original photo's main subjects, perspective, lighting, color mood, and composition recognizable.

Add annotations:
Use thin hand-drawn outlines, arrows, dotted guide lines, small labels, and short diary-like notes around the objects. Labels should be brief, readable, and emotionally natural. For food, label taste, texture, temperature, ingredients, or cooking steps. For lifestyle objects, label mood, use, memory, or atmosphere.

Visual direction:
{style}. Keep the doodles light and intentional, with enough blank space. Avoid making the image gray, dirty, overdecorated, or cluttered.

Constraints:
Do not cover the main subject. Do not add fake brand marks, watermarks, QR codes, or long paragraphs. {constraints}
```

Output settings: `model: gpt-image-2`, source-image ratio or `1024x1536`, `quality: high` if text labels matter.

Risk constraints: if no source photo is supplied, ask for one or provide a prompt template only.

## Template: Palm Reading Entertainment Diagram

Use only for playful palm-line annotation and social entertainment visuals.

Required input: palm photo without clear fingerprints or sensitive identity details.

Prompt skeleton:

```md
Create a clean palm-line annotation diagram from {source_images}.

Privacy and accuracy boundary:
For entertainment only; palm reading has no scientific basis. Do not make deterministic claims about lifespan, disease, marriage, wealth, fate, or guaranteed personality traits. Use light, playful wording.

Visual direction:
Convert the palm into a simple clean diagram with subtle outline treatment. Mark major palm-line areas with thin lines and readable labels such as life line, wisdom line, and heart line. Add short playful notes in a neutral card-like layout.

Constraints:
Avoid exposing fingerprints in high detail, avoid identity-revealing marks, avoid medical or fate predictions, and do not overstate accuracy. Keep the design minimal, clear, and respectful. {constraints}
```

Output settings: `model: gpt-image-2`, square or portrait, `quality: medium/high`, `format: png`.

Risk constraints: if the image shows sensitive biometric detail, ask for a lower-detail or redacted image instead.
