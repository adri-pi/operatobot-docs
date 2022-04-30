---

description: Enregistrez les activités les plus importantes du serveur, telles que les modifications de paramètres du bot ou les actes de modération.
icon: note
label: Logs
order: -3
---

# Logs de modération et de paramétrage

Ce paramètre permet de choisir les salons où envoyer les logs, messages résumant l'activité relative au bot sur le serveur. Il en existe deux types : les logs de modération et les logs de paramétrage.

!!! Permissions nécessaires
La modification de ce paramètre nécessite la permission *Gérer le serveur*.
!!!

## Principe
### Logs de modération
Quand un acte de modération est effectué avec le bot, celui-ci envoie un message dans le salon choisi, avec les caractéristiques de cet acte : type (bannissement, exclusion...), membres concernés (modérateur et sanctionné), date...

!!!
Les deux paramètres sont indépendants ; ainsi, vous pouvez envoyer les logs de modération dans un autre salon que les logs de paramétrage.
!!!

### Logs de paramétrage
Quand une modification de paramètre du bot est effectuée, celui-ci envoie un message dans le salon choisi, avec le nom du paramètre et les modifications apportées à celui-ci.

## Paramétrage 
!!!warning
L'usage des commandes suivantes écrase tout paramétrage précédent des salons de log.
!!!
### Avec la commande `set`
#### Syntaxe
``` Logs de modération
/set modlogs [salon]
```

``` Logs de paramétrage du bot
/set setlogs [salon]
```
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
#### Syntaxe 
```
/setup (setlogs/modlogs)
```

#### Retour de la commande en fonctionnement normal
Arrivé au paramétrage des logs, le bot vous propose de choisir le salon de log. Après votre choix, il envoie une confirmation du bon paramétrage.

#### Erreurs possibles
##### `Vous n'avez pas la permission.`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer le serveur*.

##### `Opération annulée`
Le bot a rencontré un problème. Soit il n'a pas reçu votre réponse, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).

## Suppression du paramètre
### Syntaxe
```
/delete [modlogs/setlogs]
```

### Retour de la commande en fonctionnement normal
Le bot demande confirmation avant de supprimer le paramètre indiqué. Il renvoie ensuite un message de confirmation de suppression du paramètre.

### Erreurs possibles
#### `Vous n'avez pas la permission. (Permission "Gérer le serveur" nécessaire)`
Vérifiez vos permissions : la modification de ce paramètre nécessite la permission *Gérer les rôles*.

#### `Le salon pour les logs de modération/de paramétrage du bot n'est pas paramétré.`
Aucun salon n'est paramétré pour les logs indiqués.

#### `Opération annulée.`
Le bot a rencontré un problème. Soit il n'a pas reçu votre confirmation, soit il a rencontré une erreur interne au serveur ; dans le deuxième cas, contactez le [support](/support.md).