# Learning Assignments

> **Project:** Keycloak IAM with Django
>
> Before starting implementation, you are expected to understand the technologies involved in this project. This document contains a list of research assignments that you must complete.
>
> **Important:** Do not simply copy definitions from blogs or AI tools. The objective is to understand the concepts well enough that you can explain them and apply them during implementation.

---

# General Instructions

- Complete the assignments in order.
- Use the official documentation as the primary source.
- Maintain your own notes throughout the project.
- You may use additional resources such as blogs, YouTube, or documentation, but always verify your understanding using the official documentation.
- Be prepared to explain every topic during the final project review.

---

# Assignment 1 – Identity and Access Management (IAM)

## Objective

Understand what Identity and Access Management is and why organizations use it.

## Topics to Research

- What is Identity?
- What is Identity and Access Management (IAM)?
- Why do organizations need IAM?
- Problems solved by IAM
- Benefits of centralized authentication

## Deliverables

Prepare notes covering:

- Definition of IAM
- Real-world use cases
- Advantages of IAM

## Success Criteria

You should be able to explain why enterprise applications rarely manage authentication independently.

---

# Assignment 2 – Authentication vs Authorization

## Objective

Understand the difference between authentication and authorization.

## Topics to Research

- Authentication
- Authorization
- Examples of each
- Why authentication always happens before authorization

## Deliverables

Create a comparison table between authentication and authorization with at least five differences.

## Success Criteria

You should be able to identify whether a real-world scenario relates to authentication or authorization.

---

# Assignment 3 – OAuth 2.0

## Objective

Understand OAuth 2.0 and the problem it solves.

## Topics to Research

- Why OAuth was introduced
- OAuth 2.0 Roles
- Authorization Code Flow
- Client Credentials Flow
- Access Token
- Refresh Token
- Scopes

## Deliverables

Prepare a flow diagram explaining the Authorization Code Flow.

## Success Criteria

Explain why OAuth is an authorization framework and not an authentication protocol.

---

# Assignment 4 – OpenID Connect (OIDC)

## Objective

Understand how OpenID Connect extends OAuth 2.0.

## Topics to Research

- What is OpenID Connect?
- Why OIDC exists
- ID Token
- UserInfo Endpoint
- Discovery Endpoint

## Deliverables

Write a short comparison between OAuth 2.0 and OpenID Connect.

## Success Criteria

Explain why our Django application uses OIDC.

---

# Assignment 5 – JSON Web Tokens (JWT)

## Objective

Understand JWTs and how they are used in authentication.

## Topics to Research

- JWT Structure
- Header
- Payload
- Signature
- Claims
- Token Expiration
- Token Validation

## Deliverables

Decode a sample JWT using https://jwt.io and explain the information it contains.

## Success Criteria

You should be able to explain why JWT signatures are important.

---

# Assignment 6 – Keycloak

## Objective

Become familiar with Keycloak.

## Topics to Research

- What is Keycloak?
- Features
- Supported Protocols
- Admin Console
- Architecture

## Deliverables

Prepare notes describing how Keycloak fits into the authentication flow.

## Success Criteria

Explain why Keycloak is used instead of implementing authentication directly inside Django.

---

# Assignment 7 – Keycloak Components

## Objective

Understand the major components available in Keycloak.

## Topics to Research

- Realms
- Clients
- Users
- Roles
- Groups
- Client Scopes
- Authentication Flows
- Sessions

## Deliverables

Create a one-page summary describing the purpose of each component.

## Success Criteria

Explain the purpose of each component without referring to documentation.

---

# Assignment 8 – Single Sign-On (SSO)

## Objective

Understand Single Sign-On.

## Topics to Research

- What is SSO?
- Benefits
- Login Flow
- Single Logout

## Deliverables

Create a simple diagram showing how SSO works across multiple applications.

## Success Criteria

Explain how one login provides access to multiple applications.

---

# Assignment 9 – Role-Based Access Control (RBAC)

## Objective

Understand Role-Based Access Control.

## Topics to Research

- Roles
- Permissions
- Least Privilege Principle
- Access Control

## Deliverables

Create an example RBAC model for an organization.

Example:

- Administrator
- Developer
- Viewer

List the permissions assigned to each role.

## Success Criteria

Design a secure RBAC model for a sample application.

---

# Assignment 10 – Django Authentication

## Objective

Understand Django's built-in authentication system.

## Topics to Research

- Authentication
- Authorization
- Sessions
- Middleware
- Login Required Decorator
- User Model

## Deliverables

Summarize how Django handles authentication by default.

## Success Criteria

Explain how using Keycloak changes Django's default authentication flow.

---

# Assignment 11 – Project Architecture

## Objective

Understand the architecture of this project before implementation.

## Study the following architecture

```
+-------------+
|   Browser   |
+-------------+
       |
       |
       ▼
+----------------+
| Django Backend |
+----------------+
       |
Redirect User
       |
       ▼
+----------------------+
|      Keycloak        |
+----------------------+
       |
Authenticate User
       |
Issue Tokens
       |
       ▼
+----------------+
| Django Session |
+----------------+
```

## Deliverables

Explain the responsibility of each component.

## Success Criteria

Describe the complete authentication flow from browser to dashboard.

---

# Assignment 12 – Security Best Practices

## Objective

Research common security practices for authentication systems.

## Topics to Research

- HTTPS
- Client Secrets
- Token Expiration
- Password Policies
- Multi-Factor Authentication
- Secure Session Management

## Deliverables

Prepare a checklist of security practices that should be followed in this project.

## Success Criteria

Explain why each practice improves security.

---

# Final Learning Review

Once all assignments are completed, you should be able to confidently answer the following questions:

- What is IAM?
- What is an Identity Provider?
- Why is Keycloak used?
- What is OAuth 2.0?
- What is OpenID Connect?
- What is the Authorization Code Flow?
- What is a JWT?
- What is the difference between an Access Token and an ID Token?
- What is a Realm?
- What is a Client?
- What are Roles?
- What are Groups?
- What is RBAC?
- How does Django authenticate users using Keycloak?
- How does Single Sign-On work?

If you cannot answer any of the above questions confidently, revisit the corresponding assignment before proceeding with implementation.

---

# References

Use the official documentation wherever possible.

- https://www.keycloak.org/documentation
- https://www.keycloak.org/guides
- https://docs.djangoproject.com/
- https://oauth.net/2/
- https://openid.net/connect/
- https://jwt.io
- https://www.rfc-editor.org/

---

# Completion Checklist

- [ ] Assignment 1 Completed
- [ ] Assignment 2 Completed
- [ ] Assignment 3 Completed
- [ ] Assignment 4 Completed
- [ ] Assignment 5 Completed
- [ ] Assignment 6 Completed
- [ ] Assignment 7 Completed
- [ ] Assignment 8 Completed
- [ ] Assignment 9 Completed
- [ ] Assignment 10 Completed
- [ ] Assignment 11 Completed
- [ ] Assignment 12 Completed

**Do not start the implementation phase until all learning assignments have been completed.**
