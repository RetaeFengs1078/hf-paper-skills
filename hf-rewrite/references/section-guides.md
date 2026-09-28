# Section Guides

These are guides to writing sections within the existing or author-supplied outline, not instructions to restructure the paper. Preserve the author's allocation of substantive material.

## Headings and roadmaps

Use one capitalization convention throughout. Prefer a short, informative heading that tells a human reader what question, object, or conclusion the section concerns. Avoid decorative labels, unexplained technical compounds, and vague abstract nouns.

At the beginning of a long multi-part section, a brief roadmap can state the order of ideas and why that order matters. Do not add a roadmap to a short section or mechanically list every subsection. Update it whenever the section order changes.

## Abstract

Make the abstract answer the applicable questions in an order that fits the contribution:

1. What problem or limitation matters?
2. What does the paper introduce or discover?
3. What is the defining mechanism or distinction?
4. What is proved, if the paper has a theorem?
5. What do the main experiments establish, if there are experiments?

Avoid undefined notation, literature review, implementation detail, and broad adjectives. State the real theorem condition rather than an internal nickname.

## Introduction

Move from the concrete research problem to the missing capability, then to the method and evidence. The reader should understand the contribution before encountering the contribution list.

When explaining inspiration from prior work, separate:

- what prior work reveals;
- what limitation or open need follows;
- what the present method changes;
- why that change addresses the need.

Do not describe the new method as a list of components without explaining their roles and interaction.
Locate the contribution relative to the closest prior work using the precise mechanism, condition, or guarantee that differs. Do not present a standard rate or a familiar component as the novelty when the distinctive result lies elsewhere.

The abstract, introduction, and conclusion should agree but should not be paraphrases of one another: the abstract compresses the whole paper, the introduction builds the motivation and positions the contribution, and the conclusion synthesizes what the evidence established.

## Related Work

Organize paragraphs by conceptual families or design choices, not by paper chronology. A useful paragraph usually:

1. names a standard mechanism or distinction;
2. places representative work within it;
3. narrows to the closest methods;
4. explains the present paper's precise relation to them.

Acknowledge overlap before stating differences. Compare concrete objects: recurrences, states, averaging rules, adaptation mechanisms, transformations, assumptions, or guarantees. Avoid citation inventories and vague claims that methods are “fundamentally different.” Check each attributed claim against the cited source, and do not import a later paper's interpretation into an earlier source.

## Method

Introduce the problem and mathematical object before the update equation. Before the pseudocode, briefly explain the routine's purpose, the state it retains, and the events that change that state. Present the algorithm before extended interpretation, then explain its important branches and the role of each state and parameter in the order the reader encounters them.

If the algorithm has distinct training and evaluation sequences, explain them separately and state which sequence:

- determines the optimization trajectory;
- receives gradients;
- is averaged;
- is evaluated;
- is returned.

Distinguish the conceptual method from dataset-specific implementation details. Refer precisely to experimental setup or appendix details that are already provided, rather than repeating them.

In pseudocode, keep conventional inputs compact, place a small auxiliary definition next to the line that uses it when helpful, and use comments only to identify a semantic role that the formulas alone do not make obvious.

## Mechanism or intuition section

When readers need the mechanism to interpret the evidence, use the order:

1. derive or characterize the mechanism;
2. test its effect with direct evidence or a controlled intervention;
3. examine when or where the effect matters;
4. synthesize the mechanism and evidence.

An observation can instead open the section when its meaning is clear and it motivates the mechanism question.

## Theory

State assumptions near the result that uses them. Make central theorem statements understandable without reading the proof.

Prefer the real mathematical condition to a decorative theorem nickname. Do not add parenthetical titles to theorem-like environments unless the title supplies genuinely useful standard terminology.

After a theorem:

- state its main implication in ordinary prose;
- explain the role of the unusual condition;
- identify what a corollary verifies for the proposed method, if applicable;
- refer precisely to the existing proof rather than repeating its mechanics in the surrounding explanation.

Do not mix an exact mathematical map with a finite numerical approximation, or an unconditional convergence result with a conditional one. State fixed parameters and relevant hidden-constant dependencies in asymptotic conclusions.

Give each existing example a clear explanatory role in the argument: explain what it helps the reader understand rather than present it as an isolated result.

## Experiments

Structure each experimental paragraph around a scientific question:

1. what is being tested;
2. what comparison or control answers it;
3. what metric is measured;
4. what the result is;
5. what conclusion the result supports.

State fixed and changed variables clearly in interventions. Report the observed quantity directly before interpreting why it changed.

In the main text, emphasize the comparison and pattern. Cite existing tables or appendix accounts of hyperparameters, per-case statistics, secondary diagnostics, and protocols instead of repeating those inventories in prose. When the point is change over the course of training, relative descriptions such as early, middle, and late can make the progression easier to follow; retain exact checkpoints where quantitative interpretation or reproducibility requires them.

Avoid narrating the run history or debugging process.

## Figure captions

A caption should let a reader interpret the figure without searching the main text. State:

- what each panel shows;
- the comparison or intervention;
- the metric and direction of improvement;
- the parameters, normalization, uncertainty summary, or unequal scale that materially affects interpretation.

Use established manuscript terminology. Do not introduce a new alias in a caption.

## Conclusion

Synthesize the method, strongest theoretical statement, and principal empirical finding when present. Do not reproduce the abstract sentence by sentence, reopen implementation details, or add new claims.

The final implication should follow from the paper's evidence. Avoid generic claims that the work “opens new avenues” unless a concrete avenue is identified.

## Appendix

For a long appendix, give readers a brief map of its parts and use navigable section references when the format allows. In the main text, point to the specific appendix proof, protocol, or supplementary result behind a claim; avoid a vague appendix citation when a precise section or theorem reference is available.

When a detailed appendix roadmap is useful, provide a compact hierarchy of section and subsection titles with generated page references and working links, followed by a short explanation of the organization. Follow the document's template for placement; do not hard-code page numbers or copy another paper's appendix structure.


