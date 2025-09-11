# Perspectiva de alto nivel de funcionamiento y de interconexiones



- [Funcionamiento del Computador](#funcionamiento-del-computador)
    - [Ciclo de Instrucciones](#ciclo-de-instrucciones)
    - [Interrupciones](#interrupciones)

- [Memoria Cache]()
- []()
- []()
- []()
- []()
-

El computador esta compuesto por el [CPU](), [Memoria]() y [Unidades de entrada y salida](), estos modulos se interconectas de modo que se puedan llevar a cabo las funciones basicas del computador

Todos los computadores actuales estan basados en los conceptos desarrollados por Von Neumann, los cuales se basan en 3 conceptos:
- Los datos e instrucciones se almacenan en una sola memoria de lectura-escritura.
- Los contenidos de esta memoria se direccionan indicando su posicion, sin considerar el tipo de dato contenido
- La ejecucion se produce siguiendo una secuencia de instruccion tras instruccion (a no ser que la secuencia se modifique explicitamente).


## Funcionamiento del Computador
La funcion basica que realiza un computador es la ejecucion de un programa, constituido por un conjunto de instrucciones almacenadas en memoria. El procesador es el que se encarga de ejecutar las instrucciones especificadas en el programa.<br>
La ejecucion consta de dos etapas: Ciclo de Captacion y Ciclo de Ejecucion.

El procesamiento que requiere una instruccion se llama [ciclo de Instrucciones](#ciclo-de-instrucciones)


## Ciclo de Instrucciones
Al comienzo de cada ciclo de instruccion, la CPU capta una instruccion de memoria, en una CPU se utiliza un registro llamado contador de programa (PC) para seguir la pista de la siguiente instruccion a captar, este se incrementa a no ser que se indique otra cosa.

La instruccion captada se almacena en el registro de Instrucciones (IR), la instruccion en binario, especifica la accion que debe realizar la CPU.
Pueden ser de 4 tipos: 
- Procesador - Memoria 
- Procesador - E/S
- Procesamiento de Datos
- Control

Para un ciclo de instruccion dado, algunos estados pueden no darse y otros repetirse mas de una vez. Estos estados son:
- Calculo de la direccion de la instruccion<br>
(Determina la direccion de la siguiente instruccion a ejecutar)
- Captacion de la instruccion
- Decodificacion de operacion indicada en la instruccion
- Calculo de la direccion del operando (Si la instruccion indica una referencia a un operando)
- Captacion del operando
- Operacion con los datos
- Almacenamiento de operando


## Interrupciones

Todos los computadores cuentan con un mecanismo mediante el cual otros modulos pueden interrumpir el procesamiento normal de la CPU

Clases de interrupciones: 
- <b>Programa</b> <br>
Generadas por algun condicion que se produce como resultado de la ejecucion de una instruccion(ej, div por cero, desbordamiento, etc)
- <b>Temporizacion</b> <br>
Generadas por un temporizador interno, permiten a la CPU a realizar tareas de manera regular.

- <b>E/S</b><br>
Generadas por el controlador de E/S, para indicar la finalizacion sin fallos de una operacion o errores.
- <b>Fallo de Hardware </b> <br>
Generadas por un fallo tal como falta de alimentacion o error en paridad de memoria.

Las interrupciones proporcionan una manera de mejorar la eficiencia del procesador, la mayoria de los dispositivos externos son mas lentos que el procesador, con interrupciones el procesador puede seguir su funcionamiento sin tener que esperar a que terminen sus operaciones.

### Interrupciones y Ciclo de Instruccion
Con el uso de interrupciones el procesador puede dedicarse a ejecutar otras instrucciones mientras una operacion de E/S esta en curso.