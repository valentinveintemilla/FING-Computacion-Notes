# Subespacios vectoriales
Retomamos desde los espacios vectoriales abordados la clase pasada.

En todo lo que sigue, $V$ es un espacio vectorial sobre un cuerpo $K$. Si bien la teoría es general, nosotros trabajaremos en el cuerpo $\mathbb{R}$.

> [!Subespacio vectorial - Definición]
> Un conjunto $S \subset V$ es un subespacio vectorial de $V$ cuando:
> $$
> \begin{align}
> &\text{(1)} &&\vec{0} \in S \\
> &\text{(2)} &&\text{Si } u, v \in S, \text{entonces } u + v \in S \\
> &\text{(3)} &&\text{Si } u \in S, \text{entonces } \alpha \cdot u \in S &&(\forall \alpha \in K)
> \end{align}
> $$

Podemos entender a los subespacios vectoriales como estructuras regulares contenidas dentro de espacios vectoriales.

Aquí presentamos otro punto de vista de la definición de subespacio vectorial, considerando dos propiedades en lugar de tres, que quizás faciliten las demostraciones.

> [!Proposición]
> $S \subset V$ es un $s.e.v$ de $V$ si y sólo si
> $$
> \begin{align}
> &\text{(1)} &&S \neq \emptyset \\
> &\text{(2)} &&\text{Si } u, v \in S, \text{entonces } \alpha \cdot u + \beta \cdot v \in S &&(\forall \alpha, \beta \in K)
> \end{align}
> $$

También determinamos que un espacio vectorial tiene al menos dos subespacios vectoriales.

> [!Observación]
> Dos subespacios vectoriales notables:
> $$
> \begin{align}
> &S = V &&\text{(subespacio lleno)} \\
> &S = \{ 0 \} &&\text{(subespacio nulo)}
> \end{align}
> $$

Otra observación realizada la clase pasada es que un subespacio vectorial es un espacio vectorial, puesto que esta estructurado y las operaciones de suma de vectores y producto de un escalar por un vector cumplen todas las propiedades necesarias para ser considerado como tal.

> [!Observación]
> Cada subespacio vectorial $S \subset V$ también constituye un subespacio vectorial.

Además, vimos una serie de ejemplos:

## Ejemplos
- Subespacios de $\mathbb{R}_{3}$
	- El subespacio nulo $\{ 0 \}$.
	- Cada recta que pasar el origen ("recta vectorial").
	- Cada plano que pasa por el origen ("plano vectorial").
	- El espacio lleno $S = \mathbb{R}^{3}$
No hay otros espacios vectoriales en $R_{3}$.

Recta vectorial: recta que pasa por el origen.

En general, cuando trabajamos con un espacio vectorial de dimensión $n$, todos los espacios vectoriales de dimensiones intermedias serán subespacios vectoriales.
- Subespacios de $K^{n}\dots$
	- De dimensión 0 a $n$ (similar al caso anterior).

No definimos formalmente lo que es la dimensión, cosa que en las próximas clases iremos determinando poco a poco, comenzando por una noción de "grados de libertad". Es una noción fundamental tanto en matemática y física, aunque aún no pasaremos a definiciones formales.

- Subespacios de $M_{n \times n} (K)$ (cuadradas)
	Dichos subespacios tienen dimensión $n \times n$.
	- $S_{1} = \{ A \in M_{n \times n} (K) : A = A^{t} \} \underset{sev} \subsetneq M_{n \times n} (K)$ (matrices simétricas)
		Es un subespacio estricto (menos en el caso $n = 1$, pues en este caso todas las matrices son simétricas) del subespacio vectorial de matrices cuadradas.
	- $S_{2} = \{ A \in M_{n \times n} (K) : A^{t} = -A \} \underset{sev} \subsetneq M_{n \times n} (K)$ (matrices antisimétricas)
		La matriz nula es antisimétrica, si sumamos dos matrices antisimétricas obtenemos otra antisimétrica, y el producto de un escalar por una matriz antisimétrica es otra matriz antisimétrica. Por estas razones, es un espacio vectorial.

También podemos estudiar ejemplos que vienen de Cálculo I:
- Subespacios de $\mathbb{R}^{I} = \{ f : I \to \mathbb{R} \text{ función} \}$ (donde $I \subset \mathbb{R}$ intervalo)
	Aquí, los vectores tienen una cantidad infinida de componentes, pues el valor de la función en cada punto es una componente distinta. De esta forma, tenemos un espacio de dimensión infinita.
	El vector nulo es la función nula $f(x) = 0$, y pertenece a todos los subespacios vectoriales que mencionaremos a continuación. Además, la suma entre vectores y el producto de un escalar por un vector están bien definidos.
	- $\mathcal{C}^{0}(I, \mathbb{R}) = \{ f : I \to \mathbb{R} \text{ continua} \} \underset{sev} \subset \mathbb{R}^{I}$
	- $Der(I, \mathbb{R}) = \{ f : I \to \mathbb{R} \text{ derivable} \} \underset{sev} \subset \mathbb{R}^{I}$
		Como todas las funciones derivables son continuas, podemos afirmar con seguridad que:
		- $Der(I, \mathbb{R}) \underset{sev} \subset \mathcal{C}^{0}(I, \mathbb{R}) \underset{sev} \subset \mathbb{R}^{I}$
	En base a lo anterior, también podemos definir subespacios vectoriales basados en otros y con condiciones más estrictas.
	- $\mathcal{C}^{1}(I, \mathbb{R}) = \{ f \in \mathcal{C}^{0}(I, \mathbb{R}) : f' \text{ existe y es continua} \subset \mathbb{R}^{I} \}$ (puesto que la derivada de una función no tiene porque ser continua.)
		La función nula cumple con las condiciones establecidas, y la suma de vectores y el producto de un escalar por un vector son operaciones cerradas.
	- De modo análogo, se define $\mathcal{C}^{k}(I, \mathbb{R}) \qquad (k \in \mathbb{N})$
		De esta forma:
		- $C^{1}(I, \mathbb{R})$: funciones continuas con derivada continua
		- $C^{2}(I, \mathbb{R})$: funciones continuas derivables 2 veces, y ambas derivadas continuas, y así continuamente.
		Todos estos son espacios de dimensión infinita y son espacios encajados:$$
		 \mathcal{C}^{n + 1}(I, \mathbb{R}) \subset \mathcal{C}^{n}(I, \mathbb{R}) \subset \dots \subset \mathcal{C}^{2}(I, \mathbb{R}) \subset \mathcal{C}^{1}(I, \mathbb{R}) \subset \mathcal{C}^{0}(I, \mathbb{R}) \subset \mathbb{R}^{I}
		$$
		Al límite, tenemos $\mathcal{C}^{\infty}(I, \mathbb{R}) = \underset{k \in \mathbb{N}} \cap \mathcal{C}^{k}(I, \mathbb{R})$
		
		Esto no podría ser posible en dimensión finida, pues por ejemplo, si partimos de un espacio vectorial de dimensión 3, luego siguen los espacios de dimensión 2, 1 y 0. Sin embargo, en dimensión infinita, podemos tener una sucesión infinita de espacios vectoriales encajados. Igualmente no trabajaremos mucho con los mismos.
		
		Esto nos da otro ejemplo: el subespacio de los polinomios
		- $\mathbb{R}[x] \underset{sev} \subset \mathcal{C}^{\infty}(\mathbb{R}, \mathbb{R})$

Directamente, pasaremos a estudiar los subespacios de espacios de polinomios:
- Subespacios de $\mathbb{R}[X] = \{ p(x) \text{ polinomios} \}$
	- El conjunto de los polinomios de grado $n$ no es un $sev$.
		Esto se debe a que el vector nulo no pertenece al conjunto (a no ser que consideremos $n = 0$), y la suma de vectores puede dar como resultado un vector que no forme parte del conjunto (un polinomio de menor grado, o incluso 0). Se dice que para los polinomios, el polinomio nulo (0) tiene grado $-\infty$
	  
	- El conjunto de los polinomios de grado $\leq n$ es un $sev$.
		$\mathbb{R}_{n}[X] \underset{sev} \subset \mathbb{R}[X]$
		$R_{n}[X]$ quiere decir "polinomios de grado $\leq n$"
		Este si es un subespacio vectorial, ya que incluye al elemento nulo, la suma de dos polinomios siempre se encuentra en el subespacio (pudiendo mantener o bajar el grado, nunca subir).
		
		Si consideramos el concepto de dimensión, dicho espacio tiene dimensión $n + 1$, ya que consideramos $n$ grados de libertad mas 1 (el grado 0).
		
		Algunos ejemplos:
		- $\mathbb{R}_{1}[X] = \{ ax + b : a, b \in \mathbb{R} \}$ (grado 2: a y b)
		- $\mathbb{R}_{2}[X] = \{ ax^{2} + bx + c : a, b, c \in \mathbb{R} \}$ (grado 3: a, b y c), etc.

---
Ahora, proseguimos con el siguiente tema: operaciones con subespacios vectoriales.
## Operaciones con los $sev$

### Intersección

> [!Intersección]
> Si $S_{1}, S_{2} \underset{sev} \subset V$, entonces
> $$
> S_{1} \cap S_{2} \underset{sev} \subset V
> $$

### Unión

> [!Unión]
> Si $S_{1}, S_{2} \underset{sev} \subset V$, entonces
> $$
> \text{En general, } S_{1} \cup S_{2} \text{ NO ES UN SEV}
> $$

La unión es un $sev$ únicamente si ambos subespacios vectoriales son iguales, o uno está contenido en el otro.

De esta forma, utilizaremos la intersección para dar lugar a nuevos subespacios vectoriales, pero nunca utilizaremos la unión.

De esta forma, para tener una operación de "adición" de subespacios vectoriales, definiremos a la suma para tomar el lugar de la unión.

### Suma

> [!Suma]
> Si $S_{1}, S_{2} \underset{sev} \subset V$, entonces
> $$
> \begin{align}
> S_{1} + S_{2} &= \{ u_{1} + u_{2} : u_{1} \in S_{1}, u_{2} \in S_{2} \} \\
> &\underset{sev} \subset V
> \end{align}
> $$

No solo incluimos los vectores de $S_{1}$ y $S_{2}$, sino también todas las sumas entre sí. Hacemos "copular" entre si los vectores de $S_{1}$ y $S_{2}$.

> [!Observación]
> $$
> S_{1} \cup S_{2} \subset S_{1} + S_{2} \underset{sev} \subset V
> $$

De esta forma, la suma funciona como una alternativa a la unión (encontrándose esta incluida en la suma), únicamente utilizando dicha operación en conjunto con la intersección.

---
A continuación, abordaremos otro de los temas centrales: combinaciones lineales. Este está más enfocado en la matemática dentro de un espacio vectorial fijado.

## Combinaciones lineales

Sean $u_{1}, \dots, u_{n} \in V$.

Se dice que un vector $u \in V$ es <u>combinación lineal</u> de $u_{1}, \dots, u_{n}$ cuando existen $\alpha_{1}, \dots, \alpha_{n} \in K$ tales que
$$
u = \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n}
$$

Por ejemplo, un plano vectorial es el conjunto de todas las combinaciones lineales de sus dos vectores directores.

Generalmente tendremos problemas del estilo: "dada una familia finita de vectores, y dado otro vector, determinar si el vector es combinación lineal o no, de los vectores anteriores". Esto quiere decir si esta en el espacio generado por los vectores mencionados, puesto que todas las combinaciones de los vectores determinan un subespacio, llamado el espacio generado.

Por ahora nos enfocaremos en las combinaciones lineales, pasando a ver algunos ejemplos:

### Ejemplos
- En $v = \mathbb{R}[X]$, el polinomio $p(x) = 5x^{4} + x^{2} + 3x - 4$ es combinación lineal de los monomios $x^{4}$, $x^{2}$, $x$ y 1 (a cada uno le corresponde un $\alpha$ diferente).
- En $V = C^{0}(\mathbb{R}, \mathbb{R})$, la función constante $f(x) = 3$ es combinación lineal de las funciones $\cos ^{2}$ y $\sin ^{2}$, pues $f = 3 \cdot \cos ^{2} + 3 \cdot \sin ^{2}$ (la suma de ambas equivale a la función constante 1, y si consideramos $\alpha = 0$ obtenemos $f(x) = 3$).
	Sin embargo, la misma función constante $f(x) = 3$ es combinación lineal de otras funciones, por ejemplo, los polinomios $x^{2} - 1$ y $2x^{2} + 2$.
	
	$2(x^{2} - 1) - 1(2x^{2} + 2) = -4$
	Luego: $-\frac{3}{2}(x^{2} - 1) + \frac{3}{4}(2x^{2} + 2) = 3 = f$
	
	Aquí, pudimos arreglar las cosas a mano, pero en casos más complejos es necesario desarrollar un sistema lineal.
	
	- La función constante $f(x) = 1$, ¿es combinación lineal de los polinomios $x^{2} - 1$ y $x + 1$?
		Básicamente, tenemos que encontrar coeficientes que nos permitan combinar los polinomios anteriores de tal forma que obtengamos la función deseada.
		Se trata de determinar $\alpha, \beta \in \mathbb{R}$ tales que $1 = \alpha(x^{2} - 1) + \beta(x + 1)$$$
		\begin{align}
		&\Longleftrightarrow \alpha x^{2} + \beta x + (-\alpha + \beta - 1) = 0 \\
		&\Longleftrightarrow \begin{cases}
		&\alpha = 0 \\
		&\beta = 0 \\
		&-\alpha + \beta - 1 = 0
		\end{cases}
		\end{align}
		$$
		Como vemos, obtuvimos un sistema incompatible, por lo que la función constante $f(x) = 1$ no es combinación lineal de los polinomios $x^{2} - 1$ y $x + 1$.
		
		Este es un ejemplo de un elemento que no es combinación lineal de otros dos.

A continuación, abordaremos una proposición asociada a las combinaciones lineales.

> [!Observación]
> En un $sev$ $S \subset V$, cualquier combinación lineal de vectores de $S$ también es un vector de $S$:
> $$
> \text{Si } u_{1}, \dots, u_{n} \in S, \text{entonces } \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} \in S \qquad (\forall \alpha_{1}, \dots, \alpha_{n} \in K)
> $$

De hecho, ahora podemos volver a definir un subespacio vectorial, siendo un conjunto de vectores estable por combinación lineal cualquiera.

Esto nos lleva al siguiente concepto: subespacio generado:

### Subespacio generado

Sea $V$ un $e.v$ sobre un cuerpo $K$ y $A \subset V$ subconjunto cualquiera (puede ser o no un subespacio vectorial).

El subespacio generado por $A$, escrito $[A]$, es el conjunto de todas las combinaciones lineales de vectores en $A$:
$$
[A] = \left\{ \alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n} : \space \begin{align}
&n \geq 0, \\
&u_{1}, \dots, u_{n} \in A \\
&\alpha_{1}, \dots, \alpha_{n} \in K
\end{align} \right\}
$$

Básicamente, podemos tomar cualquier subconjunto mundano y dotarlo de tal forma que se transforme en un espacio vectorial, pasando a ser un "subespacio generado".

De esta forma, obtendremos el vector nulo (caso $n = 0$), además de todos los vectores que ya estaban en $A$, y todas las combinaciones lineales posibles.
Esto se llama el subespacio generado por $A$, y es un subespacio vectorial. Por construcción, contiene el vector nulo, es estable por suma y es estable por cualquier producto. Además, es el subespacio vectorial más pequeño que contiene a $A$ como subconjunto.

Continuaremos con este mismo tema la próxima clase.