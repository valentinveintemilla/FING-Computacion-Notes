Continuamos con matrices elementales.
# Matrices elementales
Vienen de la siguiente proposición:

> [!Proposición]
> Dados enteros $m, n \geq 1$
> 1. Para cata transformación elemental $T$ sobre las matrices de tamaño $m \times n$, existe una matriz cuadrada $E \in M_{m \times m}$ tal que
> $$
> T(A) = EA \qquad \text{para toda} A \in M_{m \times n}
> $$
> 2. La <u>matriz elemental</u> asociada a la transformación elemental $T$ se obtiene por:
> $$
> E = T(I_{m})
> $$

(Las operaciones con matrices elementales se pueden aplicar sobre cualquier matriz, sin importar el tamaño. Sin embargo, para poder realizar una operación entre una matriz $m \times n$ y una matriz elemental, la matriz elemental tiene que ser de tamaño $m \times m$, cuadrada considerando la cantidad de filas de la matriz correspondiente.)

(El aplicar una transformación elemental sobre una matriz A, equivale a multiplicar la matriz a por cierta matriz elemental -que hace el mismo trabajo- por la izquierda.)

Ya vimos que en este curso, todo funciona gracias al teorema de Rouché-Frobenius, el cual consiste en aplicar transformaciones elemental en un orden determinado sobre una matriz ampliada. Por esta razón, al fundamentarse en el uso de transformaciones elementales, podemos reducir dichos problemas al estudio de matrices elementales.

## Los tres tipos de matrices elementales

1. $T_{\alpha i}$: multiplicar la fila $i$ por $\alpha \neq 0$.
$$
E_{\alpha i} := T_{\alpha i}(I_{m}) = \begin{pmatrix}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\dots & 0 & \alpha & 0 \\
\dots & \dots & \dots & \dots \\
0 & 0 & \dots & 1
\end{pmatrix}
\text{Fila } i
$$
Es igual a la matriz identidad, excepto en la fila $i$, la cual tiene valor $\alpha$ en lugar de 1 en la celda $a_{i,i}$.
Cuando multiplico esta matriz por cualquier matriz de un tamaño correspondiente, es equivalente a aplicar la transformación elemental correspondiente.

2. $T_{i \longleftrightarrow j}$: intercambiar las filas $i$ y $j$.
$$
E_{i \longleftrightarrow j} := T_{i \longleftrightarrow j}(I_{m}) = \begin{pmatrix}
1 & 0 & \dots & \dots & 0 \\
\dots & 0 & \dots & 1 & \dots \\
\dots & \dots & \dots & \dots & \dots \\
\dots & 1 & \dots & 0 & \dots \\
0 & 0 & \dots & \dots & 1
\end{pmatrix}
\begin{align}
&\text{Fila } i \\ \\

&\text{Fila } j
\end{align}
$$
Es igual a la matriz identidad, excepto en las filas $i$ y $j$, las cuales están intercambiadas ($a_{i,i} = a_{j,j} = 0$ y $a_{i,j} = a_{j,i} = 1$, todo el resto 0). La diagonal tiene 1 en todas las celdas menos en las filas $i$ y $j$.

> [!Aclaración]
> En todas las operaciones consideramos las filas, no las columnas. Siempre son las filas que cuentan. En realidad existe una noción de matriz elemental por la derecha, donde todo gira en torno a las columnas en lugar de las filas, pero no serán abordadas en el curso.

3. $T_{i + \alpha j}$: sumarle a la fila $i$ la fila $j \times \alpha$.
$$
E_{i + \alpha j} := T_{i + \alpha j}(I_{m}) = \begin{pmatrix}
1 & 0 & \dots & \dots & 0 \\
\dots & 1 & \dots & \alpha & \dots \\
\dots & \dots & \dots & \dots & \dots \\
\dots & \dots & \dots & 1 & \dots \\
0 & 0 & \dots & \dots & 1
\end{pmatrix}
\begin{align}
&\text{Fila } i \\ \\

&\text{Fila } j
\end{align}
$$
Aquí, todas las filas quedan intactas, menos la fila $i$, cuya celda $a_{i,j}$ tiene valor $\alpha$. De esta forma, la matriz no es simétrica.

Todas estas matrices se obtienen al aplicar las transformaciones correspondientes a la matriz identidad.

> [!Observación]
> Una transformación elemental es una forma particular de función $T : M_{m \times n} \to M_{m \times n}$
> Estas unciones son de la forma:
> $$
> T(A) = EA
> $$
> donde $E$ es la matriz elemental correspondiente.

Es así que la proposición anterior establece que todas estas funciones particulares pueden representarse mediante matrices elementales

---
A continuación, veremos como las trasformaciones elementales no son algo disjunto de las matrices, sino que son matrices en sí, empezando por diferentes propiedades de las mismas.

## Propiedad
==Toda matriz elemental es invertible==. Esto es posible, gracias a la idea de que toda matriz elemental se corresponde con una transformación elemental, y las mismas se pueden revertir.

En particular:
1. $(E_{\alpha i})^{-1} = E_{\alpha^{-1} i}$
2. $(E_{i \longleftrightarrow j})^{-1} = E_{i \longleftrightarrow j}$ (es su propia inversa)
Aquí tenemos muchas matrices que son sus propias inversas, en particular todas las matrices $E_{i \longleftrightarrow j}$. No es el caso en los números reales, pues ahí solo tenemos dos números que son iguales a su inverso, 1 y -1.

3. $(E_{i + \alpha j})^{-1} = E_{i - \alpha j}$

==La inversa de cada matriz elemental es una matriz elemental==.

No la demostraremos porque es completamente trivial.

---
A continuación, analizaremos el método de escalerización de Rouché-Frobenius.

## Proposición
> [!Proposición]
> Sea $A$ una matriz de tamaño $m \times n$ y $A'$ una forma escalerizada de $A$. Entonces existe una sucesión finita $E_{1}, E_{2}, \dots, E^{k}$ de matrices elementales, tal que
> $$
> A' = E_{k}\dots E_{2}E_{1}A
> $$

Como vemos, escribimos la sucesión al revés. Podemos decir que es una propiedad obvia, ya que para pasar de una matriz a su forma escalerizada, aplicamos una lista finita de transformaciones elementales. Como ahora sabemos que aplicar una transformación elemental es lo mismo que multiplicar por la matriz elemental correspondiente, entonces, para pasar de $A$ a $A'$, aplicamos $k$ transformaciones elementales, que es lo mismo que desarrollar el producto por las $k$ matrices elementales en el orden correspondiente (primero $E_{1}$, luego $E_{2}$, así hasta $E_{k}$.).

En forma gráfica:
$$
A = A_{0} \overbrace{ \longrightarrow }^{ T_{1} } \underbrace{ A_{1} }_{ = E_{1}A } \overbrace{ \longrightarrow }^{ T_{2} } \underbrace{ A_{2} }_{ = E_{2}A_{1} = E_{2}E_{1}A } \dots A_{k-1} \overbrace{ \longrightarrow }^{ T_{k} } A_{k} = A' = E_{k}A_{k-1} = E_{k} \dots E_{2}E_{1}A
$$
==Es así que, para pasar de una matriz a su forma escalerizada, tengo que aplicar una serie de transformaciones elementales, que corresponden a hacer productos con una cantidad finita de matrices elementales==.

---
Seguidamente, veremos un corolario interesante, que establece que toda matriz invertible es un producto finito de matrices elementales. Dicho de otra forma, el producto de una cantidad finita de matrices elementales, da como resultado una matriz invertible. Esto aplica para todas las matrices invertibles.

## Corolario

> [!Corolario]
> Una matriz cuadrada $A \in M_{n \times n}$ es invertible si y sólo si es producto finito de matrices elementales:
> $$
> \Longleftrightarrow A = E_{1}E_{2} \dots E_{k} \qquad \text{para algunas } E_{1}, E_{2}, \dots, E_{k} \text{ matrices elementales}
> $$
> (Descomposición no única)

Este resultado nos recuerda a la descomposición de enteros en números primos. Si bien no son equivalentes, podemos decir que las matrices elementales cumplen el rol de "matrices primas".
La diferencia aquí es que la descomposición no es única, mientras que en los números primos la descomposición siempre es única.

### Demostración
Comenzamos por el recíproco.
$(\impliedby)$ Si $A = E_{1}E_{2} \dots E_{k}$, $A$ es invertible, pues todas las matrices $E_{i}$ lo son (trivial).

Ahora nos interesa ver que cada matriz invertible se puede descomponer como un producto de matrices elementales. Esto parte del problema de demostrar que existe una cantidad finita de matrices elementales que descomponen una matriz invertible, y lo resolveremos con Rouché-Frobenius.

$(\implies)$ Si $A$ es invertible, entonces se puede escalerizar hasta $I_{n}$. Por la proposición anterior, existen matrices elementales $E_{1}, E_{2}, \dots, E_{k}$ tales que:
$$
I = E_{k}\dots E_{2}E_{1}A
$$
Luego:
$$
A^{-1} = E_{k}\dots E_{2}E_{1} \qquad \text{(por unicidad de la inversa)}
$$
Por lo tanto
$$
\begin{align}
A = (A^{-1})^{-1} &= (E_{k} \dots E_{2}E_{1})^{-1} \\
&= \underbrace{ E_{1}^{-1}E_{2}^{-1} \dots E_{k}^{-1} }_{ \text{producto finito de matrices elementales} }
\end{align}
$$
De esta forma, logré descomponer A como producto finito de matrices elementales. Recordemos que $E_{1}, E_{2}, \dots, E_{k}$ son matrices elementales, entonces $E_{1}^{-1}, E_{2}^{-1}, \dots, E_{k}^{-1}$ también lo son, de tal forma que A es producto finito de matrices elementales.

Entonces, ==una matriz es invertible si y sólo si se puede descomponer en forma de producto de matrices elementales==, y dicha descomposición fue realizada mediante Rouché-Frobenius.

Este es un teorema fundamental que vincula las matrices invertibles y las matrices elementales, de tal forma que las matrices elementales son matrices invertibles "atómicas".

---
Para terminar con la inversión de matrices, veremos otra forma del algoritmo de inversión:

En la práctica, partimos de una matriz doble, teniendo a la izquierda la matriz que queremos invertir, y a la derecha la identidad correspondiente:
$$
\begin{align}
\left(
\begin{array}{c|c}
A & I
\end{array}
\right) = &\left(
\begin{array}{c|c}
A_{0} & B_{0}
\end{array}
\right) \\ \\

&\downarrow T_{1} \\ \\

&\left(
\begin{array}{c|c}
A_{1} & B_{1}
\end{array}
\right) \\ \\

&\downarrow T_{2} \\
&\dots \\

&\downarrow T_{k} \\ \\

&\left(
\begin{array}{c|c}
A_{k} & B_{k}
\end{array}
\right) \text{ donde } A_{k} = I
\end{align}
$$
Cuando llegamos al final, si alcanzamos la forma reducida de $A (= I)$, se deduce que $B_{k} = A^{-1}$. Así tenemos:
$$
\begin{align}
&A_{0} = A, &&B_{0} = I \\
&A_{1} = E_{1}A, &&B_{1} = E_{1}\cancel{ I } \\
&A_{2} = E_{2}E_{1}A, &&B_{2} = E_{2}E_{1}\cancel{ I } \\
&\dots \\
&A_{k} = \underbrace{ \overbrace{ E_{k} \dots E_{2}E_{1} }^{ A^{-1} } A }_{ I }, &&B_{k} = E_{k} \dots E_{2}E_{1}
\end{align}
$$
Al final, como tenemos $A_{k} = E_{k} \dots E_{2}E_{1} A = I$, deducimos que $E_{k} \dots E_{2}E_{1} = A^{-1}$, pues la única matriz cuyo producto por $A$ es $I$, es $A^{-1}$.

Luego: $B_{k} = A^{-1}$

---
Ahora, pasaremos a un nuevo capítulo del temario: Determinantes
El objetivo es asociar a cada matriz cuadrada un número que indique si dicha matriz es invertible o no.
# Determinantes

> [!Objetivo]
> Asociar a cada matriz cuadrada $A \in M_{n \times n}$ un número $|A| \in \mathbb{R}$ tal que $A$ es invertible $\Longleftrightarrow |A| \neq 0$

Aunque pensemos que es una buena forma de ahorrarnos trabajo, en general, calcular el determinante de una matriz es mucho más costoso (tiene más operaciones), que intentar encontrar su inversa directamente. Tiene interés teórico principalmente.

A partir de ahora, solo trabajaremos con matrices cuadradas.

## Definición del determinante

> [!Matriz adjunta]
> Sea $A$ una matriz cuadrada de dimensión $n \geq 2$. Dados índices $i, j \in [1..n]$, se llama matriz adjunta a la matriz $A_{i,j}$ (cuadrada) de dimensión $n - 1$ obtenida eliminando la fila $i$ y la columna $j$

![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-04-08 - Clase 10 - Matrices Elementales y Determinantes/Imágenes/Representación de matriz adjunta.png]]
Es así que borrando la fila $i$ y la columna $j$ de la matriz $A$, obtenemos la matriz $A_{i,j}$ que es la misma matriz sin la fila $i$ y la columna $j$. De esta manera, se pierden $2n - 1$ elementos (puesto que la celda $a_{i,j}$ no se puede restar dos veces). La matriz obtenida es de tamaño $n - 1 \times n - 1$.

A continuación, definiremos el determinante por inducción sobre la dimensión de la matriz.

El determinante $|A| \in \mathbb{R}$ se define por inducción sobre la dimensión de $A$ de modo siguiente:
- Si $n=1$: $|A| = a_{1,1}$ (única entrada de $A$)
Podemos decir que no hay diferencia entre las matrices $1 \times 1$ y los reales, pues únicamente tienen un valor. Es así que el determinante en este caso es dicho valor.

- Si $n \geq 2$:
$$
\begin{align}
|A| &= \sum_{i = 1}^{n} (-1)^{i + 1} a_{i,1} \cdot |A_{i,1}| \\
&a_{1,1} |A_{1,1}| - a_{2,1} |A_{2,1}| + \dots + (-1)^{n+1} a_{n,1} |A_{n,1}|
\end{align}
$$
Lo que haremos es tomar la matriz adjunta de $A$ eliminando la fila $i$, y la columna 1 ($A_{i,1}$). Después, tomamos los elementos $a_{i,1}$ (todos los elementos de la primera columna), y para cada elemento construimos la matriz adjunta correspondiente (quitando la primera columna y fila correspondiente) y calculamos el producto del elemento y el determinante de la matriz adjunta correspondiente, multiplicando a este resultado por $(-1)^{i + 1}$ (-1 si el número de fila es par, y 1 si es par).

Es una fórmula bastante abstracta, pero es más sencillo representar gráficamente las operaciones realizadas.

A continuación, veremos la fórmula general para las matrices $2 \times 2$ (considerando la fórmula anterior):

## Proposición

> [!Fórmula general de cálculo de determinante en matrices dimensión 2]
> En dimensión 2:
> $$
> \left|
> \begin{array}{cc}
> a & b \\
> c & d
> \end{array}
> \right| = ad - cb
> $$

Para cada tamaño aparece una nueva fórmula, entonces, para calcular la determinante de una matriz $n \times n$, vamos a utilizar la fórmula para matrices de dimensión $n - 1$, en combinación con la fórmula general.

Seguidamente, veremos ejemplos de determinantes:

## Ejemplos
1. 
$$
\left|
\begin{array}{cc}
3 & 1 \\
7 & 2
\end{array}
\right| = 3 \times 2 - 7 \times 1 = 6 - 7 = -1
$$
Como vemos, un vistazo a los valores de una matriz no nos dicen nada sobre el valor de la determinante. No podemos deducir el signo de un determinante a partir del signo de los elementos de la matriz.

2. 
$$
\left|
\begin{array}{cc}
3 & -4 & 3 \\
-1 & 2 & 7 \\
-2 & 4 & 0
\end{array}
\right| = 3 \left|
\begin{array}{cc}
2 & 7 \\
4 & 0
\end{array}
\right| + 1 \left|
\begin{array}{cc}
-4 & 3 \\
4 & 0
\end{array}
\right| - 2 \left|
\begin{array}{cc}
-4 & 3 \\
2 & 7
\end{array}
\right|
$$
$$
= 3 (2 \times 0 - 4 \times 7) + 1 (-4 \times 0 - 4 \times 3) - 2 (-4 \times 7 - 2 \times 3) = 3 \times (-28) + 1 \times (-12) - 2 \times (-34)
$$
$$
= -84 - 12 + 68 = -28
$$
$$
\implies \left|
\begin{array}{cc}
3 & -4 & 3 \\
-1 & 2 & 7 \\
-2 & 4 & 0
\end{array}
\right| = -28
$$
La cantidad de operaciones aumenta considerablemente a medida que trabajamos con matrices mayores.

3. 
$$
\left|
\begin{array}{cc}
0_{n}
\end{array}
\right| = 0
$$
Para la matriz nula, el determinante siempre es 0, sin importar las dimensiones de dicha matriz.

4. 
$$
\left|
\begin{array}{cc}
I_{n}
\end{array}
\right| = \text{?}
$$
Aquí, el truco es hacer las cuentas por inducción sobre el tamaño:
$$
\left|
\begin{array}{cc}
1
\end{array}
\right| = 1
$$
$$
\left|
\begin{array}{cc}
1 & 0 \\
0 & 1
\end{array}
\right| = 1
$$
Aquí podemos desarrollar una conjetura: todas las matrices identidad tienen determinante igual a 1.
En este caso, demostraremos por inducción que
$$
\left|
\begin{array}{cc}
I_{n}
\end{array}
\right| = 1
$$
en todos los casos.

$$
\left|
\begin{array}{cc}
I_{n}
\end{array}
\right| = \left|
\begin{array}{cc}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\dots & \dots & \dots & \dots \\
0 & 0 & \dots & 1
\end{array}
\right|
$$
Si aplicamos la formula:
$$
=1 \cdot \left|
\begin{array}{cc}
I_{n - 1}
\end{array}
\right| - 0 \times \dots + 0 \times \dots - 0 \times \dots \dots
$$
$$
= \left|
\begin{array}{cc}
I_{n - 1}
\end{array}
\right| = 1
$$
De esta forma, demostramos por inducción sobre $n$ que la matriz identidad de tamaño cualquiera tiene determinante igual a 1.

---
Hasta ahora hemos desarrollado el determinante a partir de la primer columna, pero en realidad la formula general funciona para cualquier columna y cualquier fila, pero es fundamental cuidar los signos.

## Propiedad
Para toda matriz $A \in M_{n \times n}$ con $n \geq 2$
- $|A| = \sum_{i = 1}^{n} (-1)^{i + j} a_{i,j} \cdot |A_{i,j}| \qquad \text{para cada índice de columna } j \in [1..n]$

Podemos desarrollar la fórmula en base a las filas:
- $|A| = \sum_{j=1}^{n} (-1)^{i + j} a_{i,j} \cdot |A_{i,j}| \qquad \text{para todo índice de fila } i \in [1..n]$

Aquí, desarrollamos el determinante respecto a la columna $j$, en lugar de la columna 1. De esta manera, la formula solo depende de $j$. Ídem para la fila $i$.
Ahora, podemos operar respecto a una columna o fila particular dependiendo de si nos conviene más o no, pero siempre tenemos que considerar que el exponente del signo va a cambiar según esto.
Es importante entender que cada matriz tiene una matriz de signos (tomando como referencia el exponente de $-1$ en la formula general):
$$
\begin{pmatrix}
+ & - & + & - & \dots \\
- & + & - & + & \dots \\
+ & - & + & - & \dots \\
- & + & - & + & \dots
\end{pmatrix}
$$
Hay que considerar a esto, tomando en cuenta la columna o fila que tomamos como referencia.

Así, tenemos diferentes métodos para calcular el determinante de una matriz. Por ejemplo, si una matriz tiene una columna nula, tendrá determinante 0, ídem para las filas.