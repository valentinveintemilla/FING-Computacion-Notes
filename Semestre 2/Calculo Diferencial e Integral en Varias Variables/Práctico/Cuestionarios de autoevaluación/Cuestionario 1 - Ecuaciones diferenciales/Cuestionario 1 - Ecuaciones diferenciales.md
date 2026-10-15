# Ejercicio 1
Pregunta: Considero $a$ y $b$ números reales y $r : \mathbb{R} \to \mathbb{R}$ función continua  distinta de la función nula. Sea A el conjunto de funciones que son solución de la ecuación diferencial $y'' + ay' + by = r(x)$.

Como se trata de una ecuación diferencial de segundo orden no homogénea, su solución general se halla sumando la solución general de la homogénea y una solución particular de la no homogénea.

Sin embargo, esto no da como resultado un espacio vectorial, sino una expresión.

---
# Ejercicio 2
Considere $n \in \mathbb{N}, n \neq 1$ y $b(x)$ una función no nula. La ecuación de Bernoulli es:
$$
y' + a(x)y = b(x)y^{n}
$$
Mediante el cambio de variable $z=y^{1 - n}$ se reduce a una ecuación diferencial de variables separables. ¿Verdadero o falso?

Aplicamos el cambio de variable:
$$
\begin{align}
y' + a(x)y &= b(x)y^{n} \\
\frac{y' + a(x)y}{y^{n}} &= b(x) \\
\frac{y'}{y^{n}} + \frac{a(x)}{y^{n - 1}} &= b(x) \\
y'y^{-n} + a(x)y^{1 - n} &= b(x)
\end{align}
$$
Sabiendo que $z = y^{1 - n}$, derivamos:
$$
z' = (y^{1 - n})' = (1 - n)y^{-n}y' \implies y^{-n}y' = \frac{z'}{1 - n}
$$

Sustituimos en la ecuación:
$$
\frac{z'}{1 - n} + a(x)z = b(x)
$$
Normalizamos (multiplicando a ambos lados por $1 - n$):
$$
z' + (1 - n)a(x)z = (1 - n)b(x)
$$

Esta forma se corresponde con la de una ecuación lineal de primer orden:
$$
y'(x) + a(x)y(x) = b(x)
$$
En cambio, las ecuaciones de variables separables tienen la siguiente forma:
$$
y'(x) = F(y(x))G(x)
$$

En conclusión, el enunciado es ==falso==.

---
# Ejercicio 3
Dada la ecuación diferencial:
$$
y'' + 4y = \sin(x)
$$
Considera la solución tal que $y(0) = y'(0) = 1$. Tenemos que determinar $y(\pi)$:

Identificamos el tipo de ecuación: ecuación de segundo orden.


Estudiamos la homogénea: $y'' + 4y = 0$. Analizamos el polinomio característico:
$$
\lambda^{2} + 0\lambda + 4 = 0
$$
$$
\begin{align}
\lambda &= \frac{0 \pm \sqrt{ 0^{2} - 4 \cdot 1 \cdot 4 }}{2 \cdot 1} \\
&= \frac{0 \pm \sqrt{ -16 }}{2} \\
&= \frac{0 \pm \sqrt{ 16 }\sqrt{ -1 }}{2} \\
&= \frac{0 \pm 4i}{2} \\
&= \pm 2i
\end{align}
$$

Entonces, sabemos que la solución general de la homogénea es:
$$
y_{H}(x) = Ae^{0}\cos(2x) + Be^{0}\sin(2x) = A\cos(2x) + B\sin(2x)
$$

Ahora, procedemos a encontrar una solución particular:

Consideramos $y(x) = A\sin(x) + B\cos(x)$, entonces $y''(x) = -A\sin(x) - B\cos(x)$
$$
\begin{align}
y'' + 4y &= \sin(x) \\
-A\sin(x) - B\cos(x) + 4A\sin(x) + 4B\cos(x) &= \sin(x) \\
3A\sin(x) + 3B\cos(x) &= \sin(x)
\end{align}
$$
De esta forma:
$$
\begin{cases}
3A = 1 \implies A = \frac{1}{3} \\
3B = 0 \implies B = 0
\end{cases}
$$
Entonces, una solución particular es:
$$
y_{P}(x) = \frac{1}{3}\sin(x)
$$

Es así que determinamos la solución general de la no homogénea:
$$
y_{NH}(x) = y_{H}(x) + y_{P}(x) = A\cos(2x) + B\sin(2x) + \frac{1}{3}\sin(x)
$$

Ahora, consideramos las condiciones establecidas: $y(0) = y'(0) = 1$
$$
y(0) = A\cos(2 \cdot 0) + B\sin(2 \cdot 0) + \frac{1}{3}\sin(0) = A \cdot 1 + B \cdot 0 + \frac{1}{3} \cdot 0 = A = 1 \implies A = 1
$$
$$
y'(x) = -2A\sin(2x) + 2B\cos(2x) + \frac{1}{3}\cos(x)
$$
$$
\implies y'(0) = -2A\sin(2 \cdot 0) + 2B\cos(2 \cdot 0) + \frac{1}{3}\cos(0) = -2A \cdot 0 + 2B \cdot 1 + \frac{1}{3} \cdot 1 = 2B + \frac{1}{3} = 1
$$
$$
\implies 2B = \frac{2}{3} \implies B = \frac{1}{3}
$$

Es así que determinamos la solución general acorde a las condiciones establecidas:
$$
y(x) = \cos(2x) + \frac{1}{3}\sin(2x) + \frac{1}{3}\sin(x)
$$

Ahora, resta determinar $y(\pi)$:
$$
y(\pi) = \cos(2\pi) + \frac{1}{3}\sin(2\pi) + \frac{1}{3}\sin(\pi) = 1 + \frac{1}{3} \cdot 0 + \frac{1}{3} \cdot 0 = 1
$$

En conclusión: $y(\pi) = 1$.

---
# Ejercicio 4
Consideremos la ecuación diferencial $y' = y^{\frac{1}{3}}$ con la condición inicial $y(0) = 0$.

Estudiamos la ecuación diferencial:
$$
\begin{align}
y' &= y^{\frac{1}{3}} \\
\frac{y'}{y^{\frac{1}{3}}} &= 1 \\
\int \frac{y'}{y^{\frac{1}{3}}} dx &= \int 1 dx \\
\int \frac{y'}{y^{\frac{1}{3}}} dx &= x + C \\
\int \frac{1}{u^{\frac{1}{3}}} du &= x + C \\
\int u^{-\frac{1}{3}} du &= x + C \\
\frac{u^{\frac{2}{3}}}{\frac{2}{3}} &= x + C \\
\frac{y^{\frac{2}{3}}}{\frac{2}{3}} &= x + C \\
y^{\frac{2}{3}} &= \frac{3x}{2} + C \\
\left( y^{\frac{2}{3}} \right)^{\frac{3}{2}} &= \left( \frac{3x}{2} + C \right)^{\frac{3}{2}} \\
y &= \left( \frac{3x}{2} + C \right)^{\frac{3}{2}}
\end{align}
$$

Ahora, queremos la solución específica que cumple $y(0) = 0$:
$$
y(0) = \left( \frac{3 \cdot 0}{2} + C \right)^{\frac{3}{2}} = C^{\frac{3}{2}} = 0 \implies C = 0
$$

De esta forma, existe una única solución definida en $\mathbb{R}$ que cumple con la condición $y(0) = 0$, y es:
$$
y(x) = \left(\frac{3x}{2}\right)^{\frac{3}{2}}
$$

---
# Ejercicio 5
Dada la ecuación diferencial:
$$
y'' − 5y' + 4y = 0
$$
Considera la solución tal que $y(0) = 5$ y $y'(0) = 8$. Determina $y(1)$.

Como nos encontramos ante una ecuación homogénea de segundo orden, estudiamos las raíces del polinomio característico:
$$
\lambda^{2} - 5\lambda + 4 = 0
$$
$$
\begin{align}
\lambda &= \frac{5 \pm \sqrt{ (-5)^{2} - 4 \cdot 1 \cdot 4 }}{2 \cdot 1} \\
&= \frac{5 \pm \sqrt{ 25 - 16 }}{2} \\
&= \frac{5 \pm \sqrt{ 9 }}{2} \\
&= \frac{5 \pm 3}{2} \\
&\implies \lambda_{1} = \frac{5 + 3}{2} = \frac{8}{2} = 4, \lambda_{2} = \frac{5 - 3}{2} = \frac{2}{2} = 1
\end{align}
$$
Encontramos dos raíces reales diferentes, por lo que podemos determinar la siguiente base del espacio vectorial de las soluciones:
$$
\mathcal{B} = \{ e^{4x}, e^{x} \}
$$
Y la siguiente solución general:
$$
y_{H}(x) = Ae^{4x} + Be^{x}
$$

Ahora, pasamos a encontrar la solución particular que verifica $y(0) = 5$ y $y'(0) = 8$:
$$
y(0) = Ae^{4 \cdot 0} + Be^{0} = A + B = 5
$$
$$
y'(x) = 4Ae^{4x} + Be^{x}
$$
$$
\implies y'(0) = 4Ae^{4 \cdot 0} + Be^{0} = 4A + B = 8
$$

Resolvemos el sistema:
$$
\begin{cases}
A + B = 5 \\
4A + B = 8
\end{cases} \implies 3A = 3 \implies A = 1 \implies 1 + B = 5 \implies B = 4 
$$

De esta manera, la solución que verifica las condiciones dadas es:
$$
y(x) = e^{4x} + 4e^{x}
$$

Finalmente, hallamos $y(1)$:
$$
y(1) = e^{4 \cdot 1} + 4e^{1} = e^{4} + 4e
$$

En conclusión:
$$
y(1) = 4e + e^{4}
$$

---
# Ejercicio 6
Dada la ecuación diferencial:
$$
y' = \frac{y}{x}
$$
Considera la solución tal que $y(1) = −8$. Entonces se cumple que $y(3)$ es igual a $...$

Esta es una ecuación sencilla, puesto que es de primer orden:
$$
\begin{align}
y' &= \frac{y}{x} \\
\frac{1}{y'} &= \frac{x}{y} \\
\frac{y}{y'} &= x \\
\frac{y'}{y} &= \frac{1}{x} \\
\int \frac{y'}{y} dx &= \int \frac{1}{x} dx
\end{align}
$$
Realizamos cambio de variable:
$$
u = y \implies du = y' dx
$$
$$
\begin{align}
\int \frac{1}{u} du &= \int \frac{1}{x} dx \\
\log(|u|) &= \log(x) + C \\
\log(|y|) &= \log(x) + C \\
|y| &= \exp(\log(x) + C) = e^{\log(x) + C} = e^{\log(x)}e^{C} = xe^{C} \qquad (e^{C} \in \mathbb{R}^{+}) \\
y &= kx, k \in \mathbb{R}
\end{align}
$$

Hallamos la solución particular que cumple $y(1) = −8$:
$$
y(1) = k \cdot 1 = k = -8 \implies k = -8
$$
Entonces:
$$
y(x) = -8x
$$

Finalmente, determinamos $y(3)$:
$$
y(3) = -8 \cdot 3 = -24
$$

