# TC-002 — Create Account record with standard fields - Happy Path

- **User story:** US-02
- **Persona:** Account Executive
- **Surface:** internal_lightning
- **Pass criteria:** New Account modal opens correctly, all standard fields are available and functional, Account record is created successfully with entered values, and user is navigated to the Account detail page displaying all entered information
- **Preconditions:** app: Sales; test_data: ['Standard Account object with Name, Phone, Website, Type, and Industry fields available']; user_profile: Standard User with Account object create permissions

## Steps

1. **click** — App Launcher (9-dot grid icon)
   - _Click the App Launcher (9-dot grid) in the top-left corner_
   - ⤷ expect: App Launcher menu opens
2. **click** — Accounts
   - _Click on 'Accounts' in the App Launcher menu_
   - ⤷ expect: Accounts list view page loads
3. **click** — New button (button[name="New"], a[title="New"])
   - _Click the 'New' button on the Accounts list view_
   - ⤷ expect: New Account modal opens displaying the Account creation form
4. **verify** — New Account form fields
   - _Verify that the Account Name, Phone, Website, Type and Industry fields are visible in the form_
   - ⤷ expect: Account Name, Phone, Website, Type and Industry fields are displayed and available for entry
5. **fill** — Account Name field (input[name="Name"])
   - _Click in the Account Name field and type 'Global Tech Solutions'_
   - `data=Global Tech Solutions`
   - ⤷ expect: Account Name field displays 'Global Tech Solutions'
6. **fill** — Phone field (input[name="Phone"])
   - _Click in the Phone field and type '(555) 123-4567'_
   - `data=(555) 123-4567`
   - ⤷ expect: Phone field displays '(555) 123-4567'
7. **fill** — Website field (input[name="Website"])
   - _Click in the Website field and type 'https://www.globaltechsolutions.com'_
   - `data=https://www.globaltechsolutions.com`
   - ⤷ expect: Website field displays 'https://www.globaltechsolutions.com'
8. **select_picklist** — Type picklist (button[role="combobox"][aria-label="Type"])
   - _Click the Type picklist and select 'Customer - Direct'_
   - `value=Customer - Direct`
   - ⤷ expect: Type field shows 'Customer - Direct'
9. **select_picklist** — Industry picklist (button[role="combobox"][aria-label="Industry"])
   - _Click the Industry picklist and select 'Technology'_
   - `value=Technology`
   - ⤷ expect: Industry field shows 'Technology'
10. **click** — Save button (button[name="SaveEdit"])
   - _Click the Save button to create the Account record_
   - ⤷ expect: Account record is created and user is navigated to the Account detail page
11. **verify** — Account record page header
   - _Verify that the Account detail page shows the Account Name 'Global Tech Solutions' in the page header_
   - ⤷ expect: Account detail page header displays 'Global Tech Solutions'
12. **verify** — Account record details
   - _Verify that the Account record shows all entered values: Phone '(555) 123-4567', Website 'https://www.globaltechsolutions.com', Type 'Customer - Direct', and Industry 'Technology'_
   - ⤷ expect: Account record displays Phone: (555) 123-4567, Website: https://www.globaltechsolutions.com, Type: Customer - Direct, Industry: Technology

## Assertions

- New Account modal opens when clicking the New button from Accounts list view
- Standard Account fields (Account Name, Phone, Website, Type, Industry) are available for entry in the form
- Account record is successfully created when all required and standard fields are completed with valid values
- User is navigated to the newly created Account record page showing the entered Account Name and all field values


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-002]`. Last updated: 2026-07-01T10:08:19.913874+00:00._
