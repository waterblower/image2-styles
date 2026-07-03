macro_medium:
  primary_category: pure_3d_render
  confidence: 0.94
  evidence:
    skin: soft SSS warmth, polished CG skin planes, controlled pore detail
    hair: strand-based clumps with fine flyaways and soft edge breakup
    materials: PBR roughness separation, translucent fabric/glass/liquid highlights, clean metal accents
    lighting: high-key daylight, low black point, luminous filmic highlight rolloff
    camera: real lens depth of field, near-lens bokeh, crisp foreground with feathered distance

style_signal_split:
  transferable_invariants:
    - stylized high-end 3D render with clean pre-rendered game cutscene finish
    - bright aqua/cyan ambient color system with pale warm neutrals and restrained rose-pink accents
    - low black point, high-key contrast, soft daylight, luminous clear highlights
    - rounded delicate shape language, softened transitions, clean readable large forms
    - crisp focal edges with softly feathered peripheral and background edges
    - controlled micro-detail frequency; polished but not noisy or gritty
    - physically plausible material response with clear roughness and translucency separation
  conditional_style_variables:
    - skin uses soft subsurface scattering and translucent warm blush only for human subjects
    - hair uses strand clumps and fine flyaways only for character routes
    - transparent or wet materials use bead-like refractive sparkle only when such materials are present
    - body routes emphasize volumetric limb construction, weight shift, and clothing pulled by body tension
  non_transferable_content:
    - specific character identity, hairstyle, outfit, pose, beach setting, water splash, and camera composition from the source image

Shared base style:
stylized high-end 3D CG render, clean pre-rendered game cutscene finish, PBR material response, rounded delicate shape language, high-key luminous daylight, low black point, gentle filmic highlight rolloff, airy aqua/cyan ambient palette balanced by pale warm neutrals and restrained rose-pink accents, crisp focal material edges with softly feathered peripheral/background edges, controlled micro-detail frequency, polished surface separation, real camera depth of field and subtle lens bokeh.
