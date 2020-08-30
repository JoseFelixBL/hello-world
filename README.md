# hello-world
Start using GitHub with hello-world project.
Following the hello-world guide I found myself thinking on the sudoku project.
I have it mostly finished in the resolution phase, then I want to add GUI to show resolution steps or even play it.

## Cosas nuevas desde VSCode
https://youtu.be/RGOj5yH7evk
Esto lo estoy escribiendo en VSCode en mi PC y quiero ver cómo lo guardo en GitHub y queda todo en la última versión.
Tengo que hacer lo siguiente:
    - git status # para ver el estátus de los ficheros en la carpeta git
    - git add # para agregar los ficheros que eventualmente querré subir al repositorio, es como la versión terminada que tengo hasta ahora, lo que quiero guardar.
    - git add . # para guardar todo lo que está cambiado
    - git commit # para confirmar que eso es lo que quiero guardar, pero hasta ahora todo sigue en local.
    - git push # para subirlo al repositorio.

## Crear un repositorio nuevo con ficheros que he creado previamente en local
Tengo que inicializr git en el nuevo directorio.
git init
y se crea el git en local, siendo el local master.
Luego puedo hacer:
git status
git add .

Si trato de push:
git push origin master
Me da un error porque como no hicimos un clone del repositorio en este PC, no sabemos a dónde lo vamos a subir.

1- Creamos un empty git repository en GitHub
2- copiamos el SSH del nuevo repositorio de GitHub y lo pegamos a la siguiente instrucción:
    git remote add origin <el-SSH>
    comprobamos usando: git remote -v
3- git push -u origin master
    el "-u" es de UPSTREAM, o sea que lo voy a subir a GitHub

## SSH
ssh-keygen -t rsa -b 4096 -C "josefbl.work@gmail.com"

## Git Branch
"git branch" to check status, type "q" to exit the "less" like view. The "*" is where you are.
"git checkout -b <new-branch-name>" to create a new brach, give it a meaningfull name (usually long).
"git checkout <other-branch>" will switch you to the other branch, so you will be working in that other branch.

"git diff <branch-name>" shows the differences of files between branches, better use it before Merging.

It is "better" practice to push up branches to github and then merging them there, so first change to the appropiate branch to push: git checkout <branch-to-push>
git status
git commit ...
git push ...

then create a "pr" or a "pull request", to have your code pulled into another branch - i.e. from the feature-branch to the master-branch.
Once we have made a pr, everyone can reviewour code, comment, ask for changes...

Para borrar una branch que ya se ha mergeado en el master:
git branch -d <branch-name>