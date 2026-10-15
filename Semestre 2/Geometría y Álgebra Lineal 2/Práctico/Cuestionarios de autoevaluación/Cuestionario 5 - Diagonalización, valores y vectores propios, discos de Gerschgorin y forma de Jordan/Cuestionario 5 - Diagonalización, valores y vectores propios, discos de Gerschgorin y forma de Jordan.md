# Verdadero o falso
## Pregunta 1
El enunciado es ==falso==. Una matriz es diagonalizable, si y solo si todos sus valores propios $\lambda$ cumple que
$$
ma(\lambda) = mg(\lambda)
$$

---
## Pregunta 2
El enunciado es ==verdadero==, puesto que si pudieran formarse por combinación lineal, estarían asociados a alguno de los valores propios de los otros vectores.

---
## Pregunta 3
El enunciado es ==verdadero==, puesto que es la definición general para asegurar que una matriz es diagonalizable. No es diagonalizable si se incumple tanto que $mg(\lambda) \neq ma(\lambda)$ para algún valor propio $\lambda$, o si alguna de las raíces del polinomio característico no se encuentra en el cuerpo.

Si ocurre la primera, igualmente podemos encontrar una forma canónica de Jordan cercana a una matriz diagonal.

---
## Pregunta 4
El enunciado es ==falso==. En caso de que el 0 sea valor propio, la matriz no será invertible, ya que de esta forma se anula el determinante.

---
## Pregunta 5
$A$ y $A^{t}$ son semejantes, por lo que tienen los mismos valores propios. Sin embargo, no tienen porque tener los mismos vectores propios, ya que los vectores propios de $A$ cumplen que $A \cdot v = \lambda \cdot v$, mientras que los que $A^{t}$ cumplen que $A^{t} \cdot u = \lambda \cdot u$, productos que no tienen porque coincidir.

Por lo tanto, el enunciado es ==falso==.

---
## Pregunta 6
El enunciado es ==falso==. Si una matriz es compleja, sabemos que necesariamente todas las raíces del polinomio característico estarán en el cuerpo. Sin embargo, las multiplicidades algebraicas y geométricas pueden no coincidir para algún/os valores propios.

---
## Pregunta 7
El enunciado es ==verdadero==. Por el teorema de Gerschgorin, sabemos que si $\lambda$ es valor propio, entonces necesariamente pertenece a algún disco de Gerschgorin, por lo que pertenece a la unión de todos.

---
## Pregunta 8
El enunciado es ==falso==. En realidad el teorema de Gerschgorin asegura que todo valor propio de $A$ pertenece a la unión de todos los discos de Gerschgorin. Además, establece que si existe una unión de $n$ discos disjuntos con el resto, entonces en dicha unión viven exactamente $n$ valores propios.

---
## Pregunta 9
El enunciado es ==verdadero==, ya que indica que el 0 no es valor propio, puesto que el cero no cumple la desigualdad: $0 > \sum_{j \neq i} |a_{ij}|$.

---
## Pregunta 10
Consideremos $A$ nilpotente. Para que $A$ sea diagonalizable, necesariamente tiene que cumplirse que:
$$
D = P^{-1} A P
$$
Como $A$ es nilpotente, entonces $A^{k} = 0$, para algún $k$, por lo que:
$$
D^{k} = P^{-1} A^{k} P = O
$$
La única matriz diagonal cuyas potencias resultan en la matriz nula, es la matriz nula per se. Entonces, determinamos que necesariamente que:
$$
D = O \implies A = P^{-1} (O) P = O
$$

Sin embargo, llegamos a la matriz nula. Como el enunciado menciona explícitamente matriz no nula, llegamos a la conclusión de que es ==verdadero==.

---
## Pregunta 11
El enunciado es ==verdadero==.

Esto ocurre ya que ambos conceptos están intimamente relacionados con el polinomio característico de la matriz. Al desarrollar este polinomio, el coeficiente del término de segundo mayor grado está directamente relacionado con la traza (la suma de la diagonal), y el término independiente es exactamente el determinante.

---
## Pregunta 12
En este caso, la implicación directa es verdadera:
$$
D = P^{-1} A P \implies A = P D P^{-1}
$$
$$
\begin{align}
A^{2} &= (P D P^{-1})(P D P^{-1}) \\
&= P D (P^{-1}P) D P^{-1} \\
&= P D^{2} P^{-1}
\end{align}
$$
Para el recíproco, basta encontrar un contraejemplo:
$$
\begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}
$$
no es diagonalizable, pero
$$
\begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}^{2} = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix}
$$
sí lo es, y de forma trivial.

De esta manera, el enunciado es ==falso==.

---
# Múltiple opción
## Ejercicio 1
Estudiamos el polinomio característico $\det(A - \lambda \cdot \mathbb{I})$:
$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{cc}
5 - \lambda & 4 \\
1 & 2 - \lambda
\end{array} \right| \\
&= (5 - \lambda) \cdot (2 - \lambda) - 4 \\
&= \lambda^{2} - 7\lambda + 6 \\
&= (\lambda - 1) \cdot (\lambda - 6)
\end{align}
$$
Analizamos el subespacio propio asociado a 6:
$$
\begin{pmatrix}
-1 & 4 \\
1 & -4
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y
\end{pmatrix} = \begin{pmatrix}
0 \\
0
\end{pmatrix} \implies \begin{pmatrix}
1 & -4 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y
\end{pmatrix} = \begin{pmatrix}
0 \\
0
\end{pmatrix} \implies \begin{cases}
x - 4y = 0
\end{cases} \implies x = 4y
$$
$$
\implies S_{6} = \{ (4\alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (4, 1) \}]
$$

### Opción correcta: B

---
## Ejercicio 2
Podemos ver que $ma(2) = 3$, pero $mg(2) = 2$, por lo que la matriz no es diagonalizable, entonces descartamos la opción A.

De esta manera, desarrollamos una matriz de Jordan:
$$
\begin{pmatrix}
2 & 0 & 0 & 0 \\
1 & 2 & 0 & 0 \\
0 & 0 & 2 & 0 \\
0 & 0 & 0 & 5
\end{pmatrix}
$$

### Opción correcta: C

---
## Ejercicio 3
Analizamos los discos de Gerschgorin:
$$
\begin{align}
&\mathcal{C}_{1} = \{ z \in \mathbb{C} : |z - 4| \leq 1 \} \\
&\mathcal{C}_{2} = \{ z \in \mathbb{C} : |z + 3| \leq 2 \} \\
&\mathcal{C}_{3} = \{ z \in \mathbb{C} : |z - 8| \leq 1 \}
\end{align}
$$
Podemos ver que los tres discos son disjuntos. Por lo tanto, aplicando el enunciado del teorema de Gerschgorin que afirma que si tomamos una unión de $n$ discos disjunta al resto, ahí se encuentran exactamente $n$ valores propios. Como los tres son disjuntos entre si, cada uno posee exactamente un valor propio. Por lo tanto deben ser reales, puesto que si fueran complejos, también estaría su conjugado y habría más de uno por disco.

Sin embargo, no podemos afirmar cuales son, solo sabemos que son 3 diferentes, por lo que la matriz es diagonalizable. Además, el 0 no puede ser valor propio, ya que no se encuentra en ninguno de los discos.

### Opción correcta: B

---
## Ejercicio 4
Sabemos que $ma(\lambda) = 6$, mientras que $mg(\lambda) = 3$. De esta forma, tendremos que agregar 3 1s a la forma canónica de Jordan. Corroboremos las formas propuestas:
$$
\begin{pmatrix}
\lambda & 0 & 0 & 0 & 0 & 0 \\
1 & \lambda & 0 & 0 & 0 & 0 \\
0 & 1 & \lambda & 0 & 0 & 0 \\
0 & 0 & 0 & \lambda & 0 & 0 \\
0 & 0 & 0 & 1 & \lambda & 0 \\
0 & 0 & 0 & 0 & 0 & \lambda
\end{pmatrix}
$$
Podría ser.
$$
\begin{pmatrix}
\lambda & 0 & 0 & 0 & 0 & 0 \\
1 & \lambda & 0 & 0 & 0 & 0 \\
0 & 0 & \lambda & 0 & 0 & 0 \\
0 & 0 & 1 & \lambda & 0 & 0 \\
0 & 0 & 0 & 0 & \lambda & 0 \\
0 & 0 & 0 & 0 & 1 & \lambda
\end{pmatrix}
$$
Podría ser.
$$
\begin{pmatrix}
\lambda & 0 & 0 & 0 & 0 & 0 \\
1 & \lambda & 0 & 0 & 0 & 0 \\
0 & 1 & \lambda & 0 & 0 & 0 \\
0 & 0 & 0 & \lambda & 0 & 0 \\
0 & 0 & 0 & 1 & \lambda & 0 \\
0 & 0 & 0 & 0 & 1 & \lambda
\end{pmatrix}
$$
No podría ser.
$$
\begin{pmatrix}
\lambda & 0 & 0 & 0 & 0 & 0 \\
1 & \lambda & 0 & 0 & 0 & 0 \\
0 & 1 & \lambda & 0 & 0 & 0 \\
0 & 0 & 1 & \lambda & 0 & 0 \\
0 & 0 & 0 & 0 & \lambda & 0 \\
0 & 0 & 0 & 0 & 0 & \lambda
\end{pmatrix}
$$
Podría ser.

Entonces, nos quedamos con las opciones A, B y C.

Tenemos que entender lo siguiente:
$$
Ker(A - \lambda \cdot \mathbb{I})^{1} \subset Ker(A - \lambda \cdot \mathbb{I})^{2} \subset \dots \subset Ker(A - \lambda \cdot \mathbb{I})^{k}
$$

- $d_{1} = dim(Ker(A - \lambda \cdot \mathbb{I})^{1}) = 3$ indica la cantidad de sub-bloques de Jordan.
- $d_{2} - d_{1}$ indica la cantidad de sub-bloques de tamaño $\geq 2$.
- $d_{3} - d_{2}$ indica la cantidad de sub-bloques de tamaño $\geq 3$.
- $d_{k} - d_{k - 1}$ indica la cantidad de sub-bloques de tamaño $\geq k$.

Ahora, consideramos la información que disponemos: $d_{1} = 3 = mg(\lambda)$, $d_{2} = 5$ y $d_{3} = 6 = ma(\lambda)$. Entonces:
- Tenemos 3 sub-bloques de Jordan (pudiendo ser las opciones A, B y D).
- $d_{2} - d_{1} = 5 - 3 = 2$: Tenemos 2 sub-bloques de Jordan de tamaño $\geq 2$.
- $d_{3} - d_{2} = 6 - 5 = 1$: Tenemos 1 sub-bloque de Jordan de tamaño $\geq 3$.

Si hay dos bloques que miden $\geq 2$ y son exactamente 3, entonces el restante necesariamente mide $1 \times 1$. Por otra parte, tenemos 2 bloques que miden $\geq 2$ y uno que mide $\geq 3$, entonces hay exactamente uno que mide $2 \times 2$.

En conclusión, el restante mide exactamente $3 \times 3$, ya que de esta manera cumplimos con la suma total: $3 + 2 + 1 = 6$. Entonces, los tamaños correctos de los bloques de Jordan asociados a $\lambda$ son 3, 2, 1.

### Opción correcta: A

---
## Ejercicio 5
D ya es diagonal, así que la descartamos.

Probemos en cada caso:
$$
\begin{align}
\det(A - \lambda \cdot I) &= \left| \begin{array}{cc}
1 - \lambda & 2 \\
2 & 1 - \lambda
\end{array} \right| \\
&= (1 - \lambda)^{2} - 4 \\
&= \lambda^{2} - 2\lambda - 3 \\
&= (\lambda - 3) \cdot (\lambda + 1)
\end{align}
$$
Tenemos dos valores propios diferentes, ambos con $ma(\lambda) = 1$. Por lo tanto, es diagonalizable.

$$
\begin{align}
\det(B - \lambda \cdot I) &= \left| \begin{array}{cc}
1 - \lambda & 1 \\
0 & 2 - \lambda
\end{array} \right| \\
&= (1 - \lambda) \cdot (2 - \lambda)
\end{align}
$$
Nuevamente, tenemos dos valores propios diferentes. Por lo que es diagonalizable.

$$
\begin{align}
\det(A - \lambda \cdot I) &= \left| \begin{array}{cc}
3 - \lambda & 0 \\
1 & 3 - \lambda
\end{array} \right| \\
&= (3 - \lambda)^{2}
\end{align}
$$
Ahora, verifiquemos la multiplicidad geométrica de $\lambda = 3$:
$$
\begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y
\end{pmatrix} = \begin{pmatrix}
0 \\
0
\end{pmatrix} \implies \begin{cases}
x = 0
\end{cases} \implies y \text{ es libre}
$$
$$
\implies S_{3} = \{ (0, \alpha) : \alpha \in \mathbb{R} \} = [\{ (0, 1) \}]
$$
Como vemos, $ma(3) = 2 > mg(3) = 1$. Por lo tanto, la matriz no es diagonalizable.

### Opción correcta: C

---
## Ejercicio 6

### Opción correcta: C
