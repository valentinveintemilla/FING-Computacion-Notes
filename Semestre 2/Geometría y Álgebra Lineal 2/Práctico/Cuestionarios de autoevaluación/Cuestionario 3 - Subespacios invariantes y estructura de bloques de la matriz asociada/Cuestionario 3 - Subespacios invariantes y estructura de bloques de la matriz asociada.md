# Verdadero o falso
## Pregunta 1
Es ==falsa==, ya que el que un espacio $S$ sea $T$-invariante, en realidad significa que $T(v) \in S, \forall v \in S$.

---
## Pregunta 2
$N(T)$ es invariante bajo $T$, ya que $\forall v \in N(T), T(v) = \vec{0}$ y $\vec{0} \in N(T)$ (ya que es un espacio vectorial).

$\mathrm{Im}(T)$ también es invariante bajo $T$, ya que $\forall v \in V, T(v) \in \mathrm{Im}(T)$, pero como $\mathrm{Im}(T) \subseteq V$, también se cumple para cualquier vector en $\mathrm{Im}(T)$.

Por último, un subespacio propio es, por definición, un espacio $T$-invariante.

En conclusión, es ==verdadera==.

---
## Pregunta 3
El enunciado es ==verdadero== por lo siguiente:
Sabemos que la matriz $_{\mathcal{A}}[T]_{\mathcal{A}}$ está compuesta por las coordenadas en la base $\mathcal{A}$ de las imágenes de los vectores de la base $\mathcal{A}$. Entonces, como $\mathcal{A} = \mathcal{A}_{1} \cup \mathcal{A}_{2}$, y $\mathcal{A}_{1}$ es la base de $S$, subespacio $T$-invariante, entonces la unión con $\mathcal{A}_{2}$ no modifica dicha propiedad: las coordenadas de las imágenes de $\mathcal{A}_{1}$ únicamente incluyen elementos de $\mathcal{A}_{1}$ (por ser base de un subespacio $T$-invariante).

Entonces, esto causa que la matriz $_{\mathcal{A}}[T]_{\mathcal{A}}$ esté formada por:
- Un bloque correspondiente a $\mathcal{A}_{1}$ de tamaño $k \times k$.
- Debajo del bloque anterior, un bloque nulo de tamaño $(n - k) \times k$.
- El resto (derecha) formado en base al conjunto $\mathcal{A}_{2}$.

---
## Pregunta 4
Pensemos en la siguiente transformación:
$$
T(x, y) = (x + y, x + y)
$$
Consideremos el subespacio $T$-invariante $S_{1} = [\{ (1, 1) \}]$, pues $T(1, 1) = (2, 2)$.

Un complemento de $S_{1}$ sería $S_{2} = [\{ (1, 0) \}]$. Sin embargo, $T(1, 0) = (1, 1)$, entonces $T(1, 0) \not \in S_{2}$.

Por lo tanto, el enunciado es ==falso==. No cualquier complemento que de como resultado el espacio completo mediante suma directa es $T$-invariante.

---
## Pregunta 5
El enunciado es ==falso==. Es verdadero solo en el caso de que $[\{ v_{k + 1}, \dots, v_{n} \}]$ sea un subespacio $T$-invariante, ya que en caso de que no lo sea, puede ser que haya información necesaria en $B$ que deba ser considerada para poder determinar los vectores (no podríamos determinarlos únicamente con $C$).

En caso de no ser $T$-invariante, la restricción ni siquiera está bien definida, puesto que únicamente podemos definir una restricción de tipo $T |_{W}$, cuando $W$ es un subespacio $T$-invariante. $T |_{W}$ significa que vamos a evaluar la transformación $T$ únicamente utilizando vectores que pertenezcan a $W$.

En este caso, al solo considerar $C$, nos estaríamos perdiendo de información que se encuentre en $B$ (ya que como $W$ puede no ser $T$-invariante, hay imágenes que dan el salto a $S$).

---
## Pregunta 6
En este caso, lo que va a suceder es que la matriz asociada $_{\mathcal{A}}[T]_{\mathcal{A}}$ será diagonal por bloques, algo como:
$$
_{\mathcal{A}}[T]_{\mathcal{A}} = \begin{pmatrix}
A_{1} & O & \dots & O \\
O & A_{2} & \dots & O \\
\vdots & \vdots & \ddots & \vdots \\
O & O & \dots & A_{r}
\end{pmatrix}
$$
Esto se debe a que las coordenadas de la imagen de cada vector de las bases mencionadas no "salen" de dichas bases: se expresan como vectores de sus propias bases (ya que son bases de espacios $T$-invariantes).

De esta manera:
- El determinante de $_{\mathcal{A}}[T]_{\mathcal{A}}$ equivale al producto de los determinantes de $A_{1}, A_{2}, \dots, A_{r}$
- La traza de $_{\mathcal{A}}[T]_{\mathcal{A}}$ equivale a la suma de las trazas de $A_{1}, A_{2}, \dots, A_{r}$
- El polinomio característico de $_{\mathcal{A}}[T]_{\mathcal{A}}$ equivale al producto de los polinomios característicos de $A_{1}, A_{2}, \dots, A_{r}$

De esta manera, concluimos que el enunciado es ==verdadero==.

---
# Múltiple opción
## Ejercicio 1
Tenemos que ver para cual de los subespacios $S$, ocurre que $s \in S$, pero $T(s) \not \in S$:
$$
\begin{align}
&T(1, 0, 0) = (1, 0, 0) \\
&T(0, 0, 1) = (0, 0, 2) \\
&T(0, 1, 0) = (1, 1, 0)
\end{align}
$$
De esta manera, podemos ver que el espacio definido como $[\{ (0, 1, 0) \}]$ no es $T$-invariante, ya que la imagen de $(0, 1, 0) \neq (0, \alpha, 0)$.

### Opción correcta: C

---
## Ejercicio 2
En base al razonamiento realizar para la pregunta 3 del verdadero-falso, podemos afirmar que la matriz de $T$ tiene un bloque nulo de tamaño $3 \times 2$ ($(n - k) \times k$) en la esquina inferior izquierda.

### Opción correcta: A

---
## Ejercicio 3
Sabemos que trabajamos en la base canónica, por lo tanto las coordenadas de la matriz son las coordenadas en la base canónica de las imágenes de los vectores de la base canónica:
$$
\begin{align}
(3, 0) = coord_{\mathcal{C}}(1, 0) \implies T(1, 0) = (3, 0) \\
(1, 3) = coord_{\mathcal{C}}(0, 1) \implies T(0, 1) = (1, 3)
\end{align}
$$
De esta manera, podemos ver que el subespacio formado por $[\{ (1, 0) \}]$ es invariante.

Podemos expresar la transformación como:
$$
T(x, y) = (3x + y, 3y)
$$

Como vemos, no existe un complemento invariante que permita formar el espacio $\mathbb{R}^{2}$ mediante suma directa.

Por lo tanto, la única opción válida es que $[\{ (1, 0) \}]$ es el único subespacio invariante propio.

### Opción correcta: D

---
## Ejercicio 4
Sabemos que $E$ es invariante, ya que la rotación se hace alrededor de dicho eje: su valor nunca cambia.

Por esta razón, nos queda analizar $\Pi$:
Sabemos que la matriz de $T$ es:
$$
\begin{pmatrix}
\cos(\theta) & -\sin(\theta) & 0 \\
\sin(\theta) & \cos(\theta) & 0 \\
0 & 0 & 1
\end{pmatrix}
$$

Podemos ver que como se trata de una rotación con respecto al eje $E$, cualquier transformación aplicada a $(1, 0, 0)$, $(0, 1, 0)$ y cualquiera de sus combinaciones lineales permanece dentro del espacio $\Pi$.
De esta manera, $\Pi$ también es invariante.

Podemos ver que la matriz anterior solo es diagonalizable si $\theta = \pi$, por lo que en realidad, la transformación no es diagonalizable considerando el intervalo de valores de $\theta$.

### Opción correcta: B
