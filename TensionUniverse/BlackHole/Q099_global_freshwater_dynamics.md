# Q099 · Global freshwater dynamics under climate change

## 0. Header metadata

```txt
ID: Q099
Code: BH_EARTH_WATER_BALANCE_L3_099
Domain: Earth system science
Family: Hydrology and freshwater resources
Rank: S
Projection_dominance: M
Field_type: dynamical_field
Tension_type: thermodynamic_tension
Status: Reframed_only
Semantics: continuous
E_level: E1
N_level: N1
Last_updated: 2026-01-26
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical problem behind Q099 can be phrased as:

> Understand and quantify the long-term global balance of freshwater availability, variability, and use under anthropogenic climate change, in a way that links physical water-cycle dynamics, human withdrawals, ecological needs, and risk of large-scale scarcity or flood crises.

Operationally, this involves at least four coupled questions:

1. How do precipitation, evapotranspiration, runoff, and storage components of the water cycle respond to different warming levels and circulation patterns?
2. How do these physical changes translate into renewable freshwater availability at river-basin and aquifer scales that matter for societies and ecosystems?
3. How do human withdrawals, infrastructure, and land-use changes feed back into these dynamics, altering availability, variability, and extremes?
4. Under what conditions does the global freshwater system cross thresholds into persistent deficit, regional collapse, or cascading crises?

This is not a single theorem but a coupled set of dynamical, statistical, and socio-hydrological questions that must be kept conceptually coherent.

### 1.2 Status and difficulty

Key aspects are well studied but far from closed:

* Global water-cycle intensification under warming is supported by climate-model ensembles and observations, but regional projections remain uncertain, especially for extremes.
* Basin-scale water budgets can be estimated from observations and reanalyses, yet closure errors, data gaps, and model structural uncertainties are substantial.
* Groundwater depletion, reservoir operations, and land-use changes are known to alter runoff and storage, but large-scale feedbacks are still poorly constrained.
* Planetary-boundary frameworks for freshwater use exist, but robust quantitative thresholds and attribution of transgressions remain debated.

The difficulty arises from:

* Strong coupling between atmosphere, land, oceans, cryosphere, biosphere, and human systems.
* Multi-scale behavior in space and time, from local catchments to planetary aggregates and from daily extremes to century-scale trends.
* Deep uncertainty in future socio-economic pathways and adaptation responses.

Q099 is therefore treated as a reframed system-level problem, not as a classical open conjecture.

### 1.3 Role in the BlackHole project

Within the BlackHole S-problem collection, Q099:

1. Acts as the primary node for **global freshwater balance and stress** at the Earth system scale.
2. Connects the physical climate cluster (Q091–Q098) to socio-economic and risk clusters (Q100–Q110) through a single conserved quantity: usable freshwater.
3. Provides a reference template for encoding problems where:

   * a physically conserved quantity (water mass) is redistributed by dynamics,
   * human use changes boundary conditions and internal fluxes,
   * the main concern is long-horizon risk of deficit or excess rather than a single event.

### References

1. IPCC, “Climate Change 2021: The Physical Science Basis”, Working Group I contribution to the Sixth Assessment Report, chapters on the global water cycle.
2. IPCC, “Climate Change 2022: Impacts, Adaptation and Vulnerability”, Working Group II contribution, sections on water resources and regional freshwater risks.
3. United Nations World Water Assessment Programme, “The United Nations World Water Development Report”, recurring editions on global water resources and governance.
4. P. H. Gleick et al., review articles and assessments on global freshwater resources, water security, and climate change impacts in the peer-reviewed literature.

---

## 2. Position in the BlackHole graph

This block records how Q099 sits inside the BlackHole graph. All edges refer only to Q-IDs and give a one-line reason tied to concrete components or tension types.

### 2.1 Upstream problems

These problems provide foundations or tools that Q099 relies on at the effective layer.

* Q091
  Reason: Supplies the climate sensitivity and warming pathways that drive changes in global precipitation and evaporation fields used in the freshwater balance.

* Q092
  Reason: Encodes climate tipping points that can abruptly reorganize circulation patterns and thus freshwater distribution across basins.

* Q093
  Reason: Provides carbon-cycle feedback scenarios that determine the long-term temperature trajectories which Q099 must be conditioned on.

* Q094
  Reason: Describes ice-sheet and glacier mass loss that alters sea level, runoff timing, and the partition between solid and liquid freshwater.

* Q096
  Reason: Encodes monsoon stability and regional circulation regimes that control the seasonal timing and intensity of freshwater input in key basins.

### 2.2 Downstream problems

These problems directly reuse Q099 components or depend on its freshwater-tension structure.

* Q098
  Reason: Uses Q099 freshwater tension indices as input to the planetary-boundary assessment for the hydrological dimension of Earth system safety.

* Q100
  Reason: Reuses Q099 basin-level water stress and sanitation-related observables as drivers for water-borne and hygiene-related pandemic risks.

* Q103
  Reason: Incorporates Q099 freshwater constraints and variability as limiting factors in long-run global economic growth and capital deployment scenarios.

* Q109
  Reason: Uses Q099 regional freshwater scarcity and flood risk patterns as key drivers of long-term migration flows and displacement pressure.

### 2.3 Parallel problems

Parallel nodes share similar tension types or structural features but have no direct component dependence.

* Q095
  Reason: Both Q095 and Q099 track conserved quantities in the hydrosphere, with tension arising from imbalances between fluxes and storage.

* Q097
  Reason: Q097 focuses on extreme precipitation and flood events, while Q099 aggregates over longer timescales; both see risk_tail_tension in hydrological extremes.

* Q104
  Reason: Q104 studies wealth and income inequality; Q099 studies freshwater distribution inequality; both encode persistent imbalance across spatial units.

### 2.4 Cross-domain edges

Cross-domain edges link Q099 to problems in other domains that can reuse its components.

* Q104
  Reason: Reuses basin-level freshwater availability and stress indices as structural drivers of long-run inequality patterns across regions.

* Q105
  Reason: Uses Q099 freshwater drought and flood stress fields as inputs to models of systemic crashes in infrastructure and financial systems.

* Q108
  Reason: Treats Q099 freshwater scarcity maps as background fields that intensify political polarization around resource allocation and environmental policy.

* Q110
  Reason: Depends on Q099’s long-run freshwater dynamics to evaluate how institutions must evolve to manage shared water resources and transboundary basins.

---

## 3. Tension Universe encoding (effective layer)

All content in this block stays at the effective layer. We describe only:

* state spaces,
* fields and observables,
* invariants and tension scores,
* singular sets and domain restrictions.

No hidden generative rule or mapping from raw data to internal TU fields is specified.

### 3.1 State space

We postulate a continuous-field state space

`M`

with the following interpretation:

* Each element `m` in `M` represents a coherent configuration of the global freshwater system over a chosen time window and spatial tiling.
* For a fixed temporal resolution `Delta_t` and a finite set of spatial units `B = {B_1, ..., B_K}` (for example, river basins or grid cells), a state `m` encodes, for each unit `B_k`:

  * mean precipitation `P_k`,
  * evapotranspiration `E_k`,
  * surface and subsurface runoff `R_k`,
  * change in water storage `dS_k`,
  * human withdrawals `W_k`,
  * a small number of ancillary indicators such as groundwater depletion and environmental-flow requirements.

We assume:

* The tiling `B` comes from a finite library of pre-specified basin or grid definitions agreed upon before analysis.
* The time window and `Delta_t` are chosen from a finite set of resolutions (for example annual, seasonal, decadal) fixed in advance.
* For each `m`, all encoded quantities for the chosen tiling and time window are finite real numbers.

No assumption is made here about how these quantities are estimated from observations or models.

### 3.2 Effective fields and observables

We define the following observables on `M`:

1. Basin-level water balance residual

```txt
res_k(m) = P_k(m) - E_k(m) - R_k(m) - dS_k(m)
```

* Interpretation: `res_k(m)` measures the degree to which the encoded physical water budget closes in basin `B_k` over the chosen time window, excluding human withdrawals.

2. Renewable freshwater supply

```txt
S_renew_k(m) = max(0, R_k(m) + dS_k(m)_pos)
```

where `dS_k(m)_pos` denotes the positive part of storage change (gain).

* Interpretation: `S_renew_k` is an effective measure of the renewable freshwater made available to human and ecosystem use in basin `B_k`.

3. Human and ecological demand

```txt
D_total_k(m) = W_k(m) + E_env_k(m)
```

* `W_k(m)` is encoded human use (agriculture, industry, domestic).
* `E_env_k(m)` is an encoded environmental-flow requirement needed to maintain ecosystems.

4. Basin stress ratio

```txt
ratio_k(m) = D_total_k(m) / (S_renew_k(m) + epsilon_ref)
```

where `epsilon_ref` is a small positive reference constant to avoid division by zero, chosen from a fixed admissible set and not tuned to individual basins.

* Interpretation: `ratio_k(m)` summarizes how strongly demand presses against renewable supply in basin `B_k`.

5. Global freshwater stress index

For a chosen finite set of basins `B_study` we define:

```txt
Index_stress(m) = average over k in B_study of f_ratio(ratio_k(m))
```

where `f_ratio` is a nondecreasing function fixed before analysis (for example truncated linear or logistic) and the average is a simple arithmetic mean or a pre-declared population-weighted mean.

### 3.3 Mismatch observables and tension components

We construct three mismatch observables:

1. Budget mismatch

```txt
DeltaS_balance(m) = average over k in B_study of |res_k(m)|
```

This measures the degree to which the encoded physical budgets fail to close.

2. Supply-demand mismatch

```txt
DeltaS_demand(m) = average over k in B_study of max(0, ratio_k(m) - 1)
```

This captures how often and how strongly basins operate in effective deficit (demand exceeding renewable supply).

3. Risk-tail mismatch

For each basin we encode a tail indicator `T_extreme_k(m)` that summarizes the probability or frequency of severe droughts or floods over the time window under the encoded climate scenario.

We then define:

```txt
DeltaS_risk(m) = average over k in B_study of T_extreme_k(m)
```

where each `T_extreme_k(m)` is already scaled into a nonnegative risk score by agreed-upon rules before analysis.

### 3.4 Combined freshwater tension and tensor

We define a combined freshwater tension functional:

```txt
Tension_FW(m) = w_balance * DeltaS_balance(m)
               + w_demand * DeltaS_demand(m)
               + w_risk   * DeltaS_risk(m)
```

with:

* `w_balance`, `w_demand`, `w_risk` all nonnegative, not all zero,
* `w_balance + w_demand + w_risk = 1`,
* the triple `(w_balance, w_demand, w_risk)` chosen from a small admissible library fixed before any data-specific analysis.

At the tensor level, we use the TU core pattern:

```txt
T_ij(m) = S_i(m) * C_j(m) * Tension_FW(m) * lambda(m) * kappa
```

where:

* `S_i(m)` describes the strength of freshwater-related source components (for example agriculture, urban systems, ecosystems).
* `C_j(m)` describes the sensitivity of different receptors (for example regional economies, ecosystems, social systems) to freshwater tension.
* `lambda(m)` is a convergence-state factor from the TU core.
* `kappa` is a fixed coupling constant for the freshwater sector.

Precise indexing sets are not needed at the effective layer; it suffices that `T_ij(m)` is finite for all relevant `i`, `j`.

### 3.5 Singular set and domain restrictions

We define a singular set:

```txt
S_sing = { m in M :
           any encoded P_k, E_k, R_k, dS_k, W_k is undefined or not finite
           or DeltaS_balance(m), DeltaS_demand(m), DeltaS_risk(m)
              cannot be computed as finite real numbers }
```

and restrict analysis to the regular domain:

```txt
M_reg = M \ S_sing
```

Rules:

* All freshwater tension evaluations are carried out only on `M_reg`.
* If, during an experiment, an attempted evaluation of `Tension_FW(m)` lands in `S_sing`, the result is treated as “out of domain” rather than as evidence about the real world.
* Any encoding that routinely produces large portions of `M` inside `S_sing` is considered ill-posed for Q099 at the effective layer.

---

## 4. Tension principle for this problem

This block states how Q099 is characterized as a tension problem within TU, without asserting a single theorem.

### 4.1 Core freshwater tension principle

The core principle is:

> A globally sustainable freshwater regime corresponds to configurations `m` in `M_reg` where physical budgets are approximately closed, demand rarely and weakly exceeds renewable supply, and risk tails for drought and flood are contained within agreed safety bands.

Formally, for a given choice of admissible tilings, time windows, and weights, there should exist world-relevant configurations `m_safe` such that:

```txt
DeltaS_balance(m_safe)  <= epsilon_balance
DeltaS_demand(m_safe)   <= epsilon_demand
DeltaS_risk(m_safe)     <= epsilon_risk
Tension_FW(m_safe)      <= epsilon_FW
```

for small threshold values `epsilon_balance`, `epsilon_demand`, `epsilon_risk`, `epsilon_FW` that depend on resolution but do not grow without bound as data improve.

### 4.2 High-tension freshwater world

A high-tension freshwater regime is one where, for world-relevant configurations `m_stress`, at least one of the following holds persistently across refinements:

```txt
DeltaS_balance(m_stress)  >= delta_balance
DeltaS_demand(m_stress)   >= delta_demand
DeltaS_risk(m_stress)     >= delta_risk
Tension_FW(m_stress)      >= delta_FW
```

with strictly positive thresholds `delta_balance`, `delta_demand`, `delta_risk`, `delta_FW` that cannot be made small without contradicting the encoded physical and socio-economic information.

### 4.3 Q099 as a classification statement

Q099, at the effective layer, does not claim that the world is provably in either regime. Instead it encodes:

* a structured way to classify world-relevant configurations `m` into lower and higher freshwater tension bands,
* a requirement that any long-term scenario for climate and society be accompanied by an explicit `Tension_FW` assessment,
* a demand that any claim about sustainable or unsafe freshwater futures be expressible as inequalities in terms of `DeltaS_balance`, `DeltaS_demand`, and `DeltaS_risk`.

The tension principle is thus a classification and consistency framework, not a theorem.

---

## 5. Counterfactual tension worlds

We define two counterfactual worlds, described only through observable patterns.

### 5.1 World T (sustainable freshwater regime)

In World T:

1. Physical closure

   * For world-representing `m_T` and realistic resolutions, `DeltaS_balance(m_T)` stays within small bands consistent with current and future observational and modeling capabilities.

2. Demand versus supply

   * The basin stress ratios `ratio_k(m_T)` exceed 1 only rarely and modestly, so that `DeltaS_demand(m_T)` remains low across most basins and time windows.

3. Risk tails

   * The tail indicators `T_extreme_k(m_T)` reflect droughts and floods, but their aggregated effect `DeltaS_risk(m_T)` stays within bands agreed as acceptable for ecosystem and societal adaptation.

4. Global freshwater tension

   * The combined tension `Tension_FW(m_T)` stays in a stable low band in scenarios consistent with deliberate mitigation and adaptation efforts.

### 5.2 World F (runaway freshwater stress regime)

In World F:

1. Persistent budget discrepancy

   * World-representing `m_F` exhibit large `DeltaS_balance(m_F)` due to structural mismatches between precipitation, evapotranspiration, runoff, and storage changes under high warming and land-use change.

2. Chronic deficits

   * For many basins, `ratio_k(m_F)` is significantly greater than 1 over extended periods, pushing `DeltaS_demand(m_F)` to high levels and indicating chronic overuse.

3. Amplified risk tails

   * `T_extreme_k(m_F)` is high for multiple key basins, with `DeltaS_risk(m_F)` indicating frequent and severe droughts and floods beyond historical norms.

4. High global freshwater tension

   * `Tension_FW(m_F)` exceeds any reasonable low-tension band across most plausible socio-economic pathways, signaling a structurally stressed freshwater world.

### 5.3 Interpretive note

These worlds do not depend on how the configurations are generated or simulated. They describe only how observable freshwater quantities and risks would behave if the world were in a sustainable or runaway regime under the Q099 encoding.

---

## 6. Falsifiability and discriminating experiments

We specify experiments that can falsify specific Q099 encodings, without claiming to fully solve the underlying Earth system problem.

### Experiment 1: Basin-level budget closure under climate projections

*Goal:*
Test whether a chosen Q099 encoding yields physically consistent basin-level budgets under existing climate projections and observations.

*Setup:*

* Select a finite set of basins `B_study` that cover a broad range of climates and socio-economic conditions.
* Fix time windows (for example, recent decades and mid-century projections) and the temporal resolution `Delta_t`.
* Use published climate-model ensembles and observation-based products to construct states `m_hist` and `m_proj` in `M_reg` for each basin, encoding `P_k`, `E_k`, `R_k`, `dS_k`, and `W_k`.

*Protocol:*

1. For each basin and time window, compute `res_k(m)` and `DeltaS_balance(m)` according to the Q099 definitions.
2. Compare `res_k(m)` against known constraints on water-budget closure from hydrological literature.
3. Aggregate results into `DeltaS_balance(m_hist)` and `DeltaS_balance(m_proj)` for each scenario.

*Metrics:*

* Distribution of `res_k(m)` across basins and time windows.
* Values of `DeltaS_balance(m_hist)` and `DeltaS_balance(m_proj)` under different climate scenarios.
* Sensitivity of these metrics to small perturbations in the encoding choices allowed by the admissible library.

*Falsification conditions:*

* If `DeltaS_balance(m_hist)` is systematically large across basins, far beyond known observational and modeling closure errors, the encoding is considered physically inconsistent and rejected.
* If `DeltaS_balance(m_proj)` varies wildly and non-smoothly under small, justified changes in input climate fields, the encoding is considered numerically unstable and rejected.

*Semantics implementation note:*
All quantities in this experiment are treated as continuous fields aggregated over basins and time windows, represented as real numbers consistent with the metadata field type.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject specific freshwater tension encodings, but it does not by itself determine which future freshwater regime the real world will enter.

---

### Experiment 2: Coupled human–freshwater stress scenarios

*Goal:*
Assess whether the Q099 encoding can robustly distinguish low-tension and high-tension socio-hydrological futures under different socio-economic and adaptation scenarios.

*Setup:*

* Select a set of global scenario families combining climate pathways and socio-economic narratives.
* For each scenario family, construct states `m_scenario` in `M_reg` for a target period (for example, late-century), encoding `P_k`, `E_k`, `R_k`, `dS_k`, `W_k`, and `E_env_k` for basins in `B_study`.
* Fix a single choice of `(w_balance, w_demand, w_risk)` from the admissible library, applied uniformly across all scenarios.

*Protocol:*

1. For each scenario, compute `DeltaS_balance(m_scenario)`, `DeltaS_demand(m_scenario)`, `DeltaS_risk(m_scenario)`, and `Tension_FW(m_scenario)`.
2. Compare tension values across scenario families, noting which futures land in low-tension and high-tension bands.
3. Perform perturbation tests by slightly modifying demand projections or adaptation measures within plausible ranges and recomputing tension metrics.

*Metrics:*

* Range of `Tension_FW(m_scenario)` across scenario families.
* Share of basins in chronic deficit mode (with `ratio_k > 1` for extended periods).
* Sensitivity of classification (low-tension vs high-tension) to small scenario perturbations.

*Falsification conditions:*

* If the encoding assigns similar low tension to obviously different futures (for example, aggressive mitigation and adaptation vs unmitigated high-emission, no-adaptation pathways), the encoding is considered non-discriminating and rejected.
* If modest changes in scenario assumptions flip a future from low tension to high tension without clear structural reason, the encoding is considered too fragile and rejected as a classification tool.

*Semantics implementation note:*
All scenario quantities are treated as continuous fields aggregated over basins and time windows; discrete socio-economic narratives are only used to select which continuous fields to encode, not to alter the mathematical form of the tension functional.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can show that a particular tension encoding is unhelpful or misleading, but it does not remove uncertainty about actual future socio-hydrological paths.

---

## 7. AI and WFGY engineering spec

This block describes how Q099 can be used as an engineering module in AI systems under the WFGY framework.

### 7.1 Training signals

1. `signal_water_budget_closure`

   * Definition: a penalty proportional to `DeltaS_balance(m)` for internally simulated or reasoned freshwater configurations.
   * Purpose: encourage internal states that respect basic physical water-budget closure where appropriate.

2. `signal_water_stress_ratio`

   * Definition: a signal derived from the distribution of `ratio_k(m)` across basins, with higher penalties for widespread or severe `ratio_k > 1`.
   * Purpose: align the model’s reasoning about water availability with stress-aware interpretations.

3. `signal_risk_tail_hydrology`

   * Definition: a signal based on `DeltaS_risk(m)` that increases when drought and flood risk tails become concentrated in vulnerable basins.
   * Purpose: push the model to pay attention to extreme-event structure, not just mean conditions.

4. `signal_scenario_separation`

   * Definition: a contrastive signal that rewards large margin in `Tension_FW(m_scenario)` between clearly low-stress and clearly high-stress scenario families.
   * Purpose: improve the model’s ability to distinguish genuinely safer futures from structurally risky ones.

### 7.2 Architectural patterns

1. `FreshwaterTensionHead`

   * Role: an auxiliary head that maps internal representations of Earth system and socio-economic state into an estimate of `Tension_FW(m)`.
   * Interface: input is a compact embedding of scenario or narrative; outputs are `Tension_FW` and partial components (`DeltaS_balance`, `DeltaS_demand`, `DeltaS_risk`).

2. `BasinStressObserver`

   * Role: a module that projects latent spatial information into basin-level summaries `ratio_k(m)` and `T_extreme_k(m)`.
   * Interface: input is a spatial latent field; output is a vector of basin-level metrics for stress and extremes.

3. `ScenarioComparator`

   * Role: a module that takes two scenario embeddings and produces comparative freshwater tension judgments (which is more stressed, and by how much).
   * Interface: inputs are two scenario encodings; outputs are a signed tension difference and an uncertainty estimate.

### 7.3 Evaluation harness

A minimal evaluation harness for AI systems using Q099 components:

1. Task types

   * Narrative-to-risk: given a textual description of a climate and development pathway, estimate freshwater stress at basin and global level.
   * Policy comparison: compare two adaptation or infrastructure strategies in terms of their impact on freshwater tension metrics.

2. Baselines

   * Baseline model: standard Earth system and policy reasoning with no explicit freshwater tension heads.
   * TU-augmented model: same backbone, augmented with Q099-based heads and training signals.

3. Metrics

   * Agreement with expert qualitative assessments of freshwater risks for well-studied scenarios.
   * Internal consistency: reduced contradictions in answers about water availability, stress, and extremes across related queries.
   * Sensitivity alignment: improved sensitivity to scenario changes known to affect water stress (for example irrigation expansion, reservoir construction).

### 7.4 60-second reproduction protocol

A quick protocol for external users to experience Q099-informed reasoning.

* Baseline setup

  * Prompt: ask the AI to compare two future climate scenarios in terms of water security, without mentioning any formal tension encoding.
  * Observation: note whether the explanation is vague, mixes different notions of risk, or neglects budget closure.

* TU-encoded setup

  * Prompt: ask the AI the same question, but request an answer structured around three ideas: physical water-budget closure, supply versus demand, and extreme-event risk, using a single scalar freshwater tension score to summarize each scenario.
  * Observation: check whether the explanation now explicitly references these three components and yields a coherent scalar comparison.

* Comparison metric

  * Simple rubric scoring structure, explicitness of trade-offs, and clarity of what drives differences in stress between scenarios.

* What to log

  * Full prompts, answers, and any exposed `Tension_FW` and component values, so that external reviewers can inspect whether the encoding is used in a disciplined way.

---

## 8. Cross problem transfer template

### 8.1 Reusable components produced by this problem

1. ComponentName: `FreshwaterTensionScore`

   * Type: functional

   * Minimal interface:

     * Inputs: basin-level summaries of `P_k`, `E_k`, `R_k`, `dS_k`, `W_k`, `E_env_k` over a time window.
     * Output: scalar `Tension_FW` and component values `DeltaS_balance`, `DeltaS_demand`, `DeltaS_risk`.

   * Preconditions: input summaries must be defined for a finite set of basins and consistent with the chosen tiling and time resolution.

2. ComponentName: `BasinWaterBudgetField`

   * Type: field

   * Minimal interface:

     * Inputs: climate and socio-economic scenario descriptors.
     * Output: fields `res_k`, `S_renew_k`, `D_total_k`, `ratio_k`, and `T_extreme_k` over `B_study`.

   * Preconditions: scenario descriptors must be rich enough to determine approximate freshwater variables at the resolution of interest.

3. ComponentName: `WaterStressRiskTail_Template`

   * Type: experiment_pattern

   * Minimal interface:

     * Inputs: a scenario family and a mapping from climate and socio-economic variables to freshwater summaries.
     * Output: an experiment specification with metrics based on `DeltaS_demand` and `DeltaS_risk`.

   * Preconditions: there must be a documented way to derive approximate freshwater stress indicators from the scenario inputs.

### 8.2 Direct reuse targets

1. Q098

   * Reused component: `FreshwaterTensionScore`.
   * Why it transfers: Q098 needs a scalar indicator of freshwater pressure on the Earth system to help define and monitor a planetary boundary.
   * What changes: the safe-band thresholds are reframed in planetary-boundary language, but the functional form is preserved.

2. Q103

   * Reused component: `BasinWaterBudgetField`.
   * Why it transfers: Q103 models growth slowdowns and constraints; freshwater availability and variability appear as direct constraints on productive capacity and infrastructure viability.
   * What changes: the outputs are fed into economic modules rather than risk modules.

3. Q100

   * Reused component: `WaterStressRiskTail_Template`.
   * Why it transfers: Q100 studies global pandemic risk; water-related sanitation stress and outage patterns are natural drivers in the experiment design.
   * What changes: the metrics emphasize connections to disease transmission, not general economic or ecological impacts.

4. Q109

   * Reused component: `BasinWaterBudgetField` and `WaterStressRiskTail_Template`.
   * Why it transfers: Q109 studies migration; persistent high freshwater tension becomes a core push factor shaping migration patterns.
   * What changes: the outputs are integrated into mobility and demographic modules.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E1

  * A clear effective-layer encoding for global freshwater tension has been specified.
  * Core observables, tension components, and a combined `Tension_FW` functional are defined with explicit domain restrictions.

* N_level: N1

  * A structured narrative linking physical budgets, supply-demand balance, and risk tails has been laid out.
  * Counterfactual worlds and scenario experiments are specified conceptually.

### 9.2 Next measurable step toward E2

To progress from E1 to E2, at least one of the following should be realized:

1. A prototype implementation that, for a chosen climate-model ensemble and socio-economic scenarios, computes `Tension_FW(m)` for a curated set of basins and publishes the resulting maps and time series.
2. A structured comparison between several plausible choices of `(w_balance, w_demand, w_risk)` and `f_ratio`, demonstrating which choices pass the falsification tests in Block 6 and which do not.

Both steps operate entirely at the effective layer: they work with observable or model-derived summaries and do not reveal any deeper TU generative rules.

### 9.3 Long-term role in the TU program

In the long term, Q099 is expected to:

* Anchor the freshwater dimension of Earth system tension assessments.
* Provide an example of how to integrate physical conservation laws, human use, and extreme-event risk into a single tension framework.
* Serve as a reusable module for broader systemic-risk analyses involving food, energy, health, migration, and political stability.

---

## 10. Elementary but precise explanation

At a simple level, Q099 asks:

> How much trouble are we in, globally, when it comes to water, once we account for climate change, our own withdrawals, and extreme events like droughts and floods?

The Tension Universe view breaks this into three pieces:

1. Does the physical water budget almost close when we add up rain, evaporation, river flow, and changes in stored water?
2. In each region that matters, do people and ecosystems want much more water than nature reliably supplies?
3. How often do we get very bad events, with too little water or too much water, compared to what we can cope with?

For each region, we can compute simple numbers that say:

* how big the budget error is,
* how big the gap is between demand and renewable supply,
* how strong the tail of dangerous events is.

We then average these in a careful way to get a single freshwater tension score for the world or for a group of regions.

In a low-tension freshwater world, budgets almost close, demand rarely exceeds supply by much, and extreme droughts and floods are serious but manageable. In a high-tension world, budgets look inconsistent, many regions live in chronic deficit, and extremes become common and damaging.

Q099 does not predict exactly what will happen or claim to know which world we will end up in. Instead, it gives a precise way to:

* turn complex data and scenarios into a few meaningful tension numbers,
* compare different futures in terms of how stressed the global freshwater system would be,
* connect freshwater stress to other big questions about safety, growth, health, and migration.
