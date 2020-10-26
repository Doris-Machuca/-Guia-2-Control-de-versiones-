## Actividad 2 - Guia de aprendizaje
## Control de versiones 
## Doris Adriana Machuca Matos 
## 2020
## Centro de electricida electonica y telecomunicaciones
## Bogotá
---

**Actividad 3.2**

1.	A qué se le domina control de versiones.
Un sistema de control de versiones es una herramienta que registra todos los cambios hechos en uno o más proyectos, guardando así versiones del producto en todas sus fases del desarrollo. Las versiones son como fotografías que registran su estado en ese momento del tiempo y se van guardando a medida que se hacen modificaciones al código fuente. (Andrearrs, 2014).

2.	¿Cuáles son los tipos de sistemas de control de versiones y qué los diferencia?
Existen muchos sistemas de control de versiones como por ejemplo SourceSafe, Git, Mercurial, Gitea, Fossil, BitBucket, BitKeeper y Subversion.
Subversion es considerado el abuelo de los sistemas de control de versiones; es centralizado, lento y más pesado que sus sucesores. Git y Mercurial por el contrario son los jóvenes de la generación de relevo; distribuidos, rápidos y ligeros, acordes a las exigencias de hoy en día. (Andrearrs,2014).

3.	¿Qué es Git?
Git fue creado pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando éstas tienen un gran número de archivos de código fuente, es decir Git nos proporciona las herramientas para desarrollar un trabajo en equipo de manera inteligente y rápida y por trabajo nos referimos a algún software o página que implique código el cual necesitemos hacerlo con un grupo de personas. (Andrés, 2015).
 
4.	¿Cuáles son las principales características y ventajas de Git?

* a)	Control de código distribuido: permite a equipos de desarrolladores trabajar de manera remota sobre un mismo proyecto.
* b)	Permite trabajar fuera de línea: permite hacer contribuciones de código de manera local y luego replicarlos e un repositorio remoto.
* c)	 De fuente abierta y gratuito: no se requiere licenciamiento y su código fuente está disponible sin cargo.
* d)	Está basado en las ideas de otros sistemas que tuvieron éxito como BitKeepe y Monotone.
* e)	Viene integrado en varios de los más usados IDE’S como netbeans y Eclipse. (Articuló)

5.	¿Cuál es el funcionamiento del control de cambios del software?
Una forma de comprender el concepto que usa Git para manejar los cambios es ver el software como un árbol, en el sentido matemático del término, con un único nodo padre y uno o muchos nodos hijos.
Para Git el nodo cero es el nodo padre y es la versión inicial del software que se quiere controlar. A partir de ese estado inicial se puede realzar incrementos que son registrados cuando se confirman a través de la opción que suministra Git para tal efecto.
Cada incremento, también llamado commint, tiene un identificador único y un nombre. Además, cada incremento o commit es un nuevo nodo del árbol. (Articuló)

6.	Define los siguientes conceptos.

*	¿Qué es un repositorio?

Un repositorio de código es un lugar donde el código de una aplicación, de un programa cualquiera está almacenado y desde donde se puede distribuir. (Laballos, 2018).
*	¿Qué es una rama o Branch?

Un conjunto de nodos que forman una versión del código fuente. (Articuló).
*	¿Qué es un commit?

Un "commit" es la acción de guardar o subir tus archivos a tu repositorio remoto (una actualización de tus cambios) también puede hacerse al local (depende donde hayas creado tu repositorio). (Diana P, 2015).
*	¿Qué es un readme?

Un archivo léame es integral para un repositorio público, ya que es útil para describir el proyecto, identificar errores y enumerar dependencias , etc. 

7.	Realice un listado con todos los comandos de Git y describa cuál su función.

Según (Sanchez, 2017) estos son  algunos de los commandos que existen
Configuración básica
*	Configurar Nombre que salen en los commits
git config --global user.name "dasdo"
*	Configurar Email
git config --global user.email dasdo1@gmail.com
*	Marco de colores para los comando
git config --global color.ui true

Iniciando repositorio
*	Iniciamos GIT en la carpeta donde esta el proyecto
git init
*	Clonamos el repositorio de github o bitbucket
git clone <url>
*	Añadimos todos los archivos para el commit
git add .
*	Hacemos el primer commit
git commit -m "Texto que identifique por que se hizo el commit"
*	subimos al repositorio
git push origin master

Git clone
*	Clonamos el repositorio de github o bitbucket
git clone <url>
*	Clonamos el repositorio de github o bitbucket ?????
git clone <url> git-demo

Git add
* Añadimos todos los archivos para el commit
git add .
*	Añadimos el archivo para el commit
git add <archivo>
*	Añadimos todos los archivos para el commit omitiendo los nuevos
git add --all 
*	Añadimos todos los archivos con la extensión especificada
git add *.txt
*	Añadimos todos los archivos dentro de un directorio y de una extensión especifica
git add docs/*.txt
*	Añadimos todos los archivos dentro de un directorios
git add docs/

Git commit
*	Cargar en el HEAD los cambios realizados
git commit -m "Texto que identifique por que se hizo el commit"
*	Agregar y Cargar en el HEAD los cambios realizados
git commit -a -m "Texto que identifique por que se hizo el commit"
*	De haber conflictos los muestra
git commit -a 
*	Agregar al ultimo commit, este no se muestra como un nuevo commit en los logs. Se puede especificar un nuevo mensaje
git commit --amend -m "Texto que identifique por que se hizo el commit"

Git push 
*	Subimos al repositorio
git push <origien> <branch>
*	Subimos un tag
git push –tags

Git log
*	Muestra los logs de los commits
git log
*	Muestras los cambios en los commits
git log --oneline --stat
*	Muestra graficos de los commits
git log --oneline –graph

Git diff
*	Muestra los cambios realizados a un archivo
git diff
git diff –staged

Git head
*	Saca un archivo del commit
git reset HEAD <archivo>
*	Devuelve el ultimo commit que se hizo y pone los cambios en staging
git reset --soft HEAD^
*	Devuelve el ultimo commit y todos los cambios
git reset --hard HEAD^
*	Devuelve los 2 ultimo commit y todos los cambios
git reset --hard HEAD^^
*	Rollback merge/commit
git log
git reset --hard <commit_sha>

Git remote 
*	Agregar repositorio remoto
git remote add origin <url>
*	Cambiar de remote
git remote set-url origin <url>
*	Remover repositorio
git remote rm <name/origin>
*	Muestra lista repositorios
git remote -v
*	Muestra los branches remotos
git remote show origin
*	Limpiar todos los branches eliminados
git remote prune origin 

Git branch 
*	Crea un branch
git branch <nameBranch>
*	Lista los branches
git branch
*	Comando -d elimina el branch y lo une al master
git branch -d <nameBranch>
*	Elimina sin preguntar
git branch -D <nameBranch>

Git tag
*	Muestra una lista de todos los tags
git tag
*	Crea un nuevo tags
git tag -a <verison> - m "esta es la versión x"

Git rebase 
*	Los rebase se usan cuando trabajamos con branches esto hace que los branches se pongan al día con el master sin afectar al mismo
*	Une el branch actual con el mastar, esto no se puede ver como un merge
git rebase
*	Cuando se produce un conflicto no das las siguientes opciones:
*	cuando resolvemos los conflictos --continue continua la secuencia del rebase donde se pauso
git rebase --continue 
*	Omite el conflicto y sigue su camino
git rebase --skip
*	Devuelve todo al principio del rebase
git reabse --abort
*	Para hacer un rebase a un branch en especifico
git rebase <nameBranch>

Otros comandos 
*	Lista un estado actual del repositorio con lista de archivos modificados o agregados
git status
*	Quita del HEAD un archivo y le pone el estado de no trabajado
git checkout -- <file>
*	Crea un branch en base a uno online
git checkout -b newlocalbranchname origin/branch-name
*	Busca los cambios nuevos y actualiza el repositorio
git pull origin <nameBranch>
*	Cambiar de branch
git checkout <nameBranch/tagname>
*	Une el branch actual con el especificado
git merge <nameBranch>
*	Verifica cambios en el repositorio online con el local
git fetch
*	Borrar un archivo del repositorio
git rm <archivo> 

Fork
*	Descargar remote de un fork
git remote add upstream <url>
*	Merge con master de un fork
git fetch upstream
git merge upstream/master
