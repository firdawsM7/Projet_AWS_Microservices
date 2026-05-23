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

<!-- Upload cette image dans une Issue GitHub et remplace l'URL -->
![Architecture AWS](REMPLACE_PAR_URL_ARCHITECTURE)

*Vue complète des services AWS interconnectés — VPC, ECS Fargate, ALB, ECR, RDS, CodePipeline*

---

## 📸 Aperçu de l'application

### Application Monolithique (État initial)
<!-- Upload les screenshots dans une Issue GitHub et remplace les URLs -->
![Monolithic App](REMPLACE_PAR_URL_MONOLITH)

### Microservices déployés
![Customer Microservice port 8080](REMPLACE_PAR_URL_CUSTOMER)
![Employee Microservice port 8081](REMPLACE_PAR_URL_EMPLOYEE)

---

## 🔄 Pipeline CI/CD — Blue/Green

![CodePipeline](REMPLACE_PAR_URL_PIPELINE)

*Source → Build → Deploy Blue/Green — 0 downtime garanti*

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
| ECS Fargate (2 services, 2vCPU, 4GB) | Orchestration conteneurs | $58.40 |
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
│                                                      │
│  ┌──────────────────────────────────────────────┐   │
│  │         Application Load Balancer             │   │
│  │              microservicesLB                  │   │
│  └────────────┬─────────────────┬───────────────┘   │
│               │                 │                    │
│        /admin/*           /* (default)               │
│               ↓                 ↓                    │
│  ┌────────────────┐   ┌────────────────┐            │
│  │    Employee     │   │    Customer    │            │
│  │  Microservice  │   │  Microservice  │            │
│  │   port 8081    │   │   port 8080    │            │
│  └────────────────┘   └────────────────┘            │
│               ↓                 ↓                    │
│  ┌──────────────────────────────────────────────┐   │
│  │              RDS MySQL (db.t3.micro)          │   │
│  └──────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────┘
```

---

## 🚀 Déploiement Blue/Green

| Target Group | Port | Rôle |
|-------------|------|------|
| customer-tg-one | 8080 | Blue Environment |
| customer-tg-two | 8080 | Green Environment |
| employee-tg-one | 8080 | Blue Environment |
| employee-tg-two | 8080 | Green Environment |

**Processus de déploiement :**
1. 🔵 Déploiement sur l'environnement **Green** (nouveau)
2. ✅ Tests de validation automatiques
3. 🔄 Transfert de **100% du trafic** vers Green
4. 🗑️ Suppression de l'ancien environnement **Blue**

---

## 📦 Structure du projet

```
microservices/
├── customer/               # Microservice clients (port 8080)
│   ├── app/
│   ├── views/
│   ├── index.js
│   ├── Dockerfile
│   └── package.json
├── employee/               # Microservice employés (port 8081)
│   ├── app/
│   ├── views/
│   ├── index.js
│   ├── Dockerfile
│   └── package.json
└── README.md
```

---

## 🔒 Sécurité

- **IAM** : Rôles et permissions minimales (principe du moindre privilège)
- **Security Groups** : Accès restreint par IP source (`/admin/*`)
- **VPC** : Réseau isolé avec sous-réseaux publics/privés
- **ECR** : Registry privé pour les images Docker
- **Healthcheck** : Vérification automatique de santé des conteneurs

---

## 📊 Monitoring

- **CloudWatch** : Logs centralisés + métriques temps réel
- **ECS Health Checks** : Surveillance automatique des tâches
- **ALB Access Logs** : Journalisation de tout le trafic entrant

---

## 👤 Auteur

**Firdaws Masrour** — 3IACN2/Groupe2  
Encadrant : Marwa Boumaiz | Amazon Web Services — Projet Académique Certifié  
📅 28 décembre 2025

---

## 📄 Rapport technique

[![PDF](https://img.shields.io/badge/Rapport-PDF-red?logo=adobeacrobatreader)](./rapport_projet_DevOps_Firdaws_Masrour_3IACN2_2025.pdf)
