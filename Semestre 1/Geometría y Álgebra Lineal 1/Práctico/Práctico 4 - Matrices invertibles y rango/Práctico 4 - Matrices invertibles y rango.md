# 1 - Matrices invertibles
## Ejercicio 1.1
### Parte a)
$$
\left(
\begin{array}{cc|cc}
-3 & -5 & 1 & 0 \\
2 & 3 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|cc}
-3 & -5 & 1 & 0 \\
0 & -1 & 2 & 3
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow 3F_{2} + 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
-3 & -5 & 1 & 0 \\
0 & 1 & -2 & -3
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
-3 & 0 & -9 & -15 \\
0 & 1 & -2 & -3
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 5F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
1 & 0 & 3 & 5 \\
0 & 1 & -2 & -3
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{-3}
\end{align}
$$
La matriz inversa de $\begin{pmatrix} -3 & -5 \\ 2 & 3 \end{pmatrix}$ es $\begin{pmatrix} 3 & 5 \\ -2 & -3 \end{pmatrix}$

### Parte e)
$$
\left(
\begin{array}{ccc|ccc}
2 & 1 & 0 & 1 & 0 & 0 \\
1 & 1 & 4 & 0 & 1 & 0 \\
2 & 1 & 2 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
2 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 8 & -1 & 2 & 0 \\
0 & 0 & 2 & -1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow 2F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
2 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 8 & -1 & 2 & 0 \\
0 & 0 & 1 & -\frac{1}{2} & 0 & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{F_{3}}{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
2 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & 3 & 2 & -4 \\
0 & 0 & 1 & -\frac{1}{2} & 0 & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 8F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
2 & 0 & 0 & -2 & -2 & 4 \\
0 & 1 & 0 & 3 & 2 & -4 \\
0 & 0 & 1 & -\frac{1}{2} & 0 & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & -1 & -1 & 2 \\
0 & 1 & 0 & 3 & 2 & -4 \\
0 & 0 & 1 & -\frac{1}{2} & 0 & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{2}
\end{align}
$$
La matriz inversa de $\begin{pmatrix} 2 & 1 & 0 \\ 1 & 1 & 4 \\ 2 & 1 & 2 \end{pmatrix}$ es $\begin{pmatrix} -1 & -1 & 2 \\ 3 & 2 & -4 \\ -\frac{1}{2} & 0 & \frac{1}{2} \end{pmatrix}$

### Parte h)
$$
\left(
\begin{array}{cc|cc}
1 & i & 1 & 0 \\
2 & 1 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|cc}
1 & i & 1 & 0 \\
0 & 1 - 2i & -2 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
1 & i & 1 & 0 \\
0 & 1 & -\frac{2}{5} - \frac{4}{5}i & \frac{1}{5} + \frac{2}{5}i
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{1 - 2i}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
1 & 0 & \frac{1}{5} + \frac{2}{5}i & \frac{2}{5} - \frac{1}{5}i \\
0 & 1 & -\frac{2}{5} - \frac{4}{5}i & \frac{1}{5} + \frac{2}{5}i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - iF_{2}
\end{align}
$$
La matriz inversa de $\begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$ es $\begin{pmatrix} \frac{1}{5} + \frac{2}{5}i & \frac{2}{5} - \frac{1}{5}i \\ -\frac{2}{5} - \frac{4}{5}i & \frac{1}{5} + \frac{2}{5}i \end{pmatrix}$
### Parte i)
$$
\left(
\begin{array}{ccc|ccc}
3 & 6 & 9 & 1 & 0 & 0 \\
2i & 4 & 6 & 0 & 1 & 0 \\
1 + i & 2 & 3 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
3 & 6 & 9 & 1 & 0 & 0 \\
-2 & 0 & 0 & 0 & 1 & -2 \\
1 + i & 2 & 3 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
3 & 6 & 9 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 & -\frac{1}{2} & 1 \\
1 + i & 2 & 3 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{-2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 0 & -\frac{1}{2} & 1 \\
3 & 6 & 9 & 1 & 0 & 0 \\
1 + i & 2 & 3 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \longleftrightarrow F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 0 & -\frac{1}{2} & 1 \\
0 & 6 & 9 & 1 & \frac{3}{2} & -3 \\
0 & 2 & 3 & 0 & \frac{1}{2} + \frac{1}{2}i & i
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 3F_{1} \\
&F_{3} \leftarrow F_{3} - (1 + i)F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 0 & -\frac{1}{2} & 1 \\
0 & 6 & 9 & 1 & \frac{3}{2} & -3 \\
0 & 0 & 0 & -3 & \frac{3}{2}i & -3 + 3i
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow 3F_{3} - F_{2}
\end{align}
$$
Como llegué a anular una ecuación (pero con una incoherencia), sabemos que la matriz $\left( \begin{array}{ccc} 3 & 6 & 9 \\ 2i & 4 & 6 \\ 1 + i & 2 & 3 1 \end{array} \right)$ no es invertible.

## Ejercicio 1.2
### Parte a)
$$
A = \left(
\begin{array}{cc}
2 & -2 \\
-1 & 3
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|cc}
2 & -2 & 1 & 0 \\
-1 & 3 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|cc}
2 & -2 & 1 & 0 \\
0 & 4 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow 2F_{2} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
2 & -2 & 1 & 0 \\
0 & 1 & \frac{1}{4} & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{4}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
2 & 0 & \frac{3}{2} & 1 \\
0 & 1 & \frac{1}{4} & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
1 & 0 & \frac{3}{4} & \frac{1}{2} \\
0 & 1 & \frac{1}{4} & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{2}
\end{align}
$$
La matriz inversa de $\begin{pmatrix} 2 & -2 \\ -1 & 3 \end{pmatrix}$ es $\begin{pmatrix} \frac{3}{4} & \frac{1}{2} \\ \frac{1}{4} & \frac{1}{2} \end{pmatrix}$

$$
B = \left(
\begin{array}{cc}
6 & -2 & -3 \\
-1 & 1 & 0 \\
-1 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
6 & -2 & -3 & 1 & 0 & 0 \\
-1 & 1 & 0 & 0 & 1 & 0 \\
-1 & 0 & 1 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
4 & 0 & -3 & 1 & 2 & 0 \\
-1 & 1 & 0 & 0 & 1 & 0 \\
-1 & 0 & 1 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 2 & 3 \\
-1 & 1 & 0 & 0 & 1 & 0 \\
-1 & 0 & 1 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 3F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 2 & 3 \\
0 & 1 & 0 & 1 & 3 & 3 \\
0 & 0 & 1 & 1 & 2 & 4
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
La matriz inversa de $\begin{pmatrix} 6 & -2 & -3 \\ -1 & 1 & 0 \\ -1 & 0 & 1 \end{pmatrix}$ es $\begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 3 \\ 1 & 2 & 4 \end{pmatrix}$

$$
C = \left(
\begin{array}{cc}
1 + i & 2 \\
-i & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|cc}
1 + i & 2 & 1 & 0 \\
-i & 1 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|cc}
1 + 3i & 0 & 1 & -2 \\
-i & 1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
1 & 0 & \frac{1}{10} - \frac{3}{10}i & -\frac{1}{5} + \frac{3}{5}i \\
-i & 1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{1 + 3i}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
1 & 0 & \frac{1}{10} - \frac{3}{10}i & -\frac{1}{5} + \frac{3}{5}i \\
0 & 1 & \frac{3}{10} + \frac{1}{10}i & \frac{2}{5} - \frac{1}{5}i
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + iF_{1}
\end{align}
$$
La matriz inversa de $\begin{pmatrix} 1 + i & 2 \\ -i & 1 \end{pmatrix}$ es $\begin{pmatrix} \frac{1}{10} - \frac{3}{10}i & -\frac{1}{5} + \frac{3}{5}i \\ \frac{3}{10} + \frac{1}{10}i & \frac{2}{5} - \frac{1}{5}i \end{pmatrix}$

### Parte b)
$$
\begin{align}
&A = \left(
\begin{array}{cc}
2 & -2 \\
-1 & 3
\end{array}
\right) \\

&A \begin{pmatrix}
x \\
y
\end{pmatrix} = 
\begin{pmatrix}
1 \\
1
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
&A \begin{pmatrix}
x \\
y
\end{pmatrix} =  \\
 \\
&\begin{pmatrix}
x \\
y
\end{pmatrix} \\

\left(
\begin{array}{cc}
2 & -2 \\
-1 & 3
\end{array}
\right)

&\begin{pmatrix}
2x - 2y \\
-x + 3y
\end{pmatrix}
\end{align}
$$
$$
\implies \begin{pmatrix}
2x - 2y \\
-x + 3y
\end{pmatrix} = \begin{pmatrix}
1 \\
1
\end{pmatrix}
$$
$$
\begin{cases}
2x - 2y = 1 \\
-x + 3y = 1
\end{cases}
$$
$$
\left(
\begin{array}{cc|c}
2 & -2 & 1 \\
-1 & 3 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|c}
2 & -2 & 1 \\
0 & 2 & \frac{3}{2}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + \frac{1}{2}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
2 & -2 & 1 \\
0 & 1 & \frac{3}{4}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{2}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
2 & 0 & \frac{5}{2} \\
0 & 1 & \frac{3}{4}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
1 & 0 & \frac{5}{4} \\
0 & 1 & \frac{3}{4}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{2}F_{1}
\end{align}
$$
En conclusión, $x = \frac{5}{4}$ y $y = \frac{3}{4}$.

En realidad, la idea de la segunda parte del ejercicio es utilizar las matrices inversas calculadas en la parte a para resolver los sistemas de ecuaciones lineales, sabiendo que:
$$
A \begin{pmatrix}
x \\
y
\end{pmatrix} = 
\begin{pmatrix}
1 \\
1
\end{pmatrix}

\Longleftrightarrow

\begin{pmatrix}
x \\
y
\end{pmatrix} = A^{-1} \begin{pmatrix}
1 \\
1
\end{pmatrix}
$$
Desde ahora en más, aplicaremos esta idea para resolver el resto de puntos.
$$
\begin{align}
&B = \left(
\begin{array}{ccc}
6 & -2 & -3 \\
-1 & 1 & 0 \\
-1 & 0 & 1
\end{array}
\right) \\

&B^{-1} = \left(
\begin{array}{ccc}
1 & 2 & 3 \\
1 & 3 & 3 \\
1 & 2 & 4
\end{array}
\right) \\
 \\

&B \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = 
\begin{pmatrix}
4 \\
1 \\
0
\end{pmatrix} \Longleftrightarrow \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = B^{-1} \begin{pmatrix}
4 \\
1 \\
0
\end{pmatrix}
\end{align}
$$
De esta forma, calcularemos el producto de matrices
$$
\begin{align}
&B^{-1} \begin{pmatrix}
4 \\
1 \\
0
\end{pmatrix} \\
 \\

&\begin{pmatrix}
4 \\
1 \\
0
\end{pmatrix} \\

\left(
\begin{array}{ccc}
1 & 2 & 3 \\
1 & 3 & 3 \\
1 & 2 & 4
\end{array}
\right)

&\begin{pmatrix}
1 \times 4 + 2 \times 1 + 3 \times 0 \\
1 \times 4 + 3 \times 1 + 3 \times 0 \\
1 \times 4 + 2 \times 1 + 4 \times 0
\end{pmatrix} \\

&\begin{pmatrix}
4 + 2 + 0 \\
4 + 3 + 0 \\
4 + 2 + 0
\end{pmatrix} \\

&\begin{pmatrix}
6 \\
7 \\
6
\end{pmatrix} \\
 \\

&\begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = B^{-1} \begin{pmatrix}
4 \\
1 \\
0
\end{pmatrix} = \begin{pmatrix}
6 \\
7 \\
6
\end{pmatrix}
\end{align}
$$
En conclusión, $x = 6$, $y = 7$ y $z = 6$.

$$
\begin{align}
&C = \left(
\begin{array}{cc}
1 + i & 2 \\
-i & 1
\end{array}
\right) \\

&C^{-1} = \left(
\begin{array}{ccc}
\frac{1}{10} - \frac{3}{10}i & -\frac{1}{5} + \frac{3}{5}i \\
\frac{3}{10} + \frac{1}{10}i & \frac{2}{5} - \frac{1}{5}i
\end{array}
\right) \\
 \\

&C \begin{pmatrix}
x \\
y
\end{pmatrix} = 
\begin{pmatrix}
1 \\
2
\end{pmatrix} \Longleftrightarrow \begin{pmatrix}
x \\
y
\end{pmatrix} = C^{-1} \begin{pmatrix}
1 \\
2
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
&C^{-1} \begin{pmatrix}
1 \\
2
\end{pmatrix} \\
 \\

&\begin{pmatrix}
1 \\
2
\end{pmatrix} \\

\left(
\begin{array}{ccc}
\frac{1}{10} - \frac{3}{10}i & -\frac{1}{5} + \frac{3}{5}i \\
\frac{3}{10} + \frac{1}{10}i & \frac{2}{5} - \frac{1}{5}i
\end{array}
\right)

&\begin{pmatrix}
\left( \frac{1}{10} - \frac{3}{10}i \right) \times 1 + \left( -\frac{1}{5} + \frac{3}{5}i \right) \times 2 \\
\left( \frac{3}{10} + \frac{1}{10}i \right) \times 1 + \left( \frac{2}{5} - \frac{1}{5}i \right) \times 2
\end{pmatrix} \\

&\begin{pmatrix}
\frac{1}{10} - \frac{3}{10}i - \frac{2}{5} + \frac{6}{5}i \\
\frac{3}{10} + \frac{1}{10}i + \frac{4}{5} - \frac{2}{5}i
\end{pmatrix} \\

&\begin{pmatrix}
-\frac{3}{10} + \frac{9}{10}i \\
\frac{11}{10} - \frac{3}{10}i
\end{pmatrix} \\
 \\

&\begin{pmatrix}
x \\
y
\end{pmatrix} = C^{-1} \begin{pmatrix}
1 \\
2
\end{pmatrix} = \begin{pmatrix}
-\frac{3}{10} + \frac{9}{10}i \\
\frac{11}{10} - \frac{3}{10}i
\end{pmatrix}
\end{align}
$$
En conclusión, $x = -\frac{3}{10} + \frac{9}{10}i$ y $y = \frac{11}{10} - \frac{3}{10}i$

## Ejercicio 1.3
### Parte a)
$$
\begin{align}
&A = \left(
\begin{array}{cccc}
k_{1} & 0 & 0 & 0 \\
0 & k_{2} & 0 & 0 \\
0 & 0 & k_{3} & 0 \\
0 & 0 & 0 & k_{4} 
\end{array}
\right) \\
&A^{-1} = \text{?}
\end{align}
$$
### Parte a)
$$
\left(
\begin{array}{cccc|cccc}
k_{1} & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\
0 & k_{2} & 0 & 0 & 0 & 1 & 0 & 0 \\
0 & 0 & k_{3} & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & k_{4} & 0 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{k_{1}} & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & 0 & \frac{1}{k_{2}} & 0 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 & \frac{1}{k_{3}} & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & \frac{1}{k_{4}}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{k_{1}} \\
&F_{2} \leftarrow \frac{F_{2}}{k_{2}} \\
&F_{3} \leftarrow \frac{F_{3}}{k_{3}} \\
&F_{4} \leftarrow \frac{F_{4}}{k_{4}}
\end{align}
$$
De esta forma, la matriz inversa de $\left(\begin{array}{cccc} k_{1} & 0 & 0 & 0 \\ 0 & k_{2} & 0 & 0 \\ 0 & 0 & k_{3} & 0 \\ 0 & 0 & 0 & k_{4} \end{array} \right)$ es $\left(\begin{array}{cccc} \frac{1}{k_{1}} & 0 & 0 & 0 \\ 0 & \frac{1}{k_{2}} & 0 & 0 \\ 0 & 0 & \frac{1}{k_{3}} & 0 \\ 0 & 0 & 0 & \frac{1}{k_{4}} \end{array} \right)$

### Parte c)
$$
\begin{align}
&C = \left(
\begin{array}{cccc}
k & 0 & 0 & 0 \\
1 & k & 0 & 0 \\
0 & 1 & k & 0 \\
0 & 0 & 1 & k
\end{array}
\right) \\
&C^{-1} = \text{?}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
k & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\
1 & k & 0 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 & k & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & k & 0 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{k} & 0 & 0 & 0 \\
1 & k & 0 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 & k & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & k & 0 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{k}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{k} & 0 & 0 & 0 \\
0 & k & 0 & 0 & -\frac{1}{k} & 1 & 0 & 0 \\
0 & 1 & k & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & k & 0 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{k} & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & -\frac{1}{k^{2}} & \frac{1}{k} & 0 & 0 \\
0 & 1 & k & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & k & 0 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{k}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{k} & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & -\frac{1}{k^{2}} & \frac{1}{k} & 0 & 0 \\
0 & 0 & k & 0 & \frac{1}{k^{2}} & -\frac{1}{k} & 1 & 0 \\
0 & 0 & 1 & k & 0 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{k} & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & -\frac{1}{k^{2}} & \frac{1}{k} & 0 & 0 \\
0 & 0 & 1 & 0 & \frac{1}{k^{3}} & -\frac{1}{k^{2}} & \frac{1}{k} & 0 \\
0 & 0 & 1 & k & 0 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{F_{3}}{k}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{k} & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & -\frac{1}{k^{2}} & \frac{1}{k} & 0 & 0 \\
0 & 0 & 1 & 0 & \frac{1}{k^{3}} & -\frac{1}{k^{2}} & \frac{1}{k} & 0 \\
0 & 0 & 0 & k & -\frac{1}{k^{3}} & \frac{1}{k^{2}} & -\frac{1}{k} & 1
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{k} & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & -\frac{1}{k^{2}} & \frac{1}{k} & 0 & 0 \\
0 & 0 & 1 & 0 & \frac{1}{k^{3}} & -\frac{1}{k^{2}} & \frac{1}{k} & 0 \\
0 & 0 & 0 & 1 & -\frac{1}{k^{4}} & \frac{1}{k^{3}} & -\frac{1}{k^{2}} & \frac{1}{k}
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow \frac{F_{4}}{k}
\end{align}
$$
De esta forma, la matriz inversa de $\left(\begin{array}{cccc} k & 0 & 0 & 0 \\ 1 & k & 0 & 0 \\ 0 & 1 & k & 0 \\ 0 & 0 & 1 & k \end{array} \right)$ es $\left(\begin{array}{cccc} \frac{1}{k} & 0 & 0 & 0 \\ -\frac{1}{k^{2}} & \frac{1}{k} & 0 & 0 \\ \frac{1}{k^{3}} & -\frac{1}{k^{2}} & \frac{1}{k} & 0 \\ -\frac{1}{k^{4}} & \frac{1}{k^{3}} & -\frac{1}{k^{2}} & \frac{1}{k} \end{array} \right)$

## Ejercicio 1.4
### Parte a)
$$
\begin{align}
&A = \left(
\begin{array}{cc}
1 & 0 \\
3 & 4
\end{array}
\right) \\
 \\

&E_{2}E_{1}A = I \\

&E_{1} = \text{?} \\
&E_{2} = \text{?}
\end{align}
$$
Para esto, hacemos el proceso de encontrar la inversa, ya que cada paso que realizamos para acercarnos a la inversa, no deja una matriz elemental.
$$
\begin{align}
&A^{-1} =  \\
 \\
&\left(
\begin{array}{cc|cc}
1 & 0 & 1 & 0 \\
3 & 4 & 0 & 1
\end{array}
\right)
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
1 & 0 & 1 & 0 \\
0 & 4 & -3 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 3F_{1}
\end{align}
$$
De esta forma, tenemos la primera matriz elemental $E_{1}$: $\left( \begin{array}{cc|cc} 1 & 0 \\ -3 & 1 \end{array} \right)$
Si realizamos la operación $E_{1}A$, obtenemos $\begin{pmatrix} 1 & 0 \\ 0 & 4 \end{pmatrix}$ (la matriz obtenida luego de aplicar la operación $F_{2} \leftarrow F_{2} - 3F_{1}$, por lo tanto podría decirse que la matriz $E_{1}$ equivale a dicha operación).

Proseguimos a buscar la matriz elemental $E_{2}$:
$$
\left(
\begin{array}{cc|cc}
1 & 0 & 1 & 0 \\
0 & 1 & -\frac{3}{4} & \frac{1}{4}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{4}F_{2}
\end{align}
$$
Es así que obtenemos la segunda matriz elemental $E_{2}$: $\left( \begin{array}{cc|cc} 1 & 0 \\ 0 & \frac{1}{4} \end{array} \right)$
Quitamos el $-\frac{3}{4}$, ya que estaba dado por la primera operación correspondiente a la matriz $E_{1}$.
Es una matriz elemental, ya que:
$$
\begin{align}
&E_{2} \begin{pmatrix}
1 & 0 \\
0 & 4
\end{pmatrix} = \\
 \\
&\begin{pmatrix}
1 & 0 \\
0 & 4
\end{pmatrix} \\

\begin{pmatrix}
1 & 0 \\
0 & \frac{1}{4}
\end{pmatrix}

&\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \\
\end{align}
$$
De esta forma, si proseguimos con la operación:
$$
\begin{align}
&E_{2}E_{1}A = \text{?} \\
 \\
&E_{2}E_{1} = \\
 \\
&\begin{pmatrix}
1 & 0 \\
-3 & 1
\end{pmatrix} \\

\begin{pmatrix}
1 & 0 \\
0 & \frac{1}{4}
\end{pmatrix}

&\begin{pmatrix}
1 & 0 \\
-\frac{3}{4} & \frac{1}{4}
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
&E_{2}E_{1}A = \\
 \\
&\begin{pmatrix}
1 & 0 \\
3 & 4
\end{pmatrix} \\

\begin{pmatrix}
1 & 0 \\
-\frac{3}{4} & \frac{1}{4}
\end{pmatrix}

&\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
\end{align}
$$
De esta forma, las matrices elementales $E_{1}$ y $E_{2}$ que cumplen que $E_{2}E_{1}A = I$ son:
$$
\begin{align}
&E_{1} = \begin{pmatrix}
1 & 0 \\
-3 & 1
\end{pmatrix} \\
 \\
&E_{2} = \begin{pmatrix}
1 & 0 \\
0 & \frac{1}{4}
\end{pmatrix}
\end{align}
$$
### Parte b)
La matriz inversa de A es igual a:
$$
\begin{align}
&E_{2}E_{1}A = I \implies E_{2}E_{1} = A^{-1} \\
 \\
&E_{2}E_{1} = \\
 \\
&\begin{pmatrix}
1 & 0 \\
-3 & 1
\end{pmatrix} \\

\begin{pmatrix}
1 & 0 \\
0 & \frac{1}{4}
\end{pmatrix}

&\begin{pmatrix}
1 & 0 \\
-\frac{3}{4} & \frac{1}{4}
\end{pmatrix}

\end{align}
$$
De esta forma, la matriz inversa de A es:
$$
A^{-1} = E_{2}E_{1} = \begin{pmatrix}
1 & 0 \\
-\frac{3}{4} & \frac{1}{4}
\end{pmatrix}
$$
### Parte c)
Para expresar A como el producto de matrices elementales, podemos considerar las propiedades del inverso:
$$
A^{-1} = E_{2}E_{1} \implies A = (A^{-1})^{-1} = (E_{2}E_{1})^{-1} = E_{1}^{-1}E_{2}^{-1}
$$
Ahora, según las operaciones que nos permitieron obtener $E_{1}$ y $E_{2}$ es que deduciremos sus inversas:
$$
\begin{align}
&F_{2} \leftarrow F_{2} - 3F_{1} \rightarrow E_{1} = \left( \begin{array}{cc|cc} 1 & 0 \\ -3 & 1 \end{array} \right) \\
&\implies F_{2} \leftarrow F_{2} + 3F_{1} \rightarrow E_{1}^{-1} = \left( \begin{array}{cc|cc} 1 & 0 \\ 3 & 1 \end{array} \right)
\end{align}
$$
ACLARACIÓN: LAS OPERACIONES SIEMPRE SE REALIZAN SOBRE LA MATRIZ IDENTIDAD DEL TAMAÑO CORRESPONDIENTE. TODAS LAS MATRICES ELEMENTALES SURGEN DE APLICAR UNA OPERACIÓN DETERMINADA A LA MATRIZ ELEMENTAL.
$$
\begin{align}
&F_{2} \leftarrow \frac{1}{4}F_{2} \rightarrow E_{2} = \left( \begin{array}{cc|cc} 1 & 0 \\ 0 & \frac{1}{4} \end{array} \right) \\
&\implies F_{2} \leftarrow 4F_{2} \rightarrow E_{2}^{-1} = \left( \begin{array}{cc|cc} 1 & 0 \\ 0 & 4 \end{array} \right)
\end{align}
$$
De esta forma:
$$
\begin{align}
&E_{1}^{-1} = \left( \begin{array}{cc|cc} 1 & 0 \\ 3 & 1 \end{array} \right) \\
&E_{2}^{-1} = \left( \begin{array}{cc|cc} 1 & 0 \\ 0 & 4 \end{array} \right) \\
&E_{1}^{-1}E_{2}^{-1} = \\
 \\
&\left( \begin{array}{cc|cc}
1 & 0 \\
0 & 4
\end{array}
\right) \\

\left( \begin{array}{cc|cc}
1 & 0 \\
3 & 1
\end{array}
\right)

&\left( \begin{array}{cc|cc}
1 & 0 \\
3 & 4
\end{array}
\right) \\
 \\
&E_{1}^{-1}E_{2}^{-1} = \left( \begin{array}{cc|cc}
1 & 0 \\
3 & 4
\end{array}
\right) = A
\end{align}
$$

## Ejercicio 1.5
### $E_{1}$
$$
\begin{align}
E_{1}A = B \implies E_{1} = BA^{-1}
\end{align}
$$
$$
\begin{align}
&A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix} \\
&A^{-1} = \text{?}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 2 & 3 & 1 & 0 & 0 \\
4 & 5 & 6 & 0 & 1 & 0 \\
7 & 8 & 9 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 2 & 3 & 1 & 0 & 0 \\
0 & -3 & -6 & -4 & 1 & 0 \\
0 & -6 & -12 & -7 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 4F_{1} \\
&F_{3} \leftarrow F_{3} - 7F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 2 & 3 & 1 & 0 & 0 \\
0 & -3 & -6 & -4 & 1 & 0 \\
0 & 0 & 0 & 1 & -1 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - 2F_{2}
\end{align}
$$
La matriz $A^{-1}$ no se puede invertir. Tenemos que buscar otro método.
Si analizamos las matrices A y B, vemos que simplemente tienen las filas 1 y 3 invertidas. De esta forma, la matriz elemental $E_{1}$ tiene que tener las filas 1 y 3 invertidas:
$$
E_{1} = \begin{pmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{pmatrix}
$$
De esta forma:
$$
\begin{align}
&E_{1}A = \\
 \\
&\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix} \\

\begin{pmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{pmatrix}

&\begin{pmatrix}
7 & 8 & 9 \\
4 & 5 & 6 \\
1 & 2 & 3
\end{pmatrix} \\
 \\

&E_{1}A = \begin{pmatrix}
7 & 8 & 9 \\
4 & 5 & 6 \\
1 & 2 & 3
\end{pmatrix} = B
\end{align}
$$

### $E_{2}$
Si analizamos las matrices A y B, vemos que simplemente tienen las filas 1 y 3 invertidas. De esta forma, la matriz elemental $E_{2}$ tiene que tener las filas 1 y 3 invertidas:
$$
E_{2} = \begin{pmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{pmatrix}
$$
De esta forma:
$$
\begin{align}
&E_{2}B = \\
 \\
&\begin{pmatrix}
7 & 8 & 9 \\
4 & 5 & 6 \\
1 & 2 & 3
\end{pmatrix} \\

\begin{pmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{pmatrix}

&\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix} \\
 \\

&E_{2}B = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix} = A
\end{align}
$$

### $E_{3}$
Si comparamos las matrices A y C, vemos que la diferencia es que la fila tres de C es igual a $F_{3} + 2F_{1}$ de la matriz A:
$$
E_{3} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
2 & 0 & 1
\end{pmatrix}
$$
De esta forma:
$$
\begin{align}
&E_{3}A = \\
 \\
&\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix} \\

\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
2 & 0 & 1
\end{pmatrix}

&\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
9 & 12 & 15
\end{pmatrix} \\
 \\

&E_{3}A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
9 & 12 & 15
\end{pmatrix} = C
\end{align}
$$

### $E_{4}$
Si comparamos las matrices C y A, vemos que la diferencia es que la fila tres de A es igual a $F_{3} - 2F_{1}$ de la matriz C:
$$
E_{4} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
-2 & 0 & 1
\end{pmatrix}
$$
De esta forma:
$$
\begin{align}
&E_{4}C = \\
 \\
&\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
9 & 12 & 15
\end{pmatrix} \\

\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
-2 & 0 & 1
\end{pmatrix}

&\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix} \\
 \\

&E_{4}C = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix} = A
\end{align}
$$

## Ejercicio 1.6
### Parte a)
Para verificarlo, debemos hacer lo siguiente:
$$
\begin{align}
&(\alpha AB)^{-1} = \frac{1}{\alpha}B^{-1}A^{-1} \implies \alpha AB \cdot \frac{1}{\alpha}B^{-1}A^{-1} = I \\
&\alpha AB \cdot \frac{1}{\alpha}B^{-1}A^{-1} = \cancel{ \alpha \frac{1}{\alpha} } \cancel{ A A^{-1} } \cancel{ B B^{-1} } = I
\end{align}
$$
Efectivamente, $(\alpha AB)^{-1} = \frac{1}{\alpha}B^{-1}A^{-1}$, por lo que la afirmación es verdadera.

### Parte b)
Si A es invertible, entonces $(A^{T})^{-1} = (A^{-1})^{T}$.
Para verificarlo, debemos hacer lo siguiente:
$$
\begin{align}
&(A^{T})^{-1} = (A^{-1})^{T} \implies A^{T} \cdot (A^{-1})^{T} = I \\
&A^{T} \cdot (A^{-1})^{T} = (A^{-1}A)^{T} = I
\end{align}
$$
Efectivamente, $(A^{T})^{-1} = (A^{-1})^{T}$, por lo que la afirmación es verdadera.

### Parte c)
La afirmación es falsa, y lo demostraremos con un simple ejemplo:
$$
\begin{align}
&A = \begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 0 \\
0 & 1 & 1
\end{pmatrix}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 1 & 1 & 0 & 0 \\
0 & 1 & 0 & 0 & 1 & 0 \\
0 & 1 & 1 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 1 & 1 & 0 & 0 \\
0 & 1 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & -1 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 1 & -1 \\
0 & 1 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & -1 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3}
\end{align}
$$
Como vemos, A se puede invertir. De esta forma, sabemos que $-A$ también es invertible, por lo que consideraremos $B = -A$. De esta forma:
$$
A + B = O
$$
Es así que confirmamos que la afirmación es falsa.

### Parte d)
Para verificarlo, debemos hacer lo siguiente:
$$
\begin{align}
&(A + B)^{-1} = A^{-1} + B^{-1} \implies (A + B) \cdot (A^{-1} + B^{-1}) = I \\
&(A + B) \cdot (A^{-1} + B^{-1}) = \cancelto{ I }{ AA^{-1} } + AB^{-1} + BA^{-1} + \cancelto{ I }{ BB^{-1} } = AB^{-1} + BA^{-1} + 2I \neq I
\end{align}
$$
Como vemos, $(A + B)^{-1} \neq A^{-1} + B^{-1}$, por lo que la afirmación es falsa.

### Parte e)
Si B fuera invertible,  por la parte a), entonces AB debería ser invertible, y $(AB)^{-1} = B^{-1}A^{-1}$. Por esta razón, la afirmación es falsa.

# 2 - Rango de Matrices
## Ejercicio 2.1
El rango de una matriz equivale a la cantidad de ecuaciones no nulas de la matriz, luego de ser escalerizada.
### Parte a)
#### Matriz a)
$$
\left(
\begin{array}{cc|cc}
1 & 0 & 3 & 5 \\
0 & 1 & -2 & -3
\end{array}
\right)
$$
En la forma escalerizada, vemos que el rango de la matriz es 2 (pues tiene dos ecuaciones no nulas). En este caso, como ninguna ecuación se anula, el rango equivale a la cantidad de filas (m).

#### Matriz e)
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & -1 & -1 & 2 \\
0 & 1 & 0 & 3 & 2 & -4 \\
0 & 0 & 1 & -\frac{1}{2} & 0 & \frac{1}{2}
\end{array}
\right)
$$
En este caso, como ninguna ecuación se anula, el rango es 3, siendo equivalente a la cantidad de filas (m).

#### Matriz h)
$$
\left(
\begin{array}{cc|cc}
1 & 0 & \frac{1}{5} + \frac{2}{5}i & \frac{2}{5} - \frac{1}{5}i \\
0 & 1 & -\frac{2}{5} - \frac{4}{5}i & \frac{1}{5} + \frac{2}{5}i
\end{array}
\right)
$$
En este caso, como ninguna ecuación se anula, el rango es 2, siendo equivalente a la cantidad de filas (m).

#### Matriz i)
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 0 & -\frac{1}{2} & 1 \\
0 & 6 & 9 & 1 & \frac{3}{2} & -3 \\
0 & 0 & 0 & -3 & \frac{3}{2}i & -3 + 3i
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow 3F_{3} - F_{2}
\end{align}
$$
A diferencia de los casos anteriores, aquí logramos anular una ecuación, por lo que el rango no equivale a la cantidad de filas (m). En este caso, el rango es 2 (siendo $m = 3$).

### Parte b)
#### Matriz a)
$$
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix}
$$
$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & -6 & -12
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow F_{2} - 4F_{1} \\
&F_{3} \leftarrow F_{2} - 7F_{1}
\end{align}
$$
$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{3} \leftarrow F_{3} - 2F_{2}
\end{align}
$$
$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow -\frac{1}{3}F_{2}
\end{align}
$$
$$
\begin{pmatrix}
1 & 0 & -1 \\
0 & 1 & 2 \\
0 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{2}
\end{align}
$$
Como vemos, logramos llegar a la matriz escalerizada reducida, anulando una ecuación. De esta manera, el rango de la matriz es 2, siendo $m = 3$ (cantidad de filas).

#### Matriz d)
$$
\begin{pmatrix}
1 & 2 & 3 & 4 \\
5 & 6 & 7 & 8 \\
9 & 10 & 11 & 12 \\
13 & 14 & 15 & 16
\end{pmatrix}
$$
$$
\begin{pmatrix}
1 & 2 & 3 & 4 \\
0 & -4 & -8 & -12 \\
0 & -8 & -16 & -24 \\
0 & -12 & -24 & -36
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow F_{2} - 5F_{1} \\
&F_{3} \leftarrow F_{3} - 9F_{1} \\
&F_{4} \leftarrow F_{4} - 13F_{1}
\end{align}
$$
$$
\begin{pmatrix}
1 & 2 & 3 & 4 \\
0 & 1 & 2 & 3 \\
0 & -8 & -16 & -24 \\
0 & -12 & -24 & -36
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow -\frac{1}{4}F_{2}
\end{align}
$$
$$
\begin{pmatrix}
1 & 2 & 3 & 4 \\
0 & 1 & 2 & 3 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{3} \leftarrow F_{3} + 8F_{2} \\
&F_{4} \leftarrow F_{4} + 12F_{2}
\end{align}
$$
$$
\begin{pmatrix}
1 & 0 & -1 & -2 \\
0 & 1 & 2 & 3 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{2}
\end{align}
$$
Como vemos, logramos llegar a la matriz escalerizada reducida, anulando una ecuación. De esta manera, el rango de la matriz es 2, siendo $m = 4$ (cantidad de filas).

## Ejercicio 2.2
### Parte a)
$$
A = \begin{pmatrix}
1 & a & -2 \\
2 & 3a - 1 & a^{2} - a - 4 \\
a & a^{2} & a^{2} - 2a - 1
\end{pmatrix}
$$
$$
\begin{pmatrix}
1 & a & -2 \\
0 & a - 1 & a^{2} - a \\
0 & 0 & a^{2} - 1
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1} \\
&F_{3} \leftarrow F_{3} - aF_{1}
\end{align}
$$
$$
\begin{pmatrix}
1 & a & -2 \\
0 & a - 1 & a^{2} - a \\
0 & 0 & a^{2} - 1
\end{pmatrix}
$$
La matriz ya está en su forma escalerizada, por lo que podemos determinar los diferentes casos según los valores de $a$:
1. $a = 1$
$$
\begin{pmatrix}
1 & 1 & -2 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}
$$
En este caso, el rango es 1, pues las filas 2 y 3 se anulan.
2. $a = -1$
$$
\begin{pmatrix}
1 & -1 & -2 \\
0 & -2 & 2 \\
0 & 0 & 0
\end{pmatrix}
$$
En este caso, el rango es 2, pues las fila 3 se anulan.
3. $a \neq \pm 1$
En este último caso, el rango de la matriz es 3, ya que ninguna fila llega a anularse.

## Ejercicio 2.3
### Parte a)
Es verdadero, ya que como el rango equivale a la cantidad de filas no nulas de la matriz escalerizada, como máximo puede ser igual a la cantidad de filas (m), de forma que el rango es menor o igual a la cantidad de filas.

### Parte b)
Es falso, ya que el rango no tiene porque ser igual a m ni a n. Es verdad que siempre es menor o igual a m, pero nada más allá de eso.

### Parte c)
Es falso, en realidad el sistema es incompatible cuando $rango(A) \neq rango(A|b)$.

### Parte d)
Esto es verdadero, ya que si $rango(A) = rango(A|b)$, esto significa que la matriz es compatible. Además, si dichos valores son menores que n (cantidad de columnas de la matriz)

### Parte e)
Esto es falso, y lo demostramos con el siguiente ejemplo:
$$
A = \begin{pmatrix}
-2 & 0 \\
0 & -2
\end{pmatrix} \implies A^{-1} = \text{?}
$$
$$
\left(
\begin{array}{cc|cc}
-2 & 0 & 1 & 0 \\
0 & -2 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|cc}
1 & 0 & -\frac{1}{2} & 0 \\
0 & 1 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow -\frac{1}{2}F_{1} \\
&F_{2} \leftarrow -\frac{1}{2}F_{2}
\end{align}
$$
Como vemos, A es invertible. De este modo calculemos $A + 2Id$:
$$
A + 2Id = \begin{pmatrix}
-2 & 0 \\
0 & -2
\end{pmatrix} + \begin{pmatrix}
2 & 0 \\
0 & 2
\end{pmatrix} = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix} = B
$$
Como vemos $B = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$, por lo tanto B no es invertible.
De esta forma, el enunciado es falso.
