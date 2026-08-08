# Retail Sales Analytics — Snowflake

This folder contains the Snowflake SQL used for the retail sales analytics project.

## Architecture

Raw CSV files
→ Internal Stage
→ RAW tables
→ STAGING tables
→ ANALYTICS star schema
→ Streams
→ Tasks
→ Incremental MERGE
→ Power BI

## SQL files

| File | Purpose |
|---|---|
| `01_environment_setup.sql` | Warehouse, database, and schema setup |
| `02_raw_layer_and_stage.sql` | Raw tables, CSV file format, and internal stage |
| `03_raw_load.sql` | COPY INTO commands for six cleaned CSV files |
| `04_staging_and_business_logic.sql` | Staging tables and sales calculations |
| `05_analytics_model.sql` | Dimension and fact tables |
| `06_customer_incremental_automation.sql` | Stream, MERGE, and automated task |
| `07_validation.sql` | Data-quality and row-count checks |

## Notes

- The source data was cleaned before Snowflake ingestion.
- `DISCOUNT_PCT` is stored as a whole-number percentage (for example, `10` means 10%).
- `FACT_SALES` is the transactional fact table at order-item grain.
- `CUSTOMER_STREAM` captures changes to `RAW.CUSTOMER_RAW`.
- `CUSTOMER_LOAD_TASK` processes stream changes incrementally with `MERGE`.
