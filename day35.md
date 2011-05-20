# Day 35

Il est possible de formater les logs à volonté :

    git log --pretty=format:'%Cred%h%Creset %s %Cgreen(%cr) %Cblue<%an>'

Avec :

    %C pour changer la couleur
    %h pour le SHA1 abrégé
    %s pour le sujet du commit
    %cr pour la date relative
    %an pour le nom de l'auteur

Plus d'informations sur pretty format : 

    man git show
