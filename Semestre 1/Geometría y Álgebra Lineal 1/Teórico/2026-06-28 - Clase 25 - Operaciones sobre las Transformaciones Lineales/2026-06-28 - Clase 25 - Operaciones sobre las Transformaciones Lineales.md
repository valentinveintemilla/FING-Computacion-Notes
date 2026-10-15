# Espacios vectoriales

Continuamos indagando en el capítulo de transformaciones lineales:
# Transformaciones lineales

> [!Recordatorio]
> Dados dos espacios vectoriales $V, W$ sobre un mismo cuerpo $\mathbb{K}$ se dice que una función $T : V \to W$ es una <u>transformación lineal</u> cuando:
> $$
> \begin{align}
> &1. &&T(u + v) = T(u) + T(v) &&(\forall u, v \in V) \\
> &2. &&T(\alpha \cdot u) = \alpha \cdot T(u) &&(\forall \alpha \in \mathbb{K}, \forall u \in V)
> \end{align}
> $$

> [!Observación]
> De modo equivalente, $T : V \to W$ es una transformación lineal cuando
> $$
> T(\alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}) = \alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n})
> $$
> para toda combinación lineal en $V$.

Las proposiciones anteriores funcionan sin importar la dimensión de $V$, pudiendo ser infinito.

También abordamos el siguiente resultado interesante:

Dados:
- Una base $\{ v_{1}, \dots, v_{n} \} \in V \qquad (dim(V) = n)$, requiere que $V$ sea finito.
- Vectores $w_{1}, \dots, w_{n} \in W$ cualesquiera

Entonces, existe una única trasformación lineal $T : V \to W$ tal que
$$
T(v_{1}) = w_{1} \text{ y } \dots \text{ y } T(v_{n}) = w_{n}
$$
Sabiendo esto, y formando sus combinaciones lineales obtengo la imagen de la transformación lineal. Entonces, en dimensión finita, la transformación lineal tiene "contenido finito" (solo es necesario definir como se comporta para una base).

---
Ahora, pasaremos a algo nuevo: operaciones sobre las transformaciones lineales.
## Operaciones sobre las transformaciones lineales

### Proposición (estructura vectorial)

#Proposición 
> [!Proposición (estructura vectorial)]
> Sean $V, W$ espacios vectoriales:
> 1. Si $S, T : V \to W$ son transformaciones lineales, entonces, la función $S + T : V \to W$ definida por $(S + T)(v) = S(v) + T(v)$ es una transformación lineal.
> 2. Si $T : V \to W$ es una transformación lineal, entonces, para todo $\alpha \in \mathbb{K}$ la función $\alpha \cdot T$ definida por $(\alpha \cdot T)(v) = \alpha \cdot T(v)$ es una transformación lineal.
> 3. La función nula $"0" : V \to W$ es una transformación lineal.

Entonces, podemos sumar dos transformaciones lineales, multiplicar una transformación lineal por un escalar y obtengo una transformación lineal. Además, la función nula también es una transformación lineal. En conclusión, podemos definir al conjunto de las transformaciones lineales como un espacio vectorial (por lo tanto, mantiene las propiedades de los mismos).

De esta forma, las transformaciones lineales también son vectores, pero en un espacio superior de funciones.

#### Observación

> [!Observación]
> El conjunto $Lin(V, W)$ de las transformaciones lineales de $V$ a $W$ es un espacio vectorial.
> 
> De hecho:
> $$
> Lin(V, W) \underset{sev} \subset W^{V}
> $$

$W^{V}$: Espacio de "todas" las funciones de $V$ a $W$.

La notación surge de la siguiente idea: $A \to B$.
Consideramos que el dominio y el codominio tienen una cantidad de elementos finitos $\# A = a$ y $\# B = b$. Entonces, la cantidad de funciones diferentes está dada por la cantidad diferente de combinaciones que podemos hacer con dichos valores: para cada valor de $A$ se asigna un valor de $B$, por lo que tenemos que elegir entre $b$ elementos para cada $A$, $a$ veces, de esta manera:
$$
\# \text{funciones} = \underbrace{ b \times b \times \dots \times b }_{ a \text{ veces} } = b^{a}
$$
Entonces, $B^{A}$ nos recuerda a la cantidad de elementos que hay dentro (cantidad de funciones que se pueden definir).

De hecho es un subespacio del espacio de todas las funciones de $V$ a $W$ (incluyendo las que no son lineales).

Cuando tenemos dos espacios de dimensión finita, el conjunto de las transformaciones lineales generadas por dichos espacios también tiene dimensión finita, y veremos que sale del producto de las dimensiones.

Ahora, pasamos a estudiar otra propiedad:
### Proposición (compuesta)

#Proposición 
Dados:
- $U, V, W$ tres espacios vectoriales.
- $S : U \to V$ y $T : V \to W$ transformaciones lineales.
$$
U \overset{S} \longrightarrow V \overset{T} \longrightarrow W \implies U \overset{T \circ S} \longrightarrow W
$$
$$
(T \circ S)(u) := T(S(u))
$$
Entonces la función compuesta $T \circ S : U \to W$ es una transformación lineal.

Siempre el orden de escritura es inverso al orden de aplicación (las funciones que se aplican primero van "más adentro").

#### Demostración
Solo desarrollaremos una parte de la demostración.

Supongamos que $S : U \to V, T : V \to W$ son transformaciones lineales.

Queremos probar que $T \circ S : U \to W$ es una transformación lineal.

Sea $u_{1}, u_{2} \in U$
$$
\begin{align}
(T \circ S)(u_{1} +_{U} u_{2}) &= T(S(u_{1} +_{U} u_{2})) \\
&= T(S(u_{1}) +_{V} S(u_{2})) \qquad (\text{pues } S \text{ es lineal}) \\
&= \underbrace{ T(S(u_{1})) }_{ (T \circ S)(u_{1}) } +_{W} \underbrace{ T(S(u_{2})) }_{ (T \circ S)(u_{2}) } \qquad (\text{pues } T \text{ es lineal})
\end{align}
$$

Luego, queda probarlo para el producto.

Sea $u \in U$ y $\alpha \in \mathbb{K}$
$$
\begin{align}
(T \circ S)(\alpha \cdot_{U} u) &= T(S(\alpha \cdot_{U} u)) \\
&= T(\alpha \cdot_{V} S(u)) \qquad (\text{pues } S \text{ es lineal}) \\
&= \underbrace{ \alpha \cdot_{W} T(S(u)) }_{ \alpha \cdot (T \circ S)(u) } \qquad (\text{pues } T \text{ es lineal})
\end{align}
$$

Simplemente, se trata de probar que se comporta como lo especificamos en la definición.

Ahora, presentaremos otra proposición:
### Proposición (inversa)

#Proposición 
> [!Proposición (inversa)]
> Sean $V, W$ espacios vectoriales.
> 
> Si $T : V \to W$ es una transformación lineal biyectiva, entonces su inversa $T^{-1} : W \to V$ es una transformación lineal.

Una transformación lineal biyectiva $T : V \to W$ es aquella que asocia un elemento único de $W$ dada una entrada específica de $V$. En tal contexto, la transformación lineal se puede invertir y su inversa también es una transformación lineal.

#### Demostración
La demostración no es trivial. El truco está en hacer aparecer la función $T$ durante el desarrollo.

Como $T$ es biyectiva: $w = T(T^{-1}(w))$. Esto es válido ya que si tenemos una función y su inversa, y componemos ambas, el resultado es el parámetro pasado como entrada. O sea, se cancelan ambos y queda lo de adentro: $\cancel{ f^{-1}(f }(x)) = \cancel{ f(f^{-1} }(x)) = x$

Sean $w_{1}, w_{2} \in W$.
$$
\begin{align}
T^{-1}(w_{1} + w_{2}) &= T^{-1}(T(T^{-1}(w_{1})) + T(T^{-1}(w_{2}))) \\
&= \cancel{ T^{-1}(T( }T^{-1}(w_{1}) + T^{-1}(w_{2}))) \qquad (\text{pues } T \text{ es lineal}) \\
&= T^{-1}(w_{1}) + T^{-1}(w_{2}) \qquad (\text{pues } T \text{ es lineal})
\end{align}
$$

Se desarrolla la misma idea para el producto por un escalar (es análogo).

---
Ahora, pasaremos a estudiar terminología, comenzando por categorizaciones de transformaciones lineales:

### Terminología
Una transformación lineal biyectiva también se llama un isomorfismo lineal.

Isomorfismo = Igual forma (ambos espacios tienen igual forma).

Veremos que el tener la misma forma nos permite viajar entre dos espacios libremente, y entenderemos que a través de un isomorfismo lineal:
- una base tiene como imagen una base
- un conjunto LI tiene como imagen un conjunto LI
- un generador tiene como imagen un generador

Algunos ejemplos simples:
$$
\begin{align}
&\mathbb{R}_{n}[x] = \mathbb{R}^{n + 1} \\
&\mathcal{M}_{m \times n} = \mathbb{R}^{mn}
\end{align}
$$
El sentido de las matrices es el producto de matrices (operación que las hace únicas y les da significado). Sin embargo, el resto de problemas se pueden resolver como un vector con $m \times n$ componentes.

Entonces, si tenemos un problema que sabemos resolver en $V$, también lo sabemos resolver en $W$, teniendo una función que nos permita viajar entre ambos espacios vectoriales.

#### Ejemplo

Sean $\overbrace{ v_{1}, \dots, v_{n} }^{ A } \in V$.

$$
\phi_{A} : \mathbb{K}^{n} \to V
$$
definida por
$$
(\alpha_{1}, \dots, \alpha_{n}) \mapsto \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}
$$

Es una transformación lineal, ya que si sumo $n$ n-uplas, obtendré n-combinaciones lineales de $n$ vectores.

$\phi_{A}$ es:
- Inyectiva $\Longleftrightarrow A$ es LI.
- Sobreyectiva $\Longleftrightarrow A$ es generador.
- Biyectiva $\Longleftrightarrow A$ es una base.

Inyectiva: todo vector del espacio $V$ tiene descomposición única en función de $\phi_{A}$.

También podemos definir la función inversa: la función recíproca de $\phi_{A} : \mathbb{K}^{n} \to V$ es la función coordenadas $coord_{A} : V \to \mathbb{K}^{n}$.

Esto quiere decir que cada vez que tenemos una base, tenemos un isomorfismo lineal entre $V$ y $\mathbb{K}^{n}$. Entonces, ==todos los espacios vectoriales de dimensión finita, específicamente dimensión $n$, tienen la misma forma que $\mathbb{K}^{n}$==. Entonces, sabiendo resolver ejercicios en $\mathbb{K}^{n}$, sabemos resolver problemas en cualquier espacio de dimensión finita.

De esta manera, podemos clasificar a los espacios vectoriales según su dimensión: ==dos espacios vectoriales tienen la misma forma, si y sólo si tienen la misma dimensión==.

Esto quiere decir que tenemos un diccionario, pues el sistema de base de coordenadas nos permite pasar entre los espacios vectoriales y las n-uplas.
$$
\begin{align}
&coord_{A} : V \to \mathbb{K}^{n} \\
&coord_{B} : W \to \mathbb{K}^{m}
\end{align}
$$
$$
\begin{align}
&\text{vector } u \in V \mapsto \text{n-upla } (\alpha_{1}, \dots, \alpha_{n}) \in \mathbb{K}^{n} \\
&\text{vector } w \in W \mapsto \text{m-upla } (\beta_{1}, \dots, \beta_{m}) \in \mathbb{K}^{m}
\end{align}
$$
Ahora, para las transformaciones lineales:
$$
\text{una T.L. } T : V \to W \mapsto \text{matriz } \in \mathcal{M}_{m \times n}
$$
Entonces, la cantidad de columnas es la dimensión del espacio de partida, y la cantidad de columnas está dada por la dimensión del espacio de llegada.

Esto permitirá ver que, al final, las matrices son las representaciones naturales de las transformaciones lineales:

## Matriz asociada

Ahora se considera la siguiente situación.

- Un espacio vectorial $V$ con una base $A = \{ v_{1}, \dots, v_{n} \}$ ($dim V = n$)
- Un espacio vectorial $W$ con una base $B = \{ w_{1}, \dots, w_{m} \}$ ($dim W = m$)

Matriz asociada - Definición

#Definición 
Sea $T : V \to W$.

La matriz asociada a $T$ en las base $A$ y $B$ es la matriz de tamaño $m \times n$, escrita $_{B}(T)_{A}$, está definida
$$
_{B}(T)_{A} = \begin{pmatrix}
coord_{B}(T(v_{1})) & \dots & coord_{B}(T(v_{n}))
\end{pmatrix}
$$
Es decir, la i-ésima columna de $_{B}(T)_{A}$ es $coord_{B}(T(v_{i}))$.

- $v$: vectores de la base de partida, $n$ componentes = $n$ columnas.
- $coord_{B}(T(v))$: coordenadas en la base de llegada, $m$ componentes = $m$ filas.

Las coordenadas se "estiran" verticalmente, el primer componente de la coordenada de $v_{1}$ va en la celda $(1, 1)$, la segunda coordenada del vector $v_{1}$ va en $(2, 1)$, así sucesivamente.

O sea, partimos del conjunto de partida y aplicamos transformación lineal a cada vector. Luego, extraemos las coordenadas de cada transformación, y construimos la matriz con dicha información. De la misma, se pueden extraer las columnas que contienen a las coordenadas de las transformaciones, permitiendo comprender las transformaciones, y con algo de trabajo, los vectores originales.

Entonces:
- Cuando sumemos transformaciones lineales, sumamos matrices.
- Cuando calculemos el producto de una transformación lineal por un escalar, se corresponde con el producto de una matriz por un escalar.
- Cuando compongamos transformaciones lineales, desarrollaremos el producto entre ambas matrices asociadas.
- Cuando tomemos la transformación lineal inversa, invertimos la matriz.

En conclusión: las matrices representan transformaciones lineales en dimensión finita, y permiten manejarlas cómodamente.

A continuación, estudiaremos algunos ejemplos:
### Ejemplos

1. Hallar la matriz asociada a la transformación lineal
$$
\begin{align}
&T : \mathbb{R}^{2} \to \mathbb{R}^{3} \\
&(x, y) \mapsto (4x - 2y, 2x + y, x + y)
\end{align}
$$
en las bases canónicas de $\mathbb{R}^{2}$ y $\mathbb{R}^{3}$.
$$
\begin{align}
&A = \{ (1, 0), (0, 1) \} \\
&B = \{ (1, 0, 0), (0, 1, 0), (0, 0, 1) \}
\end{align}
$$
$$
\begin{align}
&T(1, 0) = (4, 2, 1) \\
&T(0, 1) = (-2, 1, 1)
\end{align}
$$
$$
_{B}(T)_{A} = \begin{pmatrix}
4 & -2 \\
2 & 1 \\
1 & 1
\end{pmatrix}
$$
Esta matriz contiene toda la información necesaria para comprender la transformación lineal.

**Observación**
Podemos reconstruir la transformación lineal a partir de la matriz asociada:
$$
\begin{pmatrix}
4 & -2 \\
2 & 1 \\
1 & 1
\end{pmatrix} \cdot \begin{pmatrix}
x \\
y
\end{pmatrix} = \begin{pmatrix}
4x - 2y \\
2x + y \\
x + y
\end{pmatrix} = T(x, y)
$$

Este es el caso más simple, ya que las bases manejadas son canónicas. Ahora, veremos uno con bases no canónicas.

2. $$
T : \mathbb{R}_{2}[x] \to \mathbb{R}^{2}
$$
definida para todo polinomio $p(t) = at^{2} + bt + c$ por
$$
T(p) = (2a + b, a+ b + 4c)
$$

Hallar la matriz asociada en las bases:
$$
\begin{align}
&A = \{ t^{2}, t, 1 \} \\
&B = \{ (1, 1), (1, 0) \}
\end{align}
$$

Tenemos que calcular las imágenes de todos los vectores de la base del espacio de partida:
$$
\begin{align}
&T(t^{2}) = (2, 1) = 1 \cdot (1, 1) + 1 \cdot (1, 0) \\
&T(t) = (1, 1) = 1 \cdot (1, 1) + 0 \cdot (1, 0) \\
&T(1) = (0, 4) = 4 \cdot (1, 1) - 4 \cdot (1, 0) \\
\end{align}
$$
Estos vectores están expresados en la base canónica de $\mathbb{R}^{2}$, por lo que tenemos que ajustarlos a la base $B$ (segunda igualdad).

Entonces, sabemos las coordenadas en la base $B$ de cada transformación:
$$
\begin{align}
&coord_{B}(T(t^{2})) = (1, 1) \\
&coord_{B}(T(t)) = (1, 0) \\
&coord_{B}(T(1)) = (4, -4) \\
\end{align}
$$
Luego, podemos definir la matriz asociada:
$$
_{B}(T)_{A} = \begin{pmatrix}
1 & 1 & 4 \\
1 & 0 & -4
\end{pmatrix}
$$

