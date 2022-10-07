# Comandos basicos git

* `git init` Inicializa el repositorio
* `git status` Muestra el estado actual del repositorio
* `git add {archivo}` Agrega un archivo al _stage_ del repositorio, se puede usar `.` para agregar todos los archivos
* `git rm --cached {archivo}` Elimina el archivo del _stage_
* `git commit [-m "Mensaje"] {archivo}` Envia el archivo al repositorio con un mensaje
* `git config` Muestra la configuracion de git
    * `--list` Lista las diferentes opciones de de configuracion
        * `--show-origin` Muesta las rutas de almacenamiento de los archivos de configuracion
    * `--global` Modificacion de configuracion global
        * `user.name` Configuracion del nombre
        * `user.email` Configuracion del email
* `git log {archivo}`: Muestra el historial de cambios de un archivo
