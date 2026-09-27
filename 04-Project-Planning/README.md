# Project Planning Phase

## Project Title
Implement Client Script & UI Policy (Incident)

## Project Implementation Plan

The project is planned as a sequence of configuration, development, and
testing activities on the ServiceNow Incident table.

## Implementation Sequence

### Task 1 – Create UI Policy

Create the High Impact Control UI Policy on the Incident table.

- Condition: Impact is 1 - High
- Assignment Group: Mandatory
- Reverse if false: Enabled

### Task 2 – Configure UI Policy Action

Configure the Urgency field using a UI Policy Action.

- Field: Urgency
- Read-only: Enabled

### Task 3 – Create onChange Client Script

Create an onChange Client Script for the Impact field.

The script automatically sets Urgency to 1 when Impact is High.

### Task 4 – Create onSubmit Client Script

Create an onSubmit Client Script to validate the Assigned To field.

When Impact is High, the Incident should not be saved if Assigned To
is empty.

### Task 5 – Create onCellEdit Client Script

Create an onCellEdit Client Script for the State field.

The script prevents State changes through direct list editing.

### Task 6 – Testing

Test all configured UI Policies and Client Scripts.

The testing includes:

- Mandatory field enforcement.
- Successful Incident save.
- Reverse condition behavior.
- List edit blocking.
- Form-based State update.

## Expected Project Outcome

The planned implementation should provide controlled Incident form
behavior, validation, and improved data consistency.
