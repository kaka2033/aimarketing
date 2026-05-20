# Brand Copy System

> A prompt template for generating complete, cohesive brand copy systems from a structured brief — works with any capable LLM (Claude, GPT, Gemini, DeepSeek, Qwen, etc.).

[简体中文](#中文文档) · [English](#english-docs)

---

## English Docs

### What This Is

A single-file prompt template (`SKILL.md`) that turns a 5-field brand brief into a complete brand messaging system: positioning, values, voice & tone, taglines, brand story, channel copy templates, and internal alignment docs.

It was originally built as a [Claude Skill](https://docs.claude.com/en/docs/agents-and-tools/skills) but the prompt structure is model-agnostic. Paste `SKILL.md` into any chat with a capable LLM and provide your brief.

### Why You Might Want This

Most "brand copy generators" produce a slogan or a tagline in isolation. The output looks fine until you put it next to the rest of the brand's communication and realize nothing connects. A real brand copy system is internally consistent: the tagline derives from the positioning, the social post sounds like the website, the website sounds like the founder.

This template enforces that consistency by always generating the strategic foundation (positioning → values → personality → tone) *before* writing any copy, then deriving every downstream asset from that foundation.

### How to Use It

**Option 1: With Claude (recommended)**

1. Download `brand-copy-system.skill` from the [Releases](https://github.com/kaka2033/aimarketing/releases) page
2. Install it in Claude.ai (drag into a chat or click "Save skill")
3. Start a new chat and provide your brief — the skill auto-triggers

**Option 2: With any other LLM**

1. Open `SKILL.md` in this repo
2. Copy the entire content
3. Paste into ChatGPT / Gemini / DeepSeek / Qwen / etc. with a leading instruction like: *"Follow the instructions in the document below to generate a brand copy system. My brief is: [your brief]"*
4. The model will walk through the framework and produce the same structured output

**Option 3: Build your own tool**

The template is plain Markdown — fork the repo, adapt the framework to your domain (B2B SaaS, luxury retail, F&B, etc.), and wrap it in a UI of your choice.

### The Brief Format

Provide these 5 inputs to get started:

| Field | What to provide |
|-------|-----------------|
| Brand Name | The brand or product name |
| Core Idea | One sentence: what this brand stands for |
| Industry | Category + competitive context |
| Region | Primary market(s) |
| Target Audience | Demographics + psychographics |

Four more inputs are optional (language, tone keywords, competitors, channel list, price positioning). If omitted, sensible defaults are inferred.

### What You Get

Four modules of interconnected output:

- **Module A — Core Messaging**: 3 ranked tagline options, brand story (150-250 words), elevator pitch, 3 value propositions
- **Module B — Tone of Voice Guide**: 3 voice principles with Do/Don't examples, preferred/avoid word lists, before-after rewrites
- **Module C — Channel Copy Templates**: website hero, social bios, post templates, e-commerce detail page, offline materials
- **Module D — Internal Alignment**: mission, vision, messaging hierarchy table

Plus a strategic foundation at the top (positioning statement, values, personality, tone spectrum) that anchors everything.

See [`examples/xinjiay-snack-store.md`](examples/xinjiay-snack-store.md) for a full sample output.

### Honest Limitations

- **It's a prompt, not magic.** Output quality depends on the model you use and the specificity of your brief. Vague briefs produce vague copy.
- **First drafts need editing.** Treat output as a structured starting point, not a finished deliverable. A brand strategist will still want to refine 30-40% of the language.
- **Cultural fluency varies by model.** Chinese-market copy works best with models strong in Chinese (Claude, Qwen, DeepSeek). Don't expect platform-native Xiaohongshu voice from a model that's only been trained heavily on English data.
- **No competitive research.** This template doesn't do market analysis — it assumes you've already done the strategic thinking and just need to translate it into a consistent copy system.

### Repository Structure

```
brand-copy-system/
├── SKILL.md                    ← The prompt template (core file)
├── README.md                   ← You are here
├── LICENSE                     ← MIT
├── CONTRIBUTING.md             ← How to suggest improvements
└── examples/
    └── xinjiay-snack-store.md  ← Full sample output
```

### Contributing

Improvements welcome. Particularly interested in:
- Variants for specific industries (B2B SaaS, luxury, F&B, healthcare)
- Additional language/region adaptations
- Better channel templates as platforms evolve

See [CONTRIBUTING.md](CONTRIBUTING.md).

### License

MIT — use it, fork it, sell tools built on it. Attribution appreciated but not required.

---

## 中文文档

### 这是什么

一个用于生成完整品牌文案体系的 prompt 模板（`SKILL.md`）。给它一份 5 字段的品牌 brief，它会输出一套内部一致的品牌内容：定位语、价值观、品牌人格、语调指南、Slogan、品牌故事、渠道文案模板、内部对齐文档。

最初是作为 [Claude Skill](https://docs.claude.com/en/docs/agents-and-tools/skills) 开发的，但 prompt 结构与模型无关。把 `SKILL.md` 粘贴给任何有能力的大模型（Claude、GPT、Gemini、DeepSeek、通义千问、文心一言 等）都能用。

### 为什么你可能需要它

大多数"品牌文案生成器"只能孤立地给你一个 Slogan 或 Tagline。单看挺像样，放到品牌的其他物料旁边就发现哪儿哪儿都对不上。真正的品牌文案体系是内部自洽的：Slogan 是从定位推出来的，社媒发文听起来和官网首屏是一个调调，官网首屏和创始人讲品牌时的话术也是一致的。

这个模板通过强制流程保证这种一致性：先生成战略基础（定位 → 价值观 → 人格 → 调性），再从这个基础推导所有下游文案。

### 怎么用

**方案一：配合 Claude 使用（推荐）**

1. 从[Releases](https://github.com/kaka2033/aimarketing/releases) 页下载 `brand-copy-system.skill`
2. 在 Claude.ai 里安装（拖到对话框，或点 Save skill）
3. 开新对话，直接给 brief — skill 会自动触发

**方案二：配合其他大模型使用**

1. 打开本仓库的 `SKILL.md`
2. 复制全部内容
3. 粘贴到 ChatGPT / Gemini / DeepSeek / 通义千问 / 文心一言 等，前面加一句指令：*"请按以下文档的说明生成品牌文案体系，我的 brief 是：[你的 brief]"*
4. 模型会按框架走完整流程，产出同样结构化的结果

**方案三：自己改造**

模板就是纯 Markdown — fork 仓库，按你的领域调整框架（B2B SaaS、奢侈品、餐饮、医疗等），然后包一层你喜欢的 UI。

### Brief 格式

提供 5 项核心输入即可：

| 字段 | 内容 |
|------|------|
| 品牌名称 | 品牌或产品名 |
| 核心理念 | 一句话，这个品牌最重要的是什么 |
| 行业 | 品类 + 竞争背景 |
| 区域 | 主要市场 |
| 目标人群 | 人口属性 + 心理属性 |

另外 4 项是可选的（语言、调性关键词、竞品、渠道列表、价格定位）。不填会自动推断。

### 你会得到什么

四大模块，互相关联：

- **模块 A — 核心信息**：3 个排序后的 Slogan 备选、品牌故事（150-250 字）、电梯演讲、3 个价值主张
- **模块 B — 语调指南**：3 条表达原则（含 Do/Don't 示例）、推荐/避免词表、改写示范
- **模块 C — 渠道文案模板**：官网首屏、社媒简介、社媒帖子模板、电商详情页、线下物料
- **模块 D — 内部对齐**：使命、愿景、消息层级表

外加最上面的战略基础（定位语、价值观、品牌人格、语调光谱），统领所有下游内容。

完整样例见 [`examples/xinjiay-snack-store.md`](examples/xinjiay-snack-store.md)。

### 老实说的几个局限

- **这是 prompt，不是魔法。** 输出质量取决于你用的模型和 brief 的具体程度。模糊的 brief 只会产出模糊的文案。
- **初稿需要修改。** 把输出当作结构化的起点，不是成品。品牌策略师还是会想改 30-40% 的措辞。
- **不同模型的本土化能力不同。** 中文市场文案在中文强的模型上效果最好（Claude、通义千问、DeepSeek）。别指望一个英文为主训练的模型能写出原生小红书的味道。
- **不做竞品研究。** 这个模板不做市场分析 — 它假设你已经想清楚战略，只是需要把它翻译成一套一致的文案体系。

### 仓库结构

```
brand-copy-system/
├── SKILL.md                    ← Prompt 模板（核心文件）
├── README.md                   ← 当前文件
├── LICENSE                     ← MIT
├── CONTRIBUTING.md             ← 贡献指南
└── examples/
    └── xinjiay-snack-store.md  ← 完整样例输出
```

### 贡献

欢迎改进。特别欢迎以下方向的 PR：
- 特定行业的变体（B2B SaaS、奢侈品、餐饮、医疗等）
- 更多语言/地区的适配
- 随平台演进的渠道模板更新

参见 [CONTRIBUTING.md](CONTRIBUTING.md)。

### 许可

MIT — 随便用、随便 fork、基于它做商业产品都可以。注明出处不强制但欢迎。

---

*Built with care. Open to feedback.*
