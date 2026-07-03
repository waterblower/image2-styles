Use this prompt structure:

```text
[BASE_STYLE]
<shared_style_invariants.md + selected route *_base_style.md>

[CONTENT]
<user subject request; keep this separate from style>

[LIGHT_COLOR]
soft warm directional side light, controlled shadow falloff, low-to-medium saturation, muted warm neutral palette with restrained route-appropriate accents

[COMPOSITION]
<minimal framing needed for the requested subject; keep foreground focus and readable depth>

[NEGATIVE]
<negative_prompt.md, trimmed to the relevant risks for the selected route>
```

Route discipline:

- Face requests read only face route files.
- Full-body requests read only full-body route files.
- Environment requests read only environment route files.
- Object requests read only object route files.
- Mixed requests combine only the route files for subjects that are actually present.
