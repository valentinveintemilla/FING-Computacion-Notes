# 1 - Cálculos elementales
## Ejercicio 6.1.1
Recordemos la definición de derivada en un punto $x_{0}$:
$$
f'(x_{0}) = \lim_{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}}
$$
O, considerando un punto de vista alternativo:
$$
f'(x_{0}) = \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0}) }{h}
$$
Siendo $h = x - x_{0}$
### Parte a)
$$
f'(x_{0}) = \frac{x^{2} - x_{0}^{2}}{x - x_{0}} = \frac{(x + x_{0})\cancel{ (x - x_{0}) }}{\cancel{ x - x_{0} }} = x + x_{0}
$$
De esta forma, y sabiendo que $x \to x_{0}$:
$$
f'(x_{0}) = x + x_{0} = 2x_{0} \implies f'(x) = 2x
$$
### Parte b)
$$
f'(x_{0}) = \frac{x^{3} - x_{0}^{3}}{x - x_{0}} = \frac{\cancel{ (x - x_{0}) }(x^{2} + xx_{0} + x_{0}^{2})}{\cancel{ x - x_{0} }} = x^{2} + xx_{0} + x_{0}^{2}
$$
De esta forma, y sabiendo que $x \to x_{0}$:
$$
f'(x_{0}) = x^{2} + xx_{0} + x_{0}^{2} = 3x_{0}^{2} \implies f'(x) = 3x^{2}
$$

### Parte c)
$$
f'(x_{0}) = \frac{\sqrt{ x } - \sqrt{ x_{0} }}{x - x_{0}} = \frac{(\sqrt{ x } - \sqrt{ x_{0} })(\sqrt{ x } + \sqrt{ x_{0} })}{(x - x_{0})(\sqrt{ x } + \sqrt{ x_{0} })} = \frac{\cancel{ x - x_{0} }}{\cancel{ (x - x_{0}) }(\sqrt{ x } + \sqrt{ x_{0} })} = \frac{1}{\sqrt{ x } + \sqrt{ x_{0} }}
$$
De esta forma, y sabiendo que $x \to x_{0}$:
$$
f'(x_{0}) = \frac{1}{\sqrt{ x } + \sqrt{ x_{0} }} = \frac{1}{2\sqrt{ x_{0} }} \implies f'(x) = \frac{1}{2\sqrt{ x }}
$$

### Parte d)
$$
f'(x_{0}) = \frac{\frac{1}{x} - \frac{1}{x_{0}}}{x - x_{0}} = \frac{\frac{x_{0} - x}{x x_{0}}}{x - x_{0}} = \frac{\cancel{ (x_{0} - x) } \times \frac{1}{x x_{0}}}{\cancel{ x - x_{0} }} = -\frac{1}{x x_{0}}
$$
De esta forma, y sabiendo que $x \to x_{0}$:
$$
f'(x_{0}) = -\frac{1}{x x_{0}} = -\frac{1}{x_{0}^{2}} \implies f'(x) = -\frac{1}{x^{2}}
$$

---
## Ejercicio 6.1.2
Para determinar lo solicitado, tenemos que analizar el comportamiento de la función a medida que varía $x$.
### Parte c)
Separemos el estudio de la función en dos casos:
1. $x \not \in \mathbb{Z} \implies x \neq \lfloor x \rfloor$
En este caso, si establecemos un $x_{0} \not \in \mathbb{Z}$, veremos que los valores $x$ cercanos a $x_{0}$ cumplen que
$$
x \to x_{0} \land x_{0} \not \in \mathbb{Z} \implies \lfloor x \rfloor = \lfloor x_{0} \rfloor  
$$
De esta forma:
$$
f'(x) = \frac{\lfloor \overbrace{ x \rfloor - \lfloor x_{0} }^{ = 0 } \rfloor}{\underbrace{ x - x_{0} }_{ \to 0 }} = 0
$$
Esto tiene sentido, ya que la función es constante para todos los valores $x \not \in \mathbb{Z}$. De esta forma, es derivable para todos los puntos $x \not \in \mathbb{Z}$, siendo la derivada en dichos puntos 0.

2. $x \in \mathbb{Z} \implies x = \lfloor x \rfloor$
En este caso, tenemos un problema, ya que cuando estudiamos los valores de $x$ cercanos a $x_{0}$ tenemos que analizar por separado los valores por izquierda y por derecha:
$$
x \to x_{0}^{-} \land x_{0} \in \mathbb{Z} \implies \lfloor x \rfloor - \lfloor x_{0} \rfloor = -1
$$
$$
x \to x_{0}^{+} \land x_{0} \in \mathbb{Z} \implies \lfloor x \rfloor - \lfloor x_{0} \rfloor = 0
$$
Por esta razón, vemos que la función no es continua en $x \in \mathbb{Z}$, por lo tanto, la misma no es derivable para ningún $x \in \mathbb{Z}$.

Si intentamos estudiar la derivada de cada lado, podemos ver que:

$$
x \to x_{0}^{-} \implies f'(x) = \frac{\overbrace{ \lfloor x \rfloor - \lfloor x_{0} \rfloor }^{ = -1 }}{\underbrace{ x - x_{0} }_{ \to 0^{-} }} = + \infty
$$
$$
x \to x_{0}^{+} \implies f'(x) = \frac{\lfloor \overbrace{ x \rfloor - \lfloor x_{0} }^{ = 0 } \rfloor}{\underbrace{ x - x_{0} }_{ \to 0 }} = 0
$$
De esta forma, la función es derivable únicamente por la derecha cuando consideramos $x \in \mathbb{Z}$.

En conclusión, la función $f(x) = \lfloor x \rfloor$ solo es derivable para los valores $x \not \in \mathbb{Z}$ y derivable por la derecha en el caso $x \in \mathbb{Z}$.

---
## Ejercicio 6.1.3
### Parte b)
Acabamos de estudiar la función $f(x) = \lfloor x \rfloor$, y vimos que es derivable para los valores $x \not \in \mathbb{Z}$ y derivable por la derecha en el caso $x \in \mathbb{Z}$. Por lo tanto, solo es derivable como tal para $x \not \in \mathbb{Z}$, y su derivada siempre es 0.

Ahora, si analizamos la función $g(x) = \sin x$, sabemos que la misma es continua en todo su dominio. Además, se trata de una función compuesta: $\sin$ por un lado y $x$ por otro. De esta forma, aplicamos la regla de la cadena:
$$
(f \circ g)'(x) = f'(g(x)) \times g'(x)
$$
$$
\implies \sin' x = \cos x
$$
Puesto que, por definición, la derivada de $\sin$ es $\cos$.

Ahora, si desarrollamos la compuesta y estudiamos su derivada:
$$
(\sin(\lfloor x \rfloor ))' = \sin'(\lfloor x \rfloor ) \times (\lfloor x \rfloor )' = \cos(\lfloor x \rfloor) \times 0 = 0
$$
En conclusión la derivada de $\sin(\lfloor x \rfloor )$ (en los puntos en los que es derivable) es 0.

Para determinar en que puntos es derivable la función, analizamos cada caso:
- $\sin x$ es derivable en todo su dominio.
- $\lfloor x \rfloor$ es derivable solo en los casos en los que $x \not \in \mathbb{Z}$.

Por esta razón, y considerando las reglas de derivación, como una de las funciones no es derivable en casos específicos, la función compuesta por la misma tampoco lo será.

En conclusión:
$\sin(\lfloor x \rfloor )$ es derivable para todo $x \not \in \mathbb{Z}$ y su derivada es 0.

---
## Ejercicio 6.1.4
### Parte a)
#### Parte 1)
$$
L = \lim_{ h \to 0 } \frac{f(x_{0} + 2h) - f(x_{0})}{h}
$$
Para resolver el ejercicio, tenemos que considerar la definición de derivada en un punto:
$$
f'(x_{0}) = \lim_{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}} = \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0})}{h}
$$

De esta forma, lo importante es que el parámetro que se adiciona al argumento de $f$ y el denominador sean iguales.
Por esta razón, consideraremos un nuevo valor $k = 2h$. De esta forma:
$$
\lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0})}{h} = \lim_{ k \to 0 } \frac{f(x_{0} + k) - f(x_{0})}{\frac{k}{2}}
$$
Ahora, podemos pasar el divisor de $k$ hacia afuera, ya que es constante:
$$
= \lim_{ k \to 0 } \frac{f(x_{0} + k) - f(x_{0})}{\frac{k}{2}} = 2\lim_{ k \to 0 } \frac{f(x_{0} + k) - f(x_{0})}{k}
$$
Ahora, llegamos a una expresión equivalente a $f'(x_{0})$:
$$
f'(x_{0}) = \lim_{ k \to 0 } \frac{f(x_{0} + k) - f(x_{0})}{k}
$$
Por lo tanto, a partir de la definición, $f$ es derivable en $x_{0}$.

#### Parte 2)
Ya comprobamos que $f$ es derivable en $x_{0}$. Ahora, la pregunta es, ¿Qué relación hay entre $L$ y $f'(x_{0})$:
$$
L = \lim_{ h \to 0 } \frac{f(x_{0} + 2h) - f(x_{0})}{h} = \lim_{ k \to 0 } \frac{f(x_{0} + k) - f(x_{0})}{\frac{k}{2}} \implies L = 2\lim_{ k \to 0 } \frac{f(x_{0} + k) - f(x_{0})}{k}
$$
$$
f'(x_{0}) = \lim_{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}} = \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0})}{h}
$$
De esta forma, podemos determinar que $f'(x_{0}) = \frac{L}{2} \implies L = 2f'(x_{0})$.

ACLARACIÓN: LA IDEA DE DETERMINAR UNA DERIVADA EN BASE A LA DEFINICIÓN ES SIEMPRE RESPETAR LA DEFINICIÓN ORIGINAL (CUALQUIERA DE LAS DOS FORMAS), Y LLEGAR A ALGÚN DESPEJE O CANCELACIÓN QUE NOS PERMITA LLEGAR AL RESULTADO ESPERADO.

---
# 2 - Recta tangente
## Ejercicio 6.2.1
Analizando el gráfico, para determinar que la función sea derivable, debe cumplir que:
- Sea continua.
- No sea "angulosa" (la pendiente por la izquierda y por la derecha no cambie drásticamente).
- No sea "vertical" (en cuyo caso se dice informalmente que tiende a $\pm \infty$).

En base a esto, podemos determinar que la función no es derivable para:
- $x = -1$: la pendiente "tiende a infinito" (es vertical).
- $x = 6$: la función no es continua.
- $x = 8$: es "angulosa" (la pendiente para $x \to 8^{-}$ y $x \to 8^{+}$ son diferentes).

---
## Ejercicio 6.2.2
Para determinar $a$ y $b$, tenemos que modificar los parámetros para que la función resultante $h(x) = máx\{ f(x), g(x) \}$ cumpla las propiedades mencionadas en el ejercicio anterior:
- Sea continua.
- No sea "angulosa" (la pendiente por la izquierda y por la derecha no cambie drásticamente).
- No sea "vertical" (en cuyo caso se dice informalmente que tiende a $\pm \infty$).
Para todos los valores propuestos, la función es continua y no es vertical, por lo que el reto esta en hallar valores de $a$ y $b$ para los cuales la función propuesta no tenga cambios bruscos de pendiente.

Por ejemplo, podemos considerar:
$$
\begin{align}
&a = 2.2 \\
&b = 2.3
\end{align}
$$

---
## Ejercicio 6.2.3
En este caso, tenemos que estudiar para que valor de $x$, la pendiente de la recta tangente a la función en ese punto es menor, lo que equivale a decir que la derivada en ese punto es menor.

Para esto, tenemos que analizar los puntos marcados y estudiar la "velocidad de decrecimiento" de cada uno.

A simple vista, podemos ver que $x_{4}$ es el punto en el que la derivada es mayor, seguido de $x_{3}$. Para $x_{2}$ la derivada parece ser 0. Esto nos deja únicamente una opción: $x_{1}$. Es el único punto de los destacados para el cual la pendiente es negativa, o al menos decrece considerablemente más rápido que el resto.

De esta forma:
$$
f'(x_{1}) \leq f'(x_{i})
$$
con $i \in \{ 1, 2, 3, 4 \}$

En conclusión: $i_{0} = 1$

---
## Ejercicio 6.2.4
Calcularemos la tangente, y simplemente será visualizada en GeoGebra.
### Parte a)
$$
x^{2}, p = (3, 9)
$$
De esta forma: $x = 3$ y $f(x) = x^{2} = 9$.
Considerando que la derivada para la función $x^{2}$ en un punto dado se calcula con la fórmula $f'(x) = 2x$, entonces:
$$
f(3) = 3^{2} = 9 \implies f'(3) = 2 \times 3 = 6
$$
De esta forma, la pendiente de la recta tangente a la función $x^{2}$ en el punto $(3, 9)$ es $6$.

Es así que podemos determinar la recta tangente:
$$
r := y = 6x - 9
$$
Le restamos 9, ya que tiene que pasar por el punto $(3, 9)$ y $f(x) = 6x$ pasa por el punto $(3, 18)$.

---
## Ejercicio 6.2.6
Primeramente, sabemos que la ecuación de una circunferencia en un plano cartesiano con centro en $P = (h, k)$ y radio $r$ es:
$$
\mathcal{C}(P, r) = (x - h)^{2} + (y - k)^{2} = r^{2}
$$
Lo que se nos pide probar es que para todo punto $Q$ perteneciente a la circunferencia, la recta tangente a la circunferencia en $Q$ es perpendicular a la recta que pasa por los puntos $P$ y $Q$.

Comenzaremos estudiando el caso $\mathcal{C}(0, 1)$. Aquí $P = (0, 0)$ y $r = 1$:
$$
\begin{align}
\mathcal{C}(0, 1) &= (x - 0)^{2} + (y - 0)^{2} = 1^{2} \\
&= x^{2} + y^{2} = 1
\end{align}
$$
$$
x^{2} + y^{2} = 1 \implies y = \sqrt{ 1 - x^{2} }
$$

Primero, verifiquemos que la función es derivable. Para esto, derivaremos $\sqrt{ 1 - x^{2} }$:
$$
(\sqrt{ x })' = \frac{1}{2\sqrt{ x }} \implies (\sqrt{ 1 - x^{2} })' = \frac{1}{2\sqrt{ 1 - x^{2} }} \times (1 - x^{2})' = -\frac{\cancel{ 2 }x}{\cancel{ 2 }\sqrt{ 1 - x^{2} }} = -\frac{x}{\sqrt{ 1 - x^{2} }}
$$
De esta forma, obtuvimos la derivada de la función presentada. Ahora, analicemos lo que pasa con la recta que corta a $Q$ y $P$.
Sabemos que $P = (0, 0)$ y $Q = (x, \sqrt{ 1 - x^{2} })$ (ya que $y = \sqrt{ 1 - x^{2} }$).

Entonces, podemos determinar la recta que pasa por ambos puntos:
$$
y - y_{1} = m(x - x_{1})
$$
$$
m = \frac{y_{2} - y_{1}}{x_{2} - x_{1}} = \frac{Q_{y} - P_{y}}{Q_{x} - P_{x}} = \frac{\sqrt{ 1 - x^{2} }}{x}
$$
$$
y - P_{y} = \frac{\sqrt{ 1 - x^{2} }}{x}(x - P_{x})
$$
De esta forma, como $P = (0, 0)$:
$$
\implies y = \frac{\sqrt{ 1 - x^{2} }}{x}x
$$
Como vemos, la pendiente de esta recta es:
$$
\frac{\sqrt{ 1 - x^{2} }}{x}
$$
Si consideramos la derivada de la circunferencia definida:
$$
-\frac{x}{\sqrt{ 1 - x^{2} }}
$$
Como vemos, es el opuesto del inverso, por lo tanto, si multiplicamos ambos valores:
$$
\frac{\sqrt{ 1 - x^{2} }}{x} \times \left( -\frac{x}{\sqrt{ 1 - x^{2} }} \right) = -\frac{x\sqrt{ 1 - x^{2} }}{x\sqrt{ 1 - x^{2} }} = -1
$$
Como el producto de ambos es -1, podemos determinar que ambas rectas son perpendiculares, demostrando que para todo punto $Q$ perteneciente a la circunferencia, la recta tangente a la circunferencia en $Q$ es perpendicular a la recta que pasa por los puntos $P$ y $Q$.

ACLARACIÓN:
1. Casos de tangentes verticales y horizontales.
Si $x = 0$, la pendiente de la recta que pasa por $P$ y $Q$ no está definida (es vertical), pero la tangente es horizontal (derivada 0).
Si $x = \pm_{1}$, la pendiente de la tangente no está definida (es vertical), pero la recta que pasa por $P$ y $Q$ es horizontal (derivada 0).
En estos casos, la perpendicularidad es evidente geométricamente, aunque el producto de las pendientes no se pueda calcular y determinar como -1.

2. Semicircunferencia inferior.
Cubrimos el caso $y = \sqrt{ 1 - x^{2} }$, pero para la semicircunferencia inferior, $y = -\sqrt{ 1 - x^{2} }$. El procedimiento es el mismo y se llega a la misma conclusión.

3. Generalización.
Para extender esto a cualquier centro $P(h, k)$, podemos ver a una circunferencia cualquiera sea como la traslación de la circunferencia unitaria (la estudiada en este caso), por lo que las derivadas (pendientes) se comportan de forma análoga al desplazar los ejes.

---
# 3 - Cálculo de derivadas
## Ejercicio 6.3.1
### Parte c)
$$
\frac{x^{2} + 3x + 2}{x^{4} + x^{2} + 1}
$$
Considerando la propiedad algebraica de derivada de un cociente:
$$
\left( \frac{f}{g} \right)' = \frac{f'g - fg'}{g^{2}}
$$
$$
\implies \left( \frac{x^{2} + 3x + 2}{x^{4} + x^{2} + 1} \right)' = \frac{(x^{2} + 3x + 2)'(x^{4} + x^{2} + 1) - (x^{2} + 3x + 2)(x^{4} + x^{2} + 1)'}{(x^{4} + x^{2} + 1)^{2}}
$$
$$
\begin{align}
&= \frac{(2x + 3)(x^{4} + x^{2} + 1) - (x^{2} + 3x + 2)(4x^{3} + 2x)}{(x^{4} + x^{2} + 1)^{2}} \\
&= \frac{2x^{5} + \cancel{ 2x^{3} } + 2x + 3x^{4} + 3x^{2} + 3 - 4x^{5} \cancel{ - 2x^{3} } - 12x^{4} - 6x^{2} - 8x^{3} - 4x}{(x^{4} + x^{2} + 1)^{2}} \\
&= \frac{-2x^{5} - 9x^{4} - 8x^{3} - 3x^{2} - 2x + 3}{(x^{4} + x^{2} + 1)^{2}} \\
&= \frac{-2x^{5} - 9x^{4} - 8x^{3} - 3x^{2} - 2x + 3}{x^{8} + 2x^{6} + 3x^{4} + 2x^{2} + 1}
\end{align}
$$
En conclusión:
$$
\left( \frac{x^{2} + 3x + 2}{x^{4} + x^{2} + 1} \right)' = \frac{-2x^{5} - 9x^{4} - 8x^{3} - 3x^{2} - 2x + 3}{x^{8} + 2x^{6} + 3x^{4} + 2x^{2} + 1}
$$
### Parte f)
$$
(\sqrt[5]{ x + 1 })^{2}
$$

$$
\left( (\sqrt[5]{ x + 1 })^{2} \right)' = \left( (\sqrt[5]{ x + 1 })(\sqrt[5]{ x + 1 }) \right)' = (\sqrt[5]{ x + 1 })'(\sqrt[5]{ x + 1 }) + (\sqrt[5]{ x + 1 })(\sqrt[5]{ x + 1 })' = 2((\sqrt[5]{ x + 1 })(\sqrt[5]{ x + 1 })')
$$
$$
(\sqrt[5]{ x + 1 })' = \frac{1}{5\sqrt[5]{ (x + 1)^{4} }} \times (x + 1)' = \frac{1}{5\sqrt[5]{ (x^{2} + 2x + 1)^{2} }} \times 1 = \frac{1}{5\sqrt[5]{ (x^{2} + 2x + 1)^{2} }}
$$
$$
(x^{2} + 2x + 1)^{2} = x^{4} + 2x^{3} + x^{2} + 2x^{3} + 4x^{2} + 2x + x^{2} + 2x + 1 = x^{4} + 4x^{3} + 6x^{2} + 4x + 1
$$
$$
\implies \frac{1}{5\sqrt[5]{ (x^{2} + 2x + 1)^{2} }} = \frac{1}{5\sqrt[5]{ x^{4} + 4x^{3} + 6x^{2} + 4x + 1 }}
$$
En conclusión:
$$
\left( (\sqrt[5]{ x + 1 })^{2} \right)' = \frac{1}{5\sqrt[5]{ x^{4} + 4x^{3} + 6x^{2} + 4x + 1 }}
$$

### Parte h)
$$
x^{3} \sin(x)
$$
$$
\left( x^{3} \sin(x) \right)' = (x^{3})' \sin(x) + x^{3} (\sin(x))' = 3x \sin(x) + x^{3} \cos(x) = x(3 \sin(x) + x^{2} \cos(x))
$$
En conclusión:
$$
\left( x^{3} \sin(x) \right)' = x(3 \sin(x) + x^{2} \cos(x))
$$

---
## Ejercicio 6.3.2
$$
\begin{align}
&h(x) = f(g(x)) \\
&H(x) = g(f(x))
\end{align}
$$
Antes de nada, determinemos las derivadas de ambas funciones:
$$
\begin{align}
&h'(x) = (f(g(x)))' = f'(g(x)) \times g'(x) \\
&H'(x) = (g(f(x)))' = g'(f(x)) \times f'(x)
\end{align}
$$
De esta forma:
$$
\begin{align}
&h'(1) = f'(g(1)) \times g'(1) = f'(2) \times g'(1) = 5 \times 6 = 30 \\
&H'(1) = g'(f(1)) \times f'(1) = g'(3) \times f'(1) = 9 \times 4 = 36
\end{align}
$$
En conclusión:
$$
\begin{align}
&h'(1) = 30 \\
&H'(1) = 36
\end{align}
$$

---
## Ejercicio 6.3.6
Una parte por fila

### Parte b)
$$
\sqrt{ x + \sqrt{ x + \sqrt{ x } } }
$$
$$
\left( \sqrt{ x + \sqrt{ x + \sqrt{ x } } } \right)' = \frac{1}{2\sqrt{ x + \sqrt{ x + \sqrt{ x } } }} \times \left( x + \sqrt{ x + \sqrt{ x } } \right)'
$$
$$
\left( x + \sqrt{ x + \sqrt{ x } } \right)' = 1 + \frac{1}{2\sqrt{ x + \sqrt{ x } }} \times \left( x + \sqrt{ x } \right)'
$$
$$
\left( x + \sqrt{ x } \right)' = 1 + \frac{1}{2\sqrt{ x }}
$$
$$
\implies \left( x + \sqrt{ x + \sqrt{ x } } \right)' = 1 + \frac{1}{2\sqrt{ x + \sqrt{ x } }} \times \left( 1 + \frac{1}{2\sqrt{ x }} \right) = 1 + \frac{1}{2\sqrt{ x + \sqrt{ x } }} + \frac{1}{4\sqrt{ x^{2} + x\sqrt{ x } }}
$$
$$
\implies \left( \sqrt{ x + \sqrt{ x + \sqrt{ x } } } \right)' = \frac{1}{2\sqrt{ x + \sqrt{ x + \sqrt{ x } } }} \times \left( 1 + \frac{1}{2\sqrt{ x + \sqrt{ x } }} + \frac{1}{4\sqrt{ x^{2} + x\sqrt{ x } }} \right)
$$
$$
= \frac{1}{2\sqrt{ x + \sqrt{ x + \sqrt{ x } } }} + \frac{1}{4\sqrt{ (x + \sqrt{ x })(x + \sqrt{ x + \sqrt{ x } }) }} + \frac{1}{8\sqrt{ (x^{2} + x\sqrt{ x })(x + \sqrt{ x + \sqrt{ x } }) }}
$$

### Parte d)
$$
\frac{1}{x - \frac{2}{x + \sin(x)}}
$$
$$
\left( \frac{1}{x - \frac{2}{x + \sin(x)}} \right)' = \frac{\cancel{ \overbrace{ (1)' }^{ 0 }\left( x - \frac{2}{x + \sin(x)} \right) } - 1\left( x - \frac{2}{x + \sin(x)} \right)'}{\left( x - \frac{2}{x + \sin(x)} \right)^{2}}
$$
$$
\left( x - \frac{2}{x + \sin(x)} \right)' = 1 - \frac{\cancel{ \overbrace{ (2)' }^{ = 0 }\left(x + \sin(x) \right) } - 2\left(x + \sin(x) \right)'}{(x + \sin(x))^{2}}
$$
$$
\left(x + \sin(x) \right)' = 1 + \cos(x)
$$
$$
(x + \sin(x))^{2} = x^{2} + 2x \sin(x) + \sin^{2}(x)
$$
$$
\implies \left( x - \frac{2}{x + \sin(x)} \right)' = 1 - \frac{ - 2\left( 1 + \cos(x) \right)}{x^{2} + 2x \sin(x) + \sin^{2}(x)} = 1 + \frac{ 2 + 2\cos(x) }{x^{2} + 2x \sin(x) + \sin^{2}(x)}
$$
$$
\left( x - \frac{2}{x + \sin(x)} \right)^{2} = x^{2} - \frac{4x}{x + \sin(x)} + \frac{4}{x^{2} + 2x \sin(x) + \sin^{2}(x)}
$$
$$
\implies \left( \frac{1}{x - \frac{2}{x + \sin(x)}} \right)' = -\frac{ 1 + \frac{ 2 + 2\cos(x) }{x^{2} + 2x \sin(x) + \sin^{2}(x)}}{x^{2} - \frac{4x}{x + \sin(x)} + \frac{4}{x^{2} + 2x \sin(x) + \sin^{2}(x)}}
$$
$$
\begin{align}
1 + \frac{ 2 + 2\cos(x) }{x^{2} + 2x \sin(x) + \sin^{2}(x)} &= \frac{x^{2} + 2x \sin(x) + \sin^{2}(x) + 2 + 2\cos(x)}{x^{2} + 2x \sin(x) + \sin^{2}(x)}
\end{align}
$$
$$
\begin{align}
x^{2} - \frac{4x}{x + \sin(x)} + \frac{4}{x^{2} + 2x \sin(x) + \sin^{2}(x)} &= x^{2} - \frac{4x(x + \sin(x))}{x^{2} + 2x \sin(x) + \sin^{2}(x)} + \frac{4}{x^{2} + 2x \sin(x) + \sin^{2}(x)} \\
&= \frac{x^{2}(x^{2} + 2x \sin(x) + \sin^{2}(x)) - 4x(x + \sin(x)) + 4}{x^{2} + 2x \sin(x) + \sin^{2}(x)}
\end{align}
$$
$$
\implies -\frac{ 1 + \frac{ 2 + 2\cos(x) }{x^{2} + 2x \sin(x) + \sin^{2}(x)}}{x^{2} - \frac{4x}{x + \sin(x)} + \frac{4}{x^{2} + 2x \sin(x) + \sin^{2}(x)}} = -\frac{\frac{x^{2} + 2x \sin(x) + \sin^{2}(x) + 2 + 2\cos(x)}{\cancel{ x^{2} + 2x \sin(x) + \sin^{2}(x) }}}{\frac{x^{2}(x^{2} + 2x \sin(x) + \sin^{2}(x)) - 4x(x + \sin(x)) + 4}{\cancel{ x^{2} + 2x \sin(x) + \sin^{2}(x) }}}
$$
$$
= -\frac{x^{2} + 2x \sin(x) + \sin^{2}(x) + 2 + 2\cos(x)}{x^{2}(x^{2} + 2x \sin(x) + \sin^{2}(x)) - 4x(x + \sin(x)) + 4}
$$

### Parte h)
$$
\log \left( \sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \right)
$$
$$
\left( \log \left( \sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \right) \right)' = \frac{1}{\sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right)} \times \left( \sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \right)'
$$
$$
\left( \sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \right)' = \sin'\left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \times \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right)'
$$
$$
\sin'\left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) = \cos\left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right)
$$
$$
\left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right)' = \frac{(e^{\sqrt{ x }} + x)'(e^{x} - \sqrt{ x }) - (e^{\sqrt{ x }} + x)(e^{x} - \sqrt{ x })'}{(e^{x} - \sqrt{ x })^{2}}
$$
$$
(e^{\sqrt{ x }} + x)' = (\exp(\sqrt{ x }) + x)' = \exp(\sqrt{ x }) \times \frac{1}{2\sqrt{ x }} + 1 = \frac{e^{\sqrt{ x }}}{2\sqrt{ x }} + 1
$$
$$
(e^{x} - \sqrt{ x })' = (\exp(x) - \sqrt{ x })' = \exp(x) - \frac{1}{2\sqrt{ x }} = e^{x} - \frac{1}{2\sqrt{ x }}
$$

$$
\implies \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right)' = \frac{\left( \frac{e^{\sqrt{ x }}}{2\sqrt{ x }} + 1 \right)(e^{x} - \sqrt{ x }) - (e^{\sqrt{ x }} + x)\left( e^{x} - \frac{1}{2\sqrt{ x }} \right)}{(e^{x} - \sqrt{ x })^{2}}
$$
$$
= \frac{\frac{e^{x + \sqrt{ x }}}{2\sqrt{ x }} - \frac{e^{\sqrt{ x }}}{2} + e^{x} - \sqrt{ x } - e^{x + \sqrt{ x }} + \frac{e^{\sqrt{ x }}}{2\sqrt{ x }} - xe^{x} + \frac{x}{2\sqrt{ x }} }{(e^{x} - \sqrt{ x })^{2}}
$$
$$
= \frac{\frac{e^{x + \sqrt{ x }}}{2\sqrt{ x }} - \frac{\sqrt{ x }e^{\sqrt{ x }}}{2\sqrt{ x }} + \frac{2\sqrt{ x }e^{x}}{2\sqrt{ x }} - \frac{2x}{2\sqrt{ x }} - \frac{2\sqrt{ x }e^{x + \sqrt{ x }}}{2\sqrt{ x }} + \frac{e^{\sqrt{ x }}}{2\sqrt{ x }} - \frac{2x\sqrt{ x }e^{x}}{2\sqrt{ x }} + \frac{x}{2\sqrt{ x }} }{(e^{x} - \sqrt{ x })^{2}}
$$
$$
= \frac{\frac{ e^{x + \sqrt{ x }} - \sqrt{ x }e^{\sqrt{ x }} + 2\sqrt{ x }e^{x} - 2x - 2\sqrt{ x }e^{x + \sqrt{ x }} + e^{\sqrt{ x }} - 2x\sqrt{ x }e^{x} + x}{2\sqrt{ x }} }{(e^{x} - \sqrt{ x })^{2}}
$$
$$
= \frac{ e^{x + \sqrt{ x }} - \sqrt{ x }e^{\sqrt{ x }} + 2\sqrt{ x }e^{x} - 2x - 2\sqrt{ x }e^{x + \sqrt{ x }} + e^{\sqrt{ x }} - 2x\sqrt{ x }e^{x} + x }{2\sqrt{ x }(e^{x} - \sqrt{ x })^{2}}
$$
$$
= \frac{ (1 - 2\sqrt{ x })e^{x + \sqrt{ x }} + (2\sqrt{ x } - 2x\sqrt{ x })e^{x} + (1 - \sqrt{ x })e^{\sqrt{ x }} - x }{2\sqrt{ x }(e^{x} - \sqrt{ x })^{2}}
$$
$$
= \frac{ (1 - 2\sqrt{ x })e^{x + \sqrt{ x }} + (2\sqrt{ x } - 2x\sqrt{ x })e^{x} + (1 - \sqrt{ x })e^{\sqrt{ x }} - x }{2\sqrt{ x }(e^{2x} - 2\sqrt{ x }e^{x} + x)}
$$
$$
= \frac{ (1 - 2\sqrt{ x })e^{x + \sqrt{ x }} + (2\sqrt{ x } - 2x\sqrt{ x })e^{x} + (1 - \sqrt{ x })e^{\sqrt{ x }} - x }{2\sqrt{ x }e^{2x} - 4xe^{x} + 2x\sqrt{ x }}
$$
$$
\implies \left( \sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \right)' = \cos\left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \times \frac{ (1 - 2\sqrt{ x })e^{x + \sqrt{ x }} + (2\sqrt{ x } - 2x\sqrt{ x })e^{x} + (1 - \sqrt{ x })e^{\sqrt{ x }} - x }{2\sqrt{ x }e^{2x} - 4xe^{x} + 2x\sqrt{ x }}
$$
$$
\implies \left( \log \left( \sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \right) \right)' = \frac{1}{\sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right)} \times \cos\left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \times \frac{ (1 - 2\sqrt{ x })e^{x + \sqrt{ x }} + (2\sqrt{ x } - 2x\sqrt{ x })e^{x} + (1 - \sqrt{ x })e^{\sqrt{ x }} - x }{2\sqrt{ x }e^{2x} - 4xe^{x} + 2x\sqrt{ x }}
$$
$$
= \frac{\cos\left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right) \times \frac{ (1 - 2\sqrt{ x })e^{x + \sqrt{ x }} + (2\sqrt{ x } - 2x\sqrt{ x })e^{x} + (1 - \sqrt{ x })e^{\sqrt{ x }} - x }{2\sqrt{ x }e^{2x} - 4xe^{x} + 2x\sqrt{ x }}}{\sin \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right)} = \frac{ \frac{ (1 - 2\sqrt{ x })e^{x + \sqrt{ x }} + (2\sqrt{ x } - 2x\sqrt{ x })e^{x} + (1 - \sqrt{ x })e^{\sqrt{ x }} - x }{2\sqrt{ x }e^{2x} - 4xe^{x} + 2x\sqrt{ x }} }{\tan \left( \frac{e^{\sqrt{ x }} + x}{e^{x} - \sqrt{ x }} \right)}
$$

### Parte i)
$$
\frac{\log\left( \frac{\sin(x)}{x} \right)}{\sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)}
$$
$$
\left( \frac{\log\left( \frac{\sin(x)}{x} \right)}{\sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)} \right)' = \frac{\left( \log \left( \frac{\sin(x)}{x} \right) \right)'\sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) - \log \left( \frac{\sin(x)}{x} \right)\left( \sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) \right)'}{\sin^{2}\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)}
$$
$$
\left( \log \left( \frac{\sin(x)}{x} \right) \right)' = \frac{1}{\frac{\sin(x)}{x}} \times \left( \frac{\sin(x)}{x} \right)' = \frac{x}{\sin(x)} \times \left( \frac{\sin(x)}{x} \right)'
$$
$$
\left( \frac{\sin(x)}{x} \right)' = \frac{\sin'(x)x - \sin(x)(x)'}{x^{2}} = \frac{x\cos(x) - \sin(x)}{x^{2}}
$$
$$
\implies \left( \log \left( \frac{\sin(x)}{x} \right) \right)' = \frac{x}{\sin(x)} \times \frac{x\cos(x) - \sin(x)}{x^{2}} = \frac{x^{2} \cos(x) - x \sin(x)}{x^{2} \sin(x)} = \frac{x \cos(x) - \sin(x)}{x \sin(x)}
$$
$$
= \frac{\cancel{ x } \cos(x)}{\cancel{ x } \sin(x)} - \frac{\cancel{ \sin(x) }}{x \cancel{ \sin(x) }} = \frac{\cos(x)}{\sin(x)} - \frac{1}{x} = \frac{1}{\tan(x)} - \frac{1}{x}
$$
$$
\left( \sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) \right)' = \sin'\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) \times \left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)'
$$
$$
\sin'\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) = \cos\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)
$$
$$
\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)' = \frac{1}{\frac{x + 2}{x^{2} - 1}} \times \left( \frac{x + 2}{x^{2} - 1} \right)' = \frac{x^{2} - 1}{x + 2} \times \left( \frac{x + 2}{x^{2} - 1} \right)'
$$
$$
\left( \frac{x + 2}{x^{2} - 1} \right)' = \frac{(x + 2)'(x^{2} - 1) - (x + 2)(x^{2} - 1)'}{(x^{2} - 1)^{2}} = \frac{1(x^{2} - 1) - 2x(x + 2)}{(x^{2} - 1)^{2}}
$$
$$
= \frac{x^{2} - 1 - 2x^{2} - 4x}{(x^{2} - 1)^{2}} = \frac{-x^{2} - 4x - 1}{x^{4} - 2x^{2} + 1}
$$
$$
\implies \left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)' = \frac{x^{2} - 1}{x + 2} \times \frac{-x^{2} - 4x - 1}{x^{4} - 2x^{2} + 1} = \frac{(x^{2} - 1)(-x^{2} - 4x - 1)}{(x + 2)(x^{4} - 2x^{2} + 1)}
$$
$$
= \frac{-x^{4} - 4x^{3} - \cancel{ x^{2} } + \cancel{ x^{2} } + 4x + 1}{x^{5} - 2x^{3} + x + 2x^{4} - 4x^{2} + 2} = \frac{-x^{4} - 4x^{3} + 4x + 1}{x^{5} + 2x^{4} - 2x^{3} - 4x^{2} + x + 2}
$$
$$
\implies \left( \sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) \right)' = \cos\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) \times \frac{-x^{4} - 4x^{3} + 4x + 1}{x^{5} + 2x^{4} - 2x^{3} - 4x^{2} + x + 2}
$$
$$
\implies \left( \frac{\log\left( \frac{\sin(x)}{x} \right)}{\sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)} \right)' = \frac{\left( \frac{1}{\tan(x)} - \frac{1}{x} \right) \times \sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) - \log \left( \frac{\sin(x)}{x} \right) \times \cos\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) \times \frac{-x^{4} - 4x^{3} + 4x + 1}{x^{5} + 2x^{4} - 2x^{3} - 4x^{2} + x + 2}}{\sin^{2}\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)}
$$
$$
= \frac{ \frac{\sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)}{\tan(x)} - \frac{ \sin\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)}{x} - \log \left( \frac{\sin(x)}{x} \right) \times \cos\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right) \times \frac{-x^{4} - 4x^{3} + 4x + 1}{x^{5} + 2x^{4} - 2x^{3} - 4x^{2} + x + 2}}{\sin^{2}\left( \log\left( \frac{x + 2}{x^{2} - 1} \right) \right)}
$$

---
## Ejercicio 6.3.7
Una parte
### Parte b)
$$
x \log(x) - x
$$
$$
(x \log(x) - x)' = (x \log(x))' - 1
$$
$$
(x \log(x))' = (x)'\log(x) + x(\log(x))' = \log(x) + x\left( \frac{1}{x} \right) = \log(x) + 1
$$
$$
\implies (x \log(x) - x)' = \log(x) + 1 - 1 = \log(x)
$$


---
## Ejercicio 6.3.9
Primero que nada, ¿Qué significa "la derivada de orden $n$"?
Dicho término refiere a la derivada n-ésima de una función, o derivar una misma función $n$ veces.
Para resolverlo, iremos derivando poco a poco hasta encontrar un patrón.

Una parte por fila
### Parte e)
$$
\frac{1}{1 - x}
$$
$$
\left( \frac{1}{1 - x} \right)' = \frac{\cancel{ \overbrace{ (1)' }^{ = 0 }(1 - x) } - 1(1 - x)'}{(1 - x)^{2}} = -\frac{(1 - x)'}{(1 - x)^{2}}
$$
$$
(1 - x)' = 0 - 1 = -1
$$
$$
\implies \left( \frac{1}{1 - x} \right)' = -\frac{-1}{(1 - x)^{2}} = \frac{1}{(1 - x)^{2}}
$$
Proseguimos con la segunda derivada:
$$
\frac{1}{(1 - x)^{2}}
$$
$$
\left( \frac{1}{(1 - x)^{2}} \right)' = \frac{\cancel{ \overbrace{ (1)' }^{ = 0 }(1 - x)^{2} } - 1((1 - x)^{2})'}{(1 - x)^{2}} = -\frac{((1 - x)^{2})'}{(1 - x)^{4}}
$$
$$
((1 - x)^{2})' = (1 - 2x + x^{2})' = -2 + 2x = 2x - 2
$$
$$
\implies \left( \frac{1}{(1 - x)^{2}} \right)' = - \frac{2x - 2}{(1 - x)^{4}} = \frac{2 - 2x}{(1 - x)^{4}} = \frac{2(1 - x)}{(1 - x)^{4}} = \frac{2}{(1 - x)^{3}}
$$
Calculamos la tercera derivada:
$$
\frac{2 - 2x}{(1 - x)^{4}}
$$
$$
\left( \frac{2 - 2x}{(1 - x)^{4}} \right)' = \frac{(2 - 2x)'(1 - x)^{4} - (2 - 2x)((1 - x)^{4})'}{(1 - x)^{8}}
$$
$$
(2 - 2x)' = 0 - 2 = -2
$$
$$
((1 - x)^{4})' = (1 - 4x + 6x^{2} - 4x^{3} + x^{4})' = 0 - 4 + 12x - 12x^{2} + 4x^{3} = -4 + 12x - 12x^{2} + 4x^{3}
$$
$$
\implies \left( \frac{2 - 2x}{(1 - x)^{4}} \right)' = \frac{-2(1 - 4x + 6x^{2} - 4x^{3} + x^{4}) - (2 - 2x)(-4 + 12x - 12x^{2} + 4x^{3})}{(1 - x)^{8}}
$$
$$
= \frac{-2 + 8x - 12x^{2} + 8x^{3} - 2x^{4} + 8 - 32x + 48x^{2} - 32x^{3} + 8x^{4}}{(1 - x)^{8}}
$$
$$
= \frac{6 - 24x + 36x^{2} - 24x^{3} + 6x^{4}}{(1 - x)^{8}} = \frac{6(1 - 4x + 6x^{2} - 4x^{3} + x^{4})}{(1 - x)^{8}} = \frac{6(1 - x)^{4}}{(1 - x)^{8}} = \frac{6}{(1 - x)^{4}}
$$

Por último, estudiaremos la cuarta derivada:
$$
\frac{6}{(1 - x)^{4}}
$$
$$
\left( \frac{6}{(1 - x)^{4}} \right)' = \frac{\cancel{ \overbrace{ (6)' }^{ = 0 }(1 - x)^{4} } - 6((1 - x)^{4})'}{(1 - x)^{8}} = -\frac{6((1 - x)^{4})'}{(1 - x)^{8}}
$$
$$
((1 - x)^{4})' = (1 - 4x + 6x^{2} - 4x^{3} + x^{4})' = 0 - 4 + 12x - 12x^{2} + 4x^{3} = 4(-1 + 3x - 3x^{2} + x^{3})
$$
$$
\implies \left( \frac{6}{(1 - x)^{4}} \right)' = -\frac{6 \times 4(-1 + 3x - 3x^{2} + x^{3})}{(1 - x)^{8}} = \frac{24(1 - x)^{3}}{(1 - x)^{8}} = \frac{24}{(1 - x)^{5}}
$$

Como vemos, el denominador siempre coincide con el denominador original ($1 - x$) elevado a $n + 1$, mientras que el numerador es el factorial de $n$.

En conclusión, la derivada de orden $n$ de $\frac{1}{1 - x}$ es:
$$
\left( \frac{1}{1 - x} \right)^{(n)} = \frac{n!}{(1 - x)^{n + 1}}
$$

### Parte g)
$$
\cos(3x)
$$
Primera derivada:
$$
\left( \cos(3x) \right)' = \cos'(3x) \times (3x)' = -\sin(3x) \times 3 = -3 \sin(3x)
$$

Segunda derivada:
$$
\left( -3 \sin(3x) \right)' = \cancel{ \overbrace{ (-3)' }^{ = 0 }(\sin(3x)) } - 3(\sin(3x))' = -3 \cos(3x) \times 3 = -9 \cos(3x)
$$
Tercera derivada:
$$
\left( -9 \cos(3x) \right)' = \cancel{ \overbrace{ (-9)' }^{ = 0 }(\cos(3x)) } - 9(\cos(3x))' = 9 \sin(3x) \times 3 = 27 \sin(3x)
$$
Cuarta derivada:
$$
\left( 27 \sin(3x) \right)' = \cancel{ \overbrace{ (27)' }^{ = 0 }(\sin(3x)) } + 27(\sin(3x))' = 27 \cos(3x) \times 3 = 81 \cos(3x)
$$
Quinta derivada:
$$
\left( 81 \cos(3x) \right)' = \cancel{ \overbrace{ (81)' }^{ = 0 }(\cos(3x)) } + 81(\cos(3x))' = -81 \sin(3x) \times 3 = -243 \sin(3x)
$$
Bien, ahora podemos analizar que pasa en cada caso:
- Si $n = 4k$ (múltiplo de 4): $\left( \cos(3x) \right)^{(n)} = 3^{n} \cos(3x)$
- Si $n = 4k + 1$: $\left( \cos(3x) \right)^{(n)} = -3^{n} \sin(3x)$
- Si $n = 4k + 2$: $\left( \cos(3x) \right)^{(n)} = -3^{n} \cos(3x)$
- Si $n = 4k + 3$: $\left( \cos(3x) \right)^{(n)} = 3^{n} \sin(3x)$

---
## Ejercicio 6.3.11
En este ejercicio, simplemente tenemos que aplicar las reglas y teoremas de cálculo de derivadas vistos hasta ahora, como las reglas de suma, resta, producto, cociente, composición, etc.
### Parte b)
$$
f(x) = g(x)(x - a)
$$
$$
\begin{align}
f'(x) &= (g(x)(x - a))' \\
&= g'(x)(x - a) + g(x)(x - a)' \\
&= g'(x)(x - a) + g(x) \\
&= xg'(x) - ag'(x) + g(x)
\end{align}
$$
En conclusión:
$$
f'(x) = xg'(x) - ag'(x) + g(x)
$$

### Parte f)
$$
f(x) = g(x + g(x))
$$
$$
\begin{align}
f'(x) &= (g(x + g(x)))' \\
&= g'(x + g(x)) \cdot (x + g(x))' \\
&= g'(x + g(x)) \cdot (1 + g'(x)) \\
&= g'(x + g(x)) + g'(x + g(x)) \cdot g'(x)
\end{align}
$$
En conclusión:
$$
f'(x) = g'(x + g(x)) + g'(x + g(x)) \cdot g'(x)
$$

### Parte h)
$$
f(x + 3) = g(x^{3} - x) \implies f(x) = g((x - 3)^{3} - (x - 3))
$$
$$
\begin{align}
f'(x) &= (g((x - 3)^{3} - (x - 3)))' \\
&= g'((x - 3)^{3} - (x - 3)) \cdot ((x - 3)^{3} - (x - 3))' \\
&= g'((x - 3)^{3} - (x - 3)) \cdot (3(x - 3)^{2} \cdot (x - 3)' - 1) \\
&= g'((x - 3)^{3} - (x - 3)) \cdot (3(x^{2} - 6x + 9) - 1) \\
&= g'((x - 3)^{3} - (x - 3)) \cdot (3x^{2} - 18x + 27 - 1) \\
&= g'((x - 3)^{3} - (x - 3)) \cdot (3x^{2} - 18x + 26)
\end{align}
$$
En conclusión:
$$
f'(x) = g'((x - 3)^{3} - (x - 3)) \cdot (3x^{2} - 18x + 26)
$$

---
## Ejercicio 6.3.14
Una parte por fila

Para encontrar los valores de los parámetros correspondientes que aseguren la derivabilidad de la función, tenemos que encontrar valores que aseguren no solo que la función sea continua, sino también mantenga el mismo valor para la derivada en dicho punto.

### Parte b)
$$
f(x) = \begin{cases}
\begin{align}
&e^{ax} - 3 &&x < 1 \\
&\sin(\beta \log(x)) && x \geq 1
\end{align}
\end{cases}
$$

Considerando el caso $x = 1$ (que marca el cambio entre ambos casos):
$$
e^{\alpha} - 3
$$
$$
\sin(\beta \log(1)) = \sin(0)
$$
Dichas imágenes tienen que ser iguales para asegurar la continuidad:
$$
\begin{align}
e^{\alpha} - 3 = \sin(0) \\
e^{\alpha} - 3 = 0 \\
e^{\alpha} = 3
\end{align}
$$
Podemos despejar a $\alpha$ aplicando logaritmo a cada lado:
$$
\begin{align}
e^{\alpha} &= 3 \\
\log(e^{\alpha}) &= \log(3) \\
\alpha\log(e) &= \log(3)
\end{align}
$$
Como sabemos, $\log(e) = 1$:
$$
\implies \alpha\log(e) = \alpha = \log(3)
$$

Además, para asegurar la derivabilidad en $x = 1$, se tiene que cumplir que:
$$
(e^{\alpha x} - 3)' = (\sin(\beta \log(x)))'
$$
para $x = 0$.
Determinemos cada derivada:
$$
(e^{\alpha x} - 3)' = \alpha e^{\alpha x}
$$
$$
(\sin(\beta \log(x)))' = \sin'(\beta \log(x)) \times (\beta \log(x))'
$$
$$
(\beta \log(x))' = \cancel{ \overbrace{ (\beta)' }^{ = 0 } \log(x) } + \beta (\log(x))' = \beta \times \frac{1}{x} = \frac{\beta}{x}
$$
$$
\implies (\sin(\beta \log(x)))' = \cos(\beta \log(x)) \times \frac{\beta}{x}
$$
Es así que:
$$
\alpha e^{\alpha x} = \cos(\beta \log(x)) \times \frac{\beta}{x} \overbrace{ \implies }^{ x = 1 } \alpha e^{\alpha} = \cos(\beta \log(1)) \times \frac{\beta}{1}
$$
$$
\begin{align}
\alpha e^{\alpha} &= \cos(\beta \log(1)) \times \frac{\beta}{1} \\
\alpha e^{\alpha} &= \cos(0) \times \beta \\
\alpha e^{\alpha} &= 1 \times \beta \\
\alpha e^{\alpha} &= \beta
\end{align}
$$
Como determinamos que $e^{\alpha} = 3$:
$$
3\alpha = \beta \implies 3 \log(3) = \log(3^{3}) = \log(27) = \beta
$$

De esta forma, para asegurar la derivabilidad de la función en $x = 1$, los parámetros $\alpha$ y $\beta$ deben ser:
$$
\begin{cases}
\alpha = \log(3) \\
\beta = \log(27)
\end{cases}
$$

### Parte c)
$$
f(x) = \begin{cases}
\begin{align}
&x^{2} &&x < c \\
&ax + b && x \geq c
\end{align}
\end{cases}
$$
Comparamos ambas derivadas:
$$
\begin{align}
(c^{2})' &= (ac + b)' \\
2c &= a
\end{align}
$$
Logramos determinar el parámetro $a$, ahora nos falta $b$.
Para asegurar la continuidad:
$$
\begin{align}
c^{2} &= ac + b \\
c^{2} - b &= ac \\
\frac{c^{2} - b}{c} &= a \\
\frac{c^{2}}{c} - \frac{b}{c} &= a \\
c - \frac{b}{c} &= a
\end{align}
$$
Como sabemos que $a = 2c$:
$$
\begin{align}
c - \frac{b}{c} &= 2c \\
c &= 2c + \frac{b}{c} \\
c - 2c &= \frac{b}{c} \\
-c &= \frac{b}{c} \\
(-c) \times c &= b \\
-(c)^{2} &= b
\end{align}
$$
De esta forma, para asegurar la derivabilidad de $f$ en $c$, los valores de $a$ y $b$ son:
$$
\begin{cases}
a = 2c \\
b = -(c)^{2}
\end{cases}
$$

### Parte d)
$$
f(x) = \begin{cases}
\begin{align}
&\frac{1}{|x|} &&|x| > c \\
&a + bx^{2} &&|x| \leq c
\end{align}
\end{cases}
$$
En este caso, vamos a tener que estudiar la función $\frac{1}{|x|}$ en dos partes, ya que si $x < 0 \implies (|x|)' = -1$ y si $x > 0 \implies (|x|)' = 1$.

Otra cosa a considerar: si $c < 0$, entonces la función $f$ se comporta como $\frac{1}{|x|}$ durante todo su recorrido.

Estudiamos las derivadas de $\frac{1}{|x|}$:
- $x < 0$
$$
\left( \frac{1}{|x|} \right)' = - \frac{-1}{x^{2}} = \frac{1}{x^{2}}
$$
- $x > 0$
$$
\left( \frac{1}{|x|} \right)' = - \frac{1}{x^{2}}
$$

Proseguimos con la derivada de $a + bx^{2}$
$$
(a + bx^{2})' = 2bx
$$

De esta forma, para asegurar la derivabilidad de $f$ tiene que cumplirse que:
- Si $x < 0$: $2bx = \frac{1}{x^{2}}$
- Si $x > 0$: $2bx = -\frac{1}{x^{2}}$
$$
\begin{align}
&2bx = \frac{1}{x^{2}} \\
&b = \frac{1}{2x^{3}}
\end{align}
$$
Entonces:
- Si $x < 0$: $b = \frac{1}{2x^{3}}$
- Si $x > 0$: $b = -\frac{1}{2x^{3}}$

Ahora, proseguimos a comparar las imágenes. Sabemos que para asegurar la continuidad, tiene que cumplirse que:
$$
\frac{1}{|x|} = a + bx^{2}
$$
cuando $|x| = c$

De esta forma:
$$
\begin{align}
&\frac{1}{c} = a + bc^{2} \\
&\frac{1}{c} - bc^{2} = a
\end{align}
$$
Nuevamente, diferenciamos en dos casos según los valores de $b$. Operaremos considerando $x < 0$:
$$
\begin{align}
&\frac{1}{c} - \frac{1}{2x^{3}}c^{2} = a \\
&\frac{1}{c} - \frac{c^{2}}{2x^{3}} = a \\
&\frac{2x^{3} - c^{3}}{2cx^{3}} = a
\end{align}
$$

En definitiva:
- Si $x < 0$: $a = \frac{2x^{3} - c^{3}}{2cx^{3}}$
- Si $x > 0$: $a = \frac{2x^{3} + c^{3}}{2cx^{3}}$

En conclusión, $f$ es continua y derivable si consideramos los siguientes valores:
- Si $x < 0$:
$$
\begin{align}
&a = \frac{2x^{3} - c^{3}}{2cx^{3}} \\
&b = \frac{1}{2x^{3}}
\end{align}
$$
- Si $x > 0$:
$$
\begin{align}
&a = \frac{2x^{3} + c^{3}}{2cx^{3}} \\
&b = -\frac{1}{2x^{3}}
\end{align}
$$

ERROR: LA RESOLUCIÓN ES INCORRECTA, YA QUE TRATAMOS A $a$ Y $b$ COMO FUNCIONES DE $x$. EN REALIDAD, $a$ Y $b$ SON CONSTANTES QUE DEBEN ASEGURAR LA DERIVABILIDAD EN LOS PUNTOS DE TRANSICIÓN. ESTOS SON PUNTOS DONDE EL VALOR ABSOLUTO DE $x$ IGUALA A $c$, ES DECIR, EN $x = c$ Y $x = -c$.

DE ESTA FORMA, TENEMOS QUE IGUALAR LAS DERIVADAS LATERALES EN EL PUNTO DE UNIÓN.

CORRECCIÓN:
Para que la función sea derivable, deben coincidir tanto el valor de las funciones como las pendientes en los bordes $x = c$ y $x = -c$.

En $x = c$ (suponiendo $c > 0$):
- Continuidad: El valor por izquierda ($a + bc^{2}$) debe ser igual al valor por derecha ($\frac{1}{c}$):
$$
a + bc^{2} = \frac{1}{c}
$$
- Derivabilidad: La derivada por izquierda ($2bc$) debe ser igual a la derivada por derecha ($-\frac{1}{c^{2}}$):
$$
2bc = -\frac{1}{c^{2}}
$$
$$
\implies b = -\frac{1}{2c^{3}}
$$
Ahora, sustituimos el valor de $b$ en la ecuación de continuidad:
$$
\begin{align}
&a - \frac{1}{2c^{3}}c^{2} = \frac{1}{c} \\
&a - \frac{\cancel{ c^{2} }}{2c\cancel{ ^{3} }} = \frac{1}{c} \\
&a - \frac{1}{2c} = \frac{1}{c} \\
&a = \frac{1}{c} + \frac{1}{2c} \\
&a = \frac{2}{2c} + \frac{1}{2c} \\
&a = \frac{3}{2c}
\end{align}
$$
En conclusión, determinamos que los siguientes valores de $a$ y $b$ aseguran la derivabilidad de la función $f$:
$$
\begin{align}
&a = \frac{3}{2c} \\
&b = -\frac{1}{2c^{3}}
\end{align}
$$

---
# 4 - Cálculo de límites (Regla de L'Hôpital)
## Ejercicio 6.4.1
Básicamente, la idea es calcular límites a partir de la regla de L'Hôpital, cuyo enunciado es:

> [!Regla de L'Hôpital (bilateral)]
> Sean $f, g$ dos funciones tales que:
> - $f, g$ son definidas y derivables en $\overbrace{ E^{*}(a, \delta) }^{ (a - \delta, a) \cup (a, a + \delta) }$ (con $a \in \mathbb{R}, \delta > 0$)
> - $\lim_{ x \to a } f = \lim_{ x \to a } g = 0$
> - $g'(x) \neq 0 \qquad (\forall x \in E^{*}(a, \delta))$
> - Existe $\lim_{ x \to a } \frac{f'}{g'} = \lambda \in \mathbb{R}$
> 
> Entonces:
> $$
> g(x) \neq 0 \qquad \forall x \in E^{*}(a, \delta)
> $$
> y
> $$
> \lim_{ x \to a } \frac{f(x)}{g(x)} = \lambda \left( = \lim_{ x \to a } \frac{f'(x)}{g'(x)}  \right) 
> $$

Básicamente, tenemos que derivar ambas funciones hasta eliminar la indeterminación, calculando finalmente el límite.

Una parte por fila

### Parte c)
$$
\lim_{ x \to 0 } \frac{e^{x} - \cos(x)}{\sin(\pi x)} 
$$
Si sustituimos $x$ por 0:
$$
\lim_{ x \to 0 } \frac{e^{x} - \cos(x)}{\sin(\pi x)} = \frac{e^{0} - \cos(0)}{\sin(0)} = \frac{1 - 1}{0} = \frac{0}{0}
$$
De esta forma, llegamos a una indeterminación de tipo $\frac{0}{0}$, por lo que tenemos que aplicar la regla de L'Hôpital:
$$
\lim_{ x \to 0 } \frac{e^{x} - \cos(x)}{\sin(\pi x)} = \lim_{ x \to 0 } \frac{(e^{x} - \cos(x))'}{(\sin(\pi x))'} 
$$
$$
(e^{x} - \cos(x))' = e^{x} + \sin(x)
$$
$$
(\sin(\pi x))' = \sin'(\pi x) \times (\pi x)' = \cos(\pi x) \times \pi
$$
$$
\implies \lim_{ x \to 0 } \frac{e^{x} - \cos(x)}{\sin(\pi x)} = \lim_{ x \to 0 } \frac{e^{x} + \sin(x)}{\cos(\pi x) \times \pi} 
$$
Ahora, probemos sustituir $x$ por 0:
$$
\lim_{ x \to 0 } \frac{e^{x} + \sin(x)}{\cos(\pi x) \times \pi} = \frac{e^{0} + \sin(0)}{\cos(0) \times \pi} = \frac{1 + 0}{1 \times \pi} = \frac{1}{\pi}
$$
En conclusión:
$$
\lim_{ x \to 0 } \frac{e^{x} - \cos(x)}{\sin(\pi x)} = \frac{1}{\pi}
$$

### Parte f)
$$
\lim_{ x \to 0 } \frac{x - \log(1 + x)}{x^{2} + \cos(\pi x) - 1}
$$
Intentamos determinar el límite sustituyendo $x$ por 0:
$$
\lim_{ x \to 0 } \frac{x - \log(1 + x)}{x^{2} + \cos(\pi x) - 1} = \frac{0 - \log(1 + 0)}{0^{2} + \cos(\pi 0) - 1} = \frac{-\log(1)}{\cos(0) - 1} = \frac{0}{0}
$$
A continuación, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to 0 } \frac{x - \log(1 + x)}{x^{2} + \cos(\pi x) - 1} = \lim_{ x \to 0 } \frac{(x - \log(1 + x))'}{(x^{2} + \cos(\pi x) - 1)'}
$$
$$
(x - \log(1 + x))' = 1 - (\log_{1} + x)' = 1 - \frac{1}{1 + x} \times (1 + x)' = 1 - \frac{1}{1 + x} \times 1 = 1 - \frac{1}{1 + x}
$$
$$
(x^{2} + \cos(\pi x) - 1)' = 2x + (\cos(\pi x))' = 2x - \sin(\pi x) \times (\pi x)' = 2x - \pi \sin(\pi x)
$$
$$
\implies \lim_{ x \to 0 } \frac{x - \log(1 + x)}{x^{2} + \cos(\pi x) - 1} = \lim_{ x \to 0 } \frac{1 - \frac{1}{1 + x}}{2x - \pi \sin(\pi x)}
$$
Ahora, probemos sustituir $x$ por 0:
$$
\lim_{ x \to 0 } \frac{1 - \frac{1}{1 + x}}{2x - \pi \sin(\pi x)} = \frac{1 - \frac{1}{1 + 0}}{2 \times 0 - \pi \sin(\pi 0)} = \frac{1 - 1}{0 - 0} = \frac{0}{0}
$$
Nuevamente obtuvimos una indeterminación, por lo que tenemos que derivar otra vez:
$$
\lim_{ x \to 0 } \frac{1 - \frac{1}{1 + x}}{2x - \pi \sin(\pi x)} = \lim_{ x \to 0 } \frac{\left( 1 - \frac{1}{1 + x} \right)'}{(2x - \pi \sin(\pi x))'}
$$
$$
\left( 1 - \frac{1}{1 + x} \right)' = -\left( \frac{1}{1 + x} \right)' = -\frac{\cancel{ \overbrace{ (1)' }^{ = 0 }(1 + x) } - 1(1 + x)'}{(1 + x)^{2}} = \frac{1}{x^{2} + 2x + 1}
$$
$$
(2x - \pi \sin(\pi x))' = 2 - (\cancel{ \overbrace{ (\pi)' }^{ = 0 }(\sin(\pi x)) } + \pi(\sin(\pi x))') = 2 - \pi \cos(\pi x) \times (\pi x)' = 2 - \pi^{2} \cos(\pi x)
$$
$$
\implies \lim_{ x \to 0 } \frac{1 - \frac{1}{1 + x}}{2x - \pi \sin(\pi x)} = \lim_{ x \to 0 } \frac{\frac{1}{x^{2} + 2x + 1}}{2 - \pi^{2} \cos(\pi x)}
$$
Ahora, probemos sustituir $x$ por 0:
$$
\lim_{ x \to 0 } \frac{\frac{1}{x^{2} + 2x + 1}}{2 - \pi^{2} \cos(\pi x)} = \frac{\frac{1}{0^{2} + 2 \times 0 + 1}}{2 - \pi^{2} \cos(\pi 0)} = \frac{\frac{1}{1}}{2 - \pi^{2}} = -\frac{1}{\pi^{2} - 2}
$$
En conclusión:
$$
\lim_{ x \to 0 } \frac{x - \log(1 + x)}{x^{2} + \cos(\pi x) - 1} = -\frac{1}{\pi^{2} - 2}
$$

### Parte g)
$$
\lim_{ x \to 1 } \frac{\log(x^{58})}{x^{85} - 1}
$$
Intentamos determinar el límite sustituyendo $x$ por 1:
$$
\lim_{ x \to 1 } \frac{\log(x^{58})}{x^{85} - 1} = \frac{\log(1^{58})}{1^{85} - 1} = \frac{\log(1)}{1 - 1} = \frac{0}{0}
$$
A continuación, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to 1 } \frac{\log(x^{58})}{x^{85} - 1} = \lim_{ x \to 1 } \frac{(\log(x^{58}))'}{(x^{85} - 1)'}
$$
$$
\begin{align}
(\log(x^{58}))' &= \frac{1}{x^{58}} \cdot (x^{58})' \\
&= \frac{1}{x^{58}} \cdot 58x^{57} \\
&= \frac{58\cancel{ x^{57} }}{x\cancel{ ^{58} }} \\
&= \frac{58}{x}
\end{align}
$$
$$
\begin{align}
(x^{85} - 1)' &= 85x^{84}
\end{align}
$$
$$
\implies \lim_{ x \to 1 } \frac{\log(x^{58})}{x^{85} - 1} = \lim_{ x \to 1 } \frac{\frac{58}{x}}{85x^{84}} = \lim_{ x \to 1 } \frac{58}{85x^{85}}
$$
Ahora, probemos sustituir $x$ por 1:
$$
\lim_{ x \to 1 } \frac{58}{85x^{85}} = \frac{58}{85 \cdot 1^{85}} = \frac{58}{85}
$$


### Parte h)
$$
\lim_{ x \to 0 } \frac{\cos(x)^{51} - 1}{x^{2}}
$$
Intentamos determinar el límite sustituyendo $x$ por 0:
$$
\lim_{ x \to 0 } \frac{\cos(x)^{51} - 1}{x^{2}} = \frac{\cos(0)^{51} - 1}{0^{2}} = \frac{1^{51} - 1}{0} = \frac{0}{0}
$$
A continuación, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to 0 } \frac{\cos(x)^{51} - 1}{x^{2}} = \lim_{ x \to 0 } \frac{(\cos(x)^{51} - 1)'}{(x^{2})'}
$$
$$
(\cos(x)^{51} - 1)' = 51 \cos(x)^{50} \times (\cos(x))' = 51 \cos(x)^{50} \times (-\sin (x))
$$
$$
(x^{2})' = 2x
$$
$$
\implies \lim_{ x \to 0 } \frac{\cos(x)^{51} - 1}{x^{2}} = \lim_{ x \to 0 } \frac{51 \cos(x)^{50} \times (-\sin (x))}{2x}
$$
Ahora, probemos sustituir $x$ por 0:
$$
\lim_{ x \to 0 } \frac{51 \cos(x)^{50} \times (-\sin (x))}{2x} = \frac{51 \cos(0)^{50} \times (-\sin (0))}{2 \times 0} = \frac{51 1^{50} \times 0}{2 \times 0} = \frac{0}{0}
$$
Nuevamente obtuvimos una indeterminación, por lo que tenemos que derivar otra vez:
$$
\lim_{ x \to 0 } \frac{51 \cos(x)^{50} \times (-\sin (x))}{2x} = \lim_{ x \to 0 } \frac{(51 \cos(x)^{50} \times (-\sin (x)))'}{(2x)'}
$$
$$
(51 \cos(x)^{50} \times (-\sin (x)))' = (51 \cos(x)^{50})' (-\sin (x)) + 51 \cos(x)^{50} (-\sin (x))'
$$
$$
= 2550 \cos(x)^{49} (-\sin(x)) (-\sin (x)) + 51 \cos(x)^{50} (-\cos (x)) = 2550 \cos(x)^{51}\sin(x)^{2} - 51 \cos(x)^{51}
$$
$$
(2x)' = 2
$$
$$
\implies \lim_{ x \to 0 } \frac{51 \cos(x)^{50} \times (-\sin (x))}{2x} = \lim_{ x \to 0 } \frac{2550 \cos(x)^{51}\sin(x)^{2} - 51 \cos(x)^{51}}{2}
$$
Ahora, probemos sustituir $x$ por 0:
$$
\lim_{ x \to 0 } \frac{2550 \cos(x)^{51}\sin(x)^{2} - 51 \cos(x)^{51}}{2} = \frac{2550 \cos(0)^{51}\sin(0)^{2} - 51 \cos(0)^{51}}{2}
$$
$$
= \frac{\cancel{ 2550 \times 1^{51} \times 0^{2} } - 51 \cos(0)^{51}}{2} = -\frac{51 \times 1^{51}}{2} = -\frac{51}{2}
$$
En conclusión:
$$
\lim_{ x \to 0 } \frac{\cos(x)^{51} - 1}{x^{2}} = -\frac{51}{2}
$$

### Parte k)
$$
\lim_{ x \to 1 } \frac{x}{x - 1} - \frac{1}{\log(x)}
$$
A continuación, reordenamos la función para que tenga la forma $\frac{f}{g}$:
$$
\lim_{ x \to 1 } \frac{x}{x - 1} - \frac{1}{\log(x)} = \lim_{ x \to 1 } \frac{x \log(x) - (x - 1)}{\log(x)(x - 1)} = \lim_{ x \to 1 } \frac{x \log(x) - x + 1}{x \log(x) - \log(x)}
$$
$$
\lim_{ x \to 1 } \frac{x}{x - 1} - \frac{1}{\log(x)} = \lim_{ x \to 1 } \frac{x \log(x) - x + 1}{x \log(x) - \log(x)}
$$
Intentamos determinar el límite sustituyendo $x$ por 1:
$$
\lim_{ x \to 1 } \frac{x \log(x) - x + 1}{x \log(x) - \log(x)} = \frac{\log(1) - 1 + 1}{\log(1) - \log(1)} = \frac{0 - 1 + 1}{0 - 0} = \frac{0}{0}
$$
Ahora, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to 1 } \frac{x \log(x) - x + 1}{x \log(x) - \log(x)} = \lim_{ x \to 1 } \frac{(x \log(x) - x + 1)'}{(x \log(x) - \log(x))'}
$$
$$
(x \log(x) - x + 1)' = (x)'\log(x) + x(\log(x))' - 1 = \log(x) + x \times \frac{1}{x} - 1 = \log(x) + 1 - 1 = \log(x)
$$
$$
(x \log(x) - \log(x))' = (x)'\log(x) + x(\log(x))' - \frac{1}{x} = \log(x) + x \times \frac{1}{x} - \frac{1}{x} = \log(x) + 1 - \frac{1}{x}
$$
$$
\implies \lim_{ x \to 1 } \frac{x \log(x) - x + 1}{x \log(x) - \log(x)} = \frac{\log(x)}{\log(x) + 1 - \frac{1}{x}}
$$
Ahora, probemos sustituir $x$ por 1:
$$
\lim_{ x \to 0 } \frac{\log(x)}{\log(x) + 1 - \frac{1}{x}} = \frac{\log(1)}{\log(1) + 1 - \frac{1}{1}} = \frac{0}{0 + 1 - 1} = \frac{0}{0}
$$
Nuevamente obtuvimos una indeterminación, por lo que tenemos que derivar otra vez:
$$
\lim_{ x \to 0 } \frac{\log(x)}{\log(x) + 1 - \frac{1}{x}} = \lim_{ x \to 0 } \frac{(\log(x))'}{(\log\left(x) + 1 - \frac{1}{x} \right)'}
$$
$$
(\log(x))' = \frac{1}{x}
$$
$$
\left(\log(x) + 1 - \frac{1}{x} \right)' = \frac{1}{x} - \frac{\cancel{ \overbrace{ (1)' }^{ = 0 }x } - (x)'}{x^{2}} = \frac{1}{x} + \frac{1}{x^{2}}
$$
$$
\implies \lim_{ x \to 0 } \frac{\log(x)}{\log(x) + 1 - \frac{1}{x}} = \lim_{ x \to 0 } \frac{\frac{1}{x}}{\frac{1}{x} + \frac{1}{x^{2}}}
$$
Ahora, probemos sustituir $x$ por 1:
$$
\lim_{ x \to 0 } \frac{\frac{1}{x}}{\frac{1}{x} + \frac{1}{x^{2}}} = \frac{\frac{1}{1}}{\frac{1}{1} + \frac{1}{1^{2}}} = \frac{1}{1 + 1} = \frac{1}{2}
$$
En conclusión:
$$
\lim_{ x \to 1 } \frac{x}{x - 1} - \frac{1}{\log(x)} = \frac{1}{2}
$$

---
## Ejercicio 6.4.2
Una parte por fila

### Parte b)
$$
\lim_{ x \to 1 } \frac{\sin(\log(x))}{\sin(\pi x)}
$$
Intentamos determinar el límite sustituyendo $x$ por 1:
$$
\lim_{ x \to 1 } \frac{\sin(\log(x))}{\sin(\pi x)} = \frac{\sin(\log(1))}{\sin(\pi 1)} = \frac{\sin(0)}{\sin(\pi)} = \frac{0}{0}
$$
Ahora, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to 1 } \lim_{ x \to 1 } \frac{\sin(\log(x))}{\sin(\pi x)} = \lim_{ x \to 1 } \frac{(\sin(\log(x)))'}{(\sin(\pi x))'}
$$
$$
(\sin(\log(x)))' = \sin'(\log(x)) \times \log'(x) = \cos(\log(x)) \times \frac{1}{x} = \frac{\cos(\log(x))}{x}
$$
$$
(\sin(\pi x))' = \sin'(\pi x) \times (\pi x)' = \cos(\pi x) \times \pi = \pi \cos(\pi x)
$$
$$
\implies \lim_{ x \to 1 } \lim_{ x \to 1 } \frac{\sin(\log(x))}{\sin(\pi x)} = \lim_{ x \to 1 } \frac{\frac{\cos(\log(x))}{x}}{\pi \cos(\pi x)}
$$
Ahora, probemos sustituir $x$ por 1:
$$
\lim_{ x \to 1 } \frac{\frac{\cos(\log(x))}{x}}{\pi \cos(\pi x)} = \frac{\frac{\cos(\log(1))}{1}}{\pi \cos(\pi 1)} = \frac{\cos(0)}{\pi \cos(\pi)} = \frac{1}{-\pi} = -\frac{1}{\pi}
$$
En conclusión:
$$
\lim_{ x \to 1 } \frac{\sin(\log(x))}{\sin(\pi x)} = -\frac{1}{\pi}
$$

### Parte d)
$$
\lim_{ x \to 1 } \frac{\pi \log(x) + \sin(\pi x)}{x^{3} - x^{2} - x + 1}
$$
Intentamos determinar el límite sustituyendo $x$ por 1:
$$
\lim_{ x \to 1 } \frac{\pi \log(x) + \sin(\pi x)}{x^{3} - x^{2} - x + 1} = \frac{\pi \log(1) + \sin(\pi)}{1^{3} - 1^{2} - 1 + 1} = \frac{\pi \times 0 + 0}{0} = \frac{0}{0}
$$
Ahora, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to 1 } \frac{\pi \log(x) + \sin(\pi x)}{x^{3} - x^{2} - x + 1} = \lim_{ x \to 1 } \frac{(\pi \log(x) + \sin(\pi x))'}{(x^{3} - x^{2} - x + 1)'}
$$
$$
(\pi \log(x) + \sin(\pi x))' = \cancel{ \overbrace{ (\pi)' }^{ = 0 }\log(x) } + \pi(\log(x))' + \sin'(\pi x) \times (\pi x)' = \pi \times \frac{1}{x} + \cos(\pi x) \times \pi = \frac{\pi}{x} + \pi \cos(\pi x)
$$
$$
(x^{3} - x^{2} - x + 1)' = 3x^{2} - 2x - 1
$$
$$
\implies \lim_{ x \to 1 } \frac{\pi \log(x) + \sin(\pi x)}{x^{3} - x^{2} - x + 1} = \lim_{ x \to 1 } \frac{\frac{\pi}{x} + \pi \cos(\pi x)}{3x^{2} - 2x - 1}
$$
Ahora, probemos sustituir $x$ por 1:
$$
\lim_{ x \to 1 } \frac{\frac{\pi}{x} + \pi \cos(\pi x)}{3x^{2} - 2x - 1} = \frac{\frac{\pi}{1} + \pi \cos(\pi)}{3 \times 1^{2} - 2 - 1} = \frac{\pi + \pi \cos(\pi)}{0} = \frac{\pi - \pi}{0} = \frac{0}{0}
$$
Nuevamente obtuvimos una indeterminación, por lo que tenemos que derivar otra vez:
$$
\lim_{ x \to 1 } \frac{\frac{\pi}{x} + \pi \cos(\pi x)}{3x^{2} - 2x - 1} = \lim_{ x \to 1 } \frac{(\frac{\pi}{x} + \pi \cos(\pi x))'}{(3x^{2} - 2x - 1)'}
$$
$$
\left( \frac{\pi}{x} + \pi \cos(\pi x) \right)' = \frac{\cancel{ \overbrace{ (\pi)' }^{ = 0 }x } - \pi(x)'}{x^{2}} + \cancel{ \overbrace{ (\pi)' }^{ = 0 }\cos(\pi x) } + \pi(\cos(\pi x))' = -\frac{\pi}{x^{2}} + \pi \cos'(\pi x) \times (\pi x)'
$$
$$
= -\frac{\pi}{x^{2}} - \pi^{2} \sin(\pi x)
$$
$$
(3x^{2} - 2x - 1)' = 6x - 2
$$
$$
\implies \lim_{ x \to 1 } \frac{\frac{\pi}{x} + \pi \cos(\pi x)}{3x^{2} - 2x - 1} = \lim_{ x \to 1 } \frac{-\frac{\pi}{x^{2}} - \pi^{2} \sin(\pi x)}{6x - 2}
$$
Ahora, probemos sustituir $x$ por 1:
$$
\lim_{ x \to 1 } \frac{-\frac{\pi}{x^{2}} - \pi^{2} \sin(\pi x)}{6x - 2} = \frac{-\frac{\pi}{1^{2}} - \pi^{2} \sin(\pi)}{6 - 2} = -\frac{\pi - \cancel{ \pi^{2} \times 0 }}{4} = -\frac{\pi}{4}
$$
En conclusión:
$$
\lim_{ x \to 1 } \frac{\pi \log(x) + \sin(\pi x)}{x^{3} - x^{2} - x + 1} = -\frac{\pi}{4}
$$

### Parte f)
$$
\lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)}}{x^{2}}
$$
Intentamos determinar el límite sustituyendo $x$ por 0:
$$
\lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)}}{x^{2}} = \frac{e^{0} - e^{\sin(0)}}{0^{2}} = \frac{e^{0} - e^{0}}{0} = \frac{1 - 1}{0} = \frac{0}{0}
$$
Ahora, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)}}{x^{2}} = \lim_{ x \to 0 } \frac{(e^{x} - e^{\sin(x)})'}{(x^{2})'}
$$
$$
(e^{x} - e^{\sin(x)})' = e^{x} - e^{\sin(x)} \times (\sin(x))' = e^{x} - e^{\sin(x)} \times \cos(x)
$$
$$
(x^{2})' = 2x
$$
$$
\implies \lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)}}{x^{2}} = \lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)} \times \cos(x)}{2x}
$$
Ahora, probemos sustituir $x$ por 0:
$$
\lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)} \times \cos(x)}{2x} = \frac{e^{0} - e^{\sin(0)} \times \cos(0)}{2 \times 0} = \frac{e^{0} - e^{0} \times 1}{0} = \frac{1 - 1}{0} = \frac{0}{0}
$$
Nuevamente obtuvimos una indeterminación, por lo que tenemos que derivar otra vez:
$$
\lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)} \times \cos(x)}{2x} = \lim_{ x \to 0 } \frac{(e^{x} - e^{\sin(x)} \times \cos(x))'}{(2x)'}
$$
$$
(e^{x} - e^{\sin(x)} \times \cos(x))' = e^{x} - ((e^{\sin(x)})'\cos(x) + e^{\sin(x)}(\cos(x))')
$$
$$
= e^{x} - (e^{\sin(x)} (\sin(x))' \cos(x) - e^{\sin(x)}\sin(x)) = e^{x} - (e^{\sin(x)} \cos(x) \cos(x) - e^{\sin(x)}\sin(x))
$$
$$
= e^{x} - e^{\sin(x)} \cos(x)^{2} + e^{\sin(x)}\sin(x)
$$
$$
(2x)' = 2
$$
$$
\implies \lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)} \times \cos(x)}{2x} = \lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)} \cos(x)^{2} + e^{\sin(x)}\cos(x)}{2}
$$
Ahora, probemos sustituir $x$ por 0:
$$
\lim_{ x \to 0 } \frac{e^{x} + e^{\sin(x)} \cos(x)^{2} + e^{\sin(x)}\cos(x)}{2} = \frac{e^{0} - e^{\sin(0)} \cos(0)^{2} + e^{\sin(0)}\sin(0)}{2} = \frac{e^{0} - e^{0} \times 1^{2} + \cancel{ e^{0} \times 0 }}{2}
$$
$$
= \frac{1 - 1}{2} = \frac{0}{2} = 0
$$
En conclusión:
$$
\lim_{ x \to 0 } \frac{e^{x} - e^{\sin(x)}}{x^{2}} = 0
$$

### Parte g)
$$
\lim_{ x \to 0 } \frac{\log(\cos(x^{2})) - \log ^{2}(\cos(x))}{x^{4}}
$$
Intentamos determinar el límite sustituyendo $x$ por 0:
$$
\lim_{ x \to 0 } \frac{\log(\cos(x^{2})) - \log ^{2}(\cos(x))}{x^{4}} = \frac{\log(\cos(0^{2})) - \log ^{2}(\cos(0))}{0^{4}} = \frac{\log(1) - \log ^{2}(1)}{0} = \frac{0 - 0^{2}}{0} = \frac{0}{0}
$$

Simplemente con observar el límite, podemos ver que quizás tengamos que derivar hasta unas 4 veces, ya que $x^{4}$ no dejará de ser 0 hasta que se transforme en constante.

Ahora, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to 0 } \frac{\log(\cos(x^{2})) - \log ^{2}(\cos(x))}{x^{4}} = \lim_{ x \to 0 } \frac{(\log(\cos(x^{2})) - \log ^{2}(\cos(x)))'}{(x^{4})'}
$$
Primera derivación:
$$
\begin{align}
(\log(\cos(x^{2})) - \log ^{2}(\cos(x)))' &= \frac{1}{\cos(x^{2})} \cdot (\cos(x^{2}))' - 2\log(\cos(x)) \cdot (\log(\cos(x)))' \\
&= \frac{1}{\cos(x^{2})} \cdot (-\sin(x^{2})) \cdot 2x - 2\log(\cos(x)) \cdot \frac{1}{\cos(x)} \cdot (\cos(x))' \\
&= 2x \cdot \left(- \frac{\sin(x^{2})}{\cos(x^{2})} \right) - 2\log(\cos(x)) \cdot \frac{1}{\cos(x)} \cdot (-\sin(x)) \\
&= 2x \cdot \left( -\frac{\sin(x^{2})}{\cos(x^{2})} \right) - 2\log(\cos(x)) \cdot \left( -\frac{\sin(x)}{\cos(x)} \right) \\
&= 2x \cdot \left( -\tan(x^{2}) \right) - 2\log(\cos(x)) \cdot \left( -\tan(x) \right)
\end{align}
$$
$$
\begin{align}
(x^{4})' &= 4x^{3}
\end{align}
$$
$$
\implies \lim_{ x \to 0 } \frac{\log(\cos(x^{2})) - \log ^{2}(\cos(x))}{x^{4}} = \lim_{ x \to 0 } \frac{2x \cdot \left( -\tan(x^{2}) \right) - 2\log(\cos(x)) \cdot \left( -\tan(x) \right)}{4x^{3}}
$$
Ahora, probemos sustituir $x$ por 0:
$$
\begin{align}
\lim_{ x \to 0 } \frac{2x \cdot \left( -\tan(x^{2}) \right) - 2\log(\cos(x)) \cdot \left( -\tan(x) \right)}{4x^{3}} &= \frac{\cancel{ 2 \cdot 0 \cdot \left( -\tan(0^{2}) \right) } - 2\log(\cos(0)) \cdot \left( -\tan(0) \right)}{4 \cdot 0^{3}} \\
&= \frac{0 - \cancel{ 2\log(1) \cdot 0 }}{0} \\
&= \frac{0}{0}
\end{align}
$$
Nuevamente obtuvimos una indeterminación, por lo que tenemos que derivar otra vez:
$$
\lim_{ x \to 0 } \frac{2x \cdot \left( -\tan(x^{2}) \right) - 2\log(\cos(x)) \cdot \left( -\tan(x) \right)}{4x^{3}} = \lim_{ x \to 0 } \frac{(2x \cdot \left( -\tan(x^{2}) \right) - 2\log(\cos(x)) \cdot \left( -\tan(x) \right))'}{(4x^{3})'}
$$
Simplificamos la expresión:
$$
2x \cdot \left( -\tan(x^{2}) \right) - 2\log(\cos(x)) \cdot \left( -\tan(x) \right) = -2x \cdot \tan(x^{2}) + 2\log(\cos(x)) \cdot \tan(x)
$$
Segunda derivación:
$$
\begin{align}
&(-2x \cdot \tan(x^{2}) + 2\log(\cos(x)) \cdot \tan(x))' \\
= &-2 \tan(x^{2}) - 2x \left( \frac{\sin(x^{2})}{\cos(x^{2})} \right)' - \frac{2}{\cos(x)} \cdot \sin(x) \cdot \tan(x) + 2\log(\cos(x)) \cdot \left( \frac{\sin(x)}{\cos(x)} \right)' \\
= &-2 \tan(x^{2}) - 2x \left( \frac{\sin(x^{2})}{\cos(x^{2})} \right)' - 2\tan(x) \cdot \tan(x) + 2\log(\cos(x)) \cdot \left( \frac{\sin(x)}{\cos(x)} \right)' \\
= &-2 \tan(x^{2}) - 2x \left( \frac{2x\cos ^{2}(x^{2}) + 2x\sin ^{2}(x^{2})}{\cos ^{2}(x^{2})} \right) - 2\tan(x) \cdot \tan(x) + 2\log(\cos(x)) \cdot \left( \frac{\cos ^{2}(x) + \sin ^{2}(x)}{\cos ^{2}(x)} \right) \\
= &-2 \tan(x^{2}) - 2x \left( 2x + 2x\tan ^{2}(x^{2}) \right) - 2\tan(x) \cdot \tan(x) + 2\log(\cos(x)) \cdot \left( 1 + \tan ^{2}(x) \right) \\
= &-2 \tan(x^{2}) - 4x^{2} - 4x^{2}\tan ^{2}(x^{2}) - 2\tan ^{2}(x) + 2\log(\cos(x)) + 2\log(\cos(x)) \cdot \tan ^{2}(x)
\end{align}
$$
$$
\begin{align}
(4x^{3})' &= 12x^{2}
\end{align}
$$
$$
\implies \lim_{ x \to 0 } \frac{2x \cdot \left( -\tan(x^{2}) \right) - 2\log(\cos(x)) \cdot \left( -\tan(x) \right)}{4x^{3}} = \lim_{ x \to 0 } \frac{-2 \tan(x^{2}) - 4x^{2} - 4x^{2}\tan ^{2}(x^{2}) - 2\tan ^{2}(x) + 2\log(\cos(x)) + 2\log(\cos(x)) \cdot \tan ^{2}(x)}{12x^{2}}
$$
Ahora, probemos sustituir $x$ por 0:
$$
\begin{align}
\lim_{ x \to 0 } &\frac{-2 \tan(x^{2}) - 4x^{2} - 4x^{2}\tan ^{2}(x^{2}) - 2\tan ^{2}(x) + 2\log(\cos(x)) + 2\log(\cos(x)) \cdot \tan ^{2}(x)}{12x^{2}} \\
= &\frac{-2 \tan(0^{2}) - \cancel{ 4 \cdot 0^{2} } - \cancel{ 4 \cdot 0^{2} \cdot \tan ^{2}(0^{2}) } - 2\tan ^{2}(0) + 2\log(\cos(0)) + 2\log(\cos(0)) \cdot \tan ^{2}(0)}{\cancel{ 12 \cdot 0^{2} }} \\
= &\frac{\cancel{ -2 \cdot 0 } - \cancel{ 2 \cdot 0^{2} } + \cancel{ 2\log(1) } + \cancel{ 2\log(1) \cdot 0^{2} }}{0} \\
= &\frac{0}{0}
\end{align}
$$

Si proseguimos derivando, a la cuarta vez (como sospechamos), llegaremos a una solución, la cual será $-\frac{3}{4}$.


---
## Ejercicio 6.4.3
Una parte por fila

En este caso, lo interesante del ejercicio es escribir los límites de tal forma que se forme una indeterminación de tipo $\frac{0}{0}$ o $\frac{\infty}{\infty}$. No siempre se nos presentaran indeterminaciones de este tipo, sin embargo, si logramos manipular las expresiones para llegar a dicha forma, podemos aplicar la regla de L'Hôpital para resolverlas.
### Parte b)
$$
\lim_{ x \to -\infty } x^{2} e^{x}
$$
Buscamos expresar el límite como un cociente:
$$
\lim_{ x \to -\infty } x^{2} e^{x} = \lim_{ x \to -\infty } \frac{e^{x}}{\frac{1}{x^{2}}}
$$
Intentamos determinar el límite sustituyendo $x$ por $-\infty$:
$$
\lim_{ x \to -\infty } \frac{e^{x}}{\frac{1}{x^{2}}} = \frac{e^{-\infty}}{\frac{1}{-\infty}} = \frac{0}{0}
$$
Ahora, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to -\infty } \frac{e^{x}}{\frac{1}{x^{2}}} = \lim_{ x \to -\infty } \frac{(e^{x})'}{\left( \frac{1}{x^{2}} \right)'}
$$
$$
(e^{x})' = e^{x}
$$
$$
\left( \frac{1}{x^{2}} \right)' = \frac{\cancel{ \overbrace{ (1)' }^{ = 0 }x^{2} } - 1(x^{2})'}{x^{4}} = -\frac{2x}{x^{4}} = -\frac{2}{x^{3}}
$$
$$
\implies \lim_{ x \to -\infty } \frac{e^{x}}{\frac{1}{x^{2}}} = \lim_{ x \to -\infty } \frac{e^{x}}{-\frac{2}{x^{3}}}
$$
Ahora, probemos sustituir $x$ por $-\infty$:
$$
\lim_{ x \to -\infty } \frac{e^{x}}{-\frac{2}{x^{3}}} = \frac{e^{-\infty}}{-\frac{2}{(-\infty)^{3}}} = \frac{e^{-\infty}}{\frac{2}{+\infty}} = \frac{0}{0}
$$
Nuevamente obtuvimos una indeterminación, por lo que tenemos que derivar otra vez:
$$
\lim_{ x \to -\infty } \frac{e^{x}}{\frac{2}{x^{3}}} = \lim_{ x \to -\infty } -\frac{(e^{x})'}{\left( -\frac{2}{x^{3}} \right)'}
$$
$$
(e^{x})' = e^{x}
$$
$$
\left( -\frac{2}{x^{3}} \right)' = -\frac{\cancel{ \overbrace{ (2)' }^{ = 0 }x^{3} } - 2(x^{3})'}{x^{6}} = \frac{6x^{2}}{x^{6}} = \frac{6}{x^{4}}
$$
Nos encontramos en un caso similar al anterior, así que continuamos derivando:
$$
(e^{x})' = e^{x}
$$
$$
\left( \frac{6}{x^{4}} \right)' = \frac{\cancel{ \overbrace{ (6)' }^{ = 0 }x^{4} } - 6(x^{4})'}{x^{8}} = \frac{-24x^{3}}{x^{8}} = -\frac{24}{x^{5}}
$$
Como vemos, aunque sigamos derivando, el numerador y denominador siempre tienden a 0 cuando $x \to -\infty$. Por lo tanto, tenemos que cambiar el acercamiento:
$$
\lim_{ x \to -\infty } x^{2} e^{x} = \lim_{ x \to -\infty } \frac{x^{2}}{e^{-x}}
$$
Intentamos determinar el límite sustituyendo $x$ por $-\infty$:
$$
\lim_{ x \to -\infty } \frac{x^{2}}{e^{-x}} = \frac{(-\infty)^{2}}{e^{-(-\infty)}} =  \frac{(-\infty)^{2}}{e^{+\infty}} = \frac{+\infty}{+\infty}
$$
Ahora, aplicamos la regla de L'Hôpital para determinar el límite:
$$
\lim_{ x \to -\infty } \frac{x^{2}}{e^{-x}} = \lim_{ x \to -\infty } \frac{(x^{2})'}{(e^{-x})'}
$$
$$
(x^{2})' = 2x
$$
$$
(e^{-x})' = e^{-x} \times (-x)' = -e^{-x}
$$
$$
\implies \lim_{ x \to -\infty } \frac{x^{2}}{e^{-x}} = \lim_{ x \to -\infty } \frac{2x}{-e^{-x}}
$$
Ahora, probemos sustituir $x$ por $-\infty$:
$$
\lim_{ x \to -\infty } \frac{2x}{-e^{-x}} = \frac{2 (-\infty)}{-e^{-(-\infty)}} = \frac{2 (-\infty)}{-e^{+\infty}} = \frac{-\infty}{-\infty}
$$
Nuevamente obtuvimos una indeterminación, por lo que tenemos que derivar otra vez:
$$
\lim_{ x \to -\infty } \frac{2x}{-e^{-x}} = \lim_{ x \to -\infty } \frac{(2x)'}{(-e^{-x})'}
$$
$$
(2x)' = 2
$$
$$
(-e^{-x})' = -e^{-x} \times (-x)' = e^{-x}
$$
$$
\implies \lim_{ x \to -\infty } \frac{2x}{-e^{-x}} = \lim_{ x \to -\infty } \frac{2}{e^{-x}}
$$
Ahora, probemos sustituir $x$ por $-\infty$:
$$
\lim_{ x \to -\infty } \frac{2}{e^{-x}} = \frac{2}{e^{-(-\infty)}} = \frac{2}{e^{+\infty}} = \frac{2}{+\infty} \to 0
$$
En conclusión:
$$
\lim_{ x \to -\infty } x^{2} e^{x} = 0
$$

### Parte e)
$$
\lim_{ x \to +\infty } \log ^{3}(x + 10) - \log ^{3}(x - 10)
$$
Probemos expresar el límite como un cociente. Para esto, comenzaremos considerando que tenemos una diferencia de cubos:
$$
\log ^{3}(x + 10) - \log ^{3}(x - 10) = (\log(x + 10) - \log(x - 10))(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))
$$
De esta forma, tenemos dos factores para estudiar:
$$
\lim_{ x \to +\infty } \log(x + 10) - \log(x - 10) = \lim_{ x \to +\infty } \log\left( \frac{x + 10}{x - 10} \right) \to 0
$$
Sabemos que el límite anterior tiende a 0, puesto que la diferencia entre los logaritmos se vuelve minúscula.
$$
\lim_{ x \to +\infty } \log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10) = (+\infty)^{2} + (+\infty)(+\infty) + (+\infty)^{2} = +\infty
$$
De esta forma, vemos que el límite tiende a $+\infty$, por lo que tenemos un problema de tipo $0 \cdot \infty$. Lo que haremos, es pasar el factor que tiende a $\infty$ dividiendo por su inverso:
$$
\lim_{ x \to +\infty } \log\left( \frac{x + 10}{x - 10} \right)(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10)) = \lim_{ x \to +\infty } \frac{\log\left( \frac{x + 10}{x - 10} \right)}{\frac{1}{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))}}
$$
Ahora, analicemos la derivada de numerador y denominador:
$$
\lim_{ x \to +\infty } \frac{\log\left( \frac{x + 10}{x - 10} \right)}{\frac{1}{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))}} = \lim_{ x \to +\infty } \frac{\left( \log\left( \frac{x + 10}{x - 10} \right) \right)'}{\left( \frac{1}{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))} \right)'}
$$
$$
\left( \log\left( \frac{x + 10}{x - 10} \right) \right)' = \left( \log\left( x + 10 \right) - \log(x - 10) \right)' = \frac{1}{x + 10} - \frac{1}{x - 10} = \frac{(\cancel{ x } - 10) - (\cancel{ x } + 10)}{(x - 10)(x + 10)}
$$
$$
= -\frac{20}{x^{2} - 100}
$$
$$
\left( \frac{1}{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))} \right)' = -\frac{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))'}{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))^{2}}
$$
$$
= -\frac{ \frac{2 \log(x + 10)}{x + 10} + \frac{\log(x - 10)}{x + 10} + \frac{\log(x + 10)}{x - 10} + \frac{2 \log(x - 10)}{x - 10} }{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))^{2}} = -\frac{ \frac{2 \log(x + 10) + \log(x - 10)}{x + 10} + \frac{2 \log(x - 10) + \log(x + 10)}{x - 10} }{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))^{2}}
$$

$$
\implies \lim_{ x \to +\infty } \frac{\log\left( \frac{x + 10}{x - 10} \right)}{\frac{1}{(\log ^{2 \log(x + 10)}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2 \log(x - 10)}(x - 10))}} = \lim_{ x \to +\infty } \frac{ \frac{20}{x^{2} - 100} }{ \frac{ \frac{2 \log(x + 10) + \log(x - 10)}{x + 10} + \frac{2 \log(x - 10) + \log(x + 10)}{x - 10} }{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))^{2}} }
$$
Si volvemos a sustituir $x$ por $+ \infty$, veremos que aún tenemos una indeterminación de tipo $\frac{0}{0}$:
$$
\lim_{ x \to +\infty } \frac{ \frac{20}{x^{2} - 100} }{ \frac{ \frac{2 \log(x + 10) + \log(x - 10)}{x + 10} + \frac{2 \log(x - 10) + \log(x + 10)}{x - 10} }{(\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))^{2}} } = \frac{ \frac{20}{+\infty} }{ \frac{ 0 }{+ \infty} }
$$
Lo podemos expresar como:
$$
\lim_{ x \to +\infty } \frac{20}{x^{2} - 100} \times \frac{ (\log ^{2}(x + 10) + \log(x + 10)\log(x - 10) + \log ^{2}(x - 10))^{2} }{\frac{2 \log(x + 10) + \log(x - 10)}{x + 10} + \frac{2 \log(x - 10) + \log(x + 10)}{x - 10}}
$$

En base a lo anterior, podríamos tomar la siguiente intuición: en el denominador, aún hay términos que dependen de $x$, por lo tanto tiene orden mayor. Además, cualquier término $x$ elevado a una potencia positiva crece mucho más rápido que la función logaritmo.

Por esta razón, si proseguimos estudiando la función, concluiremos que:
$$
\lim_{ x \to +\infty } \log ^{3}(x + 10) - \log ^{3}(x - 10) = 0
$$

---
# 5 - Valor medio
## Ejercicio 6.5.1
Lo que establece el teorema de valor medio de Lagrange es que, si considero una función continua y derivable en un intervalo $(a, b)$, si considero la pendiente del segmento que une a ambos extremos, entonces existirá al menos un punto $c$ en el intervalo, para el cual la derivada en dicho punto será equivalente a la pendiente mencionada. Esto se puede ver como: existe al menos un punto en el intervalo para el cual la velocidad instantánea coincide con la velocidad promedio del recorrido, definiendo la siguiente formula:
$$
f'(c) = \frac{f(b) - f(a)}{b - a}
$$


En este caso, tenemos que encontrar un valor $c \in [0, 6]$ tal que:
$$
f'(c) = \frac{f(6) - f(0)}{6}
$$
Con 0 y 6 extremos del intervalo.

Como dijimos previamente, que un punto $c \in [0, 6]$ cumpla que $f'(c) = \frac{f(6) - f(0)}{6}$ significa que la derivada en dicho punto sea equivalente a la pendiente de la recta que pasa por los puntos $(0, f(0))$ y $(6, f(6))$.

De esta forma, podemos considerar por ejemplo, el punto $c \simeq 3$. Aquí, la recta tangente es prácticamente paralela a la recta que pasa por $(0, f(0))$ y $(6, f(6))$.

Igualmente, no es el único punto que cumple dicha propiedad. También podríamos haber considerado $c \in (0.86, 1)$ o $c \in (5.1, 5.12)$. En el intervalo considerado $[0, 6]$ son los únicos valores que cumplen lo establecido.

---
## Ejercicio 6.5.2
Primero que nada, analicemos lo que establece el enunciado. Tenemos una función $f : \mathbb{R} \to \mathbb{R}$, en la cual existe un punto $a \in \mathbb{R}$ tal que la recta tangente a $f$ por $a$ corta al gráfico de $f$ en al menos otro punto más al que denominaremos $b$.

Tenemos que probar que existe un punto $c \neq a$ tal que $f'(c) = f'(a)$. Básicamente, que existe al menos un punto $c$ cuya derivada tiene pendiente equivalente a la derivada de la función $f$ en el punto $a$.

Para establecer una situación similar a la descrita en el teorema de Lagrange y así poder aprovecharlo, estudiaremos a la recta tangente a $f$ por $a$, que corta nuevamente a la función en $b$, como la recta que pasa por los puntos $(a, f(a))$ y $(b, f(b))$. De esta forma, podemos asegurar que la siguiente igualdad se cumple:
$$
f'(a) = \frac{f(b) - f(a)}{b - a}
$$
Ahora, considerando lo establecido por el teorema de Lagrange, como la función es continua y derivable, existe al menos un punto $c$ el cual cumple que:
$$
f'(c) = \frac{f(b) - f(a)}{b - a}
$$

En conclusión:
$$
f'(c) = f'(a)
$$

---
# 6 - Monotonía, extremos y geometría
## Ejercicio 6.6.1
Primero que nada, consideremos lo siguiente: si una función tiene un extremo relativo en un punto interior $x_{0}$, y la función es derivable en dicho punto, entonces $f'(x_{0}) = 0$.

Sin embargo, es importante considerar que:
- La propiedad puede no cumplirse para los extremos.
- Si la derivada en $x_{0}$ no existe, no podemos asegurar nada.
- El recíproco no se cumple: $f'(x_{0}) = 0 \cancel{ \implies } x_{0}$ es un extremo relativo

Considerando todos estos detalles, comencemos con la determinación de extremos relativos:
### Parte a y b)
$$
f(x) = |x|
$$
La función valor absoluto es continua en todo $\mathbb{R}$. Ahora, si analizamos su comportamiento, podemos ver que:
- Para $x_{0} > 0$: $f'(x_{0}) = 1$
- Para $x_{0} < 0: f'(x_{0}) = -1$

Sin embargo, si analizamos lo que sucede en $x_{0} = 0$:
$$
\begin{align}
&\lim_{ x \to 0^{-} } \frac{|x| - |x_{0}|}{x - x_{0}} = -1 \\
&\lim_{ x \to 0^{+} } \frac{|x| - |x_{0}|}{x - x_{0}} = 1
\end{align}
$$
Como vemos, la derivada por la izquierda y por la derecha de 0 son diferentes (la función no es derivable en 0), por lo tanto, no hay un extremo en 0.
Sin embargo, tampoco podemos encontrar extremos en el resto de la función, puesto que no hay valores de $x_{0}$ para los cuales $f'(x_{0}) = 0$.

$$
f(x) = \sqrt{ |x| }
$$
Este caso es idéntico al anterior.

### Parte d)
$$
f(x) = \lfloor x \rfloor
$$
Sabemos que la función $\lfloor x \rfloor$ es continua para todo $x \not \in \mathbb{Z}$, y discontinua (por lo tanto no derivable) para todo $x \in \mathbb{Z}$. De esta forma, la función es derivable en todo $x \not \in \mathbb{Z}$, y su derivada es 0 (ya hemos analizado el comportamiento de la función en ocasiones anteriores). En conclusión, todos los puntos $x \not \in \mathbb{Z}$ son extremos (máximos y mínimos) al mismo tiempo.

### Parte e)
$$
f(x) = \cos(x)
$$
En este caso, sabemos que la función es continua y derivable, por lo que determinaremos su derivada para saber para que valores de $x$ se cumple que $f'(x) = 0$:
$$
(\cos(x))' = -\sin(x)
$$
Ahora, sabemos que $\sin(x) = 0$ cuando $x \in \{ k\pi : k \in \mathbb{Z} \}$.
Además, por la forma de la función, sabemos que todos los puntos cuyas derivadas son nulas son extremos (en este caso puntual).

En conclusión:
Todo $x \in \{ k\pi : k \in \mathbb{Z} \}$ es un extremo relativo. Para ser más específico, podemos determinar cuales son máximos y mínimos relativos si analizamos lo que pasa alrededor de cada valor de $k$:
- Cuando $k$ es par, $\cos(k \pi)$ es un máximo relativo.
- Cuando $k$ es impar, $\cos(k \pi)$ es un mínimo relativo.



---
## Ejercicio 6.6.4
Sabemos que los polinomios son funciones constantes y derivables. En este caso, lo ideal sería probar que la función es monótona creciente o decreciente en dicho intervalo, asegurando que únicamente puede tener una raíz.

Sabemos que el polinomio $x^{3} - 3x + b = 0$ es una función monótona decreciente en el intervalo $[-1, 1]$, pero tenemos que demostrarlo, para lo cual podemos aprovechar que: si una función es monótona decreciente en un intervalo $I$, entonces $f'(x) \leq 0 \qquad (\forall x \in I)$.

Tenemos que analizar como se comporta la función en el intervalo. Para esto, analizaremos el signo de la derivada:
$$
(x^{3} - 3x + b)' = 3x^{2} - 3
$$
Como vemos, el valor $b$ al tratarse de una constante, no se considera cuando derivamos la función, ya que un valor constante no cambia la pendiente de la recta, aunque si altere la imagen de un valor de $x$.

Ahora, estudiaremos el signo de dicha función:
$$
3x^{2} - 3 = 3(x^{2} - 1) \implies \text{si } x = \pm 1, 3x^{2} - 3 = 0
$$

|  +  |     |  -  |     |  +  |
| :-: | :-: | :-: | :-: | :-: |
|     | -1  |     |  1  |     |

Como vemos, la función toma valores negativos en el intervalo $(-1, 1)$, siendo 0 en -1 y 1.

De esta forma, probamos que la función $x^{3} - 3x + b = 0$ es monótona decreciente en el intervalo considerado. Por tal razón, la función puede tener como máximo una raíz en dicha sección. Incluso, podríamos determinar las imágenes para -1 y 1, y así calcular el intervalo en el que debería estar $b$ para que la función tenga una raíz en $[-1, 1]$.

---
## Ejercicio 6.6.5
Básicamente, tenemos que demostrar que las funciones $f(x) = x^{2}$ y $g(x) = x \sin(x) + \cos(x)$ se cortan en exactamente dos puntos considerando que estamos trabajando en $\mathbb{R}^{2}$.

En este caso, consideraremos la derivada de cada función, para entender entre que puntos se pueden encontrar dichas intersecciones:
$$
f'(x) = 2x
$$
$$
g'(x) = \cancel{ \sin(x) } + x \cos(x) - \cancel{ \sin(x) } = x \cos(x)
$$
Sabemos que $f$ es estrictamente creciente para $x > 0$ y estrictamente decreciente para valores $x < 0$, mientras que $g$ oscila constantemente. Por esta razón, nos enfocaremos en trabajar con valores cercanos a 0.

Ahora, estudiaremos el comportamiento de ambas funciones en $x = 0$:
$$
\begin{align}
&f(0) = 0^{2} = 0 \\
&f'(0) = 2 \times 0 = 0
\end{align}
$$
$$
\begin{align}
&g(0) = 0 \times \sin(0) + \cos(0) = 0 + 1 = 1 \\
&g'(0) = 0 \times \cos(0) = 0
\end{align}
$$
Ahora, si estudiamos los extremos de ambas funciones, sabemos que 0 es un extremo (de hecho mínimo absoluto) de $f$, ya que $f'(0) = 0$. Ahora, para la función $g$, tenemos que buscar valores de $x$ para los cuales $g'(x) = 0$ (raíces de $g'$). Como es una función que oscila constantemente, nos centraremos en los extremos cercanos a 0.
$$
x \cos(x) = 0 \implies x = 0 \text{ o } \cos(x) = 0
$$
$\cos(x) = 0 \text{ si } x \in \left\{  k \pi - \frac{1}{2}\pi : k \in \mathbb{Z}  \right\}$.
De esta forma, sabemos que la función $g$ tiene dos extremos relativos en $-\frac{1}{2}\pi$ y $\frac{1}{2}\pi$. Si determinamos las imágenes en dichos puntos:
$$
\begin{align}
&g\left( -\frac{1}{2}\pi \right) = \left( -\frac{1}{2}\pi \right) \cdot \sin\left( -\frac{1}{2}\pi \right) + \cos\left( -\frac{1}{2}\pi \right) = \left( -\frac{1}{2}\pi \right) \cdot (-1) + 0 = \frac{1}{2} \pi \\
&g\left( \frac{1}{2}\pi \right) = \frac{1}{2}\pi \cdot \sin\left( \frac{1}{2}\pi \right) + \cos\left( \frac{1}{2}\pi \right) = \frac{1}{2}\pi \cdot 1 + 0 = \frac{1}{2} \pi
\end{align}
$$

Como vemos, ambos extremos son equivalentes. Ahora, sabiendo que estos son máximos relativos (ya que la función en 0 tiene como imagen a 1, siendo menor que $\frac{1}{2} \pi$, y este es el extremo relativo más cercano al que se encuentra en 0, que es un mínimo), a partir de los mismos, la función comienza a decrecer (a la izquierda de $-\frac{1}{2}\pi$ y a la derecha de $\frac{1}{2}\pi$).

Como determinamos donde se encuentran los extremos de $g$, sabemos que los siguientes extremos (en este caso, mínimos relativos) se encuentran en $-\frac{3}{2}\pi$ y $\frac{3}{2}\pi$. Esto también nos ayuda a visualizar que la función $g$ esta espejada con respecto al eje $y$.

Para este momento, ya estamos seguros de que la función $f$ "sobrepasó" a $g$, y como ambas son continuas, la tiene que haber cortado en como máximo dos puntos (por el comportamiento estudiado de dicha función).

Sabemos que la función $g$ decrece en $\left[ -\frac{1}{2}\pi, 0 \right]$ y crece en $\left[ 0, \frac{1}{2}\pi \right]$, siendo 0 un mínimo relativo y $g(0) = 1$, y $-\frac{1}{2}\pi$ y $\frac{1}{2}\pi$ máximos relativos, y $g\left( -\frac{1}{2}\pi \right) = g\left( \frac{1}{2}\pi \right) = \frac{1}{2} \pi$.

Como dijimos previamente, como la función $g$ comienza a decrecer a partir de este punto, hasta $-\frac{3}{2}\pi$ y $\frac{3}{2}\pi$, y las imágenes en dichos puntos son:
$$
\begin{align}
&g\left( -\frac{3}{2}\pi \right) = \left( -\frac{3}{2}\pi \right) \cdot \sin\left( -\frac{3}{2}\pi \right) + \cos\left( -\frac{3}{2}\pi \right) = \left( -\frac{3}{2}\pi \right) \cdot 1 + 0 = -\frac{3}{2} \pi \\
&g\left( \frac{3}{2}\pi \right) = \frac{3}{2}\pi \cdot \sin\left( \frac{3}{2}\pi \right) + \cos\left( \frac{3}{2}\pi \right) = \frac{3}{2}\pi \cdot (-1) + 0 = -\frac{3}{2} \pi
\end{align}
$$
Como vemos, son considerablemente menores que las imágenes de $-\frac{3}{2}\pi$ y $\frac{3}{2}\pi$ en $f$:
$$
\begin{align}
&f\left( -\frac{3}{2}\pi \right) = \left( -\frac{3}{2}\pi \right)^{2} = \frac{9}{4}\pi^{2} \\
&f\left( \frac{3}{2}\pi \right) = \left( \frac{3}{2}\pi \right)^{2} = \frac{9}{4}\pi^{2}
\end{align}
$$
De esta forma, confirmamos que la función $f$ sobrepasó a $g$ en algún momento, puesto que originalmente $g > f$ en un intervalo que incluye a 0, puesto que ambas funciones son continuas y derivables, y
$$
g(0) = 1 > f(0) = 0
$$

En conclusión, $g \cap f$ no es vacío y contiene dos elementos, o dicho de otra forma:
$$
x^{2} = x \sin(x) + \cos(x) \text{ tiene exactamente dos soluciones reales}
$$

---
## Ejercicio 6.6.6
$$
f(x) = \frac{x^{3}}{3} + \frac{x^{2}}{2} - 6x + 4
$$
### Parte a)
Sabemos que la inversa de una función se puede definir en un intervalo en el cual ningún punto tenga derivada nula, ya que cuando una función tiene un punto con derivada 0, la derivada de la función inversa en el mismo punto "tiende a infinito" (es vertical).

Por esta razón, analizaremos las raíces de la derivada:
$$
\left( \frac{x^{3}}{3} + \frac{x^{2}}{2} - 6x + 4 \right)' = \frac{\cancel{ 9 }x^{2}}{\cancel{ 9 }} + \frac{\cancel{ 4 }x}{\cancel{ 4 }} - 6 = x^{2} + x - 6
$$
Ahora, determinemos las raíces de la función $f'$:
$$
\begin{align}
&a = 1 \\
&b = 1 \\
&c = -6
\end{align}
$$
$$
\begin{align}
x &= \frac{-1 \pm \sqrt{ 1^{2} - 4 \cdot 1 \cdot (-6) }}{2 \cdot 1} \\
&= \frac{-1 \pm \sqrt{ 1 + 24 }}{2} \\
&= \frac{-1 \pm \sqrt{ 25 }}{2} \\
&= \frac{-1 \pm 5}{2}
\end{align}
$$
Ahora, estudiamos los dos valores posibles de $x$:
$$
\begin{align}
&x_{1} = \frac{-1 + 5}{2} = \frac{4}{2} = 2 \\
&x_{2} = \frac{-1 - 5}{2} = -\frac{6}{2} = -3
\end{align}
$$
De esta forma, sabemos que la función $f'(x) = x^{2} + x - 6$ tiene dos raíces reales, siendo 2 y -3.

Es así que el intervalo de longitud máxima que contenga al 0 en el que la función $g$ (inversa de $f$) esté definida, es el intervalo $(-3, 2)$.

### Parte b)
No graficamos la función, simplemente observamos la gráfica en GeoGebra. Como se trata de una parábola, la cual tiene raíces en -3 y 2, su vértice se encuentra en $-\frac{1}{2}$. Si calculamos la imagen en dicho punto, tenemos las coordenadas del vértice:
$$
g\left( -\frac{1}{2} \right) = \left( -\frac{1}{2} \right)^{2} + \left( -\frac{1}{2} \right) - 6 = \frac{1}{4} - \frac{1}{2} - 6 = -\frac{1}{4} - 6 = -6.25 = -\frac{25}{4}
$$

Ahora, calcularemos $g'(4)$:
$$
g'(x) = 2x + 1 \implies g'(4) = 2 \cdot 4 + 1 = 8 + 1 = 9
$$

---
## Ejercicio 6.6.10
### Parte a)
Tenemos que demostrar que, para todo $x > 0$,
$$
\frac{x}{x + 1} < \log(x + 1) < x
$$
Para esto, estudiaremos las derivadas de dichas funciones, que nos indicaran que tan rápido crecen las mismas:
$$
\begin{align}
&\left( \frac{x}{x + 1} \right)' = \frac{\cancel{ x } + 1 - \cancel{ x }}{(x + 1)^{2}} = \frac{1}{x^{2} + 2x + 1} \\
&(\log(x + 1))' = \frac{1}{x + 1} \cdot (x + 1)' = \frac{1}{x + 1} \\
&(x)' = 1
\end{align}
$$
Esto nos indica la velocidad de crecimiento de las funciones involucradas. Como vemos, $x$ tiene un crecimiento constante de 1, mientras que el resto de las funciones crecen cada vez más lento a medida que aumenta el valor de $x$ (la pendiente de la recta tangente es menor a medida que analizamos la derivada en un punto de mayor valor).

Podemos determinar, para todo $x > 0$, que:
$$
\frac{1}{x^{2} + 2x + 1} < \frac{1}{x + 1} < 1
$$

Ahora, sabiendo que estas son las derivadas de las funciones, simplemente determinemos el valor de las mismas para $x = 0$, y en caso de que cumpla con la igualdad o sea equivalente en las tres funciones, nos aseguraremos de que la desigualdad inicial es correcta:
$$
\begin{align}
&\frac{x}{x + 1} = \frac{0}{0 + 1} = \frac{0}{1} = 0 \\
&\log(x + 1) = \log(0 + 1) = \log(1) = 0 \\
&x = 0
\end{align}
$$
En conclusión, las tres funciones se interceptan en $(0, 0)$, y a partir de ahí son estrictamente crecientes, como lo indica su derivada. Además, la desigualdad de las derivadas coincide con la desigualdad de las funciones, por lo que la desigualdad es correcta.

### Parte b)
Tenemos que demostrar que, para todo $x, y \in \mathbb{R}$,
$$
|\sin (\alpha x) - \sin (\alpha y)| \leq |\alpha||x - y|
$$
Derivemos ambos lados de la desigualdad:
$$
\begin{align}
(|\sin (\alpha x) - \sin (\alpha y)|)' &\leq (|\alpha||x - y|)' \\
|\alpha \cos (\alpha x) - \alpha \cos (\alpha y)| &\leq 
\end{align}
$$



---
## Subsección 6.6.1 - Derivada segunda
#### Ejercicio 6.6.1.1
En base a la gráfica de la función, tenemos que considerar que:
- $f'$ indica la derivada de la función, por lo que $f'(x_{0})$ es igual a la pendiente de $f$ en $x_{0}$.
- $f''$ indica la derivada segunda de la función, por lo que $f''(x_{0})$ es igual a la pendiente de $f'$ en $x_{0}$, y representa la concavidad de la función $f$ en $x_{0}$.

Tenemos que observar el comportamiento de cada función cuando otras funciones se "aplanan" (su derivada es $0$ en dicho punto). Tomando como referencia esto, diría que:
- La función roja es $f$.
- La función azul es $f'$.
- La función rosa es $f''$.

Además, tomaría como referencia que la función rosa crece cuando la pendiente de la función roja crece a medida que avanza $x$, y decrece en caso contrario.

---
# 7 - Cálculo de extremos
## Ejercicio 6.7.1
Dos partes

En este caso, tenemos que determinar las raíces de la derivada de cada una de las funciones, así como el signo de la derivada para determinar si es mínimo o máximo.

### Parte a)
$$
f(x) = x^{3} + 3x + 1
$$
Derivamos la función:
$$
f'(x) = 3x^{2} + 3
$$
Determinamos las raíces de la función $f'$:
$$
\begin{align}
3x^{2} + 3 &= 0 \\
3x^{2} &= -3 \\
x^{2} &= -1 \implies \text{la función no tiene raíces reales}
\end{align}
$$
De esta forma, la derivada no tiene raíces reales. Por lo tanto, la función $f$ no tiene ningún punto para el cual la derivada sea 0.

### Parte b)
$$
f(x) = e^{-x^{2}}
$$
Derivamos la función:
$$
f'(x) = e^{-x^{2}} \times (-x^{2}) = -2xe^{-x^{2}}
$$
Determinamos las raíces de la función $f'$:
$$
-2xe^{-x^{2}} = 0
$$
Consideramos $x = 0$, puesto que el factor $e^{-x^{2}}$ nunca será 0 (no existe ningún valor de $x \in \mathbb{R}$ para el cual $\alpha^{x} = 0$, únicamente si $\alpha = 0$).
$$
-2 \times 0 \times e^{-0^{2}} = -2 \times 0 \times 1 = 0
$$
De esta forma, la función $f'$ tiene una raíz en 0, lo que indica que hay un extremo en dicho punto (y es el único extremo de la función).

Ahora, analizamos el signo de la función $f'$ para determinar si se trata de un máximo o un mínimo:

|  +  |     |  -  |
| :-: | :-: | :-: |
|     |  0  |     |
Simplemente estudiando la expresión, podemos ver que a mayor valor absoluto de $x$, la imagen será menor, puesto que $e^{-x^{2}} = \frac{1}{e^{x^{2}}}$. Por lo tanto, es el único extremo.

En conclusión, la función $f(x) = e^{-x^{2}}$ tiene máximo absoluto en $x = 0$ y vale 1.

---
## Ejercicio 6.7.2
Una parte por fila

En este caso, tenemos que estudiar la derivada y su signo en cada una de las funciones propuestas, pero centrándonos en el intervalo especificado.

### Parte a)
$$
f(x) = x^{3} - x^{2} - 8x + 1
$$
en el intervalo
$$
[-2, 1]
$$

Analizamos la derivada de la función $f$:
$$
f'(x) = 3x^{2} - 2x - 8
$$
Ahora, determinamos las raíces de $f'$:
$$
3x^{2} - 2x - 8 = 0
$$
$$
\begin{align}
&a = 3 \\
&b = -2 \\
&c = -8
\end{align}
$$
$$
\begin{align}
x &= \frac{2 \pm \sqrt{ (-2)^{2} - 4 \times 3 \times (-8) }}{2 \times 3} \\
&= \frac{2 \pm \sqrt{ 4 + 96 }}{6} \\
&= \frac{2 \pm \sqrt{ 100 }}{6} \\
&= \frac{2 \pm 10}{6}
\end{align}
$$
$$
\begin{align}
&x_{1} = \frac{2 + 10}{6} = \frac{12}{6} = 2 \\
&x_{2} = \frac{2 - 10}{6} = -\frac{8}{6} = -\frac{4}{3}
\end{align}
$$
Como vemos, la función $f'$ tiene dos raíces: 2 y $-\frac{4}{3}$.

El único extremo que entra en el intervalo considerado es $-\frac{4}{3}$. Ahora, estudiaremos el signo de $f'$ para determinar si se trata de un mínimo, un máximo o ninguno.

|  +  |                |  -  |     |  +  |
| :-: | :------------: | :-: | :-: | :-: |
|     | $-\frac{4}{3}$ |     |  2  |     |
En conclusión, la función tiene un máximo relativo en el intervalo $[-2, 1]$, en el punto $-\frac{4}{3}$.

### Parte d)
$$
f(x) = x^{10} + x^{9} + 10
$$
en el intervalo
$$
[-2, 2]
$$

Analizamos la derivada de la función $f$:
$$
f'(x) = 10x^{9} + 9x^{8}
$$
Ahora, determinamos las raíces de $f'$:
$$
10x^{9} + 9x^{8} = 0
$$
Sabemos que $x = 0$ satisface la ecuación anterior. Por lo tanto, 0 es raíz de $f'$.

Ahora, veamos si la función tiene más raíces. En caso de tener más raíces, tienen que ser para valores negativos, ya que la función es estrictamente creciente para valores $x \geq 0$.
$$
\begin{align}
10x^{9} + 9x^{8} &= 0 \\
10x^{9} &= -9x^{8} \\
10x\cancel{ x^{8} } &= -9\cancel{ x^{8} } \\
10x &= -9 \\
x &= -\frac{9}{10}
\end{align}
$$
Otra raíz de $f'$ es $-\frac{9}{10}$. Ahora, nos queda analizar el signo de la función, para terminar de entender si dichas raíces son extremos o no, y que tipo de extremos son.

|  -  |                 |  +  |     |  +  |
| :-: | :-------------: | :-: | :-: | :-: |
|     | $-\frac{9}{10}$ |     |  0  |     |
De esta manera, determinamos que, si bien $f$ tiene derivada 0 en $-\frac{9}{10}$ y 0, solo $-\frac{9}{10}$ es un extremo, ya que la función cambia de signo en dicho punto. Además, podemos determinar que es absoluto, ya que se trata de un polinomio de grado par.

En conclusión, la función tiene un mínimo absoluto en el intervalo $[-2, 2]$, en el punto $-\frac{4}{3}$.

### Parte e)
$$
f(x) = \frac{x + 1}{x^{2} + 1}
$$
en el intervalo
$$
\left[ -1, \frac{1}{2} \right]
$$

Analizamos la derivada de la función $f$:
$$
f'(x) = \frac{(x + 1)'(x^{2} + 1) - (x + 1)(x^{2} + 1)'}{(x^{2} + 1)^{2}} = \frac{(x^{2} + 1) - (x + 1)(2x)}{(x^{2} + 1)^{2}} = \frac{x^{2} + 1 - 2x^{2} - 2x}{(x^{2} + 1)^{2}}
$$
$$
= \frac{-x^{2} - 2x + 1}{x^{4} + 2x^{2} + 1}
$$
Ahora, determinamos las raíces de $f'$. Básicamente, tenemos que estudiar:
$$
-x^{2} - 2x + 1 = 0
$$
$$
\begin{align}
&a = -1 \\
&b = -2 \\
&c = 1
\end{align}
$$
$$
\begin{align}
x &= \frac{2 \pm \sqrt{ (-2)^{2} - 4 \times (-1) \times 1 }}{2 \times (-1)} \\
&= \frac{2 \pm \sqrt{ 4 + 4 }}{-2} \\
&= -\frac{2 \pm \sqrt{ 8 }}{2} \\
&= -\frac{2 \pm 2\sqrt{ 2 }}{2}
\end{align}
$$
$$
\begin{align}
&x_{1} = -\frac{2 + 2\sqrt{ 2 }}{2} = -1 - \sqrt{ 2 } \\
&x_{2} = -\frac{2 - 2\sqrt{ 2 }}{2} = -1 + \sqrt{ 2 }
\end{align}
$$
De estos dos valores, el único que entra en el intervalo $\left[ -1, \frac{1}{2} \right]$ es $x_{2} = \sqrt{ 2 } - 1$

Ahora, analicemos el signo de la función:

| -   |                    | +   |                  | -   |
| --- | ------------------ | --- | ---------------- | --- |
|     | $- \sqrt{ 2 } - 1$ |     | $\sqrt{ 2 } - 1$ |     |
De esta forma, la función tiene un extremo en el intervalo $\left[ -1, \frac{1}{2} \right]$, en $\sqrt{ 2 } - 1$. Además, determinamos que se trata de un máximo ya que su derivada crece a la izquierda y decrece a la derecha, y podemos decir que es absoluto, ya que por la naturaleza de la función, a partir de este punto, decrece a la izquierda y a la derecha (las imágenes son menores).

En conclusión, la función tiene un máximo absoluto en el intervalo $\left[ -1, \frac{1}{2} \right]$, en el punto $\sqrt{ 2 } - 1$.

### Parte f)
$$
f(x) = \frac{x}{x^{2} + 1}
$$
en el intervalo
$$
\left[ 0, 5 \right]
$$

Analizamos la derivada de la función $f$:
$$
\begin{align}
f'(x) &= \left( \frac{x}{x^{2} + 1} \right)' \\
&= \frac{(x)'x^{2} + 1 - x(x^{2} + 1)'}{(x^{2} + 1)^{2}} \\
&= \frac{x^{2} + 1 - 2x^{2}}{(x^{2} + 1)^{2}} \\
&= \frac{-x^{2} + 1}{(x^{2} + 1)^{2}} \\
&= \frac{-x^{2} + 1}{x^{4} + 2x^{2} + 1}
\end{align}
$$
Ahora, determinamos las raíces de $f'$. Básicamente, tenemos que estudiar:
$$
-x^{2} + 1 = 0
$$
$$
\begin{align}
&a = -1 \\
&b = 0 \\
&c = 1
\end{align}
$$
$$
\begin{align}
x &= \frac{0 \pm \sqrt{ 0^{2} - 4 \times (-1) \times 1 }}{2 \times (-1)} \\
&= \frac{0 \pm \sqrt{ 0 + 4 }}{-2} \\
&= -\frac{0 \pm \sqrt{ 4 }}{2} \\
&= -\frac{0 \pm 2}{2}
\end{align}
$$
$$
\begin{align}
&x_{1} = -\frac{0 + 2}{2} = -1 \\
&x_{2} = -\frac{0 - 2}{2} = 1
\end{align}
$$
De estos dos valores, el único que entra en el intervalo $\left[ 0, 5 \right]$ es $x_{2} = 1$

Ahora, analicemos el signo de la función:

|  -  |     |  +  |     |  -  |
| :-: | :-: | :-: | :-: | :-: |
|     | -1  |     |  1  |     |
De esta forma, la función tiene un extremo en el intervalo $\left[ 0, 5 \right]$, en 1. Además, determinamos que se trata de un máximo ya que su derivada crece a la izquierda y decrece a la derecha, y podemos decir que es absoluto, ya que por la naturaleza de la función (se trata de una función cuyo denominador crece mucho más rápido que el numerador), a partir de este punto, decrece a la izquierda y a la derecha (las imágenes son menores).

Podemos determinar la imagen de la función en dicho punto:
$$
f(1) = \frac{1}{1^{2} + 1} = \frac{1}{2}
$$
En conclusión, la función tiene un máximo absoluto en el intervalo $\left[ 0, 5 \right]$, en el punto 1, y su valor es de $\frac{1}{2}$.



---
## Ejercicio 6.7.3
Una parte

### Parte d)
$$
f(x) = 48\cos ^{5}(x) - 80\cos ^{3}(x) + 45\cos(x)
$$
Analizamos la derivada de la función $f$:
$$
f'(x) = 48 \times 5 \times \cos ^{4}(x) \times (-\sin (x)) - 80 \times 3 \times \cos ^{2}(x) \times (-\sin (x)) + 45 \times (-\sin(x))
$$
$$
= -240 \cos ^{4}(x) \sin (x) + 240 \cos ^{2}(x) \sin (x) - 45 \sin(x)
$$
$$
= -\sin(x)(240 \cos ^{4}(x) - 240 \cos ^{2}(x) + 45)
$$
Ahora, determinamos las raíces de $f'$. Básicamente, tenemos que estudiar para que valores de $x$ $\sin(x) = 0$ y $240 \cos ^{4}(x) - 240 \cos ^{2}(x) + 45 = 0$. Sabemos que $\sin(x) = 0$ cuando $x \in \{ k \pi : k \in \mathbb{Z} \}$. Estos valores indican que hay extremos cuando $\cos(x) = \pm 1$.

Para facilitar las operaciones, lo que haremos será transformar $240 \cos ^{4}(x) - 240 \cos ^{2}(x) + 45 = 0$ en un polinomio tradicional, manejado $\cos(x)$ como una nueva variable $u$:
$$
240 \cos ^{4}(x) - 240 \cos ^{2}(x) + 45 = 0 \implies 240 u^{4} - 240 u^{2} + 45 = 0
$$
Además, manejaremos una segunda variable $v = u^{2}$, para tener un polinomio de segundo grado y poder calcular sus raíces fácilmente:
$$
240 u^{4} - 240 u^{2} + 45 = 0 \implies 240 v^{2} - 240 v + 45 = 0
$$
Ahora, determinamos las raíces con Bhaskara:
$$
\begin{align}
&a = 240 \\
&b = -240 \\
&c = 45
\end{align}
$$
$$
\begin{align}
v &= \frac{240 \pm \sqrt{ (-240)^{2} - 4 \times 240 \times 45 }}{2 \times 240} \\
&= \frac{240 \pm \sqrt{ 57600 - 43200 }}{480} \\
&= \frac{240 \pm \sqrt{ 14400 }}{480} \\
&= \frac{240 \pm 120}{480}
\end{align}
$$
$$
\begin{align}
&v_{1} = \frac{240 + 120}{480} = \frac{360}{480} = \frac{3}{4} \\
&v_{2} = \frac{240 - 120}{480} = \frac{120}{480} = \frac{1}{4}
\end{align}
$$
De esta forma:
$$
\begin{align}
&u_{1} = \sqrt{ \frac{3}{4} } = \pm\frac{\sqrt{ 3 }}{2} \\
&u_{2} = \sqrt{ \frac{1}{4} } = \pm\frac{1}{2}
\end{align}
$$
Es así que los puntos $\pm \frac{\sqrt{ 3 }}{2}$ y $\pm \frac{1}{2}$.
Ahora, necesitamos determinar para que valores de $x$, $\cos(x) = \pm \frac{\sqrt{ 3 }}{2}$ y $\cos(x) = \pm\frac{{1}}{2}$.

Sabemos que $\cos\left( \frac{\pi}{3} \right) = \frac{1}{2}$. Por lo tanto, en base al círculo trigonométrico, consideraremos el conjunto:
$$
\begin{align}
\cos(x) &= \frac{1}{2} \Longleftrightarrow x \in \left\{  \frac{\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{5\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\} \\
&= -\frac{1}{2} \Longleftrightarrow x \in \left\{  \frac{2\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{4\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\}
\end{align}
$$
Ahora, también sabemos que $\cos()$. Por lo tanto, en base al círculo trigonométrico, consideraremos el conjunto:
$$
\begin{align}
\cos(x) &= \frac{\sqrt{ 3 }}{2} \Longleftrightarrow x \in \left\{  \frac{\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{11\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\} \\
&= -\frac{\sqrt{ 3 }}{2} \Longleftrightarrow x \in \left\{  \frac{5\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{7\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\}
\end{align}
$$

Entonces, podemos concluir que la función tiene extremos en todos los valores de $x$ que pertenecen al cojunto:
$$
\begin{align}
&\{ k \pi : k \in \mathbb{Z} \} \\
\cup \space &\left\{  \frac{\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{5\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\}
\cup \left\{  \frac{2\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{4\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\} \\
\cup \space &\left\{  \frac{\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{11\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\}
\cup \left\{  \frac{5\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{7\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\}
\end{align}
$$
Ahora, determinemos cuales de estos puntos son máximos y mínimos, tomando en cuenta la función $f(x) = 48\cos ^{5}(x) - 80\cos ^{3}(x) + 45\cos(x)$:
$$
\begin{align}
\cos(x) = 1 \implies &48 - 80 + 45 = 13 \\
\cos(x) = -1 \implies &-48 + 80 - 45 = -13 \\
\cos(x) = \frac{1}{2} \implies &48\left( \frac{1}{32} \right) - 80\left( \frac{1}{8} \right) + 45\left( \frac{1}{2} \right) = \frac{3}{2} - 10 + \frac{45}{2} = 24 - 10 = 14 \\
\cos(x) = -\frac{1}{2} \implies &-48\left( \frac{1}{32} \right) + 80\left( \frac{1}{8} \right) - 45\left( \frac{1}{2} \right) = -\frac{3}{2} + 10 - \frac{45}{2} = -24 + 10 = -14 \\
\cos(x) = \frac{\sqrt{ 3 }}{2} \implies &48\left( \frac{9\sqrt{ 3 }}{32} \right) - 80\left( \frac{3\sqrt{ 3 }}{8} \right) + 45\left( \frac{\sqrt{ 3 }}{2} \right) = \frac{27\sqrt{ 3 }}{2} - 30\sqrt{ 3 } + \frac{45\sqrt{ 3 }}{2} = \frac{72\sqrt{ 3 } - 60\sqrt{ 3 }}{2} = \frac{12\sqrt{ 3 }}{2} = 6\sqrt{ 3 } \\
\cos(x) = -\frac{\sqrt{ 3 }}{2} \implies &-48\left( \frac{9\sqrt{ 3 }}{32} \right) + 80\left( \frac{3\sqrt{ 3 }}{8} \right) - 45\left( \frac{\sqrt{ 3 }}{2} \right) = -\frac{27\sqrt{ 3 }}{2} + 30\sqrt{ 3 } - \frac{45\sqrt{ 3 }}{2} = \frac{-72\sqrt{ 3 } + 60\sqrt{ 3 }}{2} = -\frac{12\sqrt{ 3 }}{2} = -6\sqrt{ 3 }
\end{align}
$$

Por la naturaleza oscilante de la función, estamos seguros de que dichos puntos son extremos.

En conclusión, la función tiene
- máximos absolutos en
$$
x \in \left\{  \frac{\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{5\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\}
$$
- mínimos absolutos en
$$
x \in \left\{  \frac{2\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{4\pi}{3} + 2k\pi : k \in \mathbb{Z} \right\}
$$
- máximos relativos en
$$
x \in \{ 2k \pi : k \in \mathbb{Z} \} \cup \left\{  \frac{\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{11\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\}
$$
- mínimos relativos en
$$
x \in \{ k \pi : k \in \mathbb{Z} \} \setminus \{ 2k \pi : k \in \mathbb{Z} \} \cup \left\{  \frac{5\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\} \cup \left\{  \frac{7\pi}{6} + 2k\pi : k \in \mathbb{Z} \right\}
$$

---
# 8 - Optimización en problemas geométricos

### Ejercicio 6.8.1
Dos partes

#### Parte b)
Sabemos que el área de un rectángulo está dada por
$$
A = b \times h
$$
siendo $b$ la medida de la base y $h$ la altura del mismo.

También sabemos que el perímetro se determina como:
$$
P = 2b + 2h
$$

Comencemos por encontrar el rectángulo de menor perímetro cuya área es 4.
Tenemos que analizar la función perímetro como una función que depende únicamente de una variable en lugar de dos.

Por esta razón, y sabiendo que el área es 4, podemos expresar la altura como:
$$
A = b \times h = 4 \implies h = \frac{4}{b}
$$
Ahora, sustituimos dicho valor en la fórmula del perímetro:
$$
\begin{align}
P = 2b + 2h \implies P &= 2b + 2\left( \frac{4}{b} \right) \\
&= 2b + \frac{8}{b}
\end{align}
$$
De esta forma, tenemos la siguiente función:
$$
P(b) = 2b + \frac{8}{b}
$$
Ahora, derivamos la función y analizaremos las raíces de la derivada, buscando algún mínimo absoluto:
$$
P'(b) = 2 - \frac{8}{b^{2}}
$$
Analizando la función, podemos ver que la misma se anula cuando $\frac{8}{b^{2}} = 2$

Es así que consideramos $b^{2} = 4 \implies b = \sqrt{ 4 } = \pm2$.

Como se trata de una longitud, consideramos el valor 2 positivo.

Ahora, analizamos el signo de $f'$:

|  -  |     |  +  |
| :-: | :-: | :-: |
|     |  2  |     |
De esta forma, podemos ver que 2 es un mínimo absoluto de la función $P$.

En conclusión, el rectángulo de menor perímetro cuya área es 4 es un cuadrado de lado 2.


Ahora, hagamos lo mismo, pero para hallar el rectángulo de mayor área cuyo perímetro es 8.

Sabemos que:
$$
\begin{align}
P = 2b + 2h = 8 \implies &2h = 8 - 2b \\
&h = \frac{8 - 2b}{2} \\
&h = 4 - b
\end{align}
$$
Ahora, sustituimos el valor de $h$ por $4 - b$ en la fórmula del área:
$$
\begin{align}
A = b \times h \implies A &= b \times (4 - b) \\
&= 4b - b^{2}
\end{align}
$$
De esta forma, tenemos la siguiente función:
$$
A(b) = 4b - b^{2}
$$
Ahora, derivamos la función y analizaremos las raíces de la derivada, buscando algún mínimo absoluto:
$$
A'(b) = 4 - 2b
$$
Analizando la función, podemos ver que la misma se anula cuando $2b = 4$

Es así que consideramos $2b = 4 \implies b = \frac{4}{2} = 2$.

Ahora, analizamos el signo de $f'$:

|  +  |     |  -  |
| :-: | :-: | :-: |
|     |  2  |     |
De esta forma, podemos ver que 2 es un máximo absoluto de la función $P$.

En conclusión, el rectángulo de mayor área cuyo perímetro es 8 es un cuadrado de lado 2.

#### Parte c)

Tenemos que hallar el triángulo de menor perímetro cuya área es 4.

Sabemos que el área de un triángulo se determina mediante la fórmula:
$$
A = \frac{b \times h}{2}
$$
siendo $b$ la medida de la base y $h$ la altura del mismo.

También sabemos que el perímetro se determina como:
$$
P = a + b + c
$$
Siendo $a, b, c$ las medidas de sus lados.

Ahora, tomando la fórmula del área, expresemos la altura en base a $b$, sabiendo que el área es 4:
$$
\begin{align}
A = \frac{b \times h}{2} = 4 \implies &b \times h = 4 \times 2 = 8 \\
&b = \frac{8}{h}
\end{align}
$$
Ahora, sustituimos el valor de $b$ por $\frac{2}{h}$ en la fórmula del perímetro:
$$
P = a + b + c \implies P = a + \frac{8}{h} + c
$$
De esta forma, tenemos la siguiente función:
$$
P(h) = a + \frac{8}{h} + c
$$
Sin embargo, esta expresión tiene un problema: depende de más de una variable. Por lo tanto, realizaremos las siguientes consideraciones:
- Para un área fija ($b$ y $h$ fijas), el triángulo que minimiza el perímetro es siempre el isósceles. Por lo tanto, los lados $a$ y $c$ deben ser iguales ($a = c$).
- En un triángulo isósceles si trazamos la altura $h$ sobre la base $b$, formamos dos triángulos rectángulos de base $\frac{b}{2}$. Por el teorema de Pitágoras:
$$
a = c = \sqrt{ h^{2} + \left( \frac{b}{2} \right)^{2} }
$$
Considerando todo lo anterior, podemos formular nuevamente la función del perímetro del triángulo:
$$
\begin{align}
P(h) &= \frac{8}{h} + 2\sqrt{ h^{2} + \left( \frac{8}{2h} \right)^{2} } \\
&= \frac{8}{h} + 2\sqrt{ h^{2} + \frac{64}{4h^{2}} } \\
&= \frac{8}{h} + 2\sqrt{ h^{2} + \frac{16}{h^{2}} }
\end{align}
$$
Ahora, derivamos la función y analizaremos las raíces de la derivada, buscando algún mínimo absoluto:
$$
P'(h) = -\frac{8}{h^{2}} + \frac{\cancel{ 2 }}{\cancel{ 2 }\sqrt{ h^{2} + \frac{16}{h^{2}} }} \times \left( h^{2} + \frac{16}{h^{2}} \right)'
$$
$$
\begin{align}
\left( h^{2} + \frac{16}{h^{2}} \right)' &= 2h - \frac{16 \times (h^{2})'}{(h^{2})^{2}} = 2h - \frac{32h}{h^{4}} = 2h - \frac{32}{h^{3}}
\end{align}
$$
$$
\begin{align}
\implies P'(h) &= -\frac{8}{h^{2}} + \frac{1}{\sqrt{ h^{2} + \frac{16}{h^{2}} }} \times \left( 2h - \frac{32}{h^{3}} \right) \\
&= -\frac{8}{h^{2}} + \frac{2h - \frac{32}{h^{3}}}{\sqrt{ h^{2} + \frac{16}{h^{2}} }}
\end{align}
$$
Ahora, analizamos las raíces de dicha función:
$$
\begin{align}
-\frac{8}{h^{2}} + \frac{2h - \frac{32}{h^{3}}}{\sqrt{ h^{2} + \frac{16}{h^{2}} }} &= 0 \\
\frac{2h - \frac{32}{h^{3}}}{\sqrt{ h^{2} + \frac{16}{h^{2}} }} &= \frac{8}{h^{2}} \\
h^{2} \left( 2h - \frac{32}{h^{3}} \right) &= 8 \sqrt{ h^{2} + \frac{16}{h^{2}} } \\
\left( h^{2} \left( 2h - \frac{32}{h^{3}} \right) \right)^{2} &= \left( 8 \sqrt{ h^{2} + \frac{16}{h^{2}} } \right)^{2} \\
h^{4} \left( 4h^{2} - \frac{128}{h^{2}} + \frac{1024}{h^{6}} \right) &= 64 \left( h^{2} + \frac{16}{h^{2}} \right) \\
4h^{6} - 128h^{2} + \cancel{ \frac{1024}{h^{2}} } &= 64 h^{2} + \cancel{ \frac{1024}{h^{2}} } \\
4h^{6} - 192h^{2} &= 0 \\
h^{2}(4h^{4} - 192) &= 0
\end{align}
$$
De esta forma:
$$
h^{2} = 0 \implies h = 0 \qquad \text{Caso inválido}
$$
$$
\begin{align}
4h^{4} - 192 = 0 \implies &4h^{4} = 192 \\
&h^{4} = \frac{192}{4} \\
&h^{4} = 48 \\
&h = \sqrt[4]{ 48 } \\
&h = \sqrt[4]{ 2 \cdot 2 \cdot 2 \cdot 2 \cdot 3 } \\
&h = 2\sqrt[4]{ 3 }
\end{align}
$$
Determinamos que $2\sqrt[4]{ 3 }$ es raíz de la función. Ahora, estudiemos el signo de la función $f'$:


|  -  |                  |  +  |
| :-: | :--------------: | :-: |
|     | $2\sqrt[4]{ 3 }$ |     |
De esta forma, podemos ver que 2 es un mínimo absoluto de la función $P$.

Ahora, sabiendo el valor de $h$, obtenemos el valor de $b$ en base a la fórmula del área:
$$
\begin{align}
A = \frac{b \times h}{2} = 4 \implies &\frac{b \times \cancel{ 2 }\sqrt[4]{ 3 }}{\cancel{ 2 }} = 4 \\
&b \times \sqrt[4]{ 3 } = 4 \\
&b = \frac{4}{\sqrt[4]{ 3 }} \\
&
\end{align}
$$
Ahora, calculamos el resto de los lados:
$$
\begin{align}
a = c = \sqrt{ h^{2} + \left( \frac{b}{2} \right)^{2} } \implies a = c = &\sqrt{ (2\sqrt[4]{ 3 })^{2} + \left( \frac{\frac{4}{\sqrt[4]{ 3 }}}{2} \right)^{2} } \\
&\sqrt{ 4\sqrt{ 3 } + \frac{\frac{16}{\sqrt{ 3 }}}{4} } \\
&\sqrt{ 4\sqrt{ 3 } + \frac{16}{4\sqrt{ 3 }} } \\
&\sqrt{ 4\sqrt{ 3 } + \frac{4}{\sqrt{ 3 }} } \\
&\sqrt{ \frac{4\sqrt{ 3 } \cdot \sqrt{ 3 } + 4}{\sqrt{ 3 }} } \\
&\sqrt{ \frac{4 \cdot 3 + 4}{\sqrt{ 3 }} } \\
&\sqrt{ \frac{12 + 4}{\sqrt{ 3 }} } \\
&\sqrt{ \frac{16}{\sqrt{ 3 }} } \\
&\frac{4}{\sqrt[4]{ 3 }}
\end{align}
$$

En conclusión, el triángulo de menor perímetro cuya área es 4 es un triángulo equilátero de lado $\frac{4}{\sqrt[4]{ 3 }}$.

---
### Ejercicio 6.8.2

La idea será expresar todo en función a los valores $a$ y $b$, que son valores conocidos.

En lugar de usar una recta genérica (y ecuaciones genéricas en general), tomaremos el siguiente enfoque:
- Utilizaremos como centro del círculo el punto $(0, 0)$ (como dijimos anteriormente).
- Consideraremos la recta $L$ $y = b$ (donde $0 \leq b < a$). De esta manera:
	- La ecuación de la circunferencia es $x^{2} + y^{2} = a^{2}$
	- La recta $L$ divide al círculo en dos secciones:
		- Sección menor: donde $b \leq y \leq a$
		- Sección mayor: donde $-a \leq y \leq b$

En ambas secciones, el rectángulo correspondiente se "apoyará" sobre la recta $L$.

Comencemos por la sección menor.

Aquí, el rectángulo tendrá altura $h = y - b$ (sabemos que dicho valor es positivo ya que el rectángulo tendrá sus vértices inferiores en la recta $y = b$, y superiores en alguna recta $y > b$).

Luego, si estudiamos la base del mismo, esta dada por la variable $x$. Podemos decir con seguridad que será $2x$, ya que tenemos que considerar que el rectángulo tendrá una mitad de la base del lado positivo y la otra del lado negativo.
Considerando la fórmula de la circunferencia, podemos decir que la base del rectángulo más pequeño está dada por $x = \sqrt{ a^{2} - y^{2} } \implies b = 2\sqrt{ a^{2} - y^{2} }$

Con estos datos, ya podemos definir la primera función a maximizar:
$$
A_{1}(y) = \underbrace{ (y - b) }_{ h } \cdot \underbrace{ 2\sqrt{ a^{2} - y^{2} } }_{ b } = 2 (y - b) \sqrt{ a^{2} - y^{2} }
$$
para $y \in [b, a]$.

Prosigamos por la sección mayor.

Aquí hay que considerar lo siguiente:
Si $b$ es lo significantemente grande, el rectángulo de mayor área podría ser simplemente el cuadrado inscrito en el círculo completo.

En dicho caso, el lado del cuadrado es simplemente el diámetro del círculo multiplicado por $\frac{\sqrt{ 2 }}{2}$ (en este caso es $\frac{2a\sqrt{ 2 }}{2} = a\sqrt{ 2 }$. De esta forma, sabemos que tiene vértices en $y = \pm \frac{a\sqrt{ 2 }}{2} = \pm \frac{a}{\sqrt{ 2 }}$.


Aquí, el rectángulo tendrá altura $h = b - y$ (sabemos que dicho valor es positivo ya que el rectángulo tendrá sus vértices superiores en la recta $y = b$, e inferiores en alguna recta $y < b$).

Si estudiamos la base de dicho rectángulo, también será $2x$, llevando a la misma fórmula $b = 2\sqrt{ a^{2} - y^{2} }$.

De esta forma, la segunda función a maximizar es:
$$
A_{2}(y) = \underbrace{ (b - y) }_{ h } \cdot \underbrace{ 2\sqrt{ a^{2} - y^{2} } }_{ b } = 2 (b - y) \sqrt{ a^{2} - y^{2} }
$$
para $y \in [-a, b]$.

Ahora, para encontrar los máximos absolutos de cada función, tenemos que derivar ambas.

Primeramente, hagámoslo con el área menor:
$$
\begin{align}
(A_{1}(y))' &= (2 (y - b) \sqrt{ a^{2} - y^{2} })' \\
&= (2 (y - b))' \cdot \sqrt{ a^{2} - y^{2} } + 2 (y - b) \cdot (\sqrt{ a^{2} - y^{2} })' \\
&= 2 \sqrt{ a^{2} - y^{2} } + 2 (y - b) \cdot \frac{1}{2 \sqrt{ a^{2} - y^{2} }} \cdot (a^{2} - y^{2})' \\
&= 2 \sqrt{ a^{2} - y^{2} } + 2 (y - b) \cdot \frac{1}{2 \sqrt{ a^{2} - y^{2} }} \cdot (-2y) \\
&= 2 \sqrt{ a^{2} - y^{2} } + 2 (y - b) \cdot \frac{-\cancel{ 2 }y}{\cancel{ 2 } \sqrt{ a^{2} - y^{2} }} \\
&= 2 \sqrt{ a^{2} - y^{2} } + 2 (y - b) \cdot \frac{-y}{\sqrt{ a^{2} - y^{2} }} \\
&= \frac{2 (a^{2} - y^{2}) - 2y (y - b)}{\sqrt{ a^{2} - y^{2} }} \\
&= \frac{2a^{2} - 2y^{2} - 2y^{2} + 2yb}{\sqrt{ a^{2} - y^{2} }} \\
&= \frac{2a^{2} - 4y^{2} + 2yb}{\sqrt{ a^{2} - y^{2} }}
\end{align}
$$

Continuamos con el área mayor:
$$
\begin{align}
(A_{2}(y))' &= (2 (b - y) \sqrt{ a^{2} - y^{2} })' \\
&= (2 (b - y))' \cdot \sqrt{ a^{2} - y^{2} } + 2 (b - y) \cdot (\sqrt{ a^{2} - y^{2} })' \\
&= -2 \sqrt{ a^{2} - y^{2} } + 2 (b - y) \cdot \frac{1}{2 \sqrt{ a^{2} - y^{2} }} \cdot (a^{2} - y^{2})' \\
&= -2 \sqrt{ a^{2} - y^{2} } + 2 (b - y) \cdot \frac{1}{2 \sqrt{ a^{2} - y^{2} }} \cdot (-2y) \\
&= -2 \sqrt{ a^{2} - y^{2} } + 2 (b - y) \cdot \frac{-\cancel{ 2 }y}{\cancel{ 2 } \sqrt{ a^{2} - y^{2} }} \\
&= -2 \sqrt{ a^{2} - y^{2} } + 2 (b - y) \cdot \frac{-y}{\sqrt{ a^{2} - y^{2} }} \\
&= \frac{-2 (a^{2} - y^{2}) - 2y (b - y)}{\sqrt{ a^{2} - y^{2} }} \\
&= \frac{-2a^{2} + 2y^{2} - 2yb + 2y^{2}}{\sqrt{ a^{2} - y^{2} }} \\
&= \frac{-2a^{2} + 4y^{2} - 2yb}{\sqrt{ a^{2} - y^{2} }}
\end{align}
$$

Como vemos, ambas derivadas son opuestas. Además, como se trata de un cociente, la función tiene raíces cuando el numerador se anula.

Primero, estudiamos la sección menor:
$$
\begin{align}
\frac{2a^{2} - 4y^{2} + 2yb}{\sqrt{ a^{2} - y^{2} }} = 0 &\implies 2a^{2} - 4y^{2} + 2yb = 0 \\
&\implies -2y^{2} + yb + a^{2} = 0
\end{align}
$$
$$
\begin{align}
&a = -2 \\
&b = b \\
&c = a^{2}
\end{align}
$$
$$
\begin{align}
y &= \frac{-b \pm \sqrt{ (b)^{2} - 4 \cdot (-2) \cdot a^{2} }}{2 \cdot (-2)} \\
&= \frac{-b \pm \sqrt{ b^{2} + 8a^{2} }}{-4} \\
&= \frac{b \mp \sqrt{ b^{2} + 8a^{2} }}{4}
\end{align}
$$
Ahora, analicemos los posibles valores de $y$:
$$
\begin{align}
&y_{1} = \frac{b - \sqrt{ b^{2} + 8a^{2} }}{4} \\
&y_{2} = \frac{b + \sqrt{ b^{2} + 8a^{2} }}{4}
\end{align}
$$
Sabemos que $b < a$, por lo que $b < \sqrt{ b^{2} + 8a^{2} }$. Por lo tanto $y_{1} < 0$. De esta forma, nos quedamos con $y_{2}$, valor que es siempre positivo.

Si analizamos el signo de la función $A_{1}'$:

|  +  |                                         |  -  |
| :-: | :-------------------------------------: | :-: |
|     | $\frac{b + \sqrt{ b^{2} + 8a^{2} }}{4}$ |     |
Lo sabemos, ya que el numerador de la derivada representa una parábola cóncava hacia abajo.

Ahora, pasamos a estudiar la sección mayor:
$$
\begin{align}
\frac{-2a^{2} + 4y^{2} - 2yb}{\sqrt{ a^{2} - y^{2} }} = 0 &\implies -2a^{2} + 4y^{2} - 2yb \\
&\implies 2y^{2} - yb - a^{2} = 0
\end{align}
$$
$$
\begin{align}
&a = 2 \\
&b = -b \\
&c = -a^{2}
\end{align}
$$
$$
\begin{align}
y &= \frac{b \pm \sqrt{ (-b)^{2} - 4 \cdot 2 \cdot (-a^{2}) }}{2 \cdot 2} \\
&= \frac{b \pm \sqrt{ b^{2} + 8a^{2} }}{4} \\
\end{align}
$$
Si analizamos los posibles valores de $y$, podemos notar que son equivalentes a los vistos en el caso anterior:
$$
\begin{align}
&y_{1} = \frac{b + \sqrt{ b^{2} + 8a^{2} }}{4} \\
&y_{2} = \frac{b - \sqrt{ b^{2} + 8a^{2} }}{4}
\end{align}
$$
Sin embargo, aquí tenemos que considerar dos casos:
- Cuadrado inscrito en el círculo completo: en el caso de que $b$ sea lo suficientemente grande ($b \geq \frac{a}{\sqrt{ 2 }}$), entonces el rectángulo de mayor área queda contenido íntegramente dentro de la sección mayor.
- Rectángulo "apoyado" en $L$: en este caso, el extremo se daría en la raíz negativa $y_{2}$, y es un valor válido, puesto que $y_{2} > -a$ en todos los casos.

Si analizamos el signo de la función $A_{2}'$:

|  +  |                                         |  -  |
| :-: | :-------------------------------------: | :-: |
|     | $\frac{b - \sqrt{ b^{2} + 8a^{2} }}{4}$ |     |
De esta forma, se trata de un máximo absoluto.

Ahora, nos queda calcular el valor de la altura y la base. Comencemos por la sección menor, la cual no distingue entre casos:
$$
\begin{align}
h &= y - b \\
&= \frac{b + \sqrt{ b^{2} + 8a^{2} }}{4} - b \\
&= \frac{b + \sqrt{ b^{2} + 8a^{2} } - 4b}{4} \\
&= \frac{-3b + \sqrt{ b^{2} + 8a^{2} }}{4}
\end{align}
$$
$$
\begin{align}
2x &= 2\sqrt{ a^{2} - y^{2} } \\
&= 2\sqrt{ a^{2} - \left( \frac{b + \sqrt{ b^{2} + 8a^{2} }}{4} \right)^{2} } \\
&= 2\sqrt{ a^{2} - \frac{b^{2} + 2b\sqrt{ b^{2} + 8a^{2} } + b^{2} + 8a^{2}}{16} } \\
&= 2\sqrt{ a^{2} - \frac{2b^{2} + 2b\sqrt{ b^{2} + 8a^{2} } + 8a^{2}}{16} } \\
&= 2\sqrt{ a^{2} - \frac{b^{2} + b\sqrt{ b^{2} + 8a^{2} } + 4a^{2}}{8} } \\
&= 2\sqrt{ \frac{8a^{2} - b^{2} - b\sqrt{ b^{2} + 8a^{2} } - 4a^{2}}{8} } \\
&= 2\sqrt{ \frac{4a^{2} - b^{2} - b\sqrt{ b^{2} + 8a^{2} }}{8} } \\
&= \sqrt{ 4 \cdot \frac{4a^{2} - b^{2} - b\sqrt{ b^{2} + 8a^{2} }}{8} } \\
&= \sqrt{ \frac{4a^{2} - b^{2} - b\sqrt{ b^{2} + 8a^{2} }}{2} }
\end{align}
$$
De esta forma, el rectángulo tendría altura $h = \frac{-3b + \sqrt{ b^{2} + 8a^{2} }}{4}$ y base $2x = \sqrt{ \frac{4a^{2} - b^{2} - b\sqrt{ b^{2} + 8a^{2} }}{2} }$

Ahora, finalizamos con la sección mayor:
- En caso de que $b \geq \frac{a}{\sqrt{ 2 }}$, el rectángulo de mayor área es el cuadrado inscrito en el círculo completo, el cual tiene lado $a\sqrt{ 2 }$.
- En caso contrario, podemos determinar los valores de los lados en base a $a$ y $b$:
$$
\begin{align}
h &= b - y \\
&= b - \frac{b - \sqrt{ b^{2} + 8a^{2} }}{4} \\
&= \frac{4b - b + \sqrt{ b^{2} + 8a^{2} }}{4} \\
&= \frac{3b + \sqrt{ b^{2} + 8a^{2} }}{4}
\end{align}
$$
$$
\begin{align}
2x &= 2\sqrt{ a^{2} - y^{2} } \\
&= 2\sqrt{ a^{2} - \left( \frac{b - \sqrt{ b^{2} + 8a^{2} }}{4} \right)^{2} } \\
&= 2\sqrt{ a^{2} - \frac{b^{2} - 2b\sqrt{ b^{2} + 8a^{2} } + b^{2} + 8a^{2}}{16} } \\
&= 2\sqrt{ a^{2} - \frac{2b^{2} - 2b\sqrt{ b^{2} + 8a^{2} } + 8a^{2}}{16} } \\
&= 2\sqrt{ a^{2} - \frac{b^{2} - b\sqrt{ b^{2} + 8a^{2} } + 4a^{2}}{8} } \\
&= 2\sqrt{ \frac{8a^{2} - b^{2} + b\sqrt{ b^{2} + 8a^{2} } - 4a^{2}}{8} } \\
&= 2\sqrt{ \frac{4a^{2} - b^{2} + b\sqrt{ b^{2} + 8a^{2} }}{8} } \\
&= \sqrt{ 4 \cdot \frac{4a^{2} - b^{2} + b\sqrt{ b^{2} + 8a^{2} }}{8} } \\
&= \sqrt{ \frac{4a^{2} - b^{2} + b\sqrt{ b^{2} + 8a^{2} }}{2} }
\end{align}
$$

De esta manera, concluimos el ejercicio.



---
### Ejercicio 6.8.6
Primero que nada, el volumen de un cilindro se calcula como:
$$
V_{\text{cilindro}} = \pi \cdot r^{2} \cdot h
$$
Por otra parte, el volumen de un cono se calcula como:
$$
V_{\text{cono}} = \frac{1}{3} \cdot \pi \cdot r^{2} \cdot h
$$
Sabemos, por la letra, que la base del cilindro debe estar en la base del cono.

Además, el cono tiene radio $r$ y altura $h$.

De esta forma, sabemos que la base del cono es $\pi \cdot r^{2}$. Por lo que la base del cilindro no puede superar dicho valor.

De esta forma, el radio del cilindro se encuentra en el intervalo $(0, r)$, y su altura en el intervalo $(0, h)$. Sin embargo, a medida que aumenta $r$, $h$ disminuye y viceversa.

En este caso, $V_{cilindro}$ es la función que queremos maximizar.

Lo que tenemos que lograr es desarrollar una relación entre el radio del cilindro (al que denotaremos $r_{c}$) y si altura ($h_{c}$), para poder expresar el volumen como una función de una única variable.

Primero, analicemos lo que sucede cuando inscribimos un cilindro en un cono, maximizando sus atributos:
- Sabemos que el cono tiene radio $r$ y altura $h$.
- El cilindro tiene radio $r_{c}$ y altura $h_{c}$.

Sin embargo, como el cilindro inscripto está maximizado, su base superior coincide perfectamente con los bordes del cono, formando otro cono más pequeño que se apoya sobre el cilindro.
Este cono tiene radio $r_{c}$ y altura $h - h_{c}$.
Como es semejante al cono original, las proporciones entre su altura y radio son necesariamente iguales:
$$
\frac{h - h_{c}}{r_{c}} = \frac{h}{r}
$$
Para facilitar la derivación, despejamos una de las variables en función de la otra. En este caso, la altura del cilindro ($h_{c}$) en función de su radio ($r_{c}$):
$$
\begin{align}
h - h_{c} &= \frac{h}{r} \cdot r_{c} \\
-h_{c} &= \frac{h}{r} \cdot r_{c} - h \\
-h_{c} &= h\left( \frac{r_{c}}{r} - 1 \right) \\
h_{c} &= h\left( 1 - \frac{r_{c}}{r} \right)
\end{align}
$$

Ahora, logramos despejar la altura del cilindro. Lo que haremos, es sustituir dicho valor en la fórmula del volúmen del cilindro, en función de su radio $r_{c}$:
$$
\begin{align}
V(r_{c}) &= \pi \cdot r_{c}^{2} \cdot h_{c} \\
&= \pi \cdot r_{c}^{2} \cdot h\left( 1 - \frac{r_{c}}{r} \right) \\
&= \pi \cdot h \left( r_{c}^{2} - \frac{r_{c}^{3}}{r} \right)
\end{align}
$$
donde $r_{c} \in (0, r)$.

Finalmente, tenemos una función que depende de únicamente de una variable, siendo $r_{c}$.

Proseguimos a derivar la función:
$$
\begin{align}
V'(r_{c}) &= \left( \pi \cdot h \left( r_{c}^{2} - \frac{r_{c}^{3}}{r} \right) \right)' \\
&= \cancel{ \underbrace{ (\pi \cdot h)' }_{ = 0 } \left( r_{c}^{2} - \frac{r_{c}^{3}}{r} \right) } + \pi \cdot h \left( r_{c}^{2} - \frac{r_{c}^{3}}{r} \right)' \\
&= \pi \cdot h \left( 2r_{c} - \frac{3r_{c}^{2} \cdot r}{r^{2}} \right) \\
&= \pi \cdot h \left( 2r_{c} - \frac{3r_{c}^{2}}{r} \right)
\end{align}
$$
Ahora, tenemos que analizar en que valores de $r_{c}$ la función se anula:
$$
\begin{align}
\pi \cdot h \left( 2r_{c} - \frac{3r_{c}^{2}}{r} \right) = 0 \implies &2r_{c} - \frac{3r_{c}^{2}}{r} = 0 \\
&\frac{2r_{c} \cdot r - 3r_{c}^{2}}{r} = 0 \implies 2r_{c} \cdot r - 3r_{c}^{2} = 0
\end{align}
$$
Así, podemos aplicar Bhaskara:
$$
\begin{align}
&a = -3 \\
&b = 2r \\
&c = 0
\end{align}
$$
$$
\begin{align}
r_{c} &= \frac{-2r \pm \sqrt{ (2r)^{2} - \cancel{ 4 \cdot (-3) \cdot 0 } }}{2 \cdot (-3)} \\
&= \frac{-2r \pm \sqrt{ 4r^{2} }}{-6} \\
&= \frac{2r \mp \sqrt{ 4r^{2} }}{6} \\
&= \frac{2r \mp 2r}{6} \\
\end{align}
$$
$$
\begin{align}
&r_{c_{1}} = \frac{\cancel{ 2r } - \cancel{ 2r }}{6} = \frac{0}{6} = 0 \\
&r_{c_{2}} = \frac{2r + 2r}{6} = \frac{4r}{6} = \frac{2r}{3}
\end{align}
$$
De esta forma, consideraremos el valor $r_{c_{2}} = \frac{2r}{3}$.

Ahora, analizamos el signo de la función $V'(r_{c})$:

|  +  |                |  -  |
| :-: | :------------: | :-: |
|     | $\frac{2r}{3}$ |     |
Confinamos que se trata de un máximo absoluto.




Entonces, el cilindro de mayor volumen inscripto en un cono de radio $r$ y altura $h$ esta dado por calcular la imagen de la función $V(r_{c})$ para el valor $r_{c_{2}} = \frac{2r}{3}$:
$$
\begin{align}
V\left( \frac{2r}{3} \right) &= \pi \cdot h \left( r_{c}^{2} - \frac{r_{c}^{3}}{r} \right) \\
&= \pi \cdot h \left( \left( \frac{2r}{3} \right)^{2} - \frac{\left( \frac{2r}{3} \right)^{3}}{r} \right) \\
&= \pi \cdot h \left( \frac{4r^{2}}{9} - \frac{\frac{8r^{3}}{27}}{r} \right) \\
&= \pi \cdot h \left( \frac{4r^{2}}{9} - \frac{8r^{2}}{27} \right) \\
&= \pi \cdot h \left( \frac{12r^{2} - 8r^{2}}{27} \right) \\
&= \pi \cdot h \left( \frac{4r^{2}}{27} \right) \\
&= \frac{4\pi \cdot r^{2} \cdot h}{27}
\end{align}
$$

En conclusión, el cilindro de mayor volumen inscripto en un cono de radio $r$ y altura $h$ tiene volumen $\frac{4\pi \cdot r^{2} \cdot h}{27}$.

---
# 9 - Aplicaciones
## Ejercicio 6.9.1

### Parte a)
No siempre fueron a la misma velocidad, puesto que $A$ fue a velocidad constante, mientras que $B$ fue aumentando la velocidad con respecto al tiempo. Por lo tanto, considerando que ambos llegaron a la misma vez a la meta, el corredor $B$ tuvo mayor velocidad máxima.

### Parte b)
En todo momento fue ganando el corredor $A$, puesto que si estudiamos la función $A$ y la $B$, a excepción del comienzo y fin de la carrera, $A > B$ en todo momento.

### Parte c)
Considerando que hubiera un tercer corredor, que hubiera comenzado y llegado a la meta a la misma vez que el corredor $A$ y $B$. Ya que el corredor $A$ tuvo velocidad constante, consideraremos su gráfica como el segmento que une el punto de comienzo $(0, 0)$ y el punto de fin $(50, 400)$.

Como el trayecto de $B$ es continuo y derivable, comenzando y terminando el los puntos mencionados, por más irregular que haya sido su trayecto, necesariamente tiene que haber coincidido con la velocidad promedio en algún punto de su recorrido.

Si consideramos un tercer corredor $C$, el cual tendría estas mismas características, sin importar cual haya sido su recorrido, cumpliría esta misma particularidad: alcanzar la velocidad promedio en al menos un punto de su trayecto. Esto quiere decir que el corredor $B$ y $C$ tuvieron la misma velocidad, aunque no tiene porque haber sido en el mismo instante.

---
## Ejercicio 6.9.18
Si analizamos los valores "extremos", existe una proporción entre las millas debajo del agua y las millas en tierra.
Por ejemplo, si consideramos la distancia máxima, siendo 12 millas debajo del agua y 20 millas en tierra, y mínima, siendo la hipotenusa del rectángulo recto formado:
$$
\begin{align}
12^{2} + 20^{2} &= h^{2} \\
144 + 400 &= h^{2} \\
544 &= h^{2} \\
\sqrt{ 544 } &= h \\
4\sqrt{ 34 } &= h
\end{align}
$$
De esta forma, sabemos que se deben recorrer menos de 12 millas debajo del agua + 20 millas en tierra, y más de $4\sqrt{ 34 }$ millas debajo del agua.

Hay que buscar un recorrido intermedio.

Sabemos que las millas debajo del agua (a las cuales denotaremos $m_{a}$) pertenecen al intervalo $m_{a} \in [12, 4\sqrt{ 34 }]$, y las millas en tierra (a las cuales denotaremos $m_{t}$) pertenecen al intervalo $m_{t} \in [0, 20]$.

Ahora, definimos la función, pero para esto tenemos que expresar un valor en función del otro.
Si consideramos los dos parámetros para la función costo:
$$
C(m_{a}, m_{t}) = m_{a} \cdot 500000 + m_{t} \cdot 300000
$$

Si analizamos el problema geométrico considerando a la costa como el eje $x$, podemos ver que:
- El punto de la costa más cercano a la orilla es el origen $(0, 0)$.
- La refinería está a 20 millas en línea recta del origen, por lo que se encuentra en $(20, 0)$.
- Denotamos $x$ a la distancia desde el origen hasta el punto donde el oleoducto sale del agua y toca tierra. De esta forma, $x$ pertenece al intervalo $[0, 20]$.

Ahora, expresamos tanto $m_{a}$ como $m_{t}$ en función de $x$:
- $m_{a}$: Por Pitágoras, la distancia desde la plataforma (orilla) hasta el punto $x$ es:
$$
12^{2} + x^{2} = m_{a}^{2}
\sqrt{ 144 + x^{2} } = m_{a} \implies m_{a}(x) = \sqrt{ 144 + x^{2} }
$$
- $m_{t}$: Es la distancia entre $x$ y la refinería (sabiendo que $x$ pertenece a la recta formada por la refinería y el origen, el eje $x$):
$$
d(ref, x) = 20 - x \implies m_{t}(x) = 20 - x
$$

Ahora, podemos sustituir $m_{a}$ y $m_{t}$ por sus nuevas expresiones, haciendo que la función costo solo dependa de $x$:
$$
\begin{align}
C(x) &= 500000 \cdot \sqrt{ 144 + x^{2} } + 300000 \cdot (20 - x) \\
&= 500000 \cdot \sqrt{ 144 + x^{2} } + 6000000 - 300000x
\end{align}
$$
Ahora, derivamos la función para encontrar extremos:
$$
\begin{align}
C'(x) &= (500000 \cdot \sqrt{ 144 + x^{2} } + 6000000 - 300000x)' \\
&= (500000 \cdot \sqrt{ 144 + x^{2} })' - 300000 \\
&= 500000 \cdot (\sqrt{ 144 + x^{2} })' - 300000 \\
&= 500000 \cdot \frac{1}{2\sqrt{ 144 + x^{2} }} \cdot (144 + x^{2})' - 300000 \\
&= 500000 \cdot \frac{1}{\cancel{ 2 }\sqrt{ 144 + x^{2} }} \cdot \cancel{ 2 }x - 300000 \\
&= \frac{500000x}{\sqrt{ 144 + x^{2} }} - 300000
\end{align}
$$
Ahora, estudiamos el caso en el que la función se anula
$$
\begin{align}
\frac{500000x - 300000 \cdot \sqrt{ 144 + x^{2} }}{\sqrt{ 144 + x^{2} }} = 0 \implies &\frac{500000x}{\sqrt{ 144 + x^{2} }} - 300000 = 0 \\
&\frac{5x}{\sqrt{ 144 + x^{2} }} - 3 = 0 \\
&\frac{5x}{\sqrt{ 144 + x^{2} }} = 3 \\
&5x = 3\sqrt{ 144 + x^{2} } \\
&(5x)^{2} = (3\sqrt{ 144 + x^{2} })^{2} \\
&25x^{2} = 9(144 + x^{2}) \\
&25x^{2} = 1296 + 9x^{2} \\
&25x^{2} - 1296 - 9x^{2} = 0 \\
&16x^{2} - 1296 = 0
\end{align}
$$
Ahora, despejamos $x$:
$$
\begin{align}
16x^{2} - 1296 &= 0 \\
16x^{2} &= 1296 \\
x^{2} &= \frac{1296}{16} \\
x^{2} &= 81 \\
x &= \sqrt{ 81 } = 9
\end{align}
$$

Ahora, analicemos el signo de la función:

|  -  |     |  +  |
| :-: | :-: | :-: |
|     |  9  |     |
Es así que determinamos que la función tiene un mínimo relativo en $x = 9$.

Ahora, determinemos la combinación de instalación subacuática y terrestre que de la conexión más económica, así como los valores correspondientes de $m_{a}$ y $m_{t}$:
$$
\begin{align}
&m_{a}(x) = \sqrt{ 144 + x^{2} } \implies m_{a}(9) = \sqrt{ 144 + 81 } = \sqrt{ 225 } = 15 \\
&m_{t}(x) = 20 - x \implies m_{t}(9) = 20 - 9 = 11
\end{align}
$$
$$
\begin{align}
C(x) = 500000 \cdot \sqrt{ 144 + x^{2} } + 300000 \cdot (20 - x) \implies C(9) &= 500000 \cdot 15 + 300000 \cdot 11 \\
&= 7500000 + 3300000 \\
&= 10800000
\end{align}
$$
En conclusión, la combinación de instalación subacuática y terrestre que de la conexión más económica es $m_{a} = 15$ y $m_{t} = 11$, y el costo de dicha conexión es $\$ 10800000$.

---
## Ejercicio 6.9.19
Nuevamente, trabajaremos en un sistema de coordenadas, donde el origen está ubicado en la esquina interior $(0, 0)$.
De esta forma, tenemos:
- El pasillo vertical, de ancho $A$, delimitado por la pared exterior $y = -A$.
- El pasillo horizontal, de ancho $B$, delimitado por la pared exterior $x = -B$.
- Además, consideramos el ángulo que la escalera forma con una de las paredes del pasillo, denotado $\theta$.

Consideraremos la escalera en una posición que intercepte al origen, quedando así dos tramos $L_{1}$ y $L_{2}$, uno por debajo y el otro por encima.

$L_{1}$ por encima de $x = A$, es la hipotenusa de un triángulo rectángulo de base $A$. Por esta razón, y sabiendo que forma un ángulo de $\theta$ con el cateto $A$, podemos aplicar la fórmula:
$$
\cos(\theta) = \frac{A}{L_{1}} \implies L_{1} = \frac{A}{\cos(\theta)}
$$

$L_{2}$ por debajo de $x = A$, es la hipotenusa de un triángulo rectángulo con cateto $B$. Por esta razón, y sabiendo que forma un ángulo de $\theta$ con el otro cateto, podemos aplicar la fórmula:
$$
\sin(\theta) = \frac{B}{L_{2}} \implies L_{2} = \frac{B}{\sin(\theta)}
$$

En conclusión, podemos determinar la fórmula para calcular el largo de la escalera:
$$
L(\theta) = L_{1} + L_{2} = \frac{A}{\cos(\theta)} + \frac{B}{\sin(\theta)}
$$
donde $\theta \in (0, \frac{\pi}{2})$.

Ahora, pasamos a derivar la función para posteriormente encontrar sus extremos:
$$
\begin{align}
L'(\theta) &= \left( \frac{A}{\cos(\theta)} + \frac{B}{\sin(\theta)} \right)' \\
&= -\frac{A(\cos(\theta))'}{\cos ^{2}(\theta)} - \frac{B(\sin(\theta)')}{\sin ^{2}(\theta)} \\
&= \frac{A \sin(\theta)}{\cos ^{2}(\theta)} - \frac{B \cos(\theta)}{\sin ^{2}(\theta)}
\end{align}
$$
Ahora, igualamos a 0 la ecuación para hallar las raíces:
$$
\begin{align}
\frac{A \sin(\theta)}{\cos ^{2}(\theta)} - \frac{B \cos(\theta)}{\sin ^{2}(\theta)} &= 0 \\
\frac{A \sin(\theta)}{\cos ^{2}(\theta)} &= \frac{B \cos(\theta)}{\sin ^{2}(\theta)} \\
A \sin(\theta) \cdot \sin ^{2}(\theta) &= B \cos(\theta) \cdot \cos ^{2}(\theta) \\
A \sin ^{3}(\theta) &= B \cos ^{3}(\theta) \\
\frac{A \sin ^{3}(\theta)}{\cos ^{3}(\theta)} &= B \\
A \tan ^{3}(\theta) &= B \\
\tan ^{3}(\theta) &= \frac{B}{A}
\end{align}
$$
Ahora, para encontrar el valor crítico, despejamos $\theta$ y lo sustituimos en la ecuación original para obtener la longitud máxima.
$$
\begin{align}
\tan ^{3}(\theta) &= \frac{B}{A} \\
\sqrt[3]{ \tan ^{3}(\theta) } &= \sqrt[3]{ \frac{B}{A} } \\
\tan(\theta) &= \sqrt[3]{ \frac{B}{A} } \\
\tan(\theta) &= \sqrt[3]{ \frac{B}{A} } \\
\theta &= \arctan\left( \sqrt[3]{ \frac{B}{A} } \right)
\end{align}
$$
$$
L(\theta) = \frac{A}{\cos(\theta)} + \frac{B}{\sin(\theta)} \implies L\left( \arctan\left( \sqrt[3]{ \frac{B}{A} } \right) \right) = \frac{A}{\cos\left( \arctan\left( \sqrt[3]{ \frac{B}{A} } \right) \right)} + \frac{B}{\sin\left( \arctan\left( \sqrt[3]{ \frac{B}{A} } \right) \right)}
$$

Antes de calcular la longitud de la escalera más larga que se puede transportar en las situaciones propuestas, un detalle a analizar:
Cuando desarrollamos la derivada, llegamos a una expresión algebraica de la función tangente, que no depende de otras funciones trigonométricas. Sin embargo, nuestra función $L(\theta)$ depende de $\sin$ y $\cos$. Sería ideal remover dicha dependencia, haciendo que únicamente se dependa de $A$ y $B$. Esto se basa en la idea de unificación del álgebra y la geometría, propuesta por Newton y Leibniz como base del cálculo.

Primero que nada, comenzamos considerando la identidad trigonométrica fundamental mencionada en las fuentes para la derivada de la tangente:
$$
\tan ^{2}(\theta) + 1 = \frac{1}{\cos ^{2}(\theta)}
$$
Ahora, sustituimos $\tan(\theta)$ por $x$:
$$
\begin{align}
x^{2} + 1 &= \frac{1}{\cos ^{2}(\theta)} \\
\cos ^{2}(\theta) &= \frac{1}{x^{2} + 1} \\
\cos(\theta) &= \sqrt{ \frac{1}{x^{2} + 1} } \\
\cos(\theta) &= \frac{1}{\sqrt{ x^{2} + 1 }}
\end{align}
$$
Ahora, aprovechamos esto para desarrollar la misma idea para el $\sin$:
$$
\begin{align}
\tan(\theta) &= \frac{\sin(\theta)}{\cos(\theta)} \\
x &= \frac{\sin(\theta)}{\cos(\theta)} \\
x \cdot \cos(\theta) &= \sin(\theta) \\
x \cdot \frac{1}{\sqrt{ x^{2} + 1 }} &= \sin(\theta) \\
\frac{x}{\sqrt{ x^{2} + 1 }} &= \sin(\theta)
\end{align}
$$
Ahora, sustituimos dichas expresiones en la fórmula $L(\theta)$:
$$
\begin{align}
L(\theta) &= \frac{A}{\cos(\theta)} + \frac{B}{\sin(\theta)} \\
&= \frac{A}{\frac{1}{\sqrt{ x^{2} + 1 }}} + \frac{B}{\frac{x}{\sqrt{ x^{2} + 1 }}} \\
&= A\sqrt{ x^{2} + 1 } + \frac{B \sqrt{ x^{2} + 1 }}{x} \\
&= \sqrt{ x^{2} + 1 } \left( A + \frac{B}{x} \right)
\end{align}
$$
Como habíamos determinado que $x = \tan(\theta) = \sqrt[3]{ \frac{B}{A} } = \left( \frac{B}{A} \right)^{\frac{1}{3}}$:
$$
\begin{align}
L(\theta) &= \sqrt{ x^{2} + 1 } \left( A + \frac{B}{x} \right) \\
&= \sqrt{ \left( \left( \frac{B}{A} \right)^{\frac{1}{3}} \right)^{2} + 1 } \left( A + \frac{B}{\left( \frac{B}{A} \right)^{\frac{1}{3}}} \right) \\
&= \sqrt{ \frac{B^{\frac{2}{3}}}{A^{\frac{2}{3}}} + 1 } \left( A + \frac{B}{ \frac{B^{\frac{1}{3}}}{A^{\frac{1}{3}}} } \right) \\
&= \sqrt{ \frac{B^{\frac{2}{3}}}{A^{\frac{2}{3}}} + 1 } \left( A + \frac{A^{\frac{1}{3}}B}{ B^{\frac{1}{3}} } \right) \\
&= \sqrt{ \frac{B^{\frac{2}{3}}}{A^{\frac{2}{3}}} + 1 } \left( A + A^{\frac{1}{3}}B^{\frac{2}{3}} \right) \\
&= \sqrt{ \frac{B^{\frac{2}{3}} + A^{\frac{2}{3}}}{A^{\frac{2}{3}}} } \left( A + A^{\frac{1}{3}}B^{\frac{2}{3}} \right) \\
&= \frac{\sqrt{ B^{\frac{2}{3}} + A^{\frac{2}{3}} }}{\sqrt{ A^{\frac{2}{3}} }} \left( A + A^{\frac{1}{3}}B^{\frac{2}{3}} \right) \\
&= \frac{\sqrt{ B^{\frac{2}{3}} + A^{\frac{2}{3}} }}{A^{\frac{1}{3}}} \left( A + A^{\frac{1}{3}}B^{\frac{2}{3}} \right) \\
&= \frac{\sqrt{ B^{\frac{2}{3}} + A^{\frac{2}{3}} }}{\cancel{ A^{\frac{1}{3}} }} \left( \cancel{ A^{\frac{1}{3}} } \left( A^{\frac{2}{3}} + B^{\frac{2}{3}} \right) \right) \\
&= \sqrt{ B^{\frac{2}{3}} + A^{\frac{2}{3}} } \left( A^{\frac{2}{3}} + B^{\frac{2}{3}} \right) \\
&= \left( A^{\frac{2}{3}} + B^{\frac{2}{3}} \right)^{\frac{1}{2}} \left( A^{\frac{2}{3}} + B^{\frac{2}{3}} \right)^{1} \\
&= \left( A^{\frac{2}{3}} + B^{\frac{2}{3}} \right)^{\frac{3}{2}}
\end{align}
$$
En conclusión:
$$
L = \left( A^{\frac{2}{3}} + B^{\frac{2}{3}} \right)^{\frac{3}{2}}
$$
Obtuvimos una función que no depende de parámetros.

Ahora, calculamos la longitud de la escalera más larga que se puede transportar en las situaciones propuestas:

- Para $A = 2m$, $B = 3m$:
$$
\begin{align}
L &= \left( A^{\frac{2}{3}} + B^{\frac{2}{3}} \right)^{\frac{3}{2}} \\
&= \left( 2^{\frac{2}{3}} + 3^{\frac{2}{3}} \right)^{\frac{3}{2}}
\end{align}
$$

- Para $A = 3m$, $B = 3m$:
$$
\begin{align}
L &= \left( A^{\frac{2}{3}} + B^{\frac{2}{3}} \right)^{\frac{3}{2}} \\
&= \left( 3^{\frac{2}{3}} + 3^{\frac{2}{3}} \right)^{\frac{3}{2}} \\
&= \left( 2 \cdot 3^{\frac{2}{3}} \right)^{\frac{3}{2}} \\
&= 2^{\frac{3}{2}} \cdot 3 \\
&= \sqrt{ 2^{3} } \cdot 3 \\
&= 2\sqrt{ 2 } \cdot 3 \\
&= 6\sqrt{ 2 }
\end{align}
$$


Previamente habíamos desarrollado (sin la versión simplificada de $L$):

- Para $A = 2m$, $B = 3m$:
$$
\begin{align}
L\left( \arctan\left( \sqrt[3]{ \frac{3}{2} } \right) \right) &= \frac{2}{\cos\left( \arctan\left( \sqrt[3]{ \frac{3}{2} } \right) \right)} + \frac{3}{\sin\left( \arctan\left( \sqrt[3]{ \frac{3}{2} } \right) \right)}
\end{align}
$$
Para saber el valor de $\arctan\left( \sqrt[3]{ \frac{3}{2} } \right)$, tenemos que considerar que valor de $x$ cumple $\tan(x) = \sqrt[3]{ \frac{3}{2} } = \left( \frac{3}{2} \right)^{\frac{1}{3}}$.


Para $A = 3m$, $B = 3m$:
$$
\begin{align}
L\left( \arctan\left( \sqrt[3]{ \frac{3}{3} } \right) \right) &= \frac{3}{\cos\left( \arctan\left( \sqrt[3]{ \frac{3}{3} } \right) \right)} + \frac{3}{\sin\left( \arctan\left( \sqrt[3]{ \frac{3}{3} } \right) \right)} \\
&= \frac{3}{\cos\left( \arctan\left( \sqrt[3]{ 1 } \right) \right)} + \frac{3}{\sin\left( \arctan\left( \sqrt[3]{ 1 } \right) \right)} \\
&= \frac{3}{\cos\left( \arctan\left( 1 \right) \right)} + \frac{3}{\sin\left( \arctan\left( 1 \right) \right)}
\end{align}
$$
Para saber el valor de $\arctan(1)$, tenemos que considerar que valor de $x$ cumple $\tan(x) = 1$
$$
\begin{align}
\tan(x) = 1 \implies &\frac{\sin(x)}{\cos(x)} = 1 \\
&\sin(x) = \cos(x) \implies x = \frac{\pi}{4} \qquad \text{(por círculo trigonométrico)}
\end{align}
$$

$$
\begin{align}
L\left( \arctan\left( \sqrt[3]{ \frac{3}{3} } \right) \right) &= \frac{3}{\cos\left( \arctan\left( 1 \right) \right)} + \frac{3}{\sin\left( \arctan\left( 1 \right) \right)} \\
&= \frac{3}{\cos\left( \frac{\pi}{4} \right)} + \frac{3}{\sin\left( \frac{\pi}{4} \right)} \\
&= \frac{3}{\frac{1}{\sqrt{ 2 }}} + \frac{3}{\frac{1}{\sqrt{ 2 }}} \\
&= 3\sqrt{ 2 } + 3\sqrt{ 2 } \\
&= 6\sqrt{ 2 }
\end{align}
$$

---
## Ejercicio 6.9.3
Representemos la situación:
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 6 - Derivación/Imágenes/1 - Ejercicio 6.9.3.png]]

Además, sabemos que en el momento representado, el ángulo crece a razón de $0,14 \frac{rad}{min}$. Lo que quiere decir que (si el globo mantuviera su velocidad constante) en un minuto, el ángulo pasará a ser $\frac{\pi}{4} + 0,14$, luego $\frac{\pi}{4} + 0,28$, y así. Igualmente, eso es únicamente en el instante considerado. Por lo tanto, se nos solicita determinar la velocidad a la que se eleva el globo en ese momento.

Algo que hay que entender es que tenemos el dato de la distancia, que junto con el ángulo brindado, nos permite determinar la altura del globo.

Como el ángulo es $\frac{\pi}{4}$, sabemos que en dicho valor, las funciones $\cos$ y $\sin$ coinciden, ya que el triangulo rectángulo formado tiene dos ángulos iguales de $45°$, por lo que necesariamente sus dos catetos son iguales. De esta manera, sabemos que el otro cateto (la altura del globo en ese instante) vale 150m.

Ahora, sabemos que está a 150 metros de altura, calculada en base al ángulo formado con el observador (de $\frac{\pi}{4}$), el cual crece a razón de $0,14 \frac{rad}{min}$ en ese instante.

Ahora, tenemos que definir la relación matemática entre la altura del globo (a la que denotaremos $h$) y el ángulo de observación ($\theta$). Estos están vinculados por la función tangente en el triángulo rectángulo que se forma:
$$
\tan(\theta) = \frac{h}{150} \implies h = 150 \cdot \tan(\theta)
$$
Esto tiene sentido ya que $\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)}$, así que si consideramos $\cos(\frac{\pi}{4})$ y $\sin(\frac{\pi}{4})$, los cuales son iguales, obtenemos 1, siendo $h = 150$.

Ahora, para hallar la velocidad a la que se eleva el globo ($\frac{dh}{dt}$, altura con respecto al tiempo), tenemos que derivar ambos lados de la ecuación respecto al tiempo. Para esto, aplicamos la regla de la cadena en el lado de la tangente:
Derivada de la tangente:
$$
(\tan \theta)' = \left( \frac{\sin \theta}{\cos \theta} \right)' = \frac{\overbrace{ \sin' \theta }^{ \cos \theta } \cos \theta - \sin \theta \overbrace{ \cos' \theta }^{ -\sin \theta }}{\cos ^{2} \theta} = \frac{\cos \theta \cos \theta - \sin \theta (- \sin\theta)}{\cos ^{2} \theta} = \frac{\cos ^{2} \theta + \sin ^{2} \theta}{\cos ^{2} \theta} = \frac{1}{\cos ^{2} \theta}
$$

$$
\frac{dh}{dt} = 150 \cdot (\tan \theta)' \cdot \frac{d \theta}{dt} = 150 \cdot \frac{1}{\cos ^{2} \theta} \cdot \frac{d \theta}{dt}
$$
Ahora, sabemos que:
- $\theta = \frac{\pi}{4}$
- $\frac{d \theta}{dt} = 0,14 \frac{rad}{min}$

De esta forma:
$$
\frac{dh}{dt} = 150 \cdot \frac{1}{\cos ^{2} \left( \frac{\pi}{4} \right)} \cdot 0,14 = 150 \cdot \frac{1}{\frac{1}{(\sqrt{ 2 })^{2}}} \cdot 0,14 = 150 \cdot \frac{1}{\frac{1}{2}} \cdot 0,14 = 150 \cdot 2 \cdot 0,14 = 42 \frac{m}{min}
$$

En conclusión:
En el momento en que el ángulo es $\frac{\pi}{4}$, el globo se está elevando a una velocidad instantánea de $42 \frac{m}{min}$.

ACLARACIÓN: UTILIZAMOS LA FUNCIÓN TANGENTE YA QUE ES LA FUNCIÓN TRIGONOMÉTRICA QUE RELACIONA EL CATETO OPUESTO CON EL ADYACENTE.

---
## Ejercicio 6.9.16



---
## Ejercicio 6.9.18


