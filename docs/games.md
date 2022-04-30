---

description: Jouez à des jeux sur Discord avec OperaToBot !
icon: trophy
label: Jeux
order: -4
---

# Jeux OperaToBot

Avec OperaToBot, vous trouverez de nombreux jeux qui vous permettront de vous amuser sur Discord, seul ou avec vos amis !

## Le jeu des allumettes de Nim
### Règles
!!!
Ce jeu se joue à deux.
!!!
Un certain nombre d'allumettes est disposé. Chacun leur tour, les joueurs prennent une, deux ou trois allumettes. Le perdant est celui qui prend la dernière.
### Jouer 
```
/allumettes [@membre] (n)
```
`n` désigne le nombre d'allumettes (10 par défaut, minimum 10).

## Le pari
### Règles
!!!
Ce jeu se joue seul et nécessite un [compte OperaToBank](bank.md). Vous ne pouvez y jouer qu'une seule fois toutes les dix minutes.
!!!
Vous misez entre 200 et 1000 OTC sur le résultat d'un lancer de dé à 6 faces. 
- Si le résultat est égal à votre pari, vous remportez deux fois votre mise.
- Si le résultat n'est pas égal à votre pari, mais est de même parité, vous remportez la moitié de votre mise.
- Sinon, vous perdez votre mise.

### Jouer
```
/bet [mise] [pari]
```
La mise doit être entre 200 et 1000 OTC, le pari entre 1 et 6.


## Le *moneysweeper* ou démonnayeur
### Règles 
!!!
Ce jeu se joue seul et nécessite un [compte OperaToBank](bank.md). 
!!!
Il s'agit d'un démineur revisité. 
Vous vous promenez sur une grille de 100 cellules. Celles-ci peuvent contenir : 
- Rien du tout (40%, dont la cellule de départ)
- Une mine (10%)
- Un portefeuille piégé (10%)
- Un portefeuille vide (10%)
- Un portefeuille rempli d'OperaToCoins (15%)
- Un billet (15%)

Le contenu des cellules ne change pas au cours de la partie (sauf action de votre part : après ramassage, un portefeuille plein d'argent devient vide).

Avant de rentrer sur la map, vous devez déposer 500 OperaToCoins à l'entrée, que vous ne récupérerez que si vous sortez vivant de la map (chose que vous pouvez décider de faire à tout moment de la partie). Vous serez ensuite placé sur une cellule vide et la partie commence alors.

A chaque instant, vous savez si les cellules autour de vous contiennent un piège ou de l'argent, mais vous n'avez pas d'informations sur leurs emplacements exacts. Par exemple, si une mine ou un portefeuille piégé se trouve dans la cellule qui est devant vous, vous aurez l'information "il y a une cellule piégée autour de votre position", mais pas l'emplacement de celle-ci. 

Vous pouvez bouger librement sur la map. Voici ce que le contenu des cellules a comme effets sur vous :
- Une cellule vide ne fait rien.
- Une mine vous tue : vous perdez tout l'argent récolté pendant votre partie ainsi que les 500 OTC déposés au début de la partie.
- Lorsque vous tombez sur de l'argent, vous le ramassez et le gagnez si vous parvenez à sortir vivant de la mine.
- Lorsque vous tombez sur un portefeuille, vous ne savez pas ce qu'il contient. Seule l'ouverture (facultative) de celui-ci aura un effet : un piège vous tue comme une mine, un portefeuille vide ne fait rien et un portefeuille rempli d'argent vous enrichit, toujours sous la condition que vous sortiez à temps.

A la fin, lorsque vous décidez de sortir (si vous n'êtes pas mort avant), vous remportez tout l'argent récolté sur la map et vous récupérez vos 500 OTC.

### Jouer
```
/moneysweeper
```

## Pierre-feuille-ciseaux
### Règles
!!!
Ce jeu se joue seul contre le bot (pour l'instant !)
!!!
La pierre bat les ciseaux, qui battent la feuille, qui bat la pierre.
### Jouer
```
/rps [paper/rock/scissors]
```

## Autres commandes de la catégorie *Fun*
### La boule numéro 8
La boule numéro 8 est omnisciente et pourra répondre à toutes vos questions.
```
/8ball [question]
```
### Le libre choix
Laissez le bot choisir...
```
/choose [options]
```
Les options doivent être séparées par des `/`.

### Le dé
Vous souhaitez lancer un dé ? Utilisez la commande `die` ! 
```
/die (nombre de faces)
```

### Memes
Regardez des memes pris au hasard sur [imgur](https://imgur.com).
```
/meme
```

