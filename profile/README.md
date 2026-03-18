# Kalpa Health

**Clinic OS for Southeast Asia — built by clinicians, powered by Go, AI-native from day one.**

15 years of running clinics and four systems later, we decided to build our own. [WellMed](https://kalpahealth.com) is what happens when people who actually work the clinic floor design the software. It handles multi-location operations, payer logic, managed care, and full SATU SEHAT compliance — not as bolt-on integrations, but as core architecture built on the FHIR global health standard.

The platform is live and in production across clinic networks in Bali and Surabaya.

---

## What WellMed does

WellMed is a Clinic OS for groups running 2–20 locations. It handles:

- Multi-clinic patient records with strict data isolation
- Service catalog with payer-aware pricing (BPJS, private, managed care)
- Consultation workflows with async inter-service communication
- Native SATU SEHAT synchronization (KFA, SNOMED CT, ICD-10, FHIR R4)
- Managed care and crew care plan administration
- AI-assisted clinical workflows — not a feature, part of the foundation

---

## Our values

**Focus, focus, focus.** Say no to almost everything so you can say yes to the right thing.

**We take ownership for our product.** No finger-pointing, no "that's not my service." If it ships, it's ours.

**We are the caretakers of our user's experience.** Every screen, every interaction, every edge case — someone on the clinic floor has to live with it.

**Celebrate everyone's successes.** Wins are shared. Credit flows to the people who did the work.

**Push each other to exceed our own perceived maximum potential.** Comfortable is the enemy of great.

**We learn from the exploration of new knowledge and experience.** Curiosity is a job requirement.

---

## Engineering culture

We're a small team with a scrappy attitude: do the most with the fewest. "Most" means beautiful, intuitive design. Clever, elegant architecture. Performant, resilient systems. User-focused, UX-lite feature development.

- **FHIR-native.** WellMed speaks the global health interoperability standard at its core — SATU SEHAT compliance is a natural output, not a compliance checkbox.
- **AI-native.** Intelligence is woven into the platform, not bolted on after the fact.
- **Async by default.** Services communicate via RabbitMQ. Synchronous gRPC is explicit and justified.
- **Document decisions, not just code.** ADRs for anything architectural. If it's worth arguing about, it's worth writing down.

---

## Tech stack

| Layer | Stack |
|---|---|
| Services | Go (microservices) |
| Messaging | RabbitMQ + gRPC |
| API Gateway | Go (custom) |
| Infrastructure | AWS (EC2, RDS, SSM, ECR) |
| CI/CD | GitHub Actions, Docker |
| Security scanning | Trivy, govulncheck, gitleaks |
| Secrets | AWS SSM Parameter Store |

Architecture decisions are documented in ADRs in [`kalpa-docs`](https://github.com/kalpa-health/kalpa-docs).

---

## Repositories

| Repo | Purpose |
|---|---|
| `wellmed-backbone` | Core domain: patients, encounters, billing orchestration |
| `wellmed-consultation` | Consultation workflow service |
| `wellmed-gateway-go` | API gateway and auth layer |
| `wellmed-infrastructure` | IaC, deployment configs |
| `kalpa-docs` | ADRs, PRDs, architecture docs |

---

## Based in Bandung, Indonesia

Kalpa is a small team building serious infrastructure for a market that global vendors underserve. We work in the GMT+7 timezone.

If you're a Go developer who cares about healthcare systems in Southeast Asia, reach us at **[hello@kalpahealth.com](mailto:hello@kalpahealth.com)**.
