# Tension Universe Encoding and Fairness Charter (TU-EFC v1.0)

**File**: `TU_ENCODING_AND_FAIRNESS_CHARTER.md`  
**Scope**: All Tension Universe (TU) effective-layer documents that define or use encoding classes, reference families, weights, or thresholds, including the BlackHole S-problem collection.  
**Status**: Working charter, version 1.0  

This charter specifies how TU encodings are defined and constrained, with the goal of preventing hidden label leakage, post hoc tuning, and unfair comparisons.

---

## 1. Purpose and scope

1.1  
An **encoding** in TU is any rule set that:

- constructs or approximates states in a state space `M`,
- defines observables and invariants on `M`,
- computes mismatch terms and tension functionals from these observables.

1.2  
An **encoding class** is a family of encodings that share:

- the same state space structure,
- the same observable definitions,
- the same functional form for mismatch and tension,
- a specified parameter space for tunable coefficients and reference profiles.

1.3  
This charter defines:

- how encoding classes may be introduced,
- how parameters may be chosen or tuned,
- what kinds of information encodings are allowed to depend on,
- what is forbidden in order to preserve fairness and falsifiability.

---

## 2. Definition and registration of encoding classes

2.1  
Each encoding class used in TU must be identified by a stable name, for example `E_code`, `E_fold`, or `E_alignment`.

2.2  
For each encoding class, a specification document (which may be part of a problem file or a separate note) must define at least:

- the state space structure `M` and any auxiliary spaces,
- the set of observables and invariants computed from states in `M`,
- the functional form of mismatch terms `DeltaS_*`,
- the functional form of the tension functional(s), including which mismatch terms and weights are used,
- the parameter space for tunable coefficients and reference profiles.

2.3  
The specification of an encoding class must be written at the TU level, not inside a single instance of an experiment.  
Problem files may constrain or select subclasses of an encoding class, but they may not redefine the class in incompatible ways.

---

## 3. Allowed sources of information for encoding choices

3.1  
Encoding classes and their parameter ranges may depend on:

- general theoretical knowledge about the domain (for example known symmetries, conservation laws, scale separations),
- public benchmark sets chosen before experiments are run,
- practical considerations such as computational tractability and numerical stability.

3.2  
They may not depend on:

- the unknown truth value of a specific canonical problem,
- private or hidden labels indicating which counterfactual world is "actually" realized,
- post hoc inspection of experimental outcomes that are supposed to test the encoding itself.

3.3  
In particular, it is forbidden to choose an encoding class or parameter value solely because it makes one counterfactual world appear low tension and another high tension, when that distinction is not already justified by observables and independent constraints.

---

## 4. Parameter selection and tuning

4.1  
Within a registered encoding class, parameters such as:

- weights `a1, a2, ...`,
- reference profiles for funnels, code families, or baseline behaviors,
- tolerance bands for numerical comparisons,

may be selected or tuned under the following constraints.

4.2  
Pre registered tuning is allowed when:

- the tuning procedure and the data used for tuning are specified in advance,
- the data used for tuning are distinct from the data used to evaluate the encoding in critical experiments,
- the tuning does not use knowledge of the canonical problem's actual resolution.

4.3  
Post hoc tuning is allowed only for:

- exploratory analysis clearly labeled as such,
- the generation of hypotheses for future, independently evaluated experiments.

In such cases, the affected results must be marked as "exploratory" and not used as evidence for or against the canonical problem.

4.4  
Per problem or per instance parameter changes are allowed only if:

- they are drawn from a parameter range specified in the encoding class,
- the selection rule depends only on observables and meta data available before seeing the outcomes that are being used to evaluate the encoding.

---

## 5. Prohibition of label leakage and hidden answers

5.1  
Encodings must not include constructs that directly encode the truth value of a canonical statement or the identity of a counterfactual world, such as:

- indicator fields that are equal to `1` if a hypothesis is true and `0` otherwise,
- special parameter settings that are activated only when a particular answer is assumed.

5.2  
Encodings must not rely on:

- hidden tags that mark data generated under one world or another when the goal is to test whether these worlds can be distinguished from observables alone,
- any external oracle that reveals which world is "real" except where the entire experiment is explicitly about that oracle.

5.3  
File names, component names, and variable names may not be used as carriers for hidden labels that would change the semantics of an encoding when interpreted with secret knowledge.

---

## 6. Stability and nondegeneracy

6.1  
Within an encoding class, small changes in observables or in admissible parameters should not:

- arbitrarily flip the classification of an experiment from "low tension" to "high tension" or vice versa,
- invert the intended ordering of tension across clearly separated regimes without a clear reason.

6.2  
Encoding classes that are so flexible that they can realize arbitrarily low tension for arbitrary data, without meaningful constraints, are considered **non discriminating**. They may be documented but must be clearly marked as such and should not be used as primary encodings for falsifiability statements.

6.3  
Whenever possible, encoding classes should be designed so that:

- there exist realistic scenarios where tension is provably high,
- there exist realistic scenarios where tension is provably low,
- experiments can distinguish between these scenarios without relying on hidden information.

---

## 7. Interaction with experiments

7.1  
Each experiment pattern in a problem file must specify:

- which encoding class it uses,
- which parameter range is allowed,
- whether parameters are fixed, sampled, or tuned,
- what counts as falsification or support for the encoding.

7.2  
Changing the encoding class or the allowed parameter range after seeing experimental outcomes requires:

- explicit documentation of the change,
- resetting or reinterpreting previous results as exploratory rather than confirmatory.

7.3  
Results obtained under different encoding classes must not be conflated. When comparing encodings, each class must be evaluated under the same experimental protocol and fairness constraints.

---

## 8. Updates, retirement, and transparency

8.1  
Encoding classes may be:

- extended (for example by adding new observables or invariants),
- restricted (for example by narrowing parameter ranges),
- retired (no longer used for future experiments),

as the TU program evolves.

8.2  
Whenever an encoding class is changed in a way that affects tension values or experiment outcomes, the change must be:

- recorded in a change log,
- associated with a version number or date,
- reflected in the documentation of affected problem files when practical.

8.3  
Retired encoding classes should remain documented, with a brief explanation of why they were retired (for example conflicts with data, numerical instability, or redundancy).

---

## 9. Program note

9.1  
This charter does not claim that any particular encoding class is uniquely correct or optimal. It only constrains how encodings may be used within the TU program.

9.2  
The fairness constraints here are intended to make TU encodings auditable and falsifiable by external readers, including critics. They do not prevent the introduction of new encodings, but they require that such introductions be done in a way that avoids hidden dependence on unknown answers.
