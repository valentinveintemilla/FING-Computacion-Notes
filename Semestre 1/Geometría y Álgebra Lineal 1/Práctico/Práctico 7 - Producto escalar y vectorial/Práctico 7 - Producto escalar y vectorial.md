# 1 - Producto escalar y producto vectorial
## Ejercicio 1.1
$$
\begin{align}
&u = (2, -1, 7) \\
&v = (1, 1, -3) \\
&w = (1, -1, 2)
\end{align}
$$
Considerando que trabajamos en una base ortonormal:
$$
\begin{align}
&u \cdot v = \langle u, v \rangle = u_{1}v_{1} + u_{2}v_{2} + u_{3}v_{3} \\
&||u|| = \sqrt{ u \cdot u } = \sqrt{ u_{1}^{2} + u_{2}^{2} + u_{3}^{2} } \\
&u \land v = \begin{pmatrix}
u_{2}v_{3} - u_{3}v_{2} \\
u_{3}v_{1} - u_{1}v_{3} \\
u_{1}v_{2} - u_{2}v_{1}
\end{pmatrix} (\text{en base al determinante sobre primer fila } \left|
\begin{array}{ccc}
i & j & k \\
u_{1} & u_{2} & u_{3} \\
v_{1} & v_{2} & v_{3}
\end{array}
\right| \text{ pero separado en 3} )
\end{align}
$$
### Parte a)
$$
||u|| = \sqrt{ u \cdot u } = \sqrt{ u_{1}^{2} + u_{2}^{2} + u_{3}^{2} } = \sqrt{ 2^{2} + (-1)^{2} + 7^{2} } = \sqrt{ 4 + 1 + 49 } = \sqrt{ 54 } = \sqrt{ 2 \times 3 \times 3 \times 3 } = 3\sqrt{ 6 }
$$
$$
||v|| = \sqrt{ v \cdot v } = \sqrt{ v_{1}^{2} + v_{2}^{2} + v_{3}^{2} } = \sqrt{ 1^{2} + 1^{2} + (-3)^{2} } = \sqrt{ 1 + 1 + 9 } = \sqrt{ 11 }
$$
$$
\langle u, v \rangle = u \cdot v = u_{1}v_{1} + u_{2}v_{2} + u_{3}v_{3} = 2 \times 1 + (-1) \times 1 + 7 \times (-3) = 2 - 1 - 21 = -20
$$
$$
u \land v = (u_{2}v_{3} - v_{2}u_{3}, -(u_{1}v_{3} - v_{1}u_{3}), u_{1}v_{2} - v_{1}u_{2}) = (3 - 7, -(-6 - 7), 2 + 1) = (-4, 13, 3)
$$
$$
||u \land v|| = ||(-4, 13, 3)|| = \sqrt{ (-4)^{2} + 13^{2} + 3^{2} } = \sqrt{ 16 + 169 + 9 } = \sqrt{ 194 }
$$

### Parte b)
1. $u \land (v \land w)$
$$
u \land (v \land w) = u \land (v_{2}w_{3} - v_{3}w_{2}, v_{3}w_{1} - v_{1}w_{3}, v_{1}w_{2} - v_{2}w_{1}) = u \land (2 - 4, -3 - 2, -1 - 1)
$$
$$
= u \land (-2, -5, -2) = (-2u_{2} - (-5u_{3}), -2u_{3} - (-2u_{1}), -5u_{1} - (-2u_{2})) = (2 + 35, -14 + 4, -10 + 2)
$$
$$
= (37, -10, -8)
$$
2. $(u \land v) \land w$
$$
(u \land v) \land w = (-4, 13, 3) \land w = (13w_{3} - 3w_{2}, 3w_{1} - (-4w_{3}), -4w_{2} - 13w_{1}) = (26 + 3, 3 + 8, 4 - 13)
$$
$$
= (29, 11, -9)
$$
Como vemos, el producto vectorial no es una operación asociativa:
$$
u \land (v \land w) = (37, -10, -8) \neq (u \land v) \land w = (29, 11, -9)
$$

---
## Ejercicio 1.2
## Parte a)
Probar que:
$$
||x + y||^{2} = ||x||^{2} + ||y||^{2} + 2<x,y>
$$
$$
||x + y|| = ||(x_{1} + y_{1}, x_{2} + y_{2}, x_{3} + y_{3})|| = \sqrt{ (x_{1} + y_{1})^{2} + (x_{2} + y_{2})^{2} + (x_{3} + y_{3})^{2} }
$$
$$
\implies ||x + y||^{2} = (x_{1} + y_{1})^{2} + (x_{2} + y_{2})^{2} + (x_{3} + y_{3})^{2} = x_{1}^{2} + 2x_{1}y_{1} + y_{1}^{2} + x_{2}^{2} + 2x_{2}y_{2} + y_{2}^{2} + x_{3}^{2} + 2x_{3}y_{3} + y_{3}^{2}
$$
Podemos analizar cada parte por separado:
$$
||x|| = \sqrt{ x_{1}^{2} + x_{2}^{2} + x_{3}^{2} } \implies x_{1}^{2} + x_{2}^{2} + x_{3}^{2} = ||x||^{2}
$$
$$
||y|| = \sqrt{ y_{1}^{2} + y_{2}^{2} + y_{3}^{2} } \implies y_{1}^{2} + y_{2}^{2} + y_{3}^{2} = ||y||^{2}
$$
De esta manera:
$$
||x + y||^{2} = ||x||^{2} + ||y||^{2} + 2x_{1}y_{1} + 2x_{2}y_{2} + 2x_{3}y_{3}
$$
Ahora, si analizamos el producto escalar $\langle x, y \rangle$:
$$
\langle x, y \rangle = x_{1}y_{1} + x_{2}y_{2} + x_{3}y_{3} \implies 2x_{1}y_{1} + 2x_{2}y_{2} + 2x_{3}y_{3} = 2(x_{1}y_{1} + x_{2}y_{2} + x_{3}y_{3}) = 2\langle x, y \rangle
$$

En conclusión:
$$
||x + y||^{2} = ||x||^{2} + ||y||^{2} + 2\langle x, y \rangle
$$

---
## Ejercicio 1.3
Para esto, consideraremos que no estamos trabajando en una base ortonormal. Por lo tanto:
$$
\begin{align}
&u \cdot v = ||u|| \cdot ||v|| \cdot \cos \theta \\
\end{align}
$$

### Parte a)
Sabemos que:
$$
\begin{align}
&\theta = \frac{\pi}{4} \\
&||u|| = 3 \\
&(u - v) \perp u \implies (u - v) \cdot u = 0
\end{align}
$$
$$
\begin{align}
(u - v) \cdot u &= 0 \\
u \cdot u - v \cdot u &= 0 \\
u \cdot u - v \cdot u &= 0
\end{align}
$$
Sabemos que $u \cdot u = ||u||^{2}$:
$$
\begin{align}
||u||^{2} - v \cdot u &= 0 \\
9 - v \cdot u &= 0 \\
v \cdot u &= 9
\end{align}
$$
Ahora, simplemente desarrollamos el producto escalar:
$$
\begin{align}
||v|| \cdot ||u|| \cdot \cos \frac{\pi}{4} &= 9 \\
||v|| \cdot 3 \cdot \frac{1}{\sqrt{ 2 }} &= 9 \\
||v|| \cdot \frac{3}{\sqrt{ 2 }} &= 9 \\
||v|| &= 9 \cdot \frac{\sqrt{ 2 }}{3} \\
||v|| &= 3\sqrt{ 2 }
\end{align}
$$

### Parte b)
Sabemos que:
$$
\begin{align}
&\theta (u \text{ y } v) = \frac{\pi}{4} \\
&||u|| = 3 \\
&\theta (u + v \text{ y } u) = \frac{\pi}{6}
\end{align}
$$
$$
(u + v) \cdot u = u \cdot u + v \cdot u
$$
Sabemos que $u \cdot u = ||u||^{2}$:
$$
(u + v) \cdot u = ||u||^{2} + v \cdot u
$$
Desarrollamos el producto escalar $v \cdot u$:
$$
\begin{align}
||u + v|| \cdot ||u|| \cdot \cos \frac{\pi}{6} &= ||u||^{2} + ||v|| \cdot ||u|| \cdot \cos \frac{\pi}{4} \\
||u + v|| \cdot \cancel{ ||u|| } \cdot \cos \frac{\pi}{6} &= \cancel{ ||u|| } \left(||u|| + ||v|| \cdot \cos \frac{\pi}{4} \right) \\
||u + v|| \cdot \cos \frac{\pi}{6} &= ||u|| + ||v|| \cdot \cos \frac{\pi}{4} \\
||u + v|| \cdot \frac{\sqrt{ 3 }}{\cancel{ 2 }} &= 3 + ||v|| \cdot \frac{\sqrt{ 2 }}{\cancel{ 2 }} \\
||u + v|| \cdot \sqrt{ 3 } &= 6 + ||v|| \cdot \sqrt{ 2 } \\
||u + v|| \cdot \sqrt{ 3 } &= 3\sqrt{ 2 }\sqrt{ 2 } + ||v|| \cdot \sqrt{ 2 } \\
||u + v|| \cdot \frac{\sqrt{ 3 }}{\sqrt{ 2 }} &= 3\sqrt{ 2 } + ||v||
\end{align}
$$

Ahora, si consideramos la definición de norma:
$$
||u + v|| = \sqrt{ (u + v) \cdot (u + v) } = \sqrt{ ||u||^{2} + 2(u \cdot v) + ||v||^{2} }
$$
$$
\begin{align}
&= \sqrt{ ||u||^{2} + 2\left( ||u|| \cdot ||v|| \cdot \cos \frac{\pi}{4} \right) + ||v||^{2} } \\
&= \sqrt{ 9 + 2\left( \frac{3\sqrt{ 2 }}{2} \cdot ||v|| \right) + ||v||^{2} } \\
&= \sqrt{ 9 + 3\sqrt{ 2 } \cdot ||v|| + ||v||^{2} }
\end{align}
$$
Entonces:
$$
\begin{align}
||u + v|| \cdot \frac{\sqrt{ 3 }}{\sqrt{ 2 }} &= 3\sqrt{ 2 } + ||v|| \\
\sqrt{ 9 + 3\sqrt{ 2 } \cdot ||v|| + ||v||^{2} } \cdot \frac{\sqrt{ 3 }}{\sqrt{ 2 }} &= 3\sqrt{ 2 } + ||v|| \\
(9 + 3\sqrt{ 2 } \cdot ||v|| + ||v||^{2}) \cdot \frac{3}{2} &= (3\sqrt{ 2 } + ||v||)^{2} \\
\frac{27}{2} + \frac{9\sqrt{ 2 }}{2} \cdot ||v|| + \frac{3}{2} \cdot ||v||^{2} &= 18 + 6\sqrt{ 2 } \cdot ||v|| + ||v||^{2} \\
27 + \cancel{ 9\sqrt{ 2 } \cdot ||v|| } + \cancel{ 3 } \cdot ||v||^{2} &= 36 + \cancelto{ 3 }{ 12 }\sqrt{ 2 } \cdot ||v|| + \cancel{ 2 \cdot ||v||^{2} } \\
27 + ||v||^{2} &= 36 + 3\sqrt{ 2 } \cdot ||v|| \\
||v||^{2} - 3\sqrt{ 2 }||v|| - 9 = 0
\end{align}
$$
Aplicamos Bashkara:
$$
\begin{align}
||v|| &= \frac{3\sqrt{ 2 } \pm \sqrt{ (3\sqrt{ 2 })^{2} - 4 \times 1 \times (-9) }}{2 \times 1} \\
&= \frac{3\sqrt{ 2 } \pm \sqrt{ 18 + 36 }}{2} \\
&= \frac{3\sqrt{ 2 } \pm \sqrt{ 54 }}{2} \\
&= \frac{3\sqrt{ 2 } \pm 3\sqrt{ 6 }}{2}
\end{align}
$$
Si analizamos los dos posibles resultados:
$$
\begin{align}
&||v||_{1} = \frac{3\sqrt{ 2 } + 3\sqrt{ 6 }}{2} \\
&||v||_{2} = \frac{3\sqrt{ 2 } - 3\sqrt{ 6 }}{2}
\end{align}
$$
Únicamente $||v||_{1}$ es válido, ya que la norma de un vector tiene que ser positiva.

Ahora, podemos sustituir para encontrar el valor de $||u + v||$:
$$
\begin{align}
||u + v|| \cdot \frac{\sqrt{ 3 }}{\sqrt{ 2 }} &= 3\sqrt{ 2 } + ||v|| \\
||u + v|| \cdot \frac{\sqrt{ 3 }}{\sqrt{ 2 }} &= 3\sqrt{ 2 } + \frac{3\sqrt{ 2 } + 3\sqrt{ 6 }}{2} \\
||u + v|| \cdot \frac{\sqrt{ 3 }}{\sqrt{ 2 }} &= \frac{6\sqrt{ 2 } + 3\sqrt{ 2 } + 3\sqrt{ 6 }}{2} \\
||u + v|| \cdot \frac{\sqrt{ 3 }}{\sqrt{ 2 }} &= \frac{9\sqrt{ 2 } + 3\sqrt{ 6 }}{2} \\
||u + v|| &= \frac{9\sqrt{ 2 } + 3\sqrt{ 6 }}{2} \cdot \frac{\sqrt{ 2 }}{\sqrt{ 3 }} \\
||u + v|| &= \frac{18 + 3\sqrt{ 12 }}{2 \sqrt{ 3 }} \\
||u + v|| &= \frac{\cancelto{ 3 }{ 6 }\sqrt{ 3 }\cancel{ \sqrt{ 3 } } + \cancelto{ 3 }{ 6 }\cancel{ \sqrt{ 3 } }}{\cancel{ 2 } \cancel{ \sqrt{ 3 } }} \\
||u + v|| &= 3\sqrt{ 3 } + 3
\end{align}
$$

### Parte c)
En realidad, la igualdad $\langle u, v \rangle = \langle w, v \rangle$ implica:
$$
\begin{align}
\langle u, v \rangle &= \langle w, v \rangle \\
||u|| \cdot ||v|| \cdot \cos \theta &= ||w|| \cdot ||v|| \cdot \cos \alpha
\end{align}
$$
Siendo $\theta$ el ángulo formado por $u$ y $v$, y $\alpha$ el ángulo formado por $w$ y $v$. Por esta razón, la igualdad no implica que $u = w$, puesto que se considera la norma de los vectores $u$ y $w$, la cual puede ser igual aunque los vectores no coincidan, y el ángulo formado con $v$.

La afirmación tampoco es cierta incluso si trabajamos en una base ortonormal, puesto que aquí:
$$
\begin{align}
\langle u, v \rangle &= \langle w, v \rangle \\
u_{1}v_{1} + u_{2}v_{2} + u_{3}v_{3} &= w_{1}v_{1} + w_{2}v_{2} + w_{3}v_{3}
\end{align}
$$
Pueden existir varios valores de $u_{1}$, $u_{2}$ y $u_{3}$ que verifiquen la igualdad, lo mismo para $w_{1}$, $w_{2}$ y $w_{3}$.

Ahora, si estudiamos el vector $u - w$:
$$
\langle u, v \rangle = \langle w, v \rangle
$$
Podemos restar $\langle w, v \rangle$ a ambos lados de la ecuación:
$$
\langle u, v \rangle - \langle w, v \rangle = 0
$$
Sabemos que 
$$
\langle u, v \rangle - \langle w, v \rangle = u \cdot v - w \cdot v
$$
Por lo tanto:
$$
\begin{align}
\langle u, v \rangle - \langle w, v \rangle &= 0 \\
u \cdot v - w \cdot v &= 0 \\
(u - w) \cdot v &= 0
\end{align}
$$
También podemos expresarlo como
$$
\langle u - w, v \rangle = 0
$$
De esta forma, determinamos que el vector $u - w$ es ortogonal (perpendicular) al vector $v$:
$$
\langle u - w, v \rangle = 0 \implies u - w \perp v
$$

---
# 2 - Revisitando ecuaciones de rectas y planos
## Ejercicio 2.1
### Parte a)
Para empezar, tenemos que encontrar dos vectores ortogonales a $(-1, 2, 3)$, y que no sean colineales entre si. Por esta razón, utilizaremos la operación producto escalar igualado a 0 (indicando que los vectores son ortogonales):
$$
-1x + 2y + 3z = 0
$$
Por ejemplo, podemos tomar:
$$
\begin{align}
&u = (2, 1, 0) \\
&v = (3, 0, 1)
\end{align}
$$
Ahora, podemos desarrollar la ecuación paramétrica:
$$
\begin{cases}
x = -3 + 2\lambda + 3\mu \\
y = 1 + \lambda \\
z = \mu
\end{cases}
$$
Como $z = \mu$, podemos sustituir $\mu$ por $z$ en el resto de ecuaciones:
$$
\begin{cases}
x = -3 + 2\lambda + 3z \\
y = 1 + \lambda
\end{cases}
$$
Ahora, determinamos el valor de $\lambda$ en función de $y$:
$$
y = 1 + \lambda \implies \lambda = y - 1
$$
Sustituimos dicho valor en la primer ecuación:
$$
x = -3 + 2(y - 1) + 3z \implies x - 2y - 3z + 5 = 0
$$
De esta forma, la ecuación del plano que pasa por el punto $(-3, 1, 0)$ y es perpendicular a $(-1, 2, 3)$ es:
$$
x - 2y - 3z + 5 = 0
$$

En realidad, el ejercicio puede realizarse de forma directa, sabiendo que, si un plano es perpendicular a $(A, B, C)$, entonces su ecuación reducida es de la forma
$$
Ax + By + Cz + D = 0
$$
De esta forma, como tenemos un vector perpendicular $(-1, 2, 3)$, la ecuación del plano perpendicular es:
$$
-x + 2y + 3z + D = 0
$$
Para encontrar el término independiente $D$, podemos utilizar el punto $(-3, 1, 0)$:
$$
3 + 2 + 0 + D = 0 \implies D = -5
$$
En conclusión, la ecuación del plano especificado es:
$$
-x + 2y + 3z - 5 = 0
$$

### Parte b)
Primero que nada, busquemos un valor de $N$. Como tiene que ser un vector perpendicular al plano (vector normal), podemos tomar simplemente los coeficientes de las incógnitas de la ecuación del plano $\pi$:
$$
x - y + 3z = 1 \implies (1, -1, 3) \text{ es un vector normal}
$$
Entonces $N = (1, -1, 3)$

Considerando la ecuación objetivo $\langle P - P_{0}, N \rangle = 0$, el vector $P - P_{0}$ y $N$ son ortogonales, por lo tanto:
$$
(p_{1} - p_{0_{1}})n_{1} + (p_{2} - p_{0_{2}})n_{2} + (p_{3} - p_{0_{3}})n_{3} = 0
$$
Ya conocemos los componentes de $N$:
$$
(p_{1} - p_{0_{1}}) - (p_{2} - p_{0_{2}}) + 3(p_{3} - p_{0_{3}}) = 0
$$
Si analizamos la ecuación, podemos ver que $p_{1}$, $p_{2}$ y $p_{3}$ cumplen el rol de las variables $x$, $y$ y $z$, los componentes de $N$ son los coeficientes, y $p_{0_{1}}$, $p_{0_{2}}$ y $p_{0_{3}}$ (en conjunto con los coeficientes mencionados) forman el término independiente. Si desarrollamos:
$$
\begin{align}
p_{1} - p_{0_{1}} - p_{2} + p_{0_{2}} + 3p_{3} - 3p_{0_{3}} &= 0 \\
p_{1} - p_{2} + 3p_{3} - p_{0_{1}} + p_{0_{2}} - 3p_{0_{3}} &= 0 \\
p_{1} - p_{2} + 3p_{3} &= p_{0_{1}} - p_{0_{2}} + 3p_{0_{3}}
\end{align}
$$
$$
\implies p_{0_{1}} - p_{0_{2}} + 3p_{0_{3}} = 1
$$
Tenemos que encontrar un punto que satisfaga la ecuación anterior. Podemos considerar $(1, 0, 0)$:
$$
1 - 0 + 3 \times 0 = 1
$$
Es así que determinamos el vector $N$ y el punto $P_{0}$:
$$
\begin{align}
&N = (1, -1, 3) \\
&P_{0} = (1, 0, 0)
\end{align}
$$
En conclusión, la ecuación en forma de producto escalar es:
$$
\langle P - P_{0}, N \rangle = 0 \longrightarrow \langle (x, y, z) - (1, 0, 0), (1, -1, 3) \rangle = 0
$$

### Parte c)
Primero, recordemos que podemos tomar un vector normal al plano directamente al estudiar su ecuación implícita:
$$
\pi = 2x + y = 0 \implies (2, 1, 0) \text{ es un vector normal}
$$
De esta forma, tenemos que determinar dos vectores que sean paralelos a $(2, 1, 0)$ y tengan norma 1:
$$
\sqrt{ x^{2} + y^{2} + z^{2} } = 1
$$
Por lo tanto:
$$
x^{2} + y^{2} + z^{2} = 1
$$
Determinemos la norma del vector $(2, 1, 0)$:
$$
||(2, 1, 0)|| = \sqrt{ 2^{2} + 1^{2} + 0^{2} } = \sqrt{ 4 + 1 + 0 } = \sqrt{ 5 }
$$

Lo que podríamos hacer es dividir cada componente del vector entre $\sqrt{ 5 }$ para obtener un vector de norma 1:
$$
||\left( \frac{2}{\sqrt{ 5 }}, \frac{1}{\sqrt{ 5 }}, 0 \right)|| = \sqrt{ \left( \frac{2}{\sqrt{ 5 }} \right)^{2} + \left( \frac{1}{\sqrt{ 5 }} \right)^{2} + 0^{2} } = \sqrt{ \frac{4}{5} + \frac{1}{5} + 0 } = \sqrt{ \frac{5}{5} } = \sqrt{ 1 } = 1
$$
De esta forma, podemos considerar el versor $\left( \frac{2}{\sqrt{ 5 }}, \frac{1}{\sqrt{ 5 }}, 0 \right)$. Como segundo versor, podríamos considerar el opuesto: $\left( -\frac{2}{\sqrt{ 5 }}, -\frac{1}{\sqrt{ 5 }}, 0 \right)$

En conclusión, encontramos dos versores perpendiculares al plano $2x + y = 0$: $\left( \frac{2}{\sqrt{ 5 }}, \frac{1}{\sqrt{ 5 }}, 0 \right)$ y $\left( -\frac{2}{\sqrt{ 5 }}, -\frac{1}{\sqrt{ 5 }}, 0 \right)$.

---
## Ejercicio 2.2
Para determinar que las rectas
$$
\begin{cases}
x + y - 3z - 1 = 0 \\
2x - y - 9z - 2 = 0
\end{cases}, \begin{cases}
2x + y + 2z + 5 = 0 \\
2x - 2y - z + 2 = 0
\end{cases}
$$
tenemos que tomar un vector director de cada una, y comprobar que su producto escalar es 0.

Para esto, buscaremos dos puntos que se encuentren en cada recta:
$$
\begin{cases}
x + y - 3z - 1 = 0 \\
2x - y - 9z - 2 = 0
\end{cases}
$$
Si sumamos ambas ecuaciones:
$$
3x - 12z - 3 = 0 \implies 3x - 12z = 3
$$
De esta forma, podemos considerar $x = 5$ y $z = 1$. Si probamos dichos valores en las ecuaciones, podemos ver que, con tal de que se cumpla la igualdad propuesta, $y = -1$. Tenemos un punto: $(5, -1, 1)$.

Otros valores a considerar son $x = 3$, $z = \frac{1}{2}$. De esta forma, tomaremos $y = -\frac{1}{2}$. Es así que tenemos el segundo punto: $\left( 3, -\frac{1}{2}, \frac{1}{2} \right)$

Ahora, podemos determinar un vector director de dicha recta:
$$
\vec{u} = (5, -1, 1) - \left( 3, -\frac{1}{2}, \frac{1}{2} \right) = \left( 5 - 3, -1 - \left( -\frac{1}{2} \right), 1 - \frac{1}{2} \right) = \left( 2, -\frac{1}{2}, \frac{1}{2} \right)
$$

Proseguimos con la siguiente recta:
$$
\begin{cases}
2x + y + 2z + 5 = 0 \\
2x - 2y - z + 2 = 0
\end{cases}
$$

Ahora, le restaremos la recta 2 a la recta 1:
$$
3y + 3z + 3 = 0 \implies 3y + 3z = -3
$$
Podemos considerar $y = -1$ y $z = 0$, teniendo que establecer $x = -2$. Es así que obtenemos el punto $(-2, -1, 0)$.

Ahora, tomamos $y = 0$ y $z = -1$, determinando $x = -\frac{3}{2}$. El otro punto a considerar es $\left( -\frac{3}{2}, 0, -1 \right)$

Determinamos el vector director de la segunda recta:
$$
\vec{v} = \left( -\frac{3}{2}, 0, -1 \right) - (-2, -1, 0) = \left( -\frac{3}{2} - (-2), 0 - (-1), -1 - 0 \right) = \left( \frac{1}{2}, 1, -1 \right)
$$

Tenemos los dos vectores $\vec{u} = \left( 2, -\frac{1}{2}, \frac{1}{2} \right)$ y $\vec{v} = \left( \frac{1}{2}, 1, -1 \right)$. Ahora, queda desarrollar el producto escalar de ambos y determinar que, efectivamente, es 0:
$$
u \cdot v = \left( 2, -\frac{1}{2}, \frac{1}{2} \right) \cdot \left( \frac{1}{2}, 1, -1 \right) = 2 \times \frac{1}{2} + \left( -\frac{1}{2} \right) \times 1 + \frac{1}{2} \times (-1) = 1 - \frac{1}{2} - \frac{1}{2} = 0
$$

En conclusión, las rectas
$$
\begin{cases}
x + y - 3z - 1 = 0 \\
2x - y - 9z - 2 = 0
\end{cases}, \begin{cases}
2x + y + 2z + 5 = 0 \\
2x - 2y - z + 2 = 0
\end{cases}
$$
son ortogonales.

---
## Ejercicio 2.3
Sabiendo que es perpendicular al plano $2x + y = 0$, sabemos que un vector normal de dicho plano es vector director de la recta que estamos buscando. De esta forma, y analizando la ecuación implícita del plano, podemos considerar el vector $(2, 1, 0)$.

Es así que, sabiendo que la recta pasa por el punto $(4, 4, 4)$, desarrollamos la ecuación vectorial:
$$
R = (4, 4, 4) + \lambda(2, 1, 0)
$$
y paramétrica:
$$
\begin{cases}
x = 4 + 2\lambda \\
y = 4 + \lambda \\
z = 4
\end{cases}
$$
Podemos ver que todos los puntos de la recta tendrán $z = 4$. Nos queda expresar todo en base a $\lambda$:
$$
\begin{align}
&x = 4 + 2\lambda \implies \lambda = \frac{1}{2}x - 2 \\
&y = 4 + \lambda \implies \lambda = y - 4
\end{align}
$$
De esta forma:
$$
\frac{1}{2}x - 2 = y - 4 \implies \frac{1}{2}x - y + 2 = 0 \underbrace{ \implies }_{ \times 2 } x - 2y + 4 = 0
$$

Es así que llegamos a la ecuación implícita:
$$
\begin{cases}
x - 2y = -4 \\
z = 4
\end{cases}
$$
y a la ecuación paramétrica:
$$
\begin{cases}
x = 4 + 2\lambda \\
y = 4 + \lambda \\
z = 4
\end{cases}
$$

---
## Ejercicio 2.4
### Parte d)
Primeramente, sabemos que $(3, -2, -1)$ es un vector ortogonal al posible vector director de la recta que queremos determinar. Para esto, aprovecharemos las propiedades del producto vectorial, sabiendo que:
$$
u \cdot v = 0 \implies u \perp v
$$
De esta forma:
$$
(3, -2, -1) \cdot (x, y, z) = 0 \implies 3x - 2y - z = 0
$$
De esta forma, podemos considerar el vector $(1, 1, 1)$, puesto que $3 - 2 - 1 = 0$.

Entonces, teniendo el punto $(-4, -5, 3)$ y el vector director $(1, 1, 1)$, podemos desarrollar las ecuaciones vectorial y paramétrica:
$$
R = (-4, -5, 3) + \lambda(1, 1, 1)
$$
$$
\begin{cases}
x = -4 + \lambda \\
y = -5 + \lambda \\
z = 3 + \lambda
\end{cases}
$$
Ahora, desarrollaremos la ecuación implícita:
$$
z = 3 + \lambda \implies \lambda = z - 3
$$
$$
\begin{align}
&x = -4 + \lambda \implies x = -4 + z - 3 \implies x - z = -7 \\
&y = -5 + \lambda \implies y = -5 + z - 3 \implies y - z = -8
\end{align}
$$
En conclusión, la ecuación implícita es:
$$
\begin{cases}
x - z = -7 \\
y - z = -8
\end{cases}
$$
y la ecuación paramétrica es:
$$
\begin{cases}
x = -4 + \lambda \\
y = -5 + \lambda \\
z = 3 + \lambda
\end{cases}
$$
ERROR: ENCONTRAMOS UNA RECTA QUE ES PERPENDICULAR A LA ESPECIFICADA, PERO NO LA INTERSECTA. PARA COMPLETAR EL EJERCICIO, NO BASTA CON QUE LOS VECTORES DIRECTORES SEAN ORTOGONALES, LAS RECTAS TAMBIÉN DEBEN INTERSECTARSE EN UN PUNTO.

Sabemos que cualquier punto de la recta dada tiene la siguiente forma:
$$
Q = (-1 + 3\lambda, -3 - 2\lambda, 2 - \lambda)
$$
Entonces, estamos buscando un vector director de la siguiente forma:
$$
\vec{v} = \vec{P_{0}Q} = Q - P_{0} = ((-1 + 3\lambda) - (-4), (-3 - 2\lambda) - (-5), (2 - \lambda) - 3) = (3 + 3\lambda, 2 - 2\lambda, -1 - \lambda)
$$
El vector $\vec{v}$ debe ser perpendicular al vector $\vec{u} = (3, -2, -1)$. Por lo tanto, el producto escalar entre ambos debe ser 0:
$$
v \cdot u = 0 \implies (3 + 3\lambda, 2 - 2\lambda, -1 - \lambda) \cdot (3, -2, -1) = 0
$$
$$
\begin{align}
&3(3 + 3\lambda) - 2(2 - 2\lambda) - (-1 - \lambda) = 0 \\
&9 + 9\lambda - 4 + 4\lambda + 1 + \lambda = 0 \\
&6 + 14\lambda = 0
\end{align}
$$
$$
\begin{align}
\implies &14\lambda = -6 \\
&\lambda = -\frac{6}{14} \\
&\lambda = -\frac{3}{7}
\end{align}
$$
De esta forma, el vector director que utilizaremos es:
$$
\begin{align}
\vec{v} &= (3 + 3\lambda, 2 - 2\lambda, -1 - \lambda) \\
&= \left( 3 + 3\left( -\frac{3}{7} \right), 2 - 2\left( -\frac{3}{7} \right), -1 - \left( -\frac{3}{7} \right) \right) \\
&= \left( 3 - \frac{9}{7}, 2 + \frac{6}{7}, -1 + \frac{3}{7} \right) \\
&= \left( \frac{21}{7} - \frac{9}{7}, \frac{14}{7} + \frac{6}{7}, -\frac{7}{7} + \frac{3}{7} \right) \\
&= \left( \frac{12}{7}, \frac{20}{7}, -\frac{4}{7} \right) \\
&= \left( \frac{12}{7}, \frac{20}{7}, -\frac{4}{7} \right) \times \frac{7}{4} \\
&= \left( 3, 5, -1 \right)
\end{align}
$$

Ahora, podemos definir la ecuación vectorial y paramétrica:
$$
R = (-4, -5, 3) + \lambda(3, 5, -1)
$$
$$
\begin{cases}
x = -4 + 3\lambda \\
y = -5 + 5\lambda \\
z = 3 - \lambda
\end{cases}
$$
$$
z = 3 - \lambda \implies \lambda = 3 - z
$$
$$
\begin{align}
&x = -4 + 3\lambda \implies x = -4 + 3(3 - z) = -4 + 9 - 3z = 5 - 3z \implies x + 3z = 5 \\
&y = -5 + 5\lambda \implies y = -5 + 5(3 - z) = -5 + 15 - 5z = 10 - 5z \implies y + 5z = 10
\end{align}
$$
En conclusión, determinamos la ecuación implícita:
$$
\begin{cases}
x + 3z = 5 \\
y + 5z = 10
\end{cases}
$$
y la ecuación paramétrica:
$$
\begin{cases}
x = -4 + 3\lambda \\
y = -5 + 5\lambda \\
z = 3 - \lambda
\end{cases}
$$

---
# 3 - Distancias entre elementos geométricos
## Ejercicio 3.2
### Parte b)
$$
\begin{align}
&\pi_{1} : x + 2y - z = 1 \\
&\pi_{2} : 2x + 4y - 2z = -1
\end{align}
$$
Esta es la situación más sencilla en la que se presenta el cálculo de distancia entre dos objetos, puesto que la distancia es diferente de 0 únicamente en el caso en el que los planos son paralelos no coincidentes.
Habiendo dicho esto, como los planos son paralelos, basta con considerar una recta perpendicular a ambos planos, los puntos en los que corta, y calcular la norma del vector que vincula a ambos puntos.
Primero, simplificaremos la escritura de $\pi_{2}$ para asemejarla a $\pi_{1}$:
$$
\pi_{2} : x + 2y - z = -\frac{1}{2}
$$
Ahora, sabiendo que un vector normal a ambas es $(1, 2, -1)$, y considerando un punto cualquiera perteneciente a alguna de las rectas, como $(1, 0, 0) \in \pi_{1}$, podemos determinar la ecuación vectorial y paramétrica de una recta perpendicular a ambos planos:
$$
R = (1, 0, 0) + \lambda(1, 2, -1)
$$
$$
R = \begin{cases}
x = 1 + \lambda \\
y = 2\lambda \\
z = -\lambda
\end{cases}
$$
$$
\lambda = -z \implies \begin{cases}
x = 1 - z \\
y = -2z
\end{cases}
$$
$$
R = \begin{cases}
x + z = 1 \\
y + 2z = 0
\end{cases}
$$
Ahora, tenemos que encontrar el punto de corte entre $R$ y $\pi_{2}$:
$$
\begin{cases}
x + 2y - z = -\frac{1}{2} \\
x + z = 1 \\
y + 2z = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & -\frac{1}{2} \\
1 & 0 & 1 & 1 \\
0 & 1 & 2 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
0 & 2 & -2 & -\frac{3}{2} \\
1 & 0 & 1 & 1 \\
0 & 1 & 2 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 2 & -2 & -\frac{3}{2} \\
1 & 0 & 1 & 1 \\
0 & 3 & 0 & -\frac{3}{2}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 2 & -2 & -\frac{3}{2} \\
1 & 0 & 1 & 1 \\
0 & 1 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{3}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & -2 & -\frac{1}{2} \\
1 & 0 & 1 & 1 \\
0 & 1 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1}{4} \\
1 & 0 & 1 & 1 \\
0 & 1 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow -\frac{1}{2}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1}{4} \\
1 & 0 & 0 & \frac{3}{4} \\
0 & 1 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
De esta forma, determinamos que $R \cap \pi_{2} = \left( \frac{3}{4}, -\frac{1}{2}, \frac{1}{4} \right)$
Es así que tenemos los puntos entre los cuales tenemos que determinar la distancia: $\left( \frac{3}{4}, -\frac{1}{2}, \frac{1}{4} \right)$ y $(1, 0, 0)$
Consideraremos el siguiente vector:
$$
(1, 0, 0) - \left( \frac{3}{4}, -\frac{1}{2}, \frac{1}{4} \right) = \left( 1 - \frac{3}{4}, 0 - \left( -\frac{1}{2} \right), 0 - \frac{1}{4} \right) = \left( \frac{1}{4}, \frac{1}{2}, -\frac{1}{4} \right)
$$
De esta forma, el vector resultante es $\left( \frac{1}{4}, \frac{1}{2}, -\frac{1}{4} \right)$. Por lo tanto, basta con calcular la norma de dicho vector para determinar la distancia entre ambos planos:
$$
||\left( \frac{1}{4}, \frac{1}{2}, -\frac{1}{4} \right)|| = \sqrt{ \left( \frac{1}{4} \right)^{2} + \left( \frac{1}{2} \right)^{2} + \left( -\frac{1}{4} \right)^{2} } = \sqrt{ \frac{1}{16} + \frac{1}{4} + \frac{1}{16} } = \sqrt{ \frac{1}{8} + \frac{2}{8} } = \sqrt{ \frac{3}{8} }
$$
En conclusión, la distancia entre $\pi_{1}$ y $\pi_{2}$ es $\sqrt{ \frac{3}{8} } = \frac{\sqrt{ 3 }}{2\sqrt{ 2 }}$.

ACLARACIÓN: COMO DIJIMOS DESDE UN PRINCIPIO, LA NOCIÓN DE DISTANCIA DE PLANOS SOLO TIENE SENTIDO SI LOS MISMOS SON PARALELOS NO COINCIDENTES. ESTO QUIERE DECIR QUE SUS ECUACIONES SON IDENTICAS, SOLO DIFERENCIANDOSE POR EL TÉRMINO INDEPENDIENTE. POR ESTA RAZÓN, EXISTE UNA FÓRMULA PARA SIMPLIFICAR EL CÁLCULO DE LA DISTANCIA ENTRE AMBOS:
$$
d(\pi_{1}, \pi_{2}) = \frac{|D_{1} - D_{2}|}{||n||}
$$
SIENDO $D_{1}$ Y $D_{2}$ LOS TÉRMINOS INDEPENDIENTES DE LAS ECUACIONES IMPLÍCITAS DE CADA PLANO, Y $||n||$ LA NORMA DEL VECTOR NORMAL A DICHOS PLANOS (COINCIDE EN CASO DE QUE LAS ECUACIONES ESTÉN SIMPLIFICADAS).


---
## Ejercicio 3.3
### Parte b)
Tenemos la ecuación de la recta: $\pi : x = 0$. De esta forma, sabemos que un vector normal a dicho plano es $(1, 0, 0)$. Considerando este vector y el punto $(2, 3, 4)$, podemos formar una recta perpendicular a $\pi$ que pase por $(2, 3, 4)$:
$$
r = (2, 3, 4) + \lambda(1, 0, 0)
$$
$$
r = \begin{cases}
x = 2 + \lambda \\
y = 3 \\
z = 4
\end{cases}
$$
Simplemente observando la ecuación paramétrica, podemos determinar que la ecuación implícita es:
$$
r = \begin{cases}
y = 3 \\
z = 4
\end{cases}
$$
Observando las ecuaciones implícitas de $\pi : x = 0$ y $r = \begin{cases} y = 3 \\ z = 4 \end{cases}$, podemos ver que $\pi \cap r = (0, 3, 4)$.
Teniendo los puntos $(0, 3, 4)$ y $(2, 3, 4)$, podemos determinar el vector formado por ambos, y su norma será la distancia entre $P$ y $\pi$:
$$
(2, 3, 4) - (0, 3, 4) = (2 - 0, 3 - 3, 4 - 4) = (2, 0, 0)
$$
$$
||(2, 0, 0)|| = \sqrt{ 2^{2} + 0^{2} + 0^{2} } = \sqrt{ 4 } = 2
$$
De esta forma, la distancia entre el punto $P = (2, 3, 4)$ y el plano $\pi : x = 0$ es 2.

---
## Ejercicio 3.4
### Parte a)
Determinar la distancia entre dos rectas es quizás el caso más complejo, puesto que no sabemos como están distribuidas las mismas en el plano, por lo que desconocemos cual es la región "más cercana" entre ambas. Básicamente, tenemos que determinar una recta que intercepte a ambas perpendicularmente (solo existe una), considerar los puntos de intersección, formar un vector con ambos y calcular la norma de ese vector.

Tenemos las rectas
$$
\begin{align}
&r : (x, y, z) = (1, 2, 3) + \lambda(1, 0, 0) \\
&s : (x, y, z) = (3, 0, 0) + \mu(0, 1, 1)
\end{align}
$$

Teniendo las ecuaciones paramétricas de las rectas, podemos expresar el valor de cualquier punto de las rectas considerando los parámetros $\lambda$ y $\mu$. Denominaremos $R \in r$ y $S \in s$:
$$
\begin{align}
&R = (1 + \lambda, 2, 3) \\
&S = (3, \mu, \mu)
\end{align}
$$

Sabiendo que un vector director de $r$ es $(1, 0, 0)$ y un vector director de $s$ es $(0, 1, 1)$, tenemos que considerar que un vector director de la recta que estamos buscando será perpendicular a ambos. Para esto, utilizaremos el producto escalar, considerando que el vector $R - S$ es el vector director que estamos buscando:
$$
\begin{cases}
R - S \cdot (1, 0, 0) = 0 \\
R - S \cdot (0, 1, 1) = 0
\end{cases}
$$
$$
(1 + \lambda, 2, 3) - (3, \mu, \mu) = (1 + \lambda - 3, 2 - \mu, 3 - \mu) = (-2 + \lambda, 2 - \mu, 3 - \mu)
$$
$$
\implies \begin{cases}
(-2 + \lambda, 2 - \mu, 3 - \mu) \cdot (1, 0, 0) = 0 \\
(-2 + \lambda, 2 - \mu, 3 - \mu) \cdot (0, 1, 1) = 0
\end{cases}
$$
Desarrollamos cada una de las ecuaciones:
$$
\begin{align}
(-2 + \lambda, 2 - \mu, 3 - \mu) \cdot (1, 0, 0) &= 0 \\
-2 + \lambda &= 0 \\
\lambda &= 2
\end{align}
$$
$$
\begin{align}
(-2 + \lambda, 2 - \mu, 3 - \mu) \cdot (0, 1, 1) &= 0 \\
2 - \mu + 3 - \mu &= 0 \\
5 - 2\mu &= 0 \\
2\mu &= 5 \\
\mu &= \frac{5}{2}
\end{align}
$$
Ahora que logramos determinar los valores de los parámetros $\lambda$ y $\mu$, podemos calcular $R - S$:
$$
(-2 + \lambda, 2 - \mu, 3 - \mu)
$$
$$
\begin{align}
&= \left( -2 + 2, 2 - \frac{5}{2}, 3 - \frac{5}{2} \right) \\
&= \left( 0, -\frac{1}{2}, \frac{1}{2} \right)
\end{align}
$$
De esta manera, el vector dado por los puntos más cercanos de las rectas $r$ y $s$ es $\left( 0, -\frac{1}{2}, \frac{1}{2} \right)$.

Simplemente resta calcular la norma de dicho vector:
$$
\left|\left| \left( 0, -\frac{1}{2}, \frac{1}{2} \right) \right|\right| = \sqrt{ 0^{2} + \left( -\frac{1}{2} \right)^{2} + \left( \frac{1}{2} \right)^{2} } = \sqrt{ \frac{1}{4} + \frac{1}{4} } = \sqrt{ \frac{1}{2} } = \frac{1}{\sqrt{ 2 }}
$$

De esta forma, la distancia entre las rectas $r$ y $s$ es $\frac{1}{\sqrt{ 2 }}$.

ACLARACIÓN: LA NORMA DEL VECTOR DIRECTOR QUE DETERMINAMOS COINCIDE CON LA DISTANCIA MÍNIMA ENTRE LAS RECTAS $r$ Y $s$, POR LA FORMA EN LA QUE LO DETERMINAMOS. SI HUBIERMOS DETERMINADO UN VECTOR DIRECTOR GENÉRICO (DESARROLLANDO EL PRODUCTO VECTORIAL DE CADA VECTOR DIRECTOR POR UN VECTOR GENÉRICO), HUBIERAMOS OBTENIDO LOS VALORES GENERICOS DE CADA COMPONENTE, POR EJEMPLO:
$$
\begin{cases}
(x, y, z) \cdot (1, 0, 0) = 0 \implies x = 0 \\
(x, y, z) \cdot (0, 1, 1) = 0 \implies y + z = 0 \implies y = -z
\end{cases}
$$
ASÍ, PODRÍAMOS HABER LLEGADO A UN VECTOR CON LA MISMA DIRECCIÓN, COMO $(0, 1, -1)$. SIN EMBARGO, ESTE NO COINCIDE CON EL VECTOR PUNTUAL QUE ESTAMOS BUSCANDO.

TAMBIÉN EXISTE UNA FÓRMULA PARA DETERMINAR LA DISTANCIA ENTRE DOS RECTAS $r$ Y $s$, CON PUNTOS $P, Q$ Y VECTORES $u, v$:
$$
d(r, s) = \frac{|\langle PQ, u \land v \rangle|}{||u \land v||}
$$
APLICADA A ESTE EJERCICIO:
$$
\begin{align}
&PQ = (3, 0, 0) - (1, 2, 3) = (2, -2, -3) \\
&u \land v = (1, 0, 0) \land (0, 1, 1) = (0, -1, 1)
\end{align}
$$
$$
d(r, s) = \frac{|(2, -2, -3) \cdot (0, -1, 1)|}{\sqrt{ 0^{2} + (-1)^{2} + 1^{2} }} = \frac{|0 + 2 - 3|}{\sqrt{ 2 }} = \frac{1}{\sqrt{ 2 }}
$$
