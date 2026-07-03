---
name: idealized-cinematic-3d-style-generator
description: Generate new images in an idealized cinematic 3D / game cutscene render style distilled from the bundled references.
version: 1.0.0
---

# Idealized Cinematic 3D Style Generator

Use this skill to generate new images in the bundled reference style: pure high-end 3D render, idealized game-character proportions, soft cinematic daylight, restrained PBR material detail, shallow camera depth of field, and pastel cream / pale blue / warm rose / muted gold color balance.

Before prompting, read `references/router.md` and choose the relevant subject route. Then read only the matching subject reference, matching subject `*_base_style.md`, any material routes actually present in the requested image, `references/shared_style_invariants.md`, `references/negative_prompt.md`, and `references/generation_formula.md`.

Do not merge every subject and material route into one universal prompt. Keep face, full-body, environment, object, and material handling isolated so skin and hair language does not leak into environment or product prompts.
