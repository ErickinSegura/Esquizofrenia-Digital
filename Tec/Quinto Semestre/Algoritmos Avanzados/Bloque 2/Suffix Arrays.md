Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]

Dado un string S, de longitud n, su arreglo de sufijos es un arreglo de enteros que contiene las posociones que tienen los n +1 sufijos en el string T = S#, ordenados lexicográficamente, considerando a # como el primer caracter del alfabeto.

```
SuffixArray(S)
T = S#
Sea  n = |T|
Sea C = {}
Sea A  = [1...n] un nuevo arreglo
for i = 0 to n:
	C = C u {(i, T[i...n+1])}
ordenar C de forma lexicografica
for i = 1 to n+1:
	A[i] = tupla i en C'
return A
```

