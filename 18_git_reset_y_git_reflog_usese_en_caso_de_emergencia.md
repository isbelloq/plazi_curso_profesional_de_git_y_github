# `git reflog` y `git reset`: usese en caso de emergencia

El comando `git reflog` muestra __todo el historial__ en el repositorio, se puede ve interpretar como fotos puntuales de un repositorio por cada accion realizada.

Para recuperar una de estas _fotos_ se usa el comando `git reset` de la siguiente forma:

* `git reset --HARD {id_de_reflog}`: Reinicia todo al `id` espeficifado y se perderá todo lo que se encuentra en staging.
* `git reset --SOFT {id_de_reflog}`: Te recuperará todos los cambios que tengas diferentes al `id_de_reflog`, los agregará al staging area.

Usualmente se usa `git reset --HARD`

> Nota: este comando solo se debe usar en __casos de emergencia__ por si algo se rompe en el codigo.