# 3.1 - Introducción a la definición de integral
## Ejercicio 3.1.1
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 3 - Integración/Imágenes/Ejercicio 3.1.1.png]]
### Parte b)
$$
\int_{1}^{3} x \space dx = 2 \times 1 + \frac{2 \times 2}{2} = 2 + 2 = 4
$$

### Parte c)
$$
\int_{1}^{3} 2x \space dx = 2 \times 2 + \frac{2 \times 4}{2} = 4 + 4 = 8 = 2 \cdot \int_{1}^{3} x \space dx
$$

### Parte d)
$$
\int_{1}^{3} \left( \begin{cases}
\begin{align}
&x &\text{si} \qquad 1 \leq x \leq 2 \\
&x - 2 &\text{si} \qquad 2 < x \leq 3
\end{align}
\end{cases} \right) \space dx = 1 \times 1 + \left( \frac{1 \times 1}{2} \right) \times 2 = 1 + 1 = 2
$$

### Parte h)
$$
\int_{1}^{3} \frac{3}{\lfloor x \rfloor} \space dx = 1 \times 3 + 1 \times \frac{3}{2} = 3 + \frac{3}{2} = \frac{9}{2}
$$

### Parte j)
$$
\int_{1}^{3} (x + [x]) \space dx = \left( \frac{1}{2} \times 1 \right) \times 8 + \left( \frac{\frac{1}{2} \times 1}{2} \right) \times 2 = 4 + \frac{1}{2} = \frac{9}{2} 
$$


ACLARACIÓN: Varios ejercicios realizados en cuadernola.

# 3.4 - Integrabilidad de funciones
## Ejercicio 3.4.1
La implicancia entre las definiciones es la siguiente:
- $a$ implica a $c$.
- $b$ implica a $a$, $c$ y $d$.
- $d$ implica a $c$.
### Parte a)
Como sabemos, las funciones monótonas (crecientes o decrecientes) son integrables, por lo que $f_{1}(x)$ es integrable, por lo que la definición $a$ se verifica para este caso. Lo mismo sucede para $f_{2}(x)$, pues las funciones constantes también son integrables.

Sin embargo, $f_{3}(x)$ no es integrable, ya que, por como está definida, y sabiendo que siempre encontraremos infinitos valores irracionales, siempre se dará que $S^{*}(f_{3}, P) = 1$ y $S_{*}(f_{3}, P) = 0$, por lo que $S^{*}(f_{3}, P) - S_{*}(f_{3}, P) = 1$, sin importar la partición dada. Es así que podemos encontrar valores de $\epsilon > 0$, que no cumplen con la condición establecida (cualquier valor menor que 1).

### Parte c)
A diferencia de la anterior, en esta variación de la definición de integrabilidad, al ser mucho menos restrictiva que la anterior, las tres funciones podrían ser catalogadas como "integrables" al considerarla.

Por ejemplo, para $f_{1}(x) = x$, podemos considerar el intervalo $[0, 10]$ con la partición $P = \{ 0, 5, 10 \}$, sabemos que
$$
\begin{align}
&S_{*}(f_{1}, P) = 0 \times 5 + 5 \times 5 = 25 \\
&S^{*}(f_{1}, P) = 5 \times 5 + 10 \times 5 = 75
\end{align}
$$
De esta manera
$$
S^{*}(f_{1}, P) - S_{*}(f_{1}, P) = 75 - 25 = 50
$$
Es así que podemos establecer un valor mayor o igual a 50 para $\epsilon$, de tal forma que la condición $S^{*}(f, P) - S_{*}(f, P) \leq \epsilon$ se satisfaga.

En el caso de $f_{2}(x) = 0$, sin importar la partición establecida, el resultado siempre será 0 (tanto para la suma inferior como para la superior):
$$
S^{*}(f_{2}, P) - S_{*}(f_{2}, P) = 0 - 0 = 0
$$
Entonces, podemos concluir que para cualquier valor de $\epsilon$, la condición se satisface.

Finalmente, en el caso de $f_{3}(x) = \begin{cases} \begin{align} &1 &&\text{si} & x \in \mathbb{Q} \\ &0 &&\text{si} & x  \not \in \mathbb{Q} \end{align} \end{cases}$, vimos que sin importar la partición establecida, siempre se cumple que $S^{*}(f_{3}, P) - S_{*}(f_{3}, P) = 1$. Por esta razón, basta con establecer un valor de $\epsilon$ que sea mayor que 1 para que la función sea integrable (al menos en esta variante de la definición).

## Ejercicio 3.4.2
Probaremos que una función monótona creciente y acotada es integrable.

Sea $\epsilon > 0$, debemos establecer una partición $P$ para la cual se cumpla la condición $S^{*}(f, P) - S_{*}(f, P) \leq \epsilon$.

Para esto consideraremos una partición equiespaciada $P = \{ a_{0}, a_{1}, \dots, a_{n-1}, a_{n} \}$ de tamaño $n$, siendo $n$ un entero mayor que 1, de tal forma que el tamaño de cada subintervalo es de $\frac{b-a}{n}$.

Es así que cada elemento $a_{i}$ esta definido por:
$$
a_{i} = a + i \times \frac{b-a}{n}
$$

Trabajaremos en el intervalo cerrado $[a, b]$, y como $f$ es monótona creciente, sabemos que $f(a) \leq f(b)$, y en general, para todo valor $a_{i} < a_{j} \implies f(a_{i} \leq f(a_{j}))$.

Entonces, comenzamos a trabajar sobre la definición de una función integrable y lo que esto implica:

Sabemos que en cada subintervalo $[a_{i}, a_{i+1}]$:
$$
\begin{align}
&ínf(f, [a_{i}, a_{i + 1}]) = f(a_{i}) \\
&sup(f, [a_{i}, a_{i + 1}]) = f(a_{i + 1})
\end{align}
$$
De esta manera, podemos calcular la suma inferior y superior:
$$
\begin{align}
&S_{*}(f, P) = \sum_{0}^{n-1} (a_{i+1} - a_{i}) ínf(f, [a_{i}, a_{i + 1}]) = \sum_{0}^{n-1} (a_{i+1} - a_{i}) f(a_{i}) = \sum_{0}^{n-1} (\frac{b-a}{n}) f(a_{i}) \\
&S^{*}(f, P) = \sum_{0}^{n-1} (a_{i+1} - a_{i}) sup(f, [a_{i}, a_{i + 1}]) = \sum_{0}^{n-1} (a_{i+1} - a_{i}) f(a_{i+1}) = \sum_{0}^{n-1} (\frac{b-a}{n}) f(a_{i+1})
\end{align}
$$
Ahora, proseguimos a desarrollar la diferencia de ambos:
$$
S^{*}(f, P) - S_{*}(f, P) = \sum_{0}^{n-1} (\frac{b-a}{n}) f(a_{i+1}) - \sum_{0}^{n-1} (\frac{b-a}{n}) f(a_{i})
$$
$$
= (\frac{b-a}{n}) \sum_{0}^{n-1} f(a_{i+1}) - (\frac{b-a}{n}) \sum_{0}^{n-1} f(a_{i})
$$
Si desarrollamos las sumatorias correspondientes, notaremos que los términos se cancelan, menos el primer término de $\sum_{0}^{n-1} f(a_{i}) = a_{0}$ y el último de $\sum_{0}^{n-1} f(a_{i+1}) = a_{n}$:
$$
= (\frac{b-a}{n}) f(a_{n}) - (\frac{b-a}{n}) f(a_{0})
$$
Además, sabemos que $f(a_{n}) = f(b)$ y $f(a_{0}) = f(a)$:
$$
= (\frac{b-a}{n}) f(b) - (\frac{b-a}{n}) f(a)
$$
Esto también lo podemos factorizar:
$$
= \frac{b-a}{n} \cdot (f(b) - f(a)) < \epsilon
$$
Así, logramos demostrar que la diferencia entre la suma superior e inferior es minúscula (menor a $\epsilon$), por lo tanto las funciones monótonas crecientes son integrables.

## Ejercicio 3.4.6
### Parte a)
Para que $F(x) : [a, b] \to \mathbb{R}$, definida por $F(x) = \int_{a}^{x} f(t) dt$ sea lipschitziana, tenemos que comprobar que su definición es compatible con la condición $|f(x) - f(y)| \leq K |x - y|$. De esta forma (suponiendo que $a \leq x,y \leq b$):

$$
\left| \int_{a}^{x} f(t) dt - \int_{a}^{y} f(t) dt \right| \leq K |x - y|
$$
$$
= \left| \int_{y}^{x} f(t) dt \right| \leq K |x - y|
$$
$$
= \frac{\left| \int_{y}^{x} f(t) dt \right|}{|x - y|} \leq K
$$
Ahora, tenemos que utilizar una propiedad fundamental: toda función integrable en un intervalo cerrado $[a,b]$ está acotada. Como $f$ es integrable, entonces existe un número $M > 0$ tal que $|f(t)| \leq M$ para todo $t \in [a, b]$.

Supongamos que $y < x$. Usando la propiedad de la integral del valor absoluto:
$$
|F(x) - F(y)| = \left| \int_{y}^{x} f(t) dt \right| \leq \int_{y}^{x} |f(t)| dt
$$
Como sabemos que $|f(t)| \leq M$ para todo $t$:
$$
\int_{y}^{x} |f(t)| dt \leq \int_{y}^{x} M dt = M(x - y)
$$
Entonces, tenemos que:
$$
|F(x) - F(y)| \leq M |x - y|
$$
En conclusión, demostramos que existe un valor para $K$ tal que $|f(x) - f(y)| \leq K |x - y|$, por lo que la función es lipschitziana.

### Parte b)
Para probar que una función lipschitziana es integrable, tenemos que probar que si función cumple que existe un $K > 0$, tal que para todo par de puntos $x, y \in \mathbb{R}$ se verifica que $|f(x) - f(y)| \leq K |x - y|$, entonces es integrable.

En este caso, desarrollaremos la fórmula de suma superior e inferior para $x$ e $y$, con tal de relacionarla a la desigualdad anterior:

NO LO PUDE SEGUIR

### Parte c)
Probar que si $f: \mathbb{R} \to \mathbb{R}$ es lipschitziana no negativa, y $a, b \in \mathbb{R}$, con $a < b$, se cumple que.
$$
\int_{a}^{b} f(t) dt = 0 \implies f(x) = 0 \qquad \forall x \in [a, b]
$$
Como $\int_{a}^{b} f(t) dt = 0$, entonces deducimos que existe una partición $P$, tal que $S_{*}(f, P) = S^{*}(f, P) = 0$. Sin embargo, como la función es no negativa, sabemos que $\forall x \in \mathbb{R}, f(x) \geq 0$, por lo tanto:
- el ínfimo de cada subintervalo es 0.
- el supremo de cada subintervalo es 0.
Es así que $\forall x \in \mathbb{R}, f(x) = 0$.

Esto satisface la condición relacionada a las funciones lipschitzianas, sobre la existencia de un $K > 0$, tal que para todo par de puntos $x, y \in \mathbb{R}$ se verifica que $|f(x) - f(y)| \leq K |x - y|$. De hecho, 

Consideraremos el enunciado para $f$: existe un $K > 0$, tal que para todo par de puntos $x, y \in \mathbb{R}$ se verifica que $|f(x) - f(y)| \leq K |x - y|$.

# 3.5 - Cambio de variable lineal
## Ejercicio 3.5.1
### Parte a y b)
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 3 - Integración/Imágenes/Ejercicio 3.5.1.png]]

## Ejercicio 3.5.3
### Parte a)
Sea $\log (x) = \int_{1}^{x} \frac{1}{t} dt$.
Para que $\log(x)$ sea creciente, se tiene que cumplir que $\forall x, y \in \mathbb{R}^{+}, x \leq y \implies f(x) \leq f(y)$.
Por la definición de la función:
$$
\log(x) = \int_{1}^{x} \frac{1}{t} dt
$$
Si tomamos dos valores $a$ y $b$, tal que $a \leq b$, por la definición anterior, y en base a la función $\frac{1}{t}$ (la cual podemos determinar con seguridad que es positiva ya que sabemos que el dominio es $\mathbb{R}^{+}$), podemos asegurar que:
$$
\log(a) = \int_{1}^{a} \frac{1}{t} dt \leq \log(b) = \int_{1}^{b} \frac{1}{t} dt \qquad \forall a, b \in \mathbb{R}^{+}, a \leq b
$$
De esta forma, determinamos que la función es creciente para cualquier intervalo $[a, b]$.

Para determinar las raíces de dicha función, basta con estudiar su definición:
$$
\log(x) = \int_{1}^{x} \frac{1}{t} dt
$$
Como la función en un punto $x$ está dada por la integral en el intervalo entre 1 y $x$, tenemos tres casos posibles:
1. $x < 0$
En este caso, la integral será negativa, puesto que es necesario invertir los extremos:
$$
\log(x) = \int_{x}^{1} \frac{1}{t} dt = - \int_{1}^{x^{-1}} \frac{1}{t} dt < 0 \qquad \forall x < 0
$$
2. $x > 0$
Aquí, la integral será positiva, ya que no es necesario realizar modificaciones de ningún tipo para determinar la integral en el intervalo dado:
$$
\log(x) = \int_{1}^{x} \frac{1}{t} dt > 0 \qquad \forall x > 0
$$
3. $x = 0$
Este caso puede ser determinado tomando en cuenta como se calcula el límite, ya que al tener dos extremos iguales, la integral en el intervalo dado ($[1,1]$) es 0:
$$
\log(1) = \int_{1}^{1} \frac{1}{t} dt = 0 \qquad \text{con } x = 0
$$

En conclusión, la única raíz de la función logaritmo es 1.

### Parte b)
$$
\log(n (a - 1) + 1) \leq n \log(a)
$$
$$
\log(n (a - 1) + 1) \leq \log(a^{n})
$$
Ya que $\log(x)$ es creciente, $a \geq 1 \implies \log(a) \geq 0$, para que $\log(n (a - 1) + 1) \leq \log(a^{n})$ sea verdadera, tiene que cumplirse que $n (a - 1) + 1 \leq a^{n}$:
$$
n (a - 1) + 1 \leq a^{n}
$$
Esta desigualdad se cumple por la desigualdad de Bernoulli:
$$
a^{n} = (1 + (a - 1))^{n} \geq 1 + n(a - 1)
$$

De esta forma, el enunciado es verdadero.

También puede demostrarse por inducción, aunque no ha sido vista en el curso.

### Parte c)
$$
\log(a) = \int_{1}^{a} \frac{1}{t} dt
$$
$$
\log(ax) = \int_{1}^{ax} \frac{1}{t} dt
$$
Sabiendo que $\log(x) - \log(y) = \log\left( \frac{x}{y} \right)$, entonces:
$$
\log(ax) - \log(x) = \int_{1}^{ax} \frac{1}{t} dt - \int_{1}^{x} \frac{1}{t} dt
$$
$$
\log\left( \frac{ax}{x} \right) = \int_{x}^{ax} \frac{1}{t} dt
$$
$$
\log(x) = \int_{x}^{ax} \frac{1}{t} dt
$$

Para generalizar:
$$
\log(x) + \log(y) = \log(xy)?
$$

$$
\begin{align}
&\log (x) = \int_{1}^{x} \frac{1}{t} dt \\
&\log (y) = \int_{1}^{y} \frac{1}{t} dt
\end{align}
$$
En base a lo anterior, podemos expresar a $\log(x)$ como:
$$
\log(x) = \int_{y}^{xy} \frac{1}{t} dt
$$
Ahora, adicionamos $\log(y)$ a la izquierda y su integral correspondiente a la derecha:
$$
\log(x) + \log(y) = \int_{y}^{xy} \frac{1}{t} dt + \int_{1}^{y} \frac{1}{t} dt = \int_{1}^{xy} \frac{1}{t} dt = \log(xy)
$$
Así, concluimos que:
$$
\log(xy) = \log(x) + \log(y)
$$

## Ejercicio 3.5.4
### Parte a)

Conocemos la fórmula para calcular el área de un circulo de radio $r$:
$$
A_{r} = \pi \times r^{2}
$$
De esta manera, el área de un círculo de radio 1 equivale a:
$$
A_{1} = \pi \times 1^{2} = \pi
$$
De esta manera, podemos expresar la fórmula $A_{r}$ como el producto de el área de un círculo de radio 1 ($\pi$) y $r^{2}$:
$$
A_{r} = r^{2} \times A_{1} (= r^{2} \times \pi)
$$
De esta manera, podemos expresar lo siguiente:

SEGÚN EL LIBRO, ESTE TEMA AÚN NO LO HEMOS DADO.

# 3.6 - Cálculo de integrales
## Ejercicio 3.6.1
### Parte a)
Sabiendo que
$$
\begin{align}
&\int_{-1}^{1} h(t) dt = 0 \\
&\int_{-1}^{3} h(t) dt = 6
\end{align}
$$
calcular
$$
\int_{1}^{3} h(t) dt
$$

==ACLARACIÓN==: Sabiendo que $a \leq b \leq c$:
$$
\int_{a}^{c} f(t) dt - \int_{a}^{b} f(t) dt = \int_{b}^{c} f(t) dt
$$
Entonces:
$$
\int_{1}^{3} h(t) dt = \int_{-1}^{3} h(t) dt - \int_{-1}^{1} h(t) dt = 6 - 0 = 6
$$
De esta forma:
$$
\int_{1}^{3} h(t) dt = 6
$$

### Parte b)
Sabiendo que
$$
\begin{align}
&\int_{2}^{8} f(t) dt = 20 \\
&\int_{4}^{8} f(t) dt = -12
\end{align}
$$
calcular
$$
\int_{2}^{4} f(t) dt
$$

==ACLARACIÓN==: Sabiendo que $a \leq b \leq c$:
$$
\int_{a}^{c} f(t) dt - \int_{b}^{c} f(t) dt = \int_{a}^{b} f(t) dt
$$
Entonces:
$$
\int_{2}^{4} f(t) dt = \int_{2}^{8} f(t) dt - \int_{4}^{8} f(t) dt = 20 - (-12) = 20 + 12 = 32
$$
De esta forma:
$$
\int_{2}^{4} h(t) dt = 32
$$

## Ejercicio 3.6.2
### Parte a)
$$
\int_{2}^{2} g(x) dx = 0
$$
==ACLARACIÓN==: para cualquier integral:
$$
\int_{a}^{a} f(x) dx = 0
$$

### Parte b)
$$
\int_{5}^{1} f(x) dx = - \int_{1}^{5} f(x) dx = - (6) = -6
$$
Entonces:
$$
\int_{5}^{1} f(x) dx = -6
$$
==ACLARACIÓN==: para cualquier integral:
$$
\int_{b}^{a} f(x) dx = - \int_{a}^{b} f(x) dx
$$

### Parte c)
$$
\int_{1}^{2} 3 f(x) dx = 3 \cdot \int_{1}^{2} f(x) dx = 3 \times (-4) = -12
$$
Entonces:
$$
\int_{1}^{2} 3 f(x) dx = -12
$$
==ACLARACIÓN==: para cualquier integral:
$$
\int_{a}^{b} \alpha f(x) dx = \alpha \cdot \int_{a}^{b} f(x) dx
$$

### Parte d)
$$
\int_{2}^{5} f(x) dx = \int_{1}^{5} f(x) dx - \int_{1}^{2} f(x) dx = 6 - (-4) = 6 + 4 = 10
$$
Entonces:
$$
\int_{2}^{5} f(x) dx = 10
$$

### Parte e)
$$
\int_{1}^{5} (f(x) - g(x)) dx = \int_{1}^{5} f(x) dx - \int_{1}^{5} g(x) dx = 6 - 8 = -2
$$
Entonces:
$$
\int_{1}^{5} (f(x) - g(x)) dx = -2
$$

### Parte f)
$$
\int_{1}^{5} (4f(x) - g(x)) dx = \int_{1}^{5} 4f(x) dx - \int_{1}^{5} g(x) dx = 4 \cdot \int_{1}^{5} f(x) dx - \int_{1}^{5} g(x) dx = 4 \times 6 - 8 = 24 - 8 = 16
$$
Entonces:
$$
\int_{1}^{5} (4f(x) - g(x)) dx = 16
$$

## Ejercicio 3.6.4
### Parte a)
$$
\int_{1}^{4} 3x - 2 \space dx = \int_{1}^{4} 3x \space dx - \int_{1}^{4} 2 \space dx
$$
$$
\begin{align}
&\int_{1}^{4} 3x \space dx = 3 \cdot \int_{1}^{4} x \space dx = 3 \times \frac{4^{2} - 1^{2}}{2} = 3 \times \frac{15}{2} = \frac{45}{2} \\
&\int_{1}^{4} 2 \space dx = 2 \cdot \int_{1}^{4} 1 \space dx = 2 (4 - 1) = 2 \times 3 = 6
\end{align}
$$
$$
\implies \int_{1}^{4} 3x \space dx - \int_{1}^{4} 2 \space dx = \frac{45}{2} - 6 = \frac{45}{2} - \frac{12}{2} = \frac{33}{2}
$$
En conclusión:
$$
\int_{1}^{4} 3x - 2 \space dx = \frac{33}{2}
$$
### Parte d)
$$
\int_{0}^{2} 2x^{2} + x - 3 \space dx = \int_{0}^{2} 2x^{2} \space dx + \int_{0}^{2} x \space dx - \int_{0}^{2} 3 \space dx
$$
$$
\begin{align}
&\int_{0}^{2} 2x^{2} \space dx = 2 \cdot \int_{0}^{2} x^{2} \space dx = 2 \times \frac{2^{3} - 0^{3}}{3} = 2 \times \frac{8}{3} = \frac{16}{3} \\
&\int_{0}^{2} x \space dx = \frac{2^{2} - 0^{2}}{2} = \frac{4}{2} = 2 \\
&\int_{0}^{2} 3 \space dx = 3 \cdot \int_{0}^{2} 1 \space dx = 3 (2 - 0) = 3 \times 2 = 6
\end{align}
$$
$$
\implies \int_{0}^{2} 2x^{2} \space dx + \int_{0}^{2} x \space dx - \int_{0}^{2} 3 \space dx = \frac{16}{3} + 2 - 6 = \frac{16}{3} + \frac{6}{3} - \frac{18}{3} = \frac{4}{3}
$$
En conclusión:
$$
\int_{0}^{2} 2x^{2} + x - 3 \space dx = \frac{4}{3}
$$

### Parte g)
$$
\int_{0}^{2} (u + 3)(u + 1) \space du = \int_{0}^{2} u^{2} + 4u + 3 \space du = \int_{0}^{2} u^{2} \space du + \int_{0}^{2} 4u \space du + \int_{0}^{2} 3 \space du
$$
$$
\begin{align}
&\int_{0}^{2} u^{2} \space du = \frac{2^{3} - 0^{3}}{3} = \frac{8}{3} \\
&\int_{0}^{2} 4u \space du = 4 \cdot \int_{0}^{2} u \space du = 4 \times \frac{2^{2} - 0^{2}}{2} = 4 \times \frac{4}{2} = 4 \times 2 = 8 \\
&\int_{0}^{2} 3 \space du = 3 \cdot \int_{0}^{2} 1 \space du = 3 \times (2 - 0) = 3 \times 2 = 6
\end{align}
$$
$$
\implies \int_{0}^{2} u^{2} \space du + \int_{0}^{2} 4u \space du + \int_{0}^{2} 3 \space du = \frac{8}{3} + 8 + 6 = \frac{8}{3} + \frac{24}{3} + \frac{18}{3} = \frac{50}{3}
$$
En conclusión:
$$
\int_{0}^{2} (u + 3)(u + 1) \space du = \frac{50}{3}
$$

## Ejercicio 3.6.5
### Parte b)
$$
\int_{-4}^{4} \frac{r^{71}}{4} \space dr = \frac{1}{4} \cdot \int_{-4}^{4} r^{71} \space dr = \frac{1}{4} \times \frac{4^{72} - (-4)^{72}}{72}
$$
Como $4^{72} = (-4)^{72}$, ya que 72 es par, podemos deducir que:
$$
\frac{1}{4} \times \frac{4^{72} - (-4)^{72}}{72} = \frac{1}{4} \times \frac{0}{72} = \frac{1}{4} \times 0 = 0
$$
En conclusión:
$$
\int_{-4}^{4} \frac{r^{71}}{4} \space dr = 0
$$
==ACLARACIÓN==: Podemos generalizar que:
$$
\int_{-a}^{a} x^{y} \space dx = 0 \qquad \text{si } y \text{ es impar}
$$

## Parte d)
$$
\int_{0}^{2\pi} \sin(kt) + 5 \space dt, k \in \mathbb{N}
$$
$$
= \int_{0}^{2\pi} \sin(kt) \space dt + \int_{0}^{2\pi} 5 \space dt = \int_{0}^{2\pi} \sin(kt) \space dt + 5 \cdot \int_{0}^{2\pi} 1 \space dt
$$
$$
\begin{align}
&\int_{0}^{2\pi} \sin(kt) \space dt = 0 \\
&5 \cdot \int_{0}^{2\pi} 1 \space dt = 5 \times (2\pi - 0) = 5 \times 2\pi = 10\pi
\end{align}
$$
Como $k \in \mathbb{N}$ el resultado de $\sin(kt)$ siempre será una o múltiples vueltas al circulo trigonométrico (ya que el intervalo considerado es $[0, 2\pi]$). De esta forma, la parte positiva siempre se anulara con la positiva, siendo la integral 0.
$$
\implies \int_{0}^{2\pi} \sin(kt) \space dt + 5 \cdot \int_{0}^{2\pi} 1 \space dt = 0 + 10\pi = 10\pi
$$
En conclusión:
$$
\int_{0}^{2\pi} \sin(kt) + 5 \space dt, k \in \mathbb{N} = 10\pi
$$

### Parte f)
$$
\int_{-1}^{1} \tan(x) \space dx
$$
Considerando la función $\tan(x)$ en el intervalo $[-1, 1]$, en base a la definición de la misma ($\tan(\alpha) = \frac{\sin(\alpha)}{\cos(\alpha)}$). De esta forma:
- Cuando $\sin(\alpha)$ tiende a 0, $\tan(\alpha)$ tiende a 0.
- Cuando $\cos(\alpha)$ tiende a 0, $\tan(\alpha)$ tiende a $+\infty$ (si $\sin(\alpha)$ y $\cos(\alpha)$ tienen el mismo signo), o $-\infty$ (si $\sin(\alpha)$ y $\cos(\alpha)$ tienen diferente signo).

Como el intervalo analizado es $[-1, 1]$, estudiaremos lo que sucede en la función en los puntos -1, 0 y 1 en $\sin$ y $\cos$:

1. Caso $x = -1$
En este caso, como el punto está debajo del eje y considerando el circulo trigonométrico, $sen(-1) < 0$ y $\cos(-1) > 0$

2. Caso $x = 0$
Aquí, como el punto se encuentra sobre la recta x (punto $(1,0)$), $\cos(0) = 1$ (coordenada x) y $sen(0) = 0$ (coordenada y). Por esta razón, $\tan(0) = 0$

3. Caso $x = 1$
En este caso, como el punto está encima del eje y considerando el circulo trigonométrico (espejado al caso $x = -1$), $sen(1) > 0$ y $\cos(1) > 0$, además de que $sen(1) = -sen(-1)$ y $\cos(1) = \cos(-1)$.

Como podemos ver:
$$
\begin{align}
&\tan(-1) = -\tan(1) \\
&\tan(0) = 0 \\
&\tan(1) = -\tan(-1)
\end{align}
$$
De esta forma, concluimos que la función está "espejada" con respecto al eje x, por lo que $\int_{-1}^{0} \tan(x) \space dx = - \int_{0}^{1} \tan(x) \space dx$

En conclusión:
$$
\int_{-1}^{1} \tan(x) \space dx = \int_{-1}^{0} \tan(x) \space dx + \int_{0}^{1} \tan(x) \space dx = 0
$$

## Ejercicio 3.6.6
### Parte b)
$$
\int_{2}^{3} \frac{1}{2x + 3} \space dx
$$
Considerando que:
$$
\frac{1}{2x + 3} = \frac{1}{2\left( x + \frac{3}{2} \right)} = \frac{1}{2} \times \frac{1}{x + \frac{3}{2}}
$$
$$
\int_{2}^{3} \frac{1}{2x + 3} \space dx = \frac{1}{2} \cdot \int_{2}^{3} \frac{1}{x + \frac{3}{2}} \space dx
$$
==Por la propiedad de invarianza por traslación==: si desplazamos una función horizontalmente, el área bajo la curva no cambia, siempre que ajustemos los límites de integración:
$$
\int_{a}^{b} f(t - p) \space dt = \int_{a - p}^{b - p} f(t) \space dt
$$
De esta forma:
$$
\frac{1}{2} \cdot \int_{2}^{3} \frac{1}{x + \frac{3}{2}} \space dx = \frac{1}{2} \cdot \int_{2 + \frac{3}{2} = \frac{7}{2}}^{3 + \frac{3}{2} = \frac{9}{2}} \frac{1}{x} \space dx
$$
Ahora, podemos aplicar el logaritmo:
$$
\int_{2 + \frac{3}{2} = \frac{7}{2}}^{3 + \frac{3}{2} = \frac{9}{2}} \frac{1}{x} \space dx = \int_{1}^{\frac{9}{2}} \frac{1}{x} \space dx - \int_{1}^{\frac{7}{2}} \frac{1}{x} \space dx = \log \left( \frac{9}{2} \right) - \log \left( \frac{7}{2} \right)
$$
$$
\log \left( \frac{9}{2} \right) - \log \left( \frac{7}{2} \right) = \log\left( \frac{\frac{9}{2}}{\frac{7}{2}} \right) = \log \left( \frac{9 \times 2}{2 \times 7} \right) = \log \left( \frac{18}{14} \right) = \log \left( \frac{9}{7} \right)
$$
$$
\implies \int_{2}^{3} \frac{1}{2x + 3} \space dx = \frac{1}{2} \cdot \int_{2}^{3} \frac{1}{x + \frac{3}{2}} \space dx = \frac{1}{2} \times \log \left( \frac{9}{7} \right) = \log \left( \left( \frac{9}{7} \right)^{\frac{1}{2}} \right) = \log \left( \frac{\sqrt{ 9 }}{\sqrt{ 7 }} \right) = \log \left( \frac{3}{\sqrt{ 7 }} \right)
$$
En conclusión:
$$
\int_{2}^{3} \frac{1}{2x + 3} \space dx = \log \left( \frac{3}{\sqrt{ 7 }} \right)
$$

### Parte f)
$$
\int_{0}^{2} \frac{3x - 2}{2x - 10} \space dx = \int_{0}^{2} \frac{\frac{3}{2}(2x - 10) + 13}{2x - 10} dx = \int_{0}^{2} \frac{\frac{3}{2}(2x - 10) + 13}{2x - 10} dx 
$$
$$
= \int_{0}^{2} \frac{\frac{3}{2}\cancel{ (2x - 10) }}{\cancel{ 2x - 10 }} + \frac{13}{2x - 10} dx = \int_{0}^{2} \frac{3}{2} + \frac{13}{2x - 10} dx = \int_{0}^{2} \frac{3}{2} \space dx + \int_{0}^{2} \frac{13}{2x - 10} \space dx
$$
$$
\begin{align}
&\int_{0}^{2} \frac{3}{2} dx = \frac{3}{2} \cdot \int_{0}^{2} 1 \space dx = \frac{3}{2} \times (2 - 0) = \frac{3}{2} \times 2 = 3 \\
&\int_{0}^{2} \frac{13}{2x - 10} \space dx = \int_{0}^{2} \frac{13}{2(x - 5)} \space dx = \frac{13}{2} \cdot \int_{0}^{2} \frac{1}{x - 5} \space dx = \frac{13}{2} \cdot \int_{0 - 5}^{2 - 5} \frac{1}{x} \space dx = \frac{13}{2} \cdot \int_{-5}^{-3} \frac{1}{x} \space dx
\end{align}
$$
Podemos considerar que la función $\frac{1}{t}$ está en "espejo" para resolver el problema utilizando el logaritmo y los valores mayores que 0, pero estableciendo un valor negativo.

$$
\frac{13}{2} \cdot \int_{-5}^{-3} \frac{1}{x} \space dx = \frac{13}{2} \left(- \int_{3}^{5} \frac{1}{x} \space dx \right) = -\frac{13}{2} \left(\int_{1}^{5} \frac{1}{x} \space dx - \int_{1}^{3} \frac{1}{x} \space dx \right) = -\frac{13}{2} \left( \log(5) - \log(3) \right)
$$
$$
= -\frac{13}{2} \cdot \log\left( \frac{5}{3} \right) = - \log\left( \left( \frac{5}{3} \right)^{\frac{13}{2}} \right)
$$
$$
\implies \int_{0}^{2} \frac{3}{2} \space dx + \int_{0}^{2} \frac{13}{2x - 10} \space dx = 3 - \log\left( \left( \frac{5}{3} \right)^{\frac{13}{2}} \right)
$$

### Parte f)
$$
\int_{1}^{4} \frac{\pi x + 2}{e + x} \space dx = \int_{1}^{4} \frac{ \pi(e + x) + 2 -\pi e}{e + x} \space dx = \int_{1}^{4} \frac{ \pi\cancel{ (e + x) }}{\cancel{ e + x }} + \frac{2 - \pi e}{e + x} \space dx = \int_{1}^{4} \pi + \frac{2 - \pi e}{e + x} \space dx
$$
$$
= \int_{1}^{4} \pi dx + \int_{1}^{4} \frac{2 - \pi e}{e + x} \space dx
$$
$$
\begin{align}
&\int_{1}^{4} \pi dx = \pi \cdot \int_{1}^{4} 1 dx = \pi \times (4 - 1) = \pi \times 3 = 3 \pi \\
&\int_{1}^{4} \frac{2 - \pi e}{e + x} \space dx = (2 - \pi e) \cdot \int_{1}^{4} \frac{1}{e + x} \space dx = (2 - \pi e) \cdot \int_{1 + e}^{4 + e} \frac{1}{x} \space dx
\end{align}
$$
$$
= (2 - \pi e) \cdot \left( \int_{1}^{4 + e} \frac{1}{x} \space dx - \int_{1}^{1 + e} \frac{1}{x} \space dx \right) = (2 - \pi e) \cdot \left( \log(4+e) - \log(1+e) \right)
$$
$$
= (2 - \pi e) \cdot \log\left( \frac{4+e}{1+e} \right) = \log\left( \left( \frac{4+e}{1+e} \right)^{2 - \pi e} \right)
$$
$$
\implies \int_{1}^{4} \pi dx + \int_{1}^{4} \frac{2 - \pi e}{e + x} \space dx = 3\pi + \log\left( \left( \frac{4+e}{1+e} \right)^{2 - \pi e} \right)
$$

## Ejercicio 3.6.7
### Parte a)
Según la igualdad provista:
$$
\int_{2}^{5} \frac{1}{1 - x^{2}} \space dx = \int_{2}^{5} \frac{1}{2(1 - x)} + \frac{1}{2(1 + x)} \space dx = \int_{2}^{5} \frac{1}{2(1 - x)} dx + \int_{2}^{5} \frac{1}{2(1 + x)} \space dx
$$
$$
\begin{align}
&\int_{2}^{5} \frac{1}{2(1 - x)} \space dx = \frac{1}{2} \cdot \int_{2}^{5} \frac{1}{1 - x} dx = -\frac{1}{2} \cdot \int_{2}^{5} \frac{1}{-1 + x} \space dx = -\frac{1}{2} \cdot \int_{2 - 1}^{5 - 1} \frac{1}{x} \space dx = -\frac{1}{2} \cdot \int_{1}^{4} \frac{1}{x} \space dx \\
&\int_{2}^{5} \frac{1}{2(1 + x)} \space dx = \frac{1}{2} \cdot \int_{2}^{5} \frac{1}{1 + x} \space dx = \frac{1}{2} \cdot \int_{2 + 1}^{5 + 1} \frac{1}{x} \space dx = \frac{1}{2} \cdot \int_{3}^{6} \frac{1}{x} \space dx = \frac{1}{2} \cdot \left( \int_{1}^{6} \frac{1}{x} \space dx - \int_{1}^{3} \frac{1}{x} \space dx \right)
\end{align}
$$
$$
\begin{align}
&-\frac{1}{2} \cdot \int_{1}^{4} \frac{1}{x} \space dx = -\frac{1}{2} \cdot \log(4) = \log\left( 4^{-\frac{1}{2}} \right) = \log\left( \frac{1}{4^{\frac{1}{2}}} \right) = \log\left( \frac{1}{2} \right) \\
&\frac{1}{2} \cdot \left( \int_{1}^{6} \frac{1}{x} \space dx - \int_{1}^{3} \frac{1}{x} \space dx \right) = \frac{1}{2} \cdot \left( \log(6) - \log(3) \right) = \frac{1}{2} \cdot \log \left( \frac{6}{3} \right) = \frac{1}{2} \cdot \log \left( 2 \right) = \log \left( 2^{\frac{1}{2}} \right) = \log \left( \sqrt{ 2 } \right)
\end{align}
$$
$$
\implies \int_{2}^{5} \frac{1}{2(1 - x)} dx + \int_{2}^{5} \frac{1}{2(1 + x)} \space dx = \log\left( \frac{1}{2} \right) + \log(\sqrt{ 2 }) = \log\left( \frac{\sqrt{ 2 }}{2} \right) 
$$

### Parte b)
$$
\frac{1}{(x - \mu_{1})(x - \mu_{2})} = \frac{\alpha}{x - \mu_{1}} + \frac{\beta}{(x - \mu_{2})}
$$
Procedimiento:
$$
\frac{1}{(x - \mu_{1})(x - \mu_{2})} = \frac{\alpha}{x - \mu_{1}} + \frac{\beta}{(x - \mu_{2})}
$$
Establecemos un denominador común para todas las fracciones:
$$
\frac{1}{(x - \mu_{1})(x - \mu_{2})} = \frac{\alpha (x - \mu_{2})}{(x - \mu_{1})(x - \mu_{2})} + \frac{\beta (x - \mu_{1})}{(x - \mu_{2})(x - \mu_{1})}
$$
$$
\implies 1 = \alpha (x - \mu_{2}) + \beta (x - \mu_{1})
$$
$$
1 = \alpha x - \alpha \mu_{2} + \beta x - \beta \mu_{1} = x(\alpha + \beta) - \alpha \mu_{2} - \beta \mu_{1}
$$
$$
1 = x(\alpha + \beta) - \alpha \mu_{2} - \beta \mu_{1}
$$
Como a la izquierda no hay $x$, deducimos que el coeficiente es 0, por lo que:
$$
\alpha + \beta = 0 \implies \alpha = -\beta \text{ y } \beta = -\alpha
$$
De esta forma nos queda:
$$
- \alpha \mu_{2} - \beta \mu_{1} = 1
$$
Tomando como referencia que $\beta = -\alpha$:
$$
- \alpha \mu_{2} - (- \alpha) \mu_{1} = -\alpha \mu_{2} + \alpha \mu_{1} = 1
$$
$$
\alpha(\mu_{1} - \mu_{2}) = 1
$$
$$
\alpha = \frac{1}{\mu_{1} - \mu_{2}}
$$
Ahora, tomando en cuenta que $\beta = -\alpha$ y $\alpha = \frac{1}{\mu_{1} - \mu_{2}}$:
$$
\beta = -\frac{1}{\mu_{1} - \mu_{2}} = \frac{1}{\mu_{2} - \mu_{1}}
$$

Volviendo al principio:
$$
\frac{1}{(x - \mu_{1})(x - \mu_{2})} = \frac{\alpha}{x - \mu_{1}} + \frac{\beta}{x - \mu_{2}}
$$
Ahora podemos sustituir $\alpha$ y $\beta$ por los valores obtenidos:
$$
\frac{1}{(x - \mu_{1})(x - \mu_{2})} = \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{1}} - \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{2}}
$$

Ahora, podemos desarrollar fácilmente la integral especificada:

$$
\int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{1}{(x - \mu_{1})(x - \mu_{2})} \space dx = \int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{1}} - \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{2}} \space dx = \int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{1}} \space dx - \int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{2}} \space dx
$$
$$
= \frac{1}{\mu_{1} - \mu_{2}} \cdot \left( \int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{1}{x - \mu_{1}} \space dx - \int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{1}{x - \mu_{2}} \space dx \right)
$$
$$
\begin{align}
&\int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{1}{x - \mu_{2}} \space dx = \int_{\cancel{ \mu_{2} } + 1 - \cancel{ \mu_{2} }}^{\cancel{ \mu_{2} } + 5 - \cancel{ \mu_{2} }} \frac{1}{x} \space dx = \int_{1}^{5} \frac{1}{x} \space dx = \log(5) \\

&\int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{1}{x - \mu_{1}} \space dx = \int_{\mu_{2} + 1  - \mu_{1}}^{\mu_{2} + 5  - \mu_{1}} \frac{1}{x} \space dx = \int_{1}^{\mu_{2} + 5  - \mu_{1}} \frac{1}{x} \space dx - \int_{1}^{\mu_{2} + 1  - \mu_{1}} \frac{1}{x} \space dx
\end{align}
$$
$$
= \log(\mu_{2} + 5 - \mu_{1}) - \log(\mu_{2} + 1 - \mu_{1}) = \log\left( \frac{\mu_{2} + 5 - \mu_{1}}{\mu_{2} + 1 - \mu_{1}} \right)
$$
$$
\implies \int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{1}} \space dx - \int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{2}} \space dx = \log\left( \frac{\mu_{2} + 5 - \mu_{1}}{\mu_{2} + 1 - \mu_{1}} \right) - \log(5) = \log\left( \frac{\mu_{2} + 5 - \mu_{1}}{5(\mu_{2} + 1 - \mu_{1})} \right)
$$
$$
= \log\left( \frac{\mu_{2} + 5 - \mu_{1}}{5\mu_{2} + 5 - 5\mu_{1}} \right)
$$

En conclusión:
$$
\int_{\mu_{2} + 1}^{\mu_{2} + 5} \frac{1}{(x - \mu_{1})(x - \mu_{2})} \space dx = \frac{1}{\mu_{1} - \mu_{2}} \cdot \log\left( \frac{\mu_{2} + 5 - \mu_{1}}{5\mu_{2} + 5 - 5\mu_{1}} \right) = \log\left( \left( \frac{\mu_{2} + 5 - \mu_{1}}{5\mu_{2} + 5 - 5\mu_{1}} \right)^{\frac{1}{\mu_{1} - \mu_{2}}} \right)
$$

Se puede simplificar:
$$
\frac{1}{\mu_{1} - \mu_{2}} \cdot \left( \log\left( \frac{\mu_{2} + 5 - \mu_{1}}{\mu_{2} + 1 - \mu_{1}} \right) - \log(5) \right) = \frac{1}{\mu_{2} - \mu_{1}} \cdot \left( \log(5) - \log \left( \frac{\mu_{2} + 5 - \mu_{1}}{\mu_{2} + 1 - \mu_{1}} \right) \right)
$$
$$
= \frac{1}{\mu_{2} - \mu_{1}} \cdot \log \left( \frac{5(\mu_{2} + 5 - \mu_{1})}{\mu_{2} + 1 - \mu_{1}} \right)
$$

### Parte c)
#### Parte b)
$$
\frac{1}{x^{2} - 5x + 6} = \frac{1}{(x - 2)(x - 3)} = \frac{\alpha}{x - 2} + \frac{\beta}{x - 3}
$$
Considerando que $\frac{1}{(x - \mu_{1})(x - \mu_{2})} = \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{1}} - \frac{\frac{1}{\mu_{1} - \mu_{2}}}{x - \mu_{2}}$:
$$
\implies 1 = \frac{1}{2 - 3} - \frac{1}{2 - 3}
$$
$$
\begin{align}
&\alpha = \frac{1}{2 - 3} = \frac{1}{-1} = -1 \\
&\beta = -\frac{1}{2 - 3} = - \frac{1}{-1} = 1
\end{align}
$$
Entonces, podemos desarrollar la integral especificada:
$$
\int_{4}^{7} \frac{1}{x^{2} - 5x + 6} \space dx = \int_{4}^{7} \frac{1}{(x - 2)(x - 3)} \space dx = \int_{4}^{7} \frac{-1}{x-2} + \frac{1}{x-3} \space dx = -\int_{4}^{7} \frac{1}{x-2} \space dx + \int_{4}^{7} \frac{1}{x-3} \space dx
$$

Calculamos cada una de las partes:
$$
\begin{align}
&\int_{4}^{7} \frac{1}{x-2} \space dx = \int_{4 - 2}^{7 - 2} \frac{1}{x} \space dx = \int_{2}^{5} \frac{1}{x} \space dx = \int_{1}^{5} \frac{1}{x} \space dx - \int_{1}^{2} \frac{1}{x} \space dx = \log(5) - \log(2) = \log\left( \frac{5}{2} \right) \\
&\int_{4}^{7} \frac{1}{x-3} \space dx = \int_{4 - 3}^{7 - 3} \frac{1}{x} \space dx = \int_{1}^{4} \frac{1}{x} \space dx = \log(4)
\end{align}
$$

$$
\implies \int_{4}^{7} \frac{1}{x-2} \space dx - \int_{4}^{7} \frac{1}{x-3} \space dx = - \log\left( \frac{5}{2} \right) + \log(4) = \log\left( \left( \frac{5}{2} \right)^{-1} \right) + \log(4)
$$
$$
= \log\left( \frac{\frac{1}{5}}{\frac{1}{2}} \right) + \log(4) = \log\left( \frac{2}{5} \right) + \log(4) = \log\left( \frac{2}{5} \times 4 \right) = \log \left( \frac{8}{5} \right)
$$

En conclusión:
$$
\int_{4}^{7} \frac{1}{x^{2} - 5x + 6} \space dx = \log \left( \frac{8}{5} \right)
$$

## Ejercicio 3.6.8
Considerando la siguiente propiedad resolveremos los ejercicios de este apartado:
$$
\int_{a}^{b} \sqrt{ t } \space dt = \frac{2}{3}\left( b^{\frac{3}{2}} - a^{\frac{3}{2}} \right) \text{ con } a, b > 0
$$

### Parte b)
$$
\int_{3}^{4} \sqrt{ 2x } \space dx = \int_{3}^{4} \sqrt{ 2 }\sqrt{ x } \space dx = \sqrt{ 2 } \cdot \int_{3}^{4} \sqrt{ x } \space dx
$$
Considerando la propiedad anterior:
$$
\int_{3}^{4} \sqrt{ x } \space dx = \frac{2}{3}\left( 4^{\frac{3}{2}} - 3^{\frac{3}{2}} \right)
$$
$$
\begin{align}
&4^{\frac{3}{2}} = \sqrt{ 4^{3} } = \sqrt{ 64 } = 8 \\
&3^{\frac{3}{2}} = \sqrt{ 3^{3} } = \sqrt{ 27 } = \sqrt{ 3 } \sqrt{ 3 } \sqrt{ 3 } = 3 \sqrt{ 3 }
\end{align}
$$
$$
\implies \frac{2}{3}\left( 4^{\frac{3}{2}} - 3^{\frac{3}{2}} \right) = \frac{2}{3}(8 - 3 \sqrt{ 3 }) = \frac{16}{3} - \frac{6\sqrt{ 3 }}{3} = \frac{16}{3} - 2\sqrt{ 3 }
$$

En conclusión:
$$
\int_{3}^{4} \sqrt{ 2x } \space dx = \sqrt{ 2 } \cdot \left( \frac{16}{3} - 2\sqrt{ 3 } \right) = \frac{16\sqrt{ 2 }}{3} - 2\sqrt{ 3 }\sqrt{ 2 } = \frac{16\sqrt{ 2 }}{3} - 2\sqrt{ 6 }
$$

### Parte f)
$$
\int_{5}^{7} \sqrt{ x - 2 } \space dx
$$
Considerando la propiedad de invarianza por traslación, podemos ajustar los límites de integración de forma correspondiente. Consideremos los extremos del intervalo:
$$
\begin{align}
&f(5) = \sqrt{ 5 - 2 } = \sqrt{ 3 } \\
&f(7) = \sqrt{ 7 - 2 } = \sqrt{ 5 }
\end{align}
$$

De esta forma, y sabiendo además que la función es continua, podemos establecer los nuevos extremos 3 y 5, y cambiar la función $\sqrt{ x - 2 }$ por $\sqrt{ x }$:
$$
\int_{5}^{7} \sqrt{ x - 2 } \space dx = \int_{3}^{5} \sqrt{ x } \space dx = \frac{2}{3}\left( 5^{\frac{3}{2}} - 3^{\frac{3}{2}} \right)
$$
$$
\begin{align}
&5^{\frac{3}{2}} = \sqrt{ 5^{3} } = \sqrt{ 125 } = \sqrt{ 5 \times 5 \times 5 } = \sqrt{ 5 }\sqrt{ 5 }\sqrt{ 5 } = 5\sqrt{ 5 } \\
&3^{\frac{3}{2}} = \sqrt{ 3^{3} } = \sqrt{ 27 } = \sqrt{ 3 \times 3 \times 3 } = \sqrt{ 3 }\sqrt{ 3 }\sqrt{ 3 } = 3\sqrt{ 3 }
\end{align}
$$
$$
\implies \frac{2}{3}\left( 5^{\frac{3}{2}} - 3^{\frac{3}{2}} \right) = \frac{2}{3}(5\sqrt{ 5 } - 3\sqrt{ 3 }) = \frac{10\sqrt{ 5 }}{3} - \frac{6\sqrt{ 3 }}{3} = \frac{10\sqrt{ 5 }}{3} - 2\sqrt{ 3 }
$$

En conclusión:
$$
\int_{5}^{7} \sqrt{ x - 2 } \space dx = \frac{10\sqrt{ 5 }}{3} - 2\sqrt{ 3 }
$$

### Parte h)
En base a todas las propiedades que hemos utilizado anteriormente:
$$
\int_{0}^{5} \sqrt{ 12 - 2x } \space dx = \int_{0 + 12}^{5 + 12} \sqrt{ - 2x } \space dx = \int_{12}^{17} \sqrt{ - 2x } \space dx = -2 \cdot \int_{12}^{17} \sqrt{ x } \space dx = -2 \times \frac{2}{3} \left( 17^{\frac{3}{2}} - 12^{\frac{3}{2}} \right)
$$
$$
\begin{align}
&17^{\frac{3}{2}} = \sqrt{ 17^{3} } = \sqrt{ 17 }\sqrt{ 17 }\sqrt{ 17 } = 17\sqrt{ 17 } \\
&12^{\frac{3}{2}} = \sqrt{ 12^{3} } = \sqrt{ 12 }\sqrt{ 12 }\sqrt{ 12 } = 12\sqrt{ 12 } = 12\sqrt{ 2 }\sqrt{ 2 }\sqrt{ 3 } = 12 \times 2\sqrt{ 3 } = 24\sqrt{ 3 }
\end{align}
$$
$$
\implies \frac{2}{3} \left( 17^{\frac{3}{2}} - 12^{\frac{3}{2}} \right) = \frac{2}{3} (17\sqrt{ 17 } - 24\sqrt{ 3 }) = \frac{34\sqrt{ 17 }}{3} - \frac{48\sqrt{ 3 }}{3} = \frac{34 \sqrt{ 17 }}{3} - 16\sqrt{ 3 }
$$

En conclusión:
$$
\int_{0}^{5} \sqrt{ 12 - 2x } \space dx = -2 \times \left( \frac{34 \sqrt{ 17 }}{3} - 16\sqrt{ 17 } \right) = - \frac{68 \sqrt{ 17 }}{3} + 32 \sqrt{ 3 }
$$

==ATENCIÓN==: LA SOLUCIÓN ES INCORRECTA. A CONTINUACIÓN SE RESUELVE EL EJERCICIO CORRECTAMENTE.

En base a todas las propiedades que hemos utilizado anteriormente:
$$
\int_{0}^{5} \sqrt{ 12 - 2x } \space dx = \int_{0}^{5} \sqrt{ 2(6 - x) } \space dx = \int_{0}^{5} \sqrt{ 2 } \sqrt{ 6 - x } \space dx = \sqrt{ 2 } \cdot \int_{0}^{5} \sqrt{ 6 - x } \space dx
$$
Para quitar el símbolo negativo de la $x$, aplicamos la ==integración en espejo (simetría)==:
$$
\int_{a}^{b} f(x) \space dx = \int_{-b}^{-a} f(-y) \space dy
$$
De esta forma:
$$
\sqrt{ 2 } \cdot \int_{0}^{5} \sqrt{ 6 - x } \space dx = \sqrt{ 2 } \cdot \int_{-5}^{0} \sqrt{ 6 + x } \space dx = \sqrt{ 2 } \cdot \int_{-5 + 6}^{0 + 6} \sqrt{ x } \space dx = \sqrt{ 2 } \cdot \int_{1}^{6} \sqrt{ x } \space dx = \sqrt{ 2 } \cdot \frac{2}{3}\left( 6^{\frac{3}{2}} - 1^{\frac{3}{2}} \right)
$$

$$
\begin{align}
&6^{\frac{3}{2}} = \sqrt{ 6^{3} } = \sqrt{ 6 }\sqrt{ 6 }\sqrt{ 6 } = 6 \sqrt{ 6 } \\
&1^{\frac{3}{2}} = \sqrt{ 1^{3} } = 1
\end{align}
$$
$$
\implies \frac{2}{3} \left( 6^{\frac{3}{2}} - 1^{\frac{3}{2}} \right) = \frac{2}{3} (6\sqrt{ 6 } - 1) = \frac{12\sqrt{ 6 }}{3} - \frac{2}{3} = 4\sqrt{ 6 } - \frac{2}{3}
$$

En conclusión:
$$
\int_{0}^{5} \sqrt{ 12 - 2x } \space dx = \sqrt{ 2 } \times \left( 4\sqrt{ 6 } - \frac{2}{3} \right) = 4 \sqrt{ 6 }\sqrt{ 2 } - \frac{2 \sqrt{ 2 }}{3} = 4\underbrace{ \sqrt{ 2 }\sqrt{ 2 } }_{ =2 }\sqrt{ 3 } - \frac{2 \sqrt{ 2 }}{3} = 8\sqrt{ 3 } - \frac{2 \sqrt{ 2 }}{3}
$$

### Parte i)
$$
\int_{0}^{2} \sqrt{ 15 - 3x } \space dx = \int_{0}^{2} \sqrt{ 3(5 - x) } \space dx = \int_{0}^{2} \sqrt{ 3 }\sqrt{ 5 - x } \space dx = \sqrt{ 3 } \cdot \int_{0}^{2} \sqrt{ 5 - x } \space dx
$$
En base a la integración en espejo (simetría):
$$
= \sqrt{ 3 } \cdot \int_{-2}^{0} \sqrt{ 5 + x } \space dx = \sqrt{ 3 } \cdot \int_{-2 + 5}^{0 + 5} \sqrt{ x } \space dx = \sqrt{ 3 } \cdot \int_{3}^{5} \sqrt{ x } \space dx = \sqrt{ 3 } \times \frac{2}{3}\left( 5^{\frac{3}{2}} - 3^{\frac{3}{2}} \right)
$$
$$
\begin{align}
&5^{\frac{3}{2}} = \sqrt{ 5 }\sqrt{ 5 }\sqrt{ 5 } = 5\sqrt{ 5 } \\
&3^{\frac{3}{2}} = \sqrt{ 3 }\sqrt{ 3 }\sqrt{ 3 } = 3\sqrt{ 3 }
\end{align}
$$
$$
\implies \frac{2}{3}\left( 5^{\frac{3}{2}} - 3^{\frac{3}{2}} \right) = \frac{2}{3}(5 \sqrt{ 5 } - 3 \sqrt{ 3 }) = \frac{10 \sqrt{ 5 }}{3} - \frac{6 \sqrt{ 3 }}{3} = \frac{10 \sqrt{ 5 }}{3} - 2 \sqrt{ 3 }
$$

En conclusión:
$$
\int_{0}^{2} \sqrt{ 15 - 3x } \space dx = \sqrt{ 3 } \times \left( \frac{10 \sqrt{ 5 }}{3} - 2 \sqrt{ 3 } \right) = \frac{10\sqrt{ 5 }\sqrt{ 3 }}{3} - 2 \underbrace{ \sqrt{ 3 } \sqrt{ 3 } }_{ = 3 } = \frac{10\sqrt{ 5 }\sqrt{ 3 }}{3} - 6 = \frac{10\sqrt{ 15 }}{3} - 6
$$

---
## Ejercicio 3.6.9
### Parte a)
$$
\int_{0}^{3} |2u - 2| \space du
$$
Considerando que en el intervalo analizado todos los valores son positivos:
$$
\int_{0}^{3} |2u - 2| \space du = \int_{0}^{1} 2 - 2u \space du + \int_{1}^{3} 2u - 2 \space du
$$
Además, podemos ver que para $u \in [0, 1), 2u - 2 < 0$:
$$
\int_{0}^{1} 2 - 2u \space du = \int_{0}^{1} 2 \space du - \int_{0}^{1} 2u \space du
$$
$$
\begin{align}
&\int_{0}^{1} 2 \space du = 2 \times (1 - 0) = 2 \\
&\int_{0}^{1} 2u \space du = 2 \cdot \int_{0}^{1} u \space du = 2 \times \frac{1^{2} - 0^{2}}{2} = 2 \times \frac{1}{2} = 1
\end{align}
$$
De esta forma:
$$
\int_{0}^{1} 2 - 2u \space du = 2 - 1 = 1
$$


$u \in [1, 3], 2u - 2 \geq 0$:
$$
\int_{1}^{3} 2u - 2 \space du = \int_{1}^{3} 2u \space du - \int_{1}^{3} 2 \space du
$$
$$
\begin{align}
&\int_{1}^{3} 2u \space du = 2 \cdot \int_{1}^{3} u \space du = 2 \times \frac{3^{2} - 1^{2}}{2} = 2 \times \frac{9 - 1}{2} = 2 \times \frac{8}{2} = 2 \times 4 = 8 \\
&\int_{1}^{3} 2 \space du = 2 \times (3 - 1) = 2 \times 2 = 4
\end{align}
$$
De esta forma:
$$
\int_{1}^{3} 2u - 2 \space du = 8 - 4 = 4
$$

En conclusión:
$$
\int_{0}^{3} |2u - 2| \space du = 1 + 4 = 5
$$

### Parte f)
$$
\int_{-3}^{4} |t^{2} - 4| \space dt
$$
Analicemos que sucede en la función $|t^{2} - 4|$ en el intervalo $[-3, 4]$:
- Si $t \leq -2$ o $t \geq 2$ $\implies t^{2} \geq 4$
- Si $-2 < t < 2$ $\implies t^{2} < 4$

En definitiva:
$$
\int_{-3}^{4} |t^{2} - 4| \space dt = \int_{-3}^{-2} t^{2} - 4 \space dt + \int_{-2}^{2} 4 - t^{2} \space dt + \int_{2}^{4} t^{2} - 4 \space dt
$$

Entonces, tenemos tres casos:
1. Caso $t \leq -2$:
$$
\int_{-3}^{-2} t^{2} - 4 \space dt = \int_{-3}^{-2} t^{2} \space dt - \int_{-3}^{-2} 4 \space dt
$$
$$
\begin{align}
&\int_{-3}^{-2} t^{2} \space dt = \frac{(-2)^{3} - (-3)^{3}}{3} = \frac{-8 + 27}{3} = \frac{19}{3} \\
&\int_{-3}^{-2} 4 \space dt = 4 \times \int_{-3}^{-2} 1 \space dt = 4 \times (-2) - (-3) = dt = 4 \times 1 = 4
\end{align}
$$
$$
\implies \int_{-3}^{-2} t^{2} - 4 \space dt = \frac{19}{3} - 4 = \frac{19}{3} - \frac{12}{3} = \frac{7}{3}
$$

2. Caso $t \geq 2$:
$$
\int_{2}^{4} t^{2} - 4 \space dt = \int_{2}^{4} t^{2} \space dt - \int_{2}^{4} 4 \space dt
$$
$$
\begin{align}
&\int_{2}^{4} t^{2} \space dt = \frac{4^{3} - 2^{3}}{3} = \frac{64 - 8}{3} = \frac{56}{3} \\
&\int_{2}^{4} 4 \space dt = 4 \times \int_{2}^{4} 1 \space dt = 4 \times (4 - 2) = 4 \times 2 = 8
\end{align}
$$
$$
\implies \int_{2}^{4} t^{2} - 4 \space dt = \frac{56}{3} - 8 = \frac{56}{3} - \frac{24}{3} = \frac{32}{3}
$$

3. Caso $-2 < t < 2$:
$$
\int_{-2}^{2} 4 - t^{2} \space dt = \int_{-2}^{2} 4 \space dt - \int_{-2}^{2} t^{2} \space dt
$$
$$
\begin{align}
&\int_{-2}^{2} 4 \space dt = 4 \times \int_{-2}^{2} 1 \space dt = 4 \times (2 - (-2)) = 4 \times 4 = 16 \\
&\int_{-2}^{2} t^{2} \space dt = \frac{2^{3} - (-2)^{3}}{3} = \frac{8 - (-8)}{3} = \frac{16}{3}
\end{align}
$$
$$
= \int_{-2}^{2} 4 - t^{2} \space dt = 16 - \frac{16}{3} = \frac{48}{3} - \frac{16}{3} = \frac{32}{3}
$$

Para concluir:
$$
\int_{-3}^{4} |t^{2} - 4| \space dt = \int_{-3}^{-2} t^{2} - 4 \space dt + \int_{-2}^{2} 4 - t^{2} \space dt + \int_{2}^{4} t^{2} - 4 \space dt = \frac{7}{3} + \frac{32}{3} + \frac{32}{3} = \frac{71}{3}
$$

### Parte g)
$$
\int_{1}^{5} \left| \frac{27}{x} - x^{2} \right| \space dx
$$
Vamos a buscar la raíz de $\frac{27}{x} - x^{2}$:
$$
\begin{align}
&\frac{27}{x} - x^{2} = 0 \\
&\frac{27}{x} = x^{2} \\
&27 = x^{3} \implies x = \sqrt[3]{ 27 } = \sqrt[3]{ 3 }\sqrt[3]{ 3 }\sqrt[3]{ 3 } = 3
\end{align}
$$
De esta forma, analizaremos dos casos:
$$
\int_{1}^{5} \left| \frac{27}{x} - x^{2} \right| \space dx = \int_{1}^{3} \frac{27}{x} - x^{2} \space dx + \int_{3}^{5} x^{2} - \frac{27}{x} \space dx
$$

1. Caso 1: $1 \leq x \leq 3$
$$
\int_{1}^{3} \frac{27}{x} - x^{2} \space dx = \int_{1}^{3} \frac{27}{x} \space dx - \int_{1}^{3} x^{2} \space dx
$$
$$
\begin{align}
&\int_{1}^{3} \frac{27}{x} \space dx = 27 \times \int_{1}^{3} \frac{1}{x} \space dx = 27 \times \log(3) = \log(3^{27}) \\
&\int_{1}^{3} x^{2} \space dx = \frac{3^{3} - 1^{3}}{3} = \frac{27 - 1}{3} = \frac{26}{3}
\end{align}
$$
$$
\implies \int_{1}^{3} \frac{27}{x} - x^{2} \space dx = \log(3^{27}) - \frac{26}{3}
$$

2. Caso 2: $3 \leq x \leq 5$
$$
\int_{3}^{5} x^{2} - \frac{27}{x} \space dx = \int_{3}^{5} x^{2} \space dx - \int_{3}^{5} \frac{27}{x} \space dx
$$
$$
\begin{align}
&\int_{3}^{5} x^{2} \space dx = \frac{5^{3} - 3^{3}}{3} = \frac{125 - 27}{3} = \frac{98}{3} \\
&\int_{3}^{5} \frac{27}{x} \space dx = 27 \times \int_{3}^{5} \frac{1}{x} \space dx = 27 \times \left( \int_{1}^{5} \frac{1}{x} \space dx - \int_{1}^{3} \frac{1}{x} \space dx \right) = 27 \times (\log(5) - \log(3)) = 27 \times \log\left( \frac{5}{3} \right) = \log\left( \frac{5^{27}}{3^{27}} \right)
\end{align}
$$
$$
\implies \int_{3}^{5} x^{2} - \frac{27}{x} \space dx = \frac{98}{3} - \log\left( \frac{5^{27}}{3^{27}} \right)
$$

En conclusión:
$$
\int_{1}^{5} \left| \frac{27}{x} - x^{2} \right| \space dx = \log(3^{27}) - \frac{26}{3} + \frac{98}{3} - \log\left( \frac{5^{27}}{3^{27}} \right) = \frac{72}{3} + \log\left( \frac{3^{27}}{\frac{5^{27}}{3^{27}}} \right) = \frac{72}{3} + \log\left( \frac{3^{27} \times 3^{27}}{5^{27}} \right) = 24 + \log\left( \frac{3^{54}}{5^{27}} \right)
$$

---
## Ejercicio 3.6.10
### Parte a)
$$
\int_{1}^{4} [\sqrt{ x }] \space dx
$$
Considerando que $\sqrt{ 1 } = 1$ y $\sqrt{ 4 } = 2$, y sabiendo que calculamos la distancia al entero más cercano, podemos deducir que la función es 0 en 1 y 4.

Ahora, tenemos que ver para que valores de $[1, 4]$ $[\sqrt{ x }] = \frac{1}{2}$.
En este caso, tenemos un único valor: $\frac{9}{4}$

De esta manera, podemos desarrollar lo siguiente:
$$
\int_{1}^{4} [\sqrt{ x }] \space dx = \int_{1}^{\frac{9}{4}} \sqrt{ x } - 1 \space dx + \int_{\frac{9}{4}}^{4} -\sqrt{ x } + 2 \space dx
$$
$$
\begin{align}
&\int_{1}^{\frac{9}{4}} \sqrt{ x } - 1 \space dx = \int_{1}^{\frac{9}{4}} \sqrt{ x } \space dx - \int_{1}^{\frac{9}{4}} 1 \space dx = \frac{2}{3}\left( \frac{9}{4}^{\frac{3}{2}} - 1^{\frac{3}{2}} \right) - \left( \frac{9}{4} - 1 \right) \\
&\int_{\frac{9}{4}}^{4} -\sqrt{ x } + 2 \space dx = -\left( \int_{\frac{9}{4}}^{4} \sqrt{ x } \space dx \right) + \underbrace{ \int_{\frac{9}{4}}^{4} 2 \space dx }_{ 2 \times \int_{\frac{9}{4}}^{4} 1 \space dx } = -\frac{2}{3}\left( 4^{\frac{3}{2}} - \frac{9}{4}^{\frac{3}{2}} \right) + 2 \times \left( 4 - \frac{9}{4} \right)
\end{align}
$$
Calculamos los valores obtenidos:
$$
\begin{align}
&\frac{9}{4}^{\frac{3}{2}} - 1^{\frac{3}{2}} = \frac{\sqrt{ 9^{3} }}{\sqrt{ 4^{3} }} - 1 = \frac{\sqrt{ 9 }\sqrt{ 9 }\sqrt{ 9 }}{\sqrt{ 4 }\sqrt{ 4 }\sqrt{ 4 }} - 1 = \frac{9\sqrt{ 9 }}{4\sqrt{ 4 }} - 1 = \frac{9 \times 3}{4 \times 2} - 1 = \frac{27}{8} - 1 = \frac{19}{8} \\
&4^{\frac{3}{2}} - \frac{9}{4}^{\frac{3}{2}} = 8 - \frac{27}{8} = \frac{64}{8} - \frac{27}{8} = \frac{37}{8}
\end{align}
$$

$$
\begin{align}
&\frac{2}{3}\left( \frac{9}{4}^{\frac{3}{2}} - 1^{\frac{3}{2}} \right) - \left( \frac{9}{4} - 1 \right) = \frac{2}{3} \times \frac{19}{8} - \left( \frac{9}{4} - 1 \right) = \frac{38}{24} - \frac{5}{4} = \frac{19}{12} - \frac{15}{12} = \frac{4}{12} = \frac{1}{3} \\
&-\frac{2}{3}\left( 4^{\frac{3}{2}} - \frac{9}{4}^{\frac{3}{2}} \right) + 2 \times \left( 4 - \frac{9}{4} \right) = -\frac{2}{3} \times \frac{37}{8} + 2 \times \frac{7}{4} = -\frac{74}{24} + \frac{14}{4} = -\frac{37}{12} + \frac{42}{12} = \frac{5}{12}
\end{align}
$$

$$
\implies \int_{1}^{4} [\sqrt{ x }] \space dx = \frac{1}{3} + \frac{5}{12} = \frac{4}{12} + \frac{5}{12} = \frac{9}{12} = \frac{3}{4}
$$

---
## Ejercicio 3.6.11
### Parte a)
Primero, tenemos que encontrar los puntos de intersección entre $f$ y $g$:
$$
\begin{align}
&x^{2} = -2x + 1 \\
&x^{2} + 2x - 1 = 0
\end{align}
$$
De esta forma:
$$
\begin{align}
&a = 1 \\
&b = 2 \\
&c = -1
\end{align}
$$
Aplicamos Bhaskara:
$$
\begin{align}
&x = \frac{-2 \pm \sqrt{ 2^{2} - 4 \times 1 \times (-1) }}{2 \times 1} \\
&x = \frac{-2 \pm \sqrt{ 4 - (-4) }}{2} \\
&x = \frac{-2 \pm \overbrace{ \sqrt{ 8 } }^{ \sqrt{ 2^{3} } = 2\sqrt{ 2 } }}{2} \\
&x_{1} = \frac{-2 + 2\sqrt{ 2 }}{2} = -1 + \sqrt{ 2 } \\
&x_{2} = \frac{-2 - 2\sqrt{ 2 }}{2} = -1 - \sqrt{ 2 }
\end{align}
$$

De esta forma, las funciones $f$ y $g$ se cortan en los valores de $x$ $-1 + \sqrt{ 2 }$ y $-1 - \sqrt{ 2 }$.

Ahora, luego de graficar la función, podemos ver que en el intervalo $[-1 - \sqrt{ 2 }, -1 + \sqrt{ 2 }]$, la función $g$ es mayor que $f$, por lo que tendremos que calcular:
$$
\int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} -2x + 1 \space dx - \int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} x^{2} \space dx
$$
Descomponemos cada uno de los términos:
$$
\begin{align}
&\int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} -2x + 1 \space dx = -2 \times \int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} x \space dx + \int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} 1 \space dx = -2 \times \left( \frac{(-1 + \sqrt{ 2 })^{2} - (-1 - \sqrt{ 2 })^{2}}{2} \right) + \left( (-1 + \sqrt{ 2 }) - (-1 - \sqrt{ 2 }) \right) \\
&\int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} x^{2} \space dx = \frac{(-1 + \sqrt{ 2 })^{3} - (-1 - \sqrt{ 2 })^{3}}{3} = \frac{-7 + 5\sqrt{ 2 } - (-7 - 5\sqrt{ 2 })}{3} = \frac{\cancel{ -7 } + 5\sqrt{ 2 } + \cancel{ 7 } + 5\sqrt{ 2 }}{3}
\end{align}
$$
$$
\begin{align}
&\int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} -2x + 1 \space dx = -2 \times \left( \frac{\cancel{ 3 } - 2\sqrt{ 2 } - \cancel{ 3 } - 2\sqrt{ 2 }}{2} \right) + \left( \cancel{ -1 } + \sqrt{ 2 } + \cancel{ 1 } + \sqrt{ 2 }) \right) \\
&= -2 \times \left( -\frac{4\sqrt{ 2 }}{2} \right) + 2\sqrt{ 2 } = -2 \times (-2\sqrt{ 2 }) + 2\sqrt{ 2 } = 4\sqrt{ 2 } + 2\sqrt{ 2 } = 6\sqrt{ 2 }
\end{align}
$$
$$
\begin{align}
& \int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} x^{2} \space dx = \frac{5\sqrt{ 2 } + 5\sqrt{ 2 }}{2} = \frac{10\sqrt{ 2 }}{3} = \frac{10}{3}\sqrt{ 2 }
\end{align}
$$

$$
\implies \int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} -2x + 1 \space dx - \int_{-1 - \sqrt{ 2 }}^{-1 + \sqrt{ 2 }} x^{2} \space dx = 6\sqrt{ 2 } - \frac{10}{3}\sqrt{ 2 } = \frac{18}{3}s_{2} - \frac{10}{3}\sqrt{ 2 } = \frac{8}{3}\sqrt{ 2 }
$$

### Parte c)
$$
\begin{align}
&f(x) = x^{2} \\
&g(x) = \sqrt{ |x| }
\end{align}
$$
Si graficamos ambas funciones, vemos que ambas están espejadas con respecto al eje y, coincidiendo en $x = 0$. Para encontrar este valor, simplemente tenemos que pensar en que valor de $x$ sucede lo siguiente:
$$
\begin{align}
&x^{2} = \sqrt{ |x| } \\
&(x^{2})^{2} = |x| \\
&x^{4} = |x|
\end{align}
$$
Los únicos números que cumplen con dichas características son $1$ y $-1$. Por lo tanto, las funciones coinciden en $x = -1$, $x = 0$ y $x = 1$.

De esta manera, tenemos que calcular:
$$
\int_{-1}^{1} \sqrt{ |x| } - x^{2} \space dx = 2 \times \int_{0}^{1} \sqrt{ x } - x^{2} \space dx = 2 \times \left( \int_{0}^{1} \sqrt{ x } \space dx - \int_{0}^{1} x^{2} \space dx \right)
$$
$$
\begin{align}
&\int_{0}^{1} \sqrt{ x } \space dx = \frac{2}{3} \left( 1^{\frac{3}{2}} - 0^{\frac{3}{2}} \right) = \frac{2}{3}(1 - 0) = \frac{2}{3} \times 1 = \frac{2}{3} \\
&\int_{0}^{1} x^{2} \space dx = \frac{1^{3} - 0^{3}}{3} = \frac{1 - 0}{3} = \frac{1}{3}
\end{align}
$$

$$
\implies \int_{-1}^{1} \sqrt{ |x| } - x^{2} \space dx = 2 \times \left( \frac{2}{3} - \frac{1}{3} \right) = 2 \times \frac{1}{3} = \frac{2}{3}
$$

---
## Ejercicio 3.6.12
### Parte a)
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 3 - Integración/Imágenes/Ejercicio 3.6.12.png]]
Representamos el área a calcular.
Aclaración: El área total será 0, puesto que tenemos dos áreas idénticas, una sobre el eje x y la otra por debajo. Igualmente, calcularemos una de las dos.

Tenemos que encontrar los puntos de intersección entre $f_{1}(x) = 3x$, $f_{3}(x) = \frac{9}{x}$ y $f_{4}(x) = \frac{1}{x}$:
Intersección entre $f_{1}$ y $f_{3}$:
$$
\begin{align}
&3x = \frac{9}{x} \\
&3x^{2} = 9 \\
&x^{2} = \frac{9}{3} = 3 \\
&x = \sqrt{ 3 }
\end{align}
$$
Intersección entre $f_{1}$ y $f_{4}$:
$$
\begin{align}
&3x = \frac{1}{x} \\
&3x^{2} = 1 \\
&x^{2} = \frac{1}{3} \\
&x = \sqrt{ \frac{1}{3} } 
\end{align}
$$

$$
\int_{\sqrt{ \frac{1}{3} }}^{\sqrt{ 3 }} \frac{9}{x} \space dx - \int_{\sqrt{ \frac{1}{3} }}^{\sqrt{ 3 }} \frac{9}{x} \space dx
$$