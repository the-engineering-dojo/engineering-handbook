# 🔐 Transactions, concurrency & consistency

[← Notes](README.md) · [🔒 Data path](../learning-paths/02-reliable-data.md)

### The engineering problem

Two requests read “seat available” at roughly the same time. If both write without a conflict rule, both may think they succeeded.

**A mutex inside one API process is not a reliable cross-replica solution.**

### Common tools

| Tool | What it helps with | What it does not guarantee on its own |
| --- | --- | --- |
| DB unique constraint | Prevent conflicting persisted rows | A great user error message |
| Optimistic versioning | Detect concurrent updates | Progress without contention retries |
| Row locking | Coordinate writers on particular rows | Correct lock scope or deadlock avoidance |
| Serializable transactions | Strong isolation for transaction behavior | No serialization failures or retry needs |
| Idempotency keys | Avoid repeating an effect for the same operation | Global inventory consistency |

### 🧪 Thought experiment

Client A reserves seat 42; client B races it. What precise DB constraint or version check prevents both from committing? What HTTP status will the loser receive? What if the first response is lost and the client retries?

### ✅ Prove the invariant

A concurrency test is useful, but passing once is insufficient. Combine repeatable stress, integration tests, and a database-level reason the conflicting state cannot persist.

### 📎 Learn more

[PostgreSQL: Transaction Isolation](https://www.postgresql.org/docs/current/transaction-iso.html) · [PostgreSQL: Explicit Locking](https://www.postgresql.org/docs/current/explicit-locking.html)