# Day 30

Je veux que mon bash affiche dans quelle branche je suis. Dans ~/.bashrc,
j'ajoute en fin de fichier :

    PS1='\w$(__git_ps1)\$ '

\w indique le répertoire courant,
$(_\_git\_ps1) correspond à votre branche
et \$ affiche # si vous êtes super-utilisateur.
