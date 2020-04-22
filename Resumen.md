# Resumen

## Configurar Git

```bash
# --global para configuracion global, --local para configuracion local de un repositorio
git config --global user.name "Tu Nombre"

git config --global user.email ejemplo@ejemplo.ej

git config --list # Listar configuracion
```

## Crear repositorio

```bash
git clone link/to/repository # Clonar repositorio ya existente en link/to/repository

git init # Iniciar repositorio local en localizacion actual

git remote add origin link/to/repository # Asicuar un link a un repositorio a mi repositorio local

```

## Actualizar cambios

```bash
git status # ver qué cambios, archivos nuevos, archivos eliminados no han sido añadidos al área de staging o de confirmación.

git add . # Añadir cambios de todos los archivos al área de staging
git add path/to/file # Añadir cambios de archivo específico al área de staging
git commit # Commitear (confirmar) cambios de el área de staging. Se solicitará que se ingrese un mensaje de commit que puede tener varias lineas, la primera línea debe ser un resumen, añadir más descripción solo de ser necesario.

git commit -m "Mensage de commit" # Commit pero colocando el mensaje inmediatamente.

git push origin <branch-name> # Pushear cambios commiteados a la rama especificada.
```

También puedes usar ```git stash`` si deseas descartar los cambios, guardandolos para después.

## Traer datos del remoto
```bash
git fetch # descarga datos de todas las ramas de el remoto.

git pull # descarga estado en el remoto de la rama actual
```
<!-- Pendiente = hacer resumen de staging -->
## Branching
```bash
git branch # Mostrar todas las ramas existentes localmente
git branch -r # Mostrar todas las ramas existentes en el remoto
git branch -a # Mostrar todas las ramas existentes tanto localmente como en el remoto
git branch --merged # Muestra ramas que están o no mergeadas con la rama actual
git branch --no-merged
git branch <nombre-rama> # crear rama nombre-rama
git branch -d <nombre-rama> # eliminar rama especificada
git branch -d -r <nombre-rama> # eliminar rama en el remoto

git checkout <nombre-rama> # Ubicarse en la rama especificada
git checkout -b <nombre-rama> # crea la rama especificada e inmediatamente se ubica en ella.
git checkout

git branch -m <nombre-rama> <nuevo-nombre> # Cambiar nombre rama
```

## Merging
```bash
git merge <nombre-rama> # Mergea nombre-rama en la rama actual
```

Luego de mergear se deberán resolver conflictos (si existen), añadir cambios y commitear.