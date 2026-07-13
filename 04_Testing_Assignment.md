# Testing Assignment

> **Project:** Keycloak IAM with Django
>
> This document defines the testing activities that must be completed before the project is considered finished.
>
> The objective is to verify that the application works correctly, handles expected and unexpected scenarios, and follows good authentication and authorization practices.

---

# Objective

Validate that the Keycloak and Django integration is functioning correctly.

Testing should cover:

- Authentication
- Authorization
- Sessions
- Error Handling
- Security
- User Experience

---

# General Instructions

- Test every feature after implementation.
- Record all observations.
- Capture screenshots wherever applicable.
- If a test fails, document the issue and attempt to identify the root cause.
- Do not skip failed tests.

---

# Test Environment

Document your environment before testing.

Example:

| Item | Value |
|------|-------|
| Operating System | |
| Python Version | |
| Django Version | |
| Keycloak Version | |
| Browser | |
| Database | |

---

# Authentication Testing

## Test 1 – Successful Login

### Objective

Verify that a valid user can log in.

### Expected Result

- User is redirected to Keycloak.
- Authentication succeeds.
- User is redirected back to Django.
- Dashboard loads successfully.

### Evidence

- Screenshot
- Short description

---

## Test 2 – Invalid Username

### Objective

Attempt login with an invalid username.

### Expected Result

Authentication should fail.

### Evidence

Screenshot of the error.

---

## Test 3 – Invalid Password

### Objective

Attempt login using an incorrect password.

### Expected Result

Authentication should fail.

### Evidence

Screenshot.

---

## Test 4 – Disabled User

### Objective

Attempt login using a disabled account.

### Expected Result

Login should not succeed.

---

## Test 5 – Multiple Login Attempts

### Objective

Observe system behaviour after repeated failed logins.

### Record

- Number of attempts
- System response
- Any account restrictions

---

# Authorization Testing

## Test 6 – Administrator Access

### Objective

Verify Administrator permissions.

### Expected Result

Administrator can access all protected resources.

---

## Test 7 – Developer Access

### Objective

Verify Developer permissions.

### Expected Result

Developer cannot access Administrator-only resources.

---

## Test 8 – Viewer Access

### Objective

Verify Viewer permissions.

### Expected Result

Viewer should have only the permissions assigned during implementation.

---

## Test 9 – Unauthorized Page Access

### Objective

Attempt to directly access a restricted URL.

### Expected Result

Access should be denied or redirected.

---

# Session Testing

## Test 10 – Logout

### Objective

Verify logout behaviour.

### Expected Result

- Django session ends.
- Keycloak session ends.
- Protected pages are inaccessible.

---

## Test 11 – Browser Refresh

### Objective

Refresh the browser after login.

### Expected Result

Session should remain valid while authenticated.

---

## Test 12 – New Browser Session

### Objective

Open the application in another browser or incognito window.

### Expected Result

Authentication should be required unless an active SSO session exists.

---

## Test 13 – Session Expiration

### Objective

Observe behaviour when the session expires.

### Expected Result

User should be prompted to authenticate again or follow the configured session policy.

---

# Token Validation Testing

## Test 14 – JWT Inspection

### Objective

Inspect the JWT generated after login.

### Verify

- Username
- Email
- Roles (if present)
- Expiration Time
- Issuer
- Audience

### Deliverable

Brief explanation of the token contents.

---

## Test 15 – Expired Token

### Objective

Observe application behaviour when a token is no longer valid.

### Expected Result

Access should be denied or a new token obtained according to the implementation.

---

# Route Protection Testing

## Test 16 – Protected Routes

### Objective

Attempt to access protected routes without authentication.

### Expected Result

Unauthenticated users should not gain access.

---

## Test 17 – Direct URL Access

### Objective

Navigate directly to protected URLs.

### Expected Result

Proper authorization checks should be enforced.

---

# Configuration Testing

## Test 18 – Invalid Client Configuration

### Objective

Temporarily introduce an incorrect client configuration.

### Observe

- Error messages
- Application behaviour
- Recovery steps

---

## Test 19 – Incorrect Redirect URI

### Objective

Modify the redirect URI configuration.

### Expected Result

Authentication should not complete successfully.

---

## Test 20 – Invalid Realm

### Objective

Attempt authentication using an incorrect realm configuration.

### Expected Result

Authentication should fail.

---

# User Experience Testing

Verify:

- Login page is accessible.
- Navigation works correctly.
- Logout is intuitive.
- Error messages are understandable.
- Protected pages respond appropriately.

Document any usability observations.

---

# Security Checklist

Verify the following where applicable.

- [ ] Client secrets are not committed to the repository.
- [ ] Sensitive configuration uses environment variables.
- [ ] Protected routes require authentication.
- [ ] Unauthorized users cannot access restricted content.
- [ ] Sessions behave as expected.
- [ ] Logout terminates access appropriately.

---

# Bug Report Template

Use the following format for any issues discovered.

## Title

Short description.

---

### Steps to Reproduce

1.
2.
3.

---

### Expected Behaviour

Describe the expected result.

---

### Actual Behaviour

Describe what happened.

---

### Possible Cause

(Optional)

---

### Status

- Open
- Investigating
- Resolved

---

# Final Validation Checklist

## Keycloak

- [ ] Running successfully
- [ ] Realm configured
- [ ] Client configured
- [ ] Users created
- [ ] Roles assigned

---

## Django

- [ ] Application starts successfully
- [ ] Login works
- [ ] Logout works
- [ ] Protected routes work
- [ ] User information displayed correctly

---

## Authentication

- [ ] Valid login
- [ ] Invalid login
- [ ] Unauthorized access blocked

---

## Authorization

- [ ] Administrator access verified
- [ ] Developer access verified
- [ ] Viewer access verified

---

## Documentation

- [ ] Test results documented
- [ ] Screenshots captured
- [ ] Issues documented
- [ ] README updated

---

# Deliverables

Submit the following as part of testing.

- Test Report
- Screenshots
- Bug Reports (if any)
- Summary of observations
- Lessons learned

---

# Completion Criteria

Testing is considered complete when:

- All mandatory test cases have been executed.
- Results have been documented.
- Any identified issues have been recorded.
- The application behaves as expected for the implemented features.
- The project is ready for demonstration.
