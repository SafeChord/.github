# 🎼 SafeChord

> A live, solo-built cloud-native platform spanning Japan and Taiwan — run end-to-end for ~NT$800/month.

SafeChord is a hybrid-cloud data platform designed, built, and operated by one engineer, with production-grade discipline under tight resource constraints. It runs an event-driven pipeline on a multi-region K3s cluster, delivered via GitOps, and is documented in the open as a browsable knowledge base.

### 👉 Start here — [**Architecture & Knowledge Base**](https://safechord.github.io/Docs)
The full system map, design decisions (ADRs), and how the four layers fit together — the best way to understand what's here.

## The four layers

| Repo | Layer | What it is |
| :-- | :-- | :-- |
| [**Docs**](https://github.com/SafeChord/Docs) | ⬜ Knowledge | Single source of truth — architecture, ADRs, KDD knowledge tree |
| [**SafeZone**](https://github.com/SafeChord/SafeZone) | 🟦 Application | Event-driven data pipeline — Python/FastAPI + Go, Kafka, PostgreSQL |
| [**SafeZone-Deploy**](https://github.com/SafeChorvery | Helm charts + GitOps (ArgoCD) delivery config|
| [**Chorde**](https://github.com/SafeChord/Chorde)ybrid K3s platform — Tailscale mesh, multi-regionJP/TW |

## Under the hood
- **Hybrid K3s** across a JP cloud VPS, a TW edge nwired over a **Tailscale** mesh
- **Event-driven pipeline**: Kafka + Go/Python microservices, **KEDA** autoscaling on consumer lag
- **GitOps** delivery (ArgoCD); **zero-trust** ingrplanes)
- **Observability** with Prometheus / Loki / Grafana
- Live and self-running today, fully documented as D**)

---
Built & operated by **Brady Hau (陳建豪)** · [LinkedIn](https://www.linkedin.com/in/rebodutchman/) · [Knowledge Base](https://safechord.github.io/Docs)
