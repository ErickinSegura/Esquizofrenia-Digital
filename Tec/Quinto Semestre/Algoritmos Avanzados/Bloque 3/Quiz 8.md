1. Dados p0 = (−30, 10), p1 = (29, −15), p2 = (15, 28), determinar si el segmento dirigido→p0p1 está en sentido de las manecillas del reloj o no a partir de →p0p2.

$$
P_0=(-30,10)
$$
$$
P_1=(29,-15)
$$
$$
P_2=(15,28)
$$
$$
P_0 P_1 = P_1 - P_0 = (29,-15) - (-30, 10) = (59, -25)
$$
$$
P_0 P_2 = P_2 - P_0 = (15,28) - (-30, 10) = (45, 18)
$$

$$
P_1 x P_2 = det = 59(18) - (-25)(45) = 2187
$$

Quiere decir que $P_1$ se encuentra orientado en el sentido de las mencillas del reloj desde $P_2$
<div class="page-break" style="page-break-before: always;"></div>

2. Dados p2 = (−30, 10), p1 = (29, −15), p0 = (15, 28), determinar si el segmento dirigido →p0p1 está en sentido de las manecillas del reloj o no a partir de →p0p2.


$$
P_0=(15, 28)
$$
$$
P_1=(29,-15)
$$
$$
P_2=(−30, 10)
$$
$$
P_0 P_1 = P_1 - P_0 = (29,-15) - (15, 28) = (14, -43)
$$
$$
P_0 P_2 = P_2 - P_0 = (-30, 10) - (15,28) = (-45, -18)
$$

$$
P_1 x P_2 = det = 14(-18) - (-45)(43) = -2187
$$

Quiere decir que $P_1$ se encuentra orientado en el sentido contrario de las mencillas del reloj desde $P_2$
<div class="page-break" style="page-break-before: always;"></div>


3. Dados p0 = (5, 5), p1 = (7, −2), Y p2 = (−5, 5), ¿cómo gira el ángulo ∠p0p1p2: en sentido de las manecillas del reloj o no? Realice los cálculos correspondientes para justificar su respuesta

Para este ejercicio daré dos respuestas diferentes, primero la respuesta siguiendo el ejemplo de la clase grabada.

$$
P_0=(5, 5)
$$
$$
P_1=(7,-2)
$$
$$
P_2=(−5, 5)
$$
$$
P_0 P_1 = P_1 - P_0 = (7,-2) - (5, 5) = (2, -7)
$$
$$
P_0 P_2 = P_2 - P_0 = (-5, 5) - (5,5) = (-10, 0)
$$

$$
P_1 x P_2 = det = (-10)(-7) - 2(0) = 70
$$

Resolviendo de esta forma quiere decir que el ángulo se encuentra orientado en el sentido de las mencillas del reloj, ahora, la razón por la que lo resolveré es que, utilizando esta forma, estariamos considerando como $P_0$ como el centro de nuestro ángulo, cuando según lo planteado, en realidad $P_1$ sería el centro de nuestro ángulo, tomando en cuenta la solución sería así

$$
P_0=(5, 5)
$$
$$
P_1=(7,-2)
$$
$$
P_2=(−5, 5)
$$
$$
P_1 P_0 = P_0 - P_1 = (5, 5) - (7, -2) = (-2, 7)
$$
$$
P_1 P_2 = P_2 - P_1 = (-5, 5) - (7, -2) = (-12, 7)
$$

$$
P_1 x P_2 = det = (-12)(7) - (-2)(7) = -70
$$

Quiere decir que el ángulo se encuentra orientado en el sentido contrario de las mencillas del reloj.

Viendo gráficamente la posición de los vectores, se puede ver un giro antihorario, haciendo que el primer caso esté mal. Creo que no me vendría mal una explicación del por que el uso de el vector auxiliar, pero por la hora es muy tarde para preguntar, así que será mejor pregunta para más tarde.
<div class="page-break" style="page-break-before: always;"></div>

4. Dado los puntos p0 = (0, 1), p1 = (1, 1), p2 = (3, 4), p3 = (1, 8), p4 = (6, 7), p5 = (10, 4), p6 = (4, 4), p7 = (5, 10), p8 = (6, 1), p9 = (8, 0), y p10 = (4, 8), construya el cierre convexo mediante el algoritmo Graham Scan. Apoye su respuesta mediante la graficación de los puntos y los segmentos de recta que  constituyen el cierre convexo.

$p_9$ se convierte en nuestro punto ancla ($p_0$) por ser el valor de y minimo en Q

Calculamos el ángulo polar de cada punto respecto a $p_0$(8,0)
Si hay puntos con el mismo ángulo, mantenemos el más lejano
2. Ordenamos los puntos por ángulo (de menor a mayor):
1. $p_5$(10,4) - 1.11 rad
2. $p_4$(6,7) - 1.85 rad
3. $p_7$(5,10) - 1.86 rad
4. $p_10$(4,8) - 2.03 rad
5. $p_3$(1,8) - 2.29 rad
6. $p_6$(4,4) - 2.36 rad
7. $p_2$(3,4) - 2.47 rad
8. $p_8$(6,1) - 2.68 rad
9. $p_1$(1,1) - 3.00 rad
10. $p_0$(0,1) - 3.02 

Eliminamos puntos con mismo ángulo, manteniendo el más lejano: Después de eliminar puntos con ángulos similares y mantener los más lejanos, quedamos con:
1. $p_5$(10,4) - 1.11 rad
2. $p_7$(5,10) - 1.86 rad 
3. $p_3$(1,8) - 2.29 rad 
4. $p_0$(0,1) - 3.02 rad

Graficación

![[Pasted image 20241029233737.png]]
