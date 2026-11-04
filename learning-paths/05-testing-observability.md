# 🧪 Path 05 — Testing, performance & observability

[← All paths](README.md)

**Goal:** replace intuition with reproducible evidence.

| Practice | What it answers |
| --- | --- |
| Unit tests | Does domain logic behave correctly for a controlled input? |
| Integration tests | Does the database or broker obey our assumptions? |
| Contract tests | Can independently changed components still communicate? |
| Property / mutation tests | How strong are the behavioral checks? |
| Load tests | What happens to throughput, latency, and errors as traffic grows? |
| Tracing and metrics | Where time is spent and what failed |
| Fault injection | Does the system recover from an expected failure? |

### 📈 Reporting a performance experiment

Always include: machine/environment, dataset, traffic pattern, warmup, duration, concurrency, **p50/p95/p99**, error rate, and a baseline. Never present a single impressive RPS number without context.

### 🧪 Dojo challenge

Propose a load test comparing two concurrency strategies. Define pass/fail behavior **before** running it and identify what would invalidate the comparison.

### ✅ Explain it back

You can connect a metric to a hypothesis, discuss confounders, and decide what experiment to run next.