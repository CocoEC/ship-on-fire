# Spécification des entités relatives aux bateaux utilisées in-game :

## Elements liés aux navires

### Navire

```markdown
<ship> ->
- <weapons>
- "health attributes"
- "kinematics attributes"
```

Description :

Un `<ship>` est la base du jeu, que l'on peut manipuler. Il se compose de trois parties majeurs, chacunes avec leurs fonctionalités :

`<weapons>` correspond à l'équipement offensif du navire, c'est à dire le nerf de la guerre. Elles seront détaillées un peu plus loin dans ce document.

"health attributes" est lié à la survivabilité du navire. Chaque navire a deux barres de vie différentes : la coque et l'équipage. Si l'une des 
deux tombe à zéro, c'est *game over*. Ainsi, on peu mixer les armes et les objectifs pour réussir à gagner la bataille. 
De même, chaque perte de vie a ses pénalités : pour la coque, les armes peuvent êtres détruites; pour l'équipage, la vitesse des actions et le 
temps de rechargement augmente.
Remarque : une mécanique d'armure permet aux navires de réduire certains types de dégâts, rendant ainsi les combats plus dynamiques.

"kinematics attributes" correspond à la mobilité du navire. Dans ce jeu, même si l'arène est en 2D, on peut se déplacer pour esquiver des attaques, 
profiter de la portée et la précision des armes (soit de loin soit de près) ou même surprendre l'adversaire. 
Elle est gérée par un "chadburn" ("transmetteur d'ordre") qui, comme dans un vrai navire, permet de régler la vitesse non pas sur une valeur 
numérique mais sur un pourcentage de la vitesse maximale. Pour plus de précisions, cf. ce [doc](physique.md)

### Arme

```markdown
<weapons> ->
- "shells attributes"
- "health attributes"
```

Description :

Les combats sont une partie vitale de *Ship on fire !*. Dans ce sens, les `weapons` sont un composant primordial. Por fonctionner, ils ont besoin de :

"shells attributes" qui définit les différentes propritétés que possèdent les obus tirés : le calibre de l'arme (pour les dégâts et la balistique), 
le point de départ de l'obus, et surtout, leur type.
Chaque obus a un style parmi les suivants :
- Explosif (HE) : conçu pour infliger des dégâts à l'équipage et aux cibles non blindées.
- Perforants (AP) : N'inflige que peu de dégâts à l'équipage et moins de dégâts en tout, mais affecte bien plus les cibles blindées.
- Incendiaire : Peu de dégâts sur les différents armes mais décime l'équipage du navire : attention aux débuffs !

"health attributes" : comme pour les navires, mais sans notion d'équipage. L'armure reste cependant active, et si l'arme est détruite, elle devient
inutile.

### Obus

```markdown
<shell> ->
- "shells attributes"
- "kinematics attributes"
```

Description :

"shells attributes" correspond aux propritétés héritées des armes qui les ont tirées

"kinematics attributes" correspond aux données liées à au déplacement de l'obus (vitesse, direction, position...)

