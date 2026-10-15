# Teorema fundamental
En esta instancia (y durante las próximas clases), abordaremos métodos para calcular integrales. Todos estarán basados en el teorema fundamental del cálculo.

Recordemos el teorema:

> [!Teorema fundamental]
> Sea $f : [a, b] \to \mathbb{R}$ integrable, y $F : [a, b] \to \mathbb{R}$ definida por
> $$
> F(x) = \int_{a}^{x} f(t) \space dt
> $$
> Entonces, si $f$ es continua en $x_{0}$, $F$ es derivable en $x_{0}$ y
> $$
> F'(x_{0}) = f(x_{0})
> $$

Antes de demostrarlo, veremos algunas aplicaciones para el cálculo de integrables.

También surge un corolario del teorema fundamental:

> [!Corolario]
> Si $f$ es continua (en todo su dominio), entonces $F$ es derivable.

De esta forma, la hipótesis de que $f$ es integrable es redundante en caso de que $f$ sea continua. La hipótesis es importante, ya que para que se cumpla lo establecido por el teorema, es necesario que $f$ sea continua en al menos $x_{0}$.

Esto también nos da paso a definir lo que es una primitiva:

> [!Primitiva - Definición]
> Dada $f : I \to \mathbb{R}$, decimos que $F : I \to \mathbb{R}$ es una primitiva de $f$ si
> $$
> F'(x) = f(x) \qquad \forall x \in I
> $$

De esta forma, una función $f$ es primitiva de $g$, si cuando derivamos $f$ obtenemos $g$. Es como "la derivación previa".

Esto da lugar a muchos ejemplos y resultados, por ejemplo:

> [!Resultado]
> $G$ es una primitiva de $f$ y $f$ es continua, entonces
> $$
> \int_{a}^{b} f(t) \space dt = G(b) - G(a)
> $$

Es fundamental que la derivada sea continua en todos lados para poder aplicar la propiedad, ya que la derivada de una función puede existir y no ser continua.

¿Cómo se da el resultado anterior?

Sea $F(x) = \int_{a}^{x} f(t) \space dt$ y $G$ una primitiva de $f$. Podemos desarrollar lo siguiente:
$$
F(a) = 0 = G(a) - G(a)
$$
$$
F'(x) = f(x) = G'(x)
$$
Entonces:
$$
H(x) = G(x) - G(a)
$$
Esta función cumple que:
$$
F(a) = 0 = G(a) - G(a) = H(a) \implies F(a) = H(a)
$$
$$
F'(x) = f(x) = G'(x) = H'(x) \implies F'(x) = H'(x)
$$
$H$ es igual a $F$ en un punto ($a$), y sus derivadas son iguales, por lo tanto, son la misma función:
$$
F(x) = H(x)
$$

A partir de esto, es posible calcular integrables de funciones $f$, sabiendo cual es la primitiva (la función cuya derivada es $f$).

Por ejemplo, una función que no sabemos derivar:
$$
\int_{a}^{b} \sin(t) \space dt = - \cos (b) - (- \cos(a))
$$
puesto que sabemos que una función cuya derivada es $\sin(x)$ es $-\cos(x)$.

$$
\int_{a}^{b} e^{t} \space dt = e^{b} - e^{a}
$$

Esto da una idea de como calcular integrales que antes parecían complicadas.

Este teorema dice que integrar y derivar son operaciones "opuestas". Sabiendo esto, con propiedades de derivadas, tendremos propiedades de integrales, las cuales nos facilitarán los cálculos. Igualmente, calcular integrales es más difícil que calcular derivadas, cosa que veremos posteriormente.

---
A continuación, demostramos el teorema:

## Demostración
Hay que probar
$$
\lim_{ h \to 0 } \frac{F(x_{0} + h) - F(x_{0})}{h} = f(x_{0}) 
$$
o sea (según la definición de límite), dado $\epsilon > 0$, $\exists \delta > 0$ tal que
$$
\left| \frac{F(x_{0} + h) - F(x_{0})}{h} - f(x_{0}) \right| < \epsilon
$$
$$
\forall h: |h| < \delta, h \neq 0
$$

Por definición:
$$
\begin{align}
F(x_{0} + h) - F(x_{0}) &= \int_{a}^{x_{0} + h} f(t) \space dt - \int_{a}^{x_{0}} f(t) \space dt \\
&= \int_{x_{0}}^{x_{0} + h} f(t) \space dt
\end{align}
$$
Así expresamos el numerador del cociente con integrales.

Ahora, veremos que si $f$ es continua siempre, podemos aplicar el teorema del valor medio y decir que $\int_{x_{0}}^{x_{0} + h} f(t) \space dt$ es $f(x)(x_{0} + h - x_{0}) = h(f(x))$, con $x \in [x_{0}, x_{0} + h]$. Sin embargo, como $h$ divide en la expresión original, se cancelarían los factores, quedando simplemente $f(x) - f(x_{0})$, cumpliéndose que $x \to x_{0}$, ya que $h \to 0$, entonces $f(x) \to f(x_{0})$.

El problema es que no sabemos si $f$ es continua en todo el intervalo.

Por otro lado:
$$
f(x_{0}) = \frac{\int_{x_{0}}^{x_{0} + h} f(x_{0}) \space dt}{h}
$$

Sabemos que $f(x_{0})$ es una constante en $t$. Por lo tanto:
$$
\begin{align}
&f(x_{0}) = \frac{\int_{x_{0}}^{x_{0} + h} f(x_{0}) \space dt}{h} \\
&f(x_{0}) = f(x_{0})\frac{\int_{x_{0}}^{x_{0} + h} 1 \space dt}{h} \\
&f(x_{0}) = f(x_{0})\frac{\cancel{ x_{0} } + h - \cancel{ x_{0} }}{h} \\
&f(x_{0}) = f(x_{0})\cancel{ \frac{h}{h} } \\
&f(x_{0}) = f(x_{0})
\end{align}
$$
Es así que la expresión tiene sentido.

De esta forma:
$$
\begin{align}
\left| \frac{F(x_{0} + h) - F(x_{0})}{h} - f(x_{0}) \right| &= \left| \frac{\int_{x_{0}}^{x_{0} + h} f(t) \space dt - \int_{x_{0}}^{x_{0} + h} f(x_{0}) \space dt}{h} \right| \\
&= \left| \int_{x_{0}}^{x_{0} + h} \frac{f(t) - f(x_{0}) \space dt}{h} \right|
\end{align}
$$

Es así que pasamos de tener una indeterminación y una constante, a una expresión que:
- solo tiene una indeterminación.
- $f(t) - f(x_{0})$ es relativo a $h$, por lo tanto $f(t) - f(x_{0})$ es chico por la continuidad de $f$.

Resulta que
$$
\left| \int_{x_{0}}^{x_{0} + h} \frac{f(t) - f(x_{0}) \space dt}{h} \right| \leq \left| \int_{x_{0}}^{x_{0} + h} \frac{|f(t) - f(x_{0})| \space dt}{|h|} \right|
$$
El valor absoluto importa (hay que dejarlo) por si se da que el intervalo no esté bien colocado (estemos yendo "al revés", cambiando el signo del resultado).

Ahora, podemos hacer que $|f(t) - f(x_{0})| < \epsilon$.

Como $f$ es continua en $x_{0}$, $\exists \delta$ tal que $\forall t \in [x_{0} - \delta, x_{0} + \delta]$, se tiene que
$$
|f(t) - f(x_{0})| < \frac{\epsilon}{2}
$$
El $t$ de la integral definida está en $[x_{0}, x_{0} + h]$, por lo que $t \in [x_{0} - \delta, x_{0} + \delta]$ si $|h| < \delta$.

Elegimos $\frac{\epsilon}{2}$ para facilitar la demostración, en base a una propiedad que indica que si una función es menor que otra, entonces la integral es menor estricta (si el intervalo no es un punto).

Proseguimos:
$$
\begin{align}
\left| \int_{x_{0}}^{x_{0} + h} \frac{|f(t) - f(x_{0})| \space dt}{|h|} \right| &\leq \left| \int_{x_{0}}^{x_{0} + h} \frac{\frac{\epsilon}{2} \space dt}{|h|} \right| \qquad \text{si } |h| < \delta \\
&= \frac{\epsilon}{2} \left| \frac{x_{0} + h - x_{0}}{|h|} \right| \\
&= \frac{\epsilon}{2} \\
&< \epsilon
\end{align}
$$


Aquí finaliza la demostración, probando que
$$
\lim_{ h \to 0 } \frac{F(x_{0} + h) - F(x_{0})}{h} = f(x_{0}) 
$$

---
A continuación, pasaremos a estudiar una de las propiedades fundamentales surgidas del teorema fundamental:

> [!Regla de Barrow]
> Sea $f$ continua y $F$ primitiva de $f$:
> $$
> \int_{a}^{b} f(t) \space dt = F(b) - F(a)
> $$

Esto dice que si conozco una función $F$ que cuando la derivo me da $f$, entonces la integral de $f$ en el intervalo $[a, b]$ es igual a la diferencia de las imágenes de los extremos $a, b$ en la función $F$.

Uno de los problemas básicos de la matemática que es imposible resolver es como invertir una función. Esto nos sirve de puntapié para lo siguiente:
Podemos calcular la derivada de cualquier composición de funciones básicas (a no ser que estemos en un punto singular, teniendo que determinar un límite), aplicando regla de la cadena, producto, etc., y por muy complejo que fuera el problema, tenía solución. Sin embargo, aquí muchos problemas sencillos no tendrán solución.

Un ejemplo básico:
$$
\int_{a}^{x} e^{-t^{2}} dt = F(x)
$$
Sabemos que la función $F$ es derivable y su derivada es $e^{-t^{2}}$. Sin embargo, no podemos escribir a $F$ como composición de las funciones elementales que hemos visto hasta ahora ($\sin, \cos, \log, e^{x}, \dots$), en ningún punto.

Como no tenemos esa certeza, cuando nos enfrentamos a una integral, tenemos que trabajar con una serie de reglas e intentar llegar a algún resultado.

Si queremos obtener un resultado, podríamos aproximar una suma superior e inferior y llegar a un resultado aproximado, pero en determinados contextos puede ser necesario determinar la primitiva.

Ahora, analizaremos algunas primitivas e integrales:
$$
\int_{a}^{b} x^{\alpha} \space dx \underbrace{ = }_{ \alpha \neq -1 } \left. \frac{x^{\alpha + 1}}{\alpha + 1} \right|_{a}^{b} = \frac{b^{\alpha + 1} - a^{\alpha + 1}}{\alpha + 1}
$$
Notación $|_{a}^{b}$: la función previa la evaluó entre los límites establecidos, haciendo $f(b) - f(a)$.

Para definir funciones de este tipo, en todo momento tenemos que considerar la regla de Barrow, puesto que:
$$
\int_{a}^{b} f(t) \space dt = F(b) - F(a)
$$
$$
\implies \int_{b}^{b} f(t) \space dt = F(b) - F(b) = 0
$$
De esta forma, podemos notar que hay ciertas funciones que no existen:
$$
\int_{a}^{x} f(t) \space dt = e^{x}
$$
No existe función $f(t)$ tal que la integral sea $e^{x}$, ya que $e^{x}$ nunca se anula y la integral se puede anular (cuando los extremos coinciden, en este caso, si $x = a$). En este caso, hay que agregar una constante, por ejemplo:
$$
\int_{a}^{b} e^{x} \space dx = e^{x} |_{a}^{b} = e^{b} - e^{a}
$$
Otros ejemplos:
$$
\int_{a}^{b} \sin(x) \space dx = -\cos(x) |_{a}^{b}
$$
$$
\int_{a}^{b} \cos(x) \space dx = \sin(x) |_{a}^{b}
$$
$$
\int_{a}^{b} \frac{1}{t} \space dt = \log(t) |_{a}^{b} \qquad \text{con } a, b > 0
$$
Una que puede no parecer tan fácil es la función $\log$. Sin embargo, aprovechando funciones de integrales, especialmente relacionadas con las funciones inversas: se puede integrar la inversa de una función que si sabemos integrar, y aprovechar dicho resultado. Sabemos que la inversa de $\log$ es $\exp(x) = e^{x}$.

---
Ahora, analizaremos diferentes propiedades de las derivadas, y como dichas propiedades se traducen en integrales para calcular la integral de funciones. De esta forma, calcular integrales requiere conocer que funciones son las derivadas de cuales, puesto que los cálculos se facilitan.
$$
(u^{2})' = 2u u'
$$
De esta forma, si en una integral detectamos una función de tipo $2u u'$, la integral será $u^{2}$.
Por ejemplo:
$$
\int_{a}^{b} \cos(x) \sin(x) \space dx = \left. \frac{\sin ^{2}(x)}{2} \right|_{a}^{b}
$$
Ya que:
$$
\left( \frac{\sin ^{2}(x)}{2} \right)' = \frac{2 \sin(x) \cos(x)}{2} = \sin(x) \cos(x)
$$

$$
\int_{a}^{b} \frac{\log(x)}{x} \space dx = \left. \frac{\log ^{2}(x)}{2} \right|_{a}^{b}
$$

Esto se puede ampliar a potencias:
$$
\int_{a}^{b} \cos(x) \sin ^{7}(x) dx = \left. \frac{\sin ^{8}(x)}{8} \right|_{a}^{b}
$$

Aunque esta estrategia es útil, a veces puede ser algo difícil de aplicar.

Además, hay otra propiedad diferente por como se utiliza:
$$
(uv)' = u'v + uv'
$$
De esta forma:
$$
\int_{a}^{b} u'v + uv' = \left. uv \right|_{a}^{b}
$$
Sin embargo, es una regla que sirve para casos específicos y puede ser difícil de aplicar a simple vista. Lo interesante de dicha propiedad es utilizarla para explorar y buscar expresar el problema de otra manera:
$$
\int_{a}^{b} u'v + uv' = \int_{a}^{b} u'v + \int_{a}^{b} uv' = \left. uv \right|_{a}^{b}
$$
$$
\implies \int_{a}^{b} u'v = \left. uv \right|_{a}^{b} - \int_{a}^{b} uv'
$$
Simplemente se trata de buscar otro punto de vista. Si se integrar alguna de las funciones del producto, puedo intentar aplicar este método y obtener una solución.

Por ejemplo:
$$
\int_{a}^{b} x \sin(x) \space dx
$$
Aquí podemos considerar
$$
\left[
\begin{align}
&u'(x) = \sin(x) &&u(x) = -\cos(x) \\
&v(x) = x &&v'(x) = 1
\end{align}
\right]
$$
$$
\begin{align}
\int_{a}^{b} x \sin(x) \space dx &= \left. -x \cos(x) \right|_{a}^{b} + \int_{a}^{b} \cos(x) \space dx \\
&= \left. -x \cos(x) + \sin(x) \right|_{a}^{b}
\end{align}
$$

Consejo: Siempre realizar el diagrama con las derivadas de las funciones involucradas, puesto que permite evitar integrar o derivar dos veces, dejando claramente cuales son las funciones partícipes y sus derivadas.

Lo interesante es que, en base al ejemplo anterior, por inducción podemos decir que es posible calcular
$$
\int_{a}^{b} P(x) \cdot u
$$
siendo $u$ cualquier función de las que hemos estudiado hasta ahora ($e^{x}, \sin(x), \cos(x), \log(x), \dots$).

Ahora, veremos otro ejemplo que busca visualizar algunos problemas de utilizar este enfoque. Como se trata de un método exploratorio, podemos no siempre llegar a un resultado.
$$
\int_{a}^{b} \log(x) \space dx
$$
A simple vista, parecen no haber dos funciones. Sin embargo, consideraremos a uno como una función, siendo su primitiva $x$.
$$
\left[
\begin{align}
&u'(x) = 1  &&u(x) = x \\
&v(x) = \log(x) &&v'(x) = \frac{1}{x}
\end{align}
\right]
$$
De esta forma:
$$
\begin{align}
\int_{a}^{b} \log(x) \space dx &= x \log(x) |_{a}^{b} - \int_{a}^{b} 1 \space dx \\
&= x (\log(x) - 1) |_{a}^{b}
\end{align}
$$

Lo importante de este ejemplo es notar que este método siempre se puede aplicar, manipulando a la función para llevarla a una forma interesante.

Un ejemplo que retomaremos la próxima clase:
$$
\int_{a}^{b} \sin ^{2}(x) \space dx
$$
Lo más "obvio" es considerar ambas funciones como $\sin$.
$$
\left[
\begin{align}
&u'(x) = \sin(x)  &&u(x) = -\cos(x) \\
&v(x) = \sin(x) &&v'(x) = \cos(x)
\end{align}
\right]
$$
$$
\int_{a}^{b} \sin ^{2}(x) \space dx = -\cos(x) \sin(x) |_{a}^{b} + \int_{a}^{b} \cos ^{2}(x) \space dx
$$
Como vemos, obtuvimos otra integral que (por ahora) solamente sabemos simplificar mediante el mismo método. Sin embargo, si aplicamos la misma estrategia con $\int_{a}^{b} \cos ^{2}(x) \space dx$, tenemos que volver a definir $u, u', v, v'$, y si se prosigue con los cálculos, al final obtendremos $0 = 0$, puesto que del lado derecho obtendremos exactamente $\int_{a}^{b} \sin ^{2}(x) \space dx$.

Sin embargo, podemos tomar otro enfoque, sabiendo que $\cos ^{2}(x) = 1 - \sin ^{2}(x)$:
$$
\begin{align}
\int_{a}^{b} \sin ^{2}(x) \space dx &= -\cos(x) \sin(x) |_{a}^{b} + \int_{a}^{b} \cos ^{2}(x) \space dx \\
&= -\cos(x) \sin(x) |_{a}^{b} + \int_{a}^{b} 1 \space dx - \int_{a}^{b} \sin ^{2}(x) \space dx
\end{align}
$$
Ahora, tenemos que:
$$
\begin{align}
2\int_{a}^{b} \sin ^{2}(x) \space dx &= -\cos(x) \sin(x) |_{a}^{b} + \int_{a}^{b} 1 \space dx \\
&= -\cos(x) \sin(x) + x |_{a}^{b}
\end{align}
$$
$$
\begin{align}
\int_{a}^{b} \sin ^{2}(x) \space dx &= \left. -\frac{\cos(x) \sin(x) + x}{2} \right|_{a}^{b}
\end{align}
$$

En conclusión, al tratarse de un método exploratorio, no siempre se obtienen resultados satisfactorios. Sin embargo, es el mejor método de integración para comenzar, ya que es el más sencillo de comenzar a explorar, siendo aplicable a muchísimos casos, incluso aunque no tengamos un producto explícito.

La clase que viene comenzaremos viendo algunos ejemplos más. También estudiaremos el cambio de variable (visto en integrales lineales), aunque veremos la forma general, y seguiremos trabajando con el teorema fundamental.