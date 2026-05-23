# ☁️ Projet AWS — Architecture Microservices

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws)
![Docker](https://img.shields.io/badge/Docker-Containerisation-blue?logo=docker)
![Node.js](https://img.shields.io/badge/Node.js-16--alpine-green?logo=nodedotjs)
![MySQL](https://img.shields.io/badge/RDS-MySQL-blue?logo=mysql)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Status](https://img.shields.io/badge/Projet-Achevé%20✅-brightgreen)

> Migration complète d'une application monolithique **Coffee Suppliers** vers une **architecture microservices AWS** — déploiement Blue/Green automatisé, pipeline CI/CD, et infrastructure hautement disponible.

---

## 🏆 Résultats

| Métrique | Résultat |
|----------|----------|
| ✅ Taux de succès déploiement | **100%** |
| 🟢 Disponibilité application | **99.9%+** |
| ⚡ Temps de déploiement | **7 minutes** |
| 💰 Coût mensuel optimisé | **$131.28/mois** |
| 🔧 Services AWS intégrés | **12 services** |

---

## 🏗️ Architecture AWS

![Architecture AWS](https://github.com/user-attachments/assets/17238d87-ad7b-45f5-8a29-058e03d82797)

*Vue complète des services AWS interconnectés — VPC, ECS Fargate, ALB, ECR, RDS, CodePipeline*

---

## 💰 Estimation des Coûts & Application Monolithique

![Coûts et Monolith](https://github.com/user-attachments/assets/1dc60f84-ec54-4a97-b0f4-f083242bcd21)

*Analyse détaillée des coûts ($131.28/mois) + état initial de l'application monolithique*

---

## 🐳 Microservices & Conteneurisation Docker

![Docker Microservices](https://github.com/user-attachments/assets/4ba1f292-29d0-440e-a542-cf3475190e77)

*Dockerfile optimisé + Microservice Customer (port 8080) + Microservice Employee (port 8081)*

---

## 🔄 Pipeline CI/CD — Blue/Green Deployment

![Pipeline CI/CD](https://github.com/user-attachments/assets/591227c6-0b0f-4b45-97af-2d9e767a8989)

*CodePipeline → CodeDeploy → ECS Fargate — déploiement Blue/Green sans downtime*

---

## 🏆 Accomplissements — Projet Achevé

![Résultats](https://github.com/user-attachments/assets/b418827d-38be-4617-902a-c53495b5a3c3)

*100% succès · 99.9%+ disponibilité · 7 min déploiement · 12 services AWS*

---

## 📋 Phases du Projet

```
Phase 1 — Architecture & Estimation des coûts
      ↓
Phase 2 — Analyse de l'application monolithique (EC2 + RDS MySQL)
      ↓
Phase 3 — Environnement de développement AWS Cloud9
      ↓
Phase 4 — Microservices & Conteneurisation Docker
      ↓
Phase 5 — Infrastructure Cloud AWS (ECR + ECS Fargate)
      ↓
Phase 6 — Load Balancing & Réseau (ALB + Target Groups)
      ↓
Phase 7 — Orchestration Amazon ECS
      ↓
Phase 8 — Pipeline CI/CD (CodeCommit + CodePipeline + CodeDeploy)
      ↓
Phase 9 — Optimisation & Sécurité (IAM + Security Groups)
```

---

## 🔧 Services AWS utilisés

| Service | Rôle | Coût/mois |
|---------|------|-----------|
| EC2 Cloud9 (t3.small) | IDE développement | $29.20 |
| ECS Fargate (2vCPU, 4GB) | Orchestration conteneurs | $58.40 |
| Application Load Balancer | Distribution du trafic | $22.00 |
| RDS MySQL (db.t3.micro) | Base de données | $15.68 |
| CodeCommit | Repositories Git | $1.00 |
| CodePipeline | Pipeline CI/CD | $2.00 |
| CodeDeploy | Déploiement Blue/Green | $2.00 |
| ECR | Registry images Docker | $1.00 |
| CloudWatch | Monitoring & logs | $0.50 |
| IAM | Gestion des accès | $0.50 |
| **Total mensuel** | | **$131.28** |

---

## 🐳 Architecture des Microservices

```
┌─────────────────────────────────────────────────────┐
│                    AWS Cloud VPC                     │
│  ┌──────────────────────────────────────────────┐   │
│  │         Application Load Balancer             │   │
│  └────────────┬─────────────────┬───────────────┘   │
│         /admin/*           /* (default)              │
│               ↓                 ↓                    │
│  ┌────────────────┐   ┌────────────────┐            │
│  │    Employee     │   │    Customer    │            │
│  │   port 8081    │   │   port 8080    │            │
│  └────────────────┘   └────────────────┘            │
│  ┌──────────────────────────────────────────────┐   │
│  │              RDS MySQL (db.t3.micro)          │   │
│  └──────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────┘
```

---

## 🔒 Sécurité

- **IAM** : Rôles et permissions minimales
- **Security Groups** : Accès restreint par IP source
- **VPC** : Réseau isolé avec sous-réseaux publics/privés
- **ECR** : Registry privé pour les images Docker
- **Healthcheck** : Vérification automatique des conteneurs

---

## 👤 Auteur

**Firdaws Masrour** — 3IACN2/Groupe2
Encadrant : Marwa Boumaiz | Amazon Web Services — Projet Académique Certifié
📅 28 décembre 2025

---

## 📄 Rapport technique

[![PDF](https://img.shields.io/badge/Rapport-PDF-red?logo=adobeacrobatreader)](./rapport_projet_DevOps_Firdaws_Masrour_3IACN2_2025.pdf)
