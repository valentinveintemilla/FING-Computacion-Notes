# Teorema fundamental
Esta semana estará cargada de nuevas formas de afrontar el cálculo de integrales y primitivas.

Hay dos principales:
- Método de integración por partes: surge de la regla de la derivada del producto.
- Fórmula de sustitución: basado en la regla de la cadena.

En esta clase nos enforcaremos en el método de integración por partes.

También veremos (en la clase 37) el método de integración por fracciones simples, el cual permite integrar cocientes de polinomios.

Recordamos la regla de Barrow:

> [!Regla de Barrow]
> $$
> \int_{a}^{b} f(t) \space dt = F(b) - F(a)
> $$
> donde $F$ es una primitiva de $f$ (es decir, $F' = f$).

De esta forma, podemos calcular la integral de una función definida entre dos números, simplemente determinando una primitiva de dicha función y considerando la diferencia de la primitiva en los extremos de integración de la función.

De esta forma, el problema de calcular integrales pasa a ser hallar primitivas, antiderivadas.

Por ejemplo:
$$
\int_{0}^{\frac{\pi}{2}} \cos(x) \space dx
$$
Previo a la regla de Barrow, teníamos que aproximar mediante particiones, suma superior e inferior, etc.
Ahora, como $(\sin(x))' = \cos(x)$, la regla de Barrow nos dice:
$$
\int_{0}^{\frac{\pi}{2}} \cos(x) \space dx = \left. \sin(x) \right|_{0}^{\frac{\pi}{2}} = \sin\left( \frac{\pi}{2} \right) - \sin(0) = 1 - 0 = 1
$$

Antes de proseguir, es importante considerar lo siguiente:

Siempre podemos derivar una función, aplicando las diferentes fórmulas y reglas para pasar de una expresión a la derivada de la misma.

Sin embargo, no podemos decir lo mismo de las primitivas. No solo no hay un método para calcular la primitiva de una función, sino que a veces incluso no tienen fórmula.
Si bien una función siempre tiene primitiva, no siempre la misma tendrá una fórmula que podamos determinar (llamada primitiva elemental).

Algunos ejemplos de funciones que no tienen primitiva elemental (no podremos expresar su fórmula mediante otras funciones tradicionales, como $\sin, \cos, e^{x}, \log, \dots$):
$$
\sqrt{ 1 - x^{2} }, \frac{1}{\log(x)}, e^{-x^{2}}, \sin(x^{2}), \frac{\sin(x)}{x}, \dots
$$

Estos son solo algunos ejemplos, aunque lógicamente no trabajaremos con estas funciones en el práctico.

---
Existen diversos métodos para determinar primitivas de funciones, el que estudiaremos hoy: Integración por partes.
## Método de integración por partes

Dicho método está basado en la regla de Leibniz (integral del producto de dos funciones):
$$
(f(x)g(x))' = f'(x)g(x) + f(x)g'(x)
$$
Es decir, $f \cdot g$ es una primitiva de $f'g + fg'$ (ya que $f \cdot g$ derivada da como resultado $f'g + fg'$).

Por ejemplo, para calcular la siguiente integral:
$$
\int_{a}^{b} f'(x) \cdot g(x) + f(x) \cdot g'(x) \space dx = f(b) \cdot g(b) - f(a) \cdot g(a) = f(x) \cdot g(x) |_{a}^{b}
$$
Esta sería la fórmula base, aunque normalmente se expresa y utiliza de la siguiente forma:
$$
\int_{a}^{b} f'(x) \cdot g(x) \space dx = f(x) \cdot g(x) |_{a}^{b} - \int_{a}^{b} f(x) \cdot g'(x) \space dx
$$
La fórmula es sumamente útil, ya que muchas veces podemos identificar que la función se trata de un producto (o lo podemos expresar como tal), y aunque no sepamos integrar $f'(x) \cdot g(x)$, sabemos integrar $f(x) \cdot g'(x)$ (reduciendo el problema de una integral que no sabemos calcular a una que si).

Antes de proseguir, estableceremos la notación de Leibniz:

> [!Notación de Leibniz]
> $$
> \int f(x) \space dx = F(x) + c
> $$
> Se lee "$F$ es una primitiva de $f$".

Como vemos, en esta notación se ignoran los extremos (ya que es una generalización).

Es simplemente una forma de notar que una función es primitiva de otra.

La constante $c$ puede aparecer o no. Se añade ya que la primitiva de una función no es única (a diferencia de la derivada). Sabemos que a la primitiva de una función le podemos sumar una constate cualquiera, y cuando derivemos dicha función, en todos los casos obtendremos $f$.

Por esto, se dice que la primitiva es única "a menos de suma por constantes". De esta manera, todas las primitivas tienen la forma $F(x) + c$, ignorándose el término $c$ al derivar.

Se trata más que nada de una formalidad.

Con esta notación, podemos expresar de forma general la fórmula de integración por partes para primitivas:
$$
\int f'(x) \cdot g(x) \space dx = f(x) \cdot g(x) - \int_{a}^{b} f(x) \cdot g'(x) \space dx
$$

En general, trabajaremos con integrales indefinidas, ya que esto contiene todo. De esta forma, al determinar la forma general de la primitiva (con la fórmula anterior), podremos integrar en el intervalo que queramos simplemente aplicando la regla de Barrow: calculamos la resta entre el valor de la primitiva para el extremo superior y el valor de la primitiva para el extremo inferior.

### Ejemplos

#### Ejemplo 1
Hallar una primitiva de $x \cdot e^{x}$:
$$
\int x \cdot e^{x} \space dx = 
$$
Sin aplicar el método aún, definamos el objetivo: hallar una función $f$, tal que $f' = x e^{x}$. Esto es fundamental para entender realmente cual es el objetivo y como se simplifica el cálculo de integrales aplicando reglas y propiedades de derivación.

Ahora, aplicamos el método:
Una función va a tener que hacer de $f'$ y la otra de $g$. Generalmente, hay un camino más sencillo (o incluso el único viable) que el otro. Lo importante es que con la práctica y experiencia se mejora la técnica.

Por ejemplo, probemos con la siguiente combinación:
$$
\begin{align}
&f'(x) = x \implies f(x) = \frac{x^{2}}{2} \\
&g(x) = e^{x} \implies g'(x) = e^{x}
\end{align}
$$
$$
\int x \cdot e^{x} \space dx = \frac{x^{2}}{2} \cdot e^{x} - \int \frac{x^{2}}{2} \cdot e^{x} \space dx
$$
De esta forma, una primitiva de $x \cdot e^{x}$ se obtiene con $\frac{x^{2}}{2} \cdot e^{x} - \int \frac{x^{2}}{2} \cdot e^{x} \space dx$, lo que es correcto, pero ahora tenemos que hallar una primitiva de $\int \frac{x^{2}}{2} \cdot e^{x} \space dx$. Sin embargo, el problema parece haberse complejizado, por lo que probaremos en el otro sentido, cambiando la combinación:
$$
\begin{align}
&f'(x) = e^{x} \implies f(x) = e^{x} \\
&g(x) = x \implies g'(x) = 1
\end{align}
$$
$$
\int e^{x} \cdot x \space dx = e^{x} \cdot x - \int e^{x} \cdot 1 \space dx
$$
Además, sabemos que una primitiva de $e^{x}$ es $e^{x} + c$, por lo tanto:
$$
\begin{align}
&= e^{x} \cdot x - e^{x} + c \\
&= e^{x} (x - 1) + c
\end{align}
$$
En caso de dudar si el resultado obtenido es correcto o no, podemos derivarlo, y si obtenemos la función inicial (la que se integra), entonces es correcto.
De esta forma, si derivamos $e^{x} (x - 1) + c$, tenemos que obtener $e^{x} \cdot x$:
$$
\begin{align}
(e^{x} (x - 1) + c)' &= (e^{x})'(x - 1) + e^{x}(x - 1)' \\
&= e^{x}(x - 1) + e^{x} \\
&= e^{x} \cdot x - \cancel{ e^{x} } + \cancel{ e^{x} } \\
&= e^{x} \cdot x
\end{align}
$$
Esto quiere decir que $e^{x} (x - 1) + c$ es una primitiva de $e^{x} \cdot x$. Este último paso simplemente fue una verificación.

Ahora, si quisiéramos calcular la integral en un intervalo, podemos hacerlo utilizando la primitiva calculada y la regla de Barrow:
$$
\begin{align}
\int_{0}^{1} e^{x} \cdot x \space dx &= e^{x} (x - 1) |_{0}^{1} \\
&= [e^{1} (1 - 1)] - [e^{0} (0 - 1)] \\
&= \cancel{ e^{1} \cdot 0 } - e ^{0} \cdot (-1) \\
&= e^{0} \\
&= 1
\end{align}
$$
Si hubiéramos agregado el término $c$ a la primitiva, se habría cancelado en la resta. Este término es más bien para dar a entender que a la primitiva se le podría sumar cualquier constante, ya que al derivar dicha función, siempre se obtendrá el mismo resultado.

#### Ejemplo 2

Hallar una primitiva para $x \cdot \log(x)$:
$$
\int x \cdot \log(x) \space dx
$$
Consideraremos la siguiente combinación (ya que de primera no se nos ocurre una primitiva de $\log(x)$):
$$
\begin{align}
&f'(x) = x \implies f(x) = \frac{x^{2}}{2} \\
&g(x) = \log(x) \implies g'(x) = \frac{1}{x}
\end{align}
$$
$$
\begin{align}
\int x \cdot \log(x) \space dx &= \frac{\log(x) \cdot x^{2}}{2} - \int \frac{x^{2}}{2} \cdot \frac{1}{x} \space dx \\
&= \frac{\log(x) \cdot x^{2}}{2} - \int \frac{x}{2} \space dx \\
&= \frac{\log(x) \cdot x^{2}}{2} - \frac{x^{2}}{4} + c
\end{align}
$$
Aclaración: es fácil encontrar una primitiva para $\frac{x}{2}$, ya que es un polinomio.

Verificamos:
$$
\begin{align}
\left( \frac{\log(x) \cdot x^{2}}{2} - \frac{x^{2}}{4} + c \right)' &= \left( \frac{\log(x) \cdot x^{2}}{2} \right)' - \left( \frac{x^{2}}{4} \right)' \\
&= \frac{2(\log(x) \cdot x^{2})'}{4} - \frac{8x}{16} \\
&= \frac{2x + 4x \cdot \log(x)}{4} - \frac{x}{2} \\
&= \cancel{ \frac{x}{2} } + x \cdot \log(x) - \cancel{ \frac{x}{2} } \\
&= x \cdot \log(x)
\end{align}
$$
Confirmamos que $\frac{\log(x) \cdot x^{2}}{2} - \frac{x^{2}}{4} + c$ es una primitiva de $x \cdot \log(x)$.

Un detalle interesante es que, como siempre se obtiene otra integral del lado derecho, pueden existir múltiples formas de resolverla:
- Hallar la primitiva para dicha función (por cualquiera de los métodos vistos y por estudiar).
- Pasar para el lado izquierdo en caso de que sea equivalente a la anterior (casos excepcionales).

Esto abre un mundo de posibilidades.

#### Ejemplo 3
$$
\int \log(x) \space dx
$$
Aunque parezca que no (ya que no hay producto), se puede encontrar la primitiva de $\log(x)$ mediante integración por partes, pero tenemos que agregar un coeficiente 1 (el cual es trivial):
$$
\int \log(x) \space dx = \int 1 \cdot \log(x) \space dx
$$
Sin embargo, lo estudiaremos como la derivada de una función cuando establecemos la combinación utilizada:
$$
\begin{align}
&f'(x) = 1 \implies f(x) = x \\
&g(x) = \log(x) \implies g'(x) = \frac{1}{x}
\end{align}
$$
De esta manera:
$$
\begin{align}
\int 1 \cdot \log(x) \space dx &= x \cdot \log(x) - \int x \cdot \frac{1}{x} \space dx \\
&= x \cdot \log(x) - \int 1 \space dx \\
&= x \cdot \log(x) - x \\
&= x(\log(x) - 1) + c
\end{align}
$$
Verificamos:
$$
\begin{align}
(x(\log(x) - 1) + c)' &= (\log(x) - 1) + x\left( \frac{1}{x} \right) \\
&= \log(x) - \cancel{ 1 } + \cancel{ 1 } \\
&= \log(x)
\end{align}
$$
Confirmamos que $x(\log(x) - 1) + c$ es una primitiva de $\log(x)$.

Como vemos, es una buena alternativa multiplicar por 1 y utilizar una de sus primitivas para intentar hallar una solución.

#### Ejemplo 4
$$
\int \sin ^{2}(x) \space dx
$$
Aquí no tenemos mucha alternativa más que:
$$
\begin{align}
&f'(x) = \sin(x) \implies f(x) = -\cos(x) \\
&g(x) = \sin(x) \implies g'(x) = \cos(x)
\end{align}
$$
$$
\begin{align}
\int \sin ^{2}(x) \space dx &= (-\cos(x)) \cdot \sin(x) - \int (-\cos(x)) \cdot (\cos(x)) \space dx \\
&= -\cos(x) \cdot \sin(x) + \int \cos ^{2}(x) \space dx
\end{align}
$$
Aquí podríamos pensar que llegamos a un callejón sin salida, puesto que si volvemos a aplicar integración por partes, nos encontraremos con un bucle sin salida. Sin embargo, considerando propiedades de las funciones trigonométricas, podemos resolver el problema:
$$
\sin ^{2}(x) + \cos ^{2}(x) = 1 \implies \cos ^{2}(x) = 1 - \sin ^{2}(x)
$$
Entonces:
$$
\begin{align}
\int \sin ^{2}(x) \space dx &= -\cos(x) \cdot \sin(x) + \int 1 - \sin ^{2}(x) \space dx \\
&= -\cos(x) \cdot \sin(x) + \int 1 \space dx - \int \sin ^{2}(x) \space dx \\
&= -\cos(x) \cdot \sin(x) + x - \int \sin ^{2}(x) \space dx
\end{align}
$$
Ahora, llegamos a la siguiente expresión:
$$
\int \sin ^{2}(x) \space dx = -\cos(x) \cdot \sin(x) + x - \int \sin ^{2}(x) \space dx
$$
Lo que podemos hacer para evitar buscar la primitiva nuevamente, y no pasar por los mismos pasos, es sumar a ambos lados la primitiva de $\sin ^{2}(x)$:
$$
\begin{align}
\int \sin ^{2}(x) \space dx + \int \sin ^{2}(x) \space dx &= -\cos(x) \cdot \sin(x) + x \\
2\int \sin ^{2}(x) \space dx &= -\cos(x) \cdot \sin(x) + x
\end{align}
$$
Ahora, continuamos operando con normalidad:
$$
\begin{align}
2\int \sin ^{2}(x) \space dx &= -\cos(x) \cdot \sin(x) + x \\
\int \sin ^{2}(x) \space dx &= \frac{-\cos(x) \cdot \sin(x) + x}{2} + c
\end{align}
$$

Sabiendo esto, si quisiéramos determinar la derivada de $\cos ^{2}(x)$, podríamos aprovechar la propiedad mencionada:
$$
\begin{align}
\int \cos ^{2}(x) \space dx &= \int 1 - \sin ^{2}(x) \space dx \\
&= \int 1 \space dx - \int \sin ^{2}(x) \space dx \\
&= x - \frac{-\cos(x) \cdot \sin(x) + x}{2} \\
&= x + \frac{\cos(x) \cdot \sin(x) - x}{2} \\
&= \frac{\cos(x) \cdot \sin(x) - x + 2x}{2} \\
&= \frac{\cos(x) \cdot \sin(x) + x}{2} + c
\end{align}
$$

En la próxima clase, continuaremos con un nuevo método de integración: Integración por sustitución.