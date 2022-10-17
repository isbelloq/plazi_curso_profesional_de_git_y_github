# `git cherry-pick`: Traer commits viejos al head de un branch

Git Cherry-pick es un comando que permite tomar uno o varios commits de otra rama sin tener que hacer un merge completo. Así, gracias a cherry-pick, podríamos aplicar los commits relacionados con nuestra funcionalidad en la rama master sin necesidad de hacer un merge.

Para demostrar cómo utilizar git cherry-pick, supongamos que tenemos un repositorio con el siguiente estado de rama:

```
a - b - c - d   main
         \
           e - f - g feature
```

Entonces se seguiran los siguiente pasos:
1. `git checkout main`: cambio a la rama principal
2. ` git cherry-pick f`: seleccion del commit (en el ejemplo `f`) a mover a la rama principal.

Una vez ejecutado, el historial de Git se verá así:

```
a - b - c - d - f   Master
         \
           e - f - g Feature
```

> Nota: `cherry-pick` es una __mala práctica__ ya que implica un reconstruccion de la historia del repositorio y puede generar conflictos al hacer un merge completo con la rama.