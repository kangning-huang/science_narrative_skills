# Science Narrative Skills

Custom AI skills for evaluating scientific writing using the **And-But-Therefore (ABT)** storytelling framework from Randy Olson's book *"Houston, We Have a Narrative"*.

> **Multi-platform support**: Available for Claude, ChatGPT, Codex, Gemini, GitHub Copilot, Cursor, Windsurf, and more.

## Available Skills

### 1. `abt-narrative-critique` (English)
Evaluates research proposals and papers using the ABT framework. Calibrated for environmental science and urban climate research.

**Use cases:**
- Critique research proposal introductions/abstracts
- Assess whether a paper's framing is compelling for publication
- Get feedback on narrative structure of scientific writing
- Verify citations and check for proper source representation

### 2. `abt-narrative-critique-zh` (中文版)
Chinese language version with the same functionality.

**适用场景：**
- 评审研究提案的引言/摘要
- 评估论文框架是否适合发表
- 获取科学写作叙事结构的反馈
- 验证引用并检查来源表述

## Preview Skill Contents

Want to see what's inside before installing? All skill contents are available for preview:

### English Version (`abt-narrative-critique`)
- [Main skill instructions (SKILL.md)](abt-narrative-critique/SKILL.md)
- [Research proposal evaluation criteria](abt-narrative-critique/references/proposal-criteria.md)
- [Research paper evaluation criteria](abt-narrative-critique/references/paper-criteria.md)

### Chinese Version (`abt-narrative-critique-zh`)
- [主技能说明 (SKILL.md)](abt-narrative-critique-zh/SKILL.md)
- [研究提案评估标准](abt-narrative-critique-zh/references/proposal-criteria-zh.md)
- [研究论文评估标准](abt-narrative-critique-zh/references/paper-criteria-zh.md)

## What is the ABT Framework?

The ABT framework structures scientific narratives as:
- **AND**: Establishes what we know (context, cited literature)
- **BUT**: Identifies the critical gap (tension, problem)
- **THEREFORE**: Proposes the solution (methods, results, contributions)

These skills analyze your scientific writing to ensure:
1. Strong foundational context with proper citations
2. Clear, significant knowledge gaps
3. Appropriate methods that address the identified gaps
4. Proper citation verification and credibility assessment

## Installation

Choose your platform below. All platforms use the same underlying skill instructions.

---

### 🤖 Claude Platforms

<details>
<summary><strong>Claude.ai (Web Interface)</strong></summary>

1. **Download the skill file:**
   - For English: Download [`abt-narrative-critique.skill`](https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique.skill)
   - For Chinese: Download [`abt-narrative-critique-zh.skill`](https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique-zh.skill)

2. **Upload to Claude.ai:**
   - Go to [claude.ai](https://claude.ai)
   - Click on the **user menu** (bottom left corner)
   - Select **"Skills"**
   - Click **"Upload skill"**
   - Select the downloaded `.skill` file
   - The skill will now be available in your Skills library

3. **Use the skill:**
   - Start a new conversation
   - Click the **Skills button** (bottom left)
   - Select `abt-narrative-critique` or `abt-narrative-critique-zh`
   - Paste your research proposal or paper introduction/abstract
   - Ask Claude to evaluate it

</details>

<details>
<summary><strong>Claude Code CLI</strong></summary>

#### Option A: Install via Plugin Marketplace

```bash
# 1. Add this repository as a marketplace
/plugin marketplace add kangning-huang/science_narrative_skills

# 2. Install the skills plugin
/plugin install science-narrative-skills@science_narrative_skills
```

Or using the CLI directly:
```bash
claude plugin marketplace add kangning-huang/science_narrative_skills
claude plugin install science-narrative-skills@science_narrative_skills --scope user
```

#### Option B: Manual Download (Recommended for quick setup)

```bash
# Create skills directory and download
mkdir -p ~/.claude/skills/abt-narrative-critique/references

# Download English skill files
curl -o ~/.claude/skills/abt-narrative-critique/SKILL.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique/SKILL.md
curl -o ~/.claude/skills/abt-narrative-critique/references/proposal-criteria.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique/references/proposal-criteria.md
curl -o ~/.claude/skills/abt-narrative-critique/references/paper-criteria.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique/references/paper-criteria.md

# Optional: Download Chinese version
mkdir -p ~/.claude/skills/abt-narrative-critique-zh/references
curl -o ~/.claude/skills/abt-narrative-critique-zh/SKILL.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique-zh/SKILL.md
curl -o ~/.claude/skills/abt-narrative-critique-zh/references/proposal-criteria-zh.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique-zh/references/proposal-criteria-zh.md
curl -o ~/.claude/skills/abt-narrative-critique-zh/references/paper-criteria-zh.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique-zh/references/paper-criteria-zh.md
```

**Use the skill:**
```bash
claude
# Then invoke with: /abt-narrative-critique
```

</details>

<details>
<summary><strong>Claude Cowork (VS Code Extension)</strong></summary>

1. **Download the skill file** (same as Claude.ai method above)

2. **Install the skill:**
   - Open VS Code with Claude Cowork extension installed
   - Open the Command Palette (`Cmd+Shift+P` on Mac, `Ctrl+Shift+P` on Windows/Linux)
   - Type: `Claude: Manage Skills`
   - Click **"Upload skill"**
   - Select the downloaded `.skill` file

3. **Use the skill:**
   - Open a Claude chat in VS Code
   - Type `/skills` to see available skills
   - Select `abt-narrative-critique` or use `/abt-narrative-critique` to invoke it
   - Provide your text for evaluation

</details>

---

### 🟢 OpenAI Platforms

<details>
<summary><strong>OpenAI Codex CLI</strong></summary>

Codex CLI uses the same SKILL.md format as Claude Code.

```bash
# Create skills directory
mkdir -p ~/.codex/skills/abt-narrative-critique

# Download the skill
curl -o ~/.codex/skills/abt-narrative-critique/SKILL.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique/SKILL.md

# Download reference files
mkdir -p ~/.codex/skills/abt-narrative-critique/references
curl -o ~/.codex/skills/abt-narrative-critique/references/proposal-criteria.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique/references/proposal-criteria.md
curl -o ~/.codex/skills/abt-narrative-critique/references/paper-criteria.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique/references/paper-criteria.md
```

**Use the skill:**
```bash
codex
# Explicit invocation: $abt-narrative-critique
# Or let Codex auto-select based on your prompt
```

See [OpenAI Codex Skills Documentation](https://developers.openai.com/codex/skills/) for more details.

</details>

<details>
<summary><strong>ChatGPT Custom GPT</strong></summary>

Create a Custom GPT using these instructions:

1. Go to [ChatGPT](https://chat.openai.com) → **Explore GPTs** → **Create**

2. **Configure your GPT:**
   - **Name:** ABT Narrative Critique
   - **Description:** Evaluate research proposals and papers using the And-But-Therefore storytelling framework
   - **Instructions:** Copy the content from [`platforms/chatgpt/instructions.md`](platforms/chatgpt/instructions.md)

3. **Optional - Add Knowledge:**
   - Upload [`platforms/chatgpt/proposal-criteria.md`](platforms/chatgpt/proposal-criteria.md)
   - Upload [`platforms/chatgpt/paper-criteria.md`](platforms/chatgpt/paper-criteria.md)

4. **Capabilities:** Enable "Web Browsing" for citation verification

5. Click **Create** and start using your GPT

</details>

---

### 🔵 Google Platforms

<details>
<summary><strong>Gemini Gems</strong></summary>

Create a custom Gem for ABT critique:

1. Go to [gemini.google.com/gems/create](https://gemini.google.com/gems/create)

2. **Configure your Gem:**
   - **Name:** ABT Narrative Critique
   - **Instructions:** Copy the content from [`platforms/gemini/gem-instructions.md`](platforms/gemini/gem-instructions.md)

3. Click **"Use Gemini to re-write instructions"** to expand the prompt (optional)

4. **Save** your Gem

**Tip:** Gems can link to your Google Drive. Upload the reference criteria files to Drive and reference them in your Gem.

See [Google's Gem creation guide](https://support.google.com/gemini/answer/15235603) for more details.

</details>

---

### 💻 IDE Integrations

<details>
<summary><strong>GitHub Copilot</strong></summary>

Add custom instructions for Copilot:

1. Create `.github/copilot-instructions.md` in your repository:
```bash
mkdir -p .github
curl -o .github/copilot-instructions.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/platforms/github-copilot/copilot-instructions.md
```

2. **Enable instruction files** in VS Code:
   - Open Settings → search for `github.copilot.chat.codeGeneration.useInstructionFiles`
   - Enable it

3. Use Copilot Chat to evaluate your scientific writing

See [GitHub Copilot Custom Instructions](https://docs.github.com/copilot/customizing-copilot/adding-custom-instructions-for-github-copilot) for more details.

</details>

<details>
<summary><strong>Cursor IDE</strong></summary>

Add rules for Cursor AI:

1. Create the rules directory and file:
```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/abt-narrative-critique.mdc \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/platforms/cursor/abt-narrative-critique.mdc
```

2. The rule will auto-activate when you ask about scientific writing evaluation

See [Cursor Rules Documentation](https://docs.cursor.com/context/rules) for more details.

</details>

<details>
<summary><strong>Windsurf IDE</strong></summary>

Add rules for Windsurf/Codeium:

1. Create the rules directory and file:
```bash
mkdir -p .windsurf/rules
curl -o .windsurf/rules/abt-narrative-critique.md \
  https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/platforms/windsurf/abt-narrative-critique.md
```

2. The rule will be available in your Windsurf sessions

See [Windsurf Rules Directory](https://windsurf.com/editor/directory) for more details.

</details>

---

### 🌐 Other Platforms

<details>
<summary><strong>Qwen (通义千问)</strong></summary>

For Alibaba's Qwen assistant, use the instructions as a system prompt:

1. Copy the content from [`platforms/qwen/system-prompt.md`](platforms/qwen/system-prompt.md) (Chinese) or [`platforms/qwen/system-prompt-en.md`](platforms/qwen/system-prompt-en.md) (English)

2. Paste into Qwen's custom instructions or system prompt field

3. For Qwen API users, include the instructions in the `system` role message

</details>

<details>
<summary><strong>Any LLM with System Prompts</strong></summary>

The core instructions work with any LLM that supports system prompts or custom instructions:

1. Use [`platforms/generic/system-prompt.md`](platforms/generic/system-prompt.md) as your system prompt
2. Optionally include the reference criteria files for domain-specific guidance

**Tested with:** LLaMA, Mistral, Phi, DeepSeek, Yi, and other open-source models.

</details>

## Usage Examples

### Example 1: Evaluate a Research Proposal

```
Please use the ABT framework to critique the following research proposal introduction:

[Paste your introduction text here]
```

### Example 2: Assess a Paper Abstract

```
I'm submitting a paper to Nature Climate Change. Can you evaluate whether the abstract
has a compelling narrative structure?

[Paste your abstract here]
```

### Example 3: Check Citation Quality

```
Please verify the citations in this introduction and check if they accurately represent
the source material:

[Paste your introduction with citations]
```

## What You'll Get

The skills provide:

1. **Overall Verdict**: Assessment of narrative strength
2. **AND Section Analysis**: Evaluation of context and literature framing
3. **BUT Section Analysis**: Assessment of knowledge gap clarity and significance
4. **THEREFORE Section Analysis**: Evaluation of method-gap fit and implications
5. **Citation Verification**: Checks for citation accuracy and credibility
6. **Severity Assessment**: Classification of issues as Fatal/Significant/Minor
7. **Actionable Recommendations**: Specific suggestions for improvement

## Domain Calibration

These skills are calibrated for **environmental science and urban climate research**, with awareness of:
- Typical citation patterns (20-40 references in papers, 8-15 key works in introductions)
- Essential foundational literature (e.g., Oke, Stewart & Oke LCZ framework)
- Common pitfalls (scale mismatches, confusing observational vs. modeling studies)
- Interdisciplinary framing expectations

While optimized for this domain, the skills can be useful for evaluating scientific writing in related fields.

## Citation & Attribution

These skills implement the ABT (And-But-Therefore) framework from:

**Olson, R. (2015). *Houston, We Have a Narrative: Why Science Needs Story*. University of Chicago Press.**

## Marketplace & Registry

This repository supports Claude Code plugin marketplace installation:

```bash
# Add as a marketplace
/plugin marketplace add kangning-huang/science_narrative_skills

# Install the plugin
/plugin install science-narrative-skills@science_narrative_skills
```

| Platform | Installation Method |
|----------|---------------------|
| Claude Code | Plugin marketplace (see above) or manual download |
| [OpenAI Codex](https://github.com/openai/skills) | Compatible SKILL.md format |
| Other platforms | See platform-specific instructions above |

See [MARKETPLACE.md](MARKETPLACE.md) for detailed registration information.

## File Structure

```
science_narrative_skills/
├── README.md                    # This file
├── MARKETPLACE.md               # Marketplace registration info
├── .claude-plugin/              # Claude Code plugin config
│   ├── plugin.json              # Plugin manifest
│   └── marketplace.json         # Marketplace definition
├── skills/                      # Skills directory (for plugin)
│   ├── abt-narrative-critique/  # → symlink to source
│   └── abt-narrative-critique-zh/
├── abt-narrative-critique.skill # English skill (Claude.ai upload)
├── abt-narrative-critique-zh.skill # Chinese skill (Claude.ai upload)
├── abt-narrative-critique/      # Source files (English)
│   ├── SKILL.md
│   └── references/
├── abt-narrative-critique-zh/   # Source files (Chinese)
│   ├── SKILL.md
│   └── references/
└── platforms/                   # Platform-specific configs
    ├── chatgpt/                 # ChatGPT Custom GPT
    ├── gemini/                  # Gemini Gems
    ├── github-copilot/          # GitHub Copilot
    ├── cursor/                  # Cursor IDE
    ├── windsurf/                # Windsurf/Codeium
    ├── qwen/                    # Qwen (Chinese & English)
    └── generic/                 # Any LLM system prompt
```

## License

MIT License - Feel free to use, modify, and share.

## Contributing

Found a bug or have suggestions? Please open an issue or submit a pull request.

**Adding new platform support:**
1. Create a directory under `platforms/` with your platform name
2. Add the appropriate instruction/config file
3. Update this README with installation instructions
4. Submit a pull request

## Author

Created by Kangning Huang for use in research writing evaluation and pedagogy.
