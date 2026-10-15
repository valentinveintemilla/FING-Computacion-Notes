# Norma y producto escalar
Repasamos las definiciones:

## Norma

> [!Norma - Definición]
> La norma de un vector $u \in \mathbb{R}^{3}$ es el número $||u||$ definido por
> $$
> ||u|| = dist(A, B)
> $$
> donde $A, B \in \mathbb{R}^{3}$ son tales que
> $$
> \begin{align}
> u &= \vec{AB} \\
> &= B - A
> \end{align}
> $$

> [!Observación]
> La definición no depende de $A$ y $B$.
> Solo depende de que $\vec{AB} = u$

Como vemos, la norma es la distancia entre dos puntos. Es la longitud o tamaño de un vector

> [!Propiedades]
> 1. $||u|| \geq 0$ y $||u|| = 0$ si y sólo si $u = \vec{0}$ ($\vec{0}$ es el único vector con norma nula).
> 2. $||\lambda \cdot u|| = |\lambda| \cdot ||u||$
> 3. $||u + v|| \leq ||u|| + ||v||$
> En caso de que $||u + v|| = ||u|| + ||v||$, los puntos que conforman $u$ y $v$ están alineados.

También vimos lo que es un versor (terminología local):

Un versor es un vector $u$ tal que $||u|| = 1$.
Si $u \in \mathbb{R}^{3}$ tal que $u \neq \vec{0}$, entonces el vector $\frac{1}{||u||}\cdot u$ es un versor. Esto es equivalente a decir que, si "dividimos" a un vector no nulo por su norma, obtenemos un versor.

Recordemos que no definimos la división de un vector por un número, únicamente trabajamos con la multiplicación.

## Producto escalar

El producto escalar de dos vectores $u, v \in \mathbb{R}^{3}$ es un número $u \cdot v \space (<u, v>, <u | v>)$ definido por:
$$
u \cdot v = ||u|| \cdot ||v|| \cdot \cos \theta
$$
donde $\theta$ es el ángulo entre $u$ y $v$.

Para que se cumpla la definición, es importante que ningún vector sea nulo, puesto que el producto escalar también es nulo. En este caso, "vale" cualquier valor de $\theta$.

Cuando $u$ o $v$ es nulo:
$$
||u|| \cdot ||v|| \cdot \cos \theta = 0 \implies u \cdot v = 0
$$

Intuición geométrica de producto escalar:
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-05-06 - Clase 15 - Producto Escalar y Producto Vectorial/Imágenes/1 - Representación producto escalar.png]]

En base a la representación:
$$
\begin{align}
u \cdot v &= ||u|| \cdot \underbrace{ ||v|| \cdot \cos \theta }_{ ||v'|| } = ||u|| \cdot ||v'|| \\
&= ||v|| \cdot \underbrace{ ||u|| \cdot \cos \theta }_{ ||u'|| } = ||v|| \cdot ||u'||
\end{align}
$$

Lo particular aquí es que podemos intercambiar los vectores, y aunque el dibujo cambie, el resultado es el mismo. Aunque sabemos que tiene sentido, puesto que el producto es una operación conmutativa, en el dibujo no es obvio.

Sobre la nulidad del producto escalar, tenemos tres casos posibles:
1. $u = \vec{0}$
2. $v = \vec{0}$
3. $\cos \theta = 0$, $u$ y $v$ son ortogonales, forman un ángulo de $90°$.

> [!Propiedades]
> 1. $u \cdot v = v \cdot u$
> 2. $(\lambda u) \cdot v = u \cdot (\lambda v) = \lambda (u \cdot v)$
> Como vemos, el producto es conmutativo, tanto el producto escalar como su combinación con números.
> 3. $(u_{1} + u_{2}) \cdot v = u_{1} \cdot v + u_{2} \cdot v$
> $v \cdot (u_{1} + u_{2}) = v \cdot u_{1} + v \cdot u_{2}$
> En conclusión, tenemos las mismas reglas de cálculo que el producto tradicional.

Ahora, podemos definir adecuadamente cuando dos vectores son ortogonales.

> [!Vectores ortogonales - Definición]
> Dos vectores $u$ y $v$ son ortogonales cuando $u \cdot v = 0$.
> 
> De esta forma, el vector nulo es ortogonal (y al mismo tiempo colineal) a cualquier otro vector.

---
Ahora, veremos por que estas definiciones de la noción de ángulo y distancia, analizando lo que pasa en una base ortonormal.

### Expresión en una base ortonormal
Hasta ahora, habíamos asociado el espacio ambiente y $\mathbb{R}^{3}$, para lo cual utilizábamos un sistema de coordenadas, el cual explicitaremos a continuación.

> [!Base ortonormal]
> El espacio "ambiente" se ha identificado con $\mathbb{R}^{3}$ a través de un sistema de coordenadas (construido a partir de un origen y tres vectores no colineales)
> $$
> (0, \vec{i}, \vec{j}, \vec{k})
> $$
> Ahora, se supone que el sistema de coordenadas $(0, \vec{i}, \vec{j}, \vec{k})$ es ortonormal, es decir
> $$
> \begin{align}
> &1. &&||\vec{i}|| = ||\vec{j}|| = ||\vec{k}|| = 1 &&\text{(son versores)} \\
> &2. &&\vec{i} \cdot \vec{j} = \vec{i} \cdot \vec{k} = \vec{j} \cdot \vec{k} = 0 &&\text{(son ortogonales dos a dos)}
> \end{align}
> $$

> [!Propiedades]
> En una base ortonormal $(\vec{i}, \vec{j}, \vec{k})$, para todos $u = (u_{1}, u_{2}, u_{3})$ y $v = (v_{1}, v_{2}, v_{3})$, tenemos que:
> $$
> \begin{align}
> &1. &&u \cdot v = u_{1}v_{1} + u_{2}v_{2} + u_{3}v_{3} \\
> &2. &&||u|| = \sqrt{ u \cdot u } = \sqrt{ u_{1}^{2} + u_{2}^{2} + u_{3}^{2} } \\
> &&&\text{Ya que } \cos \theta = 1 \text{ en este caso, por lo que } u \cdot u = ||u|| \cdot ||u|| = ||u||^{2} \\
> &&& \text{De esta forma, también podemos definir la norma a traves del producto escalar.}
> \end{align}
> $$

A partir de ahora, trabajaremos en bases ortonormales, puesto que facilita los cálculos.

Demostramos las propiedades:

#### Demostración de 1

Por construcción:
$$
\begin{align}
&\vec{u} = u_{1} \cdot \vec{i} + u_{2} \cdot \vec{j} + u_{3} \cdot \vec{k} \\
&\vec{v} = v_{1} \cdot \vec{i} + v_{2} \cdot \vec{j} + v_{3} \cdot \vec{k}
\end{align}
$$
$$
\begin{align}
u \cdot v &= &&(u_{1} \cdot \vec{i} + u_{2} \cdot \vec{j} + u_{3} \cdot \vec{k}) \cdot (v_{1} \cdot \vec{i} + v_{2} \cdot \vec{j} + v_{3} \cdot \vec{k}) \\
&= &&u_{1}v_{1}(\overbrace{ \vec{i} \cdot \vec{i} }^{ =||i||^{2} = 1 }) + \cancel{ u_{1}v_{2}(\vec{i} \cdot \vec{j}) } + \cancel{ u_{1}v_{3}(\vec{i} \cdot \vec{k}) } \space + \\
&&&\cancel{ u_{2}v_{1}(\vec{j} \cdot \vec{i}) } + u_{2}v_{2}(\overbrace{ \vec{j} \cdot \vec{j} }^{ =||j||^{2} = 1 }) + \cancel{ u_{2}v_{3}(\vec{j} \cdot \vec{k}) } \space + \\
&&&\cancel{ u_{3}v_{1}(\vec{k} \cdot \vec{i}) } + \cancel{ u_{3}v_{2}(\vec{k} \cdot \vec{j}) } + u_{3}v_{3}(\overbrace{ \vec{k} \cdot \vec{k} }^{ =||k||^{2} = 1 }) \\
&= &&u_{1}v_{1} + u_{2}v_{2} + u_{3}v_{3}
\end{align}
$$

#### Demostración de 2
$$
\begin{align}
&u \cdot u &&= ||u|| \cdot ||u|| \cdot \cos 0 \\
&&&= ||u||^{2} \\
&\implies ||u|| &&= \sqrt{ u \cdot u }
\end{align}
$$

Aclaración, los productos escalares pueden ser negativos: si $\theta > 90° \implies \cos \theta < 0$.

Es importante entender que estas propiedades SOLO FUNCIONAN en bases ortonormales. Nosotros las utilizaremos de aquí en adelante.

> [!Moraleja]
> Cuando se consideran productos escalares, normas, distancias y ángulos, siempre se trabaja en una base ortonormal.
> En este marco:
> $$
> u \cdot v = u_{1}v_{1} + u_{2}v_{2} + u_{3}v_{3} = \begin{pmatrix}
u_{1} & u_{2} & u_{3}
\end{pmatrix} \cdot \begin{pmatrix}
v_{1} \\
v_{2} \\
v_{3}
\end{pmatrix}
> $$
> A partir del producto escalar, se deducen:
> $$
> \begin{align}
> &\text{Normas} &&||u|| = \sqrt{ u \cdot u } = \sqrt{ u_{1}^{2} + u_{2}^{2} + u_{3}^{2} } \\
> &\text{Distancias} &&AB = ||\vec{AB}|| = ||B - A|| = \sqrt{ (b_{1} - a_{1})^{2} + (b_{2} - a_{2})^{2} + (b_{3} - a_{3})^{2} } \\
> &\text{Ángulos} &&\cos \theta = \frac{u \cdot v}{||u|| \cdot ||v||} \qquad \text{donde } u, v \neq \vec{0}, \theta \text{ es el ángulo entre } u \text{ y } v
> \end{align}
> $$

Con este nuevo punto de vista geométrico, el concepto central no es la distancia ni el ángulo, sino el producto escalar, y a partir del mismo se deducen la norma de un vector, la distancia entre dos puntos, y el ángulo entre dos vectores no nulos. Además, podemos trabajar en diferentes dimensiones fácilmente, agregando o quitando entradas a la fórmula.

Incluso en física se maneja el tiempo como una cuarta dimensión, pero se agrega restando. Además, tenemos un factor de conversión para convertir distancias en segundos, el cual es la velocidad de la luz. Igualmente, esto no entra en el programa, simplemente es un dato que nos ayuda a visualizar como se manejan las dimensiones en la matemática.

---
Ahora, tenemos todas las nociones de distancia y ángulo, los ingredientes fundamentales de la geometría. Sin embargo, aun nos falta un elemento esencial:
## Producto vectorial

Antes de esto, tenemos que estudiar dos nociones:

Sea $(\vec{i}, \vec{j}, \vec{k})$ una base (ortonormal)
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-05-06 - Clase 15 - Producto Escalar y Producto Vectorial/Imágenes/2 - Representación sentido horario y antihorario.png]]

Como vemos, simplemente se intercambian los vectores $\vec{i}$ y $\vec{j}$, o se invierte $\vec{k}$. Las nociones de sentido horario y antihorario solo existen en dimensión 3.

Nosotros trabajaremos sobre bases ortonormales positivas (sentido antihorario).

Ahora podemos definir el producto vectorial:

> [!Producto vectorial - Definición]
> El producto vectorial de dos vectores $u, v \in \mathbb{R}^{3}$ es el vector $u \land v$ definido por:
> $$
> \begin{align}
> &1. &&||u \land v|| = ||u|| \cdot ||v|| \cdot \sin \theta \qquad \text{donde } \theta \text{ es el ángulo entre } u \text{ y } v \\
> &2. &&(u \land v) \cdot u = (u \land v) \cdot v = 0 \\
> &&&\text{Esto quiere decir que } u \land v \text{ es ortogonal a } u \text{ y a } v \\
> &3. &&\text{La terna } (u, v, u \land v) \text{ es positiva}
> \end{align}
> $$

Representación del producto vectorial de $u$ y $v$:
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-05-06 - Clase 15 - Producto Escalar y Producto Vectorial/Imágenes/3 - Representación de producto vectorial.png]]

De esta forma, determinamos la norma - longitud (1), dirección - recta a la que pertenece (2) y sentido (3) del vector obtenido. Es importante destacar esto último, ya que el producto vectorial es una operación que da como resultado un vector.

Además, la definición tiene sentido para vectores $u$ y $v$ no colineales, ya que en el caso de ser colineales, la norma es 0:
$$
\sin 0 = \sin \pi = 0 \implies ||u \land v|| = ||u|| \cdot ||v|| \cdot \underbrace{ \sin \theta }_{ 0 } = 0
$$

Pasaremos a estudiar las propiedades del producto vectorial

> [!Propiedades]
> $$
> \begin{align}
> &1. &&||u \land v|| \text{ es el doble del área del triángulo formado por } u \text{ y } v \\ \\
> 
> &2. &&u \land v = \vec{0} \text{ si y sólo si } u \text{ y } v \text{ son colineales} \\ \\
> 
> &3. &&\text{El producto vectorial es anticonmutativo} \\
> &&&\implies u \land v = -(v \land u) \\ \\
> 
> &4. &&(\lambda u) \land v = u \land (\lambda v) = \lambda (u \land v) \\ \\
> 
> &5. &&(u_{1} + u_{2}) \land v = (u_{1} \land v) + (u_{2} \land v) \\
> &&&u \land (v_{1} + v_{2}) = (u \land v_{1}) + (u \land v_{2}) \\ \\
> 
> &6. &&\text{"}\land\text{" no es asociativa:} \\
> &&&u \land (v \land w) \neq (u \land v) \land w \\ \\
> 
> &7. &&(u \land v) \land w + (v \land w) \land u + (w \land u) \land v = \vec{0}
> \end{align}
> $$

(2.) De esta forma:
- El producto escalar indica si dos vectores son ortogonales o no.
- El producto vectorial indica si dos vectores son colineales o no.

(3.) La anticonmutatividad es una propiedad matemática donde el intercambio de los operandos de una operación invierte el signo del resultado. Es una operación en la que importa el orden.

(4.) Es fácil integrar el producto numérico con el producto vectorial (siempre manteniendo el orden de los operandos del producto vectorial.)

(5.) Al tratarse de un producto, es una operación distributiva.

(6.) No es una operación asociativa. No tenemos derecho a quitar los paréntesis cuando tenemos un producto vectorial.

(7.) La suma en ciclo siempre da como resultado el vector nulo. Es importante que hayan tantos términos como vectores en producto vectorial.

---
Ahora, estudiaremos como se comporta el producto vectorial en una base ortonormal positiva:

### Expresión en una base ortonormal positiva

> [!Proposición]
> Si $(\vec{i}, \vec{j}, \vec{k})$ es una base ortonormal positiva, entonces para todos $u, v \in \mathbb{R}^{3}$
> $$
> u \land v = \begin{pmatrix}
> u_{2}v_{3} - u_{3}v_{2} \\
> u_{3}v_{1} - u_{1}v_{3} \\
> u_{1}v_{2} - u_{2}v_{1}
> \end{pmatrix}
> $$

La formula anterior es desarrollada en base a la matriz:
$$
\begin{pmatrix}
u_{1} & v_{1} \\
u_{2} & v_{2} \\
u_{3} & v_{3}
\end{pmatrix}
$$
La idea es que la primer coordenada del producto vectorial $u \land v$ está dada por el determinante de la matriz anterior excluyendo la primera fila. Así con cada una de las filas. Al final, lo que queda es un "ciclo", se aumenta en uno el subíndice de cada variable, a no ser que sea la última, volviendo al comienzo.

Aquí es importante entender que el producto vectorial solo existe en la dimensión 3. Se puede desarrollar el producto vectorial para dimensiones mayores, pero involucran más vectores. Por ejemplo, en dimensión 4, necesitamos tener 3 vectores para usar la fórmula del determinante, en dimensión 5 necesitamos 4 vectores, y así sucesivamente.

Daremos una idea de la demostración a continuación:
#### Demostración
$$
\begin{align}
&u = u_{1}\vec{i} + u_{2}\vec{j} + u_{3}\vec{k} \\
&v = v_{1}\vec{i} + v_{2}\vec{j} + v_{3}\vec{k}
\end{align}
$$
Además, consideramos las siguientes propiedades:
$$
\begin{align}
&\vec{i} \land \vec{i} = \vec{j} \land \vec{j} = \vec{k} \land \vec{k} = 0 \\ \\

&\vec{i} \land \vec{j} = \vec{k} &&\vec{j} \land \vec{i} = \vec{-k} \\
&\vec{j} \land \vec{k} = \vec{i} &&\vec{k} \land \vec{j} = \vec{-i} \\
&\vec{k} \land \vec{i} = \vec{j} &&\vec{i} \land \vec{k} = \vec{-j} \\
\end{align}
$$

Ahora, queda desarrollar el producto de ambos vectores, obteniendo nueve términos, y como sabemos calcular todos los pares de productos vectoriales de los vectores de bases $\vec{i}, \vec{j}, \vec{k}$, todo se simplifica y al final se obtiene la fórmula de la matriz vista al comienzo:
$$
u \land v = \begin{pmatrix}
u_{2}v_{3} - u_{3}v_{2} \\
u_{3}v_{1} - u_{1}v_{3} \\
u_{1}v_{2} - u_{2}v_{1}
\end{pmatrix}
$$


En la próxima clase, veremos todas las aplicaciones geométricas que tienen tanto el producto escalar como el producto vectorial.
