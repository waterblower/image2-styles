subject_routes:
  face:
    when: face, headshot, bust portrait, expression, makeup, hairstyle, or visible facial rendering is the main target
    read:
      - shared_style_invariants.md
      - face_base_style.md
      - face.png
      - negative_prompt.md
      - generation_formula.md
  full_body:
    when: full-body character, character lineup, action pose, outfit design, or visible body posture is the main target
    read:
      - shared_style_invariants.md
      - full_body_base_style.md
      - full_body.png
      - negative_prompt.md
      - generation_formula.md
  environment:
    when: empty scene, building, interior, exterior, garden, landscape, or spatial atmosphere is the main target
    read:
      - shared_style_invariants.md
      - environment_base_style.md
      - environment.png
      - negative_prompt.md
      - generation_formula.md
  object:
    when: object, prop, product, vessel, tool, artifact, or material close-up is the main target
    read:
      - shared_style_invariants.md
      - object_base_style.md
      - object.png
      - negative_prompt.md
      - generation_formula.md
  mixed:
    when: people, environment, and objects are all important
    read: only the subject base styles and references actually present in the requested image
material_routes:
  skin:
    when: skin, face, hands, or visible body surface
    read: [materials/skin_base_style.md, materials/skin.png]
  hair:
    when: hair, fur, eyelashes, brows, or soft fibers
    read: [materials/hair_base_style.md, materials/hair.png]
  fabric:
    when: cloth, garments, lace, curtains, upholstery, or woven soft goods
    read: [materials/fabric_base_style.md, materials/fabric.png]
  leather:
    when: leather, belts, boots, gloves, bags, straps, or waxed hide
    read: [materials/leather_base_style.md, materials/leather.png]
  metal:
    when: jewelry, trim, weapons, hardware, armor, machinery, or metal inlay
    read: [materials/metal_base_style.md, materials/metal.png]
  glass:
    when: glass, crystal, lens, transparent vessel, gemlike refraction
    read: [materials/glass_base_style.md, materials/glass.png]
  plastic:
    when: plastic, resin, coated synthetic shell, polished composite
    read: [materials/plastic_base_style.md, materials/plastic.png]
  wood:
    when: wood, furniture, flooring, tree trunk, carved wooden prop
    read: [materials/wood_base_style.md, materials/wood.png]
  stone:
    when: stone, rock, marble, concrete, brick, plaster, masonry
    read: [materials/stone_base_style.md, materials/stone.png]
  ceramic:
    when: ceramic, porcelain, pottery, glazed vessel, tile
    read: [materials/ceramic_base_style.md, materials/ceramic.png]
  paper:
    when: paper, card, page, label, packaging, scroll
    read: [materials/paper_base_style.md, materials/paper.png]
  liquid:
    when: water, oil, drink, transparent liquid, wet surface
    read: [materials/liquid_base_style.md, materials/liquid.png]
  emissive:
    when: glowing material, neon, magic energy, screen, luminous core
    read: [materials/emissive_base_style.md, materials/emissive.png]
  rubber:
    when: rubber, matte flexible synthetic surface, tire, seal, grip
    read: [materials/rubber_base_style.md, materials/rubber.png]
