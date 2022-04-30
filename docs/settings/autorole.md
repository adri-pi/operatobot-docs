---

description: Ajoutez des rôles automatiquement à tous les nouveaux arrivants de votre serveur.
icon: person-add
label: Rôles automatiques
order: -1
---

# Attribution automatiques de rôles aux nouveaux membres

Ce paramètre permet de choisir les rôles à attribuer automatiquement avec le bot aux nouveaux arrivants sur le serveur.

!!! Permissions nécessaires
La modification de ce paramètre nécessite la permission *Gérer les rôles*, et un rôle plus élevé que ceux à paramétrer (sauf si vous êtes le propriétaire du serveur). Il faut aussi que le rôle du bot soit situé au dessus des rôles à paramétrer.
!!!

## Principe
Quand un membre arrive sur votre serveur, celui-ci se voit automatiquement attribuer les rôles que vous avez choisis.

!!!
Vous pouvez paramétrer l'attribution de jusqu'à 5 rôles par serveur.
!!!

!!!danger
Le bot **ne vérifie pas** que les rôles attribués n'ont pas, par exemple, la permission *Administrateur*. Vérifiez donc que les rôles que vous souhaitez paramétrer n'aient pas de permissions sensibles.
!!!

## Paramétrage 
!!!warning
L'usage des commandes suivantes écrase tout paramétrage précédent des rôles automatiques.
!!!
### Avec la commande `set`
#### Syntaxe
```
/set autorole [rôle 1] (rôle 2) (rôle 3) (rôle 4) (rôle 5)
```
#### Retour de la commande en fonctionnement normal
Le bot demande confirmation du paramétrage, puis renvoie `Paramétrage effectué` pour signaler le bon fonctionnement du paramétrage.

#### Erreurs possibles
##### `Vous n'avez pas la permission. (Permission "Gérer les rôles" nécessaire)`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer les rôles*.

##### `Vous n'avez aucune permission sur les rôles renseignés, opération annulée.`
Vérifiez que les rôles que vous souhaitez paramétrer sont bien en dessous de votre rôle le plus élevé, ainsi que celui du bot.

##### `Sur les x rôles renseignés, seuls y rôles peuvent être ajoutés. Souhaitez-vous continuer ?`
Certains rôles ne peuvent être attribués à cause d'un problème de permissions, mais le bot vous propose de paramétrer ceux qui ne sont pas concernés. 

##### `Opération annulée`
Le bot a rencontré un problème. Soit il n'a pas reçu votre confirmation, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).

### Avec la commande `setup`
#### Syntaxe 
```
/setup (autorole)
```

#### Retour de la commande en fonctionnement normal
Arrivé au paramétrage du rôle automatique, le bot vérifie que vous souhaitez bien écraser le paramétrage précédent s'il existe. Il vous propose ensuite une liste de rôles à paramétrer, puis demande confirmation. Une fois le paramétrage effectué, il renvoie `x rôles ont bien été paramétrés pour l'autorôle`, suivi de la liste des rôles.

#### Erreurs possibles
##### `Vous n'avez pas la permission.`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer les rôles*.

##### `Vous n'avez pas la possibilité de gérer de rôle.`
Vérifiez que les rôles du serveur à paramétrer sont bien en dessous de votre rôle le plus élevé, ainsi que celui du bot.

##### `Opération annulée`
Le bot a rencontré un problème. Soit il n'a pas reçu votre confirmation, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).

## Suppression du paramètre
### Syntaxe
```
/delete autorole (rôle à supprimer)
```

### Retour de la commande en fonctionnement normal
Le bot demande confirmation avant de supprimer le rôle indiqué, ou tous si aucun n'est précisé. Il renvoie ensuite un message de confirmation de suppression du paramètre.

### Erreurs possibles
#### `Vous n'avez pas la permission. (Permission "Gérer les rôles" nécessaire)`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer les rôles*.

#### `Aucun rôle n'est paramétré.` ou `Ce rôle n'est pas paramétré`
Aucun rôle n'est paramétré, ou le rôle choisi n'est pas paramétré comme rôle automatique.

#### `Opération annulée.`
Le bot a rencontré un problème. Soit il n'a pas reçu votre confirmation, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).