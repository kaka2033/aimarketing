---
name: brand-copy-system
description: >
  Generate a complete, cohesive brand copy system from a structured brief.
  Use this skill whenever the user wants to create brand copy, brand messaging,
  brand identity text, brand guidelines text, taglines, slogans, brand stories,
  tone of voice guides, or any systematic set of brand communications materials.
  Trigger on phrases like: "品牌文案", "品牌全案", "brand copy", "brand messaging system",
  "品牌体系", "一键生成文案", "品牌定位文案", "brand identity copy", "全套品牌文案",
  "品牌故事", "tone of voice", "品牌调性", or when the user provides a brand brief
  and expects a full set of deliverables. Also trigger when the user says things like
  "help me build out brand messaging", "create copy for a new brand", or "写一套品牌文案".
  Even if the user only asks for one piece (e.g. just a tagline), consider suggesting
  the full system if context implies they're building a brand from scratch.
---

# Brand Copy System Generator

## Overview

This skill generates a complete brand copy system from a structured brief. The output is a cohesive set of brand messaging documents that work together — not a collection of isolated pieces. Every element derives from the same strategic foundation and maintains tonal consistency.

## Step 1: Collect the Brief

Before generating anything, ensure you have these inputs. If the user hasn't provided them, ask — but ask efficiently (one round, not an interview).

### Required Inputs

| Field | Description | Example |
|-------|-------------|---------|
| **Brand Name** | The brand or product name | "GreenLeaf" |
| **Core Idea** | The single most important thing the brand stands for, in one sentence | "Making sustainable living effortless for urban families" |
| **Industry** | The category and competitive context | "Organic household products / FMCG" |
| **Region** | Primary market(s), affects cultural tone and language | "China Tier 1-2 cities" |
| **Target Audience** | Who the brand speaks to — demographics + psychographics | "25-40 urban parents who care about health but lack time" |

### Optional Inputs (use defaults if not provided)

| Field | Default if omitted |
|-------|-------------------|
| **Language** | Match the user's language; if the brief is bilingual, output bilingual |
| **Tone Keywords** | Infer 3-4 from the Core Idea and Industry |
| **Competitor Context** | Skip competitive positioning section |
| **Channel List** | Use standard set: official website, social media (WeChat/Xiaohongshu or Instagram/LinkedIn based on region), offline materials, e-commerce detail page |
| **Price Positioning** | Infer from industry + audience |

## Step 2: Build the Strategic Foundation

Before writing any copy, establish these internally. Show them to the user as the first section of the output — they anchor everything that follows.

### 2a. Brand Positioning Statement

Use this formula:
> For [target audience] who [key need/tension], [Brand] is the [category frame] that [key differentiator], because [reason to believe].

Write exactly ONE positioning statement. It should be tight enough to fit in a single breath.

### 2b. Brand Values (3-5)

Each value gets:
- A short label (2-3 words)
- A one-sentence definition explaining what this value means *in practice* for this brand (not a generic dictionary definition)

### 2c. Brand Personality

Describe the brand as if it were a person. Use the "is / is not" framework:
- 3-4 "is" traits (e.g. "confident but not arrogant")
- For each trait, a concrete behavioral example of how this shows up in communication

### 2d. Tone of Voice Spectrum

Define tone on 4 dimensions, each as a position on a spectrum:

- Formal ←→ Casual
- Serious ←→ Playful
- Authoritative ←→ Approachable
- Reserved ←→ Expressive

For each, mark the brand's position (e.g. "leans casual, ~70/100") and give a one-sentence rationale.

## Step 3: Generate the Copy System

With the foundation locked, generate these deliverables in order. Each builds on the previous.

### Module A: Core Messaging

1. **Primary Tagline / Slogan**
   - Provide 3 options, ranked by recommendation strength
   - Each ≤10 words (≤15 Chinese characters)
   - For each, a one-line rationale explaining the strategic logic

2. **Brand Story (品牌故事)**
   - 150-250 words
   - Structure: tension → vision → action → invitation
   - Written in the brand's voice, not about the brand in third person
   - This is the "origin narrative" — why this brand exists in the world

3. **Elevator Pitch**
   - 30-second spoken version (~80 words)
   - Designed for a founder or sales lead to say out loud
   - Must sound natural, not like ad copy

4. **Value Propositions (3)**
   - Each: headline (≤8 words) + supporting sentence (≤25 words)
   - Map to the top 3 reasons the target audience should care

### Module B: Tone of Voice Guide

A practical reference for anyone writing on behalf of the brand.

1. **Voice Principles** — 3 rules, each with a "Do / Don't" example pair
2. **Word List**
   - "Preferred Words": 10-15 words the brand gravitates toward
   - "Avoid Words": 10-15 words that clash with the brand personality
3. **Sample Rewrites** — Take 2 generic sentences and rewrite them in the brand voice, showing before/after

### Module C: Channel Copy Templates

For each channel (from the brief or defaults), generate:

1. **Official Website — Hero Section**
   - Headline + subheadline + CTA button text
   - 2 variants

2. **Social Media Bio**
   - Platform-appropriate (WeChat/Xiaohongshu for China; Instagram/LinkedIn for global)
   - Within character limits

3. **Social Media Post Template**
   - 1 product launch post
   - 1 brand awareness / storytelling post
   - Include suggested hashtag strategy (5-8 tags)

4. **E-commerce Product Detail Page (if applicable)**
   - Hero headline
   - 3 benefit bullets
   - Trust statement

5. **Offline / Print (if applicable)**
   - One-liner for packaging or in-store display
   - Event booth headline + supporting line

### Module D: Internal Alignment

1. **Brand Mission Statement** — One sentence, for internal use (can be more direct than external copy)
2. **Brand Vision Statement** — Where the brand aims to be in 5-10 years
3. **Messaging Hierarchy** — A simple table showing which messages are primary, secondary, and tertiary, and in which contexts each is used

## Step 4: Output Format

Generate the complete system as a single structured Markdown document. Use clear H2/H3 headers for each module and sub-section so the user can navigate easily.

At the top, include a brief "Brief Summary" block that echoes back the inputs so the user can verify alignment before reading the full output.

If the user wants a Word document or presentation, convert after generating the Markdown — don't write directly into those formats.

## Quality Checks

Before delivering, verify:

- [ ] Every piece of copy traces back to the positioning statement — no orphan messages
- [ ] Tone is consistent across all modules (a tagline shouldn't sound playful if the brand story sounds corporate)
- [ ] No generic filler ("innovative solutions", "passionate team", "leverage synergies") — every sentence should be specific to THIS brand
- [ ] If bilingual, terminology is consistent (same English terms used for the same concepts throughout)
- [ ] Channel copy respects platform conventions (Xiaohongshu copy sounds different from LinkedIn copy)
- [ ] The system is self-consistent — if a reader saw only the social bio and only the packaging line, they'd know it's the same brand

## Language & Localization Notes

- **Chinese market**: Default to Mandarin Chinese output. Preserve English terms for industry-standard concepts (FMCG, SKU, KOL, ROI, CTA). Use 简体中文. Xiaohongshu copy should feel native to the platform — emoji usage, sentence rhythm, hashtag conventions.
- **Global/English market**: Default to English. Adapt cultural references and platform assumptions accordingly.
- **Bilingual brief**: Output the full system in the primary market language, then provide English translations for the Core Messaging module (Module A) only, unless the user asks for full bilingual output.

## Iteration Guidance

After delivering the first draft, invite feedback with:
"这是基于您的 brief 生成的完整品牌文案体系初稿。建议您优先确认【模块A：核心信息】的方向是否正确——如果定位语和品牌故事方向对了，其他模块的调整会很快。如果方向需要调整，告诉我哪里偏了，我会整体修订。"

(Or the English equivalent if the user is working in English.)
