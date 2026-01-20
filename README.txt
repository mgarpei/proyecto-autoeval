$ git init
Initialized empty Git repository in C:/Users/manue/Desktop/Instituto/Entornos/Trabajos/U4/proyecto-autoeval/.git/
$ mkdir proyecto-autoeval
$ cd proyecto-autoeval

¿Para qué sirve el comando git init?¿Qué carpeta oculta se crea automáticamente para rastrear los cambios?.
Git init sirve para inicializar una carpeta como un repositorio. Se crea como consecuencia una carpeta oculta llamada .git.
¿Qué comando has usado para confirmar que tu identidad es la correcta antes de empezar?
git config --global user.name  PARA EL NOMBRE
git config --global user.email  PARA EL CORREO
---------------
$ touch index.html README.txt secreto.txt
echo "*.txt" > .gitignore
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        index.html

nothing added to commit but untracked files present (use "git add" to track)

¿Por qué es importante el uso de .gitignore en proyectos profesionales?
Para mantener el repositorio limpio de archivos temporales
 Si un archivo está "preparado" (staged), ¿en qué área de Git se encuentra y cuál es el comando para ver esta diferencia antes de confirmar?.
 Se encuentra en el area de preparación. git status.
---------
$ git log --oneline
537df25 (HEAD -> incluir-estilos) Manuel_GarciaArevalo_Peinado : Crear y aplicar estilos
91d917d (main) Manuel_GarciaAreavalo_Peinado : Estructura inicial del HTML

¿Qué ocurre con los archivos de tu carpeta local cuando saltas de una rama a otra? 
Que el contenido cambia, ya que lo que está guardado en una rama no tiene porque estar guardado en otra
¿Cuál es la principal ventaja de trabajar con ramas independientes en lugar de hacer todo en la rama main?.
La principal ventaja es el aislamiento de los datos.
-----------
$ git merge incluir-estilos
Updating 91d917d..b4c625d
Fast-forward
 .gitignore  |  1 +
 estilos.css |  8 ++++++++
 index.html  | 12 ++++++++++++
 3 files changed, 21 insertions(+)
 create mode 100644 .gitignore
 create mode 100644 estilos.css

$ git remote add origin https://github.com/mgarpei/proyecto-autoeval.git

$ git push -u origin main
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 16 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (10/10), 1.20 KiB | 1.20 MiB/s, done.
Total 10 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/mgarpei/proyecto-autoeval.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

1. Al clonar un repositorio, ¿qué nombre recibe por defecto el servidor remoto en nuestra configuración local?.
Recibe el mismo nombre que la carpeta local
2. ¿Qué comando usarías para ver la URL del servidor remoto que acabas de configurar?
git remote 
---------
$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 961 bytes | 68.00 KiB/s, done.
From https://github.com/mgarpei/proyecto-autoeval
   b4c625d..4d63847  main       -> origin/main
Updating b4c625d..4d63847
Fast-forward
 index.html | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)

1. ¿Qué comandos has utilizado para comprobar si el repositorio local está actualizado? 
git log -p para ver si el commit nuevo esta o no.
2. ¿Cuál es la diferencia fundamental entre ejecutar un git fetch y git pull según lo que acabas de experimentar?.
El git fetch sirve solo para mirar la nueva información, y el git pull se descarga y se aplica al repositorio local

Indica los tres comandos que más te ha costado entender y explica por qué.
git remote add origin <URL> = ya que no lo conocía la verdad, en el curso lo hacían de otra manera.
Touch nuevoArchivo = para crear un nuevo archivo, tampoco lo conocía. 
Y por lo demás bien