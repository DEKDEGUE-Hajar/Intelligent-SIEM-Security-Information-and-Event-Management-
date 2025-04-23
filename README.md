# 📡 AI-Based SIEM - Intrusion Detection System

---
## 📖 Project Overview
Détection automatique d’intrusions réseau en temps réel, intégrée dans une architecture SIEM avec déploiement API et pipeline ELK.

---



## 🌟 Features
- Real-time detection and classification of network attacks
- RESTful API for model inference
- Support for multiple attack types
- Dashboard for visual analytics
- Automated incident response integration with Wazuh

---

## 🗃️ Dataset
We use the [CICIDS2017 Dataset](https://www.unb.ca/cic/datasets/ids-2017.html), which includes both benign and attack traffic types such as DDoS, PortScan, Bot, BruteForce, Web Attack, and more.

---

## 📌 Objectif

Développer un système intelligent capable de détecter et classifier les attaques dans un flux réseau en s’appuyant sur des algorithmes d’apprentissage automatique et l'intégration dans un environnement SIEM (ELK Stack).

---

## 🧠 Architecture du système

> ⚠️ Ce dépôt contient uniquement le **modèle de détection** et le **pipeline de prétraitement**.  
> L’infrastructure complète SIEM (déploiement API + intégration ELK) est décrite ci-dessous à titre informatif, mais n’est **pas incluse** dans ce repository.

The system is composed of the following components:

- **Logstash**: Ingests and preprocesses log data
- **Elasticsearch**: Stores and indexes logs for fast querying
- **Kibana**: Visualizes the logs and predictions in real time
- **Flask API**: Exposes the trained ML model for prediction
- **Wazuh**: Acts as the SOAR component for automated response
- **ML Models**: Includes XGBoost, LightGBM, Random Forest, and ensemble techniques

---

![Architecture SIEM](https://github.com/user-attachments/assets/0058aa43-9c06-4597-a92a-3133d876b2eb)

---

## ⚙️ Méthodologie

- **Prétraitement du dataset CIC-IDS2017** : nettoyage, normalisation, réduction dimensionnelle (PCA), sur-échantillonnage (SMOTE), regroupement des classes.
- **Modélisation** : Implémentation de l’algorithme *Triboost* (XGBoost + LightGBM + Random Forest).
- **Optimisation** : Sélection du meilleur modèle pour chaque type d’attaque selon le F1-score.
- **Déploiement (hors repo)** : Exposition du modèle via une API REST développée avec Flask.
- **Intégration (hors repo)** : Ingestion des prédictions dans le pipeline Logstash, stockage dans Elasticsearch, visualisation via Kibana.

---

## 🛠️ Technologies utilisées

- **Langages & Librairies** : Python, Scikit-learn, XGBoost, LightGBM, SMOTE, PCA
- **Backend** : Flask API (non inclus dans ce repo)
- **SIEM Stack** : Logstash, Elasticsearch, Kibana (non inclus dans ce repo)
- **Outils** : Git, Postman

---

## 📊 Résultats

- Détection multi-classes avec un F1-score > 92% sur les attaques principales
- Intégration en temps réel dans une stack ELK pour visualisation et alerting

---

## 📁 Lien GitHub

🔗 [https://github.com/AjarHDK/Network-Intrusion-Detection]([https://github.com/AjarHDK/Network-Intrusion-Detection](https://github.com/DEKDEGUE-Hajar/Intelligent-SIEM-Security-Information-and-Event-Management-))

---
