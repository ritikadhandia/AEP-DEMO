# TC-006 — Create Account record with standard fields — Field Availability Verification

- **User story:** US-02
- **Persona:** Account Executive
- **Surface:** internal_lightning
- **Pass criteria:** All standard Account fields including Account Name, Phone, Website, Type and Industry are visible and available for entry in the New Account modal
- **Preconditions:** user_profile: Standard User with Account creation permissions; test_data: ['User has access to Accounts object with Create permission']; app: Sales

## Steps

1. **click** — App Launcher
   - _Click the 9-dot App Launcher icon in the top-left corner_
   - ⤷ expect: App Launcher menu opens showing available apps and items
2. **click** — Accounts
   - _Click on Accounts in the App Launcher menu_
   - ⤷ expect: Accounts list view page opens
3. **click** — New button (button[name="New"])
   - _Click the New button on the Accounts list view_
   - ⤷ expect: New Account creation modal opens
4. **assert_visible** — Account Name field (input[name="Name"])
   - _Verify Account Name field is visible and available for entry_
   - ⤷ expect: Account Name field is present in the form
5. **assert_visible** — Phone field (input[name="Phone"])
   - _Verify Phone field is visible and available for entry_
   - ⤷ expect: Phone field is present in the form
6. **assert_visible** — Website field (input[name="Website"])
   - _Verify Website field is visible and available for entry_
   - ⤷ expect: Website field is present in the form
7. **assert_visible** — Type picklist (button[role="combobox"][aria-label="Type"])
   - _Verify Type picklist field is visible and available for selection_
   - ⤷ expect: Type picklist field is present in the form
8. **assert_visible** — Industry picklist (button[role="combobox"][aria-label="Industry"])
   - _Verify Industry picklist field is visible and available for selection_
   - ⤷ expect: Industry picklist field is present in the form

## Assertions

- New Account creation modal opens when clicking New button
- Account Name field is available for entry
- Phone field is available for entry
- Website field is available for entry
- Type picklist field is available for selection
- Industry picklist field is available for selection


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-006]`. Last updated: 2026-07-14T17:42:49.209164+00:00._
