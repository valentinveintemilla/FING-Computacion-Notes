# Integrales de las funciones polinomiales
Repasaremos las funciones potencias para hacer un recordatorio de la clase pasada. Veremos una observación antes de enunciar la propiedad importante.

## Observación
Sea $f(x) = x^{p}$, con $p \in \mathbb{N}$.
Sobre esta función, podemos decir que depende de p. A continuación representamos algunas posibilidades:
![[Gráficas x a la p.png]]
Como vemos, en todos los casos la gráfica depende de p.
Por esta razón, vamos a distinguir dos casos importantes:
- Cuando p es impar, es una función monótona creciente.
- Cuando p es par, es una función monótona decreciente en el intervalo $(-\infty, 0]$ y monótona creciente en $[0, +\infty)$. Podemos decir lo mismo del caso $p = 0$ (las funciones constantes cumplen ambas propiedades a la vez: son crecientes y decrecientes).

Simplemente:
- Si p es par: f es monótona decreciente en $(-\infty, 0]$, y monótona creciente en $[0, +\infty)$.
- Si p es impar: f es monótona creciente en $\mathbb{R}$.

**Observación**: cuando hacemos una integrar sobre un intervalo simétrico respecto a cero, obtengo una integral nula, pues las partes positivas y negativas son iguales (se compensan).

¿Éstas funciones son integrables o no?
- Si p es impar: siempre es integrable, pues tenemos un teorema que establece que si una función es monótona creciente, entonces es integrable en cualquier intervalo.
- Si p es par: es un poco más complicado.
Si tomamos un intervalo únicamente en la parte positiva, es integrable, ya que es una función monótona creciente (en el intervalo especificado).
Del mismo modo, si tomamos un intervalo solo en la parte negativa, también será integrable, pues la función es monótona decreciente en dicho intervalo.

El problema está en entender que sucede cuando trabajamos con un intervalo que tiene tanto números positivos como negativos. Sin embargo, tenemos una solución a dicho problema:
Podemos dividir el intervalo en dos partes (la primera hasta 0, solo con números negativos, y la segunda desde 0, solo con números positivos), observando que la primer parte será integrable (pues es monótona decreciente), y la segunda también será integrable (pues es monótona creciente). De esta forma, al unir ambos subintervalos, podemos determinar que la función es integrable en cualquier intervalo.

En conclusión, las funciones polinómicas son integrables en cualquier intervalo, aunque sea en trozos (caso p par).

## Proposición
Dado $p \in \mathbb{N}$, la función $f(x) = x^{p}$ es integrable en cualquier intervalo $[a, b]$ (con $a < b$) y
$$
\int_{a}^{b} x^{p} dx = \frac{b^{p + 1} - a^{p + 1}}{p + 1}
$$
Esta fórmula sirve para los monomios, las funciones potencia.
Cuando veamos el teorema fundamental, veremos que esta fórmula tiene la forma de una primitiva (conceptos que aún no conocemos, pero veremos más avanzado el curso). Por ahora, nosotros necesitamos memorizarla y justificarla.

### Lema
Para todos $x, y \in \mathbb{R}$ tales que $0 \leq x \leq y$
$$
(y - x) x^{p} \leq \frac{y^{p + 1} - x^{p + 1}}{p + 1} \leq (y-x)y^{p}
$$
Ya vimos un lema similar a este para la parábola. Esta es la generalización para cualquier potencia.

A continuación, demostraremos el lema:

#### Demostración
$$
(y - x) \sum_{i = 0}^{p} x^{i}y^{p-i} = (y-x)(y^{p} + xy^{p-1} + x^{2}y^{p-2} + \dots + x^{p-1}y + x^{p})
$$
Las potencias de x son crecientes (van de 0 a p), y las potencias de y son decrecientes (van de p a 0).
Lo interesante es que son monomios de grado p, pues cada vez que sumamos las potencias de x e y obtengo p, por lo que sus grados se compensan.
$$
\begin{align}
&= y^{p + 1} + \cancel{ xy^{p} } + \cancel{ x^{2}y^{p-1} } + \cancel{ \dots } + \cancel{ x^{p-1}y^{2} } + \cancel{ x^{p}y } \\
&- \cancel{ xy^{p} } - \cancel{ x^{2}y^{p-1} } - \cancel{ x^{3}y^{p-2} } - \cancel{ \dots } - \cancel{ x^{p}y } - x^{p + 1}
\end{align}
$$
Como vemos, al desarrollar el producto, casi todos los términos se simplifican, quedando únicamente:
$$
= y^{p + 1} - x^{p + 1}
$$
Como vemos, alcanzamos una resta que forma parte de la desigualdad establecida en el lema anterior.
El resultado alcanzado es igual al producto inicial ($(y - x) \sum_{i = 0}^{p} x^{i}y^{p-i}$), de hecho es una factorización del mismo. La suma final se puede factorizar por $(y-x)$, y el polinomio resultante es un polinomio con $p + 1$ sumandos.

Esto nos explica de donde sale dicho resultado, se trata de una generalización de la resta de dos potencias iguales:
$$
\begin{align}
&(y^{2} - x^{2}) = (y - x)(y + x) \\
&(y^{3} - x^{3}) = (y - x)(y^{2} + xy + x^{2}) \\
&\dots
\end{align}
$$
En conclusión, $(y - x) \sum_{i = 0}^{p} x^{i}y^{p-i}$ generaliza todos estos casos, y se obtiene de analizar los primeros casos de forma manual, observar que hay una generalidad que se cumple, y en base a eso desarrollar una fórmula que aplique a todos los casos.

Esto es una buena forma de entender como es que trabajan los matemáticos a la hora de desarrollar fórmulas, demostrar hipótesis, etc.:
- Parte de creación, parte sucia en la que hay una idea, se analizan casos manualmente, se llega a una generalización, aunque no se sabe si funciona.
- Proceso de verificación, donde se testea el resultado y se confirma que el mismo sea correcto.

Igualmente, los procesos formales, como la inducción sobre p en este caso, confirman con certeza que la suposición y el resultado obtenido son correctos.

A continuación, demostraremos la desigualdad del lema:

Se observa
$$
\sum_{i=0}^{p}x^{i}x^{p-i} = (p+1)x^{p} \leq \sum_{i=0}^{p}x^{i}y^{p-i} \leq \sum_{i=0}^{p}\underbrace{ y^{i}y^{p-i} }_{ y^{p} } = (p + 1)y^{p}
$$
De esta forma, podemos llegar a la siguiente conclusión:
$$
(p+1)x^{p} \leq \sum_{i=0}^{p}x^{i}y^{p-i} \leq (p + 1)y^{p}
$$
Ahora, podemos multiplicar ambos lados por $y - x$ (que sabemos que es positivo ya que $0 \leq x \leq y$:
$$
(p+1)(y-x)x^{p} \leq y^{p + 1} - x^{p + 1} \leq (p + 1)(y-x)y^{p}
$$
Aquí finaliza la demostración del lema.
Para obtener la misma desigualdad, dividimos todo entre $p + 1$:
$$
(y-x)x^{p} \leq \frac{y^{p + 1} - x^{p + 1}}{p+1} \leq (y-x)y^{p}
$$

Proseguimos con la demostración de la proposición:

### Demostración
Se distinguen 3 casos:


**Caso 1**: $0 \leq a < b \qquad ([a, b] \subset [0, +\infty))$
Aquí, la función es monótona creciente, por lo que sabemos que es integrable.

Para toda partición $P =  \{ a_{0}, a_{1}, \dots, a_{n} \} \subset [a, b]$ (podemos determinar la suma inferior)
$$
S_{*}(f, P) = \sum_{i = 0}^{n - 1} (a_{i + 1} - a_{i}) \cdot a_{i}^{p}
$$
(El ínfimo de la función $x^{p}$ en el intervalo $[a_{i}, a_{i+1}]$ es $a_{i}^{p}$. Esto es así ya que al ser monótona creciente, el valor que tendrá la imagen menor será el borde izquierdo del intervalo -$a_{i}$-, y como la imagen es $a_{i}^{p}$, ese es el ínfimo local).

Ahora, podemos ver que estamos en la condición establecida por el lema (primer desigualdad), donde:
- $y = a_{i+1}$
- $x = a_{i}$
- $a_{i}^{p} = x^{p}$

De esta forma, podemos aplicar la primer desigualdad del lema:
$$
S_{*}(f, P) = \sum_{i = 0}^{n - 1} (a_{i + 1} - a_{i}) \cdot a_{i}^{p} \leq \sum_{i = 0}^{n - 1} \left( \frac{a_{i + 1}^{p + 1} - a_{i}^{p + 1}}{p + 1} \right) = \frac{a_{n}^{p+1} - a_{0}^{p+1}}{p + 1} = \frac{b^{p + 1} - a^{p + 1}}{p + 1}
$$
En la sumatoria, los términos se simplifican de a dos.

Podemos sustituir a $a_{n}$ por b (final del intervalo) y a $a_{0}$ por a (comienzo del intervalo).

Podemos decir que $\frac{b^{p + 1} - a^{p + 1}}{p + 1}$ es independiente de la partición elegida, de modo que es una cota superior de todas las sumas inferiores.

Luego: $I_{*}(f) \leq \frac{b^{p + 1} - a^{p + 1}}{p + 1}$
De esta forma, obtuvimos una aproximación de la integral inferior.

Ahora, demostraremos que la integral superior es mayor que esto, para lo que desarrollaremos el mismo razonamiento para las sumas superiores.

Para toda partición $P = \{ a_{0}, a_{1}, \dots, a_{n} \} \subset [a, b]$
$$
S^{*}(f, P) = \sum_{i = 0}^{n - 1} (a_{i + 1} - a_{i}) \cdot a_{i + 1}^{p} \geq \sum_{i = 0}^{n - 1} \left( \frac{a_{i + 1}^{p + 1} - a_{i}^{p + 1}}{p + 1} \right) = \frac{a_{n}^{p + 1} - a_{0}^{p + 1}}{p + 1} = \frac{b^{p + 1} - a^{p + 1}}{p + 1}
$$
En este caso, tomamos el supremo de cada subintervalo $a_{i + 1}^{p}$.
Aquí, utilizamos la segunda desigualdad enunciada por el lema.

Llegamos a la conclusión de que $\frac{b^{p + 1} - a^{p + 1}}{p + 1}$ es una cota inferior de todas las sumas superiores, de modo que es menor o igual al ínfimo de todas las cotas superiores (integral superior).

Luego: $I^{*}(f) \geq \frac{b^{p + 1} - a^{p + 1}}{p + 1}$

Conclusión:
Como sabemos que la función es integrable (puesto que es monótona creciente):
$$
\int_{a}^{b} x^{p} dx = I_{*}(f) = I^{*}(f) = \frac{b^{p + 1} - a^{p + 1}}{p + 1}
$$
Con esto, logramos demostrar la proposición para el caso 1 ($0 \leq a < b \qquad ([a, b] \subset [0, +\infty))$).

Proseguimos con el caso 2.


**Caso 2: $a < b \leq 0 \qquad ([a, b] \subset (-\infty, 0])$

Aquí no podemos utilizar el lema, ya que solo funciona para valores positivos. Sin embargo, yo tengo la posibilidad de utilizar la integración en espejo, basada en nociones geométricas.
De esta forma, sabiendo que es integrable en $[a, b]$, también podemos confirmar que es integrable en $[-b, -a]$.
$$
\int_{a}^{b} x^{p} dx = \int_{-b}^{-a} (-x)^{p} dx
$$
Ahora, hay que ver cual es la función $(-x)^{p}$.
La ventaja de este acercamiento es que sabemos que $-b$ y $-a$ son positivos.

**Subcaso 2.1**: p es par
$$
\int_{a}^{b} x^{p} dx = \int_{-b}^{-a} (-x)^{p} dx = \int_{-b}^{-a} x^{p} dx \underbrace{ = }_{ \text{Caso 1} } \frac{(-a)^{p + 1} - (-b)^{p + 1}}{p + 1}
$$
Como sabemos que cualquier número elevado a un número par, da como resultado un número positivo, podemos sustituir $(-x)^{p}$ por $x^{p}$.

Al final de la desigualdad, utilizo la fórmula del caso 1, pues sabemos que $0 \leq -b < -a$.

Ahora, como p es par, pero $p + 1$ es impar:
$$
\begin{align}
&\dots = \frac{(-a)^{p + 1} - (-b)^{p + 1}}{p + 1} \\
&= \frac{-a^{p + 1} + b^{p + 1}}{p + 1} \\
&= \frac{b^{p + 1} - a^{p + 1}}{p + 1}
\end{align}
$$
Como vemos, obtuvimos la formula correspondiente.

**Subcaso 2.1**: p es impar
$$
\int_{a}^{b} x^{p} dx = \int_{-b}^{-a} (-x)^{p} dx = -\int_{-b}^{-a} x^{p} dx = - \frac{(-a)^{p + 1} - (-b)^{p + 1}}{p + 1}
$$
Aquí, no podemos quitar el signo de menos, ya que p es impar, y como sabemos, cualquier número elevado a un impar mantiene su signo.
Además, podemos sacar el - afuera de la integral por linealidad.

Como p es impar, p + 1 es par, por lo que cambian los signos con respecto al subcaso anterior:
$$
\begin{align}
&\dots = - \frac{(-a)^{p + 1} - (-b)^{p + 1}}{p + 1} \\
&=- \frac{a^{p + 1} - b^{p + 1}}{p + 1} \\
&=\frac{b^{p + 1} - a^{p + 1}}{p + 1}
\end{align}
$$
También, intercambiamos el signo de $b^{p + 1}$ y $a^{p + 1}$, puesto que teníamos un signo de menos externo a la división.

El caso que queda es en el que tenemos tanto números negativos como positivos en el intervalo.

**Caso 3**: $a < 0 < b$
$$
\int_{a}^{b} x^{p} dx = \int_{a}^{0} x^{p} dx + \int_{0}^{b} x^{p} dx
$$
Nuestro acercamiento consiste en descomponer la integral en dos trozos:
- Parte negativa ($[a, 0]$).
- Parte positiva ($[0, b]$).

Ahora no tenemos dificultades para operar, ya que sabemos que la función es integrable en los intervalos $[a, 0]$ (corresponde al caso 2) y $[0, b]$ (corresponde al caso 1).
$$
\begin{align}
&\dots = \overbrace{ \frac{\cancel{ 0^{p + 1} } - a^{p + 1}}{p + 1} }^{ \text{Caso 2} } + \overbrace{ \frac{b^{p + 1} - \cancel{ 0^{p + 1} }}{p + 1} }^{ \text{Caso 1} } \\
&= \frac{b^{p + 1} - a^{p + 1}}{p + 1}
\end{align}
$$
Obtuve la misma fórmula nuevamente. Aunque cambiemos las condiciones, la fórmula se mantiene.

Con esto, finalizamos la demostración de la proposición.
Determinamos que es verdadero en todos los casos.
Si bien no expresamos el $a = b$, sabemos que en ese caso:
$$
\int_{a}^{b} x^{p} dx = 0 \qquad \text{y} \qquad \frac{b^{p + 1} - a^{p + 1}}{p + 1} = \frac{0^{p + 1} - 0^{p + 1}}{p + 1} = 0
$$
De esta forma, también se cumple para dicho caso.

También se cumple, incluso cuando intercambiamos el orden de los extremos, puesto que, aunque se invierte el valor de la integral, también se invierte el orden de los términos de la fórmula, haciendo que la igualdad se mantenga.

En conclusión, ahora sabemos integrar todos los monomios.
Pero si sabemos integrar todos los monomios, esto significa que también sabemos integrar todos los polinomios, ya que un polinomio es una combinación lineal finita de funciones potencia con algunos coeficientes. De esta forma, si ya se integrar cada función potencia, puedo integrar todos los polinomios.

#### Ejemplo
Sea $f(x) = \frac{1}{3}x^{3} - x + 1 \qquad \int_{-1}^{2}f \text{ ?}$
![[Representación polinomio ejemplo 1.png]]
Como vemos, la función es positiva en el intervalo especificado.

Como se trata de una combinación lineal de funciones integrables, no hay ningún problema, podemos integrar.

$$
\begin{align}
&\int_{-1}^{2} \left( \frac{1}{3}x^{3} - x + 1 \right) dx \\
&=\frac{1}{3} \int_{-1}^{2} x^{3} dx - \int_{-1}^{2} x^{1} dx + \int_{-1}^{2} x^{0} dx \\
&=\frac{1}{3}\left( \frac{2^{4} - (-1)^{4}}{4} \right) - \frac{2^{2} - (-1)^{2}}{2} + \frac{2^{1} - (-1)^{1}}{1} \\
&=\frac{1}{3}\left( \frac{16 - 1}{4} \right) - \frac{4 - 1}{2} + \frac{2 - (-1)}{1} \\
&=\frac{1}{3}\left( \frac{15}{4} \right) - \frac{3}{2} + \frac{3}{1} \\
&=\frac{5}{4} - \frac{3}{2} + 3 \\
&=\frac{11}{4}
\end{align}
$$
Esto también es muy útil para verificar integrales. Por ejemplo, en base a la gráfica sabemos que el área de la función es negativa, por lo que obtener un resultado negativo sería incorrecto.
También podríamos comparar el resultado obtenido, graficando una figura de misma área y ver si tiene sentido con respecto a la gráfica de la función correspondiente.

Ahora, veremos que demostramos una formula fundamental, correspondiente al teorema fundamental del cálculo, aunque puntualmente para las funciones potencia.

$$
\int_{a}^{b} x^{p} dx = \frac{b^{p + 1} - a^{p + 1}}{p + 1} = F(b) - F(a)
$$
donde
$$
F(x) = \frac{x^{p + 1}}{p + 1}
$$
Como vemos, expresamos la fórmula que teníamos para calcular la integral de un monomio dados los intervalos en forma de la diferencia de dos funciones. De esta manera, llegamos a la definición puntual de la nueva función correspondiente a dicha diferencia.
Únicamente cambiamos de escritura, el sentido es el mismo.

Lo que podemos decir de esta función, es que es una primitiva de la función $x^{p}$.
Se observa que
$$
F'(x) = x^{p}
$$
Aclaración: si derivamos una primitiva, obtenemos la función original.

De esta forma, desarrollamos un pequeño teorema fundamental para las funciones potencia.
Por combinaciones lineales, es posible demostrar el teorema fundamental para los polinomios.

A continuación, generalizamos para todos los polinomios:

### Proposición
Si $f : \mathbb{R} \to \mathbb{R}$ es un polinomio, entonces
$$
\int_{a}^{b} f \space dx = F(b) - F(a)
$$
donde F es cualquier polinomio tal que $F' = f$

La demostración consiste en descomponer la función por linealidad, aplicar la observación anterior a cada trozo y observar que si sumo las primitivas de todos los monomios voy a obtener una primitiva del polinomio, y aunque difieren en una constante, la constante se va a cancelar gracias a la diferencia $F(b) - F(a)$, por lo que es irrelevante.
Lo importante es que este es otro método para calcular la integral de polinomios, siendo un teorema fundamental restringido para los polinomios.

#### Ejemplo
$$
\begin{align}
&f(x) = \frac{1}{3}x^{3} - x + 1 \\
&F(x) = \frac{x^{3 + 1}}{\frac{3}{3+1}} - \frac{x^{2}}{2} + x \\
&= \frac{x^{4}}{\frac{3}{4}} - \frac{x^{2}}{2} + x \\
&= \frac{x^{4}}{12} - \frac{x^{2}}{2} + x \\
&= \frac{1}{12}x^{4} - \frac{x^{2}}{2} + x \\
&\implies \int_{-1}^{2} f = F(2) - F(-1) = \frac{1}{12}2^{4} - \frac{2^{2}}{2} + 2 - \left( \frac{1}{12}(-1)^{4} - \frac{(-1)^{2}}{2} + (-1) \right) \\
&= \frac{1}{12}16 - \frac{4}{2} + 2 - \left( \frac{1}{12}1 - \frac{1}{2} - 1 \right) \\
&= \frac{16}{12} - \frac{4}{2} + 2 - \left( \frac{1}{12} - \frac{1}{2} - 1 \right) \\
&= \frac{4}{3} - \frac{6}{3} + \frac{6}{3} - \left( \frac{1}{12} - \frac{6}{12} - \frac{12}{12} \right) \\
&= \frac{4}{3} - \left( - \frac{17}{12} \right) \\
&= \frac{4}{3} + \frac{17}{12} \\
&= \frac{16}{12} + \frac{17}{12} \\
&= \frac{33}{12} \\
&= \frac{11}{4}
\end{align}
$$
Como vemos, llegamos al mismo resultado.
Para aclarar, $F(x) = \frac{x^{3 + 1}}{\frac{3}{3+1}} - \frac{x^{2}}{2} + x$ es una primitiva, específicamente la primitiva de $f(x) = \frac{1}{3}x^{3} - x + 1$, ya que $F' = f$ (la derivada de $F$ es $f$)

Podemos entender que esta forma es más sencilla, aunque podemos seguir utilizando el anterior, puesto que lo entendemos mejor y llegamos al mismo resultado.

No es importante entender todo esto, puesto que ni siquiera hemos visto el concepto de derivada.

La próxima clase, finalizaremos el capítulo sobre las integrales.