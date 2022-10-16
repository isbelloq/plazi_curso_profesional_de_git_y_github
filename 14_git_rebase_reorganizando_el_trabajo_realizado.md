# `git rebase`: reorganizando el trabajo realizado

__ATENCION__ este comando es una mala practica en general porque reescribe la historio del repositorio.

El comando `git rebase` es el proceso de cambiar el punto de partida de una rama, esto hace que los commits hechos en una rama se vuelvan parte de la historio de la rama a la cual se le hace `git reabse`. __Este comando es una mala practica en general, no se recomienda hacerlo en un repositorio remoto, se sugiere solo hacerlo en repositorios locales, se recomienda usar con criterio__.

Supongamos el siguiente escenario, se quiere hacer hacer un rebase de la `rama_1` para incluir la historia de la `rama_2`. Los pasos para su uso son:

1. Hacer un `git checkout {rama_2}`
2. Hacer un `git rebase {rama_1}`
3. Hacer un `git checkout {rama_1}`
4. Hacer un `git rebase {rama_2}`

Si no se sigue este orden __se pueden causar conflictos dificiles de arreglar__.