Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]

# Casos de Prueba
## Caso 1

#### Instancia Original

```
0 5 9 9 1
5 0 10 2 1
9 10 0 7 5
9 2 7 0 6
1 1 5 6 0
```

![[1_grafo_original.png]]
<div class="page-break" style="page-break-before: always;"></div>

#### Resultado

```
 0  0  0  0  1 
 0  0  0  2  0 
 0  0  0  0  0 
 0  0  0  0  0 
 0  1  5  0  0 
```

![[1_output_caminos_cortos.png]]
<div class="page-break" style="page-break-before: always;"></div>

## Caso 2

#### Instancia Original

```
0 1 2 0 7
1 0 6 3 2
2 6 0 0 6
0 3 0 0 10
7 2 6 10 0
```

![[2_grafo_original.png]]
<div class="page-break" style="page-break-before: always;"></div>

#### Resultado

```
 0  1  2  0  0 
 0  0  0  3  2 
 0  0  0  0  0 
 0  0  0  0  0 
 0  0  0  0  0 
```

![[2_output_caminos_cortos.png]]
<div class="page-break" style="page-break-before: always;"></div>

## Caso 3

#### Instancia Original

```
0 0 9 5 4
0 0 0 5 0
9 0 0 5 4
5 5 5 0 3
4 0 4 3 0
```

![[3_grafo_original.png]]
<div class="page-break" style="page-break-before: always;"></div>

#### Resultado

```
 0  0  0  5  4 
 0  0  0  0  0 
 0  0  0  0  0 
 0  5  0  0  0 
 0  0  4  0  0 
```

![[3_output_caminos_cortos.png]]
<div class="page-break" style="page-break-before: always;"></div>

## Caso 4

#### Instancia Original

```
0 2 0 1 0 0 0
2 0 0 10 9 0 0
0 0 0 7 10 1 0
1 10 7 0 2 1 0
0 9 10 2 0 4 6
0 0 1 1 4 0 4
0 0 0 0 6 4 0
```

![[4_grafo_original.png]]
<div class="page-break" style="page-break-before: always;"></div>

#### Resultado

```
 0  2  0  1  0  0  0 
 0  0  0  0  0  0  0 
 0  0  0  0  0  0  0 
 0  0  0  0  2  1  0 
 0  0  0  0  0  0  0 
 0  0  1  0  0  0  4 
 0  0  0  0  0  0  0 
```

![[4_output_caminos_cortos.png]]
<div class="page-break" style="page-break-before: always;"></div>

## Caso 5

#### Instancia Original

```
0 0 0 10 0 0 0 0 0 0
0 0 0 0 2 0 0 9 0 0
0 0 0 0 0 0 0 7 0 0
10 0 0 0 0 3 0 0 10 6
0 2 0 0 0 4 2 0 7 0
0 0 0 3 4 0 0 0 0 0
0 0 0 0 2 0 0 7 2 0
0 9 7 0 0 0 7 0 3 0
0 0 0 10 7 0 2 3 0 0
0 0 0 6 0 0 0 0 0 0
```

![[5_grafo_original.png]]
<div class="page-break" style="page-break-before: always;"></div>

#### Resultado

```
 0  0  0  10 0  0  0  0  0  0 
 0  0  0  0  0  0  0  0  0  0 
 0  0  0  0  0  0  0  0  0  0 
 0  0  0  0  0  3  0  0  10 6 
 0  2  0  0  0  0  2  0  0  0 
 0  0  0  0  4  0  0  0  0  0 
 0  0  0  0  0  0  0  0  0  0 
 0  0  7  0  0  0  0  0  0  0 
 0  0  0  0  0  0  0  3  0  0 
 0  0  0  0  0  0  0  0  0  0 
```

![[5_output_caminos_cortos.png]]
