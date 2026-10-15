# Ejercicio 1
Hallar la base de un espacio vectorial significa hallar un subconjunto que sea a la vez linealmente independiente y generador del espacio:
$B$ es base de $V$ si:
$$
\alpha_{1} b_{1} + \alpha_{2} b_{2} + \dots + \alpha_{n} b_{n} = 0 \Longleftrightarrow \alpha_{1} = \alpha_{2} = \dots = \alpha_{n}
$$
$$
[B] = V
$$
Además, la dimensión de un subespacio está dada por la cantidad de elementos de todas sus bases (sabemos que todas sus bases tienen la misma cantidad de elementos).
## Parte a)
$$
V = \mathbb{R}^{3}, S = \{ (x, y, z) \in \mathbb{R}^{3} : x + 2y - z = 0 \}
$$
Determinemos una base del subespacio:
$$
z = x + 2y \implies (x, 2y, x + 2y)
$$
es un elemento cualquiera del subespacio.
De esta forma, consideremos $x = y = 1$ para definir la base:
$$
B = \{ (1, 0, 1), (0, 1, 1) \}
$$
Sabemos que tiene 2 elementos, ya que se trata de un plano, y el mismo tiene 2 "grados de libertad" (dos vectores directores que lo definen).
En conclusión, $B$ es base de $S$ y $dim(S) = 2$.

## Parte b)
$$
V = \mathbb{R}_{3}[x], S = \{ p \in \mathbb{R}_{3}[x] : p(2) = 0 \}
$$
El subespacio está compuestos por los polinomios de grado 3 o menos que cumplen que $p(2) = 0$ (tienen raíz en 2). De esta forma, podemos considerar, por ejemplo $x - 2$, el cual cumple con la condición dada. También están $x^{2} - 4$ y $x^{3} - 8$, para que nos hagamos una idea del estilo de elementos que conforman el espacio. Incluso, podríamos formar una base con los elementos mencionados:
$$
B = \{ x^{3} - 8, x^{2} - 4, x - 2 \}
$$
Si lo analizamos bien, todos los polinomios de grado 3 o menos que tienen raíz en 2 están construidos en base a estos. Además, ninguno de los polinomios mencionados puede construirse en base a los otros dos.

En conclusión, $B$ es base de $S$ y $dim(S) = 3$.

En general, vamos a ir viendo que, con cada restricción que se agrega al subespacio (a comparación del espacio general), la dimensión se reduce en 1. Por ejemplo, el espacio $V$ tiene dimensión 4, mientras que $S$ tiene dimensión 3.

## Parte c)
$$
V = \mathbb{R}_{3}[x], S = \{ p \in \mathbb{R}_{3}[x] : p(0) = 0, p'(0) = 0 \}
$$
Este caso es similar al anterior, pero se agrega una condición más: no solo se requiere que los polinomios tengan raíz en 0, sino que la derivada en 0 sea 0.

Sabemos que un polinomio que cumple esto es $x^{2}$. Lo mismo podemos decir de $x^{3}$. $x$ no lo cumple ya que la derivada en cualquier punto es 1. Tampoco podemos sumar constantes, ya que perderíamos la condición de raíz en 0. De esta manera:
$$
B = \{ x^{3}, x^{2} \}
$$

En conclusión, $B$ es base de $S$ y $dim(S) = 2$.

## Parte d)
$$
V = \mathcal{M}(\mathbb{R})_{3 \times 3}, S = \{ A \in \mathcal{M}_{3 \times 3}: A \text{ es simétrica} \}
$$
Que una matriz de tamaño $3 \times 3$ sea simétrica, significa que tiene la siguiente forma:
$$
\begin{pmatrix}
\alpha & \beta & \gamma \\
\beta & \mu & \epsilon \\
\gamma & \epsilon & \eta
\end{pmatrix}
$$
De esta manera, podemos definir matrices básicas, que mediante combinaciones lineales conformen todo el espacio de las matrices simétricas:
$$
B = \left\{ \begin{pmatrix}
1 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
1 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 1 \\
0 & 1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 1
\end{pmatrix} \right\}
$$

En conclusión, $B$ es base de $S$ y $dim(S) = 6$.

## Parte e)
$$
V = \mathcal{M}(\mathbb{R})_{2 \times 2}, S = \{ A \in \mathcal{M}_{2 \times 2}: tr(A) = 0\}
$$
Recordemos que la traza de una matriz es la suma de todos los elementos de la diagonal. De esta manera, que la traza sea 0 quiere decir que, dada una matriz
$$
\begin{pmatrix}
\alpha & \beta \\
\gamma & \mu
\end{pmatrix}
$$
se cumple que
$$
\alpha + \mu = 0 \implies \alpha = -\mu
$$
Al ser matrices $2 \times 2$, simplemente tiene que cumplirse que los dos elementos de la diagonal sean opuestos. Entonces, podemos definir una base como:
$$
B = \left\{ \begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right\}
$$

En conclusión, $B$ es base de $S$ y $dim(S) = 3$.

## Parte f)
$$
V = \mathbb{C}^{3}, S = \{ (x, y, z) \in \mathbb{R}^{3} : 2x - iy + z = 0 \}
$$
Como vemos, se trata de un plano en $\mathbb{C}^{3}$. Por lo tanto, sabemos que todas sus bases tendrán 2 elementos.
$$
z = -2x + iy \implies (2x, -iy, -2x + iy)
$$
es un elemento cualquiera del subespacio.
Entonces, podemos fijar $x$ e $y$:
$$
\begin{align}
&x = 1, y = 0 \implies z = -2 \cdot 1 + i \cdot 0 = -2 \\
&x = 0, y = 1 \implies z = -2 \cdot 0 + i \cdot 1 = i
\end{align}
$$

De esta forma, podemos definir la base:
$$
B = \{ (1, 0, -2), (0, 1, i) \}
$$
En conclusión, $B$ es base de $S$ y $dim(S) = 2$.

## Parte g)
$$
V = \mathcal{M}(\mathbb{C})_{2 \times 2}, S = \left\{ A \in \mathcal{M}(\mathbb{C})_{2 \times 2}: AB = BA \text{ con } B = \begin{pmatrix}
1 & i \\
0 & 1
\end{pmatrix} \right\}
$$
Determinemos cual es la forma de las matrices que conmutan con $B$:
$$
A \cdot B = \begin{pmatrix}
a_{1,1} & ia_{1,1} + a_{1,2} \\
a_{2,1} & ia_{2,1} + a_{2,2}
\end{pmatrix} = B \cdot A = \begin{pmatrix}
a_{1,1} + ia_{2,1} & a_{1,2} + ia_{2,2} \\
a_{2,1} & a_{2,2}
\end{pmatrix}
$$
Entonces:
$$
\begin{pmatrix}
a_{1,1} & ia_{1,1} + a_{1,2} \\
a_{2,1} & ia_{2,1} + a_{2,2}
\end{pmatrix} = \begin{pmatrix}
a_{1,1} + ia_{2,1} & a_{1,2} + ia_{2,2} \\
a_{2,1} & a_{2,2}
\end{pmatrix} \implies \begin{cases}
a_{1,1} = a_{1,1} + ia_{2,1} \\
ia_{1,1} + a_{1,2} = a_{1,2} + ia_{2,2} \\
a_{2,1} = a_{2,1} \\
ia_{2,1} + a_{2,2} = a_{2,2}
\end{cases}
$$
Aquí, podemos definir que:
$$
a_{1,1} = a_{1,1} + ia_{2,1} \implies ia_{2,1} = 0 \implies a_{2,1} = 0
$$
Podemos determinar lo mismo de la ecuación 4.
$$
ia_{1,1} + a_{1,2} = a_{1,2} + ia_{2,2} \implies ia_{1,1} = ia_{2,2} \implies a_{1,1} = a_{2,2}
$$
No podemos extraer más información de las ecuaciones brindadas, por lo que llegamos a la conclusión de que la matriz $A$ tiene la forma:
$$
A = \begin{pmatrix}
\alpha & \beta \\
0 & \alpha
\end{pmatrix}
$$
De esta forma, podemos formar una base para este estilo de matrices:
$$
B = \left\{ \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right\}
$$
En conclusión, $B$ es base de $S$ y $dim(S) = 2$.

---
# Ejercicio 2
Básicamente, tenemos que determinar si $A$ es LI, y en caso de no serlo, identificar y quitar el o los elementos redundantes.

## Parte a)
$$
V = \mathbb{R}^{3}, A = \{ (1, -1, 2), (4, -3, 7), (2, 0, 5), (1, 2, 6) \}
$$
$$
\alpha(1, -1, 2) + \beta(4, -3, 7) + \gamma(2, 0, 5) + \mu(1, 2, 6) = 0
$$
$$
\begin{cases}
\alpha + 4\beta + 2\gamma + \mu = 0 \\
-\alpha - 3\beta + 2\mu = 0 \\
2\alpha + 7\beta + 5 \gamma + 6 \mu = 0
\end{cases}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 4 & 2 & 1 & 0 \\
-1 & -3 & 0 & 2 & 0 \\
2 & 7 & 5 & 6 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
0 & 1 & 2 & 3 & 0 \\
-1 & -3 & 0 & 2 & 0 \\
0 & 1 & 5 & 10 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2} \\
&F_{3} \leftarrow F_{3} + 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 1 & 2 & 3 & 0 \\
-1 & -3 & 0 & 2 & 0 \\
0 & 0 & 3 & 7 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 1 & 2 & 3 & 0 \\
-1 & -3 & 0 & 2 & 0 \\
0 & 0 & 1 & \frac{7}{3} & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{3}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 1 & 0 & -\frac{5}{3} & 0 \\
-1 & -3 & 0 & 2 & 0 \\
0 & 0 & 1 & \frac{7}{3} & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 1 & 0 & -\frac{5}{3} & 0 \\
1 & 3 & 0 & -2 & 0 \\
0 & 0 & 1 & \frac{7}{3} & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 1 & 0 & -\frac{5}{3} & 0 \\
1 & 0 & 0 & 3 & 0 \\
0 & 0 & 1 & \frac{7}{3} & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 3F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 3 & 0 \\
0 & 1 & 0 & -\frac{5}{3} & 0 \\
0 & 0 & 1 & \frac{7}{3} & 0
\end{array}
\right)
\begin{align}
&F_{1} \longleftrightarrow F_{2}
\end{align}
$$
Si lo expresamos como un sistema:
$$
\begin{cases}
\alpha + 3\mu = 0 \\
\beta - \frac{5}{3}\mu = 0 \\
\gamma + \frac{7}{3}\mu = 0
\end{cases} \implies \begin{cases}
\alpha = -3\mu \\
\beta = \frac{5}{3}\mu \\
\gamma = -\frac{7}{3}\mu
\end{cases}
$$
De esta forma, comprobamos que el conjunto es LD, ya que podemos desarrollar una solución no trivial, por ejemplo $\alpha = -9, \beta = 5, \gamma = -7, \mu = 3$.

Podemos expresar el vector 4 (vector redundante) como combinación lineal del resto:
$$
\begin{align}
(1, 2, 6) &= 3(1, -1, 2) - \frac{5}{3}(4, -3, 7) + \frac{7}{3}(2, 0, 5) \\
&= (3, -3, 6) - \left( \frac{20}{3}, -5, \frac{35}{3} \right) + \left( \frac{14}{3}, 0, \frac{35}{3} \right) \\
&= \left( 3 - \frac{20}{3} + \frac{14}{3}, -3 + 5 - 0, 6 + \cancel{ \frac{35}{3} - \frac{35}{3} } \right) \\
&= \left( 1, 2, 6 \right)
\end{align}
$$
En conclusión, $B = \{ (1, -1, 2), (4, -3, 7), (2, 0, 5) \}$ es una base de $\mathbb{R}^{3}$, por lo tanto $dim(V) = 3$.

## Parte b)
$$
V = \mathcal{M}(\mathbb{R})_{2 \times 2}, A = \left\{ \begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 2
\end{pmatrix}, \begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
1 & 3 \\
3 & 1
\end{pmatrix}, \begin{pmatrix}
1 & 2 \\
2 & 1
\end{pmatrix} \right\}
$$
$$
\alpha \begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix} + \beta \begin{pmatrix}
0 & 0 \\
1 & 2
\end{pmatrix} + \gamma \begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix} + \mu \begin{pmatrix}
1 & 3 \\
3 & 1
\end{pmatrix} + \eta \begin{pmatrix}
1 & 2 \\
2 & 1
\end{pmatrix} = \vec{0}
$$
Sabemos que el espacio $\mathcal{M}(\mathbb{R})_{2 \times 2}$ es de dimensión 4, por lo que tenemos que encontrar un vector redundante y removerlo del conjunto para que sea una base.
$$
\begin{cases}
\alpha + \gamma + \mu + \eta = 0 \\
\alpha + 2\gamma + 3\mu + 2\eta = 0 \\
\alpha + \beta + 3\mu + 2\eta = 0 \\
\alpha + 2\beta + \gamma + \mu + \eta = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 1 & 1 & 1 & 0 \\
1 & 0 & 2 & 3 & 2 & 0 \\
1 & 1 & 0 & 3 & 2 & 0 \\
1 & 2 & 1 & 1 & 1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 1 & 1 & 1 & 0 \\
0 & 0 & 1 & 2 & 1 & 0 \\
0 & 1 & -1 & 2 & 1 & 0 \\
0 & 2 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} - F_{1} \\
&F_{4} \leftarrow F_{4} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 1 & 1 & 1 & 0 \\
0 & 0 & 1 & 2 & 1 & 0 \\
0 & 1 & -1 & 2 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow \frac{1}{2}F_{4}
\end{align}
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 1 & 1 & 1 & 0 \\
0 & 0 & 1 & 2 & 1 & 0 \\
0 & 0 & -1 & 2 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{4}
\end{align}
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 1 & 1 & 1 & 0 \\
0 & 0 & 2 & 0 & 0 & 0 \\
0 & 0 & -1 & 2 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 1 & 1 & 1 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 \\
0 & 0 & -1 & 2 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{2}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 1 & 1 & 1 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 2 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 1 & -1 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 2 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 0 & -1 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 2 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
Ahora, simplemente reordenamos las filas:
$$
\left(
\begin{array}{ccccc|c}
1 & 0 & 0 & -1 & 0 & 0 \\
0 & 1 & 0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 2 & 1 & 0 \\
\end{array}
\right)
$$
$$
\begin{cases}
\alpha - \mu = 0 \\
\beta = 0 \\
\gamma = 0 \\
2\mu + \eta = 0
\end{cases} \implies \begin{cases}
\alpha = \mu \\
\beta = 0 \\
\gamma = 0 \\
\eta = -2\mu
\end{cases}
$$
De esta forma, sabemos que el sistema tiene como solución $(1, 0, 0, 1, -2)$, considerando $\mu = 1$.

Analizando la matriz resultante, podemos ver que el vector 4 es el redundante, por lo que lo expresaremos en función del resto:
$$
\begin{align}
\begin{pmatrix}
1 & 3 \\
3 & 1
\end{pmatrix} &= -\begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix} + 2\begin{pmatrix}
1 & 2 \\
2 & 1
\end{pmatrix} \\
&= \begin{pmatrix}
-1 & -1 \\
-1 & -1
\end{pmatrix} + \begin{pmatrix}
2 & 4 \\
4 & 2
\end{pmatrix} \\
&= \begin{pmatrix}
-1 + 2 & -1 + 4 \\
-1 + 4 & -1 + 2
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 3 \\
3 & 1
\end{pmatrix}
\end{align}
$$
En conclusión,
$$
B = \left\{ \begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 2
\end{pmatrix}, \begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
1 & 2 \\
2 & 1
\end{pmatrix} \right\}
$$ es una base de $\mathcal{M}(\mathbb{R})_{2 \times 2}$, por lo tanto $dim(V) = 4$.

---
# Ejercicio 3
Ahora tenemos el caso contrario. Tenemos conjuntos LI incompletos, a los cuales les faltan elementos para que también se consideren generadores de sus respectivos espacios, y por lo tanto, bases. Lo que haremos es estudiar que elementos de la base canónica se pueden conformar con dichos vectores, y agregaremos los vectores faltantes.

## Parte a)
$$
V = \mathbb{R}^{4}, A = \{ (1, 0, 2, 2), (1, 1, 0, 0) \}
$$
Sabemos que $\mathbb{R}^{4}$ tiene dimensión 4, por lo que tendremos que agregar al menos dos vectores más para formar una base del espacio mencionado.

Probaremos formar vectores de la base canónica de $\mathbb{R}^{4}$, siendo la misma:
$$
B_{\text{canónica}} = \{ (1, 0, 0, 0), (0, 1, 0, 0), (0, 0, 1, 0), (0, 0, 0, 1) \}
$$
$$
\alpha(1, 0, 2, 2) + \beta(1, 1, 0, 0) = (1, 0, 0, 0)
$$
$$
\begin{cases}
\alpha + \beta = 1 \\
\beta = 0 \\
2\alpha = 0 \\
2\alpha = 0
\end{cases}
$$
Como vemos, el sistema anterior es incompatible, ya que $\alpha = \beta = 0$, pero $\alpha + \beta = 1$, por lo que necesariamente tenemos que agregar el vector al conjunto.

Probamos con otro vector, ahora considerando que tenemos $(1, 0, 0, 0)$ en el conjunto:
$$
\alpha(1, 0, 2, 2) + \beta(1, 1, 0, 0) + \gamma(1, 0, 0, 0) = (0, 1, 0, 0)
$$
$$
\begin{cases}
\alpha + \beta + \gamma = 0 \\
\beta = 1 \\
2\alpha = 0 \\
2\alpha = 0
\end{cases}
$$
Este sistema es compatible, ya que $\beta = 1$, $\alpha = 0$, y consideraremos $\gamma = -1$ tal que $\alpha + \beta + \gamma = 1 - 1 = 0$, por lo que no debemos agregar el vector al conjunto.

Probamos con otro vector:
$$
\alpha(1, 0, 2, 2) + \beta(1, 1, 0, 0) + \gamma(1, 0, 0, 0) = (0, 0, 1, 0)
$$
$$
\begin{cases}
\alpha + \beta + \gamma = 0 \\
\beta = 0 \\
2\alpha = 1 \\
2\alpha = 0
\end{cases}
$$
Este sistema es incompatible, ya que se visualiza una incoherencia: $2\alpha = 1$ y $2\alpha = 0$ a la vez. De esta forma, también agregamos $(0, 0, 1, 0)$ al conjunto.

Ya con estos dos vectores deberíamos haber agregado lo necesario para que $A$ sea un generador de $\mathbb{R}^{4}$, pero por si acaso, verificamos el último vector de la base canónica:
$$
\alpha(1, 0, 2, 2) + \beta(1, 1, 0, 0) + \gamma(1, 0, 0, 0) + \mu(0, 0, 1, 0) = (0, 0, 0, 1)
$$
$$
\begin{cases}
\alpha + \beta + \gamma = 0 \\
\beta = 0 \\
2\alpha + \mu = 0 \\
2\alpha = 1
\end{cases}
$$
$$
\begin{align}
&2\alpha = 1 \implies \alpha = \frac{1}{2} \\
&\beta = 0 \land \alpha = \frac{1}{2} \implies \alpha + \beta + \gamma = \frac{1}{2} + \gamma = 0 \implies \gamma = -\frac{1}{2} \\
&2\alpha + \mu = 0 \implies 1 + \mu = 0 \implies \mu = -1
&\end{align}
$$
Como vemos, logramos formar el vector $(0, 0, 0, 1)$ mediante la siguiente combinación lineal:
$$
\frac{1}{2}(1, 0, 2, 2) - \frac{1}{2}(1, 0, 0, 0) - (0, 0, 1, 0) = (0, 0, 0, 1)
$$

En conclusión, para que el conjunto $A$ sea un generador (y por lo tanto base) de $V$, tenemos que agregar los vectores $(1, 0, 0, 0)$ y $(0, 0, 1, 0)$:
$$
A = \{ (1, 0, 2, 2), (1, 1, 0, 0), (1, 0, 0, 0), (0, 0, 1, 0) \}
$$
para que sea base de $\mathbb{R}^{4}$.

## Parte b)
$$
V = \mathbb{R}_{3}[x], A = \{ 1 - x + x^{2}, x - x^{2} \}
$$
Ya que $\mathbb{R}_{3}[x]$ es un espacio vectorial de dimensión 4, tendremos que agregar al menos dos elementos para formar un generador del espacio. A simple vista, podemos ver que ninguno de los elementos posee $x^{3}$, por lo que tendremos que agregar dicho elemento. Ahora, estudiemos el resto de elementos:
$$
\begin{align}
\alpha(1 - x + x^{2}) + \beta(x - x^{2}) &= 1 \\
\alpha - \alpha x + \alpha x^{2} + \beta x - \beta x^{2} &= 1 \\
\text{Considerando } \alpha = \beta = 1 \\
1 - \cancel{ x } + \cancel{ x^{2} } + \cancel{ x } - \cancel{ x^{2} } &= 1 \\
1 &= 1
\end{align}
$$
El polinomio 1 se forma mediante la combinación lineal $\alpha(1 - x + x^{2}) + \beta(x - x^{2}) = 1$ con $\alpha = \beta = 1$.

Sabiendo que el polinomio constante 1 forma parte del espacio generado del conjunto, podemos utilizarlo para formar otros:
$$
\begin{align}
\alpha(1 - x + x^{2}) + \beta(x - x^{2}) &= x^{2} \\
\alpha - \alpha x + \alpha x^{2} + \beta x - \beta x^{2} &= x^{2} \\
\text{Considerando } \alpha = 0 \text{ y } \beta = 1 \\
x - x^{2} &= x^{2}
\end{align}
$$
El problema es que por la forma de los vectores:
$$
\begin{align}
1 - x + x^{2} = (0, 1, -1, 1) \\
x - x^{2} = (0, -1, 1, 0) \\
\end{align}
$$
Si consideramos coeficientes iguales, siempre nos queda solo el polinomio constante 1, y si los coeficientes son diferentes, siempre nos quedan los términos $\alpha x + \beta x^{2}$, con $\alpha = \beta$. Por esta razón, es necesario agregar al menos uno de los dos polinomios, pudiendo elegir cualquiera. En este caso, agregaremos $x^{2}$.

En conclusión, para que el conjunto $A$ sea un generador (y por lo tanto base) de $V$, tenemos que agregar los polinomios $x^{2}$ y $x^{3}$:
$$
A = \{ 1 - x + x^{2}, x - x^{2}, x^{2}, x^{3} \}
$$
para que sea base de $\mathbb{R}_{3}[x]$.

---
# Ejercicio 4
Para probar que cada conjunto $\mathcal{B}$ es una base de $V$, probaremos que es LI, además de que se pueden conformar los elementos de la base canónica de $V$ (o sea, $\mathcal{B}$ es generador de $V$). Luego, determinaremos las coordenadas del vector $v$ ajustadas a la base proporcionada.

## Parte a)
$$
\mathcal{B} = \{ (1, 1, 0), (0, 1, 1), (1, 0, 1) \}, V = \mathbb{R}^{3}, \text{ y } v = (1, 2, 3)
$$
Verificamos que $\mathcal{B}$ es LI:
$$
\alpha(1, 1, 0) + \beta(0, 1, 1) + \gamma(1, 0, 1) = \vec{0}
$$
$$
\begin{cases}
\alpha + \gamma = 0 \\
\alpha + \beta = 0 \\
\beta + \gamma = 0
\end{cases}
$$
$$
\begin{align}
&\beta + \gamma = 0 \implies \gamma = -\beta \\
&\alpha + \gamma = \alpha - \beta = 0 \\
&\alpha - \beta = 0 \land \alpha + \beta = 0 \implies (\alpha - \beta) + (\alpha + \beta) = 2\alpha = 0 \implies \alpha = 0 \\
&\alpha + \beta = 0 \implies \beta = 0 \implies \gamma = 0
\end{align}
$$
En conclusión, la única solución posible es la trivial, por lo que $\mathcal{B}$ es LI.

Ahora, verificamos que $\mathcal{B}$ es un generador de $V$:

Como $\mathcal{B}$ es LI y tiene 3 elementos, sabiendo que estamos trabajando en el espacio vectorial $\mathbb{R}^{3}$, el cual tiene dimensión 3, podemos determinar directamente que $\mathcal{B}$ es generador de $\mathbb{R}^{3}$. Por lo tanto, $\mathcal{B}$ es una base de $\mathbb{R}^{3}$.

Ahora, determinamos las coordenadas del vector $v$ en la base $\mathcal{B}$:
$$
\alpha(1, 1, 0) + \beta(0, 1, 1) + \gamma(1, 0, 1) = (1, 2, 3)
$$
$$
\begin{cases}
\alpha + \gamma = 1 \\
\alpha + \beta = 2 \\
\beta + \gamma = 3
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 1 & 1 \\
1 & 1 & 0 & 2 \\
0 & 1 & 1 & 3
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 1 & 1 \\
0 & 1 & -1 & 1 \\
0 & 1 & 1 & 3
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 1 & 1 \\
0 & 1 & -1 & 1 \\
0 & 0 & 2 & 2
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 1 & 1 \\
0 & 1 & -1 & 1 \\
0 & 0 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{2}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 2 \\
0 & 0 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3} \\
&F_{2} \leftarrow F_{2} + F_{3}
\end{align}
$$
Entonces, podemos expresar el vector $v$ mediante la siguiente combinación lineal:
$$
0 \cdot (1, 1, 0) + 2 \cdot (0, 1, 1) + 1 \cdot (1, 0, 1) = (1, 2, 3)
$$

En conclusión, las coordenadas del vector $v$ en la base $\mathcal{B}$ son:
$$
coord(v) = (0, 2, 1)
$$

## Parte b)
$$
\mathcal{B} = \{ -1, x - 1, x^{2} - 1 \}, V = \mathbb{R}_{2}[x], \text{ y } v = x^{2} + x + 1
$$
Verificamos que $\mathcal{B}$ es LI:
$$
\alpha(-1) + \beta(x - 1) + \gamma(x^{2} - 1) = \vec{0}
$$
Lo analizamos por sus coeficientes (comenzando por el elemento de menor grado):
$$
\begin{cases}
-\alpha - \beta - \gamma = 0 \\
\beta = 0 \\
\gamma = 0
\end{cases}
$$
$$
\beta = \gamma = 0 \implies -\alpha - \beta - \gamma = -\alpha = 0 \implies \alpha = 0
$$
En conclusión, la única solución posible es la trivial, por lo que $\mathcal{B}$ es LI.

Ahora, verificamos que $\mathcal{B}$ es un generador de $V$:

Como $\mathcal{B}$ es LI y tiene 3 elementos, sabiendo que estamos trabajando en el espacio vectorial $\mathbb{R}_{2}[x]$, el cual tiene dimensión 3, podemos determinar directamente que $\mathcal{B}$ es generador de $\mathbb{R}_{2}[x]$. Por lo tanto, $\mathcal{B}$ es una base de $\mathbb{R}_{2}[x]$.

Ahora, determinamos las coordenadas del vector $v$ en la base $\mathcal{B}$:
$$
\alpha(-1) + \beta(x - 1) + \gamma(x^{2} - 1) = x^{2} + x + 1
$$
Lo analizamos por sus coeficientes (comenzando por el elemento de menor grado):
$$
\begin{cases}
-\alpha - \beta - \gamma = 1 \\
\beta = 1 \\
\gamma = 1
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
-1 & -1 & -1 & 1 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
-1 & 0 & -1 & 2 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
-1 & 0 & 0 & 3 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -3 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow -F_{1}
\end{align}
$$
Entonces, podemos expresar el vector $v$ mediante la siguiente combinación lineal:
$$
-3(-1) + (x - 1) + (x^{2} - 1) = x^{2} + x + 1
$$

En conclusión, las coordenadas del vector $v$ en la base $\mathcal{B}$ son:
$$
coord(v) = (-3, 1, 1)
$$

## Parte c)
$$
\mathcal{B} = \left\{ \begin{pmatrix}
2 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
2 & 3 \\
1 & 5
\end{pmatrix}, \begin{pmatrix}
4 & -1 \\
2 & 2
\end{pmatrix} \right\}, V = \mathcal{M}(\mathbb{R})_{2 \times 2}, \text{ y } v = \begin{pmatrix}
1 & 3 \\
-4 & 6
\end{pmatrix}
$$
Verificamos que $\mathcal{B}$ es LI:
$$
\alpha \begin{pmatrix}
2 & 0 \\
1 & 0
\end{pmatrix} + \beta \begin{pmatrix}
1 & 0 \\
1 & 0
\end{pmatrix} + \gamma \begin{pmatrix}
2 & 3 \\
1 & 5
\end{pmatrix} + \mu \begin{pmatrix}
4 & -1 \\
2 & 2
\end{pmatrix} = \vec{0}
$$
$$
\begin{cases}
2\alpha + \beta + 2\gamma + 4\mu = 0 \\
3\gamma - \mu = 0 \\
\alpha + \beta + \gamma + 2\mu = 0 \\
5\gamma + 2\mu = 0
\end{cases}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 1 & 2 & 4 & 0 \\
0 & 0 & 3 & -1 & 0 \\
1 & 1 & 1 & 2 & 0 \\
0 & 0 & 5 & 2 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 1 & 2 & 0 \\
0 & 0 & 3 & -1 & 0 \\
1 & 1 & 1 & 2 & 0 \\
0 & 0 & 11 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3} \\
&F_{4} \leftarrow F_{4} + 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 1 & 2 & 0 \\
0 & 0 & 3 & -1 & 0 \\
1 & 1 & 1 & 2 & 0 \\
0 & 0 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow \frac{1}{11}F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 2 & 0 \\
0 & 0 & 0 & -1 & 0 \\
1 & 1 & 0 & 2 & 0 \\
0 & 0 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{4} \\
&F_{2} \leftarrow F_{2} - 3F_{4} \\
&F_{3} \leftarrow F_{3} - F_{4} \\
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 2 & 0 \\
0 & 0 & 0 & 1 & 0 \\
1 & 1 & 0 & 2 & 0 \\
0 & 0 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
1 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{2} \\
&F_{3} \leftarrow F_{3} - 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
Reordenamos las filas:
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 0
\end{array}
\right)
$$

En conclusión, la única solución posible es la trivial, por lo que $\mathcal{B}$ es LI.

Ahora, verificamos que $\mathcal{B}$ es un generador de $V$:

Como $\mathcal{B}$ es LI y tiene 4 elementos, sabiendo que estamos trabajando en el espacio vectorial $\mathcal{M}(\mathbb{R})_{2 \times 2}$, el cual tiene dimensión 4, podemos determinar directamente que $\mathcal{B}$ es generador de $\mathcal{M}(\mathbb{R})_{2 \times 2}$. Por lo tanto, $\mathcal{B}$ es una base de $\mathcal{M}(\mathbb{R})_{2 \times 2}$.

Ahora, determinamos las coordenadas del vector $v$ en la base $\mathcal{B}$:
$$
\alpha \begin{pmatrix}
2 & 0 \\
1 & 0
\end{pmatrix} + \beta \begin{pmatrix}
1 & 0 \\
1 & 0
\end{pmatrix} + \gamma \begin{pmatrix}
2 & 3 \\
1 & 5
\end{pmatrix} + \mu \begin{pmatrix}
4 & -1 \\
2 & 2
\end{pmatrix} = \begin{pmatrix}
1 & 3 \\
-4 & 6
\end{pmatrix}
$$
$$
\begin{cases}
2\alpha + \beta + 2\gamma + 4\mu = 1 \\
3\gamma - \mu = 3 \\
\alpha + \beta + \gamma + 2\mu = -4 \\
5\gamma + 2\mu = 6
\end{cases}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 1 & 2 & 4 & 1 \\
0 & 0 & 3 & -1 & 3 \\
1 & 1 & 1 & 2 & -4 \\
0 & 0 & 5 & 2 & 6
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 1 & 2 & 5 \\
0 & 0 & 3 & -1 & 3 \\
1 & 1 & 1 & 2 & -4 \\
0 & 0 & 11 & 0 & 12
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3} \\
&F_{4} \leftarrow F_{4} + 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 1 & 2 & 5 \\
0 & 0 & 3 & -1 & 3 \\
1 & 1 & 1 & 2 & -4 \\
0 & 0 & 1 & 0 & \frac{12}{11}
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow \frac{1}{11}F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 2 & \frac{43}{11} \\
0 & 0 & 0 & -1 & -\frac{3}{11} \\
1 & 1 & 0 & 2 & -\frac{56}{11} \\
0 & 0 & 1 & 0 & \frac{12}{11}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{4} \\
&F_{2} \leftarrow F_{2} - 3F_{4} \\
&F_{3} \leftarrow F_{3} - F_{4} \\
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 2 & \frac{43}{11} \\
0 & 0 & 0 & 1 & \frac{3}{11} \\
1 & 1 & 0 & 2 & -\frac{56}{11} \\
0 & 0 & 1 & 0 & \frac{12}{11}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & \frac{37}{11} \\
0 & 0 & 0 & 1 & \frac{3}{11} \\
1 & 1 & 0 & 0 & -\frac{62}{11} \\
0 & 0 & 1 & 0 & \frac{12}{11}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{2} \\
&F_{3} \leftarrow F_{3} - 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & \frac{37}{11} \\
0 & 0 & 0 & 1 & \frac{3}{11} \\
0 & 1 & 0 & 0 & -9 \\
0 & 0 & 1 & 0 & \frac{12}{11}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
Reordenamos las filas:
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & \frac{37}{11} \\
0 & 1 & 0 & 0 & -9 \\
0 & 0 & 1 & 0 & \frac{12}{11} \\
0 & 0 & 0 & 1 & \frac{3}{11}
\end{array}
\right)
$$



Entonces, podemos expresar el vector $v$ mediante la siguiente combinación lineal:
$$
\frac{37}{11} \begin{pmatrix}
2 & 0 \\
1 & 0
\end{pmatrix} - 9 \begin{pmatrix}
1 & 0 \\
1 & 0
\end{pmatrix} + \frac{12}{11} \begin{pmatrix}
2 & 3 \\
1 & 5
\end{pmatrix} + \frac{3}{11} \begin{pmatrix}
4 & -1 \\
2 & 2
\end{pmatrix} = \begin{pmatrix}
1 & 3 \\
-4 & 6
\end{pmatrix}
$$

En conclusión, las coordenadas del vector $v$ en la base $\mathcal{B}$ son:
$$
coord(v) = \left( \frac{37}{11}, -9, \frac{12}{11}, \frac{3}{11} \right)
$$

---
# Ejercicio 5
Tenemos el conjunto
$$
\mathcal{A} = \{ 1 + t, 1 + \alpha t + t^{2}, 1 + t^{2} \}
$$
y queremos discutir, dependiendo del parámetro $\alpha$, en que contexto el conjunto es una base de $\mathbb{R}_{2}[t]$.

Primero que nada, sabemos que $dim(\mathbb{R}_{2}[t]) = \# \mathcal{A} = 3$, por lo que tiene la cantidad de elementos suficiente. Ahora, tenemos que verificar que el conjunto sea LI. En caso de ser LI, confirmaremos que $\mathcal{A}$ es una base de $\mathbb{R}_{2}[t]$, y por lo tanto: $[\mathcal{A}] = \mathbb{R}_{2}[t]$.

Estudiamos la siguiente igualdad:
$$
a(1 + t) + b(1 + \alpha t + t^{2}) + c(1 + t^{2}) = \vec{0}
$$
Analizaremos los polinomios en forma de terna:
$$
\begin{align}
&1 + t = (1, 1, 0) \\
&1 + \alpha t + t^{2} = (1, \alpha, 1) \\
&1 + t^{2} = (1, 0, 1)
\end{align}
$$
$$
\begin{cases}
a + b + c = 0 \\
a + \alpha b = 0 \\
b + c = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
1 & \alpha & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 0 \\
1 & \alpha & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 0 \\
0 & \alpha & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$

Ahora, tenemos dos tipos de situaciones:

- $\alpha = 0$:
En este caso, la fila 2 se anula:
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
$$
Entonces, tenemos un sistema del siguiente tipo:
$$
\begin{cases}
a = 0 \\
b + c = 0 \implies b = -c
\end{cases}
$$
De esta forma, vemos que el sistema tiene más soluciones que simplemente la solución trivial. Por ejemplo, podríamos considerar $(0, 1, -1)$. En base a la matriz final, si estudiamos los vectores considerando $\alpha = 0$, podemos ver que:
$$
\mathcal{A} = \{ 1 + t, 1 + \cancel{ \alpha t } + t^{2}, 1 + t^{2} \} \implies \mathcal{A} = \{ 1 + t, 1 + t^{2}, 1 + t^{2} \}
$$
El polinomio 2 es redundante, ya que se anuló el término que lo distinguía del polinomio 3. Por esta razón, podemos removerlo del conjunto para asegurar que sea LI:
$$
\mathcal{A} = \{ 1 + t, 1 + t^{2} \}
$$
Ahora, tendríamos que agregar un término más para asegurar que $\mathcal{A}$ sea base de $\mathbb{R}_{2}[t]$. Consideremos el polinomio constante 1:
$$
a(1 + t) + b(1 + t^{2}) = 1 = 1 + 0t + 0t^{2}
$$
$$
\begin{cases}
a + b = 1 \\
a = 0 \\
b = 0
\end{cases}
$$
$$
a = b = 0 \implies a + b \neq 1
$$
Como vemos, el sistema es incompatible, por lo que podemos agregar el polinomio y mantendremos la libertad del conjunto:
$$
\mathcal{A} = \{ 1, 1 + t, 1 + t^{2} \}
$$
Ahora, estamos seguros de que $\mathcal{A}$ es una base de $\mathbb{R}_{2}[t]$.

- $\alpha \neq 0$
En este caso, podemos escalerizar la matriz:
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 0 \\
0 & \alpha & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{\alpha}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{\alpha}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
Probamos que la única combinación que general el vector nulo es la solución trivial del sistema.

Por esta razón, el sistema es LI, lo que significa que, efectivamente, $\mathcal{A}$ es una base de $\mathbb{R}_{2}[t]$, al menos cuando $\alpha \neq 0$.



---
# Ejercicio 7
Una parte.

## Parte c)
$$
A = \begin{pmatrix}
1 & 2 & 3 & -4 & 8 \\
1 & 2 & 0 & 2 & 8 \\
2 & 4 & -3 & 10 & 9 \\
3 & 6 & 0 & 6 & 9
\end{pmatrix}
$$
Primeramente, escalerizamos la matriz:
$$
A = \begin{pmatrix}
0 & 0 & 3 & -6 & 0 \\
1 & 2 & 0 & 2 & 8 \\
0 & 0 & -3 & 6 & -7 \\
0 & 0 & 0 & 0 & -15
\end{pmatrix}
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2} \\
&F_{3} \leftarrow F_{3} - 2F_{2} \\
&F_{4} \leftarrow F_{4} - 3F_{2}
\end{align}
$$
$$
A = \begin{pmatrix}
0 & 0 & 3 & -6 & 0 \\
1 & 2 & 0 & 2 & 8 \\
0 & 0 & 0 & 0 & -7 \\
0 & 0 & 0 & 0 & 1
\end{pmatrix}
\begin{align}
&F_{3} \leftarrow F_{3} + F_{1} \\
&F_{4} \leftarrow -\frac{1}{15} F_{4}
\end{align}
$$
$$
A = \begin{pmatrix}
0 & 0 & 3 & -6 & 0 \\
1 & 2 & 0 & 2 & 0 \\
0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 1
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow F_{2} - 8F_{4} \\
&F_{3} \leftarrow F_{3} + 7F_{4}
\end{align}
$$
$$
A = \begin{pmatrix}
0 & 0 & 1 & -2 & 0 \\
1 & 2 & 0 & 2 & 0 \\
0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 1
\end{pmatrix}
\begin{align}
&F_{1} \leftarrow \frac{1}{3}F_{1}
\end{align}
$$
Como vemos, logramos anular una fila de la matriz, por lo que, estando en forma escalerizada reducida, su rango es 3.

Ahora, tenemos que estudiar el espacio
$$
Ker A = \{ X \in M_{5 \times 1}(\mathbb{K}) : AX = 0 \}
$$
Consideraremos la matriz escalerizada para facilitar los cálculos:
$$
AX = \begin{pmatrix}
x_{3} - 2x_{4} \\
x_{1} + 2x_{2} + 2x_{4} \\
x_{5}
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix}
$$
De esta forma, tenemos que estudiar el sistema:
$$
\begin{cases}
x_{3} - 2x_{4} = 0 \\
x_{1} + 2x_{2} + 2x_{4} = 0 \\
x_{5} = 0
\end{cases} \implies \begin{align}
&x_{3} = 2x_{4} \\
&x_{1} + 2x_{2} = -2x_{4}
\end{align}
$$
De esta manera, las matrices (en realidad podemos considerarlas quíntuplas) que forman parte de este sistema tienen la forma:
$$
X = \left( x_{1}, x_{2}, -x_{1} - 2x_{2}, -\frac{1}{2}x_{1} - x_{2}, 0 \right)
$$
Consideremos $x_{1} = 1, x_{2} = 0$ y $x_{1} = 0, x_{2} = 1$:
$$
\begin{align}
&x_{1} = 1, x_{2} = 0 \implies X = \left( 1, 0, -1, -\frac{1}{2}, 0 \right) \\
&x_{1} = 0, x_{2} = 1 \implies X = \left( 0, 1, -2, -1, 0 \right)
\end{align}
$$
De esta manera, el espacio tiene dimensión 2, ya que está dado por dos parámetros $x_{1}, x_{2}$:
$$
\mathcal{B}_{Ker A} = \left\{ \left( 1, 0, -1, -\frac{1}{2}, 0 \right), \left( 0, 1, -2, -1, 0 \right) \right\} \implies dim(Ker A) = 2
$$

Para concluir con el ejercicio, tenemos que verificar que $rg(A) + dim(Ker A) = n$, siendo $n = 5$ (puesto que el conjunto $Ker A$ está compuesto por quíntuplas y la matriz $A$ tiene 5 columnas).

Sabemos que
$$
\begin{align}
&rg(A) = 3 \\
&dim(Ker A) = 2 \\
&n = 5
\end{align}
$$
En conclusión:
$$
rg(A) + dim(Ker A) = 3 + 2 = n = 5
$$

---
# Ejercicio 8

## Parte a)
$$
S_{1} = \{ (x, y, z) \in \mathbb{R}^{3} : x = z \} \text{ y } S_{2} = \{ (x, y, z) \in \mathbb{R}^{3} : z = 0 \}
$$
Comenzamos por los subespacios separados:

- $S_{1}$
Sabemos que el subespacio $S_{1}$ está conformado por las ternas $(x, y, z)$ que cumplen que $x = z$. Por lo tanto, sabemos que el espacio tendrá dimensión 2 (una menos que todo $\mathbb{R}^{3}$), por lo que su base estará conformada por 2 elementos:
$$
\mathcal{B}_{S_{1}} = \{ (1, 0, 1), (0, 1, 0) \}
$$

- $S_{2}$
El subespacio $S_{2}$ está conformado por las ternas $(x, y, z)$ que cumplen que $z = 0$. Por lo tanto, sabemos que el espacio tendrá dimensión 2 (al igual que $S_{1}$), por lo que su base estará conformada por 2 elementos:
$$
\mathcal{B}_{S_{2}} = \{ (1, 0, 0), (0, 1, 0) \}
$$

- $S_{1} + S_{2}$
La suma de dos subespacios conforma un nuevo subespacio que contiene todas las combinaciones lineales de los vectores de $S_{1}$ y $S_{2}$. De esta forma, podemos considerar como base de este nuevo subespacio la unión de las bases de $S_{1}$ y $S_{2}$:
$$
\mathcal{B}_{S_{1} + S_{2}} = \{ (1, 0, 0), (0, 1, 0), (1, 0, 1) \}
$$
Como vemos tiene dimensión 3, y si lo estudiamos bien, comprenderemos que también es base del espacio vectorial $\mathbb{R}^{3}$.

- $S_{1} \cap S_{2}$
La intersección de dos subespacios siempre será otro subespacio. Lo que podemos hacer para encontrar una base de dicho subconjunto es estudiar la intersección $\mathcal{B}_{S_{1}} \cap \mathcal{B}_{S_{2}}$:
$$
\mathcal{B}_{S_{1} \cap S_{2}} = \mathcal{B}_{S_{1}} \cap \mathcal{B}_{S_{2}} = \{ (0, 1, 0) \}
$$

Ahora, tenemos que deducir cuándo la suma es directa. Que la suma sea directa ($S_{1} \oplus S_{2}$) significa que el único elemento en común entre $S_{1}$ y $S_{2}$ es el vector nulo. Sin embargo, podemos ver claramente que no es así, ya que ambos comparten el vector $(0, 1, 0)$ en sus bases, y como se trata de planos (los cuales no son paralelos), ambos se interceptan en una recta, específicamente la recta
$$
\begin{cases}
x = 0 \\
z = 0
\end{cases}
$$

En conclusión, la suma entre $S_{1}$ y $S_{2}$ no es directa.

## Parte b)
$$
S_{1} = \{ p \in \mathbb{R}_{2}[x] : p(x) = ax^{2}, \text{ con } a \in \mathbb{R} \} \text{ y } S_{2} = \{ p \in \mathbb{R}_{2}[x] : p(x) = cx^{2} + bx + c, \text{ con } b, c \in \mathbb{R} \}
$$
Comenzamos por los subespacios separados:

- $S_{1}$
Sabemos que el subespacio $S_{1}$ está conformado por los polinomios de grado dos que solo tienen un término: el término de grado 2. Por lo tanto, sabemos que el espacio tendrá dimensión 1 (dos menos que todo $\mathbb{R}_{2}[x]$), por lo que su base estará conformada por 1 elemento:
$$
\mathcal{B}_{S_{1}} = \{ x^{2} \}
$$

- $S_{2}$
El subespacio $S_{2}$ está conformado por los polinomios de grado dos que, pudiendo tener los tres términos, el coeficiente de grado 2 y 0 son iguales. Por lo tanto, sabemos que el espacio tendrá dimensión 2 (uno más que $S_{1}$), por lo que su base estará conformada por 2 elementos:
$$
\mathcal{B}_{S_{2}} = \{ 1 + x^{2}, x \}
$$

- $S_{1} + S_{2}$
La suma de dos subespacios conforma un nuevo subespacio que contiene todas las combinaciones lineales de los vectores de $S_{1}$ y $S_{2}$. De esta forma, podemos considerar como base de este nuevo subespacio la unión de las bases de $S_{1}$ y $S_{2}$:
$$
\mathcal{B}_{S_{1} + S_{2}} = \{ 1 + x^{2}, x, x^{2} \}
$$
Como vemos tiene dimensión 3, y si lo estudiamos bien, comprenderemos que también es base del espacio vectorial $\mathbb{R}_{2}[x]$.

- $S_{1} \cap S_{2}$
La intersección de dos subespacios siempre será otro subespacio. Lo que podemos hacer para encontrar una base de dicho subconjunto es estudiar la intersección $\mathcal{B}_{S_{1}} \cap \mathcal{B}_{S_{2}}$:
$$
\mathcal{B}_{S_{1} \cap S_{2}} = \mathcal{B}_{S_{1}} \cap \mathcal{B}_{S_{2}} = \{ \vec{0} \}
$$

Ahora, tenemos que deducir cuándo la suma es directa. Que la suma sea directa ($S_{1} \oplus S_{2}$) significa que el único elemento en común entre $S_{1}$ y $S_{2}$ es el vector nulo. De esta manera, podemos ver que la condición se cumple, ya que la intersección entre ambos subconjuntos es el vector nulo.

En conclusión, la suma entre $S_{1}$ y $S_{2}$ es directa, y, por lo tanto, podemos denotarla como $S_{1} \oplus S_{2}$.

---
# Ejercicio 11

## Parte a)
Sabiendo que $V = S_{1} \oplus S_{2}$, significa que la suma entre $S_{1}$ y $S_{2}$ es directa, por lo que $S_{1} \cap S_{2} = \{ \vec{0} \}$. Otra afirmación que podemos establecer a partir de la definición de $V$ es que $dim(V) = dim(S_{1}) + dim(S_{2})$. Además, como $\mathcal{B}_{1}$ y $\mathcal{B}_{2}$ son bases de los subespacios anteriores, podemos afirmar que $\mathcal{B}_{1} \cap \mathcal{B}_{2} = \emptyset$.

En base a esto último, y la igualdad de las dimensiones mencionada, podemos desarrollar lo siguiente:
$$
dim(S_{1}) = \# \mathcal{B_{1}} \land dim(S_{2}) = \# \mathcal{B_{2}} \land (S_{1} \cap S_{2} = \{ \vec{0} \} \implies \mathcal{B}_{1} \cap \mathcal{B}_{2} = \emptyset) \implies dim([\mathcal{B}_{1} \cup \mathcal{B}_{2}]) = dim(S_{1}) + dim(S_{2})
$$

De esta forma, como $dim([\mathcal{B}_{1} \cup \mathcal{B}_{2}]) = dim(S_{1}) + dim(S_{2}) = dim(V)$, y sabiendo que $\mathcal{B}_{1} \cup \mathcal{B}_{2}$ es I podemos confirmar que $\mathcal{B}_{1} \cup \mathcal{B}_{2}$ es una base de $V$.

La pregunta es, ¿vale el recíproco?
Si $\mathcal{B}_{1} \cup \mathcal{B}_{2}$ es una base de $V$, entonces $V = S_{1} \oplus S_{2}$. Ya a simple vista podemos decir que el enunciado no se cumple, ya que podríamos tomar dos bases que tengan elementos en común, tal que la suma entre los subespacios de dichas bases no sea directa. Únicamente se cumpliría si estamos seguros de que la intersección entre las bases es el conjunto vacío.

## Parte b)
$$
\mathcal{B}_{1} \cap \mathcal{B}_{2} = \emptyset \implies S_{1} \cap S_{2} ?
$$
Esta implicación no se cumple, ya que para cualquier espacio existen infinitas bases. De esta manera, para dos subespacios que tienen elementos en común más allá del vector nulo, se podrían definir bases sin elementos en común. Por ejemplo:
$$
S_{1} = \{ (x, y, z) \in \mathbb{R}^{3} : x = z \} \text{ y } S_{2} = \{ (x, y, z) \in \mathbb{R}^{3} : z = 0 \}
$$
Tal que:
$$
\begin{align}
&\mathcal{B}_{S_{1}} = \{ (1, 0, 1), (0, 1, 0) \} \\
&\mathcal{B}_{S_{2}} = \{ (1, 0, 0), (0, 1, 0) \}
\end{align}
$$
Sin embargo, también podríamos considerar $\mathcal{B}_{S_{2}} = \{ (1, 0, 0), (0, 2, 0) \}$, y en este caso la implicación no se da.

## Parte c)
Este enunciado es similar (y esta basado) en el recíproco del enunciado de la parte a, agregando una condición más: no solo sabemos que $\mathcal{B}_{1} \cup \mathcal{B}_{2}$ es una base de $V$, sino también que $\mathcal{B}_{1} \cap \mathcal{B}_{2} = \emptyset$.

Sabiendo que $\mathcal{B}_{1} \cap \mathcal{B}_{2} = \emptyset$, para unas bases cualesquiera de $S_{1}$ y $S_{2}$, podemos confirmar que $S_{1} \cap S_{2} = \{ 0 \}$. Esto significa podemos denotar a la suma como $S_{1} \oplus S_{2}$ (ya que es directa). Ahora, como $\mathcal{B}_{1} \cap \mathcal{B}_{2} = \emptyset$, podemos decir que $\mathcal{B}_{1} \cup \mathcal{B}_{2}$ es LI. Además, si estudiamos la cardinalidad del conjunto, podemos ver que:
$$
\begin{align}
&\# \mathcal{B}_{1} = dim(S_{1}) \land \# \mathcal{B}_{2} = dim(S_{2}) \implies \# (\mathcal{B}_{1} \cup \mathcal{B}_{2}) = dim(S_{1}) + dim(S_{2}) \\
&[\mathcal{B}_{1}] = S_{1} \land [\mathcal{B}_{2}] = S_{2} \implies [\mathcal{B}_{1} \cup \mathcal{B}_{2}] = S_{1} \oplus S_{2}
\end{align}
$$
Sin embargo, como $\mathcal{B}_{1} \cup \mathcal{B}_{2}$ es base de $V$, estamos seguros de que $dim(V) = dim(S_{1}) + dim(S_{2})$.

Finalmente, como determinamos que la suma entre $S_{1}$ y $S_{2}$ es directa, ambos subconjuntos de $V$, y partiendo de la hipótesis que establece que $\mathcal{B}_{1} \cup \mathcal{B}_{2}$ es base de $V$, podemos decir que $dim(S_{1} \oplus S_{2}) = dim(V)$, por lo que podemos concluir que $V = S_{1} \oplus S_{2}$.

VERSIÓN RESUMIDA:
Al ser la unión $\mathcal{B}_{1} \cup \mathcal{B}_{2}$ una base de $V$, el espacio generador $[\mathcal{B}_{1} \cup \mathcal{B}_{2}]$ es todo $V$. Como este generado coincide con $S_{1} + S_{2}$, entonces $V = S_{1} + S_{2}$ (pudiéndose denotar $S_{1} \oplus S_{2}$ ya que verificamos que la suma es directa).