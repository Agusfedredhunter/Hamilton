# Indice del grupo 9. 

## Mienbros: 
|                            | Commits | Conflicts | Ramas          | Merges |
|----------------------------|---------|-----------|----------------|--------|
| Fedigatti Augusto Mario    |    3    |           |Alumno_Fedigatti|   01   |
| Moore Andy                 |    0    |           |                |        |  
| Urdampilleta Iñaki         |    0    |           |                |        |
| Pelizza De La Orden Joaquin|    0    |     1     |Alumno_Pelizza  |        |

---

Como es especifica en las indicaciones del trabajo practico, aqui es donde estan las listas de los comandos del **Git** que se han aprendido en la clase de **Metodologia 1** de la UTN. 

## Conflictos:
hubo solo un conflicto en el que se intentó pushear dos commits que se contradecian al mismo tiempo, por lo que se hizo un git revert para solucionar el error y dejarlo como estaba antes del conflicto con la intención de arreglarlo.

## Conteo de ramas:
Para determinar la cantidad de ramas usé los comandos:
#  "git branch -a | Measure-Object -Line"
Que determina la cantidad de ramas, y el comando
# "git branch -a"
Para determinar los nombres de las ramas y confirmar que esté todo bien porque el primer comando daba un número para mí raro.
pero me soltó estas ramas:
origin/Alumno_Fedigatti
origin/Alumno_Moore
origin/Alumno_Pelizza
origin/Alumno_Urdampilleta
origin/HEAD
origin/dev
origin/main
Osea que si no contamos la rama head tenemos 6 ramas en este repositorio.

