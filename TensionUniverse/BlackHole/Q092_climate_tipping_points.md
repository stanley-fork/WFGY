# Q092 · Climate tipping points

## 0. Header metadata

```txt
ID: Q092
Code: BH_EARTH_TIPPING_L3_092
Domain: Earth system and climate
Family: tipping_dynamics
Rank: S
Projection_dominance: M
Field_type: dynamical_field
Tension_type: risk_tail_tension
Status: Partial
Semantics: continuous
E_level: E1
N_level: N1
Last_updated: 2026-01-25
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

A climate tipping point is a critical threshold in a subsystem of the Earth system such that:

* Once the subsystem crosses that threshold, its state is pushed toward a qualitatively different regime.
* The transition can be abrupt on human time scales, and it can be difficult or effectively irreversible on those scales.

Typical examples of tipping elements include:

* Major ice sheets (for example Greenland, West Antarctic).
* Large scale ocean circulation patterns (for example Atlantic Meridional Overturning Circulation, AMOC).
* Monsoon systems and large scale rainfall regimes.
* Large biomes such as the Amazon rainforest, boreal forests, or permafrost regions.

The canonical problem for Q092 is:

> To understand, at an effective and coarse grained level, when and how coupled climate subsystems approach and cross their tipping thresholds, and how local threshold crossings can cascade into large scale Earth system regime shifts.

This includes:

* Identifying key subsystems that behave as tipping elements.
* Characterizing their thresholds in terms of state variables and external forcing.
* Describing how couplings among these subsystems can create cascades of transitions.
* Quantifying how far the current and projected climate states are from such tipping and cascading regimes.

### 1.2 Status and difficulty

The basic concept of climate tipping points has strong support from theory, simple models, and paleoclimate evidence. However:

* Exact threshold values, timescales, and cascade patterns are highly uncertain.
* Different climate models and scenarios give different pictures of which elements are closest to tipping.
* The structure of interaction between tipping elements and human systems adds further complexity.

Key known points:

* Several subsystems, such as parts of the Greenland and West Antarctic ice sheets, appear to have threshold behavior in sea level contribution on multi century to multi millenium time scales under sustained warming.
* AMOC and other circulation patterns show signs that they may have multiple quasi stable regimes, with the possibility of partial or full collapse under certain forcing trajectories.
* Tropical and boreal ecosystems, as well as permafrost regions, can undergo rapid shifts in vegetation, fire regime, or carbon storage when key climatic thresholds are crossed.

Despite these advances, there is no single accepted theory that:

* Cleanly classifies all major tipping elements.
* Specifies their thresholds and mutual couplings in a unified framework.
* Quantifies systemic risk in a way that is both physically grounded and communicable to decision makers.

Q092 therefore remains a partially resolved and highly contested frontier problem.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q092 serves as:

1. The flagship example of a risk_tail_tension problem in the Earth system domain, where the focus is on rare but high impact regime shifts.
2. A bridge node between physical climate dynamics and socio technical systems that depend on climate stability.
3. A template for encoding:

   * finite libraries of tipping elements,
   * proximity to thresholds,
   * couplings that enable cascades,
   * and tail risk metrics for large scale regime shifts.

### References

1. IPCC, 2021, “Climate Change 2021: The Physical Science Basis”, Contribution of Working Group I to the Sixth Assessment Report of the Intergovernmental Panel on Climate Change, Cambridge University Press. (Chapters on climate system stability, abrupt change, and tipping elements.)
2. T. M. Lenton et al., 2008, “Tipping elements in the Earth’s climate system”, Proceedings of the National Academy of Sciences, 105(6), 1786–1793.
3. T. M. Lenton et al., 2019, “Climate tipping points too risky to bet against”, Nature, 575, 592–595.
4. V. Dakos et al., 2008, “Slowing down as an early warning signal for abrupt climate change”, Proceedings of the National Academy of Sciences, 105(38), 14308–14312.

---

## 2. Position in the BlackHole graph

This block records where Q092 sits among Q001 to Q125, with edges and one line reasons.

### 2.1 Upstream problems

These provide prerequisites or shared machinery for Q092.

* Q091 (BH_EARTH_ECS_L3_091)
  Reason: Supplies the background relation between radiative forcing and large scale temperature response used as the baseline field for tipping deviations.

* Q093 (BH_EARTH_CARBON_CYCLE_L3_093)
  Reason: Provides the long term carbon feedback structure that can push tipping elements toward or away from their thresholds.

* Q094 (BH_EARTH_OCEAN_MIXING_L3_094)
  Reason: Encodes deep ocean mixing and circulation as slow regulators of approach to tipping in ice sheets and AMOC.

### 2.2 Downstream problems

These reuse Q092 components or treat its outputs as preconditions.

* Q098 (BH_EARTH_ANTHROPOCENE_DYN_L3_098)
  Reason: Reuses the TippingElementLibrary and ClimateTensionFunctional_CTP to describe regime shifts in human Earth system co dynamics.

* Q099 (BH_EARTH_FRESHWATER_L3_099)
  Reason: Uses Q092 tipping states and cascades (for example ice melt, monsoon shifts) as structured drivers in freshwater availability regimes.

* Q100 (BH_EARTH_PANDEMIC_RISK_L3_100)
  Reason: Treats climate tipped states as exogenous shocks that alter ecological and disease regime basins, using Q092 tension outputs as inputs.

### 2.3 Parallel problems

Parallel nodes share similar tension type or structure but do not depend directly on Q092 components.

* Q105 (BH_SOC_SYSTEMIC_CRASH_L3_105)
  Reason: Both model risk_tail_tension in networks of coupled components with potential cascades and sudden regime shifts.

* Q106 (BH_SOC_MULTILAYER_ROBUSTNESS_L3_106)
  Reason: Both consider robustness and collapse in multilayer networks, with Q092 as the climate specific instance and Q106 as a more abstract network case.

### 2.4 Cross domain edges

Cross domain links reuse Q092 structures in other fields.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Can reuse the notion of tail transitions between regimes under external driving, framed as risk_tail_tension, though with microscopic physical observables.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Uses Q092 as an analogy where low probability high impact transitions in computational or information systems are framed with similar tail tension functionals.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* state space,
* fields and observables,
* invariants and tension functionals,
* singular sets and domain restrictions.

We do not describe how any internal TU fields are generated from raw data or climate models.

### 3.1 State space and finite element library

We fix a finite library of climate tipping elements:

```txt
E = {E_1, E_2, ..., E_k}
```

where each `E_i` is a named subsystem such as:

* `E_1` = Greenland ice sheet
* `E_2` = West Antarctic ice sheet
* `E_3` = AMOC like large scale circulation
* `E_4` = Amazon rainforest
* `E_5` = West African monsoon
* and so on, up to a fixed finite `k`.

We define a state space `M` whose elements `m` represent coarse grained climate regimes. For each `m` in `M`, the following effective information is encoded:

* For each tipping element `E_i`:

  * A real valued state variable `X_i(m)` representing a normalized anomaly or load (for example ice volume loss fraction, circulation strength index, biomass fraction).
  * A real valued index `theta_i(m)` representing proximity to a tipping threshold.

* A finite graph of couplings among tipping elements:

  * For each ordered pair `(i, j)` there is a coupling coefficient `C_ij(m)` that encodes effective influence of `E_i` on `E_j` for a fixed representation of interactions.
  * The adjacency and nonzero structure of `C_ij(m)` is fixed by the chosen encoding class and does not depend on the specific scenario outcome.

* External forcing descriptors:

  * A vector `F(m)` encoding global and regional forcing summaries, such as time averaged radiative forcing over a fixed horizon, or CO2 concentration profiles.

We do not specify how these effective quantities are computed from general circulation models, simplified models, or observations. We only assume that for each scenario under consideration there exist states `m` in `M` that encode consistent summaries.

### 3.2 Observables and fields

We define effective observables as follows.

1. Element state observable

```txt
X_i(m) in R
```

A normalized scalar that indicates the current state of element `E_i` in a dimensionless form.

2. Threshold proximity observable

We define for each element:

```txt
theta_i(m) = (X_i(m) - L_i) / (U_i - L_i)
```

where:

* `L_i` and `U_i` are fixed lower and upper bounds that define a threshold band for element `E_i`.
* `theta_i(m)` is interpreted as:

  * `theta_i(m) <= 0` means safely below threshold band,
  * `0 < theta_i(m) < 1` means inside a transition band,
  * `theta_i(m) >= 1` means beyond the tipping band for element `E_i`.

The bounds `L_i` and `U_i` are part of the encoding specification and do not change across scenarios once fixed.

3. Coupling field

```txt
C_ij(m) in R
```

A scalar that represents the net effect of state changes in `E_i` on the hazard for `E_j`. For the encoding class chosen here:

* The sign and sparsity pattern of `C_ij(m)` is fixed across all states in `M`.
* Only the magnitudes may vary mildly with scenario class, within bounded ranges set by the encoding specification.

4. Tail hazard observable

We fix a finite set of time horizons:

```txt
Tau = {tau_1, tau_2, ..., tau_L}
```

where each `tau_l` is a positive time scale (for example decades or centuries within a predefined upper limit).

For each `m` in `M` and horizon `tau_l` we define:

```txt
rho_tail(m; tau_l) >= 0
```

interpreted as an effective measure of the probability, rate, or intensity of crossing one or more tipping thresholds in the library `E` within time `tau_l` under the forcing profile encoded by `F(m)`.

We do not define the detailed probabilistic construction; we only require that:

* For each `tau_l` and admissible `m`, `rho_tail(m; tau_l)` is finite and well defined.
* The dependence on `m` is regular enough to allow numerical evaluation in implementations.

5. Combined tipping mismatch observable

We define a nonnegative scalar mismatch:

```txt
DeltaS_tip(m) = G(theta_1(m), ..., theta_k(m), C_ij(m), rho_tail(m; tau_l) for tau_l in Tau)
```

where `G` is a fixed function chosen once for the encoding class, satisfying:

* `DeltaS_tip(m) >= 0` for all `m` in the regular domain.
* `DeltaS_tip(m)` is small when all elements are far from threshold bands and tail hazard is small across all `tau_l`.
* `DeltaS_tip(m)` grows when more elements approach or cross their thresholds, couplings support cascades, and tail hazard increases.

The function `G` is part of the encoding specification and is not tuned per scenario.

### 3.3 Admissible encoding class and fairness constraints

To avoid arbitrary post hoc tuning, we define an admissible encoding class `A_enc` whose members are specified by:

* A fixed finite tipping element library `E`.
* Fixed threshold bands `[L_i, U_i]` for all `i`.
* A fixed adjacency structure for the coupling matrix, and fixed sign patterns for `C_ij`.
* A fixed finite horizon set `Tau`.
* A fixed functional form for `G` that maps observables into `DeltaS_tip`.
* Fixed ranges for weights and scale parameters appearing in `G`.

The fairness constraints are:

1. Once an encoding in `A_enc` is chosen for Q092, the above items are fixed for all scenarios and experiments.
2. The choice of `G`, `L_i`, `U_i`, adjacency of `C_ij`, and `Tau` cannot depend on the outcomes or goals of any particular scenario.
3. Any evaluation of `DeltaS_tip(m)` or derived invariants must use the same encoding specification across all compared cases.

This prevents artificial reduction of tension by changing thresholds or weights after observing results.

### 3.4 Effective tension tensor components

We define an effective semantic tension tensor over `M` consistent with the TU core:

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_tip(m) * lambda(m) * kappa
```

where:

* `S_i(m)` is a source like factor capturing how strongly the configuration activates different climate or decision relevant channels.
* `C_j(m)` is a receptivity like factor describing sensitivity of different downstream subsystems (such as ecological, economic, or social layers) to tipping related mismatch.
* `DeltaS_tip(m)` is the mismatch observable defined above.
* `lambda(m)` is a convergence state factor in a bounded interval, representing whether local reasoning about the state is convergent, recursive, divergent, or chaotic.
* `kappa` is a constant that sets the overall scale of climate tipping tension for this encoding.

The detailed index sets of `i` and `j` are not needed at the effective layer. It is sufficient that, for each `m` in the regular domain, `T_ij(m)` is finite and can be evaluated for all relevant indices.

### 3.5 Invariants

We define two invariants using only finite maxima over fixed index sets.

1. Proximity invariant

```txt
I_prox(m) = max over i in {1,...,k} of max(0, theta_i(m))
```

This measures the worst case normalized proximity to any tipping band. Values near zero indicate all elements are safely below their bands.

2. Tail risk invariant

Let `Tau` be as above. We define:

```txt
I_tail(m) = max over l in {1,...,L} of rho_tail(m; tau_l)
```

This measures the highest tail hazard across the finite set of considered time horizons.

These invariants are used to compare different states in `M` under the same encoding specification.

### 3.6 Singular set and domain restrictions

We define the singular set:

```txt
S_sing = { m in M :
           some theta_i(m) undefined,
           or some rho_tail(m; tau_l) undefined or infinite,
           or DeltaS_tip(m) undefined or infinite }
```

The regular domain is:

```txt
M_reg = M \ S_sing
```

All Q092 tension analysis is restricted to `M_reg`. If an experiment or protocol would attempt to use a state in `S_sing`, the outcome is treated as “out of domain” and not as evidence for or against a particular world type.

---

## 4. Tension principle for this problem

This block states how Q092 is framed as a tension problem at the effective layer.

### 4.1 Core tension functional

We define the climate tipping tension functional:

```txt
Tension_tip(m) = alpha * I_prox(m)
                 + beta * I_tail(m)
                 + gamma * CascadeIndex(m)
```

where:

* `alpha`, `beta`, `gamma` are fixed positive weights chosen once for the selected encoding in `A_enc`.
* `I_prox(m)` and `I_tail(m)` are invariants defined in Block 3.
* `CascadeIndex(m)` is a scalar function of the coupling matrix and proximities that captures the potential for cascades.

A simple example choice for `CascadeIndex` is:

```txt
CascadeIndex(m) = max over i,j of ( max(0, theta_i(m)) * max(0, C_ij(m)) )
```

under appropriate normalization of `C_ij(m)`. The only requirements are:

* `CascadeIndex(m) >= 0` for all `m` in `M_reg`.
* `CascadeIndex(m)` grows when strongly coupled elements are simultaneously near or beyond threshold bands.

The weights `alpha`, `beta`, and `gamma` are part of the encoding specification and are not tuned by scenario.

### 4.2 Low tension versus high tension regimes

At the effective layer, Q092 distinguishes between:

* Low tipping tension regimes where:

  ```txt
  Tension_tip(m) <= epsilon_tip
  ```

  for a moderate small threshold `epsilon_tip` set by the encoding, and

  * No element is near its threshold band.
  * Tail hazard is small across all horizons in `Tau`.
  * Cascade potential is limited.

* High tipping tension regimes where:

  ```txt
  Tension_tip(m) >= delta_tip
  ```

  for some strictly positive `delta_tip`, and

  * Several elements are near or beyond their bands.
  * Tail hazard is large for at least one `tau_l`.
  * Cascade potential is significant.

The core tension principle for Q092 can then be stated informally as:

> The current and projected climate states appear to be moving from low to higher tipping tension regimes in some scenarios, but the location and timing of transitions, as well as the possibility of cascades, remain highly uncertain.

The exact values of `epsilon_tip` and `delta_tip` are part of the encoding class and are chosen once for the problem.

### 4.3 Fairness and encoding stability

To guard against hidden parameter tuning, we impose:

* Once `alpha`, `beta`, `gamma`, `epsilon_tip`, `delta_tip`, and the definitions of `I_prox`, `I_tail`, and `CascadeIndex` are fixed, they are used for all experiments and scenarios in Q092.
* Any change to these choices constitutes a new encoding in `A_enc` and must be declared as such, not as a result of the same encoding.
* Comparative statements about low versus high tension regimes are only valid when all states are evaluated under the same encoding.

This ensures that changes in `Tension_tip(m)` reflect changes in climate states and forcing, not unannounced changes in the encoding itself.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds at the effective layer.

### 5.1 World T (low tipping tension world)

In World T:

1. Proximity pattern

   * For all world representing states `m_T` in `M_reg` that correspond to realistic near term scenarios:

     ```txt
     I_prox(m_T) is small
     ```

     meaning no major tipping element is close to its threshold band.

2. Tail hazard

   * For all `m_T` and for all `tau_l` in `Tau`:

     ```txt
     rho_tail(m_T; tau_l) is small and stable
     ```

     and decreasing trends in hazard may be possible if mitigation is strong.

3. Cascades

   * The cascade index `CascadeIndex(m_T)` remains low. Local threshold crossings, if they occur, stay relatively isolated and do not trigger large multi element cascades.

4. Global tension

   * For all relevant states `m_T`:

     ```txt
     Tension_tip(m_T) <= epsilon_tip
     ```

     with `epsilon_tip` as in Block 4, so the world remains in a low tension band.

### 5.2 World F (high tipping tension world)

In World F:

1. Proximity pattern

   * There exist world representing states `m_F` such that:

     ```txt
     I_prox(m_F) is moderate or large
     ```

     meaning several tipping elements are within or beyond their bands.

2. Tail hazard

   * For at least one `tau_l` in `Tau` and many states `m_F` consistent with observations and forcing scenarios:

     ```txt
     rho_tail(m_F; tau_l) is large
     ```

     and does not decrease as models are refined or new data are added.

3. Cascades

   * The cascade index `CascadeIndex(m_F)` is elevated, indicating that crossing one threshold significantly raises the hazard for others, making multi element cascades plausible.

4. Global tension

   * For some minimal resolution in the encoding, we have:

     ```txt
     Tension_tip(m_F) >= delta_tip
     ```

     where `delta_tip > 0` is the high tension threshold, and this cannot be made small without changing the encoding.

### 5.3 Interpretive note

These worlds do not describe how to generate internal TU fields from raw climate data. They only state that, if we construct effective states `m` that faithfully represent the world under certain assumptions, the resulting tension patterns would be qualitatively different between low and high tipping tension worlds.

---

## 6. Falsifiability and discriminating experiments

This block describes experiments and protocols that can falsify or support particular Q092 encodings at the effective layer. They do not solve climate dynamics, but they can rule out specific tension encodings or parameterizations.

### Experiment 1: Ensemble model tension profiling

*Goal:*
Test whether the chosen `Tension_tip` functional coherently reflects tipping risk across ensembles of Earth system model scenarios.

*Setup:*

* Select an ensemble of climate model simulations, for example from a coordinated model intercomparison project, covering a range of forcing scenarios up to a finite time horizon `T_max`.

* For each model run and scenario, define a state `m` in `M_reg` at one or more evaluation times, encoding:

  * Element states `X_i(m)` and their normalized indices `theta_i(m)`.
  * Coupling summaries `C_ij(m)` as defined by the encoding.
  * Tail hazard values `rho_tail(m; tau_l)` for `tau_l` in `Tau`, based on model transition statistics.

* Ensure all states are evaluated under the same encoding specification in `A_enc`.

*Protocol:*

1. For each state `m` from the ensemble, compute:

   * `I_prox(m)`,
   * `I_tail(m)`,
   * `CascadeIndex(m)`,
   * `Tension_tip(m)`.

2. Group states by scenario class (for example low, medium, high forcing) and by time slice.

3. For each group, compute summary statistics of `Tension_tip(m)` and the invariants.

4. Compare these summaries to prior expectations for low versus high climate risk scenarios.

*Metrics:*

* Mean and maximum `Tension_tip(m)` per scenario and time slice.
* Fraction of states in each group with `Tension_tip(m)` above `delta_tip`.
* Trends in tension statistics as forcing increases or mitigation is applied.

*Falsification conditions:*

* If low forcing scenarios repeatedly show `Tension_tip(m)` above `delta_tip` across most ensemble members, while high forcing scenarios show `Tension_tip(m)` mostly below `epsilon_tip`, the encoding is internally inconsistent and considered falsified.
* If small perturbations to the encoding within the allowed ranges in `A_enc` cause arbitrarily large changes in relative tension ranking of scenarios, the encoding is considered unstable and rejected.

*Semantics implementation note:*
All quantities are treated as continuous fields as specified in the metadata. Any discretization used in numerical practice is an implementation detail outside this effective description.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

### Experiment 2: Early warning indicators and tipping tension

*Goal:*
Assess whether the Q092 tension encoding tracks early warning indicators of approaching tipping points in model simulations or paleoclimate records.

*Setup:*

* Select time series that climate science regards as candidates for tipping behavior, such as:

  * Circulation strength indices,
  * Ice sheet volume proxies,
  * Monsoon rainfall indices.

* For each time window and series, compute standard early warning indicators, for example:

  * Rolling variance,
  * Rolling lag one autocorrelation.

* Map each time window into a state `m` in `M_reg` by:

  * Setting `X_i(m)` from the observed or simulated indicator,
  * Computing `theta_i(m)` relative to fixed bands `[L_i, U_i]`,
  * Setting `rho_tail(m; tau_l)` using a simple model that interprets early warning signals as increased hazard.

The mapping from early warning statistics to `theta_i` and `rho_tail` is fixed once and used for all series.

*Protocol:*

1. For each time window, compute `theta_i(m)`, `rho_tail(m; tau_l)` for relevant `tau_l`, and then `Tension_tip(m)`.

2. Plot or tabulate the evolution of `Tension_tip(m)` alongside early warning indicators for each series.

3. Identify whether increases in early warning indicators correspond to consistent increases in `Tension_tip(m)` under the chosen encoding.

*Metrics:*

* Correlation between `Tension_tip(m)` and early warning indicators over time.
* Frequency with which known precursor periods to suspected tipping events show rising tension.
* Rate of false positives where tension rises but no tipping or regime shift occurs in the available record.

*Falsification conditions:*

* If early warning indicators rise sharply for multiple independent cases, but `Tension_tip(m)` remains low or oscillates without clear structure, the encoding is considered misaligned and is rejected for Q092.
* If `Tension_tip(m)` shows frequent strong spikes in periods where domain experts see no evidence of tipping or precursor behavior, and this pattern persists across multiple records, the encoding is considered to produce too many false positives and is rejected.

*Semantics implementation note:*
The encoding treats both early warning statistics and tipping tension as continuous valued observables consistent with the metadata field type, with no change of semantic category.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.

---

## 7. AI and WFGY engineering spec

This block describes how Q092 can be used in AI systems within WFGY at the effective layer.

### 7.1 Training signals

We define several training signals suitable for supervising or regularizing AI models.

1. `signal_tipping_proximity_consistency`

   * Definition: a penalty proportional to `I_prox(m)` for states associated with narratives that claim the system is far from tipping.
   * Use: reduce contradictions where the model simultaneously asserts safety while describing multiple elements as near their thresholds.

2. `signal_cascade_risk_alignment`

   * Definition: a signal built from `CascadeIndex(m)` for scenarios where text or data indicate strong coupling and potential cascades.
   * Use: encourage the model to represent highly coupled tipping situations as high cascade risk, not as independent events.

3. `signal_scenario_tension_profile`

   * Definition: uses `Tension_tip(m)` as a scalar target or auxiliary prediction for scenario descriptions.
   * Use: guide the model toward coherent ranking of scenarios according to their climate tipping risk.

4. `signal_world_T_vs_world_F_separation`

   * Definition: a signal that encourages distinct internal representations for low tension world descriptions and high tension world descriptions when both are presented as counterfactuals.
   * Use: avoid collapsing qualitatively different climate futures into a single ambiguous representation.

### 7.2 Architectural patterns

We outline module patterns that can reuse Q092 structures.

1. `TippingElementHead`

   * Role: given a text description or structured scenario input, predict the vector of `theta_i(m)` for a fixed tipping element library.
   * Interface: inputs scenario embeddings, outputs a vector of normalized proximity indices.

2. `CascadeRiskAggregator`

   * Role: compute `CascadeIndex(m)` and `Tension_tip(m)` from predicted `theta_i(m)`, `C_ij(m)`, and `rho_tail(m; tau_l)`.
   * Interface: inputs are internal representations mapped to those observables, outputs are scalar scores fed to loss functions or used for interpretation.

3. `ScenarioComparator`

   * Role: given two or more scenario descriptions, produce comparative judgments with respect to Q092 tension, supported by the above modules.
   * Interface: takes multiple scenario embeddings and returns relative tension rankings and brief structured rationales.

### 7.3 Evaluation harness

A minimal evaluation harness for AI models using Q092.

1. Task design

   * Construct a benchmark of climate scenario descriptions where domain experts have qualitative expectations about tipping risk ranking.

2. Conditions

   * Baseline: model answers questions without explicit Q092 modules.
   * TU enhanced: model uses TippingElementHead and CascadeRiskAggregator to compute `Tension_tip(m)` and receives training signals derived from it.

3. Metrics

   * Accuracy of scenario ranking relative to expert judgments.
   * Internal consistency: frequency with which the model makes logically incompatible statements about tipping risk across related questions.
   * Stability: how often small perturbations in the scenario description lead to moderate, rather than extreme, changes in predicted tension.

### 7.4 60 second reproduction protocol

A simple test for users to experience the impact of Q092 encoding.

* Baseline setup:

  * Prompt the model: “Explain what climate tipping points are and how they matter for future climate risk.”
  * Record whether the explanation:

    * mixes up local and systemic tipping,
    * lacks discussion of thresholds and cascades,
    * gives inconsistent statements about reversibility.

* TU encoded setup:

  * Prompt the model: “Explain what climate tipping points are and how they matter for future climate risk, using a framework where each tipping element has a proximity index, couplings, and a scalar tension score that grows when many elements approach their thresholds and cascades become likely.”
  * Record whether the explanation:

    * explicitly organizes around tipping elements, thresholds, couplings, and tail risk,
    * presents a clearer description of systemic risk and cascades.

* Comparison metric:

  * Use a simple rubric based on structure, completeness, and internal consistency.
  * Optionally ask independent judges which answer better captures important aspects of climate tipping.

* What to log:

  * Prompts and full responses.
  * Any auxiliary `Tension_tip(m)` values the system can expose, if available.

All of this stays at the effective layer and does not reveal any deep TU generative rule.

---

## 8. Cross problem transfer template

This block describes reusable components from Q092 and where they transfer.

### 8.1 Reusable components produced by this problem

1. ComponentName: `TippingElementLibrary`

   * Type: field

   * Minimal interface:

     * Inputs: scenario description or structured climate state summary.
     * Outputs: a fixed dimension vector of element states and proximity indices `(X_i, theta_i)` for each `E_i` in the library.

   * Preconditions:

     * The scenario must specify climate conditions and time horizons clearly enough to assign consistent indices.

2. ComponentName: `ClimateTensionFunctional_CTP`

   * Type: functional

   * Minimal interface:

     * Inputs: `theta_i`, `C_ij`, `rho_tail(m; tau_l)` for `tau_l` in `Tau`.
     * Output: a nonnegative scalar `Tension_tip`.

   * Preconditions:

     * All inputs refer to the same encoding class in `A_enc`.
     * Observables are finite and defined for the given state.

3. ComponentName: `EarlyWarningToTensionMapper`

   * Type: experiment_pattern

   * Minimal interface:

     * Inputs: time series of indicators and associated early warning statistics.
     * Outputs: approximate trajectories of `theta_i` and `Tension_tip` over time.

   * Preconditions:

     * Time series are long enough to compute stable early warning statistics.
     * Indicator to element mapping is specified and fixed.

### 8.2 Direct reuse targets

1. Target: Q093 (Full carbon cycle feedbacks)

   * Reused components: `TippingElementLibrary`, `ClimateTensionFunctional_CTP`.
   * Why it transfers: carbon feedbacks can be treated as one of the tipping elements whose state and hazard directly influence overall tension.
   * What changes: forcing descriptions and element definitions are extended to include explicit carbon pools and fluxes, but the functional structure stays the same.

2. Target: Q098 (Anthropocene system dynamics)

   * Reused components: `TippingElementLibrary`, `ClimateTensionFunctional_CTP`, `EarlyWarningToTensionMapper`.
   * Why it transfers: human Earth system co dynamics can be modeled as interacting tipping elements where climate subsystems are a subset.
   * What changes: element library grows to include socio economic and technological tipping elements, but climate elements retain their Q092 definitions.

3. Target: Q105 (Prediction of systemic crashes)

   * Reused components: `ClimateTensionFunctional_CTP`.
   * Why it transfers: risk_tail_tension in financial or infrastructural networks can be encoded with a function that mirrors the climate tipping tension structure.
   * What changes: the semantics of `theta_i`, `C_ij`, and `rho_tail` shift from climate variables to network or market variables.

---

## 9. TU roadmap and verification levels

This block situates Q092 on the TU verification ladder and outlines next steps.

### 9.1 Current levels

* E_level: E1

  * A coherent effective layer encoding has been specified with:

    * a finite tipping element library,
    * well defined observables and invariants,
    * a tension functional `Tension_tip(m)`,
    * a singular set `S_sing` and domain restriction.

  * At least two concrete experiments with explicit falsification conditions have been outlined.

* N_level: N1

  * The narrative connecting tipping elements, thresholds, couplings, hazard, and systemic tension is explicit and self consistent at a qualitative level.
  * Counterfactual low and high tension worlds have been described in terms of the same observables.

### 9.2 Next measurable steps toward E2 and N2

To reach E2:

* Implement at least one of the experiments in Block 6 with real climate model ensembles or data sets.
* Publish tension profiles and basic statistics in a format that allows independent reproduction using the same encoding specification.

To reach N2:

* Fix a concrete instance of `A_enc` including:

  * a public catalog of elements `E_i` and their threshold bands,
  * a fixed coupling adjacency and sign structure for `C_ij`,
  * a public description of `Tau` and of the function `G` defining `DeltaS_tip`.

* Demonstrate, on at least one benchmark, that the encoding produces tension rankings that align reasonably with domain expert judgments.

### 9.3 Long term role in TU

In the long term, Q092 is expected to:

* Serve as the central Earth system node for risk_tail_tension questions.
* Provide reusable components for downstream problems in socio technical systems that depend on climate stability.
* Act as a bridge between physical climate risk, early warning indicators, and AI models tasked with reasoning about climate futures.

---

## 10. Elementary but precise explanation

In simple terms, climate tipping points are places in the climate system where “a little more push” can trigger a big and mostly one way change.

Examples include:

* An ice sheet that, once it melts past a certain point, keeps shrinking even if warming slows.
* An ocean circulation pattern that, once weakened enough, flips to a different mode.
* A rainforest that, once it loses enough trees or receives much less rain, shifts toward a savanna like state.

In this Q092 framing, we do not try to simulate the climate in full detail. Instead, we:

1. List a finite set of important climate pieces that can tip.
2. For each piece, define a number that tells us how close it is to its dangerous band.
3. Record how strongly each piece can push others toward tipping.
4. Define a score that measures how likely it is that one or more pieces will tip within certain time windows.

This score is the tipping tension. It is low when all pieces are safe and loosely coupled. It is high when many are close to their thresholds, especially if they are strongly connected so that one tipping event can trigger others.

We then imagine two broad kinds of worlds:

* In a low tension world, most tipping elements stay far from danger, and even large disturbances do not cause global cascades.
* In a high tension world, several elements are close to tipping, cascades are possible, and small extra pushes can have big long term consequences.

Our encoding gives a way to talk about which world our climate system is moving toward without claiming to solve climate dynamics or to predict exact tipping times. It also provides:

* Experiments to test whether a given way of scoring tension is sensible.
* Building blocks that AI systems can use to reason more carefully about climate tipping and related risks, while staying within an effective, observable based layer.
