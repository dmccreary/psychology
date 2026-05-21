# Learning Graph for AP Psychology

[Open Learning Graph Viewer Fullscreen](../sims/graph-viewer/main.html){ .md-button .md-button--primary }

<iframe src="../sims/graph-viewer/main.html" width="100%" height="600px" frameborder="0"></iframe>

This section contains the learning graph for this textbook. A learning graph is
a graph of concepts used in this textbook. Each concept is represented by a
node in a network graph. Concepts are connected by directed edges that indicate
what concepts each node depends on before that concept is understood by the student.

A learning graph is the foundational data structure for intelligent textbooks that can recommend learning paths.
A learning graph is like a roadmap of concepts to help students arrive at their learning goals.

The AP Psychology learning graph contains **387 concepts** organized into **12 categories**
aligned with the College Board AP Psychology CED (Effective Fall 2024), spanning
5 core content units and research methods as a cross-cutting practice.

## Files

- [Course Description](../course-description.md) — source document (quality score: 100/100)
- [Concept List from College Board](./concept-list-from-college-board.md) — CED seed concepts
- [Concept List](./concept-list.md) — 387 numbered concept labels
- [Learning Graph CSV](./learning-graph.csv) — dependency graph with taxonomy
- [Learning Graph JSON](./learning-graph.json) — vis-network format (387 nodes, 587 edges)

## Analysis & Documentation

- [Course Description Assessment](course-description-assessment.md) — quality score: 100/100
- [Graph Quality Analysis](quality-metrics.md) — valid DAG, 0 cycles, single connected component
- [Concept Taxonomy](concept-taxonomy.md) — 12 categories aligned to AP CED units
- [Taxonomy Distribution Report](./taxonomy-distribution.md) — all categories under 30% threshold

## Taxonomy Color Legend

| TaxonomyID | Category | Color |
|---|---|---|
| FOUND | Foundation and Research Methods | SteelBlue |
| BIO | Biological Bases of Behavior | DarkGreen |
| CHEM | Neurochemistry and Psychopharmacology | Teal |
| SEN | Sensation and Perception | DodgerBlue |
| COG | Cognition and Thinking | Gold |
| MEM | Memory | DarkGoldenrod |
| DEV | Development Across the Lifespan | MediumPurple |
| LEARN | Learning and Conditioning | LimeGreen |
| SOC | Social Psychology | Crimson |
| PERS | Personality and Motivation | DarkOrchid |
| HLTH | Health Psychology and Well-Being | Coral |
| CLIN | Clinical Psychology | DarkSlateBlue |

Use the `/book-installer` skill to add an interactive graph viewer
once `learning-graph.json` exists.
