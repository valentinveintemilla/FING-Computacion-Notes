# Cuestionario 1 - Matriz asociada, cambio de base y semejanza
## Verdadero o falso
### Pregunta 1
Es ==falso==, ya que no son las filas, sino las columnas de la matriz $_{\mathcal{C}}(T)_{\mathcal{B}}$ las que están determinadas por las coordenadas en la base $\mathcal{C}$ de las imágenes de los vectores de la base $\mathcal{B}$.

---
### Pregunta 2
Es ==falso==. Cuando multiplicamos matrices asociadas, es fundamental chequear que los subíndices sean "compatibles". Además, el orden de las matrices tiene que ser el mismo en el que se aplican las transformaciones

En este caso, el desarrollo correcto sería:
$$
_{\mathcal{D}}(S \circ T)_{\mathcal{B}} = \space _{\mathcal{D}}(S)_{\mathcal{C}} \cdot \space _{\mathcal{C}}(T)_{\mathcal{B}}
$$

---
### Pregunta 3
Es ==falso==, puesto que el producto de dos matrices cambio de base "compatibles" da como resultado una nueva matriz cambio de base:
$$
_{\mathcal{C}}(\text{id})_{\mathcal{B}} \cdot \space _{\mathcal{B}}(\text{id})_{\mathcal{C}} = \space _{\mathcal{C}}(\text{id})_{\mathcal{C}}
$$
El enunciado sería verdadero si se aclarara que $\mathcal{C}$ es la base canónica.

CORRECCIÓN:
Es verdadero, ya que por la regla de la composición:
$$
_{\mathcal{C}}(\text{id})_{\mathcal{B}} \cdot \space _{\mathcal{B}}(\text{id})_{\mathcal{C}} = \space _{\mathcal{C}}(\text{id} \circ \text{id})_{\mathcal{C}} = \space _{\mathcal{C}}(\text{id})_{\mathcal{C}} = \mathbb{I}
$$

---
### Pregunta 4
Es ==verdadero==, ya que las matrices son semejantes:
$$
\exists P \in M_{n}(\mathbb{K}) \text{ tal que } \space _{\mathcal{B}}(T)_{\mathcal{B}} = P^{-1} \cdot \space _{\mathcal{C}}(T)_{\mathcal{C}} \cdot P
$$
La invertibilidad no es una propiedad puntual de la matriz correspondiente, sino del operador $T$. De esta manera, la matriz asociada al mismo es invertible para cualquier base elegida.

---
### Pregunta 5
Es ==falso==, ya que si bien es verdadero que si dos matrices son semejantes, entonces tienen el mismo rango, el recíproco no se cumple. Dos matrices son semejantes únicamente si cumplen con la definición: existe matriz $P$ invertible tal que
$$
A = P^{-1} B P
$$
, o verificando que representan al mismo operador.

---
### Pregunta 6
Para verificarlo, tenemos que chequear que las coordenadas en la base $\mathcal{B}$ de las imágenes de los vectores de la misma base sean las presentadas en las columnas:
$$
\begin{align}
&T(1, 1) = (2, 2) \implies coord_{\mathcal{B}}(2, 2) = (2, 0) \\
&T(1, -1) = (0, 2) \implies coord_{\mathcal{B}}(0, 2) = (1, -1) 
\end{align}
$$
Entonces, la matriz asociada a $T$ en la base $\mathcal{B}$ es:
$$
\begin{pmatrix}
2 & 1 \\
0 & -1
\end{pmatrix}
$$

En conclusión, el enunciado es ==verdadero==.

---
## Múltiple opción
### Ejercicio 1
Básicamente, tenemos que determinar la matriz asociada en las bases correspondientes:
$$
\begin{align}
&T(1, 0, 0) = (1, 0) \implies coord_{\mathcal{C}}(1, 0) = (1, -1) \\
&T(1, 1, 0) = (1, 1) \implies coord_{\mathcal{C}}(1, 1) = (1, 0) \\
&T(1, 1, 1) = (0, 2) \implies coord_{\mathcal{C}}(1, 0) = (0, 2)
\end{align}
$$
De esta manera, la matriz asociada a la transformación $T$ en las bases $\mathcal{B}$ y $\mathcal{C}$ es:
$$
\begin{pmatrix}
1 & 1 & 0 \\
-1 & 0 & 2
\end{pmatrix}
$$

#### Opción correcta: C

---
### Ejercicio 2
Las columnas de dicha matriz de cambio de base están conformadas por las coordenadas en la base $\mathcal{B}$ de los vectores de la base $\mathcal{C}$. Sabiendo que $\mathcal{C} = \{ (1, 0), (0, 1) \}$:
$$
\begin{align}
&coord_{\mathcal{B}}(1, 0) = (-1, 2) \\
&coord_{\mathcal{B}}(0, 1) = (1, -1)
\end{align}
$$
De esta manera:
$$
_{\mathcal{B}}(\text{id})_{\mathcal{C}} = \begin{pmatrix}
-1 & 1 \\
2 & -1
\end{pmatrix}
$$

#### Opción correcta: B

---
### Ejercicio 3
Desarrollamos la igualdad considerando $A = \space _{\mathcal{B}}(T)_{\mathcal{B}}$ y $B = \space _{\mathcal{C}}(T)_{\mathcal{C}}$:
$$
\begin{align}
B &= P^{-1} \cdot A \cdot P \\
_{\mathcal{C}}(T)_{\mathcal{C}} &= P^{-1} \cdot \space _{\mathcal{B}}(T)_{\mathcal{B}} \cdot P
\end{align}
$$
Para que la igualdad se cumple solo si:
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \space _{\mathcal{C}}(id)_{\mathcal{B}} \cdot \space _{\mathcal{B}}(T)_{\mathcal{B}} \cdot \space _{\mathcal{B}}(id)_{\mathcal{C}}
$$
En conclusión, necesariamente $P = \space _{\mathcal{B}}(id)_{\mathcal{C}}$.

#### Opción correcta: A

---
### Ejercicio 4
Sabemos que $T(2, 1) = T(1, 1) + T(1, 0)$ (por la linealidad de la operación), y como $coord_{\mathcal{B}}(T(1, 1)) = (1, 0)$ y $coord_{\mathcal{B}}(T(1, 0)) = (2, 3)$, podemos determinar que:
$$
\begin{align}
T(1, 1) = 1 \cdot (1, 1) + 0 \cdot (1, 0) = (1, 1) \\
T(1, 0) = 2 \cdot (1, 1) + 3 \cdot (1, 0) = (5, 2)
\end{align}
$$
En conclusión:
$$
T(2, 1) = T(1, 1) + T(1, 0) = (1, 1) + (5, 2) = (6, 3)
$$

#### Opción correcta: D

---
# Cuestionario 2 - Núcleo, imagen y teorema de las dimensiones
## Verdadero o falso
### Pregunta 7
Toda transformación lineal (con $dim(V)$ finita) cumple que:
$$
dim(V) = dim(N(T)) + dim(\mathrm{Im}(T))
$$
Sabemos que $dim(V) > dim(W)$. Como podemos ver, $\mathrm{Im}(T)$ es el conjunto imagen de $T$, y no puede contener a $W$ (ya que habrían imágenes fuera del codomínio). De esta manera, en general $\mathrm{Im}(T) \subseteq W$, y en el caso de que la transformación sea sobreyectiva, $\mathrm{Im}(T) = W$. Entonces, podemos confirmar que $dim(\mathrm{Im}(T)) < dim(V)$.

Sabiendo esto, si aplicamos el teorema de las dimensiones, necesariamente
$$
dim(V) = dim(N(T)) + dim(\mathrm{Im}(T)) \implies dim(N(T)) = dim(V) - dim(\mathrm{Im}(T)) \geq dim(V) - dim(W) > 1
$$
En conclusión, como $dim(N(T)) > 1$, $T$ no es inyectiva, ya que para que sea inyectiva necesariamente tiene que cumplir $N(T) = \{ \vec{0} \} \implies dim(N(T)) = 0$.

De esta manera, la afirmación es ==verdadera==.

---
### Pregunta 8
El núcleo de una transformación lineal está compuesto por aquellos vectores que tienen como imagen el vector nulo:
$$
N(T) = \{ v \in V : T(v) = \vec{0} \}
$$
De esta manera, el núcleo de la transformación siempre será el mismo, sin importar las bases que se elijan en el domino y condominio para su representación matricial.

En conclusión, el enunciado es ==falso==.

---
### Pregunta 9
Analicemos las columnas de $A$: dicha matriz está conformada por las coordenadas en la base $\mathcal{C}$ (codominio) de las imágenes de los vectores de la base $\mathcal{B}$ (dominio).

Sabemos que dichos elementos son vectores de $W$ expresados en la base $\mathcal{C}$. Sin embargo, no tienen porque formar una base de $W$, por ejemplo, si $dim(W) > dim(V)$. Esto lo sabemos ya que la cantidad de columnas de la matriz (vectores que tenemos de $W$) se corresponde con la cantidad de vectores que transformamos de $V$ (cardinal de la base $\mathcal{B}$), y en caso de que la dimensión del codominio sea mayor, no tendremos una base de $Im(T)$.

CORRECCIÓN:
El enunciado es ==verdadero==, ya que una de las formas de definir una transformación lineal es como se transforman los elementos de una base del dominio. En este caso, tenemos las imágenes de la base $\mathcal{B}$ expresados como coordenadas de la base $\mathcal{C}$.

No es lo mismo decir que forman una base de $W$, ya que esto no es verdadero, por ejemplo si $dim(W) > dim(V)$.

CORRECCIÓN 2:
Es falsa, ya que los elementos de las columnas no son vectores de $W$, sino elementos de $\mathbb{R}^{m}$. Además, no tiene por qué ser linealmente independientes. La base solo se forma si $rango(A) = n$.

---
### Pregunta 10
Apliquemos el teorema de las dimensiones:
$$
dim(V) = dim(N(T)) + dim(\mathrm{Im}(T)) \implies  4= 2 + dim(\mathrm{Im}(T)) \implies dim(\mathrm{Im}(T)) = 2
$$

Ahora, la dimensión del codominio es $dim(\mathbb{R}^{3}) = 3$, y sabiendo que $\mathrm{Im}(T) \subseteq \mathbb{R}^{3}$, podemos confirmar que $\mathrm{Im}(T) \neq \mathbb{R}^{3}$.

En conclusión, la transformación no es sobreyectiva, y el enunciado es ==falso==.

---
### Pregunta 11
Si $V$ tiene dimensión finita, y $N(T) = \{ \vec{0} \} \implies dim(N(T)) = 0$:
$$
dim(V) = dim(N(T)) + dim(\mathrm{Im}(T)) \implies dim(V) = 0 + dim(\mathrm{Im}(T)) \implies dim(V) = dim(\mathrm{Im}(T))
$$
Además, sabemos que $\mathrm{Im}(T) \subseteq V$, por lo que si $dim(V) = dim(\mathrm{Im}(T))$, la única alternativa es que $\mathrm{Im}(T) = V$.

En conclusión, $T$ es sobreyectiva, por lo que la afirmación es ==verdadera==.

---
### Pregunta 12
Sabemos que el conjunto $\mathrm{Im}(T)$ está compuesto por todos los vectores imágenes de la transformación $T$, y el conjunto $N(T)$ por aquellos vectores del dominio que tienen como imagen el vector nulo. Entonces, si $\mathrm{Im}(T) \subseteq N(T)$, significa que $dim(\mathrm{Im}(T)) \leq dim(N(T))$.

Además, podemos confirmar que todos los vectores que son imagen de alguno, su imagen resulta ser el vector nulo.

De esta manera, si aplicamos la transformación dos veces a un mismo vector, en todos los casos obtendremos el vector nulo.

En conclusión, confirmamos que $T \circ T = 0$, por lo que la afirmación es ==verdadera==.

---
## Múltiple opción
### Ejercicio 5
Por el teorema de las dimensiones, sabemos que
$$
dim(V) = dim(N(T)) + dim(\mathrm{Im}(T))
$$
En este caso, $V = \mathbb{R}^{4}$, por lo que $dim(V) = 4$. De esta manera, $dim(N(T)) + dim(\mathrm{Im}(T)) = 4$.

Por lo tanto, podemos descartar la opción D.

Sabemos que las columnas de la matriz son las imágenes de los vectores de la base canónica de $\mathbb{R}^{4}$.

Si observamos bien, podemos ver que si quitamos dos vectores, el conjunto es LI:
- $(2, 0, 2) = 2 \cdot (1, 0, 1)$.
- $(1, 1, 2) = 1 \cdot (1, 0, 1) + 1 \cdot (0, 1, 1)$.

Entonces, la imagen de $T$ se corresponde con: $[\{ (1, 0, 1), (0, 1, 1) \}]$

De esta manera, $dim(\mathrm{Im}(T)) = 2$.

Entonces, aplicando el teorema de las dimensiones:
$$
4 = dim(N(T)) + 2 \implies dim(N(T)) = 2
$$

#### Opción correcta: B

---
### Ejercicio 6
Exploremos el núcleo de $T$:
$$
\begin{pmatrix}
v_{1} \\
v_{2} \\
v_{3} \\
v_{4}
\end{pmatrix} \in N(T) \Longleftrightarrow \begin{pmatrix}
1 & 2 & 0 & 1 \\
0 & 0 & 1 & 1 \\
1 & 2 & 1 & 2
\end{pmatrix} \cdot \begin{pmatrix}
v_{1} \\
v_{2} \\
v_{3} \\
v_{4}
\end{pmatrix} = \begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix}
$$
$$
\begin{cases}
v_{1} + 2v_{2} + v_{4} = 0 \\
v_{3} + v_{4} = 0 \\
v_{1} + 2v_{2} + v_{3} + 2v_{4} = 0
\end{cases}
$$
En definitiva:
$$
\begin{cases}
v_{1} + 2v_{2} + v_{4} = 0 \\
v_{3} + v_{4} = 0
\end{cases}
\implies v_{1} = -2v_{2} - v_{4} \land v_{3} = -v_{4}
$$
Entonces, $v_{2}$ y $v_{4}$ son parámetros:
$$
N(T) = \{ (-2\alpha - \beta, \alpha, -\beta, \beta), \alpha, \beta \in \mathbb{R} \} = \{ (-2\alpha, \alpha, 0, 0) + (-\beta, 0, -\beta, \beta), \alpha, \beta \in \mathbb{R} \}
$$
De esta manera, determinamos la siguiente base:
$$
N(T) = [\{ (-2, 1, 0, 0), (-1, 0, -1, 1) \}]
$$

#### Opción correcta: D

---
### Ejercicio 7
Básicamente, tenemos que aplicar el teorema de las dimensiones: sabemos que $dim(\mathcal{P}^{3}) = 4$ y como $T$ es sobreyectiva, entonces $\mathrm{Im}(T) = M_{2 \times 2}(\mathbb{R}) \implies dim(\mathrm{Im}(T)) = 4$.

Ahora, aplicando el teorema:
$$
4 = dim(N(T)) + 4 \implies dim(N(T)) = 0
$$

Entonces, $T$ es inyectiva, ya que $N(T) = \{ \vec{0} \}$. En conclusión, como $T$ es inyectiva y sobreyectiva, es un isomorfismo (es biyectiva).

#### Opción correcta: C

---
### Ejercicio 8
Determinemos el núcleo de la transformación:
$$
v \in N(T) \Longleftrightarrow T(v) = 0
$$
$$
T(v) = 0 \implies v' = 0
$$
Las únicas funciones cuya primitiva es 0 son las constantes. De esta manera, la única opción válida es la A.

#### Opción correcta: A


