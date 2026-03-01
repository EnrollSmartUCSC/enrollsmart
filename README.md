# Enroll Smart

> A one-stop enrollment solution for UCSC students.

Enroll Smart simplifies the course enrollment experience at UC Santa Cruz. Students can plan their degree, browse the course catalog, check class offerings, read peer reviews, and get notified when seats open up in high-demand courses — all in one place.

---

## Features

- **Course Search** — Look up descriptions, prerequisites, and offerings for any course.
- **Pinning** — Save courses you're interested in for quick access later.
- **Degree Planner** — Schedule courses by quarter using a drag-and-drop interface to map out your full degree plan.
- **Watchlist** — Add a course to your watchlist for a specific quarter and get notified when spots become available.
- **Real-Time Notifications** — Track class status and receive updates on open seats during peak enrollment season.

---

## Architecture

This repository uses Git submodules for the frontend and backend. Clone with:

```bash
git clone --recurse-submodules https://github.com/EnrollSmartUCSC/<repo-name>
```

Or, if already cloned:

```bash
git submodule update --init --recursive
```

---

### Backend

**Repository:** [EnrollSmartUCSC/backend](https://github.com/EnrollSmartUCSC/backend)

The backend is a Python/Flask REST API that handles course data, user watchlists, and notifications.

#### Hosting

- **API Server:** AWS EC2 instance
- **Database:** AWS RDS (PostgreSQL)

#### Setup

```bash
cd backend

# Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip3 install -r requirements.txt
```

#### Dependencies

| Package | Purpose |
|---|---|
| `Flask` | Web framework |
| `flask-cors` | Cross-origin request handling |
| `firebase-admin` | Firebase integration (auth/notifications) |
| `requests` | HTTP client |
| `psycopg2` | PostgreSQL adapter |
| `python-dotenv` | Environment variable management |
| `flasgger` | Swagger/OpenAPI documentation |
| `beautifulsoup4` | Web scraping for course data |
| `regex` | Extended regular expressions |

---

### Frontend

**Repository:** [EnrollSmartUCSC/frontend](https://github.com/EnrollSmartUCSC/frontend)

The frontend is a Next.js application with a rich UI built on MUI and Radix UI components, featuring drag-and-drop course planning powered by dnd-kit.

#### Hosting

- **Platform:** AWS Amplify
- **Domain:** Managed via [name.com](https://name.com)

#### Setup

```bash
cd frontend
npm install
npm run dev
```

#### Dependencies

| Package | Purpose |
|---|---|
| `next` | React framework (SSR/SSG) |
| `react` / `react-dom` | UI library |
| `next-auth` | Authentication |
| `firebase` | Client-side Firebase SDK |
| `@dnd-kit/core` | Drag-and-drop for degree planner |
| `@mui/material` / `@mui/icons-material` | Material UI components |
| `@emotion/react` / `@emotion/styled` | CSS-in-JS (MUI dependency) |
| `@radix-ui/react-*` | Accessible UI primitives (scroll area, select, tabs, switch, slot) |
| `antd` | Ant Design component library |
| `lucide-react` | Icon set |
| `tailwind-merge` | Tailwind class merging utility |
| `clsx` | Conditional class names |
| `class-variance-authority` | Component variant management |

---

## Contributing

1. Fork the repository and clone with submodules.
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make your changes in the appropriate submodule (`frontend/` or `backend/`).
4. Commit and push your branch, then open a pull request.

---

## License

This project is maintained by the EnrollSmart team at UCSC.
