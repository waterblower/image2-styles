# Router

```yaml
subject_routes:
  face: human faces, portraits, busts, facial expressions, hair framing, makeup close-ups
  full_body: full figures, character standees, action poses, clothing silhouettes, visible body weight
  environment: empty spaces, landscapes, interiors, architectural or natural settings, atmospheric backgrounds
  object: props, products, tools, close-up non-human subjects, material-focused still lifes
  mixed: read only the routes actually present in the requested image
material_routes:
  skin: visible skin, faces, hands, bodies
  hair: hair, fine strands, brows, lashes, animal fur analogues
  fabric: clothing, veils, curtains, soft wraps, woven surfaces
  leather: matte treated hide, worn straps, old bindings
  metal: dull metal, jewelry, weapons, fittings
  glass: transparent vessels, lenses, crystal, thin translucent objects
  plastic: synthetic translucent or matte formed surfaces
  wood: branches, furniture, dry carved wood
  stone: rock, carved stone, plaster-like mineral surfaces
  ceramic: porcelain, clay, pale glazed vessels
  paper: rice paper, parchment, scrolls, layered handmade paper
  liquid: ink wash, water stains, thin translucent pooling
  emissive: faint inner glow, spiritual light, dim lantern-like surfaces
  rubber: soft matte synthetic surfaces
  makeup: powder, lip tint, delicate facial pigment
  foliage: leaves, grass, petals, dry plant fiber
```

Routing rules:
- For a face request, read `face_base_style.md`, then add `skin`, `hair`, and `makeup` material files as needed.
- For a full figure, read `full_body_base_style.md`, then add only visible material files such as `fabric`, `skin`, `hair`, `paper`, or `metal`.
- For an empty environment, read `environment_base_style.md`; do not read face or body files.
- For objects, read `object_base_style.md` plus the object's actual materials.
- For mixed scenes, combine only the routes that are visibly needed.
