# 🧠 Path 01 — Engineering foundations

[← All paths](README.md) · [🧩 DDD notes](../notes/ddd-and-boundaries.md)

**Goal:** design understandable services and recognize why boundaries matter.

| Step | Question | Practice | Evidence |
| --- | --- | --- | --- |
| 1. Domain language | What does a reservation mean? | Create a glossary with business stakeholders' terms | Ambiguous terms resolved |
| 2. Invariants | What must always be true? | List rules for reserve, expire, cancel | Rules have counterexamples |
| 3. Boundaries | What belongs in an aggregate? | Compare two domain models | Explicit trade-off notes |
| 4. Dependencies | What should know about infrastructure? | Draw dependency arrows | Explain where coupling exists |
| 5. Trade-offs | When is abstraction harmful? | Compare simpler and layered designs | One-page ADR |

### 🧪 Dojo challenge

Sketch two ways to model Seat Reservation: one transactionally consistent aggregate and one model with separate Reservation and Inventory boundaries. Discuss how each prevents double booking.

### ✅ Explain it back

You can explain DDD, aggregates, invariants, and dependency direction using **one concrete example**, without relying on buzzwords.

**Related:** [Reservation Engine](https://github.com/the-engineering-dojo/reservation-engine) · [Learning note template](../templates/learning-note.md)