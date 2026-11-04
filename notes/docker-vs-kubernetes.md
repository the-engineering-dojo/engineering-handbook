# 🐳 Docker vs. Kubernetes

[← Notes](README.md) · [☸️ Cloud-native path](../learning-paths/04-cloud-native.md)

A useful mental model: **a container packages and isolates a process; Kubernetes coordinates running workloads across machines.** They address different problems.

| Technology | Core learning question |
| --- | --- |
| Docker image | Which files/dependencies are needed to run a repeatable process? |
| Docker Compose | How can multiple containers communicate on one development machine? |
| Kubernetes Deployment | What keeps the desired replica count running? |
| Kubernetes Service | How do clients reach a group of pod endpoints? |
| Probes | How does the scheduler distinguish running from ready? |
| Volumes | What data should survive a container restart? |

### 🎯 Key experiment

Two API replicas, each with local in-memory reservations, can return inconsistent answers. Adding a Kubernetes Service does not remove the race. The system still needs a shared, durable concurrency strategy.

### 💬 Team questions

- What's the difference between liveness and readiness?
- Why can a container start before a database is ready?
- How does a rolling update affect in-flight requests?
- What do we gain with Kubernetes that Compose alone doesn't provide?

### 📎 Learn more

[Docker Overview](https://docs.docker.com/get-started/docker-overview/) · [Kubernetes Concepts](https://kubernetes.io/docs/concepts/) · [kind](https://kind.sigs.k8s.io/)