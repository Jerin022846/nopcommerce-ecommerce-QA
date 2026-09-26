# Registration Test Cases – Batch 1

**Application:** [nopCommerce Demo Store](https://demo.nopcommerce.com/register)  
**Scope:** Customer registration, first 10 detailed cases  
**Basis:** [Requirement Analysis](../docs/Requirement_Analysis.md) and [Test Scenarios](../docs/Test_Scenarios.md)  
**Design status:** Ready for manual execution; no case has been executed.  
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
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-002 — Submit all required fields empty
- **Scenario:** TS-REG-002 · **Priority:** High · **Type:** Negative
- **Precondition:** Fresh registration page.
- **Steps:**
  1. Leave First name, Last name, Email, Password, and Confirm password empty.
  2. Click **Register**.
- **Expected:** Registration is prevented and the form identifies the required fields. No account is created.
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-003 — Omit First name
- **Scenario:** TS-REG-003 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill all required fields with valid data except First name.
  2. Click **Register**.
- **Expected:** Registration is prevented and First name is identified as required.
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-004 — Omit Last name
- **Scenario:** TS-REG-004 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill all required fields with valid data except Last name.
  2. Click **Register**.
- **Expected:** Registration is prevented and Last name is identified as required.
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-005 — Omit Email
- **Scenario:** TS-REG-005 · **Priority:** High · **Type:** Negative
- **Precondition:** Fresh registration page.
- **Steps:**
  1. Fill all required fields with valid data except Email.
  2. Click **Register**.
- **Expected:** Registration is prevented and Email is identified as required.
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-006 — Enter malformed Email
- **Scenario:** TS-REG-006 · **Priority:** High · **Type:** Negative
- **Test data:** `invalid-email`.
- **Precondition:** Fresh registration page.
- **Steps:**
  1. Fill all required fields with otherwise valid data and set Email to `invalid-email`.
  2. Click **Register**.
- **Expected:** Registration is prevented and an email-format validation message appears. Note whether validation comes from the browser or application.
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-007 — Reuse a registered Email
- **Scenario:** TS-REG-007 · **Priority:** High · **Type:** Negative
- **Precondition:** An account was registered in TC-REG-001; its test email is available.
- **Steps:**
  1. Open a fresh registration page.
  2. Fill all required fields using the existing email and an otherwise valid new registration.
  3. Click **Register**.
- **Expected:** A second account is not created using the same email, and a suitable error is displayed.
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-008 — Enter passwords that do not match
- **Scenario:** TS-REG-009 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill the name and email fields with valid data.
  2. Enter a valid Password and a different valid Confirm password.
  3. Click **Register**.
- **Expected:** Registration is prevented and the mismatch is identified.
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-009 — Omit Password
- **Scenario:** TS-REG-010 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill all required fields with valid data except Password; enter a nonempty Confirm password.
  2. Click **Register**.
- **Expected:** Registration is prevented and the missing Password is identified.
- **Actual:** Pending execution.
- **Status:** Not Run.

### TC-REG-010 — Omit Confirm password
- **Scenario:** TS-REG-011 · **Priority:** High · **Type:** Negative
- **Precondition:** Unique valid test email is available.
- **Steps:**
  1. Fill all required fields with valid data except Confirm password.
  2. Click **Register**.
- **Expected:** Registration is prevented and the missing or mismatched confirmation is identified.
- **Actual:** Pending execution.
- **Status:** Not Run.

## Execution record

When running a case, replace **Pending execution** with the observed behavior; change status to Pass, Fail, Blocked, or Not Applicable. Attach dated screenshots or a bug ID for failures. Record the exact validation wording and whether browser validation blocked submission. Never mark a case Pass solely because it was drafted.

## Observed form fields

The [public registration page](https://demo.nopcommerce.com/register) currently lists Gender, First name, Last name, Email, Company name, Newsletter, Password, and Confirm password. Recheck the form on the execution date, since this is a shared demo.
