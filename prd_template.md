# Product Requirements Document (PRD)

> How to use this template
>
> - Keep headings and section order; delete guidance text as you fill it in.
> - Follow repo Markdown lint rules (H1 on first line, no trailing punctuation in headings, no bare URLs).
> - Prefer links like <https://example.com> and keep line length ~100 chars.
>
## 1. Document Information

- Product/Feature Name: Church Connect+
- Author(s): Melvin Nieves Rivera
- Date Created: TODO (9/13)
- Last Updated: TODO (9/21)
- Version: 0.1 (Draft)

---

## 2. Overview

- Summary: Church Connect+ is a lightweight, Django-based application designed for small to mid-sized churches. It improves community engagement and administrative efficiency by offering prayer request management, youth group sign-ups with attendance tracking, digital tithes and offerings, and a centralized announcements board.

- Problem Statement: Small congregations lack affordable, simple, and accessible tools to track youth engagement, manage prayer requests, collect digital offerings, and distribute announcements. Existing commercial church management tools are too expensive and overly complex.
  
- Goals & Objectives:
 - Increase youth engagement and sign-up consistency.
 - Provide transparent, centralized prayer request tracking.
 - Enable secure and convenient digital giving.
 - Streamline weekly announcements for leaders and members.

- Non-Goals:
  - Not a full-scale church management suite.
  - Not offering livestreaming, sermon archiving, or advanced accounting features in MVP.


---

## 3. Context & Background

- Business Context: Aligns with faith community goals of engagement, transparency, and connection. Serves as a portfolio-ready project for showcasing Django CRUD, authentication, and workflow logic.

- Market/Customer Insights: Pew Research (2024) shows congregations adopting digital tools; Lifeway Research (2023) highlights youth attendance struggles; Barna (2022) emphasizes digital giving trends.

- Competitive/Benchmark References: Unlike enterprise-level tools, Church Connect+ focuses only on the 4 features churches need most.

---

## 4. Scope

- In Scope:
  - Prayer requests module with moderation and “answered” toggle.
  - Youth group sign-ups with attendance logs.
  - Digital giving integration via Zelle + donation log.
  - Announcements board for weekly updates.

- Out of Scope: Bullet list of excluded items to prevent ambiguity.
  - Accounting/budgeting tools.
  - Personalized profiles.
  - Mobile apps, livestreaming, or media management.

---

## 5. User Stories & Use Cases

- Primary User Persona(s):
  - Youth members and parents.
  - Congregation members.
  - Church leaders/pastors.
  - Finance/admin staff.

- User Stories:
  - As a youth member, I want sign up for events so I can attend consistently.
  - As a congregation member, I want to submit prayer requests so the church can support me.
  - As a finance staff member, I want to track donations so I can report transparently.
  - As a leader, I want to post announcements so members stay informed.

- Use Case Scenarios: Happy path and 1–2 edge cases.
  - Happy path: Member logs in > submits prayer request > leader approves > congregation views.
  - Edge case: Youth signs up for event but slot is full > receives error message.
 
---

## 6. Functional Requirements

- FR-001: Users can create, read, update, and delete prayer requests (with leader moderation).
- FR-002: Users can sign up for youth events and attendance can be logged.
- FR-003: Members can access a secure embedded link for digital giving.
- FR-004: Leaders can post, edit, and delete announcements.

> Tip: Tie each FR to a user story or acceptance criteria below.

---

## 7. Non-Functional Requirements

- Performance: Load times under 2s per page.
- Scalability: Handle 100 concurrent users.
- Accessibility: WCAG 2.2 compliance (keyboard navigation, contrast).
- Security/Compliance: Encrypted donations, secure logins, privacy for sensitive prayer requests.
- Reliability/Availability: 99% uptime for prayer/announcement modules.

---

## 8. Dependencies

- Django framework
- Zelle or similar digital banking APIs.
- GitHub repo for hosting code.

---

## 9. Risks & Assumptions

- Risks: Low adoption of digital giving; youth may not sign up consistently; privacy concerns with prayer requests; risk of scope creep.
- Assumptions: Congregation members have smartphones/internet; leaders can moderate requests weekly.

---

## 10. Acceptance Criteria

- Clear, testable conditions for acceptance.
  - FR-001: Passes if members can submit prayer requests, and leaders can approve/deny them.
  - FR-002: Passes if youth can sign up for an event and attendance is logged successfully.
  - FR-003: Passes if members can complete a donation via embedded Zelle link and log is generated.
  - FR-004: Passes if announcements can be added, viewed, and deleted without error.
    
---

## 11. Success Metrics

- 20% increase in youth sign-ups.
- At least 25% of offerings submitted digitally.
- Weekly export of prayer and donation logs.
- Leaders reduce bulletin prep time by 30–40%.

---

## 12. Rollout & Release Plan

-Phasing:
  - Week 1: Prayer requests + announcements.
  - Week 2: Youth sign-ups + digital giving.
- Release Channels: Demo via GitHub repo and class presentation.
- Training/Documentation Needs: README instructions + lightweight support guide for church staff.

---

## 13. Open Questions

- Should advanced permissions (roles: admin vs member) be part of MVP?
- Should donations include automatic receipts or manual logging only?

---

## 14. References

- Pew Research (2024), Lifeway (2023), Barna (2022).
- WCAG 2.2 standards.
- Layman, Understand Django
- RealPython: https://realpython.com/build-a-blog-from-scratch-django/
