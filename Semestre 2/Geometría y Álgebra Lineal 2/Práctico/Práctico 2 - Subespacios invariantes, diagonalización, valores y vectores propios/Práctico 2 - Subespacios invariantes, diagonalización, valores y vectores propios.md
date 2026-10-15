# 1 - Subespacios invariantes
## Ejercicio 1
Tenemos que probar que si $s \in S$, entonces $T(s) \in S$ para cada uno de los subespacios propuestos.
### Parte a
- $V$:
$T$ está definida como $T : V \to V$, por lo tanto: si $v \in V$, entonces podemos aplicarle la transformación lineal, y obtener su imagen correspondiente en el codominio (que también resulta ser $V$ ya que se trata de un operador lineal). Entonces, si $v \in V \implies T(v) \in V$. De esta forma, $V$ es un subespacio invariante bajo $T$.

- $\{ 0_{V} \}$:
Como $T$ es una transformación lineal $T : V \to V$, necesariamente se cumple que $T(\vec{0}_{V}) = \vec{0}_{V}$. De esta forma, su imagen se encuentra dentro del mismo espacio vectorial, por lo que $\{ 0_{V} \}$ es un subespacio invariante bajo $T$.

- $N(T) = Ker(T)$:
Recordemos que $N(T) = \{ v \in V : T(v) = 0_{V} \}$. Entonces, sabiendo que $\forall v \in N(T), T(v) = 0_{V}$, y que $T(0_{V}) = 0_{V} \implies 0_{V} \in N(T)$, entonces $N(T) = Ker(T)$ es un subespacio invariante bajo $T$.

- $\mathrm{Im}(T)$:
$\mathrm{Im}(T) = \{ v \in V : T(u) = v \}$. Sabemos que $\mathrm{Im}(T) \subset V$, y como $V$ es tanto dominio y codominio, se cumple que, como $v \in \mathrm{Im}(T)$ si se cumple que $T(u) = v$, con $u \in V$ (para todo el dominio), también se cumple para $\mathrm{Im}(T)$ (selección reducida del dominio): $v \in \mathrm{Im}(T)$ si verifica que $T(u) = v$ con $u \in \mathrm{Im}(T)$. En conclusión $\mathrm{Im}(T)$ es un subespacio invariante bajo $T$.

### Parte b
Sabemos que $W_{1}$ y $W_{2}$ son subespacio de $V$ invariantes bajo $T$, lo que significa que $\forall v \in W_{1}, T(v) \in W_{1}$, y $\forall v \in W_{2}, T(v) \in W_{2}$. Queremos demostrar que:

- $W_{1} \cap W_{2}$ es un subespacio invariante bajo $T$:
Nuestro objetivo es probar que $\forall u \in W_{1} \cap W_{2}, T(v) \in W_{1} \cap W_{2}$.

Sabemos que $\forall v \in W_{1}, T(v) \in W_{1}$, y $\forall v \in W_{2}, T(v) \in W_{2}$. Sea $u \in W_{1} \cap W_{2}$, esto significa que $v \in W_{1} \land v \in W_{2}$. Por lo tanto, sabiendo que:
- $\forall v \in W_{1}, T(v) \in W_{1}$, se cumple que $T(u) \in W_{1}$ (ya que $u \in W_{1}$).
- $\forall v \in W_{2}, T(v) \in W_{2}$, se cumple que $T(u) \in W_{2}$ (ya que $u \in W_{2}$).

Podemos considerar ambas condiciones simultáneamente, concluyendo en que $T(u) \in W_{1} \cap W_{2}, \forall u \in W_{1} \cap W_{2}$. Por lo tanto, $W_{1} \cap W_{2}$ es un subespacio de $V$ invariantes bajo $T$.

- $W_{1} + W_{2}$ es un subespacio invariante bajo $T$:
Recordemos que la suma de dos espacios vectoriales $W_{1}$ y $W_{2}$ da como resultado un nuevo espacio vectorial, el cual contiene todas las combinaciones lineales de los vectores de $W_{1}$ y $W_{2}$.

Consideremos las bases $\mathcal{B}_{1} = \{ v_{1}, \dots, v_{n} \}$ y $\mathcal{B}_{2} = \{ u_{1}, \dots, u_{m} \}$ tal que $[\mathcal{B}_{1}] = W_{1}$ y $[\mathcal{B}_{2}] = W_{2}$
De esta forma:
$$
w \in W_{1} + W_{2} \Longleftrightarrow w = \alpha_{1} v_{1} + \dots + \alpha_{n} v_{n} + \beta_{1} u_{1} + \dots \beta_{m} u_{m}
$$

Entonces:
$$
\begin{align}
T(w) &= T(\alpha_{1} v_{1} + \dots + \alpha_{n} v_{n} + \beta_{1} u_{1} + \dots + \beta_{m} u_{m}) \\
&= T(\alpha_{1} v_{1}) + \dots + T(\alpha_{n} v_{n}) + T(\beta_{1} u_{1}) + \dots + T(\beta_{m} u_{m}) \\
&= \alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n}) + \beta_{1} \cdot T(u_{1}) + \dots + \beta_{m} \cdot T(u_{m})
\end{align}
$$
Ahora, considerando que:
- $\alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n}) \in W_{1}$ (ya que $T(v_{1}), \dots, T(v_{n}) \in W_{1}$).
- $\beta_{1} \cdot T(u_{1}) + \dots + \beta_{m} \cdot T(u_{m}) \in W_{2}$ (ya que $T(u_{1}), \dots, T(u_{m}) \in W_{2}$).

De esta forma, $T(w) = \alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n})+ \beta_{1} \cdot T(u_{1}) + \dots + \beta_{m} \cdot T(u_{m}) \in W_{1} + W_{2}$.

En conclusión, $W_{1} + W_{2}$ es un subespacio invariante bajo $T$, ya que se cumple que $w \in W_{1} + W_{2} \implies T(w) \in W_{1} + W_{2}$.

### Parte c
Sabemos que $W_{1}$ y $W_{2}$ son subespacios de $V$ invariantes bajo $T$, tales que $V = W_{1} \oplus W_{2}$. Esto significa que $W_{1} \cap W_{2} = \{ \vec{0} \}$.

$T|_{W_{1}}$ representa la transformación lineal $T$ restringida a un subespacio invariante $W_{1} \subset V$, mismo significado para $T|_{W_{2}}$.

Entonces, la matriz $M$ asociada a $T|_{W_{1}}$ en la base $\mathcal{B}_{1}$ se determina con las coordenadas en la base $\mathcal{B}_{1}$ de las imágenes de los elementos de dicha base. Ídem para la matriz $N$ asociada a $T|_{W_{2}}$:

Considerando $\mathcal{B}_{1} = \{ u_{1}, \dots, u_{n} \}$ y $\mathcal{B}_{2} = \{ v_{1}, \dots, v_{m} \}$:
$$
\begin{align}
&T(u_{1}) = a_{1,1} \cdot u_{1} + a_{2, 1} \cdot u_{2} + \dots + a_{n, 1} \cdot u_{n} &&\implies coord(T(u_{1})) = (a_{1,1}, a_{2,1}, \dots, a_{n,1}) \\
&T(u_{2}) = a_{1,2} \cdot u_{1} + a_{2, 2} \cdot u_{2} + \dots + a_{n, 2} \cdot u_{n} &&\implies coord(T(u_{2})) = (a_{1,2}, a_{2,2}, \dots, a_{n,2}) \\
&\dots \\
&T(u_{n}) = a_{1,n} \cdot u_{1} + a_{2, n} \cdot u_{2} + \dots + a_{n, n} \cdot u_{n} &&\implies coord(T(u_{n})) = (a_{1,n}, a_{2,n}, \dots, a_{n,n})
\end{align}
$$
$$
_{\mathcal{B}_{1}}(T|_{W_{1}})_{\mathcal{B}_{1}} = M = \underbrace{ \begin{pmatrix}
coord_{\mathcal{B}_{1}}(u_{1}) & coord_{\mathcal{B}_{1}}(u_{2}) & \dots & coord_{\mathcal{B}_{1}}(u_{n})
\end{pmatrix} }_{ n } = \underbrace{ \left. \begin{pmatrix}
a_{1,1} & a_{1,2} & \dots & a_{1,n} \\
a_{2,1} & a_{2,2} & \dots & a_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n,1} & a_{n,2} & \dots & a_{n,n}
\end{pmatrix} \right\} }_{ n } n
$$
$$
\begin{align}
&T(v_{1}) = b_{1,1} \cdot v_{1} + b_{2, 1} \cdot v_{2} + \dots + b_{m, 1} \cdot v_{m} &&\implies coord(T(v_{1})) = (b_{1,1}, b_{2,1}, \dots, b_{m,1}) \\
&T(v_{2}) = b_{1,2} \cdot v_{1} + b_{2, 2} \cdot v_{2} + \dots + b_{m, 2} \cdot v_{m} &&\implies coord(T(v_{2})) = (b_{1,2}, b_{2,2}, \dots, b_{m,2}) \\
&\dots \\
&T(v_{m}) = b_{1,m} \cdot v_{1} + b_{2, m} \cdot v_{2} + \dots + b_{m, m} \cdot v_{n} &&\implies coord(T(v_{m})) = (b_{1,m}, b_{2,m}, \dots, b_{m,m})
\end{align}
$$
$$
_{\mathcal{B}_{2}}(T|_{W_{2}})_{\mathcal{B}_{2}} = N = \begin{pmatrix}
coord_{\mathcal{B}_{2}}(v_{1}) & coord_{\mathcal{B}_{2}}(v_{2}) & \dots & coord_{\mathcal{B}_{2}}(v_{m})
\end{pmatrix} = \underbrace{ \left. \begin{pmatrix}
b_{1,1} & b_{1,2} & \dots & b_{1,m} \\
b_{2,1} & b_{2,2} & \dots & b_{2,m} \\
\vdots & \vdots & \ddots & \vdots \\
b_{m,1} & b_{m,2} & \dots & b_{m,m}
\end{pmatrix} \right\} }_{ m } m
$$

Entonces, pasamos a estudiar la matriz asociada a $T$ en la base $\mathcal{B}_{1} \cup \mathcal{B}_{2}$:
$\mathcal{B}_{1} \cup \mathcal{B}_{2} = \{ u_{1}, \dots, u_{n} \} \cup \{ v_{1}, \dots, v_{m} \} = \{ u_{1}, \dots, u_{n}, v_{1}, \dots, v_{m} \}$

De esta forma, tenemos que volver a definir las coordenadas de cada vector en la nueva base para poder determinar la matriz asociada $_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(T)_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}$:
$$
\begin{align}
&T(u_{1}) = a_{1,1} \cdot u_{1} + a_{2, 1} \cdot u_{2} + \dots + a_{n, 1} \cdot u_{n} + 0 \cdot v_{1} + 0\cdot v_{2} + \dots + 0 \cdot v_{m} &&\implies coord(T(u_{1})) = (a_{1,1}, a_{2,1}, \dots, a_{n,1}, 0, 0, \dots, 0) \\
&T(u_{2}) = a_{1,2} \cdot u_{1} + a_{2, 2} \cdot u_{2} + \dots + a_{n, 2} \cdot u_{n} + 0 \cdot v_{1} + 0\cdot v_{2} + \dots + 0 \cdot v_{m} &&\implies coord(T(u_{2})) = (a_{1,2}, a_{2,2}, \dots, a_{n,2}, 0, 0, \dots, 0) \\
&\dots \\
&T(u_{n}) = a_{1,n} \cdot u_{1} + a_{2, n} \cdot u_{2} + \dots + a_{n, n} \cdot u_{n} + 0 \cdot v_{1} + 0\cdot v_{2} + \dots + 0 \cdot v_{m} &&\implies coord(T(u_{n})) = (a_{1,n}, a_{2,n}, \dots, a_{n,n}, 0, 0, \dots, 0)
\end{align}
$$
$$
\begin{align}
&T(v_{1}) = 0 \cdot u_{1} + 0\cdot u_{2} + \dots + 0 \cdot u_{n} + b_{1,1} \cdot v_{1} + b_{2, 1} \cdot v_{2} + \dots + b_{m, 1} \cdot v_{m} &&\implies coord(T(v_{1})) = (0, 0, \dots, 0, b_{1,1}, b_{2,1}, \dots, b_{m,1}) \\
&T(v_{2}) = 0 \cdot u_{1} + 0\cdot u_{2} + \dots + 0 \cdot u_{n} + b_{1,2} \cdot v_{1} + b_{2, 2} \cdot v_{2} + \dots + b_{m, 2} \cdot v_{m} &&\implies coord(T(v_{2})) = (0, 0, \dots, 0, b_{1,2}, b_{2,2}, \dots, b_{m,2}) \\
&\dots \\
&T(v_{m}) = 0 \cdot u_{1} + 0\cdot u_{2} + \dots + 0 \cdot u_{n} + b_{1,m} \cdot v_{1} + b_{2, m} \cdot v_{2} + \dots + b_{m, m} \cdot v_{n} &&\implies coord(T(v_{m})) = (0, 0, \dots, 0, b_{1,m}, b_{2,m}, \dots, b_{m,m})
\end{align}
$$
$$
\begin{align}
_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(T)_{\mathcal{B}_{1} \cup \mathcal{B}_{2}} &= \begin{pmatrix}
coord_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(u_{1}) & coord_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(u_{2}) & \dots & coord_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(u_{n}) & coord_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(v_{1}) & coord_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(v_{2}) & \dots & coord_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(v_{m})
\end{pmatrix} \\
&= \underbrace{ \left. \begin{pmatrix}
a_{1,1} & a_{1,2} & \dots & a_{1,n} & 0 & 0 & \dots & 0 \\
a_{2,1} & a_{2,2} & \dots & a_{2,n} & 0 & 0 & \dots & 0 \\
\vdots & \vdots & \ddots & \vdots & \vdots & \vdots & \vdots & \vdots \\
a_{n,1} & a_{n,2} & \dots & a_{n,n} & 0 & 0 & \dots & 0 \\
0 & 0 & \dots & 0 & b_{1,1} & b_{1,2} & \dots & b_{1,m} \\
0 & 0 & \dots & 0 & b_{2,1} & b_{2,2} & \dots & b_{2,m} \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & \dots & 0 & b_{m,1} & b_{m,2} & \dots & b_{m,m}
\end{pmatrix} \right\} }_{ n + m } n + m
\end{align}
$$

De esta manera, la matriz $_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}(T)_{\mathcal{B}_{1} \cup \mathcal{B}_{2}}$ es una matriz por bloques de la forma $\begin{pmatrix} M & 0 \\ 0 & N \end{pmatrix}$.

---
## Ejercicio 2
### Parte a
Tenemos que comprobar que para todo elemento $v \in [A], T(v) \in [A]$.

Como $[A]$ es más pequeño que $\mathbb{R}^{3}$, ya que es de dimensión 2, no es tan sencillo como decir como probar que en una transformación $T : V \to V$, $V$ es un subespacio invariante bajo $T$.

IMPORTANTE: PARA PROBAR QUE UN SUBESPACIO ES INVARIANTE POR UNA TRANSFORMACIÓN, NECESAIRAMENTE TENEMOS QUE VERIFICAR QUE LAS IMÁGENES DE LOS ELEMENTOS CAEN EN EL MISMO ESPACIO. EN ESTE CASO, SERÍA DETERMINAR LAS IMÁGENES DE LOS ELEMENTOS DE $[A]$ Y PROBAR QUE SE PUEDEN EXPRESAR COMO COMBINACIÓN LINEAL DE LOS ELEMENTOS DE $A$.

Tenemos que probarlo, para lo que estudiaremos las imágenes de los elementos de $A$:
$$
\begin{align}
&T(1, 0, 1) = (3, -1, 2) \\
&T(1, 1, 2) = (3, 1, 4)
\end{align}
$$
Ahora, tenemos que verificar las imágenes correspondientes se pueden expresar como combinación lineal de los elementos de $A$:
$$
(3, -1, 2) = \alpha \cdot (1, 0, 1) + \beta \cdot (1, 1, 2)
$$
$$
\begin{cases}
\alpha + \beta = 3 \\
\beta = -1 \\
\alpha + 2\beta = 2
\end{cases} \implies \alpha = 4
$$
$$
(3, -1, 2) = 4 \cdot (1, 0, 1) - 1 \cdot (1, 1, 2) \implies coord_{A}(3, -1, 2) = (4, -1)
$$

$$
(3, 1, 4) = \alpha \cdot (1, 0, 1) + \beta \cdot (1, 1, 2)
$$
$$
\begin{cases}
\alpha + \beta = 3 \\
\beta = 1 \\
\alpha + 2\beta = 4
\end{cases} \implies \alpha = 2
$$
$$
(3, 1, 4) = 2 \cdot (1, 0, 1) + 1 \cdot (1, 1, 2) \implies coord_{A}(3, 1, 4) = (2, 1)
$$

De esta forma, probamos que las imágenes de los elementos de $A$ se pueden expresar por combinación lineal de los elementos de $A$, por lo que $[A]$ es invariante bajo $T$.

### Parte b
Anteriormente determinamos las imágenes de los elementos de $A$:
$$
\begin{align}
&T(1, 0, 1) = (3, -1, 2) \\
&T(1, 1, 2) = (3, 1, 4)
\end{align}
$$
Como se solicita la matriz asociada que recibe elementos expresados en sus coordenadas de la base $A$ y las devuelve en las coordenadas de la canónica $\mathcal{C}$, no es necesario hacer nada más. Ya tenemos la información suficiente para determinar la matriz $_{\mathcal{C}}(T|_{S})_{A}$:
$$
_{\mathcal{C}}(T|_{S})_{A} = \begin{pmatrix}
coord_{\mathcal{C}}(3, -1, 2) & coord_{\mathcal{C}}(3, 1, 4)
\end{pmatrix} = \begin{pmatrix}
3 & 3 \\
-1 & 1 \\
2 & 4
\end{pmatrix}
$$

### Parte c
Para completar $A$ a una base $\mathcal{B}$ de $\mathbb{R}^{3}$, tenemos que agregar un elemento más, manteniendo la propiedad LI del conjunto. En este caso, agregaremos el elemento $(1, 0, 0)$:
$$
\mathcal{B} = A \cup \{ (1, 0, 0) \} = \{ (1, 0, 1), (1, 1, 2), (1, 0, 0) \}
$$
Ahora, determinemos la matriz $_{\mathcal{B}}(T)_{\mathcal{B}}$:
1. Determinar la imagen del elemento faltante:
$$
T(1, 0, 0) = (2, 0, 1)
$$

2. Determinar las coordenadas en la base $\mathcal{B}$ de las imágenes halladas:
No es necesario volver a determinar las coordenadas de los primeros dos vectores, ya que ya las calculamos en la parte a:
$$
(3, -1, 2) = 4 \cdot (1, 0, 1) - 1 \cdot (1, 1, 2) + 0 \cdot (1, 0, 0) \implies coord_{\mathcal{B}}(3, -1, 2) = \left( 4, -1, 0 \right)
$$
$$
(3, 1, 4) = 2 \cdot (1, 0, 1) + 1 \cdot (1, 1, 2) + 0 \cdot (1, 0, 0) \implies coord_{\mathcal{B}}(3, 1, 4) = \left( 2, 1, 0 \right)
$$

Tenemos que determinar las coordenadas de la nueva imagen:
$$
(2, 0, 1) = \alpha \cdot (1, 0, 1) + \beta \cdot (1, 1, 2) + \gamma \cdot (1, 0, 0)
$$
$$
\begin{cases}
\alpha + \beta + \gamma = 2 \\
\beta = 0 \\
\alpha + 2\beta = 1
\end{cases} \implies \alpha = 1 \implies \gamma = 1
$$
$$
(2, 0, 1) = 1 \cdot (1, 0, 1) + 0 \cdot (1, 1, 2) + 1 \cdot (1, 0, 0) \implies coord_{\mathcal{B}}(2, 0, 1) = \left( 1, 0, 1 \right)
$$

3. Expresar la matriz:
$$
_{\mathcal{B}}(T)_{\mathcal{B}} = \begin{pmatrix}
4 & 2 & 1 \\
-1 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$
CORRECCIÓN: NO ES NECESARIO VOLVER A DETERMINAR LAS COORDENADAS DE LOS PRIMEROS DOS VECTORES, YA QUE YA LAS CALCULAMOS ANTES. AL AGREGAR UN NUEVO VECTOR A LA BASE, PERO MANTENIENDO EL ORDEN, SIMPLEMENTE TENEMOS QUE AGREGAR 0 AL FINAL.

---
# 2 - Valores y vectores propios
## Ejercicio 3
Para todas las transformaciones, consideraremos que estamos trabajando en la base canónica.
En todos los casos, el procedimiento será:
1. Determinar las imágenes de los elementos de la base canónica.
2. Expresar la matriz asociada correspondiente.
3. Expresar el polinomio característico.
4. Hallar sus raíces.
5. Considerando las raíces, determinar las bases de los subespacios propios.
### Parte 1
#### Transformación 1
$$
T : \mathbb{R}^{2} \to \mathbb{R}^{2}, T(x, y) = (-2x - 7y, x + 2y)
$$
$$
\begin{align}
&T(1, 0) = (-2, 1) \\
&T(0, 1) = (-7, 2)
\end{align}
$$
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
-2 & -7 \\
1 & 2
\end{pmatrix}
$$
$$
\det(_{\mathcal{C}}(T)_{\mathcal{C}} - \lambda Id) = \det \begin{pmatrix}
-2 - \lambda & -7 \\
1 & 2 - \lambda
\end{pmatrix} = (-2 - \lambda)(2 - \lambda) + 7 = \lambda^{2} + 3
$$
$$
\lambda^{2} + 3 = 0 \implies \lambda^{2} = -3 \implies \lambda = \sqrt{ -3 }
$$

Como estamos trabajando en $\mathbb{R}$ y la raíz obtenida es compleja, no podemos proseguir.

#### Transformación 2
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}, T(x, y, z) = (x, z, y)
$$
$$
\begin{align}
&T(1, 0, 0) = (1, 0, 0) \\
&T(0, 1, 0) = (0, 0, 1) \\
&T(0, 0, 1) = (0, 1, 0)
\end{align}
$$
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 0 & 1 \\
0 & 1 & 0
\end{pmatrix}
$$
$$
\det(_{\mathcal{C}}(T)_{\mathcal{C}} - \lambda Id) = \det \begin{pmatrix}
1 - \lambda & 0 & 0 \\
0 & -\lambda & 1 \\
0 & 1 & -\lambda
\end{pmatrix} = (1 - \lambda)(\lambda^{2} - 1)
$$
$$
(1 - \lambda)(\lambda^{2} - 1) = 0 \implies 1 - \lambda = 0 \text{ o } \lambda^{2} - 1 = 0
$$
$$
1 - \lambda = 0 \implies \lambda = 1
$$
$$
\lambda^{2} - 1 = 0 \implies \lambda^{2} = 1 \implies \lambda = \pm1
$$
De esta manera, determinamos que los valores propios de la transformación son $\lambda = 1$ y $\lambda = -1$ ($\lambda = 1$ es doble).

Ahora, desarrollamos la matriz correspondiente a $\lambda = 1$:
$$
\begin{pmatrix}
0 & 0 & 0 \\
0 & -1 & 1 \\
0 & 1 & -1
\end{pmatrix} \implies \begin{cases}
-y + z = 0 \\
y - z = 0
\end{cases} \implies y = z \qquad (\text{y } x \text{ es libre})
$$
De esta forma, podemos determinar la base del subespacio $S_{1}$:
$$
S_{1} = \{ (\alpha, \beta, \beta) : \alpha, \beta \in \mathbb{R} \} \implies S_{1} = [\{ (1, 0, 0), (0, 1, 1) \}]
$$

Desarrollamos la matriz correspondiente a $\lambda = -1$:
$$
\begin{pmatrix}
2 & 0 & 0 \\
0 & 1 & 1 \\
0 & 1 & 1
\end{pmatrix} = \begin{pmatrix}
2 & 0 & 0 \\
0 & 1 & 1 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
2x = 0 \\
y + z = 0
\end{cases} \implies x = 0 \land z = -y
$$
Entonces:
$$
S_{-1} = \{ (0, \alpha, -\alpha) : \alpha \in \mathbb{R} \} \implies S_{-1} = [\{ (0, 1, -1) \}]
$$

#### Transformación 3
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}, T(x, y, z) = (x, z, -y)
$$
$$
\begin{align}
&T(1, 0, 0) = (1, 0, 0) \\
&T(0, 1, 0) = (0, 0, -1) \\
&T(0, 0, 1) = (0, 1, 0)
\end{align}
$$
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 0 & -1 \\
0 & 1 & 0
\end{pmatrix}
$$
$$
\det(_{\mathcal{C}}(T)_{\mathcal{C}} - \lambda Id) = \det \begin{pmatrix}
1 - \lambda & 0 & 0 \\
0 & -\lambda & -1 \\
0 & 1 & -\lambda
\end{pmatrix} = (1 - \lambda)(\lambda^{2} + 1)
$$
$$
(1 - \lambda)(\lambda^{2} + 1) = 0 \implies 1 - \lambda = 0 \text{ o } \lambda^{2} + 1 = 0
$$
$$
1 - \lambda = 0 \implies \lambda = 1
$$
$$
\lambda^{2} - 1 = 0 \implies \lambda^{2} = 1 \implies \lambda = \sqrt{ -1 }
$$
De esta manera, determinamos que el único valor propio (considerando que $\mathbb{K} = \mathbb{R}$) es $\lambda = 1$.

Ahora, desarrollamos la matriz correspondiente a $\lambda = 1$:
$$
\begin{pmatrix}
0 & 0 & 0 \\
0 & -1 & -1 \\
0 & 1 & -1
\end{pmatrix} \implies \begin{cases}
-y - z = 0 \\
y - z = 0
\end{cases} \implies y = z \implies -2z = 0 \implies z = 0 \implies y = 0 \qquad (\text{y } x \text{ es libre})
$$
De esta forma, podemos determinar la base del subespacio $S_{1}$:
$$
S_{1} = \{ (\alpha, 0, 0) : \alpha \in \mathbb{R} \} \implies S_{1} = [\{ (1, 0, 0) \}]
$$

### Parte 2
Ahora, consideramos $\mathbb{K} = \mathbb{C}$. Simplemente, seguiremos los razonamientos que no pudimos seguir, debido a que $\lambda$ era una raíz compleja.

#### Transformación 1
$$
\lambda^{2} + 3 = 0 \implies \lambda^{2} = -3 \implies \lambda = \pm \sqrt{ -3 } = \pm \sqrt{ 3 }\sqrt{ -1 } = \pm \sqrt{ 3 }i
$$
Desarrollamos la matriz correspondiente a $\lambda = \sqrt{ 3 }i$:
$$
\begin{pmatrix}
-2 - \sqrt{ 3 }i & -7 \\
1 & 2 - \sqrt{ 3 }i
\end{pmatrix} = \begin{pmatrix}
0 & 0 \\
1 & 2 - \sqrt{ 3 }i
\end{pmatrix} \implies \begin{cases}
x + (2 - \sqrt{ 3 }i)y = 0
\end{cases} \implies x = -(2 - \sqrt{ 3 }i)y
$$
De esta forma, podemos determinar la base del subespacio $S_{\sqrt{ 3 }i}$:
$$
S_{\sqrt{ 3 }i} = \left\{ \left( (-2 + \sqrt{ 3 }i)\alpha, \alpha \right) \right\} \implies S_{\sqrt{ 3 }i} = \left[ \left\{ \left( -2 + \sqrt{ 3 }i, 1 \right) \right\} \right]
$$

Desarrollamos la matriz correspondiente a $\lambda = -\sqrt{ 3 }i$:
$$
\begin{pmatrix}
-2 + \sqrt{ 3 }i & -7 \\
1 & 2 + \sqrt{ 3 }i
\end{pmatrix} = \begin{pmatrix}
0 & 0 \\
1 & 2 + \sqrt{ 3 }i
\end{pmatrix} \implies \begin{cases}
x + (2 + \sqrt{ 3 }i)y = 0
\end{cases} \implies x = -(2 + \sqrt{ 3 }i)y
$$
De esta forma, podemos determinar la base del subespacio $S_{-\sqrt{ 3 }i}$:
$$
S_{-\sqrt{ 3 }i} = \left\{ \left( -(2 + \sqrt{ 3 }i)\alpha, \alpha \right) \right\} \implies S_{-\sqrt{ 3 }i} = \left[ \left\{ \left( -2 - \sqrt{ 3 }i, 1 \right) \right\} \right]
$$

#### Transformación 2
Esta se comporta igual en $\mathbb{K} = \mathbb{C}$: tenemos dos valores propios, $\lambda = 1$ (doble), y $\lambda = -1$.
$$
S_{1} = \{ (\alpha, \beta, \beta) : \alpha, \beta \in \mathbb{R} \} \implies S_{1} = [\{ (1, 0, 0), (0, 1, 1) \}]
$$
$$
S_{-1} = \{ (0, \alpha, -\alpha) : \alpha \in \mathbb{R} \} \implies S_{-1} = [\{ (0, 1, -1) \}]
$$

#### Transformación 3
Determinamos la base dada por el valor propio $\lambda = 1$:
$$
S_{1} = \{ (\alpha, 0, 0) : \alpha \in \mathbb{R} \} \implies S_{1} = [\{ (1, 0, 0) \}]
$$

Nos queda determinar la base para el valor $\lambda = \sqrt{ -1 }$:
$$
\lambda^{2} - 1 = 0 \implies \lambda^{2} = 1 \implies \lambda = \sqrt{ -1 } = \pm i
$$
Desarrollamos la matriz correspondiente a $\lambda = i$:
$$
\begin{pmatrix}
1 - i & 0 & 0 \\
0 & -i & -1 \\
0 & 1 & -i
\end{pmatrix} = \begin{pmatrix}
1 - i & 0 & 0 \\
0 & i & 1 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
(1 - i)x = 0 \\
iy + z = 0
\end{cases} \implies x = 0 \implies z = -iy 
$$
De esta forma, podemos determinar la base del subespacio $S_{i}$:
$$
S_{i} = \{ (0, \alpha, -\alpha i) : \alpha \in \mathbb{R} \} \implies S_{i} = [\{ (0, 1, -i) \}]
$$

Desarrollamos la matriz correspondiente a $\lambda = -i$:
$$
\begin{pmatrix}
1 + i & 0 & 0 \\
0 & i & -1 \\
0 & 1 & i
\end{pmatrix} = \begin{pmatrix}
1 + i & 0 & 0 \\
0 & i & -1 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
(1 + i)x = 0 \\
iy - z = 0
\end{cases} \implies x = 0 \implies z = iy 
$$
De esta forma, podemos determinar la base del subespacio $S_{-i}$:
$$
S_{-i} = \{ (0, \alpha, \alpha i) : \alpha \in \mathbb{R} \} \implies S_{i} = [\{ (0, 1, i) \}]
$$

---
## Ejercicio 4
$$
T \left( \begin{pmatrix}
a & b \\
c & d
\end{pmatrix} \right) = \begin{pmatrix}
4a + b + d & 2a + 3b + d \\
-2a + b + 2c - 3d & 2a - b + 5d
\end{pmatrix}
$$
Para determinar los valores propios de $T$, primero tenemos que determinar la matriz asociada a la transformación. Como no se especifica una base en particular, utilizaremos la canónica:
$$
\begin{align}
&T \left( \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right) = \begin{pmatrix}
4 & 2 \\
-2 & 2
\end{pmatrix} \\
&T \left( \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right) = \begin{pmatrix}
1 & 3 \\
1 & -1
\end{pmatrix} \\
&T \left( \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right) = \begin{pmatrix}
0 & 0 \\
2 & 0
\end{pmatrix} \\
&T \left( \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right) = \begin{pmatrix}
1 & 1 \\
-3 & 5
\end{pmatrix}
\end{align}
$$
Ahora, determinamos sus coordenadas en la base canónica:
$$
\begin{align}
&coord_{\mathcal{C}}\left( \begin{pmatrix}
4 & 2 \\
-2 & 2
\end{pmatrix} \right) = (4, 2, -2, 2) \\
&coord_{\mathcal{C}}\left( \begin{pmatrix}
1 & 3 \\
1 & -1
\end{pmatrix} \right) = (1, 3, 1, -1) \\
&coord_{\mathcal{C}}\left( \begin{pmatrix}
0 & 0 \\
2 & 0
\end{pmatrix} \right) = (0, 0, 2, 0) \\
&coord_{\mathcal{C}}\left( \begin{pmatrix}
1 & 1 \\
-3 & 5
\end{pmatrix} \right) = (1, 1, -3, 5)
\end{align}
$$
Expresamos la matriz asociada $_{\mathcal{C}}(T)_{\mathcal{C}}$:
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
4 & 1 & 0 & 1 \\
2 & 3 & 0 & 1 \\
-2 & 1 & 2 & -3 \\
2 & -1 & 0 & 5
\end{pmatrix}
$$

Ahora, calculamos el determinante de $_{\mathcal{C}}(T)_{\mathcal{C}} - \lambda Id$:
$$
\begin{align}
\det(_{\mathcal{C}}(T)_{\mathcal{C}} - \lambda Id) &= \det \begin{pmatrix}
4 - \lambda & 1 & 0 & 1 \\
2 & 3 - \lambda & 0 & 1 \\
-2 & 1 & 2 - \lambda & -3 \\
2 & -1 & 0 & 5 - \lambda
\end{pmatrix} = (2 - \lambda) \cdot \det \begin{pmatrix}
4 - \lambda & 1 & 1 \\
2 & 3 - \lambda & 1 \\
2 & -1 & 5 - \lambda
\end{pmatrix} \\
&= (2 - \lambda) \cdot ((4 - \lambda)((3 - \lambda)(5 - \lambda) + 1) - (10 - 2\lambda - 2) + (-2 - 6 + 2\lambda)) \\
&= (2 - \lambda) \cdot ((4 - \lambda)((3 - \lambda)(5 - \lambda) + 1) - 8 + 2\lambda + 2\lambda - 8) \\
&= (2 - \lambda) \cdot ((4 - \lambda)((3 - \lambda)(5 - \lambda) + 1) + 4\lambda - 16) \\
&= (2 - \lambda) \cdot (-(\lambda - 4)(\lambda^{2} - 8\lambda + 16) + 4(\lambda - 4)) \\
&= (2 - \lambda) \cdot (\lambda - 4) \cdot (-\lambda^{2} + 8\lambda - 16 + 4) \\
&= (2 - \lambda) \cdot (\lambda - 4) \cdot (-\lambda^{2} + 8\lambda - 12) \\
&= (\lambda - 2) \cdot (\lambda - 4) \cdot (\lambda^{2} - 8\lambda + 12) \qquad \text{(Cambio de signo al invertir la resta del primer factor)} \\
&= (\lambda - 2) \cdot (\lambda - 4) \cdot (\lambda - 2) \cdot (\lambda - 6) \\
&= (\lambda - 2)^{2} \cdot (\lambda - 4) \cdot (\lambda - 6)
\end{align}
$$

De esta forma, tenemos los siguientes valores propios:
$$
\lambda - 2 = 0 \implies \lambda = 2 \qquad \text{(Raíz doble)}
$$
$$
\lambda - 4 = 0 \implies \lambda = 4
$$
$$
\lambda - 6 = 0 \implies \lambda = 6
$$
Ahora, estudiaremos el sistema determinado considerando cada uno de los valores propios:
- $\lambda = 2$:
$$
\begin{pmatrix}
2 & 1 & 0 & 1 \\
2 & 1 & 0 & 1 \\
-2 & 1 & 0 & -3 \\
2 & -1 & 0 & 3
\end{pmatrix} = \begin{pmatrix}
1 & 1 & 0 & 0 \\
0 & 0 & 0 & 0 \\
1 & 0 & 0 & 1 \\
0 & 0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
x_{1} + x_{2} = 0 \\
x_{1} + x_{4} = 0
\end{cases} \implies x_{2} = x_{4} = -x_{1} \qquad (x_{3} \text{ es libre})
$$
$$
\implies S_{2} = \{ (\alpha, -\alpha, \beta, -\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, -1, 0, -1), (0, 0, 1, 0) \}]
$$
$$
S_{2} = \left[ \left\{ \begin{pmatrix}
1 & -1 \\
0 & -1
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right\} \right]
$$

- $\lambda = 4$:
$$
\begin{pmatrix}
0 & 1 & 0 & 1 \\
2 & -1 & 0 & 1 \\
-2 & 1 & -2 & -3 \\
2 & -1 & 0 & 1
\end{pmatrix} = \begin{pmatrix}
0 & 1 & 0 & 1 \\
1 & 0 & 0 & 1 \\
0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
x_{2} + x_{4} = 0 \\
x_{1} + x_{4} = 0 \\
x_{3} + x_{4} = 0
\end{cases} \implies x_{1} = x_{2} = x_{3} = -x_{4}
$$
$$
\implies S_{4} = \{ (\alpha, \alpha, \alpha, -\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 1, 1, -1) \}]
$$
$$
S_{4} = \left[ \left\{ \begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix} \right\} \right]
$$

- $\lambda = 6$:
$$
\begin{pmatrix}
-2 & 1 & 0 & 1 \\
2 & -3 & 0 & 1 \\
-2 & 1 & -4 & -3 \\
2 & -1 & 0 & -1
\end{pmatrix} = \begin{pmatrix}
-1 & 0 & 0 & 1 \\
0 & -1 & 0 & 1 \\
0 & 0 & -1 & -1 \\
0 & 0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
-x_{1} + x_{4} = 0 \\
-x_{2} + x_{4} = 0 \\
-x_{3} - x_{4} = 0
\end{cases} \implies x_{1} = x_{4} \implies x_{2} = x_{4} \implies x_{3} = -x_{4}
$$
$$
\implies S_{6} = \{ (\alpha, \alpha, -\alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 1, -1, 1) \}]
$$
$$
S_{6} = \left[ \left\{ \begin{pmatrix}
1 & 1 \\
-1 & 1
\end{pmatrix} \right\} \right]
$$

---
## Ejercicio 5
### Parte 1
Que 0 no sea valor propio de $T$ significa que $\lambda = 0$ no es raíz del polinomio $X_{A}(\lambda)$. Recordemos la siguiente proposición:
> [!Proposición]
> Sea $A$ una matriz $n \times n$. El $\det(A - \lambda I)$, que se indicará por $X_{A}(\lambda)$, es un polinomio de grado $n$ en $\lambda$ cuyo término independiente coincide con el determinante de $A$.

$$
\begin{align}
T \text{ es invertible } &\Longleftrightarrow \det(A) \neq 0 \\
&\Longleftrightarrow \det(T - 0 \cdot I) \neq 0 \\
&\Longleftrightarrow X_{T}(0) \neq 0 \\
&\Longleftrightarrow \lambda = 0 \text{ no es raíz de } X_{T}(\lambda) \\
&\Longleftrightarrow 0 \text{ no es valor própio de } T
\end{align}
$$

### Parte 2
$$
\begin{align}
T \text{ es invertible y } \lambda \text{ es valor propio de } T &\implies \det(T - \lambda \cdot I) = 0 \qquad (\text{con } \lambda \neq 0) \\
&\implies \det(T^{-2}) \cdot \det(T - \lambda \cdot I) \cdot \det(\lambda^{-2} \cdot I) = 0 \\
&\implies \det(T^{-2}T \cdot \lambda^{-2} \cdot I - T^{-2} \cdot \lambda \cdot I \cdot \lambda^{-2} \cdot I) = 0 \\
&\implies \det(T^{-1} \cdot \lambda^{-2} \cdot I - T^{-2} \cdot \lambda^{-1} \cdot I) = 0 \\
&\implies \det((T^{-1} \cdot \lambda^{-1} \cdot I) \cdot (\lambda^{-1} \cdot I - T^{-1})) = 0 \\
&\implies \det(T^{-1} \cdot \lambda^{-1} \cdot I) \cdot \det(\lambda^{-1} \cdot I - T^{-1}) = 0 \\
&\implies \text{Como } \det(T^{-1} \cdot \lambda^{-1} \cdot I) \neq 0 \text{, necesariamente } \det(\lambda^{-1} \cdot I - T^{-1}) = 0 \\
&\implies \lambda^{-1} \text{ es valor propio de } T^{-1}
\end{align}
$$

### Parte 3
$$
\begin{align}
\text{Si } \lambda \text{ es valor propio de T } &\implies \exists v \in V \text{ tal que } T(v) = \lambda \cdot v \implies T \cdot v = \lambda \cdot v \\
&\text{Caso base } (n = 1) \text{: } T^{1} \cdot v = \lambda^{1} \cdot v \\
&\text{Paso inductivo: Supongamos que se cumple para } n = k \implies T^{k} \cdot v = \lambda^{k} \cdot v \\
&\implies T(T^{k} \cdot v) = T(\lambda^{k} \cdot v) \\
&\implies T^{k + 1} \cdot v = \lambda^{k} \cdot T(v) \\
&\text{Como sabemos que } T(v) = \lambda \cdot v \implies T^{k + 1} \cdot v = \lambda^{k} \cdot \lambda \cdot v = \lambda^{k + 1} \cdot v \\
&\text{Por el principio de inducción, } T^{n} \cdot v = \lambda^{n} \cdot v, \forall n \in \mathbb{N}
&\implies \lambda^{n} \text{ es valor propio de } T^{n} \qquad \forall n \in \mathbb{N}
\end{align}
$$

### Parte 4
$$
\begin{align}
\text{Si } T \text{ es invertible y } \lambda \text{ es valor propio de } T &\implies \lambda^{-1} \text{ es valor propio de } T^{-1} \\
&\implies \exists v \in V \text{ tal que } T^{-1} \cdot v = \lambda^{-1} \cdot v \\
&\text{Caso base } (n = -1) \text{: } T^{-1} \cdot v = \lambda^{-1} \cdot v \\
&\text{Paso inductivo: Supongamos que se cumple para } n = -k \implies T^{-k} \cdot v = \lambda^{-k} \cdot v \\
&\implies T^{-1}(T^{-k} \cdot v) = T^{-1}(\lambda^{-k} \cdot v) \\
&\implies T^{-k - 1} \cdot v = \lambda^{-k} \cdot T^{-1}(v) \\
&\text{Como sabemos que } T^{-1}(v) = \lambda^{-1} \cdot v \implies T^{-k - 1} \cdot v = \lambda^{-k} \cdot \lambda^{-1} \cdot v = \lambda^{-k - 1} \cdot v \\
&\text{Por el principio de inducción, } T^{-n} \cdot v = \lambda^{-n} \cdot v, \forall n \in \mathbb{N} \\
&\implies \lambda^{-n} \text{ es valor propio de } T^{-n}, \forall n \in \mathbb{N}
\end{align}
$$

---
## Ejercicio 6
### Parte 1
Básicamente, el polinomio característico de una matriz $A$ se puede determinar al desarrollar la siguiente operación:
$$
\det(A - \lambda \cdot I)
$$
Consideremos que el determinante de una matriz siempre es el mismo, sin importar que fila o columna se considere para desarrollar la operación, así como que las matrices transpuestas intercambian filas y columnas (fila $i$ pasa a ser columna $i$ y viceversa, manteniendo únicamente la diagonal).
$$
\det(A - \lambda \cdot I) = \left| \begin{array}{cccc}
a_{1,1} - \lambda & a_{1,2} & \dots & a_{1,n} \\
a_{2,1} & a_{2,2} - \lambda & \dots & a_{2,n} \\
\vdots & \vdots  & \ddots & \vdots \\
a_{n,1} & a_{n,2} & \dots & a_{n,n} - \lambda
\end{array} \right|, \det(A^{t} - \lambda \cdot I) = \left| \begin{array}{cccc}
a_{1,1} - \lambda & a_{2,1} & \dots & a_{n,1} \\
a_{1,2} & a_{2,2} - \lambda & \dots & a_{n,2} \\
\vdots & \vdots  & \ddots & \vdots \\
a_{1,n} & a_{2,n} & \dots & a_{n,n} - \lambda
\end{array} \right|
$$

De esta forma, podemos desarrollar el determinante de $A - \lambda \cdot I$ en base a la primer columna, y el determinante de $A^{t} - \lambda \cdot I$ en base a la primer fila, siendo idénticos.

En conclusión, $A$ y $A^{t}$ tienen el mismo polinomio característico.

### Parte 2
Como vimos en la parte anterior, podemos desarrollar los determinantes de $A - \lambda \cdot I$ y $A^{t} - \lambda \cdot I$ de tal manera que sean exactamente idénticos. Esto implica que tendrán el mismo polinomio característico, asociado a la misma transformación lineal. Por lo tanto, los valores propios (que coinciden con las raíces del polinomio característico) necesariamente tienen que ser los mismos.

### Parte 3
En este caso, tendríamos que desarrollar los sistemas correspondientes a cada matriz:
$$
\begin{pmatrix}
a_{1,1} - \lambda & a_{1,2} & \dots & a_{1,n} \\
a_{2,1} & a_{2,2} - \lambda & \dots & a_{2,n} \\
\vdots & \vdots  & \ddots & \vdots \\
a_{n,1} & a_{n,2} & \dots & a_{n,n} - \lambda
\end{pmatrix} \implies \begin{cases}
(a_{1,1} - \lambda) \cdot x_{1} + a_{1,2} \cdot x_{2} + \dots + a_{1,n} \cdot x_{n} = 0 \\
a_{2,1} \cdot x_{1} + (a_{2,2} - \lambda) \cdot x_{2} + \dots + a_{2,n} \cdot x_{n} = 0 \\
\dots \\
a_{n,1} \cdot x_{1} + a_{n,2} \cdot x_{2} + \dots + (a_{n,n} - \lambda) \cdot x_{n} = 0
\end{cases}
$$
$$
\begin{pmatrix}
a_{1,1} - \lambda & a_{2,1} & \dots & a_{n,1} \\
a_{1,2} & a_{2,2} - \lambda & \dots & a_{n,2} \\
\vdots & \vdots  & \ddots & \vdots \\
a_{1,n} & a_{2,n} & \dots & a_{n,n} - \lambda
\end{pmatrix} \implies \begin{cases}
(a_{1,1} - \lambda) \cdot x_{1} + a_{2,1} \cdot x_{2} + \dots + a_{n,1} \cdot x_{n} = 0 \\
a_{1,2} \cdot x_{1} + (a_{2,2} - \lambda) \cdot x_{2} + \dots + a_{n,2} \cdot x_{n} = 0 \\
\dots \\
a_{1,n} \cdot x_{1} + a_{2,n} \cdot x_{2} + \dots + (a_{n,n} - \lambda) \cdot x_{n} = 0
\end{cases}
$$
Como vemos, los sistemas homogéneos obtenidos no son iguales. Por lo tanto, los vectores propios no son necesariamente iguales.

---
## Ejercicio 7
Sean $A$ y $B$ 2 matrices semejantes de $n \times n$.

Si $A$ y $B$ son semejantes, $\exists C$ no singular tal que $B = C^{-1} A C$:
$$
\begin{align}
B &= C^{-1} A C \\
\lambda Id - B &= \lambda Id - C^{-1} A C \\
\lambda Id - B &= \lambda C^{-1} Id C - C^{-1} A C \\
\lambda Id - B &= C^{-1} [\lambda Id - A] C \\
\det(\lambda Id - B) &= \det(C^{-1} [\lambda Id - A] C) \\
\det(\lambda Id - B) &= \cancel{ \det(C^{-1}) } \cdot \det(\lambda Id - A) \cdot \cancel{ \det(C) } \\
\det(\lambda Id - B) &= \det(\lambda Id - A)
\end{align}
$$
$$
\implies \det(\lambda Id - B) = \det(\lambda Id - A)
$$
De esta forma, cuando igualemos a ambos lados a 0, las soluciones tendrán que ser necesariamente las mismas. Los polinomios serán idénticos, por lo que tendrán las mismas raíces.

Para determinar si existe alguna relación entre sus vectores propios, consideremos el siguiente desarrollo: Sea $v$ un vector propio de $B$, entonces:
$$
\begin{align}
B \cdot v &= \lambda \cdot v \\
(C^{-1} A C) \cdot v &= \lambda \cdot v \\
C(C^{-1} A C) \cdot v &= C(\lambda \cdot v) \\
(CC^{-1}) A C \cdot v &= \lambda \cdot (C \cdot v) \\
A (C \cdot v) &= \lambda \cdot (C \cdot v)
\end{align}
$$
De esta forma, logramos determinar que la relación entre sus vectores propios es directa: si $v$ es un vector propio de $B$, entonces $Cv$ es un vector propio de$A$ para el mismo valor propio $\lambda$.

---
# 3 - Diagonalización
## Ejercicio 8
En todos los casos, el procedimiento será:
1. Determinar la matriz asociada $T$ a la transformación, considerando los elementos de la base canónica.
2. Desarrollar el polinomio característico de la transformación ($\det(T - \lambda \cdot \mathbb{I})$).
3. Determinar los valores propios de la transformación (raíces del polinomio característico).
4. Para cada valor propio, hallar la forma de los vectores propios correspondientes (bases de cada subespacio característico).
5. En base a la cantidad de vectores propios linealmente independientes obtenidos, determinar si la transformación es diagonalizable o no.

### Transformación 1
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}, T(x, y, z) = (2y + z, 2x + z, x + y + z)
$$
$$
\begin{align}
&T(1, 0, 0) = (0, 2, 1) \\
&T(0, 1, 0) = (2, 0, 1) \\
&T(0, 0, 1) = (1, 1, 1)
\end{align}
$$
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
0 & 2 & 1 \\
2 & 0 & 1 \\
1 & 1 & 1
\end{pmatrix}
$$
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
-\lambda & 2 & 1 \\
2 & -\lambda & 1 \\
1 & 1 & 1 - \lambda
\end{array} \right| \\
&= -\lambda \cdot (\lambda^{2} - \lambda - 1) - 2 \cdot (2 - 2\lambda - 1) + 1 \cdot (2 + \lambda) \\
&= -\lambda \cdot (\lambda^{2} - \lambda - 1) - 2 \cdot (1 - 2\lambda) + 1 \cdot (2 + \lambda) \\
&= -\lambda^{3} + \lambda^{2} + \lambda - \cancel{ 2 } + 4\lambda + \cancel{ 2 } + \lambda \\
&= -\lambda^{3} + \lambda^{2} + 6\lambda \\
&= -\lambda \cdot (\lambda^{2} - \lambda - 6) \\
&= -\lambda \cdot (\lambda + 2) \cdot (\lambda - 3)
\end{align}
$$

- $-\lambda = 0$
$$
\begin{pmatrix}
0 & 2 & 1 \\
2 & 0 & 1 \\
1 & 1 & 1
\end{pmatrix} \implies \begin{pmatrix}
0 & 2 & 1 \\
2 & 0 & 1 \\
1 & -1 & 0
\end{pmatrix} \implies \begin{cases}
2y + z = 0 \\
2x + z = 0 \\
x - y = 0
\end{cases} \implies x = y \implies z = -2x = -2y
$$
$$
S_{0} = \{ (\alpha, \alpha, -2\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 1, -2) \}]
$$

- $\lambda + 2 = 0 \implies \lambda = -2$
$$
\begin{pmatrix}
2 & 2 & 1 \\
2 & 2 & 1 \\
1 & 1 & 3
\end{pmatrix} \implies \begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
1 & 1 & 0
\end{pmatrix} \implies \begin{cases}
z = 0 \\
x + y = 0
\end{cases} \implies y = -x
$$
$$
S_{2} = \{ (\alpha, -\alpha, 0) : \alpha \in \mathbb{R} \} = [\{ (1, -1, 0) \}]
$$

- $\lambda - 3 = 0 \implies \lambda = 3$
$$
\begin{pmatrix}
-3 & 2 & 1 \\
2 & -3 & 1 \\
1 & 1 & -2
\end{pmatrix} \implies \begin{pmatrix}
1 & -1 & 0 \\
0 & 1 & -1 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
x - y = 0 \\
y - z = 0
\end{cases} \implies x = y = z
$$
$$
S_{3} = \{ (\alpha, \alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 1, 1) \}]
$$

Ahora, determinamos que los elementos encontrados sean LI:
$$
\alpha(1, 1, -2) + \beta(1, -1, 0) + \gamma(1, 1, 1) = (0, 0, 0) \implies \begin{cases}
\alpha + \beta + \gamma = 0 \\
\alpha - \beta + \gamma = 0 \\
-2\alpha + \gamma = 0 \implies \gamma = 2\alpha
\end{cases}
$$
$$
\implies 2\alpha + 2\gamma = 0 \implies 6\alpha = 0 \implies \alpha = 0 \implies \gamma = 0 \implies \beta = 0
$$
En conclusión, los vectores propios son LI. Por lo tanto, como encontramos un conjunto de vectores propios de cardinal equivalente a $dim(\mathbb{R}^{3}) = 3$, podemos asegurar que la transformación lineal es diagonalizable.

### Transformación 2
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}, T(x, y, z) = (4x - 5y + 2z, 5x - y_{7} + 3z, 6x - 9y + 4z)
$$
$$
\begin{align}
&T(1, 0, 0) = (4, 5, 6) \\
&T(0, 1, 0) = (-5, -7, -9) \\
&T(0, 0, 1) = (2, 3, 4)
\end{align}
$$
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
4 & -5 & 2 \\
5 & -7 & 3 \\
6 & -9 & 4
\end{pmatrix}
$$
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
4 - \lambda & -5 & 2 \\
5 & -7 - \lambda & 3 \\
6 & -9 & 4 - \lambda
\end{array} \right| \\
&= (4 - \lambda) \cdot ((-7 - \lambda) \cdot (4 - \lambda) + 27) - 5 \cdot (-5 \cdot (4 - \lambda) + 18) + 6 \cdot (-15 - ((-7 - \lambda) \cdot 2)) \\
&= (4 - \lambda) \cdot (\lambda^{2} + 3\lambda - 1) - 5 \cdot (5\lambda - 2) + 6 \cdot (2\lambda - 1) \\
&= -\lambda^{3} + \lambda^{2} + 13\lambda - 4 - 25\lambda + 10 + 12\lambda - 6 \\
&= -\lambda^{3} + \lambda^{2} \\
&= \lambda^{2}(1 - \lambda)
\end{align}
$$

- $\lambda^{2} = 0 \implies \lambda = 0$
$$
\begin{pmatrix}
4 & -5 & 2 \\
5 & -7 & 3 \\
6 & -9 & 4
\end{pmatrix} \implies \begin{pmatrix}
3 & 0 & -1 \\
-2 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
3x - z = 0 \\
-2x + y = 0
\end{cases} \implies y = 2x \land z = 3x
$$
$$
S_{0} = \{ (\alpha, 2\alpha, 3\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 2, 3) \}]
$$

- $1 - \lambda = 0 \implies \lambda = 1$
$$
\begin{pmatrix}
3 & -5 & 2 \\
5 & -8 & 3 \\
6 & -9 & 3
\end{pmatrix} \implies \begin{pmatrix}
0 & -1 & 1 \\
1 & -1 & 0 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
-y + z = 0 \\
x - y = 0
\end{cases} \implies y = x = z
$$
$$
S_{1} = \{ (\alpha, \alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 1, 1) \}]
$$

En este caso, encontramos únicamente dos elementos base de vectores propios LI, y como $dim(\mathbb{R}^{3}) = 3$, resulta que no podemos formar una base de dicho espacio vectorial con los vectores determinados. Por esta razón, la transformación no es diagonalizable.

### Transformación 3
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}, T(x, y, z) = (y, -4x + 4y, 2x + y + 2z)
$$
$$
\begin{align}
&T(1, 0, 0) = (0, -4, 2) \\
&T(0, 1, 0) = (1, 4, 1) \\
&T(0, 0, 1) = (0, 0, 2)
\end{align}
$$
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
0 & 1 & 0 \\
-4 & 4 & 0 \\
2 & 1 & 2
\end{pmatrix}
$$
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
-\lambda & 1 & 0 \\
-4 & 4 - \lambda & 0 \\
2 & 1 & 2 - \lambda
\end{array} \right| \\
&= (2 - \lambda) \cdot (-\lambda \cdot (4 - \lambda) + 4) \\
&= (2 - \lambda) \cdot (\lambda^{2} - 4\lambda + 4) \\
&= (2 - \lambda) \cdot (\lambda - 2)^{2} \\
&= -(\lambda - 2) \cdot (\lambda - 2)^{2} \\
&= -(\lambda - 2)^{3}
\end{align}
$$

- $\lambda - 2 = 0 \implies \lambda = 2$
$$
\begin{pmatrix}
-2 & 1 & 0 \\
-4 & 2 & 0 \\
2 & 1 & 0
\end{pmatrix} \implies \begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 0\\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
y = 0 \\
x = 0
\end{cases} \implies x = y = 0 \land z \text{ es libre}
$$
$$
S_{2} = \{ (0, 0, \alpha) : \alpha \in \mathbb{R} \} = [\{ (0, 0, 1) \}]
$$

Encontramos únicamente un elemento base de vectores propios LI, y como $dim(\mathbb{R}^{3}) = 3$, resulta que no podemos formar una base de dicho espacio vectorial con los vectores determinados. Por esta razón, la transformación no es diagonalizable.

### Transformación 3
$$
T : \mathbb{R}^{3} \to \mathbb{R}^{3}, T(x, y, z) = (2x, 2y, 2z)
$$
$$
\begin{align}
&T(1, 0, 0) = (2, 0, 0) \\
&T(0, 1, 0) = (0, 2, 0) \\
&T(0, 0, 1) = (0, 0, 2)
\end{align}
$$
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{pmatrix}
$$
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
2 - \lambda & 0 & 0 \\
0 & 2 - \lambda & 0 \\
0 & 0 & 2 - \lambda
\end{array} \right| \\
&= (2 - \lambda) \cdot ((2 - \lambda) \cdot (2 - \lambda)) \\
&= (2 - \lambda) \cdot ((2 - \lambda)^{2}) \\
&= (2 - \lambda)^{3}
\end{align}
$$

- $2 - \lambda = 0 \implies \lambda = 2$
$$
\begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}\implies x, y, z \text{ son libres}
$$
$$
S_{2} = \{ (\alpha, \beta, \gamma) : \alpha, \beta, \gamma \in \mathbb{R} \} = [\{ (1, 0, 0), (0, 1, 0), (0, 0, 1) \}]
$$

Encontramos tres elemento base de vectores propios LI, y como $dim(\mathbb{R}^{3}) = 3$, podemos formar una base de dicho espacio vectorial con los vectores propios determinados. Por esta razón, la transformación es diagonalizable.

---
## Ejercicio 9
### Matriz a
$$
A = \begin{pmatrix}
4 & 1 - i \\
1 + i & 5
\end{pmatrix}
$$

#### Parte 1
$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{cc}
4 - \lambda & 1 - i \\
1 + i & 5 - \lambda
\end{array} \right| \\
&= (4 - \lambda) \cdot (5 - \lambda) - (1 + i) \cdot (1 - i) \\
&= \lambda^{2} - 9\lambda + 20 - 2 \\
&= \lambda^{2} - 9\lambda + 18 \\
&= (\lambda - 3) \cdot (\lambda - 6)
\end{align}
$$

- $\lambda - 3 = 0 \implies \lambda = 3$
$$
\begin{pmatrix}
1 & 1 - i \\
1 + i & 2
\end{pmatrix} \implies \begin{pmatrix}
1 & 1 - i \\
0 & 0
\end{pmatrix} \implies \begin{cases}
x + (1 - i)y = 0
\end{cases} \implies x = -(1 - i)y
$$
$$
S_{3} = \{ (-(1 - i)\alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (i - 1, 1) \}]
$$

- $\lambda - 6 = 0 \implies \lambda = 6$
$$
\begin{pmatrix}
-2 & 1 - i \\
1 + i & -1
\end{pmatrix} \implies \begin{pmatrix}
1 + i & -1 \\
0 & 0
\end{pmatrix} \implies \begin{cases}
(1 + i)x - y = 0
\end{cases} \implies y = (1 + i)x
$$
$$
S_{6} = \{ (\alpha, (1 + i)\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, i + 1) \}]
$$

#### Parte 2
Determinamos si los vectores propios obtenidos son LI:
$$
\alpha \cdot (i - 1, 1) + \beta \cdot (1, i + 1) = (0, 0) \implies \begin{cases}
(i - 1)\alpha + \beta = 0 \\
\alpha + (i + 1)\beta = 0
\end{cases}
$$
$$
\implies (i + 1)((i - 1)\alpha + \beta) = 2\alpha + (i + 1)\beta = 0 \implies \alpha = 0 \implies \beta = 0
$$
Efectivamente, el conjunto es LI, por lo que encontramos una base de $\mathbb{C}^{2}$ (conjunto LI cuyo cardinal coincide con $dim(\mathbb{C}^{2}) = 2$). De esta manera, probamos que $A$ es diagonalizable.

#### Parte 3
Queremos encontrar $D$ diagonal, semejante a $A$. Para esto, aprovecharemos la igualdad de matrices semejantes: si dos matrices $A$ y $D$ son semejantes, entonces existe una matriz de igual tamaño $P$ invertible, tal que $D = P^{-1} A P$.

Podemos expresar a $P$ utilizando los vectores propios determinados anteriormente:
$$
P = \begin{pmatrix}
i - 1 & 1 \\
1 & i + 1
\end{pmatrix}
$$
Entonces, determinamos $P^{-1}$:
$$
\left( \begin{array}{cc|cc}
i - 1 & 1 & 1 & 0 \\
1 & i + 1 & 0 & 1
\end{array} \right)
$$
$$
\left( \begin{array}{cc|cc}
i - 1 & 1 & 1 & 0 \\
i - 1 & -2 & 0 & i - 1
\end{array} \right)
\begin{align}
&F_{2} \leftarrow (i - 1)F_{2}
\end{align}
$$
$$
\left( \begin{array}{cc|cc}
i - 1 & 1 & 1 & 0 \\
0 & -3 & -1 & i - 1
\end{array} \right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
$$
\left( \begin{array}{cc|cc}
i - 1 & 1 & 1 & 0 \\
0 & 1 & \frac{1}{3} & \frac{1}{3} - \frac{1}{3}i
\end{array} \right)
\begin{align}
&F_{2} \leftarrow -\frac{1}{3}F_{2}
\end{align}
$$
$$
\left( \begin{array}{cc|cc}
i - 1 & 0 & \frac{2}{3} & \frac{1}{3}i - \frac{1}{3} \\
0 & 1 & \frac{1}{3} & \frac{1}{3} - \frac{1}{3}i
\end{array} \right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left( \begin{array}{cc|cc}
1 & 0 & -\left( \frac{1}{3} + \frac{1}{3}i \right) & \frac{1}{3} \\
0 & 1 & \frac{1}{3} & \frac{1}{3} - \frac{1}{3}i
\end{array} \right)
\begin{align}
&F_{1} \leftarrow \frac{i + 1}{2}F_{1}
\end{align}
$$
De esta manera:
$$
P^{-1} = \frac{1}{3} \cdot \begin{pmatrix}
-(1 + i) & 1 \\
1 & 1 - i
\end{pmatrix}
$$

Ahora, sustituimos las matrices correspondientes para determinar $D$:
$$
D = P^{-1} A P \implies \frac{1}{3} \cdot \begin{pmatrix}
-(1 + i) & 1 \\
1 & 1 - i
\end{pmatrix} \cdot \begin{pmatrix}
4 & 1 - i \\
1 + i & 5
\end{pmatrix} \cdot \begin{pmatrix}
i - 1 & 1 \\
1 & i + 1
\end{pmatrix}
$$
$$
\begin{pmatrix}
4 & 1 - i \\
1 + i & 5
\end{pmatrix} \cdot \begin{pmatrix}
i - 1 & 1 \\
1 & i + 1
\end{pmatrix} = \begin{pmatrix}
4i - 4 + 1 - i & 4 + 2 \\
-2 + 5 & 1 + i + 5i + 5
\end{pmatrix} = \begin{pmatrix}
3i - 3 & 6 \\
3 & 6 + 6i
\end{pmatrix}
$$
$$
\frac{1}{3} \cdot \begin{pmatrix}
-(1 + i) & 1 \\
1 & 1 - i
\end{pmatrix} \cdot \begin{pmatrix}
3i - 3 & 6 \\
3 & 6 + 6i
\end{pmatrix} = \frac{1}{3} \begin{pmatrix}
6 + 3 & -6 - 6i + 6 + 6i \\
3i - 3 + 3 - 3i & 6 + 12
\end{pmatrix} = \frac{1}{3} \begin{pmatrix}
9 & 0 \\
0 & 18
\end{pmatrix} = \begin{pmatrix}
3 & 0 \\
0 & 6
\end{pmatrix}
$$

En conclusión, la matriz diagonal $D$ semejante a $A$ es:
$$
D = \begin{pmatrix}
3 & 0 \\
0 & 6
\end{pmatrix}
$$

### Matriz b
$$
A = \begin{pmatrix}
0 & 0 & -2 \\
1 & 2 & 1 \\
1 & 0 & 3
\end{pmatrix}
$$

#### Parte 1
$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
-\lambda & 0 & -2 \\
1 & 2 - \lambda & 1 \\
1 & 0 & 3 - \lambda
\end{array} \right| \\
&= (2 - \lambda) \cdot ((-\lambda) \cdot (3 - \lambda) + 2) \\
&= (2 - \lambda) \cdot (\lambda^{2} - 3\lambda + 2) \\
&= (2 - \lambda) \cdot (\lambda - 2) \cdot (\lambda - 1) \\
&= -(\lambda - 2) \cdot (\lambda - 2) \cdot (\lambda - 1) \\
&= -(\lambda - 2)^{2} \cdot (\lambda - 1)
\end{align}
$$

- $\lambda - 2 = 0 \implies \lambda = 2$
$$
\begin{pmatrix}
-2 & 0 & -2 \\
1 & 0 & 1 \\
1 & 0 & 1
\end{pmatrix} \implies \begin{pmatrix}
1 & 0 & 1 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
x + z = 0
\end{cases} \implies z = -x \land y \text{ es libre}
$$
$$
S_{2} = \{ (\alpha, \beta, - \alpha) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 0, -1), (0, 1, 0) \}]
$$

- $\lambda - 1 = 0 \implies \lambda = 1$
$$
\begin{pmatrix}
-1 & 0 & -2 \\
1 & 1 & 1 \\
1 & 0 & 2
\end{pmatrix} \implies \begin{pmatrix}
1 & 0 & 2 \\
0 & 1 & -1 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
x + 2z = 0 \\
y - z = 0
\end{cases} \implies x = -2z \land y = z
$$
$$
S_{1} = \{ (-2\alpha, \alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (-2, 1, 1) \}]
$$

#### Parte 2
Determinamos si los vectores propios obtenidos son LI:
$$
\alpha \cdot (1, 0, -1) + \beta \cdot (0, 1, 0) + \gamma \cdot (-2, 1, 1) = (0, 0, 0) \implies \begin{cases}
\alpha - 2\gamma = 0 \\
\beta + \gamma = 0 \\
-\alpha + \gamma = 0
\end{cases}
$$
$$
\implies -\gamma = 0 \implies \gamma = 0 \implies \beta = 0 \implies \alpha = 0
$$
Efectivamente, el conjunto es LI, por lo que encontramos una base de $\mathbb{R}^{3}$ (conjunto LI cuyo cardinal coincide con $dim(\mathbb{R}^{3}) = 3$). De esta manera, probamos que $A$ es diagonalizable.

#### Parte 3
Expresamos a $P$ utilizando los vectores propios determinados anteriormente:
$$
P = \begin{pmatrix}
1 & 0 & -2 \\
0 & 1 & 1 \\
-1 & 0 & 1
\end{pmatrix}
$$
Entonces, determinamos $P^{-1}$:
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & -2 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
-1 & 0 & 1 & 0 & 0 & 1
\end{array} \right)
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & -2 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & -1 & 1 & 0 & 1
\end{array} \right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & -2 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & -1 & 0 & -1
\end{array} \right)
\begin{align}
&F_{3} \leftarrow -F_{3}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & 0 & -1 & 0 & -2 \\
0 & 1 & 0 & 1 & 1 & 1 \\
0 & 0 & 1 & -1 & 0 & -1
\end{array} \right)
\begin{align}
&F_{1} \leftarrow F_{1} + 2F_{3} \\
&F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
De esta manera:
$$
P^{-1} = \begin{pmatrix}
-1 & 0 & -2 \\
1 & 1 & 1 \\
-1 & 0 & -1
\end{pmatrix}
$$

Ahora, sustituimos las matrices correspondientes para determinar $D$:
$$
D = P^{-1} A P \implies \begin{pmatrix}
-1 & 0 & -2 \\
1 & 1 & 1 \\
-1 & 0 & -1
\end{pmatrix} \cdot \begin{pmatrix}
0 & 0 & -2 \\
1 & 2 & 1 \\
1 & 0 & 3
\end{pmatrix} \cdot \begin{pmatrix}
1 & 0 & -2 \\
0 & 1 & 1 \\
-1 & 0 & 1
\end{pmatrix}
$$
$$
\begin{pmatrix}
0 & 0 & -2 \\
1 & 2 & 1 \\
1 & 0 & 3
\end{pmatrix} \cdot \begin{pmatrix}
1 & 0 & -2 \\
0 & 1 & 1 \\
-1 & 0 & 1
\end{pmatrix} = \begin{pmatrix}
2 & 0 & -2 \\
1 - 1 & 2 & -2 + 2 + 1 \\
1 - 3 & 0 & -2 + 3
\end{pmatrix} = \begin{pmatrix}
2 & 0 & -2 \\
0 & 2 & 1 \\
-2 & 0 & 1
\end{pmatrix}
$$
$$
\begin{pmatrix}
-1 & 0 & -2 \\
1 & 1 & 1 \\
-1 & 0 & -1
\end{pmatrix} \cdot \begin{pmatrix}
2 & 0 & -2 \\
0 & 2 & 1 \\
-2 & 0 & 1
\end{pmatrix} = \begin{pmatrix}
-2 + 4 & 0 & 2 - 2 \\
2 - 2 & 2 & -2 + 1 + 1 \\
-2 + 2 & 0 & 2 - 1
\end{pmatrix} = \begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$

En conclusión, la matriz $D$ semejante a $A$ es:
$$
D = \begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$

### Matriz c
$$
A = \begin{pmatrix}
5 & 0 & 0 \\
0 & -1 & -1 + i \\
0 & -1 - i & 0
\end{pmatrix}
$$

#### Parte 1
$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
5 - \lambda & 0 & 0 \\
0 & -1 - \lambda & -1 + i \\
0 & -1 - i & -\lambda
\end{array} \right| \\
&= (5 - \lambda) \cdot ((-1 - \lambda) \cdot (-\lambda) - (-1 - i) \cdot (-1 + i)) \\
&= (5 - \lambda) \cdot ((\lambda^{2} + \lambda) - (1 - i + i - i^{2})) \\
&= (5 - \lambda) \cdot (\lambda^{2} + \lambda - 2) \\
&= (5 - \lambda) \cdot (\lambda + 2) \cdot (\lambda - 1) \\
&= -(\lambda - 5) \cdot (\lambda + 2) \cdot (\lambda - 1)
\end{align}
$$

- $\lambda - 5 = 0 \implies \lambda = 5$
$$
\begin{pmatrix}
0 & 0 & 0 \\
0 & -6 & -1 + i \\
0 & -1 - i & -5
\end{pmatrix} \implies \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 1 \\
0 & 1 & 0
\end{pmatrix} \implies \begin{cases}
y = 0 \\
z = 0
\end{cases} \implies x \text{ es libre}
$$
$$
S_{5} = \{ (\alpha, 0, 0) : \alpha \in \mathbb{R} \} = [\{ (1, 0, 0) \}]
$$

- $\lambda + 2 = 0 \implies \lambda = -2$
$$
\begin{pmatrix}
7 & 0 & 0 \\
0 & 1 & -1 + i \\
0 & -1 - i & 2
\end{pmatrix} \implies \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & -1 + i \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
x = 0 \\
y + (-1 + i)z = 0
\end{cases} \implies y = (1 - i)z
$$
$$
S_{-2} = \{ (0, (1 - i)\alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (0, 1 - i, 1) \}]
$$

- $\lambda - 1 = 0 \implies \lambda = 1$
$$
\begin{pmatrix}
4 & 0 & 0 \\
0 & -2 & -1 + i \\
0 & -1 - i & -1
\end{pmatrix} \implies \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 + i & 1 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
x = 0 \\
(1 + i)y + z = 0
\end{cases} \implies z = -(1 + i)y
$$
$$
S_{1} = \{ (0, \alpha, -(1 + i)\alpha) : \alpha \in \mathbb{R} \} = [\{ (0, 1, -1 - i) \}]
$$

#### Parte 2
Determinamos si los vectores propios obtenidos son LI:
$$
\alpha \cdot (1, 0, 0) + \beta \cdot (0, 1 - i, 1) + \gamma \cdot (0, 1, -1 - i) = (0, 0, 0) \implies \begin{cases}
\alpha = 0 \\
(1 - i)\beta + \gamma = 0 \\
\beta - (1 + i)\gamma = 0
\end{cases}
$$
$$
\implies 3\beta = 0 \implies \beta = 0 \implies \gamma = 0
$$
Efectivamente, el conjunto es LI, por lo que encontramos una base de $\mathbb{C}^{3}$ (conjunto LI cuyo cardinal coincide con $dim(\mathbb{C}^{3}) = 3$). De esta manera, probamos que $A$ es diagonalizable.

#### Parte 3
Expresamos a $P$ utilizando los vectores propios determinados anteriormente:
$$
P = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 - i & 1 \\
0 & 1 & -(1 + i)
\end{pmatrix}
$$
Entonces, determinamos $P^{-1}$:
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 - i & 1 & 0 & 1 & 0 \\
0 & 1 & -(1 + i) & 0 & 0 & 1
\end{array} \right)
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 - i & 1 & 0 & 1 & 0 \\
0 & 1 - i & -2 & 0 & 0 & 1 - i
\end{array} \right)
\begin{align}
&F_{3} \leftarrow (1 - i)F_{3}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 - i & 1 & 0 & 1 & 0 \\
0 & 0 & -3 & 0 & -1 & 1 - i
\end{array} \right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 - i & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & \frac{1}{3} & -\frac{1}{3} + \frac{1}{3}i
\end{array} \right)
\begin{align}
&F_{3} \leftarrow -\frac{1}{3}F_{3}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 - i & 0 & 0 & \frac{2}{3} & \frac{1}{3} - \frac{1}{3}i \\
0 & 0 & 1 & 0 & \frac{1}{3} & -\frac{1}{3} + \frac{1}{3}i
\end{array} \right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & 0 & \frac{1}{3} + \frac{1}{3}i & \frac{1}{3} \\
0 & 0 & 1 & 0 & \frac{1}{3} & -\frac{1}{3} + \frac{1}{3}i
\end{array} \right)
\begin{align}
&F_{2} \leftarrow \frac{1 + i}{2}F_{2}
\end{align}
$$

De esta manera:
$$
P^{-1} = \frac{1}{3} \cdot \begin{pmatrix}
3 & 0 & 0 \\
0 & 1 + i & 1 \\
0 & 1 & -1 + i
\end{pmatrix}
$$

Ahora, sustituimos las matrices correspondientes para determinar $D$:
$$
D = P^{-1} A P \implies \frac{1}{3} \cdot \begin{pmatrix}
3 & 0 & 0 \\
0 & 1 + i & 1 \\
0 & 1 & -1 + i
\end{pmatrix} \cdot \begin{pmatrix}
5 & 0 & 0 \\
0 & -1 & -1 + i \\
0 & -1 - i & 0
\end{pmatrix} \cdot \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 - i & 1 \\
0 & 1 & -(1 + i)
\end{pmatrix}
$$
$$
\begin{pmatrix}
5 & 0 & 0 \\
0 & -1 & -1 + i \\
0 & -1 - i & 0
\end{pmatrix} \cdot \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 - i & 1 \\
0 & 1 & -(1 + i)
\end{pmatrix} = \begin{pmatrix}
5 & 0 & 0 \\
0 & -1 + i - 1 + i & -1 + 2 \\
0 & -2 & -1 - i
\end{pmatrix} = \begin{pmatrix}
5 & 0 & 0 \\
0 & -2 + 2i & 1 \\
0 & -2 & -1 - i
\end{pmatrix}
$$
$$
\frac{1}{3} \cdot \begin{pmatrix}
3 & 0 & 0 \\
0 & 1 + i & 1 \\
0 & 1 & -1 + i
\end{pmatrix} \cdot \begin{pmatrix}
5 & 0 & 0 \\
0 & -2 + 2i & 1 \\
0 & -2 & -1 - i
\end{pmatrix} = \frac{1}{3} \cdot \begin{pmatrix}
15 & 0 & 0 \\
0 & -2 + 2i - 2i + 2i^{2} - 2 & 1 + i - 1 - i \\
0 & -2 + 2i + 2 - 2i & 1 + 2
\end{pmatrix} = \frac{1}{3} \cdot \begin{pmatrix}
15 & 0 & 0 \\
0 & -6 & 0 \\
0 & 0 & 3
\end{pmatrix} = \begin{pmatrix}
5 & 0 & 0 \\
0 & -2 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$

En conclusión, la matriz $D$ semejante a $A$ es:
$$
D = \begin{pmatrix}
5 & 0 & 0 \\
0 & -2 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$



---
## Ejercicio 10
### Matriz $M$
$$
M = \begin{pmatrix}
a & 1 & -1 \\
2 & a & 2 \\
1 & 1 & a
\end{pmatrix}
$$
$$
\begin{align}
\det(M - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
a - \lambda & 1 & -1 \\
2 & a - \lambda & 2 \\
1 & 1 & a - \lambda
\end{array} \right| \\
&= (a - \lambda) \cdot ((a - \lambda)^{2} - 2) - (2a - 2\lambda - 2) - (2 - a + \lambda) \\
&= (a - \lambda) \cdot ((a - \lambda)^{2} - 2) - (a - \lambda) \\
&= (a - \lambda) \cdot ((a - \lambda)^{2} - 2 - 1) \\
&= (a - \lambda) \cdot ((a - \lambda)^{2} - 3)
\end{align}
$$

Entonces, determinamos los tres posibles valores de $\lambda$:
- $a - \lambda = 0 \implies \lambda_{1} = a$
$$
\begin{pmatrix}
0 & 1 & -1 \\
2 & 0 & 2 \\
1 & 1 & 0
\end{pmatrix} \implies \begin{pmatrix}
0 & 1 & -1 \\
1 & 0 & 1 \\
1 & 1 & 0
\end{pmatrix} \implies \begin{cases}
y - z = 0 \\
x + z = 0 \\
x + y = 0
\end{cases} \implies y = z = -x
$$
$$
S_{a} = \{ (-\alpha, \alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (-1, 1, 1) \}]
$$

$$
(a - \lambda)^{2} - 3 = 0 \implies (a - \lambda)^{2} = 3 \implies a - \lambda = \pm \sqrt{ 3 } \implies \lambda = a \pm \sqrt{ 3 }
$$
- $\lambda_{2} = a + \sqrt{ 3 }$
$$
\begin{pmatrix}
-\sqrt{ 3 } & 1 & -1 \\
2 & -\sqrt{ 3 } & 2 \\
1 & 1 & -\sqrt{ 3 }
\end{pmatrix} \implies \begin{pmatrix}
0 & 1 & 2 - 2\sqrt{ 3 } \\
1 & 0 & -2 + \sqrt{ 3 } \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
y + (2 - 2\sqrt{ 3 })z = 0 \\
x - (2 - \sqrt{ 3 })z = 0
\end{cases} \implies x = (2 - \sqrt{ 3 })z \land y = (-2 + 2\sqrt{ 3 })z
$$
$$
S_{a + \sqrt{ 3 }} = \{ ((2 - \sqrt{ 3 })\alpha, (-2 + 2\sqrt{ 3 })\alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (2 - \sqrt{ 3 }, -2 + 2\sqrt{ 3 }, 1) \}]
$$

- $\lambda_{3} = a - \sqrt{ 3 }$
$$
\begin{pmatrix}
\sqrt{ 3 } & 1 & -1 \\
2 & \sqrt{ 3 } & 2 \\
1 & 1 & \sqrt{ 3 }
\end{pmatrix} \implies \begin{pmatrix}
0 & 1 & 2 + 2\sqrt{ 3 } \\
1 & 0 & -2 - \sqrt{ 3 } \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
y + (2 + 2\sqrt{ 3 })z = 0 \\
x - (2 + \sqrt{ 3 })z = 0
\end{cases} \implies x = (2 + \sqrt{ 3 })z \land y = (-2 - 2\sqrt{ 3 })z
$$
$$
S_{a - \sqrt{ 3 }} = \{ ((2 + \sqrt{ 3 })\alpha, (-2 - 2\sqrt{ 3 })\alpha, \alpha) : \alpha \in \mathbb{R} \} = [\{ (2 + \sqrt{ 3 }, -2 - 2\sqrt{ 3 }, 1) \}]
$$

Ahora, lo que nos queda probar es que los elementos de las bases determinadas son LI:
$$
\alpha \cdot (-1, 1, 1) + \beta \cdot (2 - \sqrt{ 3 }, -2 + 2\sqrt{ 3 }, 1) + \gamma \cdot (2 + \sqrt{ 3 }, -2 - 2\sqrt{ 3 }, 1) = (0, 0, 0)
$$
$$
\implies \begin{cases}
-\alpha + (2 - \sqrt{ 3 })\beta + (2 + \sqrt{ 3 })\gamma = 0 \\
\alpha + (-2 + 2\sqrt{ 3 })\beta + (-2 - 2\sqrt{ 3 })\gamma = 0 \\
\alpha + \beta + \gamma = 0
\end{cases}
$$
$$
\begin{pmatrix}
-1 & 2 - \sqrt{ 3 } & 2 + \sqrt{ 3 } \\
1 & -2 + 2\sqrt{ 3 } & -2 - 2\sqrt{ 3 } \\
1 & 1 & 1
\end{pmatrix}
$$
$$
\begin{pmatrix}
0 & 3 - \sqrt{ 3 } & 3 + \sqrt{ 3 } \\
0 & -3 + 2\sqrt{ 3 } & -3 - 2\sqrt{ 3 } \\
1 & 1 & 1
\end{pmatrix}
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3} \\
&F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
$$
\begin{pmatrix}
0 & 3 - \sqrt{ 3 } & 3 + \sqrt{ 3 } \\
0 & \sqrt{ 3 } & -\sqrt{ 3 } \\
1 & 1 & 1
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow F_{2} + F_{1}
\end{align}
$$
$$
\begin{pmatrix}
0 & 3 & 3 \\
0 & \sqrt{ 3 } & -\sqrt{ 3 } \\
1 & 1 & 1
\end{pmatrix}
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2}
\end{align}
$$
$$
\begin{pmatrix}
0 & 1 & 1 \\
0 & 1 & -1 \\
1 & 1 & 1
\end{pmatrix}
\begin{align}
&F_{1} \leftarrow \frac{1}{3}F_{1} \\
&F_{2} \leftarrow \frac{\sqrt{ 3 }}{3}F_{2}
\end{align}
$$
$$
\begin{pmatrix}
0 & 1 & 1 \\
0 & 2 & 0 \\
1 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow F_{2} + F_{1} \\
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\begin{pmatrix}
0 & 1 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow \frac{1}{2}F_{2}
\end{align}
$$
$$
\begin{pmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
Como vemos, el sistema es LI. Por lo tanto, $T$ es diagonalizable para cualquier valor de $a$.

### Matriz $N$
$$
N = \begin{pmatrix}
0 & 0 & 1 \\
0 & b & 0 \\
a & 0 & 0
\end{pmatrix}
$$
$$
\begin{align}
\det(N - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
-\lambda & 0 & 1 \\
0 & b - \lambda & 0 \\
a & 0 & -\lambda
\end{array} \right| \\
&= (-\lambda) \cdot (b - \lambda) \cdot (-\lambda) - a \cdot (b - \lambda) \\
&= \lambda^{2} \cdot (b - \lambda) - a \cdot (b - \lambda) \\
&= (b - \lambda) \cdot (\lambda^{2} - a)
\end{align}
$$

Entonces, determinamos los tres posibles valores de $\lambda$:
- $b - \lambda = 0 \implies \lambda_{1} = b$
$$
\begin{pmatrix}
-b & 0 & 1 \\
0 & 0 & 0 \\
a & 0 & -b
\end{pmatrix} \implies \begin{pmatrix}
-b & 0 & 1 \\
0 & 0 & 0 \\
a - b^{2} & 0 & 0
\end{pmatrix} \implies \begin{cases}
-bx + z = 0 \\
(a - b^{2})x = 0
\end{cases}
$$

$$
\lambda^{2} - a = 0 \implies \lambda^{2} = a \implies \lambda = \pm \sqrt{ a }
$$
- $\lambda_{2} = \sqrt{ a }$
$$
\begin{pmatrix}
-\sqrt{ a } & 0 & 1 \\
0 & b - \sqrt{ a } & 0 \\
a & 0 & -\sqrt{ a }
\end{pmatrix} \implies \begin{pmatrix}
-\sqrt{ a } & 0 & 1 \\
0 & b - \sqrt{ a } & 0 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
-\sqrt{ a }x + z = 0 \\
(b - \sqrt{ a })y = 0
\end{cases}
$$

- $\lambda_{3} = -\sqrt{ a }$
$$
\begin{pmatrix}
\sqrt{ a } & 0 & 1 \\
0 & b + \sqrt{ a } & 0 \\
a & 0 & \sqrt{ a }
\end{pmatrix} \implies \begin{pmatrix}
\sqrt{ a } & 0 & 1 \\
0 & b + \sqrt{ a } & 0 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
\sqrt{ a }x + z = 0 \\
(b + \sqrt{ a })y = 0
\end{cases}
$$


Ahora, analicemos los casos posibles:

- $a < 0$:
En este caso, las raíces de $\lambda_{2} = \sqrt{ a }$ y $\lambda_{3} = -\sqrt{ a }$ son complejas. Por lo tanto, la matriz no será diagonalizable, ya que estamos trabajando en $\mathbb{R}$.

- $a = b = 0$
$$
S_{b} = \{ (\alpha, \beta, 0) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 0, 0), (0, 1, 0) \}]
$$
$$
S_{\sqrt{ a }} = \{ (\alpha, \beta, 0) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 0, 0), (0, 1, 0) \}]
$$
$$
S_{-\sqrt{ a }} = \{ (\alpha, \beta, 0) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 0, 0), (0, 1, 0) \}]
$$
Como vemos, únicamente determinamos los vectores propios LI $(1, 0, 0), (0, 1, 0)$, los cuales no pueden formar una base (ya que estamos en un espacio de dimensión 3).

- $a = 0 \neq b$
$$
S_{b} = \{ (0, 0, 0) \} = [\{ (0, 0, 0) \}]
$$
$$
S_{\sqrt{ a }} = \{ (\alpha, 0, 0) : \alpha \in \mathbb{R} \} = [\{ (1, 0, 0) \}]
$$
$$
S_{-\sqrt{ a }} = \{ (\alpha, 0, 0) : \alpha \in \mathbb{R} \} = [\{ (1, 0, 0) \}]
$$
Como vemos, únicamente determinamos el vector propio LI $(1, 0, 0)$, el cual no puede formar una base (ya que estamos en un espacio de dimensión 3).

- $a = b^{2} \neq 0 \land \sqrt{ a } = b$
$$
S_{b} = \{ (\alpha, \beta, b\alpha) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 0, b), (0, 1, 0) \}]
$$
$$
S_{\sqrt{ a }} = \{ (\alpha, \beta, b\alpha) : \alpha, \beta \in \mathbb{R} \} = [\{ (1, 0, b), (0, 1, 0) \}]
$$
$$
S_{-\sqrt{ a }} = \{ (\alpha, 0, -b\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 0, -b) \}]
$$
En este caso, logramos encontrar una base $\{ (1, 0, b), (0, 1, 0), (1, 0, -b) \}$ conformada por vectores propios. Por lo tanto, para los valores establecidos (y también para $-\sqrt{ a } = b$), la matriz es diagonalizable.

- $a \neq b^{2} \neq 0$
$$
S_{b} = \{ (0, \alpha, 0) : \alpha \in \mathbb{R} \} = [\{ (0, 1, 0) \}]
$$
$$
S_{\sqrt{ a }} = \{ (\alpha, 0, \sqrt{ a }\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 0, \sqrt{ a }) \}]
$$
$$
S_{-\sqrt{ a }} = \{ (\alpha, 0, -\sqrt{ a }\alpha) : \alpha \in \mathbb{R} \} = [\{ (1, 0, -\sqrt{ a }) \}]
$$
Logramos encontrar una base $\{ (1, 0, \sqrt{ a }), (0, 1, 0), (1, 0, -\sqrt{ a }) \}$ conformada por vectores propios. Por lo tanto, para los valores establecidos, la matriz es diagonalizable.

Por lo tanto, los valores de $a$ y $b$ para los cuales la matriz $N$ es diagonalizable son: $a > 0$. Simplemente esa es la condición, ya que la matriz es diagonalizable tanto para $a \neq b^{2} \neq 0$ como para $a = b^{2} \neq 0 \implies \pm\sqrt{ a } = b$

---
## Ejercicio 11
Sea $A$ la matriz asociada en la base canónica a la transformación lineal mencionada. Como $T$ es simétrica, se cumple que $A = A^{T}$, lo que implica que $\det(A) = \det(A^{T})$. Entonces, podemos representar a $A$ como:
$$
A = \begin{pmatrix}
a & b \\
b & c
\end{pmatrix}
$$
Ahora, desarrollamos el determinante de la matriz $A - \lambda \cdot \mathbb{I}$:
$$
\begin{align}
\det(A - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{cc}
a - \lambda & b \\
b & c - \lambda
\end{array} \right| \\
&= (a - \lambda)(c - \lambda) - b^{2} \\
&= \lambda^{2} - (a + c)\lambda + (ac - b^{2})
\end{align}
$$
Recordemos que, si encontramos dos valores de $\lambda$ reales diferentes, habremos probado que la transformación es diagonalizable. Para saber si esta ecuación cuadrática tiene soluciones reales y si estas son distintas o repetidas, debemos estudiar su discriminante:
$$
\begin{align}
\Delta &= B^{2} - 4 \cdot A \cdot C \\
&= -(a + c)^{2} - 4 \cdot 1 \cdot (ac - b^{2}) \\
&= (a^{2} + 2ac + c^{2}) - (4ac - 4b^{2}) \\
&= a^{2} + 2ac + c^{2} - 4ac + 4b^{2} \\
&= a^{2} - 2ac + c^{2} + 4b^{2} \\
&= (a - c)^{2} + 4b^{2}
\end{align}
$$
Como estamos trabajando en $\mathbb{R}^{2}$, $a$, $b$ y $c$ son coeficientes reales, lo que significa que $(a - c)^{2} \geq 0$ y $4b^{2} \geq 0$, lo que significa que $(a - c)^{2} + 4b^{2} \geq 0, \forall a, b, c \in \mathbb{R}$. Entonces, analicemos cada caso por separado:
- $(a - c)^{2} + 4b^{2} > 0$:
En este caso, si utilizamos la ecuación trigonométrica para determinar los valores de $\lambda$, obtendremos dos valores diferentes:
$$
\lambda_{1} = \frac{(a + c) + \sqrt{ (a - c)^{2} + 4b^{2} }}{2}, \lambda_{2} = \frac{(a + c) + \sqrt{ (a - c)^{2} + 4b^{2} }}{2}
$$
con $\lambda_{1} \neq \lambda_{2}$ ya que $(a - c)^{2} + 4b^{2} > 0$. De esta manera, obtuvimos 2 valores propios diferentes relacionados a una transformación lineal en un espacio de dimensión 2. Entonces, necesariamente encontraremos dos vectores propios linealmente independientes, formando una base de $\mathbb{R}^{2}$, y concluyendo en que la transformación lineal es diagonalizable.

- $(a - c)^{2} + 4b^{2} = 0$:
En este caso, como se trata de una suma de cuadrados, necesariamente tiene que ocurrir que:
$$
(a - c)^{2} = 0 \implies a - c = 0 \implies a = c \qquad \land \qquad 4b^{2} = 0 \implies b^{2} = 0 \implies b = 0
$$
De esta forma, la matriz asociada tendría la siguiente forma:
$$
A = \begin{pmatrix}
a & 0 \\
0 & a
\end{pmatrix}
$$
Como la matriz asociada a la transformación lineal es diagonal, deducimos que la transformación lineal es diagonalizable.

---
# 4 - Otros ejercicios de diagonalización
## Ejercicio 12
Primero, expresemos la transformación lineal:
$$
T(M) = M + aM^{t} = \begin{pmatrix}
x_{1} & x_{2} \\
x_{3} & x_{4}
\end{pmatrix} + \begin{pmatrix}
ax_{1} & ax_{3} \\
ax_{2} & ax_{4}
\end{pmatrix} = \begin{pmatrix}
(a + 1)x_{1} & x_{2} + ax_{3} \\
x_{3} + ax_{2} & (a + 1)x_{4}
\end{pmatrix}
$$
ACLARACIÓN:
No es necesario tomar este camino. Al fin y al cabo conocemos la transformación lineal, por lo que podemos aplicarla a los elementos de la base canónica y obtener la matriz asociada.
### Parte 1
Aplicamos la transformación lineal a los elementos de la base canónica:
$$
\begin{align}
&T\left( \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right) = \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} + \begin{pmatrix}
a & 0 \\
0 & 0
\end{pmatrix} = \begin{pmatrix}
1 + a & 0 \\
0 & 0
\end{pmatrix} \implies coord_{\mathcal{C}}\left( \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right) = (1 + a, 0, 0, 0) \\

&T\left( \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right) = \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} + \begin{pmatrix}
0 & 0 \\
a & 0
\end{pmatrix} = \begin{pmatrix}
0 & 1 \\
a & 0
\end{pmatrix} \implies coord_{\mathcal{C}}\left( \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right) = (0, 1, a, 0) \\

&T\left( \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right) = \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} + \begin{pmatrix}
0 & a \\
0 & 0
\end{pmatrix} = \begin{pmatrix}
0 & a \\
1 & 0
\end{pmatrix} \implies coord_{\mathcal{C}}\left( \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right) = (0, a, 1, 0) \\

&T\left( \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right) = \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} + \begin{pmatrix}
0 & 0 \\
0 & a
\end{pmatrix} = \begin{pmatrix}
0 & 0 \\
0 & 1 + a
\end{pmatrix} \implies coord_{\mathcal{C}}\left( \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right) = (0, 0, 0, 1 + a)
\end{align}
$$
Ahora, podemos expresar la matriz asociada en la base canónica a la transformación T:
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
1 + a & 0 & 0 & 0 \\
0 & 1 & a & 0 \\
0 & a & 1 & 0 \\
0 & 0 & 0 & 1 + a
\end{pmatrix}
$$

$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{cc}
1 + a - \lambda & 0 & 0 & 0 \\
0 & 1 - \lambda & a & 0 \\
0 & a & 1 - \lambda & 0 \\
0 & 0 & 0 & 1 + a - \lambda
\end{array} \right| \\
&= (1 + a - \lambda) \cdot (1 + a - \lambda) \cdot ((1 - \lambda)^{2} - a^{2}) \\
&= (1 + a - \lambda)^{2} \cdot ((1 - \lambda)^{2} - a^{2}) \\
&= (1 + a - \lambda)^{2} \cdot (1 - \lambda - a)(1 - \lambda + a) \\
&= (\lambda - (1 + a))^{2} \cdot (\lambda - (1 - a))(\lambda - (1 + a)) \\
&= (\lambda - (1 + a))^{3} \cdot (\lambda - (1 - a))
\end{align}
$$
Entonces, tenemos los siguientes valores propios:
- $\lambda - (1 + a) = 0 \implies \lambda = 1 + a$
$$
\begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & -a & a & 0 \\
0 & a & -a & 0 \\
0 & 0 & 0 & 0
\end{pmatrix} \implies \begin{pmatrix}
0 & 0 & 0 & 0 \\
0 & a & -a & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
ax_{2} - ax_{3} = 0
\end{cases}
$$

- $\lambda - (1 - a) = 0 \implies \lambda = 1 - a$
$$
\begin{pmatrix}
2a & 0 & 0 & 0 \\
0 & a & a & 0 \\
0 & a & a & 0 \\
0 & 0 & 0 & 2a
\end{pmatrix} \implies \begin{pmatrix}
2a & 0 & 0 & 0 \\
0 & a & a & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 2a
\end{pmatrix} \implies \begin{cases}
2ax_{1} = 0 \\
ax_{2} + ax_{3} = 0 \\
2ax_{4} = 0
\end{cases}
$$

Ahora, veamos que sucede para diferentes valores de $a$:
- $a = 0$
$$
S_{1 + a} = S_{1} = \left\{ \begin{pmatrix}
\alpha & \beta \\
\gamma & \delta
\end{pmatrix} : \alpha, \beta, \gamma, \delta \in \mathbb{R} \right\} = \left[ \left\{ \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\} \right]
$$
$$
S_{1 - a} = S_{1} = \left\{ \begin{pmatrix}
\alpha & \beta \\
\gamma & \delta
\end{pmatrix} : \alpha, \beta, \gamma, \delta \in \mathbb{R} \right\} = \left[ \left\{ \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\} \right]
$$

- $a \neq 0$
$$
\begin{cases}
ax_{2} - ax_{3} = 0
\end{cases} \implies x_{2} = x_{3} \land x_{1}, x_{4} \text{ son libres}
$$
$$
S_{1 + a} = \left\{ \begin{pmatrix}
\alpha & \beta \\
\beta & \gamma
\end{pmatrix} : \alpha, \beta, \gamma \in \mathbb{R} \right\} = \left[ \left\{ \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\} \right]
$$
$$
\begin{cases}
2ax_{1} = 0 \\
ax_{2} + ax_{3} = 0 \\
2ax_{4} = 0
\end{cases} \implies x_{1} = x_{4} = 0 \land x_{3} = -x_{2}
$$
$$
S_{1 - a} = \left\{ \begin{pmatrix}
0 & \alpha \\
-\alpha & 0
\end{pmatrix} : \alpha \in \mathbb{R} \right\} = \left[ \left\{ \begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix} \right\} \right]
$$
### Parte 2
Aquí, intentaremos invertir la matriz:
$$
\left(
\begin{array}{cccc|cccc}
1 + a & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\
0 & 1 & a & 0 & 0 & 1 & 0 & 0 \\
0 & a & 1 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 + a & 0 & 0 & 0 & 1
\end{array}
\right)
$$
Si $a = 0$, entonces la matriz ya está escalerizada, y por lo tanto $_{\mathcal{C}}(T)_{\mathcal{C}}$ es la identidad (siendo $_{\mathcal{C}}(T)_{\mathcal{C}} = (_{\mathcal{C}}(T)_{\mathcal{C}})^{-1}$).

Ahora, consideremos $a \neq 0$:
- $a = -1$
$$
\left(
\begin{array}{cccc|cccc}
0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\
0 & 1 & a & 0 & 0 & 1 & 0 & 0 \\
0 & a & 1 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 1
\end{array}
\right)
$$
No es invertible, ya que hay filas nulas.

- $a \not \in \{ -1, 0 \}$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{1 + a} & 0 & 0 & 0 \\
0 & 1 & a & 0 & 0 & 1 & 0 & 0 \\
0 & a & 1 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & \frac{1}{1 + a}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{1}{1 + a}F_{1} \\
&F_{4} \leftarrow \frac{1}{1 + a}F_{4}
\end{align}
$$
- $a = 1$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{2} & 0 & 0 & 0 \\
0 & 1 & 1 & 0 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & \frac{1}{2}
\end{array}
\right)
$$
Dos filas son múltiplos, por lo que es posible anular una de ellas. Por lo tanto, la matriz no es invertible.

- $a \not \in \{ -1, 0, 1 \}$

$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{1 + a} & 0 & 0 & 0 \\
0 & 1 & a & 0 & 0 & 1 & 0 & 0 \\
0 & 0 & 1 - a^{2} & 0 & 0 & -a & 1 & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & \frac{1}{1 + a}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - aF_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{1 + a} & 0 & 0 & 0 \\
0 & 1 & a & 0 & 0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 & -\frac{a}{1 - a^{2}} & \frac{1}{1 - a^{2}} & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & \frac{1}{1 + a}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{1 - a^{2}}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & \frac{1}{1 + a} & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & 0 & 1 + \frac{a^{2}}{1 - a^{2}} & -\frac{a}{1 - a^{2}} & 0 \\
0 & 0 & 1 & 0 & 0 & -\frac{a}{1 - a^{2}} & \frac{1}{1 - a^{2}} & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & \frac{1}{1 + a}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - aF_{3}
\end{align}
$$

Entonces, $T$ es invertible para $a \not \in \{ -1, 1 \}$, y su inversa es:
$$
(_{\mathcal{C}}(T)_{\mathcal{C}})^{-1} = \begin{pmatrix}
\frac{1}{1 + a} & 0 & 0 & 0 \\
0 & \frac{1}{1 - a^{2}} & -\frac{a}{1 - a^{2}} & 0 \\
0 & -\frac{a}{1 - a^{2}} & \frac{1}{1 - a^{2}} & 0 \\
0 & 0 & 0 & \frac{1}{1 + a}
\end{pmatrix}
$$
En el caso $a = 0$, su inversa es la identidad.
### Parte 3
- $a = 0$
Encontramos una cantidad suficiente de vectores propios LI para conformar una base del espacio vectorial correspondiente. Entonces, si $a = 0$, $T$ es diagonalizable.

- $a \neq 0$
Nuevamente, determinamos una cantidad suficiente de vectores propios LI para conformar una base del espacio vectorial correspondiente. Entonces, si $a \neq 0$, $T$ es diagonalizable.

En definitiva, $T$ es diagonalizable $\forall a \in \mathbb{R}$.

### Parte 4
Ahora consideramos $a = 1$.

Como sabemos que $T$ es diagonalizable $\forall a \in \mathbb{R}$, también lo es para $a = 1$. 

Entonces, podemos considerar la siguiente base de vectores propios:
$$
\left\{ \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right\}
$$

---
## Ejercicio 13
### Parte 1
Aplicamos la transformación a cada uno de los elementos de la base canónica de $\mathcal{P}_{2}(\mathbb{R})$: $\{ 1, x, x^{2} \}$
$$
\begin{align}
&T(1) = 2 \cdot (1)' + 1 = 2 \cdot 0 + 1 = 1 \implies coord_{\mathcal{C}}(T(1)) = (1, 0, 0) \\
&T(x) = 2 \cdot (x)' + x = 2 + x \implies coord_{\mathcal{C}}(T(x)) = (2, 1, 0) \\
&T(x^{2}) = 2 \cdot (x^{2})' + x^{2} = 4x + x^{2} \implies coord_{\mathcal{C}}(T(x^{2})) = (0, 4, 1)
\end{align}
$$
Entonces, podemos expresar la matriz asociada $_{\mathcal{C}}(T)_{\mathcal{C}}$:
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 4 \\
0 & 0 & 1
\end{pmatrix}
$$
Ahora, desarrollamos el determinante de $T - \lambda \cdot \mathbb{I}$:
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
1 - \lambda & 2 & 0 \\
0 & 1 - \lambda & 4 \\
0 & 0 & 1 - \lambda
\end{array} \right| \\
&= (1 - \lambda)^{3}
\end{align}
$$
En este caso, la transformación tiene asociada únicamente un valor propio: $1 - \lambda = 0 \implies \lambda = 1$:

Determinamos el subespacio propio correspondiente:
$$
\begin{pmatrix}
0 & 2 & 0 \\
0 & 0 & 4 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{pmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
b = 0 \\
c = 0
\end{cases} \implies a \text{ es libre}
$$
$$
S_{1} = \{ a : a \in \mathbb{R} \} = [\{ 1 \}]
$$

De esta forma, solo obtuvimos un vector propio.

### Parte 2
En conclusión, $T$ no es diagonalizable, ya que deberíamos encontrar al menos tres vectores propios LI para llegar a dicha conclusión (una base de vectores propios).

---
## Ejercicio 14
Determinamos las coordenadas en la base canónica de las imágenes de los elementos de la base canónica:
$$
\begin{align}
&T\left( \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right) = \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} = \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix} = \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \implies coord_{\mathcal{C}}\left( \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} \right) = (0, 1, 0, 0) \\
&T\left( \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right) = \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix} \implies coord_{\mathcal{C}}\left( \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix} \right) = (0, 0, 0, 0) \\
&T\left( \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \right) = \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
0 & 0 \\
1 & 0
\end{pmatrix} = \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} - \begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix} = \begin{pmatrix}
-1 & 0 \\
0 & 1
\end{pmatrix} \implies coord_{\mathcal{C}}\left( \begin{pmatrix}
-1 & 0 \\
0 & 1
\end{pmatrix} \right) = (-1, 0, 0, 1) \\
&T\left( \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \right) = \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} \cdot \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} - \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \cdot \begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix} = \begin{pmatrix}
0 & 0 \\
0 & 0
\end{pmatrix} - \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} = \begin{pmatrix}
0 & -1 \\
0 & 0
\end{pmatrix} \implies coord_{\mathcal{C}}\left( \begin{pmatrix}
0 & -1 \\
0 & 0
\end{pmatrix} \right) = (0, -1, 0, 0)
\end{align}
$$

Entonces, expresamos la matriz asociada a la transformación en la base canónica:
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
0 & 0 & -1 & 0 \\
1 & 0 & 0 & -1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0
\end{pmatrix}
$$
Entonces, desarrollamos el determinante $T - \lambda \cdot \mathbb{I}$:
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{cccc}
-\lambda & 0 & -1 & 0 \\
1 & -\lambda & 0 & -1 \\
0 & 0 & -\lambda & 0 \\
0 & 0 & 1 & -\lambda
\end{array} \right| \\
&= (-\lambda)^{4}
\end{align}
$$
Entonces, el único valor propio es:
- $\lambda = 0$
$$
\begin{pmatrix}
0 & 0 & -1 & 0 \\
1 & 0 & 0 & -1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0
\end{pmatrix} \implies \begin{pmatrix}
1 & 0 & 0 & -1 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{pmatrix} \begin{cases}
x_{1} - x_{4} = 0 \\
x_{3} = 0
\end{cases} \implies x_{4} = x_{1} \land x_{2} \text{ es libre}
$$
$$
S_{0} = \left\{ \begin{pmatrix}
\alpha & \beta \\
0 & \alpha
\end{pmatrix} : \alpha, \beta \in \mathbb{R} \right\} = \left\{ \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}, \begin{pmatrix}
0 & 1 \\
0 & 0
\end{pmatrix} \right\}
$$

En este caso, obtuvimos únicamente dos vectores propios linealmente independientes. Por lo tanto, la transformación lineal no es diagonalizable.

---

## Ejercicio 15
### Parte 1
Conocemos como se transforman los elementos de la base canónica, por lo que podemos determinar sus coordenadas:
$$
\begin{align}
&T(1) = 4 + 4x^{2} \implies coord_{\mathcal{C}}(T(1)) = (4, 0, 4) \\
&T(x) = -1 + 2x - 3x^{2} \implies coord_{\mathcal{C}}(T(x)) = (-1, 2, -3) \\
&T(x^{2}) = b \implies coord_{\mathcal{C}}(T(x^{2})) = (b, 0, 0)
\end{align}
$$
Ahora, expresamos la matriz asociada:
$$
_{\mathcal{C}}(T)_{\mathcal{C}} = \begin{pmatrix}
4 & -1 & b \\
0 & 2 & 0 \\
4 & -3 & 0
\end{pmatrix}
$$
Entonces, podemos calcular el determinante de $T - \lambda \cdot \mathbb{I}$:
$$
\begin{align}
\det(T - \lambda \cdot \mathbb{I}) &= \left| \begin{array}{ccc}
4 - \lambda & -1 & b \\
0 & 2 - \lambda & 0 \\
4 & -3 & -\lambda
\end{array} \right| \\
&= (4 - \lambda) \cdot (\lambda - 2) \cdot \lambda + 4 \cdot (\lambda - 2) \cdot b \\
&= (\lambda - 2) \cdot ((4 - \lambda) \cdot \lambda + 4b) \\
&= (\lambda - 2) \cdot (-\lambda^{2} + 4\lambda + 4b)
\end{align}
$$
Buscamos las raíces del factor cuadrático:
$$
\begin{align}
\lambda &= \frac{-4 \pm \sqrt{ 4^{2} - 4 \cdot (-1) \cdot 4b }}{2 \cdot (-1)} \\
&= \frac{-4 \pm \sqrt{ 16 + 16b }}{-2} \\
&= \frac{-4 \pm 4\sqrt{ 1 + b }}{-2} \\
&= 2 \mp 2\sqrt{ 1 + b }
\end{align}
$$
Entonces, podemos simplificar aún más el determinante:
$$
(\lambda - 2) \cdot (-\lambda^{2} + 4\lambda + 4b) = -(\lambda - 2) \cdot (\lambda - (2 + 2\sqrt{ 1 + b })) \cdot (\lambda - (2 - 2\sqrt{ 1 + b }))
$$

Determinamos los valores de $\lambda$:
- $\lambda - 2 = 0 \implies \lambda = 2$
$$
\begin{pmatrix}
2 & -1 & b \\
0 & 0 & 0 \\
4 & -3 & -2
\end{pmatrix} \implies \begin{pmatrix}
1 & 0 & 1 + \frac{3}{2}b \\
0 & 1 & 2 + 2b \\
0 & 0 & 0
\end{pmatrix} \implies \begin{cases}
x_{1} + \left( 1 + \frac{3}{2}b \right)x_{3} = 0 \\
x_{2} + (2 + 2b)x_{3} = 0
\end{cases}
$$

- $\lambda - (2 + 2\sqrt{ 1 + b }) = 0 \implies \lambda = 2 + 2\sqrt{ 1 + b }$
$$
\begin{pmatrix}
2 - 2\sqrt{ 1 + b } & -1 & b \\
0 & -2\sqrt{ 1 + b } & 0 \\
4 & -3 & -2 - 2\sqrt{ 1 + b }
\end{pmatrix} \implies \begin{cases}
(2 - 2\sqrt{ 1 + b })x_{1} - x_{2} + bx_{3} = 0 \\
-2\sqrt{ 1 + b }x_{2} = 0 \\
4x_{1} - 3x_{2} + (-2 - 2\sqrt{ 1 + b })x_{3} = 0
\end{cases}
$$

- $\lambda - (2 - 2\sqrt{ 1 + b }) = 0 \implies \lambda = 2 - 2\sqrt{ 1 + b }$
$$
\begin{pmatrix}
2 + 2\sqrt{ 1 + b } & -1 & b \\
0 & 2\sqrt{ 1 + b } & 0 \\
4 & -3 & -2 + 2\sqrt{ 1 + b }
\end{pmatrix} \implies \begin{cases}
(2 + 2\sqrt{ 1 + b })x_{1} - x_{2} + bx_{3} = 0 \\
2\sqrt{ 1 + b }x_{2} = 0 \\
4x_{1} - 3x_{2} + (-2 + 2\sqrt{ 1 + b })x_{3} = 0
\end{cases}
$$

Ahora, estudiemos cada uno de los casos tomando como referencia el término $\sqrt{ 1 + b }$:

- $b < -1$
Bajo dicha condición, todas las raíces que contienen el término $1 + b$ resultan ser complejas, y como estamos trabajando en $\mathbb{R}$, la transformación no es diagonalizable.

- $b = -1$
$$
\begin{cases}
x_{1} + \left( 1 + \frac{3}{2}b \right)x_{3} = 0 \\
x_{2} + (2 + 2b)x_{3} = 0
\end{cases} \implies \begin{cases}
x_{1} - \frac{1}{2}x_{3} = 0 \\
x_{2} = 0
\end{cases} \implies x_{1} = \frac{1}{2}x_{3}
$$
$$
S_{2} = \left\{ \frac{1}{2}\alpha + \alpha x^{2} : \alpha \in \mathbb{R} \right\} = \left[ \left\{ \frac{1}{2} + x^{2} \right\} \right]
$$
$$
\begin{cases}
(2 - 2\sqrt{ 1 + b })x_{1} - x_{2} + bx_{3} = 0 \\
-2\sqrt{ 1 + b }x_{2} = 0 \\
4x_{1} - 3x_{2} + (-2 - 2\sqrt{ 1 + b })x_{3} = 0
\end{cases} \implies \begin{cases}
2x_{1} - x_{2} - x_{3} = 0 \\
4x_{1} - 3x_{2} - 2x_{3} = 0
\end{cases} \implies x_{2} = 0 \land x_{3} = 2x_{1}
$$
$$
S_{2} = \left\{ \alpha + 2\alpha x^{2} : \alpha \in \mathbb{R} \right\} = \left[ \left\{ 1 + 2x^{2} \right\} \right]
$$
$$
\begin{cases}
(2 + 2\sqrt{ 1 + b })x_{1} - x_{2} + bx_{3} = 0 \\
2\sqrt{ 1 + b }x_{2} = 0 \\
4x_{1} - 3x_{2} + (-2 + 2\sqrt{ 1 + b })x_{3} = 0
\end{cases} \implies \begin{cases}
2x_{1} - x_{2} - x_{3} = 0 \\
4x_{1} - 3x_{2} - 2x_{3} = 0
\end{cases} \implies x_{2} = 0 \land x_{3} = 2x_{1}
$$
$$
S_{2} = \left\{ \alpha + 2\alpha x^{2} : \alpha \in \mathbb{R} \right\} = \left[ \left\{ 1 + 2x^{2} \right\} \right]
$$
En este caso, no obtuvimos una base de vectores propios, puesto que los tres vectores obtenidos son múltiplos entre si. Por esta razón, $T$ no es diagonalizable para $b = -1$.

- $b > -1$
$$
\begin{cases}
x_{1} + \left( 1 + \frac{3}{2}b \right)x_{3} = 0 \\
x_{2} + (2 + 2b)x_{3} = 0
\end{cases} \implies x_{1} = -\left( 1 + \frac{3}{2}b \right)x_{3} \land x_{2} = -(2 + 2b)x_{3}
$$
$$
S_{2} = \left\{ -\left( 1 + \frac{3}{2}b \right) \alpha - (2 + 2b)\alpha x + \alpha x^{2} : \alpha \in \mathbb{R} \right\} = \left[ \left\{ -\left( 1 + \frac{3}{2}b \right) - (2 + 2b)x + x^{2} \right\} \right]
$$
$$
\begin{cases}
(2 - 2\sqrt{ 1 + b })x_{1} - x_{2} + bx_{3} = 0 \\
-2\sqrt{ 1 + b }x_{2} = 0 \\
4x_{1} - 3x_{2} + (-2 - 2\sqrt{ 1 + b })x_{3} = 0
\end{cases} \implies x_{2} = 0 \land x_{1} = \left( \frac{1}{2} + \frac{1}{2}\sqrt{ 1 + b } \right)x_{3}
$$
$$
S_{2} = \left\{ \left( \frac{1}{2} + \frac{1}{2}\sqrt{ 1 + b } \right) \alpha + \alpha x^{2} : \alpha \in \mathbb{R} \right\} = \left[ \left\{ \left( \frac{1}{2} + \frac{1}{2}\sqrt{ 1 + b } \right) + x^{2} \right\} \right]
$$
$$
\begin{cases}
(2 + 2\sqrt{ 1 + b })x_{1} - x_{2} + bx_{3} = 0 \\
2\sqrt{ 1 + b }x_{2} = 0 \\
4x_{1} - 3x_{2} + (-2 + 2\sqrt{ 1 + b })x_{3} = 0
\end{cases} \implies x_{2} = 0 \land x_{1} = \left( \frac{1}{2} - \frac{1}{2}\sqrt{ 1 + b } \right)x_{3}
$$
$$
S_{2} = \left\{ \left( \frac{1}{2} - \frac{1}{2}\sqrt{ 1 + b } \right) \alpha + \alpha x^{2} : \alpha \in \mathbb{R} \right\} = \left[ \left\{ \left( \frac{1}{2} - \frac{1}{2}\sqrt{ 1 + b } \right) + x^{2} \right\} \right]
$$
En el caso particular $b > -1$, obtuvimos tres vectores propios linealmente independientes $\left\{ -\left( 1 + \frac{3}{2}b \right) - (2 + 2b)x + x^{2}, \left( \frac{1}{2} + \frac{1}{2}\sqrt{ 1 + b } \right) + x^{2}, \left( \frac{1}{2} - \frac{1}{2}\sqrt{ 1 + b } \right) + x^{2} \right\}$, y siendo que estamos trabajando en un espacio de dimensión 3. Confirmamos que la transformación es diagonalizable si se cumple la condición.

### Parte 2
Determinamos los vectores de la base para $b = 3$:
$$
\left\{ -11 - 16x + 2x^{2}, 3 + 2x^{2}, -1 + 2x^{2} \right\}
$$
Ahora, en base a las coordenadas de los vectores propios anteriores, expresamos la matriz:
$$
P = \begin{pmatrix}
-11 & 3 & -1 \\
-16 & 0 & 0 \\
2 & 2 & 2
\end{pmatrix}
$$
Para hallar la forma diagonal, tenemos que encontrar $P^{-1}$:
$$
\left( \begin{array}{ccc|ccc}
-11 & 3 & -1 & 1 & 0 & 0 \\
-16 & 0 & 0 & 0 & 1 & 0 \\
2 & 2 & 2 & 0 & 0 & 1
\end{array} \right)
$$
$$
\left( \begin{array}{ccc|ccc}
-11 & 3 & -1 & 1 & 0 & 0 \\
1 & 0 & 0 & 0 & -\frac{1}{16} & 0 \\
1 & 1 & 1 & 0 & 0 & \frac{1}{2}
\end{array} \right)
\begin{align}
&F_{2} \leftarrow -\frac{1}{16}F_{2} \\
&F_{3} \leftarrow \frac{1}{2}F_{2}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
0 & 3 & -1 & 1 & -\frac{11}{16} & 0 \\
1 & 0 & 0 & 0 & -\frac{1}{16} & 0 \\
0 & 1 & 1 & 0 & \frac{1}{16} & \frac{1}{2}
\end{array} \right)
\begin{align}
&F_{1} \leftarrow F_{1} + 11F_{2} \\
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
0 & 4 & 0 & 1 & -\frac{10}{16} & \frac{1}{2} \\
1 & 0 & 0 & 0 & -\frac{1}{16} & 0 \\
0 & 1 & 1 & 0 & \frac{1}{16} & \frac{1}{2}
\end{array} \right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
0 & 1 & 0 & \frac{1}{4} & -\frac{10}{64} & \frac{1}{8} \\
1 & 0 & 0 & 0 & -\frac{1}{16} & 0 \\
0 & 1 & 1 & 0 & \frac{1}{16} & \frac{1}{2}
\end{array} \right)
\begin{align}
&F_{1} \leftarrow \frac{1}{4}F_{1}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
0 & 1 & 0 & \frac{1}{4} & -\frac{10}{64} & \frac{1}{8} \\
1 & 0 & 0 & 0 & -\frac{1}{16} & 0 \\
0 & 0 & 1 & -\frac{1}{4} & \frac{14}{64} & \frac{3}{8}
\end{array} \right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left( \begin{array}{ccc|ccc}
1 & 0 & 0 & 0 & -\frac{1}{16} & 0 \\
0 & 1 & 0 & \frac{1}{4} & -\frac{10}{64} & \frac{1}{8} \\
0 & 0 & 1 & -\frac{1}{4} & \frac{14}{64} & \frac{3}{8}
\end{array} \right)
\begin{align}
&F_{1} \leftrightarrow F_{2}
\end{align}
$$
De esta forma:
$$
P^{-1} = \begin{pmatrix}
0 & -\frac{1}{16} & 0 \\
\frac{1}{4} & -\frac{5}{32} & \frac{1}{8} \\
-\frac{1}{4} & \frac{7}{32} & \frac{3}{8}
\end{pmatrix}
$$

Ahora, resta desarrollar el siguiente producto:
$$
T = \begin{pmatrix}
4 & -1 & 3 \\
0 & 2 & 0 \\
4 & -3 & 0
\end{pmatrix}
$$
$$
D = P^{-1} \cdot (T \cdot P) = \begin{pmatrix}
0 & -\frac{1}{16} & 0 \\
\frac{1}{4} & -\frac{5}{32} & \frac{1}{8} \\
-\frac{1}{4} & \frac{7}{32} & \frac{3}{8}
\end{pmatrix} \cdot \left( \begin{pmatrix}
4 & -1 & 3 \\
0 & 2 & 0 \\
4 & -3 & 0
\end{pmatrix} \cdot \begin{pmatrix}
-11 & 3 & -1 \\
-16 & 0 & 0 \\
2 & 2 & 2
\end{pmatrix} \right)
$$

ACLARACIÓN:
En lugar de hacer todo el desarrollo anterior para determinar $D$, podemos aprovechar uno de los teoremas mencionados en el curso, el cual establece que toda transformación lineal diagonalizable tiene una matriz asociada diagonal, cuya diagonal está conformada por los valores propios asociados a la transformación.

Dicho lo anterior, podemos definir $D$ conociendo los valores propios de la transformación $T$:
- $\lambda = 2$
- $\lambda = 2 + 2\sqrt{ 1 + b } = 2 + 2\sqrt{ 1 + 3 } = 2 + 4 = 6$
- $\lambda = 2 - 2\sqrt{ 1 + b } = 2 - 2\sqrt{ 1 + 3 } = 2 - 4 = -2$

En conclusión, expresamos la matriz $D$:
$$
D = \begin{pmatrix}
2 & 0 & 0 \\
0 & 6 & 0 \\
0 & 0 & -2
\end{pmatrix}
$$

---
## Ejercicio 16
### Parte 1
Si $T = T^{3}$, entonces se cumple que $\det(T) = \det(T^{3}) = \det(T)^{3}$.

Como estamos en un $\mathbb{R}$ espacio vectorial, $\lambda_{1}, \lambda_{2}, \lambda_{3} \in \mathbb{R}$. Por lo tanto, tenemos que encontrar valores reales que verifiquen $\lambda_{i} = \lambda_{i}^{3} \Longleftrightarrow \lambda_{i} = \sqrt[3]{ \lambda_{i} }$.

Solo existen tres valores reales que verifican dicha igualdad:
$$
\begin{align}
\lambda_{1} = -1 \\
\lambda_{2} = 0 \\
\lambda_{3} = 1
\end{align}
$$

### Parte 2
1. $\frac{1}{2}T^{2}(v) - \frac{1}{2}T(v) \in S_{\lambda_{1}}$
$$
\begin{align}
&\frac{1}{2} \cdot T^{2}(v) - \frac{1}{2} \cdot T(v) \\
&\frac{1}{2} \cdot T(T(v)) - \frac{1}{2} \cdot T(v) \\
&\frac{1}{2} \cdot T(\lambda v) - \frac{1}{2} \cdot T(v) \\
&\frac{1}{2} \cdot \lambda T(v) - \frac{1}{2} \cdot T(v) \\
&\frac{1}{2} \cdot \lambda \cdot \lambda v - \frac{1}{2} \cdot \lambda v \\
&\frac{1}{2} \cdot \lambda^{2} v - \frac{1}{2} \cdot \lambda v
\end{align}
$$
Entonces, existen tres posibilidades:
- $\lambda = \lambda_{1} = -1$
$$
\frac{1}{2} \cdot v + \frac{1}{2} \cdot v = v
$$

- $\lambda = \lambda_{2} = 0$
$$
\frac{1}{2} \cdot \vec{0} - \frac{1}{2} \cdot \vec{0} = \vec{0}
$$

- $\lambda = \lambda_{3} = 1$
$$
\frac{1}{2} \cdot v - \frac{1}{2} \cdot v = \vec{0}
$$

Como vemos, con el único valor propio que no se anula el resultado es con $\lambda_{1} = -1$. Como el vector nulo pertenece a todos los subespacios (no es un vector propio), el que se anule la ecuación es un indicio de que la expresión no pertenece a ese subespacio. Por lo tanto, $\frac{1}{2} \cdot T^{2}(v) - \frac{1}{2} \cdot T(v) \in S_{\lambda_{1}}$

2. $v - T^{2}(v) \in S_{\lambda_{2}}$
$$
\begin{align}
&v - T^{2}(v) \\
&v - T(T(v)) \\
&v - T(\lambda v) \\
&v - \lambda \cdot \lambda v \\
&v - \lambda^{2} v
\end{align}
$$
Analizamos cada caso:
- $\lambda = \lambda_{1} = -1$
$$
v - v = 0
$$

- $\lambda = \lambda_{2} = 0$
$$
v - 0 \cdot v = v
$$

- $\lambda = \lambda_{3} = 1$
$$
v - v = \vec{0}
$$

Misma justificación que en caso anterior. En conclusión, $v - T^{2}(v) \in S_{\lambda_{2}}$

3. $\frac{1}{2}T(v) + \frac{1}{2}T^{2}(v) \in S_{\lambda_{3}}$
$$
\begin{align}
&\frac{1}{2} \cdot T(v) + \frac{1}{2} \cdot T^{2}(v) \\
&\frac{1}{2} \cdot \lambda v + \frac{1}{2} \cdot \lambda^{2} v
\end{align}
$$
Analizamos cada caso:
- $\lambda = \lambda_{1} = -1$
$$
-\frac{1}{2} \cdot v + \frac{1}{2} \cdot v = \vec{0}
$$

- $\lambda = \lambda_{2} = 0$
$$
\frac{1}{2} \cdot 0 \cdot v + \frac{1}{2} \cdot 0 \cdot v = \vec{0}
$$

- $\lambda = \lambda_{3} = 1$
$$
\frac{1}{2} \cdot v + \frac{1}{2} \cdot v = v
$$

Misma justificación que en caso anterior. En conclusión, $\frac{1}{2} \cdot T(v) + \frac{1}{2} \cdot T^{2}(v) \in S_{\lambda_{3}}$.

### Parte 3
Tenemos que probar que $V = S_{\lambda_{1}} \oplus S_{\lambda_{2}} \oplus S_{\lambda_{3}}$.

Sabemos que existen tres subespacios propios $S_{\lambda_{1}}, S_{\lambda_{2}}, S_{\lambda_{3}}$. Al ser subespacios propios asociados a valores propios diferentes, necesariamente son disjuntos: $S_{\lambda_{1}} \cap S_{\lambda_{2}} \cap S_{\lambda_{3}} = \emptyset$.

De esta manera, sabemos que la suma de los subespacios es directa.

Ahora, tenemos que verificar que la suma de dichos subespacios da como resultado el espacio $V$. Para empezar, consideremos que $S_{\lambda_{1}}, S_{\lambda_{2}}, S_{\lambda_{3}} \subseteq V$. De esta forma, los subespacios están compuestos por vectores de $V$, por lo que lo mismo aplica para sus bases.

En la parte anterior, probamos que
1. $\frac{1}{2} \cdot T^{2}(v) - \frac{1}{2} \cdot T(v) \in S_{\lambda_{1}}$
2. $v - T^{2}(v) \in S_{\lambda_{2}}$
3. $\frac{1}{2}T(v) + \frac{1}{2}T^{2}(v) \in S_{\lambda_{3}}$

Si combinamos los resultados anteriores, obtendremos un vector perteneciente a $V$:
$$
\left( \frac{1}{2} \cdot T^{2}(v) - \cancel{ \frac{1}{2} \cdot T(v) } \right) + (v - T^{2}(v)) + \left( \cancel{ \frac{1}{2}T(v) } + \frac{1}{2}T^{2}(v) \right) = v - \cancel{ T^{2}(v) } + \cancel{ T^{2}(v) } = v
$$
Como obtuvimos un vector $v \in V$ genérico, esto significa que podemos obtener cualquier vector perteneciente a $V$ a partir de combinaciones lineales de las expresiones anteriores.

De esta forma, no solo la suma de los subespacios vectoriales es directa, sino que también resulta en el espacio $V$, ya que podemos construir cualquier vector $v \in V$ a partir de la combinación lineal de vectores pertenecientes a $S_{\lambda_{1}}, S_{\lambda_{2}}, S_{\lambda_{3}}$.

En conclusión, probamos que $V = S_{\lambda_{1}} \oplus S_{\lambda_{2}} \oplus S_{\lambda_{3}}$.

### Parte 4
Acabamos de probar que $V = S_{\lambda_{1}} \oplus S_{\lambda_{2}} \oplus S_{\lambda_{3}}$. Ahora, en base a este resultado, probaremos que $T$ es diagonalizable.

Sea $\mathcal{B}$ base de $V$, lo que significa que $[\mathcal{B}] = V = S_{\lambda_{1}} \oplus S_{\lambda_{2}} \oplus S_{\lambda_{3}}$:
$$
\mathcal{B} = \{ v_{1}, v_{2}, \dots, v_{n} \}
$$
Reordenamos los vectores de $\mathcal{B}$ tal que los agrupemos por subespacio vectorial $S_{\lambda_{1}}, S_{\lambda_{2}}, S_{\lambda_{3}}$. De esta forma:
- Los vectores $1$ hasta $a$ pertenecen a $S_{\lambda_{1}}$
- Los vectores $a + 1$ hasta $b$ pertenecen a $S_{\lambda_{2}}$
- Los vectores $b + 1$ hasta $n$ pertenecen a $S_{\lambda_{3}}$
$$
\mathcal{B} = \{ \underbrace{ v_{1}, \dots, v_{a} }_{ \mathcal{B_{1}} }, \underbrace{ v_{a + 1}, \dots, v_{b} }_{ \mathcal{B_{2}} }, \underbrace{ v_{b + 1}, \dots, v_{n} }_{ \mathcal{B_{3}} } \}
$$
De esta manera:
- $\mathcal{B_{1}}$ es base de $S_{\lambda_{1}}$
- $\mathcal{B_{2}}$ es base de $S_{\lambda_{2}}$
- $\mathcal{B_{3}}$ es base de $S_{\lambda_{3}}$

Pero entonces, $\mathcal{B_{1}}$, $\mathcal{B_{2}}$ y $\mathcal{B_{3}}$ están compuestas por vectores propios, y como su unión conforma $\mathcal{B}$ base de $V$, entonces $\mathcal{B}$ también está compuesta por vectores propios. Es así que encontramos una base de $V$ compuesta por vectores propios, y aplicando el teorema que indica que una transformación lineal es diagonalizable sí y solo si existe una base conformada por vectores propios, concluimos en que $T$ es diagonalizable.

### Parte 5
Al tener solo tres valores propios y ser $V$ de dimensión 4, significa que en la diagonal uno de los valores propios se tiene que repetir.
Entonces, si $dim(V) = 4$, tenemos 3 tipos diferentes de matrices (sin considerar el orden de los valores propios en la diagonal, únicamente cuantas veces se repite cada uno).
Como tenemos 4 valores, donde dos son iguales, tenemos que contar la cantidad de permutaciones con repetición que podemos hacer para dos valores iguales, por ejemplo:
$$
\begin{align}
\{ -1, -1, 0, 1 \} \\
\{ -1, -1, 1, 0 \} \\
\{ -1, 0, -1, 1 \} \\
\{ -1, 1, -1, 0 \} \\
\{ -1, 0, 1, -1 \} \\
\{ -1, 1, 0, -1 \} \\
\{ 0, -1, 1, -1 \} \\
\{ 1, -1, 0, -1 \} \\
\{ 1, 0, -1, -1 \} \\
\{ 0, 1, -1, -1 \} \\
\{ 0, -1, -1, 1 \} \\
\{ 1, -1, -1, 0 \}
\end{align}
$$
Por ejemplo, las anteriores son todas las permutaciones con repetición si consideramos que el valor propio repetido es el $\lambda_{3} = -1$. Por lo tanto, tenemos que multiplicar por 3 para determinar las permutaciones con repetición totales sea cual sea el elemento que se repite:
$$
12 \cdot 3 = 36
$$

En conclusión, existen $36$ matrices diagonales diferentes de tamaño $4 \times 4$ que contienen en su diagonal los elementos $\{ -1, 0, 1 \}$ en diferente orden.