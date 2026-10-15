# 1 - Matrices
## Ejercicio 1.1

### Parte a)
$$
\begin{align}
&A=(a_{jk}) \in M_{3 \times 4}(\mathbb{R}), a_{jk} = j + k \\
 \\
&\implies A = \begin{pmatrix}
a_{1,1} & a_{1,2} & a_{1,3} & a_{1,4} \\
a_{2,1} & a_{2,2} & a_{2,3} & a_{2,4} \\
a_{3,1} & a_{3,2} & a_{3,3} & a_{3,4}
\end{pmatrix} \text{ con } a_{1,1} = 2, a_{1,2} = 3, a_{1,3} = 4, a_{2,1} = 3, a_{2,2} = 4, etc. \\
 \\
&\implies A = \begin{pmatrix}
2 & 3 & 4 & 5 \\
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7
\end{pmatrix}
\end{align}
$$

### Parte b)
$$
\begin{align}
&B=(b_{jk}) \in M_{3 \times 3}(\mathbb{R}), b_{jk} = \begin{cases}
j \text{ si } j \leq k \\
0 \text{ si } j > k
\end{cases} \\
 \\
&\implies B = \begin{pmatrix}
a_{1,1} & a_{1,2} & a_{1,3} \\
a_{2,1} & a_{2,2} & a_{2,3} \\
a_{3,1} & a_{3,2} & a_{3,3}
\end{pmatrix} \text{ con } a_{1,1} = 1, a_{1,2} = 1, a_{1,3} = 1, a_{2,1} = 0, a_{2,2} = 2, etc. \\
 \\
&\implies B = \begin{pmatrix}
1 & 1 & 1 \\
0 & 2 & 2 \\
0 & 0 & 3
\end{pmatrix}
\end{align}
$$

### Parte c)
$$
\begin{align}
&C=(c_{jk}) \in M_{2 \times 2}(\mathbb{C}), c_{jk} = j + ki \\
 \\
&\implies C = \begin{pmatrix}
a_{1,1} & a_{1,2} \\
a_{2,1} & a_{2,2}
\end{pmatrix} \text{ con } a_{1,1} = 1 + i, a_{1,2} = 1 + 2i, a_{2,1} = 2 + i, a_{2,2} = 2 + 2i \\
 \\
&\implies C = \begin{pmatrix}
1 + i & 1 + 2i \\
2 + i & 2 + 2i
\end{pmatrix} = \begin{pmatrix}
(1, 1) & (1, 2) \\
(2, 1) & (2, 2)
\end{pmatrix}
\end{align}
$$

### Parte d)
$$
\begin{align}
&D=(d_{jk}) \in M_{3 \times 2}(\mathbb{C}), d_{jk} = i^{jk} \\
 \\
&\implies D = \begin{pmatrix}
a_{1,1} & a_{1,2} \\
a_{2,1} & a_{2,2} \\
a_{3,1} & a_{3,2}
\end{pmatrix} \text{ con } a_{1,1} = i^{1 \times 1}, a_{1,2} = i^{1 \times 2}, a_{2,1} = i^{2 \times 1}, a_{2,2} = i^{2 \times 2}, etc. \\
 \\
&\implies D = \begin{pmatrix}
i^{1} & i^{2} \\
i^{2} & i^{4} \\
i^{3} & i^{6}
\end{pmatrix} = \begin{pmatrix}
i & i^{2} \\
i^{2} & i^{2} \times i^{2} \\
i^{2} \times i^{1} & i^{2} \times i^{2} \times i^{2}
\end{pmatrix} = \begin{pmatrix}
i & -1 \\
-1 & (-1) \times (-1) \\
(-1) \times i & (-1) \times (-1) \times (-1)
\end{pmatrix} = \begin{pmatrix}
i & -1 \\
-1 & 1 \\
-i & -1
\end{pmatrix}
\end{align}
$$

## Ejercicio 1.2
- La operación $BA$ no está definida, ya que para que para poder realizar el producto de matrices, la cantidad de columnas de la primer matriz, y la cantidad de filas de la segunda debe ser igual. En este caso, la matriz B tiene 5 columnas, mientras que la matriz A tiene 4 filas, por lo que no se puede realizar dicha operación.
- La operación $AC + D$ está definida, puesto que, primeramente, la operación $AC$ está definida (A tiene 5 columnas y C tiene 5 filas), dando como resultado una nueva matriz de dimensión $4 \times 2$ (comparte cantidad de filas con A y cantidad de columnas con B). De esta forma, la suma entre la nueva matriz y D está definida, ya que ambas poseen exactamente las mismas dimensiones ($4 \times 2$).
- La operación $E(A + B)$ está definida. Comenzando por la suma $A + B$, la cual está definida, ya que A y B tienen exactamente las mismas dimensiones ($4 \times 5$), y, como sabemos, el resultado será una matriz de dimensiones $4 \times 5$. Como la matriz E tiene dimensiones $5 \times 4$, el producto entre E y la matriz resultante de la suma $A + B$ también esta definido, ya que E tiene 4 columnas y la suma tiene 4 filas, de modo que pueden multiplicarse, dando como resultado una matriz de $5 \times 5$.

## Ejercicio 1.3
### $B + B^{t}$
$$
\begin{align}
&B = \begin{pmatrix}
4 & -1 \\
2 & 1
\end{pmatrix} \implies B^{t} = \begin{pmatrix}
4 & 2 \\
-1 & 1
\end{pmatrix} \\
 \\
&\implies B + B^{t} = \begin{pmatrix}
4 + 4 & -1 + 2 \\
2 - 1 & 1 + 1
\end{pmatrix} = \begin{pmatrix}
8 & 1 \\
1 & 2
\end{pmatrix}
\end{align}
$$
### $AA^{t}$
$$
\begin{align}
&A = \begin{pmatrix}
3 & 0 \\
-1 & 2 \\
1 & 1
\end{pmatrix} \implies A^{t} = \begin{pmatrix}
3 & -1 & 1 \\
0 & 2 & 1 \\
\end{pmatrix} \\
 \\
&\implies AA^{t} = \\
 \\

&\begin{pmatrix}
3 & -1 & 1 \\
0 & 2 & 1 \\
\end{pmatrix} \\

\begin{pmatrix}
3 & 0 \\
-1 & 2 \\
1 & 1
\end{pmatrix}

&\begin{pmatrix}
3 \times 3 + 0 \times 0 & 3 \times (-1) + 0 \times 2 & 3 \times 1 + 0 \times 1 \\
(-1) \times 3 + 2 \times 0 & (-1) \times (-1) + 2 \times 2 & (-1) \times 1 + 2 \times 1 \\
1 \times 3 + 1 \times 0 & 1 \times (-1) + 1 \times 2 & 1 \times 1 + 1 \times 1
\end{pmatrix} = \\
&\begin{pmatrix}
9 + 0 & -3 + 0 & 3 + 0 \\
-3 + 0 & 1 + 4 & -1 + 2 \\
3 + 0 & -1 + 2 & 1 + 1
\end{pmatrix} = \\

&\begin{pmatrix}
9 & -3 & 3 \\
-3 & 5 & 1 \\
3 & 1 & 2
\end{pmatrix} \\
 \\
&AA^{t} = \begin{pmatrix}
9 & -3 & 3 \\
-3 & 5 & 1 \\
3 & 1 & 2
\end{pmatrix}
\end{align}
$$

### $(AB)C$
$$
\begin{align}
&A = \begin{pmatrix}
3 & 0 \\
-1 & 2 \\
1 & 1
\end{pmatrix}

B = \begin{pmatrix}
4 & -1 \\
2 & 1
\end{pmatrix}

C = \begin{pmatrix}
1 & 4 & 2 \\
3 & 1 & 5
\end{pmatrix} \\
 \\
&AB =  \\
 \\
&\begin{pmatrix}
4 & -1 \\
2 & 1
\end{pmatrix} \\

\begin{pmatrix}
3 & 0 \\
-1 & 2 \\
1 & 1
\end{pmatrix}

&\begin{pmatrix}
3 \times 4 + 0 \times 2 & 3 \times (-1) + 0 \times 1 \\
(-1) \times 4 + 2 \times 2 & (-1) \times (-1) + 2 \times 1 \\
1 \times 4 + 1 \times 2 & 1 \times (-1) + 1 \times 1
\end{pmatrix} = \\
&\begin{pmatrix}
12 + 0 & -3 + 0 \\
-4 + 4 & 1 + 2 \\
4 + 2 & -1 + 1
\end{pmatrix} = \\

&\begin{pmatrix}
12 & -3 \\
0 & 3 \\
6 & 0
\end{pmatrix} \\
 \\
&AB = \begin{pmatrix}
12 & -3 \\
0 & 3 \\
6 & 0
\end{pmatrix} \\
 \\

&(AB)C = \\
 \\
&\begin{pmatrix}
1 & 4 & 2 \\
3 & 1 & 5
\end{pmatrix} \\

\begin{pmatrix}
12 & -3 \\
0 & 3 \\
6 & 0
\end{pmatrix}

&\begin{pmatrix}
12 \times 1 + (-3) \times 3 & 12 \times 4 + (-3) \times 1 & 12 \times 2 + (-3) \times 5 \\
0 \times 1 + 3 \times 3 & 0 \times 4 + 3 \times 1 & 0 \times 2 + 3 \times 5 \\
6 \times 1 + 0 \times 3 & 6 \times 4 + 0 \times 1 & 6 \times 2 + 0 \times 5
\end{pmatrix} = \\
&\begin{pmatrix}
12 - 9 & 48 - 3 & 24 - 15 \\
0 + 9 & 0 + 3 & 0 + 15 \\
6 + 0 & 24 + 0 & 12 + 0
\end{pmatrix} = \\

&\begin{pmatrix}
3 & 45 & 9 \\
9 & 3 & 15 \\
6 & 24 & 12
\end{pmatrix} \\
 \\
&(AB)C = \begin{pmatrix}
3 & 45 & 9 \\
9 & 3 & 15 \\
6 & 24 & 12
\end{pmatrix}
\end{align}
$$

### $DE - ED$
$$
\begin{align}
&D = \begin{pmatrix}
1 & -1 & 1 \\
-3 & 2 & -1 \\
-2 & 1 & 0
\end{pmatrix}

E = \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
1 & 2 & 3
\end{pmatrix} \\
 \\
&DE =  \\
 \\
&\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
1 & 2 & 3
\end{pmatrix} \\

\begin{pmatrix}
1 & -1 & 1 \\
-3 & 2 & -1 \\
-2 & 1 & 0
\end{pmatrix}

&\begin{pmatrix}
1 \times 1 + (-1) \times 2 + 1 \times 1 & 1 \times 2 + (-1) \times 4 + 1 \times 2 & 1 \times 3 + (-1) \times 6 + 1 \times 3 \\
(-3) \times 1 + 2 \times 2 + (-1) \times 1 & (-3) \times 2 + 2 \times 4 + (-1) \times 2 & (-3) \times 3 + 2 \times 6 + (-1) \times 3 \\
(-2) \times 1 + 1 \times 2 + 0 \times 1 & (-2) \times 2 + 1 \times 4 + 0 \times 2 & (-2) \times 3 + 1 \times 6 + 0 \times 3
\end{pmatrix} = \\
&\begin{pmatrix}
1 - 2 + 1 & 2 - 4 + 2 & 3 - 6 + 3 \\
-3 + 4 - 1 & -6 + 8 - 2 & -9 + 12 - 3 \\
-2 + 2 + 0 & -4 + 4 + 0 & -6 + 6 + 0
\end{pmatrix} = \\

&\begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix} \\
 \\
&DE = \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix} \\
 \\ \\

&ED =  \\
 \\
&\begin{pmatrix}
1 & -1 & 1 \\
-3 & 2 & -1 \\
-2 & 1 & 0
\end{pmatrix} \\

\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
1 & 2 & 3
\end{pmatrix}

&\begin{pmatrix}
1 \times 1 + 2 \times (-3) + 3 \times (-2) & 1 \times (-1) + 2 \times 2 + 3 \times 1 & 1 \times 1 + 2 \times (-1) + 3 \times 0 \\
2 \times 1 + 4 \times (-3) + 6 \times (-2) & 2 \times (-1) + 4 \times 2 + 6 \times 1 & 2 \times 1 + 4 \times (-1) + 6 \times 0 \\
1 \times 1 + 2 \times (-3) + 3 \times (-2) & 1 \times (-1) + 2 \times 2 + 3 \times 1 & 1 \times 1 + 2 \times (-1) + 3 \times 0
\end{pmatrix} = \\
&\begin{pmatrix}
1 - 6 - 6 & -1 + 4 + 3 & 1 - 2 + 0 \\
2 - 12 - 12 & -2 + 8 + 6 & 2 - 4 + 0 \\
1 - 6 - 6 & -1 + 4 + 3 & 1 - 2 + 0
\end{pmatrix} = \\

&\begin{pmatrix}
-11 & 6 & -1 \\
-22 & 12 & -2 \\
-11 & 6 & -1
\end{pmatrix} \\
 \\
&ED = \begin{pmatrix}
-11 & 6 & -1 \\
-22 & 12 & -2 \\
-11 & 6 & -1
\end{pmatrix} \\
 \\ \\

&\implies DE - ED = \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix} - \begin{pmatrix}
-11 & 6 & -1 \\
-22 & 12 & -2 \\
-11 & 6 & -1
\end{pmatrix} = \begin{pmatrix}
11 & -6 & 1 \\
22 & -12 & 2 \\
11 & -6 & 1
\end{pmatrix}
\end{align}
$$

## Ejercicio 1.4
### $BC$
$$
\begin{align}
&B = \begin{pmatrix}
1 + i & 3 \\
2 & 1 + 2i
\end{pmatrix}

C = \begin{pmatrix}
i & -1 & 2 + 3i \\
-3 + 3i & 2 & -1 + 2i
\end{pmatrix} \\
 \\
&\implies BC = \\
 \\

&\begin{pmatrix}
i & -1 & 2 + 3i \\
-3 + 3i & 2 & -1 + 2i
\end{pmatrix} \\

\begin{pmatrix}
1 + i & 3 \\
2 & 1 + 2i
\end{pmatrix}

&\begin{pmatrix}
(1 + i)i + 3(-3 + 3i) & -(1 + i) + 3 \times 2 & (1 + i)(2 + 3i) + 3(-1 + 2i) \\
2i + (1 + 2i)(-3 + 3i) & -2 + 2(1 + 2i) & 2(2 + 3i) + (1 + 2i)(-1 + 2i)
\end{pmatrix} = \\
&\begin{pmatrix}
i + i^{2} -9 + 9i & -1 - i + 6 & 2 + 3i + 2i + 3i^{2} - 3 + 6i \\
2i - 3 + 3i - 6i + 6i^{2} & -2 + 2 + 4i & 4 + 6i - 1 + 2i - 2i + 4i^{2}
\end{pmatrix} = \\

&\begin{pmatrix}
i - 1 - 9 + 9i & -1 - i + 6 & 2 + 3i + 2i - 3 - 3 + 6i \\
2i - 3 + 3i - 6i - 6 & -2 + 2 + 4i & 4 + 6i - 1 + 2i - 2i - 4
\end{pmatrix} =  \\

&\begin{pmatrix}
-10 + 10i & 5 - i & -4 + 11i \\
-9 - i & 4i & -1 + 6i
\end{pmatrix} \\
 \\
&BC = \begin{pmatrix}
-10 + 10i & 5 - i & -4 + 11i \\
-9 - i & 4i & -1 + 6i
\end{pmatrix}
\end{align}
$$

### $AA^{t}$
$$
\begin{align}
&A = \begin{pmatrix}
1 & i \\
-i & 1
\end{pmatrix}

\implies A^{t} = \begin{pmatrix}
1 & -i \\
i & 1
\end{pmatrix} \\
 \\
&\implies AA^{t} = \\
 \\

&\begin{pmatrix}
1 & -i \\
i & 1
\end{pmatrix} \\

\begin{pmatrix}
1 & i \\
-i & 1
\end{pmatrix}

&\begin{pmatrix}
1^{2} + i^{2} & -i + i \\
-i + i & i^{2} + 1^{2}
\end{pmatrix} = \\
&\begin{pmatrix}
1 - 1 & -i + i \\
-i + i & -1 + 1
\end{pmatrix} = \\

&\begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix} \\
 \\
&AA^{t} = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix}
\end{align}
$$

### $A^{t}A$
$$
\begin{align}
&A = \begin{pmatrix}
1 & i \\
-i & 1
\end{pmatrix}

\implies A^{t} = \begin{pmatrix}
1 & -i \\
i & 1
\end{pmatrix} \\
 \\
&\implies A^{t}A = \\
 \\

&\begin{pmatrix}
1 & i \\
-i & 1
\end{pmatrix} \\

\begin{pmatrix}
1 & -i \\
i & 1
\end{pmatrix}

&\begin{pmatrix}
1^{2} + i^{2} & i - i \\
i - i & i^{2} + 1^{2}
\end{pmatrix} = \\
&\begin{pmatrix}
1 - 1 & i - i \\
i - i & -1 + 1
\end{pmatrix} = \\

&\begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix} \\
 \\
&A^{t}A = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix}
\end{align}
$$

### $(AB)C$
$$
\begin{align}
&A = \begin{pmatrix}
1 & i \\
-i & 1
\end{pmatrix}

B = \begin{pmatrix}
1 + i & 3 \\
2 & 1 + 2i
\end{pmatrix}

C = \begin{pmatrix}
i & -1 & 2 + 3i \\
-3 + 3i & 2 & -1 + 2i
\end{pmatrix} \\
 \\
&\implies AB = \\
 \\

&\begin{pmatrix}
1 + i & 3 \\
2 & 1 + 2i
\end{pmatrix} \\

\begin{pmatrix}
1 & i \\
-i & 1
\end{pmatrix}

&\begin{pmatrix}
1(1+i) + 2i & 1 \times 3 + i(1+2i) \\
-i(1 + i) + 1 \times 2 & -3i + 1(1 + 2i)
\end{pmatrix} = \\
&\begin{pmatrix}
1 + i + 2i & 3 + i + 2i^{2} \\
-i - i^{2} + 2 & -3i + 1 + 2i
\end{pmatrix} = \\

&\begin{pmatrix}
1 + i + 2i & 3 + i - 2\\
-i + 1 + 2 & -3i + 1 + 2i
\end{pmatrix} \\

&\begin{pmatrix}
1 + 3i & 1 + i\\
3 - i & 1 - i
\end{pmatrix} \\
 \\
&AB = \begin{pmatrix}
1 + 3i & 1 + i\\
3 - i & 1 - i
\end{pmatrix} \\
 \\
&\implies (AB)C = \\
 \\

&\begin{pmatrix}
i & -1 & 2 + 3i \\
-3 + 3i & 2 & -1 + 2i
\end{pmatrix} \\

\begin{pmatrix}
1 + 3i & 1 + i\\
3 - i & 1 - i
\end{pmatrix}

&\begin{pmatrix}
(1 + 3i)i + (1 + i)(-3 + 3i) & -(1 + 3i) + 2(1 + i) & (1 + 3i)(2 + 3i) + (1 + i)(-1 + 2i) \\
(3 - i)i + (1 - i)(-3 + 3i) & -(3 - i) + 2(1 - i) & (3 - i)(2 + 3i) + (1 - i)(-1 + 2i)
\end{pmatrix} = \\
&\begin{pmatrix}
i + 3i^{2} - 3 + 3i - 3i + 3i^{2} & -1 - 3i + 2 + 2i & 2 + 3i + 6i + 9i^{2} - 1 + 2i - i + 2i^{2} \\
3i - i^{2} - 3 + 3i + 3i - 3i^{2} & -3 + i + 2 - 2i & 6 + 9i - 2i - 3i^{2} - 1 + 2i + i - 2i^{2}
\end{pmatrix} = \\

&\begin{pmatrix}
i - 3 - 3 + 3i - 3i - 3 & -1 - 3i + 2 + 2i & 2 + 3i + 6i - 9 - 1 + 2i - i - 2 \\
3i + 1 - 3 + 3i + 3i + 3 & -3 + i + 2 - 2i & 6 + 9i - 2i + 3 - 1 + 2i + i + 2
\end{pmatrix} \\

&\begin{pmatrix}
-9 + i & 1 - i & -10 + 10i \\
1 + 9i & -1 - i & 10 + 10i
\end{pmatrix} \\
 \\
&(AB)C = \begin{pmatrix}
-9 + i & 1 - i & -10 + 10i \\
1 + 9i & -1 - i & 10 + 10i
\end{pmatrix}
\end{align}
$$

## Ejercicio 1.5
Las matrices $2 \times 2$ que conmutan con $A = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$, son aquellas que tienen forma $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$, con $a = d$ y $c = 0$.
Algunos ejemplos, de matrices $2 \times 2$ que conmutan con A:
$$
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}, \begin{pmatrix}
2 & 0 \\
0 & 2
\end{pmatrix}, \begin{pmatrix}
10 & 4 \\
0 & 10
\end{pmatrix}, etc.
$$
Algunos ejemplos, de matrices $2 \times 2$ que no conmutan con A:
$$
\begin{pmatrix}
1 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 2
\end{pmatrix}, \begin{pmatrix}
2 & 3 \\
0 & 4
\end{pmatrix}, \begin{pmatrix}
10 & 0 \\
0 & -5
\end{pmatrix}, etc.
$$

## Ejercicio 1.7
### Parte a)
Esto es verdadero, y es más sencillo verlo con un ejemplo acotado:
Básicamente, sabemos que el valor de cada celda $c_{i,j}$ esta formado por la suma de productos de todos los elementos de la fila i de A, y la columna j de B.
Por esta razón sucede que, si la primera y tercera columna de B son iguales, entonces en el producto AB, cada celda de la primer columna estará conformada por la suma del producto de todos los elementos de la fila correspondiente de A, y la columna correspondiente de B. En la tercera columna se da lo mismo, por lo que las columnas serán idénticas.
$$
\begin{align}
&A = \begin{pmatrix}
a_{1} & a_{2} & a_{3} \\
a_{4} & a_{5} & a_{6} \\
a_{7} & a_{8} & a_{9}
\end{pmatrix} \\
&B = \begin{pmatrix}
b_{1} & b_{2} & b_{1} \\
b_{4} & b_{5} & b_{4} \\
b_{7} & b_{8} & b_{7}
\end{pmatrix} \\
 \\
&AB =  \\
&\begin{pmatrix}
b_{1} & b_{2} & b_{1} \\
b_{4} & b_{5} & b_{4} \\
b_{7} & b_{8} & b_{7}
\end{pmatrix} \\

\begin{pmatrix}
a_{1} & a_{2} & a_{3} \\
a_{4} & a_{5} & a_{6} \\
a_{7} & a_{8} & a_{9}
\end{pmatrix}

&\begin{pmatrix}
a_{1} \times b_{1} + a_{2} \times b_{4} + a_{3} \times b_{7} & a_{1} \times b_{2} + a_{2} \times b_{5} + a_{3} \times b_{8} & a_{1} \times b_{1} + a_{2} \times b_{4} + a_{3} \times b_{7} \\
a_{4} \times b_{1} + a_{5} \times b_{4} + a_{6} \times b_{7} & a_{4} \times b_{2} + a_{5} \times b_{5} + a_{6} \times b_{8} & a_{4} \times b_{1} + a_{5} \times b_{4} + a_{6} \times b_{7} \\
a_{7} \times b_{1} + a_{8} \times b_{4} + a_{9} \times b_{7} & a_{7} \times b_{2} + a_{8} \times b_{5} + a_{9} \times b_{8} & a_{7} \times b_{1} + a_{8} \times b_{4} + a_{9} \times b_{7}
\end{pmatrix}
\end{align}
$$
Como vemos, las columnas 1 y 3 de AB son iguales, ya que las columnas 1 y 3 de B son iguales.

# 2 - Operadores en matrices y matrices especiales
## Ejercicio 2.1
### Parte a)
#### $(A + B)^{t} = A^{t} + B^{t}$
Sean $A = ((a_{i,j})), B = ((b_{i,j})) \in M_{m \times n}$. Entonces, si notamos $C = A + B, C = ((c_{i,j}))$ donde $c_{i,j} = a_{i,j} + b_{i,j}$, tenemos que $C^{t} = ((c_{i,j}^{t})$ donde $c_{i,j}^{t} = c_{j,i}$. De esta forma:
$$
(A + B)^{t} = C^{t} = ((c_{i,j}^{t})) = ((c_{j,i})) = ((a_{j,i} + b_{j,i})) = ((a_{j,i})) + ((b_{j,i})) = ((a_{i,j}^{t})) + ((b_{i,j}^{t})) = A^{t} + B^{t}
$$

#### $(\alpha A)^{t} = \alpha A^{t}$
Sea $A = ((a_{i,j})) \in M_{m \times n}, \alpha \in \mathbb{R}$, calcularemos la traspuesta de $\alpha A = ((\alpha a_{i,j}))$:
$$
(\alpha A)^{t} = (((\alpha a_{i,j})^{t})) = ((\alpha a_{j,i})) = \alpha((a_{j,i})) = \alpha((a_{i,j}^{t})) = \alpha A^{t}
$$

#### $(AB)^{t} = B^{t}A^{t}$
Sea $A = ((a_{i,j})) \in M_{m \times p}, B = ((b_{i,j})) \in M_{p \times n}$. Entonces notamos $C = AB, C = ((c_{i,j}))$, donde $c_{i,j} = \sum_{k = 1}^{p} a_{i,k} b_{k,j}$, por lo tanto:
$$
(AB)^{t} = C^{t} = ((c_{i,j}^{t})) = ((c_{j,i})) = \left( \left( \sum_{k = 1}^{p} a_{j,k} b_{k,i} \right) \right) = \left( \left( \sum_{k = 1}^{p} a_{k,j}^{t} b_{i,k}^{t} \right) \right) = \left( \left( \sum_{k = 1}^{p} b_{i,k}^{t} a_{k,j}^{t} \right) \right) = B^{t}A^{t}
$$

### Parte b)
Sea $A = ((a_{i,j})) \in M_{n \times n}, \lambda \in \mathbb{R} \setminus \{ -1, 1 \}$. Si $A = \lambda A^{t}$, entonces:
$$
\begin{cases}
a_{i,j} = \lambda a_{i,j}^{t} = \lambda a_{j,i} \\
a_{j,i} = \lambda a_{j,i}^{t} = \lambda a_{i,j}
\end{cases}
$$
De esta forma, podemos seguir extendiendo los casos:
$$
\begin{cases}
a_{i,j} = \lambda a_{i,j}^{t} = \lambda a_{j,i} = \lambda^{2} a_{j,i}^{t} = \lambda^{2} a_{i,j} \\
a_{j,i} = \lambda a_{j,i}^{t} = \lambda a_{i,j} = \lambda^{2} a_{i,j}^{t} = \lambda^{2} a_{j,i}
\end{cases}
$$
En conclusión, determinamos que $a_{i,j} = \lambda^{2} a_{i,j}$. De esta forma, y sabiendo que $\lambda \neq \pm 1 \implies \lambda^{2} \neq 1$, concluimos que $a_{i,j} = 0$ para todos $i, j$.

### Parte c)
Sea $A = ((a_{i,j})), B = ((b_{i,j})) \in M_{n \times n}, p, q \in \mathbb{R}$. Si $A = qB^{t}$ y $B = pA^{t}$.
Recordemos que $(A^{t})^{t} = A$ y $(\alpha A)^{t} = \alpha A^{t}$. De esta forma $B^{t} = (pA^{t})^{t} = pA$ y $A^{t} = (qB^{t})^{t} = qB$.
Como $A = qB^{t}$ y $B^{t} = pA$, esto implica que $A = qpA$. En conclusión, $pq = 1$.
