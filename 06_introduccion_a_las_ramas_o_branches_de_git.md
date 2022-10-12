# Introduccion a las ramas o branches de Git
* `git commit -a` Se hace el commit de los archivos ya trakeados sin necesidad de hacer git add antes.
* `git show` Muesta el HEAD.
* `git branch {nombre_rama}` Crea una rama nueva
* `git checkout {nombre_rama}` Se cambia a la rama especificada.
    * `git checkout -b {nombre_rama}` Se crea y se cambia a la rama recien creada.
* `git reset {id}`: Nos lleva a cualquier commit no importa la rama, ya que identificamos el `id`, eliminando el historial de los commit posteriores al `id` seleccionado.
* `git checkout {rama|id}`: Nos lleva a cualquier commit sin borrar los commit posteriores a `rama|id` seleccionado.