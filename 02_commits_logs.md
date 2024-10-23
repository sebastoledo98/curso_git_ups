# Parte 02 Commits y Logs

## Agregar archivos

para esta parte vamos a comenzar a crear solo archivos markdown para mayor simplicidad, pero entender que sirve para cualquier tipo de archivo y directorio

- Crear un archivo `archivo_1.md` y agregar texto con un editor (cualquiera)
- Ver el estado del repo

        git status
Vemos que ahora tenemos un archivo que no está en nuestro repo
- Agregar el archivo al git

        git add <nombre>.<extension> (Para archivos)
        git add <nombre>/ (para directorios)
Se puede utilizar expresiones regulares para agregar archivos

        git add *.txt (agrega todos los archivos con extension .txt)
        git add carpeta/*.txt (agrega todos los archivos con extension .txt dentro del subdirectorio "carpeta")
O para agregar todos los archivos

        git add .
Se agregan todos los archivos al repo

***EXPLICAR SOBRE EL GITIGNORE Y COMO SE CONFIGURA DE MANERA CORRECTA***

## El Primer commit de todos

`git commit` es para aceptar y asentar los cambios en el repo, esto siempre debe ir acompañado de un mensaje con tags y una explicación breve de la que se realizó

Ver el estado del repo
- Realizar un commit CON UN MENSAJE

        git commit -m "Mensaje"
Se realizó un commit con el mensaje que pusimos

Ahora vamos a agregar mas texto en el archivo para tener mas commits
> Agregar mas texto al archivo y hacer un `git status`, resaltar la diferencia con el archivo antes agregado

- Si se desea agregar SOLO LOS ARCHIVOS MODIFICADOS y realizar commit al mismo tiempo se puede utilizar

        git commit -am "Mensaje"
Hemos hecho dos commits en un corto tiempo, realmente esto no es bueno cuando se esté en un proyecto ya profesional

Nunca se deben realizar commits por cada pequeño cambio que se realice, esto llena el historial de commits y resulta un dolor de cabeza al momento de buscar cambios que agreguen bugs o que rompan todo el proyecto

## log o ver el historial de commits (y a quien culpar por los cambios)

***EXPLICAR EL CONCEPTO DEL BLAME EN GIT***

Tenemos los dos commits realizados, revisemos lo que se ha realizado
- Ver el historial de commits

        git log
***EXPLICAR EL CONCEPTO DE HEAD Y EL HASH DEL COMMIT***

- Si se desea un historial más compacto

        git log --oneline
- Si se desea con un gráfico

        git log --graph
- Se pueden combinar los dos

        git log --oneline --graph

Vemos los commits realizados, la fecha y hora, y a quien le van a despedir por esos cambios

***EXPLICAR DE FORMA BREVE EL `git cat-file` Y COMO FUNCIONA DE MANERA INTERNA EL GIT***

De esta forma ya tenemos nuestras bases de git, estas dos partes son las más importantes al momento de utilizar git, de nuevo, si quieren saber más sobre como funcionan los comandos vistos hasta ahora pueden utilizar el manual, es la mejor forma de entender todo lo que se puede realizar con git
