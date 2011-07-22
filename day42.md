# Day 42

Vous avez commité sur aucune branche ? Vous avez raté un git reset --hard ? Vous avez testé git filter-branch sur un dépôt avec plein de patchs super importants ?

    git reflog

Reflog enregistre tout les changements qui sont fait sur les branches et le
dépôt. Vous devriez y voir par défaut vos commits, merge et autres pull. Un bon
espion qui peut vous sortir d'un mauvais pas.

Voici une sortie typique de reflog.

    d2bbd0e HEAD@{1}: commit: Run the bootstrap script when running bench.
    bd91916 HEAD@{2}: bd919164c72c38b88a85275ee5b9add7f7a8f382: updating HEAD
    2ce209e HEAD@{3}: pull origin master: Merge made by recursive.
    bd91916 HEAD@{4}: commit: Generate tsung scenario from a yml file.
    4cdc612 HEAD@{5}: checkout: moving from complex_metadata to develop
    44fb6fc HEAD@{6}: commit: Initial support of complex metadata in events.
    4cdc612 HEAD@{7}: checkout: moving from 4cdc61204e4ea5c6814c65c88e2ef19031c2cf6d to complex_metadata

Par exemple, pour rapratrier un commit qui est dans aucune branche (*Not currently on any branch.*) :

    git reflog (trouver le bon commit, par exemple d2bbd0e)
    git checkout master
    git cherry-pick d2bbd0e

Ou bien récupérer votre dépôt après un git filter-branch :

    git reflog
     129b276 HEAD@{0}: filter-branch: rewrite
     bbd8de8 HEAD@{1}: rebase -i (pick): Optimize uce_paginate.
    git reset --hard bbd8de8

Quelques sous-commandes sont disponibles comme *expire* et *delete*.

    git help reflog
