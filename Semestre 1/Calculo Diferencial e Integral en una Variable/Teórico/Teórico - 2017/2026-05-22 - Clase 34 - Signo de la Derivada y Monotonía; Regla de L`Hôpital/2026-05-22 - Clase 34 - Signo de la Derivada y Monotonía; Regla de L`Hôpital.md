# Derivadas
Repasamos los temas abordados la clase pasada:

## Lema de Rolle

> [!Lema de Rolle]
> - $f$ continua en $[a, b]$ y derivable en $(a, b)$
> - $f(a) = f(b)$
> 
> Entonces existe $c \in (a, b)$ tal que $f'(c) = 0$.

![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-05-22 - Clase 34 - Signo de la Derivada y Monotonía; Regla de L`Hôpital/Imágenes/1 - Lema de Rolle.png]]

## Teorema del valor medio de Lagrange
También vimos la generalización del lema de Rolle:

> [!Teorema del valor medio de Lagrange]
> $f$ continua en $[a, b]$ y derivable en $(a, b)$:
> 
> Entonces, existe $c \in (a, b)$ tal que
> $$
> f'(c) = \frac{f(b) - f(a)}{b - a}
> $$

![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-05-22 - Clase 34 - Signo de la Derivada y Monotonía; Regla de L`Hôpital/Imágenes/2 - Teorema de Lagrange.png]]

La interpretación física es que el cociente anterior mide la velocidad promedio de la función entre los puntos $a$ y $b$. Durante el recorrido entre los puntos mencionados, el teorema enuncia que al menos un punto del intervalo alcanzó dicha velocidad (al menos un punto tiene pendiente equivalente a la velocidad promedio).

De dicho teorema, surgen algunas proposiciones:

### Proposiciones

> [!Proposición]
> Si $f$ es continua en $[a, b]$ y derivable en $(a, b)$:
> $$
> \begin{align}
> &\text{(1)} && (\forall x \in (a, b), f'(x) \geq 0) \Longleftrightarrow f \text{ monótona creciente} \\
> &\text{(2)} && (\forall x \in (a, b), f'(x) \leq 0) \Longleftrightarrow f \text{ monótona decreciente} \\
> &\text{(3)} && (\forall x \in (a, b), f'(x) = 0) \Longleftrightarrow f \text{ constante}
> \end{align}
> $$

Vimos que bastaba con demostrar el punto (1), aplicando Lagrange, siendo (2) equivalente, únicamente cambiando el signo de la función (pasando a ser monótona decreciente). El punto (3) es la conjunción de los puntos (1) y (2).

También tenemos las desigualdades estrictas, aunque en este caso, solo son implicaciones, no equivalencias (como el caso anterior). Por esta razón, las recíprocas no se cumplen.

> [!Proposición]
> Si $f$ es continua en $[a, b]$ y derivable en $(a, b)$:
> $$
> \begin{align}
> &\text{(1)} && (\forall x \in (a, b), f'(x) > 0) \implies f \text{ estrictamente creciente} \\
> &\text{(2)} && (\forall x \in (a, b), f'(x) < 0) \implies f \text{ estrictamente decreciente}
> \end{align}
> $$

Básicamente podemos establecer que:
- Cuando tenemos desigualdades "amplias" y equivalencias, podemos ir en ambas direcciones.
- Cuando tenemos desigualdades estrictas, la implicación solo se da en un sentido, sin cumplirse el recíproco.

A continuación, demostraremos las desigualdades estrictas:

#### Demostración (1)
Supongamos que $\forall x \in (a, b), f'(x) > 0$.

Sean $x_{0}, x_{1} \in [a, b]$ tales que $x_{0} < x_{1}$.
Se trata de mostrar que $f(x_{0}) < f(x_{1})$.
Por Lagrange, aplicado al intervalo $[x_{0}, x_{1}]$, existe $c \in (x_{0}, x_{1})$ tal que
$$
\frac{f(x_{1}) - f(x_{0})}{x_{1} - x_{0}} = f'(c) > 0
$$
Multiplicando por $x_{1} - x_{0} > 0$, obtenemos que:
$$
f(x_{1}) - f(x_{0}) > 0
$$
es decir:
$$
f(x_{0}) < f(x_{1})
$$

El problema para las desigualdades estrictas es que si la función es estrictamente creciente, sabemos que todos los cocientes incrementales son estrictamente positivos. Sin embargo, cuando analizamos el límite, puede ser cero. Por lo tanto no se puede concluir que la derivada es estrictamente positiva, sino positiva o nula.

Por esta razón, analizaremos dos contraejemplos:

#### Ejemplo 1
$$
f(x) = x^{3} \text{ en } \mathbb{R}
$$
$f$ es estrictamente creciente en $\mathbb{R}$, pero $f'(x) = 3x^{2} = 0$ si $x = 0$.

De esta forma, podemos utilizar la desigualdad estricta de forma lineal, pero nunca el recíproco:
Que una función sea estrictamente creciente, NO IMPLICA que para todos los puntos del dominio de dicha función, la derivada sea mayor que 0. Existen casos (como el anterior, en los que es 0).

#### Ejemplo 2
$$
f(x) = x - \sin(x) \text{ en } \mathbb{R}
$$
$$
f'(x) = 1 - \cos(x) \geq 0
$$
$$
\implies f \text{ es monótona creciente}
$$
Se observa que la función es monótona creciente, siendo la pregunta donde se anula la derivada.

Dado $x \in \mathbb{R}$, tenemos que
$$
\begin{align}
f'(x) = 0 &\Longleftrightarrow \cos(x) = 1 \\
&\Longleftrightarrow \exists k \in \mathbb{Z}, x = 2k\pi
\end{align}
$$
Entonces, la derivada se anula infinitas veces, por lo que no podemos deducir que la función sea estrictamente creciente.

Sin embargo, en realidad sí lo es, pero lo descubriremos analizando la función por trozos:

Estudiemos $f$ en $[2k\pi, 2(k + 1)\pi]$
Tenemos que $f'(x) > 0$ en $(2k\pi, 2(k + 1)\pi)$

Por la proposición anterior (estricta), $f$ es estrictamente creciente en cada intervalo $[2k\pi, 2(k + 1)\pi]$

Luego:
$$
f \text{ es estrictamente creciente en } \mathbb{R}
$$

El truco fue poner los puntos problemáticos como extremos de los intervalos manejados, de forma que podemos aplicar la proposición vista (la cual no analiza lo que pasa en los extremos), y determinando que la función es estrictamente creciente.

En cada punto múltiplo de $2\pi$, la derivada es 0. Como la función es estrictamente creciente en todo $\mathbb{R}$, se puede invertir. Sin embargo, su inversa no es derivable en todos los puntos, puesto que las derivadas nulas pasan a ser infinitas en la inversa.

Todos estos teoremas valen para las funciones continuas en el intervalo cerrado y derivables (al menos) en el intervalo abierto, pudiendo generalizar a cualquier forma de intervalo:

#Corolario
### Corolario

> [!Corolario]
> Si $f$ es (continua y) derivable en $I \subseteq \mathbb{R}$
> $$
> \begin{align}
> &(\forall x \in I, f'(x) \geq 0) \Longleftrightarrow f \text{ creciente} \\
> &(\forall x \in I, f'(x) \leq 0) \Longleftrightarrow f \text{ decreciente} \\
> &(\forall x \in I, f'(x) = 0) \Longleftrightarrow f \text{ constante} \\
> &(\forall x \in I, f'(x) > 0) \implies f \text{ estrictamente creciente} \\
> &(\forall x \in I, f'(x) < 0) \implies f \text{ estrictamente decreciente}
> \end{align}
> $$

Nuevamente, aquí las recíprocas de las desigualdades estrictas no se cumplen. Este teorema agrupa todas las propiedades, pero ignora el hecho que habíamos mencionado de los extremos del intervalo (en los cuales no es necesario que la función sea derivable).

---
Ahora, pasaremos a estudiar un teorema deducido de lo anterior: el teorema de Cauchy.

#Teorema 
## Teorema de Cauchy
Es similar a Lagrange, pero con dos funciones.

> [!Teorema de Cauchy]
> Sean $f, g : [a, b] \to \mathbb{R}$ continuas en $[a, b]$ y derivables en $(a, b)$.
> 
> Entonces existe $c \in (a, b)$ tal que
> $$
> f'(x)(g(b) - g(a)) = g'(c)(f(b) - f(a))
> $$

Simplemente se intercambian de lugar $f$ y $g$.

Algo que podemos notar es que todos los teoremas que involucran derivadas tienen la misma forma.

Antes de demostrar el teorema, tenemos una observación:

> [!Observación]
> En el caso particular donde
> - o bien $g'(x) > 0 \space \forall x \in (a, b)$ (lo que significa que $g$ es estrictamente creciente).
> - o bien $g'(x) < 0 \space \forall x \in (a, b)$ (lo que significa que $g$ es estrictamente decreciente).
> 
> La expresión anterior es equivalente a
> $$
> \frac{f'(c)}{g'(c)} = \frac{f(b) - f(a)}{g(b) - g(a)}
> $$

Esta forma es más sencilla para memorizar. Sin embargo, funciona en el caso en el que la derivada de $g$ y $g(b) - g(a)$ nunca se anula.
Además, en base a esta forma podemos desarrollar la anterior:
$$
\begin{align}
&\frac{f'(c)}{g'(c)} = \frac{f(b) - f(a)}{g(b) - g(a)} \\
&\frac{f'(c)}{g'(c)} \times (g(b) - g(a)) = f(b) - f(a) \\
&f'(c)(g(b) - g(a)) = g'(c)(f(b) - f(a))
\end{align}
$$

Intuitivamente, $f$ y $g$ son las coordenadas de un punto móvil. Un físico diría:
$$
\frac{\dot{x}}{\dot{y}}(t) = \frac{x_{1} - x_{0}}{y_{1} - y_{0}}
$$
Considerando a $\frac{x_{1} - x_{0}}{y_{1} - y_{0}}$ como la pendiente de una recta dada por dos puntos, y $\frac{\dot{x}}{\dot{y}}(t)$ la pendiente de la velocidad instantánea. Por lo tanto, es un punto móvil con dos coordenadas y la variable es el tiempo $t$.

Ahora, demostraremos el teorema:
### Demostración
Sea $h : [a, b] \to \mathbb{R}$ definida por:
$$
h(x) = f(x)(g(b) - g(a)) - g(c)(f(b) - f(a))
$$
- $h$ es continua en $[a, b]$ y derivable en $(a, b)$.
- $h'(x) = f'(x)(g(b) - g(a)) - g'(c)(f(b) - f(a))$.

Ahora, calculamos el primer y último valor de $h$:
$$
\begin{align}
h(a) &= f(a)(g(b) - g(a)) - g(a)(f(b) - f(a)) \\
&= f(a)g(b) - \cancel{ f(a)g(a) } - g(a)f(b) + \cancel{ g(a)f(a) } \\
&= f(a)g(b) - g(a)f(b)
\end{align}
$$
$$
\begin{align}
h(b) &= f(b)(g(b) - g(a)) - g(b)(f(b) - f(a)) \\
&= \cancel{ f(b)g(b) } - f(b)g(a) - \cancel{ g(b)f(b) } + g(b)f(a) \\
&= f(a)g(b) - g(a)f(b) = h(a)
\end{align}
$$
En base al resultado anterior, nos encontramos en las condiciones establecidas por el lema de Rolle. Por lo tanto, sabemos que existe un punto en el que la pendiente es nula.

Por el lema de Rolle, existe $c \in (a, b)$ tal que:
$$
h'(c) = 0 = f'(c)(g(b) - g(a)) - g'(c)(f(b) - f(a))
$$
En conclusión, determinamos que
$$
f'(c)(g(b) - g(a)) - g'(c)(f(b) - f(a)) = 0 \implies f'(c)(g(b) - g(a)) = g'(c)(f(b) - f(a))
$$
confirmando lo establecido por el teorema de Cauchy.

---
Este teorema tiene una aplicación puntual y fundamental:

<u>Aplicación</u>: Regla de L'Hôpital

Dicha regla nos permitirá calcular indeterminaciones a la hora de analizar límites.

Cuando
$$
\lim_{ x \to a } f(x) = \lim_{ x \to a } g(x) = 0
$$
no se puede decir nada sobre $\frac{f}{g}$:
$$
\frac{f(x)}{g(x)} \to \text{?}
$$

La regla de L'Hôpital es simple, pero sumamente poderosa, resolviendo dicho problema.

## Regla de L'Hôpital

> [!Regla de L'Hôpital (por la derecha)]
> Sean $f, g$ dos funciones tales que:
> - $f, g$ son definidas y derivables en $(a, a + \delta)$ (con $a \in \mathbb{R}, \delta > 0$)
> - $\lim_{ x \to a^{+} } f = \lim_{ x \to a^{+} } g = 0$
> - $g'(x) \neq 0 \qquad (\forall x \in (a, a + \delta))$
> - Existe $\lim_{ x \to a^{+} } \frac{f'}{g'} = \lambda \in \mathbb{R}$
> 
> Entonces:
> $$
> g(x) \neq 0 \qquad \forall x \in (a, a + \delta)
> $$
> y
> $$
> \lim_{ x \to a^{+} } \frac{f(x)}{g(x)} = \lambda \left( = \lim_{ x \to a^{+} } \frac{f'(x)}{g'(x)}  \right) 
> $$


Basicamente, si tenemos un problema de indeterminación $\frac{0}{0}$ con un límite por la derecha, entonces basta con reemplazar $f$ y $g$ por sus derivadas. De esta forma, si puedo calcular el límite de $\frac{f'}{g'}$, este cociente será equivalente a el límite de $\frac{f}{g}$.

Durante todo el teorema, no nos importa lo que pasa en $a$.

(1) Las funciones son derivables a la derecha de $a$, sin saber lo que pasa en $a$.

No demostraremos el teorema, únicamente veremos ejemplos.

En este caso, vimos la variante por la derecha, pero también hay una regla por la izquierda y otra bilateral:

### Variante por la izquierda
Sean $f, g$ dos funciones tales que:
- $f, g$ son definidas y derivables en $(a - \delta, a)$ (con $a \in \mathbb{R}, \delta > 0$)
- $\lim_{ x \to a^{-} } f = \lim_{ x \to a^{-} } g = 0$
- $g'(x) \neq 0 \qquad (\forall x \in (a - \delta, a))$
- Existe $\lim_{ x \to a^{-} } \frac{f'}{g'} = \lambda \in \mathbb{R}$

Entonces:
$$
g(x) \neq 0 \qquad \forall x \in (a - \delta, a)
$$
y
$$
\lim_{ x \to a^{-} } \frac{f(x)}{g(x)} = \lambda \left( = \lim_{ x \to a^{-} } \frac{f'(x)}{g'(x)}  \right) 
$$

### Variante bilateral
Sean $f, g$ dos funciones tales que:
- $f, g$ son definidas y derivables en $\overbrace{ E^{*}(a, \delta) }^{ (a - \delta, a) \cup (a, a + \delta) }$ (con $a \in \mathbb{R}, \delta > 0$)
- $\lim_{ x \to a } f = \lim_{ x \to a } g = 0$
- $g'(x) \neq 0 \qquad (\forall x \in E^{*}(a, \delta))$
- Existe $\lim_{ x \to a } \frac{f'}{g'} = \lambda \in \mathbb{R}$

Entonces:
$$
g(x) \neq 0 \qquad \forall x \in E^{*}(a, \delta)
$$
y
$$
\lim_{ x \to a } \frac{f(x)}{g(x)} = \lambda \left( = \lim_{ x \to a } \frac{f'(x)}{g'(x)}  \right) 
$$

Esta última variación surge de combinar las dos anteriores, puesto que tener un límite en un punto equivale a tener límite por la izquierda y por la derecha en dicho punto, y que los valores coincidan.

Únicamente es necesario demostrar la variación bilateral, aunque no lo haremos hoy.

Concluiremos viendo un ejemplo de como se aplica la regla.

Generalmente se utiliza la variante bilateral, aunque cuando se estudia la función en un extremo o solo por la izquierda o por la derecha, podemos considerar las otras variantes. Lo importante es entender que todas las variantes tienen la misma forma, por lo que con recordar una basta.

### Ejemplo
Estudiar el límite
$$
\lim_{ x \to 0 } \frac{e^{x} - 1 - x}{x^{2}}
$$
Sabemos que en este caso:
$$
\begin{align}
e^{x} - 1 - x &\to 0 \\
x^{2} &\to 0
\end{align}
$$
por lo que tenemos una indeterminación de tipo $\frac{0}{0}$.

Analizaremos cada función por separado:
$$
\begin{align}
&f(x) := e^{x} - 1 - x \\
&g(x) := x^{2}
\end{align}
$$
Se cumple que:
$$
\lim_{ x \to 0 } f = \lim_{ x \to 0 } g = 0 
$$
Estudiamos las derivadas:
$$
\begin{align}
&f(x) := e^{x} - 1 \\
&g(x) := 2x
\end{align}
$$
Podemos ver que
$$
g' \neq 0 \text{en} \mathbb{R} \setminus \{ 0 \}
$$
Ahora, aplicamos la regla:
$$
\lim_{ x \to 0 } \frac{f'}{g'} = \frac{1}{2} \lim_{ x \to 0 } \frac{e^{x} - 1}{x} \left( = \frac{e^{x} - e^{0}}{x - 0} \right) = \frac{1}{2} \exp'(0) = \frac{1}{2}
$$
De esta forma, determinamos que el límite del cociente de las derivadas cuando $x \to 0$ es $\frac{1}{2}$.
Por lo tanto:
$$
\lim_{ x \to 0 } \frac{e^{x} - 1 - x}{x^{2}} = \frac{1}{2}
$$
Ahora, tuvimos que recordar que
$$
\lim_{ x \to 0 } \frac{e^{x} - 1}{x} = 1 
$$
Sin embargo, tampoco es necesario recordar el valor de los límites, puesto que la regla de L'Hôpital se puede aplicar varias veces sin perder su propiedad.

Otro argumento:
$$
\lim_{ x \to 0 } \frac{e^{x} - 1}{2x} \left( = \frac{0}{0} \right)
$$
$$
\begin{align}
&f''(x) = e^{x} \\
&g''(x) = 2
\end{align}
$$
De esta forma, volvemos a aplicar la regla de L'Hôpital una segunda vez, para determinar el valor del límite:
$$
\lim_{ x \to 0 } \frac{e^{x} - 1}{2x} = \lim_{ x \to 0 } \frac{e^{x}}{2}
$$
$$
= \frac{e^{0}}{2} = \frac{1}{2}
$$Como vemos, es una regla super amigable que puede ser iterada. También existe una regla de L'Hôpital para las indeterminaciones con $\infty$, aunque no la abordaremos en el curso.

En la próxima clase, demostraremos la regla.