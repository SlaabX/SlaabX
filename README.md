# SlaabX

**SlaabX** est une plateforme de gestion de cartes de collection permettant aux utilisateurs de gérer leur collection, suivre l'évolution des prix et interagir avec d'autres passionnés de cartes. Le projet intègre un système d'authentification pour permettre aux utilisateurs de créer des comptes, gérer leurs profils, et participer à la vente et à l'achat de cartes rares. Le système de notation et d'estimation des cartes est également inclus pour faciliter la prise de décision lors de l'achat ou de la vente.

## Fonctionnalités principales

- **Gestion de collection** : Les utilisateurs peuvent ajouter, modifier et supprimer des cartes dans leur collection personnelle.
- **Estimation des cartes** : Évaluation dynamique de la valeur des cartes en fonction des tendances du marché et de la demande.
- **Suivi des prix** : Visualisation des historiques de prix des cartes à travers des graphiques interactifs.
- **Notation et avis** : Les utilisateurs peuvent donner des notes et laisser des avis sur les cartes pour aider à leur évaluation.
- **Marché d'échange** : Possibilité de vendre, acheter ou échanger des cartes avec d'autres utilisateurs via un système sécurisé.
- **Authentification sécurisée** : Inscription, connexion et gestion de profil avec des technologies de sécurité avancées comme JWT et Spring Boot.
- **Notifications** : Les utilisateurs peuvent recevoir des alertes sur la valeur des cartes de leur collection ou des opportunités de marché.
- **Recherche et filtres** : Recherche rapide de cartes par type, valeur, popularité et autres critères avec des filtres personnalisables.

## Technologies utilisées

- **Frontend** : [Next.js](https://nextjs.org/) pour une interface utilisateur moderne, rapide et réactive, avec le support du rendu côté serveur (SSR).
- **Design UI** : [DaisyUI](https://daisyui.com/) pour des composants pré-construits et une intégration facile avec Tailwind CSS, offrant une interface épurée et fonctionnelle.
- **Backend** : [Spring Boot](https://spring.io/projects/spring-boot) pour construire des APIs robustes et sécurisées, avec des intégrations pour la gestion des utilisateurs et des services.
- **Base de données** : [PostgreSQL](https://www.postgresql.org/) pour une base de données relationnelle puissante, avec une prise en charge des transactions complexes et des performances élevées.
- **Sécurisation** : [Spring Security](https://spring.io/projects/spring-security) pour une gestion sécurisée de l'authentification et de l'autorisation des utilisateurs.
- **Conteneurisation** : [Docker](https://www.docker.com/) pour faciliter le déploiement de l'application dans des environnements isolés et reproductibles.
- **Gestion de version** : [GitHub](https://github.com/) pour l'hébergement du code, la gestion des versions et la collaboration via les Pull Requests et Issues.

## Installation

### Prérequis

Avant de commencer, vous devez vous assurer que les outils suivants sont installés sur votre machine :

- **[Git](https://git-scm.com/)** : Outil de gestion de version pour cloner et gérer le repository.
- **[Docker](https://www.docker.com/get-started)** : Outil de conteneurisation pour exécuter l'application et sa base de données dans des environnements isolés.
- **[Node.js](https://nodejs.org/)** : Environnement d'exécution JavaScript nécessaire pour le frontend (Next.js).
- **[Java JDK 11+](https://adoptopenjdk.net/)** : Nécessaire pour exécuter le backend (Spring Boot).
- **[PostgreSQL](https://www.postgresql.org/)** : Système de gestion de base de données relationnelle utilisé pour stocker les données. Vous pouvez également utiliser Docker pour exécuter PostgreSQL.

### Cloner le repository

Commencez par cloner le repository sur votre machine locale. Ouvrez un terminal et exécutez les commandes suivantes :

```bash
git clone https://github.com/your-username/slaabx.git
cd slaabx

## Installation

1. Clonez le repository :
   ```bash
   git clone https://github.com/ton-utilisateur/slaabx.git
Configurez le backend avec Spring Boot :
bash
Copier
Modifier
cd backend
mvn spring-boot:run
Configurez le frontend avec Next.js :
bash
Copier
Modifier
cd frontend
npm install
npm run dev
Accédez à l'application à l'adresse http://localhost:3000 pour le frontend et au backend via http://localhost:8080.
Versioning
Le versionning du projet suit une approche de versionnement sémantique (SemVer). Cela signifie que chaque version majeure, mineure et de patch est incrémentée en fonction des changements apportés au projet.

Système de versioning
Version majeure : Incrementée pour des changements majeurs qui peuvent introduire des incompatibilités avec les versions précédentes.
Version mineure : Incrementée pour de nouvelles fonctionnalités qui sont rétro-compatibles avec la version précédente.
Version de patch : Incrementée pour des corrections de bugs ou des améliorations mineures, sans nouvelles fonctionnalités.
Exemple de version :
plaintext
Copier
Modifier
1.2.3
1 : Version majeure (changements incompatibles)
2 : Version mineure (ajout de fonctionnalités)
3 : Patch (correction de bug)
Processus de mise à jour
Feature branches : Les nouvelles fonctionnalités sont développées dans des branches séparées avec le préfixe feature/.
Bugfix branches : Les corrections de bugs sont développées dans des branches avec le préfixe bugfix/.
Release branches : Lorsque le projet est prêt pour une nouvelle version, une branche release/ est créée pour les tests finaux avant la publication.
Tagging des versions : Chaque version stable est taguée avec un numéro de version.
Exemple de flux de travail Git :
Créez une nouvelle branche pour une fonctionnalité :
bash
Copier
Modifier
git checkout -b feature/ajout-notification
Lorsque la fonctionnalité est terminée, faites un commit et ouvrez une Pull Request pour l'intégrer dans la branche principale.
Une fois la fonctionnalité validée, le numéro de version est mis à jour et la version est taguée avant de publier.
Contribuer
Si vous souhaitez contribuer à ce projet, veuillez suivre les étapes ci-dessous :

Fork le repository.
Créez une branche pour votre fonctionnalité ou correction (git checkout -b feature/ma-fonctionnalité).
Committez vos changements (git commit -am 'Ajout d\'une fonctionnalité').
Push votre branche (git push origin feature/ma-fonctionnalité).
Ouvrez une Pull Request pour discuter des changements.
License
Ce projet est sous licence MIT.

markdown
Copier
Modifier

### Explication :
- **SlaabX** : Une brève introduction à ce qu'est ton projet.
- **Technologies utilisées** : Les technologies principales que tu utilises pour le front-end, le back-end et la base de données.
- **Installation** : Des instructions détaillées pour cloner et configurer ton projet localement.
- **Versioning** : Une explication du système de versioning sémantique (SemVer) et de la gestion des versions.
- **Contribuer** : Des instructions pour les autres développeurs qui souhaitent contribuer au projet.
- **License** : Mention de la licence MIT, que tu peux modifier si nécessaire.


