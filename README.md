# CivicLoop 🌍
### From Community Voice to Real-World Action

CivicLoop is a community-powered civic problem reporting and accountability platform being developed for the **Renaissance Buildathon** by a team of three first-year college students.

Our goal is to help people report local problems, bring communities together around shared concerns, verify issues through supporting evidence, and make it easier to track responses from the relevant authorities.

Instead of letting complaints disappear in social media posts or group chats, CivicLoop aims to turn them into organized, evidence-backed, trackable issues.

---

## 💡 The Problem

People frequently encounter problems in their colleges, neighbourhoods, and cities, such as:

- Damaged roads and potholes.
- Improper garbage collection.
- Water supply disruptions.
- Broken streetlights.
- Unsafe public spaces.
- Poor college infrastructure.

However, information about these problems is often scattered across social media posts, messaging groups, and individual complaints.

People may not know whether an issue has already been reported, how many others are affected, whether supporting evidence exists, or whether anyone is taking action.

## 🚀 Our Solution

CivicLoop brings community reporting, public support, evidence review, and issue tracking into one platform.

Users can report problems, discover issues affecting their local area, support relevant reports, and follow their progress. Moderators can review submitted evidence, while authorized authority users can acknowledge issues, respond to concerns, and update their status.

Our vision is simple:

**Turn individual complaints into collective awareness and accountable action.**

---

## ✨ Planned Features

> Development is being carried out in phases. Features listed here represent the project scope and may not all be implemented yet.

### 👥 1. Community Platform
- Create and browse problem reports.
- Add descriptions, categories, locations, and supporting evidence.
- Support relevant issues.
- Comment on reports and contribute useful information.
- View issue details and progress.

### 📍 2. PIN-Code-Based Issue Discovery
- Browse problems associated with a selected Indian PIN code.
- Search for issues using a six-digit PIN code.
- Search by locality or city name.
- Filter issues by category and status.
- Display the PIN code and locality on issue cards.
- Explore problems in other areas without needing precise device location.

### 🔎 3. Evidence and Verification
- Distinguish submitted reports from verified issues.
- Allow authorized moderators to review evidence.
- Track verification status.
- Help users distinguish evidence quality from popularity.

Community support alone does not establish that a report is genuine.

### 🏛️ 4. Authority Dashboard
- View reported issues.
- Review issue details, public support, evidence status, and priority.
- Acknowledge reports and provide responses.
- Update issue progress.
- Maintain a public history of important status changes.

### 🔐 5. Authentication and Access Control
- User registration and login.
- Logout and session handling.
- Separate community, moderator, and authority roles.
- Backend-enforced permissions for restricted actions.

### 📊 6. Issue Tracking and Prioritization
- Track issues from submission to resolution.
- Display severity separately from support count.
- Use transparent prototype rules for issue priority.
- Show progress updates and resolution information.

---

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Backend | Python, FastAPI |
| API validation | Pydantic |
| Database | SQLite |
| Database ORM | SQLAlchemy |
| Development server | Uvicorn |
| API testing | FastAPI Swagger UI |
| Code editor | Visual Studio Code |
| Version control | Git and GitHub |

We have deliberately selected a beginner-friendly stack that allows us to build a working prototype without unnecessary architectural complexity.

### Architecture

The application will use three separate frontend workstreams connected to one shared backend and database.

- **User frontend:** Reporting, browsing, location search, support, and comments.
- **Authority frontend:** Issue review, responses, and progress management.
- **Authentication frontend:** Registration, login, logout, and role-aware navigation.
- **Shared backend:** APIs, validation, authentication, authorization, and business logic.
- **Shared database:** Users, issues, locations, comments, support records, and status history.

---

## 📂 Planned Project Structure

The final structure will follow the existing repository and may be adjusted as development progresses.

```text
civicloop/
├── frontend/
│   ├── user/
│   │   ├── index.html
│   │   ├── issue.html
│   │   ├── css/
│   │   └── js/
│   ├── authority/
│   │   ├── index.html
│   │   ├── issue-detail.html
│   │   ├── css/
│   │   └── js/
│   ├── auth/
│   │   ├── login.html
│   │   ├── register.html
│   │   ├── css/
│   │   └── js/
│   └── shared/
│       ├── css/
│       └── js/
├── backend/
│   ├── main.py
│   ├── database.py
│   ├── models/
│   ├── schemas/
│   ├── routes/
│   └── services/
├── tests/
├── docs/
│   └── API_CONTRACT.md
├── requirements.txt
├── README.md
└── PROJECT_ROADMAP.md
```

---

## ⚙️ Getting Started

### Prerequisites

Install the following before running the application:

- Python 3.11 or a compatible version supported by the project dependencies.
- Visual Studio Code.
- Git.
- A web browser.

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd civicloop
```

Replace the placeholder with your actual GitHub repository URL.

### 2. Create a virtual environment

**Windows:**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, you can use Command Prompt instead:

```bat
.venv\Scripts\activate.bat
```

**macOS/Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

After the backend and `requirements.txt` have been created:

```bash
pip install -r requirements.txt
```

### 4. Start the backend

From the repository root, after the backend entry point is available:

```bash
uvicorn backend.main:app --reload
```

If the final repository uses a different Python module path, follow the instructions in the backend setup documentation.

### 5. Open API documentation

Once the backend is running, open:

[http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

FastAPI's interactive documentation can be used to inspect and test the implemented API endpoints.

### 6. Run the frontend

The frontend will be served using the development setup documented by the project. Follow the final instructions for the configured static-file server and API URL.

**Note:** These are setup instructions for the planned architecture. They will become fully applicable once the corresponding files and application entry points are implemented.

---

## 🗺️ Development Roadmap

We are developing CivicLoop incrementally, with a focus on building a reliable core before adding complexity.

- [ ] **Phase 0:** Repository inspection and architecture planning.
- [ ] **Phase 1:** Shared backend, database, and API contracts.
- [ ] **Phase 2A:** User frontend.
- [ ] **Phase 2B:** Authority frontend.
- [ ] **Phase 2C:** Authentication frontend.
- [ ] **Phase 3:** Integration of all three frontends.
- [ ] **Phase 4:** Verification, authority responses, and accountability workflows.
- [ ] **Phase 5:** Testing, documentation, and buildathon presentation.

The three frontend workstreams are intended to progress in parallel after the shared architecture and API contracts are approved.

---

## 👨‍💻 Team Workflow

We are a team of three first-year college students collaborating on CivicLoop.

Our planned responsibilities are:

| Workstream | Responsibility |
|---|---|
| Teammate 1 | User frontend and community issue discovery |
| Teammate 2 | Authority dashboard and progress management |
| Teammate 3 | Authentication frontend and session handling |

All team members will collaborate on integration, testing, debugging, and the final presentation.

We use Git and GitHub to coordinate changes, review code, and preserve working versions of the application.

---

## 🔒 Privacy, Security, and Trust

CivicLoop is designed around responsible community participation.

Our implementation goals include:

- Backend-enforced authentication and role permissions.
- Secure password handling.
- Prevention of duplicate support records.
- Validation of submitted reports and PIN codes.
- Separation of public issue information from private account data.
- Clear distinction between unverified and verified reports.
- Transparent status updates and documented prototype limitations.

CivicLoop is a prototype, not an official government grievance portal. Unless an actual integration confirms delivery, reports displayed in the application should not be represented as having reached a real authority.

The platform is not intended to replace emergency services.

---

## 🎯 Our Buildathon Goal

Our objective for Renaissance is to demonstrate a working end-to-end prototype that connects:

**Report → Community Support → Evidence Review → Authority Response → Progress Tracking**

We aim to demonstrate not just a website, but a practical approach to improving local awareness, community participation, and accountability.

---

## 🔮 Future Possibilities

After the core prototype is working, potential future improvements include:

- Interactive issue maps.
- Duplicate report detection.
- Notifications for updates in selected areas.
- Better tools for organizing and comparing local issues.
- Verified integrations with relevant civic authorities.
- More advanced prioritization and analytics.

These are future possibilities, not promises of current functionality.

---

## 🤝 Contributing

This project is currently being developed by our buildathon team.

During development:

1. Discuss changes with the team.
2. Work on a dedicated feature branch.
3. Follow the approved architecture and API contracts.
4. Test changes before requesting integration.
5. Avoid modifying shared interfaces without coordination.

---

## 📄 License

A license has not yet been selected. Until one is added to the repository, all rights remain with the respective copyright holders.

---

**CivicLoop — Every concern deserves a voice. Every issue deserves accountability.**
