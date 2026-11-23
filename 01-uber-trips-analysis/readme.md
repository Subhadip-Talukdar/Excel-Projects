# Uber Trips Data Analysis (Excel)

An end-to-end exploratory data analysis (EDA) project using Microsoft Excel to clean, transform, and analyze 50,000 Uber trip records across six major US cities.

## Project Files
- **`RAW_uber_trips_dataset_50k.csv`**: Raw dataset containing 50,000 trip records and 14 baseline attributes (`trip_id`, `driver_id`, `rider_id`, `city`, pickup/drop coordinates, `distance_km`, `fare_amount`, `status`, `payment_method`, `pickup_time`, `drop_time`).
- **`Pivot_Uber Dataset.xlsx`**: Completed Excel workbook featuring engineered helper columns, conditional aggregations, KPI calculations, and multi-dimensional Pivot Tables.

## Key Transformations & Feature Engineering
Added 9 calculated columns to enrich the raw trip data for segmentation and KPI tracking:
- **`Trips` & `Rides`**: Categorized trips by distance and ride type (e.g., *Short Trip* vs. *Long Trip*, *Regular*).
- **`Fare_Category`**: Segmented fares into pricing tiers (*Low*, *Medium*, *High*).
- **`Promo Eligible` & `Digital_Payment`**: Boolean flags identifying promotional eligibility and non-cash transactions (`Wallet`, `UPI`, etc.).
- **`Trip_Results` & `Trips_Complete`**: Standardized completion statuses for filtering and counting successful rides.
- **`Trip duration in mins` & `Check Above 30`**: Calculated exact ride durations from timestamps and flagged trips exceeding 30 minutes.

## Analytical Highlights & KPIs
Using `COUNTIF`/`COUNTIFS`, `SUMIF`/`SUMIFS`, `AVERAGEIF`/`AVERAGEIFS`, and Pivot Tables across **San Francisco, Boston, New York, Seattle, Chicago, and Los Angeles** (Jan–Feb 2023):
- **Completed Trips**: 42,540 successful rides out of 50,000 total records.
- **Total Completed Revenue**: $679,684.88 (with an average completed fare of $15.98).
- **High-Value & Long-Duration Rides**: 12,267 trips had fares exceeding $20, and 27,118 trips lasted longer than 20 minutes.
- **City & Payment Breakdowns**: Built dedicated Pivot Tables (`Pivot Table 1`–`3`) to evaluate city-level distance/revenue performance (e.g., Seattle average distance of 7.07 km, San Francisco long-distance revenue of $33,307.56) and top-performing payment methods.

## Tools & Excel Functions Used
- **Data Transformation**: Logical formulas (`IF`, `AND`, `OR`), timestamp arithmetic.
- **KPI & Conditional Analysis**: `COUNTIFS`, `SUMIFS`, `AVERAGEIFS`.
- **Reporting**: Excel Pivot Tables for multi-dimensional slicing by city, trip status, and payment method.