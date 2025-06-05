## Commits

### 1.1. Preguntas

1. **¿Cómo se inicializa un repositorio local? (qué comando se debe ejecutar?)**  
   `git init`

2. **¿Cómo hago para que un directorio deje de ser controlado por git? (qué comando se debe ejecutar?)**  
   `rm -rf .git`

3. **Si agrego un archivo a un directorio que ya está siendo controlado por git, ¿está siendo controlado por git?**  
   No, el archivo no estará siendo controlado por Git hasta que se ejecute el comando `git add <nombre_del_archivo>` para agregarlo al área de preparación (staging area).

4. **¿Qué comando se utiliza para agregar un archivo al repositorio local?**  
   `git add <nombre_del_archivo>`

5. **¿Cómo determino qué archivos fueron modificados? (qué comando se debe ejecutar?)**  
   `git status`

6. **¿Qué comando se utiliza para hacer un commit?**  
   `git commit -m "mensaje del commit"`

7. **En sus propias palabras, ¿qué es un commit?**  
   Un commit es una instantánea del estado actual del proyecto en un momento dado. Al hacer un commit, se guardan los cambios realizados en los archivos del repositorio, junto con un mensaje que describe esos cambios. Esto permite llevar un historial de modificaciones y facilita la colaboración en proyectos.

## 1.2. Ejercicio Práctico

1. **Crear archivo nombre_apellido.txt**   
Este paso es simple, puedes usar:
`touch JuanFran_CarrteroValle.txt`

2. **Editar sandwich.txt**   
Puedes usar un editor de texto o el comando echo:
`echo "Pan integral
Jamón
Queso
Lechuga
Tomate" > sandwich.txt`

3. **Guardar estado del git status**   
Ejecutar:
`git status >> JuanFran_CarreteroValle.txt`
La salida mostrará archivos sin seguimiento (untracked files)
y cambios no confirmados (unstaged changes)

4. **Agregar sandwich.txt al staging**   
`git add sandwich.txt`
Este comando prepara el archivo para ser commiteado

5. **Verificar cambios en status**   
`git status`
Ahora verás el archivo en "Changes to be committed"
El archivo pasó de untracked a staged

6. **Realizar primer commit**   
`git commit -m "Agrego mi sandwich.txt"`
Esto crea el primer punto de control en la historia

7. **Verificar nuevo status**   
`git status`
Ahora debería mostrar "working tree clean"

8. **Agregar salsas y nuevo commit**   
`echo "Mayonesa
Mostaza
Salsa picante" >> sandwich.txt`
`git add sandwich.txt`
`git commit -m "Agrego salsas"`

9. **Revisar historial**   
`git log >> JuanFran_CarreteroValle.txt`
Los commits aparecen en orden cronológico inverso
(más reciente primero)

10. **Variaciones de git log**   
10.1 **Formato compacto**   
`git log --oneline`
10.2 **Ver estadísticas de cambios**   
`git log --stat`

11. **Comparar commits**   
Usar los hashes de los commits:
`git diff <hash-commit1> <hash-commit2>`
En Windows:
`git difftool --tool=meld <hash>`
En Linux:
`git difftool --tool=opendiff <hash>`

12. **Crear segundo archivo**   
`echo "Pan de centeno
Atún
Aguacate" > sandwich2.txt`

13. **Agregar al repositorio**   
`git add sandwich2.txt`
`git commit -m "Agrego sandwich2.txt"`

14. **Renombrar archivo**   
`git mv sandwich2.txt sandwich2_feo.txt`
`git commit -m "Renombro sandwich2 a sandwich2_feo"`
El status mostrará el archivo como renamed

15. **Borrar archivo**   
`git rm sandwich2_feo.txt`
`git commit -m "Elimino sandwich2_feo"`
El status mostrará el archivo como deleted

16. **Revisar historial completo**   
`git log --stat`
Mostrará todos los cambios con estadísticas
incluyendo archivos añadidos, renombrados y eliminados
