# TEMA 5: STASH & REBASE

# STASH 
Es como una caja fuerte para dejar un proyecto aparcado y luego volver a el más tarde.

1. Realizo cambios en un archivo.
2. git stash > me crea una "rama" guardando los cambios hasta donde estaba.

# Para ver las ramas
- git log
- git stash

3. Realizo otra modificación
4. git commit
5. git log >> para ver como va el asunto

6. git stash pop > 
    - Agarra los cambios del stash y me los incluye al stage.
    - Elimina la "rama" del stash
7. git commit > para guardar los cambios del stash en la rama main.

Listo!

# CONFLICTOS CON EL STASH
Ocurre cuando modificamos los mismos archivos/lineas antes y despues del stash (como en el merge coflict).

1. Hago cambios
2. git stash
3. Realizo cambios en el mismo archivo
4. git stash pop > conflicto
5. Reolver el conflicto llendo al archivo (igual que con las ramas)
6. git stash grop > para eliminar la "rama" del stash, aquí no se nos elimina uatomáticamente.

# MÁS INFORMACIÓN SOBRE GIT STASH
Amplia los comandos sobre el stash (con muchos más). Si lo necesitas en el futuro hechale un ojo.

# REBASE 
Se utiliza para avanzar una rama secundaria en el tiempo de los commits de la rama principal. Esto evita muchos conflictos entre las ramas.

Es muy util > ai necesitas más info vete al video.

1. git checkout secondBranch
2. git rebase mainBranch
3. git checkout mianBranch
4. git merge secondBranch
5. got brach -d(delete) secondBranch

# REBASE INTEREACTIVO - SQUASH
- Sirve para unir/mergear commits en uno solo.

1. git rebase -i(interactive) HEAD~4(ultimos 4 commits)
2. change pick for sqush
3. Add message

Done!

# REWORD 
- Para renombrar x commit.

# EDIT
- Sirve para separar el commit. Es decir, si commiteamos dos archivos, separarlos y enviar un archivo a un comit y el otro a otro.
- No es complicado pero es un poco largo, miratelo del video si lo necesitas.
 