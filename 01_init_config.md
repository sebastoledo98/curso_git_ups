# Parte 01

## Introducción a la parte práctica

Indicar que si desean conocer mucho más sobre git o si quieren revisar más a profundidad los comandos que vamos a aprender entonces se puede acceder al manual de git. En Linux o Mac se puede utilizal el comando `man git-<opcion>` para ver información del comando, o se puede acceder a la página web del manual de git

En MacOS, instalar git desde brew, no utilizar la versión que viene instalada por defecto, puede causar conflictos con las credenciales (este problema también se da en Windows)

***COMPROBAR QUE RERERE NO ESTÉ ACTIVADO EN LA CONFIGURACIÓN***

desactivar esta opción ya que en el 99.9999999% de los casos no se utiliza

## config o La configuración de git (Global)

se indica que git tiene una configuración local (por repositorio) y una configuración global (la que se aplica por defecto a todos los repositorios)

la configuración local puede variar de la global, como se configura git desde la terminal, como se accede a la configuración global, el archivo de configuración y configurar git con nuestros nombres de usuarios y emails

Global

En Linux: ~/.gitconfig

En Windows: C:\Users\<nombre-de-usuario>\.gitconfig

En MacOS: (Buscar)

- Ver configuración:

        git config --list (Ver toda la configuración)
        git config --global --list (Ver solo la configuración global)
        git config list --global (Nueva forma)


- Verificar un valor

        git config --global <seccion>.<llave>
        git config --global --get <seccion>.<llave>
        > valor
        git config get --global <seccion>.<llave> (nueva forma)
Ejemplo

        git config --global rerere.enabled
        >true
        >

- Borrar un valor

        git config --global --unset <seccion>.<llave> (Forma deprecada)
        git config unset --global rerere.enabled (Nueva forma)
Ejemplo

        git config --local --unset rerere.enabled
        git config unset --global rerere.enabled

(verificar cambios)

- Agregar valores

        git config --global --add <seccion>.<llave> <valor> (Forma deprecada) (Con este agregas un valor sin importar que ya exista)
        git config set --local <seccion>.<llave> <valor> (Nueva forma) (Con este agregas o cambias un valor dependiendo de si ya existe)

> Hacer que ellos verifiquen la configuración de git, y si no tienen asignado el nombre de usuario y email hacer que lo agreguen
Para el usuario es `user.name`, para el email es `user.email`

        git config --global --add user.name <tu-nombre-de-usuario>
        git config --global --add user.email <tu-correo-PERSONAL>

Verificar la configuración que todo esté correcto

## init o Inicio de un repositorio

En esta parte se explica el `git init`, se explica un poco de que es un repositorio en términos de git y como se inicia con una rama por defecto

- Iniciar repo

        git init

- Iniciar con otra rama principal

        git init -b <nombre-rama>
        git init --initial-branch=<nombre-rama>

Ejemplo

        git init -b trunk
        git init -b master
        git init -b main

## config --local o configuración local de git

Local

Carpeta .git/config en cualquier sistema operativo

- Para valores locales `--local`

        git config list --local
        git config --local --list

> Agregar un valor global y local y explicar el porque de la diferencia de los valores y cual toma precedencia (el último valor agregado en el local)

Vamos a ir un poco rápido con los comandos, por lo que no nos pararemos a resolver muchas dudas durante esta parte
