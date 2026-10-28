---
name: solon-live
description: Product requirements for Solon Live, a phone-friendly web prototype that helps first-year adult family home owners in Washington state find and keep qualified caregivers. Read this before building, changing, or reviewing any feature in this repository.
---

# Solon Live

Product requirements and working instructions for Claude. The product manager owns this file; Claude acts as the engineer. Update it whenever you learn something new from owners.

## 1. One-line summary

Solon Live helps residential care home owners place high-quality caregivers into their facility so they can operate with peace of mind.

## 2. The user (initial customer segment)

Owners of a single residential care facility (an adult family home) in Washington state who:

- typically have under one year of experience,
- care for 6 beds, and
- manage at least two caregivers.

## 3. The need

Today these owners find caregivers through word of mouth, WhatsApp group chats, and sporadic outreach to discharge managers. This falls short: owners take a risk on every match, and a bad match creates problems inside the home. Setbacks include inspections, citations, resident complaints, and disruption to administrative work such as reimbursement, marketing, housekeeping, and negotiated care plans.

## 4. Value propositions

- **Quality caregiver matching:** see candidates with the skills, training, and commitment your home needs.
- **Peace of mind when you’re off site:** trust that open shifts are covered by caregivers you’ve vetted.
- **Safety rails against citations:** know each caregiver’s certification and training status before an inspector asks.
- **Time back:** spend less time recruiting and more time running your home.
- **Resident safety:** residents are cared for by prepared, committed staff.

## 5. User stories

**Persona:** Amanda, a first-year owner of a six-bed adult family home in Washington who manages two caregivers and doesn’t always live on site.

1. As Amanda, I want to know whether a candidate has the skills and genuine care for seniors before I hire them, so that I don’t hire someone who gets frustrated or disconnects from residents. *(Source: interview H)*
   **Done when:** each candidate shows their certification, training, experience, and why they do this work.

2. As Amanda, I want to hire caregivers who are committed to adult family home work, so that I don’t settle for staff below my standards or risk closing my home. *(Source: interview R)*
   **Done when:** candidates shown are actively seeking adult family home roles.

3. As Amanda, I want to cover open shifts with caregivers I trust, so that I’m not filling in myself and residents are safe when I’m not on site. *(Source: interview R)*
   **Done when:** Amanda can see qualified candidates available for the specific shifts she needs.

4. As Amanda, I want to find caregivers recommended by other owners, so that I can fill roles quickly with someone already trusted. *(Source: interview R)*
   **Done when:** Amanda can see which candidates were referred by other owners in her area.

5. As Amanda, I want to know my caregivers are prepared for the hard parts of the job, so that I can trust their care and justify paying them more. *(Source: interview L)*
   **Done when:** Amanda can see which training each caregiver has completed.

6. As Amanda, I want confidence that my caregivers follow state requirements, so that my home passes inspections and avoids citations. *(Sources: interviews L and J)*
   **Done when:** Amanda can see each caregiver’s certification status and any upcoming renewal dates.

## 6. Out of scope

Do not build:

- conversation history,
- a complex product from scratch,
- unnecessary technical infrastructure,
- a complex UI or UX,
- features that aren’t tied to a user story above,
- a retrieval-augmented generation (RAG) pipeline or vector database,
- rate limiting, token or cost tracking middleware, or caching layers such as Redis.

## 7. Constraints and assumptions

- Fake data only. Not HIPAA compliant. Never use real resident or caregiver records.
- Washington state only.
- A web app that works on a phone screen.

## 8. How Claude should work in this repo

- Before writing code, check which user story the change serves. If it serves none, ask before building it.
- Prefer the simplest thing that meets the story’s “Done when” line: plain HTML, CSS, and JavaScript, no build step, hostable as a static site.
- Keep all sample data clearly fake and in one place.
- Washington care rules change. Label any certification or training deadlines as simplified and tell the user to confirm them with WA DSHS.
- After a change, say which “Done when” lines are now met and which are not.
