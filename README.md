# **Cahier des charges : Application web de planification d’événements liés aux mariage**

<aside>
⭐

champs lexical :

- kiz isteme (littéralement : demander la fille ) = la famille de l’homme vient chez la famille de la fille pour demander la main de la fille , les fiançailles se font à ce moment là
- soirée du henné = soirée/fete traditionnel entre filles où on met de l’henné
- mariage
- evenements
- RSPV = réponse d’un invité à une invitation ( si oui ou non vous venez)
</aside>

# **1. Contexte**

En discutant avec ma meilleure amie qui est entrain de penser à son mariage (+ celle de sa cousine l’année d’apres), elle m’a confié avoir beaucoup de difficultés à s’organiser ( un tableau excel pour les invités, pinterest ou tiktok pour les inspi, les prestatires etc etc)et cette complexité est bien marquée dans sa culture turque mais aussi dans d’autres cultures où le mariage ne se limite pas à une seule journée.

Dans son cas, t**rois événements distincts (kiz isteme , soirée du henné, mariage)**

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

### **Persona 2 – Prestataire externe**

Le prestataire n’a pas besoin d’avoir acces à toutes les pages, il veut simplement les info qui concernent sa prestation sans devoir rechercher dans des dizaines de messages. 

Le prestaire peut se connecter à son espace grace à l’invitation envoyé par Ayla, il tombe nez à nez sur un dashbaord adapté à son role

Il peut directement voir :

- le statut de sa prestation
- les événements auxquels il participe(date, heure, lieu)
- le montant convenu et le statut du paiement ou de l’acompte
- la timeline de l’événement afin de savoir à quel moment sa présence est nécessaire

Le prestataire peut aussi avoir acces au moodboard si Ayla le souahite pour qu’il voit un peu l’ambiance qu’Ayla attends

---

# **3. Fonctionnalités principales**

### **Côté public**

- Présentation du service
- Boutons **Login / Register**
- Mise en avant des avantages et fonctionnalités
- Aperçu du côté admin (mockups / captures / sections résumées)

### **Côté admin**

- creation de compte / connexion / invitation d’un prestatire
- dashboard
- taches
    - CRUD une tâche
        - titre
        - description
        - statut (TODO / IN_PROGRESS / DONE)
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
