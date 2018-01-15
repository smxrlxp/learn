 # Aprenda conceptos básicos en PHP
 
 ## Índice
 
 [Creación e iniciación del documento](https://github.com/acruma/learn/blob/master/spanish/basic/php.md#creaci%C3%B3n-e-iniciaci%C3%B3n-del-documento)
 
 [Comentarios](https://github.com/acruma/learn/blob/master/spanish/basic/php.md#comentarios)
  
 [Variables](https://github.com/acruma/learn/blob/master/spanish/basic/php.md#variables)
 
 [Impresiones en pantalla](https://github.com/acruma/learn/blob/master/spanish/basic/php.md#impresiones-en-pantalla)
 
 [Operaciones aritméticas con números](https://github.com/acruma/learn/blob/master/spanish/basic/php.md#operaciones-aritm%C3%A9ticas-con-n%C3%BAmeros)
 
 [Operaciones con String (cadenas de caracteres)](https://github.com/acruma/learn/blob/master/spanish/basic/php.md#operaciones-con-string-cadenas-de-caracteres)
 
 [Conversiones de Tipos de Datos](https://github.com/acruma/learn/blob/master/spanish/basic/php.md#conversiones-de-tipos-de-datos)
 
 [Documento completo](https://github.com/acruma/learn/blob/master/spanish/basic/php.md#documento-completo)
 
 ---
 ---
  
 ### Creación e iniciación del documento
 
 Para crear un documento en python el nombre de extension debe ser `.php`.
 
 Una vez creado, se debe abrir y cerrar correctamente la etiqueta de documento php.
 
 ```PHP
 
 <?php
 
 ?>
 
 ```
 >NOTA IMPORTANTE: Todo el contenido del documento irá dentro de esta etiqueta y deben estar debidamente cerrados por "punto y coma" ";"
 
---

 ### Comentarios;
 
 Podemos escribir un comentario en una única linea o en múltiples lineas.
 
 ```PHP
 
 //Esto es un comentario

 /*
 Esto es un comentario
 en múltiples líneas 
 */
 
 ```
 

---

### Variables

  "Simbolo" que representa un valor que puede cambiar.

  La sintaxis es la siguiente; 
  
 ```PHP

 // $identificador = valor  ;     (EJ;)
    $altura     =  100   ; //El valor "100" se le asigna a la variable "altura"	

 ```

Tipos básicos de variables

 ```PHP

$edad = 34;		//"Integer" (numeros enteros)
$recorrido = 132.23;  	//"Float"  (numeros reales)
$nombre = "Acruma";    	//"String"  (cadena de caracteres)
$comparativas = true; 	//"Boolean" (valores "True" o "False")

 ```

---

### Impresiones en pantalla

Para mostrar variables en pantalla la sintaxis es la que sigue;

 ```PHP

echo  VALOR A MOSTRAR;

 ```

Ejemplos;

 ```PHP

echo "Esto es una frase";  //Se mostrará en pantalla "Esto es una frase"
echo $edad;		  //Se mostrará en pantalla la variable "edad"

 ```

Para mostrar más de una variable se hace mediante concatenación de variables y/o texto, con un punto "."

 ```PHP

echo $edad . " " . $nombre;
//Se mostrará en pantalla la variable "edad" seguido de un espacio " " y la variable "nombre"

 ```

Para hacer saltos de lineas debemos poner " . PHP_EOL " al final de un echo (EJ)

 ```PHP
 
 echo "Esto es una frase" . PHP_EOL;
 echo $edad;
 
 ```
 
---

### Operaciones aritméticas con números
 
 Como ejemplo, creamos 3 variables.
 
 ```PHP

$a = 3;
$b = 5;
$c = 0;
 
$c = $a + $b;		//Suma 						Resultado: 8.
$c = $a - $b;		//Resta						Resultado: -2.
$c = $a * $b;		//Multiplicación				Resultado: 15.
$c = $a / $b;		//Division					Resultado: 0.6.
$c = $a % $b;		//Modulo (El resto de la division)		Resultado: 2.
 
$c = $c++;		//Incremento de valor en 1.			Resultado: 4.
$c = $c--;		//Decremento de valor en 1.			Resultado: 2.

 ```
 
 El orden de las operaciones se realizan como en matemáticas
 
 ```PHP

$c =  50 - $a  *  6 / -0.5;
$c = (50 - $a) *  6 / -0.5;
$c = (50 - $a) * (6 / -0.5);

 ```

 Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)

 ```PHP

echo $c; //Mostrará el ultimo valor que le asignamos >>> "(50 - a) * (6 / -0.5)" >>> 47 * (-12) = -564

 ```
 
---

### Operaciones con String (cadenas de caracteres)

Concatenación

 ```PHP

$texto1 = "Hola, ";
$texto2 = "soy Acruma";
$texto_concatenado = $texto1 . $texto2;

echo ($texto_concatenado);

 ``` 

Resultado: "Hola, soy Acruma".

Repetición

 ```php

texto_concatenado = str_repeat($texto1, 2);
print($texto_concatenado);
 
 ```
Resultado: "Hola, Hola, ".

---

### Conversiones de Tipos de Datos
 
 ```PHP

 $numero = "123.4";
 $texto  = 123.4;

 ```
 En primer lugar debemos saber que tipo de dato queremos convertir. 
 
 Para ello, mostramos en pantalla que tipo tiene la variable (numero, por ejemplo)

 ```PHP

 echo gettype($numero);	

 ```
 >Nos devolverá "string" - Dato "String"
 
 A continuación convertimos "String" a tipo de dato "Double" y comprobamos de nuevo el tipo de variable
 
 ```PHP
 
 $numero = (double)$numero;
 echo gettype($numero);	
 
 ```
  >Nos devolverá "double" - Dato "Double"
 
 Para ello, mostramos en pantalla que tipo tiene la variable (texto, por ejemplo)
 
 ```PHP
 
 echo gettype($texto);
 
 ``` 
 
 >Nos devolverá "double" - Dato "Double"
 
 A continuación convertimos "Double" a tipo de dato "String" y comprobamos de nuevo el tipo de variable

 ```PHP
 
 $texto = (String) $texto;
 echo gettype($texto);
 
 ```
 >Nos devolverá "string" - Dato "String"
 
 ---
 
 ### Documento completo
 
 A continuación puede copiar todo el codigo y volcarlo en un archivo llamado `python.py`, para poder ejecutar y ver cada una de las impresiones vistas en el tutorial. O incluso para editarlo a voluntad
 
 ```PHP
 
 <?php
 
 // Creación e iniciación del documento
 
 // Para crear un documento en python el nombre de extension debe ser `.php`.
 
 // Una vez creado, se debe abrir y cerrar correctamente la etiqueta de documento php.
 
 // <?PHP 
 
 // ? >

 //NOTA IMPORTANTE: Todo el contenido del documento irá dentro de esta etiqueta
 
//----------------------------------------------------------------------------------------

 // Comentarios;
 
 // Podemos escribir un comentario en una única linea o en múltiples lineas.
 
 // Esto es un comentario

 /*
 Esto es un comentario
 en múltiples líneas 
 */
 
 // NOTA IMPORTANTE; Excepto los comentarios, cada linea debe acabar en "punto y coma" ";"
 
//----------------------------------------------------------------------------------------


 // Variables

 // "Simbolo" que representa un valor que puede cambiar.

 // La sintaxis es la siguiente; 
  
 // $ identificador = valor  ;     (EJ;)
 
$altura =  100; //El valor "100" se le asigna a la variable "altura"	

 // Tipos básicos de variables

$edad = 34;		//"Integer" (numeros enteros)
$recorrido = 132.23;  	//"Double"  (numeros reales)
$nombre = "Acruma";    	//"String"  (cadena de caracteres)
$comparativas = true; 	//"Boolean" (valores "True" o "False")

//----------------------------------------------------------------------------------------


 // Impresiones en pantalla

 // Para mostrar variables en pantalla la sintaxis es la que sigue;

 // echo  VALOR A MOSTRAR;

 // Ejemplos;

echo "Esto es una frase" . PHP_EOL;  //Se mostrará en pantalla "Esto es una frase"
echo $edad . PHP_EOL;		  //Se mostrará en pantalla la variable "edad"

 // Para mostrar más de una variable se hace mediante concatenación de variables y/o texto, con un punto "."

echo $edad . " " . $nombre . PHP_EOL;
 // Se mostrará en pantalla la variable "edad" seguido de un espacio " " y la variable "nombre"

//----------------------------------------------------------------------------------------


 // Operaciones aritméticas con números
 
 // Como ejemplo, creamos 3 variables.
 
 
$a = 3;
$b = 5;
$c = 0;
 
$c = $a + $b;		//Suma 						Resultado: 8.
$c = $a - $b;		//Resta						Resultado: -2.
$c = $a * $b;		//Multiplicación				Resultado: 15.
$c = $a / $b;		//Division					Resultado: 0.6.
$c = $a % $b;		//Modulo (El resto de la division)		Resultado: 2.
 
$c = $c++;		//Incremento de valor en 1.			Resultado: 4.
$c = $c--;		//Decremento de valor en 1.			Resultado: 2.

 
 // El orden de las operaciones se realizan como en matemáticas
 

$c =  50 - $a  *  6 / -0.5;
$c = (50 - $a) *  6 / -0.5;
$c = (50 - $a) * (6 / -0.5);

 // Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 // Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)


echo $c . PHP_EOL; //Mostrará el ultimo valor que le asignamos >>> "(50 - a) * (6 / -0.5)" >>> 47 * (-12) = -564


//----------------------------------------------------------------------------------------


 // Operaciones con String (cadenas de caracteres)

 // Concatenación


$texto1 = "Hola, ";
$texto2 = "soy Acruma";
$texto_concatenado = $texto1 . $texto2;

echo ($texto_concatenado) . PHP_EOL;
 
 // Resultado: "Hola, soy Acruma".

 // Repetición


$texto_concatenado = str_repeat($texto1, 2);
echo ($texto_concatenado) . PHP_EOL;

 // Resultado: "Hola, Hola, ".

//----------------------------------------------------------------------------------------


 // Conversiones de Tipos de Datos
 
$numero = "123.4";
$texto  = 123.4;

 // En primer lugar debemos saber que tipo de dato queremos convertir. 
 
 // Para ello, mostramos en pantalla que tipo tiene la variable (numero, por ejemplo)
 
echo gettype($numero) . PHP_EOL;

 // Nos devolverá "string" - Dato "String"
 
 // A continuación convertimos "String" a tipo de dato "double" y comprobamos de nuevo el tipo de variable

$numero = (double) $numero;
echo gettype($numero) . PHP_EOL;

 // Nos devolverá "double" - Dato "double"
 
 // Para ello, mostramos en pantalla que tipo tiene la variable (texto, por ejemplo)
 
echo gettype($texto) . PHP_EOL;
 
 // Nos devolverá "double" - Dato "double"
 
 // A continuación convertimos "double" a tipo de dato "String" y comprobamos de nuevo el tipo de variable


$texto = (string)$texto;
echo gettype($texto) . PHP_EOL;

 // Nos devolverá "string" - Dato "String"
 
?>

 
 ``` 

By [@acruma](https://github.com/acruma)
