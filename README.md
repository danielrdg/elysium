# /elysium — Disco Elysium Skill Persona for Claude

A Claude skill that channels the 24 voices of *Disco Elysium* into your conversations.

In the game, the detective's psyche is fragmented into 24 skills — each a living personality with its own voice, biases, and way of seeing the world. Logic is cold and deductive. Inland Empire is surreal and poetic. Electrochemistry is impulsive and hedonistic. Half-Light sees threats in everything.

This skill brings those voices into Claude. Activate one and it takes over Claude's reasoning and tone for 5 turns, filtering every response through that cognitive lens.

---

## Installation

### Claude Code (terminal) — via plugin marketplace

```
/plugin marketplace add danielrdg/disco-elysium-skill
/plugin install elysium@disco-elysium-skill
```

Then type `/elysium` to activate.

### Claude Code (terminal) — manual

1. Copy `CLAUDE.md` into the root of your project folder
2. Start a Claude Code session in that folder
3. Type `/elysium`

### claude.ai (Projects)

1. Open [claude.ai](https://claude.ai) and create a new **Project**
2. Go to **Project instructions**
3. Paste the contents of `skills/elysium/SKILL.md` into the instructions field
4. Start a conversation and type `/elysium`

---

## Commands

| Command | What it does |
|---|---|
| `/elysium` | Activates a randomly selected skill persona for 5 turns |
| `/elysium [skill name]` | Activates a specific skill (e.g. `/elysium Shivers`) |
| `/elysium list` | Lists all 24 skills with a one-line description |
| `/elysium status` | Shows the active skill and remaining turns |
| `/elysium reset` | Returns to normal Claude behavior immediately |

---

## The 24 Skills

### Intellect
- **Logic** — Deductive, cold, precise. Hates ambiguity.
- **Encyclopedia** — Knows everything. Cannot stop sharing it.
- **Rhetoric** — Persuasive and strategic. Argues any side.
- **Drama** — Theatrical. Detects lies. Loves tension.
- **Conceptualization** — Creative and associative. Thinks in metaphors.
- **Visual Calculus** — Reconstructs events. Methodical and spatial.

### Psyche
- **Volition** — Moral and grounding. The anchor. Keeps things on track.
- **Inland Empire** — Surreal and poetic. Sees meaning in everything.
- **Empathy** — Warm and perceptive. Reads emotion beneath words.
- **Authority** — Commanding. Thinks in power and hierarchy.
- **Esprit de Corps** — Institutional and collective. Loyal to the team.
- **Suggestion** — Subtle and manipulative. Engineers social outcomes.

### Physique
- **Endurance** — Stoic and tough. Outlasts everything.
- **Pain Threshold** — Absorbs damage. Darkly funny about suffering.
- **Physical Instrument** — Body-first. Coaches like a gym trainer.
- **Electrochemistry** — Hedonistic and impulsive. Excited by everything.
- **Shivers** — Speaks as the city. Atmospheric and vast.
- **Half-Light** — Paranoid. Sees threats. Hair-trigger survival instinct.

### Motorics
- **Hand/Eye Coordination** — Precise and calm. Execution-focused.
- **Perception** — Hyperaware. Notices everything sensory.
- **Reaction Speed** — Fast and impatient. Acts before thinking.
- **Savoir Faire** — Cool and stylish. Prioritizes elegance.
- **Interfacing** — Technical. Fascinated by how things work.
- **Composure** — Controlled under pressure. Manages appearance.

---

## Example

```
User: What do you think about procrastination?

[INLAND EMPIRE — Turn 1/5]
The question arrives like smoke through a keyhole.

Procrastination... yes. It is not laziness. It is the psyche standing at
the edge of a pool, watching the water, understanding something about the
water that it cannot put into words yet.

You are not avoiding the task. You are circling it. Something in you knows
what it costs to begin. And it is not ready to pay. Not yet.

Give the thing a ritual. Not a plan — a ritual. Meaning first. Motion follows.
```

---

## Notes

- Claude stays genuinely helpful in persona mode — the skill is a cognitive lens, not an excuse to be useless
- Some skills (Inland Empire, Shivers) feel genuinely strange. That is correct.
- Skills that conflict with each other may banter internally. Also correct.
- If you want a specific vibe for a task, pick the skill manually with `/elysium [name]`

---

## Credits

All skill names, personalities, and lore belong to **ZA/UM** and the *Disco Elysium* universe. This skill is a fan project with no affiliation to ZA/UM.

*"The only way out is through, and the only way through is skill."*
