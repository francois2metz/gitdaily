# Day 13

Je veux initialiser un dépôt git pour ma config système.

    git init /etc

ou sur des versions plus anciennes de git:

    GIT_DIR=/etc git init

Initialisera un dépôt git dans /etc. Alors pour votre bout de code
qui-ne-sera-pas-réutilisé-c'est-sur, git init && git add . && git commit.

    git help init
