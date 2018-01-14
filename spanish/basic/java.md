 
 ### Comentarios;
 
 Podemos escribir un comentario en una única linea o en múltiples lineas.
 
 ```Java
 //Esto es un comentario

/*
 Esto es un comentario
 en múltiples líneas 
*/
 ```
 NOTA IMPORTANTE: Debemos tener cuidado, ya que JAVA es Case Sensitive es decir distingue mayúsculas y minúsculas.
 
 ---
 
 ### Creación e iniciación del documento
 
 Para crear un documento java el nombre de extension debe ser `.java`
 
 En primer paso, debemos crear una "class" ( clase ). Con el nombre que le asignemos al archivo. (DEBE EMPEZAR POR LETRA) EJ:

 Este archivo se llama "java"
```Java
public class java{ 
}
```
 Creamos una funcion "main" dentro de class
 ```
public static void main(String[] args){
}
 ```
 
 Por lo tanto el codigo de inicio de un archivo en java debe ser como sigue;
 
 ```Java
 public class java{
   public static void main(String[] args){
   }
}
 ```
 En tutoriales más avanzados indicaremos que es una clase "class" y que es una función.
 
 >NOTA IMPORTANTE; Al final de cada linea de codigo dentro de las funciones, deben acabar en ; (punto y coma)

---

### Variables

  "Simbolo" que representa un valor que puede cambiar.

  La sintaxis es la siguiente; 
  
```Java
// tipo_dato identificador = valor  ;     (EJ;)
      int       altura     =  100   ;     //El valor "100" se le asigna a la variable "altura"	
```
//Tipos básicos de variables

```Java
int edad = 34; 			//"Integer" (numeros enteros)
double recorrido = 132.23;   	//"Double"  (numeros reales)
String nombre = "Acruma";    	//"String"  (cadena de caracteres)
boolean	comparativas = true; 	//"Boolean" (valores "true" o "false")
```

---

### Impresiones en pantalla

Para mostrar variables en pantalla la sintaxis es la que sigue;

```Java
System.out.println( VALOR A MOSTRAR );
```
Ejemplos;

```Java
System.out.println("Esto es una frase"); //Se mostrará en pantalla "Esto es una frase"
System.out.println(edad);		 //Se mostrará en pantalla la variable "edad"
```
Para mostrar más de una variable se hace mediante concatenación de variables y/o texto, con un "+"

```Java
System.out.println(edad + " " + nombre); 
//Se mostrará en pantalla la variable "edad" seguido de un espacio " " y la variable "nombre"
```
---

### Operaciones aritméticas con números
 
 Como ejemplo, creamos 3 variables.
 
 ```
 int a = 3;
 int b = 5;
 double c = 0; //Esta variable es un "numero real" por si acaba teniendo decimales (suele ocurrir en divisiones)
 
 c = a + b;		//Suma 						Resultado: 8.
 c = a - b;		//Resta						Resultado: -2.
 c = a * b;		//Multiplicación				Resultado: 15.
 c = a / b;		//Division					Resultado: 0.6.
 c = a % b;		//Modulo (El resto de la division)		Resultado: 2.
 
 c = c + 1;		//Incremento de valor en 1.			Resultado: 4.
 c = c - 1;		//Decremento de valor en 1.			Resultado: 2.
 ```
 
 El orden de las operaciones se realizan como en matemáticas
 
```Java
 c =  50 - a  *  6 / -0.5;
 c = (50 - a) *  6 / -0.5;
 c = (50 - a) * (6 / -0.5);
 ```
 Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)

```Java
System.out.println(c); //Mostrará el ultimo valor que le asignamos >>> "(50 - a) * (6 / -0.5)" >>> 47 * (-12) = -564
```
---

### Operaciones con String (cadenas de caracteres)

```Java
String texto1 = "Hola, ";
String texto2 = "soy Acruma";
String texto_concatenado = texto1 + texto2;				//Concatenación Resultado: "Hola, soy Acruma".

texto_concatenado = new String(new char[2]).replace("\0", texto1); 	//Repetición    Resultado: "Hola, Hola, ".

System.out.println(texto_concatenado);
```
---

### Conversiones de Tipos de Datos
 
 ```Java
 String numero = "123.4";
 double texto  = 123.4;
 ```
 En primer lugar debemos saber que tipo de dato queremos convertir. 
 
 Para ello, mostramos en pantalla que tipo tiene la variable (numero, por ejemplo)
 ```Java
 System.out.println(((Object) numero).getClass().getName());  		//Nos devolverá "java.lang.String" - Dato "String"
 double numero_convertido = Double.parseDouble(numero);		  	//Convertimos "String" a tipo de dato "Double"
 System.out.println(((Object) numero_convertido).getClass().getName()); //Nos devuelve "java.lang.Double"
 ```
 
 Para ello, mostramos en pantalla que tipo tiene la variable (texto, por ejemplo)
 ```Java
 System.out.println(((Object) texto).getClass().getName());  		//Nos devolverá "java.lang.Double" - Dato "Double"
 String texto_convertido = String.valueOf(texto);		  	//Convertimos "Double" a tipo de dato "String"
 System.out.println(((Object) texto_convertido).getClass().getName());  //Nos devuelve "java.lang.String"
 ```
