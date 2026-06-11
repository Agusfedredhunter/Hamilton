# git log

`git log` es el comando que usamos para ver el historial de commits del repositorio. Nos muestra quién hizo cada commit, cuándo, y qué mensaje dejó. Tiene muchas opciones para personalizar la salida según lo que necesitemos ver.

## Uso básico

git log

Por defecto muestra, para cada commit:
 El hash completo (identificador único del commit)
 El autor y su correo
 La fecha y hora
 El mensaje del commit

## Opciones más usadas

### --oneline

Muestra cada commit en una sola línea, con el hash abreviado y el mensaje. Es mucho más fácil de leer cuando hay muchos commits.


git log --oneline


### --graph

Muestra el historial como un gráfico en texto que representa las ramas y sus fusiones. Muy útil para ver cómo se relacionan las ramas entre sí.

git log --oneline --graph

### Combinaciones útiles

# Gráfico completo con todas las ramas
git log --oneline --graph --all

# Ver commits de un autor específico
git log --author="Nombre"

# Ver qué archivos cambió cada commit
git log --stat

## ¿Por qué es tan importante?

`git log` es fundamental para entender qué pasó en el proyecto: quién hizo qué y cuándo. También es el punto de partida para obtener los hashes que necesitamos para comandos como `git revert`, `git checkout` o `git commit --fixup`.
