# Indice del grupo 9. 

## Mienbros: 
|                            | Commits | Conflicts | Ramas          | Merges |
|----------------------------|---------|-----------|----------------|--------|
| Fedigatti Augusto Mario    |    15   |           |Alumno_Fedigatti|   3    |
| Moore Andy                 |    4    |           |Alumno_Moore    |   2    |  
| Urdampilleta Iñaki         |    6    |           |Alumno_Urdampill|   3    |
| Pelizza De La Orden Joaquin|   50    |     8     |Alumno_Pelizza  |   5    |

---

Como es especifica en las indicaciones del trabajo practico, aqui es donde estan las listas de los comandos del **Git** que se han aprendido en la clase de **Metodologia 1** de la UTN. 

Integrante que realizó la mayor cantidad de commits, indicando dicha
cantidad:
usé el comando git shortlog -sn, y me soltó esto:
 50  JoaquinPelizza
 15  Agusfedredhunter
 6  Iñaki Urdampilleta
 4 Andy Moore
solo que con nombres de vsc y algunos otros con el de git.

para cantidad total de merges realizados:
usé git log --oneline --merges | Measure-Object -Line
y git log --merges --format="%an" | Group-Object | Select-Object Count, Name | Sort-Object Count -Descending
me soltó:
    8 JoaquinPelizza
    3 Iñaki Urdampilleta
    2 andymoore01
    1 Sango(augusto)             
para cantidad de conflictos producidos:
agarré el texto que copié de la terminal de todos los conflictos y le pedí a la IA que los cuente(lo notifiqué en IA.md) y le sumé el otro que arreglé con git revert y me dá 8 conflictos.

para cantidad de ramas existentes en el repositorio:
git branch -r | Measure-Object -Line
me soltó 14

para commit con la mayor cantidad de archivos modificados, especificando el
hash, la cantidad de archivos involucrados y una captura del diff
correspondiente a los cambios.
usé git log --format="%H" | ForEach-Object { $hash = $_; $count = (git diff-tree --no-commit-id -r $hash | Measure-Object -Line).Lines; "$count $hash" } | Sort-Object -Descending | Select-Object -First 1
me soltó el commit con hash d86853fcca665cf20df189ee9a878f2d80b44bbd que modificó 3
<img width="1242" height="80" alt="image" src="https://github.com/user-attachments/assets/8429dcbc-0124-44fc-9646-8ae1e2572211" />

para captura de un conflicto previo a su resolución, indicando el hash del
commit asociado guardé esta captura que es del primer conflicto:
<img width="1518" height="995" alt="Captura de pantalla 2026-06-11 184534" src="https://github.com/user-attachments/assets/c6bebc1d-c456-4795-98f3-e5b591c3acab" />

 
