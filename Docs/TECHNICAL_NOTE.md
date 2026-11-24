# TransitPulse Delhi — Technical Note

**Transport Stack Hackathon 2026**

---

## 1. Solution Overview

TransitPulse Delhi is a crowding-aware journey-planning prototype built around two separate applications: Passenger and Reviewer.

The Passenger application provides journey-planning, surveys, ticket-code verification, crowding reports, and a points-based participation interface.

The Reviewer application provides an interface for authorised reviewers to inspect passenger reports, approve or reject submissions, and view dashboard analytics.

Both applications connect to a shared Supabase backend.

## 2. Technology Stack

| Component | Technology |
|---|---|
| Frontend | React 18 |
| Build Tool | Vite |
| Styling | Tailwind CSS |
| Backend Services | Supabase |
| Authentication | Supabase Auth |
| Database | Supabase |
| Android Framework | Capacitor |
| Deployment | Vercel |

## 3. System Architecture

The architecture is divided into four main parts.

### A. Passenger Application

The passenger frontend handles:

- Account authentication.
- Journey-planning interactions.
- Surveys.
- Demo ticket-code verification.
- Crowding reports.
- Rewards-related interfaces.

### B. Reviewer Application

The reviewer frontend provides:

- Access to report review.
- Approval and rejection operations.
- Dashboard analytics.
- Reviewer-specific functionality.

Reviewer access is designed to be restricted through the backend and database access policies.

### C. Supabase Backend

Supabase provides authentication and shared cloud database services.

The following are the principal database tables used by the application:

- `tp_tickets` — Demonstrative ticket-code records and their usage information.
- `tp_reports` — Passenger-submitted reports.
- `tp_reviewers` — Reviewer access records.

### D. Deployment

Passenger and Reviewer are maintained as separate applications.

The web applications are deployed independently, and Android application builds are supported through Capacitor.

## 4. Methodology

The development process followed these steps:

1. Identify the crowding-aware journey-planning problem.
2. Design separate passenger and reviewer interfaces.
3. Develop the passenger-facing application.
4. Implement authentication and cloud database integration.
5. Implement demo ticket-code verification and passenger reporting.
6. Develop the reviewer report-management workflow.
7. Deploy and test the applications.

The prototype demonstrates the application workflow from passenger participation to reviewer-side report handling.

## 5. Data Utilisation and Handling

### Important Dataset Disclosure

The current prototype uses demonstrative transport and crowding data. The official Delhi transit dataset provided by the hackathon organisers has not been integrated into the current implementation.

The current journey-planning and crowding interfaces therefore demonstrate the intended user experience and application workflow rather than providing verified real-world crowding predictions.

Demo ticket codes are used to demonstrate ticket verification and reporting. They are not official ETM records or real passenger ticket data.

Supabase is used to manage authentication and application records. Passenger reports and ticket usage information are stored in the backend. Reviewer access is intended to be controlled through database access policies.

The prototype should not be interpreted as a live public transport monitoring system.

## 6. Assumptions

- Demonstrative transport and crowding values are sufficient to demonstrate the current user workflow.
- Demo ticket codes can be used to test the reporting process.
- Passenger and reviewer interfaces require different access permissions.
- Official transport data integration will require additional data mapping, validation, and backend development.

## 7. Limitations

The current implementation has the following limitations:

- No integration with official Delhi transit datasets.
- No live ETM data integration.
- No live vehicle GPS tracking.
- Crowding information is demonstrative and not independently verified.
- Journey recommendations are not yet based on verified live transport conditions.

## 8. Future Technical Development

The next development stage can focus on:

1. Importing and mapping official Delhi transit data.
2. Integrating verified bus and Metro route information.
3. Connecting ETM data sources where access is available.
4. Integrating GPS-based vehicle positions.
5. Developing a data-processing pipeline for crowding estimation.
6. Improving journey recommendations using verified transport information.

## 9. Conclusion

TransitPulse Delhi demonstrates a working software prototype for crowding-aware journey planning, passenger participation, and reviewer-based report management.

Its current data is demonstrative rather than live. The application architecture provides a foundation for future integration of official Delhi transit information and real-time transport data sources.
