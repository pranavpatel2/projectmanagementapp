# Project Management App

## Overview
This project is a **Task Management and Collaboration Tool** built using the **T3 Stack**. It provides an intuitive interface for task creation, assignment, and tracking, alongside user profile management and project settings.

## Tech Stack
- **Frontend:** Next.js (T3 Stack), TypeScript, Tailwind CSS
- **Backend:** Serverless API using **SST (Serverless Stack)**, tRPC
- **Database:** Supabase (PostgreSQL)
- **Authentication:** NextAuth.js
- **ORM:** Prisma
- **State Management:** React Hooks & tRPC
- **Deployment:** AWS using SST & Vercel (Temporary Deployment)

## Features
### 1. Task Management
- Create, assign, and track tasks
- Set deadlines, priorities, and tags
- Add detailed task descriptions
- Assign tasks to team members

### 2. User Profiles & Project Settings
- Users can manage personal profiles
- Project managers can configure project settings

### 3. Dashboard (Optional)
- Overview of tasks, deadlines, and progress
- Project timelines and analytics

### 4. Authentication
- Email & Password login using **Supabase Auth**
- OAuth with providers via NextAuth.js

## Installation
### Prerequisites
Ensure you have the following installed:
- Node.js (>= 18.x)
- PostgreSQL (via Supabase)
- AWS CLI (for SST deployment)

### Clone the repository
```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/ProjectManagementApp.git
cd ProjectManagementApp
```

### Install Dependencies
```bash
npm install
```

### Set Up Environment Variables
Create a `.env` file and add the necessary credentials.
```env
NEXTAUTH_SECRET=your_secret
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_anon_key
AWS_REGION=your_aws_region
```

### Run the Application
```bash
npm run dev
```

## Deployment
### Deploying with SST (Future Implementation)
```bash
npx sst deploy
```

### Temporary Deployment (Vercel)
Due to ongoing work on SST integration, the project is currently deployed on Vercel.

## Testing
Unit tests are included for key functionalities using **Vitest**.
Run tests using:
```bash
npm run test
```

## API Endpoints (tRPC)
### Project Endpoints
- `project.getAllProjects` - Fetch all projects
- `project.createProject` - Create a new project
- `project.updateProject` - Update an existing project
- `project.deleteProject` - Delete a project

### Task Endpoints
- `task.createTask` - Create a new task
- `task.getTasksByProject` - Fetch tasks for a project
- `task.updateTask` - Update a task
- `task.deleteTask` - Delete a task

## Folder Structure
```
.
├── src
│   ├── pages (Frontend pages)
│   ├── components (Reusable UI components)
│   ├── server
│   │   ├── api (Backend logic using tRPC)
│   │   ├── db (Prisma ORM setup)
│   ├── utils (Helper functions, hooks)
│   ├── styles (Global styles)
├── __tests__ (Unit tests)
├── .env (Environment variables)
├── package.json
├── README.md
```

## Future Improvements
- Advanced analytics on task completion trends
- Real-time updates using WebSockets
- Mobile-friendly UI enhancements
- Role-based access control
- Email verification during sign-up using **Supabase Magic Link**
- Forgot password functionality
- **Full Integration of SST** once development progresses

## Contributors
- **Your Name** - [GitHub Profile](https://github.com/YOUR_GITHUB_USERNAME)

## License
This project is licensed under the MIT License.

