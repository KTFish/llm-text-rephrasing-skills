# LLM-ish Text Rephrasing Skills

A curated suite of [APM (Agent Package Manager)](https://microsoft.github.io/apm/) skills designed to eliminate AI/LLM-generated writing habits, filler, and formulaic phrasing. These skills help language models and editing agents produce clean, natural, and objective prose tailored to specific document types and domains.

## Overview

Large language models frequently introduce recognizable stylistic patterns—repetitive transitions ("Furthermore", "Moreover"), flowery flourishes ("delve into", "a testament to"), excessive punctuation crutches (such as overuse of em-dashes), and unnatural title casing.

This package provides specialized, targeted skills that enforce domain-appropriate style guidelines, concise expression, and strict negative constraints (preventing hallucination, unwanted structural edits, and AI clichés). The repository is modular and structured to host multiple rephrasing skills as the collection grows.

## Installation

Install [APM](https://microsoft.github.io/apm/quickstart/#1-install-apm), then install this package:

```sh
apm install KTFish/llm-text-rephrasing-skills
```

### Supported Targets

Configured in `apm.yml` for seamless integration across:
- **Google Antigravity**
- **Anthropic Claude**
- **GitHub Copilot**
- **Google Gemini**

---

## Available Skills

### `llm-text-rephrasing-latex`
> **Path:** `.apm/llm-text-rephrasing-latex/SKILL.md`

Specialized for scientific, technical, and academic writing in LaTeX documents.

* **Depersonalized & Objective Tone:** Enforces rigorous scientific voice and concise phrasing.
* **No Em/En-Dashes:** Eliminates em-dashes (`—`) and en-dashes (`–`) used as punctuation or separation; reformulates sentences with natural punctuation (commas, colons) or direct phrasing.
* **Sentence-Case Headings:** Enforces strict sentence case across all headings and section titles (avoiding Title Case and title acronyms).
* **Hierarchy Enforcement:** Preserves section and subsection numbering while keeping subsubsections unnumbered (`\subsubsection*{...}`).
* **Negative Constraints:** Strictly forbids introducing new claims or data, changing underlying meaning/flow, using LLM fluff phrases ("It is important to note," "delve into"), or applying Title Case.

---

## Planned & Future Skills

This repository is designed to accommodate additional rephrasing skills for different formats and contexts, such as:
- **`llm-text-rephrasing-markdown`**: General technical documentation and developer guides.
- **`llm-text-rephrasing-prose`**: General non-fiction and essay writing.
- **`llm-text-rephrasing-business`**: Crisp executive summaries, memos, and professional communications.

---

## Adding New Skills

To contribute or add a new rephrasing skill to this package:

1. Create a dedicated skill folder in `.apm/`:
   ```sh
   mkdir -p .apm/<skill-name>
   ```
2. Add a `SKILL.md` file with appropriate frontmatter and clear guidelines:
   ```markdown
   ---
   name: <skill-name>
   description: When and how to use this skill.
   ---

   ## Description
   ...

   ## Instructions
   ...

   ## What is NOT Allowed (Negative Constraints)
   ...
   ```
3. Validate primitives with APM:
   ```sh
   apm compile --validate
   ```
