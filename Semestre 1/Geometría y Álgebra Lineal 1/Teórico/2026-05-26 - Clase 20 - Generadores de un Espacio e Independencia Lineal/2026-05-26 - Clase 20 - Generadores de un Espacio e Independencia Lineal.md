# Espacios vectoriales
Proseguimos con el problema de las combinaciones lineales, noción abordada la clase anterior:
## Combinaciones lineales

> [!Recordatorio]
> Sea $V$ un espacio vectorial.
> 
> Sean $u_{1}, \dots, u_{n} \in V$. Se dice que un vector $u \in V$ es combinación lineal de $\{ u_{1}, \dots, u_{n} \}$ cuando existen $\alpha_{1}, \dots, \alpha_{n} \in K$ tales que
> $$
> u = \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n}
> $$

Es la noción central de la teoría de los espacios vectoriales.

La definición anterior también funciona para una familia vacía de vectores, siendo el resultado de la suma 0, por lo que el único vector que es combinación lineal del conjunto vacío es el vector nulo.

Además, tenemos una observación en base a la definición de combinación lineal, la cual establece que si tengo un espacio vectorial estable por cualquier combinación lineal dentro del mismo, quiere decir que es estable por suma, tiene el vector nulo, es estable por producto de un escalar, etc.

> [!Observación]
> Todo subespacio vectorial es "estable" por combinación lineal.
> 
> Si $u_{1}, \dots, u_{n} \in S$, entonces $\alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} \in S$ ($\forall \alpha_{1}, \dots, \alpha_{n} \in K$).

También abordamos el concepto de "subespacio generado":

### Subespacio generado

Dado un subconjunto $A \subset V$ <u>cualquiera</u>, el subespacio generado por $A$, escrito $[A]$, es el conjunto de todas las combinaciones lineales de vectores de $A$
$$
[A] = \left\{ \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} : \begin{align}
&n \geq 0, \\
&u_{1}, \dots, u_{n} \in A \\
&\alpha_{1}, \dots, \alpha_{n} \in K
\end{align} \right\}
$$

Dicho conjunto es más grande que $A$, y es un subespacio vectorial (ya que es estable por cualquier combinación lineal).

#### Ejemplos
$$
[\emptyset] = \{ \vec{0} \}
$$
$$
[\{ u \}] = \{ \alpha \cdot u : \alpha \in K \}
$$
Si se tiene exactamente un vector, el subespacio generado es la recta vectorial generada por $u$ si $u \neq \vec{0}$.
$$
[\{ u, v \}] = \{ \alpha \cdot u + \beta \cdot v : \alpha, \beta \in K \}
$$
El caso general será un plano vectorial, pero puede no serlo. Si ambos son nulos, es el vector nulo. Si ambos son colineales, es un recta vectorial.

> [!Observación]
> Siempre se consideran combinaciones lineales finitas.

De esta forma, cuando tengamos un conjunto infinito, para construir un combinación lineal, se extrae una parte finita del conjunto y se desarrolla la combinación lineal sobre el mismo.

Veremos un ejemplo sobre esto:
#### Ejemplo
Sea $V = \mathbb{R}^{\mathbb{R}} = \{ \text{funciones } f : \mathbb{R} \to \mathbb{R} \}$ (todas las funciones de $\mathbb{R}$ en $\mathbb{R}$)
Sea $A = \{ (x \mapsto x^{n}) \}$ (función que a $x$ asocia $x^{n}$ - conjunto de todos los monomios)

Si consideramos todas las combinaciones lineales de monomios, obtendremos exactamente los polinomios:
$$
[A] = \mathbb{R}[X] \qquad \text{(espacio de polinomios)}
$$
Tengo una cantidad infinita de monomios, pero cada polinomio esta conformado por una cantidad finita de monomios. Cuando consideramos el espacio generado, nunca realizamos combinaciones infinitas, incluso cuando el espacio del que partimos es infinito.

Por construcción, $[A]$ es el mínimo subespacio de $V$ que contiene $A$ como subconjunto. Es decir:
$$
\begin{align}
&\text{para todo } A \subset V \\
&\text{para todo } S \underset{sev} \subset V
\end{align}
\qquad \text{tenemos que}
\qquad A \subset S \Longleftrightarrow [A] \underset{sev} \subset S
$$
$$
A \subset [A] \underset{sev} \subset S
$$
Si partimos de un conjunto de vectores que está incluido en $S$ (un subespacio vectorial), el espacio generado a partir de $A$ (con todas las combinaciones lineales de $A$) también estará incluido en $S$. Además, siempre se cumple la equivalencia anterior: un conjunto de vectores siempre es subconjunto del espacio generado a partir del mismo, y además son subconjuntos del subespacio vectorial del que partimos.

---
A continuación, hablaremos de generadores de espacios vectoriales:
### Generador de un espacio

Se dice que $A \subset V$ es un generador de $V$ cuando $V = [A]$.

Del mismo modo, si $S \underset{sev} \subset S$ se dice que $A$ es un generador de $S$ cuando $[A] = S$ (esto implica $A \subset S$).

Necesariamente, para generar un subespacio, se tienen que tomar vectores que ya estén en el subespacio, puesto que si no se generará algo más grande (el resultado -subespacio generado- no será un subconjunto del subespacio).

En general, nos interesan los generadores mínimos. Extender un generador no cambia la propiedad de ser generador (si se tiene un generador y se le agregan elementos, aún será generador, simplemente será redundante).

> [!Observación]
> Si $G \subset V$ es generador, entonces $G'$ es generador para todo $G' \subset V$ tal que $G \subset G'$.

Si tengo un generador, entonces todo conjunto que lo contenga también será un generador.

Esto nos llevará a la intuición de base (generador mínimo).

#### Ejemplos
- Generador de $M_{2 \times 2}$.
El generador más sencillo es el siguiente:
$$
\left\{ \begin{pmatrix}
1 && 0 \\ 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 1 \\ 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 \\ 1 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 \\ 0 && 1
\end{pmatrix} \right\}
$$
es generado, pues
$$
\begin{pmatrix}
\alpha && \beta \\ \gamma && \delta
\end{pmatrix} = \alpha \begin{pmatrix}
1 && 0 \\ 0 && 0
\end{pmatrix} + \beta \begin{pmatrix}
0 && 1 \\ 0 && 0
\end{pmatrix} + \gamma \begin{pmatrix}
0 && 0 \\ 1 && 0
\end{pmatrix} + \delta \begin{pmatrix}
0 && 0 \\ 0 && 1
\end{pmatrix}
$$
Este generador es mínimo. Se pueden agregar más vectores y seguiría siendo generador (pero no mínimo).

Otro generador:
$$
\left\{ \begin{pmatrix}
1 && 0 \\ 0 && 1
\end{pmatrix}, \begin{pmatrix}
0 && 1 \\ 1 && 0
\end{pmatrix}, \begin{pmatrix}
1 && 0 \\ 1 && 0
\end{pmatrix}, \begin{pmatrix}
1 && 1 \\ 0 && 0
\end{pmatrix} \right\}
$$En este espacio, siempre tendremos al menos 4 vectores (nunca menos).
Luego veremos que la cantidad de vectores necesarios para formar una base está relacionado con la noción de dimensión (en este caso, como cada matriz tiene cuatro componentes, la dimensión sería 4).

- Generador del subespacio de las matrices simétricas de tamaño $2 \times 2$.
Sabemos que todas las matrices $2 \times 2$ simétricas siguen la forma:
$$
\begin{pmatrix}
\alpha && \beta \\ \beta && \delta
\end{pmatrix}
$$
Entonces, podemos considerar el generador:
$$\left\{ \begin{pmatrix}
1 && 0 \\ 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 1 \\ 1 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 \\ 0 && 1
\end{pmatrix} \right\}$$
Podemos decir que este subespacio es de dimensión 3.

- Generador del espacio de las matrices antisimétricas de tamaño $2 \times 2$.
Sabemos que todas las matrices $2 \times 2$ simétricas siguen la forma:
$$
\begin{pmatrix}
0 && \beta \\ -\beta && 0
\end{pmatrix}
$$Entonces, podemos considerar el generador:
$$\left\{ \begin{pmatrix}
0 && 1 \\ -1 && 0
\end{pmatrix} \right\}$$
También es el generador más pequeño. Por lo tanto, podemos decir que este subespacio es de dimensión 1 (lo estudiaremos posteriormente en el curso).

- Matrices simétricas y antisimétricas de tamaño $3 \times 3$ (todas las matrices de tamaño $3 \times 3$).
Comenzamos por las simétricas:
$$
\begin{pmatrix}
\alpha && \beta && \gamma \\
\beta && \delta && \epsilon \\
\gamma && \epsilon && \eta
\end{pmatrix}
$$
$$
G = \left\{ \begin{pmatrix}
1 && 0 && 0 \\ 0 && 0 && 0 \\ 0 && 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 1 && 0 \\ 1 && 0 && 0 \\ 0 && 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 && 1 \\ 0 && 0 && 0 \\ 1 && 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 && 0 \\ 0 && 1 && 0 \\ 0 && 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 && 0 \\ 0 && 0 && 1 \\ 0 && 1 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 && 0 \\ 0 && 0 && 0 \\ 0 && 0 && 1
\end{pmatrix} \right\}
$$
Hasta ahora, vamos 6 elementos (dimensión del espacio de matrices simétricas $3 \times 3$, por lo que para completar las "9 dimensiones" nos faltarían tres casos referentes a las matrices antisimétricas.

Matrices antisimétricas:
$$
G' = \left\{ \begin{pmatrix}
0 && 1 && 0 \\ -1 && 0 && 0 \\ 0 && 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 && 1 \\ 0 && 0 && 0 \\ -1 && 0 && 0
\end{pmatrix}, \begin{pmatrix}
0 && 0 && 0 \\ 0 && 0 && 1 \\ 0 && -1 && 0
\end{pmatrix} \right\}
$$
Como vemos, tiene 3 dimensiones.

Como vemos, la suma de las dimensiones de las matrices simétricas y antisimétricas da como resultado la dimensión de todas las matrices. Como vemos, hay más matrices simétricas que antisimétricas.

Como los generadores se pueden extender y aún así ser generadores, lo difícil es reducir generadores, encontrar cuales vectores son redundantes.

A continuación, abordamos una proposición:

#### Proposición

> [!Proposición]
> Sea $A \subset V$ (subconjunto de $V$).
> 
> Si un vector $v \in A$ es combinación lineal de los restantes vectores de $A$, entonces $[A \setminus \{ v \}] = [A]$

De esta forma, si sabemos que existe un vector en el subconjunto, el cual es combinación lineal de otros vectores ya pertenecientes al mismo, se puede remover este, y el espacio generado de $A$ y el espacio generado del resultado de extraer dicho vector de $A$ son equivalentes.

##### Demostración

Para demostrar la proposición, simplemente tenemos que demostrar que ambos conjuntos son equivalentes, cumpliéndose que $[A \setminus \{ v \}] \subset [A]$ y $[A] \subset [A \setminus \{ v \}]$.

$[A \setminus \{ v \}] \subset [A]$: obvio, pues $A \setminus \{ v \} \subset A$.

Demostremos que $[A] \subset [A \setminus \{ v \}]$.

Sea $u \in [A]$. Existen vectores $v_{1}, \dots, v_{n} \in A$ y coeficientes $\alpha_{1}, \dots, \alpha_{n} \in K$ tales que $u = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}$.

Ahora, tenemos que analizar los vectores $v_{1}, \dots, v_{n}$.

Dos casos posibles:
1. $v$ no aparecen en $\{ v_{1}, \dots, v_{n} \}$, es decir $v \neq v_{i} \qquad (1 \leq i \leq n)$.
Tenemos que $v_{1}, \dots, v_{n} \in A \setminus \{ v \}$.
Luego $u = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n} \in [A \setminus \{ v \}]$.

Como $v_{1}, \dots, v_{n} \in A \setminus \{ v \}$, entonces cualquier combinación lineal conformada por los vectores anteriores pertenece a $[A \setminus \{ v \}]$.

2. $v = v_{i}$ para algún $i \in [1..n]$. Sin pérdida de generalidad, se puede suponer que $v = v_{n}$.
Sabemos que $v = \beta_{1} \cdot w_{1} + \dots + \beta_{p} \cdot w_{p}$, donde $w_{1}, \dots, w_{p} \in A \setminus \{ v \}$, $\beta_{1}, \dots, \beta_{n} \in K$.

($A \setminus \{ v \}$: Vectores de $A$ restantes (después de haber restado $v$).)

Entonces:
(Lo que haremos es reemplazar $v_{n}$ por la combinación lineal que lo conforma:)
$$
\begin{align}
u &= \alpha_{1} \cdot v_{1} + \dots + \alpha_{n - 1} \cdot v_{n - 1} + \alpha_{n} \cdot \overbrace{ v_{n} }^{ = v } \\
&= \alpha_{1} \cdot v_{1} + \dots + \alpha_{n - 1} \cdot v_{n - 1} + \alpha_{n} \cdot \left( \beta_{1} \cdot w_{1} + \dots + \beta_{p} \cdot w_{p} \right) \\
&= \alpha_{1} \cdot v_{1} + \dots + \alpha_{n - 1} \cdot v_{n - 1} + (\alpha_{n} \beta_{1} )\cdot w_{1} + \dots + (\alpha_{n} \beta_{p}) \cdot w_{p}
\end{align}
$$
Ahora, podemos ver que eliminamos a $v$ de la ecuación, al sustituirlo por la combinación lineal que lo conforma (en función de los vectores restantes).

Luego:
$$
u \in [A \setminus \{ v \}]
$$

Esto concluye la demostración.

De esta forma, la idea es escribir un vector $u$ como combinación lineal, pudiendo no haber un vector problemático, o en caso de haberlo, lo sustituyo por la combinación lineal que lo conforma (en base a los vectores restantes), y esto no cambia el espacio generado.

Lo importante de todo esto es recordar las ideas desarrolladas y de donde surgen las mismas, así como saber expresarlas con símbolos.

Es fundamental trabajar "la función simbólica", ser capaz de comprender rápidamente que representa/significa/grafica una idea o concepto. Por ejemplo, cuando vemos la palabra "mesa", instantáneamente pensamos en una mesa.

---
Ahora, pasaremos a otro de los temas centrales del capítulo: independencia lineal.
### Independencia lineal

Familias L.D. y L.I.

> [!Familias L.D. y L.I. - Definición]
> En un espacio vectorial $V$, se dice que una familia $u_{1}, \dots, u_{n} \in V$ es:
> - Linealmente dependiente (L.D.) si existen escalares $\alpha_{1}, \dots, \alpha_{n} \in K$ <u>no todos nulos</u> tales que
> $$
> \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} = \vec{0}
> $$
> 
> - Linealmente independiente (L.I.) si para todos $\alpha_{1}, \dots, \alpha_{n} \in K$
> $$
> \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} = \vec{0} \implies \alpha_{1} = \alpha_{2} = \dots = \alpha_{n} = 0
> $$


Ambos casos son excluyentes, no existe una familia que cumpla ambos.

En L.D. no todos pueden ser nulos puesto que es un caso trivial.

Además, podemos confirmar que, teniendo el vector nulo en una familia, la misma siempre será linealmente dependiente, ya que podemos considerar el escalar nulo para todos los demás vectores y cualquier otro escalar para el vector nulo, obteniendo $\vec{0}$.

En L.I. solo la combinación nula puede cancelar la familia.

Esta es una noción de dependencia grupal, hay un vínculo entre los elementos dado por la combinación lineal:
1. L.D.: existencia de un vínculo entre los vectores de la familia.
2. L.I.: ausencia de un vínculo entre los vectores de la familia.

En base a lo anterior, realizamos algunas observaciones:

> [!Observaciones]
> Sean $u_{1}, \dots, u_{n} \in V$.
> 1. Si algún $v_{i} = \vec{0}$, entonces $\{ u_{1}, \dots, u_{n} \in V \}$ es L.D.
> 2. En general $\{ u \}$ es L.I., salvo cuando $u = \vec{0}$.

(1) Dentro de la familia existe el vector nulo, el cual se puede reconstruir trivialmente a partir de los otros. Ese es el vínculo.

(2) Como no puedo utilizar un escalar nulo en este caso, en general se tiene que dar que el vector sea nulo para que la familia sea L.D..

La definición establece que los elementos de la familia son dependientes entre sí, pero no determina si uno es dependiente del resto. Veremos que ambas cosas son equivalentes:

#### Proposición

> [!Proposición]
> Una familia finita  $\{ u_{1}, \dots, u_{n} \} \in V$ es L.D. si y sólo si existe algún vector $v_{i} (1 \leq i \leq n)$ es combinación lineal de los restantes vectores $vj$, (con $j \neq i$).

De esta forma, la dependencia demuestra que existe un vector que se puede expresar en función del resto. Pero este vector no tiene porque ser único.

Ahora, veremos que ambos puntos de vista (proposición y definición) son equivalentes.

##### Demostración
($\implies$) Supongamos que $\{ u_{1}, \dots, u_{n} \}$ es L.D, es decir:
Existe $\alpha_{1}, \dots, \alpha_{n}$ no todos nulos tales que $\alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} = \vec{0}$. Sea $i$ un índice (entre 1 y $n$) tal que $\alpha_{i} \neq 0$.

Tenemos que:
$$
\alpha_{i} \cdot v_{i} + \sum_{j \underset{j \neq i} = 1}^{n} \alpha_{j} \cdot v_{j} = \vec{0}
$$
(Índice $i$ por la izquierda y el resto por la derecha.)
$$
\alpha_{i} \cdot v_{i} = -\sum_{j \underset{j \neq i} = 1}^{n} \alpha_{j} \cdot v_{j} \implies v_{i} = -\sum_{j \underset{j \neq i} = 1}^{n} \frac{\alpha_{j}}{\alpha_{i}} \cdot v_{j}
$$
De esta forma, $v_{i}$ es combinación lineal del resto (no se incluye $v_{i}$, ya que se ignora dicho índice).

Funciona del mismo modo al revés (recíproco):
($\impliedby$) Supongamos que
$$
v_{i} = \sum_{j \underset{j \neq i} = 1}^{n} \beta_{j} \cdot v_{j}
$$
Entonces tenemos que
$$
\sum_{j \underset{j \neq i} = 1}^{n} \beta_{j} \cdot v_{j} - v_{i} = \vec{0}
$$
Escribiendo $\beta_{i} = -1$, obtenemos
$$
\sum_{j = 1}^{n} \beta_{j} \cdot v_{j} = \vec{0}
$$
(Agregamos el vector $v_{j}$ a la suma del resto de vectores, asegurando que se mantiene la igualdad. Además, se sabe que tiene al menos un coeficiente no nulo: $\beta_{i} = -1$).

Es así que obtuvimos una familia de coeficientes que se cancela y tiene al menos un coeficiente no nulo.

Luego $\{ v_{1}, \dots, v_{n} \}$ es L.D.

Es así que demostramos que una familia es linealmente dependiente si hay al menos un vector que se puede expresar como combinación de los demás, y es linealmente independiente en el caso de que ningún miembro de la familia se pueda expresar como combinación del resto.