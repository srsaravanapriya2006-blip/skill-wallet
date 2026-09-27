# Project Development Phase

## Project Title
Implement Client Script & UI Policy (Incident)

## Development Overview

The project was developed by configuring UI Policies, UI Policy Actions,
and Client Scripts on the ServiceNow Incident table.

These configurations control Incident form behavior and validate data
based on different conditions.

## 1. UI Policy Development

### High Impact Control

A UI Policy named "High Impact Control" was created for the Incident
table.

- Condition: Impact is 1 - High
- Assignment Group: Mandatory
- Reverse if false: Enabled
- Active: Yes

This makes the Assignment Group field mandatory for High-impact
Incidents.

## 2. UI Policy Action Development

A UI Policy Action was configured for the Urgency field.

- Field: Urgency
- Read-only: Enabled

This controls the behavior of the Urgency field when the UI Policy
condition is satisfied.

## 3. onChange Client Script Development

An onChange Client Script named "Auto set urgency for high impact" was
created.

- Table: Incident
- Type: onChange
- Field: Impact
- Active: Yes

When the Impact value is changed to High, the script automatically sets
Urgency to 1 and displays an information message.

## 4. onSubmit Client Script Development

An onSubmit Client Script named "Prevent save if Assigned To missing"
was created.

- Table: Incident
- Type: onSubmit
- Active: Yes

When Impact is High, the script checks whether Assigned To is empty.
If it is empty, the Incident cannot be submitted.

## 5. onCellEdit Client Script Development

An onCellEdit Client Script named "Prevent state change via list edit"
was created.

- Table: Incident
- Type: onCellEdit
- Field: State
- Active: Yes

The script prevents State changes through direct list editing.

## Development Outcome

The completed configuration provides:

- Conditional mandatory field behavior.
- Controlled Urgency field behavior.
- Automatic Urgency value setting.
- Save validation for Assigned To.
- Protection against State changes through list editing.
