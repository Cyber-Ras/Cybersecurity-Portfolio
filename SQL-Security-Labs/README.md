# SQL Security Investigations

## Overview

This project demonstrates the use of SQL queries to investigate security-related events and analyze organizational data.

Using SQL filtering techniques and logical operators, I examined login activity and employee records to identify potentially suspicious events and support security investigations.

---

## Objectives

- Investigate authentication activity using SQL
- Identify potentially suspicious login attempts
- Review employee data for security purposes
- Develop experience filtering large datasets
- Apply analytical thinking to security investigations

---

## Tools and Technologies Used

- SQL
- Relational Databases
- SQL Filtering Operators
- Pattern Matching Techniques

---

## SQL Concepts Demonstrated

### Operators Used

- `WHERE`
- `AND`
- `OR`
- `NOT`
- `LIKE`
- Wildcards (`%`)
- Greater Than (`>`)

---

## Security Investigation Scenarios

### After-Hours Login Investigation

Used SQL queries to identify login attempts occurring outside normal business hours.

Example:

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '1800';
```

Purpose:

- Review after-hours authentication activity
- Identify potentially suspicious login behavior
- Support security monitoring efforts

---

### Login Attempts on Specific Dates

Queried authentication activity occurring on specific dates surrounding a potentially suspicious event.

Example:

```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09'
OR login_date = '2022-05-08';
```

Purpose:

- Investigate activity surrounding security events
- Identify patterns and timelines

---

### Geographic Login Analysis

Reviewed login attempts originating outside expected geographic locations.

Example:

```sql
SELECT *
FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

Purpose:

- Identify anomalous login activity
- Investigate potentially unauthorized access attempts

---

### Employee Access Review

Retrieved employee records for specific departments and locations.

Examples:

```sql
SELECT *
FROM employees
WHERE department = 'Marketing'
AND office LIKE 'East%';
```

```sql
SELECT *
FROM employees
WHERE department = 'Sales'
OR department = 'Finance';
```

Purpose:

- Support access reviews
- Assist with investigations involving user accounts and organizational assets

---

### Department Exclusion Analysis

Reviewed employee records outside Information Technology.

Example:

```sql
SELECT *
FROM employees
WHERE NOT department = 'Information Technology';
```

Purpose:

- Perform targeted investigations
- Filter organizational data efficiently

---

## Skills Demonstrated

- SQL Query Development
- Data Filtering and Analysis
- Authentication Investigation
- Security Monitoring Concepts
- Pattern Recognition
- Analytical Thinking
- Investigation Methodology
- Log Analysis Fundamentals

---

## Security Concepts Demonstrated

- Authentication Monitoring
- Suspicious Activity Identification
- Geographic Anomaly Detection
- Access Review Concepts
- Investigation and Triage Processes
- Data-Driven Security Analysis

---

## Key Takeaways

This project strengthened my understanding of how SQL can be used as a security investigation tool.

I gained practical experience:

- Querying large datasets
- Filtering security-relevant information
- Identifying patterns and anomalies
- Supporting investigations through data analysis

The ability to efficiently query and analyze data is an important skill for Security Operations Center (SOC) analysts and cybersecurity professionals.

---

## Professional Relevance

SQL is frequently used by cybersecurity professionals to:

- Investigate security events
- Analyze authentication logs
- Review user activity
- Identify suspicious behavior
- Support incident response investigations

This project demonstrates foundational experience applying SQL to security-focused use cases and investigative workflows.
