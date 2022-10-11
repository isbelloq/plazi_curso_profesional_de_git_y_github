# Volver en el tiempo en nuestro repositorio utilizando reset y checkout

* `git reset {id}` Se devuelve el repositorio al estado definido por el id
    * `git reset {id} --hard` Todo se devuleve al estado anterior
    * `git reset {id} --soft` Se devuelve a la version anteior pero se mantiene los cambios en el staging, es decir lo que se agrego con `git add`
* `git diff` Muestra las diferencias entre el codigo en stagin el el ultimo commit.
* `git log --stat` Muestra las estadisticas de los cambios.
* `git checkout {id} {archivo}` Se devuelve al estado `{id}` del `{archivo}` seleccionado.
    * `git checkout main {archivo}` Se devuelve al `main` del `{archivo}` seleccionado.