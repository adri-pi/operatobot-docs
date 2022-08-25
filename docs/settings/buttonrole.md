---

description: Laissez les membres gérer certains de leurs rôles grâce à des boutons.
icon: people
label: BoutonRôle
order: -2
---

# Attribution de rôles par boutons
Ce paramètre permet de créer un message dans un salon choisi, comportant des boutons, et où les membres peuvent choisir de s'attribuer des rôles préalablement paramétrés.

!!! Permissions nécessaires
La modification de ce paramètre nécessite la permission *Gérer les rôles*, et un rôle plus élevé que ceux à paramétrer (sauf si vous êtes le propriétaire du serveur). Il faut aussi que le rôle du bot soit situé au dessus des rôles à paramétrer.
!!!

## Principe
Quand un membre souhaite s'attribuer ou se retirer un rôle parmi ceux que vous avez choisis, il se rend sur le salon du BoutonRôle, et interagit avec les boutons afin de gérer ses rôles.

!!!
Vous pouvez paramétrer l'attribution de jusqu'à 25 rôles par message (1 par bouton).
!!!

!!!danger
Le bot **ne vérifie pas** que les rôles attribués n'ont pas, par exemple, la permission *Administrateur*. Vérifiez donc que les rôles que vous souhaitez paramétrer n'aient pas de permissions sensibles.
!!!

## Paramétrage 

### Avec la commande `set`
!!!warning
Avec cette commande, vous ne pourrez paramétrer qu'un seul rôle par message à cause de sa syntaxe. Pour avoir plusieurs rôles par message, utilisez la commande `setup`, décrite plus bas sur cette page.
!!!

#### Syntaxe
```
/set buttonrole [salon textuel] [rôle] (description) (ajout) (retrait)
```
La `description` sera ajoutée dans le message envoyé. `ajout` permet de choisir si le rôle doit être ajouté ou non au clic sur le bouton si le membre n'a pas le rôle (oui par défaut) ; `retrait` permet de choisir si le rôle doit être retiré ou non au clic sur le bouton si le membre a le rôle (oui par défaut).
#### Retour de la commande en fonctionnement normal
Le bot envoie le message avec le bouton dans le salon choisi, puis renvoie `Le bouton a été ajouté avec succès !` pour signaler le bon fonctionnement du paramétrage.

#### Erreurs possibles
##### `Vous n'avez pas la permission. (Permission "Gérer les rôles" nécessaire)`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer les rôles*.

##### `Le salon doit être un salon textuel.`
Vérifiez que vous avez bien choisi un salon textuel.

##### `Ce rôle ne peut être géré par le bot. Vérifiez qu'il est bien positionné dans la hiérarchie des rôles.`
Le rôle le plus élevé du bot est trop bas par rapport à celui que vous souhaitez paramétrer, ou le bot n'a pas les permissions nécessaires.

##### `Vous ne pouvez pas gérer ce rôle.`
Votre rôle le plus élevé est trop bas par rapport à celui que vous souhaitez paramétrer.

##### `Une erreur s'est produite : veuillez vérifier les arguments de la commande avant de réessayer. Si le problème persiste, rejoignez le serveur de support.`
Le bot a rencontré une erreur interne au serveur ; si cela se reproduit, contactez le [support](/support.md).

### Avec la commande `setup`
#### Syntaxe 
```
/setup (buttonrole)
```

#### Retour de la commande en fonctionnement normal
Arrivé au paramétrage du BoutonRôle, le bot vous propose de choisir le salon, puis chaque rôle avec leurs options possibles. Ensuite, vous pouvez choisir d'ajouter une description personnalisée. A la fin, il envoie le message avec les boutons ainsi qu'un message de confirmation.

#### Erreurs possibles
##### `Vous n'avez pas la permission.`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer les rôles*.

##### `Vous n'avez pas la possibilité de gérer de rôle.`
Vérifiez que les rôles du serveur à paramétrer sont bien en dessous de votre rôle le plus élevé, ainsi que celui du bot.

##### `Opération annulée`
Le bot a rencontré un problème. Soit il n'a pas reçu votre réponse, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).

## Suppression du paramètre
Il vous suffit de supprimer le message concerné. Il n'est pas possible de supprimer les boutons un par un avec le bot.