# Ejercicio 1
Tres partes.

Sabemos que para que un conjunto sea un espacio vectorial tiene que cumplir con una serie de propiedades, como contener al vector nulo, ser estable por suma de vectores y producto de un vector por un escalar, etc. Sin embargo, simplemente probando que un conjunto $S$ cumple que
$$
\begin{align}
&\text{(1)} &&\vec{0} \in S \\
&\text{(2)} &&\text{Si } u, v \in S, \text{entonces } u + v \in S \\
&\text{(3)} &&\text{Si } u \in S, \text{entonces } \alpha \cdot u \in S &&(\forall \alpha \in K)
\end{align}
$$
o
$$
\begin{align}
&(1) &&S \neq \emptyset \\
&(2) &&\forall \alpha, \beta \in K, \forall u, v \in S, \alpha \cdot u + \beta \cdot v \in S
\end{align}
$$
sabemos que se trata de un espacio vectorial.

También lo podemos ver de la siguiente forma:

En un espacio vectorial $S$, cualquier combinación lineal de vectores de $S$ también es un vector de $S$:
$$
\text{Si } u_{1}, \dots, u_{n} \in S, \text{entonces } \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} \in S \qquad (\forall \alpha_{1}, \dots, \alpha_{n} \in K)
$$

De esta forma, tenemos que analizar las propiedades anteriores para los ejemplos propuestos.
Basta con encontrar una propiedad que no se cumpla para verificar que no se trata de un espacio vectorial.

## Parte a)
$$
\begin{align}
&\text{Suma:} &&(x_{1}, y_{1}) + (x_{2}, y_{2}) = (3y_{1} + 3y_{2}, −x_{1} − x_{2}) \\
&\text{Producto:} &&\lambda(x_{1}, y_{1}) = (3\lambda y_{1}, x_{1})
\end{align}
$$
En este caso, podemos analizar lo que sucede con la suma considerando que un vector cualquiera $u$ mas el vector nulo $\vec{0}$ debería dar como resultado a $u$ (siendo $\vec{0}$ el neutro de la suma):
$$
(x_{1}, y_{1}) + (0, 0) = (3y_{1} + 3 \cdot 0, −x_{1} − 0) = (3y_{1}, -x_{1}) \ne (x_{1}, y_{1})
$$
Como vemos, se podría decir que no existe un vector nulo para la suma en dicho conjunto.

Además, si consideramos el escalar nulo 0, tampoco se cumple que un vector $u$ cualquiera por el escalar nulo 0, da como resultado el vector nulo $\vec{0}$ por la propia definición de la operación:
$$
0 \cdot (x_{1}, y_{1}) = (3 \cdot 0 \cdot y_{1}, x_{1}) = (0, x_{1})
$$
De esta forma, no se obtiene un vector nulo $\vec{0}$ genérico, ya que para cada vector con valor único $x_{1}$ se obtendrá un resultado diferente.

De esta forma, el espacio definido no es un espacio vectorial.

## Parte d)
$$
\begin{align}
&\text{Suma:} &&(x_{1}, y_{1}) + (x_{2}, y_{2}) = (x_{1}, x_{2} + y_{2}) \\
&\text{Producto:} &&\lambda(x_{1}, y_{1}) = (\lambda x_{1}, \lambda y_{1})
\end{align}
$$
Si estudiamos lo que sucede al sumar dos vectores $u$ y $-u$ opuestos, podemos ver que:
$$
(x_{1}, y_{1}) + (-x_{1}, -y_{1}) = (x_{1}, -x_{1} - y_{1})
$$
Como vemos, este resultado no se corresponde con lo esperado: el vector nulo $\vec{0}$.

Incluso podemos analizar lo que sucede al sumar un vector y el vector nulo:
$$
(x_{1}, y_{1}) + (0, 0) = (x_{1}, 0 + 0) \neq (x_{1}, y_{1})
$$
Como vemos, tampoco existe un vector nulo para la suma.

Por estas razones, el espacio definido no es un espacio vectorial.

## Parte e)
$$
\begin{align}
&\text{Suma:} &&(x_{1}, y_{1}) + (x_{2}, y_{2}) = (|x_{1} + x_{2}|, |y_{1} + y_{2}|) \\
&\text{Producto:} &&\lambda(x_{1}, y_{1}) = (|\lambda x_{1}|, |y_{1}|)
\end{align}
$$
Si analizamos lo que sucede con respecto a la suma de un vector con elementos negativos y el vector nulo $\vec{0}$, podemos ver que:
$$
(-x_{1}, -y_{1}) + (0, 0) = (|-x_{1} + 0|, |-y_{1} + 0|) = (|-x_{1}|, |-y_{1}|) = (x_{1}, y_{1})
$$
De esta forma, podemos ver que no existe un elemento nulo de la suma, ya que no existe un vector nulo, el cual al sumarse con otro vector cualquiera $u$ de como resultado $u$ (en caso de que $u$ tenga al menos un componente negativo).

De esta forma, el espacio definido no es un espacio vectorial.


---
# Ejercicio 2
Simplemente con analizar la definición del producto de un escalar por un vector, podemos ver que la operación no genera problemas, ya que un vector multiplicado por el escalar neutro del producto da el mismo vector, y cualquier vector por 0 da como resultado el vector nulo de dicho espacio: $\vec{0} = (0, 0, 1)$.

Por esta razón, nos enfocaremos en la operación suma de vectores. 
Estudiaremos la existencia de un vector neutro para la suma, tal que un vector cualquiera $u$ más el vector nulo, de como resultado $u$:
$$
(x_{1}, y_{1}, 1) + (0, 0, 1) = \left( \frac{x_{1} + 0}{2}, \frac{y_{1} + 0}{2}, 1 \right) = \left( \frac{x_{1}}{2}, \frac{y_{1}}{2}, 1 \right)
$$
De esta forma, obtuvimos que
$$
(x_{1}, y_{1}, 1) = \left( \frac{x_{1}}{2}, \frac{y_{1}}{2}, 1 \right)
$$

Es así que comprobamos que el espacio definido no es un espacio vectorial.

---
# Ejercicio 3
A continuación, se establecen los axiomas de espacio vectorial:
**Axiomas de suma**
$$(\forall u, v, w \in V)$$
$$
\begin{align}
&\text{(S1)} &&(u + v) + w = u + (v + w) \\
&\text{(S2)} &&u + v = v + u \\
&\text{(S3)} &&(+) \text{ tiene elemento neutro: } u + \vec{0} = u \\
&\text{(S4)} &&\text{Cada vector } u \in V \text{ tiene opuesto } -u: u + (-u) = \vec{0}
\end{align}
$$
**Axiomas de producto**
$$(\forall \alpha, \beta \in K, u, v, w \in V)$$
$$
\begin{align}
&\text{(P1)} &&\alpha \cdot (\beta \cdot u) = (\alpha \beta) \cdot u \\
&\text{(P2)} &&1_{K} \cdot u = u \\
&\text{(P3)} &&\alpha \cdot_{V} (u +_{V} v) = \alpha \cdot_{V} u + \alpha \cdot_{V} v \\
&\text{(P4)} &&(\alpha +_{K} \beta) \cdot_{V} u = \alpha \cdot_{V} u +_{V} \beta \cdot_{V} u
\end{align}
$$

## Parte a)
Vamos a partir de que existen $v_{1}, v_{2} \in V$ que verifican $v_{1} + v = v_{2} + v = v$.
$$
\begin{align}
v_{1} + v &= v \\
v_{1} + v - v &= v - v \\
v_{1} + v - v &= (v_{2} + v) - v \\
v_{1} + \cancel{ v } - \cancel{ v } &= v_{2} + \cancel{ v } - \cancel{ v } \\
v_{1} &= v_{2}
\end{align}
$$
Es así que demostramos que el neutro de la suma es único.

## Parte b)
Partimos de que dado $v \in V$, $v + v_{1} = v + v_{2} = 0_{V}$. Tenemos que demostrar que $v_{1} = v_{2}$.
$$
\begin{align}
v + v_{1} &= 0_{V} \\
v + v_{1} &= v + v_{2} \\
\cancel{ v } + v_{1} - \cancel{ v } &= \cancel{ v } + v_{2} - \cancel{ v } \\
v_{1} &= v_{2}
\end{align}
$$
Es así que demostramos que el opuesto es único.

## Parte c)
Partimos de que existe $0 \in \mathbb{K}$, siendo 0 el neutro de la suma. Tenemos que demostrar que $\forall v \in V, 0 \cdot v = 0_{K}$.
$$
0_{V} + 0 \cdot v = 0 \cdot v = (0 + 0) \cdot v = 0 \cdot v + 0 \cdot v
$$
Entonces:
$$
0_{V} + \cancel{ 0 \cdot v } = 0 \cdot v + \cancel{ 0 \cdot v }
$$
En conclusión:
$$
0_{V} = 0 \cdot v
$$

Es así que cualquier vector por el escalar nulo da como resultado el vector nulo.

## Parte d)
Partimos de que existe $0_{V} \in V$, siendo $0_{V}$ el vector nulo, neutro del espacio vectorial. Tenemos que demostrar que $\forall \lambda \in \mathbb{K}, \lambda0_{K} = 0_{K}$.

Partiremos considerando un vector $u$ y su opuesto $-u$ (que ya demostramos que es único).
$$
\begin{align}
u + (-u) &= 0_{V} \\
\lambda(u + (-u)) &= \lambda 0_{V} \\
\cancel{ \lambda u } + \cancel{ \lambda (-u) } &= \lambda 0_{V} \\
0_{V} &= \lambda 0_{V}
\end{align}
$$
En conclusión, demostramos que el producto de un escalar por el vector nulo siempre será el vector nulo.

## Parte e)
Tenemos que demostrar que para todo $v \in V$, el opuesto de $v$ es $(-1)v$, siendo $-1$ el opuesto de 1 en el cuerpo $\mathbb{K}$.
$$
v + (-1) \cdot v = 1 \cdot v + (-1) \cdot v = (1 + (-1)) \cdot v = 0 \cdot v = 0_{V}
$$
En conclusión, para todo vector $v \in V$, $(-1) \cdot v$ es el opuesto de $v$.

---
# Ejercicio 4
Una parte.

## Parte a)
En este caso, comenzaremos simplificando la operación propuesta que incluye a los vectores $v$ y $w$:
$$
\begin{align}
3v + 5w &= 7v - 2w \\
5w + 2w &= 7v - 3v \\
7w &= 4v
\end{align}
$$
De esta forma, sabemos que los vectores $w$ y $v$ son colineales. Ahora, proseguiremos a encontrar el valor que nos permite pasar de uno a otro:
$$
7w = 4v \implies \frac{7}{4}w = v \text{ y } w = \frac{4}{7}v
$$
En conclusión, existe un $\lambda \in \mathbb{R}$ tal que $\lambda v = w$ y $\lambda = \frac{4}{7}$.

---
# Ejercicio 6
Tenemos que comprobar si los conjuntos propuestos verifican las propiedades mencionadas durante el curso:
$$
\begin{align}
&(1) &&S \neq \emptyset \\
&(2) &&\forall \alpha, \beta \in K, \forall u, v \in S, \alpha \cdot u + \beta \cdot v \in S
\end{align}
$$
## Parte a)
Estamos estudiando el conjunto de las funciones que tienen raíz en $x_{0}$. Esto significa que $f(x_{0}) = 0$. Llamaremos a este subconjunto $S_{1}$.

Sabemos que el vector neutro ($f(x) = 0$) forma parte del conjunto, ya que tiene raíces en todos sus puntos, incluyendo $x_{0}$. Por lo tanto, el espacio no es vacío (existe al menos una función que tiene raíz en $x_{0}$).

Ahora, analicemos el resultado de las combinaciones lineales de elementos de dicho conjunto: si dos funciones tienen raíz en $x_{0}$, entonces el resultado de sumar ambas funciones también tendrá raíz en $x_{0}$. Además, si una función tiene raíz en $x_{0}$, el resultado de multiplicar un escalar por dicha función será otra función que mantendrá las mismas raíces.

De esta forma, si tenemos dos funciones cualesquiera $f$ y $g$ siendo que $f(x_{0}) = g(x_{0}) = 0$, y $\alpha, \beta \in \mathbb{R}, \alpha, \beta \neq 0$, entonces podemos afirmar que:
$$
\alpha f + \beta g \in S_{1}
$$

En conclusión, podemos afirmar que $S_{1}$ es un subespacio vectorial.

## Parte b)
Este caso es diferente al anterior, ya que trabajaremos con el subconjunto $S_{2}$, el cual contiene a las funciones que tienen al menos una raíz, sin importar en donde esté.

Comenzamos analizando el caso de la función nula. Esta tiene raíces en todos sus puntos, por lo cual pertenece al conjunto $S_{2}$.

Ahora, pasamos a verificar que cualquier combinación lineal también forma parte del conjunto definido. En este caso, tomaremos como referencia las siguientes funciones:
$$
\begin{align}
&f(x) = x^{2} \\
&g(x) = x + 10
\end{align}
$$
Si las estudiamos, cada una de estas funciones tiene una raíz:
$$
\begin{align}
&f(0) = 0 \\
&g(0) = -10
\end{align}
$$
Ahora, analicemos su suma:
$$
(f + g)(x) = x^{2} + x + 10
$$
$$
\begin{align}
&a = 1 \\
&b = 1 \\
&c = 10
\end{align}
$$
$$
\begin{align}
x &= \frac{-1 \pm \sqrt{ 1^{2} - 4 \cdot 1 \cdot 10 }}{2 \cdot 1} \\
&= \frac{-1 \pm \sqrt{ 1 - 40 }}{2} \\
&= \frac{-1 \pm \sqrt{ -39 }}{2}
\end{align}
$$
Como vemos, llegamos a la raíz de un número negativo, indicando que dicha función no tiene raíces reales.

De esta forma, no todas las combinaciones lineales con elementos de $S_{2}$ dan como resultado otro elemento de $S_{2}$.

En conclusión, podemos afirmar que $S_{2}$ no es un subespacio vectorial.

---
# Ejercicio 7
Cinco partes.

Para determinar si son espacios vectoriales o no, tomaremos como referencia las propiedades mencionadas en el ejercicio anterior.
## Parte a)
En este caso, sabemos que la matriz nula pertenece al conjunto, ya que la misma es simétrica.

Además, sabemos que el producto entre un escalar y una matriz simétrica da como resultado otra matriz simétrica.

Ahora, pasaremos a estudiar la suma de matrices. No hay ningún caso en el que la suma de dos matrices simétricas de como resultado una matriz que no sea simétrica.

De esta forma, si definimos $A, B \in M_{n \times n}(K)$ y dos escalares $\alpha, \beta \in \mathbb{K}$, podemos asegurar que:
$$
\alpha \cdot A + \beta \cdot B \in M_{n \times n}(K)
$$
En conclusión, el conjunto de las matrices simétricas es un subespacio vectorial.

## Parte c)
En este caso, partimos sabiendo que la matriz nula no forma parte del conjunto, ya que la misma no es invertible (no hay ninguna matriz que multiplicada por la matriz nula sea la matriz identidad).

En conclusión, el conjunto de las matrices invertibles no es un subespacio vectorial.

## Parte e)
En este caso, sabemos que la matriz nula no pertenece a ninguno de los conjuntos, puesto que la matriz nula tiene rango 0.

Por esta razón, sabemos que el conjunto de matrices de rango $k$ no es un espacio vectorial, a menos que consideremos $k = 0$. Ahora, estudiaremos dicho caso.

De esta forma, sabemos que la única matriz de rango 0 es la matriz nula, la cual cumple que:
- La matriz nula por cualquier escalar da como resultado la matriz nula.
- La suma entre dos matrices nulas da como resultado la matriz nula.

En conclusión, el conjunto de las matrices de rango $k$ es un subespacio vectorial únicamente para $k = 0$. Además, dicho espacio solo contiene a la matriz nula.

## Parte f)
Sabemos que la matriz nula forma parte del conjunto mencionado, ya que todos los elementos de la diagonal son 0, siendo su suma también 0.

Ahora, si tomamos una matriz no nula cuya traza es 0, y la multiplicamos por un escalar cualquiera diferente de 0, el resultado también será una matriz cuya traza es 0, ya que:
$$
x_{0} + x_{1} + \dots + x_{n - 1} + x_{n} = 0 \implies \lambda (x_{0} + x_{1} + \dots + x_{n - 1} + x_{n}) = 0
$$

Por último, si estudiamos el resultado de la suma de dos matrices cuya traza es 0, podemos ver que también se obtiene una matriz con dicha cualidad, ya que, si analizamos las trazas por separado:
$$
\begin{align}
&x_{0} + x_{1} + \dots + x_{n - 1} + x_{n} = 0 \\
&y_{0} + y_{1} + \dots + y_{n - 1} + y_{n} = 0
\end{align} \implies (x_{0} + x_{1} + \dots + x_{n - 1} + x_{n}) + (y_{0} + y_{1} + \dots + y_{n - 1} + y_{n}) = 0 + 0 = 0
$$

De esta forma, cualquier combinación lineal de matrices cuyas trazas sean 0, dará como resultado otra matriz cuya traza sea 0.

En conclusión, el conjunto de matrices de traza 0 es un subespacio vectorial.

## Parte j)
Sabemos que la matriz nula pertenece al conjunto mencionado, ya que la matriz nula elevado a cualquier número sigue siendo la matriz nula.

Ahora, si estudiamos el producto de un escalar por una matriz nilpotente, podemos ver que el mismo también es una matriz nilpotente, ya que simplemente se trata de un múltiplo de la matriz anterior.

Por ultimo, analizamos el caso de la suma de matrices nilpotentes. Estudiaremos un simple ejemplo:
$$
A = \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \text{ y } B = \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}
$$
Podemos ver que ambas son nilpotentes, ya que:
$$
\begin{align}
&A^{2} = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix} \\
&B^{2} = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix}
\end{align}
$$
Ahora, si analizamos la suma de ambos:
$$
A + B = \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
$$
$$
(A + B)^{2} = \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}, (A + B)^{3} = \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}, \dots
$$
Como vemos, los resultados oscilan entre las matrices $\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$ y $\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$, por lo que la matriz $A + B$ no es nilpotente.

En conclusión, el conjunto de las matrices nilpotentes no es un subespacio vectorial.

---
# Ejercicio 8
## Parte a)
Analizamos el subconjunto de $\mathbb{R}^{3}$ definido como:
$$
S = \{ (x, y, z) : \langle (x, y, z), (a, b, c) \rangle = d \}
$$
considerando $(a, b, c) \neq (0, 0, 0)$ fijo.

Si consideramos el vector nulo $(0, 0, 0)$:
$$
\langle (0, 0, 0), (a, b, c) \rangle = ||(0, 0, 0)|| \cdot ||(a, b, c)|| \cdot \cos \theta = 0 \cdot ||(a, b, c)|| \cdot \cos \theta = 0
$$
De esta forma, el vector nulo forma parte del conjunto si y sólo si $d = 0$. Por lo tanto, comenzaremos estableciendo dicha restricción.

Ahora, sabemos que esto siempre pasa para el vector nulo ya que su norma es 0. Sin embargo, cuando consideremos vectores no nulos, la norma de dicho vector no será nula, por lo que tenemos que buscar otra forma de anular el resultado. Sabemos que el vector $(a, b, c) \neq (0, 0, 0)$, por lo tanto, nos queda analizar el ángulo formado por los vectores $(x, y, z)$ y $(a, b, c)$. Sabemos que $\cos\left( \frac{\pi}{2} \right) = \cos\left( \frac{3\pi}{2} \right) = 0$, por lo que los vectores tienen que ser necesariamente ortogonales para asegurar que se satisface la condición $d = 0$.

De esta forma, para que el conjunto $S$ sea un subespacio vectorial del $\mathbb{R}$ espacio vectorial $\mathbb{R}^{3}$, tiene que cumplirse que $d = 0$, lo que implica que necesariamente los vectores $(x, y, z)$ sean ortogonales al vector $(a, b, c)$. En conclusión, el subespacio vectorial estará conformado por los vectores que pertenecen a la recta que pasa por $(0, 0, 0)$ y tiene como vector director a cualquier vector ortogonal a $(a, b, c)$. Por lo tanto, todos los vectores pertenecientes al espacio serán colineales entre sí, manteniendo esta propiedad en la suma y también para el producto por un escalar.

## Parte b)
Analizamos el subconjunto de $\mathbb{R}^{3}$ definido como:
$$
S = \{ (x, y, z) : (x, y, z) \land (a, b, c) = v \}
$$
considerando $(a, b, c) \neq (0, 0, 0)$ y $v \in \mathbb{R}^{3}$ fijos.

Si consideramos el vector nulo $(0, 0, 0)$:
$$
||(0, 0, 0) \land (a, b, c)|| = ||v|| \implies ||v|| = ||(0, 0, 0)|| \cdot ||(a, b, c)|| \cdot \sin(0) = 0 \cdot ||(a, b, c)|| \cdot 1 = 0
$$
De esta forma, el vector nulo forma parte del conjunto si y sólo si $||v|| = 0$. Por lo tanto, comenzaremos estableciendo dicha restricción:
$$
||v|| = 0 \implies v = \vec{0}
$$
Ahora, como el resultado del producto vectorial debe ser el vector nulo, y el resto de vectores con los que trabajaremos no serán nulos, tenemos que buscar una forma de anular el resultado. Sabemos que el vector $(a, b, c) \neq (0, 0, 0)$, por lo tanto, nos queda analizar el ángulo formado por los vectores $(x, y, z)$ y $(a, b, c)$. Sabemos que $\sin(0) = \cos(\pi) = 0$, por lo que los vectores tienen que ser necesariamente colineales para asegurar que se satisface la condición $v = \vec{0}$.

De esta forma, para que el conjunto $S$ sea un subespacio vectorial del $\mathbb{R}$ espacio vectorial $\mathbb{R}^{3}$, tiene que cumplirse que $v = \vec{0}$, lo que implica que necesariamente los vectores $(x, y, z)$ sean colineales al vector $(a, b, c)$. En conclusión, el subespacio vectorial estará conformado por los vectores que pertenecen a la recta que pasa por $(0, 0, 0)$ y tiene como vector director a $(a, b, c)$ o cualquier vector colineal al mismo. Por lo tanto, todos los vectores pertenecientes al espacio serán colineales entre sí, manteniendo esta propiedad en la suma y también para el producto por un escalar.

## Parte c)
Analizamos el subconjunto de $\mathbb{R}^{3}$ definido como:
$$
S = \{ (x, y, z) : ||(x, y, z)|| = r \}
$$
considerando $r \in \mathbb{R}$ fijo.

Si consideramos el vector nulo $(0, 0, 0)$:
$$
||(0, 0, 0)|| = 0 \implies r = 0
$$
De esta forma, el vector nulo forma parte del conjunto si y sólo si $r = 0$. Por lo tanto, comenzaremos estableciendo dicha restricción:
$$
r = 0
$$
Ahora, como la norma de los vectores del subespacio debe ser nula, solo hay una forma de que el subespacio sea un espacio vectorial: $(0, 0, 0)$ es el único elemento de $S$.

De esta forma, para que el conjunto $S$ sea un subespacio vectorial del $\mathbb{R}$ espacio vectorial $\mathbb{R}^{3}$, tiene que cumplirse que $r = 0$, y como esto solo se cumple para el vector $\vec{0} = (0, 0, 0)$, este será el único elemento del conjunto $S$. Es un subespacio vectorial válido, ya que contiene al vector nulo, es cerrado por suma de vectores ($\vec{0} + \vec{0} = \vec{0}$) y es cerrado por producto de un escalar por un vector ($\lambda \cdot \vec{0} = \vec{0}$).

---
# Ejercicio 9
Dos partes de cada uno de los ítems $a, b, c, d, e$.

## Parte a)
### Parte 2)
$$
S = \{ (a, b, c) \in \mathbb{R}^{3} : 3a - 2 = 3b + c \}
$$
Analizamos si el vector nulo $(0, 0, 0)$ forma parte del subespacio:
$$
\begin{align}
3 \cdot 0 - 2 &= 3 \cdot 0 + 0 \\
-2 &= 0
\end{align}
$$

Como vemos, el vector nulo no pertenece al conjunto, por lo que el conjunto $S$ no es un subespacio vectorial..

### Parte 4)
$$
S = \{ (a, a + b, a + b + c) \in \mathbb{R}^{3} : a, b, c \in \mathbb{R} \}
$$
Analizamos si el vector nulo $(0, 0, 0)$ forma parte del subespacio:
$$
\begin{align}
&(0, 0 + 0, 0 + 0 + 0) \\
&(0, 0, 0)
\end{align}
$$
Como vemos, el vector nulo pertenece al conjunto.

Ahora, pasamos a verificar como se comporta el conjunto con la suma de vectores. Consideramos dos vectores $u = (d, d + e, d + e + f), v = (g, g + h, g + h + i) \in \mathbb{R}^{3}$:
$$
u + v = (d, d + e, d + e + f) + (g, g + h, g + h + i) = (d + g, d + e + g + h, d + e + f + g + h + i)
$$
Como vemos, en el nuevo vector $a = d + g$, $b = e + h$, $c = f + i$, confirmando que cumple con la restricción $(a, a + b, a + b + c)$:
$$
\begin{align}
&a = d + g \\
&a + b = d + g + e + h = d + e + g + h \\
&a + b + c = d + e + g + h + f + i = d + e + f + g + h + i
\end{align}
$$

Ahora, analizaremos el producto por un escalar. Consideramos un vector $u = (d, d + e, d + e + f) \in \mathbb{R}^{3}$ y su producto por un escalar no nulo $\lambda$:
$$
\lambda u = \lambda (d, d + e, d + e + f) = (\lambda d, \lambda (d + e), \lambda (d + e + f)) = (\lambda d, \lambda d + \lambda e, \lambda d + \lambda e + \lambda f)
$$
En el vector $u$, $a = d$, $b = e$, $c = f$, mientras que en $\lambda u$, $a = \lambda d$, $b = \lambda e$, $c = \lambda f$, confirmando que la estructura $(a, a + b, a + b + c)$ se mantiene:
$$
\begin{align}
&a = \lambda d \\
&a + b = \lambda d + \lambda e \\
&a + b + c = \lambda d + \lambda e + \lambda f
\end{align}
$$

En conclusión, el subconjunto $S$ es un subespacio vectorial.

### Parte 6)
$$
S = \left\{ \left( \frac{b}{c}, b, c \right) \in \mathbb{R}^{3} : b, c \in \mathbb{R}, c \neq 0 \right\}
$$
Analizamos si el vector nulo $(0, 0, 0)$ forma parte del subespacio. En base a la definición del subconjunto, $c \neq 0$. Por esta razón, el vector nulo no pertenece al conjunto, por lo que el conjunto $S$ no es un subespacio vectorial.

## Parte b)
### Parte 2)
$$
S = \{ (x_{1}, \dots, x_{n}) \in \mathbb{R}^{n} : x_{1} = x_{2} = \dots = x_{n} \}
$$
Analizamos si el vector nulo $(0, \dots, 0)$ forma parte del subespacio. La condición de los vectores elementos de dicho subconjunto es que todos sus componentes sean iguales, cosa que el vector nulo cumple:
$$
x_{1} = x_{2} = \dots = x_{n} = 0 \implies (0, 0, \dots, 0) \in S
$$
De esta forma, el vector nulo pertenece al conjunto.

Ahora, analizamos la suma de vectores. Si tomamos dos vectores $u = (x_{1}, x_{2}, \dots, x_{n}), v = (y_{1}, y_{2}, \dots, y_{n}) \in S$, sabemos que $x_{1} = x_{2} = \dots = x_{n}$ y $y_{1} = y_{2} = \dots = y_{n}$. Desarrollamos su suma:
$$
u + v = (x_{1}, x_{2}, \dots, x_{n}) + (y_{1}, y_{2}, \dots, y_{n}) = (x_{1} + y_{1}, x_{2} + y_{2}, \dots, x_{n} + y_{n})
$$
Dicho vector cumple con la condición para pertenecer a $S$, partiendo de que $x_{1} = x_{2} = \dots = x_{n}$ y $y_{1} = y_{2} = \dots = y_{n}$, por lo que:
$$
x_{1} + y_{1} = x_{2} + y_{2} = \dots = x_{n} + y_{n} \implies u + v \in S
$$

Por último, estudiamos el producto por un escalar. Consideramos un vector $u = (x_{1}, x_{2}, \dots, x_{n}) \in S$ y un escalar $\lambda \neq 0$:
$$
\lambda u = \lambda (x_{1}, x_{2}, \dots, x_{n}) = (\lambda x_{1}, \lambda x_{2}, \dots, \lambda x_{n})
$$
Como el vector $u$ pertenece a $S$, entonces cumple que $x_{1} = x_{2} = \dots = x_{n}$, por lo que multiplicar cada una de sus componentes por el mismo escalar mantendrá la propiedad:
$$
x_{1} = x_{2} = \dots = x_{n} \implies \lambda x_{1} = \lambda x_{2} = \dots = \lambda x_{n} \implies \lambda u \in S
$$

En conclusión, determinamos que el conjunto $S$ es un subespacio vectorial.

### Parte 4)
$$
S = \{ (x_{1}, \dots, x_{n}) \in \mathbb{R}^{n} : x_{1} + x_{2} + \dots + x_{n} = 1 \}
$$
Analizamos si el vector nulo $(0, \dots, 0)$ forma parte del subespacio. Que la suma de todos los componentes de un vector tenga que ser 1, implica que no todos son nulos, por lo que el vector nulo no forma parte del subconjunto mencionado.

De esta forma, el conjunto $S$ no es un subespacio vectorial.

### Parte 6)
$$
S = \{ (x_{1}, \dots, x_{n}) \in \mathbb{R}^{n} : x_{i} \leq x_{j} \text{ para todo } i \leq j \}
$$
Analizamos si el vector nulo $(0, \dots, 0)$ forma parte del subespacio. La condición de los vectores elementos de dicho subconjunto es que cada componente es mayor o igual al anterior, cosa que el vector nulo cumple:
$$
x_{1} \leq x_{2} \leq \dots \leq x_{n} = 0 \implies (0, 0, \dots, 0) \in S
$$

Ahora, analizamos la suma de vectores. Si tomamos dos vectores $u = (x_{1}, x_{2}, \dots, x_{n}), v = (y_{1}, y_{2}, \dots, y_{n}) \in S$, sabemos que $x_{1} \leq x_{2} \leq \dots \leq x_{n}$ y $y_{1} \leq y_{2} \leq \dots \leq y_{n}$. Desarrollamos su suma:
$$
u + v = (x_{1}, x_{2}, \dots, x_{n}) + (y_{1}, y_{2}, \dots, y_{n}) = (x_{1} + y_{1}, x_{2} + y_{2}, \dots, x_{n} + y_{n})
$$
Dicho vector cumple con la condición para pertenecer a $S$, partiendo de que $x_{1} \leq x_{2} \leq \dots \leq x_{n}$ y $y_{1} \leq y_{2} \leq \dots \leq y_{n}$, por lo que:
$$
x_{1} + y_{1} \leq x_{2} + y_{2} \leq \dots \leq x_{n} + y_{n} \implies u + v \in S
$$

Por último, estudiamos el producto por un escalar. Consideramos un vector $u = (x_{1}, x_{2}, \dots, x_{n}) \in S$ y un escalar $\lambda \neq 0$:
$$
\lambda u = \lambda (x_{1}, x_{2}, \dots, x_{n}) = (\lambda x_{1}, \lambda x_{2}, \dots, \lambda x_{n})
$$
Como el vector $u$ pertenece a $S$, entonces cumple que $x_{1} \leq x_{2} \leq \dots \leq x_{n}$. Sin embargo, no podemos decir lo mismo de $\lambda u$, ya que la propiedad se mantiene si y sólo si $\lambda \geq 0$,:
$$
x_{1} \leq x_{2} \leq \dots \leq x_{n} \implies \lambda x_{1} \leq \lambda x_{2} \leq \dots \leq \lambda x_{n} \Longleftrightarrow \lambda > 0
$$
Por esta razón el producto no es cerrado, ya que si multiplicamos por un escalar negativo se invierte la desigualdad, haciendo que el vector no forme parte del subespacio.

En conclusión, determinamos que el conjunto $S$ no es un subespacio vectorial.

## Parte c)
### Parte 1)
$$
S = \{ p \in \mathbb{R}_{n}[x] : p(\alpha) = 0 \} \text{, donde } \alpha \in \mathbb{R} \text{ es un valor fijo}
$$
Analicemos si el polinomio nulo forma parte del conjunto. Sabemos que el polinomio nulo es simplemente 0, y es así para cualquier valor $\alpha$. De esta forma, es un elemento del conjunto $S$.

Ahora, analicemos la suma de polinomios. Si tenemos dos polinomios $p_{1}(x), p_{2}(x) \in S$ tal que $p_{1}(\alpha) = 0$ y $p_{2}(\alpha) = 0$, esto significa que ambos polinomios tienen raíz en $\alpha$. Si sumamos los polinomios:
$$
p_{3}(x) = p_{1}(x) + p_{2}(x) \implies p_{3}(\alpha) = p_{1}(\alpha) + p_{2}(\alpha) = 0 + 0 = 0
$$
Como vemos, la suma de polinomios que tienen raíz en $\alpha$ es exitosa, dando como resultado un nuevo polinomio que también tiene raíz en $\alpha$.

Por último, estudiaremos el producto por un escalar. Consideraremos un polinomio $p(x) \in S$, por lo que $p(\alpha) = 0$, y $\lambda \neq 0$:
$$
p(\alpha) = 0 \implies \lambda p(\alpha) = \lambda \cdot 0 = 0
$$
Podemos ver que, incluso cuando multiplicamos un polinomio por un escalar no nulo, las raíces se mantienen.

En conclusión, determinamos que el conjunto $S$ es un subespacio vectorial.

### Parte 4)
$$
S = \{ p \in \mathbb{R}_{n}[x] : p(1 - x) = p(1 + x) \space \forall x \in \mathbb{R} \}
$$
Analicemos si el polinomio nulo forma parte del conjunto. Sabemos que el polinomio nulo es simplemente 0, y es así para cualquier valor de $x$. De esta forma, es un elemento del conjunto $S$.

Ahora, analicemos la suma de polinomios. Si tenemos dos polinomios $p_{1}(x), p_{2}(x) \in S$ tal que $p_{1}(x - 1) = p_{1}(x + 1) \space \forall x \in \mathbb{R}$ y $p_{2}(1 - x) = p_{2}(1 + x) \space \forall x \in \mathbb{R}$. Si sumamos los polinomios:
$$
p_{3}(x) = p_{1}(x) + p_{2}(x) \implies \begin{cases}
p_{3}(1 - x) = p_{1}(1 - x) + p_{2}(1 - x) = p_{1}(1 + x) + p_{2}(1 + x) \\
p_{3}(1 + x) = p_{1}(1 + x) + p_{2}(1 + x) = p_{1}(1 - x) + p_{2}(1 - x)
\end{cases}
$$
$$
\implies p_{3}(1 - x) = p_{3}(1 + x)
$$
Como vemos, la suma de polinomios $p$ que cumplen que $p(1 - x) = p(1 + x)$, dando como resultado un nuevo polinomio que también verifica dicha propiedad.

Por último, estudiaremos el producto por un escalar. Consideraremos un polinomio $p(x) \in S$, por lo que $p(1 - x) = p(1 + x)$, y $\lambda \neq 0$:
$$
p(1 - x) = p(1 + x) \implies \lambda p(1 - x) = \lambda p(1 + x)
$$
Podemos ver que, incluso cuando multiplicamos un polinomio por un escalar no nulo, la igualdad se mantiene.

En conclusión, determinamos que el conjunto $S$ es un subespacio vectorial.

### Parte 5)
$$
S = \{ p \in \mathbb{R}_{n}[x] : p(x) \leq p(2x) \}
$$
Analicemos si el polinomio nulo forma parte del conjunto. Sabemos que el polinomio nulo es simplemente 0, y es así para cualquier valor de $x$, por lo que $p(x) = p(2x) = 0$. De esta forma, es un elemento del conjunto $S$.

Ahora, analicemos la suma de polinomios. Si tenemos dos polinomios $p_{1}(x), p_{2}(x) \in S$ tal que $p_{1}(x) \leq p_{1}(2x)$ y $p_{2}(x) \leq p_{2}(2x)$. Si sumamos los polinomios:
$$
p_{3}(x) = p_{1}(x) + p_{2}(x), \text{ como } p_{1}(x) \leq p_{1}(2x) \land p_{2}(x) \leq p_{2}(2x) \implies p_{1}(x) + p_{2}(x) \leq p_{1}(2x) + p_{2}(2x)
$$
$$
\implies p_{3}(x) = p_{1}(x) + p_{2}(x) \leq p_{1}(2x) + p_{2}(2x) = p_{3}(2x)
$$
Como vemos, la suma de polinomios $p$ que cumplen que $p(x) \leq p(2x)$, dando como resultado un nuevo polinomio que también verifica dicha propiedad.

Por último, estudiaremos el producto por un escalar. Consideraremos un polinomio $p(x) \in S$, por lo que $p(x) \leq p(2x)$, y $\lambda \neq 0$:
$$
p(x) \leq p(2x) \implies \lambda p(x) \leq \lambda p(2x)
$$
Como el polinomio $p(x)$ pertenece a $S$, entonces cumple que $p(x) \leq p(2x)$. Sin embargo, no podemos decir lo mismo de $\lambda p(x)$, ya que la propiedad se mantiene si y sólo si $\lambda \geq 0$,:
$$
p(x) \leq p(2x) \implies \lambda p(x) \leq \lambda p(2x) \Longleftrightarrow \lambda > 0
$$
Por esta razón el producto no es cerrado, ya que si multiplicamos por un escalar negativo se invierte la desigualdad, haciendo que el polinomio no forme parte del subespacio.

En conclusión, determinamos que el conjunto $S$ no es un subespacio vectorial.

## Parte d)
### Parte 2)
$$
S = \{ f \in \mathcal{F} : f(x^{2}) = f(x)^{2}, \forall x \in \mathbb{R} \}
$$
Analicemos si la función nula forma parte del conjunto. Sabemos que el polinomio nulo es simplemente 0, y es así para cualquier valor de $x$. De esta forma, cumple que $f(x^{2}) = f(x)^{2} = 0$ para todo $x \in \mathbb{R}$, perteneciendo a $S$.

Ahora, analicemos la suma de funciones. Si tenemos dos funciones $f_{1}(x), f_{2}(x) \in S$ tal que $f_{1}(x^{2}) = f_{1}(x)^{2}, \forall x \in \mathbb{R}$ y $f_{2}(x^{2}) = f_{2}(x)^{2}, \forall x \in \mathbb{R}$. Si sumamos las funciones:
$$
f_{3}(x) = f_{1}(x) + f_{2}(x), \text{ como } f_{1}(x^{2}) = f_{1}(x)^{2} \land f_{2}(x^{2}) = f_{2}(x)^{2} \implies f_{1}(x^{2}) + f_{2}(x^{2}) = f_{1}(x)^{2} + f_{2}(x)^{2}
$$
$$
\implies f_{3}(x^{2}) = f_{1}(x^{2}) + f_{2}(x^{2}) = f_{1}(x)^{2} + f_{2}(x)^{2} = f_{3}(x)^{2}
$$
Como vemos, la suma de funciones $f$ cumplen que $f(x^{2}) = p(x)^{2}$, dando como resultado una nueva función que también verifica dicha propiedad.

Por último, estudiaremos el producto por un escalar. Consideraremos una función $f(x) \in S$, por lo que $f(x^{2}) = f(x)^{2}$, y $\lambda \in \mathbb{R} \setminus \{ 0 \}$:
$$
f(x^{2}) = f(x)^{2} \implies \lambda f(x^{2}) = \lambda f(x)^{2}
$$
Podemos ver que, incluso cuando multiplicamos una función por un escalar no nulo, la igualdad se mantiene.

En conclusión, determinamos que el conjunto $S$ es un subespacio vectorial.

### Parte 4)
$$
S = \{ f \in \mathcal{F} : f \text{ es impar} \}
$$
Analicemos si el polinomio nulo forma parte del conjunto. Sabemos que el polinomio nulo es simplemente 0, y es así para cualquier valor de $x$. Por esta razón, no cumple que $f$ es impar, ya que $\forall x \in \mathbb{R}, f(x) = 0$, y 0 es un número par, de forma que la función nula no pertenece a $S$.

En conclusión, determinamos que el conjunto $S$ no es un subespacio vectorial.

### Parte 7)
$$
S = \{ f \in \mathcal{F} : f(x^{2}) = f(x)^{2}, \forall x \in \mathbb{R} \}
$$
Analicemos si la función nula forma parte del conjunto. Sabemos que el polinomio nulo es simplemente 0, y es así para cualquier valor de $x$. De esta forma tiene raíz en todo $x \in \mathbb{R}$, perteneciendo a $S$.

Ahora, analicemos la suma de funciones. Si tenemos dos funciones $f_{1}(x), f_{2}(x) \in S$ y dos reales $x_{1}, x_{2} \in \mathbb{R}, x_{1} \neq x_{2}$, tal que $f_{1}(x_{1}) = 0 \land f_{1}(x) > 0, \forall x \in \mathbb{R} \setminus \{ x_{1} \}$ y $f_{2}(x_{2}) = 0 \land f_{2}(x) > 0, \forall x \in \mathbb{R} \setminus \{ x_{2} \}$. Si sumamos las funciones:
$$
f_{3}(x) = f_{1}(x) + f_{2}(x), \text{ como } (f_{1}(x_{1}) = 0 \land f_{1}(x) > 0, \forall x \in \mathbb{R} \setminus \{ x_{1} \}) \land (f_{2}(x_{2}) = 0 \land f_{2}(x) > 0, \forall x \in \mathbb{R} \setminus \{ x_{2} \})
$$
$$
\implies \begin{align}
&f_{3}(x_{1}) = f_{1}(x_{1}) + f_{2}(x_{1}) = f_{2}(x_{1}) > 0 \\
&f_{3}(x_{2}) = f_{1}(x_{2}) + f_{2}(x_{2}) = f_{1}(x_{2}) > 0 \\
&f_{3}(x) = f_{1}(x) + f_{2}(x) > 0, \forall x \in \mathbb{R} \\
\end{align}
$$
Como vemos, la suma de funciones $f$ no verifican que la función resultante tenga alguna raíz.

En conclusión, determinamos que el conjunto $S$ no es un subespacio vectorial.

## Parte e)


---
# Ejercicio 10
$$
S = \begin{cases}
\alpha_{1,1}x_{1} + \dots + \alpha_{1,n}x_{n} = 0 \\
\alpha_{2,1}x_{1} + \dots + \alpha_{2,n}x_{n} = 0 \\
\vdots \\
\alpha_{m,1}x_{1} + \dots + \alpha_{m,n}x_{n} = 0
\end{cases}
$$
Analicemos las soluciones de $S$. Primero que nada, al tener $n$ incógnitas, las soluciones se representan mediante una n-upla ($x_{1}, \dots, x_{n}$).

En todos los sistemas homogéneos existe una solución trivial: todas las incógnitas se anulan. De esta forma, sabemos que $S$ contiene a la n-upla nula $(\underbrace{ 0, \dots, 0 }_{ n })$.

Ahora, analizamos el comportamiento de la suma de soluciones. consideraremos dos n-uplas, $(a_{1}, a_{2}, \dots, a_{n})$ y $(b_{1}, b_{2}, \dots, b_{n})$ tal que:
$$
\begin{cases}
\alpha_{1,1}a_{1} + \dots + \alpha_{1,n}a_{n} = 0 \\
\alpha_{2,1}a_{1} + \dots + \alpha_{2,n}a_{n} = 0 \\
\vdots \\
\alpha_{m,1}a_{1} + \dots + \alpha_{m,n}a_{n} = 0
\end{cases} \land
\begin{cases}
\alpha_{1,1}b_{1} + \dots + \alpha_{1,n}b_{n} = 0 \\
\alpha_{2,1}b_{1} + \dots + \alpha_{2,n}b_{n} = 0 \\
\vdots \\
\alpha_{m,1}b_{1} + \dots + \alpha_{m,n}b_{n} = 0
\end{cases}
$$
De esta manera, si sumamos ambas n-uplas:
$$
\begin{cases}
\overbrace{ (\alpha_{1,1}a_{1} + \dots + \alpha_{1,n}a_{n}) }^{ 0 } + \overbrace{ (\alpha_{1,1}b_{1} + \dots + \alpha_{1,n}b_{n}) }^{ 0 } = 0 \\
\overbrace{ (\alpha_{2,1}a_{1} + \dots + \alpha_{2,n}a_{n}) }^{ 0 } + \overbrace{ (\alpha_{2,1}b_{1} + \dots + \alpha_{2,n}b_{n}) }^{ 0 } = 0 \\
\vdots \\
\overbrace{ (\alpha_{m,1}a_{1} + \dots + \alpha_{m,n}a_{n}) }^{ 0 } + \overbrace{ (\alpha_{m,1}b_{1} + \dots + \alpha_{m,n}b_{n}) }^{ 0 } = 0
\end{cases} \implies \begin{cases}
0 + 0 = 0 \\
0 + 0 = 0 \\
\vdots \\
0 + 0 = 0
\end{cases}
$$
Como vemos, el subespacio es cerrado frente a la suma. Indirectamente determinamos que la n-upla $(a_{1} + b_{1}, \dots, a_{n} + b_{n})$ es solución de $S$.

Ahora, analicemos el producto por un escalar. Si tenemos una n-upla $(a_{1}, a_{2}, \dots, a_{n})$ solución de $S$ y un escalar $\lambda \in \mathbb{R}, \lambda \neq 0$ y desarrollamos el producto de ambos:
$$
\begin{cases}
\lambda \overbrace{ (\alpha_{1,1}a_{1} + \dots + \alpha_{1,n}a_{n}) }^{ 0 } = 0 \\
\lambda \overbrace{ (\alpha_{2,1}a_{1} + \dots + \alpha_{2,n}a_{n}) }^{ 0 } = 0 \\
\vdots \\
\lambda \overbrace{ (\alpha_{m,1}a_{1} + \dots + \alpha_{m,n}a_{n}) }^{ 0 } = 0
\end{cases} \implies \begin{cases}
\lambda \cdot 0 = 0 \\
\lambda \cdot 0 = 0 \\
\vdots \\
\lambda \cdot 0 = 0
\end{cases}
$$

Es así que demostramos que dicho subespacio es cerrado por el producto por un escalar. Indirectamente determinamos que la n-upla $(\lambda a_{1}, \dots, \lambda a_{n})$ es solución de $S$.

En conclusión, las soluciones de $S$ son un subespacio de $\mathbb{R}^{n}$.

---
# Ejercicio 13
Dos partes.



---
# Ejercicio 14
Tenemos que probar que los conjuntos
$$
\mathrm{Im} = \{ v \in M_{m \times 1} : \text{existe } u \in M_{n \times 1} \text{ tal que } v = Au \} \subset M_{m \times 1}
$$
y
$$
\mathrm{Ker} = \{ u \in M_{n \times 1} : Au = 0_{m \times 1} \} \subset M_{n \times 1}
$$
son subespacios vectoriales.

Primero, analicemos cuidadosamente la estructura de cada uno. Dada una matriz $A \in M_{m \times n}$
- $\mathrm{Im}$ es un subespacio vectorial de las matrices columna de tamaño $m \times 1$, donde se incluyen únicamente aquellas matrices columna $v \in M_{m \times 1}$, para las cuales existe una matriz columna $u \in M_{n \times 1}$, tal que pueden ser expresadas mediante el producto de la matriz $A$ y dicha columna.
- $\mathrm{Ker}$ es un subespacio vectorial de las matrices columna de tamaño $n \times 1$, donde se incluyen únicamente aquellas matrices columna $u \in M_{n \times 1}$, tal que el producto de la matriz $A$ y $u$ sea la matriz nula de tamaño $m \times 1$.

Comencemos por el subespacio $\mathrm{Im}$:
Si analizamos si contiene la matriz nula $0_{m \times 1}$, tiene que existir un vector $u \in M_{n \times 1}$ tal que $0_{m \times 1} = Au$. Si consideramos $u = 0_{n \times 1}$, vemos que la propiedad se cumple para cualquier matriz $A$.

Para que un vector forma parte del conjunto $\mathrm{Im}$, tiene que cumplir:
$$
\begin{pmatrix}
u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n} \\
u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n} \\
\vdots \\
u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n}
\end{pmatrix} = \begin{pmatrix}
v_{1,1} \\
v_{2,1} \\
\vdots \\
v_{m, 1}
\end{pmatrix}
$$
$$
\begin{cases}
u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n} = v_{1,1} \\
u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n} = v_{2,1} \\
\vdots \\
u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n} = v_{m,1}
\end{cases}
$$
Si estudiamos la suma de vectores elementos de $\mathrm{Im}$:
$$
\begin{align}
&v = Au \implies v \in \mathrm{Im} \\
&w = Az \implies w \in \mathrm{Im}
\end{align} \implies v + w \in \mathrm{Im}?
$$
Para que se cumpla que $v + w \in \mathrm{Im}$, tiene que verificarse que:
$$
\begin{cases}
(u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n}) + (z_{1,1}A_{1,1} + z_{2,1}A_{1,2} + \dots + z_{n,1}A_{1,n}) = v_{1,1} + w_{1, 1} \\
(u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n}) + (z_{1,1}A_{2,1} + z_{2,1}A_{2,2} + \dots + z_{n,1}A_{2,n}) = v_{2,1} + w_{2, 1} \\
\vdots \\
(u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n}) + (z_{1,1}A_{m,1} + z_{2,1}A_{m,2} + \dots + z_{n,1}A_{m,n}) = v_{m,1} + w_{m, 1}
\end{cases}
$$
Como $v, w \in \mathrm{Im}$, esto quiere decir que:
$$
\begin{align}
&\begin{cases}
u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n} = v_{1,1} \\
u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n} = v_{2,1} \\
\vdots \\
u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n} = v_{m,1}
\end{cases} \\ \\

&\begin{cases}
z_{1,1}A_{1,1} + z_{2,1}A_{1,2} + \dots + z_{n,1}A_{1,n} = w_{1, 1} \\
z_{1,1}A_{2,1} + z_{2,1}A_{2,2} + \dots + z_{n,1}A_{2,n} = w_{2, 1} \\
\vdots \\
z_{1,1}A_{m,1} + z_{2,1}A_{m,2} + \dots + z_{n,1}A_{m,n} = w_{m, 1}
\end{cases}
\end{align}
$$
De esta forma, podemos simplificar los casos para $v + w$:
$$
\begin{cases}
\overbrace{ (u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n}) }^{ v_{1, 1} } + \overbrace{ (z_{1,1}A_{1,1} + z_{2,1}A_{1,2} + \dots + z_{n,1}A_{1,n}) }^{ w_{1, 1} } = v_{1,1} + w_{1, 1} \\
\overbrace{ (u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n}) }^{ v_{2,1} } + \overbrace{ (z_{1,1}A_{2,1} + z_{2,1}A_{2,2} + \dots + z_{n,1}A_{2,n}) }^{ w_{2, 1} } = v_{2,1} + w_{2, 1} \\
\vdots \\
\overbrace{ (u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n}) }^{ v_{m,1} } + \overbrace{ (z_{1,1}A_{m,1} + z_{2,1}A_{m,2} + \dots + z_{n,1}A_{m,n}) }^{ w_{m, 1} } = v_{m,1} + w_{m, 1}
\end{cases} \implies \begin{cases}
v_{1,1} + w_{1, 1} = v_{1,1} + w_{1, 1} \\
v_{2,1} + w_{2, 1} = v_{2,1} + w_{2, 1} \\
\vdots \\
v_{m,1} + w_{m, 1} = v_{m,1} + w_{m, 1}
\end{cases}
$$
Entonces, la suma de vectores sigue formando parte del subespacio definido.


Ahora, analizamos el producto de un escalar por un vector:
$$
v = Au \implies v \in \mathrm{Im} \implies \lambda v \in \mathrm{Im}?
$$
Para que se cumpla que $\lambda v \in \mathrm{Im}$, tiene que verificarse que:
$$
\begin{cases}
\lambda v_{1,1}A_{1,1} + \lambda v_{2,1}A_{1,2} + \dots + \lambda v_{n,1}A_{1,n} = \lambda v_{1,1} \\
\lambda v_{1,1}A_{2,1} + \lambda v_{2,1}A_{2,2} + \dots + \lambda v_{n,1}A_{2,n} = \lambda v_{2,1} \\
\vdots \\
\lambda v_{1,1}A_{m,1} + \lambda v_{2,1}A_{m,2} + \dots + \lambda v_{n,1}A_{m,n} = \lambda v_{m,1}
\end{cases}
$$
Como $v \in \mathrm{Im}$, sabemos que:
$$
\begin{cases}
v_{1,1}A_{1,1} + v_{2,1}A_{1,2} + \dots + v_{n,1}A_{1,n} = v_{1,1} \\
v_{1,1}A_{2,1} + v_{2,1}A_{2,2} + \dots + v_{n,1}A_{2,n} = v_{2,1} \\
\vdots \\
v_{1,1}A_{m,1} + v_{2,1}A_{m,2} + \dots + v_{n,1}A_{m,n} = v_{m,1}
\end{cases}
$$
Entonces:
$$
\begin{cases}
\lambda\overbrace{ (v_{1,1}A_{1,1} + v_{2,1}A_{1,2} + \dots + v_{n,1}A_{1,n}) }^{ v_{1, 1} } = \lambda v_{1,1} \\
\lambda\overbrace{ (v_{1,1}A_{2,1} + v_{2,1}A_{2,2} + \dots + v_{n,1}A_{2,n}) }^{ v_{2,1} } = \lambda v_{2,1} \\
\vdots \\
\lambda\overbrace{ (v_{1,1}A_{m,1} + v_{2,1}A_{m,2} + \dots + v_{n,1}A_{m,n}) }^{ v_{m,1} } = \lambda v_{m,1}
\end{cases} \implies \begin{cases}
\lambda \cdot v_{1, 1} = \lambda v_{1,1} \\
\lambda \cdot v_{2, 1} = \lambda v_{2,1} \\
\vdots \\
\lambda \cdot v_{m, 1} = \lambda v_{m,1}
\end{cases}
$$
Como vemos, para el producto se cumple sin problemas, ya que si ya se verificaba cada una de las ecuaciones previamente, simplemente se multiplica el resultado (celda correspondiente de la matriz columna $v$): si un vector $v \in \mathrm{Im}$ entonces para cualquier escalar $\lambda$ se verifica que $\lambda v \in \mathrm{Im}$.

En conclusión, $\mathrm{Im}$ es un subespacio vectorial de $M_{m \times 1}$.



Proseguimos con el subespacio $\mathrm{Ker}$:
Para que contenga la matriz nula $u = 0_{n \times 1}$, entonces el producto $Au = 0_{m \times 1}$. Como vemos que la propiedad se cumple para cualquier matriz $A$, entonces la matriz nula pertenece a $\mathrm{Ker}$.

Ahora, para que otros vectores formen parte del conjunto, tiene que cumplirse que:
$$
\begin{pmatrix}
u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n} \\
u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n} \\
\vdots \\
u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n}
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
\vdots \\
0
\end{pmatrix}
$$
$$
\begin{cases}
u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n} = 0 \\
u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n} = 0 \\
\vdots \\
u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n} = 0
\end{cases}
$$
Si estudiamos la suma de vectores elementos de $\mathrm{Ker}$:
$$
\begin{align}
&Au = 0_{m \times 1} \implies u \in \mathrm{Ker} \\
&Av = 0_{m \times 1} \implies v \in \mathrm{Ker}
\end{align} \implies u + v \in \mathrm{Ker}?
$$
Para que se cumpla que $v + w \in \mathrm{Ker}$, tiene que verificarse que:
$$
\begin{cases}
(u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n}) + (v_{1,1}A_{1,1} + v_{2,1}A_{1,2} + \dots + v_{n,1}A_{1,n}) = 0 \\
(u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n}) + (v_{1,1}A_{2,1} + v_{2,1}A_{2,2} + \dots + v_{n,1}A_{2,n}) = 0 \\
\vdots \\
(u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n}) + (v_{1,1}A_{m,1} + v_{2,1}A_{m,2} + \dots + v_{n,1}A_{m,n}) = 0
\end{cases}
$$
Como $v, w \in \mathrm{Ker}$, esto quiere decir que:
$$
\begin{align}
&\begin{cases}
v_{1,1}A_{1,1} + v_{2,1}A_{1,2} + \dots + v_{n,1}A_{1,n} = 0 \\
v_{1,1}A_{2,1} + v_{2,1}A_{2,2} + \dots + v_{n,1}A_{2,n} = 0 \\
\vdots \\
v_{1,1}A_{m,1} + v_{2,1}A_{m,2} + \dots + v_{n,1}A_{m,n} = 0
\end{cases} \\ \\

&\begin{cases}
w_{1,1}A_{1,1} + v_{2,1}A_{1,2} + \dots + w_{n,1}A_{1,n} = 0 \\
w_{1,1}A_{2,1} + v_{2,1}A_{2,2} + \dots + w_{n,1}A_{2,n} = 0 \\
\vdots \\
w_{1,1}A_{m,1} + v_{2,1}A_{m,2} + \dots + w_{n,1}A_{m,n} = 0
\end{cases}
\end{align}
$$
De esta forma, podemos simplificar los casos para $v + w$:
$$
\begin{cases}
\overbrace{ (u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n}) }^{ 0 } + \overbrace{ (v_{1,1}A_{1,1} + v_{2,1}A_{1,2} + \dots + v_{n,1}A_{1,n}) }^{ 0 } = 0 \\
\overbrace{ (u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n}) }^{ 0 } + \overbrace{ (v_{1,1}A_{2,1} + v_{2,1}A_{2,2} + \dots + v_{n,1}A_{2,n}) }^{ 0 } = 0 \\
\vdots \\
\overbrace{ (u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n}) }^{ 0 } + \overbrace{ (v_{1,1}A_{m,1} + v_{2,1}A_{m,2} + \dots + v_{n,1}A_{m,n}) }^{ 0 } = 0
\end{cases} \implies \begin{cases}
0 + 0 = 0 \\
0 + 0 = 0 \\
\vdots \\
0 + 0 = 0
\end{cases}
$$
Entonces, la suma de vectores sigue formando parte del subespacio definido.

ACLARACIÓN: Se puede demostrar de forma más sencilla, mediante distributividad:

Como $u, v \in \mathrm{Ker}$, se cumple que $Au = 0$ y $Av = 0$.
Consideramos la operación $A(u + v)$. Aplicando distributividad y sustituyendo por valores conocidos:
$$
A(u + v) = Au + Av = 0 + 0 = 0
$$
De esta forma, $u + v \in \mathrm{Ker}$.



Ahora, analizamos el producto de un escalar por un vector:
$$
Au = 0_{m \times 1} \implies u \in \mathrm{Ker} \implies \lambda u \in \mathrm{Ker}?
$$
Para que se cumpla que $\lambda u \in \mathrm{Ker}$, tiene que verificarse que:
$$
\begin{cases}
\lambda u_{1,1}A_{1,1} + \lambda u_{2,1}A_{1,2} + \dots + \lambda u_{n,1}A_{1,n} = 0 \\
\lambda u_{1,1}A_{2,1} + \lambda u_{2,1}A_{2,2} + \dots + \lambda u_{n,1}A_{2,n} = 0 \\
\vdots \\
\lambda u_{1,1}A_{m,1} + \lambda u_{2,1}A_{m,2} + \dots + \lambda u_{n,1}A_{m,n} = 0
\end{cases}
$$
$$
\begin{cases}
\lambda\overbrace{ (u_{1,1}A_{1,1} + u_{2,1}A_{1,2} + \dots + u_{n,1}A_{1,n}) }^{ 0 } = 0 \\
\lambda\overbrace{ (u_{1,1}A_{2,1} + u_{2,1}A_{2,2} + \dots + u_{n,1}A_{2,n}) }^{ 0 } = 0 \\
\vdots \\
\lambda\overbrace{ (u_{1,1}A_{m,1} + u_{2,1}A_{m,2} + \dots + u_{n,1}A_{m,n}) }^{ 0 } = 0
\end{cases} \implies \begin{cases}
\lambda \cdot 0 = 0 \\
\lambda \cdot 0 = 0 \\
\vdots \\
\lambda \cdot 0 = 0
\end{cases}
$$
Como vemos, para el producto se cumple sin problemas, ya que si ya se verificaba cada una de las ecuaciones previamente, significa que cada una se anula, por lo que multiplicar cada una por un escalar no afectará el resultado: si un vector $u \in \mathrm{Ker}$ entonces para cualquier escalar $\lambda$ se verifica que $\lambda u \in \mathrm{Ker}$.

ACLARACIÓN: También se puede estudiar por asociatividad con escalares:
$$
A(\lambda u) = \lambda (Au)
$$
Sabiendo que $u \in \mathrm{Ker}$, entonces $Au = 0$, por lo que
$$
A(\lambda u) = \lambda (Au) = \lambda \cdot 0 = 0
$$
De esta forma, $\lambda u \in \mathrm{Ker}$.

En conclusión, $\mathrm{Ker}$ es un subespacio vectorial de $M_{n \times 1}$.