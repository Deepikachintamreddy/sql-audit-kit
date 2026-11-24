# SQL Audit Kit

A lightweight Claude plugin that reviews SQL queries for logic bugs, performance bottlenecks, indexing opportunities, and SQL injection risks.

## What It Includes
- **`audit-sql` skill:** Automatically activates when you ask Claude to review, debug, or optimize a SQL query, or invoke it directly with `/audit-sql`.

## Example Usage
Paste any SQL query into Claude and ask:
> "Audit this MySQL query for slow joins and missing indexes."

## Data Handling & Privacy
This plugin contains only local prompt instructions (`SKILL.md`). It does not make external network requests, does not connect to external servers, and does not collect, store, or transmit user data outside your Claude session.

## License
MIT
