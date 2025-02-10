Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]

$$T_1, T_2 \epsilon \Sigma^* $$

Problema. Encontrar coincidencias entre T1 y T2
T1 = ababcaa
T2 = acabcabca

Programación Dinámica
```
for i=0 to n
	for j=0 to m	
		if T1[i] = T2[j]
			dp[i,j] = dp[i-1,j-1]+1
		else
			dp[i,j] = 0
```


| T1/T2 | j   | a   | c   | a   | b   | c   | a   | b   | c   | a   |
| ----- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| i     | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| a     | 0   | 1   | 0   | 1   | 0   | 0   | 1   | 0   | 0   | 1   |
| b     | 0   | 0   | 0   | 0   | 2   | 0   | 0   | 2   | 0   | 0   |
| a     | 0   | 1   | 0   | 1   | 0   | 0   | 1   | 0   | 0   | 1   |
| b     | 0   | 0   | 0   | 0   | 2   | 0   | 0   | 2   | 0   | 0   |
| c     | 0   | 0   | 1   | 0   | 0   | 3   | 0   | 0   | 3   | 0   |
| a     | 0   | 1   | 0   | 2   | 0   | 0   | 4   | 0   | 0   | 4   |
| a     | 0   | 1   | 0   | 1   | 0   | 0   | 1   | 0   | 0   | 1   |

LCS = abca

## Ejemplos
### Problema 1
T1 = ABCDCAB
T2 = BDCABA

| T1/T2 | j   | B   | D   | C   | A   | B   | A   |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| i     | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| A     | 0   | 0   | 0   | 0   | 1   | 0   | 1   |
| B     | 0   | 1   | 0   | 0   | 0   | 2   | 0   |
| C     | 0   | 0   | 0   | 1   | 0   | 0   | 0   |
| D     | 0   | 0   | 1   | 0   | 0   | 0   | 0   |
| C     | 0   | 0   | 0   | 2   | 0   | 0   | 0   |
| A     | 0   | 0   | 0   | 0   | 3   | 0   | 1   |
| B     | 0   | 1   | 0   | 0   | 0   | 4   | 0   |
LCS = DCAB
T1[4...7]
T2[2...5]

### Problema 2

T2 = aabcaba
T1 = cabcbabacc

| T1/T2 | j   | a   | a   | b   | c   | a   | b   | a   |
| ----- | --- | --- | --- | --- | --- | --- | --- | --- |
| i     | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   |
| c     | 0   | 0   | 0   | 0   | 1   | 0   | 0   | 0   |
| a     | 0   | 1   | 1   | 0   | 0   | 2   | 0   | 1   |
| b     | 0   | 0   | 0   | 2   | 0   | 0   | 3   | 0   |
| c     | 0   | 0   | 0   | 0   | 3   | 0   | 0   | 0   |
| b     | 0   | 0   | 0   | 1   | 0   | 0   | 1   | 0   |
| a     | 0   | 1   | 1   | 0   | 0   | 1   | 0   | 2   |
| b     | 0   | 0   | 0   | 2   | 0   | 0   | 2   | 0   |
| a     | 0   | 1   | 1   | 0   | 0   | 1   | 0   | 3   |
| c     | 0   | 0   | 0   | 0   | 1   | 0   | 0   | 0   |
| c     | 0   | 0   | 0   | 0   | 1   | 0   | 0   | 0   |
LCS = abc, cab, aba
T1 = [2...4], [1...3], [6...8]
T2 = [2...4], [4...6], [5...7]


# Pseudocódigo
```
LCS(T1,T2):
	n = |T1|, m = |T2|
	dp = matrix[0...n][0...m]
	for i = 0 to n
		dp[i,0]=0
	for i = 0 to m
		dp[0,i]=0
	max=0
	for i=0 to n
		for j=0 to m	
			if T1[i] = T2[j]
				dp[i,j] = dp[i-1,j-1]+1
			else
				dp[i,j] = 0
			max = (dp[i,j] > max) ? dp[i,j] : max
	return max
```