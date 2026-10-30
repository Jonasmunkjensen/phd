# Diabetes Self-Management Programme (DSMP) With and Without HIIT – A Randomized Controlled Trial

**Study 1 of the PhD project** *Optimizing Self-Management in Type 2 Diabetes: The Role of High Intensity Interval Training in Enhancing Health Outcomes*

This is the main study of the PhD. It is a sub-study of the **LIVING trial**, a pragmatic RCT of three levels of the Lev Livet DSMP. The LIVING protocol is published as Jensen JM et al., *Contemporary Clinical Trials* 2025;153:107891 (doi:10.1016/j.cct.2025.107891). The trial is registered at ClinicalTrials.gov as NCT06091501.

## Project Description

### Background

In Denmark, municipalities deliver DSMPs for people with type 2 diabetes (T2D). The content varies, especially how much exercise is included. Exercise improves glycaemic control and health outcomes in T2D, but the effects often fade because of poor adherence. Time-efficient formats are therefore needed.

High-intensity interval training (HIIT) gives equal or greater benefits than endurance training for glycaemic control, fitness and body composition. HIIT has not yet been evaluated as part of a DSMP.

LIVING allows a direct comparison of two DSMPs that differ **only** in whether supervised HIIT is included.

### Objective

The study evaluates between-group changes in accelerometer-derived physical activity and in biometric outcomes associated with disease progression. Participants with T2D in a municipal DSMP with HIIT are compared with participants in the DSMP without HIIT and with a waiting-list control group.

### Hypothesis

Participants receiving **DSMP + HIIT** will show greater increases in daily physical activity and greater improvements in risk factors for disease progression than participants receiving DSMP alone and those on the waiting list.

### Interventions

- **LL (Full Lev Livet, FLL in the LIVING protocol)**: 9 sessions of 2.5–3 hours. The first 4 sessions cover coping skills across chronic diseases, and the next 4 are diabetes-specific. They run over about 8 weeks, followed by a follow-up session about 3 weeks later.
- **LLH (Lev Livet + HIIT, FLL + H)**: LL plus 16 one-hour supervised exercise sessions (2/week for 8 weeks), and one self-administered session per week.
  - Each supervised session has blocks of 5 × 1 min high intensity with 1 min active recovery, and 4 min between blocks.
  - It progresses from 2 blocks (22 min) to 4 blocks (48 min).
  - Upper- and lower-body exercises alternate.
  - Target intensity is Borg 14–16 (~77–93% of max heart rate).
  - Each session includes a 5-min warm-up and a 5-min cool-down, and injury-preventive balance and strength exercises.
- **Control group**: Waiting list for the length of the intervention period (until FU1).

The LIVING trial also includes a short version of Lev Livet (SLL). It is **not** part of this sub-study.

For detailed descriptions of the interventions, see [steno-aarhus.github.io/living-project](https://www.steno-aarhus.github.io/living-project).

### Trial Sites and Participants

The trial is conducted at municipal healthcare centres in:

- Aarhus
- Vejen
- Syddjurs
- Roskilde

Each site delivers **one** intervention (LL or LLH), chosen to fit its context and resources.

**Inclusion criteria**
- Diagnosed with T2D
- Age ≥ 18 years
- Able to speak and understand Danish
- Assessed fit by a healthcare professional to attend Lev Livet

**Exclusion criteria**
- Contraindications to increased physical activity as assessed by the participant's general practitioner (e.g. unstable angina, uncontrolled arrhythmias, severe aortic stenosis)

### Randomization and Blinding

Participants are randomized at the individual level (2:1) to intervention or control within each site. Randomization uses REDCap and a computer-generated block schedule (blocks of 12) prepared by an independent statistician. Blinding of participants and staff is not possible.

### Timepoints

| Timepoint | LL / LLH and controls |
|---|---|
| Baseline | 0 months |
| Endpoint | 3 months |
| FU1 | 5 months |
| FU2 | 11 months (self-reported data only) |

Objective measures (accelerometry, HbA1c, blood pressure, body composition, physical tests) are collected at baseline, endpoint and FU1.

### Outcomes

**Primary endpoint**
- Time per day in moderate-to-vigorous physical activity (MVPA), derived from accelerometer-classified activity types. The accelerometer is a thigh-worn Axivity AX3 (right thigh, 7 consecutive days, 24 h/day).

**Secondary endpoints**
- Other physical activity measures: light activity, sedentary time, steps/day, sleep
- Change in time per day spent in each activity type (e.g. sitting, standing, walking, cycling, running) from baseline to endpoint
- HbA1c (point-of-care, Cobas B 101)
- Blood pressure
- Body composition
- BMI
- 30-second sit-to-stand test
- Six-minute walk test

**Other data available from LIVING**
- Questionnaires: PCD-5 (the primary outcome in LIVING), SF-1, EQ-5D-5L, WHO-5, PAM-13, PAID-20, IPAQ, BREQ-2
- Demographics, medication, comorbidity, smoking, sleep, loneliness

### Adherence

Adherence is considered satisfactory with:
- ≥ 7 of 9 Lev Livet sessions (LL)
- ≥ 12 of 16 supervised exercise sessions (LLH)

### Power Calculation

The sub-study is powered to detect a minimum difference of 5.45 min/day MVPA between LL and LLH (n = 32 in each group). The assumptions are:
- SD = 7.75 min/day for change in MVPA (from IDES_2, n = 300)
- 80% power, α = 0.05
- ICC = 0.01 (clustering in training groups)
- 10% dropout

The clinically relevant threshold is 5 min/day. Previous studies report mean changes of ~9 min/day. Given the supervised HIIT dose (≥ 120 min/week), larger effects are expected.

### Statistical Analysis (planned)

- Analyses follow the intention-to-treat principle.
- The model is a linear mixed model with repeated measures, consistent with the LIVING analysis plan:
  - time (categorical), group and their interaction as fixed effects
  - a random effect for participant
  - random effects for training group/site where relevant
- **Primary analysis:** between-group difference in change in MVPA, with MVPA derived from activity types.
- **Activity types:** between-group differences in the change in time spent in each activity type from baseline to endpoint.
- **Sensitivity analysis:** MVPA is re-estimated with the method previously used at SDU, where MVPA is not derived from activity types. The results are compared with the primary analysis to check whether the two methods lead to similar conclusions.
- Missing data are handled with multiple imputation (`mice`).
  - For questionnaire outcomes, imputation is done at the item level, with all questionnaires in one joint imputation model.
  - Sum scores are computed within each imputed dataset, and results are pooled with Rubin's rules.

---

## Folder and File Structure

- `data/`
  Simulated datasets used to make sure the analysis scripts run as intended. The REDCap export stays on the secure server.

- `doc/`
  Notes, drafts, figures, and documentation related to the study (e.g. the Quarto report).

- `R/`
  R scripts for data processing and analysis.

---

## Data Management and Analysis

- Data are collected in **REDCap**.
- All analyses are performed in **R/RStudio** (Quarto for reporting).
- Secure data handling is done via **Midt-X**.

---

## Resources

For more information on this project structure, see the [prodigenr documentation](https://rostools.github.io/prodigenr).
