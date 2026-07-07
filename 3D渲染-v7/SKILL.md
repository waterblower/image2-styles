---
name: high-end-cg-character-style-generator
description: Generate or edit images in a premium pure 3D CG style with soft matte PBR, idealized lifelike anatomy, restrained cinematic lighting, and tactile material rendering. Use when the user asks for a 3D render, CG image, character key art, environment render, object/product render, reference image, preview image, or any image-related output in this style; if the user request is image-related, Codex must call the imagegen skill and actually generate the image, not only return prompts.
---

# High-End CG Character Style Generator

Read `references/router.md` first. Select only the subject routes and material routes needed for the user request.

Combine the selected `*_base_style.md` files with `references/shared_style_invariants.md`, `references/negative_prompt.md`, and `references/generation_formula.md`. Keep user content separate from style rules.

## Mandatory image generation

If the user's request is related to creating, editing, previewing, or rendering an image, use `$imagegen` and call the built-in `image_gen` tool after building the final prompt. Do not stop after returning a positive prompt, negative prompt, style recipe, or generation rules unless the user explicitly asks for "prompt only", "do not generate", or "just give me the prompt".

Treat these as image-related requests: 生成图片, 出图, 渲染, 3D渲染, CG, 概念图, 参考图, 预览图, 海报, 场景, 环境, 角色, 头像, 立绘, 物品, 产品图, and natural-language descriptions meant to become a visual asset.

When image generation is required:
1. Read the required route/reference files.
2. Compose the positive and negative prompt from the formula.
3. Pass the final prompt to `$imagegen` as a `stylized-concept`, `historical-scene`, `product-mockup`, or other suitable imagegen taxonomy case.
4. Call `image_gen` in the same turn.
5. In the final response, show or link the generated image and briefly include the prompt used.

Default lighting and surface policy is mandatory unless the user explicitly asks for glossy, wet, chrome, high-key, hard spotlight, or dramatic rim-lit imagery. Every generated image should use soft global illumination, broad diffused sources, gentle bounced fill, fine tactile texture, and natural roughness. Do not allow oily skin, slick fabric, polished plastic surfaces, mirror-like floors, chrome-like armor, blown highlights, or any unnaturally smooth/glossy finish by default.

Hard rule: unless the user explicitly asks to modify this skill package itself, never write generated images, previews, exports, temporary files, or `outputs/` directories inside this skill folder. When using this skill to generate images, save generated assets outside the skill package, such as a project-level output directory chosen by the user or a sibling workspace directory.
