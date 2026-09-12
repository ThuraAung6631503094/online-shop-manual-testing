# Test plan

Version: 0.1 | Prepared: 2026-09-12 | Stage: awaiting authenticated execution

## Objective

Check whether a standard user can sign in, select products, manage a cart, complete a demo checkout and sign out. Document what was tested, actual outcomes and remaining risks.

## Scope and priorities

| Area | Risk | Cases |
| --- | --- | --- |
| Login | Valid users blocked or invalid users admitted | TC-001 to TC-007 |
| Catalogue | Incorrect information or misleading sorting | TC-008 to TC-011 |
| Cart | Lost, incorrect or unremovable items | TC-012 to TC-017 |
| Checkout | Missing validation, incorrect totals or failed order flow | TC-018 to TC-024 |
| Logout | Continued access after logout | TC-025 |

Run TC-002, TC-012, TC-021 and TC-024 first after the baseline to check the critical shopping journey. Then execute remaining high-priority cases followed by medium and low priorities. Cases are independent unless their preconditions explicitly create a shared setup.

Excluded: real payments, delivery, load testing, API testing, source-code review, penetration testing, full accessibility audit and cross-browser/mobile certification. The initial run covers one cloud Chrome browser only.

## Test basis and assumptions

No formal requirements document was supplied. OBS-01 is direct evidence: the login page visibly offers username and password inputs, a Login button and demo account guidance. A1–A5 below are proposed expectations to review against the application, not official specifications.

| Basis | Proposed expectation |
| --- | --- |
| A1 | Valid standard credentials allow access; missing, invalid and locked-user credentials are rejected. |
| A2 | Catalogue and detail data agree; sorting follows the selected direction. |
| A3 | Cart accurately represents additions/removals and retains items during navigation/refresh in the same session. |
| A4 | Checkout requires first name, last name and postal code; overview is consistent with cart; totals agree arithmetically; completion confirms an order and clears purchased cart items. |
| A5 | Logout ends access to the protected catalogue until another login. |

Disagreement with an assumption is a candidate finding requiring triage, not automatically an accepted product defect. Country-specific postal-code formats, field maximum lengths and tax rates are unspecified; do not invent acceptance rules.

## Environment and data

Target: https://www.saucedemo.com/

Baseline: remote Chrome desktop browser, screenshot 1363 × 936 pixels; exact browser version and application build not recorded. First observation at 2026-09-12T05:27:19.437Z (UTC). Do not claim testing on the owner's Windows laptop.

Use only accounts and the public demo password shown on the target login page. Use the standard user for the main run and the listed locked user for TC-007. Use fictional checkout values Demo / Tester / 10110. Record chosen product names and prices from the current UI rather than assuming a price from a tutorial.

Before each cart-dependent case, remove existing demo items through the UI and add exactly the products in its preconditions. Empty applicable form fields before negative cases. Use a new signed-out session when required. Never clear the owner's unrelated browsing data.

## Execution and evidence rules

Pass: every stated expected result was observed. Fail: an observed result disagrees with the documented expectation; link a candidate finding for triage. Blocked: an attempted case could not be completed due to a specific prerequisite/environment issue. Not run: the case has not been attempted.

Record executor, time, environment, inputs, actual behaviour and evidence. Preserve original screenshots; use filenames containing case ID and run ID for new captures. A screenshot may support several cases only when it actually demonstrates their outcomes. Never turn expected results into actual results.

## Defect triage

Report reproducible observations with steps, expected and actual behaviour, impact, environment, frequency and evidence. Severity describes impact; priority describes proposed repair urgency. Label these as provisional in this practice project. Retest only after evidence of a change; retain original and retest runs.

## Completion criteria

All 25 cases attempted; statuses and evidence recorded; failures triaged; blocked cases explained; high-risk limitations stated. Completion of testing does not require that all cases pass. The final summary must reflect the actual scope, and cannot certify production readiness.
