![Imagen.](/image/git-branch.png "Imagen.")

#
# Git - Inicial - Branches

## Comenzando 🚀
Antes que nada hay que tener un conocimiento previo [Git - Inicial](https://github.com/parrot26/git-inicial) si ya lo viste o ya tenes esos conocimientos sigamos:
Vamos a reforzar el conocimiento sobre **branches** (ramas) que se crean para poder trabajar en equipo y no trabajar todos en el master.
Se puede tener varias Branches y cada una con varias personas para trabajar todos en forma ordenada y controlada.

# 
# Git Cheat Sheet: Ramas (Branches)

## Creación y gestión de ramas

*   **`git branch`**: Lista todas las ramas locales en tu repositorio.
*   **`git branch -a`**: Lista todas las ramas locales y remotas.
*   **`git branch <nombre_de_la_rama>`**: Crea una nueva rama local con el nombre especificado.
*   **`git checkout <nombre_de_la_rama>`**: Cambia a la rama especificada.
*   **`git switch <nombre_de_la_rama>`**: Cambia a la rama especificada (alternativa a `git checkout`).
*   **`git checkout -b <nombre_de_la_rama>`**: Crea una nueva rama y cambia a ella inmediatamente.
*   **`git switch -c <nombre_de_la_rama>`**: Crea una nueva rama y cambia a ella inmediatamente (alternativa a `git checkout -b`).
*   **`git branch -d <nombre_de_la_rama>`**: Elimina una rama local (solo si ya ha sido fusionada).
*   **`git branch -D <nombre_de_la_rama>`**: Elimina una rama local (forzado, incluso si no ha sido fusionada).
*   **`git branch -m <nombre_antiguo> <nombre_nuevo>`**: Renombra una rama local.

## Trabajo con ramas remotas

*   **`git push origin <nombre_de_la_rama>`**: Envía una rama local al repositorio remoto "origin".
*   **`git push --all origin`**: Envía todas las ramas locales al repositorio remoto "origin".
*   **`git fetch origin`**: Descarga las ramas y commits del repositorio remoto "origin".
*   **`git pull origin <nombre_de_la_rama>`**: Descarga y fusiona los cambios de una rama remota en tu rama local actual.
*   **`git branch --track <nombre_de_la_rama_remota>`**: Crea una rama local que rastrea una rama remota específica.

## Fusión y comparación de ramas

*   **`git merge <nombre_de_la_rama>`**: Fusiona la rama especificada en tu rama local actual.
*   **`git rebase <nombre_de_la_rama>`**: Reorganiza tu rama local actual basándose en la rama especificada.
*   **`git diff <rama1> <rama2>`**: Muestra las diferencias entre dos ramas.
*   **`git log --oneline --graph --decorate --all`**: Muestra un gráfico del historial de commits y las ramas.

## Modificación de commits

*   **`git commit --amend`**: Modifica el último commit. Puedes cambiar el mensaje del commit, añadir o quitar archivos, etc.

## Ejemplos prácticos

*   **Crear una rama para una nueva característica:**

    ```bash
    git checkout -b nueva_caracteristica
    ```

*   **Fusionar una rama de corrección de errores en la rama principal:**

    ```bash
    git checkout main
    git merge correccion_errores
    ```

*   **Eliminar una rama antigua que ya no necesitas:**

    ```bash
    git branch -d rama_antigua
    ```

*   **Comparar los cambios entre tu rama actual y la rama `develop`:**

    ```bash
    git diff develop
    ```

*   **Modificar el mensaje del último commit:**

    ```bash
    git commit --amend -m "Nuevo mensaje para el commit"
    ```

## Notas

*   Las ramas son una herramienta fundamental en Git para trabajar en paralelo en diferentes características o correcciones sin afectar la rama principal.
*   `git merge` crea un nuevo commit de fusión, mientras que `git rebase` reescribe el historial de commits para que parezca que la rama se creó a partir de la rama principal.
*   Es importante entender la diferencia entre `git fetch` y `git pull`. `git fetch` solo descarga los cambios, mientras que `git pull` los descarga y los fusiona automáticamente.
*   `git commit --amend` es útil para corregir errores en el último commit o para añadir cambios que olvidaste incluir en él.

#
## Contribuyendo 🖇️

_Las contribuciones son lo que hacen que la comunidad de código abierto sea un lugar mejor. Cualquier contribución que hagas será muy apreciada._

_Si queres aportar con alguna sugerencia para mejorarlo, simplemente un **fork** en el repo y crear un **pull request**. También podes abrir un issue con la etiqueta **enhancement**. ¡No te olvides de sumar una estrella al repo! **¡Gracias de nuevo!**_

# 
## Autor ✒️

* **Juan Pablo Soto** - [GitHub](https://github.com/parrot26) - [Linkedin](www.linkedin.com/in/juanpablosoto26)

# 
## Licencia 📄

Este proyecto está bajo la Licencia **MIT** - mira el archivo [LICENSE](LICENSE) para detalles


# 
## Expresiones de Gratitud 🎁

* Comenta a otros sobre este repo 📢
* Invita una cerveza 🍺 o un café ☕ a alguien del equipo. 
* Da las gracias públicamente 🤓.

#### _Gracias a:_

* [GitHub](https://github.com/)
* [Git](https://git-scm.com/)

---
⌨️ con 💪 por [Juan Pablo Soto](https://github.com/parrot26)
