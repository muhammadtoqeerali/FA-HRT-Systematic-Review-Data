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

The 22 cross-cutting fields use `1` for coded membership and `0` for non-membership. Several categories may apply to a single publication. Validation settings describe the reported study context, not a quality score. Research-family links are provisional; only P006/P058 and P019/P022 were merged as repeated primary results.

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

**File:** `03_Evidence_Audits/FA_HRT_Integration_Audit_Published_Summary_Formatted.xlsx`  
**Coverage:** 22 aggregate summary rows; four columns (`Analysis`, `Category`, `Publications`, `Population`).

The five criteria are: C1, phase-aware sensing; C2, reliable or calibrated pre-impact prediction; C3, bounded robot response; C4, physical-safety outcome or proxy; and C5, human-centered or target-user evaluation. `Publications` gives the reported count; `Population` gives the relevant denominator (102 for corpus-wide results or 18 for the separate post-fall-care analysis). This workbook does not contain individual publication-level C1–C5 decisions.
