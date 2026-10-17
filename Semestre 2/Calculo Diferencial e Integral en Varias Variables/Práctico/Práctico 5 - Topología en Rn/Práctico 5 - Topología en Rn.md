# 1 - Ejercicios del práctico
## Ejercicio 1
### Conjunto $A_{1}$:
El conjunto $A_{1}$ se representa en $\mathbb{R}^{2}$ como:
![[Semestre 2/Calculo Diferencial e Integral en Varias Variables/Práctico/Práctico 5 - Topología en Rn/Imágenes/Ejercicio 1 - Conjunto A1.png]]

Como vemos, el conjunto está acotado, ya que existe $K > 0$ tal que $A_{1} \subset B(0, K)$. Por ejemplo, podemos considerar $K = 4$.

Determinamos interior ($\mathring{A_{1}}$), frontera ($\partial A_{1}$), puntos de acumulación ($A_{1}'$) y clausura ($\overline{A_{1}}$):
$$
\begin{align}
\mathring{A_{1}} &= \{ (x, y) \in \mathbb{R}^{2} : 1 < x < 2 \land 1 < y < 3 \} \\
\partial A_{1} &= \{ (x, y) \in \mathbb{R}^{2} : (x \in \{ 1, 2 \} \land 1 \leq y \leq 3) \lor (y \in \{ 1, 3 \} \land 1 \leq x \leq 2) \} \\
A_{1}' &= \mathring{A_{1}} \cup \partial A_{1} \\
\overline{A_{1}} &= A_{1} \cup \partial A_{1} = A_{1}' = \{ (x, y) \in \mathbb{R}^{2} : 1 \leq x \leq 2 \land 1 \leq y \leq 3 \}
\end{align}
$$

Finalmente, clasificamos cada conjunto:
- $A_{1}$ es abierto, ya que no incluye a todos sus puntos de acumulación. Por lo tanto, no es cerrado ni compacto.
- $\mathring{A_{1}}$ es abierto, ya que no incluye a su frontera (en realidad, el interior de un conjunto es el conjunto abierto más pequeño contenido en el conjunto). Por lo tanto, no es cerrado ni compacto.
- $\partial A_{1}$ es cerrado, ya que contiene a toda su frontera. Además, como es acotado (ya que $A$ es acotado), es compacto.
- $A_{1}'$ es cerrado, ya que consiste en $A_{1}$ agregando todos los puntos de acumulación (o frontera) faltantes. Además, como es acotado, es compacto.
- $\overline{A_{1}}$ es cerrado, ya que es equivalente a $A_{1}'$. Además, como es acotado, es compacto.

### Conjunto $B = A_{1} \cap \mathbb{Q}$:
El conjunto $B$ se representa en $\mathbb{R}^{2}$ como:
![[Semestre 2/Calculo Diferencial e Integral en Varias Variables/Práctico/Práctico 5 - Topología en Rn/Imágenes/Ejercicio 1 - Conjunto B.png]]

Como vemos, el conjunto está acotado, ya que existe $K > 0$ tal que $B \subset B(0, K)$. Por ejemplo, podemos considerar $K = 4$ (como en el caso anterior).

Determinamos interior ($\mathring{B}$), frontera ($\partial B$), puntos de acumulación ($B'$) y clausura de $\overline{B}$:
$$
\begin{align}
\mathring{B} &= \emptyset \\
\partial B &= \{ (x, y) \in \mathbb{R}^{2} : 1 \leq x \leq 2 \land 1 \leq y \leq 3 \} \\
B' &= \partial B \\
\overline{B} &= B \cup \partial B = B' = \{ (x, y) \in \mathbb{R}^{2} : 1 \leq x \leq 2 \land 1 \leq y \leq 3 \}
\end{align}
$$

Finalmente, clasificamos cada conjunto:
- $B$ no es cerrado (no incluye a toda su frontera) ni abierto (no todos sus puntos son interiores). Por lo tanto, tampoco es compacto.
- $\mathring{B}$ es abierto y cerrado a la vez, pues su complemento es abierto y cerrado.
- $\partial B$ es cerrado, ya que contiene a toda su frontera. Además, como es acotado (ya que $B$ es acotado), es compacto.
- $B'$ es cerrado y compacto, ya que es igual a $\partial B$.
- $\overline{B}$ es cerrado y compacto, ya que es equivalente a $B'$.

### Conjunto $A_{2}$:
El conjunto $A_{2}$ se representa en $\mathbb{R}^{2}$ como:
![[Semestre 2/Calculo Diferencial e Integral en Varias Variables/Práctico/Práctico 5 - Topología en Rn/Imágenes/Ejercicio 1 - Conjunto A2.png]]

Como vemos, el conjunto no está acotado, ya que para todo $K > 0$ se verifica que $B \not \subset B(0, K)$.

Determinamos interior ($\mathring{A_{2}}$), frontera ($\partial A_{2}$), puntos de acumulación ($A_{2}'$) y clausura de $\overline{A_{2}}$:
$$
\begin{align}
\mathring{A_{2}} &= \emptyset \\
\partial A_{2} &= A_{2} \\
A_{2}' &= A_{2} \\
\overline{A_{2}} &= A_{2} \cup \partial A_{2} = A_{2}
\end{align}
$$

Finalmente, clasificamos cada conjunto:
- $A_{2}$ es cerrado, ya que contiene a toda su frontera, pero no es compacto.
- $\mathring{A_{2}}$ es abierto y cerrado a la vez, pues su complemento es abierto y cerrado.
- $\partial A_{2}$ es cerrado pero no compacto, ya que es igual a $A_{2}$.
- $A_{2}'$ es cerrado pero no compacto, ya que es igual a $A_{2}$.
- $\overline{A_{2}}$ es cerrado pero no compacto, ya que es igual a $A_{2}$.

### Conjunto $A_{3}$:
El conjunto $A_{3}$ se representa en $\mathbb{R}^{2}$ como:
![[Semestre 2/Calculo Diferencial e Integral en Varias Variables/Práctico/Práctico 5 - Topología en Rn/Imágenes/Ejercicio 1 - Conjunto A3.png]]

Como vemos, el conjunto está acotado, ya que existe $K > 0$ tal que $B \subset B(0, K)$. Por ejemplo, podemos considerar $K = 1$ (como en el caso anterior).

Determinamos interior ($\mathring{A_{3}}$), frontera ($\partial A_{3}$), puntos de acumulación ($A_{3}'$) y clausura de $\overline{A_{3}}$:
$$
\begin{align}
\mathring{A_{3}} &= A_{3} \\
\partial A_{3} &= \{ (x, y) \in \mathbb{R}^{2} : x^{2} + y^{2} = 1 \} \cup (0, 0) \\
A_{3}' &= A_{3} \cup \partial A_{3} \\
\overline{A_{3}} &= A_{3} \cup \partial A_{3} = A_{3}'
\end{align}
$$

Finalmente, clasificamos cada conjunto:
- $A_{3}$ es abierto, ya que no contiene a toda su frontera, por lo que tampoco es compacto.
- $\mathring{A_{3}}$ es abierto, ya que es igual a $A_{3}$.
- $\partial A_{3}$ es cerrado, ya que contiene a toda su frontera, y es compacto.
- $A_{3}'$ es cerrado y compacto, ya que es igual a $\partial A_{3}$.
- $\overline{A_{3}}$ es cerrado y compacto, ya que es igual a $\partial A_{3}$.

---
## Ejercicio 2
### Parte a
Sea $B(a, \delta) = \{ x \in \mathbb{R}^{n} : d(x, a) < \delta \}$ una bola abierta genérica, tenemos que probar que todos los puntos de $B(a, \delta)$ son interiores. Para esto, consideramos un punto genérico $p \in B(a, \delta)$, y determinemos una bola $B(p, \delta')$ tal que $B(p, \delta') \subset B(a, \delta)$. El problema consiste encontrar el valor de $\delta'$:

Sabemos que $\delta'$ puede ser como máximo la distancia de $p$ al borde de la bola $B(a, \delta)$, puesto que si fuera mayor, la bola $B(p, \delta')$ tendría elementos fuera de $B(a, \delta)$ y no se cumpliría la inclusión. Entonces, necesariamente $d(p, a) + \delta' \leq \delta$, por lo que podemos considerar $\delta' = \delta - d(p, a)$.

Verifiquemos que el $\delta'$ elegido satisface la inclusión: consideramos un punto genérico $x \in B(p, \delta')$ y comprobemos que efectivamente se encuentra en $B(a, \delta)$. Para esto, utilizaremos la desigualdad triangular:
$$
\underbrace{ d(a, x) \leq d(a, p) + d(p, x) }_{ \text{Desigualdad triangular} } < d(a, p) + \delta' = \delta
$$

En conclusión, como se verifica $d(a, x) < \delta$, comprobamos que $\forall x \in B(p, \delta')$ se cumple que $x \in B(a, \delta)$, por lo que necesariamente $B(p, \delta') \subset B(a, \delta)$.

### Parte b
Sabemos que $A$ es abierto, lo que significa que todos los puntos de $A$ son interiores: $\forall x \in A$, $\exists \delta \in \mathbb{R}^{+}$ tal que $B(x, \delta) \subset A$. Como $p \in A$, entonces $\exists \delta \in \mathbb{R}^{+}$ tal que $B(p, \delta) \subset A$.

Tenemos que probar que el conjunto $A - p$ mantiene también es abierto, lo que implica que quitar un punto (o una cantidad finita de puntos) de un conjunto abierto no afecta a su calidad de abierto:
Sea $x \in A - p$. Queremos probar que $\exists \delta \in \mathbb{R}^{+}$ tal que $B(x, \delta) \subset A$. Basta considerar un $\delta$ que verifique que:
$$
\begin{align}
&p \not \in B(x, \delta) \\
&B(x, \delta) \subset A
\end{align} \implies B(x, \delta) \subset A - \{ p \}
$$

Por esta razón, es importante establecer un $\delta$ que sea el mínimo entre la distancia de $x$ a $p$, y la distancia al borde más cercano de $A$. Podemos aprovechar que $A$ es abierto para determinar dicha distancia, sabiendo que $x \in A - p \subset A \implies x \in A$. Entonces, existe una distancia "segura" al borde más cercano $\delta'$, tal que $B(x, \delta') \subset A$.

Habiendo dicho esto, podemos considerar $\delta = \min \{ d(x, p), \delta' \}$. Por construcción, sabemos que se verifican las dos condiciones mencionadas:
- Como $\delta \leq \delta'$, podemos confirmar que $B(x, \delta) \subset A$.
- Como $\delta \leq d(x, p)$, podemos confirmar que $p \not \in B(x, \delta)$.
Entonces, se verifica $B(x, \delta) \subset A - \{ p \}$.

En conclusión, $A - p$ también es abierto.

---
## Ejercicio 3
$A \subset \mathbb{R}^{2}$ abierto y $C = A \cap (\mathbb{Q} \times \mathbb{Q})$. Entonces, analicemos $C$:

$A$ es abierto, por lo que todos los elementos son interiores. Como $C$ únicamente está formado por racionales, excluye a los irracionales. De esta forma, por la densidad de dichos conjuntos, sabemos que para cualquier $c \in C$, se verifica que $\forall \delta > 0, B(c, \delta) \cap C \neq \emptyset \land B(c, \delta) \cap C^{C} \neq \emptyset$. Entonces, determinamos que todos los puntos del conjunto son frontera.

De esta manera:
$$
\begin{align}
\mathring{C} &= \emptyset \\
\partial C &= C \\
\overline{C} &= \mathring{C} \cup \partial C = C
\end{align}
$$

---
## Ejercicio 4
### Parte a
Tenemos que probar que:
$$
\forall a \in A, \exists \delta > 0 \text{ tal que } B(a, \delta) \subset A \implies \forall a + b \in A + B, \exists \delta' > 0 \text{ tal que } B(a + b, \delta') \subset A + B
$$

Consideramos $a \in A$, $b \in B$, tal que $a + b \in A + B$. Como $A$ es abierto, sabemos que todos sus puntos son interiores: $\exists \delta > 0$ tal que $B(a, \delta) \subset A$.

Supongamos que $A + B$ no es abierto. Entonces, existe $a + b$ tal que $\forall \delta' > 0$, $B(a + b, \delta') \cap (A + B)^{c} \neq 0$. Por lo tanto, $a + b$ es frontera de $A + B$.

La pregunta es, ¿podemos extraer información del $a$ y $b$ que conforman $a + b$?

No tenemos información del conjunto $B$ por lo que $b$ podría ser interior o frontera, pero $a$ debe ser interior por hipótesis.

Consideremos $b$ frontera de $B$. Si consideramos $a$ interior de $A$, entonces existe una bola para la cual $a$ está completamente rodeado de puntos de $A$, los cuales también tienen la cualidad de ser internos. Entonces, dicha cualidad se traslada a los puntos formados $a + b$, siendo también interiores de $A + B$. De esta manera, es necesario considerar $a$ frontera para conformar un $a + b$ frontera de $A + B$.

Sin embargo, esto rompe con la hipótesis establecida. La asunción que nos llevó a está incoherencia es el considerar que $A + B$ no es abierto.

En conclusión, $A + B$ es abierto.

---
## Ejercicio 5
### Parte a
$$
A \text{ es abierto } \Longleftrightarrow A \cap \partial A = \emptyset
$$
$(\implies)$ Como $A$ es abierto, todos los elementos de $A$ son interiores: $\forall a \in A$, $\exists \delta > 0$ tal que $B(a, \delta) \subset A$

Entonces, se cumple que $A = \mathring{A}$. Como todos los elementos son interiores, significa que no hay puntos frontera en $A$, todos pertenecen al complemento. Considerando $A = \mathring{A}$, y sabiendo que $\mathring{A} \cap \partial A = \emptyset$ en todos los casos, entonces:
$$
A \text{ es abierto } \implies A \cap \partial A = \emptyset
$$

$(\impliedby)$ Sabemos que $A \cap \partial A = \emptyset$. Como $\partial A$ es el conjunto de puntos frontera de $A$, entonces $A$ no contiene puntos frontera (si $a \in A$, entonces $a \not \in \partial A$, por lo que $a$ es necesariamente interior, $\forall a \in A$). Sabiendo que los puntos de un conjunto pueden ser interiores, frontera o exteriores, y los exteriores pertenecen al complemento, entonces deducimos que todos los puntos de $A$ son interiores. En conclusión, por definición determinamos que $A$ es abierto:
$$
A \cap \partial A = \emptyset \implies A \text{ es abierto }
$$

### Parte b
$$
\mathring{A} = \overline{A} - \partial A \text{ es un conjunto abierto}
$$
Tenemos que probar que todos los puntos de $\mathring{A}$ son interiores:
$$
\forall a \in \mathring{A}, \exists \delta > 0 \text{ tal que } B(a, \delta) \subset \mathring{A}
$$
De esta forma, $a \in \mathring{A}$ verifica que:
- $a \in \overline{A}$
- $a \not \in \partial A$

Como $a$ no es frontera, pero pertenece a la clausura $\overline{A}$ (conjunto conformado por los puntos interiores y frontera de $A$), entonces necesariamente es interior, por lo que verifica: $\exists \delta > 0$ tal que $B(a, \delta) \subset \mathring{A}$.

En conclusión, $\mathring{A}$ es abierto.

### Parte c
$$
A \text{ es cerrado } \Longleftrightarrow \partial A \subset A \Longleftrightarrow A' \subset A
$$
Estudiamos el primer sii:
$$
A \text{ es cerrado } \Longleftrightarrow \partial A \subset A
$$
$(\implies)$ Como $A$ es cerrado, entonces su complemento es abierto. Esto significa que $A^{C} = \mathring{A^{C}}$, por lo que todos los puntos de $A^{C}$ son interiores.

Sabiendo que $A$ y $A^{C}$ comparten su frontera, si todos los puntos de $A^{C}$ son interiores, entonces toda la frontera pertenece a $A$.

Por lo tanto:
$$
A \text{ es cerrado } \implies \partial A \subset A
$$

$(\impliedby)$ Sabemos que $\partial A \subset A$, por lo que $A$ contiene a todos sus puntos frontera. Como $A$ y $A^{C}$ comparten la frontera, y la misma pertenece a $A$, entonces $A^{C}$ no contiene puntos frontera. Por lo tanto $A^{C}$ es abierto.

En conclusión, por definición determinamos que $A$ es cerrado:
$$
\partial A \subset A \implies A \text{ es cerrado }
$$

Pasamos al segundo sii:
$$
\partial A \subset A \Longleftrightarrow A' \subset A
$$
$(\implies)$ Sabemos que $\partial A \subset A$, por lo que $A$ contiene a todos sus puntos frontera. Como probamos antes, esto quiere decir que $A$ es cerrado.

Por proposición, un conjunto ($A$) es cerrado si y solo si contiene a todos sus puntos de acumulación ($A'$).

De esta manera:
$$
\partial A \subset A \implies A' \subset A
$$

$(\impliedby)$ Sabemos que $A' \subset A$, por lo que $A$ contiene a todos sus puntos de acumulación. Por proposición, un conjunto ($A$) es cerrado si y solo si contiene a todos sus puntos de acumulación ($A'$).

Necesariamente, si $A$ es cerrado entonces el complemento es abierto, por lo que todos sus puntos son interiores. Como ambos comparten frontera, esto significa que todos los puntos frontera pertenecen a $A$.

En conclusión:
$$
A' \subset A \implies \partial A \subset A
$$

### Parte d
$$
\overline{A} = A \cup \partial A \text{ es un conjunto cerrado}
$$
Tenemos que probar que el complemento es abierto.

Sabemos que $\overline{A}$ y $\overline{A}^{c}$ comparten frontera. Por la definición de $\overline{A}$, contiene a todos los puntos frontera. De esta forma, $\overline{A}^{c}$ no contiene puntos frontera, por lo que todos sus puntos son internos.

En conclusión, aplicando la definición determinamos que $\overline{A}^{c}$ es abierto, y por lo tanto, $\overline{A}$ es cerrado.

### Parte e
Para probar que $A'$ es cerrado, consideremos la siguiente proposición:
Un conjunto ($A$) es cerrado si y solo si contiene a todos sus puntos de acumulación ($A'$).

En este caso, $A'$ es el conjunto de todos los puntos de acumulación de $A$ ($A$ sin sus puntos aislados).

Sin embargo, si analizamos la definición, $a \in A' \implies \forall \delta > 0, B^{*}(a, \delta) \cap A \neq \emptyset$, podemos ver que todos los puntos de acumulación de $A$ también son puntos de acumulación de $A'$.

De esta forma, todos los puntos de $A'$ son puntos de acumulación de si mismo, y por lo tanto contiene a todos sus puntos de acumulación.

En conclusión, $A'$ es cerrado. 

---
## Ejercicio 6













