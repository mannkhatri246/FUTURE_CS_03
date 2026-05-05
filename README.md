## Overview

This repository contains a professional API Security Risk Analysis Report completed as part of the Cyber Security Internship at Future Interns.

The report presents findings from a read-only passive security assessment conducted on the JSONPlaceholder public API (jsonplaceholder.typicode.com). The assessment identifies common API security risks, classifies their severity, and provides practical remediation steps.

## Objective

- Analyze a public REST API for common security vulnerabilities
- Identify security risks across authentication, authorization, and configuration
- Classify each finding by risk level (Critical / High / Medium)
- Explain risks in simple business language
- Suggest clear and practical remediation steps

## Target API

| Field | Details |
|-------|---------|
| API Name | JSONPlaceholder |
| Base URL | https://jsonplaceholder.typicode.com |
| API Type | Public REST API - Demo/Testing Platform |
| Assessment Type | Read-Only Passive Security Analysis |
| Assessment Date | May 2026 |

## Vulnerabilities Found

| Sr. | Vulnerability | OWASP Category | Risk |
|-----|--------------|----------------|------|
| 1 | Unauthenticated Access to All Users | API2 - Broken Authentication | Critical |
| 2 | Unauthenticated Data Creation | API2 - Broken Authentication | Critical |
| 3 | Unauthenticated Data Deletion | API2 - Broken Authentication | Critical |
| 4 | Missing Security Headers | API7 - Security Misconfiguration | High |
| 5 | IDOR - Insecure Direct Object Reference | API1 - Broken Object Level Authorization | High |
| 6 | No Input Validation | API6 - Unrestricted Access to Sensitive Business Flows | High |
| 7 | Weak Rate Limiting Configuration | API4 - Unrestricted Resource Consumption | Medium |

## Summary

| Critical | High | Medium | Total |
|----------|------|--------|-------|
| 3 | 3 | 1 | 7 |

## Endpoints Tested

| Method | Endpoint | Purpose | Result |
|--------|---------|---------|--------|
| GET | /users | Retrieve all users | 200 OK |
| GET | /users/5 | Retrieve particular user | 200 OK |
| GET | /users/8/posts | Retrieve user posts | 200 OK |
| POST | /users | Create a new user | 201 Created |
| DELETE | /users/5 | Delete user | 200 OK |
| GET | /posts | Retrieve all posts | 200 OK |

## Tools Used

| Tool | Purpose |
|------|---------|
| Postman | API endpoint testing and response inspection |
| Browser DevTools | Header and response analysis |
| Manual Analysis | Identifying security misconfigurations and risks |

## Scope and Ethics

- Testing limited to public-facing endpoints only
- Read-only requests (GET) and safe POST requests only
- No exploitation, flooding, or denial-of-service testing performed
- No private or production APIs were targeted
- All testing conducted on a demo API specifically designed for testing purposes

## Disclaimer

This report was prepared strictly for educational purposes as part of a Cyber Security Internship. No real systems were attacked, no data was stolen or manipulated, and no individuals were harmed. All testing was conducted ethically and within the permitted scope of a publicly available demo API.
manipulated, and no individuals were harmed. All testing was conducted ethically and within the permitted scope of a publicly available demo API.

