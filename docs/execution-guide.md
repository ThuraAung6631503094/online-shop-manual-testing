# Step-by-step execution guide

1. Read the scope and assumptions in the test plan. Review the expected result before each case.
2. Open SauceDemo. Use only its published demo accounts. For ChatGPT-controlled execution, complete the secure sign-in prompt in the conversation; never paste personal credentials into chat.
3. Run the critical path: TC-002, TC-012, TC-021, TC-024. Inspect each page and revise draft locator/button wording if the live UI differs. Record changes to the design.
4. For each case, establish its preconditions, perform the steps, compare every expected outcome, and capture useful evidence. Do not use a previous test's success as proof of the next one.
5. Run remaining high-priority cases, then medium and low priorities. Negative login cases require their own secure credential-entry flow when performed by ChatGPT.
6. If a mismatch occurs, save the evidence, reproduce from a clean starting state and check the assumption. Write a candidate bug report with provisional impact and priority. Do not invent a bug quota.
7. Update the execution log immediately. If you run the test yourself, create R02 with your real executor name, date and environment; preserve AI-assisted R01.
8. Reconcile summary counts with the log. Describe what remains untested and why. A not-run case is neither pass nor fail.
9. Review all files before publication. Be prepared to explain one positive test, one negative test, cart setup, expected-versus-actual reasoning and the remaining limitations in an interview.

## Example of recording a result

Do not copy this as an actual result: after executing TC-013, an entry should name both selected products, their observed prices, whether each appeared once and the actual badge count. Link the screenshot showing that state. If any expected check was omitted, do not mark the entire case as passed.
