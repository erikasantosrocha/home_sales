# Home Sales Challenge

Use SparkSQL to determine key metrics about home sales data. Spark is used to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Data Attributes
* `id`
* `date`
* `date_built`
* `price`
* `bedrooms`
* `bathrooms`
* `sqft_living`
* `sqft_lot`
* `floors`
* `waterfront`
* `view`

## Instructions

1. Import the necessary PySpark SQL functions.
2. Read the `home_sales_revised.csv` data into a Spark DataFrame.
3. Create a temporary table called `home_sales`.
4. Cache your temporary table home_sales.
5. Using the cached data, run the last query that calculates the average price of a home per `view` rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
6. Partition by the `date_built` field on the formatted parquet home sales data.
7. Create a temporary table for the parquet data.
8. Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
9. Uncache the home_sales temporary table.
10. Verify that the home_sales temporary table is uncached using PySpark.

## Report

The following questions were answered using SparkSQL:

* What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

* What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

* What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

* What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

## Summary

Although the the runtime difference were minor, the parquet runtime demonstrated a faster overall performance compared to both uncached and cached table data.
* The cached runtime of 0.880 seconds was faster than the uncached runtime of 1.102 seconds.
* The parquet runtime of 1.054 seconds was slighly faster than the cached runtime of 0.880 seconds.
