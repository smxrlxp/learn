 # Aprenda conceptos básicos en PYTHON
 
 ## Índice
 
 [Creación e iniciación del documento](https://github.com/acruma/learn/blob/master/spanish/basic/python.md#creaci%C3%B3n-e-iniciaci%C3%B3n-del-documento)
 
 [Comentarios](https://github.com/acruma/learn/blob/master/spanish/basic/python.md#comentarios)
  
 [Variables](https://github.com/acruma/learn/blob/master/spanish/basic/python.md#variables)
 
 [Impresiones en pantalla](https://github.com/acruma/learn/blob/master/spanish/basic/python.md#impresiones-en-pantalla)
 
 [Operaciones aritméticas con números](https://github.com/acruma/learn/blob/master/spanish/basic/python.md#operaciones-aritm%C3%A9ticas-con-n%C3%BAmeros)
 
 [Operaciones con String (cadenas de caracteres)](https://github.com/acruma/learn/blob/master/spanish/basic/python.md#operaciones-con-string-cadenas-de-caracteres)
 
 [Conversiones de Tipos de Datos](https://github.com/acruma/learn/blob/master/spanish/basic/python.md#conversiones-de-tipos-de-datos)
 
 [Documento completo](https://github.com/acruma/learn/blob/master/spanish/basic/python.md#documento-completo)
 
 ---
 ---
  
 ### Creación e iniciación del documento
 
 Para crear un documento en python el nombre de extension debe ser `.py`.
 
 No es necesario crear o especificar ( clases o funciones ) como en otros lenguajes.

---

 ### Comentarios;
 
 Podemos escribir un comentario en una única linea o en múltiples lineas.
 
 ```Python
 #Esto es un comentario

 '''
 Esto es un comentario
 en múltiples líneas 
 '''
 ```
 
---

### Variables

  "Simbolo" que representa un valor que puede cambiar.

  La sintaxis es la siguiente; 
  
```Python
# identificador = valor       (EJ;)
     altura     =  100        #El valor "100" se le asigna a la variable "altura"	
```
Tipos básicos de variables

```Python
edad = 34 			#"Integer" (numeros enteros)
recorrido = 132.23   	#"Float"  (numeros reales)
nombre = "Acruma"    	#"String"  (cadena de caracteres)
comparativas = True 	#"Boolean" (valores "True" o "False")
```

---

### Impresiones en pantalla

Para mostrar variables en pantalla la sintaxis es la que sigue;

```Python
print( VALOR A MOSTRAR )
```
Ejemplos;

```Python
print("Esto es una frase") #Se mostrará en pantalla "Esto es una frase"
print(edad)		 #Se mostrará en pantalla la variable "edad"
```
Para mostrar más de una variable se hace mediante concatenación de variables y/o texto, con una coma ","

```Python
print(edad, " ", nombre)
#Se mostrará en pantalla la variable "edad" seguido de un espacio " " y la variable "nombre"
```
---

### Operaciones aritméticas con números
 
 Como ejemplo, creamos 3 variables.
 
 ```Python
a = 3
b = 5
c = 0 
 
c = a + b		#Suma 						Resultado: 8.
c = a - b		#Resta						Resultado: -2.
c = a * b		#Multiplicación				Resultado: 15.
c = a / b		#Division					Resultado: 0.6.
c = b % a		#Modulo (El resto de la division)		Resultado: 2.
c = a ** 2 #Exponente 						Resultado: 9
c = b // a #Division entera 						Resultado: 1

c = c + 1		#Incremento de valor en 1.			Resultado: 4.
c = c - 1		#Decremento de valor en 1.			Resultado: 2.
 ```
 
 El orden de las operaciones se realizan como en matemáticas
 
```Python
c =  50 - a  *  6 / -0.5
c = (50 - a) *  6 / -0.5
c = (50 - a) * (6 / -0.5)
 ```
 Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)

```Python
print(c)  #Mostrará el ultimo valor que le asignamos >>> "(50 - a) * (6 / -0.5)" >>> 47 * (-12) = -564
```

---

### Operaciones con String (cadenas de caracteres)

Concatenación

```Python
texto1 = "Hola, "
texto2 = "soy Acruma"
texto_concatenado = texto1 + texto2

print(texto_concatenado)
``` 
Resultado: "Hola, soy Acruma".

Repetición

```Python
texto_concatenado = texto1 * 2 
print(texto_concatenado)
```
Resultado: "Hola, Hola, ".

---

### Conversiones de Tipos de Datos
 
 ```Python
 numero = "123.4"
 texto  = 123.4
 ```
 En primer lugar debemos saber que tipo de dato queremos convertir. 
 
 Para ello, mostramos en pantalla que tipo tiene la variable (numero, por ejemplo)
 ```Python
 print(type(numero))	
 ```
 >Nos devolverá "<class 'str'>" - Dato "String"
 
 A continuación convertimos "String" a tipo de dato "Float" y comprobamos de nuevo el tipo de variable
 ```Python
 numero = float(numero)		  	
 print(type(numero))
 ```
  >Nos devolverá "<class 'float'>" - Dato "Float"
 
 Para ello, mostramos en pantalla que tipo tiene la variable (texto, por ejemplo)
 ```Python
 print(type(texto))
 ``` 
 
 >Nos devolverá "<class 'float'>" - Dato "Float"
 
 A continuación convertimos "Float" a tipo de dato "String" y comprobamos de nuevo el tipo de variable

```Python
 texto = Str(texto)
 print(type(texto))
 ```
 >Nos devolverá "<class 'str'>" - Dato "String"
 
 ---
 
 ### Documento completo
 
 A continuación puede copiar todo el codigo y volcarlo en un archivo llamado `python.py`, para poder ejecutar y ver cada una de las impresiones vistas en el tutorial. O incluso para editarlo a voluntad
 
 ```Python
 # Creación e iniciación del documento
 
 # Para crear un documento en python el nombre de extension debe ser `.py`.
 
 # No es necesario crear o especificar ( clases o funciones ) como en otros lenguajes.

 #---------------------------------------------------------------------------------
 
 # Comentarios;
 
 # Podemos escribir un comentario en una única linea o en múltiples lineas.
 
 # Esto es un comentario

'''
 Esto es un comentario
 en múltiples líneas 
'''

 #---------------------------------------------------------------------------------
 
 # Variables

 # "Simbolo" que representa un valor que puede cambiar.

 # La sintaxis es la siguiente; 
  
 # identificador = valor       (EJ;)

altura = 100        #El valor "100" se le asigna a la variable "altura"	

 # Tipos básicos de variables


edad = 34 			#"Integer" (numeros enteros)
recorrido = 132.23   	#"Float"  (numeros reales)
nombre = "Acruma"    	#"String"  (cadena de caracteres)
comparativas = True 	#"Boolean" (valores "True" o "False")

 #---------------------------------------------------------------------------------

 # Impresiones en pantalla

 # Para mostrar variables en pantalla la sintaxis es la que sigue;


 # print( VALOR A MOSTRAR )

 # Ejemplos;

print("Esto es una frase") #Se mostrará en pantalla "Esto es una frase"
print(edad)		 #Se mostrará en pantalla la variable "edad"

 # Para mostrar más de una variable se hace mediante concatenación de variables y/o texto, con una coma ","

print(edad, " ", nombre)
 
 # Se mostrará en pantalla la variable "edad" seguido de un espacio " " y la variable "nombre"

 #---------------------------------------------------------------------------------

 # Operaciones aritméticas con números
 
 # Como ejemplo, creamos 3 variables.
 
a = 3
b = 5
c = 0 
 
c = a + b		#Suma 						Resultado: 8.
c = a - b		#Resta						Resultado: -2.
c = a * b		#Multiplicación				Resultado: 15.
c = a / b		#Division					Resultado: 0.6.
c = a % b		#Modulo (El resto de la division)		Resultado: 2.
 
c = c + 1		#Incremento de valor en 1.			Resultado: 4.
c = c - 1		#Decremento de valor en 1.			Resultado: 2.
 
 # El orden de las operaciones se realizan como en matemáticas
 
c =  50 - a  *  6 / -0.5
c = (50 - a) *  6 / -0.5
c = (50 - a) * (6 / -0.5)

 # Recordemos que el simbolo "=" asigna un valor a una variable. Y un programa lee de arriba a abajo.
 # Por lo tanto. La ultima operación realizada seria, el actual valor de la variable. (EJ)

print(c)  #Mostrará el ultimo valor que le asignamos >>> "(50 - a) * (6 / -0.5)" >>> 47 * (-12) = -564

 #---------------------------------------------------------------------------------

 # Operaciones con String (cadenas de caracteres)

texto1 = "Hola, "
texto2 = "soy Acruma"
texto_concatenado = texto1 + texto2

print(texto_concatenado)
 
 # Concatenación Resultado: "Hola, soy Acruma".

texto_concatenado = texto1 * 2 
print(texto_concatenado)

 # Repetición    Resultado: "Hola, Hola, ".

 #---------------------------------------------------------------------------------

 # Conversiones de Tipos de Datos
 
numero = "123.4"
texto  = 123.4
 
 # En primer lugar debemos saber que tipo de dato queremos convertir. 
 
 # Para ello, mostramos en pantalla que tipo tiene la variable (numero, por ejemplo)
 
print(type(numero))	
 
 # Nos devolverá "<class 'str'>" - Dato "String"
 
 # A continuación convertimos "String" a tipo de dato "Float" y comprobamos de nuevo el tipo de variable

numero = float(numero)		  	
print(type(numero))

 # Nos devolverá "<class 'float'>" - Dato "Float"
 
 # Para ello, mostramos en pantalla que tipo tiene la variable (texto, por ejemplo)
 
print(type(texto))
  
 # Nos devolverá "<class 'float'>" - Dato "Float"
 
 # A continuación convertimos "Float" a tipo de dato "String" y comprobamos de nuevo el tipo de variable

texto = str(texto)
print(type(texto))

 # Nos devolverá "<class 'str'>" - Dato "String"
 
 #---------------------------------------------------------------------------------

``` 
By [@acruma](https://github.com/acruma)
