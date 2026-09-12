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