# Integrales
La clase pasada vimos múltiples propiedades, finalizando con la aditividad respecto al intervalo.

# Aditividad respecto al intervalo
**Propiedad**
Sea $f: I \to \mathbb{R}$ definida en un intervalo $I \subset \mathbb{R}$, y $a, b, c \in I$ tales que $a < b < c$.
Si f es integrable en ambos intervalos $[a,b]$ y $[b,c]$, entonces f es integrable en $[a, c] (= [a, b] \cup [b, c])$ y
$$
\int_{a}^{c} f = \int_{a}^{b} f + \int_{b}^{c} f 
$$
Si bien le llamamos "aditividad respecto al intervalo", en otros lugares se conoce como la relación de Chasles. Esta regla de la suma vectorial establece que si yo tengo tres puntos cualesquiera $A, B, C$, la suma de los vectores consecutivos $\vec{AB} \text{ y } \vec{BC}$ es igual al vector $\vec{AC}$.
Aplicando esta misma idea a las áreas algebraicas, llegamos a la formula anterior que involucra a las integrales. De esta manera, podemos decir que se comportan simbólicamente como vectores.

Para demostrar esta propiedad, se utiliza el criterio de integración (puesto que conocemos como calcular la integral de dicha función en el intervalo establecido).

## Propiedad
$f: I \to \mathbb{R}$ es localmente integrable si es integrable en cualquier intervalo $[a, b] \to I$.

Cuando se integra una función, siempre se integra en un intervalo cerrado, pues la noción de integral no tiene sentido afuera.
Sin embargo, a veces tenemos funciones definidas, por ejemplo, en todo $\mathbb{R}$. Y está claro que si solo consideramos f en un intervalo dado, puede ser integrable en el mismo, pero también puede darse que f sea integrable, independientemente del intervalo establecido. Esto sucede en las funciones localmente integrables, puesto que se pueden formar nuevos intervalos con la unión de otros, acortando un intervalo existente, etc.

Hasta ahora, la notación únicamente tenía sentido cuando $a < b$. Sin embargo, vamos a extender la notación.

# Extensión de la notación $\int_{a}^{b} f$ en los casos $\begin{cases} a = b \\ a > b \end{cases}$
$$
\int_{a}^{b} f := \begin{cases}
0 \text{ si } a = b \\
-\int_{b}^{a} f \text{ si } a > b
\end{cases}
$$
Todas las funciones son integrables para el caso $a = b$, puesto que solo tengo que considerar un punto, por lo que es una función constante. En este caso, consideramos que su integral vale 0.

Para el caso $a > b$, consideramos que, en lugar de ir de izquierda a derecha, vamos "al revés", por lo que invertimos el signo de la integral. Como $a > b$, no puedo calcular la integral de $\int_{a}^{b} f$ directamente, sino que tengo que calcular la integral de $\int_{b}^{a} f$ e invertir el signo.
Por ejemplo, para una función constante $f(x) = k$:
$$
\begin{align}
&\int_{a}^{b} f = (b - a)k \\
&\int_{b}^{a} f = -(b - a)k = (a - b)k
\end{align}
$$
De esta forma, del mismo modo que decimos que cuando integramos desde el eje x hacia arriba es positivo, y cuando integramos desde el eje x hacia abajo es negativo, establecemos que cuando integramos de izquierda a derecha es positivo, y cuando integramos de derecha a izquierda es negativo:
- Eje x hacia arriba: Positivo
- Eje x hacia abajo: Negativo
- De izquierda a derecha: Positivo
- De derecha a izquierda: Negativo

La ventaja de esta convención, es que cuando escribimos $\int_{a}^{b}$, no tenemos que preocuparnos por el orden de los puntos (no es necesario que $a < b$).

## Propiedad
Si $f: I \to \mathbb{R}$ es localmente integrable, entonces para todos $a,b,c \in I$ tenemos que
$$
\int_{a}^{c} f = \int_{a}^{b} f + \int_{b}^{c} f
$$
independientemente de las posiciones relativas de $a, b, c$.

A diferencia de la propiedad anterior, aquí no se establece nada sobre el orden de los puntos, ya que como disponemos de una notación extendida, es posible extender la propiedad de aditividad en todos los casos, lo que nos ayudará a la hora de operar, ya que no será necesario chequear el orden de los puntos.

La formula funciona incluso cuando $a = b = c$, puesto que las tres integrales son nulas.

No demostraremos todo esto, pero explicaremos cual es el razonamiento.
### Demostración
Lo principal es distinguir todos los casos posibles, para todas las posiciones posibles entre a, b y c.

Se distinguen 5 casos:
- Caso 1: $a = b = c$: obvio, pues $0 = 0 + 0$.
- Caso 2: $a = b \neq c$
$$
\int_{a}^{c} f = \underbrace{ \int_{a}^{a} f }_{ 0 } + \int_{a}^{c} f = \int_{a}^{b} f + \int_{b}^{c} f
$$
En el segundo paso, a $\int_{a}^{c} f$ le sumamos $\int_{a}^{a} f$ (0) para no modificar su valor. Luego, como $a = b$, hacemos las modificaciones correspondientes.
- Caso 3: $a \neq b = c$: análogo
- Caso 4: $a = c \neq b$
$$
\int_{a}^{c} f = 0 = \int_{a}^{b} f + \int_{b}^{a} f = \int_{a}^{b} f + \int_{b}^{c} f
$$
Sabemos que la suma de opuestos es 0, entonces desarrollamos $\int_{a}^{b} f + \int_{b}^{a} f$, que son valores opuestos como habíamos establecido anteriormente (uno va de izquierda a derecha y el otro al revés).
- Caso 5: $a, b, c$ son distintos a pares
Es el caso más interesante, pues hay que ver el orden entre los puntos. En total hay 6 casos posibles (permutaciones entre 3 elementos, factorial de 3).

Se distinguen 6 subcasos:
	- Subcaso 5.1: $a < b < c$: obvio (caso común, que ya verificamos anteriormente)
	- Subcaso 5.2: $a < c < b$
$$
\begin{align}
&\int_{a}^{b} f = \int_{a}^{c} f + \int_{c}^{b} f \\
&\int_{a}^{c} f = \int_{a}^{b} f - \int_{c}^{b} f = \int_{a}^{b} f + \int_{b}^{c} f
\end{align}
$$
	- Subcaso 5.3: $b < a < c$
	- Subcaso 5.4: $b < c < a$
	- Subcaso 5.5: $c < a < b$
	- Subcaso 5.6: $c < b < a$

Hay que verificar en todos los casos (sin ser el primero que ya fue verificado) usando la definición extendida. Únicamente demostramos el subcaso 5.2, el resto de casos son análogos.

La idea es siempre llegar a $\int_{a}^{b} f + \int_{b}^{c} f$.

En definitiva, logramos demostrar que, cuando queremos calcular la integral de una función en un intervalo dado, es posible intercambiar el punto de inicio y fin del intervalo correspondiente, invirtiendo el signo de la integral. Esto es equivalente a decir que ==podemos utilizar la notación $\int_{a}^{b} f$ sin preocuparnos por el orden de a y b==.

Sin embargo, ahora tenemos que verificar cuales de las propiedades vistas se extienden y cuales no, considerando esta nueva notación.
A continuación repasaremos dichas propiedades:

**Monotonía**
$$
f \leq g \implies \int_{a}^{b} f \leq \int_{a}^{b} g \qquad \text{solo si } a \leq b
$$
En el caso en el que $a > b$, hay que intercambiar el orden debido al cambio de signo: $f \leq g \implies \int_{b}^{a} f \geq \int_{b}^{a} g$
Por esta razón, ==la monotonía no se extiende a la nueva definición.==

**Valor absoluto**
$$
|\int_{a}^{b} f| \leq \int_{a}^{b} |f| \qquad \text{solo si } a \leq b
$$
Si $a > b$, entonces $\int_{a}^{b} |f|$ será negativo, pues su signo cambia. No ocurre lo mismo para $|\int_{a}^{b} f|$, ya que se aplica el valor absoluto y es positivo. En este caso, se invierte la desigualdad: $|\int_{a}^{b} f| \geq \int_{a}^{b} |f|$
Por esta razón, ==el valor absoluto no se extiende a la nueva definición==.

**Linealidad**
Se extiende a $a,b,c$ cualesquiera.

**Aditividad respecto al intervalo**
Se extiende a $a,b,c$ cualesquiera.

De esta forma, solo nos preocupamos por el orden cuando trabajamos con la monotonía o el valor absoluto en integrales.

Es fundamental siempre considerar las intuiciones geométricas que van a impedir que nos equivoquemos. Por esto, no podemos depender únicamente de los símbolos.

A continuación, analizaremos otras propiedades geométricas con respecto a las integrales. Por ejemplo:
- Aditividad: consiste en sumar dos funciones, lo que también suma las áreas.
- Homogeneidad: consiste en multiplicar una función por un factor, y esto multiplica naturalmente la integral.
Todas estas son propiedades verticales.

Sin embargo, a continuación estudiaremos propiedades horizontales.

# Otras propiedades algebraicas
## 1 - Invariancia por traslación
Sea $f : [a,b] \to I$. Dado $\mu \in \mathbb{R}$, se considera $g : [a + \mu, b + \mu] \to \mathbb{R}$ definida por:
$$
g(y) = f(y - \mu) \qquad (\forall y \in [a + \mu, b + \mu])
$$
Si $y \in [a + \mu, b + \mu] \implies (y - \mu) \in [a, b]$
![[Invariancia por traslación.png]]
Algo a tener en cuenta es que para hacer una traslación según un vector $\mu$ de la gráfica, en la definición de la función hay que poner una resta, ya que para calcular $g(y)$, hay que tomar el punto $y - \mu$ y hacer $f(y - \mu)$.
Desplacé según la constante $\mu$, aunque está claro que la gráfica es la misma.

Además, podemos decir que si f es integrable, entonces g también es integrable, y la integral de f es igual a la integral de g.

### Proposición
Si f es integrable en $[a,b]$, entonces g es integrable en $[a + \mu, b + \mu]$, y
$$
\int_{a + \mu}^{b + \mu} g(y) dy \left(= \int_{a + \mu}^{b + \mu} f(y - \mu) dy \right) \underbrace{ = }_{ \text{Proposición} } \int_{a}^{b} f(x) dx
$$
Aquí decimos que es un caso particular de cambio de variable.
Esta es la propiedad de ==integración por traslación==. Es muy útil, pues si tenemos una función periódica, integramos el período y lo desplazamos.

No demostraremos nada, continuamos con la segunda propiedad.

## 2 - Integración en espejo
Sea $f: [a, b] \to \mathbb{R}$. Se define $g: [-b, -a] \to \mathbb{R}$ por
$$
g(y) := f(-y) \qquad (\forall y \in [-b, -a])
$$
![[Integración en espejo.png]]
Aquí, para determinar un valor $g(y)$, tenemos que calcular $f(-y)$.

La proposición establece que si una función es integrable, entonces lo mismo ocurre para la otra, además de que sus integrales son iguales.

### Proposición
Si f es integrable en $[a,b]$, entonces g es integrable en $[-b, -a]$, y
$$
\begin{align}
&\int_{-b}^{-a} g(y) dy \left(= \int_{-b}^{-a} f(-y) dy \right) \underbrace{ = }_{ \text{Proposición} } \int_{a}^{b} f(x) dx \\
&\implies \int_{-a}^{-b} g = -\int_{a}^{b} f
\end{align}
$$
Como podemos ver, hay dos formulaciones:
1. La formulación geométrica establece que si $a < b \implies -b < -a$, y las áreas no cambian (si mantengo ese orden de extremos al calcular las integrales).
2. La formulación algebraica, pone los extremos al revés, pero agregando un menos del otro lado (puesto que, como sabemos, si recorremos de derecha a izquierda, obtenemos el valor opuesto).

La segunda se deduce de la primera usando la convención de intercambio de cotas. Al intercambiar las cotas de la integral de g, se invierte su valor, por lo que hay que agregar un menos del otro lado (se cambia el signo de ambos lados).

Por construcción, g es la función simétrica de f respecto al eje y, esta es la definición de g. Estamos comparando dos funciones distintas.
Esta operación siempre se puede hacer, y según el orden en el que ponga los extremos en la integral, obtendré la misma integral (caso 1), o la opuesta (caso 2).

Se llama integración en espejo: si se integrar una función, entonces puedo hacer la transformación en espejo y también podré integrar la otra función, y obtendré la misma integral o la opuesta según el orden en el que ponga los extremos.
La segunda expresión se obtiene al aplicar el teorema de cambio de variable.

## 3 - Integración y dilatación
Sea $f: [a,b] \to \mathbb{R}$. Dado $\lambda \neq 0$ (factor de dilatación), se considera la función $g: \begin{cases} [\lambda a, \lambda b] \to \mathbb{R} \text{ si } \lambda > 0 \\ [\lambda b, \lambda a] \to \mathbb{R} \text{ si } \lambda < 0 \end{cases}$ definida por
$$
g(y) = f\left( \frac{y}{\lambda} \right) \qquad \left( \forall y \in \begin{cases} [\lambda a, \lambda b] \to \mathbb{R} \text{ si } \lambda > 0 \\ [\lambda b, \lambda a] \to \mathbb{R} \text{ si } \lambda < 0 \end{cases} \right)
$$
![[Integración y dilatación.png]]
Aquí, para determinar $g(y)$, hay que calcular $f\left( \frac{y}{\lambda} \right)$.

### Proposición
Si f es integrable en $[a,b] \implies$ g es integrable en $[\lambda a, \lambda b]$, y
$$
\begin{align}
&\int_{\lambda a}^{\lambda b} g(y) dy \left(= \int_{\lambda a}^{\lambda b} f\left( \frac{y}{\lambda} \right) dy \right) \underbrace{ = }_{ \text{Proposición} } \lambda \cdot \int_{a}^{b} f(x) dx \\
&\implies \int_{\lambda a}^{\lambda b} g = - \int_{\lambda b}^{\lambda a} g = -\lambda \cdot \int_{a}^{b} f \implies \int_{\lambda b}^{\lambda a} g = \lambda \cdot \int_{a}^{b} f \qquad ( \text{si } \lambda < 0)
\end{align}
$$
Estas son las operaciones tradicionales que se pueden hacer sobre una función, afectándola horizontalmente:
1. Traslación
2. Simetría respecto al eje y
3. Dilatación

También podemos trabajar con operaciones compuestas, por ejemplo combinar la traslación y la dilatación, pasando por ejemplo de $[a, b]$ a $[\lambda a + \mu, \lambda b + \mu]$.

Es importante memorizar estos tres casos particulares, ya que son fundamentales y se pueden usar sin hacer cambio de variable. Al ser geométricos, son fácilmente analizables mediante sus gráficas.

A continuación, veremos tres tipos de ejemplos de funciones integrables, siendo:
1. Funciones escalonadas
2. Polinomios
3. $\frac{1}{x}$
Al finalizar, sabremos integrar todos estos casos.

# Funciones escalonadas
**Definición**
Una función $f: [a,b] \to \mathbb{R}$ es escalonada (tiene escalones, es constante por trozos) si existe una partición $P= \{ a_{0}, a_{1}, \dots, a_{n} \} \subset [a, b]$ tal que f es constante en cada subintervalo $\underbrace{ (a_{i}, a_{i + 1}) }_{ abierto }$ (especificamos un intervalo abierto, ya que en los extremos -puntos de la partición- puede pasar cualquier cosa).
![[Funciones escalonadas.png]]

## Proposición
Toda función escalonada $f : [a,b] \to \mathbb{R}$ es integrable, y:
$$
\int_{a}^{b} f = \sum_{i = 0}^{n-1} (a_{i + 1} - a_{i})k_{i}
$$
donde $a_{0}, a_{1}, \dots, a_{n}$ son los puntos de la partición P
y $k_{0}, \dots , k_{n-1}$ son los valores tomados en los subintervalos $(a_{0}, a_{1}), \dots, (a_{n-1}, a_{n})$.

Lo importante es entender que usamos intervalos abiertos, pues no sabemos que sucede en los extremos. Sin embargo, respecto a la integración, los valores tomados en los extremos no cuentan, no tienen relevancia ni afectan el calculo de la integral de la función.

No lo vamos a demostrar ya que es muy aburrida. La idea es integrar en cada trozo y utilizar la aditividad respecto al intervalo. La trampa aquí es que la función no es exactamente constante en los subintervalos, pues hay que tratar el problema (o la anomalía) de lo que pasa al comienzo y al final.

En definitiva, cuando tengo que calcular la integral de una función escalonada, el problema se reduce a una sumatoria finita: calcular las cosas en cada escalón y sumar todo.
Es una buena forma de definir integral, puesto que tiene la buena forma y es fácil de comprender. De hecho, Apostol utiliza esta definición

A continuación, un ejercicio que consiste en observar lo siguiente:

**Ejercicio**
Sea $f : [a, b] \to \mathbb{R}$ acotada:
$$
\begin{align}
&I_{*}(f) = sup \left\{ \int_{a}^{b} s : s \text{ escalonada y } s \leq f \right\} \\
&I^{*}(f) = ínf \left\{ \int_{a}^{b} t : t \text{ escalonada y } f \leq t \right\}
\end{align}
$$
Consideramos el conjunto de todas las integrales de las funciones escalonadas menores o iguales a f, de forma que todas las integrales son menores o iguales a la integral de f. Esto quiere decir que tengo un conjunto de aproximaciones por defecto a f (conjunto de cosas menores o iguales a f). Esto implica que si yo tomo el supremo de dicho conjunto, obtengo exactamente la integral inferior de f.

Ídem para la integral superior. Consideramos el conjunto de todas las integrales de las funciones escalonadas mayores o iguales a f, tal que todas las integrales son mayores o iguales a la integral de f. Esto establece que tengo un conjunto de aproximaciones por exceso a f. En conclusión, si tomo el ínfimo de dicho conjunto, obtengo exactamente la integral superior de f.

De esta forma, tenemos una nueva definición de integral en dos etapas.

Primera definición:
Se define la integral para las funciones escalonadas usando la siguiente fórmula como definición:
$$
\int_{a}^{b} f = \sum_{i = 0}^{n-1} (a_{i + 1} - a_{i})k_{i}
$$Es decir, en el caso particular en el que tengo una función escalonada es muy sencillo, pues puedo calcular directamente su integral por suma finita (aplicando la fórmula anterior).

A partir de esto, establecemos que podemos definir:
- Integral inferior de una función: supremo del conjunto de integrales de funciones escalonadas que son menores o iguales a dicha función
- Integral superior de una función: ínfimo del conjunto de integrales de funciones escalonadas que son mayores o iguales a dicha función
Decimos que la función es integrable cuando ambos números son iguales.

La anterior es la función de Apóstol, y corresponde con la definición de Riemann.

Otro detalle importante de las funciones escalonadas:
Hay un caso particular de funciones escalonadas, que son las funciones nulas, salvo en una cantidad finita de puntos. Esto implica que puedo cambiar una cantidad finita de puntos sin cambiar el caracter integrable ni el valor de la integral.

## Proposición
Sean $f, g : [a, b] \to \mathbb{R}$ tales que $f = g$, salvo en un número finito de puntos.
Entonces f es integrable si y sólo si g lo es, y tienen misma integral.
Ejemplo:
![[Funciones escalonadas, segunda proposición.png|697]]

Esto se demuestra considerando la diferencia entre ambas funciones.
### Demostración
Sea $s := g - f$
Tenemos que $s = 0$, salvo en un número finito de puntos $a_{0}, a_{1}, \dots, a_{n}$
$$
\implies s \text{ es escalonada, y } \int_{a}^{b} s = 0
$$
Luego, si f es integrable
$$
\implies f + s = g \text{ es integrable (y tiene la misma integral)}
$$
En conclusión, si yo tengo una función integrable, y cambio una cantidad finita de puntos en la misma, la nueva función sigue siendo integrable, y sus integrales son iguales.
Esto dictamina que la integral es una propiedad global, no esta dada por ningún punto particular.
De esta forma, la integral no es determinada por $f(x), \forall x \in \mathbb{R}$. Esto parece no tener sentido, pero recordemos que se especifica que únicamente se puede cambiar una cantidad finita de puntos, por lo que estamos hablando de una cantidad finita de $f(x)$ (no cambia la forma global de la función).

# Integral de polinomios
Hasta ahora, vimos la parábola y las funciones constantes, pero aún nos quedan funciones más interesantes por ver.

## Propiedad
Dado $p \in \mathbb{R}$, la función $x \longmapsto x^{p}$ es integrable en cualquier intervalo $[a, b] \subset \mathbb{R}$ y
$$
\int_{a}^{b} x^{p} dx = \frac{b^{p + 1} - a^{p + 1}}{p + 1}
$$
Es equivalente a decir que es localmente integrable.
La formula anterior siempre está bien definida, siempre funciona. Además, no depende del orden entre a y b, funcionando también si se intercambian.

$x \longmapsto x^{p}$: notación lambda definición rápida de la función $f(x) = x^{p}$, la ventaja de usar $x \longmapsto x^{p}$ es que es una función anónima, no doy un nombre como f, g, h, etc. Tampoco está atada a una letra en particular.

Vimos que la integral es una función lineal, podemos hacer combinaciones de funciones integrables y obtengo nuevas funciones integrables.
Si tomo varias funciones potencia ($x^{2}, x^{3}, x^{10}, x^{42}$) y hago una combinación lineal cualquiera de estas, formo un polinomio.

Es claro que si puedo integrar todas estas funciones por combinaciones lineales, voy a poder integrar todos los polinomios, de modo que será la formula que, en la próxima clase, utilizaremos para descifrar como calcular la integral de cualquier polinomio.