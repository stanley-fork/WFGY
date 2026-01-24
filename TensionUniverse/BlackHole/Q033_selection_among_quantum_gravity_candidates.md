# Q033 · String theory vs alternative quantum gravity frameworks (selection tension)

## 0. Header metadata

```txt
ID: Q033
Code: BH_PHYS_STRINGS_VS_ALTERN_L3_033
Domain: Physics
Family: Quantum gravity candidates
Rank: S
Projection_dominance: P
Field_type: dynamical_field
Tension_type: consistency_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-24
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical problem behind Q033 can be stated as follows.

We have several broad frameworks that attempt to give a consistent quantum description
of spacetime and gravity. Examples include:

* string theory and its extensions,
* loop quantum gravity (LQG) and spin foam models,
* asymptotic safety programs for gravity,
* causal dynamical triangulations and related lattice approaches,
* other discrete, emergent, or holographic proposals.

Each framework can, in principle, be extended in many directions and can be matched
to low energy physics in different ways. Many of these frameworks can reproduce
classical general relativity in appropriate limits and can be made compatible with
standard model physics at some effective level.

The core question is:

> Given current and foreseeable observational, experimental, and theoretical
> constraints, can we identify one (or a sharply delimited subset of) quantum
> gravity framework(s) as the uniquely preferred description of nature, or are
> we forced into a long term "landscape" where several inequivalent frameworks
> remain viable and cannot be cleanly separated?

At the canonical level, this is a selection and discrimination problem among
multiple high level theories, not a problem of constructing any one theory from
scratch.

### 1.2 Status and difficulty

Empirically and conceptually, the status is:

* Multiple frameworks can be made compatible with general relativity in the
  classical limit and with low energy effective field theory in suitable regimes.
* Direct experimental access to Planck scale phenomena is extremely limited, so
  many selection criteria rely on indirect consistency arguments, cosmology,
  or structural unification.
* String theory has developed an extensive mathematical and phenomenological
  structure, including gauge/gravity duality, compactifications, and a large
  "landscape" of vacua.
* Loop quantum gravity has developed rigorous quantizations of certain
  gravitational degrees of freedom, and concrete models for discrete spectra
  of geometric operators.
* Asymptotic safety and lattice approaches provide nonperturbative paths to
  ultraviolet complete theories of gravity.
* No single framework has yet produced a decisive, widely accepted,
  quantitatively verified prediction that excludes all competitors.

The difficulty arises from a combination of:

* limited experimental reach,
* high dimensional theory spaces,
* flexibility in matching to low energy physics,
* and deep conceptual questions about spacetime, unitarity, and holography.

There is no accepted, canonical selection principle that yields a unique winner.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q033 has three roles.

1. It is the prototype **selection tension** problem for high level physical
   theories, where consistency_tension measures how well each candidate fits
   simultaneously:

   * known data,
   * theoretical consistency conditions,
   * and cross regime coherence across scales.

2. It serves as a bridge node between:

   * Q021 (foundations of quantum field theory and gravity),
   * Q031 and Q032 (effective field theory and thermodynamic behavior),
   * and Q040 (black hole information constraints).

3. It provides a template for how to encode, at the effective layer, a
   "multi framework" tension problem, where we compare not just one theory
   against data but several competing theories against a shared constraint set.

### References

1. J. Polchinski, "String Theory, Volume 1: An Introduction to the Bosonic
   String", Cambridge University Press, 1998, string theory and quantum gravity.

2. C. Rovelli, "Quantum Gravity", Cambridge University Press, 2004,
   loop quantum gravity and background independent approaches.

3. M. Reuter, "Nonperturbative evolution equation for quantum gravity",
   Physical Review D, late 1990s, early work on asymptotic safety.

4. J. Ambjorn, J. Jurkiewicz, R. Loll, "Causal dynamical triangulations and
   the quest for quantum gravity", various review articles in the 2000s,
   lattice based approaches.

(Exact citations and page ranges are handled at the project level; this entry
only records canonical sources.)

---

## 2. Position in the BlackHole graph

### 2.1 Upstream problems

These problems provide conceptual or technical foundations that Q033 relies on
at the effective layer.

* Q021 (BH_PHYS_QFT_FOUND_L3_021)
  Reason: provides the effective layer encoding of quantum field theory and
  renormalization that all candidate quantum gravity frameworks must respect.

* Q031 (BH_PHYS_EFT_GRAV_L3_031)
  Reason: defines the effective field theory of gravity and the regime where
  any candidate must reduce to general relativity plus corrections.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: formalizes thermodynamic and statistical constraints on quantum
  systems, needed to encode black hole thermodynamics and holographic hints.

* Q040 (BH_PHYS_QBLACKHOLE_INFO_L3_040)
  Reason: encodes information theoretic constraints from black hole physics
  that any candidate quantum gravity theory must satisfy.

### 2.2 Downstream problems

These problems directly reuse Q033 components or depend on its selection
tension structure.

* Q034 (BH_PHYS_QG_PHASES_L3_034)
  Reason: uses Q033's selection tension components to study phase structure
  and transitions between different quantum gravity regimes.

* Q040 (BH_PHYS_QBLACKHOLE_INFO_L3_040)
  Reason: reuses the consistency_tension framework to compare how different
  quantum gravity candidates resolve or fail to resolve information paradoxes.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: leverages Q033's cross regime consistency tools to encode relations
  between information processing, thermodynamics, and spacetime microstructure.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: reuses multi framework selection templates to interpret AI internal
  representations as competing effective theories.

### 2.3 Parallel problems

Parallel nodes share similar tension types but do not directly depend on
Q033 components.

* Q021 (BH_PHYS_QFT_FOUND_L3_021)
  Reason: both Q021 and Q033 address consistency_tension of theory spaces,
  but Q021 focuses on quantum field theory foundations rather than gravity.

* Q036 (BH_PHYS_HIGH_TC_MECH_L3_036)
  Reason: both involve competing microscopic mechanisms that try to explain
  macroscopic phenomena under strong consistency constraints.

* Q039 (BH_PHYS_QTURBULENCE_L3_039)
  Reason: both deal with complex field dynamics where global constraints must
  be satisfied by strongly coupled degrees of freedom.

### 2.4 Cross domain edges

Cross domain edges connect Q033 to non physics problems that can reuse its
components.

* Q001 (BH_MATH_NUM_L3_001)
  Reason: both encode selection among models using structured tension
  functionals on complex field data (spectral vs geometric constraints).

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: imports Q033 style consistency_tension between microscopic dynamics
  and macroscopic information flow.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: uses Q033's multi framework selection template for competing
  interpretability models of neural networks.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions,
* finite reference libraries and fairness constraints at the encoding level.

We do not describe any hidden generative rules or constructions that produce
internal TU fields from raw data.

### 3.1 State space and candidate library

We assume the existence of a hybrid semantic state space

`M_QG`

with the following structure at the effective layer.

1. Finite candidate library

   There is a finite index set

   ```txt
   Library_QG = { c_1, c_2, ..., c_K }
   ```

   where each `c_k` denotes an effective quantum gravity framework label
   (for example "string_like_family", "loop_like_family", "asymptotic_safety",
   "lattice_based_family", "emergent_spacetime_family").

   The library is fixed before any tension evaluation. Adding or removing
   entries is treated as a separate versioned update of this problem, not as
   a parameter choice made after seeing the data.

2. Finite reference envelope library

   There is also a finite set of reference envelopes

   ```txt
   Library_env = { e_1, e_2, ..., e_L }
   ```

   Each `e_l` encodes, at the effective layer, a bundle of constraints such as:

   * classical general relativity tests,
   * cosmological observations,
   * black hole thermodynamics,
   * quantum field theory consistency conditions,
   * and basic unitarity and causality requirements.

   These envelopes are also fixed before tension evaluation and versioned if
   they are changed.

3. Hybrid state space

   Each state `m` in `M_QG` is of the form

   ```txt
   m = (c, e, X)
   ```

   where:

   * `c` is a candidate label in `Library_QG`,
   * `e` is an envelope label in `Library_env`,
   * `X` is an effective summary of how the chosen candidate behaves under
     the constraints grouped in `e`.

   We do not specify how `X` is constructed from detailed calculations or data.
   We only assume `X` contains enough structured information to evaluate the
   observables defined below.

### 3.2 Admissible encoding class and fairness

We introduce an admissible encoding class

```txt
E_QG
```

consisting of all encodings that satisfy the following effective layer
constraints.

1. Shared observable set

   Each encoding in `E_QG` uses the same finite set of evaluation dimensions

   ```txt
   D_QG = { d_local, d_cosmo, d_bh, d_uv, d_internal }
   ```

   where, for example:

   * `d_local`: local and solar system tests of gravity,
   * `d_cosmo`: cosmological background and structure formation,
   * `d_bh`: black hole thermodynamics and information related constraints,
   * `d_uv`: ultraviolet completion and renormalization behavior,
   * `d_internal`: internal consistency (anomalies, unitarity, etc.).

2. Weight vector constraints

   Each encoding in `E_QG` uses a weight vector

   ```txt
   w = (w_local, w_cosmo, w_bh, w_uv, w_internal)
   ```

   with:

   ```txt
   w_d > 0 for all d in D_QG
   sum over d in D_QG of w_d = 1
   ```

   There is a fixed minimal weight `w_min > 0` such that `w_d >= w_min` for all
   `d`. This prevents any dimension from being silently ignored.

3. Fairness rule

   The weight vector `w` and any normalization scales for the observables are
   chosen:

   * before inspecting the detailed scores of individual candidates,
   * by a procedure that depends only on high level considerations such as
     experimental precision and perceived importance of regimes.

   In particular:

   * `w` cannot depend on the specific candidate index `c`,
   * `w` cannot be adjusted on a per candidate basis after seeing results,
   * any change to `w` must be applied to the entire candidate library and
     recorded as a new encoding version.

4. Finite aggregation

   All tension functionals defined below are finite sums over the finite sets
   `Library_QG`, `Library_env`, and `D_QG`. No limiting processes or suprema
   over infinite families are used in this entry. This prevents hiding
   divergences behind poorly defined limits at the effective layer.

### 3.3 Observables and mismatch functionals

For each state `m = (c, e, X)` in `M_QG`, each encoding in `E_QG` provides
well defined nonnegative mismatch values

```txt
DeltaS_QG(m; d) >= 0  for each d in D_QG.
```

The interpretation is:

* `DeltaS_QG(m; d)` measures how strongly candidate `c`, when evaluated under
  envelope `e`, fails to satisfy the constraints assigned to dimension `d`.

We assume:

* `DeltaS_QG(m; d) = 0` indicates perfect agreement with the reference envelope
  for that dimension,
* larger values indicate stronger tension or inconsistency.

We do not specify the detailed formulas for `DeltaS_QG(m; d)`; we only assume
they are well defined real numbers on a regular subset of `M_QG`.

### 3.4 Candidate level tension and library tension

For each state `m`, we define the candidate level tension as:

```txt
Tension_QG(m) = sum over d in D_QG of w_d * DeltaS_QG(m; d)
```

where `w` satisfies the fairness rules above.

For a fixed envelope `e`, we obtain for each candidate `c` a tension value

```txt
Tension_QG(c; e)
```

by evaluating `Tension_QG(m)` at a state `m` with that `(c, e)` pair.

For a given encoding and envelope, we can define:

* minimal tension among candidates:

  ```txt
  T_min(e) = min over c in Library_QG of Tension_QG(c; e)
  ```

* second best tension:

  ```txt
  T_second(e) = second smallest value of Tension_QG(c; e)
  ```

* selection gap:

  ```txt
  Gap_select(e) = T_second(e) - T_min(e)
  ```

on the understanding that for `K < 2` candidates the selection gap is not
defined.

These quantities are finite because the candidate library is finite.

### 3.5 Singular set and domain restrictions

Some states may fail to admit well defined mismatch values. We define the
singular set:

```txt
S_sing = { m in M_QG : DeltaS_QG(m; d) is undefined or not finite for some d }
```

We then define the regular domain:

```txt
M_QG_reg = M_QG \ S_sing
```

and impose:

* All tension related statements in this entry are restricted to states in
  `M_QG_reg`.
* If a proposed experiment or encoding would require evaluating
  `DeltaS_QG(m; d)` for a state in `S_sing`, this is treated as "out of domain"
  for Q033, not as evidence for or against any candidate theory.

This prevents apparent divergences from being misinterpreted as physical
selection signals.

---

## 4. Tension principle for this problem

### 4.1 Core consistency_tension functional

At the effective layer, Q033 is governed by the following principle.

For each encoding in `E_QG` and each envelope `e` in `Library_env`, we can
compute `Tension_QG(c; e)` for all candidates `c` in `Library_QG`. The
consistency_tension structure is given by:

* the distribution of `Tension_QG(c; e)` across candidates,
* the selection gaps `Gap_select(e)`,
* and how these quantities behave across different envelopes and encoding
  versions.

We can summarize the selection situation for a given encoding and envelope by
the vector

```txt
Sigma_QG(e) = { Tension_QG(c; e) for all c in Library_QG }
```

together with `Gap_select(e)` when defined.

### 4.2 Low selection tension regime

A low selection tension regime is characterized by:

1. Existence of a robustly best candidate

   There exists a candidate `c_star` such that, for a wide range of envelopes
   `e` in `Library_env` and admissible encodings in `E_QG`,

   ```txt
   Tension_QG(c_star; e) is close to T_min(e)
   Gap_select(e) is bounded below by some gamma_QG > 0
   ```

   where `gamma_QG` does not shrink to zero under modest changes of weights
   and normalization within the fairness rules.

2. Cross envelope coherence

   The identity of `c_star` does not change when moving across envelopes that
   represent qualitatively different regimes (for example local tests, black
   hole constraints, cosmology), except possibly in domains where the data are
   explicitly declared incomplete.

3. Stability under encoding refinements

   When encodings are refined in ways that add resolution but preserve the
   observable set and fairness rules, the tension values and selection gaps
   move within controlled bands and do not exhibit violent reordering of the
   candidate ranking.

### 4.3 High selection tension (landscape) regime

A high selection tension regime is characterized by one or more of:

1. Persistent near degeneracy

   For many envelopes `e` and admissible encodings, `Gap_select(e)` remains
   very small, such that different candidates can trade places as the best
   option under small, allowed changes in weights or normalization.

2. Regime dependent winners

   Different envelopes favor different candidates in a way that cannot be
   reconciled with a single robust `c_star`. For example, one candidate may
   perform best under local tests while another performs best under black hole
   constraints, with no consistent winner across all.

3. Sensitivity to encoding details

   Small changes within the fairness allowed variations of the encoding
   (for example minor reweighting of dimensions) can substantially reorder the
   ranking of candidates, indicating that no candidate has a robust tension
   advantage.

In such a regime, selection remains ambiguous at the effective layer, and the
problem functions more like a "landscape" question than a sharp selection.

---

## 5. Counterfactual tension worlds

We describe three counterfactual worlds, strictly at the effective layer:

* World S: sharp selection world,
* World L: landscape world,
* World M: mixed emergent world.

These are not microscopic theories, only patterns of tension behavior and
selection outcomes.

### 5.1 World S (sharp selection)

World S is defined by the following effective layer pattern.

1. Unique robust candidate

   There exists a candidate `c_star` such that, for all envelopes `e` in
   `Library_env` and all encodings in `E_QG` that satisfy the fairness rules,

   ```txt
   Tension_QG(c_star; e) <= Tension_QG(c; e) - gamma_QG
   ```

   for all other candidates `c` and some fixed `gamma_QG > 0`.

2. Cross regime agreement

   The same `c_star` minimizes tension in local tests, cosmology, black hole
   constraints, and ultraviolet behavior, up to small, controlled variability
   determined by experimental uncertainties and modeling choices.

3. Encodings converge

   As encodings are refined by including more accurate data and better envelope
   modeling, the selection gaps remain stable or even grow, confirming the
   dominance of `c_star` rather than eroding it.

In this world, Q033 is effectively resolved toward a single winner at the
effective layer.

### 5.2 World L (landscape)

World L is defined by persistent selection ambiguity.

1. Candidate near ties

   For many envelopes `e`, two or more candidates satisfy

   ```txt
   |Tension_QG(c_i; e) - Tension_QG(c_j; e)| <= epsilon_QG
   ```

   for small `epsilon_QG`, and small allowed changes of the encoding easily
   swap their ranking.

2. Regime fragmentation

   Some envelopes favor one candidate, others favor another, without any
   candidate maintaining an advantage across all major regimes. There is no
   stable `c_star` that dominates under all constraints.

3. Refinement does not resolve choices

   As data become more precise and modeling improves, the selection ambiguity
   does not disappear. In some cases the library tension picture becomes more
   complex, not simpler.

In this world, Q033 remains an open, structural landscape problem even at
very high effective detail.

### 5.3 World M (mixed emergent)

World M describes a situation where no single candidate library entry is
sufficient, but low tension is achieved by emergent combinations.

1. Patchwork low tension

   For different envelopes, different candidates minimize tension, but a
   patchwork of effective descriptions can be combined to yield low global
   tension if one allows context dependent use of frameworks.

2. Composite effective description

   There is no single microscopic theory in `Library_QG` with minimal tension
   everywhere. Instead, combined use of several candidates, together with
   effective coarse graining rules, yields the lowest achievable tension.

3. Selection problem shifts

   In this world, Q033 is not resolved by naming one winner. Instead, the
   selection problem shifts toward understanding how different frameworks
   should be combined, and what higher level principles control the patchwork.

These worlds are conceptual tools for reading the tension patterns; they do
not assert any specific microscopic ontology.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols at the effective layer that can:

* test the coherence of the Q033 encoding,
* discriminate between different tension encodings,
* and provide evidence about whether we are in a sharp selection or a
  landscape regime.

They do not prove or disprove any particular candidate quantum gravity theory.

### Experiment 1: Cross regime tension profiling

*Goal:*
Test whether the Q033 tension encoding can produce stable, interpretable
selection gaps across a realistic set of envelopes.

*Setup:*

* Choose a concrete finite subset of `Library_QG` and `Library_env` that
  reflects:

  * local gravity tests,
  * cosmological data,
  * black hole related constraints,
  * ultraviolet completion considerations.

* For each pair `(c, e)`, build an effective state `m = (c, e, X)` in
  `M_QG_reg` that summarizes the candidate's behavior under the envelope
  constraints.

* Use a fixed encoding in `E_QG` with a specified weight vector `w` satisfying
  the fairness rules.

*Protocol:*

1. For each `m = (c, e, X)`, evaluate `DeltaS_QG(m; d)` for all `d` in `D_QG`.
2. Compute `Tension_QG(c; e)` and derive `T_min(e)`, `T_second(e)`, and
   `Gap_select(e)` where applicable.
3. Repeat the evaluation under a small set of alternative encodings in `E_QG`,
   for example by slightly varying `w` within the allowed fairness bounds.
4. Record how the ranking of candidates and selection gaps vary across
   envelopes and encodings.

*Metrics:*

* For each envelope `e`, the mean and variance of `Tension_QG(c; e)` across
  candidate and encoding choices.
* The minimal and maximal values of `Gap_select(e)` across encodings.
* A qualitative classification into:

  * sharp selection (large, stable gaps),
  * weak preference (small gaps, modest stability),
  * no clear selection (gaps near zero and unstable).

*Falsification conditions:*

* If under all admissible encodings the mismatch values or tensions cannot be
  defined on a substantial portion of `M_QG` without entering `S_sing`, then
  the current observable design or encoding is considered invalid for Q033.
* If tiny, fairness allowed changes of weights lead to arbitrarily large
  changes in candidate ranking, the encoding is treated as unstable and
  rejected at the effective layer.

*Semantics implementation note:*
The hybrid nature of `M_QG` means candidate indices are discrete while
observables are treated as continuous real values. The experiment uses only
finite sums over candidates, envelopes, and dimensions, which is consistent
with the hybrid semantics declared in the metadata.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

### Experiment 2: Model world discrimination with simplified toy frameworks

*Goal:*
Check whether the Q033 encoding can reliably distinguish between toy
frameworks that emulate key features of sharp selection and landscape worlds.

*Setup:*

* Construct simplified toy models that play the role of candidate frameworks:

  * Family S: toy candidates designed so that one member clearly satisfies all
    constraints better than others across envelopes.
  * Family L: toy candidates constructed such that several members can be made
    nearly indistinguishable in performance across constraints.

* For each toy candidate and envelope, construct states `m` in `M_QG_reg` with
  well defined mismatch values `DeltaS_QG(m; d)`.

*Protocol:*

1. Evaluate `Tension_QG(c; e)` and `Gap_select(e)` for all toy candidates and
   envelopes using a fixed encoding in `E_QG`.
2. Check whether Family S realizations are classified as sharp selection
   cases (large, stable gaps) and Family L realizations as landscape cases
   (small, unstable gaps).
3. Repeat the procedure for several plausible choices of weights and envelope
   definitions within the fairness rules.

*Metrics:*

* Frequency with which toy sharp selection worlds are correctly identified as
  sharp.
* Frequency with which toy landscape worlds are correctly identified as
  landscape.
* Sensitivity of classification to encoding choices.

*Falsification conditions:*

* If the encoding consistently misclassifies toy worlds (for example labeling
  sharp selection toys as landscape or vice versa) under reasonable parameter
  ranges, then the current tension design is rejected for Q033.
* If misclassification can only be corrected by violating fairness rules
  (for example by tuning weights differently for each candidate), the encoding
  is considered untrustworthy.

*Semantics implementation note:*
Toy frameworks are evaluated using the same finite observable set and
aggregation rules as real candidates. This keeps the semantics consistent and
prevents hidden complexity from entering only at the toy level.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

## 7. AI and WFGY engineering spec

This block describes how Q033 can be instantiated as an engineering module
for AI systems within the WFGY framework, still at the effective layer.

### 7.1 Training signals

We define several training signals that can be used in AI models to encourage
structured reasoning about quantum gravity selection.

1. `signal_qg_tension_profile`

   * Definition: vector valued signal whose components are the normalized
     `DeltaS_QG(m; d)` values over `d` in `D_QG`.
   * Purpose: expose to the model how each candidate performs along different
     constraint dimensions when reasoning about quantum gravity.

2. `signal_qg_selection_gap`

   * Definition: scalar signal equal to `Gap_select(e)` for the current
     envelope, when at least two candidates are available.
   * Purpose: indicate how sharp or ambiguous the selection is in the current
     regime.

3. `signal_qg_consistency_penalty`

   * Definition: penalty proportional to `Tension_QG(c; e)` for the candidate
     implicitly favored in the model's internal representation.
   * Purpose: discourage reasoning paths that implicitly pick high tension
     frameworks without acknowledging their weaknesses.

4. `signal_qg_world_mode`

   * Definition: discrete or soft label indicating whether the current scenario
     is being treated as World S, World L, or World M for the sake of a
     thought experiment.
   * Purpose: help the model separate reasoning under different global
     assumptions rather than mixing them incoherently.

### 7.2 Architectural patterns

We outline module patterns that reuse Q033 structures without exposing any
deep TU generative rules.

1. `QG_Candidate_Head`

   * Role: given an internal representation of a physical context (for example
     a passage about quantum gravity), predict a distribution over candidate
     labels in `Library_QG` together with an estimated tension vector
     `(DeltaS_QG(m; d))`.
   * Interface: inputs are embeddings of the context; outputs are candidate
     probabilities and mismatch estimates.

2. `QG_Selection_Evaluator`

   * Role: compute `Tension_QG(c; e)` and `Gap_select(e)` at the effective
     layer for a chosen envelope, using the outputs of the candidate head.
   * Interface: provides scalar scores usable by training or inference time
     filters.

3. `TU_QG_Observer`

   * Role: generic observer that can be attached to complex reasoning chains,
     extracting simplified Q033 relevant summaries without changing the
     underlying model weights.
   * Interface: yields logging information such as profiles over `D_QG` and
     approximate world mode classification (S, L, or M) for diagnostics.

### 7.3 Evaluation harness

We propose an evaluation harness for AI models augmented with Q033 modules.

1. Task design

   * Collect a suite of questions and prompts about quantum gravity frameworks,
     selection principles, and landscape vs unique theory debates.

2. Baseline condition

   * The AI model answers questions without explicit use of Q033 modules,
     only using its general knowledge.

3. TU enhanced condition

   * The AI model answers the same questions but is instructed to:

     * expose a candidate distribution over `Library_QG`,
     * estimate mismatch components per dimension,
     * and consider selection gaps when drawing conclusions.

4. Metrics

   * Consistency of reasoning across related prompts (for example whether the
     same framework is implicitly favored in logically similar scenarios).
   * Clarity in distinguishing World S vs World L style reasoning when
     questions explicitly ask for both possibilities.
   * Reduction of informal contradictions about how many theories remain
     viable and why.

### 7.4 60 second reproduction protocol

A minimal protocol to let external users experience Q033 style reasoning
in an AI system.

*Baseline step*

* Prompt the AI with:

  * a short summary of several quantum gravity frameworks,
  * and a question about whether current evidence strongly favors one.

* Observe whether the answer:

  * mixes arguments without structure,
  * or jumps between "string theory wins" and "landscape" talk without
    clear criteria.

*TU encoded step*

* Repeat the question but instruct the AI to:

  * list candidates in `Library_QG`,
  * describe the constraints grouped into `D_QG`,
  * report qualitative mismatch levels per dimension,
  * and explicitly state whether the pattern looks like World S, L, or M.

*Comparison metric*

* Evaluate whether the TU encoded answer:

  * separates dimensions of constraint more clearly,
  * states explicit selection gaps or lack thereof,
  * and makes the underlying ambiguity or preference more transparent.

This protocol can be implemented quickly and logged without revealing any
internal TU generative mechanism.

---

## 8. Cross problem transfer template

### 8.1 Reusable components produced by this problem

1. ComponentName: `QG_Selection_Tension_Score`

   * Type: functional

   * Minimal interface:

     * Inputs: `candidate_label`, `envelope_label`, `dimension_mismatches`
       as a map from `D_QG` to nonnegative real numbers.
     * Output: `tension_value` (a nonnegative scalar) and optionally
       `selection_gap` when multiple candidates are provided.

   * Preconditions:

     * The mismatch map must be defined for all dimensions in `D_QG`.
     * Weights must satisfy the fairness constraints (positive, sum to one).

2. ComponentName: `QG_Candidate_Profile_Descriptor`

   * Type: descriptor

   * Minimal interface:

     * Inputs: `candidate_label`, `envelope_label`.
     * Output: `profile_vector` summarizing qualitative properties such as:

       * background dependence,
       * ultraviolet behavior,
       * black hole treatment,
       * and typical cosmological implications.

   * Preconditions:

     * Profiles are coarse summaries suitable for qualitative comparison and
       do not attempt to encode full equations of motion.

3. ComponentName: `MultiFramework_Selection_Template`

   * Type: experiment_pattern

   * Minimal interface:

     * Inputs: `candidate_set`, `envelope_set`, `observable_dimensions`.
     * Output: a standardized protocol for computing mismatch values,
       tensions, and selection gaps, plus classification into World S, L, or M
       like regimes.

   * Preconditions:

     * The candidate set and envelope set must be finite.
     * All observables must be well defined on the chosen state space.

### 8.2 Direct reuse targets

1. Q040 (BH_PHYS_QBLACKHOLE_INFO_L3_040)

   * Reused components: `QG_Selection_Tension_Score`,
     `MultiFramework_Selection_Template`.
   * Why it transfers: different proposed resolutions of the black hole
     information problem can be treated as competing frameworks, with tensions
     computed against information theoretic constraints.

2. Q059 (BH_CS_INFO_THERMODYN_L3_059)

   * Reused components: `QG_Candidate_Profile_Descriptor`,
     `MultiFramework_Selection_Template`.
   * Why it transfers: information processing architectures and their
     thermodynamic properties can be compared using the same multi framework
     selection logic.

3. Q123 (BH_AI_INTERP_L3_123)

   * Reused components: `QG_Selection_Tension_Score` (renamed in context),
     `MultiFramework_Selection_Template`.
   * Why it transfers: interpretability frameworks for AI models can be
     treated as competing candidates, with tensions defined against
     desiderata such as faithfulness, robustness, and usability.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E1

  * The effective layer structure for candidate and envelope libraries, mismatch
    observables, and selection tensions is specified.
  * Fairness rules and finite aggregation constraints are explicitly stated.

* N_level: N1

  * The narrative of sharp selection vs landscape vs mixed emergent worlds is
    clearly formulated at a conceptual level.
  * Concrete numerical instantiations are still largely schematic.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following should be implemented:

1. A working prototype that:

   * instantiates a finite `Library_QG` and `Library_env`,
   * computes approximate `DeltaS_QG(m; d)` using published constraints,
   * and publishes tension profiles and selection gaps for different encoding
     choices.

2. A toy model study that:

   * uses simplified candidate and envelope models,
   * demonstrates clear discrimination between toy sharp selection and
     landscape worlds under the Q033 encoding,
   * and makes all code and data publicly available for independent checks.

Both are compatible with the effective layer because they operate only on
observable summaries and do not expose any deep TU generative rules.

### 9.3 Long term role in the TU program

In the long term, Q033 is expected to serve as:

* the canonical prototype for multi framework selection tension problems in
  physics,
* a staging ground for designing more refined selection principles that may
  eventually interact with experimental programs,
* and a bridge from high level theoretical debates about quantum gravity to
  AI and information theory problems that share the same multi framework
  structure.

---

## 10. Elementary but precise explanation

In everyday language, Q033 is about the following situation.

Physicists have several big ideas for how spacetime and gravity might work
when quantum effects are fully taken into account. String theory is one,
loop quantum gravity is another, and there are several more. Each idea has
its own strengths, weaknesses, and open questions.

The hard question is not how to write down one such theory in detail, but
how to decide which, if any, matches our universe best, given that:

* experiments cannot directly reach the very tiny scales where these theories
  differ most,
* many different versions of each theory are possible,
* and it is easy to adjust details to avoid simple contradictions.

In the Tension Universe view, we do not claim to solve this. Instead, we
build a careful bookkeeping system.

* We list a finite set of candidate frameworks.
* We list a finite set of constraint bundles (local tests, cosmology,
  black holes, ultraviolet behavior, internal consistency).
* For each pair, we imagine a state that summarizes how that candidate behaves
  under that bundle of constraints.

Then we define mismatch scores that say, in plain numbers, how much trouble
each candidate has with each kind of constraint. By combining these scores
in a fair way, we get a tension value for each candidate and each constraint
bundle, plus a measure of how clearly one candidate beats the others.

If one candidate is consistently better across all bundles, with a clear
margin, we are in a "sharp selection" world. If several candidates remain
neck and neck, and the rankings change easily when we adjust reasonable
weights, we are in a "landscape" world. If different candidates work best
in different situations and we need to combine them, we are in a "mixed
emergent" world.

This does not tell us which of these three worlds we actually live in.
It does not prove any theory right or wrong. But it:

* makes the selection problem precise in terms of observable summaries,
* enforces explicit fairness and avoids hidden parameter tuning,
* and provides reusable tools for other problems where we must choose among
  several big frameworks that all claim to describe the same reality.

Q033 is therefore the reference template for "string theory vs alternatives"
seen as a structured tension problem, not as a popularity contest.
