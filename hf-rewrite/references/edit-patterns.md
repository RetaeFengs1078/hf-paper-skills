# Edit Patterns Derived from Accepted Revisions

These patterns are generalized from writing changes that survived manuscript revision. Apply the judgment, not the topic-specific wording.

## Replace an invented label with its mathematical content

Weak:

> We establish a cumulative-kernel stability criterion.

Better:

> We establish convergence under a uniform bound on the squared deviations of the cumulative-gradient coefficients from a constant reference.

Why: the second version tells the reader the actual condition and does not require an undefined name.

## Report what the experiment measures

Weak:

> A single exposure has a measurable effect on the parameters.

Better:

> Training once on the batch leaves a measurable reduction in its loss 5,000 steps later.

Why: the experiment directly observes the later loss, not an abstract parameter effect.

## State the purpose before procedural detail

Weak:

> At step (t), define the signed difference ... Its coefficient is ... We keep, delete, or refresh it.

Better pattern:

> To test whether stored history still contributes, branch from the same checkpoint. Define the stored contribution, then state what each branch changes and what remains fixed.

Why: readers first learn the experimental question, then can interpret the construction.

## Define a statistic before using it

Weak:

> The slow component's normalized mean age is ...

Better pattern:

> Average lag is the coefficient-weighted mean number of steps since a gradient was computed. The slow and fast components then have average lags of ...

Why: the source paper defines this quantity as a mean of lags. In another paper, use the term justified by its formula and field, rather than copying “average lag.”

## Replace a citation inventory with a conceptual progression

Weak:

> Paper A studies X. Paper B studies Y. Paper C proposes Z.

Better pattern:

> State the standard design choices, group papers by those choices, then narrow to the closest method and compare the exact mechanism.

Why: the reader learns the research landscape rather than memorizing a list.

## Separate related mathematical roles

Weak:

> The algorithm keeps a training point and an output point.

Better pattern:

> State which iterate determines the training trajectory, which sequence is averaged for evaluation, and which final iterate is returned.

Why: stable role-based terminology prevents later ambiguity in theory and experiments.



## Clarify the condition under which a sentence holds

Weak:

> For a constant gradient, the deviation decays as ...

Better:

> Once the gradient becomes constant, the deviation decays as ...

Why: in the source result, constancy begins at a particular time. The revised sentence states that condition without implying constancy throughout training. Use this pattern only when the underlying result has the same temporal condition.

## Replace empty evaluation with a specific synthesis

Weak:

> These results demonstrate the effectiveness of the method.

Better pattern:

> Name the mechanism supported by the result, the condition under which it helps, or the precise contrast established by the comparison.

Why: a synthesis should add interpretation, not approval language.

## Give a display equation visible structure

Weak pattern:

> Several principal relations and a side condition are placed on one display row.

Better pattern:

> Put distinct relations on separate aligned rows, and state a condition such as (Gamma>0) in the prose that introduces or follows the display.

Why: display math should expose the structure a reader needs to inspect. Moving a side condition to prose can improve readability without changing the mathematics.

## Keep an auxiliary definition beside its use

Weak pattern:

> Pseudocode spends a separate numbered line defining a short coefficient, then uses it on the following line.

Better pattern:

> Write the update and append “where ...” with the coefficient definition on the same logical line when the expression remains readable.

Why: the dependency is visible immediately and the algorithm's numbered lines remain focused on actual operations.

## Use a heading that forecasts the section

Weak:

> Learning from persistent gradient history

Better pattern:

> Use a plain question or claim that tells the reader what the section explains, such as why a retained quantity can remain useful.

Why: an informative heading helps readers build a map of the argument and avoids an abstract phrase that could cover several different discussions.

## Preserve paragraph unity

Weak pattern:

> Split one continuous comparison into several short paragraphs solely because the original paragraph is long.

Better pattern:

> Keep the setup, relevant prior results, and concluding comparison in one paragraph when they perform one coherent Related Work function; simplify sentence structure inside it instead.

Why: paragraph boundaries should mark changes in argumentative function, not arbitrary length thresholds.

## State asymptotic dependencies

Weak:

> The rate is (O(T^{-1/2})).

Better pattern:

> State which parameters are fixed and identify the quantities on which the hidden constants depend when that dependence affects the result's interpretation.

Why: an asymptotic rate can be technically correct yet misleading if important parameter dependence is left implicit.

## Use relative stage labels for a temporal narrative

Weak pattern:

> Repeat three exact checkpoint numbers every time the prose describes the same trend.

Better pattern:

> Use early, middle, and late training to explain the progression, while retaining the exact checkpoints in the figure, caption, table, or setup.

Why: the prose communicates the temporal pattern while the quantitative record remains available.

## Explain the sought object before its certificate

Weak pattern:

> An invariant is displayed before the target set appearing in its side condition has been explained.

Better pattern:

> State what the routine seeks, define the target set, then explain how the maintained certificate constrains the search.

Why: the reader can understand what the certificate accomplishes instead of decoding the algorithm's goal from bookkeeping.
