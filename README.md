# Jacky Growth Illustrations

> 为“Jacky无限生长”定制的 Codex 正文配图 Skill。
>
> 16:9 横版 | Jacky 小芽哥 IP | 白色小黑体型 | 头顶嫩芽 | 可选墨镜 | 纯白黑线手绘 | 少量红橙蓝中文批注

## 这个仓库是什么

这是基于 Ian Xiaohei Illustrations fork 出来的定制版。目标是把原来的“小黑”固定 IP，改造成更适合“Jacky无限生长”的视觉符号：**Jacky 小芽哥**。

Jacky 小芽哥是一个白色豆豆体型、头顶嫩芽、细手细腿的知识工位角色。它可以戴小墨镜，呈现一点“潇洒哥”的松弛自信，但仍然保持白底黑线、克制手绘、正文配图的气质。

一句话：**让 AI 不只是“配一张图”，而是把文章里的关键认知动作，画成有 Jacky 个人识别度的手绘解释图。**

## 当前可用 Skill

真正需要安装到 Codex 的是：

```text
jacky-growth-illustrations/
```

默认产出：

- 一篇文章的 4-8 张 shot list
- 单张 16:9 横版正文配图
- 白底黑线手绘风格
- Jacky 小芽哥作为核心动作主体
- 少量红/橙/蓝中文手写批注
- 极少量绿色只用于头顶嫩芽或生长点
- 墨镜可选，用于“潇洒哥”气质

## 视觉符号规范

角色形态说明图：

```text
jacky-growth-illustrations/assets/jacky-sprout-guy-character-spec-v1.svg
```

这个文件锁定三件事：

- 白色圆润豆豆/小黑体型。
- 头顶嫩芽是第一识别点。
- 墨镜是可选配件，不能喧宾夺主。

## 安装

从仓库根目录复制 skill：

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./jacky-growth-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

安装后，在 Codex 里使用：

```text
Use $jacky-growth-illustrations 为这篇中文文章设计并生成 5 张 Jacky 小芽哥正文配图。
```

## 用法示例

### 只做配图规划

```text
Use $jacky-growth-illustrations 先不要生图。
请分析下面这篇文章哪里值得配图，输出 5 张左右的 shot list。
每张图写清楚：放在哪段后、主题、核心意思、结构类型、Jacky 小芽哥在做什么、建议中文标注词。

<粘贴文章>
```

### 直接生成正文配图

```text
Use $jacky-growth-illustrations 把下面这篇文章生成 4 张 Jacky 小芽哥正文配图。
要求：16:9 横版、纯白背景、黑色手绘线稿、少量红橙蓝中文手写批注，白色豆豆体型和头顶嫩芽清楚；墨镜可选，但不要太大。

<粘贴文章>
```

### 为单个概念生成一张图

```text
Use $jacky-growth-illustrations 为“真正的成长不是收藏更多方法，而是让一个动作反复发芽”生成一张正文配图。
画面要怪诞但清爽，Jacky 小芽哥必须承担核心动作；可以有一点潇洒哥气质。
```

## 目录结构

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── examples/
│   ├── prompts.md
│   └── images/                  # 原 fork 示例，仅作来源对照
├── ian-xiaohei-illustrations/   # 原始小黑版本，保留作对照
└── jacky-growth-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── jacky-sprout-guy-character-spec-v1.svg
    └── references/
        ├── style-dna.md
        ├── jacky-sprout-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

## 注意事项

- 图片里的中文文字越短越稳定。
- 每张图只讲一个核心结构，不要把文章做成说明书。
- Jacky 小芽哥必须承担核心动作；如果去掉角色画面仍然完全成立，说明角色太装饰了。
- 头顶嫩芽必须清楚可见，但不要把整张图做成绿色主题。
- 墨镜是人格配件，不是必备；不要画太大、太凶、太油腻。
- 不要画成树桩、普通人形、动物、机器人或商业贴纸。
- AI 图像模型可能出现错字、幻觉标签、风格漂移或多余标题，生成后需要检查。

## 来源与许可

本仓库基于 [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations) 定制，保留原始目录用于来源对照。License 见 [LICENSE](LICENSE)。
