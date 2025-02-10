Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]
## Pseudocódigo

``` python
isValid(row, col, num):
    for x from 0 to 8:
        if board[row][x] == num or board[x][col] == num:
            return false
    
    startRow = row - (row mod 3)
    startCol = col - (col mod 3)
    for i from 0 to 2:
        for j from 0 to 2:
            if board[startRow + i][startCol + j] == num:
                return false
    
    return true

solve():
    for row from 1 to 9:
        for col from 1 to 9:
            if board[row][col] == 0:
                for num from 1 to 9:
                    if isValid(row, col, num):
                        board[row][col] = num
                        if solve():
                            return true
                        board[row][col] = 0
                return false
    return true
```

<div class="page-break" style="page-break-before: always;"></div>

## Árbol de estados
Ejemplo de solo un 3x3

![[Tarea 4 Backtracking 2024-09-22 22.43.58.excalidraw]]

<div class="page-break" style="page-break-before: always;"></div>

## Análisis de complejidad

``` python
bool solve() {
	for (int row = 0; row < N; row++) {
		for (int col = 0; col < N; col++) {
			if (board[row][col] == 0) {
				for (int num = 1; num <= 9; num++) {
					if (isValid(row, col, num)) {
						board[row][col] = num;
						if (solve()) return true;
						board[row][col] = 0;
					}
				}
				return false;
			}
		}
	}
	return true;
}
```

Tomando en consideración que la función de isValid es de complejidad O(n). En el peor caso, el algoritmo necesita probar todas las posibilidades para cada celda vacía.

- Hay $N^2$ celdas en total (donde $N = 9$ para un Sudoku estándar).
- Para cada celda, en el peor caso, probamos 9 números.
- Después de cada intento, el algoritmo recurre para resolver el resto del tablero.

Esto nos lleva a una complejidad temporal de:
$O(9^{N^2})$
