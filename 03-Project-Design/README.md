# Project Design Phase

## Project Title
Implement Client Script & UI Policy (Incident)

## Design Overview

The project is designed using ServiceNow UI Policies and Client Scripts
on the Incident table.

The design controls Incident form behavior based on the Impact value
and user actions.

## UI Policy Design

### High Impact Control

- Table: Incident
- UI Policy Name: High Impact Control
- Condition: Impact is 1 - High
- Assignment Group: Mandatory
- Reverse if false: Enabled
- Active: Yes

When the Incident has High Impact, the Assignment Group field is made
mandatory.

## UI Policy Action Design

The Urgency field is configured using a UI Policy Action.

- Field: Urgency
- Read-only: Enabled
- Visible: Unchanged

This controls the behavior of the Urgency field when the UI Policy
condition is satisfied.

## Client Script Design

### 1. onChange Client Script

- Name: Auto set urgency for high impact
- Table: Incident
- Type: onChange
- Field: Impact
- Active: Yes

When Impact is changed to High, the Urgency value is automatically set
to 1.

### 2. onSubmit Client Script

- Name: Prevent save if Assigned To missing
- Table: Incident
- Type: onSubmit
- Active: Yes

When Impact is High, the Incident cannot be saved if the Assigned To
field is empty.

### 3. onCellEdit Client Script

- Name: Prevent state change via list edit
- Table: Incident
- Type: onCellEdit
- Field: State
- Active: Yes

The script prevents State changes through direct list editing.

## Expected Design Behavior

- High-impact Incidents require an Assignment Group.
- Urgency is controlled according to the configured UI Policy.
- Urgency is automatically set when Impact becomes High.
- An Incident cannot be saved with High Impact when Assigned To is empty.
- State changes through list editing are prevented.
- State changes through the Incident form are allowed.
