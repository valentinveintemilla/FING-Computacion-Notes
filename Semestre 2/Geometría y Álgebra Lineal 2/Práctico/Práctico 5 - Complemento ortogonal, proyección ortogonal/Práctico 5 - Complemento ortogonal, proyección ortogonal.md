# 1 - Complemento ortogonal
## Ejercicio 1
### Parte 1
#### Propiedad a
Sabemos que:
- $a' \in A^{\perp} \Longleftrightarrow a' \perp a \Longleftrightarrow \langle a', a \rangle = 0, \forall a \in A$
- $b' \in B^{\perp} \Longleftrightarrow b' \perp b \Longleftrightarrow \langle b', b \rangle = 0, \forall b \in B$

Como $A \subset B$, se cumple que $a \in A \implies a \in B, \forall a \in A$. Por esta razón, la inclusión de un elemento en $B^{\perp}$ también implica la ortogonalidad con todos los elementos de $A$: $b' \in B^{\perp} \Longleftrightarrow b' \perp b, \forall b \in B (\land \forall b \in A)$

De esta forma, podemos ver que $b' \in B^{\perp} \implies b' \in A^{\perp}$, pero $a' \in A^{\perp} \not \implies a' \in B'$. Esto se cumple ya que $B^{\perp}$ es un conjunto más restrictivo, ya que implica la ortogonalidad con todos los vectores de $A$, mas los de $B \setminus A$, por lo que si un elemento está en $B^{\perp}$, necesariamente está en $A^{\perp}$, ya que necesariamente es ortogonal a todos los elementos de $A$. Sin embargo, el recíproco no se cumple, ya que la pertenencia a $B^{\perp}$ implica la ortogonalidad con el resto de vectores de $B$: $B \setminus A$.

En conclusión, probamos que
$$
A \subset B \implies B^{\perp} \subset A^{\perp}
$$

#### Propiedad b
Sabemos que:
- $a' \in A^{\perp} \Longleftrightarrow a' \perp a \Longleftrightarrow \langle a', a \rangle = 0, \forall a \in A$
- $a' \in [A]^{\perp} \Longleftrightarrow a' \perp a \Longleftrightarrow \langle a', a \rangle = 0, \forall a \in [A]$

Es trivial que $A \subseteq [A]$. Como $A$ es generador del espacio $[A]$, entonces podemos tomar elementos linealmente independientes de $A$, formando una base de dicho espacio.

Sea $\{ a_{1}, \dots, a_{n} \} \subset A$ base de $[A]$ ($[A] = [\{ a_{1}, \dots, a_{n} \}]$). Entonces, podemos decir que $a' \in [A]^{\perp} \Longleftrightarrow a' \perp a_{i}, \forall i \in \{ 1, \dots, n \}$ (por proposición).

Queremos ver que esta también es la condición de ortogonalidad necesaria para pertenecer a $A^{\perp}$. Podemos expresar el resto de vectores que no son linealmente independientes como combinación lineal de los elementos de $\{ a_{1}, \dots, a_{n} \}$. Consideremos $\#A = r \geq n$:
$$
a_{k} = \alpha_{1_{k}} a_{1} + \dots + \alpha_{n_{k}} a_{n} = \sum_{i = 1}^{n} \alpha_{i_{k}} a_{i}, \forall a_{k} \in A, k \not \in \{ 1, \dots, n \}, k \leq r
$$
Por lo tanto:
$$
\begin{align}
\langle a', a_{k} \rangle &= \left\langle a', \sum_{i = 1}^{n} \alpha_{i_{k}} a_{i} \right\rangle \\
&= \sum_{i = 1}^{n} \overline{\alpha_{i_{k}}} \left\langle a', a_{i} \right\rangle
\end{align}
$$
Y podemos verificar que $\sum_{i = 1}^{n} \overline{\alpha_{i_{k}}} \left\langle a', a_{i} \right\rangle = 0 \Longleftrightarrow \left\langle a', a_{i} \right\rangle = 0, \forall i \in \{ 1, \dots, n \}$, ya que $\exists \alpha_{i_{k}} \neq 0$, puesto que si $\alpha_{i_{k}} = 0, \forall i_{k} \in \{ 1, \dots, n \}$, entonces $a_{k} = \vec{0}$.

De esta forma:
$$
a' \in A^{\perp} \Longleftrightarrow a' \perp a_{i} (\forall i \in \{ 1, \dots, n \}) \land \sum_{i = 1}^{n} \overline{\alpha_{i_{k}}} \left\langle a', a_{i} \right\rangle = 0 \Longleftrightarrow a' \perp a_{i}, \forall i \in \{ 1, \dots, n \}
$$

Entonces, como $A^{\perp}$ y $[A]^{\perp}$ se definen de la misma forma:
- $a' \in A^{\perp} \Longleftrightarrow a' \perp a_{i}, \forall i \in \{ 1, \dots, n \}$
- $a' \in [A]^{\perp} \Longleftrightarrow a' \perp a_{i}, \forall i \in \{ 1, \dots, n \}$

Concluimos que $A^{\perp} = [A]^{\perp}$.

CORRECCIÓN: Se demuestra por doble inclusión.

#### Propiedad c
Sabemos que $A$ puede o no ser un espacio vectorial (puede ser simplemente un conjunto), pero necesariamente el complemento es un espacio vectorial, y de hecho es un subespacio vectorial de $V$.

Sabemos que
- $a' \in A^{\perp} \Longleftrightarrow a' \perp a, \forall a \in A$
- $a'' \in (A^{\perp})^{\perp} \Longleftrightarrow a'' \perp a', \forall a' \in A^{\perp}$

Como vemos $a \in A$ y $a'' \in (A^{\perp})^{\perp}$, por lo que ambos verifican $a \perp a'$ y $a'' \perp a'$, $\forall a' \in A^{\perp}$. Considerando que $a, a'' \in V$, y que $A^{\perp} = [A]^{\perp}$, podemos determinar que si $a \in [A] \Longleftrightarrow a \in ([A]^{\perp})^{\perp}$, por lo tanto $[A] = ([A]^{\perp})^{\perp}$. Sabiendo que $A \subset [A]$, podemos concluir que $A \subset (A^{\perp})^{\perp}$, como queríamos probar.

### Parte 2
#### Propiedad 1
Es equivalente a la propiedad 3 para conjuntos:

Sabemos que
- $s' \in S^{\perp} \Longleftrightarrow s' \perp s, \forall s \in S$
- $s'' \in (S^{\perp})^{\perp} \Longleftrightarrow s'' \perp s', \forall s' \in S^{\perp}$

Como vemos $s \in A$ y $s'' \in (A^{\perp})^{\perp}$, por lo que ambos verifican $s \perp s'$ y $s'' \perp s'$, $\forall s' \in S^{\perp}$. Considerando que $s, s'' \in V$, podemos determinar que si $s \in S \Longleftrightarrow s \in ([S]^{\perp})^{\perp}$, por lo tanto $S = (S^{\perp})^{\perp}$.

#### Propiedad 2
Tenemos que probar que
$$
v \in (S + W)^{\perp} \Longleftrightarrow v \in S^{\perp} \cap W^{\perp}
$$
$S + W$ está compuesto por todas las combinaciones lineales de los vectores $s \in S$ y $w \in W$: $v \in S + W \Longleftrightarrow v = s + w, s \in S, w \in W$.

De esta forma,
$$
v' \in (S + W)^{\perp} \Longleftrightarrow v' \perp v, \forall v \in S + W \Longleftrightarrow  v' \perp s + w, \forall s \in S, w \in W
$$
Analizamos el producto interno $\langle v', s + w \rangle$:
$$
\begin{align}
\langle v', s + w \rangle &= \langle v', s \rangle + \langle v', w \rangle
\end{align}
$$
Ahora, analicemos cada término:
- Si $\langle v', s \rangle = 0, \forall s \in S \implies v' \in S^{\perp}$.
- Si $\langle v', w \rangle = 0, \forall w \in W \implies v' \in W^{\perp}$

De esta manera, basta que se satisfagan ambas condiciones a la vez para que $\langle v', s + w \rangle = 0, \forall s \in S, w \in W$:
$$
\begin{align}
\langle v', s \rangle = 0 \land \langle v', w \rangle = 0, \forall s \in S, w \in W &\implies \langle v', s + w \rangle = 0, \forall s \in S, w \in W \\
&\implies v' \in S^{\perp} \land v' \in W^{\perp} \\
&\implies v' \in S^{\perp} \cap W^{\perp}
\end{align}
$$
En conclusión:
$$
v \in (S + W)^{\perp} \Longleftrightarrow v \in S^{\perp} \cap W^{\perp}
$$
por lo que
$$
(S + W)^{\perp} = S^{\perp} \cap W^{\perp}
$$

#### Propiedad 3
Tenemos que probar que
$$
v \in (S \cap W)^{\perp} \Longleftrightarrow v \in S^{\perp} + W^{\perp}
$$
$S^{\perp} + W^{\perp}$ está compuesto por todas las combinaciones lineales de los vectores $s \in S^{\perp}$ y $w \in W^{\perp}$: $v \in S^{\perp} + W^{\perp} \Longleftrightarrow v = s + w, s \in S^{\perp}, w \in W^{\perp}$.

De esta forma,
$$
v' \in (S^{\perp} + W^{\perp})^{\perp} \Longleftrightarrow v' \perp v, \forall v \in S^{\perp} + W^{\perp} \Longleftrightarrow  v' \perp s + w, \forall s \in S^{\perp}, w \in W^{\perp}
$$
Analizamos el producto interno $\langle v', s + w \rangle$:
$$
\begin{align}
\langle v', s + w \rangle &= \langle v', s \rangle + \langle v', w \rangle
\end{align}
$$
Ahora, analicemos cada término:
- Si $\langle v', s \rangle = 0, \forall s \in S^{\perp} \implies v' \in (S^{\perp})^{\perp} = S$.
- Si $\langle v', w \rangle = 0, \forall w \in W^{\perp} \implies v' \in (W^{\perp})^{\perp} = W$

De esta manera, basta que se satisfagan ambas condiciones a la vez para que $\langle v', s + w \rangle = 0, \forall s \in S^{\perp}, w \in W^{\perp}$:
$$
\begin{align}
\langle v', s \rangle = 0 \land \langle v', w \rangle = 0, \forall s \in S^{\perp}, w \in W^{\perp} &\implies \langle v', s + w \rangle = 0, \forall s \in S^{\perp}, w \in W^{\perp} \\
&\implies v' \in S \land v' \in W \\
&\implies v' \in S \cap W
\end{align}
$$
En conclusión:
$$
v \in (S^{\perp} + W^{\perp})^{\perp} \Longleftrightarrow v \in S \cap W
$$
por lo que
$$
(S^{\perp} + W^{\perp})^{\perp} = S \cap W
$$

Entonces, podemos deducir que:
$$
((S^{\perp} + W^{\perp})^{\perp})^{\perp} = S^{\perp} + W^{\perp} = (S \cap W)^{\perp}
$$

---
## Ejercicio 2
### Parte 1
Determinamos el subespacio $S^{\perp}$ para determinar una base del mismo:
$$
\begin{align}
S^{\perp} &= \{ (x, y, z) \in \mathbb{C}^{3} : (x, y, z) \perp (i, 0, 1) \} \\
&= \{ (x, y, z) \in \mathbb{C}^{3} : \langle (x, y, z), (i, 0, 1) \rangle = 0 \} \\
&= \{ (x, y, z) \in \mathbb{C}^{3} : x \cdot \overline{i} + y \cdot \overline{0} + z \cdot \overline{1} = 0 \} \\
&= \{ (x, y, z) \in \mathbb{C}^{3} : -xi + z = 0 \} \\
&= \{ (x, y, xi) \in \mathbb{C}^{3} : x, y \in \mathbb{C} \} \\
&= [\{ (1, 0, i), (0, 1, 0) \}]
\end{align}
$$

En conclusión, $\{ (1, 0, i), (0, 1, 0) \}$ es una base de $S^{\perp}$.

### Parte 2
#### Parte a
Determinamos el subespacio $S^{\perp}$ considerando el producto interno habitual de $\mathbb{R}^{3}$:
$$
\begin{align}
S^{\perp} &= \{ (x, y, z) \in \mathbb{R}^{3} : (x, y, z) \perp (1, 2, 1) \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : \langle (x, y, z), (1, 2, 1) \rangle = 0 \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : x + 2y + z = 0 \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : z = -x - 2y \} \\
&= \{ (x, y, -x - 2y) \in \mathbb{R}^{3} : x, y \in \mathbb{R} \} \\
&= [\{ (1, 0, -1), (0, 1, -2) \}]
\end{align}
$$

En conclusión, $\{ (1, 0, -1), (0, 1, -2) \}$ es una base de $S^{\perp}$.

#### Parte b
Determinamos el subespacio $S^{\perp}$ considerando el producto interno $\langle (x_{1}, x_{2}, x_{3}), (y_{1}, y_{2}, y_{3}) \rangle = x_{1}y_{1} + 2x_{2}y_{2} + x_{3}y_{3} - x_{1}y_{2} - x_{2}y_{1}$:
$$
\begin{align}
S^{\perp} &= \{ (x, y, z) \in \mathbb{R}^{3} : (x, y, z) \perp (1, 2, 1) \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : \langle (x, y, z), (1, 2, 1) \rangle = 0 \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : x + 4y + z - 2x - y = 0 \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : -x + 3y + z = 0 \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : z = x - 3y \} \\
&= \{ (x, y, x - 3y) \in \mathbb{R}^{3} : x, y \in \mathbb{R} \} \\
&= [\{ (1, 0, 1), (0, 1, -3) \}]
\end{align}
$$

En conclusión, $\{ (1, 0, 1), (0, 1, -3) \}$ es una base de $S^{\perp}$.

---
## Ejercicio 3
### Parte 1
Aunque $S$ es un conjunto, no un espacio vectorial, sabemos que $S^{\perp} = [S]^{\perp}$ (como probamos en el ejercicio 1). De esta forma, consideramos $[S]^{\perp} = [\{ (3, 5, 1), (0, 1, 1) \}]$, y el producto interno proporcionado $\langle (x, y, z), (x', y', z') \rangle = xx' + 2yy' + 3zz'$. Por lo tanto, tenemos que determinar que vectores son perpendiculares a $(3, 5, 1)$ y $(0, 1, 1)$ a la vez:
$$
\begin{align}
S^{\perp} &= \{ (x, y, z) \in \mathbb{R}^{3} : (x, y, z) \perp (3, 5, 1) \land (x, y, z) \perp (0, 1, 1) \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : \langle (x, y, z), (3, 5, 1) \rangle = 0 \land \langle (x, y, z), (0, 1, 1) \rangle = 0 \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : 3x + 10y + 3z = 0 \land 2y + 3z = 0 \} \\
\end{align}
$$
$$
\begin{cases}
3x + 10y + 3z = 0 \\
2y + 3z = 0
\end{cases} \implies y = -\frac{3}{2}z \implies 3x - 12z = 0 \implies x = 4z
$$
$$
\begin{align}
S^{\perp} &= \left\{  (x, y, z) \in \mathbb{R}^{3} : y = -\frac{3}{2}z \land x = 4z  \right\} \\
&= \left\{  \left( 4z, -\frac{3}{2}z, z \right) \in \mathbb{R}^{3} : z \in \mathbb{R}  \right\} \\
&= \left[ \left\{  \left( 4, -\frac{3}{2}, 1 \right)  \right\} \right]
\end{align}
$$

En conclusión, $\left\{  \left( 4, -\frac{3}{2}, 1 \right)  \right\}$ es una base de $S^{\perp}$.

### Parte 2
Nuevamente, aplicamos lo demostrado en el ejercicio 1: $A$ no es un espacio vectorial, pero sabemos que $A^{\perp} = [A]^{\perp}$, por lo que consideraremos $[A]^{\perp} = [\{ (1, 2, 4), (1, 1, 1) \}]$ y el producto interno proporcionado $\langle (x, y, z), (x', y', z') \rangle = xx' + 2yy' + 3zz'$. Por lo tanto, tenemos que determinar que vectores son perpendiculares a $(1, 2, 4)$ y $(1, 1, 1)$ a la vez:
$$
\begin{align}
S^{\perp} &= \{ (x, y, z) \in \mathbb{R}^{3} : (x, y, z) \perp (1, 2, 4) \land (x, y, z) \perp (1, 1, 1) \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : \langle (x, y, z), (1, 2, 4) \rangle = 0 \land \langle (x, y, z), (1, 1, 1) \rangle = 0 \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : x + 4y + 12z = 0 \land x + 2y + 3z = 0 \} \\
\end{align}
$$
$$
\begin{cases}
x + 4y + 12z = 0 \\
x + 2y + 3z = 0
\end{cases} \implies 2y + 9z = 0 \implies y = -\frac{9}{2}z \implies x - 6z = 0 \implies x = 6z
$$
$$
\begin{align}
S^{\perp} &= \left\{  (x, y, z) \in \mathbb{R}^{3} : y = -\frac{9}{2}z \land x = 6z  \right\} \\
&= \left\{  \left( 6z, -\frac{9}{2}z, z \right) \in \mathbb{R}^{3} : z \in \mathbb{R}  \right\} \\
&= \left[ \left\{  \left( 6, -\frac{9}{2}, 1 \right)  \right\} \right]
\end{align}
$$

En conclusión, $\left\{  \left( 6, -\frac{9}{2}, 1 \right)  \right\}$ es una base de $S^{\perp}$.

---
## Ejercicio 4
### Parte 1
Determinamos una base ortonormal de $\mathcal{M}_{2}(\mathbb{R})$ para el producto interno $\langle A, B \rangle = tr(AB^{t})$:

Consideramos la base canónica de $\mathcal{M}_{2}(\mathbb{R})$:
$$
\mathcal{C} = \left\{ \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\}
$$
Aplicamos Gram-Schmidt:
$$
\mathcal{B}_{Og} = \{ w_{1}, w_{2}, w_{3}, w_{4} \}
$$
$$
w_{1} = \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}
$$
$$
\begin{align}
w_{2} &= \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \frac{\left\langle \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle}{\left\langle \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle} \cdot \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \\
&= \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \cancel{ \frac{0}{1} \cdot \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} } \\
&= \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
w_{3} &= \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} - \frac{\left\langle \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right\rangle}{\left\langle \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right\rangle} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \frac{\left\langle \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle}{\left\langle \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle} \cdot \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \\
&= \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} - \cancel{ \frac{0}{1} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} } - \cancel{ \frac{0}{1} \cdot \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} } \\
&= \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}
\end{align}
$$
$$
\begin{align}
w_{4} &= \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} - \frac{\left\langle \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right\rangle}{\left\langle \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right\rangle} \cdot \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} - \frac{\left\langle \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right\rangle}{\left\langle \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right\rangle} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \frac{\left\langle \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle}{\left\langle \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle} \cdot \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \\
&= \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} - \cancel{ \frac{0}{1} \cdot \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} } - \cancel{ \frac{0}{1} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} } - \cancel{ \frac{0}{1} \cdot \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} } \\
&= \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}
\end{align}
$$

De esta manera, una base canónica es:
$$
\mathcal{B}_{Og} = \left\{ \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\}
$$
Ahora, verifiquemos si es ortonormal:
$$
\begin{align}
||w_{1}|| &= \sqrt{ \left\langle \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle } = tr\left( \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right) = 1 \\
||w_{2}|| &= \sqrt{ \left\langle \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right\rangle } = tr\left( \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right) = 1 \\
||w_{3}|| &= \sqrt{ \left\langle \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right\rangle } = tr\left( \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right) = 1 \\
||w_{3}|| &= \sqrt{ \left\langle \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\rangle } = tr\left( \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right) = 1
\end{align}
$$

En conclusión, determinamos una base ortonormal considerando el producto interno dado:
$$
\mathcal{B}_{On} = \left\{ \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\}
$$

### Parte 2
$$
\mathcal{D} = \left\{  \begin{pmatrix}
a & 0 \\
0 & b
\end{pmatrix} : a, b \in \mathbb{R}  \right\} = \left[ \left\{  \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}  \right\} \right]
$$
Entonces, tenemos que determinar $\mathcal{D}^{\perp}$:
$$
\begin{align}
\mathcal{D}^{\perp} &= \left\{  \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \in \mathcal{M}_{2}(\mathbb{R}) : \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \perp \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \land \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \perp \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}  \right\} \\
&= \left\{  \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \in \mathcal{M}_{2}(\mathbb{R}) : \left\langle \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle = 0 \land \left\langle \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\rangle = 0  \right\} \\
&= \left\{  \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \in \mathcal{M}_{2}(\mathbb{R}) : a = 0 \land d = 0  \right\} \\
&= \left\{  \begin{pmatrix}
0 & b \\
c & 0
\end{pmatrix} : b, c \in \mathbb{R}  \right\} \\
&= \left[ \left\{  \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}  \right\} \right]
\end{align}
$$

En conclusión:
$$
\mathcal{D}^{\perp} = \left[ \left\{  \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}  \right\} \right]
$$

### Parte 3
$$
\mathcal{S} = \left\{  \begin{pmatrix}
a & b \\
b & c
\end{pmatrix} : a, b, c \in \mathbb{R}  \right\} = \left[ \left\{  \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} , \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}  \right\} \right]
$$
Entonces, tenemos que determinar $\mathcal{S}^{\perp}$:
$$
\begin{align}
\mathcal{S}^{\perp} &= \left\{  \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \in \mathcal{M}_{2}(\mathbb{R}) : \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \perp \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \land \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \perp \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} \land \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \perp \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}  \right\} \\
&= \left\{  \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \in \mathcal{M}_{2}(\mathbb{R}) : \left\langle \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}, \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right\rangle = 0 \land \left\langle \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} \right\rangle = 0 \land \left\langle \begin{pmatrix}
a & b \\
c & d
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\rangle = 0  \right\} \\
&= \left\{  \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \in \mathcal{M}_{2}(\mathbb{R}) : a = 0 \land b + c = 0 \land d = 0  \right\} \\
&= \left\{  \begin{pmatrix}
0 & b \\
-b & 0
\end{pmatrix} : b \in \mathbb{R}  \right\} \\
&= \left[ \left\{  \begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}  \right\} \right]
\end{align}
$$

En conclusión:
$$
\mathcal{S}^{\perp} = \left[ \left\{  \begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}  \right\} \right]
$$

---
## Ejercicio 5
### Parte 1
Desarrollamos el subespacio $S^{\perp}$:
$$
\begin{align}
S^{\perp} &= \{ v \in V : v \perp s_{i}, \forall i \in \{ s_{1}, s_{2}, \dots, s_{r} \} \}
\end{align}
$$
Como $v \in V$, entonces podemos expresarlo por combinación lineal de una base:
$$
v = \alpha_{1} s_{1} + \dots + \alpha_{r} s_{r} + \alpha_{r + 1} v_{r + 1} + \dots + \alpha_{n} v_{n} = \sum_{i = 1}^{r} \alpha_{i} s_{i} + \sum_{j = r + 1}^{n} \alpha_{j} v_{j}
$$
Desarrollamos el producto interno entre un vector $v \in V$ genérico y $s_{i}, i \in \{ 1, \dots, r \}$
$$
\begin{align}
\langle v, s_{i} \rangle &= \left\langle \sum_{k = 1}^{r} \alpha_{k} s_{k} + \sum_{j = r + 1}^{n} \alpha_{j} v_{j}, s_{i} \right\rangle \\
&= \sum_{k = 1}^{r} \alpha_{k} \left\langle s_{k}, s_{i} \right\rangle + \sum_{j = r + 1}^{n} \alpha_{j} \left\langle v_{j}, s_{i} \right\rangle
\end{align}
$$
Como $s_{i}$ y $s_{k}, k \in \{ 1, \dots, r \}$ pertenecen a una base ortonormal, entonces $\langle s_{k}, s_{i} \rangle = 0$ cuando $k \neq i$ y $\langle s_{k}, s_{i} \rangle = ||s_{i}||^{2} = 1^{2} = 1$ cuando $k = i$.
Como $v_{j} \neq s_{i}, \forall j \in \{ r + 1, \dots, n \}$, entonces $\left\langle v_{j}, s_{i} \right\rangle = 0$.

De esta forma:
$$
\begin{align}
&= \alpha_{i} \left\langle s_{i}, s_{i} \right\rangle \\
&= \alpha_{i}
\end{align}
$$

Entonces, determinamos que $\forall i \in \{ 1, \dots, r \}, \langle v, s_{i} \rangle = \alpha_{i}$, y como sabemos que para que $v \in S^{\perp}$, tiene que verificarse $\langle v, s_{i} \rangle = 0, \forall i \in \{ 1, \dots, r \}$, entonces deducimos que: $\forall v \in S^{\perp}, v = \alpha_{1} s_{1} + \dots + \alpha_{r} s_{r} + \alpha_{r + 1} v_{r + 1} + \dots + \alpha_{n} v_{n}$ se cumple que $\alpha_{i} = 0, \forall i \in \{ 1, \dots, r \}$. De esta forma:
$$
\forall v \in S^{\perp}, v = \alpha_{r + 1} v_{r + 1} + \dots + \alpha_{n} v_{n} = \sum_{j = r + 1}^{n} \alpha_{j} \left\langle v_{j}, s_{i} \right\rangle
$$

Por lo tanto, las coordenadas de dichos vectores en la base $\mathcal{B} = \{ s_{1}, s_{2}, \dots, s_{r}, v_{r + 1}, \dots, v_{n} \}$ es:
$$
coord_{\mathcal{B}}(v) = (0, 0, \dots, \underbrace{ 0 }_{ \text{Posición } r }, \alpha_{r + 1}, \dots, \alpha_{n})\forall v \in S^{\perp}
$$

En conclusión, cualquier vector $v \in S^{\perp}$ se compone por combinación lineal de los vectores $v_{i}, i \in \{ r + 1, \dots, n \}$, por lo que $\{ v_{r + 1}, \dots, v_{n} \}$ es una base de $S^{\perp}$. Además, todos sus vectores tienen norma 1 y son ortogonales (por hipótesis, ya que pertenecían a una base ortonormal, y lo que hicimos fue formar una base reducida a partir de la misma, manteniendo dichas propiedades), por lo que $\{ v_{r + 1}, \dots, v_{n} \}$ es una base ortonormal.

### Parte 2
#### Parte a
Consideramos el producto interno propuesto para determinar el valor de $\alpha$ que verifique la ortogonalidad entre $v_{1}$ y $v_{2}$: ¿Qué valor de $\alpha$ verifica $\langle v_{1}, v_{2} \rangle = 0$?
$$
\begin{align}
\langle v_{1}, v_{2} \rangle &= \langle (1, 1, 1), (1, 0, -1) \rangle \\
&= 2 \cdot 1 \cdot 1 + \cancel{ 2 \cdot 1 \cdot 0 } + \alpha \cdot 1 \cdot (-1) + \cancel{ 1 \cdot (-1) } + \cancel{ 1 \cdot 1 } \\
&= 2 - \alpha
\end{align}
$$
$$
\langle v_{1}, v_{2} \rangle = 2 - \alpha \implies \langle v_{1}, v_{2} \rangle \Longleftrightarrow 2 - \alpha = 0 \Longleftrightarrow \alpha = 2
$$
En conclusión, el valor de $\alpha$ que verifica $\langle v_{1}, v_{2} \rangle = 0$ es $\alpha = 2$.

#### Parte b
Construimos la base ortonormal de $\mathbb{R}^{3}$ a partir de $\{ v_{1}, v_{2}, v_{3} \}$ considerando $\alpha = 2$:
$$
\mathcal{B}_{Og} = \{ w_{1}, w_{2}, w_{3} \}
$$
$$
w_{1} = v_{1} = (1, 1, 1)
$$
$$
\begin{align}
w_{2} &= v_{2} - \frac{\langle v_{2}, w_{1} \rangle}{\langle w_{1}, w_{1} \rangle}w_{1} \\
&= (1, 0, -1) - \frac{\langle (1, 0, -1), (1, 1, 1) \rangle}{\langle (1, 1, 1), (1, 1, 1) \rangle}(1, 1, 1) \\
&= (1, 0, -1) - \frac{2 + 0 - 2 + 1 - 1}{2 + 2 + 2 + 1 + 1}(1, 1, 1) \\
&= (1, 0, -1) - \cancel{ \frac{0}{8}(1, 1, 1) } \\
&= (1, 0, -1)
\end{align}
$$
No era necesario hacer el cálculo anterior, ya que determinamos el valor de $\alpha$ que satisfacía $\langle v_{1}, v_{2} \rangle = 0$.
$$
\begin{align}
w_{3} &= v_{3} - \frac{\langle v_{3}, w_{2} \rangle}{\langle w_{2}, w_{2} \rangle}w_{2} - \frac{\langle v_{3}, w_{1} \rangle}{\langle w_{1}, w_{1} \rangle}w_{1} \\
&= (0, 0, 1) - \frac{\langle (0, 0, 1), (1, 0, -1) \rangle}{\langle (1, 0, -1), (1, 0, -1) \rangle}(1, 0, -1) - \frac{\langle (0, 0, 1), (1, 1, 1) \rangle}{\langle (1, 1, 1), (1, 1, 1) \rangle}(1, 1, 1) \\
&= (0, 0, 1) - \frac{0 + 0 - 2 + 0 + 1}{2 + 0 + 2 - 1 - 1}(1, 0, -1) - \frac{0 + 0 + 2 + 0 + 1}{2 + 2 + 2 + 1 + 1}(1, 1, 1) \\
&= (0, 0, 1) + \frac{1}{2}(1, 0, -1) - \frac{3}{8}(1, 1, 1) \\
&= (0, 0, 1) + \left( \frac{1}{2}, 0, -\frac{1}{2} \right) - \left( \frac{3}{8}, \frac{3}{8}, \frac{3}{8} \right) \\
&= \left( \frac{1}{8}, -\frac{3}{8}, \frac{1}{8} \right)
\end{align}
$$
De esta manera, una base ortogonal es:
$$
\mathcal{B}_{Og} = \left\{  (1, 1, 1), (1, 0, -1), \left( \frac{1}{8}, -\frac{3}{8}, \frac{1}{8} \right)  \right\}
$$

De paso determinamos $||(1, 1, 1)||^{2} = 8 \implies ||(1, 1, 1)|| = \sqrt{ 8 }$ y $||(1, 0, -1)||^{2} = 2 \implies ||(1, 0, -1)|| = \sqrt{ 2 }$. Resta determinar $\left| \left| \left( \frac{1}{8}, -\frac{3}{8}, \frac{1}{8} \right) \right| \right|$:
$$
\begin{align}
\left| \left| \left( \frac{1}{8}, -\frac{3}{8}, \frac{1}{8} \right) \right| \right| &= \sqrt{ \left\langle \left( \frac{1}{8}, -\frac{3}{8}, \frac{1}{8} \right), \left( \frac{1}{8}, -\frac{3}{8}, \frac{1}{8} \right) \right\rangle } \\
&= \sqrt{ \frac{2}{64} + \frac{18}{64} + \frac{2}{64} + \frac{1}{64} + \frac{1}{64} } \\
&= \sqrt{ \frac{6}{16} } \\
&= \frac{\sqrt{ 6 }}{4}
\end{align}
$$


Finalmente, determinamos la base ortonormal:
$$
\begin{align}
\mathcal{B}_{On} &= \left\{  \frac{1}{\sqrt{ 8 }} \cdot (1, 1, 1), \frac{1}{\sqrt{ 2 }} \cdot (1, 0, -1), \frac{4}{\sqrt{ 6 }} \cdot \left( \frac{1}{8}, -\frac{3}{8}, \frac{1}{8} \right)  \right\} \\
&= \left\{  \left( \frac{1}{\sqrt{ 8 }}, \frac{1}{\sqrt{ 8 }}, \frac{1}{\sqrt{ 8 }} \right), \left( \frac{1}{\sqrt{ 2 }}, 0, -\frac{1}{\sqrt{ 2 }} \right), \left( \frac{1}{2\sqrt{ 6 }}, -\frac{3}{2\sqrt{ 6 }}, \frac{1}{2\sqrt{ 6 }} \right) \right\}
\end{align}
$$

#### Parte c
Determinamos el subconjunto $[(1, 1, 1)]^{\perp}$:
$$
\begin{align}
[(1, 1, 1)]^{\perp} &= \{ (x, y, z) \in \mathbb{R}^{3} : (x, y, z) \perp (1, 1, 1) \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : \langle (x, y, z), (1, 1, 1) \rangle = 0 \} \\
&= \{ (x, y, z) \in \mathbb{R}^{3} : 3x + 2y + 3z = 0 \} \\
&= \left\{  (x, y, z) \in \mathbb{R}^{3} : z = -x - \frac{2}{3}y  \right\} \\
&= \left\{  \left( x, y, -x - \frac{2}{3}y \right) \in \mathbb{R}^{3} : x, y \in \mathbb{R}  \right\} \\
&= \left[ \left\{  \left( 1, 0, -1 \right), \left( 0, 1, -\frac{2}{3} \right)  \right\} \right]
\end{align}
$$

En conclusión, $\left\{  \left( 1, 0, -1 \right), \left( 0, 1, -\frac{2}{3} \right)  \right\}$ es una base de $[(1, 1, 1)]^{\perp}$.

---
# 2 - Proyección ortogonal

> [!Proyección ortogonal]
> Dado $v \in V$ llamamos proyección ortogonal de $v$ sobre el subespacio $S$ al vector $P_{S}(v) = v_{S}$.
> 
> Si $V$ tiene dimensión finita y $B_{S} = \{ s_{1}, \dots, s_{k} \}$ es una base ortonormal de $S$, entonces
> $$
> P_{S}(v) = \sum_{i = 1}^{k} \langle v, s_{i} \rangle s_{i}; \space s_{i} \in S
> $$

## Ejercicio 6
### Parte 1
Sea $s \in S$, determinemos $P_{S}(s)$ según la definición. Consideremos $\{ s_{1}, \dots, s_{n} \}$ base ortonormal (existe por proposición) de $S$. De esta forma:
$$
s = \alpha_{1} \cdot s_{1} + \dots + \alpha_{n} \cdot s_{n} = \sum_{j = 1}^{n} \alpha_{j} \cdot s_{j}
$$
 Calculamos $P_{S}(s)$
$$
\begin{align}
P_{S}(s) &= \sum_{i = 1}^{n} \langle s, s_{i} \rangle s_{i} \\
&= \sum_{i = 1}^{n} \left\langle \sum_{j = 1}^{n} \alpha_{j} \cdot s_{j}, s_{i} \right\rangle s_{i} \\
&= \sum_{i = 1}^{n} \sum_{j = 1}^{n} \alpha_{j} \cdot \langle s_{j}, s_{i} \rangle s_{i}
\end{align}
$$
Como $s_{j}$ y $s_{i}$ pertenecen a una base ortonormal, $\langle s_{j}, s_{i} \rangle = 0, \forall i \neq j$ y $\langle s_{j}, s_{i} \rangle = 1 \Longleftrightarrow i = j$:
$$
\begin{align}
&= \sum_{j = 1}^{n} \alpha_{j} \cdot \langle s_{j}, s_{j} \rangle s_{j} \\
&= \sum_{j = 1}^{n} \alpha_{j} \cdot s_{j} \\
&= s
\end{align}
$$

En conclusión:
$$
P_{S}(s) = s, \forall s \in S
$$

### Parte 2
Sea $v \in S^{\perp}$, determinemos $P_{S}(v)$ según la definición. Consideremos $\{ s_{1}, \dots, s_{n} \}$ base ortonormal (existe por proposición) de $S$. Entonces
$$
P_{S}(v) = \sum_{i = 1}^{n} \langle v, s_{i} \rangle s_{i}
$$
Como $v \in S^{\perp}$ y $s_{i} \in S$, entonces $\langle v, s_{i} \rangle = 0, \forall i \in \{ 1, \dots, n \}$:
$$
\begin{align}
&= \sum_{j = 1}^{n} \alpha_{j} \cdot 0 \cdot s_{j} \\
&= \sum_{j = 1}^{n} \vec{0} \\
&= \vec{0}
\end{align}
$$

En conclusión:
$$
P_{S}(v) = \vec{0}, \forall v \in S^{\perp}
$$

### Parte 3
Para probar que es una transformación lineal, tenemos que verificar que:
- $P_{S}(\vec{0}_{V}) = \vec{0}_{V}$
- $P_{S}(u + v) = P_{S}(u) + P_{S}(v), \forall u, v \in V$
- $P_{S}(\alpha \cdot u) = \alpha \cdot P_{S}(u), \forall \alpha \in \mathbb{K}, u \in V$

Consideremos $\{ s_{1}, \dots, s_{n} \}$ base ortonormal (existe por proposición) de $S$.

- $P_{S}(\vec{0}_{V}) = \vec{0}_{V}$
$$
\begin{align}
P_{S}(\vec{0}_{V}) &= \sum_{i = 1}^{n} \langle \vec{0}, s_{i} \rangle s_{i}
\end{align}
$$
Sabemos que $\langle \vec{0}, v \rangle = 0, \forall v \in V$. Por lo tanto:
$$
\begin{align}
P_{S}(\vec{0}_{V}) &= \sum_{i = 1}^{n} 0 \cdot s_{i} \\
&= \sum_{i = 1}^{n} \vec{0} \\
&= \vec{0}
\end{align}
$$

De esta forma:
$$
P_{S}(\vec{0}_{V}) = \vec{0}
$$

- $P_{S}(u + v) = P_{S}(u) + P_{S}(v), \forall u, v \in V$
$$
\begin{align}
P_{S}(u + v) &= \sum_{i = 1}^{n} \langle u + v, s_{i} \rangle s_{i} \\
&= \sum_{i = 1}^{n} (\langle u, s_{i} \rangle + \langle v, s_{i} \rangle) s_{i} \\
&= \sum_{i = 1}^{n} \langle u, s_{i} \rangle s_{i} + \langle v, s_{i} \rangle s_{i} \\
&= \sum_{i = 1}^{n} \langle u, s_{i} \rangle s_{i} + \sum_{i = 1}^{n} \langle v, s_{i} \rangle s_{i} \\
&= P_{S}(u) + P_{S}(v)
\end{align}
$$

De esta forma:
$$
P_{S}(u + v) = P_{S}(u) + P_{S}(v)
$$

- $P_{S}(\alpha \cdot u) = \alpha \cdot P_{S}(u), \forall \alpha \in \mathbb{K}, u \in V$
$$
\begin{align}
P_{S}(\alpha \cdot u) &= \sum_{i = 1}^{n} \langle \alpha \cdot u, s_{i} \rangle s_{i} \\
&= \sum_{i = 1}^{n} \alpha \cdot \langle u, s_{i} \rangle s_{i} \\
&= \alpha \cdot \sum_{i = 1}^{n} \langle u, s_{i} \rangle s_{i} \\
&= \alpha \cdot P_{S}(u)
\end{align}
$$

De esta forma:
$$
P_{S}(\alpha \cdot u) = \alpha \cdot P_{S}(u)
$$

En conclusión, $P_{S} : V \to V$ dada por $v \overset{P_{S}} \mapsto P_{S}(v)$ es una transformación lineal.

### Parte 4
Consideramos las bases:
- $\{ s_{1}, \dots, s_{n} \} \subset S$ ortonormal tal que $[\{ s_{1}, \dots, s_{r} \}] = S$
- $\{ v_{r + 1}, \dots, v_{n} \} \subset S^{\perp}$ ortonormal tal que $[\{ v_{r + 1}, \dots, v_{n} \}] = S^{\perp}$

De esta manera, $\{ s_{1}, \dots, s_{n} \} \cup \{ v_{r + 1}, \dots, v_{n} \} = \{ s_{1}, \dots, s_{n}, v_{r + 1}, \dots, v_{n} \}$ tal que $\mathcal{B} = \{ s_{1}, \dots, s_{n}, v_{r + 1}, \dots, v_{n} \} \subset V$ y $[\{ s_{1}, \dots, s_{n}, v_{r + 1}, \dots, v_{n} \}] = V$ es una base ortonormal.

De esta manera, la matriz asociada de $P_{S}$ en la base $\mathcal{B}$ es:
$$
_{\mathcal{B}}(P_{S})_{\mathcal{B}} = \begin{pmatrix}
coord_{\mathcal{B}}(P_{S}(s_{1})) & \dots & coord_{\mathcal{B}}(P_{S}(s_{r})) & coord_{\mathcal{B}}(P_{S}(v_{r + 1})) & \dots & coord_{\mathcal{B}}(P_{S}(v_{n}))
\end{pmatrix}
$$

Ahora, determinamos las columnas correspondientes:
$$
P_{S}(s_{i}) = \sum_{j = 1}^{r} \langle s_{i}, s_{j} \rangle s_{j}
$$
Sabemos que $\langle s_{i}, s_{j} \rangle = 0, \forall j \neq i$, y $\langle s_{i}, s_{j} \rangle = 1, j = i$, por lo tanto:
$$
P_{S}(s_{i}) = \langle s_{i}, s_{i} \rangle s_{i} = s_{i}
$$
Entonces:
$$
coord_{\mathcal{B}}(P_{S}(s_{i})) = coord_{\mathcal{B}}(s_{i}) = (0, \dots, 0, \underbrace{ 1 }_{ \text{Posición i-ésima} }, 0, \dots, 0), \forall i \in \{ 1, \dots, r \}
$$

$$
P_{S}(v_{i}) = \sum_{j = 1}^{r} \langle v_{i}, s_{j} \rangle s_{j}
$$
Sabemos que $\langle v_{i}, s_{j} \rangle = 0, \forall j \in \{ 1, \dots, r \}, i \in \{ r + 1, \dots, n \}$, por lo tanto:
$$
P_{S}(v_{i}) = \sum_{j = 1}^{r} \langle v_{i}, s_{j} \rangle s_{j} = \sum_{j = 1}^{r} 0 \cdot s_{j} = \sum_{j = 1}^{r} \vec{0} = \vec{0}
$$
Entonces (como $\mathcal{B}$ es LI):
$$
coord_{\mathcal{B}}(P_{S}(v_{i})) = coord_{\mathcal{B}}(\vec{0}) = (0, \dots, 0), \forall i \in \{ r + 1, \dots, n \}
$$

En conclusión:
$$
_{\mathcal{B}}(P_{S})_{\mathcal{B}} = \begin{pmatrix}
1 & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 1 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & 0
\end{pmatrix} = \begin{pmatrix}
\underbrace{ I }_{ r \times r } & \underbrace{ O }_{ (n - r) \times (n - r) } \\
\underbrace{ O }_{ r \times r } & \underbrace{ O }_{ (n - r) \times (n - r) }
\end{pmatrix}
$$

En caso de que las bases elegidas no fueran ortonormales, en lugar de un bloque $I$, tendríamos:
$$
\begin{pmatrix}
\langle s_{1}, s_{1} \rangle & \langle s_{2}, s_{1} \rangle & \dots & \langle s_{r}, s_{1} \rangle \\
\langle s_{1}, s_{2} \rangle & \langle s_{2}, s_{2} \rangle & \dots & \langle s_{r}, s_{2} \rangle \\
\vdots & \vdots & \ddots & \vdots \\
\langle s_{1}, s_{r} \rangle & \langle s_{2}, s_{r} \rangle & \dots & \langle s_{r}, s_{r} \rangle
\end{pmatrix} = \begin{pmatrix}
||s_{1}||^{2} & \langle s_{2}, s_{1} \rangle & \dots & \langle s_{r}, s_{1} \rangle \\
\langle s_{1}, s_{2} \rangle & ||s_{2}||^{2} & \dots & \langle s_{r}, s_{2} \rangle \\
\vdots & \vdots & \ddots & \vdots \\
\langle s_{1}, s_{r} \rangle & \langle s_{2}, s_{r} \rangle & \dots & ||s_{r}||^{2}
\end{pmatrix}
$$

### Parte 5
Determinamos el núcleo de $P_{S}$:
$$
N(P_{S}) = \{ v \in V : P_{S}(v) = \vec{0} \}
$$
De esta manera:
$$
N(P_{S}) = S^{\perp}
$$
ya que como probamos en la parte 2, $P_{S}(v) = \vec{0}, \forall v \in S^{\perp}$. Como $S^{\perp}$ es un espacio vectorial, contiene al vector nulo (el cual también tiene como imagen $\vec{0}$).

Determinamos la imagen de $P_{S}$:
$$
\mathrm{Im}(P_{S}) = \{ v \in V : P_{S}(s) = v, s \in V \}
$$
En este caso, $\mathrm{Im}(P_{S}) = S$, ya que $P_{S}(s) = s, \forall s \in S^{\perp}$, y $P_{S}(s') = \vec{0}, \forall s' \in S^{\perp}$.

### Parte 6
Consideremos la matriz asociada obtenida en base a la base ortonormal de $V$:
$$
_{\mathcal{B}}(P_{S})_{\mathcal{B}} = \begin{pmatrix}
1 & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 1 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & 0
\end{pmatrix} = \begin{pmatrix}
\underbrace{ I }_{ r \times r } & \underbrace{ O }_{ (n - r) \times (n - r) } \\
\underbrace{ O }_{ r \times r } & \underbrace{ O }_{ (n - r) \times (n - r) }
\end{pmatrix}
$$
Si analizamos el determinante de la matriz $P_{S} - \lambda \cdot \mathbb{I}$:
$$
\begin{align}
\det(P_{S} - \lambda \cdot \mathbb{I}) &= \begin{pmatrix}
1 - \lambda & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 1 - \lambda & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 1 - \lambda & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & -\lambda & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & -\lambda
\end{pmatrix} \\
&= (1 - \lambda)^{r} \cdot (-\lambda)^{n - r}
\end{align}
$$

De esta manera, tenemos dos valores propios:
- $1 - \lambda = 0 \implies \lambda = 1$
$$
N\left( \begin{pmatrix}
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & -1 & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & -1
\end{pmatrix} \right) = \begin{pmatrix}
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & -1 & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & -1
\end{pmatrix} \cdot \begin{pmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{r} \\
x_{r + 1} \\
\vdots \\
x_{n}
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
\vdots \\
0 \\
0 \\
\vdots \\
0
\end{pmatrix} \implies \begin{cases}
x_{r + 1} = 0 \\
x_{r + 2} = 0 \\
\vdots \\
x_{n} = 0
\end{cases} \implies x_{1}, x_{2}, \dots, x_{r} \text{ son libres}
$$
$$
S_{1} = \{ (x_{1}, x_{2}, \dots, x_{r}, 0, \dots, 0) : x_{1}, x_{2}, \dots, x_{r} \in \mathbb{K} \} = \left[ \left\{ 
(1, 0, \dots, 0, 0, \dots, 0),
(0, 1, \dots, 0, 0, \dots, 0),
\dots
(0, 0, \dots, 1, 0, \dots, 0)
 \right\} \right]
$$
De esta manera, $dim(S_{1}) = r$.

- $-\lambda = 0 \implies \lambda = 0$
$$
N\left( \begin{pmatrix}
1 & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 1 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & 0
\end{pmatrix} \right) = \begin{pmatrix}
1 & 0 & \dots & 0 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 1 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & \dots & 0 & 0 & \dots & 0
\end{pmatrix} \cdot \begin{pmatrix}
x_{1} \\
x_{2} \\
\vdots \\
x_{r} \\
x_{r + 1} \\
\vdots \\
x_{n}
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
\vdots \\
0 \\
0 \\
\vdots \\
0
\end{pmatrix} \implies \begin{cases}
x_{1} = 0 \\
x_{2} = 0 \\
\vdots \\
x_{r} = 0
\end{cases} \implies x_{r + 1}, x_{r + 2}, \dots, x_{n} \text{ son libres}
$$
$$
S_{1} = \{ (0, \dots, 0, x_{r + 1}, x_{r + 2} \dots, x_{n}) : x_{r + 1}, x_{r + 2}, \dots, x_{n} \in \mathbb{K} \} = \left[ \left\{ 
(0, 0, \dots, 0, 1, 0, \dots, 0),
(0, 0, \dots, 0, 0, 1, \dots, 0),
\dots
(0, 0, \dots, 0, 0, 0, \dots, 1)
 \right\} \right]
$$
De esta manera, $dim(S_{1}) = n - r$.

En conclusión, $ma(1) = mg(1) = r$ y $ma(0) = mg(0) = n - r$, por lo que $P_{S}$ es diagonalizable.

ACLARACIÓN: En realidad, bastaba con ver que la matriz asociada era diagonal para concluir que $P_{S}$ es diagonalizable.

### Parte 7
Consideremos $v \in V$ genérico. Sabemos que $S \cap S^{\perp} = \{ \vec{0} \}$, y $S \oplus S^{\perp} = V$. Consideramos las bases ortonormales $\{ s_{1}, \dots, s_{r} \}$ de $S$ y $\{ v_{r + 1}, \dots, v_{n} \}$ de $S^{\perp}$ tal que $\{ s_{1}, \dots, s_{r} \} \cup \{ v_{r + 1}, \dots, v_{n} \} = \{ s_{1}, \dots, s_{r}, v_{r + 1}, \dots, v_{n} \}$ es una base de $V$. De esta manera:
$$
\begin{align}
v &= \alpha_{1} \cdot s_{1} + \dots + \alpha_{r} \cdot s_{r} + \alpha_{r + 1} \cdot v_{r + 1} + \dots + \alpha_{n} \cdot v_{n} \\
&= \sum_{i = 1}^{r} \alpha_{i} \cdot s_{i} + \sum_{j = r + 1}^{n} \alpha_{j} \cdot v_{j} \\
&= \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} + \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}
\end{align}
$$

Por otra parte, podemos desarrollar las proyecciones ortogonales de $v$ sobre $S$ y $S^{\perp}$:
$$
P_{S}(v) = \sum_{i = 1}^{r} \langle v, s_{i} \rangle s_{i}
$$
$$
P_{S^{\perp}}(v) = \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle v_{j}
$$

Finalmente, desarrollamos el producto interno $\langle v, v \rangle = ||v||^{2}$:
$$
\begin{align}
\langle v, v \rangle &= \left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} + \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} + \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j} \right\rangle \\
&= \left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle + \left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i}, \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j} \right\rangle + \left\langle \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle + \left\langle \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}, \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j} \right\rangle
\end{align}
$$
Sabiendo que $\sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} = P_{S}(v) \in S$ y $\sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j} = P_{S^{\perp}}(v) \in S^{\perp}$:
$$
\left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i}, \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j} \right\rangle = \left\langle \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle = 0
$$

Entonces:
$$
\langle v, v \rangle = \left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle + \left\langle \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}, \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j} \right\rangle
$$

En conclusión:
$$
||v||^{2} = ||P_{S}(v)||^{2} + ||P_{S^{\perp}}(v)||^{2}
$$

### Parte 8
En el mismo contexto anterior, probamos que
$$
||v||^{2} = ||P_{S}(v)||^{2} + ||P_{S^{\perp}}(v)||^{2}, \forall v \in V
$$

Trabajando la igualdad:
$$
||v|| = \sqrt{ ||P_{S}(v)||^{2} + ||P_{S^{\perp}}(v)||^{2} }
$$

Sabemos que $||P_{S^{\perp}}(v)|| \geq 0$, verificando $||P_{S^{\perp}}(v)|| = 0 \Longleftrightarrow v \in S$. De esta manera:
$$
||v|| \geq \sqrt{ ||P_{S}(v)||^{2} + 0^{2} } \geq \sqrt{ ||P_{S}(v)||^{2} } \geq ||P_{S}(v)||
$$

En conclusión:
$$
||v|| \geq ||P_{S}(v)||, \forall v \in V
$$

### Parte 9
Consideramos el contexto establecido en la parte 7 y desarrollamos el producto interno correspondiente:
$$
\begin{align}
\langle v, P_{S}(v) \rangle &= \left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} + \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle \\
&= \left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle + \left\langle \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle
\end{align}
$$

Sabiendo que $\sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} = P_{S}(v) \in S$ y $\sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j} = P_{S^{\perp}}(v) \in S^{\perp}$:
$$
\left\langle \sum_{j = r + 1}^{n} \langle v, v_{j} \rangle \cdot v_{j}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle = 0
$$

Entonces:
$$
\begin{align}
\langle v, P_{S}(v) \rangle &= \left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle
\end{align}
$$

Como definimos $P_{S}(v) = \sum_{i = 1}^{r} \langle v, s_{i} \rangle s_{i}$, determinamos que $\left\langle \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i}, \sum_{i = 1}^{r} \langle v, s_{i} \rangle \cdot s_{i} \right\rangle = ||P_{S}(v)||^{2}$.

En conclusión:
$$
\langle v, P_{S}(v) \rangle = ||P_{S}(v)||^{2}
$$

---
## Ejercicio 7
Antes de determinar $P_{S}(v)$ en base a la definición, tenemos que comprobar que la base provista sea ortonormal, y en caso de que no lo sea (o no tengamos una), aplicar Gram-Schmidt para determinarla.

### Parte 1
Comprobamos que la base $\{ (1, -1, 1, 1), (2, 1, 0, 3) \}$ sea ortonormal:
$$
\langle (1, -1, 1, 1), (2, 1, 0, 3) \rangle = 1 \cdot 2 + (-1) \cdot 1 + 1 \cdot 0 + 1 \cdot 3 = 2 - 1 + 0 + 3 = 4 \neq 0
$$
Como vemos, la base no es ortogonal, por lo que aplicamos Gram-Schmidt:
$$
\mathcal{B}_{Og} = \{ w_{1}, w_{2} \}
$$
$$
w_{1} = (1, -1, 1, 1)
$$
$$
\begin{align}
w_{2} &= (2, 1, 0, 3) - \frac{\langle (2, 1, 0, 3), (1, -1, 1, 1) \rangle}{\langle (1, -1, 1, 1), (1, -1, 1, 1) \rangle} \cdot (1, -1, 1, 1) \\
&= (2, 1, 0, 3) - \frac{4}{4} \cdot (1, -1, 1, 1) \\
&= (1, 2, -1, 2)
\end{align}
$$
$$
\mathcal{B}_{Og} = \{ (1, -1, 1, 1), (1, 2, -1, 2) \}
$$

De paso, determinamos que $||(1, -1, 1, 1)|| = \sqrt{ 4 } = 2$.
$$
||(1, 2, -1, 2)|| = \sqrt{ \langle (1, 2, -1, 2), (1, 2, -1, 2) \rangle } = \sqrt{ 1 + 4 + 1 + 4 } = \sqrt{ 10 }
$$

Finalmente, hallamos la base ortonormal:
$$
\mathcal{B}_{On} = \left\{  \frac{1}{2} \cdot (1, -1, 1, 1), \frac{1}{\sqrt{ 10 }} \cdot (1, 2, -1, 2)  \right\} = \left\{  \left( \frac{1}{2}, -\frac{1}{2}, \frac{1}{2}, \frac{1}{2} \right), \left( \frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }}, -\frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }} \right)  \right\}
$$

Pasamos a determinar $P_{S}(v)$ con $v = (x, y, z, t)$:
$$
\begin{align}
P_{S}(v) &= \left\langle (x, y, z, t), \left( \frac{1}{2}, -\frac{1}{2}, \frac{1}{2}, \frac{1}{2} \right) \right\rangle \cdot \left( \frac{1}{2}, -\frac{1}{2}, \frac{1}{2}, \frac{1}{2} \right) + \left\langle (x, y, z, t), \left( \frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }}, -\frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }} \right) \right\rangle \cdot \left( \frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }}, -\frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }} \right) \\
&= \left( \frac{1}{2}x - \frac{1}{2}y + \frac{1}{2}z + \frac{1}{2}t \right) \cdot \left( \frac{1}{2}, -\frac{1}{2}, \frac{1}{2}, \frac{1}{2} \right) + \left( \frac{1}{\sqrt{ 10 }}x + \frac{2}{\sqrt{ 10 }}y - \frac{1}{\sqrt{ 10 }}z + \frac{2}{\sqrt{ 10 }}t \right) \cdot \left( \frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }}, -\frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }} \right)
\end{align}
$$

En conclusión:
$$
P_{S}(v) = \left( \frac{1}{2}x - \frac{1}{2}y + \frac{1}{2}z + \frac{1}{2}t \right) \cdot \left( \frac{1}{2}, -\frac{1}{2}, \frac{1}{2}, \frac{1}{2} \right) + \left( \frac{1}{\sqrt{ 10 }}x + \frac{2}{\sqrt{ 10 }}y - \frac{1}{\sqrt{ 10 }}z + \frac{2}{\sqrt{ 10 }}t \right) \cdot \left( \frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }}, -\frac{1}{\sqrt{ 10 }}, \frac{2}{\sqrt{ 10 }} \right)
$$

### Parte 2
Determinamos una base ortonormal de $S$:
$$
S = \{ (x, y, z) \in \mathbb{R}^{3} : y - z = 0 \} = \{ (x, y, y) \in \mathbb{R}^{3} : x, y \in \mathbb{R} \} = [\{ (1, 0, 0), (0, 1, 1) \}]
$$
$$
\mathcal{B} = \{ (1, 0, 0), (0, 1, 1) \}
$$
Comprobamos la ortonormalidad:
$$
\langle (1, 0, 0), (0, 1, 1) \rangle = 2 \cdot 0 + 1 + 0 + 4 \cdot 0 + 0 = 1
$$
Como vemos, no son ortogonales, por lo que aplicamos Gram-Schmidt:
$$
\mathcal{B}_{Og} \{ w_{1}, w_{2} \}
$$
$$
w_{1} = (1, 0, 0)
$$
$$
\begin{align}
w_{2} &= (0, 1, 1) - \frac{\langle (0, 1, 1), (1, 0, 0) \rangle}{\langle (1, 0, 0), (1, 0, 0) \rangle} \cdot (1, 0, 0) \\
&= (0, 1, 1) - \frac{1}{2} \cdot (1, 0, 0) \\
&= \left( -\frac{1}{2}, 1, 1 \right)
\end{align}
$$
Determinamos que $||(1, 0, 0)|| = \sqrt{ 2 }$.
$$
|| \left( -\frac{1}{2}, 1, 1 \right) || = \sqrt{ \left\langle \left( -\frac{1}{2}, 1, 1 \right), \left( -\frac{1}{2}, 1, 1 \right) \right\rangle } = \sqrt{ 2 \cdot \frac{1}{4} - \frac{1}{2} - \frac{1}{2} + 4 \cdot 1 + 1 } = \sqrt{ \frac{9}{2} } = \frac{3}{\sqrt{ 2 }}
$$

Finalmente, hallamos la base ortonormal:
$$
\mathcal{B}_{On} = \left\{  \frac{1}{\sqrt{ 2 }} \cdot (1, 0, 0), \frac{\sqrt{ 2 }}{3} \cdot \left( -\frac{1}{2}, 1, 1 \right)  \right\} = \left\{  \left( \frac{1}{\sqrt{ 2 }}, 0, 0 \right), \left( -\frac{\sqrt{ 2 }}{6}, \frac{\sqrt{ 2 }}{3}, \frac{\sqrt{ 2 }}{3} \right)  \right\}
$$

Pasamos a determinar $P_{S}(v)$ con $v = (1, -1, 0)$:
$$
\begin{align}
P_{S}(v) &= \left\langle (1, -1, 0), \left( \frac{1}{\sqrt{ 2 }}, 0, 0 \right) \right\rangle \cdot \left( \frac{1}{\sqrt{ 2 }}, 0, 0 \right) + \left\langle (1, -1, 0), \left( -\frac{\sqrt{ 2 }}{6}, \frac{\sqrt{ 2 }}{3}, \frac{\sqrt{ 2 }}{3} \right) \right\rangle \cdot \left( -\frac{\sqrt{ 2 }}{6}, \frac{\sqrt{ 2 }}{3}, \frac{\sqrt{ 2 }}{3} \right) \\
&= \frac{1}{\sqrt{ 2 }} \cdot \left( \frac{1}{\sqrt{ 2 }}, 0, 0 \right) - \frac{7\sqrt{ 2 }}{6} \cdot \left( -\frac{\sqrt{ 2 }}{6}, \frac{\sqrt{ 2 }}{3}, \frac{\sqrt{ 2 }}{3} \right) \\
&= \left( \frac{1}{2}, 0, 0 \right) - \left( -\frac{7}{18}, \frac{7}{9}, \frac{7}{9} \right) \\
&= \left( \frac{8}{9}, -\frac{7}{9}, -\frac{7}{9} \right)
\end{align}
$$


En conclusión:
$$
P_{S}(v) = \left( \frac{8}{9}, -\frac{7}{9}, -\frac{7}{9} \right)
$$

### Parte 3
Determinamos una base ortonormal de $S$:
$$
S = \{ (x, y, z) \in \mathbb{C}^{3} : x + (1 + i)y - z = 0 \} = \{ (x, y, x + (1 + i)y) \in \mathbb{C}^{3} : x, y \in \mathbb{C} \} = [\{ (1, 0, 1), (0, 1, 1 + i) \}]
$$
Comprobamos la ortonormalidad:
$$
\langle (1, 0, 1), (0, 1, 1 + i) \rangle = 0 + 0 + 1 \cdot (1 - i) = 1 - i \neq 0
$$
Como vemos, no son ortogonales, por lo que aplicamos Gram-Schmidt:
$$
\mathcal{B}_{Og} \{ w_{1}, w_{2} \}
$$
$$
w_{1} = (1, 0, 1)
$$
$$
\begin{align}
w_{2} &= (0, 1, 1 + i) - \frac{\langle (0, 1, 1 + i), (1, 0, 1) \rangle}{\langle (1, 0, 1), (1, 0, 1) \rangle} \cdot (1, 0, 1) \\
&= (0, 1, 1 + i) - \frac{1 + i}{2} \cdot (1, 0, 1) \\
&= \left( -\frac{1 + i}{2}, 1, \frac{1 + i}{2} \right)
\end{align}
$$
Determinamos que $||(1, 0, 1)|| = \sqrt{ 2 }$.
$$
\begin{align}
|| \left( -\frac{1 + i}{2}, 1, \frac{1 + i}{2} \right) || &= \sqrt{ \left\langle \left( -\frac{1 + i}{2}, 1, \frac{1 + i}{2} \right), \left( -\frac{1 + i}{2}, 1, \frac{1 + i}{2} \right) \right\rangle } \\
&= \sqrt{ \left( \frac{-1 - i}{2} \right) \cdot \left( \frac{-1 + i}{2} \right) + 1^{2} + \frac{1 + i}{2} \cdot \frac{1 - i}{2} } \\
&= \sqrt{ \frac{1}{2} + 1 + \frac{1}{2} } \\
&= \sqrt{ 2 }
\end{align}
$$

Finalmente, hallamos la base ortonormal:
$$
\mathcal{B}_{On} = \left\{  \frac{1}{\sqrt{ 2 }} \cdot (1, 0, 1), \frac{1}{\sqrt{ 2 }} \cdot \left( -\frac{1 + i}{2}, 1, \frac{1 + i}{2} \right)  \right\} = \left\{  \left( \frac{1}{\sqrt{ 2 }}, 0, \frac{1}{\sqrt{ 2 }} \right), \left( -\frac{1 + i}{2\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }}, \frac{1 + i}{2\sqrt{ 2 }} \right)  \right\}
$$

Pasamos a determinar $P_{S}(v)$ con $v = (0, 1, i)$:
$$
\begin{align}
P_{S}(v) &= \left\langle (0, 1, i), \left( \frac{1}{\sqrt{ 2 }}, 0, \frac{1}{\sqrt{ 2 }} \right) \right\rangle \cdot \left( \frac{1}{\sqrt{ 2 }}, 0, \frac{1}{\sqrt{ 2 }} \right) + \left\langle (0, 1, i), \left( -\frac{1 + i}{2\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }}, \frac{1 + i}{2\sqrt{ 2 }} \right) \right\rangle \cdot \left( -\frac{1 + i}{2\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }}, \frac{1 + i}{2\sqrt{ 2 }} \right) \\
&= \frac{i}{\sqrt{ 2 }} \cdot \left( \frac{1}{\sqrt{ 2 }}, 0, \frac{1}{\sqrt{ 2 }} \right) - \frac{3 + i}{2\sqrt{ 2 }} \cdot \left( -\frac{1 + i}{2\sqrt{ 2 }}, \frac{1}{\sqrt{ 2 }}, \frac{1 + i}{2\sqrt{ 2 }} \right) \\
&= \left( \frac{i}{2}, 0, \frac{i}{2} \right) - \left( -\frac{1 + 2i}{4}, \frac{3 + i}{4}, \frac{1 + 2i}{4} \right) \\
&= \left( \frac{1}{4} + i, -\frac{3}{4} - \frac{1}{4}i, -\frac{1}{4} \right)
\end{align}
$$


En conclusión:
$$
P_{S}(v) = \left( \frac{1}{4} + i, -\frac{3}{4} - \frac{1}{4}i, -\frac{1}{4} \right)
$$




