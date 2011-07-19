# Day 39

Vous voulez réécrire votre historique git pour regrouper des commits, en supprimer, et d'une manière générale tout changer.

    git rebase -i SHA1

SHA1 étant le commit de départ, que vous ne voulez pas modifier. Tous ceux au
dessus pourront être réécrit. Git ouvre votre *EDITOR* et vous demande quelles
opérations vous voulez faire. Vous pouvez garder le commit tel qu'il est, le
fusionner avec celui précédent, le supprimer.

    pick 379ab2a Move all presence as pid.
    pick 42bab02 Update timeout module to use the new presence api.
    pick d1da4b4 No more indexes for uce_presence_mongodb.
    pick 94835c2 No more indexes for uce_presence_mnesia.
    pick 0a481e9 Optimize uce_paginate.
    pick 09b4224 Connected user as pid.

Sur l'exemple précédent, vous pouvez modifier le buffer comme suit:

    pick 379ab2a Move all presence as pid.
    squash 42bab02 Update timeout module to use the new presence api.
    squash d1da4b4 No more indexes for uce_presence_mongodb.
    squash 94835c2 No more indexes for uce_presence_mnesia.
    reword 09b4224 Connected user as pid.

Ce qui va se passer :

* 42bab02, d1da4b4 et 94835c2 vont être fusionné avec 379ab2a. Git vous proposera aussi de réécrire le message de commit.
* Vous pourrez rééecrire le message de commit de 09b4224.
* Le commit 0a481e9 étant supprimé du buffer, il sera également supprimé de l'historique.

    git help rebase
