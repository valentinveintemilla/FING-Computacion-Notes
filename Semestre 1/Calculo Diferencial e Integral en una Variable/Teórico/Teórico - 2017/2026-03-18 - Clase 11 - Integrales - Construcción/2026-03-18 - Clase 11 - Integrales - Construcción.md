En esta instancia, continuaremos con el capítulo de Integrales.
La clase pasada revisamos los conceptos de área geométrica y área algebraica, así como partición de un intervalo.

# Partición de un intervalo
**Definición**: Una partición de $[a,b]$ es un conjunto finito $P \subset [a,b]$ tal que $a \in P$ y $b \in P$

<u>Notación</u>:
$$
P={a_{0},a_{1},\dots,a_{n}} \text{ con } a = a_{0} < a_{1} < \dots < a_{n} = b
$$
También vimos que había un orden parcial sobre las particiones: $P \subset Q$
De esta forma, podemos decir que Q es más fina que P y P es más gruesa que Q (P tiene menos intervalos que Q).

Siempre que comparamos particiones, son particiones de un mismo intervalo. Se toma un intervalo fijado y comparamos las particiones dentro del mismo.

- Existe una particion más gruesa: $P_{0}={a,b}$.
Esta es la menos interesante para construir aproximaciones, ya que a medida que vamos afinando (aumentamos la cantidad de particiones), nos acercamos al área algebraica real.
Es importante aclarar que no existe una partición más fina que las otras (una que sea más fina para cualquier intervalo).

Sin embargo, puedo tomar dos particiones de un mismo intervalo, y su unión será más fina que las particiones individuales.
- Dadas $P,Q \subset [a,b]$ particiones, la partición $P \cup Q$ es más fina que P y Q a la vez (el refinamiento común).

Con esto, recordamos lo que vimos sobre las particiones. En definitiva, son útiles para cortar un intervalo $[a,b]$ en n partes, dándonos n intervalos, en los que haremos nuestras aproximaciones.

# Sumas inferiores y superiores
Sea $f:[a,b] \to \mathbb{R}$ una función acotada:
$$
\exists k_{*}m k^{*} \text{ tales que } k_{*} \leq f(x) \leq k^{*} \forall x \in [a,b]
$$
Mi objetivo es capturar el área algebraica en la región entre el eje x y la curva, siendo medir rectángulos la única cosa que sabemos hacer.
La idea es muy sencilla:
- Fijar una partición (dividir el intervalo en varios trozos).
- Estudiar lo que pasa en cada trozo. Para esto tomamos en cuenta el ínfimo local y el supremo local, de modo que el área que me interesa está entre el área del rectángulo formado con el supremo y el área del rectángulo formado con el ínfimo (se definen naturalmente dos áreas).

<u>Notaciones</u>: Si $[a',b'] \text{ (cualquier subintervalo de } [a,b]) \subset [a,b]$
$$
\begin{align}
&ínf(f,[a',b']) = ínf \{ f(x): x \in [a',b'] \} \text{ (ínfimo local)} \\
&sup(f,[a',b']) = sup \{ f(x): x \in [a',b'] \} \text{ (supremo local)}
\end{align}
$$![[Sumas inferiores y superiores.png]]
La idea es calcular el área realizando dos tipos de aproximaciones: por exceso y por defecto.

Aclaración importante: Cuando hablamos de Teorema, Proposición, Corolario o Lema, me estoy refiriendo a lo mismo, realmente no hay diferencia. Cada vez que utilizamos dichas palabras, estoy enunciando un resultado matemático que voy a demostrar, y en función al valor que atribuyo al resultado obtenido.
- La palabra más neutra es Proposición, pues solo establece que es un resultado.
- Cuando el resultado es muy importante (subjetivamente hablando), lo llamamos Teorema. Igualmente depende del autor. Quizás uno llame Teorema a algo que otros llamarían Proposición.
- Lema se utiliza para resultados que no son tan importantes, pero van a servir para demostrar un resultado más importante a posterior.
- El Corolario es el opuesto, consecuencia de un resultado importante. Entonces, en general el orden es: Lema - Teorema - Corolario
Igualmente, en función de los libros, las palabras se intercambian, así que no es algo importante.

## Lema
Si $[a_{2},b_{2}] \subset [a_{1},b_{1}] \subset [a,b]$
Yo tengo tres intervalos, uno dentro de otro, y queremos ver como ordenar el ínfimo y supremo de cada uno.

Entonces:
$$
\begin{align}
&ínf(f, [a_{2},b_{2}]) \geq ínf(f, [a_{1},b_{1}]) \\
&sup(f, [a_{2},b_{2}]) \leq sup(f, [a_{1},b_{1}])
\end{align}
$$
Los ínfimos van en el orden, de mayor a menor, de "más adentro a más afuera".
Los supremos van en el orden contrario (de mayor a menor, de "más afuera a más adentro").

Este resultado ya lo vimos con el conjunto de las imágenes de una función:
$$
\begin{align}
&A_{1}={f(x): x \in [a_{1},b_{1}]} \\
&A_{2}={f(x): x \in [a_{2},b_{2}]} \\ \\
&\text{Sabemos que el intervalo } [a_{2},b_{2}] \text{ se encuentra incluido en } [a_{1},b_{1}] \\
&\text{Por lo tanto, sucede lo mismo con las imágenes: } A_{2} \subset A_{1} \\ \\

&\text{Podemos tomar las siguientes conclusiones sobre los ínfimos y supremos:} \\
&ínf(A_{1}) \leq ínf(A_{2}) \leq sup(A_{2}) \leq sup(A_{1})
\end{align}
$$
En este caso, representar gráficamente las imágenes de los intervalos es de gran ayuda.

Ahora, tenemos que definir las sumas inferiores y superiores.

# Sumas inferiores y superiores
**Definición**
Sea $P = \{a_{0},a_{1},\dots,a_{n} \} \subset [a,c]$
Se definen dos números
$$
\begin{align}
&S_{*}(f,P) := \sum_{i=0}^{n-1}(a_{i+1} - a_{i}) \times ínf(f, [a_{i}, a_{i+1}]) \text{ (Aproximación por defecto del área algebraica)} \\
&S^{*}(f,P) := \sum_{i=0}^{n-1}(a_{i+1} - a_{i}) \times sup(f, [a_{i}, a_{i+1}]) \text{ (Aproximación por exceso del área algebraica)} \\ \\

&(a_{i+1} - a_{i}) \times ínf(f, [a_{i}, a_{i+1}]) = \text{Área algebraica del rectángulo inferior} \\
&(a_{i+1} - a_{i}) \times sup(f, [a_{i}, a_{i+1}]) = \text{Área algebraica del rectángulo superior}
\end{align}
$$
Funciona bien por razones de signo, incluso en la parte negativa.

Al final nosotros queremos medir el área algebraica de la función. Sin embargo, nunca la definimos, puesto que no sabemos. No existe una definición clara de la misma, simplemente trabajamos con aproximaciones (lo único que sabemos hacer).
De esta forma, hay que trabajar con la suma superior e inferior, y sus propiedades correspondientes.

Por ejemplo, sabemos que $S_{*}(f,P) \leq S^{*}(f,P)$ en todos los casos (por definición de ínfimo y supremo).
- El ínfimo siempre es menor o igual al supremo, y es lo único que diferencia a ambas formulas.
- La "base del rectángulo" (calculada como $(a_{i+1} - a_{i})$) siempre será positiva, puesto que al ser un intervalo de números $[a,b]$, $a_{i+1} > a_{i}$.
- Para todos los intervalos, sumo el área local resultante, y de esa forma obtengo la suma inferior y/o superior.

## Proposición
$$
S_{*}(f,P) \leq S^{*}(f,P)
$$
Esto tampoco nos dice mucho, pues es bastante obvio. Sin embargo, es algo que se debe demostrar y asegura la consistencia de la definición.

## Proposición
$$
\begin{align}
&\text{Si } P,Q \subset [a,b] \text{ son tales que } P \subset Q: \\
&S_{*}(f,P) \leq S_{*}(f,Q) \leq S^{*}(f,Q) \leq S^{*}(f,P)
\end{align}
$$
¿Qué significa lo anterior?
Significa que cuando yo reemplazo una partición por otra más fina, obtengo un par de aproximaciones mejores. Siempre se mejora la aproximación si yo reemplazo mi aproximación por otra más fina.
- Mejorar una aproximación por defecto es subir.
- Mejorar una aproximación por exceso es bajar.

Hay que demostrar que esto funciona para cualquier par de particiones P y Q, si $P \subset Q$.
Tenemos una desigualdad que es obvia ($S_{*}(f,Q) \leq S^{*}(f,Q)$), entonces tenemos que demostrar las dos siguientes:
- $S_{*}(f,P) \leq S_{*}(f,Q)$ (con ínfimos)
- $S^{*}(f,Q) \leq S^{*}(f,P)$ (con supremos)
Las demostraciones son análogas, aunque no triviales (son algo complejas).

### Demostración
Como es una demostración algo complicada, la haremos en dos partes.
Primer caso: solo hay un punto de diferencia entre ambas particiones.

$$
\begin{align}
&\text{En primer lugar, se considera el caso particular donde } Q=P \cup {a'} con a' \not \in P \qquad (\#(Q-P)=1) \\
&\text{Se pueden escribir:} \\
&P=\{ a_{0},\dots,a_{k},a_{k+1},\dots,a_{n} \} \\
&Q=\{ a_{0},\dots,a_{k},a',a_{k+1},\dots,a_{n} \} \\
&\text{Como se puede ver, consideramos que la inserción de un nuevo punto, en este caso a', va a caer entre dos puntos que ya existen }
\end{align}
$$
Ahora, calcularemos la suma inferior de ambas particiones y las compararemos:
$$
\begin{align}
&S_{*}(f,P) = \sum_{i=0}^{n-1}(a_{i+1} - a_{i}) \times ínf(f, [a_{i}, a_{i+1}]) \\ \\

&\text{Esta suma tiene n sumandos, considerando todos los n subintervalos. Vamos a extraer los indices referentes al subintervalo } [a_{k},a_{k+1}] \\ \\

&S_{*}(f,P) = S_{i < k} + (a_{k+1} - a_{k}) \times ínf(f, [a_{k}, a_{k+1}]) + S_{i > k} \\ \\

&\text{Descompusimos la suma en el término que nos interesa, y agrupamos todo lo anterior y todo lo que sigue, pues se supone que no va a cambiar para } Q \\
&\text{A continuación desarrollamos la operación:} \\

&S_{*}(f,P) = S_{i < k} + ((a' - a_{k}) + (a_{k+1} - a')) \times ínf(f, [a_{k}, a_{k+1}]) + S_{i > k} \\ \\

&\text{Aquí no cambié nada con respecto a la operación anterior, simplemente descompuse } a_{k+1} - a_{k} \text{ en } (a' - a_{k}) + (a_{k+1} - a') \text{, puesto que, como podemos ver, al estar restando de un lado y sumando del otro, los } a' \text{ se anulan.} \\
&\text{Otra forma de verlo es que antes teníamos el ancho algebráico del intervalo } [a_{k},a_{k+1}] \text{, y ahora tenemos la suma de los anchos algebráicos de } [a_{k},a'] \text{ y } [a',a_{k+1}] \text{, que son equivalentes.} \\ \\

&=S_{i < k} + (a' - a_{k}) \times ínf(f, [a_{k}, a_{k+1}]) + (a_{k+1} - a') \times ínf(f, [a_{k}, a_{k+1}]) + S_{i > k} \\ \\

&\text{Aquí estamos teniendo un pequeño "error", donde estamos multiplicando el ancho de cada mitad de intervalo por el ínfimo del intervalo total, cuando deveríamos multiplicar cada mitad de intervalo con su respectivo ínfimo del intervalo correspondiente. Es importante considerar que ahora el resultado será mayor, puesto que al aproximar más la suma inferior, su valor aumenta. De esta forma:} \\ \\

&\leq S_{i < k} + (a' - a_{k}) \times ínf(f, [a_{k}, a']) + (a_{k+1} - a') \times ínf(f, [a', a_{k+1}]) + S_{i > k} \\ \\

&\text{Si analizamos cuidadosamente el resultado obtenido, nos damos cuenta que equivale a la suma inferior de la partición Q.} \\ \\

&= S_{*}(f,Q) \\ \\
 
&\text{De esta forma, demostramos que } S_{*}(f,P) \leq S_{*}(f,Q)
\end{align}
$$
Aquí demostramos un caso particular. Ahora necesito hacer el caso general. Sabemos que funciona cuando agregamos un punto (sube la aproximación inferior), entonces podemos seguir agregando puntos, y por inducción seguiremos aumentando la suma inferior.

### <u>Caso general</u>:
$Q = P \cup \{ a',\dots,a'_{p} \}$ (sabemos que funciona con un punto, ahora lo haremos con p puntos).
$$
S_{*}(f,P) \leq S_{*}(f,P\cup \{ a'_{1} \}) \leq S^{*}(f,P\cup \{ a'_{1}, a'_{2} \}) \leq \dots \leq S^{*}(f,Q)
$$
Con la demostración anterior, sabemos que esta proposición es verdadera. Ahora, nos quedaría demostrar el caso $S^{*}(f,Q) \leq S^{*}(f,P)$ para demostrar que el siguiente enunciado es verdadero:
$$
\begin{align}
&\text{Si } P,Q \subset [a,b] \text{ son tales que } P \subset Q: \\
&S_{*}(f,P) \leq S_{*}(f,Q) \leq S^{*}(f,Q) \leq S^{*}(f,P)
\end{align}
$$
Esta es la confirmación formal de que, cuando reemplazamos una partición por otra más fina, obtenemos un par de aproximaciones mejores (suma inferior más grande y suma superior más pequeña).

## Proposición
A partir del enunciado, también podemos destacar la siguiente proposición:
$$
S_{*}(f,P) \leq S^{*}(f,Q) \qquad (\forall P,Q \subset [a,b])
$$
Antes, definimos que la suma inferior de una partición siempre es menor o igual a la suma superior de la misma partición.
Sin embargo, ahora podemos establecer que todas las aproximaciones inferiores son menores o iguales a todas las particiones superiores, siempre y cuando sean de particiones que partan del mismo intervalo.

### Demostración
$$
\begin{align}
&S_{*}(f,P) \leq S_{*}(f,P \cup Q) \leq S^{*}(f,P \cup Q) \leq S^{*}(f,Q) \\
&\text{Las desigualdades fueron establecidas en base a que conjuntos son más finos.}
\end{align}
$$
Como vemos, logramos demostrar la proposición anterior con un simple enunciado, llegando a la conclusión mencionada.
Aquí tenemos la situación ideal: dos conjuntos de aproximaciones, uno a la izquierda y el otro a la derecha. Podemos considerar el supremo de uno y el ínfimo del otro, con la idea de encontrar el área algebraica.

A continuación, podemos definir la noción de integral inferior y superior

# Integral inferior y superior
Tenemos dos conjuntos de aproximaciones:
$$
\begin{align}
&A^{-}(f) = \{ S_{*}(f,P): P \subset [a,b] \} \qquad \text{(Conjunto de todas las aproximaciones por defecto, o sumas inferiores)} \\
&A^{+}(f) = \{ S^{*}(f,P): Q \subset [a,b] \} \qquad \text{(Conjunto de todas las aproximaciones por exceso, o sumas superiores)}
\end{align}
$$
Estos son dos conjuntos numéricos, específicamente dos conjuntos reales. De estos, podemos decir que:
- No son vacíos.
- Todo elemento de $A^{-}(f)$ es menor que todo elemento de $A^{+}(f)$. Formalmente:
$$
A^{-}(f) \ll A^{+}(f) \qquad \text{(Todas las aproximaciones por defecto son menores o iguales a todas las aproximaciones por exceso)}
$$
De esto podemos deducir muchas cosas, por ejemplo:
- $A^{-}(f)$ tiene supremo
- $A^{+}(f)$ tiene ínfimo
- $sup(A^{-}(f)) \leq ínf(A^{+}(f))$
Todo esto define la integral inferior y la integral superior.

La integral inferior es el supremo del conjunto de todas las aproximaciones por defecto, una idealización de la aproximación por defecto.
La integral superior es el ínfimo del conjunto de todas las aproximaciones por exceso, una idealización de la aproximación por exceso.

A continuación, la definición formal:

**Definición**:
Integral inferior: $I_{*}f = sup(A^{-}(f)) = sup_{P \subset [a,b]S_{*}(f,P)}$
Integral superior: $I^{*}f = ínf(A^{+}(f)) = ínf_{P \subset [a,b]S^{*}(f,P)}$

Por construcción, también podemos establecer que $I_{*}f \leq I^{*}f$.

## Proposición
$$
I_{*}f \leq I^{*}f
$$
Esto funciona para cualquier función acotada, es lo único que supusimos de la función.
Aquí terminamos nuestro intento por intentar aproximarnos al área algebraica de una función, pues $I_{*}f$ es la mejor aproximación por defecto y $I^{*}f$ es la mejor aproximación por exceso.
Quizás tengamos suerte y ambos valores sean iguales, capturamos el área algebraica. En caso de ser distinto, no habremos encontrado el área en si, sino que nos quedamos con un rango en el que sabemos que está.

**Definición**:
Una función $f:[a,b] \to \mathbb{R}$ <u>acotada</u> es integrable si $I_{*}f = I^{*}f$.
Cuando es el caso, este número se escribe
$$
\int_{a}^{b}f \qquad \text{o} \qquad \int_{a}^{b}f(x) dx
$$
El símbolo utilizado es una 'S' antigua.
Esta notación se utiliza en el caso de éxito, cuando conseguimos capturar el área algebraica.

La idea es que cuando la función es bastante regular, se puede capturar el área. Pero, cuando es demasiado irregular, no se puede. Solo veremos un contraejemplo para mostrar que existe al menos un fracaso y destruir la teoría de Riemann.

La segunda notación tiene un producto ($f(x) dx$), puesto que cuando Leibniz definió la teoría, no tenía ninguna de las propiedades con las que contamos nosotros (completitud, supremo, ínfimo, etc.). Por esta razón, era un punto de vista flojo.
El pensó algo similar a lo siguiente:
$$
\int_{a}^{b}f(x) dx = \sum_{x \in [a,b]}f(x) dx
$$
El considero que se podía dividir el intervalo $[a,b]$ en subintervalos ultra finos, de forma que la base era dx (infinitamente fino) y la altura f(x). Se trata de una suma infinita, pues implica a todos los elementos del intervalo $[a,b]$.
Igualmente, consiguió calcularla con está definición, y seguimos utilizándola hasta hoy en día, pues es más intuitiva.
Aclaración: Para Leibniz, dx son números muy cercanos a 0, entre los positivos y cero (0 < dx < positivos).

Aunque parezca que no tenga sentido, se ha demostrado que es posible darle un sentido a tales objetos, pero en otros cuerpos, aunque se necesita un arduo trabajo, lo que explica que su razonamiento era correcto.

Algo importante a considerar: no se puede desplegar la definición cada vez que vamos a calcular una integral. En su lugar, vamos a demostrar una sucesión de propiedades para olvidar la definición y evitar utilizarla directamente.

## Proposición
Sean $f,g: [a,b] \to \mathbb{R}$ integrables (damos por hecho que son acotadas)
Si $f(x) \leq g(x) \qquad \forall x \in [a,b]$
Entonces:
$$
\int_{a}^{b}f \leq \int_{a}^{b}g
$$
### Demostración
Si $P=\{ a_{0},a_{1},\dots,a_{n} \}$
$$
\begin{align} \\
&\text{Para la suma inferior:} \\
&S_{*}(f,P) = \sum_{i=0}^{n-1}(a_{i+1}-a_{i}) \times ínf(f, [a_{i}, a_{i+1}]) \\
&S_{*}(f,P) \leq \sum_{i=0}^{n-1}(a_{i+1}-a_{i}) \times ínf(g, [a_{i}, a_{i+1}]) = S_{*}(g,P) \\ \\

&S_{*}(f,P) \leq S_{*}(g,P) \leq I_{*}(g) \text{ (idealización de todas las aproximaciones por defecto, la más grande)} \\
&\implies I_{*}(g) \text{ es cota superior de } \{ S_{*}(f,P): P \subset [a,b] \} \\ 
&I_{*}(g) \text{ es mayor que el supremo de } \{ S_{*}(f,P): P \subset [a,b] \} = I_{*}(f) \\ \\


&\implies I_{*}(f) \leq I_{*}g
\end{align}
$$
Este es un ejemplo de todo el razonamiento que hay que desplegar para demostrar cualquier igualdad. La idea es demostrar propiedades, para quedarnos únicamente con los métodos más eficientes.

En la próxima clase, veremos ejemplos y contraejemplos.