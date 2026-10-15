# Ejercicio 1
Calcular el determinante:
$$
\left|
\begin{array}{cc}
a_{1,1} & a_{1,2} & a_{1,3} \\
a_{2,1} & a_{2,2} & a_{2,3} \\
a_{3,1} & a_{3,2} & a_{3,3}
\end{array}
\right|
$$
$$
\left|
\begin{array}{ccc}
a_{1,1} & a_{1,2} & a_{1,3} \\
a_{2,1} & a_{2,2} & a_{2,3} \\
a_{3,1} & a_{3,2} & a_{3,3}
\end{array}
\right| = a_{1,1} \left|
\begin{array}{cc}
a_{2,2} & a_{2,3} \\
a_{3,2} & a_{3,3}
\end{array}
\right| - a_{2,1} \left|
\begin{array}{cc}
a_{1,2} & a_{1,3} \\
a_{3,2} & a_{3,3}
\end{array}
\right| + a_{3,1} \left|
\begin{array}{cc}
a_{1,2} & a_{1,3} \\
a_{2,2} & a_{2,3}
\end{array}
\right|
$$
$$
= a_{1,1} \times (a_{2,2}a_{3,3} - a_{3,2} a_{2,3}) - a_{2,1} \times (a_{1,2}a_{3,3} - a_{3,2}a_{1,3}) + a_{3,1} \times (a_{1,2}a_{2,3} - a_{2,2}a_{1,3})
$$
$$
= a_{1,1}a_{2,2}a_{3,3} - a_{1,1}a_{3,2} a_{2,3} - a_{2,1}a_{1,2}a_{3,3} + a_{2,1}a_{3,2}a_{1,3} + a_{3,1}a_{1,2}a_{2,3} - a_{3,1}a_{2,2}a_{1,3}
$$

# Ejercicio 2
$$
\left|
\begin{array}{cc}
2 & 0 & 1 & 1 \\
2 & 2 & -4 & -1 \\
-3 & 1 & 1 & 1 \\
2 & -2 & 0 & 0
\end{array}
\right|
$$
$$
\left|
\begin{array}{cc}
2 & 0 & 1 & 1 \\
0 & 2 & -5 & -2 \\
0 & 1 & \frac{5}{2} & \frac{5}{2} \\
0 & -2 & -1 & -1
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} + \frac{3}{2}F_{1} \\
&F_{4} \leftarrow F_{4} - F_{1}
\end{align}
$$
$$
\left|
\begin{array}{cc}
2 & 0 & 1 & 1 \\
0 & 2 & -5 & -2 \\
0 & 1 & \frac{5}{2} & \frac{5}{2} \\
0 & -2 & -1 & -1
\end{array}
\right| = 2 \times \left|
\begin{array}{cc}
2 & -5 & -2 \\
1 & \frac{5}{2} & \frac{5}{2} \\
-2 & -1 & -1
\end{array}
\right|
$$
$$
\left|
\begin{array}{cc}
2 & -5 & -2 \\
0 & 5 & \frac{7}{2} \\
0 & -6 & -3
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} - \frac{1}{2}F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\implies 2 \times \left|
\begin{array}{cc}
2 & -5 & -2 \\
1 & \frac{5}{2} & \frac{5}{2} \\
-2 & -1 & -1
\end{array}
\right| = 2 \times \left|
\begin{array}{cc}
2 & -5 & -2 \\
0 & 5 & \frac{7}{2} \\
0 & -6 & -3
\end{array}
\right| = 2 \times 2 \times \left|
\begin{array}{cc}
5 & \frac{7}{2} \\
-6 & -3
\end{array}
\right|
$$
$$
= 2 \times 2 \times \left( 5 \times ( -3) + 6 \times \frac{7}{2} \right) = 4 \times (-15 + 21) = 4 \times 6 = 24
$$
$$
\implies \left|
\begin{array}{cc}
2 & 0 & 1 & 1 \\
2 & 2 & -4 & -1 \\
-3 & 1 & 1 & 1 \\
2 & -2 & 0 & 0
\end{array}
\right| = 24
$$
