# Ejercicio 1
Estudiemos los puntos en común de las rectas:
Primero, pasemos todas a la ecuación paramétrica:
$$
s : \begin{cases}
x - y = 1 \\
z - x = 1
\end{cases}
$$
$$
(1, 0, 2), (0, -1, 1) \in s
$$
$$
\vec{u} = (1, 0, 2) - (0, -1, 1) = (1 - 0, 0 - (-1), 2 - 1) = (1, 1, 1)
$$
$$
s : \begin{cases}
x = 1 + \lambda \\
y = \lambda \\
z = 2 + \lambda
\end{cases}
$$
Como vemos, un vector director de $s$ es $(1, 1, 1)$, diferente de $(1, 0, 1)$, vector director de $r$, por lo tanto no son paralelas (descartando las opciones b y c).

Para determinar si son perpendiculares, tenemos que desarrollar el producto escalar de ambos vectores:
$$
(1, 1, 1) \cdot (1, 0, 1) = 1 \cdot 1 + 1 \cdot 0 + 1 \cdot 1 = 1 + 0 + 1 = 2
$$
Como es diferente de 0, no son perpendiculares, descartando la opción d.

Ahora, tenemos que ver si $s$ y $y$ se cortan en un punto para comprobar la opción e:
$$
s : \begin{cases}
x - y = 1 \\
z - x = 1
\end{cases}
$$
$$
t : \begin{cases}
x - 2z = -4 \\
y - 2z = -5
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 0 & 1 \\
-1 & 0 & 1 & 1 \\
1 & 0 & -2 & -4 \\
0 & 1 & -2 & -5
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 0 & 1 \\
0 & 0 & -1 & -3 \\
1 & 0 & -2 & -4 \\
0 & 1 & -2 & -5
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 0 & 1 \\
0 & 0 & 1 & 3 \\
1 & 0 & -2 & -4 \\
0 & 1 & -2 & -5
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 0 & 1 \\
0 & 0 & 1 & 3 \\
1 & 0 & 0 & 2 \\
0 & 1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + 2F_{2} \\
&F_{4} \leftarrow F_{4} + 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 2 \\
0 & 1 & 0 & 1 \\
1 & -1 & 0 & 1 \\
0 & 0 & 1 & 3
\end{array}
\right)
\begin{align}
&F_{1} \longleftrightarrow F_{3} \\
&F_{2} \longleftrightarrow F_{4}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 2 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 3 \\
1 & -1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{3} \longleftrightarrow F_{4}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 2 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 3 \\
0 & -1 & 0 & -1
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 2 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 3 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} + F_{2}
\end{align}
$$
De esta forma, llegamos a una única solución: $(2, 1, 3)$.
Por lo tanto, $s \cap t = (2, 1, 3) \neq \emptyset$, demostrando que la opción a es incorrecta.

## Opción correcta: e - Las rectas se cortan en un punto: $r \cap s \cap t = (2, 1, 3)$

---
# Ejercicio 2
Queremos determinar
$$
||u|| = \sqrt{ u_{1}^{2} + u_{2}^{2} + u_{3}^{2} }
$$

Sabemos que
$$
u - v \perp u + v
$$
Por lo tanto:
$$
(u - v) \cdot (u + v)
$$

Además:
$$
\langle v, (-1, -1, 1) \rangle = 9 \land \theta = \frac{\pi}{6}
$$
Entonces:
$$
\langle v, (-1, -1, 1) \rangle = ||v|| \cdot ||(-1, -1, 1)|| \cdot \cos\left( \frac{\pi}{6} \right) = 9
$$
$$
\begin{align}
&||(-1, -1, 1)|| = \sqrt{ (-1)^{2} + (-1)^{2} + 1^{2} } = \sqrt{ 1 + 1 + 1 } = \sqrt{ 3 } \\
&\cos\left( \frac{\pi}{6} \right) = \frac{\sqrt{ 3 }}{2}
\end{align}
$$
$$
\begin{align}
\implies &||v|| \cdot \sqrt{ 3 } \cdot \frac{\sqrt{ 3 }}{2} = 9 \\
&||v|| \cdot \frac{3}{2} = 9 \\
&||v|| = 9 \cdot \frac{2}{3} \\
&||v|| = \frac{18}{3} \\
&||v|| = 6
\end{align}
$$
Volvemos a $u - v \perp u + v$:
$$
\begin{align}
&u - v = (u_{1} - v_{1}, u_{2} - v_{2}, u_{3} - v_{3}) \\
&u + v = (u_{1} + v_{1}, u_{2} + v_{2}, u_{3} + v_{3}) \\
\end{align}
$$
$$
(u - v) \cdot (u + v) = 0
$$
$$
\begin{align}
\implies &u \cdot u + \cancel{ u \cdot v } - \cancel{ v \cdot u } - v \cdot v = 0 \\
&u \cdot u - v \cdot v = 0 \\
&||u||^{2} - ||v||^{2} = 0 \\
&||u||^{2} = ||v||^{2} \\
&||u||^{2} = 6^{2} \\
&||u||^{2} = 36 \\
&||u|| = \sqrt{ 36 } \\
&||u|| = 6
\end{align}
$$
En conclusión:
$$
||u|| = 6
$$

---
# Ejercicio 3
Expresemos a $Q$ como un punto del plano, considerando la siguiente ecuación vectorial:
$$
\pi := (0, 3, 1) + \lambda(1, 1, 1) + \mu (5, 1, -1)
$$
Entonces, sabemos que los puntos pertenecientes a $\pi$ tendrán la forma:
$$
Q = (\lambda + 5\mu, 3 + \lambda + \mu, 1 + \lambda - \mu)
$$
Sabemos que
$$
dist(P, Q) = dist(P, \pi)
$$

Ahora, podemos determinar un vector perpendicular al plano para obtener una recta perpendicular al mismo si desarrollamos el producto vectorial entre los dos vectores directores del plano (considerando el determinante $$
\left|
\begin{array}{ccc}
i & j & k \\
1 & 1 & 1 \\
5 & 1 & -1
\end{array}
\right|
$$
):
$$
v_{1} \land v_{2} = (-1 - 1, -(-1 - 5), 1 - 5) = (-2, 6, -4)
$$
Simplificamos el vector y nos quedamos con $(1, -3, 2)$.

Antes de continuar, necesitamos la ecuación implícita del plano. Sabiendo que un vector normal es $(1, -3, 2)$, y que pasa por el punto $(0, 3, 1)$, podemos expresarla de la siguiente forma:
$$
\begin{align}
\pi &:= 1(x - 0) - 3(y - 3) + 2(z - 1) = 0 \\
&:= x - 0 - 3y + 9 + 2z - 2 = 0 \\
&:= x - 3y + 2z +7 = 0
\end{align}
$$
$$
\pi := x - 3y + 2z + 7 = 0
$$

Ahora, consideraremos la recta $r$ que pasa por $P$ y tiene como vector director a $(1, -3, 2)$:
$$
r := (2, 7, -1) + \lambda(1, -3, 2)
$$
$$
r := \begin{cases}
x = 2 + \lambda \\
y = 7 - 3\lambda \\
z = -1 + 2\lambda
\end{cases}
$$

Lo que prosigue es determinar el punto de intersección entre $r$ y $\pi$, sustituyendo las equivalencias establecidas en cada coordenada de la ecuación de $r$ en la ecuación de $\pi$:
$$
\begin{align}
&x - 3y + 2z +7 = 0 \\
&2 + \lambda - 3(7 - 3\lambda) + 2(-1 + 2\lambda) + 7 = 0 \\
&2 + \lambda - 21 + 9\lambda - 2 + 4\lambda + 7 = 0 \\
&-14 + 14\lambda = 0 \\
&14\lambda = 14 \implies \lambda = \frac{14}{4} = 1
\end{align}
$$
Sabiendo que $\lambda = 1$ para el punto $r \cap \pi$, entonces para determinar las coordenadas de $Q$ (sabiendo que $Q = r \cap \pi$) tenemos que sustituir dicho valor de $\lambda$ en la ecuación paramétrica de $r$:
$$
\begin{cases}
x = 2 + 1 = 3 \\
y = 7 - 3 \times 1 = 4 \\
z = -1 + 2 \times 1 = 1
\end{cases}
$$
De esta forma:
$$
Q = (3, 4, 1)
$$
Por lo tanto, la suma de las coordenadas de $Q$ equivale a:
$$
3 + 4 + 1 = 8
$$
En conclusión:
$$
Q = (3, 4, 1) \text{ y } 3 + 4 + 1 = 8
$$
