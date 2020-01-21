# Tutorial sobre Gradle

_**Gradle** nos permite ejecutar tareas basadas en lenguajes como **Groovy** y **Java**_

## Comenzando 🚀
_Ahora crearemos una tarea(**task**) llamada **compilar**(puede llamarse como quieras) en la cual ejecutaremos nuestro hola mundo con el **println**_

En nuestro archivo **build.gradle** agregamos la siguientes lineas

```
task compilar <<{
    println 'Hola Mundo esta es mi tarea';
}
```
para ejecutar la tarea nos ubicamos en nuestro directorio de trabajo
```
$ gradle -q compilar
```


