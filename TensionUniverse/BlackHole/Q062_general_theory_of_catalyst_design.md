# Q062 · General theory of catalyst design

## 0. Header metadata

```txt
ID: Q062
Code: BH_CHEM_CATALYST_DESIGN_L3_062
Domain: Chemistry
Family: Catalysis and surface chemistry
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

The canonical problem behind Q062 can be stated as follows.

Given:

* a very large design space of possible catalysts
  (including bulk materials, surfaces, nanostructures, molecular and bio inspired systems),
* a set of target reactions and operating conditions,
* microscopic information about bonding, adsorption, and reaction barriers
  (when available or computable),

is there a general theory of catalyst design that provides:

1. a compact representation of the relevant design variables,
2. predictive relations between these variables and macroscopic performance
   (activity, selectivity, stability, cost),
3. principled rules for navigating the design space that do not rely on extensive trial and error?

Equivalently, Q062 asks whether one can construct a unified design framework where:

* catalysts for many reactions can be embedded into a common descriptor space,
* performance can be expressed as smooth functionals of these descriptors,
* trade offs among activity, stability, and cost can be described by structured fronts
  rather than ad hoc case by case stories.

The problem is not to find a particular good catalyst.
The problem is to understand whether a general, reusable design theory exists at all
for strongly complex catalytic systems and, if so, what its effective structure is.

### 1.2 Status and difficulty

In practice, several partial design paradigms exist.

* Structure sensitivity and active site concepts capture some aspects of heterogeneous catalysis.
* Linear scaling relations and volcano plots give low dimensional summaries for certain metals and reactions.
* Microkinetic models connect reaction networks with rate expressions when the mechanism is sufficiently understood.
* High throughput computation and machine learning provide powerful search tools, but they often work as black boxes.

Despite these advances, there is still no generally accepted theory that:

* organizes catalyst design across different reaction families,
* systematically explains when low dimensional descriptors are sufficient or doomed to fail,
* reconciles electronic structure, reaction network dynamics, and macroscopic performance
  into a single coherent design tension picture.

The problem is considered extremely difficult because it combines:

* strongly correlated electronic structure in active sites,
* complex energy landscapes with multiple intermediates and pathways,
* mass transport, deactivation, and stability issues,
* economic and engineering constraints at scale.

Q062 therefore occupies an S rank in the BlackHole collection.
It does not target a single theorem but rather a sharp question about whether a unified
effective layer design theory is possible and how such a theory would be structured.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem set, Q062 plays several roles.

1. It is the flagship problem for thermodynamic_tension in complex materials design.
2. It connects the micro scale description of chemical bonding (Q061)
   with macro scale industrial and environmental questions (for example Q091, Q098).
3. It provides a prototype for design problems where:

   * the search space is enormous,
   * naive optimization is impractical,
   * only a tension based organization of design rules can make progress.

From the Tension Universe perspective, Q062 is the place where we ask whether
catalyst design can be reframed as the systematic reduction of a well defined design tension
rather than as a historical collection of heuristics.

### References

1. J. K. Norskov et al., "The nature of the surface chemical bond,"
   Journal of Catalysis 209 (2002), 275–278.
2. J. K. Norskov, F. Abild-Pedersen, F. Studt, T. Bligaard,
   "Fundamental Concepts in Heterogeneous Catalysis,"
   Wiley, 2014, especially Chapters 2, 4, and 7.
3. G. A. Somorjai, Y. Li,
   "Introduction to Surface Chemistry and Catalysis,"
   2nd edition, Wiley, 2010, selected chapters on heterogeneous catalysis and surface science.
4. G. Ertl,
   "Reactions at Solid Surfaces," Wiley, 2009, Chapter level discussions of catalytic mechanisms.
5. A. Bruix, J. T. Margraf, M. Andersen, K. Reuter,
   "First-principles based multiscale modeling of heterogeneous catalysis,"
   Current Opinion in Chemical Engineering 13 (2016), 149–158.

---

## 2. Position in the BlackHole graph

This block records how Q062 sits inside the BlackHole graph.
All edges are given by Q identifiers and one line reasons that point to concrete components.

### 2.1 Upstream problems

These problems provide prerequisites or structural tools that Q062 relies on.

* Q061 (BH_CHEM_BOND_NATURE_L3_061)
  Reason: Supplies the effective layer description of chemical bonding and active site character in strongly correlated systems, used as input fields for catalyst performance.

* Q064 (BH_CHEM_GLASS_TRANS_L3_064)
  Reason: Provides intuition about rugged energy landscapes and kinetic trapping, reused to describe complex catalytic surfaces and multiple metastable states.

* Q068 (BH_CHEM_PREBIOTIC_NETWORK_L3_068)
  Reason: Encodes general reaction network structures that can be adapted as templates for catalytic cycles and network level design.

### 2.2 Downstream problems

These problems directly reuse Q062 components or depend on its design tension structure.

* Q066 (BH_CHEM_ELECTROCHEM_L3_066)
  Reason: Uses the catalyst design tension functional to analyse electrode materials and interfacial sites in electrocatalysis.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: Reuses the design tradeoff front descriptor to describe self assembled catalytic structures in soft matter.

* Q091 (BH_EARTH_CLIMATE_SENS_L3_091)
  Reason: Reuses catalyst design state fields and tension measures to assess intervention pathways in industrial emission control.

* Q098 (BH_EARTH_ANTHROPOCENE_L3_098)
  Reason: Uses Q062 modules to evaluate how catalyst improvements propagate into large scale Anthropocene system dynamics.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q065 (BH_CHEM_ROOMTC_SUPER_L3_065)
  Reason: Both Q062 and Q065 describe navigation in enormous materials design spaces under thermodynamic_tension with competing objectives.

* Q070 (BH_CHEM_SOFTMATTER_L3_070)
  Reason: Both treat design of complex soft structures with emergent properties governed by local interaction rules and global constraints.

### 2.4 Cross domain edges

Cross domain edges connect Q062 to other domains where its components can be reused.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Links the thermodynamic cost of information processing with the complexity of catalyst design maps and search procedures.

* Q091 (BH_EARTH_CLIMATE_SENS_L3_091)
  Reason: Embeds catalyst design modules into climate relevant process models where catalytic performance shapes emission trajectories.

* Q100 (BH_EARTH_PANDEMIC_RISK_L3_100)
  Reason: Suggests reuse of design tension tools for biocatalysts and enzyme like systems in pharmaceutical synthesis and pathogen control.

All edges reference only Q identifiers. No external identifiers are needed to merge Q062 into a global adjacency list.

---

## 3. Tension Universe encoding (effective layer)

All content in this block stays at the effective layer.
We specify state spaces, observables, invariants, tension scores, and singular sets.
We do not describe how any internal TU fields are generated from raw experimental or computational data.

### 3.1 State space

We assume a semantic state space

```txt
M
```

with the following interpretation.

Each state `m in M` represents a coherent catalyst design world snapshot that includes:

* a finite library of catalyst candidates,

  ```txt
  C(m) = { c_1, c_2, ..., c_N }
  ```

* a finite set of reactions of interest,

  ```txt
  R(m) = { r_1, r_2, ..., r_K }
  ```

* a finite set of operating condition scenarios,

  ```txt
  Env(m) = { e_1, e_2, ..., e_L }
  ```

* summary flags about data quality and model reliability for this world.

We do not specify how this information is built from raw measurements or simulations.
We only require that for each `m in M` the relevant observables defined below are well defined for every
`c in C(m)`, `r in R(m)`, and `e in Env(m)` whenever we say the state is regular.

### 3.2 Effective observables

We introduce effective observables on `M`. All maps below are defined on the regular subset of `M`.

1. Site level energy observable

```txt
E_site(m; c, s, species)
```

* Inputs: state `m`, catalyst candidate `c`, active site label `s`, adsorbed species label.
* Output: effective adsorption or binding energy summary.

2. Step level barrier observable

```txt
E_barrier(m; c, r, step)
```

* Inputs: state `m`, candidate `c`, reaction `r`, elementary step label.
* Output: effective activation barrier summary for that step.

3. Activity observable

```txt
Activity(m; c, r, e)
```

* Inputs: state `m`, candidate `c`, reaction `r`, environment `e`.
* Output: macroscopic activity summary such as turnover frequency or rate per site.

4. Selectivity observable

```txt
Selectivity(m; c, r, e)
```

* Inputs: same as above.
* Output: effective selectivity summary for the desired pathway or product.

5. Stability observable

```txt
Stability(m; c, e)
```

* Inputs: state `m`, candidate `c`, environment `e`.
* Output: summary of deactivation risk such as sintering, poisoning, or dissolution.

6. Design cost observable

```txt
Cost(m; c)
```

* Inputs: state `m`, candidate `c`.
* Output: an effective cost descriptor summarising raw materials, synthesis, and deployment effort.

### 3.3 Descriptor map and admissible encoding class

At the effective layer we assume the existence of descriptor maps and design models but we do not construct them.

1. Descriptor map

```txt
phi(m; c)
```

* Inputs: state `m`, candidate `c in C(m)`.
* Output: descriptor vector in a fixed dimensional space `R^d` with `1 <= d <= d_max`.

The dimension bound `d_max` is fixed as part of the encoding and does not depend on data for a particular world.

2. Admissible descriptor class

We define a class `Phi_adm` of admissible descriptor maps with the following properties.

* Each `phi in Phi_adm` uses only structural and chemical information that is available across the whole library `C(m)`.
* The form of `phi` is fixed by prior modelling choices, not tuned after inspecting performance labels for individual candidates.
* For any state `m` we select a single descriptor map `phi_star(m)` from `Phi_adm`
  before evaluating any tension measures that depend on performance.

3. Response function class

We define a class `F_resp` of admissible response functionals.

```txt
f_resp(phi(c), context) -> predicted_performance
```

where `context` may include reaction `r` and environment `e` labels.
The class `F_resp` is chosen in advance and does not adapt its functional form based on the particular
realisation of measured performance in a given `m`.

These choices prevent trivial encodings that simply interpolate or memorise observed performance
without providing a meaningful design structure.

### 3.4 Mismatch and tension components

We define mismatch components that compare micro level and macro level behaviour.

1. Micro level mismatch

For each state `m` we define a nonnegative scalar

```txt
DeltaS_micro(m)
```

that measures how inconsistent the collection of `E_site` and `E_barrier` values is with any
response function in `F_resp` constructed on top of a descriptor map in `Phi_adm`.

Conceptually:

```txt
DeltaS_micro(m) = min over phi in Phi_adm and f in F_resp of
                  Avg_over_c,r,e of
                  | Activity_model(phi, f; c, r, e) - Activity(m; c, r, e) |
```

where `Activity_model` is the activity predicted from micro observables using the model `f` and descriptors `phi`.
The minimum is taken over the fixed admissible classes and the averaging is over the finite library and contexts.

2. Macro level mismatch

We define

```txt
DeltaS_macro(m)
```

as a nonnegative scalar that measures how inconsistent the observed trade offs
among activity, selectivity, stability, and cost are with a smooth tradeoff front in descriptor space.

Conceptually:

```txt
DeltaS_macro(m) = Avg_over_c of
                  dist( (Activity, Selectivity, Stability, Cost)(m; c, *, *),
                        Pareto_front(phi_star(m; c)) )
```

where `dist` is a nonnegative distance to an ideal tradeoff front defined within the chosen model class.

3. Design front roughness

We define

```txt
DeltaS_front(m)
```

as a nonnegative scalar that measures the roughness or fragmentation of the design landscape in descriptor space.
For example, it can be derived from the number and depth of disconnected high performance basins
relative to a smooth reference landscape.

### 3.5 Combined catalyst design mismatch

We combine the components into a single catalyst design mismatch.

```txt
DeltaS_catalysis(m) =
  w_micro * DeltaS_micro(m) +
  w_macro * DeltaS_macro(m) +
  w_front * DeltaS_front(m)
```

where the weights satisfy:

```txt
w_micro > 0
w_macro > 0
w_front > 0
w_micro + w_macro + w_front = 1
```

The triple `(w_micro, w_macro, w_front)` is fixed once as part of the encoding
and must not be adjusted on a problem by problem basis to hide high tension behaviour.

### 3.6 Tension tensor and singular set

We assume an effective tension tensor on `M` of the form

```txt
T_ij(m) = S_i(m) * C_j(m) * DeltaS_catalysis(m) * lambda(m) * kappa
```

where:

* `S_i(m)` are source like factors for different semantic or physical channels,
* `C_j(m)` are receptivity factors of downstream subsystems,
* `lambda(m)` encodes local convergence state of reasoning,
* `kappa` is a fixed coupling scale for catalyst design tension.

These factors are treated as effective layer summary quantities.
They are not derived from any exposed first principles inside this document.

We define the singular set

```txt
S_sing = { m in M :
           DeltaS_catalysis(m) is undefined
           or at least one required observable is not finite }
```

All analysis of Q062 tension patterns is restricted to the regular domain

```txt
M_reg = M \ S_sing
```

States in `S_sing` are treated as out of domain for Q062, not as evidence about the nature of catalyst design.

---

## 4. Tension principle for this problem

This block describes Q062 as a tension problem at the effective layer.

### 4.1 Core tension functional

We define the core catalyst design tension functional as

```txt
Tension_catalysis(m) = DeltaS_catalysis(m)
```

for all `m in M_reg`.
This is a nonnegative scalar that aggregates:

* mismatch between micro level observables and any compact admissible design model,
* mismatch between observed performance trade offs and smooth tradeoff fronts,
* roughness and fragmentation in the design landscape.

A world snapshot with small `Tension_catalysis(m)` displays a coherent design picture.
A world snapshot with large `Tension_catalysis(m)` reflects a fragmented or contradictory design picture.

### 4.2 Low tension design principle

The low tension design principle can be phrased as:

> In a universe where a general theory of catalyst design exists, there are world states
> that represent realistic catalyst libraries and conditions for which the design tension
> `Tension_catalysis(m)` falls within a narrow, stable low tension band across refinements.

More concretely, consider a sequence of states

```txt
m_1, m_2, ..., m_k, ...
```

where:

* the library `C(m_k)` grows by adding more realistic candidates,
* the set of reactions and environments expands,
* the descriptor map and response models remain inside the same admissible classes.

Then in a low tension design universe we can find such sequences where:

```txt
Tension_catalysis(m_k) <= epsilon_design
```

for all `k`, with a small threshold `epsilon_design` that does not blow up with refinement.

### 4.3 Design failure as persistent high tension

The complementary high tension situation corresponds to a universe where
no compact effective theory of catalyst design is available under the given constraints.

In that case any sequence of increasingly realistic states `m_k` that attempts to remain within
the fixed admissible encoding class will eventually satisfy

```txt
Tension_catalysis(m_k) >= delta_design
```

for some strictly positive `delta_design` that cannot be driven to zero
without either leaving the admissible descriptor and model classes
or performing data dependent manipulations that violate the fairness constraints.

Under persistent high tension:

* micro level and macro level observables fail to be reconciled,
* tradeoff fronts are broken into incompatible patches,
* design rules remain essentially local and case specific.

In the Tension Universe framing of Q062, the open question is whether
our universe behaves more like the low tension or the high tension scenario under reasonable encoding choices.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds at the effective layer.

* World T: a universe with a compact, low tension catalyst design theory.
* World F: a universe where catalyst design remains fundamentally fragmented and high tension.

We only describe patterns of observables and tension, not any deep construction rules.

### 5.1 World T (low tension design universe)

In World T the following properties hold for realistic states in `M_reg`.

1. Compact descriptor success

There exists a descriptor dimension bound `d_max` and an admissible descriptor map class `Phi_adm`
such that, for broad families of catalysts and reactions, a single `phi_star` in `Phi_adm`
enables micro and macro observables to be fit with bounded `DeltaS_micro(m)`.

2. Smooth tradeoff fronts

For many reaction families, performance points `(Activity, Selectivity, Stability, Cost)`
for realistic candidate sets lie close to smooth tradeoff fronts in descriptor space.
The mismatch `DeltaS_macro(m)` remains small even as the library is expanded.

3. Navigable design landscape

Local moves in descriptor space identified by design rules have predictable effects on performance.
Designers can navigate from moderate to high performance regions without repeated random search,
and the landscape roughness `DeltaS_front(m)` stays low.

Overall, states `m_T` that represent realistic design campaigns satisfy

```txt
Tension_catalysis(m_T) <= epsilon_design
```

for a substantial range of libraries, reactions, and conditions.

### 5.2 World F (high tension design universe)

In World F, even with generous admissible encoding classes, the following patterns occur.

1. Descriptor fragmentation

Any attempt to fix a global descriptor map of dimension at most `d_max`
results in large residuals when fitting micro to macro behaviour.
`DeltaS_micro(m_F)` remains large for realistic libraries.

2. Broken tradeoff structure

For new catalyst families and reactions, observed performance points fall into
disconnected phrases of the design space.
Smooth tradeoff fronts that worked for one subset fail badly for another,
and `DeltaS_macro(m_F)` remains large or grows with refinement.

3. Rough landscape and local exceptions

High performance catalysts are isolated and surrounded by steep or irregular regions.
Local rules for improving performance frequently break down,
and the design front roughness `DeltaS_front(m_F)` stays high.

For such states `m_F` we have

```txt
Tension_catalysis(m_F) >= delta_design
```

for a positive `delta_design` that cannot be eliminated without leaving the admissible encoding choices.

### 5.3 Interpretive note

These worlds are counterfactual effective layer scenarios.
They do not claim to describe how microscopic physics generates macroscopic data.
They only encode the patterns that would be observed if a compact design theory exists or fails.

---

## 6. Falsifiability and discriminating experiments

This block describes experiments and protocols that can falsify particular Q062 encodings
without claiming to solve the underlying canonical problem.

### Experiment 1: Finite library descriptor map test

*Goal:*
Test whether a fixed admissible descriptor and response model class can achieve low design tension
across a realistic finite catalyst library for a given reaction family.

*Setup:*

* Input data:

  * A finite library of catalysts `C_data` for a specific reaction under fixed conditions.
  * Measured or reliably computed values of `Activity`, `Selectivity`, `Stability`, and `Cost` for each candidate.

* Encoding choices:

  * A descriptor class `Phi_adm` with dimension bound `d_max`.
  * A response function class `F_resp` constrained to simple function families
    (for example low order polynomials, simple neural networks with fixed architecture).

These encoding choices are fixed before fitting to the dataset.

*Protocol:*

1. For each candidate `c` in `C_data`, select or construct a descriptor `phi(c)`
   within the admissible class `Phi_adm`.

2. Fit a response function `f` in `F_resp` to predict performance summaries
   from the descriptors for all candidates in `C_data`.

3. Compute micro and macro mismatch measures `DeltaS_micro` and `DeltaS_macro`
   on the fitted model for the library, using the definitions of Block 3.

4. Evaluate the combined design mismatch `DeltaS_catalysis` and tension `Tension_catalysis`
   for the state `m_data` representing this library and encoding.

*Metrics:*

* The achieved value of `DeltaS_micro(m_data)`.
* The achieved value of `DeltaS_macro(m_data)`.
* The total `Tension_catalysis(m_data)`.

*Falsification conditions:*

* If for all choices of `phi` and `f` within the fixed admissible classes the quantity
  `Tension_catalysis(m_data)` exceeds a predefined threshold `T_design_max`,
  then the current encoding of low dimensional design for this reaction is rejected at the effective layer.

* If small changes in descriptor or model choices within the admissible classes produce
  arbitrarily different tension values without a corresponding change in predictive performance,
  then the encoding is deemed unstable and is rejected.

*Semantics implementation note:*
All observables and descriptors are treated as continuous fields consistent with the metadata header.
Discrete labels are only used as indices and are not promoted to separate semantics regimes.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.
This experiment can rule out a proposed effective encoding of design tension for a particular setting,
but it does not prove whether a deeper or different general theory exists.

---

### Experiment 2: Cross reaction transfer tension test

*Goal:*
Evaluate whether a single design tension encoding can jointly explain performance
across multiple related reactions using shared descriptors.

*Setup:*

* Input data:

  * A set of catalyst candidates `C_data` active in two or more related reactions
    (for example hydrogen evolution, oxygen reduction, oxygen evolution).
  * Performance summaries for each candidate and reaction under comparable conditions.

* Encoding choices:

  * A shared descriptor class `Phi_adm_shared`.
  * A response function class `F_resp_shared` that allows reaction labels as additional inputs.

These encoding choices are fixed before inspecting relative performance across reactions.

*Protocol:*

1. Choose a shared descriptor map `phi_shared` from `Phi_adm_shared`
   and fit a multi task response model `f_shared` in `F_resp_shared`
   to predict performance for all reactions.

2. Compute `DeltaS_micro` and `DeltaS_macro` for the joint multi reaction state `m_joint`.

3. Independently, fit separate encoding models for each reaction
   that are allowed to have their own descriptors and response functions
   within the same complexity limits.

4. Compute tension values for both the joint and separate encodings.

*Metrics:*

* `Tension_catalysis(m_joint)` for the shared encoding.
* Average of `Tension_catalysis(m_sep_r)` across separate encodings for each reaction `r`.
* A transfer score that compares the joint and separate tension values.

*Falsification conditions:*

* If the joint encoding consistently yields higher tension than all separate encodings
  by a margin larger than a predetermined tolerance for model complexity and noise,
  the claim that a shared low tension design space exists for this reaction set is rejected.

* If the joint encoding attributes low tension to clearly contradictory design stories
  (for example catalysts that switch from very high activity to very low activity
  without a clear change in descriptors), then the encoding is considered misaligned.

*Semantics implementation note:*
All encoding and tension calculations treat the underlying quantities as continuous fields.
The presence of multiple reactions is represented by labels and context variables,
not by switching semantics regimes.

*Boundary note:*
Falsifying TU encoding != solving canonical statement.
This experiment can rule out a particular shared design framework for a given reaction family,
but it does not decide whether some other general theory of catalyst design exists.

---

## 7. AI and WFGY engineering spec

This block describes how Q062 can be used to build and evaluate AI systems
that reason about catalyst design in a structured and tension aware way.

### 7.1 Training signals

We define several training signals that reuse Q062 observables.

1. `signal_activity_tension`

   * Definition: a penalty proportional to `DeltaS_micro(m)`
     when the model's internal explanation of activity contradicts micro observables.
   * Use: encourage the model to maintain alignment between qualitative explanations
     and effective microscopic trends in adsorption and barrier heights.

2. `signal_tradeoff_front_shape`

   * Definition: a penalty that increases when predicted activity, selectivity, stability, and cost
     lie far from a smooth approximated tradeoff front in descriptor space.
   * Use: push the model to represent design trade offs as structured fronts
     instead of isolated maximal points.

3. `signal_descriptor_consistency`

   * Definition: a penalty that grows when the model assigns strongly different internal descriptors
     to the same catalyst under slightly varied prompts or contexts.
   * Use: stabilise internal representations so that downstream tension modules
     see consistent `phi(c)` values.

4. `signal_cross_task_transfer`

   * Definition: a reward signal that increases when a single descriptor and response configuration
     yields low `Tension_catalysis` across several related reactions.
   * Use: explicitly encourage shared design structure when it is possible.

### 7.2 Architectural patterns

We outline module patterns that reuse Q062 components.

1. `CatalystDescriptorLayer`

   * Role: map natural language descriptions, structural encodings, or formulae of catalysts
     into descriptor vectors compatible with the Q062 encoding.
   * Interface:
     Inputs: embedded representation of a catalyst description.
     Output: descriptor vector `phi_model(c)` of fixed dimension `d_model`.

2. `ThermoTensionHead_Catalysis`

   * Role: estimate `DeltaS_catalysis(m)` or its components from internal states.
   * Interface:
     Inputs: aggregated representation of a design world state `m_model`.
     Outputs:

     * scalar approximation to `Tension_catalysis(m_model)`,
     * optional decomposition into `DeltaS_micro`, `DeltaS_macro`, and `DeltaS_front`.

3. `DesignSpaceNavigator`

   * Role: propose local moves in descriptor space that are predicted to reduce tension
     or improve position on the tradeoff front.
   * Interface:
     Inputs: current descriptor vector and context (reaction, constraints).
     Outputs: candidate moves and predicted change in performance and tension.

### 7.3 Evaluation harness

A minimal evaluation harness can proceed as follows.

1. Task definition

   * Collect a set of catalyst design questions that require balancing activity, selectivity, and stability.
   * Include both retrospective tasks (explaining known trends) and forward looking tasks (proposing new ideas).

2. Baseline condition

   * Use a general purpose model without explicit Q062 modules.
   * Evaluate its answers on accuracy of facts, internal consistency of explanations,
     and ability to suggest families of candidates rather than isolated examples.

3. TU condition

   * Use the same base model augmented with `CatalystDescriptorLayer`
     and `ThermoTensionHead_Catalysis`, with training signals as in 7.1.
   * Evaluate on the same tasks.

4. Comparison

   * Metrics may include:

     * qualitative ratings by domain experts,
     * alignment between explanations and micro level descriptors,
     * diversity and structure of proposed candidate sets,
     * the model's estimated tension values.

### 7.4 60 second reproduction protocol

A simple protocol for external users can be:

* Baseline prompt:

  * Ask the model to explain how one would design a better catalyst for a named reaction,
    including how to trade activity against stability and cost.
    No mention is made of tension or Q062.

* TU encoded prompt:

  * Ask the same question but explicitly request the model to:

    * introduce a small set of design descriptors,
    * discuss how microscopic observables constrain these descriptors,
    * describe activity and stability as lying on a tradeoff front,
    * mention how a design tension could be reduced.

* Comparison:

  * Users compare whether the TU encoded answer presents a more structured design space,
    with explicit links between descriptors, micro behaviour, and macro performance.

* Logging:

  * Prompts, full answers, and any exposed tension estimates should be logged
    to allow later inspection and reproducibility checks.

---

## 8. Cross problem transfer template

This block lists reusable components produced by Q062 and where they transfer.

### 8.1 Reusable components produced by this problem

1. ComponentName: `CatalystDesignStateField`

   * Type: field
   * Minimal interface:
     Inputs: descriptions of catalyst candidates, reactions, and environments.
     Output: canonicalised state representation `m_state` with explicit `C(m)`, `R(m)`, `Env(m)` and observables.
   * Preconditions: input information must suffice to populate activity, selectivity, stability, and cost summaries.

2. ComponentName: `ThermodynamicTensionFunctional_Catalysis`

   * Type: functional
   * Minimal interface:
     Inputs: micro mismatch `DeltaS_micro`, macro mismatch `DeltaS_macro`, front roughness `DeltaS_front`.
     Output: scalar `DeltaS_catalysis` and `Tension_catalysis`.
   * Preconditions: the mismatch components are already evaluated on a finite library and context set.

3. ComponentName: `DesignTradeoffFront_Descriptor`

   * Type: observable
   * Minimal interface:
     Inputs: performance summaries and descriptors for a finite set of candidates.
     Output: approximate description of the Pareto like front and local curvature information.
   * Preconditions: performance summaries are available and descriptors are well defined for each candidate.

### 8.2 Direct reuse targets

1. Q066 (BH_CHEM_ELECTROCHEM_L3_066)

   * Reused components: `CatalystDesignStateField`, `ThermodynamicTensionFunctional_Catalysis`.
   * Why it transfers: electrocatalyst design is a special case of catalyst design with additional electrostatic and transport fields.
   * What changes: the observables incorporate potential dependent effects and double layer structure,
     but the design tension structure remains compatible.

2. Q068 (BH_CHEM_PREBIOTIC_NETWORK_L3_068)

   * Reused component: `DesignTradeoffFront_Descriptor`.
   * Why it transfers: prebiotic reaction networks also face trade offs between efficiency, robustness, and resource use.
   * What changes: candidates become network motifs and environmental configurations,
     but the observable is still a tradeoff front in a descriptor space.

3. Q091 (BH_EARTH_CLIMATE_SENS_L3_091)

   * Reused components: `CatalystDesignStateField`, `ThermodynamicTensionFunctional_Catalysis`.
   * Why it transfers: large scale climate interventions require choosing catalytic processes
     that balance emission reduction, stability, and resource constraints.
   * What changes: the cost and stability observables are extended to include system level and policy relevant terms.

---

## 9. TU roadmap and verification levels

### 9.1 Current levels

* E_level: E1

  * A coherent effective layer encoding has been specified for catalyst design tension,
    including state space, observables, mismatch components, and singular set.

* N_level: N1

  * The narrative from micro level to macro level behaviour and tradeoff fronts is explicit,
    and counterfactual worlds have been outlined, but detailed case studies are not yet worked out.

### 9.2 Next measurable step toward E2

To advance Q062 from E1 to E2 the following concrete steps are proposed.

1. Implement at least one realistic finite library experiment as in Experiment 1,
   using an existing dataset for a specific heterogeneous catalytic reaction.

2. Publish the resulting `Tension_catalysis` values and component mismatches
   for several candidate descriptor classes and model forms, including clear falsification outcomes.

3. Repeat the analysis for a second reaction system in order to test whether
   the same descriptor and model classes can plausibly support a shared design space.

These steps remain at the effective layer and do not expose any deeper TU generative rules.
They provide checkable evidence about which encoding choices are viable.

### 9.3 Long term role in the TU program

In the long term, Q062 is expected to serve as:

* the main node for design problems in chemistry within the BlackHole graph,
* a template for similar design tension problems in materials science and biology,
* a benchmark for AI systems that aim to provide structured, tension aware advice
  on complex engineering design under thermodynamic and economic constraints.

If eventually a general theory emerges that keeps `Tension_catalysis` low across many domains,
it would represent a significant shift in how catalyst design is understood and practiced.

---

## 10. Elementary but precise explanation

Catalysts are substances that make chemical reactions go faster or cleaner
without being consumed themselves.
They are essential in energy, environment, and manufacturing technologies.

The hard question is not just how to find one good catalyst.
The hard question is whether there is any general set of rules
that explains why some materials work well and others do not,
across many different reactions and conditions.

In everyday practice, catalyst design often looks like this:

* try a material,
* see how it performs,
* adjust composition or structure,
* repeat many times.

Researchers know many useful tricks,
but those tricks are scattered and do not always fit together.

In the Tension Universe view, we describe the situation differently.

* We imagine a space of possible catalysts and conditions.
* For each point in that space we record what the microscopic behaviour looks like
  (for example how molecules bind and how barriers change),
  and what the macroscopic behaviour looks like
  (activity, selectivity, stability, cost).
* We define a number called design tension that measures how well our
  simple design story fits all these observations at once.

If the design tension is low:

* a small set of design variables explains most of what we see,
* trade offs between performance and stability form smooth fronts,
* moving in the design space changes performance in predictable ways.

If the design tension is high:

* each new catalyst needs its own explanation,
* trends that worked for one family fail for another,
* performance looks like scattered points instead of a structured landscape.

Q062 does not claim that a general theory exists or that it does not.
Instead, it gives a precise way to express that question.

* In a low tension world, there is a compact design theory that works for many systems.
* In a high tension world, even the best possible simple theories break down.

By encoding this distinction at the effective layer, Q062 becomes:

* a reference point for testing design frameworks with real data,
* a shared language for chemists, engineers, and AI systems,
* a source of reusable components for other problems in the BlackHole collection.

This is how the general theory of catalyst design is represented in the Tension Universe
without assuming or revealing any deep generative rules beneath the effective layer.
