---
name: hf-rewrite
description: Draft or polish research-paper prose from established scientific content. Use for missing or partial prose, unclear explanations, inconsistent terminology, and equation or pseudocode presentation. Preserve the existing or author-supplied paper structure; whole-paper editorial restructuring is a separate explicit workflow.
---

# HF Rewrite

Turn complete scientific content into a paper that a human researcher can understand in one forward reading. Treat equations, algorithms, experimental records, and established claims as fixed source material unless the user separately authorizes scientific changes.

Read [references/revision-criteria.md](references/revision-criteria.md) for every task. Read [references/section-guides.md](references/section-guides.md) when drafting or rewriting a full section. Read [references/algorithm-presentation.md](references/algorithm-presentation.md) when editing pseudocode or explaining algorithm interfaces and stopping rules. Read [references/edit-patterns.md](references/edit-patterns.md) when diagnosing AI-like prose or deciding how far to rewrite.

Improve the expression of established research. Do not add experiments or theorems to make the paper appear complete.

## Scope: writing, not whole-paper restructuring

Work within the existing or author-supplied outline. Improve sentence and paragraph logic, remove redundant wording, and clarify notation, formulas, and pseudocode. When prose is missing, explain the supplied scientific content without selecting a new set of contributions.

Do not automatically diagnose the paper's technical arc, triage sections, redesign the outline, move substantive material between the main text and appendix, or discard unique results. Those actions belong to the separately invoked `hf-restruct` skill. Invoking this writing skill does not invoke that companion: do not load or run its workflow unless the user explicitly invokes it. The rules in this skill's references remain subject to this scope boundary.

## Establish the scientific content before writing

Read enough of the manuscript to identify:

- the problem and motivation;
- the paper's actual contribution and its boundary;
- the mathematical objects, algorithms, assumptions, and outputs;
- the proved claims and their conditions;
- the experimental questions, measurements, and supported conclusions, if any;
- the order in which a reader must learn these facts.

Build a small internal terminology map from each important referent to one preferred term. Distinguish related but different objects, such as a sequence and its final element, a training iterate and an averaged iterate, or an exact map and its numerical approximation. When changing a term, check the same referent across the main text, appendix, figure and table labels, captions, and theorem statements.

Apply the same discipline to notation: introduce symbols when readers first need them, explain the roles of similar symbols, and flag conflicting reuse rather than silently changing the mathematics. Prefer a short explicit expression to a new alias introduced only to shorten formulas. A new symbol should reduce the reader's total effort, not merely the author's typing. Respect explicit author notation preferences throughout the authorized scope; do not restore a rejected alias under a different name.

Assume readers know the foundations of the paper's field, but not every concept imported from neighboring fields. Explain an imported concept when the argument first depends on it.

When the user provides exemplar papers, learn from their organization, pacing, and explanatory density without copying their wording or importing their claims. When no closer exemplar is supplied, the author's preferred style references are *Accelerated Distance-adaptive Methods for Hölder Smooth and Convex Optimization* and *The Coverage Principle: How Pre-Training Enables Post-Training*: use their directness and reader-oriented organization as a standard, not their topic-specific wording.

If the prose is absent, draft from this content map. If it is partial, preserve good human-written passages and repair only what is needed. If it is AI-generated, retain the scientific content but freely rebuild sentence and paragraph structure.
Change an existing sentence only when the revision removes a specific ambiguity, gap, repetition, or reading obstacle; do not rewrite for variation alone.

Do not invent a missing theorem, assumption, causal explanation, comparison, or empirical conclusion. If the source materials do not determine a necessary relation, flag the gap instead of filling it with plausible prose.

## Write for forward human reading

1. Give each paragraph one clear job. Keep a logically unified paragraph intact; do not split it merely because it is long.
2. State its controlling point early.
3. Define what readers need to understand a result when it appears. Explain a mechanism before evidence that depends on it; an intelligible result can also motivate a later mechanism explanation.
4. Order the explanation within each section by conceptual dependency, not by the chronology of the research process.
5. Use explicit subjects and verbs. Prefer a plain explanatory clause to a compressed invented label. Split or reorder sentences when nested clauses or multiple claims obscure the main action; do not split solely by length.
6. Keep one stable term for each referent; do not vary terminology for elegance.
7. Keep short supporting expressions inline. Display central equations or expressions whose structure readers need to inspect. State what an equation, theorem, or experiment actually establishes, then explain why it matters.
8. Use precise references to existing appendix material without duplicating its details in the prose. Preserve the author's allocation of substantive material.
9. End a paragraph by completing its argument or preparing the next one, not by restating its opening.

## Preserve scientific meaning

Keep quantifiers, assumptions, comparison sets, evaluation objects, causality, modality, and asymptotic dependencies unchanged. Match the strength of the prose to the evidence:

- a theorem proves only its stated conditional result;
- an experiment shows an observed result and may suggest a mechanism;
- an illustrative figure provides intuition rather than universal evidence;
- a correlation is not a causal explanation;
- an implementation detail is not automatically part of the method's conceptual definition.

If improved prose appears to require a stronger or different scientific claim, stop and identify the choice rather than silently making it.

## Eliminate characteristic AI-writing failures

Rewrite rather than cosmetically polish when the draft:

- gives one object several names;
- uses a technical-sounding phrase that is neither standard nor defined;
- repeats the same point in successive sentences;
- hides the action inside abstract nouns;
- opens with background but postpones the paragraph's purpose;
- lists citations without a conceptual organization;
- narrates implementation chronology instead of explaining the method;
- piles up caveats, exceptions, and audit-like disclosures;
- makes a generic claim such as “demonstrates effectiveness” after already reporting the result;
- asks the reader to understand a distinction that is introduced only later;
- relies on vague modifiers such as broad, strong, significant, or substantial without stating the relevant quantity or comparison.

When a term may be AI-invented, check relevant primary literature. If it is not established and is not needed as a new definition, replace it with ordinary field language or a direct description of the mathematical property.

## Final pass

Read the revised text continuously, not as isolated sentences. Verify:

- a reader never needs a later paragraph to decode an earlier one;
- terminology is consistent across the full relevant scope;
- claims in the abstract, introduction, theory, experiments, and conclusion agree on their objects, assumptions, comparisons, and evidential strength;
- pronouns and comparison words have unambiguous referents;
- displayed equations are introduced and interpreted;
- mathematical notation and typography are consistent;
- pseudocode preserves the algorithm's dependencies, scope, stopping semantics, and outputs;
- cross-references name the correct object type and point to the specific result, proof, protocol, figure, or appendix section the sentence needs;
- section and subsection titles use one capitalization convention and accurately forecast their content;
- paragraph transitions express a real logical relation;
- the main result is easy to locate;
- no sentence was added solely to sound rigorous;
- no scientific content changed during rewriting.

In the delivery note, report material changes to notation or exposition and any unresolved ambiguity. Keep this editorial account outside the paper itself.

When a rendered manuscript is available, check equation layout and page flow as well as the source. Keep added explanation proportionate and report material changes in length.


