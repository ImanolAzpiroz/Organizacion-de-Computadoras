# Memoria
La memoria de un computador tiene una organización jerarquica, separado en niveles.

<table>
<tr>
<td>
</td>

<td align="center"> 
Memoria
</td>
</tr>


<tr>
<td>
Mayor Velocidad <br>
Mayor Costo <br>
Menor Tiempo de Acceso <br>
Menor Capacidad
</td>
<td> 
Registros del procesador
</td>
</tr>

<tr>
<td>
--
</td>
<td> 
Memoria Cache
</td>
</tr>

<tr>
<td>
--
</td>
<td> 
Memoria Cache
</td>
</tr>

<tr>
<td>
--
</td>
<td> 
Memoria Principal(DRAM)
</td>
</tr>

<tr>
<td>
Menor Velocidad <br>
Menor Costo <br>
Mayor Tiempo de Acceso <br>
Mayor Capacidad
</td>
<td> 
Memoria Externa
</td>
</tr>

</table>

## Caracteristicas de los sistemas de memoria.
### Ubicacion
Si es interno o externo al computador.
La memoria interna suele identificarse con la memoria principal, sin embargo el procesador consta de su propia memoria local en forma de registros.

### Capacidad
En memorias internas se usa en terminos de bytes o palabras. <br>
En memorias externas se suele expresar en bytes.

### Acceso
- Secuencial: Se utiliza un mecanismo de lectura/escritura compartida que debe ir trasladandose desde su pos actual a la deseada pasando por cada registro intermedio.
- Directo: El acceso se lleva a cabo mediante un acceso directo a una vecindad dada, seguido de una busqueda secuencial.


## Jerarquia de Memoria
Existe un compromiso de las 3 caracteristicas claves de coste, capacidad, y tiempo de acceso.
- A menor tiempo de acceso, mayor coste por bit.
- A mayor capacidad, menor coste por bit.
- A mayor capacidad, mayor tiempo de acceso.
La respuesta al dilema es no contar con un solo componente de memoria sinó usar una jerarquia de memoria.

![image](https://github.com/ImanolAzpiroz/Organizacion-de-Computadoras/assets/122705871/c2f69e7c-d81c-4e33-8541-c8793594a4cd)
