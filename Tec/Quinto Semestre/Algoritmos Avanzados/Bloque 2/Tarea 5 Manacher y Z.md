Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]

## Pseudocódigo

```
function PAL(D, N)
    // D es el string de entrada, N es su longitud
    // M es un array auxiliar de longitud N-1
    initialize M[1..N-1] to 0
    ENP = 1 // End pointer (cursor)
    MDP = 0 // Middle pointer (centro temporal)
    BP = 0  // Beginning pointer (elemento espejo del cursor)
    
    while ENP < N
        ENP = ENP + 1
        MDP = BP = ENP - 1
        COUNT = 0
        
        while BP > 0 and ENP <= N and D[ENP] == D[BP]
            COUNT = COUNT + 1
            ENP = ENP + 1
            BP = BP - 1
        
        if BP == 0
            return ENP // Palíndromo encontrado
        
        M[MDP] = COUNT // Guardamos el número de símbolos espejados
        
        for F = 1 to COUNT
            if M[MDP - F] != COUNT - F
                M[MDP + F] = min(COUNT - F, M[MDP - F])
            else
                MDP = MDP + F
                COUNT = COUNT - F
                BP = MDP - COUNT
                break
        
        if F > COUNT
            ENP = MDP + 1 // No se encontró un nuevo centro
    
    return 0 // No se encontró palíndromo
```

## Análisis de complejidad

El algoritmo de Manacher tiene una complejidad de tiempo O(n), donde n es la longitud del string de entrada.
Explicación:
1. El bucle principal recorre solo una vez cada carácter del string.
2. Existen bucles anidados, pero el puntero de ENP siempre avanza hacia adelante.
3. El array M se llena solo una vez por cada posición

