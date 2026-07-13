# Extraction Notes

```yaml
macro_medium:
  primary_category: 2d_3d_hybrid
  confidence: 0.86
  evidence:
    skin: "Porcelain-pale simplified faces with soft volume and low-detail features."
    hair: "Ink-mass hair with fine drawn strands and dry, smoky edges."
    fabric_or_materials: "Translucent paper, vellum, gauze, wrinkles, plant fibers, and layered fibrous veils dominate the surface language."
    lighting_and_shadows: "Soft global overcast illumination, very low contrast, broad milky highlights, muted dusty shadows."
    camera_depth_edges: "Reference images have photographed/sculptural depth, but contours and surface marks are hand-drawn and ink-wash-like."
  forbidden_defaults_if_wrong:
    - anime digital painting
    - glossy pure 3D render
    - realistic photography
style_signal_split:
  transferable_invariants:
    - "Translucent handmade paper and diluted ink-wash material logic."
    - "Pale ivory, ash gray, tea beige, smoke blue-gray, and faint olive-gray palette."
    - "Fiber veins, wrinkles, dry cracks, torn veil edges, and wandering hairline contours."
    - "Soft matte highlights with preserved white detail and broad low-contrast shadows."
  conditional_style_variables:
    - "Porcelain-paper skin only for faces, hands, and visible bodies."
    - "Ink-mass hair only for hair or fur-like subjects."
    - "Papery foliage and mineral surfaces only where those materials appear."
  non_transferable_content:
    - "Ancient costumes, specific tree scene, seated figures, brush-painting action, vertical text, source-image compositions."
  missing_risk_if_only_pipeline_words:
    - "Calling it only 'ink wash' loses the sculptural translucent paper/fiber material."
    - "Calling it only '3D paper art' loses the hand-drawn contour, diluted wash, and low-saturation archaic mood."
```

No live image-generation iteration was run for this folder. The PNG route anchors are copied from the provided references; the reusable style is encoded in the route text files.
