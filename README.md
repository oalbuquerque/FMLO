# FMLO: Fairness in Machine Learning Ontology

FMLO (Fairness in Machine Learning Ontology) is an ontology designed for the semantic representation of the fairness landscape in machine learning.
It is grounded in the Basic Formal Ontology (BFO) and reuses established fairness- and statistics-related resources, integrating bias sources, sensitive attributes, sociotechnical solutions, and fairness notions into a unified, computable framework to support fairness-aware analysis, auditing, and decision-making across the ML lifecycle.

* **Ontology IRI:** [https://w3id.org/FMLO/fmlo.owl](https://w3id.org/FMLO/fmlo.owl)

**Maintainer:** [Otávio de Paula Albuquerque](https://github.com/oalbuquerque) (GitHub ID: `oalbuquerque`) | [Google Scholar](https://scholar.google.com/citations?hl=pt-BR&user=53VMpVEAAAAJ) | [ORCID](https://orcid.org/0000-0002-2504-3707) | [Lattes](http://lattes.cnpq.br/4045514018382962)

## Motivation

The rapid adoption of machine learning in high-stakes decision-making has been accompanied by growing evidence of algorithmic bias and discrimination, yet fairness-related knowledge remains fragmented across heterogeneous definitions, metrics, techniques, and assumptions. FMLO addresses this fragmentation by providing a semantic framework to model concepts such as:

* Bias sources across the ML lifecycle
* Sensitive attributes and their legal classification
* Sociotechnical solutions for bias mitigation and discovery
* Fairness notions, classified along ethical, normative, sociotechnical, methodological, and criterion-level dimensions
* Fairness metrics and their mathematical operationalization
* The relation between those areas above


## Scope and Integration

The ontology is implemented in OWL 2 using Protégé, following the OntoForInfoScience methodology for ontology development. It follows ontology engineering best practices and reuses external ontologies such as BFO, STATO, OBI, and the Fairness Metrics Ontology (FMO), and is aligned with the Data Privacy Vocabulary (DPV) for its legal framework classes.

The ontology comprises 156 classes, 104 object properties, 16 data properties, and 121 individuals, totaling 2,754 axioms, and was validated through automated reasoning (HermiT), LLM-assisted auditing, and expert panel review.

## Downloads

The latest stable release of FMLO is available at:

* **OWL (RDF/XML):** [https://w3id.org/FMLO/fmlo.owl](https://w3id.org/FMLO/fmlo.owl)
* **Turtle:** [https://w3id.org/FMLO/fmlo.ttl](https://w3id.org/FMLO/fmlo.ttl)
* **Documentation:** `https://w3id.org/FMLO/`

## Maintenance and Versioning

FMLO follows a formal maintenance and evolution policy, also declared in the ontology header annotations, so that it can keep pace with changes in fairness research and in the legal instruments that frame it.

### Versioning

Releases follow semantic versioning (`MAJOR.MINOR.PATCH`) and are identified by `owl:versionIRI` and `owl:versionInfo`, with `owl:priorVersion` pointing to the previous release.

| Release type | When it is used |
| --- | --- |
| **PATCH** | Corrections to annotations (e.g., `skos:definition`, `rdfs:label`) that do not change logical axioms |
| **MINOR** | New classes, properties, individuals, or restrictions that preserve all previously valid inferences |
| **MAJOR** | Changes that modify or remove existing axioms or alter the alignment with BFO |

### Update triggers

A new release is prepared when one of the following occurs:

- **Periodic:** the scoping review search protocol is re-executed at least every two years to incorporate new fairness notions, techniques, and terminology.
- **Regulatory:** a legal or regulatory instrument affecting sensitive data or automated decision-making enters into force, such as an ANPD regulation of Article 20 of the Brazilian General Data Protection Law (LGPD).
- **Corrective:** inconsistencies or gaps are reported by users or reviewers through [GitHub Issues](../../issues).

### Change workflow

Every change goes through five steps before release:

1. A documented request identifying the affected conceptual cluster and its bibliographic or legal source.
2. Modeling of the change, including bilingual (English/Portuguese) `skos:definition` and `rdfs:label` annotations and `rdfs:isDefinedBy` provenance.
3. A consistency check with the HermiT reasoner.
4. Regression testing of the competency questions through the SPARQL query suite; every question must keep returning non-empty, semantically coherent results.

### Deprecation

Terms are never deleted. Obsolete classes and properties are marked with `owl:deprecated` and, when a successor exists, annotated with the IAO property *term replaced by* (`IAO_0100001`), so that IRIs remain stable for any resource referencing earlier versions.

## Changelog

### v1.1.0
- Added formal maintenance and versioning policy to the ontology header.
- Extended the legal framework cluster to the level of legal provisions (`LegalProvision`), with the property chain `protectedByProvision ∘ isProvisionOf → protectedBy`.
- Aligned sensitive attributes with LGPD provisions (Art. 5, II; Art. 6, IX; Art. 11; Art. 20).
- Added Brazilian anti-discrimination legislation (Laws No. 9,029/1995, 7,716/1989, and 13,146/2015).
- Added ANPD regulatory instruments (`RegulatoryInstrument`), annotated as preparatory.
- Reworded the definitions of `Continuous`, `Age`, `Gender`, `Causal`, and `Geometric` to remove verbal repetition of the defined term.

### v1.0.0
- Initial release, as presented in the doctoral thesis.

## How to Cite

If you use FMLO in academic work, please cite it as:

Otávio de Paula Albuquerque. FMLO: Fairness in Machine Learning Ontology. 2026. Available at: `[https://w3id.org/FMLO/ontology](https://w3id.org/FMLO/fmlo.owl)`

Or use the BibTeX entry:

```bibtex
@misc{otavio2026fmlo,
  author       = {de Paula Albuquerque, Otavio},
  title        = {FMLO: Fairness in Machine Learning Ontology},
  year         = {2026},
  howpublished = {\url{https://w3id.org/FMLO/ontology}},
  note         = {Version 1.0}
}
```
