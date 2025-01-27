---
Nombre: Erick Segura Sánchez.
Matrícula: A01613821.
---
links: [[Programación de Estructuras de Datos y Algoritmos Fundamentales]]
Fecha: Lunes 7/Lunes/2023

Si se tuvieran 2 programas que hacen lo mismo, ¿cómo se  
podrían comparar?
#### Eficiencia
- Usos de espacio de memoria.
- **Tiempo de ejecución**.

Un algoritmo es una secuencia de pasos que tiene una entrada y devuelve una salida. Que pasa si una segunda vez que se ejecuta el programa la entrada es el doble de grande, ¿debería tardar el doble de tiempo? Respuesta, NO, es depende del algoritmo el tiempo de ejecución escala dependiendo de la entrada.

Para poder resolver un problema se puede realizar de maneras muy distintas, para poder clasificar las diferencias en las que crecen los algoritmos dependiendo de la entrada se utiliza la notación asintótica.

### Notación Big O (Asintótica)
Es una forma de simplificar las funciones que describen la tasa de crecimiento de un algoritmo. Al desarrollar lo que más nos interesa es como sería el comportamiento de nuestro algoritmo en el peor de los casos, ya que es el más util por que nos da más información de como manejar ese límite.


#### ¿Cómo se puede analizar código para determinar su complejidad?

Cualquier línea de código se considera O(1) cuando no sea un ciclo, que tenga recursión o que no sea una llamada a una función que a su vez no sea de tiempo constante. 
###### Ejemplo
```cpp
int a = 1+2;            //0(1)
if (a < 4) {            //0(1)
	cout<<"Hola";       //0(1)
}          
```

##### Ciclos

Para el caso de los ciclos, se considera O(n) cuando la variable del ciclo va incrementando o decrementando por un número constante, siempre y cuando el ciclo vaya iterando en base a la entrada.
###### Ejemplo
```cpp
// Donde n es la entrada
for (int i = 1; i <= n; i+=c){ //O(n)
// Cualquier sentencia O(1)
}

for (int i = 1; i <= n; i-=c){ //O(n)
// Cualquier sentencia O(1)
}
```

Si el ciclo itera un número constante se sigue tomando como tiempo constante O(1).

###### Ejemplo
```cpp
// Donde c NO varía con la entrada 
for (int i=1; i<=c; i++){ //O(1)
// Cualquier sentencia O(1)
}
```




----
## Recursos Extra
Notación Big O:
https://www.youtube.com/watch?v=MyAiCtuhiqQ
