# Learning Graph Generator Session Log

**Skill Version:** 0.05  
**Date:** 2026-05-21  
**Project:** AP Psychology Intelligent Textbook  
**Directory:** /Users/dan/Documents/ws/psychology

---

## Summary

Successfully generated a complete learning graph for AP Psychology from the College Board CED (Fall 2024). The graph contains 387 concepts, 587 dependency edges, 12 taxonomy categories, and a valid DAG structure.

---

## Step Results

| Step | Description | Result |
|---|---|---|
| 0 | Setup — copied Python scripts to docs/learning-graph/ | ✅ |
| 1 | Course description quality check | Skipped — score 100/100 (above 85 threshold) |
| 2 | Generate concept labels | ✅ 387 concepts written to concept-list.md |
| 3 | Generate dependency graph CSV | ✅ learning-graph.csv created |
| 4 | Quality validation | ✅ Valid DAG, 0 cycles, 0 orphans, 1 component |
| 5 | Concept taxonomy | ✅ 12 categories written to concept-taxonomy.md |
| 5b | taxonomy-names.json | ✅ Created |
| 6 | Add taxonomy to CSV | ✅ TaxonomyID column added via Python script |
| 7 | metadata.json | ✅ Created |
| 8 | color-config.json | ✅ 12 colors assigned |
| 9 | Generate learning-graph.json | ✅ 387 nodes, 587 edges |
| 10 | Taxonomy distribution report | ✅ taxonomy-distribution.md created |
| 11 | Update index.md | ✅ Customized for AP Psychology |
| 12 | Session log | ✅ This file |
| — | mkdocs.yml nav updated | ✅ All 7 learning-graph pages added |

---

## Python Program Versions Used

| Program | Version | Notes |
|---|---|---|
| analyze-graph.py | (from skill 0.05) | Fixed cycle: concept 131 depended on 132 which depended back on 131 — resolved by giving Multi-Store Memory Model deps of 1\|83 |
| csv-to-json.py | v0.04 | Reported in stdout |
| add-taxonomy.py | (from skill 0.05) | Config format used "range" not "ids" — replaced with custom Python inline script |
| taxonomy-distribution.py | (from skill 0.05) | Ran cleanly |

---

## Graph Statistics

| Metric | Value |
|---|---|
| Total concepts | 387 |
| Total edges | 587 |
| Taxonomy categories | 12 |
| Foundational concepts (no prereqs) | 1 (Psychology as a Science) |
| Terminal nodes | 203 (52.5%) |
| Orphaned nodes | 0 |
| Connected components | 1 |
| Max chain length | 14 |
| Cycles | 0 |
| Average dependencies per concept | 1.52 |

**Top concepts by indegree (most prerequisite-to):**

1. Defining Psychological Disorders (24)
2. Psychology as a Science (23)
3. Scientific Method in Psychology (23)
4. Central Nervous System (15)
5. Neurotransmitters (15)

---

## Taxonomy Distribution

| TaxonomyID | Category | Count | % |
|---|---|---|---|
| CLIN | Clinical Psychology | 54 | 14.0% |
| BIO | Biological Bases of Behavior | 46 | 11.9% |
| DEV | Development Across the Lifespan | 37 | 9.6% |
| SOC | Social Psychology | 37 | 9.6% |
| MEM | Memory | 36 | 9.3% |
| CHEM | Neurochemistry and Psychopharmacology | 34 | 8.8% |
| PERS | Personality and Motivation | 31 | 8.0% |
| LEARN | Learning and Conditioning | 27 | 7.0% |
| SEN | Sensation and Perception | 26 | 6.7% |
| COG | Cognition and Thinking | 24 | 6.2% |
| FOUND | Foundation and Research Methods | 21 | 5.4% |
| HLTH | Health Psychology and Well-Being | 14 | 3.6% |

---

## Files Created

- `docs/learning-graph/concept-list.md` — 387 concept labels
- `docs/learning-graph/learning-graph.csv` — dependency graph with TaxonomyID column
- `docs/learning-graph/learning-graph.json` — complete vis-network JSON
- `docs/learning-graph/concept-taxonomy.md` — 12 taxonomy categories
- `docs/learning-graph/taxonomy-names.json` — taxonomy ID to name mapping
- `docs/learning-graph/metadata.json` — Dublin Core metadata
- `docs/learning-graph/color-config.json` — taxonomy color assignments
- `docs/learning-graph/quality-metrics.md` — graph quality analysis
- `docs/learning-graph/taxonomy-distribution.md` — distribution report
- `docs/learning-graph/index.md` — updated intro page
- `docs/learning-graph/taxonomy-config.json` — taxonomy ID range config (intermediate)
- `logs/learning-graph-generator-0.05-2026-05-21.md` — this session log

---

## Notes

- One cycle found and fixed during Step 4: `Multi-Store Memory Model (131)` had dependencies `132|133|134` but `Sensory Memory (132)` depended back on `131`. Fixed by changing concept 131's dependencies to `1|83`.
- The `add-taxonomy.py` script uses `range` format in config, not `ids` lists. A custom inline Python script was used instead to assign non-contiguous ID ranges to taxonomy categories.
- Terminal node percentage (52.5%) is above the recommended 5–40% range. This is expected for a broad survey course where many specialized concepts (individual neurotransmitters, specific disorder subtypes, etc.) are endpoints rather than prerequisites for other concepts.

---

## Next Steps

1. Review `concept-list.md` and adjust any concept labels before generating chapters
2. Run `/book-installer` with the learning graph viewer option to visualize the graph interactively
3. Run `/book-chapter-generator` after reviewing concept taxonomy and chapter overview
