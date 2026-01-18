# Marketplace Registration

This document provides information for registering these skills in various AI skill/plugin marketplaces.

## Claude Code Marketplaces

### SkillsMP (skillsmp.com)

To submit to the universal skills marketplace:

1. Ensure your repository follows the SKILL.md standard
2. Submit via [skillsmp.com](https://skillsmp.com)
3. Tag with: `scientific-writing`, `research`, `narrative`, `ABT`, `environmental-science`

### Anthropic Skills Registry

This repository is structured for direct installation:

```bash
# Users can install via:
claude plugins install kangning-huang/science_narrative_skills
```

### CCPM (Claude Code Plugin Manager)

Submit to the CCPM registry:

1. Fork the CCPM registry repository
2. Add entry to the skills catalog
3. Submit pull request

### Community Registry (claude-plugins.dev)

Register at [claude-plugins.dev](https://claude-plugins.dev):

1. Add your GitHub repository URL
2. Provide metadata from `plugin.json`
3. Skills will be indexed automatically

## OpenAI Codex Registry

### Skills Catalog

Submit to [github.com/openai/skills](https://github.com/openai/skills):

1. Fork the repository
2. Add skill folder following their structure
3. Submit pull request

## Cross-Platform Compatibility

This repository uses the open SKILL.md standard, compatible with:

- Claude Code
- OpenAI Codex CLI
- Any tool supporting the SKILL.md format

## Metadata

```yaml
name: science_narrative_skills
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

## Installation URLs

### Direct Download
- English: `https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique.skill`
- Chinese: `https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique-zh.skill`

### Git Clone
```bash
git clone https://github.com/kangning-huang/science_narrative_skills.git
```
