# Funciones trigonométricas
En esta clase abordaremos las funciones trigonométricas, siendo funciones que describen "fenómenos circulares".

Para esto utilizaremos una herramienta sumamente útil: la circunferencia trigonométrica (o círculo unitario).
![[1 - Circunferencia trigonométrica.png]]

Como $\alpha \in \mathbb{R}$, si $\alpha < 0$ entonces vamos "al revés" (hacia abajo).

También lo podemos encontrar denominado como "círculo unitario" ya que circunferencia tiene radio 1.

Podemos definir las siguientes propiedades:

> [!Propiedades]
> $$
> \begin{align}
> &-1 \leq \cos \alpha \leq 1 \\
> &-1 \leq \cos \alpha \leq 1 \\
> &\cos ^{2} \alpha + \sin ^{2} \alpha = 1 \qquad \text{(por Pitágoras)} \\ \\
> 
> &\cos(\alpha + 2\pi) = \cos \alpha \\
> &\sin(\alpha + 2\pi) = \sin \alpha \\
> &\text{(Ya que } 2\pi \text{ representa una vuelta completa a la circunferencia)}  \\ \\
> 
> &\cos (-\alpha) = \cos \alpha \qquad \text{Función par} \\
> &\sin (-\alpha) = -\sin \alpha \qquad \text{Función impar}
> \end{align}
> $$

Aclaración: por convención:
$$
(\cos \alpha)^{2} = \cos ^{2} \alpha
$$
La escritura anterior evita confusión, ya que sin los paréntesis puede no saberse si se está elevando al resultado de la función coseno o solo a $\alpha$.

Si las graficamos podemos ver que son funciones periódicas y representan oscilaciones (se mueven en el intervalo $[-1, 1]$ siempre con la misma amplitud). A medida que el punto $M$ gira al rededor de la circunferencia, las variables $\cos x$ y $\sin x$ oscilan tomando valores del intervalo $[-1, 1]$:
![[2 - Gráfica de seno y coseno.png]]
Las líneas punteadas interceptan a los gráficos de la función en sus máximos (1) y mínimos (-1) absolutos (y relativos, aunque no hayamos abordado dicho concepto aún).

Además, tenemos rectas tangentes dependiente 1 y -1 cuando las funciones cortan en el eje $x$. Dependiendo de cual sea el sentido de la función en ese momento (si viene en bajada o en subida), la pendiente es -1 o 1.

Debajo se incluye una tabla de variación de las funciones trigonométricas $\sin$ y $\cos$:
![[3 - Tabla de variación de seno y coseno.png]]
Esto sale directamente del estudio de la gráfica de la función.

---
Toda la información anterior surge de la representación y entendimiento del círculo unitario y la gráfica de la función. Sin embargo, otras propiedades no son tan visibles:

## Propiedades algebraicas

### Fórmulas de adición/duplicación
De aquí también surgen las fórmulas de sustracción, pero son triviales.

> [!Fórmulas de adición]
> $$
> \begin{align}
> &\cos(\alpha + \beta) = \cos \alpha \cos \beta - \sin \alpha \sin \beta \\
> &\sin(\alpha + \beta) = \cos \alpha \sin \beta + \sin \alpha \cos \beta
> \end{align}
> $$

Estas fórmulas se demuestran mediante argumentos geométricos. Igualmente, en este caso conviene memorizar dicha fórmula.

El resto de fórmulas se deducen a partir de las anteriores:

> [!Fórmulas de duplicación]
> $$
> \begin{align}
> &\cos 2\alpha = \cos^{2} \alpha - \sin^{2} \alpha &&= 2 \cos^{2} \alpha - \overbrace{ (\sin^{2} \alpha + \cos^{2} \alpha) }^{ = 1 \text{ (por Pitágoras)} } \\
> &&&= 2 \cos^{2} \alpha - 1 \\ \\
> 
> &\sin 2\alpha = 2 \cos \alpha \sin \alpha
> \end{align}
> $$

> [!Fórmulas de sustracción]
> $$
> \begin{align}
> &\cos (\alpha - \beta) = \cos \alpha \cos (-\beta) - \sin \alpha \sin (-\beta) = \cos \alpha \cos \beta + \sin \alpha \sin \beta \\ \\
> 
> 
> &\sin (\alpha - \beta) = \cos \alpha \sin (-\beta) + \sin \alpha \cos (-\beta) = - \cos \alpha \sin \beta + \sin \alpha \cos \beta
> \end{align}
> $$

Las siguientes también se pueden deducir de las fórmulas de adición:
> [!Otras propiedades]
> $$
> \begin{align}
> &\cos \left( \alpha + \frac{\pi}{2} \right) = \cos \alpha \space \underbrace{ \cos \frac{\pi}{2} }_{ = 0 } - \sin \alpha \space \underbrace{ \sin \frac{\pi}{2} }_{ = 1 } = -\sin \alpha \\ \\
> 
> &\sin \left( \alpha + \frac{\pi}{2} \right) = \cos \alpha \space \underbrace{ \sin \frac{\pi}{2} }_{ = 1 } + \sin \alpha \space \underbrace{ \cos \frac{\pi}{2} }_{ = 0 } = \cos \alpha \\ \\
> 
> &\cos \left( \alpha + \pi \right) = \cos \alpha \space \underbrace{ \cos \pi }_{ = -1 } - \sin \alpha \space \underbrace{ \sin \pi }_{ = 0 } = -\cos \alpha \\ \\
> 
> &\sin \left( \alpha + \pi \right) = \cos \alpha \space \underbrace{ \sin \pi }_{ = 0 } + \sin \alpha \space \underbrace{ \cos \pi }_{ = -1 } = -\sin \alpha \\ \\
> 
> &\cos \left( \alpha + 2\pi \right) = \cos \alpha \space \underbrace{ \cos 2\pi }_{ = 1 } - \sin \alpha \space \underbrace{ \sin 2\pi }_{ = 0 } = \cos \alpha \\ \\
> 
> &\sin \left( \alpha + 2\pi \right) = \cos \alpha \space \underbrace{ \sin 2\pi }_{ = 0 } + \sin \alpha \space \underbrace{ \cos 2\pi }_{ = 1 } = \sin \alpha
> \end{align}
> $$

En este ultimo caso:
- Cuando hacemos una rotación de ángulo $\frac{\pi}{2}$, se intercambian las coordenadas, y una cambia de signo.
- Cuando hacemos una hacemos una rotación de ángulo $\pi$, se cambian los signos de las coordenadas.
- Cuando hacemos una hacemos una rotación de ángulo $2\pi$, no cambian las coordenadas.

Si se visualiza geométricamente, es más claro lo que sucede:
- Cuando hacemos una rotación de ángulo $\frac{\pi}{2}$, se trata de un cuarto de circunferencia.
- Cuando hacemos una hacemos una rotación de ángulo $\pi$, se trata de media circunferencia.
- Cuando hacemos una hacemos una rotación de ángulo $2\pi$, se vuelve al mismo lugar.

Como vemos, a partir de las fórmulas de adición, podemos deducir todo el resto.

Podemos concluir estableciendo que las funciones $\sin$ y $\cos$ son el prototipo de las funciones periódicas (en general).

---
Terminamos la parte algebraica, proseguimos con las propiedades de limites y continuidad (dejando de lado las demostraciones):
## Propiedades de límites y continuidad

> [!Proposición]
> Las funciones $\cos, \sin: \mathbb{R} \to \mathbb{R}$ son continuas y no tienen límites (finitos o infinitos) ni en $+ \infty$ ni en $- \infty$.

La proposición anterior surge de las siguientes desigualdades notables:

> [!Desigualdades notables]
> $$
> \begin{align}
> &1 - \frac{x^{2}}{2} \leq \cos x \leq 1 &&(\forall x \in \mathbb{R}) \\
> &x - \frac{x^{3}}{6} \leq \sin x \leq x &&(\forall x \geq 0)
> \end{align}
> $$

(1) Sabemos que el coseno esta acotado superiormente por 1 e inferiormente por la parábola $1 - \frac{x^{2}}{2}$. Esta desigualdad nos permite analizar lo que sucede por Sándwich en el punto $x = 0$:
$$
\begin{align}
&\lim_{ x \to 0 } 1 - \frac{x^{2}}{2} = 1 \\
&\lim_{ x \to 0 } 1 = 1 \\
&\implies \lim_{ x \to 0 } \cos x = 1
\end{align}
$$
![[4 - Coseno (Sándwich).png]]

(2) Para $x < 0$, se invierte la desigualdad. Ídem que el caso anterior, dicha desigualdad permite estudiar lo que sucede en el punto $x = 0$ mediante Sándwich:
$$
\begin{align}
&\lim_{ x \to 0 } x - \frac{x^{3}}{6} = 0 \\
&\lim_{ x \to 0 } x = 0 \\
&\implies \lim_{ x \to 0 } \sin x = 0
\end{align}
$$
![[5 - Seno (Sándwich).png]]

De esta manera, tanto seno como coseno son continuas en 0.

Lo interesante de esto es que, en conjunto con las fórmulas de rotación (utilizando la traslación y la compuesta, sumando una constante), se puede deducir que $\sin$ y $\cos$ son continuas en todos los puntos de $\mathbb{R}$ (por rotación).

Además de la continuidad de seno y coseno, las desigualdades notables anteriores permiten demostrar otras cosas:

> [!Proposición]
> $$
> \lim_{ x \to 0 } \frac{\sin x}{x} = 1
> $$

Este límite lleva a una indeterminación. Sin embargo, en base a las desigualdades notables:
$$
\begin{align}
&x - x^{3} \leq \sin x \leq x \\
&\frac{x - \frac{x^{3}}{6}}{x} = 1 - \frac{x^{2}}{6} \leq \frac{\sin x}{x} \leq \frac{x}{x} = 1
\end{align}
$$
Ahora, podemos estudiar:
$$
\begin{align}
&\lim_{ x \to 0 } 1 - \frac{x^{2}}{6} = \lim_{ x \to 0 } \overbrace{ 1 }^{ \to 1 } - \lim_{ x \to 0 } \overbrace{ \frac{x^{2}}{6} }^{ \to 0 } = 1 \\
&\lim_{ x \to 0 } 1 = 1
\end{align}
$$
Por Sándwich:
$$
\lim_{ x \to 0 } \frac{\sin x}{x} = 1
$$

Esto también indica que la pendiente en $x = 0$ es 1.

Otro caso:

> [!Proposición]
> $$
> \lim_{ x \to 0 } \frac{\cos x - 1}{x} = 0
> $$

Estudiamos la desigualdad notable:
$$
\begin{align}
&1 - \frac{x^{2}}{2} \leq \cos x \leq 1 \\
&-\frac{x^{2}}{2} \leq \cos x - 1 \leq 0 \\
&-\frac{x}{2} \leq \frac{\cos x - 1}{x} \leq 0
\end{align}
$$
$$
\begin{align}
&\lim_{ x \to 0 } -\frac{x}{2} = -\frac{0}{2} = 0 \\
&\lim_{ x \to 0 } 0 = 0
\end{align}
$$
Por Sándwich:
$$
\lim_{ x \to 0 } \frac{\cos x - 1}{x} = 1
$$
Es así que en base a las dos desigualdades anteriores, podemos desarrollar todas estas proposiciones

---
Para finalizar, estudiaremos la función tangente, la cual es quizás más utilizada en la práctica que las funciones seno y coseno.

## Función tangente

> [!Función tangente - Definición]
> $$
> \tan x := \frac{\sin x}{\cos x} \qquad \left( \text{si } x \neq \frac{\pi}{2} + k \pi, k \in \mathbb{Z} \right)
> $$

Su representación gráfica:
![[6 - Función tangente.png]]

Algunas operaciones considerando la definición:
$$
\begin{align}
\tan (\alpha + \pi) &= \frac{\sin (\alpha + \pi)}{\cos (\alpha + \pi)} \\
&= \frac{\cancel{ - }\sin \alpha}{\cancel{ - }\cos \alpha} = \tan \alpha
\end{align}
$$
De esta forma, la función tangente es periódica de periodo $\pi$, por lo que oscila el doble de rápido que las funciones seno y coseno (que son periódicas de periodo $2\pi$).
Como la función no está definida en puntos específicos, podemos decir que es una función definida en una unión numerable de intervalos abiertos.

> [!Propiedades]
> $\tan$ es continua en $\left( -\frac{\pi}{2} + k\pi, \frac{\pi}{2} + k\pi \right) \qquad k \in \mathbb{Z}$
> $$
> \begin{align}
> &\lim_{ x \to -\frac{\pi}{2}^{+} } \tan x = -\infty \\
> &\lim_{ x \to \frac{\pi}{2}^{-} } \tan x = +\infty
> \end{align}
> $$

La función tangente no es seccionalmente continua, ya que no tiene límites finitos.

Esta función también tiene sus propias fórmulas de adición y duplicación, desarrolladas en base a las fórmulas vistas para seno y coseno:

> [!Fórmula de adición]
> $$
> \begin{align}
> \tan (\alpha + \beta) = \frac{\sin (\alpha + \beta)}{\cos (\alpha + \beta)} &= \frac{\cos \alpha \sin \beta + \sin \alpha \cos \beta}{\cos \alpha \cos \beta - \sin \alpha \sin \beta} \left( \frac{\div \cos \alpha \cos \beta}{\div \cos \alpha \cos \beta} \right) \\
> &=\frac{\tan \alpha + \tan \beta}{1 - \tan \alpha \tan \beta}
> \end{align}
> $$

Aclaración: $\left( \frac{\div \cos \alpha \cos \beta}{\div \cos \alpha \cos \beta} \right)$ se trata de una división tanto del numerador como del denominador.
$$
\frac{\cos \alpha \sin \beta}{\cos \alpha \cos \beta} = 1 \times \frac{\sin \beta}{\cos \beta} = 1 \times \tan \beta = \tan \beta
$$
Los demás términos salen de la misma manera.

La fórmula de duplicación y sustracción se desarrollan aplicando la misma lógica.

---
Todo esto nos da las bases para comenzar a estudiar el capítulo de derivadas.

# Derivadas
La intuición de derivada surge a partir de la noción de velocidad.

Consideremos un punto móvil en una recta, al cual le tomamos la velocidad en el tiempo 0 ($f(t_{0})$) y en el tiempo 1 ($f(t_{1})$). Esto nos permite calcular la ==velocidad promedio==:
$$
v_{t_{0},t_{1}} = \frac{\Delta f_{t_{0},t_{1}}}{\Delta t} = \frac{f(t_{1}) - f(t_{0})}{t_{1} - t_{0}}
$$
Esto se llama cociente incremental, o taza de crecimiento, y mide la velocidad promedio.

Ahora, lo interesante es: ¿Qué sucede si fijo $t_{0}$ y hago variar $t_{1}$?
$$
\frac{f(t) - f(t_{0})}{t - t_{0}} \qquad \text{con } t_{0} \text{ fijado y } t \to t_{0}
$$
En este caso, $t - t_{0} \to 0$, y si consideramos una función continua regular, $f(t) - f(t_{0}) \to 0$, y esto es un problema, puesto que tenemos una indeterminación de tipo $\frac{0}{0}$.

Entonces, la derivada consiste en estudiar este tipo de indeterminaciones. Cada vez que manejamos derivadas, lo que hacemos es trabajar con indeterminaciones.

Según Leibniz, no es $t = t_{0}$, sino que son los valores cercanos, se maneja un concepto distinto de nulo: infinitésimo, expresado como $dt$ ($t - t_{0} = dt$). Simplemente se trata de una intuición.
De esta forma, lo expresamos como:
$$
\frac{f(t_{0} + dt) - f(t_{0})}{dt} = \frac{df}{dt}
$$
Esta es la notación de Leibniz. Sin embargo, también tenemos la notación de Newton (más utilizada en física):
$$
\frac{f(t_{0} + dt) - f(t_{0})}{dt} = \dot{f}
$$
En este caso, utilizaremos una notación intermedia:
$$
\frac{f(t_{0} + dt) - f(t_{0})}{dt} = f'
$$

De esta forma, todo este problema surge de la indeterminación encontrada al aproximar $t$ a $t_{0}$, y de esta forma también se motivó el desarrollo de la teoría del límite, para dar un sentido a lo que sucede cuando numerador y denominador tienden a 0, una indeterminación la cual se resuelve en muchos casos, y establece que una función es "derivable".

Como $\frac{f(t) - f(t_{0})}{t - t_{0}}$ representa la velocidad promedio entre dos tiempos, cuando $t \to t_{0}$ obtengo la velocidad instantánea, que es la ==derivada== en el punto correspondiente (en este caso $t_{0}$).

A continuación, abordaremos la definición formal de derivada en un punto.

## Derivada en un punto

> [!Definición: Derivada en un punto]
> Sean $f : I \to \mathbb{R}$ y $x_{0} \in I$.
> Se dice que $f$ es derivable en $x_{0}$ cuando el cociente
> $$
> \frac{f(x) - f(x_{0})}{x - x_{0}}
> $$
> tiene límite finito cuando $x \to x_{0}$.
> Se escribe
> $$
> f'(x_{0}) = \lim_{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}} \qquad (\text{derivada de } f \text{ en } x_{0})
> $$

Esto representa la velocidad de movimiento de la función $f$.

Antes de pasar a las propiedades, analizaremos dos observaciones que surgen de la definición formal de límite y como se integra con la definición de derivada en un punto:

1. $x \mapsto \frac{f(x) - f(x_{0})}{x - x_{0}}$ está definida en $I - \{ x_{0} \}$.
2. También tenemos que
$$
f'(x_{0}) = \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0})}{h}
$$

(1) Si recordamos la noción de límite, el límite solo está definido para una función definida en un intervalo. El problema es que aquí no analizamos el límite de $f$, sino de $\frac{f(x) - f(x_{0})}{x - x_{0}}$, la cual no está definida en $x_{0}$.
Esto significa que no está definida en un intervalo, sino dos (a no ser que $x_{0}$ sea un extremo). Sin embargo, como la noción de límite no depende del valor en el punto en el que se estudia, podemos extender la noción de limite para los casos en los que la función no está definida en el punto en el que considero el límite.

En conclusión, a partir de ahora, consideramos límites de funciones definidas en un intervalo, salvo en el punto donde considero el límite. Y esto es válido ya que el límite nunca depende del valor en dicho punto.

(2) Simplemente sustituimos $x - x_{0}$ por $h$. Las dos definiciones son equivalentes:
$$
f'(x_{0}) = \lim_{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}} = \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0})}{h}
$$

---
Ahora, abordaremos una intuición de como se representa gráficamente la derivada de una función, tomando el concepto de tangente.

Para comenzar, definiremos lo que es una tangente:

## Recta tangente
Consideramos una función y dos puntos que tengan imagen, $x_{0}$ y $x_{0} + h$. Ahora, estudiamos la recta que pasa por ambos puntos $R_{h}$.
![[7 - Recta tangente.png]]

Calculamos la fórmula de dicha recta en base a la siguiente fórmula:

> [!Ecuación de la recta en base a dos puntos]
> Sean $(x_{0}, y_{0}), (x_{1}, y_{1})$ dos puntos diferentes, podemos encontrar la ecuación de la recta que pasa por ambos:
> $$
> R: y = y_{0} + \frac{y_{1} - y_{0}}{x_{1} - x_{0}}(x - x_{0})
> $$
> Al final se obtiene una ecuación de tipo recta:
> $$
> y = mx + n
> $$
> Siendo $m$ la pendiente y $n$ la ordenada.

De esta forma. desarrollamos la fórmula de la recta $R_{h}$:
$$
R_{h}: y = f(x_{0}) + \frac{f(x_{0} + h) - f(x_{0})}{h}(x - x_{0})
$$
Aquí, $\frac{f(x_{0} + h) - f(x_{0})}{h}$ es la pendiente de la recta, y coincide con el cociente incremental definido anteriormente.

Cuando $h \to 0$ ($x \to x_{0}$), vemos el cociente incremental tiende a la derivada, lo que me da un límite de rectas.
Es fundamental entender este punto: aquí manejamos una familia de rectas, indicadas por un $h$ infinitésimo, y al final obtenemos un límite de recta cuando $h$ tiende a 0.

De esta manera, cuando $h \to 0$:
$$
R_{0} : y = f(x_{0}) + f'(x_{0}) \cdot (x - x_{0})
$$
Esto es la ecuación de la recta tangente.

En este ultimo caso, podemos ver que la derivada representa la pendiente de la recta tangente al punto $x_{0}$ en la función correspondiente.

$$
f'(x_{0}) = \text{pendiente de la recta tangente a la gráfica de } f \text{ en el punto } (x_{0}, f(x_{0}))
$$

No veremos la definición del límite de rectas, simplemente tendremos una noción del mismo para poder estudiar las derivadas adecuadamente.

Luego de haber visto la noción de derivada, la próxima clase comenzaremos a estudiar las propiedades de la derivada.