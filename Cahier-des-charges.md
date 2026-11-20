# TASKFLOW

## Cahier des charges fonctionnel et technique

**Nom du projet :** TASKFLOW  
**Nature du projet :** Application web Full Stack  
**Version du document :** 1.0  
**Date :** Novembre 2026  
**Statut :** Document de référence

---

# 1. PRÉSENTATION GÉNÉRALE DU PROJET

## 1.1. Contexte

Dans un environnement où les activités personnelles, académiques et professionnelles deviennent de plus en plus nombreuses, l'organisation des tâches et le suivi des objectifs représentent un véritable défi.

Les utilisateurs ont besoin d'un outil leur permettant de centraliser leurs activités, de planifier leur travail, de suivre leur progression et de respecter leurs échéances.

TASKFLOW est conçu pour répondre à ce besoin à travers une plateforme web moderne, intuitive et évolutive.

## 1.2. Présentation de TASKFLOW

TASKFLOW est une application web de gestion de tâches et de projets permettant aux utilisateurs de créer, organiser, planifier et suivre leurs différentes activités depuis une interface centralisée.

L'application proposera notamment :

- La gestion des comptes utilisateurs.
- La création et l'organisation de projets.
- La création et le suivi des tâches.
- La gestion des priorités et des échéances.
- Un tableau de bord présentant les statistiques.
- Une vue Kanban pour visualiser l'avancement du travail.
- Des outils de recherche, de filtrage et de tri.
- Des paramètres personnalisés.

L'objectif est de construire une application complète, sécurisée, responsive et maintenable.

## 1.3. Problématique

Les utilisateurs rencontrent souvent plusieurs difficultés :

- Manque d'organisation dans leurs activités quotidiennes.
- Difficulté à hiérarchiser les tâches.
- Oubli des échéances importantes.
- Absence de visibilité sur l'avancement des projets.
- Dispersion des informations entre plusieurs outils.
- Difficulté à évaluer leur productivité.

**Question centrale :**

Comment concevoir une application web permettant de centraliser les tâches et les projets, de faciliter leur organisation et d'améliorer le suivi de la productivité des utilisateurs ?

## 1.4. Solution proposée

TASKFLOW proposera un espace personnel dans lequel chaque utilisateur pourra gérer ses projets et ses tâches.

Un tableau de bord lui permettra de visualiser rapidement ses activités, ses tâches terminées, ses tâches en cours et ses échéances.

L'application devra être simple à utiliser tout en offrant des fonctionnalités suffisamment avancées pour répondre à des besoins réels.

---

# 2. OBJECTIFS DU PROJET

## 2.1. Objectif général

Développer une application web Full Stack de gestion des tâches et des projets permettant aux utilisateurs d'améliorer leur organisation, leur planification et leur productivité.

## 2.2. Objectifs spécifiques

Le projet vise à :

1. Permettre la création et la gestion de comptes utilisateurs.
2. Faciliter la création, la modification et l'archivage des projets.
3. Permettre la gestion complète des tâches.
4. Organiser les tâches selon leur statut et leur priorité.
5. Permettre la définition des échéances.
6. Offrir une représentation visuelle de l'avancement.
7. Fournir des statistiques utiles à travers un tableau de bord.
8. Garantir la confidentialité des données de chaque utilisateur.
9. Concevoir une architecture logicielle évolutive et maintenable.
10. Mettre en production une application accessible sur Internet.

---

# 3. ACTEURS DU SYSTÈME

## 3.1. Utilisateur

L'utilisateur est la personne qui possède un compte sur TASKFLOW.

Il peut :

- Créer un compte.
- Se connecter et se déconnecter.
- Consulter son tableau de bord.
- Créer et gérer ses projets.
- Créer et gérer ses tâches.
- Consulter ses statistiques.
- Modifier ses informations personnelles.
- Configurer ses préférences.
- Archiver et restaurer ses éléments selon les règles prévues.

Chaque utilisateur dispose d'un espace personnel indépendant.

## 3.2. Administrateur

L'administrateur est un acteur réservé à une évolution ultérieure du projet.

Ses responsabilités potentielles :

- Consulter les comptes utilisateurs.
- Gérer les utilisateurs.
- Surveiller le fonctionnement général de la plateforme.
- Intervenir sur les problèmes de gestion et de sécurité.

**Important :** les fonctionnalités d'administration ne font pas partie de la première version. Elles seront étudiées après la réalisation du cœur de l'application.

---

# 4. DESCRIPTION FONCTIONNELLE

Cette section définit les fonctionnalités attendues de TASKFLOW.

## 4.1. Gestion des comptes utilisateurs

L'application devra permettre :

### Inscription

- Création d'un compte.
- Saisie du nom.
- Saisie de l'adresse e-mail.
- Définition d'un mot de passe.
- Vérification des champs obligatoires.
- Vérification de l'unicité de l'adresse e-mail.
- Enregistrement sécurisé du compte.

### Connexion

- Saisie de l'adresse e-mail.
- Saisie du mot de passe.
- Vérification des identifiants.
- Ouverture d'une session sécurisée.
- Redirection vers le tableau de bord.

### Déconnexion

- Fermeture de la session.
- Suppression ou invalidation des informations d'authentification côté client selon la stratégie retenue.

### Gestion du profil

- Consultation du profil.
- Modification du nom.
- Modification de l'adresse e-mail avec vérification appropriée.
- Modification du mot de passe.

La récupération du mot de passe sera prévue dans une version ultérieure.

## 4.2. Gestion des projets

Chaque utilisateur pourra gérer ses propres projets.

### Création d'un projet

Informations :

- Nom du projet.
- Description.
- Date de création générée automatiquement.

### Consultation

- Afficher tous les projets de l'utilisateur.
- Consulter les informations d'un projet.
- Afficher les tâches associées.

### Modification

- Modifier le nom.
- Modifier la description.

### Archivage

- Archiver un projet.
- Consulter les projets archivés.
- Restaurer un projet.

Un projet archivé ne pourra plus recevoir de nouvelles tâches tant qu'il n'aura pas été restauré.

## 4.3. Gestion des tâches

La gestion des tâches constitue le cœur de TASKFLOW.

### Création d'une tâche

Chaque tâche devra pouvoir contenir :

- Un titre obligatoire.
- Une description facultative.
- Un statut.
- Une priorité.
- Une date d'échéance facultative.
- Un projet associé facultatif.

Les dates de création et de modification seront générées automatiquement.

### Consultation des tâches

- Afficher toutes les tâches de l'utilisateur.
- Consulter les détails d'une tâche.
- Afficher les tâches par projet.
- Afficher les tâches selon leur statut.

### Modification

- Modifier le titre.
- Modifier la description.
- Modifier le statut.
- Modifier la priorité.
- Modifier l'échéance.
- Modifier le projet associé.

### Suppression et archivage

- Archiver une tâche.
- Consulter les tâches archivées.
- Restaurer une tâche.
- Supprimer définitivement une tâche depuis la corbeille, après confirmation.

La suppression définitive devra être une action explicite.

## 4.4. Gestion des statuts

Chaque tâche possède un statut parmi les suivants :

| Statut      | Signification                    |
| ----------- | -------------------------------- |
| TODO        | Tâche à faire                    |
| IN_PROGRESS | Tâche en cours                   |
| IN_REVIEW   | Tâche en attente de vérification |
| DONE        | Tâche terminée                   |

L'utilisateur pourra modifier le statut d'une tâche.

Une tâche terminée pourra être rouverte.

## 4.5. Gestion des priorités

Chaque tâche possédera un niveau de priorité :

| Priorité | Signification |
| -------- | ------------- |
| LOW      | Faible        |
| MEDIUM   | Moyenne       |
| HIGH     | Élevée        |
| URGENT   | Urgente       |

La priorité sera indépendante du statut.

## 4.6. Tableau de bord

Le tableau de bord constituera la page principale après connexion.

Il devra présenter :

### Indicateurs

- Nombre total de tâches actives.
- Nombre de tâches terminées.
- Nombre de tâches en cours.
- Nombre de tâches en retard.
- Nombre de projets actifs.

### Informations complémentaires

- Tâches récemment créées.
- Tâches à échéance proche.
- Progression globale.
- Répartition des tâches par statut.
- Projets récemment consultés.

Les statistiques devront être calculées à partir des données réelles de l'utilisateur connecté.

## 4.7. Vue Kanban

L'application devra proposer une vue Kanban permettant de visualiser les tâches selon leur statut.

Les colonnes seront :

- À faire.
- En cours.
- En vérification.
- Terminées.

L'utilisateur pourra déplacer une tâche d'une colonne à une autre.

La modification devra être enregistrée et conservée.

## 4.8. Recherche, filtrage et tri

L'utilisateur pourra :

### Rechercher

- Rechercher une tâche par son titre.
- Rechercher un projet par son nom.

### Filtrer

- Par statut.
- Par priorité.
- Par projet.
- Par échéance.
- Par état d'archivage.

### Trier

- Par date de création.
- Par date d'échéance.
- Par priorité.
- Par ordre alphabétique.

## 4.9. Notifications et rappels

Une évolution de TASKFLOW devra permettre :

- D'afficher des alertes pour les échéances proches.
- De signaler les tâches en retard.
- D'informer l'utilisateur des événements importants.

Les notifications par e-mail ou push pourront être étudiées dans une version ultérieure.

## 4.10. Paramètres

L'utilisateur pourra personnaliser certains éléments :

- Préférences d'affichage.
- Thème clair ou sombre.
- Préférences de notification.
- Informations personnelles.

---

# 5. RÈGLES DE GESTION

Les règles suivantes devront être respectées par l'ensemble de l'application.

1. Chaque utilisateur possède un identifiant unique.
2. Chaque adresse e-mail doit être unique.
3. Un utilisateur peut posséder plusieurs projets.
4. Un utilisateur peut posséder plusieurs tâches.
5. Un projet appartient obligatoirement à un seul utilisateur.
6. Une tâche appartient obligatoirement à un seul utilisateur.
7. Une tâche peut être associée à zéro ou un projet.
8. Une tâche ne peut être associée qu'à un projet appartenant au même utilisateur.
9. Une tâche doit obligatoirement posséder un titre.
10. Une tâche doit posséder un statut valide.
11. Une tâche doit posséder une priorité valide.
12. Une tâche terminée peut être rouverte.
13. Une tâche peut être archivée et restaurée.
14. Un projet archivé ne peut plus recevoir de nouvelles tâches.
15. Les dates de création et de modification sont gérées automatiquement.
16. Une date d'échéance est facultative.
17. Un utilisateur ne peut consulter, modifier ou supprimer que ses propres ressources.
18. L'accès aux données doit être contrôlé côté serveur.
19. Les opérations sensibles doivent être validées avant leur exécution.
20. Une suppression définitive doit nécessiter une confirmation explicite.

---

# 6. EXIGENCES NON FONCTIONNELLES

## 6.1. Sécurité

- Les mots de passe doivent être hachés avec un algorithme adapté.
- Les données doivent être protégées contre les accès non autorisés.
- Les entrées doivent être validées côté client et côté serveur.
- Les requêtes SQL doivent utiliser des paramètres sécurisés.
- Les secrets et identifiants de connexion ne doivent pas être exposés dans le code public.
- Les sessions et mécanismes d'authentification doivent être correctement protégés.

## 6.2. Performance

- L'application doit répondre rapidement aux opérations courantes.
- Les requêtes à la base de données doivent être optimisées.
- La pagination devra être prévue pour les listes volumineuses.
- Les ressources inutiles devront être évitées.

## 6.3. Ergonomie

- L'interface doit être claire et cohérente.
- La navigation doit être intuitive.
- Les messages d'erreur doivent être compréhensibles.
- Les actions importantes doivent être facilement accessibles.

## 6.4. Responsive design

L'application devra être adaptée :

- Aux ordinateurs.
- Aux tablettes.
- Aux smartphones.

## 6.5. Accessibilité

- Utilisation d'une structure HTML sémantique.
- Contraste suffisant.
- Navigation au clavier.
- Libellés explicites pour les formulaires.
- États interactifs perceptibles.

## 6.6. Maintenabilité

- Séparation des responsabilités.
- Organisation modulaire du code.
- Nommage cohérent.
- Documentation technique.
- Gestion des erreurs.
- Utilisation de Git pour le suivi des versions.

## 6.7. Compatibilité

L'application devra fonctionner sur les versions récentes des principaux navigateurs : Chrome, Firefox, Edge et Safari.

---

# 7. ARCHITECTURE TECHNIQUE

TASKFLOW sera développée progressivement selon une architecture séparant le frontend, le backend et la base de données.

## 7.1. Frontend

Technologies :

- HTML5.
- CSS3.
- JavaScript moderne (Vanilla JavaScript dans la première version).

Responsabilités :

- Présentation de l'interface.
- Gestion des interactions.
- Validation initiale des formulaires.
- Communication avec l'API.
- Affichage des données reçues du serveur.

## 7.2. Backend

Technologies :

- Node.js.
- Express.js.

Responsabilités :

- Exposition d'une API REST.
- Gestion des requêtes.
- Authentification.
- Autorisation.
- Validation des données.
- Exécution de la logique métier.
- Communication avec la base de données.
- Gestion centralisée des erreurs.

Architecture logicielle envisagée :

- Routes.
- Contrôleurs.
- Services.
- Middlewares.
- Couche d'accès aux données.
- Configuration.

## 7.3. Base de données

Technologie : MySQL.

Responsabilités :

- Stockage des utilisateurs.
- Stockage des projets.
- Stockage des tâches.
- Gestion des relations.
- Garantie de l'intégrité des données.
- Exécution des opérations CRUD.

## 7.4. Outils de développement

- Visual Studio Code.
- Git.
- GitHub.
- Navigateur web.
- MySQL Workbench.
- Postman ou outil équivalent pour tester l'API.

---

# 8. MODÈLE DE DONNÉES PRÉVISIONNEL

La première version reposera sur trois entités principales.

## 8.1. USER

Représente les utilisateurs de la plateforme.

Attributs prévisionnels :

- id
- name
- email
- password_hash
- created_at
- updated_at

## 8.2. PROJECT

Représente les projets créés par les utilisateurs.

Attributs prévisionnels :

- id
- user_id
- name
- description
- created_at
- updated_at
- archived_at

## 8.3. TASK

Représente les tâches créées par les utilisateurs.

Attributs prévisionnels :

- id
- user_id
- project_id
- title
- description
- status
- priority
- due_date
- created_at
- updated_at
- archived_at

## 8.4. Relations

- Un utilisateur peut posséder plusieurs projets.
- Un utilisateur peut posséder plusieurs tâches.
- Un projet peut contenir plusieurs tâches.
- Une tâche peut exister sans projet.
- Une tâche appartient toujours à un utilisateur.

Le modèle physique définitif, les types SQL, les contraintes et les index seront établis pendant la phase de conception de la base de données.

---

# 9. API REST PRÉVISIONNELLE

Le backend devra exposer des points d'accès organisés par ressources.

Exemples de routes envisagées :

## Authentification

- POST /api/auth/register
- POST /api/auth/login
- POST /api/auth/logout
- GET /api/auth/me

## Utilisateurs

- GET /api/users/me
- PATCH /api/users/me

## Projets

- GET /api/projects
- POST /api/projects
- GET /api/projects/:id
- PATCH /api/projects/:id
- DELETE /api/projects/:id
- PATCH /api/projects/:id/archive
- PATCH /api/projects/:id/restore

## Tâches

- GET /api/tasks
- POST /api/tasks
- GET /api/tasks/:id
- PATCH /api/tasks/:id
- DELETE /api/tasks/:id
- PATCH /api/tasks/:id/status
- PATCH /api/tasks/:id/archive
- PATCH /api/tasks/:id/restore

## Tableau de bord

- GET /api/dashboard

Ces routes sont prévisionnelles. Les méthodes, réponses, paramètres et règles d'autorisation seront spécifiés pendant le développement du backend.

---

# 10. INTERFACE ET EXPÉRIENCE UTILISATEUR

L'interface devra adopter une identité visuelle moderne, professionnelle et cohérente.

## 10.1. Pages principales

1. Page d'accueil ou page de présentation.
2. Page d'inscription.
3. Page de connexion.
4. Tableau de bord.
5. Page de gestion des projets.
6. Page de détails d'un projet.
7. Page de gestion des tâches.
8. Vue Kanban.
9. Page de détails d'une tâche.
10. Page de profil.
11. Page des paramètres.
12. Page des éléments archivés.

## 10.2. Éléments d'interface

- Barre de navigation.
- Menu latéral.
- Cartes statistiques.
- Tableaux de données.
- Formulaires.
- Fenêtres de confirmation.
- Menus déroulants.
- Filtres.
- Notifications visuelles.
- Indicateurs de progression.

## 10.3. Principes de conception

L'interface devra :

- Éviter la surcharge visuelle.
- Utiliser une hiérarchie typographique cohérente.
- Faciliter la lecture des informations.
- Employer des couleurs cohérentes selon les statuts et les priorités.
- Maintenir une expérience uniforme sur les différentes pages.

La direction artistique définitive sera validée à travers des maquettes avant l'intégration complète.

---

# 11. ORGANISATION DU DÉVELOPPEMENT

Le projet sera développé par phases successives.

## PHASE 1 — Analyse et conception

- Validation du cahier des charges.
- Définition des besoins.
- Définition des règles métier.
- Modélisation des données.
- Conception des maquettes.
- Définition de l'architecture.

**Livrables :** cahier des charges, modèle de données, diagrammes et maquettes.

## PHASE 2 — Préparation de l'environnement

- Création du dépôt Git.
- Organisation du projet.
- Configuration de l'environnement.
- Mise en place des conventions de développement.

**Livrable :** structure de projet opérationnelle.

## PHASE 3 — Développement frontend

- Structure HTML.
- Intégration CSS.
- Responsive design.
- Composants d'interface.
- Interactions JavaScript.
- Gestion des tâches côté client pour les premiers essais.

**Livrable :** frontend fonctionnel avec données de démonstration.

## PHASE 4 — Développement backend

- Initialisation du serveur Node.js.
- Configuration Express.
- Création des routes.
- Création des contrôleurs.
- Mise en place des services.
- Validation et gestion des erreurs.
- Développement de l'API REST.

**Livrable :** API fonctionnelle.

## PHASE 5 — Base de données

- Installation et configuration MySQL.
- Création de la base de données.
- Création des tables.
- Définition des relations.
- Contraintes et index.
- Intégration avec le backend.

**Livrable :** base de données opérationnelle.

## PHASE 6 — Authentification et sécurité

- Inscription.
- Connexion.
- Déconnexion.
- Protection des routes.
- Gestion des sessions.
- Contrôle des autorisations.
- Protection des données utilisateurs.

**Livrable :** système d'authentification sécurisé.

## PHASE 7 — Intégration Full Stack

- Connexion du frontend à l'API.
- Récupération des données.
- Création et modification des ressources.
- Gestion des erreurs réseau.
- Synchronisation des données.

**Livrable :** application Full Stack fonctionnelle.

## PHASE 8 — Tests et qualité

- Tests unitaires.
- Tests d'intégration.
- Tests des routes API.
- Tests des règles métier.
- Tests de sécurité.
- Tests responsive.
- Correction des anomalies.

**Livrable :** version testée et stabilisée.

## PHASE 9 — Déploiement

- Préparation de la production.
- Configuration des variables d'environnement.
- Hébergement du frontend.
- Hébergement du backend.
- Hébergement de MySQL.
- Configuration HTTPS.
- Documentation du déploiement.

**Livrable :** application accessible en ligne.

---

# 12. PÉRIMÈTRE DU PROJET

Pour éviter de disperser les efforts, les fonctionnalités seront réparties en plusieurs versions.

## Version 1 — MVP

Le produit minimum viable devra comprendre :

- Inscription et connexion.
- Gestion du profil de base.
- Tableau de bord.
- Création et gestion des projets.
- Création et gestion des tâches.
- Gestion des statuts.
- Gestion des priorités.
- Gestion des échéances.
- Recherche et filtres essentiels.
- Authentification et protection des données.
- Connexion complète entre frontend, backend et MySQL.

## Version 2 — Améliorations

- Vue Kanban avec déplacement des tâches.
- Archivage et corbeille avancés.
- Statistiques détaillées.
- Thème clair et sombre.
- Notifications et rappels.
- Amélioration de l'expérience utilisateur.

## Version 3 — Fonctionnalités avancées

- Administration de la plateforme.
- Partage de projets.
- Collaboration entre utilisateurs.
- Attribution de tâches à des membres.
- Commentaires et historique des activités.
- Notifications avancées.
- Exportation de données.
- Fonctionnalités supplémentaires selon les besoins.

---

# 13. CRITÈRES D'ACCEPTATION

Le projet sera considéré comme fonctionnel lorsque les conditions suivantes seront vérifiées :

1. Un utilisateur peut créer un compte et se connecter.
2. Un utilisateur peut gérer ses propres projets.
3. Un utilisateur peut créer une tâche sans projet.
4. Un utilisateur peut associer une tâche à l'un de ses projets.
5. Un utilisateur peut modifier le statut et la priorité d'une tâche.
6. Les tâches peuvent être filtrées et recherchées.
7. Le tableau de bord présente des statistiques cohérentes.
8. Un utilisateur ne peut pas accéder aux ressources d'un autre utilisateur.
9. Les données sont conservées dans MySQL.
10. L'application fonctionne sur ordinateur et smartphone.
11. Les erreurs sont gérées proprement.
12. Les fonctionnalités principales ont été testées.
13. L'application est accessible depuis un environnement de production.

---

# 14. GESTION DU CODE ET DOCUMENTATION

Le développement sera suivi avec Git et GitHub.

Les règles suivantes seront appliquées :

- Effectuer des commits réguliers.
- Utiliser des messages de commit explicites.
- Organiser le code par responsabilités.
- Documenter les fonctionnalités importantes.
- Maintenir un fichier README.
- Documenter les variables d'environnement nécessaires dans un fichier `.env.example`.
- Ne jamais publier les secrets dans le dépôt.
- Utiliser des branches lorsque le développement de fonctionnalités parallèles le justifie.

La documentation devra permettre à un autre développeur de comprendre, installer et exécuter le projet.

---

# 15. RISQUES ET CONTRAINTES

Les principaux risques identifiés sont :

| Risque                        | Mesure préventive                           |
| ----------------------------- | ------------------------------------------- |
| Mauvaise organisation du code | Architecture définie avant l'implémentation |
| Failles de sécurité           | Validation et contrôle côté serveur         |
| Perte de données              | Sauvegardes et gestion des suppressions     |
| Difficultés d'intégration     | Développement progressif et tests           |
| Complexité excessive          | Respect du périmètre MVP                    |
| Problèmes de performance      | Requêtes optimisées et pagination           |
| Mauvaise expérience mobile    | Tests responsive réguliers                  |

Contraintes techniques :

- Utilisation des technologies retenues.
- Compatibilité avec les navigateurs modernes.
- Respect des bonnes pratiques de développement.
- Architecture évolutive.
- Possibilité de déployer l'application sur des services d'hébergement accessibles.

---

# 16. LIVRABLES FINAUX

À la fin du projet, les éléments suivants devront être disponibles :

1. Le cahier des charges.
2. Les diagrammes de conception.
3. Les maquettes de l'interface.
4. Le code source frontend.
5. Le code source backend.
6. Le script de création de la base de données.
7. La documentation de l'API.
8. Les tests automatisés.
9. Le fichier README.
10. Le dépôt GitHub.
11. L'application déployée.
12. Une présentation du projet pour le portfolio.

---

# 17. CONCLUSION

TASKFLOW est un projet de développement web Full Stack ayant pour ambition de proposer une solution moderne de gestion des tâches et des projets.

Sa réalisation reposera sur une démarche progressive allant de l'analyse des besoins à la mise en production.

Le projet permettra de mettre en pratique les principales compétences du développement web : conception, intégration frontend, programmation JavaScript, développement backend, gestion des bases de données, sécurité, tests et déploiement.

Le respect du présent cahier des charges servira de référence pour orienter les décisions techniques et fonctionnelles tout au long du développement.

**FIN DU CAHIER DES CHARGES — TASKFLOW**
