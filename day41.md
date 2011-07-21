# Day 41

Je veux regrouper deux dépôts git en un seul :

    git replace SHA1 SHA2

Le commit SHA1 va être remplacé par SHA2 et tous ses parents.

Je ne me suis jamais servi de cette commande autrement que pour la tester, mais
elle peut être pratique si vous avez un historique volumineux et qu'il n'est pas nécessaire de totalement le garder.

C'est qui a été fait pour le dépôt d'otp qui fait plus de 300 Mo : https://github.com/erlang/otp/wiki/Extending-the-history-of-Erlang-OTP.

Vous pouvez facilement le tester avec quelques commandes pour relier deux dépôts. Relions les dépôts de EventMachine et de NodeJS.

    $ git clone https://github.com/eventmachine/eventmachine.git
    $ git remote add nodejs https://github.com/joyent/node.git
    $ git fetch nodejs
    $ git replace d9a23e4779b3f555e63e4ff565ef0848a8bcabd4 61dfe5d2a9f613e3826997efa189ec8dd239aacf

Oui ça ne sert à rien. Mais regardez le git log et tout se passe comme si de rien n'était.

    git help replace (mais ça ne va pas beaucoup vous aider)

    http://progit.org/2010/03/17/replace.html
