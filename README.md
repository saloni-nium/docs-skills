# docs-skills

AI-powered Claude Code skills for the Nium docs platform.

## Structure

```
docs-skills/
├── skills/
│   ├── contributor/   # Skills for product teams — create, edit, review, commit docs
│   └── promotion/     # Skills for DevEx — validate, branch, PR, stage, publish
│
├── knowledge/         # Reference material skills draw on
│   ├── nium-style-guide.md
│   ├── writing-principles.md
│   ├── docs-ia.md
│   └── docs-templates/
│
├── examples/          # Sample inputs and outputs for each skill
└── README.md
```

## Usage

Copy the skills you need into your project's `.claude/skills/` directory, then invoke them with `/skill-name` in Claude Code.
