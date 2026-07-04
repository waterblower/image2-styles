---
name: high-end-cg-character-style-generator
description: Generate images in a premium pure 3D CG character-key-art style with soft matte PBR, idealized lifelike anatomy, restrained cinematic lighting, and tactile material rendering.
version: 1.0.0
---

# High-End CG Character Style Generator

Read `references/router.md` first. Select only the subject routes and material routes needed for the user request.

Combine the selected `*_base_style.md` files with `references/shared_style_invariants.md`, `references/negative_prompt.md`, and `references/generation_formula.md`. Keep user content separate from style rules.

Default lighting and surface policy is mandatory unless the user explicitly asks for glossy, wet, chrome, high-key, hard spotlight, or dramatic rim-lit imagery. Every generated image should use soft global illumination, broad diffused sources, gentle bounced fill, fine tactile texture, and natural roughness. Do not allow oily skin, slick fabric, polished plastic surfaces, mirror-like floors, chrome-like armor, blown highlights, or any unnaturally smooth/glossy finish by default.

Never write generated images, previews, exports, or `outputs/` directories inside this skill folder. Save generated assets outside the skill package, such as a project-level output directory chosen by the user or a sibling workspace directory.
