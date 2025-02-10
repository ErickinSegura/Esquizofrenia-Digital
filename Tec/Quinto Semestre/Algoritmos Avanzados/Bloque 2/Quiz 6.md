Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]

Dado el grafo de la figura, ejecute el algoritmo de Dijkstra de forma manual considerando al nodo A como la fuente. Asegúrese de mostrar cómo cambia v.π y v.d ∀v ∈ V.

![[Pasted image 20241004183427.png]]

### Inicialización: 

S = {} (conjunto de vértices procesados) 
Q = {A, B, C, D, E} (cola de prioridad con todos los vértices)

A.d = 0, A.π = NIL 
B.d = ∞, B.π = NIL 
C.d = ∞, C.π = NIL 
D.d = ∞, D.π = NIL 
E.d = ∞, E.π = NIL
### Iteración 1

Q = {B,C,D,E}
S={A}
B.d = 3, B.π = A
C.d = 8, C.π = A
E.d = 3, E.π = A

Estado actual
A.d = 0, A.π = NIL 
B.d = 3, B.π = A
C.d = 8, C.π = A 
D.d = ∞, D.π = NIL 
E.d = 3, E.π = A

### Iteración 2

Q = {E,D,C}
S={A,B}
D.d = 4, E.π = B
E.d = 10, E.π = B

Estado actual
A.d = 0, A.π = NIL 
B.d = 3, B.π = A
C.d = 8, C.π = A 
D.d = 4, D.π = B
E.d = 3, E.π = A

### Iteración 3

Q = {D,C}
S={A,B,E}
D.d = 9, E.π = E

Estado actual
A.d = 0, A.π = NIL 
B.d = 3, B.π = A
C.d = 8, C.π = A 
D.d = 4, D.π = B
E.d = 3, E.π = A

### Iteración 4

Q = {C}
S={A,B,E,D}
A.d = 6, A.π = D
C.d = 9, C.π = D

Estado actual
A.d = 0, A.π = NIL 
B.d = 3, B.π = A
C.d = 8, C.π = A 
D.d = 4, D.π = B
E.d = 3, E.π = A

### Iteración 5

Q = {}
S={A,B,E,D,C}
B.d = 12, E.π = C

Estado actual
A.d = 0, A.π = NIL 
B.d = 3, B.π = A
C.d = 8, C.π = A 
D.d = 4, D.π = B
E.d = 3, E.π = A

Los caminos más cortos desde A a cada vértice son:
- A → A (distancia 0)
- A → B (distancia 3)
- A → C (distancia 8)
- A → B → D (distancia 4)
- A → E (distancia 3)