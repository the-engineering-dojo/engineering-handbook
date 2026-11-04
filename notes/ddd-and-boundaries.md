# 🧩 DDD & domain boundaries

[← Notes](README.md) · [🎟️ Practice case](https://github.com/the-engineering-dojo/reservation-engine)

### 🧠 The idea

Domain-Driven Design is about representing business behavior and language accurately. It is **not** a folder template or a requirement to add repositories, services, and interfaces everywhere.

| Concept | Reservation example |
| --- | --- |
| Ubiquitous language | Hold, Reservation, Expiration, Confirmed |
| Invariant | An individual seat cannot have two simultaneously active, conflicting reservations |
| Aggregate | A consistency boundary enforcing rules within a transaction |
| Bounded context | A domain-language boundary, not necessarily a separate microservice |
| Domain event | Something meaningful that has already happened, e.g. ReservationConfirmed |

### 🔬 Compare these alternatives

- **Seat as aggregate:** seat availability is controlled where conflicts occur.
- **Reservation as aggregate with DB constraint:** the database enforces uniqueness while reservations hold lifecycle rules.

Neither is automatically correct. Consider transaction scope, event volume, persistence shape, and operational complexity.

### 💬 Discuss

What does “reserved” mean: held temporarily, paid, or confirmed? How do TTL and cancellation alter the invariant?

### 📎 Learn more

[Microsoft: Domain model / microservice design](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/) · [Learning note template](../templates/learning-note.md)