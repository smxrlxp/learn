 # Aprenda conceptos básicos en BASH
 
 ## Índice
 
 [Creación e iniciación del documento](https://github.com/acruma/learn/blob/master/spanish/basic/bash.md#creaci%C3%B3n-e-iniciaci%C3%B3n-del-documento)
 
 [Comentarios](https://github.com/acruma/learn/blob/master/spanish/basic/bash.md#comentarios)
  
 [Variables](https://github.com/acruma/learn/blob/master/spanish/basic/bash.md#variables)
 
 [Impresiones en pantalla](https://github.com/acruma/learn/blob/master/spanish/basic/bash.md#impresiones-en-pantalla)
 
 [Operaciones aritméticas con números](https://github.com/acruma/learn/blob/master/spanish/basic/bash.md#operaciones-aritm%C3%A9ticas-con-n%C3%BAmeros)
 
 [Operaciones con String (cadenas de caracteres)](https://github.com/acruma/learn/blob/master/spanish/basic/bash.md#operaciones-con-string-cadenas-de-caracteres)
 
 [Conversiones de Tipos de Datos](https://github.com/acruma/learn/blob/master/spanish/basic/bash.md#conversiones-de-tipos-de-datos)
 
 [Documento completo](https://github.com/acruma/learn/blob/master/spanish/basic/bash.md#documento-completo)
 
 ---
 ---
  
 ### Creación e iniciación del documento
 
 Para crear un documento en python el nombre de extension debe ser `.sh`.
 
 Se recomienda encarecidamente poner en la primera linea `#!/bin/bash` (para usar bash como shell predeterminada).
 
 ```bash
 
 #!/bin/bash
 
 ```
>NOTA IMPORTANTE: Bash es case sensitive es decir, distingue mayúsculas y minúsculas. Y sensible a espacios, como en la terminal, ya que bash no es mas que lenguaje terminal.
 
---

 ### Comentarios
 
 Podemos escribir un comentario en una única linea
 
 ```bash
 
 #Esto es un comentario
 
 
 ```
 
---

### Variables

  "Simbolo" que representa un valor que puede cambiar.

  La sintaxis es la siguiente 
  
 ```bash

 # identificador=valor     (IMPORTANTE SIN ESPACIOS)-(EJ)
    altura=100			 #El valor "100" se le asigna a la variable "altura"	

 ```

Tipos básicos de variables

 ```bash

edad=34		#"Integer" (numeros enteros)
recorrido=132.23  	#"Float"  (numeros reales)
nombre="Acruma"    	#"String"  (cadena de caracteres)
comparativas=true 	#"Boolean" (valores "True" o "False")

 ```
>NOTA IMPORTANTE: En realidad todas las variables en bash son string. Es decir, se guardan como cadena de caracteres. EJ: edad=34 no es un Integer, es un string "34".

Aunque, una variable no se cree identificandola con un simbolo "$", para llamarlas SÍ hay que anteponerlo.

---

### Impresiones en pantalla

Para mostrar variables en pantalla la sintaxis es la que sigue

 ```bash

echo  VALOR_A_MOSTRAR

 ```

Ejemplos

 ```bash

echo "Esto es una frase"  #Se mostrará en pantalla "Esto es una frase"
echo $edad		  #Se mostrará en pantalla la variable "edad"

 ```

Para mostrar más de una variable se hace mediante concatenación de variables y/o texto.

 ```bash

echo "$edad $nombre"
#Se mostrará en pantalla la variable "edad" seguido de un espacio y la variable "nombre"

 ```

---

### Operaciones aritméticas con números

 Para hacer operaciones en bash, debemos utilizar dos herramientas. Una de ellas es "let" si TODOS los numeros y resultados son con numeros enteros.
 
 La otra seria hacer calculos con BC, para cualquier otro tipo de calculo donde se necesite calcular numeros reales y los resultados sean del mismo tipo.
 
 >Esto se debe, a que como recordamos en BASH, las variables se guardan en cadenas de caracteres.
 
 Como ejemplo, creamos 3 variables.
 
 ```bash

a=3
b=5
c=0
 
#Siempre que sean numeros enteros con estas 4 operaciones el resultado será entero.
 
let c=a+b		#Suma 						Resultado: 8.
let c=a-b		#Resta						Resultado: -2.
let c=a*b		#Multiplicación				 Resultado: 15.
let c=a%b		#Modulo (El resto de la division)		Resultado: 2.

let c=c+1		#Incremento de valor en 1.			Resultado: 4.
let c=c-1		#Decremento de valor en 1.			Resultado: 2.

#Y ahora... operaciones con BC

#La sintaxis basica seria -> (bc -l <<< "operaciones a realizar")

c=$(bc -l <<< "$a / $b")		#Division		Resultado: 0.6.

 ```
 
 El orden de las operaciones se realizan como en matemáticas. Adicionalmente para crear complejas ecuaciones usamos BC
 
 ```bash

c=$(bc -l <<< "50 - $a  *  6 / -0.5")
c=$(bc -l <<< "(50 - $a) *  6 / -0.5")
c=$(bc -l <<< "(50 - $a) * (6 / -0.5)")

 ```

>NOTA IMPORTANTE: Recuerda usar BC para ecuaciones.

 Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)

 ```bash

echo $c #Mostrará el ultimo valor que le asignamos >>> "(50 - a) * (6 / -0.5)" >>> 47 * (-12) = -564

 ```
 
---

### Operaciones con String (cadenas de caracteres)

Concatenación

 ```bash

texto1="Hola, "
texto2="soy Acruma"
texto_concatenado=$texto1$texto2

echo $texto_concatenado

 ``` 

Resultado: "Hola, soy Acruma".

Repetición

 ```bash

texto_concatenado=$(printf "%.s$texto1" {1..2})
echo $texto_concatenado
 
 ```
Resultado: "Hola, Hola, ".

---

### Conversiones de Tipos de Datos
 
Como hemos indicado mas arriba, las variables en `BASH` son cadena de caracteres por lo que no soporta conversion de datos.
 
### Documento completo
 
 A continuación puede copiar todo el codigo y volcarlo en un archivo llamado `bash.sh`, para poder ejecutar y ver cada una de las impresiones vistas en el tutorial. O incluso para editarlo a voluntad
 
 ```bash

 # Creación e iniciación del documento
 
 # Para crear un documento en python el nombre de extension debe ser `.sh`.
 
 # Se recomienda encarecidamente poner en la primera linea `#!/bin/bash` (para usar bash como shell predeterminada).
 
 #!/bin/bash
 
 
 # NOTA IMPORTANTE: Bash es case sensitive es decir, distingue mayúsculas y minúsculas. Y sensible a espacios, como en la terminal, ya que bash no es mas que lenguaje terminal.
 
#-------------------------------------------------

 # Comentarios
 
 # Podemos escribir un comentario en una única linea
  
 #Esto es un comentario
 
#------------------------------------------------- 
 
 # Variables

 # "Simbolo" que representa un valor que puede cambiar.

 # La sintaxis es la siguiente 
  
 # identificador=valor     (IMPORTANTE SIN ESPACIOS)-(EJ)
    altura=100			 #El valor "100" se le asigna a la variable "altura"	

 # Tipos básicos de variables

edad=34		#"Integer" (numeros enteros)
recorrido=132.23  	#"Float"  (numeros reales)
nombre="Acruma"    	#"String"  (cadena de caracteres)
comparativas=true 	#"Boolean" (valores "True" o "False")

 # NOTA IMPORTANTE: En realidad todas las variables en bash son string. Es decir, se guardan como cadena de caracteres. EJ: edad=34 no es un Integer, es un string "34".

 # Aunque, una variable no se cree identificandola con un simbolo "$", para llamarlas SÍ hay que anteponerlo.

#-------------------------------------------------

 # Impresiones en pantalla

 # Para mostrar variables en pantalla la sintaxis es la que sigue

 # echo  VALOR_A_MOSTRAR

 # Ejemplos

echo "Esto es una frase"  #Se mostrará en pantalla "Esto es una frase"
echo $edad		  #Se mostrará en pantalla la variable "edad"

 # Para mostrar más de una variable se hace mediante concatenación de variables y/o texto.

echo "$edad $nombre"
 # Se mostrará en pantalla la variable "edad" seguido de un espacio y la variable "nombre"

#-------------------------------------------------

 # Operaciones aritméticas con números

 # Para hacer operaciones en bash, debemos utilizar dos herramientas. Una de ellas es "let" si TODOS los numeros y resultados son con numeros enteros.
 
 # La otra seria hacer calculos con BC, para cualquier otro tipo de calculo donde se necesite calcular numeros reales y los resultados sean del mismo tipo.
 
 # Esto se debe, a que como recordamos en BASH, las variables se guardan en cadenas de caracteres.
 
 # Como ejemplo, creamos 3 variables.
 
a=3
b=5
c=0
 
 # Siempre que sean numeros enteros con estas 4 operaciones el resultado será entero.
 
let c=a+b		#Suma 						Resultado: 8.
let c=a-b		#Resta						Resultado: -2.
let c=a*b		#Multiplicación				Resultado: 15.
let c=a%b		#Modulo (El resto de la division)		Resultado: 2.

let c=c+1		#Incremento de valor en 1.			Resultado: 4.
let c=c-1		#Decremento de valor en 1.			Resultado: 2.

 # Y ahora... operaciones con BC

 # La sintaxis basica seria -> (bc -l <<< "operaciones a realizar")

c=$(bc -l <<< "$a / $b")		#Division					Resultado: 0.6.

 # El orden de las operaciones se realizan como en matemáticas. Adicionalmente para crear complejas ecuaciones usamos BC
 
c=$(bc -l <<< "50 - $a  *  6 / -0.5")
c=$(bc -l <<< "(50 - $a) *  6 / -0.5")
c=$(bc -l <<< "(50 - $a) * (6 / -0.5)")

 # NOTA IMPORTANTE: Recuerda usar BC para ecuaciones.

 # Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 
 # Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)

echo $c #Mostrará el ultimo valor que le asignamos >>> "(50 - a) * (6 / -0.5)" >>> 47 * (-12) = -564

#-------------------------------------------------

 # Operaciones con String (cadenas de caracteres)

 # Concatenación

texto1="Hola, "
texto2="soy Acruma"
texto_concatenado=$texto1$texto2

echo $texto_concatenado

 # Resultado: "Hola, soy Acruma".

 # Repetición

texto_concatenado=$(printf "%.s$texto1" {1..2})
echo $texto_concatenado
  
 # Resultado: "Hola, Hola, ".

#-------------------------------------------------

 # Conversiones de Tipos de Datos

 # Como hemos indicado mas arriba, las variables en `BASH` son cadena de caracteres por lo que no soporta conversion de datos.
 

 ``` 

By [@acruma](https:#github.com/acruma)
