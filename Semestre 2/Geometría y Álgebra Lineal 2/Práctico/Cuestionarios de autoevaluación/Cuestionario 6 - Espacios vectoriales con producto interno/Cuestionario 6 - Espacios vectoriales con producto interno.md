# Verdadero o falso
## Pregunta 1
Lo verificamos:
- Aditividad con respecto a la primera componente:
$$
\begin{align}
\langle (x_{1}, x_{2}) + (x_{1}', x_{2}'), (y_{1}, y_{2}) \rangle &= \langle (x_{1} + x_{1}', x_{2} + x_{2}'), (y_{1}, y_{2}) \rangle \\
&= 2(x_{1} + x_{1}')\overline{y_{1}} + (x_{1} + x_{1}')\overline{y_{2}} + (x_{2} + x_{2}')\overline{y_{1}} + (x_{2} + x_{2}')\overline{y_{2}} \\
&= 2x_{1}\overline{y_{1}} + x_{1}\overline{y_{2}} + x_{2}\overline{y_{1}} + x_{2}\overline{y_{2}} + 2x_{1}'\overline{y_{1}} + x_{1}'\overline{y_{2}} + x_{2}'\overline{y_{1}} + x_{2}'\overline{y_{2}} \\
&= \langle (x_{1}, x_{2}), (y_{1}, y_{2}) \rangle + \langle (x_{1}', x_{2}'), (y_{1}, y_{2}) \rangle
\end{align}
$$

- Homogeneidad con respecto a la primera componente:
$$
\begin{align}
\langle \alpha \cdot (x_{1}, x_{2}), (y_{1}, y_{2}) \rangle &= \langle (\alpha \cdot x_{1}, \alpha \cdot x_{2}), (y_{1}, y_{2}) \rangle \\
&= 2\alpha \cdot x_{1}\overline{y_{1}} + \alpha \cdot x_{1}\overline{y_{2}} + \alpha \cdot x_{2}\overline{y_{1}} + \alpha \cdot x_{2}\overline{y_{2}} \\
&= \alpha \cdot (2x_{1}\overline{y_{1}} + x_{1}\overline{y_{2}} + x_{2}\overline{y_{1}} + x_{2}\overline{y_{2}}) \\
&= \alpha \cdot \langle (x_{1}, x_{2}), (y_{1}, y_{2}) \rangle
\end{align}
$$

- Simetría:
$$
\begin{align}
\langle (x_{1}, x_{2}), (y_{1}, y_{2}) \rangle &= 2x_{1}\overline{y_{1}} + x_{1}\overline{y_{2}} + x_{2}\overline{y_{1}} + x_{2}\overline{y_{2}} \\
&= \overline{\overline{2x_{1}\overline{y_{1}} + x_{1}\overline{y_{2}} + x_{2}\overline{y_{1}} + x_{2}\overline{y_{2}}}} \\
&= \overline{\overline{2x_{1}\overline{y_{1}}} + \overline{x_{1}\overline{y_{2}}} + \overline{x_{2}\overline{y_{1}}} + \overline{x_{2}\overline{y_{2}}}} \\
&= \overline{2\overline{x_{1}}y_{1} + \overline{x_{1}}y_{2} + \overline{x_{2}}y_{1} + \overline{x_{2}}y_{2}} \\
&= \overline{2y_{1}\overline{x_{1}} + y_{1}\overline{x_{2}} + y_{2}\overline{x_{1}} + y_{2}\overline{x_{2}}} \\
&= \overline{\langle (y_{1}, y_{2}), (x_{1}, x_{2}) \rangle}
\end{align}
$$

- No negatividad (y nulidad solo para $\vec{0}$):
$$
\begin{align}
\langle (x_{1}, x_{2}), (x_{1}, x_{2}) \rangle &= 2x_{1}\overline{x_{1}} + x_{1}\overline{x_{2}} + x_{2}\overline{x_{1}} + x_{2}\overline{x_{2}} \\
&= 2|x_{1}|^{2} + x_{1}\overline{x_{2}} + x_{2}\overline{x_{1}} + |x_{2}|^{2} \\
&= 2(a^{2} + b^{2}) + (a + bi)(c - di) + (a - bi)(c + di) + (c^{2} + d^{2}) \\
&= 2(a^{2} + b^{2}) + ac - \cancel{ adi } + \cancel{ bci } + bd + ac + \cancel{ adi } - \cancel{ bci } + bd + (c^{2} + d^{2}) \\
&= 2a^{2} + 2b^{2} + 2ac + 2bd + c^{2} + d^{2} \\
&= a^{2} + (a^{2} + 2ac + c^{2}) + b^{2} + (b^{2} + 2bd + d^{2}) + d^{2} \\
&= a^{2} + (a + c)^{2} + b^{2} + (b + d)^{2} + d^{2}
\end{align}
$$
Como vemos, logramos expresar todo como la suma de valores reales positivos o nulos (ya que todos están elevados al cuadrado).

Ahora, resta confirmar que $\langle (x_{1}, x_{2}), (x_{1}, x_{2}) = 0 \Longleftrightarrow (x_{1}, x_{2}) = 0$, y esto es verdadero, ya que como expresamos la operación como una suma de elementos elevados al cuadrado, la única forma de que sea 0 es que cada elemento sea 0.

Por lo tanto, el enunciado es ==verdadero==.

---
## Pregunta 3
Para verificar si es una norma, tenemos que probar las propiedades de la norma:
- $||\lambda \cdot u|| = |\lambda| \cdot ||u||, \forall \lambda \in \mathbb{K}, \forall u \in V$
- $||u|| \geq0, \forall u \in V$; $||u|| = 0 \Longleftrightarrow u = \vec{0}$
- $||u + v|| \leq ||u|| + ||v||$ (desigualdad triangular)

- Homogeneidad:
$$
\begin{align}
||\alpha \cdot (x, y)||_{1} &= ||(\alpha \cdot x, \alpha \cdot y)||_{1} \\
&= |\alpha \cdot x| + |\alpha \cdot y| \\
&= |\alpha| \cdot |x| + |\alpha| \cdot |y| \\
&= |\alpha| \cdot (|x| + |y|) \\
&= |\alpha| \cdot ||(x, y)||_{1}
\end{align}
$$

- No negatividad y nulidad solo para el vector nulo:
$$
\begin{align}
||(x, y)||_{1} &= |x| + |y| \geq 0
\end{align}
$$
Como está definida en base al valor absoluto, sabemos que siempre es positiva o nula. Además, únicamente es nula si tanto $x$ como $y$ son 0: $(0, 0)$.

- Desigualdad triangular:
$$
\begin{align}
||(x_{1}, y_{1}) + (x_{2}, y_{2})|| &\leq ||(x_{1}, y_{1})|| + ||(x_{2}, y_{2})|| \\
||(x_{1} + x_{2}, y_{1} + y_{2})|| &\leq ||(x_{1}, y_{1})|| + ||(x_{2}, y_{2})|| \\
|x_{1} + x_{2}| + |y_{1} + y_{2}| &\leq |x_{1}| + |y_{1}| + |x_{2}| + |y_{2}|
\end{align}
$$
Sabemos que:
- $|x_{1} + x_{2}| \leq |x_{1}| + |x_{2}|$
- $|y_{1} + y_{2}| \leq |y_{1}| + |y_{2}|$

Por lo tanto, si sumamos ambas desigualdades:
$$
|x_{1} + x_{2}| + |y_{1} + y_{2}| \leq |x_{1}| + |y_{1}| + |x_{2}| + |y_{2}|
$$

Entonces, la desigualdad triangular se cumple.

Para verificar si deriva de un producto interno, tenemos que ver que cumpla la regla del paralelogramo:
$$
||u + v||^{2} + ||u - v||^{2} = 2||u||^{2} + 2||v||^{2}
$$
$$
\begin{align}
||(x_{1}, y_{1}) + (x_{2}, y_{2})||^{2} + ||(x_{1}, y_{1}) - (x_{2}, y_{2})||^{2} &= 2||(x_{1}, y_{1})||^{2} + 2||(x_{2}, y_{2})||^{2} \\
||(x_{1} + x_{2}, y_{1} + y_{2})||^{2} + ||(x_{1} - x_{2}, y_{1} - y_{2})||^{2} &= 2||(x_{1}, y_{1})||^{2} + 2||(x_{2}, y_{2})||^{2} \\
(|x_{1} + x_{2}| + |y_{1} + y_{2}|)^{2} + (|x_{1} - x_{2}| + |y_{1} - y_{2}|)^{2} &= 2(|x_{1}| + |y_{1}|)^{2} + 2(|x_{2}| + |y_{2}|)^{2} \\
(x_{1} + x_{2})^{2} + 2|(x_{1} + x_{2})(y_{1} + y_{2})| + (y_{1} + y_{2})^{2} + (x_{1} - x_{2})^{2} + 2|(x_{1} - x_{2})(y_{1} - y_{2})| + (y_{1} - y_{2})^{2} &= 2(x_{1}^{2} + 2|x_{1}y_{1}| + y_{1}^{2}) + 2(x_{2}^{2} + 2|x_{2}y_{2}| + y_{2}^{2}) \\
2|(x_{1} + x_{2})(y_{1} + y_{2})| + 2|(x_{1} - x_{2})(y_{1} - y_{2})| &= 4|x_{1}y_{1}| + 4|x_{2}y_{2}| \\
2|x_{1}y_{1} + x_{1}y_{2} + x_{2}y_{1} + x_{2}y_{2}| + 2|x_{1}y_{1} - x_{1}y_{2} - x_{2}y_{1} + x_{2}y_{2}| &= 4|x_{1}y_{1}| + 4|x_{2}y_{2}|
\end{align}
$$
Si seguimos desarrollando la operación, veremos que no logramos probar la regla del paralelogramo. Por lo tanto, la norma no es inducida por algún producto interno en $\mathbb{K}^{2}$, y el enunciado es ==falso==.

---
## Pregunta 4
La desigualdad presentada se corresponde con la desigualdad de Cauchy-Schwarz, por lo que el enunciado es ==verdadero== únicamente si $u$ y $v$ son linealmente dependientes.

---
## Pregunta 5
Si dos vectores son ortogonales, entonces $\langle u, v \rangle = 0$. Entonces, consideremos que $||u||$ es la norma inducida:
$$
\begin{align}
||u + v||^{2} &= ||u||^{2} + ||v||^{2} \\
\langle u + v, u + v \rangle &= \langle u, u \rangle + \langle v, v \rangle \\
\langle u, u + v \rangle + \langle v, u + v \rangle &= \langle u, u \rangle + \langle v, v \rangle \\
\langle u, u \rangle + \langle u, v \rangle + \langle v, u \rangle + \langle v, v \rangle &= \langle u, u \rangle + \langle v, v \rangle \\
\langle u, u \rangle + \langle u, v \rangle + \overline{\langle u, v \rangle} + \langle v, v \rangle &= \langle u, u \rangle + \langle v, v \rangle \\
\langle u, u \rangle + 2\mathrm{Re}(\langle u, v \rangle) + \langle v, v \rangle &= \langle u, u \rangle + \langle v, v \rangle
\end{align}
$$
$$
\implies 2\mathrm{Re}(\langle u, v \rangle) = 0 \implies \langle u, v \rangle = 0
$$
Y sabemos que esto ocurre sí y solo si $u \perp v$.

Por lo tanto, el enunciado es ==verdadero==.

---
## Pregunta 6
En la parte anterior, probamos que su parte real tiene que ser 0.

Analizamos la segunda desigualdad:
$$
\begin{align}
||u + iv||^{2} &= \langle u + iv, u + iv \rangle \\
&= \langle u, u + iv \rangle + \langle iv, u + iv \rangle \\
&= \langle u, u \rangle + \langle u, iv \rangle + \langle iv, u \rangle + \langle iv, iv \rangle \\
&= \langle u, u \rangle + \overline{i}\langle u, v \rangle + i\langle v, u \rangle + i\overline{i}\langle v, v \rangle \\
&= \langle u, u \rangle - i\langle u, v \rangle + i\langle v, u \rangle - i^{2}\langle v, v \rangle \\
&= \langle u, u \rangle + i(-\langle u, v \rangle + \overline{\langle u, v \rangle}) + \langle v, v \rangle \\
&= \langle u, u \rangle - i2\mathrm{Im}(\langle u, v \rangle) + \langle v, v \rangle
\end{align}
$$
$$
\implies 2\mathrm{\mathrm{Re}}(\langle u, v \rangle) = 2\mathrm{\mathrm{Im}}(\langle u, v \rangle) = 0 \implies \langle u, v \rangle = 0
$$

En conclusión, $u \perp v$ y el enunciado es ==verdadero==.

---
# Múltiple opción
## Ejercicio 1
$$
\begin{align}
||2u - v|| &= \sqrt{ \langle 2u - v, 2u - v \rangle } \\
&= \sqrt{ \langle 2u, 2u \rangle - \langle 2u, v \rangle - \langle v, 2u \rangle + \langle v, v \rangle } \\
&= \sqrt{ 4\langle u, u \rangle - 2\langle u, v \rangle - 2\langle v, u \rangle + \langle v, v \rangle } \\
&= \sqrt{ 4||u||^{2} - 2\langle u, v \rangle - 2\overline{\langle u, v \rangle} + ||v||^{2} } \\
&= \sqrt{ 16 - 2(-3 + 4i) - 2(-3 - 4i) + 9 } \\
&= \sqrt{ 16 + 6 - \cancel{ 8i } + 6 + \cancel{ 8i } + 9 } \\
&= \sqrt{ 37 }
\end{align}
$$

### Opción correcta: C

---
## Ejercicio 2
Desarrollamos cada uno de las operaciones presentadas:
$$
\begin{align}
||u + v|| &= \sqrt{ \langle u + v, u + v \rangle } \\
&= \sqrt{ \langle u, u \rangle + \langle u, v \rangle + \langle v, u \rangle + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle + \langle u, v \rangle + \overline{\langle u, v \rangle} + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle + 2\mathrm{Re}(\langle u, v \rangle) + \langle v, v \rangle } = 5 \\
&\implies \langle u, u \rangle + 2\mathrm{Re}(\langle u, v \rangle) + \langle v, v \rangle = 25
\end{align}
$$
$$
\begin{align}
||u - v|| &= \sqrt{ \langle u - v, u - v \rangle } \\
&= \sqrt{ \langle u, u \rangle - \langle u, v \rangle - \langle v, u \rangle + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle - \langle u, v \rangle - \overline{\langle u, v \rangle} + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle - 2\mathrm{Re}(\langle u, v \rangle) + \langle v, v \rangle } = 3 \\
&\implies \langle u, u \rangle - 2\mathrm{Re}(\langle u, v \rangle) + \langle v, v \rangle = 9
\end{align}
$$
Entonces, si consideramos ambas igualdades:
$$
4\mathrm{Re}(\langle u, v \rangle) = 16 \implies \mathrm{Re}(\langle u, v \rangle) = 4
$$

Proseguimos:
$$
\begin{align}
||u + iv|| &= \sqrt{ \langle u + iv, u + iv \rangle } \\
&= \sqrt{ \langle u, u \rangle + \langle u, iv \rangle + \langle iv, u \rangle + \langle iv, iv \rangle } \\
&= \sqrt{ \langle u, u \rangle + \overline{i}\langle u, v \rangle + i\langle v, u \rangle + i\overline{i}\langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle - i\langle u, v \rangle + i\overline{\langle u, v \rangle} + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle + i(-\langle u, v \rangle + \overline{\langle u, v \rangle}) + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle - i \cdot (2i\mathrm{Im}(\langle u, v \rangle)) + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle + 2\mathrm{Im}(\langle u, v \rangle) + \langle v, v \rangle } = 3 \\
&\implies \langle u, u \rangle + 2\mathrm{Im}(\langle u, v \rangle) + \langle v, v \rangle = 9
\end{align}
$$
$$
\begin{align}
||u - iv|| &= \sqrt{ \langle u - iv, u - iv \rangle } \\
&= \sqrt{ \langle u, u \rangle - \langle u, iv \rangle - \langle iv, u \rangle + \langle iv, iv \rangle } \\
&= \sqrt{ \langle u, u \rangle - \overline{i}\langle u, v \rangle - i\langle v, u \rangle + i\overline{i}\langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle + i\langle u, v \rangle - i\overline{\langle u, v \rangle} + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle + i(\langle u, v \rangle - \overline{\langle u, v \rangle}) + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle + i \cdot (2i\mathrm{Im}(\langle u, v \rangle)) + \langle v, v \rangle } \\
&= \sqrt{ \langle u, u \rangle - 2\mathrm{Im}(\langle u, v \rangle) + \langle v, v \rangle } = 5 \\
&\implies \langle u, u \rangle - 2\mathrm{Im}(\langle u, v \rangle) + \langle v, v \rangle = 25
\end{align}
$$
Unimos los resultados:
$$
4\mathrm{Im}(\langle u, v \rangle) = -16 \implies \mathrm{Im}(\langle u, v \rangle) = -4
$$

En conclusión, como $\mathrm{Re}(\langle u, v \rangle) = 4$ y $\mathrm{Im}(\langle u, v \rangle) = -4$, determinamos que $\langle u, v \rangle = 4 - 4i$

### Opción correcta: D

---
## Ejercicio 3
El ángulo entre dos vectores $u$ y $v$ se define como:
$$
\cos \theta = \frac{\langle u, v \rangle}{||u|| \cdot ||v||}
$$
Entonces, prosigamos a calcular los valores propuestos:
$$
\begin{align}
||p|| &= \sqrt{ \langle p, p \rangle } \\
&= \sqrt{ \int_{0}^{1} p^{2}(x) dx } \\
&= \sqrt{ \int_{0}^{1} 1 dx } \\
&= \sqrt{ x |_{0}^{1} } \\
&= \sqrt{ 1 - 0 } \\
&= \sqrt{ 1 } \\
&= 1
\end{align}
$$
$$
\begin{align}
||q|| &= \sqrt{ \langle q, q \rangle } \\
&= \sqrt{ \int_{0}^{1} q^{2}(x) dx } \\
&= \sqrt{ \int_{0}^{1} x^{2} dx } \\
&= \sqrt{ \frac{x^{3}}{3} |_{0}^{1} } \\
&= \sqrt{ \frac{1}{3} - 0 } \\
&= \sqrt{ \frac{1}{3} }
\end{align}
$$
$$
\begin{align}
\langle p, q \rangle &= \int_{0}^{1} p(x)q(x) dx \\
&= \int_{0}^{1} x dx \\
&= \frac{x^{2}}{2} |_{0}^{1} \\
&= \frac{1}{2} - 0 \\
&= \frac{1}{2}
\end{align}
$$
Ahora, sustituimos en la fórmula:
$$
\cos \theta = \frac{\langle p, q \rangle}{||p|| \cdot ||q||} = \frac{\frac{1}{2}}{1 \cdot \sqrt{ \frac{1}{3} }} = \frac{\frac{1}{2}}{\frac{1}{\sqrt{ 3 }}} = \frac{\sqrt{ 3 }}{2}
$$
Ahora, si evaluamos las opciones del valor de $\theta$, podemos ver que:
- No es la $B$ ya que el valor correspondiente es 1.
- No es la $C$ ya que el valor correspondiente es $\frac{1}{2}$.

En conclusión, $\theta = \frac{\pi}{6}$.

### Opción correcta: A

---
