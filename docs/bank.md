---

description: Rejoignez le système économique OperaToBank !
icon: squirrel
label: OperaToBank
order: -3
---

# OperaToBank

!!!danger Fermeture du service OperaToBot
Le service OperaToBot cessera de fonctionner définitivement le 31 juillet 2024. [En savoir plus.](/shutdown.md)
!!!

OperaToBank, c'est un système économique global, propre au bot qui vous permettra de gagner des OperaToCoins (monnaie du système, symbole OTC) et de les échanger !

!!!danger DISCLAIMER
**Aucune transaction impliquant de l'argent réel ne sera effectuée avec ce système. Le terme "Argent" désigne ici les OperaToCoins, monnaie fictive non utilisable en dehors du bot.** Notamment, il ne s'agit en aucun cas d'une cryptomonnaie.
!!!

## Créer un compte OperaToBank
``` 
/bank
```

## Bonus
A la création de votre compte, vous recevrez différents bonus, que vous recevrez aussi si vous effectuez les actions relatives après la création du compte.
- **Création du compte** : 100 OTC
- **Avoir invité le bot sur son serveur** : nombre de membre sur le serveur en question multiplié par 10 OTC
!!!
Il est inutile de réinviter le bot plusieurs fois sur le même serveur, vous n'obtiendrez pas plus de bonus !
!!!
- **Être sur le serveur de support** : 100 OTC
!!! 
Il est inutile de rejoindre plusieurs fois le serveur de support, vous n'obtiendrez pas plus de bonus !
!!!

## Voir l'état d'un compte OperaToBank
``` Pour soi-même
/bank
```
``` Pour un autre membre
/bank [membre]
```
Vous pouvez également faire un clic droit sur l'utilisateur dont vous souhaitez connaître l'état des comptes, puis cliquer sur *Compte OperaToBank*.

## Voir le classement OperaToBank
Ce classement est commun à tous les serveurs.
```
/top
```

## Gagner des OperaToCoins
### Travailler
```
/work
```
Disponible une fois toutes les 2 heures.

### Voler un autre utilisateur
Clic droit sur la cible, puis clic sur *Dérober*.

Disponible une fois par semaine. Attention, ça ne marche pas à tous les coups !

### Jouer à des jeux
Les commandes `/bet` et `moneysweeper` vous permettent de gagner facilement quelques OperaToCoins.

## Utiliser ses OperaToCoins
### Faire un don
```
/give [utilisateur] [montant]
```

### Acheter des boosts et des items sur OperaToShop
Les boosts vous permettent de gagner en agilité pour voler, de vous protéger contre le vol et d'être mieux payé au travail.
``` Voir le magasin OperaToShop
/shop
```
``` Acheter un item ou un boost
/buy [identifiant de l'item]
```
``` Voir son inventaire
/inventory (hide)
```

### Liste des items et boosts disponibles
#### Protection contre le vol [!badge variant="info" text="Boost"]
*Identifiant : `protectRob`*

Ce boost diminue les chances pour les autres utilisateurs de réussir un [vol](#voler-un-autre-utilisateur) dont vous seriez la victime.

#### Boost du travail [!badge variant="info" text="Boost"]
*Identifiant : `workBoost`*

Ce boost augmente votre salaire moyen reçu lors de l'utilisation de la commande [`work`](#travailler).

#### Agilité de vol [!badge variant="info" text="Boost"]
*Identifiant : `robAgility`*

Ce boost augmente vos chances de réussite lors de l'utilisation de la commande [`rob`](#voler-un-autre-utilisateur).

### Calcul du prix des boosts
Le prix $p$ d'un boost respecte la formule suivante :
$$
p = \left\lfloor \frac{\exp(u)}{(u+1)^3} + u^2 \right\rfloor 
$$ 
où $u$ est le niveau actuel du boost (0 par défaut, entier incrémenté à chaque achat de telle manière que $u+1$ est le niveau de boost acheté).