# Idea to Action — a Claude skill

A staged thinking partner that takes someone from a raw idea → a tangible prototype → a tested concept, using the Fluid Intelligence **"From Ideas to Action"** methodology. It moves through five steps — **Frame → Ideate → Prototype → Iterate → Reflect** — and enforces a divergence-then-convergence rhythm at every stage so you never collapse to a single answer too early.

Use it when you're sitting between vision and execution: "I have a few ideas," "help me turn this into a prototype," "I'm stuck between ideas," "how do I move this forward."

This repo ships the skill **two ways**: as an installable Claude Code **plugin** (via a marketplace) and as a **plain skill** you can copy in manually.

---

## Option A — Install as a Claude Code plugin (recommended)

This is the one-command path and keeps the skill updated via the marketplace.

```bash
# 1. Add this repo as a marketplace
/plugin marketplace add ramchandmatta/idea-to-action-skill

# 2. Install the plugin
/plugin install idea-to-action@fluid-intelligence
```

To update later, after new commits are pushed:

```bash
/plugin marketplace update fluid-intelligence
```


---

## Option B — Install the skill manually

Copy the skill folder into your personal skills directory.

```bash
# Clone the repo
git clone https://github.com/ramchandmatta/idea-to-action-skill.git

# Copy the skill into your personal Claude skills folder
mkdir -p ~/.claude/skills/idea-to-action
cp idea-to-action-skill/plugins/idea-to-action/skills/idea-to-action/SKILL.md \
   ~/.claude/skills/idea-to-action/SKILL.md
```

Restart Claude Code (or run `/doctor`) and the skill is available as `/idea-to-action`.

For a single project instead of globally, copy to `<project>/.claude/skills/idea-to-action/SKILL.md`.

There's also a packaged `idea-to-action.skill` (a zip of the skill folder) attached for environments that accept a "Save skill" / install-from-file flow.

---

## What's inside

```
idea-to-action-skill/
├── .claude-plugin/
│   └── marketplace.json          # marketplace manifest (lists the plugin)
├── plugins/
│   └── idea-to-action/
│       ├── .claude-plugin/
│       │   └── plugin.json        # plugin manifest
│       └── skills/
│           └── idea-to-action/
│               └── SKILL.md       # the skill itself
├── README.md
└── LICENSE                        # MIT
```

## How the skill behaves

The skill is deliberately opinionated. It will:

- Make **you** own every decision — it surfaces options and tradeoffs but never picks for you.
- Insist on **diverging before converging** at each stage.
- Treat prototypes as **props for learning** ("build to think, not to ship").
- Refuse to skip stages — the skipped step is usually why a prototype fails later.

## License

Released under the [MIT License](./LICENSE) — anyone is free to use, modify, and distribute it.
