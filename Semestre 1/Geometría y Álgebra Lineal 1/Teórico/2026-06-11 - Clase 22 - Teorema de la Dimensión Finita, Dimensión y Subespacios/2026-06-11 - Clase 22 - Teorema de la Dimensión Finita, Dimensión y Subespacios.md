# Espacios vectoriales
Hoy trataremos el concepto de dimensión, estrechamente relacionado con bases.

Recordamos lo que es una base:

> [!Recordatorio]
> Sea un espacio vectorial $V$.
> 
> Un conjunto finito $B \subset V$ es una base cuando $B$ es a la vez libre y generador de $V$.

La noción de conjunto libre es absoluta: si un conjunto es libre en un subespacio $S \subset V$, también es libre en el espacio más grande $V$. Por otra parte, la noción de generador depende del espacio. Puedo ser generador de un subespacio, pero no del espacio más amplio.

También existe una noción de libre y generador para los conjuntos infinitos, aunque no las trabajaremos en el curso.

Otra característica de los conjuntos libres versus los conjuntos generadores:
- Conjuntos libres:
	- Si le quito un elemento a un conjunto libre, mantiene su calidad de libre.
	- Si le agrego un elemento a un conjunto libre, puede perder su calidad de libre.
- Conjuntos generadores:
	- Si le quito un elemento a un conjunto generador, puede perder su calidad de generador.
	- Si le agrego un elemento a un conjunto generador, mantiene su calidad de generador.

Existen conjuntos que tienen ambas cualidades (a la vez libres y generadores), y dichos conjuntos son las bases.

Ahora, nuestro objetivo es definir la noción de dimensión.

## Dimensión

Objetivo:

### Teorema

> [!Teorema]
> Si $V$ tiene una base con $n$ elementos, entonces todas las bases de $V$ tienen $n$ elementos.

Veremos que existe una cantidad infinita de bases para un mismo espacio vectorial. Sin embargo, todas tienen una característica en común: la cantidad de elementos, la cual representa la dimensión del espacio.

Ahora, veremos un teorema que nos será super útil para realizar demostraciones realizadas a la dimensión:

#### Lema técnico

> [!Lema técnico]
> Supongamos que
> - $L = \{ v_{1}, \dots, v_{p} \} \subset V$ es un conjunto libre
> - $G \subset V$ es un generador (de $V$) tal que $\{ v_{1}, \dots, v_{k} \} \subset G$, para algún $k$ tal que $0 \leq k < p$
> 
>Entonces, existe $G' \subset V$ generador tal que
> - $\{ v_{1}, \dots, v_{k}, v_{k + 1} \} \subset G'$
> - $\# G' = \# G$

En este caso, hay $p - k$ elementos que no están en $G$ pero si en $L$.

La clase anterior demostramos que si tenemos una parte común entre $L$ y $G$, y la parte en común no es todo el conjunto $L$ (hay elementos de $L$ que no están en $G$), entonces podemos introducir elementos de $L$ en $G$ de a uno, sin cambiar la cantidad de elementos de $G$ (sustituyéndolo por otro). En realidad lo probamos para un elemento: incluimos un elemento de $L$ en $G$, sustituyéndolo por otro elemento que podía representarse como combinación lineal del resto, y así conformamos $G'$. Por inducción, se puede hacer con el resto de elementos, hasta incluir todo $L$ en $G$ (sin cambiar la cantidad de elementos), demostrando finalmente que todo libre tiene igual o menos elementos que todo generador (siendo sus cardinales iguales en el caso de las bases).

Utilizaremos el siguiente teorema:

#### Teorema

> [!Teorema Libre VS Generador]
> Si $L \subset V$ es un conjunto libre y $G \subset V$ un conjunto generador (libre finito), entonces
> $$
> \# L \leq \# G
> $$

Demostraremos esto, siendo la idea repetir el lema varias veces.

##### Demostración
Sean $L = \{ v_{1}, \dots, v_{p} \} \subset V$ libre y $G \subset V$ un generador (finito).

Escribamos $G_{0} = G$ (el primer generador, el cual modificaremos paso por paso).

Primeramente, $G$ y $L$ tienen en común el conjunto vacío.

Sabemos que $\{  \} \subset G_{0}$ (caso $k = 0$).

Por el lema, existe $G_{1} \subset V$ generador tal que:
$$
\# G_{1} = \# G_{0} \text{ y } \{ v_{1} \} \subset G_{1} \qquad (\text{caso } k = 1)
$$

Por el lema, existe $G_{2} \subset V$ generador tal que:
$$
\# G_{2} = \# G_{1} \text{ y } \{ v_{1}, v_{2} \} \subset G_{2} \qquad (\text{caso } k = 2)
$$

Mientras queden elementos en $L$, podemos repetir este procedimiento (hasta $p$ veces, cantidad de elementos de $L$).

Por el lema, existe $G_{p} \subset V$ generador tal que:
$$
\# G_{p} = \# G_{p - 1} \text{ y } \underbrace{ \{ v_{1}, \dots, v_{p} \} }_{ L } \subset G_{p} \qquad (\text{caso } k = p)
$$

Ahora, tenemos todo $L$ en $G_{p}$ y no podemos aplicar más el lema (ya que no quedan elementos en $L$, en total se aplicó $p$ veces).

Luego:
$$
\# L = p \leq \# G_{p} = \# G_{p - 1} = \dots = \# G_{2} = \# G_{1} = \# G_{0} = \# G
$$
ya que
$$
L \subset G_{p}
$$


De esta forma, para demostrar que $\# L \leq \# G$ hicimos $p$ transformaciones lineales sobre $G$ para incorporar la totalidad de $L$ en $G$ (elemento por elemento).
$L$ se mantuvo durante toda la demostración, simplemente fuimos agregando elementos en $G$ sin modificar su cardinal.

El lema utilizado es muy interesante, ya que indica que hay una estrecha relación entre los conjuntos libres y los generadores (de un mismo espacio vectorial), incluso cuando son disjuntos.

Ahora, podemos concluir con nuestro objetivo: definir la dimensión finita.

### Teorema - Dimensión finita

#Teorema
> [!Teorema - Dimensión finita]
> Si $V$ tiene una base con $n$ elementos, entonces todas las base de $V$ tienen $n$ elementos.

#### Demostración
Sean $B_{1}, B_{2} \subset V$ dos bases de $V$. Queremos demostrar que ambas tienen la misma cantidad de elementos, mismo cardinal.

En base al Teorema Libre VS Generador:
$$
\# B_{1} \leq \# B_{2}
$$
pues $B_{1}$ es libre y $B_{2}$ generador.

Pero también se cumple en el otro sentido:
$$
\# B_{2} \leq \# B_{1}
$$
pues $B_{2}$ es libre y $B_{1}$ generador.

Luego:
$$
\# B_{1} = \# B_{2}
$$

Como vemos, la demostración es bastante sencilla apoyándonos en el teorema visto recientemente.

**Notación**:$$
dim(V) = n
$$cuando $V$ tiene una base (o todas sus bases, que es equivalente) con $n$ elementos.

**Observación**:
Por convención:
$$
dim(\{ \vec{0} \}) = 0
$$

### Ejemplos
A continuación, abordaremos algunos ejemplos de espacios vectoriales comunes:

- $dim(\mathbb{K}^{n}) = n$ 
	Ya que una base - específicamente la canónica - tiene $n$ elementos, todas las bases tendrán $N$ elementos.
- $dim(M_{m \times n}) = m \times n$
	Ya que la base canónica está compuesta por todas las matrices con todas las entradas nulas menos 1, teniendo un total de $m \times n$ elementos.
- $dim(\mathbb{R}_{\leq n}[X]) = n + 1$
	Ya que la base que conocemos de dicho espacio vectorial es $B = \{ \overbrace{ 1 }^{ x^{0} }, x, x^{2}, \dots, x^{n} \}$, pues cualquier polinomio de grado menor o igual a $n$ es combinación lineal de los monomios anteriores, y su escritura es única, por lo que es una base.
	Aclaración: La descomposición de cada vector es única PARA UNA BASE DADA. O sea, dentro de una base, cada vector se puede expresar de una y solo una forma, pero esto es por cada base.
- $dim(\mathbb{R}[X]) = \infty$ ($= V$ no tiene base finita)
	Esto es visible si consideramos las siguientes familias de vectores:
	- $L_{1} = \{ 1 \}$
	- $L_{2} = \{ 1, x \}$
	- $L_{n} = \{ 1, x, \dots, x^{n} \}$
	La particularidad de los conjuntos libres es que tienen cardinal menor o igual a todas las bases. Por lo tanto, cualquier base tiene que tener $n$ elementos distintos para todo $n$. En conclusión, no hay base finita. Como tenemos conjuntos libres tan grandes como queramos (arbitrariamente grandes, de cardinales no acotados), no existe base finita.
	Si existiera base finita, todos los libres tendrían cardinal menor o igual a dicha base, cosa que es imposible aquí.
	En estos casos, donde los conjuntos libres son arbitrariamente grandes, decimos que el espacio tiene dimensión infinita.
	Este se considera el primer espacio de dimensión infinita, el más pequeño. Luego, podríamos estudiar el espacio vectorial de las funciones, que contiene a todos los polinomios, teniendo dimensión infinita, pero mayor que el espacio de los polinomios.

De esta forma, podemos enunciar el teorema:


### Teorema

#Teorema
> [!Teorema]
> Si $V$ es un espacio de dimensión finita, entonces todo subespacio vectorial $S \subset V$ es de dimensión finita, y
> $$
> dim(s) \leq dim(V)
> $$

En particular, demostraremos que si $V$ (dimensión $n$) tiene una base (con $n$ elementos), entonces cada subespacio vectorial también tiene una base, pero más pequeña en general.

Además, utilizaremos el siguiente lema:

#### Lema

#Lema
> [!Lema]
> Sea $L \subset V$ un conjunto libre. Para todo vector $v \in V$, si $v \not \in [L]$, entonces $L \cup \{ v \}$ es libre.

Esto tiene sentido, ya que un conjunto es libre cuando ninguno de sus elementos puede ser definido como combinación lineal del resto. De esta forma, si consideramos un vector que pertenece al mismo espacio vectorial del que se formo dicho conjunto libre, pero no forma parte del espacio generado por el mismo, significa que el vector no es combinación lineal de los vectores pertenecientes al conjunto libre. Por tal razón, si agregamos el vector al conjunto libre, este mantendrá su característica de libre.

Esto se puede representar visualmente realizando un dibujo vago, el cual puede ayudar a entender la intuición.

Además, podemos establecer una generalidad:
En todos los casos $L$ es una base de $[L]$. Por lo tanto $L \cup \{ v \}$ es una base de $[L \cup \{ v \}]$.

##### Demostración
Sean $L = \{ v_{1}, \dots, v_{p} \}$ libre y $v \not \in [L]$.

Queremos demostrar que $L \cup \{ v \}$ es libre.

Sean coeficientes $\alpha_{1}, \dots, \alpha_{p}, \alpha \in K$ tales que:
$$
\alpha_{1} \cdot v_{1} + \dots + \alpha_{p} \cdot v_{p} + \alpha \cdot v = \vec{0}
$$


(Podemos deducir que $\alpha = 0$, ya que sabemos que, como $L$ es libre:
$$
\alpha_{1} \cdot v_{1} + \dots + \alpha_{p} \cdot v_{p} = \vec{0}
$$
con $\alpha_{1} = \alpha_{2} = \dots = \alpha_{p} = 0$, puesto que $L$ es libre. De esta forma, para que se mantenga la igualdad, tiene que cumplirse que $\alpha = 0$.)


Si $\alpha$ no fuera nulo, tendríamos que
$$
v = -\frac{\alpha_{1}}{\alpha} \cdot v_{1} - \dots - \frac{\alpha_{p}}{\alpha} \cdot v_{p} + \alpha \cdot v \qquad \in [L]
$$
Como vemos, esto significa que $v$ es combinación lineal de los elementos de $L$, perteneciendo a $[L]$. Sin embargo, contradice a la hipótesis.

Por lo tanto: $\alpha \neq 0$

Luego
$$
\alpha_{1} \cdot v_{1} + \dots + \alpha_{p} \cdot v_{p} = \vec{0}
$$
Por lo tanto:
$$
\alpha_{1} = \dots = \alpha_{p} = 0
$$
Ya que $L = \{ v_{1}, \dots, v_{p} \}$ es libre.

En conclusión:
$$
L \cup \{ v \} = \{ v_{1}, \dots, v_{p}, v \} \text{ es libre}
$$

Como vemos, realizamos varias operaciones durante la demostración. La idea de realizar operaciones es comprobar ideas, entender propiedades.

Ahora, podemos demostrar el teorema anterior utilizando el lema:

Teorema:
Si $S \underset{ sev } \subset V$ con dimensión finita, entonces
$$
dim(s) \leq dim(V)
$$

#### Demostración

Como $V$ tiene dimensión finita, todo subconjunto libre de $S$ (que también es un subconjunto libre de $V$) tiene un cardinal $\leq dim(V)$ (sea $n = dim(V)$).

Sean:
- $p = máx \{ \underbrace{ \# L : L \subset S \text{ libre} }_{ \subset \{ 0, \dots, n \} } \} \leq n$
Máximo de todos los cardinales de subconjuntos libres de $S$. Sabemos que todos estos cardinales están acotados por $n$, por lo que podemos estudiar su máximo (no es infinito).

Como es el máximo, sabemos que hay algún conjunto $L$ que tiene $p$ elementos.

- $L_{p} \subset S$ un conjunto libre con $p$ elementos.
Como todos los conjuntos libres de $S$ tienen cardinal $\leq n$, elegimos el que tenga el cardinal más alto, siendo su cardinal $p$.

De esta forma, $L_{p}$ es un "conjunto libre máximo en $S$".

Es así que demostramos que un conjunto con estas características existe. Demostramos que es libre, quedando por demostrar que también es generador de $S$, siendo en conclusión una base de $S$:

Nos queda demostrar que $L_{p}$ es un generador de $S$, es decir: $[L_{p}] = S$.

Por el absurdo, supongamos que $[L_{p}] \subsetneq S$.

Entonces, existe $v \in S$ tal que $v \not \in [L_{p}]$.

Por el lema anterior, el conjunto $L_{p + 1} := L_{p} \cup \{ v \}$ es libre.
(De esta forma, obtuvimos un subconjunto libre de $S$ que tiene demasiados elementos, ya que habíamos determinado que el límite era $p$.)

Contradicción, pues:
$L_{p + 1} \subset S$ libre, pero $\# L_{p + 1} = p + 1 > p$: contradicción.

Mostramos que si tenemos un subconjunto libre que genera un espacio más pequeño, siempre lo podemos agrandar tomando un vector fuera del espacio generado. Por lo tanto, la hipótesis es absurda:
$$
[L_{p}] \subsetneq S \text{ es absurdo}
$$
Por lo tanto: $[L_{p}] = S$.
Luego: $L_{p}$ es una base de $S$ (ya que es libre y generador).

Conclusión:
$$
dim(S) = p \leq n = dim(V)
$$

Así finalizamos la demostración del teorema.

Ahora, mencionaremos consecuencias importantes sobre el teorema anterior:

> [!Observación]
> Si $dim(V) = n$:
> 
> - Todo conjunto libre tiene cardinal $\# L \leq n$
> - Todo conjunto generador tiene cardinal $\# G \geq n$

Recordemos que $n$ es el cardinal de cualquier base de $V$. De esta forma, cualquier base de $V$ tiene cardinal $\geq$ a cualquier conjunto libre de $V$, y cualquier base de $V$ tiene cardinal $\leq$ a cualquier generador de $V$. Esto es fundamental para determinar rápidamente si un conjunto puede o no ser libre/generador/base de un espacio en base a la cantidad de elementos.

Finalizaremos la clase de hoy analizando otro teorema:

### Teorema (base incompleta)

#Teorema
> [!Teorema - Base incompleta]
> En un espacio vectorial $V$ de dimensión finita, sean:
> $L \subset V$ libre, $G \subset V$ generador tales que $L \subset G$.
> 
> Entonces, existe una base $B$ de $V$ tal que $L \subset B \subset G$.
> 
> Intuiciones:
> - $L$ es la "base incompleta".
> - $G$ es la "reserva de vectores".


De esta forma, lo que dice el teorema es que, cuando tengo una base incompleta (conjunto libre) y una reserva de vectores (generador), puedo completar la base incompleta, transformándola en una base real, solo utilizando vectores de la reserva.

Así, vemos a los conjuntos libres como bases a las que se les quitaron elementos, y a los generadores como bases con elementos de más.

Se puede transformar un libre en una base, utilizando cualquier generador que contenga al libre.

A continuación, demostramos el teorema:

#### Demostración
Sea $B$ un subconjunto de $G$ (generador) tal que $L \subset B$ y $B$ libre, con máximo cardinal.

(Usando $G$, utilizamos los conjuntos libres que extienden $L$, pero que mantienen la calidad de ser libres. En este caso, la extensión libre más grande posible será $B$.)

$B$ es una extensión libre máxima de $L$, sólo usando vectores de $G$.

Por construcción (como es libre), $\# B \leq dim(V)$.

Por construcción: $B$ es libre, y $L \subset B \subset G$.

Nos queda demostrar que $B$ es generador.

Supongamos por el absurdo que $[B] \subsetneq V$.

No lo terminaremos de demostrar en esta clase, pero la idea es la siguiente:
Como $[B] \subsetneq V$, entonces extenderemos $B$ tomando un vector que esté en $V$ y no en $[B]$, pero asegurándonos de que esté en $G$ (ya que es generador de $V$).

