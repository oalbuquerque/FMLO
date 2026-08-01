# FMLO: Fairness in Machine Learning Ontology

FMLO (Fairness in Machine Learning Ontology) is an ontology designed for the semantic representation of the fairness landscape in machine learning.
It is grounded in the Basic Formal Ontology (BFO) and reuses established fairness- and statistics-related resources, integrating bias sources, sensitive attributes, sociotechnical solutions, and fairness notions into a unified, computable framework to support fairness-aware analysis, auditing, and decision-making across the ML lifecycle.

* **Ontology IRI:** `https://w3id.org/FMLO/ontology` \[replace with your registered w3id, or your GitHub Pages raw file URL if you have not registered one yet, e.g. `https://[seu-usuario].github.io/FMLO/ontology.owl`]

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

* **OWL (RDF/XML):** `[https://w3id.org/FMLO/fmlo.owl](https://w3id.org/FMLO/fmlo.owl)`
* **Turtle:** `[https://w3id.org/FMLO/fmlo.ttl](https://w3id.org/FMLO/fmlo.ttl)`
* **Documentation:** `https://w3id.org/FMLO/doc`

## How to Cite

If you use FMLO in academic work, please cite it as:

Otávio de Paula Albuquerque. FMLO: Fairness in Machine Learning Ontology. 2026. Available at: `[https://w3id.org/FMLO/ontology](https://w3id.org/FMLO/fmlo.owl)`

Or use the BibTeX entry:

```bibtex
@misc{fmlo2026,
  author       = {Albuquerque, Otávio de Paula},
  title        = {FMLO: Fairness in Machine Learning Ontology},
  year         = {2026},
  howpublished = {\url{https://w3id.org/FMLO/ontology}},
  note         = {Version 1.0}
}
```
