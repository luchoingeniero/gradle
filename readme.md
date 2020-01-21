gradle acepta codigo groovy veamos el popular println
task compilar <<{
    println 'Hola Mundo esta es mi tarea';
}

para ejecutar el comando solo es correr
$ gradle -q compilar
o 
$ gradle compilar 

