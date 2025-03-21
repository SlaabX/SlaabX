# 🌟 SLAABX - Plateforme de Gestion de Cartes de Collection

SLAABX est une plateforme innovante permettant aux collectionneurs de cartes (**Pokémon, Yu-Gi-Oh!**, etc.) de gérer, estimer et analyser la valeur de leurs cartes en temps réel. 📈

---

## ✨ Fonctionnalités principales

- 🃏 **Gestionnaire de cartes** : Ajoutez vos cartes à votre collection avec des informations détaillées.
- 📊 **Graphiques d'évolution** : Visualisez l'évolution des prix de vos cartes.
- 🌙 **Mode sombre** : Interface adaptée pour une meilleure expérience utilisateur.
- ⭐ **Système de gradation** : Les utilisateurs peuvent évaluer l'état des cartes entre eux.
- 🔒 **Authentification sécurisée** : Connexion et gestion des utilisateurs avec **JWT**.
- 🛒 **Vente et achat de cartes** : Achetez et vendez vos cartes en toute sécurité via la plateforme.
- 🚚 **Système de livraison** : Expédition des cartes dans toute l'Europe via des **API partenaires** *(possibilité d'ajouter le Japon)*.

---

## 🛠 Technologies utilisées

- **Frontend** : [Next.js](https://nextjs.org/), [DaisyUI](https://daisyui.com/) pour une interface moderne et réactive.
- **Backend** : [Spring Boot](https://spring.io/projects/spring-boot) pour la gestion des API et services.
- **Base de données** : [PostgreSQL](https://www.postgresql.org/) pour le stockage des données.
- **Gestion de version** : [GitHub](https://github.com/) pour l'hébergement du code et la gestion du versioning.
- **Conteneurisation** : [Docker](https://www.docker.com/) pour la gestion des environnements.

---

## 📂 Structure du projet

```bash
slaabx/
├── 📂 frontend/        # Code source du frontend (Next.js)
├── 📂 backend/         # Code source du backend (Spring Boot)
├── 🗄️ database/        # Scripts SQL et configurations PostgreSQL
├── 🛠️ docker-compose.yml  # Configuration Docker
├── 📚 README.md        # Documentation du projet
```

---

## 🚀 Installation

### 👋 Prérequis

Avant de commencer, assurez-vous d'avoir installé :

- [Node.js](https://nodejs.org/) (version recommandée : **18.x** ou supérieure)
- [Java JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) (version recommandée : **17**)
- [Docker](https://www.docker.com/) et [Docker Compose](https://docs.docker.com/compose/)
- [Git](https://git-scm.com/)

### 📂 Cloner le projet

```bash
git clone https://github.com/votre-repo/slaabx.git
cd slaabx
```

### ⚙️ Configuration de l'environnement

Créez un fichier `.env` à la racine du projet et ajoutez les variables suivantes :

```env
# Base de données PostgreSQL
SPRING_DATASOURCE_URL=jdbc:postgresql://localhost:5432/slaabx
SPRING_DATASOURCE_USERNAME=your_username
SPRING_DATASOURCE_PASSWORD=your_password

# Configuration du backend
SERVER_PORT=8080
JWT_SECRET=your_secret_key
```

---

## 🐳 Configuration de Docker

### 🛠️ Construire les conteneurs

```bash
docker compose build
```

### ▶️ Démarrer les services

```bash
docker compose up
```

### 🌍 Accéder aux services

- **Frontend (Next.js)** : [http://localhost:3000](http://localhost:3000)
- **Backend (Spring Boot)** : [http://localhost:8080](http://localhost:8080)
- **Base de données (PostgreSQL)** : Accessible sur `localhost:5432`

---

## 🌱 Gestion des branches (**GitFlow**)

### 📌 Branches principales
- **`main`** → Contient le code **stable** et **prêt pour la production**.
- **`develop`** → Contient le code en **cours de développement**.

### 🌿 Branches de travail
- **`feature/*`** → Développement d'une **nouvelle fonctionnalité**.
- **`hotfix/*`** → Correction d'un **bug critique en production**.
- **`release/*`** → Préparation d'une **nouvelle version stable**.
- **`bugfix/*`** → Correction d'un **bug non critique**.

### 🚀 Workflow Git standard

1. **Créer une feature**  
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/nom-de-la-feature
   ```

2. **Pousser la feature sur le dépôt distant**  
   ```bash
   git add .
   git commit -m "Ajout de la fonctionnalité X"
   git push origin feature/nom-de-la-feature
   ```

3. **Fusionner la feature dans `develop`**  
   ```bash
   git checkout develop
   git pull origin develop
   git merge feature/nom-de-la-feature
   git push origin develop
   ```

4. **Supprimer la branche après fusion**  
   ```bash
   git branch -d feature/nom-de-la-feature
   git push origin --delete feature/nom-de-la-feature
   ```

---

## 💎 Versioning

Nous utilisons un système de versionnement en quatre niveaux :

- **V1.2.3.4**
  - 🚀 **1** : Version majeure apportant de gros changements.
  - 🔥 **2** : Mise à jour critique.
  - ✨ **3** : Ajout de nouvelles fonctionnalités.
  - 🐛 **4** : Corrections de bugs.

---

## 🤝 Contribution

Les contributions sont **les bienvenues** !

1. 🍔 Forkez le projet
2. 🌱 Créez une branche : `git checkout -b feature/nouvelle-fonctionnalite`
3. 💾 Faites vos modifications et committez : `git commit -m "Ajout d'une nouvelle fonctionnalité"`
4. 🚀 Poussez la branche : `git push origin feature/nouvelle-fonctionnalite`
5. 🔄 Ouvrez une **Pull Request**

---

## 📚 License

Ce projet est sous licence **MIT** - voir le fichier [LICENSE](LICENSE) pour plus de détails.

🌟 **SLAABX** évolue constamment, alors restez à l'affût des mises à jour ! 🚀
