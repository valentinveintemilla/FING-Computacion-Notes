Durante todo el práctico utilizaremos los conceptos de polinomio de Taylor y polinomio de Mc-Laurin.

> [!Definición - Polinomio de Taylor]
> Sea $f$ derivable hasta el orden $n$ en $x = a$, siendo $a$ un punto en el interior del dominio de $f$. Entonces:
> $$
> P_{n}(f, a)(x) := \sum_{k = 0}^{n} \frac{f^{(k)}(a)}{k!} (x - a)^{k}
> $$
> Lo denominamos Polinomio de Taylor de $f$ en el punto $a$.

> [!Definición - Polinomios de Mc-Laurin]
> Un caso particular es $a = 0$:
> $$
> P_{n}(f, 0)(x) = \frac{f(0)}{0!} + \frac{f'(0)x}{1!} + \frac{f''(0)x^{2}}{2!} + \dots + \frac{f^{(n)}(0)x^{n}}{n!}
> $$
> Estos polinomios son denominados Polinomios de Mc-Laurin, y tienen una expresión propia:
> $$
> P_{n}(f, 0)(x) = \sum_{k = 0}^{n} \frac{f^{(n)}(0)}{k!} x^{k}
> $$

Además, es fundamental comprender el teorema de Taylor, el cual es la formalización de la idea anterior:
> [!Teorema de Taylor]
> Sea $f$ una función derivable hasta el orden $n$ en $x = a$.
> 
> Entonces existe un único polinomio $P_{n}(f, a)$ de grado $n$ en $(x - a)$, tal que
> $$
> f(x) = P_{n}(f, a)(x) + r_{n}(x)
> $$
> donde $\lim_{ x \to a } \frac{r_{n}}{(x - a)^{n}} = 0$.
> 
> Además,
> $$
> P_{n}(f, a)(x) = \sum_{k = 0}^{n} \frac{f^{(k)}(a) (x - a)}{n!}
> $$

# 1 - Polinomio de Taylor y límites

## Ejercicio 8.1.1
Sabiendo que el polinomio de Mc-Laurin es el polinomio de Taylor de una función, evaluado para $a = 0$, entonces podemos identificar cada uno de los términos:

Sabiendo que:
$$
P_{4}(f, 0)(x) = 3 - 5x + 4x^{2} - x^{3} - 2x^{4}
$$
Consideremos la forma de un polinomio de Mc-Laurin genérico:
$$
P_{n}(f, 0)(x) = \sum_{k = 0}^{n} \frac{f^{(n)}(0)}{k!} x^{k} = f(0) + f'(0)x + \frac{f''(0)x^{2}}{2} + \frac{f'''(0)x^{3}}{3!} + \dots + \frac{f^{(n)}x^{n}}{n!}
$$

Procedemos a identificar los términos anteriores:
$$
P_{4}(f, 0)(x) = \underbrace{ 3 }_{ f(0) = 3 } - \underbrace{ 5 }_{ f'(0) = -5 }x + \underbrace{ 4 }_{ \frac{f''(0)}{2} = 4 \implies f''(0) = 8 }x^{2} - \underbrace{ 1 }_{ \frac{f'''(0)}{6} = -1 \implies f'''(0) = -6 }x^{3} - \underbrace{ 2 }_{ \frac{f^{(4)}(0)}{24} = -2 \implies f^{(4)}(0) = -48 }x^{4}
$$

En conclusión:
$$
\begin{align}
&f(0) = 3 \\
&f'(0) = -5 \\
&f''(0) = 8 \\
&f'''(0) = -6 \\
&f^{(4)}(0) = -48
\end{align}
$$

---
## Ejercicio 8.1.2
Una parte por fila.

### Parte 
$$
$$



---
## Ejercicio 8.1.3
Tres partes de distintas filas.

### Parte a)
$$
\begin{align}
&n = 1 \implies (x \cos(x) - \sin(x))' = \cancel{ \cos(x) } - x \sin(x) - \cancel{ \cos(x) } = -x \sin(x) \\
&n = 2 \implies (-x \sin(x))' = -\sin(x) - x \cos(x) \\
&n = 3 \implies (-\sin(x) - x \cos(x))' = -\cos(x) - \cos(x) + x \sin(x) = -2\cos(x) + x \sin(x) \\
&n = 4 \implies (-2\cos(x) + x \sin(x))' = 
\end{align}
$$

$$
P_{5}
$$


---
## Ejercicio 8.1.4
Una parte por fila.



---
## Ejercicio 8.1.5
Dos partes.



---
## Ejercicio 8.1.8
Una parte.



---
## Ejercicio 8.1.9
Una parte por fila.



---
# 2 - Resto de Taylor y aproximaciones
En estos ejercicio, tenemos que hacer uso del resto de Lagrange:

> [!Forma de Lagrange para el resto]
> Sea $f$ derivable hasta el orden $n + 1$ en $E(a, \delta)$, entonces:
> $$
> \forall x \in E(a, \delta), f(x) = f(a) + f'(a)(x - a) + \dots + \frac{f^{(n)}(x - a)^{n}}{n!} + r_{n}(x)
> $$
> donde
> $$
> r_{n}(x) = \frac{f^{(n + 1)}(c_{x})(x - a)^{n + 1}}{(n + 1)!}
> $$

## Ejercicio 8.2.1
Dos partes

Siempre que queremos aproximar a un valor racional, lo mejor es utilizar $x = 0$ (polinomio de Mc-Laurin). En realidad, no estamos obligados a hacerlo. Lo que pasa es que tenemos que considerar un punto para el que conozcamos el valor de la función utilizada (por ejemplo, también podríamos utilizar $\frac{\pi}{2}$). Dependiendo de que tan lejos esté el valor seleccionado, de mayor orden será el polinomio que tengamos que desarrollar.

### Parte b)
En este caso, fijaremos $x = 0$:
$$
\begin{align}
&n = 0 \implies \sin(0) = 0 \\
&n = 1 \implies \cos(0) = 1 \\
&n = 2 \implies -\sin(0) = 0 \\
&n = 3 \implies -\cos(0) = -1 \\
&n = 4 \implies \sin(0) = 0 \\
&n = 5 \implies \cos(0) = 1 \\
&\vdots
\end{align}
$$
$$
\begin{align}
P_{n}(\sin, 0)(2) &= 2 - \frac{2^{3}}{3!} + \frac{2^{5}}{5!} - \frac{2^{7}}{7!} + \dots
\end{align}
$$
Entonces, considerando un $n$ impar:
$$
\left| \sin(2) - \left( 2 - \frac{2^{3}}{3!} + \frac{2^{5}}{5!} - \frac{2^{7}}{7!} + \dots + \frac{2^{n}}{n!} \right) \right| = \frac{\sin(c)}{(n + 1)!}
$$

Para determinar el $n$ necesario, el resto de Lagrange:
$$
r_{n}(x) = \frac{\sin ^{(n + 1)}(c)}{(n + 1)!} < 10^{-4} = \frac{1}{10000}
$$ 