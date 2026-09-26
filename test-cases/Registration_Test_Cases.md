# Registration Test Cases – Batch 1

**Application:** [nopCommerce Demo Store](https://demo.nopcommerce.com/register)  
**Scope:** Customer registration, first 10 detailed cases  
**Basis:** [Requirement Analysis](../docs/Requirement_Analysis.md) and [Test Scenarios](../docs/Test_Scenarios.md)  
**Execution source:** Results below were supplied by the tester. They were not independently observed in this workspace. Two cases need clarification.  
**Environment to record on execution:** Date/time, OS, browser and version, viewport, and account data identifier.

## Test data

- Use a unique, controlled test email for each successful registration. Do not commit real passwords or personal data.
- `VALID_PASSWORD`: Choose a password that meets the current form rules; record the rule observed during execution.
- `VALID_USER`: Enter a first name, last name, unique email, password, and matching confirmation.
- For negative tests, start from a fresh registration page and enter `VALID_USER` except for the field under test.
- If a case submits successfully when validation was expected, record the observed outcome and investigate before reporting a defect; the demo's configuration may differ.

## Detailed cases

### TC-REG-001 — Register with valid required information
- **Scenario:** TS-REG-001 · **Priority:** High · **Type:** Positive
- **Precondition:** Registration page opens; a unique test email is available.
- **Steps:**
  1. Open `https://demo.nopcommerce.com/register`.
  2. Enter a valid first name, last name, unique email, password, and matching confirmation.
  3. Select or leave optional fields as desired and click **Register** once.
- **Expected:** Registration completes, a confirmation is displayed, and the newly registered customer can proceed to the store.
- **Actual:** User reported registration completed, confirmation appeared, and they could proceed as expected.
- **Status:** Pass (user-reported).

### TC-REG-002 — Submit all required fields empty
- **Scenario:** TS-REG-002 · **Priority:** High · **Type:** Negative
- **Precondition:** Fresh registration page.
- **Steps:**
  1. Leave First name, Last name, Email, Password, and Confirm password empty.
  2. Click **Register**.
- **Expected:** Registration is prevented and the form identifies the required fields. No account is created.
- **Actual:** User reported registration was prevented and required fields were identified as expected.
- **Status:** Pass (user-reported).

### TC-REG-003 — Omit First name
- **Scenario:** TS-REG-003 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill all required fields with valid data except First name.
  2. Click **Register**.
- **Expected:** Registration is prevented and First name is identified as required.
- **Actual:** User reported registration was prevented and First name was identified as required.
- **Status:** Pass (user-reported).

### TC-REG-004 — Omit Last name
- **Scenario:** TS-REG-004 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill all required fields with valid data except Last name.
  2. Click **Register**.
- **Expected:** Registration is prevented and Last name is identified as required.
- **Actual:** User reported registration was prevented and Last name was identified as required.
- **Status:** Pass (user-reported).

### TC-REG-005 — Omit Email
- **Scenario:** TS-REG-005 · **Priority:** High · **Type:** Negative
- **Precondition:** Fresh registration page.
- **Steps:**
  1. Fill all required fields with valid data except Email.
  2. Click **Register**.
- **Expected:** Registration is prevented and Email is identified as required.
- **Actual:** User reported registration was prevented and Email was identified as required.
- **Status:** Pass (user-reported).

### TC-REG-006 — Enter malformed Email
- **Scenario:** TS-REG-006 · **Priority:** High · **Type:** Negative
- **Test data:** `invalid-email`.
- **Precondition:** Fresh registration page.
- **Steps:**
  1. Fill all required fields with otherwise valid data and set Email to `invalid-email`.
  2. Click **Register**.
- **Expected:** Registration is prevented and an email-format validation message appears. Note whether validation comes from the browser or application.
- **Actual:** Needs clarification: the supplied results conflict. One entry says the invalid email was rejected as expected; another says registration completed without an email-format error. Browser versus application validation was not established.
- **Status:** Needs Review.

### TC-REG-007 — Reuse a registered Email
- **Scenario:** TS-REG-007 · **Priority:** High · **Type:** Negative
- **Precondition:** An account was registered in TC-REG-001; its test email is available.
- **Steps:**
  1. Open a fresh registration page.
  2. Fill all required fields using the existing email and an otherwise valid new registration.
  3. Click **Register**.
- **Expected:** A second account is not created using the same email, and a suitable error is displayed.
- **Actual:** User reported no second account was created and the message “The specified email already exists” appeared.
- **Status:** Pass (user-reported).

### TC-REG-008 — Enter passwords that do not match
- **Scenario:** TS-REG-009 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill the name and email fields with valid data.
  2. Enter a valid Password and a different valid Confirm password.
  3. Click **Register**.
- **Expected:** Registration is prevented and the mismatch is identified.
- **Actual:** User reported the message “The password and confirmation password do not match.” Registration outcome was described as expected.
- **Status:** Pass (user-reported).

### TC-REG-009 — Omit Password
- **Scenario:** TS-REG-010 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill all required fields with valid data except Password; enter a nonempty Confirm password.
  2. Click **Register**.
- **Expected:** Registration is prevented and the missing Password is identified.
- **Actual:** User reported the message “Password is required” when Password was empty.
- **Status:** Pass (user-reported).

### TC-REG-010 — Omit Confirm password
- **Scenario:** TS-REG-011 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill all required fields with valid data except Confirm password.
  2. Click **Register**.
- **Expected:** Registration is prevented and the missing or mismatched confirmation is identified.
- **Actual:** User reported “Password is required” when Confirm password was empty. It is unclear whether this message was associated with the Confirm password field or the Password field; verify field association and whether submission was prevented.
- **Status:** Needs Review.

## Execution record

The tester reported eight Pass outcomes and two cases needing review (TC-REG-006 and TC-REG-010). Preserve exact observed messages and add screenshots or a bug ID if a failure is confirmed. No defect is confirmed from the conflicting or ambiguous observations.

## Observed form fields

The [public registration page](https://demo.nopcommerce.com/register) currently lists Gender, First name, Last name, Email, Company name, Newsletter, Password, and Confirm password. Recheck the form on the execution date, since this is a shared demo.
