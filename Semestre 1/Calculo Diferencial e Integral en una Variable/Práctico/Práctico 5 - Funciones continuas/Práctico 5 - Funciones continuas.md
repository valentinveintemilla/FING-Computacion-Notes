# 5.1 - Continuidad
## Ejercicio 5.1.1

---
# 5.2 - Teorema de Bolzano
## Ejercicio 5.2.2
### Parte a)
Si estudiamos las funciones $x$ y $2 \cos (x)$ por separado, sabemos que ambas son continuas. Por esta razón, su adición también será una función continua: $x + 2 \cos (x)$. De esta forma, y sabiendo cual es el conjunto imagen de cada función:
$$
\begin{align}
&\mathrm{Im}(x) = \mathbb{R} \\
&\mathrm{Im}(2 \cos (x)) = [-2, 2]
\end{align}
$$
Simplemente tenemos que encontrar un valor de $x$ para el que la función sea negativa, y otro para el que la función sea positiva:
$$
\begin{align}
&x = -10 \\
&\text{Para } f(x) = x = -10 \\
&\text{Para } g(x) = 2 \cos (x) = 2 \cos (-10) \in [-2, 2] \\
&\implies x + 2 \cos (x) \in [-12, -8] \\
& \\
&x = 10 \\
&\text{Para } f(x) = x = 10 \\
&\text{Para } g(x) = 2 \cos (x) = 2 \cos (10) \in [-2, 2] \\
&\implies x + 2 \cos (x) \in [8, 12] \\
\end{align}
$$
En conclusión, sabiendo que la función es continua y tiene una parte positiva y otra negativa, la función corta al eje $x$ al menos una vez ($x + 2 \cos (x)$ para al menos un $x \in \mathbb{R}$) por el Teorema de Bolzano.

### Parte b)
En todos estos casos, tenemos que encontrar un $n$ tal que $f(n) < 0$ y $f(n + 1) > 0$.
#### Parte a)
$$
x^{5} + 5x^{4} + 2x + 1
$$
Sabemos que los polinomios son funciones continuas.
Ahora, tenemos que encontrar un valor de $x$ para el cual $f(x) < 0$ y $f(x + 1) > 0$.
$$
\begin{align}
&x = -5 \\
&x^{5} + 5x^{4} + 2x + 1 = \cancel{ -3125 } + \cancel{ 3125 } - 10 + 1 = -9 \\
&\implies f(-5) < 0 \\
& \\
&x = -4 \\
&x^{5} + 5x^{4} + 2x + 1 = -1024 + 1280 - 8 + 1 = 49 \\
&\implies f(-4) > 0 \\
\end{align}
$$
De esta forma, encontramos $n = -5$ tal que $f(n) < 0$ y $f(n + 1) > 0$. Es así que, considerando el Teorema de Bolzano, sabemos que existe al menos un $x \in [n, n + 1]$ tal que $f(x) = 0$.

#### Parte b)
$$
x^{5} + x + 1
$$
$$
\begin{align}
&x = -1 \\
&x^{5} + x + 1 = -1 - 1 + 1 = -1 \\
&\implies f(-1) < 0 \\
& \\
&x = 0 \\
&x^{5} + x + 1 = 0 + 0 + 1 = 1 \\
&\implies f(0) > 0 \\
\end{align}
$$
De esta forma, encontramos $n = -1$ tal que $f(n) < 0$ y $f(n + 1) > 0$. Es así que, considerando el Teorema de Bolzano, sabemos que existe al menos un $x \in [-1, 0]$ tal que $f(x) = 0$.

#### Parte c)
$$
x + e^{x}
$$
$$
\begin{align}
&x = -1 \\
&x + e^{x} = -1 + e^{-1} = -1 + \frac{1}{e} < 0 \\
&\implies f(-1) < 0 \\
& \\
&x = 0 \\
&x + e^{x} = 0 + e^{0} = 0 + 1 = 1 \\
&\implies f(0) > 0 \\
\end{align}
$$
De esta forma, encontramos $n = -1$ tal que $f(n) < 0$ y $f(n + 1) > 0$. Es así que, considerando el Teorema de Bolzano, sabemos que existe al menos un $x \in [-1, 0]$ tal que $f(x) = 0$.

#### Parte d)
$$
\cos \left( \frac{\pi x}{2} \right) + x
$$
$$
\begin{align}
&x = -1 \\
&\cos \left( \frac{\pi x}{2} \right) + x = \cos \left( -\frac{\pi}{2} \right) - 1 = 0 - 1 = -1 \\
&\implies f(-1) = -1 \\
& \\
&x = 0 \\
&\cos \left( \frac{\pi x}{2} \right) + x = \cos (0) + 0 = 1 + 0 = 1 \\
&\implies f(0) = 1 \\
\end{align}
$$
De esta forma, encontramos $n = -1$ tal que $f(n) < 0$ y $f(n + 1) > 0$. Es así que, considerando el Teorema de Bolzano, sabemos que existe al menos un $x \in [-1, 0]$ tal que $f(x) = 0$.

---
## Ejercicio 5.2.5
Podemos decir que el que una función tenga puntos fijos significa que intercepta a la función identidad ($g(x) = x$) en algún momento de su recorrido.

### Parte a)
Si $f : [0, 1] \to [0, 1]$ es una función continua, entonces sabemos que toma todos los valores del intervalo $[0, 1]$.

Consideremos dos puntos $x_{1}, x_{2} \in [0, 1], x_{1} < x_{2}$.
Aquí consideramos dos casos:
1. $f(x_{1}) \geq x_{1}$ y $f(x_{2}) \leq x_{2}$
2. $f(x_{1}) \leq x_{1}$ y $f(x_{2}) \geq x_{2}$
En cualquiera de los casos anteriores, existe $c \in [x_{1}, x_{2}]$ para el cual $f(x_{2}) \leq f(c) \leq f(x_{1})$ o $f(x_{1}) \leq f(c) \leq f(x_{2})$ (según cual sea el caso). Sin importar el orden en el que se encuentren $f(x_{1})$ y $f(x_{2})$, por el teorema de los valores intermedios, existirá al menos un valor de $c$ para el cual $c = f(c)$. Esto también significa que $f$ intercepta a la función $g$ en $c$.

ACLARACIÓN: PARA UNA PRUEBA MÁS FORMAL, SE PUEDE CONSIDERAR LA FUNCIÓN $h(x) = f(x) - x$, LA CUAL ES CONTINUA YA QUE $f$ Y LA IDENTIDAD LO SON. DICHA FUNCIÓN TIENE AL MENOS UN ELEMENTO $c$ PARA EL CUAL $h(c) = 0$, Y DEMOSTRANDO ESTO, SE DEMUESTRA QUE $f(c) = c$.

### Parte b)
Este es similar al caso anterior, pero aquí la función recorre todo $\mathbb{R}$ y es estrictamente decreciente.

Consideremos dos puntos $x_{1}, x_{2} \in \mathbb{R}, x_{1} < x_{2}$. Esto implica que $f(x_{1}) \geq f(x_{2})$. Además, $x_{1} < f(x_{1})$ y $x_{2} > f(x_{2})$.
Como la función es continua y monótona decreciente, por el teorema de los valores intermedios, existirá un único $c \in [x_{1}, x_{2}]$ tal que $f(c) = c$, puesto que $x_{1} \leq c \leq x_{2}$, y $f(x_{1}) \geq f(c) \geq f(x_{2})$.

### Parte c)
Un ejemplo de una función con estas características puede ser la función $x + 1$. Esta es paralela a la función identidad ($x$). Por lo que no existe un punto $c$ perteneciente a la función tal que $f(c) = c$.

Otro ejemplo es la función $x^{2} + 1$.

---
## Ejercicio 5.2.6
### Parte a)
Como establece el comentario del ejercicio, en todos los casos consideraremos $x = \frac{n}{2}$, con $n \in \mathbb{Z}$.

#### Parte a)
$$
3x^{4} - 2x^{3} - 36x^{2} + 36x - 8
$$
$$
x = -4 \implies 3 \times 256 - 2 \times (-64) - 36 \times 16 + 36 \times (-4) - 8
$$
$$
= 768 + 128 - 576 - 144 - 8 = 896 - 728 = 168
$$
$$
x = -\frac{7}{2} \implies 3 \times \frac{2401}{16} - 2 \times \left( -\frac{343}{8} \right) - 36 \times \frac{49}{4} + 36 \times \left( -\frac{7}{2} \right) - 8
$$
$$
= 3 \times \frac{2401}{16} - 2 \times \left( -\frac{343}{8} \right) - 36 \times \frac{49}{4} + 36 \times \left( -\frac{7}{2} \right) - 8 = \frac{8575}{16} - 567 = \frac{8575}{16} - \frac{9072}{16} < 0
$$
Encontramos una raíz en el intervalo $\left[ -4, -\frac{7}{2} \right]$.

$$
x = -1 \implies 3 \times 1 - 2 \times (-1) - 36 \times 1 + 36 \times (-1) - 8
$$
$$
= 3 + 2 - 36 - 36 - 8 = -75
$$
$$
x = -\frac{1}{2} \implies 3 \times \frac{1}{16} - 2 \times \left( -\frac{1}{8} \right) - 36 \times \frac{1}{4} + 36 \times \left( -\frac{1}{2} \right) - 8
$$
$$
= \frac{3}{16} + \frac{1}{4} - 9 - 18 - 8 = \frac{7}{16} - 35 < 0
$$
$$
x = 0 \implies 3 \times 0 - 2 \times 0 - 36 \times 0 + 36 \times 0 - 8 = -8
$$
$$
x = \frac{1}{2} \implies 3 \times \frac{1}{16} - 2 \times \frac{1}{8} - 36 \times \frac{1}{4} + 36 \times \frac{1}{2} - 8
$$
$$
= \frac{3}{16} - \frac{1}{4} - 9 + 18 - 8 = -\frac{1}{16} + 1 > 0
$$
De esta forma, encontramos una raíz en el intervalo $\left[ 0, \frac{1}{2} \right]$.

$$
x = 1 \implies 3 \times 1 - 2 \times 1 - \cancel{ 36 \times 1 } + \cancel{ 36 \times 1 } - 8 = -7
$$
De esta forma, encontramos una raíz en el intervalo $\left[ \frac{1}{2}, 1 \right]$.

$$
x = \frac{3}{2} \implies 3 \times \frac{81}{16} - 2 \times \frac{27}{8} - 36 \times \frac{9}{4} + 36 \times \frac{3}{2} - 8
$$
$$
= 3 \times \frac{81}{16} - 2 \times \frac{27}{8} - 36 \times \frac{9}{4} + 36 \times \frac{3}{2} - 8 = \frac{135}{16} - \frac{560}{16} = -\frac{425}{16}
$$

$$
x = 3 \implies 3 \times 81 - 2 \times 27 - 36 \times 9 + 36 \times 3 - 8
$$
$$
= 243 - 54 - 324 + 108 - 8 = -135 + 100 = -35
$$
$$
x = \frac{7}{2} \implies 3 \times \frac{2401}{16} - 2 \times \frac{343}{8} - 36 \times \frac{49}{4} + 36 \times \frac{7}{2} - 8
$$
$$
= 3 \times \frac{2401}{16} - 2 \times \frac{343}{8} - 36 \times \frac{49}{4} + 36 \times \frac{7}{2} - 8 = \frac{5831}{16} - 323 = \frac{5831}{16} - \frac{5168}{16} = \frac{663}{16}=
$$
De esta forma, encontramos una raíz en el intervalo $\left[ 3, \frac{7}{2} \right]$.

En conclusión, sabemos que la función $3x^{4} - 2x^{3} - 36x^{2} + 36x - 8$ tiene 4 raíces, las cuales se encuentran cada una en los siguientes intervalos:
$$
\begin{align}
&\left[ -4, -\frac{7}{2} \right] \\
&\left[ 0, \frac{1}{2} \right] \\
&\left[ \frac{1}{2}, 1 \right] \\
&\left[ 3, \frac{7}{2} \right]
\end{align}
$$

### Parte b)
Si analizamos el límite a infinito de un polinomio de grado impar (sin importar cual sea), podemos ver que:
$$
\begin{align}
&\lim_{ x \to - \infty } f(x) = - \infty \\
&\lim_{ x \to + \infty } f(x) = + \infty
\end{align}
$$

En base a esto por definición de límite, existen puntos $x_{0}$ y $x_{1}$ donde la función toma valores negativos y positivos respectivamente. Además, sabemos que todos los polinomios son funciones continuas en todo $\mathbb{R}$. De esta forma, por el teorema de Bolzano, podemos asegurar que existe al menos un $a \in \mathbb{R}$ tal que $f(a) = 0$.



---
## Ejercicio 5.2.7
### Parte a)
Si la función es no negativa, significa que $\forall x \in [a, b], f(x) \geq 0$. Además, como su integral es nula, significa que la parte positiva y negativa son equivalentes. Sin embargo, sabemos que es no negativa, por lo tanto el área de la región negativa es 0.

De esta forma, el área de la región positiva también debe ser 0 para que la integral de la función sea efectivamente nula. Además, como es continua, por el Teorema de Bolzano, si la función toma los valores $a$ y $b$, entonces toma todos los valores intermedios. De esta forma, si la función toma algún valor mayor que 0, tomara todos los valores intermedios también, haciendo que la integral pase a ser un valor positivo.

Por todos los razonamientos anteriores, podemos afirmar que la función $f$ es 0 en el intervalo $[a, b]$.

### Parte b)
#### Parte 1)
Si analizamos el enunciado de manera gráfica, se indica que se puede trazar un rectángulo con base equivalente al tamaño del intervalo ($b - a$), y altura $f(c)$ siendo $c \in [a, b]$. De esta forma, la altura de dicho rectángulo tiene que estar necesariamente entre el máximo y mínimo absoluto de la función ($ínf(f, [a, b]) \leq f(c) \leq sup(f, [a, b])$). Por lo tanto, existe una función constante $f(c)$ que corta en al menos un punto a la función $f$.

Esto tiene sentido ya que la función es continua, lo que significa (según el Teorema de Bolzano) que si la función toma valores $x_{1}$ y $x_{2}$, entonces también toma todos los valores intermedios.

Consideremos $x_{1} = ínf(f, [a, b])$ y $x_{2} = sup(f, [a, b])$.
Sabemos que, como la función es continua, por el Teorema de Bolzano, necesariamente toma todos los valores entre $x_{1}$ y $x_{2}$.

Si consideramos $x_{1}(b - a)$, dicho valor será menor o igual que $\int_{a}^{b} f(t) \space dt$, ya que coincide con la suma inferior de la partición $P = \{ a, b \}$.
En cambio, si consideramos $x_{2}(b - a)$, dicho valor será mayor o igual que $\int_{a}^{b} f(t) \space dt$, ya que coincide con la suma superior de la partición $P = \{ a, b \}$.

En base a esto, sabemos que:
$$
x_{1}(b - a) \leq \int_{a}^{b} f(t) \space dt \leq x_{2}(b - a)
$$
Como vemos, son cotas de la integral.

Por esta razón, y gracias al Teorema de Bolzano mencionado múltiples veces, necesariamente existirá al menos un elemento $c \in [a, b]$ tal que
$$
f(c)(b - a) = \int_{a}^{b} f(t)
$$

#### Parte 2)
Si bien el valor $f(c)$ es único, esto no significa que exista un único $c$ que cumpla con la hipótesis anterior. Puede suceder que en el intervalo $[a, b]$ hayan otros valores $c$ para los cuales $f(c)(b - a) = \int_{a}^{b} f(t) \space dt$ si la función no es estrictamente creciente ni decreciente.

Por ejemplo, si trazamos una función constante $f(c)$, todos los puntos de corte entre dicha función y la función $f$ serán valores de $c$ válidos.

#### Parte 3)
En caso de que $f$ no sea continua, puede no darse que exista un $c \in [a, b]$ tal que $f(c)(b - a) = \int_{a}^{b} f(x) \space dx$. Por ejemplo, consideremos $f : [0, 2] \to \mathbb{R}$ definida por
$$
f : \begin{cases}
\begin{align}
&1 &&\text{si } x \leq 1 \\
&2 &&\text{si } x > 1
\end{align}
\end{cases}
$$
Calculamos su integral:
$$
\int_{0}^{2} f(x) \space dx = \int_{0}^{1} 1 + \int_{1}^{2} 2 = 1 \times (1 - 0) + 2 \times (2 - 1) = 1 + 2 = 3
$$
De esta forma, $\int_{0}^{2} f(x) \space dx = 3$. Intentemos expresarlo de la forma propuesta:
$$
\begin{align}
&f(c)(b - a) = \int_{0}^{2} f(x) \space dx \\
&f(c)(2 - 0) = 3 \\
&2f(c) = 3 \\
&f(c) = \frac{3}{2}
\end{align}
$$
Sin embargo, la función está compuesta por elementos cuya imagen es 1 (para $x \leq 1$) o 2 (para $x > 1$), ninguno tiene imagen $\frac{3}{2}$, rompiendo con la conclusión inicial. Por esta razón, es fundamental que la función sea continua, puesto que puede ser que el valor correspondiente a ese $f(c)$ no forme parte de la función.

Lo podemos visualizar como una función constante con valor $f(c)$. Si la función es continua, interceptará en al menos un punto a dicha constante. Sin embargo, en caso de no ser continua, puede ser que la constante no intercepte a la función en ningún punto.



---
# 5.3 - Teorema de Weierstrass
## Ejercicio 5.3.1


---
## Ejercicio 5.3.5