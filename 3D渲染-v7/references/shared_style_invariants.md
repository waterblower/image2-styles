# Shared Style Invariants

Premium pure 3D CG render, physically based materials, refined game-cinematic character key art, stylized realism rather than documentary photography. The style uses idealized but anatomically grounded forms, softly sculpted planes, feathered silhouette edges, shallow optical depth of field, and restrained post-processing.

Default lighting is soft global illumination only: broad diffused key light, gentle bounced fill, no hard spotlights, no sharp rim lights, no hot pools of light, no blown window light, and no high-exposure bloom unless the user explicitly asks for that look. Mid shots and wide shots must keep the same soft lighting discipline across characters, props, floors, walls, armor, and furniture.

Surfaces should feel tactile and matte-to-satin, with controlled roughness variation and moderate micro-detail. Fine texture is mandatory by default: visible fabric weave, soft skin pores, brushed metal grain, stone mineral variation, wood pores, leather grain, and softened worn edges where appropriate. Skin uses translucent matte SSS; hair uses groomed strand systems with soft clumps and fine flyaways; fabrics show woven structure without noise.

Avoid unnatural smoothness by default. Do not make skin oily, fabric slick, leather patent-glossy, floors mirror-polished, armor chrome-like, stone wet-looking, or object edges plasticky unless the user explicitly requests glossy, wet, chrome, lacquered, or mirror materials. Specular highlights must be broad, dim, color-preserving, and broken by roughness or microtexture.

Avoid 2D linework, cel shading, brush strokes, manga flatness, and hard poster graphics unless the user explicitly asks for typography.

Color is muted and premium: warm skin and wood midtones, cream and pearl highlights, cool desaturated blue-gray shadows, occasional gentle botanical or rose accents. Preserve color detail in highlights.
