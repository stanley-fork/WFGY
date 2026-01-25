# Q096 · Earthquake predictability

## 0. Header metadata

```txt
ID: Q096
Code: BH_EARTH_QUAKE_FORECAST_L3_096
Domain: Earth system and climate
Family: Solid Earth and seismology
Rank: S
Projection_dominance: P
Field_type: solid_earth_field
Tension_type: predictability_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-25
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical question of earthquake predictability can be stated in an effective form as follows:

> To what extent, and on what spatial and temporal scales, can the future occurrence of damaging earthquakes be forecast in a way that is:
>
> * statistically reliable,
> * physically interpretable,
> * and useful for risk reduction decisions,
>
> beyond what is achievable by time-independent or trivial reference models?

Here, “forecast” is interpreted in the modern seismological sense:

* as a probabilistic statement about the number, locations, magnitudes, and times of earthquakes over specified windows,
* not as a deterministic prediction of a single event with exact time, place, and magnitude.

The problem decomposes into several tightly coupled questions:

1. Whether strong short-term predictability exists (hours to days) beyond aftershock clustering and simple empirical rules.
2. How much medium-term predictability (months to years) can be extracted from seismicity patterns, stress transfer, and fault system models.
3. How to integrate long-term geological and geodetic information into multi-decade hazard fields.
4. How to test claims of predictability in a prospective, reproducible way.

Within the BlackHole project, Q096 focuses on the fundamental limits and structures of predictability, not on any single algorithm or operational system.

### 1.2 Status and difficulty

The current scientific consensus distinguishes sharply between:

* **Deterministic prediction**

  * Statements such as “There will be a magnitude 7.5 earthquake within 10 km of this city at 14:32 tomorrow.”
  * Major geological surveys and seismological societies repeatedly state that such predictions are not currently possible and may be fundamentally unattainable with present knowledge and data.
* **Probabilistic forecasting**

  * Time-dependent, location-dependent probabilities of earthquake occurrence, evaluated over finite windows.
  * This includes long-term hazard maps, short-term clustering models, and operational earthquake forecasting frameworks.

Operationally:

* Institutions such as the United States Geological Survey emphasize that earthquakes cannot be predicted in the deterministic sense, but that probabilistic assessments and hazard maps are central tools for risk management.
* Research programs such as the Collaboratory for the Study of Earthquake Predictability (CSEP) have established global experiments to test earthquake forecast models prospectively, using standardized metrics.
* The field of operational earthquake forecasting (OEF) has developed guidelines for how time-dependent seismicity models should be evaluated and, when appropriate, communicated for civil protection.

The deep difficulty of Q096 arises from the combination of:

* strong heterogeneity and complexity of fault systems,
* limited observational windows in both space and time,
* strong clustering and heavy-tail behavior of seismic sequences,
* and substantial societal pressure for simple yes/no answers that the physics does not obviously support.

There is no consensus answer to the core question “how predictable are earthquakes, in principle.” The field is active, with ongoing work on physical models, statistical models, and testing frameworks.

### 1.3 Role in the BlackHole project

Within the BlackHole S-collection, Q096 serves as:

1. The flagship **predictability_tension** node for geohazards: it encodes how far the real Earth lies between “essentially unpredictable” and “strongly predictable” regimes for earthquakes.

2. A template for multi-scale hazard fields, coupling:

   * short-term aftershock and swarm dynamics,
   * medium-term regional seismicity rates,
   * and long-term tectonic loading and fault structures.

3. A bridge from fundamental geophysics to societal decision-making, because the value of any predictability is only realized through changes in building codes, response plans, and real-time actions.

4. A reference point for other hazard predictability problems (hurricanes, compound extremes, wildfires, space weather), which reuse its components.

### References

1. United States Geological Survey (USGS), “Can you predict earthquakes?”, Earthquake Hazards Program, official public FAQ, accessed 2026.
2. T. H. Jordan, “Earthquake predictability, brick by brick”, Seismological Research Letters, 77(1):3–6, 2006.
3. G. M. Marzocchi and T. H. Jordan, “Operational Earthquake Forecasting: State of knowledge and guidelines for utilization”, Annals of Geophysics, 54(4):315–342, 2011.
4. D. Schorlemmer et al., “The Collaboratory for the Study of Earthquake Predictability (CSEP): A global earthquake predictability experiment”, Seismological Research Letters, 81(5):861–867, 2010.

---

## 2. Position in the BlackHole graph

This block records how Q096 sits inside the BlackHole graph among Q001–Q125. Each edge is listed with a one-line reason that points to a concrete component or tension type.

### 2.1 Upstream problems

These nodes provide prerequisites or general frameworks that Q096 relies on at the effective layer.

* Q091 (BH_EARTH_MULTI_HAZARD_FIELD_L3_091)
  Reason: Supplies the general multi-hazard field formalism that Q096 specializes to seismic hazard fields.
* Q092 (BH_EARTH_TAIL_RISK_CASCADES_L3_092)
  Reason: Provides tools for modeling heavy tails and cascading risk that are essential for clustered seismicity and aftershock sequences.
* Q093 (BH_EARTH_TIPPING_POINTS_CEE_L3_093)
  Reason: Contributes general methods for dealing with non-linear transitions and regime shifts, relevant for fault system state changes.

### 2.2 Downstream problems

Downstream nodes reuse components or depend directly on Q096’s predictability structures.

* Q095 (BH_EARTH_COMPOUND_EXTREMES_L3_095)
  Reason: Uses Q096’s hazard field and predictability envelopes as one component of multi-hazard corridors that include earthquakes.
* Q097 (BH_EARTH_GIGAFIRE_REGIME_L3_097)
  Reason: Reuses predictability_tension structures for large wildfires, by analogy with clustered, heavy-tail behavior and limited forecast skill.
* Q099 (BH_SPACE_SPACE_WEATHER_CASCADE_L3_099)
  Reason: Adapts the predictability_tension envelope to space weather events, using Q096 as the calibration reference for rare, high-impact phenomena.

### 2.3 Parallel problems

Parallel nodes share similar tension types but do not directly reuse specific components.

* Q094 (BH_EARTH_HURRICANE_PATTERN_L3_094)
  Reason: Both Q096 and Q094 address storm-like or shock-like hazard fields where limited predictability and societal demand for forecasts create strong predictability_tension.
* Q098 (BH_EARTH_GRAVITY_WAVE_COUPLING_L3_098)
  Reason: Both treat wave-like phenomena where partial, scale-dependent predictability must be encoded under severe observational limits.

### 2.4 Cross-domain edges

Cross-domain edges connect Q096 to nodes in other domains that reuse its components.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Reuses Q096’s predictability envelope constructs for evaluating forecast models and scoring rules in information-theoretic terms.
* Q123 (BH_AI_INTERP_L3_123)
  Reason: Uses earthquake predictability as a case study for interpreting how AI models represent hazard, uncertainty, and heavy-tail events in internal states.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* state spaces,
* observable fields and invariants,
* tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rule or any mapping from raw data to internal TU fields.

### 3.1 State space

We assume a state space:

```txt
M_quake
```

where each state `m` in `M_quake` represents a coherent “seismic regime configuration” over a specified region and time horizon. At the effective layer, a state encodes:

* summaries of past seismicity (event counts, locations, magnitudes, clustering indicators),
* current time-varying estimates of stress and strain at a coarse level,
* a set of candidate forecast models and their parameters,
* and coarse descriptors of exposure or risk-relevant zones.

We do not specify how these summaries are computed from catalogs, geodetic measurements, or physical simulations. We only require that:

* for each region `R` and time horizon `H` in a fixed library of region-horizon pairs, there exist states in `M_quake` that encode:

  * a forecast distribution of earthquake numbers and magnitudes,
  * and matching observable summaries of actual or simulated seismicity.

### 3.2 Forecast and observation observables

We introduce the following effective observables on `M_quake`.

1. Forecast rate field

```txt
lambda_fore(m; R, H, M_min)
```

* Input: state `m`, region `R`, time horizon `H`, minimum magnitude `M_min`.
* Output: a nonnegative scalar representing the forecast average rate of earthquakes with magnitude at least `M_min` in region `R` over horizon `H`.

2. Forecast count distribution

```txt
P_fore(m; R, H, M_min; k)
```

* Input: state `m`, region `R`, horizon `H`, minimum magnitude `M_min`, integer `k >= 0`.
* Output: the forecast probability of observing exactly `k` such events in that space-time window.
* For each fixed `(m, R, H, M_min)`, the function of `k` is a discrete distribution that sums to 1.

3. Observed count summary

```txt
N_obs(m; R, H, M_min)
```

* Input: state `m`, region `R`, horizon `H`, minimum magnitude `M_min`.
* Output: an integer count summarizing the number of events actually realized in the corresponding window, as encoded in `m`.

4. Scoring rule library

We assume a finite library of proper scoring rules for count forecasts:

```txt
L_eq_score = { S_1, S_2, ..., S_K }
```

Each `S_j` is a function that takes a forecast distribution and an observed count and returns a real-valued score:

```txt
S_j( P_fore(m; R, H, M_min; ·), N_obs(m; R, H, M_min) )
```

The library `L_eq_score` is fixed in advance and does not depend on the particular state or dataset. It includes at least one strictly proper scoring rule.

5. Model library

We assume a finite library of seismicity forecast models:

```txt
L_eq_model = { M_1, M_2, ..., M_L }
```

For each model `M_l` and each region-horizon pair, there is a corresponding forecast encoded within `m`. The library is fixed before any evaluation and cannot be tuned event by event.

### 3.3 Predictability mismatch observables

Using the scoring and model libraries, we define several mismatch observables.

1. Model performance observable

```txt
Perf(m; M_l, S_j) = average_score over a test set
```

* For each model `M_l` and scoring rule `S_j`, `Perf(m; M_l, S_j)` summarizes the performance of `M_l` over a fixed prospective or retrospective test set encoded in `m`.

2. Best-known performance

```txt
Perf_best(m; S_j) = max over l in {1,...,L} Perf(m; M_l, S_j)
```

3. Reference or trivial performance

We define a simple reference model `M_ref` (for example, a time-independent Poisson model with spatial smoothing). Its performance is:

```txt
Perf_ref(m; S_j)
```

4. Predictability gain observable

```txt
Gain(m; S_j) = Perf_best(m; S_j) - Perf_ref(m; S_j)
```

This measures how much better the best model in the library performs, relative to the trivial reference, under scoring rule `S_j`.

5. Predictability mismatch scalar

We define an effective nonnegative mismatch observable:

```txt
DeltaS_pred(m) = max over j in {1,...,K} G_j(m)
```

where each `G_j(m)` is constructed as:

```txt
G_j(m) = max( 0, Target_gain_j - Gain(m; S_j) )
```

and `Target_gain_j` is a fixed benchmark gain for scoring rule `S_j`. The benchmark values are chosen in advance based on historical experiments and are not tuned per dataset.

Properties:

* `DeltaS_pred(m) >= 0` for all `m`.
* `DeltaS_pred(m) = 0` if, for all scoring rules, the best model meets or exceeds the target gains.

### 3.4 Tension tensor components and invariants

We define an effective predictability tension scalar:

```txt
Tension_EQ(m) = alpha * DeltaS_pred(m)
```

with `alpha > 0` a fixed scale factor. This scalar is then embedded into a TU-style tension tensor over `M_quake`:

```txt
T_ij(m) = S_i(m) * C_j(m) * Tension_EQ(m) * lambda_state(m) * kappa_eq
```

where:

* `S_i(m)` represents the intensity of the ith source component (for example, tectonic loading, catalog completeness limits).
* `C_j(m)` represents the sensitivity of the jth downstream component (for example, civil protection decisions, infrastructure planning).
* `lambda_state(m)` encodes the local reasoning regime (for example, convergent, recursive, divergent, or chaotic) within a bounded range.
* `kappa_eq` is a coupling constant setting the overall scale of predictability_tension.

From this we extract invariants such as:

1. Multi-scale predictability envelope

```txt
E_pred(m) = vector of Gains and DeltaS_pred over region-horizon families
```

2. Predictability contrast invariant

```txt
I_contrast(m) = difference between best and worst model gains
```

which measures structural diversity in the library.

### 3.5 Singular set and domain restrictions

Some states may be unfit for meaningful predictability analysis:

* catalogs with severe gaps or mis-located events,
* forecast libraries that collapse to trivial or ill-defined distributions,
* scoring evaluations based on too few events.

We define a singular set:

```txt
S_sing = { m in M_quake :
           DeltaS_pred(m) is undefined, or
           some Perf(m; M_l, S_j) is undefined over the required test set, or
           the basic count or rate observables are not finite }
```

We impose the following rule:

* All Q096-related tension analysis is restricted to the regular domain:

  ```txt
  M_reg = M_quake \ S_sing
  ```

* When an experiment attempts to evaluate `DeltaS_pred(m)` for `m` in `S_sing`, the result is treated as “out of domain” and not as evidence for or against predictability.

---

## 4. Tension principle for this problem

### 4.1 Core tension statement

At the effective layer, Q096 is encoded as a statement about the predictability_tension scalar:

```txt
Tension_EQ(m) = alpha * DeltaS_pred(m)
```

for world-representing states `m` in `M_reg`.

Intuitively:

* If the real Earth is strongly predictable at the tested scales, there should exist encodings and model libraries such that `DeltaS_pred(m)` is small and remains small as test sets are extended.
* If the Earth is only weakly predictable, or nearly unpredictable, then even the best model libraries will leave `DeltaS_pred(m)` significantly larger than zero across large parts of the region-horizon space.

### 4.2 Low-tension principle (predictable world)

We define an effective low-tension principle:

> In a predictability-friendly world, there exist encodings of seismic regime states and forecast libraries for which:
>
> * the best models consistently achieve target gains over trivial references,
> * these gains remain stable or improve as tests are extended,
> * and the overall predictability mismatch `DeltaS_pred(m)` can be kept within a narrow band across operationally relevant scales.

Formally, for world-representing states `m_T`:

```txt
DeltaS_pred(m_T) <= epsilon_EQ
```

for some small `epsilon_EQ` that does not grow uncontrollably as more data are collected or as tests are repeated.

### 4.3 High-tension principle (weakly predictable world)

We define the complementary high-tension scenario:

> In a weakly predictable world, no matter how the forecast library and scoring rules are refined under reasonable constraints, there remains a strictly positive gap between achievable performance and target gains.

Formally, for world-representing states `m_F`:

```txt
DeltaS_pred(m_F) >= delta_EQ
```

for some `delta_EQ > 0` that cannot be driven arbitrarily close to zero without violating constraints such as:

* fixed, finite model and score libraries,
* prospective evaluation protocols,
* and stable benchmarks.

Under this principle, Q096 is the statement that our universe lies closer to the low-tension regime than to the high-tension regime for the scales and regions of interest, or that the boundary between these regimes can be sharply characterized.

---

## 5. Counterfactual tension worlds

We outline two counterfactual worlds, described only through observables and invariants.

### 5.1 World T (moderate-to-strong predictability)

In World T:

1. Forecast libraries contain models that consistently outperform trivial references over a broad range of regions and horizons.

2. The gain observable satisfies:

   ```txt
   Gain(m_T; S_j) >= Target_gain_j - small_margin
   ```

   for all scoring rules in the library and for most operational contexts.

3. The mismatch scalar `DeltaS_pred(m_T)` remains below `epsilon_EQ` and does not grow as test windows are extended, except within a controlled fluctuation band.

4. New data generally confirm the earlier view of moderate-to-strong predictability; recalibrations refine models but do not destroy their comparative advantage.

### 5.2 World F (persistent weak predictability)

In World F:

1. No model in the library can maintain a significant performance advantage over the trivial reference model across extended tests.
2. The gain observable satisfies:

   ```txt
   Gain(m_F; S_j) <= Target_gain_j - gap_j
   ```

   for some strictly positive `gap_j` for many scoring rules and contexts.
3. The mismatch scalar `DeltaS_pred(m_F)` stays above `delta_EQ`, even after library revision and recalibration, as long as constraints remain realistic.
4. Attempts to construct more complex models lead to overfitting: performance gains in one time window are lost or reversed in future windows.

### 5.3 Interpretive note

These worlds do not assert anything about the deep physics of faults or stress. They only describe how the observable performance of coherent forecast libraries would behave in the long run. Q096 uses these worlds as reference frames for stating what it would mean for earthquake predictability to be structurally present or structurally absent at the tested scales.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments that can test the coherence and usefulness of the Q096 encoding, without claiming to solve the canonical problem itself.

### Experiment 1: Prospective CSEP-style test as a TU encoding probe

*Goal:*
Evaluate whether the Q096 predictability_tension encoding aligns with actual performance of earthquake forecast models in prospective testing.

*Setup:*

* Select one or more CSEP-style regions (for example, California or Italy), with predefined spatial grids, magnitude thresholds, and time windows.
* Fix a finite model library `L_eq_model` including both simple and advanced models.
* Fix a scoring library `L_eq_score` that includes at least one strictly proper scoring rule for count forecasts.

*Protocol:*

1. For each test window, submit forecasts from all models in `L_eq_model` according to the specified format.
2. After the window closes, record observed counts and compute scores `Perf(m; M_l, S_j)` for each model and rule.
3. Update `Gain(m; S_j)` and `DeltaS_pred(m)` for the cumulative test set.
4. Track the evolution of `DeltaS_pred(m)` and `E_pred(m)` as the number of windows grows.

*Metrics:*

* Time series of `Gain(m; S_j)` for each scoring rule.
* Time series of `DeltaS_pred(m)` as a scalar indicator of predictability_tension.
* Contrast invariant `I_contrast(m)` to measure diversity and separation among models.

*Falsification conditions:*

* If, across multiple regions and time scales, `DeltaS_pred(m)` stays large or grows despite reasonable library revisions, the current encoding of predictability_tension is considered falsified or incomplete at the effective layer.
* If trivial modifications of scoring definitions or model weighting can arbitrarily reduce `DeltaS_pred(m)` without any corresponding improvement in prospective performance, the encoding is judged structurally unstable and rejected.

*Semantics implementation note:*
All forecasts, counts, and scores are treated in a hybrid way: underlying physical fields are continuous in space and time, but forecast and observation observables are discrete summaries over fixed grid cells and windows.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can disprove a particular encoding of predictability_tension, but it does not prove or disprove the existence of deeper physical predictability.

---

### Experiment 2: Stress test under major sequence or swarm

*Goal:*
Test whether Q096’s predictability_tension encoding can detect and characterize changes in forecast skill during a major earthquake sequence or swarm.

*Setup:*

* Choose one region where a large mainshock and aftershock sequence, or a prolonged swarm, has occurred within the available catalog.

* Construct two sets of test windows:

  * Pre-sequence windows (background regime),
  * Sequence windows (high-activity regime).

* Use the same model and scoring libraries as in Experiment 1.

*Protocol:*

1. For pre-sequence windows, compute `Gain(m; S_j)` and `DeltaS_pred(m_pre)`.
2. For sequence windows, compute the same quantities, now reflecting performance under extreme clustering.
3. Compare the behavior of `DeltaS_pred` and `I_contrast` between the two regimes.
4. Optionally, include post-sequence windows to examine relaxation behavior.

*Metrics:*

* Differences in `DeltaS_pred` between pre-sequence, sequence, and post-sequence regimes.
* Changes in model ranking and performance contrast `I_contrast`.
* Stability of models that explicitly incorporate clustering versus models that do not.

*Falsification conditions:*

* If the encoding fails to register any significant change in predictability_tension between background and sequence regimes, even when performance differences are visibly large under standard seismological metrics, the encoding is considered misaligned.
* If the encoding can be tuned post hoc to erase any tension signal from known difficult regimes without corresponding gains in forecast reliability, it is judged structurally uninformative.

*Semantics implementation note:*
Counts and scores are again treated as discrete summaries, while the underlying stress evolution and clustering processes are interpreted as continuous fields whose detailed representation is external to this block.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment probes whether the Q096 encoding responds meaningfully to known difficult regimes; it does not determine whether earthquakes are fundamentally predictable.

---

## 7. AI and WFGY engineering spec

This block describes how Q096 can be used as an engineering module inside AI systems within the WFGY framework.

### 7.1 Training signals

We define several training signals derived from Q096 observables.

1. `signal_hazard_calibration`

   * Definition: a penalty proportional to miscalibration of forecast probabilities relative to observed counts in seismic contexts.
   * Source: derived from scoring rule gaps between forecasts implied by model internal states and observed seismicity summaries.

2. `signal_predictability_envelope`

   * Definition: a scalar derived from `DeltaS_pred(m)` representing distance from a low-tension predictability envelope.
   * Purpose: encourage AI systems to represent hazard in ways consistent with known limits of predictability rather than overconfident narratives.

3. `signal_model_diversity`

   * Definition: a signal based on `I_contrast(m)`, rewarding internal representations that support genuinely diverse model hypotheses where justified by data.
   * Purpose: prevent premature collapse onto a single, untested forecast narrative.

4. `signal_warning_coherence`

   * Definition: compares the AI’s suggested risk communication against the encoded predictability envelope; penalizes statements that imply deterministic certainty where only weak probabilistic signals exist.

### 7.2 Architectural patterns

We outline module patterns that reuse Q096 components.

1. `EQ_PredictabilityHead`

   * Role: given internal representations of seismic context, outputs estimates of `DeltaS_pred` and related invariants as auxiliary channels.
   * Interface: input is a task embedding for a seismic decision context; outputs are scalar or low-dimensional tension metrics.

2. `MultiScaleHazardEncoder_EQ`

   * Role: builds compressed descriptors of hazard fields over multiple scales in space and time, consistent with Q096’s region-horizon libraries.
   * Interface: inputs are raw or summarized hazard maps; outputs are low-dimensional embeddings that feed into forecast or decision modules.

3. `ForecastLibraryController_EQ`

   * Role: manages a finite internal library of forecast “modes” or hypotheses, mirroring `L_eq_model`, and tracks their relative performance over time.

### 7.3 Evaluation harness

We propose an evaluation harness for AI systems augmented with Q096 modules.

1. Task selection

   * Combine question sets on earthquake science, risk communication, and emergency planning.
   * Include both technical questions (about forecast models and tests) and layperson questions (about “prediction”).

2. Conditions

   * Baseline: AI system without explicit Q096 modules, answering questions directly from general training.
   * TU-augmented: AI system using EQ_PredictabilityHead and MultiScaleHazardEncoder_EQ as auxiliary components and signals.

3. Metrics

   * Factual accuracy on technical questions about forecast limits and testing frameworks.
   * Calibration of verbal risk statements against known forecast uncertainties.
   * Consistency across scenarios: whether the system maintains the same predictability envelope in different framings of the same hazard.

### 7.4 60-second reproduction protocol

A minimal interactive protocol for external users.

* Baseline setup

  * Prompt: ask the AI “Can we predict earthquakes?” and follow-up questions about short-term and long-term forecasts.
  * Observation: record whether the system confuses deterministic prediction with probabilistic forecasting or overstates predictability.

* TU-encoded setup

  * Prompt: same questions, but instruct the AI to reason using:

    * a finite library of forecast models,
    * explicit performance tests over time,
    * and a predictability_tension envelope as in Q096.

  * Observation: record whether the system now clearly distinguishes:

    * what can be forecast probabilistically,
    * what cannot,
    * and how tests such as CSEP fit into the picture.

* Comparison metric

  * Use a rubric scoring clarity, calibration, and explicit reference to testing frameworks.
  * Optionally, ask domain experts to compare baseline and TU-encoded answers blind.

* What to log

  * Prompts, responses, any internal tension metrics from Q096 modules, and simple metadata about which model-library patterns were invoked.

---

## 8. Cross problem transfer template

### 8.1 Reusable components produced by this problem

1. ComponentName: `PredictabilityEnvelope_EQ`

   * Type: functional

   * Minimal interface:

     * Inputs: forecast model library summaries, scoring results, reference benchmarks.
     * Output: scalar and vector indicators of predictability_tension (for example `DeltaS_pred`, `E_pred`).

   * Preconditions:

     * Inputs must correspond to a coherent set of prospective or retrospective forecast tests over defined region-horizon pairs.

2. ComponentName: `HazardField_MultiScale_Descriptor_EQ`

   * Type: field

   * Minimal interface:

     * Inputs: region-horizon grids, long-term hazard estimates, and time-varying rate fields.
     * Output: compressed descriptors of multi-scale seismic hazard suitable for reuse in other hazard problems.

   * Preconditions:

     * The grids and rates must be defined according to a fixed partition and magnitude threshold scheme.

3. ComponentName: `ProspectiveForecast_Experiment_Template_EQ`

   * Type: experiment_pattern

   * Minimal interface:

     * Inputs: region specification, model library, scoring library, test schedule.
     * Output: an experiment design including forecast submission rules, evaluation steps, and tension observables.

   * Preconditions:

     * The experiment must be feasible with existing catalog and computational resources.

### 8.2 Direct reuse targets

1. Q095 (Compound extremes and multi-hazard corridors)

   * Reused component: `HazardField_MultiScale_Descriptor_EQ`.
   * Why it transfers: compound events often involve interactions between seismic hazard and other hazards; Q095 needs multi-scale hazard descriptors as building blocks for multi-hazard corridors.
   * What changes: the descriptor is combined with equivalent descriptors for other hazards (for example flood, heat, wildfire) to form joint state representations.

2. Q094 (Hurricane pattern shifts and landfall risk)

   * Reused component: `PredictabilityEnvelope_EQ` as a template.
   * Why it transfers: both problems address predictability versus uncertainty for high-impact events, with tension between model skill and societal expectations.
   * What changes: forecast models become hurricane models, and region-horizon grids are adapted to basins and seasons instead of fault zones.

3. Q097 (Gigafire regimes)

   * Reused component: `ProspectiveForecast_Experiment_Template_EQ`.
   * Why it transfers: the same pattern of prospective testing, fixed model libraries, and scoring rules can be applied to wildfire spread and ignition forecasts.
   * What changes: observables track fire counts, burned area, and intensity statistics instead of earthquake counts and magnitudes.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E1

  * The Q096 encoding specifies state spaces, observables, a predictability mismatch scalar, and a tension functional.
  * It includes concrete experiment templates but does not yet require full implementation details or large-scale deployments.

* N_level: N1

  * The narrative describes how seismic forecast performance relates to predictability_tension, with explicit reference to forecast libraries and test regimes.
  * Counterfactual worlds and transfer patterns are sketched but not yet fully instantiated across all BlackHole nodes.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following should be realized:

1. Implement a working prototype that ingests published CSEP or OEF-style forecast and observation data, computes `DeltaS_pred(m)` and related invariants, and publishes tension profiles as open data.
2. Deploy a pilot AI system that uses Q096-derived signals to improve calibration and communication of earthquake risk compared to a baseline system, with evaluation on realistic user tasks.

Both steps remain at the effective layer, operating on published summaries and forecast archives rather than exposing any deeper TU construction rules.

### 9.3 Long-term role in the TU program

Over the longer term, Q096 is intended to:

* anchor all geohazard predictability questions as instances of predictability_tension on multi-scale hazard fields,
* provide a common language for comparing forecast skill and limitations across hazards,
* and serve as a testbed for AI systems that must reason responsibly about rare but devastating events.

Success would mean that for any serious debate about “whether earthquakes can be predicted,” there exists a clear, observable-based framing in terms of Q096’s invariants and experiments.

---

## 10. Elementary but precise explanation

This block gives an explanation for non-experts, while staying consistent with the effective-layer encoding.

People often ask, “Can we predict earthquakes?” The honest scientific answer is subtle:

* We cannot say exactly when and where a big earthquake will strike, the way we might predict a solar eclipse.
* But we can say that some places are much more likely to have earthquakes than others, and that after a big event, more earthquakes are likely nearby for some time.

Modern seismology treats this as a question about **forecasting** rather than **fortune-telling**. Instead of saying “There will be a magnitude 7 event here tomorrow,” scientists build models that say things like:

* “In this region, over the next year, the chance of a damaging earthquake is about X percent.”

Q096 takes this practical viewpoint and asks:

* How much better than a very simple model can we do?
* Do our best models really beat a “background only” model in repeated tests?
* When we think we have found patterns, do they hold up when tested prospectively?

In the Tension Universe picture, we imagine a space of “world states” where each state summarizes:

* what our forecast models say,
* what actually happened in past windows,
* and how we score the models.

From these, we build a number called `DeltaS_pred`, which measures how far we are from a world where earthquakes are clearly predictable at the tested scales. If this number can be kept small and stable across tests, the world looks predictability-friendly. If the number stays large, even after many experiments, the world looks stubbornly unpredictable.

This does not prove any deep theorem about faults. It does something more practical:

* It forces us to write down what we mean by “predictable” in terms that can be tested.
* It forces us to compare models fairly, without changing the rules after seeing the data.
* It gives us a way to carry lessons about predictability from earthquakes to other hazards, and into AI systems that talk to the public.

Q096 is therefore not a magic prediction scheme. It is a rigorous way to talk about what prediction could mean, how far we have come, and how far we might still be from the limits of what is physically and statistically possible for earthquakes.
