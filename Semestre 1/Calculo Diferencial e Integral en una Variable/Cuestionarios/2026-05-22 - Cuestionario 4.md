# Ejercicio 2
$$
h(x) = f(g(x)) + xf(x)
$$
Sabiendo que $f(g(x)) = (f \circ g)(x)$ y $(f \circ g)'(x_{0}) = f'(g(x_{0})) \times g'(x_{0})$
$$
\implies h'(x) = f'(g(x)) \times g'(x) + f(x) + xf'(x)
$$
De esta forma:
$$
\begin{align}
h'(1) &= f'(g(1)) \times g'(1) + f(1) + f'(1) \\
&= f'(3) \times g'(1) + f(1) + f'(1) \\
&= 5 \times 8 + 4 + 10 \\
&= 40 + 4 + 10 \\
&= 54
\end{align}
$$
En conclusión:
$$
h'(1) = 54
$$

---
# Ejercicio 3
$$
\lim_{ x \to 0 } \frac{\sin(2x)}{\log(x + 1)} 
$$
Obtenemos una indeterminación de tipo $\frac{0}{0}$. Por lo tanto, tenemos que aplicar L'Hopital:
$$
\lim_{ x \to 0 } \frac{\sin(2x)}{\log(x + 1)} = \lim_{ x \to 0 } \frac{\cos(2x) \times 2}{\frac{1}{x + 1}} = \lim_{ x \to 0 } \cos(2x) \times 2 \times (x + 1)
$$
Ahora, simplemente sustituimos $x$ por 0:
$$
\lim_{ x \to 0 } \cos(2x) \times 2 \times (x + 1) = \cos(0) \times 2 \times 1 = 1 \times 2 \times 1 = 2
$$
En conclusión:
$$
\lim_{ x \to 0 } \frac{\sin(2x)}{\log(x + 1)} = 2
$$

---
# Ejercicio 5
$$
f(t) = \begin{cases}
\begin{align}
&e^{2t - 2} &&\text{si } t < 1 \\
&at + b &&\text{si } t \geq 1
\end{align}
\end{cases}
$$
Analizamos $e^{2t - 2}$ para $t = 1$:
$$
e^{2 - 2} = e^{0} = 1
$$
De esta forma, sabemos que $at + b = 1$ para $t = 1$ ($\implies a + b = 1$)

Ahora, analicemos la pendiente (derivada) de la función $e^{2t - 2}$ para $t = 1$. Esto nos determinará el valor de $a$:
Sabemos que $e^{x} = \exp x \implies e^{2t - 2} = \exp(2t - 2)$. En este caso, para derivar la función, consideramos que:
$$
\exp'(x) = \exp x \implies (e^{x})' = e^{x}
$$
Además, tenemos que considerar la regla de la cadena:
$$
(f \circ g)'(x) = f'(g(x)) \times g'(x)
$$
De esta forma:
$$
(e^{2t - 2})' = e^{2t - 2} \times (2t - 2)' = e^{2t - 2} \times 2
$$
Sabiendo que analizamos el caso $t = 1$:
$$
e^{2 - 2} \times 2 = 1 \times 2 = 2
$$
Es así que la pendiente de la función $e^{2t - 2}$ en el punto $t = 1$ es 2. Por lo tanto, consideraremos $a = 2$.

Sabiendo que $a = 2$ y $a + b = 1$ (ya que estudiamos el caso $t = 1$):
$$
\begin{align}
&a + b = 1 \\
&2 + b = 1 \\
&b = 1 - 2 \\
&b = -1
\end{align}
$$
En conclusión, la función
$$
f(t) = \begin{cases}
\begin{align}
&e^{2t - 2} &&\text{si } t < 1 \\
&at + b &&\text{si } t \geq 1
\end{align}
\end{cases}
$$
es derivable en 1 si
$$
\begin{align}
&a = 2 \\
&b = -1
\end{align}
$$