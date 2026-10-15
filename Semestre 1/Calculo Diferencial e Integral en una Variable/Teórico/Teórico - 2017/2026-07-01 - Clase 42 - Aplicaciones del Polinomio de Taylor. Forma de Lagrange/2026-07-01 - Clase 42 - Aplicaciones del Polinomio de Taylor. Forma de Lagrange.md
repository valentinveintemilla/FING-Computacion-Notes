# Polinomios de Taylor
Durante esta clase, continuaremos formalizando nuestro conocimiento de los polinomios de Taylor, abordando la composicion de funciones, y algunas aplicaciones clasicas, como:
- cálculo de límites.
- clasificación de puntos estacionarios.
- cálculo numérico.

Para la última, nos vendrá bien conocer más a fondo el resto del polinomio de Taylor además de saber que tiende a 0 más rápido que $(x - a)^{n}$, a partir de la forma de Lagrange para $r_{n}(x)$.

Comenzaremos abordando lo que faltó la clase pasada a partir de las propiedades enunciadas: composición de funciones.

## Taylor de una función compuesta
Solamente veremos un ejemplo en esta sección

Consideremos el polinomio de Mc-Laurin de la función exponencial:
$$
e^{u} = 1 + u + \frac{u^{2}}{2} + r_{2}(u)
$$
con $r_{2}(u) = o(u^{2})$ ($r_{2}(u)$ tiende a cero más rápido que $u^{2}$).

Ahora, si queremos trabajar con la función:
$$
e^{x^{2}} = 1 + x^{2} + \frac{x^{4}}{2} + r_{2}(x^{2})
$$
Esta es la idea más intuitiva. ¿Es la expresión $P_{4}(e^{x^{2}}, 0) = 1 + x^{2} + \frac{x^{4}}{2}$ correcta?

Para verificarlo, tenemos que probar que $r_{2}(x^{2}) = o(x^{4})$:
$$
\lim_{ x \to 0 } \frac{r^{2}(x^{2})}{x^{4}} = 0 
$$
sabiendo que
$$
\lim_{ x \to 0 } \frac{r^{2}(u)}{u^{2}} = 0 
$$

Quizás sea más fácil analizarlo como:
$$
\lim_{ x \to 0 } \frac{r^{2}(x^{2})}{(x^{2})^{2}} = 0 \underset{u = x^{2}} \Longleftrightarrow \lim_{ x \to 0 } \frac{r^{2}(u)}{u^{2}} = 0
$$

De esta forma, probamos que es correcto.

Hay un teorema que enuncia que si conocemos el polinomio de Taylor de $f$ y el polinomio de Taylor de $g$, podemos desarrollar el Taylor de la composición (cuando la composición es posible).

Podemos ver otro ejemplo, sustituyendo $u$ por $\sin(u)$, en el cual en cada $u$ de la función $e^{u}$ quedará el polinomio de $\sin(u)$ mas un cierto resto y lo mismo elevado al cuadrado. Luego de desarrollar cada término, nos quedamos con la parte polinómica y juntamos el resto en una expresión, la cual tiene que tender a 0 más rápido que $\sin ^{2}(u)$

---
Proseguimos a estudiar uno de los usos más comunes de los polinomios de Taylor: calculo de límites con indeterminaciones de tipo $\frac{0}{0}$.

## Cálculo de límites: levantar indeterminaciones

### Ejemplo
$$
\lim_{ x \to 0 } \frac{x - \sin(x)}{x^{3}} = \frac{0}{0}
$$
Se puede resolver mediante L'Hôpital, sin embargo, en ciertos casos, puede suceder que el cociente derivado sea más complejo que el anterior, y no parezca mejorar.

La idea aquí es que, sabiendo que la función seno la podemos expresar como $\sin(x) = x - \frac{x^{3}}{3!} + o(x^{3})$. Entonces sustituiremos seno por la igualdad:
$$
\begin{align}
\lim_{ x \to 0 } \frac{x - \sin(x)}{x^{3}} &= \lim_{ x \to 0 } \frac{\cancel{ x } - (\cancel{ x } - \frac{x^{3}}{6} + r_{3}(x))}{x^{3}} \\
&= \lim_{ x \to 0 } \frac{\frac{x^{3}}{6} + r_{3}(x)}{x^{3}} \\
&= \lim_{ x \to 0 } \frac{\frac{x^{3}}{6}}{x^{3}} + \frac{r_{3}(x)}{x^{3}} \\
&= \lim_{ x \to 0 } \frac{\frac{x^{3}}{6}}{x^{3}} + \lim_{ x \to 0 } \frac{r_{3}(x)}{x^{3}}
\end{align}
$$

Sabemos determinar $\lim_{ x \to 0 } \frac{\frac{x^{3}}{6}}{x^{3}}$. Además, como $r_{3}(x) = o(x^{3})$, sabemos que el límite $\lim_{ x \to 0 } \frac{r_{3}(x)}{x^{3}}$ tiende a 0, ya que estamos dividiendo un infinitésimo de $x^{3}$ por $x^{3}$, o sea, una función que tiende a cero muy rápido por otra que no lo hace tan rápido. De esta manera:
$$
\lim_{ x \to 0 } \frac{x - \sin(x)}{x^{3}} = \underbrace{ \lim_{ x \to 0 } \frac{\frac{x^{3}}{6}}{x^{3}} }_{ = \frac{1}{6} } + \underbrace{ \lim_{ x \to 0 } \frac{r_{3}(x)}{x^{3}} }_{ = 0 } = \frac{1}{6}
$$

De esta manera, podemos ver que son muy útiles para resolver este tipo de indeterminaciones, modificando la parte que no es un polinomio, y consideramos el orden $n$, estando $n$ relacionado con la naturaleza de la indeterminación. Por ejemplo, en el caso anterior, consideramos $n = 3$ ya que estábamos dividiendo por $x^{3}$. Se puede considerar un orden mayor y el resultado será el mismo, aunque complicamos las operaciones innecesariamente.

ACLARACIÓN: el resto siempre hace referencia al último término del polinomio, por tal razón es cada vez menor a mayor orden.

---
Pasaremos a otro de los usos de los polinomios de Taylor. Para esto, tenemos que recordar los conceptos de máximo y mínimo local (o relativo):

$f$ alcanza un máximo local en $x = a$ si y sólo si, $\forall x \in E(a, \delta)$, se observaba que $f(x) \leq f(a)$. Si pasaba para todos los $x$ del dominio, hablamos de máximo absoluto. En caso contrario, hablamos de máximo local o relativo. Esto es equivalente a decir que $sg(f(x) - f(a)) \leq 0$.

También lo podemos definir para el mínimo:
$f$ alcanza un mínimo local en $x = a$ si y sólo si, $\forall x \in E(a, \delta)$, se observaba que $f(x) \geq f(a)$. Esto es equivalente a decir que $sg(f(x) - f(a)) \geq 0$.

Entonces, $f$ alcanza un máximo local en $x = a$ si y sólo si, en los puntos $x \in E^{*}(a, \delta)$, se cumple que $f(a) > f(x)$. O sea, las imágenes alrededor de $a$ son menores que en $a$. Luego, estudiamos que si $f$ alcanza un máximo o mínimo en $a$, y además la función es derivable en dicho punto, entonces la derivada en dicho punto es 0.

Ahora, abordaremos el contexto en el cual la función es derivable hasta el orden $n$ en $a$. Supongamos que $f'(a) = 0$, entonces es candidato a tener un máximo o un mínimo.

Luego, habían formas de determinar si efectivamente había un extremo en $a$:
- Estudiar el signo de $f'(x)$ en un entorno de $a$.
- Estudiar la derivada segunda, criterio de concavidad. Si $f'(a) = 0$ y $f''(a) > 0$ (concavidad positiva), entonces se trataba de un mínimo local, mientras que si $f'(a) = 0$ y $f''(a) < 0$ (concavidad negativa), entonces se trataba de un máximo local.

Veremos que estos son casos particulares de un teorema más potente relacionado con polinomios de Taylor.

Llamamos puntos críticos o puntos estacionaros a los valores de $a$ para los cuales $f'(a) = 0$.

### Reconocimiento de puntos estacionarios

> [!Reconocimiento de puntos estacionarios]
> Sea $f$ derivable hasta el orden $n$ en $x = a$.
> 
> Supongamos que todas las derivadas se anulan, siendo la primera derivada no nula, la derivada de orden $n$:
> $$
> f'(a) = 0, f''(a) = 0, \dots, f^{(n - 1)}(a) = 0, f^{(n)} \neq 0
> $$
> 
> Aquí tenemos que analizar dos casos:
> 1. Si $n$ es par, $f$ presenta un extremo local (relativo) en $x = a$:
> 	1. Mínimo si $f^{(n)}(a) > 0$
> 	2. Máximo si $f^{(n)}(a) < 0$
> 2. Si $n$ es impar, entonces $f$ presenta un punto de inflexión:
> 	1. Si $f^{(n)}(a) > 0$, entonces $f$ atraviesa el entorno en forma creciente.
> 	2. Si $f^{(n)}(a) < 0$, entonces $f$ atraviesa el entorno en forma decreciente.

De esta forma, el caso de la derivada segunda es el caso particular $n = 2$ en el que la derivada segunda no es nula.

A continuación, demostramos las proposiciones:
$$
f(x) = f(a) + f'(a)(x - a) + \dots + \frac{f^{(n)}(a)}{n!}(x - a)^{n} + r_{n}(x) \qquad (r_{n}(x) = o((x - a)^{n}))
$$
Por hipótesis, todas las derivadas en $a$ son 0, excepto la n-ésima. Por esta razón, todas se anulan, menos la n-ésima:
$$
\begin{align}
f(x) &= f(a) + \frac{f^{(n)}(a)}{n!}(x - a)^{n} + r_{n}(x) \\
f(x) - f(a) &= \frac{f^{(n)}(a)}{n!}(x - a)^{n} + r_{n}(x) \\
f(x) - f(a) &= (x - a)^{n}\left( \frac{f^{(n)}(a)}{n!} + \frac{r_{n}(x)}{(x - a)^{n}} \right)
\end{align}
$$
**Observación**:
$$
sg(f(x) - f(a)) = sg((x - a)^{n}) \cdot sg\left( \frac{f^{(n)}(a)}{n!} + \frac{r_{n}(x)}{(x - a)^{n}} \right)
$$
Supongamos que $n$ es par, entonces, el signo de $f(x) - f(a)$ estará dado por el signo de la suma, ya que $(x - a)^{n}$ será siempre positivo:

- $n$ par: $sg((x - a)^{n}) > 0 \implies sg(f(x) - f(a)) = sg\left( \frac{f^{(n)}(a)}{n!} + \frac{r_{n}(x)}{(x - a)^{n}} \right)$

Además, sabemos que $\frac{r_{n}(x)}{(x - a)^{n}}$ tiende a 0 cuando $x \to a$, entonces el signo será definido por $\frac{f^{(n)}(a)}{n!}$:
Como $\lim_{  x \to a } \frac{f^{(n)}(a)}{n!} + \frac{r_{n}(x)}{(x - a)^{n}} = \frac{f^{(n)}(a)}{n!}$, entonces, si $x$ está suficientemente cerca de $a$:
$$
sg\left( \frac{f^{(n)}(a)}{n!} + \frac{r_{n}(x)}{(x - a)^{n}} \right) = sg\left( \frac{f^{(n)}(a)}{n!} \right) = sg(f^{(n)}(a))
$$
Entonces, cuando $n$ es par: $sg(f(x) - f(a)) = sg(f^{(n)}(a))$ ($\forall x \in E(a, \delta)$, valores muy cercanos a $a$).

De esta manera, si la derivada es positiva, $f(x) - f(a) > 0$, entonces $f(x) > f(a)$, lo que indica la existencia de un mínimo local en $a$. En cambio, si la derivada es negativa, $f(x) - f(a) < 0$, entonces $f(x) < f(a)$, lo que indica la existencia de un máximo local en $a$.

Ahora, analizaremos el caso en el que la primera derivada que no se anula es una derivada de orden impar.

- $n$ impar:
$$
sg(x - a)^{n} \text{ es } - \text{ para } x < a \text{ y } + \text{ para } x > a
$$Ahora, estudiamos el otro factor, sabiendo que el término importante es $\frac{f^{(n)}(a)}{n!}$:
$$
sg\left( \frac{f^{(n)}(a)}{n!} + \frac{r_{n}(x)}{(x - a)^{n}} \right) = sg\left( \frac{f^{(n)}(a)}{n!} \right) = sg(f^{(n)}(a)) \qquad \forall x \in E(a, \delta)
$$
Entonces, ¿Cómo será el signo del producto?
$$
sg(f(x) - f(a)) = sg(x - a)^{n} sg(f^{(n)}(a))
$$

Ahora, estudiamos cada caso:
- $f^{(n)}(a) > 0$
En este caso, $sg(f(x) - f(a)) = sg(x - a)^{n}$, por lo tanto: $sg(f(x) - f(a)) \text{ es } - \text{ para } x < a \text{ y } + \text{ para } x > a$

La función cruza por $x = a$, con tangente horizontal en dicho punto, en forma ascendente (pasa de negativo a positivo, pasa subiendo).

- $f^{(n)}(a) < 0$
En este caso, $sg(f(x) - f(a)) = -sg(x - a)^{n}$ (se invierte el signo), por lo tanto: $sg(f(x) - f(a)) \text{ es } + \text{ para } x < a \text{ y } - \text{ para } x > a$

La función cruza por $x = a$, con tangente horizontal en dicho punto, en forma descendente (pasa de positivo a negativo, pasa bajando).

---
Ahora, abordaremos un concepto fundamental relacionado al resto de un polinomio de Taylor:
### Forma de Lagrange para $r_{n}(x)$

> [!Forma de Lagrange para el resto]
> Sea $f$ derivable hasta el orden $n + 1$ en $E(a, \delta)$, entonces:
> $$
> \forall x \in E(a, \delta), f(x) = f(a) + f'(a)(x - a) + \dots + \frac{f^{(n)}(x - a)^{n}}{n!} + r_{n}(x)
> $$
> donde
> $$
> r_{n}(x) = \frac{f^{(n + 1)}(c_{x})(x - a)^{n + 1}}{(n + 1)!}
> $$

Entonces, podemos expresar el resto como un término más, pero siendo la derivada evaluada en un cierto punto $c_{x}$, del cual se sabe que está en alguna parte entre $a$ y $x$ ($c_{x} \in (a, x) (x > a), c_{x} \in (x, a) (x < a)$).

Entender esta información permite aprovechar más el polinomio de Taylor.

**Ejemplo**: intentaremos calcular el número $e$ con una precisión estipulada de antemano. Queremos obtener los primeros cuatro decimales exactos:

Calcular $e$ con error menor a $10^{-4}$.
$$
e^{x} = 1 + x + \frac{x^{2}}{2!} + \frac{x^{3}}{3!} + \dots + \frac{x^{n}}{n!} + r_{n}(x)
$$
$$
e^{x} = 1 + x + \frac{x^{2}}{2!} + \frac{x^{3}}{3!} + \dots + \frac{x^{n}}{n!} + \frac{e^{c} x^{n + 1}}{(n + 1)!}, 0 < c < x
$$

Ahora, sabiendo que $e = e^{1}$:
$$
e^{1} = 1 + 1 + \frac{1}{2!} + \frac{1}{3!} + \dots + \frac{1}{n!} + \frac{e^{c}}{(n + 1)!}, 0 < c < x
$$

Sabemos que si olvidamos el término resto, la suma acumulada será aproximadamente igual a $e$. La pregunta es, ¿En que momento la suma diferirá de $e$ en una cantidad menor a $10^{-4}$?

**Observación**:
$$
e \simeq 1 + 1 + \frac{1}{2!} + \dots + \frac{1}{n!}, \left|e - \left( 1 + 1 + \frac{1}{2!} + \dots + \frac{1}{n!} \right) \right| = \frac{e^{c}}{(n + 1)!}
$$
Al expresarlo de la forma anterior, podemos considera la siguiente idea:

Buscar el primer natural a partir del cual $\frac{e^{c}}{(x + 1)!} < \frac{1}{10^{4}}$.

Para despejar $n$, tenemos que conocer el valor $c$. Sabemos que $0 < c < 1$. Como la función es creciente: $e^{0} < e^{c} < e < 3$ (como sabemos que es menor que 3, podemos aprovechar dicha información para facilitar la operatoria):
$$
\frac{e^{c}}{(x + 1)!} < \frac{3}{(n + 1)!} < \frac{1}{10^{4}} \implies 30.000 < (n + 1)!
$$
De esta forma, cuando encontremos dicho $n$, sabremos que la diferencia entre $1 + 1 + \frac{1}{2!} + \dots + \frac{1}{n!}$ y $e$, será menor que $\frac{3}{(n + 1)!}$, que a su vez es menor que $10^{-1}$.

Si realizamos las cuentas, podemos determinar que:
$$
n + 1 = 9 \implies n = 8
$$
De esta forma, si desarrollamos el polinomio de Taylor de orden $n$, habremos hallado el número $e$ con los primeros cuatro decimales exactos.
$$
e^{1} = 1 + 1 + \frac{1}{2!} + \frac{1}{3!} + \dots + \frac{1}{8!}
$$
$$
P_{8}(e^{x}, 1) = 1 + 1 + \frac{1}{2} + \frac{1}{6} + \frac{1}{24} + \frac{1}{120} + \frac{1}{720} + \frac{1}{5040} + \frac{1}{40320}
$$

| $n$ | $\sum_{k = 0}^{n} \frac{1}{k!}$ |
| :-: | :-----------------------------: |
|  0  |                1                |
|  1  |                2                |
|  2  |               2.5               |
|  3  |            2.6666...            |
|  4  |           2.708333...           |
|  5  |           2.716667...           |
|  6  |           2.718056...           |
|  7  |           2.718254...           |
|  8  |           2.718279...           |
Si lo verificamos con una calculadora:
$$
e = 2.718282
$$
coincidiendo en los primeros 4 decimales.

La idea de este tipo de problemas es encontrar una cota que no sea demasiado grande (puesto que tendremos que realizar cuentas de más al tomar un $n$ innecesariamente grande), pero lo suficientemente como para asegurar que satisfacemos la precisión requerida. De hecho, las calculadoras utilizan este método, utilizando polinomios muy similares a funciones conocidas.

Ahora, analicemos la siguiente idea:

Establecimos que
$$
e^{x} \simeq 1 + x + \frac{x^{2}}{2!} + \dots + \frac{x^{n}}{n!}
$$
que es el polinomio de Mc-Laurin de $e^{x}$. Sin embargo, consideramos $x = 1$, suponiendo que podemos aproximar mediante el polinomio de Mc-Laurin, el cual imita muy bien a una función siempre y cuando no nos alejemos demasiado de $x = 0$. Entonces, ¿Es válido considerar $x = 1$?

El razonamiento utilizado fue el siguiente:

Hasta ahora, hemos considerado polinomios de Taylor como
$$
f(x) = P_{n}(f, a)(x) + r_{n}(x)
$$

Como hasta ahora, hemos trabajado con un $n$ fijo, la aproximación del polinomio mejora en la medida en la que $x$ tienda a $a$, basados en que
$$
\lim_{ x \to a } r_{n}(x) = 0
$$

Sin embargo, en el ejemplo anterior, $x$ está fijo de antemano, $x = 1$, no podemos modificarlo. Entonces, casi sin que nos dieramos cuenta, sucedio que el hacer que $x$ tienda a $a$ no es la única manera de reducir el valor del resto $r_{n}(x)$, también podemos asegurar que el resto sea menor que una cierta tolerancia (como lo fue $10^{-4}$) aún cuando $x$ esté fijo.

¿Cómo lo hacemos? Si $x$ está fijo, lo único que podemos modificar es $n$.

Si trabajamos con un $n$ fijo, la única forma de reducir el resto es tomar valores de $x$ cada vez más cercanos a $a$.

Cuando $x$ está fijo, podemos lograr que el polinomio se parezca cada vez más a la función aumentando el orden (o grado) $n$:
$$
\lim_{ n \to +\infty } r_{n}(x) = 0
$$

$$
|f(x) - P_{n}(f, a)(x)| \rightarrow 0
$$
Anteriormente, lo anterior solo era posible considerando valores cercanos a $a$. Sin embargo, lo que podemos hacer cuando se establece un valor de $x$, es considerar valores mayores de $n$, asegurando que el parecido con la función sea cada vez mayor. Aquí, la única precondición es que $n$ pueda tender a $+\infty$ (función indefinidamente derivable).

Ahora, consideramos otra de las expresiones abordadas la clase pasada:
$$
f(x) = \frac{1}{1 - x} = 1 + x + x^{2} + \dots + x^{n} + \underbrace{ \frac{x^{n + 1}}{1 - x} }_{ r_{n}(x) }
$$
Para asegurar que el término resto sea prácticamente nulo, tenemos que considerar valores de $x$ entre -1 y 1 (ya que entre estos valores, a mayor potencia, el valor resultante será menor):

Si $x \in (-1, 1) \implies \lim_{ n \to +\infty } r_{n}(x) = \frac{1}{1 - x}$.

Entonces:
$$
1 + x + x^{2} + \dots + x^{n} + \dots = \frac{1}{1 - x}
$$
Esto es lo que se llama una serie de potencias, lo podemos ver como un polinomio de grado $+ \infty$.
Lo podemos expresar como sumatoria:
$$
\sum_{n = 0}^{+ \infty} x^{n} = \frac{1}{1 - x}
$$

Si truncamos el valor $n$, la expresión ya no es igual, sino aproximada, y hay que agregar lo que falta para llegar (el resto).

Ahora, pueden surgir dudas como: ¿Las derivadas también convergen?
$$
\sum_{n = 0}^{+ \infty} n x^{n - 1} = \frac{1}{(1 - x)^{2}}
$$

Bajo ciertas condiciones, se puede probar que es correcto. Lo mismo para las primitivas y otras operaciones.

Igualmente, esto no entra dentro del curso, pero funciona como un adelanto para muchos de los usos de los polinomios de Taylor que no abordaremos y su importancia, especialmente para la resolución de problemas complejos, reduciéndolos a problemas lineales (siendo fundamentales en computación).