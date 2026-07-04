# Style Prompt Iteration Record

## Macro Medium

Primary category: `pure_3d_render`

Evidence:

- Skin: smooth SSS-like CG surface, idealized facial planes, controlled pores.
- Hair: strand/fiber grooming with anisotropic grouped highlights.
- Materials: PBR-like fabric, leather, metal, fur, and painted surface response.
- Lighting: broad area-light behavior, controlled specular rolloff, contact shadows.
- Camera/post: shallow depth, clean CG tonal rolloff, pre-rendered game-cinematic finish.

## Round 1 Subject Anchors

Generated independent files:

- `anchor_images/round1_subjects/face_closeup_r1.png`
- `anchor_images/round1_subjects/full_body_r1.png`
- `anchor_images/round1_subjects/environment_r1.png`
- `anchor_images/round1_subjects/object_closeup_r1.png`

Comparison notes:

- Face: medium and lighting matched, but the result risked becoming too photographic/fashion-portrait; revised prompt strengthened stylized CG asset language and reduced pore/fashion finish.
- Full body: safety-safe neutral prompt worked, but the style risked drifting toward polished fashion character art; revised prompt added modest coverage, game asset language, and no runway/fashion wording.
- Environment: successful translation of warm matte surface language; revised prompt clarified low-frequency patina and no character-content transfer.
- Object: successful pure-3D prop read; revised prompt reduced product-ad gloss and chrome-like reflection risk.

## Material Anchors

Generated 16 independent material files:

- `anchor_images/materials/skin_01.png`
- `anchor_images/materials/hair_02.png`
- `anchor_images/materials/matte_fabric_03.png`
- `anchor_images/materials/structured_cloth_04.png`
- `anchor_images/materials/leather_05.png`
- `anchor_images/materials/black_gloss_06.png`
- `anchor_images/materials/brushed_gold_07.png`
- `anchor_images/materials/aged_metal_08.png`
- `anchor_images/materials/embroidered_surface_09.png`
- `anchor_images/materials/fur_trim_10.png`
- `anchor_images/materials/white_cloth_binding_11.png`
- `anchor_images/materials/painted_wall_12.png`
- `anchor_images/materials/soft_background_13.png`
- `anchor_images/materials/hard_surface_prop_14.png`
- `anchor_images/materials/fine_line_engraving_15.png`
- `anchor_images/materials/lens_post_16.png`

Material pass notes:

- Skin, leather, and black gloss were the highest-risk routes for photographic or oily highlight drift.
- Hair needed explicit grouped-fiber language to avoid either flat painted bundles or glossy helmet hair.
- Metal routes needed muted roughness and preserved highlight color to avoid chrome glare.
- Painted wall and soft background translated well with low-frequency texture and warm matte grade.

## Round 2 Final Validation Anchors

Generated independent files:

- `anchor_images/round2_validation/face_closeup_final.png`
- `anchor_images/round2_validation/full_body_final.png`
- `anchor_images/round2_validation/environment_final.png`
- `anchor_images/round2_validation/object_closeup_final.png`

Round 2 revisions:

- Replaced generic `pre-rendered game cinematic character art` emphasis with stronger `game cinematic asset art`.
- Added `less photographic than real portraiture`, `stylized asset finish`, and `no fashion-editorial skin finish`.
- Added stronger specular controls: `broad matte highlights`, `low-intensity metallic highlight rolloff`, `preserved highlight color`.
- Added explicit content boundaries for modest full-body character validation to avoid unsafe or copied costume cues.
- Added `no in-image labels or text` after material/lens prompts revealed that labels can appear if the prompt sounds like a study plate.

## Final Prompt Formula

```text
[BASE_STYLE]
shared_style_invariants.md
+ selected reference_prompts/<subject_route>_base_style.md
+ selected reference_prompts/materials/<material_route>_base_style.md

[CONTENT]
User subject request, written without copying the source characters, costumes, weapons, poses, or exact compositions.

[LIGHT_COLOR]
soft global illumination, broad area light, large diffused light source, softbox-like key light, bounced fill light, controlled specular rolloff, preserved highlight color detail, low-to-medium contrast, warm muted grade, gentle shadow transitions, no blown-out whites

[COMPOSITION]
Use the user's requested framing. Keep clean depth separation, readable silhouette, and low-clutter background unless the user asks otherwise.

[NEGATIVE]
overexposed highlights, blown-out whites, oily wet shine, greasy specular reflections, point-light hotspots, sparkle pollution, harsh flash lighting, uncontrolled glossy reflections, glossy plastic hair, wet specular hair, waxy skin, photographic skin pores, flat 2D anime cel shading, hard vector lineart, generic over-polished anime face, fashion magazine finish, product-ad gloss, in-image labels, text
```
