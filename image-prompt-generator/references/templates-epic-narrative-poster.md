# Epic Narrative Poster Templates

Use these templates for 双重曝光海报, 人物剪影海报, 小说/动漫/IP 史诗海报, film-poster-like narrative visuals, and collectible story-world posters.

## Shared Variables

- `{theme}`: IP, novel, film, game, mythology, character, or story world
- `{outline_subject}`: large silhouette subject, usually a side-profile person or symbolic object
- `{expression}`: expression or emotional state of the silhouette subject
- `{inner_world}`: story scenes, places, architecture, objects, symbols, creatures, or history inside the silhouette
- `{key_characters}`: important characters or relationships
- `{landmarks}`: iconic locations, objects, or world-building symbols
- `{foreground_subject}`: optional small figure, back view, or focal object that adds scale
- `{palette}`: unified color palette
- `{mood}`: epic, tragic, restrained, sacred, lonely, nostalgic, heroic, etc.
- `{style}`: visual style
- `{title_text}`: optional short visible title
- `{negative_constraints}`: user-specific avoid list

## Template: Double Exposure Movie Poster

Use when the prompt asks for a high-completion epic poster with a large side-profile silhouette containing a story world.

Prompt skeleton:

```md
Create a high-completion epic art poster for "{theme}".

Composition:
Use a large side-profile silhouette of {outline_subject} as the dominant outer contour, occupying the main visual area. The subject's expression is {expression}. Inside the silhouette, build a double-exposure story world containing {inner_world}, including key characters {key_characters} and iconic landmarks/symbols {landmarks}. Add {foreground_subject} as a small scale cue only if it strengthens the story.

Layering:
The composition should have clear foreground, middle ground, and background depth. The silhouette is the main container; the internal world should feel organically grown from the theme, not pasted together.

Style:
{style}. Blend cinematic anime poster design, watercolor and ink wash diffusion, soft atmospheric perspective, print grain, paper texture, and dissolved edges. Use a unified {palette} palette. Mood: {mood}. Large areas of negative space, restrained premium layout, collectible film-poster quality.

Optional text:
If visible title is needed, use "{title_text}" in a small, clean, elegant layout that does not damage the main composition.

Avoid:
Messy collage, unrelated fantasy assets, template-like background, cheap game-poster clutter, low-level glow, inaccurate character identity, overcrowded internal scenes, watermarks, logos, fake text, and {negative_constraints}.
```

## Template: Silhouette Worldview Poster

Use when the image should feel quieter, poetic, legendary, and world-building-focused.

Prompt skeleton:

```md
Create a collectible epic narrative poster for "{theme}".

Main visual:
Use a huge elegant silhouette of {outline_subject} as the outer outline. Inside the silhouette, automatically grow the most theme-bound world view: {inner_world}. Include iconic scenes, character relationships, symbolic objects, architecture, creatures, props, atmosphere, and cultural markers that make "{theme}" recognizable at first glance.

Art direction:
This should not be an ordinary collage. It should be a refined silhouette-filled narrative composition with double-exposure associations, closer to a cinematic poster fused with dreamlike watercolor illustration. Use soft air perspective, misty transitions, paper grain, dry-brush edges, large negative space, and restrained premium poster layout.

Tone:
Palette: {palette}. Mood: {mood}. Style: {style}. The image should feel quiet, grand, sacred, nostalgic, poetic, and legendary.

Optional signature:
If requested, add a small elegant signature-like mark near a lower corner or near the title. It must be subtle, clear, and integrated like a collector's poster signature, never large or cheap.

Avoid:
Hard collage seams, unrelated elements, cheap fantasy material, generic background, noisy composition, overbright effects, fake characters, watermarks, and {negative_constraints}.
```

## Template: Anime IP Epic Poster

Use when the user provides an anime, game, film, or novel IP and wants a powerful 9:16 epic poster.

Prompt skeleton:

```md
Create a double-exposure high-aesthetic anime epic poster for "{theme}".

Composition:
Use a huge side-profile character outline as the main visual carrier. The character looks calm, determined, tragic, and awakened. Inside the outline, unfold a vast fantasy world entirely sourced from "{theme}", including {inner_world}, key characters {key_characters}, and iconic visual symbols {landmarks}. Place the key characters in the middle area with group-narrative tension, heroic poses, and strong gaze rhythm.

Visual quality:
Blend Japanese anime illustration, cinematic concept poster, game key visual design, ink wash diffusion, and digital painting texture. Emphasize detailed layering, light penetration, smoke flow, fragments, energy trails, warm-cold contrast, spatial depth, sacred darkness, and emotional storytelling.

Style and format:
Palette: {palette}. Mood: {mood}. Poster should feel collectible, cinematic, beautiful, tragic, burning, epic, ultra-detailed, complete, and high-resolution. Aspect ratio: 9:16.

Avoid:
Inaccurate character identities, random unrelated IP elements, crowded unreadable composition, cheap fantasy poster style, excessive effects, fake text, watermarks, and {negative_constraints}.
```
