# Portrait Editorial Templates

Use these templates for 写真, 人像摄影, avatar-like portraits, fashion/lifestyle photos, and cinematic personal images.

## Shared Variables

- `{person}`: subject identity, age range if relevant, features, styling constraints
- `{pose}`: body language and action
- `{expression}`: emotional expression
- `{wardrobe}`: clothing and styling
- `{makeup}`: makeup and hair direction
- `{scene}`: location or background
- `{mood}`: atmosphere
- `{lighting}`: lighting setup
- `{camera}`: lens, shot type, framing, depth of field
- `{palette}`: color grading
- `{text_elements}`: optional handwritten title, signature line, or small editorial notes
- `{aspect_ratio}`: portrait ratio such as 9:10, 4:5, or 1024x1536
- `{negative_constraints}`: user-specific avoid list

## Template: Magazine Editorial Portrait

Use for polished fashion, beauty, profile, or personal-brand portraits.

Prompt skeleton:

```md
Create a realistic magazine editorial portrait.

Subject:
{person}

Pose and expression:
{pose}. Expression: {expression}.

Styling:
Wardrobe: {wardrobe}. Hair and makeup: {makeup}.

Scene and photography:
Scene: {scene}. Lighting: {lighting}. Camera: {camera}. Use refined composition, believable skin texture, coherent facial features, natural hands, and high-end editorial color grading in a {palette} palette.

Mood:
{mood}.

Avoid:
Plastic skin, distorted hands, inconsistent face, over-smoothed beauty filter, fake background, harsh AI gloss, extra text, watermark, logo, and {negative_constraints}.
```

## Template: Lifestyle Portrait

Use for approachable, natural, social-media friendly portraits.

Prompt skeleton:

```md
Create a realistic lifestyle portrait photo.

Subject:
{person}

Scene:
{scene}

Direction:
The subject is {pose}, with {expression}. Clothing: {wardrobe}. Hair and makeup: {makeup}. The image should feel candid but carefully composed, emotionally believable, and not staged like a commercial template.

Photography:
Lighting: {lighting}. Camera: {camera}. Palette: {palette}. Mood: {mood}. Keep the background simple and coherent with the subject.

Avoid:
Fake candid poses, distorted hands, waxy skin, overdone filters, crowded background, extra text, watermark, and {negative_constraints}.
```

## Template: Clear Luminous Portrait

Use for 清透人像, 明亮写真, 夏日空气感人像, 轻快通风感写真, or magazine-like portraits with a clean bright background and floating handwritten layout elements.

Prompt skeleton:

```md
Create a bright, translucent, airy portrait photo for {person}.

Composition:
Frame the subject entering from the lower part of the image, shot from a close, low camera angle looking upward. The body and arms form a soft upward arc. The hands are above or near the face, gently shielding strong light. The gaze turns upward into open blank space, creating a fresh, light, summer-air relationship between the person and the light source.

Background:
The background is the dominant visual field and occupies a large area of the image. Keep it high-key, clean, breathable, lightly ventilated, and almost structural in its simplicity. Use a bright clean base color extracted from the theme, season, material, or emotion. Add only subtle film grain or tiny gel-like particles at the edges. Do not use heavy shadows, dirty filters, or a crowded scene.

Subject styling:
Wardrobe: {wardrobe}. Hair and makeup: {makeup}. Keep clothing and skin soft and natural. Use darker accents only in small clear areas such as hair, eyes, or minimal information layers. The person should feel real, with translucent skin, natural hands, simple styling, and a soft but not blurry photo texture.

Light and color:
Lighting: {lighting}. Use strong but gentle bright light, as if sunlight is opening the image. Keep high brightness, low muddiness, breathable tonal steps, soft edges, and a light emotional temperature. Palette: {palette}. The overall feeling is clear, clean, quick, fresh, and emotionally light.

Editorial handwriting:
Reserve blank space near the top or edges for {text_elements}. The handwritten title or signature line should be thin, elongated, slightly tilted, and lightly flying, as if blown open by sunlight. Small text can sit near the edge in compact magazine-like rows, creating editorial rhythm without crowding the portrait.

Camera and format:
Camera: {camera}. Aspect ratio: {aspect_ratio}. Use realistic portrait photography, soft fine detail, natural facial structure, coherent anatomy, and a crisp overall image.

Avoid:
Heavy contrast, old-photo filters, low-key shadows, greasy skin, plastic beauty retouching, muddy color grading, overexposed face loss, distorted hands, crowded background, thick typography, fake Chinese, watermark, logo, and {negative_constraints}.
```

## Template: Cinematic Portrait

Use for dramatic mood portraits, film-still looks, and story-driven character images.

Prompt skeleton:

```md
Create a realistic cinematic portrait.

Character:
{person}

Scene and story:
{scene}. The subject is {pose}, with {expression}. The image should imply a story through posture, light, and environment rather than added text.

Photography:
Lighting: {lighting}. Camera: {camera}. Wardrobe: {wardrobe}. Hair and makeup: {makeup}. Palette: {palette}. Mood: {mood}. Use cinematic realism, coherent shadows, believable texture, and strong atmosphere.

Avoid:
Overly theatrical costume unless requested, fantasy excess, distorted anatomy, plastic skin, fake bokeh, inconsistent lighting, watermark, and {negative_constraints}.
```
