# Offer and Uptake of Municipal Exercise Programmes Among People with Type 2 Diabetes – A Cross-Sectional, Register-Linked Study

**Study 3 of the PhD project** *Optimizing Self-Management in Type 2 Diabetes: The Role of High Intensity Interval Training in Enhancing Health Outcomes*

Authors: Jonas Munk Jensen, Søren T. Skou, Kasper Norman, Henrik Støvring, Anette Andersen

## Scope

The underlying protocol covers five types of municipal health services, so that more of them can be studied in future work. **This PhD study looks only at municipal physical activity/exercise programmes.** The other service items (referral, dietary support, DSMP, mental health support) are outside the scope of the PhD.

## Project Description

### Background

Exercise is a cornerstone of type 2 diabetes (T2D) care. In Denmark, the regions are responsible for diabetes self-management support, including exercise programmes, while the municipalities deliver most of it. No national register tracks the use of municipal health services. As a result, little is known about:

- how many people with T2D are offered and take up a municipal exercise programme
- whether these programmes reach those with the greatest need for support

Internationally, uptake of self-management support is low and socially patterned. Danish evidence comes mainly from a survey of Danish Diabetes Association members, who are likely more engaged and resourceful than the wider T2D population.

The study links to Studies 1 and 2 of the PhD. Those studies examine the effect of, and engagement in, exercise within a DSMP. This study asks who is reached by municipal exercise programmes in the first place.

### Objective

The study examines the offer and uptake of municipal exercise programmes among people with T2D, and whether these programmes reach those with the greatest need for support.

### Sub-questions

1. **Mapping.** What proportion of people with T2D are offered and take up a municipal exercise programme, and what proportion report an unmet need?
2. **Attrition analysis.** How representative are the study samples of the regional T2D population?
3. **Associated factors.** Which characteristics are associated with being offered, having an unmet need for, and taking up a municipal exercise programme?
4. **Illustrative patient profiles.** How does the predicted probability of being offered an exercise programme vary across hypothetical patient profiles?

### A priori hypothesis (sub-question 1)

- About 20% will report having been offered a municipal programme, and a similar proportion will report an unmet need. This is comparable to the Danish Diabetes Association survey (2023).
- Most respondents will report no perceived need.

### Design and Data Sources

This is a cross-sectional study. It links survey data from the **Health in Central Denmark (HICD)** cohort with nationwide register data from **Statistics Denmark**.

**Study population (flow)**

| Step | n |
|---|---|
| Individuals aged 18–75 with T2D in the Central Denmark Region (2024) | 52,020 |
| Responded to the HICD questionnaire (Feb 2024) | 20,516 |
| Consented to the supplementary questionnaire | 13,328 |
| Completed the items on municipal health services (autumn 2024) | 4,704 |

### Outcome Definitions

The study is based on one survey item:

> *"Within the past 5 years, have you been offered support for physical activity and/or exercise by the municipality?"*

The item has seven response options. They are combined into the following measures and outcomes:

| Response option | Measure (sub-q. 1) | Offer / Unmet need / Uptake (sub-q. 3) |
|---|---|---|
| Yes, and I accepted the offer | Offered; uptake | 1 / – / 1 |
| Yes, but I did not accept the offer | Offered | 1 / – / 0 |
| No, but I contacted the municipality myself | Self-initiated contact | 0 / – / – |
| No, but I would have liked the offer | Unmet need | 0 / 1 / – |
| No, I do not need it | No perceived need | 0 / 0 / – |
| Not relevant | No perceived need | 0 / 0 / – |
| Don't know | Excluded | Excluded |

There are three binary outcomes, each defined on its own population:

- **Offer**: among all respondents with a valid answer
- **Unmet need**: among those not offered
- **Uptake**: among those offered

"Uptake" means accepting the offer. It does not capture attendance or completion. Self-initiated contact does not tell us whether a programme was received.

### Covariates

Covariates were selected a priori and grouped into three conceptual domains. Age and sex are included in all models.

| Domain | Variables | Source |
|---|---|---|
| Socioeconomic resources | Country of origin, education, equivalized disposable household income, cohabitation/marital status | Register |
| Disease severity | Diabetes duration, HbA1c, comorbidity (NMI) | Register |
| | BMI, smoking, physical activity level, perceived disease burden | Self-report |
| Psychological resources | Personality traits, health literacy (HLQ), diabetes distress (PAID), well-being/QoL (WHO-5, SF-12) | Self-report |

### Statistical Analysis

**Response weighting**
- The probability of completing the supplementary questionnaire is estimated among the 13,328 who consented. The model is a logistic regression with register-based and self-reported predictors, using restricted cubic splines where relevant.
- Completers receive stabilized inverse probability weights. The weight distribution (mean, range) and the effective sample size are reported.
- All analyses are run both **unweighted** (observed sample) and **weighted** (response-weighted sample), with design-based (robust) variance estimation.

**Sub-question 1 – Mapping**
- Number and proportion (unweighted and weighted) in each response category.
- Proportions offered, self-initiated contact and unmet need, and uptake among those offered. Uptake in the weighted analysis is a domain estimate.
- Denominator: all valid answers. "Don't know" and missing answers are excluded, and "Not relevant" is retained.
- Results are stratified by sex, employment status and age group.
- Sensitivity analysis: excluding "Not relevant".

**Sub-question 2 – Attrition analysis**
- The observed and weighted samples are each compared with the full HICD T2D population (n = 52,020). The comparison uses register-based variables: age, sex, country of origin, education, income, cohabitation, diabetes duration, HbA1c, total cholesterol, NMI.
- Differences are measured with standardized mean differences (|SMD| > 0.1 is considered meaningful). No hypothesis tests are used.

**Sub-question 3 – Associated factors**
- Self-reported psychosocial scales are dichotomized using established cut-offs (e.g. WHO-5 ≤ 50, PAID ≥ 40) or otherwise the median in the observed sample.
- Other continuous covariates are modelled continuously, with splines where relevant.
- Baseline characteristics are summarized by outcome status (e.g. offered vs. not offered), with SMDs.
- Logistic regression is fitted for each outcome in three steps: crude, age- and sex-adjusted, and multivariable (all covariates).
- A multivariable model is fitted only if the smaller outcome category has ≥ 10 events per parameter (unweighted counts).
- For **uptake**, few decliners are expected. The age-/sex-adjusted associations are therefore the main analysis. They are supplemented by a reduced multivariable model with a pre-specified core set: age, sex, education, income, NMI, BMI, PAID, HLQ.
- Models for subpopulations (unmet need, uptake) are fitted as domain analyses in the weighted design.
- Sensitivity analyses:
  - exclude "Not relevant" from the offer and unmet need analyses
  - exclude self-initiated contact from the offer analysis
  - classify self-initiated contact as unmet need
- Results are reported as odds ratios with 95% CI.

**Sub-question 4 – Illustrative patient profiles**
- The 3–4 covariates with the most consistent associations in the multivariable offer model are selected.
- Five hypothetical profiles are constructed along a gradient from "most favorable" to "least favorable". All other covariates are held at the mean or the reference category.
- The predicted probability (95% CI) of being offered an exercise programme is calculated for each profile, with a short narrative description of each persona.

### Ethics and Registration

- Data are accessed via Statistics Denmark's research servers. Approval from the Danish Data Protection Agency is required.
- The analysis plan will be uploaded to the **Open Science Framework (OSF)** for timestamping before analyses begin.

### Timeline

The study will be performed in 2026–2027.

---

## Folder and File Structure

- `data/`
  Simulated datasets used to make sure the analysis scripts run as intended. Real data stays on Statistics Denmark's servers.

- `doc/`
  Protocol / analysis plan, notes, drafts and figures.

- `R/`
  R scripts for data processing, weighting and analysis.

---

## Data Management and Analysis

- All analyses are performed in **R/RStudio**.
- Microdata are stored and analysed on **Statistics Denmark's** research servers. Only aggregated output that meets the disclosure rules is exported.

---

## Resources

For more information on this project structure, see the [prodigenr documentation](https://rostools.github.io/prodigenr).
