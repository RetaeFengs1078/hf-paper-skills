# Revision Criteria

## 1. One referent, one term

Terminological variation is not a virtue in technical writing. Choose the most standard, precise term for each object and use it consistently.

Before replacing terms, determine whether they are true aliases or mathematically distinct. For example, a sequence, one iterate, its final iterate, the point where a gradient is evaluated, and the point returned by an algorithm may require different names. Do not collapse real distinctions, but do not call the same object a point, output, state, trajectory, and sequence in different sections.

Apply replacements contextually. Global search-and-replace often breaks legitimate uses of words such as step, iteration, update, state, or average. Use consistent terms for the same quantities while preserving distinctions between genuinely different objects.

## 2. Prefer established or descriptive language

A technical expression is justified when it is standard in the field, explicitly defined because the paper needs a new concept, or is the most economical direct description of a mathematical object.

Replace unnecessary branded labels with the actual property. For example, an undefined “stability criterion” is less informative than saying that the sum of squared coefficient deviations is uniformly bounded. Name a statistic by the quantity it measures, using established field terminology where appropriate; define any paper-specific term before relying on it.

Do not assume that a familiar-sounding compound is established terminology. Check relevant primary papers when in doubt.

## 3. Make the grammatical subject carry the science

Prefer:

- “The coefficient rescales the first term so that ...”
- “Training once on the batch lowers its loss 5,000 steps later.”
- “The theorem gives a bound when ...”

Avoid:

- abstract subjects such as “the effectiveness,” “the framework,” or “the perspective” when a concrete mathematical object performs the action;
- unsupported latent interpretations such as “the batch changes the parameters” when the experiment measures only a later loss difference;
- passive chains that hide what is held fixed, changed, compared, or returned.

## 4. Put information in dependency order

A useful default sequence is:

1. the question or object;
2. the mechanism, definition, or controlled setup;
3. the result;
4. the interpretation;
5. the connection to the next question.

Within the current section, introduce the explanation needed to understand its evidence before relying on it. Introduce a distinction before using it in a figure caption or theorem discussion. Changing the section order belongs to the separate restructuring workflow.
For a mathematical method, explain what the procedure seeks and define that object before presenting the invariant, certificate, or construction used to find it. Do not hide an object's first definition inside a side condition of a later formula. Author-provided slides or explanatory notes may suggest a better teaching order; extract only what the paper needs and preserve the accepted manuscript's scientific statements.
An observation may precede its mechanism when readers can understand the observation and it poses the question that the mechanism answers. Use a short roadmap only when a section has several dependent parts; make it describe their intellectual progression rather than list headings mechanically. After moving material, revise the roadmap, introductions, transitions, and cross-references that relied on the old order.

Before introducing a non-obvious quantity, explain what it measures and why the argument needs it.

## 5. Control information density

Make the relevant pattern visible before listing supporting detail. When exact statistics already appear in a table or appendix, cite that location instead of repeating the entire inventory in prose. Do not use a language edit to relocate or delete substantive material.

Compression must not erase the principal result, uncertainty, comparison basis, or an exception that changes the conclusion.

Shorten a sentence when several nested qualifications or logical steps make its subject, action, or condition hard to follow. Split at a real change of thought or move a condition next to the claim it limits. Do not confuse concision with sentence fragmentation: keep tightly coupled facts together when a single sentence has a clear grammatical spine, and keep sentences in one paragraph when they serve one continuous argumentative function.

## 6. Explain equations and algorithms

Use inline math for short expressions that fit naturally into a sentence. Display an equation when it states a central definition or result, when its terms need comparison, or when readers will refer back to it. Avoid giving routine expressions a separate display solely for emphasis, and do not bury a structurally complex equation in running text. Changing the layout must not change the mathematical content.

Do not put boxes around equations for decorative emphasis. Let the placement, surrounding explanation, and equation structure provide the emphasis unless the author explicitly requests a different presentation.

Avoid introducing a symbol for a short exponent, coefficient, or expression solely to save space. Write the expression directly when that is easier to read. Retain a named quantity when it has a conceptual role or substantially simplifies a genuinely complex argument; do not replace a rejected abbreviation with a different alias. When an equivalent notation change is authorized, check its definitions and uses across the relevant text and proofs. A shared notation for distinct mathematical objects requires an explicit convention; it must not silently strengthen assumptions or imply that the objects are identical.

In a dense multi-line display, put distinct principal relations on separate rows and align corresponding operators. Move side conditions, domains, and verbal qualifications into the surrounding prose when leaving them inside the display obscures its structure. Treat an equation as part of the sentence and punctuate the surrounding prose accordingly.

Introduce an equation by naming the object or relation it expresses. After the display, explain:

- the role of its principal terms;
- the distinction from nearby coefficients or recurrences;
- the behavior that matters for the paper.

Do not merely restate the equation in words. Explain its consequence.

When an abstract definition is difficult to motivate, consider one short numerical example before the formula. Use it to replace a longer abstract explanation rather than add another layer of repetition.

For algorithms, distinguish:

- the state that determines training dynamics;
- any averaging or evaluation state;
- the quantity transformed into a step;
- the final returned object.

Use compact algorithm inputs when conventional symbols have already been defined. Put conceptual explanation in prose, not redundant labels on every input. Define an auxiliary coefficient beside the update that first uses it when this keeps the dependency visible; do not isolate a one-line definition merely because it can occupy its own algorithm line.

For detailed pseudocode guidance, use [algorithm-presentation.md](algorithm-presentation.md). Simplifying the written interface must not change the underlying procedure.

Use standard and internally consistent mathematical typography, delimiters, norm notation, differential symbols, subscripts, and capitalization. Correct presentation errors without silently changing the mathematical object.

## 7. State formal conditions and asymptotics precisely

Define the quantities, mathematical objects, and formal conditions before a theorem relies on them. Group reusable formal conditions into assumptions when that makes the theorem easier to read, but keep the central theorem sufficiently self-contained.

For big-O or asymptotic statements, state which quantities are fixed and what the hidden constants depend on when that dependence affects interpretation. Do not call a conditional bound “convergence” unless its assumptions make the relevant term vanish or otherwise justify the claim.

## 8. Match statements to evidence

Use “shows” for a directly displayed empirical result, “suggests” for an interpretation, and “illustrates” or “provides intuition” for a diagnostic example. Reserve “proves,” “guarantees,” and unconditional verbs for mathematical statements that support them.

Describe the measured quantity before interpreting hidden mechanisms. A controlled intervention can isolate effects only to the extent that its fixed and changed variables justify.
When describing prior work, check that each cited source supports the attributed claim. Distinguish what that source establishes from the present paper's inference or comparison.

## 9. Remove repetition without removing logic

Delete a sentence when it only paraphrases the previous result. Replace it when it should instead supply the missing mechanism, contrast, or implication.

Common redundant endings include:

- “This demonstrates the effectiveness of the proposed method.”
- “These results validate our approach.”
- “Together, these findings highlight ...”

Such sentences are useful only if they state a new, specific conclusion.

## 10. Avoid audit prose

The paper should report scientifically relevant design and evidence, not reproduce an internal review trail. Remove run-directory names, debugging history, abandoned variants, defensive explanations, and selection-process narration unless they are required for reproducibility or interpretation.

Do not add limitations merely to pre-empt imagined criticism. State a limitation when it changes the claim's scope or a reader's interpretation.

## 11. Check paragraph function

For each paragraph, be able to complete: “This paragraph exists to ____.”

If the answer contains “and” connecting unrelated tasks, split or reorder it. If two adjacent paragraphs have the same answer, combine them or give each a distinct role.


