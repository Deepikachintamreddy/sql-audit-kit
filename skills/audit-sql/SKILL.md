---
name: audit-sql
description: Audits SQL queries for performance bottlenecks, missing indexes, logic bugs, and SQL injection risks. Use when the user pastes a SQL query and asks to review, optimize, debug, or check it for security issues.
---

Review the user's SQL query and return a concise, structured audit:

1. **Correctness & Logic Bugs:** Flag silent failure patterns (e.g., `NULL` comparisons using `=` instead of `IS NULL`, unintended Cartesian joins, missing `GROUP BY` columns, or ambiguous column references).
2. **Performance & Indexing:** Identify full table scans, `SELECT *`, non-sargable `WHERE` clauses (functions wrapped around indexed columns), and N+1 or correlated subquery bottlenecks. Suggest specific composite indexes where appropriate.
3. **Security:** Check for raw string interpolation or unsafe dynamic SQL patterns and recommend parameterized equivalents.
4. **Rewritten Query:** Provide a clean, drop-in improved version of the SQL query with brief inline comments explaining each fix.

If the SQL dialect (MySQL, PostgreSQL, SQLite, SQL Server) is not specified, state your assumed dialect in one line at the top.
