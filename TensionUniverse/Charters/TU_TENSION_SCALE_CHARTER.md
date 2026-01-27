# Tension Universe Tension Scale Charter (TU-TSC v1.0)

**File**: `TU_TENSION_SCALE_CHARTER.md`  
**Scope**: All Tension Universe (TU) effective-layer documents that define or use tension functionals, mismatch terms, or thresholds such as `epsilon_*` and `delta_*`.  
**Status**: Working charter, version 1.0  

This charter defines how tension quantities are scaled, normalized, and compared in TU, in order to avoid unit based ambiguities and post hoc rescaling.

---

## 1. Purpose and scope

1.1  
Many TU problem files define scalar quantities such as:

- mismatch terms `DeltaS_*`,
- tension functionals `Tension_*`,
- thresholds `epsilon_*` and `delta_*` used in experiment criteria.

1.2  
This charter specifies:

- how these quantities are treated as dimensionless or normalized,
- what kinds of rescaling are allowed,
- how thresholds relate to the chosen scale,
- how to avoid artifacts from changing physical units.

---

## 2. Basic properties of tension quantities

2.1  
Every tension functional `Tension_X(m)` used in TU effective-layer documents is treated as:

- a nonnegative scalar,
- defined on a regular domain `M_reg`,
- representing a normalized measure of mismatch, residual complexity, or conflict between constraints.

2.2  
By convention:

```txt
Tension_X(m) = 0
````

represents perfect agreement with the reference structure for the encoding in use.
Larger values indicate increasing deviation, instability, or unresolved structure.

2.3
Mismatch terms `DeltaS_*` are treated similarly. They are:

* nonnegative,
* zero when a specific alignment or property holds exactly,
* larger as the alignment or property fails more strongly.

---

## 3. Normalization and dimensionlessness

3.1
Underlying observables may carry physical units (for example seconds, joules, bits).
Before such observables are combined into mismatch terms or tension functionals, they must be:

* normalized by reference scales,
* or mapped through dimensionless functions (for example ratios, exponentials, or standardized scores),

so that the resulting `DeltaS_*` and `Tension_*` are dimensionless.

3.2
A common pattern is:

```txt
DeltaS_raw(m)   = G(m)          # carries physical units
S_ref           = G_ref(domain) # reference scale for the domain
DeltaS_norm(m)  = f( G(m) / S_ref )
```

where:

* `G(m)` is an observable with units,
* `G_ref(domain)` is a positive reference value that depends only on the domain or encoding class,
* `f` is a fixed monotone function chosen at the encoding-class level.

3.3
Any tension functional of the form:

```txt
Tension_X(m) = sum_i w_i * DeltaS_i(m)
```

is understood to use normalized, dimensionless `DeltaS_i(m)` defined according to the rule above or an equivalent normalization.
Weights `w_i` are dimensionless coefficients fixed at the encoding-class level.

3.4
This normalization requirement closes the apparent loophole where a ratio like `Delta / rho` could carry units.
In TU, both numerator and denominator are first normalized to dimensionless quantities before any ratio or linear combination is taken.

---

## 4. Allowed rescalings and their scope

4.1
A global change of tension scale is represented by a strictly monotone function:

```txt
phi: [0, +inf) -> [0, +inf)
```

that is applied to all tension values and thresholds in a given TU layer or subprogram.

4.2
Such a rescaling is allowed only if:

* it is declared at the charter level,
* it is applied consistently to all relevant `Tension_*`, `epsilon_*`, and `delta_*` in the affected documents,
* it does not depend on individual experimental outcomes or on the truth value of any canonical problem.

4.3
Problem files may not introduce their own ad hoc rescaling of tension, except for:

* local re parameterizations that are explicitly stated and do not change the ordering of tension values,
* visual rescalings for plotting, clearly labeled as such.

4.4
If a rescaling would change which states fall below or above a fixed threshold, the rescaling must be treated as a change in the underlying tension scale and recorded in the charter history, not as a cosmetic change.

---

## 5. Thresholds and bands

5.1
Thresholds such as `epsilon_*` and `delta_*` are defined relative to the normalized tension scale.
They may be interpreted as:

* upper bounds for "low tension" regimes,
* lower bounds for "persistent high tension" regimes.

5.2
Threshold values may be chosen based on:

* theoretical considerations (for example asymptotic bounds),
* statistical properties of tension distributions in benchmark datasets,
* robustness requirements for experiments.

5.3
Thresholds must not be tuned per problem instance in response to experimental outcomes.
Any change in thresholds that affects the interpretation of previous experiments must be:

* clearly documented,
* justified at the charter or encoding-class level,
* treated as a change in analysis protocol.

5.4
When experiments use tolerance bands or curves rather than single thresholds, the same rules apply:

* bands are defined with respect to the normalized tension scale,
* changes in bands that affect conclusions require documentation and justification.

---

## 6. Unit changes and invariance

6.1
Changing the physical units of underlying observables (for example seconds to minutes, joules to electronvolts) must not change:

* which states are considered low tension or high tension under a fixed encoding,
* the qualitative conclusions of experiments phrased in terms of tension and thresholds.

6.2
To achieve this, normalization must be defined in terms of unit invariant quantities such as:

* ratios of observables to their domain specific reference scales,
* standardized scores based on distributions that transform predictably with units.

6.3
If a proposed definition of `DeltaS_*` or `Tension_*` does not respect unit invariance, it must be revised or rejected at the encoding-class level before it is used in problem files.

---

## 7. Cross-problem comparability

7.1
When the same tension functional is used across multiple problems (for example `Tension_code` in several neural coding or AI interpretability problems), the intention is that:

* the normalized scale is shared across these problems,
* tension values can be meaningfully compared at least qualitatively.

7.2
When different problems use tension functionals with unrelated semantics or normalizations, cross-problem numerical comparisons are discouraged.
In such cases, documents should state explicitly that tension values are only meaningful within each problem.

7.3
If a new problem introduces a variant of an existing tension functional with a different normalization, this must be:

* clearly indicated,
* justified,
* and, if necessary, accompanied by a mapping between the old and new scales.

---

## 8. Implementation guidance and diagnostics

8.1
Implementations that compute `DeltaS_*` and `Tension_*` for simulations or AI models should:

* log both the raw observables and their normalized forms,
* record which reference scales and functions `f` were used,
* provide enough meta data to reconstruct tension values if the normalization scheme is updated.

8.2
When analyzing tension distributions, it is good practice to:

* check for sensitivity to reasonable variations in reference scales,
* verify that qualitative conclusions (for example the existence of a low tension band) are stable.

8.3
If conclusions are highly sensitive to small changes in normalization, the encoding or tension definitions may need to be revised.

---

## 9. Program note

9.1
This charter does not claim that any particular numerical value of tension has a direct physical meaning. The main role of the tension scale is:

* to order configurations into lower and higher tension regimes,
* to support falsifiable statements about encodings and effective theories.

9.2
Future versions of this charter may refine normalization rules or introduce additional constraints as the TU program accumulates more examples and data.
Such changes will be documented and, when possible, accompanied by guidance on how to translate previous tension values into the new scale.
