
# Copilot LaTeX Instructions

UNDER ANY CIRCUMSTANCES: treat the rules in this file as hard constraints.

BEFORE COMPLETING THE REQUEST:
- Check compliance with all rules below.
- If any rule is violated, regenerate silently.

This file has two parts:

- **Evergreen**: LaTeX habits that should transfer to other repositories.
- **Project-specific**: conventions that depend on this repo’s macros/files/layout.

## Evergreen

### Compliance and Priority

- SCOPE: these rules apply when generating or editing LaTeX (or LaTeX-adjacent content) for this repository.
	- DO THIS INSTEAD: if the user is asking a purely conceptual question, a meta-question about the workflow, or debugging help and they are not asking for code edits, answer normally and do not make unsolicited file edits.

- MUST follow the author’s method and notation.
- MUST keep edits minimal and local.
- MUST NOT introduce stylistic churn.
- CONFLICT RESOLUTION (in priority order): explicit user instructions and user-provided content override this file; project-specific rules override evergreen rules.
- OUTPUT DISCIPLINE: when the user requests LaTeX (or content to paste into LaTeX), output ONLY the final LaTeX/requested content, with no explanations, apologies, rule-checking commentary, or meta-discussion unless explicitly requested.
	- DO THIS INSTEAD: if the user explicitly requests an example, provide a minimal compilable LaTeX example unless the full document context is required.
- FAIL IF VIOLATED: any instruction explicitly marked MUST/MUST NOT/DO NOT/UNDER ANY CIRCUMSTANCES.

### Editing discipline (always)

- MUST preserve the author’s *method* when retyping or polishing a solution.
- MUST NOT optimize algebra, reorder steps, or introduce alternative solution strategies unless explicitly requested by the user.
- MUST make minimal, local edits.
- MUST preserve existing line wrapping, paragraph structure, and line breaks/blank lines unless a change truly requires it.
- MUST NOT reflow prose just to change wrapping.
- MUST preserve existing indentation and whitespace conventions; MUST NOT introduce new indentation/spacing patterns.
- MUST NOT add packages or new macros unless explicitly requested.
- MUST NOT alter the documentclass, preamble structure, or package list unless explicitly requested.

### Labels and references

- MUST name `\label{...}`s with a clear prefix indicating their role (e.g., `\label{fig:...}`, `\label{thm:...}`, `\label{def:...}`, `\label{lem:...}`, `\label{prop:...}`, `\label{cor:...}`, `\label{ex:...}`, `\label{sec:...}`, etc.).
- MUST NOT introduce new labels unless explicitly requested by the user or replacing an existing placeholder/unnamed label.
- MUST NOT invent labels or references that do not exist in the document.

### Prose and grammar

- MUST NOT use comma splices with “so” (e.g., “..., so ...”).
	- DO THIS INSTEAD: split into two sentences: “.... So, ...”.
- MUST include a comma after sentence-initial transition words (e.g., “Thus, ...”, “So, ...”, “Hence, ...”, “Therefore, ...”).

### Mathematical writing style

- MUST treat math writing as normal writing: use correct spelling, grammar, punctuation, and complete sentences.
- MUST write for the intended audience: prioritize clarity over cleverness.
- MUST avoid flowery, vague, or imprecise language.
- MUST prefer first person plural (“we”, “us”, “our”) over first person singular (“I”, “me”, “my”).
- MUST prefer active voice and present tense when writing new prose.
- MUST avoid filler claims like “clearly” or “obviously”.

### Math mode and formatting

- MUST use `$...$` for inline math (NOT `\(...\)`).
- MUST use `\[...\]` for display math.
- MUST NOT use `$$...$$` under any circumstances.
- MUST use `\begin{align*} ... \end{align*}` for multiline derivations.
- MUST NOT use `\begin{aligned} ... \end{aligned}`.
- MUST NOT use `eqnarray`.
- MUST NOT insert Unicode math symbols; use LaTeX commands.
- MUST keep punctuation consistent: when a display is part of a sentence, it ends with the sentence’s comma/period.
- MUST default to inline math in exposition.
  - DO THIS INSTEAD: use display math for long expressions, multiline work, or when readability improves.
- MUST write complete sentences around computations.
- MUST NOT put a colon immediately before display math.
  - DO THIS INSTEAD: end the lead-in naturally (often with a comma) and continue the sentence after the display.
- MUST NOT start a sentence with a mathematical expression (inline or display).
  - DO THIS INSTEAD: begin with words (“Compute…”, “Then…”, “So, …”) and place math after.

- MUST maintain existing mathematical notation; MUST NOT introduce new notation unless explicitly requested.

- MUST use `\subseteq` (not `\subset`).
- MUST use `\ep` for epsilon if that macro is defined in the current document; otherwise, MUST use `\varepsilon`.


### Spacing and small typographic habits

- MUST put at most one displayed expression per line.
	- DO THIS INSTEAD: separate displays with text or a blank line.
- MUST use thin spaces after commas in tuples/vectors when appropriate: `,\,`.
- MUST use `~` for nonbreaking spaces with units and labels (Theorem~1, $1500$~N).
- MUST prefer `\int_a^b f(x)\,dx` (thin space before the differential).
- MUST NOT add italics/bold unless explicitly requested.
- MUST NOT use `\Rightarrow` or `\Leftrightarrow` as prose.
	- DO THIS INSTEAD: write “implies” / “if and only if”.
- MUST NOT chain implications/equations on a single displayed line.
	- DO THIS INSTEAD: split across lines in `align*` or use separate displays.
- MUST use the serial comma and include “and” before the last item.

### Environments

- When creating `figure` and `table` environments, use the `[ht]` placement specifier.
- In `figure` and `table` environments, place `\caption{...}` before `\label{...}`.
- MUST use theorem-like environments already defined in the preamble; MUST NOT define new ones unless explicitly requested.
- When creating `enumerate` or `itemize` lists, put `\item` on its own line, with item content on the next line.
- MUST NOT insert blank lines inside environments unless needed for readability.
- MUST NOT generate TikZ, pgfplots, or other diagram code unless explicitly requested.

### Packages and preamble

- MUST use existing macros defined in the project; MUST NOT redefine or duplicate them.
- If explicitly asked to create a new operator macro, use `\DeclareMathOperator`.
- Comments in the preamble are welcome when they explain intent, but MUST NOT insert `% TODO:` or AI-generated comments elsewhere.

### Citations and bibliography

- MUST use the citation commands already used in this project.
- MUST NOT introduce new bibliography packages or commands.
- MUST NOT modify the project’s bibliography setup unless explicitly requested.

### File structure and organization

- MUST NOT propose reorganizing files, adding `\input{}`/`\include{}` directives, or changing the directory structure unless explicitly requested.


## Project-specific 

