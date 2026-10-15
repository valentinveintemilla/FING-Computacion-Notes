# 1 - Puntos y vectores
## Ejercicio 1.1
### Parte a)
Utilizando el método del paralelogramo, podemos determinar el resultado de la suma de dichos vectores.
![[Semestre 1/Geometría y Álgebra Lineal 1/Práctico/Práctico 6 - Geometría en el espacio. Rectas y planos/Imágenes/1 - Ejercicio 1.1.a.png]]

Como vemos, al realizar la suma de todos los vectores (no importa el orden en el que se realiza la suma), siempre obtenemos el vector nulo (pues finalizamos al comienzo del primer vector).

### Parte b)
Si sumamos todos menos el vector a, obtenemos lo siguiente:
![[Semestre 1/Geometría y Álgebra Lineal 1/Práctico/Práctico 6 - Geometría en el espacio. Rectas y planos/Imágenes/2 - Ejercicio 1.1.b.png]]

Como vemos, el resultado equivale al opuesto del vector $a$.

### Parte c)
![[Semestre 1/Geometría y Álgebra Lineal 1/Práctico/Práctico 6 - Geometría en el espacio. Rectas y planos/Imágenes/3 - Ejercicio 1.1.c.png]]
Aquí, en todos los casos, el vector resultado es nulo.

---
## Ejercicio 1.2

Como vemos, en base a las coordenadas, el punto $P + v$ se encuentra exactamente entre $P$ y $Q$, por lo que basta con duplicar el vector $v$, y cuando lo sumemos a $P$ obtendremos $Q$:
$$
P + v = Q - v \implies Q = P + 2v \qquad (\lambda = 2, \mu = 0)
$$
Podemos tomar la misma idea para llegar al resto de puntos:
$$
P + v = S - w \implies S = P + v + w \qquad (\lambda = 1, \mu = 1)
$$
$$
P = R + w \implies R = P - w \qquad(\lambda = 0, \mu = -1)
$$
$$
P + 3w = T + 2v \implies T = P + 3w - 2v \qquad (\lambda = 3, \mu = -2)
$$

---
# 2 - Ecuación del plano y de la recta
## Ejercicio 2.1
### Parte a)
Ecuación paramétrica:
$$
\begin{cases}
x_{1} = 1 + 2\lambda \\
x_{2} = 2 + \lambda \\
x_{3} = 5 + 3\lambda
\end{cases}
$$
Ecuación implícita:
$$
\begin{cases}
\lambda = \frac{x_{1} - 1}{2} \\
\lambda = x_{2} - 2 \\
\lambda = \frac{x_{3} - 5}{3}
\end{cases}
$$
$$
\begin{cases}
\frac{x_{1} - 1}{2} = x_{2} - 2 \\
\frac{x_{1} - 1}{2} = \frac{x_{3} - 5}{3}
\end{cases}
$$
$$
\begin{align}
&\frac{x_{1} - 1}{2} = \frac{x_{1}}{2} - \frac{1}{2} \\
&\frac{x_{3} - 5}{2} = \frac{x_{3}}{2} - \frac{5}{2}
\end{align}
$$
$$
\begin{cases}
\frac{x_{1}}{2} - \frac{1}{2} = x_{2} - 2 \implies \frac{x_{1}}{2} - x_{2} = -2 + \frac{1}{2} = -\frac{3}{2} \\
\frac{x_{1}}{2} - \frac{1}{2} = \frac{x_{3}}{2} - \frac{5}{2} \implies \frac{x_{1}}{2} - \frac{x_{3}}{2} = -\frac{5}{2} + \frac{1}{2} = -\frac{4}{2} = -2
\end{cases}
$$
Simplificamos las ecuaciones obtenidas:
$$
\begin{align}
&\frac{x_{1}}{2} - x_{2} = -\frac{3}{2} \implies x_{1} - 2x_{2} = -3 \\
&\frac{x_{1}}{2} - \frac{x_{3}}{2} = -2 \implies x_{1} - x_{3} = -4
\end{align}
$$
En conclusión, la ecuación implícita es:
$$
\begin{cases}
x_{1} - 2x_{2} = -3 \\
x_{1} - x_{3} = -4
\end{cases}
$$

### Parte b)
En este caso, usaremos el segundo punto para construir el vector director:
$$
\vec{AB} = B - A = (1 - 4, 0 - 3, 1 - 0) = (-3, -3, 1)
$$
De esta forma, utilizaremos el vector $u = (-3, -3, 1)$

Ecuación paramétrica:
$$
\begin{cases}
x_{1} = 4 - 3\lambda \\
x_{2} = 3 - 3\lambda \\
x_{3} = \lambda \\
\end{cases}
$$
$$
\begin{cases}
\lambda = \frac{x_{1} - 4}{-3} \\
\lambda = \frac{x_{2} - 3}{-3} \\
\lambda = x_{3}
\end{cases}
$$
$$
\begin{align}
&\frac{x_{1} - 4}{-3} = \frac{x_{1}}{-3} - \frac{4}{-3} = -\frac{x_{1}}{3} + \frac{4}{3} \\
&\frac{x_{2} - 3}{-3} = \frac{x_{2}}{-3} - \frac{3}{-3} = -\frac{x_{2}}{3} + 1
\end{align}
$$
$$
\begin{cases}
-\frac{x_{1}}{3} + \frac{4}{3} = -\frac{x_{2}}{3} + 1 \implies -\frac{x_{1}}{3} + \frac{x_{2}}{3} = 1 - \frac{4}{3} = -\frac{1}{3} \\
-\frac{x_{1}}{3} + \frac{4}{3} = x_{3} \implies -\frac{x_{1}}{3} -x_{3} = -\frac{4}{3}
\end{cases}
$$
Simplificamos las ecuaciones obtenidas:
$$
\begin{align}
&-\frac{x_{1}}{3} + \frac{x_{2}}{3} = -\frac{1}{3} \underbrace{ \implies }_{ \times (-3) } x_{1} - x_{2} = 1 \\
&-\frac{x_{1}}{3} -x_{3} = -\frac{4}{3} \underbrace{ \implies }_{ \times (-3) } x_{1} + 3x_{3} = 4
\end{align}
$$
En conclusión, la ecuación implícita es:
$$
\begin{cases}
x_{1} - x_{2} = 1 \\
x_{1} + 3x_{3} = 4
\end{cases}
$$

---
## Ejercicio 2.2
### Parte a)
$$
(S) = \begin{cases}
x = 1 + 2 \lambda \\
y = 2 - \lambda \\
z = -2 + \lambda
\end{cases}
$$
Primero, pasaremos a la ecuación implícita de la recta:
$$
\begin{cases}
\lambda = \frac{x - 1}{2} \\
\lambda = -y + 2 \\
\lambda = z + 2
\end{cases}
$$
$$
\begin{align}
\frac{x - 1}{2} = \frac{x}{2} - \frac{1}{2}
\end{align}
$$
$$
\begin{cases}
\frac{x}{2} - \frac{1}{2} = -y + 2 \implies \frac{x}{2} + y = 2 + \frac{1}{2} = \frac{5}{2} \\
\frac{x}{2} - \frac{1}{2} = z + 2 \implies \frac{x}{2} - z = 2 + \frac{1}{2} = \frac{5}{2}
\end{cases}
$$
Simplificamos las ecuaciones obtenidas:
$$
\begin{align}
&\frac{x}{2} + y = \frac{5}{2} \underbrace{ \implies }_{ \times 2 } x + 2y = 5 \\
&\frac{x}{2} - z = \frac{5}{2} \underbrace{ \implies }_{ \times 2 } x - 2z = 5
\end{align}
$$
En conclusión, la ecuación implícita es:
$$
\begin{cases}
x + 2y = 5 \\
x - 2z = 5
\end{cases}
$$
Ahora, podemos aplicarla para identificar si los puntos pertenecen a la recta.

$¿(3, 1, -1) \in S?$
$$
\begin{cases}
3 + 2 \times 1 = 5 \\
3 - 2 \times (-1) = 5
\end{cases}
$$
$$
\begin{align}
3 + 2 \times 1 &= 5 \\
3 + 2 &= 5 \\
5 &= 5
\end{align}
$$
$$
\begin{align}
3 - 2 \times (-1) &= 5 \\
3 + 2 &= 5 \\
5 &= 5
\end{align}
$$
Efectivamente, verificamos que $(3, 1, -1) \in S$.

$¿(5, 2, 1) \in S?$
$$
\begin{cases}
5 + 2 \times 2 = 5 \\
5 - 2 \times 1 = 5
\end{cases}
$$
$$
\begin{align}
5 + 2 \times 2 &= 5 \\
5 + 4 &= 5 \\
9 &= 5
\end{align}
$$
En este caso, $(5, 2, 1)  \not \in S$, ya que no cumple la primer ecuación, no pertenece al primer plano (no es necesario verificar la segunda).

$¿(5, 0, 0) \in S?$
$$
\begin{cases}
5 + 2 \times 0 = 5 \\
5 - 2 \times 0 = 5
\end{cases}
$$
$$
\begin{align}
5 + 2 \times 0 &= 5 \\
5 + 0 &= 5 \\
5 &= 5
\end{align}
$$
$$
\begin{align}
5 - 2 \times 0 &= 5 \\
5 - 0 &= 5 \\
5 &= 5
\end{align}
$$
Efectivamente, verificamos que $(5, 0, 0) \in S$.

Se puede resolver directamente con la ecuación paramétrica, simplemente hay que sustituir los valores de $x$, $y$ y $z$ por las coordenadas del punto y verificar que los tres $\lambda$ (puesto que son 3 ecuaciones) sean iguales.
Por ejemplo, para el punto $(3, 1, -1)$:
$$
(S) = \begin{cases}
3 = 1 + 2 \lambda \\
1 = 2 - \lambda \\
-1 = -2 + \lambda
\end{cases}
$$
$$
\begin{align}
3 &= 1 + 2 \lambda \\
3 - 1 &= 2\lambda \\
\frac{2}{2} &= \lambda \\
1 &= \lambda
\end{align}
$$
$$
\begin{align}
1 &= 2 - \lambda \\
1 - 2 &= -\lambda \\
\frac{-1}{-1} &= \lambda \\
1 &= \lambda
\end{align}
$$
$$
\begin{align}
-1 &= -2 + \lambda \\
-1 + 2 &= \lambda \\
1 &= \lambda
\end{align}
$$
De esta forma, como los tres $\lambda$ son iguales, confirmamos que $(3, 1, -1) \in S$.

### Parte b)
$$
(S) = \begin{cases}
x + y - z + 1 = 0 \implies x + y - z = -1 \\
2x - y + z + 2 = 0 \implies 2x - y + z = -2
\end{cases}
$$

$¿(-1, 0, 0) \in S?$
$$
\begin{align}
-1 + 0 - 0 &= -1 \\
-1 &= -1
\end{align}
$$
$$
\begin{align}
2 \times (-1) - 0 + 0 &= -2 \\
-2 &= -2
\end{align}
$$
Efectivamente, confirmamos que $(-1, 0, 0) \in S$.

$¿(0, 1, 1) \in S?$
$$
\begin{align}
0 + 1 - 1 &= -1 \\
0 &= -1
\end{align}
$$
Como vemos, $(0, 1, 1) \not \in S$, ya que no verifica la primera ecuación: $x + y - z = -1$

$¿(1, -1, 1) \in S?$
$$
\begin{align}
1 + (-1) - 1 &= -1 \\
-1 &= -1
\end{align}
$$
$$
\begin{align}
2 \times 1 - (-1) + 1 &= -2 \\
2 - (-1) + 1 &= -2 \\
4 &= -2
\end{align}
$$
Como vemos, $(1, -1, 1) \not \in S$, ya que no verifica la segunda ecuación: $x + y - z = -1$

### Parte c)

Para verificar si los puntos están alineados, tomaremos dos, desarrollaremos la ecuación de la recta que los contiene a ambos, y comprobaremos si el tercero pertenece a dicha recta.

Por ejemplo, trabajaremos con $A = (1, 0, 2)$ y $B = (-1, 1, 1)$:

Primero, tenemos que encontrar un vector director:
$$
u = \vec{AB} = B - A = (-1 - 1, 1 - 0, 1 - 2) = (-2, 1, -1)
$$
Ahora, podemos desarrollar la ecuación paramétrica en base a $A$ y $u$:
$$
\begin{cases}
x_{1} = 1 - 2\lambda \\
x_{2} = \lambda \\
x_{3} = 2 - \lambda
\end{cases}
$$
$$
\begin{cases}
\lambda = \frac{x_{1} - 1}{-2} \\
\lambda = x_{2} \\
\lambda = \frac{x_{3} - 2}{-1}
\end{cases}
$$
$$
\begin{align}
&\frac{x_{1} - 1}{-2} = -\frac{x_{1}}{2} + \frac{1}{2} \\
&\frac{x_{3} - 2}{-1} = -x_{3} + 2
\end{align}
$$
$$
\begin{cases}
-\frac{x_{1}}{2} + \frac{1}{2} = x_{2} \implies -\frac{x_{1}}{2} - x_{2} = -\frac{1}{2} \\
-\frac{x_{1}}{2} + \frac{1}{2} = -x_{3} + 2 \implies -\frac{x_{1}}{2} + x_{3} = 2 - \frac{1}{2} = \frac{3}{2}
\end{cases}
$$
Simplificamos las ecuaciones obtenidas:
$$
\begin{align}
&-\frac{x_{1}}{2} - x_{2} = -\frac{1}{2} \underbrace{ \implies }_{ \times (-2) } x_{1} + 2x_{2} = 1 \\
&-\frac{x_{1}}{2} + x_{3} = \frac{3}{2} \underbrace{ \implies }_{ \times (2) } -x_{1} + x_{3} = 3
\end{align}
$$
En conclusión, la ecuación implícita es:
$$
\begin{cases}
x_{1} + 2x_{2} = 1 \\
-x_{1} + x_{3} = 3
\end{cases}
$$
Ahora, podemos verificar mediante esta ecuación, si el punto $C = (3, -1, 1)$ pertenece a $S$:
$$
\begin{align}
3 + 2 \times (-1) &= 1 \\
3 - 2 &= 1 \\
1 &= 1
\end{align}
$$
$$
\begin{align}
-3 + 1 &= 3 \\
-2 &= 3
\end{align}
$$
Verificamos que $(3, -1, 1) \not \in S$, por lo que los puntos $(1, 0, 2)$, $(-1, 1, 1)$ y $(3, -1, 1)$ no son colineales.

FORMA MÁS SENCILLA DE RESOLVERLO:
Tomar los vectores $\vec{AB}$ y $\vec{AC}$, y verificar si son colineales o no.

### Parte d)
Sean $A = (1, 1, 1), B = (1, 0, -1), C = (1, 2, 3)$:
Ahora, compararemos los vectores $\vec{AB}$ y $\vec{AC}$ para ver si son colineales (si son múltiplos):
$$
\begin{align}
&\vec{AB} = B - A = (1 - 1, 0 - 1, -1 - 1) = (0, -1, -2) \\
&\vec{AC} = C - A = (1 - 1, 2 - 1, 3 - 1) = (0, 1, 2)
\end{align}
$$
Si analizamos los vectores, podemos ver que $\vec{AB} = -1 \times (\vec{AC})$
Por lo tanto, los vectores son múltiplos, confirmando que son colineales. En este caso, son opuestos.

---
## Ejercicio 2.3
### Parte a)
$$
\begin{align}
&A = (1, 1, 1) \\
&u = (2, -1, 1) \\
&v = (1, 0, -1)
\end{align}
$$

Ecuación paramétrica:
$$
\begin{cases}
x_{1} = 1 + 2\lambda + \mu \\
x_{2} = 1 - \lambda \\
x_{3} = 1 + \lambda - \mu
\end{cases}
$$

Ecuación implícita:
$$
\begin{cases}
\mu = x_{1} - 1 - 2\lambda \\
x_{2} = 1 - \lambda \\
\mu = -x_{3} + 1 + \lambda \\
\end{cases}
$$
$$
\begin{cases}
x_{1} - 1 - 2\lambda = -x_{3} + 1 + \lambda \implies x_{1} + x_{3} - 2 = 3\lambda \\
x_{2} = 1 - \lambda
\end{cases}
$$
$$
3\lambda = x_{1} + x_{3} - 2 \implies \lambda = \frac{1}{3}x_{1} + \frac{1}{3}x_{3} - \frac{2}{3}
$$
$$
\begin{cases}
\lambda = \frac{1}{3}x_{1} + \frac{1}{3}x_{3} - \frac{2}{3} \\
\lambda = -x_{2} + 1
\end{cases}
$$
$$
\frac{1}{3}x_{1} + \frac{1}{3}x_{3} - \frac{2}{3} = -x_{2} + 1 \implies \frac{1}{3}x_{1} + x_{2} + \frac{1}{3}x_{3} = \frac{5}{3}
$$

Simplificamos la expresión:
$$
\frac{1}{3}x_{1} + x_{2} + \frac{1}{3}x_{3} = \frac{5}{3} \underbrace{ \implies }_{ \times 3 } x_{1} + 3x_{2} + x_{3} = 5
$$
De esta forma, la ecuación implícita del plano correspondiente es:
$$
x_{1} + 3x_{2} + x_{3} = 5
$$

### Parte b)
$$
\begin{align}
&A = (1, 1, 1) \\
&B = (2, 2, 3) \\
&C = (1, 1, -2)
\end{align}
$$
Desarrollaremos los vectores $u = \vec{AB}$ y $v = \vec{AC}$:
$$
\begin{align}
&\vec{AB} = B - A = (2 - 1, 2 - 1, 3 - 1) = (1, 1, 2) \\
&\vec{AC} = C - A = (1 - 1, 1 - 1, -2 - 1) = (0, 0, -3)
\end{align}
$$
Es así que:
$$
\begin{align}
&A = (1, 1, 1) \\
&u = (1, 1, 2) \\
&v = (0, 0, -3)
\end{align}
$$

De esta forma, la ecuación paramétrica es:
$$
\begin{cases}
x = 1 + \lambda \\
y = 1 + \lambda \\
z = 1 + 2\lambda - 3\mu
\end{cases}
$$
$$
\begin{cases}
\lambda = x - 1 \\
\lambda = y - 1 \\
\lambda = \frac{-z + 1 - 3\mu}{2}
\end{cases}
$$
$$
\frac{-z + 1 - 3\mu}{2} = -\frac{1}{2}z + \frac{1}{2} - \frac{3}{2}\mu
$$
$$
\begin{align}
&-\frac{1}{2}z + \frac{1}{2} - \frac{3}{2}\mu = x - 1 \implies -\frac{1}{2}z - x - \frac{3}{2}\mu = -\frac{3}{2} \\
&-\frac{1}{2}z + \frac{1}{2} - \frac{3}{2}\mu = y - 1 \implies -\frac{1}{2}z - y - \frac{3}{2}\mu = -\frac{3}{2}
\end{align}
$$
Simplificamos las expresiones:
$$
\begin{align}
&-\frac{1}{2}z - x - \frac{3}{2}\mu = -\frac{3}{2} \underbrace{ \implies }_{ \times (-2) } z + 2x + 3\mu = 3 \\
&-\frac{1}{2}z - y - \frac{3}{2}\mu = -\frac{3}{2} \underbrace{ \implies }_{ \times (-2) } z + 2y + 3\mu = 3
\end{align}
$$
$$
\begin{cases}
z + 2x + 3\mu = 3 \\
z + 2y + 3\mu = 3
\end{cases}
$$
$$
\begin{align}
&z + 2x + 3\mu = 3 \implies \mu = \frac{z + 2x - 3}{-3} = -\frac{1}{3}z - \frac{2}{3}x + 1 \\
&z + 2y + 3\mu = 3 \implies \mu = \frac{z + 2y - 3}{-3} = -\frac{1}{3}z - \frac{2}{3}y + 1
\end{align}
$$

Como ambos son iguales a $\mu$, entonces tienen que ser iguales:
$$
\cancel{ -\frac{1}{3}z } - \frac{2}{3}x + \cancel{ 1 } = \cancel{ -\frac{1}{3}z } - \frac{2}{3}y + \cancel{ 1 } \implies -\frac{2}{3}x + \frac{2}{3}y = 0 \underbrace{ \implies }_{ \times -\frac{3}{2} } x - y = 0
$$

De esta forma, la ecuación implícita del plano que contiene a los puntos $(1, 1, 1)$, $(2, 2, 3)$ y $(1, 1, -2)$ es:
$$
x - y = 0
$$

### Parte c)
En teste caso, tenemos que encontrar dos puntos que pasen por la recta provista. Para esto, tenemos que resolver el sistema provisto:
$$
\begin{cases}
x + y + z = -2 \\
x - y - z = 2
\end{cases}
$$
Podemos sumar las dos ecuaciones, obteniendo:
$$
2x = 0 \implies x = 0
$$
Sabemos que todos los puntos de la recta tienen $x = 0$.

Teniendo este dato, podemos simplificar las ecuaciones:
$$
\begin{cases}
y + z = -2 \\
-y - z = 2
\end{cases}
$$
Si combinamos las dos ecuaciones, vemos que se anulan:
$$
\begin{align}
\cancel{ y } + \cancel{ z } - \cancel{ y } - \cancel{ z } &= \cancel{ -2 } + \cancel{ 2 } \\
0 &= 0
\end{align}
$$
Por esta razón, ambas ecuaciones son equivalentes, por lo que basta encontrar valores que cumplan una de ellas. Analizándolas, notamos que $y = -2 - z$ y $z = -2 - y$, por lo que podemos encontrar valores para un $z$ cualquiera, y viceversa. Por ejemplo, tomaremos $y = 0$:
$$
z = -2 - 0 = -2
$$
Así, ya tenemos el primer punto de la recta: $(0, 0, -2)$

Proseguimos tomando $z = 0$:
$$
y = -2 - 0 = -2
$$
Así, obtenemos el segundo punto: $(0, -2, 0)$

De esta manera tenemos tres puntos del plano:
$$
\begin{align}
&A = (1, 1, 1) \\
&B = (0, 0, -2) \\
&C = (0, -2, 0)
\end{align}
$$
Ahora, tomaremos los vectores $u = \vec{AB}$ y $v = \vec{AC}$ para desarrollar la fórmula correspondiente:
$$
\begin{align}
&u = \vec{AB} = B - A = (0 - 1, 0 - 1, -2 - 1) = (-1, -1, -3) \\
&v = \vec{AC} = C - A = (0 - 1, -2 - 1, 0 - 1) = (-1, -3, -1)
\end{align}
$$
Finalmente, podemos desarrollar la ecuación paramétrica:
$$
\begin{cases}
x = 1 - \lambda - \mu \\
y = 1 - \lambda - 3\mu \\
z = 1 - 3\lambda - \mu
\end{cases}
$$
Expresamos todo en función de lambda:
$$
\begin{cases}
\lambda = -x + 1 - \mu \\
\lambda = -y + 1 - 3\mu \\
\lambda = -\frac{1}{3}z + \frac{1}{3} - \frac{1}{3}\mu
\end{cases}
$$
$$
\begin{align}
&-x + \cancel{ 1 } - \mu = -y + \cancel{ 1 } - 3\mu &&\implies -x + y = -2\mu \\
&-x + 1 - \mu = -\frac{1}{3}z + \frac{1}{3} - \frac{1}{3}\mu &&\implies -x + \frac{1}{3}z + \frac{2}{3} = \frac{2}{3} \mu
\end{align}
$$
$$
\begin{align}
&-x + y = -2\mu &&\implies \frac{1}{2}x - \frac{1}{2}y = \mu \\
&-x + \frac{1}{3}z + \frac{2}{3} = \frac{2}{3} \mu &&\implies - \frac{3}{2}x + \underbrace{ \frac{3}{6}z }_{ \frac{1}{2}z } + 1 = \mu
\end{align}
$$
$$
\begin{cases}
\mu = \frac{1}{2}x - \frac{1}{2}y \\
\mu = - \frac{3}{2}x + \frac{1}{2}z + 1
\end{cases}
$$
$$
\frac{1}{2}x - \frac{1}{2}y = - \frac{3}{2}x + \frac{1}{2}z + 1 \implies \underbrace{ \frac{1}{2}x + \frac{3}{2}x }_{ 2x } - \frac{1}{2}y - \frac{1}{2}z = 1
$$


Simplificamos multiplicando por 2:
$$
2x - \frac{1}{2}y - \frac{1}{2}z = 1 \underbrace{ \implies }_{ \times 2 } 4x - y - z = 2
$$

De esta forma, la ecuación implícita equivale a:
$$
4x - y - z = 2
$$

---
## Ejercicio 2.4
### Parte a)
El sistema de ecuaciones paramétricas
$$
\begin{cases}
x = p_{1} + \lambda u_{1} + \mu v_{1} \\
y = p_{2} + \lambda u_{2} + \mu v_{2} \\
z = p_{3} + \lambda u_{3} + \mu v_{3}
\end{cases}
$$
coincide con la ecuación paramétrica de un plano. De esta forma, podemos llegar a su ecuación implícita:
$$
\begin{cases}
\lambda = \frac{x - p_{1} - \mu v_{1}}{u_{1}} \\
\lambda = \frac{y - p_{2} - \mu v_{2}}{u_{2}} \\
\lambda = \frac{z - p_{3} - \mu v_{3}}{u_{3}}
\end{cases}
$$
$$
\begin{align}
&\frac{x - p_{1} - \mu v_{1}}{u_{1}} = \frac{y - p_{2} - \mu v_{2}}{u_{2}} \\
&\frac{x - p_{1} - \mu v_{1}}{u_{1}} = \frac{z - p_{3} - \mu v_{3}}{u_{3}}
\end{align}
$$
$$
\begin{align}
&u_{2}(x - p_{1} - \mu v_{1}) = u_{1}(y - p_{2} - \mu v_{2}) \\
&u_{3}(x - p_{1} - \mu v_{1}) = u_{1}(z - p_{3} - \mu v_{3})
\end{align}
$$
$$
\begin{align}
&u_{2}x - u_{2}p_{1} - \mu u_{2}v_{1} = u_{1}y - u_{1}p_{2} - \mu u_{1}v_{2} \\
&u_{3}x - u_{3}p_{1} - \mu u_{3}v_{1} = u_{1}z - u_{1}p_{3} - \mu u_{1}v_{3}
\end{align}
$$
$$
\begin{cases}
u_{2}x - u_{2}p_{1} - \mu u_{2}v_{1} = u_{1}y - u_{1}p_{2} - \mu u_{1}v_{2} \\
u_{3}x - u_{3}p_{1} - \mu u_{3}v_{1} = u_{1}z - u_{1}p_{3} - \mu u_{1}v_{3}
\end{cases}
$$
$$
u_{2}x - u_{2}p_{1} - \mu u_{2}v_{1} = u_{1}y - u_{1}p_{2} - \mu u_{1}v_{2} \implies \underbrace{ \mu u_{2}v_{1} - \mu u_{1}v_{2} }_{ \mu (u_{2}v_{1} - u_{1}v_{2}) } = \underbrace{ u_{2}x - u_{2}p_{1} }_{ u_{2}(x - p_{1}) } - \underbrace{ u_{1}y + u_{1}p_{2} }_{ u_{1} (y - p_{2}) }
$$
$$
u_{3}x - u_{3}p_{1} - \mu u_{3}v_{1} = u_{1}z - u_{1}p_{3} - \mu u_{1}v_{3} \implies \underbrace{ \mu u_{3}v_{1} - \mu u_{1}v_{3} }_{ \mu (u_{3}v_{1} - u_{1}v_{3}) } = \underbrace{ u_{3}x - u_{3}p_{1} }_{ u_{3}(x - p_{1}) } - \underbrace{ u_{1}z + u_{1}p_{3} }_{ u_{1} (z - p_{3}) }
$$
$$
\begin{cases}
\mu (u_{2}v_{1} - u_{1}v_{2}) = u_{2}(x - p_{1}) - u_{1} (y - p_{2}) \implies \mu = \frac{u_{2}(x - p_{1}) - u_{1} (y - p_{2})}{u_{2}v_{1} - u_{1}v_{2}} \\
\mu (u_{3}v_{1} - u_{1}v_{3}) = u_{3}(x - p_{1}) - u_{1} (z - p_{3}) \implies \mu = \frac{u_{3}(x - p_{1}) - u_{1} (z - p_{3})}{u_{3}v_{1} - u_{1}v_{3}}
\end{cases}
$$
$$
\frac{u_{2}(x - p_{1}) - u_{1} (y - p_{2})}{u_{2}v_{1} - u_{1}v_{2}} = \frac{u_{3}(x - p_{1}) - u_{1} (z - p_{3})}{u_{3}v_{1} - u_{1}v_{3}}
$$
$$
(u_{3}v_{1} - u_{1}v_{3}) (u_{2}(x - p_{1}) - u_{1} (y - p_{2})) = (u_{2}v_{1} - u_{1}v_{2}) (u_{3}(x - p_{1}) - u_{1} (z - p_{3}))
$$
$$
u_{3}v_{1}u_{2}(x - p_{1}) - u_{3}v_{1} u_{1} (y - p_{2}) - u_{1}v_{3}u_{2}(x - p_{1}) + u_{1}v_{3} u_{1} (y - p_{2})
$$
$$
u_{2}v_{1} u_{3}(x - p_{1}) - u_{2}v_{1} u_{1} (z - p_{3}) - u_{1}v_{2} u_{3}(x - p_{1}) + u_{1}v_{2} u_{1} (z - p_{3})
$$
$$
\begin{align}
&\cancel{ u_{3}v_{1}u_{2}(x - p_{1}) } - u_{3}v_{1} u_{1} (y - p_{2}) - u_{1}v_{3}u_{2}(x - p_{1}) + u_{1}v_{3} u_{1} (y - p_{2}) = \\
&\cancel{ u_{2}v_{1} u_{3}(x - p_{1}) } - u_{2}v_{1} u_{1} (z - p_{3}) - u_{1}v_{2} u_{3}(x - p_{1}) + u_{1}v_{2} u_{1} (z - p_{3})
\end{align}
$$
$$
\begin{align}
&\cancel{ u_{1} }(- u_{3}v_{1} (y - p_{2}) - v_{3}u_{2}(x - p_{1}) + v_{3} u_{1} (y - p_{2})) = \\
&\cancel{ u_{1} }(- u_{2}v_{1} (z - p_{3}) - v_{2} u_{3}(x - p_{1}) + v_{2} u_{1} (z - p_{3}))
\end{align}
$$
$$
\begin{align}
&- u_{3}v_{1} (y - p_{2}) - v_{3}u_{2}(x - p_{1}) + v_{3} u_{1} (y - p_{2}) = \\
&- u_{2}v_{1} (z - p_{3}) - v_{2} u_{3}(x - p_{1}) + v_{2} u_{1} (z - p_{3})
\end{align}
$$
$$
- u_{3}v_{1} (y - p_{2}) - v_{3}u_{2}(x - p_{1}) + v_{3} u_{1} (y - p_{2}) + u_{2}v_{1} (z - p_{3}) + v_{2} u_{3}(x - p_{1}) - v_{2} u_{1} (z - p_{3}) = 0
$$
Reordenamos las operaciones y los factores:
$$
-u_{2}v_{3} (x - p_{1}) + v_{2}u_{3} (x - p_{1}) + u_{1}v_{3} (y - p_{2}) - u_{3}v_{1} (y - p_{2}) - u_{1}v_{2} (z - p_{3}) + v_{1}u_{2} (z - p_{3}) = 0
$$

Ahora, desarrollaremos el determinante (suponiendo que es 0):
$$
\left|
\begin{array}{ccc}
x - p_{1} & y - p_{2} & z - p_{3} \\
u_{1} & u_{2} & u_{3} \\
v_{1} & v_{2} & v_{3}
\end{array}
\right| = (x - p_{1})(u_{2}v_{3} - v_{2}u_{3}) - (y - p_{2})(u_{1}v_{3} - v_{1}u_{3}) + (z - p_{3})(u_{1}v_{2} - v_{1}u_{2})
$$
$$
= u_{2}v_{3} (x - p_{1}) - v_{2}u_{3} (x - p_{1}) - u_{1}v_{3} (y - p_{2}) + v_{1}u_{3}(y - p_{2}) + u_{1}v_{2} (z - p_{3}) - v_{1}u_{2} (z - p_{3}) = 0
$$

Ahora, si comparamos ambos resultados:
$$
\begin{align}
&-u_{2}v_{3} (x - p_{1}) + v_{2}u_{3} (x - p_{1}) + u_{1}v_{3} (y - p_{2}) - u_{3}v_{1} (y - p_{2}) - u_{1}v_{2} (z - p_{3}) + v_{1}u_{2} (z - p_{3}) = \\
&u_{2}v_{3} (x - p_{1}) - v_{2}u_{3} (x - p_{1}) - u_{1}v_{3} (y - p_{2}) + v_{1}u_{3}(y - p_{2}) + u_{1}v_{2} (z - p_{3}) - v_{1}u_{2} (z - p_{3})
\end{align}
$$
$$
\implies 2u_{2}v_{3} (x - p_{1}) - 2v_{2}u_{3} (x - p_{1}) - 2u_{1}v_{3} (y - p_{2}) + 2v_{1}u_{3}(y - p_{2}) + 2u_{1}v_{2} (z - p_{3}) - 2v_{1}u_{2} (z - p_{3}) = 0
$$
$$
= 2(u_{2}v_{3} (x - p_{1}) - v_{2}u_{3} (x - p_{1}) - u_{1}v_{3} (y - p_{2}) + v_{1}u_{3}(y - p_{2}) + u_{1}v_{2} (z - p_{3}) - v_{1}u_{2} (z - p_{3})) = 0
$$
De esta forma, sabemos que el sistema de ecuaciones es compatible solo en el caso en el que $u_{2}v_{3} (x - p_{1}) - v_{2}u_{3} (x - p_{1}) - u_{1}v_{3} (y - p_{2}) + v_{1}u_{3}(y - p_{2}) + u_{1}v_{2} (z - p_{3}) - v_{1}u_{2} (z - p_{3}) = 0$





