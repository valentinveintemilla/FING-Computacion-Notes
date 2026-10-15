# Método de escalerización de Rouché-Frobenius
Como recordamos, tenemos tres posibles tipos de sistemas:
- Sistema Compatible Determinado.
- Sistema Compatible Indeterminado.
- Sistema Incompatible.

El caso más desafiante es el caso Compatible Indeterminado, donde aunque sepamos que hay infinitas soluciones, tenemos que llegar a una "fórmula" que, en base a determinados parámetros, represente la solución.

## Ejemplo 10
$$
\left(
\begin{array}{cccccc|c}
1 & 2 & 1 & 0 & 1 & 1 & 1 \\
-1 & -2 & 1 & 1 & 0 & -1 & 0 \\
1 & 2 & 1 & 2 & 5 & 3 & 1 \\
1 & 2 & 1 & 0 & 1 & 3 & 3 \\
1 & 2 & 1 & 4 & 9 & 3 & -1
\end{array}
\right)
$$
Al escalerizar, llegamos al siguiente resultado:
$$
\left(
\begin{array}{cccccc|c}
1 & 2 & 0 & 0 & \frac{3}{2} & 0 & -1 \\
0 & 0 & 1 & 0 & -\frac{1}{2} & 0 & 1 \\
0 & 0 & 0 & 1 & 2 & 0 & -1 \\
0 & 0 & 0 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 0 & 0 & 0
\end{array}
\right)
$$
Esta es la forma escalerizada reducida de la matriz, puesto que en todas las columnas que tienen coeficiente 1 (al comienzo de cada escalón), el resto de coeficientes de esa columna son 0.
Como vemos, tenemos un total de 4 escalones. Además, tenemos la misma cantidad de escalones en la matriz del sistema, que en la matriz ampliada, de forma que ningún escalón se encuentra en la columna de los coeficientes. Si sucediera que hubieran más escalones en la matriz ampliada que en la matriz del sistema, el sistema sería incompatible.
De esta forma, sabemos que la matriz es compatible. Sin embargo, como no nos quedó una diagonal perfecta, sino que nos quedaron escalones con ancho mayor a 1, llegamos a la conclusión de que el sistema es compatible indeterminado.

A continuación veremos como se concluye a partir de esta forma.
$$
{\begin{cases}
x_{1}+2x_{2}+\frac{3}{2}x_{5}=-1 \\
x_{3}-\frac{1}{2}x_{5}=1 \\
x_{4}+2x_{5}=-1 \\
x_{6}=1
\end{cases}}
$$
Aquí podríamos hacer sustitución por atrás, pero no es necesario. En lugar de eso, expresaremos todas las variables que no son $x_{2}$ y $x_{5}$ en función de las mismas.
$$
{\begin{cases}
x_{1}=-2x_{2}-\frac{3}{2}x_{5}-1 \\
x_{3}=\frac{1}{2}x_{5}+1 \\
x_{4}=-2x_{5}-1 \\
x_{6}=1
\end{cases}}
$$
Para expresar el conjunto solución, en lugar de utilizar $x_{2}$ y $x_{5}$, llamaremos a los parámetros $\alpha$ y $\beta$.
$$
Sol(S)=\left\{  \left( -2\alpha-\frac{3}{2}\beta-1, \alpha, \frac{1}{2}\beta+1, -2\beta-1, \beta, 1 \right): \alpha,\beta \in \mathbb{R}  \right\}
$$
El proceso de escalerización y reducción separa el conjunto de incógnitas en dos conjuntos, aquellas que no tienen ninguna restricción (los parámetros, en este caso $x_{2}$ y $x_{5}$), y las que se definen a partir de los parámetros.
Este conjunto solución tiene dos grados de libertad, tiene dos parámetros, que en un conjunto $\mathbb{R}^{6}$ representa un subespacio de dimensión 2.

Algo que anticipa lo que veremos en geometría, es que podemos expresar la solución del sistema en forma paramétrica.

$$
\begin{align}
&(-1,0,1,-1,0,1)+ \\
&\alpha(-2,1,0,0,0,0)+ \\
&\beta\left( -\frac{3}{2},0, \frac{1}{2},-2,1,0 \right)
\end{align}
$$
De esta forma, se expresa la solución del sistema como la suma de tres vectores de seis componentes cada uno, siendo:
- Vector con los términos independientes (para $\alpha=\beta=0$).
- Vector con los coeficientes de $\alpha$.
- Vector con los coeficientes de $\beta$.

Es imposible representar dicha solución geométricamente, puesto que es un sistema de seis dimensiones.

Ahora veremos el teorema fundamental, que establece que toda matriz se puede escalerizar, llegando a una forma escalerizada, y reducida si queremos.

# Teorema
Toda matriz puede ser transformada en una matriz escalerizada (o escalerizada reducida) mediante una cantidad finita de transformaciones elementales.

Este teorema funciona incluso con matrices construidas al azar.
Lo que deberíamos hacer es escribir el algoritmo y demostrar que el mismo siempre termina y llega a una forma escalerizada.
En su lugar, simplemente revisaremos como funciona el algoritmo.

Este trabaja en una tabla rectangular, no importa que sea la matriz de coeficientes o la ampliada, podemos ignorar los términos independientes.
Lo que hacemos es observar las cosas dentro de una ventana corriente. La ventana corriente es un rectángulo que se encuentra contenido en el inicial, que empieza en cierta columna y fila, yendo hasta el final. El rectángulo se llama ventana corriente, y representa el trabajo que nos queda por hacer, de forma que no incluye las filas/columnas que ya fueron escalerizada.
Al principio, la ventana corriente es todo el sistema.

A continuación, el algoritmo:
1. Se observa la primera columna, para determinar el comienzo de escalón. Hay dos casos
	1. La columna es toda nula. En este caso, reduzco la ventana corriente, eliminando la primera columna.
	2. Hay al menos 1 coeficiente diferente de 0. En este caso, si no es la primera fila la que tiene dicho coeficiente diferente de 0, intercambiar la primera fila por dicha fila.
2. A cada fila del sistema, sin ser la primera, sustituirla por:
$$
\begin{align}
&\text{Para todo } i \text{ de } i_{0}+1 \text{ (segunda fila) hasta } m \text{ (última fila)} \\
&F_{i} \leftarrow F_{i}-\frac{a_{i,j_{0}}}{a_{i_{0},j_{0}}}F_{i_{0}}
\end{align}
$$
Dicho coloquialmente, a todas las filas, sin ser la primera, las sustituyo por la diferencia entre dicha fila y la primer fila de la matriz por el cociente del primer coeficiente de la fila que se va a sustituir, y el primer coeficiente de la primer fila.
Esto anula los coeficientes de toda la columna, menos en la primera fila.

3. De esta forma, tenemos un escalón, por lo que podemos reducir la ventana corriente, excluyendo la primer fila y columna.

Luego de repetir lo suficiente la operación, se obtiene la forma escalerizada de la matriz.

Para reducir la matriz a partir de su forma escalerizada, también existe un algoritmo:
1. Dividir cada fila por el valor de su primer coeficiente. De esta forma:
$$
\begin{align}
&\text{Para todo } i \text{ de } i_{0} \text{ (primera fila) hasta } m \text{ (última fila)} \\
&F_{i} \leftarrow \frac{F_{i}}{a_{i}} \qquad \text{o} \qquad F_{i} \leftarrow \frac{1}{a_{i}} F_{i}
\end{align}
$$
2. A cada fila, restarle el buen múltiplo de cada una de las siguientes filas, buscando anular el cociente de los siguientes escalones en la fila correspondiente.
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-03-16 - Clase 5 - Teorema de Rouché-Frobenius/Imágenes/Algoritmo de escalerización.png]]

## Definición
Si E es una matriz escalerizada, se llama <u>número de escalones</u> de E al número de filas no nulas.
Esta definición solo tiene sentido para las matrices escalerizadas.

El proceso de escalerización no es un proceso determinista. No es estrictamente necesario seguir un orden especifico en las operaciones, y hay varias formas de escalerizar una misma matriz.

## Proposición (admitida)
Si una matriz A tiene dos formas escalerizadas $E_{1}$ y $E_{2}$, entonces $E_{1}$ y $E_{2}$ tienen el mismo número de escalones. En función del orden en el que aplicamos las operaciones, podemos obtener una matriz resultante diferente. Sin embargo, todas las matrices escalerizadas realizadas a partir de A deben tener la misma cantidad de escalones.

Esta proposición será demostrada más adelante en el curso.
Esto nos permite enunciar el teorema fundamental, el cual enuncia que para una matriz A, todas sus formas escalerizadas tienen el mismo número de escalones, se puede definir la noción de número de escalones para cualquier matriz. Dicho "número de escalones" se llama formalmente Rango.

## Definición
El <u>rango</u> de una matriz A es el número de escalones de cualquier forma escalerizada de A.

Con esto, podemos enunciar el Teorema de Rouché-Frobenius.

# Teorema Rouché-Frobenius
Sea S un sistema lineal de m ecuaciones y n incógnitas, con matriz ampliada $(A|b)$. Sean:
- p el rango de $A$.
- p' el rango de $(A|b)$

Es decir, cuando escalerizo una matriz ampliada, tengo la matriz de coeficientes (matriz del sistema) y la columna de los términos independientes. Puedo contar la cantidad de escalones en la matriz del sistema y contar los escalones en toda la matriz. De esta forma, surgen dos casos posibles:
1. $p' = p$, en cuyo caso el sistema es compatible.
2. $p' = p+1$, en cuyo caso el sistema es incompatible.

**Observación**: o bien $p'=p$, o bien $p'=p+1$

Entonces:
1. S es compatible si y sólo si $p=p'$
2. Si S es compatible (es decir: $p=p'$)
	1. S es determinado si y sólo si $p=n$ (p = cantidad de escalones, n = cantidad de incógnitas, se forma una diagonal con los coeficientes 1).
	2. S es indeterminado si y sólo si $p < n$ (en ningún caso puede ser mayor). Algunos escalones tienen ancho > 1.

**Observación**: En el caso 2b) ($p<n$: compatible indeterminado)
Se expresan las soluciones en función de $n-p$ parámetros (se despejan p incógnitas, por lo que quedan $n-p$ que son parámetros).
Se dice que el sistema tiene $n-p$ grados de libertad. Esto sucede porque, para que el sistema sea determinado, se tendrían que agregar $n-p$ ecuaciones. Como faltan $n-p$ ecuaciones, tienen $n-p$ grados de libertad.
$$
\text{Rango (número de ecuaciones independientes) } (p) \text{ + Grado de Libertad } (n-p) \text{ = Número de Incógnitas } (n)
$$
En otro contexto, veremos este teorema en el Teorema de las Dimensiones, durante la segunda parte del curso.

Veremos que todos los problemas de Algebra Lineal se resuelven aplicando una variante de la escalerización.

Entonces, luego de escalerizar, debemos contar la cantidad de escalones en la matriz del sistema y la matriz ampliada. Si difieren, el sistema es incompatible. Si son iguales, es compatible, habiendo dos casos:
1. Si la cantidad de escalones (rango) y cantidad de incógnitas es igual, el sistema es compatible determinado.
2. Si el rango es menor que la cantidad de incógnitas, tenemos grados de libertad, y el sistema es compatible indeterminado.

Ahora, continuamos con sistemas homogéneos:

# Sistemas homogéneos
<u>Definición</u>: Se dice que un sistema S es homogéneo cuando todos sus términos independientes son nulos: $b_{i} = 0$
$$
(A|b)=\left(
\begin{array}{cccc|c}
a_{1,1} & a_{1,2} & \dots & a_{1,n} & 0 \\
a_{2,1} & a_{1,2} & \dots & a_{2,n} & 0 \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,n} & 0
\end{array}
\right)
$$
Estos sistemas tienen la particularidad de que la solución nula siempre funciona, por lo que siempre son compatibles.

**Propiedades**:
1. Un sistema homogéneo siempre es compatible: $x_{1}=x_{2}=\dots=x_{n}=0$ es solución
De esta manera, no es necesario escalerizar para saber si es compatible o no. Sin embargo, si es necesario escalerizar para encontrar otras soluciones.

2. Durante el proceso de escalerización, la última columna de la matriz ampliada (la columna de los términos independientes) siempre es nula.
En definitiva, no se necesita tenerla en cuenta.

3. En particular los rangos de $A$ y $(A|b)$ son iguales: $p = p'$.
Siempre tendremos la misma cantidad de escalones en la matriz ampliada y en la matriz del sistema, puesto que no puede haber un escalón en la columna de los términos independientes, ya que todos son nulos.

Como vemos, la única diferencia a la hora de trabajar en este tipo de sistemas, es que de antemano sabemos que es compatible y que no tenemos porque considerar la columna de los términos independientes.

## Ejemplo 11
$$
(S){\begin{cases}
x + y - z = 0 \\
x + y - 2z = 0 \\
2x + 2y - 3z = 0
\end{cases}}
$$
$$
(S)=\left(
\begin{array}{ccc|c}
1 & 1 & -1 & 0 \\
1 & 1 & -2 & 0 \\
2 & 2 & -3 & 0
\end{array}
\right)
$$
$$
(S)=\left(
\begin{array}{ccc|c}
1 & 1 & -1 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & -1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} - 2F_{1}
\end{align}
$$
$$
(S)=\left(
\begin{array}{ccc|c}
1 & 1 & -1 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
Como vemos, la última columna siempre es nula, así que podemos ignorarla.
$$
(S)=\left(
\begin{array}{ccc|c}
1 & 1 & -1 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
$$
(S)=\left(
\begin{array}{ccc|c}
1 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2}
\end{align}
$$
Llegamos a la conclusión de que el sistema es compatible (como ya sabíamos) indeterminado.
$$
(S)\Longleftrightarrow{\begin{cases}
x + y = 0 \\
z = 0 \\
\end{cases}}
$$
Utilizaremos el parámetro $y = \alpha$
$$
(S)\Longleftrightarrow{\begin{cases}
x = -y \\
z = 0 \\
\end{cases}}
$$
$$
Sol(S)=\{ (-\alpha, \alpha, 0): \alpha \in \mathbb{R} \}
$$
También lo podemos expresar en forma vectorial:
$$
\begin{align}
&(x,y,z)= \\
&(0,0,0) \\
&+\alpha(-1,1,0)
\end{align}
$$
Tenemos un espacio de dimensión 3 (pues manejamos tres incógnitas), y se grafica una recta (pues dependemos de un único parámetro). Otra cosa que podemos ver es que (0,0,0) es solución del sistema, cosa que ya sabíamos, pues se trata de un sistema homogéneo.

La próxima clase vamos a hablar de matrices, objeto matemático que actualmente utilizamos para resolver sistemas.