# Q079 · Origin of eukaryotes

## 0. Header metadata

```txt
ID: Q079
Code: BH_BIO_ORIGIN_EUKARYOTES_L3_079
Domain: Biology
Family: Evolutionary and cell biology
Rank: S
Projection_dominance: P
Field_type: dynamical_field
Tension_type: consistency_tension
Status: Open
Semantics: hybrid
E_level: E1
N_level: N2
Last_updated: 2026-01-26
```

---

## 1. Canonical problem and status

### 1.1 Canonical statement

The canonical problem behind Q079 can be phrased as follows:

> Explain how the first eukaryotic cells arose from prokaryote like ancestors, in a way that is consistent with:
>
> * genomic and phylogenetic evidence,
> * cell biological and structural evidence,
> * bioenergetic and ecological constraints,
> * and the observed diversity of modern eukaryotes.

In standard biological terms, the question asks:

1. What were the identities and properties of the partner lineages that gave rise to the first eukaryotic cells
   (for example host archaeal lineage, bacterial endosymbiont lineages such as proto mitochondria and proto plastids)?

2. By what sequence of events did these partners establish a stable endosymbiotic relationship, including:

   * entry of the symbiont into the host,
   * stabilization of residence inside the host,
   * gene transfer and genome reduction,
   * evolution of organelles and compartmentalization?

3. How did this process produce the characteristic features of eukaryotes:

   * nuclei and internal membrane systems,
   * mitochondria (and later plastids),
   * cytoskeletal complexity,
   * greatly increased cell size and genome complexity?

The problem is not merely to describe a plausible narrative, but to determine whether there exists a relatively simple and reusable integration pattern that can account for:

* the emergence of eukaryotic complexity,
* the repeated appearance of organelles through primary and secondary endosymbiosis,
* and the tight link between bioenergetic capacity and genomic complexity.

### 1.2 Status and difficulty

Several major components of the problem are widely accepted:

* Mitochondria and plastids are of bacterial origin and are descendants of once free living bacteria.
* Eukaryotes likely arose from a partnership between an archaeal host and a bacterial endosymbiont.
* Modern eukaryotes show extensive chimerism in their genomes, with both archaeal and bacterial contributions.
* Bioenergetic arguments suggest that mitochondria provided a qualitative jump in energy per gene that enabled large complex genomes.

However, many details remain open or strongly debated:

* The exact nature of the host lineage (for example which group within Asgard archaea, and what its cell biology looked like).
* The sequence and timing of key transitions:

  * endosymbiont entry,
  * establishment of stable endosymbiosis,
  * evolution of internal membranes and cytoskeleton,
  * origin of the nucleus.
* The degree to which eukaryogenesis was:

  * a rare accident with many hard to repeat steps,
  * versus a generic outcome of certain ecological and bioenergetic conditions.

From a scientific standpoint, the problem is considered extremely hard because it combines:

* incomplete and biased fossil and molecular records,
* many potential historical contingencies,
* limited ability to perform experiments that directly replay deep time events.

The difficulty is not only empirical. There is also a structural difficulty:

* It is nontrivial to write down a compact and testable description of how genomes, energy flows, compartment structure and ecology can be jointly consistent with the origin and stability of eukaryotic cells.

### 1.3 Role in the BlackHole project

Within the BlackHole S problem collection, Q079 plays three roles:

1. It is the flagship example of a **consistency_tension** problem in evolutionary and cell biology, where:

   * multiple levels of description (genomes, organelles, cells, ecosystems) must be mutually consistent,
   * and the existence of complex cells depends on resolving tensions between these levels.

2. It provides a test ground for hybrid field encodings, where:

   * discrete structures (genes, operons, organelles, compartments, lineages),
   * and continuous quantities (energetic fluxes, population parameters, rate constants)
     must be combined into a single effective state space.

3. It anchors a family of biological problems that reuse its components:

   * biosphere level limits on complexity and energy (Q080),
   * host microbe consortia and microbiomes (Q077),
   * organellar conflict and aging (Q075),
   * symbiosis inspired architectures in AI (Q123).

### References

1. Lynn Margulis. *Symbiosis in Cell Evolution: Life and its Environment on the Early Earth.* W. H. Freeman, 1981.
2. Nick Lane, William Martin. "The energetics of genome complexity." *Nature* 467, 929–934, 2010.
3. Bruce Alberts et al. *Molecular Biology of the Cell.* Garland Science, latest edition. Chapters on mitochondria, chloroplasts, and the origin and evolution of eukaryotes.
4. A. J. Roger, S. A. Muñoz Gómez, R. Kamikawa. "The origin and diversification of mitochondria." *Current Biology* 27(21): R1177–R1192, 2017.
5. Hiroyuki Imachi et al. "Isolation of an archaeon at the prokaryote eukaryote interface." *Nature* 577, 519–525, 2020.
6. William Martin, Miklós Müller. "The hydrogen hypothesis for the first eukaryote." *Nature* 392, 37–41, 1998.
7. Douglas Futuyma et al. *Evolution.* Sinauer Associates or equivalent, chapters on eukaryote origins and complex cells.

---

## 2. Position in the BlackHole graph

This block records how Q079 sits inside the BlackHole graph as nodes and edges among Q001–Q125. Each edge is listed with a one line reason that points to a concrete component or tension type.

### 2.1 Upstream problems

These problems provide prerequisites, tools, or general foundations that Q079 relies on at the effective layer.

* Q071 (BH_BIO_ORIGIN_L3_071)
  Reason: Provides origin of minimal cells and replicators and defines the pre eukaryotic state space `M_pre` from which `M_euk` is extended.

* Q072 (BH_BIO_GENETIC_CODE_L3_072)
  Reason: Fixes the shared genetic code and translational machinery that both host and symbiont inherit and that appear inside `G_host(m)` and `G_sym(m)`.

* Q074 (BH_BIO_CELL_DIFFER_L3_074)
  Reason: Supplies general mechanisms of compartment formation and cell differentiation that are reused in the component `C_comp(m)`.

* Q078 (BH_BIO_DEVELOPMENTAL_L3_078)
  Reason: Provides `DevMap_field` and genotype to phenotype consistency_tension, which are reused in `P_euk(m)` to describe early developmental like patterns in emerging eukaryotes.

### 2.2 Downstream problems

These problems are direct reuse targets of Q079 components or depend on Q079’s tension structure.

* Q080 (BH_BIO_BIOSPHERE_LIMITS_L3_080)
  Reason: Reuses `EukCompartment_field` and `Euk_energy_profile` to relate eukaryotic complexity to biosphere level energy and adaptability limits.

* Q077 (BH_BIO_MICROBIOME_L3_077)
  Reason: Uses the `Host_symbiont_partnership_profile` observable as a template for describing host microbiome consortia stability and conflict.

* Q075 (BH_BIO_AGING_L3_075)
  Reason: Reuses `Organellar_conflict_tension` derived from Q079 to model long term breakdown of host organelle integration in aging cells.

### 2.3 Parallel problems

Parallel nodes share similar tension types but no direct component dependence.

* Q063 (BH_CHEM_PROTEIN_FOLDING_L3_063)
  Reason: Both Q079 and Q063 involve mapping from many small building blocks into complex, stable configurations under strong energetic and structural constraints.

* Q059 (BH_CS_INFO_THERMODYN_L3_059)
  Reason: Both treat consistency_tension between information structures, physical capacity and energy costs as the key organizing principle.

### 2.4 Cross domain edges

Cross domain edges connect Q079 to problems in other domains that can reuse its components.

* Q031 (BH_PHYS_QINFO_L3_031)
  Reason: Reuses `Compartment_channel_capacity` style observables to compare biological compartmentalization with constrained information channels in quantum and classical systems.

* Q123 (BH_AI_INTERP_L3_123)
  Reason: Uses the `Symbiosis_to_architecture_template` derived from Q079 to interpret layered AI systems as integrated host symbiont style architectures under consistency_tension.

---

## 3. Tension Universe encoding (effective layer)

All content in this block is at the effective layer. We only describe:

* state spaces,
* observables and fields,
* invariants and tension scores,
* singular sets and domain restrictions.

We do not describe any hidden generative rules or any mapping from raw data to internal TU fields.

### 3.1 State space

We assume an effective state space

```txt
M_euk
```

Each state `m` in `M_euk` represents a coherent configuration for early eukaryogenesis, encoded as an effective tuple:

```txt
m = (G_host(m), G_sym(m), R_coupling(m), C_comp(m), E_env(m), P_euk(m))
```

where:

* `G_host(m)` is an effective descriptor of host genomic and metabolic modules.
* `G_sym(m)` is an effective descriptor of symbiont genomic and metabolic modules.
* `R_coupling(m)` is an effective descriptor of regulatory and signaling couplings between host and symbiont.
* `C_comp(m)` is an effective descriptor of compartmental structure, including membranes, organelles and trafficking routes.
* `E_env(m)` is an effective descriptor of environmental and ecological context, including available energy sources.
* `P_euk(m)` is an effective descriptor of eukaryotic phenotypes such as cell size, genome complexity, organelle complement and basic life history traits.

We only assume that for relevant historical or model scenarios there exist states in `M_euk` that encode:

* host and symbiont configurations,
* their couplings,
* compartmental structures,
* environmental context,
* and resulting eukaryotic phenotypes.

No details are given here on how these effective descriptors are constructed from empirical data.

### 3.2 Finite libraries and admissible encodings

We introduce finite or countable libraries of modules:

```txt
Lib_G_host = {gh_1, ..., gh_Nh}
Lib_G_sym  = {gs_1, ..., gs_Ns}
Lib_R_cpl  = {rc_1, ..., rc_Nc}
Lib_C_comp = {cc_1, ..., cc_Ncc}
Lib_P_euk  = {pe_1, ..., pe_Np}
Lib_E_env  = {ee_1, ..., ee_Ne}
```

Each element is an effective building block. For example:

* `gh_k` may represent an archetypal host metabolic and regulatory package.
* `gs_l` may represent proto mitochondrial traits relevant to energy transduction.
* `cc_j` may represent a particular organelle or transport architecture.
* `pe_u` may represent a coarse phenotypic pattern, such as a class of eukaryotic cell types.

We also introduce an index set of resolutions:

```txt
R_res_euk = {r_1, r_2, ..., r_K, ...}
```

with a refinement order `<=` such that:

* `r_1 <= r_2 <= ...`, and
* moving from `r` to `r'` with `r' >= r` corresponds to adding more detail or finer resolution, never reducing information.

An admissible encoding for Q079 is any map of the form:

```txt
Gamma_r : (G_host, G_sym, R_coupling, C_comp, E_env) -> P_euk
```

for some `r` in `R_res_euk`, satisfying:

1. For each `r`, the functional form of `Gamma_r` and any hyperparameters are fixed in advance and do not depend on the particular world or dataset to be evaluated.
2. `Gamma_r` can only use modules selected from the libraries above.
3. The family `{Gamma_r}` is fixed before evaluating tension or invariants and is not tuned in response to those evaluations.
4. Refinement means moving from `Gamma_r` to `Gamma_r'` with `r' >= r` in the fixed order, not redefining the library or the functional family.

We denote the set of all such admissible encodings as:

```txt
E_euk = {Gamma_r | r in R_res_euk and Gamma_r satisfies conditions (1) to (4)}
```

This definition acts as a fairness constraint: encodings cannot be chosen after seeing outcomes in order to artificially minimize tension.

### 3.3 Effective fields and observables

On `M_euk` and for a chosen `Gamma_r`, we define the following effective observables.

1. Bioenergetic profile observable

```txt
Euk_energy_profile(m; r)
```

* Input: a state `m` in `M_euk` and a resolution index `r` in `R_res_euk`.
* Output: an effective vector of nonnegative real valued quantities summarizing, for example:

  * ATP flux per cell,
  * ATP flux per gene,
  * energy cost of maintaining compartments and organelles,
  * surplus energy available for regulation and complexity.

2. Complexity load observable

```txt
Complexity_load(m; r)
```

* Input: `m` and `r`.
* Output: an effective vector capturing aspects of genomic and regulatory complexity:

  * genome size,
  * number of expressed genes,
  * degree of regulatory network complexity,
  * number and diversity of organelles.

3. Host symbiont conflict observable

```txt
Host_symbiont_conflict(m; r)
```

* Input: `m` and `r`.
* Output: a nonnegative scalar measuring unresolved conflict between host and symbiont modules, for example:

  * conflicting replication schedules,
  * incompatible expression patterns,
  * selfish symbiont behaviors that reduce host fitness.

4. Integration modularity observable

```txt
Integration_modularity(m; r)
```

* Input: `m` and `r`.
* Output: a nonnegative scalar, with larger values indicating clearer decomposition into stable modules (for example distinct organelles with coherent function and regulation).

5. Reference profiles and mismatch observable

We fix in advance a finite reference class of eukaryogenesis scenarios:

```txt
Ref_euk = {Ref_1, ..., Ref_Nref}
```

Each `Ref_k` is an effective tuple of target values for:

* energy profiles,
* complexity loads,
* conflict levels,
* modularity levels,

for a particular resolution `r` or small set of resolutions.

The reference class `Ref_euk` is selected before evaluating any particular world or model and remains fixed. It cannot be tuned after observing tension outcomes.

Given `Ref_euk`, we define a mismatch observable:

```txt
DeltaS_euk(m; r) >= 0
```

that measures the deviation of `(Euk_energy_profile(m; r), Complexity_load(m; r), Host_symbiont_conflict(m; r), Integration_modularity(m; r))` from the closest reference pattern in `Ref_euk` at resolution `r`.

We also define fixed nonnegative weights:

```txt
w_energy > 0
w_complexity > 0
w_conflict > 0
w_modularity > 0
w_energy + w_complexity + w_conflict + w_modularity = 1
```

These weights are chosen once, before any evaluation, and are shared across all states and all worlds.

The mismatch `DeltaS_euk(m; r)` is constructed using the weights above. The exact aggregation rule is an encoding choice, but in all cases:

* `DeltaS_euk(m; r) = 0` if and only if the encoded observables match a reference pattern exactly,
* `DeltaS_euk(m; r)` increases as deviations from the reference patterns increase.

### 3.4 Tension tensor and global tension functional

We assume an effective semantic tension tensor over `M_euk` in the form:

```txt
T_ij_euk(m; r) = S_i_euk(m; r) * C_j_euk(m; r) * DeltaS_euk(m; r) * lambda_euk(m; r) * kappa_euk
```

where:

* `S_i_euk(m; r)` is a source like factor measuring how strongly the `i`th component of the configuration contributes to tension (for example host genome misalignment).
* `C_j_euk(m; r)` is a receptivity like factor measuring how sensitive the `j`th downstream structure is to that tension (for example fitness consequences in different environments).
* `DeltaS_euk(m; r)` is the mismatch defined above.
* `lambda_euk(m; r)` is a convergence state factor in a bounded interval, indicating whether local reasoning about this configuration is convergent, recursive, divergent or chaotic.
* `kappa_euk` is a constant that sets the overall scale of eukaryogenesis related consistency_tension.

All quantities are finite for `m` in the regular domain defined below.

We also define a global tension functional by aggregating across a finite or countable set of resolutions `R_eval` chosen in advance:

```txt
R_eval subset of R_res_euk, R_eval = {r_1, ..., r_M}

Tension_euk(m) = max over r in R_eval of DeltaS_euk(m; r)
```

The set `R_eval` is fixed at design time and is not chosen after inspecting any particular state. Using a maximum over a fixed set of indices avoids unbounded suprema over unconstrained families.

### 3.5 Singular set and domain restrictions

Some observables may fail to be defined or may become non finite if the encoding is incomplete or inconsistent. To ensure that tension summaries remain meaningful, we define a singular set:

```txt
S_sing_euk = {
  m in M_euk :
    for some r in R_eval,
    Euk_energy_profile(m; r),
    Complexity_load(m; r),
    Host_symbiont_conflict(m; r),
    Integration_modularity(m; r),
    or DeltaS_euk(m; r)
    is undefined or not finite
}
```

We then restrict all invariants and experiments to the regular domain:

```txt
M_euk_reg = M_euk \ S_sing_euk
```

Whenever a proposed state for analysis lies in `S_sing_euk`, evaluations of `Tension_euk` are treated as “out of domain” and are not used as evidence for or against any hypothesis about eukaryote origins.

### 3.6 Invariants

We define two effective invariants on `M_euk_reg` using the observables above.

1. Energy complexity consistency invariant

We fix in advance a reference function:

```txt
Ref_energy_complexity(r)
```

that encodes the expected relationship between bioenergetic capacity and complexity load (inspired by, but not identical to, the arguments of Lane and Martin).

For each `m` in `M_euk_reg` we define:

```txt
I_energy(m) =
  max over r in R_eval of
    Energy_mismatch(m; r)
```

where `Energy_mismatch(m; r)` is a nonnegative scalar derived from the difference between:

* the observed relationship between `Euk_energy_profile(m; r)` and `Complexity_load(m; r)`,
* the reference relationship given by `Ref_energy_complexity(r)`.

2. Integration stability invariant

We define:

```txt
I_integration(m) =
  max over r in R_eval of
    DeltaS_euk(m; r)
```

This invariant summarizes the worst case mismatch between the encoded integration pattern and the reference class across the chosen resolutions.

Both invariants are well defined and finite on `M_euk_reg`. They are built using fixed reference objects and fixed evaluation resolutions, not tuned in response to particular worlds.

---

## 4. Tension principle for this problem

This block states how Q079 is characterized as a tension problem within TU, at the effective layer.

### 4.1 Core tension functional

We use the global tension functional defined above:

```txt
Tension_euk(m) = max over r in R_eval of DeltaS_euk(m; r)
```

and interpret it as a scalar measure of how well a particular configuration `m` in `M_euk_reg` embodies a coherent, reusable pattern of eukaryogenesis.

By construction:

* `Tension_euk(m) >= 0` for all `m` in `M_euk_reg`.
* `Tension_euk(m)` is small if all evaluated resolutions show good agreement with the reference class `Ref_euk`.
* `Tension_euk(m)` is large if any evaluated resolution exhibits strong mismatch.

Different admissible encodings in `E_euk` may change the numerical value of `Tension_euk`, but they all respect the same fairness constraints:

* fixed libraries,
* fixed reference class,
* fixed weight vector,
* fixed evaluation resolutions.

### 4.2 Low tension eukaryogenesis principle

At the effective layer, the low tension principle for Q079 can be stated as:

> In the actual universe, there exist world representing states `m_T` in `M_euk_reg` and admissible encodings `Gamma_r` in `E_euk` such that:
>
> * bioenergetic capacity and complexity load are jointly consistent with a simple reference relationship across scales,
> * host symbiont conflicts are resolved by a relatively small set of reusable patterns,
> * integration modularity is high and stable across lineages,
> * and the global tension functional remains in a low band:
>
>   `Tension_euk(m_T) <= epsilon_euk`
>
>   for some small threshold `epsilon_euk` that does not grow without bound as resolution is refined within `R_eval`.

Intuitively, a low tension world is one in which:

* the origin of eukaryotes can be described by a compact set of rules,
* those rules are reused across multiple lineages and endosymbiotic events,
* and bioenergetic constraints are satisfied in a systematic way rather than by a sequence of unrelated accidents.

### 4.3 High tension eukaryogenesis principle

The contrasting high tension principle is:

> In worlds where eukaryotes, if present, arise through idiosyncratic accidents with no reusable integration pattern, any fair encoding in `E_euk` yields world representing states `m_F` in `M_euk_reg` with:
>
> `Tension_euk(m_F) >= delta_euk`
>
> for some strictly positive `delta_euk` that cannot be driven arbitrarily close to zero by refining resolution in `R_eval` or by switching to another admissible encoding in `E_euk`.

In such worlds:

* there is no stable relationship between energy supply and complexity,
* host symbiont conflicts are never cleanly resolved in a reusable way,
* compartment structures and integration patterns differ so much between lineages that a single reference class cannot capture them without high mismatch.

Q079, at the effective layer, is not the claim that low tension is known to hold, but the claim that it is meaningful to ask whether the universe is closer to a low tension or a high tension eukaryogenesis world when evaluated by `Tension_euk`.

---

## 5. Counterfactual tension worlds

We now outline two counterfactual worlds, both described strictly at the effective layer:

* World T: eukaryogenesis is governed by a structured, reusable integration pattern (low tension).
* World F: eukaryogenesis is essentially unstructured and idiosyncratic (high tension).

Each world is described through patterns of observables and invariants, not through any hidden construction rules.

### 5.1 World T (structured low tension eukaryogenesis)

In World T:

1. Energy complexity alignment

* For world representing states `m_T` in `M_euk_reg`, the invariant `I_energy(m_T)` remains within a controlled band:

  ```txt
  I_energy(m_T) <= epsilon_energy
  ```

  for a small, fixed `epsilon_energy`. As resolution increases within `R_eval`, the relationship between energy supply and complexity load stays stable and close to the reference `Ref_energy_complexity(r)`.

2. Host symbiont conflict resolution

* For most relevant states `m_T`, the observable `Host_symbiont_conflict(m_T; r)` is low across resolutions in `R_eval`, and the integration modularity is high:

  ```txt
  Host_symbiont_conflict(m_T; r) is small
  Integration_modularity(m_T; r) is large
  ```

  indicating that conflicts are resolved by a small set of reusable mechanisms such as gene transfer, genome reduction and compartment formation.

3. Cross lineage reuse

* The same libraries `Lib_G_host`, `Lib_G_sym`, `Lib_C_comp` and `Lib_R_cpl` can be used to describe:

  * mitochondria based origins,
  * plastid acquisition,
  * and secondary or tertiary endosymbioses,

  with only moderate increases in `DeltaS_euk(m_T; r)`. The reference class `Ref_euk` remains adequate without lineages specific explosion in mismatch.

4. Global tension band

* The global tension functional satisfies:

  ```txt
  Tension_euk(m_T) <= epsilon_euk
  ```

  for most world representing states and for a wide range of lineages, indicating that Q079 sits in a low tension regime.

### 5.2 World F (unstructured high tension eukaryogenesis)

In World F:

1. Energy complexity misalignment

* For world representing states `m_F`, the invariant `I_energy(m_F)` is large:

  ```txt
  I_energy(m_F) >= delta_energy
  ```

  for some positive `delta_energy`. Attempts to encode a coherent relationship between energy supply and complexity across lineages fail, with different lineages requiring inconsistent or incompatible relationships.

2. Host symbiont conflict persistence

* The observable `Host_symbiont_conflict(m_F; r)` remains high for some resolutions in `R_eval`, and integration modularity is low:

  ```txt
  Host_symbiont_conflict(m_F; r) is large
  Integration_modularity(m_F; r) is small or unstable
  ```

* Conflicts are resolved, if at all, by lineage specific, non reusable mechanisms that do not compress into a small set of patterns.

3. Cross lineage failure

* Any attempt to use a fixed reference class `Ref_euk` and fixed libraries to describe all lineages leads to large mismatch:

  ```txt
  DeltaS_euk(m_F; r) is large for some r in R_eval
  ```

* To reduce mismatch for one lineage, one must introduce special modules that increase mismatch for others, preventing a unified low tension encoding.

4. Global tension band

* For world representing states:

  ```txt
  Tension_euk(m_F) >= delta_euk
  ```

  where `delta_euk` is a positive lower bound across admissible encodings, signifying a high tension regime.

### 5.3 Interpretive note

These counterfactual worlds do not assert any specific historical narrative or mechanistic sequence. They only state that:

* if there exist effective encodings that faithfully represent a eukaryote bearing universe,
* then low tension and high tension regimes would manifest as different patterns in the observables and invariants defined above.

The question of which regime the actual universe belongs to is empirical and model dependent, not settled within this block.

---

## 6. Falsifiability and discriminating experiments

This block specifies experiments and protocols, at the effective layer, that can:

* test the coherence of the Q079 encoding,
* discriminate between different families of tension encodings,
* and provide evidence about whether eukaryogenesis behaves more like a low tension or high tension process under this framework.

These experiments cannot prove or disprove any specific biological hypothesis by themselves. They can only falsify specific TU encodings related to Q079.

### Experiment 1: Comparative bioenergetic scaling

*Goal:*
Test whether there exists an admissible encoding in `E_euk` such that real prokaryote and eukaryote data produce a stable, low `I_energy(m)` band for eukaryotes without collapsing the distinction between prokaryotes and eukaryotes.

*Setup:*

* Input data (external to TU):

  * comparative datasets of cell volume, genome size, gene count,
  * estimates of ATP flux per cell and per gene for representative bacteria, archaea and eukaryotes.
* Choose a fixed subset `R_eval_energy` of `R_eval` corresponding to a small set of resolutions:

  * for example coarse grained, intermediate, and fine grained views of energy and complexity.
* Choose a family `{Gamma_r}` in `E_euk`, a reference function `Ref_energy_complexity(r)` and energy mismatch function `Energy_mismatch(m; r)` before looking at any tension results.

*Protocol:*

1. For each taxon in the dataset, construct an effective state `m_data` in `M_euk_reg` by:

   * encoding host and symbiont modules (if any),
   * encoding environment summary,
   * assigning an effective phenotype summary.
     The construction details are external to TU and are not specified here.

2. For each `m_data` and each `r` in `R_eval_energy`, evaluate:

   * `Euk_energy_profile(m_data; r)`,
   * `Complexity_load(m_data; r)`,
   * `Energy_mismatch(m_data; r)`.

3. Compute `I_energy(m_data)` for each state using:

   ```txt
   I_energy(m_data) = max over r in R_eval_energy of Energy_mismatch(m_data; r)
   ```

4. Separate states into:

   * prokaryote like states (bacteria and archaea),
   * eukaryote states (including proto eukaryotes if data exist).

*Metrics:*

* Distribution of `I_energy(m_data)` for prokaryote and eukaryote states.
* Separation between distributions, for example median or quantile differences.
* Stability of these distributions when `R_eval_energy` is expanded within `R_eval` or when additional taxa are added.

*Falsification conditions:*

*Condition A (no distinction):*
If, for every admissible encoding in `E_euk` satisfying the fairness constraints, the distributions of `I_energy(m_data)` for prokaryotes and eukaryotes substantially overlap, with no encoding producing a robust low band for eukaryotes without also placing a comparable set of prokaryotes in that band, then:

* the current design of `Euk_energy_profile`, `Ref_energy_complexity` and `Energy_mismatch` is considered falsified and must be revised.

*Condition B (instability under refinement):*
If small, pre specified refinements of `R_eval_energy` within `R_eval` cause large, unstructured swings in `I_energy(m_data)` for the same taxa, then:

* the encoding is considered unstable and rejected at the effective layer.

*Semantics implementation note:*
All quantities are implemented with hybrid semantics as declared in Block 0: discrete components (for example module identities, taxon labels) are treated as elements of finite sets, and continuous components (for example fluxes, sizes) are treated as real valued fields. No additional semantic regime is introduced in this experiment.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. This experiment can reject specific designs of `Euk_energy_profile` and related functionals, but it does not, by itself, establish any particular biological scenario for eukaryote origins.

---

### Experiment 2: Reconstruction of endosymbiotic histories

*Goal:*
Test whether a single fixed library and encoding can describe primary and secondary endosymbiotic events with moderate `Tension_euk(m)` values across lineages, rather than requiring lineage specific modules for each case.

*Setup:*

* Input data (external to TU):

  * genomic and structural summaries for:

    * lineages with mitochondria only,
    * lineages with plastids (primary endosymbiosis),
    * lineages with secondary or tertiary plastids.
* Choose:

  * a single library of modules `Lib_G_host`, `Lib_G_sym`, `Lib_C_comp`, `Lib_R_cpl`,
  * a fixed family `{Gamma_r}` in `E_euk`,
  * a fixed evaluation subset `R_eval_sym` of `R_eval` relevant to organelle integration.
* All choices are fixed prior to computing any tension values.

*Protocol:*

1. For each lineage, construct an effective state `m_lineage` in `M_euk_reg` by encoding:

   * an approximate host module configuration,
   * relevant symbiont modules (for example proto mitochondrion, proto plastid),
   * a compartment architecture descriptor,
   * environment and phenotype summaries.

2. For each `m_lineage` and each `r` in `R_eval_sym`, evaluate observables:

   * `Host_symbiont_conflict(m_lineage; r)`,
   * `Integration_modularity(m_lineage; r)`,
   * `DeltaS_euk(m_lineage; r)`.

3. Compute the global tension:

   ```txt
   Tension_euk(m_lineage) = max over r in R_eval_sym of DeltaS_euk(m_lineage; r)
   ```

4. Compare tension values across:

   * mitochondria only lineages,
   * primary plastid lineages,
   * secondary and tertiary plastid lineages.

*Metrics:*

* Distribution of `Tension_euk(m_lineage)` for each class of lineages.
* Number of additional lineage specific modules required to keep tension under a pre specified upper bound.
* Robustness of tension values under minor, pre declared changes of module grouping inside the libraries.

*Falsification conditions:*

*Condition A (lineage explosion):*
If, to keep `Tension_euk(m_lineage)` below a moderate upper bound `T_max` for all lineages, one must introduce many lineage specific modules that break the original finite library design, then:

* the current encoding is considered to have failed to capture reusable integration patterns and is rejected.

*Condition B (misaligned tension):*
If obviously more complex endosymbiotic events (for example secondary plastids) do not show higher or at least comparable `Tension_euk` values than simpler cases (for example mitochondria only), without a clear structural explanation from the observables, then:

* the encoding is considered misaligned with its intended interpretation and is rejected.

*Semantics implementation note:*
As in Experiment 1, discrete modules and lineage labels are treated as finite set elements, while continuous summaries (for example sizes, rates) are treated as real valued fields. This is consistent with the hybrid semantics declared in Block 0.

*Boundary note:*
Falsifying TU encoding != solving canonical statement. Success or failure of this experiment bears on the adequacy of the Q079 encoding, not directly on which historical endosymbiotic sequence actually occurred.

---

## 7. AI and WFGY engineering spec

This block describes how Q079 can be used as an engineering module for AI systems within the WFGY framework, at the effective layer.

### 7.1 Training signals

We define several training signals for models that reason about early evolution, symbiosis and cellular complexity.

1. `signal_euk_energy_consistency`

   * Definition: a scalar penalty proportional to `I_energy(m)` for internal states associated with eukaryogenesis contexts.
   * Purpose: encourage the model to maintain a coherent relationship between energy supply and complexity load when it assumes eukaryote like cells exist.

2. `signal_host_symbiont_conflict`

   * Definition: a scalar penalty derived from `Host_symbiont_conflict(m; r)` aggregated over relevant resolutions.
   * Purpose: penalize internal representations that imply persistent, unresolved conflicts between host and symbiont modules in scenarios that are supposed to reflect successful eukaryogenesis.

3. `signal_integration_modularity`

   * Definition: a reward proportional to `Integration_modularity(m; r)` when the context involves stable eukaryotic cells or organelles.
   * Purpose: encourage the emergence of modular internal representations of organelles and compartment structures.

4. `signal_euk_tension`

   * Definition: a penalty equal to or proportional to `Tension_euk(m)` when the model is asked to produce a coherent account of eukaryote origins under a low tension assumption.
   * Purpose: make the model explicitly track and reduce consistency_tension in its explanations across levels.

### 7.2 Architectural patterns

We outline module patterns that reuse Q079 structures without revealing any deep TU generative rules.

1. `EukaryogenesisHead`

   * Role: an auxiliary head attached to the model that maps internal embeddings for early evolution scenarios to:

     * effective summaries of `G_host`, `G_sym`, `C_comp`,
     * estimates of `Euk_energy_profile` and `Complexity_load`,
     * an estimate of `Tension_euk(m)`.
   * Interface:

     * Inputs: internal embeddings for sequences where the model is reasoning about early cells, symbiosis or organelle origins.
     * Outputs: a vector of observables and a scalar tension estimate.

2. `EndosymbiosisConsistencyFilter`

   * Role: a filter that scores candidate narratives or intermediate reasoning steps about eukaryote origins based on:

     * implied host symbiont conflict,
     * implied integration modularity,
     * implied energy complexity alignment.
   * Interface:

     * Inputs: candidate text spans or structured intermediate hypotheses.
     * Outputs: a score or mask indicating how consistent each candidate is with low `Tension_euk`.

3. `SymbiosisTransferBridge`

   * Role: a module that reuses the Q079 encoding when the model reasons about:

     * later host microbe partnerships,
     * microbiomes,
     * synthetic endosymbiosis in engineered systems.
   * Interface:

     * Inputs: embeddings and high level tags indicating that the context involves host microbe integration.
     * Outputs: mapped observables and tension estimates that can be fed into modules defined for Q077 or related nodes.

### 7.3 Evaluation harness

We suggest an evaluation harness for AI models augmented with Q079 related modules.

1. Task families

   * Explanatory tasks:

     * explain competing hypotheses for eukaryote origins (for example hydrogen hypothesis, syntrophy models, phagocytosis first models),
     * describe the role of mitochondria in enabling complex genomes.
   * Predictive tasks:

     * predict qualitative consequences of modifying host or symbiont energy metabolism,
     * predict which host symbiont combinations are more likely to produce stable eukaryote like cells.

2. Conditions

   * Baseline condition:

     * the model operates without explicit Q079 modules, only with general purpose reasoning.
   * TU augmented condition:

     * the model uses `EukaryogenesisHead` and `EndosymbiosisConsistencyFilter` during inference, and may use `signal_euk_tension` during fine tuning.

3. Metrics

   * Accuracy on questions where the scientific community has relatively clear consensus.
   * Internal consistency:

     * frequency of contradictions between answers given under low tension assumptions and answers given under intentionally high tension prompts.
   * Structural coherence:

     * degree to which the model’s chain of thought (where accessible) respects:

       * energy constraints,
       * conflict resolution mechanisms,
       * modular compartment structure.

### 7.4 60 second reproduction protocol

A minimal protocol to let external users experience the impact of Q079 style encoding in an AI system.

*Baseline setup*

* Prompt example:

  * “Explain how eukaryotic cells originated from prokaryotes. Include the role of endosymbiosis and mitochondria, but do not use any special framework.”
* Observation:

  * record whether the explanation is fragmented, whether it mixes incompatible hypotheses, and whether it mentions energy constraints in a coherent way.

*TU encoded setup*

* Prompt example:

  * “Explain how eukaryotic cells originated from prokaryotes. Structure your answer around:

    * host symbiont integration,
    * compartmentalization into organelles,
    * and the consistency between energy supply and genome complexity.
      Use this to talk about endosymbiosis and mitochondria.”
* Observation:

  * record whether the explanation organizes itself along the three axes above,
  * check whether it uses a clear conflict and resolution structure for host symbiont interactions.

*Comparison metric*

* Use a simple rubric to rate:

  * clarity of the integration pattern,
  * explicit handling of tradeoffs and constraints,
  * alignment with known arguments about bioenergetics and complexity.
* Optionally, have domain knowledgeable readers judge which explanation captures the structure of current scientific thinking more faithfully.

*What to log*

* The exact prompts and full responses for both setups.
* Any auxiliary observables and tension scores produced by Q079 modules in the TU augmented setup.
* This allows later inspection and comparison without exposing any internal TU generative rule.

---

## 8. Cross problem transfer template

This block describes the reusable components produced by Q079 and how they transfer to other problems.

### 8.1 Reusable components produced by this problem

1. ComponentName: `EukCompartment_field`

   * Type: `field`
   * Minimal interface:

     * Inputs:

       * `G_host_descriptor`
       * `G_sym_descriptor`
       * `R_coupling_descriptor`
       * `E_env_descriptor`
     * Outputs:

       * `C_comp_descriptor`
       * `DeltaS_euk_comp` (component of `DeltaS_euk` focused on compartment structure)
   * Preconditions:

     * Host and symbiont descriptors must be consistent with a shared genetic code and basic compatibility of membranes and exchange processes.
     * Environment descriptor must fall within the range where endosymbiosis is biophysically plausible.

2. ComponentName: `Endosymbiosis_tension_functional`

   * Type: `functional`
   * Minimal interface:

     * Inputs:

       * `Euk_energy_profile`
       * `Complexity_load`
       * `Host_symbiont_conflict`
       * `Integration_modularity`
     * Outputs:

       * `Tension_euk` scalar
   * Preconditions:

     * Observables must be well defined and finite at the chosen evaluation resolutions.
     * A fixed reference class `Ref_euk` and weight vector `(w_energy, w_complexity, w_conflict, w_modularity)` must be specified in advance.

3. ComponentName: `Host_symbiont_partnership_profile`

   * Type: `observable`
   * Minimal interface:

     * Inputs:

       * `G_host_descriptor`
       * `G_sym_descriptor`
       * `R_coupling_descriptor`
       * `E_env_descriptor`
       * optionally `P_euk_descriptor`
     * Outputs:

       * `stability_index` (nonnegative scalar)
       * `conflict_index` (nonnegative scalar)
   * Preconditions:

     * Encoded host and symbiont must have clearly defined replication and expression systems.
     * Environment descriptor must include at least a coarse description of resource availability.

### 8.2 Direct reuse targets

1. Q080 (BH_BIO_BIOSPHERE_LIMITS_L3_080)

   * Reused components:

     * `EukCompartment_field`
     * `Endosymbiosis_tension_functional`
   * Why it transfers:

     * Biosphere level limits on complexity and diversity depend on how cells partition energy and structure complexity. The same field and tension functional can be reused to aggregate cell level constraints to ecosystem level.
   * What changes:

     * Inputs are aggregated over many cells and species, and the outputs feed into biosphere level observables such as total productivity and maximum achievable complexity.

2. Q077 (BH_BIO_MICROBIOME_L3_077)

   * Reused component:

     * `Host_symbiont_partnership_profile`
   * Why it transfers:

     * Large host microbiome systems can be viewed as extended host symbiont partnerships with many participants. Stability and conflict indices generalize naturally from two partner systems to multi partner consortia.
   * What changes:

     * Descriptors include multiple symbiont communities rather than a single symbiont type, and the environment descriptor is expanded to include host internal environments.

3. Q123 (BH_AI_INTERP_L3_123)

   * Reused components:

     * `Endosymbiosis_tension_functional` (as a template)
     * `Host_symbiont_partnership_profile` (as a metaphorical mapping)
   * Why it transfers:

     * Complex AI architectures can be interpreted as integrations of heterogeneous submodules under capacity and conflict constraints. The same functional form can be used to define tension between modules in an AI system.
   * What changes:

     * Inputs become descriptors of AI submodules, their couplings and resource budgets instead of biological genomes and energy fluxes. Outputs are interpreted as architectural tension rather than biological tension.

---

## 9. TU roadmap and verification levels

This block explains how Q079 is positioned along the TU verification ladder and what the next measurable steps are.

### 9.1 Current levels

* E_level: E1

  * A coherent effective encoding of eukaryote origins has been specified in terms of:

    * a state space `M_euk`,
    * observables and invariants,
    * a global tension functional,
    * a singular set and regular domain.
  * At least two concrete experiment patterns with falsification conditions have been provided for testing specific encodings.

* N_level: N2

  * A narrative exists linking:

    * host and symbiont modules,
    * energy and complexity constraints,
    * conflict resolution and compartment formation,
    * and their expression as low tension versus high tension worlds.
  * Counterfactual worlds have been described in a way that can be instantiated in artificial or model scenarios.

### 9.2 Next measurable step toward E2

To move from E1 to E2, at least one of the following should be implemented in practice:

1. An open implementation of the Q079 encoding that, given comparative datasets on prokaryotes and eukaryotes, computes:

   * `Euk_energy_profile`,
   * `Complexity_load`,
   * `I_energy`,
   * `Tension_euk`,
     and publishes both the code and the resulting tension profiles.

2. A controlled study of mock model worlds for eukaryogenesis in which:

   * different mechanistic hypotheses are instantiated as synthetic data generating processes,
   * the same `E_euk` and `Ref_euk` are applied,
   * and the resulting tension profiles are analyzed to see which hypotheses naturally fall into low tension bands.

Both steps operate entirely at the effective layer, using observables and summaries. They do not require exposing any deep TU generative rule.

### 9.3 Long term role in the TU program

In the longer term, Q079 is expected to serve as:

* The reference node for problems involving transitions from simple to complex cells.
* A template for hybrid encodings that mix discrete and continuous observables under a single tension framework.
* A bridge between:

  * evolutionary biology,
  * biosphere level ecology,
  * and systems style interpretations of AI architectures,
    all expressed in a shared language of consistency_tension across levels.

---

## 10. Elementary but precise explanation

This block gives an explanation suitable for non specialists, while remaining aligned with the effective layer description.

The basic biological question is:

> How did complex cells like ours, with nuclei and mitochondria, come from much simpler cells like bacteria and archaea?

The standard picture is that:

* there was a host cell, probably related to modern archaea,
* there was a bacterial partner that moved inside the host and became a permanent guest,
* over time, the guest turned into an organelle (the mitochondrion), and many genes moved from the guest to the host genome,
* the new cell type gained much more energy per gene, which made large complex genomes and complex structures possible.

In the Tension Universe view, we do not try to replay history step by step. Instead, we ask a more structural question:

* Is there a simple, reusable way to describe how host and guest fit together,
* and does this description stay consistent when we look at real data from many organisms?

To do this, we imagine a space of states. Each state summarizes:

* what the host genome and metabolism look like,
* what the symbiont genome and metabolism look like,
* how they interact,
* what compartments and organelles exist,
* what the environment provides,
* and what kind of eukaryotic cell is produced.

For each state, we measure:

1. How much energy the cell has, and how complex its genome and regulation are.
2. How much unresolved conflict remains between host and symbiont.
3. How cleanly the cell is organized into modules like organelles, rather than a jumble of parts.

We then compare these measurements with a small set of reference patterns that represent “well behaved” eukaryote like cells. The more a state deviates from the references, the higher its eukaryogenesis tension.

Two extreme possibilities can be contrasted.

*In a low tension world*:

* there is a fairly simple pattern that describes how host and symbiont are compatible,
* similar rules apply in different lineages and different endosymbiotic events,
* the relationship between available energy and complexity is stable,
* and most real eukaryotes fit this pattern with only small deviations.

*In a high tension world*:

* each eukaryotic lineage would need its own special explanation,
* there would be no stable rule tying energy and complexity together,
* conflicts between host and symbiont would be patched on a case by case basis,
* trying to reuse one compact description across lineages would always lead to large mismatches.

Q079, in this framework, is not a specific historical story. It is a way to ask and test a sharper question:

> Does the origin of eukaryotes behave like a reusable integration pattern with low tension, or like a one off collection of accidents with high tension?

The answer depends on data and models, not on TU alone. What TU provides is a disciplined way to:

* define the relevant observables,
* construct tension measures that are fair and testable,
* design experiments that can falsify bad encodings,
* and reuse the resulting components in other biological and artificial systems.
