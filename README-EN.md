# 🧭 AL-tatweer Projects Workflow & Management Plan

## 1. 📝 Project Documentation

Before starting any software project, a full **Project Document** must be created. It should include:

- General project description
- Main objectives
- Target audience
- Platforms (Web, Android, iOS, etc.)
- Functional and non-functional requirements
- Expected integrations (APIs, DBs, third-party services...)
- Possible challenges
- Initial timeline

### 1.1 Team Assignment

- **Lead Developer**: Primary technical authority on the project
- **Project Coordinator**: Responsible for task follow-ups, team communication, and schedule tracking
- **Database Engineer**: Designs and implements the project’s database and relationships
- **Developers**: Assigned based on specialty (Frontend, Backend, Mobile, etc.)

---

## 2. 🎯 Creating Milestones and Task Breakdown

- Create a list of project **Milestones** that represent the major stages
- Under each milestone, define all relevant **Tasks**

Each task should include:

- Task name
- Brief description
- Assigned developer
- Estimated duration
- Deadline

> **Note:** If there's disagreement on task duration, the Lead Developer will provide an estimated time based on expertise.

---

## 3. 🛠️ GitHub Repository Setup & Branch Strategy

### 3.1 Creating the Repository

- A dedicated **GitHub repository** must be created for every project.

### 3.2 Branch Organization (Based on Git Flow)

| Branch        | Description                                              |
| ------------- | -------------------------------------------------------- |
| `main`        | Stable, production-ready version                         |
| `develop`     | Ongoing development branch                               |
| `feature/xyz` | Feature-specific branches (e.g., `feature/products-api`) |
| `bugfix/xyz`  | For fixing bugs during development                       |
| `hotfix/xyz`  | For urgent fixes on the live version                     |
| `release/xyz` | Preparing a new release                                  |

### 3.3 GitHub Roles and Permissions

- **Lead Developer**: Primary owner of the repository

  - Reviews all Pull Requests
  - Ensures code quality and consistency
  - Blocks merging of poor-quality code

- **Project Coordinator**: Also has full access to monitor and organize the repository

> **Merge Policy**: No code may be merged into `develop` or `main` without approval from the Lead Developer.

---

## 4. 📢 Project Kickoff & Task Assignment

- Hold a **kickoff meeting** to explain the entire project to the team
- Break the system into modules and explain each part
- Assign specific tasks to relevant developers
- Define deadlines for each task and record any known risks or blockers

---

## 5. 📁 Documentation via `docs/` Folder

- A `docs/` folder must exist in every project
- When a developer starts work on a task/module, they must create a **Markdown file (`.md`)** named after the module (e.g., `products.md`)
- The file should include:

  - Tasks completed
  - Challenges faced
  - Technical notes or decisions
  - Documentation of API endpoints, models, or database schemas

> **A reference link for documentation format will be added later.**

---

## ✅ General Best Practices

- Follow a consistent **code style guide**
- Use the company's system to track tasks.
- Document every technical decision or change
- Conduct weekly progress meetings
- Enforce **code reviews** for all Pull Requests
- Use clear and conventional commit messages (e.g., `feat: add login API`, `fix: crash on null value`)
