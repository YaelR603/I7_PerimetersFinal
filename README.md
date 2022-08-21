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

Se debe clonar la biblioteca.
Se crea un archivo main.cc donde se probaran las funciones de la biblioteca.
En main.cc se manda a llamar la bibliote : "include/Perimeters".
Se ejecuta :  g++ main.cc -o testS -lperimeters -std=c++17 .
Finalmente se ejecuta : .\testS.exe .


## Biblioteca dinamica

El usuario debera crear un directorio en el disco local (Windows).

Se debera crear un archivo `main.cc` para poder probar las distintas funciones que contiene la biblioteca. En la cabecera del main.cc se tendra que mandar a llamar la biblioteca de la siguiente manera:

`#include "path/perimetersD"`

Path se sustituye por la direccion relativa de la biblioteca, si es que se almacena en una carpeta diferente que el archivo `main.cc`.

Cuando se crea el archivo `main.cc` se podra mandar a llamar a las funciones, sin embargo, se debe de tener en cuenta que existen distintas funciones y cada una de ellas tiene 2 tipos de datos(enteros, decimales).

Una vez realizado lo anterior el usuario debera de ejecutarlo usando el siguiente comando:

`g++ main.cc -o testD -I .\path -L .\path -lperimetersD`
- `testD` es el nombre del ejecutable, puede ser otro
- La direccion de la bandera `-I` es la de las cabeceras 
- La direccion de la bandera `-L` es la de la biblioteca dinamica y esta debe empezar por `-l`

Si no arroja errores a la hora de la compilacion, se ejecuta de la siguiente manera:

`.\testD.exe`

Un detalle a considerar para que corra el programa, es que la biblioteca dinamica debe estar al menos una carpeta arriba del ejecutable. Solamente asi se podra ejecutar.

A continuacion se mostrara como es la ejecucion del problema con la biblioteca dinamica.
