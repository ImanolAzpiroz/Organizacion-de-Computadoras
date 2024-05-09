

Indice
=========
- [Arquitectura Von Neumann](#arquitectura-von-neumann)
- [Ciclo de instrucciones](#ciclo-de-instrucción)
- [Estados](#estados)
- [Interrupciones](#interrupciones)
- [Buses](#interconexiones-con-buses)


## Arquitectura Von Neumann
- Los datos y las instrucciones se almacenan en una sola memoria de lectura-escritura.
- Los contenidos de esta memoria se direccionan indicando su posicion, sin considerar el tipo de dato contenido en la misma.
- La ejecución se produce siguiendo una secuencia de instrucción tras instrucción.

![image](https://github.com/ImanolAzpiroz/Organizacion-de-Computadoras/assets/122705871/88e358b5-a978-4044-8672-c7b8e6337a7d)


### Perspectiva de alto nivel y de las interconexiones del computador
![image](https://github.com/ImanolAzpiroz/Organizacion-de-Computadoras/assets/122705871/6a2c2d28-af5b-4d9c-9427-0dac69e81406)


La funcion basica que realiza un computador es la ejecucion de un programa, constituido por un conjunto de instrucciones almacenadas en memoria. El procesador se encarga de ejecutar las instrucciones especificas del programa.

Los aspectos de la ejecucion de un programa constan de 2 simples pasos:
- Captacion de la instruccion. (Ciclo de captación)
- Ejecucion de la instruccion. (Ciclo de ejecución)


## Ciclo de instrucción

Registros del cpu que se usan para el manejo de instrucciones
- Program Counter (PC) - Direccion de la siguiente instruccion a ejecutar.
- Instruction Register (IR) - Almacena la instruccion a ejecutar.


La cpu interpreta la instrucción y lleva a cabo la acción requerida. En general puede ser de 4 tipos: 
- Procesador - Memoria: Transferencia de datos en memoria a cpu u vicebersa
- Procesador - E/S: Transferencia de datos entre cpu y modulo de e/s
- Procesamiento de datos: Operacion aritmética o lógica con los datos
- Control - Instruccion de control, ejemplo, modificar el PC. 

Tanto las instrucciones como los datos son de 16 bits
- Registro Acumulador(AC) - Se usa para guardar datos temporales necesarios para la ejecucion de instrucciones.

![image](https://github.com/ImanolAzpiroz/Organizacion-de-Computadoras/assets/122705871/fbd8c81c-254e-44cb-aa73-cad35585cfdc)

### Estados
Los estados de un ciclo de instruccion pueden ser: 
- Calculo de la direccion de la instrucción: Determina la direccion de la siguiente instruccion a ejecutar. 
- Captación de la instrucción: Se lee la instrucción desde su pos en memoria.
- Decodificación: Analiza la instrucción para determinar el tipo de operación a realizar, y el o los operandos necesarios.
- Calculo dirección del operando (Si implica el uso de uno)
- Captación de operando. Desde memoria o E/S
- Operación con los datos.
- Almacenamiento del resultado.

### Interrupciones
Todas las computadoras disponen de un mecanismo con el cual otros modulos (memoria, e/s) pueden interrumpir el procesamiento de la cpu.

Proporcionan una forma de mejorar la eficiencia del procesador, la mayoria de los dispositivos externos son mucho mas lentos que el procesador, estas le permiten seguir funcionando sin desperdiciar tiempo en la espera a los dispositivos externos.
- Programa: Generado por alguna condición que se produce como resultado de la ejecución de una instrucción.
- Temporizacion: Generados por un temporizador interno de la cpu, permite realizar ciertas funciones demanera regular.
- E/S: Generadas por un controlador de E/S, para indicar finalización sin problemas o condiciones de error.
- Fallo de Hardware: Fallo en hardware como falta de potencia de alimentación.

Con las interrupciones el procesador puede dedicarse a ejecutar otras instrucciones mientras una operacion de e/s está en curso.

![image](https://github.com/ImanolAzpiroz/Organizacion-de-Computadoras/assets/122705871/f2824786-87fd-4323-a685-53d41c185901)


![image](https://github.com/ImanolAzpiroz/Organizacion-de-Computadoras/assets/122705871/06abb960-3873-4d18-8e5f-7756770ca9f0)



## Estructuras de interconexión
Conjunto de lineas que conectan los diversos modulos(Cpu, Memoria, e/s). 
Deben dar cobertura a los siguientes tipos de transferencias:
- Memoria a Cpu.
- Cpu a Memoria.
- e/s a Cpu.
- Cpu a e/s.
- Memoria a e/s.
- e/s a Memoria.

## Interconexiones con buses 
Camino de comunicación entre dos o mas dispositivos. <br>
Medio de transmisión compartido.<br>
Constituido por varios caminos de comuncación o lineas. Cada linea es capaz de transmitir señales binarias representadas por 1 y 0. <br>
Los computadores poseen diferentes tipos de buses que proporcionan comunicación entre sus componentes a distintos niveles dentro de la jerarquia del sistema.
El bus que conecta los componentes principales del computador(procesador, memoria y e/s) se denomina **bus de sistema**.

### Estructura del bus
Constituido usualmente por entre 50 a 100 lineas, cada una con su función particular.
Las lineas se pueden clasificar en tres grupos funcionales.
- Lineas de Datos: Transmiten datos entre los modulos del sistema. Mientras mas ancho, mayor es el numero de bits que se transmiten a la vez.
- Lineas de Direcciones: Designan la fuente o destino del dato situado en el bus de datos. El ancho de este bus determina la maxima capacidad de memoria posible del sistema.
- Lineas de Control: Controlan el acceso y el uso de las lineas de datos y direcciones, Transmiten tanto ordenes como información de temporización entre los modulos del sistema. Las señales de ordenes especifican las operaciones a realizar.

