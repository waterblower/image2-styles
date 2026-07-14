# Iteration Notes

## Macro Medium

```yaml
macro_medium:
  primary_category: pure_2d
  confidence: 0.88
  evidence:
    skin: painterly blended planes, visible brush texture, no photographic sensor evidence
    hair: painted masses and strokes, not 3D hair system
    fabric_or_materials: oil-like brush buildup and simplified material response
    lighting_and_shadows: broad soft painted transitions, not ray-traced or camera-captured
    camera_depth_edges: softened painterly edges and canvas texture dominate
  forbidden_defaults_if_wrong:
    - semi-real 2.5D digital painting
    - anime digital painting
    - pure 3D render
```

## Style Signal Split

```yaml
style_signal_split:
  transferable_invariants:
    - classical realist painterly digital oil surface
    - realistic human proportions and anatomy
    - broad soft illumination with controlled highlights
    - clean wide-gamut warm-cool color relationships without dark yellow antique cast
    - restrained background detail and soft edge hierarchy
    - matte to satin skin and low-reflection hair masses
  conditional_style_variables:
    - glass, liquid, ceramic, and metal allow controlled edge highlights only
    - makeup may use local pigment saturation without glitter
    - emissive material may glow softly but must preserve color and avoid white-core bloom
  non_transferable_content:
    - maid outfit
    - specific furniture, room layout, flowers, lamp, framed paintings, curtains
    - exact poses, camera crops, identity, expression, character role
    - stockings, shoes, cleaning prop, specific portrait accessories
  missing_risk_if_only_pipeline_words:
    - would lose low-reflection hair simplification
    - would drift into dark yellow antique oil painting
    - would over-detail backgrounds and ornaments
    - would produce anime, manga, Q-style, or glossy CG faces
```

## Iteration Summary

Iteration 1 established the classical realist oil surface and realistic anatomy, but retained too much old-paint yellowing and some hard bright window patches.

Iteration 2 added clean wide-gamut color, stronger no-antique-cast controls, simplified hair, and stricter low-detail environment rules. The face, full body, environment, and object tests passed the medium, style fingerprint, lighting quality, and body-life gates.

```yaml
best_iteration: iteration2
style_match_score: 0.91
remaining_minor_differences:
  - some warm gray classical atmosphere remains by design
  - reflective materials need route-specific limits to avoid spreading glossy highlights globally
```
