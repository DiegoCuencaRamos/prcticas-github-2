# TEMA 6: GITHUB, GIT REMOTE, PUSH & PULL

- Git demote > es un repositorio remoto a nuestro ordenador donde almacenamos nuestro proyecto, para guardarlo a salvo. Ej.: gitHub

- push > orden para enviar archivos a nuestro repositorio

- pull > orden para descargar los archivos del repositorio

# Iniciando un proyecto

1. git remote add origin https://...
    - remote: indicamos que vamos a añadir un repositorio remoto a nuestro ordenador.
    - origin: indicamos el nombre del repositprio remoto.
    - indicamos la URL de ese repositorio

2. git push -u origin main
    - indicamos que desde nuestra rama main vamos a puhear a origin (gitHub)
    - -u: indicamos que esta va a ser la rama por defectoa la que vamos a pushear. Nos permite no tener que volver a escribirlas.