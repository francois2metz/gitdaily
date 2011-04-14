# Day 12

Je veux revenir à un commit en oubliant tout ce qui est en cours:

    git reset --hard SHA1

Vous mettra dans l'état du commit en paramètre. Tout ce que vous avez pu modifier ou commiter est perdu (enfin pas tout à fait).
Si vous avez déjà pushé les commits en question c'est une mauvaise pratique.

    git help reset
