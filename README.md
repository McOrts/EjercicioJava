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
        return salida.Nombre;
  }
  public void setNombre(String nombre) {
        salida.Nombre = nombre;
  }
  public String getApellidos) {
        return salida.Apellidos;
  }
  public void setNombre(String apellidos) {
        salida.Apellidos = apellidos;
  }
  public String getEdad) {
        return salida.Edad;
  }
  public void setNombre(String edad) {
        salida.Edad = edad;
  }
```
  
	• Las funciones necesarias para crear un objeto Alumno y para mostrar por pantalla un objeto Alumno.
	
```java  
public class Alumno {
    private String Nombre;
    private String Apellidos;
    private int Edad;

    public Alumno(String nombre, String apellidos, int edad) {
        salida.Nombre = nombre;
        salida.Apellido = apellidos;
        salida.Edad = edad;
    }

    public void print() {
        System.out.println("Nombre: " + salida.Nombre + ", Apellidos: " + salida.Apellidos + ", Edad: " + salida.Edad); 
    }
  }
```
	• El programa creará un array con 10 alumnos y a continuación mostrará el contenido del array creado junto con los datos de cada alumno.

```java 
Alumno[] alumnoArray = new Alumno[10];
for (int i = 0; i < alumnoArray.length; i++) {
    alumnoArray[i] = new Alumno( "Nombre " + i , "Apellidos " + i , "Edad " + i );
}
for (Alumno a : alumnoArray) {
    a.print();
}
```

## EJERCICIO 2

Programe una web que tenga un formulario, pida los datos personales de una persona y realice las siguientes acciones:

- Una vez rellenos el nombre y los apellidos aparecerá un mensaje indicando “Usted es: nombre+apellidos”

```javascript
<form action="process.php" method="post"> 
Nombre: <input type="text" name="nombre" required/><br/> 
Apellidos: <input type="text" name="apellidos" required/><br/> 
Edad de nacimiento: <input type="date" name="nacimiento" required/><br/> 
<input type="submit" value="Submit"/> 
</form> 
 
<script>
function validaFormulario() { 
 var NombreValor = document.querySelector("input[name='nombre']").value; 
 var ApellidoValor = document.querySelector("input[name='apellido']").value; 
 var NacimientoValor = document.querySelector("input[name='nacimiento']").value; 
 if(NombreValor != "" || ApelidoValor != "") { 
  alert("Usted es: " + NombreValor + " " + ApelidoValor); 
  return false; 
 }
 
</script>
```
- Una vez rellena la fecha de nacimiento muestre un mensaje indicando la edad del usuario de la web.

```javascript
<script>
function calculaEdad(NacimientoValor) {
    var hoy = new Date();
    var fechanacimiento = new Date(NacimientoValor);
    var edad = today.getFullYear() - fechanacimiento.getFullYear();
    var m = hoy.getMonth() - fechanacimiento.getMonth();
    if (m < 0 || (m === 0 && hoy.getDate() < fechanacimiento.getDate())) {
        edad--;
    }
    return edad;
}

function MuestraEdad() { 
 var NacimientoValor = calculaEdad(document.querySelector("input[name='nacimiento']").value);
 alert("Edad " + NacimientoValor); 
}

var el = document.createElement('button');
el.innerText = 'Muestra la edad';
el.onclick = MuestraEdad;
document.body.appendChild(el);

</script>
```

- Cree un botón que al pulsarlo borre los datos del formulario y aparezca el formulario en blanco.

```javascript
<script>

function FormularioBlanco() { 
 document.querySelector("input[name='nombre']").value = "";
 document.querySelector("input[name='apellidos']").value = "";
 document.querySelector("input[name='nacimiento']").value = "";
}

var el = document.createElement('button');
el.innerText = 'Borra formulario';
el.onclick = FormularioBlanco;
document.body.appendChild(el);

</script>
```
