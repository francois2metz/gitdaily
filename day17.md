# Day 17

Je veux rajouter une super commande 'chuck' qui répond 'norris' (ahah).

    $ cat > /usr/local/bin/git-chuck <<< EOF
    #!/bin/sh
    echo 'norris'
    EOF
    $ chmod +x /usr/local/bin/git-chuck
    $ git chuck

Cela va créer un executable "git-chuck" qui répond simplement "norris".
git reconnait les exécutables qui se nomment git-xxx.
C'est comme cela que fonctionne :

* git-pulls: https://github.com/schacon/git-pulls
* git-pair: https://github.com/chrisk/git-pair

et beaucoup d'autres.
