# Ejercicio 1
$$
\begin{cases}
x = - 4\lambda + 4\mu \\
y = -2 - 3\lambda + 5\mu \\
z = -2 + 2\mu
\end{cases}
$$
Lo expresamos con la ecuación vectorial:
$$
S := (0, -2, -2) + \lambda(-4, -3, 0) + \mu(4, 5, 2)
$$
Podemos ver que se trata de un plano que pasa por $(0, -2, -2)$ y tiene como vectores directores a $(-4, -3, 0)$ y $(4, 5, 2)$.

Primero, determinemos si el origen pertenece al conjunto:
$$
\begin{cases}
0 = -4\lambda + 4\mu \\
0 = -2 - 3\lambda + 5\mu \\
0 = -2 + 2\mu
\end{cases}
$$
$$
\begin{align}
0 &= -2 + 2\mu \\
2 &= 2\mu \\
1 &= \mu
\end{align}
$$
$$
\begin{align}
0 &= -2 - 3\lambda + 5\mu \\
0 &= -2 - 3\lambda + 5 \\
0 &= 3 - 3\lambda \\
-3 &= -3\lambda \\
\frac{-3}{-3} &= \lambda \\
1 &= \lambda
\end{align}
$$
$$
\begin{align}
0 = -4\lambda + 4\mu \\
0 = -4 + 4 \\
0 = 0
\end{align}
$$
Podemos ver que, efectivamente, $(0, 0, 0) \in S$.

Por un enunciado visto en clase, sabemos que todos los planos vectoriales (planos que pasan por el origen), son espacios vectoriales.

---
# Ejercicio 2
$$
U = \{ (1, 1, 3), (3, 5, 5), (2, 1, 8) \}
$$
Para determinar si $U$ es linealmente dependiente o no, tenemos dos formas de hacerlo:
- Ver si de alguna forma podemos obtener el vector nulo desarrollando una combinación lineal de los vectores anteriores (sin que todos los coeficientes sean nulos).
- Ver si algunos de los vectores de $U$ se puede escribir como combinación lineal del resto.

Lo que podemos hacer es desarrollar una matriz que incluya a los vectores como filas o columnas y calcular su determinante: en caso de ser 0, la matriz no es invertible, por lo que los vectores son linealmente dependientes. Esto se da ya que cuando el determinante es cero, quiere decir que:
- Una fila o columna es nula.
- Una fila o columna es múltiplo de otra.
- Una fila o columna es combinación lineal del resto.

$$
\begin{align}
\left|
\begin{array}{ccc}
1 & 1 & 3 \\
3 & 5 & 5 \\
2 & 1 & 8
\end{array}
\right| &= 1(40 - 5) - 3(8 - 3) + 2(5 - 15) \\
&= 1(35) - 3(5) + 2(-10) \\
&= 35 - 15 - 20 \\
&= 35 - 35 \\
&= 0
\end{align}
$$
De esta forma, confirmamos que la familia de vectores $U$ es linealmente dependiente.

---
# Ejercicio 3
Tenemos la familia de vectores $S = \{ (7, 4, 12, 3),(11, 13, 12, 9),(10, 8, 3, 13),(5, 4, 7, 2) \}$, y tenemos que determinar cuantas dimensiones tiene el espacio generado por dicho generador.

En caso de que $S$ sea una base (además de generador, también sea linealmente independiente), su dimensión será 4 por la definición de dimensión:
"La dimensión de un espacio vectorial está dada por la cantidad de elementos de todas sus bases (todas tienen la misma cantidad de elementos)".

Por lo tanto, desarrollaremos una matriz con dichos vectores e intentaremos escalerizarla. Si en el proceso no se anula ninguna fila, entonces la dimensión es 4. Si se anulan filas, la dimensión será equivalente a la cantidad de filas no nulas:
$$
\begin{pmatrix}
7 & 4 & 3 & 2 \\
11 & 13 & 12 & 9 \\
10 & 8 & 3 & 13 \\
5 & 4 & 7 & 2
\end{pmatrix}
$$
$$
\begin{pmatrix}
7 & 4 & 3 & 2 \\
0 & 13 & 12 & 9 \\
10 & 8 & 3 & 13 \\
5 & 4 & 7 & 2
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow 7F_{2} - 11F_{1} \\
&F_{3} \\
&F_{4}
\end{align}
$$

---
# Ejercicio 4
