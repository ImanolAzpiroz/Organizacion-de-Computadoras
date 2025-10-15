


## Circuitos Secuenciales
Conjuntos de puertas logicas interconectadas entre si, en el cual, la salida en cualquier instante de tiempo t depende de las entradas en ese instante y del valor de las entradas en t-1
se pueden clasificar como:
- Asincronicos
- Sincronicos (Cambios asociados a un timer)

### Flip Flops
Circuito secuencial con la capacidad de permanecer en uno de dos estados posibles (1 o 0) durante un tiempo indefinido en ausencia de entrada utilizando el principio de retroalimentacion

- Biestable RS
Consiste en un circuito digital de dos entradas, Reset(Cuando tiene valor 1 pone en 0 la salida) y Set(Cuando tiene el valor 1 pone en 1 la salida), cuando ambos valores son 0, el biestable Rs no sabe bien como acutar y la salida puede cambiar o quedarse inalterada de forma aleatoria.
Tiene su version sincronica que posee una entrada mas de reloj, funciona igual solo que sus cambios se producen durante los pulsos de reloj.

- Biestable JK
Desarrollado para evitar el problema de indeterminacion que poseen los biestables RS, la entrada J funciona como Set y la entrada K como Reset, cuando ambos valores valen 0 no ocurre nada y cuando ambos valen 1 la salida se invierte.

- Biestable D
Circuito digital tambien denominado biestable de datos, sirve para almacenar 1 bit de datos. Posee una sola entrada D(Data) y la salida Q, obtiene el valor de la entrada cuando la senial del reloj se encuentra activada.

<img width="916" height="348" alt="Image" src="https://github.com/user-attachments/assets/70ee556a-8d1f-493d-8e6b-74aecb0eed91" />