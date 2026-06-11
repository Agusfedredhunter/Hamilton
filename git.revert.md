# Comandos de Git

## Git revert

El comando `git revert <hash>` se utiliza para deshacer los cambios introducidos por un commit anterior, pero sin eliminar ese commit del historial. En vez de borrarlo, Git crea un nuevo commit que aplica exactamente los cambios seleccionados, dejando registro de que se realizó una reversión.

Para usarlo, primero hay que identificar el hash del commit que se quiere revertir con `git log --oneline`, y luego ejecutar `git revert <hash>`. Git va a abrir el editor para confirmar el mensaje del nuevo commit, aunque esto puede evitarse agregando la opción `--no-edit`.

La principal ventaja de `git revert` por sobre otros métodos de deshacer cambios es que es seguro para usar en ramas compartidas con otros integrantes del equipo, ya que no reescribe el historial existente.
