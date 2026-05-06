# Phase 1 - Software Evolution and Maintenance

Project: UniTime University Timetabling  
Base version: https://sourceforge.net/projects/unitime/  
Local source root: `JavaSource`  
Prepared on: 2026-05-06

## 1. GitHub Repository

Repository URL: https://github.com/3MIAT/unitime-maintenance.git

Team contributors:

| Name | GitHub username 
--------------------------------------------------
| Mahmoud Magdy   | 3MIAT
| Mohamed Nadeem  | 
| Abdelrahman Amr | TODO 



## 2. System Description and Requirements

UniTime is a comprehensive university timetabling system. It helps academic institutions create, manage, and maintain schedules for courses, examinations, events, rooms, instructors, and students. The system supports multiple departments working on a shared academic schedule while trying to reduce conflicts and respect institutional constraints.

As understood from the existing project, the backend requirements include:

| Area                        |                                                                  Requirement                                                                          |
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
| Course timetabling          | Maintain course offerings, classes, meetings, departments, subject areas, instructional types, and class relationships.                               |
| Examination timetabling     | Schedule examinations while considering rooms, time periods, instructors, students, and exam conflicts.                                               |
| Student scheduling          | Assign students to class sections based on course requests, availability, limits, and conflict minimization.                                          |
| Instructor scheduling       | Manage instructor assignments, teaching preferences, availability, and assignment conflicts.                                                          |
| Room and event management   | Manage rooms, room features, room availability, non-class events, and room sharing.                                                                   |
| Preferences and constraints | Store and evaluate time, room, distribution, instructor, and student-related preferences during scheduling.                                           |
| Reporting and exports       | Provide reports and XML-based import/export interfaces for institutional data exchange.                                                               |
| Administration              | Support academic sessions, departments, users, roles, permissions, configuration, and system maintenance tasks.                                       |

The maintenance project focuses only on the Java backend, so proposed changes should be implemented in Java services, models, actions, solver logic, reports, or backend validation code rather than front-end redesign.


