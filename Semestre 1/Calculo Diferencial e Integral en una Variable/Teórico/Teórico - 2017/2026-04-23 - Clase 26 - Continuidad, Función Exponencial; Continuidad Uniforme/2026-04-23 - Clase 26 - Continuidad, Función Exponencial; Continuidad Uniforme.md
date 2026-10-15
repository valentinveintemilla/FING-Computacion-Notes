# Límites y continuidad

## Funciones inversas
Recordamos la proposición vista la clase pasada:

> [!Proposición]
> $f: I \to \mathbb{R}$ continua estrictamente creciente (o decreciente), entonces define una biyección entre $I$ y su imagen $J := f(I)$.
> 
> Además, la función inversa $f^{-1} : J \to I$ es continua y estrictamente creciente (o decreciente).

Ya sabíamos que la imagen de un intervalo por una función continua es un intervalo, gracias al teorema de Bolzano. Sin embargo, ahora que manejamos una función estrictamente creciente (o decreciente), además de ser biyectiva, su inversa es continua y estrictamente creciente (o decreciente).

==Aclaración: La idea fundamental del teorema sobre funciones continuas estrictamente crecientes (o decrecientes), es adaptarse al intercambio entre el conjunto de partida y el conjunto de llegada==.

![[1 - Funciones inversas.png]]
==Aclaración: es la simétrica con respecto a la diagonal==.

También vimos un ejemplo: las raíces n-ésimas, siendo las inversas de las funciones $x^{n}$.

Continuaremos estudiando la función exponencial:

### Ejemplo
Sea $\log : R^{+} \to \mathbb{R}$

Tenemos que
$$
\begin{align}
&\lim_{ x \to 0^{+} }  \log x = - \infty \\
&\lim_{ x \to + \infty }  \log x = + \infty
\end{align}
$$
Entonces:
$$
\log(\mathbb{R}^{+}) = \mathbb{R}
$$

Como el logaritmo es una función que es continua en todos sus puntos, es estrictamente creciente y esta dada por un intervalo (en este caso, de 0 - sin incluirlo - a $+ \infty$). Por esta razón, sabemos que su imagen está dada por el límite en $0^{+}$ y $+ \infty$, de esta forma: $\log (\mathbb{R}^{+}) = \mathbb{R}$.

Gracias a todo esto, podemos invertir la función:
Se escribe:
$$
\exp := \log^{-1} : \mathbb{R} \to \mathbb{R}^{+}
$$

Podemos describir sus límites considerando los límites de logaritmo:
$$
\begin{align}
&\lim_{ x \to - \infty }  \log x = 0 \\
&\lim_{ x \to + \infty }  \log x = + \infty
\end{align}
$$
Además, gracias al teorema sabemos que es continua, estrictamente creciente, y biyectiva.

![[2 - Función logaritmo.png]]

Sabemos que el logaritmo tiene la propiedad de transformar el producto en suma:
$$
\log(xy) = \log(x) + \log(y)
$$

De esta forma, la función exponencial hace lo contrario:

---
### Función exponencial

> [!Propiedades de la función exponencial]
> $$
> \exp(x + y) = \exp(x) \times \exp(y)
> $$
> Para demostrar esto, haremos lo siguiente:
> $$
> \begin{align}
> \log(\exp(x + y)) = x + y &= \log(\exp(x)) + \log(\exp(y)) \\
> &= \log(\exp(x) \times \exp(y)) \\
> \end{align}
> $$
> $$
> \implies \exp(x + y) = \exp(x) \times \exp(y)
> $$
> De esta forma, llegamos a la conclusión de que $\exp(x + y) = \exp(x) \times \exp(y)$ en base a que la función logaritmo es inyectiva, por lo que si $\log(x) = \log(y) \implies x = y$.
> 
> A partir de esto podemos deducir otras propiedades fundamentales de la exponencial:
> $$
> \exp(-1) = \frac{1}{\exp(x)}
> $$
> $$
> \exp(0) = 1
> $$
> 

También se define una constante:

> [!Definición]
> Sea
> $$
> e := \exp(1) \simeq 2,71828\dots \qquad (\not \in \mathbb{Q})
> $$

La dificultad de demostrar la irracionalidad de $e$ radica en que no es solución de ningún polinomio con coeficientes enteros (caso contrario a $\sqrt{ 2 }$). Sucede lo mismo con $\pi$.

> [!Proposición]
> $$
> \exp n = \exp(\underbrace{ 1 + \dots + 1 }_{ n }) = \underbrace{ e \times \dots \times e }_{ n } = e^{n}
> $$
> De esta forma, la exponencial de $n$ es $e^{n}$.
> 
> Por analogía, se escribe (extendido a los reales)
> $$
> e^{x} := \exp(x)
> $$

Esto se justifica considerando las propiedades fundamentales del exponente:
Proposición:

> [!Propiedades del exponente]
> $$
> e^{x + y} = e^{x} e^{y}
> $$
> $$
> e^{0} = 1
> $$
> $$
> e^{-x} = \frac{1}{e^{x}}
> $$

Esto nos permite extender la potencia a todos (o casi todos) los reales.

---
### Potencia
$$
\begin{align}
&x \in \mathbb{R}, &&n \in \mathbb{N} &&\rightsquigarrow x^{n} = \overbrace{ x \times \dots \times x }^{ n } \\
&x \neq 0, &&n \in \mathbb{Z}^{-} &&\rightsquigarrow x^{n} = \frac{1}{x^{-n}} \\
&x > 0, &&y \in \mathbb{R}, &&\rightsquigarrow \underbrace{ x^{y} := e^{y \log x} }_{ \text{Potencia generalizada} }
\end{align}
$$
Por convención, $0^{0} = 1$, y en general $x^{0} = 1$.

En el segundo punto, verificamos que $x \neq 0$ por la división (ya que analizamos el caso para $n < 0$, que es el que nos interesa).

En el tercer punto, tomamos $x > 0$ puesto que $\log x$ solo está definido en dicho caso.

Podemos manejar las propiedades usuales de potencia en los tres casos.

Básicamente, enunciamos tres definiciones de potencia que no tienen el mismo dominio, pero cuando trabajamos en el mismo dominio, coinciden, razón por la cual no se introduce otra notación (puesto que terminamos calculando el mismo número de tres formas distintas).

---
A continuación, enunciaremos un teorema:

## Funciones definidas a partir de integrales

En esta sección, demostraremos la primera parte (parte continua) del teorema fundamental.

> [!Proposición]
> Si $f : I \to \mathbb{R}$ es localmente integrable y $a \in I$, entonces la función $F : I \to \mathbb{R}$
> definida por
> $$
> F(x) = \int_{a}^{x} f(t) dt
> $$
> siempre es continua.

Se fija uno de los extremos ($a$), y el otro es el extremo variable ($x$).

==De esta forma, la integral es algo que regulariza la función, siempre es continua sin importar la función localmente integrable de la que partimos==.

(Si además, partimos de una función continua, obtendremos una función derivable, siendo su derivada la función original. Sin embargo, esto será abordado más adelante.)

Recordemos que ==localmente integrable significa que la función es integrable en cualquier intervalo cerrado formado a partir del intervalo de entrada==. Cuando el intervalo de entrada es cerrado, es equivalente a decir que es integrable.

### Demostración

Sea $x_{0} \in I$.
Como $f$ es localmente integrable, está acotada en el entorno de $x_{0}$, y existen $\delta > 0$ y $M \geq 0$ tales que
$$
\forall x \in E(x_{0}, \delta), |f(x)| \leq M
$$
Para todo $x \in E(x_{0}, \delta)$:
$$
|F(x) - F(x_{0})| = \left| \int_{a}^{x} f - \int_{a}^{x_{0}} f \right| = \left| \int_{x_{0}}^{x} f \right|
$$
$$
\leq \int_{mín(x_{0}, x)}^{máx(x_{0}, x)} |f| \leq M \cdot |x - x_{0}| \underbrace{ \longrightarrow }_{ x \to x_{0} } 0
$$
Por el sándwich:
$$
|F(x) - F(x_{0})| \underbrace{ \longrightarrow }_{ x \to x_{0} } 0
$$
Equivale a decir que:
$$
F(x) \underbrace{ \longrightarrow }_{ x \to x_{0} } F(x_{0})
$$
De esta forma, demostramos que la función es continua en el punto $x_{0}$, reafirmando las proposiciones sobre las funciones definidas a partir de integrales.

Esto aplica, por ejemplo, para el logaritmo, función definida a partir de una integral, por lo que demostramos la continuidad del logaritmo.

Otro ejemplo de función localmente integrable es
$$
f(t) = \frac{1}{1 + t^{2}}
$$
De esta forma, es integrable en general.

Por esta razón, podemos definir:
$$
F(x) = \int_{0}^{x} \frac{1}{1 + t^{2}} \space dt
$$
![[3 - Función arctang.png]]

De esta forma, se define una de las funciones trigonométricas. Si yo tomo la inversa de $\arctan$, obtengo $\tan$.

---
Pasaremos al siguiente tema:
# Continuidad uniforme
Sobre la demostración de la continuidad de una función, generalmente trabajamos con la lógica de:
$$
\epsilon \mapsto \delta_{\epsilon}
$$
Esta función no es única, puesto que siempre puedo reducir el radio, y seguirá funcionando. Sin embargo, en la mayoría de los casos existe un valor máximo para $\delta_{\epsilon}$. Veremos un ejemplo para determinar cual sería el valor máximo:

## Ejemplo
Sea $f : \mathbb{R} \to \mathbb{R}$ definida por $f(x) = x^{2}$.
Sean $x_{0} > 0$ y $\epsilon > 0$ tal que $\epsilon \leq x_{0}^{2}$.
Determinar el máximo $\delta > 0$ tal que
$$
\forall x \in \mathbb{R^{+}}, |x - x_{0}| < \delta \implies |x^{2} - x_{0}^{2}| < \epsilon
$$
(Podemos sustituir $|f(x) - f(x_{0})|$ por $|x^{2} - x_{0}^{2}|$.)

Haremos una figura para visualizar el problema:
![[4 - Continuidad uniforme x a la 2.png]]
$$
\begin{align}
|x^{2} - x_{0}^{2}| < \epsilon &\Longleftrightarrow x_{0}^{2} - \epsilon < x^{2} < x_{0}^{2} + \epsilon \\
&\Longleftrightarrow \sqrt{ x_{0}^{2} - \epsilon } < x < \sqrt{ x_{0}^{2} + \epsilon }
\end{align}
$$
$\delta > 0$ debe cumplir dos desigualdades:
$$
\begin{align}
&\delta \leq x_{0} - \sqrt{ x_{0}^{2} - \epsilon } \\
&\delta \leq \sqrt{ x_{0}^{2} + \epsilon } - x_{0} \leftarrow \text{más restrictiva}
\end{align}
$$
Como hay uno que es menor que el otro, una condición es más restrictiva, en este caso: $\sqrt{ x_{0}^{2} + \epsilon } - x_{0}$ (no lo demostraremos).

De esta manera, se deduce que es máximo radio que podemos usar.

El máximo radio es $\delta := \sqrt{ x_{0}^{2} + \epsilon } - x_{0}$

Aquí, podemos ver que $\delta$ no solo depende de $\epsilon$, sino también de $x_{0}$. Este es un fenómeno común.

> [!Moraleja]
> $\delta$ depende de $\epsilon$ y de $x_{0}$.

Sin embargo, pueden existir casos, como cuando demostramos la continuidad en un punto determinado, en el que queremos encontrar un $\delta$ que dependa de $\epsilon$ (casi todos los casos), pero no de $x_{0}$. En este caso, si se cambia el punto, seguramente el $\delta$ no funcione.

Esto es la continuidad uniforme, una condición más restrictiva de continuidad regular, la cual es igual, pero en la cual $\delta$ no puede depender de $x_{0}$, solo de $\epsilon$.

## Definición

> [!Continuidad uniforme]
> Una función $f : I \to \mathbb{R}$ es uniformemente continua en $I$ cuando:
> $$
> \forall \epsilon > 0, \exists \delta > 0, \forall x, x' \in  I, |x - x'| < \delta \implies |f(x) - f(x')| < \epsilon
> $$

Es más exigente, ya que $\delta$ solo depende de $\epsilon$ y no más de $x_{0}$.

Son bastante similares, por lo que hay que ser cuidadosos a la hora de manipular los conceptos.

## Proposición

> [!Proposición]
> Toda función uniformemente continua es continua.

### Demostración
$f$ uniformemente continua
$$
\Longleftrightarrow \forall \epsilon > 0, \exists \epsilon > 0, \forall x, x' \in I, |x - x'| < \delta \implies |f(x) - f(x')| < \epsilon
$$
Si tenemos un $\dots, \exists \dots, \forall \dots, \dots$, podemos intercambiarlo, sabiendo que la recíproca no se cumple.
$$
\begin{align}
&\exists \forall \qquad \text{existe un algo para todos} \\
&\forall \exists \qquad \text{todos tienen uno (no es el mismo)}
\end{align}
$$
$$
\Longrightarrow \forall \epsilon > 0, \forall x \in I , \exists \epsilon > 0, \forall x' \in I, |x - x'| < \delta \implies |f(x) - f(x')| < \epsilon
$$
Ahora, como tenemos $\forall\dots, \forall\dots$, podemos intercambiarlos sin problema:
$$
\Longleftrightarrow \forall x \in I, \forall \epsilon > 0, \exists \epsilon > 0, \forall x' \in I, |x - x'| < \delta \implies |f(x) - f(x')| < \epsilon
$$De esta forma, llegamos a la definición de continuidad, demostrando que la fórmula de continuidad uniforme es más fuerte (implica a la continuidad regular).

Para demostrar que no son equivalentes:

### Contraejemplo
$$
f(x) = x^{2} \text{ en } \mathbb{R}
$$
Supongamos que $f(x) = x^{2}$ es uniformemente continua en $\mathbb{R}$.
Esto quiere decir que fijado $\epsilon > 0, \exists \delta > 0, \forall x, x' \in I, |x - x'| < \delta \implies |x^{2} - x'^{2}| < \epsilon$

Fijado $x > 0$, tenemos que
$$
\forall x' \in \mathbb{R}, |x' - x| < \delta \implies |x^{2} - x'^{2}| < \epsilon
$$
Entonces, tenemos que $\delta \leq \sqrt{ x^{2} + \epsilon } - x \qquad \forall x$

Simplificamos la expresión:
$$
\begin{align}
\delta \leq \sqrt{ x^{2} + \epsilon } - x &= \frac{(\sqrt{ x^{2} + \epsilon } - x)(\sqrt{ x^{2} + \epsilon } + x)}{\sqrt{ x^{2} + \epsilon } + x } \\
&= \frac{(x^{2} + \epsilon) - x^{2}}{\sqrt{ x^{2} + \epsilon } + x } \\
&= \underbrace{ \frac{\epsilon}{\sqrt{ x^{2} + \epsilon } + x } }_{ \underset{x \to + \infty} \longrightarrow 0 }
\end{align}
$$
Cuando $x \to \infty$, $\epsilon$ es fijo, por lo que todo tiende a 0.

Como $\delta$ tampoco cambia, podemos determinar que $\delta \leq 0$.

Esto es una contradicción, pues supusimos que $\delta > 0$.

La intuición nos dice que la noción de continuidad uniforme se relaciona con la idea de pendiente más empinada, pues para obtener una misma ventana vertical, se requiere una ventana horizontal más pequeña.

Por ejemplo, en el caso de la raíz cuadrada:
Cuando trabajamos con $x \to + \infty$ no tendremos problema, ya que como la pendiente es cada vez más baja, para la misma ventana de $\epsilon$, podremos tomar un radio más grande, por lo tanto un radio menor siempre nos servirá. De esta manera, tendremos problemas para hacer lo mismo cuando $x \to 0$.
Sin embargo, esto no es así, ya que analizamos intervalos finitos. Por lo tanto, no hay que dejarse llevar por esa intuición.

Demostramos que una función continua no tiene porque ser uniformemente continua con el ejemplo más sencillo: $f(x) = x^{2}$. Sin embargo, la función identidad, $g(x) = x$ sí es uniformemente continua.

Esto nos demuestra que la propiedad de uniformemente continua no se extiende entre el producto de funciones, puesto que $f(x) = x^{2} = x \times x = g(x) \cdot g(x)$.

La suma y la resta si extienden dicha propiedad.

---
Analizando el caso de la función $x^{2}$, podemos enunciar un nuevo teorema.

En general, tenemos que
$$
\begin{align}
\text{Continuidad uniforme} &\implies \text{Continuidad} \\
&\not \Longleftarrow
\end{align}
$$
Pero, cuando el intervalo es de la forma $[a, b]$, entonces ambas definiciones son equivalentes.

Considerando esto, podemos analizar una función continua que no es uniformemente continua por partes, y será uniformemente continua en cada parte.

## Teorema de Heine-Cantor

> [!Teorema de Heine-Cantor]
> Toda función continua en un intervalo cerrado $[a, b]$ es uniformemente continua en $[a, b]$.

Lo demostraremos en próximas clases.