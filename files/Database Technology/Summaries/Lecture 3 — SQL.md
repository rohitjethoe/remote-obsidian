---
date: 2025-11-22
title: SQL
tags:
  - CSE1500
---
## Lecture Slides
****
**Requirements of a DB Language**
****
**Functional Requirements**:
- Create database & relational structures
- Perform data management tasks:
	- **Insertion**
	- **Modification**
	- **Deletion**
- Perform simple and complex queries

**Non-functional Requirements**:
- Structure & syntax easy to learn
- Portability across systems

****
**The SQL Language**
****
SQL = Structured Query Language
- Richer than a query language: A DML & DDL/VDL
- Declarative language: describes what to do with data, not how to do it

Set-Based Language: Operators work on relations and results are always relations
- Rows (tuples/records)
- Columns (attributes/fields)

There are three major classes of DB operations:
- **Data Definition Language (DDL)**: defining relations, attributes, domains, constraints
- **Data Manipulation Language (DML)**: adding, deleting and modifying tuples
- Asking queries (often part of the DML)

****
**Data Definition Language**
****
**Creation, modification & deletion of tables:**

```sql
CREATE TABLE, ALTER TABLE, DROP TABLE;
```

**Deriving tables/views:**

```sql
CREATE VIEW, ALTER VIEW, DROP VIEW;
```

**Indexes:**

```sql
CREATE INDEX, DROP INDEX;
```

**Management of user access control:**

```sql
GRANT, REVOKE;
```

**Retrieve information:**

```sql
SELECT
```

**Instructions to modify the database:**
- `INSERT`: add new row(s) to a table
- `UPDATE`: modify existing row(s) in a table
- `DELETE`: delete existing row(s) from a table

