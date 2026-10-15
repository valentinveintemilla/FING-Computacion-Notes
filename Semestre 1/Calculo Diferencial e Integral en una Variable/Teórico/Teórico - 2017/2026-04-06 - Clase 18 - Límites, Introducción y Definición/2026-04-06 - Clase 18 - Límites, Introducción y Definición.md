En esta clase comenzamos con un nuevo capítulo: Límites y Continuidad.
# Límites y Continuidad
# Introducción
El tema central de las próximas clases será el concepto de continuidad.

En general, todos tenemos una noción del concepto de continuidad, la cual surge de la observación sobre las funciones que son estudiadas en matemática tienen una gráfica que no esta "dividida", sin saltos. Por ejemplo, una recta o muchas de las funciones que hemos visto durante el curso (funciones potencia, logaritmo, etc.). Uno de los casos que no satisface esta noción es la función $f(x)=\frac{1}{x}$, aunque en este caso, esta dado por el dominio, ya que esta separado en dos partes (pues no tiene 0, $dom(f) = \mathbb{R} - \{ 0 \}$). Aunque si analizamos cada subconjunto por separado, podemos ver que la función es continua en los mismos.

Antes se consideraba (según Gauss) que una función por casos podía no ser continua (hay casos en los que es continua, como $|x|=\begin{cases} \begin{align} &x &\text{si} &\qquad x > 0 \\ &0 &\text{si} &\qquad x = 0 \\ &-x &\text{si} &\qquad x < 0 \end{align} \end{cases}$), de forma que una función que no esta separada por casos es siempre continua. Sin embargo, sabemos que este no es así. Por esta razón, hasta el siglo $XIX$ no tuvimos una definición correcta y general de continuidad, siendo bastante compleja (la analizaremos con ejemplos).

Todo el problema se reduce a la idea de límite, la cual consiste en aproximar de modo arbitrario el valor de una función a un punto, tomando valores de x cercanos al punto en cuestión. La idea vulgar es que una función tiene límite en un punto x cuando con mínimos movimientos horizontales, se realizan mínimos movimientos verticales (las imágenes de los valores cercanos a x son próximas).

A continuación, veremos las definiciones necesarias para comenzar a definir la continuidad y los límites.

## Entornos

> [!Definición]
> Sean $x_{0} \in \mathbb{R}$ y $\epsilon > 0$
> El entorno de centro $x_{0}$ y de radio $\epsilon$ es el conjunto
> $$
> \begin{align}
> E(x_{0}, \epsilon) :&= \{ x \in \mathbb{R} : |x - x_{0}| < \epsilon \} \\
> &= (x_{0} - \epsilon, x_{0} + \epsilon)
> \end{align}
> $$
> De esta forma, $E(x_{0}, \epsilon)$ contiene las aproximaciones de $x_{0}$ a menos de $\epsilon$. Equivale al intervalo abierto $(x_{0} - \epsilon, x_{0} + \epsilon)$.

Esto permite formalizar la noción de proximidad, pues en matemática no existe una definición absoluta de dicho termino. Solo podemos decir que dos valores son cercanos, pero podemos decir que son cercanos a menos de alguna distancia (en este caso tienen que cumplir que $|x - x_{0}| < \epsilon$).

También podemos definir el **entorno reducido**:

El entorno reducido de centro $x_{0}$ y de radio $\epsilon > 0$ por
$$
\begin{align}
E^{*}(x_{0}, \epsilon) :&= E(x_{0}, \epsilon) \setminus \{ x_{0} \} \\
&=\{ x \in \mathbb{R} : 0 < |x - x_{0}| < \epsilon \} \\
&=(x_{0} - \epsilon, x_{0}) \cup (x_{0}, x_{0} + \epsilon)
\end{align}
$$
Como vemos, equivale al entorno, menos el punto $x_{0}$, son las aproximaciones estrictas (las aproximaciones sin incluir el centro, el valor al que queremos aproximar).

**<u>Observación</u>**:
$$
\begin{align}
0 < \epsilon' < \epsilon \implies &E(x_{0}, \epsilon') \subset E(x_{0}, \epsilon) \\
\text{y } &E^{*}(x_{0}, \epsilon') \subset E^{*}(x_{0}, \epsilon)
\end{align}
$$
Como sabemos, la noción de entorno depende de un centro y un radio. De esta forma, si se reduce el radio, también se reducen los entornos como conjuntos.

---
A continuación, veremos otros conceptos con el fin de llegar a la definición formal de límites y continuidad: interior y clausura de un intervalo.

## Interior y clausura de un intervalo

> [!Definición]
> Sea un intervalo $I \subset \mathbb{R}$
> - El <u>interior de I</u> es el subintervalo $I^{\circ} \subset I$ obtenido excluyendo los extremos de $I$ (si no pertenecen a $I$, entonces $\overset{\circ} I = I$).
> - La <u>clausura de I</u> es el sobreinvervalo $\overset{-} I \supset I$ obtenido incluyendo los extremos finitos de $I$ (si ya pertenecen a $I$, entonces $\overset{-} I = I$).

En todos los casos:
$$
I^{\circ} \subseteq I \subseteq \overset{-} I
$$
Para completar la definición, estudiaremos lo que pasa en cada tipo de intervalo (son los 10 vistos en clases previas).

|                   Intervalo $I$                   | Interior $\overset{\circ} I$ | Clausura $\overset{-} I$ |
| :-----------------------------------------------: | :--------------------------: | :----------------------: |
| $$[a,b], (a,b], [a,b), (a,b) \text{ con } a < b$$ |          $$(a, b)$$          |        $$[a,b]$$         |
|          $$(-\infty, a], (-\infty, a)$$           |       $$(-\infty, a)$$       |     $$(-\infty, a]$$     |
|          $$[a, +\infty), (a, +\infty)$$           |       $$(a, +\infty)$$       |     $$[a, +\infty)$$     |
|        $$(-\infty, +\infty) = \mathbb{R}$$        |        $$\mathbb{R}$$        |      $$\mathbb{R}$$      |
|              $$\{ a \} ( = [a, a])$$              |        $$\emptyset$$         |       $$\{ a \}$$        |
|                   $$\emptyset$$                   |        $$\emptyset$$         |      $$\emptyset$$       |
**<u>Observación</u>**:

En todos los casos tenemos la doble inclusión: el intervalo contiene a su interior, y está contenido en su clausura.
$$
I^{\circ} \subseteq I \subseteq \overset{-} I
$$
---
Ahora, con estas notaciones, introduciremos algo de terminología.
## Vocabulario
- $x$ es interior a $I$ si $x \in \overset{\circ} I$.
En particular, en un intervalo $[a,b]$, los puntos interiores son todos los puntos del intervalo salvo los extremos ($a$ y $b$). De esta forma, es un punto del intervalo que no es un extremo.

- $x$ es adherente a $I$ si $x \in \overset{-} I$.
De esta forma, también $x \in \overset{\circ} I$, siendo cualquier punto del intervalo (incluso los extremos aunque no pertenezcan al mismo).

En general, podemos decir que:
$$
\begin{align}
x \text{ es un punto interior de } &[a,b] \Longleftrightarrow x \in (a,b) \\
&(a,b)
\end{align}
$$
---
Anteriormente realizamos una caracterización por casos. Sin embargo, desarrollaremos una idea uniforme que no depende de la forma del intervalo.

## Proposición
Dados $I \subset \mathbb{R}$ y $x \in \mathbb{R}$
- $x \in \overset{\circ} I \Longleftrightarrow \exists \epsilon > 0, E(x, \epsilon) \subset I$
Esta definición funciona, puesto que si $x$ se encuentra en el intervalo siempre habrá un valor de $\epsilon$ que asegura que cualquier intervalo de centro $x$ y radio $\epsilon$ estará dentro del intervalo $I$. En cambio, si $x$ es un extremo del intervalo, ya no es interior a $I$, puesto que por más mínimo que sea el valor de $\epsilon$, el entorno siempre se saldrá del intervalo por algún lado.

- $x \in \overset{-} I \Longleftrightarrow \forall \epsilon > 0, E(x, \epsilon) \cap I \neq \emptyset$
Aquí tenemos dos casos:
1. Sabemos que si $x \in I$, $x \in E(x, \epsilon)$, por lo tanto la intersección de ambos no será vacía (al menos incluirá al punto $x$).
2. Cuando $x \not \in I$, siempre encontraremos un valor de $\epsilon$ para el que $E(x, \epsilon) \cap I = \emptyset$. Sin embargo, si $x$ es uno de los extremos de $I$, entonces sabemos que para cualquier valor de $\epsilon$, la intersección entre el entorno $E(x, \epsilon)$ e $I$ no será vacía.

En conclusión, también podemos tomar las proposiciones anteriores como definición de interior y clausura de un intervalo, la cual no depende de la forma del intervalo y es una definición más bien lógica. Utiliza el concepto de "espacio de seguridad" ($\epsilon$).

En pocas palabras:
- Interior: excluyo los extremos.
- Clausura: incluyo los extremos.
---
Seguimos con una convención:
## Convención
En lo que sigue (en el resto de materias matemáticas de ingeniería), sólo consideraremos funciones definidas en intervalos $I$ cuyo interior no es vacío:
$$
\overset{\circ} I \neq \emptyset
$$
Es así, ya que las funciones con dominio vacío no son muy interesantes para analizar (pues no tienen gráfica). Esto también descarta las funciones que tienen un único punto.
De esta manera, a partir de ahora, tenemos que aclarar que el interior de un intervalo no es vacío cuando lo utilicemos para definir una función.

Esto acarrea una consecuencia importante:

### Propiedad
Si $I \subset \mathbb{R}$ es un intervalo tal que $\overset{\circ} I \neq \emptyset$, entonces:
$$
\forall x_{0} \in \overset{-} I, \forall \epsilon > 0, E^{*}(x_{0}, \epsilon) \cap I \neq \emptyset
$$
A diferencia de las caracterizaciones anteriores, aquí consideramos los entornos reducidos. De esta forma, no solo hay una intersección, sino que existe un punto distinto de $x_{0}$ en la intersección.

Esta claro que esta propiedad no funciona para los intervalos vacíos ni para aquellos que tienen un único punto (puesto que sería el centro y este se excluye).

La propiedad anterior siempre se utilizará en casos posteriores.

---
A continuación, definiremos qué es un límite.
# Límites

> [!Definición]
> Sean $f : I \to \mathbb{R}$ (no vacío, por la convención anterior), $x_{0} \in \overset{-} I$ (interior o extremo de $I$) y $L \in \mathbb{R}$.
> Se escribe:
> $$
> \begin{align}
> &f(x) \underset{x \to x_{0}} \to L &\text{("f(x) tiende a L cuando x tiende a } x_{0} \text{")} \\
> &\lim_{x \to x_{0}} f(x) = L &\text{("f tiene límite L en el punto } x_{0} \text{")}
> \end{align}
> $$
> Cuando:
> $$
> \forall \epsilon > 0, \exists \delta > 0, \forall x \in I, 0 \underbrace{ < }_{ x \neq x_{0} } |x - x_{0}| < \delta \implies |f(x) - L| < \epsilon
> $$
> 

Como vemos es una definición algo compleja, por lo que la explicaremos a continuación. Primero, aclarar que la misma definición se puede desarrollar con diferentes notaciones.

**<u>Observación</u>**:
1. Con los entornos, la definición se escribe:

$$
\begin{align}
&\forall \epsilon > 0, \exists \delta > 0, \forall x \in E^{*}(x_{0}, \delta) \cap I, f(x) \in E(L, \epsilon) \\ \\

&\Longleftrightarrow \forall \epsilon > 0, \exists \delta > 0, f( E^{*}(x_{0}, \delta) \cap I) \subset E(L, \epsilon)
\end{align}
$$
Las tres definiciones son equivalentes, tres métodos que describen el mismo concepto.

<u>Idea</u>
La definición expresa que $f(x)$ es arbitrariamente $\epsilon$ cercano a $L$ en cuanto $x$ sea suficientemente $\delta$ cercano a $x_{0}$.

A continuación, decodificamos lo anterior:
$$
\begin{align}
&\forall \epsilon > 0, & \text{"para toda precisión } \epsilon > 0, \\
&\exists \delta > 0, & \text{existe un radio } \delta > 0, \\
&\forall x \in E^{*}(x_{0}, \delta) \cap I, & \text{si } x \text{ es cercano a } x_{0} ( \text{a menos de } \delta ) \\
&f(x) \in E(L, \epsilon) & \text{entonces f(x) es cercano a L a menos de } \epsilon \text{"}
\end{align}
$$
Si lo bajamos a tierra, esto quiere decir que me doy una precisión $\epsilon > 0$ cualquiera para $f(x)$ (referente al codominio). Dada esta precisión, existe un radio de seguridad en el dominio, que es bastante pequeño, tal que si aplico la función f en este radio de seguridad, no me saldré de la precisión.

Tenemos una función, y el límite está en el codominio. Al fijar una precisión $\epsilon$ (codominio, banda vertical) y un radio $\delta$ (dominio, banda horizontal), la gráfica se encuentra entre ambas bandas (no sale de dicha zona).
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-04-06 - Clase 18 - Límites, Introducción y Definición/Imágenes/Representación de definición de límite.png]]

Aclaración: el factor arbitrario es $\epsilon$ y la suficiencia esta dada por $\delta$.

Esta definición debe ser leída múltiples veces y analizada para entenderla completamente.

**<u>Observación</u>**:
Podemos ver que hay una asimetría entre el dominio y el codominio. El dominio es referenciado en la parte de $x_{0}$ y $\delta$, mientras que el codominio corresponde a $\epsilon$, $f(x)$ y $L$. El detalle es que en el dominio solo se consideran entornos reducidos, mientas que en el codominio no son reducidos.
De esta forma, podemos ver que la definición nunca chequea el valor de $x_{0}$, puesto que no es necesario, ya que por hipótesis $x \neq x_{0}$, por lo que solo se examina lo que sucede alrededor de $x_{0}$, ignorando al mismo.

La consecuencia de esto es que ==cuando existe el valor de f en $x_{0}$, no influye ni en la existencia del límite ni en su valor==.

> [!Observación]
> El valor de $f(x_{0})$ (cuando existe) no influye ni en la existencia del límite, ni en su valor.

Es decir, para saber el valor del límite de una función en el punto $x_{0}$, tenemos que enfocarnos en lo que pasa alrededor del mismo, y no en el punto en sí. Es un intento de predecir lo que pasa en $x_{0}$ basándonos en sus alrededores.

Esto también se relaciona con que antes establecimos que ==$x_{0}$ es adherente a $I$, pero no tiene porque pertenecer a $I$==, lo que refuerza aún más la no necesidad de revisar que sucede en dicho punto.

---
A continuación veremos un teorema.

## Proposición
Sean $f: I \to \mathbb{R}$ y $x_{0} \in \overset{-} I$.
Si $f(x) \underset{x \to x_{0}} \to L$ y $f(x) \underset{x \to x_{0}} \to L'$, entonces $L = L'$.

==Esto establece que el límite para un valor dado en una función siempre es único (en caso de existir)==.

Demostraremos la proposición anterior por el absurdo:

### Demostración
Por el absurdo, supongamos que $L \neq L'$.
Sea $\epsilon := \frac{|L - L'|}{2} > 0$

**Aclaración**: en matemáticas, una precisión puede ser cualquier número positivo. En este caso, nosotros tomamos la mitad de la distancia entre ambos números.

- Como $f(x) \underset{x \to x_{0}} \to L$, existe $\delta > 0$ tal que
$$
\forall x \in E^{*}(x_{0}, \delta) \cap I, f(x) \in E(L, \epsilon)
$$
- Como $f(x) \underset{x \to x_{0}} \to L'$, existe $\delta' > 0$ tal que
$$
\forall x \in E^{*}(x_{0}, \delta') \in I, f(x) \in E(L', \epsilon)
$$
Sabemos que todos los elementos cercanos a $x_{0}$ a menos de $\delta$ cumplen que $f(x) \in E(L, \epsilon)$, y todos los elementos cercanos a $x_{0}$ a menos de $\delta'$ cumplen que $f(x) \in E(L', \epsilon)$, entonces podemos tomar un punto que cumpla la condición más estricta: que pertenezca a $E^{*}(x_{0}, mín(\delta, \delta'))$, de forma que pertenezca a ambos entornos (pues al tener el mismo centro, uno está contenido en el otro).

Se fija $x \in E^{*}(x_{0}, mín(\delta, \delta')) \cap I$ (sabemos que la intersección no es vacía por la convención anterior).
De esta forma sabemos que podemos fijar un punto en dicha intersección, y el mismo es tan cercano a $x_{0}$ que pertenece a la vez a los entornos $E^{*}(x_{0}, \delta)$ y $E^{*}(x_{0}, \delta')$. Además, sabemos que para el punto fijado, ambas condiciones anteriores se cumplen ($f(x) \in E(L, \epsilon)$ y $f(x) \in E(L', \epsilon)$).

Luego:
$$
\begin{align}
&f(x) \in E(L, \epsilon) \text{ y} \\
&f(x) \in E(L', \epsilon)
\end{align}
$$
==Es absurdo, pues ambos conjuntos no se interceptan==.

Si revisamos la definición de $\epsilon$, podemos ver que esto que la conclusión es imposible, ya que $E(L, \epsilon)$ y $E(L', \epsilon)$ no se interceptan (son disjuntos). Por esta razón, no puede ser que $f(x)$ pertenezca a ambos conjuntos si los mismos no tienen elementos en común.

Lo importante desde el principio era fijar una precisión lo suficientemente pequeña para que las bandas verticales (codominio, $\epsilon$) no se intercepten. Como tengo dos límites, sabemos que para un radio, la función estará en uno, y para otro radio, la función estará en el otro, cosa que no tiene sentido.
![[Representación de definición de límite (figura 2).png]]

De esta forma, demostramos que el límite (cuando existe) es único.

---
Vimos que el límite solo tiene sentido cuando el punto de referencia $x_{0}$ esta dentro de $I$ o es un extremo de $I$ ($x_{0} \in \overset{-} I$). Proseguimos con una observación, la cual aborda el caso particular $x_{0} \in I$.

En el caso donde $x_{0} \in I$, existen esencialmente 3 situaciones posibles:
- o bien $f$ no tiene límite en $x_{0}$
- o bien $f$ tiene límite $L \neq f(x_{0})$ en $x_{0}$
- o bien $f$ tiene límite $L = f(x_{0})$ en $x_{0}$
![[Situaciones posibles respecto a un límite.png]]

En el último caso, se dice que la función $f$ es continua en el punto $x_{0}$. Aquí tenemos la definición de continuidad en un punto, y por definición, diremos que una función es continua en el intervalo cuando es continua en todos los puntos, lo que nos da una definición formal de la noción de continuidad.