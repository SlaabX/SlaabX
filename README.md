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

# 🌱 Gestion des branches (GitFlow)

Notre projet suit le workflow **GitFlow** pour assurer une gestion propre et efficace du code. Voici comment sont organisées les branches :

## 📌 Branches principales
- **`main`** → Contient le code **stable** et **prêt pour la production**.
- **`develop`** → Contient le code en **cours de développement**. C'est ici que toutes les nouvelles fonctionnalités sont intégrées avant d'être validées pour la production.

## 🌿 Branches de travail
- **`feature/*`** → Utilisée pour développer une **nouvelle fonctionnalité**.
  - 📌 Créée depuis `develop`.
  - ✅ Fusionnée dans `develop` une fois terminée.
  - 🏷️ Exemple : `feature/authentification`

- **`hotfix/*`** → Utilisée pour corriger un **bug critique en production**.
  - 📌 Créée depuis `main`.
  - ✅ Fusionnée dans `main` et `develop` après correction.
  - 🏷️ Exemple : `hotfix/fix-paiement`

- **`release/*`** → Utilisée pour préparer une **nouvelle version stable**.
  - 📌 Créée depuis `develop`.
  - ✅ Fusionnée dans `main` et `develop` après validation.
  - 🏷️ Exemple : `release/v1.0.0`

- **`bugfix/*`** → Utilisée pour corriger un **bug non critique**.
  - 📌 Créée depuis `develop`.
  - ✅ Fusionnée dans `develop` une fois corrigée.
  - 🏷️ Exemple : `bugfix/correction-affichage`

## 🚀 Workflow Git détaillé

### 1️⃣ Ajout d'une nouvelle fonctionnalité (`feature`)
1. **Créer une branche feature**  
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/nom-de-la-feature
   ```
2. **Développer et pousser la feature**  
   ```bash
   git add .
   git commit -m "✨ Ajout de la fonctionnalité X"
   git push origin feature/nom-de-la-feature
   ```
3. **Fusionner dans `develop` (via une PR ou en local)**  
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

### 2️⃣ Mise en production (`release`)
1. **Créer une branche release**  
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b release/vX.Y.Z
   ```
2. **Tester et corriger les bugs éventuels**  
3. **Fusionner dans `main` et `develop`**  
   ```bash
   git checkout main
   git merge release/vX.Y.Z
   git push origin main
   git checkout develop
   git merge release/vX.Y.Z
   git push origin develop
   ```
4. **Taguer la version et supprimer la branche**  
   ```bash
   git tag vX.Y.Z
   git push origin vX.Y.Z
   git branch -d release/vX.Y.Z
   git push origin --delete release/vX.Y.Z
   ```

### 3️⃣ Correction d'un bug critique en production (`hotfix`)
1. **Créer une branche hotfix depuis `main`**  
   ```bash
   git checkout main
   git pull origin main
   git checkout -b hotfix/fix-nom-du-bug
   ```
2. **Corriger et pousser la correction**  
   ```bash
   git add .
   git commit -m "🐛 Correction d'un bug critique"
   git push origin hotfix/fix-nom-du-bug
   ```
3. **Fusionner dans `main` et `develop`**  
   ```bash
   git checkout main
   git merge hotfix/fix-nom-du-bug
   git push origin main
   git checkout develop
   git merge hotfix/fix-nom-du-bug
   git push origin develop
   ```
4. **Supprimer la branche après correction**  
   ```bash
   git branch -d hotfix/fix-nom-du-bug
   git push origin --delete hotfix/fix-nom-du-bug
   ```

### 4️⃣ Correction d'un bug non critique (`bugfix`)
1. **Créer une branche bugfix depuis `develop`**  
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b bugfix/fix-nom-du-bug
   ```
2. **Corriger et pousser la correction**  
   ```bash
   git add .
   git commit -m "🐞 Correction d'un bug mineur"
   git push origin bugfix/fix-nom-du-bug
   ```
3. **Fusionner dans `develop`**  
   ```bash
   git checkout develop
   git merge bugfix/fix-nom-du-bug
   git push origin develop
   ```
4. **Supprimer la branche après correction**  
   ```bash
   git branch -d bugfix/fix-nom-du-bug
   git push origin --delete bugfix/fix-nom-du-bug
   ```

---

💡 **Rappel important :**  
- **Ne jamais travailler directement sur `main` ou `develop` !**  
- Toujours créer des **pull requests** pour fusionner du code.  
- Bien tester les fonctionnalités avant de les intégrer. 

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
