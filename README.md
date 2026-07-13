# Keycloak IAM with Django

> Enterprise Identity and Access Management (IAM) implementation using **Keycloak** as the Identity Provider (IdP) and **Django** as the web application.

---

## Project Overview

This repository serves as the onboarding project for interns joining the backend/cloud engineering team.

The objective of this project is to understand how enterprise applications authenticate users using a centralized Identity Provider instead of maintaining authentication logic within every application.

In this project, you will integrate **Keycloak** with a **Django** application using the **OpenID Connect (OIDC)** protocol.

By the end of this project, you should understand not only *how* the integration works, but also *why* modern organizations rely on Identity and Access Management (IAM) solutions.

---

# Project Goals

By completing this project, you will learn:

- Identity and Access Management (IAM)
- Authentication vs Authorization
- OAuth 2.0
- OpenID Connect (OIDC)
- JSON Web Tokens (JWT)
- Keycloak Architecture
- Django Authentication
- Role-Based Access Control (RBAC)
- Session Management
- Enterprise Authentication Flows

---

# Learning Objectives

After completing this project, you should be able to answer the following questions:

- What is IAM?
- What problems does Keycloak solve?
- What is an Identity Provider?
- What is OAuth2?
- What is OpenID Connect?
- What is a JWT?
- What is an Access Token?
- What is a Refresh Token?
- What is a Realm?
- What is a Client?
- How does Django trust Keycloak?
- How does SSO work?
- How is authorization implemented?

If you can confidently answer these questions and demonstrate a working implementation, the project can be considered successfully completed.

---

# Repository Structure

```
keycloak-django-iam/
│
├── README.md
├── 01_Project_Overview.md
├── 02_IAM_Theory_Guide.md
├── 03_Implementation_Guide.md
├── 04_Testing_Checklist.md
├── 05_Project_Deliverables.md
│
├── diagrams/
│     ├── architecture.png
│     ├── oidc-flow.png
│     ├── jwt-structure.png
│     ├── rbac.png
│     └── keycloak-components.png
│
├── screenshots/
│
└── sample-project/
```

---

# Documentation Order

Read the documents in the following order.

| Step | Document | Purpose |
|-------|----------|----------|
| 1 | Project Overview | Understand the project |
| 2 | IAM Theory Guide | Learn the concepts |
| 3 | Implementation Guide | Build the project |
| 4 | Testing Checklist | Validate implementation |
| 5 | Project Deliverables | Submit the project |

Do **not** start coding before reading the first two documents.

Understanding the concepts is an important part of this assignment.

---

# High-Level Architecture

```text
                    User
                     │
                     ▼
              Django Application
                     │
                     │ Redirect
                     ▼
             +------------------+
             |    Keycloak      |
             | Identity Provider|
             +------------------+
                     │
              Authenticate User
                     │
             Generate JWT Tokens
                     │
                     ▼
              Django validates
                     │
                     ▼
             User is authenticated
```

---

# Authentication Flow

```text
Browser

↓

Open Django

↓

Click Login

↓

Redirect to Keycloak

↓

Enter Credentials

↓

Keycloak verifies credentials

↓

Authorization Code

↓

Django exchanges code

↓

Access Token

↓

ID Token

↓

User Session Created

↓

Dashboard
```

---

# Project Scope

The intern is expected to:

- Install Keycloak
- Configure a Realm
- Configure a Client
- Create Users
- Create Roles
- Integrate Django
- Configure OIDC Authentication
- Implement Login
- Implement Logout
- Protect Routes
- Implement RBAC
- Validate JWT Tokens
- Test the application

---

# Out of Scope

The following topics are optional and are not mandatory for successful completion of this project.

- LDAP Integration
- Active Directory
- Kubernetes Deployment
- Multi-Realm Architecture
- Keycloak Clustering
- High Availability
- Custom Authentication Providers
- Custom Themes

These topics may be explored as bonus tasks.

---

# Project Timeline

| Phase | Duration |
|---------|----------|
| IAM Concepts | 2 Days |
| Keycloak Setup | 1 Day |
| Django Setup | 1 Day |
| OIDC Integration | 2 Days |
| RBAC | 1 Day |
| Testing | 1 Day |
| Documentation | 1 Day |

Estimated duration:

**8–10 Working Days**

---

# Expected Deliverables

The final submission should include:

- Working Django Application
- Working Keycloak Instance
- Documentation
- Screenshots
- Testing Report
- README
- Source Code

---

# Skills You Will Gain

## Identity

- Identity Providers
- Authentication
- Authorization

## Security

- OAuth2
- OpenID Connect
- JWT
- Sessions

## Backend

- Django
- Middleware
- Route Protection
- RBAC

## Enterprise

- Keycloak
- IAM
- SSO
- User Management

---

# Software Required

Install the following software before beginning the project.

| Software | Purpose |
|----------|----------|
| Python 3.12+ | Backend |
| Django | Web Framework |
| Docker | Run Keycloak |
| Git | Version Control |
| VS Code | IDE |
| PostgreSQL (Optional) | Database |

---

# Prerequisites

The intern should have a basic understanding of:

- Python
- Django
- REST APIs
- HTTP
- HTML
- Git
- Docker (Basic)

No prior knowledge of OAuth or Keycloak is required.

---

# Success Criteria

The project is considered complete when:

- Django redirects users to Keycloak for authentication.
- Login succeeds using Keycloak credentials.
- Users can log out successfully.
- Private pages are protected.
- RBAC is implemented.
- JWT tokens are validated.
- Documentation is complete.
- The intern can explain the complete authentication flow.

---

# Recommended Reading Order

```
README

↓

01_Project_Overview

↓

02_IAM_Theory_Guide

↓

03_Implementation_Guide

↓

04_Testing_Checklist

↓

05_Project_Deliverables
```

---

# Repository Standards

Follow these guidelines throughout the project.

- Use meaningful commit messages.
- Write clean, readable code.
- Add comments where necessary.
- Do not hardcode secrets.
- Use environment variables.
- Keep documentation updated.
- Commit frequently.

---

# References

## Keycloak

https://www.keycloak.org/

## Django

https://docs.djangoproject.com/

## OAuth2

https://oauth.net/2/

## OpenID Connect

https://openid.net/connect/

## JWT

https://jwt.io

---

# Final Goal

By the end of this project, you should have built a production-style authentication system where:

- Keycloak acts as the centralized Identity Provider.
- Django delegates authentication to Keycloak.
- Users authenticate using OpenID Connect.
- Authorization is controlled using Keycloak Roles.
- JWT tokens are securely validated.
- The application follows enterprise IAM best practices.

More importantly, you should understand **why** each component exists and how they work together to provide secure authentication and authorization.
