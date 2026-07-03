routes:
  face:
    when: face, headshot, bust portrait, facial expression, makeup, hair, or close character portrait is the main target
    read:
      - shared_style_invariants.md
      - face_base_style.md
      - face.png
      - negative_prompt.md
      - generation_formula.md
  full_body:
    when: full-body character, character design, action character, outfit, body pose, or visible limbs are the main target
    read:
      - shared_style_invariants.md
      - full_body_base_style.md
      - full_body.png
      - negative_prompt.md
      - generation_formula.md
  environment:
    when: empty scene, architecture, interior, exterior, landscape, natural space, or spatial atmosphere is the main target
    read:
      - shared_style_invariants.md
      - environment_base_style.md
      - environment.png
      - negative_prompt.md
      - generation_formula.md
  object:
    when: object, prop, product, vessel, tool, packaging, material study, or close-up item is the main target
    read:
      - shared_style_invariants.md
      - object_base_style.md
      - object.png
      - negative_prompt.md
      - generation_formula.md
  mixed:
    when: people, environment, and objects are all important
    read: only the route files for the subject types that are actually present; do not read every route automatically
