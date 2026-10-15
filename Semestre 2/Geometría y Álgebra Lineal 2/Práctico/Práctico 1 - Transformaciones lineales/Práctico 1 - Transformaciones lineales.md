# 1 - Transformaciones lineales
## Ejercicio 1
### Parte 1
Básicamente, tenemos que hallar las expresiones analíticas. Para esto, operaremos buscando obtener las transformaciones de los elementos de la base canónica de $T$ y $S$:
$$
B_{\text{canónica}} (\mathbb{R}^{2}) = \{ (1, 0), (0, 1) \}
$$

Comenzamos por $T(x, y)$:
$$
T(1, 1) = (1, 2) \land T(-1, 1) = (0, 1)
$$
$$
\begin{align}
\text{Dado que } (1, 0) = \frac{1}{2}((1, 1) - (-1, 1)) \implies &T(1, 0) = \frac{1}{2}(T(1, 1) - T(-1, 1)) \\
&T(1, 0) = \frac{1}{2}((1, 2) - (0, 1)) \\
&T(1, 0) = \frac{1}{2}(1, 1) \\
&T(1, 0) = \left( \frac{1}{2}, \frac{1}{2} \right)
\end{align}
$$
$$
\begin{align}
\text{Dado que } (0, 1) = \frac{1}{2}((1, 1) + (-1, 1)) \implies &T(0, 1) = \frac{1}{2}(T(1, 1) + T(-1, 1)) \\
&T(0, 1) = \frac{1}{2}((1, 2) + (0, 1)) \\
&T(0, 1) = \frac{1}{2}(1, 3) \\
&T(0, 1) = \left( \frac{1}{2}, \frac{3}{2} \right)
\end{align}
$$

De esta forma:
$$
T(x, 0) = \left( \frac{1}{2}x, \frac{1}{2}x \right) \land T(0, y) = \left( \frac{1}{2}y, \frac{3}{2}y \right)
$$
$$
\implies T(x, y) = T(x, 0) + T(0, y) = \left( \frac{1}{2}x, \frac{1}{2}x \right) + \left( \frac{1}{2}y, \frac{3}{2}y \right) = \left( \frac{1}{2}x + \frac{1}{2}y, \frac{1}{2}x + \frac{3}{2}y \right) = \left( \frac{1}{2}(x + y), \frac{1}{2}(x + 3y) \right)
$$

Prosigamos a encontrar $S(x, y)$:
$$
S(1, 1) = (1, 1) \land S(0, 1) = (0, 4)
$$
$$
\begin{align}
\text{Dado que } (1, 0) = (1, 1) - (0, 1) \implies &S(1, 0) = S(1, 1) - S(0, 1) \\
&S(1, 0) = (1, 1) - (0, 4) \\
&S(1, 0) = (1, -3)
\end{align}
$$

De esta forma:
$$
S(x, 0) = (x, -3x) \land S(0, y) = (0, 4y)
$$
$$
\implies S(x, y) = S(x, 0) + S(0, y) = (x, -3x) + (0, 4y) = (x, -3x + 4y)
$$

En conclusión:
$$
\begin{align}
&T(x, y) = \frac{1}{2}(x + y, x + 3y) \\
&S(x, y) = (x, -3x + 4y)
\end{align} \qquad \forall (x, y) \in \mathbb{R}^{2}
$$

### Parte 2
$$
\begin{align}
S \circ T = S(T(x, y)) &= S\left( \frac{1}{2}(x + y, x + 3y) \right) \\
&= \frac{1}{2}S(x + y, x + 3y) \\
&= \frac{1}{2}(x + y, -3(x + y) + 4(x + 3y)) \\
&= \frac{1}{2}(x + y, -3x - 3y + 4x + 12y) \\
&= \frac{1}{2}(x + y, x + 9y)
\end{align}
$$

$$
\begin{align}
T \circ S = T(S(x, y)) &= T(x, -3x + 4y) \\
&= \frac{1}{2}(x + (-3x + 4y), x + 3(-3x + 4y)) \\
&= \frac{1}{2}(x - 3x + 4y, x - 9x + 12y) \\
&= \frac{1}{2}(-2x + 4y, -8x + 12y) \\
&= (-x + 2y, -4x + 6y)
\end{align}
$$

Como vemos:
$$
S \circ T = \frac{1}{2}(x + y, x + 9y) \neq T \circ S = (-x + 2y, -4x + 6y)
$$

Por esta razón, $S$ y $T$ no conmutan, ya que el orden en el que se aplican importa. No es lo mismo aplicar primero $T$ y luego $S$ que primero $S$ y luego $T$.

### Parte 3
$$
\begin{align}
S \circ S = S(S(x, y)) &= S(x, -3x + 4y) \\
&= (x, -3x + 4(-3x + 4y)) \\
&= (x, -3x - 12x + 16y) \\
&= (x, -15x + 16y)
\end{align}
$$

$$
\begin{align}
T \circ T = T(T(x, y)) &= T\left( \frac{1}{2}(x + y, x + 3y) \right) \\
&= \frac{1}{2} T(x + y, x + 3y) \\
&= \frac{1}{2} (x + y + x + 3y, x + y + 3(x + 3y)) \\
&= \frac{1}{2} (x + y + x + 3y, x + y + 3x + 9y) \\
&= \frac{1}{2} (2x + 4y, 4x + 10y) \\
&= (x + 2y, 2x + 5y)
\end{align}
$$

En conclusión:
$$
\begin{align}
&S \circ S = (x, -15x + 16y) \\
&T \circ T = (x + 2y, 2x + 5y)
\end{align}
$$

---
## Ejercicio 2
Aquí es importante entender que significa considerar a $\mathbb{C}$ como un $\mathbb{R}-E.V.$:
- Dimensión de $\mathbb{C}$ sobre $\mathbb{C}$ es 1, ya que una base es $B_{\mathbb{C}} = \{ 1 \}$.
- Basta con definir a $T(1)$ para conocer la transformación.
- Dimensión de $\mathbb{C}$ sobre $\mathbb{R}$ es 2, ya que una base es $B_{\mathbb{R}} = \{ 1, i \}$.
- Además de $T(1)$, también necesitamos conocer a $T(i)$ para definir a la transformación.
### Parte 1
#### Transformación a
$$
T(3 - i) = (4i) \text{ y } T(-6 + 2i) = (8 + 6i)
$$
$$
(-6 + 2i) = -2(3 - i) \implies T(-6 + 2i) = T(-2(3 - i)) = -2 \cdot T(3 - i)
$$
$$
\begin{align}
T(-6 + 2) &= -2 \cdot T(3 - i) \\
8 + 6i &= -2 \cdot 4i \\
8 + 6i &\neq -8i
\end{align}
$$
Como vemos, no existe una transformación lineal $T : \mathbb{C} \to \mathbb{C}$ considerando a $\mathbb{C}$ como $\mathbb{R}-E.V.$ que satisfaga $T(3 - i) = (4i)$ y $T(-6 + 2i) = (8 + 6i)$.

#### Transformación b
$$
T(2) = (1 + i, 1 - i) \text{ y } T(i) = (1 - i, 1 + i)
$$
Como no existe ninguna relación directa entre $T(2) = 2T(1)$ y $T(i)$, no importa como se transformen dichos valores. Por lo tanto, existe una transformación lineal $T : \mathbb{C} \to \mathbb{C}$ considerando a $\mathbb{C}$ como $\mathbb{R}-E.V.$ que satisfaga $T(2) = (1 + i, 1 - i)$ y $T(i) = (1 - i, 1 + i)$.

$$
\begin{align}
T(x + yi) &= T(x) + T(yi) \\
&= x \cdot T(1) + y \cdot T(i) \\
&= x \cdot \frac{1}{2}T(2) + y \cdot T(i) \\
&= x \cdot \frac{1}{2}(1 + i, 1 - i) + y \cdot (1 - i, 1 + i) \\
&= \left( \frac{1}{2}x + \frac{1}{2}xi, \frac{1}{2}x - \frac{1}{2}xi \right) + (y - yi, y + yi) \\
&= \left( \frac{1}{2}x + y + \left( \frac{1}{2}x - y \right)i, \frac{1}{2}x + y - \left( \frac{1}{2}x - y \right)i \right)
\end{align}
$$
En conclusión:
$$
T(x + yi) = \left( \frac{1}{2}x + y + \left( \frac{1}{2}x - y \right)i, \frac{1}{2}x + y - \left( \frac{1}{2}x - y \right)i \right)
$$

#### Transformación c
$$
T(1 + i) = (1 + i, i) \text{ y } T(-1 + i) = (-1 + i, -1)
$$
No existe ninguna relación entre $(1 + i)$ y $(-1 + i)$ que podamos comparar (no son múltiplos). Por lo tanto, existe una transformación lineal $T : \mathbb{C} \to \mathbb{C}$ considerando a $\mathbb{C}$ como $\mathbb{R}-E.V.$ que satisfaga $T(1 + i) = (1 + i, i)$ y $T(-1 + i) = (-1 + i, -1)$.

Buscamos $T(x + yi)$:
$$
\begin{align}
i &= \frac{1}{2}((1 + i) + (-1 + i)) \\
T(i) &= T(\frac{1}{2}((1 + i) + (-1 + i))) \\
T(i) &= \frac{1}{2}(T(1 + i) + T(-1 + i)) \\
T(i) &= \frac{1}{2}((1 + i, i) + (-1 + i, -1)) \\
T(i) &= \frac{1}{2}(2i, i - 1) \\
T(i) &= \left( i, \frac{1}{2}i - \frac{1}{2} \right)
\end{align}
$$
$$
\begin{align}
1 &= \frac{1}{2}((1 + i) - (-1 + i)) \\
T(1) &= T(\frac{1}{2}((1 + i) - (-1 + i))) \\
T(1) &= \frac{1}{2}(T(1 + i) - T(-1 + i)) \\
T(1) &= \frac{1}{2}((1 + i, i) - (-1 + i, -1)) \\
T(1) &= \frac{1}{2}(2, i + 1) \\
T(1) &= \left( 1, \frac{1}{2}i + \frac{1}{2} \right)
\end{align}
$$
$$
\begin{align}
\implies T(x + yi) &= T(x) + T(yi) \\
&= x \cdot T(1) + y \cdot T(i) \\
&= x \cdot \left( 1, \frac{1}{2}i + \frac{1}{2} \right) + y \cdot \left( i, \frac{1}{2}i - \frac{1}{2} \right) \\
&= \left( x, \frac{1}{2}xi + \frac{1}{2}x \right) + \left( yi, \frac{1}{2}yi - \frac{1}{2}y \right) \\
&= \left( x + yi, \frac{1}{2}(x + y)i + \frac{1}{2}(x - y) \right)
\end{align}
$$

En conclusión:
$$
T(x + yi) = \left( x + yi, \frac{1}{2}(x + y)i + \frac{1}{2}(x - y) \right)
$$

### Parte 2
#### Transformación a
$$
T(3 - i) = (4i) \text{ y } T(-6 + 2i) = (8 + 6i)
$$
No existe una transformación lineal $T : \mathbb{C} \to \mathbb{C}$ considerando a $\mathbb{C}$ como $\mathbb{C}-E.V.$ que satisfaga $T(3 - i) = (4i)$ y $T(-6 + 2i) = (8 + 6i)$ por la verificación realizada anteriormente.

#### Transformación b
$$
T(2) = (1 + i, 1 - i) \text{ y } T(i) = (1 - i, 1 + i)
$$
Aquí tenemos que verificar que $T(i) = i \cdot T(1)$:
$$
\begin{align}
T(i) &= i \cdot T(1) \\
T(i) &= i \cdot \frac{1}{2}T(2) \\
(1 - i, 1 + i) &= i \cdot \frac{1}{2}(1 + i, 1 - i) \\
(1 - i, 1 + i) &= \left( \frac{1}{2}i + \frac{1}{2}i^{2}, \frac{1}{2}i - \frac{1}{2}i^{2} \right) \\
(1 - i, 1 + i) &\neq \left( \frac{1}{2}i - \frac{1}{2}, \frac{1}{2}i + \frac{1}{2} \right)
\end{align}
$$

Como vemos, la igualdad no se cumple. Por lo tanto, no existe una transformación lineal $T : \mathbb{C} \to \mathbb{C}$ considerando a $\mathbb{C}$ como $\mathbb{C}-E.V.$ que satisfaga $T(2) = (1 + i, 1 - i)$ y $T(i) = (1 - i, 1 + i)$.

#### Transformación c
$$
T(1 + i) = (1 + i, i) \text{ y } T(-1 + i) = (-1 + i, -1)
$$
Siguiendo con el razonamiento de la parte 1, tenemos que verificar que $T(i) = i \cdot T(1)$:
$$
\begin{align}
T(i) &= i \cdot T(1) \\
\left( i, \frac{1}{2}i - \frac{1}{2} \right) &= i \cdot \left( 1, \frac{1}{2}i + \frac{1}{2} \right) \\
\left( i, \frac{1}{2}i - \frac{1}{2} \right) &= \left( i, \frac{1}{2}i^{2} + \frac{1}{2}i \right) \\
\left( i, \frac{1}{2}i - \frac{1}{2} \right) &= \left( i, -\frac{1}{2} + \frac{1}{2}i \right) \\
\left( i, \frac{1}{2}i - \frac{1}{2} \right) &= \left( i, \frac{1}{2}i - \frac{1}{2} \right)
\end{align}
$$
Efectivamente, la igualdad se cumple. De esta manera, verificamos que existe una transformación lineal $T : \mathbb{C} \to \mathbb{C}$ considerando a $\mathbb{C}$ como $\mathbb{C}-E.V.$ que satisfaga $T(1 + i) = (1 + i, i)$ y $T(-1 + i) = (-1 + i, -1)$.

En conclusión (por la parte anterior):
$$
T(x + yi) = \left( x + yi, \frac{1}{2}(x + y)i + \frac{1}{2}(x - y) \right)
$$

---
## Ejercicio 3
### Transformación 1
#### Parte a
$$
\begin{align}
T(ax^{3} + bx^{2} + cx + d) &= (a + b + c + d + (-a + b - c + d), d) \\
&= (\cancel{ a } + b + \cancel{ c } + d - \cancel{ a } + b - \cancel{ c } + d, d) \\
&= (2b + 2d, d)
\end{align}
$$
En conclusión:
$$
T(ax^{3} + bx^{2} + cx + d) = T(2b + 2d, d
$$

#### Parte b
$$
Ker(T) = \{ p(x) : p(1) + p(-1) = 0 \land p(0) = 0 \}
$$
$$
\begin{align}
p(x) = ax^{3} + bx^{2} + cx + d &\implies \begin{aligned}
&p(1) = a + b + c + d \\
&p(-1) = -a + b - c + d
\end{aligned} \implies p(1) + p(-1) = 2b + 2d \\
&\implies p(0) = d
\end{align}
$$
Entonces, los polinomios que pertenecen a $Ker(T)$ tienen que cumplir las siguientes condiciones:
$$
\begin{cases}
2b + 2d = 0 \\
d = 0
\end{cases} \implies 2b = 0 \implies b = 0
$$
De esta manera, dichos polinomios tienen la siguiente forma:
$$
p(x) = ax^{3} + cx
$$
Entonces, podemos definir al núcleo como:
$$
Ker(T) = \{ ax^{3} + cx : a, c \in \mathbb{R} \}
$$
Esto nos permite definir una base del núcleo:
$$
B_{Ker(T)} = \{ x, x^{3} \}
$$

Pasamos a estudiar la imagen. Recordemos que la imagen es el subconjunto del codominio que incluye a todos los elementos que tienen una preimagen:
$$
\mathrm{Im}(T) = \{ w \in W : T(v) = w \}, \text{con } v \in V
$$
Un vector $(x, y)$ pertenece a la imagen, si cumple que:
$$
\begin{cases}
x = p(1) + p(-1) = \cancel{ a } + b + \cancel{ c } + d - \cancel{ a } + b - \cancel{ c } + d = 2b + 2d \\
y = p(0) = d
\end{cases}
$$
para algún $p(x) \in \mathbb{R}_{3}[x]$

De esta forma, podemos definir a $\mathrm{Im}(T)$:
$$
\mathrm{Im}(T) = \{ (2b + 2d, d) : b, d \in \mathbb{R} \}
$$
En definitiva, lo expresamos como:
$$
\mathrm{Im}(T) = \{ (b, d) : b, d \in \mathbb{R} \} = \mathbb{R}^{2}
$$
Es así que podemos definir la siguiente base:
$$
B_{\mathrm{Im}(T)} = \{ (1, 0), (0, 1) \}
$$

Todo esto tiene sentido si lo verificamos con el teorema de las dimensiones:
$$
dim(\mathbb{R}_{3}[x]) = 4 = dim(Ker(T)) + dim(\mathrm{Im}(T)) = 2 + 2 = 4
$$

### Transformación 2
#### Parte a
$$
T \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} = a + d
$$

#### Parte b
$$
Ker(T) = \left\{ \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} : tr \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} = a + d = 0 \right\}
$$
Entonces, las matrices que pertenecen a $Ker(T)$ tienen que cumplir las siguientes condiciones:
$$
\begin{cases}
a + d = 0
\end{cases} \implies a = -d
$$
De esta manera, dichas matrices tienen la siguiente forma:
$$
A = \begin{pmatrix}
a & b \\
c & -a
\end{pmatrix}
$$
Entonces, podemos definir al núcleo como:
$$
Ker(T) = \left\{ \begin{pmatrix}
a & b \\
c & -a
\end{pmatrix} : a, b, c \in \mathbb{R} \right\} = \left\{ \begin{pmatrix}
a & 0 \\
0 & -a
\end{pmatrix}, \begin{pmatrix}
0 & b \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
c & 0
\end{pmatrix} : a, b, c \in \mathbb{R} \right\}
$$
Esto nos permite definir una base del núcleo:
$$
B_{Ker(T)} = \left\{ \begin{pmatrix}
1 & 0 \\
0 & -1
\end{pmatrix} + \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} + \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right\}
$$

Pasamos a estudiar la imagen:

Un elemento $x$ pertenece a la imagen, si cumple que:
$$
\begin{cases}
x = tr(A) = a + d
\end{cases} \qquad \left( \text{con } A = \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \right)
$$

De esta forma, podemos definir a $\mathrm{Im}(T)$:
$$
\mathrm{Im}(T) = \{ a + d : a, d \in \mathbb{R} \}
$$
En definitiva, lo expresamos como:
$$
\mathrm{Im}(T) = \{ a : a \in \mathbb{R} \} = \mathbb{R}
$$
Es así que podemos definir la siguiente base:
$$
B_{\mathrm{Im}(T)} = \{ 1 \}
$$

Nuevamente, verificamos con el teorema de las dimensiones:
$$
dim(\mathbb{\mathcal{M}}_{2}(\mathbb{R})) = 4 = dim(Ker(T)) + dim(\mathrm{Im}(T)) = 3 + 1 = 4
$$

---
## Ejercicio 4
### Parte 1
$$
S \left( \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \right) = \begin{pmatrix}
1 & x
\end{pmatrix} \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \begin{pmatrix}
x \\
x^{2}
\end{pmatrix}
$$
$$
\begin{pmatrix}
1 & x
\end{pmatrix} \cdot \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} = \begin{align}
&\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \\

\begin{pmatrix}
1 & x
\end{pmatrix}

&\begin{pmatrix}
a + cx & b + dx
\end{pmatrix}
\end{align}
$$
$$
\begin{pmatrix}
a + cx & b + dx
\end{pmatrix} \cdot \begin{pmatrix}
x \\
x^{2}
\end{pmatrix} = \begin{align}
&\begin{pmatrix}
x \\
x^{2}
\end{pmatrix} \\

\begin{pmatrix}
a + cx & b + dx
\end{pmatrix}

&\begin{pmatrix}
ax + cx^{2} + bx^{2} + dx^{3}
\end{pmatrix}
\end{align}
$$
$$
ax + cx^{2} + bx^{2} + dx^{3} = dx^{3} + (b + c)x^{2} + ax
$$

De esta forma, logramos expresar la imagen de una matriz genérica para la transformación $S$:
$$
S \left( \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \right) = dx^{3} + (b + c)x^{2} + ax
$$

### Parte 2
Básicamente, tenemos que verificar que:
$$
\begin{align}
&T(\alpha u + \beta v) = \alpha T(u) + \beta T(v) \\
&S(\alpha u + \beta v) = \alpha S(u) + \beta S(v)
\end{align}
$$
$$
\begin{align}
T(\alpha (x_{1}, y_{1}, z_{1}) + \beta (x_{2}, y_{2}, z_{2})) &= T((\alpha x_{1}, \alpha y_{1}, \alpha z_{1}) + (\beta x_{2}, \beta y_{2}, \beta z_{2})) \\
&= T((\alpha x_{1} + \beta x_{2}, \alpha y_{1} + \beta y_{2}, \alpha z_{1} + \beta z_{2})) \\
&= \begin{pmatrix}
\alpha x_{1} + \beta x_{2} - \alpha y_{1} - \beta y_{2} & \alpha y_{1} + \beta y_{2} \\
\alpha y_{1} + \beta y_{2} & \alpha y_{1} + \beta y_{2} - \alpha z_{1} - \beta z_{2}
\end{pmatrix} \\
&= \begin{pmatrix}
\alpha x_{1} - \alpha y_{1} & \alpha y_{1} \\
\alpha y_{1} & \alpha y_{1} - \alpha z_{1}
\end{pmatrix} + \begin{pmatrix}
\beta x_{2} - \beta y_{2} & \beta y_{2} \\
\beta y_{2} & \beta y_{2} - \beta z_{2}
\end{pmatrix} \\
&= \alpha \cdot \begin{pmatrix}
x_{1} - y_{1} & y_{1} \\
y_{1} & y_{1} - z_{1}
\end{pmatrix} + \beta \cdot \begin{pmatrix}
x_{2} - y_{2} & y_{2} \\
y_{2} & y_{2} - z_{2}
\end{pmatrix} \\
&= \alpha \cdot T(x_{1}, y_{1}, z_{1}) + \beta \cdot T(x_{2}, y_{2}, z_{2})
\end{align}
$$
$$
\begin{align}
S \left( \alpha \cdot \begin{pmatrix}
a_{1} & b_{1} \\
c_{1} & d_{1}
\end{pmatrix} + \beta \cdot \begin{pmatrix}
a_{2} & b_{2} \\
c_{2} & d_{2}
\end{pmatrix} \right) &= S \left( \begin{pmatrix}
\alpha a_{1} & \alpha b_{1} \\
\alpha c_{1} & \alpha d_{1}
\end{pmatrix} + \begin{pmatrix}
\beta a_{2} & \beta b_{2} \\
\beta c_{2} & \beta d_{2}
\end{pmatrix} \right) \\
&= S \left( \begin{pmatrix}
\alpha a_{1} + \beta a_{2} & \alpha b_{1} + \beta b_{2} \\
\alpha c_{1} + \beta c_{2} & \alpha d_{1} + \beta d_{2}
\end{pmatrix} \right) \\
&= \begin{pmatrix}
1 & x
\end{pmatrix} \cdot \begin{pmatrix}
\alpha a_{1} + \beta a_{2} & \alpha b_{1} + \beta b_{2} \\
\alpha c_{1} + \beta c_{2} & \alpha d_{1} + \beta d_{2}
\end{pmatrix} \cdot \begin{pmatrix}
x \\
x^{2}
\end{pmatrix} \\
&= \begin{pmatrix}
\alpha a_{1} + \beta a_{2} + \alpha x c_{1} + \beta x c_{2} & \alpha b_{1} + \beta b_{2} + \alpha x d_{1} + \beta x d_{2}
\end{pmatrix} \cdot \begin{pmatrix}
x \\
x^{2}
\end{pmatrix} \\
&=
\alpha x a_{1} + \beta x a_{2} + \alpha x^{2} c_{1} + \beta x^{2} c_{2} + \alpha x^{2} b_{1} + \beta x^{2} b_{2} + \alpha x^{3} d_{1} + \beta x^{3} d_{2} \\
&= \alpha (x a_{1} + x^{2} (b_{1} + c_{1}) + x^{3} d_{1}) + \beta (x a_{2} + x^{2} (b_{2} + c_{2}) + x^{3} d_{2}) \\
&= \alpha \cdot S \left( \begin{pmatrix}
a_{1} & b_{1} \\
c_{1} & d_{1}
\end{pmatrix} \right) + \beta \cdot S \left( \begin{pmatrix}
a_{2} & b_{2} \\
c_{2} & d_{2}
\end{pmatrix} \right)
\end{align}
$$

Ahora que verificamos que $T$ y $S$ son lineales, determinaremos la composición $S \circ T$ (ya que la $T \circ S$ propuesta carece de sentido):
$$
\begin{align}
S \circ T &= S(T(a, b, c)) \\
&= S \left( \begin{pmatrix}
a - b & b \\
b & b - c
\end{pmatrix} \right) \\
&= \begin{pmatrix}
1 & x
\end{pmatrix} \cdot \begin{pmatrix}
a - b & b \\
b & b - c
\end{pmatrix} \cdot \begin{pmatrix}
x \\
x^{2}
\end{pmatrix} \\
&= \begin{pmatrix}
a - b + bx & b + bx - cx
\end{pmatrix} \cdot \begin{pmatrix}
x \\
x^{2}
\end{pmatrix} \\
&= ax - bx + bx^{2} + bx^{2} + bx^{3} - cx^{3} \\
&= (b - c)x^{3} + 2bx^{2} + (a - b)x
\end{align}
$$

En conclusión:
$$
S \circ T = S(T(a, b, c)) = (b - c)x^{3} + 2bx^{2} + (a - b)x
$$

### Parte 3
- $Ker(T)$
Para que un vector $(x, y, z)$ pertenezca al núcleo $Ker(T)$, tiene que cumplir:
$$
\begin{cases}
x - y = 0 \\
y = 0 \\
y - z = 0
\end{cases} \implies x = 0 \land z = 0
$$
$$
Ker(T) = \{ (x, y, z) : x, y, z = 0 \} = \{ (0, 0, 0) \} = \{ \vec{0} \}
$$
De esta manera, el único vector que tiene como imagen la matriz nula es $\vec{0}$.

- $Im(T)$
Para que una matriz $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ pertenezca a la imagen $\mathrm{Im}(T)$, tiene que cumplir:
$$
\begin{cases}
a = x - y \\
b = y \\
c = y \\
d = y - z
\end{cases} \implies b = c
$$
$$
\mathrm{Im}(T) = \left\{ \begin{pmatrix}
a & b \\
b & d
\end{pmatrix} : a, b, d \in \mathbb{R} \right\}
$$
De esta manera, podemos definir una base de $\mathrm{Im}(T)$:
$$
B_{\mathrm{Im}(T)} = \left\{ \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\}
$$

- $Ker(S)$
Para que una matriz $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ pertenezca al núcleo $Ker(S)$, tiene que cumplir:
$$
\begin{cases}
a = 0 \\
b + c = 0 \\
d = 0
\end{cases} \implies b = -c
$$
$$
Ker(S) = \left \{ \begin{pmatrix}
0 & b \\
-b & 0
\end{pmatrix} : b \in \mathbb{R} \right \}
$$
Entonces, podemos definir la base:
$$
B_{Ker(S)} = \left \{ \begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix} \right \}
$$

- $Im(S)$
Para que un polinomio $ax^{3} + bx^{2} + cx + d$ pertenezca a la imagen $\mathrm{Im}(S)$, tiene que cumplir:
$$
\begin{cases}
d = 0
\end{cases}
$$
$$
\mathrm{Im}(S) = \{ ax^{3} + bx^{2} + cx : a, b, c \in \mathbb{R} \}
$$
Definimos la base correspondiente:
$$
B_{\mathrm{Im}(S)} = \{ x^{3}, x^{2}, x \}
$$

- $Ker(S \circ T)$
Para que un vector $(a, b, c)$ pertenezca al núcleo $Ker(S \circ T)$, tiene que cumplir:
$$
\begin{cases}
b - c = 0 \\
2b = 0 \implies b = 0 \\
a - b = 0
\end{cases} \implies a = 0 \land c = 0
$$
$$
Ker(S \circ T) = \{ (a, b, c) : a, b, c = 0 \} = \{ (0, 0, 0) \} = \{ \vec{0} \}
$$
De esta manera, el único vector que tiene como imagen la matriz nula es $\vec{0}$.

- $Im(S \circ T)$
Para que un polinomio $ax^{3} + bx^{2} + cx + d$ pertenezca a la imagen $\mathrm{Im}(S \circ T)$, tiene que cumplir:
$$
\begin{cases}
d = 0
\end{cases}
$$
$$
\mathrm{Im}(S \circ T) = \{ ax^{3} + bx^{2} + cx : a, b, c \in \mathbb{R} \}
$$
Definimos la base correspondiente:
$$
B_{\mathrm{Im}(S \circ T)} = \{ x^{3}, x^{2}, x \}
$$

---
En los siguientes dos ejercicios, tendremos que recurrir al teorema de las dimensiones:

> [!Teorema de las dimensiones]
> Sean:
> - $V, W$ espacios vectoriales, con $dim(V) < \infty$ ($V$ con dimensión finita, $W$ puede ser de dimensión finita o infinita).
> - $T : V \to W$ transformación lineal cualquiera.
> 
> <u>Entonces</u>: Los subespacios $\mathrm{Ker}(T)$ e $\mathrm{Im}(T)$ son de dimensión finita, y
> $$
> dim(\mathrm{Ker}(T)) + dim(\mathrm{Im}(T)) = dim(V)
> $$

## Ejercicio 5
### Parte 1
Sabemos que, como $A$ es L.I. y $\# A = r$, entonces $dim(V) \geq r$, pero necesariamente finita para poder recurrir al teorema mencionado.

Que exista un conjunto LI cuyas imágenes de elementos conformen un conjunto LI en el codominio, no garantiza que la transformación lineal sea inyectiva. Lo probaremos con un contraejemplo:

Primero que nada, un conjunto LI puede ser un conjunto con un solo elemento, y dicho elemento siempre se corresponderá con un único elemento del codominio, por lo que ambos conjuntos serán LI siempre. Sin embargo, puede ser que al agregar elementos en el conjunto LI del dominio, se pierda la propiedad de LI en el conjunto del codominio correspondiente.

Ejemplo:
$$
T : \mathbb{R}^{2} \to \mathbb{R}^{3} / (x, y) = (x + y, x + y, x + y)
$$
Consideremos los vectores $(1, 0)$ y $(2, -1)$:
$$
\begin{align}
&T(1, 0) = (1 + 0, 1 + 0, 1 + 0) = (1, 1, 1) \\
&T(2, -1) = (3 - 1, 3 - 1, 3 - 1) = (1, 1, 1)
\end{align}
$$

Si bien $A = \{ (1, 0) \}$ es LI, la transformación lineal no es inyectiva.

En conclusión, el enunciado es falso.

### Parte 2
Consideremos una transformación lineal $T : V \to W$ tal que $B = \{ v_{1}, \dots, v_{n} \}$ es base de $V$ ($dim(V) = n$), y los elementos de dicha base tienen imágenes que también resultan ser LI entre si, o sea $T(B) = \{ T(v_{1}), \dots, T(v_{n}) \}$ es también LI.

Como $B$ es base de $V$, cualquier elemento $v$ de $V$ se expresa de forma única como combinación lineal de los vectores $v_{1}, \dots, v_{n}$:
$$
v = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}
$$
Al estar hablando de una transformación lineal, la misma debe ser lineal (por muy redundante que suene). Por lo tanto, tenemos que poder aplicar la transformación a ambos lados de la igualdad, manteniendo la misma:
$$
\begin{align}
T(v) &= T(\alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}) \\
&= T(\alpha_{1} \cdot v_{1}) + \dots + T(\alpha_{n} \cdot v_{n}) \\
&= \alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n})
\end{align}
$$

Ahora, como sabemos que el conjunto resultante en el codominio $T(B) = \{ T(v_{1}), \dots, T(v_{n}) \}$ también es LI (sin importar si es o no base), significa que ningún vector es redundante, y por lo tanto, cualquier vector que se pueda formar por combinación lineal de estos, se formará de forma única. Esto significa que no existen múltiples combinaciones de $T(v_{1}), \dots, T(v_{n})$ que den como resultado al vector $T(v)$, dicho vector se puede formar por una única combinación, o ninguna (ya que no se especifica que $T(B)$ sea base de $W$, pudiendo suceder que $dim(W) > n$).

De esta manera, como se verifica que
$$
v = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n} \implies T(v) = \alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n})
$$
con $B = \{ v_{1}, \dots, v_{n} \}$ base de $V$ y $T(B) = \{ T(v_{1}), \dots, T(v_{n}) \}$ conjunto LI en $W$, podemos asegurar que cualquier vector transformado $T(v)$ será único en $W$, cumpliéndose que
$$
T(v) = T(u) \implies v = u
$$

En conclusión, la transformación lineal $T : V \to W$ es inyectiva.

---
## Ejercicio 6
### Parte 1
Para probar que $T : V \to W$ no es sobreyectiva, tenemos que demostrar que $\mathrm{Im}(T) \neq W$

Básicamente, tenemos que tomar en cuenta el teorema de las dimensiones, el cual establece que para una transformación lineal $T : V \to W$, con $dim(V) < \infty$, entonces $Ker(T)$ y $\mathrm{Im}(T)$ son de dimensión finita, y
$$
dim(V) = dim(Ker(T)) + dim(\mathrm{Im}(T))
$$

Considerando que $dim(V) < dim(W)$ y $dim(A) \geq 0$ para cualquier espacio vectorial $A$, esto es bastante sencillo:
$$
\begin{align}
dim(V) &< dim(W) \\
dim(Ker(T)) + dim(\mathrm{Im}(T)) &< dim(W) \implies dim(\mathrm{Im}(T)) < dim(W)
\end{align}
$$

En conclusión:
$$
dim(\mathrm{Im}(T)) < dim(W) \implies \mathrm{Im}(T) \neq W
$$
Por lo tanto, $T : V \to W$ no es sobreyectiva.


### Parte 2
Para probar que $S : W \to V$ no es inyectiva, tenemos que demostrar que $\mathrm{Ker}(S) \neq \{ \vec{0} \} \Longleftrightarrow dim(Ker(S)) > 0$

Según el teorema de las dimensiones:
$$
dim(W) = dim(Ker(S)) + dim(\mathrm{Im}(S))
$$
En base a esto, tenemos que probar que:
$$
dim(\mathrm{Im}(S)) < dim(W)
$$


Considerando que $dim(V) < dim(W)$ y $dim(\mathrm{Im}(S)) \leq dim(V)$ para cualquier espacio vectorial $A$, esto es bastante sencillo:
$$
\begin{align}
dim(V) &< dim(W) \\
dim(V) &< dim(Ker(S)) + dim(\mathrm{Im}(S)) \\
dim(V) - dim(\mathrm{Im}(S)) &< dim(Ker(S)) \\
0 \leq dim(V) - dim(\mathrm{Im}(S)) &< dim(Ker(S)) 
\end{align}
$$
Sabiendo que $dim(V) - dim(\mathrm{Im}(S)) \geq 0$, probamos que $dim(Ker(S)) > 0$.

En conclusión, $dim(Ker(S)) > 0 \Longleftrightarrow \mathrm{Ker}(S) \neq \{ \vec{0} \}$, demostrando que $S : W \to V$ no es inyectiva.

---
## Ejercicio 7
### Parte 1
Necesariamente, la transformación lineal está bien definida, ya que no hay "conflictos" en la definición de las operaciones, ya que se especifican $T(1), T(x), T(x^{2})$, siendo $\{ 1, x, x^{2} \}$ base de $\mathbb{R}_{2}[x]$.

### Parte 2
$$
\begin{align}
T(p) &= T(ax^{2} + bx + c) \\
&= T(ax^{2}) + T(bx) + T(c) \\
&= a \cdot T(x^{2}) + b \cdot T(x) + c \cdot T(1) \\
&= a \cdot (0, 0) + b \cdot (1, 1) + c \cdot (1, 0) \\
&= (0, 0) + (b, b) + (c, 0) \\
&= (b + c, b)
\end{align}
$$

### Parte 3
Recordemos para que sirve la matriz asociada:
$$
coord_{\mathcal{B}}(T(v)) = \space _{\mathcal{B}}(T)_{\mathcal{A}} \cdot coord_{\mathcal{A}}(v)
$$
$$
\begin{align}
&coord_{\mathcal{B}}(T(v)) = (\alpha_{1}, \dots, \alpha_{n}) \implies T(v) = \alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n}) \\
&coord_{\mathcal{A}}(v) = (\alpha_{1}, \dots, \alpha_{n}) \implies v = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}
\end{align}
$$

La matriz asociada a $T$ tiene como columnas a las coordenadas en la base $\mathcal{B}$ de las imágenes de cada elemento de la base $\mathcal{A}$. De esta manera, tenemos que determinar las imágenes de los elementos de $\mathcal{A}$, y encontrar sus coordenadas en $\mathcal{B}$, pudiendo determinar la matriz asociada:
$$
\begin{align}
T(1) = (1, 0) = \alpha \cdot (3, -3) + \beta \cdot (5, 0) \implies coord_{\mathcal{B}}(T(1)) = coord_{\mathcal{B}}((1, 0)) = (\alpha, \beta)
\end{align}
$$
$$
\begin{cases}
3 \alpha + 5 \beta = 1 \\
-3 \alpha = 0
\end{cases} \implies \alpha = 0 \implies 5 \beta = 1 \implies \beta = \frac{1}{5}
$$
$$
coord_{\mathcal{B}}(T(1)) = coord_{\mathcal{B}}((1, 0)) = \left( 0, \frac{1}{5} \right)
$$

$$
\begin{align}
T(x) = (1, 1) = \alpha \cdot (3, -3) + \beta \cdot (5, 0) \implies coord_{\mathcal{B}}(T(x)) = coord_{\mathcal{B}}((1, 1)) = (\alpha, \beta)
\end{align}
$$
$$
\begin{cases}
3 \alpha + 5 \beta = 1 \\
-3 \alpha = 1
\end{cases} \implies \alpha = -\frac{1}{3} \implies 5 \beta = 2 \implies \beta = \frac{2}{5}
$$
$$
coord_{\mathcal{B}}(T(x)) = coord_{\mathcal{B}}((1, 1)) = \left( -\frac{1}{3}, \frac{2}{5} \right)
$$

$$
\begin{align}
T(x^{2}) = (0, 0) = \alpha \cdot (3, -3) + \beta \cdot (5, 0) \implies coord_{\mathcal{B}}(T(x^{2})) = coord_{\mathcal{B}}((0, 0)) = (\alpha, \beta)
\end{align}
$$
$$
\begin{cases}
3 \alpha + 5 \beta = 0 \\
-3 \alpha = 0
\end{cases} \implies \alpha = 0 \implies 5 \beta = 0 \implies \beta = 0
$$
$$
coord_{\mathcal{B}}(T(x^{2})) = coord_{\mathcal{B}}((0, 0)) = \left( 0, 0 \right)
$$

De esta forma, podemos concluir definiendo la matriz asociada:
$$
\space _{\mathcal{B}}(T)_{\mathcal{A}} = \begin{pmatrix}
0 & -\frac{1}{3} & 0 \\
\frac{1}{5} & \frac{2}{5} & 0
\end{pmatrix}
$$

---
## Ejercicio 8
### Parte 1
Verificaremos como se transforman los elementos utilizando la matriz asociada:
$$
\begin{align}
coord_{\mathcal{A}}(x_{1}, y_{1}, z_{1}) &= \begin{pmatrix}
1 & 4 & 1 \\
2 & 1 & 1 \\
2 & 1 & 1
\end{pmatrix} \cdot coord_{\mathcal{B}}(x_{2}, y_{2}, z_{2}) \\
\begin{pmatrix}
\alpha_{1} \\
\beta_{1} \\
\gamma_{1}
\end{pmatrix} &= \begin{pmatrix}
1 & 4 & 1 \\
2 & 1 & 1 \\
2 & 1 & 1
\end{pmatrix} \cdot \begin{pmatrix}
\alpha_{2} \\
\beta_{2} \\
\gamma_{2}
\end{pmatrix} \\
\begin{pmatrix}
\alpha_{1} \\
\beta_{1} \\
\gamma_{1}
\end{pmatrix} &= \begin{pmatrix}
\alpha_{2} + 4\beta_{2} + \gamma_{2} \\
2\alpha_{2} + \beta_{2} + \gamma_{2} \\
2\alpha_{2} + \beta_{2} + \gamma_{2}
\end{pmatrix}
\end{align}
$$
$$
\begin{cases}
\alpha_{1} = \alpha_{2} + 4\beta_{2} + \gamma_{2} \\
\beta_{1} = 2\alpha_{2} + \beta_{2} + \gamma_{2} \\
\gamma_{1} = 2\alpha_{2} + \beta_{2} + \gamma_{2}
\end{cases} \implies \beta_{1} = \gamma_{1}
$$
Podemos probar con los elementos de la base:
$$
coord_{\mathcal{A}}(1, -1, 1) = (1, 0, 0) = \begin{cases}
1 = \alpha_{2} + 4\beta_{2} + \gamma_{2} \\
0 = 2\alpha_{2} + \beta_{2} + \gamma_{2} \\
0 = 2\alpha_{2} + \beta_{2} + \gamma_{2}
\end{cases}
$$
$$
coord_{\mathcal{A}}(1, 1, 1) = (0, 1, 0) = \begin{cases}
0 = \alpha_{2} + 4\beta_{2} + \gamma_{2} \\
1 = 2\alpha_{2} + \beta_{2} + \gamma_{2} \\
0 = 2\alpha_{2} + \beta_{2} + \gamma_{2}
\end{cases}
$$
$$
coord_{\mathcal{A}}(1, 0, 0) = (0, 0, 1) = \begin{cases}
0 = \alpha_{2} + 4\beta_{2} + \gamma_{2} \\
0 = 2\alpha_{2} + \beta_{2} + \gamma_{2} \\
1 = 2\alpha_{2} + \beta_{2} + \gamma_{2}
\end{cases}
$$
El segundo y tercer caso son impositbles, por lo que no existe una transformación lineal que satisfaga $M = \space _{\mathcal{A}}(T)_{\mathcal{B}}$.

LO ANTERIOR ES INCORRECTO, A CONTINUACIÓN RESOLVEMOS LA PARTE 1 ADECUADAMENTE:

La teoría establece que, dada cualquier matriz $M$ de tamaño $m \times n$ y dos bases cualesquiera $\mathcal{B}$ (del dominio) y $\mathcal{A}$ (del codominio), siempre se corresponde con una única transformación lineal tal que $M = \space_{\mathcal{A}}(T)_{\mathcal{B}}$.

Esto se cumple ya que las columnas de $M$ son, por definición, las coordenadas en la base de llegada $\mathcal{A}$ de las imágenes de los vectores de la base de partida $\mathcal{B}$:
$$
\begin{align}
&\begin{pmatrix}
1 \\
2 \\
2
\end{pmatrix} = coord_{\mathcal{A}}(T(1, -1, 1)) \\
&\begin{pmatrix}
4 \\
1 \\
1
\end{pmatrix} = coord_{\mathcal{A}}(T(1, 1, 1)) \\
&\begin{pmatrix}
1 \\
1 \\
1
\end{pmatrix} = coord_{\mathcal{A}}(T(1, 0, 0))
\end{align}
$$

Como conocemos las imágenes de cada elemento de una base del dominio, por el Teorema de Existencia y Unicidad de transformaciones lineales, la transformación existe y es única.

Por lo tanto, existe exactamente una transformación lineal $T : \mathbb{R}^{3} \to \mathbb{R}^{3}$ que satisface $M = \space_{\mathcal{A}}(T)_{\mathcal{B}}$.

### Parte 2
A continuación, determinamos su expresión analítica:
$$
\begin{align}
\begin{pmatrix}
1 \\
2 \\
2
\end{pmatrix} = coord_{\mathcal{A}}(T(1, -1, 1)) \implies T(1, -1, 1) &= 1 \cdot (1, 2, 0) + 2 \cdot (2, 1, 0) + 2 \cdot (1, 1, 1) \\
&= (1, 2, 0) + (4, 2, 0) + (2, 2, 2) \\
&= (7, 6, 2)
\end{align}
$$

$$
\begin{align}
\begin{pmatrix}
4 \\
1 \\
1
\end{pmatrix} = coord_{\mathcal{A}}(T(1, 1, 1)) \implies T(1, 1, 1) &= 4 \cdot (1, 2, 0) + 1 \cdot (2, 1, 0) + 1 \cdot (1, 1, 1) \\
&= (4, 8, 0) + (2, 1, 0) + (1, 1, 1) \\
&= (7, 10, 1)
\end{align}
$$

$$
\begin{align}
\begin{pmatrix}
1 \\
1 \\
1
\end{pmatrix} = coord_{\mathcal{A}}(T(1, 0, 0)) \implies T(1, 0, 0) &= 1 \cdot (1, 2, 0) + 1 \cdot (2, 1, 0) + 1 \cdot (1, 1, 1) \\
&= (1, 2, 0) + (2, 1, 0) + (1, 1, 1) \\
&= (4, 4, 1)
\end{align}
$$

Entonces, determinamos las imágenes de cada elemento de la base $\mathcal{B}$:
$$
\begin{align}
&T(1, -1, 1) = (7, 6, 2) \\
&T(1, 1, 1) = (7, 10, 1) \\
&T(1, 0, 0) = (4, 4, 1)
\end{align}
$$

Ahora, determinaremos como se comporta con la base canónica $\{ (1, 0, 0), (0, 1, 0), (0, 0, 1) \}$:
$$
\begin{align}
(0, 1, 0) &= \frac{1}{2}((1, 1, 1) - (1, -1, 1)) \\
T(0, 1, 0) &= T \left( \frac{1}{2}((1, 1, 1) - (1, -1, 1)) \right) \\
&= \frac{1}{2}(T(1, 1, 1) - T(1, -1, 1)) \\
&= \frac{1}{2}((7, 10, 1) - (7, 6, 2)) \\
&= \frac{1}{2}(0, 4, -1) \\
&= \left( 0, 2, -\frac{1}{2} \right)
\end{align}
$$
$$
\begin{align}
(0, 0, 1) &= \frac{1}{2}((1, 1, 1) + (1, -1, 1) - 2(1, 0, 0)) \\
T(0, 0, 1) &= T \left( \frac{1}{2}((1, 1, 1) + (1, -1, 1) - 2(1, 0, 0)) \right) \\
&= \frac{1}{2}(T(1, 1, 1) + T(1, -1, 1) - 2T(1, 0, 0)) \\
&= \frac{1}{2}((7, 10, 1) + (7, 6, 2) - (8, 8, 2)) \\
&= \frac{1}{2}(6, 8, 1) \\
&= \left( 3, 4, \frac{1}{2} \right)
\end{align}
$$

Entonces:
$$
\begin{align}
&T(1, 0, 0) = (4, 4, 1) \\
&T(0, 1, 0) = \left( 0, 2, -\frac{1}{2} \right) \\
&T(0, 0, 1) = \left( 3, 4, \frac{1}{2} \right)
\end{align}
$$
Esto nos permite definir la expresión general $T(x, y, z)$:
$$
\begin{align}
T(x, y, z) &= x \cdot T(1, 0, 0) + y \cdot T(0, 1, 0) + z \cdot T(0, 0, 1) \\
&= x \cdot (4, 4, 1) + y \cdot \left( 0, 2, -\frac{1}{2} \right) + z \cdot \left( 3, 4, \frac{1}{2} \right) \\
&= (4x, 4x, x) + \left( 0, 2y, -\frac{1}{2}y \right) + \left( 3z, 4z, \frac{1}{2}z \right) \\
&= \left( 4x + 3z, 4x + 2y + 4z, x - \frac{1}{2}y + \frac{1}{2}z \right)
\end{align}
$$

En conclusión:
$$
T(x, y, z) = \left( -\frac{1}{2}y + \frac{3}{2}z, \frac{1}{2}y + \frac{3}{2}z, x \right)
$$

---
## Ejercicio 9
### Parte 1
Considerando que las columnas de la matriz asociada a $T$ se corresponden con las coordenadas en la base $\mathcal{B}$ de las imágenes de los elementos de la base $\mathcal{A}$:
$$
\begin{align}
\begin{pmatrix}
2 \\
1 \\
1
\end{pmatrix} = coord_{B}(T(1)) \implies T(1) &= 2 \cdot (1, 1, 0) + 1 \cdot (1, 2, 3) + 1 \cdot (3, 2, 1) \\
&= (2, 2, 0) + (1, 2, 3) + (3, 2, 1) \\
&= (6, 6, 4)
\end{align}
$$
$$
\begin{align}
\begin{pmatrix}
2 \\
3 \\
2
\end{pmatrix} = coord_{B}(T(x + 1)) \implies T(x + 1) &= 2 \cdot (1, 1, 0) + 3 \cdot (1, 2, 3) + 2 \cdot (3, 2, 1) \\
&= (2, 2, 0) + (3, 6, 9) + (6, 4, 2) \\
&= (11, 12, 11)
\end{align}
$$
$$
\begin{align}
\begin{pmatrix}
1 \\
1 \\
2
\end{pmatrix} = coord_{B}(T((x + 1)^{2})) \implies T((x + 1)^{2}) &= 1 \cdot (1, 1, 0) + 1 \cdot (1, 2, 3) + 2 \cdot (3, 2, 1) \\
&= (1, 1, 0) + (1, 2, 3) + (6, 4, 2) \\
&= (8, 7, 5)
\end{align}
$$

Entonces, conocemos las imágenes de los elementos de $\mathcal{A}$:
$$
\begin{align}
&T(1) = (6, 6, 4) \\
&T(x + 1) = (11, 12, 11) \\
&T((x + 1)^{2}) = T(x^{2} + 2x + 1) = (8, 7, 5)
\end{align}
$$

Ahora, determinamos $T(x^{2} + 2x - 1)$:
$$
\begin{align}
x^{2} + 2x - 1 &= (x^{2} + 2x + 1) - 2(1) \\
T(x^{2} + 2x - 1) &= T((x^{2} + 2x + 1) - 2(1)) \\
&= T(x^{2} + 2x + 1) - 2 \cdot T(1) \\
&= (8, 7, 5) - 2 \cdot (6, 6, 4) \\
&= (8, 7, 5) - (12, 12, 8) \\
&= (-4, -5, -3)
\end{align}
$$

En conclusión:
$$
T(x^{2} + 2x - 1) = (-4, -5, -3)
$$

### Parte 2
Ahora, pasaremos a hallar la expresión general $T(ax^{2} + bx + c)$, para lo que necesitaremos hallar $T(x)$ y $T(x^{2})$:
$$
\begin{align}
x &= (x + 1) - (1) \\
T(x) &= T(x + 1) - T(1) \\
&= (11, 12, 11) - (6, 6, 4) \\
&= (5, 6, 7)
\end{align}
$$
$$
\begin{align}
x^{2} &= (x^{2} + 2x + 1) - (x + 1) - (x) \\
T(x^{2}) &= T(x^{2} + 2x + 1) - T(x + 1) - T(x) \\
&= (8, 7, 5) - (11, 12, 11) - (5, 6, 7) \\
&= (-8, -11, -13)
\end{align}
$$

De esta forma:
$$
\begin{align}
T(1) = (6, 6, 4) \\
T(x) = (5, 6, 7) \\
T(x^{2}) = (-8, -11, -13)
\end{align}
$$

Ahora, podemos determinar la expresión general:
$$
\begin{align}
T(ax^{2} + bx + c) &= T(ax^{2}) + T(bx) + T(c) \\
&= a \cdot T(x^{2}) + b \cdot T(x) + c \cdot T(1) \\
&= a \cdot (-8, -11, -13) + b \cdot (5, 6, 7) + c \cdot (6, 6, 4) \\
&= (-8a, -11a, -13a) + (5b, 6b, 7b) + (6c, 6c, 4c) \\
&= (-8a + 5b + 6c, -11a + 6b + 6c, -13a + 7b + 4c)
\end{align}
$$

En conclusión:
$$
T(ax^{2} + bx + c) = (-8a + 5b + 6c, -11a + 6b + 6c, -13a + 7b + 4c)
$$

---
## Ejercicio 10
### Parte 1
Probamos que $T$ es lineal:
$$
\begin{align}
T(\alpha u + \beta v) &= i(\alpha u + \beta v) \\
&= \alpha iu + \beta iv \\
&= \alpha \cdot T(u) + \beta \cdot T(v)
\end{align}
$$

Probamos que $T$ preserva el módulo:
$$
\begin{align}
|z| &= |a + bi| \\
&= \sqrt{ a^{2} + b^{2} } \\
|T(z)| &= |T(a + bi)| \\
&= |ai - b| \\
&= \sqrt{ a^{2} + b^{2} }
\end{align} \implies |T(z)| = |z|
$$

### Parte 2
Para esto, tenemos que:
1. Aplicar la transformación lineal a cada uno de los elementos de $\mathcal{A}$.
$$
\begin{align}
&T(1) = i \\
&T(i) = i^{2} = -1
\end{align}
$$
2. Hallar las coordenadas de cada imagen.
$$
\begin{align}
&T(1) = i = 0 \cdot 1 + 1 \cdot i \implies coord_{\mathcal{A}}(T(1)) = (0, 1) \\
&T(i) = -1 = -1 \cdot 1 + 0 \cdot i \implies coord_{\mathcal{A}}(T(i)) = (-1, 0)
\end{align}
$$
3. Expresar la matriz asociada.
$$
_{\mathcal{A}}(T)_{\mathcal{A}} = \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix}
$$

### Parte 3
$$
\begin{align}
coord_{A}(T(v)) &= \space _{\mathcal{A}}(T)_{\mathcal{A}} \cdot coord_{A}(v) \\
\begin{pmatrix}
x_{2} \\
y_{2}
\end{pmatrix} &= \begin{pmatrix}
0 & -1 \\
1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x_{1} \\
y_{1}
\end{pmatrix} \\
&= \begin{pmatrix}
-y_{1} \\
x_{1}
\end{pmatrix}
\end{align}
$$
Podríamos decir que, en el plano $\mathbb{R}^{2}$, la transformación toma un elemento, intercambia sus coordenadas $x$ e $y$, y luego cambia el signo de su nueva coordenada $x$.

---
## Ejercicio 11
### Transformación 1

$$
\begin{align}
&T(1, 1, -1) = (2, 1, 0) \\
&T(1, 2, 1) = (-1, 2, 3) \\
&T(1, 0, 3) = (0, 0, 1)
\end{align}
$$

#### Parte a
$$
(1, 0, 0) = \alpha \cdot (1, 1, -1) + \beta \cdot (1, 2, 1) + \gamma (1, 0, 3)
$$
$$
\begin{cases}
\alpha + \beta + \gamma = 1 \\
\alpha + 2\beta = 0 \\
-\alpha + \beta + 3 \gamma = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
1 & 2 & 0 & 0 \\
-1 & 1 & 3 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
0 & -1 & 1 & 1 \\
1 & 2 & 0 & 0 \\
0 & 3 & 3 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2} \\
&F_{3} \leftarrow F_{3} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & -1 & 1 & 1 \\
1 & 2 & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{3}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 2 & 1 \\
1 & 2 & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1}{2} \\
1 & 2 & 0 & 0 \\
0 & 1 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{2}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1}{2} \\
1 & 2 & 0 & 0 \\
0 & 1 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1}{2} \\
1 & 0 & 0 & 1 \\
0 & 1 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{3}
\end{align}
$$
$$
\begin{align}
\implies (1, 0, 0) &= 1 \cdot (1, 1, -1) - \frac{1}{2} \cdot (1, 2, 1) + \frac{1}{2} (1, 0, 3) \\
T(1, 0, 0) &= 1 \cdot T(1, 1, -1) - \frac{1}{2} \cdot T(1, 2, 1) + \frac{1}{2} T(1, 0, 3) \\
&= 1 \cdot (2, 1, 0) - \frac{1}{2} \cdot (-1, 2, 3) + \frac{1}{2} (0, 0, 1) \\
&= (2, 1, 0) - \left( -\frac{1}{2}, 1, \frac{3}{2} \right) + \left( 0, 0, \frac{1}{2} \right) \\
&= \left( \frac{5}{2}, 0, -1 \right)
\end{align}
$$

$$
(0, 1, 0) = \alpha \cdot (1, 1, -1) + \beta \cdot (1, 2, 1) + \gamma (1, 0, 3)
$$
$$
\begin{cases}
\alpha + \beta + \gamma = 0 \\
\alpha + 2\beta = 1 \\
-\alpha + \beta + 3 \gamma = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
1 & 2 & 0 & 1 \\
-1 & 1 & 3 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
0 & -1 & 1 & -1 \\
1 & 2 & 0 & 1 \\
0 & 3 & 3 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2} \\
&F_{3} \leftarrow F_{3} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & -1 & 1 & -1 \\
1 & 2 & 0 & 1 \\
0 & 1 & 1 & \frac{1}{3}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{3}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 2 & -\frac{2}{3} \\
1 & 2 & 0 & 1 \\
0 & 1 & 1 & \frac{1}{3}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & -\frac{1}{3} \\
1 & 2 & 0 & 1 \\
0 & 1 & 1 & \frac{1}{3}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{2}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & -\frac{1}{3} \\
1 & 2 & 0 & 1 \\
0 & 1 & 0 & \frac{2}{3}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & -\frac{1}{3} \\
1 & 0 & 0 & -\frac{1}{3} \\
0 & 1 & 0 & \frac{2}{3}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{3}
\end{align}
$$
$$
\begin{align}
\implies (0, 1, 0) &= -\frac{1}{3} \cdot (1, 1, -1) + \frac{2}{3} \cdot (1, 2, 1) - \frac{1}{3} (1, 0, 3) \\
T(0, 1, 0) &= -\frac{1}{3} \cdot T(1, 1, -1) + \frac{2}{3} \cdot T(1, 2, 1) - \frac{1}{3} T(1, 0, 3) \\
&= -\frac{1}{3} \cdot (2, 1, 0) + \frac{2}{3} \cdot (-1, 2, 3) - \frac{1}{3} (0, 0, 1) \\
&= -\left( \frac{2}{3}, \frac{1}{3}, 0 \right) + \left( -\frac{2}{3}, \frac{4}{3}, 2 \right) - \left( 0, 0, \frac{1}{3} \right) \\
&= \left( -\frac{4}{3}, 1, \frac{5}{3} \right)
\end{align}
$$

$$
(0, 0, 1) = \alpha \cdot (1, 1, -1) + \beta \cdot (1, 2, 1) + \gamma (1, 0, 3)
$$
$$
\begin{cases}
\alpha + \beta + \gamma = 0 \\
\alpha + 2\beta = 0 \\
-\alpha + \beta + 3 \gamma = 1
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
1 & 2 & 0 & 0 \\
-1 & 1 & 3 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
0 & -1 & 1 & 0 \\
1 & 2 & 0 & 0 \\
0 & 3 & 3 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2} \\
&F_{3} \leftarrow F_{3} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & -1 & 1 & 0 \\
1 & 2 & 0 & 0 \\
0 & 1 & 1 & \frac{1}{3}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{3}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 2 & \frac{1}{3} \\
1 & 2 & 0 & 0 \\
0 & 1 & 1 & \frac{1}{3}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1}{6} \\
1 & 2 & 0 & 0 \\
0 & 1 & 1 & \frac{1}{3}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{2}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1}{6} \\
1 & 2 & 0 & 0 \\
0 & 1 & 0 & \frac{1}{6}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1}{6} \\
1 & 0 & 0 & -\frac{1}{3} \\
0 & 1 & 0 & \frac{1}{6}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{3}
\end{align}
$$
$$
\begin{align}
\implies (0, 0, 1) &= -\frac{1}{3} \cdot (1, 1, -1) + \frac{1}{6} \cdot (1, 2, 1) + \frac{1}{6} (1, 0, 3) \\
T(0, 0, 1) &= -\frac{1}{3} \cdot T(1, 1, -1) + \frac{1}{6} \cdot T(1, 2, 1) + \frac{1}{6} T(1, 0, 3) \\
&= -\frac{1}{3} \cdot (2, 1, 0) + \frac{1}{6} \cdot (-1, 2, 3) + \frac{1}{6} (0, 0, 1) \\
&= -\left( \frac{2}{3}, \frac{1}{3}, 0 \right) + \left( -\frac{1}{6}, \frac{1}{3}, \frac{1}{2} \right) + \left( 0, 0, \frac{1}{6} \right) \\
&= \left( -\frac{5}{6}, 0, \frac{2}{3} \right)
\end{align}
$$

De esta manera:
$$
\begin{align}
&T(1, 0, 0) = \left( \frac{5}{2}, 0, -1 \right) \\
&T(0, 1, 0) = \left( -3, 1, \frac{11}{3} \right) \\
&T(0, 0, 1) = \left( -\frac{5}{6}, 0, \frac{7}{6} \right)
\end{align}
$$

Ahora, podemos definir la forma general:
$$
\begin{align}
(x, y, z) &= (x, 0, 0) + (0, y, 0) + (0, 0, z) \\
&= x \cdot (1, 0, 0) + y \cdot (0, 1, 0) + z \cdot (0, 0, 1) \\
T(x, y, z) &= x \cdot T(1, 0, 0) + y \cdot T(0, 1, 0) + z \cdot T(0, 0, 1) \\
&= x \cdot \left( \frac{5}{2}, 0, -1 \right) + y \cdot \left( -\frac{4}{3}, 1, \frac{5}{3} \right) + z \cdot \left( -\frac{5}{6}, 0, \frac{2}{3} \right) \\
&= \left( \frac{5}{2}x, 0, -x \right) + \left( -\frac{4}{3}y, y, \frac{5}{3}y \right) + \left( -\frac{5}{6}z, 0, \frac{2}{3}z \right) \\
&= \left( \frac{5}{2}x - \frac{4}{3}y - \frac{5}{6}z, y, -x + \frac{5}{3}y + \frac{2}{3}z \right)
\end{align}
$$

En conclusión:
$$
T(x, y, z) = \left( \frac{5}{2}x - \frac{4}{3}y - \frac{5}{6}z, y, -x + \frac{5}{3}y + \frac{2}{3}z \right)
$$

#### Parte b
Tenemos que hallar las coordenadas en la base $\mathcal{B}$ de las imágenes de los elementos de $\mathcal{A}$:
$$
\begin{align}
T(1, 2, 0) &= \left( \frac{5}{2} - \frac{8}{3}, 2, -1 + \frac{10}{3} \right) \\
&= \left( -\frac{1}{6}, 2, \frac{7}{3} \right) \\
T(1, 2, 2) &= \left( \frac{5}{2} - \frac{8}{3} - \frac{5}{3}, 2, -1 + \frac{10}{3} + \frac{4}{3} \right) \\
&= \left( -\frac{11}{6}, 2, \frac{11}{3} \right) \\
T(1, 1, 0) &= \left( \frac{5}{2} - \frac{4}{3}, 1, -1 + \frac{5}{3} \right) \\
&= \left( \frac{7}{6}, 1, \frac{2}{3} \right)
\end{align}
$$

$$
\left( -\frac{1}{6}, 2, \frac{7}{3} \right) = \alpha \cdot (-1, 0, -3) + \beta \cdot (5, 0, 3) + \gamma \cdot (0, 1, 0) \implies coord_{\mathcal{B}}\left( -\frac{1}{6}, 2, \frac{7}{3} \right) = (\alpha, \beta, \gamma)
$$
$$
\begin{align}
&\begin{cases}
-\alpha + 5\beta = -\frac{1}{6} \\
\gamma = 2 \\
-3\alpha + 3\beta = \frac{7}{3}
\end{cases} \\ \\

&-3\alpha + 3\beta = \frac{7}{3} \implies -\alpha + \beta = \frac{7}{9} \implies \beta = \frac{7}{9} + \alpha \\

&\implies -\alpha + 5 \left( \frac{7}{9} + \alpha \right) = -\frac{1}{6} \implies \begin{aligned}
&-\alpha + 5 \left( \frac{7}{9} + \alpha \right) = -\frac{1}{6} \\
&-\alpha + \frac{35}{9} + 5\alpha = -\frac{1}{6} \\
&\frac{35}{9} + 4\alpha = -\frac{1}{6} \\
&4\alpha = -\frac{73}{18} \\
&\alpha = -\frac{73}{72}
\end{aligned} \\

&\implies \frac{73}{72} + 5\beta = -\frac{1}{6} \implies \begin{aligned}
&5\beta = -\frac{1}{6} - \frac{73}{72} \\
&5\beta = -\frac{85}{72} \\
&\beta = -\frac{17}{72}
\end{aligned}
\end{align}
$$
$$
\implies coord_{\mathcal{B}} \left( -\frac{1}{6}, 2, \frac{7}{3} \right) = \left( -\frac{73}{72}, -\frac{17}{72}, 2 \right)
$$

$$
\left( -\frac{11}{6}, 2, \frac{11}{3} \right) = \alpha \cdot (-1, 0, -3) + \beta \cdot (5, 0, 3) + \gamma \cdot (0, 1, 0) \implies coord_{\mathcal{B}} \left( -\frac{11}{6}, 2, \frac{11}{3} \right) = (\alpha, \beta, \gamma)
$$
$$
\begin{align}
&\begin{cases}
-\alpha + 5\beta = -\frac{11}{6} \\
\gamma = 2 \\
-3\alpha + 3\beta = \frac{11}{3}
\end{cases} \\ \\

&-3\alpha + 3\beta = \frac{11}{3} \implies -\alpha + \beta = \frac{11}{9} \implies \beta = \frac{11}{9} + \alpha \\

&\implies -\alpha + 5 \left( \frac{11}{9} + \alpha \right) = -\frac{11}{6} \implies \begin{aligned}
&-\alpha + 5 \left( \frac{11}{9} + \alpha \right) = -\frac{11}{6} \\
&-\alpha + \frac{55}{9} + 5\alpha = -\frac{11}{6} \\
&\frac{55}{9} + 4\alpha = -\frac{11}{6} \\
&4\alpha = -\frac{143}{18} \\
&\alpha = -\frac{143}{72}
\end{aligned} \\

&\implies \frac{143}{72} + 5\beta = -\frac{11}{6} \implies \begin{aligned}
&5\beta = -\frac{11}{6} - \frac{143}{72} \\
&5\beta = -\frac{275}{72} \\
&\beta = -\frac{55}{72}
\end{aligned}
\end{align}
$$
$$
\implies coord_{\mathcal{B}} \left( -\frac{11}{6}, 2, \frac{11}{3} \right) = \left( -\frac{143}{72}, -\frac{55}{72}, 2 \right)
$$

$$
\left( \frac{7}{6}, 1, \frac{2}{3} \right) = \alpha \cdot (-1, 0, -3) + \beta \cdot (5, 0, 3) + \gamma \cdot (0, 1, 0) \implies coord_{\mathcal{B}} \left( \frac{7}{6}, 1, \frac{2}{3} \right) = (\alpha, \beta, \gamma)
$$
$$
\begin{align}
&\begin{cases}
-\alpha + 5\beta = \frac{7}{6} \\
\gamma = 1 \\
-3\alpha + 3\beta = \frac{2}{3}
\end{cases} \\ \\

&-3\alpha + 3\beta = \frac{2}{3} \implies -\alpha + \beta = \frac{2}{9} \implies \beta = \frac{2}{9} + \alpha \\

&\implies -\alpha + 5 \left( \frac{2}{9} + \alpha \right) = \frac{7}{6} \implies \begin{aligned}
&-\alpha + 5 \left( \frac{2}{9} + \alpha \right) = \frac{7}{6} \\
&-\alpha + \frac{10}{9} + 5\alpha = \frac{7}{6} \\
&\frac{10}{9} + 4\alpha = \frac{7}{6} \\
&4\alpha = \frac{1}{18} \\
&\alpha = \frac{1}{72}
\end{aligned} \\

&\implies -\frac{1}{72} + 5\beta = \frac{7}{6} \implies \begin{aligned}
&5\beta = \frac{7}{6} + \frac{1}{72} \\
&5\beta = \frac{85}{72} \\
&\beta = \frac{17}{72}
\end{aligned}
\end{align}
$$
$$
\implies coord_{\mathcal{B}} \left( -\frac{11}{6}, 2, \frac{11}{3} \right) = \left( \frac{1}{72}, \frac{17}{72}, 1 \right)
$$

Finalmente, definimos la matriz asociada a la transformación de las bases $\mathcal{A}$ y $\mathcal{B}$:
$$
_{\mathcal{B}}(T)_{\mathcal{A}} = \begin{pmatrix}
-\frac{73}{72} & -\frac{143}{72} & \frac{1}{72} \\
-\frac{17}{72} & -\frac{55}{72} & \frac{17}{72} \\
2 & 2 & 1
\end{pmatrix}
$$

### Transformación 2
#### Parte a
$$
\begin{align}
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} = \alpha \cdot \begin{pmatrix}
-1 & 1 \\
1 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
1 & 0 \\
-1 & 2
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & -2 \\
1 & -1
\end{pmatrix} + \mu \cdot \begin{pmatrix}
1 & 0 \\
1 & 3
\end{pmatrix}
\end{align}
$$
$$
\begin{cases}
-\alpha + \beta - \gamma + \mu = a \\
\alpha - 2\gamma = b \\
\alpha - \beta + \gamma + \mu = c \\
\alpha + 2\beta - \gamma + 3\mu = d
\end{cases}
$$
$$
\left(
\begin{array}{cccc|c}
-1 & 1 & -1 & 1 & a \\
1 & 0 & -2 & 0 & b \\
1 & -1 & 1 & 1 & c \\
1 & 2 & -1 & 3 & d
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
0 & 1 & -3 & 1 & a + b \\
1 & 0 & -2 & 0 & b \\
0 & -1 & 3 & 1 & c - b \\
0 & 2 & 1 & 3 & d - b
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2} \\
&F_{3} \leftarrow F_{3} - F_{2} \\
&F_{4} \leftarrow F_{4} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 0 & 0 & 2 & a + c \\
1 & 0 & -2 & 0 & b \\
0 & -1 & 3 & 1 & c - b \\
0 & 2 & 1 & 3 & d - b
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 0 & 0 & 1 & \frac{1}{2}a + \frac{1}{2}c \\
1 & 0 & -2 & 0 & b \\
0 & -1 & 3 & 1 & c - b \\
0 & 2 & 1 & 3 & d - b
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{2}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 0 & 0 & 1 & \frac{1}{2}a + \frac{1}{2}c \\
1 & 0 & -2 & 0 & b \\
0 & -1 & 3 & 0 & \frac{1}{2}c - b - \frac{1}{2}a \\
0 & 2 & 1 & 0 & d - b - \frac{3}{2}a - \frac{3}{2}c
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1} \\
&F_{4} \leftarrow F_{3} - 3F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 0 & 0 & 1 & \frac{1}{2}a + \frac{1}{2}c \\
1 & 0 & -2 & 0 & b \\
0 & -1 & 3 & 0 & \frac{1}{2}c - b - \frac{1}{2}a \\
0 & 0 & 7 & 0 & d - 3b - \frac{5}{2}a - \frac{1}{2}c
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} + 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 0 & 0 & 1 & \frac{1}{2}a + \frac{1}{2}c \\
1 & 0 & -2 & 0 & b \\
0 & -1 & 3 & 0 & \frac{1}{2}c - b - \frac{1}{2}a \\
0 & 0 & 1 & 0 & \frac{1}{7}d - \frac{3}{7}b - \frac{5}{14}a - \frac{1}{14}c
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow \frac{1}{7}F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 0 & 0 & 1 & \frac{1}{2}a + \frac{1}{2}c \\
1 & 0 & 0 & 0 & \frac{1}{7}b + \frac{2}{7}d - \frac{5}{7}a - \frac{1}{7}c \\
0 & -1 & 0 & 0 & \frac{5}{7}c + \frac{2}{7}b + \frac{4}{7}a - \frac{3}{7}d \\
0 & 0 & 1 & 0 & \frac{1}{7}d - \frac{3}{7}b - \frac{5}{14}a - \frac{1}{14}c
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + 2F_{4} \\
&F_{3} \leftarrow F_{3} - 3F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 0 & 0 & 1 & \frac{1}{2}a + \frac{1}{2}c \\
1 & 0 & 0 & 0 & \frac{1}{7}b + \frac{2}{7}d - \frac{5}{7}a - \frac{1}{7}c \\
0 & 1 & 0 & 0 & -\frac{5}{7}c - \frac{2}{7}b - \frac{4}{7}a + \frac{3}{7}d \\
0 & 0 & 1 & 0 & \frac{1}{7}d - \frac{3}{7}b - \frac{5}{14}a - \frac{1}{14}c
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow -F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 0 & 0 & 1 & \frac{1}{2}a + \frac{1}{2}c \\
1 & 0 & 0 & 0 & -\frac{5}{7}a + \frac{1}{7}b - \frac{1}{7}c + \frac{2}{7}d \\
0 & 1 & 0 & 0 & -\frac{4}{7}a - \frac{2}{7}b - \frac{5}{7}c + \frac{3}{7}d \\
0 & 0 & 1 & 0 & -\frac{5}{14}a - \frac{3}{7}b - \frac{1}{14}c + \frac{1}{7}d
\end{array}
\right)
$$

Ahora, determinamos la expresión general de $T$:
$$
\begin{align}
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} &= \alpha \cdot \begin{pmatrix}
-1 & 1 \\
1 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
1 & 0 \\
-1 & 2
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & -2 \\
1 & -1
\end{pmatrix} + \mu \cdot \begin{pmatrix}
1 & 0 \\
1 & 3
\end{pmatrix} \\
\implies T\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} &= \alpha \cdot T\begin{pmatrix}
-1 & 1 \\
1 & 1
\end{pmatrix} + \beta \cdot T\begin{pmatrix}
1 & 0 \\
-1 & 2
\end{pmatrix} + \gamma \cdot T\begin{pmatrix}
-1 & -2 \\
1 & -1
\end{pmatrix} + \mu \cdot T\begin{pmatrix}
1 & 0 \\
1 & 3
\end{pmatrix}
\end{align}
$$
$$
\alpha \cdot T\begin{pmatrix}
-1 & 1 \\
1 & 1
\end{pmatrix} = \left( -\frac{5}{7}a + \frac{1}{7}b - \frac{1}{7}c + \frac{2}{7}d \right) \cdot (1, -1) = \left( -\frac{5}{7}a + \frac{1}{7}b - \frac{1}{7}c + \frac{2}{7}d, \frac{5}{7}a - \frac{1}{7}b + \frac{1}{7}c - \frac{2}{7}d \right)
$$
$$
\beta \cdot T\begin{pmatrix}
1 & 0 \\
-1 & 2
\end{pmatrix} = \left( -\frac{4}{7}a - \frac{2}{7}b - \frac{5}{7}c + \frac{3}{7}d \right) \cdot (1, 1) = \left( -\frac{4}{7}a - \frac{2}{7}b - \frac{5}{7}c + \frac{3}{7}d, -\frac{4}{7}a - \frac{2}{7}b - \frac{5}{7}c + \frac{3}{7}d \right)
$$
$$
\gamma \cdot T\begin{pmatrix}
-1 & -2 \\
1 & -1
\end{pmatrix} = \left( -\frac{5}{14}a - \frac{3}{7}b - \frac{1}{14}c + \frac{1}{7}d \right) \cdot (1, 1) = \left( -\frac{5}{14}a - \frac{3}{7}b - \frac{1}{14}c + \frac{1}{7}d, -\frac{5}{14}a - \frac{3}{7}b - \frac{1}{14}c + \frac{1}{7}d \right)
$$
$$
\mu \cdot T\begin{pmatrix}
1 & 0 \\
1 & 3
\end{pmatrix} = \left( \frac{1}{2}a + \frac{1}{2}c \right) \cdot (1, -3) = \left( \frac{1}{2}a + \frac{1}{2}c, -\frac{3}{2}a - \frac{3}{2}c \right)
$$

$$
\begin{align}
\implies T\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} &= \left( -\frac{5}{7}a + \frac{1}{7}b - \frac{1}{7}c + \frac{2}{7}d, \frac{5}{7}a - \frac{1}{7}b + \frac{1}{7}c - \frac{2}{7}d \right) + \left( -\frac{4}{7}a - \frac{2}{7}b - \frac{5}{7}c + \frac{3}{7}d, -\frac{4}{7}a - \frac{2}{7}b - \frac{5}{7}c + \frac{3}{7}d \right) + \left( -\frac{5}{14}a - \frac{3}{7}b - \frac{1}{14}c + \frac{1}{7}d, -\frac{5}{14}a - \frac{3}{7}b - \frac{1}{14}c + \frac{1}{7}d \right) + \left( \frac{1}{2}a + \frac{1}{2}c, -\frac{3}{2}a - \frac{3}{2}c \right) \\
&= \left( \left( -\frac{5}{7} - \frac{4}{7} - \frac{5}{14} + \frac{1}{2} \right)a + \left( \frac{1}{7} - \frac{2}{7} - \frac{3}{7} \right)b + \left( -\frac{1}{7} - \frac{5}{7} - \frac{1}{14} + \frac{1}{2} \right)c + \left( \frac{2}{7} + \frac{3}{7} + \frac{1}{7} \right)d, \left( \frac{5}{7} - \frac{4}{7} - \frac{5}{14} - \frac{3}{2} \right)a + \left( -\frac{1}{7} - \frac{2}{7} - \frac{3}{7} \right)b + \left( \frac{1}{7} - \frac{5}{7} - \frac{1}{14} - \frac{3}{2} \right)c + \left( -\frac{2}{7} + \frac{3}{7}d + \frac{1}{7} \right)d \right) \\
&= \left( -\frac{16}{14}a - \frac{4}{7}b - \frac{6}{14}c + \frac{6}{7}d, -\frac{12}{7}a - \frac{6}{7}b - \frac{15}{7}c + \frac{2}{7}d \right)
\end{align}
$$

En conclusión:
$$
T\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} = \left( -\frac{8}{7}a - \frac{4}{7}b - \frac{3}{7}c + \frac{6}{7}d, -\frac{12}{7}a - \frac{6}{7}b - \frac{15}{7}c + \frac{2}{7}d \right) = \left( \frac{-8a - 4b - 3c + 6d}{7}, \frac{-12a - 6b - 15c + 2d}{7} \right)
$$

#### Parte b
Determinamos las imágenes de los elementos de la base $\mathcal{A}$:
$$
\begin{align}
&T\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} = \left( \frac{-8 + 6}{7}, \frac{-12 + 2}{7} \right) = \left( -\frac{2}{7}, -\frac{10}{7} \right) \\
&T\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} = \left( \frac{-4 - 3}{7}, \frac{-6 - 15}{7} \right) = \left( -1, -3 \right) \\
&T\begin{pmatrix}
-1 & 0 \\
0 & 1
\end{pmatrix} = \left( \frac{8 + 6}{7}, \frac{12 + 2}{7} \right) = \left( 2, 2 \right) \\
&T\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix} = \left( \frac{-4 + 3}{7}, \frac{-6 + 15}{7} \right) = \left( -\frac{1}{7}, \frac{9}{7} \right)
\end{align}
$$

Hallamos las coordenadas de dichas imágenes en la base $\mathcal{B}$:
$$
coord_{\mathcal{B}} \left( T\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \right) = coord_{\mathcal{B}} \left( -\frac{2}{7}, -\frac{10}{7} \right) = (\alpha, \beta) \text{ tal que } \left( -\frac{2}{7}, -\frac{10}{7} \right) = \alpha \cdot (1, 1) + \beta \cdot (-1, 1)
$$
$$
\begin{cases}
\alpha - \beta = -\frac{2}{7} \\
\alpha + \beta = -\frac{10}{7}
\end{cases} \implies 2 \alpha = -\frac{12}{7} \implies \alpha = -\frac{6}{7} \implies \beta = -\frac{10}{7} + \frac{6}{7} = -\frac{4}{7}
$$
$$
\implies coord_{\mathcal{B}} \left( -\frac{2}{7}, -\frac{10}{7} \right) = \left( -\frac{6}{7}, -\frac{4}{7} \right)
$$

$$
coord_{\mathcal{B}} \left( T\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} \right) = coord_{\mathcal{B}} \left( -1, -3 \right) = (\alpha, \beta) \text{ tal que } \left( -1, -3 \right) = \alpha \cdot (1, 1) + \beta \cdot (-1, 1)
$$
$$
\implies coord_{\mathcal{B}} \left( -1, -3 \right) = \left( -2, -1 \right)
$$

$$
coord_{\mathcal{B}} \left( T\begin{pmatrix}
-1 & 0 \\
0 & 1
\end{pmatrix} \right) = coord_{\mathcal{B}} \left( 2, 2 \right) = (\alpha, \beta) \text{ tal que } \left( 2, 2 \right) = \alpha \cdot (1, 1) + \beta \cdot (-1, 1)
$$
$$
\implies coord_{\mathcal{B}} \left( 2, 2 \right) = \left( 2, 0 \right)
$$

$$
coord_{\mathcal{B}} \left( T\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix} \right) = coord_{\mathcal{B}} \left( -\frac{1}{7}, \frac{9}{7} \right) = (\alpha, \beta) \text{ tal que } \left( -\frac{1}{7}, \frac{9}{7} \right) = \alpha \cdot (1, 1) + \beta \cdot (-1, 1)
$$
$$
\begin{cases}
\alpha - \beta = -\frac{1}{7} \\
\alpha + \beta = \frac{9}{7}
\end{cases} \implies 2 \alpha = \frac{8}{7} \implies \alpha = \frac{4}{7} \implies \beta = \frac{9}{7} - \frac{4}{7} = \frac{5}{7}
$$
$$
\implies coord_{\mathcal{B}} \left( -\frac{1}{7}, \frac{9}{7} \right) = \left( \frac{4}{7}, \frac{5}{7} \right)
$$

Para finalizar, expresamos la matriz asociada a la transformación lineal de las bases $\mathcal{A}$ y $\mathcal{B}$:
$$
_{\mathcal{B}}(T)_{\mathcal{A}} = \begin{pmatrix}
-\frac{6}{7} & -2 & 2 & \frac{4}{7} \\
-\frac{4}{7} & -1 & 0 & \frac{5}{7}
\end{pmatrix}
$$

---
## Ejercicio 12
### Parte 1
$$
\begin{align}
T(\alpha \cdot a + \beta \cdot b, \alpha \cdot c + \beta \cdot d) &= (\alpha \cdot a + \beta \cdot b + \alpha \cdot c + \beta \cdot d, \alpha \cdot a + \beta \cdot b - \alpha \cdot c - \beta \cdot d) \\
&= (\alpha \cdot a + \alpha \cdot c, \alpha \cdot a - \alpha \cdot c) + (\beta \cdot b + \beta \cdot d, \beta \cdot b - \beta \cdot d) \\
&= \alpha \cdot (a + c, a - c) + \beta \cdot (b + d, b - d) \\
&= \alpha \cdot T(a, c) + \beta \cdot T(b, d)
\end{align}
$$
$$
\begin{align}
|(z, w)| &= |T(z, w)|? \\
&= |(z + w, z - w)| \\
\sqrt{ |z|^{2} + |w|^{2} } &= \sqrt{ |z + w|^{2} + |z - w|^{2} } \\
\sqrt{ z_{1}^{2} + z_{2}^{2} + w_{1}^{2} + w_{2}^{2} } &= \sqrt{ (z_{1} + w_{1})^{2} + (z_{2} + w_{2})^{2} + (z_{1} - w_{1})^{2} + (z_{2} - w_{2})^{2} } \\
&= \sqrt{ z_{1}^{2} + \cancel{ 2z_{1}w_{1} } + w_{1}^{2} + z_{2}^{2} - \cancel{ 2z_{2}w_{2} } + w_{2}^{2} + z_{1}^{2} - \cancel{ 2z_{1}w_{1} } + w_{1}^{2} + z_{2}^{2} - \cancel{ 2z_{2}w_{2} } + w_{2}^{2} } \\
&= \sqrt{ 2z_{1}^{2} + 2w_{1}^{2} + 2z_{2}^{2} + 2w_{2}^{2} } \\
&= \sqrt{ 2(z_{1}^{2} + w_{1}^{2} + z_{2}^{2} + w_{2}^{2}) } \\
&= \sqrt{ 2 }\sqrt{ z_{1}^{2} + w_{1}^{2} + z_{2}^{2} + w_{2}^{2} }
\end{align}
$$

Como vemos, el módulo no se preserva luego de aplicar $T$.

### Parte 2
1. Determinamos las imágenes de los elementos de $\mathcal{A}$:
$$
\begin{align}
&T(1, 0) = (1, 1) \\
&T(i, 0) = (i, i) \\
&T(0, 1) = (1, -1) \\
&T(0, i) = (i, -i)
\end{align}
$$

2. Expresar las imágenes como coordenadas en $\mathcal{A}$:
~~Sabemos que, como trabajamos con una base canónica, no es necesario traducir las coordenadas a la base $\mathcal{A}$, ya que ya se encuentran expresadas en dicha base.~~

Actualmente, las imágenes se encuentran expresadas en la base canónica de $\mathbb{C}^{2}$ como un $\mathbb{C}$-espacio vectorial: $\{ (1, 0), (0, 1) \}$

Tenemos que expresar cada imagen considerando la base provista:
$$
\begin{align}
&(1, 1) = 1 \cdot (1, 0) + 0 \cdot (i, 0) + 1 \cdot (0, 1) + 0 \cdot (0, i) \implies coord_{\mathcal{A}}(1, 1) = (1, 0, 1, 0) \\
&(i, i) = 0 \cdot (1, 0) + 1 \cdot (i, 0) + 0 \cdot (0, 1) + 1 \cdot (0, i) \implies coord_{\mathcal{A}}(1, 1) = (0, 1, 0, 1) \\
&(1, -1) = 1 \cdot (1, 0) + 0 \cdot (i, 0) - 1 \cdot (0, 1) + 0 \cdot (0, i) \implies coord_{\mathcal{A}}(1, 1) = (1, 0, -1, 0) \\
&(i, i) = 0 \cdot (1, 0) + 1 \cdot (i, 0) + 0 \cdot (0, 1) - 1 \cdot (0, i) \implies coord_{\mathcal{A}}(1, 1) = (0, 1, 0, -1)
\end{align}
$$

3. Expresar la matriz:
$$
_{\mathcal{A}}(T)_{\mathcal{A}} = \begin{pmatrix}
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
1 & 0 & -1 & 0 \\
0 & 1 & 0 & -1
\end{pmatrix}
$$

### Parte 3
Recordemos que:
$$
\begin{align}
&Ker(T) = \{ v \in \mathbb{C}^{2} : T(v) = \vec{0} \} \\
&\mathrm{Im}(T) = \{ w \in \mathbb{C}^{2} : w = T(v), v \in \mathbb{C}^{2} \}
\end{align}
$$
1. Determinamos $Ker(T)$:
$$
(z, w) \in Ker(T) \Longleftrightarrow T(z, w) = \vec{0} \implies (z + w, z - w) = (0, 0)
$$
$$
\begin{cases}
z + w = 0 \implies z = -w \\
z - w = 0 \implies z = w
\end{cases} \implies z = 0 \implies w = 0
$$
De esta forma:
$$
Ker(T) = \{ \vec{0} \} \implies dim(Ker(T)) = 0
$$

2. Determinamos $\mathrm{Im}(T)$:
Por el teorema de las dimensiones:
$$
dim(\mathbb{C}^{2}) = 2 = dim(Ker(T)) + dim(\mathrm{Im}(T)) = 0 + dim(\mathrm{Im}(T)) \implies dim(\mathrm{Im}(T)) = 2
$$
Entonces, considerando que $\mathrm{Im}(T) \subset \mathbb{C}^{2}$ y $dim(\mathrm{Im}(T)) = 2 = dim(\mathbb{C}^{2})$, podemos afirmar que $\mathrm{Im}(T) = \mathbb{C}^{2}$.

### Parte 4
Probamos que $\mathcal{B}$ es base de $\mathbb{C}^{2}$, verificando que es LI (ya que tiene 4 elementos):
$$
(0 + 0i, 0 + 0i) = \alpha \cdot (1, i) + \beta \cdot (1, -i) + \gamma \cdot (1 + i, 1) + \delta \cdot (1 - i, -2i)
$$
Es importante verificar que tanto la parte real como la imaginaria son 0, para cada componente del vector en $\mathbb{C}^{2}$: 
$$
\begin{cases}
\alpha + \beta + (1 + i) \gamma + (1 - i) \delta = 0 + 0i \\
i \alpha - i \beta + \gamma - 2i \delta = 0 + 0i
\end{cases} \implies \text{considerando por separado parte } \mathbb{R} \text{ y } \mathbb{C} \begin{cases}
\alpha + \beta + \gamma + \delta = 0 \\
\gamma - \delta = 0 \\
\gamma = 0 \\
\alpha - \beta - 2\delta = 0
\end{cases}
$$
$$
\gamma = 0 \implies \delta = 0 \implies \alpha - \beta = 0 \implies \alpha = \beta \implies 2\beta = 0 \implies \alpha = 0
$$
De esta forma, probamos que $\mathcal{B}$ es base de $\mathbb{C}^{2}$ estudiado como $\mathbb{R}$-espacio vectorial.

Pasamos a determinar $_{\mathcal{B}}(T)_{\mathcal{B}}$:
$$
\begin{align}
&T(1, i) = (1 + i, 1 - i) \\
&T(1, -i) = (1 - i, 1 + i) \\
&T(1 + i, 1) = (1 + i + 1, 1 + i - 1) = (2 + i, i) \\
&T(1 - i, -2i) = (1 - i - 2i, 1 - i + 2i) = (1 - 3i, 1 + i)
\end{align}
$$
Ahora, expresamos las coordenadas de las imágenes en la base $\mathcal{B}$:
$$
(1 + i, 1 - i) = \alpha \cdot (1, i) + \beta \cdot (1, -i) + \gamma \cdot (1 + i, 1) + \delta \cdot (1 - i, -2i)
$$
$$
\begin{cases}
\alpha + \beta + \gamma + \delta = 1 \\
\gamma - \delta = 1 \\
\gamma = 1 \\
\alpha - \beta - 2\delta = -1
\end{cases}
$$
$$
\gamma = 1 \implies \delta = 0 \implies \alpha + \beta = 0 \implies \alpha = -\beta \implies -2\beta = -1 \implies \beta = \frac{1}{2} \implies \alpha = -\frac{1}{2}
$$
$$
\implies coord_{\mathcal{B}}(1 + i, 1 - i) = \left( -\frac{1}{2}, \frac{1}{2}, 1, 0 \right)
$$

$$
(1 - i, 1 + i) = \alpha \cdot (1, i) + \beta \cdot (1, -i) + \gamma \cdot (1 + i, 1) + \delta \cdot (1 - i, -2i)
$$
$$
\begin{cases}
\alpha + \beta + \gamma + \delta = 1 \\
\gamma - \delta = -1 \\
\gamma = 1 \\
\alpha - \beta - 2\delta = 1
\end{cases}
$$
$$
\gamma = 1 \implies \delta = 2 \implies \alpha + \beta = -2 \land \alpha - \beta = 5 \implies 2\alpha = 3 \implies \alpha = \frac{3}{2} \implies \beta = -\frac{7}{2}
$$
$$
\implies coord_{\mathcal{B}}(1 - i, 1 + i) = \left( \frac{3}{2}, -\frac{7}{2}, 1, 2 \right)
$$

$$
(2 + i, i) = \alpha \cdot (1, i) + \beta \cdot (1, -i) + \gamma \cdot (1 + i, 1) + \delta \cdot (1 - i, -2i)
$$
$$
\begin{cases}
\alpha + \beta + \gamma + \delta = 2 \\
\gamma - \delta = 1 \\
\gamma = 0 \\
\alpha - \beta - 2\delta = 1
\end{cases}
$$
$$
\gamma = 0 \implies \delta = -1 \implies \alpha + \beta = 3 \land \alpha - \beta = -1 \implies 2\alpha = 2 \implies \alpha = 1 \implies \beta = 2
$$
$$
\implies coord_{\mathcal{B}}(2 + i, i) = \left( 1, 2, 0, -1 \right)
$$

$$
(1 - 3i, 1 + i) = \alpha \cdot (1 - 3i, 1 + i) + \beta \cdot (1, -i) + \gamma \cdot (1 + i, 1) + \delta \cdot (1 - i, -2i)
$$
$$
\begin{cases}
\alpha + \beta + \gamma + \delta = 1 \\
\gamma - \delta = -3 \\
\gamma = 1 \\
\alpha - \beta - 2\delta = 1
\end{cases}
$$
$$
\gamma = 1 \implies \delta = 4 \implies \alpha + \beta = -4 \land \alpha - \beta = 9 \implies 2\alpha = 5 \implies \alpha = \frac{5}{2} \implies \beta = -\frac{13}{2}
$$
$$
\implies coord_{\mathcal{B}}(1 - 3i, 1 + i) = \left( \frac{5}{2}, -\frac{13}{2}, 1, 4 \right)
$$

Finalmente, podemos definir la matriz asociada $_{\mathcal{B}}(T)_{\mathcal{B}}$:
$$
_{\mathcal{B}}(T)_{\mathcal{B}} = \begin{pmatrix}
-\frac{1}{2} & \frac{3}{2} & 1 & \frac{5}{2} \\
\frac{1}{2} & -\frac{7}{2} & 2 & -\frac{13}{2} \\
1 & 1 & 0 & 1 \\
0 & 2 & -1 & 4
\end{pmatrix}
$$



---
## Ejercicio 13
Recordemos las transformaciones lineales del ejercicio 4:
$$
\begin{align}
&S \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} = dx^{3} + (b + c)x^{2} + ax \\
&T(x, y, z) = \begin{pmatrix}
x - y & y \\
y & y - z
\end{pmatrix} \\
&S \circ T = S(T(a, b, c)) = (b - c)x^{3} + 2bx^{2} + (a - b)x
\end{align}
$$
### Parte 1
1. Determinamos las imágenes de los vectores de $\mathcal{B}$:
$$
\begin{align}
&T(1, 2, 1) = \begin{pmatrix}
-1 & 2 \\
2 & 1
\end{pmatrix} \\
&T(1, 2, -1) = \begin{pmatrix}
-1 & 2 \\
2 & 3
\end{pmatrix} \\
&T(-1, 1, -2) = \begin{pmatrix}
-2 & 1 \\
1 & 3
\end{pmatrix}
\end{align}
$$

2. Determinamos las coordenadas en $\mathcal{A}$ de las imágenes anteriores:
$$
\begin{pmatrix}
-1 & 2 \\
2 & 1
\end{pmatrix} = \alpha \cdot \begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
0 & 1 \\
1 & 1
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & 0 \\
0 & 0
\end{pmatrix} + \delta \cdot \begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
\begin{cases}
\alpha - \gamma - \delta = -1 \\
\alpha + \beta + \delta = 2 \\
\beta - \delta = 2 \\
\alpha + \beta = 1
\end{cases}
$$
$$
\alpha + \beta = 1 \implies \delta = 1 \implies \beta = 3 \implies \alpha = -2 \implies \gamma = -2
$$
$$
\implies coord_{\mathcal{A}}\begin{pmatrix}
-1 & 2 \\
2 & 1
\end{pmatrix} = \left( -2, 3, -2, 1 \right)
$$

$$
\begin{pmatrix}
-1 & 2 \\
2 & 3
\end{pmatrix} = \alpha \cdot \begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
0 & 1 \\
1 & 1
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & 0 \\
0 & 0
\end{pmatrix} + \delta \cdot \begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
\begin{cases}
\alpha - \gamma - \delta = -1 \\
\alpha + \beta + \delta = 2 \\
\beta - \delta = 2 \\
\alpha + \beta = 3
\end{cases}
$$
$$
\alpha + \beta = 3 \implies \delta = -1 \implies \beta = 1 \implies \alpha = 2 \implies \gamma = 4
$$
$$
\implies coord_{\mathcal{A}}\begin{pmatrix}
-1 & 2 \\
2 & 3
\end{pmatrix} = \left( 2, 1, 4, -1 \right)
$$

$$
\begin{pmatrix}
-2 & 1 \\
1 & 3
\end{pmatrix} = \alpha \cdot \begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
0 & 1 \\
1 & 1
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & 0 \\
0 & 0
\end{pmatrix} + \delta \cdot \begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
\begin{cases}
\alpha - \gamma - \delta = -2 \\
\alpha + \beta + \delta = 1 \\
\beta - \delta = 1 \\
\alpha + \beta = 3
\end{cases}
$$
$$
\alpha + \beta = 3 \implies \delta = -2 \implies \beta = -1 \implies \alpha = 4 \implies \gamma = 8
$$
$$
\implies coord_{\mathcal{A}}\begin{pmatrix}
-2 & 1 \\
1 & 3
\end{pmatrix} = \left( 4, -1, 8, -2 \right)
$$

3. Expresamos la matriz asociada $_{\mathcal{A}}(T)_{\mathcal{B}}$:
$$
_{\mathcal{A}}(T)_{\mathcal{B}} = \begin{pmatrix}
-2 & 2 & 4 \\
3 & 1 & -1 \\
-2 & 4 & 8 \\
1 & -1 & -2
\end{pmatrix}
$$

### Parte 2
1. Determinamos las imágenes de los vectores de $\mathcal{A}$:
$$
\begin{align}
&S \begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix} = x^{3} + x^{2} + x \\
&S \begin{pmatrix}
0 & 1 \\
1 & 1
\end{pmatrix} = x^{3} + 2x^{2} \\
&S \begin{pmatrix}
-1 & 0 \\
0 & 0
\end{pmatrix} = -x \\
&S \begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix} = -x
\end{align}
$$

2. Determinamos las coordenadas en $\mathcal{C}$ de las imágenes anteriores:
$$
x^{3} + x^{2} + x = \alpha \cdot (x^{3}) + \beta \cdot (1 + x^{3}) + \gamma \cdot (x^{2} - 1) + \delta \cdot (-x)
$$
$$
\begin{cases}
\beta - \gamma = 0 \\
-\delta = 1 \\
\gamma = 1 \\
\alpha + \beta = 1
\end{cases}
$$
$$
\gamma = 1 \land \delta = -1 \implies \beta = 1 \implies \alpha = 0
$$
$$
\implies coord_{\mathcal{C}}(x^{3} + x^{2} + x) = \left( 0, 1, 1, -1 \right)
$$

$$
x^{3} + 2x^{2} = \alpha \cdot (x^{3}) + \beta \cdot (1 + x^{3}) + \gamma \cdot (x^{2} - 1) + \delta \cdot (-x)
$$
$$
\begin{cases}
\beta - \gamma = 0 \\
-\delta = 0 \\
\gamma = 2 \\
\alpha + \beta = 1
\end{cases}
$$
$$
\gamma = 2 \land \delta = 0 \implies \beta = 2 \implies \alpha = -1
$$
$$
\implies coord_{\mathcal{C}}(x^{3} + 2x^{2}) = \left( -1, 2, 2, 0 \right)
$$

$$
-x = \alpha \cdot (x^{3}) + \beta \cdot (1 + x^{3}) + \gamma \cdot (x^{2} - 1) + \delta \cdot (-x)
$$
$$
\begin{cases}
\beta - \gamma = 0 \\
-\delta = -1 \\
\gamma = 0 \\
\alpha + \beta = 0
\end{cases}
$$
$$
\gamma = 0 \land \delta = 1 \implies \beta = 0 \implies \alpha = 0
$$
$$
\implies coord_{\mathcal{C}}(-x) = \left( 0, 0, 0, 1 \right)
$$

3. Expresamos la matriz asociada $_{\mathcal{C}}(S)_{\mathcal{A}}$:
$$
_{\mathcal{C}}(S)_{\mathcal{A}} = \begin{pmatrix}
0 & -1 & 0 & 0 \\
1 & 2 & 0 & 0 \\
1 & 2 & 0 & 0 \\
-1 & 0 & 1 & 1
\end{pmatrix}
$$

### Parte 3
Podemos determinar a $_{\mathcal{C}}(S \circ T)_{\mathcal{B}}$ como el producto de las matrices anteriores:
$$
\begin{align}
_{\mathcal{C}}(S \circ T)_{\mathcal{B}} &= \space_{\mathcal{C}}(S)_{\mathcal{A}} \cdot \space_{\mathcal{A}}(T)_{\mathcal{B}} \\
&= \begin{pmatrix}
0 & -1 & 0 & 0 \\
1 & 2 & 0 & 0 \\
1 & 2 & 0 & 0 \\
-1 & 0 & 1 & 1
\end{pmatrix} \cdot \begin{pmatrix}
-2 & 2 & 4 \\
3 & 1 & -1 \\
-2 & 4 & 8 \\
1 & -1 & -2
\end{pmatrix} \\
&= \begin{pmatrix}
-3 & -1 & 1 \\
4 & 4 & 2 \\
4 & 4 & 2 \\
1 & 1 & 2
\end{pmatrix}
\end{align}
$$

En conclusión:
$$
_{\mathcal{C}}(S \circ T)_{\mathcal{B}} = \begin{pmatrix}
-3 & -1 & 1 \\
4 & 4 & 2 \\
4 & 4 & 2 \\
1 & 1 & 2
\end{pmatrix}
$$

---
## Ejercicio 14
Consideremos que el ejercicio pide lo contrario ($_{\mathcal{A}}(Id)_{\mathcal{E}}$ en lugar de $_{\mathcal{E}}(Id)_{\mathcal{A}}$), ya que de otra forma la matriz buscada siempre sería la identidad.

Comencemos estudiando lo solicitado para $n = 2$ y $n = 3$:
- Caso $n = 2$:
$$
\begin{align}
&\mathcal{E} = \{ (1, 0), (0, 1) \} \\
&\mathcal{A} = \{ (1, 1), (2, 1) \}
\end{align}
$$

Básicamente, consideramos una transformación lineal dentro de un mismo espacio vectorial, que lo que hace es cambiar como se expresa un elemento.
Entonces, dicha matriz estará conformada por las coordenadas en la base $\mathcal{A}$ (arbitraria) de los elementos de la base $\mathcal{E}$ (canónica):
$$
\begin{align}
&(1, 0) = (-1) \cdot (1, 1) + 1 \cdot (2, 1) \implies coord_{\mathcal{A}}(1, 0) = (-1, 1) \\
&(0, 1) = 2 \cdot (1, 1) - 1 \cdot (2, 1) \implies coord_{\mathcal{A}}(0, 1) = (2, -1)
\end{align}
$$

De esta forma, podemos expresar la matriz:
$$
_{\mathcal{A}}(Id)_{\mathcal{E}} = \begin{pmatrix}
-1 & 2 \\
1 & -1
\end{pmatrix}
$$

- Caso $n = 3$:
$$
\begin{align}
&\mathcal{E} = \{ (1, 0, 0), (0, 1, 0), (0, 0, 1) \} \\
&\mathcal{A} = \{ (1, 1, 1), (1, 1, 0), (1, 0, 0) \}
\end{align}
$$

Expresamos las coordenadas en la base $\mathcal{A}$ de los vectores de la base $\mathcal{E}$:
$$
\begin{align}
&(1, 0, 0) = 0 \cdot (1, 1, 1) + 0 \cdot (1, 1, 0) + 1 \cdot (1, 0, 0) \implies coord_{\mathcal{A}}(1, 0, 0) = (0, 0, 1) \\
&(0, 1, 0) = 0 \cdot (1, 1, 1) + 1 \cdot (1, 1, 0) - 1 \cdot (1, 0, 0) \implies coord_{\mathcal{A}}(0, 1, 0) = (0, 1, -1) \\
&(0, 0, 1) = 1 \cdot (1, 1, 1) - 1 \cdot (1, 1, 0) + 0 \cdot (1, 0, 0) \implies coord_{\mathcal{A}}(0, 0, 1) = (1, -1, 0)
\end{align}
$$

De esta forma, podemos expresar la matriz:
$$
_{\mathcal{A}}(Id)_{\mathcal{E}} = \begin{pmatrix}
0 & 0 & 1 \\
0 & 1 & -1 \\
1 & -1 & 0
\end{pmatrix}
$$

Entonces, encontramos un patrón en como determinar la matriz cambio de base desde la base canónica hasta una base arbitraria, simplemente tenemos que:
1. Determinar las coordenadas en la base arbitraria de los vectores de la base canónica (tomar los elementos de la base canónica y expresarlos con los vectores de la base arbitraria).
2. Expresar la matriz "colgando" las coordenadas determinadas (considerando el orden de los vectores en la base).

Entonces, tenemos una base canónica:
$$
\mathcal{E} = \{ u_{1}, u_{2}, \dots, u_{n} \}
$$
Y una base arbitraria:
$$
\mathcal{A} = \{ v_{1}, v_{2}, \dots, v_{n} \}
$$

Determinamos las coordenadas en la base arbitraria de los vectores de la base canónica:
$$
\begin{align}
&u_{1} = a_{1,1} \cdot v_{1} + a_{2,1} \cdot v_{2} + \dots + a_{n,1} \cdot v_{n} \implies coord_{\mathcal{A}}(u_{1}) = (a_{1,1}, a_{2,1}, \dots, a_{n,1}) \\
&u_{2} = a_{1,2} \cdot v_{1} + a_{2,2} \cdot v_{2} + \dots + a_{n,2} \cdot v_{n} \implies coord_{\mathcal{A}}(u_{2}) = (a_{1,2}, a_{2,2}, \dots, a_{n,2}) \\
&\dots \\
&u_{n} = a_{1,n} \cdot v_{1} + a_{2,n} \cdot v_{2} + \dots + a_{n,n} \cdot v_{n} \implies coord_{\mathcal{A}}(u_{n}) = (a_{1,n}, a_{2,n}, \dots, a_{n,n})
\end{align}
$$

Finalmente, expresamos la matriz correspondiente:
$$
_{\mathcal{A}}(Id)_{\mathcal{E}} = \begin{pmatrix}
a_{1,1} & a_{2,1} & \dots & a_{n,1} \\
a_{1,2} & a_{2,2} & \dots & a_{n,2} \\
\vdots & \vdots & \vdots & \vdots \\
a_{1,n} & a_{2,n} & \dots & a_{n,n}
\end{pmatrix}
$$

CORRECCIÓN: En realidad, la letra del ejercicio era correcta.

Comencemos estudiando lo solicitado para $n = 2$ y $n = 3$:
- Caso $n = 2$:
$$
\begin{align}
&\mathcal{E} = \{ (1, 0), (0, 1) \} \\
&\mathcal{A} = \{ (1, 1), (2, 1) \}
\end{align}
$$

Básicamente, consideramos una transformación lineal dentro de un mismo espacio vectorial, que lo que hace es cambiar como se expresa un elemento.
Entonces, dicha matriz estará conformada por las coordenadas en la base $\mathcal{A}$ (arbitraria) de los elementos de la base $\mathcal{E}$ (canónica):
$$
\begin{align}
&(1, 1) = 1 \cdot (1, 0) + 1 \cdot (0, 1) \implies coord_{\mathcal{E}}(1, 1) = (1, 1) \\
&(2, 1) = 2 \cdot (1, 0) + 1 \cdot (0, 1) \implies coord_{\mathcal{E}}(2, 1) = (2, 1)
\end{align}
$$

De esta forma, podemos expresar la matriz:
$$
_{\mathcal{A}}(Id)_{\mathcal{E}} = \begin{pmatrix}
1 & 2 \\
1 & 1
\end{pmatrix}
$$

- Caso $n = 3$:
$$
\begin{align}
&\mathcal{E} = \{ (1, 0, 0), (0, 1, 0), (0, 0, 1) \} \\
&\mathcal{A} = \{ (1, 1, 1), (1, 1, 0), (1, 0, 0) \}
\end{align}
$$

Expresamos las coordenadas en la base $\mathcal{A}$ de los vectores de la base $\mathcal{E}$:
$$
\begin{align}
&(1, 1, 1) = 1 \cdot (1, 0, 0) + 1 \cdot (0, 1, 0) + 1 \cdot (0, 0, 1) \implies coord_{\mathcal{A}}(1, 1, 1) = (1, 1, 1) \\
&(1, 1, 0) = 1 \cdot (1, 0, 0) + 1 \cdot (0, 1, 0) + 0 \cdot (0, 0, 1) \implies coord_{\mathcal{A}}(1, 1, 0) = (1, 1, 0) \\
&(1, 0, 0) = 1 \cdot (1, 0, 0) + 0 \cdot (0, 1, 0) + 0 \cdot (0, 0, 1) \implies coord_{\mathcal{A}}(1, 0, 0) = (1, 0, 0)
\end{align}
$$

De esta forma, podemos expresar la matriz:
$$
_{\mathcal{A}}(Id)_{\mathcal{E}} = \begin{pmatrix}
1 & 1 & 1 \\
1 & 1 & 0 \\
1 & 0 & 0
\end{pmatrix}
$$

Entonces, podemos identificar un patrón:

Como queremos construir una matriz correspondiente a la transformación lineal identidad (no es necesario transformar los vectores de $\mathcal{A}$), definida a partir de las coordenadas de los vectores de la base $\mathcal{A}$ expresados con los elementos de la base $\mathcal{E}$, en realidad directamente estamos utilizando los elementos de la base $\mathcal{A}$ (ya que sus coordenadas en la base $\mathcal{E}$ equivale a su expresión natural). Entonces, simplemente hay que tomar los vectores de la base $\mathcal{A}$ y en ese mismo orden, usarlos para formar las columnas de la matriz $_{\mathcal{A}}(Id)_{\mathcal{E}}$.

---
## Ejercicio 15
### Parte 1
Tenemos que probar que:
$$
T(\alpha x_{1} + \beta x_{2}, \alpha y_{1} + \beta y_{2}, \alpha z_{1} + \beta z_{2}) = \alpha \cdot T(x_{1}, y_{1}, z_{1}) + \beta \cdot T(x_{2}, y_{2}, z_{2})
$$
$$
\begin{align}
T(\alpha x_{1} + \beta x_{2}, \alpha y_{1} + \beta y_{2}, \alpha z_{1} + \beta z_{2}) &= (\alpha y_{1} + \beta y_{2} - \alpha x_{1} - \beta x_{2}, \alpha z_{1} + \beta z_{2} + \alpha y_{1} + \beta y_{2}) \\
&= (\alpha y_{1} - \alpha x_{1} + \beta y_{2} - \beta x_{2}, \alpha z_{1} + \alpha y_{1} + \beta z_{2} + \beta y_{2}) \\
&= (\alpha \cdot (y_{1} - x_{1}) + \beta \cdot (y_{2} - x_{2}), \alpha \cdot (z_{1} + y_{1}) + \beta \cdot (z_{2} + y_{2})) \\
&= (\alpha \cdot (y_{1} - x_{1}), \alpha \cdot (z_{1} + y_{1})) + (\beta \cdot (y_{2} - x_{2}), \beta \cdot (z_{2} + y_{2})) \\
&= \alpha \cdot (y_{1} - x_{1}, z_{1} + y_{1}) + \beta \cdot (y_{2} - x_{2}, z_{2} + y_{2}) \\
&= \alpha \cdot T(x_{1}, y_{1}, z_{1}) + \beta \cdot T(x_{2}, y_{2}, z_{2})
\end{align}
$$

### Parte 2
$$
\begin{align}
&E = \{ (1, 0, 0), (0, 1, 0), (0, 0, 1) \} \\
&E' = \{ (1, 0), (0, 1) \}
\end{align}
$$

Sigamos los siguientes pasos:
1. Determinemos las imágenes de los elementos de $E$:
$$
\begin{align}
&T(1, 0, 0) = (-1, 0) \\
&T(0, 1, 0) = (1, 1) \\
&T(0, 0, 1) = (0, 1)
\end{align}
$$

2. Hallamos las coordenadas en la base $E'$ de las imágenes anteriores:
Considerando el ejercicio 14, las coordenadas en la base canónica de un vector, es el mismo vector, por lo que:
$$
\begin{align}
&coord_{E'}(-1, 0) = (-1, 0) \\
&coord_{E'}(1, 1) = (1, 1) \\
&coord_{E'}(0, 1) = (0, 1)
\end{align}
$$

3. Expresar la matriz asociada correspondiente:
Considerando las coordenadas halladas como columnas de la matriz asociada:
$$
_{E'}(T)_{E} = \begin{pmatrix}
-1 & 1 & 0 \\
0 & 1 & 1
\end{pmatrix}
$$

### Parte 3
Probamos que $A$ es base:
$$
(0, 0, 0) = \alpha \cdot (1, 0, 1) + \beta \cdot (0, 2, 1) + \gamma \cdot (-1, -1, 2)
$$
$$
\begin{cases}
\alpha - \gamma = 0 \\
2\beta - \gamma = 0 \\
\alpha + \beta + 2\gamma = 0
\end{cases}
$$
$$
\alpha = 2\beta \implies 3\beta + 2\gamma = 0 \implies 7\beta = 0 \implies \beta = 0 \implies \gamma = 0 \implies \alpha = 0
$$
Efectivamente, $A$ es LI, y por lo tanto base del espacio vectorial $\mathbb{R}^{3}$.

Probamos que $B$ es base:
$$
(0, 0) = \alpha \cdot (3, -1) + \beta \cdot (-1, 3)
$$
$$
\begin{cases}
3\alpha - \beta = 0 \\
-\alpha + 3\beta = 0
\end{cases}
$$
$$
\alpha = 3\beta \implies 8\beta = 0 \implies \beta = 0 \implies \alpha = 0
$$
Efectivamente, $B$ es LI, y por lo tanto base del espacio vectorial $\mathbb{R}^{2}$.

Para encontrar la matriz asociada $_{B}(T)_{A}$, aprovecharemos la siguiente igualdad (teorema que se encuentra explicado y probado en las notas del curso):
$$
_{B}(T)_{A} = \space _{B}(Id)_{E'} \cdot \space _{E'}(T)_{E} \cdot \space _{E}(Id)_{A}
$$

Entonces, simplemente tenemos que determinar las dos matrices cambio de base:
- $_{E}(Id)_{A}$
Es sumamente sencillo, ya que considerando que las coordenadas en la base canónica $E$ de los elementos de la base $A$ son propiamente los elementos de la base $A$, simplemente utilizamos los mismos para formar la matriz:
$$
_{E}(Id)_{A} = \begin{pmatrix}
1 & 0 & -1 \\
0 & 2 & -1 \\
1 & 1 & 2
\end{pmatrix}
$$

- $_{B}(Id)_{E'}$
En este caso, tenemos que determinar las coordenadas en la base $B$ de los elementos de la base canónica $E'$:
$$
(1, 0) = \alpha \cdot (3, -1) + \beta \cdot (-1, 3)
$$
$$
\begin{cases}
3\alpha - \beta = 1 \\
-\alpha + 3\beta = 0
\end{cases}
$$
$$
3\beta = \alpha \implies 8\beta = 1 \implies \beta = \frac{1}{8} \implies \alpha = \frac{3}{8}
$$
$$
\implies coord_{B}(1, 0) = \left( \frac{3}{8}, \frac{1}{8} \right)
$$

$$
(0, 1) = \alpha \cdot (3, -1) + \beta \cdot (-1, 3)
$$
$$
\begin{cases}
3\alpha - \beta = 0 \\
-\alpha + 3\beta = 1
\end{cases}
$$
$$
3\alpha = \beta \implies 8\alpha = 1 \implies \alpha = \frac{1}{8} \implies \beta = \frac{3}{8}
$$
$$
\implies coord_{B}(0, 1) = \left( \frac{1}{8}, \frac{3}{8} \right)
$$

Proseguimos a expresar la matriz:
$$
_{B}(Id)_{E'} = \begin{pmatrix}
\frac{3}{8} & \frac{1}{8} \\
\frac{1}{8} & \frac{3}{8}
\end{pmatrix}
$$


Calculamos los productos correspondientes:
$$
\begin{align}
_{B}(T)_{A} &= \space _{B}(Id)_{E'} \cdot \space _{E'}(T)_{E} \cdot \space _{E}(Id)_{A} \\
&= \begin{pmatrix}
\frac{3}{8} & \frac{1}{8} \\
\frac{1}{8} & \frac{3}{8}
\end{pmatrix} \cdot \begin{pmatrix}
-1 & 1 & 0 \\
0 & 1 & 1
\end{pmatrix} \cdot \begin{pmatrix}
1 & 0 & -1 \\
0 & 2 & -1 \\
1 & 1 & 2
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{3}{8} & \frac{1}{8} \\
\frac{1}{8} & \frac{3}{8}
\end{pmatrix} \cdot \begin{pmatrix}
-1 & 2 & 0 \\
1 & 3 & 1
\end{pmatrix} \\
&= \begin{pmatrix}
-\frac{2}{8} & \frac{9}{8} & \frac{1}{8} \\
\frac{2}{8} & \frac{9}{8} & \frac{3}{8}
\end{pmatrix}
\end{align}
$$

En conclusión:
$$
_{B}(T)_{A} = \begin{pmatrix}
-\frac{2}{8} & \frac{9}{8} & \frac{1}{8} \\
\frac{2}{8} & \frac{11}{8} & \frac{3}{8}
\end{pmatrix}
$$

---
## Ejercicio 16
### Parte a
1. Expresamos las coordenadas en la base $\mathcal{B}$ de los elementos de la base $\mathcal{A}$:
$$
(0, 2, 1) = \alpha \cdot (1, 2, 1) + \beta \cdot (1, 2, -1) + \gamma \cdot (-1, 1, -2)
$$
$$
\begin{cases}
\alpha + \beta - \gamma = 0 \\
2\alpha + 2\beta + \gamma = 2 \\
\alpha - \beta - 2\gamma = 1
\end{cases}
$$
$$
F_{2} - 2F_{1} \implies 3\gamma = 2 \implies \gamma = \frac{2}{3} \implies \alpha + \beta = \frac{2}{3} \land \alpha - \beta = \frac{7}{3} \implies 2\alpha = 3 \implies \alpha = \frac{3}{2} \implies \beta = -\frac{5}{6}
$$
$$
\implies coord_{\mathcal{B}}(0, 2, 1) = \left( \frac{3}{2}, -\frac{5}{6}, \frac{2}{3} \right)
$$

$$
(1, 1, 0) = \alpha \cdot (1, 2, 1) + \beta \cdot (1, 2, -1) + \gamma \cdot (-1, 1, -2)
$$
$$
\begin{cases}
\alpha + \beta - \gamma = 1 \\
2\alpha + 2\beta + \gamma = 1 \\
\alpha - \beta - 2\gamma = 0
\end{cases}
$$
$$
F_{2} - 2F_{1} \implies 3\gamma = -1 \implies \gamma = -\frac{1}{3} \implies \alpha + \beta = \frac{2}{3} \land \alpha - \beta = -\frac{2}{3} \implies 2\alpha = 3 \implies \alpha = 0 \implies \beta = \frac{2}{3}
$$
$$
\implies coord_{\mathcal{B}}(1, 1, 0) = \left( 0, \frac{2}{3}, -\frac{1}{3} \right)
$$

$$
(-1, -1, 1) = \alpha \cdot (1, 2, 1) + \beta \cdot (1, 2, -1) + \gamma \cdot (-1, 1, -2)
$$
$$
\begin{cases}
\alpha + \beta - \gamma = -1 \\
2\alpha + 2\beta + \gamma = -1 \\
\alpha - \beta - 2\gamma = 1
\end{cases}
$$
$$
F_{2} - 2F_{1} \implies 3\gamma = 1 \implies \gamma = \frac{1}{3} \implies \alpha + \beta = -\frac{2}{3} \land \alpha - \beta = \frac{5}{3} \implies 2\alpha = 1 \implies \alpha = \frac{1}{2} \implies \beta = -\frac{7}{6}
$$
$$
\implies coord_{\mathcal{B}}(-1, -1, 1) = \left( \frac{1}{2}, -\frac{7}{6}, \frac{1}{3} \right)
$$

2. Finalmente, expresamos la matriz de cambio de base $_{\mathcal{B}}(Id)_{\mathcal{A}}$:
$$
_{\mathcal{B}}(Id)_{\mathcal{A}} = \begin{pmatrix}
\frac{3}{2} & 0 & \frac{1}{2} \\
-\frac{5}{6} & \frac{2}{3} & -\frac{7}{6} \\
\frac{2}{3} & -\frac{1}{3} & \frac{1}{3}
\end{pmatrix}
$$

### Parte b
1. Expresamos las coordenadas en la base $\mathcal{B}$ de los elementos de la base $\mathcal{A}$:
$$
x^{3} = \alpha \cdot (x^{3} - x) + \beta \cdot (1 + x^{2}) + \gamma \cdot (x^{2} - x) + \delta \cdot (2)
$$
$$
\begin{cases}
\beta + 2\delta = 0 \\
-\alpha - \gamma = 0 \\
\beta + \gamma = 0 \\
\alpha = 1
\end{cases}
$$
$$
\alpha = 1 \implies \gamma = -1 \implies \beta = 1 \implies \delta = -\frac{1}{2}
$$
$$
\implies coord_{\mathcal{B}}(x^{3}) = \left( 1, 1, -1, -\frac{1}{2} \right)
$$

$$
1 + x^{3} = \alpha \cdot (x^{3} - x) + \beta \cdot (1 + x^{2}) + \gamma \cdot (x^{2} - x) + \delta \cdot (2)
$$
$$
\begin{cases}
\beta + 2\delta = 1 \\
-\alpha - \gamma = 0 \\
\beta + \gamma = 0 \\
\alpha = 1
\end{cases}
$$
$$
\alpha = 1 \implies \gamma = -1 \implies \beta = 1 \implies \delta = 0
$$
$$
\implies coord_{\mathcal{B}}(1 + x^{3}) = \left( 1, 1, -1, 0 \right)
$$

$$
x^{2} - 1 = \alpha \cdot (x^{3} - x) + \beta \cdot (1 + x^{2}) + \gamma \cdot (x^{2} - x) + \delta \cdot (2)
$$
$$
\begin{cases}
\beta + 2\delta = -1 \\
-\alpha - \gamma = 0 \\
\beta + \gamma = 1 \\
\alpha = 0
\end{cases}
$$
$$
\alpha = 0 \implies \gamma = 0 \implies \beta = 1 \implies \delta = -1
$$
$$
\implies coord_{\mathcal{B}}(x^{2} - 1) = \left( 0, 1, 0, -1 \right)
$$

$$
-x = \alpha \cdot (x^{3} - x) + \beta \cdot (1 + x^{2}) + \gamma \cdot (x^{2} - x) + \delta \cdot (2)
$$
$$
\begin{cases}
\beta + 2\delta = 0 \\
-\alpha - \gamma = -1 \\
\beta + \gamma = 0 \\
\alpha = 0
\end{cases}
$$
$$
\alpha = 0 \implies \gamma = 1 \implies \beta = -1 \implies \delta = \frac{1}{2}
$$
$$
\implies coord_{\mathcal{B}}(-x) = \left( 0, -1, 1, \frac{1}{2} \right)
$$

2. Finalmente, expresamos la matriz de cambio de base $_{\mathcal{B}}(Id)_{\mathcal{A}}$:
$$
_{\mathcal{B}}(Id)_{\mathcal{A}} = \begin{pmatrix}
1 & 1 & 0 & 0 \\
1 & 1 & 1 & -1 \\
-1 & -1 & 0 & 1 \\
-\frac{1}{2} & 0 & -1 & \frac{1}{2}
\end{pmatrix}
$$

### Parte 3
1. Expresamos las coordenadas en la base $\mathcal{B}$ de los elementos de la base $\mathcal{A}$:
$$
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix} = \alpha \cdot \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & 1 \\
0 & 0
\end{pmatrix} + \delta \cdot \begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
\begin{cases}
\alpha - \gamma - \delta = 1 \\
\beta + \gamma + \delta = 1 \\
\beta - \delta = 0 \\
\alpha = 1
\end{cases}
$$
$$
\alpha = 1 \implies -\gamma - \delta = 0 \implies \beta = 1 \implies \delta = 1 \implies \gamma = -1
$$
$$
\implies coord_{\mathcal{B}}\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix} = \left( 1, 1, -1, 1 \right)
$$

$$
\begin{pmatrix}
0 & 1 \\
1 & 1
\end{pmatrix} = \alpha \cdot \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & 1 \\
0 & 0
\end{pmatrix} + \delta \cdot \begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
\begin{cases}
\alpha - \gamma - \delta = 0 \\
\beta + \gamma + \delta = 1 \\
\beta - \delta = 1 \\
\alpha = 1
\end{cases}
$$
$$
\alpha = 1 \implies -\gamma - \delta = -1 \implies \gamma + \delta = 1 \implies \beta = 0 \implies \delta = -1 \implies \gamma = 2
$$
$$
\implies coord_{\mathcal{B}}\begin{pmatrix}
0 & 1 \\
1 & 1
\end{pmatrix} = \left( 1, 0, 2, -1 \right)
$$

$$
\begin{pmatrix}
-1 & 0 \\
0 & 0
\end{pmatrix} = \alpha \cdot \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & 1 \\
0 & 0
\end{pmatrix} + \delta \cdot \begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
\begin{cases}
\alpha - \gamma - \delta = -1 \\
\beta + \gamma + \delta = 0 \\
\beta - \delta = 0 \\
\alpha = 0
\end{cases}
$$
$$
\alpha = 0 \implies -\gamma - \delta = -1 \implies \gamma + \delta = 1 \implies \beta = -1 \implies \delta = -1 \implies \gamma = 2
$$
$$
\implies coord_{\mathcal{B}}\begin{pmatrix}
-1 & 0 \\
0 & 0
\end{pmatrix} = \left( 0, -1, 2, -1 \right)
$$

$$
\begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix} = \alpha \cdot \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} + \beta \cdot \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} + \gamma \cdot \begin{pmatrix}
-1 & 1 \\
0 & 0
\end{pmatrix} + \delta \cdot \begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix}
$$
$$
\begin{cases}
\alpha - \gamma - \delta = -1 \\
\beta + \gamma + \delta = 1 \\
\beta - \delta = -1 \\
\alpha = 0
\end{cases}
$$
$$
\alpha = 0 \implies -\gamma - \delta = -1 \implies \gamma + \delta = 1 \implies \beta = 0 \implies \delta = 1 \implies \gamma = 0
$$
$$
\implies coord_{\mathcal{B}}\begin{pmatrix}
-1 & 1 \\
-1 & 0
\end{pmatrix} = \left( 0, 0, 0, 1 \right)
$$

2. Finalmente, expresamos la matriz de cambio de base $_{\mathcal{B}}(Id)_{\mathcal{A}}$:
$$
_{\mathcal{B}}(Id)_{\mathcal{A}} = \begin{pmatrix}
1 & 1 & 0 & 0 \\
1 & 0 & -1 & 0 \\
-1 & 2 & 2 & 0 \\
1 & -1 & -1 & 1
\end{pmatrix}
$$

---
## Ejercicio 17
### Parte 1
Si consideramos $\mathcal{B} = \{ w_{1}, \dots, w_{n} \}$:
$$
u = a_{1} w_{1} + \dots + a_{n} w_{n} \implies T(u) = (a_{1}, \dots, a_{n}) \text{ y } v = b_{1} w_{1} + \dots + b_{n} w_{n} \implies T(v) = (b_{1}, \dots, b_{n})
$$
$$
\begin{align}
T(\alpha \cdot u + \beta \cdot v) &\overset{?} = \alpha \cdot T(u) + \beta \cdot T(v) \\
T(\alpha \cdot u + \beta \cdot v) &= (\alpha a_{1} + \beta b_{1}, \dots, \alpha a_{n} + \beta b_{n}) \\
&= (\alpha a_{1}, \dots, \alpha a_{n}) + (\beta b_{1}, \dots, \beta b_{n}) \\
&= \alpha \cdot (a_{1}, \dots, a_{n}) + \beta \cdot (b_{1}, \dots, b_{n}) \\
&= \alpha \cdot T(u) + \beta \cdot T(v)
\end{align}
$$
Como vemos, la transformación lineal propuesta es efectivamente lineal.

### Parte 2
Si multiplicáramos las coordenadas en la base $\mathcal{B}$ de un vector $w$ por dicha matriz, obtendríamos las coordenadas en la base $\mathcal{E}$ del mismo vector.

Entonces, para formar la matriz, tenemos que tomar los vectores de la base $\mathcal{B}$, encontrar sus imágenes y determinar sus coordenadas en la base $\mathcal{E}$. Dichas coordenadas serán las columnas de la matriz correspondiente.

Recordemos que $T(v) = coord_{\mathcal{B}}(v)$, entonces tenemos que encontrar las coordenadas en la base canónica de $\mathbb{R}^{n}$ de vectores que ya de por si pertenecen a $\mathbb{R}^{n}$. Por lo tanto, $T(v) = coord_{\mathcal{B}}(v) = coord_{\mathcal{E}}(coord_{\mathcal{B}}(v))$

De esta manera, si consideramos $\mathcal{B} = \{ w_{1}, \dots, w_{n} \}$ y
$$
\begin{align}
&w_{1} = a_{1} w_{1} + a_{2} w_{2} + \dots + a_{n} w_{n} \implies T(w_{1}) = (a_{1}, a_{2}, \dots, a_{n}) = (1, 0, \dots, 0) \\
&w_{2} = a_{1} w_{1} + a_{2} w_{2} + \dots + a_{n} w_{n} \implies T(w_{2}) = (a_{1}, a_{2}, \dots, a_{n}) = (0, 1, \dots, 0) \\
&\dots \\
&w_{n} = a_{1} w_{1} + a_{2} w_{2} + \dots + a_{n} w_{n} \implies T(w_{n}) = (a_{1}, a_{2}, \dots, a_{n}) = (0, 0, \dots, 1)
\end{align}
$$

Entonces, la matriz $_{\mathcal{E}}(T)_{B}$ es:
$$
_{\mathcal{E}}(T)_{B} = \begin{pmatrix}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 1
\end{pmatrix}
$$

### Parte 3
Consideremos la siguiente transformación lineal:
- $T_{1}$ tal que $T_{1}(v) = coord_{B_{1}}(v)$, $\mathcal{B}_{1} = \{ a_{1}, a_{2}, \dots, a_{n} \}$
- $T_{2}$ tal que $T_{2}(v) = coord_{B_{2}}(v)$, $\mathcal{B}_{2} = \{ b_{1}, b_{2}, \dots, b_{n} \}$

Para formar la matriz $_{\mathcal{B}_{1}}(Id)_{\mathcal{B_{2}}}$, hay que tomar los elementos de $\mathcal{B}_{2}$ determinar sus coordenadas con la matriz $\mathcal{B}_{1}$:
$$
\begin{align}
&b_{1} = \alpha_{1,1} \cdot a_{1} + \alpha_{2,1} \cdot a_{2} + \dots + \alpha_{n,1} \cdot a_{n} \implies coord_{\mathcal{B}_{1}}(b_{1}) = (\alpha_{1,1}, \alpha_{2,1}, \dots, \alpha_{n,1}) \\
&b_{2} = \alpha_{2,1} \cdot a_{1} + \alpha_{2,2} \cdot a_{2} + \dots + \alpha_{n,2} \cdot a_{n} \implies coord_{\mathcal{B}_{1}}(b_{2}) = (\alpha_{1,2}, \alpha_{2,2}, \dots, \alpha_{n,2}) \\
&\dots \\
&b_{n} = \alpha_{n, 1} \cdot a_{1} + \alpha_{2,n} \cdot a_{2} + \dots + \alpha_{n,n} \cdot a_{n} \implies coord_{\mathcal{B}_{1}}(b_{n}) = (\alpha_{1,n}, \alpha_{2,n}, \dots, \alpha_{n,n})
\end{align}
$$
$$
_{\mathcal{B}_{1}}(Id)_{\mathcal{B_{2}}} = \begin{pmatrix}
\alpha_{1,1} & \alpha_{1,2} & \dots & \alpha_{1,n} \\
\alpha_{2,1} & \alpha_{2,2} & \dots & \alpha_{2,n} \\
\vdots & \vdots & \vdots & \vdots \\
\alpha_{n,1} & \alpha_{n,2} & \dots & \alpha_{n,n}
\end{pmatrix}
$$

Esta matriz cumple la siguiente característica:
$$
coord_{\mathcal{B}_{1}}(v) = \space _{\mathcal{B}_{1}}(Id)_{\mathcal{B_{2}}} \cdot coord_{\mathcal{B}_{2}}(v)
$$

Entonces, la relación entre las transformaciones lineales y la matriz es la siguiente:

La primera transformación lineal nos permite determinar las coordenadas en la base $\mathcal{B}_{1}$ de un vector perteneciente a $V$, mientras que la segunda tiene el mismo propósito pero para la base $\mathcal{B}_{2}$. La matriz $_{\mathcal{B}_{1}}(Id)_{\mathcal{B_{2}}}$ cumple el propósito de la primera transformación lineal, pero sin dejar de lado la segunda: si conocemos las coordenadas en la base $\mathcal{B}_{2}$ de un vector $v$, y realizamos el producto de dichas coordenadas por la matriz $_{\mathcal{B}_{1}}(Id)_{\mathcal{B_{2}}}$, obtenemos las coordenadas en la base $\mathcal{B}_{1}$ del mismo vector.






