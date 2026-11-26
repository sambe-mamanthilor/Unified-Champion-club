# Consignes du projet — Unified Champions

> Source : réunion de lancement du 20/11/2026 (enregistrement `reunions/fichiers-audio/Reunion_20-11-26.m4a`, transcription `reunions/transcription/Transcription_Reunion_20-11-26`).
> Les passages marqués *(interprétation)* corrigent une erreur probable de la transcription automatique et sont à confirmer avec l'enseignant.

---

## 1. Contexte

L'application **Unified Champions** sera mise à disposition de la **salle esport**. Elle sert à la fois d'outil de suivi pour l'enseignant (assiduité, progression, engagement) et d'outil de vie de club pour les joueurs (actualité, échanges, recrutement).

L'ambition affichée : que rejoindre l'équipe esport soit aussi prestigieux que **faire partie de l'équipe de football américain d'une université américaine**. L'application doit être assez attractive pour que tout le monde veuille l'installer.

---

## 2. Objectifs de l'application

### 2.1 Gérer l'assiduité — priorité n°1

L'enseignant ne veut plus faire l'appel : l'assiduité doit être enregistrée automatiquement.

- **Définition** : un joueur est présent quand il **joue un match depuis l'intérieur de la salle**.
- **Détection : les deux conditions doivent être réunies**
  1. **Connexion à l'application depuis la salle**, vérifiée par l'**adresse IP** (IP de la salle).
  2. **Activité sur le compte Riot** du joueur (match joué) sur ce même créneau.
  → Connexion depuis la salle **+** activité Riot = joueur présent.
- **Existant à reprendre** : une partie de l'application existe déjà. Elle permet :
  - l'inscription des joueurs avec **login + mot de passe** ;
  - l'enregistrement des connexions depuis la salle (via IP) ;
  - l'enregistrement des **résultats de match** ;
  - le suivi de la **progression**.
- **À réparer** : la liaison des joueurs avec leur **compte Riot** (« contrat IOT » dans la transcription) ne fonctionne plus. **Il faut la remettre en marche** : sans elle, impossible de détecter l'activité (assiduité) ni de mesurer la progression.

### 2.2 Suivre la progression

- **Source des données : le compte Riot** du joueur (historique et résultats de matchs, rang, statistiques).
- Les résultats sont enregistrés dans l'application pour visualiser la **progression** de chaque joueur dans le temps.

### 2.3 Suivre l'engagement en compétition

Troisième critère de notation : le joueur doit **s'engager en compétition**. L'application doit permettre de le mesurer / le valoriser.

> **La note d'esport repose sur 3 critères :**
> 1. **Assiduité** — être là.
> 2. **Progression** — s'améliorer.
> 3. **Engagement en compétition** — participer à des compétitions.

### 2.4 Actualité de la salle

Les joueurs doivent pouvoir consulter l'actualité :
- matchs programmés ;
- **scrims** (matchs d'entraînement) ;
- annonces de joueurs qui cherchent des coéquipiers / partenaires.

### 2.5 Connexion avec le Discord Unified Champions

- L'application doit être **reliée au serveur Discord** de Unified Champions.
- Pistes évoquées : **webhooks** Discord (publication automatique d'annonces, etc.). Le mode d'intégration est à étudier par l'équipe.

### 2.6 Échanger

L'application doit permettre aux joueurs **d'échanger** entre eux.

### 2.7 Recruter des joueurs

- N'importe qui doit pouvoir installer l'application et **demander à devenir membre**.
- **L'enseignant valide les comptes** : l'adhésion à l'équipe passe par une validation manuelle (rôle administrateur).

---

## 3. Organisation du travail (obligatoire)

### 3.1 Réunion hebdomadaire

- **Fréquence** : 1 réunion par semaine, **en général le vendredi**.
- **Durée** : **15 minutes**.
- **Lieu** : en bas, autour de la table ronde de l'enseignant.
- **Ordre du jour fixe** :
  1. Qu'est-ce qu'on a fait ?
  2. Qu'est-ce qui coince ?
  3. Qu'est-ce qu'on fait ensuite ?
- **Responsabilité** : **c'est l'équipe qui organise** la réunion et qui **invite l'enseignant via Google Agenda**.

### 3.2 GitHub — la source de vérité

- Créer un dépôt GitHub et **y inviter l'enseignant** (il suit l'activité du dépôt). ✅ Dépôt créé.
- **Tout** doit s'y trouver, en fichiers **Markdown (.md)** :
  - les **enregistrements** de réunion ;
  - leurs **transcriptions** ;
  - un dossier dédié aux réunions avec **tous les comptes rendus** ;
  - les **spécifications de l'application** ;
  - toute autre documentation utile.
- **Objectif final** : la spécification doit être si complète qu'à la fin il suffira de demander à un agent IA « fais le site » pour qu'il puisse construire l'application **tout seul**, puisque tout aura été spécifié et défini.

### 3.3 Trello — répartition des tâches

- Tenir un tableau Trello pour savoir **qui fait quoi et pour quand**.
- Les tâches doivent être :
  - **actionnables** ;
  - **de petite taille** (réalisables par une seule personne) ;
  - chacune avec **un responsable** et **une échéance**.

---

## 4. Checklist

### Organisation
- [x] Créer le dépôt GitHub
- [ ] Inviter l'enseignant sur le dépôt GitHub
- [x] Déposer l'enregistrement et la transcription de la réunion du 20/11
- [ ] Rédiger le compte rendu de la réunion du 20/11 dans `reunions/`
- [x] Créer le Trello
- [ ] Remplir le Trello avec des tâches courtes (responsable + échéance)
- [ ] Envoyer l'invitation Google Agenda pour la réunion hebdo (vendredi, 15 min)
- [ ] Après chaque réunion : enregistrement + transcription + compte rendu sur le GitHub

### Spécifications à rédiger
- [ ] Récupérer et analyser l'application existante (inscription, IP, résultats, progression)
- [ ] Spécifier la liaison compte Riot (à réparer) et l'accès à l'API Riot (clé API, données récupérables)
- [ ] Spécifier la détection de présence : IP de la salle **+** activité Riot sur le même créneau
- [ ] Spécifier le calcul / l'affichage de la progression à partir des données Riot
- [ ] Spécifier le suivi de l'engagement en compétition
- [ ] Spécifier le fil d'actualité (matchs, scrims, recherches de joueurs)
- [ ] Spécifier l'intégration Discord (webhooks, bot, etc.)
- [ ] Spécifier la messagerie / les échanges entre joueurs
- [ ] Spécifier le parcours d'inscription + validation des comptes par l'enseignant (rôles : joueur, admin)

---

## 5. Questions à poser à l'enseignant

1. Quels jeux Riot sont concernés (League of Legends, Valorant, TFT…) ? Quels indicateurs de progression comptent (rang, winrate, KDA…) ?
2. Où est le code de l'application existante, et sous quelle techno ?
3. Quelle(s) adresse(s) IP correspondent à la salle ?
4. Comment mesure-t-on concrètement « l'engagement en compétition » (inscriptions, matchs officiels, résultats) ?
5. Plateforme visée : web, mobile, ou les deux ?
6. Avons-nous un accès administrateur au serveur Discord Unified Champions ?
