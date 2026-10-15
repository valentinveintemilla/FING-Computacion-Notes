# 1 - Teorema de Gerschgorin
## Ejercicio 1
Sabemos que $\mathcal{C}_{i} \cap \mathcal{C}_{j} = \emptyset \qquad (i \neq j)$, lo que significa que todos los discos son disjuntos dos a dos.

Por el teorema de Gerschgorin, si $\lambda$ es valor propio de $A$, entonces pertenece a algún disco $\mathcal{C}_{i}$.

Ahora, si consideramos el segundo punto del teorema, el cual indica que si existe una unión de discos $M = \mathcal{C}_{i_{1}} \cup \dots \cup \mathcal{C}_{i_{m}}$, con $m < n$, la cual es disjunta con la unión de los restantes discos, entonces en $M$ hay exactamente $m$ valores propios de $A$ (lo que no indica que todos sean distintos).

Sin embargo, en este caso, podemos considerar $M = \mathcal{C}_{1}$ como la unión que solo incluye a dicho disco. $M$ es disjunta a la unión del resto de los discos, y por lo tanto en $M = \mathcal{C}_{1}$ hay exactamente un valor propio de $A$. Podemos aplicar el mismo razonamiento con el resto de discos:
$$
\begin{align}
&\mathcal{C}_{1} \cap \mathcal{C}_{2} \cup \mathcal{C}_{3} \cup \dots \cup \mathcal{C}_{n} \implies \mathcal{C}_{1} \text{ contiene exactamente un valor propio} \\
&\mathcal{C}_{2} \cap \mathcal{C}_{1} \cup \mathcal{C}_{3} \cup \dots \cup \mathcal{C}_{n} \implies \mathcal{C}_{2} \text{ contiene exactamente un valor propio} \\
&\vdots \\
&\mathcal{C}_{n} \cap \mathcal{C}_{1} \cup \mathcal{C}_{2} \cup \dots \cup \mathcal{C}_{n - 1} \implies \mathcal{C}_{n} \text{ contiene exactamente un valor propio}
\end{align}
$$

De esta manera, cada disco $\mathcal{C}_{i}$, con $i \in \{ 1, 2, \dots, n \}$ contiene exactamente un valor propio.

Entonces, podemos confirmar que todos los valores propios son diferentes (ya que todos los discos contienen 1 y son disjuntos).

Ahora, para verificar que son reales, basta con confirmar que no puede tener raíces complejas:
Sabemos que como $A \in M_{n}(\mathbb{R})$, sus coeficientes son reales. Por lo tanto, existiera algún valor propio complejo, con la forma $\lambda = a + bi$ (con $b \neq 0$), entonces necesariamente su conjugado $\overset{\_} \lambda = a + bi$ también es valor propio de $A$.

Ahora, como ambos se encuentran asociados al centro $a_{ii}$, se cumple que la distancia de ambos al centro es la misma:
$$
|\lambda - a_{ii}| = |\overset{\_} \lambda - a_{ii}|
$$

Entonces, si $\lambda$ pertenece al disco $\mathcal{C}_{i}$, necesariamente $\overset{\_} \lambda$ también pertenece al mismo disco. Sin embargo, esto es imposible, ya que cada disco contiene exactamente un valor propio. 

En conclusión, como todos los valores propios son raíces del polinomio característico (no al revés), todas las raíces son distintas y reales.

---
## Ejercicio 2
Como se trata de una matriz $2 \times 2$, como máximo pueden haber dos valores propios diferentes. Tenemos que ver si los discos de centro 1 y -1 son disjuntos. En caso de serlo, y sabiendo que cada uno contiene un valor propio (al menos, puede tener más dependiendo de si hay discos que se intersectan), será diagonalizable.

Determinemos los discos de la matriz para ver si la misma es diagonalizable:
$$
\begin{align}
\mathcal{C}_{1} = \left\{ z \in \mathbb{C} : |z - 1| \leq \frac{2}{3} \right\} \\
\mathcal{C}_{2} = \left\{ z \in \mathbb{C} : |z + 1| \leq \frac{3}{2} \right\}
\end{align}
$$

Entonces, sabemos que un valor propio se encuentra en el intervalo $\left[ \frac{1}{3}, \frac{5}{3} \right]$, y el otro se encuentra en $\left[ -\frac{5}{2}, \frac{1}{2} \right]$

Como vemos, $\left[ -\frac{5}{2}, \frac{1}{2} \right] \cap \left[ \frac{1}{3}, \frac{5}{3} \right] = [\frac{1}{3}, \frac{1}{2}]$.

Más en general: la distancia entre los centros es $|1 - (-1)| = 2$, y la suma de sus radios es $\frac{2}{3} + \frac{3}{2} = \frac{13}{6}$. Como la suma de los radios es mayor que la distancia de los centros, los discos no son disjuntos.

Como no son disjuntos, podría suceder que haya una única raíz doble $\lambda \in [\frac{1}{3}, \frac{1}{2}]$. Entonces, si su multiplicidad geométrica no es 2, la matriz no sería diagonalizable.

En conclusión, no podemos confirmar que la matriz es diagonalizable según el Teorema de Gerschgorin, ya que no se cumple la hipótesis de exclusión.

---
## Ejercicio 3
### Parte 1
Verifiquemos si $A$ es diagonalizable aplicando el Teorema de Gerschgorin:
- Determinamos los discos:
$$
\begin{align}
&\mathcal{C}_{1} = \{ z \in \mathbb{C} : |z - 6| \leq 4 \} \\
&\mathcal{C}_{2} = \{ z \in \mathbb{C} : |z - 14| \leq 3 \} \\
&\mathcal{C}_{3} = \{ z \in \mathbb{C} : |z + 9| \leq 5 \} \\
&\mathcal{C}_{4} = \{ z \in \mathbb{C} : |z + 20| \leq 3 \}
\end{align}
$$
Analizamos el intervalo abarcado por cada uno de los discos:
$$
\begin{align}
&\mathcal{C}_{1} \text{: } [2, 10] \\
&\mathcal{C}_{2} \text{: } [11, 17] \\
&\mathcal{C}_{3} \text{: } [-14, -4] \\
&\mathcal{C}_{4} \text{: } [-23, -17]
\end{align}
$$
Como vemos, todos los intervalos son disjuntos: $[-23, -17] \cap [-14, -4] \cap [2, 10] \cap [11, 17] = \emptyset$

Entonces, aplicando el teorema de Gerschgorin, en cada disco habrá exactamente un valor propio de $A$, por lo que todos serán diferentes. En conclusión, la matriz es diagonalizable.

### Parte 2
En base a los intervalos obtenidos, podemos determinar el signo de cada valor propio de $A$: sean $\lambda_{1}, \lambda_{2}, \lambda_{3}, \lambda_{4}$ valores propios de $A$:
$$
\begin{align}
&\lambda_{1} \in [-23, -17] \implies \lambda_{1} < 0 \\
&\lambda_{2} \in [-14, -4] \implies \lambda_{2} < 0 \\
&\lambda_{3} \in [2, 10] \implies \lambda_{3} > 0 \\
&\lambda_{4} \in [11, 17] \implies \lambda_{4} > 0
\end{align}
$$

Como ningún valor propio es 0, la matriz diagonal semejante a $A$ no tendrá filas ni columnas nulas (pudiendo intercambiar el orden de los elementos):
$$
D = \begin{pmatrix}
\lambda_{1} & 0 & 0 & 0 \\
0 & \lambda_{2} & 0 & 0 \\
0 & 0 & \lambda_{3} & 0 \\
0 & 0 & 0 & \lambda_{4}
\end{pmatrix}
$$

Por lo tanto, como no hay filas ni columnas nulas, y se trata de una matriz diagonal, $D$ es invertible, y como $A$ es semejante, entonces también lo es.

---
## Ejercicio 4
### Parte 1
Estudiemos los discos de la matriz $A$:
$$
\begin{align}
&\mathcal{C}_{1} = \left\{  z \in \mathbb{C} : |z - \frac{11}{2}| \leq 3 \right\} \implies \mathcal{C}_{1} \text{: } \left[ \frac{11}{2} - 3, \frac{11}{2} + 3 \right] = \left[ \frac{5}{2}, \frac{17}{2} \right] \\
&\mathcal{C}_{2} = \{ z \in \mathbb{C} : |z| \leq 5 \} \implies \mathcal{C}_{2} \text{: } [-5, 5] \\
&\mathcal{C}_{3} = \{ z \in \mathbb{C} : |z + 7| \leq 1 \} \implies \mathcal{C}_{3} \text{: } [-7 - 1, -7 + 1] = [-8, -6]
\end{align}
$$
Como vemos, $\mathcal{C}_{1} \cap \mathcal{C}_{2} \cap \mathcal{C}_{3} = \emptyset$, pero $\mathcal{C}_{1} \cap \mathcal{C}_{2} = \left[ \frac{5}{2}, 5 \right]$. Entonces, aplicando la hipótesis de exclusión del Teorema de Gerschgorin, podemos asegurar que existe exactamente un valor propio (y como es solo uno, es real), en $\mathcal{C}_{3}$, al cual llamaremos $\lambda_{3} \in [-8, -6]$.

Sin embargo, como $\mathcal{C}_{1} \cap \mathcal{C}_{2} = \left[ \frac{5}{2}, 5 \right]$, pueden darse tres casos:
- $\lambda_{1} \neq \lambda_{2} \in \left[ \frac{5}{2}, 5 \right] (\in \mathbb{R})$: ambas raíces son reales y distintas.
- $\lambda_{1} = \lambda_{2} \in \left[ \frac{5}{2}, 5 \right] (\in \mathbb{R})$: ambas raíces son reales e iguales.
- $\lambda_{1} = \overset{_{}} \lambda_{2} \in \mathbb{C}, \mathrm{Re}(\lambda_{1}) = \mathrm{Re}(\lambda_{2}) \in \left[ \frac{5}{2}, 5 \right], \mathrm{Im}(\lambda_{1}) = -\mathrm{Im}(\lambda_{2})$: ambas raíces son complejas, y como sabemos que si existe un valor propio complejo, entonces su conjugado también es valor propio.

### Parte 2
Estudiemos los discos de la matriz $B$:
$$
\begin{align}
&\mathcal{C}_{1} = \left\{  z \in \mathbb{C} : |z - \frac{11}{2}| \leq 3 \right\} \implies \mathcal{C}_{1} \text{: } \left[ \frac{11}{2} - 3, \frac{11}{2} + 3 \right] = \left[ \frac{5}{2}, \frac{17}{2} \right] \\
&\mathcal{C}_{2} = \{ z \in \mathbb{C} : |z| \leq 3 \} \implies \mathcal{C}_{2} \text{: } [-3, 3] \\
&\mathcal{C}_{3} = \{ z \in \mathbb{C} : |z + 7| \leq 1 \} \implies \mathcal{C}_{3} \text{: } [-7 - 1, -7 + 1] = [-8, -6]
\end{align}
$$
Como vemos, $\mathcal{C}_{1} \cap \mathcal{C}_{2} \cap \mathcal{C}_{3} = \emptyset$, pero $\mathcal{C}_{1} \cap \mathcal{C}_{2} = \left[ \frac{5}{2}, 3 \right]$. Entonces, aplicando la hipótesis de exclusión del Teorema de Gerschgorin, podemos asegurar que existe exactamente un valor propio (y como es solo uno, es real), en $\mathcal{C}_{3}$, al cual llamaremos $\lambda_{3} \in [-8, -6]$.

Sin embargo, como $\mathcal{C}_{1} \cap \mathcal{C}_{2} = \left[ \frac{5}{2}, 3 \right]$, pueden darse tres casos:
- $\lambda_{1} \neq \lambda_{2} \in \left[ \frac{5}{2}, 3 \right] (\in \mathbb{R})$: ambas raíces son reales y distintas.
- $\lambda_{1} = \lambda_{2} \in \left[ \frac{5}{2}, 3 \right] (\in \mathbb{R})$: ambas raíces son reales e iguales.
- $\lambda_{1} = \overset{_{}} \lambda_{2} \in \mathbb{C}, \mathrm{Re}(\lambda_{1}) = \mathrm{Re}(\lambda_{2}) \in \left[ \frac{5}{2}, 3 \right], \mathrm{Im}(\lambda_{1}) = -\mathrm{Im}(\lambda_{2})$: ambas raíces son complejas, y como sabemos que si existe un valor propio complejo, entonces su conjugado también es valor propio.

### Parte 3
No podemos confirmar si alguna de ellas es diagonalizable, ya que la única manera de confirmar que la misma sea diagonalizable es que todos los discos sean disjuntos. Como en este caso los discos $\mathcal{C}_{1} \cap \mathcal{C}_{2}$ no son disjuntos, puede darse que exista una raíz real doble en la intersección de ambos, en cuyo caso, es necesario que la multiplicidad geométrica sea 2. Si no sucede esto último, las matrices no serán diagonalizables. En cualquier otro caso, las matrices son diagonalizables.

ACLARACIÓN:
En este ejercicio, el objetivo era aplicar uno de los resultados demostrados en el práctico anterior: $M$ y $M^{T}$ tienen exactamente los mismos valores propios.
De esta forma, si examinamos la transpuesta de $A$ y $B$ podemos obtener resultados interesantes:
- $A^{T}$: El caso es el mismo, dos de los discos se intersectan, por lo que no podemos confirmar que la matriz sea diagonalizable.
- $B^{T}$: En este caso, todos los discos son disjuntos, lo que confirma que la matriz es diagonalizable.

---
## Ejercicio 5
### Parte 1
$$
\begin{align}
&\mathcal{C}_{1} = \left\{  z \in \mathbb{C} : \left| z - 1 \right| \leq 3 \times 10^{-5} \right\} \\
&\mathcal{C}_{2} = \left\{  z \in \mathbb{C} : \left| z - \frac{1}{2} \right| \leq 7 \times 10^{-5} \right\} \\
&\mathcal{C}_{3} = \left\{  z \in \mathbb{C} : \left| z - \frac{1}{10} \right| \leq 4 \times 10^{-5} \right\}
\end{align}
$$
$$
\begin{align}
&\lambda_{1} \in \left[ 1 - 3 \times 10^{-5}, 1 + 3 \times 10^{-5} \right] \implies \lambda_{1} \sim 1 \\
&\lambda_{2} \in \left[ \frac{1}{2} - 7 \times 10^{-5}, \frac{1}{2} + 7 \times 10^{-5} \right] \implies \lambda_{2} \sim \frac{1}{2} \\
&\lambda_{3} \in \left[ \frac{1}{10} - 4 \times 10^{-5}, \frac{1}{10} + 4 \times 10^{-5} \right] \implies \lambda_{3} \sim \frac{1}{10}
\end{align}
$$

Como los radios son tan pequeños y los centros tienen una distancia considerable (tomando en cuenta los radios), podemos asegurar que cada disco tiene exactamente un valor propio. Por lo tanto, los tres valores propios son diferentes, y la matriz es diagonalizable.

### Parte 2
$$
S^{-1} = \begin{pmatrix}
\frac{1}{\alpha} & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$
$$
\begin{align}
\implies S^{-1}AS &= \begin{pmatrix}
\frac{1}{\alpha} & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
1 & -10^{-5} & 2 \times 10^{-5} \\
4 \times 10^{-5} & \frac{1}{2} & -3 \times 10^{-5} \\
-10^{-5} & 3 \times 10^{-5} & \frac{1}{10}
\end{pmatrix} \cdot \begin{pmatrix}
\alpha & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \\
&= \begin{pmatrix}
\frac{1}{\alpha} & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
\alpha & -10^{-5} & 2 \times 10^{-5} \\
4\alpha \times 10^{-5} & \frac{1}{2} & -3 \times 10^{-5} \\
-\alpha \times 10^{-5} & 3 \times 10^{-5} & \frac{1}{10}
\end{pmatrix} \\
&= \begin{pmatrix}
1 & -\frac{1}{\alpha} \times 10^{-5} & \frac{2}{\alpha} \times 10^{-5} \\
4\alpha \times 10^{-5} & \frac{1}{2} & -3 \times 10^{-5} \\
-\alpha \times 10^{-5} & 3 \times 10^{-5} & \frac{1}{10}
\end{pmatrix}
\end{align}
$$
Determinamos los discos de $S^{-1}AS$:
$$
\begin{align}
&\mathcal{C}_{1} = \left\{  z \in \mathbb{C} : \left| z - 1 \right| \leq \frac{3}{\alpha} \times 10^{-5} \right\} \\
&\mathcal{C}_{2} = \left\{  z \in \mathbb{C} : \left| z - \frac{1}{2} \right| \leq (4\alpha + 3) \times 10^{-5} \right\} \\
&\mathcal{C}_{3} = \left\{  z \in \mathbb{C} : \left| z - \frac{1}{10} \right| \leq (\alpha + 3) \times 10^{-5} \right\}
\end{align}
$$

### Parte 3
Tenemos que estudiar, para que valores de $\alpha$, $\mathcal{C}_{1}$, $\frac{3}{\alpha} \times 10^{-5}$ es lo más pequeño posible, sin interceptarse con $\mathcal{C}_{2}$ (disco más cercano y de radio mayor):

Para que dos discos $\mathcal{C}_1$ y $\mathcal{C}_2$ sean disjuntos (no se intersequen), la distancia entre sus centros $d(c_1, c_2)$ debe ser estrictamente mayor (o igual, en el caso límite de tangencia) que la suma de sus radios: $d(\mathcal{C}_1, \mathcal{C}_2) \geq r_1 + r_2$

En este caso, $d(\mathcal{C}_1, \mathcal{C}_2) = |1 - \frac{1}{2}|$ y  $r_1 + r_2 = \frac{3}{\alpha} \times 10^{-5} + (4\alpha + 3) \times 10^{-5}$

Entonces, la pregunta es: ¿Cuál es el primer valor máximo de $\alpha$ que verifica la desigualdad $\frac{1}{2} \geq \frac{3}{\alpha} \times 10^{-5} + (4\alpha + 3) \times 10^{-5}$?
$$
\begin{align}
\frac{1}{2} &\geq \frac{3}{\alpha} \times 10^{-5} + (4\alpha + 3) \times 10^{-5} \\
\frac{1}{2} &\geq \left( \frac{3}{\alpha} + 4\alpha + 3 \right) \times 10^{-5} \\
50000 &\geq \frac{3}{\alpha} + 4\alpha + 3 \\
0 &\geq 4\alpha - 49997 + \frac{3}{\alpha} \\
0 &\geq 4\alpha^{2} - 49997\alpha + 3
\end{align}
$$

Aplicamos la fórmula cuadrática:
$$
\begin{align}
\alpha &= \frac{49997 \pm \sqrt{ 49997^{2} - 4 \cdot 4 \cdot 3 }}{2 \cdot 4} \\
&= \frac{49997 \pm \sqrt{ 49997^{2} - 48 }}{8}
\end{align}
$$
Como queremos el valor máximo, nos quedamos con
$$
\alpha = \frac{49997 + \sqrt{ 49997^{2} - 48 }}{8} \underbrace{ \sim }_{ < } \frac{2 \cdot 49997}{8} = \frac{49997}{4} = 12500 - \frac{3}{4} = 12499 + \frac{1}{4}
$$

### Parte 4
Ahora, utilizamos el valor de $\lambda$ encontrado (su aproximación), para localizar el valor propio $\lambda_{1}$: $\lambda_{1} \in \mathcal{C}_{1}, \mathcal{C}_{1} \cap (\mathcal{C}_{2} \cup \mathcal{C}_{3}) = \emptyset \implies \lambda_{1} \in \mathbb{R}$

Considerando el valor de $lambda = 12499 + \frac{1}{4}$:
$$
\mathcal{C}_{1} = \left\{  z \in \mathbb{C} : \left| z - 1 \right| \leq \frac{3}{12499 + \frac{1}{4}} \times 10^{-5} \right\}
$$
$$
\frac{3}{12499 + \frac{1}{4}} \times 10^{-5} = \frac{3}{12499 + \frac{1}{4}} \times \frac{1}{100000} = \frac{3}{1249900000 + \frac{100000}{4}} = \frac{3}{1249925000}
$$
De esta forma, podemos acotar muchísimo el intervalo al que pertenece dicho valor propio:
$$
\lambda_{1} \in \left[ 1 - \frac{3}{1249925000}, 1 + \frac{3}{1249925000} \right]
$$

### Parte 5
Para esta parte, tenemos que realizar el mismo desarrollo que en las partes 2, 3, 4 y 5 para los otros dos valores propios: $\lambda_{2}$ y $\lambda_{3}$.

$$
S = \begin{pmatrix}
1 & 0 & 0 \\
0 & \beta & 0 \\
0 & 0 & 1
\end{pmatrix}
$$
$$
S^{-1} = \begin{pmatrix}
1 & 0 & 0 \\
0 & \frac{1}{\beta} & 0 \\
0 & 0 & 1
\end{pmatrix}
$$
$$
\begin{align}
\implies S^{-1}AS &= \begin{pmatrix}
1 & 0 & 0 \\
0 & \frac{1}{\beta} & 0 \\
0 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
1 & -10^{-5} & 2 \times 10^{-5} \\
4 \times 10^{-5} & \frac{1}{2} & -3 \times 10^{-5} \\
-10^{-5} & 3 \times 10^{-5} & \frac{1}{10}
\end{pmatrix} \cdot \begin{pmatrix}
1 & 0 & 0 \\
0 & \beta & 0 \\
0 & 0 & 1
\end{pmatrix} \\
&= \begin{pmatrix}
1 & 0 & 0 \\
0 & \frac{1}{\beta} & 0 \\
0 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
1 & -\beta \times 10^{-5} & 2 \times 10^{-5} \\
4 \times 10^{-5} & \frac{1}{2}\beta & -3 \times 10^{-5} \\
-10^{-5} & 3\beta \times 10^{-5} & \frac{1}{10}
\end{pmatrix} \\
&= \begin{pmatrix}
1 & -\beta \times 10^{-5} & 2 \times 10^{-5} \\
\frac{4}{\beta} \times 10^{-5} & \frac{1}{2} & -\frac{3}{\beta} \times 10^{-5} \\
-10^{-5} & 3\beta \times 10^{-5} & \frac{1}{10}
\end{pmatrix}
\end{align}
$$
Determinamos los discos de $S^{-1}AS$:
$$
\begin{align}
&\mathcal{C}_{1} = \left\{  z \in \mathbb{C} : \left| z - 1 \right| \leq (\beta + 2) \times 10^{-5} \right\} \\
&\mathcal{C}_{2} = \left\{  z \in \mathbb{C} : \left| z - \frac{1}{2} \right| \leq \frac{7}{\beta} \times 10^{-5} \right\} \\
&\mathcal{C}_{3} = \left\{  z \in \mathbb{C} : \left| z - \frac{1}{10} \right| \leq (3\beta + 1) \times 10^{-5} \right\}
\end{align}
$$

Nuevamente, tenemos que encontrar valores de $\beta$ para que el radio $r_{2} = \frac{7}{\beta} \times 10^{-5}$ sea lo más pequeño posible, y aun así sea disjunto al resto.

El disco que tiene más chances de interceptarlo antes es $\mathcal{C}_{3}$, ya que su radio es mayor al de $\mathcal{C}_{1}$: $r_{3} = (3\beta + 1) \times 10^{-5}$

Ahora, comparamos las distancias y los radios, $d(\mathcal{C}_2, \mathcal{C}_3) = |\frac{1}{2} - \frac{1}{10}| = \frac{4}{10}$ y  $r_2 + r_3 = \frac{7}{\beta} \times 10^{-5} + (3\beta + 1) \times 10^{-5} = \left( \frac{7}{\beta} + 3\beta + 1 \right) \times 10^{-5}$

Entonces, para que no haya intersección entre los discos:
$$
\begin{align}
\frac{4}{10} &\geq \left( \frac{7}{\beta} + 3\beta + 1 \right) \times 10^{-5} \\
\frac{4}{10} \cdot 10^{5} &\geq \frac{7}{\beta} + 3\beta + 1 \\
0 &\geq \frac{7}{\beta} + 3\beta + 1 - \frac{4}{10} \cdot 10^{5} \\
0 &\geq \frac{7}{\beta} + 3\beta - 39999 \\
0 &\geq 7 + 3\beta^{2} - 39999\beta \\
0 &\geq 3\beta^{2} - 39999\beta + 7 
\end{align}
$$
Aplicamos la fórmula cuadrática:
$$
\begin{align}
\beta &= \frac{39999 \pm \sqrt{ (-39999)^{2} - 4 \cdot 3 \cdot 7 }}{2 \cdot 3} \\
&= \frac{39999 \pm \sqrt{ (-39999)^{2} - 84 }}{6}
\end{align}
$$
Como queremos el valor máximo, nos quedamos con
$$
\beta = \frac{39999 \pm \sqrt{ (-39999)^{2} - 84 }}{6} \underbrace{ \sim }_{ < } \frac{2 \cdot 39999}{6} = \frac{39999}{3} = 13333
$$
Ahora, utilizamos el valor de $\lambda$ encontrado (su aproximación), para localizar el valor propio $\lambda_{1}$: $\lambda_{2} \in \mathcal{C}_{2}, \mathcal{C}_{2} \cap (\mathcal{C}_{1} \cup \mathcal{C}_{3}) = \emptyset \implies \lambda_{2} \in \mathbb{R}$

Considerando el valor de $\lambda = 13333$:
$$
\mathcal{C}_{2} = \left\{  z \in \mathbb{C} : \left| z - \frac{1}{2} \right| \leq \frac{7}{13333} \times 10^{-5} \right\}
$$
$$
\frac{7}{13333} \times 10^{-5} = \frac{7}{13333} \times \frac{1}{100000} = \frac{7}{1333300000}
$$
De esta forma, podemos acotar muchísimo el intervalo al que pertenece dicho valor propio:
$$
\lambda_{2} \in \left[ \frac{1}{2} - \frac{7}{1333300000}, \frac{1}{2} + \frac{7}{1333300000} \right]
$$

El procedimiento para el valor $\lambda_{3}$ sigue la misma lógica, por lo que no lo desarrollaremos para proseguir con el resto del práctico.

---
## Ejercicio 6
Estudiamos los discos de la matriz $A$:
$$
\begin{align}
&\mathcal{C}_{1} = \left\{ z \in \mathbb{C} : \left| z - 15 - 3i \right| \leq 2  \right\} \\
&\mathcal{C}_{2} = \left\{ z \in \mathbb{C} : \left| z - 7 + 4i \right| \leq 3 \right\} \\
&\mathcal{C}_{3} = \left\{ z \in \mathbb{C} : \left| z + 5 + 5i \right| \leq 3 \right\}
\end{align}
$$
Ahora, analicemos si alguno de los discos se intercepta con el resto:
$$
\begin{align}
&d(\mathcal{C}_{1}, \mathcal{C}_{2}) = |15 + 3i - 7 + 4i| = \sqrt{ (15 - 7)^{2} + (3 + 4)^{2} } = \sqrt{ 64 + 49 } = \sqrt{ 113 } \\
&d(\mathcal{C}_{2}, \mathcal{C}_{3}) = |7 - 4i + 5 + 5i| = \sqrt{ (7 + 5)^{2} + (-4 + 5)^{2} } = \sqrt{ 144 + 1 } = \sqrt{ 145 } \\
&d(\mathcal{C}_{1}, \mathcal{C}_{3}) = |15 + 3i + 5 + 5i| = \sqrt{ (15 + 5)^{2} + (3 + 5)^{2} } = \sqrt{ 400 + 64 } = \sqrt{ 464 }
\end{align}
$$
$$
\begin{align}
&r_{1} + r_{2} = 2 + 3 = 5 \\
&r_{2} + r_{3} = 3 + 3 = 6 \\
&r_{1} + r_{3} = 2 + 3 = 5
\end{align}
$$
De esta forma, podemos ver que:
$$
\begin{align}
&d(\mathcal{C}_{1}, \mathcal{C}_{2}) = \sqrt{ 113 } > \sqrt{ 100 } = 10 > 5 = r_{1} + r_{2} \implies d(\mathcal{C}_{1}, \mathcal{C}_{2}) > r_{1} + r_{2} \implies \mathcal{C}_{1} \cap \mathcal{C}_{2} = \emptyset \\
&d(\mathcal{C}_{2}, \mathcal{C}_{3}) = \sqrt{ 145 } > \sqrt{ 144 } = 12 > 6 = r_{2} + r_{3} \implies d(\mathcal{C}_{2}, \mathcal{C}_{3}) > r_{2} + r_{3} \implies \mathcal{C}_{2} \cap \mathcal{C}_{3} = \emptyset \\
&d(\mathcal{C}_{1}, \mathcal{C}_{3}) = \sqrt{ 464 } > \sqrt{ 441 } = 21 > 5 = r_{1} + r_{3} \implies d(\mathcal{C}_{1}, \mathcal{C}_{3}) > r_{1} + r_{3} \implies \mathcal{C}_{1} \cap \mathcal{C}_{3} = \emptyset
\end{align}
$$
De esta forma, como tenemos tres discos disjuntos, necesariamente cada uno tiene exactamente un valor propio. Por lo tanto, los tres valores propios son diferentes, lo que prueba que la matriz $A$ es diagonalizable.

Ninguno de estos discos incluye al valor 0 real, entonces podemos afirmar que el 0 no es valor propio de la matriz. Esto nos lleva a que la matriz diagonal no tendrá ninguna fila ni columna nula, por lo que será invertible.

Por último, si una matriz únicamente contiene coeficientes reales, para que un complejo sea valor propio, también lo tiene que ser su conjugado. Sin embargo, no es el caso, por lo que los valores propios pueden ser complejos. El único valor propio que podría ser real se encuentra en $\mathcal{C}_{1}$: si estudiamos la traspuesta de $A$, podemos ver que el radio de dicho disco es 3, y como la parte imaginaria del centro es 3, se intersecta a la recta real en el valor 15. Sin embargo, es el único caso en el que sucede esto. En el resto, el radio no es suficiente para compensar la parte imaginaria del centro, y por lo tanto no se intersecta, y mucho menos pasa, del eje real.

ACLARACIÓN:
En realidad, la tercer afirmación es falsa, ya que para que un número sea un valor propio de $A$, debe cumplir simultáneamente las cotas de filas y de columnas. Esto significa que el valor debe pertenecer a la intersección del disco por filas y el disco por columnas.

---
# 2 - Forma de Jordan
## 2.1 - Subespacios invariantes
### Ejercicio 7
#### Parte 1
Si $W_{1}$ y $W_{2}$ son subespacios de $V$ invariantes bajo $T$, significa que
- $u \in W_{1} \implies T(u) \in W_{1}$
- $v \in W_{2} \implies T(v) \in W_{2}$

- $W_{1} \cap W_{2}$
Consideramos $w \in W_{1} \cap W_{2}$. De esta forma, $w \in W_{1} \land w \in W_{2}$.

Como $w \in W_{1} \implies T(w) \in W_{1}$, pero lo mismo pasa para $W_{2}$: $w \in W_{2} \implies T(w) \in W_{2}$.

En conclusión, $T(w) \in W_{1} \land T(w) \in W_{2} \implies T(w) \in W_{1} \cap W_{2}$, por lo que $W_{1} \cap W_{2}$ es un subespacio invariante bajo $T$.

- $W_{1} + W_{2}$
Sabemos que $W_{1} + W_{2} = \{ u + v : u \in W_{1} \land v \in W_{2} \}$
Entonces, consideramos el vector genérico $u + v \in W_{1} + W_{2}$.

Podemos aplicar $T$ a dicho vector: $T(u + v) = T(u) + T(v)$. Como $W_{1}$ y $W_{2}$ son subespacios $T$-invariantes, sabemos que $T(u) \in W_{1}$ y $T(v) \in W_{2}$.

De esta manera, podemos concluir que $T(u) + T(v) \in W_{1} + W_{2}$, lo que prueba que $W_{1} + W_{2}$ es un subespacio invariante bajo $T$.

#### Parte 2
Sabemos que $\lambda$ es valor propio de $T$, lo que significa que para todo $v \in S_{\lambda}, T(v) = \lambda v$.
Sin embargo, como $v \in S_{\lambda}$, entonces $\lambda v = T(v) \in S_{\lambda}$.

Entonces, por definición, el subespacio propio $S_{\lambda}$ es un subespacio invariante bajo $T$.

#### Parte 3
Sabemos que:
- $\lambda$ es valor propio de $T$, entonces existe $S_{\lambda}$ tal que $\forall u \in S_{\lambda}, T(u) = \lambda u$.
- $W = [v_{1}, v_{2}]$, con $v_{1} \in S_{\lambda}$ y $T(v_{2}) = v_{1}$

$\{ v_{1}, v_{2} \}$ es base de $W$.

Como $v_{1} \in S_{\lambda}$, por definición de subespacio propio sabemos que $T(v_{1}) = \lambda v_{1}$, por lo tanto se cumple que $v_{1} \in W$ y $\lambda v_{1} = T(v_{1}) \in W$.

Ahora, sabiendo que $T(v_{2}) = v_{1}$, se cumple que $v_{2} \in W$ y $v_{1} = T(v_{2}) \in W$.

De esta forma, las transformaciones de ambos elementos de la base $\{ v_{1}, v_{2} \}$ pertenecen a $W$. Como $T$ es una transformación lineal, por su característica lineal, las imágenes de todas las combinaciones lineales de $v_{1}$ y $v_{2}$ (que se corresponden con el espacio generado por dicha base, o sea $W$) también pertenecen a $W$: $\forall v \in W, v = \alpha v_{1} + \beta v_{2} \implies T(v) = \alpha T(v_{1}) + \beta T(v_{2})$, y como $T(v_{1}) \in W$ y $T(v_{2}) \in W$, entonces, para todo $\alpha v_{1} + \beta v_{2} \in W, T(\alpha v_{1} + \beta v_{2}) \in W$.

En conclusión $W$ es un subespacio invariante bajo $T$.

#### Parte 4
$W$ es un subespacio de $V$ invariante bajo $T$, por lo que se cumple que $\forall w \in W, T(w) \in W$. Además, $dim(W) = 1$, lo que significa que podemos tomar una base $\{ w \}$ de $W$, de modo que todos los vectores de $W$ se construyen como múltiplos de $w$: $W = [\{ w \}] = \{ \alpha w : \alpha \in \mathbb{K} \}$.

Entonces, como $W = [\{ w \}] = \{ \alpha w : \alpha \in \mathbb{K} \}$ y $\forall w \in W, T(w) \in W$, entonces necesariamente se cumple que $T(w) = \lambda w, \forall w \in W$.

Esto prueba que todos los vectores de $W$ (a excepción del vector nulo), son vectores propios de $T$, ya que $\forall w \in W, T(w) = \alpha w, \alpha \in \mathbb{K}$.

Sin embargo, esto no significa que $W$ sea un subespacio propio de $T$, ya que si el subespacio asociado a $\alpha$ tiene multiplicidad geométrica mayor a 1, $W \subset S_{\alpha}$. Por lo tanto, no será un subespacio propio.

### Parte 5
#### Parte a
Sabemos que
- $\forall w \in W_{1} \implies T(w) \in W_{1}$
- $\forall w \in W_{2} \implies T(w) \in W_{2}$
- $\forall w \in W_{3} \implies T(w) \in W_{3}$

Lo que convendría es probar que con los elementos de los espacios anteriores podemos formar una base de $\mathbb{R}^{3}$.
$$
\begin{align}
&(x, y, z) \in W_{1} \implies x + 2y - z = 0 \implies W_{1} = [\{ (-1, 1, 1), (1, 0, 1) \}] \\
&(x, y, z) \in W_{2} \implies x + y + z = 0 \implies W_{2} = [\{ (1, 0, -1), (1, -1, 0) \}] \\
&(x, y, z) \in W_{3} \implies x + y - 2z = 0 \implies W_{3} = [\{ (1, 1, 1), (1, -1, 0) \}]
\end{align}
$$
No podemos afirmar que los espacios anteriores sean subespacios propios, puesto que para esto deberíamos conocer la transformación.

Sin embargo, como los tres son subespacios invariantes, basta con tomar tres vectores LI y comprobar que:
$$
\begin{align}
(1, 0, 1) \in W_{1} &\implies T(1, 0, 1) = \alpha \cdot (1, 0, 1) \\
(1, 0, -1) \in W_{1} &\implies T(1, 0, -1) = \beta \cdot (1, 0, -1) \\
(1, 1, 1) \in W_{1} &\implies T(1, 1, 1) = \gamma \cdot (1, 1, 1)
\end{align}
$$
A priori, no sabemos si $\alpha \neq \beta \neq \gamma$, pero eso no importa, ya que como estamos trabajando con vectores propios diferentes, y tenemos 3 (que corresponde con $dim(\mathbb{R}^{3}) = 3$). Podemos confirmar que $T$ es diagonalizable.

#### Parte b
- $2T - T^{2} = Id$ en $W_{1}$
$W_{1} = [\{ (-1, 1, 1), (1, 0, 1) \}]$

Si consideramos $v \in W_{1}$ vector propio:
$$
\begin{align}
2T - T^{2} &= Id \\
2T(v) - T^{2}(v) &= Id(v) \\
2T(v) - T(T(v)) &= v \\
2\lambda v - T(\lambda v) &= v \\
2\lambda v - \lambda^{2} v &= v \\
(2\lambda - \lambda^{2})v &= v \implies &2\lambda - \lambda^{2} = 1 \\
&&2\lambda - \lambda^{2} - 1 = 1 \\
&&-\lambda^{2} + 2\lambda - 1 = 0
\end{align}
$$

Aplicamos la fórmula cuadrática:
$$
\begin{align}
\lambda &= \frac{-2 \pm \sqrt{ 2^{2} - 4 \cdot (-1) \cdot (-1) }}{2 \cdot (-1)} \\
&= \frac{-2 \pm \sqrt{ 4 - 4 }}{-2} \\
&= \frac{-2 \pm \sqrt{ 0 }}{-2} \\
&= \frac{-2}{-2} \\
&= 1
\end{align}
$$

Entonces, podemos afirmar que
$$
\begin{align}
&T(-1, 1, 1) = (-1, 1, 1) \\
&T(1, 0, 1) = (1, 0, 1)
\end{align}
$$

- $T = 2Id$ en $W_{2} \cap W_{3}$
$W_{2} \cap W_{3} = [\{ (1, 0, -1) \}]$

De esta forma:
$$
\begin{align}
&T(1, 0, -1) = (2, 0, -2) = 2 \cdot (1, 0, -1)
\end{align}
$$

En conclusión, la transformación $T$ tiene dos valores propios asociados:
- $\lambda = 1$, con multiplicidad algebraica y geométrica igual a 2.
- $\lambda = 2$, con multiplicidad algebraica y geométrica igual a 1.

---
### Ejercicio 8
#### Parte a
Por como se forma la matriz asociada, sabemos que:
$$
\begin{align}
&coord_{\mathcal{E}}(T(1, 0, 0)) = T(1, 0, 0) = (\cos \theta, -\sin \theta, 0) \\
&coord_{\mathcal{E}}(T(0, 1, 0)) = T(0, 1, 0) = (\sin \theta, \cos \theta, 0) \\
&coord_{\mathcal{E}}(T(0, 0, 1)) = T(0, 0, 1) = (0, 0, 1)
\end{align}
$$

Entonces, podemos ver lo siguiente: el subespacio formado por el vector $(0, 0, 1)$ es un subespacio invariante de $T$, ya que:
$$
T(\alpha \cdot (0, 0, 1)) = \alpha \cdot T(0, 0, 1) = \alpha \cdot (0, 0, 1)
$$

#### Parte b
Si analizamos un poco más a fondo este resultado, podemos ver que el subespacio $[(0, 0, 1)]$ no solo es un subespacio invariante de $T$, sino que también es el subespacio propio asociado al valor propio 1, ya que contiene a todos los vectores cuya transformación resulta en si mismos:
$$
\forall (0, 0, \alpha) \in S_{1}, T(0, 0, \alpha) = (0, 0, \alpha)
$$

Realmente, este es el único valor propio, sin considerar valores puntuales de $\theta$.

#### Parte c
REALIZAR EN ALGÚN MOMENTO.

---
## 2.2 - Forma canónica de Jordan
### Ejercicio 9
El procedimiento será:
1. Determinamos las imágenes de los elementos de la base canónica: $\{ (1, 0, 0), (0, 1, 0), (0, 0, 1) \}$
2. Hallar el polinomio característico de la matriz $T - \lambda \cdot \mathbb{I}$
3. Estudiar el subespacio propio asociado a cada valor propio (poniendo énfasis en la coincidencia entre multiplicidad algebraica y geométrica)
4. Si la multiplicidad algebraica y geométrica coinciden para todos los valores propios: la transformación es diagonalizable y su matriz diagonal está conformada por los valores propios repetidos según su multiplicidad.
5. Si la multiplicidad algebraica y geométrica no coinciden para algún: la transformación no es diagonalizable, pero podemos hallar una matriz lo suficientemente simple formada en una base de Jordan.

#### Parte 1
$$
\begin{align}
&T(1, 0, 0) = (0, 1, 1) \\
&T(0, 1, 0) = (-1, 3, 0) \\
&T(0, 0, 1) = (-2, 1, 3)
\end{align}
$$
Entonces, la matriz asociada en la base canónica es:
$$
_\mathcal{C}(T)_{\mathcal{C}} = \begin{pmatrix}
0 & -1 & -2 \\
1 & 3 & 1 \\
1 & 0 & 3
\end{pmatrix}
$$
Estudiamos el determinante $\det(T - \lambda \cdot \mathbb{I})$:
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
-\lambda & -1 & -2 \\
1 & 3 - \lambda & 1 \\
1 & 0 & 3 - \lambda
\end{array} \right| \\
&= (-1 + 2(3 - \lambda)) + (3 - \lambda)(\lambda^{2} - 3\lambda + 1) \\
&= -1 + 6 - 2\lambda + 3\lambda^{2} - 9\lambda + 3 - \lambda^{3} + 3\lambda^{2} - \lambda \\
&= -\lambda^{3} + 6 \lambda^{2} - 12\lambda + 8 \\
&= -(\lambda^{3} - 6 \lambda^{2} + 12\lambda - 8) \\
&= -(\lambda - 2) \cdot (\lambda^{2} - 4\lambda + 4) \\
&= -(\lambda - 2) \cdot (\lambda - 2) \cdot (\lambda - 2) \\
&= -(\lambda - 2)^{3}
\end{align}
$$
Estudiamos la multiplicidad geométrica del valor propio 2, analizando su subespacio propio:
$$
\begin{align}
Ker\left( \begin{pmatrix}
-2 & -1 & -2 \\
1 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix} \right) &= Ker\left( \begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
x + z = 0 \\
y = 0
\end{cases} \implies z = -x
\end{align}
$$
$$
\implies S_{2} = \{ (\alpha, 0, -\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 0, -1) \}]
$$
Como vemos, $ma(2) = 3$, pero $mg(2) = 1$. Por esta razón, la matriz asociada a la transformación en la base de Jordan tiene la siguiente forma, con un único sub-bloque de Jordan de tamaño 3:
$$
_{\mathcal{B}}(T)_{\mathcal{B}} = \begin{pmatrix}
2 & 0 & 0 \\
1 & 2 & 0 \\
0 & 1 & 2
\end{pmatrix}
$$

Ahora, buscamos la base de Jordan en la que está definida la matriz anterior. Sabemos que las columnas de la matriz se corresponden con las coordenadas en la base $\mathcal{B}$ de los vectores de dicha base. Entonces, si consideramos $\mathcal{B} = \{ v_{1}, v_{2}, v_{3} \}$:
$$
\begin{align}
&(2, 1, 0) = coord_{\mathcal{B}}(T(v_{1})) \implies T(v_{1}) = 2v_{1} + v_{2} \\
&(0, 2, 1) = coord_{\mathcal{B}}(T(v_{2})) \implies T(v_{2}) = 2v_{2} + v_{3} \\
&(0, 0, 2) = coord_{\mathcal{B}}(T(v_{3})) \implies T(v_{3}) = 2v_{3}
\end{align}
$$
De esta manera, podemos ver que $v_{3}$ es vector propio asociado al valor propio 2, por lo que podemos considerar $v_{3} = (1, 0, -1)$. Ahora, podemos determinar $v_{2}$:
$$
\begin{align}
T(v_{2}) &= 2v_{2} + v_{3} \\
T(v_{2}) - 2v_{2} &= v_{3} \\
T(v_{2}) - 2Id(v_{2}) &= v_{3} \\
(T - 2Id)(v_{2}) &= v_{3}
\end{align}
$$
Entonces, tenemos que resolver el siguiente sistema:
$$
\begin{align}
\begin{pmatrix}
-2 & -1 & -2 \\
1 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
1 \\
0 \\
-1
\end{pmatrix} &\implies \begin{pmatrix}
-1 & 0 & -1 \\
0 & 0 & 0 \\
0 & -1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
1 \\
0 \\
-1
\end{pmatrix} \\
&\implies \begin{cases}
-x - z = 1 \\
-y = -1
\end{cases} \implies y = 1 \land z = -x - 1
\end{align}
$$
De esta forma, podemos considerar $v_{2} = (1, 1, -2)$

Finalmente, determinamos $v_{1}$:
$$
\begin{align}
T(v_{1}) &= 2v_{1} + v_{2} \\
T(v_{1}) - 2v_{1} &= v_{2} \\
T(v_{1}) - 2Id(v_{1}) &= v_{2} \\
(T - 2Id)(v_{1}) &= v_{2}
\end{align}
$$
Resolvemos el siguiente sistema:
$$
\begin{align}
\begin{pmatrix}
-2 & -1 & -2 \\
1 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
1 \\
1 \\
-2
\end{pmatrix} &\implies \begin{pmatrix}
0 & 0 & 0 \\
0 & 1 & 0 \\
1 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
3 \\
-2
\end{pmatrix} \\
&\implies \begin{cases}
y = 3 \\
x + z = -2
\end{cases} \implies z = -x - 2
\end{align}
$$
De esta forma, podemos considerar $v_{1} = (1, 3, -3)$

En conclusión, una base de Jordan para el operador $T$ es:
$$
\mathcal{B} = \{ (1, 3, -3), (1, 1, -2), (1, 0, -1) \}
$$

#### Parte 2
$$
\begin{align}
&T(1, 0, 0) = (3, 0, 0) \\
&T(0, 1, 0) = (2, 4, 1) \\
&T(0, 0, 1) = (-2, -1, 2)
\end{align}
$$
Entonces, la matriz asociada en la base canónica es:
$$
_\mathcal{C}(T)_{\mathcal{C}} = \begin{pmatrix}
3 & 2 & -2 \\
0 & 4 & -1 \\
0 & 1 & 2
\end{pmatrix}
$$
Estudiamos el determinante $\det(T - \lambda \cdot \mathbb{I})$:
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
3 - \lambda & 2 & -2 \\
0 & 4 - \lambda & -1 \\
0 & 1 & 2 - \lambda
\end{array} \right| \\
&= (3 - \lambda) \cdot ((4 - \lambda)(2 - \lambda) + 1) \\
&= (3 - \lambda) \cdot (\lambda^{2} - 6\lambda + 9) \\
&= (3 - \lambda) \cdot (\lambda - 3) \cdot (\lambda - 3) \\
&= -(\lambda - 3)^{3}
\end{align}
$$
Estudiamos la multiplicidad geométrica del valor propio 3, analizando su subespacio propio:
$$
\begin{align}
Ker\left( \begin{pmatrix}
0 & 2 & -2 \\
0 & 1 & -1 \\
0 & 1 & -1
\end{pmatrix} \right) &= Ker\left( \begin{pmatrix}
0 & 1 & -1 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
0 & 1 & -1 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
y - z = 0
\end{cases} \implies z = y \land x \text{ es libre}
\end{align}
$$
$$
\implies S_{3} = \{ (\alpha, \beta, \beta) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 0, 0), (0, 1, 1) \}]
$$
Como vemos, $ma(3) = 3$, pero $mg(3) = 1$. Por esta razón, la matriz asociada a la transformación en la base de Jordan tiene la siguiente forma, con dos sub-bloques de Jordan, uno de tamaño 1 y otro de tamaño 2:
$$
_{\mathcal{B}}(T)_{\mathcal{B}} = \begin{pmatrix}
3 & 0 & 0 \\
0 & 3 & 0 \\
0 & 1 & 3
\end{pmatrix}
$$

Ahora, buscamos la base de Jordan en la que está definida la matriz anterior. Sabemos que las columnas de la matriz se corresponden con las coordenadas en la base $\mathcal{B}$ de los vectores de dicha base. Entonces, si consideramos $\mathcal{B} = \{ v_{1}, v_{2}, v_{3} \}$:
$$
\begin{align}
&(3, 0, 0) = coord_{\mathcal{B}}(T(v_{1})) \implies T(v_{1}) = 3v_{1} \\
&(0, 3, 1) = coord_{\mathcal{B}}(T(v_{2})) \implies T(v_{2}) = 3v_{2} + v_{3} \\
&(0, 0, 3) = coord_{\mathcal{B}}(T(v_{3})) \implies T(v_{3}) = 3v_{3}
\end{align}
$$
De esta manera, podemos ver que $v_{1}$ y $v_{3}$ son vectores propios asociados al valor propio 3, por lo que podemos considerar $v_{1} = (1, 0, 0)$ y $v_{3} = (0, 1, 1)$. Ahora, podemos determinar $v_{2}$:
$$
\begin{align}
T(v_{2}) &= 3v_{2} + v_{3} \\
T(v_{2}) - 3v_{2} &= v_{3} \\
T(v_{2}) - 3Id(v_{2}) &= v_{3} \\
(T - 3Id)(v_{2}) &= v_{3}
\end{align}
$$
Resolvemos el siguiente sistema:
$$
\begin{align}
\begin{pmatrix}
0 & 2 & -2 \\
0 & 1 & -1 \\
0 & 1 & -1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
1 \\
1
\end{pmatrix} &\implies \begin{pmatrix}
0 & 0 & 0 \\
0 & 1 & -1 \\
0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
1 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
y - z = 1
\end{cases} \implies z = y - 1 \land x \text{ es libre}
\end{align}
$$
De esta forma, podemos considerar $v_{2} = (1, 1, 0)$

En conclusión, una base de Jordan para el operador $T$ es:
$$
\mathcal{B} = \{ (1, 0, 0), (1, 1, 0), (0, 1, 1) \}
$$

#### Parte 3
$$
\begin{align}
&T(1, 0, 0, 0) = (0, -2, 0, 0) \\
&T(0, 1, 0, 0) = (2, 4, 0, 0) \\
&T(0, 0, 1, 0) = (0, 0, 1, 1) \\
&T(0, 0, 0, 1) = (0, 0, 1, 1) \\
\end{align}
$$
Entonces, la matriz asociada en la base canónica es:
$$
_\mathcal{C}(T)_{\mathcal{C}} = \begin{pmatrix}
0 & 2 & 0 & 0 \\
-2 & 4 & 0 & 0 \\
0 & 0 & 1 & 1 \\
0 & 0 & 1 & 1
\end{pmatrix}
$$
Estudiamos el determinante $\det(T - \lambda \cdot \mathbb{I})$:
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
-\lambda & 2 & 0 & 0 \\
-2 & 4 - \lambda & 0 & 0 \\
0 & 0 & 1 - \lambda & 1 \\
0 & 0 & 1 & 1 - \lambda
\end{array} \right| \\
&= (-\lambda) \cdot ((4 - \lambda) \cdot ((1 - \lambda)^{2} - 1)) + 2 \cdot 2((1 - \lambda)^{2} - 1) \\
&= ((1 - \lambda)^{2} - 1) \cdot ((-\lambda) \cdot ((4 - \lambda)) + 4) \\
&= (\lambda^{2} - 2\lambda + 1 - 1) \cdot (\lambda^{2} - 4\lambda + 4) \\
&= (\lambda^{2} - 2\lambda) \cdot (\lambda - 2)^{2} \\
&= \lambda \cdot (\lambda - 2) \cdot (\lambda - 2)^{2} \\
&= \lambda \cdot (\lambda - 2)^{3}
\end{align}
$$
En este caso, obtuvimos 2 valores propios:
- $\lambda = 0$, con multiplicidad algebraica 1.
- $\lambda = 2$, con multiplicidad algebraica 3.

Estudiamos la multiplicidad geométrica del valor propio 0, analizando su subespacio propio:
$$
\begin{align}
Ker\left( \begin{pmatrix}
0 & 2 & 0 & 0 \\
-2 & 4 & 0 & 0 \\
0 & 0 & 1 & 1 \\
0 & 0 & 1 & 1
\end{pmatrix} \right) &= Ker\left( \begin{pmatrix}
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z \\
t
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
y = 0 \\
x = 0 \\
z + t = 0
\end{cases} \implies t = -z
\end{align}
$$
$$
\implies S_{0} = \{ (0, 0, \alpha, -\alpha) : \alpha \in \mathbb{R} \} = [\{ (0, 0, 1, -1) \}]
$$
Como vemos, $mg(0) = ma(0) = 1$.

Pasamos a estudiar el subespacio propio asociado a 2.
$$
\begin{align}
Ker\left( \begin{pmatrix}
-2 & 2 & 0 & 0 \\
-2 & 2 & 0 & 0 \\
0 & 0 & -1 & 1 \\
0 & 0 & 1 & -1
\end{pmatrix} \right) &= Ker\left( \begin{pmatrix}
-1 & 1 & 0 & 0 \\
0 & 0 & -1 & 1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
-1 & 1 & 0 & 0 \\
0 & 0 & -1 & 1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z \\
t
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
-x + y = 0 \\
-z + t = 0
\end{cases} \implies y = x \land t = z
\end{align}
$$
$$
\implies S_{2} = \{ (\alpha, \alpha, \beta, \beta) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 1, 0, 0), (0, 0, 1, 1) \}]
$$
Como vemos, $mg(2) = 2$, pero $ma(2) = 3$. Esto significa que la transformación no es diagonalizable (como $ma(2) - mg(2) = 1$, tenemos que agregar un 1 extra a la matriz diagonal), por lo que continuamos definiendo la forma canónica:
$$
_{\mathcal{B}}(T)_{\mathcal{B}} = \begin{pmatrix}
0 & 0 & 0 & 0\\
0 & 2 & 0 & 0 \\
0 & 0 & 2 & 0 \\
0 & 0 & 1 & 2
\end{pmatrix}
$$

Ahora, buscamos la base de Jordan en la que está definida la matriz anterior. Sabemos que las columnas de la matriz se corresponden con las coordenadas en la base $\mathcal{B}$ de los vectores de dicha base. Entonces, si consideramos $\mathcal{B} = \{ v_{1}, v_{2}, v_{3}, v_{4} \}$:
$$
\begin{align}
&(0, 0, 0, 0) = coord_{\mathcal{B}}(T(v_{1})) \implies T(v_{1}) = (0, 0, 0, 0) \\
&(0, 2, 0, 0) = coord_{\mathcal{B}}(T(v_{2})) \implies T(v_{2}) = 2v_{2} \\
&(0, 0, 2, 1) = coord_{\mathcal{B}}(T(v_{3})) \implies T(v_{3}) = 2v_{3} + v_{4} \\
&(0, 0, 0, 2) = coord_{\mathcal{B}}(T(v_{4})) \implies T(v_{4}) = 2v_{4} \\
\end{align}
$$
De esta manera, podemos ver que $v_{1}$ es vector propio asociado al valor propio 0, y $v_{2}$ y $v_{4}$ son vectores propios asociados al valor 2, por lo que podemos considerar $v_{1} = (0, 0, 1, -1)$, $v_{2} = (1, 1, 0, 0)$ y $v_{4} = (0, 0, 1, 1)$. Ahora, podemos determinar $v_{3}$:
$$
\begin{align}
T(v_{3}) &= 2v_{3} + v_{4} \\
T(v_{3}) - 2v_{3} &= v_{4} \\
T(v_{3}) - 2Id(v_{3}) &= v_{4} \\
(T - 2Id)(v_{3}) &= v_{4}
\end{align}
$$
Entonces, tenemos que resolver el siguiente sistema:
$$
\begin{align}
\begin{pmatrix}
-2 & 2 & 0 & 0 \\
-2 & 2 & 0 & 0 \\
0 & 0 & -1 & 1 \\
0 & 0 & 1 & -1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z \\
t
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
1 \\
1
\end{pmatrix} &\implies \begin{pmatrix}
-1 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & -1 & 1 \\
0 & 0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z \\
t
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
1 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
-x + y = 0 \\
-z + t = 1
\end{cases} \implies y = x \land t = 1 + z
\end{align}
$$
De esta forma, podemos considerar $v_{3} = (1, 1, 1, 2)$

En conclusión, una base de Jordan para el operador $T$ es:
$$
\mathcal{B} = \{ (0, 0, 1, -1), (1, 1, 0, 0), (1, 1, 1, 2), (0, 0, 1, 1) \}
$$

ACLARACIÓN:
Para elegir correctamente los vectores que usaremos para despejar, por ejemplo en el caso de la parte 3 con $v_{4}$, tenemos que asegurarnos de que dicho vector pertenece a la intersección $v_4 \in S_{2} \cap \mathrm{Im}(T - 2Id)$, ya que de esta forma aseguramos que el sistema a resolver no sea incompatible. Por ejemplo, en dicho caso tendríamos que haber elegido $v_{4} = (0, 0, 1, 1)$, y en la parte 2, una combinación de $(1, 0, 0)$ y $(0, 1, 1)$ coherente con el sistema, como por ejemplo $v_{3} = (2, 1, 1)$.

---
### Ejercicio 10
#### Matriz A
$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{cc}
4 - \lambda & -6 \\
2 & -4 - \lambda
\end{array} \right| \\
&= (4 - \lambda) \cdot (-4 - \lambda) + 12 \\
&= \lambda^{2} - 16 + 12 \\
&= \lambda^{2} - 4 \\
&= (\lambda - 2) \cdot (\lambda + 2)
\end{align}
$$
Encontramos dos valores propios:
- $\lambda - 2 = 0 \implies \lambda = 2$
$$
\begin{align}
Ker\left( \begin{pmatrix}
2 & -6 \\
2 & -6
\end{pmatrix} \right) &= Ker\left( \begin{pmatrix}
1 & -3 \\
0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
1 & -3 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y
\end{pmatrix} = \begin{pmatrix}
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
x - 3y = 0
\end{cases} \implies x = 3y
\end{align}
$$
$$
\implies S_{2} = \{ (3\alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (3, 1) \}]
$$

- $\lambda + 2 = 0 \implies \lambda = -2$
$$
\begin{align}
Ker\left( \begin{pmatrix}
6 & -6 \\
2 & -2
\end{pmatrix} \right) &= Ker\left( \begin{pmatrix}
1 & -1 \\
0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
1 & -1 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y
\end{pmatrix} = \begin{pmatrix}
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
x - y = 0
\end{cases} \implies x = y
\end{align}
$$
$$
\implies S_{-2} = \{ (\alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 1) \}]
$$

En realidad, no era necesario efectuar todos los cálculos anteriores, ya que simplemente con ver que teníamos dos valores propios distintos, ya podíamos intuir que la matriz es diagonalizable:
$$
_{\mathcal{B}}(A)_{\mathcal{B}} = \begin{pmatrix}
2 & 0 \\
0 & -2
\end{pmatrix}
$$
Determinamos la base $\mathcal{B}$: $\mathcal{B} = \{ v_{1}, v_{2} \}$
$$
\begin{align}
&(2, 0) = coord_{\mathcal{B}}(T(v_{1})) \implies T(v_{1}) = 2v_{1} \\
&(0, -2) = coord_{\mathcal{B}}(T(v_{2})) \implies T(v_{2}) = -2v_{2}
\end{align}
$$
Entonces, $v_{1}$ es un vector propio asociado al valor propio 2, y $v_{2}$ es un vector propio asociado al valor propio -2. Es así que determinamos $v_{1} = (3, 1)$ y $v_{2} = (1, 1)$ (pudiendo ser cualquiera de los vectores propios de $S_{2}$ y $S_{-2}$): $\mathcal{B} = \{ (3, 1), (1, 1) \}$

#### Matriz C
$$
\begin{align}
\det(C - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{cc}
-\lambda & -1 & -2 \\
1 & 3 - \lambda & 1 \\
1 & 0 & 3 - \lambda
\end{array} \right| \\
&= (-1 + 2(3 - \lambda)) + (3 - \lambda) \cdot (\lambda(\lambda - 3) + 1) \\
&= 5 - 2\lambda + (3 - \lambda) \cdot (\lambda^{2} - 3\lambda + 1) \\
&= 5 - 2\lambda + 3\lambda^{2} - 9\lambda + 3 - \lambda^{3} + 3\lambda^{2} - \lambda \\
&= -\lambda^{3} + 6\lambda^{2} - 12\lambda + 8 \\
&= -(\lambda - 2) \cdot (\lambda^{2} - 4\lambda + 4) \\
&= -(\lambda - 2) \cdot (\lambda - 2) \cdot (\lambda - 2) \\
&= -(\lambda - 2)^{3}
\end{align}
$$
Encontramos un valor propio con multiplicidad algebraica 3:
- $\lambda - 2 = 0 \implies \lambda = 2$
$$
\begin{align}
Ker\left( \begin{pmatrix}
-2 & -1 & -2 \\
1 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix} \right) &= Ker\left( \begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
1 & 0 & 1 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
x + z = 0 \\
y = 0
\end{cases} \implies z = -x
\end{align}
$$
$$
\implies S_{2} = \{ (\alpha, 0, -\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 0, -1) \}]
$$

Como vemos, $ma(2) = 3$, pero $mg(2) = 1$, por lo que $C$ no es diagonalizable. Proseguimos a definir la forma canónica de la matriz:
$$
_{\mathcal{B}}(C)_{\mathcal{B}} = \begin{pmatrix}
2 & 0 & 0 \\
1 & 2 & 0 \\
0 & 1 & 2
\end{pmatrix}
$$
Determinamos la base $\mathcal{B}$: $\mathcal{B} = \{ v_{1}, v_{2}, v_{3} \}$
$$
\begin{align}
&(2, 1, 0) = coord_{\mathcal{B}}(T(v_{1})) \implies T(v_{1}) = 2v_{1} + v_{2} \\
&(0, 2, 1) = coord_{\mathcal{B}}(T(v_{2})) \implies T(v_{2}) = 2v_{2} + v_{3} \\
&(0, 0, 2) = coord_{\mathcal{B}}(T(v_{3})) \implies T(v_{3}) = 2v_{3}
\end{align}
$$
Entonces, $v_{3}$ es un vector propio asociado al valor propio 2. Es así que determinamos $v_{3} = (1, 0, -1)$.

Ahora, calculamos $v_{2}$:
$$
\begin{align}
T(v_{2}) &= 2v_{2} + v_{3} \\
T(v_{2}) - 2v_{2} &= v_{3} \\
T(v_{2}) - 2Id(v_{2}) &= v_{3} \\
(T - 2Id)(v_{2}) &= v_{3}
\end{align}
$$
Entonces, tenemos que resolver el siguiente sistema:
$$
\begin{align}
\begin{pmatrix}
-2 & -1 & -2 \\
1 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
1 \\
0 \\
-1
\end{pmatrix} &\implies \begin{pmatrix}
0 & 0 & 0 \\
0 & 1 & 0 \\
1 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
1 \\
-1
\end{pmatrix} \\
&\implies \begin{cases}
y = 1 \\
x + z = -1
\end{cases} \implies y = 1 \land z = -1 - x
\end{align}
$$
De esta forma, podemos considerar $v_{2} = (1, 1, -2)$

Hacemos lo mismo para $v_{1}$:
$$
\begin{align}
T(v_{1}) &= 2v_{1} + v_{2} \\
T(v_{1}) - 2v_{1} &= v_{2} \\
T(v_{1}) - 2Id(v_{1}) &= v_{2} \\
(T - 2Id)(v_{1}) &= v_{2}
\end{align}
$$
Resolvemos el sistema correspondiente:
$$
\begin{align}
\begin{pmatrix}
-2 & -1 & -2 \\
1 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
1 \\
1 \\
-2
\end{pmatrix} &\implies \begin{pmatrix}
0 & 0 & 0 \\
0 & 1 & 0 \\
1 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
3 \\
-2
\end{pmatrix} \\
&\implies \begin{cases}
y = 3 \\
x + z = -2
\end{cases} \implies y = 3 \land z = -2 - x
\end{align}
$$
De esta forma, podemos considerar $v_{1} = (1, 3, -3)$

En conclusión, una base de Jordan para la matriz $C$ es:
$$
\mathcal{B} = \{ (1, 3, -3), (1, 1, -2), (1, 0, -1) \}
$$

#### Matriz D
$$
\begin{align}
\det(C - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{cc}
3 - \lambda & 2 & -2 \\
0 & 4 - \lambda & -1 \\
0 & 1 & 2 - \lambda
\end{array} \right| \\
&= (3 - \lambda) \cdot ((4 - \lambda) \cdot (2 - \lambda) + 1) \\
&= (3 - \lambda) \cdot (\lambda^{2} - 6\lambda + 9) \\
&= (3 - \lambda) \cdot (\lambda - 3)^{2} \\
&= -(\lambda - 3)^{3}
\end{align}
$$
Encontramos un valor propio con multiplicidad algebraica 3:
- $\lambda - 3 = 0 \implies \lambda = 3$

Esta matriz y valor propio son los obtenidos en el ejercicio 9, parte 2, por lo que la forma canónica de la matriz es:
$$
_{\mathcal{B}}(T)_{\mathcal{B}} = \begin{pmatrix}
3 & 0 & 0 \\
0 & 3 & 0 \\
0 & 1 & 3
\end{pmatrix}
$$
También calculamos una base de Jordan:
$$
\mathcal{B} = \{ (1, 0, 0), (1, 1, 0), (2, 1, 1) \}
$$

---
### Ejercicio 11
En este caso, tenemos que probar la igualdad para todo $n \in \mathbb{N}$, por lo que lo haremos mediante inducción.
- Caso base
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{1} = \begin{pmatrix}
a^{1} & 0 \\
1 \cdot a^{1 - 1} & a^{1}
\end{pmatrix} = \begin{pmatrix}
a & 0 \\
1 \cdot a^{0} & a
\end{pmatrix} = \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}
$$
- Paso inductivo:
Suponemos que se cumple para $n$:
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix}
$$


Queremos probar que se cumple para $n + 1$
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n + 1} = \begin{pmatrix}
a^{n + 1} & 0 \\
(n + 1) \cdot a^{n} & a^{n + 1}
\end{pmatrix}
$$
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n + 1} = \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n}
$$
$$
\begin{align}
\begin{pmatrix}
a^{n + 1} & 0 \\
(n + 1) \cdot a^{n} & a^{n + 1}
\end{pmatrix} &= \begin{pmatrix}
a \cdot a^{n} & 0 \\
a \cdot (n + 1) \cdot a^{n - 1} & a \cdot a^{n}
\end{pmatrix} \\
&= a \cdot \begin{pmatrix}
a^{n} & 0 \\
(n + 1) \cdot a^{n - 1} & a^{n}
\end{pmatrix} \\
&= \begin{pmatrix}
a & 0 \\
0 & a
\end{pmatrix} \cdot \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} + a^{n - 1} & a^{n}
\end{pmatrix} \\
&= \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix} \underbrace{ = }_{ \text{Verificamos} } \begin{pmatrix}
a \cdot a^{n} & 0 \\
a^{n} + a \cdot (n \cdot a^{n - 1}) & a \cdot a^{n}
\end{pmatrix} = \begin{pmatrix}
a^{n + 1} & 0 \\
(n + 1) \cdot a^{n} & a^{n + 1}
\end{pmatrix}
\end{align}
$$

Ahora, comparamos los dos resultados:
$$
\begin{align}
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n + 1} = \begin{pmatrix}
a^{n + 1} & 0 \\
(n + 1) \cdot a^{n} & a^{n + 1}
\end{pmatrix} &\Longleftrightarrow \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix} \\
&\Longleftrightarrow \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{-1} \cdot \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{-1} \cdot  \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix} \\
&\Longleftrightarrow \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix}
\end{align}
$$

De esta forma, como supusimos que
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix}
$$
y llegamos a
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n + 1} = \begin{pmatrix}
a^{n + 1} & 0 \\
(n + 1) \cdot a^{n} & a^{n + 1}
\end{pmatrix} \Longleftrightarrow \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix}
$$
probamos que
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix}, \forall n \in \mathbb{N}
$$

ACLARACIÓN:
La demostración era mucho más sencilla:
- Paso inductivo (o hipótesis inductiva - H.I.):
Suponemos que se cumple para $n$:
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix}
$$


Queremos probar que se cumple para $n + 1$:
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n + 1} = \begin{pmatrix}
a^{n + 1} & 0 \\
(n + 1) \cdot a^{n} & a^{n + 1}
\end{pmatrix}
$$

$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n + 1} = \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} \underbrace{ = }_{ \text{H.I.} } \begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix}
$$
Entonces, desarrollamos el segundo producto:
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix} \cdot \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix} = \begin{pmatrix}
a \cdot a^{n} & 0 \\
a^{n} + a \cdot n \cdot a^{n - 1} & a \cdot a^{n}
\end{pmatrix} = \begin{pmatrix}
a^{n + 1} & 0 \\
(n + 1) \cdot a^{n} & a^{n + 1}
\end{pmatrix}
$$

De esta forma,  probamos que
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n + 1} = \begin{pmatrix}
a^{n + 1} & 0 \\
(n + 1) \cdot a^{n} & a^{n + 1}
\end{pmatrix}
$$
por lo que queda demostrado que
$$
\begin{pmatrix}
a & 0 \\
1 & a
\end{pmatrix}^{n} = \begin{pmatrix}
a^{n} & 0 \\
n \cdot a^{n - 1} & a^{n}
\end{pmatrix}, \forall n \in \mathbb{N}
$$

Entonces, tenemos que aplicar el resultado anterior para calcular
$$
\begin{pmatrix}
3 & 1 \\
-1 & 1
\end{pmatrix}^{10}
$$
Primero, será necesario encontrar la forma canónica de la matriz, así como dos matrices de cambio de base (una matriz $P$ y su inversa $P^{-1}$) con tal de aprovechar la igualdad:
$$
A = P^{-1} J P \implies A^{10} = P^{-1} J^{10} P
$$

HACER EN ALGÚN MOMENTO

---
### Ejercicio 12
Analizamos el polinomio característico de $A$:
$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
2 - \lambda & -2 & 0 \\
1 & a - \lambda & 1 \\
0 & a & 2 - \lambda
\end{array} \right| \\
&= (2 - \lambda) \cdot ((a - \lambda) \cdot (2 - \lambda) - a) + 2(2 - \lambda) \\
&= (2 - \lambda) \cdot (((a - \lambda) \cdot (2 - \lambda) - a) + 2) \\
&= (2 - \lambda) \cdot (\lambda^{2} - (a + 2)\lambda + (a + 2))
\end{align}
$$
Aplicamos la fórmula cuadrática para determinar las raíces del polinomio de segundo grado:
$$
\begin{align}
\lambda &= \frac{(a + 2) \pm \sqrt{ (-(a + 2))^{2} - 4 \cdot 1 \cdot (a + 2) }}{2 \cdot 1} \\
&= \frac{(a + 2) \pm \sqrt{ a^{2} + 4a + 4 - 4a - 8 }}{2} \\
&= \frac{(a + 2) \pm \sqrt{ a^{2} - 4 }}{2}
\end{align}
$$
Ahora, analicemos los casos según los valores de $a$:
- $|a| < 2 \implies -2 < a < 2$:
En este caso, el término de la raíz cuadrada sería negativo, por lo que las raíces restantes serían complejas. De esta manera, como $A$ está conformada por cocientes reales, no sería diagonalizable.

- $|a| = 2$:
En este caso, la raíz $\lambda = 2$ tendría multiplicidad algebraica 3 (para $a = 2$), o 0 sería raíz doble (para $a = -2$, por lo que sería diagonalizable si y solo si la multiplicidad geométrica de los valores propios coincide con la multiplicidad algebraica.

Para $a = 2$:
$$
\begin{align}
\frac{(a + 2) \pm \sqrt{ a^{2} - 4 }}{2} &= \frac{(2 + 2) \pm \sqrt{ 2^{2} - 4 }}{2} \\
&= \frac{4}{2} \\
&= 2
\end{align}
$$
$$
\implies \mathcal{X}_{A}(\lambda) = -(\lambda - 2)^{3}
$$
$$
\begin{align}
Ker \left( \begin{pmatrix}
0 & -2 & 0 \\
1 & 0 & 1 \\
0 & 2 & 0
\end{pmatrix} \right) &= Ker \left( \begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
y = 0 \\
x + z = 0
\end{cases} \implies z = -x
\end{align}
$$
$$
\implies S_{2} = \{ (\alpha, 0, -\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 0, -1) \}]
$$
Como vemos, no es diagonalizable, ya que $mg(2) < ma(2)$. Entonces, expresemos su forma canónica de Jordan, la cual tendrá dos 1s extras, ya que faltan dos vectores propios LI en el subespacio propio para formar una base:
$$
J = \begin{pmatrix}
2 & 0 & 0 \\
1 & 2 & 0 \\
0 & 1 & 2
\end{pmatrix}
$$

Para $a = -2$:
$$
\begin{align}
\frac{(a + 2) \pm \sqrt{ a^{2} - 4 }}{2} &= \frac{(-2 + 2) \pm \sqrt{ (-2)^{2} - 4 }}{2} \\
&= \frac{0}{2} \\
&= 0
\end{align}
$$
$$
\implies \mathcal{X}_{A}(\lambda) = -\lambda^{2} \cdot (\lambda - 2)
$$
$$
\begin{align}
Ker \left( \begin{pmatrix}
0 & -2 & 0 \\
1 & -4 & 1 \\
0 & -2 & 0
\end{pmatrix} \right) &= Ker \left( \begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
y = 0 \\
x + z = 0
\end{cases} \implies z = -x
\end{align}
$$
$$
\implies S_{2} = \{ (\alpha, 0, -\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 0, -1) \}]
$$

$$
\begin{align}
Ker \left( \begin{pmatrix}
2 & -2 & 0 \\
1 & -2 & 1 \\
0 & -2 & 2
\end{pmatrix} \right) &= Ker \left( \begin{pmatrix}
1 & -1 & 0 \\
0 & -1 & 1 \\
0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
1 & -1 & 0 \\
0 & -1 & 1 \\
0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
x - y = 0 \\
-y + z = 0
\end{cases} \implies x = y = z
\end{align}
$$
$$
\implies S_{0} = \{ (\alpha, \alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 1, 1) \}]
$$


Como vemos, no es diagonalizable, ya que $mg(0) < ma(0)$. Entonces, expresemos su forma canónica de Jordan, la cual tendrá un 1 extra, ya que falta un vector propio LI en el subespacio propio para formar una base:
$$
J = \begin{pmatrix}
0 & 0 & 0 \\
1 & 0 & 0 \\
0 & 0 & 2
\end{pmatrix}
$$

- $|a| > 2$:
En este caso, encontraremos dos raíces distintas aparte de $\lambda = 2$ cuando desarrollemos la fórmula cuadrática. Por lo tanto, al tener tres valores propios distintos, la matriz será diagonalizable.

---
### Ejercicio 13
Tenemos que probar que $\exists P \in M_{4 \times 4}$ invertible tal que
$$
A = P^{-1} B P
$$

Por otra parte, también podríamos verificar que cumplen con las condiciones de semejanza entre matrices:
- Tienen igual traza.
- Tienen igual determinante.
- Tienen mismo rango.
- Comparten polinomio característico y valores propios.

Mejor busquemos sus semejantes diagonales o formas de Jordan, para así ser capaces de fácilmente comparar las matrices mediante la definición de semejanza.

$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
2 - \lambda & 0 & 0 & 0 \\
0 & -\lambda & -1 & -1 \\
0 & 1 & 1 - \lambda & 0 \\
0 & 0 & 1 & 2 - \lambda
\end{array} \right| \\
&= (2 - \lambda) \cdot ((-\lambda) \cdot (1 - \lambda) \cdot (2 - \lambda) + (2 - \lambda) - 1) \\
&= (2 - \lambda) \cdot ((-\lambda) \cdot (1 - \lambda) \cdot (2 - \lambda) + (1 - \lambda)) \\
&= (2 - \lambda) \cdot (1 - \lambda) \cdot ((-\lambda) \cdot (2 - \lambda) + 1) \\
&= (2 - \lambda) \cdot (1 - \lambda) \cdot (\lambda^{2} - 2\lambda + 1) \\
&= (2 - \lambda) \cdot (1 - \lambda) \cdot (\lambda - 1)^{2} \\
&= -(2 - \lambda) \cdot (\lambda - 1)^{3}
\end{align}
$$
Analizamos los subespacios de cada valor:
- $2 - \lambda = 0 \implies \lambda = 2$

$$
\begin{align}
Ker \left( \begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & -2 & -1 & -1 \\
0 & 1 & -1 & 0 \\
0 & 0 & 1 & 0
\end{pmatrix} \right) &= Ker \left( \begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z \\
t
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
t = 0 \\
y = 0 \\
z = 0
\end{cases} \implies x \text{ es libre}
\end{align}
$$
$$
\implies S_{2} = \{ (\alpha, 0, 0, 0) : \alpha \in \mathbb{R} \} = [\{ (1, 0, 0, 0) \}]
$$

- $\lambda - 1 = 0 \implies \lambda = 1$
$$
\begin{align}
Ker \left( \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & -1 & -1 & -1 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 1
\end{pmatrix} \right) &= Ker \left( \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z \\
t
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
x = 0 \\
y = 0 \\
z + t = 0
\end{cases} \implies t = -z
\end{align}
$$
$$
\implies S_{1} = \{ (0, 0, \alpha, -\alpha) : \alpha \in \mathbb{R} \} = [\{ (0, 0, 1, -1) \}]
$$

Como vemos, $mg(1) < ma(1)$, por lo que la matriz no es diagonalizable. Determinamos la forma canónica de Jordan:
$$
J_{A} = \begin{pmatrix}
1 & 0 & 0 & 0 \\
1 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 2
\end{pmatrix}
$$

Ahora, hacemos lo mismo con la matriz $B$:
$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
-\lambda & -1 & -1 & 0 \\
1 & 2 - \lambda & 1 & 0 \\
0 & 0 & 1 - \lambda & 0 \\
0 & 0 & 0 & 2 - \lambda
\end{array} \right| \\
&= (2 - \lambda) \cdot (1 - \lambda) \cdot ((-\lambda) \cdot (2 - \lambda) + 1) \\
&= (2 - \lambda) \cdot (1 - \lambda) \cdot (\lambda^{2} - 2\lambda + 1) \\
&= (2 - \lambda) \cdot (1 - \lambda) \cdot (\lambda - 1)^{2} \\
&= -(2 - \lambda) \cdot (\lambda - 1)^{3}
\end{align}
$$
Como vemos, el polinomio característico es exactamente el mismo, así como los valores propios.

Analizamos los subespacios de cada valor:
- $2 - \lambda = 0 \implies \lambda = 2$

$$
\begin{align}
Ker \left( \begin{pmatrix}
-2 & -1 & -1 & 0 \\
1 & 0 & 1 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix} \right) &= Ker \left( \begin{pmatrix}
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
0 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z \\
t
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
y = 0 \\
x = 0 \\
z = 0
\end{cases} \implies t \text{ es libre}
\end{align}
$$
$$
\implies S_{2} = \{ (0, 0, 0, \alpha) : \alpha \in \mathbb{R} \} = [\{ (0, 0, 0, 1) \}]
$$

- $\lambda - 1 = 0 \implies \lambda = 1$
$$
\begin{align}
Ker \left( \begin{pmatrix}
-1 & -1 & -1 & 0 \\
1 & 1 & 1 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix} \right) &= Ker \left( \begin{pmatrix}
1 & 1 & 1 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix} \right) \\
&\implies \begin{pmatrix}
1 & 1 & 1 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z \\
t
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0 \\
0
\end{pmatrix} \\
&\implies \begin{cases}
x + y + z = 0 \\
t = 0
\end{cases} \implies z = -x - y
\end{align}
$$
$$
\implies S_{1} = \{ (\alpha, \beta, -\alpha - \beta, 0) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 0, -1, 0), (0, 1, -1, 0) \}]
$$

Como vemos, $mg(1) < ma(1)$, por lo que la matriz no es diagonalizable. Determinamos la forma canónica de Jordan:
$$
J_{B} = \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 2
\end{pmatrix}
$$

ACLARACIÓN:
En realidad, podemos probar su semejanza considerando uno de los teoremas vistos en el curso: Dos matrices $A$ y $B$ son semejantes si y sólo si poseen exactamente la misma Forma Canónica de Jordan (salvo posible permutación en el orden de los bloques).

Por esta razón, podemos determinar que las matrices $A$ y $B$ no son semejanes, ya que:
$$
J_{A} = \begin{pmatrix}
1 & 0 & 0 & 0 \\
1 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 2
\end{pmatrix} \neq J_{B} = \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 2
\end{pmatrix}
$$

---
### Ejercicio 14
Analicemos cada uno de los puntos presentados:
- Sabemos que el polinomio característico de $T$ tiene todas sus raíces en el cuerpo. No se especifica que sea $\mathbb{R}$ o $\mathbb{C}$, pero en caso de ser $\mathbb{R}$, esto significa que no tiene raíces complejas.

- $(t - 2)^{3}$ divide al polinomio característico, por lo que el polinomio característico factorizado tiene la forma:
$$
(\lambda - 2)^{3} \cdot \dots
$$
De esta manera, sabemos que 2 es raíz del polinomio característico, y valor propio con multiplicidad algebraica 3.

- Si $N(T - 3Id) \neq \{ \vec{0} \}$, entonces existen vectores $v \in V$ que satisfacen:
$$
\begin{align}
N(T - 3Id) \neq \{ \vec{0} \} \implies \exists v \in V \text{ tal que } &(T - 3Id) \cdot v = \vec{0} \\
&T(v) - 3Id(v) = \vec{0} \\
&T(v) - 3v = \vec{0} \\
&T(v) = 3v
\end{align}
$$
De esta manera, 3 es valor propio de $T$.

- La multiplicidad algebraica de 4 es mayor que 1 indica tanto que 4 es valor propio de $T$ (ya que es raíz del polinomio característico y pertenece al cuerpo), sino que su multiplicidad es mayor que 1.

Sabemos que 2 también es valor propio y su multiplicidad algebraica es 3, y 3 es valor propio, pero no conocemos su multiplicidad algebraica. Sin embargo, como el espacio $V$ es de dimensión 6, la matriz asociada es de tamaño $6 \times 6$. Por lo tanto, la transformación tiene asociada 6 valores propios (contando su multiplicidad), de forma que para que 3 sea valor propio, tiene que tener al menos multiplicidad 1, y si la multiplicidad de 4 es mayor que 1, no puede ser 3 (por lo que solo habrían dos valores propios: 2 y 4).

En conclusión, los valores propios son:
- 2 con multiplicidad algebraica 3.
- 3 con multiplicidad algebraica 1.
- 4 con multiplicidad algebraica 2.

De esta manera, podemos determinar que la transformación lineal es diagonalizable, y la matriz diagonal asociada a $T$ es:
$$
\begin{pmatrix}
2 & 0 & 0 & 0 & 0 & 0 \\
0 & 2 & 0 & 0 & 0 & 0 \\
0 & 0 & 2 & 0 & 0 & 0 \\
0 & 0 & 0 & 3 & 0 & 0 \\
0 & 0 & 0 & 0 & 4 & 0 \\
0 & 0 & 0 & 0 & 0 & 4
\end{pmatrix}
$$
Ahora, considerando que las matrices semejantes son aquellas que están asociadas a un mismo operador lineal, y que las mismas tienen igual traza, calculando la traza de la matriz anterior estamos calculando la traza de $T$:
$$
tr(T) = 2 + 2 + 2 + 3 + 4 + 4 = 17
$$
ACLARACIÓN:
La transformación lineal no tiene porque ser diagonalizable, no tenemos la suficiente información como para determinar eso. Sin embargo, no importa porque la traza es equivalente para todas las matrices semejantes, por lo que diagonal o no, la traza será 17 (ya que solo toma en cuenta los elementos de la diagonal).


---
### Ejercicio 15
#### Parte 1
Sabemos como se transforman los elementos de la base $\mathcal{A} = \{ (1, 1, 0), (-1, 0, 1), (0, -1, 1) \}$

Entonces, tenemos que expresar sus coordenadas en la misma base:
$$
\begin{align}
&(2, -2, 0) = 0 \cdot (1, 1, 0) + (-2) \cdot (-1, 0, 1) + 2 \cdot (0, -1, 1) \implies coord_{\mathcal{A}}(2, -2, 0) = (0, -2, 2) \\
&(-6, 2, -4) = (-4) \cdot (1, 1, 0) + 2 \cdot (-1, 0, 1) + (-6) \cdot (0, -1, 1) \implies coord_{\mathcal{A}}(2, -2, 0) = (-4, 2, -6)
\end{align}
$$

De esta forma, la matriz asociada a $T$ en la base correspondiente es:
$$
_{\mathcal{A}}(T)_{\mathcal{A}} = \begin{pmatrix}
0 & 0 & -4 \\
-2 & -2 & 2 \\
2 & 2 & -6
\end{pmatrix}
$$

Calculamos el determinante de $T - \lambda \cdot \mathbb{I}$:
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
-\lambda & 0 & -4 \\
-2 & -2 - \lambda & 2 \\
2 & 2 & -6 - \lambda
\end{array} \right| \\
&= (-\lambda) \cdot ((-2 - \lambda) \cdot (-6 - \lambda) - 4) - 4 \cdot (-4 - 2 \cdot (-2 - \lambda)) \\
&= (-\lambda) \cdot (\lambda^{2} + 2\lambda + 6\lambda + 12 - 4) - 4 \cdot (\cancel{ -4 } + \cancel{ 4 } + 2\lambda) \\
&= (-\lambda) \cdot (\lambda^{2} + 8\lambda + 8) - 4 \cdot (2\lambda) \\
&= -\lambda^{3} - 8\lambda^{2} - 8\lambda - 8\lambda \\
&= -\lambda^{3} - 8\lambda^{2} - 16\lambda \\
&= (-\lambda) \cdot (\lambda^{2} + 8\lambda + 16) \\
&= (-\lambda) \cdot (\lambda + 4)^{2}
\end{align}
$$
Tenemos los siguientes valores propios:
- $\lambda + 4 = 0 \implies \lambda = -4$, $ma(-4) = 2$
$$
Ker \begin{pmatrix}
4 & 0 & -4 \\
-2 & 2 & 2 \\
2 & 2 & -2
\end{pmatrix} = Ker \begin{pmatrix}
1 & 0 & -1 \\
0 & 0 & 0 \\
0 & 1 & 0
\end{pmatrix} \implies \begin{pmatrix}
1 & 0 & -1 \\
0 & 0 & 0 \\
0 & 1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \implies \begin{cases}
x - z = 0 \\
y = 0
\end{cases} \implies z = x
$$
$$
\implies S_{-4} = \{ (\alpha, 0, \alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 0, 1) \}]
$$

- $\lambda = 0$
$$
Ker \begin{pmatrix}
0 & 0 & -4 \\
-2 & -2 & 2 \\
2 & 2 & -6
\end{pmatrix} = Ker \begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
1 & 1 & 0
\end{pmatrix} \implies \begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
1 & 1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix} \implies \begin{cases}
z = 0 \\
x + y = 0
\end{cases} \implies y = -x
$$
$$
\implies S_{0} = \{ (\alpha, -\alpha, 0) : \alpha \in \mathbb{R} \} = [\{ (1, -1, 0) \}]
$$

Como vemos, $ma(0) = mg(0) = 1$, pero $ma(-4) = 2$ y $mg(-4) = 1$. Por lo tanto, $T$ no es diagonalizable.

Procedemos a construir la forma canónica de la transformación:
$$
J = \space _{\mathcal{B}}(T)_{\mathcal{B}} = \begin{pmatrix}
-4 & 0 & 0 \\
1 & -4 & 0 \\
0 & 0 & 0
\end{pmatrix}
$$

Ahora, determinamos la base $\mathcal{B} = \{ v_{1}, v_{2}, v_{3} \}$. En base a las columnas de la matriz, sabemos que:
$$
\begin{align}
&coord_{\mathcal{B}}(T(v_{1})) = (-4, 1, 0) \implies T(v_{1}) = -4v_{1} + v_{2} \\
&coord_{\mathcal{B}}(T(v_{2})) = (0, -4, 0) \implies T(v_{2}) = -4v_{2} \\
&coord_{\mathcal{B}}(T(v_{3})) = (0, 0, 0) \implies T(v_{3}) = \vec{0}
\end{align}
$$
El vector $v_{3}$ es un vector propio asociado al valor propio $0$, por lo que podemos definirlo: $v_{3} = (1, -1, 0)$. Por otro lado, el vector $v_{2}$ es vector propio asociado al valor propio $0$, y considerando la base del subespacio propio: $v_{2} = (1, 0, 1)$.

Finalmente, definimos $v_{1}$:
$$
\begin{align}
T(v_{1}) &= -4v_{1} + v_{2} \\
T(v_{1}) + 4v_{1} &= v_{2} \\
(T + 4Id)(v_{1}) &= v_{2}
\end{align}
$$

$$
\begin{align}
(T + 4Id)(v_{1}) = v_{2} &\implies \begin{pmatrix}
4 & 0 & -4 \\
-2 & 2 & 2 \\
2 & 2 & -2
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
1 \\
0 \\
1
\end{pmatrix} \\
&\implies \begin{pmatrix}
1 & 0 & -1 \\
0 & 0 & 0 \\
0 & 1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y \\
z
\end{pmatrix} = \begin{pmatrix}
\frac{1}{4} \\
0 \\
\frac{1}{4}
\end{pmatrix} \\
&\implies \begin{cases}
x - z = \frac{1}{4} \\
y = \frac{1}{4}
\end{cases} \implies z = x - \frac{1}{4}
\end{align}
$$
De esta forma, podemos considerar $x = 0$: $v_{1} = \left( 0, \frac{1}{4}, -\frac{1}{4} \right)$

Es así que encontramos una base de Jordan:
$$
\mathcal{B} = \left\{ \left( 0, \frac{1}{4}, -\frac{1}{4} \right), (1, 0, 1), (1, -1, 0) \right\}
$$

#### Parte 2
Tenemos dos subespacios invariantes bajo $T$ de dimensión 1: $S_{-4}$ y $S_{0}$

#### Parte 3
No existen subespacios invariantes bajo $T$ de dimensión 2.

ACLARACIÓN:
Podemos formas subespacios invariantes de mayor dimensión considerando la suma de los subespacios propios.

Además, los cálculos no son correctos, ya que cuando obtuvimos los vectores que conforman los subespacios vectoriales, en realidad se trataba de las coordenadas de dichos vectores en la base $\mathcal{A}$, por lo que faltó traducirlos y trabajar con los mismos en lugar de sus coordenadas:
$$
\begin{align}
&coord_{\mathcal{A}}(v_{1}) = (\alpha, 0, \alpha) \implies v_{1} = \alpha \cdot (1, 1, 0) + 0 \cdot (-1, 0, 1) + \alpha \cdot (0, -1, 1) = (\alpha, 0, \alpha) \implies v_{1} = (1, 0, 1) \text{(por ejemplo, justo coincidió)} \\
&coord_{\mathcal{A}}(v_{2}) = (\alpha, -\alpha, 0) \implies v_{2} = \alpha \cdot (1, 1, 0) - \alpha \cdot (-1, 0, 1) + 0 \cdot (0, -1, 1) = (2\alpha, \alpha, \alpha) \implies v_{2} = (2, 1, 1) \text{(por ejemplo)}
\end{align}
$$

