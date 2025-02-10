Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]

## 1. Algoritmo de Kruskal

### Funcionamiento
El algoritmo de Kruskal es un método eficiente para encontrar un árbol de expansión mínima (MST) en un grafo conectado y ponderado. El proceso es el siguiente:

1. Ordenar todas las aristas del grafo en orden ascendente según su peso.
2. Inicializar un conjunto donde cada vértice es un árbol separado.
3. Para cada arista, en orden ascendente de peso:
   - Si los vértices que conecta la arista pertenecen a árboles diferentes:
     - Agregar la arista al MST.
     - Unir los dos árboles en uno solo.
4. El proceso termina cuando todos los vértices están en un solo árbol.

### Complejidad
- Tiempo: O(E log E), donde E es el número de aristas en el grafo.

### Aplicaciones
- Diseño de redes (telecomunicaciones, eléctricas, de transporte).
- Agrupamiento en aprendizaje automático.
- Optimización de rutas en logística.
- Diseño de circuitos integrados.

## 2. Algoritmo de Welsh-Powell

### Funcionamiento
El algoritmo de Welsh-Powell es un algoritmo para la coloración de grafos. Los pasos son:

1. Ordenar los vértices en orden descendente según su grado.
2. Asignar el primer color al primer vértice de la lista.
3. Recorrer la lista ordenada y asignar este color a cada vértice que no sea adyacente a ningún vértice ya coloreado con este color.
4. Repetir los pasos 2 y 3 con un nuevo color hasta que todos los vértices estén coloreados.

### Complejidad
- Tiempo: O(V^2), donde V es el número de vértices del grafo.

### Aplicaciones
- Asignación de frecuencias en redes de telecomunicaciones.
- Programación de horarios y recursos.
- Registro de asignación en compiladores.
- Resolución de conflictos en sistemas distribuidos.


## Conclusiones

Tanto Kruskal como Welsh-Powell son algoritmos fundamentales en teoría de grafos, pero sirven para propósitos muy diferentes. Kruskal se especializa en encontrar la forma más económica de conectar todos los puntos de una red (como encontrar la manera más barata de conectar ciudades con cables), mientras que Welsh-Powell se centra en asignar diferentes "colores" o recursos a elementos que no pueden compartir el mismo recurso (como asignar frecuencias de radio a estaciones cercanas sin que interfieran entre sí).

Lo interesante es que, aunque tienen objetivos distintos, ambos algoritmos siguen una estrategia similar: ordenar elementos (aristas en Kruskal, vértices en Welsh-Powell) y luego procesarlos de manera sistemática para llegar a una solución óptima o cercana a la óptima.