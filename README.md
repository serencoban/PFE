# **Cahier des charges : Application web de planification d’événements liés aux mariage**



> champs lexical :
>
> - **Projet de mariage** : espace regroupant l’ensemble des événements et informations liés à l’organisation d’un mariage.
>- **Événement** : célébration distincte faisant partie d’un projet de mariage, comme les fiançailles, le henné ou le mariage.
>- **kiz isteme** (littéralement en turc : demander la fille ) = la famille de l’homme vient chez la famille de la fille pour demander la main de la fille , les fiançailles peuvent se faire à ce moment là
>- **soirée du henné** : soirée/fête traditionnel entre filles où on pose du henné décoratif sur les mains de la future mariée.
>- **RSVP** : réponse d’un invité indiquant s’il confirme ou non sa présence à un événement.


# **1. Contexte**

En discutant avec ma meilleure amie qui est entrain de penser à son mariage (+ celle de sa cousine l’année d’apres), elle m’a confié avoir beaucoup de difficultés à s’organiser ( un tableau excel pour les invités, pinterest ou tiktok pour les inspi, les prestatires etc etc)et cette complexité est bien marquée dans sa culture turque mais aussi dans d’autres cultures où le mariage ne se limite pas à une seule journée.

Dans son cas, **trois événements distincts (kiz isteme , soirée du henné, mariage)**

Et en y réfléchissant, j’ai réalisé que depuis mon plus jeune âge, mon entourage a toujours rencontré les mêmes difficultés lors de l’organisation de ces événements. C’est donc pour ca que j’aimerai concevoir une app web qui permet de planifier et gérer efficacement ce type d’évenement comme un journal 

---

# **2. Personas et scénarios**

### **Persona 1 – Ayla la mariée (admin principale)**

Ayla arrive sur le dashboard et voit une un resumé de tout :

- une carte pour les **jours restant** avant le prochain evenement à venir (date, progress bar)
- une carte pour tous les **evenements** et les info pour chacune de ses evenements ( date, nb invité, budget actuelle)
- une carte pour le **budget**, qu’elle peut filtrer par événement afin de voir le budget maximum prévu, les dépenses actuelles et le budget restant
- une carte pour les **taches**, où elle retrouve ses prochaines tâches, peu importe l’événement auquel elles appartiennent, et peut directement les marquer comme terminées
- une carte avec un graphique des **invités** confirmé, en attente et refusé
- une carte indiquant le statut des **prestataires**, afin de voir rapidement lesquels sont confirmés, en attente ou encore à rechercher

Son **dashboard** lui sert donc un peu de centre de contrôle. Par exemple, en se connectant, Ayla peut voir qu’il reste 42 jours avant sa soirée henné, que 7 invités n’ont toujours pas répondu, qu’un acompte doit être payé au traiteur et qu’elle a trois tâches à terminer cette semaine.

Pour la page **évenements**, Ayla peut créer plusieurs événements et les gérer indépendamment. Pour chaque événement, elle peut définir une date, lieu, budget, nb d’invités, tâches, prestataires et timeline et elle peut donc avoir 80 invités au henné et 150 au mariage sans mélanger les deux listes.

Ayla voudrait egalement une page dédié a ses **inspirations** car enregistré des tableaux sur Pinterest ou mettre en favori des Tiktok, elle s’y perd vite. Grace à cette section, elle va pouvoir neutraliser toutes ses inspirations et elle pourrait aussi avoir different moodbaord pour chaque evenements

En parlant de s’y perdre, elle voudrait aussi neutraliser tout ses **prestataires** pour qu’elle n’ait plus besoin de rechercher dans ses conversations pour se rappeler si elle avait déjà contacté quelqu’un ou non et savoir si c’est ok ou non

Ayla aime beaucoup quand c’est visuel, elle aimerait donc une **timeline** simple et efficace où elle peut preparer facilement le déroulement d’un evenement par tranches d’horaires + cerise sur le gateau, elle trouverait ca fantastique de pouvoir exporter cette timeline en PDF pour pouvoir l’envoyer a ses amies ( dont moi :> ) pour avoir un avis géneral et voir le déroulement qu’elle souhaite avoir et pourquoi pas l’envoyer au prestataire pour voir quand il sera utile.

chaque événements a ses invités, et dans cette page elle gere si l’invité et a confirmé, en attente ou refusé, et ce qui serait top, c’est un plan interactive ou elle peut positionner des tables et associé des invités à des chaises, juste pour avoir un joli visuel ( a voir, en fonction de la complexité)

---

### **Persona 2 – Prestataire externe, le photographe**

Le photographe reçoit un accès limité au projet. (Ayla peut cocher pour chaque prestataire, à quelle vue ils ont accès)
Il voit uniquement les informations nécessaires à sa prestation ( date - lieu - horaires, le budget specifique au photographe et le moodboard)

Depuis sa fiche de prestation, il retrouve également le montant convenu, l'acompte déjà versé et le solde restant. Il peut déposer son devis ou sa facture afin de centraliser les documents liés à sa prestation.
Si Ayla modifie l'horaire d'un moment important, la timeline partagée est mise à jour afin que le photographe puisse consulter les dernières informations.


---
### **Persona 3 – Ayla qui organise le mariage de sa cousine**

Depuis son profil, Ayla peut créer un nouveau projet pour sa cousine indépendamment de son projet à elle. Elle invite sa cousine pour lui donner quelque taches à faire sans avoir acces à tt l’admin en complet

Ca permet aussi à l’application de ne pas etre limité aux futurs mariés mais qu’une personne de confiance ou un organisateur peut également créer et gérer un mariage pour quelqu'un d'autre.

---
### **Persona 4 – La cousine d'Ayla qui cède l'admin à Ayla**

Puisque Ayla connait l’application sur les bouts des doigts, sa cousine lui propose de gerer ca en temps qu’admin principale et que elle, elle puisse simplement voir les info auxquelles Ayla lui a donné accès. 
Donc elle se connecte grace à l’invitation d’Ayla et elle a deja qql taches à faire, elle peut aussi voir le moodbaord et y contribuer, elle peut aussi voir la liste des invité 


---

# **3. Fonctionnalités principales**

### **Côté public**

- Présentation du service
- Boutons **Login / Register**
- Mise en avant des avantages et fonctionnalités
- Aperçu du côté admin (mockups / captures / sections résumées)

### **Côté admin**

- creation de compte / connexion / invitation d’un prestataire
- dashboard
- taches
    - CRUD une tâche
        - titre
        - description
        - statut
        - date limite
        - événement associé
    - Acces au prestataire possible
- liste des invités, RSVP
- budget
    - definir un budget total
    - budget par evenement
    - créer des catégories (salle, robe, déco, etc.)
    - acces au prestataire possible
- timeline
- moodboard
- a voir : plan des tables
