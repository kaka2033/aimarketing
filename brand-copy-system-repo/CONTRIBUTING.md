# Contributing

Thanks for considering a contribution. This repo is intentionally small — the value lives in one prompt file — so contributions should be focused and high-quality.

## What's Most Useful

**Industry variants** — A version of `SKILL.md` tuned for a specific domain. For example:
- `variants/b2b-saas.md` — adapted for B2B software (different channels, ROI-driven tone)
- `variants/luxury-retail.md` — adapted for luxury (different word lists, restrained tone)
- `variants/healthcare.md` — adapted for healthcare (regulatory caution, trust-building)

Submit as a new file in a `variants/` directory with a brief note in the README explaining when to use it.

**Example outputs** — Run the prompt on a real or fictional brand and add the result to `examples/`. The more variety the better — different industries, regions, brand types.

**Translation** — README is currently bilingual (EN + ZH-CN). Translations to other languages welcome. Add as `README.{locale}.md`.

**Bug fixes in the prompt** — If you find that a particular section reliably produces poor output, propose a fix. Include before/after examples.

## What's Less Useful

- Renaming files or restructuring the repo without a clear improvement reason
- Adding tooling (build scripts, package.json, etc.) — this is meant to stay simple
- Expanding scope (e.g. turning it into a full brand kit generator with logo/colors) — that's a separate project

## How to Submit

1. Fork the repo
2. Create a branch with a descriptive name (e.g. `variant/luxury-retail`, `example/fintech-startup`)
3. Make your change
4. Open a PR with:
   - What changed and why
   - For variants: an example output showing how it differs from the base prompt
   - For prompt fixes: before/after examples on the same brief

## Style Notes

- Keep the prompt instructional, not theoretical. Tell the model what to do, not what brand strategy is.
- Match the existing tone — direct, practical, honest about limitations.
- Don't add buzzwords. If a section can't be explained without "synergy" or "leverage", rewrite it.

## Questions

Open an issue. No template needed — just describe what you're thinking.
