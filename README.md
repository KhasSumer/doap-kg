# DOAP-KG: Dynamic Oversight for Agentic Payments Knowledge Graph

DOAP-KG is a governance-focused ontology and knowledge graph for **agentic payment systems**.

The goal of DOAP-KG is to make policies, controls, control executions, exceptions, attestations, risk assessments, and evidentiary artefacts **first-class, queryable objects** that can be linked to payment transactions, agents, rails, channels, and jurisdictions.

**Note:** DOAP-KG (Dynamic Oversight for Agentic Payments) is unrelated to the DOAP “Description of a Project” vocabulary; our namespace prefix is `doapk:` (`https://w3id.org/doap-kg#`).


This repository contains:

- `ontology/` – the DOAP-KG OWL/Turtle ontology.
- `kg/` – a synthetic but realistic knowledge graph instantiating DOAP-KG.
- `shapes/` – SHACL shapes for governance and data quality constraints.
- `queries/` – SPARQL 1.1 queries implementing the competency questions (CQ1–CQ9).
- `docs/` – additional documentation, examples, and usage notes.

## Validate (SHACL)
Example SPARQL query outputs (synthetic KG) are available in `docs/query-results.md`.

You can validate DOAP-KG data against the SHACL constraints using `pyshacl`.

### Install
```bash
pip install pyshacl

pyshacl \
  -s shapes/doap-kg-shapes.ttl \
  -d kg/doap-kg-synthetic.ttl \
  -e ontology/doap-kg.ttl \
  -i rdfs \
  -f human
```


Validate the synthetic KG

The resource is designed to support:
- **Risk & compliance** (high-risk transactions, overrides, control weaknesses),
- **Product & operations** (what-if scenarios, friction vs. safety trade-offs),
- **Audit & supervision** (decision provenance and explanation),
- **AI governance & model risk** (attestations, AI agents, decision modalities).

The ESWC 2026 resource paper describes the design and evaluation of DOAP-KG and provides the formal citation for this repository.

## Links and citation

- Persistent URI (w3id): **https://w3id.org/doap-kg**
- Repository: https://github.com/KhasSumer/doap-kg
- Archived release (Zenodo): [[10.5281/zenodo.18330294](https://doi.org/10.5281/zenodo.18330294)](https://doi.org/10.5281/zenodo.18332082)
- Queries live here: [queries/queries/queries/](queries/queries/queries/)
- Ontology (TTL): [ontology/doap-kg.ttl](ontology/doap-kg.ttl)
- SHACL shapes: shapes/doap-kg-shapes.ttl



### Cite this work

Shukanayev, D. (2025). *DOAP-KG: A Governance-Focused Knowledge Graph for Dynamic Oversight of Agentic Payments*. ESWC 2026 Resource Track. [[https://doi.org/10.5281/zenodo.18330294](https://doi.org/10.5281/zenodo.18330294)](https://doi.org/10.5281/zenodo.18332082)


## License

- Ontology and synthetic knowledge graph: **CC BY 4.0** (see `LICENSE-CC-BY-4.0.md`)
- Code, scripts, and configuration: **Apache 2.0** (see `LICENSE`)
