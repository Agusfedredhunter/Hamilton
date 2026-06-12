# git rebase

`git rebase` es el comando que usamos para reescribir el historial de commits, moviendo o reorganizando commits de una rama sobre otra. A diferencia de `git merge`, que une dos ramas creando un commit de fusión, `git rebase` "reaplica" los commits uno por uno, logrando un historial más lineal y limpio.

## Uso básico


# Reescribe la rama actual sobre otra rama
git rebase main

# Rebase interactivo: permite editar, reordenar, fusionar o eliminar commits
git rebase -i HEAD~3


## Rebase interactivo (-i)

El rebase interactivo abre un editor donde podemos modificar los últimos commits.


## ¿Cuándo usar rebase en lugar de merge?

 Usamos rebase cuando queremos un historial limpio y lineal, especialmente antes de integrar una rama al proyecto.
 Usamos merge cuando queremos conservar el registro exacto de cuándo se unieron las ramas.

No se debe hacer rebase de commits que ya fueron subidos y compartidos con otros, ya que reescribe el historial y puede generar conflictos para el resto del equipo.
