# Intent-Driven Quality Assurance (IDQA)

**Intent-Driven Quality Assurance (IDQA)** is a methodological research proposal by **Rodrigo Candido Costa**, developed through **IsenForge Research**.

Working definition:

> IDQA is a quality-assurance approach in which software quality is assessed by deriving explicit guarantees from product intent, context, constraints and objectives, then determining whether those guarantees are sufficiently supported by appropriate evidence.

Core working chain:

    Intent
      → Guarantees
      → Evidence Requirements
      → Evidence Strategies
      → Observations
      → Evidence
      → Assurance

## Status

**Working research proposal — v0.1.**

IDQA is under empirical evaluation. This repository should not be read as a claim that general effectiveness, superiority or cross-domain generality has already been established.

## Current public specification

Canonical page:
https://isenforge.com/idqa/specification/v0.1/

Research hub:
https://isenforge.com/research/

## Relationship to OmniQA

**IDQA** is the methodology/research proposal.

**OmniQA** is the reference implementation used to operationalize and empirically challenge the model.

A successful OmniQA implementation demonstrates feasibility; it is not by itself proof that IDQA's methodological claims are correct.

## Research direction

Current research questions include:
- whether test-centric baselines can remain green while intent-level violations persist;
- whether heterogeneous evidence adds unique assurance signal;
- whether explicit composite assurance exposes failures missed by component checks;
- whether scenarios/executions can be ephemeral without harming repeatability;
- whether explicit uncertainty reduces unsupported positive conclusions.

## Citation

Costa, Rodrigo Candido. “Intent-Driven Quality Assurance (IDQA): Working Specification and Research Agenda.” Version 0.1. IsenForge Research, 28 September 2026.

Version DOI: https://doi.org/10.5281/zenodo.23032992

All-versions DOI: https://doi.org/10.5281/zenodo.23032991

ORCID: https://orcid.org/0009-0000-2604-9564

## License

Methodology text and working specifications: **CC BY-NC 4.0**. Commercial use requires separate permission. OmniQA software and other implementation artifacts are not automatically covered by this content license.

