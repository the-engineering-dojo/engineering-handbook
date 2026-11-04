# 🐳 Path 04 — Cloud-native engineering

[← All paths](README.md) · [☸️ Docker & Kubernetes notes](../notes/docker-vs-kubernetes.md)

**Goal:** understand packaging, deployment, scaling, and operating services.

| Stage | Learn | Prove |
| --- | --- | --- |
| Docker | Images, layers, networks, volumes, non-root runtime | Explain what survives container restart |
| Compose | Local multi-service integration | Describe dependency readiness vs startup order |
| Kubernetes | Deployments, Services, ConfigMaps, Secrets | Explain routing to multiple pods |
| Reliability | Probes, limits, requests, rollout/rollback | Describe how a failing pod is handled |
| Statelessness | Externalized session and reservation data | Show why per-process in-memory state causes divergent results |
| Operations | Logs, metrics, traces | Trace one request across boundaries |

### 🧪 Dojo challenge

Imagine two API pods behind a Kubernetes Service. Each keeps a local set of reserved seats. Can two users reserve the same seat? Explain why. Then propose a persistent consistency boundary.

### ✅ Explain it back

You understand why **Kubernetes scales processes, not correctness guarantees**. You can state a resource's ownership and persistence requirements.

**Related:** [Reservation Engine](https://github.com/the-engineering-dojo/reservation-engine)