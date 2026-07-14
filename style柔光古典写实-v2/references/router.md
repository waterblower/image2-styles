# Router

Normal generation uses only files inside this style package. Do not read `original/` or `iterations/`; those folders are archival only.

## Global Base Style

- Always read `shared_style_invariants.md` first.
- Keep the "Embedded Base Style" line from `shared_style_invariants.md` as the first style line in `[BASE_STYLE]`.
- Treat the remaining shared invariants, subject route files, and material route files as refinements of that embedded base style, not replacements for it.

## Subject Routes

```yaml
subject_routes:
  face: 人脸、头像、半身特写、面部表情、妆容、发型
  full_body: 人物全身、角色立绘、动作人物、服装造型
  environment: 无人场景、建筑、室内、室外、空间氛围
  object: 物品、道具、产品、材质近景
  mixed: 只读取实际涉及主体类型，不默认全读
```

Routing rules:

- Face requests: read `shared_style_invariants.md`, `face_base_style.md`, relevant material files such as `skin`, `hair`, `makeup`, and `negative_prompt.md`.
- Full-body requests: read `shared_style_invariants.md`, `full_body_base_style.md`, relevant material files such as `skin`, `hair`, `fabric`, `leather`, and `negative_prompt.md`.
- Environment requests: read `shared_style_invariants.md`, `environment_base_style.md`, relevant non-character material files, and `negative_prompt.md`.
- Object requests: read `shared_style_invariants.md`, `object_base_style.md`, relevant material files, and `negative_prompt.md`.
- Mixed requests: read only the actually involved subject route files. Do not default to all subject files.

## Material Routes

```yaml
material_routes:
  skin: 皮肤、面部、手部、可见肌肤
  hair: 头发、毛发、绒毛、动物毛
  fabric: 布料、服装、织物、窗帘、软装
  leather: 皮革、漆皮、皮带、皮包、皮质服装
  metal: 金属、首饰、盔甲、机械、刀剑、五金
  glass: 玻璃、水晶、镜片、透明容器、透明折射宝石
  plastic: 塑料、树脂、涂层、合成材料
  wood: 木头、木家具、木地板、树干、木制道具
  stone: 石头、岩壁、雕塑、混凝土、砖石
  ceramic: 陶瓷、瓷器、釉面器皿、瓷砖
  paper: 纸张、书页、卡纸、包装、卷轴
  liquid: 水、油、饮料、透明液体、湿润表面
  emissive: 发光材质、霓虹、能量、屏幕、魔法辉光
  rubber: 橡胶、哑光软质合成表面、轮胎、密封件
  makeup: 妆容、眼影、唇釉、腮红、粉质/膏状彩妆
  foliage: 叶片、草、苔藓、植物纤维、自然植被纹理
```

Material routing:

- Read each selected `references/materials/<material>_base_style.md`.
- The paired `references/materials/<material>.png` is a visual anchor for that material only.
- Do not use material images as global color palettes when they conflict with the user's content.
- For reflective materials, keep highlights broad and color-preserving; they must not loosen the global no-oily/no-overexposed rule.
