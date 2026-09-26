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

## M03 – Product Catalog

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-CAT-001 | Product Catalog | Verify the homepage category navigation opens a selected category | Positive | High |
| TS-CAT-002 | Product Catalog | Verify a customer can navigate from a parent category to a subcategory | Positive | High |
| TS-CAT-003 | Product Catalog | Verify a category page displays products belonging to that category | Functional | High |
| TS-CAT-004 | Product Catalog | Verify each product listing shows its name and relevant price or availability information | UI/Functional | High |
| TS-CAT-005 | Product Catalog | Verify selecting a product from a listing opens its matching product details page | Positive | High |
| TS-CAT-006 | Product Catalog | Verify changing the category sort order changes product ordering as selected | Functional | Medium |
| TS-CAT-007 | Product Catalog | Verify changing the page size updates the number of visible product results where supported | Functional | Medium |
| TS-CAT-008 | Product Catalog | Verify pagination navigates between product result pages where available | Functional | Medium |
| TS-CAT-009 | Product Catalog | Verify grid and list display options show the same products where supported | UI/Functional | Low |
| TS-CAT-010 | Product Catalog | Verify category filters narrow the displayed products where supported | Functional | Medium |
| TS-CAT-011 | Product Catalog | Verify a customer can return to a parent category or homepage using available navigation | Functional | Medium |
| TS-CAT-012 | Product Catalog | Verify a category with no matching products displays an appropriate empty result state where reproducible | Edge Case | Low |
| TS-CAT-013 | Product Catalog | Verify product images and links in a category listing lead to the matching product | UI/Functional | Medium |
| TS-CAT-014 | Product Catalog | Verify category navigation remains usable at mobile and desktop viewport sizes | Responsive | Medium |

> Confirm which categories offer filters, pagination, display modes, and empty states before turning conditional scenarios into detailed test cases.

## M04 – Product Search

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-SRCH-001 | Search | Verify a known product keyword returns relevant products | Positive | High |
| TS-SRCH-002 | Search | Verify a partial product name returns relevant matching products | Positive | High |
| TS-SRCH-003 | Search | Verify a keyword with no matching products shows a clear empty result message | Negative | Medium |
| TS-SRCH-004 | Search | Verify submitting an empty search term shows appropriate validation or search behavior | Negative | Medium |
| TS-SRCH-005 | Search | Verify search results link to the correct product details pages | Functional | High |
| TS-SRCH-006 | Search | Verify case variation in a keyword produces the expected search results | Edge Case | Medium |
| TS-SRCH-007 | Search | Verify leading and trailing spaces in a keyword are handled appropriately | Edge Case | Medium |
| TS-SRCH-008 | Search | Verify search with punctuation or special characters handles the input safely | Negative/Edge Case | Medium |
| TS-SRCH-009 | Search | Verify a long keyword is handled without breaking the search page | Boundary | Low |
| TS-SRCH-010 | Search | Verify advanced search can narrow results by category | Functional | Medium |
| TS-SRCH-011 | Search | Verify advanced search can include subcategories when the option is available | Functional | Medium |
| TS-SRCH-012 | Search | Verify advanced search can narrow results by manufacturer where applicable | Functional | Medium |
| TS-SRCH-013 | Search | Verify searching product descriptions changes matching results when enabled | Functional | Medium |
| TS-SRCH-014 | Search | Verify searching product tags changes matching results when enabled | Functional | Medium |
| TS-SRCH-015 | Search | Verify combining advanced search options produces results consistent with the selected criteria | Functional | Medium |
| TS-SRCH-016 | Search | Verify a customer can revise a keyword and search again from the results page | Functional | Medium |

> Choose reproducible products and search terms during test case design; catalog content on the shared demo may change.
