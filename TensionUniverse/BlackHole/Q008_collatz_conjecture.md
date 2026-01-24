# Q008 · Collatz conjecture

## 0. Header metadata

```txt
ID: Q008
Code: BH_MATH_COLLATZ_L3_008
Domain: Mathematics
Family: Discrete dynamics and Diophantine trajectories
Rank: S
Projection_dominance: I
Field_type: dynamical_field
Tension_type: computational_tension
Status: Open
Semantics: discrete
E_level: E1
N_level: N1
Last_updated: 2026-01-24
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Define the map `T` on positive integers as follows:

```txt
T(n) = n / 2    if n is even
T(n) = 3 * n + 1 if n is odd
```

Given a starting integer `n >= 1`, define its Collatz orbit as the sequence

```txt
n_0 = n
n_{k+1} = T(n_k) for k >= 0
```

The classical form of the Collatz conjecture (the `3 * n + 1` problem) is:

> For every positive integer `n`, the orbit of `n` under `T` eventually reaches the cycle `1 -> 4 -> 2 -> 1`.

Equivalently, every positive integer is conjectured to have a finite total stopping time, where the total stopping time of `n` is the smallest `k` such that `n_k = 1`, if such a `k` exists.

### 1.2 Status and difficulty

The Collatz conjecture is an open problem in number theory and discrete dynamics. It is easy to state, yet remains unresolved despite extensive numerical and theoretical work.

Known partial results include:

* It has been verified by computer for very large ranges of starting values (up to at least `n` on the order of `2^68` and beyond in various computations).
* Many structural properties of orbits are known, such as typical growth and decay patterns, parity structure, and the existence of long but ultimately terminating orbits.
* Terence Tao proved that for almost all starting values (in a density sense), the orbit eventually attains values that are bounded by a fixed power of the starting value. This provides strong evidence that non terminating behavior, if it exists, must be extremely rare.

However, no proof is known that every orbit reaches the trivial cycle, and no explicit counterexample has been found. The problem is widely regarded as very difficult and is often cited as a model case of a simple rule generating complex dynamics.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q008 has three roles:

1. Prototype of a discrete dynamical S problem:
   It is the benchmark example of a system where a very simple local update rule on integers induces globally hard to analyze orbit structure.

2. Testbed for computational_tension:
   It is used to define a tension functional that measures how well finite orbit statistics match a Collatz true world versus a world with non terminating behavior or nontrivial cycles.

3. Bridge to complexity and information problems:
   The discrete trajectory and stopping time ideas from Q008 transfer directly to problems in computational complexity (such as P vs NP) and information thermodynamics, where long discrete processes must be summarized and compared.

### References

1. Richard K. Guy, "Unsolved Problems in Number Theory", 3rd edition, Springer, 2004. Chapter on the `3 * n + 1` problem and related iterative maps.
2. Jeffrey C. Lagarias (editor), "The Ultimate Challenge: The 3x+1 Problem", American Mathematical Society, 2010.
3. Terence Tao, "Almost all orbits of the Collatz map attain almost bounded values", arXiv preprint arXiv:1909.03562, 2019, with subsequent journal publication.
4. Standard encyclopedia entry "Collatz conjecture" in a widely used mathematical encyclopedia or reference site.

---

## 2. Position in the BlackHole graph

This block describes how Q008 is embedded in the BlackHole graph. Edges are labeled with one line reasons that refer to concrete components or tension structures in this file.

### 2.1 Upstream problems

Upstream nodes provide prerequisites or general frameworks that Q008 reuses at the effective layer.

* Q016 (BH_MATH_ZFC_CONTINUUM_L3_016)
  Reason: Supplies foundational set and real line background used to speak about infinite orbits, densities of starting values, and limit behaviors that underlie the stopping time observables in Block 3.

* Q019 (BH_MATH_DIOPH_DENSITY_L3_019)
  Reason: Provides general Diophantine density and distribution tools that Q008 reuses when defining the observable `Obs_termination_ratio` and its interpretation as a density over starting values.

### 2.2 Downstream problems

Downstream nodes reuse Q008 components or depend on its discrete trajectory tension structure.

* Q051 (BH_CS_P_VS_NP_L3_051)
  Reason: Reuses the functional component `DiscreteTrajectory_Tension_008` from Block 8 as a toy model for the difficulty of predicting or verifying extremely long computation traces.

* Q053 (BH_CS_ONE_WAY_FUNCTIONS_L3_053)
  Reason: Reuses the field component `StoppingTimeField_Descriptor_008` from Block 8 to build intuition for one way like behavior in simple iterative maps.

### 2.3 Parallel problems

Parallel nodes share similar tension types without direct component reuse.

* Q006 (BH_MATH_GOLDBACH_L3_006)
  Reason: Both Q006 and Q008 are elementary number theoretic problems where computational_tension arises from the gap between simple local rules and globally elusive patterns.

* Q009 (BH_MATH_ODD_PERFECT_L3_009)
  Reason: Both study special integer structures with extreme rarity, where tension is driven by the difficulty of reconciling local multiplicative patterns with global classification.

### 2.4 Cross domain edges

Cross domain edges show where Q008 components transfer into other domains.

* Q051 (BH_CS_P_VS_NP_L3_051)
  Reason: Cross domain transfer of `DiscreteTrajectory_Tension_008` into complexity theory, where discrete iterative structure is used to reason about verification costs and resource limits.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Reuses `StoppingTimeField_Descriptor_008` as a toy discrete model of information flow and dissipation in stepwise processes.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. Only state spaces, observables, invariants, tension functionals, and singular sets are described. No rule is given for how raw Collatz data is mapped into internal Tension Universe fields.

### 3.1 State space

We assume an effective state space

```txt
M_008
```

with the following interpretation:

* Each state `m` in `M_008` encodes a coherent finite snapshot of Collatz like trajectories for a fixed and finite set of starting integers, together with summary statistics for those trajectories.
* For each refinement level `k`, there exists a designated set of starting integers up to a bound `N_k` and corresponding cutoffs on orbit length and maximal excursion.
* The exact representation of trajectories or statistics inside `m` is not specified. We only require that the observables defined below are well defined on `M_008`.

No explicit mapping from raw integers or step by step trajectories to `M_008` is given. The existence of suitable encodings is assumed.

### 3.2 Finite encoding library

We introduce a finite encoding library for Q008:

```txt
L_enc_008_finite = { Enc_orbit_length, Enc_max_excursion, Enc_parity_signature }
```

Intended roles:

* `Enc_orbit_length`
  Encodes summaries of total stopping times or truncated orbit lengths for starting values in a fixed finite set determined by refinement level `k`.

* `Enc_max_excursion`
  Encodes summaries of maximal values attained along orbits up to a cutoff determined by `k`.

* `Enc_parity_signature`
  Encodes compact summaries of parity or related symbolic patterns along orbits, again limited by refinement level `k`.

For each encoding `Enc` in `L_enc_008_finite`:

* Its internal structure and weights are fixed once and for all at the effective layer.
* It does not change as a function of observed data or experimental outcome.
* Refinement is represented by an integer index `k`, not by switching to a different encoding.

### 3.3 Observables and fields

On `M_008` we define the following effective observables. Each observable depends on a state `m` and a refinement index `k`.

1. Orbit length observable

```txt
Obs_orbit_length(m; k)
```

* Input: a state `m` that includes an encoding of trajectories up to refinement level `k`.
* Output: a finite vector or histogram that summarizes total stopping times or truncated lengths for starting values in a fixed set `S_k` with size depending on `k`, for example all `n` with `1 <= n <= N_k`.

2. Maximal excursion observable

```txt
Obs_max_excursion(m; k)
```

* Input: a state `m` at refinement level `k`.
* Output: a finite vector or histogram summarizing maximal orbit values attained for starting values in `S_k`, up to truncation limits compatible with `k`.

3. Termination ratio observable

```txt
Obs_termination_ratio(m; k)
```

* Input: a state `m` at refinement level `k`.
* Output: a scalar between `0` and `1` representing the fraction of starting values in `S_k` whose trajectories, as encoded in `m`, have reached the trivial cycle `1 -> 4 -> 2 -> 1` within the truncation limit for level `k`.

We do not specify how `Obs_orbit_length`, `Obs_max_excursion`, or `Obs_termination_ratio` are computed from raw trajectories. We only assume they are internally consistent and finite on the regular domain.

### 3.4 Reference profiles and mismatch functionals

We fix reference profiles in advance, independent of any specific state `m` in `M_008`.

1. Reference orbit length profile

For each refinement level `k`, there is a reference vector

```txt
Ref_orbit_length(k)
```

representing a hypothetical distribution of stopping times in a Collatz true world, consistent with current heuristic and analytic knowledge. This profile is chosen once and for all and does not depend on `m`.

2. Reference maximal excursion profile

For each `k`, there is a reference vector

```txt
Ref_max_excursion(k)
```

representing a hypothetical distribution of maximal orbit values for a Collatz true world, again fixed at the effective layer.

3. Mismatch functionals

We define nonnegative mismatch functionals:

```txt
DeltaS_length(m; k) >= 0
DeltaS_excursion(m; k) >= 0
```

One possible definition, stated in ASCII form, is:

```txt
DeltaS_length(m; k) =
    max over j in J_k of
    | L_obs(m; k, j) - L_ref(k, j) |

DeltaS_excursion(m; k) =
    max over j in E_k of
    | E_obs(m; k, j) - E_ref(k, j) |
```

where:

* `L_obs(m; k, j)` are components of `Obs_orbit_length(m; k)` indexed by `j` in a finite index set `J_k`.
* `L_ref(k, j)` are components of `Ref_orbit_length(k)`.
* `E_obs(m; k, j)` are components of `Obs_max_excursion(m; k)` indexed by `j` in a finite index set `E_k`.
* `E_ref(k, j)` are components of `Ref_max_excursion(k)`.

These definitions are examples. Any alternative definition must preserve:

* nonnegativity,
* zero mismatch if and only if observed and reference profiles match exactly at the resolution of `k`,
* monotone increase in mismatch magnitude when observed profiles diverge from reference profiles.

### 3.5 Combined Collatz tension functional

We define a combined tension functional

```txt
Tension_Collatz(m; k) =
    w_len * DeltaS_length(m; k)
  + w_exc * DeltaS_excursion(m; k)
```

where:

* `w_len >= 0`, `w_exc >= 0`,
* `w_len + w_exc = 1`,
* `(w_len, w_exc)` is chosen once and for all from a fixed finite set of admissible weight pairs `W_008_adm`.

Fairness constraints:

* The weight pair `(w_len, w_exc)` is not allowed to depend on the specific state `m` or the outcome of any experiment.
* The reference profiles `Ref_orbit_length(k)` and `Ref_max_excursion(k)` are fixed before any data are examined.
* All statements about low or high tension worlds are made relative to this fixed choice of weights and reference profiles.

### 3.6 Effective tension tensor

Consistent with the general Tension Universe core, we introduce an effective tension tensor

```txt
T_ij(m; k) =
    S_i(m; k) * C_j(m; k)
  * Tension_Collatz(m; k)
  * lambda(m; k) * kappa_008
```

where:

* `S_i(m; k)` represents source like contributions from the i th semantic component of the Collatz context at refinement level `k`.
* `C_j(m; k)` represents receptivity of the j th downstream component to Collatz related tension.
* `lambda(m; k)` encodes the local convergence or divergence state of reasoning about Collatz at refinement level `k`, with values in a bounded interval.
* `kappa_008` is a fixed coupling constant specific to Q008.

Indices `i` and `j` run over finite sets appropriate to the model. Their exact nature is not specified at the effective layer.

### 3.7 Singular set and domain restriction

Some states may encode incomplete or inconsistent information, leading to undefined or infinite mismatch measures. We define the singular set

```txt
S_sing_008 =
    { m in M_008 :
      DeltaS_length(m; k) or DeltaS_excursion(m; k)
      is undefined or not finite
      for some refinement level k }
```

The regular domain is

```txt
M_008_reg = M_008 \ S_sing_008
```

All Q008 tension statements are restricted to states in `M_008_reg`. If an experiment would require evaluating `Tension_Collatz(m; k)` for `m` in `S_sing_008`, the result is treated as out of domain rather than as evidence about the conjecture.

---

## 4. Tension principle for this problem

This block states the effective layer principle that Q008 uses to distinguish low tension and high tension worlds.

### 4.1 Core tension principle

At the effective layer, the Collatz conjecture is encoded as the claim that our universe belongs to a branch where discrete trajectory tension can be kept persistently low along a fixed refinement path.

We say that a sequence of states `m(k)` in `M_008_reg` follows a refinement path if:

* For each integer `k >= 1`, `m(k)` encodes summaries for starting values in `S_k` and truncation rules consistent with refinement level `k`.
* Refinement is implemented only by increasing `k`, not by changing the encoding or weight choices.

We then assert:

* Low tension branch:
  There exists a refinement path `m_T(k)` such that

  ```txt
  Tension_Collatz(m_T(k); k) <= epsilon_Collatz
  ```

  for all `k` beyond some baseline level, where `epsilon_Collatz` is a small constant that depends on modeling choices but does not grow with `k`.

* High tension branch:
  For any encoding that remains faithful to actual trajectories in a Collatz false world, there exists a refinement path `m_F(k)` and a threshold `delta_Collatz > 0` such that

  ```txt
  Tension_Collatz(m_F(k); k) >= delta_Collatz
  ```

  for infinitely many `k`.

The Collatz conjecture itself is expressed as the claim that the actual universe belongs to the low tension branch.

### 4.2 Stability and fairness conditions

The tension principle is subject to the following stability conditions:

* The encoding library `L_enc_008_finite` and weight set `W_008_adm` are fixed in advance.
* Reference profiles `Ref_orbit_length(k)` and `Ref_max_excursion(k)` may depend on `k` but not on which world branch we are in.
* High or low tension labels are not allowed to be adjusted retrospectively after observing data; all thresholds and profiles are fixed before experiments.

Under these conditions, the Collatz conjecture is rephrased as the existence of a low tension refinement path for some admissible encoding and weight choice in the fixed library, without retrospective parameter tuning.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds, purely in terms of observable patterns and tension behavior.

### 5.1 World T: Collatz true, low discrete trajectory tension

In World T:

1. Termination behavior

   * For each refinement level `k`, there exists a state `m_T(k)` in `M_008_reg` encoding orbit summaries for all starting values up to `N_k`.
   * The termination ratio satisfies

     ```txt
     Obs_termination_ratio(m_T(k); k) is close to 1
     ```

     with deviations that can be absorbed into the reference profiles and small modeling noise.

2. Orbit length patterns

   * The observable `Obs_orbit_length(m_T(k); k)` tracks `Ref_orbit_length(k)` within small bounded error, so that `DeltaS_length(m_T(k); k)` remains small and does not increase uncontrollably with `k`.

3. Maximal excursion patterns

   * The observable `Obs_max_excursion(m_T(k); k)` tracks `Ref_max_excursion(k)` within bounded error, keeping `DeltaS_excursion(m_T(k); k)` small.

4. Global tension

   * The combined tension satisfies

     ```txt
     Tension_Collatz(m_T(k); k) <= epsilon_Collatz
     ```

     for all sufficiently large refinement levels `k`, with `epsilon_Collatz` chosen in advance based on encoding library and expected noise.

### 5.2 World F: Collatz false, high discrete trajectory tension

In World F:

1. Non terminating or anomalous behavior

   * There exist starting values whose orbits do not reach the trivial cycle or enter nontrivial cycles that break the reference boundedness picture.
   * Any honest encoding that respects those trajectories will reflect this through orbit length or maximal excursion summaries.

2. Orbit length and excursion anomalies

   * Along some refinement path `m_F(k)` in `M_008_reg`, the mismatch functionals satisfy

     ```txt
     DeltaS_length(m_F(k); k) >= delta_length
     DeltaS_excursion(m_F(k); k) >= delta_excursion
     ```

     for infinitely many `k`, with positive thresholds that cannot be made arbitrarily small without contradicting the encoded trajectories.

3. Global tension

   * The combined tension satisfies

     ```txt
     Tension_Collatz(m_F(k); k) >= delta_Collatz
     ```

     for some `delta_Collatz > 0` and infinitely many `k`. This bound does not disappear under further refinement as long as encodings remain faithful.

### 5.3 Interpretive note

These worlds do not claim to construct raw trajectories within the Tension Universe formalism. They only specify the patterns that observable summaries and tension functionals would exhibit under the two scenarios.

---

## 6. Falsifiability and discriminating experiments

This block defines experiments that can falsify or validate specific Q008 encodings at the effective layer. They do not prove or disprove the Collatz conjecture itself, but they can reject poorly designed tension encodings.

### Experiment 1: Numerical discrete trajectory tension profile

*Goal:*
Test whether the chosen `Tension_Collatz` functional behaves in a stable and interpretable way when applied to actual computed Collatz trajectories up to large ranges.

*Setup:*

* Input: published or freshly computed data of Collatz orbits for all starting values `n` with `1 <= n <= N_k` for several refinement levels `k`.
* For each `k`, define a set `S_k` of starting values (for example `1` to `N_k`) and a truncation rule for maximal allowed steps and values.
* Fix a choice of encoding from `L_enc_008_finite`, a weight pair from `W_008_adm`, and reference profiles `Ref_orbit_length(k)` and `Ref_max_excursion(k)` prior to inspecting the detailed data.

*Protocol:*

1. For each `k`, construct a state `m_data(k)` in `M_008_reg` that encodes the following summaries for `S_k`:

   * stopping time distribution up to truncation limits,
   * maximal excursion distribution up to truncation limits,
   * termination ratio.
     The internal encoding method is not specified inside the Tension Universe formalism.
2. Evaluate `DeltaS_length(m_data(k); k)` and `DeltaS_excursion(m_data(k); k)` using the fixed reference profiles.
3. Compute `Tension_Collatz(m_data(k); k)` for each refinement level `k`.
4. Record the sequence of tension values and simple statistics such as maximum, mean, and variance across `k`.

*Metrics:*

* The sequence of tension values `Tension_Collatz(m_data(k); k)` as `k` increases.
* Stability of this sequence under modest variations of encoding within `L_enc_008_finite`.
* Sensitivity of the tension to known approximate behaviors of orbits (for example, presence of long orbits within the tested range).

*Falsification conditions:*

* If for every admissible choice of encoding and weights the observed `Tension_Collatz(m_data(k); k)` oscillates or grows in a way that clearly contradicts the intended low tension branch behavior in a Collatz true world, the current encoding is considered falsified at the effective layer.
* If small, justifiable changes in reference profiles lead to arbitrarily different qualitative conclusions about low or high tension behavior, the encoding is considered unstable and rejected.

*Semantics implementation note:*
All quantities are treated as discrete summaries over finite sets of starting values and orbits, consistent with the discrete metadata. No continuous approximations are required in this experiment.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can only reject or refine the Q008 encoding. It does not provide a proof or disproof of the Collatz conjecture.

---

### Experiment 2: Toy model comparison of terminating and non terminating maps

*Goal:*
Check whether the Q008 tension encoding can systematically distinguish between toy iterative maps that always terminate and toy maps that have engineered non terminating cycles.

*Setup:*

* Construct two families of maps on positive integers:

  * Family Ttoy: maps that mimic the structure of the Collatz map but are designed so that all orbits eventually reach a trivial cycle.
  * Family Ftoy: maps that are similar in complexity to the Collatz rule but are known to have non terminating or nontrivial cycles for some starting values.
* For each map in both families, compute or simulate trajectories for starting values in suitable finite sets `S_k` for several refinement levels.

*Protocol:*

1. For each map in Family Ttoy and each refinement level `k`, construct a state `m_Ttoy(k)` in `M_008_reg` that encodes orbit length, maximal excursion, and termination ratio summaries using one encoding from `L_enc_008_finite`.
2. For each map in Family Ftoy and each `k`, construct a state `m_Ftoy(k)` in `M_008_reg` with the same type of summaries.
3. Using fixed weights and reference profiles, compute `Tension_Collatz(m_Ttoy(k); k)` and `Tension_Collatz(m_Ftoy(k); k)` for all maps and refinement levels.
4. Compare the distributions of tension values between the two families.

*Metrics:*

* Mean and distribution of `Tension_Collatz` for Family Ttoy and Family Ftoy at each refinement level.
* Separation between the two distributions, for example in terms of differences in mean or quantiles.
* Robustness of the separation under changes of encoding inside the finite library.

*Falsification conditions:*

* If for reasonable encoding choices the tension values for Family Ttoy and Family Ftoy are systematically indistinguishable, the encoding fails to capture basic differences between terminating and non terminating behavior and is rejected.
* If the encoding consistently assigns lower tension to maps in Family Ftoy than to maps in Family Ttoy, contrary to their known termination properties, the encoding is considered misaligned and rejected.

*Semantics implementation note:*
Both families are treated as discrete iterative systems on integers, encoded using the same discrete framework as the actual Collatz map. The experiment does not rely on any continuous approximation.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. Success or failure on toy maps only tests the Q008 encoding, not the truth of the original Collatz conjecture.

---

## 7. AI and WFGY engineering spec

This block describes how Q008 can be used as a module inside AI systems, within the WFGY framework, at the effective layer.

### 7.1 Training signals

1. `signal_discrete_orbit_consistency`

   * Definition: a penalty signal proportional to the mismatch between internally implied orbit statistics and the reference profiles `Ref_orbit_length(k)` and `Ref_max_excursion(k)` when the context clearly assumes Collatz true behavior.
   * Purpose: encourage models to maintain coherent stopping time and excursion narratives when reasoning under a Collatz true background.

2. `signal_termination_ratio_alignment`

   * Definition: a signal based on how close the model implied `Obs_termination_ratio(m; k)` is to 1 in contexts where all starting values are assumed to terminate.
   * Purpose: penalize internal representations that imply widespread non termination under a Collatz true assumption.

3. `signal_tension_contrast_T_vs_F`

   * Definition: a signal that measures the difference in predicted `Tension_Collatz` when the model is prompted with explicit World T versus World F assumptions.
   * Purpose: teach the model to separate clearly between the two counterfactual worlds instead of mixing them.

4. `signal_discrete_dynamics_transfer`

   * Definition: a signal that rewards successful transfer of Q008 style discrete trajectory reasoning to other simple iterative systems, while maintaining low tension in known terminating cases.
   * Purpose: support generalization of discrete trajectory intuition beyond the Collatz map itself.

### 7.2 Architectural patterns

1. `DiscreteTrajectoryHead_008`

   * Role: specialized head that reads internal embeddings of a discrete dynamics context and outputs approximate summaries analogous to `Obs_orbit_length`, `Obs_max_excursion`, and `Obs_termination_ratio`.
   * Interface: takes a representation of the current problem state as input and returns a triple `(length_summary, excursion_summary, termination_score)` plus an optional tension estimate.

2. `TerminationConsistencyFilter_008`

   * Role: module that checks whether candidate statements about termination or non termination are consistent with low or high tension scenarios given Q008.
   * Interface: takes proposed statements and associated internal representations as input and returns a soft mask or score indicating whether they align with a low tension Collatz true narrative or with a high tension alternative.

3. `TU_DiscreteDynamics_Observer_008`

   * Role: generic observer that extracts from internal states the minimal information required to evaluate or approximate `Tension_Collatz`.
   * Interface: maps internal embeddings to a compact vector that is sufficient to compute approximate values of `DeltaS_length`, `DeltaS_excursion`, and `Tension_Collatz`.

### 7.3 Evaluation harness

An evaluation harness for AI models augmented with Q008 components can proceed as follows.

1. Task design

   * Construct a benchmark of discrete dynamics problems, including:

     * questions about Collatz like maps,
     * questions about other toy iterative maps with known termination properties,
     * mixed contexts where assumptions about termination are explicitly stated or explicitly denied.

2. Conditions

   * Baseline condition:

     * Model runs without Q008 specific modules or training signals.
   * TU encoded condition:

     * Model uses `DiscreteTrajectoryHead_008`, `TerminationConsistencyFilter_008`, and the training signals from Section 7.1.

3. Metrics

   * Accuracy on questions where termination properties are known.
   * Rate of internal contradictions, measured by how often the model in the same context asserts both that all orbits terminate and that some orbits do not.
   * Stability of answers when moving between World T and World F prompts.

4. Analysis

   * Compare the two conditions to see whether Q008 modules increase coherence and reduce contradictions in discrete trajectory reasoning.

### 7.4 60 second reproduction protocol

A simple protocol that allows external users to experience the impact of Q008 style encoding on AI behavior.

* Baseline setup

  * Prompt: Ask the model to explain why the Collatz conjecture is considered hard and how typical trajectories behave, with no mention of WFGY or tension.
  * Observation: Record whether the answer mixes numerical facts, heuristic statements, and termination claims in a coherent way or not.

* TU encoded setup

  * Prompt: Ask the same question, but instruct the model to organize the explanation around:

    * discrete trajectory statistics,
    * low versus high `Tension_Collatz`,
    * World T and World F counterfactuals.
  * Observation: Record whether the explanation becomes more structured, i.e. clearly separating observed summaries, heuristics, and counterfactual scenarios.

* Comparison metric

  * Use a simple rubric to rate:

    * clarity about what is known versus unknown,
    * explicit acknowledgment of the difference between proving termination and observing large finite ranges,
    * consistency between local statements and global conclusions.

* What to log

  * Prompts, full responses, any internal tension estimates and relevant intermediate summaries from Q008 modules.
  * These logs can be inspected later to evaluate whether the Q008 encoding improves coherence, without revealing any deep Tension Universe generative rules.

---

## 8. Cross problem transfer template

This block lists reusable components produced by Q008 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `DiscreteTrajectory_Tension_008`

   * Type: functional
   * Minimal interface:

     * Inputs: discrete trajectory summary vector for a finite set of starting states and a refinement index.
     * Output: nonnegative scalar tension value summarizing how well the trajectories match a low tension terminating pattern.
   * Preconditions:

     * Input summaries must be internally consistent and represent finite or truncated trajectories.

2. ComponentName: `StoppingTimeField_Descriptor_008`

   * Type: field
   * Minimal interface:

     * Inputs: description of a domain of starting states and refinement parameters.
     * Output: histogram or small vector summarizing total stopping times or analogous length measures.
   * Preconditions:

     * Domain and refinement parameters must be chosen so that stopping times or truncation rules are well defined.

3. ComponentName: `WorldT_WorldF_DiscreteCycle_Template_008`

   * Type: experiment_pattern
   * Minimal interface:

     * Inputs: a family of discrete maps with known or hypothesized termination behavior.
     * Output: two experiment descriptions, one for World T style behavior and one for World F style behavior, each including a tension evaluation method.
   * Preconditions:

     * Each map must have a clearly defined update rule and configuration space, such that finite trajectory summaries are meaningful.

### 8.2 Direct reuse targets

1. Q051 (BH_CS_P_VS_NP_L3_051)

   * Reused components: `DiscreteTrajectory_Tension_008`, `StoppingTimeField_Descriptor_008`.
   * Why it transfers:

     * Complexity problems often involve very long discrete computations. Discrete trajectory tension provides a way to reason about how computation length and structure relate to low or high tension regimes, without directly solving complexity class separations.
   * What changes:

     * Trajectories become computation traces rather than Collatz orbits. Stopping times become measures of computation duration or resource use.

2. Q053 (BH_CS_ONE_WAY_FUNCTIONS_L3_053)

   * Reused components: `StoppingTimeField_Descriptor_008`, `WorldT_WorldF_DiscreteCycle_Template_008`.
   * Why it transfers:

     * One way function candidates often rely on iterative structure. The Q008 template allows construction of low tension worlds where inversion is easy and high tension worlds where inversion appears difficult, with discrete trajectory summaries as the carrier.
   * What changes:

     * The fields now summarize difficulty of inversion or backward tracking rather than orbit termination.

3. Q059 (BH_CS_INFO_THERMODYN_L3_059)

   * Reused components: `DiscreteTrajectory_Tension_008`.
   * Why it transfers:

     * Q059 treats information processing as stepwise transformations. Q008 tension can be adapted to measure how far real processes deviate from simple toy models with predictable termination and energy like measures.

---

## 9. TU roadmap and verification levels

This block positions Q008 on the Tension Universe verification ladder and states the next measurable steps.

### 9.1 Current levels

* E_level: E1

  * A coherent effective encoding has been specified, including:

    * finite encoding library `L_enc_008_finite`,
    * mismatch functionals `DeltaS_length`, `DeltaS_excursion`,
    * combined tension `Tension_Collatz`,
    * singular set `S_sing_008`.
  * At least one concrete experiment with explicit falsification conditions has been defined.

* N_level: N1

  * World T and World F have been described through discrete trajectory tension patterns.
  * Basic cross problem transfer directions have been identified but not yet instantiated in full detail.

### 9.2 Next measurable step toward E2

To move Q008 from E1 to E2, one or more of the following should be implemented and documented outside this effective layer description:

1. A working implementation of one encoding from `L_enc_008_finite` that:

   * computes `Obs_orbit_length`, `Obs_max_excursion`, and `Obs_termination_ratio` from numerical data,
   * evaluates `DeltaS_length`, `DeltaS_excursion`, and `Tension_Collatz` for several refinement levels.

2. A set of published experimental results for the numerical trajectory tension profile experiment in Block 6, including:

   * tables of tension values across `k`,
   * discussion of stability under changes of encoding within the finite library.

3. A demonstration of the toy map experiment in Block 6, showing:

   * clear separation in tension distributions between terminating and non terminating families,
   * robustness of the result under modest encoding changes.

These steps stay at the effective layer. They do not reveal any deep generative rules of the Tension Universe.

### 9.3 Long term role in the TU program

In the long term, Q008 is expected to serve as:

* A reference node for discrete dynamical S problems with simple rules and hard global behavior.
* A test case for how computational_tension functionals should be designed in order to be falsifiable yet robust.
* A bridge to complexity, cryptography, and information thermodynamics, where long discrete processes need to be summarized in tension based ways.

---

## 10. Elementary but precise explanation

This block gives a precise but accessible explanation of Q008 in everyday language, aligned with the effective layer description.

The Collatz conjecture is about a very simple game played with positive integers. The rule is:

* If the number is even, divide it by 2.
* If the number is odd, multiply it by 3 and add 1.

You repeat this rule over and over. The conjecture says that no matter which positive integer you start with, if you follow this rule, you will eventually reach the loop `1, 4, 2, 1, 4, 2, 1, ...`.

This is easy to simulate on a computer for many numbers, and all tested numbers have reached the loop. Yet nobody has proved that this always happens, and nobody has found a number that does not.

In the Tension Universe picture, we do not try to prove the conjecture directly. Instead, we treat the behavior of many trajectories at once as a kind of discrete field and ask:

* How long do these trajectories take to reach the loop?
* How high do they climb before they come back down?
* What fraction of starting numbers appear to reach the loop within a reasonable number of steps?

For each batch of starting numbers, we summarize this information in a compact way and compare it to a reference pattern that would be natural if the conjecture is true. The difference between what we see and what the reference pattern suggests is called the Collatz tension.

We then imagine two kinds of worlds:

* In a Collatz true world, there should be a way to look at bigger and bigger batches of starting numbers so that the Collatz tension stays small and does not explode.
* In a Collatz false world, if we are honest about what the trajectories do, the tension should eventually stay noticeably large no matter how we refine our view.

This does not prove anything by itself. What it does provide is:

* a clear way to talk about what we can measure from many trajectories at once,
* a way to design experiments that can reject bad ways of summarizing or scoring this behavior,
* a small collection of components that can be reused in other problems where simple rules create complex discrete dynamics.

Q008 is therefore the discrete trajectory benchmark of the Tension Universe. It shows how to encode a famous open problem as a tension structure while respecting strict boundaries: we only talk about observable summaries and consistency patterns, and we do not claim any hidden generative rule or proof at the deep level.
