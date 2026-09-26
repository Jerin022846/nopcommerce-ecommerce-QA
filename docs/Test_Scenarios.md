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

## M05 – Product Details

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-PDP-001 | Product Details | Verify the product page shows the selected product name and description | Functional | High |
| TS-PDP-002 | Product Details | Verify the displayed product price is consistent with its listing, accounting for selected options | Functional | High |
| TS-PDP-003 | Product Details | Verify the main product image and available additional images can be viewed | UI/Functional | Medium |
| TS-PDP-004 | Product Details | Verify availability and stock information is displayed accurately when available | Functional | Medium |
| TS-PDP-005 | Product Details | Verify required product options must be selected before adding an applicable product to the cart | Negative | High |
| TS-PDP-006 | Product Details | Verify selecting product options updates the price or details where applicable | Functional | High |
| TS-PDP-007 | Product Details | Verify a configurable product with valid options can be added to the cart | Positive | High |
| TS-PDP-008 | Product Details | Verify a simple product can be added to the cart from its details page | Positive | High |
| TS-PDP-009 | Product Details | Verify the quantity field rejects zero, negative, and nonnumeric values where editable | Negative/Boundary | High |
| TS-PDP-010 | Product Details | Verify adding multiple units reflects the selected quantity in the cart | Functional | High |
| TS-PDP-011 | Product Details | Verify adding a product to the wishlist from the details page where supported | Functional | Medium |
| TS-PDP-012 | Product Details | Verify adding a product to the compare list from the details page where supported | Functional | Medium |
| TS-PDP-013 | Product Details | Verify available product reviews and rating information are visible | UI/Functional | Low |
| TS-PDP-014 | Product Details | Verify product review submission behavior for eligible and ineligible customers | Positive/Negative | Medium |
| TS-PDP-015 | Product Details | Verify product information and purchase controls remain usable on mobile and desktop viewports | Responsive | Medium |

> Select representative simple and configurable products during test case design. Some controls depend on product configuration or store settings.

## M06 – Shopping Cart

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-CART-001 | Shopping Cart | Verify adding a simple product updates the cart contents and item count | Positive | High |
| TS-CART-002 | Shopping Cart | Verify a configured product retains its selected options in the cart | Functional | High |
| TS-CART-003 | Shopping Cart | Verify changing an item quantity updates the line total and cart subtotal | Functional | High |
| TS-CART-004 | Shopping Cart | Verify the cart rejects or handles zero, negative, nonnumeric, and excessive quantities appropriately | Negative/Boundary | High |
| TS-CART-005 | Shopping Cart | Verify removing one product leaves other cart items unchanged | Functional | High |
| TS-CART-006 | Shopping Cart | Verify removing the last product displays the empty-cart state | Functional | Medium |
| TS-CART-007 | Shopping Cart | Verify adding the same product again produces the expected line item and quantity behavior | Edge Case | Medium |
| TS-CART-008 | Shopping Cart | Verify unit prices, discounts, line totals, and subtotal are calculated consistently | Functional | High |
| TS-CART-009 | Shopping Cart | Verify a customer can continue shopping and return to the cart | Functional | Medium |
| TS-CART-010 | Shopping Cart | Verify the cart persists during normal navigation within the current session | Functional | Medium |
| TS-CART-011 | Shopping Cart | Verify checkout is available when the cart contains eligible items | Positive | High |
| TS-CART-012 | Shopping Cart | Verify checkout is unavailable or handled appropriately for an empty cart | Negative | High |
| TS-CART-013 | Shopping Cart | Verify discount code acceptance and rejection where an applicable code is available | Positive/Negative | Low |
| TS-CART-014 | Shopping Cart | Verify shipping estimate inputs and results where the feature is available | Functional | Low |

## M07 – Wishlist

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-WISH-001 | Wishlist | Verify a customer can add an eligible product to the wishlist | Positive | High |
| TS-WISH-002 | Wishlist | Verify a configurable product requires valid selections before it is added to the wishlist where applicable | Negative | Medium |
| TS-WISH-003 | Wishlist | Verify the wishlist shows the correct product, options, and quantity | Functional | High |
| TS-WISH-004 | Wishlist | Verify updating an item quantity works when the wishlist permits it | Functional | Medium |
| TS-WISH-005 | Wishlist | Verify a customer can remove one product from the wishlist | Functional | High |
| TS-WISH-006 | Wishlist | Verify removing the last item displays the empty-wishlist state | Functional | Medium |
| TS-WISH-007 | Wishlist | Verify moving an eligible wishlist item to the cart retains the correct product and options | Functional | High |
| TS-WISH-008 | Wishlist | Verify wishlist behavior for guest and signed-in customers according to observed store behavior | Functional | Medium |
| TS-WISH-009 | Wishlist | Verify the wishlist link or item count reflects changes where displayed | UI/Functional | Low |

> Execute feature-dependent scenarios only where the current demo configuration supports them; record Not Applicable otherwise.

## M08 – Compare Products

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-CMP-001 | Compare Products | Verify adding a product to compare makes it appear on the comparison page | Positive | High |
| TS-CMP-002 | Compare Products | Verify adding two distinct products shows their information side by side | Functional | High |
| TS-CMP-003 | Compare Products | Verify compared product names, images, prices, and listed attributes correspond to the selected products | Functional | High |
| TS-CMP-004 | Compare Products | Verify adding the same product twice does not create an unexpected duplicate | Edge Case | Medium |
| TS-CMP-005 | Compare Products | Verify removing one product preserves the remaining compared products | Functional | Medium |
| TS-CMP-006 | Compare Products | Verify clearing the comparison list displays the empty state | Functional | Medium |
| TS-CMP-007 | Compare Products | Verify links from comparison results open the corresponding product pages | Functional | Medium |
| TS-CMP-008 | Compare Products | Verify comparison behavior when the supported product limit is reached, if a limit exists | Boundary | Low |

> Execute feature-dependent scenarios only where the current demo configuration supports them; record Not Applicable otherwise.

## M09 – Checkout

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-CHK-001 | Checkout | Verify a customer can start checkout with an eligible cart item | Positive | High |
| TS-CHK-002 | Checkout | Verify a registered customer can complete a demo checkout with valid information | Positive | High |
| TS-CHK-003 | Checkout | Verify guest checkout works where permitted by store configuration | Positive | High |
| TS-CHK-004 | Checkout | Verify required billing address fields display validation for missing or invalid values | Negative | High |
| TS-CHK-005 | Checkout | Verify an existing or new billing address can be selected when supported | Functional | Medium |
| TS-CHK-006 | Checkout | Verify shipping address selection or entry works for a physical product | Functional | High |
| TS-CHK-007 | Checkout | Verify shipping method selection updates the checkout summary where applicable | Functional | High |
| TS-CHK-008 | Checkout | Verify an available demo payment method can be selected | Functional | High |
| TS-CHK-009 | Checkout | Verify billing and shipping steps adapt appropriately for a nonshipped product where applicable | Functional | Medium |
| TS-CHK-010 | Checkout | Verify checkout totals reflect item price, quantity, shipping, discounts, and tax displayed by the demo | Functional | High |
| TS-CHK-011 | Checkout | Verify the order review displays the selected products and customer information before confirmation | Functional | High |
| TS-CHK-012 | Checkout | Verify the terms acceptance requirement is enforced where displayed | Negative | High |
| TS-CHK-013 | Checkout | Verify final confirmation produces an order confirmation or order number | Positive | High |
| TS-CHK-014 | Checkout | Verify repeated confirmation actions do not create unintended duplicate orders | Edge Case | High |
| TS-CHK-015 | Checkout | Verify the cart state after a completed order matches observed store behavior | Functional | Medium |
| TS-CHK-016 | Checkout | Verify leaving checkout and returning preserves or resets entered information according to observed behavior | Edge Case | Medium |

> Execute feature-dependent scenarios only where the current demo configuration supports them; record Not Applicable otherwise.

## M10 – My Account

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-ACC-001 | My Account | Verify a signed-in customer can open My Account | Positive | High |
| TS-ACC-002 | My Account | Verify a guest is redirected or denied access to account-only pages | Security/Functional | High |
| TS-ACC-003 | My Account | Verify customer information displays the current account details | Functional | High |
| TS-ACC-004 | My Account | Verify valid customer information changes persist after saving | Functional | High |
| TS-ACC-005 | My Account | Verify invalid or missing required customer information is rejected appropriately | Negative | Medium |
| TS-ACC-006 | My Account | Verify the address book allows an address to be added with valid details | Positive | Medium |
| TS-ACC-007 | My Account | Verify address editing and removal update the address book correctly | Functional | Medium |
| TS-ACC-008 | My Account | Verify address forms validate required fields | Negative | Medium |
| TS-ACC-009 | My Account | Verify order history displays a completed demo order for the same account | Functional | High |
| TS-ACC-010 | My Account | Verify order details correspond to the selected order | Functional | Medium |
| TS-ACC-011 | My Account | Verify password change accepts correct current credentials and matching new passwords | Positive | High |
| TS-ACC-012 | My Account | Verify incorrect current password or mismatched new passwords are rejected | Negative | High |
| TS-ACC-013 | My Account | Verify account-only information is unavailable after logout | Security/Functional | High |

> Execute feature-dependent scenarios only where the current demo configuration supports them; record Not Applicable otherwise.

## M11 – UI and Responsive

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-UI-001 | UI and Responsive | Verify header navigation, cart, and account controls remain usable on desktop | UI | Medium |
| TS-UI-002 | UI and Responsive | Verify header navigation and main controls remain usable at a mobile viewport | Responsive | High |
| TS-UI-003 | UI and Responsive | Verify forms and validation messages remain readable at mobile and tablet viewport sizes | Responsive | Medium |
| TS-UI-004 | UI and Responsive | Verify product cards, images, and prices do not overlap or clip at common viewport sizes | Responsive | Medium |
| TS-UI-005 | UI and Responsive | Verify cart and checkout controls are usable without horizontal scrolling at mobile widths where supported | Responsive | High |
| TS-UI-006 | UI and Responsive | Verify focus is visible when navigating core controls by keyboard | Accessibility/UI | Medium |
| TS-UI-007 | UI and Responsive | Verify input labels and error messages identify the associated field | Accessibility/UI | Medium |
| TS-UI-008 | UI and Responsive | Verify loading, empty, and error states are understandable where encountered | UI | Medium |

## M12 – Cross-Browser Compatibility

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-COMPAT-001 | Cross-Browser | Verify homepage and category navigation work in supported Chrome, Firefox, and Edge versions | Compatibility | Medium |
| TS-COMPAT-002 | Cross-Browser | Verify registration and login forms behave consistently across target browsers | Compatibility | High |
| TS-COMPAT-003 | Cross-Browser | Verify product search and product details work consistently across target browsers | Compatibility | Medium |
| TS-COMPAT-004 | Cross-Browser | Verify add-to-cart and quantity update work consistently across target browsers | Compatibility | High |
| TS-COMPAT-005 | Cross-Browser | Verify checkout forms and confirmation work consistently across target browsers | Compatibility | High |
| TS-COMPAT-006 | Cross-Browser | Verify responsive navigation works in the browsers and viewport sizes actually tested | Compatibility/Responsive | Medium |

## M13 – Negative and Edge Cases

| Scenario ID | Module | Test Scenario | Type | Priority |
|---|---|---|---|---|
| TS-EDGE-001 | Negative and Edge Cases | Verify unexpected navigation during a multi-step checkout does not place an unintended order | Edge Case | High |
| TS-EDGE-002 | Negative and Edge Cases | Verify refreshing cart and checkout pages does not duplicate an action unexpectedly | Edge Case | High |
| TS-EDGE-003 | Negative and Edge Cases | Verify invalid quantity and required product options are handled without corrupting cart totals | Negative | High |
| TS-EDGE-004 | Negative and Edge Cases | Verify opening an invalid or unavailable product link shows an appropriate response | Negative | Medium |
| TS-EDGE-005 | Negative and Edge Cases | Verify rapid repeated add-to-cart actions have predictable quantities and feedback | Edge Case | Medium |
| TS-EDGE-006 | Negative and Edge Cases | Verify submitting forms with long or unusual text produces controlled validation and readable messages | Negative/Boundary | Medium |
| TS-EDGE-007 | Negative and Edge Cases | Verify session expiration during an account-only journey returns the customer to an appropriate sign-in flow | Edge Case | Medium |
| TS-EDGE-008 | Negative and Edge Cases | Verify a customer cannot access another customer's account or order by changing a visible URL identifier, using only their own demo accounts | Security/Functional | High |

## Execution note

These are planned scenarios, not test execution results or confirmed defects. During test case design, verify current controls and store settings, select reproducible test data, and record the browser and date used for execution.
