routes:
  face:
    when: face, avatar, bust close-up, facial expression, makeup, or hairstyle is the main target
    read:
      - shared_style_invariants.md
      - face_base_style.md
      - face.png
      - negative_prompt.md
      - generation_formula.md
  full_body:
    when: full-body character, character lineup, action character, outfit, or body pose is the main target
    read:
      - shared_style_invariants.md
      - full_body_base_style.md
      - full_body.png
      - negative_prompt.md
      - generation_formula.md
  environment:
    when: empty scene, architecture, interior, exterior, or spatial atmosphere is the main target
    read:
      - shared_style_invariants.md
      - environment_base_style.md
      - environment.png
      - negative_prompt.md
      - generation_formula.md
  object:
    when: object, prop, product, material close-up, or still life is the main target
    read:
      - shared_style_invariants.md
      - object_base_style.md
      - object.png
      - negative_prompt.md
      - generation_formula.md
  mixed:
    when: people, environment, and objects are all important
    read: Read only the base_style and reference files for the subject types actually present.
