# 1 - Ejercicios del práctico
## Ejercicio 1
### Parte a
Comencemos demostrando que $F(x)$ es creciente:
Como $f$ es continua y $F(x) = \int_{a}^{x} f(t) dt$, podemos aplicar el teorema fundamental:
$$
F(x) = \int_{a}^{x} f(t) dt \implies F'(x) = f(x)
$$
De esta forma, la derivada de la función $F(x)$ es $f(x)$, y como por hipótesis sabemos que $f(t) \geq 0$, entonces $F'(x) \geq 0$. En conclusión, la función $F(x)$ es creciente, ya que su derivada es no negativa.

Ahora, pasamos a demostrar la doble implicación, comenzando por la implicación directa: $\int_{a}^{+\infty} f(t) dt$ converge $\implies F(x)$ está acotada superiormente.

Por la definición de integrales impropias de primera especie, sabemos que necesariamente para que la integral impropia $\int_{a}^{+\infty} f(t) dt$ converja, $\lim_{ x \to \infty } F(x) = L$ finito. Además, como $F(x)$ es creciente, entonces necesariamente $F(x)$ está acotada superiormente por $L$.

Finalmente, demostramos el recíproco: $F(x)$ está acotada superiormente $\implies \int_{a}^{+\infty} f(t) dt$ converge

Sabemos que $F(x)$ es creciente, entonces si está acotada superiormente, significa que existe $L$ finito tal que $\lim_{ x \to \infty } F(x) = L$. De esta forma, por definición, la integral impropia $\int_{a}^{+\infty} f(t) dt$ es convergente, y lo hace a $L$.

### Parte b
Consideremos la desigualdad propuesta:
$$
0 \leq f(t) \leq g(t), \forall t \geq a
$$
Entonces, podemos integrar a ambos lados de la desigualdad:
$$
\int_{a}^{x} 0 \space dt \leq \int_{a}^{x} f(t) \space dt \leq \int_{a}^{x} g(t) \space dt
$$
$$
0 \leq F(t) \leq G(t)
$$

#### Parte i
Ahora, supongamos que $\int_{a}^{+\infty} g(t) \space dt$ converge. Esto significa (por la parte anterior), que $G(t)$ está superiormente acotada por $L$ finito. De esta forma, como se cumple que
$$
F(t) \leq G(t) \leq L
$$
y sabiendo que $F(t)$ es creciente, entonces necesariamente $F(t) \leq L' \leq L$. Por lo tanto,
$$
\lim_{ t \to \infty } F(t) = L'
$$
y en conclusión (por definición) $\int_{a}^{+\infty} f(t) \space dt$ converge.

#### Parte ii
En este caso, $\int_{a}^{+\infty} f(t) dt$ diverge. Por la definición de integrales impropias, esto se debe a que $\lim_{ t \to \infty } F(t) = +\infty$.

Entonces, si analizamos la desigualdad anterior, ahora considerando los límites:
$$
0 \leq F(t) \leq G(t) \implies \lim_{ t \to \infty } 0 \leq \lim_{ t \to \infty } F(t) \leq \lim_{ t \to \infty } G(t)
$$
De esta manera, necesariamente se cumple que $\lim_{ t \to \infty } G(t) = +\infty$.

En conclusión (por definición) $\int_{a}^{+\infty} g(t) \space dt$ diverge.

---
## Ejercicio 2
### Parte a
$$
\int_{2}^{+\infty} \frac{1}{x \log^{\alpha}(x)} dx
$$
Realizamos el siguiente cambio de variable:
$$
u = \log(x) \geq du = \frac{1}{x} dx
$$
$$
\begin{align}
\int_{2}^{x} \frac{1}{t \log^{\alpha}(t)} dt &= \int_{2}^{x} \frac{1}{\log^{\alpha}(t)} \cdot \frac{1}{t} dt \\
&= \int_{2}^{x} \frac{1}{u^{\alpha}} du \\
&= \int_{2}^{x} u^{-\alpha} du \\
&= \left. \frac{u^{-\alpha + 1}}{-\alpha + 1} \right|_{2}^{x} + C \\
&\underbrace{ = }_{ D.C.V. } \left. \frac{\log^{-\alpha + 1}(t)}{-\alpha + 1} \right|_{2}^{x} + C \\
&= \frac{\log^{-\alpha + 1}(x)}{-\alpha + 1} - \frac{\log^{-\alpha + 1}(2)}{-\alpha + 1} + C
\end{align}
$$
Ahora, analizamos los diferentes valores posibles de $\alpha$ (sin considerar $\alpha = 1$, ya que anula los denominadores):
- $\alpha < 1$:
Aquí, $-\alpha + 1 > 0$, por lo que:
$$
\lim_{ x \to \infty } \frac{\log^{-\alpha + 1}(x)}{-\alpha + 1} - \frac{\log^{-\alpha + 1}(2)}{-\alpha + 1} = \frac{+\infty}{-\alpha + 1} - \frac{\log^{-\alpha + 1}(2)}{-\alpha + 1} = +\infty - C = +\infty
$$
Por lo tanto, para $\alpha < 1$, la integral $\int_{2}^{+\infty} \frac{1}{x \log^{\alpha}(x)} dx$ diverge.

- $\alpha > 1$
Aquí, $-\alpha + 1 < 0$, por lo que:
$$
\lim_{ x \to \infty } \frac{\log^{-\alpha + 1}(x)}{-\alpha + 1} - \frac{\log^{-\alpha + 1}(2)}{-\alpha + 1} = \frac{0}{-\alpha + 1} - \frac{\log^{-\alpha + 1}(2)}{-\alpha + 1} = 0 - \frac{\log^{-\alpha + 1}(2)}{-\alpha + 1} = \frac{\log^{1 - \alpha}(2)}{\alpha - 1}
$$
Por lo tanto, para $\alpha > 1$, la integral $\int_{2}^{+\infty} \frac{1}{x \log^{\alpha}(x)} dx$ converge, y $\int_{2}^{+\infty} \frac{1}{x \log^{\alpha}(x)} dx = \frac{\log^{1 - \alpha}(2)}{\alpha - 1}$.

### Parte b
$$
\int_{0}^{+\infty} x^{3} e^{-x^{2}} dx = \int_{0}^{+\infty} x^{2} \cdot x e^{-x^{2}} dx
$$
En este caso, aplicamos integración por partes:
$$
\left[
\begin{align}
&f(x) = x^{2} &f'(x) = 2x \\
&g'(x) = x e^{-x^{2}} &g(x) = -\frac{1}{2} e^{-x^{2}}
\end{align}
\right]
$$
De esta forma:
$$
\begin{align}
\int_{0}^{x} x^{3} e^{-x^{2}} dx &= \left. - \frac{x^{2} e^{-x^{2}}}{2} \right|_{0}^{x} + \int_{0}^{x} x e^{-x^{2}} dx \\
&= \left. - \frac{x^{2} e^{-x^{2}}}{2} \right|_{0}^{x} - \frac{1}{2}\int_{0}^{x} - 2x e^{-x^{2}} dx \\
&= \left. - \frac{x^{2} e^{-x^{2}}}{2} \right|_{0}^{x} - \left. \frac{1}{2}e^{-x^{2}} \right|_{0}^{x} \\
&= - \frac{x^{2} e^{-x^{2}}}{2} + \cancel{ \frac{0^{2} e^{-0^{2}}}{2} } - \frac{1}{2}e^{-x^{2}} + \frac{1}{2}e^{-0^{2}} \\
&= -\frac{x^{2} e^{-x^{2}}}{2} - \frac{1}{2}e^{-x^{2}} + \frac{1}{2}
\end{align}
$$
Ahora, analizamos el comportamiento de la función $F(x)$ en el infinito:
$$
\begin{align}
\lim_{ x \to \infty } -\frac{x^{2} e^{-x^{2}}}{2} - \frac{1}{2}e^{-x^{2}} + \frac{1}{2} &= \lim_{ x \to \infty } -\frac{x^{2} e^{-x^{2}}}{2} - \lim_{ x \to \infty } \frac{1}{2}e^{-x^{2}} + \lim_{ x \to \infty } \frac{1}{2} \\
&= -\frac{0}{2} - \frac{1}{2} \cdot 0 + \frac{1}{2} \\
&= \frac{1}{2}
\end{align}
$$

En conclusión:
$$
\int_{0}^{+\infty} x^{3} e^{-x^{2}} dx = \frac{1}{2}
$$

### Parte c
$$
\int_{0}^{1} \frac{1}{x^{2}} \sin\left( \frac{1}{x} \right) dx
$$
Procedemos a hallar la primitiva correspondiente, aplicando el siguiente cambio de variable:
$$
u = \frac{1}{x} \implies du = -\frac{1}{x^{2}} dx
$$
$$
\begin{align}
\int_{0}^{1} \frac{1}{x^{2}} \sin\left( \frac{1}{x} \right) dx &= \int_{+\infty}^{1} \sin(u) du \\
&= -\cos(u) |_{+\infty}^{1} \\
&\underbrace{ = }_{ D.C.V. } \left. -\cos\left( \frac{1}{x} \right) \right|_{0}^{1} \\
&= -\cos\left( \frac{1}{1} \right) + \cos\left( \frac{1}{0} \right)
\end{align}
$$
En este caso, podemos determinar que la integral no converge ni diverge, sino que oscila, ya que la expresamos como la suma de dos términos: $-\cos(1)$ que es un valor real, y $\lim_{ x \to +\infty } \cos\left( \frac{1}{x} \right)$, que no es determinado.

### Parte d
$$
\int_{-\infty}^{+\infty} \frac{1}{1 + x^{2}} dx = \arctan(x) |_{-\infty}^{+\infty}
$$
Lo analizamos en dos partes:
$$
\begin{align}
\arctan(x) |_{-\infty}^{+\infty} &= \arctan(x) |_{-\infty}^{0} + \arctan(x) |_{0}^{+\infty} \\
&= \arctan(0) - \lim_{ x \to -\infty } \arctan(x) + \lim_{ x \to +\infty } \arctan(x) - \arctan(0) \\
&= \lim_{ x \to +\infty } \arctan(x) - \lim_{ x \to -\infty } \arctan(x)
\end{align}
$$
Estudiamos los límites correspondientes:
$$
\lim_{ x \to +\infty } \arctan(x) = \frac{\pi}{2}
$$
$$
\lim_{ x \to -\infty } \arctan(x) = -\frac{\pi}{2}
$$
De esta forma:
$$
\int_{-\infty}^{+\infty} \frac{1}{1 + x^{2}} dx = \arctan(x) |_{-\infty}^{+\infty} = \lim_{ x \to +\infty } \arctan(x) - \lim_{ x \to -\infty } \arctan(x) = \frac{\pi}{2} - \left( -\frac{\pi}{2} \right) = \pi
$$
En conclusión, $\int_{-\infty}^{+\infty} \frac{1}{1 + x^{2}} dx$ es convergente, y converge a $\pi$.

### Parte e
$$
\int_{-\infty}^{+\infty} \frac{1}{e^{x} + e^{-x}} dx = \int_{-\infty}^{+\infty} \frac{e^{x}}{e^{2x} + 1} dx
$$
Aplicamos cambio de variable:
$$
u = e^{x} \implies du = e^{x} dx
$$
$$
\begin{align}
\int_{-\infty}^{+\infty} \frac{e^{x}}{e^{2x} + 1} dx &= \int_{0}^{+\infty} \frac{1}{u^{2} + 1} du \\
&= \int_{0}^{1} \frac{1}{u^{2} + 1} du + \int_{1}^{+\infty} \frac{1}{u^{2} + 1} du \\
&= \arctan(u)|_{0}^{1} + \arctan(u)|_{1}^{+\infty} \\
&\underbrace{ = }_{ D.C.V. } \arctan(e^{x})|_{-\infty}^{0} + \arctan(e^{x})|_{0}^{+\infty} \\
&= \cancel{ \lim_{ x \to 0 } \arctan(e^{x}) } - \lim_{ x \to -\infty } \arctan(e^{x}) + \lim_{ x \to +\infty } \arctan(e^{x}) - \cancel{ \lim_{ x \to 0 } \arctan(e^{x}) } \\
&= \lim_{ x \to +\infty } \arctan(e^{x}) - \lim_{ x \to -\infty } \arctan(e^{x})
\end{align}
$$
Estudiamos cada límite:
$$
\lim_{ x \to +\infty } \arctan(e^{x}) = \frac{\pi}{2}
$$
$$
\lim_{ x \to -\infty } \arctan(e^{x}) = \arctan(0) = 0
$$

De esta manera:
$$
\int_{-\infty}^{+\infty} \frac{1}{e^{x} + e^{-x}} dx = \frac{\pi}{2} + 0 = \frac{\pi}{2}
$$
y, por lo tanto, la integral es convergente, y converge a $\frac{\pi}{2}$

---
## Ejercicio 3
$$
\begin{align}
\int_{1}^{+\infty} \left( \frac{x}{2x^{2} + 2k} - \frac{k}{x + 1} \right) dx &= \int_{1}^{+\infty} \frac{1}{2} \cdot \frac{x}{x^{2} + k} - k \cdot \frac{1}{x + 1} dx
\end{align}
$$

Ahora, pasemos a analizar cada término, buscando una primitiva para cada uno:
$$
\begin{align}
\int \frac{1}{2} \cdot \frac{x}{x^{2} + k} &= \frac{1}{2} \cdot \int \frac{x}{x^{2} + k} \\
&= \frac{1}{2} \cdot \left( \frac{1}{2} \cdot \log(x^{2} + k) \right) \\
&= \frac{1}{4} \cdot \log(x^{2} + k) \\
&= \log\left( (x^{2} + k)^{\frac{1}{4}} \right)
\end{align}
$$
$$
\int k \cdot \frac{1}{x + 1} = k \cdot \int \frac{1}{x + 1} = k \cdot \log(x + 1) = \log((x + 1)^{k})
$$

Entonces, considerando la integral general:
$$
\begin{align}
\int_{1}^{+\infty} \frac{1}{2} \cdot \frac{x}{x^{2} + k} - k \cdot \frac{1}{x + 1} dx &= \left. \left( \log\left( (x^{2} + k)^{\frac{1}{4}} \right) - \log((x + 1)^{k}) \right) \right|_{1}^{+\infty} \\
&= \left. \left( \log\left( \frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} \right) \right) \right|_{1}^{+\infty} \\
&= \lim_{ x \to +\infty } \log\left( \frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} \right) - \log\left( \frac{(1 + k)^{\frac{1}{4}}}{2^{k}} \right)
\end{align}
$$
$\log\left( \frac{(1 + k)^{\frac{1}{4}}}{2^{k}} \right)$ es un valor finito $\forall k > 0$. De esta manera, resta analizar el límite del otro término:
$$
\lim_{ x \to +\infty } \log\left( \frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} \right)
$$
Estudiemos el comportamiento de la fracción interna:
$$
\lim_{ x \to +\infty } \frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} \sim \lim_{ x \to +\infty } \frac{(x^{2})^{\frac{1}{4}}}{x^{k}} = \lim_{ x \to +\infty } \frac{\sqrt{ x }}{x^{k}} = \lim_{ x \to +\infty } x^{\frac{1}{2} - k}
$$
Sustituimos en el logaritmo:
$$
\lim_{ x \to +\infty } \log\left( \frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} \right) \sim \lim_{ x \to +\infty } \log\left( x^{\frac{1}{2} - k} \right) = \lim_{ x \to +\infty } \left( \frac{1}{2} - k \right) \cdot \log(x) = \left( \frac{1}{2} - k \right) \cdot \lim_{ x \to +\infty } \log(x)
$$


Por lo tanto, necesitamos un valor $k > 0$ tal que $\lim_{ x \to +\infty } \left( \frac{1}{2} - k \right) \cdot \log(x) < \infty$. Sabemos que $\lim_{ x \to +\infty } \log(x) = +\infty$.

De esta manera:
- Si $k < \frac{1}{2}$, $\left( \frac{1}{2} - k \right) \cdot \lim_{ x \to +\infty } \log(x) = +\infty$
- Si $k > \frac{1}{2}$, $\left( \frac{1}{2} - k \right) \cdot \lim_{ x \to +\infty } \log(x) = -\infty$

Entonces, la única posibilidad es $k = \frac{1}{2}$, de tal forma que $\left( \frac{1}{2} - k \right) \cdot \lim_{ x \to +\infty } \log(x) = 0$

Ahora, procedemos a calcular a que valor converge la integral:
$$
\begin{align}
\int_{1}^{+\infty} \frac{1}{2} \cdot \frac{x}{x^{2} + k} - k \cdot \frac{1}{x + 1} dx &= \lim_{ x \to +\infty } \log\left( \frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} \right) - \log\left( \frac{(1 + k)^{\frac{1}{4}}}{2^{k}} \right) \\
&= \lim_{ x \to +\infty } \log\left( \frac{\left( x^{2} + \frac{1}{2} \right)^{\frac{1}{4}}}{(x + 1)^{\frac{1}{2}}} \right) - \log\left( \frac{\left( 1 + \frac{1}{2} \right)^{\frac{1}{4}}}{2^{\frac{1}{2}}} \right) \\
&= \lim_{ x \to +\infty } \log\left( \sqrt[4]{ \frac{x^{2} + \frac{1}{2}}{x^{2} + 2x + 1} } \right) - \log\left( \sqrt[4]{ \frac{3}{8} } \right)
\end{align}
$$
Estudiamos el límite:
$$
\lim_{ x \to +\infty } \log\left( \sqrt[4]{ \frac{x^{2} + \frac{1}{2}}{x^{2} + 2x + 1} } \right) = \lim_{ x \to +\infty } \log\left( \sqrt[4]{ \frac{x^{2}}{x^{2}} } \right) = \lim_{ x \to +\infty } \log\left( \sqrt[4]{ 1 } \right) = \lim_{ x \to +\infty } \log\left( 1 \right) = 0
$$

En conclusión, la integral es convergente para $k = \frac{1}{2}$ y
$$
\int_{1}^{+\infty} \left( \frac{x}{2x^{2} + 2k} - \frac{k}{x + 1} \right) dx = -\log\left( \sqrt[4]{ \frac{3}{8} } \right)
$$

ACLARACIÓN:
Sobre los límites:
Decir que $\lim_{ x \to +\infty } \frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} \sim \lim_{ x \to +\infty } \frac{(x^{2})^{\frac{1}{4}}}{x^{k}}$ no es del todo correcto, en su lugar:
Como $\frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} \sim \frac{(x^{2})^{\frac{1}{4}}}{x^{k}}$ cuando $x \to +\infty$, entonces $\lim_{ x \to +\infty } \frac{(x^{2} + k)^{\frac{1}{4}}}{(x + 1)^{k}} = \lim_{ x \to +\infty } \frac{(x^{2})^{\frac{1}{4}}}{x^{k}}$

---
## Ejercicio 4
### Parte a
$$
\frac{\sin(x)}{\sqrt{ x }} + \frac{\sin^{2}(x)}{x} \sim \frac{\sin(x)}{\sqrt{ x }}
$$
Probemos aplicar el criterio de equivalencia:
$$
\frac{\sin(x)}{\sqrt{ x }} + \frac{\sin^{2}(x)}{x} \sim \frac{\sin(x)}{\sqrt{ x }} \implies \lim_{ x \to \infty } \frac{\frac{\sin(x)}{\sqrt{ x }} + \frac{\sin^{2}(x)}{x}}{\frac{\sin(x)}{\sqrt{ x }}} = 1
$$
$$
\begin{align}
\lim_{ x \to +\infty } \frac{\frac{\sin(x)}{\sqrt{ x }} + \frac{\sin^{2}(x)}{x}}{\frac{\sin(x)}{\sqrt{ x }}} &= \lim_{ x \to +\infty } \frac{\sqrt{ x } \sin(x)}{\sqrt{ x } \sin(x)} + \frac{\sqrt{ x } \sin^{2}(x)}{x \sin(x)} \\
&= \lim_{ x \to +\infty } \frac{\cancel{ \sqrt{ x } \sin(x) }}{\cancel{ \sqrt{ x } \sin(x) }} + \frac{\cancel{ \sqrt{ x } } \cancel{ \sin(x) } \sin(x)}{\cancel{ \sqrt{ x } }\sqrt{ x } \cancel{ \sin(x) }} \\
&= \lim_{ x \to +\infty } 1 + \frac{\sin(x)}{\sqrt{ x }} \\
&= \lim_{ x \to +\infty } 1 + \lim_{ x \to +\infty } \frac{\sin(x)}{\sqrt{ x }} \\
&= 1 + 0 \\
&= 1
\end{align}
$$
De esta forma, probamos que para $x \to +\infty$.

### Parte b
$$
\int_{1}^{+\infty} \frac{\sin(x)}{\sqrt{ x }} dx < \infty
$$
ACLARACIÓN:
Como el término no es siempre positivo, y tampoco es absolutamente convergente, lo mejor es intentar integrar directamente, aplicando partes:
$$
\int_{1}^{x} \frac{\sin(t)}{\sqrt{ t }} dt = \int_{1}^{x} \sin(t) \cdot \frac{1}{\sqrt{ t }} dt
$$
$$
\left[
\begin{align}
&f(x) = \frac{1}{\sqrt{ t }} &f'(x) = -\frac{\frac{1}{2\sqrt{ t }}}{t} = -\frac{1}{2t^{\frac{3}{2}}} \\
&g'(x) = \sin(t) &g(x) = -\cos(t) \\
\end{align}
\right]
$$
$$
\begin{align}
\int_{1}^{x} \frac{\sin(t)}{\sqrt{ t }} dt &= \left. -\frac{\cos(t)}{\sqrt{ t }} \right|_{1}^{x} - \int_{1}^{x} \frac{\cos(t)}{2t^{\frac{3}{2}}} dt \\
&= -\frac{\cos(x)}{\sqrt{ x }} + \cos(1) - \int_{1}^{x} \frac{\cos(t)}{2t^{\frac{3}{2}}} dt
\end{align}
$$
Ahora, analicemos la nueva integral: $\int_{1}^{x} \frac{\cos(t)}{2t^{\frac{3}{2}}} dt$

En este caso, sí conviene estudiar la convergencia absoluta:
$$
|\cos(t)| \leq 1 \implies \frac{|\cos(t)|}{2t^{\frac{3}{2}}} \leq \frac{1}{2t^{\frac{3}{2}}}
$$
Sabemos que $\frac{1}{t^{\alpha}}$ es convergente para todo $\alpha \geq 1$, entonces deducimos que $\frac{1}{2t^{\frac{3}{2}}}$ es convergente.
De esta manera, por el criterio de comparación deducimos que $\int_{1}^{+\infty} \frac{|\cos(t)|}{2t^{\frac{3}{2}}} dt$ es convergente.

Entonces, $\int_{1}^{+\infty} \frac{\cos(t)}{2t^{\frac{3}{2}}} dt$ es absolutamente converge, lo que implica que también es convergente:
$$
\lim_{ x \to \infty } \int_{1}^{x} \frac{\cos(t)}{2t^{\frac{3}{2}}} dt = L
$$

De esta forma:
$$
\begin{align}
\lim_{ x \to \infty } \int_{1}^{x} \frac{\sin(t)}{\sqrt{ t }} dt &= \lim_{ x \to \infty } -\frac{\cos(x)}{\sqrt{ x }} + \cos(1) - \int_{1}^{x} \frac{\cos(t)}{2t^{\frac{3}{2}}} dt \\
&= \lim_{ x \to \infty } -\frac{\cos(x)}{\sqrt{ x }} + \lim_{ x \to \infty } \cos(1) - \lim_{ x \to \infty } \int_{1}^{x} \frac{\cos(t)}{2t^{\frac{3}{2}}} dt \\
&= 0 + \cos(1) - L \\
&= \cos(1) - L
\end{align}
$$

En conclusión, $\int_{1}^{+\infty} \frac{\sin(x)}{\sqrt{ x }} dx < \infty$, y $\int_{1}^{+\infty} \frac{\sin(x)}{\sqrt{ x }} dx = \cos(1) - L$

Ahora, proseguimos a demostrar la divergencia de $\int_{1}^{+\infty} \left( \frac{\sin(x)}{\sqrt{ x }} + \frac{\sin^{2}(x)}{x} \right) dx$
$$
\int_{1}^{+\infty} \left( \frac{\sin(x)}{\sqrt{ x }} + \frac{\sin^{2}(x)}{x} \right) dx = \infty
$$

$$
\int_{1}^{+\infty} \left( \frac{\sin(x)}{\sqrt{ x }} + \frac{\sin^{2}(x)}{x} \right) dx = \int_{1}^{+\infty} \frac{\sin(x)}{\sqrt{ x }} dx + \int_{1}^{+\infty} \frac{\sin^{2}(x)}{x} dx
$$
Sabemos que $\int_{1}^{+\infty} \frac{\sin(x)}{\sqrt{ x }} dx < \infty$. Por lo tanto, para probar que la integral total diverge, tenemos que verificar que $\int_{1}^{+\infty} \frac{\sin^{2}(x)}{x} dx = \infty$.

Como sabemos que $\sin^{2}(x) = 1 - \cos(2x)$ (identidad trigonométrica del ángulo doble), podemos reescribir el término general:
$$
\int_{1}^{+\infty} \frac{\sin^{2}(x)}{x} dx = \int_{1}^{+\infty} \frac{1 - \cos(2x)}{2x} dx = \int_{1}^{+\infty} \frac{1}{2x} - \frac{\cos(2x)}{2x} dx = \int_{1}^{+\infty} \frac{1}{2x} dx - \int_{1}^{+\infty} \frac{\cos(2x)}{2x} dx
$$
Sabemos que $\int_{1}^{+\infty} \frac{1}{2x} dx = +\infty$, ya que $\frac{1}{2x} = \frac{1}{2} \cdot \frac{1}{x}$, y $\frac{1}{2} \cdot \int_{1}^{+\infty} \frac{1}{x} dx = \frac{1}{2} \cdot +\infty = +\infty$. Entonces, tenemos que analizar el término restante, para lo cual aplicaremos partes:
$$
\left[
\begin{align}
&f(x) = \frac{1}{2x} &f'(x) = -\frac{1}{2x^{2}} \\
&g'(x) = \cos(2x) &g(x) = \frac{\sin(2x)}{2} \\
\end{align}
\right]
$$
$$
\begin{align}
\int_{1}^{x} \frac{\cos(2t)}{2t} dt &= \left. \frac{\sin(2t)}{4t} \right|_{1}^{x} + \int_{1}^{x} \frac{\sin(2t)}{4t^{2}} dt \\
&= \frac{\sin(2x)}{4x} - \frac{\sin(2)}{4} + \int_{1}^{x} \frac{\sin(2t)}{4t^{2}} dt
\end{align}
$$
Ahora, analicemos la integral $\int_{1}^{+\infty} \frac{\sin(2x)}{4x^{2}} dx$. Podemos aplicar criterio de comparación:
$$
\frac{|\sin(2x)|}{4x^{2}} \leq \frac{1}{x^{2}}
$$
Sabemos que $\int_{1}^{+\infty} \frac{1}{x^{2}} dx$ converge. Por lo tanto, $\int_{1}^{+\infty} \frac{\sin(2x)}{4x^{2}} dx$ es absolutamente convergente, lo que implica que es convergente.

De esta manera, sabemos que $\int_{1}^{+\infty} \frac{\sin(2x)}{4x^{2}} dx = L$ finito:
$$
\begin{align}
\int_{1}^{x} \frac{\cos(2t)}{2t} dt &= \frac{\sin(2x)}{4x} - \frac{\sin(2)}{4} + \int_{1}^{x} \frac{\sin(2t)}{4t^{2}} dt \\
&= \frac{\sin(2x)}{4x} - \frac{\sin(2)}{4} + L
\end{align}
$$

Entonces, analizamos el límite cuando $x \to \infty$:
$$
\begin{align}
\lim_{ x \to \infty } \int_{1}^{x} \frac{\cos(2t)}{2t} dt &= \lim_{ x \to \infty } \frac{\sin(2x)}{4x} - \frac{\sin(2)}{4} + L \\
&= \lim_{ x \to \infty } \frac{\sin(2x)}{4x} - \lim_{ x \to \infty } \frac{\sin(2)}{4} + \lim_{ x \to \infty } L \\
&= 0 - \frac{\sin(2)}{4} + L \\
&= L - \frac{\sin(2)}{4}
\end{align}
$$
Como vemos, $\int_{1}^{+\infty} \frac{\cos(2x)}{2x} dx < \infty$. Por lo tanto:
$$
\int_{1}^{+\infty} \frac{\sin^{2}(x)}{x} dx = \int_{1}^{+\infty} \frac{1}{2x} dx - \int_{1}^{+\infty} \frac{\cos(2x)}{2x} dx = +\infty - \left( L - \frac{\sin(2)}{4} \right) = +\infty
$$

En conclusión, $\int_{1}^{+\infty} \frac{\sin^{2}(x)}{x} dx = \infty$, lo que implica que $\int_{1}^{+\infty} \left( \frac{\sin(x)}{\sqrt{ x }} + \frac{\sin^{2}(x)}{x} \right) dx = \infty$.

---
## Ejercicio 5
### Parte a
Sabemos que $\lim_{ x \to \infty } f(x)g(x) = L \in \mathbb{R}$. Además, sus derivadas $f'$ y $g'$ son funciones integrables en el dominio en el que están definidas.

Ahora, considerando la definición de integrales impropias:
$$
\lim_{ x \to \infty } f(x)g(x) = L \in \mathbb{R} = \int_{a}^{+\infty} (f(x)g(x))' dx
$$
Desarrollamos la integral:
$$
\int_{a}^{+\infty} (f(x)g(x))' dx = \int_{a}^{+\infty} f'(x)g(x) + f(x)g'(x) dx = \int_{a}^{+\infty} f'(x)g(x) + \int_{a}^{+\infty} f(x)g'(x) dx
$$
Ahora, como $\int_{a}^{+\infty} (f(x)g(x))' dx$ converge y lo hace a $L$ (por definición), entonces:
$$
\int_{a}^{+\infty} (f(x)g(x))' dx = \int_{a}^{+\infty} f'(x)g(x) + \int_{a}^{+\infty} f(x)g'(x) dx = L
$$

De esta forma, analicemos cada implicación:
1. $\int_{a}^{+\infty} f'(x)g(x) dx < \infty \implies \int_{a}^{+\infty} f(x)g'(x) dx < \infty$
$$
\int_{a}^{+\infty} f'(x)g(x) + \int_{a}^{+\infty} f(x)g'(x) dx = L \implies L_{1} + \int_{a}^{+\infty} f(x)g'(x) dx = L \implies \int_{a}^{+\infty} f(x)g'(x) dx = L - L_{1}
$$
Como $\int_{a}^{+\infty} f(x)g'(x) dx = L - L_{1}$, siendo $L, L_{1} \in \mathbb{R}$, entonces necesariamente $\int_{a}^{+\infty} f(x)g'(x) dx = L_{2} \in \mathbb{R} < \infty$.

2. $\int_{a}^{+\infty} f(x)g'(x) dx < \infty \implies \int_{a}^{+\infty} f'(x)g(x) dx < \infty$
$$
\int_{a}^{+\infty} f'(x)g(x) + \int_{a}^{+\infty} f(x)g'(x) dx = L \implies \int_{a}^{+\infty} f'(x)g(x) + L_{2} = L \implies \int_{a}^{+\infty} f'(x)g(x) dx = L - L_{2}
$$
Como $\int_{a}^{+\infty} f'(x)g(x) dx = L - L_{2}$, siendo $L, L_{2} \in \mathbb{R}$, entonces necesariamente $\int_{a}^{+\infty} f'(x)g(x) dx = L_{1} \in \mathbb{R} < \infty$.

ACLARACIÓN: Conviene explicitar como se desarrolla la regla de Barrow.

### Parte b
Clasificamos las integrales propuestas:
#### Parte 1
Comenzamos con la primer integral:
$$
\int_{0}^{+\infty} \frac{\sin(t)}{t} dt
$$
La dividimos en dos integrales, para asegurar que manejamos un único inconveniente en cada una:
$$
\int_{0}^{+\infty} \frac{\sin(t)}{t} dt = \int_{0}^{1} \frac{\sin(t)}{t} dt + \int_{1}^{+\infty} \frac{\sin(t)}{t} dt
$$

- Función indeterminada en 0:
$$
\int_{0}^{1} \frac{\sin(t)}{t} dt
$$
Estudiamos:
$$
\int_{x}^{1} \frac{\sin(t)}{t} dt
$$
Y luego buscamos:
$$
\lim_{ x \to 0 } \int_{x}^{1} \frac{\sin(t)}{t} dt
$$
y en caso de ser finito, la función converge.

Sabemos que alrededor de 0, $\sin(t) \sim x$. Aplicamos desarrollo de Taylor de $\sin(t)$ en 0:
$$
\sin(t) = 0 + 1 \cdot t - 0 \cdot \frac{t^{2}}{2} - 1 \cdot \frac{t^{3}}{3!} + r(t) =t - \frac{t^{3}}{6} + r(t) \implies \sin(t) \sim t - \frac{t^{3}}{6}
$$
De esta manera, podemos asumir que:
$$
\frac{\sin(t)}{t} \sim \frac{t - \frac{t^{3}}{6}}{t} = \frac{t}{t} - \frac{\frac{t^{3}}{6}}{t} = 1 - \frac{t^{2}}{6}
$$
Y si analizamos el límite cuando $t \to 0$:
$$
\lim_{ t \to \infty } \frac{\sin(t)}{t} \sim \lim_{ t \to \infty } 1 - \frac{t^{2}}{6} = 1 - \frac{0}{6} = 1
$$
Por lo que:
$$
t \sim \sin(t) \text{ cuando } t \to 0
$$
$$
\int_{x}^{1} 1 - \frac{t^{2}}{6} dt = \int_{x}^{1} 1 dt - \int_{x}^{1} \frac{t^{2}}{6} dt = t |_{x}^{1} - \left. \frac{t^{2}}{6} \right|_{x}^{1} = 1 - x - \left( \frac{1^{2}}{6} - \frac{x^{2}}{6} \right) = 1 - x - \frac{1}{6} + \frac{x^{2}}{6} = \frac{5}{6} - x + \frac{x^{2}}{6}
$$

Finalmente, estudiamos el límite de la expresión cuando $x \to 0$:
$$
\lim_{ x \to 0 } \frac{5}{6} - x + \frac{x^{2}}{6} = \frac{5}{6} - 0 + \frac{0^{2}}{6} = \frac{5}{6}
$$

En conclusión, como $\int_{0}^{1} \frac{t - \frac{t^{3}}{6}}{t} dt$ es convergente, entonces por el criterio de equivalentes,  $\int_{0}^{1} \frac{\sin(t)}{t} dt$ también lo es.

ACLARACIÓN:
En realidad, la integral propuesta no es una impropia. Lo que podríamos haber hecho para facilitar los cálculos es considerar el límite $\lim_{ t \to 0 } \frac{\sin(t)}{t} = 1$. Por lo tanto, la integral no es impropia, sino que es continua en todo el intervalo $[0, 1]$. De esta manera, podríamos haber considerado este resultado:
Sabiendo que la integral $\int_{0}^{1} \frac{t}{t} dt = \int_{0}^{1} 1 dt$ converge, y $1 > \frac{\sin(t)}{t} \implies \int_{0}^{1} 1 dt > \int_{0}^{1} \frac{\sin(t)}{t} dt$, por el criterio de equivalentes concluimos que la integral $\int_{0}^{1} \frac{\sin(t)}{t} dt$ también es convergente.

- Dominio infinito:
$$
\int_{1}^{+\infty} \frac{\sin(t)}{t} dt
$$
Aquí podemos aplicar partes:
$$
\left[
\begin{align}
&f(t) = \frac{1}{t} &&f'(t) = -\frac{1}{t^{2}} \\
&g'(t) = \sin(t) &&g(t) = -\cos(t)
\end{align}
\right]
$$
$$
\begin{align}
\int_{1}^{x} \frac{\sin(t)}{t} dt &= \left. -\frac{\cos(t)}{t} \right|_{1}^{x} - \int_{1}^{x} \frac{\cos(t)}{t^{2}} dt \\
&= -\frac{\cos(1)}{1} + \frac{\cos(x)}{x} - \int_{1}^{x} \frac{\cos(t)}{t^{2}} dt
\end{align}
$$
Entonces, si analizamos el límite a infinito:
$$
\lim_{ x \to +\infty } \int_{1}^{x} \frac{\sin(t)}{t} dt = \lim_{ x \to +\infty }  -\cos(1) + \frac{\cos(x)}{x} - \int_{1}^{x} \frac{\cos(t)}{t^{2}} dt = -\cos(1) - \int_{1}^{+\infty} \frac{\cos(t)}{t^{2}} dt
$$
Por lo tanto, la convergencia depende de $\int_{1}^{+\infty} \frac{\cos(t)}{t^{2}} dt$. En este caso, podemos analizar la convergencia absoluta:
$$
\left| \frac{\cos(t)}{t^{2}} \right| = \frac{|\cos(t)|}{t^{2}} \leq \frac{1}{t^{2}}
$$
Sabemos que $\int_{1}^{+\infty} \frac{1}{t^{2}} dt$ es convergente, por lo que aplicando el criterio de comparación, $\int_{1}^{+\infty} \frac{|\cos(t)|}{t^{2}} dt$ también lo es.

De esta manera, como $\int_{1}^{+\infty} \frac{\cos(t)}{t^{2}} dt$ es absolutamente convergente, llegamos a la conclusión de que es convergente, y por lo tanto $\int_{1}^{+\infty} \frac{\sin(t)}{t} dt$ también lo es, ya que logramos expesarla como la suma de dos términos finitos (expresiones convergentes).

En conclusión, $\int_{0}^{+\infty} \frac{\sin(t)}{t} dt$ es convergente, ya que $\int_{0}^{+\infty} \frac{\sin(t)}{t} dt = \int_{0}^{1} \frac{\sin(t)}{t} dt + \int_{1}^{+\infty} \frac{\sin(t)}{t} dt$ y cada término es convergente.

Proseguimos con la segunda integral:
$$
\int_{1}^{+\infty} \frac{\sin(t)}{t^{2}} dt
$$
Este caso es más sencillo que el anterior, ya que aparentemente tenemos un solo problema: dominio infinito (aunque en el anterior esto no sucedía).

Analicemos la convergencia absoluta de la sucesión:
$$
\left| \frac{\sin(t)}{t^{2}} \right| = \frac{|\sin(t)|}{t^{2}} \leq \frac{1}{t^{2}}
$$

Sabemos que $\int_{1}^{+\infty} \frac{1}{t^{2}} dt$ es convergente, por lo que aplicando el criterio de comparación, $\int_{1}^{+\infty} \frac{|\sin(t)|}{t^{2}} dt$ es convergente.

En conclusión, como $\int_{1}^{+\infty} \frac{\sin(t)}{t^{2}} dt$ es absolutamente convergente, determinamos que la integral es convergente.

#### Parte 2
Comenzamos evaluando la primera integral:
$$
\int_{0}^{+\infty} \sin(t^{2}) dt
$$
En este caso, consideraremos la sugerencia provista:
$$
\int_{0}^{+\infty} \sin(t^{2}) dt = \int_{0}^{+\infty} 2t \cdot \sin(t^{2}) \cdot \frac{1}{2t} dt
$$
y aplicaremos partes:
$$
\left[
\begin{align}
&f(t) = \frac{1}{2t} &f'(t) = -\frac{1}{2t^{2}} \\
&g'(t) = 2t \cdot \sin(t^{2}) &g(t) = -\cos(t^{2})
\end{align}
\right]
$$
$$
\begin{align}
\int_{0}^{x} 2t \cdot \sin(t^{2}) \cdot \frac{1}{2t} dt &= \left. -\frac{\cos(t^{2})}{2t} \right|_{0}^{x} - \int_{0}^{x} \frac{\cos(t^{2})}{2t^{2}} dt
\end{align}
$$
Analizamos los límites de $\frac{\cos(t^{2})}{2t}$ evaluado en $0$ y $+\infty$:
$$
\lim_{ t \to +\infty } \frac{\cos(t^{2})}{2t}
$$
$$
\begin{align}
\lim_{ t \to +\infty } \frac{-1}{2t} \leq &\lim_{ t \to +\infty } \frac{\cos(t^{2})}{2t} \leq \lim_{ t \to +\infty } \frac{1}{2t} \\
\frac{-1}{+\infty} \leq &\lim_{ t \to +\infty } \frac{\cos(t^{2})}{2t} \leq \frac{1}{+\infty} \\
0 \leq &\lim_{ t \to +\infty } \frac{\cos(t^{2})}{2t} \leq 0 \implies \lim_{ t \to +\infty } \frac{\cos(t^{2})}{2t} = 0
\end{align}
$$
$$
\lim_{ t \to 0 } \frac{\cos(t^{2})}{2t} = \frac{\cos(0^{2})}{2 \cdot 0} = \frac{1}{0} = +\infty
$$

Ahora, si procedemos a evaluar la integral $\int_{0}^{x} \frac{\cos(t^{2})}{2t^{2}} dt$, podemos ver que:
$$
\left| \frac{\cos(t^{2})}{2t^{2}} \right| = \frac{|\cos(t^{2})|}{2t^{2}} \leq \frac{1}{2t^{2}} < \frac{1}{t^{2}}
$$

Entonces, como sabemos que $\int_{0}^{+\infty} \frac{1}{t^{2}} dt$ es convergente, por criterio de comparación, deducimos que $\int_{0}^{+\infty} \frac{|\cos(t^{2})|}{2t^{2}} dt$.

Por lo tanto, como $\int_{0}^{+\infty} \frac{\cos(t^{2})}{2t^{2}} dt$ es absolutamente convergente, también es convergente.

Entonces, analizando la integral propuesta:
$$
\begin{align}
\int_{0}^{+\infty} 2t \cdot \sin(t^{2}) \cdot \frac{1}{2t} dt &= \lim_{ t \to +\infty } -\frac{\cos(t^{2})}{2t} + \lim_{ t \to 0 } \frac{\cos(t^{2})}{2t} - \int_{0}^{+\infty} \frac{\cos(t^{2})}{2t^{2}} dt \\
&= 0 + +\infty - L \\
&= +\infty
\end{align}
$$

En conclusión, la integral $\int_{0}^{+\infty} \sin(t^{2}) dt$ es divergente.

CORRECCIÓN: El resultado es completamente incorrecto.

Separamos la integral en dos partes:
$$
\int_{0}^{+\infty} \sin(t^{2}) dt = \int_{0}^{1} \sin(t^{2}) dt + \int_{1}^{+\infty} \sin(t^{2}) dt
$$
Analizamos el primer término: es una integral como las vistas en Cálculo 1, una función continua en un intervalo acotado. Por lo tanto, la integral $\int_{0}^{1} \sin(t^{2}) dt$ es convergente.

Pasamos al segundo término y aplicamos partes:
$$
\left[
\begin{align}
&f(t) = \frac{1}{2t} &f'(t) = -\frac{1}{2t^{2}} \\
&g'(t) = 2t \cdot \sin(t^{2}) &g(t) = -\cos(t^{2})
\end{align}
\right]
$$
$$
\begin{align}
\int_{1}^{x} 2t \cdot \sin(t^{2}) \cdot \frac{1}{2t} dt &= \left. -\frac{\cos(t^{2})}{2t} \right|_{1}^{x} - \int_{1}^{x} \frac{\cos(t^{2})}{2t^{2}} dt \\
&= -\frac{\cos(x^{2})}{2x} + \frac{\cos(1)}{2} - \int_{1}^{x} \frac{\cos(t^{2})}{2t^{2}} dt
\end{align}
$$
Entonces, estudiamos cada término y su límite a $+\infty$:
$$
\lim_{ x \to +\infty } -\frac{\cos(x^{2})}{2x} = 0
$$
$$
\lim_{ x \to +\infty } \frac{\cos(1)}{2} = \frac{\cos(1)}{2}
$$
$$
\lim_{ x \to \infty } \int_{1}^{x} \frac{\cos(t^{2})}{2t^{2}} dt
$$
En este caso, tomamos como referencia un término conocido:
$$
\frac{\cos(t^{2})}{2t^{2}} \leq \left| \frac{\cos(t^{2})}{2t^{2}} \right| = \frac{|\cos(t^{2})|}{2t^{2}} \leq \frac{1}{t^{2}}
$$
Sabemos que $\int_{1}^{x} \frac{1}{t^{2}} dt$ es convergente, entonces aplicando criterio de comparación, determinamos que $\frac{\cos(t^{2})}{2t^{2}}$ también lo es (en realidad, es absolutamente convergente, y a partir de ahí llegamos a la conclusión anterior).

De esta manera:
$$
\int_{1}^{+\infty} 2t \cdot \sin(t^{2}) \cdot \frac{1}{2t} dt = \frac{\cos(1)}{2} + L
$$

Como $\int_{1}^{+\infty} \sin(t^{2}) dt$ está constituida como suma de términos reales finitos, deducimos que la integral es convergente.

En conclusión, como $\int_{0}^{1} \sin(t^{2}) dt < \infty$ y $\int_{1}^{+\infty} \sin(t^{2}) dt < \infty$, entonces $\int_{0}^{+\infty} \sin(t^{2}) dt$ es convergente.

Continuamos con la segunda integral presentada:
$$
\int_{1}^{+\infty} |\sin(t^{2})| dt
$$
Nuevamente, aplicamos partes:
$$
\left[
\begin{align}
&f(t) = \frac{1}{2t} &f'(t) = -\frac{1}{2t^{2}} \\
&g'(t) = 2t \cdot \sin(t^{2}) &g(t) = -\cos(t^{2})
\end{align}
\right]
$$
$$
\begin{align}
\int_{1}^{x} \left| 2t \cdot \sin(t^{2}) \cdot \frac{1}{2t} \right| dt &= \left. \left| -\frac{\cos(t^{2})}{2t} \right| \right|_{1}^{x} - \int_{1}^{x} \left| \frac{\cos(t^{2})}{2t^{2}} \right| dt \\
&= \left| \frac{\cos(x^{2})}{2x} \right| + \left| \frac{\cos(1)}{2} \right| - \int_{1}^{x} \left| \frac{\cos(t^{2})}{2t^{2}} \right| dt \\
\int_{1}^{+\infty} \left| 2t \cdot \sin(t^{2}) \cdot \frac{1}{2t} \right| dt &= \lim_{ x \to +\infty } \left| \frac{\cos(x^{2})}{2x} \right| + \left| \frac{\cos(1)}{2} \right| - \int_{1}^{+\infty} \left| \frac{\cos(t^{2})}{2t^{2}} \right| dt \\
&= 0 + \left| \frac{\cos(1)}{2} \right| - L
\end{align}
$$

Como vemos, tomando en cuenta el resultado de la integral anterior, logramos expresar la integral como la suma de términos e integrales convergentes (suma de números reales finitos).

En conclusión, la integral $\int_{1}^{+\infty} |\sin(t^{2})| dt$ es convergente.

CORRECCIÓN: nuevamente, el desarrollo es totalmente erróneo.
Tenemos que aplicar el siguiente cambio de variable:
$$
u = t^{2} \implies du = 2t dt \implies dt = \frac{du}{2t} = \frac{du}{2\sqrt{ u }}
$$
$$
\int_{1}^{+\infty} |\sin(t^{2})| dt = \int_{1}^{+\infty} \frac{|\sin(u)|}{2\sqrt{ u }} du
$$
Ahora, consideramos la desigualdad $|\sin(u)| \geq \sin^{2}(u) = \frac{1 - \cos(2u)}{2}$, tal que:
$$
\begin{align}
\int_{1}^{+\infty} \frac{|\sin(u)|}{2\sqrt{ u }} du \geq \int_{1}^{+\infty} \frac{1 - \cos(2u)}{2} \cdot \frac{1}{2\sqrt{ u }} du &= \int_{1}^{+\infty} \frac{1 - \cos(2u)}{4\sqrt{ u }} du \\
&= \int_{1}^{+\infty} \frac{1}{4\sqrt{ u }} - \frac{\cos(2u)}{4\sqrt{ u }} du \\
&= \int_{1}^{+\infty} \frac{1}{4\sqrt{ u }} du - \int_{1}^{+\infty} \frac{\cos(2u)}{4\sqrt{ u }} du \\
&= \frac{1}{4} \cdot \left( \int_{1}^{+\infty} \frac{1}{\sqrt{ u }} du - \int_{1}^{+\infty} \frac{\cos(2u)}{\sqrt{ u }} du \right)
\end{align}
$$
Deshacemos el cambio de variable y analizamos cada integral por separado:
$$
\int_{1}^{+\infty} \frac{1}{\sqrt{ u }} du = \int_{1}^{+\infty} \frac{1}{t} dt
$$
Como ya hemos probado anteriormente, $\int_{1}^{+\infty} \frac{1}{t^{\alpha}} du$ es divergente $\forall \alpha \leq 1$. Por lo tanto, en este caso la integral es divergente.

$$
\int_{1}^{+\infty} \frac{\cos(2u)}{\sqrt{ u }} du = \int_{1}^{+\infty} \frac{\cos(2t^{2})}{t} dt
$$
Para clasificarla, consideremos $\int_{1}^{+\infty} \sin(t^{2}) dt < \infty$. En este caso, el término $\frac{\cos(2t^{2})}{t}$ oscila cada vez más rápido, y a partir de cierto $t$, $\frac{\cos(2t^{2})}{t} < \sin(t^{2})$.

Por lo tanto, determinamos que por el criterio de comparación, $\int_{1}^{+\infty} \frac{\cos(2t^{2})}{t} du$ es convergente.

De esta forma:
$$
\int_{1}^{+\infty} |\sin(t^{2})| dt = \int_{1}^{+\infty} \frac{|\sin(u)|}{2\sqrt{ u }} du \geq \int_{1}^{+\infty} \frac{1 - \cos(2u)}{2} \cdot \frac{1}{2\sqrt{ u }} du = \int_{1}^{+\infty} \frac{1}{t} dt + \int_{1}^{+\infty} \frac{\cos(2t^{2})}{t} dt = L + +\infty = +\infty
$$

Por lo tanto, $\int_{1}^{+\infty} |\sin(t^{2})| dt$ es divergente:
$$
\int_{1}^{+\infty} |\sin(t^{2})| dt = +\infty
$$

---
## Ejercicio 6
### Parte a
$$
\int_{-\infty}^{+\infty} e^{-x^{2}} dx
$$
En este caso, la integral impropia es de primera clase: dominio infinito. No existe ningún valor de $x \in \mathbb{R}$ para el que la función $e^{-x^{2}}$ no esté definida.

Comparamos la función con otra conocida:
$$
e^{-x^{2}} =  \frac{1}{e^{x^{2}}} \leq \frac{1}{x^{2}}
$$
Sabemos que $\int_{1}^{+\infty} \frac{1}{x^{2}} dx$ es convergente, por lo que aplicando comparación, llegaos a la conclusión de que $\int_{1}^{+\infty} \frac{1}{e^{x^{2}}} dx$ también lo es.

Como la función $e^{-x^{2}} = \frac{1}{e^{x^{2}}}$ es una función par (lo que significa que $f(x) = f(-x)$), ya que el término $x$ está elevado a un número par, podemos asegurar que $\int_{1}^{+\infty} \frac{1}{e^{x^{2}}} dx = \int_{-\infty}^{-1} \frac{1}{e^{x^{2}}} dx$. De esta forma, determinamos que $\int_{-\infty}^{-1} \frac{1}{e^{x^{2}}} dx$ también es convergente.

Finalmente, analizamos $\int_{-1}^{1} \frac{1}{e^{x^{2}}} dx$. La función es continua en todo el intervalo, pues está definida en $[-1, 1]$, por lo que la integral es convergente.

En conclusión, como $\int_{-\infty}^{+\infty} e^{-x^{2}} dx = \int_{-\infty}^{-1} \frac{1}{e^{x^{2}}} dx + \int_{-1}^{1} \frac{1}{e^{x^{2}}} dx + \int_{1}^{+\infty} \frac{1}{e^{x^{2}}} dx = L_{1} + L_{2} + L_{3} < \infty$, la integral $\int_{-\infty}^{+\infty} e^{-x^{2}} dx$ es convergente.

### Parte b
$$
\int_{0}^{1} \frac{e^{-x}}{x} dx = \int_{0}^{1} \frac{1}{xe^{x}} dx
$$
Sabemos que $\int \frac{1}{x} dx$ es divergente en general (tanto para $\int_{0}^{1}$ como para $\int_{1}^{+\infty}$). Entonces, considerando que $\lim_{ x \to 0 } e^{x} = 1$, podemos asegurar que:
$$
\int_{x}^{1} \frac{1}{te^{t}} dt \sim \int_{x}^{1} \frac{1}{t} dt
$$
cuando $x \to 0$, por lo que son de la misma clase.

De esta manera, determinamos que por el criterio de equivalencias, como $\int_{0}^{1} \frac{1}{x} dx$ es divergente, entonces $\int_{0}^{1} \frac{e^{-x}}{x} dx$ también lo es.

### Parte c
$$
\int_{0}^{1} \frac{\log(x)}{\sqrt{ x }} dx
$$
El problema de la integral anterior se encuentra en $x \to 0$, ya que:
$$
\lim_{ x \to 0 } \log(x) = -\infty
$$
$$
\lim_{ x \to 0 } \sqrt{ x } = 0
$$

Aplicamos partes:
$$
\left[
\begin{align}
&f(x) = \log(x) \implies f'(x) = \frac{1}{x} \\
&g'(x) = \frac{1}{\sqrt{ x }} \implies g(x) = 2\sqrt{ x }
\end{align}
\right]
$$

$$
\begin{align}
\int_{0}^{1} \frac{\log(x)}{\sqrt{ x }} dx &= 2\sqrt{ x } \cdot \log(x) |_{0}^{1} - 2 \cdot \int_{0}^{1} \frac{\sqrt{ x }}{x} dx \\
&= \cancel{ 2\sqrt{ 1 } \cdot \log(1) } - \lim_{ x \to 0 } 2\sqrt{ x } \cdot \log(x) - 2 \cdot \int_{0}^{1} \frac{1}{\sqrt{ x }} dx
\end{align}
$$
Analizamos el límite:
$$
\lim_{ x \to 0 } 2\sqrt{ x } \cdot \log(x) = 2 \cdot \lim_{ x \to 0 } \frac{\log(x)}{x^{-\frac{1}{2}}} = \frac{-\infty}{+\infty}
$$
Aplicamos L'Hôpital:
$$
(\log(x))' = \frac{1}{x}
$$
$$
\left( x^{-\frac{1}{2}} \right)' = -\frac{1}{2} \cdot x^{-\frac{3}{2}}
$$
$$
\begin{align}
\implies 2 \cdot \lim_{ x \to 0 } \frac{\log(x)}{x^{-\frac{1}{2}}} &= 2 \cdot \lim_{ x \to 0 } \frac{\frac{1}{x}}{-\frac{1}{2} \cdot x^{-\frac{3}{2}}} \\
&= -4 \cdot \lim_{ x \to 0 } \frac{1}{x^{-\frac{1}{2}}} \\
&= -4 \cdot \lim_{ x \to 0 } x^{\frac{1}{2}} \\
&= -4 \cdot 0 \\
&= 0
\end{align}
$$

Estudiamos la integral $\int_{0}^{1} \frac{1}{\sqrt{ x }} dx$: sabemos que $\int_{0}^{1} \frac{1}{x^{\alpha}} dx < \infty, \forall \alpha < 1$. Por lo tanto, la integral presentada es convergente.

De esta forma:
$$
\int_{0}^{1} \frac{\log(x)}{\sqrt{ x }} dx = -0 - 2 \cdot L = 2 \cdot L
$$

En conclusión, $\int_{0}^{1} \frac{\log(x)}{\sqrt{ x }} dx$ es convergente.

### Parte d
$$
\int_{1}^{+\infty} \frac{\sin(x)}{x^{2}} dx
$$
En este caso, conviene aplicar criterio de comparación con el valor absoluto:
$$
\left| \frac{\sin(x)}{x^{2}} \right| = \frac{|\sin(x)|}{x^{2}} \leq \frac{1}{x^{2}}
$$
Ahora, sabemos que $\int_{1}^{+\infty} \frac{1}{x^{2}} dx$ es convergente, por lo que aplicando criterio de comparación, $\int_{1}^{+\infty} \frac{|\sin(x)|}{x^{2}} dx$ también lo es.

De esta manera, probamos que $\int_{1}^{+\infty} \frac{\sin(x)}{x^{2}} dx$ es absolutamente convergente.

En conclusión, como $\int_{1}^{+\infty} \frac{\sin(x)}{x^{2}} dx$ es absolutamente convergente, entonces es convergente.

### Parte e
$$
\int_{0}^{+\infty} \sin ^{2}(t) dt
$$
Aplicamos partes:
$$
\left[
\begin{align}
&f(x) = \sin(t) &f'(x) = \cos(t) \\
&g'(x) = \sin(t) &g(x) = -\cos(t)
\end{align}
\right]
$$
$$
\begin{align}
\int_{0}^{+\infty} \sin ^{2}(t) dt &= -\sin(t)\cos(t) |_{0}^{+\infty} + \int_{0}^{+\infty} \cos ^{2}(t) dt \\
&= -\sin(t)\cos(t) |_{0}^{+\infty} + \int_{0}^{+\infty} 1 - \sin ^{2}(t) dt \\
&= -\sin(t)\cos(t) |_{0}^{+\infty} + \int_{0}^{+\infty} 1 dt - \int_{0}^{+\infty} \sin ^{2}(t) dt \\
2\int_{0}^{+\infty} \sin ^{2}(t) dt &= -\sin(t)\cos(t) |_{0}^{+\infty} + t |_{0}^{+\infty} \\
\int_{0}^{+\infty} \sin ^{2}(t) dt &= \frac{-\sin(t)\cos(t) |_{0}^{+\infty} + t |_{0}^{+\infty}}{2} \\
&= \frac{\lim_{ t \to +\infty } -\sin(t)\cos(t) + \cancel{ \sin(0)\cos(0) } + \lim_{ t \to +\infty } t - 0}{2} \\
&= \frac{\lim_{ t \to +\infty } -\sin(t)\cos(t) + \lim_{ t \to +\infty } t}{2}
\end{align}
$$

Si analizamos los límites:
$$
\lim_{ t \to +\infty } -\sin(t)\cos(t) \text{ no existe, la función oscila infinitamente entre -1 y 1}
$$
$$
\lim_{ t \to +\infty } t = +\infty
$$

En conclusión:
$$
\int_{0}^{+\infty} \sin ^{2}(t) dt = \frac{\lim_{ t \to +\infty } -\sin(t)\cos(t) + \lim_{ t \to +\infty } t}{2} = \frac{\lim_{ t \to +\infty } -\sin(t)\cos(t) + +\infty}{2} = +\infty
$$
La integral $\int_{0}^{+\infty} \sin ^{2}(t) dt$ es divergente.

### Parte f
$$
\int_{0}^{+\infty} \frac{x}{\sqrt{ x^{4} + 1 }} dx
$$

La función está bien definida en el dominio $[0, +\infty]$. Es así que $\int_{0}^{1} \frac{x}{\sqrt{ x^{4} + 1 }} dx$ es finito. Ahora, analicemos lo que sucede en el infinito:
$\frac{x}{\sqrt{ x^{4} + 1 }} \sim \frac{x}{\sqrt{ x^{4} }} = \frac{x}{x^{2}} = \frac{1}{x}$ cuando $x \to +\infty$.

De esta forma:
$$
\int_{1}^{+\infty} \frac{x}{\sqrt{ x^{4} + 1 }} dx \sim \int_{1}^{+\infty} \frac{1}{x} dx
$$

Entonces, sabiendo que $\int_{1}^{+\infty} \frac{1}{x} dx$ es divergente, aplicando criterio de equivalentes, concluimos que $\int_{1}^{+\infty} \frac{x}{\sqrt{ x^{4} + 1 }} dx$ también lo es.

En conclusión:
$$
\int_{0}^{+\infty} \frac{x}{\sqrt{ x^{4} + 1 }} dx = \int_{0}^{1} \frac{x}{\sqrt{ x^{4} + 1 }} dx + \int_{1}^{+\infty} \frac{x}{\sqrt{ x^{4} + 1 }} dx = L + +\infty = +\infty
$$
$\int_{0}^{+\infty} \frac{x}{\sqrt{ x^{4} + 1 }} dx$ es divergente.

### Parte g
$$
\int_{-\infty}^{+\infty} \frac{x}{\cosh(x)} dx
$$

### Parte h
$$
\int_{-1}^{1} \frac{1}{x^{2} - 1} dx
$$
Esta función no está definida en -1 y 1. Por lo tanto, conviene separarla en dos partes:
$$
\int_{-1}^{1} \frac{1}{x^{2} - 1} dx = \int_{-1}^{0} \frac{1}{x^{2} - 1} dx + \int_{0}^{1} \frac{1}{x^{2} - 1} dx
$$
Como la función es par, sabemos que:
$$
\int_{-1}^{0} \frac{1}{x^{2} - 1} dx + \int_{0}^{1} \frac{1}{x^{2} - 1} dx = 2 \cdot \int_{0}^{1} \frac{1}{x^{2} - 1} dx
$$
Podemos determinar que
$$
\lim_{ x \to 1^{+} } \frac{1}{x^{2} - 1} = \lim_{ x \to 0^{+} } \frac{1}{x^{2}} \implies \lim_{ x \to 1^{-} } \frac{1}{x^{2} - 1} = \lim_{ x \to 0^{+} } -\frac{1}{x^{2}} = -\lim_{ x \to 0^{+} } \frac{1}{x^{2}}
$$
De esta forma, es como si el comportamiento de la función $\frac{1}{x^{2}}$ estuviera trasladado. Por lo tanto, podemos considerar esto para determinar la convergencia:
Sabemos que $\int_{0}^{1} \frac{1}{x^{2}} dx$ es divergente, ya que $\int_{0}^{1} \frac{1}{x^{\alpha}} dx = \infty, \forall \alpha \geq 1$.

Entonces, como los límites anteriores coinciden, determinamos que $\int_{0}^{1} \frac{1}{x^{2} - 1} dx \sim \int_{0}^{1} \frac{1}{x^{2}} dx$.

En conclusión, como $\int_{0}^{1} \frac{1}{x^{2}} dx$ es divergente, aplicando criterio de equivalentes, determinamos que $\int_{0}^{1} \frac{1}{x^{2} - 1} dx$ también es divergente.

De esta manera, $\int_{-1}^{1} \frac{1}{x^{2} - 1} dx = 2 \cdot \int_{0}^{1} \frac{1}{x^{2} - 1} dx$ es divergente.

### Parte i
$$
\int_{0}^{+\infty} \frac{\cos(x)}{\sqrt{ x }} dx
$$
Aplicamos partes:
$$
\left[
\begin{align}
&f(x) = \frac{1}{\sqrt{ x }} &f'(x) = -\frac{1}{2x^{\frac{3}{2}}} \\
&g'(x) = \cos(x) &g(x) = \sin(x)
\end{align}
\right]
$$
$$
\begin{align}
\int_{0}^{+\infty} \frac{\cos(x)}{\sqrt{ x }} dx &= \left. \frac{\sin(x)}{\sqrt{ x }} \right|_{0}^{+\infty} + \int_{0}^{+\infty} \frac{\sin(x)}{2x^{\frac{3}{2}}} dx \\
&= \lim_{ x \to +\infty }  \frac{\sin(x)}{\sqrt{ x }} - \lim_{ x \to 0 }  \frac{\sin(x)}{\sqrt{ x }} + \frac{1}{2} \cdot \int_{0}^{+\infty} \frac{\sin(x)}{x^{\frac{3}{2}}} dx
\end{align}
$$
Analizamos los límites:
$$
\lim_{ x \to +\infty }  \frac{\sin(x)}{\sqrt{ x }} = 0
$$
$$
\lim_{ x \to 0 }  \frac{\sin(x)}{\sqrt{ x }} = \frac{0}{0}
$$
Aplicamos L'Hôpital:
$$
(\sin(x))' = \cos(x)
$$
$$
(\sqrt{ x })' = \frac{1}{2\sqrt{ x }}
$$
$$
\implies \lim_{ x \to 0 }  \frac{\sin(x)}{\sqrt{ x }} = \lim_{ x \to 0 } \frac{\cos(x)}{\frac{1}{2\sqrt{ x }}} = \lim_{ x \to 0 } \cos(x) \cdot 2\sqrt{ x } = \cos(0) \cdot 2\sqrt{ 0 } = 1 \cdot 2 \cdot 0 = 0
$$

Analizamos la integral:
$$
\int_{0}^{+\infty} \frac{\sin(x)}{x^{\frac{3}{2}}} dx = \int_{0}^{1} \frac{\sin(x)}{x^{\frac{3}{2}}} dx + \int_{1}^{+\infty} \frac{\sin(x)}{x^{\frac{3}{2}}} dx
$$

Estudiamos el límite en 0:
$$
\lim_{ x \to 0 } \frac{\sin(x)}{x^{\frac{3}{2}}} = \frac{0}{0}
$$
Aplicamos L'Hôpital:
$$
(\sin(x))' = \cos(x)
$$
$$
\left( x^{\frac{3}{2}} \right)' = \frac{3\sqrt{ x }}{2}
$$
$$
\implies \lim_{ x \to 0 } \frac{\sin(x)}{x^{\frac{3}{2}}} = \lim_{ x \to 0 } \frac{2\cos(x)}{3\sqrt{ x }} = \frac{2 \cos(0)}{3\sqrt{ 0 }} = \frac{2 \cdot 1}{3 \cdot 0} = \frac{2}{0} = +\infty
$$

De esta manera, verificamos que tenemos una integral de segunda especie en $x = 0$.

Sin embargo, sabemos que $\sin(x) \sim x$ cuando $x \to 0$. Por lo tanto:
$$
\frac{\sin(x)}{x^{\frac{3}{2}}} \sim \frac{x}{x^{\frac{3}{2}}} = \frac{1}{\sqrt{ x }}
$$
cuando $x \to 0$, por lo que son de la misma clase. Entonces, sabiendo que $\int_{0}^{1} \frac{1}{\sqrt{ x }} dx < \infty$, y aplicando el criterio de equivalentes, concluimos que $\int_{0}^{1} \frac{\sin(x)}{x^{\frac{3}{2}}} dx$ es convergente.

Ahora, analizamos la convergencia absoluta:
$$
\left| \frac{\sin(x)}{x^{\frac{3}{2}}} \right| = \frac{|\sin(x)|}{x^{\frac{3}{2}}} \leq \frac{1}{x^{\frac{3}{2}}}
$$
Sabemos que $\int_{1}^{+\infty} \frac{1}{x^{\frac{3}{2}}} dx$ es convergente, entonces, aplicando el criterio de comparación, determinamos que $\int_{1}^{+\infty} \frac{|\sin(x)|}{x^{\frac{3}{2}}} dx$ también lo es.

De esta forma, $\int_{1}^{+\infty} \frac{\sin(x)}{x^{\frac{3}{2}}} dx$ es absolutamente convergente, y por lo tanto es convergente.

Entonces, sustituimos en la igualdad:
$$
\begin{align}
\int_{0}^{+\infty} \frac{\cos(x)}{\sqrt{ x }} dx &= \lim_{ x \to +\infty } \frac{\sin(x)}{\sqrt{ x }} - \lim_{ x \to 0 }  \frac{\sin(x)}{\sqrt{ x }} + \frac{1}{2} \cdot \int_{0}^{+\infty} \frac{\sin(x)}{x^{\frac{3}{2}}} dx \\
&= 0 - 0 + \frac{1}{2} \cdot \left( \int_{0}^{1} \frac{\sin(x)}{x^{\frac{3}{2}}} dx + \int_{1}^{+\infty} \frac{\sin(x)}{x^{\frac{3}{2}}} dx \right) \\
&= \frac{1}{2} \cdot \left( L_{1} + L_{2} \right) \\
&= \frac{L_{1} + L_{2}}{2}
\end{align}
$$

En conclusión, $\int_{0}^{+\infty} \frac{\cos(x)}{\sqrt{ x }} dx$ es convergente.

### Parte j
$$
\int_{0}^{+\infty} \frac{e^{-\sqrt{ x }}}{\sqrt{ x }} dx = \int_{0}^{+\infty} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx
$$
$e^{-\sqrt{ x }} > 0, \forall x \in \mathbb{R}$, sin embargo, $\sqrt{ x } = 0$ si $x = 0$. Entonces, tenemos que ser precavidos:
$$
\int_{0}^{+\infty} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx = \int_{0}^{1} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx + \int_{1}^{+\infty} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx
$$

Consideremos lo siguiente: $e^{\sqrt{ x }} \to 1$ cuando $x \to 0$, por lo tanto, $\frac{1}{\sqrt{ x }e^{\sqrt{ x }}} \to \frac{1}{\sqrt{ x }}$ cuando $x \to 0$.

De esta manera, sabemos que $\int_{0}^{1} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx$ y $\int_{0}^{1} \frac{1}{\sqrt{ x }} dx$ son de la misma clase (por el criterio de equivalentes), entonces, sabiendo que $\int_{0}^{1} \frac{1}{\sqrt{ x }} dx$ es convergente, podemos deducir que $\int_{0}^{1} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx$ también lo es.

Nos queda analizar la segunda integral: $e^{\sqrt{ x }}$ es mayor que cualquier polinomio a partir de un valor $x_{0} \in \mathbb{R}$. Por lo tanto, $\exists x_{0}$ tal que $\sqrt{ x }e^{\sqrt{ x }} > x^{2}, \forall x > x_{0} \implies \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} < \frac{1}{x^{2}}, \forall x > x_{0}$

De esta manera, considerando que $\int_{1}^{+\infty} \frac{1}{x^{2}} dx$ es convergente, aplicamos el criterio de comparación y deducimos que $\int_{1}^{+\infty} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx$ también lo es.

En conclusión, $\int_{0}^{+\infty} \frac{e^{-\sqrt{ x }}}{\sqrt{ x }} dx$ es convergente, puesto que $\int_{0}^{+\infty} \frac{e^{-\sqrt{ x }}}{\sqrt{ x }} dx = \int_{0}^{+\infty} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx = \int_{0}^{1} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx + \int_{1}^{+\infty} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} dx$, con $\int_{0}^{1} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} < \infty$ y $\int_{1}^{+\infty} \frac{1}{\sqrt{ x }e^{\sqrt{ x }}} < \infty$

### Parte k
$$
\int_{0}^{+\infty} e^{x^{2} - \frac{1}{x^{2}}} dx
$$
La función tiene un problema cuando $x \to 0$:
$$
\int_{0}^{+\infty} e^{x^{2} - \frac{1}{x^{2}}} dx = \int_{0}^{1} e^{x^{2} - \frac{1}{x^{2}}} dx + \int_{1}^{+\infty} e^{x^{2} - \frac{1}{x^{2}}} dx
$$
En la primer integral: cuando $x \to 0$, $e^{x^{2} - \frac{1}{x^{2}}} \sim e^{-\frac{1}{x^{2}}}$, ya que $x^{2} \to 0$.
Si estudiamos el límite:
$$
\lim_{ x \to 0 } e^{x^{2} - \frac{1}{x^{2}}} = \lim_{ x \to 0 } e^{-\frac{1}{x^{2}}} = \lim_{ x \to 0 } \frac{1}{e^{\frac{1}{x^{2}}}} = \frac{1}{e^{+\infty}} = 0
$$

Entonces, podemos determinar que $\int_{0}^{1} e^{x^{2} - \frac{1}{x^{2}}} dx < \infty$.

Estudiemos la segunda integral: cuando $x \to +\infty$, $e^{x^{2} - \frac{1}{x^{2}}} \sim e^{x^{2}}$, ya que $\frac{1}{x^{2}} \to 0$.
Estudiamos el límite:
$$
\lim_{ x \to +\infty } e^{x^{2} - \frac{1}{x^{2}}} = \lim_{ x \to +\infty } e^{x^{2}} = e^{+\infty} = +\infty
$$
De esta forma, $\int_{1}^{+\infty} e^{x^{2} - \frac{1}{x^{2}}} dx = \infty$.

En conclusión, la integral $\int_{0}^{+\infty} e^{x^{2} - \frac{1}{x^{2}}} dx$ es divergente, ya que $\int_{0}^{+\infty} e^{x^{2} - \frac{1}{x^{2}}} dx = L + +\infty = +\infty$.

### Parte l
$$
\int_{-1}^{1} \frac{e^{\frac{-1}{x - 1}}}{(x - 1)^{2}} dx
$$
El problema ocurre cuando $x \to 1$, ya que $(x - 1)^{2} \to 0$ y $x - 1 \to 0$:
Analizamos numerador y denominador por separado:
$$
\lim_{ x \to 1^{-} } e^{\frac{-1}{x - 1}} = e^{\frac{-1}{0^{-}}} = e^{+\infty} = +\infty
$$
$$
\lim_{ x \to 1^{-} } (x - 1)^{2} = (1 - 1)^{2} = 0^{+}
$$

Entonces:
$$
\lim_{ x \to 1^{-} } \frac{e^{\frac{-1}{x - 1}}}{(x - 1)^{2}} = \frac{+\infty}{0^{+}} = +\infty
$$

CORRECCIÓN:
Intentemos encontrar una primitiva inmediata aplicando sustitución:
$$
u = \frac{-1}{x - 1} \implies du = \frac{1}{(x - 1)^{2}} dx
$$
Entonces:
$$
\begin{align}
&x = -1^{+} \implies u = \frac{-1}{-1 - 1} = \frac{-1}{-2} = \frac{1}{2} \\
&x = 1^{-} \implies u = \frac{-1}{1^{-} - 1} = \frac{-1}{0^{-}} = +\infty
\end{align}
$$
De esta forma:
$$
\int_{-1}^{1} \frac{e^{\frac{-1}{x - 1}}}{(x - 1)^{2}} dx = \int_{\frac{1}{2}}^{+\infty} e^{u} du = e^{u} |_{\frac{1}{2}}^{+\infty} = e^{\frac{-1}{x - 1}} |_{-1}^{1} = \lim_{ x \to 1^{-} } e^{\frac{-1}{x - 1}} - \lim_{ x \to -1^{+} } e^{\frac{-1}{x - 1}}
$$

Estudiamos los límites:
$$
\lim_{ x \to 1^{-} } e^{\frac{-1}{x - 1}} = e^{\frac{-1}{1^{-} - 1}} = e^{\frac{-1}{0^{-}}} = e^{+\infty} = +\infty
$$
$$
\lim_{ x \to -1^{+} } e^{\frac{-1}{x - 1}} = e^{\frac{-1}{-1^{-} - 1}} = e^{\frac{-1}{-2^{-}}} = e^{\frac{1}{2}}
$$

Sustituimos:
$$
\int_{-1}^{1} \frac{e^{\frac{-1}{x - 1}}}{(x - 1)^{2}} dx = \lim_{ x \to 1^{-} } e^{\frac{-1}{x - 1}} - \lim_{ x \to -1^{+} } e^{\frac{-1}{x - 1}} = +\infty - e^{\frac{1}{2}} = +\infty
$$

En conclusión, la integral $\int_{-1}^{1} \frac{e^{\frac{-1}{x - 1}}}{(x - 1)^{2}} dx$ es divergente.

### Parte m
$$
\int_{0}^{\frac{\pi}{2}} \frac{1}{\sin ^{\alpha}(x) \cos ^{\beta}(x)} dx \qquad (\alpha, \beta \in \mathbb{R})
$$

---
## Ejercicio 7
### Parte a
$$
\int_{0}^{+\infty} \frac{x^{\alpha}}{x + 1} dx = \int_{0}^{+\infty} \frac{x^{\alpha - 1}}{1 + \frac{1}{x}} dx
$$
La integral presentada es una impropia de primera especie (ya que la función es continua en el intervalo presentado).

Cuando $x \to +\infty$, se cumple que $\frac{x^{\alpha - 1}}{1 + \frac{1}{x}} \sim x^{\alpha - 1} = \frac{1}{x^{1 - \alpha}}$. Por lo tanto, $\frac{x^{\alpha - 1}}{1 + \frac{1}{x}}$ y $\frac{1}{x^{1 - \alpha}}$ son de la misma clase.

Entonces, tenemos que determinar para que valores de $\alpha$ $\int_{0}^{+\infty} \frac{1}{x^{1 - \alpha}} dx$ es convergente. Sin embargo, nos encontramos ante un problema, ya que sabemos que este tipo de integrales solo convergen si consideramos el dominio $\int_{0}^{1}$, o $\int_{1}^{+\infty}$ (o cualquier otro real $> 0$ en lugar de 1), ya que:
$$
\int_{0}^{1} \frac{1}{x^{1 - \alpha}} dx < \infty \Longleftrightarrow \alpha > 0
$$
$$
\int_{1}^{+\infty} \frac{1}{x^{1 - \alpha}} dx < \infty \Longleftrightarrow \alpha < 0
$$

De esta forma, $\alpha$ tendría que cumplir ambas condiciones a la vez, lo que es imposible.

En conclusión, la integral propuesta no es convergente sin importar el valor de $\alpha$.

CORRECCIÓN:
El desarrollo es incorrecto, ya que deducimos correctamente que "cuando $x \to +\infty$, se cumple que $\frac{x^{\alpha - 1}}{1 + \frac{1}{x}} \sim x^{\alpha - 1}$. Por lo tanto, $\frac{x^{\alpha - 1}}{1 + \frac{1}{x}}$ y $x^{\alpha - 1}$ son de la misma clase". Sin embargo, esto es válido para el intervalo $[1, +\infty]$, pero no para $[0, 1]$. Entonces, para este segundo intervalo, tenemos que buscar otra equivalencia:

Cuando $x \to 0$, se cumple que $\frac{x^{\alpha}}{x + 1} \sim x^{\alpha} = \frac{1}{x^{-\alpha}}$. Entonces, estudiamos su comportamiento en $[0, 1]$:
$$
\int_{0}^{1} \frac{1}{x^{-\alpha}} dx < \infty \Longleftrightarrow \alpha > -1
$$

Entonces, considerando que $\int_{1}^{+\infty} \frac{1}{x^{1 - \alpha}} dx < \infty \Longleftrightarrow \alpha < 0$, por el criterio de equivalentes (por partes considerando $\frac{x^{\alpha}}{x + 1} \sim \frac{1}{x^{-\alpha}}$ en $[0, 1]$ y $\frac{x^{\alpha - 1}}{1 + \frac{1}{x}} \sim \frac{1}{x^{1 - \alpha}}$ en $[1, +\infty]$) concluimos que $\int_{0}^{+\infty} \frac{x^{\alpha}}{x + 1} dx$ es convergente $\forall \alpha \in (-1, 0)$.

### Parte b
$$
\int_{0}^{+\infty} \frac{1}{(e^{x^{2}} - 1)^{\alpha}} dx
$$
Esta función no está definida en 0, por lo que tenemos que dividirla en dos partes:
$$
\int_{0}^{+\infty} \frac{1}{(e^{x^{2}} - 1)^{\alpha}} dx = \int_{0}^{1} \frac{1}{(e^{x^{2}} - 1)^{\alpha}} dx + \int_{1}^{+\infty} \frac{1}{(e^{x^{2}} - 1)^{\alpha}} dx
$$

Nuevamente, tenemos que hacer una separación similar:

- Cuando $x \to +\infty$, se cumple que $\frac{1}{(e^{x^{2}} - 1)^{\alpha}} \sim \frac{1}{e^{\alpha x^{2}}}$. Por lo tanto, $\frac{1}{(e^{x^{2}} - 1)^{\alpha}}$ y $\frac{1}{e^{\alpha x^{2}}}$ son de la misma clase en el intervalo $[1, +\infty]$.
- Cuando $x \to 0$, se cumple que $\frac{1}{(e^{x^{2}} - 1)^{\alpha}} \sim \frac{1}{x^{2\alpha}}$ por el desarrollo de Taylor de $(e^{x^{2}} - 1)^{\alpha}$ en 0:
$$
\begin{align}
e^{x^{2}} - 1 &= (e^{0^{2}} - 1) + (e^{0^{2}} - 1)'x + \frac{(e^{0^{2}} - 1)''}{2}x^{2} + r(x) \\
&= \cancel{ (1 - 1) } + \cancel{ (2 \cdot 0 \cdot e^{0^{2}})x } + \frac{2 \cdot e^{0^{2}} + \cancel{ 2 \cdot 0 \cdot (2 \cdot 0 \cdot e^{0^{2}}) }}{2}x^{2} + r(x) \\
&= \frac{2 \cdot 1}{2}x^{2} + r(x) \\
&= x^{2} + r(x) \implies (e^{x^{2}} - 1)^{\alpha} = (x^{2} + r(x))^{\alpha} \sim x^{2\alpha}
\end{align}
$$

Por lo tanto, $\frac{1}{(e^{x^{2}} - 1)^{\alpha}}$ y $\frac{1}{x^{2\alpha}}$ son de la misma clase en el intervalo $[0, 1]$.

Entonces, analizamos la integral de cada equivalente:
$$
\int_{1}^{+\infty} \frac{1}{e^{\alpha x^{2}}} dx < \infty \Longleftrightarrow \alpha > 0
$$
$$
\int_{0}^{1} \frac{1}{x^{2\alpha}} dx < \infty \Longleftrightarrow \alpha < \frac{1}{2}
$$

En conclusión, considerando los valores válidos de $\alpha$ que aseguran la convergencia de las integrales presentadas, y aplicando el criterio de equivalentes, podemos asegurar que $\int_{0}^{+\infty} \frac{1}{(e^{x^{2}} - 1)^{\alpha}} dx$ es convergente $\forall \alpha \in (0, \frac{1}{2})$.

---
## Ejercicio 8
### Parte a
$$
\sum_{n = 1}^{\infty} n \cdot e^{-n^{2}}
$$
En este caso, analizaremos la integral:
$$
\int_{1}^{+\infty} x \cdot e^{-x^{2}} dx
$$
La función $x \cdot e^{-x^{2}}$ es positiva y monótona decreciente $\forall x \in [1, +\infty]$, por lo que podemos aplicar el criterio Serie-Integral: $\int_{1}^{+\infty} x \cdot e^{-x^{2}} dx$ y $\sum_{n = 1}^{\infty} n \cdot e^{-n^{2}}$ son de la misma clase.

Estudiamos la integral:
$$
\begin{align}
\int_{1}^{+\infty} x \cdot e^{-x^{2}} dx &= -\frac{1}{2} \cdot \int_{1}^{+\infty} -2x \cdot e^{-x^{2}} dx \\
&= -\frac{1}{2} \cdot \left( e^{-x^{2}} |_{1}^{+\infty} \right) \\
&= -\frac{1}{2} \cdot \left( \lim_{ x \to +\infty } e^{-x^{2}} - e^{-1^{2}} \right) \\
&= -\frac{1}{2} \cdot \left( 0 - \frac{1}{e} \right) \\
&= \frac{1}{2e}
\end{align}
$$

En conclusión, $\int_{1}^{+\infty} x \cdot e^{-x^{2}} dx$ es convergente y converge a $\frac{1}{2e}$. De esta manera, aplicamos el criterio Serie-Integral, y determinamos que la serie $\sum_{n = 1}^{\infty} n \cdot e^{-n^{2}}$ también es convergente.

### Parte b
$$
\sum_{n = 2}^{\infty} \frac{1}{n \sqrt{ \log(n) }}
$$
Analizamos la integral correspondiente:
$$
\int_{2}^{+\infty} \frac{1}{x \sqrt{ \log(x) }} dx
$$
La función $\frac{1}{x \sqrt{ \log(x) }}$ es positiva y monótona decreciente $\forall x \in [2, +\infty]$, por lo que podemos aplicar el criterio Serie-Integral: $\frac{1}{x \sqrt{ \log(x) }}$ y $\sum_{n = 2}^{\infty} \frac{1}{n \sqrt{ \log(n) }}$ son de la misma clase.

Aplicamos sustitución:
$$
u = \log(x) \implies du = \frac{1}{x} dx
$$
$$
\begin{align}
\int \frac{1}{x \sqrt{ \log(x) }} dx &= \int \frac{1}{\sqrt{ \log(x) }} \cdot \frac{1}{x} dx \\
&= \int \frac{1}{\sqrt{ u }} du \\
&= 2 \cdot \int \frac{1}{2\sqrt{ u }} du \\
&= 2 \cdot \sqrt{ u } \\
&= 2 \cdot \sqrt{ \log(x) }
\end{align}
$$
De esta manera:
$$
\begin{align}
\int_{2}^{+\infty} \frac{1}{x \sqrt{ \log(x) }} dx &= 2 \cdot \left( \sqrt{ \log(x) } |_{2}^{+\infty} \right) \\
&= 2 \cdot \left( \lim_{ x \to +\infty } \sqrt{ \log(x) } - \sqrt{ \log(2) } \right) \\
&= 2 \cdot \left( +\infty - \sqrt{ \log(2) } \right) \\
&= +\infty
\end{align}
$$
En conclusión, determinamos que la integral $\int_{2}^{+\infty} \frac{1}{x \sqrt{ \log(x) }} dx$ es divergente. Por lo tanto, si aplicamos el criterio Serie-Integral con la serie correspondiente, deducimos que $\sum_{n = 2}^{\infty} \frac{1}{n \sqrt{ \log(n) }}$ es divergente.

### Parte c
$$
\sum_{n = 1}^{\infty} \frac{\log(n)}{n^{2}}
$$
Analizamos la integral correspondiente:
$$
\int_{1}^{+\infty} \frac{\log(x)}{x^{2}} dx
$$
La función $\frac{\log(x)}{x^{2}}$ es positiva y monótona decreciente $\forall x \in [1, +\infty]$, por lo que podemos aplicar el criterio Serie-Integral: $\frac{\log(x)}{x^{2}}$ y $\sum_{n = 1}^{\infty} \frac{\log(n)}{n^{2}}$ son de la misma clase.

Aplicamos partes:
$$
\left[
\begin{align}
&f(x) = \log(x) &f'(x) = \frac{1}{x} \\
&g'(x) = \frac{1}{x^{2}} &g(x) = -\frac{1}{x}
\end{align}
\right]
$$
$$
\begin{align}
\int_{1}^{+\infty} \frac{\log(x)}{x^{2}} dx &= \left. -\frac{\log(x)}{x} \right|_{1}^{+\infty} + \int_{1}^{+\infty} \frac{1}{x^{2}} dx \\
&= - \lim_{ x \to +\infty } \frac{\log(x)}{x} + \cancel{ \log(1) } + \int_{1}^{+\infty} \frac{1}{x^{2}} dx \\
&= 0 + \int_{1}^{+\infty} \frac{1}{x^{2}} dx
\end{align}
$$
Como vemos, determinamos que $\int_{1}^{+\infty} \frac{\log(x)}{x^{2}} dx = \int_{1}^{+\infty} \frac{1}{x^{2}} dx$, entonces, como sabemos que $\int_{1}^{+\infty} \frac{1}{x^{2}} dx$ es convergente, concluimos que $\int_{1}^{+\infty} \frac{\log(x)}{x^{2}} dx$ también lo es (y convergen al mismo valor).

Ahora, aplicando el criterio Serie-Integral, deducimos que $\sum_{n = 1}^{\infty} \frac{\log(n)}{n^{2}}$ es de la misma especie que la integral correspondiente. Por lo tanto, $\sum_{n = 1}^{\infty} \frac{\log(n)}{n^{2}}$ es convergente.

---
## Ejercicio 9
Comenzamos con la integral
$$
\int_{2}^{+\infty} \frac{1}{x \log(x)} dx
$$
Nuevamente, nos encontramos frente a una integral positiva y monótona decreciente (al menos a partir de un $x_{0}$ determinado, en el infinito). Por esta razón, basta con determinar si la integral es convergente o divergente, para calificar a la serie (siendo que son de la misma clase).

Estudiamos la integral:
$$
u = \log(x) \implies du = \frac{1}{x} dx
$$
$$
\begin{align}
\int \frac{1}{x \log(x)} dx &= \int \frac{1}{\log(x)} \cdot \frac{1}{x} dx \\
&= \int \frac{1}{u} du \\
&= \log(u) \\
&= \log(\log(x))
\end{align}
$$
De esta manera:
$$
\begin{align}
\int_{2}^{+\infty} \frac{1}{x \log(x)} dx &= \log(\log(x)) |_{2}^{+\infty} \\
&= \lim_{ x \to +\infty } \log(\log(x)) - \log(\log(2)) \\
&= +\infty - \log(\log(2)) \\
&= +\infty
\end{align}
$$

En conclusión, la integral $\int_{2}^{+\infty} \frac{1}{x \log(x)} dx$ es divergente.

Continuamos con la serie
$$
\sum_{2}^{\infty} \frac{1}{n \log(n)}
$$
Aplicando el criterio Serie-Integral, deducimos que la serie $\sum_{2}^{\infty} \frac{1}{n \log(n)}$ y su integral correspondiente son de la misma clase. Entonces, como $\int_{2}^{+\infty} \frac{1}{x \log(x)} dx$ es divergente, determinamos que $\sum_{2}^{\infty} \frac{1}{n \log(n)}$ también es divergente.

---
## Ejercicio 10
$$
\int_{0}^{+\infty} \log\left( 1 + \frac{a^{2}}{x^{2}} \right) dx
$$
Desarrollamos partes considerando la sugerencia:
$$
\left[
\begin{align}
&f(x) = \log\left( 1 + \frac{a^{2}}{x^{2}} \right) &f'(x) = -\frac{2a^{2}}{x^{3} + a^{2}x} \\
&g'(x) = 1 &g(x) = x
\end{align}
\right]
$$
$$
\begin{align}
\int_{0}^{+\infty} \log\left( 1 + \frac{a^{2}}{x^{2}} \right) dx &= \left. x \log\left( 1 + \frac{a^{2}}{x^{2}} \right) \right|_{0}^{+\infty} + \int_{0}^{+\infty} \frac{2a^{2}}{x^{2} + a^{2}} dx \\
&= \lim_{ x \to +\infty } x \log\left( 1 + \frac{a^{2}}{x^{2}} \right) - \lim_{ x \to 0 } x \log\left( 1 + \frac{a^{2}}{x^{2}} \right) + 2a^{2} \cdot \int_{0}^{+\infty} \frac{1}{x^{2} + a^{2}} dx
\end{align}
$$

Calculamos los límites presentados:
$$
x \log\left( 1 + \frac{a^{2}}{x^{2}} \right) = \log\left( \left( 1 + \frac{a^{2}}{x^{2}} \right)^{x} \right)
$$
$$
\lim_{ x \to +\infty } \log\left( \left( 1 + \frac{a^{2}}{x^{2}} \right)^{x} \right) = \log\left( \left( 1 + 0 \right)^{+\infty} \right) = \log(1) = 0
$$
$$
\lim_{ x \to 0 } x \log\left( 1 + \frac{a^{2}}{x^{2}} \right) = \lim_{ x \to 0 } \frac{\log\left( 1 + \frac{a^{2}}{x^{2}} \right)}{\frac{1}{x}}
$$
Aplicamos L'Hôpital:
$$
\left( \log\left( 1 + \frac{a^{2}}{x^{2}} \right) \right)' = -\frac{2a^{2}}{x^{3} + a^{2}x}
$$
$$
\left( \frac{1}{x} \right)' = -\frac{1}{x^{2}}
$$
$$
\implies \lim_{ x \to 0 } \frac{\log\left( 1 + \frac{a^{2}}{x^{2}} \right)}{\frac{1}{x}} = \lim_{ x \to 0 } \frac{\frac{2a^{2}}{x^{3} + a^{2}x}}{\frac{1}{x^{2}}} = \lim_{ x \to 0 } \frac{2a^{2}x}{x^{2} + a^{2}} = \frac{2a^{2} \cdot 0}{0^{2} + a^{2}} = \frac{0}{a^{2}} = 0
$$

Estudiamos la integral $\int_{0}^{+\infty} \frac{1}{x^{2} + a^{2}} dx$:
$$
\int_{0}^{+\infty} \frac{1}{x^{2} + a^{2}} dx = \int_{0}^{1} \frac{1}{x^{2} + a^{2}} dx + \int_{1}^{+\infty} \frac{1}{x^{2} + a^{2}} dx
$$

- Cuando $x \to +\infty$, $\frac{1}{x^{2} + a^{2}} \sim \frac{1}{x^{2}}$, por lo que $\int_{1}^{+\infty} \frac{1}{x^{2} + a^{2}} dx$ y $\int_{1}^{+\infty} \frac{1}{x^{2}} dx$ son de la misma clase. Sabemos que $\int_{1}^{+\infty} \frac{1}{x^{2}} dx$ es convergente, por lo que aplicando criterio de equivalentes, determinamos que $\int_{1}^{+\infty} \frac{1}{x^{2} + a^{2}} dx$ también lo es.
- Cuando $x \to 0$, $\frac{1}{x^{2} + a^{2}} \sim \frac{1}{a^{2}}$, que es una constante. De esta manera, la integral $\int_{0}^{1} \frac{1}{x^{2} + a^{2}} dx$ es convergente (pues el intervalo es acotado, y la función está bien definida en el mismo, ya que ambos términos del denominador son positivos).

De esta manera, determinamos que $\int_{0}^{+\infty} \frac{1}{x^{2} + a^{2}} dx$ es convergente, pues la expresamos como dos integrales para las cuales logramos demostrar su convergencia.

Entonces, si sustituimos en la integral inicial:
$$
\begin{align}
\int_{0}^{+\infty} \log\left( 1 + \frac{a^{2}}{x^{2}} \right) dx &= \lim_{ x \to +\infty } x \log\left( 1 + \frac{a^{2}}{x^{2}} \right) - \lim_{ x \to 0 } x \log\left( 1 + \frac{a^{2}}{x^{2}} \right) + 2a^{2} \cdot \int_{0}^{+\infty} \frac{1}{x^{2} + a^{2}} dx \\
&= 0 - 0 + 2a^{2} \cdot L \\
&= 2a^{2} \cdot L \\
&< \infty
\end{align}
$$

En conclusión, probamos que la integral $\int_{0}^{+\infty} \log\left( 1 + \frac{a^{2}}{x^{2}} \right) dx$ es convergente.