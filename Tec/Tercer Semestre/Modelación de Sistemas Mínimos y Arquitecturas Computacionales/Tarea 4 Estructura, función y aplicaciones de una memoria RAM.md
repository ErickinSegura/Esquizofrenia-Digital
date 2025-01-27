---
Nombre: Erick Segura Sánchez.
Matrícula: A01613821.
---
links: [[Modelación de Sistemas Mínimos y Arquitecturas Computacionales]]

### 1) Estructura. 
En los sistemas de almacenamiento principal, la unidad mínima de información se le conoce como bit; al agrupar a diferentes bits con un significado común obtenemos la longitud de palabra de almacenamiento, misma que puede ser de 1, 2, 4, 8,... siempre congruente con una potencia de 2, los cuales se denominan localidades. Contesta las siguientes preguntas en relación a la hoja de datos de la memoria 2114 (un modelo clásico que se comercializó por muchos años):

a) ¿Qué **_longitud de palabra_** tiene?
La memoria 2114 tiene una longitud de palabra de 4 bits.

b) ¿Cuál es el **_tamaño_** de la memoria?
El tamaño de la memoria 2114 es de 4096 bits, que equivalen a 1024 palabras de 4 bits cada una.

c) ¿Cuántas **_localidades_** se pueden acceder?
La memoria 2114 tiene 10 localidades, que equivalen a 1024 palabras de 4 bits cada una.

d) ¿Cuántas **_líneas de dirección_** tiene esta memoria?
La memoria 2114 tiene 10 líneas de dirección.

e) ¿Cuántas **_líneas de datos_** se consideran en esta memoria?
La memoria 2114 tiene 4 líneas de datos.

f) ¿Cuáles señales son consideradas **_líneas de control_** y qué función tienen?
Las señales consideradas líneas de control son:
- **CS:** Chip Select. Se utiliza para seleccionar el chip de memoria que se va a acceder.
- **WE:** Write Enable. Se utiliza para habilitar la escritura en la memoria.
- **OE:** Output Enable. Se utiliza para habilitar la salida de datos de la memoria.

----
### 2) Función. 
Acceso a la memoria. Las memorias son unidades que operan a través de un conjunto de señales eléctricas agrupadas de acuerdo a su función: control, direcciones y datos. Cada sistema de memoria puede accederse a través de la activación de un conjunto particular de señales durante cierto intervalo de tiempo, a lo cual se les conoce como ciclos de lectura y escritura. En relación a las gráficas proporcionadas para la RAM 2114.

a) ¿Cuáles buses están relacionados con la **_operación de lectura_**?
Los buses relacionados con la operación de lectura son:
- **Data:** Se utiliza para transferir los datos leídos de la memoria.
- **Address:** Se utiliza para indicar la localidad de memoria que se desea leer.

b) ¿Qué señales determinan la **_habilitación_** y **_disponibilidad_** del dato en una operación de lectura?
Las señales que determinan la habilitación y disponibilidad del dato en una operación de lectura son:
- **CS:** Debe estar activada para que la memoria esté disponible para la operación.
- **OE:** Debe estar activada para que los datos puedan salir de la memoria.

c) ¿Qué proceso de activación se necesita para realizar una **_operación de escritura_**?
El proceso de activación para realizar una operación de escritura es el siguiente:

1. Activar **CS** para seleccionar el chip de memoria.
2. Activar **WE** para habilitar la escritura.
3. Escribir los datos en las líneas de datos.
4. Desactivar **WE** para finalizar la escritura.

d) ¿Cómo se emplearía una **_máquina de estados_** para realizar las operaciones anteriores?
Una máquina de estados para realizar las operaciones de lectura y escritura de la memoria 2114 podría ser la siguiente:

```
Estado | Acción
------- | --------
Inicial | Esperar activación de **CS**
Activo | Esperar activación de **WE** para escritura o ciclo de lectura
Lectura | Transferir datos de la memoria a las líneas de datos
Escritura | Transferir datos de las líneas de datos a la memoria
Final | Desactivar **CS**
```

----
### 3) Aplicaciones. 
Diseño de bloques de bloques de memoria. En muchas ocasiones es necesario agrupar un conjunto de memorias para satisfacer los requerimientos de almacenamiento. Conteste a las siguientes preguntas en las que las memorias base (los chips de memoria indicados) se deben estructurar como bancos de memoria para cumplir con el almacenamiento requerido.

a) Empleando chips de memoria del tipo 2114, ¿cuántos chips se requeriría y cómo se interconectarían para ofrecer un almacenamiento 4K x 8 bits? Indique todas las señales involucradas (datos, dirección y control) para realizar apropiadamente los ciclos de lectura y escritura.

Para ofrecer un almacenamiento de 4K x 8 bits, se requieren 4 chips de memoria 2114. Los chips se interconectan de la siguiente manera:

- Las líneas de dirección se conectan en paralelo.
- Las líneas de datos se conectan en paralelo.
- Las señales de control se conectan en paralelo.

b) Qué modificación se haría al banco de memoria de 4K localidades si ahora se requiere una longitud de palabra de 32 bits (conocido como _double word_).

Para obtener una longitud de palabra de 32 bits, se requiere un banco de memoria con 8 chips de memoria 2114. Los chips se interconectan de la siguiente manera:

- Las líneas de dirección se conectan en paralelo.
- Las líneas de datos se conectan en serie.
- Las señales de control se conectan en paralelo.

----

### 4) Conclusiones.

Una memoria de modelo reciente tiene las siguientes características de estructura y función:

- **Estructura:**
    - La memoria está organizada en filas y columnas.
    - Cada fila almacena una palabra.
    - Cada columna almacena un bit de la palabra.
- **Función:**
    - La memoria se accede a través de un conjunto de señales eléctricas.
    - Las señales de dirección se utilizan para indicar la fila y la columna de la palabra que se desea acceder.
    - La señal de datos se utiliza para transferir los datos de la memoria.

Las ventajas de realizar un banco de memorias intercalado con respecto a usar un chip del tamaño deseado son:

- **Costo:** Un banco de memorias intercalado es más económico que un chip del tamaño deseado.
- **Disponibilidad:** Un banco de memorias intercalado puede estar disponible en tamaños que no están disponibles en un chip individual.

Las desventajas de realizar un banco de memorias intercalado con respecto a usar un chip del tamaño deseado son:

- **Rendimiento:** Un banco de memorias intercalado puede tener un rendimiento menor que un chip individual.
- **Complexidad:** Un banco de memorias intercalado es más complejo de implementar que un chip individual.
