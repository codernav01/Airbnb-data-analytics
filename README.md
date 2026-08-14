# Airbnb Data Analytics

## Project Overview

This project presents an end-to-end analysis of an Airbnb listings dataset using **Python, Pandas, NumPy, Matplotlib, and Seaborn**. The analysis focuses on improving data quality, creating meaningful analytical features, and exploring pricing, availability, reviews, ratings, host behavior, and geographic patterns.

The project follows a structured workflow:

**Data Cleaning → Feature Engineering → Exploratory Data Analysis**

The objective is to transform raw Airbnb listing data into a reliable, analysis-ready dataset and extract meaningful insights from listing-level information.

---

## Project Objectives

- Identify and handle missing, inconsistent, and duplicate data.
- Standardize categorical, numerical, date, and geographic fields.
- Validate data quality before analysis.
- Create analytical features related to pricing, reviews, availability, hosts, and revenue.
- Explore relationships between price, availability, ratings, reviews, and listing characteristics.
- Identify geographic and host-level patterns.
- Generate data-driven insights through statistical analysis and visualizations.

---

## Dataset

The project uses an Airbnb listings dataset containing **10,019 listings and 17 original columns**.

### Key Data Fields

| Category | Variables |
|---|---|
| Listing | `listing_id`, `name`, `listing_added` |
| Host | `host_id`, `host_name` |
| Location | `neighbourhood_full`, `coordinates` |
| Accommodation | `room_type` |
| Pricing | `price` |
| Reviews | `number_of_reviews`, `last_review`, `reviews_per_month`, `rating`, `5_stars` |
| Availability | `availability_365` |
| Stay Activity | `number_of_stays` |

The dataset contains listing-level information related to **hosts, locations, pricing, reviews, ratings, availability, and estimated stay activity**.

---

## Coding & Analysis Workflow

### Part 1 — Data Cleaning & Data Quality

The raw dataset is prepared for analysis by:

- Checking missing values and their proportions.
- Investigating zero-review listings and review-related missing values.
- Handling missing and invalid prices.
- Converting price and date fields into appropriate data types.
- Extracting latitude and longitude from coordinate strings.
- Standardizing room-type categories.
- Separating borough and neighborhood information.
- Validating duplicate rows and repeated listing IDs.
- Detecting price outliers.
- Correcting numerical precision issues.
- Applying hierarchical median-based price imputation.
- Performing final data-quality validation.

### Part 2 — Data Wrangling & Feature Engineering

The cleaned dataset is enhanced with analytical features including:

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

These features enable deeper comparison of **listings, hosts, pricing, review activity, availability, and potential revenue**.

### Part 3 — Exploratory Data Analysis

The feature-engineered dataset is analyzed across multiple dimensions:

- Price distribution and skewness.
- Room-type and borough composition.
- Listing availability.
- Price differences across boroughs and room types.
- Relationship between reviews and ratings.
- Relationship between price and availability.
- Review activity by room type.
- Neighborhood-level price and five-star performance.
- Single-listing versus multi-property hosts.
- Geographic distribution of listings.
- Listing additions over time.
- Review recency versus availability.
- Never-reviewed listings.
- Review-data consistency and final analytical validation.

---

## Key Analytical Areas

The project examines how **location, accommodation type, pricing, availability, review activity, and host portfolio size** relate to Airbnb listing performance.

The analysis particularly focuses on:

- Pricing behavior and price concentration.
- Geographic differences in listing prices.
- Review engagement and listing activity.
- Availability patterns across host types.
- High-value and highly rated neighborhoods.
- Potential occupancy and revenue patterns.
- Listings with no review history.

---

## Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**
- **GitHub**

---

## Project Structure

```text
Airbnb-Data-Analytics/
│
├── Airbnb-data-analytics.ipynb
├── airbnb (1).csv
└── README.md
