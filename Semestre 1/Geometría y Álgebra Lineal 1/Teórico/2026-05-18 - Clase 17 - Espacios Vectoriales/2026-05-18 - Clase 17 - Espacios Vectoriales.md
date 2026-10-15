# Espacios vectoriales
En esta clase, comenzaremos con un nuevo capítulo: espacios vectoriales.
Abordaremos la noción más general de vector posible. Hasta ahora hemos visto vectores en geometría, n-uplas, vectores columnas y filas, matrices, etc. Todos estos son ejemplos de espacios vectoriales.

Antes de abordar esto, tenemos que hablar de la noción de número y cuerpo:
## Cuerpo ($\mathbb{Q}, \mathbb{R}, \mathbb{C}, \dots$)
Es un conjunto de número con las cuatro operaciones (suma, resta, multiplicación y división) bien definidas.

> [!Cuerpo - Definición]
> Un cuerpo es un conjunto $K$ equipado con dos operaciones $+, \times$ tales que:
> 
> **Propiedades de la suma**
> - $+$ es asociativa y conmutativa:
> $$
> (\alpha + \beta) + \gamma = \alpha + (\beta + \gamma)
> $$
> $$
> \alpha + \beta = \beta + \alpha
> $$
> - $+$ tiene elemento neutro $0 \in K$:
> $$
> \alpha + 0 = \alpha
> $$
> - Cada elemento $\alpha \in K$ tiene opuesto $-\alpha \in K$:
> $$
> \alpha + (-\alpha) = 0
> $$
> Esto permite definir la resta por:
> $$
> \alpha - \beta := \alpha + (-\beta)
> $$
> 
> **Propiedades del producto**
> - $\times$ es asociativo y conmutativo:
> $$
> (\alpha \beta)\gamma = \alpha(\beta \gamma) \qquad (\alpha \beta := \alpha \times \beta)
> $$
> $$
> \alpha \beta = \beta \alpha
> $$
> - $\times$ tiene elemento neutro $1 \neq 0 \qquad (1 \in K)$:
> $$
> 1 \alpha = \alpha
> $$
> - $\times$ es distributivo respecto a $+$:
> $$
> \alpha(\beta + \gamma) = \alpha \beta + \alpha \gamma
> $$
> - Cada elemento $\alpha \neq 0$ tiene inversa $\alpha^{-1} \in K$
> $$
> \alpha \alpha^{-1} = 1
> $$
> Esto permite definir la división $\frac{\alpha}{\beta}$ por:
> $$
> \frac{\alpha}{\beta} := \alpha \beta^{-1} \qquad (\text{si } \beta \neq 0)
> $$

### Ejemplos y contraejemplos
- $\mathbb{N}$ no es un cuerpo, pues $1 \in \mathbb{N}$ no tiene opuesto (en $\mathbb{N}$).
Es un conjunto en el que las operaciones suma y producto funcionan sin problema, pero no la resta, y la división también presenta algunos problemas (solo existe el inverso para 1).

- $\mathbb{Z}$ no es un cuerpo, pues $2 \in \mathbb{Z}$ no tiene inverso ($\mathbb{Z}$ es un anillo). Cumple todas las propiedades menos la última.
En este caso, la resta está bien definida, pero no la división.

- $\mathbb{Q}$, $\mathbb{R}$ y $\mathbb{C}$ son cuerpos.

En cálculo I vimos los axiomas de $\mathbb{R}$. Los primeros axiomas sirven para determinar que $\mathbb{R}$ es un cuerpo, pero también se agrega el orden (relación). No es el caso de todos los cuerpos (un cuerpo puede no tener orden, no interesa comparar los números). Por ejemplo, $\mathbb{Q}$ y $\mathbb{R}$ tienen orden, pero $\mathbb{C}$ no.

Los cuerpos tampoco tienen por que ser infinitos (como los ejemplos vistos). Pueden ser finitos:
- El conjunto $\mathbb{Z}_{2} = \{ 0, 1 \}$ con la suma y el producto definidos por:

| $+$ |  0  |  1  |
| :-: | :-: | :-: |
|  **0**  |  0  |  1  |
|  **1**  |  1  |  0  |
No podemos definir $1 + 1 = 1$, ya que determinamos que $1 = 0$ y habíamos establecido que $1 \neq 0$. Por lo tanto, $1 + 1 = 0$.

| $\times$ |  0  |  1  |
| :------: | :-: | :-: |
|  **0**   |  0  |  0  |
|  **1**   |  0  |  1  |
Si consideramos los opuestos, sabemos que $-0 = 0$, y como $1 + 1 = 0$, entonces $-1 = 1$.
Hablando de los cocientes, podemos determinar que $\frac{1}{1} = 1$ y no consideramos a 0 porque no tiene inverso.

De esta forma, tenemos una suma y un producto que cumple todos los axiomas anteriores. Por lo tanto: $\mathbb{Z}_{2}$ es un cuerpo. De hecho, es el cuerpo más pequeño del universo, puesto que un cuerpo debe tener como mínimo 2 elementos.
Dicho conjunto se corresponde con las operaciones binarias.

Existen otros cuerpos finitos:

- El conjunto $Z_{3} = \{ 0, 1, 2 \}$

|  $+$  |  0  |  1  | **2** |
| :---: | :-: | :-: | :---: |
| **0** |  0  |  1  |   2   |
| **1** |  1  |  2  |   0   |
| **2** |  2  |  0  |   1   |
Como vemos, se forma un ciclo en las celdas.
En base a la tabla:
$$
\begin{align}
&-0 = 0 \\
&-1 = 2 \\
&-2 = 1
\end{align}
$$
Aclaración: para obtener el opuesto de un número, observo la celda que contenga 0 en la fila o columna de ese número.

| $\times$ |  0  |  1  | **2** |
| :------: | :-: | :-: | :---: |
|  **0**   |  0  |  0  |   0   |
|  **1**   |  0  |  1  |   2   |
|  **2**   |  0  |  2  |   1   |
$$
\begin{align}
&1^{-1} = 1 \\
&2^{-1} = 2
\end{align}
$$
Aclaración: para obtener el inverso de un número, observo la celda que contenga 1 en la fila o columna de ese número.
Esto es un cuerpo con 3 elementos. Se puede verificar que todas las propiedades se cumplen.

- El conjunto $\mathbb{Z}_{5} = \{ 0, 1, 2, 3, 4 \}$

|  $+$  |  0  |  1  | **2** |  3  |  4  |
| :---: | :-: | :-: | :---: | :-: | :-: |
| **0** |  0  |  1  |   2   |  3  |  4  |
| **1** |  1  |  2  |   3   |  4  |  0  |
| **2** |  2  |  3  |   4   |  0  |  1  |
| **3** |  3  |  4  |   0   |  1  |  2  |
| **4** |  4  |  0  |   1   |  2  |  3  |

En base a la tabla:
$$
\begin{align}
&-0 = 0 \\
&-1 = 4 \\
&-2 = 3 \\
&-3 = 2 \\
&-4 = 1
\end{align}
$$

| $\times$ |  0  |  1  | **2** |  3  |  4  |
| :------: | :-: | :-: | :---: | :-: | :-: |
|  **0**   |  0  |  0  |   0   |  0  |  0  |
|  **1**   |  0  |  1  |   2   |  3  |  4  |
|  **2**   |  0  |  2  |   4   |  1  |  3  |
|  **3**   |  0  |  3  |   1   |  4  |  2  |
|  **4**   |  0  |  4  |   3   |  2  |  1  |
$$
\begin{align}
&1^{-1} = 1 \\
&2^{-1} = 3 \\
&3^{-1} = 2 \\
&4^{-1} = 4
\end{align}
$$

Podemos resolver las operaciones de la tabla tomando como referencia que $5 = 0$, entonces $6 = 1$, $7 = 2$, etc.

De esta forma, $\mathbb{Z}_{5}$ es un cuerpo.

No realizamos el ejemplo $\mathbb{Z}_{4}$ ya que no es un cuerpo. Se puede demostrar. Lo que termina sucediendo es que 2 no tiene inverso (no aparece un 1 en su fila ni columna de la tabla del producto). De esta forma, es un anillo y no un cuerpo.

Si vamos más allá, podemos comprobar que obtenemos un cuerpo solo cuando el número de elementos es primo (cuando se trata de un conjunto finito).

Lo que es importante entender es que las operaciones funcionan exactamente igual que en los conjuntos usuales.

Hasta aquí la noción de cuerpo.

---
Continuamos con la noción de espacio vectorial.
## Espacios vectoriales

> [!Espacio vectorial - Definición]
> Un espacio vectorial es una cuádrupla $(K, V, +, \cdot)$ donde:
> - $K$ es un cuerpo, cuyos elementos se llaman <u>escalares</u>
> - $V$ es un conjunto no vacío, cuyos elementos se llaman <u>vectores</u>
> - Una operación $(+) : V \times V \to V \qquad (\ll \text{suma de vectores} \gg)$
> - Otra operación $(\cdot) : K \times V \to V \qquad (\ll \text{producto de un vector por un escalar} \gg)$
> 
> Además, la **suma** cumple los siguientes axiomas:
> $$
> \begin{align}
> &(S1) &&(u + v) + w = u + (v + w) && (\text{para todos } u, v, w \in V) \\
> &(S2) &&u + v = v + u && (\text{para todos } u, v \in V) \\
> &(S3) &&(+) \text{ tiene elemento nuetro: } \vec{0 \in V} \\
> &&&u + \vec{0} = \vec{0} + u = u \\
> &(S4) &&\text{Cada vector } u \in V \text{ tiene opuesto } -u \in V \\
> &&&u + (-u) = (-u) + u = \vec{0} \\
> \end{align}
> $$
> 
> Y el **producto "externo"** cumple los siguientes axiomas:
> $$
> \begin{align}
> &(P1) &&\alpha \cdot (\beta \cdot u) = (\alpha \beta) \cdot u \\
> &(P2) &&1_{k} \cdot u = u \\
> &(P3) &&\alpha \cdot (u + v) = \alpha \cdot u + \alpha \cdot v \\
> &(P4) &&(\alpha +_{K} \beta) \cdot u = \alpha \cdot u +_{V} \beta \cdot u \\
> & \\
> &&&\text{para todos } \alpha, \beta \in K \text{ y } u, v \in V
> \end{align}
> $$

Le llamamos producto "externo" ya que se da entre elementos de diferentes conjuntos: $K$ y $V$, escalares y vectores.

(P1) - esta regla define cuál es la interacción entre el producto del espacio $V$ con el producto del cuerpo $K$. Tenemos dos productos: producto entre escalares y producto de un escalar por un vector.

Muchas veces llamamos escalares a los coeficientes de una matriz. Ahora, consideraremos escalares a todos los elementos de $K$, números. También se tiene un conjunto de vectores.
Además, se definen la operación suma de vectores y producto de un vector por un escalar, ambas resultando en un vector.

No definimos algo como el producto vectorial, puesto que solo existe en $\mathbb{R}^{3}$.

Definimos la teoría en el marco general (y no en $\mathbb{R}$) con tal de definir teoremas aplicables a cualquier cuerpo. Lo interesante es que los teoremas y propiedades definidas funcionaran para cualquier cuerpo, puesto que los mismos no dependen del cuerpo considerado.

Ahora, abordamos la terminología utilizada:

> [!Terminología]
> Un espacio vectorial cuyo cuerpo de escalares es $K$ se llama un <u>espacio vectorial sobre </u>$K$ (o un K-espacio vectorial).

Pasaremos a ver algunos ejemplos:

### Ejemplos
- El espacio de las n-uplas $\mathbb{R}^{n}$ o ($K^{n}$).
En este caso, $K = \mathbb{R}$ y $V = \mathbb{R}^{n} (\text{o } K^{n})$

Definimos la suma y el producto "externo":
Suma de dos n-uplas:
$$
(\alpha_{1}, \dots, \alpha_{n}) + (\beta_{1}, \dots, \beta_{n}) = (\alpha_{1} + \beta_{1}, \dots, \alpha_{n} + \beta_{n})
$$
Producto de un escalar por una n-upla:
$$
\alpha \cdot (\beta_{1}, \dots, \beta_{n}) = (\alpha \beta_{1}, \dots, \alpha \beta_{n})
$$

Ahora podemos considerar cualquier cuerpo en lugar de $\mathbb{R}$.

En este ejemplo particular, cada vector tiene $n$ componentes, por lo que se corresponde con un espacio de $n$ dimensiones. Ahora no solo podemos cambiar las dimensiones, sino también el cuerpo utilizado, modificando completamente el comportamiento y las capacidades del mismo.

Diremos que este espacio tiene $n$ dimensiones, y durante el curso formalizaremos esta noción, siendo el objetivo entender como se define que un espacio vectorial tiene $x$ dimensiones (cosa que a veces no es tan evidente).

Otro ejemplo:

- El conjunto $V = M_{m \times n}(K)$.
Es un espacio vectorial sobre $K$.

Ya vimos como se define la suma de dos matrices y el producto de un escalar por una matriz.

De esta forma, la definición que consideraremos de vector es todo elemento que existe dentro de algún espacio vectorial. Es así que las matrices serán consideradas vectores.

El grado de libertad (dimensiones) de este espacio está dado por el tamaño de las matrices utilizadas: $m \times n$.

- Dado un intervalo $I \subset \mathbb{R}$:
El conjunto $\mathbb{R}^{I}$ de todas las funciones de $I$ a $\mathbb{R}$.
$$
\mathbb{R}^{I} = \{ f : I \to \mathbb{R} \}
$$
es un espacio vectorial:
$$
\begin{align}
&(f + g)(x) = f(x) + g(x) &&(x \in I) \\
&(\alpha \cdot f)(x) = \alpha \times f(x)
\end{align}
$$
De esta forma, la suma de funciones está bien definida, así como el producto de una función por un escalar, y ambas operaciones dan como resultado una función. Aquí, los vectores son funciones.
De esta forma, el espacio coincide con las reglas definidas anteriormente.

Aquí es más complejo definir los grados de libertad. En este caso, los grados de libertad están dados por cada $x \in I$ (por cada $x \in I$ tengo un grado de libertad). De esta manera, es un espacio de dimensión infinita.

Este es el primer ejemplo de espacio de funciones, aunque podemos restringir el espacio. Por ejemplo, en cálculo I consideramos funciones continuas:

- El conjunto $\mathcal{C}^{0}(I, \mathbb{R}) = \{ f : I \to \mathbb{R} \text{ continuas} \}$
es un espacio vectorial sobre $\mathbb{R}$.

Tiene la suma y el producto "externo" bien definidos (ambos resultando en funciones continuas).

- El conjunto $Der(I, \mathbb{R}) = \{ f : I \to \mathbb{R} \text{ derivables} \}$
es otro espacio vectorial sobre $\mathbb{R}$.

Cumple con todas las propiedades vistas, pues la suma y el producto "externo" dan como resultado otra función derivable.

- El conjunto $Int(I, \mathbb{R}) = \{ f : I \to \mathbb{R} \text{ integrables} \}$
es otro espacio vectorial sobre $\mathbb{R}$.

Cumple con todas las propiedades vistas, pues la suma y el producto "externo" dan como resultado otra función integrable.

De esta forma, todos los espacios en los que trabajamos en GAL I y Cálculo I son espacios vectoriales. De esta forma, la noción de espacio vectorial es la noción fundamental del primer año de la carrera, es adyacente a todo.

- El conjunto $\mathbb{R}[x]$ de los polinomios
es un espacio vectorial.

También tenemos ejemplos de la vida cotidiana:
- El espacio de los píxeles:
$\text{pixel } = (R, G, B) \qquad \text{con } R, G, B \in \mathbb{R}$
(En la realidad, $R, G, B \in [0, 1]$)

Consideramos a una imagen como una colección de píxeles. De esta forma, una pantalla es:
$$
\text{pantalla } : u \in \mathbb{R}^{m \times n \times 3}
$$
De esta forma, en informática también se utilizan espacios vectoriales, especialmente vinculados a matrices.

También se puede definir un espacio vectorial en los sonidos.

Por todas estas razones, los espacios vectoriales y su teoría son fundamentales.

Proseguiremos con el mismo tema en futuras clases.