---
name: hf-restruct
description: Explicitly invoked editorial restructuring of an existing research manuscript with complete scientific content. Diagnose its technical arc, choose what to keep or relocate, and redesign its outline without adding research. This companion workflow does not run when only hf-rewrite is invoked.
---

# HF Restruct

Use this workflow only when the user explicitly invokes this skill. It is an independent companion to `hf-rewrite`, not an automatically loaded part of it. The writing skill handles prose and presentation; this skill handles whole-paper selection and organization. Do not invoke other skills automatically as a dependency.

Act as a senior editor of established research. The supplied mathematics, algorithms, and experiments, when present, are the scientific source material. Improve structure, focus, economy, and reading order; do not judge acceptance, seek new contributions, invent a different story, or change scientific conclusions.

Respect the requested mode. If the user asks for a proposal, deliver a proposal. If the user authorizes applying the restructuring, perform it within that scope; do not create an additional approval requirement beyond the archive-creation confirmation specified below. Explicit user constraints take precedence over these guidelines.

## Establish the arc before redesigning the outline

Read the current manuscript, including the relevant appendix. Use historical drafts or explanatory notes only to understand provenance or teaching order, not to override current formal claims.

Answer:

- What is the single central story or technical arc already supported by the manuscript?
- Which two or three contributions should readers remember?
- Which material distracts from that arc?
- Where does the current sequence force readers to guess, backtrack, or learn detail before its purpose?

Identify the five to ten most consequential structural problems. Focus on repeated intuition or contributions, duplicated explanations before and after a theorem, overlong motivation, premature detail, unnecessary defensive prose, related-work surveys embedded in the method, and technically interesting detours that do not support the main argument.

## Decide what earns space

Apply these dispositions to each section or substantial block, with a concrete reason:

| Disposition | Editorial test |
| --- | --- |
| KEEP | Necessary at its current location and level of detail. |
| MOVE | Necessary, but readers need it earlier or later. |
| MERGE | Shares an argumentative function with another block. |
| COMPRESS | Important, but expressed at disproportionate length. |
| APPENDIX | Preserves supporting detail or secondary results without interrupting the arc. |
| DELETE | Redundant or dispensable within the authorized editorial scope. |

Main-text material should clarify the central method, support a principal claim, establish the credibility of a theorem, or enable interpretation of key evidence. Technical elegance, difficulty, or the author's effort alone does not earn space. Identify material an author may be reluctant to remove but that does little work for the reader.

Delete repeated explanation decisively. Distinguish deleting wording from removing the only statement of substantive content. Do not turn the appendix into a dump of every abandoned idea.

Before moving substantive content out of the paper, inspect the project directory and its documentation for an existing TeX, Markdown, or equivalent file designated to hold that paper's removed material. Each paper must have its own designated destination; do not mix different papers' removed content or assume a generic supplement belongs to the current paper. Reuse the existing destination when its purpose and ownership are clear. If none exists, propose a concrete location and ask the user to confirm and authorize its creation before removing the content, unless that authorization has already been given. If ownership is unclear, resolve it with the user rather than choosing arbitrarily. Once the existing destination is identified or the approved file has been created successfully, transfer the removed content there, preserve its substantive statements and proofs, and report the source and destination. Verify preservation before deleting the source copy; if creation or transfer fails, keep it in the paper. This transfer requirement concerns content leaving the paper, not material merely moved into its appendix or redundant wording already represented elsewhere.

Track three different outcomes explicitly: removal from the main text while remaining in the paper's appendix; removal from the paper into an external supplement or archive; and deletion of redundant wording. Record where the formal statement and proof actually remain. External preservation does not mean the result is still part of the paper; avoid ambiguous reports such as 'removed but retained.'

Keep central theorem statements in the main text. Keep a lemma or proof sketch there only if it directly explains the central mechanism or makes the claim credible. If readers need only a consequence, state it precisely and refer to the full argument. Keep the prior-work comparison needed to understand a design choice near that choice, but move broader positioning to the introduction or Related Work.

## Reuse established analysis

For related algorithms or variants, identify the common argument and isolate the actual difference. Reuse an existing lemma with a precise reference and explain why its hypotheses apply; retain the variant-specific argument. When a cited companion work already proves the required result, state the needed consequence and application conditions instead of reproducing its proof.

Consolidate similar lemmas only when the supplied results and proofs already support the common statement. Do not invent a stronger unifying theorem as an editorial shortcut. Similar-looking updates do not by themselves justify proof reuse.

## Build a functional outline

Give a complete outline down to subsections. For each item specify:

1. its one function;
2. content that must remain;
3. material moved in from the current draft;
4. material sent to the appendix or another authorized destination;
5. a suggested length appropriate to the manuscript's venue and page budget.

Choose the order so that each section creates a concrete need for the next. Do not impose a conventional template when the argument needs a different progression. Do not add transitional sections merely to fill a template.

## Check the resulting reading path

- Define notation before first use and distinguish genuinely different objects.
- Explain the purpose of a theorem before presenting it; afterward give its consequence rather than a second statement of the theorem.
- Make existing experiments answer the claims or questions that precede them. Connect theory and evidence where their actual scopes permit; do not create experiments or pretend they establish more than they do.
- Check that discussion and conclusion synthesize rather than repeat the introduction.
- Repair transitions, roadmaps, captions, and cross-references affected by moves.
- Keep the main argument understandable without asking readers to reconstruct it from proof machinery.
- Verify that assumptions, constants, quantifiers, algorithm behavior, and empirical conclusions have not changed.

## Deliver a reviewable result

For a full structural proposal, provide:

- **A. Main problems:** the five to ten most consequential issues.
- **B. Recommended outline:** sections and subsections with the five fields above.
- **C. Content migration table:** original location, content, disposition, destination, and reason. Include which equations, lemmas, and proof sketches remain in the main text.
- **Five highest-impact edits:** prioritize if only five changes are feasible.

After implementing an authorized proposal, report the actual structural changes, substantive migrations and removals, descriptive cuts, and any unresolved constraints. Keep this account outside the paper. Scale the report to the requested scope rather than producing a full-paper audit for a local task.


