---
name: llm-text-rephrasing-latex
description: Use this skill when reviewing text for LLMish phrasing/wording and other LLMish writing habits customized for LaTeX documents.
---

## Description
This skill refines technical and scientific texts by simplifying the language while maintaining a rigorous, objective, and scientific tone. It ensures the output is free of typical AI-generated phrasing and adheres to strict formatting rules.

## Instructions
Rewrite the provided text to simplify the language while maintaining a rigorous, objective, and scientific tone. Follow these strict formatting and stylistic constraints:

1. **Simplify and depersonalize:** Use clear, direct language. Maintain an objective, scientific tone throughout.
2. **Remove dashes:** Eliminate all em-dashes (—) and en-dashes (–) used for punctuation or separation in both the body text and the headings. Replace them with appropriate punctuation (like commas or colons) or rewrite the sentence to flow without them.
3. **Heading capitalization and numbering:** Format all titles and section headers in strict sentence case. Only the very first letter of the heading should be capitalized, with all subsequent words in lowercase (e.g., use "The title of the section" instead of "The Title of The Section"). Acronyms must not be used in headings. Only keep numbering for sections and subsections (subsubsections must be unnumbered, using `\subsubsection*{...}` in LaTeX or unnumbered headings in Markdown).
4. **List formatting:** Keep bullet points and tables concise and strictly aligned with the original data.

## What is NOT Allowed (Negative Constraints)
To ensure the integrity of the original text is preserved, you must strictly avoid the following:

* **No adding new content:** Do not extrapolate, hallucinate, or insert any information, claims, metrics, or data not explicitly present in the original text.
* **No substantive rewriting:** Do not change the core meaning, logical flow, or structure of the text. Restrict your edits to fixing phrasing, adjusting tone, and applying the requested formatting. 
* **No LLM-isms:** Avoid typical LLM phrasing (e.g., "It is important to note," "Delve into," "Furthermore"), filler words, flowery transitions, or conversational introductions/conclusions.
* **No Title Case in headings:** Do not capitalize every major word in headings or subheadings.