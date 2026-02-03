# Supplementary Material
This appendix provides implementation details, extraction examples, evaluation statistics, and baseline comparisons for the main paper.
More details, see - [**AIED_appendix.pdf**](https://anonymous.4open.science/r/AIED_supplementary_material_submission613-C453/AIED_appendix.pdf).


## Contents

| Section | Page | Description |
|---------|------|-------------|
| §1 | 1 | **Implementation Details** — Full hyperparameters and model configurations |
| §2 | 2–5 | **Skill Extraction Examples** — Explicit vs. implicit extraction with evidence spans |
| §3 | 5 | **KG Statistics** — Overall extraction and grounding coverage |
| §4 | 5–6 | **Inter-Annotator Agreement** — Annotation protocol and evaluator details |
| §5 | 6–7 | **Baseline Comparison** — KW and ZS-LLM baselines with quantitative results |
| §6 | 7–8 | **Generalization** — Cross-discipline extensibility (Physics case study) |

---

## Tables

- **Table 1** (p.1): Pipeline hyperparameters, thresholds, and model configurations
- **Table 2** (p.5): Knowledge graph construction statistics (grounding coverage, evidence preservation)
- **Table 3** (p.7): Baseline comparison on 50-module test set (Extraction / Grounding / Inference metrics)

---

## Quick Reference

### §1 Implementation Details
Complete configuration for all pipeline components: knowledge integration, skill extraction, graph construction, and pathway planning.

### §2 Skill Extraction Examples
- **§2.1** Explicit extraction with character-level evidence spans (Linear Algebra example)
- **§2.2** Implicit prerequisite inference without direct textual evidence
- **§2.3** Design rationale for two-tiered extraction approach

### §3 KG Statistics
- 108 modules processed → 1,735 module–skill relations
- 93% grounding coverage (Stage 1 ∪ Stage 2)
- 89.2% relations with character-level evidence spans

### §4 Inter-Annotator Agreement
Two domain experts evaluated 265 sampled relations across 5 dimensions (Q1–Q5).

### §5 Baseline Comparison
| Method | Extraction F1 | Grounding Cov. | Inference Prec. |
|--------|---------------|----------------|-----------------|
| KW | 0.55 | – | 0.38 |
| ZS-LLM | 0.70 | 43% | 0.51 |
| **Ours** | **0.85** | **93%** | **0.71** |

### §6 Generalization
Physics pilot (16 modules): 87.4% extraction quality, 84% grounding coverage — demonstrates cross-discipline extensibility.
