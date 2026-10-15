# Ejercicio 1
Sea el sistema
$$
{\begin{cases}
x + y + z = 0 \\
2x + \lambda y + z = 1 \\
-x + y + \lambda z = 2
\end{cases}}
$$
con $\lambda \in \mathbb{R}$.

$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
2 & \lambda & 1 & 1 \\
-1 & 1 & \lambda & 2
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
0 & \lambda - 2 & -1 & 1 \\
0 & 2 & \lambda + 1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
0 & \lambda & \lambda & 1 \\
0 & 2 & \lambda + 1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
0 & 1 & 1 & \frac{1}{\lambda} \\
0 & 2 & \lambda + 1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{\lambda}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -\frac{1}{\lambda} \\
0 & 1 & 1 & \frac{1}{\lambda} \\
0 & 2 & \lambda + 1 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -\frac{1}{\lambda} \\
0 & 1 & 1 & \frac{1}{\lambda} \\
0 & 0 & \lambda - 1 & 2 - \frac{2}{\lambda}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -\frac{1}{\lambda} \\
0 & 1 & 1 & \frac{1}{\lambda} \\
0 & 0 & 1 & \frac{2\lambda - 2}{\lambda^{2} - \lambda}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{F_{3}}{\lambda - 1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -\frac{1}{\lambda} \\
0 & 1 & 0 & \frac{-\lambda - 3}{\lambda^{2} - \lambda} \\
0 & 0 & 1 & \frac{2\lambda - 2}{\lambda^{2} - \lambda}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
$$
Sol(S) = \left\{  \left( -\frac{1}{\lambda}, \frac{-\lambda - 3}{\lambda^{2} - \lambda}, \frac{2\lambda - 2}{\lambda^{2} - \lambda}  \right)  \right\}
$$
$$
\left\{  \left( -\frac{1}{2}, \frac{-5}{2}, 1  \right)  \right\}
$$

# Ejercicio 2
$$
\left(
\begin{array}{ccc}
3 & -1 & -1 \\
-2 & 1 & 1 \\
-4 & 1 & 2
\end{array}
\right)^{-1} = \left(
\begin{array}{ccc}
x + z & y & y + z \\
y + z & x & z \\
x & y & y
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
3 & -1 & -1 & 1 & 0 & 0 \\
-2 & 1 & 1 & 0 & 1 & 0 \\
-4 & 1 & 2 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
3 & -1 & -1 & 1 & 0 & 0 \\
1 & 0 & 0 & 1 & 1 & 0 \\
-1 & 0 & 1 & 1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 1 & 0 \\
3 & -1 & -1 & 1 & 0 & 0 \\
-1 & 0 & 1 & 1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \longleftrightarrow F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 1 & 0 \\
2 & -1 & 0 & 2 & 0 & 1 \\
-1 & 0 & 1 & 1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 1 & 0 \\
0 & -1 & 0 & 0 & -2 & 1 \\
0 & 0 & 1 & 2 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 1 & 0 \\
0 & 1 & 0 & 0 & 2 & -1 \\
0 & 0 & 1 & 2 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
# Ejercicio 4
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 2 & 1 & 0 & 1 & 0 \\
0 & 1 & 1 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & 0 & 1 & -1 \\
0 & 1 & 1 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & 0 & 1 & -1 \\
0 & 0 & 1 & 0 & -1 & 2
\end{array}
\right)
\begin{align}
F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
La inversa de A es $$
\left(
\begin{array}{ccc}
1 & 0 & 0 \\
0 & 1 & -1 \\
0 & -1 & 2
\end{array}
\right)
$$
$$
\begin{align}
&A^{-1}v =  \\
 \\

&\left(
\begin{array}{c}
1 \\
0 \\
2
\end{array}
\right) \\

\left(
\begin{array}{ccc}
1 & 0 & 0 \\
0 & 1 & -1 \\
0 & -1 & 2
\end{array}
\right)

&\left(
\begin{array}{c}
1 \times 1 + 0 \times 0 + 0 \times 2 \\
0 \times 1 + 1 \times 0 + (-1) \times 2 \\
0 \times 1 + (-1) \times 0 + 2 \times 2
\end{array}
\right) \\

&\left(
\begin{array}{c}
1 + 0 + 0 \\
0 + 0 - 2 \\
0 + 0 + 4
\end{array}
\right) \\

&\left(
\begin{array}{c}
1 \\
-2 \\
4
\end{array}
\right) \\
 \\
&A^{-1}v = \left(
\begin{array}{c}
1 \\
-2 \\
4
\end{array}
\right)
\end{align}
$$