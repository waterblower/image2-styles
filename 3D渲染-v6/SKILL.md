---
name: stylized-3d-render-style
description: Reusable routed style distilled from the provided stylized pure-3D character render references. Use for soft cinematic game-CG style with idealized anatomy, controlled PBR material response, fine hair strands, matte-refined surfaces, and warm muted color grading.
version: 0.1.0
author: Codex
license: MIT
---

# Stylized 3D Render Style

Use this skill by composing:

```text
shared_style_invariants.md
+ reference_prompts/<subject_route>_base_style.md
+ reference_prompts/materials/<material_route>_base_style.md
+ user content request
```

## Router

Choose one subject route:

- `face_closeup_base_style.md`: portraits, busts, face-focused character renders.
- `full_body_base_style.md`: complete character renders and fashion/costume turnarounds.
- `environment_base_style.md`: empty spaces, interiors, exterior sets, scenic backgrounds.
- `object_closeup_base_style.md`: props, weapons, accessories, product-like closeups.

Choose any relevant material routes from `reference_prompts/materials/`:

- `skin_base_style.md`
- `hair_base_style.md`
- `matte_fabric_base_style.md`
- `structured_cloth_base_style.md`
- `leather_base_style.md`
- `black_gloss_material_base_style.md`
- `brushed_gold_base_style.md`
- `aged_metal_base_style.md`
- `embroidered_surface_base_style.md`
- `fur_trim_base_style.md`
- `white_cloth_or_binding_base_style.md`
- `painted_wall_base_style.md`
- `soft_background_base_style.md`
- `hard_surface_prop_base_style.md`
- `fine_line_engraving_base_style.md`
- `lens_and_post_base_style.md`

## Required Lighting

Always include:

```text
soft global illumination, broad area light, large diffused light source, softbox-like key light, bounced fill light, controlled specular rolloff, preserved highlight color detail, low-to-medium contrast, warm muted grade, gentle shadow transitions, no blown-out whites
```

## Output Location

When this skill is used to generate images, do not save newly generated images inside this skill directory. Save outputs only to the user-requested destination, the active project/workspace output path, or a temporary task directory outside `3D渲染-v6/`, this directory.

## Stable Negative

Always include these negative prompts:

```text
overexposed highlights, blown-out whites, oily wet shine, greasy specular reflections, point-light hotspots, sparkle pollution, harsh flash lighting, uncontrolled glossy reflections, glossy plastic hair, wet specular hair, waxy skin, flat 2D anime cel shading, hard vector lineart, noisy photorealistic pores, generic over-polished anime face
```
