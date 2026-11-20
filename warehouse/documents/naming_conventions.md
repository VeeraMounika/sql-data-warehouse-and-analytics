# Naming Conventions

This document describes the naming standards used across the data warehouse.

## General Principles
- Use lowercase `snake_case` with underscores.
- Use English for all names.
- Avoid SQL reserved keywords.

## Table Naming Conventions

### Bronze and Silver Layers
Follow the source system and original entity name:

`<sourcesystem>_<entity>`

Examples: `crm_cust_info`, `erp_cust_az12`

### Gold Layer
Use business-friendly names with category prefixes:

`<category>_<entity>`

- `dim_` – Dimension tables (e.g., `dim_customers`, `dim_products`)
- `fact_` – Fact tables (e.g., `fact_sales`)

## Column Naming Conventions

- **Surrogate Keys:** Use the `_key` suffix (e.g., `customer_key`, `product_key`).
- **Technical Columns:** Use the `dwh_` prefix (e.g., `dwh_create_date`).

## Stored Procedure Naming

Use the pattern:

`load_<layer>`

Examples: `load_bronze`, `load_silver`.
