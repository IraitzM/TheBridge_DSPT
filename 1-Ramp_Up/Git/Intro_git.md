# Introducción a Git y GitHub

## Tabla de Contenidos

1. ¿Qué es Git?
2. ¿Por qué necesitamos Git?
3. ¿Cómo funciona Git?
4. Configuración básica de Git
5. Conceptos básicos de Git
6. Comandos básicos de Git
7. ¿Qué es GitHub?
8. Clonando un repositorio de GitHub
9. Referencias y recursos adicionales

## 1. ¿Qué es Git?

Git es un sistema de control de versiones distribuido gratuito y de código abierto diseñado para manejar todo, desde proyectos pequeños hasta muy grandes, con velocidad y eficiencia. Es fácil de aprender y tiene un rendimiento diminuto con operaciones de tipo lightning-fast. 

Git se creó por primera vez en 2005 por Linus Torvalds, el creador del sistema operativo Linux, con el objetivo de rastrear los cambios en el código fuente durante el desarrollo de software. Desde entonces, se ha convertido en el sistema de control de versiones más popular entre los desarrolladores.

## 2. ¿Por qué necesitamos Git?

El desarrollo de software implica mucho más que simplemente escribir código. Implica el seguimiento de los cambios, la colaboración con otros desarrolladores, el pruebas de diferentes características y, a veces, el deshacer cambios que resultan ser una mala idea. Git nos ayuda con todas estas tareas y muchas más.

Git también es muy útil para los científicos de datos y los analistas de datos. Permite el seguimiento de los cambios en los conjuntos de datos, los modelos de aprendizaje automático, los notebooks de Jupyter, etc. Esto facilita enormemente la experimentación y la colaboración.

## 3. ¿Cómo funciona Git?

Git rastrea y registra los cambios en los archivos en un directorio llamado repositorio. Cada vez que realizamos un cambio y lo registramos en Git, Git crea una instantánea del nuestros archivos y almacena una referencia a esa instantánea. Si los archivos no han cambiado, Git no almacena el archivo de nuevo, solo un enlace al archivo idéntico anterior que ya tiene almacenado.

## 4. Configuración básica de Git

Antes de comenzar a usar Git, debes configurar tu nombre y dirección de correo electrónico. Git usa esta información para asociar commits con un identificador.

Abre una terminal y ejecuta los siguientes comandos:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

## 5. Conceptos básicos de Git

Antes de profundizar en los comandos de Git, aqui te dejo algunos conceptos básicos que debes conocer:

- **Repositorio**: Un repositorio es un contenedor para un proyecto que se está rastreando con Git. Contiene todos los archivos del proyecto, así como el historial completo de cambios.
- **Commit**: Un commit es una instantánea de nuestros archivos. Es esencialmente una "versión guardada" de nuestro código.
- **Branch**: Un branch es una versión paralela de un repositorio. Se utiliza para trabajar en diferentes versiones de un proyecto simultaneamente.
- **Staging Area**: El Staging Area es un lugar donde podemos agrupar nuestros cambios en archivos en preparación para un commit.

## 6. Comandos básicos de Git

A continuación se presentan algunos de los comandos básicos que utilizaremos con más frecuencia al trabajar con Git. Si deseas una referencia más completa, consulta la [documentación oficial de Git](https://git-scm.com/doc).

- `git clone <url>`: Clona un repositorio de Git desde la URL especificada.
- `git pull`: Actualiza los cambios del repositorio en remoto en tu repositorio local.

- `git init`: Inicia un nuevo repositorio de Git.
- `git status`: Muestra el estado del repositorio actual.
- `git add <archivo>`: Agrega un archivo al staging area.
- `git commit -m "<mensaje>"`: Crea un nuevo commit con un mensaje descriptivo.
- `git push`: Sube los cambios al repositorio en remoto.
- `git log`: Muestra el historial de commits.
- `git branch <nombre>`: Crea un nuevo branch.
- `git checkout <nombre>`: Cambia al branch especificado.
- `git merge <nombre>`: Fusiona el branch especificado con el branch actual.


[Esquema](/img/git_schema.PNG)

## 7. ¿Qué es GitHub?

GitHub es un servicio de alojamiento en la nube para repositorios de Git. Permite a los desarrolladores almacenar repositorios de Git de manera remota y ofrece muchas características que facilitan la colaboración en proyectos de código abierto y privados. GitHub proporciona una interfaz de usuario basada en web, así como integración con la línea de comandos de Git.

https://github.com/

## 8. Clonando un repositorio de GitHub

Para trabajar en un proyecto almacenado en GitHub, necesitas clonar el repositorio. Esto descargará una copia del repositorio en tu máquina local.

```bash
git clone <URL del repositorio>
```

Esto también podremos realizarlo desde IDE's como VSCode mediante su menu de inicio.

![clonar-vscode](./img/vscode-clone.png)

## 9. Referencias y recursos adicionales

- [Documentación oficial de Git](https://git-scm.com/doc)
- [Guía de GitHub para principiantes](https://guides.github.com/activities/hello-world/)
- [Tutorial interactivo de Git](https://learngitbranching.js.org/)

Espero que esta introducción te haya ayudado a entender qué es Git y GitHub y por qué son herramientas tan importantes para el desarrollo de software y la ciencia de datos. ¡Ahora estás listo para empezar a utilizar Git y GitHub en tus propios proyectos!