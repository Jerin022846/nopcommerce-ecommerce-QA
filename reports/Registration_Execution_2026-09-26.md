# Registration Execution Run – 2026-09-26

## Scope

- Cases: TC-REG-001 through TC-REG-010 in [Registration_Test_Cases.md](../test-cases/Registration_Test_Cases.md)
- Target: https://demo.nopcommerce.com/register
- Browser: Cloud Chrome session
- Outcome: **Blocked before test execution**

## Environment observation

The registration URL opened a Cloudflare page headed **“Performing security verification”**. It stated that the site was verifying the visitor was not a bot. One page reload returned to the same verification page. The registration form never became available in this browser.

This is an **environment/access blocker**, not a confirmed nopCommerce application defect. No registration data was submitted and no functional assertions were made.

| Case IDs | Run result | Reason |
|---|---|---|
| TC-REG-001 – TC-REG-010 | Blocked | Registration form inaccessible in the test browser |

**Execution totals:** 0 Pass · 0 Fail · 10 Blocked · 0 executed.

## Resume criteria

Run the cases using a normal browser session that can access the public demo, or a permitted local nopCommerce test installation. Record the execution date, browser/OS, test data identifiers, actual results, and screenshots for any failures. Do not infer a Pass or a product defect from this blocked run.
