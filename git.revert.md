# Comandos de Git

## Git revert

El comando `git revert <hash>` se utiliza para deshacer los cambios introducidos por un commit anterior, pero sin eliminar ese commit del historial. En vez de borrarlo, Git crea un nuevo commit que aplica exactamente los cambios seleccionados, dejando registro de que se realizó una reversión.

Para usarlo, primero hay que identificar el hash del commit que se quiere revertir con `git log --oneline`, y luego ejecutar `git revert <hash>`. Git va a abrir el editor para confirmar el mensaje del nuevo commit, aunque esto puede evitarse agregando la opción `--no-edit`.

La principal ventaja de `git revert` por sobre otros métodos de deshacer cambios es que es seguro para usar en ramas compartidas con otros integrantes del equipo, ya que no reescribe el historial.

Otras variaciones con un efecto parecido al Git revert, pero que editan la historia del repo son:

## Git reset --soft

El comando `git reset --soft <hash>` mueve el puntero `HEAD` al commit indicado, deshaciendo los commits posteriores, pero conservando todos los cambios de esos commits en el índice. Esto significa que los archivos modificados quedan listos para ser confirmados nuevamente con `git commit`.

Al igual que `git reset --hard`, este comando reescribe el historial, por lo que debe usarse con precaución en ramas compartidas con otros integrantes del equipo.

## Git reset --hard

El comando `git reset --hard <hash>` mueve el puntero `HEAD` al commit indicado y descarta por completo todos los cambios posteriores, tanto del indice como del directorio de trabajo. Los archivos vuelven exactamente al estado en que estaban en ese commit.

Este comando es irreversible en la práctica: los cambios descartados no pueden recuperarse fácilmente. Por eso, debe usarse con precaución y nunca en ramas compartidas con otros integrantes del equipo, ya que reescribe el historial.