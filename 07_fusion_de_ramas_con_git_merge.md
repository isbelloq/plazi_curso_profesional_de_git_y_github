# Fucion de ramas con Git merge

* `git branch` Muestra las ramas creadas en git, se indica la rama de trabajo con un `*` al inicio.
* `git merge {nombre_rama}` Se hace la fusion de los cambios. __IMPORTANE__ El merge se hace desde el `nombre_rama` hacia la rama actual de trabjo, ie. Si estoy en `*main` y hago `git merge foo` entonces la rama `foo` se fusiona con `*main`