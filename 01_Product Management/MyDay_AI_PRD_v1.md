
# MyDay AI - Product Requirements Document

**Version:** 1.2  
**Status:** Product Definition  
**Product Direction:** Aggregator-first AI Personal Assistant  
**Prototype Timeline:** 8 Weeks  
**Document Owner:** Product Team

---

# 1. Product Overview

## 1.1 Product Vision

MyDay AI is an AI-powered personal assistant that brings together information from the applications and services people already use to help them organise, understand and manage their everyday lives.

It acts as a central intelligence layer across productivity, personal tasks, health, wellness, nutrition and daily routines.

Rather than replacing existing applications, MyDay AI connects to supported services, retrieves relevant information with user permission, understands the user's needs and provides a unified, personalised experience.

The assistant can inform, recommend and help execute actions, while keeping users in control.

## 1.2 Problem Statement

People use multiple applications to manage different aspects of their lives:

- Calendar applications for meetings and appointments.
- Fitness and health applications for activity and wellness.
- Weather applications for daily conditions.
- Navigation applications for travel planning.
- Task applications for reminders and pending activities.
- Food and grocery applications for meals and shopping.

These applications generally operate independently.

Users must repeatedly switch between applications, interpret information, remember important activities and decide how to prioritise their day.

This creates fragmented information, missed reminders, duplicated effort and difficulty maintaining consistent routines.

MyDay AI aims to address this problem by bringing relevant information together and using AI to help users make better everyday decisions.

## 1.3 Product Objectives

1. Provide a unified view of the user's day.
2. Reduce the effort required to manage multiple applications.
3. Help users prioritise tasks, appointments and personal commitments.
4. Support consistent health, wellness and nutrition routines.
5. Provide personalised recommendations based on user preferences and available information.
6. Track completion and adapt future recommendations.
7. Enable users to initiate actions across connected services with appropriate permission and approval.
8. Protect personal information through privacy-first design.

## 1.4 Target Users

The initial target audience includes:

- Working professionals managing demanding schedules.
- Individuals balancing professional and personal responsibilities.
- People using multiple applications to manage productivity and wellness.
- Individuals seeking help establishing consistent daily routines.
- People who want personalised recommendations without maintaining multiple separate tracking systems.

The initial prototype will be designed around a single-user experience.

Family accounts and multi-user support are future opportunities.

---

# 2. Product Strategy and Principles

## 2.1 Aggregator-First Approach

MyDay AI will follow an aggregator-first model.

It will connect to existing applications and services rather than attempting to recreate their functionality.

External applications remain the source of truth for the information they manage.

Examples:

| Information | Source of Truth |
|---|---|
| Meetings and appointments | Google Calendar |
| Health and activity records | Connected health applications |
| Weather | Supported weather service |
| Travel and navigation | Google Maps or supported travel service |
| Grocery inventory and orders | Grocery service such as BigBasket |
| Medication schedules | User-entered information or supported authorised source |
| Personal preferences | MyDay AI |

MyDay AI will retrieve, interpret and present relevant information across these sources.

## 2.2 Core Product Principles

**1. One assistant, multiple services**

Users should be able to interact through one conversational interface rather than repeatedly switching between applications.

**2. Do not unnecessarily duplicate existing functionality**

Use existing services wherever practical. Build native capabilities only when necessary to deliver the unified experience.

**3. User control and consent**

Users decide which applications to connect, which permissions to grant and which actions MyDay AI may initiate.

**4. Inform, recommend and act**

MyDay AI should progress beyond displaying information.

- Inform: retrieve and consolidate relevant information.
- Recommend: identify opportunities, conflicts and priorities.
- Act: help users execute approved actions through supported integrations.

**5. Adaptive intelligence**

Recommendations should improve using user preferences, feedback and recorded outcomes.

**6. Privacy and security by design**

Use minimum necessary permissions, secure authentication and data minimisation.

**7. Modular architecture**

Connectors should be independently replaceable so that additional services can be introduced without redesigning the entire application.

---

# 3. Core Product Capabilities

MyDay AI will be organised into five major capability areas.

## 3.1 Daily Intelligence

Provide a consolidated understanding of the user's day.

Functional requirements:

- Retrieve meetings, appointments and calendar events.
- Present a personalised daily briefing.
- Retrieve weather information.
- Identify available calendar slots.
- Highlight scheduling conflicts.
- Surface birthdays, anniversaries and important occasions.
- Retrieve travel information where supported.
- Recommend departure times based on estimated travel conditions.
- Identify important events requiring preparation.
- Present pending tasks and reminders.

Example user requests:

- "Show me everything I need to know about today."
- "What does my afternoon look like?"
- "Do I have time for a workout tomorrow?"
- "When should I leave for my appointment?"
- "Whose birthday is coming up this week?"

## 3.2 Personal Productivity

Help users manage tasks, reminders and everyday responsibilities.

Functional requirements:

- Retrieve or maintain supported tasks and reminders.
- Identify incomplete tasks from previous days.
- Carry forward pending activities.
- Highlight approaching deadlines.
- Suggest task priorities.
- Recommend available time slots for tasks.
- Help users create or modify calendar events.
- Support reminders for bills, renewals and other personal responsibilities.
- Require approval before making changes to external services.

Example user requests:

- "What did I forget to do yesterday?"
- "Remind me to pay my phone bill tomorrow."
- "Find an hour this week for this task."
- "Move my appointment to Friday."

## 3.3 Health and Wellness Intelligence

Provide a consolidated view of available health and activity information.

Functional requirements:

- Retrieve supported health and activity data from connected services.
- Present weight trends and progress against user-defined goals.
- Track workout schedules and completed activities.
- Identify missed or postponed workouts when reliable information is available.
- Present available metrics such as steps and active minutes.
- Monitor workout consistency.
- Recommend activities based on availability and user-defined goals.
- Identify changes in activity patterns.
- Provide a consolidated wellness overview.

Potential integrations:

- Health Connect.
- Google Fit, where supported.
- Samsung Health, through supported access.
- Cult Fitness, through supported access.
- Fitelo, through supported access.

Health Connect is a potential aggregation route for compatible Android applications. Actual access will depend on supported permissions and platform capabilities.

The prototype will use simulated health and activity data rather than claiming live integration.

## 3.4 Nutrition and Daily Routine Intelligence

Help users maintain consistent meal, medication and hydration routines.

### A. Personalised Meal Recommendations

Functional requirements:

- Generate proactive breakfast, lunch and dinner suggestions.
- Provide on-demand meal recommendations.
- Support user-defined nutrition goals.
- Support dietary preferences and food restrictions.
- Consider available preparation time.
- Consider planned activities and daily schedules.
- Provide alternative meal suggestions.
- Explain why a meal matches the user's stated goals.
- Provide estimated nutritional information when reliable ingredient and portion data is available.

Potential nutrition preferences:

- High protein.
- Lower carbohydrate.
- Balanced macronutrients.
- Higher fibre.
- Calorie-conscious.
- Vegetarian.
- Vegan.
- Other user-defined dietary preferences.

Example user requests:

- "Suggest a high-protein vegetarian lunch."
- "What can I prepare in 20 minutes?"
- "Give me a lower-carb dinner option."
- "Suggest meals for tomorrow based on my nutrition goals."

### B. Meal Planning

Future capabilities:

- Daily and weekly meal planning.
- Meal logging.
- Nutrition summaries.
- Ingredient and pantry management.
- Grocery list generation.
- Grocery application integration.
- Suggestions based on available ingredients.

### C. Medication Reminders

Functional requirements:

- Allow users to enter medication names and reminder schedules.
- Provide reminders at configured times.
- Allow users to record completion, postponement or skipping.
- Maintain a history of recorded reminder outcomes.

MyDay AI must not independently prescribe medication or change dosage, timing or medical instructions.

### D. Hydration Reminders

Functional requirements:

- Allow users to define daily hydration goals.
- Provide reminders at configurable intervals.
- Allow users to record water consumption.
- Track progress against user-defined goals.
- Support flexible reminder schedules.

### E. Daily Routine Management

Meal, medication and hydration reminders should be considered alongside the user's calendar and daily activities.

Recommendations should avoid unnecessary notification overload.

## 3.5 Adaptive Intelligence

MyDay AI should learn from user feedback and recorded outcomes.

The system should operate through a continuous feedback loop:

**Plan → Remind → Track → Learn → Adapt**

Functional requirements:

- Track completion of planned activities.
- Record skipped, postponed and missed activities.
- Distinguish between incomplete activities and unavailable completion data.
- Retrieve completion information from connected services where supported and authorised.
- Identify recurring behaviour patterns.
- Adapt future recommendations.
- Suggest more realistic schedules.
- Consider changes in user preferences and availability.
- Allow users to correct completion records.
- Allow users to disable or modify personalised recommendations.

Examples:

| Observed behaviour | Possible adaptation |
|---|---|
| Evening workouts repeatedly skipped | Suggest an earlier workout slot |
| Breakfast reminders regularly missed | Ask whether the reminder time should change |
| Hydration goal consistently missed | Suggest smaller, manageable targets |
| Meal recommendations frequently rejected | Offer different meal preferences |
| Tasks repeatedly carried forward | Suggest reprioritisation |
| Calendar becomes unexpectedly busy | Reconsider optional activities |

Supported activity statuses:

- Planned
- Completed
- Skipped
- Postponed
- Missed
- Completion unknown

The system must not assume that an activity was missed simply because a connected service did not report completion.

Adaptive recommendations must remain transparent and user-controlled.

---

# 4. Primary User Journey: Daily Briefing

The primary product entry point is:

"Show me everything I need to know about my day."

MyDay AI should retrieve relevant information from connected services and present a consolidated daily briefing.

The briefing should include:

1. Weather and relevant conditions.
2. Meetings and appointments.
3. Travel and commute information where supported.
4. Important occasions.
5. Pending tasks and reminders.
6. Upcoming deadlines and personal responsibilities.
7. Meal suggestions.
8. Medication and hydration reminders.
9. Planned workouts and activity recommendations.
10. Important actions requiring attention.

The briefing should distinguish between:

- Information retrieved from connected services.
- Information entered directly by the user.
- AI-generated recommendations.
- Actions awaiting user approval.

---

# 5. Supporting User Journeys

## Journey A: Daily Planning

1. User requests a daily briefing.
2. MyDay AI retrieves relevant calendar and connected-service information.
3. It identifies pending tasks and important commitments.
4. It evaluates available time.
5. It recommends priorities and optional activities.
6. User accepts, rejects or modifies recommendations.

## Journey B: Adaptive Wellness

1. MyDay AI retrieves available activity and weight information.
2. It compares information against user-defined goals.
3. It identifies planned activities and available calendar slots.
4. It recommends realistic workout opportunities.
5. User records completion, postponement or skipping.
6. MyDay AI adapts subsequent recommendations based on the recorded outcome.

## Journey C: Personalised Nutrition

1. User defines nutrition goals and dietary preferences.
2. MyDay AI generates meal suggestions in the daily briefing.
3. User can request alternatives or additional suggestions.
4. MyDay AI explains how recommendations relate to stated preferences.
5. User records whether a suggested meal was followed.
6. Future suggestions adapt to preferences and feedback.

## Journey D: Reminders and Routine Tracking

1. User configures meal, medication and hydration reminders.
2. MyDay AI presents reminders at configured times.
3. User records completion, postponement or skipping.
4. MyDay AI tracks reminder outcomes.
5. It identifies recurring patterns.
6. It suggests changes to flexible reminders, subject to user approval.

Medication instructions are not modified by the AI.

## Journey E: Task and Action Management

1. MyDay AI retrieves pending tasks and reminders.
2. It identifies incomplete activities.
3. It recommends priorities and available time slots.
4. User approves proposed calendar or task changes.
5. MyDay AI initiates supported actions.
6. It confirms the outcome based on the connected service response.

---

# 6. Integration Strategy

## 6.1 Initial Integration Priorities

| Service | Intended capability | Prototype approach |
|---|---|---|
| Google Calendar | Meetings, appointments and availability | First real integration, read-only |
| Health Connect | Health and activity information | Simulated connector |
| Weather service | Current conditions and forecasts | Mock data initially |
| Google Maps | Travel and commute planning | Mock data or navigation link |
| BigBasket | Grocery discovery and ordering | Future integration |

## 6.2 Health Data Sources

Potential health data sources include:

- Google Fit.
- Cult Fitness.
- Fitelo.
- Samsung Health.

Where supported, compatible applications may share information through Health Connect.

The architecture should avoid unnecessary duplicate records and should identify the original data source.

Live integration with each individual provider is not assumed.

## 6.3 Integration Principles

- Use supported APIs and platform permissions.
- Do not bypass application security or access restrictions.
- Use OAuth or other appropriate secure authentication mechanisms.
- Keep access tokens and credentials out of frontend code and source control.
- Request only the permissions required for each capability.
- Support disconnection and permission revocation.
- Display source attribution and data freshness.
- Handle unavailable services and incomplete data gracefully.

## 6.4 Connector Architecture

Each external service should be integrated through a modular connector.

The application should be able to retrieve information through a consistent internal interface, regardless of the external provider.

Adding or replacing a connector should not require rewriting the core assistant.

---

# 7. Data Ownership and Storage

External services remain the source of truth for their respective information.

MyDay AI should store only the information needed to support its own functionality.

| Data category | Storage approach |
|---|---|
| Calendar events | Retrieve from source; minimise local persistence |
| Health records | Retrieve with permission; avoid unnecessary duplication |
| User preferences | Store minimal required preferences |
| Connection metadata | Store connection status and necessary metadata |
| Reminder schedules | Store where required for reminder functionality |
| Completion history | Store minimal activity outcomes needed for adaptation |
| AI context | Retain only the minimum necessary context |
| Credentials and tokens | Store securely, never in frontend code |

For the prototype, use synthetic or mock health data.

Do not use real personal health information or private journal content in experimental AI services.

---

# 8. AI Orchestration and Action Management

AI will interpret natural-language requests and determine which information or capabilities are needed.

The backend will control access to connectors and actions.

The intended flow is:

1. User submits a request.
2. AI interprets the request.
3. The system identifies the required data or action.
4. Backend checks permissions and validates parameters.
5. Supported connectors retrieve information or prepare an action.
6. Consequential actions are presented for user approval.
7. Backend executes approved actions.
8. MyDay AI communicates the confirmed outcome.

AI must not directly access databases, credentials or external services without backend validation.

Examples of consequential actions include:

- Creating or changing calendar events.
- Sending communications.
- Booking appointments.
- Placing grocery orders.
- Making payments.

These actions require explicit approval.

---

# 9. Security, Privacy and Safety Requirements

- Follow privacy-by-design and data-minimisation principles.
- Use secure authentication and authorisation.
- Protect API credentials and access tokens.
- Request explicit permissions for connected services.
- Allow users to disconnect services and revoke access.
- Display the origin of retrieved information.
- Identify stale, unavailable or incomplete information.
- Distinguish facts from AI-generated suggestions.
- Never invent missing health or nutrition information.
- Label nutritional information as estimated when appropriate.
- Do not diagnose medical conditions or prescribe diets.
- Do not change medication dosage or prescribed schedules.
- Require approval for consequential external actions.
- Use synthetic data for prototype testing wherever possible.
- Avoid using sensitive personal information for experimental AI model training.

---

# 10. Eight-Week Prototype Scope

The prototype will demonstrate the central product concept without attempting to deliver every future integration.

## Week 1: Product Foundation

- Finalise product requirements.
- Define target user and core journeys.
- Establish functional and non-functional requirements.
- Define the connector strategy.
- Document data ownership and permissions.
- Create prioritised product backlog.

## Week 2: UX and Technical Architecture

- Design conversational interface.
- Design daily briefing dashboard.
- Design connected-services screen.
- Design reminder and completion interactions.
- Define empty, error and permission states.
- Define modular architecture and data model.

## Week 3: Frontend Development

- Learn and implement React and TypeScript foundations.
- Build responsive application shell.
- Build conversational input.
- Build daily briefing interface.
- Build connector status display.
- Use mock data initially.

## Week 4: Backend Development

- Build Python/FastAPI backend.
- Understand REST APIs and JSON.
- Implement basic data validation.
- Introduce minimal persistence.
- Implement reminder and completion data structures.
- Add logging and error handling.

## Week 5: First Real Connector

- Explore Google Calendar API.
- Implement OAuth if feasible.
- Retrieve calendar events using read-only access.
- Display source attribution.
- Test permissions and failure handling.
- Retain a clearly labelled mock fallback if live integration is blocked.

## Week 6: AI and Adaptive Intelligence

- Implement natural-language request interpretation.
- Introduce structured AI outputs and tool calling.
- Connect AI orchestration to backend functions.
- Build meal recommendations using user preferences and mock information.
- Build basic workout recommendations.
- Implement completion tracking.
- Demonstrate adaptation based on recorded outcomes.

## Week 7: Safety and Refinement

- Test permissions and access controls.
- Test reminder and completion flows.
- Test AI responses and recommendations.
- Test missing and conflicting data.
- Test source attribution.
- Refine user experience.
- Address privacy and security risks.

## Week 8: Testing and Portfolio Delivery

- Complete functional and integration testing.
- Test the end-to-end daily briefing.
- Demonstrate real and simulated connectors.
- Demonstrate adaptive recommendations.
- Deploy a working demonstration if free hosting is feasible.
- Document architecture and limitations.
- Prepare GitHub documentation and portfolio case study.

The eight-week timeline is an ambitious prototype target. Integration and deployment feasibility will determine the final demonstration scope.

---

# 11. Prototype Technology Stack

The project will use a free-first approach.

| Area | Proposed technology |
|---|---|
| Code editor | Visual Studio Code |
| Version control | Git and GitHub |
| UX/UI design | Figma Starter |
| Frontend | React and TypeScript |
| Backend | Python and FastAPI |
| API testing | Postman |
| Database | Supabase free tier or suitable alternative |
| Calendar integration | Google Calendar API |
| AI | Gemini API or another suitable free-tier service |
| Hosting | Suitable free hosting options |

Technology choices are provisional and will be validated during development.

Check current pricing, free-tier limits, API availability and terms before implementation.

Never commit API keys or credentials to GitHub.

---

# 12. Functional and Non-Functional Requirements

## Functional Requirements

The prototype should:

1. Accept natural-language user requests.
2. Present a consolidated daily briefing.
3. Retrieve calendar information from a real connector where feasible.
4. Retrieve simulated health and activity information.
5. Generate meal and activity recommendations.
6. Support basic user-defined reminders.
7. Record completion, skipped and postponed activities.
8. Demonstrate basic adaptive recommendations.
9. Display source attribution.
10. Respect permissions and approval requirements.

## Non-Functional Requirements

- Usable on desktop and mobile browsers.
- Modular and maintainable architecture.
- Secure handling of credentials.
- Appropriate error handling.
- Clear distinction between real and simulated information.
- Data minimisation.
- Accessible and understandable interface.
- Reliable handling of unavailable integrations.

---

# 13. Prototype Out of Scope

The following are not required for the initial eight-week prototype:

- Production-ready universal personal assistant.
- Native Android application and Play Store release.
- Live Health Connect integration.
- Direct integration with every health application.
- Advanced health analytics or medical recommendations.
- Real-time traffic and comprehensive navigation integration.
- Automated grocery purchases.
- Payment execution.
- Email and messaging integrations.
- Family and multi-user accounts.
- Advanced weekly meal planning.
- Pantry and inventory management.
- Subscription management and monetisation implementation.
- Autonomous consequential actions.

These capabilities may be considered in later releases.

---

# 14. Success Criteria

The prototype will be considered successful when it demonstrates:

1. A working conversational interface.
2. A useful consolidated daily briefing.
3. At least one real external integration, preferably Google Calendar, subject to feasibility.
4. At least one simulated connector for health and activity data.
5. Natural-language interpretation and information retrieval.
6. Meal and workout recommendations based on user-defined preferences and mock data.
7. Basic reminder and completion tracking.
8. At least one example of an adaptive recommendation based on recorded outcomes.
9. Clear source attribution and separation of facts from suggestions.
10. Appropriate permission handling and approval for consequential actions.
11. A documented and demonstrable end-to-end user journey.

---

# 15. Assumptions and Risks

| Risk or assumption | Mitigation |
|---|---|
| Third-party APIs may restrict access | Validate feasibility early and use modular mock connectors |
| Google Calendar OAuth may require additional configuration | Start integration research during the prototype foundation |
| Health data access varies by provider | Use Health Connect as a future route and simulate data initially |
| AI may generate inaccurate recommendations | Validate outputs and label estimates clearly |
| Integration complexity may affect timelines | Prioritise one real integration and limited simulated connectors |
| Free-tier services may have usage limits | Evaluate alternatives before committing to a service |
| Multiple sources may contain duplicate information | Define source attribution and duplicate-handling rules |
| Users may receive excessive reminders | Allow configurable schedules and notification preferences |

---

# 16. Future Product Opportunities

Potential future enhancements include:

- Native Android application.
- Health Connect integration.
- Additional productivity and health connectors.
- Real-time weather and travel intelligence.
- Weekly meal planning and nutrition tracking.
- Grocery list generation and BigBasket integration.
- Voice-first interactions.
- Journaling and personal reflection.
- Family and household assistance.
- Advanced adaptive recommendations.
- Personalised automation workflows.
- Freemium and premium subscription models.

Monetisation options are future hypotheses and require user research and validation.

Personal health, journal and other sensitive user data must never be sold.

---

# 17. Product Success Vision

MyDay AI should evolve into a trusted personal intelligence layer that helps people manage their everyday lives.

It should understand the user's schedule, commitments, preferences and goals, bring relevant information together, recommend useful next steps and help execute approved actions.

Its value should come from reducing cognitive load, improving everyday decision-making and helping users build sustainable routines.

**The ultimate product promise:**

"One assistant. A clearer picture of your day. Better decisions, with you in control."
