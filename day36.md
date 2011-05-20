# Day 36

Je veux n'afficher que les commits d'une personne :

    git log --author="John Smith"

Je peux aussi faire un alias pour ne montrer que mes commits :

    mylog = !git log --author=`git config --get user.email`

Le point d'exclamation demande une exécution directe par bash.
