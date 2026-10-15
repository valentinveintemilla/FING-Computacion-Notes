# Ejercicio 1
La integral impropia
$$
\int_{0}^{+\infty} \frac{1}{\log(x)^{\alpha}x} dx
$$
Realizamos el siguiente cambio de variable para facilitar el estudio de la integral:
$$
u = \log(x) \implies du = \frac{1}{x} dx
$$
$$
\int \frac{1}{\log(x)^{\alpha}x} dx = \int \frac{1}{\log(x)^{\alpha}} \cdot \frac{1}{x} dx \underbrace{ = }_{ C.V. } \int \frac{1}{u^{\alpha}} du
$$
Además, tenemos que dividir a la integral en cuatro partes, ya que presenta tres puntos problemáticos: 0 (donde $\log(x)$ no está definido y $x = 0$), 1 ($\log(1) = 0$), $+\infty$:
$$
\int_{0}^{+\infty} \frac{1}{\log(x)^{\alpha}x} dx = \int_{0}^{\frac{1}{2}} \frac{1}{\log(x)^{\alpha}x} dx + \int_{\frac{1}{2}}^{1} \frac{1}{\log(x)^{\alpha}x} dx + \int_{1}^{2} \frac{1}{\log(x)^{\alpha}x} dx + \int_{2}^{+\infty} \frac{1}{\log(x)^{\alpha}x} dx
$$

Procedemos a retocar los extremos de integración, considerando el cambio de variable:
$$
\begin{align}
&x = 0 \implies u = -\infty \\
&x = \frac{1}{2} \implies u = \log\left( \frac{1}{2} \right) \\
&x = 1 \implies u = 0 \\
&x = 2 \implies u = \log(2) \\
&x = +\infty \implies u = +\infty
\end{align}
$$
Entonces, tenemos que:
$$
\int_{-\infty}^{+\infty} \frac{1}{u^{\alpha}} du = \int_{-\infty}^{\log\left( \frac{1}{2} \right)} \frac{1}{u^{\alpha}} du + \int_{\log\left( \frac{1}{2} \right)}^{0} \frac{1}{u^{\alpha}} du + \int_{0}^{\log(2)} \frac{1}{u^{\alpha}} du + \int_{\log(2)}^{+\infty} \frac{1}{u^{\alpha}} du
$$

Entonces, tenemos que encontrar los valores de $\alpha$ que aseguran la convergencia en cada tramo, sabiendo que:
$$
\begin{align}
&\int_{0}^{1} \frac{1}{x^{\alpha}} dx < \infty \Longleftrightarrow \alpha < 1 \\
&\int_{1}^{+\infty} \frac{1}{x^{\alpha}} dx < \infty \Longleftrightarrow \alpha > 1
\end{align}
$$
Entonces:
$$
\begin{align}
&\int_{-\infty}^{\log\left( \frac{1}{2} \right)} \frac{1}{u^{\alpha}} du < \infty \Longleftrightarrow \alpha > 1 \\
&\int_{\log\left( \frac{1}{2} \right)}^{0} \frac{1}{u^{\alpha}} du < \infty \Longleftrightarrow \alpha < 1 \\
&\int_{0}^{\log(2)} \frac{1}{u^{\alpha}} du < \infty \Longleftrightarrow \alpha < 1 \\
&\int_{\log(2)}^{+\infty} \frac{1}{u^{\alpha}} du < \infty \Longleftrightarrow \alpha > 1
\end{align}
$$

Por lo tanto, determinamos que la integral es convergente si se cumple que $\alpha < 1$ y $\alpha > 1$, lo que es imposible.

En conclusión, la integral diverge para todo $\alpha$ en los reales.

---
# Ejercicio 2
¿A cuanto converge la integral impropia $\int_{0}^{+\infty} e^{-x} dx$?
Buscamos una primitiva:
$$
\int_{0}^{+\infty} e^{-x} dx = -\int_{0}^{+\infty} -e^{-x} dx = - (e^{-x} |_{0}^{+\infty})
$$
$$
\begin{align}
- (e^{-x} |_{0}^{+\infty}) &= - (\lim_{ x \to +\infty } e^{-x} - e^{0}) \\
&= - (0 - 1) \\
&= 1
\end{align}
$$

En conclusión:
$$
\int_{0}^{+\infty} e^{-x} dx = 1
$$

---
# Ejercicio 3
¿Cómo se comporta la integral impropia $\int_{0}^{1} \frac{e^{-\sqrt{ x }}}{\sqrt{ x }} dx$?

Podemos encontrar una primitiva de la integral anterior:
$$
u = \sqrt{ x } \implies du = \frac{1}{2\sqrt{ x }} dx
$$
$$
\int \frac{e^{-\sqrt{ x }}}{\sqrt{ x }} dx = -2 \cdot \int -\frac{e^{-\sqrt{ x }}}{2\sqrt{ x }} dx = -2 \cdot \int -e^{-u} dx = -2 \cdot (e^{-u}) = -2 \cdot (e^{-\sqrt{ x }})
$$
Entonces:
$$
\begin{align}
\int_{0}^{1} \frac{e^{-\sqrt{ x }}}{\sqrt{ x }} dx &= -2 \cdot (e^{-\sqrt{ x }} |_{0}^{1}) \\
&= -2 \cdot (e^{-\sqrt{ 1 }} - e^{-\sqrt{ 0 }}) \\
&= -2 \cdot (e^{-1} - e^{0}) \\
&= -2 \cdot \left( \frac{1}{e} - 1 \right) \\
&= -2 \cdot \frac{1 - e}{e} \\
&= \frac{2e - 2}{e}
\end{align}
$$

Como vemos, la integral converge. Ahora, también lo hace absolutamente, ya que todos los términos son positivos.

---
# Ejercicio 4
Sea $f : [1, \infty] \to \mathbb{R}$ una función continua. Considere las siguientes afirmaciones:

1. Si $\int_{1}^{+\infty} |f(x)| dx$ converge $\implies \lim_{ x \to \infty } f(x) = 0$
2. Si $\int_{1}^{+\infty} f(x) dx$ converge, $f$ es decreciente y no negativa $\implies \lim_{ x \to \infty } f(x) = 0$.
3. Si $\int_{1}^{+\infty} f(x) dx$ diverge, $f$ es decreciente y no negativa $\implies \lim_{ x \to \infty } f(x) \neq 0$.

(1) Es ==verdadero==. En realidad, no solo se cumple para el valor absoluto, sino en general:
Si $\int_{1}^{+\infty} f(x) dx$ converge $\implies \lim_{ x \to \infty } f(x) = 0$

Es una condición necesaria para asegurar la convergencia, sumar "cada vez menos área".

CORRECCIÓN: Es ==falsa==, ya que la función $f(x)$ no necesariamente tiene límite.

Una integral impropia puede ser convergente si se suma "cada vez menos área", aunque esto no significa que la función interna tenga que tender a 0. En caso de tener límite (asegurado por condiciones extra como decreciente y no negativa), necesariamente es 0.

(2) Es ==verdadera==. Aplicando el criterio Serie-Integral (ya que cumplimos todas las condiciones necesarias) es más sencillo visualizarlo, ya que desarrollamos un teorema que decía: Si $\sum a_{n}$ es convergente, entonces necesariamente $\lim_{ n \to \infty } a_{n} = 0$

CORRECCIÓN: Es ==verdadera==, pero la justificación real es que, como $f$ es decreciente y no negativa, entonces el límite obligatoriamente existe y es un número $L \geq 0$.

Si suponemos que $L > 0$, entonces a partir de cierto valor de $x$, la función siempre será mayor o igual que $L$.

De esta forma, necesariamente $L = 0$.

Sin embargo, al integrar, $\int_{1}^{+\infty} f(x) dx \geq \int_{1}^{+\infty} L dx = +\infty$, lo que contradice que la integral sea convergente

(3) Es ==falso==. Un contraejemplo conocido: $f(x) = \frac{1}{x}$.

Sabemos bien que $\int_{1}^{+\infty} \frac{1}{x} dx$ es divergente, $\frac{1}{x}$ es decreciente y no negativa, y sin embargo $\lim_{ x \to \infty } f(x) = 0$.

---
# Ejercicio 5
Si $f : (a,b] \to \mathbb{R}$ es continua y $\lim_{ x \to a } f(x) = +\infty$, clasifica a la integral:
$$
\int_{a}^{b} f(t) dt
$$
Como vemos, la función $f(x)$ no está definida en $a$ (tiende a $+\infty$ cuando $x \to a$). Por lo tanto, la integral es impropia.

Sin embargo, no podemos confirmar que la integral converja o diverja, ya que este factor depende de la función en si. Por ejemplo
$$
\begin{align}
&\int_{0}^{1} \frac{1}{\sqrt{ t }} dt < \infty \\
&\int_{0}^{1} \frac{1}{t} dt = \infty
\end{align}
$$

También puede no tener límite si consideramos funciones que combinan un crecimiento asintótico con oscilaciones trigonométricas extremas en el punto de discontinuidad.