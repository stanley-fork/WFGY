# Q097 · Triggering of large volcanic eruptions

## 0. Header metadata

```txt
ID: Q097
Code: BH_EARTH_VOLCANISM_L3_097
Domain: Earth
Family: Volcanism and solid Earth dynamics
Rank: S
Projection_dominance: I
Field_type: dynamical_field
Tension_type: risk_tail_tension
Status: Partial
Semantics: continuous
E_level: E1
N_level: N1
Last_updated: 2026-01-25
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical problem behind Q097 can be stated as:

> Given the physical state of a volcanic and surrounding crustal system, what combination of stresses, melts, volatiles, and pathways triggers a large volcanic eruption, and on what time scales, in a way that allows at least partial forecasting of such events?

Here:

* "large volcanic eruption" means events in the upper tail of explosivity and impact, for example Volcanic Explosivity Index (VEI) 6 and above, including so-called "super-eruptions".
* "triggering" refers to the transition from a metastable magmatic–crustal configuration to rapid failure and magma discharge, not only to the existence of long-lived magma reservoirs.

The problem is to identify:

1. which combinations of observable state variables are necessary or sufficient for large eruptions,
2. how close the system can approach such conditions without erupting,
3. whether useful, nontrivial forecasting signals can be defined in terms of these state variables.

### 1.2 Status and difficulty

Key facts about the current scientific status include:

* Many large eruptions are associated with long-lived magma reservoirs, evolving over tens of thousands to hundreds of thousands of years, with episodic recharge and cooling.
* Physical models exist for:

  * overpressure and mechanical failure of crustal rocks,
  * magma ascent through conduits and dikes,
  * fragmentation and explosive behavior.
* However, there is no consensus predictive theory that reliably links observed precursors (for example seismic swarms, ground deformation, gas emissions) to the timing and magnitude of very large eruptions.
* Statistical studies show that large eruptions are rare tail events in time and magnitude, and that their inter-event times are highly variable.
* Reviews on super-eruptions emphasize that:

  * reservoirs can remain in near-eruptible states for extended periods,
  * not all such states result in an eruption,
  * the detailed trigger mechanisms are still poorly constrained.

As a result, the triggering of large eruptions remains a partially understood, high-impact open problem in Earth sciences. It is not "open" in the sense of having no models at all, but "partial" in the sense that there is no widely accepted, quantitative, forecasting-capable theory.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q097 plays several roles:

1. It is a canonical example of **risk_tail_tension** in a physical dynamical system, where:

   * the observable state space is high-dimensional and noisy,
   * catastrophic events occupy a small region of that space,
   * forecasting is essentially forecasting entry into a rare tail region.

2. It provides a concrete physical testbed for:

   * defining tail-risk indices over configuration space,
   * defining metastability margins for complex systems,
   * probing how much information is needed to meaningfully forecast extreme events.

3. It acts as a bridge between:

   * solid Earth physics,
   * global risk assessment,
   * AI forecasting and alignment for low-frequency, high-impact hazards.

### References

1. Smithsonian Institution, Global Volcanism Program, "Volcanoes of the World" database and documentation on large explosive eruptions and the Volcanic Explosivity Index (VEI).
2. R. S. J. Sparks, "The dynamics of bubble growth and nucleation in magmas: internal processes and explosive volcanism", and related works on conduit flow, overpressure, and explosive eruption physics.
3. C. G. Newhall and S. Self, "The Volcanic Explosivity Index (VEI): An estimate of explosive magnitude for historical volcanism", Journal of Geophysical Research, 1982.
4. Review literature on "super-eruptions" and unresolved questions in the triggering of very large volcanic eruptions in solid Earth geoscience.

---

## 2. Position in the BlackHole graph

This block records the graph position of Q097 with explicit edges and one-line reasons. All edges refer only to Q IDs and text names.

### 2.1 Upstream problems

These nodes provide conceptual or methodological prerequisites for Q097.

* Q091
  Reason: Supplies background climate sensitivity notions that condition the global impact and feedbacks of large eruptions.

* Q092
  Reason: Provides a general framework for tipping and threshold behavior in Earth subsystems that can be reused for crustal–magmatic transitions.

* Q096
  Reason: Shares tools and ideas for predictability and triggering in highly nonlinear solid Earth systems (stress accumulation, failure, and rare events).

* Q094
  Reason: Offers multi-scale fluid dynamical patterns that are analogs for volatile transport and crustal fluid migration relevant to magmatic systems.

### 2.2 Downstream problems

These nodes can directly reuse components defined in Q097.

* Q100
  Reason: Uses large eruptions as environmental shocks that modulate conditions for disease emergence and spread in global risk models.

* Q095
  Reason: Treats large eruptions as discrete, high-impact shocks to ecosystems in biodiversity loss and recovery dynamics.

* Q099
  Reason: Includes large eruptions as drivers of regional hydrological shifts and long-term freshwater stress via radiative forcing and ash deposition.

### 2.3 Parallel problems

Parallel nodes share similar tension types without direct component reuse.

* Q096
  Reason: Both Q096 and Q097 aim to characterize and forecast rare, high-impact events in solid Earth driven by complex stress fields and thresholds.

* Q105
  Reason: Q105 deals with systemic crashes in complex networks, another case of risk_tail_tension in a high-dimensional configuration space.

* Q092
  Reason: Q092 studies rapid transitions between states of Earth subsystems, making it parallel in both threshold structure and rare-event focus.

### 2.4 Cross-domain edges

Cross-domain edges show where Q097 components can transfer.

* Q059
  Reason: Reuses tail-risk tension formalizations to quantify how much information is needed to forecast rare catastrophic events in information processing systems.

* Q098
  Reason: Incorporates large eruptions as external shocks within an Anthropocene-scale dynamical system of human–Earth interactions.

* Q121
  Reason: Uses Q097 as a concrete physical scenario for aligning AI forecasts and decisions under low-frequency, high-impact risk.

* Q125
  Reason: Models multi-agent coordination and response to super-eruption scenarios as a case of global decision-making under tail-risk tension.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is restricted to the effective layer. We describe only:

* state spaces,
* observables and fields,
* invariants and tail-risk indices,
* singular sets and domain restrictions.

We do not describe any hidden TU generative rules or explicit mappings from raw data to internal TU fields.

### 3.1 State space

We introduce an effective state space

```txt
M_volc
```

with the following interpretation:

* Each state `m` in `M_volc` represents a coarse-grained configuration of:

  * a volcanic system, including one or more magma reservoirs,
  * the surrounding crust and lithosphere in a relevant region,
  * the immediate hydrosphere and atmosphere where they directly interact with the volcano.

For each `m` we assume access to a finite-dimensional summary of key variables, such as:

* stress and strain indicators in specified crustal regions,
* overpressure and melt fraction indicators in magma reservoirs,
* volatile content indicators in reservoirs,
* permeability or flow capacity measures along potential pathways to the surface,
* external forcing indicators (for example tectonic loading, ice unloading, rapid erosion).

We do not specify how such summaries are computed from observational, geological, or simulation data. We only assume that:

* each state `m` encodes a set of scalar or low-dimensional vector observables that can be consistently interpreted across states.

### 3.2 Admissible encoding class

We define a class `E_volc` of admissible encodings, with the following properties:

1. Each encoding `e` in `E_volc` maps physical configurations of the volcanic region to states in `M_volc` using:

   * a fixed set of regions and reservoir definitions,
   * a fixed set of summary statistics,
   * a fixed time window for temporal averaging or aggregation.

2. Encodings in `E_volc` must satisfy:

   * Finite dimensionality:
     Each `m` is represented by a finite list of real-valued or bounded discrete-valued observables.

   * Monotonicity of hazard indicators:
     If a physical change obviously increases stress, melt fraction, or volatile content in a region, then the corresponding observables must not decrease.

   * Temporal coherence:
     For a slowly varying physical system, small changes in physical state over a short time window must not produce arbitrarily large jumps in the summary observables.

3. For a given analysis or experiment, a specific encoding `e` is chosen from `E_volc` and must be fixed before any evaluation of tail-risk indices on new data. It may not be tuned post hoc based on eruption outcomes.

### 3.3 Observables and fields

For a fixed admissible encoding `e` in `E_volc`, we define the following observables on `M_volc`.

1. Effective stress or overpressure indicator

```txt
sigma_eff(m; R_c)
```

* Input: state `m`, crustal region label `R_c`.
* Output: nonnegative scalar summarizing effective stress or overpressure in `R_c`.

2. Effective melt fraction indicator

```txt
phi_melt(m; R_r)
```

* Input: state `m`, reservoir region label `R_r`.
* Output: scalar in `[0, 1]` summarizing melt fraction.

3. Volatile content indicator

```txt
C_vol(m; R_r)
```

* Input: state `m`, reservoir region label `R_r`.
* Output: nonnegative scalar summarizing dissolved and exsolved volatile content.

4. Permeability or flow capacity

```txt
K_flow(m; P)
```

* Input: state `m`, path label `P` from reservoir to surface.
* Output: nonnegative scalar summarizing the ability of magma or gas to flow along `P`.

5. External forcing indicator

```txt
F_ext(m)
```

* Input: state `m`.
* Output: scalar or short vector describing relevant external forcings (for example tectonic loading rate, surface unloading).

These observables are defined in terms of the encoded state; the specifics of physical measurement, inversion, or simulation are abstracted away.

### 3.4 Tail-risk mismatch observables

We introduce two mismatch measures that compare the current configuration to reference ensembles.

1. Tail-risk index relative to non-eruptive ensemble

Let `L_ne` be a fixed finite library of states in `M_volc_reg` (to be defined below) that are known to have occurred during extended non-eruptive intervals at a given volcano or comparable systems.

For each `m` in `M_volc_reg` we define:

```txt
TailRiskIndex(m) = G_non_eruptive(m, L_ne)
```

where `G_non_eruptive` is a nonnegative function of:

* the distances between the observables of `m` and those of states in `L_ne`,
* the distribution of such distances over the library.

Properties:

* `TailRiskIndex(m) >= 0` for all `m` in `M_volc_reg`.
* If `m` is very similar to many states in `L_ne`, then `TailRiskIndex(m)` tends to be small.
* The exact form of `G_non_eruptive` must be fixed before analysis and must not depend on whether `m` later leads to an eruption.

2. Metastability margin

Let `S_meta` be a subset of `M_volc_reg` representing configurations that are empirically judged to be metastable, with no large eruptions in a specified time horizon.

We define:

```txt
MetastabilityMargin(m) = H_meta(m, S_meta)
```

where `H_meta` is a nonnegative function measuring how far `m` is, in observable space, from the center of mass or a typical point of `S_meta`.

Properties:

* `MetastabilityMargin(m) >= 0` for all `m` in `M_volc_reg`.
* If `m` lies deep inside the region of configurations similar to `S_meta`, then `MetastabilityMargin(m)` is small.
* If `m` lies far outside typical `S_meta` configurations, `MetastabilityMargin(m)` becomes large.

The definitions of `L_ne`, `S_meta`, `G_non_eruptive`, and `H_meta` must be part of the encoding choice and fixed before any test on new events.

### 3.5 Singular set and domain restriction

We define a singular set:

```txt
S_sing_volc = { m in M_volc :
                at least one of sigma_eff, phi_melt, C_vol, K_flow, F_ext
                is undefined, non-finite, or clearly inconsistent }
```

Examples of inconsistency include:

* negative melt fraction,
* negative variance in any observable,
* missing data in required observables for the given encoding `e`.

We restrict all tail-risk tension analysis to:

```txt
M_volc_reg = M_volc \ S_sing_volc
```

Whenever an experiment or protocol would attempt to evaluate `TailRiskIndex(m)` or `MetastabilityMargin(m)` for a state in `S_sing_volc`, the result is treated as "out of domain" rather than as evidence about triggering physics.

---

## 4. Tension principle for this problem

This block states how Q097 is represented as a tension problem.

### 4.1 Core tail-risk tension functional

For a fixed admissible encoding `e` in `E_volc`, and fixed choices of `L_ne`, `S_meta`, `G_non_eruptive`, and `H_meta`, we define an effective tail-risk tension functional:

```txt
Tension_VOLC(m) = alpha * TailRiskIndex(m)
                  + beta  * MetastabilityMargin(m)
```

with:

```txt
alpha > 0
beta  > 0
alpha + beta = 1
```

The parameters `alpha` and `beta` are chosen from a fixed compact interval of positive values satisfying `alpha + beta = 1`. They must be fixed as part of the encoding and cannot be adapted after seeing eruption outcomes for the states being evaluated.

Properties:

* `Tension_VOLC(m) >= 0` for all `m` in `M_volc_reg`.
* If `m` is similar to many known non-eruptive states and lies deep inside the metastable region, then `Tension_VOLC(m)` is small.
* If `m` lies far from non-eruptive states and far from the metastable region, then `Tension_VOLC(m)` becomes large.

### 4.2 Triggering as low vs high tail-risk tension

At the effective layer, triggering of large eruptions is framed as:

* a question of whether real volcanic systems pass through regions of state space where `Tension_VOLC(m)` becomes large,
* and whether such transitions can be detected and meaningfully forecast using the observables encoded in `M_volc`.

Informally:

* Non-eruptive intervals should correspond to trajectories where `Tension_VOLC(m(t))` mostly stays within a low-to-moderate band.
* Approaching a large eruption should correspond to a systematic rise in `Tension_VOLC(m(t))` towards a high-tension region, subject to measurement and modeling uncertainties.

### 4.3 Failure of predictability as misaligned or diffuse tension

If, after selecting an admissible encoding and libraries, we find that:

* `Tension_VOLC(m(t))` does not distinguish eruptive from non-eruptive intervals,
* or any such distinction is extremely sensitive to small admissible changes in encoding parameters,

then the tail-risk tension encoding for Q097 is considered misaligned with the physical triggering process. This does not prove that triggering is inherently unpredictable, but it shows that the chosen encoding fails to capture meaningful tail-risk structure.

---

## 5. Counterfactual tension worlds

We now define two counterfactual worlds at the effective layer:

* World T: triggering is partially predictable via tail-risk tension.
* World F: triggering is effectively opaque in the chosen configuration space.

These worlds describe patterns in observables and tension, not hidden generative rules.

### 5.1 World T (partially predictable triggering)

In World T, we assume:

1. Hindcast structure

   * For well-instrumented large eruptions and coherent reconstructions of state trajectories `m(t)`, there exist encodings in `E_volc` such that:

     * in pre-eruption windows, `Tension_VOLC(m(t))` tends to rise above typical baseline values,
     * in matched non-eruptive intervals, `Tension_VOLC(m(t))` remains in a lower band.

2. Stability across systems

   * When applying the same encoding to different volcanoes with similar physical regimes, the qualitative behavior of `Tension_VOLC` is similar:

     * rising towards eruption,
     * remaining moderate when no large eruption is imminent.

3. Model-world consistency

   * In synthetic crustal–magmatic models with known eruption and non-eruption trajectories, `Tension_VOLC` computed from encoded states:

     * consistently separates eruptive trajectories from non-eruptive ones,
     * shows limited sensitivity to small admissible changes in encoding.

4. Limited but nontrivial forecastability

   * Forecasting attempts based on `Tension_VOLC` outperform naive baselines that ignore configuration-space structure, given realistic observational noise.

### 5.2 World F (effectively opaque triggering)

In World F, we assume:

1. Hindcast failure

   * For the same set of case studies, no admissible encoding in `E_volc` yields a stable pattern where `Tension_VOLC(m(t))` rises before large eruptions without also frequently producing high tension in non-eruptive intervals.

2. Encoding instability

   * Small admissible changes in encoding parameters or libraries cause large changes in which trajectories are labeled as high-tension:

     * eruptive and non-eruptive trajectories cannot be robustly separated by any fixed encoding.

3. Model-world confusion

   * In synthetic systems, attempts to define `Tension_VOLC` lead to poor separation even when full state information is available:

     * any apparent separation disappears under mild changes in encoding.

4. Forecasting collapse

   * Forecasts based on `Tension_VOLC` perform no better than naive baselines, or worse, and these failures cannot be corrected by any admissible parameter choice without violating the pre-committed encoding rules.

### 5.3 Interpretive note

These counterfactual worlds are not claims about the true Earth. They specify:

* what patterns in tension observables we would see if the world were closer to "partially predictable" or "effectively opaque" in the sense above,
* how Q097 serves as a testing ground for tail-risk encodings, rather than as a claim to have solved eruption prediction.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can:

* test the coherence of the Q097 encoding,
* discriminate between better and worse tail-risk encodings,
* provide evidence for or against particular parameter choices.

These experiments do not claim to solve the triggering problem. They can only accept or reject specific encodings.

### Experiment 1: Hindcast tension profiles for well-instrumented eruptions

*Goal:*
Test whether a fixed `Tension_VOLC` encoding can distinguish pre-eruption periods from matched non-eruptive intervals for well-studied large eruptions.

*Setup:*

* Select a set of large eruptions with relatively good observational records, for example:

  * Mt. St. Helens 1980,
  * Pinatubo 1991,
  * other late 20th and early 21st century large eruptions.
* For each case, define:

  * a pre-eruption window of length `T_pre` (for example months to a few years),
  * one or more control windows of the same length in earlier non-eruptive periods.
* Choose a specific encoding `e` in `E_volc`, a library `L_ne`, a metastable set `S_meta`, and parameters `alpha`, `beta`.
* Commit to these choices before computing any tension for the test windows.

*Protocol:*

1. For each eruption and each window, reconstruct an approximate trajectory `m(t)` in `M_volc_reg` at a fixed sampling interval (for example weekly or monthly).
2. Compute `Tension_VOLC(m(t))` along each trajectory.
3. For each case, compute:

   * the distribution of `Tension_VOLC` values in pre-eruption windows,
   * the distribution of `Tension_VOLC` values in control windows.
4. Compare these distributions across all cases.

*Metrics:*

* For each case, a statistic such as:

  * `Delta_mean = mean_pre - mean_control`,
  * `Delta_quantile = q_pre - q_control` for upper quantiles.
* Aggregated performance over all cases:

  * fraction of cases where pre-eruption windows show significantly higher tension than controls.

*Falsification conditions:*

* Define a minimal acceptable pattern, for example:

  * at least a fixed fraction `p_min` of eruption cases must show `Delta_mean` above a positive threshold,
  * and the same pattern must not be present in randomly chosen non-eruptive window pairs.
* If, after applying the encoding to the full set of cases:

  * the observed fraction of cases with significantly higher pre-eruption tension is less than `p_min`,
  * or the pattern appears equally often in purely non-eruptive window pairs,
    then this specific encoding of `Tension_VOLC` is rejected for Q097.

*Field implementation note:*
All observables and tension values are treated as continuous fields aggregated over finite volumes and time windows consistent with the metadata regime.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

### Experiment 2: Synthetic crustal–magmatic model discrimination

*Goal:*
Evaluate whether the Q097 encoding can systematically separate eruptive and non-eruptive trajectories in a controlled synthetic model where ground truth is known.

*Setup:*

* Select or construct a family of dynamical models of crustal–magmatic systems where:

  * the full internal state is available at each time step,
  * eruption events are clearly defined by model criteria.
* For each model, generate:

  * multiple trajectories that lead to large eruptions,
  * multiple trajectories that remain non-eruptive over comparable time spans.
* Choose an encoding `e` in `E_volc`, libraries `L_ne` and `S_meta`, and parameters `alpha`, `beta` before labelling trajectories as eruptive or non-eruptive.

*Protocol:*

1. For each trajectory, map the model state at each time step to `M_volc_reg` using `e`.
2. Compute `Tension_VOLC(m(t))` along each trajectory.
3. For each trajectory, derive:

   * summary statistics of tension (for example mean, maximum, time spent above a threshold).
4. Use simple classification rules (for example a single threshold on a summary statistic) to predict:

   * whether a trajectory is eruptive or non-eruptive.

*Metrics:*

* Classification performance measures, for example:

  * true positive rate (eruptive trajectories correctly flagged),
  * false positive rate (non-eruptive trajectories incorrectly flagged),
  * area under a receiver operating characteristic curve for threshold-based classifiers.

*Falsification conditions:*

* Define minimal performance criteria, such as:

  * a required lower bound on true positive rate and an upper bound on false positive rate at some threshold.
* If no admissible encoding in `E_volc` can achieve performance above these criteria across a range of models:

  * under mild changes in encoding parameters that remain within the pre-committed rules,
    then the Q097 tail-risk encoding is considered ineffective for model-world discrimination and must be revised.

*Field implementation note:*
Model states are aggregated into the same type of finite-dimensional summaries used for real systems, preserving the distinction between continuous fields and their coarse-grained representations.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

## 7. AI and WFGY engineering spec

This block describes how Q097 can be used as an engineering module for AI systems within the WFGY framework.

### 7.1 Training signals

We define training signals that AI models can use as auxiliary objectives.

1. `signal_volc_tail_risk`

   * Definition: a scalar signal equal or proportional to `Tension_VOLC(m)` for states associated with volcanic contexts in the model’s internal representation.
   * Purpose: encourage the model to form internal representations where high tail-risk conditions are distinguishable from typical non-eruptive conditions.

2. `signal_stability_baseline`

   * Definition: a penalty applied when model-inferred states corresponding to long non-eruptive intervals are assigned high `Tension_VOLC`.
   * Purpose: enforce that quiet periods are mapped to low or moderate tail-risk tension.

3. `signal_counterfactual_clarity`

   * Definition: a measure of how clearly the model separates narratives framed as "World T" and "World F" when asked to reason under explicit assumptions.
   * Purpose: avoid mixing incompatible assumptions about predictability within a single reasoning chain.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q097 structures without exposing deep TU rules.

1. `VolcanicRiskHead`

   * Role: an auxiliary head attached to the model that produces an estimate of `Tension_VOLC(m)` whenever the context refers to volcanic systems.
   * Interface:

     * Inputs: internal embeddings of text or data describing current volcanic conditions.
     * Outputs: a scalar estimated tail-risk tension and possibly a small vector decomposing contributions (for example stress, melt, volatiles).

2. `GeoRiskConsistencyFilter`

   * Role: a filter module that evaluates model outputs about eruption risk against encoded tail-risk structure.
   * Interface:

     * Inputs: candidate statements about volcanic risk and internal state summaries.
     * Outputs: a consistency score or mask indicating whether the statements align with plausible `Tension_VOLC` patterns.

3. `ExtremeEventScenarioSampler`

   * Role: a module that proposes scenario variations by exploring directions in state space that change `Tension_VOLC` while staying within admissible physical bounds.
   * Interface:

     * Inputs: a baseline configuration summary.
     * Outputs: perturbed configurations representing higher or lower tail-risk tension cases.

### 7.3 Evaluation harness

We propose an evaluation harness with baseline and TU-augmented conditions.

1. Task categories

   * Explanation tasks:

     * explain known large eruptions and their precursors,
     * summarize current scientific uncertainty about triggering.
   * Scenario tasks:

     * answer "what if" questions about changes in monitoring signals,
     * qualitatively assess risk under hypothetical configurations.

2. Conditions

   * Baseline condition:

     * the model operates without explicit Q097-related modules.
   * TU condition:

     * the model uses `VolcanicRiskHead` and `GeoRiskConsistencyFilter` as auxiliary tools.

3. Metrics

   * Factual correctness:

     * consistency with current volcanology and geophysics.
   * Internal coherence:

     * absence of contradictions across closely related questions.
   * Tail-risk sensitivity:

     * ability to distinguish low-risk from high-risk scenarios in a manner consistent with encoded `Tension_VOLC` structure.

### 7.4 60-second reproduction protocol

A minimal protocol for external users to perceive the impact of Q097 encoding.

* Baseline setup:

  * Prompt: ask the AI to explain what triggers large volcanic eruptions and the limits of current forecasting.
  * Observation: examine whether the explanation mixes short-term and long-term processes and whether it clearly distinguishes known precursors from speculative triggers.

* TU encoded setup:

  * Prompt: ask the same question but include an instruction to organize the answer using:

    * configuration space,
    * tail-risk tension,
    * approaches to defining indices like `TailRiskIndex` and `MetastabilityMargin`.
  * Observation: examine whether the explanation:

    * clearly separates background conditions from trigger-like changes,
    * highlights the difficulty of obtaining reliable signals in the tail region.

* Comparison metric:

  * Rate both answers on:

    * structure,
    * explicitness of risk-tail concepts,
    * clarity about uncertainty.
  * Optionally, have multiple evaluators compare the two explanations.

* What to log:

  * full prompts and responses in both setups,
  * any auxiliary tension values produced by `VolcanicRiskHead`,
  * basic metadata about which Q097 components were invoked.

---

## 8. Cross problem transfer template

This block describes reusable components from Q097 and their transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `TailRiskIndex_VOLC`

   * Type: functional
   * Minimal interface:

     * Inputs: state `m` in `M_volc_reg`.
     * Output: scalar `r_tail` representing proximity to known non-eruptive configurations.
   * Preconditions:

     * A library `L_ne` and distance-like function have been fixed as part of the encoding.

2. ComponentName: `MetastabilityMargin_VOLC`

   * Type: functional
   * Minimal interface:

     * Inputs: state `m` in `M_volc_reg`.
     * Output: scalar `d_meta` representing distance to a metastable region.
   * Preconditions:

     * A metastable set `S_meta` and function `H_meta` have been fixed.

3. ComponentName: `GeoExtremeWorld_Template`

   * Type: experiment_pattern
   * Minimal interface:

     * Inputs: a geophysical system with rare, high-impact events and an encoding class analogous to `E_volc`.
     * Output: a pair of experiment designs:

       * World T: partially predictable extremes,
       * World F: effectively opaque extremes,
         each with specified tail-risk observables and falsification criteria.
   * Preconditions:

     * The system has a notion of configuration space and extreme events.

### 8.2 Direct reuse targets

1. Q096 (Earthquake predictability and triggering)

   * Reused components:

     * `GeoExtremeWorld_Template`,
     * conceptual structure of `TailRiskIndex` and `MetastabilityMargin`.
   * Why it transfers:

     * seismic systems also exhibit rare, high-impact events driven by stress accumulation and failure.
   * What changes:

     * state space and observables become fault stress, slip deficits, and fluid pressures instead of magmatic variables.

2. Q105 (Systemic crashes in complex networks)

   * Reused components:

     * `GeoExtremeWorld_Template`,
     * tail-risk functional pattern.
   * Why it transfers:

     * systemic crashes can be viewed as transitions from metastable configurations into failure regimes.
   * What changes:

     * state space becomes network load, connectivity, and flow variables; libraries of non-crash configurations and metastable regions are defined in network terms.

3. Q100 (Pandemic risk under environmental shocks)

   * Reused components:

     * tail-risk framing of rare environmental triggers,
     * methods for connecting environmental extremes to downstream risk models.
   * Why it transfers:

     * large eruptions are part of the exogenous shock space that can affect disease emergence and spread.
   * What changes:

     * tail-risk indices are defined on epidemiological and environmental variables, with volcanic variables appearing as exogenous drivers.

---

## 9. TU roadmap and verification levels

This block explains the role of Q097 in the TU program and the next measurable steps.

### 9.1 Current levels

* E_level: E1

  * A coherent effective encoding for large-eruption triggering has been specified.
  * At least two experiment types have been defined with explicit falsification conditions.

* N_level: N1

  * A stable narrative of "large eruptions as tail-risk tension in configuration space" has been articulated.
  * Counterfactual worlds (World T and World F) have been framed in observable and tension terms.

### 9.2 Next measurable step toward E2

To progress from E1 to E2, Q097 should achieve at least one of the following:

1. Implementation of a prototype analysis where:

   * case studies of real eruptions and non-eruptive intervals are encoded into `M_volc_reg`,
   * `Tension_VOLC` is computed,
   * tension profiles and hindcast statistics are published as open data.

2. Construction of synthetic model families where:

   * eruptive and non-eruptive trajectories are generated,
   * tail-risk encodings are applied,
   * classification performance is systematically benchmarked.

In both cases, the implementation must:

* use an encoding `e` in `E_volc`,
* fix libraries and parameters before analyzing test data,
* publish enough detail for independent reproduction.

### 9.3 Long-term role in the TU program

In the longer term, Q097 is expected to:

* serve as a reference node for physical tail-risk problems in Earth systems,
* inform how to encode rare extreme events in other domains (for example finance, infrastructure, pandemics),
* provide a grounded example for AI alignment work on forecasting and decision-making under low-frequency, high-impact hazards.

Q097 does not seek to replace domain-specific volcanology. Instead, it proposes a way to:

* frame triggering of large eruptions as a structured tension problem,
* clarify where forecasting attempts are limited by information, encoding choices, or intrinsic unpredictability.

---

## 10. Elementary but precise explanation

This block gives an accessible explanation aligned with the effective-layer encoding.

Large volcanic eruptions are among the most dramatic events on Earth. They can affect climate, ecosystems, and human societies. Scientists know a lot about how magma forms, how gases drive explosions, and how ash spreads, but they still cannot reliably say when a very large eruption will happen.

In this problem, we describe the situation in terms of a state space:

* each state describes the condition of a volcano and the surrounding crust, including:

  * how stressed the rocks are,
  * how much molten rock is present,
  * how much gas is dissolved or free,
  * how easy it is for magma or gas to move toward the surface.

We then define numbers that measure:

* how similar the current state is to past quiet periods (non-eruptive library),
* how far it is from states that seem safely metastable.

From these we build a tail-risk tension:

* low tail-risk tension means the system looks like states that did not erupt soon,
* high tail-risk tension means the system looks unlike those safe states and more like states that might be close to failure.

Two broad possibilities exist:

* In a world where triggering is partly predictable, this tail-risk tension:

  * tends to rise before large eruptions,
  * stays moderate in most quiet times.
* In a world where triggering is effectively opaque, no matter how we summarize the system:

  * tail-risk tension cannot separate pre-eruption periods from normal variability,
  * small changes in how we encode the state completely change the result.

Q097 does not claim to solve eruption prediction. It does not tell us exactly when a given volcano will erupt. Instead, it offers:

* a way to think about the problem as a question of whether useful tail-risk structure exists in the configuration space,
* explicit experiments that can falsify or support specific ways of encoding that structure,
* reusable tools for other problems where rare, extreme events arise in complex systems.

In the Tension Universe framework, Q097 is a prototype for how to treat extreme physical hazards as questions about tail-risk tension, without crossing the boundary into hidden or unobservable rules.
