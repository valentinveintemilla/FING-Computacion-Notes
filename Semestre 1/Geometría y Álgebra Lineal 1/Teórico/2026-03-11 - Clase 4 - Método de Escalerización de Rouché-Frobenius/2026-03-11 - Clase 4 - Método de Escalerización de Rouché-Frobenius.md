# El método de escalerización de Rouché-Frobenius
La clase pasada, vimos que todo sistema lineal se puede expresar en forma de matriz ampliada:
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
Esta representación aligera las notaciones, puesto que no nos interesan los nombres de las variables.
También tenemos la matriz de los coeficientes:
$$
A=\begin{pmatrix}
a_{1,1} & a_{1,2} & \dots & a_{1,n} \\
a_{2,1} & a_{2,2} & \dots & a_{2,n} \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,n}
\end{pmatrix}
$$
Y la columna de los términos independientes:
$$
b=\begin{pmatrix}
b_{1} \\
b_{2} \\
\dots \\
b_{m}
\end{pmatrix}
$$
Se dice que una matriz está en forma escalerizada cuando:
1. Todas las filas, salvo quizá la primera, comienzan con una sucesión de ceros.
2. Cada fila que sigue una fila no nula (contiene al menos un coeficiente no nulo), tiene al principio por lo menos un cero más que la fila anterior. Cada fila que sigue una fila nula, es nula.
Se dice que la matriz está en forma reducida cuando además:
3. La primera entrada no nula de una fila es 1.
4. La columna que corresponde a la primera entrada no nula de una fila, tiene el resto de las entradas todas nulas.
Veremos que a veces nos interesa simplemente escalerizar la matriz, y otras veces nos conviene alcanzar la forma reducida.
Cada vez que tenemos una matriz, podemos expresarla en forma escalerizada. Además, si dividimos a cada fila entre su primer coeficiente no nulo, logramos expresarlo en 1, y podemos restar a cada fila las filas inferiores, con el objetivo de anular dichos coeficientes en filas superiores.
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-03-11 - Clase 4 - Método de Escalerización de Rouché-Frobenius/Imágenes/Matriz escalerizada y escalerizada reducida.png]]

Vimos que cuando se resuelve un sistema hay tres casos posibles:
- Compatible Determinado: el sistema tiene una solución única.
- Compatible Indeterminado: el sistema tiene infinitas soluciones.
- Incompatible: el sistema no tiene solución.
Volvemos a uno de los ejemplos que ya vimos.

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
Existen muchas formas de alcanzar la forma escalerizada. La vez pasada, llegamos al siguiente resultado:
$$
\left(
\begin{array}{ccc|c}
2 & 4 & 2 & -2 \\
0 & -1 & 1 & 1 \\
0 & 0 & 2 & 4
\end{array}
\right)
$$
Aquí tenemos dos formas de proseguir:
- Aplicamos "sustitución por atrás", obteniendo el valor para z con coeficiente 1, y aplicándolo a la fila dos para despejar y, y con estos dos valores despejar x de la primera fila.
- Alcanzar la forma escalerizada reducida de la matriz.
Si decidimos escalerizar hasta poder aplicar la sustitución por atrás, llegamos al siguiente sistema:
$$
(S){\begin{cases}
2x+4y+2z=-2 \\
-y+z=1 \\
2z=4
\end{cases}}
$$
Según las operaciones de la clase pasada: $Sol(S)={(-5,1,2)}$

Si elegimos el camino de la forma reducida, el resultado es el siguiente:
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -5 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 2
\end{array}
\right)
$$
Como vemos, alcanzamos una diagonal, de forma que cada fila nos expresa directamente el valor de cada incógnita: $Sol(S)={(-5,1,2)}$

Continuamos con otro ejemplo:
## Ejemplo 9
$$
(S){\begin{cases}
2x+4y+2z=-2 \\
x+y+2z=0 \\
-x+y-4z=2
\end{cases}}
$$
Lo único que cambia es la tercer fila, en lugar de tener un "-2z", tenemos un "-4z".
$$
\left(
\begin{array}{ccc|c}
2 & 4 & 2 & -2 \\
1 & 1 & 2 & 0 \\
-1 & 1 & -4 & 2
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 2 & 1 & -1 \\
1 & 1 & 2 & 0 \\
-1 & 1 & -4 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{2}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 2 & 1 & -1 \\
0 & -1 & 1 & 1 \\
0 & 3 & -3 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 2 & 1 & -1 \\
0 & -1 & 1 & 1 \\
0 & 0 & 0 & 4
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + 3F_{2}
\end{align}
$$
Como vemos, la última ecuación dice que 0=4. De esta forma, ya no necesitamos seguir escalerizando, pues llegamos a una incoherencia.
En conclusión, podemos determinar con seguridad que el sistema es incompatible.
$Sol(S)=\emptyset$

**¿Cómo se reconoce que un sistema es incompatible?**
Hay dos modos:
- Observamos si hay alguna fila con todos los coeficientes 0 y el termino independiente no nulo ($b\neq 0)$. Representa que $0 = a, a\neq 0$, cosa que no tiene sentido.
- Observar que tenemos un escalón más en la parte ampliada (columna de los términos independientes). Cuando un escalón aparece solo en la columna de los términos independientes, esto significa que el sistema es incompatible.
En este caso, podemos ver que tenemos dos escalones en la matriz de coeficientes, pero 3 si incluimos la columna de los términos independientes (en la matriz ampliada).

No intentamos reducirla, puesto que no nos va a servir de nada. Puesto que no vamos a lograr hacer desaparecer el 4 de ninguna forma, de forma que dicha fila se mantendrá intacta por siempre.

Por último, nos queda ver que pasa en el caso compatible indeterminado.
Para esto, utilizaremos otro ejemplo:

## Ejemplo 10

$$
(S){\begin{cases}
x_{1}+2x_{2}+x_{3}+x_{5}+x_{6}=1 \\
-x_{1}-2x_{2}+x_{3}+x_{4}-x_{6}=0 \\
x_{1}+2x_{2}+x_{3}+2x_{4}+5x_{5}+3x_{6}=1 \\
x_{1}+2x_{2}+x_{3}+x_{5}+3x_{6}=3 \\
x_{1}+2x_{2}+x_{3}+4x_{4}+9x_{5}+3x_{6}=-1
\end{cases}}
$$
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
$$
\left(
\begin{array}{cccccc|c}
1 & 2 & 1 & 0 & 1 & 1 & 1 \\
0 & 0 & 2 & 1 & 1 & 0 & 1 \\
0 & 0 & 0 & 2 & 4 & 2 & 0 \\
0 & 0 & 0 & 0 & 0 & 2 & 2 \\
0 & 0 & 0 & 4 & 8 & 2 & -2
\end{array}
\right)
\begin{align}
&F_{2} \rightarrow F_{2}+F_{1} \\
&F_{3} \rightarrow F_{3}-F_{1} \\
&F_{4} \rightarrow F_{4}-F_{1} \\
&F_{5} \rightarrow F_{5}-F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccccc|c}
1 & 2 & 1 & 0 & 1 & 1 & 1 \\
0 & 0 & 2 & 1 & 1 & 0 & 1 \\
0 & 0 & 0 & 2 & 4 & 2 & 0 \\
0 & 0 & 0 & 0 & 0 & 2 & 2 \\
0 & 0 & 0 & 0 & 0 & -2 & -2
\end{array}
\right)
\begin{align}
&F_{5} \rightarrow F_{5}-2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccccc|c}
1 & 2 & 1 & 0 & 1 & 1 & 1 \\
0 & 0 & 2 & 1 & 1 & 0 & 1 \\
0 & 0 & 0 & 2 & 4 & 2 & 0 \\
0 & 0 & 0 & 0 & 0 & 2 & 2 \\
0 & 0 & 0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{5} \rightarrow F_{5}-F_{4}
\end{align}
$$
Alcanzamos la forma escalerizada. La primer cosa que notamos es que la cantidad de escalones en la matriz de los coeficientes, es igual a la cantidad de escalones de la matriz ampliada, de forma que no hay escalones en la columna de los términos independientes. Esto ya nos indica que el sistema es compatible.
Además de esto, aparece una fila nula $0=0$, de forma que podemos quitar dicha fila. Esto significa que el sistema solo tiene 4 ecuaciones, comenzando con 5. Esto quiere decir que había una redundancia entre las ecuaciones que no vimos al principio. Había una que era una combinación del resto. El grado de libertad no era 5, sino que era 4, y esto lo podemos decir con seguridad, ya que alcanzamos una forma escalerizada.
¿Es posible determinar cual era la ecuación combinada? En realidad son todas y ninguna a la vez. Cualquiera de las ecuaciones se puede deducir de las demás, por lo que el grado de libertad ("cuantas ecuaciones son únicas") era limitado.

Es fácil ver que las ecuaciones que nos quedaron son independientes, ya que cualquier combinación de, por ejemplo, las ecuaciones 2, 3 y 4, nunca va a alcanzar la ecuación 1, ya que solo la 1 tiene las dos primeras columnas no nulas.

Sobre este sistema, podemos decir que el rango es 4. El rango equivale al número de escalones. Esto quiere decir que, si al principio teníamos 5 ecuaciones, había una que se podía formar en base a las 4 que tenemos actualmente. Esto es visible gracias a la escalerización, permitiéndonos ver cuantas ecuaciones tiene realmente un sistema.

Si bien sabemos que el sistema es compatible, este no es determinado, ya que los escalones no forman una diagonal "perfecta" (hay incógnitas que no se pueden despejar).

Continuamos con la reducción:
$$
\left(
\begin{array}{cccccc|c}
1 & 2 & 1 & 0 & 1 & 1 & 1 \\
0 & 0 & 1 & \frac{1}{2} & \frac{1}{2} & 0 & \frac{1}{2} \\
0 & 0 & 0 & 1 & 2 & 1 & 0 \\
0 & 0 & 0 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \rightarrow \frac{1}{2}F_{2} \\
&F_{3} \rightarrow \frac{1}{2}F_{3} \\
&F_{4} \rightarrow \frac{1}{2}F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccccc|c}
1 & 2 & 0 & -\frac{1}{2} & \frac{1}{2} & 1 & \frac{1}{2} \\
0 & 0 & 1 & \frac{1}{2} & \frac{1}{2} & 0 & \frac{1}{2} \\
0 & 0 & 0 & 1 & 2 & 1 & 0 \\
0 & 0 & 0 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \rightarrow \frac{1}{2}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccccc|c}
1 & 2 & 0 & 0 & \frac{3}{2} & \frac{3}{2} & \frac{1}{2} \\
0 & 0 & 1 & 0 & -\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
0 & 0 & 0 & 1 & 2 & 1 & 0 \\
0 & 0 & 0 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \rightarrow F_{1}+\frac{1}{2}F_{3} \\
&F_{2} \rightarrow F_{2}-\frac{1}{2}F_{3}
\end{align}
$$
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
\begin{align}
&F_{1} \rightarrow F_{1}-\frac{3}{2}F_{4} \\
&F_{2} \rightarrow F_{2}+\frac{1}{2}F_{4} \\
&F_{3} \rightarrow F_{3}-F_{4}
\end{align}
$$
De esta forma, alcanzamos la forma escalerizada reducida de la matriz. A continuación, resolvemos el problema:
$$
{\begin{cases}
x_{1}+2x_{2}+\frac{3}{2}x_{5}=-1 \\
x_{3}-\frac{1}{2}x_{5}=1 \\
x_{4}+2x_{5}=-1 \\
x_{6}=1
\end{cases}}
$$
Ahora, vamos a expresar el coeficiente 1 del comienzo de cada fila, en función del resto:
$$
{\begin{cases}
x_{1}=-2x_{2}-\frac{3}{2}x_{5}-1 \\
x_{3}=\frac{1}{2}x_{5}+1 \\
x_{4}=-2x_{5}-1 \\
x_{6}=1
\end{cases}}
$$
De esta forma, podemos ver que solo 4 de las 6 incógnitas que tienen una expresión (siendo $x_{1},x_{3},x_{4} \text{ y } x_{6}$), que se corresponden con los comienzos de escalón. Además, por la parte derecha, podemos ver que únicamente dependemos de $x_{2}, x_{5}$ y otros valores constantes. De esta manera, tenemos las incógnitas principales (las que están al comienzo de un escalón), que se expresan en función de las otras (que no corresponden a un comienzo de escalón).
En conclusión, podemos decir que las soluciones del sistema son séxtuplas (puesto que se trata de seis incógnitas), teniendo $x_{1},x_{3},x_{4} \text{ y } x_{6}$ las formas correspondientes, y pudiendo ser $x_{2} \text{ y } x_{5}$ cualquier valor.
El conjunto solución se expresa de la siguiente forma:
$$
Sol(S)=\{ \left( -2x_{2}-\frac{3}{2}x_{5}-1, x_{2}, \frac{1}{2}x_{5}+1, -2x_{5}-1, x_{5}, 1 \right): x_{2},x_{5} \in \mathbb{R}\}
$$
Como dijimos, es una séxtupla (6 componentes), que depende de dos parámetros llamados $x_{2} \text{ y } x_{5}$. Entonces, para obtener cualquier solución del sistema, le asigno dos valor cualesquiera a $x_{2} \text{ y } x_{5}$, y calculo el resto de valores en base a los mismos.
Vamos a cambiar los nombres de los parámetros, por razones estéticas:
$$
Sol(S)=\{ \left( -2\alpha-\frac{3}{2}\beta-1, \alpha, \frac{1}{2}\beta+1, -2\beta-1, \beta, 1 \right): \alpha,\beta \in \mathbb{R}\}
$$
Como tenemos dos parámetros en el sistema, de los cuales no tenemos restricción alguna (simplemente les asignamos un valor, a diferencia del resto de incógnitas, las cuales dependen de dichos parámetros), el tamaño del conjunto solución es infinito. En conclusión, el sistema es compatible indeterminado, puesto que aunque lo definamos con un conjunto por comprensión.
La única complejidad es que se trata de un sistema de 6 dimensiones (puesto que tenemos 6 variables en total, siendo dos de estos parámetros modificables), de tal manera que no lo podemos representar gráficamente.
Lo que si podemos confirmar es que, como tenemos dos grados de libertad (dos parámetros), podemos imaginar a los grados de libertad como una superficie (particularmente un plano) en dicho espacio de 6 dimensiones.
Sin embargo, también podemos verlo como una combinación de vectores. Para explicar esto, buscamos una solución para valores de $\alpha \text{ y } \beta$ determinados:
$$
\begin{align}
&\alpha=1, \beta=0 \quad (-3,1,1,-1,0,1) \\
&\alpha=0, \beta=1 \quad \left( -\frac{5}{2},0,\frac{3}{2},-3,1,1 \right) \\
&\alpha=0, \beta=0 \quad (-1,0,1,-1,0,1)
\end{align}
$$
Estos son 3 puntos en el espacio de dimensión 6. Por conjunción no son alineados. Estos tres puntos generan un plano. A continuación, desarrollamos la solución general del sistema:
$$
\begin{align}
&(-1,0,1,-1,0,1) \\
&+ \alpha(-2,1,0,0,0,0) \\
&+ \beta\left( -\frac{3}{2},0,\frac{1}{2},-2,1,0 \right)
\end{align}
$$
La combinación de vectores anterior da como resultado la solución general. Los vectores se combinan componente por componente. Por ejemplo, para valores determinados de $\alpha \text{ y } \beta$, simplemente multiplicamos cada uno por los componentes de su vector correspondiente, y luego sumamos los tres vectores componente por componente (1er componente de vector 1 + 1er componente de vector 2 + 1er componente de vector 3, 2do componente de vector 1 + 2do componente de vector 2...). Es otra escritura para el conjunto solución, sumando un punto para el cual pasa el plano (solución particular, que en este caso es resultado de aplicar la formula para $\alpha = 0 \text{ y } \beta = 0$) y dos vectores directores, dando como resultado un plano. Cualquier combinación de los elementos anteriores (punto + vector multiplicado por cualquier valor de $\alpha \in \mathbb{R}$ + vector multiplicado por cualquier valor de $\beta \in \mathbb{R}$).
$$
\left\{ (-1,0,1,-1,0,1) + \alpha(-2,1,0,0,0,0) + \beta\left( -\frac{3}{2},0,\frac{1}{2},-2,1,0 \right):\alpha, \beta \in \mathbb{R} \right\}
$$