# Spécification des entités relatives aux terrains

Un terrain représente l'endroit où les bateaux s'affrontent. Il y en a un par niveau.


## Représentation

Un terrain ("map" en anglais, "carte" en français) est décomposé en plusieurs couches, chacunes avec leur utilité.

La première est cachée : il s'agit de calculs. Chaque objet possède une position, et ces positions sont placés sur une "ligne". Ainsi, chaque intéraction
qui existe compare ainsi leurs positions pour déterminer les contacts, par exemple en vérifiant si un obus "touche" un navire en vérifiant les coordonnées
et les zones de contact ("hitboxes").

Les autres couches sont visibles, comme dans un théâtre : plusieurs plans se superposent pour former une image en profondeur. D'abord l'eau, puis les
navires, puis les nuages, puis le ciel. Cela paraît évident dit comme ça, mais tout cela représente une étude couche par couche et une actualisation
résulière importante et méthodique, pour donner un bon rendu visuel.
