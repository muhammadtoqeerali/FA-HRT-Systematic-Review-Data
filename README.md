# FA-HRT systematic review data

This dataset supports *Fall-Aware Human–Robot Teaming: A Systematic Review of Simulation, Perception, Prediction, and Control* by Muhammad Toqeer Ali, Florenc Demrozi, and Filippo Sanfilippo.

It covers 102 publications (P001–P102): 11 simulation/modeling, 26 perception/detection-response, 9 prediction/anticipation, and 56 control/assistance/prevention/response. Publication IDs are stable identifiers and do not depend on the article's reference numbering.

## Files

| Location | Description |
|---|---|
| `01_Data_Extraction/FA_HRT_102_Data_Extraction.xlsx` | The 42-field extraction database for all 102 publications. |
| `02_Search_and_Screening/` | Search blocks, search-round totals, PRISMA selection summary and archived bibliographic database exports. |
| `03_Evidence_Audits/FA_HRT_102_Classification_and_Lineage_Formatted.xlsx` | Publication taxonomy, validation settings, primary-evidence IDs and verified research-family assignments, including a family summary. |
| `03_Evidence_Audits/FA_HRT_35_Learned_Detector_Validation_Formatted.xlsx` | Evaluation-method coding for 35 learned detectors. |
| `FA_HRT_102_C1-C5_Audit.xlsx` | Author-reconciled publication-level C1–C5 ratings for P001–P102, supporting observations and calculated summaries. |
| `03_Evidence_Audits/FA_HRT_Integration_Audit_Reconciled_Summary_Formatted.xlsx` | Aggregate audit counts consistent with the publication-level ratings. |
| `FA_HRT_MTA_Independent_Coding_15_Papers.xlsx` | MTA's original pre-consensus ratings; supporting explanations clarified after the original rating exercise. |
| `FA_HRT_FD_Independent_Coding_15_Papers.xlsx` | FD's independent pre-consensus ratings, retained unchanged. |
| `03_Evidence_Audits/FA_HRT_15_Publication_Inter_Rater_Agreement.xlsx` | Paired ratings for the 15-paper sample and unweighted Cohen's kappa calculations. |
| `DATA_DICTIONARY.md` | Field definitions and interpretation guidance. |
| `LICENSE` | Licence scope and third-party material exclusions. |

## C1–C5 integration audit

Ratings are based on explicitly supported study evidence. `Yes` counts as a satisfied criterion; `No` and `Partial` do not. `N/A` is used for C2 outside the five direct pre-impact prediction publications (P033, P035, P038, P072 and P083).

| Criterion | Publications rated Yes |
|---|---:|
| C1 — Phase-aware sensing | 21 |
| C2 — Reliable or calibrated pre-impact prediction | 0 |
| C3 — Bounded robot response | 71 |
| C4 — Physical-safety outcome | 24 |
| C5 — Human-centered or target-user evaluation | 14 |

The numbers of publications satisfying zero, one, two, three, four and five criteria are, respectively, **20, 43, 31, 7, 1 and 0**. P055 satisfies C1, C3, C4 and C5; C2 is not applicable to that study. No publication satisfies all five criteria. This is the reconciled audit result and supersedes counts in earlier manuscript drafts. The manuscript and response letter should cite this version when they are next updated.

## Agreement analysis

The inter-rater workbook preserves independent ratings from MTA and FD for 15 randomly sampled publications (seed 20261109), before consensus. Unweighted Cohen's kappa is 0.783 for primary branch, 0.448 for strongest validation, 0.898 for C1, 0.651 for C3, 0.844 for C4 and 0.468 for C5. C2 kappa is not estimable because only one sample publication was applicable. Original ratings are separate from final consensus decisions.

## Interpretation and coverage

Each P-code denotes a publication rather than an independent system or experiment. The checked classification identifies **77 broad research-family groups** and **79 high-confidence groups**. The `Family summary` worksheet lists the membership and basis for each related group. The broad grouping links P028 with P019/P022 (F04) and P080 with P085 (F16); these connections do not imply repeated experiments. The higher-confidence grouping retains only directly supported platform/programme connections. P006/P058 and P019/P022 repeat specific primary results, giving **100 distinct primary-result IDs** across 102 publications. Research-family counts are not counts of statistically independent experiments or deployed systems.

The search directories contain saved original and updated database exports. The PRISMA workbooks document aggregate selection counts but **do not contain individual title/abstract screening decisions, itemized reasons for the 19 full-text exclusions, or identifiers for the 12 unretrieved reports**. Those details must be documented separately if claimed as available. Complete executed platform-specific query histories are not included. Source-publication PDFs are not redistributed.

## Rights

The authors' original research materials are offered under CC BY 4.0 as set out in [`LICENSE`](LICENSE). Raw database exports and third-party source material are **not** relicensed by this notice; their public redistribution requires a separate rights check.
