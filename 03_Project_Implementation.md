# Project Implementation

> **Project:** Keycloak IAM with Django
>
> This document describes the implementation tasks for the project.
>
> You are expected to research, design, implement, and document your solution. The objective is not just to make the project work, but to understand every component involved.
>
> Do **not** skip documentation while implementing.

---

# Project Objective

Build a Django application that uses **Keycloak** as its Identity Provider (IdP) for authentication and authorization.

The final application should:

- Authenticate users using Keycloak.
- Protect authenticated routes.
- Support role-based authorization.
- Allow users to log out correctly.
- Demonstrate understanding of enterprise IAM architecture.

---

# Deliverables

At the end of implementation, submit:

- Source Code
- README
- Screenshots
- Architecture Diagram
- Documentation
- Demo

---

# Task 1 — Prepare the Development Environment

## Objective

Prepare your local development environment.

## Requirements

Install and configure:

- Git
- Python
- Docker
- Docker Compose (if required)
- VS Code (or preferred IDE)

## Deliverables

- Screenshot of installed software
- Version information for each tool

## Validation

All required software should be installed and working.

---

# Task 2 — Setup Keycloak

## Objective

Run Keycloak locally.

## Requirements

- Run Keycloak using a supported approach.
- Access the Keycloak Admin Console.
- Create an administrator account.

## Deliverables

Include screenshots of:

- Running Keycloak
- Login screen
- Admin Console

## Validation

You should be able to access the Admin Console successfully.

---

# Task 3 — Create a Realm

## Objective

Create a dedicated realm for this project.

## Requirements

- Create one realm.
- Give the realm a meaningful name.
- Document why realms are used.

## Deliverables

- Screenshot of the created realm.
- Short explanation of the purpose of a realm.

## Validation

The realm should be visible in the Admin Console.

---

# Task 4 — Configure a Client

## Objective

Create a client representing the Django application.

## Requirements

Configure:

- Client Name
- Client Type
- Redirect URI
- Logout URI
- Web Origins

Document why each configuration is required.

## Deliverables

Screenshots of the client configuration.

## Validation

The client should be successfully created and enabled.

---

# Task 5 — Create Users

## Objective

Create users for testing.

## Requirements

Create at least three users.

Suggested roles:

- Administrator
- Developer
- Viewer

Configure passwords.

## Deliverables

Screenshots of created users.

## Validation

Each user should be able to authenticate successfully.

---

# Task 6 — Configure Roles

## Objective

Implement Role-Based Access Control.

## Requirements

Create application roles.

Assign appropriate roles to each user.

Document your RBAC design.

## Deliverables

- Screenshots
- RBAC documentation

## Validation

Every user should have at least one assigned role.

---

# Task 7 — Create the Django Project

## Objective

Create a new Django application.

## Requirements

- Initialize the project.
- Organize the project structure.
- Configure environment variables.

## Deliverables

Repository structure.

## Validation

The Django application should run successfully.

---

# Task 8 — Integrate Keycloak

## Objective

Configure Django to authenticate using Keycloak.

## Requirements

Research and configure:

- OpenID Connect
- Client ID
- Client Secret
- Issuer URL
- Redirect URLs

Document every configuration value.

## Deliverables

Configuration documentation.

## Validation

Django should redirect users to Keycloak for authentication.

---

# Task 9 — Implement Login

## Objective

Implement authentication using Keycloak.

## Requirements

Users should be able to:

- Open the application.
- Be redirected to Keycloak.
- Authenticate successfully.
- Return to Django.

## Deliverables

Screenshots showing the complete login flow.

## Validation

Users should reach the dashboard after successful authentication.

---

# Task 10 — Display User Information

## Objective

Display authenticated user information.

## Requirements

Display at least:

- Username
- Email
- Assigned Roles

Research how this information is obtained.

## Deliverables

Dashboard screenshot.

## Validation

Displayed information should match the authenticated user.

---

# Task 11 — Protect Application Routes

## Objective

Restrict access to authenticated users.

## Requirements

Unauthenticated users must not access protected pages.

Document your implementation approach.

## Deliverables

Screenshots demonstrating:

- Authorized access
- Unauthorized access

## Validation

Protected routes should redirect unauthenticated users appropriately.

---

# Task 12 — Implement Role-Based Access

## Objective

Restrict pages based on user roles.

## Requirements

Create at least three protected sections.

Example:

- Administrator Dashboard
- Developer Dashboard
- Viewer Dashboard

Only users with appropriate roles should gain access.

## Deliverables

Screenshots of successful and denied access.

## Validation

Role restrictions should work as expected.

---

# Task 13 — Implement Logout

## Objective

Implement secure logout.

## Requirements

Logging out should:

- End the Django session.
- End the Keycloak session.

Research the correct logout flow.

## Deliverables

Logout demonstration.

## Validation

After logout, protected pages should no longer be accessible.

---

# Task 14 — Handle Errors

## Objective

Implement appropriate error handling.

## Test scenarios

- Invalid login
- Incorrect configuration
- Expired session
- Unauthorized access
- Invalid token

## Deliverables

Document how each scenario was handled.

---

# Task 15 — Documentation

## Objective

Document your implementation.

Include:

- Architecture
- Authentication Flow
- Authorization Flow
- Challenges
- Learnings
- Future Improvements

## Deliverables

Markdown documentation inside the repository.

---

# Bonus Tasks

Complete any of the following for additional learning.

## Bonus 1

Enable self-registration.

---

## Bonus 2

Enable password reset.

---

## Bonus 3

Enable email verification.

---

## Bonus 4

Configure Multi-Factor Authentication (MFA).

---

## Bonus 5

Configure Google Login.

---

## Bonus 6

Configure GitHub Login.

---

## Bonus 7

Deploy the application using Docker.

---

# Final Validation Checklist

- [ ] Keycloak installed
- [ ] Realm created
- [ ] Client configured
- [ ] Users created
- [ ] Roles created
- [ ] Django project created
- [ ] Django integrated with Keycloak
- [ ] Login working
- [ ] Logout working
- [ ] Protected routes implemented
- [ ] Role-based access implemented
- [ ] Documentation completed
- [ ] Screenshots captured
- [ ] README updated

---

# Important Notes

- Do not commit secrets or passwords to Git.
- Use environment variables wherever appropriate.
- Keep commits small and meaningful.
- Document design decisions.
- If you encounter issues, document your troubleshooting process instead of simply applying fixes.
- During the final review, you may be asked to explain your implementation choices and demonstrate your understanding of the authentication flow.

> **Completion of all implementation tasks, along with clear documentation and a working demonstration, constitutes successful completion of this project.**
