# Project: SonicWave Analytics Platform

## The Business Question

How does listening behaviour and revenue break down across plan tiers over time - attributing every play to the plan and price each user actually held at the moment of that play

## Example queries the model must support

Each query below references at least one technique the model has to demonstrate:

1. **Listening minutes per plan tier, per month** — total minutes streamed grouped by the plan the user held *at play time* and by calendar month.
   *[point-in-time SCD2 join · GROUP BY · DATE_TRUNC]*

2. **Revenue per plan, per month, at the price in effect then** — monthly recurring revenue attributed to each plan using the price valid at the time, so the 7.99 → 9.99 change shows up correctly in the timeline.
   *[point-in-time SCD2 pricing · aggregation]*
