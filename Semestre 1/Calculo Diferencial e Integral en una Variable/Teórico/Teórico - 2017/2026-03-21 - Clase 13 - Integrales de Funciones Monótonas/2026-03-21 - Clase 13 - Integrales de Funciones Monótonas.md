Continuamos con integrales y criterios de integración.

# Integrales
La clase pasada vimos ejemplos de funciones integrales. También vimos que todas las funciones constantes son integrales, así como un ejemplo de función no integrable, la función de Dirichlet. Durante esta clase continuaremos con los criterios de integración, así como otros tipos de funciones integrales.

# Proposición - Criterio de integrabilidad a menos de $\epsilon$
Dada una función acotada $f: [a,b] \to \mathbb{R}$, las siguientes condiciones son equivalentes:
1. f es integrable
2. Para todo $\epsilon$, existe una partición $P \subset [a,b]$ tal que
$$
(0 \leq ) \space S^{*}(f,P) - S_{*}(f,P) < \epsilon
$$
Nuevamente, aclarar que la desigualdad entre paréntesis es obvia, puesto que $S^{*}(f,P) \geq S_{*}(f,P)$ en todos los casos.

En la práctica, es un método para demostrar que una función es integrable, establecer un $\epsilon > 0$ y construir una partición tal que la suma inferior y la suma superior tengan diferencia menor que $\epsilon$. Si consigo hacerlo para todo $\epsilon > 0$, entonces sé que la función es integrable.

A continuación, veremos un tipo de función particular.

# Integrales de funciones monótonas
Antes, cuando hacíamos las funciones integrales ya conocíamos la noción de función continua, por esto, podíamos demostrar que toda función continua es integrable. Sin embargo, aún no conocemos la definición de función continua, aún no la hemos visto. Utilizaremos otra condición que ya conocemos: función monótona.
Se sabe que todas las funciones monótonas crecientes o decrecientes son integrables, y esto sin tener en cuenta ningún fenómeno de continuidad.

## Teorema
Si $f: [a,b] \to \mathbb{R}$ es monótona creciente o decreciente, entonces es integrable en $[a,b]$.

Como vemos, el teorema no menciona nada sobre la continuidad, no es necesario verificar que es continua (absolutamente todas las funciones monótonas son integrables). Luego, en el capítulo de continuidad demostraremos el teorema que menciona que toda función continua es integrable, pero esto no significa que una función no es integrable si no es continua.

No especificamos en el teorema que la función debe estar acotada, puesto que la acotación viene automáticamente con la monotonía. Recordemos que las funciones integrables siempre se integran en un intervalo cerrado, no veremos integrales en otro tipo de intervalos.

### Demostración
Solo se considera el caso donde f es creciente.
Como f es monótona creciente, está acotada por $f(a)$ y $f(b)$.
(Acotada horizontalmente por $a$ y $b$, verticalmente por $f(a)$ y $f(b)$. Por esta misma razón no especificamos nada sobre estar acotada en la hipótesis).

Cuando $f(a) = f(b)$, f es constante e integrable. (Ya vimos que todas las funciones constantes son integrables).

A continuación, demostraremos que todas las funciones monótonas crecientes son integrables. Utilizaremos el criterio visto anteriormente. La idea es cortar la función en trozos tan pequeños que al final $I_{*}(f) < I_{*}(f) < \epsilon$.

Ahora, se supone que $f(a) < f(b)$
Sea $\epsilon > 0$. Sea un entero $n \geq 1$ tal que $\frac{b-a}{n} < \frac{\epsilon}{f(b) - f(a)}$
(Cuando corto la longitud del intervalo en n partes, n es tan grande que el resultado es menor que $\frac{\epsilon}{f(b) - f(a)}$).
(Tal entero existe por el principio de Arquímedes).
Podemos desarrollar lo siguiente en base al principio de Arquímedes:
$$
\begin{align}
&\frac{b-a}{n} < \frac{\epsilon}{f(b) - f(a)} \\
&\Longleftrightarrow \frac{n}{b-a} > \frac{f(b) - f(a)}{\epsilon} \\
&\Longleftrightarrow n > \frac{f(b) - f(a)}{\epsilon} \times (b-a) \\
&\Longleftrightarrow n > \frac{(f(b) - f(a)) \times (b-a)}{\epsilon} \\
\end{align}
$$

Sea $P=\{ a_{0}, a_{1}, \dots, a_{n} \}$ la partición de $[a,b]$ definida por
$$
a_{i} = a + i \times \frac{b-a}{n}
$$
$\frac{b-a}{n}$ es la longitud de cada subintervalo de la partición P. Todos los subintervalos tienen la misma longitud.

![[Integrales de funciones monótonas (demostración).png]]
En la representación gráfica utilizamos una función continua, aunque si no lo fuera también funcionaría.
Como vemos, al tomar el ínfimo y supremo de cada subintervalo, obtenemos un área que está presente en la suma superior, pero no en la inferior (la diferencia de ambos). Con dichas figuras, podemos construir un rectángulo de base $\frac{b-a}{n}$ y altura $f(b)-f(a)$.
Como elegí el valor de n en base a la desigualdad anterior, tenemos que $\frac{b-a}{n} < \frac{\epsilon}{f(b) - f(a)}$. De esta forma, y sabiendo que el área de la figura es $\frac{(b-a) \times (f(b)-f(a))}{n}$, llegamos a la conclusión de que
$$
\frac{(b-a) \times (f(b)-f(a))}{n} < \epsilon
$$
De esta forma, demostramos gráficamente que la partición cumple con la condición establecida.
En base a esta representación, realizaremos la demostración formal:

En cada subintervalo $a_{i}, a_{i+1}$
$$
\begin{align}
&ínf(f, [a_{i},a_{i+1}]) = f(a_{i}) \\
&sup(f, [a_{i},a_{i+1}]) = f(a_{i+1})
\end{align}
$$
Esto nos permite calcular las sumas superiores e inferiores:
$$
\begin{align}
&S_{*}(f,P) = \sum_{i=0}^{n-1}(a_{i+1}-a_{i})f(a_{i}) \\
&S^{*}(f,P) = \sum_{i=0}^{n-1}(a_{i+1}-a_{i})f(a_{i+1})
\end{align}
$$
Ahora, desarrollaremos la diferencia entre la suma superior e inferior, considerando además que el factor común $a_{i+1}-a_{i} = \frac{b-a}{n}$ para todos los subintervalos.
$$
\begin{align}
&S^{*}(f,P) - S_{*}(f,P) = \sum_{i=0}^{n-1} \left( \frac{b-a}{n} \right)(f(a_{i+1})-f(a_{i})) \\
&=\left( \frac{b-a}{n} \right) \sum_{i=0}^{n-1} (f(a_{i+1})-f(a_{i}))
\end{align}
$$
Otra cosa que podemos observar es que $\left( \frac{b-a}{n} \right)$, al ser factor común, lo podemos extraer de la sumatoria y que sea simplemente un factor del resultado.
Además, si desarrollamos la sumatoria, podemos ver lo siguiente: 
$$
\begin{align}
&\sum_{i=0}^{n-1} (f(a_{i+1})-f(a_{i})) = \\
&(\cancel{ f(a_{1}) } - f(a_{0})) + \cancel{ (f(a_{2}) } - \cancel{ f(a_{1}) }) + \cancel{ (f(a_{3}) } - \cancel{ f(a_{2}) }) + \dots + (f(a_{n}) - \cancel{ f(a_{n-1}) }) \\
&=f(a_{n}) - f(a_{0})
\end{align}
$$
Proseguimos en base a esto:
$$
=\frac{b-a}{n} \times (f(b) - f(a)) < \epsilon
$$
La idea es seguir la lógica de la figura en lenguaje matemático al mismo tiempo, con la idea de llegar al mismo resultado y conseguir demostrar exitosamente.

Finalizamos la demostración. Logramos construir una partición, tal que la diferencia entre la suma superior y la suma inferior es menor que $\epsilon$.

Por el criterio de integrabilidad a menos de $\epsilon$, deduzco que la función es integrable. Como vemos, para mostrar que una función es integrable, tenemos que comparar sus sumas inferiores y superiores y mostrar al final que la diferencia es minúscula.

Deberíamos hacer la misma demostración con las funciones decrecientes (también con el dibujo que corresponde). La demostración es análoga, aunque hay que adaptar cada uno de los detalles necesarios, siendo un buen ejercicio para entender la demostración.

Ahora, veremos un ejemplo de función integrable.
Por supuesto, conocemos infinidad de funciones integrables luego de ver que las funciones constantes y monótonas son integrables. En este caso, estudiaremos la primer función no trivial: la parábola.

A continuación, demostraremos que la parábola, en su parte positiva, es integrable. Solo nos enfocamos en la parte positiva, ya que así trabajamos con una función monótona creciente.

### Ejemplo
Dado $a > 0$, calcular $\int_{0}^{a} x^{2} dx$
Podríamos usar el criterio de integración, pero no se necesita, realizaremos una demostración más directa. Para esto, utilizaremos un lema.

### Lema
Si $0 \leq x \leq y$, entonces
$$
(y-x)x^{2} \leq \frac{y^{3} - x^{3}}{3} \leq (y-x)y^{2}
$$
### Demostración
$(y^{3}-x^{3})= (y-x)(x^{2} + xy + y^{2})$

Aclarar que tanto x como y son positivos.
Se observa que
$$
3x^{2} \leq x^{2} + xy + y^{2} \leq y^{2} + y^{2} + y^{2} = 3y^{2}
$$
La desigualdad anterior tiene sentido ya que $x \leq y$, entonces $x^{3} \leq y^{3}$
A continuación, multiplicamos la desigualdad por y-x:
$$
3(y-x)x^{2} \leq (y-x)(x^{2} + xy + y^{2}) = y^{3} - x^{3} \leq 3(y-x)y^{2}
$$
Si divido esta desigualdad entre 3, obtengo la desigualdad inicial.
$$
(y-x)x^{2} \leq \frac{y^{3} - x^{3}}{3} \leq (y-x)y^{2}
$$
La desigualdad está dividida en tres partes:
- $(y-x)x^{2}$ es un trozo de suma inferior de un intervalo de amplitud entre x e y, y el valor de la función cuadrado en el comienzo. Aquí, $y-x$ representa la base del rectángulo, mientras que $x^{2}$ es el ínfimo del intervalo local.
- $(y-x)y^{2}$ ídem que el anterior, pero para la suma superior. $y-x$ representa la base del rectángulo, mientras que $y^{2}$ es el supremo del intervalo local.
- $\frac{y^{3} - x^{3}}{3}$ es el valor exacto del área bajo la curva.

De esta forma, tenemos algo bien conocido entre el trozo de suma inferior y el trozo de suma superior. Cuando sumamos todo, los elementos se simplifican de a dos.

Esto nos va a permitir integrar todas las funciones polinomiales previo al teorema fundamental.

Ahora, calcularemos la integral deseada:
Sea $P = \{ a_{0}, a_{1}, \dots, \} \subset [a, b]$
Podemos utilizar el lema para expresar la relación entre la suma inferior y superior, así como la fórmula para calcular el área debajo de la curva.
$$
S_{*}(f,P) = \sum_{i=0}^{n-1}(a_{i+1} - a_{i})a_{i}^{2} \leq \sum_{i=0}^{n-1} \left( \frac{a_{i+1}^{3}}{3} - \frac{a_{i}^{3}}{3} \right) = \frac{a_{n}^{3}}{3} - \frac{a_{0}^{3}}{3} = \frac{a^{3}}{3}
$$

$a_{i}^{2}$ es el ínfimo local.
De esta forma, demostré que todas las sumas inferiores son menores o iguales a $\frac{a^{3}}{3}$.
Esto me dice que $\frac{a^{3}}{3}$ es un número que no depende de P, entonces esté valor es una cota superior de todas las sumas inferiores, de modo que es mayor o igual a $I_{*}(f)$.

Luego:
$$
I_{*}(f) \leq \frac{a^{3}}{3}
$$
Ahora, haremos el mismo razonamiento con la suma superior
$$
S^{*}(f,P) = \sum_{i=0}^{n-1}(a_{i+1} - a_{i})a_{i+1}^{2} \geq \sum_{i=0}^{n-1} \left( \frac{a_{i+1}^{3}}{3} - \frac{a_{i}^{3}}{3} \right) = \frac{a_{n}^{3}}{3} - \frac{a_{0}^{3}}{3} = \frac{a^{3}}{3}
$$
$a_{i}^{2}$ es el supremo local.
En definitiva, nos basamos totalmente en el lema.
Esto demuestra que $\frac{a^{3}}{3}$ es cota inferior de todas las sumas superiores, de forma que es menor o igual a $I^{*}(f)$.

Luego:
$$
I^{*}(f) \geq \frac{a^{3}}{3}
$$
Como sabemos que la función es monótona creciente, es integrable (como demostramos previamente), por lo que $I_{*}(f) = I^{*}(f)$.
Por lo tanto:
$$
\int_{0}^{a} x^{2} dx = I_{*}(f) = I^{*}(f) = \frac{a^{3}}{3}
$$
Ahora, sabemos medir el área de parábolas, funciones con curvas. Esto era imposible de calcular antes de desarrollar toda la teoría.

Ejemplos:
![[Cálculo de área de parábola.png]]

**IMPORTANTE**: Todo esto únicamente nos sirve para calcular el área de parábolas entre 0 y a puntualmente. Al final veremos como hacer la parte negativa, además de saber como trabajar con funciones de tipo $x^{n}$, pudiendo integrar todos los polinomios.

Todos estos avances fueron y son super utilizados en cálculos astronómicos, por ejemplo, por lo que supuso un avance gigantesco.

# Propiedad - Monotonía de la integral
Sean $f, g: [a,b] \to \mathbb{R}$ dos funciones integrables. (dos funciones integrables en un mismo intervalo)
Si $f(x) \leq g(x) \qquad (\forall x \in [a,b])$ ($f \leq g$ (punto a punto)), entonces $\int_{a}^{b} f \leq \int_{a}^{b} g$

Con hacer la figura ya es evidente. Para demostrarlo, hay que demostrar que todas las sumas inferiores de f son menores que las sumas inferiores correspondientes de g, entre otras cosas.

## Corolario
$$
\begin{align}
&f \geq 0 \implies \int_{a}^{b}f \geq 0 \\
&f \leq 0 \implies \int_{a}^{b}f \leq 0
\end{align}
$$
En ambos casos, la integral puede ser nula (incluso aunque sea estrictamente positiva o estrictamente negativa). Por si acaso, en este tipo de enunciado, no conviene utilizar desigualdades estrictas.

En particular, esto nos da un método para calcular la integral entre dos curvas.

## Observación
Si $f \leq g$, entonces el caso es el siguiente:

¿Cómo se calcula la integral en este caso? (Área entre las dos funciones).

Muy sencillo, simplemente debemos restar las integrales de cada función (al área mayor le restamos el área menor, u obtenemos el valor absoluto de la diferencia).
![[Representación de operaciones (resta de funciones).png]]
$$
\int_{a}^{b} g - \int_{a}^{b} f = \left( \int_{a}^{b} (g-f) \right)
$$
Es bastante intuitivo, puesto que al área de g le resto el área de f, y es válido, ya que f se encuentra dentro de g.

Incluso, este mismo razonamiento nos sirve para calcular el área de figuras más complejas, capturando la parte por debajo con una función "más pequeña", y la parte por encima con otra función "más grande".

Algo que veremos posteriormente es que la resta de las integrales es lo mismo que la integral de la resta (planteado en la imagen).

Esto se utiliza muchísimo, puesto que el cálculo de áreas es una tarea constante en el trabajo de un ingeniero, aplicando estos mismos conceptos, por ejemplo, en el cálculo de volúmenes.
Por ejemplo, si yo tengo una figura de tres dimensiones (generalmente son regulares, pero puede ser cualquier cosa), la cual tiene una medida que va desde $z_{min}$ hasta $z_{max}$, yo puedo calcular, para cada valor de z, el área de la figura en ese punto (utilizando una integral). Luego, para calcular el área de la figura, realizo la integral desde $z_{min}$ hasta $z_{max}$, de cada una de las áreas:
![[Representación de operaciones (cálculo de volúmenes).png]]
$$
\begin{align}
&A(z) = \int \dots \\
&V = \int_{z_{min}}^{z_{max}} A(z) dz
\end{align}
$$
De esta forma, el método de calculo de áreas es tan general que también puede utilizarse para calcular volúmenes.

Otro ejemplo:
Construimos dos funciones $f,g: [-1,1] \to \mathbb{R}$
$$
\begin{align}
&f(x) = \sqrt{ 1-x^{2} } \\
&g(x) = -f(x)
\end{align}
$$
Tomamos como dominio el intervalo $[-1,1]$, ya que más allá de -1 y 1, pasamos a números complejos (queda raíz cuadrada de un negativo).
$$
f(x) = \sqrt{ 1-x^{2} } \implies y = \sqrt{ 1-x^{2} } \implies y^{2} = 1 - x^{2} \implies x^{2} + y^{2} = 1
$$
La fórmula se grafica como un semicírculo de radio 1 y origen en (0,0).
De esta forma, g(x) permite completar el círculo.
![[Representación de operaciones (circunferencia).png]]
La diferencia de sus integrales dará como resultado el área del círculo correspondiente.

El análisis fue impulsado por problemas como estos, el cálculo de áreas y la aplicación de integrales. Como las dos anteriores, hay muchas más aplicaciones y usos de área e integrales en matemáticas e ingeniería en general.

A continuación, hablaremos de la linealidad de la integral.

# Linealidad de la integral

## Teorema
Sean $f, g: [a,b] \to \mathbb{R}$ integrables.
1. $f + g$ es integrable (si tengo dos funciones integrables, la suma de ambas también será integrable), y $\int_{a}^{b} (f+g) = \int_{a}^{b} f + \int_{a}^{b} g$
Se dice que la integral es aditiva: si se integrar f y g por separado, también se integrar $f + g$. Es la razón que explica por que consideramos áreas algebraicas. Si en lugar de considerar el área algebraica, consideramos el área geométrica, no funciona. Por ejemplo, si tenemos dos funciones opuestas, al utilizar el área geométrica los valores serán positivos, por lo que no se anularan (cosa que pasa para el área algebraica).

2. Para todo $\alpha \in \mathbb{R}$, $\alpha f$ es integrable y $\int_{a}^{b} \alpha f = \alpha \cdot \int_{a}^{b} f$
Esto tiene fuertes influencias de Geometría y Álgebra Lineal.

**Observación**
El conjunto $F([a,b], \mathbb{R})$ (conjunto de funciones del intervalo $[a,b]$ en $\mathbb{R}$) es un $\mathbb{R}$-espacio vectorial.
$$
Int([a,b]) \subsetneq F([a,b], \mathbb{R})
$$
$Int([a,b])$ es el conjunto que contiene a todas las funciones integrables en el intervalo $[a,b]$, de este modo, es un subconjunto no equivalente a $F([a,b], \mathbb{R})$. En conclusión, podemos decir que $Int([a,b])$ es un subespacio vectorial.

La integral es una función definida en este subespacio vectorial. La operación integral toma como argumento una función integral y devuelve un valor perteneciente a $\mathbb{R}$, siendo la integral de dicha función. Entonces, podemos establecer que ==la función integral es una transformación lineal==.
El vínculo entre cálculo y algebra lineal es constante, y será algo habitual a lo largo del curso.

Relación entre las funciones, funciones acotadas, y funciones integrales:
$$
\text{funciones} f: [a,b] \to \mathbb{R} \qquad \supset \qquad \text{funciones acotadas} \qquad \supset \qquad \text{funciones integrales}
$$
Los tres conjuntos son de dimensión infinita.