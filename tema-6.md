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

# Tags
Para subir los tags que teníamos en nuestro proyecto, github no lo hace de manera automática, tenmos que ordenarselo manualmente:

- git push --tags

# Pull
Son buenas prácticas hacerlo cada vez que volvemos a trabajar.

# Clone
1. Ir al repositorio en gitHub
2. Cliclar clonar repositorio
3. Copiar URL (HTTP || SSH)
4. git clone <URL> <repositoryName: (opcional - el que tu quieras)>

# Fetch & Pull
Como buenas prácticas es aconsejable realizar un git fetch / pull antes de realizar un git push.
De esta manera, nos aseguramos de que nuestro proyecto local esta en consonancia con el repositorio remoto, antes de subir nuestros cambios.

- git fetch es una via menos agresiva que git pull (que lo que hace es un mergeado automático)
> para realizarlo, revisa el video si necesitas.
