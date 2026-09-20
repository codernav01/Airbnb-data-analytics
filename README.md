# Airbnb Data Analytics — Cleaning, Feature Engineering & EDA

> **Python portfolio case study:** data-quality decisions, feature engineering, exploratory analysis, and careful interpretation of analytical proxies.

## Recruiter Snapshot

| Area | Evidence |
|---|---|
| Dataset | **10,019 listings**, 17 original columns |
| Core work | cleaning, validation, feature engineering, EDA |
| Python | Pandas, NumPy, Matplotlib, Seaborn |
| Analytical focus | pricing, availability, reviews, hosts, geography |
| Judgment | preserves meaningful missingness and labels proxy metrics clearly |

## Project Overview

The project starts with raw listing data, audits quality issues, cleans and standardizes fields, engineers analysis-ready features, validates the result, and then explores business-relevant patterns.

```text
Raw listings
   ↓
Quality audit
   ↓
Cleaning & type correction
   ↓
Feature engineering
   ↓
Validation
   ↓
EDA
   ↓
Business interpretation
```

## Data Quality Decisions

The notebook investigates:

- missing values across review, price, and identity fields
- zero-review listings and structurally missing review metrics
- price parsing and invalid values
- duplicate rows and repeated listing IDs
- date conversion
- latitude / longitude extraction
- room-type standardization
- borough / neighborhood extraction
- price outlier detection
- hierarchical median-based price imputation
- final type and consistency checks

A key decision is to **preserve meaningful missingness**. Listings with zero reviews keep review-derived fields missing rather than receiving arbitrary replacement values.

## Feature Engineering

Created analytical variables include:

- `borough`
- `neighborhood`
- `days_since_last_review`
- `price_per_review`
- `price_per_stay`
- `has_reviews`
- `five_star_percentage`
- `five_star_category`
- `price_category`
- `occupancy_estimate`
- `host_listing_count`
- `host_type`
- `revenue_estimate`

> `occupancy_estimate` and `revenue_estimate` are analytical proxies derived from available fields. They are not verified Airbnb occupancy or realized revenue.

## Analytical Questions

The analysis examines:

- price distribution and outliers
- room-type and borough mix
- price differences by borough and room type
- availability patterns
- relationships between reviews and ratings
- review activity by room type
- neighborhood pricing and rating signals
- single-listing vs multi-property hosts
- geographic patterns
- listing activity over time
- never-reviewed listings

## Dataset Note

The repository includes the CSV used for the analysis. The original public source and licence are not documented in the repository, so the project does not infer a publisher without evidence.

## Repository Structure

```text
Airbnb-data-analytics/
├── README.md
├── requirements.txt
├── airbnb_data_analysis.ipynb
└── airbnb (1).csv
```

## How to Review

**Recruiter:** read this README and the notebook markdown/outputs.  
**Technical reviewer:** inspect the cleaning, validation, and feature-engineering sections before the EDA.  
**Run locally:** install packages from `requirements.txt`, open the notebook, and run it with the dataset in its current path.

## What This Project Demonstrates

**Data cleaning discipline + feature-engineering judgment + exploratory analysis + careful interpretation of proxy variables.**
