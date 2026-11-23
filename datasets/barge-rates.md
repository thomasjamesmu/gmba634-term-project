# When should a grain exporter buy barge capacity?

## Who decides what
A grain exporter's transportation buyer decides how much fall barge capacity to contract ahead and how much to buy on the spot market at harvest.

## Data
- Publisher: US DOT Bureau of Transportation Statistics, Supply Chain and Freight Indicators (USDA Agricultural Marketing Service series)
- Link: https://data.bts.gov/d/y5ut-ibwt
- Indicator: Downbound Grain Barge Rates
- Date accessed: 2026-11-23
- License: Public Domain U.S. Government

## What one row means
One week's spot rate for downbound grain barge freight, in dollars per ton, at one of seven origins on the Mississippi River System: Twin Cities, Mid-Mississippi, Lower Illinois, St. Louis, Cincinnati, Lower Ohio and Cairo-Memphis.

## What was done
- Tool: Python scripts, run by Claude (see the AI disclosure in the README).
- Columns kept: date, measure1 (origin), value1 (dollars per ton).
- Filter: indicator is Downbound Grain Barge Rates; rows with no rate dropped (272 of 2,877), leaving 2,605 weeks from 2019-01-01 to 2026-11-10.
- Pivots:
  - [op2-barge-rates-by-month-2019-2025.csv](../analysis/op2-barge-rates-by-month-2019-2025.csv): rows origin, columns calendar month, values average rate, 2019 to 2025 only (full years).
  - [op2-barge-rates-by-origin-and-year.csv](../analysis/op2-barge-rates-by-origin-and-year.csv): rows origin and year, values average, minimum and maximum weekly rate.
  - [op2-st-louis-monthly-average.csv](../analysis/op2-st-louis-monthly-average.csv): St. Louis average rate for every month, Jan 2019 to Nov 2026.
  - [op2-st-louis-summer-vs-fall-by-year.csv](../analysis/op2-st-louis-summer-vs-fall-by-year.csv): St. Louis week-weighted average for May to July and for September to November, each year.
  - [op2-june-vs-october-by-origin.csv](../analysis/op2-june-vs-october-by-origin.csv): June and October averages for each origin, 2019 to 2025.
- Check: the row count (2,605) and the sum of all rates were computed on the downloaded data and again from the saved pivots; they agree to within rounding.

## What the numbers show
- St. Louis averaged $9.96 per ton in June and $31.11 in October (2019 to 2025), 3.1 times as much.
- October was the most expensive month at all seven origins.
- Fall cost more than summer at St. Louis in 7 of the 8 years from 2019 to 2026; 2019 was the exception.
- October 2022 averaged $89.33 at St. Louis; the worst week was $105.86.

## What this data cannot show
Contract or forward prices, any one firm's costs, or why rates move. Twin Cities and Mid-Mississippi have no winter rates because the upper river closes. In 2019 most summer weeks at St. Louis have no rate.
