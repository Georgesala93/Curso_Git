# Curso_Git
What is documented in the repository is from the Git course on the Platzi platform, I share it so that it is available to everyone.

### Config Git / Configuracion de Git

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `git config --global user.name "name-example"` | Add a user name | Añade un nombre de usuario |
| `git config --global user.email user@example.com` | Add a email for user | Añade un correo del usuario |
| `git config --list` | List all setings | Muestra todas las configuraciones |

### Config SSH Keys / Configuracion de Credenciales SSH

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `ssh-keygen -t rsa -b 4096 -C "Email"` | Generate SSH key | Generar credencial SSH |
| `eval $(ssh-agent -s)` | Verify ssh agent | Verifica la existencia del servidor de credenciales SSH |
| `ssh-add [rute]` | Add SSH key to your workspace | Agrega la credencial SSH al entorno de trabajo |

### Creating Projects / Creacion de proyectos

| Command | Description | Descripción |
| ------- | ----------- | ------------ |
| `git init` | Initialize a local Git repository | Inicia un repositorio local de Git |
| `git clone [url]` | Create a local copy of a remote repository | Crea una copia local de un repositorio remoto |

### Basic Snapshotting / Snapshooting Basico

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git status` | Check status | Verifica el estatus del repositorio |
| `git add [file-name.txt]` | Add a file to the staging area | Añade un archivo al area de preparación |
| `git add .` | Add all new and changed files to the staging area | Añade todos los archivos al area de preparación |
| `git commit -m "[commit message]"` | Commit changes | Añade los archivos al repositorio |
| `git commit -am "[commit message]"` |Add changed files and commit | Añande los cambios y hace commit |
| `git rm -r [file-name.txt]` | Remove a file (or folder) | Elimina archivos o carpetas |
| `git commit --amend` | Ammend the last commit | Agrega los cambios al ultimo commit en caso de error |

### Branching & Merging / Ramas y fusionar

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) | Lista todas las ramas |
| `git branch -a` | List all branches (local and remote) | Lista todas las ramas locales y remotas |
| `git branch [branch name]` | Create a new branch | Crea una nueva rama |
| `git branch -d [branch name]` | Delete a branch | Elimina una rama |
| `git show-branch --all` | List all branches local | Lista todas las ramas en local |
| `git push origin --delete [branch name]` | Delete a remote branch | Elimina una rama remota |
| `git checkout -b [branch name]` | Create a new branch and switch to it | Crea una nueva rama y cambia a ella |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it | Clona una rama remota y cambia a ella |
| `git checkout [branch name]` | Switch to a branch | Cambiar a una rama determinada |
| `git checkout -` | Switch to the branch last checked out | Cambia a la ultima rama seleccionada |
| `git checkout -- [file-name.txt]` | Discard changes to a file | Descarta los cambios de un archivo |
| `git merge [branch name]` | Merge a branch into the active branch | Fusiona una rama a la rama activa
| `git merge [source branch] [target branch]` | Merge a branch into a target branch | Fusiona una rama a una rama determinada |
| `git stash` | Stash changes in a dirty working directory | Guarda los cambios en un directorio de trabajo temporal |
| `git stash clear` | Remove all stashed entries | Elimina todas las entradas ocultas |

### Sharing & Updating Projects / Compartiendo y Repositorios Remotos

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository | Envia el repositorio local a remoto |
| `git push origin --delete [branch name]` | Delete a remote branch | Elimina un repositorio remoto |
| `git pull` | Update local repository to the newest commit | Actualizar el repositorio local a la confirmación más reciente |
| `git pull origin [branch name]` | Pull changes from remote repository | Hace un feth y fusiona
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository | Crea un repositorio remoto |
| `fork` | Copy a external repository | Copa un repositorio externo |
| `git remote -v` | list remote connections | Lista las conexiones remotas |
| `git remote set-url [branch name] [url]` | Change the url | Cambia la url del repositorio |

### Inspection & Comparison / Inspeccion y Comparacion

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git log` | View changes | Muestra los cambios en el repositorio |
| `git log --summary` | View changes (detailed) | Muestra los cambios en el repositorio detalladamente |
| `git log -all --graph --decorate --oneline` | View changes (Max-detailed) | Muestra todos los cambios del repositorio detallada y graficamente |
| `git diff [source branch] [target branch]` | Preview changes before merging | Compara los diferentes cambios |

### Reset
| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `git reset --soft [SHA1]` | Remove commits but leave the files in the staging area | Elimina commits pero deja los archivos en el staging area |
| `git reset --mixed [SHA1]` | Remove commits and the files are left in the working directory | Elimina commits y los archivos quedan en el working directory |
| `git reset --hard [SHA1]` | It eliminates changes to us even from the working directory | Nos elimina los cambios incluso del working directory |

### Others / Otros

| Command | Description | Descripción |
| ------- | ----------- | ----------- |
| `alias [name=] "command"` | Create a shorcut for a command | Crea un alias para llamar a un comando |
| `git tag -a [name] -m "message" [id/hashtag]` | Create a tag for a commit | Crea un tag de un commit en especifico |
| `git show-ref --tags` | List all tags | Lista los tags existentes |
| `git push --tags` | Push tags to your repository | Envia los tags al repositorio remoto |
| `git tag -d [name]` | Delete a tag | Elimina un tag en especifico |
| `git push origin :refs/tags/[name]` | Delete a tag from GitHub | Elimina un tag dentro de GitHub |
| `gitk` | Open GUI | Abre una interfaz grafica |
| `git cherry.pick [id]` | Take commit from other branches | Trae un commit especifico desde otra rama |
| `git grep -n [word]` | Search words in the proyect | Busca la palabra especificada en todo el proyecto |
| `git shortlog` | Displays the number and description of commits made by each user. | Muestra la cantidad y la descripcon de los commit realizados por cada usuario.
| `git shortlog -sn` | Shows how many commits each user has made.| Muestra cuantos commit han hecho cada usuario.
| `git shortlog -sn --all` | Displays how many commits each user has made, up to the deleted ones| Muestra cuantos commit han hecho cada usuario, hasta los eliminados.
| `git shortlog -sn --all --no-merge` | Displays how many commits each user has made, removing the deleted ones without the merges.| Muestra cuantos commit ha hecho cada usuario, quitando los eliminados sin los merges.
| `git blame <Nombre archivo>` | Shows who did what line by line.| Muestra quien hizo cada cosa línea por línea.
| `git <Nombre Comando> --help` | Shows how the command works.| Muestra como funciona el comando.
| `git blame <Nombre archivo> -L<linea_inicial>,<linea_final>` |  Shows who did what line by line, indicating the range of lines to view. | Muestra quien hizo cada cosa línea por línea, indicándole el rango de las lineas a ver. 
| `git branch -r` | Show all remote branches.| Muestran todas las ramas remotas.
| `git branch -a` | Show all branches (local and remote).| Muestran todas las ramas(locales y remotas).

 ## Execution examples / Ejemplos de Ejecución
 >`git status`

![Status](/img/Comando_status.png)

 >`git commit`

![commit](/img/Comando_commit.png)

 >`git push`

![push](/img/Comando_push.png)

 >`git show`

![show](/img/Comando_show.png)

 >`git log`

![log](/img/Comando_log.png)

 >`git diff`

 ![diff](/img/Comando_diff.png)

 >`git checkout`
 
 ![checkout](/img/Comando_checkout.png)

 >`git branch`
 
 ![branch](/img/Comando_branch.png)

 >`git merge` : Trae lo que esta en la rama cabecera a la rama main/master
 
 ![merge](/img/Comando_merge.png)

>`git log --all --graph` : Muestra los commit realizados de forma grafica
 
 ![logall1](/img/Comando_log_--all_--graph.png)

>`git log --all --graph --decorate --oneline` : Muestra los commit realizados de forma resumida y grafica
 
 ![logall2](/img/Comando_log_--all_--graph_--decorate_--oneline.png)

>`git alias` : Crea un alias para un comando largo, esto funciona en la terminal de git bash
 
 ![alias](/img/Comando_alias.png)

>`git branch` : Crea ramas en el repositorio locar y en el repositorio remoto

 ![branch](/img/Comando_create_branch_and_send_repositorie.png)

>`git tag` 
>- `git tag -a <"referencia del tag"> -m <"Mensaje de commit"> <identificador del commit>` : Crear un tag o un release (version) apartir de un commit
>- `git show-ref --tags` : Muestra los tags creados

 ![tag](/img/Comando_tag_show-ref--tags.png)

>`git pusg origin --tags` : Realiza el envio del tag al repositorio remoto

 ![pusgorigintags](/img/Comando_push_origin_--tags.png)

>`git tag -d <nombre del tag>` : Eliminar un tag del repositorio local y remoto

![tagd](/img/Comando_tag_-d.png)

>`git --ammend` : reescribe el commit realizado anteriormente en llegado el caso que allas dado commit y te falto un cambio, realizas el cambio que te falto, despues añades(git add .) los cambios y hay si ejecutas el comando para reescribir el commit.

![ammend](/img/Comando_--amend.png)

>`grep` 
>- `git grep <palabra a buscar>` : Nos saldra un display con la ruta del archivo donde se utiliza la palabra buscada.
>- `git grep -n <palabra a buscar>` : Nos saldra un display con la ruta del archivo y la linea donde se utiliza la palabra buscada.
>- `git grep -c <palabra a buscar>` : Nos saldra un display con ruta del archivo donde se utiliza la palabra buscada y la sumatoria de cuantas veces se repite.

![grep](/img/Comando_grep.png)