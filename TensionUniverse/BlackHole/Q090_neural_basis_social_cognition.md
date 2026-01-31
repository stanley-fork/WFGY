<!-- QUESTION_ID: TU-Q090 -->
# Q090 · Neural basis of social cognition

## 0. Header metadata

```txt
ID: Q090
Code: BH_NEURO_SOC_BRAIN_L3_090
Domain: Neuroscience
Family: social_neuroscience
Rank: S
Projection_dominance: C
Field_type: cognitive_field
Tension_type: cognitive_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N1
Last_updated: 2026-01-31
```

---

## 0. Effective layer disclaimer and scope

All statements in this entry are made strictly at the **effective layer** of the Tension Universe (TU) framework.

* We only describe **state spaces, observables, fields, tension functionals and counterfactual worlds** at an effective layer.
* We do **not** introduce any new axiom system, deep generative rule or constructive definition of TU itself.
* We do **not** provide any explicit mapping from raw biological measurements or personal data to internal TU fields.
  We only assume the existence of encoding families that are consistent with the TU Charters.
* We do **not** claim to solve the canonical scientific question in Section 1.
  This page only specifies an encoding of that question as an effective layer tension problem.
* We do **not** claim any new theorem or proof in mathematics, neuroscience or AI.
  All scientific claims remain within the scope of cited literature and standard methods.
* We do **not** provide any clinical diagnosis, mental health evaluation or judgment about individuals.
  Tension quantities defined here are abstract observables on states, not scores on people.

This entry should be interpreted as a **candidate encoding pattern** for the neural basis of social cognition.
It is governed by the TU Effective Layer, Encoding and Tension Scale Charters.
Concrete implementations must respect those Charters, including fairness, preregistration and audit requirements.

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical question is:

> What concrete neural systems and circuit level mechanisms in the brain support social cognition, and how do they coordinate to generate stable, flexible social understanding of self and others?

In this context:

* **Social cognition** includes:

  * inferring others' mental states,
  * understanding intentions, beliefs and desires,
  * empathy and affective sharing,
  * processing social norms and roles,
  * predicting others' behavior.

* **Neural basis** refers to:

  * identifiable brain regions and networks,
  * effective connectivity between them,
  * local circuit motifs that implement computations relevant for social cognition.

The problem is not only to list regions. It is to explain how:

1. Large scale social brain networks
   such as medial prefrontal, temporo parietal, superior temporal, anterior temporal, amygdala, striatum and insula systems organize over time.
2. Local microcircuit motifs support the computations implied by social tasks.
3. These multiscale structures jointly realize robust, context sensitive social cognition in healthy individuals.

In this entry we treat the question as an effective layer tension problem.
We describe observables and fields that summarize social brain structure and function, and we define a social tension functional that can be probed and falsified.
We do not specify any deep TU mechanism.

### 1.2 Status and difficulty

The state of knowledge can be summarized as follows.

1. **Social brain networks**

   Lesion studies, functional imaging and electrophysiology show that social cognition recruits a distributed set of regions, including:

   * medial prefrontal cortex,
   * temporo parietal junction,
   * posterior superior temporal sulcus,
   * anterior temporal cortex,
   * amygdala and connected limbic circuits,
   * striatal and orbitofrontal value systems,
   * insula and salience related regions.

   These systems show selective engagement during tasks that involve thinking about others, understanding narratives or evaluating social outcomes.

2. **Partial computational hypotheses**

   Multiple computational hypotheses have been proposed, such as:

   * predictive coding of others' actions and mental states,
   * hierarchical generative models of agents and groups,
   * value based learning of social norms and reputations,
   * graph like internal models of social networks.

   These hypotheses connect some local circuit motifs and global network patterns to social behaviors, but none is complete or universally accepted.

3. **Gaps and open aspects**

   Key difficulties remain:

   * how large scale coordination among social networks is organized across time scales,
   * how social and non social computations share or compete for neural resources,
   * how individual differences in social cognition emerge from variations in structure and plasticity,
   * how developmental, aging or disease related changes produce specific social cognitive profiles.

The problem is therefore open and multiscale.
It is unlikely to admit a single simple solution, but it is still meaningful to encode it as a structured effective layer question.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q090:

1. Serves as the central node for social cognition inside the neuroscience cluster.
2. Connects micro level coding and plasticity encodings to macro level social behavior and AI social agents.
3. Provides a template for expressing **cognitive_tension** between internal social models and external social realities.
4. Supplies reusable components for AI and multi agent governance problems that need biologically informed social reasoning models.
5. Acts as a reference pattern for any TU encodings that involve social brain networks, empathy related signals or social prediction tasks.

---

## 2. Position in the BlackHole graph

This block records how Q090 sits in the BlackHole graph.
All edges use one line reasons that point to concrete components or tension types.
Codes for other problems are shown for adjacency and may be refined elsewhere.

### 2.1 Upstream problems

These nodes provide prerequisites or general tools that Q090 reuses.

* Q083 (`BH_NEURO_NEURAL_CODING_L3_083`)
  Reason: Supplies general neural coding principles reused when defining SocialGraphField and social feature observables.

* Q084 (`BH_NEURO_LTM_STORAGE_L3_084`)
  Reason: Provides long term memory storage mechanisms used for stable person specific and group specific social representations.

* Q085 (`BH_NEURO_PLASTICITY_RULES_L3_085`)
  Reason: Contributes plasticity rules that underlie social learning and updates to internal social models.

* Q089 (`BH_NEURO_PREDICTIVE_CODE_L3_089`)
  Reason: Gives predictive coding implementation patterns extended here to social predictive circuits and social prediction errors.

### 2.2 Downstream problems

These nodes directly reuse Q090 components or depend on its tension structure.

* Q121 (`BH_AI_SOCIAL_AGENTS_L3_121`)
  Reason: Reuses SocialGraphField and SocialTensionFunctional_Soc to design AI agents with engineered social cognition modules.

* Q122 (`BH_AI_MULTI_AGENT_GOVERN_L3_122`)
  Reason: Uses Q090 social tension observables to formulate norms and governance rules in multi agent systems.

* Q111 (`BH_SOC_COLLECTIVE_BEHAVIOR_L3_111`)
  Reason: Imports SocialGraphField and EmpathyChannelFilter to model collective social dynamics and belief flows.

### 2.3 Parallel problems

Parallel nodes share similar tension types but do not reuse specific components.

* Q081 (`BH_NEURO_CONSCIOUS_HARD_L3_081`)
  Reason: Both study subjective and higher order cognition under cognitive_tension, but Q081 focuses on consciousness rather than social content.

* Q089 (`BH_NEURO_PREDICTIVE_CODE_L3_089`)
  Reason: Both rely on predictive circuits, yet Q089 stays content agnostic while Q090 specializes prediction for social signals and agents.

* Q087 (`BH_NEURO_NEURODEGEN_L3_087`)
  Reason: Both involve large scale network degradation patterns, with Q087 focused on disease progression and Q090 on resulting social cognitive changes.

### 2.4 Cross domain edges

Cross domain edges connect Q090 to problems in other clusters.

* Q059 (`BH_CS_INFO_THERMODYN_L3_059`)
  Reason: Reuses tension between internal models and external outcomes to quantify social information bottlenecks and cognitive costs.

* Q123 (`BH_AI_INTERP_L3_123`)
  Reason: Uses SocialRepresentationProbe from Q090 as a template for probing social concepts inside AI representations.

* Q032 (`BH_PHYS_QTHERMO_L3_032`)
  Reason: Adapts the idea of multiscale field interactions and effective temperature to social brain fields and cognitive load measures.

All references to Q numbers here are adjacency only.
No external URLs appear in this block.
The full graph can be assembled as a simple adjacency list.

---

## 3. Tension Universe encoding (effective layer)

In this block we specify how Q090 is encoded at the effective layer.
The encoding is consistent with:

* `Field_type: cognitive_field`
* `Tension_type: cognitive_tension`
* `Semantics: hybrid`

Hybrid semantics means that:

* some observables are continuous valued fields over regions or tasks,
* some observables are discrete graph structures,
* all of them are combined into a unified but finite dimensional representation.

### 3.1 State space and parameter space

We assume a semantic state space

```txt
M
```

with the following interpretation.

* Each state `m` in `M` represents a coherent social brain configuration for a single individual at a chosen time scale.
* A configuration `m` encodes summaries of:

  * activity levels in key social brain subsystems,
  * effective connectivity among these subsystems,
  * latent variables that describe internal social models of self, others and groups,
  * current social context class such as cooperative, competitive or neutral.

We assume the existence of a finite dimensional parameter space

```txt
Par_SOC subset of R^k
```

such that every state `m` can be represented by at least one point

```txt
theta(m) in Par_SOC
```

for some finite `k`.
We do not specify the value of `k`, the coordinates of `Par_SOC` or any explicit mapping `m -> theta(m)`.
We only require that:

* `Par_SOC` is fixed for a given encoding,
* the mapping is measurable and depends only on observable data that are allowed by the TU Charters.

No TU axiom or deep generative rule is introduced at this step.

### 3.2 Effective observables and fields

We define the following effective observables on `M`.

1. **Social activity field**

   ```txt
   SocActivity(m; R_set) >= 0
   ```

   * Input: state `m` and a finite set of regions or parcels `R_set` in a predefined social brain atlas.
   * Output: a vector of nonnegative values summarizing activity in each region, for example normalized amplitudes or rates.
   * Interpretation: captures how strongly each social subsystem is engaged in the current configuration.

2. **Social connectivity observable**

   ```txt
   SocConn(m; R_pair)
   ```

   * Input: state `m` and an ordered pair of regions `R_pair`.
   * Output: an effective connectivity value that summarizes influence from the first region to the second in the present configuration.
   * Interpretation: encodes directed or undirected functional coupling among social subsystems.

3. **Social model descriptor**

   ```txt
   SocModel(m)
   ```

   * Input: state `m`.
   * Output: a low dimensional descriptor vector summarizing:

     * internal beliefs about others' traits and intentions,
     * internal beliefs about group norms and roles,
     * internal beliefs about self in the current social context.
   * Interpretation: a compact code for the internal social generative model at that moment.
     We only assume such a descriptor exists and fits in `Par_SOC`.

4. **Social prediction error observable**

   ```txt
   SocPredErr(m; C_task) >= 0
   ```

   * Input: state `m` and a task or context label `C_task` that belongs to a finite family of social tasks.
   * Output: a nonnegative scalar summarizing mismatch between predicted and observed social cues or outcomes in that context.
   * Interpretation: aggregates social error signals across relevant circuits, without exposing any micro level update rules.

These observables already reflect **hybrid semantics**.
Region and task sets are discrete, values are continuous, and the combination is finite dimensional.

### 3.3 Social graph field

We combine activity and connectivity into a single field.

```txt
SocialGraphField(m)
```

* Input: state `m`.
* Output: a structured object that consists of:

  * a list of nodes for the selected social brain regions,
  * node features derived from `SocActivity(m; R_set)` and `SocModel(m)`,
  * edge features derived from `SocConn(m; R_pair)`.

`SocialGraphField` is defined only at the level of summaries.
We do not specify how neural signals are transformed into these quantities or how the atlas is chosen.
Any concrete choice must obey the TU Encoding and Fairness Charter.

### 3.4 Tension related quantities

We define two primary mismatch observables and a combined social tension.

1. **Structural mismatch**

   ```txt
   DeltaS_soc_struct(m) >= 0
   ```

   * Measures how far `SocialGraphField(m)` deviates from a reference class of healthy social network architectures, after normalizing for age and global brain size.
   * Properties:

     * `DeltaS_soc_struct(m) = 0` if `SocialGraphField(m)` falls exactly inside the reference class.
     * Larger values indicate greater deviation in connectivity patterns or subsystem balance.

2. **Predictive mismatch**

   ```txt
   DeltaS_soc_pred(m) >= 0
   ```

   * Measures how far `SocPredErr(m; C_task)` deviates from a reference pattern of low social prediction error across tasks.
   * Properties:

     * `DeltaS_soc_pred(m) = 0` if social prediction errors match the reference low tension profile.
     * Larger values indicate persistent or widespread social prediction errors.

3. **Combined social tension**

   For fixed positive weights chosen in advance, we define:

   ```txt
   DeltaS_SOC(m) = w_struct * DeltaS_soc_struct(m)
                 + w_pred   * DeltaS_soc_pred(m)
   ```

   with

   ```txt
   w_struct > 0
   w_pred   > 0
   w_struct + w_pred = 1
   ```

   We will often write

   ```txt
   Tension_SOC(m) = DeltaS_SOC(m)
   ```

   to emphasize that `DeltaS_SOC` is the core social tension functional for Q090.
   No distinct second functional is introduced.

Weights are fixed for all evaluations within a given study and must obey the encoding library rules in Section 3.6.
They cannot be tuned after seeing outcome data.

### 3.5 Singular set and regular domain

Some configurations may make `DeltaS_SOC` undefined or misleading, for example when data are missing, contradictory or outside the calibration range.

We define a singular set:

```txt
S_sing = {
  m in M :
  DeltaS_soc_struct(m) is undefined or infinite
  or DeltaS_soc_pred(m)   is undefined or infinite
}
```

We restrict our main analysis to the regular domain:

```txt
M_reg = M \ S_sing
```

Handling of the singular set:

* States in `S_sing` are treated as **out of domain** for Q090 tension analysis.
* They may still appear in data quality checks or encoding diagnostics.
* Experiments must report how many data derived states fall in `S_sing` and how they were handled.

### 3.6 Encoding libraries and registry

To keep encodings finite and auditable, we introduce explicit encoding libraries and a registry, in line with the TU Encoding and Fairness Charter.

1. **Structural encoding library**

   ```txt
   Lib_SOC_struct = { E_struct_1, ..., E_struct_K }
   ```

   Each `E_struct_k` specifies:

   * a reference class of healthy social architectures,
   * a distance or divergence measure on `SocialGraphField`,
   * a normalization rule for age and brain scale.

   Together these define one concrete version of `DeltaS_soc_struct`.

2. **Predictive encoding library**

   ```txt
   Lib_SOC_pred = { E_pred_1, ..., E_pred_L }
   ```

   Each `E_pred_l` specifies:

   * a reference low tension profile for social prediction errors across a finite task family,
   * an aggregation rule that maps `SocPredErr(m; C_task)` values into a scalar `DeltaS_soc_pred(m)`.

3. **Weight library**

   ```txt
   Lib_SOC_weights = {
     (w_struct, w_pred) :
     w_struct > 0, w_pred > 0, w_struct + w_pred = 1,
     w_struct >= w_min_struct, w_pred >= w_min_pred
   }
   ```

   where `w_min_struct`, `w_min_pred` are fixed lower bounds strictly between zero and one half.
   `Lib_SOC_weights` is finite.

4. **Encoding registry**

   An encoding element for Q090 is a triple

   ```txt
   E_SOC = (E_struct_k, E_pred_l, (w_struct, w_pred))
   ```

   with `E_struct_k` in `Lib_SOC_struct`, `E_pred_l` in `Lib_SOC_pred`, and `(w_struct, w_pred)` in `Lib_SOC_weights`.

   We collect admissible encodings in a finite registry

   ```txt
   Registry_SOC = { E_SOC_1, ..., E_SOC_R }
   ```

5. **Fairness and preregistration rule**

   For any empirical study or AI evaluation that uses Q090:

   * The experimenter must **preselect** a single encoding element `E_SOC_r` from `Registry_SOC` before looking at outcome data.
   * All tension computations in that study must use the same `E_SOC_r`.
   * Comparing different encoding elements requires separate preregistered runs, each with its own logs.

Experiments in Section 6 must report which `E_SOC_r` was used and how it was chosen.

---

## 4. Tension principle for this problem

This block states how Q090 is characterized as a tension problem in the TU sense.

### 4.1 Core social tension functional

The core social tension functional is

```txt
Tension_SOC(m) = DeltaS_SOC(m)
```

for `m` in `M_reg`.
It is a nonnegative scalar that summarizes:

* mismatch between actual social brain structure and the chosen reference architecture class,
* mismatch between social prediction performance and the chosen low tension profile.

Required properties:

* `Tension_SOC(m) >= 0` for all `m` in `M_reg`.
* `Tension_SOC(m)` is small if both mismatch terms are small.
* `Tension_SOC(m)` becomes large when either structural or predictive mismatch grows.

No claim is made that the true brain implements any particular optimization of `Tension_SOC`.
Q090 only states that this functional is a useful observable for organizing data and models.

### 4.2 Low tension social brain principle

At the effective layer, the low tension principle for Q090 is:

> For typical individuals in typical social environments, there exist configurations `m` in `M_reg` where `Tension_SOC(m)` remains within a narrow band across a broad range of everyday social contexts.

More concretely, for a chosen encoding `E_SOC_r` in `Registry_SOC` and a finite set of social tasks and contexts, we expect that for many individuals:

```txt
Tension_SOC(m) <= epsilon_SOC
```

for states `m` that represent well practiced or well understood social situations.
The threshold `epsilon_SOC` depends on measurement noise and modeling precision but should not grow without bound as better data become available.

### 4.3 Persistent high tension social brain patterns

Conversely, persistent high tension patterns arise when no configuration in `M_reg` can keep `DeltaS_SOC` small across core social domains.

At the effective layer we state:

> If structural and predictive properties of the social brain are sufficiently misaligned with reference patterns in a given encoding, then any realistic sequence of configurations will yield `Tension_SOC(m)` that exceeds a positive lower bound on a substantial subset of social contexts.

Formally, for a chosen encoding `E_SOC_r` in `Registry_SOC` there can exist a value `delta_SOC > 0` such that for all configurations `m` in a certain subset of `M_reg` that represent particular individuals and contexts,

```txt
Tension_SOC(m) >= delta_SOC
```

on a nontrivial set of tasks.
This expresses **persistent cognitive tension** rather than a transient fluctuation.

Q090 does not claim which pattern is realized for any given person.
It only codifies how to describe and measure these possibilities in a way that is compatible with falsification and fairness.

---

## 5. Counterfactual tension worlds

We now describe two counterfactual worlds, entirely at the effective layer.

* World T: typical social brains with low sustained social tension.
* World F: social systems where misalignments produce persistent high social tension.

These worlds are characterized by observable patterns.
No hidden Tension Universe generative rules are exposed.

### 5.1 World T (low social tension world)

In World T:

1. **Structural robustness**

   * For most individuals, `SocialGraphField(m)` stays close to the reference architecture class during development and adulthood.
   * Redundancy and alternative pathways allow the network to absorb moderate perturbations without large increases in `DeltaS_soc_struct`.

2. **Efficient social prediction**

   * `SocPredErr(m; C_task)` is typically small for frequently encountered social contexts.
   * Learning reduces social prediction errors over time, and `DeltaS_soc_pred` remains bounded even in moderately novel situations.

3. **Cross subsystem coherence**

   * Activity in mentalizing, mirroring, value and salience subsystems tends to form coherent patterns during social interactions.
   * Conflicts among goals, norms and empathic responses are resolved over time without leaving long term high `Tension_SOC`.

4. **Gradual adaptation**

   * When environments change, individuals can move through sequences of states `m` that adjust `SocialGraphField` and `SocModel` while keeping `Tension_SOC` under moderate control.

### 5.2 World F (high social tension world)

In World F:

1. **Structural misalignment**

   * For certain individuals or populations, `SocialGraphField(m)` systematically deviates from the reference architecture in ways that simple plasticity cannot compensate.
   * `DeltaS_soc_struct` stays large across many configurations, indicating chronic network level misalignment.

2. **Persistent prediction error**

   * `SocPredErr(m; C_task)` remains high even after extended experience with common social situations.
   * `DeltaS_soc_pred` does not decrease with learning, or decreases only in narrow situations while staying high elsewhere.

3. **Cross subsystem conflict**

   * Activity patterns in different social subsystems are frequently incompatible, for example strong value signals for one action combined with strong empathic signals for another.
   * As a result, `Tension_SOC(m)` is often above a nonzero lower bound in important social contexts.

4. **Fragile compensation**

   * Some configurations may temporarily reduce `Tension_SOC` in narrow contexts, but small changes in context or network parameters cause tension to rise again.
   * There is no broad region of `M_reg` where social tension remains low across diverse social interactions.

### 5.3 Interpretive note

These worlds neither categorize real individuals nor diagnose any condition.
They are abstract models that:

* help classify patterns of observables,
* guide the design of experiments,
* provide structure for AI architectures inspired by social brain organization.

They make no claim about the prevalence of any particular pattern in real populations.

---

## 6. Falsifiability and discriminating experiments

Experiments in this block test **Q090 encodings**, not human beings.
They can falsify specific choices of observables, reference classes or parameter ranges.
They cannot prove or disprove any fundamental truth about social cognition.

Concrete implementations must:

* pick an encoding `E_SOC_r` from `Registry_SOC`,
* define how to construct data derived states `m_data`,
* specify how `S_sing` and `M_reg` are used.

### Experiment 1: Social prediction tension mapping

**Goal**

Test whether the defined `Tension_SOC(m)` functional tracks social prediction difficulty across tasks and individuals in a stable way.

**Setup**

* Participants:

  * a group of adults with typical social functioning,
  * one or more comparison groups with well characterized social cognitive challenges, where inclusion respects ethical and clinical standards.
* Tasks:

  * a battery of social prediction tasks and matched non social control tasks, each labeled with a context tag `C_task`.
* Data:

  * non invasive measurements that allow construction of SocialGraphField like summaries,
  * behavioral measures that allow construction of `SocPredErr`.

**Protocol**

1. **Encoding selection**

   * Choose a single encoding element `E_SOC_r` in `Registry_SOC` before looking at group differences.
   * Record the choice and the date in an audit log.

2. **State construction**

   * For each participant, task and measurement session, construct a state `m_data` that encodes:

     * `SocActivity` summaries for key social regions,
     * `SocConn` summaries for selected pairs of regions,
     * `SocModel` summaries for self and other representations,
     * `SocPredErr` derived from behavioral performance.

   The construction procedure uses standard neuroimaging and behavioral analysis pipelines and must be documented outside TU language.
   Q090 does not prescribe any particular pipeline.

3. **Tension computation**

   * For each `m_data`, compute:

     * `DeltaS_soc_struct(m_data)` by applying the structural part of `E_SOC_r`,
     * `DeltaS_soc_pred(m_data)` by applying the predictive part of `E_SOC_r`,
     * `Tension_SOC(m_data) = DeltaS_SOC(m_data)`.

4. **Domain restriction**

   * Identify states `m_data` that fall in `S_sing`.
   * Exclude these from tension distribution analyses.
   * Keep them only for data quality and encoding diagnostics.

5. **Analysis**

   * Analyze how `Tension_SOC` distributions differ:

     * between social and non social tasks,
     * between participant groups,
     * across repeated measurements and small perturbations of analysis choices that stay within `E_SOC_r`.

**Metrics**

* Distribution of `Tension_SOC` across tasks and individuals.
* Correlation between `Tension_SOC` and observed social prediction error at the behavioral level.
* Stability of `Tension_SOC` when measurement noise or analysis pipelines are slightly varied within the same encoding.

**Falsification conditions**

* If no reasonable choice of `E_SOC_r` in `Registry_SOC` yields a robust positive correlation between `Tension_SOC` and behavioral social prediction error across individuals and tasks, then the current encoding registry for Q090 is considered falsified or incomplete.
* If small, methodologically justified changes in the construction of `m_data` inside the same `E_SOC_r` produce arbitrarily different `Tension_SOC` patterns for the same participants and tasks, the encoding is judged unstable and rejected or revised.

**Domain note**

* States in `S_sing` must not be included in group comparisons of `Tension_SOC`.
* The fraction of states that fall in `S_sing` is itself a diagnostic of encoding quality and data quality.

**Audit trace requirements**

An implementation of Experiment 1 must log at least:

* the chosen encoding `E_SOC_r` and its components from `Lib_SOC_struct`, `Lib_SOC_pred` and `Lib_SOC_weights`,
* the number of constructed states, the size of `S_sing` and the size of `M_reg`,
* summary statistics of `Tension_SOC` by group and task,
* the specification of all analysis pipelines used to construct `m_data`,
* any deviations from preregistered plans and their rationale.

These logs should be sufficient for an independent group to reproduce the main tension distributions.

---

### Experiment 2: Network perturbation and compensation pattern

**Goal**

Evaluate whether Q090 encodings can predict structured changes in `Tension_SOC` under targeted perturbations of social brain networks.

**Setup**

* Data sources:

  * lesion studies,
  * naturally occurring focal brain injuries,
  * or ethically acceptable perturbation methods that modulate activity in social brain regions.
* Regions of interest:

  * key nodes in `SocialGraphField`, such as medial prefrontal cortex or temporo parietal junction.

**Protocol**

1. **Encoding selection**

   * Choose a single encoding element `E_SOC_r` in `Registry_SOC` before comparing perturbed and comparison groups.
   * Record this choice in the audit log.

2. **Group definition**

   * Identify a set of individuals with focal perturbations in specific social brain regions.
   * Identify matched comparison individuals without such perturbations, controlled for age and other factors.

3. **State construction**

   * For each individual and a set of social tasks, construct states `m_pre`, `m_post` or matched `m_pert`, `m_ctrl` that represent:

     * configurations before and after perturbation, or
     * configurations in perturbed and non perturbed groups.

4. **Tension computation and domain restriction**

   * For each state, compute:

     * `DeltaS_soc_struct` and `DeltaS_soc_pred`,
     * `Tension_SOC` using the chosen `E_SOC_r`.
   * Identify states that fall into `S_sing` and treat them as out of domain for tension analysis, as in Experiment 1.

5. **Analysis**

   * Analyze:

     * whether perturbations produce systematic shifts in `Tension_SOC` in the expected directions,
     * whether evidence of compensation in other regions reduces `Tension_SOC` in some contexts,
     * whether changes are specific to social tasks or also appear in non social controls.

**Metrics**

* Change in `Tension_SOC` associated with perturbation, by task and group.
* Task dependence of tension changes across social and non social conditions.
* Degree of compensation indicated by partial recovery of `Tension_SOC` toward baseline over time or across conditions.

**Falsification conditions**

* If perturbations that strongly affect known social brain hubs do not produce any structured changes in `Tension_SOC` beyond noise, for any encoding element in `Registry_SOC`, then the current Q090 encoding scheme is misaligned with social brain physiology.
* If `Tension_SOC` suggests large tension shifts in contexts where behavior and standard imaging show minimal changes, the corresponding encoding element is considered inconsistent and should be rejected or revised.

**Domain note**

* As in Experiment 1, states in `S_sing` must be explicitly identified and excluded from tension statistics.
* The dependence of `S_sing` on perturbation condition is itself a possible indicator of encoding problems.

**Audit trace requirements**

An implementation of Experiment 2 must log at least:

* the chosen encoding `E_SOC_r` from `Registry_SOC`,
* the definition of perturbed and comparison groups and inclusion criteria,
* the construction pipeline for `m_pre`, `m_post` or `m_pert`, `m_ctrl`,
* distributions of `Tension_SOC` and their changes by group and task,
* summary of how many states entered `S_sing` and how they were handled.

As before, logs should be sufficient for independent verification.

---

## 7. AI and WFGY engineering spec

This block shows how Q090 becomes an engineering module for AI systems, without revealing any deep Tension Universe rules.
The goal is to reuse the same observables and tension functionals as internal diagnostics or training signals.

### 7.1 Training signals

We consider four training related signals inspired by Q090.

1. **`signal_social_prediction_error`**

   * Definition: a scalar signal proportional to `DeltaS_soc_pred` for model internal states that represent social prediction tasks.
   * Purpose: encourage models to form internal states that reduce social prediction mismatch when the task requires accurate social forecasting.

2. **`signal_social_consistency`**

   * Definition: a signal derived from internal consistency between different parts of a model representation that correspond to self, others and groups, modeled on `SocModel` and `SocialGraphField` structure.
   * Purpose: penalize internal states where representations of others and groups are strongly incompatible with past commitments in contexts that should be stable.

3. **`signal_empathic_alignment`**

   * Definition: a signal that measures alignment between value like representations for self and inferred value like representations for relevant others under cooperative contexts.
   * Purpose: support the ability to reason about cooperative outcomes while keeping social cognitive tension moderate.

4. **`signal_social_tension_score`**

   * Definition: a direct analogue of `Tension_SOC` for internal model states, computed by a dedicated head that estimates structural and predictive mismatch according to a selected encoding element `E_SOC_r`.
   * Purpose: act as an auxiliary loss that keeps social reasoning modules within a low tension regime for scenarios designated as typical.

All these signals must be implemented using only Q090 style observables and encodings.
They must not introduce hidden scoring rules that conflict with the TU Encoding and Fairness Charter.

### 7.2 Architectural patterns

We sketch three architectural patterns for AI models.

1. **`SocialCognitionHead`**

   * Role: a module attached to a general purpose model that reads latent states and outputs:

     * an estimate of SocialGraphField like structure,
     * an estimate of SocModel like descriptors,
     * an estimate of `Tension_SOC`.
   * Interface:

     * Inputs: internal hidden states or embeddings for social scenarios.
     * Outputs: structured summaries and a scalar tension value.
   * Use: training with Q090 style signals or as a diagnostic head in evaluation.

2. **`SocialGraphEncoder`**

   * Role: a module that encodes interaction graphs, roles and observed social cues into a representation compatible with `SocialGraphField`.
   * Interface:

     * Inputs: descriptions of agents, their relations and recent interactions.
     * Outputs: graph structured embeddings with node and edge features.
   * Use: front end for models that need explicit social structure.

3. **`EmpathyChannelFilter`**

   * Role: a mechanism that compares predicted outcomes for self and others and gauges mismatches similar to empathic tension.
   * Interface:

     * Inputs: separate channels for self related and other related value estimates.
     * Outputs: a discrepancy score that can be incorporated into `signal_empathic_alignment`.
   * Use: constrain models to treat cooperative contexts with bounded mismatch between self and other value channels.

### 7.3 Evaluation harness

A harness for assessing models that use Q090 modules can include:

1. **Tasks**

   * Social scenario understanding:

     * narratives or dialogues where models must infer beliefs, intentions and social roles.
   * Social prediction tasks:

     * forecasting likely actions of agents given their history and context.
   * Social norm reasoning:

     * judging appropriateness of actions under explicit or implicit norms.

2. **Conditions**

   * Baseline condition:

     * model runs without any Q090 specific modules or signals.
   * TU condition:

     * model uses `SocialCognitionHead`, `SocialGraphEncoder` and Q090 training signals as auxiliaries.

3. **Metrics**

   * Task performance measures:

     * accuracy in predictions,
     * consistency of explanations,
     * calibration of uncertainty.
   * Internal social tension measures:

     * average estimated `Tension_SOC` across tasks where low tension is expected.
   * Robustness to prompt variations:

     * stability of inferred social structures and explanations under controlled paraphrases.

### 7.4 Social safety boundary

Because Q090 concerns social cognition, there is a risk that tension measures could be misused as scores on real people.
To keep the framework within scientific and ethical bounds, we impose the following effective layer safety boundary.

* Q090 encodings, observables and tension quantities must **not** be used to:

  * label real individuals as socially good or bad,
  * rank or filter people for employment, access, rights or opportunities,
  * assign any moral or legal status.

* Q090 based modules in AI systems may be used to:

  * study internal reasoning patterns,
  * analyze model robustness and fairness,
  * design better architectures for social understanding.

* They should **not** be used as a black box decision score for high stakes applications.
  Any deployment that touches real people must include additional domain specific safeguards well beyond this entry.

This boundary is part of the TU Effective Layer Charter.
Violating it falls outside the permitted scope of Q090.

### 7.5 60 second reproduction protocol

A minimal procedure can help users observe the effect of Q090 framing in an AI system.

* **Baseline setup**

  * Prompt the model:

    * "Explain how the human brain supports social cognition and understanding of others."
  * Record the answer and any intermediate representations that are observable.
  * Typical issues:

    * scattered lists of regions,
    * vague descriptions of mental processes,
    * limited structural clarity.

* **TU encoded setup**

  * Prompt the model with an additional instruction:

    * "Organize your explanation around social brain networks, internal social models and social tension between prediction and outcome, using an explicit notion similar to `Tension_SOC` at the effective layer."

  * If available, request the model to output:

    * its estimated social brain structure summary,
    * an estimate of social tension for example scenarios,
    * any graph or field summaries that correspond to `SocialGraphField` and `SocModel`.

* **Comparison metric**

  * Rate:

    * structural clarity,
    * explicit linkage between networks, internal models and behavior,
    * consistency across repeated questions.

  * Compare how often the TU encoded setup yields explanations that can be mapped directly to Q090 observables.

* **What to log**

  * Prompts and full responses,
  * any auxiliary quantities the model reports that correspond to Q090 observables or `Tension_SOC`,
  * settings of any model flags that enable or disable Q090 inspired modules.

These logs allow third parties to inspect whether Q090 framing produces stable and interpretable patterns.
They do not certify correctness but provide a reproducible target.

---

## 8. Cross problem transfer template

This block lists reusable components and direct reuse targets.

### 8.1 Reusable components produced by this problem

1. **ComponentName: `SocialGraphField`**

   * Type: field
   * Minimal interface:

     * Inputs:

       * a set of brain regions or abstract agent units,
       * measures of activity and connectivity,
       * role or context labels.
     * Output:

       * a structured representation that combines node and edge features into a graph like object.
   * Preconditions:

     * the region set or agent set is finite and indexed,
     * activity and connectivity summaries are well defined and finite.

2. **ComponentName: `SocialTensionFunctional_Soc`**

   * Type: functional
   * Minimal interface:

     * Inputs:

       * SocialGraphField like structure,
       * social prediction summary data.
     * Output:

       * a nonnegative scalar tension value `DeltaS_SOC(m)` and an optional vector of component wise mismatches.
   * Preconditions:

     * reference architecture class and reference prediction profile are specified before evaluation,
     * weight parameters `(w_struct, w_pred)` are taken from `Lib_SOC_weights` and fixed ahead of time.

3. **ComponentName: `SocialRepresentationProbe`**

   * Type: experiment_pattern
   * Minimal interface:

     * Inputs:

       * a model class (biological or artificial),
       * a set of social tasks.
     * Output:

       * an experimental protocol that maps internal states to Q090 observables and computes `Tension_SOC` without altering the underlying model.

### 8.2 Direct reuse targets

1. **Q089 (`BH_NEURO_PREDICTIVE_CODE_L3_089`)**

   * Reused component:

     * `SocialTensionFunctional_Soc`.
   * Why it transfers:

     * Q089 studies predictive coding implementations in general.
     * `SocialTensionFunctional_Soc` gives a concrete way to assess how well predictive architectures handle social content.
   * What changes:

     * the internal predictive circuits vary,
     * the functional applied to their observable summaries remains the same.

2. **Q121 (`BH_AI_SOCIAL_AGENTS_L3_121`)**

   * Reused components:

     * `SocialGraphField`,
     * `SocialRepresentationProbe`.
   * Why it transfers:

     * Q121 builds AI agents with explicit social modules that can be structured and audited with the same graph and probe patterns.
   * What changes:

     * physical brain regions are replaced by abstract agent components,
     * the interface of the field and the probe stays identical.

3. **Q123 (`BH_AI_INTERP_L3_123`)**

   * Reused component:

     * `SocialRepresentationProbe`.
   * Why it transfers:

     * Q123 needs standardized protocols for probing internal representations of AI systems for social concepts and roles.
   * What changes:

     * the underlying models are artificial networks,
     * the observable mapping and tension evaluation follow Q090 style patterns.

---

## 9. TU roadmap and verification levels

This block explains the current verification level and the next measurable steps.

### 9.1 Current levels

* **E_level: E1**

  * Q090 defines a coherent effective layer encoding of the neural basis of social cognition.
  * Observables, tension functionals and a singular set `S_sing` are specified.
  * Encoding libraries and a finite registry `Registry_SOC` are described, but no empirical implementations are required yet.

* **N_level: N1**

  * The narrative connecting social brain structure, social prediction and social tension is explicit and internally coherent.
  * Cross problem links and reusable components are identified.
  * Detailed quantitative case studies and code libraries remain future work.

### 9.2 Next measurable step toward E2

To reach E2, at least one of the following must be realized:

1. A working analysis pipeline that takes non invasive measurements and behavioral data and outputs for a nontrivial cohort:

   * approximate `SocialGraphField` summaries,
   * `DeltaS_soc_struct`, `DeltaS_soc_pred` and `Tension_SOC` for a set of participants and tasks,
   * published distributions of tension values for typical and comparison groups,
   * logs that satisfy the audit trace requirements in Section 6.

2. A suite of experiments on artificial models where:

   * Q090 observables are implemented as functions over network internal states,
   * `Tension_SOC` is computed during social task simulations using registry encodings,
   * results are shared and reproduced by at least one independent group.

These steps operate only on observables and encodings.
They do not require revealing any deep Tension Universe mechanisms.

### 9.3 Long term role in the TU program

In the long term, Q090 is intended to:

1. Anchor the social cognition part of the neuroscience cluster as a structured node with precise tension observables.
2. Provide biologically informed but effective layer templates for designing AI agents with social reasoning abilities.
3. Connect to societal and governance problems by making it possible to move from individual social brain patterns to higher level social dynamics through explicit transfer components.

---

## 10. Elementary but precise explanation

This section explains Q090 for non specialists while keeping the description precise.

Social cognition is the collection of abilities that let a person understand other people.
It includes:

* guessing what others think or feel,
* predicting how they might act,
* understanding social rules,
* keeping track of relationships and reputations.

The brain does not do this using a single point that says "social".
Many brain areas work together in patterns that researchers call social brain networks.

In this entry we do not try to explain every detail of biology.
Instead we ask a simpler but still precise question:

> Can we describe how well the social brain is working using a few observable quantities and a single number that measures social tension?

We imagine that at any moment the brain is in a state `m`.
For that state we look at:

* how active different social brain areas are,
* how strongly they influence each other,
* what kind of internal story the person has about self and others,
* how big the errors are when the person tries to predict other people.

From these pieces we build:

* a `SocialGraphField` that captures which areas are talking to which,
* a summary of social prediction error,
* a combined social tension number `Tension_SOC(m)`.

If the brain structure and social predictions fit well together, `Tension_SOC(m)` is small.
If they do not fit well, `Tension_SOC(m)` is large.

We then describe two kinds of abstract worlds.

* In a low tension world, many people can reach states where social tension is small across everyday situations.
  The social brain is robust and can adapt to change without breaking.
* In a high tension world, some brains are built or shaped in ways that keep social tension high across important situations.
  Learning helps only a little and compensation is fragile.

This does not classify any real person and does not diagnose any condition.
It gives researchers and engineers:

* a way to talk about the neural basis of social cognition in terms of fields and tension,
* a clear target for experiments that test whether their models are reasonable,
* a reusable template for building and analyzing AI systems that need social understanding.

Q090 is therefore a structured, effective layer description of the neural basis of social cognition that others can test, extend and connect to different parts of the Tension Universe.

---

## Tension Universe effective-layer footer

This page is part of the **WFGY / Tension Universe** S problem collection.

### Scope of claims

* The goal of this document is to specify an **effective layer encoding** of the named problem.
* It does not claim to prove or disprove the canonical scientific statement in Section 1.
* It does not introduce any new theorem beyond what is already established in the cited literature.
* It should not be cited as evidence that the corresponding open problem has been solved.
* It must not be used to assign scores, labels or diagnoses to individual human beings.

### Effective-layer boundary

* All objects used here
  such as state spaces `M`, parameter spaces `Par_SOC`, observables, fields, tension scores and counterfactual worlds
  live at the effective layer.
* No deep TU axioms, generative rules or hidden mechanisms are exposed or claimed.
* Any concrete implementation must choose encodings from finite libraries and registries and must document those choices.

This page should be read together with the following charters:

* [TU Effective Layer Charter](../Charters/TU_EFFECTIVE_LAYER_CHARTER.md)
* [TU Encoding and Fairness Charter](../Charters/TU_ENCODING_AND_FAIRNESS_CHARTER.md)
* [TU Tension Scale Charter](../Charters/TU_TENSION_SCALE_CHARTER.md)
* [TU Global Guardrails](../Charters/TU_GLOBAL_GUARDRAILS.md)

---

**Index:**  
[`← Back to Event Horizon`](../EventHorizon/README.md)  
[`← Back to WFGY Home`](https://github.com/onestardao/WFGY)

**Consistency note:**  
This entry has passed the internal formal-consistency and symbol-audit checks under the current WFGY 3.0 specification.  
The structural layer is already self-consistent; any remaining issues are limited to notation or presentation refinement.  
If you find a place where clarity can improve, feel free to open a PR or ping the community.  
WFGY evolves through disciplined iteration, not ad-hoc patching.
