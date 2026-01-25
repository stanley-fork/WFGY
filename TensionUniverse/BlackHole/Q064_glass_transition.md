# Q064 · Glass transition in supercooled liquids and amorphous solids

## 0. Header metadata

```txt
ID: Q064
Code: BH_CHEM_GLASS_TRANS_L3_064
Domain: Chemistry
Family: Physical chemistry / soft matter
Rank: S
Projection_dominance: I
Field_type: dynamical_field
Tension_type: thermodynamic_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-25
````

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The classical glass transition problem can be stated as follows.

Consider liquids that can be cooled below their melting temperature without crystallizing. These supercooled liquids exhibit a dramatic increase in viscosity and relaxation times over a modest change in control parameters (for example temperature or density), and eventually form amorphous solids called glasses.

The core question is:

> Is there a compact, physically grounded, and quantitatively predictive theory that explains how microscopic interactions and configurations in supercooled liquids give rise to:
>
> * the enormous slowdown of dynamics,
> * the emergence of rigidity without long range crystalline order,
> * and the associated thermodynamic and dynamic anomalies,
>
> across families of materials and control protocols, using a finite set of effective invariants and rules?

This includes questions such as:

* Is there an underlying thermodynamic phase transition or only a dynamic crossover?
* Can a small set of structural or landscape descriptors fully account for the slowing down?
* How do dynamic heterogeneity and cooperative motion arise and scale?

### 1.2 Status and difficulty

Key observed facts include:

* The viscosity `eta(T)` and main structural relaxation time `tau_alpha(T)` can increase by 10 or more orders of magnitude over a moderate temperature range as the system approaches a glassy state.
* Dynamic heterogeneity emerges: different regions relax at very different rates, and cooperative rearrangements become important.
* The structure factor and pair correlations change only modestly, even as dynamics slow dramatically.
* Many different theoretical frameworks have been proposed, including:

  * mode coupling theory type approaches,
  * energy landscape and inherent structure pictures,
  * random first order transition type scenarios,
  * dynamic facilitation and kinetically constrained models.

Despite major progress, there is no universally accepted compact theory that yields a small set of invariants and rules which:

* describe the onset of dynamic arrest,
* unify different classes of glass formers (molecular, polymer, colloidal),
* and predict key observables across protocols without extensive case by case fitting.

The problem is widely considered extremely difficult and cross cutting between chemistry, soft matter physics, and statistical mechanics.

### 1.3 Role in the BlackHole project

In the BlackHole S problem set, Q064 has three main roles.

1. It is the flagship example of a **thermodynamic_tension** problem in soft condensed matter, where:

   * thermodynamic quantities,
   * dynamic observables,
   * and emergent rigidity
     must be held together in a single effective description.

2. It provides a test bed for the idea that a rugged high dimensional energy landscape can be summarized by:

   * a finite set of landscape complexity and fragility invariants,
   * combined with a small number of dynamic arrest indicators.

3. It acts as a bridge between:

   * microscopic chemistry and bonding (Q061),
   * general non equilibrium thermodynamics (Q032),
   * and biological or AI systems that may exhibit glass like dynamic arrest (for example Q071, Q121, Q123).

### References

1. C. A. Angell, “Formation of glasses from liquids and biopolymers”, *Science* 267 (1995), 1924–1935.
2. P. G. Debenedetti and F. H. Stillinger, “Supercooled liquids and the glass transition”, *Nature* 410 (2001), 259–267.
3. L. Berthier and G. Biroli, “Theoretical perspective on the glass transition and amorphous materials”, *Reviews of Modern Physics* 83 (2011), 587–645.
4. W. Kob, “Supercooled liquids, the glass transition, and computer simulations”, in *Soft and Fragile Matter* (C. R. A. Catlow et al., eds.), Institute of Physics Publishing, 2000.

---

## 2. Position in the BlackHole graph

This block records how Q064 sits inside the BlackHole graph. Each edge has a one line reason pointing to a concrete component or tension type.

### 2.1 Upstream problems

These nodes provide prerequisites or general tools for Q064 at the effective layer.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Supplies the general thermodynamic_tension framework for non equilibrium relaxation and slow dynamics used to interpret glassy behavior.

* Q061 (BH_CHEM_BOND_NATURE_L3_061)
  Reason: Provides an effective description of bonding and strong correlations needed to justify coarse grained interaction models for glass forming liquids and solids.

* Q067 (BH_CHEM_QUANTUM_MOL_SIM_L3_067)
  Reason: Constrains what can in practice be computed from microscopic simulations, bounding how directly landscape and dynamics can be resolved.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: Gives general soft matter organization principles which Q064 specializes to the amorphous, dynamically arrested regime.

### 2.2 Downstream problems

These nodes reuse Q064 components or depend on its tension structure.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: Reuses the GlassEnergyLandscapeDescriptor component to classify soft matter phases and transitions between fluid, gel, and glassy states.

* Q071 (BH_BIO_ORIGIN_LIFE_L3_071)
  Reason: Uses the DynamicArrestIndex to bound prebiotic environments where reaction and diffusion rates are controlled by amorphous matrices.

* Q080 (BH_BIO_BIOSPHERE_LIMITS_L3_080)
  Reason: Reuses glassy arrest indicators to discuss how dynamic slowdowns in cells and tissues constrain biosphere level adaptability.

### 2.3 Parallel problems

Parallel nodes share similar tension structures but no direct component dependence.

* Q063 (BH_CHEM_PROTEIN_FOLDING_L3_063)
  Reason: Both Q063 and Q064 deal with rugged landscapes and strong sensitivity of dynamics to shallow thermodynamic changes.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: Both problems focus on soft matter systems where emergent rigidity and slow dynamics come from many body interactions, with different geometric constraints.

* Q077 (BH_BIO_MICROBIOME_L3_077)
  Reason: Both Q064 and Q077 involve many interacting units on a high dimensional landscape where metastability and slow relaxation are central.

### 2.4 Cross domain edges

Cross domain edges capture reuse outside chemistry.

* Q032 (BH_PHYS_QTHERMO_L3_032)
  Reason: Reuses glassy relaxation invariants as concrete examples of extreme non equilibrium thermodynamic behavior.

* Q095 (BH_EARTH_BIODIVERSITY_L3_095)
  Reason: Uses amorphous state and dynamic arrest ideas as microscopic mechanisms affecting ecological timescales and niche persistence.

* Q121 (BH_AI_ALIGNMENT_L3_121)
  Reason: Uses the DynamicArrestIndex as an analogy for pathological trapping in AI objective landscapes and policy spaces.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Reuses the GlassEnergyLandscapeDescriptor as a template for describing slow modes and meta stable regions in AI representation spaces.

---

## 3. Tension Universe encoding (effective layer)

This block defines the Q064 encoding strictly at the effective layer. We specify:

* state space,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any deep generative rule or raw data to field mapping.

### 3.1 State space

We assume a state space

```txt
M
```

with the following interpretation.

* Each element `m` in `M` represents a coherent glass forming configuration at the effective layer, specified by:

  * material type (molecular liquid, polymer melt, colloidal suspension, and so on),
  * interaction class (for example strong directional bonding vs nearly isotropic),
  * control parameters (temperature, pressure, density, composition, cooling rate),
  * regime label (for example equilibrium liquid, deeply supercooled, near glass transition, glassy solid).

* For each `m` we assume the existence of finite, well defined summaries of:

  * structural information at some chosen coarse graining scale,
  * potential energy landscape statistics at that scale,
  * dynamic relaxation time distributions under the chosen protocol.

We do not specify how these summaries are constructed from microscopic coordinates or trajectories. We only assume that for each regime and protocol of interest, states `m` exist with consistent summaries.

We define the regular subset:

```txt
M_reg subset of M
```

as the set of states for which all observables and invariants defined below are finite and well defined. The singular set `S_sing` will be specified in Section 3.5.

### 3.2 Observables and effective fields

We introduce the following observables on `M_reg`.

1. Structural relaxation time

```txt
tau_alpha(m) > 0
```

* Main structural relaxation time or a closely related timescale, measured under the protocol encoded in `m`.

2. Viscosity or effective viscosity like quantity

```txt
eta(m) > 0
```

* Effective viscosity or equivalent measure of resistance to flow.

3. Configurational entropy proxy

```txt
S_conf(m)
```

* A scalar summarizing the effective number of distinct amorphous basins relevant at the control parameters of `m`.
* We only assume `S_conf(m)` is finite and monotone with respect to effective landscape complexity in the regime considered.

4. Dynamic heterogeneity length scale

```txt
xi_dyn(m) >= 0
```

* A characteristic length associated with spatial correlations in relaxation dynamics.

5. Landscape roughness index

```txt
R_rough(m) >= 0
```

* A scalar that summarizes the spread and height of energy barriers between relevant amorphous basins.

6. Caged fraction

```txt
f_cage(m) in [0, 1]
```

* Fraction of regions or particles that are effectively trapped on the timescale `tau_alpha(m)`.

7. Protocol label field

```txt
Prot(m)
```

* A discrete label for the preparation or measurement protocol (for example slow cooling, fast quench, isothermal aging).
* This is used only to group states and is not a continuous observable.

Each observable above is an effective map from `M_reg` to real numbers or a small discrete set. The hybrid nature of the overall field type comes from the combination of continuous valued observables and discrete labels.

### 3.3 Invariants and effective constraints

From the observables we define effective invariants.

1. Fragility index

```txt
Fragility_index(m)
```

* An effective index summarizing how sharply `tau_alpha(m)` grows as the control parameter approaches the glassy regime.
* For example, in a given encoding the fragility index can be derived from fits of the form

```txt
tau_alpha(T) ~ exp( A / ( T - T0 ) )
```

or similar, but the exact fitting choice is fixed at the encoding class level, not per material.

2. Dynamic arrest index

```txt
DynamicArrestIndex(m)
```

* A scalar combining relaxation time, viscosity, and caging into a single measure of arrest, for example:

```txt
DynamicArrestIndex(m) =
  c1 * log10( tau_alpha(m) / tau_ref )
  + c2 * log10( eta(m) / eta_ref )
  + c3 * f_cage(m)
```

* Constants `c1`, `c2`, `c3`, `tau_ref`, `eta_ref` are fixed at the encoding class level, shared across materials.

3. Landscape complexity index

```txt
LandscapeComplexityIndex(m)
```

* A scalar summarizing how crowded and rough the relevant part of the landscape is, for example:

```txt
LandscapeComplexityIndex(m) =
  d1 * S_conf(m) + d2 * R_rough(m)
```

* Constants `d1`, `d2` are again fixed at the encoding class level.

These invariants must be stable under modest changes in coarse graining and data quality, within explicit tolerance bands that are specified once for the encoding class.

### 3.4 Encoding class and fairness constraints

To prevent post hoc tuning and to make tension measures falsifiable, we fix an admissible encoding class for Q064.

1. Encoding class definition

We define a class `E_glass` of encodings, where each encoding `E` in `E_glass` specifies:

* the functional forms used to extract `Fragility_index`, `DynamicArrestIndex`, and `LandscapeComplexityIndex` from raw observable summaries,
* the global constants such as `c1`, `c2`, `c3`, `d1`, `d2`, `tau_ref`, `eta_ref`,
* the allowed tolerances for coarse graining and numerical errors,
* the specific set of control parameter ranges in which the encoding is expected to apply.

2. Fairness constraints

For any fixed encoding `E` in `E_glass`:

* All constants and functional forms must be chosen before looking at individual material data sets that will later be used for evaluation.
* The same encoding must be applied to all materials and protocols in a given study.
* If an encoding `E` is modified after inspecting specific data to improve apparent agreement, the modified encoding is treated as a new element in `E_glass` and must be re tested on the full suite of systems.

This prevents cheating by adapting the encoding to each case and ensures that tension functionals have genuine predictive content.

### 3.5 Singular set and domain restriction

We define a singular set:

```txt
S_sing = { m in M :
           tau_alpha(m), eta(m), S_conf(m), xi_dyn(m),
           R_rough(m), or f_cage(m) are undefined,
           inconsistent, or not finite in the encoding E }
```

for a fixed encoding `E` in `E_glass`.

Domain restriction:

* All glass tension functionals introduced later are defined only on:

```txt
M_reg = M \ S_sing
```

* If experiments or models produce states that map into `S_sing`, the result is treated as an out of domain event for this encoding, not as evidence for extreme but finite tension values.

This is the explicit handling of the singular set `S_sing` required by the constitution.

---

## 4. Tension principle for this problem

This block defines how Q064 is framed as a tension problem at the effective layer.

### 4.1 Core tension functional

For a fixed encoding `E` in `E_glass`, we define a glass tension functional on `M_reg`:

```txt
Tension_glass(m) =
  b1 * DeltaS_relax(m) +
  b2 * DeltaS_structure(m)
```

where:

* `b1 > 0` and `b2 > 0` are global constants fixed once for the encoding,
* `DeltaS_relax(m)` measures mismatch between observed relaxation scaling and a chosen reference scaling law for the class of materials,
* `DeltaS_structure(m)` measures mismatch between structural or landscape observables and a reference pattern expected for a compact glass theory.

A simple construction consistent with the effective layer view is:

```txt
DeltaS_relax(m) =
  | Fragility_index(m) - Fragility_ref(Class(m)) |

DeltaS_structure(m) =
  | LandscapeComplexityIndex(m) - LCI_ref(Class(m)) |
```

where:

* `Fragility_ref(Class(m))` is a reference fragility value for the material class encoded in `m`,
* `LCI_ref(Class(m))` is a reference landscape complexity value for that class,
* both reference maps are fixed once per encoding `E` and cannot be chosen separately for each material.

By construction:

```txt
Tension_glass(m) >= 0
```

for all `m` in `M_reg`. Small tension corresponds to systems where both dynamic and structural invariants lie near the reference values for their class.

### 4.2 Low tension principle for compact glass theory

At the effective layer, a compact theory of the glass transition corresponds to the following principle.

> For a wide range of glass forming systems and protocols, there exists an encoding `E` in `E_glass` and states `m` in `M_reg` representing those systems such that:
>
> * `Tension_glass(m)` lies in a low tension band,
> * the band does not blow up as data quality improves or as more systems are added.

Formally, there exists an `E` and constants `epsilon_glass > 0` and `K >= 1` such that for all systems within the declared scope of `E`:

```txt
Tension_glass(m_data) <= epsilon_glass
```

up to a factor `K` accounting for controlled experimental and numerical uncertainties.

If such an encoding exists and is stable across many systems, the glass transition can be seen as governed by a small set of invariants and rules.

### 4.3 High tension failure for non compact scenarios

If no compact theory exists within the constraints of `E_glass`, we expect the following pattern.

> For every encoding `E` in `E_glass` and for any candidate bounds `epsilon_glass`, there exist glass forming systems within the declared scope of `E` whose faithful states `m` in `M_reg` satisfy:
>
> * `Tension_glass(m)` is bounded below by a strictly positive value that does not go away under refinement.

Concretely, for each encoding `E` in `E_glass` there would exist a positive `delta_glass(E)` such that for some systems:

```txt
Tension_glass(m_data) >= delta_glass(E)
```

and this inequality persists when:

* more accurate data are used,
* reasonable coarse graining changes are applied,
* protocol labels remain within the declared scope.

In this case, any attempt to compress the glass transition into a small set of invariants and rules under the specified constraints fails at the effective layer.

---

## 5. Counterfactual tension worlds

We now consider two counterfactual worlds described purely at the level of observables and invariants.

* World T: a compact glass theory world with low thermodynamic tension.
* World F: a non compact world where glass behavior resists compression and exhibits persistent high tension.

### 5.1 World T (compact glass theory, low tension)

In World T, for a fixed encoding `E` in `E_glass`:

1. Coherent scaling of relaxation and viscosity

* The relation between `tau_alpha(m)`, `eta(m)`, and control parameters can be expressed by a small family of scaling forms with parameters tied to `Fragility_index(m)`.
* Most materials in the scope of `E` lie close to these forms, so `DeltaS_relax(m)` remains small.

2. Controlled landscape complexity

* `S_conf(m)` and `R_rough(m)` combine into `LandscapeComplexityIndex(m)` values that cluster around class dependent reference values `LCI_ref(Class(m))`.
* Scaling of `LandscapeComplexityIndex(m)` as control parameters change remains predictable.

3. Dynamic heterogeneity aligned with invariants

* `xi_dyn(m)` and `f_cage(m)` correlate with `DynamicArrestIndex(m)` in a way that can be captured by a small set of relations.
* No large population of systems shows strong violations of these relations within the declared scope.

4. Overall low glass tension

* For most relevant states `m_T`:

```txt
Tension_glass(m_T) <= epsilon_glass
```

with `epsilon_glass` stable as more systems are considered and as measurements improve.

### 5.2 World F (non compact glass behavior, high tension)

In World F, for every encoding `E` in `E_glass`:

1. Wide variation in relaxation patterns

* Different glass formers exhibit scaling of `tau_alpha(T)` and `eta(T)` that cannot be captured by any small family of forms with parameters tied to `Fragility_index`.
* Clusters of materials that look similar structurally display very different dynamic slowdowns.

2. Uncompressible landscape diversity

* `S_conf(m)` and `R_rough(m)` combine into `LandscapeComplexityIndex(m)` values that are broadly scattered.
* Attempts to define `LCI_ref(Class(m))` with small residuals fail: large systematic deviations appear regardless of encoding details.

3. Irregular dynamic heterogeneity

* `xi_dyn(m)` and `f_cage(m)` do not correlate in a clean way with `DynamicArrestIndex(m)` across systems.
* Systems with similar `DynamicArrestIndex` show very different patterns of heterogeneity.

4. Persistent high glass tension

* For some states `m_F` representing real systems within the declared scope of `E`:

```txt
Tension_glass(m_F) >= delta_glass(E)
```

for some `delta_glass(E) > 0`, and this lower bound does not vanish as the encoding is refined.

### 5.3 Interpretive note

These worlds do not claim any specific microscopic mechanism. They only describe how patterns of observables and invariants differ, depending on whether a compact effective theory exists under the encoding class constraints.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols that can falsify or support particular encodings `E` in `E_glass` for Q064, without proving or disproving any microscopic theory.

### Experiment 1: Multi material glass tension profiling

*Goal:*

Test whether there exists an encoding `E` in `E_glass` such that a diverse set of glass formers exhibit low and clustered values of `Tension_glass(m)` under fixed parameters.

*Setup:*

* Select a representative set of materials:

  * molecular glass formers,
  * polymer glasses,
  * colloidal glasses.
* For each material, collect published data or simulations that provide:

  * `tau_alpha(T)` or equivalent relaxation times,
  * `eta(T)` or viscosities,
  * estimates or proxies for `S_conf(T)`,
  * measures of dynamic heterogeneity such as four point correlations or related indicators.

*Protocol:*

1. Choose an encoding `E` in `E_glass` by:

   * fixing functional forms for `Fragility_index`, `DynamicArrestIndex`, and `LandscapeComplexityIndex`,
   * selecting global constants and reference values `Fragility_ref(Class)`, `LCI_ref(Class)` and so on,
   * without inspecting detailed data for the specific materials to be tested.

2. For each material and control parameter range, construct an effective state `m_data` in `M_reg` that summarizes the observables.

3. Compute invariants and the tension:

```txt
Fragility_index(m_data)
DynamicArrestIndex(m_data)
LandscapeComplexityIndex(m_data)
Tension_glass(m_data)
```

4. Analyze the distribution of `Tension_glass(m_data)` values across all materials and conditions.

*Metrics:*

* Histogram or distribution summary of `Tension_glass(m_data)` across the material set.
* Spread of `Tension_glass` values within each material class and across classes.
* Correlation between `Tension_glass` and intuitive indicators of glassy behavior strength.

*Falsification conditions:*

* If for the chosen encoding `E` there is no finite `epsilon_glass` such that a large majority of systems fall into `Tension_glass(m_data) <= epsilon_glass` with modest spread, the encoding is considered falsified as a candidate compact description.
* If small changes of the encoding parameters within their declared tolerance bands lead to arbitrarily different tension distributions, the encoding is considered unstable and rejected.

*Semantics implementation note:*

Hybrid field type is used. Continuous observables (`tau_alpha`, `eta`, `S_conf`, `xi_dyn`, `R_rough`, `f_cage`) are treated as real valued functions on `M_reg`, while material and protocol types are discrete labels. All computations are performed in this mixed but well defined framework.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment can rule out specific glass tension encodings, but it does not by itself prove or disprove the existence of a compact microscopic theory.

---

### Experiment 2: Protocol and composition perturbation tests

*Goal:*

Check whether `Tension_glass(m)` changes in a way that is consistent with observed changes in dynamic arrest when protocols or compositions are varied.

*Setup:*

* Select one or more glass forming systems for which systematic data exist under:

  * different cooling rates,
  * different pressures or densities,
  * small compositional changes (for example binary mixtures with varied composition).
* For each condition, obtain:

  * `tau_alpha`,
  * `eta`,
  * estimates of `S_conf` and `xi_dyn`,
  * caged fraction `f_cage`.

*Protocol:*

1. Use the same encoding `E` in `E_glass` as in Experiment 1, without modifying parameters after inspecting these particular data.

2. For each condition, construct states `m_cond` in `M_reg`.

3. Compute invariants:

```txt
Fragility_index(m_cond)
DynamicArrestIndex(m_cond)
LandscapeComplexityIndex(m_cond)
Tension_glass(m_cond)
```

4. Compare changes in `Tension_glass(m_cond)` between conditions with changes in:

   * `tau_alpha(m_cond)`,
   * `eta(m_cond)`,
   * `xi_dyn(m_cond)`,
   * `f_cage(m_cond)`.

*Metrics:*

* Direction and magnitude of changes in `Tension_glass` when:

  * cooling rate is decreased or increased,
  * pressure is increased at fixed temperature,
  * composition is varied.
* Consistency between increased dynamic arrest and increased `Tension_glass`.

*Falsification conditions:*

* If across multiple systems and perturbations, the encoding predicts:

  * decreasing `Tension_glass` when dynamic arrest is clearly increasing,
  * or no consistent trend while observables show clear systematic changes,
    then the encoding is considered misaligned and rejected.

*Semantics implementation note:*

The hybrid field type is again used. Protocol changes are represented by changes in discrete labels and continuous control parameters, while observables are continuous. No deeper mapping from microscopic dynamics to fields is specified.

*Boundary note:*

Falsifying TU encoding != solving canonical statement. This experiment tests whether a given encoding captures protocol dependence coherently; success does not guarantee that the encoding is fundamentally correct, and failure does not rule out the existence of some other compact theory.

---

## 7. AI and WFGY engineering spec

This block describes how Q064 can be used as an engineering module for AI systems in WFGY, strictly at the effective layer.

### 7.1 Training signals

We define several training signals derived from the glass encoding.

1. `signal_glass_relaxation_scaling`

* Definition: a loss term proportional to `DeltaS_relax(m)` for internal states that represent glass forming systems.
* Use: penalizes internal representations that imply relaxation patterns incompatible with the chosen compact scaling forms under the assumed conditions.

2. `signal_dynamic_heterogeneity`

* Definition: a loss term based on the difference between inferred dynamic heterogeneity indicators from internal representations and target patterns mapped to `xi_dyn` and `f_cage`.
* Use: encourages the model to keep track of which regions are fast or slow in a way that matches known glassy behavior.

3. `signal_glass_tension_score`

* Definition: a scalar auxiliary prediction target equal to `Tension_glass(m)` as computed from encoded invariants.
* Use: gives the model a continuous knob indicating how close a scenario is to dynamic arrest.

4. `signal_counterfactual_glass_consistency`

* Definition: a consistency signal that compares the model’s answers when prompted under:

  * a World T assumption (compact theory world),
  * a World F assumption (non compact world),
    and penalizes mixing of assumptions in a single reasoning chain.
* Use: helps the model keep different high level hypotheses about the glass transition separate.

### 7.2 Architectural patterns

We outline module patterns that reuse Q064 components.

1. `GlassTensionHead`

* Role: given an internal representation of a glass related context, predict:

  * `Fragility_index`,
  * `DynamicArrestIndex`,
  * `LandscapeComplexityIndex`,
  * `Tension_glass`.
* Interface:

  * Input: an embedding summarizing the problem context (material, protocol, observables).
  * Output: a small vector of invariant estimates plus a scalar tension.

2. `ConfigEntropyObserver`

* Role: map internal representations to an effective `S_conf` and to coarse measures of landscape roughness.
* Interface:

  * Input: internal states capturing structural descriptions.
  * Output: a pair `(S_conf_hat, R_rough_hat)` that can be fed into invariant computations.

3. `HeterogeneityFilter`

* Role: interpret internal space time like descriptions of glassy systems and extract a `DynamicHeterogeneityIndex` compatible with `xi_dyn` and `f_cage`.
* Interface:

  * Input: sequences or grids of local state embeddings.
  * Output: a scalar or short vector characterizing heterogeneity patterns.

### 7.3 Evaluation harness

We suggest an evaluation harness for AI models augmented with Q064 modules.

1. Task suite

* Questions and design tasks about:

  * explaining glass transition phenomena,
  * predicting qualitative effects of protocol changes,
  * comparing different glass formers,
  * suggesting experimental or simulation probes.

2. Conditions

* Baseline:

  * Model without explicit Q064 modules.
* TU augmented:

  * Same base model with:

    * GlassTensionHead,
    * ConfigEntropyObserver,
    * HeterogeneityFilter,
    * and training signals defined above.

3. Metrics

* Accuracy on factual and explanatory questions about glassy dynamics.
* Internal consistency:

  * how often predictions about relaxation and heterogeneity agree across prompts that describe the same physical situation.
* Stability of reasoning:

  * whether answers remain consistent when the prompt is rephrased but the encoded invariants should be unchanged.

### 7.4 60 second reproduction protocol

This is a minimal user facing protocol.

* Baseline setup:

  * Prompt: ask the model
    "Explain what the glass transition is and why dynamics slow down in supercooled liquids."
  * Observe:

    * whether the answer is fragmented,
    * whether it mixes incompatible pictures,
    * whether it ignores dynamic heterogeneity.

* TU encoded setup:

  * Prompt: same question, plus an instruction such as
    "Organize your explanation using configurational entropy, relaxation time scaling, dynamic heterogeneity, and an effective glass tension that measures mismatch between dynamics and structure."
  * Observe:

    * whether the explanation becomes more structured,
    * whether it links observables to a clear notion of dynamic arrest,
    * whether it acknowledges unresolved aspects without confusion.

* Comparison metric:

  * A simple rubric scoring:

    * clarity of structure,
    * explicit linking of structure and dynamics,
    * internal consistency about how arrest emerges.

* What to log:

  * Prompts, responses, and any auxiliary tension scores from GlassTensionHead.
  * This allows later inspection and comparison without exposing any deeper TU generative mechanism.

---

## 8. Cross problem transfer template

This block describes reusable components produced by Q064 and their direct reuse targets.

### 8.1 Reusable components produced by this problem

1. ComponentName: `GlassEnergyLandscapeDescriptor`

* Type: field
* Minimal interface:

  * Inputs:

    * summaries of basin depths and barrier heights,
    * control parameters such as temperature and density.
  * Output:

    * feature vector containing:

      * `Fragility_index`,
      * `LandscapeComplexityIndex`,
      * additional optional landscape features.
* Preconditions:

  * The system is in a regime where an effective landscape description is meaningful and observables are well defined (`m` in `M_reg`).

2. ComponentName: `DynamicHeterogeneityIndex`

* Type: observable
* Minimal interface:

  * Inputs:

    * local relaxation patterns or equivalent internal representations.
  * Output:

    * scalar or short vector summarizing strength and length scale of dynamic heterogeneity.
* Preconditions:

  * The underlying data allow extraction of local relaxation statistics or correlators.

3. ComponentName: `CounterfactualGlassWorld_Template`

* Type: experiment_pattern
* Minimal interface:

  * Inputs:

    * specification of a class of glass forming systems and protocols,
    * an encoding `E` in `E_glass`.
  * Output:

    * two experiment designs:

      * a World T style evaluation assuming compact behavior,
      * a World F style evaluation assuming non compact behavior,
        each with a procedure to compute distribution of `Tension_glass`.
* Preconditions:

  * Sufficient data or model access to estimate invariants and tension in both scenarios.

### 8.2 Direct reuse targets

1. Q070 (BH_CHEM_SOFTMATTER_L3_070)

* Reused component:

  * `GlassEnergyLandscapeDescriptor`.
* Why it transfers:

  * soft matter self assembly problems can be framed using similar landscape descriptors even when the final states are gels or ordered structures rather than glasses.
* What changes:

  * the interpretation of the invariants shifts from dynamic arrest to pathway selection and phase competition.

2. Q071 (BH_BIO_ORIGIN_LIFE_L3_071)

* Reused component:

  * `DynamicHeterogeneityIndex`.
* Why it transfers:

  * prebiotic chemistry in crowded or amorphous environments experiences glass like dynamic constraints, which can be summarized by the same heterogeneity indices.
* What changes:

  * observables relate to reaction networks and diffusion limits rather than purely physical relaxation.

3. Q123 (BH_AI_INTERP_L3_123)

* Reused components:

  * `GlassEnergyLandscapeDescriptor`,
  * `CounterfactualGlassWorld_Template`.
* Why it transfers:

  * representation spaces in AI models can exhibit rugged landscapes and slow modes analogous to glassy systems.
* What changes:

  * physical control parameters are replaced by training and architecture parameters, and tension measures relate to learning dynamics and generalization rather than viscosity.

---

## 9. TU roadmap and verification levels

This block explains Q064’s position in the TU verification ladder and the next measurable steps, consistent with E1 and N1.

### 9.1 Current levels

* E_level: E1

  * A coherent effective encoding for glassy systems has been specified:

    * state space,
    * observables,
    * invariants,
    * singular set,
    * tension functional.
  * Discriminating experiments are defined at the level of observables and encodings, not microscopic theories.

* N_level: N1

  * The narrative linking rugged landscapes, dynamic arrest, and thermodynamic_tension is explicit at the effective layer.
  * Counterfactual worlds and cross domain connections are stated, but not yet systematically instantiated.

### 9.2 Next measurable step toward E2

To reach E2, at least one of the following should be implemented and documented.

1. Data based prototype

* Build a prototype tool that:

  * ingests published data on `tau_alpha`, `eta`, `S_conf`, `xi_dyn`, and `f_cage` for several glass formers,
  * constructs states `m_data` for a fixed encoding `E`,
  * computes `Fragility_index`, `DynamicArrestIndex`, `LandscapeComplexityIndex`, and `Tension_glass`,
  * publishes the resulting tension profiles and distributions as an open data set.

2. Model world study

* Construct model glass forming systems (for example Lennard Jones mixtures) under different protocols and:

  * apply the same encoding `E` to simulation outputs,
  * compare experiment like and simulation based tension profiles,
  * test stability of results under coarse graining changes.

Both steps operate entirely at the effective layer, and success or failure of particular encodings can be recorded without any claim about microscopic uniqueness.

### 9.3 Long term role in the TU program

Long term, Q064 is expected to serve as:

* the reference S level node for thermodynamic_tension problems in soft condensed matter,
* a template for how to encode rugged landscape and dynamic arrest phenomena without revealing deep TU generative rules,
* a bridge from physical glassiness to:

  * biological crowding and aging,
  * AI training and representation pathologies,
  * and broader non equilibrium systems where dynamic arrest appears.

---

## 10. Elementary but precise explanation

This block provides a non technical explanation aligned with the effective layer description.

In everyday terms, the glass transition is about how a liquid can become so sluggish that it behaves like a solid, even though its atoms or molecules never form an orderly crystal.

As such a liquid is cooled or compressed, its viscosity and relaxation times shoot up by many orders of magnitude. Motion slows down enormously. Yet if you look only at simple structural measures, the system still looks like a disordered liquid, not like a crystal.

In the Tension Universe view, we do not try to explain every microscopic detail. Instead, we ask:

* Can we describe glass forming systems using a small number of effective quantities that capture:

  * how fast they relax,
  * how crowded their energy landscape is,
  * how uneven their local dynamics are?
* Can we combine these into a single number, a glass tension, that:

  * is small when structure and dynamics fit together in a simple way,
  * becomes large when they do not?

We imagine assigning to each material and protocol a state, which stores:

* its typical relaxation time and viscosity,
* a measure of how many distinct disordered configurations matter,
* a measure of how rough the energy landscape is,
* a measure of how patchy and unequal the local motion is.

From these, we build invariants such as:

* a fragility index,
* a dynamic arrest index,
* a landscape complexity index.

Then we define a glass tension that grows when:

* relaxation behavior does not match the expected patterns for a given class,
* or when landscape and heterogeneity indicators are out of line with those patterns.

In a world where a compact glass theory exists, we should be able to choose one reasonable encoding so that many different glass formers end up with similar low glass tension. In a world where no such theory exists, any fixed encoding will see some systems with stubbornly high glass tension, and this will not go away as data improve.

Q064 therefore does not claim to solve the glass transition. It instead states:

* how to talk about it in a structured, observable based way,
* how to define a tension that can be tested and possibly falsified,
* and how to reuse the same ideas in other domains where systems become stuck or slow without obvious order.

This is the role of Q064 as a BlackHole S level problem in the Tension Universe framework.
