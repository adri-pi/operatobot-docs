---
author: Adrien
description: Activez ou désactivez les fonctionnalités d'OperaToBot.
icon: multi-select
label: Modules OperaToBot
order: -5
---

# Modules OperaToBot

Ce paramètre permet de choisir les modules de commande à activer sur votre serveur.

!!! Permissions nécessaires
La modification de ce paramètre nécessite la permission *Gérer le serveur*.
!!!

## Principe
Lorsqu'une commande est utilisée sur votre serveur, si le module dont elle fait partie est désactivé, celle-ci n'enclenchera aucune action de la part du bot.

!!!
Certains modules ne peuvent être désactivés, car sont absolument nécessaires au bon fonctionnement du bot. C'est le cas du module *Administration*, contenant les commandes de paramétrage comme `set`.

## Paramétrage 
### Avec la commande `set`
#### Syntaxe
```
/set modules [activation] [modules]
```
`activation` est un booléen, vous permettant d'indiquer si le bot doit activer ou non les modules choisis. `modules` doit contenir la liste des identifiants de module, séparés par une virgule. 
Vous trouverez la liste des modules avec leurs identifiants et leur statut en utilisant la commande `/modules`.

#### Retour de la commande en fonctionnement normal
Le bot demande confirmation du paramétrage, puis renvoie `Paramétrage effectué` pour signaler le bon fonctionnement du paramétrage.

#### Erreurs possibles
##### `Vous n'avez pas la permission. (Permission "Gérer le serveur" nécessaire)`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer le serveur*.

##### `Les modules renseignés ne sont pas valides : soit leur identifiant n'est pas correct, soit ils ne peuvent être désactivés. Consultez la documentation pour plus d'informations.`
Vérifiez que vous avez bien recopié l'identifiant et non le nom des modules à (dés)activer, et que ceux-ci ne font pas partie des modules non paramétrables (comme indiqué ci-dessus).

##### `Opération annulée`
Le bot a rencontré un problème. Soit il n'a pas reçu votre confirmation, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).

### Avec la commande `setup`
#### Syntaxe 
```
/setup (modules)
```

#### Retour de la commande en fonctionnement normal
Arrivé au paramétrage des modules, le bot affiche la liste des modules désactivables sous forme de boutons, à cocher selon le statut que vous souhaitez leur donner. Le statut du bouton affiche l'état actuel du module. Validez pour confirmer les changements.

#### Erreurs possibles
##### `Vous n'avez pas la permission.`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer le serveur*.

##### `Opération annulée`
Le bot a rencontré un problème. Soit il n'a pas reçu votre confirmation, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).