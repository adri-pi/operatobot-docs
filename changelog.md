---

description: Notes de mise à jour des services OperaToBot
icon: history
label: Notes de mise à jour
order: -20
---


# Notes de mise à jour
Cette page contient toutes les notes de mise à jour du bot, depuis la version 1.0.0.

## Version 3.0.1 [!badge text="BETA" variant="info"] [!badge text="Dernière version" variant="info"]
*Déployée le 13/05/2022*
### Modifié
- Commande `/status` mise à jour pour être cohérente avec la nouvelle page de statut
- Bug emoji OperaToCoin résolu

## Version 3.0.0 [!badge text="BETA" variant="info"]
*Déployée le 12/05/2022.*
### Ajouté
- Commandes slash
- Commandes utilisateur 
- BoutonRôle
- Logs de paramétrage du bot
- CGU et Politique de Confidentialité
- Bouton "Inviter le bot" et profil bot
- Commande `modules`
### Modifié
- Nouveau site internet, déplacé sur un autre domaine et une autre plateforme
- Système de permissions pour les commandes, maintenant cohérent avec le nouveau système de permissions Discord
- Commandes `mute`, maintenant cohérentes avec le système d'exclusion intégré par Discord
- Les commandes `rob` et `userstats` (fusion de `avatar` et `userinfo`) est maintenant uniquement accessible via le menu clic droit utililisateur
- Commande `setup` améliorée
- Amélioration de la confirmation d'actions sensibles
- Commande `hackban` renommée en `hardban`
- Serveur de support
- Mise à jour de la page [top.gg](https://top.gg/fr/bot/503954760139800577)
- Identité visuelle
- De nombreux bugs corrigés
### Supprimé
- Toutes les commandes avec le préfixe `tb!`, pour suivre la nouvelle politique de Discord en matière de bots
- Réglage du ReactionRole, du préfixe, des administrateurs bot, du rôle muet, des webhooks
- OperaToShop : item `supportAd` (publicité sur le serveur de support)
- VCS
- Commandes rendues obsolètes par les commandes `set` et `setup` : `autorole`, `module`, `reactionrole`
- Commandes rendues obsolètes par les informations disponibles sur le profil : `botinfo`, `invite`, `support`, `suggest`
- Commande `use` temporairement retirée en l'absence d'items dans OperaToShop
- Commande `bingo` supprimée, suite à la nouvelle politique de Discord en matière de bots qui l'empêche de voir le contenu des messages

## Version 2.0.5
*Déployée le 27/04/2021.*
### Modifié
- Bugs corrigés
- Message de la commande `purge` complété
- Mise à jour du serveur de monitoring (utilisé notamment pour la commande `status`)

## Version 2.0.4
*Déployée le 14/04/2021.*
### Modifié
- Bugs corrigés

## Version 2.0.3
*Déployée le 26/08/2020.*
### Modifié
- Bugs corrigés

## Version 2.0.2
*Déployée le 22/08/2020.*
### Ajouté
- Commande `moneysweeper`
### Modifié
- Commande `help` revue afin d'ajouter des liens vers la documentation
- Bugs corrigés

## Version 2.0.1
*Déployée le 19/08/2020.*
### Modifié
- Bugs corrigés

## Version 2.0.0
*Déployée le 19/08/2020.*
### Ajouté
- Commandes d'administration `setup` et `delete`
- Recherche d'images : commandes `imgur` et `giphy`
- OperaToShop : commandes `shop`, `inventory`, `use` et `buy`
- Mini-jeux : commande `bet`
### Modifié
- Mise à jour de discord.js vers la version 12.3.1
- Mise à jour et optimisation de la base de données
- Optimisation et mise à jour du reaction role en vue d'autres mises à jour
- Fusion des commandes `serverinvite` et `botinvite` dans la commande `invite`
- Nouveau système de suggestions avec une modification de la commande `suggest`
- Commande `support` modifiée, plus d'envoi de message direct au support.
- Refonte de la plupart des commandes du bot, pour une meilleure optimisation
- Plusieurs commandes dépréciées
- OperaToShop : commande `give` permettant de donner des items ; commandes `work`, `bingo` et `rob` améliorées en conséquence
- Commande `meme` totalement revue avec l'utilisation d'[imgur](https://imgur.com) et non plus des suggestions des utilisateurs
### Supprimé
- Système d'alertes
- Anciennes commandes de recherche et d'édition d'images qui ne fonctionnaient plus
- Suppression de la commande `mention`
- Suppression du `set vcs`

## Version 1.5.1
*Déployée le 28/04/2020.*
### Modifié
- Nouveau serveur plus rapide pour l'hébergement du bot
- Correction de la commande `give`
- Limitations ajoutées sur le `bingo`

## Version 1.5.0
*Déployée le 11/01/2020.*
### Ajouté
- Système de modules activables et désactivables avec la commande `module`

## Version 1.4.0
*Déployée le 27/10/2019.*
### Ajouté
- Système OperaToBank avec les commandes `bank`, `bingo`, `give`, `rob` et `work`

## Version 1.3.4
*Déployée le 07/09/2019.*
### Ajouté
- Commande `changelog`
### Modifié
- Système de notifications de mises à jour. Désormais, toutes les notes de mise à jour seront envoyées uniquement sur le VCS et sur le serveur de support.
### Retiré
- Commande `update` 

## Version 1.3.3
*Déployée le 21/08/2019.*
### Ajouté
- Cooldown d'une minute sur le VCS
### Modifié
- Transfert de la base de données du VCS et mise à jour
- Bugs corrigés

## Version 1.3.2
*Déployée le 19/08/2019.*
## Modifié 
- Bugs corrigés

## Version 1.3.1
*Déployée le 18/08/2019.*
### Ajouté
- Envoi d'un message dans le VCS lors d'un ban VCS
- Message d'erreur quand un utilisateur banni du VCS tente de l'utiliser
- Détection et blocage des messages comprenant un URL dans le VCS
### Modifié
- Mise à jour des liens menant vers la documentation
- Bugs corrigés

## Version 1.3.0
*Déployée le 11/08/2019.*
### Ajouté
- Commande `reactionrole`
- Attribution de rôles par réaction

## Version 1.2.0
*Déployée le 28/06/2019.*
### Ajouté
- Aliases
- Commande `steamplaying`
- Commande `vcslist`
### Modifié
- Commande `help`
### Supprimé
- Toutes les commandes remplacées par la commande `set`

## Version 1.1.2
*Déployée le 09/06/2019.*
### Ajouté
- Commande `status`
### Modifié
- Ajout de détails sur la commande `botinfo`

## Version 1.1.1
*Déployée le 30/05/2019.*
### Ajouté
- Badge *Modérateur* sur le VCS pour les membres du support.
### Modifié
- Le `help` de la commande `set` était erroné et a été corrigé.
- Correction d'un bug sur la commande `set prefix`

## Version 1.1.0
*Déployée le 18/05/2019.*
### Ajouté
- Commandes d'édition d'images (via HelixusAPI)

## Version 1.0.2
*Déployée le 27/04/2019.*
### Modifié
- Correction d'un bug sur la commande `userinfo` qui ne fonctionnait pas correctement
- Correction du bug du jeu de la commande `allumettes` sur le message qui informe qu'aucune réponse n'a été reçue au bout d'une minute de la part d'un joueur

## Version 1.0.1
*Déployée le 15/04/2019.*
### Modifié
- Amélioration de la commande `mention`, qui utilise désormais des webhooks.
- Bugs corrigés

## Version 1.0.0
*Déployée le 06/04/2019.*
### Ajouté
- Commande `set` 
- Site Internet
### Modifié
- Refonte de plusieurs commandes