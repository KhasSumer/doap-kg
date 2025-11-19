# DOAP-KG: Dynamic Oversight for Agentic Payments Knowledge Graph

DOAP-KG is a governance-focused ontology and knowledge graph for **agentic payment systems**.

The goal of DOAP-KG is to make policies, controls, control executions, exceptions, attestations, risk assessments, and evidentiary artefacts **first-class, queryable objects** that can be linked to payment transactions, agents, rails, channels, and jurisdictions.

This repository contains:

- `ontology/` – the DOAP-KG OWL/Turtle ontology.
- `kg/` – a synthetic but realistic knowledge graph instantiating DOAP-KG.
- `shapes/` – SHACL shapes for governance and data quality constraints.
- `queries/` – SPARQL 1.1 queries implementing the competency questions (CQ1–CQ9).
- `docs/` – additional documentation, examples, and usage notes.

The resource is designed to support:
- **Risk & compliance** (high-risk transactions, overrides, control weaknesses),
- **Product & operations** (what-if scenarios, friction vs. safety trade-offs),
- **Audit & supervision** (decision provenance and explanation),
- **AI governance & model risk** (attestations, AI agents, decision modalities).

The ESWC 2026 resource paper describes the design and evaluation of DOAP-KG and provides the formal citation for this repository.
