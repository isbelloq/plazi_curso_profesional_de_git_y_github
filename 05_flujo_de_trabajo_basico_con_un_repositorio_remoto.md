# Flujo de trabajo basico con un repositorio remoto

## Comandos para trabajar remoto con git

* `git clone {url}`: Nos permite descargar los archivos de la última versión de la rama principal y todo el historial de cambios en la carpeta .git.
* `git push`: Luego de hacer git add y git commit debemos ejecutar este comando para mandar los cambios al servidor remoto.
* `git fetch`: Lo usamos para traer actualizaciones del servidor remoto y guardarlas en nuestro repositorio local (en caso de que hayan, por supuesto).
* `git merge`: También usamos el comando `git merge` con servidores remotos. Lo necesitamos para combinar los últimos cambios del servidor remoto y nuestro directorio de trabajo.
* `git pull`: Básicamente, `git fetch` y `git merge` al mismo tiempo.
* `git grep "{palabra}"`: Busqueda de palabras en archivos
    * `git grep -n "{palabra}"`: Indica la linea en donde esta la palabra dentro del archivo.
    * `git grep -c "{palabra}"`: Cuneta las palabras en los diferentes archivos.

## Log avanzados para trabajo remoto

* `git log` 
    * `--oneline`:Te muestra el id commit y el título del commit.
    * `--decorate`: Te muestra donde se encuentra el head point en el log.
    * `--stat`: Explica el número de líneas que se cambiaron brevemente.
    * `-p`: Explica el número de líneas que se cambiaron y te muestra que se cambió en el contenido.
    * `--graph --oneline --decorate` o `--pretty=format:"%cn hizo un commit %h el dia %cd"` Muestra mensajes personalizados de los commits.
    * `-{n}`: Limitamos el número de commits a `n`.
    * `--after=“2018-1-2”` o `--after=“today”` o `--after=“2018-1-2”` o `--before=“today”`: Commits para localizar por fechas.
    * `--author=“Name Author”`: Commits hechos por autor que cumplan exactamente con el nombre.
    * `--grep=“INVIE”`: Busca los commits que cumplan tal cual está escrito entre las comillas.
    * `--grep=“INVIE” –i`: Busca los commits que cumplan sin importar mayúsculas o minúsculas.
    * `{nombre_archivo}`: Busca los commits en un archivo en específico.
    * `-S “Por contenido”`: Buscar los commits con el contenido dentro del archivo.
* `git log > log.txt`: guardar los logs en un archivo txt
* `git shortlog`: Indica que commits ha realizado un usuario, mostrando el usuario y el título de sus commits.