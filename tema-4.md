# TEMA 4: RAMAS, UNIONES, CONFLICTOS Y TAGS

Tipos de uniones o merges:
- Fast-fordward
- Unión automática
- Uniones con conflictos

# Merge fast-forward
Cuando hacermos cambios en la rama secundaria y no tocamos la principal. No hay interferencias entre ambas.

1. git branch > para ver la ramas
2. git branch nombreRAma > para crear una rama nueva
3. git chekout nombreRama > para cambiar de rama

* Hago un par de commits en esa rama

4. git diff ramaActual ramaMain > para ver las diferencias
5. git checkout ramaMain > para cambiar a la rama principal donde quiero realizar la unión. (Para realizar el merge tengo que estar en la rama en la que quiero que este se realize).
6. git merge ramaSecundaria > para mergearlas

7. git branch -d(delete) ramaSecundaria

# Merge automatico
Ocurre cuando realizamos cambios en la rama principal Y en la secundaria. Pero los cambios de una no interfieren con los de la otra (no son el mismo archivo, no son las mismas lineas).

1. Creas una rama y haces unos comits
2. Comaas a la master y añades algun comit
3. Mergeas ramas > metes el commit
4. Git te fuciona las ramas de manera automática y te lo muestra en su gráfico.

# Merge con conflito

* Para esto necesitamos intelar un plugin (tener configurado) nuestro editor de texto, para verlo mejor.

Ocurren cuando realizamos cambios en la rama principal y en la secundaria. Y los cambios de una interfieren en la otra, es decir, se realizaron dentro del mismo archivo.

1. Hacemos cambios en la rama secundaria
2. Hacemos cambios en la rama principal

* Ambos cambios modivicaron un mismo archivo comun

3. git merge > no me va a dejar me indica un conflicto
4. Voy al archivo y soluciono el conflicto: eliminando etiquetas y guardando cambios como yo quiero que queden.

5. git status > para ver el estado
6. git commit (desde la rama padre) > para resolver el conflicto

7. git branch -d(delete) ramaSecundaria

# Tags
Un tag hace referencia a un commit y sirve para nombrar o establecer las versiones de nuestro proyecto.

- git tag -a(anotated) v1.0.0 -m "Version 1.0.0" > me inserta el tag en el último commit.
- git tag -a v0.1.0 commitId -m "Message" > para insertar un tag en un commit en concreto. 

- git tag > para ver la lista, info. general
- git log > para ver los commits con los tags
- git show (commitId) > para ver la información detallada de los tags