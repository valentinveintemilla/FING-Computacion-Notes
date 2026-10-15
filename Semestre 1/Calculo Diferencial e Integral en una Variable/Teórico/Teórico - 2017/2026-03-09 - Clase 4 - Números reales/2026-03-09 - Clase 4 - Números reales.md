<u>Intuición</u>: Números reales son aquellos que permiten representar todos los puntos de una recta. Incluyen:
* los enteros naturales
* los enteros relativos (naturales + cero + enteros negativos)
* los números racionales
* y muchos más números, como: $\sqrt{2}, \pi, e, \log_{}2, \dots$

Si bien aquí solo especificamos cuatro números irracionales, y sabemos que los conjuntos de elementos naturales, enteros y racionales son infinitos, pero en realidad, hay muchos más números irracionales que irracionales. El infinito de los números irracionales es mayor que el infinito de los racionales, y el problema actual es como capturarlos.

Cada vez que me doy un sistema de coordenadas, utilizo dos puntos, 0 y la unidad (representada como I), de forma que si yo tengo un numero real x, yo puedo asociar el punto X en la recta, de forma que el vector $\vec{OX}$ sea igual a el producto de x y el vector $\vec{OI}$ (vector unitario por convención).
De esta manera, partimos de una recta $\mathbb{R}$, que utilizaremos para representar dicha relación:
![[Figura 1.png]]
$x \in \mathbb{R} \rightarrow X \in R \text{ tal que } \vec{OX} = x \times \vec{OI}$

Es importante destacar que la correspondencia entre los números reales (x) y los puntos de la recta (X) es biyectiva, es decir, existe la misma cantidad de reales, que de números reales.

$\mathbb{R} = \text{recta real }$

La definición de números reales fue un problema central en el siglo XIX, para lo que se tomaron dos enfoques:
* Construcción: suponiendo que los números reales no existen (no están definidos), ¿cómo pueden ser reconstruidos?
* Axiomatización: capturar las propiedades de los números reales e introducir axiomas para dicho conjunto.

Aquí no veremos el método de construcción, aunque es interesante saber que se hizo desarrollando cada uno de los conjuntos a partir del anterior, de la forma $\mathbb{N} \rightarrow \mathbb{Z} \rightarrow \mathbb{Q} \rightarrow \mathbb{R}$, siendo $\mathbb{Q} \rightarrow \mathbb{R}$ el paso más difícil.

## Axiomatización

Axioma: Propiedad, enunciado, regla matemática fundamental que se acepta como verdadera sin necesidad de demostración, siendo útil como punto de partida para deducir y desarrollar otros teormas. Son la base lógica 

Pasaremos a desarrollar una axiomatización, viendo una lista de axiomas y establecer que existe un único objeto $\mathbb{R}$ que satisface toda la lista de axiomas.
$\mathbb{R}$ viene con:
1. Una operación $x + y$ (suma)
2. Una operación $x \times y = x . y = xy$ (producto)
3. Una relación $x \leq y \text{, también escrita } y \geq x$

Se supone que satisface la siguiente lista de 15 axiomas:
1. ($I.1-4$) $\rightarrow$ suma
2. ($II.1-5$) $\rightarrow$ producto
3. ($III.1-5$) $\rightarrow$ orden
4. ($IV$) $\rightarrow$ completitud

A continuación, desarrollamos cada axioma:

### Axiomas de la suma ($I$)

$(I.1) \rightarrow (x+y)+z=x+(y+z) \space \space \space (\forall x,y,z \in \mathbb{R})$
$(I.2) \rightarrow x+y=y+x \space \space \space (\forall x,y \in \mathbb{R})$
$(I.3) \rightarrow \exists 0 \in \mathbb{R} \text{, tal que } x+0=0 \space \space \space (\forall x)$
$(I.4) \rightarrow \forall x \in \mathbb{R}, \exists (-x) \in \mathbb{R}, x+(-x)=0$

Def(Resta): $x-y:=x+(-y) \rightarrow \text{ definida en base a la suma y el opuesto}$

---
### Axiomas del producto ($II$)

$(II.1) \rightarrow (xy)z=x(yz)$
$(II.2) \rightarrow xy=yz$
$(II.3) \rightarrow \exists 1 \in \mathbb{R}, 1 \neq 0 \text{ tal que } x \times 1 = 0 \space \space \space (\forall x)$
$(II.4) \rightarrow \forall x \in \mathbb{R}, x \neq 0, \exists x^{-1} \in \mathbb{R} \text{ tal que } x \times x^{-1} = 1$
$(II.5) \rightarrow (x+y)z=xz+yz$
---
### Axiomas del orden ($III$)

$(III.1) \rightarrow x \leq y \lor y \leq x \space \space \space (\forall x,y)$
$(III.2) \rightarrow x \leq y \land y \leq z \implies x \leq z$
$(III.3) \rightarrow x \leq y \land y \leq x \implies x=y$
$(III.4) \rightarrow x \leq y \implies x+z \leq y+z$
$(III.5) \rightarrow x \geq 0 \land y \geq 0 \implies xy \geq 0$
---
### Axioma de completitud ($IV$)

$(IV)$ Lo veremos en próximas clases

Todo lo que se puede demotrar en $\mathbb{R}$ es consecuencia de la lista anterior. Es fundamental entender como funcionan los números reales para poder operar con los mismos adecuadamente.

## Propiedades de la suma

- Gracias a los axiomas $(I.1-2)$, es posible $x+y+z=z+x+y=\dots$
- $(I.3)$ establece que el neutro $0 \in \mathbb{R}$ es único:
	Si $0,0' \in \mathbb{R}$ fueran dos elementos neutros, por + tendríamos que:
	$0=0+0'=0'$, por lo tanto si hay dos neutros, son iguales. Por esta razón, el neutro es una constante, tratándose de un valor único.
* $(I.4)$ Propiedad: $\forall x,y \in \mathbb{R}, x+y=0 \Leftrightarrow x=-y \Leftrightarrow y=-x$
	Gracias a esta propiedad, podemos demostrar todas las propiedades usuales del opuesto
	Consecuencias:
	1. $(-x+y)=(-x)+(-y)$
	2. $-(-x)=x$
	3. $-0=0$

## Propiedades del producto

* $x0=0x=0 \rightarrow$ el 0 es absorbente en la multiplicación.
	A continuación lo demostramos:$$
	\begin{aligned}
	0+0x=0x=(0+0)x=0x+0x \\
	0+0x-0x=0x+0x-0x \\
	0=0x
	\end{aligned}
	$$
	Es una consecuencia del resto de axiomas, por eso no hay uno específico para establecer dicha propiedad.
* $xy=0 \Leftrightarrow x=0 \lor y=0$
* $xy=1 \Leftrightarrow x=y^{-1} \Leftrightarrow y=x^{-1}$

Ejemplo aplicando las propiedades del producto:
$$
\begin{aligned}
(x+y)^{2} = (x+y)(x+y) = x(x+y) + y(x+y) \\
= xx+xy+yx+yy \\
= x^{2}+2xy+y^{2}
\end{aligned}
$$
Utilizamos el 2, pero no lo definimos:
Def: $2:=1+1,3:=2+1,4:=3+1,\dots$

Vamos a verificar que $xy+yx=2xy$
$$
\begin{aligned}
= xy+yx=xy+xy \\
= 1 \times xy + 1 \times xy \\
= (1+1) \times xy \\
= 2 \times xy
\end{aligned}
$$

También tenemos que definir el cociente, el cual se define de modo similar a la resta.

Def(cociente):
$x/y=\frac{x}{y} := x \times y^{-1} \space \space \space (\text{si } y \neq 0)$
Aclaramos que y no puede ser 0, ya que y no puede ser divisor, además de que no tiene inverso.

Consecuencias:
$\frac{x}{z}+\frac{y}{u} = \frac{xu}{zu} + \frac{yz}{uz} = \frac{xu+yz}{zu} \rightarrow \text{Reducción al mismo denominador}$
Esta regla no se cumple solo para los racionales, sino también para los reales.
Ejemplo: $\frac{1}{2}+\frac{1}{3}=\frac{3}{6}+\frac{2}{6}=\frac{5}{6}$

Anticipando sobre la existencia de la raíz cuadrada ($\sqrt{  }$):
$\frac{1}{\sqrt{ 2 }}+\frac{1}{\sqrt{ 3 }}=\frac{\sqrt{ 3 }}{\sqrt{ 2 } \times \sqrt{ 3 }}+\frac{\sqrt{ 2 }}{\sqrt{ 2 } \times \sqrt{ 3 }}=\frac{\sqrt{ 2 }+\sqrt{ 3 }}{\sqrt{ 6 }}=\frac{(\sqrt{ 2 }+\sqrt{ 3 }) \times \sqrt{ 6 }}{\sqrt{ 6 } \times \sqrt{ 6 }}=\frac{\sqrt{ 12 }+\sqrt{ 18 }}{6}$
De esta forma, la reducción al mismo denominador no solo involucra racionales, sino que también se puede usar en otros ámbitos.

## Interpretación geométrica de $+,\times,(-)^{-1}$

Trabajaremos sobre una recta para representar geométricamente cómo funciona cada una de las operaciones.
Para la suma no necesitamos conocer la unidad, ya que se trata de una operación lineal.
Para la suma utilizamos la construcción de paralelogramos, por la misma razón anterior, mientras que para el producto utilizamos triángulos, aplicando el Teorema de Tales.
![[Figura 2.png|697]]
![[Figura 3.png]]
Todo esto nos sirve para entender como los griegos veían y utilizaban las matemáticas, puesto que al no tener números, tenían que ingeniárselas con representaciones geométricas.
Es fundamental saber que dicha idea aplica para prácticamente todo en las matemáticas. De esta forma, cualquier operación o construcción se corresponde con una idea geométrica, lo que ayuda realmente a entender como se manejan internamente 

Por último, pasaremos a hablar del orden.

## Propiedades del orden

El primer axioma implica que $x \leq x$ o $x \leq x$, concluyendo en que $x \leq x$, siendo un caso particular dentro de la regla, aunque válido.
El tercer axioma es posiblemente el axioma de orden más importante, pues partimos de que $x \leq y \land y \leq x$, para concluir que $x=y$. Esto es super útil para demostrar igualdades de dos elementos, partiendo de la idea de que si se logra demostrar que el primero es menor o igual (o está contenido) al segundo, y viceversa, entonces los elementos son iguales.

<u>Def</u>: $x < y \Leftrightarrow x \leq y \land x \neq y$, de tal modo que: $x \leq y \Leftrightarrow x < y \lor x = y$

<u>Prop</u>:
* $x \not< x$
* $x<z \land y<x \implies x<z$ (no puede ser un sí y solo sí, puesto que no vamos a llegar a la misma idea si partimos del lado derecho)
* $x<y \oplus x=y \oplus x>y$

Sobre la implicación ($\implies$): cuando yo escribo "x implica y", digo que y es al menos tan verdadero como x. El falso implica el verdadero, pero no al revés, puesto que si un antecedente implica una consecuencia, y el antecedente es verdadero, la consecuencia tiene que ser verdadera. Sin embargo, puede pasar que el antecedente sea falso y la consecuencia verdadera, o que ambos sean falsos. Aclarar que la matemática no prohíbe el falso, es válido escribir cosas falsas, siempre y cuando sepamos que sean falsas, y que las formulas generales, ampliamente utilizadas, sean verdaderas.

Ahora, desarrollaremos algunas proposiciones en base a el axioma $(III.4) \space \space \space \forall z$
$$
\begin{aligned}
x \leq y \Longleftrightarrow x + z \leq y + z \\
\Longleftrightarrow x - z \leq y - z \\
\Longleftrightarrow -x \geq -y
\end{aligned}
$$
También aplica para las desigualdades estrictas:
$$
\begin{aligned}
x < y \Longleftrightarrow x + z < y + z \\
\Longleftrightarrow x - z < y - z \\
\Longleftrightarrow -x > -y
\end{aligned}
$$

Ahora veremos que pasa con el producto:
$$
\begin{aligned}
x \leq y \implies xz \leq yz \quad \forall z \geq 0 \\
\implies xz \geq yz \quad \forall z \leq 0
\end{aligned}
$$
Es fundamental verificar en que franja se encuentra z antes de establecer la desigualdad entre x e y.
$$
\begin{aligned}
x < y \implies xz < yz \quad \forall z > 0 \\
\implies xz > yz \quad \forall z < 0 \\
\implies xz = yz \quad si \space x=0
\end{aligned}
$$