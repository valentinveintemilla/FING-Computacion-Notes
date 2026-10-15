# Concepto y ejemplos de transformaciones lineales
## Ejercicio 1
Tres partes.

Para determinar si una función entre dos espacios vectoriales es una transformación lineal. tenemos que determinar que:
$$
\begin{align}
&T(\vec{0}_{V}) = \vec{0}_{W} \\
&T(u +_{V} v) = T(u) +_{W} T(v) \\
&T(\alpha \cdot_{V} u) = \alpha \cdot_{W} T(u)
\end{align}
$$

### Parte a)
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{2} \text{ tal que } T(x, y, z) = (y - x, z + y)
$$
Probamos que el nulo de $\mathbb{R}^{3}$ lleve al nulo de $\mathbb{R}^{2}$:
$$
T(0, 0, 0) = (0 - 0, 0 + 0) = (0, 0)
$$

Probamos la suma:
$$
\begin{align}
T((a, b, c) +_{\mathbb{R}^{3}} (d, e, f)) &= T(a + d, b + e, c + f) \\
&= (b + e - a - d, c + f + b + e) \\
T(a, b, c) +_{\mathbb{R}^{2}} T(d, e, f) &= (b - a, c + b) +_{\mathbb{R}^{2}} (e - d, f + e) \\
&= (b - a + e - d, c + b + f + e) \\
&= (b + e - a - d, c + f + b + e) \\
&= T((a, b, c) +_{\mathbb{R}^{3}} (d, e, f))
\end{align}
$$

Probamos el producto por un escalar:
$$
\begin{align}
T(\alpha \cdot_{\mathbb{R}^{3}} (a, b, c)) &= T(\alpha a, \alpha b, \alpha c) \\
&= (\alpha b - \alpha a, \alpha c + \alpha b) \\
\alpha \cdot_{\mathbb{R}^{2}} T(a, b, c) &= \alpha \cdot_{\mathbb{R}^{2}} (b - a, c + b) \\
&= (\alpha(b - a), \alpha(c + b)) \\
&= (\alpha b - \alpha a, \alpha c + \alpha b) \\
&= T(\alpha \cdot_{\mathbb{R}^{3}} (a, b, c))
\end{align}
$$

En conclusión, demostramos que $T$ es una transformación lineal.

### Parte c)
$$
\text{Dado } v \in \mathbb{R}^{3} \text{ fijo, y } T : \mathbb{R}^{3} \to \mathbb{R} \text{ tal que } T(u) = \langle u, v \rangle
$$
Esta transformación lineal consiste en transformar un vector de $\mathbb{R}^{3}$ en el resultado del producto escalar de dicho vector por un vector $v \in \mathbb{R}^{3}$ fijo.

Probamos que el nulo de $\mathbb{R}^{3}$ lleve al nulo de $\mathbb{R}$:
$$
T(0, 0, 0) = \langle (0, 0, 0), v \rangle = ||(0, 0, 0)|| \cdot ||v|| \cdot \cos \theta = 0 \qquad ( \text{ya que } ||\vec{0}|| = 0 )
$$

Probamos la suma:
$$
\begin{align}
T((a, b, c) +_{\mathbb{R}^{3}} (d, e, f)) &= T(a + d, b + e, c + f) \\
&= \langle (a + d, b + e, c + f), v \rangle \\
&= ||(a + d, b + e, c + f)|| \cdot ||v|| \cdot \cos \theta \\
T(a, b, c) +_{\mathbb{R}} T(d, e, f) &= (b - a, c + b) +_{\mathbb{R}} (e - d, f + e) \\
&= \langle (a, b, c), v \rangle +_{\mathbb{R}} \langle (d, e, f), v \rangle \\
&= ||(a, b, c)|| \cdot ||v|| \cdot \cos \theta + ||(d, e, f)|| \cdot ||v|| \cdot \cos \theta \\
&= (||(a, b, c)|| + ||(d, e, f)||) \cdot ||v|| \cdot \cos \theta \\
&= (||(a + d, b + e, c + f)|| \cdot ||v|| \cdot \cos \theta \\
&= T((a, b, c) +_{\mathbb{R}^{3}} (d, e, f))
\end{align}
$$

Probamos el producto por un escalar:
$$
\begin{align}
T(\alpha \cdot_{\mathbb{R}^{3}} (a, b, c)) &= T(\alpha a, \alpha b, \alpha c) \\
&= \langle (\alpha a, \alpha b, \alpha c), v \rangle \\
&= ||(\alpha a, \alpha b, \alpha c)|| \cdot ||v|| \cdot \cos \theta \\
&= ||\alpha(a, b, c)|| \cdot ||v|| \cdot \cos \theta \\
&= \alpha \cdot_{\mathbb{R}} ||(a, b, c)|| \cdot ||v|| \cdot \cos \theta \\
\alpha \cdot_{\mathbb{R}} T(a, b, c) &= \alpha \cdot_{\mathbb{R}} \langle (a, b, c), v \rangle \\
&= \alpha \cdot_{\mathbb{R}} ||(a, b, c)|| \cdot ||v|| \cdot \cos \theta \\
&= T(\alpha \cdot_{\mathbb{R}^{3}} (a, b, c))
\end{align}
$$

En conclusión, demostramos que $T$ es una transformación lineal.

ACLARACIÓN: En realidad se demuestra utilizando las propiedades de aditividad y homogeneidad del producto escalar (sin necesidad de desarrollar la expresión):
- Aditividad: por propiedad distributiva, $\langle u + w, v \rangle = \langle u, v \rangle + \langle w, v \rangle$
- Homogeneidad: $\langle \alpha u, v \rangle = \alpha \langle u, v \rangle$

### Parte e)
$$
T : \mathcal{M}_{n \times n}(\mathbb{R}) \to \mathcal{M}_{n \times n}(\mathbb{R}) \text{ tal que } T(A) = A^{T}
$$
Esta transformación lineal consiste en transformar una matriz cuadrada en su traspuesta.

Probamos que el nulo de $\mathcal{M}_{n \times n}(\mathbb{R})$ lleve al nulo de $\mathcal{M}_{n \times n}(\mathbb{R})$:
$$
T(O) = O^{T} = O
$$

Probamos la suma:
$$
\begin{align}
T(A + B) &= (A + B)^{T} \\
&= A^{T} + B^{T} \\
T(A) + T(B) &= A^{T} + B^{T} \\
&= (A + B)^{T} \\
&= T(A + B)
\end{align}
$$

Probamos el producto por un escalar:
$$
\begin{align}
T(\alpha \cdot A) &= (\alpha \cdot A)^{T} \\
&= \alpha \cdot A^{T} \\
\alpha \cdot T(A) &= \alpha \cdot A^{T} \\
&= T(\alpha \cdot A)
\end{align}
$$

En conclusión, demostramos que $T$ es una transformación lineal.

### Parte g)
$$
T : \mathbb{C}^{3} \to \mathbb{C}^{2} \text{ tal que } T(z_{1}, z_{2}, z_{3}) = (z_{2} - iz_{1}, z_{3} + 2z_{2})
$$

Probamos que el nulo de $\mathbb{C}^{3}$ lleve al nulo de $\mathbb{C}^{2}$:
$$
T(0, 0, 0) = (0 - 0i, 0 + 2 \cdot 0) = (0, 0)
$$

Probamos la suma:
$$
\begin{align}
T((z_{1}, z_{2}, z_{3}) + (z_{4}, z_{5}, z_{6})) &= T(z_{1} + z_{4}, z_{2} + z_{5}, z_{3} + z_{6}) \\
&= (z_{2} + z_{5} - i(z_{1} + z_{4}), z_{3} + z_{6} + 2(z_{2} + z_{5})) \\
&= (z_{2} + z_{5} - iz_{1} - iz_{4}, z_{3} + z_{6} + 2z_{2} + 2z_{5}) \\
T(z_{1}, z_{2}, z_{3}) + T(z_{4}, z_{5}, z_{6}) &= (z_{2} - iz_{1}, z_{3} + 2z_{2}) + (z_{5} - iz_{4}, z_{6} + 2z_{5}) \\
&= (z_{2} - iz_{1} + z_{5} - iz_{4}, z_{3} + 2z_{2} + z_{6} + 2z_{5}) \\
&= (z_{2} + z_{5} - iz_{1} - iz_{4}, z_{3} + z_{6} + 2z_{2} + 2z_{5}) \\
&= T((z_{1}, z_{2}, z_{3}) + (z_{4}, z_{5}, z_{6}))
\end{align}
$$

Probamos el producto por un escalar:
$$
\begin{align}
T(\alpha \cdot (z_{1}, z_{2}, z_{3})) &= T(\alpha \cdot z_{1}, \alpha \cdot z_{2}, \alpha \cdot z_{3}) \\
&= (\alpha \cdot z_{2} - \alpha \cdot iz_{1}, \alpha \cdot z_{3} + \alpha \cdot 2z_{2}) \\
&= (\alpha (z_{2} - iz_{1}), \alpha (z_{3} + 2z_{2})) \\
\alpha \cdot T(z_{1}, z_{2}, z_{3}) &= \alpha \cdot (z_{2} - iz_{1}, z_{3} + 2z_{2}) \\
&= (\alpha (z_{2} - iz_{1}), \alpha (z_{3} + 2z_{2})) \\
&= T(\alpha \cdot (z_{1}, z_{2}, z_{3}))
\end{align}
$$

En conclusión, demostramos que $T$ es una transformación lineal.

### Parte h)
$$
T : \mathbb{C}^{2} \to \mathbb{C}^{2} \text{ tal que } T(z_{1}, z_{2}) = (\overline{z_{1}}, iz_{1} + z_{2})
$$

Probamos que el nulo de $\mathbb{C}^{3}$ lleve al nulo de $\mathbb{C}^{2}$:
$$
T(0, 0) = (\overline{0}, 0i + 0) = (0, 0)
$$

Probamos la suma:
$$
\begin{align}
T((z_{1}, z_{2}) + (z_{3}, z_{4})) &= T(z_{1} + z_{3}, z_{2} + z_{4}) \\
&= (\overline{z_{1} + z_{3}}, i(z_{1} + z_{3}) + z_{2} + z_{4}) \\
T(z_{1}, z_{2}) + T(z_{3}, z_{4}) &= (\overline{z_{1}}, iz_{1} + z_{2}) + (\overline{z_{3}}, iz_{3} + z_{4}) \\
&= (\overline{z_{1}} + \overline{z_{3}}, iz_{1} + z_{2} + iz_{3} + z_{4}) \\
&= (\overline{z_{1} + z_{3}}, i(z_{1} + z_{3}) + z_{2} + z_{4}) \\
&= T((z_{1}, z_{2}) + (z_{3}, z_{4}))
\end{align}
$$

Probamos el producto por un escalar:
$$
\begin{align}
T(\alpha \cdot (z_{1}, z_{2})) &= T(\alpha \cdot z_{1}, \alpha \cdot z_{2}) \\
&= (\overline{\alpha \cdot z_{1}}, i(\alpha \cdot z_{1}) + \alpha \cdot z_{2}) \\
&= (\alpha \cdot \overline{z_{1}}, \alpha \cdot iz_{1} + \alpha \cdot z_{2}) \\
\alpha \cdot T(z_{1}, z_{2}) &= \alpha \cdot (\overline{z_{1}}, iz_{1} + z_{2}) \\
&= (\alpha \cdot \overline{z_{1}}, \alpha \cdot (iz_{1} + z_{2})) \\
&= (\alpha \cdot \overline{z_{1}}, \alpha \cdot iz_{1} + \alpha \cdot z_{2}) \\
&= T(\alpha \cdot (z_{1}, z_{2}))
\end{align}
$$

En conclusión, demostramos que $T$ es una transformación lineal.

---
## Ejercicio 2
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}
$$
$$
\begin{align}
&T(1, 0, 0) = (2, 1, 0) \\
&T(1, 1, 0) = (-1, 2, 3) \\
&T(1, 1, 1) = (0, 0, 1)
\end{align}
$$
Sabemos que $\{ (1, 0, 0), (1, 1, 0), (1, 1, 1) \}$ es una base de $\mathbb{R}^{3}$. De esta forma, $\{ (2, 1, 0), (-1, 2, 3), (0, 0, 1) \}$ tiene que ser una base también:
$$
\begin{cases}
2\alpha - \beta = 0 \\
\alpha + 2\beta = 0 \\
3\beta + \gamma = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
2 & -1 & 0 & 0 \\
1 & 2 & 0 & 0 \\
0 & 3 & 1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
0 & -5 & 0 & 0 \\
1 & 2 & 0 & 0 \\
0 & 3 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & 0 \\
1 & 2 & 0 & 0 \\
0 & 3 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow -\frac{1}{5}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1} \\
&F_{3} \leftarrow F_{3} - 3F_{1}
\end{align}
$$
Como vemos, la única solución del sistema es la solución trivial, lo que confirma que el conjunto es LI, y al tener 3 elementos (sabiendo que $dim(\mathbb{R}^{3}) = 3$) confirmamos que es un generador, y en conclusión, base de $\mathbb{R}^{3}$.

Intentaremos definir la forma genérica de la transformación lineal:
$$
\begin{align}
T(x, y, z) &= T(x(1, 0, 0) + y(0, 1, 0) + z(0, 0, 1)) \\
&= xT(1, 0, 0) + yT(0, 1, 0) + zT(0, 0, 1) \\
&= xT(1, 0, 0) + yT((1, 1, 0) - (1, 0, 0)) + zT((1, 1, 1) - (1, 1, 0)) \\
&= xT(1, 0, 0) + y(T(1, 1, 0) - T(1, 0, 0)) + z(T(1, 1, 1) - T(1, 1, 0)) \\
&= x(2, 1, 0) + y((-1, 2, 3) - (2, 1, 0)) + z((0, 0, 1) - (-1, 2, 3)) \\
&= x(2, 1, 0) + y(-3, 1, 3) + z(1, -2, -2) \\
&= (2x, x, 0) + (-3y, y, 3y) + (z, -2z, -2z) \\
&= (2x - 3y + z, x + y - 2z, 3y - 2z)
\end{align}
$$

En conclusión:
$$
T(x, y, z) = (2x - 3y + z, x + y - 2z, 3y - 2z)
$$

## Ejercicio 3
Dos partes.

### Parte a)
$$
T : \mathbb{R}_{2}[x] \to \mathbb{R}^{2}
$$
$$
\begin{align}
&T(1) = (1, 0) \\
&T(x) = (1, 1) \\
&T(x^{2}) = (0, 0)
\end{align}
$$
Sabemos que $\{ 1, x, x^{2} \}$ es la base canónica de $\mathbb{R}_{2}[x]$.

Tenemos que determinar cual es la fórmula general para una trasformación lineal $T(p)$, siendo $p$ cualquier polinomio:
$$
\begin{align}
p = c + bx + ax^{2} \implies T(p) &= T(c + bx + ax^{2}) \\
&= T(c) + T(bx) + T(ax^{2}) \\
&= cT(1) + bT(x) + aT(x^{2}) \\
&= c(1, 0) + b(1, 1) + a(0, 0) \\
&= (c, 0) + (b, b) + (0, 0) \\
&= (c + b, b)
\end{align}
$$

En conclusión:
$$
T(p) = (c + b, b)
$$

### Parte b)
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}
$$
$$
\begin{align}
&T(1, 0, 0) = (2, 1, 0) \\
&T(1, 1, 0) = (-1, 2, 3) \\
&T(3, 2, 0) = (0, 5, 6)
\end{align}
$$
Primero que nada, determinemos si la transformación lineal es correcta:
$$
(1, 0, 0) = (3, 2, 0) - 2(1, 1, 0) \implies T(1, 0, 0) = T(3, 2, 0) - T(2(1, 1, 0))
$$
$$
\begin{align}
T(1, 0, 0) &= T(3, 2, 0) - 2T(1, 1, 0) \\
&= (0, 5, 6) - 2(-1, 2, 3) \\
&= (0, 5, 6) - (-2, 4, 6) \\
&= (0 + 2, 5 - 4, 6 - 6) \\
&= (2, 1, 0) \\
&= T(1, 0, 0)
\end{align}
$$
Verificamos que la transformación lineal está correctamente definida. Ahora, definamos la forma genérica:
$$
\begin{align}
T(x, y, z) &= T(x(1, 0, 0)) + T(y(0, 1, 0)) + T(z(0, 0, 1)) \\
&= xT(1, 0, 0) + yT(0, 1, 0) + zT(0, 0, 1)
\end{align}
$$
Si bien podemos formar los vectores $(1, 0, 0) = (3, 2, 0) - 2(1, 1, 0)$ y $(0, 1, 0) = (1, 1, 0) - (1, 0, 0)$, no tenemos forma de dar con el vector $(0, 0, 1)$ mediante combinación lineal de los vectores anteriores (ya que todos tienen 0 en la tercera posición). Entonces $\{ (1, 0, 0), (1, 1, 0), (3, 2, 0) \}$ no es LI, por lo que no es base de $\mathbb{R}^{3}$. Por esta razón, existen infinitas transformaciones lineales que cumplen las condiciones iniciales.

Si agregáramos una condición más, como la propuesta:
$$
T(0, 0, 1) = (6, 2, 3)
$$
Ahora, podemos definir una forma genérica para la transformación lineal:
$$
\begin{align}
T(x, y, z) &= T(x(1, 0, 0)) + T(y(0, 1, 0)) + T(z(0, 0, 1)) \\
&= xT(1, 0, 0) + yT(0, 1, 0) + zT(0, 0, 1) \\
&= xT((3, 2, 0) - 2(1, 1, 0)) + yT((1, 1, 0) - (1, 0, 0)) + zT(0, 0, 1) \\
&= x(T(3, 2, 0) - 2T(1, 1, 0)) + y(T(1, 1, 0) - T(1, 0, 0)) + zT(0, 0, 1) \\
&= x((0, 5, 6) - (-2, 4, 6)) + y((-1, 2, 3) - (2, 1, 0)) + z(6, 2, 3) \\
&= x(2, 1, 0) + y(-3, 1, 3) + z(6, 2, 3) \\
&= (2x, x, 0) + (-3y, y, 3y) + (6z, 2z, 3z) \\
&= (2x - 3y + 6z, x + y + 2z, 3y + 3z)
\end{align}
$$

En conclusión, si agregamos la condición anterior, existe una única transformación lineal que verifica las condiciones dadas, y tiene la siguiente forma:
$$
T(x, y, z) = (2x - 3y + 6z, x + y + 2z, 3y + 3z)
$$

### Parte c)
$$
T : \mathbb{R}_{2}[x] \to \mathbb{R}^{2}
$$
$$
\begin{align}
&T(1) = (1, 0) \\
&T(1 + x) = (1, 1) \\
&T(1 + x + x^{2}) = (0, 0) \\
&T(3 + 2x + x^{2}) = (2, 1)
\end{align}
$$
Para saber si existe la transformación lineal propuesta, tenemos que determinar si $T(3 + 2x + x^{2})$ se puede conformar por combinación lineal del resto, ya que $\{ 1, 1 + x, 1 + x + x^{2} \}$ es base de $\mathbb{R}_{2}[x]$:
$$
\begin{align}
T(3 + 2x + x^{2}) &= T(1 + (1 + x) + (1 + x + x^{2})) \\
&= T(1) + T(1 + x) + T(1 + x + x^{2}) \\
&= (1, 0) + (1, 1) + (0, 0) \\
&= (2, 1)
\end{align}
$$

Como vemos, la igualdad se cumple, por lo que existe alguna transformación lineal que satisface las condiciones establecidas. Ahora, también podemos enunciar que es única, ya que estamos trabajando sobre una base de $\mathbb{R}_{2}[x]$, por lo tanto podemos determinar la forma genérica de la transformación:
$$
\begin{align}
T(c + bx + ax^{2}) &= T(c(1)) + T(b((1 + x) - (1))) + T(a((1 + x + x^{2}) - (1 + x))) \\
&= cT(1) + b(T(1 + x) - T(1)) + a(T(1 + x + x^{2}) - T(1 + x)) \\
&= c(1, 0) + b((1, 1) - (1, 0)) + a((0, 0) - (1, 1)) \\
&= c(1, 0) + b(0, 1) + a(-1, -1) \\
&= (c, 0) + (0, b) + (-a, -a) \\
&= (c - a, b - a)
\end{align}
$$

En conclusión, existe una única transformación lineal que verifica las condiciones dadas, y tiene la siguiente forma:
$$
T(c + bx + ax^{2}) = (c - a, b - a)
$$

---
## Ejercicio 4

### Parte a)
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}
$$
tal que
$$
\begin{align}
&T(1, 1, -1) = (2, 1, 0) \\
&T(1, 2, 1) = (-1, 2, 3) \\
&T(1, 0, -3) = (0, 0, 1)
\end{align}
$$
Probemos desarrollar la expresión analítica de la transformación lineal:
$$
\begin{align}
T(x, y, z) = T(x(1, 0, 0)) + T(y(0, 1, 0)) + T(z(0, 0, 1))
\end{align}
$$
Primero, determinemos si el conjunto provisto $\{ (1, 1, -1), (1, 2, 1), (1, 0, -3) \}$ es base de $\mathbb{R}^{3}$.
$$
\begin{cases}
\alpha + \beta + \gamma = 0 \\
\alpha + 2\beta = 0 \\
-\alpha + \beta - 3\gamma = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
1 & 2 & 0 & 0 \\
-1 & 1 & -3 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
0 & 1 & -1 & 0 \\
0 & 2 & -2 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
0 & 1 & -1 & 0 \\
0 & 1 & -1 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{2}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
0 & 1 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 2 & 0 \\
0 & 1 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
Como vemos, logramos anular una fila, por lo que el conjunto no es LI (no es base). Identificamos que el vector $(1, 0, -3)$ se puede conformar con los otros:
$$
\begin{align}
(1, 0, -3) &= 2(1, 1, -1) - (1, 2, 1) \\
&= (2, 2, -2) - (1, 2, 1) \\
&= (2 - 1, 2 - 2, -2 - 1) \\
&= (1, 0, -3)
\end{align}
$$

Sabiendo esto, verifiquemos que la definición que las condiciones establecidas tengan sentido:
$$
(1, 0, -3) = 2(1, 1, -1) - (1, 2, 1) \implies T(1, 0, -3) = T(2(1, 1, -1) - (1, 2, 1))
$$
$$
\begin{align}
T(1, 0, -3) &= T(2(1, 1, -1) - (1, 2, 1)) \\
&= 2T(1, 1, -1) - T(1, 2, 1) \\
&= 2(2, 1, 0) - (-1, 2, 3) \\
&= (4, 2, 0) - (-1, 2, 3) \\
&= (4 + 1, 2 - 2, 0 - 3) \\
&= (5, 0, -3) \\
&\neq (0, 0, 1)
\end{align}
$$

En conclusión, no existe ninguna transformación lineal que cumpla con las condiciones dadas.

### Parte b)
$$
T : \mathcal{M}_{2 \times 2}(\mathbb{R}) \to \mathbb{R}^{2}
$$
tal que
$$
\begin{align}
&T(M_{1}) = (1, -1) \\
&T(M_{2}) = (1, 1) \\
&T(M_{3}) = (1, 1) \\
&T(M_{4}) = (3, 1) \\
&T(M_{5}) = (1, -3)
\end{align}
$$
donde
$$
M_{1} = \begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix}, M_{2} = \begin{pmatrix}
1 & 0 \\
-1 & 2
\end{pmatrix}, M_{3} = \begin{pmatrix}
1 & 2 \\
1 & -1
\end{pmatrix}, M_{4} = \begin{pmatrix}
3 & 3 \\
1 & 2
\end{pmatrix}, M_{5} = \begin{pmatrix}
1 & 0 \\
1 & 3
\end{pmatrix}
$$
Primero, observamos las matrices provistas y verificamos si alguna se puede formar por combinación lineal de los demás. En este caso, como trabajamos en $\mathcal{M}_{2 \times 2}$, $dim(\mathcal{M}_{2 \times 2}) = 4$, por lo que al tener 5 elementos, necesariamente no es LI (al menos uno es redundante).

Simplemente con observar los elementos, podemos ver que:
$$
\begin{pmatrix}
1 & 0 \\
1 & 3
\end{pmatrix} = 2\begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix} - \begin{pmatrix}
1 & 2 \\
1 & -1
\end{pmatrix} = \begin{pmatrix}
2 - 1 & 2 - 2 \\
2 - 1 & 2 + 1
\end{pmatrix} = \begin{pmatrix}
1 & 0 \\
1 & 3
\end{pmatrix}
$$
Así, podemos utilizarlo para determinar la validez de la transformación lineal:
$$
\begin{align}
T(M_{5}) &= T(2M_{1} - M_{3}) \\
&= 2T(M_{1}) - T(M_{3}) \\
&= 2(1, -1) - (1, 1) \\
&= (2, -2) - (1, 1) \\
&= (2 - 1, -2 - 1) \\
&= (1, -3)
\end{align}
$$

Si volvemos a analizar las matrices restantes, podemos ver que el conjunto aún no es LI, ya que la matriz $M_{4}$ se puede expresar como combinación lineal de las restantes:
$$
\begin{pmatrix}
3 & 3 \\
1 & 2
\end{pmatrix} = \begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix} + \begin{pmatrix}
1 & 0 \\
-1 & 2
\end{pmatrix} + \begin{pmatrix}
1 & 2 \\
1 & -1
\end{pmatrix} = \begin{pmatrix}
1 + 1 + 1 & 1 + 0 + 2 \\
1 - 1 + 1 & 1 + 2 - 1
\end{pmatrix} = \begin{pmatrix}
3 & 3 \\
1 & 2
\end{pmatrix}
$$
$$
\begin{align}
T(M_{4}) &= T(M_{1} + M_{2} + M_{3}) \\
&= T(M_{1}) + T(M_{2}) + T(M_{3}) \\
&= (1, -1) + (1, 1) + (1, 1) \\
&= (1 + 1 + 1, -1 + 1 + 1) \\
&= (3, 2)
\end{align}
$$

Comprobamos que las condiciones establecidas tienen sentido, de forma que existe al menos una transformación lineal con dichas características.

Ahora, podemos determinar lo siguiente:
Dado que el conjunto $\{ M_{1}, M_{2}, M_{3}, M_{4}, M_{5} \}$ solo tiene tres matrices LI (puesto que $M_{4}$ y $M_{5}$ se forman por combinación lineal del resto), el conjunto tiene cardinal 3, y considerando que estamos trabajando en el espacio $\mathcal{M}_{2 \times 2}$, el cual cumple que $dim(\mathcal{M}_{2 \times 2}) = 4$, podemos confirmar que el conjunto no es un generador de $\mathcal{M}_{2 \times 2}$. Por lo tanto, no podemos determinar cuánto vale $T$ en todo el espacio.

De esta manera, no es posible hallar una única expresión analítica que determine a los espacios que cumplen las condiciones dadas, ya que existe infinitas transformaciones lineales que las satisfacen.

---
# Núcleo e imagen de una transformación lineal
## Ejercicio 5
### Parte a)
$$
T : \mathbb{R}_{3}[x] \to \mathbb{R}^{2}
$$
tal que
$$
T(p) = (p(1) + p(-1), p(0))
$$
Comenzamos por estudiar el núcleo:
$$
p \in \mathrm{Ker}(T) \Longleftrightarrow \begin{cases}
p(1) + p(-1) = 0 \\
p(0) = 0
\end{cases}
$$
Entonces, tenemos que encontrar polinomios de tercer grado que cumplan que:
$$
\begin{cases}
p(1) + p(-1) = 0 \\
p(0) = 0
\end{cases}
$$
Consideremos un polinomio de grado 3 genérico: $ax^{3} + bx^{2} + cx + d$.
- Si $p(0) = 0 \implies d = 0$.
- Si
$$
\begin{align}
p(1) + p(-1) = 0 \implies \cancel{ a } + b + \cancel{ c } + d + (\cancel{ -a } + b - \cancel{ c } + d) &= 0 \\
2b + 2d &= 0
\end{align}
$$
Como $d = 0 \implies 2b = 0 \implies b = 0$. De esta manera, solo nos quedamos con los polinomios de forma $ax^{3} + cx$

Entonces, podemos definir al núcleo:
$$
\mathrm{Ker}(T) = \{ ax^{3} + cx : a, c \in \mathbb{R} \}
$$
Ahora, podemos definir una base de $\mathrm{Ker}(T)$:
$$
\{ x^{3}, x \}
$$
es base de $\mathrm{Ker}(T)$.

Pasamos a analizar la imagen:

Para que $(\alpha, \beta) \in \mathrm{Im}(T)$, tiene que cumplirse que
$$
\begin{cases}
\alpha = p(1) + p(-1) \\
\beta = p(0)
\end{cases}
$$
para algún $p \in \mathbb{R}_{3}[x]$.

Nuevamente,  un polinomio de grado 3 genérico: $ax^{3} + bx^{2} + cx + d$.
$$
\begin{cases}
\alpha = a + b + c + d + (-a + b - c + d) \\
\beta = d
\end{cases}
$$
$$
\begin{align}
\alpha &= a + b + c + d + (-a + b - c + d) \\
&= \cancel{ a } + b + \cancel{ c } + d - \cancel{ a } + b - \cancel{ c } + d \\
&= b + d + b + d \\
&= 2b + 2d
\end{align}
$$
$$
\implies \begin{cases}
\alpha = 2b + 2d \\
\beta = d
\end{cases}
$$
Entonces, definimos la imagen:
$$
\begin{align}
\mathrm{Im}(T) &= \{ (2b + 2d, d) : b, d \in \mathbb{R} \} \\
&= \{ b(2, 0) + d(2, 1) : b, c \in \mathbb{R} \}
\end{align}
$$
Ahora, podemos definir una base de $\mathrm{Im}(T)$:
$$
\{ (2, 0), (2, 1) \}
$$
es base de $\mathrm{Im}(T)$.

### Parte c)

$$
T : \mathcal{M}_{2 \times 2}(\mathbb{C}) \to \mathbb{C}^{2}
$$
tal que
$$
T \begin{pmatrix}
z_{1} & z_{2} \\
z_{3} & z_{4}
\end{pmatrix} = (z_{1} + iz_{2}, 0)
$$
Comenzamos por estudiar el núcleo:
$$
\begin{pmatrix}
z_{1} & z_{2} \\
z_{3} & z_{4}
\end{pmatrix} \in \mathrm{Ker}(T) \Longleftrightarrow z_{1} = -iz_{2} \implies \begin{pmatrix}
z_{1} & z_{2} \\
z_{3} & z_{4}
\end{pmatrix} = \begin{pmatrix}
-iz_{2} & z_{2} \\
z_{3} & z_{4}
\end{pmatrix}
$$
Entonces, podemos definir al núcleo:
$$
\begin{align}
\mathrm{Ker}(T) &= \left\{ \begin{pmatrix}
-iz_{2} & z_{2} \\
z_{3} & z_{4}
\end{pmatrix} : z_{2}, z_{3}, z_{4} \in \mathbb{C} \right\} \\
&= \left\{ z_{2}\begin{pmatrix}
-i & 1 \\
0 & 0
\end{pmatrix} + z_{3}\begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} + z_{4}\begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} : z_{2}, z_{3}, z_{4} \in \mathbb{C} \right\}
\end{align}
$$
Ahora, podemos definir una base de $\mathrm{Ker}(T)$:
$$
\left\{ \begin{pmatrix}
-i & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\}
$$
es base de $\mathrm{Ker}(T)$.

Pasamos a analizar la imagen:

Para que $(\alpha, \beta) \in \mathrm{Im}(T)$, tiene que cumplirse que
$$
\begin{cases}
\alpha = z_{1} + iz_{2} \\
\beta = 0
\end{cases}
$$
para algún $\begin{pmatrix} z_{1} & z_{2} \\ z_{3} & z_{4} \end{pmatrix} \in \mathcal{M}_{2 \times 2}(\mathbb{C})$.

Entonces, definimos la imagen:
$$
\begin{align}
\mathrm{Im}(T) &= \{ (z_{1} + iz_{2}, 0) : z_{1}, z_{2} \in \mathbb{C} \} \\
&= \{ z_{1}(1, 0) + z_{2}(i, 0) : z_{1}, z_{2} \in \mathbb{C} \}
\end{align}
$$
Ahora, podemos definir una base de $\mathrm{Im}(T)$:
$$
\{ (1, 0), (i, 0) \} = \{ (1, 0) \}
$$
es base de $\mathrm{Im}(T)$.

ACLARACIÓN: Siempre es bueno verificar aplicando la fórmula del teorema de las dimensiones.

---
## Ejercicio 6
Comenzamos por $T$:

Probamos que el nulo lleva al nulo:
$$
T(0, 0, 0) = \begin{pmatrix}
0 - 0 & 0 \\
0 & 0 - 0
\end{pmatrix} = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix}
$$


Estudiamos el núcleo de $T$:
$$
(x, y, z) \in \mathrm{Ker}(T) \Longleftrightarrow \begin{cases}
x - y = 0 \\
y = 0 \\
\cancel{ y = 0 } \\
y - z = 0
\end{cases}
$$
$$
\begin{align}
y = 0 &\implies x = 0 \\
&\implies -z = 0 \implies z = 0
\end{align}
$$
Como vemos, el único vector que parece pertenecer al núcleo es el vector nulo $(0, 0, 0)$.

De esta forma:
$$
\mathrm{Ker}(T) = \{ 0 \}
$$
Pasamos a la imagen de $T$:
$$
\begin{pmatrix}
\alpha & \beta \\
\gamma & \mu
\end{pmatrix} \in \mathrm{Im}(T) \Longleftrightarrow \exists (x, y, z) \text{ tal que } T(x, y, z) = \begin{pmatrix}
\alpha & \beta \\
\gamma & \mu
\end{pmatrix}
$$
Esto significa que:
$$
\begin{cases}
\alpha = x - y \\
\beta = y \\
\gamma = y \\
\mu = y - z
\end{cases}
$$
$$
\begin{align}
\beta = \gamma = y &\implies \alpha + \beta = x \\
&\implies \mu - \beta = -z \implies \beta - \mu = z
\end{align}
$$
Entonces, definimos la imagen:
$$
\begin{align}
\mathrm{Im}(T) &= \{  : z_{1}, z_{2} \in \mathbb{C} \} \\
&= \{ z_{1}(1, 0) + z_{2}(i, 0) : z_{1}, z_{2} \in \mathbb{C} \}
\end{align}
$$
Ahora, podemos definir una base de $\mathrm{Im}(T)$:
$$
\{ (1, 0), (i, 0) \} = \{ (1, 0) \}
$$
es base de $\mathrm{Im}(T)$.



---
## Ejercicio 7




---
# Teorema de las dimensiones
## Ejercicio 8









---
## Ejercicio 10





---
## Ejercicio 11
Tres partes.