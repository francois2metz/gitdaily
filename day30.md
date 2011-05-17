# Day 30

Je veux que mon bash affiche dans quelle branche je suis. Dans ~/.bashrc,
j'ajoute en fin de fichier :

    PS1='\w\e[1;32m$(__git_ps1)\e[m$ '

\w indique le répertoire courant, 
\e[1;32m démarre une chaine en vert flashy,
$(_\_git\_ps1) correspond à votre branche 
et \e[m revient à la couleur normale.
