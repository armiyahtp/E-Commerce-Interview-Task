# Architecture Plan

## Database Schema
- customers (id, name, email)
- orders (id, customer_id, total_amount, status, shipping_region, created_at)
- Relationship: One customer → many orders

## SQL Injection Prevention
- Use Django database cursor with parameterized queries (%s)
- No string concatenation with user input
- Allow-list mapping for dynamic queries (Part C)

## Database Connections
- Use Django’s built-in connection pooling via psycopg2

## API Validation
- Validate query parameters manually
- Validate view_name and fields using metadata mapping
