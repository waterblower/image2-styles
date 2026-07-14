# Generation Formula

Use this prompt structure:

```text
[BASE_STYLE]
[CONTENT]
[LIGHT_COLOR]
[COMPOSITION]
[NEGATIVE]
```

`[BASE_STYLE]` should start with the "Embedded Base Style" line from `shared_style_invariants.md`, then combine the remaining shared invariants with the selected subject and material routes.

`[CONTENT]` should contain the user's requested subject, scene, pose, clothing, object, action, identity, setting, and any story details.

`[LIGHT_COLOR]` should include:

```text
clean wide-gamut color, no dark yellow antique cast, global soft illumination, broad diffused area light, natural bounced light, controlled highlight rolloff, preserved color detail in highlights, low-to-medium contrast, soft atmospheric shadows
```

`[COMPOSITION]` should contain only the requested framing, camera distance, layout, and subject placement.

`[NEGATIVE]` should include `negative_prompt.md` and any user-specific failure items.
