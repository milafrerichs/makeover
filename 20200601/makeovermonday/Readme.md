# Makeover Monday Week 1 2020


## Queries
https://data.world/milafrerichs/makeover-monday-most-popular-viewing-sport-usa/workspace/query?queryid=9b189c0e-b750-49bf-8fb6-6c658b025ccb

```SQL
SELECT sport,week_1.`2017` as viewer_percentage,2017 as year,
    CASE (week_1.`2017`-week_1.`2004`)
        WHEN > 0 THEN "incr"
        WHEN < 0 THEN "decr"
        ELSE ""
        END AS `inc_decr`
FROM week_1
UNION ALL
SELECT sport,week_1.`2004` as viewer_percentage,2014 as year,
CASE (week_1.`2017`-week_1.`2004`)
        WHEN > 0 THEN "incr"
        WHEN < 0 THEN "decr"
        ELSE ""
        END AS `inc_decr`
FROM week_1
```

## Data Source
https://data.world/makeovermonday/2020w1-what-is-americas-most-popular-sport
