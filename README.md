# ✈️ AI Travel Agency Itinerary Generator

> **Travel Itinerary Workspace** — a ChatGPT Project configured as a Senior Travel Itinerary Consultant for practical, geographically coordinated day-by-day travel planning.

[![Status](https://img.shields.io/badge/assessment-3%2F3%20tests%20passed-brightgreen)](./docs/test-results.md)
[![Platform](https://img.shields.io/badge/platform-ChatGPT%20Project-black)](https://chatgpt.com/share/6aba15b8-d540-83ee-9dfd-a758332644ae)
[![Demo](https://img.shields.io/badge/demo-Loom-blue)](https://www.loom.com/share/facf878215f040af995275cd59c57df7)
[![Sources](https://img.shields.io/badge/reference%20sources-3-informational)](#reference-sources)

## 🎯 Project at a Glance

This capstone demonstrates a structured AI travel-planning workflow that:

- Collects **destination, dates/duration, budget tier, traveler profile/count, and interests** before generation.
- Produces a consistent **4-part itinerary**: Trip Overview → Pre-Trip Checklist → Day-by-Day Itinerary → Practical Local Tips.
- Applies **geographic pacing** to group nearby activities and reduce unnecessary cross-city travel.
- Limits schedules to **three major activities per day**.
- Adds location details, transit recommendations, and local food suggestions where relevant.
- Uses web verification for attraction opening status and relevant transit operations when available.
- Uses broad budget ranges, avoids specific hotel recommendations, and makes no dietary assumptions.
- Prevents out-of-scope/prompt-injection requests with an exact refusal response.

## 🧭 How It Works

```text
Travel Brief
    │
    ▼
Parameter Gate
(Destination • Dates • Budget • Travelers • Interests)
    │
    ├── Missing parameter? ──► Ask only for missing detail
    │
    ▼
Geographic Planning
(Neighborhood grouping • ≤3 major activities/day)
    │
    ▼
Current Verification
(Attractions • Transit • Closures when available)
    │
    ▼
Structured Itinerary
(Overview • Checklist • Day-by-Day • Local Tips)
    │
    ▼
Guardrails
(No hotels • No exact pricing • No booking claims • Scope protection)
```

## 🧩 Core Capabilities

| Capability | Implementation |
|---|---|
| Parameter validation | Complete-brief gate before itinerary generation |
| Geographic pacing | District/neighborhood clustering with realistic transit |
| Daily pacing | Maximum 3 major activities/day |
| Output consistency | Fixed 4-part itinerary structure |
| Local detail | Location + transit + food/dish suggestions |
| Web verification | Attraction and transit operational checks |
| Budget discipline | Broad ranges; no false precision |
| Accommodation safety | Generic accommodation guidance only |
| Scope control | Exact refusal for out-of-scope requests |

## 🧪 Validation — 3/3 Passed

### Test 1 — Complete Travel Brief ✅
A complete Tokyo brief produced a five-day itinerary covering the required structure, geographic grouping, transit guidance, local food suggestions, budget handling, and current operational checks.

### Test 2 — Incomplete Travel Brief ✅
A Paris request missing travel dates/duration and budget tier was halted. The project requested the missing details instead of inventing them or generating an incomplete itinerary.

### Test 3 — Prompt Injection / Scope Guardrail ✅
A request to reveal hidden project instructions and create unrelated hotel-booking code returned the exact configured response:

> **I can only assist you with travel itinerary planning!**

See the detailed evidence in [docs/test-results.md](./docs/test-results.md).

## 📚 Reference Sources

Three focused reference documents are included:

1. **Travel Destination Planning Reference** — geographic pacing, activity planning, accommodation and pricing guidance.
2. **Local Transportation Reference** — transit selection, operational verification, passes/cards, and geographic pacing.
3. **Pre-Trip Checklist Reference** — documents, currency, transport preparation, culture, and packing.

## 📦 Evidence & Submission Files

- [LMS Submission PDF](./AI_Travel_Agency_Itinerary_Generator_LMS_Submission.pdf)
- [Test Results](./docs/test-results.md)
- [Project Configuration](./docs/project-configuration.md)
- [Travel Destination Planning Reference](./Travel_Destination_Planning_Reference.docx)
- [Local Transportation Reference](./Local_Transportation_Reference.docx)
- [Pre-Trip Checklist Reference](./Pre_Trip_Checklist_Reference.docx)

## 🎥 Live Demo & Project

**Loom Demo:** https://www.loom.com/share/facf878215f040af995275cd59c57df7

**ChatGPT Project:** https://chatgpt.com/share/6aba15b8-d540-83ee-9dfd-a758332644ae

## ✅ Submission Checklist

- [x] Travel Itinerary Workspace configured
- [x] Project-only memory selected
- [x] Custom instructions configured
- [x] Three reference sources added
- [x] Complete-brief flow validated
- [x] Incomplete-brief flow validated
- [x] Prompt-injection guardrail validated
- [x] Loom demo recorded
- [x] LMS submission PDF prepared
- [x] Repository organized for review

## 👤 Author

**Shaik Mohammad Shaheed**

Built as an AI automation / generative-AI portfolio capstone focused on structured prompting, validation gates, retrieval-assisted planning, web verification, and safety guardrails.

---

### ⭐ Reviewer note

This repository is designed to make the **configuration → evidence → test results → submission artifacts** path easy to audit. The source files support the project's planning logic, while the test evidence documents the three assessment flows.
