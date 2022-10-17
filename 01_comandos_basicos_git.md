# Comandos basicos git

* `git init` Inicializa el repositorio
* `git status` Muestra el estado actual del repositorio
* `git add {archivo}` Agrega un archivo al _stage_ del repositorio, se puede usar `.` para agregar todos los archivos
* `git rm --cached {archivo}` Elimina el archivo del _stage_
* `git commit [-m "Mensaje"] {archivo}` Envia el archivo al repositorio con un mensaje
    * `git commit --amend`: Es el remiendo de un commit, el commit que se genera se agrega al commit anterior.
* `git config` Muestra la configuracion de git
    * `--list` Lista las diferentes opciones de de configuracion
        * `--show-origin` Muesta las rutas de almacenamiento de los archivos de configuracion
    * `--global` Modificacion de configuracion global
        * `user.name "{Nombre}"` Configuracion del nombre
        * `user.email {email}` Configuracion del email
        * `--replace-all user.name {nombre}` Se reemplaza el nombre en caso de errores.
        * `--unset-all user.name` Elimina el nombre del usuario
* `git log {archivo}`: Muestra el historial de cambios de un archivo
