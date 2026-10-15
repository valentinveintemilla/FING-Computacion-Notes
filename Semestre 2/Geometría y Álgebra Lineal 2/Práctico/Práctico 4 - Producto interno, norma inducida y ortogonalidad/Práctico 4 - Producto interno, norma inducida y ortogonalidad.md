# 1 - Producto interno y norma inducida
## Ejercicio 1
En este caso, tenemos que probar las cuatro propiedades de producto interno para cada una de las operaciones propuestas:
1. $\langle u + w, v \rangle = \langle u, v \rangle + \langle w, v \rangle, \forall u, v, w \in V$ (aditividad con respecto a la primera componente)
2. $\langle \alpha \cdot u, v \rangle = \alpha \cdot \langle u, v \rangle, \forall \alpha \in \mathbb{K}, \forall u, v, w \in V$ (homogeneidad con respecto a la primera componente, junto con la 1 forman la linealidad)
3. $\langle u, v \rangle = \overline{\langle v, u \rangle}, \forall u, v \in V$ (simetría)
4. $\langle v, v \rangle \geq 0, \forall v \in V$, $\langle v, v \rangle = 0 \Longleftrightarrow v = \vec{0}$ (no negatividad)

### Parte 1
1. Aditividad con respecto a la primera componente:
$$
\begin{align}
f((x_{1}, y_{1}, z_{1}) + (x_{2}, y_{2}, z_{2}), (x', y', z')) &= f((x_{1} + x_{2}, y_{1} + y_{2}, z_{1} + z_{2}), (x', y', z')) \\
&= (x_{1} + x_{2})x' + 2(y_{1} + y_{2})y' + 3(z_{1} + z_{2})z' \\
&= x_{1}x' + x_{2}x' + 2y_{1}y' + 2y_{2}y' + 3z_{1}z' + 3z_{2}z' \\
&= x_{1}x' + 2y_{1}y' + 3z_{1}z' + x_{2}x' + 2y_{2}y' + 3z_{2}z' \\
&= f((x_{1}, y_{1}, z_{1}), (x', y', z')) + f((x_{2}, y_{2}, z_{2}), (x', y', z'))
\end{align}
$$

2. Homogeneidad con respecto a la primera componente:
$$
\begin{align}
f(\alpha \cdot (x, y, z), (x', y', z')) &= f((\alpha \cdot x, \alpha \cdot y, \alpha \cdot z), (x', y', z')) \\
&= \alpha \cdot xx' + 2\alpha \cdot yy' + 3\alpha \cdot zz' \\
&= \alpha \cdot (xx' + 2yy' + 3zz') \\
&= \alpha \cdot f((x, y, z), (x', y', z'))
\end{align}
$$

3. Simetría:
$$
\begin{align}
f((x, y, z), (x', y', z')) &= xx' + 2yy' + 3zz' \\
&= x'x + 2y'y + 3z'z \\
&= f((x', y', z'), (x, y, z))
\end{align}
$$
No fue necesario operar con el conjugado, ya que estamos en $\mathbb{R}$.

4. No negatividad:
$$
\begin{align}
f((x, y, z), (x, y, z)) &= xx + 2yy + 3zz \\
&= x^{2} + 2y^{2} + 3z^{2} \geq 0?
\end{align}
$$
$$
a^{2} \geq 0 \forall a \in \mathbb{R} \implies f((x, y, z), (x, y, z)) \geq 0 \space \forall (x, y, z) \in \mathbb{R}^{3}
$$
$$
f((x, y, z), (x, y, z)) = 0 \Longleftrightarrow (x, y, z) = (0, 0, 0)?
$$
$$
f((x, y, z), (x, y, z)) = 0 \implies x^{2} + 2y^{2} + 3z^{2} = 0
$$
Como $x^{2}, y^{2}, z^{2} \geq 0, \forall x, y, z \in \mathbb{R}$, entonces $x^{2}, y^{2}, z^{2} = 0 \Longleftrightarrow x = y = z = 0$

### Parte 2
$$
\begin{pmatrix}
x & y
\end{pmatrix} \cdot \begin{pmatrix}
1 & i \\
-i & 2
\end{pmatrix} \cdot \begin{pmatrix}
\overline{x'} \\
\overline{y'}
\end{pmatrix} = \begin{pmatrix}
x & y
\end{pmatrix} \cdot \begin{pmatrix}
\overline{x'} + \overline{y'}i \\
-\overline{x'}i + 2\overline{y'}
\end{pmatrix} = x\overline{x'} + x\overline{y'}i - y\overline{x'}i + 2y\overline{y'}
$$
1. Aditividad con respecto a la primera componente:
$$
\begin{align}
f((x_{1}, y_{1}) + (x_{2}, y_{2}), (x', y')) &= f((x_{1} + x_{2}, y_{1} + y_{2}), (x', y')) \\
&= (x_{1} + x_{2})\overline{x'} + (x_{1} + x_{2})\overline{y'}i - (y_{1} + y_{2})\overline{x'}i + 2(y_{1} + y_{2})\overline{y'} \\
&= x_{1}\overline{x'} + x_{1}\overline{y'}i - y_{1}\overline{x'}i + 2y_{1}\overline{y'} + x_{2}\overline{x'} + x_{2}\overline{y'}i - y_{2}\overline{x'}i + 2y_{2}\overline{y'} \\
&= f((x_{1}, y_{1}), (x', y')) + f((x_{2}, y_{2}), (x', y'))
\end{align}
$$

2. Homogeneidad con respecto a la primera componente:
$$
\begin{align}
f(\alpha \cdot (x, y), (x', y')) &= f((\alpha \cdot x, \alpha \cdot y), (x', y')) \\
&= \alpha \cdot x\overline{x'} + \alpha \cdot x\overline{y'}i - \alpha \cdot y\overline{x'}i + \alpha \cdot 2y\overline{y'} \\
&= \alpha \cdot (x\overline{x'} + x\overline{y'}i - y\overline{x'}i + 2y\overline{y'}) \\
&= \alpha \cdot f((x, y), (x', y'))
\end{align}
$$

3. Simetría:
$$
\begin{align}
f((x, y), (x', y')) &= x\overline{x'} + x\overline{y'}i - y\overline{x'}i + 2y\overline{y'} \\
&= \overline{\overline{x\overline{x'} + x\overline{y'}i - y\overline{x'}i + 2y\overline{y'}}} \\
&= \overline{x'\overline{x} - y'\overline{x}i + x'\overline{y}i + 2y'\overline{y}} \\
&= \overline{x'\overline{x} + x'\overline{y}i - y'\overline{x}i + 2y'\overline{y}} \\
&= \overline{f((x', y'), (x, y))}
\end{align}
$$

4. No negatividad:
$$
\begin{align}
f((x, y), (x, y)) &= x\overline{x} + x\overline{y}i - y\overline{x}i + 2y\overline{y} \\
&= |x|^{2} + x\overline{y}i - y\overline{x}i + 2|y|^{2} \geq 0?
\end{align}
$$
$$
\begin{align}
x = a + bi \land y = c + di &\implies |x|^{2} = a^{2} + b^{2} \\
&\implies x\overline{y}i = (ac - adi + bci + bd)i = (aci + ad - bc + bdi) \\
&\implies y\overline{x}i = (ac + adi - bci + bd)i = (aci - ad + bc + bdi) \\
&\implies 2|y|^{2} = 2c^{2} + 2d^{2}
\end{align}
$$
Ahora, unimos los resultados:
$$
\begin{align}
|x|^{2} + x\overline{y}i - y\overline{x}i + 2|y|^{2} &= a^{2} + b^{2} + \cancel{ aci } + ad - bc + \cancel{ bdi } - \cancel{ aci } + ad - bc - \cancel{ bdi } + 2c^{2} + 2d^{2} \\
&= a^{2} + b^{2} + 2ad - 2bc + 2c^{2} + 2d^{2} \\
&= (a^{2} + 2ad + d^{2}) + d^{2} + (b^{2} - 2bc + c^{2}) + c^{2} \\
&= (a + d)^{2} + d^{2} + (b - c)^{2} + c^{2}
\end{align}
$$
Como todos los términos están elevados al cuadrado, podemos deducir que:
$$
f((x, y), (x, y)) \geq 0 \space \forall (x, y) \in \mathbb{C}^{2}
$$
Ahora, tenemos que verificar que solo se anule para el vector nulo:
$$
f((x, y), (x, y)) = 0 \Longleftrightarrow (x, y) = (0, 0)?
$$
$$
f((x, y), (x, y)) = 0 \implies x\overline{x} + x\overline{y}i - y\overline{x}i + 2y\overline{y} = 0
$$
Como $x = \overline x = y = \overline y = 0$, entonces $x\overline{x} = x\overline{y}i = -y\overline{x}i = 2y\overline{y} = 0 \Longleftrightarrow x = y = 0$

### Parte 3
1. Aditividad con respecto a la primera componente:
$$
\begin{align}
f(A + A', B) &= tr((A + A')B^{t}) \\
&= tr(AB^{t} + A'B^{t}) \\
&= tr(AB^{t}) + tr(A'B^{t}) \\
&= f(A, B) + f(A', B)
\end{align}
$$

2. Homogeneidad con respecto a la primera componente:
$$
\begin{align}
f(\alpha \cdot A, B) &= tr((\alpha \cdot A)B^{t}) \\
&= tr(\alpha \cdot (AB^{t})) \\
&= \alpha \cdot tr(AB^{t}) \\
&= \alpha \cdot f(A, B)
\end{align}
$$

3. Simetría:
$$
\begin{align}
f(A, B) &= tr(AB^{t}) \\
&= tr(B^{t}A) \\
&= tr((B^{t}A)^{t}) \\
&= tr(BA^{t}) \\
&= f(B, A)
\end{align}
$$

4. No negatividad:
$$
\begin{align}
f(A, A) &= tr(AA^{t}) \geq 0?
\end{align}
$$
Sabemos que la traza de una matriz cuadrada por su traspuesta es:
$$
tr(AA^{t}) = \sum_{i = 1}^{n} \sum_{j = 1}^{n} (a_{ij})^{2}
$$
Ya que si lo representamos:
$$
\begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \dots & a_{nn}
\end{pmatrix} \cdot \begin{pmatrix}
a_{11} & a_{21} & \dots & a_{n_{1}} \\
a_{12} & a_{22} & \dots & a_{n2} \\
\vdots & \vdots & \ddots & \vdots \\
a_{1n} & a_{2n} & \dots & a_{nn}
\end{pmatrix} = \begin{pmatrix}
a_{11}^{2} + a_{12}^{2} + \dots + a_{1_{n}}^{2} & \dots & \dots & \dots \\
\vdots & a_{21}^{2} + a_{22}^{2} + \dots + a_{2n}^{2} & \dots & \vdots \\
\vdots & \vdots & \ddots & \vdots \\
\dots & \dots & \dots & a_{n1}^{2} + a_{n2}^{2} + \dots + a_{nn}^{2}
\end{pmatrix}
$$
Entonces, como estamos sumando elementos elevados al cuadrado, estos serán siempre positivos o nulos, lo que verifica la propiedad.

Ahora, tenemos que verificar que solo se anule para el vector nulo:
$$
f(A, A) = 0 \Longleftrightarrow A = O?
$$
Como
$$
f(A, A) = tr(AA^{t}) = \sum_{i = 1}^{n} \sum_{j = 1}^{n} (a_{ij})^{2}
$$
Como todos los términos están elevados al cuadrado, la única forma de que la suma total sea 0 es que todos sean 0. Por lo tanto:
$$
f(A, A) = 0 \Longleftrightarrow A = O
$$

---
## Ejercicio 2
En este caso, solo es necesario verificar que no se cumple una de las propiedades mencionadas para verificar que las operaciones no son un producto interno:

### Parte 1
En este caso, basta con ver que el producto interno se anula con elementos que no son el polinomio 0:
$$
f(p, q) = p(1)p(1) = p(1)^{2} = 0 \Longleftrightarrow p = O
$$
Podemos ver que el polinomio nulo cumple dicha condición. Sin embargo, podemos tomar otro polinomio que tenga raíz en 1 y no sea el polinomio nulo, por ejemplo: $p = x - 1$

Dicho polinomio cumple que $p(1) = 0 \implies p(1)^{2} = 0$.

Por lo tanto, $f(p, q) = p(1)p(1)$ no es un producto interno en $V$.

### Parte 2
Verifiquemos la no negatividad de la operación: consideremos lo que sucede con un vector cuyos componentes sean negativos (basta con que uno de los dos componentes sea negativo y su valor absoluto sea mayor al del otro).
$$
f((x, y), (x, y)) = x|x| + y|y|
$$
Al estar definida con valores absolutos, el signo de cada valor se mantiene, por lo que>
- Si $x, y < 0$, el resultado será negativo.
- Si $x \leq 0, y \geq 0$, pero $|x| \geq y$, entonces el resultado será negativo o nulo (sin que $x = y = 0$ necesariamente).

En conclusión, la operación no es un producto interno.

### Parte 3
Esta operación se corresponde con el cálculo del determinante de una matriz de la forma
$$
\begin{pmatrix}
a & b \\
d & c
\end{pmatrix}
$$

Fácilmente, podemos encontrar casos que no cumplan la no negatividad del producto interno, por ejemplo:
$$
f((1, 1), (1, 1)) = 1 \cdot 1 - 1 \cdot 1 = 0
$$
También podríamos buscar cualquier otra combinación que de como resultado 0, sin tratarse del vector nulo.

En conclusión, la operación no es un producto interno, ya que no cumple con la propiedad 4: no negatividad (y nulidad solo con el vector nulo).

### Parte 4
En este caso, basta con seleccionar dos matrices tal que la traza de su suma sea 0 (o incluso negativa). De esta forma, probaríamos que la operación no es un producto interno.

Por ejemplo, consideramos la matriz $A$, tal que $tr(A) \leq 0$:
$$
f(A, A) = tr(A + A) = tr(2A) = 2 \cdot \underbrace{ tr(A) }_{ \leq 0 } \implies f(A, A) \leq 0
$$
Sin embargo, en caso de que la matriz $A$ no sea $O$, estaríamos incumpliendo la propiedad 4 (no negatividad y nulidad únicamente para la matriz $O$).

En conclusión, la operación propuesta no es un producto interno correctamente definido.

### Parte 5
En este caso, verifiquemos la nulidad solo para $u = 0$: definamos una función continua, nula en el intervalo $\left[ 0, \frac{1}{2} \right]$, y no nula en el intervalo $\left[ \frac{1}{2}, 1 \right]$:
$$
u(x) = \begin{cases}
0 \text{ si } x \in \left[ 0, \frac{1}{2} \right] \\
x - \frac{1}{2} \text{ si } x \in \left[ \frac{1}{2}, 1 \right]
\end{cases}
$$
Si determinamos el producto interno de dicha función consigo misma:
$$
f(u, u) = \int_{0}^{\frac{1}{2}} u(t)u(t) dt = \int_{0}^{\frac{1}{2}} u^{2}(t) dt = 0
$$
Sin embargo, la función no es nula.

En conclusión, la operación definida no es un producto interno, ya que incumple la propiedad de no negatividad y nulidad exclusiva para el vector nulo (consigo mismo).

---
## Ejercicio 3
### Parte 1
Probemos que la afirmación es correcta.

Sabemos, por definición de producto interno, que:
$$
\langle u + v, w \rangle = \langle u, w \rangle + \langle v, w \rangle, \forall u, v, w \in V
$$
y
$$
\langle \alpha \cdot u, v \rangle = \alpha \cdot \langle u, v \rangle, \forall \alpha \in \mathbb{K}, \forall u, v \in V
$$
Ahora, probemos que también se cumple para la segunda componente. Para ello, tendremos que aplicar diferentes propiedades del producto interno:
$$
\langle u, v + w \rangle = \overline{\langle v + w, u \rangle} = \overline{\langle v, u \rangle + \langle w, u \rangle} = \overline{\langle v, u \rangle} + \overline{\langle w, u \rangle} = \langle u, v \rangle + \langle u, w \rangle
$$
Pasamos a probar la homogeneidad con respecto a la segunda componente:
$$
\langle u, \alpha \cdot v \rangle = \overline{\langle \alpha \cdot v, u \rangle} = \overline{\alpha \cdot \langle v, u \rangle} = \overline{\alpha} \cdot \overline{\langle v, u \rangle} = \overline{\alpha} \cdot \langle u, v \rangle
$$
Con esto, probamos que el producto interno es lineal en ambas componentes, por lo que el enunciado es verdadero.

### Parte 2
Para verificar el enunciado, tenemos que desarrollar la expresión:
$$
\begin{align}
\langle v_{1} + v_{2}, w_{1} + w_{2} \rangle &= \langle v_{1}, w_{1} + w_{2} \rangle + \langle v_{2}, w_{1} + w_{2} \rangle \\
&= \langle v_{1}, w_{1} \rangle + \langle v_{1}, w_{2} \rangle + \langle v_{2}, w_{1} \rangle + \langle v_{2}, w_{2} \rangle
\end{align}
$$
Como vemos,
$$
\langle v_{1} + v_{2}, w_{1} + w_{2} \rangle = \langle v_{1}, w_{1} \rangle + \langle v_{1}, w_{2} \rangle + \langle v_{2}, w_{1} \rangle + \langle v_{2}, w_{2} \rangle \neq \langle v_{1}, w_{1} \rangle + \langle v_{2}, w_{2} \rangle
$$
por lo que el enunciado es falso.

### Parte 3
Nuevamente, aplicamos las propiedades conocidas del producto interno:
$$
\langle v, w \rangle = 0, \forall w \in V
$$
Entonces, también pasa cuando $w = v$, por lo que:
$$
\langle v, v \rangle = 0 \Longleftrightarrow v = \vec{0}
$$
De esta manera, probamos que necesariamente $v = \vec{0}$ en el caso $w = v$. Si evaluamos el caso general, sabiendo que $v = \vec{0}$:
$$
\langle v, w \rangle = \langle \vec{0}, w \rangle = \langle 0 \cdot v, w \rangle = 0 \cdot \langle v, w \rangle = 0
$$

En conclusión, el enunciado es verdadero.

---
## Ejercicio 4
### Parte 1
Sea $A := (a_{ij}) \in M_{n}(\mathbb{R})$ una matriz, y $\vec{X} = \begin{pmatrix} x_{1} \\ \vdots \\ x_{n} \end{pmatrix}$ y $\vec{Y} = \begin{pmatrix} y_{1} \\ \vdots \\ y_{n} \end{pmatrix}$ dos vectores de $\mathbb{R}^{n}$ cualesquiera.

Si consideramos $\mathcal{E} = \{ e_{1}, \dots, e_{n} \}$ base canónica de $\mathbb{R}^{n}$, podemos expresar a los vectores previos como $\vec{X} = \sum_{i = 1}^{n} x_{i} \cdot e_{i}$ y $\vec{Y} = \sum_{j = 1}^{n} y_{j} \cdot e_{j}$.

Entonces, si aplicamos la definición de producto interno habitual en $\mathbb{R}^{n}$:
$$
\langle u, v \rangle = \sum_{i = 1}^{n} \sum_{j = 1}^{n} u_{i} \cdot v_{j}
$$
podemos expresar el producto interno entre $\vec{X}$ y $\vec{Y}$:
$$
\begin{align}
\langle \vec{X}, \vec{Y} \rangle &= \left\langle \sum_{i = 1}^{n} x_{i} \cdot e_{i}, \sum_{j = 1}^{n} y_{j} \cdot e_{j} \right\rangle \\
&\underbrace{ = }_{ 1 } \sum_{i = 1}^{n} x_{i} \langle e_{i}, \sum_{j = 1}^{n} y_{j} \cdot e_{j} \rangle \\
&\underbrace{ = }_{ 2 } \sum_{i = 1}^{n} \sum_{j = 1}^{n} x_{i} \cdot y_{j} \langle e_{i}, e_{j} \rangle
\end{align}
$$
1. Linealidad con respecto a primera componente.
2. Linealidad con respecto a segunda componente.

Si bien no sabemos como está definido el producto interno, sabemos que da como resultado un valor real no negativo, por lo que $\langle e_{i}, e_{j} \rangle \geq 0, \forall i, j = 1, \dots, n$. Entonces, denotamos a dichos valores como coeficientes $a_{ij} = \langle e_{i}, e_{j} \in \mathbb{R}, \forall i, j = 1, \dots, n$. De esta manera, podemos expresar el producto interno como:
$$
\begin{align}
\langle \vec{X}, \vec{Y} \rangle &= \sum_{i = 1}^{n} \sum_{j = 1}^{n} x_{i} \cdot y_{j} \langle e_{i}, e_{j} \rangle \\
&= \sum_{i = 1}^{n} \sum_{j = 1}^{n} a_{ij} \cdot x_{i} \cdot y_{j} \\
&= a_{11} \cdot x_{1} \cdot y_{1} + \dots + a_{1n} \cdot x_{1} \cdot y_{n} \\
&+ a_{21} \cdot x_{2} \cdot y_{1} + \dots + a_{2n} \cdot x_{2} \cdot y_{n} \\
&+ \dots \\
&+ a_{n1} \cdot x_{n} \cdot y_{1} + \dots + a_{nn} \cdot x_{n} \cdot y_{n}
\end{align}
$$
Si aplicamos factor común:
$$
\begin{align}
&= x_{1} \cdot (a_{11} \cdot y_{1} + \dots + a_{1n} \cdot y_{n}) \\
&+ x_{2} \cdot (a_{21} \cdot y_{1} + \dots + a_{2n} \cdot y_{n}) \\
&+ \dots \\
&+ x_{n} \cdot (a_{n1} \cdot y_{1} + \dots + a_{nn} \cdot y_{n}) \\
&= \sum_{i = 1}^{n} x_{i} \cdot \sum_{j = 1}^{n} a_{ij} \cdot y_{j}
\end{align}
$$
Ahora, podemos ver que la operación $\sum_{j = 1}^{n} a_{ij} \cdot y_{j}$ se corresponde con un producto entre matrices, donde $(a_{ij}), i, j = 1, \dots, n$ es una matriz cuadrada de tamaño $n$, a la cual llamaremos $A$, y $(y_{j}), j = 1, \dots, n$ es una matriz columna. De esta manera:
$$
\sum_{j = 1}^{n} a_{ij} \cdot y_{j} = A \cdot \vec{Y}
$$
Esto da como resultado una matriz columna de tamaño $n$. Por otra parte, el factor $\sum_{i = 1}^{n} x_{i}$ se corresponde con una matriz fila (puesto que de otra forma el producto no sería posible), con los coeficientes de la matriz $\vec{X}$. Para esto, podemos trasponer la matriz $\vec{X}$.

En conclusión, podemos expresar el producto interno de los vectores $\vec{X}$ y $\vec{Y}$ como el producto de las siguientes matrices:
$$
\langle \vec{X}, \vec{Y} \rangle = \sum_{i = 1}^{n} \sum_{j = 1}^{n} a_{ij} \cdot x_{i} \cdot y_{j} = \sum_{i = 1}^{n} x_{i} \cdot \sum_{j = 1}^{n} a_{ij} \cdot y_{j} = \vec{X}^{t} \cdot A \cdot \vec{Y}
$$

### Parte 2
Si consideramos que $A$ es la matriz identidad, la mayoría de los términos se anulan:
$$
\begin{align}
\langle \vec{X}, \vec{Y} \rangle &= \sum_{i = 1}^{n} \sum_{j = 1}^{n} a_{ij} \cdot x_{i} \cdot y_{j} \\
&= a_{11} \cdot x_{1} \cdot y_{1} + \dots + a_{1n} \cdot x_{1} \cdot y_{n} \\
&+ a_{21} \cdot x_{2} \cdot y_{1} + \dots + a_{2n} \cdot x_{2} \cdot y_{n} \\
&+ \dots \\
&+ a_{n1} \cdot x_{n} \cdot y_{1} + \dots + a_{nn} \cdot x_{n} \cdot y_{n} \\
&= x_{1} \cdot y_{1} + x_{2} \cdot y_{2} + \dots + x_{n} \cdot y_{n}
\end{align}
$$
Esta operación se corresponde con el producto interno habitual en $\mathbb{R}^{n}$.

---
## Ejercicio 5



---
## Ejercicio 6
### Parte 1
- $\langle v, w \rangle$
$$
\begin{align}
\langle (2, 1 + i, i), (2 - i, 2, 1 + 2i) \rangle &= 2\overline{(2 - i)} + (1 + i)\overline{2} + i\overline{(1 + 2i)} \\
&= 2(2 + i) + (1 + i)2 + i(1 - 2i) \\
&= 4 + 2i + 2 + 2i + i + 2 \\
&= 8 + 5i
\end{align}
$$
- $||v||^{2}$
$$
\begin{align}
||v||^{2} &= \langle (2, 1 + i, i), (2, 1 + i, i) \rangle \\
&= 2 \cdot 2 + (1 + i)(1 - i) + i \cdot (-i) \\
&= 4 + 1 + 1 + 1 \\
&= 7
\end{align}
$$

- $||w||^{2}$
$$
\begin{align}
||w||^{2} &= \langle (2 - i, 2, 1 + 2i), (2 - i, 2, 1 + 2i) \rangle \\
&= (2 - i)(2 + i) + 2^{2} + (1 + 2i)(1 - 2i) \\
&= 4 + 1 + 4 + 1 + 4 \\
&= 14
\end{align}
$$

- $||v + w||^{2}$
$$
\begin{align}
||v + w||^{2} &= \langle (2, 1 + i, i) + (2 - i, 2, 1 + 2i), (2, 1 + i, i) + (2 - i, 2, 1 + 2i) \rangle \\
&= \langle (4 - i, 3 + i, 1 + 3i), (4 - i, 3 + i, 1 + 3i) \rangle \\
&= (4 - i)(4 + i) + (3 + i)(3 - i) + (1 + 3i)(1 - 3i) \\
&= 16 + 1 + 9 + 1 + 1 + 9 \\
&= 37
\end{align}
$$

Pasamos a analizar las desigualdades de Cauchy-Schwarz y triangular:
- $|\langle v, w \rangle| \leq ||v|| \cdot ||w||$
$$
\begin{align}
|8 + 5i| &\leq \sqrt{ 7 } \cdot \sqrt{ 14 } \\
\sqrt{ 8^{2} + 5^{2} } &\leq \sqrt{ 98 } \\
\sqrt{ 64 + 25 } &\leq \sqrt{ 98 } \\
\sqrt{ 89 } &\leq \sqrt{ 98 }
\end{align}
$$

- $||v + w|| \leq ||v|| + ||w||$
$$
\begin{align}
\sqrt{ 37 } &\leq \sqrt{ 7 } + \sqrt{ 14 } \\
(\sqrt{ 37 })^{2} &\leq (\sqrt{ 7 } + \sqrt{ 14 })^{2} \\
37 &\leq 7 + 2\sqrt{ 7 }\sqrt{ 14 } + 14 \\
37 &\leq 21 + 2\sqrt{ 98 } \\
16 &\leq 2\sqrt{ 98 } \\
\end{align}
$$
Y como $9 < \sqrt{ 98 } < 10 \implies 2\sqrt{ 98 } > 18 > 16$, probamos que $||v + w|| \leq ||v|| + ||w||$.

### Parte 2
- $\langle v, w \rangle$
$$
\begin{align}
\langle t, e^{t} \rangle &= \int_{0}^{1} t \cdot e^{t} dt \\
&= t \cdot e^{t} |_{0}^{1} - e^{t} |_{0}^{1} \\
&= e - (e - 1) \\
&= e - e + 1 \\
&= 1
\end{align}
$$
- $||v||^{2}$
$$
\begin{align}
\langle t, t \rangle &= \int_{0}^{1} t \cdot t dt \\
&= \frac{t^{3}}{3} |_{0}^{1} \\
&= \frac{1}{3}
\end{align}
$$

- $||w||^{2}$
$$
\begin{align}
\langle e^{t}, e^{t} \rangle &= \int_{0}^{1} e^{t} \cdot e^{t} dt \\
&= \frac{e^{2t}}{2} |_{0}^{1} \\
&= \frac{e^{2}}{2} - \frac{e^{0}}{2} \\
&= \frac{e^{2} - 1}{2}
\end{align}
$$

- $||v + w||^{2}$
$$
\begin{align}
||t + e^{t}||^{2} &= \langle t + e^{t}, t + e^{t} \rangle \\
&= \int_{0}^{1} (t \cdot e^{t})^{2} dt \\
&= \int_{0}^{1} t^{2} + 2t \cdot e^{t} + e^{2t} dt \\
&= \int_{0}^{1} t^{2} dt + 2 \cdot \int_{0}^{1} t \cdot e^{t} dt + \int_{0}^{1} e^{2t} dt \\
&= \frac{1}{3} + 2 + \frac{e^{2} - 1}{2} \\
&= \frac{e^{2} + \frac{11}{3}}{2}
\end{align}
$$

Pasamos a analizar las desigualdades de Cauchy-Schwarz y triangular:
- $|\langle v, w \rangle| \leq ||v|| \cdot ||w||$
$$
\begin{align}
|1| &\leq \sqrt{ \frac{1}{3} } \cdot \sqrt{ \frac{e^{2} - 1}{2} } \\
1 &\leq \sqrt{ \frac{e^{2} - 1}{6} }
\end{align}
$$
$e^{2} - 1 > 6$? $e^{2} > 7 \implies \sqrt{ \frac{e^{2} - 1}{6} } > 1$

- $||v + w|| \leq ||v|| + ||w||$
$$
\begin{align}
\sqrt{ \frac{e^{2} + \frac{11}{3}}{2} } &\leq \sqrt{ \frac{1}{3} } + \sqrt{ \frac{e^{2} - 1}{2} } \\
\frac{e^{2} + \frac{11}{3}}{2} &\leq \frac{1}{3} + 2\sqrt{ \frac{e^{2} - 1}{6} } + \frac{e^{2} - 1}{2} \\
e^{2} + \frac{11}{3} &\leq \frac{2}{3} + 4\sqrt{ \frac{e^{2} - 1}{6} } + e^{2} - 1 \\
e^{2} + \frac{11}{3} - e^{2} + 1 - \frac{2}{3} &\leq 4\sqrt{ \frac{e^{2} - 1}{6} } \\
4 &\leq 4\sqrt{ \frac{e^{2} - 1}{6} } \\
1 &\leq \sqrt{ \frac{e^{2} - 1}{6} }
\end{align}
$$
Esta es exactamente la misma desigualdad que probamos en el paso anterior, lo que verifica la desigualdad triangular para el producto interno presentado.

---
# 2 - Conjuntos ortogonales y ortonormales
### Ejercicio 7
### Parte 1
Sabemos que dos vectores son ortogonales si y solo si su producto interno es nulo. De esta forma:
$$
v + w \perp v - w \Longleftrightarrow \langle v + w, v - w \rangle = 0
$$
Entonces, procedemos a desarrollar el producto interno aplicando las propiedades conocidas:
$$
\begin{align}
\langle v + w, v - w \rangle &= \langle v, v - w \rangle + \langle w, v - w \rangle \\
&= \langle v, v \rangle - \overline{\langle v, w \rangle} + \langle w, v \rangle - \overline{\langle w, w \rangle} \\
&= \langle v, v \rangle - \cancel{ \langle w, v \rangle } + \cancel{ \langle w, v \rangle } - \langle w, w \rangle \\
&= ||v||^{2} - ||w||^{2}
\end{align}
$$
Ahora, sabemos que $\langle v + w, v - w \rangle = 0$, y como $\langle v + w, v - w \rangle = ||v||^{2} - ||w||^{2}$, entonces por transitividad, $||v||^{2} - ||w||^{2} = 0$:
$$
\begin{align}
||v||^{2} - ||w||^{2} &= 0 \\
||v||^{2} &= ||w||^{2} \\
||v|| &= ||w||
\end{align}
$$
En conclusión, si $v + w$ y $v - w$ son ortogonales, entonces $v$ y $w$ tienen la misma norma.

### Parte 2
$$
\langle u, v \rangle = 0
$$
Ahora, desarrollamos la norma inducida de la suma de vectores, sabiendo que se corresponde con la raíz del producto interno:
$$
\begin{align}
||u + \lambda v|| &= \sqrt{ \langle u + \lambda v, u + \lambda v \rangle } \\
&= \sqrt{ \langle u, u + \lambda v \rangle + \langle \lambda v, u + \lambda v \rangle } \\
&= \sqrt{ \langle u, u \rangle + \langle u, \lambda v \rangle + \langle \lambda v, u \rangle + \langle \lambda v, \lambda v \rangle } \\
&= \sqrt{ \langle u, u \rangle + \overline{\alpha} \cdot \langle u, v \rangle + \alpha \cdot \langle v, u \rangle + |\alpha|^{2} \cdot \langle v, v \rangle }
\end{align}
$$
Como $u \perp v$, sabemos que $\langle u, v \rangle = 0$, por lo tanto:
$$
\begin{align}
||u + \lambda v|| &= \sqrt{ \langle u, u \rangle + \overline{\alpha} \cdot 0 + \alpha \cdot 0 + |\alpha|^{2} \cdot \langle v, v \rangle } \\
&= \sqrt{ ||u||^{2} + |\alpha|^{2} \cdot ||v||^{2} } \\
||u + \lambda v||^{2} &= ||u||^{2} + |\alpha|^{2} \cdot ||v||^{2} \\
||u + \lambda v||^{2} - |\alpha|^{2} \cdot ||v||^{2} &= ||u||^{2} \\
\sqrt{ ||u + \lambda v||^{2} - |\alpha|^{2} \cdot ||v||^{2} } &= ||u||
\end{align}
$$
Ahora, sabemos que $|\alpha|^{2} \cdot ||v||^{2} \geq 0$, por lo tanto
$$
||u + \lambda v|| = \sqrt{ ||u + \lambda v||^{2} } \geq \sqrt{ ||u + \lambda v||^{2} - |\alpha|^{2} \cdot ||v||^{2} } = ||u|| \implies ||u + \lambda v|| \geq ||u||
$$
De esta manera, por transitividad, probamos que si $u$ y $v$ son ortogonales, entonces $||u + \lambda v|| \geq ||u||, \forall \lambda \in \mathbb{R}$.

---
## Ejercicio 8
Recordemos como funciona el método de Gram-Schmidt:

Comenzamos considerando el producto interno $\langle p, q \rangle$ y el conjunto $\mathcal{B} = \{ v_{1}, \dots, v_{n} \}$ propuestos.
Luego, definimos una base ortogonal $\mathcal{B}_{Og} = \{ w_{1}, \dots, w_{n} \}$ de la siguiente forma:
$$
\begin{align}
w_{1} &= v_{1} \\
w_{2} &= v_{2} - \frac{\langle v_{2}, w_{1} \rangle}{\langle w_{1}, w_{1} \rangle} w_{1} = v_{2} - \frac{\langle v_{2}, w_{1} \rangle}{||w_{1}||^{2}} w_{1} \\
w_{3} &= v_{3} - \frac{\langle v_{3}, w_{2} \rangle}{\langle w_{2}, w_{2} \rangle} w_{2} - \frac{\langle v_{3}, w_{1} \rangle}{\langle w_{1}, w_{1} \rangle} w_{1} = v_{3} - \frac{\langle v_{3}, w_{2} \rangle}{||w_{2}||^{2}} w_{2} - \frac{\langle v_{3}, w_{1} \rangle}{||w_{1}||^{2}} w_{1} \\
&\vdots \\
w_{n} &= v_{n} - \frac{\langle v_{n}, w_{n - 1} \rangle}{\langle w_{n - 1}, w_{n - 1} \rangle} w_{n - 1} - \frac{\langle v_{n}, w_{n - 2} \rangle}{\langle w_{n - 2}, w_{n - 2} \rangle} w_{n - 2} - \dots - \frac{\langle v_{n}, w_{1} \rangle}{\langle w_{1}, w_{1} \rangle} w_{1} \\
&= v_{n} - \frac{\langle v_{n}, w_{n - 1} \rangle}{||w_{n - 1}||^{2}} w_{n - 1} - \frac{\langle v_{n}, w_{n - 2} \rangle}{||w_{n - 2}||^{2}} w_{n - 2} - \dots - \frac{\langle v_{n}, w_{1} \rangle}{||w_{1}||^{2}} w_{1}
\end{align}
$$

Luego, podemos obtener una base ortonormal $\mathcal{B}_{On} = \left\{  \frac{1}{||w_{1}||}w_{1}, \dots, \frac{1}{||w_{n}||}w_{n}  \right\}$.

En este caso, trabajamos en $V = \mathbb{R}_{2}[t]$ con el producto interno $\langle p, q \rangle = \int_{-1}^{1} p(t) q(t) dt$ y queremos construir una base ortonormal de $V$ a partir de la base $\mathcal{B} = \{ 1, t, t^{2} \}$ (base canónica).

Entonces, definimos una base $\mathcal{B}_{Og} = \{ w_{1}, w_{2}, w_{3} \}$ considerando el método de Gram-Schmidt:
$$
w_{1} = 1
$$
$$
\begin{align}
w_{2} &= t - \frac{\langle t, 1 \rangle}{\langle 1, 1 \rangle} \cdot 1 \\
&= t - \frac{\int_{-1}^{1} t dt}{\int_{-1}^{1} 1 dt} \\
&= t - \frac{\left. \frac{t^{2}}{2} \right|_{-1}^{1}}{t |_{-1}^{1}} \\
&= t - \frac{\cancel{ \frac{1^{2}}{2} } - \cancel{ \frac{(-1)^{2}}{2} }}{1 - (-1)} \\
&= t
\end{align}
$$
$$
\begin{align}
w_{3} &= t^{2} - \frac{\langle t^{2}, t \rangle}{\langle t, t \rangle} \cdot t - \frac{\langle t^{2}, 1 \rangle}{\langle 1, 1 \rangle} \cdot 1 \\
&= t^{2} - \frac{\cancel{ \int_{-1}^{1} t^{3} dt }}{\int_{-1}^{1} t^{2} dt}t - \frac{\int_{-1}^{1} t^{2} dt }{\int_{-1}^{1} 1 dt}1 \\
&= t^{2} - \frac{\left. \frac{t^{3}}{3} \right|_{-1}^{1}}{t |_{-1}^{1}} \\
&= t^{2} - \frac{\frac{1^{3}}{3} - \frac{(-1)^{3}}{3} }{1 - (-1)} \\
&= t^{2} - \frac{\frac{2}{3}}{2} \\
&= t^{2} - \frac{1}{3}
\end{align}
$$

De esta manera, determinamos el siguiente conjunto ortogonal:
$$
\mathcal{B}_{Og} = \{ w_{1}, w_{2}, w_{3} \} = \left\{  1, t, t^{2} - \frac{1}{3}  \right\}
$$

Finalmente, resta normalizar la base para obtener una base ortonormal (en la cual, además de ser ortogonales, los elementos tienen norma 1):
$$
||1|| = \sqrt{ \langle 1, 1 \rangle } = \sqrt{ \int_{-1}^{1} 1 dt } = \sqrt{ t |_{-1}^{1} } = \sqrt{ 1 - (-1) } = \sqrt{ 2 }
$$
$$
||t|| = \sqrt{ \langle t, t \rangle } = \sqrt{ \int_{-1}^{1} t^{2} dt } = \sqrt{ \frac{t^{3}}{3} |_{-1}^{1} } = \sqrt{ \frac{1^{3}}{3} - \frac{(-1)^{3}}{3} } = \sqrt{ \frac{2}{3} }
$$
$$
\begin{align}
\left| \left| t^{2} - \frac{1}{3} \right| \right| &= \sqrt{ \left\langle t^{2} - \frac{1}{3}, t^{2} - \frac{1}{3} \right\rangle } \\
&= \sqrt{ \int_{-1}^{1} t^{4} - \frac{2t^{2}}{3} + \frac{1}{9} dt }
\end{align}
$$
$$
\begin{align}
\int_{-1}^{1} t^{4} - \frac{2t^{2}}{3} + \frac{1}{9} dt &= \int_{-1}^{1} t^{4} dt - \int_{-1}^{1} \frac{2t^{2}}{3} dt + \int_{-1}^{1} \frac{1}{9} dt \\
&= \int_{-1}^{1} t^{4} dt - \frac{2}{3} \cdot \int_{-1}^{1} t^{2} dt + \frac{1}{9} \cdot \int_{-1}^{1} 1 dt \\
&= \left. \frac{t^{5}}{5} \right|_{-1}^{1} - \frac{2}{3} \cdot \left( \left. \frac{t^{3}}{3} \right|_{-1}^{1} \right) + \frac{1}{9} \cdot \left( \left. t \right|_{-1}^{1} \right) \\
&= \frac{2}{5} - \frac{2}{3} \cdot \frac{2}{3} + \frac{1}{9} \cdot 2 \\
&= \frac{2}{5} - \frac{4}{9} + \frac{2}{9} \\
&= \frac{8}{45}
\end{align}
$$
$$
\left| \left| t^{2} - \frac{1}{3} \right| \right| = \sqrt{ \frac{8}{45} }
$$

En conclusión:
$$
\mathcal{B}_{On} = \left\{  \frac{1}{||w_{1}||} w_{1}, \frac{1}{||w_{2}||} w_{2}, \frac{1}{||w_{3}||} w_{3}  \right\} = \left\{  \frac{1}{\sqrt{ 2 }}, \sqrt{ \frac{3}{2} } \cdot t, \sqrt{ \frac{45}{8} } \cdot \left( t^{2} - \frac{1}{3} \right)  \right\}
$$

---
## Ejercicio 9
### Parte 1
1. Determinamos los vectores ortogonales de una base de $S$, considerando $\mathcal{B} = \{ (1, 1, 0, 0), (1, 1, 1, 1), (-1, 0, 2, 1) \}$:
$$
\mathcal{B}_{Og} = \{ w_{1}, w_{2}, w_{3} \}
$$
$$
w_{1} = (1, 1, 0, 0)
$$
$$
\begin{align}
w_{2} &= (1, 1, 1, 1) - \frac{\langle (1, 1, 1, 1), (1, 1, 0, 0) \rangle}{\langle (1, 1, 0, 0), (1, 1, 0, 0) \rangle} \cdot (1, 1, 0, 0) \\
&= (1, 1, 1, 1) - \frac{1^{2} + 1^{2}}{1^{2} + 1^{2}} \cdot (1, 1, 0, 0) \\
&= (1, 1, 1, 1) - 1 \cdot (1, 1, 0, 0) \\
&= (0, 0, 1, 1)
\end{align}
$$
$$
\begin{align}
w_{3} &= (-1, 0, 2, 1) - \frac{\langle (-1, 0, 2, 1), (0, 0, 1, 1) \rangle}{\langle (0, 0, 1, 1), (0, 0, 1, 1) \rangle} \cdot (0, 0, 1, 1) - \frac{\langle (-1, 0, 2, 1), (1, 1, 0, 0) \rangle}{\langle (1, 1, 0, 0), (1, 1, 0, 0) \rangle} \cdot (1, 1, 0, 0) \\
&= (-1, 0, 2, 1) - \frac{2 \cdot 1 + 1 \cdot 1}{1^{2} + 1^{2}} \cdot (0, 0, 1, 1) - \frac{(-1) \cdot 1}{1^{2} + 1^{2}} \cdot (1, 1, 0, 0) \\
&= (-1, 0, 2, 1) - \frac{3}{2} \cdot (0, 0, 1, 1) + \frac{1}{2} \cdot (1, 1, 0, 0) \\
&= (-1, 0, 2, 1) - \left( 0, 0, \frac{3}{2}, \frac{3}{2} \right) + \left( \frac{1}{2}, \frac{1}{2}, 0, 0 \right) \\
&= \left( -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2} \right)
\end{align}
$$

De esta forma, obtuvimos la siguiente base ortogonal:
$$
\mathcal{B}_{Og} = \{ w_{1}, w_{2}, w_{3} \} = \left\{  (1, 1, 0, 0), (0, 0, 1, 1), \left( -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2} \right)  \right\}
$$

2. Normalizar el conjunto, multiplicando cada vector por el inverso de su norma:
Determinamos la norma de cada vector:
$$
||w_{1}|| = ||(1, 1, 0, 0)|| = \sqrt{ \langle (1, 1, 0, 0), (1, 1, 0, 0) \rangle } = \sqrt{ 1^{2} + 1^{2} } = \sqrt{ 2 }
$$
$$
||w_{2}|| = ||(0, 0, 1, 1)|| = \sqrt{ \langle (0, 0, 1, 1), (0, 0, 1, 1) \rangle } = \sqrt{ 1^{2} + 1^{2} } = \sqrt{ 2 }
$$
$$
\begin{align}
||w_{3}|| &= \left| \left| \left( -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2} \right) \right| \right| \\
&= \sqrt{ \left\langle \left( -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2} \right), \left( -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2} \right) \right\rangle } \\
&= \sqrt{ \left( -\frac{1}{2} \right)^{2} + \left( \frac{1}{2} \right)^{2} + \left( \frac{1}{2} \right)^{2} + \left( -\frac{1}{2} \right)^{2} } \\
&= \sqrt{ \frac{1}{4} + \frac{1}{4} + \frac{1}{4} + \frac{1}{4} } \\
&= \sqrt{ 1 } \\
&= 1
\end{align}
$$

En conclusión, una base ortonormal es:
$$
\begin{align}
\mathcal{B}_{On} &= \left\{  \frac{1}{||w_{1}||} \cdot w_{1}, \frac{1}{||w_{2}||} \cdot w_{2}, \frac{1}{||w_{3}||} \cdot w_{3}  \right\} \\
&= \left\{ \frac{1}{\sqrt{ 2 }} \cdot (1, 1, 0, 0), \frac{1}{\sqrt{ 2 }} \cdot (0, 0, 1, 1), \frac{1}{1} \cdot \left( -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2} \right)  \right\} \\
&= \left\{ \left( \frac{1}{\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }}, 0, 0 \right), \left( 0, 0, \frac{1}{\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }} \right), \left( -\frac{1}{2}, \frac{1}{2}, \frac{1}{2}, -\frac{1}{2} \right)  \right\}
\end{align}
$$

### Parte 2
1. Determinamos los vectores ortogonales de una base de $S$, considerando $\mathcal{B} = \{ (1, i, 0), (1, 1, 1) \}$:
$$
\mathcal{B}_{Og} = \{ w_{1}, w_{2} \}
$$
$$
w_{1} = (1, i, 0)
$$
$$
\begin{align}
w_{2} &= (1, 1, 1) - \frac{\langle (1, 1, 1), (1, i, 0) \rangle}{\langle (1, i, 0), (1, i, 0) \rangle} \cdot (1, i, 0) \\
&= (1, 1, 1) - \frac{1^{2} + 1 \cdot (-i)}{1^{2} + i \cdot (-i)} \cdot (1, i, 0) \\
&= (1, 1, 1) - \frac{1 - i}{2} \cdot (1, i, 0) \\
&= (1, 1, 1) - \left( \frac{1}{2} - \frac{1}{2}i, \frac{1}{2} + \frac{1}{2}i, 0 \right) \\
&= \left( \frac{1}{2} + \frac{1}{2}i, \frac{1}{2} - \frac{1}{2}i, 1 \right)
\end{align}
$$

De esta forma, obtuvimos la siguiente base ortogonal:
$$
\mathcal{B}_{Og} = \{ w_{1}, w_{2} \} = \left\{  (1, i, 0), \left( \frac{1}{2} + \frac{1}{2}i, \frac{1}{2} - \frac{1}{2}i, 1 \right)  \right\}
$$

2. Normalizar el conjunto, multiplicando cada vector por el inverso de su norma:
$$
||w_{1}|| = ||(1, i, 0)|| = \sqrt{ \langle (1, i, 0), (1, i, 0) \rangle } = \sqrt{ 1^{2} + i \cdot (-i) } = \sqrt{ 1 + 1 } = \sqrt{ 2 }
$$
$$
\begin{align}
||w_{2}|| &= \left| \left| \left( \frac{1}{2} + \frac{1}{2}i, \frac{1}{2} - \frac{1}{2}i, 1 \right) \right| \right| \\
&= \sqrt{ \left\langle \left( \frac{1}{2} + \frac{1}{2}i, \frac{1}{2} - \frac{1}{2}i, 1 \right), \left( \frac{1}{2} + \frac{1}{2}i, \frac{1}{2} - \frac{1}{2}i, 1 \right) \right\rangle } \\
&= \sqrt{ \left( \frac{1}{2} + \frac{1}{2}i \right) \cdot \left( \frac{1}{2} - \frac{1}{2}i \right) + \left( \frac{1}{2} - \frac{1}{2}i \right) \cdot \left( \frac{1}{2} + \frac{1}{2}i \right) + 1^{2} } \\
&= \sqrt{ 2 \cdot \left( \frac{1}{4} - \frac{1}{4}i^{2} \right) + 1 } \\
&= \sqrt{ 2 \cdot \left( \frac{1}{2} \right) + 1 } \\
&= \sqrt{ 1 + 1 } \\
&= \sqrt{ 2 }
\end{align}
$$

En conclusión, una base ortonormal es:
$$
\begin{align}
\mathcal{B}_{On} &= \left\{  \frac{1}{||w_{1}||} \cdot w_{1}, \frac{1}{||w_{2}||} \cdot w_{2}  \right\} \\
&= \left\{  \frac{1}{\sqrt{ 2 }} \cdot (1, i, 0), \frac{1}{\sqrt{ 2 }} \cdot \left( \frac{1}{2} + \frac{1}{2}i, \frac{1}{2} - \frac{1}{2}i, 1 \right)  \right\} \\
&= \left\{  \left( \frac{1}{\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }}i, 0 \right), \left( \frac{1}{\sqrt{ 8 }} + \frac{1}{\sqrt{ 8 }}i, \frac{1}{\sqrt{ 8 }} - \frac{1}{\sqrt{ 8 }}i, \frac{1}{\sqrt{ 2 }} \right)  \right\}
\end{align}
$$

---
## Ejercicio 10
Consideremos los vectores $\mathcal{B} = \{ v_{1}, \dots, v_{n} \} \subset \mathbb{R}^{m}$ tal que $v_{i} \perp v_{j}, \forall i \neq j$ considerando el producto interno habitual $\langle v_{i}, v_{j} \rangle = \sum_{k = 1}^{m} v_{i_{k}} \cdot v_{j_{k}}$, y $||v_{i}|| = 1, \forall i \in \{ 1, \dots, n \}$. Dichos vectores conforman las columnas de la matriz $A$:
$$
A = \begin{pmatrix}
v_{1} & v_{2} & \dots & v_{n}
\end{pmatrix}
$$

De esta forma, desarrollamos el producto con la traspuesta:
$$
A^{t} \cdot A = \begin{pmatrix}
v_{1}^{t} \\
v_{2}^{t} \\
\vdots \\
v_{n}^{t}
\end{pmatrix} \cdot \begin{pmatrix}
v_{1} & v_{2} & \dots & v_{n}
\end{pmatrix}
$$
Como $A^{t} \in M_{n \times m}(\mathbb{R})$ y $A \in M_{m \times n}(\mathbb{R})$, el resultado de su producto será una matriz $B \in M_{n \times n}$ donde cada celda $i, j$ estará conformada por $\sum_{k = 1}^{m} v_{i_{k}} \cdot v_{j_{k}} = \langle v_{i}, v_{j} \rangle$. Como todos los vectores $v \in \mathcal{B}$ son ortogonales dos a dos, esto significa que $\langle v_{i}, v_{j} \rangle = 0, \forall i \neq j$.

Entonces, todas las celdas de la matriz resultante serán nulas, a excepción de aquellas en las que se desarrolla el producto interno entre un vector y el mismo. Además, como el conjunto es ortonormal, todos los vectores tienen norma 1, por lo tanto: $\langle v_{i}, v_{i} \rangle = ||v_{i}||^{2} = 1^{2} = 1, \forall v_{i} \in \{ 1, \dots, n \}$.

En conclusión:
$$
A^{t} \cdot A = \begin{pmatrix}
v_{1}^{t} \\
v_{2}^{t} \\
\vdots \\
v_{n}^{t}
\end{pmatrix} \cdot \begin{pmatrix}
v_{1} & v_{2} & \dots & v_{n}
\end{pmatrix} = \begin{pmatrix}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 1
\end{pmatrix}
$$

---
## Ejercicio 11
En este caso, se nos provee de un espacio vectorial y una base del mismo, y tenemos que definir un producto interno en el espacio provisto tal que la base $\mathcal{B}$ resulte ser ortonormal.

Entonces, el producto interno construido tiene que cumplir que $\forall v \in \mathcal{B}$:
$$
\begin{align}
\langle v_{i}, v_{i} \rangle &= 1 \\
\langle v_{i}, v_{j} \rangle &= 0 \qquad (\forall i \neq j)
\end{align}
$$

Si tomamos dos vectores cualesquiera $u, w \in V$ y los escribimos en base a la base $\mathcal{B}$ provista:
$$
\begin{align}
u = \alpha_{1}v_{1} + \alpha_{2}v_{2} + \dots + \alpha_{n}v_{n} &\implies coord_{\mathcal{B}}(u) = (\alpha_{1}, \alpha_{2}, \dots, \alpha_{n})^{t} \\
w = \beta_{1}v_{1} + \beta_{2}v_{2} + \dots + \beta_{n}v_{n} &\implies coord_{\mathcal{B}}(w) = (\beta_{1}, \beta_{2}, \dots, \beta_{n})^{t}
\end{align}
$$

Si imponemos que $\mathcal{B}$ sea ortonormal, por las propiedades del producto interno tiene que verificarse que:
$$
\begin{align}
\langle u, w \rangle &= \left\langle \sum_{i = 1}^{n} \alpha_{i}v_{i}, \sum_{j = 1}^{n} \beta_{j}v_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \alpha_{i} \left\langle v_{i}, \sum_{j = 1}^{n} \beta_{j}v_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \alpha_{i} \overline{\sum_{j = 1}^{n} \beta_{j}} \left\langle v_{i}, v_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \sum_{j = 1}^{n} \alpha_{i} \overline{\beta_{j}} \left\langle v_{i}, v_{j} \right\rangle
\end{align}
$$
Como $\langle v_{i}, v_{j} \rangle = 0, \forall i \neq j$:
$$
= \sum_{i, j = 1}^{n} \alpha_{i} \overline{\beta_{j}} \left\langle v_{i}, v_{j} \right\rangle
$$
Como $\langle v_{i}, v_{j} \rangle = 1, \forall i = j$:
$$
= \sum_{i = 1}^{n} \alpha_{i} \overline{\beta_{i}}
$$

Conclusión conceptual: Definir un producto interno para el cual la base $\mathcal{B}$ sea ortonormal equivale a definir el producto interno de dos vectores como el producto escalar usual de sus coordenadas en la base $\mathcal{B}$.

### Parte 1
Tenemos que determinar un producto interno que cumpla:
$$
\begin{align}
\langle (1, 1), (1, 1) \rangle &= 1 \\
\langle (2, -1), (2, -1) \rangle &= 1 \\
\langle (1, 1), (2, -1) \rangle &= 0
\end{align}
$$
Consideramos los vectores genéricos $(x, y)$ y $(x', y')$, tales que:
$$
\begin{align}
(x, y) = \alpha_{1} \cdot (1, 1) + \alpha_{2} \cdot (2, -1) &\implies coord_{\mathcal{B}}((x, y)) = (\alpha_{1}, \alpha_{2})^{t} \\
(x', y') = \beta_{1} \cdot (1, 1) + \beta_{2} \cdot (2, -1) &\implies coord_{\mathcal{B}}((x', y')) = (\beta_{1}, \beta_{2})^{t}
\end{align}
$$

De esta manera:
$$
\langle (x, y), (x', y') \rangle = \alpha_{1} \cdot \beta_{1} + \alpha_{2} \cdot \beta_{2}
$$

Entonces, estudiamos los productos internos mencionados:
$$
\begin{align}
\langle (1, 1), (1, 1) \rangle = 1 &\Longleftrightarrow 1 \cdot 1 + 0 \cdot 0 = 1 \\
\langle (2, -1), (2, -1) \rangle = 1 &\Longleftrightarrow 0 \cdot 0 + 1 \cdot 1 = 1 \\
\langle (1, 1), (2, -1) \rangle = 0 &\Longleftrightarrow 1 \cdot 0 + 0 \cdot 1 = 0
\end{align}
$$

De esta forma, el producto interno definido como $\langle (x, y), (x', y') \rangle = \alpha_{1} \cdot \beta_{1} + \alpha_{2} \cdot \beta_{2}$, siendo $\alpha_{i}$ y $\beta_{i}$ coordenadas de los vectores involucrados satisface las condiciones presentadas.

Para encontrar la fórmula explicita a partir de $(x, y)$ y $(x', y')$, tenemos que desarrollar el siguiente sistema, tomando en cuenta la base provista:

ACLARACIÓN: Los $\alpha_{1}, \alpha_{2}, \beta_{1}, \beta_{2}$ utilizados más abajo hacen referencia a los utilizados en la fórmula general. Queremos determinar una fórmula que esté dada por $x, y, x', y'$.
$$
\begin{cases}
x = \alpha_{1} + 2\alpha_{2} \\
y = \alpha_{1} - \alpha_{2}
\end{cases} \implies 3\alpha_{2} = x - y \implies \alpha_{2} = \frac{x - y}{3} \implies \alpha_{1} = y + \frac{x - y}{3} = \frac{x + 2y}{3}
$$
Es análogo para $(x', y')$:
$$
\begin{align}
\beta_{1} &= \frac{x' + 2y'}{3} \\
\beta_{2} &= \frac{x' - y'}{3}
\end{align}
$$

Desarrollamos la fórmula:
$$
\begin{align}
\langle (x, y), (x', y') \rangle &= \alpha_{1} \cdot \beta_{1} + \alpha_{2} \cdot \beta_{2} \\
&= \left( \frac{x + 2y}{3} \right) \cdot \left( \frac{x' + 2y'}{3} \right) + \left( \frac{x - y}{3} \right) \cdot \left( \frac{x' - y'}{3} \right) \\
&= \frac{xx' + 2xy' + 2x'y + 4yy'}{9} + \frac{xx' - xy' - x'y + yy'}{9} \\
&= \frac{2xx' + xy' + x'y + 5yy'}{9} 
\end{align}
$$

En conclusión:
$$
\langle (x, y), (x', y') \rangle = \frac{2xx' + xy' + x'y + 5yy'}{9} 
$$
es el producto interno que satisface las condiciones establecidas.

### Parte 2
Tenemos que determinar un producto interno que cumpla:
$$
\begin{align}
\langle (1, i), (1, i) \rangle &= 1 \\
\langle (-1, i), (-1, i) \rangle &= 1 \\
\langle (1, i), (-1, i) \rangle &= 0
\end{align}
$$
Consideramos el mismo producto interno utilizado en la parte anterior, pero agregando el conjugado en la segunda componente:
$$
\langle (x, y), (x', y') \rangle = \alpha_{1} \cdot \overline{\beta_{1}} + \alpha_{2} \cdot \overline{\beta_{2}}
$$

Entonces, estudiamos los productos internos mencionados:
$$
\begin{align}
\langle (1, i), (1, i) \rangle = 1 &\Longleftrightarrow 1 \cdot 1 + 0 \cdot 0 = 1 \\
\langle (-1, i), (-1, i) \rangle = 1 &\Longleftrightarrow 0 \cdot 0 + 1 \cdot 1 = 1 \\
\langle (1, i), (-1, i) \rangle = 0 &\Longleftrightarrow 1 \cdot 0 + 0 \cdot 1 = 0
\end{align}
$$

De esta forma, el producto interno definido como $\langle (x, y), (x', y') \rangle = \alpha_{1} \cdot \overline{\beta_{1}} + \alpha_{2} \cdot \overline{\beta_{2}}$, siendo $\alpha_{i}$ y $\beta_{i}$ coordenadas de los vectores involucrados satisface las condiciones presentadas.

Para encontrar la fórmula explicita a partir de $(x, y)$ y $(x', y')$, tenemos que desarrollar el siguiente sistema, tomando en cuenta la base provista:

$$
\begin{cases}
x = \alpha_{1} - \alpha_{2} \\
y = \alpha_{1}i + \alpha_{2}i
\end{cases} \implies 2\alpha_{1} = x - yi \implies \alpha_{1} = \frac{x - yi}{2} \implies \alpha_{2} = \frac{x - yi}{2} - x = \frac{-x - yi}{2}
$$
Es análogo para $(x', y')$:
$$
\begin{align}
\beta_{1} &= \frac{x - yi}{2} \\
\beta_{2} &= \frac{-x' - y'i}{2}
\end{align}
$$

Desarrollamos la fórmula:
$$
\begin{align}
\langle (x, y), (x', y') \rangle &= \alpha_{1} \cdot \overline{\beta_{1}} + \alpha_{2} \cdot \overline{\beta_{2}} \\
&= \left( \frac{x - yi}{2} \right) \cdot \overline{\left( \frac{x' - y'i}{2} \right)} + \left( \frac{-x - yi}{2} \right) \cdot \overline{\left( \frac{-x' - y'i}{2} \right)} \\
&= \frac{x\overline{x'} + x\overline{y'}i - \overline{x'}yi + y\overline{y'}}{4} + \frac{x\overline{x'} - x\overline{y'}i + \overline{x'}yi + y\overline{y'}}{4} \\
&= \frac{2x\overline{x'} + 2y\overline{y'}}{2} \\
&= x\overline{x'} + y\overline{y'}
\end{align}
$$

En conclusión:
$$
\begin{align}
\langle (x, y), (x', y') \rangle = x\overline{x'} + y\overline{y'}
\end{align}
$$
es el producto interno que satisface las condiciones establecidas.

### Parte 3
Tenemos que determinar un producto interno que cumpla:
$$
\begin{align}
\langle (1, i, 1), (1, i, 1) \rangle &= 1 \\
\langle (0, 0, 1), (0, 0, 1) \rangle &= 1 \\
\langle (0, 1, i), (0, 1, i) \rangle &= 1 \\
\langle (1, i, 1), (0, 0, 1) \rangle &= 0 \\
\langle (1, i, 1), (0, 1, i) \rangle &= 0 \\
\langle (0, 0, 1), (0, 1, i) \rangle &= 0
\end{align}
$$

Consideramos el mismo producto interno utilizado en la parte anterior, pero considerando que cada vector tiene tres componentes:
$$
\langle (x, y, z), (x', y', z') \rangle = \alpha_{1} \cdot \overline{\beta_{1}} + \alpha_{2} \cdot \overline{\beta_{2}} + \alpha_{3} \cdot \overline{\beta_{3}}
$$

Entonces, estudiamos los productos internos mencionados:
$$
\begin{align}
\langle (1, i, 1), (1, i, 1) \rangle = 1 &\Longleftrightarrow 1 \cdot 1 + 0 \cdot 0 + 0 \cdot 0 = 1 \\
\langle (0, 0, 1), (0, 0, 1) \rangle = 1 &\Longleftrightarrow 0 \cdot 0 + 1 \cdot 1 + 0 \cdot 0 = 1 \\
\langle (0, 1, i), (0, 1, i) \rangle = 1 &\Longleftrightarrow 0 \cdot 0 + 0 \cdot 0 + 1 \cdot 1 = 1 \\
\langle (1, i, 1), (0, 0, 1) \rangle = 0 &\Longleftrightarrow 1 \cdot 0 + 0 \cdot 1 + 0 \cdot 0 = 0 \\
\langle (1, i, 1), (0, 1, i) \rangle = 0 &\Longleftrightarrow 1 \cdot 0 + 0 \cdot 0 + 0 \cdot 1 = 0 \\
\langle (0, 0, 1), (0, 1, i) \rangle = 0 &\Longleftrightarrow 0 \cdot 0 + 1 \cdot 0 + 0 \cdot 1 = 0
\end{align}
$$

De esta forma, el producto interno definido como $\langle (x, y, z), (x', y', z') \rangle = \alpha_{1} \cdot \overline{\beta_{1}} + \alpha_{2} \cdot \overline{\beta_{2}} + \alpha_{3} \cdot \overline{\beta_{3}}$, siendo $\alpha_{i}$ y $\beta_{i}$ coordenadas de los vectores involucrados satisface las condiciones presentadas.

Para encontrar la fórmula explicita a partir de $(x, y, z)$ y $(x', y', z')$, tenemos que desarrollar el siguiente sistema, tomando en cuenta la base provista:

$$
\begin{cases}
x = \alpha_{1} \\
y = \alpha_{1}i + \alpha_{3} \\
z = \alpha_{1} + \alpha_{2} + \alpha_{3}i
\end{cases} \implies \alpha_{3} = y - xi \implies \alpha_{2} = z - 2x - yi
$$
Es análogo para $(x', y', z')$:
$$
\begin{align}
\beta_{1} &= x' \\
\beta_{2} &= z' - 2x' - y'i \\
\beta_{3} &= y' - x'i
\end{align}
$$

Desarrollamos la fórmula:
$$
\begin{align}
\langle (x, y, z), (x', y', z') \rangle &= \alpha_{1} \cdot \overline{\beta_{1}} + \alpha_{2} \cdot \overline{\beta_{2}} + \alpha_{3} \cdot \overline{\beta_{3}} \\
&= \left( x \right) \cdot \overline{\left( x' \right)} + \left( z - 2x - yi \right) \cdot \overline{\left( z' - 2x' - y'i \right)} + \left( y - xi \right) \cdot \overline{\left( y' - x'i \right)} \\
&= x\overline{x'} + z\overline{z'} - 2\overline{x'}z + \overline{y'}zi - 2x\overline{z'} + 4x\overline{x'} - 2x\overline{y'}i - y\overline{z'}i + 2\overline{x'}yi + y\overline{y'} + y\overline{y'} + \overline{x'}yi - x\overline{y'}i + x\overline{x'} \\
&= 6x\overline{x'} + z\overline{z'} - 2\overline{x'}z + \overline{y'}zi - 2x\overline{z'} - 3x\overline{y'}i - y\overline{z'}i + 3\overline{x'}yi + 2y\overline{y'}
\end{align}
$$

En conclusión:
$$
\langle (x, y, z), (x', y', z') \rangle = 6x\overline{x'} + z\overline{z'} - 2\overline{x'}z + \overline{y'}zi - 2x\overline{z'} - 3x\overline{y'}i - y\overline{z'}i + 3\overline{x'}yi + 2y\overline{y'}
$$
es el producto interno que satisface las condiciones establecidas.

---
## Ejercicio 12
Tenemos que probar que $\forall v \in \mathbb{B}, \langle v, v \rangle = ||v||^{2} = 1 \implies ||v|| = 1$.

$\forall w = \sum_{i = 1}^{n} a_{i}v_{i} \in V$ significa que todo $w$ expresado como combinación lineal de los elementos de $\mathbb{B}$ pertenece a $V$ (cosa que sabemos ya que $\mathbb{B}$ es base de $V$). Sin embargo, sabemos que para todo $w$, se verifica que $\langle w, w \rangle = \sum_{i = 1}^{n} a_{i}^{2}$. Desarrollemos el producto interno (aplicando propiedades como la linealidad en la primera componente, y en la segunda - considerando el conjugado):
$$
\begin{align}
\langle w, w \rangle &= \left\langle \sum_{i = 1}^{n} a_{i}v_{i}, \sum_{j = 1}^{n} a_{j}v_{j} \right\rangle \\
&= \sum_{i = 1}^{n} a_{i} \left\langle v_{i}, \sum_{j = 1}^{n} a_{j}v_{j} \right\rangle \\
&= \sum_{i = 1}^{n} a_{i} \sum_{j = 1}^{n} a_{j} \left\langle v_{i}, v_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \sum_{j = 1}^{n} a_{i} a_{j} \left\langle v_{i}, v_{j} \right\rangle
\end{align}
$$
Sabemos que $\langle w, w \rangle = \sum_{i = 1}^{n} a_{i}^{2}$, lo que significa que, de la suma anterior, los únicos términos que sobreviven son aquellos que verifican $i = j$. De esta forma, determinamos que $\left\langle v_{i}, v_{j} \right\rangle = 0, \forall i \neq j$. Por lo tanto:
$$
\begin{align}
\langle w, w \rangle &= \sum_{i = 1}^{n} \sum_{j = 1}^{n} a_{i} a_{j} \left\langle v_{i}, v_{j} \right\rangle \\
&= \sum_{i, j = 1}^{n} a_{i} a_{j} \left\langle v_{i}, v_{j} \right\rangle \\
&= \sum_{i = 1}^{n} a_{i}^{2} \left\langle v_{i}, v_{i} \right\rangle
\end{align}
$$

Entonces, recordando que $\langle w, w \rangle = \sum_{i = 1}^{n} a_{i}^{2}$, podemos deducir que $\left\langle v_{i}, v_{i} \right\rangle = 1, \forall i \in \{ 1, \dots, n \}$. Sabiendo que $\left\langle v_{i}, v_{i} \right\rangle = ||v_{i}||^{2} = 1 \implies ||v_{i}|| = 1, \forall i \in \{ 1, \dots, n \}$, demostramos que $\mathbb{B}$ es una base ortonormal de $V$.

CORRECCIÓN:
En realidad, lo que hay que hacer es tomar un vector genérico perteneciente a $\mathbb{B}$ y probar que su norma es 1, desarrollando su producto interno y considerando sus coordenadas (la única que no se anula para un vector genérico $v_{i}$ es la coordenada $a_{i}$, y sabiendo que $a_{i} = 1$ para el vector $v_{i}$, aplicando la fórmula provista, determinamos que $\langle v_{i}, v_{i} \rangle = \sum_{i = 1}^{n} a_{i}^{2} = a_{i}^{2} = 1^{2} = 1 = ||v_{i}||^{2} = ||v_{i}||$).

Para la ortogonalidad, podemos considerar el vector $w = v_{i} + v_{j}$, tal que la única coordenada no nula de $v_{i}$ es $a_{i} = 1$, y $a_{j} = 1$ para $v_{j}$, de forma que $a_{k} = 0, \forall k \not \in \{ i, j \}$.

Cuando desarrollemos dicho producto interno:
- Por las hipótesis del ejercicio:
$$
\langle v_{i} + v_{j}, v_{i} + v_{j} \rangle = 1^{2} + 1^{2} + 0^{2} + \dots + 0^{2} = 2
$$
- Por las propiedades del producto interno:
$$
\begin{align}
\langle w, w \rangle &= \langle v_{i} + v_{j}, v_{i} + v_{j} \rangle \\
&= \langle v_{i}, v_{i} + v_{j} \rangle + \langle v_{j}, v_{i} + v_{j} \rangle \\
&= \langle v_{i}, v_{i} \rangle + \langle v_{i}, v_{j} \rangle + \langle v_{j}, v_{i} \rangle + \langle v_{j}, v_{j} \rangle \\
&= \langle v_{i}, v_{i} \rangle + \langle v_{i}, v_{j} \rangle + \langle v_{i}, v_{j} \rangle + \langle v_{j}, v_{j} \rangle \\
&= 1 + 2\langle v_{i}, v_{j} \rangle + 1 \\
&= 2 + 2\langle v_{i}, v_{j} \rangle
\end{align}
$$

Ahora, igualamos ambas expresiones:
$$
2 + 2\langle v_{i}, v_{j} \rangle = 2 \implies 2\langle v_{i}, v_{j} \rangle = 0 \implies \langle v_{i}, v_{j} \rangle = 0, \forall i \neq j
$$
Lo que demuestra la ortogonalidad.

---
## Ejercicio 13
Primero que nada, consideremos que la norma inducida de un espacio vectorial con producto interno es:
$$
||v|| = \sqrt{ \langle v, v \rangle }, \forall v \in V
$$

Ahora, comenzamos la demostración:
Como $\mathcal{B} = \{ u_{1}, \dots, u_{n} \}$ es una base ortogonal, entonces verifica que:
$$
\forall v \in V, v = \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} = \sum_{i = 1}^{n} \alpha_{i}u_{i} \implies coord_{\mathcal{B}}(v) = (\alpha_{1}, \dots, \alpha_{n})
$$
$$
\forall u_{i}, u_{j} \in \mathcal{B}, u_{i} \perp u_{j} \Longleftrightarrow \langle u_{i}, u_{j} \rangle = 0, \forall i \neq j
$$

1. Tenemos que probar que $\alpha_{i} = \frac{\langle v, u_{i} \rangle}{||u_{i}||^{2}}, \forall i \in \{ 1, \dots, n \}$
Desarrollemos el producto interno de un vector genérico $v \in V$, y $u_{j}$:
$$
\begin{align}
\langle v, u_{j} \rangle &= \left\langle \sum_{i = 1}^{n} \alpha_{i}u_{i}, u_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \alpha_{i} \langle u_{i}, u_{j} \rangle
\end{align}
$$
Como $\mathcal{B}$ es ortogonal, $\langle u_{i}, u_{j} \rangle = 0, \forall i \neq j$, por lo que:
$$
\begin{align}
&= \alpha_{j} \langle u_{j}, u_{j} \rangle \\
&= \alpha_{j} ||u_{j}||^{2}
\end{align}
$$
Finalmente, si pasamos dividiendo $||u_{j}||^{2}$ (válido ya que $\vec{0} \not \in \mathcal{B}$, pues $\mathcal{B}$ es ortogonal):
$$
\langle v, u_{j} \rangle = \alpha_{j} ||u_{j}||^{2} \implies \frac{\langle v, u_{j} \rangle}{||u_{j}||^{2}} = \alpha_{j}
$$
En conclusión, $\alpha_{j} = \frac{\langle v, u_{j} \rangle}{||u_{j}||^{2}}, \forall j \in \{ 1, \dots, n \}$, por lo que
$$
\forall v \in V, v = \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} = \sum_{i = 1}^{n} \alpha_{i}u_{i} \implies coord_{\mathcal{B}}(v) = (\alpha_{1}, \dots, \alpha_{n}) = \left( \frac{\langle v, u_{1} \rangle}{||u_{1}||^{2}}, \dots, \frac{\langle v, u_{n} \rangle}{||u_{n}||^{2}} \right)
$$

2. Tenemos que probar que $\langle v, w \rangle = \frac{\langle v, u_{1} \rangle \langle u_{1}, w \rangle}{||u_{1}||^{2}} + \dots + \frac{\langle v, u_{n} \rangle \langle u_{n}, w \rangle}{||u_{n}||^{2}}, \forall v, w \in V$
Consideramos $v, w \in V$ genéricos, tal que
$$
\begin{align}
v = \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} &\implies coord_{\mathcal{B}}(v) = (\alpha_{1}, \dots, \alpha_{n}) \\
w = \beta_{1} \cdot u_{1} + \dots + \beta_{n} \cdot u_{n} &\implies coord_{\mathcal{B}}(w) = (\beta_{1}, \dots, \beta_{n})
\end{align}
$$
Desarrollamos el producto interno:
$$
\begin{align}
\langle v, w \rangle &= \left\langle \sum_{i = 1}^{n} \alpha_{i}u_{i}, \sum_{j = 1}^{n} \beta_{j}u_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \alpha_{i} \left\langle u_{i}, \sum_{j = 1}^{n} \beta_{j}u_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \alpha_{i} \overline{\sum_{j = 1}^{n} \beta_{j}} \left\langle u_{i}, u_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \sum_{j = 1}^{n} \alpha_{i} \overline{\beta_{j}} \left\langle u_{i}, u_{j} \right\rangle
\end{align}
$$
Como $\langle u_{i}, u_{j} \rangle = 0, \forall i \neq j$:
$$
\begin{align}
&= \sum_{i, j = 1}^{n} \alpha_{i} \overline{\beta_{j}} \left\langle u_{i}, u_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \alpha_{i} \overline{\beta_{i}} \left\langle u_{i}, u_{i} \right\rangle
\end{align}
$$
Como $||v|| = \sqrt{ \langle v, v \rangle } \implies \langle v, v \rangle = ||v||^{2}, \forall v \in V$:
$$
\begin{align}
&= \sum_{i, j = 1}^{n} \alpha_{i} \overline{\beta_{j}} \left\langle u_{i}, u_{j} \right\rangle \\
&= \sum_{i = 1}^{n} \alpha_{i} \overline{\beta_{i}} \cdot ||u_{i}||^{2}
\end{align}
$$

Como probamos en la parte 1, conocemos los valores de $\alpha_{i}$ y $\overline{\beta_{i}}$:
$$
\begin{align}
&\alpha_{i} = \text{i-ésima coordenada de } v = \frac{\langle v, u_{i} \rangle}{||u_{i}||^{2}} \\
&\beta_{i} = \text{i-ésima coordenada de } w = \frac{\langle w, u_{i} \rangle}{||u_{i}||^{2}} \implies \overline{\beta_{i}} = \overline{\frac{\langle w, u_{i} \rangle}{||u_{i}||^{2}}} = \frac{\langle u_{i}, w \rangle}{||u_{i}||^{2}}
\end{align}
$$

Resta sustituir en la expresión:
$$
\begin{align}
\sum_{i = 1}^{n} \alpha_{i} \overline{\beta_{i}} \cdot ||u_{i}||^{2} &= \sum_{i = 1}^{n} \frac{\langle v, u_{i} \rangle}{||u_{i}||^{2}} \cdot \frac{\langle u_{i}, w \rangle}{\cancel{ ||u_{i}||^{2} }} \cdot \cancel{ ||u_{i}||^{2} } \\
&= \sum_{i = 1}^{n} \frac{\langle v, u_{i} \rangle \langle u_{i}, w \rangle}{||u_{i}||^{2}} \\
&= \frac{\langle v, u_{1} \rangle \langle u_{1}, w \rangle}{||u_{1}||^{2}} + \dots + \frac{\langle v, u_{n} \rangle \langle u_{n}, w \rangle}{||u_{n}||^{2}}
\end{align}
$$

En conclusión:
$$
\langle v, w \rangle = \frac{\langle v, u_{1} \rangle \langle u_{1}, w \rangle}{||u_{1}||^{2}} + \dots + \frac{\langle v, u_{n} \rangle \langle u_{n}, w \rangle}{||u_{n}||^{2}}, \forall v, w \in V
$$