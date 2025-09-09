
# To‑Do Manager (Flask + SQLite)

A clean, beginner‑friendly CRUD app with a bonus **Smart Generate** feature.
- Create, read, update, delete tasks
- Status (pending/done)
- **Quick Suggestion**: adds a random productivity task


---

## 1) Tech Stack
- Python 3.8+
- Flask (web)
- SQLite (built‑in)

## 2) Folder Structure
```text
todo_manager_flask/
├─ app/
│  ├─ __init__.py        
│  ├─ models.py         
│  ├─ routes.py         
│  ├─ ai.py              
│  ├─ templates/
│  │  ├─ base.html
│  │  └─ index.html
│  └─ static/
│     └─ css/
│        └─ styles.css
├─ instance/            
├─ run.py                
├─ requirements.txt     
└─ README.md
```

## 3) How to Run (Step‑by‑Step, No Hiccups)

### A. Windows (PowerShell)
```powershell
cd todo_manager_flask
py -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python run.py
```
Open http://127.0.0.1:5000 in your browser.


```


### Optional: Enable real OpenAI generation
1) Install the OpenAI package:
```bash
pip install openai
```

## 4) Features Implemented
- CRUD: Add, view, update (title/description/status), delete tasks
- List sorted by newest first
- Quick Suggestion (one‑click useful task)
- Smart Generate (N tasks from your goal) with AI fallback
- Bootstrap 5 styling

## 5) Notes
- The SQLite database file lives at `instance/todo.db` and is created automatically.
- No migrations needed. Delete `instance/todo.db` to reset data.
- For production, set a real `SECRET_KEY` in `app/__init__.py` or via env var.





# Overview

This is a full-stack web application for Iron Lady, a women's leadership development organization. The application features an AI-powered chatbot that helps users learn about Iron Lady's leadership programs and provides guidance. The system combines a React frontend with an Express.js backend, using modern web technologies and UI components.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture
Tech Stack : React with TypeScript using Vite for build tooling and Node 
## Frontend Architecture
- **Framework**: React with TypeScript using Vite for build tooling
- **UI Library**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Component Structure**: Organized into reusable UI components and feature-specific components

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful API endpoints for chat functionality
- **Session Management**: UUID-based chat sessions
- **Storage Pattern**: Interface-based storage with in-memory implementation (MemStorage)
- **Development Setup**: Integrated Vite development server with hot module replacement

## Data Layer
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Schema Management**: Drizzle Kit for migrations and schema management
- **Database Provider**: Neon serverless PostgreSQL
- **Current Implementation**: In-memory storage for development with database schema ready for production

## Key Features
- **Chat Interface**: Real-time messaging with AI-powered responses
- **Program Information**: Dedicated sidebar showcasing Iron Lady's three main programs
- **Responsive Design**: Mobile-first approach with adaptive layouts
- **Session Management**: Persistent chat sessions with message history
- **TypeScript Safety**: Shared types between frontend and backend

## AI Integration
- **Service**: OpenAI GPT integration with knowledge base fallback
- **Knowledge Base**: Static information about Iron Lady programs and mentors
- **Response Strategy**: Hybrid approach using local knowledge base for quick responses and OpenAI for complex queries
- **Context Awareness**: Conversation history maintained for contextual responses

# External Dependencies

## Core Technologies
- **Database**: Neon PostgreSQL serverless database
- **AI Service**: OpenAI API for chat responses
- **Build Tools**: Vite for frontend bundling and development server
- **Package Manager**: npm with lock file for consistent builds

## UI and Styling
- **Component Library**: Radix UI primitives for accessible components
- **Styling Framework**: Tailwind CSS for utility-first styling
- **Icons**: Lucide React for consistent iconography
- **Fonts**: Google Fonts (Inter, DM Sans, Geist Mono, etc.)

## Development Tools
- **Type Checking**: TypeScript for static type analysis
- **Database Tools**: Drizzle Kit for schema management and migrations
- **Development**: Replit-specific plugins for runtime error handling and debugging
- **Build Process**: ESBuild for server-side bundling in production

