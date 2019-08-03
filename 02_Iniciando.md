# Iniciando

## I. Instalación

El instalador de Git y las instrucciones de instalación en detalle pueden ser encontradas en la página oficial de Git (click (aquí)[https://git-scm.com/downloads]).

Si se instala un programa de manejo de repositorios con Git con interfaz gráfica (como Sourcetree, GitKraken u otro), Git se instalará automáticamente. Sin embargo, en Windows debes asegurarte de que Git esté en las variables de entorno si quieres utilizarlo desde la consola de comandos.

Si usas _Visual Studio Code_ recomiendo instalar las siguientes extensiones:

![Extensiones Visual Studio para GIT](images/git_extensions.png)

--

## II. Configurar usuario

Para configurar el usuario global de git corre los siguientes comandos:

```bash

git config --global user.name "Tu Nombre"

git config --global user.email ejemplo@ejemplo.ej

git config --global user.password "tu_contraseña_aqui"

```

Al hacer la configuracion global, se asigna esta configuración a todos lo repositorios de tu computador. Si requieres tener una configuración específica para uno de tus repositorios, debes cambiar _--global_ por _--local_ y los comandos deben ser ejecutados dentro de la carpeta del repositorio.

Para consultar las configuraciones, usen el siguiente comando:

```bash

git config --list

```

## III. Iniciar repositorio

Existen dos opciones para iniciar un repositorio: Crear un repositorio desde cero, o clonar un repositorio ya existente.

1. **Clonar un repositorio**

En Git, **clonar** significa que iniciaras un repositorio local de git (en tu computador) descargando un el código de un repositorio ya existente.

Primero debes obtener el link de clonación del repositorio, para ello accede a la página del repositorio y busca la opción "clonar", y copias el link de clonación con la opción HTTPS (más adelante veremos otros métodos de clonación). En la siguiente imagen se puede apreciar un ejemplo de cómo encontrar el link de clonación para un repositorio en _GitHub_:

<img src="images\clone_github_example_edited.png" alt="Clonación repositorio GitHub" width=800/>

Luego ese link utilizarlo en el siguiente comando:

```bash
git clone link-to-repository
```

Donde _link-to-repository_ es el link que acabas de copiar.

Cabe aclarar que este comando creará una carpeta con el mismo nombre del repositorio que se clone, y que dentro de dicha carpeta está el repositorio en sí.

2. **Crear repositorio desde cero**

Primero colocate en la carpeta de tu proyecto con la consola de comandos y corre el comando:

```bash
git init
```

Eso dará inicio a tu **repositorio local**. Para poder compartir el repositorio con otras personas, debes configurar el "remoto".

El **remoto** (_remote_ en inglés) es un repositorio que está montado sobre un servidor (como GitHub, GitLab, Bitbucket, entre otros) para poder compartir con el público o con miembros de tu equipo.

Para configurar el remoto de tu repositorio local debes primero crear un repositorio vacío en uno de los servidores, obtener el link de clonación

--

<div style="text-align: right">
    <a href="03_Fundamentos.md"> Siguiente capítulo (Fundamentos de Git) &rarr; </a>
</div>