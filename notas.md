# Clases

## · Clase 1 - ¿Qué es Git? ·

Git: Es un sistema de control de versiones
Git -> Se usa en la máquina local
Github -> Es el ambiente remoto que permite agregar colaboradores

## · Clase 2 - ¿Por qué usar un sistema de control de versiones como Git ·

Por que git solo guarda los cambios realizados en los archivos o carpetas.

``git init``  
    Comando para iniciar un repositorio

``git add``  
    Comando para que el repositorio sepa de la existencia de uno o varios archivos.

``git commit``
    - Comando que envía los últimos cambios del archivo a la base de datos del sistema de control de versiones GitDB
    - Es una buena practica acompañar el comando commit por commit -m "" Entre las comillas irán comentarios.

``git push``
    Comando para enviar el comit al servidor remoto

``git status``
    Comando que muestra como está el estado de GitDB

``git show``
    Comando que muestra todos los cambios historicos realizados.

``git log file_name``
    permite observar la historia completa de un archivo.

## Clase 3 · Instalando Git y GitBash en Windows ·

## Clase 4 · Instalando Git en OSX ·

## Clase 5 ·Instalando Git en Linux·

## Clase 6 ·Editores de código, archivos binarios y de texto plano·

## Clase 7 ·Terminal y línea de comandos·

## Clase 8 · ¿Que es staging, repositorios y cual es el ciclo básico de trabajo en GitHub? ·

Cuando estamos en una carpeta y escribimos el comando git init:
    - Se crea un área en RAM que se llama staging y allí se van agregando los cambios
    - Se crea el repositorio, es decir, se crea la carpeta .git donde se guardarán todos los archivos al finalizar su edición.
    - El nombre por defecto del repositorio local es **master**

Al ejecutar el comando git add . git add nombreArchivo:
    - Se agregan los archivos al staging area Area de preparación
    - Los archivos pasan a un estado "tracked"

El comando checkout sirve para traer un cambio que está en repositorio pero no está en la carpeta local.

Cada que se ejecuta el comando commit hacia el repositorio se crea una nueva versión del proyecto

### Ciclo básico de trabajo en Git

                          +               +          +                +            +          +
                          |               |          |                |            |          |
                Untraked  |               |  Staged  |                |  Unstaged  |  Traked  |
                          |               |          |                |            |          |
                 +----+   |               |          |                |            |          |
                 | V1 |   |               |          |                |            |          |
                 +--+-+   |               |          |                |            |          |
                    |     |               |          |                |            |          |
                    |     |               |          |                |            |          |
                    |     |  +-------+    |  +----+  |                |            |          |
                    +------->+git add+------>+ V1 |  |                |            |          |
                          |  +-------+    |  +--+-+  |                |            |          |
                          |               |     |    |                |            |          |
                          |               |     |    |  +----------+  |            |  +----+  |
                          |               |     +------>+git commit+----------------->+ V1 |  |
                          |               |          |  +----------+  |            |  +----+  |
                          |               |          |                |            |          |
                          |               |          |                |            |          |
                          |               |          |                |            |          |
                          |               |          |                |  +----+    |  +----+  |
                          |               |          |                |  | V2 +<------+ V1 |  |
                          |               |          |                |  +----+    |  +----+  |
                          |               |          |                |            |          |
                          +               +          +                +            +          +

(realizado en: [asciiflow](http://asciiflow.com/))

## Clase 9 · ¿Qué es un Branch (rama) y cómo funciona un Merge en Git? ·

Por defecto al inicio del proyecto se está en una rama llamada **master** y ahí es donde se registran los cambios en los archivos.
Cada vez que se realiza un commit se crea una nueva versión.
Estandar de ramas:

- **master:** Todo lo que va a produccción
- **development:** Las nuevas funciones, características y experimentos
- **hotfix:**  Errores para unirse a master tan pronto como sea posible.

``Checkout`` Para crear una nueva rama

``Merge`` Para combinar ramas.

![Flujo](https://i.imgur.com/TQASU2Y.png)

## Clase 10 ·Crea un repositorio de Git y haz tu primer commit·

Para devolver el comando `git add .` se usa el comando `git rm --cached`
Es decir, lo que se hace es que se pasa el archivo del estado unstaged al estado untracked.

`git config --list`
Muestra las configuraciones por defecto de git

### Preparar git para el primer commit

`git config --global user.name "user_name"`
Donde **user_name** corresponde un nombre de usuario

`git config --global user.email "user_email"`
Donde **user_email** corresponde al correo electrónico

`cat file_name`
Para poder observar el contenido del archivo **file_name**

`git log`
Ver el historial de cambios:

![log](https://i.imgur.com/o6mzNkx.png)

Se podrá observar que el último cambio es:
commit 0b290e6989c3329ab4bae2adc70cb48e696d99dd (HEAD -> master)

> **0b290e6989c3329ab4bae2adc70cb48e696d99dd** Este número representa el **tag** o el nombre de esa modificación y donde estoy ubicado.
> **HEAD** Esta es la versión "HEAD" en la rama **master**, es decir, es la versión mas reciente.

## Clase 11 · Analizar cambios en los archivos de tu proyecto con Git ·

`git shot file_name`

Muestra los cambios realizados en el archivo **file_name**

`git diff tag_1 tag_2`
Muestra las diferencias entre el commit con **tag_1** y el commit **tag_2**

## Clase 12 · Volver en el tiempo en nuestro repositorio utilizando branches y checkout ·

Mediante el comando `git checkout tagID file_name` donde **tagID** será el identificador, se podrá volver hacia otro commit

## Clase 13 ·Flujo de trabajo básico con un repositorio remoto·

Para iniciar un proyecto desde un repositorio local se inicia mediante el comando `git clone URL` en
donde la **URL** será  la dirección donde está almacenado el repositoro remoto. Al hacer esto, se crea
un repositorio local con todo el historial hasta ese momento y se descargan todos los archivos del proyecto.

Enviar los cambios al repositorio remoto mediante un **push**
![push](https://i.imgur.com/HbHFQNI.png)

Actualizar los cambios desde un repositorio remoto a un repositorio local
![pull](https://i.imgur.com/YsnCPen.png)

## ·Clase 14 - Introducción a las ramas o branches de Git·

`git checkout -b branchName` Para crear una rama y pasar a esa rama, donde **branchName** es el nombre de la rama que se desea crear.

Se puede decir que el **head** es como un puntero al commit donde se está trabajando.

## · Clase 15 - Fusión de ramas con Git merge·

`git -am "mensaje"` Se hace el **add** y el **commit** en un solo comando

Para realizar el `git merge branchName` es necesario ubicarse en la rama **master**.

`git commit -a --amend` Para corregir el mensaje de un commit.

## · Clase 16 - Solución de conflictos al hacer un merge ·

Existirá un conflicto de merge cuando dos o mas personas modifiquen las mismas líneas de un archivo

## · Clase 17 - Uso de GitHub ·

Se crea el repositorio remoto mediante el comando:
`git remote add origin https://github.com/cardonacoder/platziGitCourseNotes.git`

Luego le vamos a decir a git que envie al origen, osea **origin** la rama **master** mediante el comando:
`git push origin master`

Sin embargo sale este error:
![Error](https://i.imgur.com/XuJAq42.png)

Este errors nos dice que el **remoto** tiene trabajo que el **local** no tiene. Entonces primero debemos realizar un
 `git fetch` y un  `git merge` mediante un `git pull origin master` es decir, descargue todo desde la rama remota **origin**
 hasta la rama local **master** sin embargo saldrá el siguiente error:

![Error2](https://i.imgur.com/7r2TXlL.png)

Debido a que existe **historias** que no tienen relación. Una **historia** es un conjunto de commits.
Lo anterior se soluciona mediante el comando `git pull origin master --allow-unrelated-histories`
