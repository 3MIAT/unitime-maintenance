# Phase 1 Change Requests

These change requests are intentionally backend-focused because the assignment scope excludes front-end work. The team used Jira Cloud to register and track each change request.

## CR-01 - Improve Room Availability Validation Message Details

Type: Existing feature change  
Priority: High  
Suggested owner: Abdelrahman Amr  
Ticket URL: https://unitime-maintenance-1.atlassian.net/browse/KAN-1

### Motivation

Room availability problems are common in scheduling systems. Vague validation messages slow down administrators because they do not clearly show which room, date, time, event, or class caused the conflict.

### Proposed Change

Improve backend validation messages for room availability conflicts so the response includes actionable details such as room name, conflicting time, related event/class, and academic session when available.

### Acceptance Criteria

- Room availability conflict messages include clearer details.
- Existing validation behavior remains unchanged except for message content.
- Manual validation or tests show the old and new message behavior.

### Ticket Updates

| Date | Status | Note |
| --- | --- | --- |
| 2026-05-06 | In Progress | Change request registered in Jira for Phase 1. |

## CR-02 - Validate Negative or Invalid Class Limits

Type: Bug fix / validation improvement  
Priority: Medium  
Suggested owner: Mohamed Nadeem  
Ticket URL: https://unitime-maintenance-1.atlassian.net/browse/KAN-2

### Motivation

Class limits affect student scheduling and course capacity. Invalid class limits, such as negative values, can lead to incorrect scheduling results or inconsistent academic data.

### Proposed Change

Add backend validation to prevent saving invalid class limits, such as negative values or values lower than already assigned/enrolled students when this information is available.

### Acceptance Criteria

- Negative class limits cannot be saved.
- Invalid capacity values produce a clear validation error.
- Valid class limits continue to save normally.

### Ticket Updates

| Date | Status | Note |
| --- | --- | --- |
| 2026-05-06 | To Do | Change request registered in Jira for Phase 1. |

## CR-03 - Improve Exception Logging in Backend Operations

Type: Bug fix / code quality improvement  
Priority: Medium  
Suggested owner: Mahmoud Magdy  
Ticket URL: https://unitime-maintenance-1.atlassian.net/browse/KAN-3

### Motivation

Weak exception handling makes backend failures difficult to diagnose. Replacing direct `printStackTrace()` usage or swallowed exceptions with proper logging improves maintainability and supports better static analysis results.

### Proposed Change

Replace unsafe or unclear exception handling in selected backend classes with application logging and meaningful error messages.

### Acceptance Criteria

- Selected backend exceptions are logged using the project logging mechanism.
- Direct `printStackTrace()` usage is reduced in the selected files.
- Behavior remains unchanged except for improved diagnostics.

### Ticket Updates

| Date | Status | Note |
| --- | --- | --- |
| 2026-05-06 | To Do | Change request registered in Jira for Phase 1. |
