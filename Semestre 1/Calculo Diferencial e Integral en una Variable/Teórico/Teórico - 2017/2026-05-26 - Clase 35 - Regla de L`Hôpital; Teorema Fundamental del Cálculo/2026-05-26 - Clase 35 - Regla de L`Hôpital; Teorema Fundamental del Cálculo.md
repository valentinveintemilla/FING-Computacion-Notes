# Derivadas
Proseguimos con el capítulo de Derivadas.

Comenzaremos repasando la regla de L'Hôpital.
## Regla de L'Hôpital
Primeramente, estudiaremos la versión más general del enunciado: formulación bilateral.

Lo que busca solucionar dicha regla es el caso en el que a la hora de calcular un límite se obtiene una indeterminación del estilo $\frac{0}{0}$. En dicho caso, se establece que se pueden derivar la función numerador y denominador por separado, asegurando que el resultado de dicho límite es equivalente al anterior.

> [!Regla de L'Hôpital]
> - $f, g$ definidas y derivables en $E^{*}(a, \delta) \qquad (\delta > 0)$
> - $\lim_{ x \to a } f(x) = \lim_{ x \to a } g(x) = 0$
> - $\forall x \in E^{*}(a, \delta), g'(x) \neq 0$
> - $\exists \lim_{ x \to a } \frac{f'(x)}{g'(x)} ( = \lambda \in \mathbb{R})$
> 
> Entonces
> $$
> \lim_{ x \to a } \frac{f(x)}{g(x)} = \lambda 
> $$
> (y además: $\forall x \in E^{*}(a, \delta), g(x) \neq 0$)

Básicamente, si las funciones cumplen las propiedades establecidas, se pueden derivar ambas partes, siendo un límite equivalente.

> [!Observación]
> Se pueden reemplazar:
> $E^{*}(a, \delta)$ y $x \to a$ por:
> - o bien $(a, a + \delta)$ y $x \to a^{+}$
> - o bien $(a - \delta, a)$ y $x \to a^{-}$

De esta forma, sabemos que podemos utilizar cualquiera de las reglas según el caso presentado. Además, la regla bilateral surge de la combinación de la regla por la izquierda y por la derecha, y la demostración de ambos es simétrica (por lo que solo es necesario demostrar uno).

En este caso, demostraremos el caso por la derecha:
### Demostración
Como $\lim_{ x \to a^{+} } f(x) = \lim_{ x \to a^{+} } g(x) = 0$ y $f, g$ son continuas en $(a, a + \delta)$.

Se pueden extender "por continuidad" $f$ y $g$ en $a$ por $f(a) = g(a) = 0$.
(Aseguramos que la función sea continua en $a$. Esto lo hacemos con la idea de utilizar el teorema de Lagrange y el teorema de Cauchy)

Ahora:
$f, g : [a, a + \delta) \to \mathbb{R}$ son continuas.

Sea $x \in (a, a + \delta)$ fijado.
Aplicando el teorema de Lagrange en $[a, x]$, existe $x' \in (a, x)$ tal que
$$
\frac{g(x) - g(a)}{x - a} = \frac{g(x)}{x - a} = g'(x') \neq 0
$$
Luego $g(x) \neq 0$ (puesto que si el cociente no es nulo, entonces el numerador no es nulo).

Esto nos asegura que podemos dividir por $g(x)$.

Ahora, demostramos la propiedad deseada: aplicaremos Cauchy considerando el mismo $x$.

Aplicando el teorema de Cauchy a $f$ y $g$ en $[a, x]$, existe $c_{x} \in (a, x)$ tal que
$$
f'(c_{x})(g(x) - g(a)) = g'(c_{x})(f(x) - f(a))
$$
Como $f(a) = g(a) = 0$:
$$
f'(c_{x})\underbrace{ g(x) }_{ = 0 } = \underbrace{ g'(c_{x}) }_{ = 0 }f(x)
$$
$$
\frac{f'(c_{x})}{g'(c_{x})} = \frac{f(x)}{g(x)}
$$
De esta forma, el cociente en el punto $x$ de $\frac{f}{g}$ es igual al cociente $\frac{f'}{g'}$ en otro punto cercano a $x$.

Sea $\begin{align} &h : (a, a + \delta) \to (a, a + \delta) \\ &x \mapsto h(x) = c_{x} \end{align}$

En base a la definición, sabemos que:
$$
\begin{align}
\forall x \in (a, a + \delta) \qquad a < \underbrace{ h(x) }_{ = c_{x} } < x
\end{align}
$$
Por sándwich:
$$
\lim_{ x \to a } h(x) = a 
$$
(Puesto que $x \to a^{+}$ y "encierran" a $h(x)$)

Ahora, podemos analizar el límite de $\frac{f(x)}{g(x)}$:
$$
\frac{f(x)}{g(x)} = \frac{f'(h(x))}{g'(h(x))} \underset{x \to a^{+}} \longrightarrow \lambda \qquad \text{(por composición de límites)}
$$
Puesto que cuando $x \to a^{+}$:
$$
\frac{f(x)}{g(x)} \underset{x \to a^{+}} \longrightarrow \frac{f(a)}{g(a)}  = \frac{f'(x)}{g'(x)} \underset{x \to a^{+}} \longrightarrow \frac{f'(a)}{g'(a)}
$$
Esto demuestra la regla de L'Hôpital por la derecha. La demostración por la izquierda es análoga, y su unión conforma la versión bilateral.

A continuación, veremos otra aplicación de la regla:
$$
\lim_{ x \to 0 } \frac{\cos x - 1}{x^{2}}
$$
En las hipótesis sobre $a$, no nos interesa lo que pasa en $a$, sino en sus alrededores. Por lo tanto $x^{2} \neq 0$ pero $x^{2} \to 0$ cuando $x \to 0$.
$$
\begin{align}
&f'(x) = -\sin(x) \\
&g'(x) = 2x
\end{align}
$$
$$
\lim_{ x \to 0 } \frac{-\sin(x)}{2x} = -\frac{1}{2}
$$
pues sabemos que
$$
\lim_{ x \to 0 } \frac{\sin(x)}{x} = 1
$$
Por L'Hôpital, determinamos que
$$
\lim_{ x \to 0 } \frac{\cos x - 1}{x^{2}} = -\frac{1}{2}
$$

Esta es la resolución corta, recordando que $\lim_{ x \to 0 } \frac{\sin(x)}{x} = 1$. Sin embargo, si no recordamos dicho límite, podemos seguir aplicando L'Hôpital (en caso de que se sigan cumpliendo las características necesarias, como lo es el caso):
$$
\begin{align}
&f''(x) = -\cos(x) \\
&g''(x) = 2
\end{align}
$$
$$
\lim_{ x \to 0 } \frac{-\cos(x)}{2} = -\frac{1}{2}
$$
A partir de aquí, no podemos seguir aplicando L'Hôpital, ya que numerador y denominador no tienden a 0.

Como vemos, es una técnica super eficaz.

---
Ahora que hemos abordado las derivadas y varios de los teoremas relacionados con el tema, podemos introducir el tema central de la segunda parte del curso: Teorema Fundamental del Cálculo.

Fue descubierto por Leibniz cuando inventó el cálculo integral. Vincula dos temas que a priori no tienen ninguna relación: integral (área) y derivada (tangentes y pendientes, velocidad).

Sin embargo, tienen una coincidencia: son operaciones inversas. Entonces, calcular una integral es lo mismo que anti derivar.

# Teorema fundamental (del cálculo)

Está dividido en dos partes:

> [!Teorema fundamental - Parte 1]
> Sean $f : I \to \mathbb{R}$ una función localmente integrable en $I$ y un punto $a \in I$ fijado. Se considera la función
> $$
> F(x) = \int_{a}^{x} f(t) \space dt \qquad (\forall x \in I)
> $$
> Dicha función siempre cumple las siguientes características:
> 1. $F: I \to \mathbb{R}$ siempre es continua.
> 2. En todo punto $x \in I$ donde $f$ es continua, la función $F$ es derivable, y $F'(x) = f(x)$

Función localmente integrable: se puede integrar en cualquier subintervalo cerrado.

Ya vimos la función $F(x)$ previamente, e incluso utilizamos la misma idea para definir la función logaritmo, siendo $a = 1$ y $f(t) = \frac{1}{t}$.

También habíamos visto que todas las funciones de tipo $F(x)$ son continuas. Por ejemplo, una funciones constantes se transforman en funciones lineales por trozos.

Si en un tramo, el valor es 1, entonces en $F(x)$, la pendiente será 1 en dicho tramo. Si en otro tramo, el valor es 2, la pendiente de $F(x)$ será 2 en el mismo tramo, así con el resto de la función. Los valores constantes se transforman en pendientes. Esto significa que el valor en un tramo de $f$ es la pendiente (valor de la derivada) del mismo tramo en $F$. Lo podemos analizar punto a punto, pero es fundamental que en ese punto $f$ sea continua (para poder ser derivable).

La derivada en cada punto de $F$ es el valor de la función $f$ en el mismo punto.

De esta forma, la idea es que, cuando $f$ es continua, la derivada de $F$ es la función de partida $f$.

Podemos ver un ejemplo sobre esto abordado anteriormente en el curso:

Definimos
$$
\log(x) = \int_{1}^{x} \frac{1}{t} \space dt
$$
$$
\implies \log'(x) = \frac{1}{x}
$$
No solo lo vimos para la función $\log$. También lo estudiamos para los monomios:
$$
F(x) = \int_{a}^{x} t^{n} \space dt = \frac{x^{n + 1} - a^{n + 1}}{n + 1}
$$
$$
\implies F'(n) = x^{n}
$$
Si operamos, llegamos a dicho resultado calculando $\left( \frac{x^{n + 1} - a^{n + 1}}{n + 1} \right)$.

Dicho teorema no es trivial, puesto que vincula dos conceptos que no parecen tener relación, estableciendo que: la pendiente del área fundamental es la función de partida.

Con área aquí nos referimos al área incremental, puesto que se considera un punto fijo y un parámetro móvil. Luego, tenemos la derivada, que aplicada al área incremental determina la función de partida.

Esto es sumamente útil para el cálculo de integrales, puesto que permite facilitar su cálculo. Si sabemos calcular derivadas, sabemos realizar la operación inversa, calcular primitivas, y esto nos permitirá calcular integrales.

Si la función inicial no es continua en todo su recorrido (tiene saltos), no será derivable en dichos puntos, haciendo que la función $F$ tampoco lo sea (puesto que habrá un salto en el valor de la pendiente, será angulosa).

Es fundamental entender esta idea de como las funciones $f$ y $F$ se relacionan punto a punto, el área y la pendiente. Teniendo la idea de como $F$ se "dibuja" a medida que consideramos más y más área de $f$ ayuda a comprender la idea, así como la necesidad de que $f$ sea no solo localmente integrable, sino también continua, para que $F$ sea derivable.

Es así que, cuando se integra $f$, dando como resultado $F$, la idea intuitiva es que se regulariza aún más el comportamiento de la función. Por ejemplo, veremos que si $f$ es derivable, entonces $F$ será 2 veces derivable, si $f$ es 5 veces derivable, entonces $F$ será 6 veces derivable, etc.

Proseguimos con la segunda parte del teorema:

> [!Teorema fundamental - Parte 2]
> Sea $x_{0} \in I$ donde $f$ es continua.
> 
> Se trata de mostrar que
> $$
> \lim_{ x \to x_{0} } \frac{F(x) - F(x_{0})}{x - x_{0}} = f(x_{0}) 
> $$

Queremos estudiar el límite de $\frac{F(x) - F(x_{0})}{x - x_{0}}$ cuando $x \to x_{0}$ (la derivabilidad de $F$ en $x_{0}$). Esto coincide con la idea anterior, puesto que $\lim_{ x \to x_{0} } \frac{F(x) - F(x_{0})}{x - x_{0}} = F'(x_{0})$.

Para demostrar la existencia de dicho límite, utilizaremos $\epsilon$ y $\delta$.

## Demostración

Sea $\epsilon > 0$. Como $f$ es continua en $x_{0}$, existe $\delta > 0$ tal que $\forall x \in I, |x - x_{0}| < \delta \implies |f(x) - f(x_{0})| < \epsilon$.

Sabemos que existe un $\delta$, pero tenemos que hallarlo.

Tenemos dos problemas de límites:
$$
\lim_{ x \to x_{0} } \frac{F(x) - F(x_{0})}{x - x_{0}} \text{ y } \lim_{ x \to x_{0} } f(x_{0}) 
$$
Como la función $f$ es continua, sabemos que existe el segundo limite (en $x_{0}$) existe. Por lo tanto, existe un valor de $\delta$ correspondiente al mismo, y tomaremos el mismo. Lo interesante será que el mismo $\delta$ funciona para $\lim_{ x \to x_{0} } \frac{F(x) - F(x_{0})}{x - x_{0}}$. Utilizaremos varias integrales durante la demostración.

Básicamente, determinaremos la distancia entre $\lim_{ x \to x_{0} } \frac{F(x) - F(x_{0})}{x - x_{0}}$ y $f(x_{0})$, por lo que restaremos ambos, quitándonos el problema del denominador multiplicando todo por $x - x_{0}$.

Tenemos que
$$
\begin{align}
&F(x) - F(x_{0}) - f(x_{0})(x - x_{0}) \\
= \space &\int_{a}^{x} f(t) \space dt - \int_{a}^{x_{0}} f(t) \space dt - \int_{x_{0}}^{x} f(x_{0}) \space dt \\
= \space &\int_{x_{0}}^{x} f(t) \space dt - \int_{x_{0}}^{x} f(x_{0}) \space dt \\
= \space &\int_{x_{0}}^{x} (f(t) - f(x_{0})) \space dt
\end{align}
$$
$$
\implies |F(x) - F(x_{0}) - f(x_{0})(x - x_{0})| = \left| \int_{x_{0}}^{x} (f(t) - f(x_{0})) \space dt \right| \leq \int_{x_{0}}^{x} |(f(t) - f(x_{0}))| \space dt
$$
En realidad, habría que considerar dos casos:
- Si $x_{0} < x$: $\int_{x_{0}}^{x} (f(t) - f(x_{0})) \space dt$
- Si $x_{0} > x$: $\int_{x}^{x_{0}} (f(t) - f(x_{0})) \space dt$

Sea $x$ tal que $|x - x_{0}| < \delta$, entrando dentro de los valores considerados para la integral $\int_{x_{0}}^{x} |(f(t) - f(x_{0}))| \space dt$. Como la variable $t$ esta entre $x$ y $x_{0}$, sabemos que
$$
\int_{x_{0}}^{x} |(f(t) - f(x_{0}))| \space dt \leq \epsilon |x - x_{0}|
$$
ya que se cumple que $|(f(t) - f(x_{0}))| \leq \epsilon$.

Luego, cuando $x \in E(x_{0}, \delta)$:
$$
\left| \frac{F(x) - F(x_{0})}{x - x_{0}} - f(x_{0}) \right| \leq \frac{\epsilon \cancel{ |x - x_{0}| }}{\cancel{ |x - x_{0}| }}
$$

Esto demuestra la propiedad de integración.

Existen muchos corolarios surgidos del teorema fundamental. A continuación abordaremos 2:

> [!Corolario 1]
> Si $f : I \to \mathbb{R}$ es continua, entonces $F(x) = \int_{a}^{x} f(t) \space dt$ es derivable en $I$, y $F' = f$.
> 
> Dicho de otro modo: $F$ es una primitiva de $f$.

Aclaración:
La primitiva es la operación opuesta de la derivada. Por definición $F$ es una primitiva de $f$ cuando $f$ es la derivada de $F$.

> [!Primitiva - Definición]
> $f$ es una <u>primitiva</u> de $g$ cuando $g$ es derivable y $g' = f$.

Es la operación opuesta a la derivada.

Es importante entender que las primitivas no son únicas. Por ejemplo, todas las funciones constantes tienen como derivada 0. Entonces, todas las funciones constantes son primitivas de la función nula.

Lo que dice el teorema fundamental en función a las primitivas es que, si tengo una función continua, para calcular una primitiva, tengo una integral:

> [!Corolario 2]
> Toda función continua $f$ tiene una primitiva, dada por
> $$
> F(x) = \int_{a}^{x} f(t) \space dt
> $$

De esta forma, vimos que la integración y derivación son operaciones opuestas (con algunas sutilezas que abordaremos a posteriori).

Es importante entender dos cosas relacionadas al teorema fundamental:
- Si tenemos una primitiva, sabemos calcular la integral.
- Si queremos calcular una primitiva, con métodos numéricos, podemos usar la integral.
