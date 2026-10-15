Comenzamos viendo un complemento sobre los números reales
# Números reales
Sean $A,B \neq \emptyset \subset \mathbb{R}$ tales que
$\forall x \in A, \forall y \in B, x \leq y$ (De esta forma no se cruzan)
Se puede escribir $A\ll B$ (Todos los puntos de A están a la izquierda de todos los puntos de B)

<u>Entonces</u>:
A tiene supremo
B tiene ínfimo, y
$sup(A) \leq ínf(B)$

Para proseguir, tenemos que demostrar que A tiene supremo. Para esto, tenemos que demostrar que A tiene cota superior. Para esto, podemos tomar cualquier elemento de B (además, sabemos que son no vacíos).
$$
\text{Dado } y_{0} \in B \text{ (cualquiera)}, y_{0} \text{ es cota superior de A.}
$$
Esto demuestra la existencia de supremo (pues si tiene cota superior, también tiene supremo).
De modo análogo se demuestra la existencia de ínfimo para B.
$$
\text{Dado } x_{0} \in A \text{ (cualquiera)}, x_{0} \text{ es cota inferior de B.}
$$
Por último, me queda demostrar que el primer número es menor o igual al segundo número.
Aquí aplicamos un razonamiento de doble paso al límite.
$$
\begin{align}
&\text{Dado } x \in A: \\
&x\leq y (\forall y \in B) \\
&\implies x \text{ es cota inferior de } B \\
&\implies x \leq ínf(B) (\forall x \in A)\text{ (el ínfimo de B es la cota inferior más grande)} \\
&\implies ínf(B) \text{ es cota superior de A.} \\
&\implies sup(A) \leq ínf(B)
\end{align}
$$
Es fundamental entender cada uno de los pasos en este tipo de razonamientos, ya que se utilizan todo el tiempo en matemática.

A continuación, hablaremos de los intervalos encajados:
## Intervalos cerrados encajados
$$
\begin{align}
&[a_{n}, b_{n}]_{n\in \mathbb{N}} \qquad (a_{n} \leq b_{n}) \\
&\text{tales que } [a_{n+1}, b_{n+1}]\subset [a_{n}, b_{n}] \\
&a_{n} \leq a_{n+1} \leq b_{n+1} \leq b_{n} \\
\end{align}
$$
Como vemos, se trata de una sucesión de intervalos, de tal forma que cada intervalo que sigue está contenido en el intervalo anterior.
Lo interesante es que ahora tenemos dos conjuntos de aproximaciones. La idea es capturar la intersección. Para esto, vamos a definir dos conjuntos, siendo uno para todos los $a_{n}$ y otro para todos los $b_{n}$.
$$
\begin{align}
&Sea \\
&A={a_{n}: n \in \mathbb{N}} \\
&B={b_{m}: m \in \mathbb{N}}
\end{align}
$$
Queremos demostrar que estos conjuntos cumplen la propiedad $a_{n} \leq b_{n}$, de modo que $\forall a \in A, \forall b \in B, a \leq b$.
Sabemos que se cumple para elementos a, b de mismo índice (como lo establecimos previamente), pero tenemos que probarlo para todos los elementos.

Lo primero que tenemos que destacar es que la sucesión $a_{n}$ es creciente, mientras que la sucesión $b_{n}$ es decreciente.

$$
\begin{align}
&\text{Por inducción: } \\
&n \leq m \implies a_{n} \leq a_{m} \\
&\implies b_{n} \geq b_{m} \\
&\longrightarrow \text{por inducción sobre } m - n
\end{align}
$$
$$
\begin{align}
&\forall n,m \in \mathbb{N} \\
&a_{n} \leq a_{máx(n,m)} \leq b_{máx(n,m)} \leq b_{m}
\end{align}
$$
Si tomo dos índices n y m, tengo que $a_{n} \leq a_{máx(n,m)}$, puesto que cuanto mayor sea el índice de a, mayor será el valor (más a la derecha estará en la recta).
Nuestro objetivo es comparar $a_{n}$ y $b_{m}$, y el truco está en pasar por $a_{máx(n,m)}$, que es mayor o igual a $a_{n}$. Tomamos como referencia la desigualdad anterior ($n \leq m$), y reemplazamos m por el máximo entre n y m.
La desigualdad establecida anteriormente funciona, ya que sabemos que para un mismo índice, $b\geq a$, puesto que los intervalos tienen como límite superior a b. De esta forma, para el índice $máx(n,m), a\leq b$. Además, como sabemos que m es mayor que n, $máx(n,m) \leq m \implies b_{máx(n,m)} \leq b_{m}$.

Conclusión: $A \ll B$
Después de definir el supremo de A, el ínfimo de B, sabemos que el supremo de A será menor o igual al ínfimo de B.

$$
\begin{align}
&\implies sup(A) \leq ínf(B) \\
&[sup(A), ínf(B)] \subset [a_{n}, b_{n}] \qquad (\forall n \in \mathbb{N})
\end{align}
$$
De esta manera, demostramos que la intersección es vacía. Contiene al menos a $sup(A)$, $ínf(B)$ y todos los valores intermedios. En caso de que $sup(A) = ínf(B)$, entonces el intervalo se reduce a un punto.
Es fundamental sentirse cómodo con esta forma de razonamiento.

Ahora, podemos comenzar con las integrales:

# Integrales
Solo vamos a hablar de integrales del punto de vista del área, libre del teorema fundamental, puesto que no hemos visto derivadas.

El tema general de la teoría de integración consiste en medir áreas de regiones del plano, o del espacio, definidas a partir de curvas. La idea es tener trucos o métodos para medir el área de regiones particulares. Primero vamos a repasar lo que sabemos del área en general.

<u>Introducción</u>:
Para comenzar, sabemos medir el área de un rectángulo:
$$
\text{Área Rectángulo} = a \times b \text{, siendo a y b el largo y el ancho del mismo}
$$
Los cálculos de área se basan en reducir los problemas de área a problemas de rectángulos. Es fundamental saber que la única cosa que sabemos medir directamente son los rectángulos, pero podemos descomponer cosas con rectángulos.

Vamos a ver una figura más compleja: un paralelogramo.
Podemos cortar en trozos para reducir el problema a un rectángulo.
Lo mismo para un triángulo.
![[Figuras simplificadas a rectángulos.png]]
Si entendemos la idea de área, que es un concepto invariante por transformación, isometría del plano, con la posibilidad de cortar figuras y moverlas, siempre se puede transformar en rectángulos.

Ahora, ¿Qué pasa cuando aparecen curvas y figuras que no son polígonos?
Vamos a tomar a el círculo como ejemplo.
En el pasado, surgió la idea de aproximar por polígonos. Por ejemplo, si utilizamos dos hexágonos, uno fuera y otro dentro del círculo, sabemos que el área del círculo estará entre el área del hexágono interno y el área del hexágono externo. La aproximación mejora a medida que se aumentan la cantidad de lados.
![[Cálculo aproximado del área de un círculo.png]]

Afortunadamente, los supremos y los ínfimos serán muy útiles para el cálculo de áreas. Por ejemplo, vamos a considerar un conjunto de aproximaciones inferiores, que serán aproximaciones por defecto pero más y más precisas, y un conjunto de aproximaciones por exceso pero más y más precisas, y al final tendremos dos conjuntos de aproximaciones, unas por defecto y otras por exceso. Tomando el supremo de las aproximaciones inferiores y el ínfimo de las aproximaciones superiores, obtendremos dos números en dicho orden, y, con la suficiente suerte, serán iguales, indicando que esa es el área de la figura.

Esto finaliza la introducción al tema.

Es fundamental entender que, históricamente, la teoría de integración tardó en desarrollarse, puesto que esta íntimamente relacionada con los conceptos de supremo, ínfimo, etc., conceptos surgidos del axioma de completitud. Por ejemplo, a Leibniz se le dificultó el correcto desarrollo de dicha teoría por ausencia de dichas propiedades. Sin embargo, años después, Riemann pudo desarrollar la teoría de integración, la cual permite resolver casi todos los casos posibles.

## Objetivo y método
Queremos definir áreas de regiones del plano definidas a partir de curvas. Para nosotros, una curva es una gráfica de una función.

Entonces, delimitamos una función entre dos puntos a y b, lo que establece una región entre el eje x y la gráfica. El objetivo es medir el área algebraica de la función pintada.

<u>Objetivo</u>: medir el área algebraica de la región entre el eje x y la gráfica de f.
Con área algebraica, nos referimos a que es más sencillo considerar a las regiones superiores al eje x como positivas, y las inferiores como negativas.
![[Gráfica curva.png]]
De esta forma, queremos aprender a, dada una función cualquiera, entre dos puntos a y b fijados, como calcular la región entre f y el eje x. Está claro que el área algebraica no es lo mismo que el área geométrica, pues en el área geométrica consiste en tomar todo como positivo. Igualmente, esto no es un problema, ya que hay un simple truco que consiste en aplicar el valor absoluto a f, haciendo que todo quede positivo.
No es un problema contar las cosas negativas como negativas, pues obtendremos valiosas propiedades algebraicas gracias a esto.

Ahora vamos a entender cuidados que hay que tener sobre la forma de f, puesto que no se puede hacer con cualquier función f. Por ejemplo, corremos el riesgo de que el área sea infinita, por lo que es importante acotar las cosas. Nosotros establecimos dos acotaciones:
- Acotación horizontal
Considerar funciones cuyo dominio sea un intervalo cerrado: $f:[a,b] \to \mathbb{R}$
- Acotación vertical
Se supone que f está acotada: $k_{*} \leq f(x) \leq k^{*}$
De esta manera, la imagen de un valor del dominio no puede pasar determinados límites conocidos.

Todo esto asegura que la figura se queda dentro de un rectángulo, de forma que si tiene área, tiene que ser finita.

Ahora, vamos con el método de Riemann, que parte de que como no se sabe medir directamente tal función, utilizaremos aproximaciones.

La técnica de Riemann consiste en dividir el intervalo $[a,b]$ en trozos. Entonces, para estudiar el área de la figura, puedo estudiar lo que pasa en cada intervalo, y en cada subintervalo, como se que la función está acotada superior e inferiormente, se que tiene ínfimo local y supremo local.
Como vemos, obtenemos rectángulos, pero que a veces están por debajo del eje y. Por esta razón, tenemos que modificar el cálculo de área de rectángulo, de tal forma que el ancho siempre tiene que ser positivo, pero la altura puede ser negativa, obteniendo un área negativa o positiva dependiendo de dicho valor.

![[Técnica de Riemann.png]]

La idea es calcular el área total de la función, en base a los rectángulos trazados en cada subintervalo. Dichos rectángulos pueden ser trazados en base al ínfimo o al supremo de cada subintervalo, siendo la idea que posteriormente se determine que el área de la función se encuentra entre el área calculada en base a los rectángulos trazados por el ínfimo, y el área calculada en base a los rectángulos trazados por el supremo.
Si proseguimos, cada vez trazando intervalos más finos, iremos ajustando el valor cada vez más (obteniendo aproximaciones por defecto y exceso cada vez más cercanas), llegando idealmente a que el área calculada en base a los rectángulos trazados por el ínfimo, y el área calculada en base a los rectángulos trazados por el supremo son iguales.

Está claro que este sistema de aproximaciones depende de una división de intervalo de partida, lo que se denomina partición. Cada partición $P= \{ a_{0}, \dots, a_{n} \}$, divide al intervalo en trozos, introduce dos aproximaciones:
$$
\begin{align}
&S_{*}(f,P) \\
&S^{*}(f,P)
\end{align}
$$
## Particiones de un intervalo
<u>Definición</u>: Una <u>partición</u> de $[a,b]$ (con $a<b$) es un conjunto finito $P \subset [a,b]$ tal que $a \in P$ y $b \in P$.

Notación: $P=\{ a_{0},a_{1},\dots,a_{n} \}$ (siempre se escribe de modo ordenado)
$a=a_{0} < a_{1} < \dots < a_{n} = b$
Contamos a partir de 0, ya que de esta forma tenemos n subintervalos.
![[Particiones.png]]
Como vemos, los subintervalos son esencialmente disjuntos, puesto que únicamente se interceptan por su valor de cierre/inicio.
La distancia entre dos puntos consecutivos de la partición puede ser cualquiera.

<u>Definición</u>: (Orden entre las particiones)
$P \subset Q$:
- $Q$ es más fina que $P$ (tiene más subintervalos)
- $P$ es más gruesa que $Q$ (tiene menos subintervalos)
Veremos las propiedades de este orden. Se llama orden, ya que nos permite clasificar las particiones. Este es un orden parcial.
Un orden es aquella relación que es:
- reflexiva: $P \subset P$
- transitiva: $P \subset Q \land Q \subset R \implies P \subset R$
- antisimétrica: $P \subset Q \land Q \subset P \implies P = Q$

No es una relación de orden total, pues existe $P,Q \subset [a,b]$ tales que $P \not \subset Q$ y $Q \not \subset P$.
Ejemplo: $P = \left\{  0, \frac{1}{2}, 1  \right\}, Q = \left\{  0, \frac{1}{3}, \frac{2}{3}, 1  \right\}$
Esto es lo que distingue a este orden (particiones) al orden de los números.
De esta forma, es una relación de orden parcial.

**Observación**:
1. $P_{0}={a,b}$ es la partición más gruesa (la que tiene menos subintervalos)
¿Existe una partición más fina que todas las otras?
La respuesta es no, ya que tendría que contener todos los puntos del intervalo, y esto es imposible ya que hay una cantidad infinita.

2. Dadas $P,Q \subset [a,b]$
La partición $P \cup Q$ es más fina que $P$ y $Q$ a la vez $\implies$ el refinamiento común (de $P$ y $Q$)
Básicamente, si tengo las particiones P y Q, y quiero una partición más fina, puedo unir P y Q, para formar una partición que contenga todos los puntos de ambas. Entonces, si tengo dos particiones, puedo hacer una más fina a partir de estas.

**Definición**
(Norma) Dado $P= \{ a_{0},a_{1},\dots,a_{n} \}$
$$
||P||=máx_{i=0\dots n-1}(a_{i+1}-a_{i})
$$
En pocas palabras, $||P||$ es igual a la longitud del subintervalo más grande.

**Observación**: $P \subset Q \implies ||Q|| \leq ||P||$
Sobre el recíproco: no se cumple, ya que un conjunto puede tener menor norma que otro, pero no tiene porque ser un subconjunto del mismo.

Es importante recordar todos estos términos, ya que serán utilizados de forma extensiva posteriormente.

## Sumas inferiores y superiores
$$
\begin{align}
&\text{Sea } f: [a,b] \to \mathbb{R} \text{ acotada}: \\
&k_{*} \leq f(x) \leq k^{*} \qquad (\forall x \in [a,b]) \\
\end{align}
$$
<u>Notación</u>: Dado $[a', b'] \subset [a,b]$, se escriben:
$$
\begin{align}
&ínf(f,[a',b']) := ínf\{ f(x): x \in [a', b'] \} \\
&sup(f,[a',b']) := sup\{ f(x): x \in [a', b'] \}
\end{align}
$$
La notación anterior, permite especificar el ínfimo y el supremo de un intervalo indicado.
Con esto, podemos definir las sumas inferiores y superiores.

$$
\begin{align}
&\text{Sea } P={a_{0},a_{1},\dots,a_{n}} \\
&\text{Tomamos un subintervalo } [a_{i}, a_{i+1}] \\
&\text{De esta manera, podemos determinar que:} \\
&\text{Suma inferior = } (a_{i+1}-a_{i})\times ínf(f,[a_{i}, a_{i+1}]) \\
&\text{Suma superior = } (a_{i+1}-a_{i})\times sup(f,[a_{i}, a_{i+1}])
\end{align}
$$
Como vemos, la base del rectángulo (ancho) siempre se mantiene igual para el mismo intervalo.

**Definición**
$$
\begin{align}
&\text{Dado } P={a_{0},a_{1},\dots,a_{n}} \subset [a,b] \\
&S_{*}(f,P) = \sum ^{n-1}_{i=0} (a_{i+1}-a_{i}) \times ínf(f,[a_{i}, a_{i+1}]) \\
&S^{*}(f,P) = \sum ^{n-1}_{i=0} (a_{i+1}-a_{i}) \times sup(f,[a_{i}, a_{i+1}])
\end{align}
$$
Esto es simplemente la formalización de la aproximación inferior y superior que definí anteriormente. De esta manera $S_{*}(f,P) \leq Áf \leq S^{*}(f,P)$.

La próxima clase vamos a considerar el conjunto de las aproximaciones $S_{*}(f,P)$ y vamos a tomarle el supremo, y vamos a considerar el conjunto de las aproximaciones $S^{*}(f,P)$ y vamos a tomarle el ínfimo, siendo el supremo mayor que el ínfimo obtenidos, o, en caso de tener suerte, iguales, de forma que habremos calculado exitosamente el área de la función.