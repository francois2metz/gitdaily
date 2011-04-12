# Day 9

Je veux connaitre tous les commits depuis hier.

    git log --since yesterday

Un petit bonus ajourd'hui:

    git log HEAD^

Listera les commits a partir de l'avant dernier commit.

    git log HEAD~4..

Listera les quatres dernier commit. Equivalent à :

    git log HEAD~4..HEAD

Plus d'infos:

    git help revisions
