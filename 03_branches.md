# Parte 03

## Ramas

pero que pasa si mas de una persona trabaja en el mismo proyecto. para eso están las ramas

un repo se puede entender como un árbol, donde la principal es el tronco del árbol, es decir, desde donde todo el repo se inicia, y las ramas, donde cada persona o cada característica del programa se trabaja, esto se hace para que se pueda modificar o agregar funcionalidad al proyecto sin tener que cambiar el código inicial, y al final todo se vuelve a unir en la rama principal, en concepto, ya veremos más adelante que no necesariamente se así, se pueden tener varias ramas y al final unirse en otra rama diferente para mantener un mejor control de versiones

- Para crear una rama

        git branch <nombre-rama>

- Para cambiar de rama

        git switch <nombre-rama>
Se puede utilizar el `checkout`, pero con branch se tienen muchas mas operaciones que se pueden realizar sobre una rama, como listar todas las ramas, ver ramas remotas, ver ramas que se han realizado merge, borrar ramas, cambiar el nombre de las ramas, crear copias de las ramas, etc; lo mismo con switch, estos son comandos especializados para las operaciones y se recomiendan utilizar estas antes de `checkout`, para más información, RTFM

- Con checkout

        git checkout -b <nombre-rama> (Se crea una rama y se cambia a esa rama)
