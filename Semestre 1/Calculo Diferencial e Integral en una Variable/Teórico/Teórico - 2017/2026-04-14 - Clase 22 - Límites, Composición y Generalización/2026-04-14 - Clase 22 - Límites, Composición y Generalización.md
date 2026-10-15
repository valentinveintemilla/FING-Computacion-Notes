Esta será la última clase de límites. Continuamos con la composición de límites.
# Composición de límites

> [!Composición de límites]
> $f: I \to \mathbb{R}, g: J \to \mathbb{R}$ tales que $f(I) \subset J$ (cada vez que aplico $f$ a un elemento de $I$, obtengo un elemento de $J$, por lo que es posible definir la compuesta)
> $$
> \begin{align}
> &g \circ f : I \to \mathbb{R} \\
> &x \mapsto (g \circ f)(x) = g(f(x))
> \end{align}
> $$

($x \mapsto \dots$ se lee: "función que a cada $x$ me asocia $\dots$").

Aclarar que, en la composición, el orden de escritura es inverso al orden de aplicación: se aplican las funciones de derecha a izquierda.

## Propiedad

> [!Propiedad]
> Si $x_{0} \in \overset{-} I$
> Si $\lim_{ x \to x_{0} } f(x) = y_{0}$ con $y_{0} \in J$
> y $\lim_{ y \to y_{0} } g(y) = g(y_{0})$ ($g$ continua en $y_{0}$)
> entonces
> $$
> \lim_{ x \to x_{0} } (g \circ f)(x) = g(y_{0})
> $$

Este es el teorema más general que veremos. Considerar que las funciones $f$ y $g$ no se tratan del mismo modo. $f$ tiene límite y no necesariamente se trata de $f(x_{0})$. Además, $x_{0}$ puede incluso estar fuera de $I$ (en caso de que sea abierto). Lo importante es que el límite $y_{0}$ pertenezca a $J$.

En cambio, sobre la segunda función, esta tiene límite y además tiene que coincidir con el valor de la función en el punto.

Por esta razón, hay una asimetría.

Veremos un corolario que es mucho más sencillo (y utilizaremos a lo largo del curso). En lugar de utilizar un límite general para $f$, usamos un caso puntual de continuidad.

> [!Corolario]
> Si $f$ es continua en $x_{0} \in I$ y $g$ es continua en $y_{0} = f(x_{0}) \in J$
> entonces $g \circ f$ es continua en $x_{0}$.

Como vemos, se trata de un caso particular, en el que $x_{0} \in I$, $y_{0} = f(x_{0})$, y $g(y_{0}) = g(f(x))$.

Veremos un contraejemplo que demuestra que si la primer hipótesis de la propiedad es aún más general, no funciona. Lo que es fundamental es suponer que $g$ es continua.

### Contraejemplo
$f, g : \mathbb{R} \to \mathbb{R}$
$f(x) = 0$ (continua)
$g(y) = \begin{cases} \begin{align} &1 &&\text{si} &y = 0 \\ &0 &&\text{si} &y \neq 0 \end{align} \end{cases}$ (discontinua en un punto para no satisfacer la condición de continuidad)

Se observa que: si $x_{0} = y_{0} = 0$
$$
\lim_{ x \to x_{0} } f(x) = 0 = y_{0}
$$
$$
\lim_{ y \to y_{0} } g(y) = 0
$$
Ahora, si la propiedad funcionase, cuando tiendo a $x_{0}$ obtengo 0, y cuando tiendo a $y_{0}$ obtengo 0, si componemos deberíamos obtener una función que tienda a 0 en dicho punto. Sin embargo, esto es falso:

<u>Pero</u>:
$$
(g \circ f)(x) = g(f(x)) = g(0) = 1
$$
De esta manera, la función compuesta es constante ($(g \circ f)(x) = 1$).

<u>Luego</u>:
$$
\lim_{ x \to x_{0} } (g \circ f)(x) = 1 \neq 0
$$

La idea es que ignoramos el caso $y = 0$ para tomar el límite cuando $g$ tiende a 0, pero como la compuesta únicamente considera este valor, este punto determinó la definición de la compuesta y el límite en $y_{0}$.
Igualmente, en la mayoría de los casos, consideraremos el corolario (propiedad sencilla): si $f$ es continua en todos los puntos de $I$, y $g$ es continua en todos los puntos de $J$, entonces la compuesta será continua en todos los puntos de $I$.

---
Ahora, ¿Cómo se usa este teorema en la práctica?

### Ejemplo: Continuidad de $\log: \mathbb{R}^{+} \to \mathbb{R} \qquad (\log(x) = \int_{1}^{x} \frac{dt}{t})$
La clase pasada demostramos utilizando el teorema del Sándwich que la función logaritmo es continua en el punto 1.

Ya sabemos que $\log$ es continua en 1, y su valor es 0.
(Ahora, usaremos el teorema de composición para extender la propiedad de continuidad a todos los puntos que nos interesan del logaritmo.)

Queremos demostrar que $\log$ es continua en cualquier punto $x_{0} \in \mathbb{R}^{+}$.
(Usaremos el punto de referencia 1, y aplicaremos la propiedad fundamental para determinar que logaritmo es continua en todo su dominio de definición.)

Sea $x_{0} \in \mathbb{R}^{+}$ fijado:
Sea $f : \mathbb{R}^{+} \to \mathbb{R}$ definida por $f(x) = \frac{x}{x_{0}}$ continua.
(Sabemos que es continua porque es cociente de la identidad y una constante, ambas continuas).

En particular
$$
\lim_{ x \to x_{0} } f(x) = 1 = f(x)
$$
(Esta función nos sirve para reducir el problema al punto 1, puesto que es lo único que conocemos de la función logaritmo).

Sea $g : \mathbb{R}^{+} \to \mathbb{R}$ definida por $g(x) = \log(f(x)) = \log \frac{x}{x_{0}}$.
(Sobre esta función podemos decir que es la compuesta de $f$ con $\log$: $g(x) = \log \circ f = \log(f(x))$. Además, sabemos que $f$ es continua en $x_{0}$ y como su imagen es 1, el logaritmo también es continuo en 1, por lo que la compuesta es continua en $x_{0}$).

Por composición: $g = \log \circ f$ es continua en $x_{0}$.
(Es fundamental verificar que la imagen de $f$ sea el conjunto $\mathbb{R}^{+}$, puesto que recordemos que el codominio de $f$ tiene que estar contenido en el dominio de $\log$, para poder realizar la composición correctamente. En este caso lo es, ya que $x \in \mathbb{R}^{+}$ y $x_{0}$ es un valor constante positivo).

Pero se observa que
$$
\begin{align}
\log (x) &= \log \left( \frac{x}{x_{0}} \right) + \log(x_{0}) \\
&= \underbrace{ g(x) + \log(x_{0}) }_{ \underset{x \to x_{0}} \to \log(x_{0}) }
\end{align}
$$
Como sabemos, $g$ es continua en $x_{0}$, a la cual le sumamos $\log(x_{0})$, que es constante, por lo que no afecta su continuidad. De esta forma, deducimos que $\log$ es continuo en $x_{0}$ (usando la propiedad fundamental del logaritmo).

Esto nos da un nuevo teorema: la función logaritmo es continua en su dominio de definición.

---
Ahora, pasaremos a hablar de generalización de límites, puesto que por ahora solo hemos trabajado con límites finitos.

Por esta razón, desarrollaremos una única definición que abarque todos los casos posibles.

## Generalización de la noción de límite
La idea es que la noción de límite trata principalmente de entornos, por lo que lo importante aquí sería definir que es un entorno, especificando el conjunto de todos los entornos de un punto.

**Notación**
Dado un real $a \in \mathbb{R}$, se definen:
$$
\begin{align}
\mathcal{E}(a) &= \{ E(a, \epsilon) : \epsilon > 0 \} = \{ (a - \epsilon, a + \epsilon) : \epsilon \in \mathbb{R}^{+} \} \\
\mathcal{E}^{*}(a) &= \{ E^{*}(a, \epsilon) : \epsilon > 0 \} = \{ (a - \epsilon, a) \cup (a, a + \epsilon) : \epsilon \in \mathbb{R}^{+} \}
\end{align}
$$
(Conjunto de conjuntos, todos los entornos, además de todos los entornos reducidos).

Aquí tenemos un nivel de abstracción mayor, puesto que partimos de un punto y un $\epsilon$, pasando a la noción de entorno que es un conjunto de puntos y ahora definimos el conjunto de todos los entornos.

### Observación

> [!Observación]
> Dados $f : I \to \mathbb{R}, x_{0} \in \overset{-} I, L \in \mathbb{R}$, tenemos que:
> $$
> \begin{align}
> \lim_{ x \to x_{0} } f(x) = L &\Longleftrightarrow \forall \epsilon > 0, \exists \delta > 0, \forall x \in I, 0 < |x - x_{0}| < \delta \implies |f(x) - L| < \epsilon \\
> &\Longleftrightarrow \forall \epsilon > 0, \exists \delta > 0, \forall x \in E^{*}(x_{0}, \delta) \cap I, 0 < |x - x_{0}| < \delta, f(x) \in E(L, \epsilon) \\
> &\Longleftrightarrow \forall \epsilon > 0, \exists \delta > 0, f(\underbrace{ E^{*}(x_{0}, \delta) }_{ E } \cap I) \subset \underbrace{ E(L, \epsilon) }_{ F }
> \end{align}
> $$

Únicamente son variantes de la definición, partiendo desde la original.
Como vemos, cada vez utilizamos conceptos algo más complejos y abstractos, con la idea de hacer desaparecer los $\epsilon$ y $\delta$.

De esta forma, la última establece que "para todo entorno del límite (tomando $\epsilon$), existe un entorno reducido del punto $x_{0}$ (tomando $\delta$), que verifica $f(E^{*}(x_{0}, \delta) \cap I) \subset E(L, \epsilon)$".

Es así que podemos establecer:
$$
\forall F \in \mathcal{E}(L), \exists E \in \mathcal{E}^{*}(x_{0}), f(E \in I) \subset F
$$
Así, logramos definir a los límites sin utilizar $\epsilon$ y $\delta$.
La idea es que $\epsilon$ solo sirve para definir cual es el entorno particular de $L$ considerado, mientras que $\delta$ solo sirve para definir el entorno reducido particular de $x_{0}$ considerado, pero ahora que tengo un conjunto de entornos, podemos desarrollar una definición más abstracta:

"Para todo entorno del límite (tamaño alrededor de $L$), existe un entorno reducido alrededor de $x_{0}$ tal que la imagen de la función nunca sale fuera de la banda horizontal ni vertical".
![[1 - Definición de límite con entornos.png]]

---
Ahora, teniendo una definición más general de límite, tenemos una función parametrizada por la noción de entorno, de forma que esta definición nos sirve para todos los tipos de límites, siendo necesario únicamente cambiar la noción de entorno, las cuales serán introducidas a continuación:

Se consideran las siguientes nociones de entorno:
1. Entornos de $a \in \mathbb{R}$, definidos por $\mathcal{E}(a)$ (llenos) y $\mathcal{E}^{*}(a)$ (reducidos):
(En las nociones que prosiguen, solo trabajamos con entornos llenos, pues son iguales en el resto).

2. Entornos de $\pm \infty$:
$$
\mathcal{E}(+ \infty) = \mathcal{E}^{*}(+ \infty) = \{ (L, + \infty) : L \in \mathbb{R} \} \qquad \text{(todo intervalo abierto que va hasta el infinito)}
$$
$$
\mathcal{E}(- \infty) = \mathcal{E}^{*}(- \infty) = \{ (- \infty, L) : L \in \mathbb{R} \} \qquad
$$

3. Entornos de $a \in \mathbb{R}$ por la izquierda/derecha:
$$
\mathcal{E}(a^{+}) = \mathcal{E}^{*}(a^{+}) = \{ (a, a + \epsilon) : \epsilon \in \mathbb{R}^{+} \} \qquad \text{(todo intervalo por la derecha)}
$$
$$
\mathcal{E}(a^{-}) = \mathcal{E}^{*}(a^{-}) = \{ (a - \epsilon, a) : \epsilon \in \mathbb{R}^{+} \}
$$

Estas son las 5 nociones de entorno: entornos de $a$, entornos de $+ \infty$, entornos de $- \infty$, entornos de $a$ por la derecha, y entornos de $a$ por la izquierda.

---
Finalmente, podemos desarrollar una noción general de límite.

## Límite generalizado

> [!Definición]
> Dados:
> - $f : I \to \mathbb{R}$
> - un "punto generalizado": $k = \underbrace{ a }_{ \text{real} }, \underbrace{ + \infty, - \infty }_{ \text{real extendido} }, \underbrace{ a^{+}, a^{-} }_{ \text{pseudonúmeros} } \qquad (a \in \mathbb{R})$
> - un "límite generalizado": $l = b, + \infty, - \infty, b^{+}, b^{-} \qquad (b \in \mathbb{R})$
> 
> Se define:
> $$
> \lim_{ x \to k } f(x) = l \Longleftrightarrow \forall F \in \mathcal{E}(L), \exists E \in \mathcal{E}^{*}(k), f(E \cap I) \subset F
> $$

De esta manera, definimos 25 nociones diferentes de límite (todas las combinaciones de las anteriores).
La noción que ya estudiamos es el caso particular en el que $k$ y $l$ son reales.

Cada vez que necesitemos una definición de límite, tomamos la definición general y pasamos a la definición real.

> [!Observación]
> La definición sólo tiene sentido cuando
> $$
> \forall E \in \mathcal{E}^{*}, E \cap I \neq \emptyset
> $$

Esto nos sirve para reemplazar la noción de punto adherente (cosa que antes podíamos utilizar), pues como $k$ no siempre es un real, no podemos decir que es un punto adherente.
Esto lo reemplazamos verificando que todos los entornos reducidos de $k$ intercepten $I$.
Además, cuando $k$ es un real, coincide con la noción de punto adherente.

Aclaración

> [!Aclaración]
> Cada vez que hablamos de límites (SIEMPRE):
> - Codominio: Entornos llenos   $\qquad E() \text{ o } \mathcal{E}()$
> - Dominio: Entornos reducidos $\qquad E^{*}() \text{ o } \mathcal{E}^{*}()$

Igualmente, en el caso de los límites extendidos, no hay ninguna diferencia, solo se da para el límite usual.

---
Ahora, pasaremos a ver algunos ejemplos de límites.

### Límites infinitos
$$
\lim_{ x \to x_{0} } f(x) = + \infty \Longleftrightarrow \forall L \in \mathbb{R}, \exists \delta > 0, \forall x \in I, 0 < |x - x_{0}| < \delta \implies f(x) > L
$$
Para que $f(x)$ pertenezca al entorno dado por $L$ y $+ \infty$, tiene que cumplirse que $f(x) > L$.

Este es el caso particular en el que $k$ es un número real y $l$ es $+ \infty$, logrando desarrollar la definición en base a la general y consiguiendo la que yo quiero.

Para el caso $l = - \infty$
$$
\lim_{ x \to x_{0} } f(x) = - \infty \Longleftrightarrow \forall L \in \mathbb{R}, \exists \delta > 0, \forall x \in I, 0 < |x - x_{0}| < \delta \implies f(x) < L
$$

De esta manera, logramos extender la noción de límite a $\pm \infty$, por lo que se pueden extender casi todos los resultados usuales. Para esto definiremos la recta real extendida:

> [!Definición - Recta real extendida]
> $$
> \mathbb{\overset{-} R} = \mathbb{R} \cup \{ - \infty, + \infty \}
> $$

Llamaremos $\mathbb{\overset{-} R}$ al conjunto de los números reales, agregando a dicho conjunto los elementos $- \infty$ y $+ \infty$.

### Proposición

> [!Proposición - Unicidad del límite]
> Si una misma función tiene dos límites en $\mathbb{\overset{-} R}$, entonces los límites son iguales. Esto significa que si la función tiene límite finito, no solo no puede tener otro límite finito, sino que tampoco puede tener límite infinito, y viceversa (si tiende al infinito, no solo no puede tener límite finito, sino que tampoco puede tener límite menos infinito).

De esta forma, las opciones se excluyen.

---
A continuación, veremos como operar con los límites:

### Proposición (Suma)
Si $\lim_{ x \to x_{0} } f(x) = L \in \mathbb{\overset{-} R}$ y $\lim_{ x \to x_{0} } f(x) = L' \in \mathbb{\overset{-} R}$
entonces el límite de $f + g$ en $x_{0}$ es dado (cuando existe) por:

(veremos que pasa en cada uno de los casos posibles de suma)

|                    | $L' = - \infty$ | $L' \in \mathbb{R}$ | $L' = + \infty$ |
| :----------------: | :-------------: | :-----------------: | :-------------: |
|   $L = - \infty$   |   $- \infty$    |     $- \infty$      |       $?$       |
| $L \in \mathbb{R}$ |   $- \infty$    |      $L + L'$       |   $+ \infty$    |
|   $L = + \infty$   |       $?$       |     $+ \infty$      |   $+ \infty$    |
$? \to \text{Indeterminación}$
En esos casos no se puede predecir nada, ni siquiera si la función tiene límite. (IGUALMENTE, DEPENDE DEL CASO).

### Caso del producto
Pasamos del teorema (tiene exactamente la misma forma), solo analizaremos la tabla:

|                | $L' = - \infty$ |  $L' < 0$  | $L' = 0$ |  $L' > 0$  | $L' = + \infty$ |
| :------------: | :-------------: | :--------: | :------: | :--------: | :-------------: |
| $L = - \infty$ |   $+ \infty$    | $+ \infty$ |   $?$    | $- \infty$ |   $- \infty$    |
|    $L < 0$     |   $+ \infty$    |   $L L'$   |    0     |   $L L'$   |   $- \infty$    |
|     L = 0      |       $?$       |     0      |    0     |     0      |       $?$       |
|     L > 0      |   $- \infty$    |   $L L'$   |    0     |   $L L'$   |   $+ \infty$    |
| $L = + \infty$ |   $- \infty$    | $- \infty$ |   $?$    | $+ \infty$ |   $+ \infty$    |
De esta forma, la indeterminación esta dada por $0 \times \pm \infty = \space ?$ (no se puede deducir nada en este caso).

### Caso del cociente
Por último, veremos la tabla para el cociente:

- Si $f \to L \neq 0 \implies \frac{1}{f} = \frac{1}{L}$
- Si $f \to + \infty \implies \frac{1}{f} \to 0^{+}$ (por valores positivos)
- Si $f \to - \infty \implies \frac{1}{f} \to 0^{-}$ (por valores negativos)
- Si $f \to 0 \implies \frac{1}{|f|} \to + \infty$
(No sabemos cual es el signo de $f$, por lo tanto utilizamos valor absoluto. No lo utilizamos en la definición, ya que)
(Si $f$ no nula en un entorno de $x_{0}$)

Igualmente, la definición anterior cuando $f \to 0$ tiene algunos vacíos que deberíamos aclarar, por lo que podemos utilizar otra mejor:
- Si $f \to 0^{+} \implies \frac{1}{f} \to + \infty$
- Si $f \to 0^{-} \implies \frac{1}{f} \to - \infty$

No realizamos demostraciones, ya que no son tan interesantes.

También existe la noción de límite lateral, la cual se trata de mirar lo que pasa por la izquierda y por la derecha. Además, hay un teorema de pegado que establece que:

> [!Límites laterales - Teorema de pegado]
> Cuando se tiene un punto interior al intervalo $I$, entonces tiene límite en el punto, si y solo si tiene límite por la izquierda y por la derecha, y ambos coinciden. En caso de no coincidir, la función no tiene límite en el punto correspondiente.
