---
name: stylized-3d-render-style-generator
description: Generate new images in the routed stylized high-end 3D render style distilled from the included references.
---

# Stylized 3D Render Style Generator

Use this skill when the user wants a new image in the included stylized high-end 3D render style.

Before prompting an image model:

1. Read `references/router.md` and choose the route that matches the user's target subject.
2. Read only the route-specific reference image and `*_base_style.md`, plus `shared_style_invariants.md`, `negative_prompt.md`, and `generation_formula.md`.
3. Compose the final prompt as shared style invariants + route base style + user content request + light/color + composition + negative prompt.

Do not merge all route files by default. Environment and object requests should not inherit face, skin, hair, or body-specific language unless the user explicitly asks for a mixed scene containing those subjects.
