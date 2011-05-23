# Day 37

Je veux que Git vérifie que je n'ai pas laissé d'espaces en fin de ligne
avant chaque commit, et qu'il annule ce dernier le cas échéant :

    mv .git/hooks/pre-commit.sample .git/hooks/pre-commit

Plus d'informations sur les hooks :

    man githooks
