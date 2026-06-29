# US-001 — Create custom Lead intake form with Indian mobile validation

- **Priority:** high
- **Status:** backlog

## Story

> Currently users must navigate Salesforce's standard Lead creation form with numerous optional fields, slowing down lead capture. This custom form will replace the standard 'New' button behavior to show only the 5 mandatory fields (First Name, Last Name, Mobile, Email, Lead Source) with Indian mobile format validation. Upon successful save, users will be automatically redirected to the newly created Lead record page for immediate follow-up actions.

## Acceptance criteria

- Given a user clicks the 'New' button on Lead object pages, when the action is triggered, then the custom Lead intake form opens instead of the standard Salesforce form
- Given the custom form is displayed, when a user views the form, then only First Name, Last Name, Mobile, Email and Lead Source fields are visible with all marked as required
- Given a user enters a mobile number, when the number format is not valid Indian format (+91 followed by 10 digits), then an error message displays preventing form submission
- Given all required fields are completed with valid data, when the user clicks Save, then a new Lead record is created in Salesforce with the entered values
- Given a Lead record is successfully created, when the save operation completes, then the user is automatically navigated to the newly created Lead record page
- Given invalid or incomplete data is entered, when the user attempts to save, then appropriate field-level error messages display and the form remains open for correction


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.user_stories[US-001]`. Last updated: 2026-06-29T09:51:44.292451+00:00._
