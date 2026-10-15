# Verdadero o falso
## Pregunta 1
$_{\mathcal{A}}(T)_{\mathcal{A}}$ está formada por las coordenadas en la base $\mathcal{A}$ de las imágenes de los elementos de $\mathcal{A}$, mientras que $_{\mathcal{A'}}(T)_{\mathcal{A'}}$ está formada por las coordenadas en la base $\mathcal{A'}$ de las imágenes de los elementos de $\mathcal{A'}$.

Con la explicación antes mencionada, podemos intuir que el enunciado no es verdadero. Sabemos que las matrices son semejantes, ya que representan al mismo operador, pero sus entradas no tienen porque ser iguales.

En conclusión, el enunciado es ==falso==.

---
## Pregunta 2
La afirmación es ==verdadera==, y de hecho fueron dos teoremas demostrados en clase:
Sean $A$ y $B$ dos matrices semejantes, entonces.
- $\det(A) = \det(B)$
- $tr(A) = tr(B)$
- $rango(A) = rango(B)$

Además, $X_{A}(\lambda) = X_{B}(\lambda)$.

---
## Pregunta 3
La afirmación es ==falsa==. Podemos buscar un simple ejemplo:
$$
A = \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \text{ y } B = \begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$
Sus polinomios característicos coinciden: $X_{A}(\lambda) = X_{B}(\lambda) = (1 - \lambda)^{2}$

Sin embargo, la matriz identidad ($A$) solo es semejante a si misma.

---
## Pregunta 4
El enunciado es ==verdadero==, fue otra de las pruebas realizadas en clase: la semejanza es una relación de equivalencia, ya que es:
- Reflexiva: $A \sim A$.
- Simétrica: $A \sim B$ y $B \sim A$.
- Transitiva: $A \sim B \land B \sim C \implies A \sim C$

---
## Pregunta 5
La afirmación es ==falsa==. Si bien coinciden en polinomio característico y valores propios, no tienen porque coincidir en vectores propios, ya que los mismos están dados por $N(T - \lambda \cdot \mathbb{I})$.

---
## Pregunta 6
La afirmación es ==falsa==. Una matriz es diagonalizable si y solo si es semejante a una matriz diagonal.

La forma más sencilla de probarlo es viendo un ejemplo de una matriz diagonal por bloques, y probando que no es diagonalizable. Sabiendo que una matriz diagonal por bloques es diagonalizable únicamente si cada uno de sus bloques individuales es diagonalizable, basta con elegir una para la cual alguno de sus bloques no sea diagonalizable. Por ejemplo:
$$
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 0 \\
0 & 0 & 2
\end{pmatrix}
$$

---
# Múltiple opción
## Ejercicio 1
Tenemos que expresar $_{\mathcal{A'}}(T)_{\mathcal{A'}}$ en base a $_{\mathcal{A}}(T)_{\mathcal{A}}$, y una matriz $P = \space _\mathcal{A}(\text{id})_{\mathcal{A'}}$, por lo que aplicamos la definición de matriz semejante:
$$
_{\mathcal{A'}}(T)_{\mathcal{A'}} = \space _\mathcal{A'}(\text{id})_{\mathcal{A}} \cdot \space _{\mathcal{A}}(T)_{\mathcal{A}} \cdot \space _\mathcal{A}(\text{id})_{\mathcal{A'}}
$$
Sustituyendo por $M$ y $P$ obtenemos:
$$
_{\mathcal{A'}}(T)_{\mathcal{A'}} = P^{-1} \cdot \space M \cdot P
$$

### Opción correcta: B

---
## Ejercicio 2
Aquí, verificamos diferentes propiedades de las matrices semejantes:
- Determinante:
$$
\left| \begin{array}{cc}
1 & 1 \\
0 & 1
\end{array} \right| = 1^{2} = 1, \left| \begin{array}{cc}
1 & 0 \\
0 & 2
\end{array} \right| = 1 \cdot 2 = 2
$$
Como vemos, no conciden los determinantes, por lo que las matrices no son semejantes, y esto implica que no pueden representar a la misma transformación lineal.

### Opción correcta: C

---
## Ejercicio 3
Fácilmente, podemos ver que B y C son verdaderas.

Verifiquemos la D:
$$
\begin{align}
&coord_{\mathcal{A}}(T(v_{1})) = (2, 0, 0, 0) \implies T(v_{1}) = 2v_{1} \\
&coord_{\mathcal{A}}(T(v_{2})) = (1, 2, 0, 0) \implies T(v_{2}) = v_{1} + 2v_{2} \\
&coord_{\mathcal{A}}(T(v_{3})) = (0, 0, 5, 0) \implies T(v_{3}) = 5v_{3} \\
&coord_{\mathcal{A}}(T(v_{4})) = (0, 0, 3, 5) \implies T(v_{4}) = 3v_{3} + 5v_{4}
\end{align}
$$

De esta manera, si consideramos los subespacios $[\{ v_{1}, v_{2} \}]$ y $[\{ v_{3}, v_{4} \}]$, podemos ver que ambos son subespacios $T$-invariantes.

En conclusión, la única opción falsa es la A.

### Opción correcta: A

---
## Ejercicio 4
En base al razonamiento realizado para un ejercicio del cuestionario anterior, podemos afirmar que la única opción correcta es la A, ya que es semejante a una matriz diagonal por bloques (la presentada), pero no puede ser diagonalizada, ya que $\pi$ no se encuentra en el intervalo presentado.

Además, la opción B no tiene sentido, ya que no es lo mismo que se mantenga el módulo de un vector, que sus componentes.

### Opción correcta: A



