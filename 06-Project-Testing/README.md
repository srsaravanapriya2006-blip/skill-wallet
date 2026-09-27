# Project Testing Phase

## Project Title
Implement Client Script & UI Policy (Incident)

## Testing Overview

The implemented UI Policies and Client Scripts were tested on the
ServiceNow Incident table to verify that the configured conditions and
validations work correctly.

## Test 1 – Mandatory Field Enforcement

### Test Condition
Set Impact to 1 - High.

### Expected Result
The Assignment Group field becomes mandatory.

### Test Result
The mandatory field behavior works according to the configured UI Policy.

## Test 2 – Successful Incident Save

### Test Condition
Provide the required Incident information, including Assigned To.

### Expected Result
The Incident can be saved successfully.

### Test Result
The Incident is saved successfully when the required information is
provided.

## Test 3 – Reverse Condition

### Test Condition
Change the Impact value from High to another value.

### Expected Result
The UI Policy condition is reversed and the mandatory behavior is
removed.

### Test Result
The reverse condition works as configured.

## Test 4 – List Edit Blocking

### Test Condition
Try to change the State directly from the Incident list.

### Expected Result
The State change is prevented.

### Test Result
The onCellEdit Client Script prevents the State change through list
editing.

## Test 5 – Form-Based State Update

### Test Condition
Change the State through the Incident form.

### Expected Result
The State can be updated through the form.

### Test Result
The form-based State update works correctly.

## Testing Outcome

The testing confirms the configured UI Policies and Client Scripts
provide the required field control, validation, and list-edit
restrictions for Incident records.
