# TransitPulse Delhi
### A Smarter, Crowding-Aware Public Transport Journey Planner

<p align="center">
  <strong>Making every journey smarter.</strong>
</p>

<p align="center">
  A public transport technology prototype focused on crowding awareness, commuter participation, and smarter journey planning for Delhi.
</p>

---

## Overview

**TransitPulse Delhi** is a crowding-aware public transport platform designed to improve how commuters access transport information and make travel decisions.

The project aims to address a common urban mobility problem: commuters often have limited information about public transport crowding and travel conditions before starting their journey.

TransitPulse introduces a platform where passengers can participate through surveys and crowding reports, while authorized reviewers can verify submitted information.

The project currently consists of two dedicated applications connected to a shared Supabase backend.

## Problem Statement

Public transport commuters frequently face challenges such as:

- Uncertainty about crowding levels.
- Difficulty making informed travel decisions.
- Limited opportunities to contribute structured feedback.
- Challenges in collecting and verifying passenger-reported information.

TransitPulse explores how software, commuter participation, and transport data can work together to address these challenges.

## Our Solution

TransitPulse provides two separate applications for different user groups.

### 1. TransitPulse Passenger

The passenger application is designed for everyday commuters.

**Features:**
- Crowd-aware journey planning.
- Passenger surveys and feedback.
- Ticket-based survey verification.
- Crowding reports.
- Points and rewards system.
- Passenger account authentication.
- Transport information interface.

### 2. TransitPulse Reviewer

The reviewer application provides a dedicated interface for authorized reviewers.

**Features:**
- Reviewer authentication and access control.
- Passenger report monitoring.
- Report verification.
- Approve or reject submitted reports.
- Analytics and report monitoring.
- Dedicated reviewer dashboard.

## Application Preview

| Passenger Application | Reviewer Application |
|---|---|
| Journey planning | Report verification |
| Passenger feedback | Review management |
| Crowding reports | Approval and rejection |
| Points and rewards | Analytics dashboard |


## System Architecture

TransitPulse follows a two-application architecture with a shared backend.

```text
                 TRANSITPULSE DELHI
                         |
             +-----------+-----------+
             |                       |
             v                       v
    PASSENGER APPLICATION    REVIEWER APPLICATION
             |                       |
             v                       v
       React + Vite             React + Vite
             |                       |
             +-----------+-----------+
                         |
                         v
                  SUPABASE BACKEND
                         |
             +-----------+-----------+
             |           |           |
             v           v           v
        Authentication  Database  Backend Logic
             |
             v
       Passenger and Reviewer
       Access Management
```

Both applications communicate with the same Supabase backend, while reviewer access is intended to be restricted to authorized accounts.

## Technology Stack

| Technology | Purpose |
|---|---|
| React 18 | Frontend application development |
| Vite | Development server and build tooling |
| Tailwind CSS | User interface styling |
| Supabase | Authentication, database and backend services |
| PostgreSQL | Relational database |
| Capacitor | Android application packaging |
| JavaScript | Application logic |
| Git & GitHub | Version control and collaboration |
| Vercel | Passenger web application deployment |

## Data Management and Verification

TransitPulse uses a shared Supabase backend for application data and authentication.

Important backend components include:

- `tp_tickets` — stores ticket codes and their usage status.
- `tp_reports` — stores passenger-submitted reports.
- `tp_reviewers` — manages authorized reviewer accounts.

Ticket-based verification helps prevent the same ticket from being used repeatedly for survey submissions.

Reviewer access is designed around database-backed authorization rather than simply hiding reviewer screens in the frontend.

## Platforms

| Application | Platform |
|---|---|
| TransitPulse Passenger | Web and Android |
| TransitPulse Reviewer | Web and Android |
 
**Passenger Web Application:**  
https://transitpulse-passenger.vercel.app/

**Passenger Web Application:**  
https://transitpulse-authenticator.vercel.app/

## Getting Started

### Prerequisites

Install the following tools:

- Node.js and npm
- Git
- Android Studio (for Android builds)

### 1. Clone the repository

### 2. Install dependencies

Navigate into the application directory you want to run:

```bash
cd apps/passenger
npm install
```

For the reviewer application:

```bash
cd apps/reviewer
npm install
```

### 3. Configure environment variables

Create a `.env.local` file inside the relevant application directory.

```env
VITE_SUPABASE_URL=YOUR_SUPABASE_PROJECT_URL
VITE_SUPABASE_ANON_KEY=YOUR_SUPABASE_PUBLIC_KEY
```

Use your Supabase public anon/publishable key. Never expose a Supabase service-role or secret key in frontend code.

### 4. Run the development server

```bash
npm run dev
```

### 5. Create a production build

```bash
npm run build
```

### 6. Build the Android application

After configuring Capacitor and building the web application:

```bash
npx cap sync android
npx cap open android
```

Build the APK using Android Studio.

*Note: The commands above assume the repository retains the current split-app directory structure and that dependencies and Capacitor configuration are present.*

## Current Development Status

| Component | Status |
|---|---|
| Passenger application | Implemented |
| Reviewer application | Implemented |
| Supabase authentication | Implemented |
| Ticket verification | Implemented |
| Passenger feedback system | Implemented |
| Reviewer report workflow | Implemented |
| Rewards system | Implemented |
| Passenger web deployment | Deployed |
| Android packaging | Integrated |
| Live ETM integration | Planned |
| GPS-based vehicle tracking | Planned |
| Real-time transport crowding data | Planned |

### Important Data Disclaimer

The current version is a functional prototype. Crowding levels, journey information, and transport information are demonstrative and should not be interpreted as verified live Delhi transport data.

Integration with official Electronic Ticketing Machine (ETM) data, GPS-based vehicle information, and real-world transport feeds is part of the future development roadmap.

## Roadmap

### Phase 1 — Core Platform
- [x] Passenger application
- [x] Reviewer application
- [x] Supabase integration
- [x] Ticket-based verification
- [x] Report review workflow

### Phase 2 — Transport Data Integration
- [ ] Explore official ETM data integration.
- [ ] Develop GPS-based vehicle tracking.
- [ ] Establish a transport-data ingestion pipeline.
- [ ] Improve crowding estimation using verified data.

### Phase 3 — Intelligent Journey Planning
- [ ] Improve crowding-aware route selection.
- [ ] Incorporate real-world transport conditions.
- [ ] Develop more accurate journey recommendations.
- [ ] Evaluate route suggestions using actual transport data.

### Phase 4 — Platform Expansion
- [ ] Improve analytics and reporting.
- [ ] Expand transport coverage.
- [ ] Improve passenger participation.
- [ ] Explore integration with additional public transport services.

## Future Vision

TransitPulse aims to evolve from a demonstration platform into a data-driven public transport intelligence system.

With access to official transport datasets and real-time vehicle information, the platform could help commuters understand transport conditions, compare journey options, and make better-informed travel decisions.

## Project Development

TransitPulse Delhi is being developed as a technology prototype for the Delhi Transport Stack Hackathon 2026.

The project explores the intersection of:

- Urban mobility
- Software engineering
- Data-driven decision-making
- Public transport technology
- Passenger participation

---

<p align="center">
  <strong>TransitPulse Delhi</strong><br/>
  Making every journey smarter. 🚍
</p>
