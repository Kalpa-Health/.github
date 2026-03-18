# Kalpa Health

**Healthcare infrastructure for Southeast Asia — built in Go, designed for the clinic floor.**

We build [WellMed](https://kalpahealth.com), a microservices platform for multi-location clinic networks. Our focus is the operational layer that most healthcare SaaS ignores: payer rules, crew care, managed care contracts, and the compliance surface area that comes with SATU SEHAT and Indonesian Ministry of Health reporting.

---

## What we're building

**WellMed** is a clinic management backbone designed for groups running 2–20 locations. It handles:

- Multi-clinic patient records with strict data isolation
- Service catalog + payer-aware item pricing
- Consultation workflows with async inter-service communication
- BPJS and SATU SEHAT compliance hooks (KFA, SNOMED, ICD-10)
- Managed care / crew care plan administration

The platform is live and in production across Padma Medical Group's clinic network in Bali and Surabaya.

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

## Engineering culture

- **Document decisions, not just code.** We use ADRs for anything architectural. If it's worth arguing about, it's worth writing down.
- **Async by default.** Services communicate via RabbitMQ. Synchronous gRPC is explicit and justified.
- **Conservative automation.** Human review gates on `main`. Automated pipelines on `develop` and `staging`.
- **Compliance as a first-class concern.** SATU SEHAT, BPJS, and DJP requirements are requirements, not afterthoughts.

---

## We're based in Bali, Indonesia

Kalpa is a small team building serious infrastructure for a market that global vendors underserve. We work in the GMT+8 timezone across a distributed setup.

If you're a Go developer who cares about healthcare systems in Southeast Asia, reach us at **[hello@kalpahealth.com](mailto:hello@kalpahealth.com)**.

---

![GitHub Org Stats](https://github-readme-stats.vercel.app/api?username=kalpa-health&show_icons=true&theme=default&hide_border=true&include_all_commits=true)
