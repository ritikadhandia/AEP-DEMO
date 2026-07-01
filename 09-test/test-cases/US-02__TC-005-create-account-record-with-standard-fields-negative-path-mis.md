# TC-005 — Create Account record with standard fields — Negative Path: Missing Required Account Name

- **User story:** US-02
- **Persona:** Account Executive
- **Surface:** internal_lightning
- **Pass criteria:** Required field validation prevents save and keeps form open when Account Name is missing
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
4. **fill** — Phone field (input[name="Phone"])
   - _Click in the Phone field and enter '(555) 123-4567' but leave Account Name empty_
   - `data=(555) 123-4567`
   - ⤷ expect: Phone field displays '(555) 123-4567'
5. **select_picklist** — Type picklist (button[role="combobox"][aria-label="Type"])
   - _Click the Type picklist and select 'Customer - Direct'_
   - `value=Customer - Direct`
   - ⤷ expect: Type field shows 'Customer - Direct'
6. **click** — Save button (button[name="SaveEdit"])
   - _Click the Save button without entering an Account Name_
   - ⤷ expect: Form remains open and validation error appears on Account Name field
7. **verify** — Complete this field
   - _Verify the required field error message appears for Account Name_
   - ⤷ expect: Complete this field
8. **assert_visible** — New Account modal
   - _Verify the New Account modal remains open and the record was not saved_
   - ⤷ expect: New Account modal is still visible

## Assertions

- Required-field error is shown when Account Name is not entered
- Account record is not saved when required Account Name field is empty
- Form remains open after validation failure


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-005]`. Last updated: 2026-07-01T09:08:15.664619+00:00._
