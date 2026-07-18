# Hack The Box - Appointment

## Difficulty
Very Easy

## Objective
Gain access to the web application by exploiting a SQL Injection vulnerability.

## Tools Used
- Nmap
- Firefox
- Gobuster

## Enumeration

```bash
nmap -sV -p80 TARGET_IP
```

Result:

```
80/tcp open http Apache 2.4.38
```

## Vulnerability

The login page was vulnerable to SQL Injection.

Input:

```
admin' --
```

allowed authentication to be bypassed.

## Remediation

- Use parameterized queries.
- Validate user input.
- Avoid constructing SQL queries by concatenating strings.

## What I Learned

Through this lab, I developed an understanding of SQL Injection authentication bypass and why parameterized queries are essential to prevent user input from being executed as SQL commands. Additionally, I practiced using Gobuster to discover hidden directories and improve web application enumeration.
