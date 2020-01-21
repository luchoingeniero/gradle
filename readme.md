# Título del Proyecto

_Tutorial sobre Gradle_
_**Gradle** nos permite ejecutar tareas basadas en lenguajes como **Groovy** y **Java**_

## Comenzando 🚀
_Ahora crearemos una tarea(**task**) llamada **compilar**(puede llamarse como quieras) en la cual ejecutaremos nuestro hola mundo con el **println**_
_**Veamos** en nuestro archivo **build.gradle** agregamos la siguientes lineas_
```
task compilar <<{
    println 'Hola Mundo esta es mi tarea';
}
```


para ejecutar el comando solo es correr
$ gradle -q compilar
o 
$ gradle compilar 

