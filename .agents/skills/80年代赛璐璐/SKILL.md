---
name: 80年代赛璐璐
description: 80年代赛璐璐风格
---

# 80年代赛璐璐

使用此技能生成或编辑图片时，必须使用本技能目录下 `sources/` 文件夹中的图片作为美术风格参考。

硬性规则：每次生成新图片时，都必须把 `sources/` 文件夹中的参考图作为图片输入传入生成工具。不能只在提示词中描述风格，也不能省略参考图输入。

## 风格来源

- 主要参考图：`sources/1.png`
- 只迁移美术风格，不照搬参考图中的具体人物、构图、文字、标志或可识别内容。
- 参考图中的人物发色、瞳色、服装配色不属于必须迁移的风格要素。生成角色时必须根据用户主体设定或角色身份选择发色，不能因为参考图而默认使用蓝色、紫色、蓝紫色或深蓝发。
- 如果用户另有主体、场景或构图要求，以用户要求为内容核心，以 `sources/` 图片为风格核心。

## 生成要求

调用图片生成工具时，必须把 `sources/1.png` 作为参考图传入，并在提示词中明确要求：

- 1980s Japanese cel animation look
- hand-painted cel shading
- clean ink outlines
- slightly soft analog film grain
- clean simplified hand-painted animation background
- limited but expressive vintage color palette
- gentle bloom and practical anime lighting
- authentic retro frame composition
- flat 2D cel character drawing, like a photographed animation cel
- hard-edged two-tone shadow blocks, no soft volume rendering
- prohibit mottled, stained, speckled, cracked, noisy, or over-detailed background texture
- background mountains, cliffs, roads, dirt paths, walls, floors, and rocks must be simplified into broad clean painted planes, with no repeated pattern detail, no repeated cracks, no pebble fields, and no stacked fake texture
- do not copy the reference character hair color; choose hair color from the requested character design, and avoid default blue, purple, blue-black, or blue-violet hair unless the user explicitly asks for it
- strictly avoid 3D render, CGI, sculpted anatomy, glossy shader highlights, airbrushed gradients, and photographic chiaroscuro
- avoid Miyazaki / Studio Ghibli face design, rounded childlike features, soft pastoral character design, and watercolor storybook warmth

## 参考图 1 的画面语法

`sources/1.png` 的核心不是普通“复古日漫”或“精致风景插画”，而是 80 年代赛璐璐动画帧的画面语法。生成时必须优先迁移以下特征：

- 角色脸部、眼睛、鼻影、下颌和头发块面应带有 80 年代动画造型：轮廓明确，表情集中，五官清晰，不使用现代日漫的柔软萌系脸或过度精修脸。
- 角色头发的“块面画法”和“硬边阴影”可以参考 `sources/1.png`，但发色不能照搬参考图。除非用户明确要求蓝发、紫发或蓝紫发，否则应优先使用与角色设定匹配的黑发、棕发、银灰、金发、红棕、白发等不同发色。
- 必须避免宫崎骏/吉卜力式人脸画风：不要圆润幼态脸、圆鼻头、柔软小嘴、温和田园感表情、故事书式水彩暖调或朴素可爱儿童造型。即使主体是儿童，也应保持参考图所示的更锋利、更清晰、更赛璐璐动画帧式的五官结构、鼻影、眼形和下颌线。
- 线条应更粗、更黑、更果断，具有手绘墨线感；避免过细、过淡、过平滑的现代插画线稿。
- 阴影应是大块、清楚分层的赛璐璐平涂阴影，尤其是脸部鼻影、颈部、头发内侧和衣领下方；避免柔焦渐变、复杂反光和照片式明暗。
- 角色身体必须保持二维赛璐璐绘制感。即使主体是肌肉壮汉、巨人或怪兽，也只能用少量硬边阴影块表现体积，不能出现雕塑般的肌肉建模、照片式胸肌高光、油亮皮肤、连续渐变明暗或 3D 模型渲染感。
- 肌肉、皮革、金属、鳞片等材质只能做动画式概括：粗线轮廓 + 一到两层平涂阴影 + 少量必要高光。禁止用密集刮痕、过多反光点、皮肤纹理、金属镜面反射或复杂微细节来增加真实感。
- 色彩应偏低饱和、偏冷或旧胶片色调，允许青灰、暗蓝、土橙、米白等复古配色；避免金色夕阳电影光、现代高饱和蓝绿水面、霓虹感和过甜的暖色滤镜。
- 背景应服务于角色，保持简化、概括、手绘动画背景感；远景和中景不应有过密的建筑、水波、树叶、石块或透视细节。
- 背景必须干净、平整、低纹理，使用大块概括色面和少量必要边线；禁止斑驳墙面、污渍、霉点、裂痕、密集刷痕、颗粒堆叠、随机噪点和做旧脏污感。
- 任何背景细节都必须被压缩为动画场景所需的简洁信息；禁止通过小石块、小树叶、小水波、小窗格、小砖缝、小刮痕或高频纹理制造“丰富感”。
- 山体、悬崖、峡谷、土路、石路、荒地、河岸和城墙是最容易失控的背景，必须额外简化：只允许大块轮廓、少量结构线和一到两层平涂阴影；禁止成片重复裂缝、重复碎石、重复草点、重复刷痕、重复岩面斑块或 pattern 堆砌式伪细节。
- 路面和山体不能画成铺满小石头、小裂纹、小斑点的材质样本；它们应像动画背景里的概括色面，而不是现代风景插画或游戏场景贴图。
- 画面应像单帧动画截图，而不是现代精致复古插画、风景明信片、电影概念图或新海诚式高光背景。

避免现代数码插画感、3D 渲染感、过度光滑的矢量质感、厚涂游戏原画质感、现代高饱和霓虹渐变、现代精致复古插画感、新海诚式背景、高细节风景插画、强夕阳电影光、复杂水面反光、背景透视细节抢戏、背景斑驳做旧、污损纹理、密集假细节、宫崎骏/吉卜力式人脸和田园故事书氛围。

## 反 3D 与反现代精修硬性规则

只要结果出现以下任一特征，即判定为不符合本技能，必须重生或修改提示词：

- 角色看起来像 3D 模型、CGI、游戏角色渲染、雕塑、手办、可动人偶或现代厚涂概念图。
- 肌肉、脸部、皮革、金属或怪兽皮肤出现连续渐变体积、油亮高光、复杂反射、环境光遮蔽、皮肤毛孔或摄影棚式打光。
- 画面依靠透视压迫、镜头畸变、电影级景深、体积光或照片式明暗来制造真实感。
- 背景比角色更精细，或出现大量砖缝、石块、裂痕、旗帜纤维、观众细节、树叶、水波、云层纹理等高频信息。
- 山、路、岩壁、地面或远景出现重复 pattern 堆砌的伪细节，例如连续相似的裂纹、碎石点、岩面斑块、草点、刷痕或噪点纹理。
- 角色发色明显继承了参考图人物的蓝色、紫色、蓝紫色或深蓝发倾向，而用户并未要求这种发色。
- 复古感来自噪点、脏污、刮痕、斑驳、泛黄滤镜或过量颗粒，而不是来自线条、色彩、构图和赛璐璐分层阴影。

生成提示词中应优先使用以下正向约束：

- flat 2D cel animation drawing
- photographed animation cel over a simplified painted background
- bold hand-inked outlines
- large flat color shapes
- hard-edged two-tone cel shadows
- minimal highlights
- simplified low-detail animation background
- broad clean painted background planes for mountains, cliffs, roads, walls, floors, and distant scenery
- character hair color independent from the reference image, chosen by character design

生成提示词中必须加入以下负向约束：

- no 3D render
- no CGI
- no sculpted anatomy
- no glossy shader highlights
- no smooth gradient volume shading
- no photographic lighting
- no airbrushed rendering
- no modern polished retro illustration
- no dense background texture
- no high-frequency fake detail
- no repeated pattern detail on mountains, roads, cliffs, rocks, walls, floors, or distant scenery
- no copied blue, purple, blue-black, or blue-violet hair color from the reference image unless requested

对于“壮汉、巨人、怪兽、铠甲、武器、室内建筑”等最容易生成 3D 感的主体，必须额外强调：

- 体积只通过 1 到 2 层硬边赛璐璐阴影表达。
- 不使用真实材质渲染，不使用连续明暗过渡。
- 高光必须少、硬、平，不能像塑料、金属 shader 或油亮皮肤。
- 背景必须比主体更概括，不能用细碎纹理填满画面。

## 质感控制

- 胶片颗粒只能非常轻微，不能形成明显噪点、脏污感或数字压缩感。
- 路面、墙面、河岸、天空等大面积区域应使用干净、概括、稳定的手绘色块，只保留少量服务结构和光影的边缘变化。
- 山体、悬崖、峡谷、土路、石路、荒地和岩壁也属于大面积背景区域，应和天空、墙面一样被概括处理，不能因为是自然或战斗场景就填满碎石、裂纹、岩面斑点或重复刷痕。
- 禁止用重复的小石块、小裂纹、小斑点、小笔刷纹理、污渍、霉点或破损边缘制造“伪细节”。
- 禁止路面、墙面、水面、天空和远景出现机械重复的简单形状、随机噪点堆叠、过密碎纹或斑驳做旧感。
- 禁止把山、路、岩壁、地面画成可见的 pattern 贴图；一旦出现整片重复的裂缝、碎石、草点、岩面斑块或笔刷纹理，即判定为背景过度复杂。
- 背景细节应服从画面层次：远景更简化，中景适量，主体附近才保留清晰线条。
- 如果需要复古质感，优先使用柔和色偏、轻微晕光、干净的手绘边缘和赛璐璐分层阴影，而不是强噪点、斑驳纹理或脏污做旧。
- 如果场景包含城市、河流、街道、树林或建筑，必须压低背景信息密度，避免背景比角色更精修、更明亮或更吸引视线。
- 角色与背景的关系应接近赛璐璐角色叠在手绘背景上的动画帧：角色线条更清楚，背景边缘更概括，层次明确。

## 输出原则

最终图像应看起来像 80 年代赛璐璐动画的一帧：线条清晰，阴影分层明确，色彩复古，背景干净、概括、低纹理，整体带有轻微胶片年代感，但画面应平整、有层次，不依赖噪点、斑驳纹理、污损做旧或重复纹理制造细节。

如果生成结果看起来像“现代精致复古插画”“风景插画”“电影感日系背景图”“角色很小的旅游场景图”“斑驳做旧背景图”“高频细节背景图”“3D/CGI 角色渲染”“雕塑感肌肉角色”“游戏原画”“厚涂概念图”“塑料或金属 shader 质感”或“宫崎骏/吉卜力式圆润儿童脸”，即使有复古滤镜，也判定为不符合本技能风格。

交付前自检：

- 角色是否明显是二维手绘赛璐璐线稿，而不是 3D 体块？
- 阴影是否主要是硬边平涂块，而不是连续渐变？
- 背景是否足够干净、概括、低纹理，并且不抢角色？
- 山、路、岩壁、地面是否避免了重复 pattern、碎石堆砌、裂纹堆砌和伪细节？
- 人物发色是否来自角色设定，而不是无意识继承参考图的蓝色、紫色或蓝紫色头发？
- 复古感是否来自造型、线条、色彩和动画帧构图，而不是噪点和脏污？
- 如果把画面看作动画截图，是否比“现代复古插画”更像真实 80 年代赛璐璐动画帧？
