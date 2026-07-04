# Generation Formula

```text
[BASE_STYLE]
[CONTENT]
[LIGHT_COLOR]
[COMPOSITION]
[NEGATIVE]
```

`[BASE_STYLE]` should contain the selected shared, subject, and material style rules. `[CONTENT]` contains only the requested subject. `[LIGHT_COLOR]` must include soft global illumination, large diffused area light, bounced fill, controlled specular rolloff, and preserved highlight color detail.

`[LIGHT_COLOR]` must also state that this is the default lighting unless the user explicitly requests otherwise: no hard spotlights, no sharp rim lights, no high-key overexposure, no bloom, no glossy glare, and no mirror-like reflections. For medium shots and wide shots, apply this to the entire scene, including skin, clothing, props, armor, floors, walls, furniture, and background practical lights.

`[BASE_STYLE]` or `[COMPOSITION]` must include fine tactile texture by default: matte-to-satin roughness, visible but restrained microtexture, and broad dim highlights broken by surface grain. Do not rely only on the negative prompt to prevent oily or polished results.
