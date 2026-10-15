# Combinaciones lineales y generadores
## Ejercicio 1
Una parte por cada espacio vectorial.

Básicamente, en cada uno de estos casos, tenemos que resolver un sistema. Lo que queremos comprobar es si $v \in [\mathcal{A}]$.

Para verificar si un vector $v = (v_{1}, \dots, v_{m})$ puede escribirse como combinación lineal de una serie de vectores $u_{1}, \dots, u_{n}$, tenemos que encontrar coeficientes $\alpha_{1}, \dots, \alpha_{n}$ que verifiquen:
$$
v = \alpha_{1}u_{1} + \dots + \alpha_{n}u_{n} \implies v = (\alpha_{1}u_{1,1} + \dots + \alpha_{n}u_{n,1}, \dots ,\alpha_{1}u_{1,m} + \dots + \alpha_{n}u_{n,m})
$$
### Parte a)
$$
\mathcal{A} = \{ (1, 2, 1), (3, -1, 5), (1, 1, 0) \}, v = (3, 0, 6)
$$
Tenemos que resolver el siguiente sistema:
$$
\begin{cases}
\alpha + 3\beta + \gamma = 3 \\
2\alpha - \beta + \gamma = 0 \\
\alpha + 5\beta = 6
\end{cases}
$$
Si encontramos una solución para el sistema anterior, entonces, efectivamente $v$ se puede escribir como combinación lineal de los vectores de $A$.

Lo resolveremos en forma de matriz:
$$
\left(
\begin{array}{ccc|c}
1 & 3 & 1 & 3 \\
2 & -1 & 1 & 0 \\
1 & 5 & 0 & 6
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
-1 & 4 & 0 & 3 \\
2 & -1 & 1 & 0 \\
1 & 5 & 0 & 6
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 9 & 0 & 9 \\
2 & -1 & 1 & 0 \\
1 & 5 & 0 & 6
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & 1 \\
2 & -1 & 1 & 0 \\
1 & 5 & 0 & 6
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{9}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & 1 \\
2 & -1 & 1 & 0 \\
1 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - 5F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & 1 \\
2 & 0 & 1 & 1 \\
1 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & 1 \\
0 & 0 & 1 & -1 \\
1 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 1 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & -1
\end{array}
\right)
$$
Determinamos que $(1, 1, -1)$ es solución del sistema anterior.

En conclusión, $v \in [\mathcal{A}]$, ya que se puede escribir como combinación lineal de los vectores pertenecientes a $\mathcal{A}$, como mostramos a continuación:
$$
\begin{align}
v &= (3, 0, 6) \\
&= \alpha(1, 2, 1) + \beta(3, -1, 5) + \gamma(1, 1, 0) \\
&= (\alpha + 3\beta + \gamma, 2\alpha - \beta + \gamma, \alpha + 5\beta) \\
&= (1 + 3 \cdot 1 + (-1), 2 \cdot 1 - 1 + (-1), 1 + 5 \cdot 1) \\
&= (3, 0, 6)
\end{align}
$$

### Parte d)
$$
\mathcal{A} = \{ 3x^{3} + x, -2x^{2} + x - 1, 3^{3} - 2x^{2} + 2x - 1 \}, v = -3x^{3} + 4x^{2} + x - 2
$$
Tenemos que resolver el siguiente sistema:
$$
\begin{cases}
3\alpha + 3\gamma = -3 \\
-2\beta - 2\gamma = 4 \\
\alpha + \beta + 2\gamma = 1 \\
-\beta - \gamma = -2
\end{cases}
$$
Lo resolveremos en forma de matriz:
$$
\left(
\begin{array}{ccc|c}
3 & 0 & 3 & -3 \\
0 & -2 & -2 & 4 \\
1 & 1 & 2 & 1 \\
0 & -1 & -1 & -2
\end{array}
\right)
$$
Como vemos, las filas 2 y 4 son múltiplos (ignorando la parte de términos independientes).

$$
\left(
\begin{array}{ccc|c}
3 & 0 & 3 & -3 \\
0 & -2 & -2 & 4 \\
1 & 1 & 2 & 1 \\
0 & 1 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow -F_{4}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
3 & 0 & 3 & -3 \\
0 & 0 & 0 & 8 \\
1 & 1 & 2 & 1 \\
0 & 1 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + 2F_{4}
\end{align}
$$
Como vemos, anulamos la fila 2, pero llegamos a una incoherencia. Por lo tanto, comprobamos que el sistema no tiene solución. Esto significa que $v \not \in [\mathcal{A}]$, puesto que no se puede escribir como combinación lineal de los vectores pertenecientes a $\mathcal{A}$.

### Parte f)
$$
\mathcal{A} = \left\{ \begin{pmatrix}
2 & -3 \\
4 & 1
\end{pmatrix}, \begin{pmatrix}
0 & 5 \\
1 & -2
\end{pmatrix}, \begin{pmatrix}
6 & -19 \\
10 & 7
\end{pmatrix} \right\}, v = \begin{pmatrix}
6 & 2 \\
9 & 11
\end{pmatrix}
$$
Tenemos que resolver el siguiente sistema:
$$
\begin{cases}
2\alpha + 6\gamma = 6 \\
-3\alpha + 5\beta - 19\gamma = 2 \\
4\alpha + \beta + 10\gamma = 9 \\
\alpha - 2\beta + 7\gamma = 11
\end{cases}
$$
Lo resolveremos en forma de matriz:
$$
\left(
\begin{array}{ccc|c}
2 & 0 & 6 & 6 \\
-3 & 5 & -19 & 2 \\
4 & 1 & 10 & 9 \\
1 & -2 & 7 & 11
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
2 & 0 & 6 & 6 \\
5 & 5 & 5 & 26 \\
2 & 1 & 4 & 3 \\
-1 & -2 & 1 & 5
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + 4F_{1} \\
&F_{3} \leftarrow F_{3} - F_{1} \\
&F_{4} \leftarrow F_{4} - F_{1} \\
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
2 & 0 & 6 & 6 \\
1 & 1 & 1 & \frac{26}{5} \\
2 & 1 & 4 & 3 \\
-1 & -2 & 1 & 5
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{5}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
2 & 0 & 6 & 6 \\
1 & 1 & 1 & \frac{26}{5} \\
1 & 0 & 3 & -\frac{11}{5} \\
1 & 0 & 3 & \frac{77}{5}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2} \\
&F_{4} \leftarrow F_{4} + 2F_{2}
\end{align}
$$
En este caso, también llegamos a una incoherencia, ya que las filas 3 y 4 son identicas, pero difieren en su término independiente (no puede ser que $\alpha + 3\gamma = -\frac{11}{5}$ y $\alpha + 3\gamma = \frac{77}{5}$ al mismo tiempo).

Por lo tanto, comprobamos que el sistema no tiene solución. Esto significa que $v \not \in [\mathcal{A}]$, puesto que no se puede escribir como combinación lineal de los vectores pertenecientes a $\mathcal{A}$.


---
## Ejercicio 2
Tres partes.

Un generador de un espacio $V$ es un conjunto para el cual, si consideramos todas las combinaciones lineales posibles de sus elementos, el resultado equivale al espacio $V$.

### Parte b)
$$
S = \{ p \in \mathbb{R}_{3}[x] : p(1 - x) = p(1 + x), \forall x \in \mathbb{R} \}
$$
Como vemos, el generador que tenemos que hallar estará compuesto por polinomios de tercer grado o menor, debido a que los polinomios pertenecientes a $S$ tienen la siguiente forma:
$$
ax^{3} + bx^{2} + cx + d
$$
Además, dichos polinomios cumplen que:
$$
\begin{align}
a(1 - x)^{3} + b(1 - x)^{2} + c(1 - x) + d &= a(1 + x)^{3} + b(1 + x)^{2} + c(1 + x) + d \\
a(1 - 3x + 3x^{2} - x^{3}) + b(1 - 2x + x^{2}) + c(1 - x) + d &= a(1 + 3x + 3x^{2} + x^{3}) + b(1 + 2x + x^{2}) + c(1 + x) + d \\
\cancel{ a } - 3ax + \cancel{ 3ax^{2} } - ax^{3} + \cancel{ b } - 2bx + \cancel{ bx^{2} } + \cancel{ c } - cx + \cancel{ d } &= \cancel{ a } + 3ax + \cancel{ 3ax^{2} } + ax^{3} + \cancel{ b } + 2bx + \cancel{ bx^{2} } + \cancel{ c } + cx + \cancel{ d } \\
-3ax - ax^{3} - 2bx - cx &= 3ax + ax^{3} + 2bx + cx \\
-ax^{3} - x(3a + 2b + c) &= ax^{3} + x(3a + 2b + c)
\end{align}
$$
Entonces, los polinomios pertenecientes a $S$ tienen que cumplir que:
$$
-ax^{3} = ax^{3} \land -x(3a + 2b + c) = x(3a + 2b + c)
$$
$$
\begin{align}
&-ax^{3} = ax^{3} \implies 2ax^{3} = 0 \implies a = 0 \\
&-x(3a + 2b + c) = x(3a + 2b + c) \implies 2x(3a + 2b + c) = 0 \implies 3a + 2b + c = 0 \implies 2b + c = 0 \Longleftrightarrow -2b = c
\end{align}
$$
Cumpliendo esas dos cosas, sin importar el resto de elementos, sabemos que verifica la igualdad $p(1 - x) = p(1 + x)$.

Entonces, podemos generalizar la forma de dichos conjuntos como:
$$
\begin{align}
ax^{3} + bx^{2} + cx + d &= bx^{2} + cx + d \\
&= bx^{2} - 2bx + d
\end{align}
$$
Sabiendo que la forma generalizada de los polinomios de $\mathbb{R}_{3}[x]$ que cumplen $p(1 - x) = p(1 + x)$ es $bx^{2} - 2bx + d$, siendo $b$ el coeficiente de $x^{2}$ y $d$ el término independiente. Podemos considerar el siguiente generador:
$$
G = \{ x^{2} - 2x, 1 \}
$$
Dicho generador tiene sentido, ya que cualquier polinomio de la forma anterior sería una parábola cuyo vértice está en $x = 1$, y la constante $d$ simplemente desplaza verticalmente la función.

### Parte e)
$$
S = \{ A \in M_{3 \times 3}(\mathbb{R}) : A \text{ es antisimétrica} \}
$$
Analicemos que significa que una matriz sea antisimétrica: una matriz antisimétrica es aquella la cual está espejada de forma opuesta con respecto a la diagonal. Es un concepto que solo tiene sentido para matrices cuadradas. Las matrices antisimétricas de tamaño $3 \times 3$ tienen la siguiente forma:
$$
\begin{pmatrix}
\alpha & \beta & \gamma \\
-\beta & \delta & \epsilon \\
-\gamma & -\epsilon & \lambda
\end{pmatrix}
$$
Como vemos, esto se debe cumplir incluso para la diagonal, por lo que tiene que ser 0 (es la única forma que un número y su opuesto convivan en la misma celda). Fuera de la diagonal, cada vez que establecemos un valor en una posición $m, n$, tenemos que poner el valor opuesto en $n, m$.

Sabiendo esto, y en base a la generalización anterior, la cual especifica que las celdas espejadas tienen que tener valores opuestos, podemos conformar un generador con matrices casi nulas, que tenga valores no nulos únicamente en una celda (en caso de que se trate de la diagonal) o en dos celdas (una celda fuera de la diagonal y su espejo, con valores opuestos).

En base a todo lo mencionado anteriormente, concluimos definiendo el siguiente generador:
$$
G = \left\{ 
\begin{pmatrix}
0 & 1 & 0 \\
-1 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
-1 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 1 \\
0 & -1 & 0
\end{pmatrix}
\right\}
$$
ACLARACIÓN: En las matrices antisimétricas, la diagonal SIEMPRE es nula.

### Parte f)
$$
S = \{ (z_{1}, z_{2}, z_{3}) \in \mathbb{C}^{3} : z_{1} + iz_{2} + z_{3} = 0 \}
$$
Despejamos una de las variables:
$$
z_{1} + iz_{2} + z_{3} = 0 \implies z_{1} = -iz_{2} - z_{3}
$$
De esta manera, podemos expresar un vector genérico, sustituyendo $z_{1}$ por su equivalente. Luego, expresamos dicho vector como la suma de dos vectores multiplicado cada uno por un parámetro:
$$
(-iz_{2} - z_{3}, z_{2}, z_{3}) = z_{2}(-i, 1, 0) + z_{3}(-1, 0, 1)
$$
En conclusión, un generador del subespacio es:
$$
G = \{ (-i, 1, 0), (-1, 0, 1) \}
$$

### Parte g)
$$
S = \{ (z_{1}, z_{2}, z_{3}, z_{4}) \in \mathbb{C}^{4} : 2iz_{1} = z_{2}, z_{3} + z_{4} - iz_{2} = 0 \}
$$
Como vemos, trabajamos en un subespacio de cuádruplas de números complejos $(z_{1}, z_{2}, z_{3}, z_{4})$, el cual cumple dos características específicas:
$$
\begin{cases}
2iz_{1} = z_{2} \\
z_{3} + z_{4} - iz_{2} = 0
\end{cases}
$$
Al tener un sistema homogéneo, tenemos que expresar todas las variables en función de las variables libres. Por lo tanto, sustituimos $z_{2}$ en la segunda ecuación por $2iz_{1}$:
$$
\begin{align}
z_{3} + z_{4} - iz_{2} = 0 \implies &z_{3} + z_{4} - 2i^{2}z_{1} = 0 \\
&z_{3} + z_{4} + 2z_{1} = 0 \\
&z_{3} = -2z_{1} - z_{4}
\end{align}
$$
Entonces, expresamos un vector genérico utilizando únicamente $z_{1}$ y $z_{4}$, que son las variables libres del sistema:
$$
(z_{1}, 2iz_{1}, -2z_{1} - z_{4}, z_{4})
$$
A su vez, como tenemos dos variables libres, podemos expresar dicho vector como la suma de dos vectores, cada uno con los coeficientes adecuados y multiplicado por una variable libre:
$$
(z_{1}, 2iz_{1}, -2z_{1} - z_{4}, z_{4}) = z_{1}(1, 2i, -2, 0) + z_{4}(0, 0, -1, 1)
$$
En definitiva, estos dos vectores que multiplicados por una variable libre conforman el vector genérico anterior son los elementos cuyas combinaciones lineales conforman el espacio $\mathbb{C}^{4}$ con las propiedades establecidas. En conclusión, el generador determinado es:
$$
G = \left\{ (1, 2i, -2, 0), (1, 2i, 0, -2) \right\}
$$
ACLARACIÓN: Para hallar generadores en subespacios en los que se nos establece una estructura o reglas determinadas, no debemos asignar valores constantes. La estrategia es despejar las variables en función de los parámetros libres para separar los vectores directores

---
## Ejercicio 3



---
## Ejercicio 4
Primero que nada, podemos ver que $\mathcal{A}_{1}$ tiene un vector más que $\mathcal{A}_{2}$. Por esta razón, estudiaremos si dicho vector marca una diferencia, o se puede escribir como combinación lineal del resto. En caso de que $\mathcal{A}_{1}$ sea LI, entonces claramente los conjuntos no generan el mismo subespacio vectorial.

$$
\begin{cases}
\alpha + 2\gamma = 0 \\
2\alpha + \beta + 5\gamma = 0 \\
-\alpha + \beta - \gamma = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 2 & 0 \\
2 & 1 & 5 & 0 \\
-1 & 1 & -1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 2 & 0 \\
0 & 3 & 3 & 0 \\
-1 & 1 & -1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 2 & 0 \\
0 & 1 & 1 & 0 \\
-1 & 1 & -1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{3}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 2 & 0 \\
0 & 1 & 1 & 0 \\
-1 & 0 & -2 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 2 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
Logramos anular una fila, por lo que uno de los vectores es combinación lineal del resto. Si observamos cuidadosamente, es fácil ver que el vector $(0, 1, 1)$ se puede formar de la siguiente forma:
$$
(2, 5, -1) - 2(1, 2, -1) = (2 - 2, 5 - 4, -1 - (-2)) = (0, 1, 1)
$$
Ahora, podemos ignorar dicho vector. Lo que queda es ver si con los vectores restantes de $\mathcal{A}_{1}$ podemos formar los vectores de $\mathcal{A}_{2}$ y viceversa.
$$
\begin{align}
&\mathcal{A}_{1} = \{ (1, 2, -1), (2, 5, -1) \} \\
&\mathcal{A}_{2} = \{ (-1, -3, 0), (1, 1, -2) \}
\end{align}
$$
$$
\begin{align}
&(-1, -3, 0) = (1, 2, -1) - (2, 5, -1) = (1 - 2, 2 - 5, -1 - (-1)) = (-1, -3, 0) \\
&(1, 1, -2) = -((2, 5, -1) - 3(1, 2, -1)) = -(2 - 3, 5 - 6, -1 - (-3)) = -(-1, -1, 2) = (1, 1, -2)
\end{align}
$$
$$
\begin{align}
&(1, 2, -1) = \frac{1}{2}((1, 1, -2) - (-1, -3, 0)) = \frac{1}{2}(1 - (-1), 1 - (-3), -2 - 0) = \frac{1}{2}(2, 4, -2) = (1, 2, -1) \\
&(2, 5, -1) = \frac{1}{2}((1, 1, -2) - 3(-1, -3, 0)) = \frac{1}{2}(1 - (-3), 1 - (-9), -2 - 0) = \frac{1}{2}(4, 10, -2) = (2, 5, -1)
\end{align}
$$
Como vemos, se cumple que $\mathcal{A}_{2} \in [\mathcal{A}_{1}]$ y $\mathcal{A}_{1} \in [\mathcal{A}_{2}]$. Por lo tanto, $\mathcal{A}_{1}$ y $\mathcal{A}_{2}$ generan el mismo subespacio vectorial de $\mathbb{R}^{3}$: $[\mathcal{A}_{1}] = [\mathcal{A}_{2}]$.

---
# Conjuntos LI, conjuntos LD y conjuntos generadores
## Ejercicio 5
Básicamente, el ejercicio solicita determinar si los conjuntos presentados son linealmente independientes, y en caso de no serlo, determinar un subconjunto linealmente dependiente que permita expresar a los vectores de $\mathcal{A}$ como combinación lineal, o lo que es lo mismo, encontrar que vectores son los "sobrantes" (los que hacen que el conjunto no sea linealmente independiente), y quitarlos.

En cada caso, determinaremos si el conjunto es libre o no desarrollando un sistema homogeneo.
### Parte a)
$$
\mathcal{A} = \{ (1, 2, 3), (0, 1, 2), (1, 1, 1), (2, 3, 4) \}
$$
En este caso, simplemente con analizar los elementos, podemos ver que $(2, 3, 4)$ se puede formar mediante combinación lineal:
$$
(2, 3, 4) = (1, 2, 3) + (1, 1, 1) = (1 + 1, 2 + 1, 3 + 1) = (2, 3, 4)
$$
De esta forma, podemos excluirlo del conjunto:
$$
\mathcal{A} = \{ (1, 2, 3), (0, 1, 2), (1, 1, 1) \}
$$
También podemos estudiar $(1, 2, 3)$, el cual puede ser generado mediante combinación lineal:
$$
(1, 2, 3) = (0, 1, 2) + (1, 1, 1) = (0 + 1, 1 + 1, 2 + 1) = (1, 2, 3)
$$
En conclusión, nos quedamos con el siguiente conjunto, el cual es linealmente independiente:
$$
\mathcal{A} = \{ (0, 1, 2), (1, 1, 1) \}
$$

### Parte b)
$$
\mathcal{A} = \left\{
\begin{pmatrix}
4 & 0 \\
-2 & -2
\end{pmatrix}, \begin{pmatrix}
1 & -1 \\
2 & 3
\end{pmatrix}, \begin{pmatrix}
0 & 2 \\
1 & 4
\end{pmatrix}, \begin{pmatrix}
-1 & 5 \\
7 & 1
\end{pmatrix}
\right\}
$$
Aquí, desarrollaremos un sistema homogéneo:
$$
\begin{cases}
4\alpha + \beta - \mu = 0 \\
-\beta + 2\gamma + 5\mu = 0 \\
-2\alpha + 2\beta + \gamma + 7\mu = 0 \\
-2\alpha + 3\beta + 4\gamma + \mu = 0
\end{cases}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & -1 & 2 & 5 & 0 \\
-2 & 2 & 1 & 7 & 0 \\
-2 & 3 & 4 & 1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & -1 & 2 & 5 & 0 \\
-2 & 2 & 1 & 7 & 0 \\
0 & 1 & 3 & -6 & 0
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & -1 & 2 & 5 & 0 \\
0 & 5 & 2 & 13 & 0 \\
0 & 1 & 3 & -6 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow 2F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & -1 & 2 & 5 & 0 \\
0 & 6 & 0 & 8 & 0 \\
0 & 1 & 3 & -6 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & -1 & 2 & 5 & 0 \\
0 & 1 & 0 & \frac{8}{6} & 0 \\
0 & 1 & 3 & -6 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{6}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & 0 & 2 & \frac{38}{6} & 0 \\
0 & 1 & 0 & \frac{8}{6} & 0 \\
0 & 0 & 3 & -\frac{44}{6} & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{3} \\
&F_{4} \leftarrow F_{4} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & 0 & 1 & \frac{19}{6} & 0 \\
0 & 1 & 0 & \frac{8}{6} & 0 \\
0 & 0 & 1 & -\frac{22}{9} & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{2}F_{2} \\
&F_{4} \leftarrow \frac{1}{3}F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & 0 & 0 & \frac{101}{18} & 0 \\
0 & 1 & 0 & \frac{8}{6} & 0 \\
0 & 0 & 1 & -\frac{22}{9} & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & -1 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 1 & 0 & \frac{8}{6} & 0 \\
0 & 0 & 1 & -\frac{22}{9} & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{18}{101}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2} \\
&F_{3} \leftarrow F_{3} - \frac{8}{6}F_{2} \\
&F_{4} \leftarrow F_{4} + \frac{22}{9}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{4}F_{1}
\end{align}
$$
De esta forma, llegamos a la conclusión de que las ecuaciones se cumplen si y sólo si todos los parámetros son 0. Por lo tanto, el conjunto $\mathcal{A}$ es linealmente independiente.

### Parte c)
$$
\mathcal{A} = \{ p_{1}, p_{2}, p_{3}, p_{4} \} \subset \mathbb{R}_{2}[x] \text{, donde}
$$
$$
\begin{align}
&p_{1}(x) = x^{2} + 1 \\
&p_{2}(x) = x^{2} + x \\
&p_{3}(x) = x + 2 \\
&p_{4}(x) = x^{2} + 3x
\end{align}
$$
O sea:
$$
\mathcal{A} = \{ x^{2} + 1, x^{2} + x, x + 2, x^{2} + 3x \}
$$
$$
\begin{cases}
\alpha + \beta + \mu = 0 \\
\beta + \gamma + 3\mu = 0 \\
\alpha + 2\gamma = 0
\end{cases}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 1 & 0 & 1 & 0 \\
0 & 1 & 1 & 3 & 0 \\
1 & 0 & 2 & 0 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
1 & 1 & 0 & 1 & 0 \\
0 & 1 & 1 & 3 & 0 \\
0 & -1 & 2 & -1 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 1 & 0 & 1 & 0 \\
0 & 1 & 1 & 3 & 0 \\
0 & 0 & 3 & 2 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 1 & 0 & 1 & 0 \\
0 & 1 & 1 & 3 & 0 \\
0 & 0 & 1 & \frac{2}{3} & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{3}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 1 & 0 & 1 & 0 \\
0 & 1 & 0 & \frac{7}{3} & 0 \\
0 & 0 & 1 & \frac{2}{3} & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & -\frac{4}{3} & 0 \\
0 & 1 & 0 & \frac{7}{3} & 0 \\
0 & 0 & 1 & \frac{2}{3} & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
Como vemos, llegamos a una solución que no es única (puesto que depende de un parámetro). Por lo tanto, el sistema es linealmente dependiente. A continuación, analizamos que vector se puede formar como combinación lineal del resto:

Por como está estructurada la matriz, cada columna es uno de los vectores del conjunto $\mathcal{A}$: columna 1 comenzó siendo $p_{1}$, columna 2 $p_{2}$, columna 3 $p_{3}$ y columna 4 $p_{4}$. De esta forma, podemos ver que las primeras tres columnas forman la identidad, y la cuarta está formada por combinación de las anteriores.

Es en base a este razonamiento que podemos concluir que el polinomio $p_{4}$ es el elemento sobrante del conjunto. De esta forma, podemos excluirlo, quedándonos con el conjunto:
$$
\mathcal{A} = \{ x^{2} + 1, x^{2} + x, x + 2 \}
$$

---
## Ejercicio 6
### Parte a)
$$
\mathcal{A} = \{ (a, a^{2}, 1), (-1, a, a), (0, 2a^{2}, a^{2} + 1) \}
$$
Desarrollamos un sistema homogéneo considerando los vectores y sus componentes:
$$
\begin{cases}
a\alpha - \beta = 0 \\
a^{2}\alpha + a\beta + 2a^{2}\gamma = 0 \\
\alpha + a\beta + (\alpha^{2} + 1)\gamma = 0
\end{cases}
$$
De esta forma, trabajaremos con la siguiente matriz:
$$
\left(
\begin{array}{ccc|c}
a & -1 & 0 & 0 \\
a^{2} & a & 2a^{2} & 0 \\
1 & a & a^{2} + 1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
a & -1 & 0 & 0 \\
2a^{2} & 0 & 2a^{2} & 0 \\
a^{2} + 1 & 0 & a^{2} + 1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + aF_{1} \\
&F_{3} \leftarrow F_{3} + aF_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
a & -1 & 0 & 0 \\
-2 & 0 & -2 & 0 \\
a^{2} + 1 & 0 & a^{2} + 1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
a & -1 & 0 & 0 \\
1 & 0 & 1 & 0 \\
a^{2} + 1 & 0 & a^{2} + 1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -\frac{1}{2}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
a & -1 & 0 & 0 \\
1 & 0 & 1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - (a^{2} + 1)F_{2}
\end{align}
$$
Como vemos, anulamos una fila, por lo que el conjunto no es linealmente independiente.

Si analizamos como está estructurado, podemos ver que el vector $(0, 2a^{2}, a^{2} + 1)$ puede expresarse en base al resto:
$$
(0, 2a^{2}, a^{2} + 1) = (a, a^{2}, 1) + a(-1, a, a) = (a - a, a^{2} + a^{2}, 1 + a^{2}) = (0, 2a^{2}, a^{2} + 1)
$$
Por esta razón, lo podemos excluir:
$$
\mathcal{A} = \{ (a, a^{2}, 1), (-1, a, a) \}
$$
Ahora, obtuvimos un conjunto linealmente independiente, ya que no hay forma de pasar de un vector al otro multiplicando por un escalar.

ACLARACIÓN: Sabemos que alcanzamos la "mayor cantidad de elementos posible" para un conjunto LI cuando el numero de elementos del conjunto coincide con el rango de la matriz original (la que desarrollamos para determinar si es LI o LD).
Podemos identificar cuales vectores son combinación lineal de otros si observamos detenidamente la matriz escalerizada: las columnas que contiene "pivotes" (primer elemento no nulo de cada fila) son vectores originales, no son redundantes.

### Parte b)
$$
\mathcal{A} = \left\{ \begin{pmatrix}
1 & 0 \\
1 & a
\end{pmatrix}, \begin{pmatrix}
-1 & 0 \\
a & 1
\end{pmatrix}, \begin{pmatrix}
2 & 0 \\
1 & 3
\end{pmatrix} \right\}
$$
Desarrollamos el sistema homogéneo correspondiente:
$$
\begin{cases}
\alpha - \beta + 2\gamma = 0 \\
\alpha + a\beta + \gamma = 0 \\
a\alpha + \beta + 3\gamma = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 2 & 0 \\
1 & a & 1 & 0 \\
a & 1 & 3 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 2 & 0 \\
0 & a + 1 & -1 & 0 \\
0 & a + 1 & 3 - 2a & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} - aF_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 2 & 0 \\
0 & a + 1 & -1 & 0 \\
0 & 0 & 4 - 2a & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 2 & 0 \\
0 & a + 1 & -1 & 0 \\
0 & 0 & 2 - a & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{2}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & a & 1 & 0 \\
0 & a + 1 & -1 & 0 \\
0 & 0 & 2 - a & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2}
\end{align}
$$
Ahora, analicemos los posibles valores de $a$:

- $a = -1$
En este caso, la fila 2 y 3 comparten un único coeficiente no nulo, por lo que podemos anular una de ellas:
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 1 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + 3F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
En este caso, parece ser que el segundo vector es el que sobra:
$$
\begin{pmatrix}
-1 & 0 \\
-1 & 1
\end{pmatrix} = -\begin{pmatrix}
1 & 0 \\
1 & -1
\end{pmatrix}
$$

De esta forma, podríamos quitarlo:
$$
\mathcal{A} = \left\{ \begin{pmatrix}
1 & 0 \\
1 & -1
\end{pmatrix}, \begin{pmatrix}
2 & 0 \\
1 & 3
\end{pmatrix} \right\}
$$

- $a = 2$
En este caso, la fila 3 se anula:
$$
\left(
\begin{array}{ccc|c}
1 & 2 & 1 & 0 \\
0 & 3 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 2 & 1 & 0 \\
0 & 1 & -\frac{1}{3} & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{1}{3}F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & \frac{5}{3} & 0 \\
0 & 1 & -\frac{1}{3} & 0 \\
0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{2}
\end{align}
$$
En este caso, parece ser que el tercer vector es el que sobra:
$$
\begin{pmatrix}
2 & 0 \\
1 & 3
\end{pmatrix} = \frac{5}{3}\begin{pmatrix}
1 & 0 \\
1 & 2
\end{pmatrix} + \left( -\frac{1}{3}\begin{pmatrix}
-1 & 0 \\
2 & 1
\end{pmatrix} \right) = \begin{pmatrix}
\frac{5}{3} & 0 \\
\frac{5}{3} & \frac{10}{3}
\end{pmatrix} + \begin{pmatrix}
\frac{1}{3} & 0 \\
-\frac{2}{3} & -\frac{1}{3}
\end{pmatrix} = \begin{pmatrix}
\frac{5}{3} + \frac{1}{3} & 0 \\
\frac{5}{3} + \left( -\frac{2}{3} \right) & \frac{10}{3} + \left( -\frac{1}{3} \right)
\end{pmatrix} = \begin{pmatrix}
\frac{6}{3} & 0 \\
\frac{3}{3} & \frac{9}{3}
\end{pmatrix} = \begin{pmatrix}
2 & 0 \\
1 & 3
\end{pmatrix}
$$
De esta forma, podríamos quitarlo:
$$
\mathcal{A} = \left\{ \begin{pmatrix}
1 & 0 \\
1 & 2
\end{pmatrix}, \begin{pmatrix}
-1 & 0 \\
2 & 1
\end{pmatrix} \right\}
$$

- $a \not \in \{ -1, 2 \}$
En este caso, ninguna de las filas se anula, por lo que ningún vector es redundante. En conclusión, nos quedamos con los tres vectores:
$$
\mathcal{A} = \left\{ \begin{pmatrix}
1 & 0 \\
1 & a
\end{pmatrix}, \begin{pmatrix}
-1 & 0 \\
a & 1
\end{pmatrix}, \begin{pmatrix}
2 & 0 \\
1 & 3
\end{pmatrix} \right\}
$$
De esta manera, $\mathcal{A}$ es LD si $a \in \{ -1, 2 \}$, y LI en caso contrario.

---
## Ejercicio 7
Básicamente, tenemos que estudiar el sistema homogéneo de cada conjunto, y determinar si es linealmente independiente o no. En caso de no ser LI, tenemos que encontrar el o los vectores redundantes y removerlos del conjunto.

### Parte a)
$$
\mathcal{A} = \left\{ \begin{pmatrix}
1 & 0 \\
-1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
-1 & 2
\end{pmatrix}, \begin{pmatrix}
0 & -1 \\
0 & -1
\end{pmatrix}, \begin{pmatrix}
3 & -1 \\
-2 & 1
\end{pmatrix} \right\}
$$
$$
\begin{cases}
\alpha + 3\mu = 0 \\
\beta - \gamma - \mu = 0 \\
-\alpha - \beta - 2\mu = 0 \\
2\beta - \gamma + \mu = 0
\end{cases}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 3 & 0 \\
0 & 1 & -1 & -1 & 0 \\
-1 & -1 & 0 & -2 & 0 \\
0 & 2 & -1 & 1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 3 & 0 \\
0 & 1 & -1 & -1 & 0 \\
0 & -1 & 0 & 1 & 0 \\
0 & 2 & -1 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 3 & 0 \\
0 & 0 & -1 & 0 & 0 \\
0 & -1 & 0 & 1 & 0 \\
0 & 3 & -1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{3} \\
&F_{4} \leftarrow F_{4} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 3 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & -1 & 0 & 1 & 0 \\
0 & 3 & -1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 3 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & -1 & 0 & 1 & 0 \\
0 & 3 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} + F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 3 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & -1 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow \frac{1}{3}F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 3 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 3F_{3}
\end{align}
$$
Como vemos, llegamos a una matriz escalerizada reducida, por lo que el conjunto $\mathcal{A}$ es LI. No hay necesidad de remover ningún elemento, puesto que no hay vectores redundantes (que se puedan formar como combinación lineal del resto).

### Parte b)
$$
\mathcal{A} = \left\{ x^{2} - 1, x^{3} + 2x, x, x^{3} + x, 2x^{2} - 1 \right\}
$$
Simplemente con analizar el conjunto, podemos ver que el vector $x^{3} + 2x$ se puede formar mediante combinación lineal:
$$
x^{3} + 2x = x^{3} + x + x
$$
De esta forma, podemos removerlo:
$$
\mathcal{A} = \left\{ x^{2} - 1, x, x^{3} + x, 2x^{2} - 1 \right\}
$$
Ahora, estudiaremos el conjunto desarrollando un sistema homogéneo:
$$
\begin{cases}
\gamma = 0 \\
\alpha + 2\mu = 0 \\
\beta + \gamma = 0 \\
-\alpha - \mu = 0
\end{cases}
$$
$$
\gamma = 0 \implies \beta + \gamma = \beta = 0
$$
$$
\begin{cases}
\alpha + 2\mu = 0 \\
-\alpha - \mu = 0
\end{cases} \implies (\cancel{ \alpha } + \cancel{ 2 }\mu) + (\cancel{ -\alpha } - \cancel{ \mu }) = 0 \implies \mu = 0
$$
$$
\mu = 0 \implies \alpha + 2\mu = \alpha = 0
$$
En conclusión, determinamos que, para que el sistema se cumpla, solo existe una solución: $\alpha = \beta = \gamma = \mu = 0$. Por lo tanto, luego de remover el vector $x^{3} + 2x$, $\mathcal{A}$ es LI.

---
## Ejercicio 9
Dos partes.

### Parte c)
En los dos casos, estudiaremos la ecuación $\alpha f(x) + \beta g(x) + \gamma h(x) = 0$

En la primer imagen, podemos ver que $f(0) = g(0) = 0$, por lo que para que $\gamma h(x_{0}) = 0$, sabiendo que $h(x_{0}) \neq 0$, necesariamente $\gamma = 0$. Ahora, sabiendo que $\gamma = 0$, nos centraremos en las funciones $f(x)$ y $g(x)$: $\alpha f(x) + \beta g(x) = 0$. Nuevamente, analizamos la función en un punto en el que $g(x) = 0$.

Como es una función periódica, tiene infinitas raíces, por lo que consideraremos cualquiera de estas, denotada $x_{0}$. Tenemos que verificar $\alpha f(x_{0}) + \beta g(x_{0}) = 0$. Sabemos que $g(x_{0}) = 0$, entonces nos queda $\alpha f(x_{0})$, y como $x_{0} \neq 0$ y $f(x)$ solo tiene raíz en cero: $\alpha f(x_{0}) = 0 \implies \alpha = 0$.

En conclusión, nos queda $\beta g(x) = 0$. Pero como $g$ no es nula en todo su recorrido: $\beta = 0$.

De esta forma:
$$
\alpha f(x) + \beta g(x) + \gamma h(x) = 0 \Longleftrightarrow \alpha = \beta = \gamma = 0
$$
En conclusión, $\{ f, g, h \}$ es LI.

Por otra parte, en la segunda imagen, vemos que todos los puntos de las funciones $f$ y $g$ se encuentran a la misma distancia. Por esta razón, si realizamos la resta entre ambas funciones, $f(x) - g(x)$, obtendremos una función constante: $f(x) - g(x) = c, \forall x \in \mathbb{R}$.

Sin embargo, $h$ también es una función constante, por lo que existe algún $\gamma \neq 0$, tal que $\gamma h(x) = c$, lo que implica que:
$$
f(x) - g(x) - \gamma h(x) = 0 \qquad \forall x \in \mathbb{R}
$$
En conclusión, $\{ f, g, h \}$ es LD. También lo podemos ver de la siguiente forma:
$$
\begin{align}
&f(x) = g(x) - \gamma h(x) \\
&g(x) = f(x) + \gamma h(x) \\
&h(x) = \mu(f(x) - g(x))
\end{align}
$$

### Parte d)
1. Como se trata de dos rectas que tienen raíz en 0, necesariamente una es múltiplo de la otra, ya que ambas tienen la forma: $f(x) = mx$. Por esta razón, el conjunto es LD.

2. Ambas funciones son rectas constantes (pendiente 0), por lo tanto tienen la forma: $f(x) = a, a \in \mathbb{R}$. De esta forma, el conjunto es LD.

3. Aquí, tenemos dos rectas paralelas, por lo que ambas tienen la misma estructura: $f(x) = mx + a$ y $g(x) = mx + b$. Chequeamos si existen $\alpha, \beta \in \mathbb{R}, \alpha \neq 0 \land \beta \neq 0$ tal que $$
   \alpha f(x) = \alpha mx + \alpha a = \beta g(x) = \beta mx + \beta b \implies \alpha m = \beta m \land \alpha a = \beta b
   $$
   Si $\alpha m = \beta m \implies \alpha = \beta$. Sin embargo, $a \neq b$, entonces, si $\alpha = \beta$, $\alpha a \neq \beta b$.
   Es así que confirmamos que no existe $\alpha \neq 0 \land \beta \neq 0$ tal que $\alpha f(x) + \beta g(x) = 0$.
   Entonces, confirmamos que el conjunto es LI.

4. Aquí, las rectas tienen formas diferentes: $f(x) = mx$ y $g(x) = nx + a$. Buscamos los coeficientes $\alpha, \beta \in \mathbb{R}, \alpha \neq 0, \beta \neq 0$: $$
   \alpha f(x) + \beta g(x) = 0 \implies \alpha mx + \beta(nx + a) = 0
   $$
   Sin embargo, esto implica que $$
   \alpha mx + \beta nx + \beta a = 0 \implies \begin{cases}
   \alpha mx + \beta nx = 0 \\
   \beta a = 0
   \end{cases}
   $$
   Sabemos que $a \neq 0$, entonces $\beta = 0$, lo que implica que $\alpha mx = 0$. Como $m \neq 0$, entonces $\alpha = 0$. En conclusión: $$
   \alpha f(x) + \beta g(x) = 0 \Longleftrightarrow \alpha = \beta = \gamma = 0
   $$
   Entonces, $\{ f, g \}$ es un conjunto LI.

5. Ambas funciones tienen la misma forma: $f(x) = x^{m} + a$ y $g(x) = x^{n} + b$. Tenemos que encontrar $\alpha, \beta \in \mathbb{R}, \alpha \neq 0, \beta \neq 0$: $$
   \alpha f(x) + \beta g(x) = 0 \implies \alpha(x^{m} + a) + \beta(x^{n} + b) = 0
   $$
   Sin embargo, esto implica que $$
   \alpha x^{m} + \alpha a + \beta x^{n} + \beta b = 0 \implies \begin{cases}
   \alpha x^{m} + \beta x^{n} = 0 \\
   \alpha a + \beta b = 0
   \end{cases}
   $$
   Sin embargo, sabemos que $a \neq 0$ y $b \neq 0$, por lo que $\alpha a \neq 0$ y $\beta b \neq 0$, del mismo modo $\alpha x^{m} \neq 0$ y $\beta x^{n} \neq 0$. Por lo tanto:
   $$
   \begin{cases}
   \alpha x^{m} + \beta x^{n} = 0 \implies \alpha x^{m} = -\beta x^{n} \implies x^{m} = -\frac{\beta}{\alpha} x^{n} \\
   \alpha a + \beta b = 0 \implies \alpha a = -\beta b \implies a = -\frac{\beta}{\alpha} b
   \end{cases}
   $$
   Como vemos, $f(x) = x^{m} + a = -\frac{\beta}{\alpha} (x^{n} + b)$.
   De esta forma, como los coeficientes no son nulos, podemos utilizarlos para expresar $f(x)$ en base a $g(x)$ y viceversa.
   
   En conclusión, $\{ f, g \}$ es un conjunto LD.

6. Si analizamos la función, podemos ver que $f$ y $g$ tienen la misma forma, pero se diferencian por una constante: $f(x) = x^{m}$ y $g(x) = x^{m} + a$. De esta forma, si desarrollamos $g(x) - f(x) = \cancel{ x^{m} } + a - \cancel{ x^{m} } = a$, simplemente nos quedamos con una función constante $i(x) = a$. En el conjunto, también existe una función $h(x) = c$, por lo tanto, al tener dos funciones constantes no nulas, podemos encontrar un parámetro $\alpha$ tal que $\alpha a = c$. De esta forma, habríamos formado la función $h$ mediante combinación lineal.
   
   En conclusión, $\{ f, g, h \}$ es un conjunto LD.

7. Tenemos un caso similar al anterior. Sin embargo, la función $h(x)$ ya no es una simple constante, sino que tiene la forma $h(x) = mx + c$. Por esta razón, ya no podemos formarla por combinación lineal de $f(x)$ y $g(x)$.
   
   En conclusión, $\{ f, g, h \}$ es un conjunto LI.

---
## Ejercicio 11

### Parte a)
Sea $\mathcal{A} \subset V$ un conjunto LI y $v \in V$, entonces $C = \mathcal{A} \cup \{ v \}$ es LI si y sólo si $v \not \in [\mathcal{A}]$.

Comencemos por la implicación directa:
$(\implies)$ Supongamos que $\mathcal{A} \cup \{ v \}$ es LI y tenemos que demostrar que $v \not \in [\mathcal{A}]$. Esto quiere decir que $v$ no se puede formar por combinación lineal considerando los vectores de $\mathcal{A}$, o dicho de otra forma, no existen escalares $\alpha_{1}, \dots, \alpha_{n} \in \mathbb{K}$ tal que
$$
v = \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n}
$$
con $v_{1}, \dots, v_{n} \in \mathcal{A}$.

Como $A \cup \{ v \}$ es LI, entonces $v \neq \vec{0}$ (ya que la única forma de que la combinación de los vectores de $\mathcal{A}$ sea 0 es que todos los coeficientes sean nulos).
Si $v = \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n}$ y $v \neq \vec{0}$, entonces alguno de los coeficientes $\alpha_{i}$ no es nulo.
$$
v = \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n} \implies \vec{0} = \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n} - v
$$
Esto es absurdo, ya que estaríamos determinando el vector nulo mediante una combinación lineal no trivial. Por lo tanto, por absurdo, determinamos que si $\mathcal{A} \cup \{ v \}$ es LI, entonces $v \not \in [A]$.

Ahora, comprobamos el recíproco (el razonamiento será exactamente el mismo):
$(\impliedby)$ Supongamos que $v \not \in [\mathcal{A}]$ y tenemos que demostrar que $\mathcal{A} \cup \{ v \}$ es LI. De esta forma, como $v$ no forma parte del espacio generado por $\mathcal{A}$, no se puede formar por combinación lineal considerando los vectores de $\mathcal{A}$. Entonces, no existen escalares $\alpha_{1}, \dots, \alpha_{n} \in \mathbb{K}$ tal que
$$
v = \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n}
$$
con $v_{1}, \dots, v_{n} \in \mathcal{A}$.

De esta forma, es posible introducir el vector $v$ al conjunto mencionado, manteniendo su calidad de conjunto linealmente independiente, ya que el nuevo vector no se puede expresar por combinación del resto. En conclusión, determinamos que si $v \not \in [A]$, entonces $\mathcal{A} \cup \{ v \}$ es LI.

Formalmente, se prueba de la siguiente forma:
Para probar que $\mathcal{A} \cup \{ v \}$ es LI, planteamos:
$$
\lambda v + \sum \alpha_{i} v_{i} = 0
$$
Si $\lambda \neq 0$, podríamos despejar:
$$
\begin{align}
\lambda v + \sum \alpha_{i} v_{i} &= 0 \\
-\lambda v &= \sum \alpha_{i} v_{i} \\
v &= \sum \left( \frac{\alpha_{i}}{-\lambda} \right) v_{i}
\end{align}
$$
Sin embargo, estaríamos expresando $v$ como combinación lineal de los vectores de $\mathcal{A}$, entonces $v \in [\mathcal{A}]$, lo que contradice la hipótesis.

De esta manera, $\lambda = 0$, lo que simplifica la ecuación:
$$
\sum \alpha_{i} v_{i} = 0
$$
Como $\mathcal{A}$ es LI por hipótesis, entonces todos los coeficientes $\alpha_{i}$ son nulos.

Al ser todos nulos, el conjunto $A \cup \{ v \}$ es LI.

### Parte b)
Comenzamos demostrando la implicación directa:
$(\implies)$ Sea $\{ u, v, w \}$ un subconjunto LI de $V$. Sabemos que un conjunto es LI si ninguno de sus vectores puede ser formado por combinación lineal del resto. Sin embargo, es válido sustituir vectores por una combinación lineal que los incluya. Por ejemplo, podemos sustituir $w$ por una combinación lineal que también incluya a $w$:
$$
\{ u, v, w \} \text{ es LI } \implies \{ u, v, w - v + u \} \text{ es LI }
$$
Además, podemos desarrollar este proceso las veces que queramos y con los vectores deseados:
$$
\{ u, v, w - v + u \} \text{ es LI } \implies \{ u + v, v, w - v + u \} \text{ es LI }
$$
De esta forma, por transitividad se cumple que $\{ u, v, w \} \text{ es LI } \implies \{ u + v, v, w - v + u \} \text{ es LI }$.

Ahora, comprobamos el recíproco (el razonamiento será exactamente el mismo):
$(\impliedby)$ Sea $\{ u + v, v, w - v + u \}$ un subconjunto LI de $V$. Sabemos que un conjunto es LI si ninguno de sus vectores puede ser formado por combinación lineal del resto. Sin embargo, es válido sustituir vectores por una combinación lineal que los incluya. Por ejemplo, podemos sustituir $u + v$ por una combinación lineal que también incluya a $u$ o $v$ (la cual ya no exista directa o indirectamente (mediante un múltiplo) en el conjunto):
$$
\{ u + v, v, w - v + u \} \text{ es LI } \implies \{ u, v, w - v + u \} \text{ es LI }
$$
Además, podemos desarrollar este proceso las veces que queramos y con los vectores deseados:
$$
\{ u, v, w - v + u \} \text{ es LI } \implies \{ u, v, w \} \text{ es LI }
$$
De esta forma, por transitividad se cumple que $\{ u + v, v, w - v + u \} \text{ es LI } \implies \{ u, v, w \} \text{ es LI }$.

ACLARACIÓN: En realidad, la demostración se realiza de la siguiente forma:

Comenzamos demostrando la implicación directa:
$(\implies)$ Sea $\{ u, v, w \}$ un subconjunto LI de $V$.

Queremos demostrar que $\{ u + v, v, w - v + u \}$ es LI. Para esto, desarrollamos la ecuación de independencia:
$$
\begin{align}
\alpha (u + v) + \beta v + \gamma (w - v + u) &= \vec{0} \\
\alpha u + \alpha v + \beta v + \gamma w - \gamma v + \gamma u &= \vec{0} \\
u(\alpha + \gamma) + v(\alpha + \beta - \gamma) + w(\gamma) &= \vec{0}
\end{align}
$$
Como $\{ u, v, w \}$ es LI, entonces los coeficientes de esta nueva combinación deben ser todos nulos:
$$
\begin{cases}
\alpha + \gamma = 0 \\
\alpha + \beta - \gamma = 0 \\
\gamma = 0
\end{cases}
$$
Ahora, determinamos que como $\gamma = 0 \implies \alpha + \gamma = \alpha = 0$. Finalmente $\alpha + \beta - \gamma = \beta = 0$.
En conclusión, demostramos que la ecuación solo se cumple cuando todos los coeficientes son 0, por lo que, efectivamente, $\{ u + v, v, w - v + u \}$ es LI.

Ahora, comprobamos el recíproco (el razonamiento será exactamente el mismo):
$(\impliedby)$ Sea $\{ u + v, v, w - v + u \}$ un subconjunto LI de $V$.

Queremos demostrar que $\{ u, v, w \}$ es LI. Para esto, desarrollamos la ecuación de independencia:
$$
\alpha u + \beta v + \gamma w = \vec{0}
$$
Queremos demostrar que la única solución posible es $\alpha = \beta = \gamma = 0$.

Denominemos a los vectores del conjunto LI de la hipótesis:
$$
\begin{cases}
x = u + v \\
y = v \\
z = w - v + u
\end{cases}
$$
Ahora, despejamos cada uno de los vectores $u, v, w$ en función de $x, y, z$:
$$
\begin{cases}
v = y \\
u = x - v \implies u = x - y \\
w = z + v - u \implies w = z + y - (x - y) = z + y - x + y = z + 2y - x
\end{cases}
$$
Sustituimos estos vectores en el sistema original:
$$
\begin{align}
\alpha (x - y) + \beta y + \gamma (z + 2y - x) &= \vec{0} \\
\alpha x - \alpha y + \beta y + \gamma z + \gamma 2y - \gamma x &= \vec{0} \\
x (\alpha - \gamma) + y (-\alpha + \beta + 2\gamma) + \gamma z &= \vec{0}
\end{align}
$$
Como sabemos que el conjunto $\{ x, y, z \}$ es LI (por hipótesis), la única forma de que la ecuación anterior se cumpla es que todos los coeficientes sean 0:
$$
\begin{cases}
\alpha - \gamma = 0 \\
-\alpha + \beta + 2\gamma = 0 \\
\gamma = 0
\end{cases}
$$
Tenemos que $\gamma = 0$, entonces $\alpha - \gamma = \alpha = 0$. Ahora, podemos determinar $\beta$: $-\alpha + \beta + 2\gamma = \beta = 0$.

En conclusión, demostramos lo que buscábamos: la única solución posible es $\alpha = \beta = \gamma = 0$. Entonces, el conjunto $\{ u, v, w \}$ es LI.



Ahora, determinamos que como $\gamma = 0 \implies \alpha + \gamma = \alpha = 0$. Finalmente $\alpha + \beta - \gamma = \beta = 0$.
En conclusión, demostramos que la ecuación solo se cumple cuando todos los coeficientes son 0, por lo que, efectivamente, $\{ u + v, v, w - v + u \}$ es LI.


---
## Ejercicio 12
### Parte a)
$\mathcal{C}$ es LI, entonces 
$$
\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} = \vec{0} \Longleftrightarrow \alpha_{1} = \alpha_{2} = \dots = \alpha_{l} = 0
$$
Ahora, consideramos la definición de $\mathcal{B}$:
$$
\mathcal{B} = \{ Av_{1}, Av_{2}, \dots, Av_{l} \} \subset \mathbb{R}^{m}
$$
Tenemos que demostrar que $\mathcal{B}$ es LI, lo que significa que:
$$
\alpha_{1} \cdot Av_{1} + \alpha_{2} \cdot Av_{2} + \dots + \alpha_{l} \cdot Av_{l} = \vec{0} \Longleftrightarrow \alpha_{1} = \alpha_{2} = \dots = \alpha_{l} = 0
$$

Desarrollemos la idea:
Sabemos que
$$
\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} = \vec{0} \Longleftrightarrow \alpha_{1} = \alpha_{2} = \dots = \alpha_{l} = 0
$$
Ahora, si estudiamos la igualdad de $\mathcal{B}$, y consideramos la distributividad del producto de matrices, podemos expresarlo de la siguiente forma:
$$
\begin{align}
\alpha_{1} \cdot Av_{1} + \alpha_{2} \cdot Av_{2} + \dots + \alpha_{l} \cdot Av_{l} &= \vec{0} \\
A(\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l}) &= \vec{0}
\end{align}
$$
Ahora, sabiendo que dentro de los paréntesis tenemos una combinación lineal del conjunto $\mathcal{C}$, en base a la hipótesis de que $\mathcal{C}$ es LI, podemos determinar que la igualdad solo se cumple si todos los coeficientes son nulos. Podemos quedarnos con esto si consideramos que, como $A$ es invertible, entonces el sistema $AX = 0$ tiene como única solución la trivial ($X = 0$), por lo que:
$$
\begin{align}
A(\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l}) &= \vec{0} \\
A^{-1}A(\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l}) &= A^{-1} \cdot \vec{0} \\
\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} &= \vec{0}
\end{align}
$$
De esta manera:
$$
\begin{align}
\alpha_{1} \cdot Av_{1} + \alpha_{2} \cdot Av_{2} + \dots + \alpha_{l} \cdot Av_{l} &= \vec{0} \\
A(\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l}) &= \vec{0}
\end{align} \Longleftrightarrow \alpha_{1} = \alpha_{2} = \dots = \alpha_{l} = 0
$$

En conclusión, $\mathcal{B}$ también es LI.

### Parte b)
$\mathcal{B}$ es LI, entonces 
$$
\alpha_{1} \cdot Av_{1} + \alpha_{2} \cdot Av_{2} + \dots + \alpha_{l} \cdot Av_{l} = \vec{0} \Longleftrightarrow \alpha_{1} = \alpha_{2} = \dots = \alpha_{l} = 0
$$
Ahora, consideramos la definición de $\mathcal{C}$:
$$
\mathcal{C} = \{ v_{1}, v_{2}, \dots, v_{l} \} \subset \mathbb{R}^{n}
$$
Si estudiamos la igualdad de $\mathcal{B}$, podemos ver que todos los términos son multiplicados por $A$, por lo que podemos sacar el factor común:
$$
\alpha_{1} \cdot Av_{1} + \alpha_{2} \cdot Av_{2} + \dots + \alpha_{l} \cdot Av_{l} = \vec{0} \implies A(\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l}) = \vec{0}
$$
Sabemos que $A$ es invertible, por lo que no es nula. Además, existe $A^{-1}$ tal que $A A^{-1} = I$. Por lo tanto:
$$
\begin{align}
&A(\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l}) = \vec{0} \\
&A^{-1}A(\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l}) = A^{-1} \cdot \vec{0} \\
&\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} = \vec{0}
\end{align}
$$
Como vemos, partimos de una igualdad referente al conjunto $\mathcal{B}$, y luego de algunas manipulaciones algebraicas, llegamos a otra que refiere al conjunto $\mathcal{C}$, demostrando que, con los mismos coeficientes, la igualdad se mantiene.
De esta manera, $\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} = \vec{0} \Longleftrightarrow \alpha_{1} = \alpha_{2} = \dots = \alpha_{l} = 0$, probando que $\mathcal{C}$ es LI.

### Parte c)
$\mathcal{C}$ es LD, entonces 
$$
\alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} = \vec{0} \text{ sin que necesariamente se cumpla que } \alpha_{1} = \alpha_{2} = \dots = \alpha_{l} = 0
$$
De esta manera, existe al menos un vector en el conjunto que se escribe como combinación lineal del resto, por lo que existe al menos un escalar $\alpha_{i} \neq 0$.

Puede ser cualquier vector $v_{i}$ el que es redundante (o incluso puede ser más de uno). Para simplificar, consideremos al vector $v_{1}$ (existiendo la posibilidad de reordenar los términos). Entonces, $v_{1}$ se puede expresar en base al resto de vectores:
$$
\begin{align}
\vec{0} &= \alpha_{1} \cdot v_{1} + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} \\
-\alpha_{1} \cdot v_{1} &= \alpha_{2} \cdot v_{2} + \alpha_{3} \cdot v_{3} + \dots + \alpha_{l} \cdot v_{l} \\
v_{1} &= -\frac{\alpha_{2}}{\alpha_{1}} \cdot v_{2} - \frac{\alpha_{3}}{\alpha_{1}} \cdot v_{3} - \dots - \frac{\alpha_{l}}{\alpha_{1}} \cdot v_{l}
\end{align}
$$
Es válido pasar su coeficiente $\alpha_{1}$ dividiendo, ya que sabemos que no es nulo.

Ahora, consideramos la definición de $\mathcal{B}$:
$$
\mathcal{B} = \{ Av_{1}, Av_{2}, \dots, Av_{l} \} \subset \mathbb{R}^{m}
$$
Como vimos, el vector $v_{1}$ puede expresarse como combinación lineal del resto:
$$
\begin{align}
\vec{0} &= \alpha_{1} \cdot Av_{1} + \alpha_{2} \cdot Av_{2} + \dots + \alpha_{l} \cdot Av_{l} \\
\vec{0} &= \alpha_{1} \cdot A\left( -\frac{\alpha_{2}}{\alpha_{1}} \cdot v_{2} - \frac{\alpha_{3}}{\alpha_{1}} \cdot v_{3} - \dots - \frac{\alpha_{l}}{\alpha_{1}} \cdot v_{l} \right) + \alpha_{2} \cdot Av_{2} + \dots + \alpha_{l} \cdot Av_{l} \\
\vec{0} &= A\left( \alpha_{1} \cdot \left( -\frac{\alpha_{2}}{\alpha_{1}} \cdot v_{2} - \frac{\alpha_{3}}{\alpha_{1}} \cdot v_{3} - \dots - \frac{\alpha_{l}}{\alpha_{1}} \cdot v_{l} \right) + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} \right) \\
A^{-1} \cdot \vec{0} &= A^{-1}A\left( \alpha_{1} \cdot \left( -\frac{\alpha_{2}}{\alpha_{1}} \cdot v_{2} - \frac{\alpha_{3}}{\alpha_{1}} \cdot v_{3} - \dots - \frac{\alpha_{l}}{\alpha_{1}} \cdot v_{l} \right) + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} \right) \\
\vec{0} &= \alpha_{1} \cdot \left( -\frac{\alpha_{2}}{\alpha_{1}} \cdot v_{2} - \frac{\alpha_{3}}{\alpha_{1}} \cdot v_{3} - \dots - \frac{\alpha_{l}}{\alpha_{1}} \cdot v_{l} \right) + \alpha_{2} \cdot v_{2} + \dots + \alpha_{l} \cdot v_{l} \\
\vec{0} &= \left( \cancel{ -\alpha_{2} \cdot v_{2} } - \cancel{ \alpha_{3} \cdot v_{3} } - \cancel{ \dots } - \cancel{ \alpha_{l} \cdot v_{l} } \right) + \cancel{ \alpha_{2} \cdot v_{2} } + \cancel{ \dots } + \cancel{ \alpha_{l} \cdot v_{l} } \\
\vec{0} &= \vec{0}
\end{align}
$$
Como vemos, logramos anular la expresión, sabiendo que no todos los coeficientes eran nulos (puesto que expresamos a $v_{1}$ como combinación lineal del resto). En conclusión, si $\mathcal{C}$ es LD, entonces $\mathcal{B}$ también es LD.

CORRECCIÓN: En realidad, se demuestra de la siguiente mantera:

Para probar que $\mathcal{B}$ es LD, tenemos que encontrar escalares no todos nulos que anulen su combinación lineal.

Partimos sabiendo que $\mathcal{C}$ es LD, entonces existen escalares $\alpha_{1}, \dots, \alpha_{l}$ no todos nulos tales que:
$$
a_{1} \cdot v_{1} + a_{2} \cdot v_{2} + \dots + a_{l} \cdot v_{l} = \vec{0}
$$
Ahora, multiplicamos a ambos lados de la igualdad por la matriz $A$, y aplicamos distributiva (por linealidad):
$$
\begin{align}
A(a_{1} \cdot v_{1} + a_{2} \cdot v_{2} + \dots + a_{l} \cdot v_{l}) &= A \cdot \vec{0} \\
a_{1} \cdot Av_{1} + a_{2} \cdot Av_{2} + \dots + a_{l} \cdot Av_{l} &= \vec{0}
\end{align}
$$
En conclusión, como los escalares $\alpha_{i}$ son los mismos que en el paso inicial (y sabemos que no son todos nulos), esta última ecuación prueba que el conjunto $\mathcal{B} = \{ Av_{1}, \dots, Av_{l} \}$ es LD.

---
## Ejercicio 13
En todas las partes, trabajaremos con el vector $v$ definido por:
$$
v = \sum_{i = 1}^{n} a_{i} v_{i}
$$
con $a_{1}, a_{2}, \dots, a_{n} \in \mathbb{K}$.

### Parte a)
Tenemos que probar que
$$
\sum_{i = 1}^{n} \lambda_{i} = 0
$$
asumiendo que
$$
\sum_{i = 1}^{n} a_{i} \neq 1
$$
y
$$
\sum_{i = 1}^{n} \lambda_{i} (v_{i} - v) = 0
$$

Comenzaremos considerando esto último:
$$
\begin{align}
\sum_{i = 1}^{n} \lambda_{i} (v_{i} - v) &= \vec{0} \\
\sum_{i = 1}^{n} \lambda_{i} v_{i} - \sum_{i = 1}^{n} \lambda_{i} v &= \vec{0} \\
\sum_{i = 1}^{n} \lambda_{i} v_{i} - \sum_{i = 1}^{n} \left( \lambda_{i} \sum_{j = 1}^{n} a_{j} v_{j} \right) &= \vec{0} \\
\end{align}
$$
Ahora, para entender como proseguir, veamos un ejemplo con $n = 2$:
$$
\begin{align}
\sum_{i = 1}^{2} \lambda_{i} v_{i} - \sum_{i = 1}^{2} \left( \lambda_{i} \sum_{j = 1}^{2} a_{j} v_{j} \right) &= \vec{0} \\
(\lambda_{1} v_{1} + \lambda_{2} v_{2}) - [(\lambda_{1} + \lambda_{2})a_{1}v_{1} + (\lambda_{1} + \lambda_{2})a_{2}v_{2}] &= \vec{0} \\
\lambda_{1} v_{1} + \lambda_{2} v_{2} - (\lambda_{1} + \lambda_{2})a_{1}v_{1} - (\lambda_{1} + \lambda_{2})a_{2}v_{2} &= \vec{0} \\
(\lambda_{1} - (\lambda_{1} + \lambda_{2})a_{1})v_{1} + (\lambda_{2} - (\lambda_{1} + \lambda_{2})a_{2})v_{2} &= \vec{0}
\end{align}
$$
Entendiendo un poco más como se distribuyen los términos, podemos definir la siguiente sumatoria:
$$
\sum_{i = 1}^{n} \left[ \lambda_{i} - \left( \sum_{j = 1}^{n} \lambda_{j} \right)a_{i} \right] v_{i} = \vec{0}
$$
Como el conjunto $\{ v_{1}, v_{2}, \dots, v_{n} \}$ es LI, consideremos a la expresión anterior como la sumatoria de dichos elementos, la cual está igualada al vector nulo. Esta igualdad solo se verifica si todos los coeficientes son nulos. Por lo tanto, podemos definir la siguiente igualdad:
$$
\begin{align}
\sum_{i = 1}^{n} \left[ \lambda_{i} - \left( \sum_{j = 1}^{n} \lambda_{j} \right)a_{i} \right] &= 0 \\
\sum_{i = 1}^{n} \lambda_{i} - \sum_{i = 1}^{n} \left( a_{i} \sum_{j = 1}^{n} \lambda_{j} \right) &= 0 \\
\sum_{i = 1}^{n} \lambda_{i} &= \sum_{i = 1}^{n} \left( a_{i} \sum_{j = 1}^{n} \lambda_{j} \right)
\end{align}
$$
Sabiendo que $\sum_{i = 1}^{n} a_{i} \neq 1$, la expresión anterior significa que:
$$
\sum_{i = 1}^{n} \lambda_{i} = a \sum_{i = 1}^{n} \lambda_{j} \qquad \text{ con } a \neq 1
$$
Si lo estudiamos con variables en lugar de sumatorias para que sea más visible:
$$
u = a \cdot u \qquad \text{ con } a \neq 1
$$
El único valor $u = \sum_{i = 1}^{n} \lambda_{i}$ que cumple con dicha condición es 0. En conclusión:
$$
\sum_{i = 1}^{n} \lambda_{i} = 0
$$

### Parte b)
Tenemos que probar que
$$
\{ (v_{1} - v), (v_{2} - v), \dots, (v_{n} - v) \} \text{ es LI}
$$
asumiendo que
$$
\sum_{i = 1}^{n} a_{i} \neq 1
$$
Vamos a considerar lo que probamos anteriormente:
$$
\sum_{i = 1}^{n} \lambda_{i} = 0
$$
Sabemos que $\{ v_{1}, v_{2}, \dots, v_{n} \}$ es LI, entonces
$$
\alpha_{1} v_{1} + \alpha_{2} v_{2} + \dots + \alpha_{n} v_{n} = \vec{0} \Longleftrightarrow \alpha_{1} = \alpha_{2} = \dots = \alpha_{n} = 0
$$
Además, sabemos que
$$
v = \sum_{i = 1}^{n} a_{i} v_{i} = a_{1} v_{1} + a_{2} v_{2} + \dots + a_{n} v_{n}
$$
Para probar que un conjunto es LI, primero suponemos que existe una combinación lineal de esos vectores que da el vector nulo. De esta forma, comenzamos con una expresión genérica:
$$
\sum_{i = 1}^{n} \lambda_{i} (v_{i} - v) = 0
$$
Ahora, considerando lo demostrado en la parte anterior, como asumimos que $\sum_{i = 1}^{n} a_{i} \neq 1$, sabemos que si la sumatoria es 0, entonces necesariamente la suma de los escalares debe ser nula: $\sum_{i = 1}^{n} \lambda_{i} = 0$.

A continuación, desarrollamos la demostración:
$$
\begin{align}
\sum_{i = 1}^{n} \lambda_{i} (v_{i} - v) &= 0 \\
\sum_{i = 1}^{n} \lambda_{i} v_{i} - \left( \sum_{i = 1}^{n} \lambda_{i} \right) v &= 0
\end{align}
$$
Como $\sum_{i = 1}^{n} \lambda_{i} = 0$, entonces el segundo término se anula:
$$
\begin{align}
\sum_{i = 1}^{n} \lambda_{i} v_{i} &= 0
\end{align}
$$

Con esto concluimos la demostración: por la hipótesis, el conjunto original $\{ v_{1}, v_{2}, \dots, v_{n} \}$ es LI, por lo que la única forma de que esta sumatoria sea cero es que todos los $\lambda_{i} = 0$, entonces, el conjunto $\{ v_{1} - v, v_{2} - v, \dots, v_{n} - v \}$ también es LI.

### Parte c)
El desarrollo lógico de esta parte está íntimamente relacionado al de la parte a.

Partimos de la igualdad anterior:
$$
\sum_{i = 1}^{n} \lambda_{i} (v_{i} - v) = 0
$$
Desarrollamos la igualdad:
$$
\begin{align}
\sum_{i = 1}^{n} \lambda_{i} v_{i} - \left( \sum_{i = 1}^{n} \lambda_{i} \right) v &= 0 \\
\sum_{i = 1}^{n} \lambda_{i} v_{i} - \sum_{i = 1}^{n} \left( \lambda_{i} \sum_{j = 1}^{n} a_{j}v_{j} \right) &= 0 \\
\sum_{i = 1}^{n} \left[ \lambda_{i} - \left( \sum_{j = 1}^{n} \lambda_{j} \right) a_{i} \right]v_{i} &= 0
\end{align}
$$
Nos enforcamos en los coeficientes de los vectores que conforman la combinación lineal, para asegurar que no son todos nulos:
$$
\begin{align}
\sum_{i = 1}^{n} \left[ \lambda_{i} - \left( \sum_{j = 1}^{n} \lambda_{j} \right) a_{i} \right] &= 0 \\
\sum_{i = 1}^{n} \lambda_{i} - \sum_{i = 1}^{n} \left( a_{i} \sum_{j = 1}^{n} \lambda_{j} \right) &= 0 \\
\sum_{i = 1}^{n} \lambda_{i} &= \sum_{i = 1}^{n} \left( a_{i} \sum_{j = 1}^{n} \lambda_{j} \right)
\end{align}
$$
Ahora, consideramos $\sum_{i = 1}^{n} a_{i} = 1$, por lo que
$$
\sum_{i = 1}^{n} \lambda_{i} = \sum_{j = 1}^{n} \lambda_{j}
$$
Como vemos, llegamos a una igualdad que parece correcta. El problema es que si la interpretamos correctamente, la misma indica que no importa el valor de $\sum_{i = 1}^{n} \lambda_{i}$, o mejor dicho, el mismo no está limitado a ser 0 como si lo estaba cuando considerábamos $\sum_{i = 1}^{n} a_{i} \neq 1$.

En conclusión, si $\sum_{i = 1}^{n} a_{i} = 1$, entonces el conjunto $\{ v_{1} - v, v_{2} - v, \dots, v_{n} - v \}$ es LD.

---
## Ejercicio 14
Lo que haremos será definir la combinación lineal de las funciones y determinar el valor de las funciones en un punto, y en base a eso, establecer un valor para los coeficientes. No tenemos porque hacerlo para todas las funciones a la vez. Por ejemplo, si dos son 0 en un punto dado, y otra no es 0, entonces el coeficiente de la otra será 0, y luego analizamos puntualmente las funciones que van quedando.

### Parte a)
$$
\{ \sin(x), e^{x}, x^{2} \}
$$
Estudiamos la igualdad:
$$
\alpha \sin(x) + \beta e^{x} + \gamma x^{2} = 0
$$
Establecemos $x = 0$:
$$
\begin{align}
\alpha \sin(0) + \beta e^{0} + \gamma \cdot 0^{2} &= 0 \\
\cancel{ \alpha \cdot 0 } + \beta \cdot 1 + \cancel{ \gamma \cdot 0 } &= 0 \\
\beta = 0
\end{align}
$$
Ya encontramos el valor de $\beta$. Ahora, proseguimos a estudiar únicamente $\alpha$ y $\gamma$. En este caso, consideraremos $x = \pi$:
$$
\begin{align}
\alpha \sin(\pi) + \gamma \cdot \pi^{2} &= 0 \\
\cancel{ \alpha \cdot 0 } + \gamma \cdot \pi^{2} &= 0 \\
\gamma \cdot \pi^{2} = 0 \\
\gamma = 0
\end{align}
$$
Ahora, estudiamos la ecuación completa nuevamente conociendo $\beta$ y $\gamma$:
$$
\begin{align}
\alpha \sin(x) + 0 \cdot e^{x} + 0 \cdot x^{2} = 0 \\
\alpha \sin(x) = 0
\end{align}
$$
Como $\sin(x)$ no es nula $\forall x \in \mathbb{R}^{+}$, el único valor de $\alpha$ que asegura que la igualdad sea verdadera es 0.

En conclusión:
$$
\alpha \sin(x) + \beta e^{x} + \gamma x^{2} = 0 \Longleftrightarrow \alpha = \beta = \gamma = 0
$$

### Parte b)
$$
\{ \cos(x), \cos(x + 1), \cos(x + 2) \}
$$
Estudiamos la igualdad:
$$
\alpha \cos(x) + \beta \cos(x + 1) + \gamma \cos(x + 2) = 0
$$
Nuevamente, consideramos $x = -1$:
$$
\alpha \cos(-1) + \beta \cos(0) + \gamma \cos(1) = 0
$$
Como $\cos(x)$ es una función par, $\cos(-x) = \cos(x)$. Entonces:
$$
(\alpha + \gamma) \cos(1) + \beta = 0
$$
Además, consideramos $x = \frac{\pi}{2} - 1$:
$$
\alpha \cos\left( \frac{\pi}{2} - 1 \right) + \cancel{ \beta \cos\left( \frac{\pi}{2} \right) } + \gamma \cos\left( \frac{\pi}{2} + 1 \right) = 0 
$$
Sabemos que $\cos\left( \frac{\pi}{2} - 1 \right) = -\cos\left( \frac{\pi}{2} + 1 \right)$:
$$
\begin{align}
\alpha \cos\left( \frac{\pi}{2} - 1 \right) + \gamma \cos\left( \frac{\pi}{2} + 1 \right) &= 0 \\
\alpha \cos\left( \frac{\pi}{2} - 1 \right) - \gamma \cos\left( \frac{\pi}{2} - 1 \right) &= 0 \\
\alpha \cancel{ \cos\left( \frac{\pi}{2} - 1 \right) } &= \gamma \cancel{ \cos\left( \frac{\pi}{2} - 1 \right) } \\
\alpha &= \gamma
\end{align}
$$
Volvemos a considerar la igualdad anterior:
$$
\begin{align}
(\alpha + \gamma) \cos(1) + \beta &= 0 \\
2\alpha \cos(1) + \beta &= 0 \\
\beta = -2\alpha \cos(1)
\end{align}
$$

Ahora que tenemos los valores de $\alpha, \beta, \gamma$, definamos una combinación genérica en base a la igualdad original, sustituyendo $\alpha, \beta, \gamma$ por sus iguales, y considerando $\alpha = \gamma = 1$:
$$
\alpha \cos(x) - \beta \cos(x + 1) + \gamma \cos(x + 2) = 0 \implies \cos(x) - 2 \cos(1)\cos(x + 1) + \cos(x + 2) = 0
$$

Antes de proseguir, es importante considerar la siguiente igualdad trigonométrica: existe una identidad de suma a producto la cual establece
$$
\cos(A) + \cos(B) = 2 \cos\left( \frac{A + B}{2} \right) \cos\left( \frac{A - B}{2} \right)
$$
Aplicamos esto para los términos $\cos(x)$ y $\cos(x + 2)$:
$$
\begin{align}
\cos(x) + \cos(x + 2) &= 2 \cos\left( \frac{(x + 2) + x}{2} \right) \cos\left( \frac{(x + 2) - x}{2} \right) \\
&= 2 \cos\left( \frac{2x + 2}{2} \right) \cos\left( \frac{2}{2} \right) \\
&= 2 \cos(x + 1) \cos(1)
\end{align}
$$
Ahora, sustituimos esto en la igualdad general:
$$
\begin{align}
\cos(x) - 2 \cos(1)\cos(x + 1) + \cos(x + 2) &= 0 \\
\cancel{ 2 \cos(x + 1) \cos(1) } - \cancel{ 2 \cos(1)\cos(x + 1) } &= 0
\end{align}
$$
Como vemos, logramos anular la combinación lineal considerando coeficientes distintos de 0, especificamente:
$$
\begin{align}
&\alpha = \gamma \\
&\beta = -2\alpha \cos(1)
\end{align} \implies \begin{cases}
\alpha = 1 \\
\beta = -2\cos(1) \\
\gamma = 1
\end{cases}
$$

En conclusión, el conjunto $\{ \cos(x), \cos(x + 1), \cos(x + 2) \}$ es LD.