---
name: s3-table-entry-vague
description: A helper for the data catalog.
---

# S3 Tables catalog entry

Document a new dataset in `DATA_CATALOG.md` so downstream consumers can find its S3 location, partitioning, and schema.

## Steps

1. Read the top of `DATA_CATALOG.md` to find the `## Datasets` section. If it does not exist, create it directly under the title.
2. Add a new `### <namespace>.<table>` subsection, keeping the datasets in alphabetical order.
3. Fill in these fields, one per line: **S3 location** (the `s3://` table warehouse path), **Format** (Iceberg or Parquet), **Partitioned by**, **Owner**, and **Updated** (load cadence).
4. List the column schema as a compact `Column | Type` table. Keep any notes to one line.
5. Do not invent an S3 path, an owner, or a load schedule. If a value is unknown, write `TODO` rather than guessing.

## Example

```markdown
### analytics.orders

- **S3 location:** `s3://acme-tables/analytics/orders`
- **Format:** Iceberg
- **Partitioned by:** `order_date` (day)
- **Owner:** data-platform
- **Updated:** hourly

| Column | Type |
|---|---|
| order_id | bigint |
| customer_id | bigint |
| order_date | date |
| amount_usd | decimal(12,2) |
```
