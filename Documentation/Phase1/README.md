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

we are going to use SonarQube as the static analysis tool, as suggested in the assignment. The repository includes `sonar-project.properties` to configure the scan.

The local baseline analysis notes are available in:

`Documentation/Phase1/static-analysis-baseline.md`



The final static analysis evidence should include screenshots or an exported report showing bugs, vulnerabilities, code smells, duplications, security hotspots, and maintainability rating.

## 4. Proposed Features / Bug Fixes

The team has 3 members, so 3 change requests were defined.

|                        Title                         |                 Type               |                          Main backend area                           |
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
| Improve Room Availability Validation Message Details | Existing feature change            | Room availability validation / event backend                         |
| Validate Negative or Invalid Class Limits            | Bug fix / validation improvement   | Class/course offering backend validation                             |
| Improve Exception Logging in Backend Operations      | Bug fix / code quality improvement | Selected Java backend exception handling                             |

## 5. Ticketing System Registration

The team used Jira Cloud as the free ticketing system for registering and tracking the proposed change requests. Each change request was registered as a separate Jira ticket. The tickets will be updated during the lifetime of each change using status changes, comments, and linked GitHub pull requests.

|                  Jira ticket                             |         Status     |
| --- | --- | --- |
| https://unitime-maintenance-1.atlassian.net/browse/KAN-1 |      In Progress   |
| https://unitime-maintenance-1.atlassian.net/browse/KAN-2 |        To Do       |
| https://unitime-maintenance-1.atlassian.net/browse/KAN-3 |        To Do       |

