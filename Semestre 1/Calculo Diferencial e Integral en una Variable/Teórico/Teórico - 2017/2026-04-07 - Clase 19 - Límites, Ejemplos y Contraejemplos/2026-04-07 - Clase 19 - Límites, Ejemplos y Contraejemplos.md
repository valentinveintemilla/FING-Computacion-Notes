La clase pasada vimos la noción de límite y su compleja definición.
# Límites y continuidad
Repasamos la noción de límite.

> [!Límite]
> Dados
> - una función $f: I \to \mathbb{R}$ ($I$ tiene interior no vacío según convención)
> - un punto $x_{0} \in \overset{-} I$ (dentro de $I$ o un extremo)
> - un número $L \in \mathbb{R}$
> 
> $$
> \left.
> \begin{align}
> &\lim_{ x \to x_{0} } f(x) = L \\
> &f(x) \underset{x \to x_{0}} \to L \\
> \end{align}
> \right\} \Longleftrightarrow
> \forall \epsilon > 0\underbrace{ , }_{ \text{tenemos que} } \exists \delta_{\epsilon} > 0\underbrace{ , }_{ \text{tal que} } \forall x \in I, \delta), \underbrace{ 0 < |x - x_{0}| < \delta }_{ E^{*}(x_{0}, \delta) }
> \implies \underbrace{ |f(x) - L| < \epsilon }_{ f(x) \in E(L, \epsilon) }
> $$
> En palabras:
> Para toda precisión $\epsilon$, existe un radio de seguridad $\delta$, tal que para todo $x$ en el dominio de definición, si la distancia entre $x$ y $x_{0}$ es no nula ($x \neq x_{0}$) y menor que $\delta$ ($x$ pertenece a $E^{*}(x_{0}, \delta)$, excluyendo a $x_{0}$), esto implica que la distancia entre $f(x)$ y el límite $L$ es menor que $\epsilon$.

---
Aclaración:
La notación que usan algunos profesores es incorrecta, por ejemplo: $\exists \epsilon > 0$ tal que, o $\exists \epsilon > 0 /$
Esto es incorrecto, ya que estamos suponiendo que $\exists$ únicamente significa "existe", como una abreviatura. Sin embargo, se trata de un símbolo matemático que envuelve todo un significado (múltiples palabras, expresión), como el resto de símbolos matemáticos. Por esta razón, es incorrecto agregar un "tal que" luego, por ejemplo (ya está implícito en la expresión).

Además, podemos utilizar una coma o paréntesis curvos posterior a la expresión:
$$
\begin{align}
&\forall \epsilon > 0, (\dots) \\
&\forall \epsilon > 0, \dots
\end{align}
$$
Nosotros utilizaremos la segunda.

---

Es fundamental comprender lo siguiente:
Si yo tengo un límite, este pertenece al codominio (está en el eje vertical, es un $y$), pues será comparado con $f(x)$. Teniendo un $x_{0}$, la propiedad dice que si se establece un $\epsilon$, esto define una banda horizontal (banda de precisión). Además, la función correspondiente oscila alrededor de la intersección del límite y $x_{0}$.
Finalmente, la idea es hallar un $\delta$ lo suficientemente pequeño (sin llegar a ser nulo), tal que la imagen en la banda de radio $\delta$ este dentro de la banda horizontal.
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-04-07 - Clase 19 - Límites, Ejemplos y Contraejemplos/Imágenes/Representación de definición de límite.png]]
No podemos tomar $\delta$ en una región donde la función esté fuera de la barra horizontal (dada por $\epsilon$).

Además, un detalle importante es que ignoramos lo que sucede en $x_{0}$, pues el límite busca deducir lo que sucede en $x_{0}$ sin analizarlo directamente (se estudian los alrededores del mismo). Por esta razón, no sería un problema que $f(x_{0})$ esté fuera de $L$, sin cambiar el límite.

Esto corresponde con el objetivo fundamental de formalizar matemáticamente la idea de que $x$ es arbitrariamente cercano a $L$ en cuanto $x$ sea suficientemente cercano a $x_{0}$.

De esta forma, ==la noción de límite tiene sentido incluso cuando $x_{0}$ está fuera del intervalo, pero en uno de los extremos== ($x_{0} \in x_{0} \in \overset{-} I$), pues lo que sucede en dicho punto no afecta al valor del límite (en caso de existir).

---
Además, estudiamos la definición importante del caso particular:

**Definición**
$f : I \to \mathbb{R}$ es <u>continua</u> en un punto $x_{0} \in I$ (pertenece al intervalo) si
$$
\underbrace{ \lim_{ x \to x_{0} } f(x) }_{ \text{(existe)} } = f(x_{0})
$$
Entonces, ¿en que casos una función no es continua?
Hay dos casos:
1. La función no tiene límite (discontinuidad por ausencia de límite).
2. Tiene límite, pero distinto del valor de la función en el punto considerado.

Por supuesto, para que esto tenga sentido, se supone que $x_{0}$ pertenece al intervalo.

Si bien no estudiaremos continuidad, ya podemos establecer su definición visto lo anterior:

**Definición**
> [!Continuidad]
> $f$ es continua en $I$ si es continua en todo punto $x_{0} \in I$.
> Es decir, si en todo punto de $I$, la función tiene límite, y el límite es igual al valor de la función en el mismo punto.

En realidad, tendríamos que desarrollar la definición de continuidad considerando la definición de límite, de modo que: una función es continua en $I$ si es continua en todo punto $x_{0} \in I$, $\forall \epsilon > 0 \dots$, etc.

Toda esta definición permite verificar que se corresponde con la idea de que es una función que no está "partida", siendo una formalización de dicha noción.
==El tener una formalización matemática completa nos permitirá verificar límites para funciones complejas==.

---
A continuación, veremos varios casos posibles de límites (con dibujos) antes de pasar a los ejemplos.
Los gráficos nos permiten predecir rápidamente si la misma tiene límite o no en un determinado punto.

1. Una función puede tener límite en un lugar, pero ser discontinua en otras partes (caso A).
2. Una función puede no tener límite en un punto dado, puesto que oscila infinitamente en el mismo, de modo que no hay forma de aproximarse a un valor. Ejemplo:
$$
f(x) = \begin{cases}
\begin{align}
&\sin \frac{1}{x} &&\text{si } &x \neq 0 \\
&42 &&\text{si } &x = 0
\end{align} 
\end{cases}
$$
3. Una función puede no tener límite en un punto, pero si puede tener límite por un lado y por el otro (izquierda y derecha).
![[Casos posibles de límites.png]]

---
Ahora, demostraremos a mano que algunas funciones conocidas tienen límite:

## Ejemplos
A continuación, estudiaremos diversas funciones y demostraremos su continuidad.

### Ejemplo 1 - Identidad
Sea $f(x) = x \qquad (x \in \mathbb{R})$

Entonces para todo $x_{0} \in \mathbb{R}$
$$
\lim_{ x \to x_{0} } f(x) = x_{0} \space \space (= f(x_{0}))
$$
De esta forma, sabemos que la función es continua en todo $x \in \mathbb{R}$. Lo demostraremos:
![[Ejemplo 1 en funciones conocidas.png]]
(Para demostrarlo, se nos brinda un $\epsilon$ que define una banda horizontal, y estableceremos un $\delta$ tal que la función se encuentre en los límites establecidos por dichas franjas. En este caso, elegimos $\delta = \epsilon$ por simetría. ==Cuando vamos a demostrar la existencia de un límite, se nos da un $\epsilon$ y nosotros establecemos $\delta$==).

Sea $\epsilon > 0$. Se define $\delta_{\epsilon} := \epsilon > 0$.

(Ahora, verificamos que la propiedad funciona (es una demostración trivial).
Para verificar si el valor de $\delta$ elegido es correcto, se nos da un $x$.)

Sea $x \in \mathbb{R}$ tal que $0 < |x - x_{0}| < \delta_{\epsilon}$
Tenemos que $|x - x_{0}| < \epsilon$ (por definición de $\delta$)
es decir $|f(x) - x_{0}| < \epsilon$

Aquí concluimos la demostración. Logramos demostrar que para todo $\epsilon > 0$, encontramos un valor de $\delta_{\epsilon}$ que cumple la implicación $0 < |x - x_{0}| < \delta_{\epsilon} \implies |f(x) - x_{0}| < \epsilon$, para todo $x$.
En el ejemplo $x_{0} = L$, por eso pusimos $x_{0}$ en la segunda parte de implicación.
Este es el ejemplo más sencillo de demostración de existencia de límite.

### Ejemplo 2 - Raíz cuadrada
Esta segunda demostración es bastante más complicada. En general, demostrar la existencia de límites a mano es bastante complicado. Para esto, existen una serie de teoremas que abordaremos posteriormente.

Sea $f : [0, +\infty) \to \mathbb{R}$ definida por $f(x) = \sqrt{ x }$ (para todo $x \geq 0$).

Entonces,
$$
\forall x_{0} \in \mathbb{R}, \lim_{ x \to x_{0} } f(x) = \sqrt{ x_{0} } \space \space (= f(x_{0}))
$$
![[Ejemplo 2 en funciones conocidas.png]]
Dividiremos la demostración en dos casos:

#### Caso $x_{0} = 0$ (sencillo)
![[Ejemplo 2 (caso 1) en funciones conocidas.png]]
(Para el valor de $\delta$, consideramos la siguiente idea: para encontrar la imagen de un valor $x$, hacemos $\sqrt{ x }$, entonces, para encontrar la preimagen de $y$, hacemos $y^{2}$. Entonces, establecemos $\delta = \epsilon^{2}$, ya que utilizamos la función inversa.)
==Ya que nuestro trabajo es asociar a todo $\epsilon$ un $\delta$, lo que tenemos que lograr es definir una función que a cada $\epsilon$, me asigna un $\delta_{\epsilon}$ ($\epsilon \mapsto \delta_{\epsilon}$)==.

Se define $\delta_{\epsilon} := \epsilon^{2} > 0 \qquad (\forall \epsilon > 0)$

Sea $x \in [0, +\infty)$ tal que $0 < |x - 0| < \delta_{\epsilon}$, es decir $0 < x < \epsilon^{2} \space \space (= \delta_{\epsilon})$
Entonces $0 < \sqrt{ x } < \sqrt{ \epsilon^{2} } = \epsilon$
Entonces $|\sqrt{ x } - 0| < \epsilon$

Como vemos llegamos a la definición de límite, puesto que desde $0 < |x - 0| < \delta_{\epsilon}$, llegamos a $|\sqrt{ x } - 0| < \epsilon$, que equivale a $|f(x) - L| < \epsilon$.

#### Caso $x_{0} > 0$
![[Ejemplo 2 (caso 2) en funciones conocidas.png]]
En este caso, nuestro objetivo es obtener la desigualdad $\sqrt{ x_{0} } - \epsilon < \sqrt{ x } < \sqrt{ x_{0} } + \epsilon$. Entonces, tenemos que definir un $\delta$ que funcione y confirme dicha desigualdad. De primeras, pensamos en $\epsilon^{2}$, aunque el problema radica en que no sabemos si $\sqrt{ x_{0} } - \epsilon$ puede ser negativo para dicho valor (y recordamos que estamos trabajando únicamente con los reales positivos).

Para evitar este problema, utilizaremos un $\epsilon$ más pequeño, con la idea de que si el razonamiento funciona para una precisión más fina, por más pequeña que sea, también funcionará para precisiones mayores. ==Esta es una práctica muy útil: $\epsilon$ siempre se puede achicar, pero nunca agrandar==.

Se definen $\epsilon' := mín(\epsilon, \sqrt{ x_{0} }) > 0$

De esta forma, cambiamos el enfoque objetivo: $\sqrt{ x_{0} } - \epsilon' < \sqrt{ x } < \sqrt{ x_{0} } + \epsilon'$
(Ahora, estamos seguros de que todos los valores son positivos o nulos, puesto que $\epsilon' \leq \epsilon$ y $\epsilon' \leq \sqrt{ x_{0} }$.)

La desigualdad es equivalente a $(\sqrt{ x_{0} } - \epsilon')^{2} < x < (\sqrt{ x_{0} } + \epsilon')^{2}$

Así, llegamos a una equivalencia lógica:
$$
\sqrt{ x_{0} } - \epsilon' < \sqrt{ x } < \sqrt{ x_{0} } + \epsilon' \Longleftrightarrow (\sqrt{ x_{0} } - \epsilon')^{2} < x < (\sqrt{ x_{0} } + \epsilon')^{2}
$$
De esta forma, obtuvimos el radio de seguridad ($\delta_{\epsilon}$).

Proseguimos con la definición:

Se definen $\epsilon' := mín(\epsilon, \sqrt{ x_{0} }) > 0$ y $\delta_{\epsilon} = min((\sqrt{ x_{0} } + \epsilon')^{2} - x_{0}, x_{0} - (\sqrt{ x_{0} } - \epsilon')^{2}) > 0$

Podemos ver que $\delta_{\epsilon}$ no es trivial. A continuación, verificamos que sea positivo (ambas partes son positivas): si sustituimos $x$ por $x_{0}$ en la desigualdad anterior, obtenemos una desigualdad obvia: $\sqrt{ x_{0} } - \epsilon' < \sqrt{ x_{0} } < \sqrt{ x_{0} } + \epsilon'$. Así, confirmamos que tanto $(\sqrt{ x_{0} } + \epsilon')^{2} - x_{0}$ como $x_{0} - (\sqrt{ x_{0} } - \epsilon')^{2}$ son positivos.

Verificamos que el valor de $\delta_{\epsilon}$ funciona bien:

Sea $x \in [0, +\infty)$ tal que $0 < |x - x_{0}| < \delta_{\epsilon}$

Sabemos que:
- $x < x_{0} + \delta_{\epsilon}$ (en base a la desigualdad anterior)
$$
x \leq x_{0} + ((\sqrt{ x_{0} } + \epsilon')^{2} - x_{0}) = (\sqrt{ x_{0} } + \epsilon')^{2}
$$
- $x > x_{0} - \delta_{\epsilon}$
$$
x \geq x_{0} - (x_{0} - (\sqrt{ x_{0} } - \epsilon')^{2}) = - (-(\sqrt{ x_{0} } - \epsilon')^{2}) = (\sqrt{ x_{0} } - \epsilon')^{2}
$$

Luego:
$$
(\sqrt{ x_{0} } - \epsilon')^{2} < x < (\sqrt{ x_{0} } + \epsilon')^{2}
$$
Ahora, como estamos seguros de que los tres valores son positivos o nulos, podemos tomar las raíces cuadradas de las tres partes (manteniendo la desigualdad):
$$
\sqrt{ x_{0} } - \epsilon' < \sqrt{ x } < \sqrt{ x_{0} } + \epsilon'
$$
Y esto nos dice que la distancia entre $\sqrt{ x }$ y $\sqrt{ x_{0} }$ es menor que $\epsilon'$. De esta forma, también es menor que $\epsilon$ (por construcción).
$$
\implies |\sqrt{ x } - \sqrt{ x_{0} }| < \epsilon' \leq \epsilon
$$
De esta forma concluimos la demostración, pues obtuvimos que $|f(x) - L| < \epsilon$ para todo $x \in [0, +\infty), |x - x_{0}| < \delta_{\epsilon}$.

Esta demostración, como otras demostraciones manuales sobre la existencia de límite en funciones (continuidad), es bastante compleja. Para facilitar esto, existen diferentes propiedades y teoremas que podemos utilizar a nuestro favor.

Antes de eso, repasaremos algunos ejemplos de funciones que no tienen límites (contraejemplos).

---
### Observación
Vimos que
$$
f(x) \underset{x \to x_{0}} \to L \Longleftrightarrow \forall \epsilon > 0, \exists \delta > 0, \forall x \in E^{*}(x_{0}, \delta), f(x) \in E(L, \epsilon)
$$
Entonces
$$
f(x) \cancel{ \underset{x \to x_{0}} \to } L \Longleftrightarrow \exists \epsilon > 0, \forall \delta > 0, \exists x \in E^{*}(x_{0}, \delta), |f(x) - L| \geq \epsilon
$$
En palabras: "Existe una precisión que no funciona: para cualquier radio, tendré un contraejemplo (un punto en el entorno reducido), tal que la distancia entre su imagen y el límite será mayor o igual a el radio correspondiente ($f(x)$ no pertenece al entorno de centro $L$ y radio $\epsilon$)".

En particular: $f$ no tiene límite en $x_{0} \in \overset{-} I$ si y solo si
$$
\forall L \in \mathbb{R}, \exists \epsilon > 0, \forall \delta > 0, \exists x \in E^{*}(x_{0}, \delta), |f(x) - L| \geq \epsilon
$$

---

A continuación, demostraremos que una función no tiene límite.

#### Contraejemplo:
$sgn: \mathbb{R} \to \mathbb{R}$ definida por $sgn(x) = \begin{cases} \begin{align} &1 &&\text{si} &x > 0 \\ &0 &&\text{si} &x = 0 \\ &-1 &&\text{si} &x < 0 \end{align} \end{cases}$
**Proposición**
La función signo no tiene límite en $x_{0} = 0$

Sabemos que la función signo tiene límite en todos los puntos de la recta $\mathbb{R}$, siendo el límite 1 para todos los valores positivos y -1 para todos los negativos. Sin embargo, no tiene límite en 0, cosa que demostraremos a continuación.
![[Contraejemplos en funciones conocidas.png]]

Se trata de demostrar que:
$$
\forall L \in \mathbb{R}, \exists \epsilon > 0, \forall \delta > 0, \exists x \in \mathbb{R}, 0 < |x| < \delta \underbrace{ \land }_{ \text{pero} } |sgn(x) - L| \geq \epsilon
$$
Entonces, tomaremos un $L$ cualquiera, construir un $\epsilon$, tomar un $\delta$ cualquiera, construir un $x$ en función de lo anterior, y verificar que todo funciona.

> [!Aclaración]
> Podríamos decir, en rasgos generales, que a la hora de demostrar algo, siempre tomamos un $a$ cualquiera cuando el enunciado que queremos demostrar dice $\forall a > 0$ (Sea $a \in \mathbb{R}$, por ejemplo), y construimos un valor $b$ cuando se especifica $\exists b > 0$ (en base a $a$, $b_{a} := \frac{a}{2}$, por ejemplo).

Sea $L \in \mathbb{R}$, se toma $\epsilon := 1$ (con los límites divididos, se toma la mitad de la distancia entre los límites). Sea $\delta > 0$ cualquiera

(Tenemos que construir $x$ a partir de los valores anteriores.)

Se distinguen 2 casos:
- $L \geq 0$. Se toma $x := -\frac{\delta}{2}$. Por construcción: $0 < |x| < \delta$
Pero $|sgn(x) - L| = |-1 - L| = |L + 1| = L + 1 \geq 1 = \epsilon$

- $L < 0$. Se toma $x := \frac{\delta}{2}$. Por construcción: $0 < |x| < \delta$
Pero $|sgn(x) - L| = |1 - L| = 1 - L > 1 = \epsilon$
(Recordemos que en este caso $L < 0$, por lo que $1 - L > 1$.)

(Para los contraejemplos, tomamos valores lejanos a $L$ (en este caso, entre 0 y $\delta$, sin poder ser ninguno de estos), por ejemplo, negativo (en este caso $-\frac{\delta}{2}$) si $L \geq 0$.)

(La distancia entre $L$ y la función aplicada a dicho valor es mayor que el $\epsilon$ elegido, lo que demuestra que la función no tiene límite, no es continua).

De esta forma, hallamos un contraejemplo, un valor de $\epsilon$ para el que todo $\delta$ desarrollamos un contraejemplo, lo que finaliza la demostración. Entonces, logramos demostrar que la función signo no tiene límite en 0.