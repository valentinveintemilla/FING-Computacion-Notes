# Espacios vectoriales
Comenzamos recordando la definición de espacio vectorial:

Un espacio vectorial es una cuádrupla $(K, V, +, \cdot)$ donde:
- $K$ es un cuerpo ($\ll \text{los escalares} \gg$)
- $V$ es un conjunto no vacío ($\ll \text{los vectores} \gg$)
- $(+): V \times V \to V$
- $(\cdot) : K \times V \to V$

Las operaciones $(+)$ y $(\cdot)$ satisfacen:

**Axiomas de suma**
$$(\forall u, v, w \in V)$$
$$
\begin{align}
&\text{(S1)} &&(u + v) + w = u + (v + w) \\
&\text{(S2)} &&u + v = v + u \\
&\text{(S3)} &&(+) \text{ tiene elemento neutro: } u + \vec{0} = u \\
&\text{(S4)} &&\text{Cada vector } u \in V \text{ tiene opuesto } -u: u + (-u) = \vec{0}
\end{align}
$$
**Axiomas de producto**
$$(\forall \alpha, \beta \in K, u, v, w \in V)$$
$$
\begin{align}
&\text{(P1)} &&\alpha \cdot (\beta \cdot u) = (\alpha \beta) \cdot u \\
&\text{(P2)} &&1_{K} \cdot u = u \\
&\text{(P3)} &&\alpha \cdot_{V} (u +_{V} v) = \alpha \cdot_{V} u + \alpha \cdot_{V} v \\
&\text{(P4)} &&(\alpha +_{K} \beta) \cdot_{V} u = \alpha \cdot_{V} u +_{V} \beta \cdot_{V} u
\end{align}
$$

Ahora, estudiaremos algunas propiedades de los espacios vectoriales.

## Propiedades

### Proposición 1

> [!Proposición 1]
> En todo espacio vectorial $(K, V, +, \cdot)$
> 1. El neutro $\vec{0}$ es único.
> 2. Para todo vector $u \in V$, su opuesto $-u$ es único.

#### Demostración (1.1)
Supongamos que $V$ tenga dos neutros $\vec{0}$ y $\overleftarrow{0}$. Es decir
$$
\begin{align}
&u + \vec{0} = u &&(\forall u \in V) &&(a) \\
&u + \overleftarrow{0} = u &&(\forall u \in V) &&(b)
\end{align}
$$
Queremos demostrar que $\vec{0} = \overleftarrow{0}$.

Entonces:
$$
\vec{0} \underbrace{ = }_{ \text{por } (b) } \vec{0} + \overleftarrow{0} = \overleftarrow{0} + \vec{0} \underbrace{ = }_{ \text{por } (a) } \overleftarrow{0}
$$

De esta forma, cuando tengo un elemento neutro, este siempre es único. Esto no solo se da en los espacios vectoriales, sino también en los cuerpos (por la misma razón).

Ahora, demostraremos que el opuesto es único:

#### Demostración (1.2)
Supongamos que $u \in V$ tenga dos opuestos: $-u, \sim u$. Es decir
$$
\begin{align}
&u + (-u) = \vec{0} &&(a) \\
&u + (\sim u) = \vec{0} &&(b)
\end{align}
$$
Queremos demostrar que $-u = \sim u$.

Entonces:
$$
(-u) = (-u) + \vec{0} \underbrace{ = }_{ \text{por } (b) } (-u) + \underbrace{ (u + (\sim u)) }_{ = 0 \text{ por igualdad ant.} } = ((-u) + u) + (\sim u) \underbrace{ = }_{ \text{por } (a) } \vec{0} + (\sim u) = \space \sim u
$$

Nuevamente, los desarrollos anteriores sirven como un ejemplo de como la creatividad es un elemento fundamental en combinación con el pensamiento matemático.

Los razonamientos no dependen del espacio vectorial ni del cuerpo, son genéricos.

### Proposición 2

> [!Proposición 2]
> En todo espacio vectorial $(K, V, +, \cdot)$:
> 1. Si $u + \cancel{ w } = v + \cancel{ w }$, entonces $u = v$.
> 2. Si $\alpha \cdot u = \alpha \cdot v$ y $\alpha \neq 0$, entonces $u = v$
> 3. $0 \cdot u = \vec{0}$
> 4. $(-1_{K}) \cdot u = -u$

(2) Si $\alpha = 0$ no podemos simplificar, no tiene porque cumplirse que $u = v$ ya que $\alpha$ los anula, quedando $\vec{0} = \vec{0}$.

(4) $-1_{K}$ es el $-1$ del cuerpo $K$ relacionado, no tiene porque ser el número $-1$. Por ejemplo, en $Z_{2}$, $-1 = 1$.

#### Demostración (2.1)
Supongamos: $u + w = v + w$
$$
\begin{align}
\implies (u + w) + (-w) &= (v + w) + (-w) \\
\implies u + (w + (-w)) &= v + (w + (-w)) \\
\implies u + \vec{0} &= v + \vec{0} \\
\implies u &= v
\end{align}
$$

Esta regla de simplificación clásica sigue funcionando para los espacios vectoriales.

#### Demostración (2.2)
Supongamos: $\alpha \cdot u = \alpha \cdot v \qquad(\alpha \neq 0)$
$$
\begin{align}
\implies \alpha^{-1} \cdot (\alpha \cdot u) &= \alpha^{-1} \cdot (\alpha \cdot v) \\
\implies (\alpha^{-1} \alpha) \cdot u &= (\alpha^{-1} \alpha) \cdot v &&\text{(por P1)} \\
\implies 1 \cdot u &= 1 \cdot v \\
\implies u &= v
\end{align}
$$

Es necesario suponer que $\alpha \neq 0$ ya que en la demostración utilizamos $\alpha^{-1}$, y es bien sabido que 0 no tiene inverso, además de que como se anulan $u$ y $v$, la igualdad se mantendría aunque $u \neq v$.

Otra regla que aún podemos aprovechar cuando operamos en un espacio vectorial.

#### Demostración (2.3)
$$
\vec{0} + 0 \cdot v = 0 \cdot v = (0 + 0) \cdot u = 0 \cdot u + 0 \cdot u
$$
Luego:
$$
\vec{0} + \cancel{ 0 \cdot v } = 0 \cdot u + \cancel{ 0 \cdot u }
$$
Por (1):
$$
\vec{0} = 0 \cdot u
$$
Utilizamos la regla que demostramos anteriormente: Si $u + \cancel{ w } = v + \cancel{ w }$, entonces $u = v$.

#### Demostración (2.4)
Se observa que:
$$
u + (-1) \cdot u = 1 = 1 \cdot u + (-1) \cdot u = (\overbrace{ 1 + (-1) }^{ \text{en } K = 0 }) \cdot u = 0 \cdot u = \vec{0}
$$
Luego: $(-1) \cdot u$ es el opuesto de $u$

Por unicidad:
$$
(-1) \cdot u = -u
$$

Todas estas reglas son más que conocidas y las hemos utilizado siempre en álgebra. Lo que estamos enunciando y demostrando es que las mismas aplican a cualquier espacio vectorial. Las demostraciones son genéricas.

---
También analizamos varios ejemplos de espacios vectoriales:

## Ejemplos de espacios vectoriales

- $K^{n} = \{ (\alpha_{1}, \dots, \alpha_{n}) : \alpha_{1}, \dots, \alpha_{n} \in K \}$
Es el conjunto de todas las n-uplas de escalares. Tiene dimensión $n$. Vimos que la suma de dos vectores de realiza componente por componente, y el producto de un escalar por un vector se realiza multiplicando cada uno de los componentes del vector por el escalar.

- Dado un intervalo $I \subset \mathbb{R}$
	- $\mathbb{R}^{I} = \{ f : I \to \mathbb{R} \}$
	Conjunto de todas las funciones de $I$ en $\mathbb{R}$. Tiene tantos componentes como elementos hay en $I$ (infinitos), lo que determina la dimensión
	
	- $\mathcal{C}^{0}(I, \mathbb{R}) = \{ f : I \to \mathbb{R} \text{ continuas} \}$
	La suma de dos funciones continuas es otra función continua, y el producto de una constante por una función continua es otra función continua. Por lo tanto, el espacio de las funciones continuas es un espacio vectorial.
	
	- $Der(I, \mathbb{R}) = \{ f : I \to \mathbb{R} \text{ derivables} \}$
	Mismo caso que el anterior, las operaciones de suma y producto de un escalar por una función derivable dan como resultado otra función derivable.
	Cuando hablamos de funciones, el vector nulo es la función constante 0.
	
	- $Int(I, \mathbb{R}) = \{ f : I \to \mathbb{R} \text{ integrables} \}$
	
	Podemos generalizar y decir que todos los espacios de funciones de cualquier cosa a $\mathbb{R}$ son espacios vectoriales.

- $\mathbb{R}[x] = p(x) \text{ polinomio con coeficientes reales}$
También podemos sustituir $\mathbb{R}$ por $K$.

- Para todos $m, n \geq 1$: $M_{m \times n} (K)$ es un espacio vectorial sobre $K$.
La suma entre matrices y el producto de una matriz por un escalar están bien definidas. Además, el vector nulo es la matriz nula.

- Dados dos espacios vectoriales $V_{1}$ y $V_{2}$ sobre (el mismo) $K$
Se considera el conjunto
$$
V_{1} \times V_{2} = \{ (u_{1}, u_{2}) : u_{1} \in V_{1}, v_{2} \in V_{2} \}
$$
equipado con las operaciones:
$$
(u_{1}, u_{2}) +_{V_{1} \times V_{2}} (v_{1}, v_{2}) = (u_{1} +_{V_{2}} v_{1}, u_{2} +_{V_{2}} v_{2})
$$
$$
\alpha \cdot_{V_{1} \times V_{2}} (u_{1}, u_{2}) = (\alpha \cdot_{V_{1}} V_{1}, \alpha \cdot_{V_{2}} u_{2})
$$

De esta forma, podemos formar un nuevo espacio vectorial a partir de dos espacios vectoriales definidos sobre el mismo conjunto de escalares $K$, desarrollando el producto cartesiano entre ambos espacios vectoriales. Es así que las operaciones de suma entre vectores y producto de un vector por un escalar estarán perfectamente definidas.
El vector nulo estaría compuesto por el par del vector nulo del primer espacio vectorial y el vector nulo del segundo espacio vectorial.

Esto se puede hacer con $n$ espacios vectoriales, siempre manteniendo la característica de que todos compartan el mismo cuerpo $K$.

---
Pasamos al siguiente tema fundamental dentro del capítulo de espacios vectoriales:
## Subespacios vectoriales

> [!Subespacio vectorial - Definición]
> Sea $V = (V, K, +, \cdot)$ un espacio vectorial.
> 
> Se dice que un subconjunto $S  \subset V$ es un espacio vectorial ($sev$) de $V$ cuando:
> $$
> \begin{align}
> &(1) &&\vec{0} \in S \\
> &(2) &&\text{Si } u, v \in S, \text{ entonces } u + v \in S &&(S \text{ es estable por suma}) \\
> &(3) &&\text{Si } u \in S, \text{ entonces } \alpha \cdot u \in S \text{ para todo } \alpha \in K
> \end{align}
> $$
> 
> <u>Notación</u>: $S \underset{sev} \subset V$

Utilizaremos esta abreviatura desde ahora. Simplemente nos referiremos a los espacios vectoriales por el conjunto de vectores que lo definen (el componente que más nos interesa).

De esta forma, para que sea un subespacio vectorial, tiene que contener al vector nulo, ser cerrado por suma de vectores, y ser cerrado por producto de un escalar por un vector. Que sea cerrado (estable), quiere decir que el resultado de la operación se mantenga dentro del conjunto inicial.

Un subespacio vectorial es algo "derecho", no es irregular (por como se comporta). La idea es reducir problemas "irregulares" a estructuras idealizadas.

Por ejemplo, la derivada permite estudiar el comportamiento de una curva (irregular) como si fuera una recta.

> [!Proposición]
> Un subconjunto $S \subset V$ es un subespacio vectorial de $V$ si y sólo si:
> $$
> \begin{align}
> &(1) &&S \neq \emptyset \\
> &(2) &&\forall \alpha, \beta \in K, \forall u, v \in S, \alpha \cdot u + \beta \cdot v \in S
> \end{align}
> $$

Esto quiere decir que si tengo un subespacio vectorial, este no es vacío, y además puedo desarrollar combinaciones lineales de elementos de $S$ y el resultado recae dentro de $S$. Recíprocamente, si tengo un subconjunto que cumple ambas propiedades, entonces es un subespacio vectorial.

Podemos justificar las dos propiedades:
(1) $S$ no es vacío ya que tiene nulo.

(2) Suponemos que $u, v \in S$, entonces, por el axioma 3, $\alpha \cdot u, \beta \cdot v \in S$. Finalmente, por el axioma 2, $\alpha \cdot u + \beta \cdot v \in S$.

Esta caracterización nos permite unificar los puntos (2) y (3), facilitando algunas demostraciones.

> [!Observación]
> Todo espacio vectorial $V$ tiene al menos dos subespacios vectoriales:
> - $V \underset{sev} \subset V$: subespacio lleno
> - $\vec{0} \underset{sev} \subset V$: subespacio nulo

También puede pasar que $V$ y $\vec{0}$ coincidan, en caso de que $V$ solo contenga a $\vec{0}$. En dicho caso, únicamente tendría un subespacio vectorial único.

Ahora, nos queda otra observación que es fundamental:

> [!Observación]
> Todo $sev$ $S \subset V$ se puede ver como un espacio vectorial.

De esta forma, cada subespacio vectorial induce un espacio vectorial más pequeño que el anterior (olvidando las partes del espacio vectorial original que no están incluidas en el mismo).

### Ejemplos de subespacios
- En $\mathbb{R}^{3}$, los subespacios vectoriales son
	- $\{ (0, 0, 0) \}$: espacio nulo.
	- Cualquier recta que pasa por el origen (debido a la definición de espacio vectorial: debe incluir al vector nulo).
	- Cualquier plano que pasa por el origen (debido a la definición de espacio vectorial).
	- $\mathbb{R}^{3} \subset \mathbb{R}^{3}$: espacio lleno.

Veremos un teorema fundamental que dicta que no hay otros subespacios vectoriales de $\mathbb{R}^{3}$.