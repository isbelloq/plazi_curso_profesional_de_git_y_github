# `git stash`: guarda cambios en memoria y recuperalos despues

El _stashed_ nos sirve para guardar cambios para después, Es una lista de estados que nos guarda algunos cambios que hicimos en Staging para poder cambiar de rama sin perder el trabajo que todavía no guardamos en un commit.

Ésto es especialmente útil porque hay veces que no se permite cambiar de rama, ésto porque tenemos cambios sin guardar, no siempre es un cambio lo suficientemente bueno como para hacer un commit, pero no queremos perder ese código en el que estuvimos trabajando.

El stashed nos permite cambiar de ramas, hacer cambios, trabajar en otras cosas y, más adelante, retomar el trabajo con los archivos que teníamos en Staging, pero que podemos recuperar, ya que los guardamos en el Stash.


* `git stash` El comando git stash guarda el trabajo actual del Staging en una lista diseñada para ser temporal llamada Stash, para que pueda ser recuperado en el futuro.
    * `list`: Lista de todos los cambios realizados.
    * `save "mensaje identificador del elemento del stashed"`: poner un mensaje en el stash.

    * `pop`: El método pop recuperará y __sacará__ de la lista el último estado del stashed y lo insertará en el staging area.
        * `stash@{<num_stash>}` _los corchetes `{}` son necesarios_: Para aplicar los cambios de un stash específico y eliminarlo del stash.
    * `apply stash@{<num_stash>}`: El método apply recuperará y __no saca__ de la lista y lo insertará en el staging area.
    * `branch <nombre_de_la_rama>`: Para crear una rama y aplicar el stash más reciente.
        * `stash@{<num_stash>}`: crear una rama con el stash especificado.
    * `drop`: eliminar los cambios __más recientes__ dentro del stash.
        * `stash@{<num_stash>}`: se elimina el stash especifico.
    * `clear`: elimina __todos__ los stash en la lista.


> Consideraciones:
> * El cambio más reciente (al crear un stash) SIEMPRE recibe el valor 0 y los que estaban antes aumentan su valor.
> * Al crear un stash tomará los archivos que han sido modificados y eliminados. Para que tome un archivo creado es necesario agregarlo al Staging Area con git add [nombre_archivo] con la intención de que git tenga un seguimiento de ese archivo, o también utilizando el comando git stash -u (que guardará en el stash los archivos que no estén en el staging).
> * Al aplicar un stash este no se elimina, es buena práctica eliminarlo.