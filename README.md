# **Cahier des charges – Application Web de planification d’événements liés au mariage**

# **1. Contexte général**

En discutant avec ma meilleure amie qui est entrain de penser à son mariage, elle m’a confié avoir beaucoup de difficultés à s’organiser et cette complexité est bien marquée dans sa culture turque mais aussi dans d’autres cultures asiatiques, maghrébines,... où le mariage ne se limite pas à une seule journée. Chacun implique des invités, des prestataires, un budget et un programme propres.

Dans son cas, trois événements distincts (kiz isteme (= fiancailles), soirée du henné, cérémonie du mariage)

Et en y réfléchissant, j’ai réalisé que depuis mon plus jeune âge, mon entourage a toujours rencontré les mêmes difficultés lors de l’organisation de ces événements. C’est donc pour ça que j’aimerai concevoir une app web qui permet de planifier et gérer efficacement ce type d’évenement.

---


# **2. Personas et scénarios**

## **👰🏻‍♀️Persona 1.A – Ayla la mariée (admin principale)**

**Âge :** 23 ans

**Profil :** Organisée et perfectionniste, elle souhaite garder une vision globale et maîtriser chaque détail de son mariage.

**Objectif :** Centraliser tous les événements et accéder à chaque catégorie pour chaque événement facilement (budget, planning, invités, prestataires) dans un seul outil.

### **Scénario 1 – Suivre le budget par catégories**

Ayla se connecte sur l’application et arrive sur le Dashboard principal.
Elle y voit une vue synthétique du budget global des événements :

- budget total,
- montant déjà utilisé,
- budget restant.

Une barre de progression horizontale lui permet de visualiser rapidement la répartition par catégories (salle, restauration, robe, décoration, animation…).
Grâce au bouton dropdown, elle peut naviguer entre le budget global et les 3 autres événements séparément.
En cliquant sur la catégorie « Décoration », Ayla accède à une vue détaillée listant toutes les dépenses associées, avec pour chacune :

- le nom,
- le montant,
- le statut (prévu, confirmé, payé),
- une éventuelle note interne.

Elle remarque que la décoration va bientôt dépasser le budget initial prévu.
Elle décide alors d’ajouter une nouvelle dépense avant de l'oublier :

- Intitulé : Location florale
- Catégorie : Décoration
- Montant estimé : 250 €
- Statut : Prévu
- Note interne : Comparer avec d’autres prestataires avant validation finale.

Après validation, la dépense est immédiatement ajoutée à la liste.
Le dashboard se met à jour en temps réel, recalculant le total utilisé et mettant visuellement en évidence le dépassement de budget pour la catégorie décoration.

### **Scénario 2 – Structurer la planification jusqu’au jour J**

Ayla souhaite organiser le déroulé complet des événements liés au mariage.
Depuis la sidebar, elle accède au module Planning.

Elle crée successivement trois événements principaux :
- Fiançailles
- Soirée henné
- Mariage

Pour chacun, elle encode :
- le lieu (nom + adresse),
- la date,
- l’heure de début et de fin.
- le budget 
- le nombre d'invités

Elle peut aller plus loin avec plus de precisions en cliquant sur une des cartes des événements et peut découper la journée en tranches horaires :
- 14h00 – 15h00 : Cérémonie
- 15h00 – 16h30 : Photos
- 17h00 – 19h00 : Réception
- 19h00 – … : Soirée

Chaque tranche horaire peut contenir :
- une description détaillée,
- un lieu associé,
- les prestataires concernés.
- L’interface lui permet de visualiser la journée sous forme de timeline verticale, claire et lisible.

Une fois satisfaite, Ayla utilise la fonction Exporter en PDF afin de générer un document récapitulatif qu’elle pourra partager avec sa famille ou ses prestataires.

### **Scénario 3 – Gestion des invités et plan de table**

À mesure que les réponses arrivent, Ayla met à jour la liste des invités.
Chaque invité possède un statut :

- Confirmé
- En attente
- Refusé

Elle peut filtrer la liste selon ces statuts pour suivre facilement l’avancement.

### *Fonctionnalité à voir*
Une fois la majorité des réponses reçues, Ayla accède au module Plan de table.
Elle crée plusieurs tables (Table 1, Table 2, Table famille, Table amis…) et y assigne les invités par simple glisser-déposer.

Certaines règles implicites guident son placement :

- placer certaines personnes ensemble,
- éviter certains mélanges.

Le plan de table final est enregistré et devient visible pour les prestataires concernés, notamment le service de location de chaises et le traiteur.

---

## **🤵🏽‍♂️Persona 1.B –  Peter, le futur marié (co-admin)**

**Âge :** 24 ans

**Profil :** Il souhaite savoir clairement ce qu’il doit faire sans se perdre dans les détails.

**Objectif :** Gérer ses tâches, valider les décisions importantes et garder un œil sur le budget.

### **Scénario 1 – Voir sa liste de tâches**

Peter se connecte et arrive sur le même Dashboard qu'Ayla. Grâce à un filtre « Mes tâches », il peut se concentrer sur ce qui lui est assigné sans être noyé par tous les détails :
	•	Aller choisir le costume — À faire
	•	Contacter le DJ — À faire
	•	Valider le devis des chaises — À faire

Il marque « Contacter le DJ » comme Terminée. Le pourcentage d'avancement global se met automatiquement à jour sur le dashboard, visible par Ayla et Peter en temps réel.

### **Scénario 2 – Vérifier le budget avant validation**

Avant de valider la location de chaises, Peter consulte le module Budget. Il filtre par catégorie « Décoration » et vérifie le budget prévu, le montant déjà engagé et le restant disponible.

Constatant que la dépense reste dans les limites, il se rend dans le module Prestataires, ouvre la fiche du loueur et clique sur « Valider le devis ». 
*A voir : Ayla reçoit une notification automatique indiquant que le devis a été validé par Peter.*

---

## **🧑‍🔧Persona 2 – Prestataire externe (ex : location de chaises)**

**Profil :** Prestataire avec un accès limité à l’application.

**Objectif :** Suivre ce qui le concerne : budget associé, planning, matériel.

### **Scénario 1 – Consulter le budget lié à sa catégorie**

La prestataire se connecte avec un compte à droits restreints.
Elle accède uniquement à la catégorie de budget Décoration / Location matériel.

Elle peut consulter :
- les montants prévus,
- les montants validés,
- l’état de validation des dépenses.

Aucune modification n’est possible sans validation de la mariée.

### **Scénario 2 – Voir le planning et ajouter un rendez-vous**

Depuis le module Planning, la prestataire visualise uniquement les événements où elle intervient.

Elle repère son créneau le jour du mariage et propose un rendez-vous :
- Livraison des chaises – 10h30

Ce rendez-vous apparaît comme « à valider » dans l’interface d’Ayla, qui peut l’accepter ou le modifier.

### **Scénario 3 – Ajuster sa liste de matériel**

Dans sa section Matériel, la prestataire ajuste les quantités nécessaires :

- Chaises : 120
- Housses : 120

Ces modifications sont enregistrées et visibles par Ayla, qui peut les valider définitivement si nécessaire.

---

# **3. Fonctionnalités principales**

### **Côté public**

- Présentation du service
- Boutons **Login / Register**
- Mise en avant des avantages et fonctionnalités
- Aperçu du côté admin (mockups / captures / sections résumées)

---

# **4. Côté admin**

## **Auth**

- Création de compte
- Connexion / Déconnexion
- Invitation du futur marié (co-admin)
- Invitation d’un prestataire (accès limité) (pas besoin de créer un compte, joindre avec un code ?)
- Gestion du profil (nom, email, rôle)
- Mot de passe oublié (réinitialisation par email)

---

## **Dashboard**

- Avancement global du projet
- Prochaines deadlines (tâches)
- Budget utilisé / restant **trié par événement et domaine**
- Prochaines réunions avec prestataires
- Accès rapide aux sections
- statistique invité en fonction du status

---

## **Tâches**

- CRUD une tâche
    - titre
    - description
    - statut (TODO / IN_PROGRESS / DONE)
    - date limite
    - événement associé
- Vue personnalisée selon les rôles :
    - **Admin**  : voit et gère tout
    - **Co-admin** : gère uniquement ses tâches
    - **Prestataire** : lecture seule des tâches liées à son domaine (optionnel)
- Filtrage par statut
- Indicateur de progression (global + par catégorie si souhaité)

---

## **Lieux**

- Gestion des lieux pour chaque événement :
- Champs :
    - type d’événement
    - date / heure
    - nom du lieu
    - adresse

---

## **Liste des invités**

- CRUD invité
- status
- en ajoutant un invité, on peut en ajouter d'autres pour faire un groupe de famille ( pour pas lister tout les membre de chaque famille)

---

## **Budget**

- Définir un budget total
- budget par événement
- Créer des catégories (salle, robe, déco, etc.)
- Ajouter des dépenses (recommandé)
    - montant
    - catégorie
    - statut (prévu / payé)
    - prestataire lié (optionnel)
- Accès prestataire : lecture seule sur sa catégorie

---

## **Programme de l’événement**

- Création du programme global (timeline par heure)
- Ajout d’un élément :
    - heure début
    - heure fin
    - description
- Modification / suppression d’un élément

---

## **Moodboard**

- Importer des photos
- Créer des catégories (déco, fleurs, robe, couleurs…)
- Ajouter une note à une photo
- Partage avec prestataires (lecture ou contribution selon rôle)

---

## **À voir : Plan des tables**

Fonctions proposées :

- créer des tables
- assigner les invités aux tables

---

## **5. Mon planning**

1. Site public
2. Auth + rôles
3. Tâches + dashboard
4. Invités
5. Budget + catégories + dépenses
6. Programme + lieux
7. Moodboard + prestataire + (plan de table)


