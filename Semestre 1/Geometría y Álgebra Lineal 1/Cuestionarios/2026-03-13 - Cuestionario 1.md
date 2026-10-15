# Ejercicio 3
Consideremos el siguiente sistema de ecuaciones lineales:
$$
{\begin{cases}
2x+y-z+w=1 \\
2y+z-w=0 \\
2x+3y=2
\end{cases}}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 1 & -1 & 1 & 1 \\
0 & 2 & 1 & -1 & 0 \\
2 & 3 & 0 & 0 & 2
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
2 & 1 & -1 & 1 & 1 \\
0 & 2 & 1 & -1 & 0 \\
2 & 3 & 0 & 0 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 3 & 0 & 0 & 1 \\
0 & 2 & 1 & -1 & 0 \\
2 & 3 & 0 & 0 & 2
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 3 & 0 & 0 & 1 \\
0 & 2 & 1 & -1 & 0 \\
0 & 0 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
\end{align}
$$
El sistema es Incompatible, ya que llegamos a una incoherencia. Además, si aplicamos el Teorema de Rouché-Frobenius, vemos que el rango de la matriz ampliada es menor que el de la matriz del sistema (hay un escalón en la columna de los términos independientes).

# Ejercicio 4
Hallar $\lambda$ tal que $z=\frac{\lambda-4i}{2+i}$ sea un imaginario puro.

Para que sea un imaginario puro, entonces la parte real debe ser 0 ($\mathrm{Re}(z)=0$). O sea, que la forma de z sea simplemente bi.
Primero resolvamos la división:
$$
\begin{align}
&z=\frac{\lambda-4i}{2+i} \\
&=\frac{(\lambda-4i)(2-i)}{(2+i)(2-i)} \\
&=\frac{2\lambda-\lambda i-8i+4i^{2}}{4- \not 2i+ \not 2i-i^{2}} \\
&=\frac{(2\lambda-4)-(\lambda +8)i}{5} \\
&=\frac{(2\lambda-4)}{5} - \frac{(\lambda +8)i}{5} \\
\end{align}
$$
Para que la parte real sea 0, tenemos que hacer que $2\lambda-4=0$:
$$
\begin{align}
&2\lambda-4=0 \\
&2\lambda=4 \\
&\lambda=\frac{4}{2} \\
&\lambda=2
\end{align}
$$
De esta forma, el valor de z es:
$$
\begin{align}
&\frac{(2 \times 2-4)}{5} - \frac{(2 +8)i}{5} \\
&=\frac{(4-4)}{5} - \frac{10i}{5} \\
&=\frac{0}{5} - \frac{10i}{5} \\
&=- \frac{10i}{5} \\
&=-2i
\end{align}
$$
En conclusión, para que z sea un imaginario puro, el valor de lambda debe ser 2. También encontramos el valor de z para lambda = 2:
$$
\begin{align}
&z=-2i=(0,-2)
\end{align}
$$
