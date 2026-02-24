# Sprint Planning Document — Sprint 1

## CareBot: Caregiver Connect — Crowdsourcing Team

**Sprint Dates:** January 20, 2026 — February 24, 2026  
**Team Members:** Sheala Miller, Jarl Evanson, Carlos Marquez, Jaylon Sanders, Cole Segura

---

## High-Level Project Overview

### Project Mission

CareBot is committed to providing an AI-powered platform that helps caregivers, social workers, and families quickly find reliable local resources before they reach a crisis. We crowdsource resource recommendations, moderate submissions, and maintain a high-quality database of Alabama healthcare and social services.

### Problems We Are Solving

- **Resource discovery:** Caregivers and families struggle to find local healthcare resources (providers, programs, support services) when they need them.
- **Data quality:** Community-submitted resources need validation, deduplication, and structured merge to avoid duplicate or outdated entries.
- **Rural access:** Gaps exist in counties with limited or scattered services; the platform surfaces resources across Alabama.
- **Trust & moderation:** Submissions must be reviewed and integrated into the database in a controlled, auditable way.

### Project Overview (High-Level Features)

- **Django web application** (PostgreSQL, PostGIS, pgvector)
  - **AI chatbot:** Google Gemini–powered conversational search for healthcare resources.
  - **Resource submission:** Public form for community members to suggest new resources (provider name, service type, contact info, etc.).
  - **Moderation workflow:** Queue of pending submissions with similarity scores against existing resources.
  - **Moderation actions:** Approve as new resource, merge into existing resource (field-level merge), or reject.
  - **Similarity search:** Semantic search using pgvector and sentence transformers for deduplication and matching.
- **Development & operations**
  - Docker Compose for local development (Mac and Windows).
  - Security improvements (rate limiting, COOP policy, security headers, sanitized error messages).
  - Documentation (CHANGES.md, build guide) and onboarding for new team members.

---

## Sprint 1 Goals (3–4 sentences)

Sprint 1 focused on rebuilding the resource submission and moderation system, enabling community submissions to flow into a moderation queue where moderators can approve, merge, or reject. We prioritized fixing the public submission form, implementing merge functionality with field-level deduplication, improving Docker portability across Mac and Windows, and applying initial security hardening. The team also produced documentation and setup guides to support onboarding and future development. Also a majority of our work was just researching Docker usage and familiarizing ourselves with the code.

---

## Sprint 1 Scope

| Priority | Goal | Status |
|----------|------|--------|
| P0 | Fix resource submission flow | Done |
| P0 | Implement merge functionality (approve, merge, reject) | Done |
| P1 | Improve Docker environment (Mac + Windows) | Done |
| P1 | Initial security improvements | Done |
| P2 | Documentation & onboarding | Done |
