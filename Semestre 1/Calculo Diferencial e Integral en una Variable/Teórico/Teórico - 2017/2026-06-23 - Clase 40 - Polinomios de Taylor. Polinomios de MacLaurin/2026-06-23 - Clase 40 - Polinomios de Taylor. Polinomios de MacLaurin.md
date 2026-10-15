# Polinomios de Taylor
Recordamos la función de derivada en un punto:

Recordatorio

> [!Recordatorio - Definición de derivada en un punto]
> $f$ es derivable en $x = a$ si y sólo si
> $$
> \lim_{ x \to a } \frac{f(x) - f(a)}{x - a} = f'(a) 
> $$

Una consecuencia de dicha definición es:

> [!Consecuencia]
> Si $f$ es derivable en $x = a$, entonces
> $$
> f(x) = \underbrace{ f(a) + f'(a)(x - a) }_{ P_{1}(x) } + E(x)
> $$
> donde
> $$
> \lim_{ x \to a } \frac{E(x)}{x - a} = 0 
> $$

De esta forma, se puede expresar $f(x)$ como un polinomio de primer grado formado por la imagen de $a$ y el producto de la derivada en $a$ por $x - a$, mas un término $E(x)$.

Esto no lo vimos cuando abordamos el tema derivada, por lo que lo digeriremos a continuación:
Si estudiamos la función lo suficientemente cerca de $a$, no obtenemos $f'(a)$ exactamente, si no
$$
\frac{f(x) - f(a)}{x - a} = f'(a) + \epsilon(k)
$$
donde
$$
\epsilon(x) = \frac{f(x) - f(a)}{x - a} - f'(a)
$$
A medida que nos acercamos a $a$, $\epsilon(k)$ tiende a 0.

**Observación**:
$$
\lim_{ x \to a } \epsilon(x) = 0 
$$

De esta forma, podemos desarrollar (directamente de la expresión anterior):
$$
f(x) - f(a) = f'(a)(x - a) + \epsilon(k)(x - a)
$$

Donde:
- $\epsilon(k)(x - a) = E(x)$
- Pasamos el $f(a)$ al lado derecho

$$
\implies f(x) = f(a) + f'(a)(x - a) + E(x)
$$

Geométricamente, $\underbrace{ f(a) + f'(a)(x - a) }_{ P_{1}(x) }$ es la ecuación de la recta tangente a la función $f(x)$ por el punto $(a, f(a))$.
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-06-23 - Clase 40 - Polinomios de Taylor. Polinomios de MacLaurin/Imágenes/1 - Representación geométrica.png]]

De esta manera, cuando una función es derivable en un punto $a$ en el interior de su dominio, que la función sea derivable en dicho punto quiere decir que podemos determinar una recta tangente al gráfico por $(a, f(a))$, y su ecuación está dada por $f(a) + f'(a)(x - a)$.

Si yo estudio puntos cercanos a $a$, por ejemplo, $x$, puedo ver que la recta no intercepta dichos puntos, aunque pasa cerca de los mismos. Por lo tanto, aquí podemos encontrar una diferencia, entre $P_{1}(x)$ y $f(x)$, la cual es precisamente el término $E(x)$.

Entonces, la igualdad dice que, localmente, mientras no me aleje demasiado de $a$, la diferencia entre $f(x)$ y $P_{1}(x)$ tenderá a 0 a medida que $x \to a$.

Lo que podemos sacar de esto es, que una función sea derivable en $a$, lo podemos traducir a, localmente podemos aproximar ese trozo de gráfica por la gráfica de algo más sencillo, en este caso un polinomio de primer grado.

De esta diferencia podemos decir lo siguiente:
$$
\lim_{ x \to a } E(x) = 0 
$$
Incluso:
$$
\lim_{ x \to a } \frac{E(x)}{x - a} = \lim_{ x \to a } \epsilon(x) = 0
$$
Esto nos dice que el numerador se achica más rápidamente que el denominador (ya que es un limite de tipo $\frac{0}{0}$).

Entonces, cuando aproximamos $f$ por una función más sencilla, la diferencia (error) obtenido será, en el peor de los casos, $x - a$.

**Observación**:
$$
P_{1}(a) = f(a), P_{1}'(x) = f'(a) \implies P_{1}'(a) = f'(a)
$$

Para tener una noción más física, teniendo en cuenta la igualdad original, si quitamos el término $E(x)$, la igualdad deja de ser tal y pasa a ser una aproximación, ya que la función no se comporta exactamente igual que la recta tangente, sino que es un comportamiento "similar" (al menos localmente):
$$
f(x) \simeq f(a) + f'(a)(x - a) \qquad (\forall x \text{ "cerca" de } a)
$$

Esto equivale a decir que, si $f(x)$ es la posición de una partícula en el tiempo $x$ y $f'(x)$ es la velocidad de una partícula en el tiempo $x$. Si conozco $f(a)$ y $f'(a)$ (la posición y velocidad de la partícula en el tiempo $a$), y quisiera sustituir dicha función de comportamiento por una más sencilla, podría utilizar $P_{1}(x)$. Si solo conozco los datos mencionados, la mejor predicción que puedo hacer es asumir que mantuvo la velocidad (velocidad constante), esto mientras la ventana considerada (radio alrededor de $a$) no sea demasiado grande. Esto funciona ya que el polinomio "repite" la velocidad $f'(a)$ durante todo su recorrido. Es una aproximación lineal.

Ahora, si además de conocer la posición y velocidad en $a$ conocemos la aceleración (derivada segunda), puedo realizar aproximaciones más exactas, si encuentro un polinomio de segundo grado que coincida con $f$, $f'$ y $f''$ en $a$ (al menos localmente). Este polinomio funcionaría aún mejor que el anterior, siendo la diferencia con $f$ menor (se reduce $E(x)$).

Buscamos $P_{2}(x) = a_{0} + a_{1}(x - a) + a_{2}(x - a)^{2}$ tal que
$$
\begin{align}
&P_{2}(a) = f(a) &&\implies a_{0} = f(a) \\
&P_{2}'(a) = f'(a) && P_{2}'(x) = a_{1} + 2a_{2}(x - a) &&\implies P_{2}'(a) = a_{1} = f'(a) \\
&P_{2}''(a) = f''(a) && P_{2}''(x) = 2a_{2} = f''(a) &&\implies a_{2} = \frac{f''(a)}{2}
\end{align}
$$

Desarrollamos un modelo simple considerando la posición de la partícula, su velocidad y su aceleración en $x = a$, tal que la trayectoria que predice ese modelo simple sea lo más similar posible a la trayectoria verdadera $f(x)$.

Originalmente, definimos
$$
P_{1}(x) = f(a) + f'(a)(x - a)
$$
el cual imitaba la posición y velocidad inicial.

Si estudiamos $P_{2}(x)$, tenemos que encontrar sus tres incógnitas, dadas por los datos $f(a), f'(a), f''(a)$. En el paso anterior las definimos, determinando que $a_{0}, a_{1}, a_{2}$ no pueden ser valores cualesquiera, si no:
$$
P_{2}(x) = f(a) + f'(a)(x - a) + \frac{f''(a)}{2}(x - a)^{2}
$$

Supongamos que tenemos aún más información disponible: $f$ tiene hasta derivada tercera en el punto $a$. En este caso, buscamos un polinomio que va a tener un término más:
$$
P_{3}(x) = a_{0} + a_{1}(x - a) + a_{2}(x - a)^{2} + a_{3}(x - a)^{3}
$$
Buscamos nuevamente los valores de los coeficientes:
$$
\begin{align}
&P_{3}(a) = f(a) &&\implies a_{0} = f(a) \\
&P_{3}'(a) = f'(a) && P_{3}'(x) = a_{1} + 2a_{2}(x - a) + 3a_{3}(x - a)^{2} \implies P_{3}'(a) = f'(a) &&\Longleftrightarrow a_{1} = f'(a) \\
&P_{3}''(a) = f''(a) && P_{3}''(x) = 2a_{2} + 2 \cdot 3 a_{3}(x - a) = f''(a) \implies P_{3}''(a) = 2a_{2} = f''(a) &&\Longleftrightarrow a_{2} = \frac{f''(a)}{2} \\
&P_{3}'''(a) = f'''(a) && P_{3}'''(x) = 3! a_{3} \implies P_{3}'''(a) = 3! a_{3} = f'''(a) &&\Longleftrightarrow a_{3} = \frac{f'''(a)}{3!}
\end{align}
$$
Entonces, definimos a $P_{3}(x)$ como:
$$
P_{3}(x) = f(a) + f'(a)(x - a) + \frac{f''(a)}{2}(x - a)^{2} + \frac{f'''(a)}{3!}(x - a)^{3}
$$

Como vemos, los coeficientes compartidos con $P_{2}(x)$ son idénticos.

Si graficáramos el polinomio $P_{3}(x)$, este debería ser aún más similar a la función $f(x)$, o dicho de otra forma: la diferencia entre $f(x)$ y $P_{3}(x)$ considerando un $x \to a$ debería ser menor a comparación de los polinomios anteriores (al menos alrededor de $a$).

Desarrollamos un polinomio $P_{4}(x)$ considerando que $f$ tiene derivada cuarta:
$$
P_{4}(x) = a_{0} + a_{1}(x - a) + a_{2}(x - a)^{2} + a_{3}(x - a)^{3} + a_{4}(x - a)^{4}
$$
$$
\begin{align}
&P_{4}(a) = f(a) &&\implies a_{0} = f(a) \\
&P_{4}'(a) = f'(a) && P_{4}'(x) = a_{1} + 2a_{2}(x - a) + 3a_{3}(x - a)^{2} + 4a_{4}(x - a)^{3} \implies P_{4}'(a) = f'(a) &&\Longleftrightarrow a_{1} = f'(a) \\
&P_{4}''(a) = f''(a) && P_{4}''(x) = 2a_{2} + 2 \cdot 3 a_{3}(x - a) + 3 \cdot 4 a_{4}(x - a)^{2} = f''(a) \implies P_{4}''(a) = 2a_{2} = f''(a) &&\Longleftrightarrow a_{2} = \frac{f''(a)}{2} \\
&P_{4}'''(a) = f'''(a) && P_{4}'''(x) = 3! a_{3} + 4! a_{4}(x - a) \implies P_{4}'''(a) = 3! a_{3} = f'''(a) &&\Longleftrightarrow a_{3} = \frac{f'''(a)}{3!} \\
&P_{4}^{(4)}(a) = f^{(4)}(a) && P_{4}^{(4)}(x) = 4! a_{4} \implies P_{4}^{(4)}(a) = 3! a_{3} = f^{(4)}(a) &&\Longleftrightarrow a_{4} = \frac{f^{(4)}(a)}{4!}
\end{align}
$$

Entonces:
$$
P_{3}(x) = f(a) + f'(a)(x - a) + \frac{f''(a)}{2}(x - a)^{2} + \frac{f'''(a)}{3!}(x - a)^{3} + \frac{f^{(4)}(a)}{4!}(x - a)^{4}
$$

En general, para ordenes altos de derivación, utilizamos la siguiente notación: $f^{(n)}(x)$, derivada de orden $n$ (derivada n-ésima) de $f$.

Ahora,¿ Qué pasa si $f$ se pudiera derivar $n$ veces, y queremos determinar un polinomio de grado $n$ que coincide con $f$ y sus $n$ derivadas en el punto $a$?

En tal caso, uno esperaría que hubiera un polinomio de la siguiente forma:
$$
P_{n}(x) = \frac{f(a)}{0!} + \frac{f'(a)(x - a)}{1!} + \frac{f''(a)(x - a)^{2}}{2!} + \dots + \frac{f^{(n)}(a)(x - a)^{n}}{n!}
$$
Se puede probar que el polinomio $P_{n}(x)$ se comporta igual que sus predecesores, agregando un término más de exactitud.

Podemos abreviar la expresión, considerando a $f$ como la derivada de orden 0:
$$
P_{n}(x) = \sum_{k = 0}^{n} \frac{f^{k}(a)}{k!} (x - a)^{k}
$$

A este polinomio lo denominaremos Polinomio de Taylor de orden $n$ de la función $f$ en el punto $a$, cuyos coeficientes se fabrican utilizando los valores de $f$ y de las derivadas en el punto $a$.

Podemos realizar la predicción física considerada anteriormente (comenzamos únicamente considerando la posición y velocidad en el punto $a$ ($n = 1$), luego la aceleración ($n = 2$), etc. - los siguientes casos no se ajustan bien a una intuición física, aunque se entiende la idea).

Definimos dicha estructura:

> [!Definición - Polinomio de Taylor]
> Sea $f$ derivable hasta el orden $n$ en $x = a$, siendo $a$ un punto en el interior del dominio de $f$. Entonces:
> $$
> P_{n}(f, a)(x) := \sum_{k = 0}^{n} \frac{f^{(k)}(a)}{k!} (x - a)^{k}
> $$
> Lo denominamos Polinomio de Taylor de $f$ en el punto $a$.

Uno de las principales motivaciones para utilizar polinomios de Taylor es que, a pesar de conocer la función $f$, la misma puede ser difícil de tratar, o incluso podemos solo conocer la imagen en $a$ y sus derivadas en $a$ y no mucho más, permitiendonos definir un polinommio, estructura bien conocida, con un comportamiento regular y con el que es sencillo trabajar.

De esta forma, aproximamos a $f$ por una función más sencilla y dócil, teniendo bastante fidelidad con la función original. Incluso en la computación, su uso es super extendido.

Igualmente, siempre es importante considerar que la diferencia entre $f$ y $P(f, a)(x)$ esté bien controlada, cosa que trataremos en el teorema de Taylor (próxima clase). Vimos que el "resto" disminuía más rápidamente que la diferencia entre $x$ y $a$. Luego veremos que a mayor orden, este resto ($\epsilon(x)$) decrece aún más deprisa.

Ahora, imaginemos que tenemos dos funciones $f$ y $g$, cada una con un polinomio de Taylor definido. Quiero estudiar la suma $f + g$. ¿Será posible utilizar los polinomios de cada función para definir un nuevo polinomio que se aproxime al comportamiento de $f + g$?
La respuesta es si, y se debe a lo siguiente:
$$
P_{n}(f, a)(x) \simeq f(x) \qquad (\forall x \in E(a, \delta))
$$
$$
P_{n}(g, a)(x) \simeq g(x) \qquad (\forall x \in E(a, \delta))
$$
En base a los anteriores, buscamos:
$$
P_{n}(\alpha f + \beta g, a)(x) \simeq \alpha f(x) + \beta g(x) \qquad (\forall x \in E(a, \delta))
$$
Si desarrollamos el arduo trabajo anterior de igualar cada uno de los coeficientes, llegamos a una solución. Sin embargo, no es necesario, ya que, considerando que la derivada de una combinación lineal es la combinación lineal de las derivadas, podemos iterar varias veces sobre este polinomio, concluyendo en que:
$$
\alpha P_{n}(f, a)(x) + \beta P_{n}(g, a)(x) 
$$
De esta forma, el Taylor de una combinación lineal, es la combinación lineal de los Taylor. Entonces, si conozco los polinomios de Taylor de las funciones habituales con las que componemos funciones más complejas, podremos fabricar polinomios de Taylor de dichas funciones más complejas. Esto se basa un poco en la idea de las tablas de derivada: conociendo como derivar las funciones básicas, podemos derivar cualquier función derivable utilizando dicha información, o integrar cualquier función (cuya primitiva se pueda expresar mediante funciones básicas).

Ahora, determinaremos los polinomios de Taylor de las funciones normalmente utilizadas, como $\sin(x), \cos(x), \log(x), e^{x}, \dots$

Es importante entender que los coeficientes de los polinomios se construyen considerando las derivadas en el punto $a$. Si cambio de punto, nada garantiza que el polinomio sea el mismo (lo más seguro es que sea distinto).

## Polinomios de Mc-Laurin

> [!Definición - Polinomios de Mc-Laurin]
> Un caso particular es $a = 0$:
> $$
> P_{n}(f, 0)(x) = \frac{f(0)}{0!} + \frac{f'(0)x}{1!} + \frac{f''(0)x^{2}}{2!} + \dots + \frac{f^{(n)}(0)x^{n}}{n!}
> $$
> Estos polinomios son denominados Polinomios de Mc-Laurin, y tienen una expresión propia:
> $$
> P_{n}(f, 0)(x) = \sum_{k = 0}^{n} \frac{f^{(n)}(0)}{k!} x^{k}
> $$

ACLARACIÓN: Siempre estamos asumiendo que $f$ es derivable $n$ veces, puesto que si no las operaciones no tienen sentido.

Procedemos a calcular los Polinomios de Mc-Laurin de las funciones tradicionales:

### Ejemplos de Polinomios de Mc-Laurin

#### Ejemplo 1: $f(x) = e^{x}$
$$
P_{n}(e^{x}, 0) = f(0) + f'(0)x + \frac{f''(0)x^{2}}{2!} + \dots + \frac{f^{(n)}(0)x^{n}}{n!}
$$
Sabemos que:
$$
\begin{align}
&f(0) = e^{0} = 1 \\
&f'(0) = e^{0} = 1 \\
&f''(0) = e^{0} = 1 \\
&\vdots \\
&f^{(n)}(0) = e^{0} = 1
\end{align}
$$

De esta forma, simplificamos:
$$
P_{n}(e^{x}, 0) = 1 + x + \frac{x^{2}}{2!} + \dots + \frac{x^{n}}{n!}
$$
Si estudiamos el signo del polinomio, sabiendo que la función $e^{x}$ es positiva en todo su dominio, podemos ver que (y se puede probar), efectivamente, que el polinomio es siempre positivo. Entonces, el polinomio se parece a la función más allá de su valor y el valor de sus derivadas en $x = 0$.

Sabemos que $e^{x}$ se puede derivar infinitas veces, pero si fijamos un $n$ determinado, el polinomio de Mc-Laurin correspondiente será el anterior.

Las funciones $\sin$ y $\cos$, al igual que $e^{x}$, son funciones infinitamente derivables, por lo que no tendremos problema para determinar el Polinomio de Mc-Laurin de dichas funciones para un $n$ cualquiera

#### Ejemplo 2: $f(x) = \sin(x)$
El polinomio tendrá la forma:
$$
P_{n}(\sin(x), 0) = \sin(0) + \cos(0)x - \frac{\sin(0)x^{2}}{2!} - \frac{\cos(0)x^{3}}{3!} + \dots + \frac{(\sin(x))^{(n)}x^{n}}{n!}
$$
Podemos determinar cada componente:
$$
\begin{align}
&f(0) = \sin(0) = 0 \\
&f'(x) = \cos(x) &&\implies f'(0) = \cos(0) = 1 \\
&f''(x) = -\sin(x) &&\implies f''(0) = -\sin(0) = 0 \\
&f'''(x) = -\cos(x) &&\implies f'''(0) = -\cos(0) = -1 \\
&f^{(4)}(x) = \sin(x) &&\implies f^{(4)}(0) = \sin(0) = 0
\end{align}
$$
Como vemos, se produce un patrón, un periodo 4 a partir del cual las derivadas dan siempre lo mismo.

Entonces:
$$
P_{n}(\sin(x), 0) = 0 + 1x - \frac{0}{2!}x^{2} - \frac{1}{3!}x^{3} + \frac{0}{4!}x^{4} + \frac{1}{5!}x^{5} + \dots + \frac{(\sin(x))^{(n)}x^{n}}{n!}
$$
Luego, veremos bien como queda el último término.

Ahora, podemos determinar un patrón: las derivadas de orden par evaluadas en 0 dan 0, ya que son $\sin(0)$ o $-\sin(0)$. Entonces, solo tenemos sumandos de potencia impar (ya que los pares se anulan), y además los signos se van alternando, comenzando con positivo:
$$
P_{n}(\sin(x), 0) = x - \frac{x^{3}}{3!} + \frac{x^{5}}{5!} - \frac{x^{7}}{7!} + \frac{x^{9}}{9!} - \dots + \frac{f^{(n)}(0)}{n!} x^{n}
$$

Para entender un poco mejor el caso, abordaremos un ejemplo más sencillo:
$$
\begin{align}
&P(x) &&= x - x^{3} \\
&P(-x) &&= -x - (-x^{3}) \\
&&&= -x + x^{3}) \\
\implies &P(-x) = -P(x)
\end{align}
$$
Este tipo de funciones se llaman funciones impares, donde $f(x)$ y $f(-x)$ son opuestas, por lo tanto: $f(-x) = -f(x)$. Se les llama funciones impares ya que los ejemplos clásicos son $x, x^{3}, x^{5}, \dots$

Entonces, si estudiamos la función $\sin(x)$, podemos ver que también es una función impar, ya que cumple que $-\sin(x) = \sin(-x)$.
Y de esta forma, el polinomio de Taylor imitador de la función $\sin(x)$ también es una función impar lo que es positivo ya que hace que la función sea aún más aproximada.

Sabiendo esto, podemos llegar a una expresión para el último término del polinomio, que sea positivo cuando $n \in \{ 1, 5, 9, \dots \}$ y negativo cuando $n \in \{ 3, 7, 11, \dots \}$. Consideremos el siguiente término:
$$
P(\sin(x), 0) = \dots + (-1)^{n} \frac{x^{2n + 1}}{(2n + 1)!}
$$

Ahora, nos aseguramos de que dicho término sea correcto:
$$
\begin{align}
&n = 0 \implies \frac{x^{1}}{1!} \\
&n = 1 \implies -\frac{x^{3}}{3!} \\
&n = 2 \implies \frac{x^{5}}{5!} \\
&n = 3 \implies -\frac{x^{7}}{7!} \\
&\vdots
\end{align}
$$
Por inducción, se puede probar la correctitud de dicho término.

Finalmente, encontramos una forma de representar el Polinomio de Mc-Laurin de la función seno como una sumatoria de dichos términos:
$$
P_{2n + 1}(\sin(x), 0)(x) = \sum_{k = 0}^{n} \frac{(-1)^{k} x^{2k + 1}}{(2k + 1)!}
$$
$$
P_{2n + 1}(\sin(x), 0) = x - \frac{x^{3}}{3!} + \frac{x^{5}}{5!} - \frac{x^{7}}{7!} + \frac{x^{9}}{9!} - \dots + (-1)^{n} \frac{x^{2n + 1}}{(2n + 1)!}
$$
Básicamente, identificamos un patrón y sintetizamos el patrón para desarrollar un término genérico con el que notar el último término del polinomio.

Ahora, hacemos lo mismo para la función coseno:
#### Ejemplo 3: $f(x) = \cos(x)$
Primero, identificamos los valores para entender el patrón:
$$
\begin{align}
&f(0) = \cos(0) = 1 \\
&f'(x) = -\sin(x) &&\implies f'(0) = -\sin(0) = 0 \\
&f''(x) = -\cos(x) &&\implies f''(0) = -\cos(0) = -1 \\
&f'''(x) = \sin(x) &&\implies f'''(0) = \sin(0) = 0 \\
&f^{(4)}(x) = \cos(0) &&\implies f^{(4)}(0) = \cos(0) = 1
\end{align}
$$
Como vemos, aquí también visualizamos un bucle que se repite cada 4 elementos, pero ahora son los sumandos pares los que se anulan. Esto tiene sentido ya que la función $\cos(x)$ es una función par (cumple que $f(x) = f(-x)$), lo que indica una relación más allá de la imagen y las derivadas en 0.

Desarrollamos el polinomio correspondiente:
$$
P_{n}(\cos, 0)(x) = 1 + 0x - \frac{1x^{2}}{2!} + \frac{0x^{3}}{3!} + \frac{1x^{4}}{4!} + \frac{0x^{5}}{5!} - \frac{1x^{6}}{6!} + \dots + \frac{f^{(n)}(0)x^{n}}{n!}
$$
Ignoramos los nulos:
$$
P_{n}(\cos, 0)(x) = 1 - \frac{1x^{2}}{2!} + \frac{1x^{4}}{4!} - \frac{1x^{6}}{6!} + \frac{1x^{8}}{8!} - \frac{1x^{10}}{10!} \dots + \frac{f^{(n)}(0)x^{n}}{n!}
$$

Ahora, buscamos un término genérico para definir la esencia del patrón y representar a cada uno de los términos. Podemos considerar:
$$
\frac{(-1)^{n} x^{2n}}{(2n)!}
$$
$$
\begin{align}
&n = 0 \implies 1 \\
&n = 1 \implies -\frac{x^{2}}{2!} \\
&n = 2 \implies \frac{x^{4}}{4!} \\
&n = 3 \implies -\frac{x^{6}}{6!} \\
&\vdots
\end{align}
$$
De esta forma:
$$
P_{2n}(\cos, 0)(x) = 1 - \frac{1x^{2}}{2!} + \frac{1x^{4}}{4!} - \frac{1x^{6}}{6!} + \frac{1x^{8}}{8!} - \frac{1x^{10}}{10!} \dots + \frac{(-1)^{n} x^{2n}}{(2n)!}
$$

Al igual que para las derivadas y primitivas, existen tablas con los Polinomios de Taylor y de Mc-Laurin de funciones conocidas.

#### Ejemplo 4: $f(x) = \log(1 + x)$
Como estudiamos puntos de Mc-Laurin donde el punto de interés es 0, en lugar de trabajar con $\log(x)$, que con $x = 0$ es $\log(0)$ que no está definida, estudiaremos $\log(x + 1)$.

Realizamos el mismo procedimiento de siempre:
$$
\begin{align}
&f(0) = \log(1) = 0 \\
&f'(x) = \frac{1}{1 + x} &&\implies f'(0) = \frac{1}{1} = 1 \\
&f''(x) = -\frac{1}{(1 + x)^{2}} &&\implies f''(0) = -1 \\
&f'''(x) = \frac{2}{(1 + x)^{3}} &&\implies f''''(0) = 2! \\
&f^{(4)}(x) = -\frac{2 \cdot 3}{(1 + x)^{4}} &&\implies f^{(4)}(0) = -3! \\
&f^{(5)}(x) = \frac{2 \cdot 3 \cdot 4}{(1 + x)^{5}} &&\implies f^{(5)}(0) = 4! \\
&f^{(6)}(x) = -\frac{2 \cdot 3 \cdot 4 \cdot 5}{(1 + x)^{6}} &&\implies f^{(6)}(0) = -5! \\
&\vdots \\
&f^{(k)}(x) = -\frac{(k - 1)!}{(1 + x)^{k}} &&\implies f^{(k)}(0) = (-1)^{k - 1}(k - 1)!
\end{align}
$$
De esta forma, se puede demostrar por inducción completa que la forma de los términos es la definida.

ACLARACIÓN: Es más sencillo estudiar la derivada de $-\frac{1}{(1 + x)^{2}}$ como $(1 + x)^{-2}$, y luego pasar el coeficiente que sale de derivar la función exponente multiplicando al numerador y cambiando el signo.

Entonces, podemos desarrollar el polinomio de Mc-Laurin de dicha función:
$$
\begin{align}
P_{n}(\log, 0)(x) &= 0 + 1x - \frac{1}{2!}x^{2} + \frac{\cancel{ 2! }}{3\cancel{ ! }}x^{3} - \frac{\cancel{ 3! }}{4\cancel{ ! }}x^{4} + \frac{\cancel{ 4! }}{5\cancel{ ! }}x^{5} - \dots + \frac{(-1)^{n}\cancel{ (n - 1)! }}{n\cancel{ ! }}x^{n} \\
&= x - \frac{x^{2}}{2} + \frac{x^{3}}{3} - \frac{x^{4}}{4} + \frac{x^{5}}{5} - \dots + \frac{(-1)^{n} x^{n}}{n}
\end{align}
$$

La próxima clase, probaremos el teorema de Taylor que da condiciones de existencia y unicidad, y además establece la velocidad con la que tiende a 0 la diferencia entre el polinomio y la función. Por ahora, sospechamos que a medida que aumenta $n$, la calidad de la aproximación mejora notoriamente. Con el teorema de Taylor, formalizaremos dicha intuición.