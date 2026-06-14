# Product Visual/Edit Templates

Use these templates for product image refinement, product compositing, product replacement, exploded views, product lighting, and industrial design line art. These often require image editing: preserve product identity, geometry, perspective, and material unless the user explicitly asks to change them.

## Shared Variables

- `{product}`: product name or description
- `{source_image}`: source image role if provided, such as image 1 product or image 2 scene
- `{scene}`: target environment or background
- `{material}`: glass, matte plastic, metal, fabric, ceramic, etc.
- `{lighting}`: lighting setup or correction goal
- `{color_temperature}`: warm, neutral, cool, matched to scene, etc.
- `{effect}`: blue/orange light, particles, dynamic lines, glow, etc.
- `{components}`: internal parts or structure to show
- `{negative_constraints}`: user-specific avoid list

## Template: Product Refinement

Use for clean e-commerce-like product retouching or precise product render upgrades.

Prompt skeleton:

```md
Refine the product image of {product}.

Place the product on a clean pure-white background. Accurately preserve the product's shape, color, proportions, branding if intentionally present, and material qualities: {material}. Remove fingerprints, dust, blemishes, scratches, and visual noise. Improve soft, even lighting and realistic shadows so the product looks new, premium, clean, dimensional, and suitable for a high-end product hero image.

Avoid:
Changing the product design, wrong material, warped geometry, fake reflections, dirty background, over-sharpening, watermarks, extra text, and {negative_constraints}.
```

## Template: Exploded Product View

Use when the user wants to show internal parts, electronics, or a technical structure.

Prompt skeleton:

```md
Create a product exploded-view visualization of {product}.

Break the product into precise floating layers and components: {components}. Show internal structure, electronic elements, shell layers, connectors, and functional modules with clear spacing. Use a clean 3D-rendered technical style, high clarity, rich but organized detail, and a premium technology feel.

Preserve:
The product's original identity, proportions, material logic, and functional relationships.

Avoid:
Random impossible parts, messy component spacing, unreadable clutter, wrong scale, cheap sci-fi effects, watermarks, labels unless requested, and {negative_constraints}.
```

## Template: Natural Product Compositing

Use when removing a product's white background or placing it naturally into a scene.

Prompt skeleton:

```md
Naturally composite {product} into {scene}.

Preserve the product's position, shape, proportions, details, and material identity. Remove the original white/background edge if needed. Match perspective, contact shadows, reflections, color temperature, brightness, saturation, and light direction to the target environment. Eliminate visual seams and unrealistic overlap so the product physically belongs in the scene.

Lighting:
{lighting}. Color temperature: {color_temperature}.

Avoid:
Changing product design, floating look, mismatched shadows, pasted-on edges, wrong perspective, inconsistent reflections, excessive blur, watermarks, and {negative_constraints}.
```

## Template: Product Light Effect

Use when adding technical blue/orange inner light, particles, or dynamic energy effects while preserving product detail.

Prompt skeleton:

```md
Enhance {product} with premium technology light effects.

Preserve the original product details, shape, material, and background integrity. Add refined orange and blue dual-color light effects to internal mechanical or electronic areas. Use dynamic light trails, subtle particles, controlled glow, and high-saturation highlights only where they support the product's technology feeling.

Avoid:
Overpowering the product, changing its structure, cheap neon, messy particles, blown-out highlights, fake sci-fi clutter, watermarks, and {negative_constraints}.
```

## Template: Industrial Line Art

Use when converting product imagery into a professional design sketch or line draft.

Prompt skeleton:

```md
Convert {product} into a professional industrial design sketch.

Use clean, accurate black line art to preserve the product outline, structural transitions, connection lines, functional part boundaries, and main volume. Add a few construction lines, auxiliary marks, and light hatching only when they help explain form and space. Keep the image black-and-white, minimal, precise, and hand-drawn in an early product concept sketch style.

Avoid:
Cartoon style, messy scribbles, losing product identity, wrong proportions, dense shading, color, labels unless requested, watermarks, and {negative_constraints}.
```

## Template: Product Replacement

Use when the user provides one image with a product and another image with a target scene.

Prompt skeleton:

```md
Place the product from {source_image} into {scene}.

Keep the product's design, shape, proportions, color, and material unchanged. Reset and match lighting, shadow, perspective, reflections, brightness, saturation, and color temperature so the product is physically integrated into the target scene. Preserve scene background integrity while removing any visible compositing seams.

Avoid:
Changing the product, wrong scale, mismatched perspective, pasted-on look, inconsistent shadows, distorted material, watermarks, and {negative_constraints}.
```
