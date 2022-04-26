---
author: Adrien
description: Avertissez vos membres de l'arrivée ou du départ de l'un d'entre eux, et souhaitez la bienvenue aux nouveaux venus.
icon: arrow-switch
label: Messages de bienvenue et de départ
order: -4
---

# Messages de bienvenue et de départ

Ce paramètre permet de choisir le message à envoyer lors de l'arrivée ou du départ d'un membre du serveur.

!!! Permissions nécessaires
La modification de ce paramètre nécessite la permission *Gérer le serveur*.
!!!

## Principe
Quand un membre arrive sur votre serveur, celui-ci est accueilli par le message que vous avez choisi dans le salon paramétré au préalable.
Quand un membre quitte le serveur, les autres en sont informés grâce au message que vous avez choisi envoyé dans le salon paramétré au préalable.

!!!
Les deux paramètres sont indépendants ; ainsi, vous pouvez envoyer les messages d'arrivée dans un autre salon que les messages de départ.
!!!

## Paramétrage 
!!!warning
L'usage des commandes suivantes écrase tout paramétrage précédent des messages d'arrivée ou de départ selon le cas.
!!!
### Avec la commande `set`
#### Syntaxe
```
/set [welcome/goodbye] [salon] [message]
```
Utilisez `welcome` pour les messages d'arrivée, `goodbye` pour les messages de départ. `message` peut contenir des balises, le rendant adapté à chaque membre et à chaque changement sur le serveur (nom du serveur...). En voici la liste complète, avec pour exemple l'arrivée (ou le départ) de Wumpus#1234 sur le serveur de Owner#0001 qui s'appelle "Amis de Wumpus" en date du 01/01/2020 à 12h. Les accolades sont obligatoires.

Balise | Description | Exemple
---|---|---
`{member_id}` | Identifiant du membre | 123456789012345
`{member_tag}` | Tag du membre | Wumpus#1234
`{member_username}` | Nom d'utilisateur du membre | Wumpus
`{member_mention}` | Mention du membre (message d'arrivée uniquement) (notifie le membre) | [@Wumpus]() 
`{date}` | Date d'envoi du message | 01/01/2020
`{time}` | Heure d'envoi du message | 12h00
`{server_name}` | Nom du serveur | Amis de Wumpus
`{server_name_initials}` | Initiales du nom du serveur | ADW
`{server_owner_id}` | Identifiant du propriétaire du serveur | 123456789012340
`{server_owner_tag}` | Tag du propriétaire du serveur | Owner#0001
`{server_owner_mention}` | Mention du propriétaire du serveur (ne notifie pas le propriétaire) | [@Owner]() 
`{server_owner_username}` | Nom d'utilisateur du propriétaire du serveur | Owner
`{server_owner_displayname}` | Pseudo sur le serveur du propriétaire du serveur, ou son nom d'utilisateur si non applicable | Owner

#### Retour de la commande en fonctionnement normal
Le bot demande confirmation du paramétrage, puis renvoie `Paramétrage effectué` pour signaler le bon fonctionnement du paramétrage.

#### Erreurs possibles
##### `Vous n'avez pas la permission. (Permission "Gérer le serveur" nécessaire)`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer le serveur*.

##### `Ce salon n'est pas textuel.`
Vérifiez que vous avez bien choisi un salon textuel.

##### `Opération annulée`
Le bot a rencontré un problème. Soit il n'a pas reçu votre confirmation, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).

### Avec la commande `setup`
Le paramétrage par la commande `setup` n'est pas supporté pour l'instant.

## Suppression du paramètre
### Syntaxe
```
/delete [welcome/goodbye]
```

### Retour de la commande en fonctionnement normal
Le bot demande confirmation avant de supprimer le message de bienvenue ou de départ, puis confirme sa suppression.

### Erreurs possibles
#### `Vous n'avez pas la permission. (Permission "Gérer le serveur" nécessaire)`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer le serveur*.

#### `Le message de bienvenue/départ n'est pas paramétré`
Il n'y a rien à supprimer.

#### `Opération annulée.`
Le bot a rencontré un problème. Soit il n'a pas reçu votre confirmation, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).