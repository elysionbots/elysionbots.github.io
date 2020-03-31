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
Pour débloquer le drop, il suffit de réagir à l'émoji 🎁 qui apparaît  sous le message. Vous avez quelques informations sur le message du drop, comme le jeu proposé si le contenu est un jeu Steam, le type de nitro mis en jeu, la réduction du coupon ou encore le montant de la carte cadeau mise en jeu.

Pour récupérer le nitro, il suffit de cliquer sur le lien.

Pour récupérer le coupon ou la carte cadeau, allez sur [la boutique](https://boutique.elysionrp.fr), puis une fois vos achats faits allez dans votre panier. Rentrez le code dans le champ prévu à cet effet et cliquez sur **"Echanger"**.

![echanger](https://i.imgur.com/cTnuaGy.png)

Pour récupérer une clé Steam, il faut avoir l'application de bureau Steam (c'est à dire le logiciel installé sur votre ordinateur). Une fois sur cette dernière, cliquez en haut sur l'onglet **"Jeux"** puis sur **"Activer un produit sur Steam"** dans la liste déroulante.

![jeux](https://i.imgur.com/Wfesb15.png)

Ensuite, dans la fenêtre qui s'ouvre, cliquez sur **"Suivant"**, **"Je suis d'accord"** puis rentrez la clé Steam obtenue et cliquez sur **"Suivant"**. Confirmez que vous voulez récupérer le jeu, et c'est bon !

![code](https://i.imgur.com/VBoxETH.png)

### Notes
Si il est marqué que le jeu Steam est dupliqué, que le Nitro a été récupéré ou encore qu'il ne reste que quelques centimes sur une giftcard par exemple, c'est que le lot en question a déjà été utilisé. Tout ce qui est mis en jeu est valide.

## Être notifié des drops
Vous pouvez décider d'être notifié lors des drops ! <br>
Dès lors,, il vous suffit de vous rendre dans le channel [#➕roles](https://discord.gg/wtrefNM) et de réagir au message, ou bien de cliquer sur l'émoji **"Follow"** en dessous d'un drop <u>actif</u>.

![follow](https://cdn.discordapp.com/emojis/691275755136614451.png?v=1)

## Bot de Tickets
Vous apprendrez ici à utiliser le bot de Gestion de Staff **@Elysion Tickets#3240**

### Informations de base

|Item|Valeur  |
|--|--|
|Préfixe  |+  |
|Rôle minimum|@Joueur  |

### Commandes

<strong>&lt;valeur&gt;</strong> = argument requis

<strong>[valeur]</strong> = argument optionnel

|Commande&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Fonction  |Arguments|Rôle requis|
|--|--|--|--|
|+new|Permet de créer un ticket |<strong>&lt;type&gt; &lt;raison&gt;</strong>|@Joueur|
|+close|Permet de fermer un ticket|<strong>[raison]</strong>|@Joueur|
|+rename|Permet de renommer un ticket|<strong>&lt;nouveau nom&gt;</strong>|@Modo test|
|+reponse|Permet d'envoyer une réponse prédéfinie|<strong>&lt;nom de la réponse&gt;</strong>|@Modo Test|

**Note :** Toutes les commandes excepté **+new** sont à effectuer dans un ticket.

### La commande "+new"
La commande **"+new"** permet de créer un ticket. Elle prend deux arguments. Le premier, c'est le type de serveur pour lequel vous souhaitez ouvrir un ticket : vous avez le choix entre **darkrp**, **military** ou **basewars**. Ensuite, spécifiez la raison.

**Exemple :** je veux ouvrir un ticket DarkRP pour une question RP, je tape **"+new darkrp j'ai une question RP"**. 

Un message vous est alors renvoyé avec le nom du channel, et le ticket apparaît dans vos channels Discord.

### Fermer un ticket
Pour fermer un ticket, vous avez le choix entre réagir sous le message du bot en haut du channel avec l'émoji 🔒, ou bien tapez la commande **"+close &lt;raison&gt;"**.

### Réponses prédéfinies
Le staff a accès à la commande **"+reponse"** qui permet de renvoyer une réponse prédéfinie.

Voici la liste des réponses disponibles, avec leur nom, qui est à ajouter à la suite de la commande :

|Nom|Contenu  |
|--|--|
|ddd  |https://pastebin.com/7dJQTgv5  |
|ddb|https://pastebin.com/pErNckdt|
|remboursement|https://pastebin.com/8B6UEiyc|
|error|https://pastebin.com/W0Y8kfhD|
|boutique|https://pastebin.com/yLBX5JEx|
|plaintes|https://pastebin.com/e21ZcFf7|
|staff|https://pastebin.com/b4xnpZiN|

La liste précédente est également proposée lorsque vous n'ajoutez pas d'arguments à la commande.

**Exemple :** Je veux renvoyer la réponse concernant les remboursements, je tape **"+reponse remboursement"**.

### Logs
Les channels de logs sont : 

|Type de serveur|Channel  |
|--|--|
|DarkRp  |[#logs-tickets-darkrp](https://discord.gg/x89BzjE)  |
|Military|[#logs-tickets-military](https://discord.gg/PguEhx2)|
|Basewars|[#logs-tickets-basewars](https://discord.gg/78vbrtu)|

## Bot de Levels & IQ
Enfin, ici vous apprendrez à utiliser le bot **@MODO PARFAIT#0652**.

### Informations de base

|Item|Valeur  |
|--|--|
|Préfixe  |!  |
|Rôle minimum|@Joueur  |

### Commandes

<strong>&lt;valeur&gt;</strong> = argument requis

<strong>[valeur]</strong> = argument optionnel

|Commande&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Fonction  |Arguments|Rôle requis|
|--|--|--|--|
|!leaderboard|Permet de voir le classement des levels|Aucun.|@Joueur|
|!iqboard|Permet de voir le classement des IQs|Aucun.|@Joueur|
|!trade|Permet d'envoyer des IQs à quelqu'un|<strong>&lt;@utilisateur&gt; &lt;nombre d'IQ à envoyer&gt;</strong>|@Joueur|
|!rank|Permet de voir la carte de profil d'un membre (ou la sienne si aucun membre n'est mentionné)|<strong>[@utilisateur]</strong>|@Joueur|
|!clean|Permet de supprimer x messages|<strong>&lt;nombre de messages à supprimer&gt;</strong> <u>(doit être inférieur à 100)</u>|@Admin discord|
|!setxp|Permet de définir l'XP d'un member|<strong>&lt;@utilisateur&gt; &lt;nombre d'XP&gt;|@Admin discord|
|!setlevel|Permet de définir le niveau d'un membre|<strong>&lt;@utilisateur&gt; &lt;nombre de levels&gt;|@Admin discord|
|!setiq|Permet de définir l'IQ d'un membre|<strong>&lt;@utilisateur&gt; &lt;nombre d'IQ&gt;|@Admin discord|

### XP, Levels & IQ
Vous gagnez 5 XP par message envoyé sur le serveur ou réaction ajoutée dans les canaux RP. Au bout d'un certain nombre d'XP, défini selon votre niveau, vous gagnez un niveau, le *level*. Le nombre d'XP à avoir augmente de **20%** à chaque level.

Au bout de 50 niveaux, vous gagnez un rôle de <u>Membre Actif</u>, et avez une couleur différente ainsi qu'un accès à un channel privé de drops.

Quant à l'IQ, il est donné lorsque vous invitez quelqu'un (mais se retire si la personne part). Il donnera par la suite accès à des récompenses.

Toutes les données énoncées ci-dessus sont accessibles sur la carte donnée par la commande **!rank** :

![rank](https://cdn.discordapp.com/attachments/612016126838177870/694503987654950952/rank.png)

Pour l'instant, le membre avec le *level* le plus élevé est **Martin Favre**, au niveau 18 :

![favre](https://cdn.discordapp.com/attachments/612016126838177870/694504236075188275/rank.png)


## Lier son grade IG à Discord
Cette fonctionnalité arrive d'ici quelques jours, vous serez averti lorsqu'elle sera mise en place. Elle sera automatisée.

## En cas de problème...
En cas de problème, contactez **@DarkScientist_#9449** sur Discord ou ouvre un ticket.
> Markdown edité avec [StackEdit](https://stackedit.io/), documentation générée par [Flatdocs](https://ricostacruz.com/flatdoc/), écrite par **DarkScientist_**.
