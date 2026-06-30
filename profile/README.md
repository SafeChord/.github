# 🎼 SafeChord

> A live, solo-built cloud-native platform spanning Japan and Taiwan — run end-to-end for ~NT$800/month.

SafeChord is a hybrid-cloud data platform designed, built, and operated by one engineer, with production-grade discipline under tight resource constraints. It runs an event-driven pipeline on a multi-region K3s cluster, delivered via GitOps, and is documented in the open as a browsable knowledge base.

### 👉 Start here — [**Architecture & Knowledge Base**](https://safechord.github.io/Docs)
The full system map, design decisions (ADRs), and how the four layers fit together — the best way to understand what's here.

## The four layers

| Repo | Layer | What it is |
| :-- | :-- | :-- |
| [**Docs**](https://github.com/SafeChord/Docs) | ⬜ Knowledge | Single source of truth — architecture, ADRs, KDD knowledge tree |
| [**SafeZone**](https://github.com/SafeChord/SafeZone) | 🟦 Application | Event-driven data pipeline — Python/FastAPI + Go, Kafka, PostgreSQL|
| [**SafeZone-Deploy**](https://github.com/SafeChord/SafeZone-Deploy) | 🟨 Delivery | Helm charts + GitOps (ArgoCD) delivery config |
| [**Chorde**](https://github.com/SafeChord/Chorde)| 🟥 Infrastructure | The hybrid K3s platform — Tailscale mesh, multi-region JP/TW |

## Under the hood
- **Hybrid K3s** across a JP cloud VPS, a TW edge node, and home-lab hardware, wired over a **Tailscale** mesh
- **Event-driven pipeline**: Kafka + Go/Python microservices, **KEDA** autoscaling on consumer lag
- **GitOps** delivery (ArgoCD); **zero-trust** ingress (split public / private planes)
- **Observability** with Prometheus / Loki / Grafana
- Live and self-running today, fully documented as an open knowledge base (**KDD**)

---
Built & operated by **Brady Hau (陳建豪)** · [LinkedIn](https://www.linkedin.com/in/rebodutchman/) · [Knowledge Base](https://safechord.github.io/Docs)
