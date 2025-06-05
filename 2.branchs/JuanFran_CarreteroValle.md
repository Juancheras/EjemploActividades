## 2. Branchs

### 2.1. Preguntas

1. **¿Qué es un branch?**  
   Un branch (rama) es una línea de desarrollo independiente en un repositorio de Git. Permite trabajar en diferentes características o correcciones de errores de forma aislada sin afectar la rama principal (generalmente master o main).

2. **¿Por qué pueden ser útiles los branches?**  
   Los branches son útiles porque permiten:
   a. Desarrollar nuevas características sin afectar el código estable.  
   b. Realizar pruebas de cambios sin comprometer la rama principal.  
   c. Facilitar la colaboración en equipo, permitiendo que múltiples desarrolladores trabajen en diferentes tareas simultáneamente.

3. **¿Cómo se crea una branch?**  
   `git branch <nombre_de_la_branch>`

4. **¿Cómo se cambia a una branch?**  
   `git checkout <nombre_de_la_branch>`

5. **¿Cómo se elimina una branch?**  
   `git branch -d <nombre_de_la_branch>`

6. **¿Cómo se crea una branch y se cambia a ella en un solo paso?**  
   `git checkout -b <nombre_de_la_branch>`

7. **¿Qué es un merge?**  
   Un merge es el proceso de combinar los cambios de dos branches diferentes en uno solo. Esto permite integrar las contribuciones realizadas en una branch a otra.

8. **¿Cómo se realiza un merge?**  
   Para realizar un merge, primero se debe estar en la branch de destino (por ejemplo, master) y luego usar el comando:  
   `git merge <nombre_de_la_branch_a_mergear>`

9. **¿Qué es un tag?**  
   Un tag es una referencia que apunta a un commit específico en el historial de Git. Se utiliza comúnmente para marcar versiones de lanzamiento o hitos importantes en el desarrollo del proyecto.

10. **¿Cómo se crea un tag?**  
    `git tag -a <nombre_del_tag> -m "mensaje del tag"`

### 2.2. Ejercicio Práctico

1. **Configurar un Alias para Git**   
- **Comando:** `git config --global alias.graph "log --all --graph --decorate --oneline"`
- **Explicación:** Este comando crea un alias llamado `graph` que simplifica la visualización del historial de commits en Git. Al usar este alias, puedes ejecutar `git graph` para mostrar una representación gráfica de todos los commits, ramas y etiquetas en tu repositorio.

2. **Ejecutar el Comando del Alias**   
- **Comando:** `git graph`
- **Explicación:** Aquí, ejecutas el alias que acabas de crear. Esto te permite ver el historial de cambios de manera visual y más comprensible.

3. **Crear una Rama Nueva**   
- **Comando:** `git branch experimento master`
- **Explicación:** Este comando crea una nueva rama llamada `experimento` basada en la rama `master`. Esto es útil para trabajar en nuevas características sin afectar el código en la rama principal.

4. **Cambiar a la Nueva Rama**   
- **Comando:** `git checkout experimento`
- **Explicación:** Cambias de la rama actual a la rama `experimento` para comenzar a trabajar en ella.

5. **Verificar la Rama Actual**   
- **Comando:** `git branch`
- **Explicación:** Este comando muestra todas las ramas en el repositorio y resalta la rama en la que te encuentras actualmente. Te ayuda a confirmar que estás en la rama correcta.

6. **Modificar un Archivo**   
- **Acción:** Agregar "albahaca" arriba del "queso" en `2.branchs/pizza.txt`.
- **Explicación:** Estás editando un archivo de texto en tu proyecto para incluir un nuevo ingrediente en la receta de pizza.

7. **Commit de los Cambios**   
- **Comando:** `git commit -m "Agregar albahaca"`
- **Explicación:** Guardas los cambios realizados en el archivo, añadiendo un mensaje que describe lo que hiciste.

8. **Modificar el Archivo Nuevamente**   
- **Acción:** Agregar "oregano" arriba de "albahaca" en `2.branchs/pizza.txt`.
- **Explicación:** Realizas otra modificación en el mismo archivo para añadir otro ingrediente.

9. **Commit de los Nuevos Cambios**   
- **Comando:** `git commit -m "Agregar oregano"`
- **Explicación:** Guardas esta segunda modificación con un mensaje correspondiente.

10. **Visualizar el Historial de Ramas**   
- **Comando:** `git graph`
- **Explicación:** Vuelves a ejecutar el alias para ver cómo se han añadido tus commits en la rama `experimento`.

11. **Volver a la Rama Principal**   
- **Comando:** `git checkout master`
- **Explicación:** Cambias de nuevo a la rama `master` para continuar trabajando en ella.

12. **Crear Otra Rama**   
- **Comando:** `git checkout -b anana`
- **Explicación:** Creas y cambias a una nueva rama llamada `anana` en un solo paso.

13. **Modificar el Archivo en la Nueva Rama**   
- **Acción:** Agregar "anana" debajo del "queso" en `2.branchs/pizza.txt`.
- **Explicación:** Estás añadiendo otro ingrediente a la receta en esta nueva rama.

14. **Commit de los Cambios**   
- **Comando:** `git commit -m "Agregar anana"`
- **Explicación:** Guardas los cambios realizados en la rama `anana`.

15. **Visualizar el Historial de Ramas**   
- **Comando:** `git graph`
- **Explicación:** Observas cómo se ha modificado el historial de commits tras agregar el nuevo ingrediente en la rama `anana`.

16. **Volver a la Rama Principal**   
- **Comando:** `git checkout master`
- **Explicación:** Regresas a la rama `master` para realizar más cambios.

17. **Agregar Otro Ingrediente**   
- **Acción:** Agregar "cebolla" debajo de "salsa" en `2.branchs/pizza.txt`.
- **Explicación:** Modificas el archivo una vez más para incluir más ingredientes.

18. **Commit de los Cambios**   
- **Comando:** `git commit -m "Agregar cebolla"`
- **Explicación:** Guardas los cambios realizados en la rama `master`.

19. **Visualizar el Historial de Ramas**   
- **Comando:** `git graph`
- **Explicación:** Vuelves a ejecutar el alias para ver cómo se ha actualizado el historial de commits después de agregar la cebolla.

20. **Fusionar la Rama `anana` a `master`**   
- **Comando:** `git merge anana`
- **Explicación:** Combinas los cambios de la rama `anana` en la rama `master`, integrando el nuevo ingrediente.

21. **Visualizar el Historial de Ramas**   
- **Comando:** `git graph`
- **Explicación:** Observas cómo se ha integrado la rama `anana` en `master`.

22. **Ver Ramas Fusionadas a `master`**   
- **Comando:** `git branch --merged`
- **Explicación:** Este comando lista todas las ramas que han sido fusionadas a `master`, ayudándote a entender el estado de tu repositorio.

23. **Fusionar la Rama `experimento` a `master`**   
- **Comando:** `git merge experimento`
- **Explicación:** Integras los cambios de la rama `experimento` en la rama `master`.

24. **Visualizar el Historial de Ramas**   
- **Comando:** `git graph`
- **Explicación:** Vuelves a ver el historial para observar cómo se han fusionado los cambios de `experimento`.

25. **Determinar si se Requirió un Merge Manual**   
- **Pregunta:** ¿Tuvo que hacer un merge manual, o git lo hizo automáticamente? ¿Por qué?
- **Explicación:** Dependiendo de si hubo conflictos entre los cambios de las ramas, Git puede resolver automáticamente la fusión o requerir intervención manual.

26. **Ver Ramas Fusionadas a `master`**   
- **Comando:** `git branch --merged`
- **Explicación:** Nuevamente, verificas qué ramas han sido fusionadas a `master` tras la última fusión.

27. **Eliminar la Rama `anana`**   
- **Comando:** `git branch -d anana`
- **Explicación:** Eliminas la rama `anana` porque ya no es necesaria, ya que sus cambios han sido integrados en `master`.

28. **Eliminar la Rama `experimento`**   
- **Comando:** `git branch -d experimento`
- **Explicación:** Similarmente, eliminas la rama `experimento` por razones similares.

29. **Ver Ramas Fusionadas a `master`**   
- **Comando:** `git branch --merged`
- **Explicación:** Una vez más, compruebas el estado de las ramas fusionadas a `master`.

30. **Visualizar el Resultado**   
- **Comando:** `git graph`
- **Explicación:** Finalmente, observas el resultado final del estado del repositorio tras todas las fusiones y eliminaciones.

31. **Crear un Tag**   
- **Comando:** `git tag -a pizza -m "Receta de la pizza."`
- **Explicación:** Creas un tag llamado `pizza` en el último commit, que sirve como una referencia importante en el historial.

32. **Ver Tags Creado**   
- **Comando:** `git tag`
- **Explicación:** Listas todos los tags existentes en el repositorio.

33. **Ver el Tag `pizza`**   
- **Comando:** `git show pizza`
- **Explicación:** Muestras información detallada sobre el tag `pizza`, incluyendo el commit al que está asociado.
