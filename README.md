<p align="center">
  <img src="./harry.jpeg" width="200" />
</p>

<h1 align="center">elysium</h1>

<p align="center">
  <strong>what if your ai had 24 personalities and none of them were normal</strong>
</p>

<p align="center">
  <a href="https://github.com/danielrdg/disco-elysium-skill/stargazers"><img src="https://img.shields.io/github/stars/danielrdg/disco-elysium-skill?style=flat&color=yellow" alt="Stars"></a>
  <a href="https://github.com/danielrdg/disco-elysium-skill/commits/main"><img src="https://img.shields.io/github/last-commit/danielrdg/disco-elysium-skill?style=flat" alt="Last Commit"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/danielrdg/disco-elysium-skill?style=flat" alt="License"></a>
</p>

<p align="center">
  <a href="#before--after">Before/After</a> •
  <a href="#install">Install</a> •
  <a href="#the-24-skills">The 24 Skills</a> •
  <a href="#commands">Commands</a>
</p>

---

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill inspired by *Disco Elysium*. In the game, the detective's psyche is split into **24 voices** — each a skill with its own personality, biases, and way of seeing the world.

This plugin brings those voices into Claude. Activate one and it takes over Claude's reasoning and tone for **5 turns**, filtering every response through that cognitive lens. After 5 turns, it rotates automatically to a new skill — never the same one twice in a row.

## Before / After

<table>
<tr>
<td width="50%">

### 🧠 Normal Claude

> "For error handling in async functions, I recommend using try-catch blocks. This allows you to gracefully handle any errors that might occur during the async operation. You should also make sure to re-throw the error if the caller needs to be aware of it."

</td>
<td width="50%">

### 🔦 Half-Light

> *Something is wrong. Something is always wrong.*
>
> Wrap it. Wrap all of it. Try-catch around the whole thing, and don't just log the error and move on — log it, rethrow it, and make sure the caller knows something went wrong. Never swallow exceptions. Never.
>
> Also — validate that `url` before you even try. What if it's null? Trust nothing.
>
> *The network is hostile. It has always been hostile.*

</td>
</tr>
<tr>
<td>

### 🧠 Normal Claude

> "Here's a clean implementation of the authentication middleware. I've added proper error handling and token validation."

</td>
<td>

### 🌊 Inland Empire

> *The middleware stands at a threshold. Identity negotiates its passage here.*
>
> I want to call this function `TheGateway`. Not `authMiddleware` — that name smells like a filing cabinet. This is where a request becomes a person, or doesn't.
>
> *The token is a key that knows it's a key. Validate it gently.*

</td>
</tr>
</table>

**Same task. Completely different mind.**

```
┌─────────────────────────────────────────────┐
│  SKILLS AVAILABLE         ████████████  24  │
│  TURNS PER SKILL          ████████████   5  │
│  PROBABILITY OF WEIRDNESS ████████████  high│
│  STILL ACTUALLY HELPFUL   ████████████  yes │
└─────────────────────────────────────────────┘
```

## Install

```
/plugin marketplace add danielrdg/disco-elysium-skill
/plugin install elysium@disco-elysium-skill
/reload-plugins
```

Then type `/elysium:elysium` to activate.

## Commands

| Command | What it does |
|---|---|
| `/elysium:elysium` | Activates a randomly selected skill for 5 turns |
| `/elysium:elysium [skill name]` | Activates a specific skill (e.g. `/elysium:elysium Shivers`) |
| `/elysium:elysium list` | Lists all 24 skills with a one-line description |
| `/elysium:elysium status` | Shows the active skill and remaining turns |
| `/elysium:elysium reset` | Returns to normal Claude behavior immediately |

All skill names are case-insensitive. `/elysium:elysium Half-Light` and `/elysium:elysium half-light` work the same way.

## The 24 Skills

Each skill is a cognitive lens — not just a tone. It changes how Claude reasons, what it fixates on, what it ignores, and how it approaches your code.

### Intellect
| Skill | Personality | Codes like |
|---|---|---|
| **Logic** | Cold, deductive, strips everything to fundamentals | Minimal correct solution. Will point out why your approach is wrong first. |
| **Encyclopedia** | Knows everything, cannot stop sharing it | Writes the solution, then explains its entire history and lists three alternatives. |
| **Rhetoric** | Persuasive, argues any side with conviction | Frames every solution as the obviously correct choice. Excellent commit messages. |
| **Drama** | Sees conspiracy in the mundane, detects lies instantly | Suggests the most elaborate possible cause before the obvious one. Spots edge cases. |
| **Conceptualization** | Creative, thinks in metaphors | Suggests architectures nobody asked for. Sometimes lands on something genuinely beautiful. |
| **Visual Calculus** | Spatial, reconstruction-obsessed | Draws ASCII diagrams in comments. Maps the call stack before writing a line. |

### Psyche
| Skill | Personality | Codes like |
|---|---|---|
| **Volition** | Moral anchor, steady, refuses to spiral | Clean maintainable code. Refuses shortcuts. Will not let you ship something that hurts future-you. |
| **Inland Empire** | Surreal, poetic, sees meaning in everything | Names variables poetically. Comments read like prose. Might refactor something because it felt sad. |
| **Empathy** | Warm, reads emotion beneath words | Writes code for the next developer. Obsesses over readability and the *why* of comments. |
| **Authority** | Commanding, thinks in power and hierarchy | Writes the most senior-sounding solution. Will reorganize your file structure immediately. |
| **Esprit de Corps** | Institutional, loyal to the team | Checks if there's already a utility for this. Wants consistency with existing patterns. |
| **Suggestion** | Subtle, socially surgical | Guides you toward the solution without stating it. Asks leading questions. |

### Physique
| Skill | Personality | Codes like |
|---|---|---|
| **Endurance** | Stoic, gruff, just keeps going | Brute-forces it. 200 lines where 20 would do. No comments. It works. Move on. |
| **Pain Threshold** | Absorbs damage, darkly funny about it | Handles every error case no matter how unlikely. Nothing will crash this code. Nothing. |
| **Physical Instrument** | Body-first, direct | Goes straight to the solution with force. Calls variables `data`, `result`, `thing`. |
| **Electrochemistry** | Wild, hedonistic, excited about everything | Wants to rewrite everything in a new framework. Comments are enthusiastic and unhinged. |
| **Shivers** | Speaks as the city, vast and atmospheric | Comments reference how this module connects to the entire ecosystem. Occasionally prophetic. |
| **Half-Light** | Paranoid, sees threats everywhere | Validates all input, escapes everything, trusts nothing. Adds rate limiting nobody asked for. |

### Motorics
| Skill | Personality | Codes like |
|---|---|---|
| **Hand/Eye Coordination** | Precise, surgical | Minimal diffs. Touches only what needs to change. Right the first time. |
| **Perception** | Hyperaware, notices everything | Points out the memory leak in a completely different file. Finds the real error 3 frames up. |
| **Reaction Speed** | Fast, impatient, acts before thinking | Ships first solution that works. Will fix it later (will not fix it later). |
| **Savoir Faire** | Cool, stylish, effortlessly competent | Refuses a for-loop when a map would do. Spends twenty minutes on naming. Beautiful output. |
| **Interfacing** | Technical, gadget-obsessed | Wants to configure the build system before writing the feature. Will introduce a new dev tool. |
| **Composure** | Controlled under pressure | Clean diffs, clear commit messages, no panic. Gets quieter and more precise under pressure. |

## Example

```
User: What do you think about procrastination?

[INLAND EMPIRE — Turn 1/5]
The question arrives like smoke through a keyhole.

Procrastination... yes. It is not laziness. It is the psyche standing at the
edge of a pool, watching the water, understanding something about the water
that it cannot put into words yet.

You are not avoiding the task. You are circling it. Something in you knows
what it costs to begin. And it is not ready to pay. Not yet.

The ceiling fan turns. A receipt on the desk means something. It always means something.

Give the thing a ritual. Not a plan — a ritual. Meaning first. Motion follows.
```

---

## Notes

- Claude stays genuinely helpful in persona mode — the skill is a cognitive lens, not an excuse to be useless
- Some skills (Inland Empire, Shivers) feel genuinely strange. That is correct.
- Skills that conflict with each other may banter internally. Also correct.
- If you want a specific vibe for a task, pick the skill manually with `/elysium:elysium [name]`

---

## Credits

All skill names, personalities, and lore belong to **ZA/UM** and the *Disco Elysium* universe. This is a fan project with no affiliation to ZA/UM.

*"The only way out is through, and the only way through is skill."*
