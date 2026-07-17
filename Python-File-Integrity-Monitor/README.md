# Python Access Control Automation

## Overview

This project demonstrates the use of Python to automate access control management by updating an allow list of authorized IP addresses.

The scenario involved identifying employees whose IP addresses were no longer authorized to access a restricted healthcare subnetwork containing sensitive patient information. The script reads an allow list from a file, removes unauthorized IP addresses, and updates the file automatically.

---

## Objectives

- Automate access control management
- Remove unauthorized users from an allow list
- Improve administrative efficiency
- Reduce manual errors through scripting
- Apply Python programming to security operations

---

## Technologies Used

- Python 3
- File Handling
- Lists
- Loops
- Conditional Statements
- String Methods

---

## Security Scenario

A healthcare organization maintains a restricted network containing sensitive patient records.

Certain employees are no longer authorized to access this environment, requiring their IP addresses to be removed from the allow list.

The script automates this process by:

1. Reading authorized IP addresses from a file
2. Comparing them against a list of unauthorized IP addresses
3. Removing unauthorized entries
4. Updating the original allow list

---

## Core Python Concepts Demonstrated

### File Handling

```python
with open(import_file, "r") as file:
    ip_addresses = file.read()
```

Used Python file handling to import and read data from an external file.

---

### Data Conversion

```python
ip_addresses = ip_addresses.split()
```

Converted file contents into a list structure to allow processing and manipulation.

---

### Iteration

```python
for element in ip_addresses:
```

Used loops to process entries individually.

---

### Conditional Logic

```python
if element in remove_list:
```

Compared authorized entries against a removal list.

---

### List Manipulation

```python
ip_addresses.remove(element)
```

Removed unauthorized IP addresses from the allow list.

---

### Updating the File

```python
ip_addresses = " ".join(ip_addresses)

with open(import_file, "w") as file:
    file.write(ip_addresses)
```

Rebuilt the updated allow list and wrote the revised data back to the file.

---

## Security Concepts Demonstrated

- Access Control Management
- Authorization Review
- Least Privilege Principles
- Security Automation
- Administrative Security Controls
- Protection of Sensitive Data

---

## Skills Demonstrated

- Python Programming
- Security Automation
- File Handling
- Data Processing
- Access Management
- Scripting for Security Operations
- Problem Solving
- Analytical Thinking

---

## Key Takeaways

This project strengthened my understanding of how automation can assist security professionals in managing access controls efficiently.

Through this exercise, I gained practical experience:

- Reading and writing files with Python
- Manipulating data structures
- Automating repetitive administrative tasks
- Applying programming concepts to security use cases

---

## Professional Relevance

Security teams frequently use scripting and automation to manage:

- User access reviews
- Allow lists and block lists
- Security administration tasks
- Incident response workflows
- Large-scale data processing

This project demonstrates foundational experience using Python to automate security processes and improve operational efficiency.
