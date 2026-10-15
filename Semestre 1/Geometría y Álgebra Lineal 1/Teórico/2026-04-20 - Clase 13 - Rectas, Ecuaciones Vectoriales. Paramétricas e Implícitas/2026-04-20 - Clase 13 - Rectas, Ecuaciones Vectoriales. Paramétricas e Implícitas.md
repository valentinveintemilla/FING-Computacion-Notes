Continuamos con los problemas geométricos.

# El espacio $R^{3}$

Vimos que se puede hacer geometría en un espacio de $n$ dimensiones. Sin embargo, únicamente podemos trabajar gráficamente en un espacio de como máximo tres dimensiones ($\mathbb{R}^{3}$).

En este caso, trabajaremos con una idealización del espacio físico: $\mathbb{R}^{3}$. De esta manera, manejaremos un sistema de coordenadas.

En este marco, podemos trabajar tanto con puntos como con vectores, que se representan matemáticamente de forma idéntica, aunque son conceptualmente distintos:
$$
A \in \mathbb{R}^{3}, u \in \mathbb{R}^{3}
$$
Además, tenemos diferentes operaciones:
$$
\begin{align}
&u + v, u - v \qquad \text{paralelogramo} \\
&\vec{0} \\
&\lambda \cdot \vec{u} \\
&A + u \qquad \text{da como resultado un punto} \\
&B - A = \vec{AB}
\end{align}
$$
Estas son las únicas operaciones que tienen un sentido geométrico, es decir, no hacen referencia al origen.

---
# Vectores colineales y puntos alineados

> [!Vectores colineales]
> Dos vectores $u, v \in \mathbb{R}^{3}$ son colineales cuando existe $\lambda \in \mathbb{R}$ tal que
> $$
> u = \lambda \cdot v \qquad \text{o} \qquad v = \lambda \cdot u
> $$

> [!Observación]
> El $\ll \text{o} \gg$ está para tener en cuenta el caso en el que uno de los vectores es nulo:
> - Si $u = \vec{0}$ y $v \neq \vec{0}$:
> $$
> u = 0 \cdot v \qquad \text{pero} \qquad v \neq \lambda \cdot u \space (\forall \lambda)
> $$
> - Si $u \neq \vec{0}$ y $v = \vec{0}$:
> $$
> v = 0 \cdot u \qquad \text{pero} \qquad u \neq \lambda \cdot v \space (\forall \lambda)
> $$
> - Si $u, v \neq \vec{0}$:
> $$
> v = \lambda \cdot u \Longleftrightarrow u = \lambda^{-1} \cdot v \space (\text{pues } \lambda \neq 0)
> $$

Por esta razón, si no sabemos nada de los vectores, tiene que funcionar al menos en una de las dos direcciones posibles.

Sin embargo, cuando ambos son no nulos, podemos elegir la dirección que queremos, no hay ningún problema.

Por definición, $\vec{0}$ es colineal a todos los vectores.

![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-04-20 - Clase 13 - Rectas, Ecuaciones Vectoriales. Paramétricas e Implícitas/Imágenes/1 - Vectores colineales.png]]

Ahora, pasaremos a definir la noción de puntos alineados:

> [!Puntos alineados]
> Tres puntos $A, B, C$ son alineados cuando $\vec{AB}$ y $\vec{AC}$ son colineales.

> [!Observación]
> $A, B, C$ alineados
> $$
> \begin{align}
> &\Longleftrightarrow \vec{AB} \text{ y } \vec{AC} \text{ colineales} \\
> &\Longleftrightarrow \vec{BA} \text{ y } \vec{BC} \text{ colineales} \\
> &\Longleftrightarrow \vec{CA} \text{ y } \vec{CB} \text{ colineales}
> \end{align}
> $$

De esta forma, la relación colineal es simétrica, si $u$ es colineal a $v$, entonces $v$ es colineal a $u$, pero la relación ser alineados no depende del orden de los puntos $A$, $B$ y $C$. De esta forma, si $\vec{AB}$ y $\vec{AC}$ son colineales, entonces $\vec{BA}$ y $\vec{BC}$ también lo son, y lo mismo para $\vec{CA}$ y $\vec{CB}$.
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-04-20 - Clase 13 - Rectas, Ecuaciones Vectoriales. Paramétricas e Implícitas/Imágenes/2 - Puntos alineados.png]]

Como vemos, esta noción no tiene en cuenta el orden.

---
Ahora, podemos definir lo que es una recta:

# Recta

> [!Recta]
> Dados dos puntos $A, B \in \mathbb{R}^{3}$ tales que $A \neq B$, la recta $R$ que pasa por $A$ y $B$ es el conjunto de los puntos $X$ tales que $A$, $B$ y $X$ son alineados.
> $$
> X \in R \Longleftrightarrow \vec{AX} \text{ y } \vec{AB} \text{ son colineales}
> $$

Es importante que $A$ y $B$ sean distintos, puesto que si son iguales (el mismo punto), cualquier punto $X$ estará alineado, por lo que $\vec{AB}$ es nulo, siendo colineal a cualquier vector.

## Ecuación vectorial

> [!Ecuación vectorial]
> Se puede demostrar que
> $$
> X \in R \Longleftrightarrow \underbrace{ X = A + \lambda(\overbrace{ B - A }^{ \vec{AB} }) }_{ \text{Ecuación vectorial de la recta } R } \qquad \text{para algún } \lambda \in R
> $$

Esto es correcto, ya que $A + \lambda(B - A)$ representa una traslación del punto $A$ a otro punto, considerando un múltiplo del vector $\vec{AB}$ (el cual no es nulo). Por esta razón, $\vec{AX}$ es necesariamente múltiplo de $\vec{AB}$ (cuando son colineales).
$$
X = A + \lambda(B - A) \implies X - A = \lambda(B - A)
$$
Es importante establecer que $X = A \lambda (B - A)$ es una ==ecuación vectorial de la recta $R$==. Todos los puntos de la recta son de esta forma. Es importante entender que no es única, puesto que podemos cambiar los puntos $A$ y $B$ por otros puntos diferentes, obteniendo otra ecuación vectorial de la misma recta.

Además, esta ecuación vale para cualquier espacio de cualquier dimensión. ==No hay una forma específica dada según la dimensión en la que se trabaje==.

Es una ecuación paramétrica, siendo $\lambda$ el parámetro. De esta forma, podemos considerar a $A$ como el origen y $B$ como la unidad, pudiendo encontrar cualquier punto a partir de estos dos:
![[Semestre 1/Geometría y Álgebra Lineal 1/Teórico/2026-04-20 - Clase 13 - Rectas, Ecuaciones Vectoriales. Paramétricas e Implícitas/Imágenes/3 - Recta.png]]

## Ecuación paramétrica

> [!Ecuación paramétrica]
> Escribiendo $A = (a_{1}, a_{2}, a_{3})$, $B = (b_{1}, b_{2}, b_{3})$ y $X = (x_{1}, x_{2}, x_{3})$, tenemos que
> $$
> \underbrace{ (x_{1}, x_{2}, x_{3}) \in R \Longleftrightarrow \begin{cases}
> x_{1} = a_{1} + \lambda (b_{1} - a_{1}) \\
> x_{2} = a_{2} + \lambda (b_{2} - a_{2}) \\
> x_{3} = a_{3} + \lambda (b_{3} - a_{3})
> \end{cases} }_{ \text{Ecuación paramétrica de la recta } R } \qquad \text{para algún } \lambda \in \mathbb{R}
> $$

Esto es un sistema lineal, cuya variable (en general) es $\lambda$, valor que queremos hallar.
De esta forma, es un sistema de tres ecuaciones, con ==$\lambda$ como única incógnita==.

En conclusión, ==el punto $(x_{1}, x_{2}, x_{3})$ pertenece a la recta, si y solo si el sistema es compatible determinado== (si existe un $\lambda$ que cumpla las tres ecuaciones). ==En caso de ser incompatible, el punto no pertenece a la recta==.

==Esta es la ecuación paramétrica de la recta $R$== (aunque no sea una ecuación, sino un sistema de tres ecuaciones). Esta tampoco es única, puesto que podemos tomar como referencia otros puntos, obteniendo una ecuación paramétrica diferente.

A diferencia de la ecuación vectorial, la ecuación paramétrica sí depende de las dimensiones del espacio. En este caso, ==la cantidad de ecuaciones del sistema lineal a resolver estará dado por las dimensiones del espacio en el que se trabaje==.

---
### Vector director

> [!Vector director]
> Un vector director de una recta $R$ es cualquier vector $u$ de la forma
> $$
> u = \vec{AB} \space (= B - A)
> $$
> donde $A, B \in R, A \neq B$.

De esta forma, una recta tiene infinitos vectores directores, los cuales son colineales entre si.
Es así que un vector colineal a un vector director, es otro vector director, salvo cuando $\lambda = 0$, puesto que un vector director no puede ser nulo.

> [!Observación]
> 1. Un vector director nunca es nulo.
> 2. Todos los vectores directores de una misma recta son colineales entre si.
> 3. Si $u$ es un vector director de $R$, entonces $\lambda \cdot u$ es un vector director de $R$ para todo $\lambda \neq 0$.

Ninguno de estos puntos depende de la dimensión, aplican a todos los espacios, sin importar la dimensión del mismo.

> [!Observación]
> Una recta también se puede definir a partir de un punto $A$ y de un vector $u \neq 0$.
> Obtenemos su ==ecuación vectorial==:
> $$
> X = A + \lambda \cdot u \qquad \text{para algún } \lambda \in \mathbb{R}
> $$
> Y su ==ecuación paramétrica==:
> $$
> \begin{cases}
> x_{1} = a_{1} + \lambda u_{1} \\
> x_{2} = a_{2} + \lambda u_{2} \\
> x_{3} = a_{3} + \lambda u_{3}
> \end{cases} \qquad \text{para algún } \lambda \in \mathbb{R}
> $$

Este método para definir una recta es algo más sencillo.

Además, es sencillo pasar de una definición a la otra (definición por dos puntos y definición por un punto y un vector):
- Si tengo una recta definida por dos puntos $A$ y $B$, elijo como vector a $B - A = \vec{AB}$.
- Si tengo una recta definida por un punto $A$ y un vector $u$, tomo como punto $B$ a $A + u$ (corresponde a $\lambda = 1$).

### Rectas paralelas

> [!Rectas paralelas]
> Dos rectas son paralelas cuando tienen los mismos vectores directores.

> [!Observación]
> 1. $$
> \begin{align}
> R // R' &\Longleftrightarrow dir(R) = dir(R') \\
> &\Longleftrightarrow dir(R) \cap dir(R') \neq \emptyset
> \end{align}
> $$
> 2. Dos rectas paralelas que se encuentran en un puntos son iguales.


$dir(R)$ es el conjunto de los vectores directores de la recta $R$. Igualmente, basta con verificar que hay un vector director común, pues todos los múltiplos de ese vector estarán en ambos conjuntos, por lo que los conjuntos son equivalentes.

Si tienen un punto común y un mismo vector director, van a tener la misma ecuación vectorial por lo que serán la misma recta.

---
Ahora, veremos un ejemplo asociado a los conceptos abordados hasta ahora:

#### Ejemplo 1
Determinar ecuación vectorial y paramétrica para:

1. $A = (1, 1, 1), B = (3, 5, -5)$
Ecuación vectorial:
$$
\begin{align}
&X = (1, 1, 1) + \lambda (2, 4, -6) \qquad (\text{para algún } \lambda) \\
&X = (1, 1, 1) + \lambda (1, 2, -3)
\end{align}
$$
Lo ideal es encontrar un vector director que sea "mínimo", si es posible dividirlo por algún valor con tal de simplificar las operaciones, es lo mejor.

Ecuación paramétrica:
$$
\begin{cases}
x_{1} = 1 + \lambda \\
x_{2} = 1 + 2 \lambda \\
x_{3} = 1 - 3 \lambda
\end{cases} \qquad (\text{para algún } \lambda)
$$
Como vectores directos, podemos tomar cualquier múltiplo de los anteriores:
$$
\begin{align}
&(2, 4, -6) \\
&(1, 2, -3) \\
&(-1, -2, 3) \\
&\text{etc} \dots
\end{align}
$$

Ahora, queremos determinar si un punto pertenece a la recta o no:
2. $C = (0, -1, 4), D = (1, 4, -3) \qquad ¿ C, D \in R ?$

Comenzamos por $C$: $¿C \in R?$
$$
\begin{cases}
0 = 1 + \lambda \\
-1 = 1 + 2 \lambda \\
4 = 1 - 3 \lambda
\end{cases} \implies \begin{cases}
\lambda = -1 \\
2\lambda = -2 \implies \lambda = -1 \\
-3\lambda = 3 \implies \lambda = -1
\end{cases}
$$
$$
Sol(S) = \{ -1 \}
$$
En conclusión: $C \in R$

Como tenemos una única solución (sistema compatible determinado), el punto pertenece a $R$. 

Seguimos con $D$: $¿D \in R?$
$$
\begin{cases}
1 = 1 + \lambda \\
4 = 1 + 2 \lambda \\
-3 = 1 - 3 \lambda
\end{cases} \implies \begin{cases}
\lambda = 0 \\
2\lambda = 3 \implies \lambda = \frac{3}{2}
\end{cases}
$$
$$
Sol(S) = \emptyset
$$
En conclusión: $D \not \in R$

Solo hay dos posibilidades cuando queremos saber si un punto pertenece a una recta:
- Sistema compatible determinado: $\lambda$ tiene el mismo valor en todas las ecuaciones, obtenemos el valor de $\lambda$ correspondiente a ese punto.
- Sistema incompatible: obtenemos una incoherencia, el punto no pertenece a la recta

---
Pasaremos a estudiar la ecuación implícita de la recta.

La representación anterior es "poco práctica", puesto que es algo extensa. Por esta razón, estudiaremos un tipo de ecuación que es más sencilla y acotada.

## Ecuación implícita de la recta

> [!Ecuación implícita de la recta]
> Sea $R$ una recta definida por un punto $A$ y un vector director $u \neq \vec{0}$.
> 
> Para determinar si un punto $X = (x_{1}, x_{2}, x_{3})$ pertenece a $R$ o no, tenemos que determinar si el sistema
> $$
> \begin{cases}
> x_{1} = a_{1} + \lambda u_{1} \\
> x_{2} = a_{2} + \lambda u_{2} \\
> x_{3} = a_{3} + \lambda u_{3}
> \end{cases} \qquad \text{es compatible } (\text{en } \lambda)
> $$
> con matriz ampliada:
> $$
> \left(
> \begin{array}{c|c}
> u_{1} & x_{1} - a_{1} \\
> u_{2} & x_{2} - a_{2} \\
> u_{3} & x_{3} - a_{3}
> \end{array}
> \right)
> $$

De esta forma, buscamos obtener un método que permita extraer el parámetro $\lambda$, con tal de reducir la cantidad de operaciones. Es así que queremos buscar una representación que no incluya a $\lambda$.

Se distinguen 3 casos:
1. $u_{1}, u_{2}, u_{3} \neq 0$
$$
\begin{cases}
\lambda = \frac{x_{1} - a_{1}}{u_{1}} \\
\lambda = \frac{x_{2} - a_{2}}{u_{2}} \\
\lambda = \frac{x_{3} - a_{3}}{u_{3}}
\end{cases}
$$
De esta forma, $\lambda$ existe si y solo si
$$
\overbrace{ \begin{cases}
\frac{x_{1} - a_{1}}{u_{1}} = \frac{x_{2} - a_{2}}{u_{2}} \\
\frac{x_{1} - a_{1}}{u_{1}} = \frac{x_{3} - a_{3}}{u_{3}}
\end{cases} }^{ \text{Ecuación implícita de } R }
$$
De esta forma, de forma recíproca, los 3 números son iguales.

Es así que un punto pertenece a $R$ si y solo si las 2 ecuaciones anteriores se cumplen.

Poniendo el sistema anterior en forma lineal, se obtiene:
$$
\begin{cases}
\frac{1}{u_{1}} x_{1} - \frac{1}{u_{2}} x_{2} = \frac{a_{1}}{u_{1}} - \frac{a_{2}}{u_{2}} \\
\frac{1}{u_{1}} x_{1} - \frac{1}{u_{3}} x_{3} = \frac{a_{1}}{u_{1}} - \frac{a_{3}}{x_{3}}
\end{cases} \qquad \text{sistema lineal de 2 ecuaciones y 3 incógnitas } (x_{1}, x_{2}, x_{3})
$$
De esta forma, las soluciones son los puntos de la recta, compuestos por $(x_{1}, x_{2}, x_{3})$.
Podemos concluir estableciendo que un punto $(x_{1}, x_{2}, x_{3})$ resuelve el sistema lineal si y solo si existe un $\lambda$ correspondiente.

Por construcción: $Sol(S) = R$

No es necesario memorizar la fórmula, pero si entender el método de como se alcanza la misma y en que casos se puede expresar de esta forma (cuando $u_{1}, u_{2}, u_{3} \neq 0$).

2. $u_{1}, u_{2} \neq 0$, pero $u_{3} = 0$
$$
\begin{cases}
x_{1} = a_{1} + \lambda u_{1} \\
x_{2} = a_{2} + \lambda u_{2} \\
x_{3} = a_{3}
\end{cases} \qquad (\text{para algún } \lambda)
$$
De esta forma, obtenemos una expresión menos de $\lambda$:
$$
\begin{cases}
\lambda = \frac{x_{1} - a_{1}}{u_{1}} \\
\lambda = \frac{x_{2} - a_{2}}{u_{2}}
\end{cases}
$$
En base a las anteriores, y la tercera ecuación, desarrollamos la ecuación implícita:
$$
\begin{cases}
\frac{x_{1} - a_{1}}{u_{1}} = \frac{x_{2} - a_{2}}{u_{2}} \\
x_{3} = a_{3}
\end{cases}
$$
$$
Sol(S) = R
$$
Ahora, tenemos un sistema lineal con dos ecuaciones y tres incógnitas. De esta forma, para que un punto pertenezca a la recta, tiene que cumplirse la igualdad de los $\lambda$, además de la tercera ecuación (que es una constante). Indirectamente, se cumplen las tres ecuaciones iniciales.

En el caso de que otra variable sea nula en lugar de $u_{3}$, simplemente se simplifica otra ecuación que no es la tercera. En general, este caso aplica para 1 variable nula y 2 no nulas.

3. $u_{1} \neq 0$, pero $u_{2} = u_{3} = 0$
$$
\begin{cases}
x_{1} = a_{1} + \lambda u_{1} \\
x_{2} = a_{2} \\
x_{3} = a_{3}
\end{cases}
$$
$$
\implies (S) : \begin{cases}
x_{2} = a_{2} \\
x_{3} = a_{3}
\end{cases}
$$
Así, tenemos un sistema lineal con dos ecuaciones y tres incógnitas, pero $x_{1}$ es implícita. De esta forma, sabemos que si el sistema simplificado se cumple, solo necesito tomar $\lambda = \frac{x_{1} - a_{1}}{u_{1}}$ para obtenerlo, por lo que $x_{1}$ puede ser cualquier valor.

Es válido tener hasta 1 incógnita ausente, puesto que si tenemos todas las demás fijas, sin importar el valor de la faltante, el punto pertenecerá a la recta.

En conclusión, nuevamente:
$$
\begin{align}
Sol(S) &= R \\
&= \{ (x_{1}, a_{2}, a_{3}) : x_{1} \in \mathbb{R} \}
\end{align}
$$


La conclusión de todo esto, es que cada recta tiene una ecuación paramétrica (sistema con 3 ecuaciones y 1 incógnita: $\lambda$) y puede transformarse a una ecuación implícita (sistema de 2 ecuaciones y 3 incógnitas: las coordenadas del punto), y viceversa.

Es fundamental entender que la ecuación implícita es un sistema lineal de 2 ecuaciones y 3 incógnitas, cuyo conjunto solución es exactamente la recta, sin contener el parámetro $\lambda$.

De esta forma:
$$
\begin{align}
X \in R &\Longleftrightarrow X \text{ cumple } (S) \\
&\Longleftrightarrow X \in Sol(S)
\end{align}
$$

No existe el caso donde las cuatro variables son nulas, ya que un vector director no puede ser nulo.

---
En base a lo anterior, podemos enunciar un teorema:

> [!Proposición]
> Toda recta tiene una ecuación implícita (o cartesiana)
> $$
> (S)\begin{cases}
> a_{1,1}x_{1} + a_{1,2}x_{2} + a_{1,3}x_{3} = b_{1} \\
> a_{2,1}x_{1} + a_{2,2}x_{2} + a_{2,3}x_{3} = b_{2}
> \end{cases}
> $$
> es decir: un sistema tal que $Sol(S) = R$

Para toda recta, siempre existen dos ecuaciones lineales cuyo conjunto solución me da exactamente la recta.
De esta manera, para verificar que un punto está en la recta, hay que verificar que las coordenadas del mismo sean solución.

### Ejemplo 1 - Continuación
Encontrar la ecuación cartesiana (o implícita), para $A = (1, 1, 1), B = (1, 2, -3)$:
$$
\begin{cases}
x_{1} = 1 + \lambda \\
x_{2} = 1 + 2 \lambda \\
x_{3} = 1 - 3 \lambda
\end{cases} \implies \begin{cases}
\lambda = x_{1} - 1 \\
\lambda = \frac{x_{2} - 1}{2} \\
\lambda = \frac{1 - x_{3}}{3}
\end{cases}
$$
$$
\begin{cases}
x_{1} - 1 = \frac{x_{2} - 1}{2} \\
x_{1} - 1 = \frac{1 - x_{3}}{3}
\end{cases}
$$
Simplificamos para obtener la buena forma:
$$
\begin{cases}
x_{1} - \frac{x_{2}}{2} = \frac{1}{2} \\
x_{1} + \frac{x_{3}}{3} = \frac{4}{3}
\end{cases} \implies \begin{cases}
2x_{1} - x_{2} = 1 \\
3x_{1} + x_{3} = 4
\end{cases}
$$
Por construcción: $Sol(S) = R$

Ahora, verificaremos si $C = (0, -1, 4)$ y $D = (1, 4, -3)$ pertenecen a la recta:

$¿C \in R?$
$$
\begin{align}
2 \times 0 - (-1) &= 1 \\
0 + 1 &= 1 \\
1 &= 1
\end{align}
$$
La primera ecuación se verifica correctamente.
$$
\begin{align}
3 \times 0 + 4 &= 4
0 + 4 &= 4
4 &= 4
\end{align}
$$
También se verifica la segunda.

De esta forma, confirmamos que $C \in R$.

$¿D \in R?$
$$
\begin{align}
2 \times 1 - 4 &= 1 \\
2 - 4 &= 1 \\
-2 &\neq 1
\end{align}
$$
Como vemos, no se cumple para la primera ecuación, por lo que confirmamos que $D \not \in R$.

En conclusión, tenemos dos tipos de ecuaciones:
- Ecuaciones fáciles de construir: paramétricas y vectoriales.
- Ecuaciones fáciles de usar: implícitas.

