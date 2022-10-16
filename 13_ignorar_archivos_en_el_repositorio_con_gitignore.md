# Ignorando archivos en el repositorio con `.gitignore`

Por lo general, los archivos binarios (`.jpge`, `.docx`, `.mp3`, etc) o archivos con informacion sensible (contrasenhas, nombres, numeros de identificacion, etc) no deben ser sometidos a un control de versiones, por lo tanto, es necesario indicarle a git que ignore estos archivos con un archivo que se debe alojar en la raiz del proyecto y se llama `.gitignore`.

Un ejemplo de lo que debe tener este archivo es:

```
# Ignorar imagenes
*.jpge

# No ignorar contenido
!README.md
```

* Lo que empiece por `#` es un comentario
* Lo que empiece por `!` __NO__ se ignora, util si se quiere hacer un filtro selectivo de ficheros en carpetas.