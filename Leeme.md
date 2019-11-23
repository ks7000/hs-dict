Diccionarios para Hunspell
==========================

For english speakers: [https://github.com/ks7000/hs-dict/readme.md]

Este repositorio proporciona los diccionarios para el corrector ortográfico *Hunspell*. Cada idioma está separado dentro de su propia rama, donde cada una está directamente basada en la rama que sirve como `ancla` y además todas están fusionadas en la rama `master`. El corrector ortográfico en sí mismo *no está incluido* pero está disponible en [http://hunspell.sourceforge.net].

Si usted gusta de agregar otro diccionario, por ejemplo un *nuevo* idioma abreviado `zz` y cuyo país sea `ZZ` entonces:

    $ git checkout anchor
    $ git checkout -b zz
    $ git add zz_ZZ.aff
    $ git add zz_ZZ.dic
    $ git commit -m "Nuevo diccionario: zz"
    $ git push --set-upstream origin zz
    $ git checkout master
    $ git merge zz

De otra manera, si la rama del idioma `zz` ya existe, etnonces:

    $ git checkout zz
    $ git add zz_ZZ.aff
    $ git add zz_ZZ.dic
    $ git commit -m "Nuevo diccionario: zz"
    $ git push --set-upstream origin zz
    $ git checkout master
    $ git merge zz

Esta secuencia de comandos asegurará que la historia del repositorio permanecerá limpia, y habilita el acceso a dad diccionario de manera separada. Si su diccionario es de alta calidad y puede ser usado por otros y otras, por favor considere hacer un aporte (`pull request`) con su información.

Todos los archivos deben contener una cabecera con respecto a qué; de otro modo una licencia GPL puede ser adoptada. No obstante si el autor original no incluyó una cabecera, *por favor* haga el esfuerzo de hacer la debida aclaratoria. Los autores originales que sientan que omitieron dicha información pueden contactar al encargado de este repositorio y solicitar se le incluya la debida información sobre la licencia de uso.
