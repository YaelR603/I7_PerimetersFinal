# I7_PerimetersFinal

Este repositorio permite calcular los perimetros de las figuras: 
- Triangulo 
- Rectangulo  
- Cuadrado 
- Pentagono 
- Hexagono 
- Circulo 

Para medidas de numeros naturales y de punto flotante.


## Estructura de directorios

La estructura de la carpetas y archivos que se realizo para llevar acabo la creacion de las bibliotecas estatica y dinamica, es la siguiente:

```
C:.
│   main.cc
│
├───.vscode
│       settings.json
│
├───app
│       test.exe
│       testD.exe
│
├───include
│       Perimeters
│
├───lib
│   ├───dinamic
│   │       perimetersD.dll
│   │
│   └───static
│           perimetersS.lib
│
├───obj
│       circulo.o
│       cuadrado.o
│       hexagono.o
│       pentagono.o
│       rectangulo.o
│       triangulo.o
│
└───src
        circulo.cc
        Cuadrado.cc
        Hexagono.cc
        Pentagono.cc
        rectangulo.cc
        triangulo.cpp
```



## Biblioteca estática

El usuario debera crear un directorio en su dispositivo.

Se debera crear un archivo `main.cc` para poder probar las distintas funciones que contiene la biblioteca. En la cabecera del `main.cc` se tendra que mandar a llamar la biblioteca estatica de la siguiente manera:

`#include "path/perimetersS"`

Path se sustituye por la direccion relativa de la biblioteca estatica, si es que se almacena en una carpeta diferente que el archivo `main.cc`.

Cuando se crea el archivo `main.cc` se podra mandar a llamar a las funciones, sin embargo, se debe de tener en cuenta que existen distintas funciones y cada una de ellas tiene 2 tipos de datos (enteros, decimales). Checar cuales son, los parametros de cada una y el valor que regresa, en el archivo de cabeceras.

Una vez realizado lo anterior el usuario debera de ejecutarlo usando el siguiente comando:

`g++ main.cc -o testS -I .\path -L .\path -lperimetersS`
- `testS` es el nombre del ejecutable, puede ser otro
- La direccion de la bandera `-I` es la de las cabeceras 
- La direccion de la bandera `-L` es la de la biblioteca estatica y esta debe empezar por `-l`

Si no arroja errores a la hora de la compilacion, se ejecuta de la siguiente manera:

`.\testS.exe`

#### A continuacion se mostrara como el flujo de la ejecucion del `main.cc` con la biblioteca estatica.


Al momento de ejecutarlo se desplegara un menu en donde se podra escoger el tipo de figura geometrica que se desea calcular el perimentro.
```
                         C A L C U L O   D E   P E R I M E T R O S 
 --- NOTA: Ingrese numeros MAYORES de cero. --- 

        1. Cuadrado
        2. Rectangulo
        3. Triangulo
        4. Circulo
        5. Pentagono
        6. Hexagono
        7. Salir
Ingrese la opcion de la figura que quiere calcular: 1
```
Una vez seleccionada la figura podremos seleccionar el tipo de numero que ingresaremos entero o decimal. 

```
                CALCULO DEL PERIMETRO DEL CUADRADO

    1. Lado entero
    2. Lado decimal
    3. Salir
Ingrese el tipo de numero que quiere trabajar:  1
```
En nuestro primer caso seleccionamos la opcion 1 e ingresamos nuestro numero entero, siguiendo la restriccion del principio, que decia que la medida sea mayor que 0

```
 Lado: 5
 ----> El perimetro del cuadrado es:    20 
 
```
 Como resultado obtenemos nuestro perimetro del cuadrado
 
```
    1. Lado entero
    2. Lado decimal
    3. Salir
Ingrese el tipo de numero que quiere trabajar:  2
```
En caso contrario si escogemos la opcion 2 nuestra entrada debera ser un numero con decimales. De igual manera se sigue la resticcion

```
 Lado: 12.34
 ----> El perimetro del cuadrado es:    49.36 

```
Otros ejemplos en el flujo de la ejecucion:

```

                CALCULO DEL PERIMETRO DEL HEXAGONO

    1. Lado entero
    2. Lado decimal
    3. Salir
Ingrese el tipo de numero que quiere trabajar:  1
 Lado: 8
 ----> El perimetro del hexagono es:    48 

    1. Lado entero
    2. Lado decimal
    3. Salir
Ingrese el tipo de numero que quiere trabajar:  2
 Lado: 4.67
 ----> El perimetro del hexagono es:    28.02 

    1. Lado entero
    2. Lado decimal
    3. Salir
Ingrese el tipo de numero que quiere trabajar:  3
 

        1. Cuadrado
        2. Rectangulo
        3. Triangulo
        4. Circulo
        5. Pentagono
        6. Hexagono
        7. Salir
Ingrese la opcion de la figura que quiere calcular:  4


                CALCULO DEL PERIMETRO DEL CIRCULO

 Diametro: 12.4
 ----> El perimetro del circulo es:     38.9557 
 

        1. Cuadrado
        2. Rectangulo
        3. Triangulo
        4. Circulo
        5. Pentagono
        6. Hexagono
        7. Salir
Ingrese la opcion de la figura que quiere calcular:  7

  -----> BYE :) <-----
 
```





## Biblioteca dinamica

El usuario debera crear un directorio en el disco local (Windows).

Se debera crear un archivo `main.cc` para poder probar las distintas funciones que contiene la biblioteca. En la cabecera del main.cc se tendra que mandar a llamar la biblioteca de la siguiente manera:

`#include "path/perimetersD"`

Cuando se crea el archivo `main.cc` se podra mandar a llamar a las funciones, sin embargo, se debe de tener en cuenta que existen distintas funciones y cada una de ellas tiene 2 tipos de datos(enteros, decimales).

Una vez realizado lo anterior el usuario debera de ejecutarlo usando el siguiente comando:

`g++ main.cc -o testD -I .\path -L .\path -lperimetersD`
- `testD` es el nombre del ejecutable, puede ser otro
- La direccion de la bandera `-I` es la de las cabeceras 
- La direccion de la bandera `-L` es la de la biblioteca dinamica y esta debe empezar por `-l`

Si no arroja errores a la hora de la compilacion, se ejecuta de la siguiente manera:

`.\testD.exe`

> Un detalle a considerar para que corra el programa, es que la biblioteca dinamica debe estar al menos una carpeta arriba del ejecutable. Solamente asi se podra ejecutar.

#### A continuacion se mostrara como el flujo de la ejecucion del `main.cc` con la biblioteca dinamica.
Cuando se ejecuta se verá un menú de opciones, donde se podra seleccionar el poligono que que se desea calcular el perimetro.
```
                C A L C U L O   D E   P E R I M E T R O S 
 --- NOTA: Ingrese numeros MAYORES de cero. ---

        1. Cuadrado
        2. Rectangulo
        3. Triangulo
        4. Circulo
        5. Pentagono
        6. Hexagono
        7. Salir
```
Una vez que se selecciono número de poligono, podrás elegir el tipo de dato que desees.

         CALCULO DEL PERIMETRO DEL CUADRADO

    1. Lado entero
    2. Lado decimal
    3. Salir
    Ingrese el tipo de numero que quiere trabajar:  1
    
Posteriormente se pedira el valor de se lado y se hara el cálculo.

       Lado: 13
    
    ----> El perimetro del cuadrado es:    52 
    
Después seleccionamos en lado decimal para hacer el cálculo

    1. Lado entero
    2. Lado decimal
    3. Salir
    Ingrese el tipo de numero que quiere trabajar:  2
    Lado: 7.9
    ----> El perimetro del cuadrado es:    31.6 
  
Ejemplo del rectángulo

       CALCULO DEL PERIMETRO DEL RECTANGULO

    1. Altura y base enteros
    2. Altura y base decimales
    3. Salir
    Ingrese el tipo de numero que quiere trabajar:  1
    Altura: 4
    Base: 6
    ----> El perimetro del rectangulo es:  20 

    1. Altura y base enteros
    2. Altura y base decimales
    3. Salir
    Ingrese el tipo de numero que quiere trabajar:  2
    Altura: 6.7
    Base: 8.2
    ----> El perimetro del rectangulo es:  29.8 
    
Ejemplo del círculo

     C A L C U L O   D E   P E R I M E T R O S 
        --- NOTA: Ingrese numeros MAYORES de cero. ---

        1. Cuadrado
        2. Rectangulo
        3. Triangulo
        4. Circulo
        5. Pentagono
        6. Hexagono
        7. Salir
      Ingrese la opcion de la figura que quiere calcular:  4


                CALCULO DEL PERIMETRO DEL CIRCULO

      Diametro: 5
      ----> El perimetro del circulo es:    15.708
       
Ejemplo del pentágono
    
                CALCULO DEL PERIMETRO DEL PENTAGONO

    1. Lado entero
    2. Lado decimal
    3. Salir
     Ingrese el tipo de numero que quiere trabajar:  1
    Lado: 7
     ----> El perimetro del pentagono es:   35 

    1. Lado entero
    2. Lado decimal
    3. Salir
     Ingrese el tipo de numero que quiere trabajar:  2
    Lado: 5.6
     ----> El perimetro del pentagono es:   28 

ejemplo de Hexágono

     CALCULO DEL PERIMETRO DEL HEXAGONO

    1. Lado entero
    2. Lado decimal
    3. Salir
    Ingrese el tipo de numero que quiere trabajar:  1
    Lado: 3
     ----> El perimetro del hexagono es:    18 

    1. Lado entero
    2. Lado decimal
    3. Salir
    Ingrese el tipo de numero que quiere trabajar:  2
    Lado: 7.4
     ----> El perimetro del hexagono es:    44.4 
    
