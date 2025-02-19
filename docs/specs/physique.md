# Spécification des aspects physiques

À chaque instant du combat, les objets se déplacent en fonction de leurs valeurs cinématiques à l'instant précédent. Tout les paramètres réels ne 
sont pas forcément utilisé (vent et vagues par exemple) pour des raisons de simplicité, mais une mécanique d'accélération et décélération progressive
a été mise en place.

## Principe

### Navires

Le joueur peut régler la vitesse de son navire en utilsant un "chadburn" ("transmetteur d'ordre"). Ce "chadbrun", utilisé sur les navires à vapeur 
puis ceux jusqu'à la fin du XXè siècle (toujours présent aujourd'hui mais peut utilisé) permet de donner une vitesse désirée étant un pourcentage de 
la vitesse maximale, allant de "full ahead" (avance à pleine vitesse) à "full reverse" (recule à pleine vitesse) en passant par "full stop" (arrêt).
Le "chadburn" est contrôlé par une icône sur le bas de l'écran, pouvant régler cran par cran la vitesse désirée.

### Obus

Il n'y a pas que les navires qui se déplacent dans le jeu : en effet, un système de ballistique a été mis en place, gérant la trajectoire que prennent
les obus pour toucher leur cible. Comme pour les navires, le vent n'a pas été pris en compte mais les obus parcourrent une trajectoire parabolique,
nécessitant ainsi du joueur de prévoir ses attaques.

## Calculs

Les calculs utilisés pour représenter les mouvements se basent tous sur cette formule :
```markdown
x(t+dt) = x(t) + v(t) * dt
```

Avec : `x(t)` = position d'un objet, `v(t)` = vitesse de l'objet et `dt` = temps passé entre deux calculs ("delta t" en physique ou "tick" dans les jeux vidéos).




