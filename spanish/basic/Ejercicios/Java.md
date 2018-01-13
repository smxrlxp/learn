# Ejercicios basicos resueltos.  

**1.-** Imprima en pantalla la cadena de caracteres "¡Hola, mundo!" .

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-1-)

**2.-** Inicializa una variable (crea una variable y dale un valor) de tipo número real e imprimela por pantalla.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-2-)

**3.-** Inicializa dos variables (de tipo número real) con identificadores `edad` y `altura`, e imprímerlas junto en el mensaje: Tengo `edad` años y mido `altura` cm.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-3-)

**4.-** Inicializa cuatro variables, una de cada tipo de variable básico, e imprímelas todas en un mismo mensaje indicando cual es cual.
> Opcional - Cada una debe aparecer en una línea distinta (consejo usa \n).

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-4-)

**5.-** Inicializa 2 variables de tipo número entero y súmalos en una tercera variable. Imprime en pantalla esta última.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-5-)

**6.-** Inicializa una variable `radio` y calcula la circunferencia guardando el resultado en la variable `circunferencia`. 
**Fórmula: 2 · п · radio**. A posteriori imprime en pantalla `circunferencia`

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-6-)

**7.-** Inicializa una variable `radio` y calcula el área de un círculo guardando el resultado en la variable `area`. **Fórmula: п · radio · radio**. A posteriori imprime en pantalla `area`

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-7-)

**8.-** Convierte una variable con identificador `latitud` de tipo **cadena de caracteres** y con valor -234.62 a tipo número real. Réstale a la variable el valor 21.34 e imprime finalmente dicha variable.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-8-)

**9.-** Inicializa una variable `celsius`, calcula su equivalente a grados Fahrenheit guardando el resultado en la variable `fahrenheit` e ímprimelo por pantalla. **Fórmula: fahrenheit = (celsius * 1.8) + 32**.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-9-)

**10.-** Inicializa una variable `fahrenheit`, calcula su equivalente a grados Celsius guardando el resultado en la variable `celsius` e ímprimelo por pantalla. **Fórmula: celsius = (fahrenheit - 32) / 1.8**.

Ejercicio resuelto  ---------------------  [SPOILER](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicio-10-)


> A continuación verás los ejercicios corregidos, son un ejemplo de como hacerlos, pues hay más de una forma.

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 1
---
---
---
# Ejercicio 1.-

Imprima en pantalla la cadena de caracteres "¡Hola, mundo!" .

```Java
public class Ejercicio1JAVA{
  public static void main(String[] args){
    System.out.println("¡Hola, mundo!");
  }
}
```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 2
---
---
---
# Ejercicio 2.-

Inicializa una variable (crea una variable y dale un valor) de tipo número real e imprimela por pantalla.

```Java
public class Ejercicio2JAVA{
  public static void main(String[] args){
    double numero_real = -123.3;
    System.out.println(numero_real);
  }
}
```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 3
---
---
---
# Ejercicio 3.-

Inicializa dos variables (de tipo número real) con identificadores `edad` y `altura`, e imprímerlas junto en el mensaje: Tengo `edad` años y mido `altura` cm.

```Java
public class Ejercicio3JAVA{
  public static void main(String[] args){
    int edad = 26;
    int altura = 183;
    System.out.println("Tengo " + edad + " años y mido " + altura + " cm.");
  }
}
```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 4
---
---
---
# Ejercicio 4.-

Inicializa cuatro variables, una de cada tipo de variable básico, e imprímelas todas en un mismo mensaje indicando cual es cual.
> Opcional - Cada una debe aparecer en una línea distinta (consejo usa \n).

```Java
public class Ejercicio4JAVA{
  public static void main(String[] args){
    int entero=1;
    double real=-10.10;
    String palabra="Java es facil";
    boolean comparativa=true;
    System.out.println("Este es un número entero: " + entero + ".\nEste es un numero real: " + real + ".\nEsto es una cadena de caracteres: " + palabra + ".\nEsto es un boleano: " + comparativa + ".");
  }
}
```


Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 5
---
---
---
# Ejercicio 5.-

Inicializa 2 variables de tipo número entero y súmalos en una tercera variable. Imprime en pantalla esta última.

```Java
public class Ejercicio5JAVA{
  public static void main(String[] args){
    int a = 1;
    int b = 10;
    int c = a + b;
    System.out.println(c);	
  }	
}
```


Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 6
---
---
---
# Ejercicio 6.-

Inicializa una variable `radio` y calcula la circunferencia guardando el resultado en la variable `circunferencia`. 
**Fórmula: 2 · п · radio**. A posteriori imprime en pantalla `circunferencia`

```Java
public class Ejercicio6JAVA{
  public static void main(String[] args){
    int radio = 11;
    double circunferencia = 2 * 3.14 * radio;
    System.out.println(circunferencia);
  }
}
```


Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 7
---
---
---
# Ejercicio 7.-

Inicializa una variable `radio` y calcula el área de un círculo guardando el resultado en la variable `area`. **Fórmula: п · radio · radio**. A posteriori imprime en pantalla `area`

```Java
public class Ejercicio7JAVA{
  public static void main(String[] args){
    int radio = 10;
    double area = 3.14 * radio * radio;
    System.out.println(area);
  }
}
```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 8
---
---
---
# Ejercicio 8.-

Convierte una variable con identificador `latitud` de tipo **cadena de caracteres** y con valor -234.62 a tipo número real. Réstale a la variable el valor 21.34 e imprime finalmente dicha variable.

```Java
public class Ejercicio8JAVA{
  public static void main(String[] args){
    String latitud="-234.62";
    double latitud2= Double.parseDouble(latitud) -21.34;
    System.out.println(latitud2);
  }
}
```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 9
---
---
---
# Ejercicio 9.-

Inicializa una variable `celsius`, calcula su equivalente a grados Fahrenheit guardando el resultado en la variable `fahrenheit` e ímprimelo por pantalla. **Fórmula: fahrenheit = (celsius * 1.8) + 32**.

```Java

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)

---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ATENCION SI SIGUES VERÁS LOS EJERCICIOS RESUELTOS
---
---
---
---
---
---
#### ULTIMO AVISO - Ejercicio 10
---
---
---
# Ejercicio 10.-

Inicializa una variable `fahrenheit`, calcula su equivalente a grados Celsius guardando el resultado en la variable `celsius` e ímprimelo por pantalla. **Fórmula: celsius = (fahrenheit - 32) / 1.8**.

```Java

```

Volver a la descripcion de los [Ejercicios](https://github.com/acruma/learn/blob/master/spanish/basic/Ejercicios/Java.md#ejercicios-basicos-resueltos)
