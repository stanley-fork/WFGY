# Q094 · Deep ocean mixing and circulation

## 0. Header metadata

```txt
ID: Q094
Code: BH_EARTH_OCEAN_MIX_L3_094
Domain: Earth system science
Family: Physical oceanography and climate dynamics
Rank: S
Projection_dominance: M
Field_type: dynamical_field
Tension_type: thermodynamic_tension
Status: Open
Semantics: continuous
E_level: E1
N_level: N1
Last_updated: 2026-01-25
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical problem behind Q094 can be stated as follows.

Deep ocean mixing and large scale overturning circulation must together close the global budgets of:

* heat,
* mechanical and buoyancy related energy,
* key tracers such as carbon and nutrients,

on climate time scales ranging from decades to millennia. The open question is whether there exists a coherent and physically consistent description of deep ocean mixing and circulation that:

1. respects known constraints from observations and theory on energy input, dissipation, and stratification,
2. reproduces observed deep tracer and heat distributions within credible error bounds,
3. remains stable under refinement of models and data, instead of requiring ad hoc or unphysical mixing structures.

In simple terms:

> Can we describe deep ocean mixing and circulation in a way that closes the global energy and tracer budgets without violating physical constraints, and that remains coherent as we look more closely at the system?

This canonical problem is not a single theorem to prove. It is a coupled inference and consistency task. The question is whether there exists an effective description of deep mixing and overturning that satisfies all known constraints and does so in a way that is robust to improved resolution and observations.

### 1.2 Status and difficulty

Key points about the current scientific status:

1. Observations show that the deep ocean is stratified yet weakly mixed, with mixing driven by processes such as internal wave breaking, boundary turbulence, and mesoscale eddies. Direct measurements are sparse in space and time.
2. The large scale overturning circulation connects surface and deep waters across basins and between hemispheres, and it is sensitive to wind forcing, buoyancy fluxes, and small scale mixing.
3. Energetic arguments show that only a finite amount of mechanical energy is available to drive diapycnal mixing. This constrains how strong deep mixing can be if it is to remain physically plausible.
4. Tracer and heat distributions in the deep ocean indicate that real mixing is highly inhomogeneous, with enhanced mixing in some regions and very weak mixing in others.
5. Climate models require parametrizations of deep mixing and overturning that are not uniquely determined by theory and limited data. Different choices can lead to different projections of heat uptake, carbon storage, and circulation changes.

Because of these factors, the problem of defining a unified and physically consistent description of deep ocean mixing and circulation remains open. It is not classified as a single classical conjecture, but it has the character of an S level structural problem. The difficulty arises from:

* multi scale dynamics,
* limited observations,
* strong coupling between energy, stratification, mixing, and circulation,

and from the requirement that any proposed description must satisfy several independent constraints at the same time.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q094 plays several roles.

1. It is the main Earth system node for thermodynamic_tension in the physical ocean, focusing on how energy input, mixing, and circulation jointly determine deep ocean states.
2. It links the climate sensitivity and carbon cycle problems (for example Q091 and Q093) to the actual physical transport and storage mechanisms in the ocean interior.
3. It provides a template for how to encode:

   * small scale turbulence and mixing,
   * large scale circulation pathways,
   * global budget closure,

within a single effective tension functional.

4. It serves as an example of a problem where the system is not only mathematically complex but also observationally incomplete, so any encoding must handle domain restrictions and singular sets explicitly.

### References

1. IPCC, 2021, “Climate Change 2021: The Physical Science Basis”, Contribution of Working Group I to the Sixth Assessment Report of the Intergovernmental Panel on Climate Change, Cambridge University Press. Chapters on ocean heat uptake and large scale circulation.
2. Wunsch, C. and Ferrari, R., 2004, “Vertical mixing, energy, and the general circulation of the oceans”, Annual Review of Fluid Mechanics, 36, 281–314.
3. Munk, W., 1966, “Abyssal recipes”, Deep Sea Research and Oceanographic Abstracts, 13(4), 707–730. See also Munk, W. and Wunsch, C., 1998, “Abyssal recipes II: energetics of tidal and wind mixing”, Deep Sea Research Part I, 45(12), 1977–2010.
4. Kunze, E., 2017, “Internal wave driven mixing: mechanisms and parameterization”, Annual Review of Marine Science, 9, 205–236.

---

## 2. Position in the BlackHole graph

This block records how Q094 sits inside the BlackHole graph as edges among Q001–Q125.

### 2.1 Upstream problems

These provide prerequisites, tools, or general frameworks that Q094 relies on at the effective layer.

* Q039 (BH_PHYS_TURBULENCE_L3_039)
  Reason: Supplies turbulence and cascade concepts needed to interpret how small scale motions generate effective mixing coefficients in the ocean interior.

* Q091 (BH_EARTH_CLIM_SENS_L3_091)
  Reason: Provides global energy balance constraints that any deep mixing and circulation configuration must satisfy over climate time scales.

* Q093 (BH_EARTH_CARBON_FEEDBACK_L3_093)
  Reason: Encodes carbon cycle frameworks that restrict how deep ocean mixing and overturning can store and release carbon in the Earth system.

### 2.2 Downstream problems

These reuse Q094 components or treat Q094 tension patterns as constraints.

* Q099 (BH_EARTH_FRESHWATER_L3_099)
  Reason: Reuses deep mixing and overturning templates to propagate freshwater anomalies and assess long term water stress patterns.

* Q098 (BH_EARTH_ANTHROPOCENE_DYN_L3_098)
  Reason: Uses deep ocean storage and transport as slow components in Anthropocene scale response and recovery trajectories.

* Q100 (BH_EARTH_ENV_PANDEMIC_RISK_L3_100)
  Reason: Reuses ocean circulation pathways and mixing templates when reasoning about marine related pollutant or pathogen transport.

### 2.3 Parallel problems

Nodes here share similar tension types but do not depend on Q094 at the module level.

* Q091 (BH_EARTH_CLIM_SENS_L3_091)
  Reason: Both treat thermodynamic_tension between energy input, storage, and dissipation across Earth system compartments, though Q091 is global and Q094 is ocean specific.

* Q092 (BH_EARTH_CLIM_TIPPING_L3_092)
  Reason: Both involve multistable circulation states and slow fast dynamics, but they operate on different state spaces and stability structures.

* Q095 (BH_EARTH_BIODIV_LOSS_L3_095)
  Reason: Both depend on transport and storage processes controlling long term ecological patterns, yet Q095 focuses on biodiversity and ecosystems rather than physical mixing.

### 2.4 Cross domain edges

Edges here connect Q094 to problems in other domains that can reuse its components.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Reuses thermodynamic_tension ideas linking microscopic dissipation and macroscopic energy budgets in complex systems.

* Q059 (BH_CS_INFO_THERMO_L3_059)
  Reason: Uses Q094 as a physical analogy for the thermodynamic cost of mixing and information dissipation.

* Q105 (BH_SOC_SYSTEMIC_CRASH_L3_105)
  Reason: Reuses the pattern of hidden transport networks plus slow storage when reasoning about delayed responses and abrupt shifts in socio technical systems.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We describe:

* state space,
* effective fields and observables,
* invariants and tension scores,
* singular set and domain restriction.

We do not describe any hidden generative rule or construction of internal TU fields from raw data.

### 3.1 State space

We introduce a state space

```txt
M_ocean
```

with this interpretation:

* Each element `m` in `M_ocean` represents a coarse grained “deep ocean configuration” containing:

  * vertically resolved summaries of mixing coefficients and stratification,
  * large scale overturning circulation summaries,
  * regional energy and tracer budgets over chosen time windows.

We assume that:

* There is a finite library of regions and basins,

  ```txt
  L_region = { R_1, ..., R_N }
  L_basin  = { B_1, ..., B_M }
  ```

  and each `m` provides fields and summaries on these elements.

* The construction of `m` from raw data or model output is not described in TU terms. It is treated as an external process that yields well defined summaries.

### 3.2 Effective fields and observables

We define the following effective fields and observables on `M_ocean`. All outputs are real valued and finite for states in the regular domain introduced later.

1. Mixing coefficient field

```txt
K_mix(m; R_k, z_bin)
```

* Input: state `m`, region `R_k` in `L_region`, vertical bin index `z_bin`.
* Output: an effective diapycnal mixing coefficient for that coarse cell.
* Interpretation: summarises the net impact of small scale turbulence and internal wave breaking.

2. Overturning circulation summary

```txt
Psi_overturn(m; B_j, depth_bin)
```

* Input: state `m`, basin `B_j` in `L_basin`, vertical bin index `depth_bin`.
* Output: a scalar summarising the strength and direction of large scale overturning at that depth in that basin.
* Interpretation: a coarse summary of overturning streamfunction structure.

3. Energy budget mismatch observable

```txt
DeltaS_energy(m; R_k)
```

* Input: state `m`, region `R_k`.
* Output: nonnegative scalar measuring the mismatch between:

  * mechanical and buoyancy related energy input,
  * storage and dissipation,
    in region `R_k` over a chosen time window.
* Properties:

  * `DeltaS_energy(m; R_k) >= 0` for all states in the regular domain.
  * `DeltaS_energy(m; R_k) = 0` when the encoded budgets close within the accepted tolerance.

4. Tracer budget mismatch observable

```txt
DeltaS_tracer(m; B_j, tracer_type)
```

* Input: state `m`, basin `B_j`, tracer label such as heat or carbon.
* Output: nonnegative scalar measuring inconsistency between:

  * deep tracer distributions implied by `K_mix` and `Psi_overturn`,
  * observed or externally specified tracer distributions,
    for that tracer in basin `B_j`.
* Properties:

  * `DeltaS_tracer(m; B_j, tracer_type) >= 0`.
  * `DeltaS_tracer(m; B_j, tracer_type) = 0` when implied and observed tracer fields agree within the accepted tolerance.

### 3.3 Combined mixing tension functional

We define a combined mixing tension functional on `M_ocean` using fixed weights.

1. Weight constraints

We choose two positive weights:

```txt
w_energy > 0
w_tracer > 0
w_energy + w_tracer = 1
```

These weights are fixed once for the problem and cannot be tuned after examining data or outcomes.

2. Basin and region aggregation

We define averaged mismatches:

```txt
E_mis(m) = max over R_k in L_region of DeltaS_energy(m; R_k)

T_mis(m) = max over (B_j, tracer_type) in L_basin x L_tracer
           of DeltaS_tracer(m; B_j, tracer_type)
```

where `L_tracer` is a finite set of tracers of interest such as heat and carbon. The maxima are taken over finite sets, so they are well defined for all states where each mismatch is finite.

3. Global mixing tension

The global tension functional is:

```txt
Tension_mix(m) = w_energy * E_mis(m) + w_tracer * T_mis(m)
```

Properties:

* `Tension_mix(m) >= 0` for all states in the regular domain.
* `Tension_mix(m)` is small when both energy and tracer mismatches are small.
* `Tension_mix(m)` grows when mismatches in either sector grow.

The choice of weights and finite libraries defines an admissible encoding class. Different admissible choices may exist, but any particular study must specify them in advance.

### 3.4 Singular set and domain restriction

Some states represent incomplete or inconsistent descriptions where mismatch observables are not finite. To handle this, we define the problem specific singular set:

```txt
S_sing = { m in M_ocean :
           exists R_k or B_j or tracer_type
           such that DeltaS_energy(m; R_k) or
                    DeltaS_tracer(m; B_j, tracer_type)
           is undefined or not finite }
```

We then restrict attention to the regular domain:

```txt
M_ocean_reg = M_ocean \ S_sing
```

Rules:

* All evaluations of `E_mis`, `T_mis`, and `Tension_mix` are only defined on `M_ocean_reg`.
* When an experiment encounters a state in `S_sing`, the outcome is labelled “out of domain” rather than being treated as evidence about deep mixing physics.

This explicit domain restriction prevents divergent or incomplete configurations from being mistaken for genuine high tension states.

---

## 4. Tension principle for this problem

This block states how Q094 is characterised as a tension problem within TU.

### 4.1 Core tension principle

The core principle for Q094 can be stated as:

> Deep ocean mixing and large scale overturning circulation should form configurations for which the combined energy and tracer budget mismatches, summarised by `Tension_mix(m)`, can be kept within a low and stable band across regions, basins, and tracers, when the configuration is consistent with physical constraints and observations.

In more detail:

* Low tension configurations:

  * For many states `m_T` in `M_ocean_reg` that represent physically plausible and well constrained worlds,
  * both `E_mis(m_T)` and `T_mis(m_T)` lie within small bounds,
  * `Tension_mix(m_T)` remains within a band associated with acceptable closure of budgets.

* High tension configurations:

  * For states `m_F` that attempt to represent the actual world but rely on inconsistent or unphysical mixing and overturning patterns,
  * at least one of `E_mis(m_F)` or `T_mis(m_F)` is large,
  * `Tension_mix(m_F)` remains bounded away from zero even after refining data and parametrizations in ways that respect independent constraints.

### 4.2 Role of constraints

The tension principle includes explicit constraints:

* Energetic constraints:

  * Available mechanical energy from winds and tides is limited.
  * Diapycnal mixing must not exceed what this energy can plausibly support.

* Stratification constraints:

  * Observed stratification profiles limit how much mixing can occur without destroying density structure.

* Tracer constraints:

  * Observed distributions of heat and carbon in the deep ocean restrict allowable combinations of mixing and overturning.

The Q094 tension principle requires that any proposed configuration must respect all three constraint types at the same time in order to qualify as a low tension solution.

---

## 5. Counterfactual tension worlds

We describe two counterfactual worlds that differ only in their effective deep mixing and circulation patterns. We stay at the effective layer and do not describe how internal fields are constructed from data.

### 5.1 World T (well behaved deep mixing and circulation)

World T represents a class of worlds where deep mixing and circulation are physically consistent and observationally plausible.

Characteristics:

1. Energy budget closure

   * For world representing states `m_T` in `M_ocean_reg`, the energy mismatch satisfies:

     ```txt
     E_mis(m_T) <= epsilon_energy
     ```

     for a small threshold `epsilon_energy` that reflects measurement and model uncertainties.

2. Tracer budget closure

   * For heat and carbon tracers in all basins, the tracer mismatch satisfies:

     ```txt
     T_mis(m_T) <= epsilon_tracer
     ```

     where `epsilon_tracer` is a small threshold consistent with known observational errors and model limitations.

3. Stable global mixing tension

   * The global mixing tension satisfies:

     ```txt
     Tension_mix(m_T) <= epsilon_mix
     ```

     for a small `epsilon_mix`, and this bound remains of the same order when the library of regions and basins is refined and when more precise data are added.

4. Physical plausibility

   * Mixing coefficients `K_mix(m_T; R_k, z_bin)` remain within ranges that can be supported by known sources of mechanical energy and turbulence.
   * Overturning circulation summaries `Psi_overturn(m_T; B_j, depth_bin)` are consistent with large scale observational constraints.

### 5.2 World F (pathological or mis specified deep mixing)

World F represents a class of worlds where deep mixing and overturning are mis specified in a way that cannot satisfy constraints.

Characteristics:

1. Energy budget failure

   * For some states `m_F` in `M_ocean_reg`, there exist regions `R_k` where:

     ```txt
     DeltaS_energy(m_F; R_k) >= delta_energy
     ```

     with `delta_energy` strictly larger than credible tolerance levels derived from observations and theory.

2. Tracer inconsistency

   * For some basins and tracers, the mismatch satisfies:

     ```txt
     DeltaS_tracer(m_F; B_j, tracer_type) >= delta_tracer
     ```

     where `delta_tracer` is too large to be explained by observational and modelling uncertainty.

3. Persistent high tension

   * For world representing states `m_F`, the global tension satisfies:

     ```txt
     Tension_mix(m_F) >= delta_mix
     ```

     with `delta_mix > 0` that cannot be removed by refining the region and basin library or by incorporating additional physically consistent data.

4. Implausible parameter regimes

   * Some mixing coefficients or overturning patterns require energy sources that are not available or would destroy observed stratification if realised.

### 5.3 Interpretive note

World T and World F are not claims about the actual Earth. They are effective layer constructions to express:

* how deep ocean mixing and circulation could behave in a low tension regime,
* how they would behave in a high tension regime that conflicts with constraints.

The Q094 tension principle then asks which class better matches the available evidence when evaluated with a particular admissible encoding.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that:

* test the coherence of the Q094 encoding,
* distinguish between different deep mixing models,
* provide evidence for or against particular parameter choices.

These experiments can falsify Q094 related encodings at the effective layer. They do not solve the canonical problem.

### Experiment 1: Energy budget consistency under mixing profiles

*Goal:*
Test whether a given family of deep mixing and overturning encodings is consistent with regional and global energy budgets.

*Setup:*

* Input data:

  * output from an ocean or climate model with several prescribed mixing parameter sets,
  * external estimates of mechanical energy input to the deep ocean in each region,
  * estimates of observed stratification.
* For each parameter set, an external procedure constructs a state `m_param` in `M_ocean` that encodes:

  * `K_mix(m_param; R_k, z_bin)`,
  * `Psi_overturn(m_param; B_j, depth_bin)`,
  * derived energy budget summaries.

*Protocol:*

1. For each parameter set, check whether `m_param` lies in `M_ocean_reg`. If not, flag as out of domain and exclude from tension analysis.
2. For each `m_param` in `M_ocean_reg`, compute `DeltaS_energy(m_param; R_k)` for all regions `R_k` in `L_region`.
3. Compute `E_mis(m_param)` and `Tension_mix(m_param)` using the fixed weights and tracer related components that are defined for this experiment.
4. Record the distribution of `Tension_mix(m_param)` across parameter sets and regions.
5. Compare the tension values against a pre defined low tension band derived from energetic and observational constraints.

*Metrics:*

* Fraction of parameter sets for which `Tension_mix(m_param)` lies within the low tension band.
* Maximum and median values of `E_mis(m_param)` across regions.
* Sensitivity of tension values to small changes in mixing parameters.

*Falsification conditions:*

* If, for all parameter sets that obey basic physical constraints on mixing strength and energy input, the observed `Tension_mix(m_param)` exceeds the low tension band by a significant margin, then the current encoding of `DeltaS_energy`, region library, and weight selection is considered falsified.
* If small changes in mixing parameters produce large and erratic swings in `Tension_mix(m_param)` without clear physical reasons, the encoding is considered unstable and rejected for Q094.

*Semantics implementation note:*
All quantities are represented as continuous fields on coarse regions and depth bins. The evaluation of mismatch and tension uses finite sums and maxima, consistent with the continuous field interpretation in the metadata.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject specific Q094 encodings, but it does not provide a unique deep ocean mixing solution.

---

### Experiment 2: Tracer inversion consistency

*Goal:*
Assess whether combining `K_mix` and `Psi_overturn` can reproduce deep tracer distributions within realistic error bounds.

*Setup:*

* Input data:

  * observed or externally specified deep tracer distributions for heat and carbon in each basin,
  * a family of mixing and overturning parametrizations that yield states `m_trial` in `M_ocean`.
* A forward model maps each state `m_trial` to predicted tracer fields, without being described in TU terms.

*Protocol:*

1. For each `m_trial`, verify membership in `M_ocean_reg`. If not, mark as out of domain.
2. For each basin and tracer, compute `DeltaS_tracer(m_trial; B_j, tracer_type)` by comparing predicted and observed tracer summaries.
3. Compute `T_mis(m_trial)` and `Tension_mix(m_trial)` using the fixed weights.
4. Analyse how `Tension_mix(m_trial)` changes across the family of parametrizations.

*Metrics:*

* Basin wise distributions of tracer mismatches.
* Global tracer mismatch measure `T_mis(m_trial)` for each state.
* Trade off between fitting tracer data and preserving energy budget consistency (by reusing results from Experiment 1).

*Falsification conditions:*

* If, under any physically plausible combination of mixing and overturning parametrizations, `T_mis(m_trial)` cannot be reduced below a threshold consistent with observational uncertainties, the current tracer mismatch definition or region selection is considered falsified.
* If parametrizations that produce acceptable tracer fits require mixing patterns that violate energy constraints established in Experiment 1, the joint encoding of energy and tracer tension is considered misaligned.

*Semantics implementation note:*
Tracer fields and mismatches are represented as continuous field summaries aggregated over finite regions and basins. All operations use finite sums and differences, consistent with the continuous field interpretation.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment tests the joint encoding of mixing, circulation, and tracers but does not determine the unique true configuration of the deep ocean.

---

## 7. AI and WFGY engineering spec

This block describes how Q094 can be used as an engineering module for AI systems within the WFGY framework.

### 7.1 Training signals

We introduce training signals that use Q094 tension quantities in AI models.

1. `signal_mixing_energy_balance`

   * Definition: a penalty signal proportional to `E_mis(m)` for states inferred from climate related prompts or internal representations.
   * Purpose: discourage internal configurations that imply large unclosed energy mismatches in deep ocean regions.

2. `signal_tracer_pathway_consistency`

   * Definition: a signal derived from `T_mis(m)` when the model reasons about deep heat or carbon storage patterns.
   * Purpose: penalise internal states that combine mixing and overturning in ways that are inconsistent with expected tracer distributions.

3. `signal_ocean_tension_score`

   * Definition: a scalar supervision target equal to `Tension_mix(m)` for constructed states in training scenarios.
   * Purpose: provide a simple tension metric that can be minimised in tasks where physically plausible deep ocean behaviour is desired.

4. `signal_scenario_contrast`

   * Definition: a signal that measures relative tension between alternative policy or forcing scenarios `m_1` and `m_2` constructed from different climate narratives.
   * Purpose: help the model compare the physical plausibility and risk profile of different scenario descriptions.

### 7.2 Architectural patterns

We outline patterns that can reuse Q094 structures without exposing internal TU generative rules.

1. `OceanTensionHead`

   * Role: takes internal embeddings representing deep ocean or climate states and outputs an estimate of `Tension_mix(m)` and a decomposition into energy and tracer parts.
   * Interface:

     * Input: embedding vector summarising ocean relevant context.
     * Output: scalar tension estimate and a small vector `[E_mis_estimate, T_mis_estimate]`.

2. `VerticalProfileEncoder`

   * Role: converts textual or numerical descriptions of stratification and mixing into a compact representation compatible with the state space `M_ocean`.
   * Interface:

     * Input: profile descriptions for a region or basin.
     * Output: encoded features that can be fed into the OceanTensionHead.

3. `ScenarioComparator`

   * Role: given two scenario representations, estimates differential tension and highlights which aspects of mixing and circulation drive the difference.
   * Interface:

     * Input: two internal state representations.
     * Output: difference in estimated tension and an explanation vector tying it to energy and tracer mismatches.

### 7.3 Evaluation harness

A simple evaluation harness for AI models augmented with Q094 modules:

1. Task selection

   * Select tasks where the model must reason about:

     * deep ocean heat uptake,
     * long term carbon storage in the ocean,
     * overturning circulation responses to forcing.

2. Conditions

   * Baseline condition:

     * Model operates without explicit Q094 tension modules.
   * Q094 condition:

     * Model uses OceanTensionHead and related signals during training or inference.

3. Metrics

   * Accuracy on questions that require correctly ranking or explaining different mixing and overturning scenarios.
   * Consistency between qualitative narratives and implied energy and tracer budget closure.
   * Robustness under small perturbations of the prompt or input data.

### 7.4 60 second reproduction protocol

A minimal protocol for external users to experience the impact of Q094 encoding in an AI system.

* Baseline setup:

  * Prompt: ask the AI to explain how deep ocean mixing and overturning affect long term climate, including heat and carbon storage, without any reference to tension or explicit budgets.
  * Observation: record whether the explanation is vague, internally inconsistent, or missing key constraints.

* Q094 encoded setup:

  * Prompt: ask the same question but require the explanation to:

    * explicitly mention closure of energy and tracer budgets,
    * describe the role of mixing coefficients and overturning patterns,
    * indicate how inconsistent configurations would manifest as high tension.
  * Observation: record whether the explanation becomes more structured and constraint aware.

* Comparison metric:

  * Human or expert judges score the two explanations on:

    * clarity of the budget closure story,
    * consistency with known physical constraints,
    * explicit recognition of deep ocean time scales.

* What to log:

  * The prompts, responses, and any tension estimates produced by Q094 modules.
  * This enables later inspection and comparison without exposing any deep TU generative mechanism.

---

## 8. Cross problem transfer template

This block lists reusable components produced by Q094 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `DeepMixingTensionFunctional`

   * Type: functional
   * Minimal interface:

     * Inputs: `mixing_profiles`, `overturning_summaries`, `budget_constraints`.
     * Output: `tension_value` as a nonnegative scalar indicating consistency of deep mixing and circulation with energy and tracer budgets.
   * Preconditions:

     * Inputs describe coherent summaries on the finite region and basin library.
     * Basic physical constraints on energy availability are already enforced.

2. ComponentName: `OceanColumnStateField`

   * Type: field
   * Minimal interface:

     * Inputs: `location`, `depth_range`.
     * Output: descriptors of stratification, mixing, and storage suitable for climate scale reasoning.
   * Preconditions:

     * Location and depth range belong to defined regions and depth bins.
     * Observational or model based summaries exist for those elements.

3. ComponentName: `MixingScenarioComparator`

   * Type: experiment_pattern
   * Minimal interface:

     * Inputs: two sets of deep mixing and overturning summaries.
     * Output: a comparative report containing:

       * estimated tension for each scenario,
       * sectors where energy or tracer budgets are most stressed.
   * Preconditions:

     * Both scenarios use the same region and basin library and the same budget constraints.

### 8.2 Direct reuse targets

1. Target: Q091 (Equilibrium climate sensitivity)

   * Reused component: `DeepMixingTensionFunctional`.
   * Why it transfers: Q091 needs to connect surface forcing and global energy balance to deep ocean heat uptake patterns. The functional constrains how much energy can be stored in the deep ocean without violating budgets.
   * What changes: the focus shifts to time integrated heat uptake and its role in the global sensitivity parameter.

2. Target: Q093 (Full carbon cycle feedbacks)

   * Reused component: `OceanColumnStateField`.
   * Why it transfers: long term carbon storage and release depend on how carbon is sequestered in and returned from deep ocean layers.
   * What changes: tracers of interest include dissolved inorganic carbon and related chemical variables in addition to heat.

3. Target: Q099 (Global freshwater dynamics)

   * Reused components: `OceanColumnStateField` and `MixingScenarioComparator`.
   * Why it transfers: freshwater anomalies travel through and are stored in deep ocean structures shaped by mixing and overturning.
   * What changes: tracers include salinity and freshwater content, and the comparator highlights regions where anomalies are likely to persist or resurface.

---

## 9. TU roadmap and verification levels

This block explains how Q094 is positioned on the TU verification ladder and what the next measurable steps are.

### 9.1 Current levels

* E_level: E1

  * A coherent effective encoding of deep ocean mixing and circulation has been specified.
  * Tension observables and a combined tension functional have been defined, with explicit weights and finite libraries.
  * At least two discriminating experiments with clear falsification conditions have been described.

* N_level: N1

  * The narrative connects small scale mixing, large scale overturning, and global budget closure in a single framework.
  * Counterfactual low tension and high tension worlds have been outlined.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following concrete steps should be achieved:

1. Implement a prototype tool that:

   * takes model based deep mixing and overturning summaries as input,
   * constructs states in `M_ocean_reg`,
   * computes `Tension_mix(m)` for a set of standard climate scenarios,
   * publishes the tension profiles for external scrutiny.

2. Carry out an initial application of Experiments 1 and 2 on:

   * a limited set of climate model outputs and observations,
   * with fully specified region and basin libraries,
   * and report whether the resulting tension values fall in plausible ranges.

These steps remain entirely within the effective layer. They do not require exposing any deep TU generative mechanism.

### 9.3 Long term role in the TU program

In the longer term, Q094 is expected to serve as:

* The central Earth system node for thermodynamic_tension in the ocean, connecting mixing, circulation, and climate time scales.
* A template for how to treat under observed yet structurally constrained systems where closure of budgets is the main organising principle.
* A bridge between climate physics, biogeochemistry, and risk analysis nodes that depend on slow but powerful deep ocean processes.

---

## 10. Elementary but precise explanation

This block provides a non expert explanation that stays aligned with the effective layer description.

The deep ocean is a huge, cold, and dark reservoir that stores heat, carbon, and other tracers for very long times. Small scale turbulence and waves mix water up and down, while large scale currents slowly move water masses between regions and between the surface and the deep.

Scientists know that:

* only a limited amount of energy is available to stir the deep ocean,
* mixing cannot be too strong or it would erase the observed layering,
* mixing cannot be too weak or it would fail to explain how heat and carbon reach the deep ocean.

At the same time, we can measure how much heat and carbon end up stored in the deep ocean over decades and centuries. The difficult part is to find descriptions of mixing and circulation that:

* respect energy limits,
* preserve stratification,
* match the observed patterns of heat and carbon.

In the Tension Universe view, we do not try to write down every fluid motion. Instead, we ask:

* For a given summary of mixing and circulation, how badly do the energy and tracer budgets fail to close?
* Can we assign a number, the mixing tension, that is small when the budgets nearly close and large when they do not?

We imagine a space of possible “ocean configurations”. Each configuration records:

* how strong mixing is in different regions and depths,
* how strong large scale currents are,
* how much energy and tracer mismatch appears in each region.

From this information we calculate a mixing tension. Then we compare two types of worlds:

* In a low tension world, we can choose mixing and currents so that:

  * energy input, storage, and dissipation nearly balance,
  * heat and carbon distributions are reproduced within reasonable error bars.
* In a high tension world, any attempt to match the data either:

  * violates energy limits, or
  * produces tracer patterns that do not look like the real ocean.

This does not tell us the exact true state of the deep ocean. It does not solve the full fluid dynamics. However, it gives us:

* a way to say when a proposed mixing and circulation picture is physically and observationally coherent,
* a way to test and reject encodings that are inconsistent,
* reusable tools for AI systems that need to reason about deep ocean behaviour inside the wider climate and Earth system.

Q094 is the node that organises all of this inside the Tension Universe. It turns the question “how does the deep ocean really mix and circulate?” into a precise problem about closing budgets and controlling tension across time scales.
