# Facebook Ads Performance Analysis

This repository contains a simple yet effective SQL project that focuses on analyzing basic daily data from Facebook Ads. The goal of this project was to extract and analyze key metrics that can provide insights into the performance of ad campaigns.

## Project Overview

This project was built as part of a SQL task aimed at extracting meaningful insights from a table named `facebook_ads_basic_daily`. The task involved writing a SQL query that selects specific columns, calculates a performance metric, and applies conditions to filter the data. The steps below outline the entire process.

### Task Requirements

1. **Connect to the Database**: Established a connection to the database using the provided credentials.
2. **Identify the Table**: Located the `facebook_ads_basic_daily` table and reviewed its structure, including column names and data types.
3. **Write SQL Query**:
   - Selected the following fields: `ad_date`, `spend`, `clicks`, and calculated the `spend/clicks` ratio as `spend_per_click`.
   - Applied a condition to ensure that only records with more than zero clicks are included in the result.
4. **Sort the Results**: Sorted the resulting dataset by `ad_date` in descending order to highlight the most recent data first.

### SQL Query

Here is the SQL query that was crafted to meet the requirements:

```sql
SELECT ad_date,
       spend,
       clicks,
       spend/clicks as spend_per_click
FROM public.facebook_ads_basic_daily
WHERE clicks > 0
ORDER BY ad_date DESC;
```

### Key Metrics

- **Ad Date (`ad_date`)**: The date on which the ad data was recorded.
- **Spend (`spend`)**: The amount of money spent on the ad for the given date.
- **Clicks (`clicks`)**: The number of clicks the ad received on the given date.
- **Spend Per Click (`spend_per_click`)**: A calculated metric representing the average cost per click, derived by dividing the spend by the number of clicks.

### Project Insights

The query effectively filters out any days where no clicks were recorded, ensuring that the `spend_per_click` metric is meaningful and relevant. By sorting the results in descending order by date, the analysis focuses on the most recent data, which is often the most critical for decision-making.

### How to Run the Query

1. Connect to your PostgreSQL database.
2. Copy and paste the SQL query provided above into your SQL editor or command line.
3. Execute the query to retrieve the results.
4. Analyze the output for insights into your Facebook Ads performance.

### Conclusion

This project demonstrates the power of SQL in transforming raw data into actionable insights. By focusing on key metrics and applying the appropriate filters, it’s possible to gain a deeper understanding of ad performance and make data-driven decisions.

Feel free to clone this repository, modify the query to suit your needs, and explore the data further. Contributions and feedback are welcome!

## Acknowledgements

Special thanks to [GoIT school] for providing the foundational knowledge and resources needed to complete this project.
