# Creando un Fork, contribuyendo a un repositorio

* `git remote -v` Muestra los repositorios remotos con las url
* `git remote add upstream <url_del_remoto>` En caso de fork, se agrega una nueva localizacion remota, usualmente se llama `upstream`

Los pasos para sincronizar un repositorio Fork son:
1. `git pull upstream main` Sincronizacion de la rama principal del repo origial a mi repo local.
2. `git commit -am "{Mensaje}"` Crear commit con los cambios realizados.
3. `git push origin main` Subir los cambios al repo del Fork.
