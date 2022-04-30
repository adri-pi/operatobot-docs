---

label: Paramétrage du bot
icon: gear
order: -10
description: Liste des paramètres personnalisables pour utiliser OperaToBot sur vos serveurs.
---

# Paramétrer le bot

Besoin d'aide pour paramétrer le bot ? Retrouvez ici la liste des paramètres modifiables, ainsi que la documentation des commandes permettant de les modifier.

!!!warning
Attention : toute modification des paramètres avec une des commandes indiquées ci-dessous est immédiate et irréversible.
!!!

## Paramétrer le bot pour la première fois
C'est la première fois que vous utilisez le bot ? Utilisez la commande `/setup` et laissez-vous guider par le bot. Vous pourrez paramétrer chaque fonction du bot une par une.

## Modifier les paramètres du bot
Le premier paramétrage est terminé, ou vous ne souhaitez utiliser que peu de fonctions paramétrables du bot ? Dans ce cas-là, utilisez la commande `/set`. Elle vous permet de modifier une propriété paramétrable à la fois rapidement. Vous pouvez aussi utiliser la commande `/setup` avec le nom du paramètre à modifier pour une expérience interactive.

Vous retrouverez ici la syntaxe utilisée pour chaque paramètre avec la commande `set` ou `setup`.

### Rôles automatiques
``` Avec la commande set
/set autorole [rôle 1] (rôle 2) (rôle 3) (rôle 4) (rôle 5)
```
``` Avec la commande setup
/setup autorole
```
[!ref](autorole.md)

### Modules du bot
``` Avec la commande set
/set modules [activation] [identifiants des modules séparés par une virgule]
```
``` Avec la commande setup
/setup modules
```
[!ref](modules.md)

### BoutonRôle
``` Avec la commande set
/set buttonrole [salon textuel] [rôle] (description) (ajout) (retrait)
```
``` Avec la commande setup
/setup buttonrole
```
[!ref](buttonrole.md)

### Messages d'arrivée et de départ de membres
``` Avec la commande set
/set [welcome/goodbye] [salon] [message]
```
``` Avec la commande setup
/setup (welcome/goodbye)
```
[!ref](messages.md)

### Logs de modération/de paramétrage du bot
``` Avec la commande set
/set [modlogs/setlogs] [salon]
```
``` Avec la commande setup
/setup (modlogs/setlogs)
```
[!ref](logs.md)

## Supprimer des paramètres du bot
Vous souhaitez supprimer certains paramètres que vous avez ajoutés au bot ? Dans ce cas-là, utilisez la commande `delete`. Elle vous permet de supprimer une propriété paramétrable à la fois rapidement. 

Vous retrouverez ici la syntaxe utilisée pour chaque paramètre avec la commande `delete`.

### Rôles automatiques
```
/delete autorole (rôle à supprimer)
```
[!ref](autorole.md)

### Messages d'arrivée et de départ de membres
```
/delete [welcome/goodbye]
```
[!ref](messages.md)

### Logs de modération
```
/delete [modlogs/setlogs]
```
[!ref](logs.md)