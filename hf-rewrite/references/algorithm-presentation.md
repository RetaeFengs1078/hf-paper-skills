# Presenting Established Algorithms

These rules concern exposition, not algorithm design. Preserve the actual updates, dependencies, initialization, stopping semantics, and outputs. A shorter algorithm box is not an improvement if it changes the procedure or requires the reader to reconstruct missing mathematics.

## Explain the hierarchy

Before a routine, explain its task and the information it carries. Distinguish the complete algorithm from reusable computational routines and from analysis-only objects. Split a long algorithm when the resulting routines have clear purposes and interfaces; do not split mechanically by loop depth. One box can contain both an outer and an inner loop, and those loops must remain explicit when both are part of the procedure.

When the format permits, reserve numbered Algorithm captions for complete methods and use concise named captions for helper routines. Give helpers meaningful names and consistent typography, and refer to them by name with working links. This is a presentation option, not a requirement to renumber every existing manuscript.

## Keep interfaces and state readable

- Put inputs, parameter ranges, and constraints in Require or Input. Put initialization on its own unnumbered Initialize line when the template allows; initialize local state inside the block where it belongs rather than only once globally.
- A helper accepts local parameters. Do not carry the caller's outer index into every parameter name when it has no meaning inside the helper. Keep genuine local iteration indices and distinguish nested loop roles.
- Use accurate indexed recurrences when presenting mathematical sequences. Use equality for definitions or the same quantity under two equivalent notations; reserve assignment arrows for actual procedural state changes. Do not turn an in-place update into an ambiguous self-referential equality.
- Show a short coefficient directly in an update when a separate alias adds no understanding. Combine tightly related state updates on one readable line; separate them when their structures or dependencies need inspection.
- Prepare parameters before the updates that use them, and define the next state where its dependencies require. Often this places parameter preparation near the top and the next-state update near the end of a branch; preserving the algorithm takes precedence over a visual ordering preference.
- Keep unchanged parameters implicit when their scope already makes constancy clear. Avoid identity recurrences and extra bookkeeping variables introduced only by the rewrite.
- Indent control structures visibly. Use short comments for roles that formulas do not reveal; do not force wide alignment gaps or crowd unrelated operations onto a line to save space.

## Separate the mechanism from execution conventions

Keep the main recurrence and essential branching visible. Routine caching, redundant computation announcements, and implementation bookkeeping can move to adjacent prose when they obscure the mechanism. Keep or explain any execution convention necessary to interpret the algorithm correctly; do not mistake a shorter box for permission to remove essential information.

When several return tests dominate the box, state them immediately below as clearly labeled conditions with their associated outputs. The loop can then say to check those conditions and return the indicated result. Preserve their priority, evaluation points, and any early exit that skips remaining updates. Do not move all tests after an update merely for symmetry if the original procedure checks one earlier.

An exceptional case can be described in adjacent prose when its handling is immediate and established. Do not silently omit it or assume that a test valid for one problem class applies to another. Define outputs and indices precisely; a verbal position such as “previous” must agree with the sequence actually being referenced.

## Check the rewritten presentation

Trace one ordinary iteration and each distinct exit against the supplied algorithm: which values exist, which updates have occurred, and what is returned? Cross-check the surrounding prose and proof references. This is a consistency check on writing, not authorization to repair or redesign the underlying method.


