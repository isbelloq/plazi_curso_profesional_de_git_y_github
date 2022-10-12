# Resolucion de conflictos al hacer un merge

Un conflicto se genera cuando dos lineas de codigo son modificadas en dos ramas diferenes. Para solucionar este conflicto es neceario:

1. Se realiza un `git merge {rama}`, esta accion generara la alerta de conflicto que se ve como
    ```sh
    Auto-merging {archivo}
    CONFLICT (content): Merge conflict in {archivo}
    Automatic merge failed; fix conflicts and then commit the result.
    ```
2. Al abrir el editor el conflicto se ve de la siguiente forma en el archivo
    ```
    <<<<<<< HEAD
    {texto en rama actual}
    =======
    {texto en rama a fusionar}
    >>>>>>> {rama}
    ```
    Para solucionar el conflicto se debe modificar manualmente el problema, por ejemplo
    ```
    {texto en rama a fusionar}
    ```
    > Nota:  VSCode tiene una ayuda que hace la vida mas facil

3. Terminada la resolucion del conflicto, es decir, la modificacion del texto es necesario hacer un `git commit -am` documentando los cambios realizados.


