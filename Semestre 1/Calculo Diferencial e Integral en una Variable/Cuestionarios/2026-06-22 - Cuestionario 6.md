# Ejercicio 1
$$
\int_{0}^{3} x e^{x^{2}} \space dx
$$
Aplicaremos sustitución para resolver la integral:
$$
\int_{0}^{3} x e^{x^{2}} \space dx = \frac{1}{2}\int_{0}^{3} 2x e^{x^{2}} \space dx
$$
Como vemos:
$$
\begin{align}
&f(g(x)) = e^{x^{2}} \\
&g(x) = x^{2} \implies g'(x) = 2x \\
\end{align}
$$
$$
\frac{1}{2}\int 2x e^{x^{2}} \space dx \underbrace{ = }_{ \begin{align}
&u = x^{2} \\
&du = 2x \space dx
\end{align} } \frac{1}{2}\int e^{u} \space du = \frac{e^{u}}{2} + C = \frac{e^{x^{2}}}{2} + C
$$
Ahora, aplicamos Barrow:
$$
\begin{align}
\int_{0}^{3} x e^{x^{2}} \space dx &= \left. \frac{e^{x^{2}}}{2} \right|_{0}^{3} \\
&= \frac{e^{3^{2}}}{2} - \frac{e^{0^{2}}}{2} \\
&= \frac{e^{9}}{2} - \frac{e^{0}}{2} \\
&= \frac{e^{9}}{2} - \frac{1}{2} \\
&= \frac{e^{9} - 1}{2}
\end{align}
$$
En conclusión:
$$
\int_{0}^{3} x e^{x^{2}} \space dx = \frac{e^{9} - 1}{2}
$$

---
# Ejercicio 3
$$
\int_{0}^{2} f^{(3)}(x) x^{2} \space dx
$$
Una primitiva de $f^{(3)}(x)$ es $f^{(2)}(x)$, ya que $(f^{(2)}(x))' = f^{(3)}(x)$. De esta forma, podemos aplicar partes:
$$
\left[
\begin{align}
&f(x) = x^{2} \implies f'(x) = 2x \\
&g'(x) = f^{(3)}(x) \implies g(x) = f^{(2)}(x) \\
\end{align}
\right]
$$
$$
\begin{align}
\int f^{(3)}(x) x^{2} \space dx &= x^{2} \cdot f^{(2)}(x) - \int f^{(2)}(x) 2x \space dx \\
&= x^{2} \cdot f^{(2)}(x) - 2\int f^{(2)}(x) x \space dx
\end{align}
$$
Volvemos a aplicar partes sobre la nueva integral:
$$
\int f^{(2)}(x) x \space dx
$$$$
\left[
\begin{align}
&f(x) = x \implies f'(x) = 1 \\
&g'(x) = f^{(2)}(x) \implies g(x) = f^{(1)}(x) \\
\end{align}
\right]
$$$$
\begin{align}
\int f^{(2)}(x) x \space dx &= x \cdot f^{(1)}(x) - \int f^{(1)}(x) \space dx \\
&= x \cdot f^{(1)}(x) - f^{(0)}(x)
\end{align}
$$
$$
\begin{align}
\implies \int f^{(3)}(x) x^{2} \space dx &= x^{2} \cdot f^{(2)}(x) - 2(x \cdot f^{(1)}(x) - f^{(0)}(x)) \\
&= x^{2} \cdot f^{(2)}(x) - 2x \cdot f^{(1)}(x) + 2f^{(0)}(x)
\end{align}
$$
A continuación, consideramos los extremos de integración:
$$
\begin{align}
\int_{0}^{2} f^{(3)}(x) x^{2} \space dx &= (x^{2} \cdot f^{(2)}(x)) |_{0}^{2} - (2x \cdot f^{(1)}(x)) |_{0}^{2} + 2f^{(0)}(x) |_{0}^{2} \\
&= (2^{2} \cdot f^{(2)}(2) - \cancel{ 0^{2} \cdot f^{(2)}(0) }) - (2 \cdot 2 \cdot f^{(1)}(2) - \cancel{ 2 \cdot 0 \cdot f^{(1)}(0) }) + (2f^{(0)}(2) - 2f^{(0)}(0)) \\
&= (4 \cdot 5) - (4 \cdot 4) + (2 \cdot 3 - 2 \cdot 2) \\
&= (4 \cdot 5) - (4 \cdot 4) + (6 - 4) \\
&= 20 - 16 + 2 \\
&= 6
\end{align}
$$

En conclusión:
$$
\int_{0}^{2} f^{(3)}(x) x^{2} \space dx = 6
$$

---
# Ejercicio 4
Tenemos tres funciones:
$$
\begin{align}
&f(x) = x^{2} \\
&g(x) = x + 2 \\
&h(x) = 4 - x^{2}
\end{align}
$$
Primero, determinemos los puntos de intersección de las funciones: podemos ver que:
- $x^{2}$ y $x + 2$ se interceptan en $x = -1$
- $x^{2}$ y $4 - x^{2}$ se interceptan en $x = \sqrt{ 2 }$
- $4 - x^{2}$ y $x + 2$ se interceptan en $x = -2$ y $x = 1$

Calculemos el área pequeña:
$$
\int_{-\sqrt{ 2 }}^{-1} 4 - x^{2} \space dx - \int_{-\sqrt{ 2 }}^{-1} x^{2} \space dx = \int_{-\sqrt{ 2 }}^{-1} 4 \space dx - 2\int_{-\sqrt{ 2 }}^{-1} x^{2} \space dx
$$
Conocemos primitivas de ambas funciones:
$$
\begin{align}
&f'(x) = 4 \implies f(x) = 4x \\
&g'(x) = x^{2} \implies g(x) = \frac{x^{3}}{3}
\end{align}
$$
De esta forma:
$$
\begin{align}
&\int_{-\sqrt{ 2 }}^{-1} 4 \space dx = 4x |_{-\sqrt{ 2 }}^{-1} = 4 \cdot (-1) - 4 \cdot (-\sqrt{ 2 }) = -4 + 4\sqrt{ 2 } = 4\sqrt{ 2 } - 4 \\
&\int_{-\sqrt{ 2 }}^{-1} x^{2} \space dx = \left. \frac{x^{3}}{3} \right|_{-\sqrt{ 2 }}^{-1} = \frac{(-1)^{3}}{3} - \frac{(-\sqrt{ 2 })^{3}}{3} = -\frac{1}{3} + \frac{2\sqrt{ 2 }}{3}
\end{align}
$$
Entonces:
$$
\begin{align}
\int_{-\sqrt{ 2 }}^{-1} 4 \space dx - 2\int_{-\sqrt{ 2 }}^{-1} x^{2} \space dx &= (4\sqrt{ 2 } - 4) - 2\left( -\frac{1}{3} + \frac{2\sqrt{ 2 }}{3} \right) \\
&= 4\sqrt{ 2 } - 4 + \frac{2}{3} - \frac{4\sqrt{ 2 }}{3} \\
&= \frac{12\sqrt{ 2 }}{3} - \frac{12}{3} + \frac{2}{3} - \frac{4\sqrt{ 2 }}{3} \\
&= \frac{12\sqrt{ 2 } - 12 + 2 - 4\sqrt{ 2 }}{3} \\
&= \frac{8\sqrt{ 2 } - 10}{3}
\end{align}
$$
Ahora, proseguimos con la otra parte:
$$
\int_{-1}^{1} 4 - x^{2} \space dx - \int_{-1}^{1} x + 2 \space dx = \int_{-1}^{1} 4 \space dx - \int_{-1}^{1} x^{2} \space dx - \int_{-1}^{1} x \space dx - \int_{-1}^{1} 2 \space dx = \int_{-1}^{1} 2 \space dx - \int_{-1}^{1} x^{2} \space dx - \int_{-1}^{1} x \space dx
$$
$$
\begin{align}
&\int_{-1}^{1} 2 \space dx = 2x |_{-1}^{1} = 2 \cdot 1 - 2 \cdot (-1) = 2 + 2 = 4 \\
&\int_{-1}^{1} x^{2} \space dx = \left. \frac{x^{3}}{3} \right|_{-1}^{1} = \frac{1^{3}}{3} - \frac{(-1)^{3}}{3} = \frac{1}{3} + \frac{1}{3} = \frac{2}{3} \\
&\int_{-1}^{1} x \space dx = \left. \frac{x^{2}}{2} \right|_{-1}^{1} = \frac{1^{2}}{2} - \frac{(-1)^{2}}{2} = \frac{1}{2} - \frac{1}{2} = 0
\end{align}
$$
$$
\begin{align}
\int_{-1}^{1} 2 \space dx - \int_{-1}^{1} x^{2} \space dx - \int_{-1}^{1} x \space dx &= 4 - \frac{2}{3} - 0 \\
&= \frac{12}{3} - \frac{2}{3} \\
&= \frac{10}{3}
\end{align}
$$
Ahora, sumamos ambos cálculos:
$$
\frac{8\sqrt{ 2 } - 10}{3} + \frac{10}{3} = \frac{8\sqrt{ 2 } - 10 + 10}{3} = \frac{8\sqrt{ 2 }}{3}
$$