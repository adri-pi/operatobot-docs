---

description: Gérez la modération de votre serveur.
icon: law
label: Modération
order: -2
---

# Modération


!!!danger Fermeture du service OperaToBot
Le service OperaToBot cessera de fonctionner définitivement le 31 juillet 2024. [En savoir plus.](/shutdown.md)
!!!

OperaToBot est une solution de modération très complète pour gérer les sanctions sur votre serveur.

!!!
Les permissions indiquées sur cette page sont les permissions **par défaut**, et peuvent être modifiées dans les paramètres de votre serveur.
!!!

## Avertissements (`warn`)
OperaToBot vous permet d'avertir les membres de votre serveur. 
!!!warning
Les commandes suivantes nécessitent la permission *Modérer les membres*.
!!!
### Ajouter un avertissement
```
/warn add [@membre] [raison]
```
Ceci enregistre un avertissement dans la base de données, envoie un message privé au membre concerné si cela est possible, et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

### Retirer un avertissement
```
/warn remove [@membre] [numéro]
```
Ceci retire l'avertissement mentionné de la base de données et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.
Le numéro de l'avertissement est celui qui s'affiche dans la [liste des avertissements](#lister-les-avertissements-dun-membre).

### Retirer tous les avertissements d'un membre
```
/warn remove [@membre]
```
Ceci retire tous les avertissements du membre de la base de données et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

### Lister les avertissements d'un membre
```
/warn list [@membre]
```
Ceci liste les avertissements du membre mentionné.


## Exclusion temporaire d'un membre (`mute`)
!!!warning
Les commandes suivantes nécessitent la permission *Modérer les membres*.
!!!
Pour sanctionner un membre en l'empêchant temporairement de participer aux conversations de votre serveur sans l'expulser ni le bannir, vous pouvez l'exclure temporairement.
!!!
Autrefois, le `mute` était effectué à l'aide d'un rôle avec des permissions qui n'étaient pas toujours bien réglées. Aujourd'hui, nous utilisons le système intégré de Discord qui fait bien mieux les choses.
!!!
### Exclure temporairement un membre
```
/mute [@membre] (raison) (jours) (heures) (minutes)
```
Exclure temporairement le membre pour la durée indiquée. Envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

### Mettre fin à l'exclusion temporaire d'un membre
```
/unmute [@membre] (raison)
```
Met fin à l'exclusion temporaire du membre. Envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

## Expulsion d'un membre
!!!warning
La commande suivante nécessite la permission *Expulser des membres*.
!!!
```
/kick [@membre] (raison)
```
Ceci envoie un message privé au membre concerné si cela est possible, l'expulse du serveur, et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

## Bannissement d'un membre
!!!warning
La commande suivante nécessite la permission *Bannir des membres*.
!!!
```
/ban [@membre] (raison)
```
Ceci envoie un message privé au membre concerné si cela est possible, le bannit du serveur, et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

## Bannissement d'un utilisateur n'étant pas sur le serveur
!!!warning
La commande suivante nécessite la permission *Bannir des membres*.
!!!
```
/hardban [identifiant de l'utilisateur] (raison)
```
Ceci bannit l'utilisateur du serveur et envoie un log dans le salon paramétré pour les logs de modération, s'il existe.

## Nettoyage d'un salon
```
/purge [n]
```
Ceci supprime les $n$ derniers messages (de moins de 15 jours) en masse dans le salon où est effectuée la commande.
!!!danger
Si le nombre de messages indiqués est strictement supérieur au nombre de messages effectivement envoyés dans le salon, un comportement inattendu peut se produire : des messages envoyés ultérieurement à la commande pourraient être supprimés. Soyez donc attentif au nombre $n$ indiqué.
!!!