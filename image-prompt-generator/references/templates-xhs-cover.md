# XHS Cover Templates

Use these templates for 小红书封面, social-media covers, product seeding covers, and knowledge/lifestyle cover images.

## Shared Variables

- `{topic}`: content topic or theme
- `{headline}`: main visible title, usually 4-14 Chinese characters or a very short English phrase
- `{subtitle}`: optional supporting line; omit if it would reduce readability
- `{audience}`: target reader
- `{subject}`: primary visual object, person, product, or metaphor
- `{mood}`: emotional direction
- `{palette}`: color palette
- `{background}`: background scene or surface
- `{style}`: visual style
- `{negative_constraints}`: user-specific avoid list

## Template: Minimal Impact Cover

Use when the cover needs a strong first glance, a large title, and one clear subject.

Prompt skeleton:

```md
Create a vertical Xiaohongshu cover image for the topic "{topic}".

Main visible headline: "{headline}".
Audience: {audience}.

Composition:
Use one dominant visual subject: {subject}. Place it in a simple, high-impact composition with clear negative space around the headline. The headline should be large, readable, and visually dominant. Build a three-level hierarchy: headline first, subject second, small supporting detail third.

Style:
{style}. Use a refined {palette} palette, crisp details, clean edges, and a premium social-media editorial feeling. Background: {background}. Mood: {mood}.

Avoid:
Fake or incorrect Chinese characters, tiny text, dense paragraphs, cheap Canva-like templates, clutter, random stickers, watermarks, logos, QR codes, and {negative_constraints}.
```

## Template: Emotional Value Cover

Use when the cover sells a feeling: healing, self-growth, relationship tension, life advice, comfort, or aspiration.

Prompt skeleton:

```md
Create a vertical Xiaohongshu cover image with a warm editorial lifestyle feeling.

Topic: {topic}.
Main visible headline: "{headline}".
Optional subtitle: "{subtitle}".

Composition:
Use {subject} as the emotional anchor. Keep the scene intimate and uncluttered. The headline is large and readable, integrated into the atmosphere without looking pasted on. Use soft negative space and one memorable visual detail that supports the emotion.

Visual direction:
Mood: {mood}. Palette: {palette}. Background: {background}. Style: {style}. The image should feel personal, polished, and shareable, not like a generic stock image.

Avoid:
Overly sentimental cliches, fake Chinese text, unreadable typography, heavy filters, excessive decorations, watermarks, and {negative_constraints}.
```

## Template: Knowledge Card Cover

Use when the image must package practical information while staying visually clean.

Prompt skeleton:

```md
Create a vertical Xiaohongshu knowledge-card cover.

Topic: {topic}.
Main visible headline: "{headline}".
Audience: {audience}.

Composition:
Make the headline the largest readable element. Use {subject} as the central visual metaphor or icon-like object. Arrange the layout with clean editorial structure, generous spacing, and only a few supporting marks or blocks. Do not include dense body text.

Style:
{style}. Palette: {palette}. Background: {background}. The design should feel trustworthy, modern, and easy to understand at a glance.

Avoid:
Crowded infographic layouts, small unreadable labels, fake interface elements unless requested, cheap template aesthetics, watermarks, and {negative_constraints}.
```

## Template: Product Seeding Cover

Use when a product, place, tool, food, fashion item, or lifestyle object should be the hero.

Prompt skeleton:

```md
Create a vertical Xiaohongshu product-seeding cover.

Topic: {topic}.
Main visible headline: "{headline}".
Hero subject/product: {subject}.

Composition:
Make {subject} the clear hero in a polished lifestyle context. The headline should be large, clean, and readable, with enough contrast from the background. Use a simple supporting scene that makes the product desirable without adding clutter.

Style:
Premium commercial editorial style, {style}. Palette: {palette}. Background: {background}. Mood: {mood}. Use realistic details and appetizing/tactile material quality when relevant.

Avoid:
Fake brand logos, watermarks, QR codes, messy backgrounds, overpacked product collage, unreadable text, cheap e-commerce ad style, and {negative_constraints}.
```
