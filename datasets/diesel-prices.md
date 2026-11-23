# Is fuel pushing freight costs up again? US diesel prices

## Who decides what
The same transportation buyer decides when to lock in fall freight. Diesel is a major cost for towboats and for the trucks that bring grain to the river, so a fuel spike is a reason to lock in rates sooner.

## Data
- Publisher: US DOT Bureau of Transportation Statistics, Supply Chain and Freight Indicators. The diesel series comes from the U.S. Energy Information Administration (named in the dataset's source column). Course menu ID OP-2 (a second indicator from the same table as the barge rates).
- Link: https://data.bts.gov/d/y5ut-ibwt
- Indicator: U.S. Diesel Sales Prices (in Dollars per Gallon)
- Date accessed: 2026-11-23
- License: Public Domain U.S. Government

## What one row means
One week's US average retail diesel price in dollars per gallon, a weighted average from about 350 retail outlets, not seasonally adjusted.

## What was done
- Tool: Python and the publisher's data interface, run by Claude.
- Columns kept: date, value1.
- Filter: the diesel indicator only. 411 weekly rows, 2019-01-07 to 2026-11-16, none blank.
- Pivots:
  - [op2-diesel-monthly-average.csv](../analysis/op2-diesel-monthly-average.csv): average of the weekly prices in each month.
  - [op2-diesel-annual-average.csv](../analysis/op2-diesel-annual-average.csv): average of the monthly averages in each year.
- Check: the 411 weekly prices sum to $1,569.36 in the publisher query; the saved monthly pivot gives the same total to within rounding.

## What the numbers show
- The highest week in the series was $6.529 on 2026-09-21; the lowest was $2.372 on 2020-11-02.
- The September 2026 monthly average, $6.29, is above the 2022 peak month (June 2022, $5.75).
- October 2026 averaged $6.25, 70% above October 2025 ($3.68).
- Across the 95 months from 2019 to November 2026, the monthly diesel price and the monthly St. Louis barge rate have a correlation of 0.46: they tend to move together, but this does not show that diesel causes barge rates.

## What this data cannot show
This is a national retail pump price, not the marine fuel price towboat operators pay, and it says nothing about why prices rose. Correlation is not cause: river levels and harvest size also move barge rates.
