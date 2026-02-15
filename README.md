# 📊 Infrastructure de supervision centralisée sous AWS avec Zabbix
<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/d2141ed4-fa7f-4edc-9928-e8e2a676bdf5" />


## 👨‍🎓 Informations

- **Étudiant** : Diallo Mohamed Ibrahim  
- **Encadrant** : Prof. Azeddine KHIAT  
- **Filière** : 4ème année Cybersécurité  
- **Année universitaire** : 2025/2026  

---

## 🎯 Objectif du projet

Ce projet vise à mettre en œuvre une solution de supervision centralisée basée sur **Zabbix conteneurisé**, déployée sur **AWS**, afin de surveiller un parc hybride composé de :

- Machines Linux  
- Machines Windows  

L’utilisation de Docker permet une meilleure portabilité, isolation et facilité de déploiement.

---

## 🏗️ Architecture

- VPC dédié : `10.0.0.0/16`
- Subnet : `10.0.0.0/24`
- Internet Gateway configurée
- Security Groups séparés (serveur / agents)
- 3 instances EC2 :
  - Serveur Zabbix (Ubuntu 22.04)
  - Client Linux
  - Client Windows Server 2022

---

## 🐳 Déploiement Zabbix (Docker)

Services déployés :

- MySQL
- Zabbix Server
- Zabbix Web (Nginx)

Lancement :

```bash
docker-compose up -d
