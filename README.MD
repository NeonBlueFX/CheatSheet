#  GIT Cheat Sheet 

## Indice
1. Git

1. Usos

1. Instalacion

1. Como configurarlo

1. Comandos (Hoja de trucos)

1. Glosario de Terminos
---
## - Git

###  Git es un sistema de control de versiones distribuido, lo que significa que un clon local del proyecto es un repositorio de control de versiones completo. Estos repositorios locales plenamente funcionales permiten trabajar sin conexión o de forma remota con facilidad. Los desarrolladores confirman su trabajo localmente y, a continuación, sincronizan su copia del repositorio con la copia en el servidor. Este paradigma es distinto del control de versiones centralizado, donde los clientes deben sincronizar el código con un servidor antes de crear nuevas versiones
---
## - Usos

### Git se ha ideado para posibilitar la ramificación y el etiquetado como procesos de primera importancia (a diferencia de SVN) y las operaciones que afectan a las ramas y las etiquetas (como la fusión o la reversión) también se almacenan en el historial de cambios.
---
## - Instalacion

para instalar git se deben de realizar los siguientes pasos

1. Primero debemos de ingresar a la pagina de git https://git-scm.com

2. Despues de descargar se debe de ingresar al instalador y seguir los pasos en este

3. Al terminar de instalar es recomendable ingresar al command prompt e ingresar el codigo "git --version" para revisar que se instalo completamente y que es la version correcta
---
## Comandos Basicos
git init:
Este comando inicializa un nuevo repositorio en el repositorio local.

    git init << Nombre de directorio >>
git clone:
Este comando inicializa un nuevo repositorio en el repositorio local clonando íntegramente el contenido de un repositorio remoto que le indiquemos mediante una URL.

    git clone << Nombre de Repositorio >>

git add:
se utiliza para comenzar la confirmación de dichos cambios, es necesario pasar todos los archivos que queramos confirmar al área de preparación (staging area).

    git add [ opciones ] < Archivo >

    git add .

git commit:
se utiliza para una vez que tenemos archivos preparados en el área de preparación, confirmar dichos archivos y crear una confirmación de cambios la sentencia utilizada es git commit.

    git commit -m << mensaje >>

git log:
Cada vez que confirmamos cambios (Hacemos un git commit), se crea una confirmación con un número hash identificativo. Dicho número hash determina cada confirmación realizada y será importante para futuras operaciones.

El comando para ver todas las confirmaciones realizadas en nuestro repositorio es Git log.

    git log

git diff:
Este comando permite ver las diferencias que existen entre las confirmaciones que determinemos. Se hace referenciando las confirmaciones mediante su número hash.

    git diff

git reset
Puede descartar confirmaciones que ya no necesita usar utilizando el comando git reset. Hay que tener mucho cuidado con este comando ya que es destructivo y por tanto borrará todos los cambios realizados en el commit que le indiquemos.

    git reset

git revert:
Puede utilizar dicho comando para deshacer de forma segura una confirmación que ya se haya enviado.

    git revert
git tag:
Una etiqueta Git (tag) se utiliza para etiquetar y marcar una confirmación específica en el historial. Las etiquetas se usan comúnmente para indicar versiones de lanzamiento (release), con el nombre de la versión (por ejemplo, v1.0) que es el nombre de la etiqueta.

    git tag
---
## Glosario de Terminos

### repository

Un repositorio es el elemento más básico de GitHub. Es más fácil imaginarlos como carpetas de proyecto. Un repositorio contiene todos los archivos de un proyecto (incluyendo la documentación), y almacena el histórico de modificaciones de cada archivo. Los repositorios pueden tener múltiples colaboradores y pueden ser tanto públicos como privados.

### commit

Un commit se puede entender como la confirmación de una modificación individual en un archivo (o serie de archivos). Es como cuando guardas un archivo, excepto que con Git, cada vez que haces commit se crea un ID único (también conocido como SHA o hash) que te permite registrar qué cambios se hicieron y quién los hizo. Los commits generalmente contienen un mensaje de commit que consiste en una breve descripción de los cambios realizados.

### push

Literalmente, empujar. Se refiere a enviar tus cambios confirmados (tus commits) a un repositorio remoto, como por ejemplo un repositorio alojado en GitHub. Si cambias algo localmente, querrás hacer push de esos cambios para que los demás miembros de tu equipo puedan acceder a ellos.

### pull

Literalmente, tirar. Se refiere a traer los cambios del servidor remoto y combinarlos con tu copia local. Por ejemplo, si alguien ha editado el archivo remoto en el que ambos estáis trabajando, querrás hacer pull de esos cambios a tu copia local para que esté actualizada.
issue
Los issues son sugerencias de mejora, tareas o cuestiones relacionadas con el repositorio o el proyecto. Cualquiera puede crear issues (en un repositorio público), y los moderan los colaboradores del repositorio. Cada issue contiene su propio foro de dissusión, y se puede etiquetar y asignar a un usuario.

### pull request

Los pull requests o, literalmente, solicitudes de tirar, son cambios propuestos para un repositorio que un usuario ha enviado, y que pueden ser aceptados o rechazados por los colaboradores del repositorio. Igual que los issues, los pull requests tienen cada uno su propio foro de discusión.

### branch

Un branch o, literalmente, rama, es una versión paralela de un repositorio. Está contenido dentro del repositorio, pero no afecta al branch principal o master, permitiéndote trabajar libremente sin estropear la versión “real”. Cuando has terminado de realizar los cambios que querías hacer, puedes hacer merge de tu branch al branch principal para publicar tus cambios.

### merge

Literalmente, combinar. Hacer merge toma los cambios de un branch (en el mismo repositorio o también desde un fork), y los aplica en otro. Esto a menudo ocurre como un pull request (que se puede entender como una solicitud de hacer merge), o a través de la línea de comandos. Un merge puede realizarse automáticamente a través de un pull request en la interfaz web de GitHub siempre y cuando no haya cambios que generen conflictos, o puede hacerse siempre via línea de comandos.

### remote

La versión remota es una versión de algo que está alojada en un servidor, muy probablemente GitHub en este contexto. Puede estar conectado a clones locales de forma que los cambios se sincronicen.

### local

La versión local es la copia que tienes del repositorio en tu ordenador, sobre la que trabajas.

### clone

Un clon es la copia de un repositorio que se aloja en tu ordenador, en lugar de en un servidor en alguna parte, o el acto de realizar esa copia. En tu clone puedes editar los archivos en tu editor preferido y utilizar Git para llevar un registro de esas modificaciones sin necesidad de tener conexión a internet. Sin embargo, este clon está conectado a la versión remota de forma que los cambios se puedan sincronizar entre ambos. Puedes hacer push de tus cambios locales a la versión remota para mantenerlas sincronizadas cuando estés online.

### fork

Un fork o, literalmente, tenedor, es una copia personal de un repositorio de otro usuario que se aloja en tu cuenta. Los forks te permiten modificar libremente cualquier proyecto sin alterar el original. Los forks se mantienen relacionados con el original, de manera que puedes enviar un pull request al autor del repositorio original para que lo actualice con tus cambios. También puedes mantener tu fork actualizado haciendo pull de las modificaciones del original.