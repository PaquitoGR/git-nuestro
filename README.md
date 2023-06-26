# Práctica del curso de git, gitHub

## Ejercicio 1
Se deberá crear un repositorio y realizar una serie de operaciones desde la consola de
comandos sobre el mismo para posteriormente subir el repositorio a Github.
Se deberá entregar a través del formulario de prácticas indicando la URL del repositorio. En el
repositorio, deberá existir un archivo *readme.md* con las respuestas a las siguientes preguntas:
- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
  
	`git reset --hard HEAD~1` para deshacer el *commit* y los cambios realizados en el *working copy*.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
  
	`git reset --hard a4561be` (id del *commit*), para volver hacer el *commit* y los cambios del *working copy*.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
  
	Dice que el archivo ya está actualizado (*Already up to date*), ya que la rama *styled* no tiene cambios que añadir con respecto a *main*. En *styled*, se han hecho cambios a partir de la *working copy* de *main*, de modo que es *main* la rama que podría absorver los cambios hechos en la rama *styled*, y no al revés.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

  Causaron conflictos dos bloques de líneas que eran diferentes. Tan solo se mantuvo una línea a la que *htmlify* añadía la etiqueta `<br>` al final. (**Nota**: dado que en la práctica no se indica lo contrario, he dejado esa etiqueta ya que, para _Git_, eso no es un conflicto.)

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

  No causó conflicto dado el contenido de la rama *main* se actualiza con las modificaciónes de la rama *styled*, pero *styled* ya contenía todo lo que hay en la rama *main*.

- ¿Qué comando o comandos utilizaste en el paso 25?

  `git log --graph --oneline`
	`--graph` para dibujar el diagrama, y `--oneline` para resumir ids y líneas

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

  Sí, porque el *commit* al que apunta *title* ya contiene las mismas líneas del *commit* al que apunta la rama *main*, pero añadiendo el título. No hay conflictos

- ¿Qué comando o comandos utilizaste en el paso 27?

  `git reset HEAD~1` para volver al *commit* anterior al *merge*.

- ¿Qué comando o comandos utilizaste en el paso 28?

  `git restore git-nuestro.md`

- ¿Qué comando o comandos utilizaste en el paso 29?

  `git branch -D title` el parámetro `-D` (mayúscula) fuerza la eliminación cuando, como en este caso, se queda un *commit* inaccesible.

- ¿Qué comando o comandos utilizaste en el paso 30?

  `git reflog` para buscar el *id* del *commit* donde hicimos el *merge*, que es `be7108b` (que quedó inaccesible de forma directa al borrar la rama *title*).
	`git reset --hard be7108b` para volver al *commit*, rehaciendo la modificación de hicimos desde *title*.

- ¿Qué comando o comandos usaste en el paso 32?

  `git log --oneline` para buscar el *id* del *commit* inicial, que es `a3932ea` (en formato resumido, gracias al `--oneline`.)
  `git reset a3932ea` para volver a dicho commit
  
- ¿Qué comando o comandos usaste en el punto 33?

  `git checkout main` para volver a la rama *main*, que la habíamos dejado en el estado final.
