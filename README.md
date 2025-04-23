
# 📡 SIEM-Based Intrusion Detection System

Détection automatique d’intrusions réseau en temps réel, intégrée dans une architecture SIEM avec déploiement API et pipeline ELK.

---

## 📌 Objectif

Développer un système intelligent capable de détecter et classifier les attaques dans un flux réseau en s’appuyant sur des algorithmes d’apprentissage automatique et l'intégration dans un environnement SIEM (ELK Stack).

---

## 🧠 Architecture du système

![Architecture SIEM](<img width="545" alt="image" src="https://github.com/user-attachments/assets/00ce53ea-0a34-46b9-af8d-a7b8418fdbdc" />
)

---

## ⚙️ Méthodologie

- **Prétraitement du dataset CIC-IDS2017** : nettoyage, normalisation, réduction dimensionnelle (PCA), sur-échantillonnage (SMOTE), regroupement des classes.
- **Modélisation** : Implémentation de l’algorithme *Triboost* (XGBoost + LightGBM + Random Forest).
- **Optimisation** : Sélection du meilleur modèle pour chaque type d’attaque selon le F1-score.
- **Déploiement** : Exposition du modèle via une API REST (Flask).
- **Intégration** : Ingestion des alertes dans le pipeline Logstash, visualisation avec Kibana.

---

## 🛠️ Technologies utilisées

- **Langages & Librairies** : Python, Scikit-learn, XGBoost, LightGBM, SMOTE, PCA
- **Backend** : Flask API
- **SIEM Stack** : Logstash, Elasticsearch, Kibana
- **Outils** : Git, Postman

---

## 📊 Résultats

- Détection multi-classes avec un F1-score > 92% sur les attaques principales
- Intégration en temps réel dans une stack ELK pour visualisation et alerting

---
