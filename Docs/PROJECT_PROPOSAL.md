# TransitPulse Delhi — Project Proposal

**Transport Stack Hackathon 2026**

- **Selected Problem Statement:** Crowdedness-aware Journey Planner
- **Project Name:** TransitPulse Delhi
- **Tagline:** Making Every Journey Smarter

---

## 1. Problem Statement

Public transport commuters often face uncertainty about crowding conditions when planning their journeys. A route may appear convenient based on travel time or distance, but overcrowding can make the actual commuting experience uncomfortable and inefficient.

TransitPulse Delhi aims to address this problem through a passenger-focused journey-planning platform that demonstrates how crowding information, passenger feedback, and journey information can be brought together in one system.

## 2. Proposed Solution

TransitPulse Delhi is a two-application platform consisting of:

### Passenger Application

- User registration, login, and authentication.
- Crowding-aware journey-planning interface.
- Demonstrative transport and crowding information.
- Passenger surveys and demo ticket-code verification.
- Crowding report submission.
- Points, wallet, and rewards interface.

### Reviewer Application

- Reviewer authentication and access control.
- Passenger report review.
- Report approval and rejection workflow.
- Dashboard analytics.
- Administrative review interface.

Both applications use a shared Supabase backend.

## 3. Approach and Methodology

The project was developed using an iterative software development approach.

### Phase 1 — Problem Identification

We selected crowding-aware journey planning as the problem area and identified the need for a platform that combines journey information with passenger participation.

### Phase 2 — System Design

We separated the platform into Passenger and Reviewer applications. This provides distinct interfaces for commuters and authorised reviewers.

### Phase 3 — Application Development

We developed the frontend using React, Vite, and Tailwind CSS. Supabase was used for authentication and cloud data management.

### Phase 4 — Passenger Participation

We implemented surveys, demonstrative ticket-code verification, crowding reports, and a points-based participation interface.

### Phase 5 — Review Workflow

We developed a reviewer dashboard to support report review, approval, rejection, and analytics.

### Phase 6 — Testing and Deployment

The applications were tested as working web applications and deployed for demonstration.

## 4. Data Handling

The current prototype uses demonstrative transport and crowding information. It does not currently consume the official Delhi transit dataset supplied by the organisers, nor does it integrate live ETM or vehicle GPS feeds.

Demo ticket codes are used to demonstrate the ticket-verification and passenger-reporting workflow. They should not be interpreted as official transport ticket records.

Passenger authentication and application data are managed through Supabase. Access to reviewer functionality is intended to be restricted to authorised reviewers.

## 5. System Architecture

The system consists of the following layers:

1. **Passenger Frontend:** React-based passenger application.
2. **Reviewer Frontend:** Separate React-based reviewer application.
3. **Authentication and Backend:** Supabase authentication and database services.
4. **Data Layer:** Application records for tickets, passenger reports, and reviewer access.
5. **Deployment:** Web applications deployed independently.

## 6. Expected Impact

TransitPulse aims to demonstrate how passenger participation and crowding-aware journey planning can improve public transport information systems.

Potential benefits include:

- Better awareness of crowding conditions.
- More informed journey-planning decisions.
- Structured passenger feedback.
- A review mechanism for submitted reports.
- A foundation for integrating official transport information.

## 7. Limitations and Future Scope

The current prototype uses demonstrative data. Its crowding information should not be treated as verified real-time conditions.

Future development includes:

- Integration of official Delhi transit datasets.
- ETM-based transport data integration.
- GPS-based vehicle tracking.
- More accurate crowding estimation.
- Improved journey recommendations using verified transport information.

## 8. Conclusion

TransitPulse Delhi is a functional prototype demonstrating a crowding-aware public transport platform with passenger participation and reviewer workflows.

Although official transport data integration remains future work, the prototype establishes an application architecture that can be extended towards a more data-driven public transport experience.
