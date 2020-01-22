# Tutorial sobre Gradle

_**Gradle** nos permite ejecutar tareas basadas en lenguajes como **Groovy** y **Java**_

## Hola Mundo
_Ahora crearemos una tarea(**task**) llamada **compilar**(puede llamarse como quieras) en la cual ejecutaremos nuestro hola mundo con el **println**_

En nuestro archivo **build.gradle** agregamos la siguientes lineas

```
task compilar {
    println 'Hola Mundo esta es mi tarea';
}
```
para ejecutar la tarea nos ubicamos en nuestro directorio de trabajo
```
$ gradle -q compilar
```
Tenemos como salida de Consola
```
Hola Mundo esta es mi tarea
```
## Declaracion y Acceso de variables
_Ahora veremos como declarar variables y como accederlas para esto utilizaremos el objeto **ext** existen dos formar de utilizarlo tal como se muestra a continuacion_
```
ext{
    miAtributo = "atributo1"
    otroAtributo ="atributo2"
}
```
la otra forma para declarar valores accediento directamente al objecto ext
```
ext.miAtributo = "atributo1"
ext.otroAtributo = "atributo2"
```
_Realicemos una tarea para ver el ejemplo en accion la llamaremos variables_
```
task variablesTask {
    ext{
    miAtributo = "atributo1"
    
    }
    ext.otroAtributo ="atributo2"

    println 'Esta es mi tarea variables';
    println 'valor almacenado en miAtributo '+miAtributo
    println 'valor almacenado en otroAtributo '+otroAtributo
}
```
_Ahora si queremos acceder a estas variables desde otra tarea(**task**) simplemente lo hacemos accediendo a la tarea y luego el atributo ejemplo_
```
task otraTarea{
    println 'Accediendo a los atributos desde otra tarea '+ variablesTask.miAtributo
}
```
