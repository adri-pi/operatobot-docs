---

description: Liste des commandes OperaToBot
icon: list-unordered
label: Commandes
order: 0
---

# Liste des commandes
OperaToBot embarque **de nombreuses commandes** ; la plupart d'entre elles sont des **commandes slash** [!badge SLASH], mais il existe aussi des commandes apparaissant dans les **menus contextuels utilisateur** [!badge variant="secondary" text="USER"].

## Administration
[!ref](/docs/settings/index.md)
!!!warning Permissions nécessaires
Des permissions sont demandées pour les commandes de cette catégorie, et diffèrent suivant la commande et le paramètre modifié s'il s'agit de `delete`, `set` ou `setup`. Consultez la documentation du paramètre concerné pour en savoir plus.
!!!

### `delete` [!badge SLASH]
Supprime un paramètre du bot.
```
/delete [nom du paramètre] (...)
```

### `say` [!badge SLASH]
Fait parler le bot dans le salon où la commande est effectuée.
```
/say [texte]
```

### `set` [!badge SLASH]
Modifie un paramètre du bot.
```
/set [nom du paramètre] [...]
```

### `setup` [!badge SLASH]
Accéder à l'assistant de paramétrage d'OperaToBot.
```
/setup (nom du paramètre)
```

## OperaToBank
[!ref](bank.md)
!!!
Les commandes listées dans cette catégorie nécessitent un compte OperaToBank, à l'exception de `bank`.
!!!
### `bank` [!badge SLASH] [!badge variant="secondary" text="USER"]
Créer ou consulter l'état d'un compte OperaToBank.
!!!
Pour consulter l'état d'un compte d'un autre utilisateur, celui-ci doit avoir un compte OperaToBank.
!!!
#### Commande slash
```
/bank (utilisateur)
```
L'option `utilisateur` n'est à utiliser que pour consulter l'état d'un compte d'un autre utilisateur.
#### Commande utilisateur
Apparaît dans le menu contextuel de clic droit sur un utilisateur sous le nom *Compte OperaToBank*.

### `buy` [!badge SLASH]
Effectuer un achat sur le magasin OperaToShop.
```
/buy [item]
```

### `give` [!badge SLASH]
Faire un don d'OperaToCoins à un autre utilisateur.
!!!
L'autre utilisateur doit également avoir un compte OperaToBank.
!!!
```
/give [utilisateur] [montant]
```

### `inventory` [!badge SLASH]
Consulter son inventaire. Sélectionner `hide` permet de cacher le résultat aux yeux des autres utilisateurs.
```
/inventory (hide)
```

### `rob` [!badge SLASH]
!!!
L'utilisateur cible doit également avoir un compte OperaToBank.
!!!
Voler un autre utilisateur.

Apparaît dans le menu contextuel de clic droit sur un utilisateur sous le nom *Dérober*.

### `shop` [!badge SLASH]
Affiche la liste des items disponibles à l'achat sur OperaToShop.
```
/shop
```

### `top` [!badge SLASH]
Affiche le classement des plus riches du système OperaToBank.
```
/top
```

### `work` [!badge SLASH]
Travailler afin de gagner quelques OperaToCoins.
```
/work
```

## Bot
### `changelog` [!badge SLASH]
Affiche les modifications apportées au bot lors d'une mise à jour (la dernière par défaut).
```
/changelog (version)
```

### `help` [!badge SLASH]
Affiche la liste des commandes ou comment utiliser l'une d'entre elles.
```
/help (commande)
```

### `modules` [!badge SLASH]
Liste les modules du bot.
```
/modules
```

### `ping` [!badge SLASH]
Renvoie le temps de latence du bot.
```
/ping
```

### `status` [!badge SLASH]
Affiche le statut des services OperaToBot.
```
/status
```

## Fun & jeux
[!ref](games.md)
### `8ball` [!badge SLASH]
Répond par oui ou non de manière aléatoire à une question.
```
/8ball [question]
```

### `allumettes` [!badge SLASH]
Jouer au jeu des allumettes face à un autre utilisateur.
```
/8ball [membre] (nombre d'allumettes) 
```

### `bet` [!badge SLASH]
!!!
Nécessite un compte OperaToBank.
!!!
Parier sur le résultat d'un lancer de dé.
```
/bet [montant] [chiffre]
```

### `choose` [!badge SLASH]
Laisse le bot faire un choix parmi les différentes propositions.
```
/choose [choix (séparées par /)]
```

### `die` [!badge SLASH]
Lance un dé à $n$ faces, $n$ étant un entier strictement positif ($n=6$ par défaut).
```
/die [n]
```

### `meme` [!badge SLASH]
Affiche un meme pris au hasard sur [imgur](https://imgur.com)
```
/meme
```

### `moneysweeper` [!badge SLASH]
!!!
Nécessite un compte OperaToBank.
!!!
Jouer au MoneySweeper.
```
/moneysweeper
```

### `rps` [!badge SLASH]
Jouer à pierre-feuille-ciseaux contre le bot
```
/rps [rock/paper/scissors]
```

## Images
[!ref](pics.md)
### `giphy` [!badge SLASH]
Recherche des GIF sur [giphy](https://giphy.com)
```
/giphy [mots-clés]
```

### `imgur` [!badge SLASH]
Recherche des images sur [imgur](https://imgur.com)
```
/imgur [mots-clés]
```

## Informations
### `serverinfo` [!badge SLASH]
Informations et statistiques sur le serveur.
```
/serverinfo
```

### `userstats` [!badge variant="secondary" text="USER"]
Informations sur un utilisateur.

Apparaît dans le menu contextuel de clic droit sur un utilisateur sous le nom *Statistiques*.

## Modération
[!ref](moderation.md)
!!!warning Permissions nécessaires
Des permissions sont demandées pour les commandes de cette catégorie, et diffèrent suivant la commande. Consultez la page [Modération](moderation.md) pour en savoir plus.
!!!
### `ban` [!badge SLASH]
Bannit un membre du serveur en lui envoyant une notification
```
/ban [membre] (raison)
```

### `hardban` [!badge SLASH]
Bannit un utilisateur n'étant pas sur le serveur, grâce à son [identifiant](https://support.discord.com/hc/fr/articles/206346498-O%C3%B9-trouver-l-ID-de-mon-compte-utilisateur-serveur-message-).
```
/hardban [identifiant] (raison)
```

### `kick` [!badge SLASH]
Expulse un membre du serveur et lui envoie une notification.
```
/kick [membre] (raison)
```

### `mute` [!badge SLASH]
Rend un membre [muet](https://support.discord.com/hc/fr/articles/4413305239191-Time-Out-FAQ)
```
/mute [membre] (raison) (nombre de jours) (nombre d'heures) (nombre de minutes)
```

### `purge` [!badge SLASH]
Supprimer des messages (de moins de 15 jours) en masse dans le salon où est effectuée la commande.
!!!danger
Si le nombre de messages indiqués est strictement supérieur au nombre de messages effectivement envoyés dans le salon, un comportement inattendu peut se produire : des messages envoyés ultérieurement à la commande pourraient être supprimés. Soyez donc attentif au nombre indiqué.
!!!
```
/purge [nombre de messages à supprimer]
```

### `unmute` [!badge SLASH]
Retire le statut muet d'un membre.
```
/unmute [membre] (raison)
```

### `warn` [!badge SLASH]
Gérer les avertissements d'un membre
``` Ajout d'un avertissement
/warn add [membre] [raison]
```
``` Retrait d'un avertissement
/warn remove [membre] [numéro de l'avertissement]
```
``` Retrait de tous les avertissements
/warn add [membre]
```
``` Liste des avertissements
/warn list [membre]
```