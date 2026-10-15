# Determinantes
Recordamos la definición de determinante

> [!Definición de determinante]
> El determinante $|A| \in \mathbb{R}$ de una matriz cuadrada $A \in M_{n \times n}$ está definido por inducción sobre $n$ (comenzando por $n = 1$):
> - $n = 1$: $|A| = a_{1,1}$ (única entrada)
> - $n \geq 2$:
> $$
> \begin{align}
> &|A| = a_{1,1} |A_{1,1}| - a_{2,1} |A_{2,1}| + a_{3,1} |A_{3,1}| - \dots + (-1)^{n+1} a_{n,1} |A_{n,1}| \\
> &= \sum_{i = 1}^{n} (-1)^{i + 1} a_{i,1} |A_{i,1}|
> \end{align}
> $$
> - $\left| \begin{array}{cc} a & b \\ c & d \end{array} \right| = ad - cd$
> - $|O_{n}| = 0$ y $|I_{n}| = 1$ para todo $n \geq 1$
> 
> Cuando una columna o una fila es todo 0, la determinante es 0, en base a la fórmula general (pues el factor $a_{i,j}$ será 0 en todos los casos).

(Definición en base a la columna 1. Hay un total de $n$ términos. La matriz adjunta $A_{i,1}$, consiste en la matriz $A$ sin la fila $i$ ni la columna).
(Por ejemplo, para calcular un determinante de una matriz de tamaño 6, hay que calcular 6 determinantes de matrices de tamaño 5. Para cada matriz de tamaño 5, hay que calcular 4 determinantes de matrices de tamaño 4, etc.).

Como vemos, para matrices grandes el cálculo es complejo.
Luego veremos que hay determinadas operaciones que nos permiten simplificar el determinante, cambiando su valor, y otras sin modificarlo.

## Complejidad del cálculo de determinante
- $n = 1$: 1 entrada
- $n = 2$: suma de 2 productos de 2 entradas
- $n = 3$: suma de 6 productos de 3 entradas

**Caso general**:
$$
\text{suma de } n! \text{ productos de } n \text{ entradas}
$$
Aclaración: una entrada es una casilla de la matriz (una celda).

Por ejemplo: para calcular el determinante de una matriz de 7 entradas ($7! = 5040$), tendría que hacer 5040 sumas de productos de 7 elementos.

---
Veremos métodos para acelerar el cálculo de determinantes, reduciendo la complejidad del cálculo.

Para empezar, es importante generalizar la fórmula.

## Desarrollo por filas y columnas
Anteriormente, hicimos un desarrollo en base a la primer columna, pero podemos elegir cualquier columna y cualquier fila para desarrollar la fórmula.

### Propiedad

> [!Fórmula generalizada del determinante]
> Dada $A \in M_{n \times n}$, con $n \geq 2$, tenemos que:
> $$
> \begin{align}
> &|A| = \sum_{i = 1}^{n} (-1)^{i + j} a_{i, j} |A_{i, j}| && \text{para todo } j \in [1..n] &&j \text{ está fijada (solo cambia el índice de fila)} \\
> &|A| = \sum_{j = 1}^{n} (-1)^{i + j} a_{i, j} |A_{i, j}| && \text{para todo } i \in [1..n] &&i \text{ está fijada (solo cambia el índice de columna)}
> \end{align}
> $$

Es fundamental considerar los signos en base a cada entrada. Los signos están dados según la fila o columna seleccionada.

Estudiaremos propiedades surgidas de la anterior

### Propiedad

> [!Determinante de la traspuesta]
> Para toda matriz $A \in M_{n \times n}$:
> $$
> |A^{t}| = |A|
> $$

Esto es así, ya que, por ejemplo, si calculamos $|A|$ en base a una columna determinada, podemos tomar como referencia la fila correspondiente en $A^{t}$ para calcular $|A^{t}|$, obteniendo el mismo resultado.

Pasaremos a otro ejemplo interesante: la matriz triangular superior.

### Ejemplo
Determinante de una matriz triangular superior.

Una matriz triangular superior es aquella que sigue la estructura:
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-04-15 - Clase 11 - Determinantes/Imágenes/1 - Matriz triangular superior.png]]

Al aplicar la formula general sobre esta matriz, veremos lo siguiente:

Sea $A$ una matriz triangular superior:
$$
|A| = \alpha_{1} \times \alpha_{2} \times \dots \times \alpha_{n}
$$
Esto se demuestra por inducción sobre $n$. El caso $n = 1$ es obvio (su única entrada es la diagonal). Por inducción suponemos que se cumple para $n - 1$, y calculamos el determinante de la matriz de tamaño $n$. Aquí nos damos cuenta de que:
$$
|A| = a{1, 1} |A_{1,1}| - a_{2,1} |A_{2,1}| + \dots + (-1)^{n + 1} a_{n,1} |A_{n,1}|
$$
Sin embargo, como el único elemento no nulo de la primer columna es $a_{1,1} = \alpha_{1}$, podemos simplificar:
$$
|A| = \alpha_{1} |A_{1,1}|
$$
Como la matriz adjunta $|A_{1,1}|$ también es triangular superior, podemos hacer lo mismo. Por hipótesis de inducción, sabemos que su determinante es el producto $\alpha_{2}$ hasta $\alpha_{n}$. En conclusión, el determinante global es:
$$
|A| = \alpha_{1} \times \alpha_{2} \times \dots \times \alpha_{n}
$$
De forma simétrica, funciona igual para una matriz triangular inferior (tomando en este caso la última columna, la columna $n$).

==De esta manera, el algoritmo a aplicar es pasar de una matriz no triangular a una matriz triangular, y desarrollar el producto de los elementos de la diagonal==.

**Caso particular (matrices diagonales)**
$$
\left|
\begin{array}{cc}
\alpha_{1} & 0 & \dots & 0 & 0 \\
0 & \alpha_{2} & 0 & \dots & 0 \\
0 & \dots & \dots & \dots & 0 \\
0 & \dots & \dots & 0 & \alpha_{n}
\end{array}
\right| = \alpha_{1} \times \alpha_{2} \times \dots \times \alpha_{n}
$$
Es una matriz triangular superior e inferior a la vez. Como vemos, se calcula de la misma manera que para la matriz triangular.

Un caso particular es la matriz identidad, donde todos los elementos de la diagonal son 1, por lo que la determinante es 1.

---
## Propiedades del determinante

> [!Importante]
> El determinante no es una función lineal:
> En general:
> $$
> |A + B| \neq |A| + |B|
> $$
> $$
> |\lambda \cdot A| \neq \lambda \cdot |A|
> $$

Si bien trabajamos con muchas operaciones lineales, el determinante no es una de ellas.

Sin embargo, veremos que es una operación lineal por filas y lineal por columnas.

---
### Propiedad 1 - Aditividad respecto a una fila

> [!Aditividad respecto a una fila]
> Para toda matriz $A \in M_{n \times n}$, para todo $i \in [1..n]$ y para toda descomposición de la fila $i$ en la forma $A_{i} = B_{i} + C_{i}$, tenemos que
> $$
> |A| = \left|
> \begin{array}{cc}
> A_{1} & \dots \\
> \dots & \dots \\
> A_{i} & \dots \\
> \dots & \dots \\
> A_{n} & \dots
> \end{array}
> \right| = \left|
> \begin{array}{cc}
> A_{1} & \dots \\
> \dots & \dots \\
> B_{i} & \dots \\
> \dots & \dots \\
> A_{n} & \dots
> \end{array}
> \right| + \left|
> \begin{array}{cc}
> A_{1} & \dots \\
> \dots & \dots \\
> C_{i} & \dots \\
> \dots & \dots \\
> A_{n} & \dots
> \end{array}
> \right|
> $$
> Si $A_{i} = B_{i} + C_{i}$

Solo cambiamos la fila $A_{i}$ por la suma de $B_{i}$ y $C_{i}$. De esta manera, si podemos descomponer una fila en dos partes, la suma de los determinantes de las matrices compuestas por dichas descomposiciones será equivalente al determinante de la matriz original. Las demás filas no deben cambiar, son idénticas.

#### Ejemplos
$$
\left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right| = \left|
\begin{array}{ccc}
0 & 1 & 2 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right| = \left|
\begin{array}{ccc}
1 & 1 & 1 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right|
$$
Hicimos una descomposición respecto a la primera fila.

También se puede hacer con el resto de filas.
$$
\left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right| = \left|
\begin{array}{ccc}
1 & 2 & 3 \\
3 & 2 & 1 \\
7 & 8 & 9
\end{array}
\right| = \left|
\begin{array}{ccc}
1 & 2 & 3 \\
1 & 2 & 5 \\
7 & 8 & 9
\end{array}
\right|
$$

==Se dice que es una función n-lineal: es lineal respecto a cada fila==.

**Propiedad - Aditividad respecto a una columna**: Se puede utilizar la misma propiedad para las columnas

---
### Propiedad 2 - Homogeneidad

> [!Homogeneidad]
> Dada una matriz $A = \begin{pmatrix} A_{1} & \dots \\ \dots & \dots \\ A_{n} & \dots \end{pmatrix}$
> Para todo índice $i \in [1..n]$, tenemos que:
> $$
> \left|
> \begin{array}{cc}
> A_{1} & \dots \\
> \dots & \dots \\
> \lambda A_{i} & \dots \\
> \dots & \dots \\
> A_{n} & \dots
> \end{array}
> \right| = \lambda |A|
> $$
> También se puede expresar como una transformación elemental:
> $$
> \alpha |A| = |T_{\alpha i}(A)|
> $$
> Incluso funciona para el caso $\alpha = 0$, donde $0 \cdot |A| = 0$ y $|T_{0 \times i}(A)| = 0$.

Siempre que multiplico una fila por $\lambda$ (sin modificar el resto de filas), multiplico todo el determinante por $\lambda$.

De esta manera, si yo multiplico todas las filas por $\lambda$, el determinante será multiplicado por $\lambda^{n}$

Podemos ver que es una función lineal por filas.

**Propiedad - Homogeneidad**: La misma propiedad vale para las columnas.

#### Ejemplos
$$
\left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right| = \frac{1}{2} \left|
\begin{array}{ccc}
2 & 4 & 6 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right|
$$
$$
\left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right| = \frac{1}{3} \left|
\begin{array}{ccc}
1 & 2 & 3 \\
12 & 15 & 18 \\
7 & 8 & 9
\end{array}
\right|
$$
$$
\left|
\begin{array}{ccc}
1 & 2 & 3 \\
12 & 15 & 18 \\
7 & 8 & 9
\end{array}
\right| = 3 \left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right|
$$
En conclusión, al multiplicar una fila o columna por un valor $x$, el determinante de la nueva matriz será $x$ veces más grande (si $B = A$, pero con$A_{i}$ = $\lambda A_{i}$, entonces $|B| = \lambda |A|$).

> [!Corolario]
> $$
> |\lambda \cdot A| = \lambda^{n} \cdot |A|
> $$
> Como vemos, depende de la dimensión de $A$.

---
### Propiedad 3 - Intercambio de filas
$$
|T_{i \longleftrightarrow j}(A)| = -|A|
$$
Si partimos de $A$ e intercambiamos dos filas $i$ y $j$, cambia el signo del determinante.

**Propiedad - Intercambio de columnas**: La misma propiedad vale para las columnas.
#### Ejemplos
$$
\left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right| = - \left|
\begin{array}{ccc}
7 & 8 & 9 \\
4 & 5 & 6 \\
1 & 2 & 3
\end{array}
\right|
$$
De esta manera, sabemos que si hacemos un intercambio par de filas y/o columnas, no afectaremos el determinante:
$$
\left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right| = - \left|
\begin{array}{ccc}
7 & 8 & 9 \\
4 & 5 & 6 \\
1 & 2 & 3
\end{array}
\right| = \left|
\begin{array}{ccc}
4 & 5 & 6 \\
7 & 8 & 9 \\
1 & 2 & 3
\end{array}
\right|
$$
$$
\implies \left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right| = \left|
\begin{array}{ccc}
4 & 5 & 6 \\
7 & 8 & 9 \\
1 & 2 & 3
\end{array}
\right|
$$
A veces, es necesario intercambiar filas y columnas para lograr una buena forma de la matriz (buscando facilitar el cálculo del determinante).

---
Hasta aquí vimos las tres propiedades fundamentales de las matrices, siendo:
1. Suma de filas.
2. Multiplicar una fila por $\alpha$.
3. Intercambiar dos filas.

Ahora veremos una propiedad extra que sigue los anteriores:
### Propiedad 4 - Corolario

> [!Corolario]
> $$
> |T_{i + \alpha j}(A)| = |A|
> $$
> De esta manera, sumarle a una fila un múltiplo de otra no afecta al valor del determinante.

**Propiedad - Corolario**: La misma propiedad vale para las columnas.

A continuación expresamos por qué:
$$
\left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
A_{i} + \alpha A_{j} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| = \underbrace{ \left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
A_{i} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| + \left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
\alpha A_{j} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| }_{ \text{Aplicamos propiedad 1} } = \underbrace{ \left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
A_{i} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| + \alpha \left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
A_{j} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| }_{ \text{Aplicamos propiedad 2} }
$$
Lo particular de la matriz $$ \left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
A_{j} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| $$ 
es que tiene dos filas idénticas ($i$ y $j$, $A_{j}$ está dos veces). Cuando una matriz tiene dos filas idénticas, podemos intercambiar dichas filas y la matriz no cambia, pero su determinante será el opuesto. De esta forma, una matriz con dos filas idénticas es el opuesto de ella misma. El único número que es su propio opuesto es 0.

De esta forma, el determinante de una matriz que tiene dos filas o dos columnas idénticas es 0, ya que es invariante por intercambio, por lo que es invariante por intercambio de signo.

Es así que simplemente nos quedamos con:
$$
\begin{align}
\left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
A_{i} + \alpha A_{j} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| &= \left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
A_{i} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| + \cancel{ \alpha \left|
\begin{array}{cc}
A_{1} & \dots \\
\dots & \dots \\
A_{j} & \dots \\
\dots & \dots \\
A_{n} & \dots
\end{array}
\right| } \\
&=|A|
\end{align}
$$

Esto no significa que las matrices sean invariantes por las transformaciones elementales, simplemente depende de la transformación elemental:

1. Si se trata de multiplicar una fila por $\alpha$, el determinante se multiplica por $\alpha$
2. Si se trata de intercambiar dos filas, el determinante cambia de signo.
3. Si se trata de sumarle un múltiplo de una fila a otra, el determinante no cambia.

Por esta razón, es fundamental llevar un registro de como el determinante se ve afectado en base a las operaciones realizadas mientras simplificamos la matriz.

---
A continuación veremos algunos ejemplos (trabajando con matrices más grandes):

#### Ejemplo
$$
\left|
\begin{array}{cccccc}
1 & 1 & 1 & 1 & 1 & 1 \\
1 & -1 & 1 & -1 & 1 & -1 \\
1 & 1 & -1 & -1 & 1 & 1 \\
1 & 1 & 1 & -1 & -1 & -1 \\
1 & 1 & 1 & 1 & 2 & 2 \\
1 & 1 & 1 & 1 & 1 & 2
\end{array}
\right|
$$
Si desarrollamos la formula usual, tenemos una suma de 120 sumandos, cada uno con un producto de 6 entradas, siendo completamente inviable calcularlo de forma general. Como vemos, debajo de la diagonal solo tenemos 1, por lo que haremos combinaciones para deshacernos de los mismos y llegar a una matriz triangular superior:
$$
\left|
\begin{array}{cccccc}
1 & 1 & 1 & 1 & 1 & 1 \\
0 & -2 & 0 & -2 & 0 & -2 \\
0 & 0 & -2 & -2 & 0 & 0 \\
0 & 0 & 0 & -2 & -2 & -2 \\
0 & 0 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 0 & 1
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} - F_{1} \\
&F_{4} \leftarrow F_{4} - F_{1} \\
&F_{5} \leftarrow F_{5} - F_{1} \\
&F_{6} \leftarrow F_{6} - F_{1}
\end{align}
$$
Al aplicar la transformación elemental $T_{i + \alpha j}(A)$, no modificamos el valor del determinante.

Ahora, al tener una matriz triangular superior, podemos calcular fácilmente su determinante:
$$
\left|
\begin{array}{cccccc}
1 & 1 & 1 & 1 & 1 & 1 \\
0 & -2 & 0 & -2 & 0 & -2 \\
0 & 0 & -2 & -2 & 0 & 0 \\
0 & 0 & 0 & -2 & -2 & -2 \\
0 & 0 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 0 & 1
\end{array}
\right| = 1 \times (-2) \times (-2) \times (-2) \times 1 \times 1 = -8
$$
Si hubiéramos realizado alguna operación que modificara el valor del determinante, tendríamos que haber llevado registro del mismo para aplicarlo al final.

---
Continuaremos viendo otras propiedades de los determinantes.

Ahora, estudiaremos los casos en los que, sin operar, se puede determinar que un determinante es nulo.

## Determinantes nulos

> [!Determinantes nulos]
> Sea $A$ una matriz cuadrada.
> Cuando una de las siguientes propiedades se cumple, tenemos que $|A| = 0$:
> 1. $A$ tiene una fila (o columna) nula.
> (Si se desarrolla la formula general en base a dicha fila, obtendremos una suma de términos nulos.)
> 
> 2. $A$ tiene dos filas (o dos columnas) iguales.
> (Al intercambiar las filas, la matriz es la misma, pero se invierte el valor de su determinante, por lo que 0 es el único valor con estas características.)
> 
> 3. $A$ tiene dos filas (o dos columnas) proporcionales.
> (Ídem que el punto 2).
> 
> 4. $A$ tiene una fila (o una columna) que es combinación lineal de las filas (columnas) restantes.
> (Combinar linealmente filas es sumar varios múltiplos de filas. Cada vez que una fila es combinación lineal de otras, el determinante es nulo, ya que operando se puede llegar a anular la fila.)
> Esta es la condición más general.

#### Ejemplo
$$
\left|
\begin{array}{ccc}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}
\right|
$$
$$
2 \begin{pmatrix}
4 & 5 & 6
\end{pmatrix} - \begin{pmatrix}
1 & 2 & 3
\end{pmatrix} = \begin{pmatrix}
7 & 8 & 9
\end{pmatrix} \implies F_{3} = 2F_{2} - F_{1}
$$
De esta forma, sabemos que la matriz es nula.
También se puede hacer con columnas:
$$
\begin{pmatrix}
3 \\
6 \\
9
\end{pmatrix} = 2\begin{pmatrix}
2 \\
5 \\
8
\end{pmatrix} - \begin{pmatrix}
1 \\
4 \\
7
\end{pmatrix}
$$
ACLARACIÓN: Puede darse que una matriz tenga una fila igual a una columna, pero eso no cuenta. Solo son las filas entre si, o las columnas entre si. Si se pudiera, la identidad tendría determinante nulo, y sabemos que no es así.

---
## Determinante de un producto

> [!Recordatorio]
> En general:
> $$
> |A + B| \neq |A| + |B|
> $$
> $$
> |\lambda \cdot A| = \lambda^{n} \cdot |A| \qquad (\neq \lambda \cdot |A|)
> $$

La linealidad solo funciona fila por fila, o bien columna por columna.

A continuación, veremos como se comporta el determinante con el producto de matrices:

### Teorema (Binet-Cauchy)
Para todas matrices $A, B \in M_{n \times n}$:
$$
|AB| = |A| \times |B|
$$

A partir de esto, deduciremos que una matriz es invertible si y solo si su determinante no es nulo.

De esta forma, ==el determinante de una matriz es la medida del carácter invertible de la matriz==.

La idea de la prueba es comenzar demostrándola con matrices elementales (con las cuales podemos calcular los determinantes fácilmente), y luego, pasando por matrices más amplias, complejas, lograremos llegar hasta la fórmula de producto.