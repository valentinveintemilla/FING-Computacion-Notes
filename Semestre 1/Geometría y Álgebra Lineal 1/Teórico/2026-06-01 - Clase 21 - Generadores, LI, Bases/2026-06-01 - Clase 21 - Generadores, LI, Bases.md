# Espacios vectoriales
Continuaremos con los problemas de combinaciones lineales, así como conjuntos linealmente dependientes o independientes.

> [!Recordatorio]
> Sea $V$ un espacio vectorial.
> 
> Se dice que un conjunto $\{ u_{1}, \dots , u_{n} \}$ es:
> - Linealmente dependiente (LD) si existen $\alpha_{1}, \dots, \alpha_{n} \in \mathbb{K}$ <u>no todos nulos</u> tales que
> $$
> \alpha_{1} u_{1} + \dots + \alpha_{n} u_{n} = \vec{0}
> $$
> - Linealmente independiente (LI) si para todos $\alpha_{1}, \dots, \alpha_{n} \in \mathbb{K}$, tenemos que
> $$
> \alpha_{1} u_{1} + \dots + \alpha_{n} u_{n} = \vec{0} \implies \alpha_{1} = \dots = \alpha_{n} = 0
> $$

(LD) No pueden ser todos nulos, ya que si todos pudieran ser nulos, se cumpliría la condición especificada de modo trivial.

No se considera al vector nulo en este caso, ya que para que un espacio vectorial sea tal, debe contener al vector nulo.

Podemos ver a un conjunto como linealmente dependiente si:
- Existe un vector que es combinación lineal del resto (no tienen porque ser todos). O sea, hay uno o más vectores que "sobran", ya que son múltiplos de otros o el resultado de combinaciones lineales en base al resto.

También vimos una caracterización:

#Caracterización
> [!Caracterización]
> Un conjunto $\{ u_{1}, \dots, u_{n} \} \subset V$ es LD si y sólo si alguno vector $v_{i} \space (1 \leq i \leq n)$ es combinación lineal de los vectores restantes.

Existe una terminología alternativa:
- Conjunto libre = conjunto linealmente independiente
De esta forma: LI = Linealmente Independiente o LIbre.

Cuando decimos libre, es libre de relaciones entre los elementos (no están relacionados de ninguna forma).

Otro de los conceptos abordados la clase pasada es el de base:

## Base

#Definición 
> [!Base de un espacio - Definición]
> Un conjunto $B = \{ v_{1}, \dots, v_{n} \} \subset V$ es una <u>base</u> de $V$ cuando es a la vez libre y generador de $V$.

De esta forma, es un conjunto linealmente independiente, además de ser generador de $V$ (si se desarrollan todas las combinaciones lineales posibles con los elementos de $B$, se obtiene $V$).

Veremos algunos ejemplos de bases:
- Base canónica de $\mathbb{K}^{n} \qquad (n \geq 1)$
$$
B = \{ \underbrace{ (1, 0, \dots, 0) }_{ e^{1} }, \underbrace{ (0, 1, \dots, 0) }_{ e^{2} }, \dots, \underbrace{ (0, 0, \dots, 1) }_{ e^{n} } \}
$$
De esta forma, una n-upla cualquiera $(\alpha_{1}, \dots, \alpha_{n})$ del espacio vectorial $\mathbb{K}^{n}$ se puede escribir como combinación lineal de los elementos de $B$:
$$
(\alpha_{1}, \dots, \alpha_{n}) = \alpha_{1} e^{2} + \alpha_{2} e^{2} + \dots + \alpha_{n} e^{n}
$$
Por ejemplo, si consideramos:
$$
n = 3: (\alpha, \beta, \gamma) = \alpha e^{1} + \beta e^{2} + \gamma e^{3}
$$
Esto nos demuestra que el conjunto $B$ es un generador, ya que cada elemento de $\mathbb{K}^{n}$ se puede escribir como combinación lineal de los elementos de $B$, pero además, $B$ es linealmente independiente (libre), ya que no hay forma de escribir un elemento cualquiera $e^{i}$ en forma de combinación lineal del resto de elementos:
$$
e^{1} = 0 \times e^{2} + 0 \times e^{3} + \dots + 0 \times e^{n}
$$
ya que $e_{1}$ tiene 0 en la posición $2, 3, \dots, n$.
Lo mismo sucede para el resto de elementos.
Por estas razones, $B$ es una base de $\mathbb{K}^{n}$: <u>base canónica</u> (la más sencilla del conjunto $\mathbb{K}^{n}$).

Existen infinitas otras bases de $\mathbb{K}^{n}$. Por ejemplo, podemos considerar los opuestos de $e^{1}, e^{2}, \dots, e^{n}$, los dobles, los triples, etc., y se sigue manteniendo la propiedad de base. Además, todas tienen la misma cantidad de elementos.

Aclaración: con base canónica, nos referimos a la base "estándar", o "ideal" de un conjunto.

- En $\mathbb{R}^{3}$:
	- Todas las bases de una recta vectorial $R$ son de la forma: $B = \{ u \}$ donde $u$ es cualquier vector director de $R$ (no nulo).
		De esta forma, todas las bases de una recta tienen en común que únicamente tienen un elemento, por lo tanto, decimos que tienen dimensión 1.
	- Todas las bases de un plano vectorial $P$ son de la forma $B = \{ u, v \}$ donde $u$ y $v$ son vectores directores no colineales de $P$. 
		Que no sean colineales, asegura que no son múltiplos entre si, por lo que el conjunto es linealmente independiente.
		Si fueran colineales, no formaría un plano, sería una recta, y no sería una base, puesto que los vectores serían múltiplos entre sí.

Las bases tienen sentido para los espacios vectoriales, pero como los subespacios vectoriales también son espacios vectoriales, sabemos que existe la noción de base para subespacios vectoriales. Ahora abordaremos algunos ejemplos:
- En el espacio $V = M_{3 \times 3}(\mathbb{K})$
	- El subespacio $S_{1}$ de las matrices simétricas tiene base:$$
B_{1} = \left\{ \begin{pmatrix}
1 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
1 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 1 \\
0 & 1 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 1
\end{pmatrix} \right\}
	  $$
	  Como vemos, este conjunto solo contiene matrices simétricas, y es claro que, sabiendo que la forma de cada matriz simétrica es:$$
\begin{pmatrix}
\alpha & \beta & \gamma \\
\beta & \delta & \epsilon \\
\gamma & \epsilon & \eta
\end{pmatrix}
	  $$
	  es claro que cada matriz simétrica se puede expresar como $\alpha m_{1} + \beta m_{2} + \gamma m_{3} + \dots + \eta m_{6}$. Por lo tanto, es un generador.
	  
	  Ahora, verificamos que es libre: si intentamos escribir una matriz como combinación lineal del resto, es imposible, ya que, donde una matriz tiene un 1, el resto tiene 0, por lo que nunca podré obtener un 1 en la posición donde haya uno en base al resto de matrices.
	  
	  En conclusión, es una base del subespacio $S_{1}$.
	  
	  Aquí, la dimensión del subespacio es 6.
	  
	- El subespacio $S_{2} \underset{sev} \subset V$ de las matrices antisimétricas tiene base:$$
B_{1} = \left\{ \begin{pmatrix}
0 & 1 & 0 \\
-1 & 0 & 0 \\
0 & 0 & 0
\end{pmatrix}, \begin{pmatrix}
0 & 0 & 1 \\
0 & 0 & 0 \\
-1 & 0 & 0
\end{pmatrix},
\begin{pmatrix}
0 & 0 & 0 \\
0 & 0 & 1 \\
0 & -1 & 0
\end{pmatrix}
\right\}
	  $$
	  Como vemos, este conjunto solo contiene matrices antisimétricas, por lo que, sabiendo que la forma de cada matriz simétrica es:$$
\begin{pmatrix}
0 & \alpha & \beta \\
-\alpha & 0 & \gamma \\
-\beta & -\gamma & 0
\end{pmatrix}
	  $$
	  es claro que cada matriz simétrica se puede expresar como $\alpha m_{1} + \beta m_{2} + \gamma m_{3}$. Por lo tanto, es un generador.
	  
	  Ahora, verificamos que es libre: si intentamos escribir una matriz como combinación lineal del resto, es imposible, por la misma razón vista anteriormente.
	  
	  En conclusión, es una base del subespacio $S_{2}$.
	  
	  Aquí, la dimensión del subespacio es 3.
	  
	  Lo que se puede verificar es que, si unimos ambas bases, obtenemos una base del espacio global (todas las matrices $M_{3 \times 3}(\mathbb{K})$), teniendo 9 vectores. Sin embargo, será una base no canónica a causa de los coeficientes "extraños" (no simples)

Es así que definiremos a la dimensión de un espacio como la cantidad de elementos de sus bases.

Algo general de las matrices (luego de estudiarlas), es que cualquier matriz se puede descomponer como combinación lineal de una matriz simétrica y una matriz antisimétrica.

Ahora, pasaremos a estudiar un teorema relacionado:

#Teorema
> [!Teorema]
> Un conjunto $\{ v_{1}, \dots, v_{n} \} \subset V$ es una base si y sólo si todo vector de $V$ se escribe <u>en forma única</u> como combinación lineal de los vectores $v_{1}, \dots, v_{n}$.

¿Por que en forma única? Esto es importante, ya que indica que, además de que la familia $v_{1}, \dots, v_{n}$ es generador de $V$, sino que es una base, puesto que la descomposición es única. Cuando no es una base, pero si un generador, entonces existen múltiples formas de descomponer cada vector de $V$.

A continuación, demostramos el teorema:
Comenzamos por la implicación directa.
$(\implies)$ Supongamos que $v_{1}, \dots, v_{n}$ sea una base. Como $v_{1}, \dots, v_{n}$ también es un generador, para todo vector $u \in V$, existen $\alpha_{1}, \dots, \alpha_{n} \in \mathbb{K}$ tales que $u = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}$.

<u>Unicidad</u>: Supongamos que haya otra descomposición:
$$
u = \beta_{1} \cdot v_{1} + \dots + \beta_{n} \cdot v_{n}
$$
Entonces:
$$
\vec{0} = u - u = (\alpha_{1} - \beta_{1}) \cdot v_{1} + \dots + (\alpha_{n} - \beta_{n}) \cdot v_{n}
$$
Como la familia $v_{1}, \dots, v_{n}$ es libre, tenemos que necesariamente todos los coeficientes son nulos:
$$
\alpha_{1} - \beta_{1} = \alpha_{2} - \beta_{2} = \dots = \alpha_{n} - \beta_{n} = 0
$$

Luego:
$$
\alpha_{1} = \beta_{1}, \alpha_{2} = \beta_{2}, \dots, \alpha_{n} = \beta_{n}
$$

Ahora, pasaremos al recíproco.
$(\impliedby)$ Supongamos que todo vector $u \in V$ se escribe en forma única como combinación lineal de los vectores $v_{1}, \dots, v_{n}$.

(Demostraremos que la familia es una base, suponiendo que cada vector tiene una descomposición única en función de los vectores de la familia mencionada.)

Obviamente, esto implica que $\{ v_{1}, \dots, v_{n} \}$ es un generador de $V$.

Ahora, queremos demostrar que $\{ v_{1}, \dots, v_{n} \}$ es libre.

<u>Libertad</u>: Supongamos que
$$
\alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n} = \vec{0}
$$
(queremos demostrar que $\alpha_{1} = \alpha_{2} = \dots = \alpha_{n} = 0$.)

Se observa que:
$$
0 \cdot v_{1} + \dots + 0 \cdot v_{n} = \vec{0}
$$
Como supusimos que todos los vectores de $V$ tienen descomposición única, esto también incluye al vector nulo $\vec{0}$. Por lo tanto, como definimos dos descomposiciones del vector nulo, deducimos que ambas son iguales (por la hipótesis).

Por unicidad de la descomposición (hipótesis), tenemos que
$$
\alpha_{1} = 0, \dots, \alpha_{n} = 0
$$
Luego: $\{ v_{1}, \dots, v_{n} \}$ es libre.

Aunque el razonamiento parezca simple y trivial, es totalmente válido y correcto.

---
Ahora, pasamos al tema central del curso dentro de la teoría de espacios vectoriales: la noción de dimensión.

## Dimensión

Antes de esto, estudiaremos un teorema, el cual será el primer (y quizás único) teorema no trivial (al menos para un matemático) que veremos en el curso.

La intuición que tenemos sobre dimensión es que coincide con la cantidad de elementos de una base de un espacio vectorial. Sin embargo, ¿Qué pasa si tenemos muchas bases? ¿Qué pasa si no todas tienen la misma cantidad de elementos?

Ahora, verificaremos que, si una base de un espacio vectorial tiene $n$ elementos, entonces, todas las bases de dicho espacio vectorial tienen $n$ elementos.
Luego de comprobar esto, podremos utilizar dicha noción para definir lo que es la dimensión.

Objetivo: demostrar el siguiente teorema:

### Teorema

#Teorema 
> [!Teorema]
> Si un espacio vectorial $V$ tiene una base con $n$ elementos, entonces todas las bases de $V$ tienen $n$ elementos.

Utilizaremos lemas intermedios para demostrar dicho teorema.

Para cumplir con el objetivo, comenzaremos por estudiar y demostrar el siguiente teorema:

### Teorema

#Teorema
> [!Teorema - Libre VS Generador]
> Si $V$ es un espacio vectorial, $L \subset V$ un conjunto libre finito, y $G \subset V$ un conjunto generado finito.
> 
> Entonces:
> $$
> \# L \leq \# G
> $$

Demostraremos que el cardinal de cualquier conjunto libre es menor o igual al cardinal de cualquier conjunto generador, incluso si no tienen nada que ver (siempre y cuando hagan referencia al mismo espacio vectorial).

También, se puede ver que el primer teorema es fácilmente deducible a partir de este:
Tenemos dos bases: $B_{1}, B_{2}$, y queremos demostrar que tienen la misma cantidad de elementos.

Si $B_{1}$ es base, entonces es libre.
Si $B_{2}$ es base, entonces es generador.

Por el teorema, $\# B_{1} \leq \# B_{2}$.

Sin embargo, también se cumple que (por simetría):

Si $B_{2}$ es base, entonces es libre.
Si $B_{1}$ es base, entonces es generador.

Nuevamente, por el teorema, $\# B_{2} \leq \# B_{1}$.

En conclusión: $\# B_{2} = \# B_{1}$.

A continuación, demostramos el teorema "Libre VS Generador".

La demostración se trata de contar la cantidad de elementos de conjuntos a partir de las nociones de independencia lineal y combinación lineal, deduciendo información sobre la cardinalidad a partir de propiedades y operaciones vectoriales.

<u>Idea de la prueba</u>:
A partir de un libre $L \subset V$ y un generador $G \subset V$ vamos a construir otro generador $G' \subset V$ tal que $\# G' = \# G$ y $L \subset G'$.

Si construir un $G'$ con las características mencionadas, vamos a deducir que $\# L \leq \# G'$, y, en conclusión, $\# L \leq \# G$.

El conjunto $L$ será fijo, pero iremos manipulando el generador $G$, para que contenga a todo $L$, y cuando tengamos la inclusión, la desigualdad de cardinalidad será trivial.

Para ello, se demuestra el siguiente lema:

#### Lema

#Lema 
> [!Lema]
> Supongamos que
> - $L = \{ v_{1}, \dots, v_{p} \} \in P$ es un conjunto libre.
> - $G \subset V$ es un conjunto generador (finito) tal que
> $$
> \{ v_{1}, \dots, v_{k} \} \subset G
> $$
> para algún $k$ tal que $0 \leq k < p$.
> 
> Entonces, existe otro generador $G'$ tal que $\# G' = \# G$ y $\{ v_{1}, \dots, v_{k}, v_{k + 1} \} \subset G'$.

De esta forma, $G$ ya tiene $k$ elementos en común con $L$ (específicamente, todos los elementos de $v_{1}$ a $v_{k}$, pero faltando desde $v_{k + 1}$ a $v_{p}$.

Lo que veremos es que podemos quitar elementos de $G$ de a uno, y agregar otro elemento de $L$ que no esté presente en $G$.

Es fundamental entender la noción de la demostración para comprender lo que se está buscando realmente.

Ahora, si logramos demostrar este lema, podremos aplicar la estrategia mencionada y probar los teoremas anterior fácilmente.

##### Demostración
Escribamos:
- $L = \{ v_{1}, \dots, v_{p} \}$
- $G = \{ v_{1}, \dots, v_{k}, w_{1}, \dots, w_{r} \}$ para algún $k$ tal que $0 \leq k < p$.
Básicamente, cambiamos la forma de nombrar a los vectores restantes, llamándolos $w_{1}, \dots, w_{r}$.

Esta demostración se realiza mediante una visualización de los cambios y las operaciones realizadas. No sabemos cuales son los elementos restantes, simplemente los reemplazaremos por los faltantes que están en $L$.

Ahora, nos centraremos en el vector $v_{k + 1}$, ya que es el primero que queremos incluir en $G$.

Como $G = \{ v_{1}, \dots, v_{k}, w_{1}, \dots, w_{r} \}$ es generador, existen $\alpha_{1}, \dots, \alpha_{k}, \beta_{1}, \dots, \beta_{r} \in \mathbb{K}$ tales que
$$v_{k + 1} = \alpha_{1} \cdot v_{1} + \dots + \alpha_{k} \cdot v_{k} + \beta_{1} \cdot w_{1} + \dots + \beta_{r} \cdot w_{r}$$

(Esto es posible ya que $G$ es generador de $V$, por lo que en base a combinaciones lineales de los vectores de $G$, podemos generar todo el espacio $V$, y $L$ es simplemente una colección linealmente independiente de vectores de $V$.)

Queremos demostrar que $\beta_{i} \neq 0$ para algún $i \in [1..r]$.

(Como $v_{k + 1}$ está en un conjunto linealmente dependiente, necesariamente se tiene que poder formar a partir de los términos con $\beta$, ya que si se pudiera formar en base a los términos con $\alpha$, el conjunto al que pertenece ($L$) ya no sería linealmente independiente (y lo es por hipótesis).)

En efecto, si todos los $B_{i}$ fueran nulos, tendríamos que
$$
v_{k + 1} = \alpha_{1} \cdot v_{1} + \dots + \alpha_{k} \cdot v_{k}
$$
Esto es imposible, pues $\{ v_{1}, \dots, v_{k}, v_{k + 1} \}$ es LI (ya que si yo defino una familia libre, y restrinjo la familia, la nueva familia sigue siendo libre. Si no hay relación en una familia grande, y tomo una parte de dicha familia, la característica de independencia se mantiene).

Ahora, sabemos que $\beta_{i} \neq 0$ para algún $i \in [1..r]$.

Reordenando $w_{1}, \dots, w_{r}$, se puede suponer que $\beta_{1} \neq 0$ (no nos importa cual es no nulo, tomamos el primero).

(Expresaremos todo en base a $\beta_{1} \cdot w_{1}$.)

Tenemos que:
$$
\begin{align}
\beta_{1} \cdot w_{1} = v_{k + 1} &- \alpha_{1} \cdot v_{1} - \dots - \alpha_{k} \cdot v_{k} \\
&- \beta_{2} \cdot w_{2} - \dots - \beta_{r} \cdot w_{r}
\end{align}
$$
Como $\beta_{1} \neq 0$:
$$
\begin{align}
w_{1} = \frac{1}{\beta_{1}} \cdot v_{k + 1} &- \frac{\alpha_{1}}{\beta_{1}} \cdot v_{1} - \dots - \frac{\alpha_{k}}{\beta_{1}} \cdot v_{k} \\
&- \frac{\beta_{2}}{\beta_{1}} \cdot w_{2} - \dots - \frac{\beta_{r}}{\beta_{1}} \cdot w_{r}
\end{align}
$$
Logramos expresar $w_{1}$ como combinación lineal del resto.
Luego
$$
w_{1} \in [v_{1}, \dots, v_{k}, v_{k + 1}, w_{1}, w_{2}, \dots, w_{r}]
$$

Tenemos que $[G] = [v_{1}, \dots, v_{k}, w_{1}, \dots, w_{r}] = V$

¿Qué pasa si añadimos $v_{k + 1}$? Nada, ya que la propiedad de generador no cambia.

Luego:
$$
[v_{1}, \dots, v_{k}, v_{k + 1}, \cancel{ w_{1} }, w_{2}, \dots, w_{r}]
$$
Sin embargo, como $w_{1}$ es combinación lineal de los demás, lo podemos quitar y se seguira manteniendo la propiedad de generador.

Luego:
$$
\underbrace{ [v_{1}, \dots, v_{k}, v_{k + 1}, w_{2}, \dots, w_{r}] }_{ \text{Sea } G' }
$$
Tenemos:
$$
\# G' = \# G
$$
y
$$
\{ v_{1}, \dots, v_{k}, v_{k + 1} \} \subset G'
$$

No solo mantuvimos la cantidad de elementos, sino que $G'$ tiene un elemento más en común con $L$ que $G$. Es así que determinamos que al menos un coeficiente de $\beta$ (vectores que están en $G$ pero no en $L$) no era nulo, lo pusimos en primera posición ($w_{1}$), descompusimos el vector de $G$ que no está en $L$ como combinación lineal del resto, remplazándolo por un vector partícipe de la combinación lineal que no pertenecía a $G$.

Todo funciona, ya que siempre mantenemos la propiedad de conjunto generador.

Con esto concluimos la clase.