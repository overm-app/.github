# overm-app

A deliberately overengineered microservices system built to learn distributed systems end to end — not because a recipe app needs Kafka, but because the patterns should be familiar before they matter for real.

**Author:** Mario Irigoyen — [@Tar-Mairon24](https://github.com/Tar-Mairon24)  
**Stack:** Go · Python · Angular · Kubernetes · Kafka · MongoDB · PostgreSQL · AWS EKS · Terraform  
**Status:** Active development — Phase 1

---

## What is it

A recipe and weekly menu planning app. You add recipes, it calculates macros, generates a meal plan for the week. You can also upload a photo of a handwritten recipe and it transcribes it automatically.

The app is simple on purpose. The architecture is not.

---

## Why it exists

Polyrepo microservices. Event-driven async flows. Contract-first API design. CI/CD pipelines. Infrastructure as code. Production-grade observability. Everything you would find in a real distributed system at a real company — built from scratch by one person to learn it firsthand before doing it professionally.

---

## Services

| Repository | What it does |
|---|---|
| [api-auth](https://github.com/overm-app/api-auth) | JWT auth, Google OAuth, PostgreSQL |
| [api-recipe-catalog](https://github.com/overm-app/api-recipe-catalog) | Recipe CRUD, image upload trigger |
| [api-menu-shuffle](https://github.com/overm-app/api-menu-shuffle) | Weekly menu generation |
| [api-nutrition](https://github.com/overm-app/api-nutrition) | Macro calculation, USDA API |
| [api-image-processing](https://github.com/overm-app/api-image-processing) | OCR, handwriting transcription |
| [api-notifications](https://github.com/overm-app/api-notifications) | Kafka → Novu notification bridge |
| [web-frontend](https://github.com/overm-app/web-frontend) | Angular app |
| [contracts](https://github.com/overm-app/contracts) | OpenAPI specs + Kafka schemas |
| [IaC](https://github.com/overm-app/IaC) | Terraform — AWS infrastructure |
| [pipelines](https://github.com/overm-app/pipelines) | Reusable GitHub Actions workflows |

---

## Full documentation

Architecture, design decisions, git flow, CI/CD, and roadmap — [overm-app/docs](https://github.com/overm-app/docs)

---

*Built during the final semester of a Computer Systems Engineering degree while working as an SRE intern at Softtek.*
