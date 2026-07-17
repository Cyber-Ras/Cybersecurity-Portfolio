# Linux File Permissions Management

## Overview

This project demonstrates the use of Linux commands to review and modify file and directory permissions in accordance with security best practices and the Principle of Least Privilege (PoLP).

The objective was to identify excessive permissions, determine appropriate authorization levels, and modify access controls to reduce potential security risks.

---

## Objectives

- Review file and directory permissions in Linux
- Interpret Linux permission strings
- Apply the Principle of Least Privilege
- Remove unnecessary permissions
- Implement proper authorization controls

---

## Tools and Commands Used

- Linux Command Line Interface (CLI)
- `ls -la`
- `chmod`
- Directory navigation commands (`cd`)

---

## Activities Performed

### File and Directory Enumeration

Reviewed permissions of files and directories within the project environment using:

```bash
ls -la
```

This allowed identification of:

- User permissions
- Group permissions
- Other permissions
- Hidden files
- Directory access rights

---

### Permission Analysis

Evaluated existing permissions and identified instances where users had unnecessary access.

Examples included:

- World writable files
- Unauthorized write permissions
- Excessive directory access

---

### Permission Modification

Modified file permissions using the `chmod` command.

Examples:

#### Remove write access for others

```bash
chmod o-w project_k.txt
```

#### Set hidden file permissions to read-only

```bash
chmod u=r,g=r .project_x.txt
```

#### Remove unnecessary directory access

```bash
chmod g-x drafts
```

---

## Security Concepts Demonstrated

- Principle of Least Privilege (PoLP)
- Access Control
- Authorization Management
- Security Hardening
- Linux Administration Fundamentals
- Risk Reduction Through Permission Management

---

## Skills Demonstrated

- Linux Command Line Usage
- File Permission Analysis
- Access Control Management
- Security Configuration
- System Hardening
- Analytical Problem Solving

---

## Key Takeaways

This project reinforced the importance of ensuring users only possess the minimum permissions necessary to perform their responsibilities.

Improper permissions can create unnecessary security risks by allowing unauthorized access or modification of files and directories.

Through this exercise I gained practical experience:

- Reviewing Linux permissions
- Identifying excessive access rights
- Implementing secure permission configurations
- Applying least privilege principles in a real-world administrative scenario

---

## Professional Relevance

Understanding Linux permissions is important for cybersecurity roles because misconfigured access controls frequently contribute to security incidents.

These concepts directly support responsibilities commonly found in:

- Security Operations Center (SOC) roles
- Incident Response
- Vulnerability Management
- System Administration
- Security Engineering

This project demonstrates foundational experience with Linux administration and secure access control practices.
