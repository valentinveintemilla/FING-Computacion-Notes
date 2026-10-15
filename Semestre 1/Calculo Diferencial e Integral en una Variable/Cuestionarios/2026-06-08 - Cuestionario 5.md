# Ejercicio 2
Sabemos que
$$
f(x) = 3x + e^{2x}
$$
Queremos estudiar $g(x)$, siendo $g$ la función inversa de $f$. Por esta razón, se cumple que
$$
g \circ f(x) = f \circ g(x) = x
$$

Además, queremos determinar $g'(1)$ (en caso de existir).

Comenzamos:
$$
g \circ f(x) = f \circ g(x) = x \implies g \circ f(1) = f \circ g(1) = 1
$$
Podemos derivar y la igualdad se mantiene:
$$
(g \circ f)'(1) = (f \circ g)'(1) = (1)'
$$
$$
(g \circ f)'(1) = g'(f(1)) \times f'(1)
$$
$$
(f \circ g)'(1)  = f'(g(1)) \times g'(1)
$$
$$
(1)' = 0
$$
$$
f'(x) = (3x)' + (e^{2x})' = 3 + e^{2x} \times (2x)' = 3 + 2e^{2x}
$$
$$
\implies \begin{align}
&f(1) = 3 \times 1 + e^{2 \times 1} = 3 + e^{2} \\
&f'(1) = 3 + 2e^{2 \times 1} = 3 + 2e^{2}
\end{align}
$$
Sabiendo que $g$ es la inversa de $f$, entonces:
$$
f(1) = 3 + e^{2} \implies g(3 + e^{2}) = 1
$$
$$
\implies f'(g(1)) = 3 + 2e^{2 \times \frac{1}{3 + e^{2}}} = 3 + 2e^{\frac{2}{3 + e^{2}}}
$$
Nos falta descubrir

Ahora, sustituimos los valores obtenidos en las fórmulas:
$$
g'(f(1)) \times f'(1) = g'(3 + e^{2}) \times 3 + 2e^{2}
$$

$$
f'(g(1)) \times g'(1) = \left( 3 + 2e^{\frac{2}{3 + e^{2}}} \right) \times (3 + 2e^{2})
$$

Sabemos que para las funciones inversas se cumple que:
$$
(f^{-1})'(y) = \frac{1}{f'(f^{-1}(y))}
$$
Entonces, consideraremos la función $g = f^{-1}$:
$$
(g)'(y) = \frac{1}{f'(g(y))}
$$
Ahora, queremos determinar $g'(1)$:
$$
(g)'(1) = \frac{1}{f'(g(1))}
$$
Para determinar $g(1)$, tenemos que descubrir para que valor de $x$ se cumple que $f(x) = 1$:
$$
f(x) = 3x + e^{2x} = 1
$$
Si consideramos $x = 0$, podemos ver que:
$$
3x + e^{2x} = 0 + e^{0} = 1
$$
De esta forma, sabemos que $g(1) = 0$:

Ahora, podemos continuar:
$$
(g)'(1) = \frac{1}{f'(g(1))} = \frac{1}{f'(0)}
$$
$$
f'(x) = 3 + 2e^{2x} \implies f'(0) = 3 + 2e^{2 \times 0} = 3 + 2e^{0} = 3 + 2 = 5
$$
$$
\frac{1}{f'(0)} = \frac{1}{5}
$$
En conclusión:
$$
g'(1) = \frac{1}{5}
$$

---
# Ejercicio 3
Básicamente, tenemos la siguiente función:
$$
A(x) = x \times 1 + \frac{x \times \sqrt{ 1 - x^{2} }}{2} = x + \frac{x \times \sqrt{ 1 - x^{2} }}{2} = \frac{2x + x \times \sqrt{ 1 - x^{2} }}{2}
$$
Ahora, derivamos la función:
$$
A'(x) = 1 + \frac{x \times \sqrt{ 1 - x^{2} }}{2}
$$

Luego, tenemos que encontrar las raíces de la derivada:
$$
A(x) = 0 \implies 2x + x \sqrt{ 1 - x^{2} } = 0 \implies 2x = - x \times \sqrt{ 1 - x^{2} }
$$
$$
\begin{align}
2x &= - x \times \sqrt{ 1 - x^{2} } \\
-\frac{2\cancel{ x }}{\cancel{ x }} &= \sqrt{ 1 - x^{2} } \\
-2 &= \sqrt{ 1 - x^{2} } \\
(-2)^{2} &= 1 - x^{2} \\
4 &= 1 - x^{2} \\
4 - 1 &= -x^{2} \\
3 &= -x^{2} \\
-3 &= x^{2}
\end{align}
$$

## Opción correcta:
$$
\left( \frac{3}{4} \right)^{\frac{1}{4}}
$$

---
# Ejercicio 4:
$$
g(x) = \int_{1}^{f(x)} f(t) dt \implies g(x) = \int_{1}^{x + 1} f(t) dt
$$
$$
\implies g'(x) = f(f(x)) \times f'(x) - \cancel{ f(1) \times (1)' } = f(f(x)) \times f'(x)
$$
$$
g'(x) = f(x + 1) \times x^{2} = (x + 2) \times x^{2} = x^{3} + 2x^{2}
$$
$$
\implies g'(3) = 3^{3} + 2 \times 3^{2} = 27 + 18 = 45
$$
## Opción correcta:
$$
g'(3) = 45
$$

---
# Ejercicio 5:
