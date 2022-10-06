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