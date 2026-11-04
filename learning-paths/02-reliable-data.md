# 🔐 Path 02 — Correctness & data

[← All paths](README.md) · [🗃️ Transactions notes](../notes/concurrency-transactions.md)

**Goal:** understand how database choices protect business invariants during concurrent work.

| Step | Investigate | Evidence |
| --- | --- | --- |
| 1 | ACID and commit/rollback | A timeline with failure points |
| 2 | Read Committed vs Repeatable Read vs Serializable | An isolation anomaly comparison |
| 3 | Lost updates / write skew | A minimal interleaving that reproduces the problem |
| 4 | Optimistic version checks vs locking | A trade-off table with latency/retry implications |
| 5 | Unique constraints and retries | An explanation of the database-enforced invariant |

### 🧪 Dojo challenge

**100 clients, 1 seat.** Predict the result of 100 simultaneous reservations, then design two ways to guarantee no double booking. State which failure should be visible to the user.

### ✅ Explain it back

You can tell the difference between a *test that happened to pass* and a *database-enforced invariant*. You can justify your transaction and retry strategy.

**Related:** [Reservation Engine](https://github.com/the-engineering-dojo/reservation-engine)