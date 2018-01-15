 # Aprenda conceptos básicos en PowerShell
 
 ## Índice
 
 [Creación e iniciación del documento](https://github.com/acruma/learn/blob/master/spanish/basic/powershell.md#creaci%C3%B3n-e-iniciaci%C3%B3n-del-documento)
 
 [Comentarios](https://github.com/acruma/learn/blob/master/spanish/basic/powershell.md#comentarios)
  
 [Variables](https://github.com/acruma/learn/blob/master/spanish/basic/powershell.md#variables)
 
 [Impresiones en pantalla](https://github.com/acruma/learn/blob/master/spanish/basic/powershell.md#impresiones-en-pantalla)
 
 [Operaciones aritméticas con números](https://github.com/acruma/learn/blob/master/spanish/basic/powershell.md#operaciones-aritm%C3%A9ticas-con-n%C3%BAmeros)
 
 [Operaciones con String (cadenas de caracteres)](https://github.com/acruma/learn/blob/master/spanish/basic/powershell.md#operaciones-con-string-cadenas-de-caracteres)
 
 [Conversiones de Tipos de Datos](https://github.com/acruma/learn/blob/master/spanish/basic/powershell.md#conversiones-de-tipos-de-datos)
 
 [Documento completo](https://github.com/acruma/learn/blob/master/spanish/basic/powershell.md#documento-completo)
 
 ---
 ---
  
 ### Creación e iniciación del documento
 
 Para crear un documento en PowerShell el nombre de extension debe ser `.ps1`.
 
 ---

 ### Comentarios
 
 Podemos escribir un comentario en una única linea o en múltiples lineas.
 
 ```powershell
 
 #Esto es un comentario

 <#
 Esto es un comentario
 en múltiples líneas 
 #>
 
 ```
 

---

### Variables

  "Simbolo" que representa un valor que puede cambiar.

  La sintaxis es la siguiente 
  
 ```powershell

 # $identificador = valor       (EJ)
    $altura       =  100    #El valor "100" se le asigna a la variable "altura"	

 ```

Tipos básicos de variables

 ```powershell

$edad = 34		#"Integer" (numeros enteros)
$recorrido = 132.23  	#"Double"  (numeros reales)
$nombre = "Acruma"    	#"String"  (cadena de caracteres)
$comparativas = $true 	#"Boolean" (valores "True" o "False")

 ```

---

### Impresiones en pantalla

>NOTA IMPORTANTE: En este tutorial usaremos para imprimir por pantalla el comando `echo` . Aunque en `PowerShell` este comando se traduce en `Write-Host`

En PowerShell hay que diferenciar entre comillas simples `'` y comillas dobles `"`

Los datos introducidos entre comillas simples `' '` se mostraran tal y como aparece el texto entre ellas. EJ;


 ```powershell
 
$VALOR = 123
echo  '$VALOR A MOSTRAR'
#Se mostrará en pantalla -> $VALOR A MOSTRAR

 ```
 
En cambio si usamos comillas dobles `" "` se mostrarán las variables dentro de ellas. EJ;

 ```powershell
 
$VALOR = 123
echo  "$VALOR A MOSTRAR"
#Se mostrará en pantalla -> 123 A MOSTRAR

 ```

Podemos hacer combinaciones de ambas comillas en una misma sentencia con un pequeño cambio, debemos poner una acentuación ` antes de la variable para que muestre el nombre de la variable y no su valor . EJ;

 ```powershell

$VALOR = 123
echo  " `$VALOR A MOSTRAR"
#Se mostrará en pantalla -> $VALOR A MOSTRAR

 ```

Para mostrar más de una variable se hace mediante concatenación de variables y/o texto

 ```powershell

echo "$edad $nombre"
#Se mostrará en pantalla la variable "edad" seguido de un espacio " " y la variable "nombre"

 ```
>NOTA IMPORTANTE: Si escribimos todo entre comillas `"` aparecerá todo en la misma linea. Si lo hacemos cada uno por separado saltará de linea.

 ```powershell

echo $edad $nombre
#Se mostrará en pantalla las variables en distintas lineas;
#"edad"
#"nombre"

 ```
 
---

### Operaciones aritméticas con números
 
 Como ejemplo, creamos 3 variables.
 
 ```powershell

$a = 3
$b = 5
$c = 0
 
$c = $a + $b		#Suma 						Resultado: 8.
$c = $a - $b		#Resta						Resultado: -2.
$c = $a * $b		#Multiplicación				Resultado: 15.
$c = $a / $b		#Division					Resultado: 0.6.
$c = $a % $b		#Modulo (El resto de la division)		Resultado: 2.
 
$c = $c++		#Incremento de valor en 1.			Resultado: 4.
$c = $c--		#Decremento de valor en 1.			Resultado: 2.

 ```
 
 El orden de las operaciones se realizan como en matemáticas
 
 ```powershell

$c =  50 - $a  *  6 / -0.5
$c = (50 - $a) *  6 / -0.5
$c = (50 - $a) * (6 / -0.5)

 ```

 Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)

 ```powershell

echo $c #Mostrará el ultimo valor que le asignamos >>> "(50 - a) * (6 / -0.5)" >>> 47 * (-12) = -564

 ```
 
---

### Operaciones con String (cadenas de caracteres)

Concatenación

 ```powershell

$texto1 = "Hola, "
$texto2 = "soy Acruma"
$texto_concatenado = "$texto1 $texto2"

echo $texto_concatenado

 ``` 

Resultado: "Hola, soy Acruma".

Repetición

 ```powershell

$texto_concatenado = $texto1 * 2
echo $texto_concatenado
 
 ```
Resultado: "Hola, Hola, ".

---

### Conversiones de Tipos de Datos
 
 ```powershell

 $numero = "123.4"
 $texto  = 123.4

 ```
 En primer lugar debemos saber que tipo de dato queremos convertir. 
 
 Para ello, mostramos en pantalla que tipo tiene la variable (numero, por ejemplo)

 ```powershell

 $numero.GetType()	

 ```
 
 >Nos devolverá: IsPublic IsSerial Name                                     BaseType            
 >				 -------- -------- ----                                     --------            
 >				 True     True     String                                   System.Object   
 
 A continuación convertimos "String" a tipo de dato "Double" y comprobamos de nuevo el tipo de variable
 
 ```powershell
 
 $numero_convertido = [double]$numero
 $numero_convertido.GetType()
 
 ```
 
 >Nos devolverá: IsPublic IsSerial Name                                     BaseType            
 >				 -------- -------- ----                                     --------            
 >				 True     True     Double                                   System.Object   
 
 Para ello, mostramos en pantalla que tipo tiene la variable (texto, por ejemplo)
 
 ```powershell
 
 $texto.GetType()
 
 ``` 
 
 >Nos devolverá: IsPublic IsSerial Name                                     BaseType            
 >				 -------- -------- ----                                     --------            
 >				 True     True     Double                                   System.Object 
  
 A continuación convertimos "Double" a tipo de dato "String" y comprobamos de nuevo el tipo de variable

 ```powershell
 
 $texto_convertido = [string]$texto
 $texto_convertido.GetType()
 
 ```
 >Nos devolverá: IsPublic IsSerial Name                                     BaseType            
 >				 -------- -------- ----                                     --------            
 >				 True     True     String                                   System.Object   
 
 ---
 
 ### Documento completo
 
 A continuación puede copiar todo el codigo y volcarlo en un archivo llamado `python.py`, para poder ejecutar y ver cada una de las impresiones vistas en el tutorial. O incluso para editarlo a voluntad
 
 ```powershell
 
  # Creación e iniciación del documento
 
 # Para crear un documento en PowerShell el nombre de extension debe ser `.ps1`.
 
 # Comentarios
 
 # Podemos escribir un comentario en una única linea o en múltiples lineas.
  
 #Esto es un comentario

 <#
 Esto es un comentario
 en múltiples líneas 
 #>
 
 # Variables

 # "Simbolo" que representa un valor que puede cambiar.

 # La sintaxis es la siguiente 
  
 # $identificador = valor       (EJ)
    $altura       =  100    #El valor "100" se le asigna a la variable "altura"	

 # Tipos básicos de variables

$edad = 34		#"Integer" (numeros enteros)
$recorrido = 132.23  	#"Double"  (numeros reales)
$nombre = "Acruma"    	#"String"  (cadena de caracteres)
$comparativas = $true 	#"Boolean" (valores "True" o "False")

 # Impresiones en pantalla

 # NOTA IMPORTANTE: En este tutorial usaremos para imprimir por pantalla el comando `echo` . Aunque en `PowerShell` este comando se traduce en `Write-Host`

 # En PowerShell hay que diferenciar entre comillas simples `'` y comillas dobles `"`

 # Los datos introducidos entre comillas simples `' '` se mostraran tal y como aparece el texto entre ellas. EJ;
 
$VALOR = 123
echo  '$VALOR A MOSTRAR'
 # Se mostrará en pantalla -# $VALOR A MOSTRAR
 
 # En cambio si usamos comillas dobles `" "` se mostrarán las variables dentro de ellas. EJ;
 
$VALOR = 123
echo  "$VALOR A MOSTRAR"
 # Se mostrará en pantalla -# 123 A MOSTRAR

 # Podemos hacer combinaciones de ambas comillas en una misma sentencia con un pequeño cambio, debemos poner una acentuación ` antes de la variable para que muestre el nombre de la variable y no su valor . EJ;

$VALOR = 123
echo  " `$VALOR A MOSTRAR"
 # Se mostrará en pantalla -# $VALOR A MOSTRAR

 # Para mostrar más de una variable se hace mediante concatenación de variables y/o texto

echo "$edad $nombre"
 # Se mostrará en pantalla la variable "edad" seguido de un espacio " " y la variable "nombre"
 
 # NOTA IMPORTANTE: Si escribimos todo entre comillas `"` aparecerá todo en la misma linea. Si lo hacemos cada uno por separado saltará de linea.

echo $edad $nombre
 # Se mostrará en pantalla las variables en distintas lineas;
 # "edad"
 # "nombre"

 # Operaciones aritméticas con números
 
 # Como ejemplo, creamos 3 variables.

$a = 3
$b = 5
$c = 0
 
$c = $a + $b		#Suma 						Resultado: 8.
$c = $a - $b		#Resta						Resultado: -2.
$c = $a * $b		#Multiplicación				Resultado: 15.
$c = $a / $b		#Division					Resultado: 0.6.
$c = $a % $b		#Modulo (El resto de la division)		Resultado: 2.
 
$c = $c++		#Incremento de valor en 1.			Resultado: 4.
$c = $c--		#Decremento de valor en 1.			Resultado: 2.
 
 # El orden de las operaciones se realizan como en matemáticas

$c =  50 - $a  *  6 / -0.5
$c = (50 - $a) *  6 / -0.5
$c = (50 - $a) * (6 / -0.5)

 # Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 # Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)

echo $c #Mostrará el ultimo valor que le asignamos # "(50 - a) * (6 / -0.5)" # 47 * (-12) = -564

 # Operaciones con String (cadenas de caracteres)

 # Concatenación

$texto1 = "Hola, "
$texto2 = "soy Acruma"
$texto_concatenado = "$texto1 $texto2"

echo $texto_concatenado

 # Resultado: "Hola, soy Acruma".

 # Repetición

$texto_concatenado = $texto1 * 2
echo $texto_concatenado
  
 # Resultado: "Hola, Hola, ".

 # Conversiones de Tipos de Datos
 
 $numero = "123.4"
 $texto  = 123.4

 # En primer lugar debemos saber que tipo de dato queremos convertir. 
 
 # Para ello, mostramos en pantalla que tipo tiene la variable (numero, por ejemplo)

 $numero.GetType()	
 
 # Nos devolverá: IsPublic IsSerial Name                                     BaseType            
 #				 -- -- -                                     --            
 #				 True     True     String                                   System.Object   
 
 # A continuación convertimos "String" a tipo de dato "Double" y comprobamos de nuevo el tipo de variable
  
 $numero_convertido = [double]$numero
 $numero_convertido.GetType()
  
 # Nos devolverá: IsPublic IsSerial Name                                     BaseType            
 #				 -- -- -                                     --            
 #				 True     True     Double                                   System.Object   
 
 # Para ello, mostramos en pantalla que tipo tiene la variable (texto, por ejemplo)
 
 $texto.GetType()
 
 # Nos devolverá: IsPublic IsSerial Name                                     BaseType            
 #				 -- -- -                                     --            
 #				 True     True     Double                                   System.Object 
  
 # A continuación convertimos "Double" a tipo de dato "String" y comprobamos de nuevo el tipo de variable

 $texto_convertido = [string]$texto
 $texto_convertido.GetType()
 
 
 # Nos devolverá: IsPublic IsSerial Name                                     BaseType            
 #				 -- -- -                                     --            
 #				 True     True     String                                   System.Object   

 
 ``` 

By [@acruma](https:#github.com/acruma)
