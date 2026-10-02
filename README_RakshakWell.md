# RakshakWell — AI-Powered Personnel Stress & Welfare Monitoring System

## Overview
RakshakWell is an AI-enabled, privacy-first personnel welfare platform designed for high-stress organizations such as CAPFs, Armed Forces, police organizations, disaster-response teams, and other uniformed services.

The platform aims to identify early indicators of occupational stress, burnout, emotional fatigue, and welfare concerns using authorized organizational data and voluntary wellness information. It supports timely, human-led welfare intervention while protecting sensitive information.

## Problem
Personnel in uniformed services may experience prolonged deployments, irregular duty schedules, operational pressure, heavy workloads, separation from families, and exposure to traumatic situations. Traditional stress identification can depend on manual observation or self-reporting, which may delay support.

RakshakWell provides a proactive digital approach that helps authorized welfare teams identify patterns that may require attention.

## Objectives
- Identify early indicators of stress and burnout.
- Analyze workload, deployment, leave, and duty-pattern trends.
- Provide secure voluntary wellness self-assessments.
- Generate explainable AI-based risk indicators.
- Recommend appropriate welfare interventions.
- Support authorized welfare officers with actionable dashboards.
- Protect confidentiality through privacy-preserving architecture.
- Separate welfare support from disciplinary action.

## Major Features

### Personnel Wellness Dashboard
- Workforce wellness overview
- Stress and burnout trends
- Risk distribution
- Deployment and workload analytics
- Intervention tracking

### AI Risk Assessment Engine
The prototype combines indicators such as workload intensity, deployment exposure, leave patterns, fatigue/sleep signals, and voluntary stress assessments to produce an indicative risk score and level.

> The prototype is a decision-support demonstration, not a medical diagnostic system.

### Wellness Self-Assessment
Personnel can voluntarily provide approved information about stress, fatigue, sleep, mood, and general wellness.

### Welfare Recommendation Engine
Potential recommendations include counseling referral, rest/recovery review, workload review, wellness resources, peer support, and follow-up assessments.

### Intervention Management
Authorized officers can create, assign, track, and close welfare interventions.

### Privacy & Security
- Role-Based Access Control (RBAC)
- Authentication and authorization
- Data minimization
- Anonymization/pseudonymization
- Consent management
- Secure storage
- Audit logging
- Restricted access to sensitive information

## System Architecture

```text
 Web / Mobile UI
       |
       v
 REST API — Node.js + Express
       |
  +----+---------+----------------+
  |              |                |
Personnel     AI/Analytics    Interventions
Data             Engine            |
  |              |                |
  +--------------+----------------+
                 |
          Secure Database
```

## Suggested Technology Stack

**Frontend:** React, Vite, JavaScript, HTML5/CSS3, Recharts

**Backend:** Node.js, Express.js, REST APIs, JWT authentication

**Prototype Database:** SQLite + Better-SQLite3

**Production Database:** PostgreSQL with encrypted storage and backups

**Production AI/ML:** Python, FastAPI, Scikit-learn/XGBoost, explainable AI and model monitoring

## Core Data Flow

```text
Authorized HR / Operational Data
              +
Voluntary Wellness Data
              ↓
      Secure Data Processing
              ↓
       Feature Extraction
              ↓
      Behavioral Analytics
              ↓
       Risk Assessment
              ↓
   Explainable Risk Factors
              ↓
 Welfare Recommendation Engine
              ↓
 Authorized Human Review
              ↓
      Welfare Intervention
              ↓
        Follow-up / Outcome
```

## User Roles

### Personnel
Complete voluntary assessments, view permitted personal wellness information, and access wellness resources.

### Welfare Officer
Review authorized welfare indicators, risk factors, alerts, and welfare interventions.

### Commander / Authorized Manager
View appropriate aggregated trends and support workload balancing.

### Administrator
Manage users, roles, configuration, security settings, and audit logs.

## Ethical AI Principles
1. Welfare first.
2. Human-in-the-loop decision making.
3. Explainable risk indicators.
4. Privacy by design.
5. Consent and appropriate authorization.
6. Bias and fairness evaluation.
7. No medical diagnosis.
8. No automatic disciplinary action.

## SIH Demonstration Flow
1. Login as Welfare Officer.
2. Open the Personnel Wellness Dashboard.
3. Review workforce wellness and workload trends.
4. Run/view AI risk assessment.
5. Open a personnel profile.
6. Review explainable contributing factors.
7. Generate a welfare recommendation.
8. Create a welfare intervention.
9. Submit a voluntary wellness assessment.
10. Review intervention status and audit trail.
11. Demonstrate privacy and role-based access.

## Example Risk Interpretation

```text
Workload          → Elevated
Deployment        → Elevated
Leave utilization → Low
Sleep/Fatigue     → Elevated
Stress assessment → Elevated
                    ↓
              Risk Indicator
                    ↓
          Human Welfare Review
```

The output is an early-warning indicator, not proof of a psychological disorder.

## Project Structure

```text
rakshakwell/
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
├── backend/
│   ├── server.js
│   ├── package.json
│   └── .env.example
├── README.md
└── deployment/
```

## Local Development

### Prerequisites
- Node.js 18+
- npm
- Git

### Backend

```bash
cd backend
npm install
```

Create `.env` from `.env.example`, then:

```bash
npm run dev
```

### Frontend

In another terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the Vite URL shown in the terminal, typically:

```text
http://localhost:5173
```

## Demo Accounts

| Role | Email | Password |
|---|---|---|
| Welfare Officer | welfare@rakshakwell.demo | Welfare@123 |
| Administrator | admin@rakshakwell.demo | Admin@123 |
| Personnel | personnel@rakshakwell.demo | Personnel@123 |

These credentials are for prototype demonstrations only.

## Production Roadmap

### AI/ML
- Train on ethically governed datasets.
- Validate and calibrate models.
- Test for bias and fairness.
- Add explainability.
- Monitor model drift.
- Maintain human review.

### Infrastructure
- PostgreSQL
- HTTPS/TLS
- Secrets management
- Encrypted backups
- Disaster recovery

### Security
- Multi-factor authentication
- Fine-grained RBAC/ABAC
- Security monitoring
- Vulnerability testing
- Immutable audit logs

### Privacy
- Data minimization
- Purpose limitation
- Retention/deletion policies
- Consent workflows
- Pseudonymized analytics
- Separation of welfare and disciplinary information

### Integrations
- HRMS
- Secure personnel-management APIs
- Approved wearable/biometric sources
- Enterprise identity providers
- Notification services

## Expected Impact
- Earlier welfare intervention
- Better workload distribution
- Reduced occupational fatigue
- Improved personnel well-being
- Stronger workforce resilience
- Evidence-based welfare planning
- Better allocation of welfare resources
- Improved organizational readiness

## Future Enhancements
- Native Android/iOS application
- Indian-language support
- Time-series stress prediction
- Privacy-preserving/federated learning
- Secure wearable integration
- Offline-first assessments
- Advanced workload balancing
- Explainable AI reports

## Disclaimer
RakshakWell is a prototype and decision-support platform. AI-generated risk indicators must not be treated as medical diagnoses or definitive assessments of mental health. Real-world interventions should be reviewed by appropriately authorized and qualified personnel.

Sensitive personnel, biometric, health, or psychological information must only be collected, processed, stored, and shared according to applicable laws, organizational policies, consent requirements, security standards, and ethical guidelines.

## Project Vision
**Transform personnel welfare from reactive observation to proactive, privacy-preserving support — identifying potential welfare concerns early while protecting dignity, confidentiality, and trust.**
