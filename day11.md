# Day 11

Je veux supprimer les branches distantes qui n'existent plus.

    git fetch -p origin

Récupèrera les objets de origin et supprimera les branches distantes qui
n'existent plus. Vous aurez un 'git branch -a' correct.

L'option -p n'est pas disponible sur des versions plus anciennes de git.
On utilisera alors plutôt:

    git gc

Lance le garbage collector de git pour nettoyer et optimiser le dépôt.

    git help gc
