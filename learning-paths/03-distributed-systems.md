# 📨 Path 03 — Distributed systems

[← All paths](README.md) · [🔀 Microservices notes](../notes/microservices-when-and-why.md)

**Goal:** reason about coordination when processes fail independently.

| Step | Engineering problem | Experiment |
| --- | --- | --- |
| 1 | Network timeouts & retries | Simulate response loss after a successful operation |
| 2 | Duplicate messages | Deliver the same message twice and check effects |
| 3 | Outbox + Inbox | Draw failure windows between DB commit and publish |
| 4 | Ordering & eventual consistency | Observe stale read models and define acceptable lag |
| 5 | Dead-letter handling | Plan recovery without silent message loss |
| 6 | Ownership of data | Identify where a shared database creates coupling |

### 🔎 Questions worth debating

- Can exactly-once **effects** be achieved despite at-least-once delivery?
- Should reservation creation wait synchronously for pricing or notification?
- What is the difference between a saga and a single ACID transaction?

### ✅ Explain it back

You can model a failure timeline and describe the consistency guarantee—not just draw service boxes.

**Related:** [Reservation Engine roadmap](https://github.com/the-engineering-dojo/reservation-engine/blob/main/docs/roadmap.md)