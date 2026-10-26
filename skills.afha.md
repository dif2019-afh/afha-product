# skills.afha — Product Requirements + Skill Document

> **How to use this:** I am the product manager and Claude is my engineer. This document is the brief that sets up the engineer to build what I think my user needs. Update it whenever I learn something new.

---

## 1. One-Line Summary

**Solon Live** helps **residential care home owners** place high-quality caregivers and residents into their facility **so they can operate effectively with peace of mind**.

## 2. The User (Initial Customer Segment)

A residential care home owner, typically with under one year of experience, who cares for **6 beds in Washington State** and manages **at least two caregivers**.

## 3. The Need

**Problem statement:** Today, my user relies on word of mouth, WhatsApp group chats, and sporadic outreach to discharge managers to find qualified caregivers and residents for their community.

This falls short because owners are left taking a risk on a match that may not be mutually beneficial for the organization. They then experience the problem firsthand while still developing their residential community, which creates setbacks like inspections, resident complaints, and overall disruption to fast-tracking their business revenue.

## 4. Value Propositions *(to tighten)*

- Quality Caregiver Matching
- Quality Patient Referral Network
- Sleep with Surveillance
- Safety Rails Against Citations
- Clear Your Time
- Residential Safety

## 5. User Stories

**Persona: Amara**, a first-year owner of a six-bed adult family home in Washington who manages two caregivers, often while working or studying, and doesn't always live on site.

### Epic 1: Fill beds with the right residents (Matches)

| # | Story | Done when | Source |
|---|-------|-----------|--------|
| 1.1 | As Amara, I want to fill my open beds quickly, so that my revenue covers my staff and house costs. | Amara can see residents who match her home and request an introduction. | Laura |
| 1.2 | As Amara, I want people seeking placement to find my home, so that I can get my first residents without an established reputation. | Amara's home profile, including her specialties and open beds, is visible to referral sources. | Hiwot |
| 1.3 | As Amara, I want to reach residents seeking placement without hours of outreach, so that I can grow my business around my other commitments. | Amara can view all matched residents in one list without contacting each source separately. | Hiwot |
| 1.4 | As Amara, I want referral sources to know which residents my home is equipped to care for, so that I'm the first call for placements that fit. | Amara's accepted care types, such as hospice and challenging behaviors, appear on her home profile. | Josie |
| 1.5 | As Amara, I want to meet a potential resident before admitting them, so that each new resident fits with the household. | Amara can request a meeting from a resident lead. | Josie |
| 1.6 | As Amara, I want to know about a resident's past complaints or red flags before admitting them, so that I avoid placements that lead to investigations and citations. | Any history of complaints or frequent moves appears on the lead before Amara requests an intro. | Josie |

### Epic 2: Hire and keep quality caregivers (Matches)

| # | Story | Done when | Source |
|---|-------|-----------|--------|
| 2.1 | As Amara, I want to know whether a candidate has the skills and genuine care for seniors before I hire them, so that I don't hire someone who gets frustrated or disconnects from residents. | Each candidate shows their certification, training, experience, and why they do this work. | Hiwot |
| 2.2 | As Amara, I want to cover open shifts with caregivers I trust, so that I'm not filling in myself and residents are safe when I'm not on site. | Amara can see candidates available for the specific shifts she needs filled. | Robin |
| 2.3 | As Amara, I want to hire caregivers who are committed to adult family home work, so that I don't settle for staff below my standards or risk closing my home. | Candidates shown are actively seeking adult family home roles. | Robin |
| 2.4 | As Amara, I want to recommend a great caregiver I no longer need to other owners, so that good caregivers stay in the industry. | Amara can refer a caregiver into the candidate pool with a recommendation. | Robin |
| 2.5 | As Amara, I want to find a resident manager recommended by other owners in my area, so that I can fill the role quickly with someone trusted. | Amara can see candidates recommended by other owners, filtered by location. | Robin |

### Epic 3: Admit residents compliantly (Care Plan Builder)

| # | Story | Done when | Source |
|---|-------|-----------|--------|
| 3.1 | As Amara, I want to understand the responsibilities the state class didn't cover, so that I stay compliant without learning through citations. | Amara is guided through each required step when admitting a new resident. | Laura |

### Epic 4: Trust my caregivers' work (Caregiver Training)

| # | Story | Done when | Source |
|---|-------|-----------|--------|
| 4.1 | As Amara, I want to know my caregivers are prepared for the hard parts of the job, so that I can trust their care and justify paying them more. | Amara can see which training modules each caregiver has completed. | Laura |

### Stories out of scope for now

- As Amara, I want to manage caregiver hours and resident records without switching between systems, so that I spend less time on admin. *(Hiwot)*
- As Amara, I want to plan meals for residents with different diets in less time, so that I get hours back each week. *(Robin)*
- As Amara, I want to learn what's working for other homes to fill their beds, so that I can compete in a crowded market. *(Robin)*
- As Daniel, a caregiver planning to open his own home, I want to know how much competition exists in different areas, so that I open where there's enough demand to fill my beds. *(Robin)*

> *Note:* The Daniel story uses a second persona. Someone planning to open a home is a different user than the initial customer segment, which is another reason it belongs out of scope.

## 6. Out of Scope

- Do not build a conversation history
- Do not build a complex product from scratch
- Do not build unnecessary technical infrastructure by default
- Do not build a complex UI/UX
- Do not build unnecessary features
- Do not build a Retrieval Augmented Generation (RAG) pipeline using a made-up vector database to inject document snippets into the prompt
- Do not build rate limiting or cost tracking infrastructure (no middleware for per-user token usage, no API rate-limit management, no caching layer such as Redis)

## 7. Constraints and Assumptions

- **Fake data only.** Not HIPAA compliant; not for real residents or real caregiver records.
- **Washington State only.**
- **Web app that works on a phone screen.**
