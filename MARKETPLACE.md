# Marketplace & Distribution

This document provides information for installing and distributing these skills across various AI platforms.

## Claude Code Plugin Installation

This repository is structured as a Claude Code plugin marketplace.

### For Users: Installing the Plugin

```bash
# Step 1: Add this repository as a marketplace
/plugin marketplace add kangning-huang/science_narrative_skills

# Step 2: Install the skills plugin
/plugin install science-narrative-skills@science_narrative_skills
```

Or using the CLI directly:
```bash
claude plugin marketplace add kangning-huang/science_narrative_skills
claude plugin install science-narrative-skills@science_narrative_skills --scope user
```

### Manual Installation (Alternative)

Copy the skill folders to your Claude Code skills directory:

```bash
# Personal skills (available in all projects)
cp -r abt-narrative-critique ~/.claude/skills/
cp -r abt-narrative-critique-zh ~/.claude/skills/

# Or project-specific skills
cp -r abt-narrative-critique .claude/skills/
```

## Plugin Structure

This repository follows the Claude Code plugin format:

```
.claude-plugin/
├── plugin.json          # Plugin manifest
└── marketplace.json     # Marketplace definition

skills/
├── abt-narrative-critique/      # English skill
│   ├── SKILL.md
│   └── references/
└── abt-narrative-critique-zh/   # Chinese skill
    ├── SKILL.md
    └── references/
```

## OpenAI Codex CLI

This repository uses the SKILL.md standard, which is compatible with OpenAI Codex CLI.

```bash
# Copy to Codex skills directory
cp -r abt-narrative-critique ~/.codex/skills/
```

## Cross-Platform Compatibility

The SKILL.md format is an open standard compatible with:

- Claude Code
- OpenAI Codex CLI
- Any tool supporting the SKILL.md format

## Metadata

```yaml
name: science-narrative-skills
version: 1.0.0
author: Kangning Huang
license: MIT
homepage: https://github.com/kangning-huang/science_narrative_skills
categories:
  - scientific-writing
  - research-tools
  - academic
languages:
  - en
  - zh
```

## Direct Download URLs

### Claude.ai (.skill files)
- English: `https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique.skill`
- Chinese: `https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique-zh.skill`

### SKILL.md Files
- English: `https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique/SKILL.md`
- Chinese: `https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique-zh/SKILL.md`

### Git Clone
```bash
git clone https://github.com/kangning-huang/science_narrative_skills.git
```
