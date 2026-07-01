# TC-004 — Custom Lead intake form — Edge Case: Required Field Validation

- **User story:** US-001
- **Persona:** Sales Representative
- **Surface:** internal_lightning
- **Pass criteria:** Required field validation prevents submission and displays appropriate error messages while keeping form open
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
   - `data=Amit`
   - ⤷ expect: First Name field displays 'Amit'
5. **fill** — Email field (input[name="Email"])
   - _Click in the Email field and enter a valid email address, leaving Last Name and Mobile empty_
   - `data=amit@example.com`
   - ⤷ expect: Email field displays 'amit@example.com'
6. **click** — Save button (button[name="SaveEdit"])
   - _Click the Save button to attempt form submission with incomplete required fields_
   - ⤷ expect: Form submission is prevented and required field validation errors display
7. **verify** — Last Name field validation
   - _Verify that Last Name field shows required field validation error_
   - ⤷ expect: Complete this field
8. **verify** — Mobile field validation
   - _Verify that Mobile field shows required field validation error_
   - ⤷ expect: Complete this field
9. **verify** — Lead Source field validation
   - _Verify that Lead Source field shows required field validation error_
   - ⤷ expect: Complete this field
10. **verify** — Form state
   - _Verify that the form remains open for correction_
   - ⤷ expect: Custom Lead intake form remains visible and open for field corrections

## Assertions

- Required field validation errors display for incomplete fields
- Appropriate field-level error messages show 'Complete this field'
- Form remains open for correction when validation fails


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.test_scripts.test_cases[TC-004]`. Last updated: 2026-07-01T07:26:18.735992+00:00._
