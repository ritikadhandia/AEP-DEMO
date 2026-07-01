# US-02 — Create Account record with standard fields

- **Priority:** medium
- **Status:** backlog

## Story

> As an Account Executive, I want to create a new Account record using Salesforce's standard Account creation form so that I can capture a customer organization's core details (name, type, industry, phone, website) and maintain an accurate account base for sales follow-up.

## Acceptance criteria

- Given an Account Executive is on the Accounts list view, when they click the 'New' button, then the standard 'New Account' creation modal opens
- Given the New Account modal is displayed, when the user views the form, then the standard Account fields including Account Name, Phone, Website, Type and Industry are available for entry
- Given no Account Name has been entered, when the user clicks Save, then a required-field error is shown and the record is not saved
- Given the Account Name and other standard fields are completed with valid values, when the user clicks Save, then a new Account record is created with the entered values
- Given the Account record is created successfully, when the save operation completes, then the user is navigated to the newly created Account record page showing the entered Account Name


---
_Auto-generated from in-app state. Source field: `pipeline_artifacts.user_stories[US-02]`. Last updated: 2026-07-01T10:11:16.800723+00:00._
