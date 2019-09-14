Clase 1(
¿Qué es Git?
    Git: Es un sistema de control de versiones
    Git -> Se usa en la máquina local
    Github -> Es el ambiente remoto que permite agregar colaboradores
)
Clase 2(
    
¿Por qué usar un sistema de control de versiones como Git?
    Git solo guarda los cambios realizados en los archivos o carpetas.
    git init -> Comando para iniciar un repositorio
    git add -> Comando para que el repositorio sepa de la existencia de uno o varios archivos. 
    git commit -> (
        - Comando que envía los últimos cambios del archivo a la base de datos del sistema de control de versiones (GitDB)
        - Es una buena practica acompañar el comando commit por commit -m "" Entre las comillas irán comentarios.

    ) 
    
    
    git push -> Comando para enviar el comit al servidor remoto
    git status -> Comando que muestra como está el estado de GitDB
    git show -> Comando que muestra todos los cambios historicos realizados.
    git log file_name -> permite observar la historia completa de un archivo.
)
Clase 3 ( Instalando Git y GitBash en Windows )
Clase 4 ( Instalando Git en OSX )
Clase 5 ( Instalando Git en Linux )
Clase 6 ( Editores de código, archivos binarios y de texto plano )
Clase 7 ( Terminal y línea de comandos )
Clase 8 (
    ¿Que es staging, repositorios y cual es el ciclo básico de trabajo en GitHub?
        Cuando estamos en una carpeta y escribimos el comando git init
            - Se crea un área en RAM que se llama staging y allí se van agregando los cambios
            - Se crea el repositorio, es decir, se crea la carpeta .git donde se guardarán todos los archivos al finalizar su edición.
            - El nombre por defecto del repositorio local es master
    
        Al ejecutar el comando git add . (git add nombreArchivo):
            - Se agregan los archivos al staging area (Area de preparación)
            - Los archivos pasan a un estado "tracked"

        El comando checkout sirve para traer un cambio que está en repositorio pero no está en la carpeta local.

        Cada que se ejecuta el comando commit hacia el repositorio se crea una nueva versión del proyecto

        Ciclo básico de trabajo en Git ( http://asciiflow.com/ )
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


















    
)
Clase 9(
    Un proyecto puede tener cuantas ramas se desee
    Un
)