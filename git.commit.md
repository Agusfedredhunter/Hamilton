# Comandos de Git

## Git commit

El comando `git commit` es uno de los comandos fundamentales de Git. Se utiliza para guardar los cambios que fueron previamente agregados al área de staging mediante `git add`, registrándolos de forma permanente en el historial del repositorio.

Cada commit funciona como una "foto" del estado del proyecto en un momento determinado. Para que quede claro qué se hizo en cada commit, es obligatorio acompañarlo de un mensaje descriptivo: `git commit -m "mensaje"`.

En este trabajo seguimos la convención de **Conventional Commits**, lo que significa que los mensajes tienen un formato estándar según el tipo de cambio realizado. Por ejemplo: `feat: agregar explicación de git log` para una nueva funcionalidad, `fix: corregir typo en rebase.md` para una corrección, o `style: formatear tabla en indice.md` para cambios de formato.

---

## Git commit --fixup

El comando `git commit --fixup <hash>` es una variante de `git commit` que se utiliza para marcar un commit como corrección de otro commit anterior específico. En lugar de escribir un mensaje manualmente, Git genera automáticamente uno con el formato `fixup! <mensaje del commit original>`.

Para usarlo, primero hay que obtener el hash del commit que se quiere corregir mediante `git log --oneline`, y luego ejecutar `git commit --fixup <hash>` apuntando a ese hash.
