# Ejercicio Java

## EJERCICIO 1

Cree una clase Alumno en Java con atributos:

   1. Nombre de tipo String y ámbito privado.
```java
public class Alumnos {
    private String Nombre;
}
```

   2. Apellidos de tipo String y ámbito privado
```java
public class Alumnos {
    private String Apellidos;
}
```

   3. Edad de tipo Int de ámbito privado.
```java
public class Alumnos {
    private int Edad;
}
```

Incluya las siguientes funciones:

	• Los constructores necesarios para crear un objeto alumno.
```java
public class Alumno {
    private String Nombre;
    private String Apellidos;
    private int Edad;

    public Alumno(String nombre) {
        salida.Nombre = nombre;
    }
    public Alumno(String apellidos) {
        salida.Nombre = apellidos;
    }
    public Alumno(String edad) {
        salida.Edad = edad;
    }
}
```

	• Los métodos (get() y set()) que permitan consultar y modificar estos atributos.
```java  
  public String getNombre() {
        return this.Nombre;
  }
  public void setNombre(String nombre) {
        salida.Nombre = nombre;
  }
  public String getApellidos) {
        return this.Apellidos;
  }
  public void setNombre(String apellidos) {
        salida.Apellidos = apellidos;
  }
  public String getEdad) {
        return this.Edad;
  }
  public void setNombre(String edad) {
        salida.Edad = edad;
  }
```
  
	• Las funciones necesarias para crear un objeto Alumno y para mostrar por pantalla un objeto Alumno.
	
```java  
public class Alumno {
    private String Nombre;
    private String Apellido;
    private int Edad;

    public Alumno(String nombre, String apellido, int edad) {
        salida.Nombre = nombre;
        salida.Apellido = apellido;
        salida.Edad = edad;
    }

    public void print() {
        System.out.println("Nombre: " + salida.Nombre + ", Apellido: " + salida.Apellido + ", Edad: " + salida.Edad); 
    }
  }
```
	• El programa creará un array con 10 alumnos y a continuación mostrará el contenido del array creado junto con los datos de cada alumno.

```java 
Alumno[] alumnoArray = new Alumno[10];
for (int i = 0; i < alumnoArray.length; i++) {
    alumnoArray[i] = new Alumno( "Name " + i , "Surname " + i );
}
for (Alumno a : alumnoArray) {
    a.print();
}
```

## EJERCICIO 2

Programe una web que tenga un formulario, pida los datos personales de una persona y realice las siguientes acciones:

	• Una vez rellenos el nombre y los apellidos aparecerá un mensaje indicando “Usted es: nombre+apellidos”

	• Una vez rellena la fecha de nacimiento muestre un mensaje indicando la edad del usuario de la web.

Cree un botón que al pulsarlo borre los datos del formulario y aparezca el formulario en blanco.
 
