# Phase 1 Change Requests

These change requests are intentionally backend-focused because the assignment scope excludes front-end work. Use one ticket per change request in GitHub Issues, Jira, Bugzilla, or another approved free ticketing system.

## CR-01 - Validate Duplicate Instructor Assignments Before Saving

Type: Bug fix / validation improvement  
Priority: Medium  
Suggested owner: TODO  
Ticket URL: TODO

### Motivation

Instructor assignment conflicts should be caught as early as possible. If duplicate or conflicting instructor assignments are accepted and only discovered later, schedule managers may waste time debugging solver results or manual scheduling errors.

### Proposed Change

Add or improve backend validation so class/instructor assignment saving checks for duplicate instructor assignment conflicts in the same academic session and reports a clear validation error before persistence.

### Acceptance Criteria

- Backend validation rejects duplicate/conflicting instructor assignments.
- The validation message identifies the instructor and the conflicting class or time information when available.
- Existing valid instructor assignments continue to save successfully.
- Unit or integration-level validation evidence is provided.

### Ticket Updates

| Date | Status | Note |
| --- | --- | --- |
| 2026-05-06 | Open | Change request proposed for Phase 1. |

## CR-02 - Add Conflict Summary to Course Timetable Export

Type: Feature addition  
Priority: Medium  
Suggested owner: TODO  
Ticket URL: TODO

### Motivation

Exported timetable data is more useful when it includes a compact summary of known conflicts. This helps reviewers identify schedule quality issues without manually inspecting multiple reports.

### Proposed Change

Extend the backend export/reporting path for course timetables to include a conflict summary section containing counts for student conflicts, instructor conflicts, and room conflicts where the data is available.

### Acceptance Criteria

- Exported timetable data includes a conflict summary.
- Summary values are generated from backend scheduling/conflict data, not manually entered text.
- Existing export consumers remain compatible, or compatibility impact is documented.
- Validation evidence compares export output before and after the change.

### Ticket Updates

| Date | Status | Note |
| --- | --- | --- |
| 2026-05-06 | Open | Change request proposed for Phase 1. |

## CR-03 - Improve Room Availability Validation Message Details

Type: Change to existing feature  
Priority: High  
Suggested owner: TODO  
Ticket URL: TODO

### Motivation

Room availability problems are common in scheduling systems. Vague validation messages slow down administrators because they do not clearly show which room, date, time, or event caused the failure.

### Proposed Change

Improve backend validation messages for room availability conflicts so the response includes actionable details such as room name, conflicting time, event/class reference, and academic session when available.

### Acceptance Criteria

- Room availability conflict messages include enough details for an administrator to identify the issue.
- Existing validation behavior remains unchanged except for clearer message content.
- Tests or manual validation demonstrate the old and new message behavior.
- The implementation avoids exposing sensitive data to users without permission.

### Ticket Updates

| Date | Status | Note |
| --- | --- | --- |
| 2026-05-06 | Open | Recommended first implementation because it is useful and lower risk than solver logic changes. |

## CR-04 - Add Audit Log Entry When Class Limit Changes

Type: Feature addition  
Priority: Medium  
Suggested owner: TODO  
Ticket URL: TODO

### Motivation

Class limits affect section capacity and student scheduling outcomes. Recording class limit changes improves traceability and helps administrators understand why schedule capacity changed over time.

### Proposed Change

Add backend audit logging when a class limit is changed, including the class identifier, previous limit, new limit, user, timestamp, and academic session when available.

### Acceptance Criteria

- Changing a class limit creates an audit entry.
- The entry includes previous and new values.
- No audit entry is created when the value is unchanged.
- Validation evidence shows an audit entry after a class limit update.

### Ticket Updates

| Date | Status | Note |
| --- | --- | --- |
| 2026-05-06 | Open | Change request proposed for Phase 1. |
