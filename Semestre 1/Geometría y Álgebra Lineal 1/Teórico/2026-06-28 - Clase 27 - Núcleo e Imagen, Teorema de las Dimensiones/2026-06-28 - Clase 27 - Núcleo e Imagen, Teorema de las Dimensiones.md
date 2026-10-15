# Espacios vectoriales
Esta es la clase final del curso, y abordaremos el tema de núcleo e imagen de una transformación lineal:

## Núcleo e Imagen

#Definición 
> [!Núcleo e Imagen - Definición]
> Sean
> - $V, W$ espacios vectoriales
> - $T : V \to W$
> 
> Se definen
> - El núcleo de $T$ por $\mathrm{Ker}(T) = \{ v \in V : T(v) = 0_{W} \}$
> - La imagen de $T$ por $\mathrm{Im}(T) = T(V) = \{ T(v) : v \in V \}$

De esta forma, el núcleo (kernel) contiene a todos los vectores del espacio de partida que se anulan al aplicarles la transformación lineal $T$. O sea, todos los vectores de $V$ que se transforman en el vector nulo en $W$ luego de aplicarles la transformación correspondiente. El núcleo es un subconjunto de $V$ (la partida).

La imagen de $T$ es la imagen del espacio $V$ por $T$: todos los vectores generados a partir de vectores del espacio vectorial de entrada $V$. La imagen es un subconjunto de $W$ (la llegada).

Además de subconjuntos, ambos son subespacios vectoriales (son estables por suma de vectores, y por producto de un escalar por un vector).

### Proposición

#Proposición 
> [!Proposición]
> Para toda transformación lineal $T : V \to W$
> - El núcleo $\mathrm{Ker}(T) \underset{sev} \subset V$ es un subespacio vectorial de $V$.
> - La imagen $\mathrm{Im}(T) \underset{sev} \subset W$ es un subespacio vectorial de $W$.

Ahora, pasaremos a ver ejemplos para calcular y determinar dichos conjuntos para una transformación lineal dada:

### Ejemplo 1
Sea $T : \mathbb{R}^{4} \to \mathbb{R}^{3}$ definida por:
$$
T(x, y, z, t) = (x - y + z + t, x + 2z - t, x + y + 3z - 3t)
$$

Queremos:
1. Hallar una base de $\mathrm{Ker}(T) \underset{sev} \subset V$.
2. Hallar una base de $\mathrm{Im}(T) \underset{sev} \subset W$.

Antes de hallar las bases, tenemos que determinar el núcleo y la imagen propiamente dicho:
1. Determinación del núcleo
$$
(x, y, z, t) \in \mathrm{Ker}(T) \Longleftrightarrow T(x, y, z, t) = (0, 0, 0)
$$
Entonces, tenemos que resolver un sistema lineal:
$$
\begin{cases}
x - y + z + t = 0 \\
x + 2z - t = 0 \\
x + y + 3z - 3t = 0
\end{cases}
$$
$$
\left(
\begin{array}{cccc|c}
1 & -1 & 1 & 1 & 0 \\
1 & 0 & 2 & -1 & 0 \\
1 & 1 & 3 & -3 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
1 & -1 & 1 & 1 & 0 \\
0 & 1 & 1 & -2 & 0 \\
0 & 2 & 2 & -4 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & -1 & 1 & 1 & 0 \\
0 & 1 & 1 & -2 & 0 \\
0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - 2F_{2}
\end{align}
$$
Hasta aquí tenemos la forma escalerizada, y al anularse una fila, sabemos que vamos a trabajar con parámetros.
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 2 & -1 & 0 \\
0 & 1 & 1 & -2 & 0 \\
0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2}
\end{align}
$$
Entonces, podemos determinar las condiciones para que un vector genérico pertenezca al núcleo.
$$
\begin{align}
(x, y, z, t) \in \mathrm{Ker}(T) &\Longleftrightarrow \begin{cases}
x + 2z - t = 0 \\
y + z - 2t = 0 \\
\cancel{ 0 = 0 }
\end{cases} \\
&\Longleftrightarrow \begin{cases}
x = -2x + t \\
y = -z + 2t
\end{cases}
\end{align}
$$
De esta forma:
$$
\begin{align}
\mathrm{Ker}(T) &= \{ (-2z + t, -z + 2t, z, t) : z, t \in \mathbb{R} \} \\
&= \{ z(-2, -1, 1, 0) + t(1, 2, 0, 1) : z, t \in \mathbb{R} \}
\end{align}
$$
Se observa que el conjunto $\{ (-2, -1, 1, 0), (1, 2, 0, 1) \}$
- es un generador de $\mathrm{Ker}(T)$
- es LI.
Por lo tanto, es una base de $\mathrm{Ker}(T)$.

Con esto, finalizamos el análisis del núcleo. Pasamos a estudiar la imagen:
2. Determinación de la imagen
$$
\begin{align}
(\alpha, \beta, \gamma) \in \mathrm{Im}(T) &\Longleftrightarrow \exists x, y, z, t \in \mathbb{R}, T(x, y, z, t) = (\alpha, \beta, \gamma) \\
&\Longleftrightarrow \begin{cases}
x - y + z + t = \alpha \\
x + 2z - t = \beta \\
x + y + 3z - 3t = \gamma
\end{cases}
\end{align}
$$
Entonces, definimos un nuevo sistema, y en caso de ser compatible, aseguramos que el elemento pertenece a $\mathrm{Im}(T)$. No es necesario resolver el sistema, simplemente tenemos que determinar si es compatible y cuando se da dicho caso.
$$
\left(
\begin{array}{cccc|c}
1 & -1 & 1 & 1 & \alpha \\
1 & 0 & 2 & -1 & \beta \\
1 & 1 & 3 & -3 & \gamma
\end{array}
\right)
$$
Saltamos varios pasos intermedios:
$$
\left(
\begin{array}{cccc|c}
1 & -1 & 1 & 1 & \alpha \\
0 & 1 & 1 & -2 & \beta - \alpha \\
0 & 2 & 2 & -4 & \gamma - \alpha
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
1 & -1 & 1 & 1 & \alpha \\
0 & 1 & 1 & -2 & \beta - \alpha \\
0 & 0 & 0 & 0 & \gamma - 2\beta + \alpha
\end{array}
\right)
$$
Sabemos que el sistema es compatible si las filas son nulas tanto del lado izquierdo como del derecho. Entonces:
$$
\begin{align}
(\alpha, \beta, \gamma) \in \mathrm{Im}(T) &\Longleftrightarrow S_{\alpha, \beta, \gamma} \text{ es compatible} \\
&\Longleftrightarrow \alpha - 2\beta + \gamma = 0
\end{align}
$$
De esta manera, tenemos un nuevo sistema con una ecuación:
$$
\begin{align}
S' : \alpha - 2b + \gamma = 0 \implies Sol(S') &= \{ (2\beta - \gamma, \beta, \gamma) : \beta, \gamma \in \mathbb{R} \} \\
&= \{ \beta(2, 1, 0) + \gamma(-1, 0, 1) : \beta, \gamma \in \mathbb{R} \} \\
&= \mathrm{Im}(T)
\end{align}
$$

Luego, tenemos un generador de la imagen $\mathrm{Im}(T)$:
$$
\mathrm{Im}(T) = \{ \beta(2, 1, 0) + \gamma(-1, 0, 1) : \beta, \gamma \in \mathbb{R} \}
$$
$$
\implies \{ (2, 1, 0), (-1, 0, 1) \} \text{ es generador de } \mathrm{Im}(T)
$$
Pero, como $\{ (2, 1, 0) + (-1, 0, 1) \}$ es LI, podemos determinar que el conjunto anterior es una base de $\mathrm{Im}(T)$.

Al final, podemos concluir que:
$$
\underbrace{ \mathrm{Ker}(T) }_{ dim(\mathrm{Ker}(T)) = 2 } \subset \mathbb{R}^{4} \qquad \text{y} \qquad \underbrace{ \mathrm{Im}(T) }_{ dim(\mathrm{Im}(T)) = 2 } \subset \mathbb{R}^{3}
$$

La observación final es que $dim(\mathrm{Ker}(T)) + dim(\mathrm{Im}(T)) = dim(\mathbb{R}^{4})$ (en este caso).

Luego veremos que es una regla general: la suma de las dimensiones del núcleo y la imagen de una transformación lineal da como resultado la dimensión del espacio vectorial de partida de la transformación lineal.

Veremos otro ejemplo:
### Ejemplo 2
Sea $T : \mathbb{R}_{2}[x] \to \mathbb{R}^{2}$ definida por
$$
T(p) := (p(0), p(1))
$$
Queremos hallar una base del núcleo y una base de la imagen.

Primero, estudiemos el núcleo:
$$
\begin{align}
p \in \mathrm{Ker}(T) &\Longleftrightarrow \begin{cases}
p(0) = 0 \\
p(1) = 0
\end{cases} \\
&\Longleftrightarrow p \text{ es de la forma } p = \alpha x(x - 1)
\end{align}
$$Como 0 y 1 son raíces del polinomio, podemos factorizarlo.

El razonamiento para llegar a dicha forma es el siguiente:
$$
p(x) = \alpha x^{2} + \beta x + \gamma
$$
$$
\begin{align}
p(0) = 0 \Longleftrightarrow \gamma = 0 \\
p(1) = 0 \Longleftrightarrow \alpha + \beta + \gamma = 0
\end{align}
$$
$$
\begin{align}
\begin{cases}
\beta = -\alpha \\
\gamma = 0
\end{cases} \implies p &= \alpha x^{2} - \alpha x \\
&= \alpha x(x - 1)
\end{align}
$$
La forma del núcleo será una recta de polinomios, pues está compuesto por todos los múltiplos del polinomio $x(x - 1)$.

Entonces:
$$
\mathrm{Ker}(T) = \{ \alpha x(x - 1) : \alpha \in \mathbb{R} \} = \mathbb{R}x(x - 1)
$$
Base:
$$
\{ x(x - 1) \}
$$

Pasamos a estudiar la imagen:
$$
\mathrm{Im}(T) = \{ (p(0), p(1)) : p \in \mathbb{R}_{2}[x] \}
$$
La dimensión de la imagen está entre 0 y 2 (ya que está delimitado por $\mathbb{R}^{2}$).

Buscamos un polinomio que valga $\alpha$ en 0 y $\beta$ en 1, siendo la función más sencilla una función lineal.

$\forall (\alpha, \beta) \in \mathbb{R}^{2}$, existe una función $f : \mathbb{R} \to \mathbb{R}$ tal que
$$
f(0) = \alpha, f(1) = \beta \implies f(x) = \alpha + (\beta - \alpha)x
$$
Ya que
$$
\begin{align}
&f(0) = \alpha + \cancel{ (\beta - \alpha) \cdot 0 } = \alpha \\
&f(1) = \alpha + (\beta - \alpha) \cdot 1 = \cancel{ \alpha } + \beta - \cancel{ \alpha } = \beta
\end{align}
$$

En conclusión: la imagen es todo el espacio de llegada $\mathbb{R}^{2}$.
$$
\mathrm{Im}(T) = \mathbb{R}^{2}
$$
Podemos tomar cualquier base de $\mathbb{R}^{2}$:
$$
\text{base de } \mathrm{Im}(T) = \{ (1, 0), (0, 1) \}
$$
Nuevamente, $dim(\mathrm{Ker}(T)) = 1$, $dim(\mathrm{Im}(T)) = 2$, $dim(\mathbb{R}_{2}[x]) = 3$, por lo que
$$
dim(\mathrm{Ker}(T)) + dim(\mathrm{Im}(T)) = dim(\mathbb{R}_{2}[x])
$$

Como vemos, utilizamos un método diferente al anterior para hallar el núcleo y la imagen.

---
## Teorema de las dimensiones
Pasaremos a anunciar el teorema de las dimensiones:

**Objetivo**: Demostrar el siguiente teorema.

#Teorema 
> [!Teorema de las dimensiones]
> Sean:
> - $V, W$ espacios vectoriales, con $dim(V) < \infty$ ($V$ con dimensión finita, $W$ puede ser de dimensión finita o infinita).
> - $T : V \to W$ transformación lineal cualquiera.
> 
> <u>Entonces</u>: Los subespacios $\mathrm{Ker}(T)$ e $\mathrm{Im}(T)$ son de dimensión finita, y
> $$
> dim(\mathrm{Ker}(T)) + dim(\mathrm{Im}(T)) = dim(V)
> $$

Esto quiere decir que conociendo dos de las dimensiones anteriores, conocemos la tercera, facilitando la determinación de núcleo e imagen.

Esto también nos indica que la imagen nunca es de dimensión infinita (aunque el espacio de llegada lo sea), ya que no se cumpliría el teorema. La transformación lineal siempre asocia con un espacio finito.

Para la demostración, utilizaremos algunos lemas:

### Lema 1

#Lema
> [!Lema 1]
> Sean
> - $V, W$ espacio vectorial
> - $T : V \to W$
> - $\{ v_{1}, \dots, v_{n} \}$ generador de $V$
> 
> Entonces:
> $$
> \{ T(v_{1}), \dots, T(v_{n}) \} \text{ es un generador de } \mathrm{Im}(T)
> $$

#### Demostración

Sea $w \in \mathrm{Im}(T)$. Entonces $w = T(v)$ para algún $v \in V$.

Como $\{ v_{1}, \dots, v_{n} \}$ es generador, tenemos que
$$
v = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}
$$
para algunos $\alpha_{1}, \dots, \alpha_{n} \in \mathbb{K}$.

Luego
$$
\begin{align}
w &= T(\alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}) \\
&= \alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n}) \\
&\in [T(v_{1}), \dots, T(v_{n})]
\end{align}
$$
Demostramos que cualquier vector de la imagen se puede escribir como combinación lineal de las transformaciones de los elementos del generador de $V$.

Por lo tanto:
$$
\{ T(v_{1}), \dots, T(v_{n}) \} \text{ es generador de } \mathrm{Im}(T)
$$

Básicamente, el lema uno enuncia que la imagen de un generador (del espacio de entrada) siempre es un generador de la imagen (de la transformación lineal).

### Lema 2

#Lema 
> [!Lema 2]
> Sean
> - $V, W$ espacios vectoriales
> - $\{ v_{1}, \dots, v_{n} \} \subset V$
> 
> Si $\{ T(v_{1}), \dots, T(v_{n}) \} \subset W$ es LI, entonces $\{ v_{1}, \dots, v_{n} \} \subset V$ es LI.

Si la imagen de un conjunto es LI, entonces el conjunto es LI. Por lo tanto, sabemos que la imagen de un conjunto LI también será un conjunto LI.

La demostración también es simple:

#### Demostración
Supongamos $\{ T(v_{1}), \dots, T(v_{n}) \} \subset W$ es LI.

Sean $(\alpha_{1}, \dots, \alpha_{n}) \in \mathbb{K}^{n}$ tales que
$$
\alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n} = 0
$$
Luego
$$
T(\alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}) = 0
$$
Luego
$$
\alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n}) = 0
$$

Entonces, como $\{ T(v_{1}), \dots, T(v_{n}) \} \subset W$ es LI, deducimos que $\alpha_{1} = \alpha_{2} = \dots = \alpha_{n} = 0$.

Por lo tanto: $\{ v_{1}, \dots, v_{n} \}$ es LI.

Continuamos con el siguiente lema, el cual es algo más sutil y no tan trivial.

### Lema 3

#Lema 

Sean
- $V, W$ espacios vectoriales
- $T : V \to W$ una transformación lineal
- $\{ v_{1}, \dots, v_{k} \}$ base de $\mathrm{Ker}(T)$
- $\{ v_{1}, \dots, v_{k}, v_{k + 1}, \dots, v_{n} \}$ base de $V$

Entonces:
$$
\{ T(v_{k + 1}), \dots, T(v_{n}) \} \text{ es una base de } \mathrm{Im}(T)
$$

De esta forma, tomamos una base del núcleo, generador del núcleo, la cual es libre en el núcleo, pero también en el espacio de entrada. Entonces, completamos la base del núcleo hasta formar una base del espacio de entrada (base incompleta).

De esta manera, las transformaciones de los elementos agregados para completar la base de $V$ forman una base de la imagen de la transformación lineal.

Ahora, tenemos que demostrar que el conjunto es generador y también es libre.

#### Demostración
$\{ v_{1}, \dots, v_{k}, v_{k + 1}, \dots, v_{n} \}$ generador de $V$.

Por el lema 1:
$\{ T(v_{1}), \dots, T(v_{k}), T(v_{k + 1}), \dots, T(v_{n}) \}$ generador de $\mathrm{Im}(T)$

Sin embargo, sabiendo que $\{ v_{1}, \dots, v_{k} \}$ generador de $\mathrm{Ker}(T)$, entonces $T(v_{1}) = \dots = T(v_{k}) = 0$.
Por lo tanto, no aportan nada al conjunto y podemos removerlos.

Entonces $\{ T(v_{k + 1}), \dots, T(v_{n}) \}$ generador de $\mathrm{Im}(T)$.

Ahora, queremos demostrar que $\{ T(v_{k + 1}), \dots, T(v_{n}) \}$ es LI.

Supongamos que existen $\alpha_{k + 1}, \dots, \alpha_{n} \in \mathbb{K}$ tales que
$$
\alpha_{k + 1} \cdot T(v_{k + 1}) + \dots + \alpha_{n} \cdot T(v_{n}) = 0
$$

Tenemos que $T(\alpha_{k + 1} v_{k + 1} + \dots + \alpha_{n} v_{n}) = 0$.
Entonces $\alpha_{k + 1} v_{k + 1} + \dots + \alpha_{n} v_{n} \in \mathrm{Ker}(T)$.

Entonces (sabiendo que conocemos una base del núcleo), existen $\beta_{1}, \dots, \beta_{k} \in \mathbb{K}$ tales que
$$
\alpha_{k + 1} v_{k + 1} + \dots + \alpha_{n} v_{n} = \beta_{1} v_{1} + \dots + \beta_{k} v_{k} 
$$

Luego
$$
\beta_{1} v_{1} + \dots + \beta_{k} v_{k} - \alpha_{k + 1} v_{k + 1} - \dots - \alpha_{n} v_{n} = 0
$$

Sabemos que $\{ v_{1}, \dots, v_{k}, v_{k + 1}, \dots, v_{n} \}$ es una base de todo el espacio $V$. Por lo que, la única forma de que la combinación de dichos vectores sea nula es que todos los coeficientes sean nulos:
$$
\implies \beta_{i} \text{ y } \alpha_{i} \text{ son todos nulos} \qquad (\text{pues } \{ v_{1}, \dots, v_{n} \} \text{ es base de } V)
$$

Por lo tanto: $\{ T(v_{k + 1}), \dots, T(v_{n}) \}$ es L.I.

Luego: es una base de $\mathrm{Im}(T)$.

Ahora, concluiremos con la demostración del teorema de las dimensiones:
### Demostración - Teorema de las dimensiones

- Sean $V, W$ espacios vectoriales, con $V$ de dimensión finita
- $T : V \to W$ transformación lineal

Entonces:
$\mathrm{Ker}(T)$ y $\mathrm{Im}(T)$ tienen dimensión finita y
$$
dim(\mathrm{Ker}(T)) + dim(\mathrm{Im}(T)) = dim(V)
$$

Primero, queremos demostrar que el ambos conjuntos tienen dimensión finita:

Sea $n = dim(V)$. Como $\mathrm{Ker}(T) \underset{sev} \subset V$, tiene dimensión finita $k := dim(\mathrm{Ker}(T)) \leq n$.

Sea $\{ v_{1}, \dots, v_{k} \}$ una base de $\mathrm{Ker}(T)$.

Lo podemos extender hasta formar una base de todo el espacio:
Por el teorema de la base incompleta, existen vectores $v_{k + 1}, \dots, v_{n} \in V$ tales que
$$
\{ v_{1}, \dots, v_{k}, v_{k + 1}, \dots, v_{n} \}
$$
es una base de $V$.

(Recordemos que $\mathrm{Ker}(T) \underset{sev} \subset V$, esta es la razón detrás del razonamiento anterior).

Por el lema 3:
$$
\underbrace{ \{ T(v_{k + 1}), \dots, T(v_{n}) \} }_{ n - k }
$$
es una base de $\mathrm{Im}(T)$.

Entonces, obtuvimos la dimensión de la imagen, que era el dato faltante.

Luego:
$$
dim(\mathrm{Im}(T)) = n - k
$$

Por lo tanto:
$$
dim(\mathrm{Ker}(T)) + dim(\mathrm{Im}(T)) = k + (n - k) = n = dim(V)
$$

Así, concluimos la demostración del teorema de las dimensiones, siendo el último tema del curso.