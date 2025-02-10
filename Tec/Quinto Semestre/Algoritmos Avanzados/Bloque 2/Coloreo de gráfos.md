Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]

Entrada: Un grafo no dirigido G = (V,E)
Problema: Colorear los vértices de V usando el mínimo de números de colores tal que i, j E V tengan diferente color para todo (i,j) E E.
El mínimo número de colores T* se le llama NÚMERO CROMÁTICO DE G

* Grado de un vértice uEV
grad(u) = |{xEV|x!=}|


Algoritmo de Welsh-Powell
1. Calcular el grado de cada uno de los nodos.
2. Ordenas los nodos por el grado en forma decreciente por el grado.
3. Colorear el promer nodo en la lista y asignarle el color 1.
4. Recorrer la lista y colorear todos los nodos no adyacentes al noodo coloreado con el mismo color y verificar la restricción de color con sus adyacentes.
5. Eliminar los nodos coloreados de la vista
6. Repitiendo los pasos 4 y 5 en todos los nodos no coloreados con un nuevo color hasta que no haya más nodos por colorear