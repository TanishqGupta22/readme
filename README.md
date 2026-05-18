
---

## 1. Project Overview

### 1.1 Platform Description
**HireConnect** is an enterprise-grade, highly scalable job portal and recruitment orchestration platform. Designed on a decentralized microservices architecture, it bridges the gap between candidates searching for career opportunities and recruiters managing hiring pipelines. The application separates operational domains (authentication, profile, job posting, application tracking, interview scheduling, notifications, billing, and system telemetry) into independent, fine-grained microservices.

### 1.2 Core Capabilities & Value Proposition
- **Dynamic Profile Portability**: Candidates build robust profiles showcasing skills, professional history, and educational backgrounds, with integrated resume storage.
- **Quota-Restricted Job Publishing**: Recruiters post job requisitions governed by active monetization plans and real-time usage quotas.
- **Asynchronous Pipeline Telemetry**: Real-time notifications keep candidates and recruiters aligned when job states update, applications are submitted, or interviews are scheduled.
- **System-Wide Analytics**: Interactive dashboards aggregate high-performance operational metrics and business intelligence diagrams across multiple transactional databases.

### 1.3 System Roles & Permissions Matrix
The platform enforces strict role separation at both the API Gateway and service levels:

```
+------------------+----------------------------------------------------------------------------------+
| Role             | Permissions & Scope                                                              |
+------------------+----------------------------------------------------------------------------------+
| CANDIDATE        | - Authenticate, build/update personal profiles, and upload resumes.              |
|                  | - Search, filter, and apply for open job postings.                               |
|                  | - Track job application statuses (Applied, Reviewing, Shortlisted, Hired).        |
|                  | - View interview invites, confirm availability, and receive alerts.              |
+------------------+----------------------------------------------------------------------------------+
| RECRUITER        | - Set up company profiles, logos, and contact information.                       |
|                  | - Purchase, renew, or upgrade subscription plans (Free, Professional, Enterprise).|
|                  | - Create, edit, and deactivate job listings (restricted by subscription quotas).  |
|                  | - Review, filter, and shortlist job applications.                                |
|                  | - Schedule, reschedule, or cancel candidate interviews.                          |
|                  | - Access recruiter dashboard analytics (views, conversion rates, hiring counts). |
+------------------+----------------------------------------------------------------------------------+
| ADMIN            | - Moderate users, profiles, and job postings across the entire platform.         |
|                  | - Access master administrative console with financial and user telemetry.        |
|                  | - Send bulk operational alerts and system-wide notifications.                    |
|                  | - Track revenue generation and active subscription plan distributions.          |
+------------------+----------------------------------------------------------------------------------+
```

---
