# Q009 · Odd perfect numbers

## 0. Header metadata

```txt
ID: Q009
Code: BH_MATH_ODDPERF_L3_009
Domain: Mathematics
Family: Number theory (multiplicative / divisor)
Rank: S
Projection_dominance: I
Field_type: combinatorial_field
Tension_type: consistency_tension
Status: Open
Semantics: discrete
E_level: E1
N_level: N1
Last_updated: 2026-01-24
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

For a positive integer `n`, let `sigma(n)` denote the sum of all positive divisors of `n`.

An integer `n` is called perfect if

```txt
sigma(n) = 2 * n
```

Equivalently, the sum of all positive divisors of `n` equals twice `n`.

Classically:

* There are infinitely many **even** perfect numbers if and only if there are infinitely many Mersenne primes.
* All known perfect numbers are even and have the form

  ```txt
  n = 2^(p - 1) * (2^p - 1)
  ```

  where `2^p - 1` is prime.

The **odd perfect number problem** asks:

> Does there exist any odd integer `n` such that `sigma(n) = 2 * n`?

Equivalently:

* Are there any **odd perfect numbers**, or are all perfect numbers necessarily even?

### 1.2 Status and difficulty

The problem remains open. No odd perfect number is known, and no proof of impossibility is known.

Partial results include:

* If an odd perfect number exists, it must be extremely large (far beyond current computational bounds).

* It must have a very constrained prime factorization:

  * It must be divisible by at least one prime raised to a high power.
  * It must satisfy tight relationships between its prime factors, exponents, and the structure of `sigma(n)`.

* Many necessary conditions have been derived:

  * Lower bounds on the number of distinct prime factors.
  * Congruence conditions on prime factors.
  * Restrictions on the exponents of primes in its factorization.

Despite significant progress on these necessary conditions and large computational searches, the existence question remains unresolved. It is considered one of the central unsolved problems of multiplicative number theory.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q009 plays several roles:

1. It is the canonical example of a **consistency_tension** problem in discrete multiplicative number theory, where many local constraints must jointly fit a global equality `sigma(n) = 2 * n`.

2. It provides a test bed for Tension Universe encodings of:

   * discrete state spaces of factorization data,
   * divisor sum observables,
   * consistency-based tension functionals.

3. It generates reusable components for other problems where:

   * strong necessary conditions are known,
   * no examples are known,
   * and the main issue is whether the constraint system can be jointly satisfied at all.

### References

1. R. K. Guy, “Unsolved Problems in Number Theory”, 3rd edition, Springer, 2004. See the chapter on perfect numbers and related problems.
2. P. P. Nielsen, “An upper bound for odd perfect numbers”, Journal of Number Theory, 2015. Survey style discussion and improved bounds on hypothetical odd perfect numbers.
3. P. Hagis and W. L. McDaniel, “On the structure of odd perfect numbers”, Various papers in number theory journals, 1980s and 1990s, describing factorization constraints and structural properties.

---

## 2. Position in the BlackHole graph

This block records how Q009 sits inside the BlackHole graph among Q001–Q125. Each edge is listed with a one-line reason pointing to a concrete component or tension concept.

### 2.1 Upstream problems

These provide prerequisites, tools, or general frameworks that Q009 relies on at the effective layer.

* Q001 (BH_MATH_NUM_L3_001 · Riemann Hypothesis)
  Reason: Supplies the general perspective on multiplicative number theory and Dirichlet series that underlies the divisor sum observable and its analytic interpretations, reused in the `DivisorProfileDescriptor` component.

* Q005 (BH_MATH_ABC_CONJ_L3_005 · abc conjecture)
  Reason: Provides a general framework for tension between additive and multiplicative structure for integers, which is reused conceptually in the consistency constraints of `OddPerfectTensionFunctional`.

* Q019 (BH_MATH_DIOPH_DENSITY_L3_019 · Diophantine density problems)
  Reason: Provides tools for thinking about how sparse certain special sets of integers can be, which informs the way Q009 treats the possible “density zero” nature of odd perfect numbers within the `ConstraintSaturationWorld_OPN` pattern.

### 2.2 Downstream problems

These problems directly reuse the components of Q009.

* Q020 (BH_MATH_MULT_FUNC_STRUCT_L3_020 · structure of multiplicative functions)
  Reason: Reuses `DivisorProfileDescriptor` to study more general multiplicative functions and their divisor-like behavior.

* Q021 (BH_MATH_EXTREME_DIVISOR_L3_021 · extreme values of divisor sums)
  Reason: Reuses `OddPerfectTensionFunctional` as a special case of extreme divisor sum consistency tension.

* Q023 (BH_MATH_SPARSE_SPECIAL_SET_L3_023 · sparsity of special integer sets)
  Reason: Uses `ConstraintSaturationWorld_OPN` as a template for building worlds where special integer classes are either empty or extremely sparse.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component reuse.

* Q007 (BH_MATH_TWINPRIME_L3_007 · twin primes)
  Reason: Both Q007 and Q009 study extremely constrained integer patterns where many local conditions might forbid global existence, under a consistency_tension view.

* Q006 (BH_MATH_GOLDBACH_L3_006 · Goldbach type problems)
  Reason: Both problems sit in the space of “combinatorially plausible, globally unproven” structures where known constraints do not match current data in an obvious way.

### 2.4 Cross-domain edges

Cross-domain edges connect Q009 to problems in other domains that can reuse its components.

* Q059 (BH_CS_INFO_THERMODYN_L3_059 · information thermodynamics)
  Reason: Can reuse the idea of `ConstraintSaturationWorld_OPN` to model how extreme configurations in discrete state spaces may or may not be realized in physical or informational systems.

* Q123 (BH_AI_INTERP_L3_123 · AI interpretability via discrete structures)
  Reason: Reuses `DivisorProfileDescriptor` as an analogy for describing structured discrete features inside AI models (for example, factorization-like patterns in neuron activations).

---

## 3. Tension Universe encoding (effective layer)

All content in this block stays at the effective layer. We only describe:

* discrete state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rules or any mapping from raw computational data to internal TU fields.

### 3.1 State space

We assume a discrete semantic state space

```txt
M
```

with the following effective interpretation:

* Each `m` in `M` is a finite “odd-integer configuration” up to some search horizon `H(m)`, containing:

  * a finite set of odd positive integers,

  * for each such integer `n`, its prime factorization,

  * for each such `n`, the value `sigma(n)` and the normalized deficit

    ```txt
    deficit_rel(n) = (2 * n - sigma(n)) / (2 * n)
    ```

  * metadata describing which known necessary conditions for odd perfect numbers have been checked for each `n`.

We do not specify how the factorizations or `sigma(n)` values are computed or stored. We only require that:

* For any finite search bound `B`, there exist states `m` in `M` whose content reflects all odd `n` up to `B` together with consistent divisor sum and factorization summaries.

### 3.2 Effective fields and observables

On `M` we define the following discrete observables.

1. Minimal relative deficit

```txt
Delta_sigma_min(m) = inf over odd n in content(m) of deficit_rel(n)
```

If all deficits are positive, `Delta_sigma_min(m)` is simply the smallest normalized deficit observed in the configuration.

2. Constraint violation index

We assume a finite library of necessary conditions for odd perfect numbers:

```txt
L_OPN = {C_1, C_2, ..., C_K}
```

Each `C_k` is a condition that can be checked on the data for `n` in `content(m)`, such as:

* lower bounds on the number of distinct prime factors,
* specific congruence conditions on prime factors,
* required multiplicity patterns for certain primes.

We define a constraint violation observable:

```txt
V_constraints(m) = total number of condition instances
                   for which "odd perfect" structure would
                   require satisfaction, but which are violated
                   by all candidates in content(m).
```

3. Normalized constraint saturation index

We define a normalized index

```txt
Delta_struct(m) = V_constraints(m) / (1 + total_possible_instances(m))
```

where `total_possible_instances(m)` counts how many condition instances could in principle be satisfied within the searched range represented by `m`.

This quantity lies in `[0, 1)` and measures how “far” the current configuration is from jointly satisfying the known necessary conditions.

### 3.3 Combined odd perfect mismatch

We define a combined mismatch observable:

```txt
DeltaS_OPN(m) = w_sigma * Delta_sigma_min(m)
                + w_struct * Delta_struct(m)
```

where:

* `w_sigma > 0` and `w_struct > 0` are fixed weights chosen from a finite admissible set before any experiment is run,
* the weights do not depend on the data in `m`,
* `DeltaS_OPN(m) >= 0` for all `m` in the regular domain.

This ensures that the encoding is not tuned post hoc to a specific data configuration.

### 3.4 Effective tension tensor components

Consistent with the TU core, we define a semantic tension tensor component

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_OPN(m) * lambda(m) * kappa
```

where:

* `S_i(m)` is a source-like factor describing the influence of the ith structural component (for example, contribution from divisor sums or from factorization patterns).
* `C_j(m)` is a receptivity-like factor describing how sensitive the jth downstream object is to violations of odd perfect consistency.
* `DeltaS_OPN(m)` is the combined mismatch above.
* `lambda(m)` is a convergence-state factor from the TU core, chosen in a fixed bounded interval, encoding whether local reasoning around `m` is stable or unstable.
* `kappa` is a fixed coupling constant setting the scale of odd-perfect-number tension in this encoding.

We do not specify the detailed index sets for `i` and `j`. It is enough that for each regular `m` in `M`, `T_ij(m)` is well defined and finite.

### 3.5 Invariants and effective constraints

We introduce simple invariants that summarize the state of the search.

1. Search horizon invariant

```txt
I_horizon(m) = H(m)
```

interpreted as the maximum odd integer for which the configuration `m` includes divisor and factorization data.

2. Minimal deficit invariant

```txt
I_min_deficit(m) = Delta_sigma_min(m)
```

which captures how close the current explored region has come to satisfying `sigma(n) = 2 * n` for an odd `n`.

3. Structural gap invariant

```txt
I_struct_gap(m) = Delta_struct(m)
```

which measures how jointly satisfiable the known necessary conditions appear within the explored range.

In potential odd-perfect worlds, we expect that for suitable sequences of states `m_k` with increasing horizons, `I_min_deficit(m_k)` might tend to zero, and `I_struct_gap(m_k)` might display patterns compatible with the existence of extremely rare but structurally feasible candidates.

### 3.6 Singular set and domain restrictions

Some configurations might be incomplete or inconsistent, for example:

* factorization or divisor sums missing for some odd `n` in the nominal horizon,
* contradictory annotation about whether a condition `C_k` holds for a given `n`.

We define the singular set:

```txt
S_sing = { m in M : Delta_sigma_min(m) or Delta_struct(m)
                     is undefined or not finite }
```

All Q009 tension analysis is restricted to the regular domain

```txt
M_reg = M \ S_sing
```

Whenever an experiment would require evaluating `DeltaS_OPN(m)` for `m` in `S_sing`, that case is treated as “out of domain” and not as evidence about the truth of the odd perfect number problem itself.

---

## 4. Tension principle for this problem

This block states how Q009 is characterized as a tension problem within TU.

### 4.1 Core tension functional

At the effective layer we define an odd perfect tension functional:

```txt
Tension_OPN(m) = G(Delta_sigma_min(m), Delta_struct(m))
```

where `G` is a fixed nonnegative combining function, for example:

```txt
Tension_OPN(m) = alpha * Delta_sigma_min(m)
                 + beta * Delta_struct(m)
```

with `alpha > 0` and `beta > 0` chosen in advance from a finite admissible set.

The functional must satisfy:

* `Tension_OPN(m) >= 0` for all `m` in `M_reg`,
* `Tension_OPN(m)` is small when both the minimal deficit and structural gap are small,
* `Tension_OPN(m)` is large when either the minimal deficit stays large or many structural conditions are jointly violated.

### 4.2 Odd perfect numbers as a low-tension principle

At the effective layer, the “odd perfect numbers exist” scenario can be rephrased as:

> There exist sequences of regular states `m_k` in `M_reg` with increasing horizons such that the tension `Tension_OPN(m_k)` enters and remains in a narrow low band.

Intuitively, in a world where odd perfect numbers exist:

* exploration states that correctly reflect larger and larger ranges of odd integers should exhibit:

  * some candidates with very small deficit,
  * configurations where many structural conditions are nearly simultaneously satisfiable.

Under such circumstances, `Delta_sigma_min(m_k)` and `Delta_struct(m_k)` can both become small, driving `Tension_OPN(m_k)` toward a stable low value.

### 4.3 Nonexistence as persistent high tension

By contrast, the “no odd perfect numbers exist” scenario can be expressed as:

> For any admissible encoding and sequence of regular states `m_k` with horizons going to infinity, there exists a positive lower bound `delta_OPN` such that `Tension_OPN(m_k)` cannot be made arbitrarily small.

Informally, in a world where odd perfect numbers do not exist:

* minimal relative deficits for odd `n` never approach zero in a stable way,
* structural constraints cannot be jointly satisfied even as the search horizon grows,
* the combined tension functional stays bounded away from zero.

The tension principle does not prove either scenario. It only provides a structured way to talk about how discrete search data and theoretical constraints would look in the two worlds.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds at the effective layer:

* World T: odd perfect numbers exist.
* World F: no odd perfect number exists.

We describe how observables behave in each world, not how any internal TU fields are generated.

### 5.1 World T (odd perfect numbers exist, low consistency tension)

In World T:

1. Existence of candidates

   * There exist infinitely many horizons `H_k` and associated states `m_T_k` in `M_reg` such that:

     ```txt
     content(m_T_k) includes at least one odd n
     with sigma(n) = 2 * n
     ```

   * For such states, `Delta_sigma_min(m_T_k) = 0`.

2. Structural compatibility

   * For many of the horizons where candidates appear, the constraint library `L_OPN` has instances that are exactly or nearly satisfied by those candidates, producing small `Delta_struct(m_T_k)`.

3. Global tension pattern

   * For appropriate sequences of states, the tension functional satisfies:

     ```txt
     Tension_OPN(m_T_k) <= epsilon_OPN
     ```

     where `epsilon_OPN` is a small threshold determined by the encoding and expected numerical noise.

### 5.2 World F (no odd perfect numbers, persistent high consistency tension)

In World F:

1. No exact solutions

   * In every regular state `m_F` in `M_reg`, and for every odd `n` in `content(m_F)`:

     ```txt
     sigma(n) != 2 * n
     ```

   * Thus `Delta_sigma_min(m_F) > 0` for all such states.

2. Structural obstruction

   * For many horizons, the structural constraints in `L_OPN` cannot be nearly jointly satisfied by any candidate in the explored range.
   * This leads to a structural gap `Delta_struct(m_F)` that does not drift toward zero as the horizon increases.

3. Global tension pattern

   * For regular states reflecting large horizons, there exists a strictly positive `delta_OPN` such that:

     ```txt
     Tension_OPN(m_F) >= delta_OPN
     ```

   * This lower bound persists under admissible refinements of the encoding that remain faithful to the underlying arithmetic.

### 5.3 Interpretive note

The two worlds are not constructed in TU. They are only described in terms of how:

* minimal deficits,
* structural gap indices,
* and tension functionals

would behave if we had faithful large-scale configurations in each scenario.

---

## 6. Falsifiability and discriminating experiments

This block describes experiments and protocols that can:

* test the coherence of the Q009 encoding,
* distinguish between different odd-perfect tension encodings,
* provide evidence for or against particular parameter choices.

They do not prove or disprove the existence of odd perfect numbers. They only test the chosen TU encoding.

### Experiment 1: Search horizon tension profile

*Goal:*
Test whether the `Tension_OPN` functional provides a stable and interpretable summary of existing computational searches for odd perfect numbers.

*Setup:*

* Input data: published tables of odd integers checked up to a search bound `B`, together with `sigma(n)` and factorization data for each `n`.
* For each bound `B_1 < B_2 < ... < B_K`, define a state `m_Bk` in `M_reg` that encodes all checked odd `n <= B_k` and the status of conditions in `L_OPN`.

*Protocol:*

1. For each `k`:

   * compute `Delta_sigma_min(m_Bk)`,
   * compute `Delta_struct(m_Bk)`,
   * compute `Tension_OPN(m_Bk)`.

2. Plot or tabulate `Tension_OPN(m_Bk)` as a function of `B_k`.

3. Repeat for different admissible choices of weights `(alpha, beta)` chosen from a fixed finite set.

*Metrics:*

* Trend of `Delta_sigma_min(m_Bk)` with respect to `B_k`.
* Trend of `Delta_struct(m_Bk)` with respect to `B_k`.
* Trend and variability of `Tension_OPN(m_Bk)` as `B_k` grows.

*Falsification conditions:*

* If small admissible changes in `(alpha, beta)` lead to wildly different and incompatible tension trends without clear mathematical justification, the current encoding of `Tension_OPN` is considered unstable and rejected.
* If known search data suggest that minimal deficits and structural gaps behave in one qualitative way, but the encoding produces the opposite pattern for any reasonable parameter choice, then the encoding is considered misaligned and rejected.

*Semantics implementation note:*
All quantities are treated as discrete, consistent with the metadata semantics. No continuous interpolation or gradient structure is assumed in this experiment.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject specific tension encodings, but it does not prove or disprove the existence of odd perfect numbers.

---

### Experiment 2: Model-world comparison with synthetic multiplicative structures

*Goal:*
Check whether the Q009 encoding can distinguish between synthetic worlds where “odd perfect like” structures are forced to exist and worlds where they are ruled out by construction.

*Setup:*

* Construct two families of artificial multiplicative models:

  * Family T_model: integer-like objects where the divisor sum function has forced exact solutions `sigma(n) = 2 * n` for some odd-like entities.
  * Family F_model: integer-like objects where structural constraints ensure `sigma(n) != 2 * n` for all odd-like entities.

* For each model, define factorization and divisor sum summaries analogous to those used in Q009.

*Protocol:*

1. For each model in Family T_model, build a state `m_Tmodel` in `M_reg` with divisor and constraint data for its “odd” sector; compute `Delta_sigma_min`, `Delta_struct`, and `Tension_OPN`.
2. For each model in Family F_model, build a state `m_Fmodel` and compute the same observables.
3. Compare the distributions of `Tension_OPN` across the two families for admissible choices of encoding parameters.

*Metrics:*

* Mean and variance of `Tension_OPN` over Family T_model versus Family F_model.
* Separation between the two distributions, for example by any simple distance metric in the nonnegative real line.
* Robustness of the separation under small admissible changes in weights and in the finite constraint library `L_OPN`.

*Falsification conditions:*

* If the encoding systematically fails to assign lower tension to Family T_model than to Family F_model across reasonable parameter sets, it is considered ineffective and rejected.
* If the encoding assigns lower tension to clearly “no odd perfect” constructions than to “forced odd perfect” constructions, the misalignment indicates that the basic choice of observables or combination rule is flawed.

*Semantics implementation note:*
The synthetic models and their observables are treated as discrete objects, aligned with the discrete semantics of Q009.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. Success or failure on synthetic families only tests the quality of the encoding, not the reality of odd perfect numbers for actual integers.

---

## 7. AI and WFGY engineering spec

This block describes how Q009 can be used as an engineering module for AI systems within the WFGY framework, at the effective layer.

### 7.1 Training signals

Possible training signals include:

1. `signal_divisor_gap_profile`

   * Definition: a scalar derived from `Delta_sigma_min(m)` that penalizes configurations where the model implicitly treats odd integers as “too close” to being perfect without explicit justification.
   * Purpose: encourage the AI to track how large divisor sum deficits actually are, rather than assuming that exact equalities are likely.

2. `signal_structural_consistency_OPN`

   * Definition: a signal proportional to `Delta_struct(m)` whenever the model reasons about hypothetical odd perfect numbers.
   * Purpose: encourage internal states that respect known structural constraints from `L_OPN`.

3. `signal_world_split_OPN`

   * Definition: a stability signal that measures how consistently the model can maintain separate reasoning chains under “World T” and “World F” assumptions without mixing them.
   * Purpose: improve robustness when the AI is asked to explore both existence and nonexistence scenarios as deliberate counterfactuals.

### 7.2 Architectural patterns

Module patterns that can reuse Q009 components:

1. `DivisorTensionHead`

   * Role: given an internal representation of a number-theoretic context, estimate a proxy for `Tension_OPN(m)`.
   * Interface:

     * Input: internal embeddings for statements about `sigma(n)`, prime factors, and related constraints.
     * Output: a scalar tension estimate and optional components for `Delta_sigma_min` and `Delta_struct`.

2. `ConstraintSaturationChecker_OPN`

   * Role: check whether the model’s current candidate arguments about odd perfect numbers respect the constraint library `L_OPN`.
   * Interface:

     * Input: structured representation of a candidate odd integer or a sketch proof.
     * Output: a small vector of scores indicating how many constraints are violated or nearly violated.

3. `TU_DiscreteField_Observer`

   * Role: a general observer that extracts a simplified discrete configuration suitable for applying Q009’s tension functional.
   * Interface:

     * Input: latent states relevant to divisor sums and factorization.
     * Output: a compact discrete summary that can be treated as a state `m` in `M_reg`.

### 7.3 Evaluation harness

An evaluation harness for AI systems augmented with Q009 modules:

1. Task selection

   * Choose a set of problems and expository tasks about perfect numbers and related multiplicative topics, including:

     * explaining known results about even perfect numbers,
     * summarizing constraints on hypothetical odd perfect numbers,
     * distinguishing between “known necessary conditions” and “speculative heuristics”.

2. Conditions

   * Baseline condition: model operates without Q009-specific modules.
   * TU condition: model uses `DivisorTensionHead` and `ConstraintSaturationChecker_OPN` as auxiliary guidance.

3. Metrics

   * Factual accuracy on known theorems and constraints.
   * Internal consistency: how often the model contradicts itself about known necessary conditions.
   * Clarity in separating what is proved, what is conjectured, and what is purely hypothetical.

### 7.4 60 second reproduction protocol

A minimal protocol to let external users experience the impact of Q009 encoding.

* Baseline setup

  * Prompt: ask the AI to explain what perfect numbers are and whether any odd perfect numbers are known, without mentioning WFGY or tension.
  * Observation: record whether the explanation clearly separates the existence of even perfect numbers from the open status of odd perfect numbers, and whether it misstates any constraints.

* TU encoded setup

  * Prompt: ask the same question, but instruct the AI to:

    * treat the problem as a consistency_tension problem in a discrete state space,
    * explicitly mention “deficit between `sigma(n)` and `2 * n` for odd `n`”
    * and discuss structural constraints from a finite library of necessary conditions.

  * Observation: record whether the answer is more precise about:

    * what is known,
    * what is conjectured,
    * how the various constraints fit together.

* Comparison metric

  * Use a simple rubric for:

    * correctness of statements,
    * clarity in describing open status,
    * explicit handling of constraints and search data.

* What to log

  * Both prompts and responses,
  * any auxiliary tension estimates computed by Q009 components,
  * any explicit references to structural constraints or deficits.

---

## 8. Cross problem transfer template

This block describes reusable components produced by Q009 and their direct reuse targets.

### 8.1 Reusable components produced by this problem

1. ComponentName: `OddPerfectTensionFunctional`

   * Type: functional

   * Minimal interface:

     ```txt
     Inputs: divisor_sum_summaries, factorization_summaries
     Output: tension_value (nonnegative scalar)
     ```

   * Preconditions:

     * Inputs must encode consistent divisor sum and factorization data for a finite set of odd integers.

2. ComponentName: `DivisorProfileDescriptor`

   * Type: observable

   * Minimal interface:

     ```txt
     Inputs: integer_configuration
     Output: profile_vector summarizing divisor sums and deficits
     ```

   * Preconditions:

     * The configuration provides enough information to compute `sigma(n)` and deficits for the odd integers under consideration.

3. ComponentName: `ConstraintSaturationWorld_OPN`

   * Type: experiment_pattern

   * Minimal interface:

     ```txt
     Inputs: constraint_library, search_horizon
     Output: experiment_definition describing how to
             evaluate Delta_sigma_min, Delta_struct,
             and Tension_OPN across horizons
     ```

   * Preconditions:

     * The constraint library is finite and can be applied consistently to all integers in the search range.

### 8.2 Direct reuse targets

1. Q020 (structure of multiplicative functions)

   * Reused component: `DivisorProfileDescriptor`.
   * Why it transfers: many questions about multiplicative functions involve patterns of divisor sums or related quantities; the descriptor captures these patterns in a reusable way.
   * What changes: the observable is applied to broader classes of multiplicative functions, not just `sigma(n)`.

2. Q021 (extreme values of divisor sums)

   * Reused component: `OddPerfectTensionFunctional`.
   * Why it transfers: extreme behavior of `sigma(n)` relative to `n` can be modeled as a tension between observed growth and theoretical bounds.
   * What changes: the target equality `sigma(n) = 2 * n` is replaced by inequalities or different normalization factors, but the same structure is used.

3. Q023 (sparsity of special integer sets)

   * Reused component: `ConstraintSaturationWorld_OPN`.
   * Why it transfers: many special sets (for example, certain smooth numbers or special factorization classes) can be modeled using finite constraint libraries and tension between “search data” and “structural possibility”.
   * What changes: the constraint library and notion of “special” are adapted to the target set, but the horizon based experiment pattern remains.

---

## 9. TU roadmap and verification levels

This block describes the current verification level of Q009 and possible next steps.

### 9.1 Current levels

* E_level: E1

  * A coherent effective-layer encoding for odd perfect numbers as a consistency_tension problem in a discrete state space has been specified.
  * Invariants, mismatch observables, and a tension functional have been defined.

* N_level: N1

  * The narrative clearly distinguishes between:

    * existence versus nonexistence scenarios,
    * search data versus structural constraints,
    * what the tension functional is meant to summarize.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following should be implemented in practice:

1. Build a concrete prototype that, given published search data up to a horizon `B`, constructs states `m_B` and computes `Delta_sigma_min`, `Delta_struct`, and `Tension_OPN(m_B)`, publishing the tension profiles as open data.
2. Implement synthetic model families as in Experiment 2 and provide reproducible results showing how well Q009’s encoding distinguishes the “forced existence” and “forced nonexistence” model worlds.

Both steps operate only on observable summaries (factorization and divisor sums) and do not require revealing any deep TU generative rule.

### 9.3 Long-term role in the TU program

In the long term, Q009 is expected to serve as:

* the canonical discrete consistency_tension problem in multiplicative number theory,
* a standard module for reasoning about whether highly constrained structures should exist at all,
* a bridge between number-theoretic search experiments and formalized tension-based narratives in AI systems.

---

## 10. Elementary but precise explanation

This block gives a nontechnical explanation aligned with the effective-layer description.

Classically, perfect numbers are integers `n` such that the sum of all their positive divisors equals `2 * n`. Examples are `6` and `28`. All known perfect numbers are even and follow a very specific pattern tied to Mersenne primes.

The odd perfect number problem asks a simple question:

> Could there be a perfect number that is odd?

Nobody has ever found one, and nobody has proved they cannot exist. This makes the question both easy to state and very hard to answer.

In the Tension Universe view, we do not try to prove or disprove the existence directly. Instead, we:

* look at all odd numbers that have been checked up to some limit,
* record how far each one is from being perfect, using the difference between `sigma(n)` and `2 * n`,
* record which of many known structural conditions would have to hold if an odd perfect number existed.

We combine these two pieces of information into a single “tension score”:

* low tension means “the data and constraints fit well with the idea that an odd perfect number could exist”,
* high tension means “the data and constraints seem to resist the existence of such a number”.

We then imagine two worlds:

* In a world where odd perfect numbers exist, as we explore more and more odd numbers, we would expect to see some that get extremely close to perfect, and structural conditions that can be almost jointly satisfied, leading to low tension.
* In a world where no odd perfect number exists, we would expect that no matter how far we search, the gap to perfection stays noticeably large, and the structural constraints cannot be made compatible, leading to persistent high tension.

This framework does not answer the question by itself. Instead, it gives us:

* a clear way to summarize search and structural information,
* a way to test different encodings of that information in AI systems,
* reusable tools for other problems where “many constraints” and “no known examples” are the main features.

Q009 is therefore the prototype for discrete consistency_tension problems in Tension Universe, centered on one of the most famous open questions in multiplicative number theory.
