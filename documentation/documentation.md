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

La durée sera alors exprimée ainsi : <strong>[durée][unité]</strong>

Note : <strong>[durée]</strong> doit être un nombre entier.

**Exemple** : Si je veux appliquer une durée de trois jours, j'écrirai **3d**.

### Liste des commandes
<strong>&lt;valeur&gt;</strong> = argument optionnel

<strong>[valeur]</strong> = argument requis

|Commande|Fonction  |Arguments|Rôle requis|
|--|--|--|--|
|*getwarns|Permet d'avoir ses derniers warns / voir ceux d'un autre utilisateur|<strong><@utilisateur></strong>|@Joueur|
|*warn  |Permet d'avertir un utilisateur  |<strong>[@utilisateur] [raison]</strong>|@Modo Test|
|*mute|Permet de rendre muet un utilisateur|<strong>[@utilisateur] [durée] [raison]</strong>|@Modo|
|*unmute|Permet d'annuler le mute d'un utilisateur|<strong>[@utilisateur]</strong>|@Modo
|*tempban|Permet de bannir temporairement un utilisateur|<strong>[@utilisateur][durée][raison]</strong>|@Responsable Modérateur|
|*unban|Permet de débannir un utilisateur|<strong>[identifiant de l'utilisateur]|@Responsable Modérateur|
|*ban|Permet de bannir définitivement un utilisateur|<strong>[@utilisateur] [durée] [raison]</strong>|@Responsable Staff|

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

### Logs
Toutes les sanctions sont automatiquement renseignées dans le channel [#logs-sanctions](https://discord.gg/uKSqSEp) du Discord.

## Bot de gestion de Staff
Vous apprendrez ici à utiliser le bot de Gestion de Staff **@Elysion Staff#8062**

### Informations de base

|Item|Valeur  |
|--|--|
|Préfixe  |?  |
|Rôle minimum|@Responsable Modérateur  |

### Commandes

<strong>&lt;valeur&gt;</strong> = argument optionnel

<strong>[valeur]</strong> = argument requis

|Commande|Fonction  |Arguments|Rôle requis|
|--|--|--|--|
|?staffpromote  |Permet de promote un staff.  |Aucun.|@Responsable Modérateur|
|?demote|Permet de totalement demote un staff.|<strong><@utilisateur></strong>|@Responsable Modérateur|

### La commande "?staffpromote"


> Markdown edité avec [StackEdit](https://stackedit.io/), documentation générée par [Flatdocs](https://ricostacruz.com/flatdoc/), écrite par **DarkScientist_**.
