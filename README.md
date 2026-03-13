

## Problem 1 — Bot-aware sessionization + week-over-week retention

This section:
1. Deduplicates replayed events using the required tie-break order
2. Classifies user agents with the required scalar Python UDF
3. Filters bot traffic
4. Sessionizes events using America/New_York local date logic
5. Computes weekly retention metrics using window functions

## Problem 2 — Prorated February billing with pauses

This section:
1. Expands active membership days within the February 2026 reporting window
2. Applies the required billing cohort UDF
3. Excludes paused days from billing while keeping them active
4. Computes prorated February billing using decimal-safe arithmetic
5. Produces daily cohort metrics by day, plan, and cohort
