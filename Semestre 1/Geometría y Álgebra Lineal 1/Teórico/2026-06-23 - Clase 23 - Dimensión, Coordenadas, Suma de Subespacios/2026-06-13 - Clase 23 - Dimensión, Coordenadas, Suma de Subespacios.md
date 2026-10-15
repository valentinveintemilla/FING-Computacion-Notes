# Espacios vectoriales

## Dimensión
En esta oportunidad, continuamos con los problemas relacionados con dimensión.

Vimos que cuando un espacio vectorial tiene una base con $n$ vectores, entonces todas sus bases tienen $n$ vectores, y, por lo tanto, decimos que el espacio vectorial tiene dimensión $n$.

Además:

> [!Recordatorio]
> Si $S \underset{sev} \subset V$, entonces $dim(S) \leq dim(V)$
> 

Además, veremos que en caso de que $dim(S) = dim(V)$, entonces el subespacio esta lleno (completo), contiene todo.

Nos faltaba demostrar el teorema de la base incompleta:
### Teorema (base incompleta)

> [!Teorema (base incompleta)]
> Sean:
> - $V$ un espacio vectorial de dimensión $n$.
> - $L \subset V$ conjunto libre finito. Necesariamente $\# L \leq n$.
> - $G \subset V$ conjunto generador (de $V$) cualquiera. Necesariamente $\# G \geq n$.
> 
> Tales que $L \subset G$, entonces existe una base $B$ de $V$ tal que $L \subset B \subset G$.

De esta forma, la intuición es la siguiente:
- $L$ = base incompleta
- $G$ = reserva de vectores

Entonces, podemos tomar un conjunto libre cualquiera y agregarle vectores (asegurando que mantenga su libertad) hasta que se transforme en una base.
Hay dos puntos de vista:
- Agregar vectores a una base incompleta.
- Quitarle vectores a una reserva de vectores.

La base es el punto de contacto entre un conjunto libre y un generador (posee ambas características).

### Demostración
Trivial cuando $n = 0$.

Ahora, se supone que $n \geq 1$.

Sea $p := máx \{ \#L' : L' \text{ libre y } L \subset L' \subset G \} \leq n$.

Sobre $L'$ podemos decir que cumple que $\# L' \leq n$. $n$ es un máximo en sentido de la dimensión de los conjuntos libres de $V$.

La noción de máximo tiene sentido ya que sabemos que $\# L' \leq n$, por lo tanto el conjunto está acotado superiormente y se puede tomar un valor máximo.

Tenemos que $\# L \leq p \leq n$.

Sea $L'$ libre tal que $L \subset L' \subset G$ y además $\# L' = p$.

Básicamente, queremos demostrar que $L'$ es base, lo que lograremos demostrando que es generador (puesto que ya es libre).

Lo demostramos por absurdo:
Supongamos (por el absurdo) que $L'$ no es generador, lo que quiere decir que $[L'] \subsetneq V$.
Esto implica que $G \not \subset [L']$, ya que por lo contrario $L'$ contendría todas las bases de $V$, conteniendo a $V$ también.

Si no fuera el caso, tendríamos que $V = [G] = [L']$.

Luego, existe $v \in G$, tal que $v \not \in [L']$.

Consideramos $L'' := L' \cup \{ v \}$ ($p + 1$ vectores).

Tenemos que $L''$ es libre (por lema anterior) y $L \subset L'' \subset G$ (ya que por hipótesis todos estos vectores están en $G$, en ningún momento salimos del conjunto).

Sin embargo, llegamos a una contradicción. Conseguimos un conjunto $L''$ que tiene cardinal mayor a $p$.
Contradicción, pues $\# L'' = p + 1 > p$.

Por lo tanto, la hipótesis $[L'] \subsetneq V$ es falsa: $[L'] = V$.
$L'$ es libre y generador, entonces es una base: $B := L'$.

Esto demuestra el teorema de la base incompleta.

Ahora, estudiaremos las consecuencias de este resultado:
#### Corolario 1

#Corolario
> [!Corolario]
> 1. Todo conjunto libre se puede extender hasta formar una base.
> 2. Todo conjunto generador (de $V$) contiene una base.

Demostraremos el corolario, aunque es trivial.

##### Demostración
Para extender el conjunto libre, consideraremos como reserva de vectores a todo el espacio.
1. Tomar $G = V$ y aplicar base incompleta.
2. Tomar $L \neq \emptyset$ y aplicar base incompleta.

Hay dos situaciones particulares que nos interesan:
- Tenemos $L$ vacío y queremos reducir un generador.
- No tengo generador y quiero agrandar un libre (y tomamos el generador lleno, todo el espacio).

Esto nos permite trabajar con otros corolarios:

#### Corolario 2

#Corolario

> [!Corolario]
> Sea $V$ un espacio vectorial de dimensión n.
> 1. Si $A \subset V$ es libre y $\# A \geq n$, entonces $\# A = n$ y $A$ es una base.
> 2. Si $A \subset V$ es generador y $\# A \leq n$, entonces $\# A = n$ y $A$ es una base.
> 
> En particular, para todo conjunto $A \subset V$ tal que $\# A = n$:
> $$
> A \text{ es libre } \Longleftrightarrow A \text{ es generador } \Longleftrightarrow A \text{ es base}
> $$

Estas propiedades son excelentes para determinar conjuntos generadores de espacios vectoriales. Si en un espacio de dimensión $n$ tenemos un conjunto de $n$ elementos, simplemente tenemos que determinar si es libre o generador, y con cualquiera de los dos caminos llegamos a la conclusión de que es base del espacio.

Este nos permite verificar que, dado un espacio vectorial $V$ de dimensión $n$, todo subespacio de $V$ de dimensión $n$ es el espacio lleno (es $V$).

Ahora, pasamos a una proposición:
#### Proposición

#Proposición
Sea $V$ un espacio vectorial de dimensión $n$.

Si un espacio vectorial $S \underset{sev} \subset V$ tiene dimensión $n$, entonces $S = V$.

No lo demostraremos ya que es obvio, pero se toma como referencia el corolario anterior.

**Demostración**:
Sea $B$ una base de $S$ ($B$ es libre y $[B] = S$). Como $dim(S) = n$, tenemos que $\# B = n = dim(V)$.

Como $B$ es libre en $V$, tenemos que $B$ es una base de $V$ por el corolario anterior (es un conjunto libre de $V$ con $\# B = dim(V)$, entonces es necesariamente una base del conjunto).

La libertad de un conjunto no esta dada por el espacio considerado. Si tenemos $S \underset{sev} \subset V$ y un conjunto $L \subset S$ libre, entonces $L$ también es libre en el contexto de $V$.

---
## Coordenadas

Ahora, pasaremos a definir la noción de coordenada. La idea es que cuando tengo una base, la misma define una noción de coordenada.

> [!Coordenadas - Definición]
> Sea $V$ un espacio vectorial con una base $B = \{ v_{1}, \dots, v_{n} \}$.
> 
> Dado un vector $u \in V$n se llaman las coordenadas de $u$ en la base $B$ la única n-upla $(\alpha_{1}, \dots, \alpha_{n}) \in \mathbb{K}^{n}$ tal que:
> $$
> u = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}
> $$
> **Notación**: $(\alpha_{1}, \dots, \alpha_{n}) = coord_{B}(u)$
> 
> Dicho de otro modo:
> $$
> coord_{B}(u) = (\alpha_{1}, \dots, \alpha_{n}) \Longleftrightarrow u = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}
> $$

Sabemos que en una base, la descomposición es única (solo podemos asociar una n-upla única para definir su descomposición). Esta n-upla se llama las coordenadas del vector $u$ en la base $B$.

De esta forma, las coordenadas de un mismo vector cambian según la base considerada, y una base es simplemente un sistema de coordenadas.

Conocemos la noción de coordenada, aunque estamos habituados a las coordenadas considerando la base canónica.

ACLARACIÓN: Como estamos en la teoría de los espacio vectoriales, necesariamente el origen es el vector nulo. Hay otra teoría, que permite desplazar el vector nulo: teoría de los espacio afines. Igualmente, no la abordaremos en el curso.

A continuación, veremos algunos ejemplos:
### Ejemplos
- $V := \mathbb{R}_{\leq 3}[X] \qquad (\mathbb{R}_{3}[X])$
$$
B = \{ 1, x, x^{2}, x^{3} \}
$$
Considerando esto, determinemos las coordenadas de
$$
coord_{B}(3x + 2x^{2} - x^{3}) = (0, 3, 2, -1)
$$
Al ser de dimensión cuatro, las coordenadas siempre estarán dadas por cuatro componentes.

- $V := \mathbb{R}^{3}$
$$
B = \{ (1, 1, 0), (0, 1, 0), (0, 0, 1) \}
$$
Podemos demostrar que es base considerando que tiene tres elementos (dimensión de $V$), y verificando que sea libre o generador.

Como vemos, no es la base canónica, por lo que definir las coordenadas no será tan sencillo.
1. $$
coord_{B}(1, 2, 1) = (1, 1, 1)
$$
Para llegar al resultado, tenemos que resolver
$$
\begin{cases}
\alpha = 1 \\
\alpha + \beta = 2 \\
\gamma = 1
\end{cases}
$$
que es un sistema trivial. Nos define las coordenadas del vector: $coord_{B}(1, 2, 1) = (\alpha, \beta, \gamma) = (1, 1, 1)$

Cuando consideramos la base canónica, las coordenadas del vector coinciden con la expresión del vector (en una base canónica: $coord_{B}(1, 2, 1) = (1, 2, 1)$).

2. $$
coord_{B}(2, 4, 6)
$$
$$
(2, 4, 6) = \alpha(1, 1, 0) + \beta(0, 1, 0) + \gamma(0, 0, 1)
$$
$$
\begin{cases}
\alpha = 2 \\
\alpha + \beta = 4 \\
\gamma = 6
\end{cases}
$$
Entonces: $coord_{B}(2, 4, 6) = (\alpha, \beta, \gamma) = (2, 2, 6)$

De esta forma, al tener que trabajar con sistemas, es un problema que se resuelve mediante Rouché-Frobenius.

Ahora, a la inversa: tenemos las coordenadas y queremos obtener el vector. Este caso será mucho más sencillo.
3. Hallar $(x, y, z)$ tal que $coord_{B}(x, y, z) = (1, 3, 1)$

Al conocer las coordenadas, sabemos que el vector se expresa como:
$$
\begin{align}
(x, y, z) &= 1(1, 1, 0) + 3(0, 1, 0) + 1(0, 0, 1) \\
&= (1, 1, 0) + (0, 3, 0) + (0, 0, 1) \\
&= (1, 4, 1)
\end{align}
$$
En conclusión, $x = 1, y = 4, z = 1$, por lo que $(x, y, z) = (1, 4, 1)$

¿Qué dice todo esto en forma general?
- Cada vector $u$ se puede reemplazar por una n-upla.
- Todo espacio vectorial de dimensión $n$ tiene la misma estructura que $\mathbb{K}^{n}$.

Entonces, cuando estudio todos los espacios de $\mathbb{K}^{n}$ a menos de un isomorfismo, son todos los espacios de dimensión $n$.
Esto es super útil cuando trabajamos con espacios que son poco familiares.

Luego, volveremos a estudiar coordenadas con el problema de cambio de coordenadas: cuando tenemos dos bases diferentes y las coordenadas de una, como pasar dichas coordenadas a la otra base.

Por ahora, pasaremos del tema y comenzaremos el siguiente.

---
## Suma de subespacios
En una clase anterior trabajamos con una alternativa a la unión de espacio vectoriales (operación la cual generalmente no da como resultado otro espacio vectorial): la suma.

> [!Recordatorio]
> Dados $S, T \underset{sev} \subset V$, se define el subespacio vectorial $S + T$ por:
> $$
> S + T = \{ u + v : u \in S, v \in T \}
> $$
> Se dice que la suma $S + T$ es <u>directa</u> cuando la descomposición es única:
> $$
> (\forall u \in S + T) (\exists! v \in S) (\exists! w \in T) \text{ tq } u = v + w
> $$
> 
> Notación: $S \oplus T$

Por ejemplo, si sumamos dos rectas, obtenemos un plano vectorial.

La suma contiene a la unión: $S \cup T \subset S + T$

La suma directa no es una operación como tal, simplemente es la suma, pero en el caso particular en el que cada vector perteneciente a la suma se descompone de forma única como la suma de un vector de $S$ y un vector de $T$.

Ahora, veremos algunos ejemplos de sumas (algunas directas y otras no):

### Ejemplos
- **Contraejemplo**
En $\mathbb{R}^{3}$:
$$
\begin{align}
&S = \{ (x, y, 0): x, y \in \mathbb{R} \} \underset{sev} \subset \mathbb{R}^{3} \\
&T = \{ (0, y, z): y, z \in \mathbb{R} \} \underset{sev} \subset \mathbb{R}^{3}
\end{align}
$$
En este caso, la suma es un plano más otro plano, siendo la dimensión al menos 2:
- Si la dimensión es 2, significa que los planos son iguales, pero no es el caso.
- Si la dimensión es al menos 3, como estamos en $\mathbb{R}^{3}$, la suma es todo $\mathbb{R}^{3}$, considerando los lemas anteriores.

En conclusión: $S + T = \mathbb{R}^{3}$

Ahora, verificamos si es una suma directa:
$$
\begin{align}
(0, 1, 0) &= \underbrace{ (0, 1, 0) }_{ \in S } + \underbrace{ (0, 0, 0) }_{ \in T } \\
&= \underbrace{ (0, 0, 0) }_{ \in S } + \underbrace{ (0, 1, 0) }_{ \in T } \\
&= \underbrace{ \left( 0, \frac{1}{2}, 0 \right) }_{ \in S } + \underbrace{ \left( 0, \frac{1}{2}, 0 \right) }_{ \in T }
\end{align}
$$
Con un simple ejemplo, comprobamos que $S + T$ no es una suma directa (no denotamos $S \oplus T$).

Ahora, veremos una caracterización de las sumas directas para facilitar su reconocimiento.

### Proposición

#Proposición
> [!Proposición]
> Una suma $S + T$ es directa si y sólo si
> $$
> S \cap T = \{ \vec{0} \}
> $$

De esta forma, es mucho más sencillo determinar si la suma de dos subespacios es directa o no. En el caso anterior, es evidente que no es directa, ya que ambos planos se interceptan.

#### Demostración
$(\implies)$ Supongamos que $S + T$ es directa ($S \oplus T$).

Sea $u \in S \cap T$.
Tenemos que $u = \underbrace{ u }_{ \in S } + \underbrace{ \vec{0} }_{ \in T } = \underbrace{ \vec{0} }_{ \in S } + \underbrace{ u }_{ \in T }$.

Por unicidad de la escritura: tenemos $u = \vec{0}$.

Ahora, pasamos al recíproco:
$(\impliedby)$ Supongamos que $S \cap T = \{ \vec{0} \}$.

Para demostrar que la suma es directa se supone que algún $u \in V$ tenga 2 descomposiciones
$$
u = v_{1} + w_{1} = v_{2} + w_{2}, \text{ con } \begin{align}
&v_{1}, v_{2} \in S \\
&w_{1}, w_{2} \in T
\end{align}
$$

Ahora, queremos demostrar que, necesariamente, $v_{1} = v_{2}$ y $w_{1} = w_{2}$.

Se observa que
$$
\vec{0} = u - u = \underbrace{ (v_{1} - v_{2}) }_{ \in S } + \underbrace{ (w_{1} - w_{2}) }_{ \in T }
$$
Se deduce que
$$
\underbrace{ (v_{1} - v_{2}) }_{ \in T } = -\underbrace{ (w_{1} - w_{2}) }_{ \in T }
$$
Tenemos que $(v_{1} - v_{2}) \in S \cup T$ (ya que originalmente pertenece a $S$ y lo expresamos en función de $(w_{1} - w_{2}) \in T$)
$$
\implies v_{1} - v_{2} = \vec{0}, v_{1} = v_{2}
$$
De mismo modo: $w_{1} = w_{2}$

Finalizamos la demostración de la proposición.

Pasaremos a estudiar una última proposición: cuando tenemos suma directa, podemos desarrollar la unión de bases, y se obtiene una base de la suma directa.

### Proposición

#Proposición

> [!Proposición]
> Si la suma $S \oplus T$ es directa.
> 
> Si
> - $A \subset S$ es una base de $S$
> - $B \subset T$ es una base de $T$
> 
> Entonces: $A \cup B$ es una base de $S \oplus T$.

Esto no funciona si la suma no es directa, ya que podríamos tener vectores comunes entre las bases de $S$ y $T$.

Esto nos lleva a un corolario:

### Corolario
En caso de suma directa $S \oplus T$, tenemos que
$$
dim(S \oplus T) = dim(S) + dim(T)
$$

Esto se cumple trabajando en un espacio de dimensión finita. Es trivial, considerando la proposición anterior de las bases.

Si consideramos dos bases, una de $S$ y otra de $T$, sabiendo que las dimensiones son correspondientes a las bases. Por la proposición anterior, podemos unir las bases y formar una base de la suma directa, siendo su cardinal la suma de las dimensiones de las bases anteriores.

Cuando la suma no es directa, en general, se mantiene la propiedad de ser generador, pero se pierde la propiedad de ser libre:

#### Observación

> [!Observación]
> En general:
> $$
> dim(S + T) \leq dim(S) + dim(T)
> $$

Es menor o igual ya que el caso general incluye el caso directo.

Finalizamos con la clase de hoy.