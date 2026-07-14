# Iteration Notes

```yaml
macro_medium:
  primary_category: pure_2d
  confidence: 0.86
  evidence:
    skin: clean flat anime color planes with softened shadow blocks, no pores or 3D skin shader
    hair: line-defined ribbon locks, painted highlight shapes, no hair-system strands
    fabric_or_materials: leather and metal separated by line weight and painted highlight shapes, not PBR
    lighting_and_shadows: graphic cast shadow and cel-style value blocks
    camera_depth_edges: cropped poster composition without lens blur or camera artifacts
  forbidden_defaults_if_wrong:
    - semi-real 2.5D digital painting
    - anime digital painting
    - painterly 2D illustration
surface_language:
  visible_brushwork: low
  paper_or_canvas_grain: absent
  global_noise_or_speckle: absent
  texture_distribution: none
  texture_evidence_regions: []
  value_transition: softened_blocks
  material_separation: precise
  highlight_design: painted_selective
  likely_failure_if_misread: paper grain, gouache, watercolor, or 3D product-render gloss
style_signal_split:
  transferable_invariants:
    - thick dark contour hierarchy with tapered interior linework
    - smooth broad color fields and graphic cast shadows
    - youthful manga facial simplification and high eye detail
    - warm orange/coral accents against muted teal-gray and dark green
    - selective highlights and precise material separation
    - quiet middle areas with structural detail only
  conditional_style_variables:
    - ribbon-like hair locks and eye catchlights for face routes
    - seam-following folds and dull metal/leather highlights for full-body routes
    - panel, sign, vent, and hinge lines for environment routes
    - folds, clips, printed lines, and contact shadows for object routes
  non_transferable_content:
    - source character identity, orange hair, green eye, newspaper, text, collar, open mouth, crop, clothing
  missing_risk_if_only_pipeline_words:
    - losing graphic shadow placement
    - losing bold line hierarchy
    - adding unwanted paper grain or 3D gloss
iteration_1:
  overall_pass: false
  notes:
    - face was close but too polished and content-contaminated by source colors
    - full_body was too mature and fashion-illustration-like
    - environment and object leaned too realistic and product-rendered
    - no major noise overlay failure, but several material backgrounds showed mild mottling
  prompt_update:
    add_to_base:
      - flat anime cel-painting
      - thick dark outer contour lines
      - bold graphic cast-shadow placement
      - poster-like diagonal crop
      - structural detail only
    remove_from_base:
      - over-polished editorial finish
      - realistic product-render cues
    update_light_color:
      - lower contrast into broad soft area light while keeping cast shadows graphic
    add_to_neg:
      - photorealistic render
      - 3D render volume
      - mature realistic portrait
      - dense accessories
iteration_2:
  overall_pass: true
  tests:
    macro_medium_gate: {pass: true, reason: pure 2D line and cel-plane behavior retained}
    style_fingerprint_gate: {pass: true, reason: bold contour hierarchy, graphic shadows, smooth fields, and selective detail matched}
    surface_language_gate: {pass: true, reason: low visible brushwork and no paper/canvas texture}
    noise_overlay_gate: {pass: true, reason: no uniform grain, speckle, or film noise in main references}
    character_design_gate: {pass: true, reason: youthful simplified anime proportions and large eyes matched}
    material_response_gate: {pass: true, reason: skin, hair, fabric, leather, metal, glass, and paper have distinct highlight widths}
    detail_distribution_gate: {pass: true, reason: detail concentrated at eyes, hair overlaps, seams, signs, panels, and object edges}
    detail_integrity_gate: {pass: true, reason: high-frequency detail serves structure instead of filling transitions}
    lighting_quality_gate: {pass: true, reason: highlights preserved color and avoided oil, sparkle, and hotspots}
    full_body_life_gate: {pass: true, reason: pose has visible weight, limb tension, and clothing response}
  scores:
    face_closeup: 0.93
    full_body: 0.91
    environment: 0.90
    object_closeup_in_environment: 0.90
materials:
  noise_overlay_gate: pass_with_notes
  notes:
    - ceramic and rubber were regenerated after content/text failures
    - fabric, metal, stone, plastic, paper, and rubber show mild background mottling; do not absorb this as a style invariant
    - material texture should be structural and localized, never a global overlay
```
