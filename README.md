
# MyDay AI

**One assistant. A clearer picture of your day. Better decisions, with you in control.**

MyDay AI is an AI-powered personal assistant designed to bring together information from the applications and services people already use.

Instead of switching between multiple applications to manage calendars, tasks, health, wellness and daily routines, users can interact with one intelligent assistant that consolidates information, provides personalised recommendations and helps manage everyday activities.

## The Problem

Our daily lives are spread across multiple applications. Calendar events, reminders, health information, workouts, meals, weather and personal responsibilities are often managed separately.

This creates fragmented information, missed reminders and unnecessary effort.

MyDay AI aims to bring these pieces together into one personalised daily experience.

## Product Vision

MyDay AI is an aggregator-first personal assistant.

It connects to supported external services, retrieves relevant information with user permission, interprets requests and provides a unified view of the user's day.

Existing applications remain the source of truth for their information. MyDay AI acts as the intelligence and interaction layer across them.

## Core Capabilities

### 1. Daily Intelligence
- Daily briefings covering schedules, appointments and reminders.
- Weather information.
- Travel and commute planning.
- Birthdays, anniversaries and important occasions.
- Daily priorities and pending actions.

### 2. Personal Productivity
- Task and reminder management.
- Carry-forward of incomplete activities.
- Priority recommendations.
- Suggested time slots for tasks and appointments.
- Assistance with approved actions.

### 3. Health and Wellness
- Consolidated health and activity information.
- Weight and activity trends.
- Workout planning and completion tracking.
- Personalised activity recommendations.
- Progress against user-defined goals.

### 4. Nutrition and Daily Routines
- Personalised meal recommendations.
- High-protein, lower-carbohydrate and other nutrition preferences.
- Meal reminders.
- Medication reminders based on user-entered schedules.
- Hydration reminders.
- Future meal planning and grocery integration.

### 5. Adaptive Intelligence
- Completion tracking for reminders and activities.
- Recognition of recurring patterns.
- Recommendations that adapt to user feedback and behaviour.
- Personalised suggestions based on availability, preferences and goals.

## Initial Integration Strategy

| Service | Intended use | Initial approach |
|---|---|---|
| Google Calendar | Meetings and appointments | First real integration, read-only |
| Health Connect | Health and activity information | Simulated connector |
| Weather service | Weather information | Mock data initially |
| Google Maps | Travel and commute planning | Mock data or navigation link |
| BigBasket | Grocery discovery and ordering | Future opportunity |

Additional health data sources may include Google Fit, Cult Fitness, Fitelo and Samsung Health, subject to supported integration access.

## Technology Stack

The project follows a free-first learning and development approach.

- **Frontend:** React and TypeScript
- **Backend:** Python and FastAPI
- **Database:** Supabase free tier or suitable alternative
- **AI:** Gemini API or another suitable free-tier model
- **APIs:** Google Calendar API
- **Design:** Figma
- **Development:** Visual Studio Code
- **Version Control:** Git and GitHub
- **API Testing:** Postman

Technology choices will be validated during development.

## Eight-Week Prototype Roadmap

| Week | Focus |
|---|---|
| 1 | Product foundation, requirements and backlog |
| 2 | UX/UI design and technical architecture |
| 3 | Frontend development |
| 4 | Backend development and data model |
| 5 | Google Calendar integration and simulated health connector |
| 6 | AI orchestration, recommendations and adaptive logic |
| 7 | Testing, security and refinement |
| 8 | Deployment, documentation and portfolio demonstration |

## Architecture Principles

- Aggregator-first, modular connector architecture.
- External services remain the source of truth.
- Permission-based access.
- Privacy and data minimisation.
- Source attribution and data freshness.
- AI-assisted recommendations with backend validation.
- User approval for consequential actions.
- Clear separation between real integrations and simulated data.

## Current Project Status

**Phase:** Product Definition and Foundation

- [x] Initial product vision and direction defined.
- [x] Product Requirements Document v1.2 prepared.
- [x] Git and GitHub repository established.
- [ ] Product backlog and acceptance criteria.
- [ ] UX/UI designs.
- [ ] Technical architecture.
- [ ] Frontend and backend development.
- [ ] External integration.
- [ ] AI orchestration and adaptive intelligence.
- [ ] Testing and deployment.

## Repository Structure

```text
MyDay AI/
│
├── 01_Product Management/
├── 02_UX_UI_Design/
├── 03_Technical_Architecture/
├── 04_Development/
├── 05_Testing_QA/
├── 06_Deployment/
├── 07_Learning_Journal/
└── README.md
```

## Project Objective

This project is an eight-week, hands-on prototype and learning initiative exploring product management, AI orchestration, APIs, UX/UI design, software development, testing and deployment.

The prototype will demonstrate the core product concept using a combination of real and simulated integrations. It is not intended to be a production-ready universal personal assistant.

---

**MyDay AI: One assistant. A clearer picture of your day. Better decisions, with you in control.**
