# Evidence index

Screenshot evidence for the [SauceDemo / Swag Labs](https://www.saucedemo.com/) manual testing project by Thura Aung.

Read the screenshots alongside the [execution log](../test-cases/execution-log.md), which records the actions performed and observed results. A screenshot alone does not demonstrate every step of a test.

This index lists 30 test-case screenshots and 1 follow-up screenshot covering 25 unique test cases and the OBS-001 visual observation across R01, R02 and R03.

## R01 — Initial check by ChatGPT

| Case | Evidence | Visible result |
| --- | --- | --- |
| TC-001 | [Login page](TC-001-login-page.jpg) | Public login controls and demo-account guidance |

Captured by ChatGPT in remote Chrome on 2026-09-12 at 05:27:19 UTC. Original dimensions: 1363 × 936. This screenshot documents the public login page, not successful authentication.

## R02 — Manual testing by Thura Aung

Test date recorded in the execution log: 2026-09-12. Environment: Chrome on Windows. Accounts included standard_user and locked_out_user, with invalid or empty inputs for negative login tests. Exact screenshot capture times are not recorded in this index.

| Case | Evidence | Result documented |
| --- | --- | --- |
| TC-002 | [Successful login](TC-002-R02-login-success.png) | Products page after login |
| TC-003 | [Wrong password](TC-003-R02-wrong-password.png) | Incorrect credentials rejected |
| TC-004 | [Empty login](TC-004-R02-empty-login.png) | Required-field validation with both fields empty |
| TC-005 | [Missing username](TC-005-R02-missing-username.png) | Username-required validation |
| TC-006 | [Missing password](TC-006-R02-missing-password.png) | Password-required validation |
| TC-007 | [Locked user](TC-007-R02-locked-user.png) | Locked-account rejection |
| TC-012 | [Add to cart](TC-012-R02-add-to-cart.png) | One Backpack, quantity 1, price $29.99 and badge 1 |
| TC-021 | [Checkout overview](TC-021-R02-checkout-overview.png) | Overview with the selected Backpack |
| TC-024 | [Order confirmation](TC-024-R02-order-confirmation.png), [Empty cart](TC-024-R02-empty-cart.png) | Demo order confirmation and cart after completion |

## R03 — Manual testing by Thura Aung

Execution date: 2026-10-10, Asia/Bangkok. Exact screenshot capture times are not recorded in this index.

| Case | Evidence | Result documented |
| --- | --- | --- |
| TC-008 | [Catalogue](TC-008-R03-catalogue.png), [Product details](TC-008-R03-product-details.png) | Matching Backpack name, description and price |
| TC-009 | [Price low to high](TC-009-R03-price-low-to-high.png) | Ascending price order |
| TC-010 | [Price high to low](TC-010-R03-price-high-to-low.png) | Descending price order |
| TC-011 | [Name A to Z](TC-011-R03-name-a-to-z.png) | Alphabetical product order |
| TC-013 | [Two products](TC-013-R03-two-products.png) | Two selected products, their prices and badge count |
| TC-014 | [Remove one product](TC-014-R03-remove-one-product.png) | Bike Light remaining after Backpack removal |
| TC-015 | [Empty cart](TC-015-R03-empty-cart.png) | No product rows after final removal |
| TC-016 | [Before refresh](TC-016-R03-before-refresh.png), [After refresh](TC-016-R03-after-refresh.png) | Cart contents before and after refresh |
| TC-017 | [Products page](TC-017-R03-return-to-products.png), [Preserved cart](TC-017-R03-cart-preserved.png) | Catalogue navigation and retained cart item |
| TC-018 | [First name required](TC-018-R03-first-name-required.png) | Validation with first name empty |
| TC-019 | [Last name required](TC-019-R03-last-name-required.png) | Validation with last name empty |
| TC-020 | [Postal code required](TC-020-R03-postal-code-required.png) | Validation with postal code empty |
| TC-022 | [Overview and totals](TC-022-R03-overview-totals.png) | Both items and quantities, $39.98 subtotal, $3.20 displayed tax and $43.18 total |
| TC-023 | [Cancel checkout](TC-023-R03-cancel-checkout.png) | Cart after cancelling checkout |
| TC-025 | [After logout](TC-025-R03-after-logout.png), [Access blocked](TC-025-R03-protected-page-blocked.png) | Login page and rejection of direct catalogue access |

## Open visual observation

Some login error text appears partly clipped in the TC-003 and TC-025 evidence. The recorded login rejection and protected-page blocking checks passed; the visual behaviour remains an open observation pending investigation, not a confirmed defect.

See the [test summary](../docs/test-summary.md) for the follow-up and limitations.

## Evidence conventions

- Preserve earlier screenshots and run records.
- Use filenames such as `TC-NNN-RNN-short-description.png`; retain the original `.jpg` extension for TC-001.
- Keep filenames and links identical, including letter case and file extensions.
- Record actions and actual outcomes in the execution log; do not infer unobserved steps from screenshots alone.
- Keep original screenshots as evidence. Store any annotated copies separately.
- Credentials shown for the practice application are public demo credentials, not personal account credentials.

## Follow-up evidence — OBS-001

[Login error screenshot](OBS-001-login-error-100-percent.png) — error text remained partly clipped in the follow-up capture.

[Observation report](../bug-reports/OBS-001-login-error-clipping.md)