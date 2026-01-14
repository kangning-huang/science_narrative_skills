# Science Narrative Skills

Custom Claude skills for evaluating scientific writing using the **And-But-Therefore (ABT)** storytelling framework from Randy Olson's book *"Houston, We Have a Narrative"*.

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

### For Claude.ai (Web Interface)

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

### For Claude Code CLI

1. **Download the skill file:**
   ```bash
   # Navigate to your skills directory
   cd ~/.claude/skills

   # Download English version
   curl -O https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique.skill

   # Download Chinese version (optional)
   curl -O https://raw.githubusercontent.com/kangning-huang/science_narrative_skills/main/abt-narrative-critique-zh.skill
   ```

2. **Verify installation:**
   ```bash
   # List available skills
   claude skills list
   ```

   You should see `abt-narrative-critique` (and `abt-narrative-critique-zh` if you downloaded it) in the list.

3. **Use the skill:**
   ```bash
   # Start Claude Code and invoke the skill
   claude

   # In the conversation, use the skill:
   # /abt-narrative-critique
   # Then paste your text or provide a file path
   ```

### For Claude Cowork (VS Code Extension)

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

## License

MIT License - Feel free to use, modify, and share.

## Contributing

Found a bug or have suggestions? Please open an issue or submit a pull request.

## Author

Created by Kangning Huang for use in research writing evaluation and pedagogy.
