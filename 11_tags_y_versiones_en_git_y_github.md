# Tags y versiones en Git y Github

* `git tag` muestra los tags de un proyecto
    * `git tag -a v0.1 -m "{mensaje}" {id}` Se crea un tag en un commit especifico. La bandera `-a` agrega la version y `{id}` debe ser el identificador del commit.
    * `-d {nombre_tag}` Elimina el tag en el repo local
* `git show-ref --tags` muestra el `{id}` del commit con el que estan los tags
* `git push origin --tags` Agrega los tags al repositorio remoto
    * `git push origin :refs/tags/{nombre_tag}` elimina el tag en el repositorio remoto