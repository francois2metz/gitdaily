# Day 40

Vous avez des conflits récurrents lors des merge et vous voulez les corriger une bonne fois pour toute.

La première chose à faire est de configurer la variable *rerere.enabled*.

    git config --global rerere.enabled 1

Ensuite ? Vous laissez faire git. Il va automatiquement enregistrer les conflits et leurs résolutions pour refaire la même chose automatiquement.

Aux prochains git pull --rebase ou aux git merge, plus besoin de réappliquer le même correctif.

Si vous avez enregistré une mauvaise résolution, vous pouvez utilisez git rerere forget.

Et pourquoi rerere ? C'est l'abbréviation de Reuse recorded resolution.

    git help rerere

    http://progit.org/2010/03/08/rerere.html
