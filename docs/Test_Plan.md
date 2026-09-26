# Test Plan – nopCommerce E-Commerce QA Project

## 1. Introduction

This test plan defines the testing strategy, scope, objectives, resources,
test environment, execution approach, entry and exit criteria, defect
management process, and deliverables for the nopCommerce Demo Store QA project.

The project focuses primarily on validating customer-facing e-commerce
workflows through manual testing and automated regression testing.

---

## 2. Test Objectives

The objectives of testing are to:

- Verify that major customer-facing features work as expected.
- Validate critical end-to-end e-commerce workflows.
- Identify functional, UI, validation, and usability defects.
- Validate positive, negative, boundary, and edge-case scenarios.
- Verify application behavior across supported browsers and viewport sizes.
- Build automated regression coverage for stable and repetitive workflows.
- Maintain clear test evidence and defect documentation.
- Produce a final test execution summary.

---

## 3. Scope

### 3.1 Features In Scope

The following modules are included:

- User Registration
- Login and Logout
- Product Catalog
- Product Search
- Product Details
- Shopping Cart
- Wishlist
- Compare Products
- Checkout
- My Account
- UI and Responsive Behavior
- Cross-Browser Behavior
- Negative and Edge Cases

### 3.2 Out of Scope

The following are outside the initial scope:

- nopCommerce source-code testing
- Production database testing
- Real payment processing
- Real financial transactions
- Destructive security testing
- Server/infrastructure testing
- Admin panel testing during the initial phase

---

## 4. Test Strategy

### 4.1 Manual Testing

Manual testing will be used for:

- Exploratory testing
- UI validation
- Usability observations
- Negative testing
- Boundary-value testing
- New functionality
- Scenarios unsuitable for automation

### 4.2 Automation Testing

Stable and repetitive regression scenarios will be automated using:

- Python
- Selenium WebDriver
- pytest

Automation will initially focus on critical workflows such as:

- Registration
- Login
- Product search
- Product navigation
- Add to cart
- Cart modification
- Wishlist
- Checkout-related workflows

### 4.3 Regression Testing

Regression testing will be performed after significant changes or when
previously tested functionality may be affected.

Automated regression tests will be created for stable, high-value scenarios.

### 4.4 Smoke Testing

A small smoke suite will verify that critical application functionality is
available before detailed testing begins.

Example smoke checks:

- Homepage loads
- Registration page is accessible
- Login page is accessible
- Products can be viewed
- Search works
- Product can be added to cart
- Cart can be opened

---

## 5. Test Design Techniques

The project will use:

- Equivalence Partitioning
- Boundary Value Analysis
- Decision Table Testing where applicable
- State Transition Testing where applicable
- Error Guessing
- Exploratory Testing

---

## 6. Test Environment

### Application

nopCommerce Demo Store

### Initial Environment

- Browser: Google Chrome
- Additional Browsers: Firefox and Microsoft Edge
- Platform: Desktop Web
- Additional Testing: Mobile and tablet viewport sizes

### Automation Stack

- Python
- Selenium WebDriver
- pytest
- Git/GitHub

Additional reporting and CI/CD tools may be introduced during later phases.

---

## 7. Test Data Strategy

Test data will be created specifically for testing purposes.

Examples include:

- Valid customer information
- Invalid email addresses
- Existing email addresses
- Valid and invalid passwords
- Boundary-value inputs
- Product quantities
- Search keywords
- Checkout information

Because the public demo environment may reset periodically, tests should not
depend on permanent user or product data where avoidable.

---

## 8. Entry Criteria

Testing may begin when:

- The application is accessible.
- Major functionality required for testing is available.
- Testing scope has been identified.
- Test environment is available.
- Required test data can be created.
- Test scenarios/test cases for the relevant functionality are prepared.

---

## 9. Exit Criteria

Testing may be considered complete for the planned release/project phase when:

- Planned critical test cases have been executed.
- Critical workflows have been validated.
- No unresolved blocker defects remain within the tested scope.
- Critical defects have been documented and communicated.
- Regression testing has been completed for the planned scope.
- Test execution results have been documented.
- A test summary report has been prepared.

---

## 10. Defect Management

Each confirmed defect should contain:

- Defect ID
- Title
- Module
- Environment
- Preconditions
- Steps to Reproduce
- Expected Result
- Actual Result
- Severity
- Priority
- Status
- Evidence

### Severity Levels

**Blocker**
A defect that prevents testing or prevents a critical workflow from being used.

**Critical**
A major failure affecting critical functionality with no reasonable workaround.

**Major**
Important functionality is affected, but testing or usage can continue.

**Minor**
A limited functional or UI issue with relatively low impact.

**Trivial**
A cosmetic or very low-impact issue.

### Priority Levels

**P1 – Urgent**

Requires immediate attention.

**P2 – High**

Should be addressed as a high priority.

**P3 – Medium**

Should be addressed during normal development.

**P4 – Low**

Can be addressed when higher-priority work is complete.

Severity represents the impact of a defect, while priority represents how
urgently the defect should be addressed.

---

## 11. Test Case Status

Test execution will use the following statuses:

- Not Run
- Pass
- Fail
- Blocked
- Not Applicable

---

## 12. Defect Status

Where applicable, defects may use:

- New
- Open
- In Progress
- Fixed
- Retest
- Reopened
- Closed
- Rejected
- Duplicate

---

## 13. Risks and Mitigation

| Risk | Impact | Mitigation |
|---|---|---|
| Public demo data reset | Test data may disappear | Generate reusable test data |
| Shared environment | Results may be affected by other users | Avoid dependency on permanent data |
| UI changes | Automation locators may break | Use maintainable locator strategies |
| Demo downtime | Testing may be blocked | Resume execution when environment returns |
| Dynamic data | Assertions may become unstable | Avoid unnecessary hard-coded values |
| Browser differences | Behavior may vary | Perform cross-browser testing |

---

## 14. Test Deliverables

The project will produce:

1. Requirement Analysis
2. Test Plan
3. Test Scenarios
4. Test Cases
5. Test Execution Results
6. Defect Reports
7. Requirement Traceability Matrix
8. Automation Test Suite
9. Automation Reports
10. Test Evidence
11. CI/CD Configuration
12. Final Test Summary Report

---

## 15. Automation Selection Criteria

A test is a good automation candidate when it is:

- Repetitive
- Stable
- Frequently executed
- Important for regression testing
- Time-consuming when executed manually
- Based on predictable expected results

Exploratory, rapidly changing, and highly subjective UI/usability checks will
generally remain manual.

---

## 16. Completion Criteria

The project will be considered complete when the planned QA documentation,
manual test coverage, defect documentation, automation coverage, execution
evidence, and final QA summary have been added to the repository.
