En esta ocasión, comenzaremos con funciones continuas.
# Límites y continuidad
## Funciones continuas

> [!Recordatorio]
> Dado $f: I \to \mathbb{R}$, y $x_{0} \in \mathbb{R}$.
> $f$ es continua en $x_{0} \Longleftrightarrow \lim_{ x \to x_{0} } f(x) = f(x_{0})$
> $$
> \begin{align}
> &\Longleftrightarrow \forall \epsilon > 0, \exists \delta > 0, \forall x \in E^{*}(x_{0}, \delta) \cap I, f(x) \in E(f(x_{0}), \epsilon) \\
>  \\
> 
> &\Longleftrightarrow \forall \epsilon > 0, \exists \delta > 0, \forall x \in I, 0 < |x - x_{0}| < \delta \implies |f(x) - f(x_{0})| < \epsilon
> \end{align}
> $$

Observación

Para todos $\epsilon > 0$ y $\delta > 0$, los enunciados
$$
\forall x \in E^{*}(x_{0}, \delta) \cap I, f(x) \in E(f(x_{0}), \epsilon)
$$
y
$$
\forall x \in E(x_{0}, \delta) \cap I, f(x) \in E(f(x_{0}), \epsilon)
$$
son equivalentes.

Esto es así cuando trabajamos con funciones continuas, puesto que sabemos que en el caso $x = x_{0}$, la condición $f(x) \in E(f(x_{0}), \epsilon)$ también se cumple, por lo que podemos considerar el entorno lleno en lugar del reducido.
El considerar el entorno reducido viene de la idea de que la imagen en un punto específico no afecta al valor del límite, por lo que únicamente analizamos lo que ocurre alrededor de $x_{0}$.

Sin embargo, consideraremos la segunda formulación al trabajar con funciones continuas ya que es más simple.

> [!Función continua]
> Una función $f: I \to \mathbb{R}$ es continua en $I$ cuando es continua en cada punto $x_{0} \in I$.
> 
> Formalmente:
> $f$ continua en $I$
> $$
> \begin{align}
> &\Longleftrightarrow \forall x_{0} \in I, \lim_{ x \to x_{0} } f(x) = f(x_{0}) \\
>  \\
> 
> &\Longleftrightarrow \forall x_{0} \in I, \forall \epsilon > 0, \exists \delta > 0, \forall x \in E(x_{0}, \delta) \cap I, f(x) \in E(f(x_{0}), \epsilon) \\
>  \\
> 
> &\Longleftrightarrow \forall x_{0} \in I, \forall \epsilon > 0, \exists \delta > 0, \forall x \in I, 0 < |x - x_{0}| < \delta, |f(x) - f(x_{0})| < \epsilon
> \end{align}
> $$

Podemos intercambiar el orden de los cuantificadores iguales que estén seguidos, en este caso:
$$
\forall x_{0} \in I, \forall \epsilon > 0, \dots = \forall \epsilon > 0, \forall x_{0} \in I, \dots
$$
No se pueden intercambiar el orden cuantificadores diferentes (o al menos la definición obtenida no es equivalente).

En este caso, si escribimos:
$$
\forall \epsilon > 0, \exists \delta > 0, \forall x_{0} \in I, \forall x \in I, 0 < |x - x_{0}| < \delta, |f(x) - f(x_{0})| < \epsilon
$$
obtenemos la definición de continuidad uniforme (que no es equivalente a la definición de continuidad).

Por esta razón, es fundamental ser cuidadosos cuando manipulamos definiciones de este tipo.

La noción de continuidad es super intuitiva: una función que no está "separada en partes", "se puede dibujar sin levantar la mano". El problema es que esto es una intuición, no una definición, por lo que no puede ser utilizada en teoremas.
Se trabajó mucho a lo largo de la historia para llegar a la definición mencionada anteriormente, la cual tiene su complejidad, por lo que pasaremos el resto del curso verificando que dicha definición cumple con las intuiciones de continuidad.

---
## Propiedades algebraicas

- Las funciones constantes son continuas.
- La función identidad $x \mapsto x$ es continua.
- La función raíz cuadrada $x \mapsto \sqrt{ x }$ es continua en $[0, + \infty)$.
- La función logaritmo es continua en $(0, + \infty)$.

### Proposición

> [!Proposición]
> Si $f, g : I \to \mathbb{R}$ son continuas, entonces las funciones $f + g$, $f - g$ y $fg$ son continuas.
> 
> Además, si $g$ nunca se anula en $I$, entonces $\frac{f}{g}$ también es continua.

Esto se demuestra en base a la definición de función continua: en cada punto tiene como límite el valor en ese punto. Por esta razón se deducen los teoremas de suma, resta, producto y límite.

Gracias a este teorema, es posible construir todos los polinomios, fracciones racionales, y son todos funciones continuas.

> [!Corolario]
> Así: todos los polinomios son funciones continuas en $\mathbb{R}$.
> Y toda fracción racional $f(x) = \frac{p(x)}{q(x)}$ (siendo $p(x)$ y $q(x)$ polinomios) es continua en todo intervalo $I$ donde $q(x)$ no se anula.

---
A continuación, vemos el teorema, que es otra proposición:

### Proposición

> [!Proposición]
> Si $f : I \to \mathbb{R}$ y $g : I \to \mathbb{R}$ son continuas y tales que $f(I) \subset J$, entonces $g \circ f : I \to \mathbb{R}$ es continua.

Esto se fundamenta en base al teorema de composición de límites.

En definitiva, esto establece que si tengo una función construida a partir de una expresión que solo involucra las funciones de base, más resta, producto, cociente y compuesta, al final obtenemos una función continua en un intervalo donde está definida.

#### Ejemplo
$$
f(x) = \frac{\log(\sqrt{ x^{2} + 5 } - 3x^{3} + 5x^{6})}{\sqrt{ \sqrt{ \sqrt{ \log(\log(x^{8})) } } }}
$$
No sabemos en qué intervalo está definida la función anterior, tendríamos que estudiarla para saberlo. Sin embargo, podemos asegurar con certeza que en el intervalo en el que esté definida, la función es continua, puesto que es una mezcla de composición, y tanto el numerador como el denominador son continuos.

==Es así que podemos establecer que, en general, cualquier expresión que se puede escribir con un único caso ($f(x) = \dots$, y no $f(x) = \begin{cases}\dots \\ \dots \end{cases}$), a partir de las funciones de base, será una función continua==.

---
## Valores intermedios


Intuitivamente, una función es continua cuando no está separada por partes. De esta forma, podemos decir que cuando una función es continua, en el eje y, tiene que pasar por todos los valores intermedios. Por ejemplo, si la función es continua y tiene tanto valores positivos como negativos, tiene que cortar al eje x en al menos un punto (en caso de tener tres dimensiones, es posible esquivarlo, aunque no analizaremos este caso).
También es posible que una función tenga tanto valores positivos como negativos en su codominio, pero no sea continua, de forma que contenga saltos intermedios, pudiendo no cortar al eje x en ningún punto.
![[1 - Valores intermedios.png]]

De igual forma, por muy obvio e intuitivo que sea, hay que demostrarlo.

Lo anterior es el teorema de Bolzano: si tengo una función continua entre $a$ y $b$, tal que $f(a) < 0$ y $f(b) > 0$, entonces existe al menos un punto $c$ entre $a$ y $b$, tal que $f(c) = 0$.

Antes de demostrar el teorema, estudiaremos un lema.

### Lema

> [!Lema]
> Sea $f : I \to \mathbb{R}$ continua, y $x_{0} \in I$ cualquiera.
> 1. Si $f(x_{0}) > 0$, entonces $\exists \delta > 0, \forall x \in E(x_{0}, \delta), f(x) > 0$
> 2. Si $f(x_{0}) < 0$, entonces $\exists \delta > 0, \forall x \in E(x_{0}, \delta), f(x) < 0$

(Si $f$ es continua, podemos hallar un radio, por más pequeño que sea, alrededor de $x_{0}$, donde todas las imágenes son positivas o negativas, dependiendo del valor de $f(x_{0})$.)

Demostraremos solo una de las dos, ya que son análogas

#### Demostración - 1
Supongamos que $f(x_{0}) > 0$.
Sea $\epsilon := f(x_{0}) > 0$.
Como $\lim_{ x \to x_{0} } f(x) = f(x_{0})$ existe $\delta > 0$ (asociado a $\epsilon$) tal que
$$
\forall x \in E(x_{0}, \delta) \cap I, |f(x) - f(x_{0})| < \underbrace{ \epsilon }_{ f(x_{0}) }
$$
En particular, para todo $x \in E(x_{0}, \delta)$ tenemos que $f(x) - f(x_{0}) > -f(x_{0})$

Ahora, podemos simplificar por $f(x_{0})$:
$$
f(x) - \cancel{ f(x_{0}) } > \cancel{ -f(x_{0}) } \implies f(x) > 0
$$
Así concluimos la demostración. Para todo $x$ en el entorno especificado, $f(x) > 0$.

Básicamente, nos aseguramos un entorno en el que para todo x, $f(x) > 0$. Para esto, especificamos $\epsilon := f(x_{0}) > 0$, sabiendo por la definición de límite que existe un $\delta$ que satisface la propiedad deseada.
De esta manera, sabemos que la función se queda en la banda horizontal, que como está en la parte positiva, deducimos que la función es positiva en dicha banda

Utilizamos la propiedad de valor absoluto:
$$
|a| < \epsilon \Longleftrightarrow - \epsilon < a < \epsilon
$$

La demostración del punto 2 es análoga.

---
Ahora, podemos probar y demostrar el teorema de Bolzano, uno de los teoremas fundamentales de continuidad.

## Teorema (Bolzano)

Si $f : [a, b] \to \mathbb{R}$ es continua y tal que $f(a)$ y $f(b)$ tienen distinto signo (no nulos), entonces existe $c \in [a, b]$ tal que $f(c) = 0$.

Esto no significa que haya un único $c$, simplemente se especifica que siempre hay al menos uno (pudiendo haber más).

### Demostración
Habría que considerar dos casos:
1. $f(a) > 0$ y $f(b) < 0$
2. $f(a) < 0$ y $f(b) > 0$

Únicamente desarrollaremos uno, ya que son simétricos.

Supongamos que $f(a) < 0$ y $f(b) > 0$.
Se define el conjunto
$$
A := \{ x \in [a, b] : f(x) < 0 \}
$$
Ejemplo en la figura anterior:
![[2 - Conjunto A.png]]

$A \neq \emptyset$, pues $a \in A$. $A$ está acotado por $a$ y $b$.

(Aplicando el axioma de completitud, como $A$ está acotado superiormente (por $b$), entonces tiene supremo.)

Sea $c := sup(A) (\in [a, b])$
(El último punto donde la función se anula.)

(Ahora, tenemos que demostrar que $f(c) = 0$ para el $c$ especificado. Lo demostraremos por el absurdo.)

Supongamos (por el absurdo) que $f(c) \neq 0$.
Se distinguen 2 casos:

1. $f(c) < 0$. En este caso, tenemos que $c < b$ (pues $f(b) > 0$).
Por el lema, existe $\delta > 0$ tal que $f(x) < 0$ para todo $x \in E(c, \delta) \cap [a, b]$.
Sea $x = mín\left( c + \frac{\delta}{2}, b \right)$ (así impedimos que $x$ se salga de $[a, b]$ en caso de que $\delta$ sea demasiado grande).

Por construcción, tenemos que $E(x_{0}, \delta) \cap [a, b]$. Entonces $f(x) < 0$.
Entonces $x \in A$, entonces $x \leq c = sup(A)$.

Contradicción, pues por construcción $x > c$ (ya que $x = mín\left( c + \frac{\delta}{2}, b \right)$, dos valores mayores que $c$).

Ahora, veremos que tampoco puede ser positivo.

2. $f(c) > 0$. En este caso, tenemos que $c > a$ (pues $f(a) < 0$).
Por el lema, existe $\delta > 0$ tal que $f(x) > 0$ para todo $x \in E(c, \delta) \cap [a, b]$

Como $c = sup(A)$ existe $x \in A$ tal que
$$
máx(a, c - \delta) < x \leq c
$$
(De esta forma, sabemos que el máximo siempre será menor que c.)
(Es así que podemos usar el principio de aproximación al supremo, sabiendo que existe un elemento de $A$, aproximación a menos de $\epsilon$, donde $\epsilon$ es la distancia entre $c$ y $máx(a, c - \delta)$).

Por construcción: $x \in E(c, \delta) \cap [a, b]$.
Entonces: $f(x) > 0$
Y como $x \in A$, tenemos que $f(x) < 0$.

De esta forma llegamos a otra contradicción, es imposible que para un mismo $x$, $f(x) > 0$ y $f(x) < 0$.

Como demostramos que $f(c) \not > 0$ y $f(c) \not < 0$, podemos concluir que $f(x) = 0$.
Es así que gracias al lema y al axioma de completitud, logramos demostrar el Teorema de Bolzano.

Es la misma técnica de demostración que utilizamos para demostrar la existencia de $\sqrt{ 2 }$

Algo importante a considerar es que la demostración del absurdo para $f(c) > 0$ no es idéntica a la de $f(c) < 0$. Esto es así, ya que toda la demostración se fundamenta en torno a un conjunto $A$ que contiene todos los $x$ para los que $f(x) < 0$, por lo que se facilita el caso $f(c) < 0$, no se toman de forma simétrica los positivos y negativos.

---
Ahora, veremos varios corolarios que son consecuencia de lo anterior.

## Corolario - Teorema de los valores intermedios
Sea $f : [a, b] \to \mathbb{R}$ una función continua y $\lambda \in \mathbb{R}$ un valor intermedio entre $f(a)$ y $f(b)$.
(Es decir: $f(a) \leq \lambda \leq f(b)$ o bien $f(b) \leq \lambda \leq f(a)$)

Entonces existe $c \in [a, b]$ tal que $f(c) = \lambda$.
![[3 - Teorema de los valores intermedios.png]]

Es decir, si $f$ es continua en $[a, b]$, entonces toma todos los valores entre $f(a)$ y $f(b)$ al menos una vez.

### Demostración
En el caos donde $\lambda = f(a)$ o $\lambda = f(b)$ basta con tomar $c := a$ o $c := b$ (casos triviales).

Ahora, se supone que o bien $f(a) < \lambda < f(b)$ o bien $f(b) < \lambda < f(a)$.

Se considera 
$$
g(x) = f(x) - \lambda
$$
La función $g$ cumple las hipótesis del teorema de Bolzano (sabemos que $g$ es continua, pues esta construida a partir de una función continua menos una constante, y $f(a)$ o $f(b)$ será negativo (el menor de estos dos), y el otro será positivo, de forma que $\lambda$ será 0. Todo esto se da por traslación.)

Entonces existe $c \in [a, b]$ tal que $g(c) = 0$, es decir: $f(x) = \lambda$.

El teorema de los valores intermedios es igual al teorema de Bolzano, pero generalizado.

---
Ahora, veremos aplicaciones del teorema de los valores intermedios.

## Aplicaciones
1. $f(x) = x^{2}$
$$
\begin{align}
&f(0) = 0 \\
&f(2) = 4
\end{align}
$$
$\exists c \in [0, 2]$ tal que $f(x) = 2 \qquad (c := \sqrt{ 2 }$

(Como es continua, $f$ en el intervalo $[0, 2]$ tiene que pasar por todos los valores entre 0 y 4, específicamente 2 (demostrando la existencia de la $\sqrt{ 2 }$).)

Además de este uso (demostrar la existencia de valores), nos permite invertir muchas funciones.

2. $f(x) = \log(x)$ en $(0, + \infty)$
Ya vimos que $\lim_{ x \to + \infty } \log(x) = + \infty$.
Entonces existe un $x_{0} > 1$ tal que $\log(x_{0}) \geq 2$.
Tenemos que
$$
\begin{align}
&f(0) = 0 \\
&f(x_{0}) \geq 2
\end{align}
$$
Por el teorema de los valores intermedios, existe $e \in \mathbb{R}$ tal que $\log(e) = 1$.
Además, como es estrictamente creciente, este valor es único.

Así, en base al teorema de los valores intermedios, demostramos que, considerando la continuidad de la función, sabiendo que hay una imagen de valor $a$ y otra de valor $b$, existirán imágenes que tomarán todos los valores intermedios.

La existencia de muchos otros valores se hace de esta misma forma, las funciones adecuadas y el teorema correspondiente. De esta forma, es una herramienta fundamental para construir y demostrar la existencia de muchos números.