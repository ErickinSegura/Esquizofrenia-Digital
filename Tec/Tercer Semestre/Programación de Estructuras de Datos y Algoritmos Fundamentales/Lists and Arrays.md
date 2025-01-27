---
Nombre: Erick Segura Sánchez.
Matrícula: A01613821.
---
links: [[Programación de Estructuras de Datos y Algoritmos Fundamentales]]
Fecha: Thursday 10/August/2023, 06:13 pm

#### Array
- Fixed size: int[] arr = new int[5];
- Simple access to any element arr[i]
- Enlarging and inserting and removing elements is expensive.

Inserting elements at the beginning of an array is "expensive":
  - The array must be enlarged.
  - All the follow elements must be moved to the back.
  - Only then is the space available to insert the new items.

#### List 
- Each element holds a reference to the next.
- No arbitrary access to elements.
- Iteration always starts at the first element.
- Depending on the implementation, also backwards.

Easy insertion and removal of items, even at the top of the list.
Insert or delete a node “Bend” reference to next node.



![[Pasted image 20230811113906.png]]


