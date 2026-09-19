# Airbnb Data Analytics — Cleaning, Feature Engineering & EDA

## Project Overview

This project analyzes an Airbnb listings dataset using **Python, Pandas, NumPy, Matplotlib, and Seaborn**. The workflow focuses on data quality first, then feature engineering, followed by exploratory analysis of pricing, availability, reviews, host behaviour, and geographic patterns.

The raw dataset contains **10,019 listings and 17 original columns**. After cleaning and feature engineering, the analysis works with an expanded analytical dataset containing additional variables for pricing, review activity, host type, occupancy proxies, and revenue proxies.

## Analytical Workflow

```text
Raw listing data
      ↓
Data-quality audit
      ↓
Cleaning and type correction
      ↓
Feature engineering
      ↓
Validation
      ↓
Exploratory analysis
      ↓
Business interpretation
```

## Data Quality Work

The project investigates and handles:

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
- final data-type and consistency checks

An important decision in the project is to **preserve meaningful missingness**. For example, listings with zero reviews retain missing review-derived metrics rather than receiving arbitrary replacement values.

## Feature Engineering

The project creates analytical variables including:

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

> `occupancy_estimate` and `revenue_estimate` are analytical proxies derived from available fields. They should not be interpreted as verified Airbnb occupancy or realized revenue.

## Exploratory Questions

The analysis examines:

- How is listing price distributed?
- Which room types and boroughs dominate the dataset?
- How does price differ by borough and room type?
- How is availability distributed?
- How do reviews and ratings relate?
- Does review activity differ by room type?
- Which neighborhoods have higher median prices or stronger rating signals?
- How do single-listing and multi-property hosts differ?
- What geographic patterns appear across listings?
- How has listing activity changed over time?
- Which listings have never received reviews?

## Dataset

Key original fields include:

| Area | Variables |
|---|---|
| Listing | `listing_id`, `name`, `listing_added` |
| Host | `host_id`, `host_name` |
| Location | `neighbourhood_full`, `coordinates` |
| Accommodation | `room_type` |
| Pricing | `price` |
| Reviews | `number_of_reviews`, `last_review`, `reviews_per_month`, `rating`, `5_stars` |
| Availability | `availability_365` |
| Stay activity | `number_of_stays` |

## Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Git / GitHub

## Repository Structure

```text
Airbnb-data-analytics/
├── airbnb_data_analysis.ipynb
├── airbnb (1).csv
└── README.md
```

## What This Project Demonstrates

This project is primarily evidence of **data cleaning discipline, feature-engineering judgment, exploratory analysis, and careful interpretation of proxy variables** rather than just chart generation.
