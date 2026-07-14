---
name: 3D渲染-v8
description: Generate images in a soft idealized Japanese game cinematic 3D style with refined character anatomy, tactile PBR materials, and diffused natural light.
---

# Soft Idealized Game CG Style Generator

Read `references/router.md`. Select only the subject and material routes required by the request, then combine those files with `references/shared_style_invariants.md`, `references/negative_prompt.md`, `references/generation_formula.md`, and the user's content.

## Output handling

- Keep generated images in the conversation by default; do not save them to the project or any other local directory.
- Save an image only when the user or the established task context explicitly requests a file output. Use the explicitly requested destination, or ask for one if none is specified.
- Never write generated images into this skill's directory, including `3D渲染-v8/` and all of its subdirectories.
