Recordamos lo que es una matriz
# Matriz
**Definición**: Dados enteros $m,n \geq 1$ se llama matriz de tamaño $m \times n$ a toda función
$$
\begin{align}
&A:[1..m]\times[1..n] \to \mathbb{R} \\
&\text{Es una definición más formal que la que vimos anteriormente, aunque en esencia describe una tabla de valores.} \\ \\

&A=(a_{i,j})=\left(
\begin{array}{cccc}
a_{1,1} & a_{1,2} & \dots & a_{1,n} \\
a_{2,1} & a_{2,2} & \dots & a_{2,n} \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,n}
\end{array}
\right)
\end{align}
$$
El conjunto de las matrices de tamaño $m \times n$ se escribe $M_{m \times n}$.

Algunas convenciones:
- Siempre ponemos primero el índice de fila (i) y luego el índice de columna (j).
- Utilizamos m para denotar la cantidad de filas (ecuaciones), y n para denotar la cantidad de columnas (incógnitas).

## Observación
Se pueden considerar matrices con coeficientes en cualquier <u>cuerpo</u> (conjunto de números que se porta bien con la suma, resta, multiplicación y división) K ($K = \mathbb{Q}, \mathbb{R}, \text{ o } \mathbb{C}$)
**Notación**: $M_{m \times n}(K)$

Vamos a observar que las matrices tienen operaciones.

# Suma de matrices
**Definición**
Si tengo dos matrices del mismo tamaño, sumo entrada por entrada (primer elemento + primer elemento, segundo elemento + segundo elemento, etc.).

Dadas dos matrices $A=(a_{i,j}) \text{ y } B=(b_{i,j})$ de mismo tamaño $m \times n$ (obligatoriamente deben tener el mismo tamaño), se define la suma $A + B$ como la matriz ($c_{i,j}$) de mismo tamaño dada por:
$$
c_{i,j}=a_{i,j}+b_{i,j} \qquad \text{(para todos } i \in [1..m], j \in [1..n])
$$
Aclaración: $[1..m]$ es un intervalo entero, solo contiene enteros naturales (entre 1 y m).

## Ejemplo 1
$$
\left(
\begin{array}{cc}
1 & 2 \\
0 & \pi \\
-3 & 5
\end{array}
\right)
+
\left(
\begin{array}{cc}
0 & 9 \\
5 & -4 \\
2 & \sqrt{ 2 }
\end{array}
\right)
=
\left(
\begin{array}{cc}
1 & 11 \\
5 & \pi-4 \\
-1 & 5+\sqrt{ 2 }
\end{array}
\right)
$$
Aunque la operación sea obvia, tiene propiedades interesantes

## Propiedades
La operación $(+): M_{m \times n} \times M_{m \times n} \to M_{m \times n}$ es asociativa y conmutativa:
$$
\begin{align}
&\text{1. } (A + B) + C = A + (B + C) \text{ (es asociativa)} \\
&\text{2. } A + B = B + A \text{ (es conmutativa, el orden no importa)} \\
&\text{3. } A + O = A\text{ (Tiene un elemento neutro: la matriz nula } 0_{m \times n} \text{ (todo 0)})\\
&\text{4. } A + (-A) = (-A) + A = O \text{ (Toda matriz tiene una matriz opuesta} -A=(-a_{i,j}))
\end{align}
$$
Aclaración:
$(+): M_{m \times n} \times M_{m \times n} \to M_{m \times n}$ significa que estamos definiendo la función "+".
Normalmente definimos a la suma como $x+y=(+)(x,y)$.
Se lee como "la función '+' aplicada a sus dos argumentos. Sus dos argumentos forman un par, y dicho par pertenece a un producto cartesiano."

Otra particularidad es que hay infinitas matrices nulas, de diferentes tamaños.

Podemos decir que es lo mismo que la suma usual, ampliada para tablas de números. Sin embargo, es fundamental chequear siempre que las matrices sean del mismo tamaño.

# Producto de números por matrices
**Definición**
Dados un número $\lambda \in \mathbb{R}$ y una matriz $A=(a_{i,j})$ de tamaño $m \times n$, se define la matriz $\lambda \cdot A$ como la matriz $C=(c_{i,j})$ definida por
$$
c_{i,j} = \lambda \cdot a_{i,j} \qquad \text{(para todos } i \in [1..m], j \in [1..n])
$$
Para obtener la matriz resultante, hay que multiplicar cada entrada de la matriz origen por $\lambda$.
Es igual que el producto de números por vectores: se multiplican todas las dimensiones por el valor correspondiente.

## Ejemplo 2
$$
\begin{align}
&\lambda = \sqrt{ 2 } \text{ y }
A=\left(
\begin{array}{cc}
\sqrt{ 2 } & 1 \\
0 & -\sqrt{ 2 }
\end{array}
\right) \\
&\text{ Entonces } \lambda \cdot A=\left(
\begin{array}{cc}
2 & \sqrt{ 2 } \\
0 & -2
\end{array}
\right) 
\end{align}
$$
Hay que entender que es una función que toma un número, una matriz de cierto tamaño, y devuelve una matriz de mismo tamaño.

A continuación, estudiamos las propiedades:

## Propiedades
La operación $(\cdot): \mathbb{R} \times M_{m \times n} \to M_{m \times n}$ cumple las siguientes igualdades:
1. $0 \cdot A = O$
2. $1 \cdot A = A$
3. $(-1) \cdot A = -A$
4. $(\lambda \mu) \cdot A = \lambda \cdot (\mu \cdot A)$
5. $(\lambda + \mu) \cdot A = \lambda \cdot A + \mu \cdot A$
6. $\lambda \cdot (A + B) = \lambda \cdot A + \lambda \cdot B$
Es fundamental entender que no es lo mismo la suma de números que la suma de matrices. Hay que tener en cuenta sus diferencias en todo momento con tal de no cometer errores a la hora de operar. Ídem para el producto (en este caso incluso cambia el símbolo, pasando de $\times$ para números, a $\cdot$ para matrices).

### Observación
Combinando (5) y (6) se deduce:
7. $(\lambda + \mu) \cdot (A + B) = \lambda \cdot A + \lambda \cdot B + \mu \cdot A + \mu \cdot B$
Esta es la distributividad total.

Hasta aquí hemos visto las dos operaciones sencillas que envuelven matrices. A continuación, veremos el producto de matrices, operación que no es trivial. La lógica nos diría que se multiplican entrada por entrada, pero nada más alejado de la realidad.

# Producto de matrices
**Definición**
Dadas matrices
- $A = (a_{i,j})$ de tamaño $m \times p$
- $B = (b_{i,j})$ de tamaño $p \times n$
Tenemos tres enteros que pueden ser distintos. Lo importante para hacer el producto de matrices es que la cantidad de columnas de la primera matriz sea igual a la cantidad de filas de la segunda matriz.

Se define el producto $AB$ como la matriz $(c_{i,j})$ de tamaño $m \times n$ (cantidad de filas de la primera y cantidad de columnas de la segunda) definida por:
$$
c_{i,j} = \sum_{k=1}^{p} a_{i,k} \cdot b_{k,j} \qquad \text{(para todos } i \in [1..m], j \in [1..n])
$$
- i: Índice de fila de C e índice de fila de A (recorre todos los enteros de 1 a m).
- j: Índice de columna de C e índice de columna de B (recorre todos los enteros de 1 a n).
- k: Índice de columna de A e índice de fila de B (recorre todos los enteros de 1 a p).

IMPORTANTE: No se puede multiplicar cualquier par de matrices.
Solo se pueden multiplicar AB cuando $\#col(a) = \#filas(B)$ y tenemos que
$$
\begin{align}
&\#filas(AB) = \#filas(A) \\
&\#col(AB) = \#col(B)
\end{align}
$$

Ahora veremos el algoritmo para calcular un producto. La disposición del cálculo es la siguiente:
$$
\begin{align}
&A=(a_{ij}) \in M_{m \times p} \\
&B=(b_{ij}) \in M_{p \times n} \\ \\

&A=\left(
\begin{array}{cccc}
a_{1,1} & a_{1,2} & \dots & a_{1,p} \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,p}
\end{array}
\right) \\
&B=\left(
\begin{array}{cccc}
b_{1,1} & b_{1,2} & \dots & b_{1,n} \\
\dots \\
b_{p,1} & b_{p,2} & \dots & b_{p,n}
\end{array}
\right)
\end{align}
$$
Colocamos la primera matriz a la izquierda y la segunda arriba, dejando un espacio en el medio (donde ira la matriz resultante) de tamaño $m \times n$.
Para calcular cada uno de los valores de la matriz resultante, tenemos que hacer lo siguiente:
- Considerar el valor de i y j para la celda correspondiente en la matriz C.
- Considerar todos los valores de la fila i en la matriz A.
- Considerar todos los valores de la fila j en la matriz B.
- El resultado de $c_{i,j}$ será un producto miembro por miembro de los valores de la fila i en la matriz A y los valores de la fila j en la matriz B:
$$
c_{i,j}=a_{i,1} \times b_{1,j} + a_{i,2} \times b_{2,j} + a_{i,3} \times b_{3,j} + \dots + a_{i,p} \times b_{p,j}
$$
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-03-18 - Clase 6 - Álgebra de Matrices/Imágenes/Producto de matrices.png]]
Siempre que multiplico A y B, se posicionan como mencionamos anteriormente.

## Ejemplo 3
$$
\begin{align}
&A=\left(
\begin{array}{cc}
2 & -1 \\
0 & 2
\end{array}
\right) \\
&B=\left(
\begin{array}{cc}
3 & 1 \\
-2 & 6
\end{array}
\right) \\
&AB=?

\end{align}
$$
Primero que nada, analizamos que las matrices se puedan multiplicar. Como vemos que el número de filas de A es igual al número de columnas de
$$
\begin{align}
&\left(
\begin{array}{cc}
3 & 1 \\
-2 & 6
\end{array}
\right) \\

\left(
\begin{array}{cc}
2 & -1 \\
0 & 2
\end{array}
\right)

&\left(
\begin{array}{cc}
2 \times 3 + (-1) \times (-2) & 2 \times 1 + (-1) \times 6 \\
0 \times 3 + 2 \times (-2) & 0 \times 1 + 2 \times 6
\end{array}
\right)
\end{align}
$$
Resolución
$$
\begin{align}
&\left(
\begin{array}{cc}
3 & 1 \\
-2 & 6
\end{array}
\right) \\

\left(
\begin{array}{cc}
2 & -1 \\
0 & 2
\end{array}
\right)

&\left(
\begin{array}{cc}
6 + 2 & 2 - 6 \\
0 - 4 & 0 + 12
\end{array}
\right)
\end{align}
$$
$$
\begin{align}
&\left(
\begin{array}{cc}
3 & 1 \\
-2 & 6
\end{array}
\right) \\

\left(
\begin{array}{cc}
2 & -1 \\
0 & 2
\end{array}
\right)

&\left(
\begin{array}{cc}
8 & -4 \\
-4 & 12
\end{array}
\right) \\ \\

&AB = \left(
\begin{array}{cc}
8 & -4 \\
-4 & 12
\end{array}
\right)
\end{align}
$$
Lo interesante es que como ambas matrices son de $2 \times 2$ (todas sus dimensiones son 2), no solo puedo hacer el producto $AB$, sino también $BA$. A continuación, realizamos dicho producto.
$$
\begin{align}
&\left(
\begin{array}{cc}
2 & -1 \\
0 & 2
\end{array}
\right) \\

\left(
\begin{array}{cc}
3 & 1 \\
-2 & 6
\end{array}
\right)

&\left(
\begin{array}{cc}
3 \times 2 + 1 \times (0) & 3 \times (-1) + 1 \times 2 \\
(-2) \times 2 + 6 \times 0 & (-2) \times (-1) + 6 \times 2
\end{array}
\right)
\end{align}
$$
$$
\begin{align}
&\left(
\begin{array}{cc}
2 & -1 \\
0 & 2
\end{array}
\right) \\

\left(
\begin{array}{cc}
3 & 1 \\
-2 & 6
\end{array}
\right)

&\left(
\begin{array}{cc}
6 + 0 & -3 + 2 \\
-4 + 0 & 2 + 12
\end{array}
\right)
\end{align}
$$
$$
\begin{align}
&\left(
\begin{array}{cc}
2 & -1 \\
0 & 2
\end{array}
\right) \\

\left(
\begin{array}{cc}
3 & 1 \\
-2 & 6
\end{array}
\right)

&\left(
\begin{array}{cc}
6 & -1 \\
-4 & 14
\end{array}
\right) \\ \\

&BA = \left(
\begin{array}{cc}
6 & -1 \\
-4 & 14
\end{array}
\right)
\end{align}
$$
Como vemos, en este caso el resultado es diferente ($AB \neq BA$).

**Moraleja**: $AB \neq BA$ (en general)
De esta forma, podemos establecer que, en general, el producto de matrices no es conmutativo, por lo que no debemos cambiar el orden de dos matrices a la hora de hacer su producto.

En conclusión, la conmutatividad del producto es siempre verdadera para los números, pero rara vez es verdadera para las matrices. Entonces, siempre que se nos pregunte sobre la conmutatividad de dos elementos para el producto, debemos chequear que tipo de objetos son.

## Ejemplo 4
$$
\begin{align}
&A=\left(
\begin{array}{cccc}
2 & -1 & 4 & 0 \\
0 & 2 & 1 & 5
\end{array}
\right) \\
&B=\left(
\begin{array}{cc}
1 & 2 \\
2 & 1 \\
1 & 1 \\
1 & 0
\end{array}
\right) \\
&AB=?
\end{align}
$$
En este caso, también es posible calcular $BA$.
$$
\begin{align}
&\left(
\begin{array}{cc}
1 & 2 \\
2 & 1 \\
1 & 1 \\
1 & 0
\end{array}
\right) \\

\left(
\begin{array}{cccc}
2 & -1 & 4 & 0 \\
0 & 2 & 1 & 5
\end{array}
\right)

&\left(
\begin{array}{cc}
2 - 2 + 4 + 0 & 4 - 1 + 4 + 0 \\
0 + 4 + 1 + 5 & 0 + 2 + 1 + 0
\end{array}
\right) \\
\end{align}
$$
$$
\begin{align}
&\left(
\begin{array}{cc}
1 & 2 \\
2 & 1 \\
1 & 1 \\
1 & 0
\end{array}
\right) \\

\left(
\begin{array}{cccc}
2 & -1 & 4 & 0 \\
0 & 2 & 1 & 5
\end{array}
\right)

&\left(
\begin{array}{cc}
4 & 7 \\
10 & 3
\end{array}
\right) \\ \\

&AB = \left(
\begin{array}{cc}
4 & 7 \\
10 & 3
\end{array}
\right)
\end{align}
$$
Ahora calculamos $BA$:
$$
\begin{align}
&\left(
\begin{array}{cccc}
2 & -1 & 4 & 0 \\
0 & 2 & 1 & 5
\end{array}
\right) \\

\left(
\begin{array}{cc}
1 & 2 \\
2 & 1 \\
1 & 1 \\
1 & 0
\end{array}
\right)

&\left(
\begin{array}{cccc}
2+0 & -1+4 & 4+2 & 0+10 \\
4+0 & -2+2 & 8+1 & 0+5 \\
2+0 & -1+2 & 4+1 & 0+5 \\
2+0 & -1+0 & 4+0 & 0+0
\end{array}
\right) \\
\end{align}
$$
$$
\begin{align}
&\left(
\begin{array}{cccc}
2 & -1 & 4 & 0 \\
0 & 2 & 1 & 5
\end{array}
\right) \\

\left(
\begin{array}{cc}
1 & 2 \\
2 & 1 \\
1 & 1 \\
1 & 0
\end{array}
\right)

&\left(
\begin{array}{cccc}
2 & 3 & 6 & 10 \\
4 & 0 & 9 & 5 \\
2 & 1 & 5 & 5 \\
2 & -1 & 4 & 0
\end{array}
\right) \\ \\

&BA=\left(
\begin{array}{cccc}
2 & 3 & 6 & 10 \\
4 & 0 & 9 & 5 \\
2 & 1 & 5 & 5 \\
2 & -1 & 4 & 0
\end{array}
\right)
\end{align}
$$
Como vemos AB y BA no tienen nada que ver, ni en sus valores ni en su tamaño. Es casi seguro de que si trabajamos con matrices aleatorias, estas nunca se van a conmutar desde el punto de vista del producto.

Ahora podemos hablar de la complejidad de las distintas operaciones.

<u>Suma</u>:
$$
\begin{align}
&M_{m \times n} \times M_{m \times n} \to M_{m \times n} \\
&m \cdot n \text{ sumas elementales.} \\
&(n^{2} \text{ si } m = n)
\end{align}
$$
<u>Producto por un número</u>
$$
\begin{align}
&\mathbb{R} \times M_{m \times n} \to M_{m \times n} \\
&m \cdot n \text{ productos elementales.} \\
&(n^{2} \text{ si } m = n)
\end{align}
$$
<u>Producto de matrices</u>
Supongo que tengo dos matrices (caso general):
$$
\begin{align}
&(\times): M_{m \times p} \times M_{p \times n} \to M_{m \times n} \\
&m \cdot n \cdot p \text{ productos elementales} \\
&m \cdot n \cdot (p-1) \text{ sumas elementales} \\
&(n^{3} \text{ productos } + n^{2}(n-1) \text{ sumas cuando } n=m=p)
\end{align}
$$
Analizamos a la operación de modo geométrico para entender cuantas veces se realiza cada operación:
Para calcular una entrada del producto, tengo que hacer sumas de p números, necesitando un total de p-1 sumas (estamos hablando de que esto es únicamente para una celda). Para calcular la cantidad total, multiplicamos dichos valores por $m \cdot n$ (el tamaño de la matriz resultante).

![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-03-18 - Clase 6 - Álgebra de Matrices/Imágenes/Producto de matrices (geometría).png]]

El producto de matriz ha sido un tema de especial interés para investigadores, más aún sabiendo lo importante que es para la ingeniería. Se han buscado algoritmos que reduzcan la cantidad de operaciones realizadas, con la idea de facilitar el cálculo para matrices extremadamente grandes (y que el cálculo sea posible para las computadoras). Si bien existen, no los veremos puesto que son bastante complejos. Seguiremos utilizando el método tradicional.

A continuación, vamos a justificar por qué adoptamos una definición tan complicada para el producto de matrices (por qué no podía simplemente ser una multiplicación entrada por entrada). Para esto, hay tres razones, las cuales serán vistas a través de un ejemplo:

## Ejemplo 5

Sea el sistema:
$$
(S){\begin{cases}
2x+4y+2z=-2 \\
x+y+2z=0 \\
-x+y-4z=2
\end{cases}}
$$
No lo vamos a resolver, simplemente lo expresaremos gracias a las matrices.
Sean
$$
\begin{align}
A=\left(
\begin{array}{ccc}
2 & 4 & 2 \\
1 & 1 & 2 \\
-1 & 1 & -4
\end{array}
\right) \qquad

B=\left(
\begin{array}{c}
-2 \\
0 \\
2
\end{array}
\right) \qquad

X=\left(
\begin{array}{c}
x \\
y \\
z
\end{array}
\right)
\end{align}
$$
A contiene los coeficientes, B los términos independientes, y X las incógnitas (columna de las incógnitas, no la vimos anteriormente).
A continuación, calculamos $AX$:
$$
\begin{align}
&\left(
\begin{array}{c}
x \\
y \\
z
\end{array}
\right) \\

\left(
\begin{array}{ccc}
2 & 4 & 2 \\
1 & 1 & 2 \\
-1 & 1 & -4
\end{array}
\right)

&\left(
\begin{array}{ccc}
2x + 4y + 2z \\
x + y + 2z \\
-x + y - 4z
\end{array}
\right) \\ \\

&AX=\left(
\begin{array}{ccc}
2x + 4y + 2z \\
x + y + 2z \\
-x + y - 4z
\end{array}
\right)
\end{align}
$$
De esta forma, obtuvimos el lado izquierdo del sistema, de forma que podemos concluir que el sistema es equivalente a:
$$
AX = B
$$
La ventaja es que pudimos reemplazar un sistema de ecuaciones (pudiendo ser cualquier sistema), por una simple ecuación. Esto funciona con cualquier sistema lineal, pudiendo reemplazarlo por una ecuación de matrices.
Entonces, resolver un sistema lineal es equivalente a resolver una única ecuación matricial.

Cuando se nos presenta la ecuación $AX = B$, el primer instinto es igualarlo a $X = \frac{B}{A}$. De hecho, toda el algebra de matriz consiste en dar un sentido a lo anterior, para extender todos los métodos de resolución que ya conocemos para ecuaciones de primer grado a las matrices. Todo lo que haremos después se basa en qué sentido podríamos definir $X = \frac{B}{A}$. En realidad $X = \frac{B}{A}$ es totalmente incorrecto, pero podemos escribir su equivalente $X = A^{-1}B$, en caso de que $A^{-1}$ exista.

El movimiento general de la matemática consiste en transformar problemas muy complejos sobre objetos sencillos, en problemas sencillos sobre objetos complejos. De esta forma, ponemos la complejidad del problema en los objetos, y trabajar sobre estos como si fueran sencillos, que es exactamente lo que hicimos (partiendo de un sistema de ecuaciones, y llegando a una ecuación de primer grado de matrices).

A continuación, las propiedades del producto de matrices.

## Propiedades
1. $(AB)C = A(BC) \qquad \#c(A)=\#f(B) \land \#c(B) = \#f(C)$ (es una operación asociativa)
2. $(A+B)C = AC + BC$ (es una operación distributiva por la izquierda)
3. $C(A + B) = CA + CB$ (es una operación distributiva por la derecha)
4. $AO = O$ y $OA = O$
5. $\lambda \cdot (AB) = (\lambda \cdot A)B = A(\lambda \cdot B)$ (producto de número por matriz por producto de número funciona bien)

En todas estas propiedades, se requiere que las matrices tengan los tamaños adecuados. Por ejemplo, entre otras cosas a considerar, $AC + BC \neq CA + CB \implies (A+B)C \neq C(A + B)$.

Las propiedades del producto de matrices serán profundizadas próximamente.