# Sistemas lineales de ecuaciones

Forma general de un sistema de m ecuaciones y n incógnitas
$$
(S){\begin{cases}
a_{1,1}x_{1}+a_{1,2}x_{2}+\dots+a_{1,n}x_{n}=b_{1} \\
a_{2,1}x_{1}+a_{2,2}x_{2}+\dots+a_{2,n}x_{n}=b_{2} \\
\dots{} \\
a_{m,1}x_{1}+a_{m,2}x_{2}+\dots+a_{m,n}x_{n}=b_{m}
\end{cases}}
$$
donde
- $x_{j}$ son las incógnitas
- $a_{ij}$ son los coeficientes
- $b_{i}$ son los términos independientes
Una forma más sencilla de entender esta representación, es viendo a i como el índice de las filas, y j como el índice de las columnas.

$Sol(S)={(x_{1},\dots,x_{n}) \in \mathbb{R}^{n} \text{ que cumplen (S)}}$
La/s soluciones no están dadas por valores individuales, sino por conjuntos de los mismos, siendo pares de n valores (columnas).

El sistema (S) es
* compatible determinado cuando $\lvert Sol(S) \rvert=1$.
Aclaración: normalmente usamos $\#A$ para denotar el cardinal del conjunto A.
* compatible indeterminado cuando $\lvert Sol(S) \rvert \geq 2$
* incompatible $\begin{cases} \lvert Sol(S) \rvert = 0 \\ Sol(S)= \emptyset \end{cases}$

Existen tres tipos de transformaciones elementales:
1. $F_{i} \longleftrightarrow F_{j}$
2. $F_{i} \longleftarrow \alpha F_{j}$ (con $\alpha \neq 0$)
3. $F_{i} \longleftarrow F_{i} + \alpha F_{j}$ (con $i \neq j$)

La clase pasa vimos que estas tres operaciones producen un nuevo sistema, el cual es equivalente al anterior, no importa si aplicamos una, o una serie de las mismas, siempre con la idea de encontrar la/s soluciones correspondientes.

Es importante adoptar una presentación menos pesada y cargada para facilitar la resolución de los mismos. Como podemos ver, en un sistema, los nombres de las incógnitas no nos interesan. Lo que si es importante son los números $a_{ij}$ y $b_{i}$. Para esto utilizaremos matrices.

# Representación con matrices.

<u>Def</u>: una matriz de m filas y n columnas (o matriz de tamaño $m \times n$) es un ordenamiento rectangular de números con m filas y n columnas.
$$
A=\begin{pmatrix}
a_{1,1} & a_{1,2} & \dots & a_{1,n} \\
a_{2,1} & a_{2,2} & \dots & a_{2,n} \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,n}
\end{pmatrix}
$$
Notación de matriz: $A=(a_{i,j})^{j=1\dots n}_{i=1\dots m}, \text{ o } A=(a_{i,j})$
Sucesión de los coeficientes $a_{i,j}$, con la particularidad de que tiene dos índices, siendo un rectángulo (un índice i para las filas y un índice j para las columnas). La segunda escritura es más sencilla, aunque no se especifica hasta donde van los índices, está implícito.

El conjunto de las matrices reales se escribe $M_{m \times n}$, también se utiliza $(M_{m \times n}(K) \text{ matrices con coeficientes en K})$. Cuando no se especifica nada, tomamos los coeficientes de los números reales, aunque también se pueden formar matrices con otros coeficientes, como pueden ser enteros, racionales, o incluso complejos.

Dos matrices $A=(a_{i,j})$ y $B=(b_{i,j})$ son iguales cuando:
1. tienen el mismo tamaño $m \times n$
2. $\forall i \in {1 \dots m},\forall j \in {1 \dots n}, a_{i,j}=b_{i,j}$ (para cualquier posición en la matriz A, la entrada tiene el mismo valor que la entrada correspondiente en B -mismo coeficiente-).
3. 

## Vocabulario
- matriz fila = matriz de tamaño $1 \times n$
- matriz columna = matriz de tamaño $m \times 1$
- matriz cuadrada = matriz de tamaño $n \times n$, de forma que $m=n$

Ahora, veremos como representamos un sistema lineal en forma de matriz:
Dado un sistema (S), se llaman:
- matriz del sistema a la matriz de los coeficientes (parte izquierda del sistema sin las incógnitas):
$$
A=\begin{pmatrix}
a_{1,1} & a_{1,2} & \dots & a_{1,n} \\
a_{2,1} & a_{2,2} & \dots & a_{2,n} \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,n}
\end{pmatrix}
$$
* columna de los términos independientes a la matriz columna
$$
b=\begin{pmatrix}
b_{1} \\
b_{2} \\
\dots \\
b_{m}
\end{pmatrix}
$$
- matriz ampliada del sistema (S) a la matriz
$$
(A|b)=\left(
\begin{array}{cccc|c}
a_{1,1} & a_{1,2} & \dots & a_{1,n} & b_1 \\
a_{2,1} & a_{1,2} & \dots & a_{2,n} & b_2 \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,n} & b_m
\end{array}
\right)
$$
## Ejemplo 6

$$
(S){\begin{cases}
x+y+2z=9 \\
3x+6y-5z=0 \\
2x+4y-3z=1
\end{cases}}
$$
Matriz ampliada:
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 2 & 9 \\
3 & 6 & -5 & 0 \\
2 & 4 & -3 & 1
\end{array}
\right)
$$
Es bastante sencillo traducir un sistema lineal de ecuaciones a una matriz. Simplemente eliminamos las variables, y nos quedamos con los coeficientes.
Para resolver el sistema, primeramente tenemos que definir el primer escalón, eliminando al 3 y 2 de la primer columna.
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 2 & 9 \\
0 & 3 & -11 & -27 \\
0 & 2 & -7 & -17
\end{array}
\right)
\begin{align}
F_{2} \leftarrow F_{2}-3F_{1} \\
F_{3} \leftarrow F_{3}-2F_{1}
\end{align}
$$
Definimos el primer escalón exitosamente. Proseguimos con el segundo:
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 2 & 9 \\
0 & 3 & -11 & -27 \\
0 & 0 & 1 & 3
\end{array}
\right)
F_{3} \leftarrow 3F_{3}-2F_{2}
$$
La matriz resultante representa un nuevo sistema, el cual comparte conjunto solución con S. Lo llamaremos S'
$$
(S'){\begin{cases}
x+y+2z=9 \\
3y-11z=-27 \\
z=3
\end{cases}}
$$
Sustitución por atrás:
$$
\begin{aligned}
&z=3 \\
&3y = 11z-27=11 \times 3 - 27 = 33-27 = 6 \\
&y=2 \\
&x=9-y-2z=9-2-2 \times 3 = 9-2-6 = 1 \\
&x=1
\end{aligned}
$$
Entonces, teniendo los valores correspondientes de x, y, y z, podemos responder definiendo el conjunto solución: $Sol(S)={(1,2,3)}$

Sin embargo, en lugar de utilizar la sustitución por atrás (comenzando por el último escalón), podríamos haber seguido reduciendo la matriz escalerizada.
Nosotros llegamos a la forma escalerizada de la matriz, lo que nos permitió aplicar la sustitución por atrás.
Sin embargo, se puede seguir reduciendo, hasta llegar a la forma escalerizada reducida:
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 2 & 9 \\
0 & 3 & -11 & -27 \\
0 & 0 & 1 & 3
\end{array}
\right)
$$
Lo que haremos es eliminar todos los coeficientes de las filas 1 y 2, sin ser el primero que es diferente de 0, con la idea de que en cada fila tengamos una ecuación con una única variable. De esta manera, la matriz tendrá forma de "diagonal".
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 2 & 9 \\
0 & 3 & 0 & 6 \\
0 & 0 & 1 & 3
\end{array}
\right)
F_{2} \leftarrow F_{2}+11F_{3}
$$
$$
\left(
\begin{array}{ccc|c}
3 & 0 & 6 & 21 \\
0 & 3 & 0 & 6 \\
0 & 0 & 1 & 3
\end{array}
\right)
F_{1} \leftarrow 3F_{1}-F_{2}
$$
$$
\left(
\begin{array}{ccc|c}
3 & 0 & 0 & 3 \\
0 & 3 & 0 & 6 \\
0 & 0 & 1 & 3
\end{array}
\right)
F_{1} \leftarrow F_{1}-6F_{3}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 1 \\
0 & 1 & 0 & 2 \\
0 & 0 & 1 & 3
\end{array}
\right)
\begin{aligned}
F_{1} \leftarrow \frac{F_{1}}{3} \\
F_{2} \leftarrow \frac{F_{2}}{3}
\end{aligned}
$$
Ahora que logramos llegar a la mencionada "diagonal", haciendo que cada ecuación del sistema contenga una única incógnita (específicamente con coeficiente 1, para que no tengamos que realizar posteriores operaciones), podemos proseguir a definir los valores de x, y, y z.
$$
\begin{aligned}
&x=1 \\
&y=2 \\
&z=3 \\
&Sol(S)={(1,2,3)}
\end{aligned}
$$
En definitiva, cada vez que llegamos a una forma escalerizada de una matriz, tenemos dos formas de proseguir:
* Aplicar la sustitución por atrás.
* Seguir reduciendo hasta alcanzar la forma escalerizada reducida.

Como podemos ver, el método de reducir hasta alcanzar la forma escalerizada reducida es algorítmico, puesto que es un procedimiento completamente monótono.

# Matriz escalerizada

<u>Def</u>: Se dice que una matriz está escalerizada cuando:
1. Todas las filas, salvo quizá la primera, comienzan con una sucesión de ceros.
2. Cada fila que sigue una fila no nula tiene al principio al menos un cero más que la fila anterior. Y cada fila que sigue una fila nula es nula.

Además, se dice que la matriz está en forma reducida cuando:
3. La primer entrada no nula de una fila es un 1.
4. La columna que corresponde a la primera entrada no nula de una fila tiene el resto de las entradas nulas. Esto significa que, para cada columna, habrá una única fila en la que el valor correspondiente a dicha columna será no nulo.

Un sistema es escalerizado cuando su matriz es escalerizada.

A continuación, presentamos la forma general de una matriz escalerizada no reducida:
![[Forma general de una matriz escalerizada no reducida.png|697]]

Es fundamental entender como se estructura la forma general de una matriz escalerizada reducida geométricamente. A continuación, una representación de la misma:
![[Forma general de una matriz escalerizada reducida.png]]
Como vemos, en las columnas en las que hay un 1, el resto de los elementos tienen que ser 0, mientras que cuando no hay un uno visible, puede haber cualquier cosa.

## Ejemplo 7
$$
A=\begin{pmatrix}
2 & 1 & 0 & 1 \\
0 & 3 & 2 & 1 \\
0 & 0 & 0 & 4
\end{pmatrix}
$$
Como podemos ver, la matriz está escalerizada, puesto que se visualizan varios de los escalones, aunque no está reducida, por varias razones:
* Vemos que en varias columnas hay varias filas con valores diferentes de 0, cuando únicamente debería haber una (siempre y cuando se trate de una columna en la que comienza algún escalón).
* No en todas las filas se comienza con el coeficiente 1, sino que algunas comienzan un coeficiente mayor.

Otro ejemplo de escalerizada no reducida:
$$
A=\begin{pmatrix}
2 & 1 & 0 & 1 \\
0 & 0 & 3 & 1 \\
0 & 0 & 0 & 2 \\
0 & 0 & 0 & 0
\end{pmatrix}
$$
Ejemplo de una matriz escalerizada reducida:
$$
A=\begin{pmatrix}
1 & 0 & 4 & 0 \\
0 & 1 & 2 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0
\end{pmatrix}
$$
En este caso, se nos presenta una matriz escalerizada (los escalones son claramente visibles), pero además reducida. Uno podría dudar por la columna que tiene 4 y 2, pero como esa columna no contiene ningún escalón (donde debería haber un único coeficiente 1) no hay problema.

Otro ejemplo:
$$
A=\begin{pmatrix}
1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & 2 & 0\\
0 & 0 & 0 & 0 & 1\\
0 & 0 & 0 & 0 & 0
\end{pmatrix}
$$
Aquí también se presenta una matriz escalerizada que está reducida, pues no hay columnas que contengan escalones (coeficiente 1 al comienzo) con múltiples coeficientes diferentes de 0, y todos los comienzos de escalón (coeficiente diferente de 0) tienen coeficiente 1.

## Ejemplo 8
$$
(S){\begin{cases}
2x+4y+2z=-2 \\
x+y+2z=0 \\
-x+y-2z=2
\end{cases}}
$$
$$
\left(
\begin{array}{ccc|c}
2 & 4 & 2 & -2 \\
1 & 1 & 2 & 0 \\
-1 & 1 & -2 & 2
\end{array}
\right)
$$
Vamos a comenzar con la sustitución de la segunda ecuación:
$$
\left(
\begin{array}{ccc|c}
2 & 4 & 2 & -2 \\
0 & 2 & 0 & 2 \\
-1 & 1 & -2 & 2
\end{array}
\right)
F_{2} \leftarrow F_{2}+F_{3}
$$
$$
\left(
\begin{array}{ccc|c}
2 & 4 & 2 & -2 \\
0 & 1 & 0 & 1 \\
-1 & 1 & -2 & 2
\end{array}
\right)
F_{2} \leftarrow \frac{F_{2}}{2}
$$
Ahora, proseguimos con la primer ecuación:
$$
\left(
\begin{array}{ccc|c}
1 & 5 & 0 & 0 \\
0 & 1 & 0 & 1 \\
-1 & 1 & -2 & 2
\end{array}
\right)
F_{1} \leftarrow F_{1}+F_{3}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -5 \\
0 & 1 & 0 & 1 \\
-1 & 1 & -2 & 2
\end{array}
\right)
F_{1} \leftarrow F_{1}-5F_{2}
$$
Finalmente, solo nos queda la tercer ecuación:
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -5 \\
0 & 1 & 0 & 1 \\
0 & 1 & -2 & -3
\end{array}
\right)
F_{3} \leftarrow F_{3}+F_{1}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -5 \\
0 & 1 & 0 & 1 \\
0 & 0 & -2 & -4
\end{array}
\right)
F_{3} \leftarrow F_{3}-F_{2}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -5 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 2
\end{array}
\right)
F_{3} \leftarrow \frac{F_{3}}{-2}
$$
De esta forma, llegamos al conjunto solución, tal que:
$$
\begin{aligned}
&x=-5 \\
&y=1 \\
&z=2 \\
&Sol(S)={(-5,1,2)}
\end{aligned}
$$
Recordar que se pueden desarrollar múltiples operaciones al mismo tiempo (siempre que sean sobre diferentes ecuaciones), no es necesario hacer paso por paso. Por ejemplo, es posible sustituir la fila 1 y la 2 a la vez, si eso agiliza el proceso y no complejiza el entendimiento del desarrollo.

Hasta ahora, hemos trabajado en sistemas compatibles determinados, pero en próximas clases veremos sistemas compatibles indeterminados, además de sistemas incompatibles.