# Uso de GitHub

* `git remote add origin {url}` Agregar un repositorio remoto al proyecto
    * `git remote set-url origin {url}` Modifica la url del repositorio remoto, util cuando se quiere cambiar a SSH.
* `git pull origin main` Sincroniza el repositorio remoto al local, se hacen dos acciones, `git fetch` y `git merge`
    * `--allow-unrelated-histories` Se fuciona dos _historias_ que no tienen nada que ver, ejemplo, si hay un README en el repositorio remoto y otros commits en el local.
* `git push origin main` Se envian los cambios al repositorio remoto
* `git push origin {rama}` Sincroniza ramas creadas en el repo local.