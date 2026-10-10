# Execution log

Run: R01 | Executor: ChatGPT browser interaction | Date: 2026-09-12 UTC

TC-001 was executed. TC-002–TC-025 have not been attempted and await secure browser sign-in; this is not a product failure. Keep separate run records when the owner repeats these tests.

| Case | Status | Actual result / reason | Evidence |
| --- | --- | --- | --- |
| TC-001 | Pass | Swag Labs title, Username and Password inputs, Login button and demo guidance visible. Captured 05:27:19 UTC. | [Screenshot](../evidence/TC-001-login-page.jpg) |
| TC-002 | Not run | Not attempted; authenticated execution pending. | — |
| TC-003 | Not run | Not attempted; authenticated execution pending. | — |
| TC-004 | Not run | Not attempted; authenticated execution pending. | — |
| TC-005 | Not run | Not attempted; authenticated execution pending. | — |
| TC-006 | Not run | Not attempted; authenticated execution pending. | — |
| TC-007 | Not run | Not attempted; authenticated execution pending. | — |
| TC-008 | Not run | Not attempted; authenticated execution pending. | — |
| TC-009 | Not run | Not attempted; authenticated execution pending. | — |
| TC-010 | Not run | Not attempted; authenticated execution pending. | — |
| TC-011 | Not run | Not attempted; authenticated execution pending. | — |
| TC-012 | Not run | Not attempted; authenticated execution pending. | — |
| TC-013 | Not run | Not attempted; authenticated execution pending. | — |
| TC-014 | Not run | Not attempted; authenticated execution pending. | — |
| TC-015 | Not run | Not attempted; authenticated execution pending. | — |
| TC-016 | Not run | Not attempted; authenticated execution pending. | — |
| TC-017 | Not run | Not attempted; authenticated execution pending. | — |
| TC-018 | Not run | Not attempted; authenticated execution pending. | — |
| TC-019 | Not run | Not attempted; authenticated execution pending. | — |
| TC-020 | Not run | Not attempted; authenticated execution pending. | — |
| TC-021 | Not run | Not attempted; authenticated execution pending. | — |
| TC-022 | Not run | Not attempted; authenticated execution pending. | — |
| TC-023 | Not run | Not attempted; authenticated execution pending. | — |
| TC-024 | Not run | Not attempted; authenticated execution pending. | — |
| TC-025 | Not run | Not attempted; authenticated execution pending. | — |


## R02 — Manual testing by Thura Aung

Test date: 2026-09-12
Environment: Chrome on Windows
Account: standard_user

| Case | Status | Actual result | Evidence |
| --- | --- | --- | --- |
| TC-002 | Pass | Entered the standard demo credentials and clicked Login. The Products page opened and product cards were visible. | [Screenshot](../evidence/TC-002-R02-login-success.png) |
| TC-012 | Pass | Added one Sauce Labs Backpack. The cart displayed the correct product, quantity 1, price $29.99, and cart badge 1. | [Cart screenshot](../evidence/TC-012-R02-add-to-cart.png) |
| TC-021 | Pass | After entering valid checkout information and clicking Continue, Checkout: Overview opened with one Sauce Labs Backpack priced $29.99, matching the cart. | [Overview screenshot](../evidence/TC-021-R02-checkout-overview.png) |
| TC-024 | Pass | Completed the demo checkout and saw the order confirmation. Returned to the catalogue and opened the cart; no products remained. | [Order confirmation](../evidence/TC-024-R02-order-confirmation.png), [Empty cart](../evidence/TC-024-R02-empty-cart.png) |
| TC-003 | Pass | Login was rejected with an incorrect-credentials message; the login page remained visible. Error text appeared partly clipped in the screenshot; visual issue needs investigation. | [wrong-password](../evidence/TC-003-R02-wrong-password.png) |
| TC-004 | Pass | With both fields empty, clicking Login displayed “Username is required” and kept the user on the login page. | [empty-login](../evidence/TC-004-R02-empty-login.png) |
| TC-005 | Pass | With username empty and password entered, clicking Login displayed “Username is required.” | [missing-username](../evidence/TC-005-R02-missing-username.png) |
| TC-006 | Pass | With standard_user entered and password empty, clicking Login displayed “Password is required.” | [missing-password](../evidence/TC-006-R02-missing-password.png) |
| TC-007 | Pass | Login as locked_out_user was rejected with “Sorry, this user has been locked out.” | [locked-user](../evidence/TC-007-R02-locked-user.png) |

## R03 — Testing by Thura Aung

Date: 2026-10-10

| Case | Status | Actual result | Evidence |
| --- | --- | --- | --- |
| TC-008 | Pass | Backpack name, description and price matched between the catalogue and product details. Back to products returned to the Products page. | [Catalogue](../evidence/TC-008-R03-catalogue.png), [Details](../evidence/TC-008-R03-product-details.png) |
| TC-009 | Pass | Selected Price (low to high) and verified all product prices were ordered from smallest to largest. | [price-low-to-high](../evidence/TC-009-R03-price-low-to-high.png) |
| TC-010 | Pass | Selected Price (high to low) and verified all product prices were ordered from largest to smallest. | [price-high-to-low](../evidence/TC-010-R03-price-high-to-low.png) |
| TC-011 | Pass | Selected Name (A to Z) and verified all product names were in alphabetical order. | [name-a-to-z](../evidence/TC-011-R03-name-a-to-z.png) |
| TC-013 | Pass | Backpack and Bike Light each appeared once in the cart, with prices matching the catalogue. Cart badge showed 2. | [Screenshot](../evidence/TC-013-R03-two-products.png) |
| TC-014 | Pass | Removed the Backpack. Only the Bike Light remained, and the cart badge showed 1. | [Screenshot](../evidence/TC-014-R03-remove-one-product.png) |
| TC-015 | Pass | Removed the final product. No product rows remained and no positive item count was shown. | [Screenshot](../evidence/TC-015-R03-empty-cart.png) |
| TC-016 | Pass | After refreshing the cart page, the Backpack remained once with the same price. | [Before refresh](../evidence/TC-016-R03-before-refresh.png), [After refresh](../evidence/TC-016-R03-after-refresh.png) |
| TC-017 | Pass | Continue Shopping opened the Products page. Reopening the cart showed the Backpack still present once. | [Products page](../evidence/TC-017-R03-return-to-products.png), [Cart](../evidence/TC-017-R03-cart-preserved.png) |
| TC-018 | Pass | Leaving first name empty displayed first-name validation and prevented advancing from the checkout information page. | [Screenshot](../evidence/TC-018-R03-first-name-required.png) |
| TC-019 | Pass | Leaving last name empty displayed last-name validation and prevented advancing from the checkout information page. | [Screenshot](../evidence/TC-019-R03-last-name-required.png) |
| TC-020 | Pass | Leaving postal code empty displayed postal-code validation and prevented advancing from the checkout information page. | [Screenshot](../evidence/TC-020-R03-postal-code-required.png) |
| TC-022 | Pass | Backpack (1 × $29.99) and Bike Light (1 × $9.99) totalled $39.98, matching the subtotal. Adding displayed tax of $3.20 gave $43.18, matching the total. | [Screenshot](../evidence/TC-022-R03-overview-totals.png) |
| TC-023 | Pass | Cancel closed the checkout information page without order confirmation. The Backpack remained in the cart. | [Screenshot](../evidence/TC-023-R03-cancel-checkout.png) |
| TC-025 | Pass | Logout returned to the login page. Direct navigation to /inventory.html was blocked with a login-required error. Error text appeared partly clipped; visual observation remains open. | [After logout](../evidence/TC-025-R03-after-logout.png), [Access blocked](../evidence/TC-025-R03-protected-page-blocked.png) |