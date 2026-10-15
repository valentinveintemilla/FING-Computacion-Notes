# Límites y continuidad
En esta clase veremos nuevas propiedades algebraicas.

# Propiedades algebraicas

## Proposición

> [!Proposición]
> Sea $f: I \to \mathbb{R}$, y $x_{0} \in \overset{-} I$
> Si
> - $f(x) \neq 0 \qquad \text{para todo } x \in I$
> - $\lim_{ x \to x_{0} } f(x) = L \neq 0$
> Entonces
> $$
> \lim_{ x \to x_{0} } \frac{1}{f(x)} = \frac{1}{L}
> $$

(Es necesario especificar las dos condiciones, puesto que una no implica la otra)

Antes de demostrar la propiedad veremos un corolario.

> [!Corolario]
> Si $f, g : I \to \mathbb{R}$, y $x_{0} \in \overset{-} I$
> 
> Si $\lim_{ x \to x_{0} } f(x) = L \in \mathbb{R}$
> Si $\lim_{ x \to x_{0} } g(x) = L' \neq 0$
> 
> Entonces
> $$
> \lim_{ x \to x_{0} } \frac{f(x)}{g(x)} = \frac{L}{L'}
> $$

Podemos ver que el corolario se deduce a partir de la proposición. El cociente entre $f$ y $g$, es equivalente al producto de $f$ por $\frac{1}{g}$. Gracias a la proposición anterior, se que $\frac{1}{g}$ tiene límite, y esto nos permite usar la propiedad del producto para resolver el problema. Por esta razón, no lo demostraremos.

**Idea de la demostración**:
$$
\frac{f}{g} = f \times \frac{1}{g}
$$

### Demostración de la proposición
Se observa que $\forall x \in I$:
$$
\frac{1}{f(x)} - \frac{1}{L} = \frac{L - f(x)}{f(x) L} = -\frac{1}{L} \cdot \frac{1}{f(x)} \cdot \underbrace{ (f(x) - L) }_{ \to 0 }
$$

Aclaración, desarrollo completo del producto:
$$
\begin{align}
&\frac{1}{f(x)} - \frac{1}{L} = \frac{L - f(x)}{f(x) L} \\ \\

&\text{Sabiendo que } L - f(x) = - (f(x) - L) \\ \\

&\frac{- (f(x) - L)}{f(x) L} = \left( -\frac{1}{Lf(x)} \right) \cdot (f(x) - L) = -\frac{1}{L} \cdot \frac{1}{f(x)} \cdot \underbrace{ (f(x) - L) }_{ \to 0 }
\end{align}
$$
Analizaremos cada uno de los puntos:
Como sabemos, cuando $x$ tiende a $x_{0}$, $f(x)$ tiende a $L$, por lo que en este caso, cuando $x$ tiende a $x_{0}$, $f(x) - L$ tiende a 0.

La clase pasada, vimos una propiedad que establecía que el producto de una función que tiene límite 0 por una función localmente acotada, es otra función que también tiene límite 0. Por esta razón, lo que nos queda demostrar es que $-\frac{1}{L} \cdot \frac{1}{f(x)}$ es localmente acotada. $-\frac{1}{L}$ es localmente acotada, pues $L$ es un valor fijo. Sin embargo, nos queda demostrarlo para $\frac{1}{f(x)}$.

Al finalizar, podremos aplicar la propiedad mencionada, y llegaremos a la conclusión de que $\frac{1}{f(x)} - \frac{1}{L}$ tiene límite 0, demostrando lo que buscamos.

Sea $\epsilon = \frac{|L|}{2} > 0$.
Como $f(x) \underset{x \to x_{0}} \to L$, existe $\delta > 0$ tal que
$$
\forall x \in E^{*}(x_{0}, \delta), |f(x) - L| < \epsilon
$$
Para todo $x \in E^{*}(x_{0}, \delta)$, se observa que:
$$
\begin{align}
|L| &= |f(x) - (f(x) - L)| \\
&\leq |f(x)| + |f(x) - L| < |f(x)| + \overbrace{ \frac{|L|}{2} }^{ \epsilon }
\end{align}
$$
($|L| = |f(x) - (f(x) - L)|$ parece totalmente artificial, pero se justifica por el resultado posterior)

Ahora, utilizamos la desigualdad al revés:
$$
|f(x)| > |L| - \frac{|L|}{2} = \frac{|L|}{2}
$$

De esta forma, obtuvimos una minoración de $f(x)$.
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-04-10 - Clase 21 - Límites, Monotonía, Teorema del Sándwich/Imágenes/1 - Representación de demostración.png]]
Gracias a las desigualdades alcanzadas (y representación anterior), sabemos que $f(x)$ en el intervalo $(x_{0} - \delta, x_{0} + \delta)$, la función se queda en la zona demarcada por $(L - \epsilon, L + \epsilon)$, y como $\epsilon = \frac{|L|}{2}$, deducimos que en esta región, la función vale al menos $\frac{|L|}{2}$ (en valor absoluto).

Así, hallamos una cota inferior para $f$. Esto es sumamente útil, ya que cuando invirtamos la función ($\frac{1}{f(x)}$), tendremos una cota superior.

Entonces, podemos deducir que:
$$
\left| \frac{1}{f(x)} \right| < \frac{2}{|L|} \qquad \forall x \in E^{*}(x_{0}, \delta) \cap I
$$
Así, la función $f$ está localmente acotada. Como vemos, esto no considera lo que sucede en $x_{0}$.

Si queremos extender la propiedad, tenemos que añadir una cota específica para $x_{0}$:

Luego:
$$
\left| \frac{1}{f(x)} \right| < máx\left( \frac{2}{|L|}, \frac{1}{|f(x_{0})|} \right) \qquad \text{en } E(x_{0},\delta) \cap I
$$
Sabemos que esta última cota funciona en todos los casos, evitando que $x_{0}$ quede fuera de la cota.

La idea fue encontrar una cota inferior para $f(x)$, para luego invertir la función y tener una cota superior.

En conclusión, la función esta localmente acotada, por lo que podemos aplicar el lema en la proposición original:
$$
\underbrace{ \frac{1}{f(x)} - \frac{1}{L} }_{ \underset{x \to x_{0}} \to 0 } = \frac{L - f(x)}{f(x) L} = \underbrace{ -\frac{1}{L} \cdot \frac{1}{f(x)} }_{ \text{localmente acotado} } \cdot \underbrace{ (f(x) - L) }_{ \underset{x \to x_{0}} \to 0 }
$$
En definitiva, $\frac{1}{f(x)}$ tiende a $\frac{1}{L}$.

Esto es una prueba más de la complejidad de los límites y el porque llevó tanto desarrollar la teoría.

---
Ahora, veremos un pequeño contraejemplo sobre las condiciones de la proposición: $f(x) \neq 0 \qquad \text{para todo } x \in I$   no implica que   $\lim_{ x \to x_{0} } f(x) = L \neq 0$

### Observación
> [!Observación]
> Sea $f : \mathbb{R} \to \mathbb{R}$ definida por $f(x) = \begin{cases} \begin{align} &|x| &&\text{si} &x \neq 0  \\ &1 &&\text{si} &x = 0 \end{align} \end{cases}$
> 
> La función definida es estrictamente positiva
> $$f(x) > 0 \qquad \forall x \in \mathbb{R}$$
> pero
> $$
> \lim_{ x \to 0 } f(x) = 0
> $$

Así vemos que la condición $f(x) \neq 0 \qquad \text{para todo } x \in I$ no implica que $\lim_{ x \to x_{0} } f(x) = L \neq 0$, hay que verificarlo. Sin embargo, al revés tenemos la implicación recíproca al menos localmente. Cada vez que tenemos un limite no nulo, tenemos un entorno reducido donde la función no se anula, aunque puede pasar en $x_{0}$ (pero no alrededor de este).

---
Recordamos varias de las propiedades algebraicas abordadas en estas clases:

> [!Recordatorio]
> $$
> \lim_{x \to x_{0}} (f + g) = \lim_{x \to x_{0}} f + \lim_{x \to x_{0}} g
> $$
> $$
> \lim_{x \to x_{0}} (f - g) = \lim_{x \to x_{0}} f - \lim_{x \to x_{0}} g
> $$
> $$
> \lim_{x \to x_{0}} f g = \lim_{x \to x_{0}} f \times \lim_{x \to x_{0}} g
> $$
> $$
> \lim_{x \to x_{0}} \frac{f}{g} = \frac{\lim_{x \to x_{0}} f}{\lim_{x \to x_{0}} g} \qquad \text{si } \lim_{x \to x_{0}} g \neq 0
> $$

En el caso particular donde las funciones $f$ y $g$ son continuas, entonces su suma, diferencia, y producto y cociente (si el límite en $g$ nunca se anula) son también continuos. Esta propiedad de continuidad la supondremos para las instancias de evaluación del curso. No es necesario demostrar nada, simplemente se trata de una verificación.

En general, siempre que haya un caso con división, es fundamental verificar que el divisor no sea ni pueda ser 0.

Ahora, ¿Qué pasa cuando una de las dos es discontinua? Aquí, el resultado necesariamente es discontinuo.

### Ejercicio
Demostrar que si $f$ es continua y $g$ es discontinua (al menos en un punto), entonces $f + g$ es discontinua (al menos en un punto).

En lugar de utilizar $\epsilon$ y $\delta$, que estan bien para las definiciones, es mucho más simple utilizar los teoremas. En este caso, demostraremos por el absurdo:

Por el absurdo, supongamos que $f + g$ fuera continua.
$$
\underbrace{ (f + g) - f }_{ g \text{: absurdo!} } \text{ es continua}
$$
De esta forma, llegamos rápidamente al resultado deseado, sin necesidad de realizar un arduo trabajo.

Ahora, ¿Qué pasa si sumamos dos funciones discontinuas? Aquí, puede darse cualquiera de los dos casos. La función resultante puede ser continua o discontinua.

### Ejemplo
Sea $D$ una función discontinua.
$$
D + D = 2D \qquad \text{discontinua}
$$
$$
D + (-D) = 0 \qquad \text{continua}
$$
Para construir este contraejemplo, se puede tomar cualquier función discontinua.

En cuanto a las propiedades algebraicas, esto es todo lo que tenemos que saber.

---
A continuación, abordaremos propiedades de monotonía.

En análisis, siempre definimos una noción, estudiamos sus propiedades algebraicas (suma, resta, etc., como se opera), y luego sus propiedades de orden, pues de esto se tratan los reales.
Ahora abordaremos el orden.

# Propiedades de monotonía

## Lema

> [!Lema]
> Sea $f : I \to \mathbb{R}$ tal que $f(x) \geq 0$ para todo $x \in I \qquad (f \geq 0)$
> 
> Si $f$ tiene límite en un punto $x_{0} \in \overset{-} I$, entonces
> $$
> \lim_{ x \to x_{0} } f(x) \geq 0
> $$

Esto se puede demostrar a menos de $\epsilon$, o por el absurdo.

Nosotros lo haremos por el absurdo:

Si $L < 0$ (por el absurdo)
Se toma $\epsilon = |L|$

![[2 - Demostración de lema.png]]

Esto define una banda sabiendo que los valores dentro de la mismo son todos negativos, lo que es una contradicción.
La idea es la misma de siempre, con la particularidad de que aquí la utilizamos para establecer una función en la que la función es negativa entre las bandas especificadas, contradiciendo la hipótesis inicial.

Aunque suponemos que $f$ es estrictamente positiva, no podemos suponer que el límite también lo es. Por ejemplo, en la función de valor absoluto que desarrollamos anteriormente no pasa (tiende a 0).
Esto es general para las propiedades de monotonía: ==las propiedades de monotonía solo funcionan para el orden amplo, no para el orden estricto==.

Veremos un corolario relacionado a todo esto:

> [!Corolario]
> Si $f, g : I \to \mathbb{R}$ son tales que $f \leq g$ en $I$, y si tienen límites en $x_{0} \in \overset{-} I$, entonces
> $$
> \lim_{ x \to x_{0} } f(x) \leq \lim_{ x \to x_{0} } g(x)
> $$

Cuando tengo dos funciones que están en un orden particular (orden amplio, no estricto), entonces tengo el mismo orden para los límites (si es estricta, el resultado aún sigue siendo amplio).

Es una consecuencia obvia, simplemente hay que considerar la función $g - f$. Si $f \leq g$, entonces la función $g - f$ es positiva o nula, entonces cuando tiene límite es positivo o nulo, pero su límite es la diferencia entre el límite de $g$ y el límite de $f$.

En general, para la mayoría que propiedades que demostraremos, primero las demostraremos para cero, y después, por traslación, se deduce para dos funciones cualesquiera.

---
Hasta ahora hemos trabajado sin mucha dificultad, suponiendo que todas las funciones tenían límites.

A continuación veremos una propiedad interesante: el Teorema del Sándwich.

# Teorema del Sándwich

Suponemos que tenemos dos funciones (trozos de pan) en el plano, $g_{1}$ y $g_{2}$. Además, hay una tercera función que se mueve entre estas, manteniendo el orden $g_{1} \leq f \leq g_{2}$.
Si en algún punto $g_{1}$ y $g_{2}$ tienen el mismo límite, entonces podemos deducir que $f$ también tiene el mismo límite (fuerza el límite de $f$).
![[3 - Teorema del Sándwich.png]]

> [!Teorema del Sándwich]
> Sean $f, g_{1}, g_{2} : I \to \mathbb{R}$ tales que
> $$
> g_{1}(x) \leq f(x) \leq g_{2}(x) \qquad \forall x \in I
> $$
> Dado un punto $x_{0} \in \overset{-} I$, si $g_{1}$ y $g_{2}$ tienen el mismo límite en el punto $x_{0}$, entonces $f$ también tiene el mismo límite en $x_{0}$.

No lo demostraremos, pero la idea de la demostración es que de la función $g_{1}$ obtendré una correspondencia de $\epsilon$ y $\delta_{\epsilon}$, y para $g_{2}$ obtendré una correspondencia de $\epsilon$ y $\delta'_{\epsilon}$, y a partir de varias funciones puedo construir una correspondencia que funcione bien para $f$.

Es muy útil para trabajar con funciones complicadas $f$, y no sabemos demostrar que tienen límites en $x_{0}$. Sin embargo, a veces $f$ está rodeada de funciones $g_{1}$ y $g_{2}$ las cuales tienen límite en $x_{0}$, permitiéndonos deducir el límite para dicha función.

Veremos algunos ejemplos:

## Ejemplo 1
Sea $f : \mathbb{R} \to \mathbb{R}$ definida por $f(x) = \begin{cases} \begin{align} &x &&\text{si} & x \in \mathbb{Q} \\ &-x &&\text{si} &x \not \in \mathbb{Q} \end{align} \end{cases}$   (similar a la función de Dirichlet)
Se observa que $-x \leq f(x) \leq x \qquad \forall x \in \mathbb{R}$

En el punto 0, $-x$ tiende a 0, $x$ tiende a 0, y luego, por Sándwich, $f(x)$ tiende a 0.

Llegamos a la conclusión sin utilizar $\epsilon$ ni $\delta$, nuevamente.
Es más difícil demostrar que es discontinua en todos los puntos, menos en el punto 0.

## Ejemplo 2
Se recuerda que
$$
\log (x) = \int_{1}^{x} \frac{dt}{t} \qquad \forall x > 0
$$
En particular: $\log 1 = 0$

Queremos demostrar que la función es continua en 1, pero la definición nos dificulta un poco las cosas.

Ya vimos que
$$
1 - \frac{1}{x} \leq \log x \leq x - 1 \qquad \forall x > 0
$$
$(\log : \mathbb{R}^{+} \to \mathbb{R})$

La propiedad anterior fue demostrada utilizando la integral de cada una de las funciones:
$$
\frac{1}{x} \leq \frac{1}{t} \leq 1
$$
Al desarrollar la integral de cada función, llegamos a la conclusión de que:
$$
1 - \frac{1}{x} \leq \log x \leq x - 1 \qquad \forall x > 0
$$

Tomando en cuenta esto, cuando $x$ tiende a 1 podemos decir que:
- $1 - \frac{1}{x}$ tiende a 0
- $x - 1$ tiende a 0

De esta forma, por Sándwich, podemos deducir que $\log 1$ tiende a 0:
$$
\underbrace{ 1 - \frac{1}{x} }_{ \to 0 } \leq \underbrace{ \log x }_{ \to 0 } \leq \underbrace{ x - 1 }_{ \to 0 } \qquad \forall x > 0
$$
Conclusión:
$$
\lim_{ x \to 1 } \log (x) = 0 = \log (1)
$$
$\log$ es continua en $x_{0} = 1$

Lo interesante de estudiar la desigualdad anterior, es que si la dividimos por $x-1$, también obtendremos la propiedad de derivada de logaritmo.

Como vemos, el teorema del Sándwich es super útil para facilitar ciertas demostraciones cuando tenemos conocimiento de funciones que envuelvan a la función con la que estamos trabajando.

---
Concluiremos la clase con composición de funciones.

# Composición de funciones
> [!Composición de funciones]
> Sean $f: I \to \mathbb{R}$ y $g : J \to \mathbb{R}$, tales que $f(I) \subset J$, es decir
> $$
> \forall x \in I, f(x) \in J
> $$
> En esta situación, se puede definir
> $$
> g \circ f : I \to \mathbb{R}
> $$
> por
> $$
> (g \circ f)(x) = g(f(x)) \qquad \forall x \in I
> $$

Queremos como esta operación afecta a los límites.

## Proposición

> [!Proposición]
> Si $x_{0} \in \overset{-} I$ y si $\lim_{ x \to x_{0} } f(x) = y_{0} \in J$ y si $g$ es continua en $y_{0} (\in J)$, entonces
> $$
> \lim_{ x \to x_{0} } (g \circ f)(x) = g(y_{0})
> $$

No demostraremos el teorema, aunque no es complicado. La idea es, sabiendo que para cada límite tengo un radio para todas las precisiones, partimos de una precisión, y aplicando la función $\epsilon \mapsto \delta_{\epsilon}$ de $g$ obtengo un $\delta$ que va a convertirse en una precisión, usando la segunda función al revés.

Lo importante es que la proposición anterior es el resultado general de la composición para los límites, aunque hay una forma más sencilla, que es un caso particular.

### Caso particular

> [!Caso particular]
> Si $f$ es continua en $x_{0} \in I$
> y $g$ es continua en $y_{0} = f(x_{0}) \in J$
> entonces $g \circ f$ es continua en $x_{0}$

Vamos a utilizar este último, que es el más sencillo e interesante en la practica. Si tomo dos funciones continuas y desarrollo la composición, obtendré otra función continua (la continuidad se preserva por composición de funciones).