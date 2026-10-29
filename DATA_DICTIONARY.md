# Data dictionary

The workbooks contain one record per publication or reported summary item. Blank cells indicate that the information was not recorded in the source extraction; they do not necessarily mean zero or “no.” Publication identifiers P001–P102 are consistent across the study-level files.

## Publication extraction

`01_Data_Extraction/FA_HRT_102_Papers_GitHub_Clean_Extraction.xlsx` — 102 rows, 42 fields.

| Column | Description |
|---|---|
| Record ID | Publication identifier (P001–P102). |
| Title | Publication title. |
| Authors | Listed authors. |
| Year | Publication year. |
| Venue | Journal or conference. |
| Research Objective or Purpose | Study aim. |
| Application or Clinical Context | Intended use. |
| Robot Device or System | Robot or assistive device. |
| System or Platform Description | Main platform characteristics. |
| Study Design or Approach | Study design or method. |
| Experimental Setting | Test environment. |
| Target Population | Intended users. |
| Participant Count | Number of participants, where reported. |
| Participant Details | Participant characteristics. |
| Age Details | Ages or age range. |
| Sex or Gender Details | Reported sex or gender characteristics. |
| Ethics and Consent | Ethics approval or consent information. |
| Tasks or Activities | Activities studied. |
| Fall Instability or Risk Scenarios | Fall or balance-related scenarios. |
| Experimental Conditions or Trials | Test conditions and trials. |
| Sensors or Inputs | Input measurements or signals. |
| Data Source or Dataset | Dataset or data source. |
| Dataset or Sample Size | Size of dataset or set of observations. |
| Sampling Rate or Frequency | Data sampling frequency. |
| Features or Representations | Features used in analysis. |
| Algorithms Models or Analyses | Models, algorithms, or analytical methods. |
| Control or Decision Strategy | Robot decision or control logic. |
| Robot or System Output | System output or robot action. |
| Hardware and Software | Implementation details. |
| Training Validation Test Protocol | Model training and evaluation procedure. |
| Comparator or Baseline | Comparison method or condition. |
| Outcome Measures | Outcomes assessed. |
| Metrics Reported | Performance measures. |
| Statistical Analysis | Statistical tests or analyses. |
| Latency or Real Time Performance | Reported processing or response times. |
| Main Quantitative Results | Main numerical results. |
| Main Qualitative Findings | Main nonnumerical findings. |
| Safety Related Outcomes | Safety measures, including simulated proxies. |
| Human Centered or User Reported Outcomes | Participant or caregiver-reported outcomes. |
| Failure Cases or Adverse Events | Failures or adverse observations. |
| Author Reported Limitations | Limitations identified by the authors. |
| Data or Code Availability | Availability reported in the source publication. |

## Classification and research lineage

`03_Evidence_Audits/FA_HRT_102_Classification_and_Lineage_Formatted.xlsx` — 102 rows, 34 fields.

| Fields | Meaning |
|---|---|
| P-code; Paper title; Citation key; Source DOI / URL | Publication identification and source link. |
| Primary branch; Level-2 subtype | One primary classification and subtype per paper. |
| Strongest validation | Highest reported evaluation setting used in the review. |
| Research family (broad); Research family (high confidence) | Related research-program groupings, with different evidence thresholds. |
| Primary evidence ID; Shared primary result with; Lineage evidence note | Links between repeated results and the basis for those links. |
| Model / digital human; Walker/cane; Rehab/exoskeleton; Care/service; Smart-home; Balance/mobile | System or embodiment categories. |
| Model/simulation/digital twin; Vision/depth/RF; Wearable/IMU; Force/contact/robot state; Multimodal/context | Evidence inputs. |
| Elevated risk; Active instability; Near-onset; Direct pre-impact; Post-fall; Multistage | Fall timing or operational state. |
| Model/state estimate; Monitor/verify; Predict/plan; Reactive/care response; Physical support/prevention | Robot function or action. |

The 22 cross-cutting category fields use **1** for a coded membership and **0** when membership was not coded. Categories can overlap. `Strongest validation` is assigned once per publication and is not a quality score.

Related research families do not necessarily use the same dataset or experiment. Only P006/P058 and P019/P022 share identified primary results.

## Learned-detector validation

`03_Evidence_Audits/FA_HRT_35_Learned_Detector_Validation_Formatted.xlsx` — 35 rows, 13 fields.

| Fields | Meaning |
|---|---|
| P-code; Paper title; Primary branch; Evaluated task | Study and task under review. |
| Participant independence; Participant split evidence | Whether evaluation on unseen participants is established, and supporting details. |
| Fall-event realism; Event evidence | Nature of the fall or instability events tested. |
| False-alarm reporting; False-alarm evidence | Reported false alarms and their denominators. |
| Monitoring hours verified | Whether active monitoring time was available for an alarm-rate calculation. |
| Original publication URL | Source link. |
| Interpretation and limitations | Limits on what the reported validation supports. |

“Not reported” and “not established” refer to the available publication evidence, not proof that testing was not carried out.

## Search and screening

| File | Contents |
|---|---|
| `Search_Rounds_Database_Counts_Formatted.xlsx` | Search date, round, database, searched field, and number of records retrieved. “Supplementary” in the search-round column means the expanded search of 26 October 2026. |
| `Published_Combined_Search_Blocks_Formatted.xlsx` | Three Boolean concept blocks used to describe the combined search strategy in the manuscript. These are not the exact database-specific historical queries. |
| `PRISMA_Selection_Summary_Formatted.xlsx` | Selection stages and reported counts for the original and combined searches. These are summary figures, not record-level screening decisions. |

## Integration audit

`03_Evidence_Audits/FA_HRT_Integration_Audit_Published_Summary_Formatted.xlsx` — 22 summary rows, four fields: `Analysis`, `Category`, `Publications`, and `Population`.

C1 = phase-aware sensing; C2 = reliable or calibrated pre-impact prediction; C3 = bounded robot response; C4 = physical-safety outcome or proxy; C5 = human-centered or target-user evaluation.

`Publications` gives the reported count. `Population` gives the denominator (102 for the full corpus or 18 for the separate post-fall-care analysis). The combination rows are selected reported patterns, not a full study-by-study audit.
