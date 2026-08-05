TaskMatrix

Enterprise Agile Project Management Capstone Application

TaskMatrix is a commercial-grade project management platform designed for teams that need a centralized system to create workspaces, manage projects, organize tasks, collaborate with members, and track project progress through Kanban-style workflows.

Project Information

Field

Details

Project Name

TaskMatrix

Repository

prodesk-capstone-taskmatrix

Designated Track

Full-Stack MERN Development

Project Type

Enterprise Agile Project Management Application

Capstone Duration

4 Weeks

Current Phase

Product Planning, System Architecture, and UI/UX Design

Priority

P0 MVP, P1 Enterprise Features, P2 Stretch Goals

Table of Contents

Project Overview

Problem Statement

Product Goals

Target Users

User Roles

Core User Flows

Technology Stack

Feature Priorities

UI/UX Wireframes

System Architecture

Planned Database Collections

Frontend State Structure

Mock API Endpoints

Security Requirements

Validation and Error Handling

Testing Strategy

Deployment Plan

Proposed Repository Structure

Four-Week Roadmap

MVP Acceptance Criteria

Future Enhancements

Author

Project Overview

TaskMatrix will allow teams to:

Create and manage workspaces.

Create multiple projects inside a workspace.

Add members and assign workspace roles.

Create Kanban boards and workflow columns.

Create, update, move, assign, and delete tasks.

Add priorities, labels, deadlines, comments, and attachments.

Track project progress through dashboards and activity feeds.

Receive notifications for important project events.

Collaborate through real-time updates.

The application will be built as a full-stack MERN application with a responsive React frontend, REST API, MongoDB database, secure authentication, authorization, and production deployment.

Problem Statement

Teams often manage work through disconnected tools such as spreadsheets, chats, notes, and emails. This creates several problems:

Tasks are difficult to track.

Responsibilities are unclear.

Deadlines are missed.

Team members cannot easily see project progress.

Important project activity is scattered across different platforms.

Managers lack a single dashboard for monitoring work.

TaskMatrix solves these problems by providing one platform for project planning, task execution, team collaboration, and project visibility.

Product Goals

Primary Goals

Provide a centralized project and task management system.

Support team collaboration through shared workspaces.

Allow users to organize work visually through Kanban boards.

Provide role-based permissions for secure collaboration.

Make project progress visible through analytics and activity tracking.

Deliver a responsive and accessible interface.

Deploy the application as a production-ready full-stack system.

Non-Goals for the Initial MVP

The first release will not attempt to include:

Payroll or employee management.

Full video-conferencing functionality.

Advanced enterprise billing.

Native mobile applications.

Artificial intelligence task generation.

Complex time-sheet and invoicing systems.

These may be considered after the core product is stable.

Target Users

TaskMatrix is designed for:

Software development teams

Internship teams

Project managers

Product managers

Designers

Marketing teams

Small companies

Student teams

Freelancers working with clients

User Roles

Workspace Owner

The workspace owner can:

Update workspace information.

Add or remove members.

Assign member roles.

Create and delete projects.

View all workspace activity.

Delete the workspace.

Workspace Admin

An admin can:

Manage members.

Create and update projects.

Manage boards, columns, and tasks.

View workspace analytics.

Project Member

A project member can:

View assigned projects.

Create and update tasks where permitted.

Move tasks between columns.

Add comments and attachments.

View project activity.

Viewer

A viewer can:

View projects and tasks.

View project progress.

View comments and activity.

Cannot modify protected project data.

Core User Flows

Authentication Flow

User opens the application.

User registers or logs in.

Server validates credentials.

User receives a secure authenticated session.

User is redirected to the dashboard.

Workspace Flow

User creates a workspace.

User becomes the workspace owner.

User invites or adds members.

User assigns member roles.

Members access workspace projects based on permissions.

Project Flow

Authorized user creates a project.

User configures project name, description, status, and dates.

A default board is created.

Default workflow columns are created.

Team members begin adding and assigning tasks.

Task Flow

User creates a task.

User adds title, description, priority, status, assignee, labels, and deadline.

Task appears inside a board column.

Task can be moved using drag-and-drop.

Team members can comment and update the task.

Changes are recorded in the activity log.

Technology Stack

Frontend

React

Vite

React Router

Zustand

Axios

Tailwind CSS

React Hook Form

Zod

DnD Kit

Socket.IO Client

Backend

Node.js

Express.js

MongoDB

Mongoose

JSON Web Token authentication

bcrypt

Cookie Parser

CORS

Helmet

Morgan

Express Rate Limit

Socket.IO

Multer

Cloudinary

Testing

Vitest

React Testing Library

Supertest

Postman

Design and Architecture

Figma

Draw.io

MongoDB data-model planning

State-tree planning

Development and Deployment

Git

GitHub

ESLint

Prettier

Vercel for frontend deployment

Node-compatible cloud hosting for backend deployment

MongoDB Atlas for database hosting

Cloudinary for file storage

Feature Priorities

P0 — Mandatory MVP Features

The following features are required for the minimum functional product.

Authentication and User Management

User registration

User login

User logout

Secure password hashing

Authenticated user profile

Update user profile

Protected frontend routes

Protected backend routes

Workspace Management

Create workspace

View user workspaces

View workspace details

Update workspace

Delete workspace

Add workspace members

Remove workspace members

Assign member roles

Project Management

Create project

View workspace projects

View project details

Update project

Delete project

Set project status

Set project start and due dates

Board and Column Management

Create project board

View project board

Create workflow columns

Rename workflow columns

Reorder workflow columns

Delete workflow columns

Task Management

Create task

View task details

Update task

Delete task

Assign task to a user

Set task priority

Set task deadline

Set task labels

Move tasks between columns

Reorder tasks inside a column

Authorization and Reliability

Role-based access control

Request validation

Centralized error handling

Loading states

Empty states

Responsive user interface

Production deployment

P1 — Priority Enterprise Features

Drag-and-drop Kanban interaction

Task comments

Task activity timeline

Project search

Task search

Priority filters

Assignee filters

Status filters

Project dashboard analytics

Workspace member management

User profile image

Task labels

Due-date reminders

Notification center

Light and dark mode

Pagination

Sorting

Mobile-responsive navigation

P2 — Stretch Goals and Optimization

Real-time board synchronization with Socket.IO

Real-time notifications

File attachments

Email workspace invitations

Password reset flow

Project audit logs

Export project report

Project archive functionality

Automated frontend tests

Automated backend tests

API rate limiting

Database indexing

Optimistic UI updates

Advanced dashboard charts

Progressive Web App support

Docker configuration

Continuous integration workflow

UI/UX Wireframes

A minimum of three core viewports will be created in Figma.

Planned Screens

Authentication Screen

Main Dashboard

Project Kanban Board

Task Details Modal or Page

Workspace Members Screen

Project Analytics Screen

Figma Link

Replace the placeholder below after publishing the Figma file.

Public Figma File: ADD_PUBLIC_FIGMA_LINK_HERE

Design Principles

Clear visual hierarchy

Consistent spacing

Responsive layouts

Accessible contrast

Reusable components

Visible loading and error states

Simple navigation

Minimal user effort for common actions

System Architecture

TaskMatrix will use a client-server architecture.

React Client
     |
     | HTTPS / REST / WebSocket
     |
Express API Server
     |
     | Mongoose
     |
MongoDB Atlas

Additional Services:
- Cloudinary for file uploads
- Socket.IO for real-time updates
- Email service for invitations and password reset

Request Flow

The React frontend sends an HTTP request through Axios.

Express receives the request.

Middleware validates authentication, authorization, and request data.

A controller calls the required service or database operation.

Mongoose communicates with MongoDB.

The API returns a structured JSON response.

Zustand updates the frontend state.

React updates the interface.

Architecture Diagrams

The exported architecture diagrams will be stored inside the docs directory.

MongoDB Entity Relationship Diagram

![TaskMatrix ERD](./docs/taskmatrix-erd.png)

After adding the exported file, the diagram will appear below:



Frontend State Tree Diagram

![TaskMatrix State Tree](./docs/taskmatrix-state-tree.png)

After adding the exported file, the diagram will appear below:



Planned Database Collections

User

{
  name: String,
  email: String,
  passwordHash: String,
  avatar: String,
  jobTitle: String,
  createdAt: Date,
  updatedAt: Date
}

Workspace

{
  name: String,
  description: String,
  owner: ObjectId,
  logo: String,
  createdAt: Date,
  updatedAt: Date
}

Membership

{
  workspace: ObjectId,
  user: ObjectId,
  role: "owner" | "admin" | "member" | "viewer",
  joinedAt: Date
}

Project

{
  workspace: ObjectId,
  name: String,
  description: String,
  status: "planning" | "active" | "completed" | "archived",
  createdBy: ObjectId,
  members: [ObjectId],
  startDate: Date,
  dueDate: Date,
  createdAt: Date,
  updatedAt: Date
}

Board

{
  project: ObjectId,
  name: String,
  createdAt: Date,
  updatedAt: Date
}

Column

{
  board: ObjectId,
  name: String,
  position: Number,
  createdAt: Date,
  updatedAt: Date
}

Task

{
  project: ObjectId,
  board: ObjectId,
  column: ObjectId,
  title: String,
  description: String,
  priority: "low" | "medium" | "high" | "urgent",
  assignees: [ObjectId],
  labels: [String],
  dueDate: Date,
  position: Number,
  createdBy: ObjectId,
  createdAt: Date,
  updatedAt: Date
}

Comment

{
  task: ObjectId,
  author: ObjectId,
  content: String,
  createdAt: Date,
  updatedAt: Date
}

Activity

{
  workspace: ObjectId,
  project: ObjectId,
  task: ObjectId,
  actor: ObjectId,
  action: String,
  metadata: Object,
  createdAt: Date
}

Notification

{
  recipient: ObjectId,
  type: String,
  title: String,
  message: String,
  link: String,
  isRead: Boolean,
  createdAt: Date
}

Collection Relationships

User ──< Membership >── Workspace
Workspace ──< Project
Project ──< Board
Board ──< Column
Project ──< Task
Column ──< Task
Task ──< Comment
User ──< Comment
Project ──< Activity
User ──< Notification

Frontend State Structure

The global state will be divided into focused Zustand stores.

Global State
│
├── authStore
│   ├── user
│   ├── isAuthenticated
│   ├── isLoading
│   ├── login()
│   ├── register()
│   ├── logout()
│   └── getCurrentUser()
│
├── workspaceStore
│   ├── workspaces
│   ├── activeWorkspace
│   ├── workspaceMembers
│   ├── fetchWorkspaces()
│   ├── createWorkspace()
│   └── updateWorkspace()
│
├── projectStore
│   ├── projects
│   ├── activeProject
│   ├── projectFilters
│   ├── fetchProjects()
│   ├── createProject()
│   └── updateProject()
│
├── boardStore
│   ├── board
│   ├── columns
│   ├── tasks
│   ├── selectedTask
│   ├── fetchBoard()
│   ├── createTask()
│   ├── updateTask()
│   └── moveTask()
│
├── notificationStore
│   ├── notifications
│   ├── unreadCount
│   ├── fetchNotifications()
│   └── markAsRead()
│
└── uiStore
    ├── sidebarOpen
    ├── activeModal
    ├── theme
    ├── globalSearch
    └── toggleSidebar()

Local component state will be used for temporary UI data such as:

Form values

Dropdown state

Modal animation state

Hover state

Temporary validation messages

Mock API Endpoints

All planned API routes will use the /api prefix.

Authentication

Method

Endpoint

Purpose

POST

/api/auth/register

Register a new user

POST

/api/auth/login

Log in a user

POST

/api/auth/logout

Log out the current user

GET

/api/auth/me

Get authenticated user

PATCH

/api/auth/profile

Update user profile

POST

/api/auth/forgot-password

Request password reset

POST

/api/auth/reset-password

Reset user password

Workspaces

Method

Endpoint

Purpose

GET

/api/workspaces

Get user workspaces

POST

/api/workspaces

Create workspace

GET

/api/workspaces/:workspaceId

Get workspace

PATCH

/api/workspaces/:workspaceId

Update workspace

DELETE

/api/workspaces/:workspaceId

Delete workspace

Workspace Members

Method

Endpoint

Purpose

GET

/api/workspaces/:workspaceId/members

Get members

POST

/api/workspaces/:workspaceId/members

Add or invite member

PATCH

/api/workspaces/:workspaceId/members/:memberId

Update member role

DELETE

/api/workspaces/:workspaceId/members/:memberId

Remove member

Projects

Method

Endpoint

Purpose

GET

/api/workspaces/:workspaceId/projects

Get workspace projects

POST

/api/workspaces/:workspaceId/projects

Create project

GET

/api/projects/:projectId

Get project

PATCH

/api/projects/:projectId

Update project

DELETE

/api/projects/:projectId

Delete project

Boards and Columns

Method

Endpoint

Purpose

GET

/api/projects/:projectId/board

Get project board

POST

/api/projects/:projectId/columns

Create column

PATCH

/api/columns/:columnId

Update column

PATCH

/api/columns/reorder

Reorder columns

DELETE

/api/columns/:columnId

Delete column

Tasks

Method

Endpoint

Purpose

GET

/api/projects/:projectId/tasks

Get project tasks

POST

/api/projects/:projectId/tasks

Create task

GET

/api/tasks/:taskId

Get task

PATCH

/api/tasks/:taskId

Update task

DELETE

/api/tasks/:taskId

Delete task

PATCH

/api/tasks/:taskId/move

Move or reorder task

POST

/api/tasks/:taskId/attachments

Add attachment

DELETE

/api/tasks/:taskId/attachments/:attachmentId

Delete attachment

Comments

Method

Endpoint

Purpose

GET

/api/tasks/:taskId/comments

Get task comments

POST

/api/tasks/:taskId/comments

Create comment

PATCH

/api/comments/:commentId

Update comment

DELETE

/api/comments/:commentId

Delete comment

Activity and Notifications

Method

Endpoint

Purpose

GET

/api/projects/:projectId/activities

Get project activity

GET

/api/notifications

Get user notifications

PATCH

/api/notifications/:notificationId/read

Mark notification as read

PATCH

/api/notifications/read-all

Mark all notifications as read

Analytics

Method

Endpoint

Purpose

GET

/api/workspaces/:workspaceId/analytics

Get workspace analytics

GET

/api/projects/:projectId/analytics

Get project analytics

Standard API Response Format

Successful Response

{
  "success": true,
  "message": "Operation completed successfully.",
  "data": {}
}

Error Response

{
  "success": false,
  "message": "A clear error message.",
  "errors": []
}

Security Requirements

Hash passwords using bcrypt.

Never return password hashes in API responses.

Store authentication tokens securely.

Protect private routes.

Apply role-based authorization.

Validate request bodies.

Sanitize user-generated content.

Configure CORS correctly.

Use Helmet for secure HTTP headers.

Add rate limiting to sensitive endpoints.

Restrict file types and upload sizes.

Store secrets in environment variables.

Never commit .env files.

Validate MongoDB ObjectIds.

Use generic authentication error messages where appropriate.

Validation and Error Handling

Frontend Validation

Required field validation

Email format validation

Password strength validation

Character limits

Date validation

File-type validation

File-size validation

Backend Validation

Request-body validation

Route-parameter validation

Query-parameter validation

Permission validation

Duplicate-data handling

Resource-not-found handling

Error Handling

The backend will use centralized error middleware for:

Validation errors

Authentication errors

Authorization errors

Duplicate-key errors

Invalid ObjectIds

Missing resources

Upload errors

Unexpected server errors

Testing Strategy

Frontend Tests

Component rendering tests

Form validation tests

Authentication-flow tests

Store-action tests

Board interaction tests

Empty, loading, and error-state tests

Backend Tests

Authentication endpoint tests

Workspace CRUD tests

Project CRUD tests

Task CRUD tests

Permission tests

Validation tests

Error middleware tests

Manual Tests

Responsive design checks

Browser compatibility

Drag-and-drop behavior

Authentication persistence

Unauthorized access attempts

File upload validation

Production API connectivity

Deployment Plan

Frontend

The React frontend will be deployed using Vercel.

Backend

The Express backend will be deployed using a Node-compatible cloud platform.

Database

MongoDB Atlas will host the production database.

File Storage

Cloudinary will store uploaded images and attachments.

Required Environment Variables

NODE_ENV=
PORT=
CLIENT_URL=
MONGODB_URI=
JWT_SECRET=
JWT_EXPIRES_IN=
COOKIE_EXPIRES_IN=
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
EMAIL_HOST=
EMAIL_PORT=
EMAIL_USER=
EMAIL_PASSWORD=

The actual values must never be committed to GitHub.

Proposed Repository Structure

prodesk-capstone-taskmatrix/
│
├── client/
│   ├── public/
│   └── src/
│       ├── api/
│       ├── assets/
│       ├── components/
│       ├── features/
│       ├── hooks/
│       ├── layouts/
│       ├── pages/
│       ├── routes/
│       ├── stores/
│       ├── utils/
│       ├── App.jsx
│       └── main.jsx
│
├── server/
│   └── src/
│       ├── config/
│       ├── controllers/
│       ├── middleware/
│       ├── models/
│       ├── routes/
│       ├── services/
│       ├── sockets/
│       ├── utils/
│       ├── app.js
│       └── server.js
│
├── docs/
│   ├── taskmatrix-erd.png
│   ├── taskmatrix-state-tree.png
│   └── wireframes/
│
├── .env.example
├── .gitignore
├── README.md
└── LICENSE

Four-Week Roadmap

Week 1 — Planning and Foundation

Finalize product requirements

Create Figma wireframes

Create MongoDB ERD

Create frontend state-tree diagram

Define API endpoints

Initialize frontend and backend

Configure linting and formatting

Configure database connection

Week 2 — Authentication and Core Data

Build registration and login

Build protected routes

Build user profile

Build workspace CRUD

Build membership and roles

Build project CRUD

Week 3 — Board and Task Management

Build boards and columns

Build task CRUD

Add task assignment

Add priorities, labels, and deadlines

Add drag-and-drop

Add comments

Add filters and search

Week 4 — Enterprise Features and Deployment

Add notifications

Add activity logs

Add analytics

Add real-time updates if time permits

Add tests

Fix responsive issues

Optimize API and database queries

Deploy frontend and backend

Complete final documentation

MVP Acceptance Criteria

The MVP will be considered complete when:

A user can register, log in, and log out.

An authenticated user can create a workspace.

A workspace owner can add members and assign roles.

Authorized users can create projects.

Every project can display a Kanban board.

Users can create, edit, move, and delete tasks.

Tasks can be assigned to members.

Tasks can contain priority and deadline information.

Unauthorized users cannot access protected resources.

The application shows loading, error, and empty states.

The application works on desktop and mobile screen sizes.

Frontend and backend are deployed.

The deployed frontend communicates successfully with the deployed API.

The production database stores application data.

The README contains setup and architecture documentation.

Future Enhancements

After the capstone MVP, TaskMatrix may be expanded with:

Calendar view

Timeline or Gantt view

Recurring tasks

Custom workflow templates

Team workload reports

Time tracking

Client guest accounts

Advanced audit logs

Integrations with GitHub, Slack, and Google Calendar

AI-assisted task descriptions

Native mobile applications

Current Project Status

Planning Phase

The current sprint is dedicated to:

Product planning

Feature prioritization

System architecture

Database design

Frontend state planning

API planning

UI/UX wireframes

Application development will begin after the planning deliverables are completed.

Author

Mohit Korodiya

Capstone Project for Prodesk IT Internship

License

No license has been selected at this stage.
