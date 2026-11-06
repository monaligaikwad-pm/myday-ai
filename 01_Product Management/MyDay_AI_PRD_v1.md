
# MyDay AI - Product Requirements Document
Version: 1.1
Product direction: Aggregator-first personal AI assistant

## 1. Product Vision

MyDay AI is an AI-powered personal assistant that acts as a central conversational interface across the applications and services people already use.

Rather than replacing existing applications, MyDay AI connects to supported services, retrieves information with user permission, brings relevant information together, understands the user's requests, and helps coordinate actions across services.

The goal is to reduce the effort involved in managing everyday life across multiple disconnected applications.

Users should be able to ask MyDay AI questions, receive consolidated information, get recommendations and initiate approved actions without having to manually navigate multiple apps.

## 2. Problem Statement

People use multiple applications to manage their daily lives, including calendars, health trackers, email, shopping services, reminders and personal notes.

Each application serves a specific purpose, but information remains fragmented.

Users must:
- Open multiple applications to understand their daily commitments.
- Remember where specific information is stored.
- Manually connect information from different sources.
- Repeat information or tasks across applications.
- Switch between applications to complete related activities.

MyDay AI aims to solve this fragmentation through a unified conversational interface and intelligent cross-application workflows.

## 3. Product Objectives

1. Provide one conversational interface for interacting with multiple applications.
2. Retrieve relevant information from authorised external services.
3. Present consolidated information with clear source attribution.
4. Understand natural-language requests and identify the appropriate service or workflow.
5. Help users initiate actions in connected applications, subject to permissions and approval.
6. Minimise unnecessary duplication of information.
7. Protect user privacy and maintain transparency and control.

## 4. Target User

Initial target: An individual Android user who regularly uses multiple applications to manage personal activities and wants a simpler way to access and coordinate information.

Future audience: Individuals and households using multiple digital services who value convenience, personalisation and privacy.

## 5. Core Product Principles

- Aggregator first: Connect existing applications rather than recreate their functionality.
- Source of truth: Each external application remains the authoritative source for its own information.
- Modular integrations: New services should be connectable without redesigning the entire application.
- User consent: Access only information the user has authorised.
- Read first: Start with information retrieval before introducing write actions.
- Human approval: Require confirmation for consequential actions.
- Privacy first: Minimise data collection, protect credentials and provide access controls.
- Transparency: Show the source and freshness of retrieved information.
- Graceful failure: Explain when a service is unavailable or does not support a requested capability.

## 6. MVP Functional Scope

| Priority | Capability | MVP expectation |
|---|---|---|
| Must | Conversational interface | Accept natural-language requests through text. |
| Must | Connector architecture | Provide a modular structure for connecting external services. |
| Must | Calendar integration | Retrieve calendar events using authorised Google Calendar access, subject to API availability. |
| Must | Unified daily view | Consolidate relevant information from connected services. |
| Must | Source attribution | Identify the service providing each piece of information. |
| Must | Permission management | Communicate connection permissions and provide a way to revoke access. |
| Must | Request interpretation | Understand supported requests and identify the appropriate information source. |
| Must | Safe information retrieval | Validate connector requests and handle errors, missing data and unavailable services. |
| Must | Personal context | Maintain minimal user preferences and connection information needed for workflows. |
| Should | Mock health connector | Demonstrate retrieval of sample health and activity information. |
| Should | AI-powered summaries | Provide useful summaries across connected information sources. |
| Should | Voice input | Support spoken requests where the core text-based experience is stable. |
| Could | Health Connect | Explore real Android Health Connect integration after the prototype. |
| Could | Additional integrations | Explore email, shopping and other services through supported APIs. |

## 7. Initial Integration Strategy

| Service | Information | Initial approach |
|---|---|---|
| Google Calendar | Appointments and events | First real integration, read-only |
| Health Connect | Activity and health information | Mock connector initially |
| Email | Messages and relevant information | Future exploration |
| Shopping services | Orders and shopping information | Future exploration |
| Other applications | Information and workflows | Based on API availability and user demand |

All integrations are subject to provider permissions, supported APIs, technical feasibility and applicable terms.

## 8. Data Ownership and Storage

MyDay AI should not unnecessarily duplicate information already maintained by external applications.

| Data | Preferred source of truth |
|---|---|
| Calendar events | Connected calendar |
| Health and activity | Connected health service |
| Emails | Connected email provider |
| Shopping orders | Relevant shopping provider |
| User preferences | MyDay AI |
| Connection settings | MyDay AI |
| Cross-service context | MyDay AI, with appropriate data minimisation |

MyDay AI may temporarily process retrieved information to answer a request. Any persistent storage must have a clear purpose, appropriate permission and retention policy.

## 9. Security and Privacy Requirements

- Use authorised APIs and permission-based access.
- Request only the minimum permissions required.
- Securely manage API credentials and tokens.
- Never expose secrets in frontend code or public repositories.
- Allow users to disconnect services and revoke access.
- Clearly identify the source of retrieved information.
- Require user approval for consequential actions.
- Do not send sensitive personal information to external AI services without appropriate consent.
- Use synthetic information for development and testing.
- Do not sell or use personal, health or journal information for advertising or profiling.

## 10. Out of Scope for the Initial Prototype

- Replacing existing calendar, health, email or shopping applications.
- Building a complete personal health tracker.
- Building a full-featured journaling application.
- Multiple live third-party integrations.
- Autonomous purchases, bookings or message sending.
- Payment processing, subscriptions and advertising.
- Multi-user and family-sharing functionality.
- Full native Android or Play Store release.

These capabilities may be considered in later product releases.

## 11. Product Assumptions

- Users experience friction when information is spread across multiple applications.
- Users value a single conversational interface for retrieving information.
- Users will authorise access when the value is clear and permissions are transparent.
- External services will provide sufficient API access for selected use cases.
- Users prefer their existing applications to remain the source of truth.
- AI can improve the experience by interpreting requests and coordinating information retrieval.

These assumptions must be validated through user research and prototype testing.

## 12. Open Questions

- Which external applications should be prioritised after Google Calendar?
- Which integrations offer useful free API access?
- How should MyDay AI handle conflicting or outdated information?
- How should users manage permissions across multiple services?
- What information should be temporarily cached versus permanently stored?
- How should MyDay AI communicate when a service does not support a requested action?
- Which AI capabilities genuinely improve the experience beyond conventional search?

## 13. Product Risks

- Limited API access or changing third-party integration policies.
- Complex authentication and permission requirements.
- Inconsistent information across connected services.
- Privacy and security risks associated with aggregated personal information.
- AI misinterpreting user requests.
- Incorrect or incomplete information retrieval.
- Dependence on external AI providers.
- Free-tier limitations affecting deployment or usage.

## 14. Success Criteria

The prototype should demonstrate:

1. A working conversational interface.
2. Successful retrieval of information from at least one real external service, preferably Google Calendar.
3. A second information source through a clearly labelled mock connector.
4. A consolidated response using information from both sources.
5. Clear source attribution and information freshness.
6. Permission-aware access and safe handling of requests.
7. Appropriate handling of unavailable services, missing information and errors.
8. No unauthorised consequential actions.

## 15. Future Product and Monetisation Opportunities

Potential future capabilities:
- Additional application integrations.
- Advanced cross-service planning and automation.
- Health and activity insights.
- Email and shopping workflows.
- Optional private journaling integration or functionality.
- Personalised daily and weekly summaries.

Potential monetisation hypotheses:
- Freemium access with optional advanced AI capabilities.
- Premium integrations and automation.
- Household or family plans.

These are hypotheses for future validation, not commitments or part of the initial prototype. Personal, health and journal data will not be sold or monetised.

# MyDay AI - Product Requirements Document
Version: 1.1
Product direction: Aggregator-first personal AI assistant

## 1. Product Vision

MyDay AI is an AI-powered personal assistant that acts as a central conversational interface across the applications and services people already use.

Rather than replacing existing applications, MyDay AI connects to supported services, retrieves information with user permission, brings relevant information together, understands the user's requests, and helps coordinate actions across services.

The goal is to reduce the effort involved in managing everyday life across multiple disconnected applications.

Users should be able to ask MyDay AI questions, receive consolidated information, get recommendations and initiate approved actions without having to manually navigate multiple apps.

## 2. Problem Statement

People use multiple applications to manage their daily lives, including calendars, health trackers, email, shopping services, reminders and personal notes.

Each application serves a specific purpose, but information remains fragmented.

Users must:
- Open multiple applications to understand their daily commitments.
- Remember where specific information is stored.
- Manually connect information from different sources.
- Repeat information or tasks across applications.
- Switch between applications to complete related activities.

MyDay AI aims to solve this fragmentation through a unified conversational interface and intelligent cross-application workflows.

## 3. Product Objectives

1. Provide one conversational interface for interacting with multiple applications.
2. Retrieve relevant information from authorised external services.
3. Present consolidated information with clear source attribution.
4. Understand natural-language requests and identify the appropriate service or workflow.
5. Help users initiate actions in connected applications, subject to permissions and approval.
6. Minimise unnecessary duplication of information.
7. Protect user privacy and maintain transparency and control.

## 4. Target User

Initial target: An individual Android user who regularly uses multiple applications to manage personal activities and wants a simpler way to access and coordinate information.

Future audience: Individuals and households using multiple digital services who value convenience, personalisation and privacy.

## 5. Core Product Principles

- Aggregator first: Connect existing applications rather than recreate their functionality.
- Source of truth: Each external application remains the authoritative source for its own information.
- Modular integrations: New services should be connectable without redesigning the entire application.
- User consent: Access only information the user has authorised.
- Read first: Start with information retrieval before introducing write actions.
- Human approval: Require confirmation for consequential actions.
- Privacy first: Minimise data collection, protect credentials and provide access controls.
- Transparency: Show the source and freshness of retrieved information.
- Graceful failure: Explain when a service is unavailable or does not support a requested capability.

## 6. MVP Functional Scope

| Priority | Capability | MVP expectation |
|---|---|---|
| Must | Conversational interface | Accept natural-language requests through text. |
| Must | Connector architecture | Provide a modular structure for connecting external services. |
| Must | Calendar integration | Retrieve calendar events using authorised Google Calendar access, subject to API availability. |
| Must | Unified daily view | Consolidate relevant information from connected services. |
| Must | Source attribution | Identify the service providing each piece of information. |
| Must | Permission management | Communicate connection permissions and provide a way to revoke access. |
| Must | Request interpretation | Understand supported requests and identify the appropriate information source. |
| Must | Safe information retrieval | Validate connector requests and handle errors, missing data and unavailable services. |
| Must | Personal context | Maintain minimal user preferences and connection information needed for workflows. |
| Should | Mock health connector | Demonstrate retrieval of sample health and activity information. |
| Should | AI-powered summaries | Provide useful summaries across connected information sources. |
| Should | Voice input | Support spoken requests where the core text-based experience is stable. |
| Could | Health Connect | Explore real Android Health Connect integration after the prototype. |
| Could | Additional integrations | Explore email, shopping and other services through supported APIs. |

## 7. Initial Integration Strategy

| Service | Information | Initial approach |
|---|---|---|
| Google Calendar | Appointments and events | First real integration, read-only |
| Health Connect | Activity and health information | Mock connector initially |
| Email | Messages and relevant information | Future exploration |
| Shopping services | Orders and shopping information | Future exploration |
| Other applications | Information and workflows | Based on API availability and user demand |

All integrations are subject to provider permissions, supported APIs, technical feasibility and applicable terms.

## 8. Data Ownership and Storage

MyDay AI should not unnecessarily duplicate information already maintained by external applications.

| Data | Preferred source of truth |
|---|---|
| Calendar events | Connected calendar |
| Health and activity | Connected health service |
| Emails | Connected email provider |
| Shopping orders | Relevant shopping provider |
| User preferences | MyDay AI |
| Connection settings | MyDay AI |
| Cross-service context | MyDay AI, with appropriate data minimisation |

MyDay AI may temporarily process retrieved information to answer a request. Any persistent storage must have a clear purpose, appropriate permission and retention policy.

## 9. Security and Privacy Requirements

- Use authorised APIs and permission-based access.
- Request only the minimum permissions required.
- Securely manage API credentials and tokens.
- Never expose secrets in frontend code or public repositories.
- Allow users to disconnect services and revoke access.
- Clearly identify the source of retrieved information.
- Require user approval for consequential actions.
- Do not send sensitive personal information to external AI services without appropriate consent.
- Use synthetic information for development and testing.
- Do not sell or use personal, health or journal information for advertising or profiling.

## 10. Out of Scope for the Initial Prototype

- Replacing existing calendar, health, email or shopping applications.
- Building a complete personal health tracker.
- Building a full-featured journaling application.
- Multiple live third-party integrations.
- Autonomous purchases, bookings or message sending.
- Payment processing, subscriptions and advertising.
- Multi-user and family-sharing functionality.
- Full native Android or Play Store release.

These capabilities may be considered in later product releases.

## 11. Product Assumptions

- Users experience friction when information is spread across multiple applications.
- Users value a single conversational interface for retrieving information.
- Users will authorise access when the value is clear and permissions are transparent.
- External services will provide sufficient API access for selected use cases.
- Users prefer their existing applications to remain the source of truth.
- AI can improve the experience by interpreting requests and coordinating information retrieval.

These assumptions must be validated through user research and prototype testing.

## 12. Open Questions

- Which external applications should be prioritised after Google Calendar?
- Which integrations offer useful free API access?
- How should MyDay AI handle conflicting or outdated information?
- How should users manage permissions across multiple services?
- What information should be temporarily cached versus permanently stored?
- How should MyDay AI communicate when a service does not support a requested action?
- Which AI capabilities genuinely improve the experience beyond conventional search?

## 13. Product Risks

- Limited API access or changing third-party integration policies.
- Complex authentication and permission requirements.
- Inconsistent information across connected services.
- Privacy and security risks associated with aggregated personal information.
- AI misinterpreting user requests.
- Incorrect or incomplete information retrieval.
- Dependence on external AI providers.
- Free-tier limitations affecting deployment or usage.

## 14. Success Criteria

The prototype should demonstrate:

1. A working conversational interface.
2. Successful retrieval of information from at least one real external service, preferably Google Calendar.
3. A second information source through a clearly labelled mock connector.
4. A consolidated response using information from both sources.
5. Clear source attribution and information freshness.
6. Permission-aware access and safe handling of requests.
7. Appropriate handling of unavailable services, missing information and errors.
8. No unauthorised consequential actions.

## 15. Future Product and Monetisation Opportunities

Potential future capabilities:
- Additional application integrations.
- Advanced cross-service planning and automation.
- Health and activity insights.
- Email and shopping workflows.
- Optional private journaling integration or functionality.
- Personalised daily and weekly summaries.

Potential monetisation hypotheses:
- Freemium access with optional advanced AI capabilities.
- Premium integrations and automation.
- Household or family plans.

These are hypotheses for future validation, not commitments or part of the initial prototype. Personal, health and journal data will not be sold or monetised.
