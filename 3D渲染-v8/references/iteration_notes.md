# Iteration notes

```yaml
macro_medium:
  primary_category: pure_3d_render
  confidence: 0.97
  evidence:
    skin: stable SSS and PBR specular response
    hair: strand and grouped-card rendering
    fabric_or_materials: geometric knit, glass, metal, wood, and cloth responses
    lighting_and_shadows: global illumination, contact shadows, environment reflections
    camera_depth_edges: optical depth of field and rendered edge bevels
style_signal_split:
  transferable_invariants:
    - softly idealized Japanese game-CG realism
    - clean tapered shapes and restrained microdetail
    - tactile PBR with diffused highlight rolloff
    - warm neutral palette with dusty pastel accents
  conditional_style_variables:
    - facial SSS and eye proportions
    - grouped hair strands
    - material-specific roughness and refraction
  non_transferable_content:
    - individual characters, clothing, flowers, shops, poster typography
  missing_risk_if_only_pipeline_words:
    - distinctive graceful facial proportions and selective detail frequency
iteration_1:
  scores: {face: 0.86, full_body: 0.84, environment: 0.82, object: 0.83}
  issues: [face too photoreal, body background too empty, environment genre drift, object highlights too glossy]
iteration_2:
  scores: {face: 0.94, full_body: 0.93, environment: 0.92, object: 0.91}
  gates: {macro_medium: pass, style_fingerprint: pass, lighting_quality: pass, full_body_life: pass}
```
