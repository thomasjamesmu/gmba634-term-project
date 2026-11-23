# Where does barge grain end up? Four ports on the lower Mississippi

## Who decides what
The same grain exporter's transportation buyer decides which export elevators to contract barge deliveries to, and how much rides on one river corridor.

## Data
- Publisher: US DOT Bureau of Transportation Statistics, Port Data (National Transportation Atlas Database). Course menu ID OP-3.
- Link: https://data.bts.gov/d/5rpz-kgm9
- Date accessed: 2026-11-23
- License: Public Domain (BTS portal metadata)

## What one row means
One port, one reporting year and one cargo measure. For this page I used the rows where cargo_type is "TOP 5 FOOD/FARM COMMODITIES" and the commodity (trade_type) is Corn or Soybeans. The volume is short tons handled at the port in that year.

## What was done
- Tool: Python and the publisher's data interface, run by Claude (see the AI disclosure in the README).
- Columns kept: port_name, region, reporting_year, trade_type, volume.
- Filter: cargo_type = TOP 5 FOOD/FARM COMMODITIES; trade_type in (Corn, Soybeans). This leaves 157 rows for 2020 to 2023 (the only years these rows exist).
- Pivots:
  - [op3-corn-soy-tons-by-port-2023.csv](../analysis/op3-corn-soy-tons-by-port-2023.csv): top 10 ports by corn plus soybean tons in 2023, with each port's share of the listed total.
  - [op3-corn-soy-share-by-year.csv](../analysis/op3-corn-soy-share-by-year.csv): for each year, the listed total, South Louisiana's share and the share of four lower-Mississippi ports (South Louisiana, New Orleans, Plaquemines and Greater Baton Rouge).
- Check: the 157 rows sum to 690,228,606 short tons both in the publisher query and in the saved copy.

## What the numbers show
- In 2023, the Port of South Louisiana handled 73.5 million short tons of corn and soybeans, 53.6% of all corn and soybean tons listed.
- The four lower-Mississippi ports together handled 75.8% in 2023, up from 69.0% in 2020.
- The largest non-Gulf port was Kalama, Washington, with 7.2 million tons (5.2%).

## Why it matters for the barge decision
Almost all of that grain reaches these ports by barge down the river, so the barge rates on the [barge rates page](barge-rates.md) are the price of reaching the ports that handle three quarters of the listed corn and soybeans.

## What this data cannot show
These are tons handled at the port, inbound and outbound, foreign and domestic, not exports alone. A port only lists corn or soybeans when they are in its top 5 food and farm commodities, so smaller flows are missing and the number of ports listed changes each year (27 in 2020, 21 in 2023); the shares are shares of the listed total, not of all US grain. The data end in 2023.
