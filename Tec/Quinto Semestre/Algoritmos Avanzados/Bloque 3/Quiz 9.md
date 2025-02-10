Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]

Dados los puntos p0 = (0, 3), p1 = (1, 1), p2 = (3, 7), p3 = (1, 8), p4 = (6, 7), p5 = (10, 4), p6 = (10, 8), p7 = (5, 8), p8 = (6, 1), p9 = (8, 0), y p10 = (10, 9), construya el cierre convexo mediante el algoritmo Graham Scan. Apoye su respuesta mediante la graficación de los puntos y los segmentos de recta que constituyen el cierre convexo. Calcule manualmente todos los elementos que solicita el algoritmo, i.e., ángulos, pila,  ordenamiento.

$p_9$ se convierte en nuestro punto ancla ($p_0$) por ser el valor de y minimo en Q
Ordenamiento

Q ordenada

| $P_0$    | $P_9$    |
| -------- | -------- |
| $P_1$    | $P_5$    |
| $P_2$    | $P_6$    |
| $P_3$    | $P_{10}$ |
| $P_4$    | $P_4$    |
| $P_5$    | $P_7$    |
| $P_6$    | $P_2$    |
| $P_7$    | $P_3$    |
| $P_8$    | $P_8$    |
| $P_9$    | $P_0$    |
| $P_{10}$ | $P_1$    |
<div class="page-break" style="page-break-before: always;"></div>

Gráficación

![[Quiz 9 2024-11-01 20.22.34.excalidraw]]

Pila resultante
CH(Q) = {$P_0$, $P_1$, $P_3$, $P_7$,$P_9$, $P_{10}$}
