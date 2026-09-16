A Vibe Coding Hackathon Project on UIxcellerate
# VeriTour --- Tourist Safety & Emergency Response Platform

VeriTour is a full-stack safety platform designed to support tourists
and response authorities through digital identity, emergency reporting,
location sharing, and incident management workflows.

## Overview

The platform provides a centralized ecosystem for:

-   Tourist onboarding and digital identity management
-   Emergency alert creation and incident tracking
-   e-FIR generation and incident documentation
-   Secure, time-bound location sharing
-   Geofenced safety zones and risk information
-   Authority dashboards and system analytics
-   Role-based user and access management

## Key Features

### Tourist Services

-   Tourist registration and profile management
-   Digital ID creation and QR-based activation
-   Emergency contact management
-   Safety information and risk-zone access
-   Secure location-sharing sessions
-   Emergency alert submission

### Authority Services

-   Role-based access for authorized personnel
-   Incident acknowledgement and status tracking
-   Incident logs and response workflow management
-   e-FIR generation and report management
-   Geofenced zone creation and administration
-   Analytics dashboards for operational insights

## Technology Stack

### Backend

-   Python
-   FastAPI
-   SQLAlchemy
-   Pydantic
-   SQLite
-   OAuth2/JWT authentication
-   Passlib/Bcrypt password hashing

### Frontend

-   HTML5
-   CSS3
-   JavaScript

### Design & Documentation

-   User research and UX task flows
-   Database entity-relationship design
-   API endpoint documentation
-   Workflow diagrams for onboarding, alerts, e-FIR, incident response,
    location sharing, monitoring, and analytics

## Architecture

The project follows a modular full-stack architecture:

1.  **Frontend layer** --- role-specific interfaces for tourists,
    authorities, administrators, and analytics users.
2.  **API layer** --- FastAPI REST endpoints for authentication,
    onboarding, incidents, e-FIRs, location sharing, zones, and user
    management.
3.  **Data layer** --- SQLAlchemy models and relational database schemas
    for tourists, digital IDs, trips, emergency contacts, incidents,
    logs, location sessions, geofenced zones, and e-FIR records.
4.  **Security layer** --- token-based authentication, password hashing,
    role-based access, and controlled location-sharing sessions.

## Core Data Entities

-   Tourist
-   Digital ID
-   Trip
-   Emergency Contact
-   System User
-   Role
-   Incident
-   Incident Log
-   Location Share Session
-   Location History
-   Geofenced Zone
-   e-FIR

## Project Structure

``` text
VERITOUR PROJECT/
├── BACKEND/
│   ├── API CODE
│   ├── SCHEMA SCRIPT
│   ├── API ENDPOINTS.png
│   ├── DATABASE STRUCTURE ENTITIES.png
│   └── DATABASE STRUCTURE RELATIONSHIPS.png
├── TASK FLOWS/
│   ├── Tourist Onboarding
│   ├── Emergency Alert
│   ├── Generate e-FIR
│   ├── Incident Response
│   ├── Share Location
│   ├── Proactive Monitoring
│   ├── System Analytics
│   ├── User Management
│   ├── Zone Management
│   └── View Safety Information
├── VERITOUR CODE UI.zip
├── UserResearch.pdf
├── BUSINESS REQUIREMENT DOCUMENT.pdf
└── VeriTour Project Logo.png
```

## Getting Started

### Prerequisites

-   Python 3.9+
-   pip
-   A virtual environment

### Installation

Clone the repository and navigate to the backend directory:

``` bash
git clone <your-repository-url>
cd "VERITOUR PROJECT/BACKEND"
```

Create and activate a virtual environment:

``` bash
python -m venv .venv
```

Windows:

``` bash
.venv\Scripts\activate
```

Linux/macOS:

``` bash
source .venv/bin/activate
```

Install the required dependencies:

``` bash
pip install fastapi uvicorn sqlalchemy pydantic[email] python-jose passlib[bcrypt] python-multipart
```

### Run the API

Save the backend API code as `main.py`, then run:

``` bash
uvicorn main:app --reload
```

The API will be available at:

``` text
http://127.0.0.1:8000
```

Interactive API documentation:

``` text
http://127.0.0.1:8000/docs
```

> The current implementation uses SQLite for local development.
> Configure a production database, secret management, HTTPS, logging,
> and deployment controls before using the platform in a live
> environment.

## Security Considerations

-   Use environment variables for secret keys and database
    configuration.
-   Replace development secrets with securely managed production
    credentials.
-   Enforce HTTPS in deployed environments.
-   Apply least-privilege access controls to authority and
    administrative roles.
-   Validate and sanitize all user-submitted data.
-   Protect location data with explicit consent, expiration, and access
    auditing.
-   Store passwords only as secure hashes.
-   Add rate limiting, centralized logging, monitoring, and security
    testing before production deployment.

## Future Enhancements

-   PostgreSQL deployment for production workloads
-   Real-time notifications through WebSockets or push messaging
-   Integration with verified emergency and law-enforcement systems
-   Advanced geospatial processing for geofenced zones
-   Mobile applications for tourists and authorities
-   Automated anomaly detection and risk scoring
-   Cloud deployment with CI/CD, observability, and disaster recovery

## Project Purpose

VeriTour aims to improve tourist safety and response coordination by
connecting travelers, emergency contacts, and authorized authorities
through structured digital workflows and secure information sharing.

## License

Add an appropriate license before publishing the repository publicly.
