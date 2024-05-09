---

description: Activez ou désactivez les fonctionnalités d'OperaToBot.
icon: multi-select
label: Modules OperaToBot
order: -5
---

# Modules OperaToBot


!!!danger Fermeture du service OperaToBot
Le service OperaToBot cessera de fonctionner définitivement le 31 juillet 2024. [En savoir plus.](/shutdown.md)
!!!

Ce paramètre permet de choisir les modules de commande à activer sur votre serveur.

!!! Permissions nécessaires
La modification de ce paramètre nécessite la permission *Gérer le serveur*.
!!!

## Principe
Lorsqu'une commande est utilisée sur votre serveur, si le module dont elle fait partie est désactivé, celle-ci n'enclenchera aucune action de la part du bot.

!!!
Certains modules ne peuvent être désactivés, car sont absolument nécessaires au bon fonctionnement du bot. C'est le cas du module *Administration*, contenant les commandes de paramétrage comme `set`.
!!!

## Paramétrage 
### Avec la commande `set`
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

## Liste des modules
Vous retrouverez cette liste en utilisant la commande `/modules` sur votre serveur. Cette même commande indique également si chaque module est activé ou non sur votre serveur.

!!!
Tous les modules ne peuvent être désactivés. Les modules qui peuvent l'être sont signalés ci-dessous par le badge [!badge variant="success" text="Réglable"] ; les autres sont signalés par le badge [!badge variant="danger" text="Persistant"].
!!!

Module | Identifiant | Description
--- | --- | ---
:books: Administration [!badge variant="danger" text="Persistant"] | `admin` | Commandes pour gérer un serveur, essentiellement réservées aux administrateurs.
:moneybag: OperaToBank [!badge variant="success" text="Réglable"] | `bank` | Commandes liées à OperaToBank, le système économique fictif d'OperaToBot.
:robot_face: Bot [!badge variant="danger" text="Persistant"] | `bot` | Commandes pour obtenir des informations, de l'aide ou des liens en rapport avec OperaToBot.
:bowling: Jeux & loisirs [!badge variant="success" text="Réglable"] | `fun` | Commandes pour s'amuser un peu avec le bot.
:frame_with_picture: Images [!badge variant="success" text="Réglable"] | `images` | Commandes pour afficher et éditer simplement des images.
:information_source: Informations [!badge variant="success" text="Réglable"] | `info` | Commandes permettant d'afficher des informations diverses.
:scales: Modération [!badge variant="success" text="Réglable"] | `mods` | Commandes de modération