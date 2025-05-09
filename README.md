# GamingVerse Hub Projekt - Sprint Terv

Ez a dokumentum összefoglalja a GamingVerse Hub hobby projekt sprintjeit és feladatait.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/) 

## Clone the Repository

Open your terminal or command prompt and run:

```bash
git clone https://github.com/me-and-the-boys-hu/GamingVerseHub.git
```

## Tartalom
- [Sprint 0: Fejlesztői környezet beállítása](#sprint-0-fejlesztői-környezet-beállítása)
- [Sprint 1: Autentikáció és alapprofil](#sprint-1-autentikáció-és-alapprofil)
- [Sprint 2: Posztolási rendszer és moderáció](#sprint-2-posztolási-rendszer-és-moderáció)
- [Sprint 3: Lootbox rendszer és inventory](#sprint-3-lootbox-rendszer-és-inventory)
- [Sprint 4: Piactér és webhook integráció](#sprint-4-piactér-és-webhook-integráció)
- [Sprint 5: CI/CD és tárhely](#sprint-5-cicd-és-tárhely)
- [Sprint 6: Kubernetes és infra](#sprint-6-kubernetes-és-infra)

---

## Sprint 0: Fejlesztői környezet beállítása
- Projekt scaffold létrehozása: Spring Boot backend, React frontend
- Docker Compose konfiguráció: backend, frontend, PostgreSQL szolgáltatások
- Git repository inicializálás és alap .gitignore
- Fejlesztési környezet dokumentáció: README részlet a futtatásról

## Sprint 1: Autentikáció és alapprofil
- OAuth2 integráció **Google** providerrel
- JWT alapú saját regisztráció és login endpoint
- Felhasználói entitás és szerepek definiálása (user, moderator, admin)
- Profiloldal backend API (Spring Boot) és React komponens
- Egység- és integrációs tesztek bevezetése autentikációhoz és profilhoz
- Swagger UI konfiguráció és dokumentáció

## Sprint 2: Posztolási rendszer és moderáció
- Backend fájlfeltöltés lokális `/uploads` mappába
- React fájlfeltöltő komponens képek/videók feltöltéséhez
- Poszt létrehozása API és React űrlap (először csak szöveg, majd médiával)
- Feed endpoint implementálása lapozással (pagináció)
- Feed komponens React-ben a paginált lista megjelenítéséhez
- Komment API és React komponens hozzászólásokhoz
- Like API és gomb a posztoknál
- Share gomb (URL másolás) implementálása
- Moderációs API és admin felület posztok szűréséhez, jóváhagyáshoz

## Sprint 3: Lootbox rendszer és inventory
- Headless "loot-open" API az odds generálására TDD-vel
- Loot entitás, rarity modell (common, rare, epic, legendary)
- Inventory backend modell és API a felhasználói gyűjteményhez
- Admin CRUD API lootok kezelésére
- Inventory React oldal a gyűjtemény megjelenítéséhez
- React lootbox nyitó animáció komponens csomagolva a logikára
- Konfigurációs fájl (JSON/YAML) a loot definiálásához

## Sprint 4: Piactér és webhook integráció
- Gift (ajándékozás) entitás és API
- Piactér React komponens ajánlatok listázásához és elfogadásához
- Felhasználói trade beállítások API és UI
- Üzenetsorozat (pl. Redis Streams) bevezetése webhook queue-hoz
- Discord webhook kliens Spring Boot-ban konfigurálva
- Webhook események: legendary loot, új poszt, top comment

## Sprint 5: CI/CD és tárhely
- GitHub Actions pipeline beállítása backend és frontend build/test-re
- Dockerfile-ek megírása backend és frontend image-ekhez
- MinIO integráció Spring Boot klienssel és React fájlfeltöltéssel
- Redis cache konfiguráció a leaderboard gyorsításhoz
- Pipeline staging deploy lépés bevezetése dev környezetbe

## Sprint 6: Kubernetes és infra
- Helm chart készítése dev és prod namespace-ekre
- Kubernetes Deployment manifestek a szolgáltatásokhoz
- Ingress konfiguráció HTTPS-sel, cert-manager + Let's Encrypt
- Prometheus integráció Spring Boot actuator metrikákkal
- Grafana dashboard alap beállítások (CPU/memory, custom metrikák)
- Loggyűjtés konfiguráció Loki vagy Elasticsearch használatával

---

> **Jegyzet:** A sprintfeladatok fokozatosan épülnek egymásra, és az MVP-t célozzák meg először (Sprint 0–3), majd a skálázást és üzemeltetést (Sprint 4–6). A projekt során iteratívan fejlesszük és teszteljük a funkciókat, valamint a CI/CD és infra elemeket is fokozatosan építsük be.


---


# GamingVerse Hub Project - Sprint Plan

This document outlines the sprints and tasks for the GamingVerse Hub hobby project.

## Table of Contents
- [Sprint 0: Developer Environment Setup](#sprint-0-developer-environment-setup)
- [Sprint 1: Authentication & Basic Profile](#sprint-1-authentication--basic-profile)
- [Sprint 2: Posting System & Moderation](#sprint-2-posting-system--moderation)
- [Sprint 3: Lootbox System & Inventory](#sprint-3-lootbox-system--inventory)
- [Sprint 4: Marketplace & Webhook Integration](#sprint-4-marketplace--webhook-integration)
- [Sprint 5: CI/CD & Storage](#sprint-5-cicd--storage)
- [Sprint 6: Kubernetes & Infrastructure](#sprint-6-kubernetes--infrastructure)

---

## Sprint 0: Developer Environment Setup
- **Scaffold Project:** Initialize Spring Boot backend and React frontend.
- **Docker Compose Configuration:** Services for backend, frontend, and PostgreSQL.
- **Git Repository Setup:** Initialize repo, add `.gitignore`.
- **Dev Environment Docs:** Instructions in README for running locally.

## Sprint 1: Authentication & Basic Profile
- **OAuth2 Integration:** Google provider setup
- **JWT Registration & Login:** Custom registration and authentication endpoints
- **User Entity & Roles:** Define roles (user, moderator, admin)
- **Profile API & UI:** Backend endpoints and React component for user profiles
- **Unit & Integration Tests:** For authentication flows and profile API
- **Swagger UI:** Configure API documentation

## Sprint 2: Posting System & Moderation
- **File Upload Backend:** Store uploads in local `/uploads` directory
- **React Upload Component:** For images and videos
- **Create Post API & Form:** Start with text-only, then add media
- **Feed Endpoint:** Implement pagination
- **Feed Component:** Display paginated posts in React
- **Comment API & UI:** Backend and React component for comments
- **Like API & Button:** Implement liking posts
- **Share Button:** Copy post URL functionality
- **Admin Moderation:** API and admin UI to review and approve posts

## Sprint 3: Lootbox System & Inventory
- **Headless Loot API:** TDD for odds generation logic
- **Loot Entity & Rarity:** Models for common, rare, epic, legendary
- **Inventory Backend:** Model and API for user collections
- **Admin Loot CRUD:** Backend endpoints for managing loot items
- **Inventory UI:** React page to display user inventory
- **Lootbox Animation:** React component for opening lootboxes
- **Config File:** JSON/YAML for loot definitions and drop rates

## Sprint 4: Marketplace & Webhook Integration
- **Gift Entity & API:** Basic gifting workflow
- **Marketplace UI:** React component for listing and accepting gifts
- **Trade Settings:** User preferences API and UI
- **Webhook Queue:** Implement message queue (e.g., Redis Streams)
- **Discord Webhook Client:** Spring Boot integration
- **Events to Webhook:** legendary loot, new post, top comment notifications

## Sprint 5: CI/CD & Storage
- **GitHub Actions:** Pipelines for backend and frontend build/test
- **Dockerfiles:** Create images for backend and frontend
- **MinIO Integration:** Spring Boot client and React upload adaptation
- **Redis Cache:** Configure for leaderboard performance
- **Staging Deploy:** Add pipeline step for deploying to dev environment

## Sprint 6: Kubernetes & Infrastructure
- **Helm Charts:** Create for dev and prod namespaces
- **Kubernetes Manifests:** Deployment resources for services
- **Ingress & TLS:** Setup HTTPS using cert-manager and Let's Encrypt
- **Prometheus Monitoring:** Integrate Spring Boot Actuator metrics
- **Grafana Dashboards:** Basic CPU/memory and custom metrics
- **Log Aggregation:** Configure Loki or Elasticsearch for logs

---

> **Note:** These sprints build progressively, targeting MVP features first (Sprints 0–3) and moving towards scalability and operations (Sprints 4–6). Develop and test iteratively, integrating CI/CD and infra components along the way.

