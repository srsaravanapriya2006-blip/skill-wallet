# Requirement Analysis Phase

## Project Title
Implement Client Script & UI Policy (Incident)

## Problem Statement
Incident records require consistent and accurate data entry for effective
triage, routing, and resolution.

Relying only on user awareness and manual checks can result in incomplete,
inconsistent, or incorrect information being submitted. This can affect
reporting accuracy, SLA compliance, and overall service quality.

Therefore, conditional field behavior and validation need to be enforced
directly at the user interface level.

## Project Objective
The objective is to demonstrate how ServiceNow client-side controls can be
used to enforce data integrity on Incident records.

The project uses UI Policies and Client Scripts to:

- Make fields mandatory when required.
- Auto-populate values based on conditions.
- Control field behavior.
- Prevent record submission when required conditions are not met.
- Ensure Incident records contain complete and valid information.

## Functional Requirements

The project requires the following functionality:

1. Create a UI Policy for high-impact Incidents.
2. Make the required field mandatory when the condition is satisfied.
3. Configure the Urgency field behavior using a UI Policy Action.
4. Automatically set Urgency when Impact is High.
5. Prevent saving an Incident when Assigned To is missing for a High-impact Incident.
6. Prevent State changes through direct list editing.
7. Allow State changes through the Incident form.
8. Test all configured behaviors.

## Skills / Technologies Required

- ServiceNow
- Incident Management
- UI Policy
- UI Policy Actions
- Client Scripts
- Form Validation
