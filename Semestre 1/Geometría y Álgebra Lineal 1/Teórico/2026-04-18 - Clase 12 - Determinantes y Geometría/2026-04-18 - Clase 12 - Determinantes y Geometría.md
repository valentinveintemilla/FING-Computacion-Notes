En esta instancia, terminaremos el capitulo de determinantes y comenzaremos con geometría.

# Determinante de un producto
Durante la clase pasada, vimos una serie de propiedades del determinante y operaciones que podemos realizar sobre una matriz para facilitar el cálculo de dicho valor, algunas afectando el determinante y otras no.

> [!Recordatorio]
> En general:
> $$
> |A + B| \neq |A| + |B| \qquad \text{salvo si } n = 1
> $$
> $$
> |\lambda \cdot A| = \lambda^{n} \cdot |A|
> $$

---
Ahora, queremos relacionar el determinante con el producto de matrices, demostrando el siguiente teorema:

# Teorema (Binet-Cauchy) - Teorema del producto

> [!Teorema (Binet-Cauchy) - Teorema del producto]
> $$
> \forall A, B \in M_{n \times n}, \qquad |AB| = |A| \cdot |B|
> $$

Esta demostración no es sencilla, tomando en cuenta la definición del determinante (por inducción sobre n), y que el producto no tiene una definición trivial.

Por esta razón, lo demostraremos paso a paso, cada vez utilizando hipótesis más generales, así como 4 lemas que veremos a continuación:

---
## Lema 1

> [!Lema 1]
> Si $A$ es una matriz elemental, entonces
> $$
> |AB| = |A| \cdot |B| \qquad ( \text{para toda } B \in M_{n \times n} )
> $$

Enuncia lo mismo que el teorema, pero solo en el caso donde $A$ es una matriz elemental.

### Demostración

3 casos (tipos de matriz elemental):
1. $A = E_{i \longleftrightarrow j} = T_{i \longleftrightarrow j}(I_{n})$. Tenemos que:
$$
|A| = -|I_{n}| = -1
$$
$$
AB = E_{i \longleftrightarrow j}B = T_{i \longleftrightarrow j}(B)
$$
Tenemos que:
$$
|AB| = -|B|
$$
Luego:
$$
|AB| = (-1)|B| = |A| \cdot |B|
$$

2. $A = E_{\alpha i} = T_{\alpha i}(I_{n}) \qquad (\alpha \neq 0)$. Entonces:
$$
|A| = \alpha|I_{n}| = \alpha
$$
$$
AB = E_{\alpha i}B = T_{\alpha i}(B)
$$
$$
|AB| = \alpha |B|
$$
Luego:
$$
|AB| = \alpha |B| = \underbrace{ |A| }_{ \alpha } \cdot |B|
$$

3. $A = E_{i + \alpha j} = T_{i + \alpha j}(I_{n})$. Entonces
$$
|A| = |I_{n}| = 1
$$
$$
AB = E_{i + \alpha j}B = T_{i + \alpha j}(B)
$$
$$
|AB| = |B|
$$
Luego:
$$
|AB| = 1|B| = \underbrace{ |A| }_{ 1 } \cdot |B|
$$

En los tres casos, logramos demostrar que
$$
|AB| = |A| \cdot |B|
$$
siempre que $A$ sea una matriz elemental.

---
Ahora, extenderemos el resultado a todas las matrices invertibles:

## Lema 2

> [!Lema 2]
> Si $A$ es invertible, entonces
> $$
> |AB| = |A| \cdot |B| \qquad ( \text{para toda } B \in M_{n \times n} )
> $$

Ahora, analizamos el caso en el que $A$ es una matriz invertible.

### Demostración
Utilizaremos la descomposición de matrices invertibles como producto de matrices elementales. De esta forma, podremos usar el lema 1.

Como $A$ es invertible, existen matrices elementales $E_{1}, E_{2}, \dots, E_{k}$ tales que $A = E_{1}, E_{2}, \dots, E_{k}$.
Tenemos que:
$$
\begin{align}
|A| &= |E_{1} E_{2} \dots E_{k}| \\
&= |E_{1}| \times |E_{2} \dots E_{k}| \qquad \text{(lema 1)} \\
= \dots &= |E_{1}| \times |E_{2}| \times \dots \times |E_{k}|
\end{align}
$$
(Consideramos $E_{1}$ como matriz $A$ y $E_{2} \dots E_{k}$ como matriz $B$.)
(El proceso se puede volver a repetir considerando a $E_{2}$ como matriz $A$ y $E_{3} \dots E_{k}$ como matriz $B$, llegando a descomponer todo al final en el producto de los determinantes de $E_{1}, E_{2}, \dots E_{k}$, aplicando el lema 1 un total de $k - 1$ veces.)

Además, tenemos que:
$$
\begin{align}
|AB| &= |E_{1} E_{2} \dots E_{k} B| \\
&= |E_{1}| \times |E_{2} \dots E_{k} B| \\
= \dots &= \underbrace{ |E_{1}| \times |E_{2}| \times \dots \times |E_{k}| }_{ |A| } \times |B| \\
&= |A| \times |B|
\end{align}
$$
(Ahora, siguiendo la misma lógica, aplicamos el lema 1 $k$ veces para descomponer $|E_{1} E_{2} \dots E_{k} B|$).

Al comienzo, sabíamos que $|AB| = |A| \cdot |B|$ se cumplía para las matrices elementales. Ahora, por inducción, sabemos que se cumple para todos los productos finitos de matrices elementales, que equivale a las matrices invertibles.

---
Ahora, estudiaremos que pasa con las matrices no invertibles:

## Lema 3

> [!Lema 3]
> Si $A$ no es invertible, entonces
> $$
> |A| = 0
> $$

De esta forma, podremos establecer que:
- Cuando $A$ es invertible, su determinante es un producto de matrices elementales, y nunca será 0, por la forma y propiedades de dichas matrices (no hay filas ni columnas nulas, por ejemplo).
- Cuando $A$ no es invertible, su determinante es nulo.

### Demostración

Sea $A'$ una forma escalerizada de $A$ y sean $E_{1}, E_{2}, \dots, E_{k}$ matrices elementales tales que
$$
A' = E_{k} \dots E_{2} E_{1} A
$$
(Es el resumen del proceso de escalerización. Parto de $A$, aplico determinadas transformaciones elementales en el orden adecuado, y obtengo la forma escalerizada $A'$.)

También tenemos que
$$
A = (E_{k} \dots E_{2} E_{1})^{-1} A'
$$
(Ambas afirmaciones son equivalentes, ya que $E_{k} \dots E_{2} E_{1}$ es invertible.)

Como $A'$ tiene $< n$ escalones:
$$
|A'| = 0
$$
Luego (aplicando los lemas anteriores):
$$
|A| = |(\underbrace{ E_{k} \dots E_{2} E_{1} }_{ \text{Matriz invertible} })^{-1}| \cdot |A'| = 0
$$

==Ahora sabemos que las matrices no invertibles tienen rango nulo==. Es decir, las matrices escalerizadas cuadradas, que no tienen rango $n$, necesariamente tienen la última fila nula.

---
Nos queda el último tema, el cual enuncia que si una matriz es no invertible, entonces cualquier producto de esa matriz por otra matriz tampoco es invertible.

## Lema 4

> [!Lema 4]
> Si $A$ no es invertible, entonces $AB$ tampoco es invertible (para toda $B \in M_{n \times n}$).

### Demostración
Por el absurdo, supongamos que $AB$ es invertible.
Sea $A' := B(AB)^{-1}$

(Podemos construir esta matriz, ya que $AB$ es invertible, y la podemos multiplicar por $B$, además todas tienen el tamaño correcto.)

Se observa que
$$
AA' = A(B(AB)^{-1}) = (AB)(AB)^{-1} = I
$$
Luego: $A'$ es la inversa de $A$, y $A$ es invertible: CONTRADICCIÓN

En la hipótesis, supuse que $A$ no es invertible, así como la negación de la conclusión ($AB$ es invertible).
Del mismo modo, demostramos que si $AB$ es invertible, entonces $A$ es invertible.
Esto también determina que $B$ es invertible, haciendo lo siguiente:
$$
AB = (AB)^{t} = B^{t} \cdot A^{t}
$$
Si $B^{t}$ es invertible, entonces $B$ también lo es.

---
Ahora podemos demostrar el teorema en el caso general:

## Demostración del teorema de Binet-Cauchy (teorema del producto)

Sean $A, B \in M_{n \times n}$ cualesquiera.
Se distinguen 2 casos:

1. $A$ es invertible
$$
|AB| = |A| \cdot |B| \qquad \text{(lema 2)}
$$

2. $A$ no es invertible
Entonces:
$$
|A| = 0 \qquad \text{(lema 3)}
$$
AB no es invertible (lema 4).
Luego $|AB|$ (lema 3).
Por lo tanto:
$$
|AB| = 0 = 0 \cdot |B| = |A| \cdot |B|
$$

Como vemos, el teorema funciona para todas las matrices cuadradas, con la particularidad de que en el caso de las matrices no invertibles, el resultado siempre es 0.

La formula enunciada puede utilizarse para facilitar el calculo de determinantes: en lugar de calcular un determinante complicado, es posible descomponerlo en sus factores.

---
Por último, veremos el vinculo entre matriz determinante y matriz inversa.

## Determinante y matriz inversa

> [!Teorema]
> Para toda matriz $A \in M_{n \times n}$, tenemos que $A$ es invertible si y solo si $|A| \neq 0$.
> Además $|A^{-1}| = \frac{1}{|A|}$.

Veremos que la demostración es trivial.

### Demostración
Si $A$ es invertible:
$$
|A| = \underbrace{ |E_{1}| }_{ \neq 0 } \times \dots \times \underbrace{ |E_{k}| }_{ \neq 0 } \neq 0
$$
Si $A$ no es invertible:
$$
|A| = 0 \qquad \text{(por el lema 3)}
$$

Además, cuando $A$ es invertible, tenemos que
$$
|A| \cdot |A^{-1}| = |AA^{-1}| = |I_{n}| = 1
$$
Luego:
$$
|A^{-1}| = \frac{1}{|A|}
$$

---
Ahora, estudiaremos la noción de cofactores: una forma de calcular la inversa mediante determinantes. Sin embargo no la demostraremos porque nunca la usaremos en la práctica.

## Cofactores

> [!Cofactores]
> Dada una matriz $A \in M_{n \times n}$ se llama cofactor de $A$ en la posición $(i, j)$ el número
> $$
> c_{i, j} := (-1)^{i + j} \cdot |A_{i, j}|
> $$
> Los números ($c_{i,j}$, con $1 \leq i \leq n$ y $1 \leq j \leq n$) forman una matriz, escrita
> $$
> cof(A) \qquad \ll \text{matriz de los cofactores} \gg
> $$

(Es un calculo bastante complejo. Consiste en calcular los determinantes de todas las matrices adjuntas de $A$, considerando el signo que lo multiplica, y con eso formar una matriz. Para calcular la matriz de los cofactores, tengo que calcular $n^{2}$ determinantes de tamaño $n - 1$.)

### Teorema

> [!Teorema]
> Para toda matriz cuadrada $A \in M_{n \times n}$:
> $$
> A \cdot cof(A)^{t} = |A| \cdot I_{n}
> $$
> En particular, cuando $A$ es invertible ($|A| \neq 0$), tenemos que:
> $$
> A^{-1} = \frac{1}{|A|} \cdot cof(A)^{t}
> $$

No demostraremos este teorema.

En la práctica, no es una fórmula factible, pero es interesante a nivel teórico, y quizás pueda ser útil para análisis puntuales. Por ejemplo, nos brinda una fórmula explícita para calcular la inversa, pero se necesitan muchas más operaciones que utilizando el algoritmo tradicional de escalerización.

En conclusión, los determinantes son una noción interesante para estimar el factor invertible de una matriz, tratándose de un número que, en la práctica no se suele usar, salvo en determinadas excepciones. 

Con esto finalizamos el capítulo de determinantes.

---
Comenzamos con el capítulo de geometría.

# Rectas y planos en el espacio
## El espacio $R^{n}$ de las n-uplas

> [!Definición]
> Dado $n \geq 1$, se llama n-upla de reales a toda sucesión finita ($x_{1}, \dots, x_{n}$) donde $x_{1}, \dots, x_{n} \in \mathbb{R}$.
> 
> Se escribe $R^{n}$ el conjunto de las n-uplas de reales.

==Una n-upla es una generalización de la noción de par==:
1. Una 1-upla es un número real.
2. Una 2-upla es un par de reales.
3. Una 3-upla es un terna de reales.
4. Una 4-upla es una cuádrupla de reales.
Y así sucesivamente.

$R^{n}$: Producto cartesiano de $\mathbb{R} \times \mathbb{R} \times \mathbb{R} \times \dots \times \mathbb{R}$, $n$ veces.

El espacio $\mathbb{R}^{n}$ tiene la misma estructura que el espacio de las matrices columna ($: 1 \times n$) o de las matrices filas ($: n \times 1$).

Es así que cuando tengamos una matriz y no sepamos si es una fila o una columna, la trataremos como una n-upla

De esta forma, utilizaremos la misma noción de suma y de producto por un número.

## Operaciones

> [!Operaciones con n-uplas]
> Como para las matrices, se pueden definir:
> - la suma:
> $$
> \begin{align}
> &(x_{1}, \dots, x_{n}) + (y_{1}, \dots, y_{n}) \\
> &= (x_{1} + y_{1}, \dots, x_{n} + y_{n})
> \end{align}
> $$
> - la n-upla nula:
> $$
> \vec{0} = (\underbrace{ 0, \dots, 0 }_{ n \text{ veces} })
> $$
> - la opuesta:
> $$
> -(x_{1}, \dots, x_{n}) = (-x_{1}, \dots, -x_{n})
> $$
> - el producto de un número por una n-upla:
> $$
> \lambda \cdot (x_{1}, \dots, x_{n}) = (\lambda x_{1}, \dots, \lambda x_{n})
> $$

A continuación, veremos propiedades de las n-uplas:

## Propiedades
Para todos $u, v, w \in \mathbb{R}^{n}$
$$
\begin{align}
&(u + v) + w = u + (v + w) \\
&u + v = v + u \\
&u + \vec{0} = \vec{0} + u \\
&u + (-u) = (-u) + u = \vec{0} \\
&0 \cdot u = \vec{0} \\
&1 \cdot u = u \\
&(-1) \cdot u = -u \\
&(\lambda \mu) \cdot u = \lambda \cdot (\mu \cdot u) \\
&(\lambda + \mu) \cdot u = \lambda \cdot u + \mu \cdot u \\
&\lambda \cdot (u + v) = \lambda \cdot u + \lambda \cdot v
\end{align}
$$

Es importante recordar estas propiedades, ya que se dice que ==$R^{n}$ es un espacio vectorial==, el cual tiene $n$ dimensiones.

Cada vez que algo es ==elemento de un espacio vectorial, se puede denominar como vector==.

Para trabajar con conceptos manejables, trabajaremos con objetos de:
- Dimensión 0 (puntos)
- Dimensión 1 (rectas)
- Dimensión 2 (planos)
- Dimensión 3 (volúmenes).

Es posible trabajar con dimensiones mayores, hipervolúmenes, hiper-hipervolúmenes, etc., al menos ver como la geometría de Euclides se comporta en dichos espacios. No sabemos como representar dichas figuras, pero si podemos extender el razonamiento matemático.

---
## El espacio $R^{3}$
Lo podemos comparar con el espacio físico. Sin embargo, este no está bien definido matemáticamente hablando, ya que no se comporta de forma ideal.

Por esta razón, nosotros trabajaremos en un espacio ideal, una idealización (aproximación) del espacio físico.

Este espacio tiene tres dimensiones, lo que significa que para identificar un punto necesitamos tres coordenadas. De esta forma, a trabes de cualquier sistema de coordenadas, podemos transformar cualquier punto en una terna, las cuales tienen propiedades claras y definidas.

En la antigüedad, se axiomaba la geometría a partir de la noción de punto, vector, recta, etc. Era una época en la que los objetos geométricos estaban mejor definidos que la noción de número. Sin embargo, en el siglo $XIX$, desarrollamos una definición mucho mejor de los números, superior a la de los objetos geométricos, por lo que cambiamos el enfoque (el punto de vista algebraico). Usamos los números para reconstruir los objetos geométricos.

> [!Espacio ambiente]
> A través de un sistema fijado de coordenadas se identifica el $\ll \text{espacio ambiente} \gg$ con $R^{3}$
> $$
> E = R^{3}
> $$

#### Observación

> [!Observación]
> Cada 3-upla puede representar
> - o bien un punto $A \in \mathbb{R}^{3}$
> - o bien un vector $u \in \mathbb{R}^{3}$

De esta forma, los puntos y los vectores se representan de la misma forma, una n-upla.

Además, las operaciones sobre $R^{3}$ corresponden a las operaciones $\ll \text{geométricas} \gg$ sobre los puntos y los vectores:
- $u + v$ (suma de 2 vectores)
- $\vec{0} = (0, 0, 0)$
- $-\vec{u} = (-u_{1}, -u_{2}, -u_{3})$ (vector opuesto geométrico y vector opuesto como terna)
- $\lambda \cdot \vec{u} = (\lambda u_{1}, \lambda u_{2}, \lambda u_{3})$
- $A + u$ (traslación de $A$ según un vector $u$, como resultado da un punto)
- $B - A = \vec{AB}$ (construcción de un vector a partir de dos puntos)

Como vemos, las operaciones de suma de 2 vectores, y suma de un punto y un vector son idénticas (matemáticamente hablando), aunque tienen resultados conceptuales diferentes:
- Suma de 2 vectores: mediante el método del paralelogramo, se construye un nuevo vector.
- Suma de un punto y un vector: se obtiene un nuevo punto al final del vector sumando.

Sobre la resta de dos puntos, es el equivalente conceptual al vector que une a los puntos correspondientes.