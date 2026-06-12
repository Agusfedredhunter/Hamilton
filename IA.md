Usamos la IA para pedirle los comandos que se pedía en la consigna, estos són:
- git shortlog -sn --all
- git log --oneline --merges | Measure-Object -Line
- git log --merges --format="%an" | Group-Object | Select-Object Count, Name | Sort-Object Count -Descending
- git branch -r | Measure-Object -Line
- git log --format="%H" | ForEach-Object { $hash = $_; $count = (git diff-tree --no-commit-id -r $hash | Measure-Object -Line).Lines; "$count $hash" } | Sort-Object -Descending | Select-Object -First 1
- git show (el hash)

Luego usamos la IA para confirmar comandos hechos en el trabajo con el fin de estar seguro de nuestras elecciones.
También se usó para inspirarnos para soluciones de conlfictos a partir del segundo al último pero al final hicimos una solución que se le ocurrió a cierto integrante.
