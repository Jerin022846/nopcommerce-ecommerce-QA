# Test Scenarios – nopCommerce Demo Store

## Purpose

This document contains high-level test scenarios for the customer-facing nopCommerce Demo Store. Scenarios describe what to verify; detailed steps, expected results, and execution status belong in the test cases and execution records.

## M01 – User Registration

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-REG-001 | Registration | Verify registration with valid customer information | Positive | High |
| TS-REG-002 | Registration | Verify validation when all required fields are empty | Negative | High |
| TS-REG-003 | Registration | Verify validation when First Name is empty | Negative | High |
| TS-REG-004 | Registration | Verify validation when Last Name is empty | Negative | High |
| TS-REG-005 | Registration | Verify validation when Email is empty | Negative | High |
| TS-REG-006 | Registration | Verify registration with an invalid email format | Negative | High |
| TS-REG-007 | Registration | Verify registration with an already registered email | Negative | High |
| TS-REG-008 | Registration | Verify password validation against the observed password rules | Negative/Boundary | High |
| TS-REG-009 | Registration | Verify validation when Password and Confirm Password do not match | Negative | High |
| TS-REG-010 | Registration | Verify validation when Password is empty | Negative | High |
| TS-REG-011 | Registration | Verify validation when Confirm Password is empty | Negative | High |
| TS-REG-012 | Registration | Verify registration with a Gender selection | Positive | Medium |
| TS-REG-013 | Registration | Verify registration without selecting Gender | Positive | Medium |
| TS-REG-014 | Registration | Verify Date of Birth field behavior with valid values | Positive | Medium |
| TS-REG-015 | Registration | Verify registration without Date of Birth | Positive | Low |
| TS-REG-016 | Registration | Verify Company field accepts valid input | Positive | Low |
| TS-REG-017 | Registration | Verify registration without Company information | Positive | Low |
| TS-REG-018 | Registration | Verify newsletter subscription selection during registration | Functional | Medium |
| TS-REG-019 | Registration | Verify entered Password is masked | UI/Security | Medium |
| TS-REG-020 | Registration | Verify entered Confirm Password is masked | UI/Security | Medium |
| TS-REG-021 | Registration | Verify leading and trailing whitespace handling in applicable fields | Edge Case | Medium |
| TS-REG-022 | Registration | Verify behavior when Register is clicked repeatedly | Edge Case | Medium |
| TS-REG-023 | Registration | Verify successful registration confirmation is displayed | Positive | High |
| TS-REG-024 | Registration | Verify navigation from registration confirmation to the store | Functional | Medium |

> These are proposed scenarios, not executed test results. Confirm field availability and validation rules against the demo before writing detailed expected results.

## M02 – Login and Logout

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-AUTH-001 | Login/Logout | Verify login with a registered email and correct password | Positive | High |
| TS-AUTH-002 | Login/Logout | Verify login with an unregistered email | Negative | High |
| TS-AUTH-003 | Login/Logout | Verify login with a registered email and incorrect password | Negative | High |
| TS-AUTH-004 | Login/Logout | Verify validation when email and password are both empty | Negative | High |
| TS-AUTH-005 | Login/Logout | Verify validation when email is empty | Negative | High |
| TS-AUTH-006 | Login/Logout | Verify validation when password is empty | Negative | High |
| TS-AUTH-007 | Login/Logout | Verify validation for a malformed email address | Negative | Medium |
| TS-AUTH-008 | Login/Logout | Verify password characters are masked on the login form | UI/Security | Medium |
| TS-AUTH-009 | Login/Logout | Verify the Remember Me option preserves login as configured | Functional | Medium |
| TS-AUTH-010 | Login/Logout | Verify the login page provides a password recovery path | Functional | Medium |
| TS-AUTH-011 | Login/Logout | Verify a user can request password recovery with a registered email | Functional | Medium |
| TS-AUTH-012 | Login/Logout | Verify password recovery behavior with an unregistered or invalid email | Negative | Medium |
| TS-AUTH-013 | Login/Logout | Verify a logged-in customer can log out | Positive | High |
| TS-AUTH-014 | Login/Logout | Verify account-only pages are protected after logout | Security/Functional | High |
| TS-AUTH-015 | Login/Logout | Verify browser Back navigation after logout does not restore an authenticated session | Security/Edge Case | High |
| TS-AUTH-016 | Login/Logout | Verify a customer can log in again after logging out | Positive | Medium |

> Verify the precise Remember Me and password recovery behavior against the public demo before defining detailed expected results.
