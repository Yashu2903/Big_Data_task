PySpark HW2 Problem Set — LARGE Synthetic Datasets (Seed=42)

These files are synthetic and designed to preserve the same schemas as the public datasets,
but at big-data-friendly sizes (>= 50k rows each).

Files
-----
- p1_raw_events_large.jsonl         (65000 rows)  — includes duplicates, out-of-order ingests, bot UAs, timestamp ties
- p2_memberships_large.jsonl        (50000 rows)  — includes pauses, overlaps, invalid pauses, null member_id edge cases
- p2_plan_dim.csv                   (3 rows)
- p3_order_lines_large.jsonl        (55000 rows)  — includes messy SKUs, returns, null prices, duplicate line_numbers

Conventions
-----------
- Timestamps are ISO-8601 UTC strings with a trailing 'Z'.
- Dates are 'YYYY-MM-DD'.
- Timezone for all 'local date' computations in the problems: America/New_York

Recommended loading (students should define schemas explicitly):

from pyspark.sql.types import *
raw_events = spark.read.schema(<schema>).json('p1_raw_events_large.jsonl')

