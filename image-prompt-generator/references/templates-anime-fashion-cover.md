# Anime Character Fashion Cover Templates

Use these templates for anime/pirate-adventure character fan posters, luxury magazine covers, and character replacement prompts. They are designed for a single protagonist and three selectable image styles.

If the user asks for a known franchise or visible masthead such as "ONE PIECE", keep the requested text only when the user explicitly wants that fan-poster context. Otherwise use a generic premium adventure-fashion masthead such as "GRAND LINE", "VOYAGE", or "NEW WORLD".

## Shared Variables

- `{character_name}`: protagonist name or role
- `{franchise_masthead}`: visible magazine masthead, such as ONE PIECE or a generic replacement
- `{style_variant}`: Mediterranean Resort Muse, Intellectual Coastal Palace, or Royal Crimson Empress
- `{character_traits}`: confidence, intellect, queen-like aura, charm, or other personality signals
- `{wardrobe}`: fashion styling, dress, accessories, fabric, and silhouette
- `{setting}`: terrace, palace, balcony, seaside town, flowers, or coast
- `{pose}`: standing, looking toward camera, over-the-shoulder, looking back, model pose
- `{palette}`: color grading
- `{typography}`: masthead, serif/sans layout, editorial blocks, badge elements
- `{negative_constraints}`: user-specific avoid list

## Style Selection

- Choose **Mediterranean Resort Muse** for bright seaside holiday energy, white/gold/ocean-blue palette, elegant summer styling, and confident approachable charm.
- Choose **Intellectual Coastal Palace** for sophisticated beauty, purple/gold/ivory palette, dreamy cliffside architecture, long hair, graceful over-the-shoulder poses, and refined travel-editorial mood.
- Choose **Royal Crimson Empress** for queen-like luxury, crimson/gold/sapphire palette, palace balcony, marble columns, flower petals, powerful feminine charisma, and high-impact fashion cover drama.
- If the user names a character but not a style, infer from requested mood. If still unclear, default to **Mediterranean Resort Muse** for bright commercial appeal.

## Template: Mediterranean Resort Muse

Use for a bright, luxurious seaside vacation cover inspired by high-end fashion magazines.

Prompt skeleton:

```md
Create a vertical luxury anime fashion magazine cover featuring {character_name} as the only protagonist.

Theme and rendering:
Use a pirate-adventure anime fan-poster spirit with ultra-realistic anime character rendering, cinematic luxury atmosphere, high-end editorial photography, polished commercial fashion campaign quality, HDR clarity, and rich detail without clutter.

Setting:
Place the character on a beautiful Mediterranean seaside terrace overlooking an azure ocean. Include a white marble balcony, warm daytime sunlight, sparkling sea reflections, orange trees, an elegant European coastal town in the distance, and a soft ocean breeze feeling.

Character direction:
{character_name} is {pose}, with {character_traits}. Wardrobe: {wardrobe}. Use elegant summer resort styling, refined accessories, dynamic hair strands, natural skin texture, graceful posture, and a sophisticated model-like presence.

Cover design:
Set a large metallic-gold "{franchise_masthead}" masthead across the top. Use premium magazine typography, clean fashion-cover composition, elegant text arrangement, luxury badge elements only if they improve the hierarchy, and a clear editorial layout.

Color and finish:
Palette: white, gold, ocean blue, warm sunlight, and luxury resort neutrals. Keep the image bright, crisp, polished, and premium.

Avoid:
Group shots, chibi style, cheap cosplay look, cluttered props, low-quality anime screenshot look, distorted anatomy, plastic skin, unreadable text, fake logos beyond the requested masthead, watermark, QR code, and {negative_constraints}.
```

Output settings: vertical `9:16`, `1024x1536` or higher, `quality: high`, `format: png`.

## Template: Intellectual Coastal Palace

Use for an elegant, knowing, travel-editorial cover with purple tones and a cliffside palace atmosphere.

Prompt skeleton:

```md
Create a vertical luxury anime fashion magazine cover featuring {character_name} as the only protagonist.

Theme and rendering:
Use a pirate-adventure anime fan-poster spirit with ultra-detailed anime realism, cinematic photography, luxury travel issue cover mood, global illumination, high-end editorial finishing, and rich but controlled depth.

Setting:
Place the character on an elegant Mediterranean cliffside palace terrace. Include blooming purple flowers, sea horizon in the background, luxury coastal architecture, warm afternoon sunlight, dreamy atmosphere, and layered depth.

Character direction:
{character_name} is {pose}, with {character_traits}. Wardrobe: {wardrobe}. Favor sophisticated intellectual beauty, long flowing hair, graceful over-the-shoulder or composed model pose, confident expression, and refined supermodel styling.

Cover design:
Set a premium metallic-gold "{franchise_masthead}" logo at the top. Use luxury serif typography, editorial text blocks, sophisticated cover layout, clean visual hierarchy, and high-end branding design.

Color and finish:
Palette: purple, gold, ivory, and ocean blue. Use realistic skin rendering, luxury fabric texture, cinematic lighting, elegant shadows, and magazine-quality retouching.

Avoid:
Overly dark fantasy mood, cluttered palace details, cheap purple glow, stiff pose, generic AI glamour, distorted anatomy, fake text, watermark, QR code, and {negative_constraints}.
```

Output settings: vertical `9:16`, `1024x1536` or higher, `quality: high`, `format: png`.

## Template: Royal Crimson Empress

Use for a queen-like, ultra-luxury fashion cover with red, gold, palace, and dramatic editorial impact.

Prompt skeleton:

```md
Create a vertical ultra-luxury anime fashion magazine cover featuring {character_name} as the only protagonist.

Theme and rendering:
Use a pirate-adventure anime fan-poster spirit with cinematic editorial photography, masterpiece-level fashion publication design, ultra-detailed anime realism, ray-traced luxury light, HDR clarity, and premium commercial campaign impact.

Setting:
Place the character on a magnificent Mediterranean royal palace balcony overlooking a sparkling sea. Include marble columns, blooming pink flowers, floating flower petals, luxury coastal cityscape, warm golden sunlight, and a dreamy cinematic atmosphere.

Character direction:
{character_name} is {pose}, with {character_traits}. Wardrobe: {wardrobe}. Favor queen-like aura, long flowing hair, looking back toward camera, crimson silk, gold embroidery, royal accessories, elegant earrings, powerful feminine charisma, and an empress-like model pose.

Cover design:
Set a giant metallic-gold "{franchise_masthead}" title in the upper area. Use premium magazine-cover layout, luxury typography, editorial composition, fashion publication design, and clean but impactful hierarchy.

Color and finish:
Palette: rich crimson red, gold, sapphire blue, and sunset tones. Use realistic silk texture, glossy luxury finish, premium skin rendering, dynamic hair movement, cinematic lighting, and rich detail without clutter.

Avoid:
Overcrowded royal symbols, cheap costume look, excessive red glow, fantasy armor unless requested, distorted anatomy, plastic skin, unreadable masthead, watermark, QR code, and {negative_constraints}.
```

Output settings: vertical `9:16`, `1024x1536` or higher, `quality: high`, `format: png`.
