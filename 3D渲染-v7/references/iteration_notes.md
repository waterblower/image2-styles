# Iteration Notes

```yaml
macro_medium:
  primary_category: pure_3d_render
  confidence: 0.92
  evidence:
    skin: physically modeled facial planes, matte SSS, idealized pores and blush gradients
    hair: strand-based groomed clumps with flyaways and anisotropic highlight behavior
    fabric_or_materials: PBR cloth, knit, metal, glass, fur, wood, and ceramic response
    lighting_and_shadows: soft area lighting, bounced fill, shallow depth of field, contact shadows
    camera_depth_edges: optical defocus and render-like edge softness
  forbidden_defaults_if_wrong:
    - semi-real 2.5D digital painting
    - anime digital painting
    - painterly 2D illustration

style_signal_split:
  transferable_invariants:
    - premium pure 3D CG, stylized realism, physically based materials
    - idealized lifelike anatomy, soft facial planes, controlled depth of field
    - matte-to-satin roughness, preserved highlight color, pearly cool shadows
  conditional_style_variables:
    - SSS skin for visible face/body
    - strand-groom hair only when hair/fur is visible
    - textile weave, metal anisotropy, glass refraction, or foliage translucency by material route
  non_transferable_content:
    - specific characters, sweaters, skirts, bouquets, store interiors, poster typography, named-game identity
  missing_risk_if_only_pipeline_words:
    - would lose the soft matte PBR finish, idealized facial proportions, and restrained non-oily highlights

iterations:
  - iteration: 1
    overall_pass: false
    notes: medium matched but drifted too photographic/warm in environment and object tests; some content leakage from references.
  - iteration: 2
    overall_pass: true
    style_match_score: 0.91
    notes: macro medium, matte PBR lighting, anatomy volume, and material response stabilized.
materials:
  generated_independently: true
  count: 16
```
