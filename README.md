# 📚 GestionBIBLIO

Système de gestion de bibliothèque moderne conçu avec **Spring Boot 3** et **Thymeleaf**.

## ⚖️ Règles de Gestion (Logique Métier)
Pour assurer une gestion fluide, l'application applique les contrôles suivants :

* **Quota d'emprunt :** Un étudiant est limité à un maximum de **3 livres simultanés**. Le système bloque automatiquement toute tentative de prêt supplémentaire.
* **Blocage des Retards :** Tout étudiant ayant un livre non rendu après la date prévue (statut `RETARD`) est suspendu de nouveaux emprunts jusqu'à régularisation.
* **Gestion des Statuts :** Calcul dynamique et visuel des états (`EN_COURS`, `RETARD`, `RETOURNE`).

## 🛠️ Stack Technique
* **Backend :** Java / Spring Boot
* **Frontend :** HTML5 / Bootstrap 5 (Design épuré)
* **Template Engine :** Thymeleaf
