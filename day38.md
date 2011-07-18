# Day 38

Je veux créer un dépôt git à partir d'un autre dépôt pour garder une partie de l'historique.

Par exemple pour créer un dépot git du sous répertoire lib/captcha.

    git filter-branch --subdirectory-filter lib/captcha -- --all

filter-branch va remplacer votre dépôt git actuel en ne gardant que les fichiers et les commits correspondant à lib/captcha.
lib/captcha deviendra donc le répertoire courant.

Vous pouvez également supprimer un fichier de votre historique git.

    git filter-branch --index-filter 'git rm --cached --ignore-unmatch config/prod.yml' HEAD

Réécrira tous les commits pour que le fichier de config/prod.yml n'y figure plus.

    git help filter-branch

Pour tester ces commandes, utiliser un nouveau clone de votre projet préféré. Ou attendez le dernier Git "Hardcore" Daily.
