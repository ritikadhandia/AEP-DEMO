# TC-001 — Custom Lead intake form — Happy Path

- **User story:** US-001
- **Persona:** Sales Representative
- **Surface:** internal_lightning
- **Pass criteria:** Custom form opens, accepts valid data, creates Lead record, and navigates to record page
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
4. **verify** — Custom form fields
   - _Verify that only First Name, Last Name, Mobile, Email and Lead Source fields are visible and all are marked as required_
   - ⤷ expect: Only the 5 specified fields (First Name, Last Name, Mobile, Email, Lead Source) are visible with required field indicators
5. **fill** — First Name (input[placeholder="First Name"])
   - _Click in the First Name field and enter a valid first name_
   - `data=Rajesh`
   - ⤷ expect: First Name field displays 'Rajesh'
6. **fill** — Last Name (input[placeholder="Last Name"])
   - _Click in the Last Name field and enter a valid last name_
   - `data=Kumar`
   - ⤷ expect: Last Name field displays 'Kumar'
7. **fill** — Mobile field (input[name="MobilePhone"])
   - _Click in the Mobile field and enter a valid Indian mobile number_
   - `data=+919876543210`
   - ⤷ expect: Mobile field displays '+919876543210'
8. **fill** — Email field (input[name="Email"])
   - _Click in the Email field and enter a valid email address_
   - `data=rajesh.kumar@example.com`
   - ⤷ expect: Email field displays 'rajesh.kumar@example.com'
9. **select_picklist** — Lead Source (button[role="combobox"][aria-label="Lead Source"])
   - _Open the Lead Source picklist and select a valid option_
   - `value=Web`
   - ⤷ expect: Lead Source shows 'Web'
10. **click** — Save button (button[name="SaveEdit"])
   - _Click the Save button to create the Lead record_
   - ⤷ expect: Form submits successfully and Lead record is created
11. **verify** — Lead record page
   - _Verify navigation to the newly created Lead record page_
   - ⤷ expect: Lead record detail page opens showing the created Lead with entered values

## Assertions

- Custom Lead intake form opens when New button is clicked
- Only 5 specified fields are visible and marked as required
- Valid Indian mobile format is accepted
- Lead record is created with entered values
- User is automatically navigated to the newly created Lead record page


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-001]`. Last updated: 2026-07-01T09:16:37.876075+00:00._
