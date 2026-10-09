---
layout: home
title: Home
nav_order: 1
---

<div style="text-align: center; margin: 2rem 0 2.5rem 0;">
  <img src="{{ '/assets/CLAIM-logo.jpg' | relative_url }}" alt="CLAIM Logo" style="max-width: 480px; width: 100%;" />
</div>

# Checklist for Artificial Intelligence in Medical Imaging (CLAIM): Explanation, Elaboration and Examples

{: .note }
**Quick links:** [CLAIM Guideline site](https://pubs.rsna.org/page/ai/claim) &nbsp;·&nbsp; [Checklist 2024 (Word)](https://pubs.rsna.org/pb-assets/AI/CLAIM/CLAIMChecklist-6142024-1718376172847.docx) &nbsp;·&nbsp; [CLAIM 2024 Update](https://pubs.rsna.org/doi/10.1148/ryai.240300) &nbsp;·&nbsp; [Published article](https://doi.org/10.1148/ryai.260835)

{: .highlight }
**How to cite:** Akinci D'Antonoli T, Adams LC, Amyar A, et al. Checklist for Artificial Intelligence in Medical Imaging (CLAIM): Explanation, Elaboration, and Examples. *Radiol Artif Intell* 2026; 8:e260835. [https://doi.org/10.1148/ryai.260835](https://doi.org/10.1148/ryai.260835)

---

## Introduction

Artificial intelligence (AI) offers promising applications in disease detection, diagnosis, workflow optimization, and clinical decision-making. The exponential growth of AI research in medical imaging has created unprecedented opportunities for clinical implementation. However, the inherent methodological complexities of AI studies present significant challenges. The literature is replete with inconsistently reported studies that cannot be adequately evaluated by readers and replicated by researchers. These shortcomings contribute to a proliferation of non-reproducible research, ultimately hindering the reliable clinical translation of AI innovations in imaging [(1)](https://doi.org/10.1148/ryai.220081). To address these challenges, adherence to domain-specific reporting guidelines is essential. Such guidelines ensure that AI research in medical imaging is communicated with the rigor, transparency, and reproducibility required for both scientific integrity and clinical trustworthiness.

The Checklist for Artificial Intelligence in Medical Imaging (CLAIM) was introduced in 2020 to support comprehensive and standardized reporting practices, tailored to the distinctive features of AI studies in imaging [(2)](https://doi.org/10.1148/ryai.2020200029). Since its release, CLAIM has served as a valuable tool for researchers, peer reviewers, and journal editors—clarifying study objectives, methodology, data sources, and model evaluation. Its impact is evident from the rapid rise in citations, reflecting its broad adoption and influence in the field of medical imaging [(3)](https://doi.org/10.1148/ryai.240300). Recognizing the rapid advancements in AI technologies and the increasing complexity of methodologies since 2020, the CLAIM Steering Committee published an update in 2024 [(3)](https://doi.org/10.1148/ryai.240300). This CLAIM 2024 Update was guided by a structured Delphi consensus process involving 72 experts from diverse backgrounds, including physicians from a variety of medical imaging–related specialties, AI scientists, journal editors, and statisticians [(3)](https://doi.org/10.1148/ryai.240300). The resulting CLAIM 2024 Update refines and expands the original checklist, introduces a "Not Applicable" option for each item to improve flexibility, and clarifies ambiguous terminology. Notably, the term "ground truth" has been replaced with "reference standard," and the terms "internal testing" and "external testing" are recommended instead of "validation" to mitigate ambiguities. Item 11 of the original checklist has been removed.

This article provides a detailed explanation and elaboration of each item in the CLAIM 2024 Update, supplemented by illustrative examples from the literature that demonstrate appropriate adherence to each item. The objective of this paper is to support researchers and reviewers in the accurate and effective application of the CLAIM guideline. By clarifying the intent and proper implementation of each item, this paper aims to reduce common misinterpretations and encourage effective use of the checklist [(4)](https://doi.org/10.1007/s00330-023-10243-9). Enhancing the correct use of CLAIM is intended to improve the overall quality of reporting and, in turn, promote greater transparency, standardization, and reproducibility in AI research within medical imaging and ultimately facilitating its safe and reliable integration into clinical practice.

---

## How to Use This Document

This document explains the CLAIM items in detail; each section includes the item's definition and continues with an explanation and elaboration of the item, accompanied by illustrative examples from the literature showing how each item should be appropriately addressed.

Text of the CLAIM guideline is included verbatim by permission of the Radiological Society of North America (RSNA). Incorporation of text from RSNA journals, particularly from *Radiology: Artificial Intelligence*, is provided with RSNA's permission. Text from other articles is provided under the Creative Commons (CC) license, as noted in the references. For simplicity citations are removed from the original text, and ellipses are used to indicate removals and to ensure all manipulations remain traceable. This rule applies to both CLAIM excerpts and examples.

**To navigate**, use the sidebar on the left:

- **[CLAIM 2024 Checklist](checklist.md)** — Interactive checklist with checkboxes and page/line fields; print or export to PDF.
- **[CLAIM 2024 Items](claim-items.md)** — All 44 items grouped by section. Each item page contains:
  1. The item's **definition** (as specified in the CLAIM 2024 guideline)
  2. An **explanation and elaboration** of the item's intent
  3. Illustrative **examples from the literature** demonstrating appropriate adherence
- **[References](references.md)** — Full reference list.

{: .note }
Site content is licensed under [CC BY-NC-ND 4.0](https://github.com/RSNA/CLAIM/blob/main/LICENSE); site code and tooling are licensed under [MIT](https://github.com/RSNA/CLAIM/blob/main/LICENSE-CODE). Illustrative examples and CLAIM guideline text retain their original copyright and permissions as described above.
