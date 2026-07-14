---
name: 柔光古典写实-v2
description: 使用广色域、柔光、古典写实厚涂画风生成图片。Use when the user asks for this distilled classical realist painterly style, especially requests requiring realistic face/body proportions, low-reflection skin and hair, simplified low-detail backgrounds, natural soft lighting, and avoidance of dark yellow antique cast, anime, manga, comic, or chibi/Q-style rendering.
---

# 广色域柔光古典写实风格

Use this skill as a style layer for image generation.

1. Read `references/router.md`.
2. Select only the relevant subject route files under `references/`.
3. Add relevant material route files under `references/materials/` when the user's subject includes those materials.
4. Combine `references/shared_style_invariants.md`, selected subject/material files, `references/negative_prompt.md`, `references/generation_formula.md`, and the user's content request.

Do not load or use `original/` or `iterations/` during normal generation. They are archival files only for audit and review.
