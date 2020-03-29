Documentation des bots Elysion
=======
Voici une petite documentation vis-à-vis des bots Elysion réalisés par **DarkScientist_ aka Edward Bestkoder**. Elle est valable uniquement pour ces bots là et est susceptible d'être modifiée.

## Bot de Modération
Vous apprendrez ici à utiliser le bot de Modération **@Elysion Modération#1525**

### Informations de base

|Item|Valeur  |
|--|--|
|Préfixe  |*  |
|Rôle minimum|@Joueur  |

### Durées
Les durées doivent être exprimées d'une certaine manière, voir le tableau ci-dessous :

|Unité|Suffixe  |
|--|--|
|Minutes|m|
|Heures|h|
|Jours|d|

Les secondes ne sont pas disponibles.

La durée sera alors exprimée ainsi : <strong>&lt;durée&gt;&lt;unité&gt;</strong>

Note : <strong>&t;durée&gt;</strong> doit être un nombre entier.

**Exemple** : Si je veux appliquer une durée de trois jours, j'écrirai **3d**.

### Liste des commandes
<strong>&lt;valeur&gt;</strong> = argument requis

<strong>[valeur]</strong> = argument optionnel

|Commande|Fonction  |Arguments|Rôle requis|
|--|--|--|--|
|*getwarns|Permet d'avoir ses derniers warns / voir ceux d'un autre utilisateur|<strong>[@utilisateur]</strong>|@Joueur|
|*warn  |Permet d'avertir un utilisateur  |<strong><@utilisateur> &lt;raison&gt;</strong>|@Modo Test|
|*mute|Permet de rendre muet un utilisateur|<strong><@utilisateur> <durée> &lt;raison&gt;</strong>|@Modo|
|*unmute|Permet d'annuler le mute d'un utilisateur|<strong><@utilisateur></strong>|@Modo
|*tempban|Permet de bannir temporairement un utilisateur|<strong><@utilisateur> <durée> &lt;raison&gt;</strong>|@Responsable Modérateur|
|*unban|Permet de débannir un utilisateur|<strong><identifiant de l'utilisateur>|@Responsable Modérateur|
|*ban|Permet de bannir définitivement un utilisateur|<strong><@utilisateur> <durée> &lt;raison&gt;</strong>|@Responsable Staff|

### Sanctions automatiques
Voici la liste des sanctions automatiques, appliquées par le bot :

|Infraction|Sanctions  |
|--|--|
|Envoi d'invitation discord  |Warn  |
|Mot interdit (cliquez [ici](https://pastebin.com/9YhhHnGt) pour consulter la liste)|Warn|
|Spam de majuscules (plus de 50% du message est écrit en majuscule et le message fait plus de 6 caractères)|Warn|
|5 warns en moins de 5 minutes|Mute de 5 minutes|

### Respect de la hiérarchie et du type de staff
Les sanctions de type **warn** et **ban**/**tempban** sont associées à un grade et à un type de staff. Ainsi, pour débannir un utilisateur, la personne devra avoir un grade supérieur à celui de celle qui a banni cet utilisateur, et doit être du même type de staff (**military**, **basewars**, **darkrp**).

**Par exemple**, une personne bannie par un Responsable Modérateur Military ne pourra être débannie que par un Responsable Modérateur Military, un Responsable Staff Military ou la **main team**.

### Obtenir l'identifiant d'un utilisateur
Il est possible de bannir un utilisateur qui a quitté le discord avec son identifiant, et il est nécessaire de l'avoir pour débannir quelqu'un. Voici comment l'obtenir.

Allez dans vos paramètres Discord puis dans **"Apparence"** :

![settings](https://i.imgur.com/qIvazOQ.png)

![apparance](https://i.imgur.com/tR7G2Qk.png)

Descendez tout en bas et cochez l'option **"Mode développeur"**. Redémarrez ensuite Discord pour que les changements prennent effet.

![dev](https://i.imgur.com/iHbgVkT.png)

Pour avoir l'identifiant d'un utilisateur, faites un clic droit dessus puis cliquez sur **"Copier l'identifiant"**. L'identifiant a alors été copié dans votre presse papier, et vous pouvez l'utiliser dans une commande.

![copier identifiant](https://i.imgur.com/Tzc864Y.png)

### Logs
Toutes les sanctions sont automatiquement renseignées dans le channel [#logs-sanctions](https://discord.gg/uKSqSEp) du Discord. De plus, un message avec les détails de la sanction est envoyé à l'utilisateur sanctionné.

## Bot de gestion de Staff
Vous apprendrez ici à utiliser le bot de Gestion de Staff **@Elysion Staff#8062**

### Informations de base

|Item|Valeur  |
|--|--|
|Préfixe  |?  |
|Rôle minimum|@Responsable Modérateur  |

### Commandes

<strong>&lt;valeur&gt;</strong> = argument requis

<strong>[valeur]</strong> = argument optionnel

|Commande&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Fonction  |Arguments|Rôle requis|
|--|--|--|--|
|?staffpromote|Permet de promote un staff.  |Aucun.|@Responsable Modérateur|
|?demote|Permet de totalement demote un staff.|<strong><@utilisateur></strong>|@Responsable Modérateur|

### La commande "?staffpromote"
La commande **?staffpromote** sert à promouvoir quelqu'un en staff ou à promouvoir un staff. Elle se déroule en plusieurs étapes.

#### 1. Catégorie
Vous devez choisir la catégorie de staff dans laquelle vous voulez promouvoir l'utilisateur. Voici les différentes options : **darkrp**, **militaryrp**, **basewars**. Notez que vous ne pourrez promouvoir un utilisateur dans une catégorie que si vous avez le rôle nécessaire <u>dans la catégorie mentionnée</u>.

#### 2. Utilisateur à promouvoir
Vous devez ensuite mentionner l'utilisateur que vous souhaitez promouvoir. Il doit avoir <u>un rang inférieur au vôtre</u>.

#### 3. Rôle auquel promouvoir l'utilisateur
Vous devez ensuite marquer le nom du rôle auquel l'utilisateur doit être promu.

Voici la liste :

|Nom|Rôle correspondant  |
|--|--|
|MODOTEST  |@Modo Test  |
|MODO|@Modérateur|
|MODOSENIOR|@Modérateur Sénior|
|RESPMODO|@Responsable Modérateur|
|RESPSTAFF|@Responsable Staff|

Notez que vous pouvez promouvoir quelqu'un à un rôle qui est inférieur au vôtre. Ainsi, seuls **Toshiro** et **Diaboloz** peuvent promouvoir des personnes au rôle de Responsable Staff, le plus haut. Vous pouvez rétrogader un staff en mentionnant un rôle inférieur à celui qu'il a actuellement.

### La commande "?demote"
La commande **?demote** permet de rétrogader totalement un staff. Il suffit de mentionner le staff à rétrogader.

### Logs
Tous les promote / demote sont notifiés dans le channel [#logs-promotes](https://discord.gg/PnVDVaJ).
 
## Bot de drops
Vous apprendrez ici à utiliser le bot de Drops **@Elysion Drops#7959**

### Informations de base

|Item|Valeur  |
|--|--|
|Préfixe  |&  |
|Rôle minimum|@Créateur de drops  |

### Commandes

<strong>&lt;valeur&gt;</strong> = argument requis

<strong>[valeur]</strong> = argument optionnel

|Commande|Fonction  |Arguments|Rôle requis|
|--|--|--|--|
|&drop  |Permet de créer un drop  |<strong>add &lt;type&gt; &lt;nombre de réactions&gt; &lt;channel&gt;|@Créateur de drops|

### La commande "&drop"

#### 1. Type
Choisissez le type de contenu à mettre en jeu. Vous avez le choix entre **coupon**, **giftcard**, **steam**, **nitro**.

#### 2. Nombre de réactions
Précisez le nombre de réactions de l'émoji 🎁 à atteindre pour débloquer le contenu. Il doit être un nombre entier.

#### 3. Channel
Précisez le channel où le contenu doit être mis en jeu. Vous avez le choix entre **boost** et **normal** (**boost** étant le channel de drops disponibles aux boosters du serveur Discord).

**Alors, le bot vous posera une série de questions.**

#### 1. Le contenu
Entrez le contenu du drop. Cela peut être un lien **Discord Nitro**, le code d'un **coupon**, d'une **giftcard** ou d'un jeu **Steam**.

#### 2. Plus de précisions...
Entrez alors plus de précisions, selon le tableau ci-dessous :

|Type de contenu|Précision demandée  |
|--|--|
|Nitro  |Type de nitro : **classic** ou **game**  |
|Coupon|Réduction en % (sans préciser l'unité, doit être un nombre entier)|
|Giftcard|Montant de la giftcard en € (sans préciser l'unité, doit être un nombre entier)|
|Steam|Lien du jeu steam. Le lien doit se terminer par une suite de chiffres et ne doit pas comporter le nom du jeu. Par exemple, le lien du jeu Garry's Mod tel qu'on le trouve est [https://store.steampowered.com/app/4000/Garrys_Mod/](https://store.steampowered.com/app/4000/Garrys_Mod/), le lien à entrer est [https://store.steampowered.com/app/4000/](https://store.steampowered.com/app/4000/). **Ceci est très important, sans quoi le drop ne marchera pas !**|

**Note** : pour les drops de type Steam, vous pouvez obtenir une erreur comme quoi l'URL est invalide. Vérifiez qu'il n'y a aucun espace à la fin et réessayez autant de fois que nécessaire (souvent une ou deux fois en cas de bug).

**Note** : Même si le contenu du drop est supprimé du channel par sécurité, veuillez effectuer vos commandes dans [#créateur-de-drop](https://discord.gg/FatUsqe).

### Débloquer et récupérer le drop
Pour débloquer le drop, il suffit de réagir à l'émoji 🎁 qui apparaît  sous le message. Vous avez quelques informations sur le message du drop, comme le jeu mis en jeu si le contenu est un jeu steam, le type de nitro mis en jeu, la réduction du coupon ou encore le montant de la carte cadeau mise en jeu.

Pour récupérer le nitro, il suffit de cliquer sur le lien.

Pour récupérer le coupon ou la carte cadeau, allez sur [la boutique](https://boutique.elysionrp.fr), puis une fois vos achats faits allez dans votre panier. Rentrez le code dans le champ prévu à cet effet et cliquez sur **"Echanger"**.

![echanger](https://i.imgur.com/cTnuaGy.png)

> Markdown edité avec [StackEdit](https://stackedit.io/), documentation générée par [Flatdocs](https://ricostacruz.com/flatdoc/), écrite par **DarkScientist_**.
