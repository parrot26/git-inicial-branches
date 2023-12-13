![Imagen.](/image/git-branch.png "Imagen.")

#
# _Git - Inicial - Branches_

### Comenzando 🚀
_Antes que nada hay que tener un conocimiento previo [Git - Inicial](https://github.com/parrot26/git-inicial) si ya lo viste o ya tenes esos conocimientos sigamos:
Las **branches** (ramas) se crean para poder trabajar en equipo y no trabajar todos en el master._
_Se puede tener varias Branches y cada una con varias personas y trabajar todos en forma ordenada y controlada._

# 
### Hora de meter mano 🛠️

* _Creamos una branch._

```ssh
git checkout -b newbranch
```

* _Para pasarnos a esa branch creada:_

```ssh
git checkout newbranch
```

* _Verificamos donde estamos parados (va a decir: On branch ..nombre)_

```ssh
git status
```

* _También se puede verificar con:_

```ssh
git branch
```

* _Una vez dentro de la branch nueva:_

_Modificamos el código del archivo:_

```ssh
vim ejemplo.html
```

* _Lo agregamos:_

```ssh
git add ejemplo.html # se puede usar 'git add -A' o 'git add .' si queremos agregar todo.
```

* _Agregamos un commit:_

```ssh
git commit -m "agregamos nueva línea"
```

* _Le decimos a la copia local de git que hay una nueva branch en el repo externo que va a estar linqueada con mi branch local._

```ssh
git push -u origin newbranch
```

###### _Se pone el -u la primera vez para q luego podamos hacer solo push._

* _Podemos ver los cambios de todo:_

```ssh
git log
```

```ssh
git branch -a
```

###### _nos muestra todas las banches_


* _Nos pasamos a la branch master:_

```ssh
git checkout master
```

* _Para asegurarnos que tenemos lo último:_

```ssh
git pull origin master
```

* _Nos va a mostrar las branches mergeadas y va a faltar la nueva creada:_

```ssh
git branch --merge
```

* _Hacer un merge de la nueva branch:_

```ssh
git merge newbranch
```


* _Para limpiar (eliminar) la branch creada sí ya no se usa mas:_

```ssh
git push origin --delete newbranch
```

* _Chequeamos que sigue apareciendo localmente:_

```ssh
git branch -a
```

* _Elimina la branch localmente:_

```ssh
git branch -d newbranch
```


#
# _Arreglando errores:_


#### Si nos equivocamos en un cambio que hicimos con un archivo en el working directory:

* _Vuelve al estado que estaba:_

```ssh
git checkout NOMBRE.txt
```

* _Lo modificamos nuevamente:_

```ssh
vim NOMBRE.txt
```

* _Lo agregamos de nuevo:_

```ssh
git add NOMBRE.txt
```

* _Lo chequeamos:_

```ssh
git status
```

* _Luego:_

```ssh
git commit --amend
```

###### _Nos permite dos cosas 1 agregar el archivo, 2 poder modificar el mensaje de commit._

* _Para ver todos los archivos modificados por los commits:_

```ssh
git log --stat
```

#### Cómo hacemos cuando un commit que era para una branch lo hicimos en otra?

```ssh
git log # Para ver los hashes y copiarlo.
git checkout newbranch # Nos pasamos a la branch q queremos.
git log # Vemos que en esta branch está el commit viejo.
git cherry-pick HASH # Ejecutamos ese comando con el número de hash del commit donde dice HASH.
```

###### _Hasta ahora lo q se hizo es COPIAR el commit de una branch a otra pero sin moverlo._

* _Como hacemos ahora?_

```ssh
git checkout master # Nos pasamos a la master.
git log # Vemos que está el commit.
```

* _Ahora hacemos un git reset (tiene 3 modos: soft, mix y hard)._

```ssh
git reset --soft HASH # Ahí le pasamos el hash del primer commit no del último q queremos eliminar.
git log # Verificamos.
git status # Vemos los commit en el staging area.
```

###### _NOTA: git reset HASH (sin argumento usa el modo mix, la diferencia q el commit 1 y el 2 los deja afuera del staging area y los deja en el working directory)._
#
#

#### Cómo ver el historial de commit para saber los que se hicieron incluyendo los amend y todo? 
###### (Se guardan por un tiempo y luego se van borrando, ejemplo 30 días).
#

```ssh
git reflog # Veo todos los cambios
```

#### Cómo ver diferencias entre commits?
#

```ssh
git diff HASH1 HASH2 # Veo la diferencia entre dos hashes de commits.
```



_En **Github**, por ejemplo, si tenemos dos branches te sugiere mediante un botón hacer un **Compare & pull request** esto permite comparar los cambios que uno hizo y se deja un comentario, se lo podemos pasar a un compañero para que lo veo y lo analice._

_Permite en **Review changes** realizar una charla para ir aprobando, desaprobando o sugerir cambios._

_Luego de eso se puede hacer un **Merge** desde **Github** y ver los cambios en ambas branches._



# 
### Contribuyendo 🖇️

_Las contribuciones son lo que hacen que la comunidad de código abierto sea un lugar mejor. Cualquier contribución que hagas será muy apreciada._

_Si queres aportar con alguna sugerencia para mejorarlo, simplemente un **fork** en el repo y crear un **pull request**. También podes abrir un issue con la etiqueta **enhancement**. ¡No te olvides de sumar una estrella al repo! **¡Gracias de nuevo!**_

# 
### Autor ✒️

* **Juan Pablo Soto** - [GitHub](https://github.com/parrot26) - [Linkedin](www.linkedin.com/in/juanpablosoto26)

# 
### Licencia 📄

Este proyecto está bajo la Licencia **MIT** - mira el archivo [LICENSE](LICENSE) para detalles


# 
### Expresiones de Gratitud 🎁

* Comenta a otros sobre este repo 📢
* Invita una cerveza 🍺 o un café ☕ a alguien del equipo. 
* Da las gracias públicamente 🤓.

#### _Gracias a:_

* [GitHub](https://github.com/)
* [Git](https://git-scm.com/)
* [Linkedin](https://www.linkedin.com/)


---
⌨️ con ❤️ por [Juan Pablo Soto](https://github.com/parrot26)





