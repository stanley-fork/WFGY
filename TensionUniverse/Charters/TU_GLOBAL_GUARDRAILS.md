# TU Global Guardrails and Global Coherence Policy

## 0. Scope and intent

This document defines global guardrails for the Tension Universe effective layer specifications, and a cross problem coherence policy.
It is a program level constraint document.
It applies to every problem entry unless an entry explicitly declares a scoped exception that is itself auditable and non adaptive.

## 1. No hidden solution assumption

1.1 Non dependence on the unknown truth value  
Encoding choices, weights, reference families, thresholds, and probe sets must not depend on the unknown truth value of the canonical statement of any specific problem.

1.2 No uninterpreted answer channel  
No encoding may encode the canonical answer as an uninterpreted label, privileged feature, hidden parameter, or any equivalent information channel.

## 2. Reference use restrictions

2.1 References define admissible families, not truth  
References may be used only to define admissible measurement families, public baselines, and hard constraints.
They must not be used to import any claim about the canonical statement’s truth.

2.2 Exclusion rule for solution asserting references  
Any reference that directly asserts a solution, disproof, or privileged oracle for a specific canonical statement is out of scope for the corresponding encoding.
Such a reference may be cited only as historical context, never as an admissibility basis.

## 3. Experiments test encodings only

3.1 What experiments mean  
Experiments described in any TU problem entry test the coherence, stability, and usefulness of the encoding.
They do not test the truth of the underlying canonical statement.

3.2 Passing is not evidence of solving  
Falsifying an encoding is not solving the canonical problem, and passing tests is not evidence of a solution.

3.3 Observability failure rule  
If required observables cannot be reliably estimated, the outcome must be recorded as inconclusive.
It must not be presented as supportive evidence.

## 4. Effective layer boundary and wording discipline

4.1 Effective layer only  
All objects used in TU problem entries live at the effective layer, including state spaces, observables, invariants, tension scores, and counterfactual worlds.

4.2 No constructive mapping claim to deep layer  
No entry may provide or imply a constructive mapping from raw data into internal TU deep fields, nor expose any deep generative rule or first principle axiom system.

4.3 No ontological implication  
No deep layer mechanism is implied by any wording in an effective layer entry.
Implementation details that map raw data to effective summaries are outside scope and carry no TU ontological claim.

## 5. Canonical statement precedence

The canonical statement in Section 1 of any entry always takes precedence over any narrative, heuristic, or interpretive commentary in later sections.
If a conflict is discovered, the correct action is to revise the commentary, not to reinterpret the canonical statement.

## 6. Global coherence policy across problems

This section defines cross problem consistency requirements.
When a term appears across multiple entries, it must preserve its declared role and type.

6.1 DeltaS role consistency  
All symbols of the form DeltaS_* denote effective layer mismatch terms on a fixed tension scale.
They are dimensionless or normalized quantities.
They must not silently change meaning from error, to constraint slack, to a domain specific physical variable without an explicit type declaration.

6.2 Tension type discipline  
A symbol of the form Tension_* must declare its type in each entry:
either a scalar score, a field over a state space, or a time indexed functional.
If an entry uses a field form, the scalar reported value must be a declared aggregator functional, with an explicit definition.
No entry may mix scalar and field interpretations without stating the mapping.

6.3 Counterfactual definition compatibility  
All counterfactual worlds used in TU entries must satisfy:
a declared intervention grammar, admissibility conditions, and invariance constraints.
If an entry uses a domain specific counterfactual rule, it must be expressed as a specialization of the shared counterfactual schema, not as an incompatible alternative.
If two entries cannot share a compatible schema, the conflict must be explicitly marked, and the involved entries must be treated as belonging to disjoint counterfactual regimes.

6.4 Cross domain assumption collisions  
If an entry assumes compressibility, ergodicity, or any analogous regularity, and another entry assumes the opposite in a shared scope, the pair must be treated as a declared regime split.
Regime splits must be labeled and must include a testable discriminator observable.

6.5 E_level and N_level escalation rule  
Verification level escalation must not be implicit.
Any entry that claims an E_level or N_level above the baseline used by the collection must provide:
a stronger observability contract, a stricter falsification block, and a logging and reproducibility plan that exceeds the baseline.
Otherwise the entry must be treated as baseline level and must not use higher level language.

## 7. Failure modes

An encoding is considered failed if any of the following holds:

7.1 Instability under admissible perturbations  
Small admissible perturbations of measurement choices, within the declared encoding class, produce qualitatively unstable conclusions.

7.2 Conflict with established results  
The encoding contradicts established theorems or hard constraints in the cited field, under the declared interpretation.

7.3 Non auditability  
The encoding cannot be externally audited because required identifiers, probe sets, weights, thresholds, and version tags are missing or ambiguous.

## 8. Versioning and non mutation

8.1 Semantic changes require a new version  
Any non trivial change to encoding choices, probe sets, normalization rules, thresholds, or weights defines a new encoding version and must be logged with explicit version tags and hashes.

8.2 Charter level changes for multi problem effects  
Any change that affects multiple problems must be made at the charter or program level documents, not by silent local edits to individual problem files.
