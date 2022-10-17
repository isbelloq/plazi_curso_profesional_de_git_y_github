# `git clean`: limpiar tu proyecto de archivos no deseados

El comando `git clean` __borra los archivos__ los archivos nuevos que no se han agregado al area de stagin. Este comando es util para borrar logs de ejecucion, resultados de compilacion, metadatos de documentos, entre otros archivos generados. 

El comando debe estar acompanado de parametros de ejecucion ya que es un comando que __elimina archivos__ que no estan dentro del repositorio y __no hay forma de recuperarlos__, algunos de los mas usados son:

* `git clean --dry-run`: Simula la ejecucion del comando y muestra que archivos se eliminaran si se ejecuta la accion
    > Dato curiso: La exprecion _dry run_ se usa cuando se prueban los barcos antes de navegar.
* `git clean -f`: Borra los archivos que no tengan seguimiento, pero se negara a borrar directorios o subdirectorios que no tengan seguimiento. Ejemplo: si tengo `dir1/a.txt`, `dir1/b.txt` y `dir1/a.txt` esta dentro del repositorio, entonces `dir1/b.txt` se eliminara, pero si tengo `dir2/foo.txt` y esta ruta nunca a sido agregada al repositorio, entonces `dir2/foo.txt` no es eliminara.

* `git clean -fd`: Borra los archivos que no tengan seguimiento incluyecto a los directorios y subdirectorios. Tomando el ejemplo anterior, en ese caso `dir2/foo.txt` si se eliminara.

> Nota: No se borraran archivos que ya esten dentro de `.gitignore` ya que no son visibles en git.