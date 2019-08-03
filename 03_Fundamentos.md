# Fundamentos de Git

## Tres estados de los archivos

Git tiene tres estados principales en los que se pueden encontrar tus archivos:

- **Commited** (confirmado): Los datos están almacenados de manera segura en la base de datos local.
- **Modified** (modificado): El archivo ha sido modificado pero todavía no e ha confirmado a la base de datos local.
- **Staged** (preparado): Se ha marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación.

Esto nos lleva a las tres secciones principales de un proyecto de Git:

- **Git directory** (directorio de Git): Es donde se almacenan los metadatos y la base de datos de objetos para tu proyecto. Es lo que se copia cuando clonas un repositorio.
- **Working directory** (directorio de trabajo): es una copia de una versión del proyecto. Estos archivos se sacan de la base
de datos comprimida en el directorio de Git, y se colocan en disco para que los puedas usar o modificar.
- **Staging Area** (área de preparación): Es un archivo que almacena información acerca de lo que va a ir en tu próxima confirmación.

El flujo de trabajo básico de Git corresponde a lo siguiente:

1. Modificas archivos en tu _Working Directory_.
2. Preparas tus archivos moviendolos a tu área de preparación.
3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.