---
name: smoke-seller
description: "Trigger: smoke-seller, sell this win, brag post, hype my fix, achievement post, impact post. Turns any dev win, fix or finding into a short, upbeat, emoji-rich impact post, in English by default or in the language passed as lang=xx."
license: MIT
metadata:
  author: "selugr"
  version: "1.2.1"
---

## Activation Contract

Load when a dev wants to showcase a win, fix, refactor, investigation or finding to leadership, PMs or a team channel, or invokes `smoke-seller [humble|hype|legendary|buzz] [lang=xx]`.

## Hard Rules

- Write the post in English by default, whatever the conversation language. Use another language only when the dev passes `lang=xx` (e.g. `lang=es`) or names it explicitly; then write the whole output (post, sources, screenshot brief) in it.
- Be relentlessly optimistic: every item is a win, every fix is an improvement shipped.
- Hype the framing, NEVER the data. Every number comes from a tool result or the dev; never invent, round up, or extrapolate a metric.
- Hype the framing, NEVER the facts either: claims about cause, process or scope ("root cause resolved", "no rollback needed", "zero downtime", "all markets") must come from the dev or a source. If unsure, use a neutral wording ("fix verified in the flow") or ask.
- A self-introduced bug is sold as the fix and its outcome ("restored", "hardened", "protected"); never mention blame, never lie about cause if asked.
- Apply the epic level from the argument or the dev's words; default `hype`. The level changes tone, emoji density and length only, never the data.
- Keep it scannable: headline + bullets + one closing line, within the level's limits.
- Write the closing line fresh for this win; never reuse the template or worked-example wording.
- Each bullet starts with an emoji and leads with the outcome, not the code.
- Missing a number that would make the case? Ask the dev for it, one question at a time, then stop and wait.
- Stay platform agnostic: plain markdown, mentions as `@Full Name` for the dev to turn into native tags.
- Thank every collaborator found in tickets, PRs, reviews or commits, except the dev; never invent one.
- Never accept a screenshot that shows customer data (names, emails, phones, order or payment IDs, card data); ask to blur it first.

## Decision Gates

Use whatever data tools are connected (MCP servers, CLIs, connectors). Examples are illustrative, not required.

| Situation | Action |
|-----------|--------|
| Win touches traffic, conversion, SEO | Query web analytics or search console (e.g. GA4, Plausible, Adobe) for before vs after |
| Win touches errors or stability | Query error tracking (e.g. Sentry, Datadog, Bugsnag) for volume and affected users |
| Win touches performance | Query performance monitoring (e.g. Lighthouse, SpeedCurve, DebugBear) for Core Web Vitals deltas |
| Win touches revenue or business KPIs | Query BI or the warehouse (e.g. BigQuery, Snowflake, Tableau, Looker, Metabase) |
| No tool connected, or it needs auth or fails | Ask the dev for the figure or a screenshot |
| No measurable impact exists | Sell scope instead: users, pages, markets, risk avoided, time saved |

| Level | Tone | Emojis | Length |
|-------|------|--------|--------|
| `humble` | Professional, understated, no superlatives | 1 to 2 total | 3 bullets, ~50 words |
| `hype` (default) | Upbeat, confident | 1 per bullet | 5 bullets, ~80 words |
| `legendary` | Heroic verbs, keynote closing | Generous | 5 bullets, ~100 words |
| `buzz` | Parody. Buzz Lightyear levels of excitement plus LinkedIn clichés (see template) | Maximum | 5 bullets, ~120 words |

`buzz` is the explicit satire mode: laugh with it, not at anyone. It stays truthful, the volume goes to 11 but the numbers never move.

## Execution Steps

1. Read the win from the dev's message, branch, commits, PRs or linked tickets (any tracker the dev points to).
2. Identify the outcome, the audience (leadership by default), the epic level, the output language and the collaborators.
3. Pick data sources from the gates; fetch before/after windows of equal length.
4. Ask the dev for any missing figure that would strengthen the post; stop and wait.
5. Apply the spin vocabulary and template in `assets/post-template.md`, ending with the shoutout line.
6. Verify every number in the draft maps to a source; drop any that does not.
7. Write a screenshot brief (max 2) for the claims a picture proves best, using the brief format in the template.
8. When the dev shares a screenshot, check it shows what the brief asks and no customer data; report match, mismatch or what to blur.

## Output Contract

Return, in this order:
1. The post, ready to paste (plain markdown), with the shoutout line.
2. A `Sources` list: each number → tool, query window, or "provided by dev".
3. A `Screenshots` brief: per image, the claim it backs, where to capture it, what must be visible, what to blur.
4. One line suggesting the next data point that would make the next post even bigger. 🚀

## References

- `assets/post-template.md` — post skeleton, shoutout line, screenshot brief, spin vocabulary, epic levels, worked example.
