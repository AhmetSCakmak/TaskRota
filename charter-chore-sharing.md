# Project Charter: TaskRota – Shared Job & Task Manager

## 1. Project Purpose and Objectives
TaskRota is a web application for any group of people who share responsibilities, such as housemates, student clubs, project teams, volunteer groups or small offices. It shows which jobs need to be done, who is responsible for each one, and rotates recurring jobs fairly among group members. The objective is to deliver a secure, service-based web application where users create or join groups, define one-time and recurring jobs, see their assigned jobs, and mark them as done, deployed on a cloud platform and developed with a test-first approach.

## 2. Stakeholders & Roles
* **Product Owner:** Ahmet Selim Çakmak
* **Software Engineering Team:**
    * Kaan Gürsu : Project Manager / Backend Developer (Authentication & Groups)
    * Zeynep Sude Genç : Customer Meeting & Requirements Lead / Backend Developer (Jobs, Scheduling & Rotation Logic)
    * Ahmet Selim Çakmak : Documentation Lead / Backend Developer (Notifications & Reminders)
    * Zümra Aydoğan : AI Usage Reporting Lead / Frontend Developer
    * Nehir Güneş Aydemir : QA Lead / DevOps (Database, CI/CD, Deployment, Testing)
* **GH Repo/Project URL:** https://github.com/AhmetSCakmak/TaskRota

## 3. Project Scope
### Project domain
Collaboration and shared responsibility management. Possible customers are shared houses and dorms, student clubs and societies, university project teams, volunteer organizations, and small offices or shops that rotate duties (e.g. opening shifts, kitchen cleaning, meeting notes). Key users are group members who share recurring or one-time jobs and want a fair, transparent way to divide them.

### In-Scope
* User registration, login and profile management (authentication)
* Group management: creating a group, joining with an invite code, leaving a group, group owner removing a member; a user can belong to multiple groups
* Job management: creating, editing and deleting jobs with a title, description, due date and optional category
* One-time jobs assigned to a specific member or claimed by a volunteer from an open job list
* Recurring jobs with a frequency (daily, weekly, monthly) and automatic fair rotation among group members
* "My jobs" view across all groups, and a group overview of the current period
* Marking jobs as done and highlighting overdue jobs
* Job history (who completed what and when) and simple contribution statistics per member
* Swap and skip requests between group members
* Authorization: users can only view and edit jobs in groups they belong to, and can only complete jobs assigned to them
* Email reminders for due and overdue jobs
* Cloud deployment of backend, frontend and database

### Out-of-Scope
* Native mobile applications (iOS / Android)
* Full project management features (Gantt charts, sprints, time tracking)
* Payments, wages or reward systems for completed jobs
* Shared expense and bill splitting
* In-app chat between group members
* Integration with external tools (Slack, Trello, Jira, calendars)
* Third-party login (Google, Facebook, etc.)

## 4. Technology Stack

### Backend Stack
* Python with FastAPI (REST API)
* PostgreSQL (relational database)
* SQLAlchemy and Alembic (ORM and database migrations)
* JWT-based authentication with hashed passwords (bcrypt)
* APScheduler (scheduled rotation and reminder jobs)
* SMTP / transactional email service (e.g. SendGrid) for reminders
* pytest (test-first development)
* Docker
* GitHub Actions (CI pipeline)
* Render or Railway (cloud hosting)

### Frontend Stack
* React with TypeScript
* Vite
* Tailwind CSS
* Axios (API calls)
* Vitest and React Testing Library

### AI Stack
* {_AI coding agent, e.g. Claude Code / GitHub Copilot_} as an AI teammate for code generation, test generation and code review
* Tracking of AI contributions, effort and review time through GitHub issues and labels
* Logging of Gen-AI-introduced errors, how they were detected and how they were fixed

## 5. Project Milestones
| Deliverable                       | Deadline          |
|---                                |---                |
| Project Charter                   | 13.10.2026 23:59  |
| Project Plan                      | 28.10.2026 23:59  |
| Requirement Specification Report  | 10.11.2026 23:59  |
| Requirement Analysis Report       | 24.11.2026 23:59  |
| Software Design Report            | 08.12.2026 23:59  |
| Software Test Report              | 22.12.2026 23:59  |
| Codebase                          | 27.12.2026 23:59  |
| Demo                              | 30.12.2026 12:30  |
| Presentation                      | 30.12.2026 12:30  |
