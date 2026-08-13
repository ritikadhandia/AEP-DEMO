# TC-002 — Create Account record with standard fields — Happy Path

- **User story:** US-02
- **Persona:** Account Executive
- **Surface:** internal_lightning
- **Pass criteria:** Account record is created with all entered field values and user is navigated to the new record page with success confirmation
- **Preconditions:** app: Sales; test_data: ['User has access to Accounts object with Create permission']; user_profile: Standard User with Account creation permissions

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
4. **fill** — Account Name field (input[name="Name"])
   - _Click in the Account Name field and type 'Tech Solutions Corp'_
   - `data=Tech Solutions Corp`
   - ⤷ expect: Account Name field displays 'Tech Solutions Corp'
5. **fill** — Phone field (input[name="Phone"])
   - _Click in the Phone field and type '555-123-4567'_
   - `data=555-123-4567`
   - ⤷ expect: Phone field displays '555-123-4567'
6. **fill** — Website field (input[name="Website"])
   - _Click in the Website field and type 'www.techsolutions.com'_
   - `data=www.techsolutions.com`
   - ⤷ expect: Website field displays 'www.techsolutions.com'
7. **select_picklist** — Type picklist (button[role="combobox"][aria-label="Type"])
   - _Click the Type picklist and select 'Customer - Direct'_
   - `value=Customer - Direct`
   - ⤷ expect: Type field shows 'Customer - Direct'
8. **select_picklist** — Industry picklist (button[role="combobox"][aria-label="Industry"])
   - _Click the Industry picklist and select 'Technology'_
   - `value=Technology`
   - ⤷ expect: Industry field shows 'Technology'
9. **click** — Save button (button[name="SaveEdit"])
   - _Click the Save button in the New Account modal_
   - ⤷ expect: New Account modal closes and Account record page loads
10. **verify** — Account "Tech Solutions Corp" was created.
   - _Verify the success toast message appears_
   - ⤷ expect: Account "Tech Solutions Corp" was created.
11. **verify** — Tech Solutions Corp
   - _Verify the Account record page header shows the entered Account Name_
   - ⤷ expect: Account record page header displays 'Tech Solutions Corp'

## Assertions

- New Account creation modal opens when clicking New button on Accounts list view
- Standard Account fields (Name, Phone, Website, Type, Industry) are available for entry
- Account record is created successfully with entered values
- User is navigated to the newly created Account record page showing the entered Account Name


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-002]`. Last updated: 2026-08-13T06:55:32.609088+00:00._
