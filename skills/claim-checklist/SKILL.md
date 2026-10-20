---
name: claim-checklist
description: "Fill out or assess the CLAIM 2024 checklist (Checklist for Artificial Intelligence in Medical Imaging; 44 items, each Yes/No/NA) for a medical imaging AI manuscript. Use when authors need a completed CLAIM checklist for journal submission (e.g., Radiology: Artificial Intelligence), when a reviewer or meta-researcher rates a paper's CLAIM adherence, or when checking which CLAIM items a draft still misses. Triggers: CLAIM, CLAIM 2024, Checklist for Artificial Intelligence in Medical Imaging, imaging AI reporting checklist, reporting guideline adherence."
license: MIT (CLAIM item text © RSNA, reproduced by permission)
---

# CLAIM 2024 Checklist

CLAIM 2024 (Tejani et al., Radiol Artif Intell 2024;6(4):e240300) has 44 items answered Yes, No, or NA. It is a reporting checklist, not a quality score. CLAIM 2020 had 42 items with different numbering; confirm the version if a journal asks for 2020. Radiomics/imaging-biomarker studies are out of scope (suggest CLEAR).

Each item's explanation, elaboration and published examples are at `https://rsna.github.io/claim/item-NN.html` (NN = 01–44; Akinci D'Antonoli et al., Radiol Artif Intell 2026;8:e260835). Consult them for borderline items when web access is available.

## Workflow

1. **Get the whole manuscript**: main text, tables, figure captions, supplements. Confusion matrices, acquisition parameters, demographics tables and code links often sit outside the main text. If part is missing, say so instead of answering No.
2. **Pick the mode.**
   - *Author* (their own paper): for Yes give page/line (section if unnumbered); for No/NA give a one-line reason, and offer draft text for fixable Nos. Also flag "ground truth"/"gold standard" (CLAIM prefers "reference standard") and "validation" used for test data (prefer "internal testing"/"external testing").
   - *Assessor* (someone else's paper): each answer gets a short quote or section pointer as evidence.
3. **Rate every item** with the rules below. One passage can support several items.
4. **Output** the table, then the human-check list.

## Answer rules

- **Yes**: the item's core requirement is reported anywhere in the manuscript or supplement. The guideline's elaboration lists examples of good reporting; not every example is required.
- **No**: the item applies but is absent or only implied. Do not infer from convention (a "random split" is not a patient-level split).
- **NA**: the thing the item asks about does not exist in this study (no ensemble, no clinical trial, no model training). Never use NA for "not reported". Things a study *should* do (robustness, explainability, external testing, sample-size justification, failure analysis, rater variability) are **No** when absent.
- Still unsure after checking everything: give the stricter answer and flag the item.

## Items and item-specific rules

Rules target the 19 items where LLM answers most often disagreed with an adjudicated three-rater human reference (23 imaging AI preprints, 1,012 item judgments).

**Title/Abstract**
- 1 Identification as a study of AI methodology, specifying the category of technology used (e.g., deep learning)
- 2 Summary of study design, methods, results, and conclusions

**Introduction**
- 3 Scientific and/or clinical background, including the intended use and role of the AI approach
- 4 Study aims, objectives, and hypotheses — hypotheses only if not a data-driven approach.

**Methods – Study design**
- 5 Prospective or retrospective study
- 6 Study goal

**Methods – Data**
- 7 Data sources
- 8 Inclusion and exclusion criteria
- 9 Data pre-processing — needs concrete, reproducible steps (resampling, normalization, windowing, bit depth). "Images were preprocessed" → No. Augmentation belongs to 25.
- 10 Selection of data subsets — sub-selection *within* the data: slice/frame selection, cropping, ROI or report-segment extraction. Patient inclusion is item 8. Whole examinations used as-is → NA.
- 11 De-identification methods — needs how protected health information was removed. An ethics approval or consent waiver is not de-identification → No.
- 12 How missing data were handled — silence → No. Stated exclusion of incomplete cases counts as handling → Yes. NA only when no case-level data could be missing (eg, segmentation of complete image volumes); unsure between No and NA → No.
- 13 Image acquisition protocol — needs parameters (vendor/scanner, sequence, slice thickness, kVp, resolution). Naming only the modality or dataset → No.

**Methods – Reference standard**
- 14 Definition of method(s) used to obtain reference standard
- 15 Rationale for choosing the reference standard — Yes if the choice is justified over alternatives **or** its errors, biases or limitations are discussed (often in the Discussion). Merely describing it is item 14.
- 16 Source of reference standard annotations
- 17 Annotation of test set — an annotation procedure described for the whole dataset covers the test set → Yes. NA if the study created no test-set labels of its own (labels reused unchanged from a published dataset); the label source then belongs to item 16.
- 18 Measures of inter- and intra-rater variability of features described by the annotators — agreement statistics, consensus reading, or a stated adjudication rule → Yes. NA if the reference standard is not human annotation (histopathology, follow-up, lab values).

**Methods – Data partitions**
- 19 How data were assigned to partitions
- 20 Level at which partitions are disjoint — Yes only if the level is stated (patient/study/image) or structurally certain (test set from another site or period, one image per patient).

**Methods – Testing data**
- 21 Intended sample size — needs *how* the test-set size was determined (power or precision calculation, explicit justification). Stating N alone → No.

**Methods – Model**
- 22 Detailed description of model
- 23 Software libraries, frameworks, and packages
- 24 Initialization of model parameters — "pretrained on ImageNet", "initialized from [model] weights", fine-tuning a foundation model, or a named random-init scheme → Yes. Often missed: search for "pretrained", "transfer learning", "fine-tuned". NA if no model was trained.

**Methods – Training**
- 25 Details of training approach
- 26 Method of selecting the final model — needs the selection criterion (best tuning-set metric, early stopping rule, checkpoint choice). Describing training alone → No. NA if no model was trained.
- 27 Ensembling techniques — no ensemble → **NA** (the most common error is answering No). Averaged cross-validation fold models or combined networks are ensembles: Yes if components and combination are described, else No.

**Methods – Evaluation**
- 28 Metrics of model performance
- 29 Statistical measures of significance and uncertainty
- 30 Robustness or sensitivity analysis — ablations, multiple seeds, performance by scanner/site/vendor, input perturbations, or threshold variation → Yes.
- 31 Methods for explainability or interpretability
- 32 Evaluation on internal data
- 33 Testing on external data
- 34 Clinical trial registration — **NA** for every retrospective study and every prospective study that is not a clinical trial. Yes/No only for a prospective clinical trial.

**Results – Data**
- 35 Numbers of patients or examinations included and excluded
- 36 Demographic and clinical characteristics of cases in each partition and dataset — needs a breakdown per partition or per dataset. Overall cohort only → No (say so).

**Results – Model performance**
- 37 Performance metrics and measures of statistical uncertainty
- 38 Estimates of diagnostic performance and their precision — do not answer NA just because the task is segmentation, detection or regression; estimates with CIs or equivalent → Yes.
- 39 Failure analysis of incorrect results — confusion matrix, examples of misclassified cases, or analysis of error patterns → Yes. Check figures and supplements.

**Discussion**
- 40 Study limitations
- 41 Implications for practice, including intended use and/or clinical role

**Other information**
- 42 Provide a reference to the full study protocol or to additional technical details — a pointer to a supplement, appendix, code repository, or published protocol with technical details → Yes. Often missed.
- 43 Statement about the availability of software, trained model, and/or data
- 44 Sources of funding and other support; role of funders

## Output

```
| # | Item | Answer | Location | Evidence / reason |
|---|------|--------|----------|-------------------|
| 1 | AI methodology in title/abstract | Yes | p1 l2 | "deep learning" in title |
| 27 | Ensembling technique | NA | – | Single model, no ensemble |
```

Then:
- **Totals**: n Yes / n No / n NA. If a percentage is requested, use Yes / (Yes + No) and state the denominator.
- **Human check**: borderline items with the reason (typically 12, 15, 17, 21, 24, 36, or anything judged from incomplete input).
