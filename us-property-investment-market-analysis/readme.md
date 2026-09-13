# 2022 U.S. Housing Market Value Analysis
<img width="1920" height="1080" alt="Zillow and Realtor" src="https://github.com/user-attachments/assets/650ebb50-ac0b-494f-9ec0-318c0df44445" />

## Project Overview

This project combines 2022 housing data from Realtor.com with Zillow Home Value Index data to compare housing prices, market activity, and property characteristics across the United States.

The analysis was designed to answer the following business question:

> **Which U.S. housing markets appear most promising for further property-investment research?**

PostgreSQL was used to prepare, combine, and analyze the data. Tableau was used to build an interactive two-page dashboard for exploring results by region and state.

## Dashboard

[View the Interactive Tableau Dashboard](https://public.tableau.com/views/2022U_S_HousingMarketValue/MarketOverview?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

The workbook contains two dashboard pages:

### Market Overview

The Market Overview compares:

* Average home price
* Average Zillow Home Value
* Average price per square meter
* Average house size
* Average bedrooms and bathrooms
* Geographic housing activity
* Realtor.com prices against Zillow values by state

### Region Details

The Region Details page allows users to:

* Compare regions and individual states
* Identify states with the most recorded home sales
* Compare average price per square meter
* Explore geographic pricing patterns
* Review regional housing characteristics
* Filter all results by region and state

The Realtor.com housing data covers **April 1, 2022 through June 1, 2022**.

## Tools Used

* **PostgreSQL:** Data preparation, transformation, joining, and analysis
* **SQL:** `JOIN`, `CASE`, `GROUP BY`, aggregate functions, CTEs, `PARTITION BY`, and `ROW_NUMBER()`
* **Excel and Power Query:** Zillow data transformation and validation
* **Tableau:** Interactive dashboards, maps, filters, rankings, and KPI reporting

## Data Sources

### Realtor.com Housing Data

The Realtor.com dataset contains information such as:

* Listing status
* Home price
* Bedrooms
* Bathrooms
* Lot size
* City and state
* ZIP code
* House size
* Previous sale date

### Zillow Home Value Index

The Zillow dataset provides estimated typical home values across U.S. states. These estimates were used as an external benchmark for comparing Realtor.com housing prices.

Zillow Home Value should not be interpreted as the guaranteed appraisal or “true value” of an individual house.

## Data Preparation

### Realtor.com Data

I prepared the Realtor.com data by:

* Importing the original CSV columns as `VARCHAR` to simplify the initial PostgreSQL import
* Converting relevant columns into appropriate numeric and date data types
* Creating backup and staging tables
* Standardizing geographic fields
* Separating and analyzing housing records by status
* Aggregating housing metrics by state and region
* Checking missing, inconsistent, and unusually low values

### Zillow Data

The Zillow Home Value dataset originally stored states across multiple columns.

I used Power Query to:

* Unpivot the state columns
* Convert the data into a normalized structure
* Prepare the dataset for state-level comparison
* Join the Zillow values with the Realtor.com housing data

## SQL Analysis

PostgreSQL was used to:

* Join the Realtor.com and Zillow datasets
* Categorize states into U.S. regions with `CASE`
* Calculate average prices and property characteristics
* Aggregate home sales by state
* Compare Realtor.com prices with Zillow Home Values
* Rank geographic markets using window functions
* Use `PARTITION BY` and `ROW_NUMBER()` to perform rankings within geographic groups

## Analytical Indicators

I used the following indicators to screen housing markets:

### Housing Sales Activity

The number of recorded home sales was used to estimate relative market activity. A higher number of sales may indicate stronger demand and greater transaction activity.

### Realtor.com Price Compared with Zillow Value

Average Realtor.com prices were compared with Zillow Home Values to determine how closely observed prices aligned with Zillow’s estimated market benchmark.

A smaller difference may indicate closer price alignment, but it does not prove that properties are undervalued.

### Price per Square Meter

Price per square meter was used to compare relative housing costs across states while accounting for differences in property size.

### Property Characteristics

Average house size, bedrooms, and bathrooms provided additional context about the typical properties available within each market.

## Key Findings

### Georgia Appeared Promising for Further Research

Georgia combined meaningful housing activity with prices that were relatively close to Zillow’s estimated values.

Its property characteristics and proximity to other active Southeastern markets, including Florida and South Carolina, also made it a reasonable candidate for additional property-level investment research.

### Several Midwestern States Showed Potential

The Midwest contained several states where Realtor.com prices were comparatively close to Zillow Home Values.

Minnesota, Illinois, and Wisconsin stood out as markets worth investigating further based on their relative pricing and recorded housing activity.

### High-Cost Western and Northeastern Markets Require Caution

Several Western and Northeastern markets—including California, New York, and Connecticut—had comparatively high housing prices and price-per-area measurements.

These markets may require:

* More initial investment capital
* Greater appreciation to produce a return
* More careful property-level evaluation
* Greater consideration of financing and holding costs

This does not mean that profitable investments are impossible in these markets. It means that they may present higher barriers to entry.

## Recommendation

Based on the available data, **Georgia should be prioritized for additional property-level research**.

Selected Midwestern markets should also be considered because of their relative pricing and housing activity.

Before making an investment decision, the next stage of analysis should include:

* Purchase price
* Renovation costs
* Expected resale value
* Property taxes and insurance
* Financing and transaction costs
* Average time on market
* Neighborhood-level demand
* Comparable property sales

## Limitations

* The analysis does not include renovation costs.
* Financing, taxes, insurance, and transaction expenses are not included.
* The data does not calculate actual return on investment.
* State averages may hide major differences between cities and neighborhoods.
* Zillow Home Value is an estimated benchmark, not a guaranteed appraisal.
* Listing and sales coverage may not be equally complete across all states.
* The Realtor.com data represents a limited period in 2022.
* Historical housing conditions may not reflect the current market.

Therefore, this dashboard should be interpreted as a **market-screening analysis tool**, not a guarantee that purchasing and renovating a property will result in a profit.

## Skills Demonstrated

* Combining data from multiple sources
* Cleaning and transforming data with Excel, Power Query, and PostgreSQL
* Writing SQL with joins, CTEs, aggregations, `CASE`, `PARTITION BY`, and `ROW_NUMBER()`
* Evaluating and validating inconsistent data
* Creating state and regional comparisons
* Designing interactive Tableau dashboards
* Translating analysis into a business recommendation
* Communicating data limitations responsibly

## Conclusion

This project demonstrates how PostgreSQL and Tableau can be used to compare housing markets and identify areas that warrant additional investment research.

Georgia emerged as a strong initial candidate, while several Midwestern states also showed promising characteristics. A complete investment decision would require property-level acquisition, renovation, financing, and resale data.
