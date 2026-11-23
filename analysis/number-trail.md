# Number trail

Every number on the site, the README and the executive case has one line here. Years and dates need no line. Claude built these pivot files with scripts; the last column says where each number sits.

| Number | What it is | How it was computed | Where it is |
|---|---|---|---|
| $9.96 | St. Louis average rate in June, 2019 to 2025 | Mean of all June weekly rates, 2019 to 2025 | op2-barge-rates-by-month-2019-2025.csv, row St. Louis, month 06 |
| $31.11 | St. Louis average rate in October, 2019 to 2025 | Mean of all October weekly rates | same file, row St. Louis, month 10 |
| 3.1 times | October divided by June at St. Louis | 31.11 / 9.96 = 3.12 | op2-june-vs-october-by-origin.csv, row St. Louis |
| $25.79 | St. Louis September to November average (reversal price) | Mean of 24.87, 31.11 and 21.40 | op2-barge-rates-by-month-2019-2025.csv, St. Louis months 09 to 11 |
| 7 of 7 origins | Origins where October is the most expensive month | Highest month per origin | op2-barge-rates-by-month-2019-2025.csv |
| 3.1 times, 1.7 times | October to June ratio at Cairo-Memphis (3.13) and Twin Cities (1.67) | October average / June average | op2-june-vs-october-by-origin.csv |
| 7 of 8 years | Years where the fall average beat the summer average | fall_to_summer_ratio above 1 | op2-st-louis-summer-vs-fall-by-year.csv |
| $13.97, $12.42 | 2019 summer and fall averages (the exception) | Week-weighted average | same file, row 2019 |
| $14.10, $55.74 | 2022 summer and fall averages | Week-weighted average | same file, row 2022 |
| $89.33 | St. Louis October 2022 monthly average | Mean of the October 2022 weekly rates | op2-st-louis-monthly-average.csv, row 2022-10 |
| $105.86 | Worst St. Louis week in 2022 | Maximum weekly rate in 2022 | op2-barge-rates-by-origin-and-year.csv, row St. Louis 2022, column max |
| 2,605 and 272 | Weeks with a rate, and blank rows, out of 2,877 | Row counts | data/SOURCES.md |
| 73.5 million tons, 53.6% | South Louisiana corn plus soybean tons in 2023, and its share of the listed total | Sum of Corn and Soybeans rows; divided by the year total | op3-corn-soy-tons-by-port-2023.csv, row South Louisiana; op3-corn-soy-share-by-year.csv, row 2023 |
| 75.8% and 69.0% | Share of the four lower-Mississippi ports in 2023 and 2020 | Sum of the 4 ports / year total | op3-corn-soy-share-by-year.csv, rows 2023 and 2020 |
| 7.2 million tons, 5.2% | Kalama, WA, the largest non-Gulf port in 2023 | Same method | op3-corn-soy-tons-by-port-2023.csv, row Kalama |
| 27 and 21 ports | Ports listing corn or soybeans in 2020 and 2023 | Count of distinct ports | op3-corn-soy-share-by-year.csv |
| 157 rows, 690,228,606 tons | Rows kept and their total | Row count and sum | datasets/grain-ports.md |
| $6.529 | Highest weekly diesel price (2026-09-21) | Maximum weekly value | datasets/diesel-prices.md (publisher query) |
| $2.372 | Lowest weekly diesel price (2020-11-02) | Minimum weekly value | same |
| $6.29 | September 2026 monthly diesel average | Mean of the weekly prices in the month | op2-diesel-monthly-average.csv, row 2026-09 |
| $5.75 | June 2022 monthly average, the 2022 peak month | Same | same file, row 2022-06 |
| $6.25, $3.68, 70% | October 2026 and October 2025 averages, and the change | 6.252 / 3.678 minus 1 | same file, rows 2026-10 and 2025-10 |
| 0.46 | Correlation of monthly diesel and monthly St. Louis barge rate, 95 months | Pearson correlation | op2-diesel-monthly-average.csv and op2-st-louis-monthly-average.csv |
