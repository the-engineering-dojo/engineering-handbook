# 📨 Microservices — when and why?

[← Notes](README.md) · [📨 Distributed path](../learning-paths/03-distributed-systems.md)

**Microservices are a way to distribute ownership and change—not a learning badge earned by adding HTTP calls.**

### 📌 Before splitting

Ask: which capabilities change independently? Which team owns them? What data must remain strongly consistent? Is a network boundary worth the latency, fault handling, and operations cost?

| Approach | Benefits | Costs |
| --- | --- | --- |
| Modular monolith | Straightforward local transactions, easy debug, fewer moving parts | Requires discipline to keep modules separated |
| Independently deployable services | Independent releases and scaling, explicit ownership | Timeouts, partial failures, contract versioning, operational overhead |

### 🧪 Practice sequence

1. Define Booking, Inventory, and Notification modules without a network.
2. Identify a feature that needs independent deployment or failure isolation.
3. Move the least consistency-sensitive capability out first.
4. Compare operation traces, failure scenarios, and deployment complexity.
5. Keep transactionally sensitive state within an explicit owner.

### ⚠️ Watch out for

Distributed monoliths, synchronous request chains, shared DB writes, and “exactly once” claims without a clearly specified effect.

**Question for the team:** Is pricing an independent domain capability or simply a deterministic function inside checkout? Justify both possibilities.

### 📎 Learn more

[Microsoft: Microservices architecture](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/)