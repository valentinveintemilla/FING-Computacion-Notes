# Integrales
Esta será la última clase de integrales.

La vez pasada, desarrollamos la formula general para calcular la integral de un monomio en un intervalo dado:
$$
\int_{a}^{b} x^{p} dx = \frac{b^{p + 1} - a^{p + 1}}{p + 1}
$$
Haciendo combinaciones lineales de la formula anterior, podemos calcular la integral de cualquier polinomio.

Además, vimos una generalización a todos los polinomios, utilizando la primitiva de f:
$$
\int_{a}^{b} f(x) dx = \underbrace{ F(b) }_{ \text{primitiva de } f } - F(a)
$$
$$
\text{Primitiva de } f: F' = f
$$
Se puede utilizar cualquiera de los dos métodos, puesto que nos llevan al mismo resultado.

A continuación, veremos un nuevo tipo de función que no es abarcada por la fórmula anterior:

# Integral de $t \mapsto \frac{1}{t}$
Sea $f(t) = \frac{1}{t}$ para todo $t > 0$ ($f: \mathbb{R}^{+} \to \mathbb{R}$)

Problema: calcular $\int_{a}^{b} \frac{1}{t} dt$ para $0 < a < b$

Después de haber estudiado los polinomios, la función más sencilla que no es un polinomio es $\frac{1}{t}$. Después también explicaremos por que utilizamos la letra t en lugar de otra (si bien se puede utilizar cualquiera).

**Observación**: f es monótona decreciente en $(0, +\infty)$: es localmente integrable.
De esta forma, sabemos que es integrable en cualquier intervalo.

A continuación, graficamos la función correspondiente:
![[Gráfica de la función 1 sobre t.png]]
Como vemos, es una función que invierte las cosas con respecto a la multiplicación (a medida que nos acercamos a 0 tiende a $+\infty$, y si nos acercamos a $+\infty$ tiende a 0).

Podemos visualizar lo siguiente:
Si tomamos un intervalo $[a, b]$ y multiplicamos dicho intervalo por $\lambda$, quedando $[\lambda a, \lambda b]$, podemos observar que tenemos una dilatación horizontal según un factor $\lambda$. Una de las cosas más interesantes que suceden a la hora de examinar la relación entre a y $\lambda a$, y b y $\lambda b$ es:
$$
\begin{align}
&f(\lambda a) = \frac{f(a)}{\lambda} \\
&f(\lambda b) = \frac{f(b)}{\lambda}
\end{align}
$$
Esto quiere decir que al multiplicar el intervalo por lambda, estoy haciendo al mismo tiempo una dilatación horizontal por el factor mencionado, y una dilatación vertical por un factor $\frac{1}{\lambda}$. De esta forma, las áreas de las regiones son iguales, ya que hay una compensación entre la dilatación horizontal y la vertical.

## Propiedad
Para todos $a, b, \lambda > 0$ con $a < b$:
$$
\int_{\lambda a}^{\lambda b} \frac{1}{t} dt = \int_{a}^{b} \frac{1}{t} dt
$$
==Dicha propiedad SOLO FUNCIONA para esta función==.

### Demostración
Sea $f : [a, b] \to \mathbb{R}$ definida por $f(t) = \frac{1}{t}$
Se define $g : [\lambda a, \lambda b] \to \mathbb{R}$ definida por $g(t) = f\left( \frac{t}{\lambda} \right) = \frac{\lambda}{t}$

Estudiaremos la función dilatada g.
$$
\int_{\lambda a}^{\lambda b} g(t) dt = \int_{\lambda a}^{\lambda b} \frac{\lambda}{t} dt \overbrace{ = }^{ \text{por dilatación} } \lambda \cdot \int_{a}^{b} f(t) dt = \lambda \cdot \int_{a}^{b} \frac{1}{t} dt
$$
Y ahora solo nos queda operar. Podemos sacar $\lambda$ de la integral de g, por linealidad (ya que es un valor que se mantiene siempre).
$$
\implies \int_{\lambda a}^{\lambda b} \frac{\lambda}{t} dt = \lambda \cdot \int_{\lambda a}^{\lambda b} \frac{1}{t} dt = \lambda \cdot \int_{a}^{b} \frac{1}{t} dt \implies \int_{\lambda a}^{\lambda b} \frac{1}{t} dt = \int_{a}^{b} \frac{1}{t} dt
$$
De esta forma, llegamos a la conclusión de que la integral para la región $[a, b]$ es igual a la integral en el intervalo $[\lambda a, \lambda b]$. Esto se da ya que la región se dilata por un factor $\lambda$ horizontalmente, y se dilata por un factor $\frac{1}{\lambda}$ verticalmente.

Esta propiedad es fundamental de la función $\frac{1}{t}$ y es casi la única función que cumple con dicha propiedad.

En particular, esto dice que la integral entre dos extremos de la función $\frac{1}{t}$ no depende de los extremos, únicamente depende del cociente entre ambos extremos (ya que, por ejemplo, $\frac{\lambda b}{\lambda a} = \frac{b}{a}$).

Por esta razón es importante tener claro que la propiedad de simplificación por $\lambda$, solo se cumple para esta función y no se cumple para el resto.

En definitiva, demostramos la propiedad indicada. También se puede demostrar de forma directa, comparando las sumas inferiores y superiores de ambos intervalos, así como su ínfimo y supremo, y finalmente su integral inferior y superior, llegando a la conclusión de que son iguales.

Ahora, nos gustaría calcular este área. Sin embargo, existe un metateorema que indica que la integral anterior no se puede expresar de modo sencillo a partir de a y b, de modo que no puede ser expresada como un polinomio o fracción racional (por sumas, restas, productos y cocientes a partir de a y b).
Por esta razón, tenemos que introducir una nueva función.

**Observación**:
$\int_{a}^{b} \frac{1}{t} dt$ no se puede expresar como un polinomio o una fracción racional en función de a y de b.

A continuación, introducimos la nueva función que nos permitirá calcular el valor de la integral.

# Función logaritmo
**Definición**
La función logaritmo es la función
$$
\log: (0, +\infty) \to \mathbb{R}
$$
definida por
$$
\log x := \int_{1}^{x} \frac{1}{t} dt \qquad ( \text{para todo } x > 0)
$$
A partir de esta definición, tenemos una nueva función con sus particularidades y comportamiento.
Esta definición solo supone que x es positivo, por lo que, con respecto a 1, puede ser menor (pero mayor que 0), igual, o mayor. De esta forma, utilizo la notación extendida, ya que los extremos se pueden encontrar en un orden cualquiera.

**Observación**
Por definición, tenemos que
$$
\log x = \begin{cases}
\int_{1}^{x} \frac{1}{t} dt \geq 0 &\text{si} \qquad x > 1 \\
0 &\text{si} \qquad x = 1 \\
-\int_{x}^{1} \frac{1}{t} dt \leq 0 &\text{si} \qquad x < 1
\end{cases}
$$
Podríamos decir que la gráfica es negativa antes de 1, es 0 en 1, y positiva después de 1.

Previo a graficarla, vamos a demostrar que es una función estrictamente creciente. En el futuro, veremos que cuando x tiende a 0, la función tiende a $-\infty$, cuando x tiende a $+\infty$, la función tiende a $+\infty$, y que en f(1), la pendiente es exactamente 1.

## Proposición
La función logaritmo es estrictamente creciente en el intervalo $(0, +\infty)$
Esto quiere decir que si tomo dos números, tal que $a \leq b$, entonces $\log(a) \leq \log(b)$

### Demostración
Sean $x, y > 0$ tales que $x < y$. Se observa que:
$$
\log y - \log x = \int_{1}^{y} \frac{1}{t} dt - \int_{1}^{x} \frac{1}{t} dt
$$
Podemos invertir los extremos de $\int_{1}^{x} \frac{1}{t} dt$, de modo que cambia su signo. De esta forma, también podemos unir ambas integrales en una, puesto que una comienza en 1 y la otra finaliza en 1.
$$
\int_{1}^{y} \frac{1}{t} dt - \int_{1}^{x} \frac{1}{t} dt = \int_{1}^{y} \frac{1}{t} dt + \int_{x}^{1} \frac{1}{t} dt = \int_{x}^{y} \frac{1}{t} dt \geq (y - x) \cdot \frac{1}{x} > 0
$$
Sobre la función $\frac{1}{t}$, podemos decir que es estrictamente positiva. Además, como x es menor que y, nos encontramos frente a una integral usual, que nos dará un valor positivo. Por último, podemos decir que dicha integral es mayor o igual a la longitud del intervalo por el mínimo, que como también es un valor positivo, es mayor que 0.

Luego: $\log x < \log y$

De esta forma, demostramos que si un número es menor que otro, entonces su logaritmo también lo es.

A continuación, demostraremos la propiedad fundamental del logaritmo.

## Proposición - Propiedad fundamental del logaritmo
$\forall x, y > 0$:
0. $\log 1 = 0$
1. $\log(xy) = \log x + \log y$
2. $\log\left( \frac{x}{y} \right) = \log x - \log y$
3. $\log\left( \frac{1}{x} \right) = - \log x$
Esta propiedad se cumple para todo par de números positivos. La propiedad establece que el logaritmo transforma los productos en sumas. Transforma la estructura multiplicativa en la estructura aditiva.
Incluso transforma el neutro de la multiplicación en el neutro de la adición, por lo que $\log 1 = 0$

Ahora, demostraremos la propiedad enunciada, punto por punto.

### Demostración (1)
$$
\log(xy) = \int_{1}^{xy} \frac{1}{t} dt = \int_{1}^{x} \frac{1}{t} dt + \int_{x}^{xy} \frac{1}{t} dt
$$
Básicamente, desarrollamos la integral equivalente al logaritmo especificado, descompusimos la integral en dos trozos aplicando la propiedad de aditividad respecto al intervalo, que funciona en todos los casos.

En base a la propiedad de dilatación en función de $\lambda$ que vimos anteriormente, podemos desarrollar lo siguiente: x se puede expresar como $x1$, quedando x en ambos extremos de la integral. De esta forma, podemos cancelar los x de ambos lados, quedando la integral del intervalo $(1, y)$.
$$
\int_{1}^{x} \frac{1}{t} dt + \int_{x}^{xy} \frac{1}{t} dt = \int_{1}^{x} \frac{1}{t} dt + \int_{\cancel{ x }1}^{\cancel{ x }y} \frac{1}{t} dt = \int_{1}^{x} \frac{1}{t} dt + \int_{1}^{y} \frac{1}{t} dt = \log(xy)
$$
En conclusión, logramos demostrar que:
$$
\log(xy) = \log(x) + \log(y)
$$
Esto me da la propiedad fundamental del logaritmo.

### Demostración (2)
$$
\log x = \log \left( y \times \frac{x}{y} \right) = \log y + \log \frac{x}{y} \qquad (\text{por (1)})
$$
Luego:
$$
\log \frac{x}{y} = \log x - \log y
$$
Como vemos, al llegar a $\log x = \log y + \log \frac{x}{y}$, llegamos a la conclusión de que $\log \frac{x}{y} = \log x - \log y$, ya que, de esta forma:
$$
\log x = \log y + \log \frac{x}{y} = \cancel{ \log y } + \log x - \cancel{ \log y } = \log x
$$

### Demostración (3)
$\log \left( \frac{1}{x} \right) = \log (1) - \log (x) = - \log x$
Es un caso particular de la propiedad (2).

Una convención de la función logaritmo es que, cuando solo hay una variable no es necesario poner paréntesis, como seno y coseno.


### Observación
La función logaritmo fue inventada por John Napier (1550 - 1617). En realidad, el inventó el logaritmo decimal, pero se puede deducir a partir del logaritmo natural. Su profesión principal no era la matemática, aunque su principal invención es en el área de la matemática. En su época ni siquiera existían las calculadoras.

Napier observó que hay una gran diferencia entre el algoritmo de cálculo de adición (suma), y el algoritmo de cálculo del producto, siendo más complejo este último, y más aún a medida que aumentaba el tamaño de los factores.

Por esta razón, Napier tuvo la idea de inventar una nueva clase de número en los cuales la suma se comporta como un producto, o el producto se comporta como una suma.

Esta es la función logaritmo, y nos da un nuevo algoritmo para simplificar el cálculo de los productos. Incluso produjo la primera tabla de logaritmos, un libro que da muchos de los valores de logaritmo.

#### Tabla de logaritmos
Dicha tabla se utilizaba de la siguiente forma:
1. Yo tengo dos números y quiero hallar su producto.
2. Busco ambos números en la parte izquierda del "diccionario" (tabla de algoritmos) para saber su correspondiente en logaritmo.
3. Sumo los logaritmos de ambos números, por ejemplo $\log a + \log b = \log(ab)$, de forma que el resultado obtenido es el logaritmo del producto de dichos números.
4. Busco el resultado obtenido en la parte derecha del "diccionario", y su valor correspondiente será el producto de los dos números que tenía al inicio.

Esta forma de operar cambio mucho el mundo de las matemáticas, puesto que facilitaba sumamente el cálculo de productos. Incluso se llegaron a utilizar hasta mediados del siglo pasado.
Los logaritmos en dichas tablas son los logaritmos naturales.

Dicha tabla también sirve para hacer divisiones, pues las tratamos como restas de logaritmos.
Incluso sirve para calcular raíces cuadradas, o raíces n-ésimas, considerando que:
$$
\begin{align}
&\log \sqrt{ x } = \frac{1}{2} \log x \\
&\log \sqrt[n]{ x } = \frac{1}{n} \log x
\end{align}
$$
Ahora entendemos la importancia de los logaritmos.

Todo este tiempo hemos estado hablando del logaritmo natural, o también conocido como logaritmo neperiano.
$$
\log x : \text{ logaritmo natural/neperiano}
$$
El cual tiene la siguiente particularidad:
$$
\log \underbrace{ e }_{ 2,718\dots } = 1
$$
Igualmente, este no fue el logaritmo inventado por Napier, sino que fue el logaritmo en base 10:
$$
\log_{10}x := \frac{\log x}{\log 10}
$$
Este logaritmo satisface exactamente las mismas propiedades vistas anteriormente, siendo lo único que cambia el valor del cual se va a obtener 1:
$$
\log_{10}(10) = 1
$$
Como las tablas de este tipo de logaritmo iban únicamente del 1 al 10, se podía hacer lo siguiente para números mayores:
$$
\log_{10}(357,223) = \log_{10}(3,57223) + 2 \qquad \text{(+ cantidad de lugares que se corre la coma)}
$$

A continuación, realizaremos algunas observaciones ahora que tenemos a la función logaritmo.

### Proposición
Para todos $a, b > 0$ (sin importar el orden), tenemos que:
$$
\int_{a}^{b} \frac{1}{t} dt = \log b - \log a = \log \frac{b}{a}
$$
Ahora, el logaritmo nos permite calcular la integral de la función inverso
Además, $\log b - \log a$ equivale a $\log \frac{b}{a}$ gracias a la propiedad fundamental del logaritmo demostrada anteriormente. De esta forma, la integral solo depende del cociente entre b y a propiamente dicho, no de a y b por separado.
Es así que tenemos una formula explícita para calcular la integral de la función $\frac{1}{t}$.

A continuación, demostramos la fórmula:
$$
\int_{a}^{b} \frac{1}{t} dt = \int_{1}^{b} \frac{1}{t} dt - \int_{1}^{a} \frac{1}{t} dt = \log b - \log a = \log \frac{b}{a}
$$
Utilizamos la propiedad de aditividad respecto al intervalo para descomponer la integral en dos partes.

A continuación, resolveremos un ejercicio:

### Ejercicio
Demostrar que $\forall x > 0$:
$$
1 - \frac{1}{x} \leq \log x \leq x - 1
$$
De esta forma, se establecen cotas de logaritmo.
Graficaremos las funciones para visualizar y comparar las funciones adecuadamente:

Esta fórmula es interesante ya que nos brinda el límite del logaritmo, nos permite demostrar que es continuo en el punto 1, y que además es derivable.
![[Grafica de los límites de la función logaritmo.png]]

Demostraremos la fórmula
Vimos que cuando se define el logaritmo, tenemos tres casos:
- $x > 1$
- $x = 1$
- $x < 1$
Distinguiremos los tres casos, aunque uno de ellos es trivial: $x = 1$

#### Demostración
Distinguimos 3 casos
- Caso $x = 1$:
$$
0 \leq 0 \leq 0
$$
Es un caso trivial, no hay nada que demostrar.

- Caso $x > 1$:
$$
\log x = \int_{1}^{x} \frac{1}{t} dt
$$
La formula anterior siempre se cumple, pero además, como x esta a la derecha de 1 (es mayor), podemos aplicar las propiedades de monotonía. Además, podemos decir que el ínfimo de la función en el intervalo $[1, x]$ es $\frac{1}{x}$ (RECORDEMOS QUE ESTAMOS HABLANDO DE LA FUNCIÓN $\frac{1}{t}$)

Para todo $t \in [1, x]$:
$$
\frac{1}{x} \leq \frac{1}{t} \leq 1
$$
$\frac{1}{x}$ es el ínfimo en el intervalo, mientras que 1 es el supremo. Además, sabemos que dichos valores son constantes.

Podemos hacer la integración de la función:
$$
\int_{1}^{x} \frac{1}{t} dt
$$
Sabemos que el valor de dicha integral se encuentra entre el área en base al ínfimo ($\frac{1}{x}$) y el área en base al supremo (1) de dicha función.
De esta manera:
$$
\underbrace{ (x - 1) \cdot \frac{1}{x} }_{ \text{Rectángulo de menor área (con ínfimo)} } \leq \int_{1}^{x} \frac{1}{t} dt \leq \underbrace{ (x - 1) \cdot 1 }_{ \text{Rectángulo de mayor área (con supremo)} }
$$
Al final, si desarrollamos los productos, obtenemos:
$$
1 - \frac{1}{x} \leq \log x \leq x - 1
$$
Esto demuestra la desigualdad cuando $x > 1$.

- Caso $x < 1$:
Ahora, x está a la izquierda de 1, por lo que trabajaremos con el intervalo $[x, 1]$. De esta forma, también se invierte la desigualdad (por inversión).

Para todo $t \in [x, 1]$:
$$
1 \leq \frac{1}{t} \leq \frac{1}{x}
$$
Ahora, podemos integrar (considerando el intervalo actual, o sea de x a 1):
$$
(1-x) \cdot 1 \leq \int_{x}^{1} \frac{1}{t} dt \leq (1 - x) \cdot \frac{1}{x}
$$
Concluimos con el desarrollo de los productos:
$$
1 - x \leq - \log x \leq \frac{1}{x} - 1
$$
Para llegar a la desigualdad original, simplemente invertimos los signos de todas las partes, invirtiendo el orden:
$$
1 - \frac{1}{x} \leq \log x \leq x - 1
$$

==IMPORTANTE: RECORDAR QUE SIEMPRE TRABAJAMOS CON VALORES POSITIVOS. CONSIDERAMOS A LA FUNCIÓN $\log x$ EN EL INTERVALO $(0, +\infty)$==.

Con esto, demostramos la desigualdad propuesta para todos los casos posibles de valores de x. De esta manera, conseguimos poner la gráfica de logaritmo entre dos funciones sencillas que tienen la misma pendiente para $x = 1$.
Esto implica que la función logaritmo es continua y derivable en este punto, y tiene la misma pendiente. Este ejercicio nos brindó un montón de información de la función logaritmo.

Consideramos una definición y al final obtuvimos todas las propiedades del logaritmo que salen de la definición geométrica.

Como vimos al comienzo, la forma más intuitiva de ver al logaritmo $\log x$ es quizás como el área de un intervalo $[1, x]$ en la función $\frac{1}{t}$.

Importante destacar que este algoritmo no funciona para 0, ya que 0 no tiene logaritmo.