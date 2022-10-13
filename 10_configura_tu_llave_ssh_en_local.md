# Configura tu llave SSH en local

Para crear una conexion segura con GitHub se recomienda crear una llave SSH para la comunicacion entre Git (local) y GitHub (remoto). Los pasos a seguir son:

1. Crear la carperta `.ssh` y entrar en ella
    ```sh
    mkdir ~/.ssh
    cd ~/.ssh
    ```
2. Crear la pareja de llave publica-llave privada
    ```sh
    ssh-keygen -t ed25519 -C "your_email@example.com"
    ```
    La bandera `-t` es el tipo de algoritmo a usar para crear la llave y `-C` el e-mail al cual se va a enlazar.

    Al correr este comando se realiza el proceso de creacion de la llave es necesario seguir las instrucciones.

3. Encender el sevirdor de llaves SSH
    ```sh
    eval $(ssh-agent -s)
    ```

    y anadir la llave al servidor

    ```sh
    ssh-add ~/.ssh/{nombre_llave}
    ```

    > Nota: se debe agregar la llave privada, no la publica

4. Crear el archivo `~/.ssh/config` con la siguiente informacion
    ```sh
    Host github.com
        HostName github.com
        IdentityFile ~/.ssh/{nombre_llave}
    ```
5. Copiar la llave `{nombre_llave}.pub` en el almacen de contrasenas de GitHub