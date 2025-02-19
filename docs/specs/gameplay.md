# Spécification du gameplay

Élément essentiel : combat.

Un combat oppose 2 bateaux et se passe sur un terrain.
Le joueur affronte un bateau commandé par une IA.

## Actions possibles

Pendant un combat, le joueur peut :
* déplacer la caméra
* sélectionner une arme en cliquant sur son icône en bas, si elle est activable. Il rentre alors en mode visée, choisit un angle et peut cliquer pour confirmer son tir.
* sélectionner un équipement en cliquant sur son icône en bas, s'il est activable. Les effets de l'équipement sont alors activés.
* changer la vitesse demandée au chadburn.
* mettre le jeu en pause

## Gestion des cooldowns

Pour chaque type d'équipement à cooldown, le cooldown a une valeur minimale et une valeur maximale. La valeur effective du cooldown est 
répartie de la manière suivante :
* 100% -> 80% d'équipage : 1x cooldown_min
* 80% -> 20% d'équipage : de 1x cooldown_min à 2x cooldown_min de manière linéaire
* 20% -> 0% d'équipage : 2x cooldown_min
