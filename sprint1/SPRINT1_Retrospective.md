# Sprint 1 Retrospective

**Sprint Dates:** January 20, 2026 — February 24, 2026  
**Team:** Sheala Miller, Jarl Evanson, Carlos Marquez, Jaylon Sanders, Cole Segura

---

## What Went Well

- **Docker environment:** Eventually got Docker building and running across team members' machines after working through platform-specific issues (Mac vs Windows, Apple Silicon).
- **Collaboration:** Regular scrum meetings kept the team aligned on blockers and next steps.
- **Fork selection:** As a group, agreed on a single fork to use for the project, reducing confusion.
- **Merge flow:** Successfully implemented approve, merge, and reject actions with field-level deduplication and audit logging.
- **Documentation:** CHANGES.md and BUILD_AND_TEST.md helped us and understand how to run the app when changes were made independently.
- **Security hardening:** Rate limiting, COOP policy, security headers, and SQL error sanitization completed as planned.

---

## What Didn't Go Well

- **Docker setup:** Initial Docker build failures, credential helper errors, missing `.env` file, and cross-platform differences caused significant delays.
- **Write access:** Some team members lacked write access to the GitHub repo early in the sprint.
- **Personal struggles with submission code:** Individual challenges understanding and modifying the inherited submission flow.
- **Inherited codebase:** Limited prior familiarity with Django, PostGIS, pgvector, and the existing data flow slowed initial progress.

---

## What Could Be Improved

- **Cross-platform testing:** Test Docker and environment setup on Mac and Windows earlier to catch platform issues sooner.
- **Architecture review:** Review inherited code and architecture before making changes to avoid rework.
- **Onboarding:** Start with clearer setup instructions and environment checklists so members can build quickly.
- **Sponsor alignment:** Ensure access to codebase and sponsor feedback earlier in the sprint.

---

## Challenges

| Challenge | Impact |
|-----------|--------|
| Docker build failures (permissions, credential helper, missing .env) | Delayed local development for several members |
| Write access to GitHub repo | Blocked some contributions until resolved |
| Understanding inherited Django/PostGIS structure | Slower ramp-up on submission and merge logic |
| Mac vs Windows Docker behavior | Required platform-specific fixes (e.g., `--platform=linux/amd64`) |
| DB schema mismatch (matched_resource FK) | Required workarounds in merge flow |
