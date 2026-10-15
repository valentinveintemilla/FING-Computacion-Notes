# Álgebra de matrices
Continuamos con el álgebra de matrices.

La clase pasada revisamos varias de las operaciones que se pueden realizar con matrices:
- Suma $A+B$ (se suman las celdas correspondientes, por lo que las matrices tienen que tener el mismo tamaño).
- Producto de un número por una matriz $\lambda \cdot A$ (se multiplica cada una de las celdas por $\lambda$).
- Matriz nula $0_{m \times n}$ (matriz de todo 0, elemento neutro respecto a la suma, obtengo la matriz inicial nuevamente).
- Matriz opuesta $-A = (-1) \cdot A$ (cada valor de la matriz A se cambia por el opuesto).
- Producto de matrices $AB : m \times n \text{ si } A: m \times p, B: p \times n$ (el producto de matrices se puede realizar si la cantidad de columnas de la primera es igual a la cantidad de columnas de la segunda, dando como resultado una matriz que tiene la misma cantidad de filas que la primera, y la misma cantidad de columnas que la segunda).

El producto $AB$ es la matriz $C = (c_{i,j})$ dada por
$$
c_{i,j} = \sum_{k = 1}^{p} a_{i,k} \cdot b_{k,j} \text{ para todos } i \in [1..m], j \in [1..n]
$$
Cada celda $c_{i,j}$ de la matriz resultante, está dada por la suma de los productos:
$$
a_{i,1} \times b_{1,j} + a_{i,2} \times b_{2,j} + \dots + a_{i,p} \times b_{p,j}
$$
Esto es válido ya que hay p elementos en la fila correspondiente en A, y en la columna correspondiente en B.

También determinamos la complejidad de la operación, necesitándose:
$$
\begin{align}
&m \cdot n \cdot p \text{ productos} \\
&m \cdot n \cdot (p-1) \text{ sumas}
\end{align}
$$
## Observación
A continuación, veremos como se pueden reducir y facilitar los cálculos de producto de matrices.

### Productos por columnas y por filas.

1. $\text{matriz } \times \text{ columna } = \text{ columna}$ ($m \times p, p \times 1 \longrightarrow m \times 1$)
Si multiplicamos una matriz por cualquier columna, obtenemos una columna (siendo posible si la matriz tiene misma cantidad de columnas que filas en la segunda).
2. $\text{fila } \times \text{ matriz } = \text{ fila}$ ($1 \times p, p \times n \longrightarrow 1 \times n$)
También podemos descomponer la segunda matriz de un producto en columnas, de modo que voy a trabajar con columnas de matrices que luego voy a unir para formar la matriz resultante, en lugar de trabajar con una matriz entera. También podemos hacer lo mismo, pero con las filas de la primer matriz: descomponer la primer matriz en filas y multiplicar cada fila con la segunda matriz, quedando varias matrices fila, que luego podemos unir para formar la matriz resultante.
$$
AB = \left(
\begin{array}{cccc}
AB^{1} & AB^{2} & \dots & AB^{n} \\
\dots & \dots & \dots & \dots
\end{array}
\right) = \left(
\begin{array}{cccc}
A_{1}B & \dots & \dots & \dots \\
\dots & \dots & \dots & \dots \\
A_{m}B & \dots & \dots & \dots
\end{array}
\right)
$$
$$
\begin{align} \\
&A_{i}B = \text{ i-ésima fila de A por B } = \text{ i-ésima fila de AB} \\
&AB^{j} = \text{ A por j-ésima columna de B } = \text{ j-ésima columna de AB}
\end{align}
$$
De esta forma, si alguna fila o columna es nula, la fila o columna correspondiente será nula. El objetivo de estos trucos es facilitar los cálculos. Por lo tanto, puedo descomponer a la primer matriz en filas, o a la segunda matriz en columnas para simplificar los cálculos. NO SE PUEDE HACER DE OTRA FORMA, no puedo descomponer a la primera en columnas o a la segunda en filas.

De esta manera, si cambio de lugar dos filas de la primer matriz, estarán intercambiadas en el resultado AB. Ídem para la segunda matriz con las columnas.

### Producto por bloques
Supongamos que
$A: m \times p, B: p \times n$
$m = m_{1} + m_{2}, p = p_{1} + p_{2}, n = n_{1} + n_{2}$ (los números m, p y n se pueden descomponer en las formas especificadas).
Sabiendo esto, podemos dividir nuestras matrices, cada una en cuatro bloques. De esta forma, lo que hago es dividir en bloques las matrices correspondientes, de forma que pueda calcular el producto de los bloques asociados, siendo la unión de dichos bloques el producto de las matrices iniciales. Igualmente, no tengo derecho a conmutar las cosas (siempre multiplico un trozo de la primer matriz por uno de la segunda, nunca al revés).
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-03-23 - Clase 7 - Producto de Matrices. Traspuesta. Matriz Invertible/Imágenes/Producto por bloques.png]]
La fórmula correspondiente es:
$$
C_{i,j} = \sum_{k = 1}^{2} A_{i,k}B_{k,j}
$$
Como vemos, la fórmula de producto de matrices también funciona a nivel macroscópico, es decir, la podemos aplicar en una matriz de matrices, por ejemplo (como hacemos en el dibujo anterior). Esto nos permite facilitar las operaciones y organizar de otra manera la resolución de problemas.

Incluso, este es el método tradicional para operar matrices para calcular producto de matrices en informática:
- Si las matrices son pequeñas, calculo el producto directamente.
- Si no son lo suficientemente pequeñas, las divido en cuatro e intento calcular el producto de cada una por separado.
Esto es recursivo, por lo que las dos condiciones anteriores se chequean en cada llamada (la segunda llamada vuelve a llamar a la función).

En todo caso, siempre hay que verificar que las divisiones sean adecuadas para permitir el producto de matrices, así como que la cantidad de bloques en cada matriz sea la necesaria como para permitir operar de forma adecuada (por ejemplo, la cantidad de bloques "en fila" de la primer matriz, debe ser igual a la cantidad de bloques "en columna" de la segunda matriz).

#### Ejemplo
$M,N \in M_{2n \times 2n}$ definida por
$$
\begin{align}

&M = \left(
\begin{array}{cc}
A & B \\
O_{n,n} & C
\end{array}
\right) \\
&N = \left(
\begin{array}{cc}
D & E \\
O_{n,n} & F
\end{array}
\right) \\
 \\
&MN =  \\
&\left(
\begin{array}{cc}
D & E \\
O & F
\end{array}
\right) \\

\left(
\begin{array}{cc}
A & B \\
O & C
\end{array}
\right)

&\left(
\begin{array}{cc}
AD & AE + BF \\
O & CF
\end{array}
\right)

\end{align}
$$
Aclaración $O_{n,n}$ es la matriz nula.

Ahora, recordaremos las propiedades del producto de matrices.

## Propiedades
1. $(AB)C = A(BC) \text{ si } \#c(A) = \#f(B), \#c(B) = \#f(C)$
Esto quiere decir que cuando tengo que desarrollar dos producto, significa que puedo comenzar por cualquiera de los dos productos, SIEMPRE Y CUANDO SE CUMPLA LA CONDICIÓN ESTABLECIDA. De esta manera, podemos escribir simplemente ABC.

Aunque tengamos derecho a sacar los paréntesis, esto no significa que podamos cambiar el orden de las matrices que se están multiplicando.

2. $A(B + C) = AB + AC \text{ si } \#c(A) = \#f(B) = \#f(C), \#c(B) = \#c(C)$
3. $(A + B)C = AC + BC \text{ si } \#f(A) = \#f(B) = \#c(C), \#c(A) = \#c(B)$
Lo mismo de siempre, no podemos intercambiar el orden de los productos. El orden en la suma no importa, pero si en el producto, por lo que si tengo AC, no puedo cambiarlo por CA.

El punto aquí es que la matriz $A(B + C)$ no tiene nada que ver con la matriz $C(A + B)$, lo que implica que la matriz $AB + AC$ no tiene nada que ver con la matriz $CA + CB$.

4. $OA = O, AO = O$
5. $\lambda \cdot (AB) = (\lambda \cdot A)B = A(\lambda \cdot B)$
Tenemos dos productos: producto por un número y producto por matrices. El producto con número es el único que conmuta con el producto de matrices. Esto se da ya que lambda es simplemente un número y no tiene problemas de conmutación.

PERO: $$AB \neq BA \text{ (en general)}$$
Hay excepciones, como por ejemplo que A y B sean iguales.

### Ejemplo
$A, B \in M_{n \times n}$ (trabajaremos con matrices cuadradas para simplificar las cosas, puesto que si tienen el mismo tamaño, siempre se pueden multiplicar y sumar. Las dimensiones no son un impedimento).
Quiero calcular las identidades notables
$$
\text{Por definición: } A^{2} = AA
$$
$$
\begin{align}
&(A+B)^{2} \\
&=(A+B)(A+B) \\
&=A(A+B) + B(A+B) \\
&=A^{2} + \underbrace{ AB + BA }_{ \neq 2AB \text{ y }
\neq 2BA }  + B^{2}
\end{align}
$$
Del mismo modo:
$$
(A-B)^{2} = A^{2} \underbrace{ - AB - BA }_{ \neq -2AB \text{ y }
\neq -2BA } + B^{2}
$$
Por último:
$$
(A+B)(A-B) = A^{2} \underbrace{ - AB + BA }_{ \neq O } - B^{2}
$$
La idea de todo esto es ver que las cuentas se hacen casi de la misma manera que con números normales, pero con la diferencia de que el producto no es conmutativo, no podemos intercambiar cosas como lo hacíamos anteriormente. Fuera de esto, todo funciona de modo usual.

Esto también justifica por qué lo llamamos "producto de matrices" y no "segunda suma" o "suma-producto" (puesto que también operamos con sumas cuando multiplicamos dos matrices, también hay sumas envueltas). La justificación de esto yace en las propiedades de la operación, que son las mismas que la del producto en los números (menos la conmutatividad).

Ahora, pasamos a un nuevo concepto dentro de las matrices.

# Matriz traspuesta
Como vimos, podemos descomponer las matrices en filas y columnas. Lo que esta claro es que por simetría, lo que funciona para filas, debería funcionar para las columnas, y viceversa.
Existe una operación que permite intercambiar la noción de fila y columna realizando una simetría considerando la diagonal de una matriz, y esta es la matriz traspuesta.

**Definición**
Dada una matriz $A = (a_{i,j}) \in M_{m \times n}$, se llama traspuesta de A a la matriz $A^{t} = (a'_{i,j}) \in M_{n \times m}$ definida por:
$$
a'_{i,j} = a_{j,i} \text{ para todos } i \in [1..n], j \in [1..m]
$$
Importante: si la matriz es de $m \times n$, la traspuesta es de $n \times m$.
Al aplicar la traspuesta a una matriz, las columnas se vuelven filas y viceversa (primer fila se vuelve primer columna, segunda fila se vuelve segunda columna, etc., y primer columna se vuelve primer fila, segunda columna se vuelve segunda fila, etc.).
## Ejemplo
$$
\left(
\begin{array}{ccc}
3 & 0 & 1 \\
\sqrt{ 2 } & \pi & -5
\end{array}
\right)^{t} = \left(
\begin{array}{cc}
3 & \sqrt{ 2 } \\
0 & \pi \\
1 & -5
\end{array}
\right)
$$
El interés de esta operación es intercambiar la noción de fila y columna, lo que nos permite que todas las propiedades que apliquen a una (filas por ejemplo), también aplican para la otra (columnas), y viceversa.

Esta operación tiene una serie de propiedades.

## Propiedades
1. $(A+B)^{t} = A^{t} + B^{t}, O^{t}_{m \times n} = O_{n \times m}, (-A)^{t} = -(A^{t})$
2. $(\lambda \cdot A)^{t} = \lambda \cdot (A^{t})$
3. $(AB)^{t} = B^{t}A^{t}$
Tenemos que intercambiar el producto (invertir el orden de las matrices). Esto se debe a que intercambiamos el papel de fila y columna, y el producto depende fuertemente de las mismas (cuales son filas y cuales son columnas).

4. $(A^{t})^{t} = A$
La matriz traspuesta es una operación involutiva, ya que cuando se aplica dos veces, volvemos al punto inicial. Existen otras, como el opuesto, el inverso cuando está definido, entre otras.

## Vocabulario
Una matriz cuadrada $A \in M_{n \times n}$ es:
- simétrica cuando $A^{t} = A$
- antisimétrica cuando $A^{t} = -A$ (la diagonal tiene que ser nula, puesto que es la única forma que , sin cambiar en la traspuesta, el elemento sea igual a su opuesto. Además, un elemento y su "correspondiente en la trasposición" tienen que ser opuestos).

Pasamos al siguiente tema.
# Ecuaciones matriciales. Matriz inversa
Ya vimos que cuando teníamos un sistema, podíamos expresarlo como la matriz de coeficientes por la columna de las incógnitas, e igualar esto a los términos independientes.

## Proposición
Cada sistema lineal
$$
(S){\begin{cases}
a_{1,1}x_{1} + \dots + a_{1,n}x_{n} = b_{1} \\
\dots \\
a_{m,1}x_{1} + \dots + a_{m,n}x_{n} = b_{m}
\end{cases}}
$$
es equivalente a la ecuación matricial
$$
\begin{align}
&\underbrace{ \left(
\begin{array}{ccc}
a_{1,1} & \dots & a_{1,n} \\
a_{2,1} & \dots & a_{2,n} \\
\dots \\
a_{m,1} & \dots & a_{m,n}
\end{array}
\right) }_{ A } \times \underbrace{ \left(
\begin{array}{c}
x_{1} \\
x_{2} \\
\dots \\
x_{n}
\end{array}
\right) }_{ X } = \underbrace{ \left(
\begin{array}{c}
b_{1} \\
b_{2} \\
\dots \\
b_{m}
\end{array}
\right) }_{ B } \\
 \\
&AX = B
\end{align}
$$
Como sabemos, el producto de las matrices anteriores nos dará como resultado una nueva matriz columna, la cual tendrá en cada celda, la suma de todos los elementos de cada fila (correspondiente a esa celda), cada uno multiplicado por la incógnita correspondiente (por ejemplo, el único elemento de la primera fila será $a_{1,1}x_{1} + a_{1,2}x_{2} + \dots + a_{1,n}x_{n}$).

Partimos de un problema complejo, un sistema de ecuaciones, cargado de incógnitas, ecuaciones, con objetos sencillos como lo son los números, y lo transformamos en un problema sencillo, una ecuación, una incógnita, con objetos complejos. Este es uno de los principales fundamentos de matemática.
Sin embargo, es fundamental saber como manipular dichos objetos, saber que se puede y no puede hacer con ellos.

Por ejemplo, si intentamos despejar la X, dividiendo a B entre A, nos encontramos con una serie de problemas. Primero que nada, no sabemos si podemos dividir entre A. Además, como la multiplicación no es conmutativa, la división tampoco lo es. Esto último resulta en tener dos cocientes a la hora de dividir por matrices:
$$
\begin{align}
&A^{-1}B = A \setminus B \rightarrow \text{(cociente por la izquierda)} \\
&BA^{-1} = B / A \rightarrow \text{(cociente por la derecha)}
\end{align}
$$
De esta forma, en lugar de escribir
$$
AX = B \implies X = \frac{B}{A}
$$
lo expresaremos como
$$
AX = B \implies X = A^{-1}B
$$
Aún nos falta dar un sentido al inverso de una matriz.

La idea es poder extender las propiedades de los números a las matrices.
Para esto, vamos a comprender el concepto de inverso para los números:
$$
y = x^{-1} \Longleftrightarrow xy = 1
$$
El problema de expresarlo de esta forma es que aún no hemos definido una matriz 1 (tenemos una matriz nula, pero no una 1), y el orden, en que orden deberían multiplicarse los valores (puesto que si importa en las matrices).

Comencemos por la matriz identidad (matriz 1):
### Matriz identidad
Se llama matriz identidad de tamaño $n \times n$ a la matriz $I_{n} = (S_{i,j})$ definida por
$$
\begin{align}
&S_{i,j}= \begin{cases}
1 \text{ si } i = j \\
0 \text{ si no} 
\end{cases} \\
 \\
&I_{n} = \left(
\begin{array}{cc}
1 & 0 \\
0 & 1
\end{array}
\right)
\end{align}
$$
Como vemos, según la definición, el coeficiente es 1 únicamente en la diagonal, siendo 0 en todo el resto de casos.

Ahora, tenemos que verificar que se comporta como 1. Por ejemplo, cuando multiplicamos algo por 1, obtenemos el valor inicial nuevamente.

#### Propiedad
Para toda matriz $A \in M_{m \times n}$
$$
\underbrace{ I_{m} \cdot A }_{ m \times n } = \underbrace{ A \cdot I_{n} }_{ m \times n } = A
$$
Como vemos, la identidad es el neutro del producto de matrices. Es muy fácil de demostrar con un ejemplo. Además, considerar que es una matriz simétrica.

A continuación, podemos definir la nocion de matriz invertible.

### Matriz invertible
Se dice que una matriz cuadrada $A \in M_{n \times n}$ es invertible cuando existe $B \in M_{n \times n}$ tal que
$$
AB = BA = I_{n}
$$
Digo que una matriz es invertible cuando existe una matriz B que es inversa por la derecha, y a la vez es inversa por la izquierda.
Cuando es el caso, la matriz B es única, se llama la inversa de A y se escribe $B = A^{-1}$.
Con esto, también queda claro que hay matrices que no son invertibles (incluso siendo cuadradas).
Un ejemplo es la matriz nula.

En la próxima clase, veremos varios ejemplos más.