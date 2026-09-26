# BUG-REG-001 — Registration accepts malformed email

| Field | Value |
|---|---|
| Module | Registration |
| Linked test case | [TC-REG-006](../test-cases/Registration_Test_Cases.md#tc-reg-006--enter-malformed-email) |
| Severity | Major (provisional) |
| Priority | P2 – High (provisional) |
| Status | New – reported by manual tester; independent reproduction pending |
| Environment | nopCommerce public demo storefront; browser and OS not yet recorded |
| Evidence | Tester observation; screenshot or screen recording pending |

## Preconditions

Open a fresh registration page. Use otherwise valid required details and a unique test email value.

## Steps to reproduce

1. Go to https://demo.nopcommerce.com/register.
2. Complete First name, Last name, Password, and Confirm password with valid matching values.
3. Enter `invalid-email` in Email.
4. Click **Register** once.

## Expected result

Registration is prevented and the user receives an email-format validation message.

## Actual result

The tester reported that registration completed successfully with `invalid-email` and no email-format validation message appeared.

## Impact and follow-up

An account may be created with a malformed email address, which could interfere with email-based account functions. This impact is an inference and has not been separately tested. Reproduce in a controlled test environment, capture the browser/OS and form behavior, and attach evidence. Check whether the stored account email and subsequent login/recovery behavior are affected. Do not classify browser-side versus server-side validation until confirmed.
