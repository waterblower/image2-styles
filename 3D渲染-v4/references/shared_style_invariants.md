stylized high-end 3D render, reference-matched semi-realistic premium CG, PBR material response, clean idealized sculpted geometry, physically plausible light and material behavior, cinematic ray-traced lighting, precise contact shadows, shallow depth of field, crisp foreground forms with softened distant edges, warm muted neutral base palette, restrained rust red, rose, ivory, stone gray, soft green, and subdued gold accents, controlled low-frequency surface texture with selective high-frequency imperfections, tactile material separation, polished game-cinematic and editorial CGI finish, stylized idealization rather than documentary photorealism.

Macro medium:

```yaml
primary_category: pure_3d_render
confidence: 0.94
evidence:
  skin: soft SSS-like skin rolloff, clean sculpted facial planes, controlled pores
  hair: strand-based hair with readable locks and fine flyaways
  fabric_or_materials: PBR ceramic, brushed metal, fabric, leather, water, glass, damp stone
  lighting_and_shadows: ray-traced directional light, contact shadows, controlled specular highlights
  camera_depth_edges: lens DOF, sharp foreground subjects, creamy blurred backgrounds
forbidden_defaults_if_wrong:
  - semi-real 2.5D digital painting
  - anime digital painting
  - painterly 2D illustration
```

Style signal split:

```yaml
transferable_invariants:
  - pure 3D render medium with PBR material response and lens depth of field
  - idealized but believable sculpted forms, rounded silhouettes with crisp contact edges
  - warm muted palette with restrained rose, rust, gold, ivory, gray, and natural green accents
  - foreground clarity, soft background depth, controlled shadow rolloff
  - tactile surfaces with subtle imperfections, never noisy or gritty
  - polished game-cinematic/editorial CGI finish
conditional_style_variables:
  - SSS skin, glossy eyes, lips, pores, and strand hair only for face or character routes
  - body volume, limb construction, and clothing tension only for full-body character routes
  - stone, water, plaster, architecture, and spatial depth only for environment routes
  - ceramic, metal, glass, enamel, fabric, scratches, droplets, and worn edges only for object routes
non_transferable_content:
  - specific people, outfits, haircuts, poses, accessories, weapons, cups, bottles, flowers, locations, and exact compositions
missing_risk_if_only_pipeline_words:
  - generic high-end CG without the warm muted palette, idealized rounded geometry, restrained detail frequency, and editorial depth hierarchy
```
