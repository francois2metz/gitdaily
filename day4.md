# Day 4

Je veux modifier mon dernier commit, parce que j'ai mis un mauvais
message de commit.

    git commit --amend

Modifie le dernier message de commit. Peut aussi rajouter les
modifications de votre zone de staging.

    git add myfile.erl && git commit --amend

Rajoutera la modification de myfile.erl dans le précédent commit.

Cette commande réécrivant l'historique git, vous ne devez PAS le faire
si vous avez déjà pushé.
