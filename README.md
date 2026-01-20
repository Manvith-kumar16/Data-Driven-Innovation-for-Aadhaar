# Data-Driven Analysis of Aadhaar Enrolment, Updates, and Operational Risk

![Project Status](https://img.shields.io/badge/Project-UIDAI_Data_Hackathon_2026-blue)
![Python](https://img.shields.io/badge/Python-3.x-green)
![Data Analysis](https://img.shields.io/badge/Analysis-Operational_Risk-orange)

## Overview
Aadhaar is India’s foundational digital identity system, serving over a billion residents. As Aadhaar coverage matures across states, operational priorities increasingly shift from enrolment expansion to managing updates, biometric reliability, and region-specific service demand.

This project presents a data-driven analytical framework to examine Aadhaar enrolment maturity, demographic update burden, biometric stress patterns, and state-level operational risk using anonymised, aggregated public datasets. The objective is to transform raw administrative data into actionable, decision-ready insights that support efficient planning, monitoring, and resource allocation.

## Objectives
* **Identify Maturity:** Pinpoint states where Aadhaar enrolment has largely matured.
* **Quantify Burden:** Measure the demographic update burden relative to enrolment activity.
* **Analyze Stress:** Assess biometric update stress across age groups and regions.
* **Detect Patterns:** Identify operational anomalies and seasonal demand patterns.
* **Risk Prioritization:** Develop a composite risk framework to prioritise states for intervention.

## Datasets Used
All datasets were sourced from the **Open Government Data (OGD) Platform** and published by **UIDAI**. The data is anonymised and aggregated, ensuring privacy preservation.

| Dataset | Description | Key Attributes |
| :--- | :--- | :--- |
| **Aadhaar Enrolment** | New Aadhaar registrations | State, district, age groups, date |
| **Aadhaar Demographic Updates** | Address and demographic changes | State, age categories |
| **Aadhaar Biometric Updates** | Biometric re-captures | State, age categories |

## Project Structure
```text
├── 01_data_loading_and_cleaning.ipynb
├── 02_core_analysis.ipynb
├── datasets/
│   ├── api_data_aadhar_enrolment/
│   ├── api_data_aadhar_demographic/
│   └── api_data_aadhar_biometric/
└── README.md

```

## Methodology

### Data Preparation

* Standardised state and region names.
* Aligned date formats for time-series consistency.
* Validated missing and inconsistent records.

### Analytical Design

* **Enrolment Saturation:** Inferred using age composition patterns as a proxy for maturity.
* **Update Burden:** Quantified through update-to-enrolment ratios.
* **Biometric Stress:** Assessed using age-wise biometric update volumes.
* **Normalization:** Metrics normalised to enable fair comparison across states of different sizes.

## Key Analyses Performed

1. **Enrolment Saturation Analysis:** Identifies states where new enrolment activity is limited.
2. **Update Burden Analysis:** Highlights operational workload beyond onboarding.
3. **Biometric Stress Analysis:** Identifies stress drivers related to biometric degradation.
4. **Seasonal Demand Patterns:** Evaluates monthly trends to identify peak service periods.
5. **Composite Operational Risk Framework:** Integrates all metrics into a single interpretable risk score per state.

## Key Insights

* **Saturation:** Aadhaar enrolment activity is approaching saturation in several states, indicating mature coverage.
* **Workload Shift:** Demographic updates consistently exceed new enrolments, creating sustained operational workload.
* **Biometric Drivers:** Biometric updates among the adult (17+) population are the primary source of biometric stress.
* **Risk Convergence:** Composite analysis highlights states where multiple operational pressures converge.

## Operational Use of the Framework

The composite decision framework serves as a monitoring tool to classify states into risk categories:

| Risk Category | Indicative Action |
| --- | --- |
| **High Risk** | Extra biometric stations, staff redeployment |
| **Medium Risk** | Targeted optimisation and monitoring |
| **Low Risk** | Routine operations |

## Impact

* Enables proactive reduction of service congestion and delays.
* Improves utilisation of enrolment and biometric infrastructure.
* Supports data-driven resource allocation and policy planning.
* Potential for significant system-wide efficiency gains (even a 5–10% reduction in repeat updates).

## Tools & Technologies

* **Python** (Pandas, NumPy, Matplotlib)
* **Jupyter Notebook**

---

**Note:** This project was developed as part of the UIDAI Data Hackathon 2026.
