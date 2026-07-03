iteration: 1
style_prompt: initial pure 3D render base with PBR, SSS, strand hair, cinematic light, muted warm palette, tactile material separation, shallow depth of field, and editorial CGI finish
negative: 2D illustration, digital painting, painterly brushwork, cel shading, lineart, flat anime rendering, 2.5D look, glossy plastic hair, waxy skin, harsh flash, oversaturated colors
macro_medium: pure_3d_render
tests:
  macro_medium_gate:
    target: pure_3d_render
    candidate_category: pure_3d_render
    pass: true
    reason: candidates retained 3D geometry, PBR materials, lens depth, and contact shadows
  style_fingerprint_gate:
    pass: false
    reason: full-body and environment candidates leaned toward generic character/fantasy and real-estate photographic defaults
  face_closeup:
    style_match_score: 0.88
    pass: false
    missing_or_weak: [more reference-like sculpted facial plane control, lower pore frequency]
    excess_or_wrong: [slightly generic beauty render]
  full_body:
    style_match_score: 0.84
    pass: false
    missing_or_weak: [route needed stronger body-volume and clothing-tension language]
    excess_or_wrong: [too much costume specificity]
  environment:
    style_match_score: 0.82
    pass: false
    missing_or_weak: [stylized CG idealization]
    excess_or_wrong: [photographic location-render feel]
  object_closeup_in_environment:
    style_match_score: 0.89
    pass: false
    missing_or_weak: [stronger selective imperfections and edge wear]
    excess_or_wrong: [slightly clean product default]
overall_pass: false
prompt_update:
  add_to_base:
    - reference-matched semi-realistic CG rather than documentary photography
    - clean sculpted geometry and low-frequency texture with selective imperfections
    - route-specific body volume, spatial material, and object edge-wear language
  remove_from_base:
    - broad generic high-end render phrasing where route-specific detail is needed
  add_to_neg:
    - real-estate photography
    - busy fantasy costume
    - sterile catalog render
stop: false
reason: first round only; several route fingerprints needed tightening

iteration: 2
style_prompt: revised routed pure 3D render base with stronger idealized geometry, route-specific material/detail frequency, warm muted palette, and stylized CG finish
negative: route-trimmed medium exclusions plus repeated defaults such as documentary photo, busy fantasy costume, sterile catalog render, waxy skin, paper-thin body
macro_medium: pure_3d_render
tests:
  macro_medium_gate:
    target: pure_3d_render
    candidate_category: pure_3d_render
    pass: true
    reason: all selected candidates preserve CG geometry, PBR material response, lens depth, and contact shadows
  style_fingerprint_gate:
    pass: true
    reason: selected anchors keep idealized rounded geometry, warm muted palette, controlled detail frequency, edge hierarchy, and editorial CGI finish
  face_closeup:
    style_match_score: 0.93
    pass: true
    missing_or_weak: []
    excess_or_wrong: [slightly more polished skin than source]
  full_body:
    style_match_score: 0.91
    pass: true
    missing_or_weak: []
    excess_or_wrong: [costume still a little decorative, controlled in route prompt]
  environment:
    style_match_score: 0.90
    pass: true
    missing_or_weak: []
    excess_or_wrong: [minor photographic edge, controlled by environment base]
  object_closeup_in_environment:
    style_match_score: 0.94
    pass: true
    missing_or_weak: []
    excess_or_wrong: []
overall_pass: true
stop: true
reason: two rounds completed; four route anchors pass macro medium and style fingerprint gates
