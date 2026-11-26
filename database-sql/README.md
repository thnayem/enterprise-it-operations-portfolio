# DBMS & SQL Reference

## Scope

Foundational relational database concepts and safe SQL examples for application support, reporting and troubleshooting. Syntax can vary between MySQL/MariaDB, PostgreSQL, Microsoft SQL Server and other database engines.

## Core Topics

- Tables, rows, columns, primary keys and foreign keys.
- Relationships, normalization and indexes.
- SELECT filtering, sorting, grouping and joins.
- Transactions and data consistency.
- Backup, restore and access control.
- Query performance basics and execution plans.

## Generic SQL Examples

The following examples use illustrative table and column names. Confirm schema and SQL dialect before use.

### Filter records

```sql
SELECT id, status, created_at
FROM service_requests
WHERE status = 'OPEN'
ORDER BY created_at DESC;
```

### Aggregate by status

```sql
SELECT status, COUNT(*) AS total
FROM service_requests
GROUP BY status
ORDER BY total DESC;
```

### Join related records

```sql
SELECT u.user_name, r.request_id, r.status
FROM users AS u
JOIN service_requests AS r
  ON r.user_id = u.id
WHERE r.status = 'OPEN';
```

### Parameterized query concept

Use prepared statements and bind parameters through the application database driver. Do not concatenate untrusted user input into SQL strings.

## Query Review Checklist

- Select only the columns required.
- Filter using indexed columns where appropriate.
- Review join conditions and expected row counts.
- Avoid unnecessary functions on indexed filter columns.
- Use an execution plan before optimizing.
- Validate changes on representative non-production data.
- Consider transaction boundaries for multi-step updates.

## Backup & Recovery

- Define RPO and RTO with business owners.
- Use database-native backup methods appropriate to the engine.
- Protect backup files with access controls and encryption.
- Store a separate copy according to the organization's backup policy.
- Test restore regularly; a successful backup job alone does not prove recoverability.
- Document point-in-time recovery requirements where supported.

## Safety

Examples in this repository are read-only. Never run UPDATE, DELETE, DROP, TRUNCATE or schema-changing statements in production without authorization, a reviewed change plan, a verified backup and a rollback strategy. Never publish database dumps, credentials, personal information or production schema details.
