# Detailed test cases

Version 0.1. Expected results refer to the assumptions in [the test plan](../docs/test-plan.md). Record outcomes separately in [the execution log](execution-log.md). Test steps for authenticated pages are drafts until the current UI is inspected.

## TC-001 — Login page loads

- Priority: Medium
- Technique: Smoke / UI
- Basis: OBS-01
- Preconditions: Signed out.
- Data: None

**Steps:** Open https://www.saucedemo.com/. Inspect the page.

**Expected result:** Swag Labs title, Username and Password inputs, Login button and published demo-account guidance are visible.

## TC-002 — Standard user can log in

- Priority: High
- Technique: Positive
- Basis: A1
- Preconditions: Signed out.
- Data: standard_user; published demo password

**Steps:** Enter standard_user and the published demo password. Select Login.

**Expected result:** Product catalogue opens and products are visible.

## TC-003 — Wrong password is rejected

- Priority: High
- Technique: Negative
- Basis: A1
- Preconditions: Signed out; fresh login page.
- Data: standard_user; wrong_demo_password

**Steps:** Enter standard_user with the wrong password. Select Login.

**Expected result:** Login is rejected with a useful error; catalogue does not open.

## TC-004 — Both login fields empty

- Priority: Medium
- Technique: Negative
- Basis: A1
- Preconditions: Signed out; clear both fields.
- Data: Empty username; empty password

**Steps:** Leave both fields empty. Select Login.

**Expected result:** Validation appears and user remains on login page.

## TC-005 — Username missing

- Priority: Medium
- Technique: Negative
- Basis: A1
- Preconditions: Signed out; username empty.
- Data: Empty username; published demo password

**Steps:** Enter only the published demo password. Select Login.

**Expected result:** Username validation appears; catalogue does not open.

## TC-006 — Password missing

- Priority: Medium
- Technique: Negative
- Basis: A1
- Preconditions: Signed out; password empty.
- Data: standard_user; empty password

**Steps:** Enter standard_user only. Select Login.

**Expected result:** Password validation appears; catalogue does not open.

## TC-007 — Locked user is denied access

- Priority: High
- Technique: Negative
- Basis: A1
- Preconditions: Signed out.
- Data: locked_out_user; published demo password

**Steps:** Enter locked_out_user and published demo password. Select Login.

**Expected result:** Account is denied access with an explanation that it is locked.

## TC-008 — Product details agree with catalogue

- Priority: Medium
- Technique: Consistency
- Basis: A2
- Preconditions: Standard user logged in; catalogue visible.
- Data: Record selected product during execution

**Steps:** Choose one product and record its name, description and price. Open its details. Compare the details with the recorded values. Return to catalogue.

**Expected result:** Name, description and price agree; navigation returns to catalogue.

## TC-009 — Sort prices low to high

- Priority: Medium
- Technique: Ordering
- Basis: A2
- Preconditions: Standard user logged in; catalogue visible.
- Data: All displayed prices

**Steps:** Choose ascending price sort. Record every displayed price in order. Compare each price with the next.

**Expected result:** Every price is less than or equal to the following price.

## TC-010 — Sort prices high to low

- Priority: Medium
- Technique: Ordering
- Basis: A2
- Preconditions: Standard user logged in; catalogue visible.
- Data: All displayed prices

**Steps:** Choose descending price sort. Record every displayed price in order. Compare each price with the next.

**Expected result:** Every price is greater than or equal to the following price.

## TC-011 — Sort names A to Z

- Priority: Low
- Technique: Ordering
- Basis: A2
- Preconditions: Standard user logged in; catalogue visible.
- Data: All displayed product names

**Steps:** Choose ascending name sort. Record the displayed names and compare their order alphabetically.

**Expected result:** Product names appear in ascending alphabetical order.

## TC-012 — Add one product

- Priority: High
- Technique: Positive
- Basis: A3
- Preconditions: Standard user logged in; cart empty.
- Data: Product A chosen during execution

**Steps:** Record one product name and price. Add it to the cart. Open the cart.

**Expected result:** Cart contains that product once with matching name and price; cart badge shows 1.

## TC-013 — Add two different products

- Priority: High
- Technique: Positive
- Basis: A3
- Preconditions: Standard user logged in; cart empty.
- Data: Products A and B chosen during execution

**Steps:** Record names and prices of two different products. Add both. Open the cart.

**Expected result:** Both selected products appear once; badge shows 2 and prices match the catalogue.

## TC-014 — Remove one of two products

- Priority: High
- Technique: State transition
- Basis: A3
- Preconditions: Standard user logged in; cart contains A and B exactly once.
- Data: A and B recorded in setup

**Steps:** Open cart. Remove product A. Inspect remaining items and badge.

**Expected result:** A is absent, B remains and badge shows 1.

## TC-015 — Remove the final product

- Priority: Medium
- Technique: Boundary
- Basis: A3
- Preconditions: Standard user logged in; cart contains A only.
- Data: Product A

**Steps:** Open cart. Remove A. Inspect cart and badge.

**Expected result:** No product rows remain; badge is absent or shows 0.

## TC-016 — Cart survives a page refresh

- Priority: Medium
- Technique: State persistence
- Basis: A3
- Preconditions: Standard user logged in; A in cart.
- Data: Product A

**Steps:** Open cart and record A. Refresh the page. Inspect cart.

**Expected result:** A remains once with the same price after refresh.

## TC-017 — Continue shopping preserves the cart

- Priority: Medium
- Technique: Navigation
- Basis: A3
- Preconditions: Standard user logged in; A in cart.
- Data: Product A

**Steps:** Open cart. Choose Continue Shopping. Confirm catalogue opens. Reopen cart.

**Expected result:** Catalogue is reachable and A remains once in cart.

## TC-018 — Checkout first name required

- Priority: High
- Technique: Negative
- Basis: A4
- Preconditions: Standard user logged in; A in cart; checkout information page open.
- Data: First name empty; Tester; 10110

**Steps:** Leave first name empty. Enter last name Tester and postal code 10110. Continue.

**Expected result:** Cannot advance; first-name validation is visible.

## TC-019 — Checkout last name required

- Priority: High
- Technique: Negative
- Basis: A4
- Preconditions: Standard user logged in; A in cart; checkout information page open.
- Data: Demo; last name empty; 10110

**Steps:** Enter first name Demo. Leave last name empty. Enter postal code 10110. Continue.

**Expected result:** Cannot advance; last-name validation is visible.

## TC-020 — Checkout postal code required

- Priority: High
- Technique: Negative
- Basis: A4
- Preconditions: Standard user logged in; A in cart; checkout information page open.
- Data: Demo; Tester; postal code empty

**Steps:** Enter Demo and Tester. Leave postal code empty. Continue.

**Expected result:** Cannot advance; postal-code validation is visible.

## TC-021 — Valid information opens order overview

- Priority: High
- Technique: Positive
- Basis: A4
- Preconditions: Standard user logged in; A in cart; checkout information page open.
- Data: Demo; Tester; 10110

**Steps:** Enter Demo, Tester and 10110. Continue. Compare order item with cart.

**Expected result:** Order overview opens and contains A with matching quantity and price.

## TC-022 — Overview totals are arithmetically consistent

- Priority: High
- Technique: Calculation
- Basis: A4
- Preconditions: Standard user logged in; A and B in cart; valid demo checkout details submitted.
- Data: Actual line amounts and displayed tax

**Steps:** Record each line price and quantity. Calculate their sum independently. Compare with item subtotal. Add displayed tax and compare with total.

**Expected result:** Subtotal equals sum of line amounts; total equals subtotal plus displayed tax to two decimals. No assertion about an undocumented tax rate.

## TC-023 — Cancel checkout without placing an order

- Priority: Medium
- Technique: Negative / Navigation
- Basis: A4
- Preconditions: Standard user logged in; A in cart; checkout information page open.
- Data: Product A

**Steps:** Choose Cancel. Inspect destination and cart.

**Expected result:** Checkout information closes without confirmation of an order; A remains available in cart.

## TC-024 — Complete a demo order

- Priority: High
- Technique: End-to-end
- Basis: A4
- Preconditions: Standard user logged in; clean cart.
- Data: Product A; Demo; Tester; 10110

**Steps:** Add A. Open cart and checkout. Enter Demo, Tester and 10110. Continue. Review item and amounts. Select Finish. Inspect confirmation. Return to catalogue and inspect cart.

**Expected result:** Order confirmation appears; returning to catalogue is possible and purchased item no longer remains in cart.

## TC-025 — Logout prevents reopening protected catalogue

- Priority: High
- Technique: Session behaviour
- Basis: A5
- Preconditions: Standard user logged in; record the actual catalogue URL.
- Data: Catalogue URL observed while signed in

**Steps:** Open menu and choose Logout. Confirm login page. Navigate directly to the recorded catalogue URL.

**Expected result:** Logout returns to login page; protected catalogue cannot be used without signing in again.
