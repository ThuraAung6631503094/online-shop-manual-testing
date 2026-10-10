# Test summary

Updated: 2026-10-10 (Asia/Bangkok)
Runs covered: R01, R02 and R03
Stage: planned execution completed; final documentation review in progress

## Scope

Manual testing of SauceDemo / Swag Labs covering login, product details, sorting, cart behaviour, checkout and logout.

## Recorded results

| Measure | Result |
| --- | ---: |
| Designed test cases | 25 |
| Unique cases executed | 25 |
| Passed | 25 |
| Failed | 0 |
| Not run | 0 |
| Confirmed defects | 0 |
| Open observations | 1 |

Execution coverage is 25/25 (100%) of the planned cases, based on the recorded results.

Each case is counted once across the three runs. Earlier “Not run” entries in R01 describe that earlier session and do not override later results.

Passing these cases does not establish that the application is defect-free or production-ready.

## Execution ownership

- R01: ChatGPT performed TC-001, the initial login-page check, on 12 September 2026.
- R02: Thura Aung performed login, cart and checkout tests.
- R03: Thura Aung performed the remaining product, sorting, cart, checkout and logout tests on 10 October 2026.

ChatGPT assisted with test guidance, review of submitted screenshots and documentation. The execution log records the reported outcomes.

## Results by area

| Area | Cases | Recorded outcome |
| --- | --- | --- |
| Login page and authentication | TC-001–TC-007 | 7 passed |
| Product details and sorting | TC-008–TC-011 | 4 passed |
| Cart behaviour and persistence | TC-012–TC-017 | 6 passed |
| Checkout validation and order flow | TC-018–TC-024 | 7 passed |
| Logout and protected-page access | TC-025 | 1 passed |

For TC-022, one Backpack at $29.99 and one Bike Light at $9.99 produced a subtotal of $39.98. Adding the displayed tax of $3.20 produced the displayed total of $43.18.

This verified arithmetic consistency, not the correctness of an undocumented tax rate.

## Open observation: clipped login error text

Error text appeared partly clipped in some screenshots, including the message shown when attempting to open /inventory.html after logout.

Login rejection and protected-page blocking worked in the recorded tests. The possible visual issue remains separate from those functional results.

Status: needs investigation; not a confirmed defect.

Follow-up:
- Repeat the affected steps at 100% browser zoom.
- Record browser version and window size.
- Check whether the complete message is readable.
- If reproducible, document the steps, expected and actual behaviour, and screenshot evidence.

## Evidence and traceability

- [Detailed test cases](../test-cases/test-cases.md)
- [Execution log](../test-cases/execution-log.md)
- [Screenshot folder](../evidence/)
- [Evidence index](../evidence/README.md)
- [Defect register and template](../bug-reports/README.md)

## Limitations

- Results cover the planned scenarios and recorded sessions only.
- Browser version and application build were not recorded.
- No cross-browser or mobile testing results are available.
- No automated suite, load testing or comprehensive security assessment was performed.
- Expected results are project assumptions, not verified official business requirements.
- Historical results have not all been rerun in a single session.

## Repository status

The owner reported committing and pushing test results and screenshots to:

https://github.com/ThuraAung6631503094/online-shop-manual-testing

## Remaining work

- Review evidence links and the evidence index.
- Investigate or explicitly retain the open visual observation.
- Commit and push the updated project documentation.

## Observation follow-up — 2026-10-10

Clipping remained visible in the follow-up screenshot. OBS-001 stays open; its cause remains unverified.

[Observation report and evidence](../bug-reports/OBS-001-login-error-clipping.md)

