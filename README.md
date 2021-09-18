# Implentation en C du jeu de la vie 
Le principe du jeu de la vie est simple. L’univers est défini sur une grille à deux dimensions, de taille variable, ou chaque case est une cellule pouvant prendre deux états différents: morte ou vivante. Le passage d’un état à l’autre est guidé par les règles d'évolution suivantes:

-  Une cellule morte au temps t devient vivante au temps t + 1 si et seulement si elle a exactement 3
cellules vivantes dans son voisinage.
- Une cellule vivante au temps t reste vivante au temps t + 1 si et seulement si elle a exactement 2
ou 3 cellules vivantes dans son voisinage, sinon elle meurt.
- Le voisinage utilise est le 8-voisinage : pour une cellule donnée, ses voisines sont les 8 cellules
qui l’entourent.

# Commandes importantes 
### Mode graphique Cairo
Compiler
```
make
```
Lancer le jeu
```
bin/main <fichier grille>
```
Exemple
```
bin/main grilles/grille4.txt
```
### Mode texte
Compiler
```
make MODE=TEXTE
```
Lancer le jeu
```
bin/main <fichier grille>
```
Exemple
```
bin/main grilles/grille4.txt
```

# Touches importantes du programme
### Mode graphique Cairo
Faire évoluer la grille  
```
entrée ou clic gauche
```
Activer/désactiver le mode cyclique
```
c
```
Activer/désactiver le vieillissement 
```
v
```
Afficher la période d'oscillement
```
o
```
Quitter le programme
```
q ou clic droit
```
Charger une nouvelle grille  
```
n puis <fichier grille>
```
Annuler le changement de grille  
```
touche échap
```
### Mode texte
Faire evoluer la grille  
```
entrée
```
Activer/désactiver le mode cyclique
```
c
```
Activer/désactiver le vieillissement 
```
v
```
Quitter le programme
```
q
```
Charger une nouvelle grille  
```
n puis <fichier grille>
```
Annuler le changement de grille  
```
touche échap
```

# Générer la documentation
Le paquet Doxygen est requis pour générer la documentation
```
make docs
```
# Générer une archive (tarball)
```
make dist
```
# Nettoyer les artefacts de compilation et l'archive
```
make clean
```

# Système de versionnement
### vX.Y.Z

- X: Correspond au niveau, version majeur et complet
- Y: Ajouts et modifications majeurs
- Z: Ajouts et modifications mineurs

# Les différentes versions
~~~{.sh}
- 5.0.1 : Une fuite de mémoire corrigé
- 5.0.0 : Niveau 5 du projet
- 4.6.2 : Test d'oscillation fini et autres changements mineurs
- 4.6.1 : Test d'oscillation amélioré
- 4.6.0 : Affichage en mode Cairo mis à jour
- 4.5.1 : Mise à jour README.md
- 4.5.0 : L'oscillation devient non testée si on change de grilles, le mode vieillissement ou bien le mode cyclique
- 4.4.0 : Touche échap pour quitter le changement de grilles et gestion d'erreur en mode texte
- 4.3.0 : Test d'oscillation fonctionnel en mode texte
- 4.2.1 : Mise à jour README.md
- 4.2.0 : Gestion des grilles et du jeu désormais sous forme d'une bibliothéque
- 4.1.0 : Test d'oscillation fonctionnel en mode texte
- 4.0.0 : Changement de grille fonctionnel en mode Cairo
- 3.1.0 : Mode Cairo ajouté avec certaines des fonctionnalitées
- 3.0.1 : Mise à jour du makefile en préparation du niveau 4
- 3.0.0 : Le code est désormais en répertoires, makefile changé
- 2.2.1 : Mise à jour tags
- 2.2.0 : Appuyer sur n, v, ou c ne fait désormais plus passer une étape
- 2.1.1 : Mise à jour tags et README.md
- 2.1.0 : Mise à jour README.md
- 2.0.0 : Vieillissement des cellules
- 1.4.0 : Choix mode cyclique/non-cyclique
- 1.3.0 : Temps d'évolution affiché au dessus de la grille
- 1.2.0 : Documentation amélioré
- 1.1.0 : Touche n pour charger une nouvelle grille
- 1.0.0 : Fonctions alloue_grille & libere_grille
- 0.2.0 : Makefile et Doxyfile
- 0.1.0 : Commit initiale du projet.
~~~


