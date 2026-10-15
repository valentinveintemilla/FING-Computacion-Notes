# Integrales
Tenemos una función $f: [a,b] \to \mathbb{R}$ acotada y queremos calcular el área algebraica (con su correspondiente signo según su posición con respecto al eje x). Como no había una formula establecida para calcular dicha área, desarrollamos aproximaciones por exceso y por defecto.
$$
\begin{align}
&\{ S_{*}(f,P): P \subset [a,b] \text{ partición} \} \\
&\{ S^{*}(f,P): P \subset [a,b] \text{ partición} \}
\end{align}
$$
Entonces, buscamos calcular el área algebraica, valor que aún no conocemos, pero tenemos un conjunto de aproximaciones por defecto (sumas inferiores, sumas de áreas de los rectángulos construidos a partir del ínfimo de cada subintervalo), además de un conjunto de aproximaciones por exceso (sumas superiores, sumas de áreas de los rectángulos construidos a partir del supremo de cada subintervalo).

También vimos que cada aproximación por defecto es menor o igual a cada aproximación por exceso, y lo demostramos.

Lo natural en este punto es definir un valor ideal para cada uno de los conjuntos, el supremo de las sumas inferiores y el ínfimo de las sumas superiores:
$$
\begin{align}
&I_{*}(f) := sup\{ S_{*}(f,P): P \subset [a,b] \text{ partición} \} \\
&I^{*}(f) := ínf\{ S^{*}(f,P): P \subset [a,b] \text{ partición} \} \\ \\

&I_{*}(f) \leq I^{*}(f)
\end{align}
$$
De esta forma, también podemos definir que la integral inferior de f siempre es menor o igual a la integral inferior de f, y esto se cumple en todos los casos.

En el caso de que ambos valores sean iguales, necesariamente tiene que ser el valor del área algebraica, puesto que sabemos que el área se encuentra entre estos dos números.
![[Representación de suma inferior y suma superior.png]]

**Definición**
Una función $f:[a,b] \to \mathbb{R}$ acotada es <u>integrable</u> cuando $I_{*}(f) = I^{*}(f)$.
Se escribe:
$$
\int_{a}^{b}f = \int_{a}^{b}f(x) dx := I_{*}(f) = I^{*}(f)
$$
Esta notación es válida únicamente cuando $I_{*}(f) = I^{*}(f)$, en caso contrario no tiene sentido.

Ahora, veremos que esta definición tiene sentido.

## Observación
Para toda partición $P \subset [a,b]$
$$
S_{*}(f,P) \leq \int_{a}^{b}f \leq S^{*}(f,P)
$$
De esta forma, la integral siempre es mayor o igual que todas las sumas inferiores y menor o igual que todas las sumas superiores., de esta forma se encuentra entre ambos conjuntos.

Caso particular: $P=\{a,b\}$ (partición más gruesa del intervalo)
En este caso tenemos que
![[Representación de suma inferior y suma superior caso particular.png]]
$$
\begin{align}
&S_{*}(f,P) = (b-a) \cdot ínf(f) \\
&S^{*}(f,P) = (b-a) \cdot sup(f) \\ \\ \\

&\text{Esto determina la siguiente igualdad: } \\
&(b-a) \cdot ínf(f) \leq \int_{a}^{b}f \leq (b-a) \cdot sup(f)
\end{align}
$$
Esto se debe a que hay un único subintervalo, por lo que tenemos un sumando del área del rectángulo que corresponde.
Todo esto son cosas triviales, pero nos asegura que nuestra definición no es trivial. Es fundamental asegurarnos de que mantuvimos el sentido de los conceptos iniciales (supremo, ínfimo, entre otros) en todo momento.

El problema es el siguiente: decimos que una función es integrable cuando $I_{*}(f) = I^{*}(f)$. Ahora, tenemos que probar que existe al menos una función integrable (que si las hay, y muchas).

Ahora veremos dos ejemplos, una función integral y otra que no lo es (donde no se puede capturar el área).

Aclarar que estas nociones tienen sentido cuando la función es bastante regular, siendo un ejemplo perfecto la función constante.

## Ejemplo
Sea una función constante:
$$
f: [a,b] \to \mathbb{R} \text{ definida por: } f(x)=k(\in \mathbb{R})
$$![[Funciones regulares.png]]
Ya de antemano, sabemos que el resultado del área algebraica será $(b-a)k$. Igualmente, haremos el desarrollo.

Sea $P = \{ a_{0},a_{1},\dots,a_{n} \} \subset [a,b]$
En cada subintervalo $[a_{i}, a_{i+1}]$ tenemos que
$$
\begin{align}
&ínf(f,[a_{i},a_{i+1}]) = k \\
&sup(f,[a_{i},a_{i+1}]) = k
\end{align}
$$
Como vemos, el ínfimo y supremo en cada subintervalo son iguales, de modo que la suma inferior y la suma superior son iguales (pues lo único que las diferenciaba era el ínfimo y el supremo).
$$
S_{*}(f,P) = S^{*}(f,P) = \sum_{i=0}^{n-1}(a_{i+1}-a_{i})k = k\sum_{i=0}^{n-1}(a_{i+1}-a_{i})=k(b-a)
$$
Al final, sumamos las longitudes de todos los subintervalos, que es equivalente a $b-a$, quedando $k(b-a)$. El truco es que estaba haciendo sumatoria de la longitud de cada subintervalo, y cuando sumo todos estos valores, obtengo la longitud del intervalo $[a,b]$, la longitud global.

Esto se puede demostrar de modo algebraico, con un método de simplificación de A2:
$$
\begin{align}
&\sum_{i=0}^{n-1} (a_{i+1} - a_{i}) = \sum_{i=0}^{n-1} (-a_{i} + a_{i+1}) \\
&=(-a_{0} + \cancel{ a_{1} }) + (\cancel{ -a_{1} } + \cancel{ a_{2} }) + (\cancel{ -a_{2} } + \cancel{ a_{3} }) + \dots + (\cancel{ -a_{n-1} } + a_{n}) \\
&=-a_{0} + a_{n} = a_{n} - a_{0} = b - a
\end{align}
$$
Esta expresión demuestra que la suma de las longitudes de los subintervalos es igual a la longitud del intervalo global.

Entonces, podemos concluir que $k(b-a)$ no depende de $P$. Esto es un caso super particular, en el que todas las aproximaciones por exceso y por defecto son iguales. De esta forma, se representa en una recta como un punto, en el que coinciden $k(b-a) = S_{*}(f,P) = S^{*}(f,P)$.

Tenemos que
$$
\begin{align}
&I_{*}(f)=(b-a)k \\
&I^{*}(f)=(b-a)k
\end{align}
$$
Luego: $\int_{a}^{b}f=(b-a)k$

La predicción que hicimos era correcta: el área de la función constante $f(x)=k$ es $(b-a)k$.
Con esto podemos determinar que todas las funciones constantes son integrables. Aquí vimos un ejemplo trivial de funciones en las que se puede observar inmediatamente que son integrales.

Sin embargo, también existen funciones no integrales, funciones que destruyen la teoría de la integración.

## Ejemplo
La función de Dirichlet $f: [0,1] \to \mathbb{R}$ es definida por:
$$
f(x)=\begin{cases}
1 \text{ si } x \in \mathbb{Q} \\
0 \text{ si } x \not \in \mathbb{Q}
\end{cases}
$$
Como vemos, es una función bien definida. Sin embargo, prácticamente no la podemos graficar, puesto que al graficar, lo hacemos de modo finito. Es super irregular, puesto que está llena de saltos de continuidad.
Por ejemplo, si tomamos el valor $\sqrt{ 2 } - 1$, su imagen es 0, sin embargo, la imagen de todos los números que tienden a $\sqrt{ 2 } - 1$ por la izquierda y por la derecha es 1, y esta misma situación se repite por todas partes en el intervalo.
Es una función que no sirve en la práctica, pero es fundamental para probar la robustez de la teoría.

Vamos a comprobar que sea integrable:

Sea $P = \{ a_{0}, a_{1}, \dots, a_{n} \} \subset [a,b]$
En cada subintervalo $[a_{i}, a_{i+1}]$
$$
\begin{align}
&ínf(f, [a_{i}, a_{i+1}])=0 \\
&sup(f, [a_{i}, a_{i+1}])=1
\end{align}
$$
El ínfimo de cualquier subintervalo siempre será 0, puesto que entre dos números racionales, siempre puedo encontrar un irracional. Sabiendo esto, el ínfimo de cualquier subintervalo será 0 para la función de Dirichlet. El análogo ocurre para el supremo de cualquier subintervalo.

Este comportamiento ocurre en el intervalo general (oscila infinitamente entre 0 y 1), y también aplica a los subintervalos. Debido a la función particular, el comportamiento de la función no esta dado por el intervalo.

Ahora veremos la suma inferior y superior:
$$
\begin{align}
&S_{*}(f,P) := \sum_{i=0}^{n-1}(a_{i+1} - a_{i}) \times ínf(f, [a_{i}, a_{i+1}]) = \sum_{i=0}^{n-1}(a_{i+1} - a_{i}) \times 0 = 0 \\
&S^{*}(f,P) := \sum_{i=0}^{n-1}(a_{i+1} - a_{i}) \times sup(f, [a_{i}, a_{i+1}]) = \sum_{i=0}^{n-1}(a_{i+1} - a_{i}) \times 1 = \sum_{i=0}^{n-1}(a_{i+1} - a_{i}) = b - a = 1 \\
 \\
&f \text{ no es integrable}
\end{align}
$$
Con esto, podemos concluir que todas las aproximaciones por defecto (suma inferior) son iguales a 0, y todas las aproximaciones por exceso (suma superior) son iguales a 1.
Recordemos que la integral inferior es igual al supremo de las aproximaciones por defecto, que como todas equivalen a 0, entonces es 0. Ídem para la integral superior.
Sabemos que el área estaría entre 0 y 1, aunque no tenemos su valor puntual.

En definitiva, es imposible calcular el área de las funciones que no son integrables con este método, aunque el conjunto este bien definido.

Esto trajo un montón de problemas para la teoría de integración, que posteriormente fueron solucionados por la teoría de integración de Lebesgue (1905), dando una definición más precisa, una versión de la teoría que permite integrar más funciones. Igualmente, incluso con esta teoría hay contraejemplos.
Sin embargo, no la abordaremos en la carrera.

Como este contraejemplo, hay muchos más.

Ahora vamos a definir criterios para saber si una función es integrable o no, y en caso de serlo, poder calcular la integral.

# Criterios de integración
Tenemos una definición de integral y necesitamos herramientas para operar.

## Observación
Para toda partición P
$$
\begin{align}
&S_{*}(f, P) \leq I_{*}(f) \leq I^{*}(f) \leq S^{*}(f, P) \\
&0 \leq I^{*}(f) - I_{*}(f) \leq S^{*}(f, P) - S_{*}(f, P)
\end{align}
$$
Podemos deducir que la distancia entre la integral inferior e integral superior es menor que la distancia entra la suma inferior y suma superior.
Esto se cumple siempre que tengo cuatro números en el orden $A \leq B \leq C \leq D$. Queda más claro si los números se representan sobre una recta.
$$
\begin{align}
&a \leq b \leq c \leq d \\
&c \leq d \\
&-b \leq -a \\
&\implies c - b \leq d - a
\end{align}
$$
Este truco lo vamos a utilizar regularmente.

Más generalmente: Si $P \subset Q$
$$
0 \leq I^{*}(f) - I_{*}(f) \leq S^{*}(f,Q) - S_{*}(f,Q) \leq S^{*}(f,P) - S_{*}(f,P)
$$
Para los dos conjuntos, puedo construir tres diferencias:
- La diferencia de las integrales superior e inferior.
- La diferencia entre la suma superior e inferior de Q.
- La diferencia entre la suma superior e inferior de P.
La diferencia entre la suma superior e inferior de Q es menor que la diferencia entre la suma superior e inferior de P, puesto que Q es más fino, por lo que se trata de una aproximación mejor.

A medida que trabajamos con particiones más finas, llegamos a una diferencia menor, hasta, idealmente, la integral superior e inferior (que pueden no ser iguales).

Es más sencillo de visualizar si lo representamos gráficamente. Sin embargo, con los dibujos no se puede razonar, pero si con las desigualdades desarrolladas a partir de los mismos.
Cada vez que escribimos algo en matemática, casi siempre hay un dibujo o una representación más sencilla que nos facilita el razonamiento.

Este es un fenómeno muy general y utilizaremos muchas veces dicha desigualdad. La utilizaremos de modo implícito

A continuación, vamos a introducir dos criterios que nos van a permitir decidir si una función es integrable o no.

## Proposición - Criterio de integración a menos de $\epsilon$
Ya vimos que hay un montón de teoremas a menos de $\epsilon$:
- Demostrar igualdades a menos de $\epsilon$.
- Demostrar desigualdades a menos de $\epsilon$.
- Aproximar un supremo o un ínfimo a menos de $\epsilon$.

Dados una función acotada $f: [a,b] \to \mathbb{R}$ y un número $I \in \mathbb{R}$, las siguientes dos condiciones son equivalentes:
1. La función f es integrable y tiene integral $\int_{a}^{b}f = I$
2. Para todo $\epsilon > 0$, existe una partición $P \subset [a,b]$ tal que $I - \epsilon < S_{*}(f,P) \leq S^{*}(f,P) < I + \epsilon$

Es decir, para cada $\epsilon$, yo puedo hallar una partición tal que las dos aproximaciones por defecto y por exceso vinculadas a la partición son tan cercanas que la distancia está entre $-\epsilon$ y $+\epsilon$ con respecto al número $I$.
Si esta condición se cumple para todo $\epsilon$, entonces la función es integrable y conocemos el valor de su integral.
Ambos puntos se vinculas mediante un si y solo si (1 implica 2 y 2 implica 1).

En la práctica, cuando queramos demostrar que una función es integrable, muchas veces usaremos el criterio anterior. Sin embargo, el criterio anterior solo tiene sentido si ya tenemos una idea del valor de la integral.

Después veremos otro criterio que corresponde al caso cuando no tenemos ni idea del valor de la integral.

Anteriormente utilizamos desigualdades estrictas, aunque podríamos utilizar desigualdades amplias, pues la idea es la misma y no va a cambiar el razonamiento.

Ahora, demostraremos que 1 implica a 2 y 2 implica a 1.

### Demostración
$(1) \implies (2)$
Supongamos: $I_{*}(f)=I^{*}(f)=I$ (es lo que dice la condición 1)
Sea $\epsilon > 0$.
- Como $I = I_{*}(f) = sup \{ S_{*}(f,P) : P \subset [a,b] \}$ existe una partición $P_{1}$ tal que $S_{*}(f,P_{1}) > I - \epsilon$
Normalmente sabemos que $S_{*}(f,P) < I$ (porque es menor que el supremo), pero sabemos que podemos restarle un pequeño valor a $I$, tal que $S_{*}(f,P) > I - \epsilon$.

- Como $I = I^{*}(f) = ínf \{ S^{*}(f,P) : P \subset [a,b] \}$ existe una partición $P_{2}$ tal que $S^{*}(f,P_{2}) < I + \epsilon$
$I$ es a la vez un supremo y un ínfimo, pudiendo aplicar el acercamiento a menos de $\epsilon$ dos veces, como supremo y como ínfimo, obteniendo dos particiones distintas al final.

Al haber obtenido dos particiones, podemos tomar la unión de ambas.

Sea $P:= P_{1} \cup P_{2}$. Tenemos que:
$$
I - \epsilon < S_{*}(f,P_{1}) \leq S_{*}(f,P) \leq S^{*}(f,P) \leq S^{*}(f,P_{2}) < I + \epsilon
$$
Como $P$ es más fina que $P_{1}$, entonces la suma inferior de $P$ es más grande que la suma inferior de $P_{1}$. Con esa misma lógica, la suma superior de $P$ es más pequeña que la suma superior de $P_{2}$.

Ahora, podemos ignorar la suma inferior de $P_{1}$ y la suma superior de $P_{2}$ (ingredientes temporales para obtener la expresión), y nos queda exactamente lo que estábamos buscando: la proposición (2).
$$
\begin{align}
&I - \epsilon < \cancel{ S_{*}(f,P_{1}) } \leq S_{*}(f,P) \leq S^{*}(f,P) \leq \cancel{ S^{*}(f,P_{2}) } < I + \epsilon \\
&I - \epsilon < S_{*}(f,P) \leq S^{*}(f,P) < I + \epsilon
\end{align}
$$
Demostramos que $(1) \implies (2)$. Ahora, proseguimos a demostrar que $(2) \implies (1)$

$(2) \implies (1)$ Supongamos $(2)$
Si yo tengo la expresión $I - \epsilon < S_{*}(f,P) \leq S^{*}(f,P) < I + \epsilon$, esto significa que yo puedo agregar la integral inferior y superior entre las sumas inferiores y superiores y la desigualdad aún se mantiene.
$$
I - \epsilon < S_{*}(f,P) \leq I_{*}(f) \leq I^{*}(f) \leq S^{*}(f,P) < I + \epsilon
$$
De esta forma, puedo remover las sumas inferiores y superiores, dejando solo las integrales inferiores y superiores.

Esto implica que
$$
I - \epsilon < I_{*}(f) \leq I^{*}(f) < I + \epsilon \qquad (\forall \epsilon > 0)
$$
Esta es una desigualdad a menos de $\epsilon$, si comparamos $I - \epsilon$, $I_{*}(f)$ y $I^{*}(f)$, podemos ver que los tres números son iguales. La idea es que la desigualdad anterior nos llega al siguiente razonamiento: decir que $I_{*}(f)$ está entre $I - \epsilon$ e $I + \epsilon$, es lo mismo que decir que la distancia en valor absoluto es menor que $\epsilon$. De esta forma, tomando como referencia $I - \epsilon < I_{*}(f)$
$$
\implies |I_{*}(f) - I| < \epsilon \qquad (\forall \epsilon > 0)
$$
Ahora, tomando en cuenta $I - \epsilon < I^{*}(f)$, podemos agregar
$$
|I^{*}(f) - I| < \epsilon \qquad (\forall \epsilon > 0)
$$
Luego:
$$
I_{*}(f) = I^{*}(f) = I
$$
Esto funciona porque cuando establecemos que $|I^{*}(f) - I| < \epsilon \qquad (\forall \epsilon > 0)$, lo único que puede ser verdad es que $I^{*}(f) = I$, puesto que si su diferencia es menor que $\epsilon$, y $\epsilon$ es cualquier número positivo, si o si tienen que ser iguales.

Esto termina la demostración del primer criterio, el cual establece que si yo quiero demostrar que una función es integrable y que su integrable vale $I$, lo que tenemos que hacer es, para cada $\epsilon$ tengo que construir una partición que cumple $I - \epsilon < S_{*}(f,P) \leq S^{*}(f,P) < I + \epsilon$, y esto reduce el problema de integración a un problema de sumas inferiores y superiores que ya sabemos calcular.

Sin embargo, el problema de este criterio es que para usarlo ya hay que adivinar el valor de la integral (pues establece que "tiene integral $\int_{a}^{b}f = I$"), entonces solo nos sirve si tenemos un método para calcular el valor de la integral.

Aquí vimos como saber determinar si dos números son iguales sin realizar ninguna operación, simplemente por pura lógica y desarrollo (aplicación de propiedades y razonamiento matemático).

Ahora veremos el segundo criterio, pero importante aclarar lo siguiente:
1. El primer criterio es para la gente que ya tiene idea del valor de la integral.
2. El primer criterio es para la gente que no tiene idea del valor de la integral.
Veremos que en la práctica los dos criterios sirven.

## Proposición - Criterio de integrabilidad a menos de $\epsilon$
Aclaración:
- Integración = Dar el valor de la integral.
- Integrabilidad = Decir que la función es integrable sin conocer su valor.
Al contrario del criterio anterior, aquí no me doy ningún numero I.

Dad una función acotada $f: [a,b] \to \mathbb{R}$, las siguientes 2 condiciones son equivalentes:
1. La función f es integrable en $[a,b]$ (lo que queremos obtener)
2. Para todo $\epsilon > 0$, existe $P\subset [a,b]$ tal que
$$
(0 \leq) S^{*}(f,P) - S_{*}(f,P) < \epsilon 
$$
Agregamos el 0 previo a la desigualdad importante para aclarar que la diferencia siempre es positiva o nula.
Aquí estamos estableciendo que para todo $\epsilon$ existe una partición que me da dos aproximaciones con una distancia menor que $\epsilon$, y si es el caso, la función es integrable y recíprocamente. Es de integrabilidad ya que determinamos que es integrable sin obtener el valor de la integral, y esto nos sirve o no dependiendo de que estemos buscando.

Ahora demostraremos que $(1) \implies (2)$
Supongamos que $I_{*}(f) = I^{*}(f)$ (f es integrable).
Se escribe $I:= I_{*}(f) = I^{*}(f)$ (cuando son iguales simplifico la notación).
Sea $\epsilon > 0$.

Queremos demostrar para todo $\epsilon$. Ahora que introdujimos un nombre para la integral, podemos usar el criterio anterior.

Por el criterio anterior, existe $P \subset [a,b]$ tal que
$$
I - \frac{\epsilon}{2} < S_{*}(f,P) \leq S^{*}(f,P) < I + \frac{\epsilon}{2}
$$
Esto lo sabemos por el criterio anterior. Ahora queda analizar las distancias entre estos números.
$$
\begin{align}
&0 \leq S^{*}(f,P) - S_{*}(f,P) < \left( I + \frac{\epsilon}{2} \right) - \left( I - \frac{\epsilon}{2} \right) \\
&0 \leq S^{*}(f,P) - S_{*}(f,P) < \epsilon
\end{align}
$$
De esta forma, obtuvimos lo que habíamos establecido anteriormente em la segunda condición del criterio de integrabilidad a menos de $\epsilon$.

El recíproco es más sencillo, ya que sabemos que $S^{*}(f,P) - S_{*}(f,P)$ siempre es mayor que $I^{*}(f) - I_{*}(f)$, que es el caso ideal. Por esta razón, podemos intercalar la diferencia de las integrales, de modo que: $0 \leq I^{*}(f) - I_{*}(f) \leq S^{*}(f,P) - S_{*}(f,P) < \epsilon$

$(2) \implies (1)$
Supongamos $(2)$
Esto implica que
$$
0 \leq I^{*}(f) - I_{*}(f) < \epsilon \qquad (\forall \epsilon > 0)
$$
Si tengo esta desigualdad para todo $\epsilon$, esto demuestra que ambos números son iguales.

Luego $I^{*}(f) = I_{*}(f)$
Finalmente, teniendo esta igualdad, podemos asegurar que la función f es integrable.
Aquí finaliza la demostración del segundo criterio.

La próxima clase, veremos una aplicación fundamental del segundo criterio, demostrando que todas las funciones monótonas son integrables.