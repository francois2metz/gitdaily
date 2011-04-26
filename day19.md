# Day 19

Je veux récupérer un commit qui est sur une autre branche.

    git cherry-pick SHA1

Va récupérer le commit SHA1 et l'appliquer sur la branche courante. Attention, le commit parent n'étant pas le même, le SHA1 va changer.

    git help cherry-pick
