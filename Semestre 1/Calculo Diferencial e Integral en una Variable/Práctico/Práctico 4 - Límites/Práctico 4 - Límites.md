# 4.1 - Interpretación geométrica de límites

## Ejercicio 4.1.1
Para determinar si una función tiene límite cuando tiene a un valor puntual de $x$ observando su gráfica, hay que ver si la función es continua en dicho punto. Básicamente, el límite por izquierda debe ser equivalente al límite por derecha:

### Parte a)
$\lim_{ x \to -1 } g(x)$ no existe, ya que el límite por derecha y por izquierda son diferentes:
$$
\begin{align}
&\lim_{ x \to -1^{-} } g(x) = 2 \\
&\lim_{ x \to -1^{+} } g(x) = 0
\end{align}
$$

### Parte b)
$\lim_{ x \to 0 } g(x)$ no existe, ya que el límite por derecha y por izquierda son diferentes:
$$
\begin{align}
&\lim_{ x \to 0^{-} } g(x) = 0 \\
&\lim_{ x \to 0^{+} } g(x) = 1
\end{align}
$$

### Parte c)
$$
\lim_{ x \to 1 } g(x) = 0
$$
Aunque $f(x) = 2 (\neq 0)$ esto no importa, ya que $f(x_{0})$ no determina $\lim_{ x \to x_{0} } f(x)$.

### Parte d)
$$
\lim_{ x \to 2 } g(x) = 1
$$

### Cálculo de imágenes
$$
\begin{align}
&g(-1) = 0 \\
&g(0) = 1 \\
&g(1) = 2 \\
&g(2) = 1
\end{align}
$$

---
## Ejercicio 4.1.2
### Parte a)
$\lim_{ x \to 0 } f(x) \neq 0$ ya que, para los valores de $x$ cercanos a 0, el límite por izquierda ($\lim_{ x \to 0^{-} } f(x) = 0$) es diferente al límite por derecha ($\lim_{ x \to 0^{+} } f(x) = 3$). 0 únicamente coincide con la imagen de los valores cercanos a cero por su izquierda, pero no por su derecha.

### Parte b)
Similar a la parte a. En este caso, $f(0) = 2$, pero la imagen de un punto no determina la existencia ni el valor del límite en ese punto.

### Parte c)
Ídem a la parte a. 3 únicamente coincide con la imagen de los valores cercanos a cero por su derecha, pero no por su izquierda.

---
## Ejercicio 4.1.3
Como la función "salta" cada vez que se avanza al siguiente entero, entonces existe límite para todo $a$ siempre que $a \not \in \mathbb{Z}$.

Además, el límite para todo $a \not \in \mathbb{Z}$ coincide con su imagen:
$$
\lim_{ x \to a } f(x) = f(a) \qquad (\forall a \not \in \mathbb{Z})
$$

---
## Ejercicio 4.1.4



---
# 4.2 - Definición y propiedades básicas de límites
## Ejercicio 4.2.1
### Parte a)
$$
f(x) = x^{2}, a = 0
$$
$$
L = \lim_{ x \to 0 } x^{2} = 0
$$
De esta forma, $L = 0$.

Dado $\epsilon > 0$:
$$
\begin{align}
&|x^{2} - 0^{2}| < \epsilon \\
&x^{2} < \epsilon
\end{align}
$$
Proseguimos con $\delta$:
Sabemos que, como
$$
\begin{align}
&|x - 0| < \delta \\
&|x| < \delta \implies -\delta < x < \delta
\end{align}
$$

De esta forma:
$$
\begin{align}
0 < x^{2} < &\delta^{2} < \epsilon \\
&\delta^{2} - \epsilon < 0 \\
&(\delta - \sqrt{ \epsilon })(\delta + \sqrt{ \epsilon }) < 0
\end{align}
$$
De esta forma, $\delta = \pm \sqrt{ \epsilon }$ como máximo.

### Parte b)
$$
f(x) = \frac{1}{x}, a = 1
$$


### Parte d)
$$
f(x) = x^{2}, a \in \mathbb{R}
$$
$$
\lim_{ x \to a } x^{2} = a^{2}
$$
De esta forma, $L = a^{2}$.

Dado $\epsilon > 0$:
$$
\begin{align}
&|x^{2} - a^{2}| < \epsilon \\
&|(x - a)(x + a)| < \epsilon \\
&|x - a||x + a| < \epsilon
\end{align}
$$
Proseguimos con $\delta$:
Sabemos que, como
$$
|x - a| < \delta \implies a - \delta < x < a + \delta
$$
$$
\begin{align}
&a + a - \delta < a + x < a + a + \delta = 2a + \delta \\
&2a - \delta < a + x < 2a + \delta
\end{align}
$$
$$
\begin{align}
&|a + x| &< |2a + \delta| \\
&&\leq |2a| + \delta \\
&&= 2|a| + \delta
\end{align}
$$
De esta forma:
$$
\begin{align}
0 < |x - a||x + a| < &\delta (2|a| + \delta) < \epsilon \\
&2|a| \delta + \delta^{2} < \epsilon \\
&\delta^{2} + 2|a| \delta - \epsilon < 0
\end{align}
$$
Aplicamos Bhaskara:
$$
\begin{align}
0 < \delta < &\frac{-2|a| \pm \sqrt{ (2|a|)^{2} - 4 \times 1 - \epsilon }}{2 \times 1} \\
&\frac{-2|a| \pm \sqrt{ 4a^{2} + 4\epsilon }}{2} \\
&\frac{-2|a| \pm \sqrt{ 4(a^{2} + \epsilon) }}{2} \\
&\frac{\cancel{ -2 }|a| \pm \cancel{ 2 }\sqrt{ a^{2} + \epsilon }}{\cancel{ 2 }} \\
&|a| \pm \sqrt{ a^{2} + \epsilon }
\end{align}
$$
De esta forma, tenemos que tomar $\delta = |a| + \sqrt{ a^{2} + \epsilon }$ para asegurar que $\delta > 0$.

Por ejemplo, si $\epsilon = 10^{-2}$, puedo tomar:
$$
\delta = -|a| + \sqrt{ a^{2} + 10^{-2} }
$$

### Parte e)
$$
f(x) = \frac{1}{x}, a \in \mathbb{R}^{+}
$$
$$
L = \lim_{ x \to a } \frac{1}{x} = \frac{1}{a}
$$
De esta forma, $L = \frac{1}{a}$.

Dado $\epsilon > 0$:
$$
\begin{align}
&\left| \frac{1}{x} - \frac{1}{a} \right| < \epsilon \\
&\left| \frac{a - x}{ax} \right| < \epsilon \\
&\left| \frac{x - a}{ax} \right| < \epsilon \\
&\left| (x - a)\frac{1}{ax} \right| < \epsilon \\
&\left| x - a \right| \left| \frac{1}{ax} \right| < \epsilon
\end{align}
$$
Proseguimos con $\delta$:
Sabemos que, como
$$
|x - a| < \delta \implies a - \delta < x < a + \delta
$$
$$
\begin{align}
&\frac{a - \delta}{ax^{2}} < \frac{x}{ax^{2}} < \frac{a + \delta}{ax^{2}} \\
&\frac{1}{x^{2}} - \frac{\delta}{ax^{2}} < \frac{1}{ax} < \frac{1}{x^{2}} + \frac{\delta}{ax^{2}}
\end{align}
$$

Como vemos, llegamos a un obstáculo: si bien obtuvimos una cota para $\frac{1}{ax}$, el problema es que depende de $x$ ($\frac{1}{x^{2}}$). Tenemos que acotar ese término por una constante numérica que solo dependa de $a$.

Para solucionar esto, supondremos un $\delta$ inicial.

Para que $\frac{1}{ax}$ no crezca indefinidamente, tenemos que asegurarnos de que $x$ no se acerque demasiado a 0. Como $a > 0$, podemos establecer que $x$ se mantenga a una distancia de al menos $\frac{a}{2}$ del origen.

Entonces, tomamos $\delta_{1} = \frac{a}{2}$:
$$
a - \frac{a}{2} < x < a + \frac{a}{2} \implies \frac{a}{2} < x < \frac{3a}{2}
$$
De esto, únicamente nos interesa el límite inferior $x > \frac{a}{2}$. Además, podemos invertir los términos para alcanzar los valores deseados:
$$
\frac{a}{2} < x \implies \frac{1}{x} < \frac{2}{a}
$$
Ahora, podemos retomar la expresión $\frac{1}{ax}$ y sustituir $x$ por la cota constante:
$$
\left| \frac{1}{ax} \right| = \frac{1}{a} \cdot \frac{1}{|x|} < \frac{1}{a} \cdot \frac{2}{a} = \frac{2}{a^{2}}
$$

Finalmente, podemos determinar el valor de $\delta$:
$$
\begin{align}
0 < |x - a| \left|  \frac{1}{ax}  \right| < &|x - a| \frac{2}{a^{2}} < \epsilon \\
&|x - a| < \frac{\epsilon}{\frac{2}{a^{2}}} \\
&|x - a| < \frac{a^{2}\epsilon}{2}
\end{align}
$$
De esta manera, $\delta_{2} = \frac{a^{2}\epsilon}{2}$.

En conclusión:
Para garantizar que se cumplan ambas condiciones:
- $x$ no se acerque a 0.
- la distancia a $L$ sea menor que $\epsilon$.
Tenemos que definir a $\delta$ como:
$$
\delta = min\left( \frac{a}{2}, \frac{a^{2}\epsilon}{2} \right)
$$

### Parte f)
$$
f(x) = \sqrt{ |x| }, a \in \mathbb{R}
$$
Comenzamos con $L$:
$$
\lim_{ x \to a } \sqrt{ |x| } = \sqrt{ |a| }
$$
Continuamos con $\epsilon > 0$:
$$
\begin{align}
&|f(x) - L| < \epsilon \\
&\left| \sqrt{ |x| } - \sqrt{ |a| } \right| < \epsilon
\end{align}
$$
Desarrollamos a partir del conjugado para llegar a $|x - a|$.
$$
\begin{align}
&=\frac{\left| \sqrt{ |x| } - \sqrt{ |a| } \right| \cdot \left| \sqrt{ |x| } + \sqrt{ |a| } \right|}{ \sqrt{ |x| } + \sqrt{ |a| } } \\
&=\frac{|x| - |a|}{ \sqrt{ |x| } + \sqrt{ |a| } } \\
&=\frac{|x - a|}{ \sqrt{ |x| } + \sqrt{ |a| } }
\end{align}
$$
Ahora, necesitamos acotar el denominador. Sabiendo que $\sqrt{ |x| } \geq 0$:
$$
\sqrt{ |x| } + \sqrt{ |a| } \geq \sqrt{ |a| }
$$
Ahora, si consideramos los inversos, obtenemos la cota superior:
$$
\frac{1}{\sqrt{ |x| } + \sqrt{ |a| }} \leq \frac{1}{\sqrt{ |a| }}
$$
A continuación, en nuestra desigualdad objetivo:
$$
\begin{align}
\left| \sqrt{ |x| } - \sqrt{ |a| } \right| \leq &\frac{|x - a|}{\sqrt{ |a| }} < \epsilon \\
&|x - a| < \epsilon\sqrt{ |a| }
\end{align}
$$
Es así que para el caso $a \neq 0$, podemos considerar
$$
\delta = \epsilon \sqrt{ |a| }
$$

ACLARACIÓN: SIEMPRE QUE TRABAJEMOS CON RAÍZ CUADRADA Y QUERRAMOS SIMPLIFICAR, COMBIENE UTILIZAR EL CONJUGADO Y DESARROLLAR EL PRODUCTO.

---
## Ejercicio 4.2.2

---
## Ejercicio 4.2.4

Tenemos dos funciones $f, g : I \to \mathbb{R}$, donde $I$ es un intervalo abierto y $p \in I$, tal que
$$
\lim_{ x \to p } f(x) = a, \lim_{ x \to p } g(x) = b
$$
### Parte a)
La función $h$ esta definida por $h(x) = f(x) + \lambda$. Por lo tanto, podemos aplicar propiedades de los límites para probar que
$$
\lim_{ x \to p } h(x) = \lambda + a
$$
Sabemos que $h$ está definida en base a $f$, la cual tiene límite cuando $x \to p$ y es $a$. Además, también está definida por la función constante $\lambda$ (llamémosla $i(x) = \lambda$), cuyo límite es $\lambda$ para cualquier valor de $x$ estudiado. Por esta razón, podemos deducir que el límite cuando $x \to p$ en la función $h$ está dado por la combinación de dichos límites por separado:
$$
\lim_{ x \to p } h(x) = \underbrace{ \lim_{ x \to p } f(x) }_{ a } + \underbrace{ \lim_{ x \to p } i(x) }_{ \lambda } = a + \lambda
$$

### Parte b)
Ídem que el caso anterior. En lugar de tener una función definida a partir de una función que tiene límite para $x \to p$ y una constante, nos enfrentamos a una función definida a partir de dos funciones, las cuales tienen límite en $x \to p$, queriendo encontrar el límite para $x \to p$ en esta última.

Tenemos que
$$
h(x) = f(x) + g(x)
$$
y
$$
\begin{align}
&\lim_{ x \to p } f(x) = a \\
&\lim_{ x \to p } g(x) = b
\end{align}
$$
y queremos determinar que
$$
\lim_{ x \to p } h(x) = a + b
$$

¿Cómo llegamos a dicha conclusión?
Partimos de la definición de la función $h$, definida a partir de las funciones $f$ y $g$. Como las funciones $f$ y $g$ tienen límite cuando $x \to p$, entonces $h$ también lo tendrá y será la suma de ambos límites, aplicando la propiedad:
$$
\lim_{ x \to p } f(x) + g(x) = \lim_{ x \to p } f(x) + \lim_{ x \to p } g(x)
$$
Es así que concluimos que:
$$
\lim_{ x \to p } h(x) = \underbrace{ \lim_{ x \to p } f(x) }_{ a } + \underbrace{ \lim_{ x \to p } g(x) }_{ b } = a + b
$$

---
## Ejercicio 4.2.5
### Parte a)
$$
\begin{align}
&\lim_{ x \to 3 } \frac{2 f(x)}{x} = 1 \\
&\lim_{ x \to 3 } 2 f(x) \times \lim_{ x \to 3 } \frac{1}{x} = 1 \\
&2 \times \lim_{ x \to 3 } f(x) \times \lim_{ x \to 3 } \frac{1}{x} = 1
\end{align}
$$
Entonces:
$$
\lim_{ x \to 3 } f(x) \times \lim_{ x \to 3 } \frac{1}{x} = \frac{1}{2}
$$
Además:
$$
\lim_{ x \to 3 } \frac{1}{x} = \frac{1}{3}
$$
En conclusión:
$$
\begin{align}
&\lim_{ x \to 3 } f(x) \times \frac{1}{3} = \frac{1}{2} \\
&\lim_{ x \to 3 } f(x) = \frac{\frac{1}{2}}{\frac{1}{3}} \\
&\lim_{ x \to 3 } f(x) = \frac{3}{2}
\end{align}
$$
De esta forma:
$$
\lim_{ x \to a } f(x) = \frac{3}{2}, a = 3
$$

### Parte d)
$$
\begin{align}
&\lim_{ x \to 0 } \frac{f(x)}{\sin(x)} = 5 \\
&\lim_{ x \to 0 } f(x) \times \lim_{ x \to 0 } \frac{1}{\sin(x)} = 5
\end{align}
$$
Sabemos que:
$$
\begin{align}
&\lim_{ x \to 0^{+} } \frac{1}{\sin(x)} = +\infty \\
&\lim_{ x \to 0^{-} } \frac{1}{\sin(x)} = -\infty
\end{align}
$$
De esta forma, si consideramos:
$$
\begin{align}
&\lim_{ x \to 0 } f(x) \times \lim_{ x \to 0 } \frac{1}{\sin(x)} = 5 \\
&\lim_{ x \to 0 } f(x) = \frac{5}{\lim_{ x \to 0 } \frac{1}{\sin(x)}}
\end{align}
$$
La única posibilidad es que:
$$
\begin{align}
&\lim_{ x \to 0^{+} } f(x) = 0^{+} \\
&\lim_{ x \to 0^{-} } f(x) = 0^{-}
\end{align}
$$
En conclusión:
$$
\lim_{ x \to 0 } f(x) = 0
$$

---
# 4.3 - Cálculo de límites
## Ejercicio 4.3.1
### Parte a)
$$
\lim_{ x \to 2 } \frac{x^{2} - x + 2}{x^{2} + 4}
$$
Como son polinomios, sabemos que son continuos en todos sus puntos, por lo tanto:
$$
\lim_{ x \to a } f(x) = f(a)
$$
$$
\begin{align}
&\lim_{ x \to 2 } x^{2} - x + 2 = 2^{2} - \cancel{ 2 } + \cancel{ 2 } = 4 \\
&\lim_{ x \to 2 } x^{2} + 4 = 2^{2} + 4 = 4 + 4 = 8
\end{align}
$$
$$
\implies \lim_{ x \to 2 } \frac{x^{2} - x + 2}{x^{2} + 4} = \frac{4}{8} = \frac{1}{2}
$$

### Parte d)
$$
\lim_{ x \to 1 } \frac{e^{x}}{x}
$$
Ambas funciones son constantes cuando $x \to 1$:
$$
\begin{align}
&\lim_{ x \to 1 } e^{x} = e^{1} = e \\
&\lim_{ x \to 1 } x = 1
\end{align}
$$
$$
\implies \lim_{ x \to 1 } \frac{e^{x}}{x} = \frac{e}{1} = e
$$

### Parte g)
$$
\lim_{ x \to 1 } \frac{x^{2} - 1}{x^{2} - 3x + 2}
$$
Si intentamos calcular directamente la imagen para $x = 1$, obtenemos una indeterminación:
$$
\lim_{ x \to 1 } \frac{x^{2} - 1}{x^{2} - 3x + 2} = \frac{1 - 1}{1 - 3 + 2} = \frac{0}{0}
$$
Por esta razón, tenemos que factorizar los polinomios:
$$
\lim_{ x \to 1 } \frac{x^{2} - 1}{x^{2} - 3x + 2} = \lim_{ x \to 1 } \frac{\cancel{ (x - 1) }(x + 1)}{\cancel{ (x - 1) }(x - 2)} = \lim_{ x \to 1 } \frac{x + 1}{x - 2}
$$
Ahora si podemos sustituir $x$ por 1 sin problemas:
$$
\begin{align}
&\lim_{ x \to 1 } x + 1 = 2 \\
&\lim_{ x \to 1 } x - 2 = -1
\end{align}
$$
En conclusión:
$$
\lim_{ x \to 1 } \frac{x^{2} - 1}{x^{2} - 3x + 2} = \lim_{ x \to 1 } \frac{x + 1}{x - 2} = \frac{2}{-1} = -2
$$

### Parte i)
$$
\lim_{ x \to 1 } \frac{\sqrt{ x } - 1}{x - 1}
$$
Si sustituimos a $x$ por 1 directamente, obtenemos una indeterminación:
$$
\lim_{ x \to 1 } \frac{\sqrt{ x } - 1}{x - 1} = \frac{1 - 1}{1 - 1} = \frac{0}{0}
$$
Tenemos que utilizar el conjugado del numerador:
$$
\frac{\sqrt{ x } - 1}{x - 1} = \frac{(\sqrt{ x } - 1)(\sqrt{ x } + 1)}{(x - 1)(\sqrt{ x } + 1)} = \frac{\cancel{ x - 1 }}{\cancel{ (x - 1) }(\sqrt{ x } + 1)} = \frac{1}{\sqrt{ x } + 1}
$$
De esta forma:
$$
\lim_{ x \to 1 } \frac{\sqrt{ x } - 1}{x - 1} = \lim_{ x \to 1 } \frac{1}{\sqrt{ x } + 1} = \frac{1}{\sqrt{ 1 } + 1} = \frac{1}{2}
$$

### Parte j)
$$
\lim_{ x \to 0 } \frac{\sqrt{ 1 + x } - \sqrt{ 1 - x }}{x}
$$
Utilizamos el conjugado del numerador:
$$
\frac{\sqrt{ 1 + x } - \sqrt{ 1 - x }}{x} = \frac{(\sqrt{ 1 + x } - \sqrt{ 1 - x })(\sqrt{ 1 + x } + \sqrt{ 1 - x })}{x(\sqrt{ 1 + x } + \sqrt{ 1 - x })} = \frac{(1 + x) - (1 - x)}{x(\sqrt{ 1 + x } + \sqrt{ 1 - x })}
$$
$$
= \frac{\cancel{ 1 } + x - \cancel{ 1 } + x}{x(\sqrt{ 1 + x } + \sqrt{ 1 - x })} = \frac{2\cancel{ x }}{\cancel{ x }(\sqrt{ 1 + x } + \sqrt{ 1 - x })} = \frac{2}{\sqrt{ 1 + x } + \sqrt{ 1 - x }}
$$
Ahora si podemos sustituir $x$ por 0:
$$
\lim_{ x \to 0 } \frac{\sqrt{ 1 + x } - \sqrt{ 1 - x }}{x} = \lim_{ x \to 0 } \frac{2}{\sqrt{ 1 + x } + \sqrt{ 1 - x }} = \frac{2}{\sqrt{ 1 + 0 } + \sqrt{ 1 - 0 }} = \frac{2}{\sqrt{  1 } + \sqrt{ 1 }} = \frac{2}{2} = 1
$$

### Parte l)
$$
\lim_{ x \to a } \frac{x^{2} - a^{2}}{x - a}
$$
No podemos sustituir $x$ por $a$, ya que obtenemos una indeterminación:
$$
\lim_{ x \to a } \frac{x^{2} - a^{2}}{x - a} = \frac{a^{2} - a^{2}}{a - a} = \frac{0}{0}
$$
Utilizaremos el conjugado del denominador:
$$
\frac{x^{2} - a^{2}}{x - a} = \frac{(x^{2} - a^{2})(x + a)}{(x - a)(x + a)} = \frac{\cancel{ (x^{2} - a^{2}) }(x + a)}{\cancel{ x^{2} - a^{2} }} = x + a
$$
De esta forma:
$$
\lim_{ x \to a } \frac{x^{2} - a^{2}}{x - a} = \lim_{ x \to a } x + a = a + a = 2a
$$

---
## Ejercicio 4.3.2
### Parte a)
$$
\lim_{ x \to a } \lceil x \rceil - \lfloor x \rfloor
$$
Aquí tenemos dos casos:
1. $a \in \mathbb{Z}$:
$$
\lceil a \rceil = \lfloor a \rfloor \implies \lceil a \rceil - \lfloor a \rfloor = 0
$$
2. $a \not \in \mathbb{Z}$
$$
\lceil a \rceil \neq \lfloor a \rfloor \implies \lceil a \rceil - \lfloor a \rfloor = 1
$$
Igualmente, como la función es 0 solo en los casos en los que $a$ es entero, no modifica el valor del límite en dichos puntos. Por lo tanto:
$$
\lim_{ x \to a } \lceil x \rceil - \lfloor x \rfloor = 1
$$

$$
\lim_{ x \to 0 } \lceil x \rceil - \lfloor x \rfloor = 1
$$
Aunque 
$$
\lceil 0 \rceil - \lfloor 0 \rfloor = 0
$$

### Parte c)
$$
\lim_{ x \to 1 } \frac{\left| (x - 1)^{3} \right|}{(x - 1)^{2}}
$$
$$
\frac{\left| (x - 1)^{3} \right|}{(x - 1)^{2}} = \frac{\left| (x - 1)\cancel{ (x^{2} - 2x + 1) } \right|}{\cancel{ x^{2} - 2x + 1 }} = \left| x - 1 \right|
$$

De esta forma:
$$
\lim_{ x \to 1 } \frac{\left| (x - 1)^{3} \right|}{(x - 1)^{2}} = \lim_{ x \to 1 } \left| x - 1 \right| = |1 - 1| = 0
$$

### Parte d)
$$
\lim_{ x \to 2 } \frac{\left| x^{4} - 6x^{3} + 12x^{2} - 8x \right|}{x^{5} - 5x^{4} + 6x^{2} + 4x - 8}
$$
Podemos intentar sustituir $x$ por 2:
$$
\lim_{ x \to 2 } \frac{\left| x^{4} - 6x^{3} + 12x^{2} - 8x \right|}{x^{5} - 5x^{4} + 6x^{2} + 4x - 8} = \frac{|16 - 6 \times 8 + 12 \times 4 - 8 \times 2|}{32 - 5 \times 16 + 6 \times 4 + 4 \times 2 - 8} = \frac{|\cancel{ 16 } - \cancel{ 48 } + \cancel{ 48 } - \cancel{ 16 }|}{32 - 80 + 24 + \cancel{ 8 } - \cancel{ 8 }} = \frac{0}{-24}
$$
Podríamos intentar factorizar, sin embargo, el polinomio divisor no tiene raíces enteras.
$$
\begin{align}
&x^{4} - 6x^{3} + 12x^{2} - 8x = x(x - 2)^{3} \\
&x^{5} - 5x^{4} + 6x^{2} + 4x - 8 = \text{?}
\end{align}
$$

Podemos operar con tranquilidad:
$$
\lim_{ x \to 2 } \frac{\left| x^{4} - 6x^{3} + 12x^{2} - 8x \right|}{x^{5} - 5x^{4} + 6x^{2} + 4x - 8} = \frac{0}{-24} = 0
$$

### Parte f)
$$
\lim_{ x \to 0 } \left[ \frac{1}{x} \right]
$$
El límite anterior no existe, ya que la función oscila infinitamente a medida que $x$ se acerca a 0.

---
## Ejercicio 4.3.4
Tenemos que:
$$
\begin{align}
&P(x) = \sum_{k = 0}^{n} a_{k}x^{k} \\
&Q(x) = \sum_{j = 0}^{m} b_{j}x^{j}
\end{align}
$$
Como $a \in \mathbb{R}$ es raíz de $P$ y $Q$, entonces tenemos que:
$$
\begin{align}
&P(x) = P_{1}(x)(x - a)^{n_{1}} \\
&Q(x) = Q_{1}(x)(x - a)^{m_{1}}
\end{align}
$$

### Parte a, b y c)
$$
\lim_{ x \to a } \frac{P(x)}{Q(x)} = 0 \text{ si y sólo si } n_{1} > m_{1}
$$
Sabemos que $a$ es raíz de $P$ y $Q$, entonces tenemos que:
$$
\begin{align}
&P(a) = 0 \\
&Q(a) = 0
\end{align}
$$
Por esta razón, llegamos a una indeterminación. Sin embargo, podemos aprovechar otras formas de expresar $P(x)$ y $Q(x)$ sabiendo que $a$ es raíz de ambas:
$$
\begin{align}
&P(x) = P_{1}(x)(x - a)^{n_{1}} \\
&Q(x) = Q_{1}(x)(x - a)^{m_{1}}
\end{align}
$$
De esta forma:
$$
\lim_{ x \to a } \frac{P(x)}{Q(x)} = \frac{P(a)}{Q(a)} = \frac{P_{1}(a)(a - a)^{n_{1}}}{Q_{1}(a)(a - a)^{m_{1}}}
$$
Es así que podemos distinguir tres casos en base a los exponentes:
1. $n_{1} < m_{1}$
$$
\frac{P_{1}(a)\cancel{ (a - a)^{n_{1}} }}{Q_{1}(a)(a - a)^{\cancelto{ m_{1} - n_{1} }{ m_{1} }}} = \frac{P_{1}(a)}{Q_{1}(a)(a - a)^{m_{1} - n_{1}}} = \frac{P_{1}(a)}{Q_{1}(a)(0)^{m_{1} - n_{1}}} = \frac{P_{1}(a)}{0}
$$
Como vemos, el resultado depende de $P_{1}(a)$, pudiendo tratarse de una indeterminación si $P_{1}(a) = 0$. Si $P_{1}(a) \neq 0$, tenemos dos casos (únicamente consideraremos el límite cuando $x$ tiende a $a$ por derecha):
	1. $P_{1}(a) < 0$
	Como $P_{1}(a)$ es negativo, pero los valores que toma $x$ no:
	$$
	\lim_{ x \to a } \frac{P(x)}{Q(x)} = \frac{P_{1}(a)}{0} \implies \lim_{ x \to a } \frac{P(x)}{Q(x)} = -\infty
	$$
	2. $P_{1}(a) > 0$
	Como $P_{1}(a)$ es positivo, y los valores que toma $x$ también:
	$$
	\lim_{ x \to a } \frac{P(x)}{Q(x)} = \frac{P_{1}(a)}{0} \implies \lim_{ x \to a } \frac{P(x)}{Q(x)} = +\infty
	$$

3. $n_{1} = m_{1}$
$$
\frac{P_{1}(a)\cancel{ (a - a)^{n_{1}} } }{Q_{1}(a)\cancel{ (a - a)^{ m_{1} } }} = \frac{P_{1}(a)}{Q_{1}(a)}
$$
En este caso, el límite está dado por el resultado de dividir $\frac{P_{1}(a)}{Q_{1}(a)}$.

3. $n_{1} > m_{1}$
$$
\frac{P_{1}(a)(a - a)^{\cancelto{ n_{1} - m_{1} }{ n_{1} }} }{Q_{1}(a)\cancel{ (a - a)^{ m_{1} } }} = \frac{P_{1}(a)(a - a)^{n_{1} - m_{1}} }{Q_{1}(a)} = \frac{P_{1}(a)(0)^{n_{1} - m_{1}} }{Q_{1}(a)} = \frac{0}{Q_{1}(a)}
$$
De esta forma, el límite es 0.

En conclusión, demostramos que
$$
\begin{align}
&\lim_{ x \to a } \frac{P(x)}{Q(x)} = 0 \text{ si y sólo si } n_{1} > m_{1} \\
&\lim_{ x \to a } \frac{P(x)}{Q(x)} = \frac{P_{1}(x)}{Q_{1}(x)} \text{ si y sólo si } n_{1} = m_{1} \\
&\lim_{ x \to a } \frac{P(x)}{Q(x)} = + \infty \text{ o } - \infty \text{ si y sólo si } n_{1} > m_{1}
\end{align}
$$

---
## Ejercicio 4.3.5
### Parte a)
$$
\lim_{ x \to 0 } x \sin\left( \frac{1}{x} \right)
$$
Aplicando propiedades de límites:
$$
\lim_{ x \to 0 } x \sin\left( \frac{1}{x} \right) = \lim_{ x \to 0 } x \times \lim_{ x \to 0 } \sin\left( \frac{1}{x} \right)
$$
Ahora, podemos estudiar cada uno por separado:
$$
\begin{align}
&\lim_{ x \to 0 } x = 0\\
&-1 = \lim_{ x \to 0 } -1 \leq \lim_{ x \to 0 } \sin\left( \frac{1}{x} \right) \leq \lim_{ x \to 0 } 1 = 1
\end{align}
$$
Como sabemos que la función $\sin$ necesariamente está acotada entre -1 y 1, podemos determinar que:
$$
\lim_{ x \to 0 } x \sin\left( \frac{1}{x} \right) = \underbrace{ \lim_{ x \to 0 } x }_{ \to 0 } \times \underbrace{ \lim_{ x \to 0 } \sin\left( \frac{1}{x} \right) }_{ \text{Acotada entre } -1, 1 } = 0
$$
Esto sin importar que $\sin\left( \frac{1}{x} \right)$ oscile infinitamente cuando $x \to 0$.

---
## Ejercicio 4.3.6
### Parte a)
$$
\lim_{ x \to 1 } \frac{\log(x)}{x - 1}
$$
Si sustituimos $x$ por 1, llegamos a una indeterminación:
$$
\lim_{ x \to 1 } \frac{\log(x)}{x - 1} = \frac{\log(1)}{1 - 1} = \frac{0}{0}
$$
Por esta razón, tenemos que buscar otro camino.

Consideremos la definición de logaritmo:
$$
\log(x) = \int_{1}^{x} \frac{1}{t} \space dt
$$

Entonces:
$$
\frac{\log(x)}{x - 1} = \frac{\int_{1}^{x} \frac{1}{t} \space dt}{x - 1} = \frac{1}{x - 1} \int_{1}^{x} \frac{1}{t} \space dt
$$
Como vemos, llegamos a una expresión que coincide exactamente con la definición de valor medio vista en el curso ([[Libro CDIV - Edición 2025.pdf#page=145|Ir a página 145]]).
Como la función es continua en el intervalo de integración (para $x > 0$), existe un punto $c \in [1, x]$ tal que:
$$
f(c) = \frac{1}{x - 1} \int_{1}^{x} \frac{1}{t} \space dt
$$
Ahora, sustituimos $f(c)$ por su valor:
$$
\frac{1}{c} = \frac{\log(x)}{x - 1}
$$
Ahora, tenemos que calcular el límite cuando $x \to 1$:
$$
\lim_{ x \to 1 } \frac{\log(x)}{x - 1} = \lim_{ x \to 1 } \frac{1}{c}
$$
Como $c$ es un valor intermedio entre 1 y $x$, cuando $x \to 0$, necesariamente $c \to 0$ (si se reduce el intervalo $[1, x]$, de tal forma que $x$ se acerca a 0, entonces $c$ también se acerca a 0):
$$
\lim_{ x \to 1 } \frac{1}{c} = \frac{1}{1} = 1
$$

---
## Ejercicio 4.3.7
$$
\lim_{ x \to 0^{+} } x \log(x)
$$
Aplicando reglas algebraicas:
$$
x \log(x) = \log(x^{x})
$$
Como sabemos que $x \to 0^{+}$, y considerando que cualquier número elevado a 0 es 1:
$$
\lim_{ x \to 0^{+} } x \log(x) = \lim_{ x \to 0^{+} } \log(x^{x}) = \log(0^{0}) = \log(1) = 0
$$
ESTA MAL, SE RESUELVE APLICANDO LA REGLA DE L'HOPITAL


---
# 4.4 - Límites en infinito
## Ejercicio 4.4.2
### Parte d)
#### Parte a)
$$
\lim_{ x \to +\infty } 2x + 3 - (2(x + 5) + 3)
$$
Desarrollamos la función:
$$
2x + 3 - (2(x + 5) + 3) = 2x + 3 - (2x + 13) = \cancel{ 2x } + 3 - \cancel{ 2x } - 13 = -10
$$
De esta forma:
$$
\lim_{ x \to +\infty } 2x + 3 - (2(x + 5) + 3) = -10
$$

#### Parte b)
$$
\lim_{ x \to +\infty } \frac{2x + 3}{(2(x + 5) + 3)}
$$
Desarrollamos la función:
$$
\frac{2x + 3}{(2(x + 5) + 3)} = \frac{2x + 3}{2x + 13}
$$
Considerando las reglas vistas anteriormente con respecto a los grados de los polinomios y los límites, podemos afirmar que:
$$
\lim_{ x \to +\infty } \frac{2x + 3}{(2(x + 5) + 3)} = \lim_{ x \to +\infty } \frac{2x + 3}{2x + 13} = \frac{2}{2} = 1
$$

#### Parte c)
$$
\lim_{ x \to +\infty } (x - 1)^{2} - x^{2}
$$
Desarrollamos la función:
$$
(x - 1)^{2} - x^{2} = \cancel{ x^{2} } - 2x + 1 - \cancel{ x^{2} } = -2x + 1
$$
De esta forma:
$$
\lim_{ x \to +\infty } (x - 1)^{2} - x^{2} = \lim_{ x \to +\infty } -2x + 1 = -\infty
$$

#### Parte e)
$$
\lim_{ x \to +\infty } \frac{x^{3} - 10x - 1}{10x^{2} + 1}
$$
Considerando las propiedades de límites considerando el grado de los polinomios, podemos afirmar que:
$$
\lim_{ x \to +\infty } \frac{x^{3} - 10x - 1}{10x^{2} + 1} = + \infty
$$

#### Parte g)
$$
\lim_{ x \to +\infty } \frac{100x^{2} + x}{x^{3} - 100x}
$$
Intentemos simplificar la función:
$$
\frac{100x^{2} + x}{x^{3} - 100x} = \frac{\cancel{ x^{2} }\left( 100 + \frac{1}{x} \right)}{\cancel{ x^{2} }\left( x - \frac{100}{x} \right)} = \frac{100 + \frac{1}{x}}{x - \frac{100}{x}}
$$
Si analizamos el numerador y denominador por separado:
$$
\begin{align}
&\lim_{ x \to +\infty } 100 + \frac{1}{x} = 100 \\
&\lim_{ x \to +\infty } x - \frac{100}{x} = +\infty
\end{align}
$$
De esta forma, podemos asegurar que:
$$
\lim_{ x \to +\infty } \frac{100x^{2} + x}{x^{3} - 100x} = \lim_{ x \to +\infty } \frac{100 + \frac{1}{x}}{x - \frac{100}{x}} = 0
$$


---
## Ejercicio 4.4.3

Para todos estos ejercicios, tenemos que determinar la existencia del límite cuando $x$ tiene a infinito, y en caso de existir, calcular su valor. Luego, tenemos que despejar la asíntota de la misma, considerando la ecuación:
$$
\begin{align}
&\lim_{ x \to +\infty } f(x) - r(x) = 0 \\
&\lim_{ x \to +\infty } f(x) = r(x)
\end{align}
$$
### Parte a)
$$
f(x) = \frac{1}{x}
$$
$$
\lim_{ x \to + \infty } \frac{1}{x} = 0
$$
De esta forma:
$$
\begin{align}
&\lim_{ x \to + \infty } \frac{1}{x} - r(x) = 0 \\
&0 - r(x) = 0 \\
&r(x) = 0
\end{align}
$$

### Parte e)
$$
f(x) = \frac{\sin(x)}{x}
$$
$$
\lim_{ x \to + \infty } \frac{\sin(x)}{x} = \underbrace{ \lim_{ x \to + \infty } \sin(x) }_{ \text{Acotado entre -1 y 1} } \times \underbrace{ \lim_{ x \to + \infty } \frac{1}{x} }_{ \to 0 } = 0
$$
De esta forma:
$$
\begin{align}
&\lim_{ x \to + \infty } \frac{\sin(x)}{x} - r(x) = 0 \\
&0 - r(x) = 0 \\
&r(x) = 0
\end{align}
$$

### Parte f)
$$
f(x) = \frac{\cos(x) + \sin(x)}{x^{2}}
$$
$$
\lim_{ x \to + \infty } \frac{\cos(x) + \sin(x)}{x^{2}} = \underbrace{ \lim_{ x \to + \infty } \cos(x) + \sin(x) }_{ \text{Acotado entre } \sqrt{ 2 } \text{ y } -\sqrt{ 2 } } \times \underbrace{ \lim_{ x^{2} \to + \infty } \frac{1}{x} }_{ \to 0 } = 0
$$
De esta forma:
$$
\begin{align}
&\lim_{ x \to + \infty } \frac{\cos(x) + \sin(x)}{x^{2}} - r(x) = 0 \\
&0 - r(x) = 0 \\
&r(x) = 0
\end{align}
$$

### Parte g)
$$
f(x) = \frac{x^{3} + x^{2} + x + 1}{2x^{2} + x + 1}
$$
Si intentamos simplificar la expresión:
$$
\frac{x^{3} + x^{2} + x + 1}{2x^{2} + x + 1} = \frac{\cancel{ x^{2} }\left( x + 1 + \frac{1}{x} + \frac{1}{x^{2}} \right)}{\cancel{ x^{2} }\left( 2 + \frac{1}{x} + \frac{1}{x^{2}} \right)} = \frac{x + 1 + \frac{1}{x} + \frac{1}{x^{2}}}{2 + \frac{1}{x} + \frac{1}{x^{2}}}
$$
Ahora, si estudiamos los límites por separado:
$$
\begin{align}
&\lim_{ x \to +\infty } x + 1 + \frac{1}{x} + \frac{1}{x^{2}} = +\infty \\
&\lim_{ x \to +\infty } 2 + \frac{1}{x} + \frac{1}{x^{2}} = 2
\end{align}
$$
Por esta razón:
$$
\lim_{ x \to +\infty } \frac{x^{3} + x^{2} + x + 1}{2x^{2} + x + 1} = \lim_{ x \to +\infty } \frac{\overbrace{ x + 1 + \frac{1}{x} + \frac{1}{x^{2}} }^{ \to +\infty }}{\underbrace{ 2 + \frac{1}{x} + \frac{1}{x^{2}} }_{ \to 2 }} = +\infty
$$

En este caso, la asíntota no es una constante, sino una recta (la cual tendrá la forma $r(x) = mx + n$.
Calcularemos su pendiente y ordenada por separado:
Sabiendo que $r(x) = mx + n$
- Pendiente ($m$):
$$
\lim_{ x \to +\infty } f(x) - mx - n = \lim_{ x \to +\infty } \frac{f(x) - m\cancel{ x } - n}{x} = \lim_{ x \to +\infty } \frac{f(x)}{x} - m - \underbrace{ \frac{n}{x} }_{ \to 0 } \implies m = \lim_{ x \to +\infty } \frac{f(x)}{x}
$$
$$
\lim_{ x \to +\infty } \frac{f(x)}{x} = \lim_{ x \to +\infty } \frac{x^{3} + x^{2} + x + 1}{2x^{3} + x^{2} + x}
$$
Como numerador y denominador tienen mismo grado, su límite a infinito será equivalente a la división entre los coeficientes de mayor grado:
$$
\lim_{ x \to +\infty } \frac{x^{3} + x^{2} + x + 1}{2x^{3} + x^{2} + x} = \frac{\cancel{ x^{3} }}{2\cancel{ x^{3} }} = \frac{1}{2}
$$
De esta forma: $m = \frac{1}{2}$

- Ordenada ($n$):
$$
\lim_{ x \to +\infty } f(x) - mx - n \implies n = \lim_{ x \to +\infty } f(x) - mx = \lim_{ x \to +\infty } f(x) - \frac{1}{2}x
$$
Ahora, calcularemos el límite de $f(x) - \frac{1}{2}x$ cuando $x \to +\infty$:
$$
\lim_{ x \to +\infty } f(x) - \frac{1}{2}x = \lim_{ x \to +\infty } \frac{x^{3} + x^{2} + x + 1}{2x^{2} + x + 1} - \frac{1}{2}x = \lim_{ x \to +\infty } \frac{x^{3} + x^{2} + x + 1}{2x^{2} + x + 1} - \frac{\frac{1}{2}x(2x^{2} + x + 1)}{2x^{2} + x + 1}
$$
$$
\frac{x^{3} + x^{2} + x + 1}{2x^{2} + x + 1} - \frac{\frac{1}{2}x(2x^{2} + x + 1)}{2x^{2} + x + 1} = \frac{x^{3} + x^{2} + x + 1}{2x^{2} + x + 1} - \frac{x^{3} + \frac{1}{2}x^{2} + \frac{1}{2}x}{2x^{2} + x + 1} = \frac{\frac{1}{2}x^{2} + \frac{1}{2}x + 1}{2x^{2} + x + 1}
$$
$$
\lim_{ x \to +\infty } f(x) - \frac{1}{2}x = \lim_{ x \to +\infty } \frac{\frac{1}{2}x^{2} + \frac{1}{2}x + 1}{2x^{2} + x + 1} = \frac{\frac{1}{2}\cancel{ x^{2} }}{2\cancel{ x^{2} }} = \frac{1}{4}
$$
De esta forma: $n = \frac{1}{4}$

En conclusión:
$$
r(x) = \frac{1}{2}x + \frac{1}{4}
$$

### Parte h)
$$
f(x) = \frac{x^{2} + 1}{3x - 1}
$$
Simplificamos la expresión:
$$
\frac{x^{2} + 1}{3x - 1} = \frac{\cancel{ x }\left( x + \frac{1}{x} \right)}{\cancel{ x }\left( 3 - \frac{1}{x} \right)} = \frac{x + \frac{1}{x}}{3 - \frac{1}{x}}
$$
Ahora, estudiamos los límites por separado:
$$
\begin{align}
&\lim_{ x \to +\infty } x + \frac{1}{x} = +\infty \\
&\lim_{ x \to +\infty } 3 - \frac{1}{x} = 3
\end{align}
$$
Por esta razón:
$$
\lim_{ x \to +\infty } \frac{x^{2} + 1}{3x - 1} = \lim_{ x \to +\infty } \frac{\overbrace{ x + \frac{1}{x} }^{ \to +\infty }}{\underbrace{ 3 - \frac{1}{x} }_{ \to 3 }} = +\infty
$$

En este caso, la asíntota no es una constante, sino una recta.
Calcularemos su pendiente y ordenada por separado:
Sabiendo que $r(x) = mx + n$
- Pendiente ($m$):
$$
\lim_{ x \to +\infty } \frac{f(x)}{x} = \lim_{ x \to +\infty } \frac{x^{2} + 1}{3x^{2} - x}
$$
Como numerador y denominador tienen mismo grado, su límite a infinito será equivalente a la división entre los coeficientes de mayor grado:
$$
\lim_{ x \to +\infty } \frac{x^{2} + 1}{3x^{2} - x} = \frac{\cancel{ x^{2} }}{3\cancel{ x^{2} }} = \frac{1}{3}
$$
De esta forma: $m = \frac{1}{3}$

- Ordenada ($n$):
Ahora, calcularemos el límite de $f(x) - \frac{1}{3}x$ cuando $x \to +\infty$:
$$
\lim_{ x \to +\infty } f(x) - \frac{1}{3}x = \lim_{ x \to +\infty } \frac{x^{2} + 1}{3x - 1} - \frac{1}{3}x = \lim_{ x \to +\infty } \frac{x^{2} + 1}{3x - 1} - \frac{\frac{1}{3}x(3x - 1)}{3x - 1}
$$
$$
\frac{x^{2} + 1}{3x - 1} - \frac{\frac{1}{3}x(3x - 1)}{3x - 1} = \frac{x^{2} + 1}{3x - 1} - \frac{x^{2} - \frac{1}{3}x}{3x - 1} = \frac{\frac{1}{3}x + 1}{3x - 1}
$$
$$
\lim_{ x \to +\infty } f(x) - \frac{1}{2}x = \lim_{ x \to +\infty } \frac{\frac{1}{3}x + 1}{3x - 1} = \frac{\frac{1}{3}\cancel{ x }}{3\cancel{ x }} = \frac{1}{9}
$$
De esta forma: $n = \frac{1}{9}$

En conclusión:
$$
r(x) = \frac{1}{3}x + \frac{1}{9}
$$

---
## Ejercicio 4.4.6
Podemos pensar en algo que oscile infinitamente cuando tiende a $+ \infty$. Tenemos que pensar en funciones que se "desestabilicen" mientras mayor es el valor de $x$.
Por ejemplo, podemos considerar algo como:
$$
f(x) = \frac{\sin(x^{2}) + 1}{3} \text{ o } f(x) = \frac{\sin(2^{x}) + 1}{3}
$$
En este caso, si bien el conjunto imagen es $\left[ 0, \frac{2}{3} \right]$, es imposible determinar el límite cuando $x \to +\infty$ ya que la función oscila cada vez más violentamente a medida que aumenta el valor de $x$.

Ahora, si analizamos la función $\lfloor f(x) \rfloor$, podemos ver que, como el conjunto imagen es $\left[ 0, \frac{2}{3} \right]$, $\lfloor f(x) \rfloor = 0$. En conclusión:
$\lim_{ x \to +\infty } f(x)$ no existe, pero
$$
\lim_{ x \to +\infty } \lfloor f(x) \rfloor = 0
$$

Analizamos el caso contrario:

Podemos considerar una función que oscile cuando $x \to +\infty$, pero que esté cada vez más cerca de 0:
$$
f(x) = \frac{\sin(x^{2})}{x} \text{ o } f(x) = \frac{\sin(2^{x})}{x}
$$
En este caso, la oscilación se va haciendo cada vez más pequeña a medida que aumenta el valor de $x$, por lo que podemos determinar con seguridad que:
$$
\lim_{ x \to +\infty } f(x) = 0
$$

Sin embargo, no podemos decir lo mismo de $\lfloor f(x) \rfloor$, ya que, como la función oscila rápidamente alrededor de 0, cambia de signo constantemente. Por lo tanto:
$\lim_{ x \to +\infty } \lfloor f(x) \rfloor$ no existe, pero
$$
\lim_{ x \to +\infty } f(x) = 0
$$

---
## Ejercicio 4.4.7
### Parte a)
$$
\lim_{ x \to +\infty } \lfloor x + 1 \rfloor - \lfloor x \rfloor
$$
Podemos intentar descomponer la función, sin cambiar el resultado obtenido:
$$
\lim_{ x \to +\infty } \lfloor x + 1 \rfloor - \lfloor x \rfloor = \lim_{ x \to +\infty } \cancel{ \lfloor x \rfloor } + 1 - \cancel{ \lfloor x \rfloor } = 1
$$

### Parte d)
$$
\lim_{ x \to +\infty } \lfloor 2x \rfloor - \lfloor x \rfloor
$$
Aquí hay que analizar un poco más la función, ya que hay dos casos:
1. La parte decimal de $x$ es menor a $\frac{1}{2}$:
   $$
\lfloor 2x \rfloor - \lfloor x \rfloor = \lfloor x \rfloor \implies \lim_{ x \to +\infty } \lfloor 2x \rfloor - \lfloor x \rfloor = +\infty
   $$
2. La parte decimal de $x$ es mayor o igual a $\frac{1}{2}$:
   $$
\lfloor 2x \rfloor - \lfloor x \rfloor = \lfloor x \rfloor + 1 \implies \lim_{ x \to +\infty } \lfloor 2x \rfloor - \lfloor x \rfloor = +\infty
   $$

En cualquiera de los dos casos:
$$
\lim_{ x \to +\infty } \lfloor 2x \rfloor - \lfloor x \rfloor = +\infty
$$

### Parte f)
$$
\lim_{ x \to +\infty } 2x - \lfloor 2x \rfloor
$$
Aquí, hay que entender como se comporta la función:
1. Si la parte decimal es 0:
$$
2x - \lfloor 2x \rfloor = 0
$$
2. Si la parte decimal es menor a $\frac{1}{2}$:
$$
2x - \lfloor 2x \rfloor = \text{parte decimal de } 2x (\in (0, 1))
$$
3. Si la parte decimal es mayor o igual a $\frac{1}{2}$:
$$
2x - \lfloor 2x \rfloor = \text{parte decimal de } 2x (\in [0, 1))
$$

De esta forma, sabemos que la imagen de la función está acotada, dentro del intervalo $[0, 1)$, pero por la forma de la función, la misma no tiene límite cuando $x \to +\infty$:
$$
\text{No existe } \lim_{ x \to +\infty } 2x - \lfloor 2x \rfloor
$$

---
## Ejercicio 4.4.8
### Parte a)
$$
\lim_{ x \to +\infty } \frac{\sin(x)}{x}
$$
Si analizamos el numerador y denominador por separado, podemos ver que:
$$
\begin{align}
&\lim_{ x \to +\infty } \sin(x) \text{ no existe } (\text{la función está acotada en el intervalo } [-1, 1]) \\
&\lim_{ x \to +\infty } x = +\infty
\end{align}
$$
De esta forma, como tenemos una función acotada, dividida por otra que tiende a infinito (no acotada), podemos concluir que:
$$
\lim_{ x \to +\infty } \frac{\sin(x)}{x} = 0
$$

### Parte d)
$$
\lim_{ x \to +\infty } \frac{x}{\sqrt{ x^{2} + x + 1 }}
$$
Si analizamos los límites por separado:
$$
\begin{align}
&\lim_{ x \to +\infty } x = +\infty \\
&\lim_{ x \to +\infty } \sqrt{ x^{2} + x + 1 } = +\infty
\end{align}
$$
De esta forma, nos encontramos ante una indeterminación de tipo $\frac{\infty}{\infty}$. Probemos multiplicar por el denominador:
$$
\frac{x}{\sqrt{ x^{2} + x + 1 }} = \frac{x}{\sqrt{ x^{2}\left( 1 + \frac{1}{x} + \frac{1}{x^{2}} \right) }} = \frac{x}{\sqrt{ x^{2} }\sqrt{ 1 + \frac{1}{x} + \frac{1}{x^{2}} }} = \frac{\cancel{ x }}{\cancel{ x }\sqrt{ 1 + \frac{1}{x} + \frac{1}{x^{2}} }} = \frac{1}{\sqrt{ 1 + \frac{1}{x} + \frac{1}{x^{2}} }}
$$
Ahora, podemos estudiar por separado los límites de:
$$
\begin{align}
&\lim_{ x \to +\infty } 1 = 1 \\
&\lim_{ x \to +\infty } \sqrt{ 1 + \frac{1}{x} + \frac{1}{x^{2}} } = 1
\end{align}
$$
En conclusión:
$$
\lim_{ x \to +\infty } \frac{x}{\sqrt{ x^{2} + x + 1 }} = \lim_{ x \to +\infty } \frac{1}{\sqrt{ 1 + \frac{1}{x} + \frac{1}{x^{2}} }} = \frac{1}{1} = 1
$$

### Parte f)
$$
\lim_{ x \to +\infty } \frac{\frac{1}{x} - \frac{1}{x^{2}}}{\frac{1}{x^{3}} - \frac{1}{x^{2}}}
$$
Simplificamos la expresión:
$$
\frac{\frac{1}{x} - \frac{1}{x^{2}}}{\frac{1}{x^{3}} - \frac{1}{x^{2}}} = \frac{x^{2}\left( \frac{1}{x} - \frac{1}{x^{2}} \right)}{x^{2}\left( \frac{1}{x^{3}} - \frac{1}{x^{2}} \right)} = \frac{ \frac{x\cancel{ ^{2} }}{\cancel{ x }} - \frac{\cancel{ x^{2} }}{\cancel{ x^{2} }} }{ \frac{\cancel{ x^{2} }}{x\cancel{ ^{3} }} - \frac{\cancel{ x^{2} }}{\cancel{ x^{2} }} } = \frac{x - 1}{\frac{1}{x} - 1}
$$
Ahora, si analizamos al numerador y denominador por separado:
$$
\begin{align}
&\lim_{ x \to +\infty }  x - 1 = +\infty \\
&\lim_{ x \to +\infty }  \frac{1}{x} - 1 = -1
\end{align}
$$
En conclusión:
$$
\lim_{ x \to +\infty } \frac{\frac{1}{x} - \frac{1}{x^{2}}}{\frac{1}{x^{3}} - \frac{1}{x^{2}}} = \lim_{ x \to +\infty } \frac{x - 1}{\frac{1}{x} - 1} = \frac{+\infty}{-1} = -\infty
$$

---
## Ejercicio 4.4.9
### Parte a)
$$
\lim_{ x \to +\infty } x - \sqrt{ x^{2} + x }
$$
Descomponemos la función:
$$
x - \sqrt{ x^{2} + x } = x - \sqrt{ x^{2}\left( 1 + \frac{1}{x} \right) } = x - \sqrt{ x^{2} }\sqrt{ 1 + \frac{1}{x} } = x - x\sqrt{ 1 + \frac{1}{x} }
$$
Ahora, analizamos los límites de cada término:
$$
\begin{align}
&\lim_{ x \to +\infty } x = +\infty \\
&\lim_{ x \to +\infty } x\sqrt{ 1 + \frac{1}{x} } = \underbrace{ \lim_{ x \to +\infty } x }_{ \to +\infty } \times \underbrace{ \lim_{ x \to +\infty } \sqrt{ 1 + \frac{1}{x} } }_{ \to 1 } = \lim_{ x \to +\infty } x = +\infty
\end{align}
$$
Como $\sqrt{ 1 + \frac{1}{x} } \to 1$ cuando $x \to +\infty$, podemos concluir que:
$$
\lim_{ x \to +\infty } x - \sqrt{ x^{2} + x } = \lim_{ x \to +\infty } x - x\sqrt{ 1 + \frac{1}{x} } = \lim_{ x \to +\infty } x - x = 0
$$
INCORRECTO: A CONTINUACIÓN LO RESOLVEMOS CORRECTAMENTE UTILIZANDO EL CONJUGADO.

Desarrollamos la función utilizando el conjugado:
$$
x - \sqrt{ x^{2} + x } = \frac{(x - \sqrt{ x^{2} + x })(x + \sqrt{ x^{2} + x })}{x + \sqrt{ x^{2} + x }} = \frac{\cancel{ x^{2} } - (\cancel{ x^{2} } + x)}{x + \sqrt{ x^{2} + x }} = \frac{-x}{x + \sqrt{ x^{2} + x }}
$$
Ahora, estudiamos el denominador:
$$
x + \sqrt{ x^{2} + x } = x + \sqrt{ x^{2}\left( 1 + \frac{1}{x} \right) } = x + \sqrt{ x^{2} }\sqrt{ 1 + \frac{1}{x} } = x + x\sqrt{ 1 + \frac{1}{x} } = x\left( 1 + \sqrt{ 1 + \frac{1}{x} } \right)
$$
Volvemos a considerar la expresión completa:
$$
\frac{-x}{x + \sqrt{ x^{2} + x }} = -\frac{\cancel{ x }}{\cancel{ x }\left( 1 + \sqrt{ 1 + \frac{1}{x} } \right)} = -\frac{1}{1 + \sqrt{ 1 + \frac{1}{x} }}
$$
Finalmente, estudiamos los límites:
$$
\lim_{ x \to +\infty } x - \sqrt{ x^{2} + x } = \lim_{ x \to +\infty } -\frac{\overbrace{ 1 }^{ \to 1 }}{\underbrace{ 1 }_{ \to 1 } + \underbrace{ \sqrt{ 1 + \frac{1}{x} } }_{ \to 1 }} = -\frac{1}{2}
$$



### Parte d)
$$
\lim_{ x \to +\infty } \sin(x + 1) - \sin(x)
$$
En este caso, simplemente basta con entender que $\sin(x + 1)$ y $\sin(x)$ son funciones cuyo comportamiento no cambia en base al tramo estudiado (no varían según que tan grande es el valor de $x$), sea cual sea el trozo de su recorrido analizado. Además, ambas funciones están acotadas en los intervalo $[-1, 1]$. Sin embargo, por el primer punto mencionado, podemos afirmar que:
$$
\lim_{ x \to +\infty } \sin(x + 1) - \sin(x) = \underbrace{ \lim_{ x \to +\infty } \sin(x + 1) }_{ \text{No existe} } - \underbrace{ \lim_{ x \to +\infty } \sin(x) }_{ \text{No existe} } \implies \lim_{ x \to +\infty } \sin(x + 1) - \sin(x) \text{ no existe}
$$
ACLARACIÓN: LA FORMA CORRECTA DE EXPRESAR LA IDEA DE QUE LA FUNCIÓN "NO VARÍA SEGÚN EL TRAMO ANALIZADO" ES QUE LA FUNCIÓN OSCILA SIN REDUCIR SU AMPLITUD, POR LO QUE EL LÍMITE NUNCA EXISTE (A NO SER QUE SE ESTUDIE EL LÍMITE PARA UN VALOR PUNTUAL DE $x$).

### Parte e)
$$
\lim_{ x \to +\infty } \log(x + 1) - \log(x)
$$
Aplicando propiedades de $\log$:
$$
\log(x + 1) - \log(x) = \log\left( \frac{x + 1}{x} \right) = \log\left( \frac{\cancel{ x }\left( 1 + \frac{1}{x} \right)}{\cancel{ x }} \right) = \log\left( 1 + \frac{1}{x} \right)
$$
En conclusión:
$$
\lim_{ x \to +\infty } \log(x + 1) - \log(x) = \log\left( \underbrace{ 1 }_{ \to 1 } + \underbrace{ \frac{1}{x} }_{ \to 0 } \right) = \log(1) = 0
$$

# 4.5 - Continuidad
## Ejercicio 4.5.1
Importante: como sabemos que las funciones son continuas, podemos suponer que:
$$
\begin{align}
&\lim_{ x \to a } f(x) = f(a) \\
&\lim_{ x \to a } g(x) = g(a)
\end{align}
$$
Además, la continuidad se mantiene para la suma, resta, producto, y división (si no se anula el divisor) de dichas funciones. Esto también incluye a la composición: la composición de funciones continuas es continua.

### Parte a)
$$
\lim_{ x \to 5 } f(x - 2) + g(x + 2)
$$
Consideremos $x = 5$ para determinar las imágenes:
$$
\begin{align}
&f(5 - 2) = f(3) = 4 \\
&g(5 + 2) = g(7) = 2
\end{align}
$$
En conclusión:
$$
\lim_{ x \to 5 } f(x - 2) + g(x + 2) = f(5 - 2) + g(5 + 2) = f(3) + g(7) = 4 + 2 = 6
$$

### Parte b)
$$
\lim_{ x \to 1 } f(g(x)) - g(f(x))
$$
Consideremos $x = 1$ para determinar las imágenes:
$$
\begin{align}
&g(1) = 3 \implies f(g(1)) = f(3) = 4 \\
&f(1) = 2 \implies g(f(1)) = g(2) = 1
\end{align}
$$
En conclusión:
$$
\lim_{ x \to 1 } f(g(x)) - g(f(x)) = f(g(1)) - g(f(1)) = f(3) - g(2) = 4 - 1 = 3
$$

### Parte c)
$$
\lim_{ x \to 1 } f(g(x) + 1) - 2g(x + 2)
$$
Consideremos $x = 1$ para determinar las imágenes:
$$
\begin{align}
&g(1) = 3 \implies f(g(1) + 1) = f(3 + 1) = f(4) = 0 \\
&g(1 + 2) = g(3) = 0
\end{align}
$$
En conclusión:
$$
\lim_{ x \to 1 } f(g(x) + 1) - 2g(x + 2) = f(g(1) + 1) - 2g(1 + 2) = f(3 + 1) - 2g(1 + 2) = f(4) - 2g(3) = 0 - 2 \times 0 = 0
$$

### Parte d)
$$
\lim_{ x \to 1 } g(f(x) + 1) - 2f(x + 2)
$$
Consideremos $x = 1$ para determinar las imágenes:
$$
\begin{align}
&f(1) = 2 \implies g(f(1) + 1) = g(2 + 1) = g(3) = 0 \\
&f(1 + 2) = f(3) = 4
\end{align}
$$
En conclusión:
$$
\lim_{ x \to 1 } g(f(x) + 1) - 2f(x + 2) = g(f(1) + 1) - 2f(1 + 2) = g(2 + 1) - 2f(1 + 2) = g(3) - 2f(3) = 0 - 2 \times 4 = -8
$$

---
## Ejercicio 4.5.2
Para trabajar en este ejercicio, tenemos que entender que una función es continua en un punto $a$, cuando:
$$
\lim_{ x \to a } f(x) = f(a)
$$
O lo que es lo mismo
$$
\forall \epsilon > 0, \exists \delta > 0, \forall x \in I, 0 < |x - x_{0}| < \delta \implies |f(x) - f(x_{0})| < \epsilon
$$
### Parte b)
Si analizamos la función y su comportamiento, podemos ver que se trata de una función escalonada, la cual "salta" cada vez que $x$ alcanza un valor entero.

Vamos a demostrar esto formalmente:
Podemos distinguir dos casos para la función $f(x) = \lfloor x \rfloor = max(n \leq x), n \in \mathbb{Z}$.
1. $a \not \in \mathbb{Z}$
$$
\lim_{ x \to a } \lfloor x \rfloor = \lfloor a \rfloor 
$$

Sea $\epsilon > 0$
$$
\begin{align}
&|f(x) - L| < \epsilon \\
&|\lfloor x \rfloor - \lfloor a \rfloor | < \epsilon
\end{align}
$$
Como $x \to a$ y $a \not \in \mathbb{Z}$:
$$
\lfloor x \rfloor = \lfloor a \rfloor \implies \lfloor x \rfloor - \lfloor a \rfloor = 0
$$
Pasando a $\delta$:
$$
0 < |x - a| < \delta
$$
Podemos determinar un $\delta$ válido sabiendo que no podemos alcanzar ningún valor entero. De esta forma, $\delta \in (0, min(|max(n \leq a) - a|, |min(n \geq a) - a|))$ con $n \in \mathbb{Z}$.

Es así que podemos considerar $\delta = min(|max(n \leq a) - a|, |min(n \geq a) - a|)$.

Entonces, encontramos un $\delta$ para el cual $|x - a| < \delta$, lo que implica que $|f(x) - L| < \epsilon$

De esta forma, la función $\lfloor x \rfloor$ es continua si estudiamos valores no enteros.

2. $a \in \mathbb{Z}$
$$
\lim_{ x \to a } \lfloor x \rfloor = \text{?}
$$
$$
\begin{align}
&\lim_{ x \to a^{-} } \lfloor x \rfloor = a - 1 \\
&\lim_{ x \to a^{+} } \lfloor x \rfloor = a
\end{align}
$$
Por esta razón, el límite en la función $\lfloor x \rfloor$ no existe si $x \in \mathbb{Z}$, por lo que la función no es continua en este caso.

En conclusión, la función $\lfloor x \rfloor$ únicamente es continua para todo $x \not \in \mathbb{Z}$.

### Parte d)
Tenemos que determinar para que valores de $a$ se cumple que:
$$
\lim_{ x \to a^{+} } \sqrt{ x - \lfloor x \rfloor } = \lim_{ x \to a^{-} } \sqrt{ x - \lfloor x \rfloor } \text{ y } \lim_{ x \to a } \sqrt{ x - \lfloor x \rfloor } = \sqrt{ a - \lfloor a \rfloor }
$$

En este caso, conviene analizar que es lo que sucede dentro de la raíz cuadrada. Aquí tenemos nuevamente dos casos diferentes:
1. $a \not \in \mathbb{Z}$
$$
\begin{align}
&\lim_{ x \to a^{-} } \sqrt{ x - \lfloor x \rfloor } = \sqrt{ a - \lfloor a \rfloor } \\
&\lim_{ x \to a^{-} } \sqrt{ x - \lfloor x \rfloor } = \sqrt{ a - \lfloor a \rfloor }
\end{align}
$$
En ambos casos, $\lfloor a \rfloor < a$ y en ambos límites $\lfloor a \rfloor$ son iguales, por lo tanto:
$$
\lim_{ x \to a^{-} } \sqrt{ x - \lfloor x \rfloor } = \lim_{ x \to a^{+} } \sqrt{ x - \lfloor x \rfloor }
$$

Ya que $a \not \in \mathbb{Z}$, podemos asegurar que existe un entorno alrededor de $a$, para el cual para todo $x$ en dicho entorno, se cumple que $\lfloor x \rfloor = \lfloor a \rfloor$. Por esta razón, la función (en la región planteada) se comporta como:
$$
f(x) = \sqrt{ x - \lfloor a \rfloor  }
$$
De esta forma, podemos considerar un $\delta$ inicial, con la idea de que $\lfloor x \rfloor$ no cambie de valor:
$$
\delta_{1} = min(a - \lfloor a \rfloor, \lfloor a \rfloor + 1 - a )
$$

Sea $\epsilon > 0$
$$
\begin{align}
&|f(x) - L| < \epsilon \\
&\left| \sqrt{ x - \lfloor x \rfloor } - \sqrt{ a - \lfloor a \rfloor } \right| < \epsilon \\
&\left| \sqrt{ x - \lfloor x \rfloor } - \sqrt{ a - \lfloor a \rfloor } \right|  \left| \sqrt{ x - \lfloor x \rfloor } + \sqrt{ a - \lfloor a \rfloor } \right| < \epsilon \left| \sqrt{ x - \lfloor x \rfloor } + \sqrt{ a - \lfloor a \rfloor } \right| \\
&\left| x - \lfloor x \rfloor - a + \lfloor a \rfloor \right| < \epsilon \left| \sqrt{ x - \lfloor x \rfloor } + \sqrt{ a - \lfloor a \rfloor } \right| \\
&| x - a | < \epsilon \left| \sqrt{ x - \lfloor x \rfloor } + \sqrt{ a - \lfloor a \rfloor } \right| \qquad \text{considerando que } \lfloor x \rfloor = \lfloor a \rfloor \\
&\frac{| x - a |}{\left| \sqrt{ x - \lfloor x \rfloor } + \sqrt{ a - \lfloor a \rfloor } \right|} < \epsilon
\end{align}
$$

Como $a \not \in \mathbb{Z}$, sabemos que $a - \lfloor a \rfloor > 0$, por lo tanto, el denominador es mayor o igual a una constante positiva:
$$
\sqrt{ x - \lfloor a \rfloor } + \sqrt{ a - \lfloor a \rfloor } \geq \sqrt{ a - \lfloor a \rfloor }
$$
Ahora, podemos aplicar esta cota inferior al denominador, obteniendo una cota superior para la fracción y determinando un $\delta$ más ajustado:
$$
\frac{| x - a |}{\sqrt{ x - \lfloor x \rfloor } + \sqrt{ a - \lfloor a \rfloor }} \leq \frac{|x - a|}{\sqrt{ a - \sqrt{ a } }} < \epsilon
$$
Entonces, podemos tomar $|x - a| < \epsilon \sqrt{ a - \lfloor a \rfloor }$.

En conclusión, el $\delta$ final será el mínimo entre la restricción del entorno inicial y este nuevo valor:
$$
\delta = min \left( a - \lfloor a \rfloor, \lfloor a \rfloor + 1 - a, \epsilon \sqrt{ a - \lfloor a \rfloor  } \right)
$$
De esta forma, para cualquier $\epsilon > 0$, logramos determinar un $\delta > 0$, tal que la función es continua en todo $a \not \in \mathbb{Z}$.

2. $a \in \mathbb{Z}$
En este caso:
$$
a - \lfloor a \rfloor 0 \implies f(a) = 0
$$
Además, si estudiamos los límites por izquierda y por derecha:
$$
\begin{align}
&\lim_{ x \to a^{-} } \sqrt{ a - \lfloor a \rfloor } \simeq \sqrt{ \cancel{ a } - (\cancel{ a } - 1) } = \sqrt{ 1 } = 1 \\
&\lim_{ x \to a^{-} } \sqrt{ a - \lfloor a \rfloor } \simeq \sqrt{ \cancel{ a } - \cancel{ a } } = \sqrt{ 0 } = 0
\end{align}
$$
Como vemos, los límites por izquierda y por derecha no coinciden.

En conclusión, la función $\sqrt{ x - \lfloor x \rfloor }$ es continua únicamente para $x \not \in \mathbb{Z}$.

---
## Ejercicio 4.5.3
### Parte a)
$$
f(x) = \begin{cases}
\begin{align}
&x^{2} + 3x + 2 &&\text{si } x \leq 1  \\
&ax^{2} + bx + 1 &&\text{si } x > 1
\end{align}
\end{cases}
$$
$$
\lim_{ x \to 1 } x^{2} + 3x + 2 = 1^{2} + 3 \times 1 + 2 = 1 + 3 + 2 = 6
$$
Entonces, tenemos que encontrar valores de $a$ y $b$ para los cuales:
$$
\lim_{ x \to 1 } ax^{2} + bx + 1 = 6
$$
De esta forma:
$$
\begin{align}
&ax^{2} + bx + 1 = 6 \\
&ax^{2} + bx = 5
\end{align}
$$
Además, sabiendo que $x \to 1$:
$$
a + b = 5
$$
En conclusión:
$$
\begin{align}
&a = 5 - b \\
&b = 5 - a
\end{align}
$$
### Parte b)
$$
f(x) = \begin{cases}
\begin{align}
&\log(x + 1) &&\text{si } x > 0  \\
&(x + a)^{2} &&\text{si } x \leq 0
\end{align}
\end{cases}
$$
$$
\lim_{ x \to 0 } \log(x + 1) = \log(0 + 1) = \log(1) = 0
$$
Entonces, tenemos que encontrar valores de $a$ para los cuales:
$$
\lim_{ x \to 0 } (x + a)^{2} = 0
$$
$$
(x + a)^{2} = (x + a)(x + a)
$$
Para que $(x + a)(x + a) = 0$, $a = -x$

Entonces, podemos determinar que:
$$
\lim_{ x \to 0 } (x + a)^{2} = (0 + a)^{2} = a^{2}
$$
En conclusión:
$$
\lim_{ x \to 0 } (x + a)^{2} = 0 \text{ y } a = -x \implies a = 0
$$

### Parte c)
$$
f(x) = \begin{cases}
\begin{align}
&\sin (\pi x) &&\text{si } x < 1 \\
&ax + b &&\text{si } 1 \leq x \leq 2 \\
&x^{2} &&\text{si } x > 2
\end{align}
\end{cases}
$$
Tenemos que determinar:
$$
\begin{align}
&\lim_{ x \to 1 } \sin (\pi x) = \lim_{ x \to 1 } ax + b \\
&\lim_{ x \to 2 } ax + b = \lim_{ x \to 2 } x^{2}
\end{align}
$$
$$
\lim_{ x \to 1 } \sin (\pi x) = \sin (\pi) = 0
$$
De esta forma:
$$
\lim_{ x \to 1 } ax + b = 0 \implies a + b = 0
$$
Tenemos la primer ecuación:
$$
a + b = 0
$$
Proseguimos:
$$
\lim_{ x \to 2 } x^{2} = 2^{2} = 4
$$
De esta forma:
$$
\lim_{ x \to 2 } ax + b = 4 \implies 2a + b = 4
$$
Tenemos la segunda ecuación:
$$
2a + b = 4
$$

Ahora, tenemos que resolver el sistema que incluye a las dos ecuaciones anteriores:
$$
\begin{cases}
a + b = 0 \\
2a + b = 4
\end{cases}
$$
$$
\left(
\begin{array}{cc|c}
1 & 1 & 0 \\
2 & 1 & 4
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|c}
1 & 1 & 0 \\
1 & 0 & 4
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
0 & 1 & -4 \\
1 & 0 & 4
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
1 & 0 & 4 \\
0 & 1 & -4
\end{array}
\right)
\begin{align}
&F_{1} \longleftrightarrow F_{2}
\end{align}
$$
En conclusión, para que $f$ sea continua:
$$
\begin{align}
&a = 4 \\
&b = -4
\end{align}
$$

### Parte e)
$$
f(x) = \begin{cases}
\begin{align}
&2 \cos (x) &&\text{si } x \leq \pi \\
&ax^{2} + b &&\text{si } x > \pi
\end{align}
\end{cases}
$$
Para que $f$ sea continua, tiene que cumplirse que:
$$
\lim_{ x \to \pi } 2 \cos(x) = \lim_{ x \to \pi } ax^{2} + b
$$
$$
\lim_{ x \to \pi } 2 \cos(x) = 2 \times \cos(\pi) = 2 \times (-1) = -2
$$
Entonces:
$$
\lim_{ x \to \pi } ax^{2} + b = -2 \implies a \pi^{2} + b = -2
$$
$$
a \pi^{2} + b = -2
$$
De esta forma:
$$
\begin{align}
&a = \frac{-2 - b}{\pi^{2}} \\
&b = -2 - a\pi^{2}
\end{align}
$$




---
## Ejercicio 4.5.4
### Parte a)
$$
\lim_{ x \to 0 } \frac{\overbrace{ \sin (2x) }^{ \to 0 }}{\underbrace{ 3x }_{ \to 0 }} = \frac{0}{0}
$$
Para resolver este límite, necesitamos aplicar el límite trigonométrico fundamental:
$$
\lim_{ x \to 0 } \frac{\sin(u)}{u} = 1
$$
Entonces, tenemos que despejar un factor con la forma anterior a partir de la función propuesta.
$$
\lim_{ x \to 0 } \frac{\sin (2x)}{3x} = \lim_{ x \to 0 } \frac{\sin(2x)}{2x} \times \frac{2}{3} = \lim_{ x \to 0 } \frac{\sin(2x)}{2x} \times \lim_{ x \to 0 } \frac{2}{3}
$$
Ahora, si analizamos cada uno por separado:
$$
\begin{align}
&\lim_{ x \to 0 } \frac{\sin(2x)}{2x} = 1 \\
&\lim_{ x \to 0 } \frac{2}{3} = \frac{2}{3}
\end{align}
$$

En conclusión:
$$
\lim_{ x \to 0 } \frac{\sin (2x)}{3x} = \lim_{ x \to 0 } \frac{\sin(2x)}{2x} \times \lim_{ x \to 0 } \frac{2}{3} = 1 \times \frac{2}{3} = \frac{2}{3}
$$

### Parte c)
$$
\lim_{ x \to 1 } \frac{\overbrace{ \log(\sqrt{ x }) }^{ \to 0 }}{\underbrace{ 2x - 4 }_{ \to -2 }} = \frac{0}{-2} = 0
$$
En este caso no obtuvimos una indeterminación, por lo que el límite es 0 cuando $x \to 1$.


---
# 4.7 - Complementarios
## Ejercicio 4.7.1
Para determinar un límite para un cociente de polinomios, lo primero que tenemos que hacer es revisar el tipo de límite:

1. Si es un límite finito:
Al sustituir $x$ por el valor del límite, puede pasar que:
	1. El denominador no se anule: Se opera con normalidad y se obtiene un límite finito.
	2. El denominador se anule: Aquí pueden pasar dos cosas:
		1. El numerador no es nulo: El límite será siempre infinito ($\pm \infty$).
		2. El numerador es nulo: Se trata de una indeterminación $\frac{0}{0}$. Por esta razón, hay que estudiar la multiplicidad de la raíz $a$ en cada polinomio (cuantas veces se puede descomponer cada polinomio en $(x - a)$). Lo que sucede aquí es que se comienzan a anular factores que se encuentran tanto en el numerador como en el denominador:
			1. Si se cancela por completo el numerador, el límite es 0.
			2. Si se cancela por completo el denominador, el límite es infinito ($\pm \infty$).
			3. Si no se cancela por completo ninguno, el límite es una constante no nula, resultado de calcular el cociente entre ambos polinomios nuevamente.

2. Si es un límite a infinito:
Consideramos únicamente los términos de mayor grado del numerador y el denominador.
	1. Si el numerador es de mayor grado que el denominador: el resultado será infinito (positivo o negativo dependiendo de los signos del numerador y el denominador).
	2. Si el denominador es de mayor grado que el numerador: el resultado será 0.
	3. Si numerador y denominador son de mismo grado: el resultado estará dado por el cociente de los coeficientes de cada termino.


