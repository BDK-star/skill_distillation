# Template Index

Use this file to select a template family before loading detailed templates. Load only the template file needed for the user's mode.

## XHS Cover

- **Minimal Impact Cover**: strong headline, one visual subject, high contrast, clean negative space. Best for knowledge, mindset, productivity, finance, career, and opinion topics.
- **Emotional Value Cover**: warm or intimate mood, lifestyle subject, soft but readable title. Best for self-growth, relationships, healing, daily life, and personal narrative topics.
- **Knowledge Card Cover**: structured visual hierarchy, readable title, subtle information design. Best for lists, frameworks, tutorials, explanations, and practical guides.
- **Product Seeding Cover**: product as hero, lifestyle context, premium commercial feel. Best for beauty, fashion, food, home, travel, tools, and recommendations.

## Concept Poster

- **Typography Metaphor Poster**: the word or phrase becomes the visual structure. Best for single words, slogans, philosophical concepts, and abstract emotions.
- **Typography Aesthetic Master Poster**: text must dominate the whole image; the type structure, material, aspect ratio, and visual metaphor all adapt to the word. Best for custom typography images and "字体美学" requests.
- **Advanced Concept Poster**: image and text form a visual sentence with minimal graphic-art poster logic. Best for short phrases, social commentary, abstract concepts, and poetic posters.
- **LUMEN ATLAS City Poster**: National Geographic-inspired city atlas editorial poster with cinematic skyline, geographic coordinates, cartographic graphics, poetic city text, and luxury Swiss layout. Best for city/travel posters where only the city name changes.
- **Object Metaphor Poster**: one symbolic object carries the concept. Best for clear ideas that can be expressed through a surprising object relationship.
- **Spatial Tension Poster**: scale, distance, pressure, emptiness, enclosure, or fracture expresses the theme. Best for loneliness, freedom, anxiety, desire, time, conflict, and transformation.

## Epic Narrative Poster

- **Double Exposure Movie Poster**: a large side-profile silhouette filled with story scenes, characters, landmarks, and atmosphere. Best for novels, anime, games, films, and mythic IP posters.
- **Silhouette Worldview Poster**: a large elegant person/object silhouette becomes a container for a complete world view. Best for collectible posters, legendary themes, and poetic story-world visuals.
- **Anime IP Epic Poster**: side-profile or hero outline with internal group narrative, high-density details, dramatic light, and 9:16 poster impact. Best for fan-poster-like IP prompts.

## Product Visual/Edit

- **Product Refinement**: clean white-background product render with corrected material, lighting, and defects.
- **Exploded Product View**: floating layered components and visible internal structure.
- **Natural Product Compositing**: remove or replace background while preserving product geometry and making light/perspective match.
- **Product Light Effect**: add internal blue/orange technical light effects while preserving product details.
- **Industrial Line Art**: convert product to professional black-and-white industrial design sketch.
- **Product Replacement**: place product from one image into another scene with physical perspective and lighting integration.

## Portrait Editorial

- **Magazine Editorial Portrait**: refined fashion/photo direction, controlled styling, strong lighting. Best for polished personal branding, portraits, and fashion.
- **Lifestyle Portrait**: natural daily scene, relaxed pose, believable emotion. Best for social media, personal story, approachable brand images, and soft realism.
- **Cinematic Portrait**: dramatic light, scene-based storytelling, strong mood. Best for narrative portraits, film stills, atmosphere-heavy images, and character concepts.
- **Clear Luminous Portrait**: bright, translucent, airy portrait with low-angle close framing, large clean background, upward body arc, soft skin, minimal clothing, and floating handwritten/editorial text. Best for 清透人像, 明亮写真, 夏日空气感写真, and 晴朗记忆感 portraits.

## Anime Character Fashion Cover

Load `references/templates-anime-fashion-cover.md` when the user asks for 海贼王人物海报, 动漫角色封面, pirate-adventure anime fashion cover, or a luxury magazine cover with a single anime protagonist.

- **Mediterranean Resort Muse**: bright white-gold-ocean-blue luxury resort cover, seaside terrace, marble balcony, orange trees, confident summer styling.
- **Intellectual Coastal Palace**: purple-gold-ivory editorial cover, cliffside palace terrace, purple flowers, sea horizon, over-the-shoulder elegance.
- **Royal Crimson Empress**: crimson-gold-sapphire royal luxury cover, palace balcony, marble columns, flower petals, queen-like charisma.

## GPT Image 2 Advanced Workflows

These templates are image-model-only. Load `references/templates-gpt-image-2-advanced.md` when the request needs `gpt-image-2` or an image_generation-capable model.

- **Layered Poster**: complete poster plus recomposable background, people/scene, hero object, decoration, and text/graphic layers.
- **Batch Product Variants**: multiple product or campaign variants with controlled differences in scene, angle, palette, composition, and copy.
- **Life Milestone Narrative Poster**: portrait-based personal story poster for graduation, career, family, travel, or other milestones.
- **Personalized Fitness Infographic**: non-medical training-plan image with illustrated actions and clear safety boundaries.
- **Photo Doodle Annotation**: uploaded photo preserved with hand-drawn outlines, arrows, labels, and short social-note captions.
- **Palm Reading Entertainment Diagram**: palm-line annotation image for entertainment only, with privacy and non-scientific disclaimers.

## Selection Rules

- If the user provides a reusable prompt template, classify it into the closest family and follow its structure first.
- Before loading the detailed template, use `references/intake-guide.md` to collect only the missing fields for the selected family.
- If the user asks for "替换关键词" or "套模板", keep the original template's composition logic and only adapt conflicting details.
- If no template is requested, choose a family silently and generate the first draft.
- Prefer fewer elements, clearer hierarchy, and stronger subject readability over decorative complexity.
- Use GPT Image 2 Advanced Workflow templates only when the output requires an image model or image editing. In text-only contexts, output a runnable prompt and model requirement instead of claiming images were generated.
