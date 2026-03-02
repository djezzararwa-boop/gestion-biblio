# 📚 GestionBIBLIO

<h3 align="left"><b>Gestion</b><font weight="300">BIBLIO</font></h3>

**GestionBIBLIO** est une application web moderne, légère et intuitive développée avec **Spring Boot 3**.  
Elle permet de gérer efficacement le cycle de vie des emprunts de livres, tout en appliquant automatiquement les règles internes d’une bibliothèque.

---

## 🎯 Objectif

Faciliter la gestion des prêts et retours de livres tout en garantissant :

- Une rotation équitable des ouvrages  
- Un respect strict des quotas  
- Une expérience utilisateur fluide et minimaliste  

---

## ✨ Fonctionnalités

- 📖 **Gestion dynamique des prêts**  
  Visualisation complète des emprunts avec indicateurs visuels clairs (`EN_COURS`, `RETARD`, `RETOURNE`).

- 🔄 **Gestion simplifiée des retours**  
  Archivage des prêts en un clic grâce au bouton **"Rendre"**.

- ⚡ **Statuts automatiques**  
  Calcul en temps réel des états selon la date prévue de retour.

- 🎨 **Design minimaliste & professionnel**  
  Interface responsive conçue avec **Bootstrap 5**.

---

## ⚖️ Règles de Gestion (Logique Métier)

> 💡 *Parce qu'une bibliothèque sans règles, c'est juste une pile de papier gratuite…*

### 📌 1. Quota d’emprunt
Un étudiant ne peut pas emprunter plus de **3 livres simultanément**.  
➡️ Toute nouvelle tentative est bloquée si le quota est atteint.

### ⛔ 2. Blocage en cas de retard
Si un étudiant possède un livre en **retard**,  
➡️ ses droits d’emprunt sont suspendus jusqu’à régularisation.

### 📦 3. Disponibilité des exemplaires
Un livre emprunté devient automatiquement **indisponible** jusqu’à son retour et archivage.

---

## 🛠️ Stack Technique

| Couche | Technologies |
|--------|--------------|
| Backend | Java 17+, Spring Boot 3, Spring Data JPA |
| Frontend | HTML5, Thymeleaf, Bootstrap 5 |
| Base de données | MySQL (`gestionbib`) |
| ORM | Hibernate |
| Build Tool | Maven |
| Icônes | Bootstrap Icons |

---

## 🚀 Installation & Lancement

### 1️⃣ Prérequis

- Java 17 ou supérieur  
- Maven installé  
- Serveur MySQL (XAMPP, WAMP ou MySQL Server)  

---

### 2️⃣ Création de la base de données

```sql
CREATE DATABASE gestionbib;
```

---

### 3️⃣ Cloner le projet

```bash
git clone https://github.com/djezzararwa-boop/gestion-biblio.git
cd gestion-biblio
```

---

### 4️⃣ Lancer l’application

```bash
mvn spring-boot:run
```

---

### 5️⃣ Accéder à l’interface

Ouvrez votre navigateur :

👉 http://localhost:8080

---
### 🔐 Accès par défaut (Admin)
Pour accéder à l'interface de gestion, utilisez les identifiants suivants :

Identifiant : admin

Mot de passe : 1234
## ⚙️ Configuration (application.properties)

```properties
server.port=8080

spring.datasource.url=jdbc:mysql://localhost:3306/gestionbib
spring.datasource.username=root
spring.datasource.password=

spring.jpa.hibernate.ddl-auto=create
```

---

## 📌 Remarques

- `ddl-auto=create` recrée les tables à chaque démarrage (mode développement).
- Pour la production, utiliser `update` ou `validate`.

---

## 👨‍💻 Auteur

Développé avec passion par **djezzararwa-boop** ✨
