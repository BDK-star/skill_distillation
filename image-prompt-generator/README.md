# Image Prompt Generator

`image-prompt-generator` 是一个交互式图片提示词生成技能，用来把用户的图片想法整理成可直接用于 GPT Image / image2 / `gpt-image-2` 的高质量视觉提示词。

它不是简单堆关键词，而是先判断图片类型，按模板收集关键输入，再输出完整的视觉策略、提示词、生成设置和质量检查清单。

## 适合生成的图片类型

- **XHS Cover**：小红书封面、种草图、知识卡封面、情绪价值封面。
- **Concept Poster**：概念海报、字体美学、视觉隐喻、艺术海报。
- **City Atlas Poster**：国家地理风城市海报、LUMEN ATLAS、旅行编辑海报。
- **Epic Narrative Poster**：双重曝光、人物剪影、小说/IP/动漫史诗叙事海报。
- **Portrait Editorial**：写真、人像、清透人像、个人品牌照、明亮夏日感人像。
- **Anime Character Fashion Cover**：动漫角色奢华杂志封面，支持海贼王人物海报风格。
- **Product Visual/Edit**：产品精修、换背景、结构图、合成、工业线稿。
- **GPT Image 2 Advanced Workflows**：分层图、批量生图、人生叙事海报、健身训练图、照片手绘标注、手相娱乐图解。

## 工作流程

1. **图片类型选择**：如果用户请求很宽泛，先展示可生成的图片类型菜单。
2. **模板化信息收集**：根据用户选择的类型，只询问最少必要信息。
3. **提示词生成与确认**：输出可复制的 GPT Image prompt，并询问是否需要调整风格、文字、构图、比例或负面约束。
4. **Image2 生成询问**：提示词确认后，询问是否要调用 image2 / `gpt-image-2` 直接生成图片。

如果当前环境没有 image 模型工具，技能只输出可复制的提示词，不会声称已经完成图片生成、编辑、分层或批量产出。

## 输出格式

默认输出包含：

- `Visual Strategy`：视觉策略和核心创意。
- `GPT Image Prompt`：可直接复制到 GPT Image 的完整提示词。
- `Image Model Requirement`：仅在 image-only 工作流中出现，说明需要 `gpt-image-2` 或 image-generation-capable model。
- `Variant Plan`：仅在批量生成任务中出现，列出每张图的差异维度。
- `Output Settings`：推荐模型、尺寸、质量和格式。
- `QA Checklist`：可读性、主体清晰度、构图、风格和人像一致性检查。
- `Next Step`：询问是否基于提示词调用 image2 / `gpt-image-2`。

## 模板文件

正式模板都放在 `references/` 下：

- `template-index.md`：模板索引和选择规则。
- `intake-guide.md`：不同图片类型的关键信息收集规则。
- `templates-xhs-cover.md`：小红书封面模板。
- `templates-concept-poster.md`：概念海报和 LUMEN ATLAS 城市海报模板。
- `templates-epic-narrative-poster.md`：史诗叙事海报模板。
- `templates-product-visual.md`：产品视觉和图片编辑模板。
- `templates-portrait.md`：人像写真模板，包括清透人像。
- `templates-anime-fashion-cover.md`：动漫角色奢华杂志封面模板，包括海贼王人物海报风格。
- `templates-gpt-image-2-advanced.md`：GPT Image 2 进阶工作流模板。

## 使用示例

```text
帮我做一张北京的 LUMEN ATLAS 城市海报，主色是金色和雾蓝色，标题写北京。
```

```text
我要做一个清透人像提示词，主题是夏日空气感，人物向上看，比例 9:10。
```

```text
做海贼王人物海报，角色是娜美，使用地中海度假风。
```

```text
基于这张产品图，生成 8 张小红书种草图变体，每张场景和文案不同。
```

## 安全和边界

- 公众人物或名人风格人像默认生成“氛围/风格参考”，不承诺复刻真实面孔。
- 私人人像、身份保留型编辑、产品图编辑等任务需要用户提供源图和必要授权。
- 健身训练图必须标注“非医疗建议”，不提供诊断、治疗或伤病承诺。
- 手相娱乐图必须标注“仅娱乐、无科学依据”，并避免上传清晰指纹或敏感身份信息。
- image-only 工作流必须使用 `gpt-image-2` 或支持 `image_generation` 的模型/工具。

## 安装

将整个 `image-prompt-generator/` 目录复制到 Codex 全局 skills 目录，或在项目中通过技能路径引用：

```text
C:\Users\<User>\.codex\skills\image-prompt-generator
```

技能入口文件是 `SKILL.md`。
