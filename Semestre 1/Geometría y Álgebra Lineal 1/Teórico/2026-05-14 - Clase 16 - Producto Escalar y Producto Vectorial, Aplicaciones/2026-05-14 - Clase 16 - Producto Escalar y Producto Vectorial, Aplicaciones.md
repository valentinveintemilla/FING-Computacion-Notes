# Producto escalar y producto vectorial
En esta oportunidad, concluiremos con los productos escalares y vectoriales, analizando sus aplicaciones.

Repasamos lo visto anteriormente:

## Producto escalar

> [!Producto escalar - Definición]
> $$
> u \cdot v \in \mathbb{R}
> $$
> $$
> \begin{align}
> &u \cdot v := ||u|| \cdot ||v|| \cdot \cos \theta \qquad (0 \leq \theta < \pi) \\
> &<u, v>
> \end{align}
> $$

![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-05-14 - Clase 16 - Producto Escalar y Producto Vectorial, Aplicaciones/Imágenes/1 - Representación producto escalar.png]]

De esta forma:
$$
u \cdot v = ||u|| \cdot \underbrace{ ||v'|| }_{ ||v|| \cdot \cos \theta }
$$

La definición anterior nos sirve para entender como se comporta el producto escalar geométricamente.

El único empleo de la fórmula es para deducir ángulos. De esta forma, podemos realizar una observación.

> [!Observación]
> $$
> u \cdot v = 0 \Longleftrightarrow u \perp v
> $$
> Podemos decir que mide el carácter ortogonal de los vectores.

En una base ortonormal:
$$
u \cdot v = u_{1}v_{1} + u_{2}v_{2} + u_{3}v_{3} = \begin{pmatrix}
u_{1} & u_{2} & u_{3}
\end{pmatrix}
\begin{pmatrix}
v_{1} \\
v_{2} \\
v_{3}
\end{pmatrix}
$$

En la práctica trabajaremos con bases ortonormales para facilitar los cálculos y evitar el uso de ángulos.

Dicha operación tiene muchas propiedades:
### Propiedades

> [!Propiedades]
> $$
> \begin{align}
> &1. &&u \cdot v = v \cdot u \\
> &2. &&(\lambda u) \cdot v = u \cdot (\lambda v) = \lambda(u \cdot v) \\
> &3. &&(u_{1} + u_{2}) \cdot v = u_{1} \cdot v + u_{2} \cdot v \\
> &4. &&u \cdot (v_{1} + v_{2}) = u \cdot v_{1} + u \cdot v_{2} \\
> &5. &&u \cdot u = ||u||^{2} \qquad (\geq 0)
> \end{align}
> $$
> En particular:
> $$
> \begin{align}
> ||u|| &= \sqrt{ u \cdot u } \\
> &=\sqrt{ u_{1}^{2} + u_{2}^{2} + u_{3}^{2} }
> \end{align}
> $$

Podemos decir que el producto escalar es un objeto que contiene a la vez la noción de distancia y de ángulo, puesto que podemos obtener ambos conociendo el valor del producto escalar y su definición. Además, se comporta de forma regular con las operaciones tradicionales.

---
## Producto vectorial

> [!Producto vectorial - Definición]
> A diferencia del producto escalar, el producto vectorial es un vector. Por lo tanto, el mismo tiene un eje, longitud y sentido.
> $$
> u \land v \in \mathbb{R}^{3}
> $$
> $$
> \begin{align}
> &||u \land v|| = ||u|| \cdot ||v|| \cdot \sin \theta \qquad (0 \leq \theta < \pi) \\ \\
> 
> &(u \land v) \perp u \text{ y } (u \land v) \perp v \\ \\
> 
> &\text{La terna } (u, v, u \land v) \text{ es positiva}
> \end{align}
> $$
> 
> En una base ortonormal positiva:
> $$
> u \land v = \begin{pmatrix}
> u_{2}v_{3} - u_{3}v_{2} \\
> u_{3}v_{1} - u_{1}v_{3} \\
> u_{1}v_{2} - u_{2}v_{1}
> \end{pmatrix} \qquad \left|
> \begin{array}{cc}
> u_{1} & v_{1} \\
> u_{2} & v_{2} \\
> u_{3} & v_{3}
> \end{array}
> \right|
> $$

Aclaración: también podemos tomar como referencia el determinante
$$
\left|
\begin{array}{cc}
i & j & k \\
u_{1} & u_{2} & u_{3} \\
v_{1} & v_{2} & v_{3}
\end{array}
\right|
$$
y desarrollarlo en base a la primera fila (para no tener elementos $i$, $j$ y $k$).

$(u \land v) \perp u \text{ y } (u \land v) \perp v \implies$ $u \land v$ es ortogonal a la vez a $u$ y a $v$, por lo tanto está en la recta, el eje ortogonal al plano definido por $u$ y $v$ (siempre y cuando no sean colineales, en cuyo caso el producto vectorial es 0).

$\text{La terna } (u, v, u \land v) \text{ es positiva} \implies$ Tienen que estar en sentido antihorario. Conviene utilizar el método de los tres dedos.

> [!Observación]
> $$
> u \land v = \vec{0} \text{ si y sólo si } u \text{ y } v \text{ son colineales}
> $$
> Podemos decir que mide el carácter colineal de dos vectores.


Esta operación también tiene propiedades:
### Propiedades

> [!Propiedades]
> $$
> \begin{align}
> &1. &&u \land v = -(v \cdot u) \\
> &2. &&(\lambda u) \land v = u \land (\lambda v) = \lambda(u \land v) \\
> &3. &&(u_{1} + u_{2}) \land v = u_{1} \land v + u_{2} \land v \\
> &4. &&u \land (v_{1} + v_{2}) = u \land v_{1} + u \land v_{2} \\
>  \\
> &&&\text{Importante: en general no es una operación asociativa} \\
> &5. &&(u \land v) \land w \neq u \land (v \land w) \\
>  \\
> &&&\text{Pero} \\
> &6. &&(u \land v) \land w + (v \land w) \land u + (w \land u) \land v = \vec{0}
> \end{align}
> $$

En la práctica, el producto vectorial sirve para construir un vector que siempre es perpendicular a dos vectores dados: se utiliza para construir vectores normales a planos.

---
Es lo que estudiaremos a continuación: aplicaciones de dichas operaciones para la resolución de problemas geométricos.
## Aplicaciones a la geometría

> [!Fórmulas para resolución de problemas]
> Los productos $u \cdot v$ y $u \land v$ permiten calcular distancias y ángulos:
> $$
> \begin{align}
> d(A, B) = ||\vec{AB}|| &= \sqrt{ \vec{AB} \cdot \vec{AB} } \\
> &= \sqrt{ (b_{1} - a_{1})^{2} + (b_{2} - a_{2})^{2} + (b_{3} - a_{3})^{2} }
> \end{align}
> $$
> $$
> \begin{align}
> &\cos \theta = \frac{u \cdot v}{||u|| \cdot ||v||} \\
> &\sin \theta = \frac{||u \land v||}{||u|| \cdot ||v||}
> \end{align}
> $$

Para entender las aplicaciones de esto último, abordaremos la noción de normal a un plano.

### Normal a un plano
En lo que sigue, se trabaja en una base ortonormal positiva (con tal de poder utilizar las fórmulas definidas anteriormente).

> [!Normal a un plano - Definición]
> Un vector $n \neq \vec{0}$ es normal a un plano $P$ cuando $n$ es ortogonal a todo vector director de $P$.
> 
> En particular, si $P$ está definido por un punto $A$ y 2 vectores directores $u, v$ no colineales:
> $$
> n \text{ es normal a } P \Longleftrightarrow n \cdot u = n \cdot v = 0
> $$

![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-05-14 - Clase 16 - Producto Escalar y Producto Vectorial, Aplicaciones/Imágenes/2 - Vector normal.png|496]]


En la práctica, simplemente hay que verificar que es ortogonal a dos vectores no colineales. De esta forma, comprobamos que es un vector normal del plano (ortogonal a cualquier vector director de dicho plano).

> [!Observación]
> 1. Todos los vectores normales de un plano son colineales entre sí.
> 2. Si $u, v$ son vectores directores no colineales de $P$, entonces el vector $u \land v$ es normal a $P$.

> [!Utilidad del vector normal]
> También se puede definir un plano $P$ por un punto y un vector normal $n$.
> Para todo $X \in \mathbb{R}^{3}$, tenemos que
> $$
> \begin{align}
> X \in P &\Longleftrightarrow \vec{AX} \perp n \\
> &\Longleftrightarrow \vec{AX} \cdot n = 0 \\
> &\Longleftrightarrow (x_{1} - a_{1})n_{1} + (x_{2} - a_{2})n_{2} + (x_{3} - a_{3})n_{3} = 0 \\
> &\Longleftrightarrow \alpha x_{1} + \beta x_{2} + \gamma x_{3} + \delta = 0 \\ \\
> 
> \text{donde } &\alpha = n_{1}, \beta = n_{2}, \gamma = n_{3} \\
> &\gamma = -A \cdot n
> \end{align}
> $$
> 
> Recíprocamente: Si $P$ tiene ecuación
> $$
> \alpha x_{1} + \beta x_{2} + \gamma x_{3} + \delta = 0
> $$
> entonces $n := (\alpha, \beta, \gamma)$ es un vector normal de $P$.

Es así que obtuvimos la ecuación implícita del plano.

De esta forma, descubrimos la principal aplicación del producto vectorial en la práctica: encontrar vectores normales a planos, conociendo dos vectores directores no colineales.

Esto también nos permite definir un plano no por un punto y dos vectores directores no colineales, sino por un punto y un vector normal. De esta forma, los vectores directores son redundantes cuando conocemos un vector normal.
Además, por la facilidad que supone determinar la ecuación implícita en base a un vector normal y a un punto, y determinar un vector normal en base a la ecuación implícita, se prefiere trabajar con vectores normales.

Esto también nos permite pasar de la ecuación paramétrica a la implícita fácilmente:
#### Paramétrica $\longrightarrow$ Implícita
$$
X = A + \lambda u + \mu v \qquad (u, v \text{ no colineales}, \lambda, \mu \in \mathbb{R})
$$
Sea $n := u \land v = (\alpha, \beta, \gamma)$
$$
\begin{align}
&\alpha x_{1} + \beta x_{2} + \gamma x_{3} + \delta = 0 \\
&\text{donde } \delta = -A \cdot n
\end{align}
$$

#### Implícita $\longrightarrow$ Paramétrica
$$
\alpha x_{1} + \beta x_{2} + \gamma x_{3} + \delta = 0
$$
Sean:
$$
\begin{align}
&n = (\alpha, \beta, \gamma) \text{ vector normal} \\
&A \text{ un punto de } P \space (\text{hallar una solución})
\end{align}
$$
Sea
$$
\begin{align}
&u := n \land (\text{cualquier vector no colineal a } n \text{ o  bien } \vec{i}, \vec{j} \text{ o } \vec{k}) \\
&v := n \land v
\end{align}
$$

De esta forma, $u$ es un vector ortogonal a $n$. Generalmente lo mejor es probar directamente con $\vec{i}$, $\vec{j}$ o $\vec{k}$.
Además, sabemos que $v \neq \vec{0}$ puesto que $u$ y $n$ son ortogonales, y será ortogonal a $u$.
Esta es la mejor situación para definir un plano: en base a dos vectores directores no colineales, y además ortogonales.

Ahora, podemos definir la ecuación paramétrica:
$$
P : X = A + \lambda u + \mu v
$$

La pregunta es: ¿Para qué se usa esto en la práctica?
Dichas operaciones son fundamentales para el desarrollo de simulaciones, por ejemplo poder entender y prever fallas en el funcionamiento de vehículos.
Además, también son muy utilizadas en los videojuegos tridimensionales, para calcular los polígonos, iluminación, etc., y en películas con el mismo fin (efectos especiales, por ejemplo).

Todo está formado por triángulos (polígonos). Cada uno de estos tiene 9 coordenadas (3 puntos). Lo que se hace (por ejemplo) para determinar la sombra del mismo es calcular el vector normal (producto vectorial) y en base al vector de luz (fuente de iluminación), se calcula el ángulo entre ambos. De esta forma:
- Si el producto escalar es positivo, no hay sombra.
- Si el producto escalar es negativo, está totalmente oscuro.
- El grado determina el nivel de luminosidad. Consideramos el siguiente coeficiente:
$$
\frac{\vec{DL} \cdot \vec{n}}{||\vec{DL}|| \cdot ||\vec{n}||}
$$
Siendo
$$
\begin{align}
&n \to \text{vector normal} \\
&D \to \text{origen de } n \\
&L \to \text{fuente de luz}
\end{align}
$$

El coeficiente anterior se multiplica por el color del cada pixel. Si es 0, el color es negro, si es positivo se multiplica, y será como máximo 1 en cada valor (recordemos que los colores se codifican como un vector de tres dimensiones: rojo, verde y azul - RGB). 
Además, también se considera la posición del pixel en el triángulo.

En el cine se utiliza el trazado de rayos.

También hay que considerar que siempre hay una "cámara", la cual está determinada por dos vectores, y un "espectador", y mediante su posición, la de la cámara y vectores que van desde el "espectador" y pasan por la "cámara" se determina la escena visible en ese momento. Dicho vector puede "chocar" con elementos opacos, o encontrarse con algunos translucidos, los cuales alteran los cálculos y permiten atravesar los vectores.

De esta forma, el color de un pixel se determina por múltiples sucesos, reflexión, refracción, luz difusa, etc.

---
A continuación, abordaremos aplicaciones de dichas operaciones para resolver problemas manuales.

### Ángulos entre rectas y planos
Angulo formado por dos rectas:
$$
\begin{align}
&R : X = A + \lambda u \\
&R' : X = A' + \lambda u'
\end{align}
$$
$$
\cos \theta = \frac{u \cdot u'}{||u|| \cdot ||u'||}
$$

Angulo formado por dos planos:
$$
\begin{align}
&P : \alpha x_{1} + \beta x_{2} + \gamma x_{3} + \delta = 0 \\
&P' : \alpha' x_{1} + \beta' x_{2} + \gamma' x_{3} + \delta' = 0
\end{align}
$$
$$
\begin{align}
\cos \theta = \frac{n \cdot n'}{||n|| \cdot ||n'||} \qquad \text{donde } &n = (\alpha, \beta, \gamma) \\
&n' = (\alpha', \beta', \gamma')
\end{align}
$$

Angulo formado por una recta y un plano:
$$
\begin{align}
&R : X = A + \lambda u \\
&P : \alpha x_{1} + \beta x_{2} + \gamma x_{3} + \delta = 0
\end{align}
$$
$$
\cos \left( \frac{\pi}{2} - \theta \right) = \frac{u \cdot n}{||u|| \cdot ||n||} \qquad \text{donde } n = (\alpha, \beta, \gamma)
$$
Equivale a $\cos \left( \frac{\pi}{2} - \theta \right)$ y no a $\cos \theta$ ya que estamos calculando el ángulo entre el vector director de la recta y el vector normal del plano (que forma $90°$ con cualquier vector director del plano). Sabemos que $\cos\left( \frac{\pi}{2} - \theta \right) = \cos\left( \theta - \frac{\pi}{2} \right)$, ya que:
$$
\cos\left( \frac{\pi}{2} - \theta \right) = \cos\left( \theta - \frac{\pi}{2} \right) = \underbrace{ \cos \frac{\pi}{2} }_{ = 0 } \cos \theta + \underbrace{ \sin \frac{\pi}{2} }_{ = 1 } \sin \theta = \sin \theta
$$
Además, sabemos que el ángulo formado por una recta y un plano siempre estará entre $0° (0)$ y $90° \left( \frac{\pi}{2} \right)$.
Todas estas intuiciones se deducen a partir de representaciones geométricas y figuras.

Distancia de un punto $Q$ a un plano $P$:
$$
dist(Q, P) = mín \{ dist(Q, X): X \in P \}
$$
Tengo:
- $P$ plano definido por un punto $A$ y un vector normal $n$
- $Q$ punto cualquiera

$$
dist(Q, P) = \frac{|\vec{AQ} \cdot \vec{n}|}{||\vec{n}||} = \frac{|\alpha a_{1} + \beta a_{2} + \gamma a_{3} + \delta|}{\sqrt{ \alpha^{2} + \beta^{2} + \gamma^{2} }}
$$
Esto funciona, ya que:
$$
P : \underbrace{ \alpha x_{1} + \beta x_{2} + \gamma x_{3} + \delta }_{ \vec{AX} \cdot \vec{n} } = 0
$$

En los apuntes se pueden encontrar el resto de fórmulas, aunque la idea no es memorizarlas, sino ser capaz de reconocer las intuiciones que las forman y así resolver los problemas que requieran dichos conocimientos.