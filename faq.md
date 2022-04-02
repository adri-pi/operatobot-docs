---
author: Adrien
description: Une question ? Un problème avec le bot ? Avant de demander au support, lisez la FAQ !
icon: question
label: FAQ
order: -10
---

# Foire aux questions

## Comment inviter le bot ?
En cliquant sur le bouton suivant : 

[!button Inviter le bot](invite.md)

Ne désactivez pas les permissions administrateur, elles sont essentielles au bon fonctionnement du bot. Veillez à élever le rôle du bot au-dessus des rôles à contrôler (notamment pour le BoutonRole ou les commandes de modération).

## J'ai lancé une commande, mais celle-ci ne répond pas ou ne fonctionne pas correctement. Pourquoi ?
Vérifiez que vous avez bien indiqué des arguments corrects, et que vous avez les bonnes permissions. Si c'est le cas, mais que la commande ne fonctionne pas ou mal, rejoignez le [serveur de support](support.md) et signalez le problème dans le salon #bugs, en précisant la commande lancée avec les arguments indiqués.

## Je vois un message "Echec de l'interaction", mais la commande fonctionne tout de même. Pourquoi ?
**C'est un bug.** Signalez-le sur le [serveur de support](support.md) dans le salon #bugs, en précisant la commande lancée, avec les arguments indiqués, ainsi qu'un screenshot du message.

## Le BoutonRole ne fonctionne pas lorsque j'appuie sur le bouton. Pourquoi ?
Plusieurs raisons possibles : 
- Le rôle **n'existe plus.** Il faut alors supprimer le message sur lequel se trouve le bouton et le reconfigurer.
- Le rôle **ne peut pas être contrôlé**, car le bot n'a pas les permissions nécessaires (rôle au-dessus de lui, ou permission Administrateur désactivée).
- Le BoutonRole **n'a pas été réglé pour votre cas**. Par exemple, l'administrateur peut décider que le bouton ne puisse que retirer un rôle, et non l'ajouter ; et vous ne possédez pas ce rôle. Le bot envoie donc un message d'erreur. Un tel comportement est indiqué sur le message.
Si aucun de ces points n'explique le dysfonctionnement, veuillez rejoindre le [serveur de support](support.md) et indiquer votre problème.

## De nombreuses commandes ne répondent pas sur mon serveur. Que faire ?
Il est probable que les commandes soient désactivées via les modules : vérifiez-le avec `/setup modules`. Il est aussi possible que le bot n'ait pas les permissions nécessaires à son bon fonctionnement : en effet, il a besoin de la permission Administrateur.

## Comment paramétrer le bot ?
[!ref](docs/settings)

## Comment soutenir le projet ?
Le développeur n'accepte pas les donations financières pour le moment. Cependant, vous pouvez voter pour le bot sur top.gg ou parler du projet autour de vous pour le soutenir !

[!button Voter pour le bot sur top.gg](https://top.gg/bot/503954760139800577/vote)