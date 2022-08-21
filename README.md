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

#### A continuacion se mostrara como es la ejecucion del problema con la biblioteca estatica.

```
ara poder ejecutar la biblioteca estatica se debera usar el siguiente comando:
g++ main.cc -o testS -I .\path -L .\path -lperimetersS
anteriormente cometado, una vez realizado lo anterior el usuario podra ingresar datos enteros y decimales segun sea el caso, con la resticcion que sean mayores que 0.
En nuestro ejemplo se visualiza nuestro menu, en el se podra escoger el tipo de dato que queremos ingresar.
                CALCULO DEL PERIMETRO DEL CUADRADO

    1. Lado entero
    2. Lado decimal
    3. Salir
En nuestro primer caso seleccionamos la opcion 1 y ingresamos nuestro numero entero, siguiendo la restriccion que el numero sea mayor que 0.

Ingrese el tipo de numero que quiere trabajar:  1
 Lado: 5

 Como resultado obtenemos nuestro perimetro del cuadrado
 ----> El perimetro del cuadrado es:    20 

    1. Lado entero
    2. Lado decimal
    3. Salir

En caso contrario si escogemos la opcion 2 nuestra entrada debera ser un numero con decimales.
Ingrese el tipo de numero que quiere trabajar:  2

De igual manera se sigue la resticcion
 Lado: 12.34
 ----> El perimetro del cuadrado es:    49.36 

Otros ejemplos:

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

            CALCULO DEL PERIMETRO DEL CIRCULO
Diametro:       12.4
Perimetro:      38.9557
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

#### A continuacion se mostrara como es la ejecucion del problema con la biblioteca dinamica.

```

```

