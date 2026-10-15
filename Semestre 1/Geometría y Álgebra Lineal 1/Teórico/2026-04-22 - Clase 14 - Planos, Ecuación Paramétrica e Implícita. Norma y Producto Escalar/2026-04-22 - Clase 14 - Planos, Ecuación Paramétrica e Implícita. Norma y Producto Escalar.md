# Rectas y planos en el espacio

Continuamos analizando la geometría en $\mathbb{R}^{3}$.

> [!Recordatorio]
> Cada recta $R \subset \mathbb{R}^{3}$ se puede representar:
> - por una ecuación vectorial
> $$
> R : X = A + \lambda u \qquad (\text{para algún } \lambda u)
> $$
> donde $A \in R$ y $u \neq \vec{0}$ es un vector director de $R$.
> Si se tienen dos puntos, se puede utilizar uno, y el otro sirve para construir el vector director (sabiendo que $B - A = \vec{AB}$).
> 
> - por una ecuación paramétrica
> $$
> R : \begin{cases}
> x_{1} = a_{1} + \lambda u_{1} \\
> x_{2} = a_{2} + \lambda u_{2} \\
> x_{3} = a_{3} + \lambda u_{3}
> \end{cases} \qquad (\text{para algún } \lambda \in \mathbb{R})
> $$
> $$
> X = (x_{1}, x_{2}, x_{3}), A = (a_{1}, a_{2}, a_{3}), u = u_{1}, u_{2}, u_{3}
> $$
> 
> - por una ecuación implícita (o cartesiana), la cual no depende de un parámetro $\lambda$
> $$
> R : \begin{cases}
> a_{1,1}x_{1} + a_{1,2}x_{2} + a_{1,3}x_{3} = b_{1} \\
> a_{2,1}x_{1} + a_{2,2}x_{2} + a_{2,3}x_{3} = b_{2}
> \end{cases}
> $$
> donde la matriz de coeficientes $\begin{pmatrix} a_{1,1} & a_{1,2} & a_{1,3} \\ a_{2,1} & a_{2,2} & a_{2,3} \end{pmatrix}$ tiene rango 2.

Ambas formas son equivalentes, y no dependen de la dimensión del espacio en el que se trabaja, con la particularidad de que se tendrán tantos componentes como dimensiones tenga el espacio.

La ecuación implícita se trata de un sistema lineal cuyas soluciones son los puntos de la recta, tiene $n - 1$ ecuaciones, siendo n las dimensiones del espacio.

Si la matriz de coeficientes no tiene rango 2:
- Si tiene rango 0: el conjunto solución no es una recta.
	La matriz de coeficientes es nula, por lo que hay dos opciones:
	1. La columna de términos independientes es nula ($b_{1} = b_{2} = 0$), por lo que la ecuación describe a todo el espacio (cualquier punto forma parte de la misma).
	2. La columna de términos independientes no es nula, por lo que el conjunto solución es vacío.

- Si tiene rango 1: el conjunto solución no es una recta.
	1. Dos filas proporcionales, incluyendo los términos independientes
	En este caso, dos filas son proporcionales (dos veces la misma ecuación). El conjunto solución tendrá dos parámetros, por lo que será un plano en lugar de una recta.
	2. Dos filas proporcionales, pero no los términos independientes.
	Aquí, el sistema es incompatible, por lo que el conjunto solución es vacío.

> [!Observación]
> 1. Una ecuación implícita es un sistema lineal $(S)$ de 2 ecuaciones y 3 incógnitas tal que
> $$
> Sol(S) = R
> $$
> Para deducir una ecuación paramétrica de R, basta con resolver el sistema (a través de Rouché-Frobenius).
> 2. Otro método para deducir una ecuación paramétrica a partir de una ecuación implícita consiste en hallar dos soluciones distintas del sistema. A partir de dichas soluciones (que son dos puntos distintos de $R$), se reconstruye fácilmente la ecuación paramétrica.
> 3. Una ecuación implícita de una recta $R$ es lo mismo que una descripción de $R$ como intersección de 2 planos no paralelos.

Este último punto hace referencia a que cada ecuación de la ecuación implícita de una recta es un plano. De esta forma, tenemos dos planos, los cuales no son paralelos, de forma que se cortan, y los puntos de corte forman una recta.


---
Luego de haber estudiado todo lo relacionado a rectas, pasaremos a los planos.

# Ecuación paramétrica del plano


> [!Definición]
> Tres puntos $A, B, C \in \mathbb{R}^{3}$ no alineados definen un plano $P$ por la ecuación vectorial:
> $$
> X = A + \lambda \vec{AB} + \mu \vec{AC} \qquad (\text{para algunos } \lambda, \mu \in \mathbb{R})
> $$

Como vemos, un plano está definido por dos parámetros, en lugar de 1.

- Si tomamos $\lambda = \mu = 0$, obtenemos $A$
- Si tomamos $\lambda = 1, \mu = 0$, obtenemos $B$
- Si tomamos $\lambda = 0, \mu = 1$, obtenemos $C$
- Para cualquier otra combinación, obtenemos otro punto del plano.

> [!Observación]
> Como $A, B, C$ no son alineados, los vectores $\vec{AB}$ y $\vec{AC}$ no son colineales.

> [!Ecuación paramétrica]
> $$
> \begin{cases}
> x_{1} = a_{1} + \lambda(b_{1} - a_{1}) + \mu(c_{1} - a_{1}) \\
> x_{2} = a_{2} + \lambda(b_{2} - a_{2}) + \mu(c_{2} - a_{2}) \\
> x_{3} = a_{3} + \lambda(b_{3} - a_{3}) + \mu(c_{3} - a_{3})
> \end{cases} \qquad (\text{para algunos } \lambda, \mu \in \mathbb{R})
> $$

Las mismas reglas respecto a las dimensiones que vimos para las rectas aplican para los planos.

Ahora, podemos hablar de vectores directores:

> [!Observación]
> Un vector director de un plano $P$ es cualquier vector $u \space (\neq \vec{0})$ de la forma $u = \vec{AB}$, donde $A, B$ son puntos distintos de $P$.

Básicamente, es cualquier vector que esté conformado por puntos del plano.

Como vemos, la noción de vector directos se define del mismo modo para la recta, sin embargo, la diferencia es que en una recta todos los vectores directores son colineales, mientras que en un plano no lo son (generalmente).

También se puede definir a un plano a partir de un punto $A$ y dos vectores $u, v$ no colineales:
$$
X = A + \lambda u + \mu v \qquad (\text{para algunos } \lambda, \mu \in \mathbb{R})
$$
$$
\begin{cases}
x_{1} = a_{1} + \lambda u_{1} + \mu v_{1} \\
x_{2} = a_{2} + \lambda u_{2} + \mu v_{2} \\
x_{3} = a_{3} + \lambda u_{3} + \mu v_{3}
\end{cases}
$$

==IMPORTANTE: La noción de vector no tiene origen, representa un desplazamiento==.

---
Ahora, pasamos a hablar de planos paralelos:

> [!Planos paralelos]
> Dos planos $P$ y $P'$ son paralelos cuando tienen los mismos vectores directores:
> $$
> dir(P) = dir(P')
> $$
> Para verificar que un plano con vectores directores no colineales $u, v \in dir(P)$ es paralelo a otro plano $P'$, basta con verificar que $u, v \in dir(P')$.

De esta forma, si tengo dos vectores directores no colineales pertenecientes al primer plano, y también son vectores directores del segundo, entonces los planos son paralelos.

> [!Observación]
> Dos planos paralelos que se encuentran en un punto son iguales.

Verificar que dos planos son paralelos con la ecuación paramétrica es algo complejo. Es más sencillo resolverlo utilizando la ecuación implícita.

---
A continuación, pasamos a estudiar la ecuación implícita del plano:

## Ecuación implícita de un plano

Primero, enunciaremos una proposición:

> [!Proposición]
> Sea $P$ un plano definido por un punto $A = (a_{1}, a_{2}, a_{3})$ y dos vectores directores no colineales $u = (u_{1}, u_{2}, u_{3})$ y $v = (v_{1}, v_{2}, v_{3})$.
> Para todo $X = (x_{1}, x_{2}, x_{3})$ tenemos las siguientes equivalencias:
> $$
> \begin{align}
> X \in P &\Longleftrightarrow \vec{AX} \text{ es combinación lineal de } u \text{ y } v \\
> &\Longleftrightarrow
> \left|
> \begin{array}{ccc}
> x_{1} - a_{1} & u_{1} & v_{1} \\
> x_{2} - a_{2} & u_{2} & v_{2} \\
> x_{3} - a_{3} & u_{3} & v_{3}
> \end{array}
> \right| = 0
> \end{align}
> $$

El primero es obvio por la paramétrica, pues es lo mismo que decir que $\vec{AX} = \lambda u + \mu v$, pero no en este caso.

En el segundo, la idea es que el determinante es nulo si y solo si la primera columna es combinación lineal de la segunda y la tercera, lo que es equivalente a decir que $\vec{AX}$ es combinación lineal de $u$ y $v$ ($X$ es un punto de $P$). Mediante el cálculo del determinante, obtenemos la ecuación implícita.

Nuevamente, la idea no es memorizar estas fórmulas, sino entender los razonamientos y ser capaz de razonarlos cuando sea necesario. Es fundamental entender los puntos de vista y como se pasa de una idea o representación a otra.

Gracias a la proposición (desarrollo del cálculo del determinante), se deduce que
$$
\begin{align}
X \in P &\Longleftrightarrow &&(x_{1} - a_{1})(u_{2}v_{3} - u_{3}v_{2}) \space - \\
&&&(x_{2} - a_{2})(u_{1}v_{3} - u_{3}v_{1}) \space + \\
&&&(x_{3} - a_{3})(u_{1}v_{2} - u_{2}v_{1}) = 0 \\ \\

&\Longleftrightarrow && \overbrace{ \alpha x_{1} + \beta x_{2} + \gamma x_{3} = \delta }^{ \text{Ecuación implícita} } \\
& \text{con } &&\alpha = (u_{2}v_{3} - u_{3}v_{2}) \\
&&&\beta = (u_{3}v_{1} - u_{1}v_{3}) \\
&&&\gamma = (u_{1}v_{2} - u_{2}v_{1}) \\ \\

&&&\delta = \det(A, u, v)
\end{align}
$$

Se puede verificar que $\alpha$, $\beta$ y $\gamma$ no pueden ser todos nulos, al menos uno tiene que ser no nulo.

Recíprocamente, toda ecuación de la forma
$$
\alpha x_{1} + \beta x_{2} + \gamma x_{3} = \delta
$$
donde $(\alpha, \beta, \gamma) \neq (0,0,0)$ define un plano.

Como vemos, ahora no tenemos parámetros ($\lambda, \mu$).
Por construcción, para comprobar si un punto pertenece o no al plano, verificamos si cumple o no la ecuación.

Para pasar de la implícita a la paramétrica, tenemos que aplicar Rouché-Frobenius a la ecuación implícita, tratándolo como un sistema con 1 ecuación y 3 incógnitas. En general será un sistema compatible indeterminado, dependiendo de 2 parámetros (siendo $u$ y $v$) y expresado como una ecuación paramétrica.

> [!Observación]
> Para deducir la ecuación paramétrica a partir de la implícita, basta con resolver el sistema (con 1 ecuación y 3 incógnitas).

Teniendo las ecuaciones implícitas, es fácil calcular la intersección de dos planos: desarrollo un sistema lineal de dos ecuaciones y resuelvo, pudiendo ser compatible indeterminado (obteniendo un plano si son iguales, o una recta), o incompatible (si son paralelos y no se cortan).

Como nos interesa lo que sucede en dimensión 3, podemos concluir que:
- Una recta se define por 3 ecuaciones con 1 parámetro, o dos ecuaciones implícitas.
- Un plano se define por 3 ecuaciones con 2 parámetros, o una ecuación implícita.

En general, para la ecuación implícita, si trabajamos en dimensión $n$:
- Una recta se define por $n - 1$ ecuaciones.
- Un plano se define por $n - 2$ ecuaciones.

Igualmente, solo trabajaremos en dimensión 3, aunque es fundamental entender que podemos trabajar con cualquier dimensión, puesto que el punto de vista actual no está dado en base a intuiciones visuales, sino por propiedades algebraicas y numéricas.

Incluso se pueden combinar elementos de diferentes dimensiones y calcular las intersecciones entre si.

---
Ahora, pasaremos a hablar sobre la norma y el producto escalar:

# Norma y producto escalar
Hasta ahora, hemos trabajado con cosas rectas. Aún no hemos hablado de dos ingredientes fundamentales: noción de distancia, y noción de ángulo.

Aquí, manejaremos a la distancia como norma, y el ángulo será utilizado indirectamente mediante el producto escalar.

Comenzamos por la norma:
## Norma

> [!Norma]
> Se define la norma $||u||$ de un vector $u \in \mathbb{R}^{3}$ por $||u|| = dist(A, B)$, donde $A, B$ son tales que $u = \vec{AB}$.

Es la longitud del mismo. Únicamente depende del vector, no de los puntos utilizados, puesto que un mismo vector puede ser formado por infinitos puntos. Es la distancia entre los dos puntos utilizados como referencia.

Luego veremos que hay fórmulas que nos permiten calcularla fácilmente.

> [!Propiedades]
> 1. $||u|| \geq 0 \text{ y } ||u|| = 0 \text{ si y solo si } u = \vec{0}$
> De esta forma, solo el vector nulo tiene norma 0.
> 
> 2. $||\lambda \cdot u|| = |\lambda| \cdot ||u||$
> Es importante extraer el factor $\lambda$ en valor absoluto, puesto que la distancia siempre es positiva.
> 
> 3. $||u + v|| \leq ||u|| + ||v||$
> Para calcular la suma de un vector, aplicamos el método del paralelogramo. Al representarlo gráficamente, notamos que la longitud de la suma es menor o igual que la longitud de las sumas separadas. Es lo único seguro sobre la suma de vectores.

A continuación, un término más bien utilizado en física, aunque relacionado con el tema.
> [!Definición]
> Un versor es un vector de norma 1.


Proseguimos con el producto escalar, el cual es un concepto más complejo:
## Producto escalar

> [!Producto escalar]
> Dados dos vectores $u, v \in \mathbb{R}^{3}$ se define el producto escalar (producto interno) por
> $$
> u \cdot v := ||u|| \cdot ||v|| \cdot \cos \theta
> $$
> donde $\theta$ es el ángulo formado por los vectores $u$ y $v$.

De esta forma, el producto escalar es un número real, pues está construido a partir de los vectores (de su distancia).
Si bien puede darse el caso en el que uno de los vectores sea nulo, donde que el ángulo no está definido, o que ambos sean nulos, esto no nos importa, ya que cuando al menos uno es nulo, el producto de su distancia es nulo, por lo que ignoramos la noción de ángulo.

> [!Observación]
> Cuando $u$ o $v$ es nulo:
> $$
> u \cdot v = 0
> $$

Cuando los vectores son no nulos, es posible calcular el ángulo, utilizando el coseno para esto. Además, como el coseno es una función par, no tiene signo, entonces da igual si tomamos el ángulo entre $u$ y $v$ o entre $v$ y $u$. Nunca usaremos el angulo directamente, siempre utilizamos $\sin$ o $\cos$ de por medio.

> [!Notaciones]
> $$
> u \cdot v = \space < u, v > \space = \space < u | v > \space
> $$

Finalizaremos viendo las propiedades del producto escalar:

> [!Propiedades]
> 1. $u \cdot v = v \cdot u$
> 2. $(\lambda \cdot u) \cdot u = u \cdot (\lambda \cdot v) = \lambda (u \cdot v)$
> 3. $(u + u') \cdot v = u \cdot v + u' \cdot v$
> 	$u \cdot (v + v') = u \cdot v + u \cdot v'$

Como vemos, podemos calcular el producto escalar usando las reglas de producto tradicionales.

Es fundamental entender los tipos manejados, por ejemplo $\lambda \cdot u$ es el producto de vector por un número (resulta en un vector), mientras que $(\lambda \cdot u) \cdot u$ es el producto escalar, y $\lambda (u \cdot v)$ es el producto de dos números.
Entendiendo los tipos manejados, entendemos los resultados obtenidos y es más fácil recordar las propiedades utilizadas y su similitud con las operaciones tradicionales.

Continuaremos viendo propiedades en las próximas clases.