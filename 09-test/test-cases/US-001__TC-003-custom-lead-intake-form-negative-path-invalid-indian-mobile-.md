# TC-003 — Custom Lead intake form — Negative Path: Invalid Indian Mobile Format

- **User story:** US-001
- **Persona:** Sales Representative
- **Surface:** internal_lightning
- **Pass criteria:** Invalid Indian mobile format is rejected with error message and form submission is prevented
- **Preconditions:** app: Sales; test_data: ['Custom Lead intake form is deployed and configured to override standard New button behavior', 'Lead Source picklist contains valid values']; user_profile: Sales Representative or System Administrator

## Steps

1. **click** — App Launcher (9-dot waffle icon, top-left)
   - _Click the App Launcher waffle icon in the top-left corner of the page_
   - ⤷ expect: App Launcher menu opens showing available apps and items
2. **click** — Leads
   - _Click on 'Leads' in the App Launcher to navigate to the Leads object_
   - ⤷ expect: Leads list view page opens showing existing Lead records
3. **click** — New button (button[name="New"])
   - _Click the 'New' button on the Leads list view page_
   - ⤷ expect: Custom Lead intake form opens instead of the standard Salesforce form
4. **fill** — First Name (input[placeholder="First Name"])
   - _Click in the First Name field and enter a valid first name_
   - `data=Priya`
   - ⤷ expect: First Name field displays 'Priya'
5. **fill** — Last Name (input[placeholder="Last Name"])
   - _Click in the Last Name field and enter a valid last name_
   - `data=Singh`
   - ⤷ expect: Last Name field displays 'Singh'
6. **fill** — Mobile field (input[name="MobilePhone"])
   - _Click in the Mobile field and enter an invalid mobile number format (not Indian format)_
   - `data=1234567890`
   - ⤷ expect: Mobile field displays '1234567890'
7. **fill** — Email field (input[name="Email"])
   - _Click in the Email field and enter a valid email address_
   - `data=priya.singh@example.com`
   - ⤷ expect: Email field displays 'priya.singh@example.com'
8. **select_picklist** — Lead Source (button[role="combobox"][aria-label="Lead Source"])
   - _Open the Lead Source picklist and select a valid option_
   - `value=Phone Inquiry`
   - ⤷ expect: Lead Source shows 'Phone Inquiry'
9. **click** — Save button (button[name="SaveEdit"])
   - _Click the Save button to attempt form submission_
   - ⤷ expect: Form submission is prevented and mobile format validation error displays
10. **verify** — Mobile field validation error
   - _Verify that an error message displays for invalid mobile format and form remains open_
   - ⤷ expect: Mobile field shows validation error and form remains open for correction

## Assertions

- Invalid mobile number format triggers validation error
- Error message displays preventing form submission
- Form remains open for correction


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-003]`. Last updated: 2026-07-01T10:08:19.913195+00:00._
