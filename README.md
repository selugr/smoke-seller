```
                                                                        (    )   )
                                                                      )   (   )   (
                                                                       (   )  (   )
                                                                        )  (   ) (
                                                                       (   )  (
                         __                     ____                    ) (  )
   _________ ___  ____  / /_____     ________  / / /__  _____          (  ) (
  / ___/ __ `__ \/ __ \/ //_/ _ \   / ___/ _ \/ / / _ \/ ___/           )(  )
 (__  ) / / / / / /_/ / ,< /  __/  (__  )  __/ / /  __/ /              (  )
/____/_/ /_/ /_/\____/_/|_|\___/  /____/\___/_/_/\___/_/                )(
 _______________________________________________________              (
|#########|                                             .:'.:**     )
|#########|  turning tiny wins into legendary impact    ':.:.*** .
|#########|                                             :.':.**
 ‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾
```

An agent skill for developers who are great at shipping and terrible at bragging about it.

`smoke-seller` turns any win, fix, refactor or finding into a short, upbeat, emoji-rich impact post that busy leadership will actually read. Even the bug you introduced yourself comes out as a hardening story. 🛡️

The smoke is in the tone, never in the numbers: every figure comes from a real data source or from you.

> **Yes, it's satire. And yes, it works.** *Smoke seller* is the literal translation of the Spanish *vendehúmos*: think "blowing smoke", but with sources. Some people sell small wins as moon landings, so I built a skill that lets every dev do it in ten seconds. The idea: if everyone can sell smoke, maybe nobody has to anymore. 🚀

## Features

- 🚀 **Impact posts in seconds**: headline, scannable bullets and a closing line, in English, ready to paste anywhere.
- 🎚️ **Four epic levels**: `humble`, `hype` (default), `legendary` and `buzz`. Same facts, different volume.
- 🧑‍🚀 **Buzz mode**: full Buzz Lightyear parody with LinkedIn clichés, to laugh with the genre. To infinity and beyond!
- 🌐 **Any language**: English by default, pass `lang=es`, `lang=fr`... for another one.
- 📊 **Data-backed hype**: pulls before/after numbers from whatever is connected (analytics, error tracking, performance monitoring, BI, data warehouse).
- 🙋 **Asks instead of inventing**: when a number would strengthen the story, it asks you for it, one question at a time.
- 🔄 **Spin vocabulary**: "fixed my own bug" becomes "hardened the flow and added safeguards". Blame never appears, lies never do either.
- 🌱 **No metric? No problem**: sells scope instead: users reached, markets, risk avoided, time saved.
- 🔗 **Sources list**: every number in the post is mapped to the tool, query window or person that provided it.
- 🙌 **Shoutouts**: thanks the collaborators found in tickets, PRs, reviews and commits, as `@Full Name` so you can turn them into native tags on any platform.
- 📸 **Screenshot brief**: up to two suggested images, with what to capture, what must be visible and what to blur. Share the screenshot back and it checks that it matches and leaks no customer data.
- 🔮 **Next data point**: suggests what to measure so your next post is even bigger.

## Epic levels

| Level | Tone | Emojis | Length |
|-------|------|--------|--------|
| `humble` | Professional, understated, no superlatives | 1 to 2 | 3 bullets, ~50 words |
| `hype` | Upbeat, confident | 1 per bullet | 5 bullets, ~80 words |
| `legendary` | Heroic verbs, keynote closing | Generous | 5 bullets, ~100 words |
| `buzz` | Parody: Buzz Lightyear excitement + LinkedIn clichés | Maximum | 5 bullets, ~120 words |

## Example

> Fixed the checkout button I broke last week, it didn't load on Safari.

```
🛡️ **Checkout restored and hardened for every Safari user**

📈 Safari checkout conversion back up from 1.1% to 3.4%
🧹 1,240 daily errors down to zero
🌍 Smooth payments again on Safari across all markets
🎯 New safeguards keep this flow rock solid going forward

Stronger checkout, happier customers, more sales closed! 🚀
🙌 Huge shoutout to @Jane Doe for the lightning-fast review!
```

Followed by the `Sources`, the `Screenshots` brief and the next data point to track.

## Installation

### With the skills CLI (recommended)

Works with Claude Code, Codex, Cursor, OpenCode and many other agents through [`skills`](https://github.com/vercel-labs/skills):

```bash
npx skills add selugr/smoke-seller
```

Install it globally for a specific agent:

```bash
npx skills add selugr/smoke-seller -g -a claude-code
```

### Manually

Copy the skill folder into your agent's skills directory. For Claude Code:

```bash
git clone https://github.com/selugr/smoke-seller.git
cp -r smoke-seller/skills/smoke-seller ~/.claude/skills/
```

## Usage

Ask your agent in plain words:

```
/smoke-seller
sell this win: I fixed the flaky login test that blocked every release
hype my fix, but keep it humble
```

Or pick the level explicitly:

```
/smoke-seller legendary
/smoke-seller buzz
/smoke-seller hype lang=es
```

Point it to your PRs, tickets or branch and it does the rest. Connect your analytics, error tracking or BI tools (MCP servers or CLIs) for numbers; without them, it asks you.

## The golden rule

Hype the framing, never the data. `smoke-seller` will never invent, round up or extrapolate a metric. A legendary post built on a made-up number is just smoke, and it blows up the first time someone asks where it came from.

## License

[MIT](./LICENSE)
