# FA-HRT systematic review data

This repository contains the extracted evidence and supporting tables for *Fall-Aware Human–Robot Teaming: A Systematic Review of Simulation, Perception, Prediction, and Control*.

The review includes 102 publications, identified as P001–P102. They are classified into simulation/modeling (11), perception/detection-response (26), prediction/anticipation (9), and control/assistance/prevention/response (56).

## Repository files

| Folder | File | Description |
|---|---|---|
| `01_Data_Extraction` | `FA_HRT_102_Papers_GitHub_Clean_Extraction.xlsx` | Extracted study details, methods, results, and limitations (102 publications). |
| `02_Search_and_Screening` | `Search_Rounds_Database_Counts_Formatted.xlsx` | Records retrieved from each database in the two search rounds. |
| `02_Search_and_Screening` | `Published_Combined_Search_Blocks_Formatted.xlsx` | Boolean search blocks reported in the paper. |
| `02_Search_and_Screening` | `PRISMA_Selection_Summary_Formatted.xlsx` | Reported screening and eligibility totals. |
| `03_Evidence_Audits` | `FA_HRT_102_Classification_and_Lineage_Formatted.xlsx` | Taxonomy assignments, overlapping categories, validation settings, and research-lineage links. |
| `03_Evidence_Audits` | `FA_HRT_35_Learned_Detector_Validation_Formatted.xlsx` | Participant independence, fall-event realism, and false-alarm reporting for 35 studies. |
| `03_Evidence_Audits` | `FA_HRT_Integration_Audit_Published_Summary_Formatted.xlsx` | Published aggregate results of the five-criterion integration audit. |

Field definitions are provided in [DATA_DICTIONARY.md](DATA_DICTIONARY.md).

## Notes on the data

A P-code identifies a publication, not an independent experiment. The pairs P006/P058 and P019/P022 report shared primary results. Under this distinction, the 102 publications represent 100 non-repeated primary results. Other research-family links indicate related work, not necessarily repeated experiments.

The search files give the published search blocks and selection totals. They do not contain the original platform-specific search strings, database exports, or individual screening decisions. Likewise, the integration-audit file reports aggregate counts, not publication-level C1–C5 decisions.

Unreported validation details should not be read as negative findings. Source publications are identified by title and DOI or source link where available; publisher PDFs are not distributed here.
