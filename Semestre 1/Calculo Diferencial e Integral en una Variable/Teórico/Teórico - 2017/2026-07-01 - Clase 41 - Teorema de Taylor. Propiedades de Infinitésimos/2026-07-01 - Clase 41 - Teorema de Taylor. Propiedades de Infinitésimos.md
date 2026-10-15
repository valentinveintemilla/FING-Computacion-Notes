# Polinomios de Taylor
La clase pasada, abordamos el concepto de polinomio de Taylor:

> [!Recordatorio]
> Dada una función $f$, $n$ veces derivable en $x = a$, podemos definir su polinomio de Taylor:
> $$
> \begin{align}
> P_{n}(f, a)(x) &= f(a) + f'(a)(x - a) + \dots + \frac{f^{(n)}(a)(x - a)^{n}}{n!} \\
> &= \sum_{k = 0}^{n} \frac{f^{(k)}(a) (x - a)^{k}}{k!}
> \end{align}
> $$

También definimos un caso particular del polinomio de Taylor: Polinomio de Mc-Laurin.

Si $a = 0$, entonces lo denominamos polinomio de Mc-Laurin.

Abordamos varios ejemplos:
$$
\begin{align}
&P_{n}(e^{x}, 0) = 1 + x + \frac{x^{2}}{2!} + \dots + \frac{x^{n}}{n!} \\
&P_{2n + 1}(\sin(x), 0) = x - \frac{x^{3}}{3!} + \frac{x^{5}}{5!} - \frac{x^{7}}{7!} + \dots + \frac{(-1)^{n} x^{2n + 1}}{(2n + 1)!} \\
&P_{n}(\log(x), 0) = x - \frac{x^{2}}{2!} + \frac{x^{3}}{3} - \frac{x^{4}}{4} + \dots + \frac{(-1)^{n - 1} x^{n}}{n}
\end{align}
$$

También vimos que el polinomio de Taylor de una combinación de funciones es la combinación de los polinomios de Taylor de las funciones mencionadas:
$$
P_{1}(f, a)(x) = f(a) + f'(a)(x - a)
$$
Vimos que la diferencia entre el polinomio anterior y la función $f$ tiende a 0 cuando $x \to a$, ya que son cada vez más similares. Lo expresamos en función del resto (diferencia entre el polinomio de Taylor y la función):
$$
f(x) = P_{1}(f, a)(x) + r_{1}(x)
$$
donde
$$
\frac{r_{1}(x)}{x - a} \underset{x \to a} \longrightarrow 0
$$

Queríamos determinar que sucedía si consideramos un polinomio de Taylor de mayor orden, ¿El resto tenderá a 0 más rápido? Es lo que veremos con el teorema de Taylor:

## Teorema de Taylor

#Teorema 
> [!Teorema de Taylor]
> Sea $f$ una función derivable hasta el orden $n$ en $x = a$.
> 
> Entonces existe un único polinomio $P_{n}(f, a)$ de grado $n$ en $(x - a)$, tal que
> $$
> f(x) = P_{n}(f, a)(x) + r_{n}(x)
> $$
> donde $\lim_{ x \to a } \frac{r_{n}}{(x - a)^{n}} = 0$.
> 
> Además,
> $$
> P_{n}(f, a)(x) = \sum_{k = 0}^{n} \frac{f^{(k)}(a) (x - a)}{n!}
> $$

De esta forma, cuando mayor es el grado del polinomio de Taylor, menor es el resto (diferencia con la función, imprecisión).

Para demostrar el teorema, comenzaremos demostrando la unicidad:

### Demostración

#### Unicidad
Comenzaremos suponiendo que existen dos polinomios con dichas características asociados a la misma función.

Supongamos que existen
$$
\begin{align}
&P(x) = a_{0} + a_{1}(x - a) + a_{2}(x - a)^{2} + \dots + a_{n}(x - a)^{n} \\
&Q(x) = b_{0} + b_{1}(x - a) + b_{2}(x - a)^{2} + \dots + b_{n}(x - a)^{n}
\end{align}
$$
tales que:
$$
\begin{align}
&f(x) = P(x) + r(x) \\
&f(x) = Q(x) + R(x)
\end{align}
$$
donde
$$
\begin{align}
&\lim_{ x \to a } \frac{r(x)}{(x - a)^{n}} = 0 \\
&\lim_{ x \to a } \frac{R(x)}{(x - a)^{n}} = 0
\end{align}
$$

Queremos probar que ambos son iguales.

En caso de trabajar con funciones cualesquiera, tendríamos que demostrar que para cada elemento del dominio, la imagen es exactamente la misma. Sin embargo, como son polinomios, basta con probar que tienen los mismos coeficientes en los mismos monomios ($a_{0} = b_{0}, a_{1} = b_{1}, \dots$).

Entonces:
$$
\begin{align}
&a_{0} + a_{1}(x - a) + a_{2}(x - a)^{2} + \dots + a_{n}(x - a)^{n} + r(x) \\
&b_{0} + b_{1}(x - a) + b_{2}(x - a)^{2} + \dots + b_{n}(x - a)^{n} + R(x)
\end{align} = f(x)
$$
$$
\lim_{ x \to a } a_{0} + a_{1}(x - a) + a_{2}(x - a)^{2} + \dots + a_{n}(x - a)^{n} + r(x) = a_{0} + \underbrace{ \lim_{ x \to a } r(x) }_{ = 0 } = a_{0} = f(a)
$$
$$
\lim_{ x \to a } b_{0} + b_{1}(x - a) + b_{2}(x - a)^{2} + \dots + b_{n}(x - a)^{n} + R(x) = b_{0} + \underbrace{ \lim_{ x \to a } R(x) }_{ = 0 } = a_{0} = f(a)
$$
$$
\implies a_{0} = b_{0}
$$
Entonces, determinamos que estos polinomios tienen que compartir al menos el término independiente.

Como $a_{0} = b_{0}$, continuamos analizando el resto de la expresión
$$
a_{1}(x - a) + a_{2}(x - a)^{2} + \dots + a_{n}(x - a)^{n} + r(x) = b_{1}(x - a) + b_{2}(x - a)^{2} + \dots + b_{n}(x - a)^{n} + R(x)
$$

Ahora, dividiremos entre $(x - a)$ y tomamos $\lim_{ x \to a }$:
$$
a_{1} + a_{2}(x - a) + \dots + a_{n}(x - a)^{n - 1} + \frac{r(x)}{x - a} = b_{1} + b_{2}(x - a) + \dots + b_{n}(x - a)^{n - 1} + \frac{R(x)}{x - a}
$$

Analizamos el límite nuevamente:
$$
\lim_{ x \to a } a_{1} + a_{2}(x - a) + \dots + a_{n}(x - a)^{n - 1} + \frac{r(x)}{x - a} = a_{1} + \underbrace{ \lim_{ x \to a } \frac{r(x)}{x - a} }_{ = 0 } = a_{1}
$$
$$
\lim_{ x \to a } b_{1} + b_{2}(x - a) + \dots + b_{n}(x - a)^{n - 1} + \frac{R(x)}{x - a} = b_{1} + \underbrace{ \lim_{ x \to a } \frac{R(x)}{x - a} }_{ = 0 } = b_{1}
$$
$$
\implies a_{1} = b_{1}
$$

Entonces, además de compartir el término independiente, también tienen que compartir los coeficientes del monomio de grado 1.

Ahora, volvemos a realizar el mismo proceso:
$$
a_{2}(x - a) + \dots + a_{n}(x - a)^{n - 1} + \frac{r(x)}{x - a} = b_{2}(x - a) + \dots + b_{n}(x - a)^{n - 1} + \frac{R(x)}{x - a}
$$
Dividimos entre $x - a$:
$$
\implies a_{2} + \dots + a_{n}(x - a)^{n - 2} + \frac{r(x)}{(x - a)^{2}} = b_{2} + \dots + b_{n}(x - a)^{n - 2} + \frac{R(x)}{(x - a)^{2}}
$$

Si seguimos así (tomando el límite de cada lado cuando $x \to a$), hallaremos que $a_{2} = b_{2}$. Iterando, llegaremos a que $a_{n} = b_{n}$, confirmando que $P(x) = Q(x)$.

De esta forma, solo existe un polinomio con dichas características para una función determinada (ya que si consideramos otro, todos los coeficientes coinciden).

Ahora, nos queda probar la existencia: ya sabemos que si existe es único, ahora nos falta demostrar que el candidato cumple con las hipótesis establecidas.

#### Existencia
Veremos que el polinomio de Taylor
$$
P_{n}(f, a)(x) = \sum_{k = 0}^{n} \frac{f^{(k)}(a) (x - a)}{n!}
$$
cumple que $f(x) - P_{n}(f, a)(x) = r_{n}(x)$,
$$
\lim_{ x \to a } \frac{r_{n}(x)}{(x - a)^{n}} = 0 
$$

Entonces tenemos que probar que la diferencia entre la función y su polinomio de Taylor (el resto) tiende a 0 más deprisa que $(x - a)^{n}$.

Lo haremos por inducción. Ya sabemos que sucede para $n = 1$, que es el caso base. Así que lo haremos para $n$.

$n = 1$ (Paso Base): $P_{1}(f, a)(x) = f(a) + f'(a)(x - a)$

Ya vimos que si
$$
r_{1}(x) = f(x) - P_{1}(f, a)(x) \implies \lim_{ x \to a } \frac{r_{1}(x)}{x - a} = 0
$$

Ahora, pasamos a demostrar el caso general:
**Hipótesis**: Sea $g$ $(n - 1)$ veces derivable en $x = a$, $P_{n - 1}(g, a)(x) = \sum_{k = 0}^{n - 1} \frac{g^{(k)}(a) (x - a)^{k}}{k}$
$$
\implies g(x) = P_{n}(g, a)(x) + r_{n - 1}(x)
$$
donde
$$
\lim_{ x \to a } \frac{r_{n}}{(x - a)^{n - 1}} = 0
$$

**Tesis**
$f$ $n$ veces derivable
$$
f(x) = P_{n}(f, a)(x) + r_{n}(x)
$$
donde
$$
\lim_{ x \to a } \frac{r_{n}(x)}{(x - a)^{n}} = 0 
$$
El candidato a utilizar será el polinomio de Taylor:
$$
P_{n}(f, a)(x) = \sum_{k = 0}^{n} \frac{f^{(k)}(a) (x - a)^{k}}{k!}
$$

Simplemente, tenemos que demostrar que el límite efectivamente tiende a 0:
Basta con demostrar que
$$
r_{n}(x) = f(x) - \left[ f(a) + f'(a)(x - a) + \dots + \frac{f^{(n)}(a)(x - a)^{n}}{n!} \right] \implies \lim_{ x \to a } \frac{r_{n}(x)}{(x - a)^{n}} = 0 
$$

Queremos hacer aparecer $(x - a)^{n - 1}$, para lo que utilizaremos la derivada, ya que para indeterminaciones de tipo $\frac{0}{0}$ utilizamos L'Hôpital:

Por L'Hôpital:
$$
\lim_{ x \to a } \frac{r_{n}(x)}{(x - a)^{n}} = \lim_{ x \to a } \frac{r'_{n}(x)}{n(x - a)^{n - 1}} = \frac{1}{n} \lim_{ x \to a } \frac{r'_{n}(x)}{(x - a)^{n - 1}}
$$
De esta manera, probaremos que $\lim_{ x \to a } \frac{r_{n}(x)}{(x - a)^{n}} = 0$, lo que afirma la existencia de dicho polinomio.

Calculamos la derivada:
$$
\begin{align}
&r_{n}(x) = f(x) - \left[ f(a) + f'(a)(x - a) + \frac{f''(a)(x - a)^{2}}{2!} + \dots + \frac{f^{(n)}(a)(x - a)^{n}}{n!} \right] \\
&r'_{n}(x) = f'(x) - \left[ f'(a) + f''(a)(x - a) + \frac{f'''(a)(x - a)^{2}}{2!} + \frac{f^{(4)}(a)(x - a)^{3}}{3!} + \dots + \frac{f^{(n)}(a)(x - a)^{n - 1}}{(n - 1)!} \right]
\end{align}
$$

Como vemos, esto coincide con el Taylor de orden $n - 1$ de la función $f'$, ya que el término independiente coincide con la derivada de $f$ en $a$, y si analizamos el resto de los términos, podemos ver que todos fueron derivados.

Entonces:
$$
\begin{align}
r'_{n}(x) &= f'(x) - P_{n - 1}(f', a)(x) \\
&= r_{n - 1}(x)
\end{align}
$$
De esta forma:
$$
\lim_{ x \to a } \frac{r'_{n}(x)}{(x - a)^{n - 1}} = 0 
$$

Y como verificamos que este cociente tiende a 0, también verificamos que $\lim_{ x \to a } \frac{r_{n}(x)}{(x - a)^{n}} = 0$, ya que lo realizamos por L'Hôpital derivando ambas partes. Entonces, existe un único polinomio con las características mencionadas, y además es el que habíamos llamado polinomio de Taylor.

Con esto finaliza la demostración.

Este teorema es sumamente útil, pudiendo aplicarlo para resolver múltiples problemas. Pasaremos a analizar algunas consecuencias:

### Consecuencia
Vimos que el polinomio de Taylor de una suma es la suma de los polinomios de Taylor, y el producto de Taylor de una función por un escalar es el escalar por el polinomio de Taylor de dicha función. Esto significa que el polinomio de Taylor es estable por combinación lineal.

Sin embargo, no siempre utilizamos simplemente números, también podríamos considerar el producto de dos funciónes (las cuales son $n$ veces derivables). El problema es que la derivada del producto de dos funciones $(f(x) \cdot g(x))' = f'(x)g(x) + f(x)g'(x)$. Esto puede complicar sumamente la determinación del polinomio de Taylor.

Afortunadamente, existe un atajo consecuencia del teorema de Taylor:

Supongamos que $f(x), g(x)$ ambas funciones derivables la cantidad de veces que haga falta.
$$
\begin{align}
&f(x) = P_{n}(f, a)(x) + r_{n}(x) \\
&g(x) = P_{n}(g, a)(x) + R_{n}(x)
\end{align}
$$
donde
$$
\begin{align}
&\lim_{ x \to a } \frac{r_{n}}{(x - a)^{n}} = 0 \\
&\lim_{ x \to a } \frac{R_{n}}{(x - a)^{n}} = 0
\end{align}
$$

Veremos que si multiplicamos los dos polinomios y nos quedamos con los términos de grado menor o igual a $n$, ese será el polinomio de Taylor.

Lo haremos viendo que el resto de dicho producto tenderá a 0 más rápido que $(x - a)^{n}$.

Desarrollamos el producto:
$$
f(x)g(x) = P_{n}(f, a)(x) \cdot P_{n}(g, a)(x) + P_{n}(f, a)(x) \cdot R_{n}(x) + P_{n}(g, a)(x) \cdot r_{n}(x) + r_{n}(x) \cdot R_{n}(x)
$$

Definimos dos polinomios (simplemente para no tener que estar escribiendo términos continuamente):
$$
\begin{align}
&P(x) = \text{ parte de } P_{n}(f) \cdot P_{n}(g) \text{ de grado } \leq n \\
&H(x) = \text{ parte de } P_{n}(f) \cdot P_{n}(g) \text{ de grado } > n
\end{align}
$$
$$
\implies f(x)g(x) = P(x) + H(x) + P_{n}(f, a)(x) \cdot R_{n}(x) + P_{n}(g, a)(x) \cdot r_{n}(x) + r_{n}(x) \cdot R_{n}(x)
$$

Ahora es cuando invocamos al teorema.

Queremos demostrar que todo el resto (sin ser $P(x)$) tiende a 0, o sea, equivale al resto. Entonces, estudiaremos el límite:
$$
\lim_{ x \to a } \frac{H(x)}{(x - a)^{n}} + P_{n}(f, a)(x) \cdot \frac{R_{n}(x)}{(x - a)^{n}} + P_{n}(g, a)(x) \cdot \frac{r_{n}(x)}{(x - a)^{n}} + r_{n}(x) \cdot \frac{R_{n}(x)}{(x - a)^{n}}
$$
$H(x)$ tiene términos todos de grado mayor e igual a $n + 1$. Entonces, al dividirlo por dicho término tiende a 0.

Luego, como $P_{n}(f)(x)$ es constante (tiende a $f(a)$) y el cociente con el resto tiende a 0 (por definición), todo el término tiende a 0.

Lo mismo aplica para el tercer término.

El cuarto término tiende a 0 por definición.

Entonces, al multiplicar los Taylor de $f$ y $g$ y quedarnos únicamente con los términos de grado menor o igual a 1, obtenemos el polinomio de Taylor del producto de ambas funciones.

Otro ejemplo de obtención del polinomio de Taylor de forma sencilla:

Consideremos la siguiente función:
$$
f(x) = \frac{1}{1 - x}
$$

Queremos obtener el polinomio de Mc-Laurin de dicha función. Podríamos calcular cada una de las derivadas, pero podemos tomar ventaja de la siguiente igualdad como camino más rápido:
$$
\frac{1}{1 - x} = \underbrace{ 1 + x + x^{2} + \dots + x^{n} }_{ P_{n}(x) } + \frac{x^{n + 1}}{1 - x}
$$
Para estar seguros de que $P_{n}(x)$ es el polinomio de Mc-Laurin de orden $n$ de la función, tenemos que comprobar que $\frac{x^{n + 1}}{1 - x}$ se comporta como $r_{n}(x)$:
$$
\lim_{ x \to 0 } \frac{x^{n + 1}}{(1 - x) x^{n}} = \lim_{ x \to 0 } \frac{x}{1 - x} = 0
$$
Entonces, el término extra se comporta como lo haría $\frac{x^{n + 1}}{1 - x}$, entonces, podemos confirmar que el resto de la expresión se comporta como el polinomio de Mc-Laurin de la función $\frac{1}{1 - x}$. De esta manera, este tipo de igualdades permiten facilitar el hallazgo del polinomio de Taylor para una función dada.

Por si acaso, demostraremos la expresión:
$$
S_{n}(x) = 1 + x + x^{2} + x^{3} + \dots + x^{n - 1} + x^{n}
$$
Si multiplicamos por $(1 - x)$:
$$
\begin{align}
(1 - x) \cdot S_{n}(x) &= 1 + \cancel{ x } + \cancel{ x^{2} } + \cancel{ x^{3} } + \cancel{ \dots } + \cancel{ x^{n - 1} } + \cancel{ x^{n} } - \cancel{ x } - \cancel{ x^{2} } - \cancel{ x^{3} } - \cancel{ \dots } - \cancel{ x^{n} } - x^{n + 1} \\
(1 - x) \cdot S_{n}(x) &= 1 - x^{n + 1} \\
S_{n}(x) &= \frac{1 - x^{n + 1}}{1 - x} \\
1 + x + x^{2} + x^{3} + \dots + x^{n - 1} + x^{n} &= \frac{1 - x^{n + 1}}{1 - x} = \frac{1}{1 - x} - \frac{x^{n + 1}}{1 - x} \\
1 + x + x^{2} + x^{3} + \dots + x^{n - 1} + x^{n} + \frac{x^{n + 1}}{1 - x} &= \frac{1}{1 - x}
\end{align}
$$

En conclusión, determinamos que $1 + x + x^{2} + x^{3} + \dots + x^{n - 1} + x^{n} + \frac{x^{n + 1}}{1 - x} = \frac{1}{1 - x}$

Es así que, para casos puntuales, podemos determinar los polinomios de Taylor para funciones dadas considerando igualdades (así como la propiedades probadas con el teorema de Taylor: unicidad y existencia).

Ahora, nos queda ver como se comportan los polinomios de Taylor con una operación más: ¿El Taylor de la función compuesta será el mismo que la composición de los Taylor?

En la composición, la idea será similar a la del producto, quedando el polinomio que nos interesa y otros términos extra, los cuales tienen que tender a 0 para asegurar que, efectivamente, encontramos el polinomio de Taylor.

Para lograr todo esto, tenemos que introducir nueva notación:

### Infinitésimos

#Definición 
> [!Infinitésimo - Definición]
> Sean $f$ y $g$ dos infinitésimos en $x = a$
> $$
> \left (\lim_{ x \to a } f(x) = 0, \lim_{ x \to a } g(x) = 0 \right)
> $$
> Diremos que $f$ es de mayor orden que $g$ ($f = o g$), si y sólo si
> $$
> \lim_{ x \to a } \frac{f(x)}{g(x)} = 0 
> $$

Lo que dice es que ambas funciones tienden a 0, pero $f$ lo hace más rápido. A medida que se acercan a $a$, $f(x)$ se reduce más rápidamente.

Entonces, podemos expresar a $f(x)$ como:
$$
f(x) = P_{n}(f, a)(x) + \overbrace{ o((x - a)^{n}) }^{ r_{n}(x) }
$$

Podemos expresar de manera más compacta la idea de resto (incluyendo todas las características de límite), con la expresión $o((x - a)^{n})$.

Por ejemplo, para que $f(x)$ sea de mayor orden que $g(x)$, podemos considerar $g(x) = (x - a)^{2}$ y $f(x) = (x - a)^{2 + k}, k \in \mathbb{N}^{+}$.

Otros ejemplos:
$x^{2} = o(\sin(x))$ (en $x = 0$) ya que
$$
\lim_{ x \to 0 } \frac{x^{2}}{\sin(x)} = \lim_{ x \to 0 } \overbrace{ x }^{ \to 0 } \overbrace{ \frac{x}{\sin(x)} }^{ \to 1 } = 0
$$
De esta forma, determinamos que $x^{2} = o(\sin(x))$ en $a = 0$. Ambos tienden a 0 cuando $a \to 0$, pero $x^{2}$ lo hace más rápido.

También podemos enunciar una serie de propiedades respecto a los infinitésimos:

#### Propiedades

$f, g$ son infinitésimos cuando $x \to a$

1. $o(g(x)) + o(g(x)) = o(g(x))$
Esto tiene sentido ya que $o(g(x))$ es una familia de funciones:
$$
o(g(x)) = \left\{  f(x) : \lim_{ x \to a } \frac{f(x)}{g(x)} = 0  \right\}
$$
Entonces, si tengo dos funciones que tienden más a prisa que $g(x)$ a 0 (pertenecen a la familia anterior), entonces su suma también pertenecerá a la familia (tenderá más a prisa que $g(x)$ a 0).

Si $f \in o(g), h \in o(g) \implies f + h \in o(g)$
**Demostración**:
$$
\lim_{ x \to a } \frac{(f + h)(x)}{g(x)} = \lim_{ x \to a } \frac{f(x)}{g(x)} + \lim_{ x \to a } \frac{h(x)}{g(x)} = 0 + 0 = 0
$$

ACLARACIÓN: los infinitésimos tienen sentido para un $a$ dado.

2. $o(k g) = o(g)$
De esta forma, cuando tengo un infinitésimo $f$ de orden mayor que $g$ y una constante $k$. Si $f$ tiende a 0 más a prisa que $g$, entonces $kg$ también tiende a 0 más a prisa que $g$ (es un infinitésimo de orden mayor).

**Demostración**:
Sea $f \in o(kg)$, o sea
$$
\lim_{ x \to a } \frac{f(x)}{kg(x)} = 0 = \frac{1}{k} \lim_{ x \to a } \frac{f(x)}{g(x)} \implies \lim_{ x \to a } \frac{f(x)}{g(x)} = 0 \implies f \in o(g) \implies o(kg) \subseteq o(g)
$$

Ahora, probamos la otra inclusión, tomando una función de $o(g)$ y demostrar que también está en $o(kg)$ (o sea, si multiplicamos por una constante, se mantiene la propiedad de infinitésimo):

Sea $h \in o(g)$, o sea
$$
\lim_{ x \to a } \frac{h(x)}{g(x)} = 0 \implies \lim_{ x \to a } \frac{f(x)}{kg(x)} = 0 \implies h \in o(g) \implies o(g) \subseteq o(kg)
$$

3. $o(o(g)) = o(g)$
Si $f \in o(g)$ y $h \in o(o(g))$, lo que quiere decir que $f$ tiende a 0 más de prisa que $g$ y $h$ tiende a 0 más de prisa que $f$, entonces $h$ tiende a 0 más de prisa que $f$. Es una especie de transitividad.

Por ejemplo:
Hipótesis (lo sabemos): $\lim_{ x \to a } \frac{f(x)}{g(x)} = 0$ y $\lim_{ x \to a } \frac{h(x)}{f(x)} = 0$

Tesis: $\lim_{ x \to a } \frac{h(x)}{g(x)} = 0$
$$
\frac{h(x)}{g(x)} = \frac{h(x)}{f(x)} \cdot \frac{f(x)}{g(x)}
$$
(suponiendo que $f$ no se anula en el entorno manejado).

Todas estas propiedades son necesarias para fabricar polinomios de Taylor a partir de otros ya conocidos.

4. $h(x) o(g(x)) = o(g(x))$ si $h$ está acotada en $E(a, \delta)$.
(si $\lim_{ x \to a } \frac{f}{g} = 0 \implies \lim_{ x \to a } \frac{hf}{g} = 0$)

Es similar al caso de producto por una constante.

5. $[o(g(x))]^{n} = o(g^{n}(x))$
Si $f$ tiende a 0 más deprisa que $g$, entonces $f^{n}$ va a tender a 0 más deprisa que $g^{n}$.
$$
\lim_{ x \to a } \frac{f}{g} = 0 \implies \lim_{ x \to a } \frac{f^{n}}{g^{n}} = 0
$$

6. Si $h \sim g$ en $x = a$
$$
\lim_{ x \to a } \frac{h(x)}{g(x)} = 1 \implies o(h) = o(g)
$$
O sea, si dos funciones son equivalentes, y se que $f$ tiende a 0 más deprisa que una de ellas, entonces también tiende a 0 más deprisa que la otra.

Recordemos que si dos funciones son equivalentes en un punto, entonces el límite en ese punto del cociente de ambas tiende a 1.

Estas propiedades serán sumamente útiles para fabricar polinomios de Taylor a partir de otros polinomios dados, como es el caso de la composición de funciones. También veremos distintas aplicaciones para los polinomios de Taylor, como el cálculo de límites, para lo que necesitaremos conocer mejor al resto ($r(x)$), a partir de un teorema que nos permitirá expresarlo como un valor.