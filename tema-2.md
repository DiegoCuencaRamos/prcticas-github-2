# TEMA 2: FUNDAMENTALS

- git help (nombre comando - específico)
# Crear repositorio local
- git init

# Básicos
- git status (-s: silent -b: branch)
- git add [., "*.png" (todos), *.png, css/*.css, css/, nombreArchivo] > añadir al stage
- git reset [., *.png, css/, nombreArchivo] > eliminar del stage
- git commit -m "Message"

# Reconstruye el proyecto en el último commit :)
- git checkout -- [., nombreArchivo]

# Log all commits (cronologically desc. order)
- git log (--oneline --decorate --all --graph) 

# Crear alias
- git config --global aslias.aliasName "git log --online...: the command to execute"
- git config --global -e > para ver los alias y editarlos
- git config --global -l > para ver solo el listado de aliases



# TEMA 3: ADVANCED FUNDAMENTALS
- git diff > para ver las diferencias en el stage

# Actualizar el mensaje de commit y revertir cambios
- git commit --amend -m "Mensage"
- git reset --soft [HEAD^ (ultimo comit),commitId]

# Resetear cambios del commit
- git reset --soft commitId > no elimina los archivos, solo los deja fuera del stage.
- git reset --hard commitId > elimina los archivos y los commits desde ese en adelante.
- git reflog > para ver todo el historial de commits, incluso los "eliminados"
- git reset --hard commitId > nos lo trae todo de vuelta.

(Reset el como que resetea cambia el punto en el que estes a la iversa)

#  Renombrar y eliminar archivos nediante Git
- git mv(move) nombreArchivoActual NombreArchivoActualizado 
    - Ventaja: renombras el archivo y no pierdes el historial de git del trackeado de ese archivo (si lo renombras manualmente si, porque aparece como nuevo).
- git status
- git commit -m "..." > para guardar renombrado

- git rm nombreArchivo
- git status
- git commit -m "..." > para guardar borrado

# Renombrar y eliminar archivos fuera de Git
1. Renombramos eliminamos el archivo
2. git status
3. git add -u(update) > para actualizar los cambios
4. git status > para ver que nos coje el nuevo status
5. git commit -m "Archivo renombrado/eliminado"

# Ignorando archivos
.gitignore
