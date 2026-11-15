# Data dictionary

The workbooks retain the publication identifiers P001–P102 used in the review. Each worksheet has a header row. Blank cells indicate information not recorded in the extraction, not necessarily a zero or a negative finding.

## 1. Publication extraction

**File:** `01_Data_Extraction/FA_HRT_102_Data_Extraction.xlsx`  
**Coverage:** 102 publications; 42 fields.

| Column | Description |
|---|---|
| Record ID | Stable publication identifier (P001–P102). |
| Title | Publication title. |
| Authors | Authors recorded in the extraction. |
| Year | Publication year. |
| Venue | Publication venue. |
| Research Objective or Purpose | Main study aim. |
| Application or Clinical Context | Intended setting or application. |
| Robot Device or System | Robot or assistive device considered. |
| System or Platform Description | Main platform features. |
| Study Design or Approach | Research method or study design. |
| Experimental Setting | Evaluation environment. |
| Target Population | Intended user population. |
| Participant Count | Number of participants, where reported. |
| Participant Details | Reported participant characteristics. |
| Age Details | Reported age information. |
| Sex or Gender Details | Reported sex or gender information. |
| Ethics and Consent | Ethics or consent information. |
| Tasks or Activities | Activities examined. |
| Fall Instability or Risk Scenarios | Fall- or balance-related conditions. |
| Experimental Conditions or Trials | Tested conditions and trial details. |
| Sensors or Inputs | Recorded or simulated inputs. |
| Data Source or Dataset | Data source used by the study. |
| Dataset or Sample Size | Reported dataset or sample size. |
| Sampling Rate or Frequency | Sampling frequency, if reported. |
| Features or Representations | Features used for analysis. |
| Algorithms Models or Analyses | Models and analytical methods. |
| Control or Decision Strategy | Robot control or decision logic. |
| Robot or System Output | Robot action or system output. |
| Hardware and Software | Main implementation components. |
| Training Validation Test Protocol | Model training and testing procedure. |
| Comparator or Baseline | Comparison method or condition. |
| Outcome Measures | Outcomes evaluated. |
| Metrics Reported | Reported performance measures. |
| Statistical Analysis | Reported statistical tests. |
| Latency or Real Time Performance | Processing or response timings. |
| Main Quantitative Results | Main numerical findings. |
| Main Qualitative Findings | Main descriptive findings. |
| Safety Related Outcomes | Physical-safety measures, including modeled proxies. |
| Human Centered or User Reported Outcomes | User- or caregiver-related outcomes. |
| Failure Cases or Adverse Events | Reported failures or adverse events. |
| Author Reported Limitations | Limitations identified in the study. |
| Data or Code Availability | Availability reported by the publication. |

## 2. Classification and research lineage

**File:** `03_Evidence_Audits/FA_HRT_102_Classification_and_Lineage_Formatted.xlsx`  
**Coverage:** 102 publications; 34 fields.

| Field group | Contents |
|---|---|
| Publication | P-code, title, citation key, DOI or source URL. |
| Primary taxonomy | Primary branch and Level-2 subtype (one of each per publication). |
| Validation | Strongest reported validation setting (one per publication). |
| Research lineage | Broad and high-confidence family IDs, primary evidence ID, repeated-result link, and supporting note. |
| System/embodiment | Model/digital human; walker/cane; rehabilitation/exoskeleton; care/service; smart-home; balance/mobile. |
| Evidence source | Model/simulation/digital twin; vision/depth/RF; wearable/IMU; force/contact/robot state; multimodal/context. |
| Fall timing | Elevated risk; active instability; near-onset; direct pre-impact; post-fall; multistage. |
| Robot function | Model/state estimate; monitor/verify; predict/plan; reactive/care response; physical support/prevention. |

The 22 cross-cutting fields use `1` for coded membership and `0` for non-membership. Several categories may apply to a single publication. Validation settings describe the reported study context, not a quality score. The `Family summary` worksheet documents the evidence-checked groupings, members and counting rules: **77 broad groups, 79 high-confidence groups and 100 distinct primary-result IDs**. Broad groups allow a documented research-programme connection; high-confidence links require a clearer shared platform or directly traceable research continuation. P028 is a broad F04 link but not part of the repeated P019/P022 classifier result. P080/P085 form broad group F16 while retaining separate high-confidence IDs. Only P006/P058 and P019/P022 share primary-result identifiers. Related studies are not automatically identical experiments.

## 3. Learned-detector validation audit

**File:** `03_Evidence_Audits/FA_HRT_35_Learned_Detector_Validation_Formatted.xlsx`  
**Coverage:** 35 publications; 13 fields.

| Field group | Contents |
|---|---|
| Publication and task | P-code, paper title, primary branch, evaluated task. |
| Participant independence | Coding and evidence for whether testing used participants unseen during training. |
| Fall-event realism | Nature of the evaluated fall or instability events and supporting evidence. |
| False alarms | Reporting type, denominator, and evidence for alarm-related findings. |
| Monitoring hours | Whether continuous active monitoring time was verified. |
| Source and limitations | Publication link and interpretation limits. |

“Not reported” or “not established” indicates insufficient reporting, not proof that the test was absent.

## 4. Search and screening

**Folder:** `02_Search_and_Screening/`

| File or folder | Contents |
|---|---|
| `Search_Rounds_Database_Counts_Formatted.xlsx` | Database, date, search round, search field, and retrieved-record counts. The term “Supplementary” in the workbook means the updated search of 26 October 2026. |
| `Published_Combined_Search_Blocks_Formatted.xlsx` | Three Boolean concept blocks reported in the article; not verbatim platform-specific search histories. |
| `PRISMA_Selection_Summary_Formatted.xlsx` | Aggregate identification, screening, retrieval, eligibility, and inclusion counts. |
| `old_query_outcomes/` | Saved database-result exports associated with the original search. |
| `new_query_outcomes/` | Saved database-result exports associated with the updated search. |

The export folders contain bibliographic search results in formats including BibTeX, RIS, and text. They are not a record of individual inclusion/exclusion decisions. Where platform-specific filters or exact executed query syntax were not retained, they cannot be inferred from these exports.

## 5. Integration audit

**Publication-level file:** `FA_HRT_102_C1-C5_Audit.xlsx`  
**Summary file:** `03_Evidence_Audits/FA_HRT_Integration_Audit_Reconciled_Summary_Formatted.xlsx`  
**Coverage:** 102 publications; five ratings and a brief supporting observation for each publication–criterion pair.

| Criterion | Rule for a positive (`Yes`) decision |
|---|---|
| C1 — Phase-aware sensing | Action-relevant discrimination between fall/instability states; an already-fallen classification by itself is insufficient. |
| C2 — Reliable/calibrated pre-impact prediction | Direct pre-impact prediction with adequate reliability, uncertainty calibration or risk-sensitive validation. Only the five direct predictor studies are applicable. |
| C3 — Bounded robot response | An evaluated robot/device action or care response, or an explicitly modeled action envelope. |
| C4 — Physical-safety outcome | A measured downstream physical consequence or a justified modeled proxy (e.g., recovery, stability, force or impact). |
| C5 — Human-centered evaluation | Reported intended-user/caregiver experience or functional outcome; participation in a technical experiment alone does not suffice. |

`Yes` counts as met. `No` means the required evidence is not established; `Partial` means relevant but incomplete support. Neither counts as met. `N/A` is used for C2 in the 97 publications without direct pre-impact prediction claims. The audit's `Criteria met` and `Combination` fields count only `Yes` ratings; combinations describe exact positive-criterion sets.

The current Yes counts are **21 (C1), 0 (C2), 71 (C3), 24 (C4) and 14 (C5)**. The satisfied-criterion distribution for 0–5 criteria is **20, 43, 31, 7, 1, 0**. P055 is the sole publication satisfying C1+C3+C4+C5. The separate 18-publication post-fall operational-link summary is carried forward as a distinct analysis and is not calculated from the C1–C5 columns.

## 6. Independent coding and agreement

**Pre-consensus rating files:**
- `FA_HRT_MTA_Independent_Coding_15_Papers.xlsx`
- `FA_HRT_FD_Independent_Coding_15_Papers.xlsx`

**Agreement calculations:** `03_Evidence_Audits/FA_HRT_15_Publication_Inter_Rater_Agreement.xlsx`

The MTA and FD files hold original independent ratings for the 15 sampled P-codes (seed 20261109). The MTA evidence explanations were clarified after the rating exercise; the rating categories used for kappa were not changed. The separate agreement file presents the paired categories, observed and chance-expected agreement and unweighted Cohen's kappa. It excludes nonapplicable C2 ratings and does not calculate kappa for C2 when only one publication remains. Consensus ratings may differ from either pre-consensus set.

## 7. Scope of the archived source records

The PRISMA workbook contains aggregate counts rather than individual screening decisions or individual reasons for the 19 full-text exclusions and 12 unretrieved reports. The saved database exports are bibliographic records, not screen-by-screen Rayyan decisions. Research-family identifiers describe verified programme or platform connections, not proof that studies share participants, experimental results or statistically independent systems. Authors' annotations are licensed as stated in `LICENSE`; original third-party database records and source-publication text may have separate redistribution restrictions.
