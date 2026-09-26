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
