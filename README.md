# Hospital Healthcare Analytics Dashboard

A Power BI dashboard built on a year of synthetic hospital operations data — admissions, LOS, revenue, doctor performance, and payer mix, all in one report.

## What's in here

- `healthcare_analytics_dataset.csv` — 5,000 patient case records across 12 months
- `Hospital_Healthcare_dasboard_report_final.pbix` — the Power BI report file

## Why I built this

I wanted a project that looked at a hospital the way an operations or finance team actually would — not just "how many patients came in" but things like how long they stayed, which doctors were driving revenue, how much of the billing was still pending, and whether cases were getting discharged before noon (which matters a lot for bed turnover). This dataset covers OP, IP, and DC cases across 10 specialties, so there's enough variety to build out a proper multi-page report instead of one flat table.

## Dataset overview

| | |
|---|---|
| Records | 5,000 |
| Time span | 12 months |
| Specialties | 10 (General Surgery, Orthopaedics, Emergency, Cardiology, Pulmonology, OB/GYN, Nephrology, Internal Medicine, Gastroenterology, Family Medicine) |
| Case types | OP, IP, DC |
| Admission types | Planned, Emergency, Referral |
| Avg. revenue/day | ~$4,037 |
| Avg. length of stay | ~1.27 days |

### Columns

| Column | What it means |
|---|---|
| Month | Admission month (date) |
| Case_No | Unique case ID |
| DOB | Birth year |
| Nationality | Patient nationality |
| Gender | M/F |
| DoctorLicense | Attending doctor's license ID |
| Doctor Type | Consultant / Specialist |
| Doctor Status | Active / Inactive |
| CMI Value | Case Mix Index |
| Specialty | Clinical specialty |
| Insurance/Payer | Payer name |
| InsurancePlanName | Specific plan tier |
| Payer Mix | Insurance / Self-Pay / Corporate |
| Case type | OP (outpatient), IP (inpatient), DC (day case) |
| LOS | Length of stay, in days |
| Severity | Severity score |
| Surgical Mix | Medical vs Surgery |
| Discharge Time | Time of discharge |
| Discharge Before 12PM | Flag for early discharges |
| Patient_Age | Age at admission |
| Revenue_per_day | Revenue generated per day of stay |
| High_Severity_Flag | Flags high-severity cases |
| Admission_Type | Planned / Emergency / Referral |
| Billing_Pending | Whether billing is still outstanding |
| Length_Category | LOS bucketed (Same Day / Short / etc.) |
| Revenue_Category | Revenue bucketed (Low / Medium / High) |
| Doctor_Experience_Yrs | Years of experience of attending doctor |
| Hospital_Department | Department |
| Insurance_Category | Insurance vs Self-Pay |

## Dashboard

The `.pbix` file has the report pages built on top of this data — patient volume trends, LOS and revenue breakdowns by specialty, doctor-level performance, and payer/insurance mix. Open it in Power BI Desktop to explore; no external connections needed since the data is embedded/loaded from the CSV.

## Getting started

1. Clone the repo
2. Open `Hospital_Healthcare_dasboard_report_final.pbix` in Power BI Desktop
3. If prompted to refresh data, point it at `healthcare_analytics_dataset.csv` in this repo

## Notes

- This is a synthetic/sample dataset built for analytics practice — it's not real patient data.
- Filenames kept as-is from the original build (yes, "dasboard" has a typo, I know 😅).

## Tech

- Power BI Desktop
- CSV / Excel-compatible source data
