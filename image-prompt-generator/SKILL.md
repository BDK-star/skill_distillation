---
name: "image-prompt-generator"
description: "Generates high-quality image prompts from word/phrase input via step-by-step guided workflow. Invoke when user wants to create concept images, typography art, or visual metaphor posters."
---

# Image Prompt Generator

A step-by-step guided skill that helps users generate professional image prompts. Supports two core modes: Typography Aesthetic Concept Image and Advanced Concept Poster.

## Trigger Conditions

Invoke this skill when user:
- Wants to generate an image prompt for a word/phrase
- Mentions "concept image", "typography art", "concept poster", "visual metaphor"
- Asks to create a word-based visual design
- Says "生成图片提示词", "概念图", "字体美学", "概念海报"

## Workflow

### Step 1: Choose Image Type

Ask the user to select one of two image types using AskUserQuestion:

**Option A: Typography Aesthetic Concept Image (字体美学概念图)**
- Text IS the art — the word itself becomes the visual subject
- Typography becomes metaphor: stretch, fracture, nest, deform
- Style self-adapts to word meaning (minimalism to surrealism)
- 14 aspect ratios available, matched to word semantics
- Best for: single words, abstract concepts, philosophical terms, emotional words

**Option B: Advanced Concept Poster (高级概念海报)**
- Image + Text together form a visual sentence
- Visual metaphor deepens the word's meaning through composition
- Fixed style: graphic art poster with silkscreen/lithograph texture
- Image elements interact with text to tell a story
- Best for: phrases, short sentences, social commentary, narrative concepts

### Step 2: Collect Core Input

Based on the chosen type, collect the following information step by step:

**Required for both types:**
1. **Core Text** — The word, phrase, or short sentence (核心文字/单词/词组)
2. **Language** — Chinese or English (文字语言)

**Optional for both types:**
3. **Supplementary Context** — Any background or context for the word (补充语境)
4. **Emotion Tendency** — Preferred emotional direction (情绪倾向), e.g.: 温柔/冷峻/危险/孤独/浪漫/压迫/希望/纯真/欲望/秩序/冲突/疏离/自由/沉默/毁灭/重生
5. **Disabled Elements** — Elements to avoid in the image (禁用元素)

**Additional for Type A only:**
6. **Aspect Ratio Preference** — Auto/Square/Portrait/Landscape/Ultrawide/Ultratall/Banner (画幅偏好), default: auto-detect from word meaning
7. **Style Preference** — Auto/Minimalist/Constructivist/Swiss Grid/Japanese/Oriental Calligraphy/Luxury Brand/Futurist/Classical/Surrealist/Avant-garde/Abstract/Neo-Bauhaus (风格偏好), default: auto-detect from word meaning

**Additional for Type B only:**
6. **Visual Metaphor Preference** — Preferred metaphor type (隐喻偏好), e.g.: 人物关系/物体关系/空间关系/对比关系/象征关系/冲突关系/荒诞关系/诗意关系
7. **Auxiliary Text** — Optional small subtitle to deepen the theme (辅助短句)

### Step 3: Semantic Analysis

Before generating the prompt, perform a deep semantic analysis of the core text:

1. **Literal meaning** — What does this word/phrase literally mean?
2. **Emotion type** — Which emotion category does it belong to?
3. **Deep metaphor** — What is the deeper, non-cliché metaphor?
   - NOT "freedom = blue sky + birds", BUT "freedom = boundaries dissolving, structures loosening, space expanding"
   - NOT "desire = red + fire", BUT "desire = gravity, pulling, emptiness, unstoppable approach"
   - NOT "loneliness = one person", BUT "loneliness = absence of response, scale imbalance, too much blank space"
   - NOT "time = clock", BUT "time = afterimages, repetition, fading, weathering, echoes, irreversibility"
4. **Visual logic** — Which visual logic best carries this meaning?
5. **Spatial tendency** — Expand/compress/fall/rise/enclose/fracture/condense/diffuse/cycle?

### Step 4: Generate Prompt

Based on the chosen type and collected inputs, generate the complete image prompt.

**For Type A (Typography Aesthetic Concept Image), include these sections:**

```
请以「[Core Text]」为核心，生成一张顶级字体美学概念图像。

[Auto-generated semantic analysis paragraph — explain the deep metaphor and visual logic chosen]

一、最重要原则：文字必须绝对突出
「[Core Text]」必须是画面的绝对主角。
1. 文字在画面中尺寸足够大。
2. 文字位于视觉中心、黄金位置或最强视觉区域。
3. 文字与背景有清晰对比。
4. 文字不能被大量元素遮挡。
5. 文字不能缩小成装饰。
6. 文字不能像海报标题一样附属在画面边缘。
7. 文字不能被场景淹没。
8. 文字不能只是贴在背景上的普通字。
9. 文字必须具有强烈字体设计感。
10. 观者第一眼必须先看到文字，再看到其他元素。

二、文字本身必须体现隐喻
[Based on semantic analysis, specify how the typography should express the metaphor]
- 字形变化方式：[stretch/fracture/compress/grow/nest/etc.]
- 如果是中文：准确呈现每个汉字，尊重基本结构，不能多笔少笔错笔乱码，偏旁重心笔画粗细间架结构必须有设计感
- 如果是英文：准确拼写，字距字重比例基线节奏负形空间必须高级

三、围绕文字建立隐喻系统
[Specify 2-4 core metaphor elements that serve the word meaning]
- 核心隐喻元素：[element 1], [element 2], [element 3]
- 元素与文字的互动方式：[grow from strokes / cut through / enclose / support / compress / release / etc.]

四、风格
[Auto-selected style based on word meaning and user preference]
- 视觉风格：[specific style]
- 画幅比例：[specific ratio with justification]

五、色彩与光影
[Auto-selected color palette and lighting based on word meaning]
- 主色调：[colors]
- 光影逻辑：[how light serves the metaphor]

六、材质
[Auto-selected material language based on word meaning]
- 材质语言：[specific materials]

七、禁止内容
不要让文字太小。不要让文字不突出。不要让场景抢走文字。不要把文字当成小标题。不要只生成背景加小字。不要使用普通默认字体。不要错字乱码伪文字。不要加入额外说明文字。不要水印签名Logo二维码。不要随机堆砌符号。不要使用无关装饰。不要让风格千篇一律。不要廉价3D字。不要俗气霓虹。不要PPT封面。不要Canva模板。不要淘宝广告风。不要儿童插画风。不要低清晰度模糊锯齿。不要AI随机感。
```

**For Type B (Advanced Concept Poster), include these sections:**

```
你要生成的是一张"基于词语含义自动构建视觉隐喻"的高级概念海报。

核心文字：「[Core Text]」

[Auto-generated semantic analysis paragraph — explain the deep metaphor and visual logic chosen]

一、画面构图逻辑
- 大字「[Core Text]」作为画面核心骨架，大尺寸占据重要区域，具有强识别性与压迫感
- 图像元素与文字产生关系：[specific interaction — standing before text / embedded in text / cutting text / forming contrast with text]
- 元素数量克制，控制在少量关键主体之内
- 视觉层级：文字第一层，图像叙事第二层，细小说明文字第三层
- 留白聪明，让画面有呼吸感和设计感

二、图像表达逻辑
[Based on semantic analysis, specify the visual metaphor strategy]
- 隐喻方式：[specific metaphor — scale contrast / directional relationship / distance / occlusion / action moment / etc.]
- 画面应具有"看到后会心一击"的感觉
- [If conflict/paradox exists]: 通过对立元素强化张力
- [If poetic/emotional]: 使用含蓄、留白、克制的图像策略

三、视觉风格
- 高级图形艺术海报，具有拼贴感、丝网印刷感、石版印刷感或版画式质感
- 强烈平面设计感，不是普通三维插画
- 干净统一的色彩逻辑，颜色数量不宜过多
- [Color scheme based on word meaning]
- 质感带细微颗粒、纸张纹理、印刷噪点、轻微做旧感，整体清爽利落高级

四、文字排版
- 「[Core Text]」作为核心标题，大且醒目
- [If Chinese]: 中文大字排布，保证画面核心地位
- [If English]: 保留原文，字形强烈清晰有视觉冲击力
- [If auxiliary text provided]: 画面[位置]加入小型辅助短句「[auxiliary text]」深化主题
- 可加入极小号辅助信息/编号/署名增强海报艺术感
- 所有文字像从画面中生长出来，不能像后期贴上去

五、禁止内容
不要做成廉价模板。不要低级拼贴感。不要广告页。不要普通电商排版。不要过度解释。不要多余元素。不要画面拥挤。不要为了好看偏离主题。
```

### Step 5: Review and Iterate

After generating the prompt:
1. Show the complete prompt to the user
2. Ask if they want to adjust any aspect: metaphor, style, color, composition, aspect ratio, etc.
3. If adjustments are needed, modify the corresponding section and regenerate
4. Confirm final prompt

## Important Rules

1. Always use AskUserQuestion for interactive steps — never assume user preferences
2. Semantic analysis must go beyond surface-level associations — find deeper metaphors
3. The generated prompt must be complete and self-contained, ready to paste into an image generation tool
4. If the user provides partial input, intelligently fill in the gaps based on semantic analysis
5. Never generate the same style for different words — each word deserves its own visual personality
6. Keep the prompt in the same language as the user's core text (Chinese input → Chinese prompt, English input → English prompt), but the skill workflow language follows the user's conversation language
