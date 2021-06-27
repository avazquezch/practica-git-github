### ¿Qué comando utilizaste en el paso 11? ¿Por qué?
$ git reset --hard HEAD~1  -> Con este comando desago el commit recien hecho y el estado del proyecto me queda tal y como se encontraba antes de la modificación del fichero.

#### Contenido del fichero antes del comando 
$ cat git-nuestro.md
*Git* nuestro que estás en los repos
Comprimidos sean tus *commits*
Venga a nosotros tu *log*
En el local como en el *remote*
Danos hoy nuestro *pull* de cada día
Perdona nuestros *conflictos*
Como también perdonamos los de otros geeks
No nos dejes caer en *detached HEAD*
y líbranos de *SVN*
`git commit --amend`

#### Contenido del fichero después del comando 
$ cat git-nuestro.md
Git nuestro
Git nuestro que estas en los repos
Comprimidos sean tus commits
Venga a nosotros tu log
En el local como en el remote
Danos hoy nuestro pull de cada día
Perdona nuestros conflictos
Como también perdonamos los de otros geeks
No nos dejes caer en detached HEAD
y líbranos de SVN
git commit --amend


### ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
git reset --hard 495a7ff -> Primero listo con reflog y veo el id al cual tengo que recuperar el trabajo recién desechado.

#### Contenido del fichero después del comando 
$ cat git-nuestro.md
*Git* nuestro que estás en los repos
Comprimidos sean tus *commits*
Venga a nosotros tu *log*
En el local como en el *remote*
Danos hoy nuestro *pull* de cada día
Perdona nuestros *conflictos*
Como también perdonamos los de otros geeks
No nos dejes caer en *detached HEAD*
y líbranos de *SVN*
`git commit --amend`

### El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
$ git merge master  -> No causó ningún conflicto porque la rama que está intentando fusionar es un padre de la rama actual. 

### El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
$ git merge htmlify -> Este merge si causó conflictos porque los ficheros están modificados en diferentes líneas.

### El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
$ git merge styled -> No causó conflictos porque como lo hice desde el master que es el padre de styled este movió la rama y apuntó al mismo commit ambas ramas(master y styled) es decir ambas tienen la misma líneas en el fichero git-nuestro.md, hizo un Fast-forward. 

### ¿Qué comando o comandos utilizaste en el paso 25?
$ git log --graph --decorate --pretty=oneline
*   ff2485bb639a8e0334b7a55ce61331d2033ecc26 (HEAD -> master, styled) Solucionando conflictos tras el merge de la rama htmlify en styled, quedándonos con el contenido de la rama styled. Paso 20.
|\
| * 3870f541e9517664c974b4e9bc42d76bdee5ec9b (htmlify) Haciendo commit del fichero modificado git-nuestro-md en la rama htmlify. Paso 18.
* | 495a7ffa18a9ffa0023886f5f50cc5c23f7d25a6 Añadiendo los cambios al staging area y luego pasarlo al repositorio en la rama styled tras modificar el fichero git-nuestro.md. Paso 10.
|/
* 68eaa9d5759ce323361ef4cd6b3f17c46372c038 Moviendo lo que hay en el staging area al repositorio. Paso 4.


### El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
$ git merge --no-ff title -> Si puede ser no fast forward porque crea un commit con el merge de las dos ramas y el HEAD apunta a ese commit de la rama master.

$ git log --graph --decorate --pretty=oneline
*   0ca12bc772301d981406f36d13c274ec225045f8 (HEAD -> master) Merge branch 'title' Estoy haciendo un merge --no-ff desde la rama master con la rama title.
|\
| * f58674247ed5eb833e1c3a3d3cc1d318432cf618 (title) Haciendo commit del fichero git-nuestro.md con el título. Paso 23.
|/
*   ff2485bb639a8e0334b7a55ce61331d2033ecc26 (styled) Solucionando conflictos tras el merge de la rama htmlify en styled, quedándonos con el contenido de la rama styled. Paso 20.
|\
| * 3870f541e9517664c974b4e9bc42d76bdee5ec9b (htmlify) Haciendo commit del fichero modificado git-nuestro-md en la rama htmlify. Paso 18.
* | 495a7ffa18a9ffa0023886f5f50cc5c23f7d25a6 Añadiendo los cambios al staging area y luego pasarlo al repositorio en la rama styled tras modificar el fichero git-nuestro.md. Paso 10.
|/
* 68eaa9d5759ce323361ef4cd6b3f17c46372c038 Moviendo lo que hay en el staging area al repositorio. Paso 4.


### ¿Qué comando o comandos utilizaste en el paso 27?
$ git reset HEAD~1

alevaz@ESEURALEVAZ-LAP MINGW64 ~/Datos-D/Bootcamp Web/Curso - Git, GitHub Y SourceTree/practica-git-github-avazquezch (master)
$ git reset HEAD~1
Unstaged changes after reset:
M       git-nuestro.md

alevaz@ESEURALEVAZ-LAP MINGW64 ~/Datos-D/Bootcamp Web/Curso - Git, GitHub Y SourceTree/practica-git-github-avazquezch (master)
$ cat git-nuestro.md
#Título del fichero git-nuestro.md

*Git* nuestro que estás en los repos
Comprimidos sean tus *commits*
Venga a nosotros tu *log*
En el local como en el *remote*
Danos hoy nuestro *pull* de cada día
Perdona nuestros *conflictos*
Como también perdonamos los de otros geeks
No nos dejes caer en *detached HEAD*
y líbranos de *SVN*
`git commit --amend`

alevaz@ESEURALEVAZ-LAP MINGW64 ~/Datos-D/Bootcamp Web/Curso - Git, GitHub Y SourceTree/practica-git-github-avazquezch (master)
$ git log --graph --decorate --pretty=oneline
*   ff2485bb639a8e0334b7a55ce61331d2033ecc26 (HEAD -> master, styled) Solucionando conflictos tras el merge de la rama htmlify en styled, quedándonos con el contenido de la rama styled. Paso 20.
|\
| * 3870f541e9517664c974b4e9bc42d76bdee5ec9b (htmlify) Haciendo commit del fichero modificado git-nuestro-md en la rama htmlify. Paso 18.
* | 495a7ffa18a9ffa0023886f5f50cc5c23f7d25a6 Añadiendo los cambios al staging area y luego pasarlo al repositorio en la rama styled tras modificar el fichero git-nuestro.md. Paso 10.
|/
* 68eaa9d5759ce323361ef4cd6b3f17c46372c038 Moviendo lo que hay en el staging area al repositorio. Paso 4.


### ¿Qué comando o comandos utilizaste en el paso 28?
$ git reset --hard 68eaa9d5759ce323361ef4cd6b3f17c46372c038

Con esto lo dejo tal y como estaba antes cuando hice el primer commit.


### ¿Qué comando o comandos utilizaste en el paso 29?
$ git branch -d title
error: The branch 'title' is not fully merged.
If you are sure you want to delete it, run 'git branch -D title'.

alevaz@ESEURALEVAZ-LAP MINGW64 ~/Datos-D/Bootcamp Web/Curso - Git, GitHub Y SourceTree/practica-git-github-avazquezch (master)
$ git branch -D title
Deleted branch title (was f586742).


### ¿Qué comando o comandos utilizaste en el paso 30?

Con este veo el id
$ git reflog
68eaa9d (HEAD -> master) HEAD@{0}: reset: moving to 68eaa9d5759ce323361ef4cd6b3f17c46372c038
ff2485b (styled) HEAD@{1}: reset: moving to HEAD~1
0ca12bc HEAD@{2}: merge title: Merge made by the 'recursive' strategy.
ff2485b (styled) HEAD@{3}: checkout: moving from title to master
f586742 HEAD@{4}: commit: Haciendo commit del fichero git-nuestro.md con el título. Paso 23.
ff2485b (styled) HEAD@{5}: checkout: moving from master to title
ff2485b (styled) HEAD@{6}: checkout: moving from styled to master
ff2485b (styled) HEAD@{7}: checkout: moving from master to styled
ff2485b (styled) HEAD@{8}: merge styled: Fast-forward
68eaa9d (HEAD -> master) HEAD@{9}: checkout: moving from styled to master
ff2485b (styled) HEAD@{10}: commit (merge): Solucionando conflictos tras el merge de la rama htmlify en styled, quedándonos con el contenido de la rama styled. Paso 20.
495a7ff HEAD@{11}: checkout: moving from htmlify to styled
3870f54 (htmlify) HEAD@{12}: commit: Haciendo commit del fichero modificado git-nuestro-md en la rama htmlify. Paso 18.
68eaa9d (HEAD -> master) HEAD@{13}: checkout: moving from master to htmlify
68eaa9d (HEAD -> master) HEAD@{14}: checkout: moving from master to master
68eaa9d (HEAD -> master) HEAD@{15}: checkout: moving from styled to master
495a7ff HEAD@{16}: reset: moving to 495a7ff
68eaa9d (HEAD -> master) HEAD@{17}: reset: moving to HEAD~1
495a7ff HEAD@{18}: commit: Añadiendo los cambios al staging area y luego pasarlo al repositorio en la rama styled tras modificar el fichero git-nuestro.md. Paso 10.
68eaa9d (HEAD -> master) HEAD@{19}: checkout: moving from master to styled
68eaa9d (HEAD -> master) HEAD@{20}: commit (initial): Moviendo lo que hay en el staging area al repositorio. Paso 4.

Con este comando veo el contenido del fichero antes de Rehacer el merge que hemos deshecho
$ cat git-nuestro.md
Git nuestro
Git nuestro que estas en los repos
Comprimidos sean tus commits
Venga a nosotros tu log
En el local como en el remote
Danos hoy nuestro pull de cada día
Perdona nuestros conflictos
Como también perdonamos los de otros geeks
No nos dejes caer en detached HEAD
y líbranos de SVN
git commit --amend

Con este comando rehago el merge que hemos deshecho
$ git reset --hard 0ca12bc
HEAD is now at 0ca12bc Merge branch 'title' Estoy haciendo un merge --no-ff desde la rama master con la rama title.

Con este comando veo el contenido del fichero después de Rehacer el merge que hemos deshecho. 
$ cat git-nuestro.md
#Título del fichero git-nuestro.md

*Git* nuestro que estás en los repos
Comprimidos sean tus *commits*
Venga a nosotros tu *log*
En el local como en el *remote*
Danos hoy nuestro *pull* de cada día
Perdona nuestros *conflictos*
Como también perdonamos los de otros geeks
No nos dejes caer en *detached HEAD*
y líbranos de *SVN*
`git commit --amend`


### ¿Qué comando o comandos usaste en el paso 32?

Con este comando veo el contenido del fichero git-nuestro.md
$ cat git-nuestro.md
#Título del fichero git-nuestro.md

*Git* nuestro que estás en los repos
Comprimidos sean tus *commits*
Venga a nosotros tu *log*
En el local como en el *remote*
Danos hoy nuestro *pull* de cada día
Perdona nuestros *conflictos*
Como también perdonamos los de otros geeks
No nos dejes caer en *detached HEAD*
y líbranos de *SVN*
`git commit --amend`

Con este otro vuelvo al commit inicial cuando se creó el poema
$ git reset --hard 68eaa9d5759ce323361ef4cd6b3f17c46372c038
HEAD is now at 68eaa9d Moviendo lo que hay en el staging area al repositorio. Paso 4.

Este me permite ver que he vuelto tay y como estaba en el primer commit.
$ cat git-nuestro.md
Git nuestro
Git nuestro que estas en los repos
Comprimidos sean tus commits
Venga a nosotros tu log
En el local como en el remote
Danos hoy nuestro pull de cada día
Perdona nuestros conflictos
Como también perdonamos los de otros geeks
No nos dejes caer en detached HEAD
y líbranos de SVN
git commit --amend


### ¿Qué comando o comandos usaste en el punto 33?

Con este veo el id
$ git reflog
68eaa9d (HEAD -> master) HEAD@{0}: reset: moving to 68eaa9d5759ce323361ef4cd6b3f17c46372c038
0ca12bc HEAD@{1}: reset: moving to 0ca12bc
68eaa9d (HEAD -> master) HEAD@{2}: reset: moving to 68eaa9d5759ce323361ef4cd6b3f17c46372c038
ff2485b HEAD@{3}: reset: moving to HEAD~1
0ca12bc HEAD@{4}: merge title: Merge made by the 'recursive' strategy.
ff2485b HEAD@{5}: checkout: moving from title to master
f586742 HEAD@{6}: commit: Haciendo commit del fichero git-nuestro.md con el título. Paso 23.
ff2485b HEAD@{7}: checkout: moving from master to title
ff2485b HEAD@{8}: checkout: moving from styled to master
ff2485b HEAD@{9}: checkout: moving from master to styled
ff2485b HEAD@{10}: merge styled: Fast-forward
68eaa9d (HEAD -> master) HEAD@{11}: checkout: moving from styled to master
ff2485b HEAD@{12}: commit (merge): Solucionando conflictos tras el merge de la rama htmlify en styled, quedándonos con el contenido de la rama styled. Paso 20.
495a7ff HEAD@{13}: checkout: moving from htmlify to styled
3870f54 HEAD@{14}: commit: Haciendo commit del fichero modificado git-nuestro-md en la rama htmlify. Paso 18.
68eaa9d (HEAD -> master) HEAD@{15}: checkout: moving from master to htmlify
68eaa9d (HEAD -> master) HEAD@{16}: checkout: moving from master to master
68eaa9d (HEAD -> master) HEAD@{17}: checkout: moving from styled to master
495a7ff HEAD@{18}: reset: moving to 495a7ff
68eaa9d (HEAD -> master) HEAD@{19}: reset: moving to HEAD~1
495a7ff HEAD@{20}: commit: Añadiendo los cambios al staging area y luego pasarlo al repositorio en la rama styled tras modificar el fichero git-nuestro.md. Paso 10.
68eaa9d (HEAD -> master) HEAD@{21}: checkout: moving from master to styled
68eaa9d (HEAD -> master) HEAD@{22}: commit (initial): Moviendo lo que hay en el staging area al repositorio. Paso 4.

Veo el contenido antes del comando reset
$ cat git-nuestro.md
Git nuestro
Git nuestro que estas en los repos
Comprimidos sean tus commits
Venga a nosotros tu log
En el local como en el remote
Danos hoy nuestro pull de cada día
Perdona nuestros conflictos
Como también perdonamos los de otros geeks
No nos dejes caer en detached HEAD
y líbranos de SVN
git commit --amend

$ git reset --hard 0ca12bc
HEAD is now at 0ca12bc Merge branch 'title' Estoy haciendo un merge --no-ff desde la rama master con la rama title.

Veo que se ha actualizado hasta el último estado que estaba antes del Paso 32.
$ cat git-nuestro.md
#Título del fichero git-nuestro.md

*Git* nuestro que estás en los repos
Comprimidos sean tus *commits*
Venga a nosotros tu *log*
En el local como en el *remote*
Danos hoy nuestro *pull* de cada día
Perdona nuestros *conflictos*
Como también perdonamos los de otros geeks
No nos dejes caer en *detached HEAD*
y líbranos de *SVN*
`git commit --amend`
