# Q091 · Equilibrium climate sensitivity

## 0. Header metadata

```txt
ID: Q091
Code: BH_EARTH_CLIMATE_SENS_L3_091
Domain: Earth system and climate
Family: Climate dynamics
Rank: S
Projection_dominance: I
Field_type: dynamical_field
Tension_type: thermodynamic_tension
Status: Partial
Semantics: continuous
E_level: E1
N_level: N1
Last_updated: 2026-01-25
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

Equilibrium climate sensitivity (ECS) is an effective number that describes how much the global mean surface temperature will eventually change when the radiative forcing of the climate system is increased by a specified amount and then held fixed until a new equilibrium is reached.

In the standard setting:

* A reference state is chosen, usually preindustrial conditions.
* Carbon dioxide concentration is doubled relative to this reference.
* Other long lived greenhouse gases and forcing agents are treated in a consistent way.
* The system is allowed to evolve until fast and intermediate feedbacks have acted and a new statistical equilibrium is reached.

The canonical definition used in many assessments is:

* ECS is the eventual change in global mean surface air temperature, measured in degrees Celsius or Kelvin, for a doubling of carbon dioxide concentration, after the ocean and atmosphere have come to a new equilibrium, but before very slow processes such as large ice sheet changes have fully equilibrated.

Formally, at the effective layer for this project:

* There is a reference forcing `F_2xCO2` that represents the radiative forcing from carbon dioxide doubling relative to a baseline.
* For each world model considered, there is an effective equilibrium temperature change `DeltaT_eq` for that forcing.
* ECS is defined as:

```txt
ECS = DeltaT_eq / F_2xCO2
```

where the units are adjusted so that ECS is expressed as a temperature change per specified forcing scenario, or as a temperature change if `F_2xCO2` is taken as a fixed constant.

The central scientific question is not whether ECS exists, but:

* What range of ECS values is consistent with known physics and observations.
* Whether there is a reasonably narrow band in which ECS is likely to lie.
* How this band changes when new evidence is added.

### 1.2 Status and difficulty

Equilibrium climate sensitivity has been studied for many decades. The broad structure is understood:

* Basic radiative physics gives a lower bound: without feedbacks, doubling carbon dioxide would produce a modest temperature change.
* Feedbacks from water vapor, clouds, sea ice, and other processes amplify or damp this response.
* Coupled atmosphere ocean models, energy balance models, and observational constraints provide multiple lines of evidence.

However, there is still substantial uncertainty:

* Cloud feedbacks, especially low level cloud responses, remain difficult to constrain.
* Deep ocean heat uptake introduces long time scales, which complicates the relationship between transient warming and equilibrium warming.
* Observational records are finite in length and contain internal variability that can mask or mimic forced responses.

Recent assessments have suggested:

* Very low ECS values are unlikely.
* Very high ECS values are also disfavored, but not completely ruled out.
* The most likely range lies in a band, but that band is still wide enough to have large implications for long term risk.

The problem is therefore:

* Partially constrained by a large body of evidence.
* Still open regarding the exact numeric range and tails of the distribution.
* Structurally difficult because it combines thermodynamics, fluid dynamics, radiative transfer, and statistical inference.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q091 plays several roles:

1. It is the primary example of a thermodynamic_tension problem in the Earth system domain, where global energy balance, feedbacks, and long time scale dynamics interact.
2. It provides a reference point for other Earth system problems such as tipping points, carbon cycle feedbacks, and Anthropocene dynamics, which reuse its components.
3. It offers a way to express climate sensitivity as a tension problem:

   * between forcings and responses,
   * between model based and observation based estimates,
   * between physically plausible feedbacks and statistical fits.

Q091 does not aim to determine a single true value of ECS. Instead, it frames ECS as:

* An observable that lives in an effective state space.
* A source of thermodynamic_tension when different lines of evidence do not align.
* A calibration problem for how Tension Universe encodings behave when faced with complex, partially observed physical systems.

### References

1. IPCC, 2021. "Climate Change 2021: The Physical Science Basis." Contribution of Working Group I to the Sixth Assessment Report of the Intergovernmental Panel on Climate Change. Cambridge University Press. See Chapter 7 and the Summary for Policymakers sections on climate feedbacks and equilibrium climate sensitivity.
2. Knutti, R., and Hegerl, G. C., 2008. "The equilibrium sensitivity of the Earth’s temperature to radiation changes: observations and model results." Nature Geoscience 1, 735–743.
3. Roe, G. H., and Baker, M. B., 2007. "Why is climate sensitivity so unpredictable?" Science 318, 629–632.
4. Sherwood, S. C., Webb, M. J., Annan, J. D., Armour, K. C., Forster, P. M., et al., 2020. "An assessment of Earth's climate sensitivity using multiple lines of evidence." Reviews of Geophysics 58, e2019RG000678.

---

## 2. Position in the BlackHole graph

This block records how Q091 sits inside the BlackHole graph as nodes and edges among Q001–Q125. Each edge is listed with a one line reason that points to a concrete component or tension type.

### 2.1 Upstream problems

These problems provide prerequisites, tools, or general foundations that Q091 relies on at the effective layer.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Provides the coarse grained thermodynamic and energy balance principles used to define global energy budget fields for Q091.

* Q093 (BH_EARTH_CARBON_CYCLE_L3_093)
  Reason: Supplies carbon cycle feedback structure that determines effective forcing and feedback parameters in the ECS_TensionFunctional.

* Q094 (BH_EARTH_OCEAN_MIX_L3_094)
  Reason: Defines constraints on deep ocean mixing and circulation that shape long term heat uptake and the mapping from forcing to DeltaT_eq.

### 2.2 Downstream problems

These problems directly reuse Q091 components or depend on Q091 tension structure.

* Q092 (BH_EARTH_TIPPING_L3_092)
  Reason: Reuses ECS_TensionFunctional as an input when estimating how close the system is to climate tipping thresholds.

* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: Uses EquilibriumClimateState_Descriptor to define Anthropocene steady state candidates under different forcing trajectories.

* Q099 (BH_EARTH_WATER_STRESS_L3_099)
  Reason: Uses ECS driven equilibrium warming from Q091 as a driver for long term freshwater redistribution scenarios.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q041 (BH_COSMO_DARKMATTER_L3_041)
  Reason: Both involve hidden components inferred from indirect observables under thermodynamic_tension between energy budgets and observed fields.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Both analyse links between information measures and thermodynamic budgets, but in Q091 the system is the climate rather than an abstract information engine.

### 2.4 Cross domain edges

Cross domain edges connect Q091 to problems in other domains that can reuse its components.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Reuses the idea of a tension functional that compares energy balance models with data constrained descriptions as a case study of information thermodynamics.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: Uses ECS based risk tails and EquilibriumClimateState_Descriptor as inputs into long term alignment scenarios where powerful AI systems plan over climate outcomes.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We describe:

* state space,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rules or construction of internal TU fields from raw data.

### 3.1 State space

We assume the existence of a state space

```txt
M
```

with the following interpretation at the effective layer:

* Each element `m` in `M` represents a coherent climate sensitivity configuration for a specified forcing scenario.
* A state `m` aggregates:

  * a global energy budget summary for that scenario,
  * a small set of feedback descriptors (for example short wave cloud feedback, long wave cloud feedback, water vapor feedback, surface albedo feedback),
  * an effective equilibrium global mean temperature response `DeltaT_eq(m)` to the forcing,
  * a compact score describing how strongly `m` is constrained by observations rather than only by model structure.

We do not specify how these states are constructed from simulations or observations. We only require that for any fixed forcing scenario of interest, there exist states in `M` that encode reasonable candidate equilibrium responses whose observables are finite and well defined.

We also assume there is a fixed reference forcing constant `F_2xCO2` associated with carbon dioxide doubling, used as a scaling factor but not tuned during experiments.

### 3.2 Effective fields and observables

We introduce the following effective fields and observables on `M`.

1. Effective forcing for the scenario

```txt
F_eq(m)
```

* A nonnegative scalar that represents the effective radiative forcing for the scenario encoded in `m`, in consistent units.
* For the canonical ECS scenario, `F_eq(m)` is normally equal to `F_2xCO2`, but the encoding allows other scenarios if needed.

2. Equilibrium temperature response

```txt
DeltaT_eq(m)
```

* The long term equilibrium change in global mean surface temperature, relative to the chosen baseline, for the forcing scenario encoded in `m`.
* This is an effective quantity that summarises the eventual response including fast and intermediate feedbacks.

3. Equilibrium climate sensitivity number

```txt
ECS(m) = DeltaT_eq(m) / F_ref
```

where `F_ref` is a fixed positive constant, chosen once for Q091. In the canonical case `F_ref` is equal to `F_2xCO2`. The exact numerical value of `F_ref` is not part of the TU encoding; it is part of the physical context.

4. Feedback vector

```txt
FeedbackVector(m)
```

* A vector valued observable that encodes the aggregated contributions of main feedbacks.
* Components may include, for example, water vapor, lapse rate, cloud, and surface albedo feedbacks, but at the effective layer we treat them as unnamed entries in a finite vector.

5. Observation constraint score

```txt
ObsConstraintScore(m)
```

* A scalar in a fixed interval, for example between 0 and 1.
* A higher value means that the state `m` is more strongly supported by observations, such as historical energy budget fits or paleoclimate reconstructions.
* A lower value means the state is based mainly on unconstrained model structure.

All of these observables are assumed to be well defined real valued functions on a suitable subset of `M`. They are not defined by any explicit algorithm in this document.

### 3.3 Mismatch and tension components

We now define mismatch components that will be combined into a tension functional. To avoid after the fact tuning, we fix a small library of reference objects and weight choices before any experiment is considered.

#### 3.3.1 Admissible reference band for ECS

We choose a closed interval

```txt
[ECS_low_ref, ECS_high_ref]
```

that represents a reference band for ECS values, based on expert assessments from external literature. The precise numeric values are not important for TU; what matters is that:

* The band is fixed once for Q091 and is not adjusted based on Q091 experiment outcomes.
* It is wide enough to include ECS values that are physically plausible under current knowledge.
* It is narrow enough that lying far outside the band signals meaningful tension.

We also fix a finite library of bands

```txt
B_1, B_2, ..., B_K
```

that may be used in later stages for refined analysis. In this Stage 1 encoding, we use only the primary band `[ECS_low_ref, ECS_high_ref]`.

#### 3.3.2 Sensitivity mismatch

We define the sensitivity mismatch

```txt
DeltaS_sens(m)
```

as follows:

* If `ECS_low_ref <= ECS(m) <= ECS_high_ref`, then

```txt
DeltaS_sens(m) = 0
```

* Otherwise,

```txt
DeltaS_sens(m) = distance from ECS(m) to the nearest bound
```

in the usual real number sense. This means:

* If `ECS(m)` is below `ECS_low_ref`, the distance is `ECS_low_ref - ECS(m)`.
* If `ECS(m)` is above `ECS_high_ref`, the distance is `ECS(m) - ECS_high_ref`.

This mismatch is always nonnegative and is zero exactly when ECS lies inside the reference band.

#### 3.3.3 Model versus observation mismatch

We assume that for states in `M` that represent worlds where both models and observations are available, there exist two derived quantities:

```txt
ECS_model(m)
ECS_obs(m)
```

* `ECS_model(m)` is the ECS implied by model based analysis inside `m`.
* `ECS_obs(m)` is the ECS implied by observation based constraints inside `m`.

We then define

```txt
DeltaS_model(m) = (ECS_model(m) - ECS_obs(m))^2
```

where the square is taken in the usual real sense. This term is nonnegative and measures disagreement between model and observation based ECS estimates.

#### 3.3.4 Feedback structure mismatch

We define a function

```txt
FeedbackRangePenalty(FeedbackVector(m))
```

that is:

* Nonnegative.
* Equal to zero if all components of `FeedbackVector(m)` lie inside predetermined physically acceptable ranges.
* Positive if any component lies outside such ranges or if the combination of components implies net feedback strength that is outside a predetermined plausible band.

We then set

```txt
DeltaS_feedback(m) = FeedbackRangePenalty(FeedbackVector(m))
```

This captures the tension between feedback combinations encoded in `m` and basic physical limits.

#### 3.3.5 Combined ECS mismatch

We fix three positive weights

```txt
w_sens, w_model, w_fb
```

satisfying

```txt
w_sens + w_model + w_fb = 1
```

These weights are:

* Chosen once for Q091.
* Drawn from a finite set of simple rational values (for example halves, quarters).
* Recorded as part of the encoding and not adjusted after any experiment results.

We then define the combined ECS mismatch:

```txt
DeltaS_ECS(m) = w_sens * DeltaS_sens(m)
              + w_model * DeltaS_model(m)
              + w_fb * DeltaS_feedback(m)
```

By construction, `DeltaS_ECS(m)` is nonnegative and equals zero only when:

* ECS lies inside the reference band.
* Model and observation based ECS agree.
* Feedbacks lie inside their acceptable ranges.

### 3.4 Effective tension tensor and singular set

#### 3.4.1 Effective tension tensor

We follow the TU core pattern and define an effective tension tensor

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_ECS(m) * lambda(m) * kappa
```

where:

* `S_i(m)` is a source like factor for the i th semantic source component, for example the strength of the climate forcing discussion in the current reasoning context.
* `C_j(m)` is a receptivity like factor for the j th downstream or cognitive component that is affected by climate sensitivity assumptions.
* `DeltaS_ECS(m)` is the combined mismatch defined above.
* `lambda(m)` is a convergence state factor that indicates whether reasoning around `m` is in a convergent, recursive, divergent, or chaotic mode; it is bounded between two fixed positive constants.
* `kappa` is a coupling constant that sets the overall scale for ECS related thermodynamic_tension in this encoding.

The details of `S_i`, `C_j`, and `lambda` are not exposed here. We only assume that for each `m` in the regular domain, `T_ij(m)` is finite.

#### 3.4.2 Singular set and domain restriction

Some observables can become undefined or unbounded. To handle this, we define the singular set

```txt
S_sing = { m in M :
           ECS(m) is undefined or not finite
           or F_eq(m) <= 0
           or FeedbackVector(m) is undefined
           or ObsConstraintScore(m) is undefined }
```

We then take the regular domain

```txt
M_reg = M \ S_sing
```

and impose the following rule:

* All Q091 tension functionals and experiments are evaluated only on `M_reg`.
* If a procedure would require evaluating `DeltaS_ECS(m)` or `Tension_ECS(m)` for `m` in `S_sing`, the result is treated as "out of domain" and is not interpreted as evidence about ECS or about the truth of any physical proposition.

This is a domain restriction choice. We do not attempt to regularise or interpret singular states in a weak sense. The practical effect is:

* Experiments in Block 6 will specify how they handle missing or ill defined states.
* Statistical summaries will be taken over states in `M_reg` only.

---

## 4. Tension principle for this problem

This block states how Q091 is characterised as a tension problem within TU, at the effective layer.

### 4.1 Core tension functional

We define an effective ECS tension functional

```txt
Tension_ECS(m) = DeltaS_ECS(m) / max(ObsConstraintScore(m), eps_obs)
```

where:

* `DeltaS_ECS(m)` is the combined mismatch from Block 3.
* `ObsConstraintScore(m)` is the observation constraint score.
* `eps_obs` is a small positive constant fixed once for Q091, which prevents division by very small scores and avoids giving unlimited weight to states with almost no observational support.

This functional has the following behaviour:

* For states that are strongly constrained by observations, high mismatch leads to high ECS tension.
* For states that are weakly constrained, the denominator keeps the tension finite but still penalises large mismatches.
* If a state fits the reference band, the model observation agreement, and feedback ranges while being well constrained, then `Tension_ECS(m)` is small.

### 4.2 ECS as a low tension principle

At the effective layer, Q091 can be phrased as the following low tension principle:

> In physically reasonable world models that respect both known climate physics and observational constraints, there exists a narrow band of ECS values for which the ECS tension functional is small and stable under refinement of data and models.

More concretely, suppose we consider a sequence of states

```txt
m_1, m_2, ..., m_n, ...
```

that represent increasingly refined descriptions of the same real world, as more data and more detailed models are incorporated, but with the encoding class and weights fixed. The low tension principle asserts that there exists a band

```txt
[ECS_low_star, ECS_high_star]
```

such that for states whose ECS lies inside this band:

```txt
Tension_ECS(m_k) <= tau_low
```

for a small threshold `tau_low` that does not grow without bound as `k` increases, except for fluctuations that can be explained by finite data or model resolution.

### 4.3 ECS failure as persistent high tension

The complementary high tension picture is:

> If the combination of physical laws, feedback structures, and observational records is such that no stable ECS band exists, then any encoding that remains faithful to the evidence will show persistent high ECS tension.

In this case, for any candidate band `[ECS_low, ECS_high]` and for any encoding that deserves to be called faithful, we would eventually find states representing the real world for which:

```txt
Tension_ECS(m_fail) >= tau_high
```

where `tau_high` is a fixed positive threshold that cannot be pushed arbitrarily close to zero just by refining the description. In practice, this would manifest as:

* model based ECS and observation based ECS estimates that stay far apart,
* feedback combinations that repeatedly violate plausible ranges,
* an inability to find a narrow band where tension is reliably low.

Q091 does not assert which of these pictures is realised in our universe. It only provides:

* a way to express the problem in terms of a tension functional,
* a set of observables to monitor,
* a language to compare low tension and high tension worlds.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds at the effective layer:

* World L: a low sensitivity world.
* World H: a high sensitivity world.

We do not construct any deep generative rules. We only describe patterns in observables and tension scores.

### 5.1 World L (low sensitivity world)

In World L:

1. ECS band

   * Most observationally supported states `m_L` have

   ```txt
   ECS(m_L) in [ECS_low_L, ECS_high_L]
   ```

   where `[ECS_low_L, ECS_high_L]` is a band at the lower end of physically plausible sensitivities, such as values near 2 degrees Celsius per carbon dioxide doubling.

2. Sensitivity mismatch

   * For these states, `DeltaS_sens(m_L)` is close to zero because ECS lies well inside the reference band.
   * `DeltaS_model(m_L)` is small because model based and observation based ECS estimates are compatible.
   * `DeltaS_feedback(m_L)` is small because feedback combinations lie inside their plausible ranges.

3. Global ECS tension

   * The ECS tension functional satisfies

   ```txt
   Tension_ECS(m_L) <= tau_low
   ```

   for reasonably small `tau_low`. Refining data or model detail shrinks fluctuations in tension rather than driving it upward.

4. Long term response pattern

   * Equilibrium warming remains moderate even under large forcing, and this is reflected in many states that combine:

     * moderate `DeltaT_eq(m_L)`,
     * consistent feedback vectors,
     * good observation constraint scores.

### 5.2 World H (high sensitivity world)

In World H:

1. ECS band

   * Many observationally relevant states `m_H` exhibit

   ```txt
   ECS(m_H) in [ECS_low_H, ECS_high_H]
   ```

   where `[ECS_low_H, ECS_high_H]` is a band at the high end of plausible sensitivities, for example values closer to 5 or 6 degrees Celsius per carbon dioxide doubling.

2. Sensitivity mismatch and model observation tension

   * If reference bands and feedback ranges are chosen based on standard physical and observational arguments, then:

     * `DeltaS_sens(m_H)` tends to be larger, because ECS values sit near or beyond the upper part of the reference band.
     * `DeltaS_model(m_H)` may be large when models that imply high ECS struggle to match historical energy budget constraints.
     * `DeltaS_feedback(m_H)` can grow when required feedback combinations approach or exceed physically plausible limits.

3. Global ECS tension

   * For many states representing the real world under this assumption, we have

   ```txt
   Tension_ECS(m_H) >= tau_high
   ```

   for a strictly positive `tau_high` that persists under refinement.

4. Long term response pattern

   * Equilibrium warming is large under realistic forcing trajectories.
   * Many states with high observation constraint score and consistent energy budgets still require large feedback strengths, leading to sustained thermodynamic_tension between different lines of evidence.

### 5.3 Interpretive note

These counterfactual worlds do not say anything about which world we actually inhabit. They only illustrate:

* How the same TU encoding behaves under two different assumptions about the structure of ECS.
* How observable patterns, such as `ECS(m)`, `FeedbackVector(m)`, and `ObsConstraintScore(m)`, would lead to different tension profiles.
* How the existence or absence of a stable low tension ECS band becomes a central question.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments at the effective layer that can:

* test the coherence of the Q091 encoding,
* distinguish between different ECS related tension models,
* provide evidence for or against particular parameter choices.

These experiments can falsify specific TU encodings related to Q091. They do not prove or disprove any physical law by themselves.

### Experiment 1: Historical energy balance tension profile

*Goal:*

Test whether the chosen ECS tension functional `Tension_ECS` aligns in a stable way with historical energy balance constraints, given fixed encoding parameters.

*Setup:*

* Use published reconstructions of:

  * global mean surface temperature over the historical period,
  * radiative forcing histories (greenhouse gases, aerosols, solar, volcanic),
  * estimates of ocean heat content change.

* Fix:

  * the reference band `[ECS_low_ref, ECS_high_ref]`,
  * the weights `w_sens`, `w_model`, `w_fb`,
  * the constant `eps_obs`.

* Construct a simple energy balance model class with a range of ECS values, for example values from 1 to 6 degrees Celsius per doubling.

*Protocol:*

1. For each candidate ECS value in the chosen range, calibrate an energy balance model to the historical forcing and temperature records.

2. For each calibrated model, construct a state `m_hist(ECS_value)` in `M_reg` that encodes:

   * `F_eq(m_hist)`,
   * `DeltaT_eq(m_hist)` implied by the model,
   * an `ECS_model(m_hist)` equal to the ECS value used,
   * an `ECS_obs(m_hist)` inferred from a standard energy balance fit,
   * a feedback vector consistent with the model,
   * an observation constraint score derived from fit quality.

3. For each `m_hist(ECS_value)`, compute:

   * `DeltaS_sens(m_hist)`,
   * `DeltaS_model(m_hist)`,
   * `DeltaS_feedback(m_hist)`,
   * `DeltaS_ECS(m_hist)`,
   * `Tension_ECS(m_hist)`.

4. Plot or otherwise summarise `Tension_ECS(m_hist)` as a function of ECS value.

*Metrics:*

* The location and width of the ECS band where `Tension_ECS(m_hist)` is minimal.
* The height of `Tension_ECS(m_hist)` outside this band.
* Stability of these features when:

  * the time window is slightly changed,
  * observational uncertainty is varied within reasonable limits.

*Falsification conditions:*

* If, after fixing encoding parameters as described, no reasonably narrow ECS band can be identified where `Tension_ECS(m_hist)` is consistently lower than outside the band, then this particular tension encoding is considered falsified for Q091.
* If very small changes in encoding choices, such as tiny adjustments of weights inside the allowed finite library, can move the apparent low tension band across the entire ECS range without a clear physical reason, then the encoding is considered unstable and rejected.

*Semantics implementation note:*

All quantities in this experiment are treated as continuous fields or continuous time series summaries, consistent with the continuous field view declared in Block 0. No discrete or hybrid encodings are introduced here.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment can reject specific choices of `Tension_ECS` and related parameters, but it does not directly determine the true value of ECS.

---

### Experiment 2: Model ensemble versus emergent constraints

*Goal:*

Check whether the ECS tension encoding can systematically distinguish between model states that are compatible with emergent constraints and those that are not.

*Setup:*

* Consider a multi model ensemble of climate models, each with:

  * a diagnosed ECS value,
  * a set of feedback parameters,
  * simulated observables that can be compared with emergent constraint relationships.

* Obtain one or more emergent constraint relationships from the literature that link present day or historical climate statistics to ECS.

*Protocol:*

1. For each model in the ensemble, construct a state `m_model` in `M_reg` that encodes:

   * `ECS_model(m_model)` equal to the model’s ECS,
   * `ECS_obs(m_model)` derived from emergent constraint relations,
   * `FeedbackVector(m_model)` from the model output,
   * `ObsConstraintScore(m_model)` based on how well the model matches the emergent constraint data.

2. Compute `DeltaS_sens(m_model)`, `DeltaS_model(m_model)`, `DeltaS_feedback(m_model)`, and `Tension_ECS(m_model)`.

3. Partition the models into:

   * a set that is broadly consistent with emergent constraints,
   * a set that is clearly inconsistent.

4. Compare the distributions of `Tension_ECS(m_model)` in these two sets.

*Metrics:*

* Mean and spread of `Tension_ECS(m_model)` for models that respect emergent constraints.
* Mean and spread for models that violate emergent constraints.
* Overlap between the two distributions.

*Falsification conditions:*

* If models that respect emergent constraints do not show lower ECS tension than models that violate them, in a statistically clear way, then the current choice of `Tension_ECS` and mismatch components is considered misaligned for Q091.
* If models with very similar observables and feedbacks receive very different tension scores without a clear explanation from the mismatch components, the encoding is judged inconsistent and rejected.

*Semantics implementation note:*

Model outputs and constraints are treated as continuous summary statistics and fields, consistent with the continuous field view from Block 0. The encoding does not rely on discrete approximations in this experiment.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment tests only whether the ECS tension encoding behaves in a reasonable way on a model ensemble, not whether any particular model is correct or what the true ECS value is.

---

## 7. AI and WFGY engineering spec

This block describes how Q091 can be used as an engineering module for AI systems within the WFGY framework, at the effective layer.

### 7.1 Training signals

We define several training signals that can be used in AI models to encourage ECS aware and tension aware reasoning about climate questions.

1. `signal_ecs_band_penalty`

   * Definition: a nonnegative signal proportional to `DeltaS_sens(m)` whenever the model proposes or relies on an ECS value outside the reference band.
   * Purpose: discourage reasoning paths that assume extremely low or extremely high ECS values without clearly marking them as speculative.

2. `signal_feedback_consistency`

   * Definition: a signal based on `DeltaS_feedback(m)` that increases when implied feedback combinations violate physical ranges.
   * Purpose: guide the model toward feedback narratives that respect known limits even when reasoning in a qualitative way.

3. `signal_obs_model_gap`

   * Definition: a signal derived from `DeltaS_model(m)` that measures disagreement between model implied and observation implied ECS in the current state.
   * Purpose: penalise explanations or scenarios that rely on models which are far from observational constraints, unless this is explicitly stated.

4. `signal_ecs_tension_score`

   * Definition: directly equal to `Tension_ECS(m)` for a given internal state `m`.
   * Purpose: provide a scalar tension indicator that can be minimised or monitored when answering questions where long term climate response is relevant.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q091 structures without revealing any deep TU generative rules.

1. `ClimateSensitivityHead`

   * Role: a module that, given an internal representation of a climate related context, produces an estimate of `Tension_ECS(m)` and its components.
   * Interface:

     * Inputs: internal embeddings or structured summaries representing forcing, feedbacks, and evidence.
     * Outputs: a scalar tension estimate and a small set of component scores such as `DeltaS_sens`, `DeltaS_model`, and `DeltaS_feedback`.

2. `EarthSystemRiskFilter`

   * Role: a module that flags answers which imply high equilibrium climate sensitivity combined with weak evidence, or which understate risks given the assumed ECS band.
   * Interface:

     * Inputs: candidate answers and their associated internal states.
     * Outputs: soft masks or scores indicating whether the answer should be revised or marked as high uncertainty.

3. `TU_ClimateObserver`

   * Role: a general observer module that reads internal representations and produces a simplified `EquilibriumClimateState_Descriptor` for use by other parts of the system.
   * Interface:

     * Inputs: embeddings connected to climate state descriptions.
     * Outputs: a low dimensional descriptor capturing forcing, ECS estimates, and key feedback indicators.

### 7.3 Evaluation harness

We suggest an evaluation harness for AI models that include Q091 based modules.

1. Task selection

   * Select sets of questions that require reasoning about long term warming under different emission or forcing scenarios.
   * Include questions that test understanding of the difference between transient and equilibrium response.

2. Conditions

   * Baseline condition:

     * The model operates without Q091 specific modules.
     * Answers are judged on correctness and internal consistency.

   * TU condition:

     * The model uses Q091 modules to track `Tension_ECS` and related signals.
     * High tension answers can be revised or marked as speculative.

3. Metrics

   * Consistency of ECS related statements across different parts of the same conversation.
   * Frequency of contradictory claims about how much the climate will warm under specified forcing.
   * Clarity of distinction between well constrained ranges and speculative extremes.

### 7.4 60 second reproduction protocol

A minimal protocol to let external users experience the impact of Q091 encoding in an AI system.

* Baseline setup

  * Prompt: ask the AI to explain what equilibrium climate sensitivity is and how it affects long term warming under carbon dioxide doubling, without mentioning tension or ECS bands.
  * Observation: record whether the explanation clearly separates central estimates from extreme possibilities, and whether it explains why uncertainty exists.

* TU encoded setup

  * Prompt: ask the same question, but request that the AI explicitly organise the explanation around:

    * a reference ECS band,
    * sources of tension between models and observations,
    * the idea of a low tension ECS band.

  * Observation: record whether the explanation now:

    * identifies a central ECS band,
    * discusses feedbacks and observational constraints,
    * highlights which parts of the range are high tension.

* Comparison metric

  * Use a rubric that scores:

    * conceptual accuracy,
    * explicitness of assumptions,
    * internal consistency about ECS ranges and risks.

* What to log

  * Both answers,
  * internal tension scores if available,
  * any flags raised by `EarthSystemRiskFilter`.

This protocol does not require access to TU internals. It only uses Q091 components as an organising frame for explanations.

---

## 8. Cross problem transfer template

This block describes the reusable components produced by Q091 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `ECS_TensionFunctional`

   * Type: functional

   * Minimal interface:

     * Inputs: a bundle containing `F_eq`, `DeltaT_eq`, `FeedbackVector`, `ECS_model`, `ECS_obs`, and `ObsConstraintScore` for a state.
     * Output: a nonnegative scalar `tension_value` equal to `Tension_ECS(m)`.

   * Preconditions:

     * The input bundle must correspond to a state in `M_reg` where all fields are defined and finite.
     * The reference band and weights must be those fixed for Q091.

2. ComponentName: `EquilibriumClimateState_Descriptor`

   * Type: field

   * Minimal interface:

     * Inputs: a forcing scenario descriptor and associated physical context.
     * Output: a compact descriptor of the equilibrium climate state, including `F_eq`, `DeltaT_eq`, `ECS`, and a small number of feedback and constraint indicators.

   * Preconditions:

     * The scenario must fall within the range where an equilibrium description is meaningful (for example not in regimes of runaway greenhouse or complete glaciation).
     * Required physical information such as approximate energy budget and feedback structure must be available.

3. ComponentName: `ECS_CounterfactualWorld_Template`

   * Type: experiment_pattern

   * Minimal interface:

     * Inputs: a specification of a low ECS band and a high ECS band, plus simple constraints on feedback and observational support.
     * Output: two experiment templates describing World L and World H style scenarios and how to compute `Tension_ECS` in each.

   * Preconditions:

     * The bands and constraints must respect basic physical and observational limits and must be fixed before any data fitting.

### 8.2 Direct reuse targets

1. Q092 (BH_EARTH_TIPPING_L3_092)

   * Reused component: `ECS_TensionFunctional`.
   * Why it transfers: climate tipping analyses often depend on both the magnitude and timing of warming relative to thresholds. ECS related tension directly affects how close the system is to such thresholds in the long term.
   * What changes: in Q092, the output of `ECS_TensionFunctional` is combined with tipping specific fields such as critical temperatures and feedback switches, forming a composite tension measure.

2. Q098 (BH_EARTH_ANTHROPOCENE_L3_098)

   * Reused component: `EquilibriumClimateState_Descriptor`.
   * Why it transfers: Anthropocene dynamics depend on the long term climate state under sustained human forcing. ECS based descriptors provide a base layer for those states.
   * What changes: Q098 augments the descriptor with socio economic variables and land use patterns, and uses it to define multiple possible Anthropocene equilibria.

3. Q121 (BH_AI_ALIGNMENT_L3_121)

   * Reused component: `ECS_CounterfactualWorld_Template`.
   * Why it transfers: alignment scenarios that consider long horizon planning under climate uncertainty can reuse World L and World H style branches as environmental backdrops.
   * What changes: in Q121, the focus shifts from physical accuracy to the impact of different ECS worlds on AI decisions and safety constraints. ECS tension becomes part of a broader risk landscape.

---

## 9. TU roadmap and verification levels

This block explains how Q091 is positioned along the TU verification ladder and what the next measurable steps are.

### 9.1 Current levels

* E_level: E1

  * A concrete effective layer encoding for ECS has been specified, including:

    * state space observables,
    * mismatch components,
    * a combined tension functional,
    * a singular set and domain restriction.

  * At least one experiment has clear falsification conditions that apply to the encoding.

* N_level: N1

  * The narrative linking ECS, feedbacks, and tension is explicit and coherent at a basic level.
  * It is accessible to readers familiar with climate science but does not yet explore deeper structural links to other BlackHole problems.

### 9.2 Next measurable step toward E2

To move from E1 to E2 for Q091, at least one of the following should be implemented in practice:

1. A working tool that:

   * reads standardised datasets for historical forcing, temperature, and ocean heat content,
   * constructs states `m_data` in `M_reg`,
   * computes `Tension_ECS(m_data)` over a range of ECS values and model structures,
   * publishes the resulting tension profiles and the encoding parameters.

2. A model ensemble analysis that:

   * uses `ECS_TensionFunctional` on a multi model ensemble,
   * documents how tension scores distribute between models that are consistent with emergent constraints and those that are not,
   * demonstrates that these findings are reproducible by independent groups.

These steps remain at the effective layer. They operate on observable summaries and model outputs, not on any hidden TU generative rules.

### 9.3 Long term role in the TU program

In the long term, Q091 is expected to serve as:

* The central node for thermodynamic_tension problems in the Earth system cluster.
* A test bed for encoding complex, partially constrained physical problems where both natural variability and anthropogenic forcing are present.
* A bridge between Earth system science and AI safety questions that rely on climate trajectories, by providing a disciplined way to talk about equilibrium responses and their uncertainty.

---

## 10. Elementary but precise explanation

Equilibrium climate sensitivity is a way of summarising a very complicated question in a single number:

* If we double the amount of carbon dioxide in the atmosphere and then wait a long time for the climate system to settle down, how much warmer will the planet become on average?

We know that:

* Without feedbacks, the answer would be a modest warming.
* In reality, feedbacks from water vapor, clouds, snow and ice, and other processes amplify the warming.
* Different models and different kinds of evidence do not all agree on the exact amount.

In the Tension Universe view, we do not try to pick one magic number for ECS. Instead, we do three things.

First, we describe states:

* A state collects the basic facts for a given scenario:

  * how strong the forcing is,
  * how much warming is implied,
  * how the main feedbacks add up,
  * how well this picture matches observations.

Second, we measure mismatches:

* We check whether ECS in that state falls inside a reasonable reference band.
* We check whether model based and observation based estimates agree.
* We check whether the feedbacks look physically plausible.

Each mismatch is turned into a nonnegative number. If everything lines up well, these numbers are small. If something is off, they grow.

Third, we combine mismatches into a tension score:

* The ECS tension is small when a state fits all of the following:

  * ECS is inside the reference band.
  * Models and observations agree.
  * Feedbacks stay inside their plausible ranges.

* The tension becomes large when these pieces conflict.

We can then imagine:

* A low sensitivity world, where there is a narrow band of ECS values that keeps tension low as we add more data.
* A high sensitivity world, where any honest attempt to match observations and physics with high ECS values leads to persistent high tension.

This approach does not tell us which world is real. It does something simpler and more controlled:

* It gives us a clear list of observables to watch.
* It provides experiments that can falsify bad ways of encoding climate sensitivity.
* It creates building blocks that other problems, such as tipping points and Anthropocene dynamics, can reuse.

Q091 is therefore the place in the Tension Universe where equilibrium climate sensitivity is turned from a single mysterious number into a structured tension problem that can be analysed, tested, and connected to many other questions.
