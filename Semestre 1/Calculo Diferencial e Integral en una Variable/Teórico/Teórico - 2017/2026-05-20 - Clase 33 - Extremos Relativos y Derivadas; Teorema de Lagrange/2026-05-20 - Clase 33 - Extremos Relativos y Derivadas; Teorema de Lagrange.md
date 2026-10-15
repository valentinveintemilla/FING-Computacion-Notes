# Derivadas
Durante esta instancia, trataremos el tema extremos relativos y derivada.

## Extremos relativos y derivada
Anteriormente, vimos el concepto de extremo absoluto en el teorema de Weierstrass.

#Definición
> [!Extremos relativos - Definición]
> Sea $f : I \to \mathbb{R}$. Un punto $(x_{0}, f(x_{0}))$ es:
> - Un máximo relativo de $f$ si
> $$
> \exists \delta > 0, \forall x \in E(x_{0}, \delta) \cap I, \qquad f(x) \leq f(x_{0})
> $$
> - Un mínimo relativo de $f$ si
> $$
> \exists \delta > 0, \forall x \in E(x_{0}, \delta) \cap I, \qquad f(x) \geq f(x_{0})
> $$
> 
> Además, se dice que $f$ tiene un máximo/mínimo/extremo relativo en $x_{0} \in I$ cuando el punto $(x_{0}, f(x_{0}))$ es mínimo/máximo/extremo relativo de $f$.
> 
> Los mínimo/máximos/extremos absolutos son casos particulares de mínimos/máximos/extremos relativos.

Lógicamente, denotamos como extremo relativo a todo punto que sea máximo relativo o mínimo relativo.

La diferencia con el máximo o mínimo absoluto es que aquí se restringe la cuantificación a un entorno de $x_{0}$. Para la definición de absoluto, se remueven los entornos, simplemente se consideran los $x \in I$.
Además, la noción de absoluto es global, tenemos que conocer toda la función para determinarlo. Sin embargo, cuando hablamos de extremo relativo (o máximo/mínimo local), simplemente estudiamos la función en un radio reducido.

En una función pueden haber como máximo 2 extremos absolutos (mínimo y máximo) diferentes (pudiendo haber más si son iguales), pero pueden haber infinitos extremos relativos diferentes.

Posteriormente, demostraremos que en los extremos relativos, la derivada es nula. Sin embargo, para los extremos del intervalo, solo existe la derivada por uno de los dos lados (izquierda -si es el extremo derecho- o derecha -si es el extremo izquierdo-) (mismo caso para los límites).

Demostraremos una condición necesaria para hacer un extremo relativo:

#Proposición 
### Proposición

> [!Proposición]
> Sea $f : I \to \mathbb{R}$. Si $f$ tiene un extremo relativo en un punto interior $x_{0} \in \overset{\circ} I$, y si $f$ es derivable en $x_{0}$, entonces $f'(x_{0}) = 0$.

De esta forma, el teorema no se aplica para los puntos extremos del intervalo (solo funciona en el interior del mismo).

#### Demostración
Caso de un máximo relativo (el otro caso es análogo).

Como $(x_{0}, f(x_{0}))$ es un máximo relativo, existe $\delta > 0$ tal que
$$
f(x) \leq f(x_{0}) \qquad \forall x \in E(x_{0}, \delta) \cap I
$$
Como $x_{0} \in \overset{\circ} I$, se puede tomar $\delta > 0$ suficientemente pequeño para que $E(x_{0}, \delta) \subset I$.

Tenemos que
$$
\forall x \in \underbrace{ [x_{0} - \delta, x_{0} + \delta] }_{ \subset I }, f(x) \leq f(x_{0})
$$

Ahora, analizaremos el cociente incremental, el cual tiene sentido para todo $x$, menos para $x_{0}$.

Ahora, utilizaremos la hipótesis de derivabilidad:
Como $f$ es derivable en $x_{0}$, el cociente incremental $\frac{f(x) - f(x_{0})}{x - x_{0}}$ tiene límites por la izquierda y por la derecha en $x_{0}$, las cuales son iguales.

(Ahora, como $x_{0} \in \overset{\circ} I$, podemos considerar a la vez la derivada por la izquierda y por la derecha, por lo que el cociente incremental tiene sentido por ambos lados.)

Se observa que
$$
\frac{f(x) - f(x_{0}) (\leq 0)}{x - x_{0} (> 0)} \leq 0 \qquad \forall x \in (x_{0}, x_{0} + \delta]
$$
Luego:
$$
\lim_{ x \to x_{0}^{+} } \frac{f(x) - f(x_{0})}{x - x_{0}} \leq 0
$$
(Si estudiamos el cociente incremental, podemos ver que el denominador es positivo, mientras que el numerador es negativo o nulo, puesto que $f(x_{0})$ es el máximo relativo.)

Ahora, estudiamos lo que pasa por la izquierda:
$$
\frac{f(x) - f(x_{0}) (\leq 0)}{x - x_{0} (< 0)} \geq 0 \qquad \forall x \in [x_{0} - \delta, x_{0})
$$
Luego:
$$
\lim_{ x \to x_{0}^{-} } \frac{f(x) - f(x_{0})}{x - x_{0}} \geq 0
$$
(De esta forma, vemos que la derivada por la izquierda es positiva o nula, y la derivada por la derecha es negativa o nula. En conclusión, la derivada en el punto $x_{0}$ tiene que ser a la vez positiva o nula y negativa o nula, por lo que determinamos que es nula.)

Por lo tanto:
$$
\begin{cases}
f'(x_{0}) \leq 0 \\
f'(x_{0}) \geq 0
\end{cases} \implies f'(x_{0}) = 0
$$

Esta demostración muestra algo más importante, sin hipótesis sobre la posición del punto $x_{0}$:
Cuando tengo un máximo relativo, entonces la derivada por la izquierda tiene que ser positiva y la derivada por la derecha tiene que ser negativa. Más en general, sucede con los máximos (relativos y absolutos).

Observación

1. La propiedad no se cumple en general cuando $x_{0}$ es uno de los extremos de $I$ ($x_{0} \in \overset{-} I \land x_{0} \not \in \overset{\circ} I$).
2. Cuando $f'(x_{0})$ no existe, no se puede deducir nada.
3. El recíproco no se cumple:
$$
f'(x_{0}) = 0 \cancel{ \implies } \text{extremo relativo}
$$

(2) Sin embargo, si se pueden estudiar la derivada por la izquierda y por la derecha (en caso de que existan). En este caso, si el punto es un máximo/mínimo, entonces si se cumplen las propiedades enunciadas.

(3) Ejemplo: $f(x) = x^{3}$
En este caso $f'(0) = 0$, pero:
$$
\begin{align}
&\lim_{ x \to 0^{-} } \frac{f(x) - f(0)}{x - 0} > 0 \\
&\lim_{ x \to 0^{+} } \frac{f(x) - f(0)}{x - 0} > 0
\end{align}
$$

---
Antes de abordar el teorema de Lagrange, estudiaremos el lema de Rolle, el cual nos dará paso a la demostración del teorema correspondiente:

#Lema
## Lema (Rolle)

> [!Lema - Rolle]
> Si $f : [a, b] \to \mathbb{R}$ es continua en $[a, b]$, derivable en $(a, b)$ y tal que $f(a) = f(b)$, entonces existe $c \in (a, b)$ tal que $f'(c) = 0$.

La derivada se anula debido a que hay extremos relativos.

![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-05-20 - Clase 33 - Extremos Relativos y Derivadas; Teorema de Lagrange/Imágenes/1 - Lema de Rolle.png]]

### Demostración
Por el teorema de Weierstrass, existen $x_{0}, x_{1} \in [a, b]$ tales que
$$
\forall x \in [a, b], \qquad \underbrace{ f(x_{0}) }_{ m } \leq f(x) \leq \underbrace{ f(x_{1}) }_{ M }
$$
**Caso 1: $m = M$**:
$f$ es constante:
$$
f'(x) = 0 \qquad \forall x \in (a, b)
$$
Entonces, se toma $c$ cualquiera.

**Caso 2: $m < M$**:
(En este caso, al menos uno de los dos puntos $x_{0}, x_{1}$ está dentro del intervalo (puesto que $f(a) = f(b)$).)

Como $f(a) = f(b)$, hay al menos uno de los dos puntos $x_{0}$ y $x_{1}$ en $(a, b)$.
- Si $x_{0} \in (a, b)$, se toma $c := x_{0}$, y tenemos que $f'(c) = 0$.
- Si $x_{1} \in (a, b)$, se toma $c := x_{1}$, y tenemos que $f'(c) = 0$.

(Si $x_{0}, x_{1} \in (a, b)$, podemos tomar cualquiera.)
(Básicamente, cada vez que tengo una función derivable en un intervalo, y las imágenes de los extremos del intervalo son iguales, entonces necesariamente encuentra algún mínimo/máximo relativo, donde la derivada se anula.)

Finalmente, podemos abordar el Teorema de Lagrange:

#Teorema
## Teorema (del valor medio) de Lagrange

> [!Teorema (del valor medio) de Lagrange]
> Sea $f : [a, b] \to \mathbb{R}$, continua en $[a, b]$ y derivable en $(a, b)$.
> 
> Entonces, existe $c \in (a, b)$ tal que
> $$
> f'(c) = \frac{f(b) - f(a)}{b - a}
> $$

El lema es un resultado preliminar al teorema, razón por la cual lo estudiamos y demostramos antes. Ahora, utilizaremos dicho lema para demostrar el teorema correspondiente. (que es una generalización del lema de Rolle).

### Demostración
Sea $\lambda := \frac{f(b) - f(a)}{b - a}$.

Se define $g : [a, b] \to \mathbb{R}$ por $g(x) = f(x) - \lambda (x - a)$.
$g$ es continua en $[a, b]$ y derivable en $(a, b)$.
$$
\begin{align}
&g'(x) = f'(x) - \lambda \\
&g(a) = f(a) - \lambda(a - a) = f(a) \\
&g(b) = f(b) - \lambda(b - a) = f(b) - (f(b) - f(a)) = f(a)
\end{align}
$$
Como vemos, $g(a) = g(b)$.

Por el lema de Rolle, existe $c \in (a, b)$ tal que $g'(c) = 0$.

Entonces $f'(c) = g'(c) + \lambda = \lambda$.

![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-05-20 - Clase 33 - Extremos Relativos y Derivadas; Teorema de Lagrange/Imágenes/2 - Teorema de Lagrange.png]]

Lo que dice el teorema de Lagrange (geométricamente), es que si consideramos la pendiente global de la función en el intervalo considerado (recta que pasa por los puntos $(a, f(a))$ y $(b, f(b))$), se puede hallar un punto, para el cual la recta tangente tiene la misma pendiente que la pendiente global. De esta forma, la tangente a dicho punto es paralela al segmento formado por los dos extremos de la gráfica.

Básicamente, el lema de Rolle es un caso específico, puesto que se cumple que $f(a) = f(b)$, haciendo que el segmento $AB$ tenga pendiente 0. De esta forma, habrá al menos un punto para el cual la tangente en dicho punto tenga pendiente 0, coincidiendo con un mínimo/máximo relativo.

En conclusión, Lagrange vincula la velocidad global $\frac{f(b) - f(a)}{b - a}$ con la velocidad local $f'(c)$, en al menos un punto del intervalo. Veremos que esto implica directamente que el signo de la derivada determina el crecimiento de la función.

A continuación, estudiaremos dos proposiciones relacionadas:

### Proposición 1

> [!Proposición 1]
> Sea $f : [a, b] \to \mathbb{R}$ continua en $[a, b]$ y derivable en $(a, b)$. Entonces:
> 1. $f$ es monótona creciente en $[a, b]$
> $$
> \Longleftrightarrow \forall x \in (a, b), f'(x) \geq 0
> $$
> 2. $f$ es monótona decreciente en $[a, b]$
> $$
> \Longleftrightarrow \forall x \in (a, b), f'(x) \leq 0
> $$
> 3. $f$ es constante en $[a, b]$
> $$
> \Longleftrightarrow \forall x \in (a, b), f'(x) = 0
> $$

Es interesante porque solo se estudian las derivadas del intervalo abierto, pero se deducen propiedades en el intervalo cerrado. Es debido a que la función es continua en el intervalo cerrado.

Aquí, las dos primeras demostraciones son análogas. Podemos demostrar una de las dos, y luego intercambiar $f$ por $-f$.
El tercer punto es la conjunción de 1 y 2: si es constante, entonces es a la vez creciente y decreciente, su derivada es a la vez positiva o nula y negativa o nula, entonces es nula.

#### Demostración (1)
Comenzaremos por la implicación directa:
$\implies$: Supongamos que $f$ monótona creciente. Sea $x_{0} \in (a, b)$

Se observa que $\frac{f(x) - f(x_{0})}{x - x_{0}}$.
Hay dos casos:
1. Si $x > x_{0}$:
$x - x_{0} > 0$ y $f(x) - f(x_{0}) \geq 0$ (ya que es monótona creciente).

Luego:
$$
\frac{f(x) - f(x_{0})}{x - x_{0}} \geq 0
$$

2. Si $x < x_{0}$:
$x - x_{0} < 0$ y $f(x) - f(x_{0}) \leq 0$ (ya que es monótona creciente).

Luego:
$$
\frac{f(x) - f(x_{0})}{x - x_{0}} \geq 0
$$

En ambos casos, determinamos que todos los cocientes incrementales son positivos o nulos.

En conclusión:
$$
f'(x_{0}) \geq 0
$$

Continuamos con el recíproco:
$\impliedby$: Supongamos que $\forall x \in (a, b), f'(x) \geq 0$

Sean $x_{0}, x_{1} \in [a, b]$ tales que $x_{0} < x_{1}$, queremos mostrar que $f(x_{0}) \leq f(x_{1})$.

Por Lagrange, existe $x \in (x_{0}, x_{1})$ tal que
$$
f'(x) = \frac{f(x_{1}) - f(x_{0})}{x_{1} - x_{0} (> 0)} \geq 0
$$
Luego:
$$
f(x_{1}) - f(x_{0}) \geq 0
$$
Es decir
$$
f(x_{0}) \leq f(x_{1})
$$
Por lo tanto, la función es monótona creciente.

La próxima clase abordaremos otra versión de la proposición con derivadas estrictamente positivas y negativas, sin el caso nulo.

