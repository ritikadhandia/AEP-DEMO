# TC-006 — Create Account record with standard fields — Field Availability Verification

- **User story:** US-02
- **Persona:** Account Executive
- **Surface:** internal_lightning
- **Pass criteria:** All specified standard Account fields are present and accessible in the New Account creation form
- **Preconditions:** app: Sales; user_profile: Standard User with Account create permissions

## Steps

1. **click** — App Launcher
   - _Click the App Launcher (9-dot waffle icon) in the top-left corner_
   - ⤷ expect: App Launcher menu opens showing available apps and items
2. **click** — Accounts
   - _Click on Accounts in the App Launcher to navigate to the Accounts tab_
   - ⤷ expect: Accounts list view page loads showing existing Account records
3. **click** — New button (button[name="New"])
   - _Click the New button on the Accounts list view page_
   - ⤷ expect: New Account modal opens with the standard Account creation form
4. **assert_visible** — Account Name field (input[name="Name"])
   - _Verify Account Name field is present and available for entry_
   - ⤷ expect: Account Name field is visible on the form
5. **assert_visible** — Phone field (input[name="Phone"])
   - _Verify Phone field is present and available for entry_
   - ⤷ expect: Phone field is visible on the form
6. **assert_visible** — Website field (input[name="Website"])
   - _Verify Website field is present and available for entry_
   - ⤷ expect: Website field is visible on the form
7. **assert_visible** — Type picklist (button[role="combobox"][aria-label="Type"])
   - _Verify Type picklist field is present and available for selection_
   - ⤷ expect: Type picklist field is visible on the form
8. **assert_visible** — Industry picklist (button[role="combobox"][aria-label="Industry"])
   - _Verify Industry picklist field is present and available for selection_
   - ⤷ expect: Industry picklist field is visible on the form

## Assertions

- Standard Account fields including Account Name, Phone, Website, Type and Industry are available for entry in the New Account form


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-006]`. Last updated: 2026-07-01T14:02:32.059170+00:00._
