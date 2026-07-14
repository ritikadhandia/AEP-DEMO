# TC-005 — Create Account record with standard fields — Negative Path: Missing Required Account Name

- **User story:** US-02
- **Persona:** Account Executive
- **Surface:** internal_lightning
- **Pass criteria:** Save operation is prevented, required field validation error appears, and user remains on the creation form
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
4. **fill** — Phone field (input[name="Phone"])
   - _Click in the Phone field and type '555-123-4567' while leaving Account Name empty_
   - `data=555-123-4567`
   - ⤷ expect: Phone field displays '555-123-4567'
5. **select_picklist** — Type picklist (button[role="combobox"][aria-label="Type"])
   - _Click the Type picklist and select 'Customer - Direct'_
   - `value=Customer - Direct`
   - ⤷ expect: Type field shows 'Customer - Direct'
6. **click** — Save button (button[name="SaveEdit"])
   - _Click the Save button without entering an Account Name_
   - ⤷ expect: Form validation prevents save and remains on the New Account modal
7. **verify** — Complete this field
   - _Verify required field error message appears for Account Name field_
   - ⤷ expect: Complete this field
8. **assert_visible** — New Account modal
   - _Verify the New Account modal is still visible and has not closed_
   - ⤷ expect: New Account modal remains open

## Assertions

- Required field error is shown when Account Name is not entered
- Record is not saved when required Account Name field is empty
- User remains on the New Account modal after attempting to save without Account Name


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-005]`. Last updated: 2026-07-14T17:49:32.668390+00:00._
