---
name: "jacky-illustration"
description: "Jacky-Illustration 统一生图入口：信息可视化配图、文章配图、Excalidraw 架构图、黑板报、可爱漫画，以及小黑 / 小芽哥 IP 型正文配图。"
---

# Jacky-Illustration

统一的中文内容配图与信息可视化生图入口。

它合并两类能力：

1. **信息可视化型**：适合知识科普、文章配图、结构图、黑板报、白板架构图。
2. **IP 型正文配图**：适合小黑 / Jacky 小芽哥这类固定视觉角色，让文章里的关键认知动作变成有识别度的正文插图。

## API Configuration

- **API Key**: 从环境变量 `GOOGLE_API_KEY` 读取，禁止写入 `SKILL.md` 或脚本
- **Default Model**: `nano-banana-pro-preview`
- **Default Aspect Ratio**: `4:3`
- **response_modalities**: Must be `['TEXT', 'IMAGE']` (not `['IMAGE']` alone)

## 图片风格选择

生成配图前，**必须先让用户选择风格**。使用 AskUserQuestion 工具展示以下 5 种风格供用户选择：

| 编号 | 风格名称 | 适用场景 |
|------|---------|---------|
| 1 | 信息洞察可视化（涂鸦手绘风） | AI 自媒体博主分享、知识科普、PPT 演示感 |
| 2 | 黑板报风格 | 教学场景、怀旧学术氛围、头脑风暴可视化 |
| 3 | 可爱漫画信息可视化 | 萌系科普、轻松教学、社交媒体传播 |
| 4 | Excalidraw 白板架构风格 | 技术架构图、系统设计、流程梳理 |
| 5 | IP 型正文配图（小黑 / Jacky 小芽哥） | 中文长文、方法论文章、观点文正文插图 |

---

### 风格 1：信息洞察可视化（涂鸦手绘风）

```
请帮我生成 4:3 比例的涂鸦风格图片来阐释此内容。
图片需保持统一的彩色粗铅笔手绘风格，信息提炼结构清晰，包含中文文本，采用白色纸张感背景，卡片边缘带轮廓线，并配有统一标题，类似于PPT演示文稿的呈现形式。
筛选最核心的信息进行图像生成，使信息能够清晰的演示，适用于有洞察的ai自媒体博主的分享演示，将专业的内容通俗易懂、结构清晰的明了地传递。

内容：[具体段落内容]
```

---

### 风格 2：黑板报风格

```
请帮我生成 [宽高比] 比例的黑板报风格图片来阐释此内容。

=== 标题样式 ===
"[主标题]" 使用粗体手写粉笔字排版，笔画粗壮，带有明显的粉笔颗粒质感。
字体颜色：[标题颜色]（如亮白色、明黄色、霓虹粉色）
纹理：干燥粉笔质感，覆盖不均匀，附带粉尘颗粒

=== 场景与布局 ===
布局：[布局类型]（如：问题-解决方案桥梁跨越鸿沟 / 圆形生命周期流程 / 带勾叉的结构化对比表格 / "该做vs不该做"分屏面板 / 输入-处理-输出等式 / 纵向功能列表 / 鱼骨因果图 / 收窄漏斗图 / 冰山表面vs隐藏层图 / 蜿蜒路线图旅程 / 分层技术堆栈——根据下方主要内容的逻辑选择）
背景：逼真的深绿色或哑光黑色黑板纹理，表面覆盖细微的粉笔灰残留、擦除痕迹和隐约可见的擦除文字痕迹，增强真实感。

=== 主要内容 ===
[步骤1] 视觉元素：[视觉元素描述1] 动作：手绘粉笔素描、轮廓图或数学图形 标签："[标签文字1]" 使用随性手写粉笔字体

[步骤2] 视觉元素：[视觉元素描述2] 动作：[动作或状态] 标签："[标签文字2]" 连接：[箭头样式]（如弯曲粉笔箭头 / 虚线 / 双向箭头）从上一步骤指向此步骤

[步骤3] [根据需要继续添加后续步骤]

=== 视觉风格 ===
材质：石板上的干粉彩粉笔。渲染：照片级真实纹理，呈现黑板的纹理质感和粉笔的粉末感。色彩：高对比度配色——深色背景搭配鲜艳的霓虹粉笔色调（青色、品红、酸橙绿、亮黄色），主要文字使用纯白色。

=== 装饰元素 ===
在角落空白处随机分布数学公式（如 E=mc²）、几何图形、星星、灯泡、下划线、波浪线和粉笔灰尘云。可选：底部添加木质粉笔槽，放置板擦或碎粉笔。

=== 氛围 ===
学术感、怀旧感、头脑风暴、教室氛围、教育性、专注、创意。

画质：高清晰度，粉笔纹理细节锐利，适合教室场景的逼真光照。

内容：[具体段落内容]
```

---

### 风格 3：可爱漫画信息可视化

```
请帮我生成 [宽高比] 比例的原创可爱漫画风格教育插图来阐释此内容。

=== 标题 ===
"[主标题]" 使用柔和粉色（#FFB7C5）圆润字体
[副标题（如需要）]

=== 场景与布局 ===
布局：[布局类型]（如：问题-解决方案桥梁跨越鸿沟 / 圆形生命周期流程 / 带勾叉的结构化对比表格 / "该做vs不该做"分屏面板 / 输入-处理-输出等式 / 纵向功能列表 / 鱼骨因果图 / 收窄漏斗图 / 冰山表面vs隐藏层图 / 蜿蜒路线图旅程 / 分层技术堆栈——根据下方主要内容的逻辑选择）
背景：柔和渐变色，从奶油色（#FFF8E7）到[主题色]，搭配少量[装饰元素]

=== 主要内容 ===
使用原创圆润小角色，不模仿任何受版权保护的具体 IP。

[内容段落1]
角色：[角色名称]
- [角色动作与表情]
- [道具或物品]
视觉元素：[关键视觉元素]
标签："[标签文字]"
[对话框或注释]

[内容段落2]
[与上方相同结构]

[内容段落N]
[根据需要继续]

=== 核心概念 ===
[数量] 个带可爱边框的浮动信息卡片：
卡片1："[概念1]"
卡片2："[概念2]"
卡片N："[概念N]"

=== 可爱漫画风格要求 ===
圆润身体、大而闪亮的眼睛、柔和腮红、小小四肢、超级变形比例、柔和线条画。角色必须是原创设计。

=== 氛围 ===
[情感基调]、[教育目标]，可爱但有信息量

画质：高质量可爱漫画插图，视觉层次清晰，[用途说明]

内容：[具体段落内容]
```

---

### 风格 4：Excalidraw 白板架构风格

```
请帮我生成符合以下要求的 [架构名称] 架构图。

风格：Excalidraw 风格的架构图，手绘风格，简洁的黑色线条，极简的方框和箭头布局，专业的技术草图，纯白色背景（#FFFFFF），逻辑清晰明了，高对比度，架构可视化。如果需要突出显示，可以使用少量红色线条和文字。

布局：16:9 横向布局/纵向布局（根据需求选择）

内容结构：
 【模块A】：功能1 | 功能2 | 功能3
 【模块B】：功能1 | 功能2
 （根据实际架构情况填写）

连接关系：
使用箭头指示数据流/处理方向
用虚线表示辅助/监控关系
标注关键节点描述

内容：[具体架构内容]
```

---

### 风格 5：IP 型正文配图（小黑 / Jacky 小芽哥）

这个模式用于文章正文插图，不追求 PPT 式完整说明，而是把文章里的一个认知动作画成清爽、怪诞、有识别度的手绘解释图。

用户选择此风格后，继续让用户二选一：

| IP | 使用目录 | 适合场景 |
| --- | --- | --- |
| 小黑 | `ian-xiaohei-illustrations/` | 黑色小人、怪诞手绘、白底正文配图 |
| Jacky 小芽哥 | `jacky-growth-illustrations/` | 白色豆豆体型、头顶嫩芽、Jacky 无限生长视觉符号 |

工作方式：

1. 先读对应目录的 `SKILL.md` 和 `references/`。
2. 先输出 shot list：放在哪段后、图的主题、核心意思、结构类型、角色动作、建议中文标注词。
3. 如果用户明确要求生成图片，再用 `image_gen` 逐张生成。
4. 每张图只讲一个核心结构，不要把文章做成说明书。

通用提示词骨架：

```
请为以下内容生成 16:9 横版中文正文配图。
风格：纯白背景，黑色手绘线稿，大量留白，少量红色/橙色/蓝色中文手写批注。
主体：[小黑 / Jacky 小芽哥] 必须参与画面的核心动作，不能只是站在旁边装饰。
画面目标：把这段内容里的关键判断、流程、状态或隐喻变成一张清爽但有记忆点的解释图。
禁止：PPT感、复杂架构图、商业插画、幼稚贴纸、过多中文、左上角大标题。

内容：[具体段落内容]
```

---

## Workflow

1. **选择风格**: 使用 AskUserQuestion 让用户从 5 种风格中选择
2. **Read Article**: Read the target article, split into logical sections
3. **Plan Illustrations**: For each section, extract core information as image content prompt
4. **Generate Images**: Use the selected style prompt + section content to generate images via Gemini API；IP 型正文配图优先使用内置 `image_gen`
5. **Save Output**: Save images to `output/` directory in the project folder

## Image Generation Code Pattern

```python
from google import genai
from google.genai import types
from PIL import Image
import io
import os

api_key = os.environ.get("GOOGLE_API_KEY")
if not api_key:
    raise RuntimeError("Missing GOOGLE_API_KEY")

client = genai.Client(api_key=api_key)

# style_prompt 根据用户选择的风格动态设置
# 参见上方「图片风格选择」章节中的 5 种风格 prompt
style_prompt = selected_style_prompt + "\n\n内容："

response = client.models.generate_content(
    model='nano-banana-pro-preview',
    contents=[style_prompt + section_content],
    config=types.GenerateContentConfig(
        response_modalities=['TEXT', 'IMAGE'],
        image_config=types.ImageConfig(aspect_ratio='4:3')
    )
)

for part in response.candidates[0].content.parts:
    if part.inline_data:
        img = Image.open(io.BytesIO(part.inline_data.data))
        img.save('output/image_name.png')
```

## Important Notes

- **response_modalities** MUST be `['TEXT', 'IMAGE']`, not `['IMAGE']` alone
- Add `time.sleep(3)` between API calls for rate limiting
- Required packages: `google-genai`, `Pillow`
- Image count: decide based on content, aim for 1 per section, max 2 per section

## Resources

- **`assets/template.html`**: HTML/CSS template for converting articles to web pages
- **`references/api_guide.md`**: Nano Banana Pro API documentation
- **`scripts/article-Illustration-generator.py`**: Automated script (legacy, use code pattern above instead)
- **`ian-xiaohei-illustrations/`**: 小黑 IP 型正文配图 skill
- **`jacky-growth-illustrations/`**: Jacky 小芽哥 IP 型正文配图 skill
