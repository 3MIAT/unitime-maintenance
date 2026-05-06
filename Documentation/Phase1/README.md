# Phase 1 - Software Evolution and Maintenance

Project: UniTime University Timetabling  
Base version: https://sourceforge.net/projects/unitime/  
Repository URL: https://github.com/3MIAT/unitime-maintenance.git  
Local source root: `JavaSource`  
Prepared on: 2026-05-06

## 1. GitHub Repository

The team created a GitHub repository for the maintenance project:

https://github.com/3MIAT/unitime-maintenance.git

All team members were added as contributors.

| Name | GitHub username | Role |
| --- | --- | --- |
| Mahmoud Magdy | 3MIAT | Maintainer / developer |
| Mohamed Nadeem | mrm9393 | Developer / reviewer |
| Abdelrahman Amr | abdo610amr | Developer / reviewer |

Repository workflow:

1. Each change is implemented on a separate branch.
2. The branch is pushed to GitHub.
3. A pull request is opened for review.
4. Another team member reviews the pull request before merge.
5. Each implementation pull request is linked to its Jira ticket.

## 2. System Description and Requirements

UniTime is a comprehensive university timetabling and scheduling system. It is used by universities to create, manage, and maintain academic schedules for courses, examinations, rooms, instructors, events, and students. The system helps different departments coordinate their scheduling work while reducing conflicts between students, instructors, rooms, and time slots.

As we understood the system, UniTime supports the following main requirements:

| Area | Requirement |
| --- | --- |
| Course timetabling | Create and manage course offerings, classes, instructional types, departments, subject areas, meeting times, rooms, and class relationships. |
| Examination timetabling | Schedule examinations while considering available rooms, exam periods, instructors, enrolled students, and possible exam conflicts. |
| Student scheduling | Assign students to class sections based on course requests, available seats, academic rules, and conflict minimization. |
| Instructor scheduling | Manage instructor information, teaching assignments, instructor availability, preferences, and conflicts between assigned classes. |
| Room and event management | Manage rooms, buildings, room features, room availability, non-class events, meetings, and room sharing. |
| Preferences and constraints | Store and evaluate scheduling preferences and constraints such as preferred times, preferred rooms, distribution constraints, student conflicts, and instructor availability. |
| Reporting and data exchange | Provide reports and support import/export of academic data using formats such as XML, CSV, PDF, and spreadsheets. |
| Administration and security | Support academic sessions, users, roles, permissions, system configuration, and administrative maintenance tasks. |

For this maintenance project, the team will focus only on the Java backend of UniTime. The proposed changes target backend behavior such as validation, reporting, data processing, and logging rather than front-end design changes.

## 3. Static Code Analysis

The team will use SonarQube as the static analysis tool, as suggested in the assignment. The repository includes `sonar-project.properties` to configure the scan.

The local baseline analysis notes are available in:

`Documentation/Phase1/static-analysis-baseline.md`

Recommended SonarScanner command:

```powershell
sonar-scanner `
  -Dsonar.projectKey=unitime-maintenance `
  -Dsonar.host.url=http://localhost:9000 `
  -Dsonar.token=<your-token>
```

The final static analysis evidence should include screenshots or an exported report showing bugs, vulnerabilities, code smells, duplications, security hotspots, and maintainability rating.

## 4. Proposed Features / Bug Fixes

The team has 3 members, so 3 change requests were defined.

| ID | Title | Type | Motivation | Main backend area |
| --- | --- | --- | --- | --- |
| CR-01 | Improve Room Availability Validation Message Details | Existing feature change | Helps administrators understand room conflicts faster by showing clearer room, time, event/class, and session details. | Room availability validation / event backend |
| CR-02 | Validate Negative or Invalid Class Limits | Bug fix / validation improvement | Prevents invalid capacity data that can affect student scheduling and course correctness. | Class/course offering backend validation |
| CR-03 | Improve Exception Logging in Backend Operations | Bug fix / code quality improvement | Improves maintainability and makes backend failures easier to diagnose; may also reduce static analysis issues. | Selected Java backend exception handling |

## 5. Ticketing System Registration

The team used Jira Cloud as the free ticketing system for registering and tracking the proposed change requests. Each change request was registered as a separate Jira ticket. The tickets will be updated during the lifetime of each change using status changes, comments, and linked GitHub pull requests.

| Change request | Jira ticket | Status |
| --- | --- | --- |
| CR-01 | https://unitime-maintenance-1.atlassian.net/browse/KAN-1 | In Progress |
| CR-02 | https://unitime-maintenance-1.atlassian.net/browse/KAN-2 | To Do |
| CR-03 | https://unitime-maintenance-1.atlassian.net/browse/KAN-3 | To Do |

## Phase 1 Submission Checklist

| Item | Status |
| --- | --- |
| GitHub repository exists | Done |
| All team members added as contributors | Done |
| Base UniTime project pushed to GitHub | Done |
| Pull request workflow prepared | Done |
| Project requirements description written | Done |
| Static analysis setup prepared | Done |
| Baseline static analysis report prepared | Done |
| Change requests described | Done |
| Change requests registered in Jira | Done |
| Final SonarQube report attached | TODO |
