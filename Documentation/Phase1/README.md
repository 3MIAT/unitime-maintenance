# Phase 1 - Software Evolution and Maintenance

Project: UniTime University Timetabling  
Base version: https://sourceforge.net/projects/unitime/  
Local source root: `JavaSource`  
Prepared on: 2026-05-06

## 1. GitHub Repository

Repository URL: https://github.com/3MIAT/unitime-maintenance.git

Team contributors:

| Name            | GitHub username | Role      |
---------------------------------------------------------------
| Mahmoud Magdy   | 3MIAT           |  reviewer |
| Mohammed Nadem  | mrm9393         | Developer |
| Abdelrahman Amr | abdo610amr      | Developer |




## 2. System Description and Requirements

UniTime is a comprehensive university timetabling system. It helps academic institutions create, manage, and maintain schedules for courses, examinations, events, rooms, instructors, and students. The system supports multiple departments working on a shared academic schedule while trying to reduce conflicts and respect institutional constraints.

As understood from the existing project, the backend requirements include:

| Area                       |                                                     Requirement                                                                    |
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
| Course timetabling          | Maintain course offerings, classes, meetings, departments, subject areas, instructional types, and class relationships.           |
| Examination timetabling     | Schedule examinations while considering rooms, time periods, instructors, students, and exam conflicts.                           |
| Student scheduling          | Assign students to class sections based on course requests, availability, limits, and conflict minimization.                      |
| Instructor scheduling       | Manage instructor assignments, teaching preferences, availability, and assignment conflicts.                                      |
| Room and event management   | Manage rooms, room features, room availability, non-class events, and room sharing.                                               |
| Preferences and constraints | Store and evaluate time, room, distribution, instructor, and student-related preferences during scheduling.                       |
| Reporting and exports       | Provide reports and XML-based import/export interfaces for institutional data exchange.                                           |
| Administration              | Support academic sessions, departments, users, roles, permissions, configuration, and system maintenance tasks.                   |

The maintenance project focuses only on the Java backend, so proposed changes should be implemented in Java services, models, actions, solver logic, reports, or backend validation code rather than front-end redesign.

## 3. Static Code Analysis

Tooling plan:

- Primary recommended tool: SonarQube / SonarScanner, matching the lab workflow.
- Project configuration added in `sonar-project.properties`.
- Baseline local scan summary is recorded in `static-analysis-baseline.md`.

The local machine did not have `mvn`, `ant`, `sonar-scanner`, `pmd`, `checkstyle`, or `spotbugs` available on PATH at preparation time. Because of that, the baseline report includes a lightweight local scan using PowerShell pattern checks. Run SonarQube from a machine with the scanner installed before final submission and attach/export the Sonar report screenshots or PDF.



## 4. Proposed Change Requests

Minimum required number of changes equals the number of team members. The table below defines four candidate backend changes so a 3-person or 4-person team is covered. Remove one only if your team has exactly 3 members and your instructor prefers one change per member.

| ID | Title | Type | Motivation | Main backend area |
| --- | --- | --- | --- | --- |
| CR-01 | Validate duplicate instructor assignments before saving | Bug fix / validation improvement | Prevents an instructor from being assigned in conflicting ways and improves data correctness before the timetable reaches the solver. | Instructor and class assignment validation |
| CR-02 | Add conflict summary to course timetable export | Feature addition | Users exporting timetable data need a quick backend-generated summary of student, room, and instructor conflicts for review. | XML export / timetable reports |
| CR-03 | Improve room availability validation message details | Change to existing feature | Existing validation errors can be difficult to act on; clearer backend messages reduce troubleshooting time for administrators. | Room availability / event validation |
| CR-04 | Add audit log entry when class limit changes | Feature addition | Class limits affect student scheduling and capacity planning, so administrators should be able to trace when and why limits changed. | Class/course offering maintenance |

Recommended first implementation choice: CR-03. It is useful, backend-focused, and likely lower risk than solver changes while still being demonstrable in Phase 2 through tests and before/after validation output.

## 5. Ticketing System Registration

Use a free ticketing system such as GitHub Issues, Jira, Bugzilla, or another tool approved by the instructor. Since the repository is already on GitHub, GitHub Issues is the simplest option.

Create one ticket for each selected change request:

| Change request | Ticket URL | Status |
| --- | --- | --- |
| CR-01 | TODO | Open |
| CR-02 | TODO | Open |
| CR-03 | TODO | Open |
| CR-04 | TODO | Open |

Each ticket should include:

- Change type: bug fix, existing-feature change, or new feature.
- Motivation and expected benefit.
- Affected backend modules/classes after impact analysis.
- Acceptance criteria.
- Pull request link when implementation starts.
- Status updates during the change lifetime.

See `change-requests.md` for ready-to-copy ticket descriptions.

## Phase 1 Submission Checklist

| Item | Status |
| --- | --- |
| GitHub repository exists | Done: https://github.com/3MIAT/unitime-maintenance.git |
| All team members added as contributors | Done |
| Pull request workflow prepared | Done: `.github/pull_request_template.md` |
| Project requirements description written | Done |
| Static analysis setup prepared | Done: `sonar-project.properties` |
| Baseline static analysis report prepared | Done: `static-analysis-baseline.md` |
| Change requests described | Done: `change-requests.md` |
| Tickets created in ticketing system | TODO: add ticket URLs |
