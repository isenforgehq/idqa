# Intent-Driven Quality Assurance (IDQA): Working Specification and Research Agenda

**Version:** 0.1  
**Date:** 2026-09-28  
**Author:** Rodrigo Candido Costa  
**ORCID:** https://orcid.org/0009-0000-2604-9564  
**Affiliation / research home:** IsenForge Research  
**Status:** Working research proposal; empirical validation ongoing  
**Canonical URL:** https://isenforge.com/idqa/specification/v0.1/
**License:** CC BY-NC 4.0 — https://creativecommons.org/licenses/by-nc/4.0/

## Status notice

IDQA is a research proposal under empirical evaluation. This document defines the current model and research agenda; it does not claim that general effectiveness has already been established.

## 1. Motivation

Modern software engineering can produce implementation and validation artifacts increasingly quickly. This changes the economics of testing, but not the underlying assurance problem: a system may satisfy local assertions while the evidence remains insufficient to establish that a higher-level product intent, journey, constraint or composed behavior has been realized.

> A requirement is not adequately covered merely because an assertion exists for it. The evidence strategy must be compatible with the nature of the guarantee being claimed.

## 2. Working definition

**Intent-Driven Quality Assurance (IDQA)** is a quality-assurance approach in which software quality is assessed by deriving explicit guarantees from product intent, context, constraints and objectives, then determining whether those guarantees are sufficiently supported by appropriate evidence.

Tests, scenarios, automation and executions remain valid techniques and artifacts. IDQA does not assume, however, that they are the durable unit of quality assurance. They may instead be generated, reused, cached or discarded as evidence-producing materializations.

## 3. Core assurance chain

```text
Intent
  → Guarantees
  → Evidence Requirements
  → Evidence Strategies
  → Observations
  → Evidence
  → Assurance
```

- **Intent** expresses what reality the software is expected to create or preserve.
- **Guarantees** state what must be supportably true.
- **Evidence Requirements** describe what must be observable or demonstrated without prematurely binding the requirement to a particular tool.
- **Evidence Strategies** materialize appropriate ways to obtain that evidence.
- **Observations** describe what actually happened.
- **Evidence** is provenance-bearing support or contradiction relevant to a guarantee.
- **Assurance** is the bounded conclusion that the available evidence permits.

## 4. Candidate methodological propositions

### 4.1 Evidence must match the claim

Different guarantees may require different evidence. A final-state assertion may be sufficient for a narrow deterministic property while being inadequate for a temporal journey, visual manifestation, cross-service invariant or composed user-facing behavior.

### 4.2 Local evidence does not automatically compose

Evidence supporting child/component guarantees does not automatically establish a parent or composite guarantee. Claims must be supported at the level at which they are made.

### 4.3 Context can extend the assurance boundary

The unit of development may be smaller than the unit of assurance. Dependencies, preconditions, architectural invariants, downstream effects and cross-cutting constraints can create guarantees that are not visible inside a local feature description.

### 4.4 Unknown is a valid conclusion

IDQA should distinguish at least `PROVEN`, `VIOLATED`, `INSUFFICIENT_EVIDENCE` and `UNKNOWN`. The absence of evidence must not silently become a positive quality conclusion.

### 4.5 Durable knowledge may outlive test artifacts

IDQA investigates whether Intent, Guarantees and Evidence Requirements can remain durable while scenarios, automation assets, probes and executions are treated according to their actual reuse value. This proposition is currently a hypothesis and must be evaluated for repeatability, auditability, maintenance cost and correctness.

## 5. Evidence strategies

IDQA is intentionally technique-agnostic. Depending on the guarantee and available access, suitable strategies may include deterministic tests, browser or API execution, runtime traces, static/source analysis, visual or multimodal observations, simulation, exploratory investigation, production telemetry, model-based judgment or human review. No single technique is assumed to be universally sufficient.

## 6. Relationship to existing QA

IDQA is not proposed as a replacement for software testing, verification, validation, exploratory testing, observability, assurance cases or other established quality techniques. The research question is whether these techniques can be organized around an explicit intent-to-guarantee-to-evidence model that produces better bounded conclusions about the software than test-artifact coverage alone.

## 7. Initial research questions

- **RQ1.** Can test-centric baselines remain green in the presence of known intent-level violations?
- **RQ2.** Does IDQA improve detection of known intent-level gaps on held-out systems or experimental worlds?
- **RQ3.** Which combinations of evidence add unique signal rather than redundant cost?
- **RQ4.** Does explicit composite assurance expose failures missed by child/component checks?
- **RQ5.** Can scenarios and executions be ephemeral without materially harming repeatability or assurance quality?
- **RQ6.** Does explicit uncertainty reduce unsupported positive conclusions?

## 8. Evaluation discipline

The methodology should not be evaluated only on examples that contributed to its creation. The planned program separates hypothesis-origin observations from calibration cases, held-out cases and adversarial or contradictory cases.

Candidate metrics include known-gap recall, precision, false-positive rate, unsupported-conclusion rate, correct-unknown rate, time, cost, evidence diversity and transfer performance.

## 9. Reference implementation

**OmniQA** is the reference implementation currently used to operationalize and challenge IDQA. It is expected to model features, context, guarantees, evidence requirements, observations, evidence, unknowns and composite assurance while reusing existing testing and execution infrastructure where appropriate.

OmniQA is not treated as independent proof that IDQA is correct. A successful implementation demonstrates feasibility; comparative and held-out experiments are required to support methodological claims.

## 10. Current limitations

Version 0.1 does not establish that IDQA generalizes across software domains, that its evidence model is optimal, that qualitative product judgment can be fully operationalized, or that ephemeral test materializations are always preferable. The related-work review is still being expanded, and the main confirmatory experimental protocol has not yet been preregistered.

## 11. License

This working specification and the public IDQA methodology text are licensed under **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**. Non-commercial sharing and adaptation are permitted with attribution under the license terms. Commercial use requires separate permission from the rights holder.

## 12. Working citation

Costa, Rodrigo Candido. “Intent-Driven Quality Assurance (IDQA): Working Specification and Research Agenda.” Version 0.1. IsenForge Research, 28 September 2026. https://isenforge.com/idqa/specification/v0.1/

DOI: pending.  
ORCID linkage: pending.  
Peer review: not yet peer reviewed.

Future versions will preserve the v0.1 record rather than silently overwriting its intellectual history.

