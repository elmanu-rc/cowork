# GEMINI.md - CognitionBase Project Context

## Project Overview

**CognitionBase** is a digital product incubator and innovation engine for the **23people** group. Its primary goal is to eliminate the friction between conceptualization and market validation using a high-velocity, AI-augmented workflow called the **Iron-Legion Protocol**.

### Core Services

1. **Idea2Market:** A two-stage service to launch products.
    * **Idea2Landing (I2LP):** Transforms an idea into a functional landing page with an interactive demo in 7–10 days to validate market interest.
    * **Landing2MVP (L2MVP):** Builds a functional MVP in < 6 weeks if the landing page hits specific traction metrics.
2. **Technical Evaluations:** High-level technical assessment service for talent acquisition within the 23people ecosystem.

### Principles (Iron-Legion / GSD-Inspired)

* **Output-First:** Focus on functional success (Landing/MVP) over excessive documentation.
* **Atomic Decomposition:** Break ideas into small units that AI agents can execute in hours.
* **Bias for Action:** Prioritize deployment and iteration over perfect design.
* **Boring Tools:** Use stable, low-friction stacks (Next.js, Tailwind, Vercel) for maximum speed.

---

## Directory Structure & Usage

The project follows a strict organizational structure to manage the flow from idea to execution:

| Directory | Purpose | Rule |
| :--- | :--- | :--- |
| **`1 - Fleeting Docs/`** | **Mandatory Inbox.** | ALL new files/tasks MUST start here. |
| **`2 - References Docs/`** | External research and raw input data. | Investigation artifacts (e.g., GSD docs, company handbook). |
| **`3 - Permanent Docs/`** | Official, validated documentation. | Permanent and official files only. |

### Key Documentation Files

* **`docs/COGNITIONBASE-COMPANY.md`**: Mission, vision, and high-level service definitions.
* **`docs/services/I2LP-FLOW.md`**: Detailed step-by-step workflow for the Idea2Landing service.
* **`docs/services/I2LP-REQUEST-TEMPLATE.md`**: The mandatory template (`REQUEST.md`) required to initiate any new project.
* **`STRUCTURE.md`**: Core directory rules.
* **`CLAUDE.md`**: High-level technical summary and common commands.

---

## Operational Workflow (Idea2Landing)

All development work follows the sequence defined in `I2LP-FLOW.md`:

1. **Intake & Validation:** SRM (Service Request Manager) validates the `REQUEST.md`.
2. **Blueprint:** Lead Dev AI generates the master technical plan and GSD artifacts.
3. **Copy & Marketing Design:** AI agents generate copy based on strategic narrative.
4. **UI/UX Design:** AI agents design responsive layouts (mobile-first).
5. **Build:** Implementation using **Next.js + Tailwind + Vercel**.
6. **QA, SEO & Analytics:** Validation of Lighthouse scores and GA4 events.
7. **Deploy:** Production launch and client handoff.

---

## Development & Usage Guidelines

### Starting a New Project

To start a new project within CognitionBase:

1. Copy `docs/services/I2LP-REQUEST-TEMPLATE.md` to a new file in `fleeting-tasks/` (e.g., `fleeting-tasks/REQUEST-my-project.md`).
2. Fill out the **4 mandatory blocks**: Strategic Narrative, Marketing Data, Operational Data, and GSD Scope.
3. Ensure the `aha_moment_hipotesis` is written as a narrative scene, not a feature list.

### Standard Tech Stack (CB Standard)

* **Frontend:** Next.js + Tailwind CSS + TypeScript.
* **Deployment:** Vercel.
* **Analytics:** Google Analytics 4 (GA4).
* **Protocol Management:** GSD (Get Shit Done) commands (e.g., `/gsd-new-project`, `/gsd-plan-phase`).

### Working with the AI (Iron-Legion)

* Always reference the `REQUEST.md` for project-specific context.
* Use `PROJECT.md`, `REQUIREMENTS.md`, and `ROADMAP.md` as the source of truth for execution.
* Follow the "Discuss -> Plan -> Execute -> Verify" lifecycle for every phase.

---
*"Stop talking, start building. Done is better than perfect."*
