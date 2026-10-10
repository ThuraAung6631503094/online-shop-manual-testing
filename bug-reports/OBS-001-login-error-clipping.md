# OBS-001 — Login error message partly clipped

- Date: 2026-10-10
- Reporter: Thura Aung
- Status: Open observation — needs further investigation
- Environment: Chrome on Windows; exact version and viewport not recorded
- Related tests: TC-003 and TC-025

## Steps performed

1. Open the SauceDemo login page.
2. Enter standard_user with an incorrect password.
3. Click Login.
4. Inspect the error message.

## Expected result

Login is rejected and the complete error message is readable.

## Actual result

Login was rejected, but the error text appeared clipped at the top and bottom of the red message box. Clipping was also visible in earlier screenshots.

## Impact

The message is harder to read. Login rejection still works.

## Evidence

[Follow-up screenshot](../evidence/OBS-001-login-error-100-percent.png)

The filename reflects the requested 100% zoom check; zoom is not visible in the screenshot and has not been independently verified.

## Assessment

The visual symptom is documented. Its cause and behaviour across browser settings remain unverified. It is not yet counted as a confirmed application defect.

The functional Pass results for TC-003 and TC-025 remain unchanged.