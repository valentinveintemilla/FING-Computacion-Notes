Continuamos con el axioma de completitud de $\mathbb{R}$.
<u>Recordatorio</u>: Dados $A \subset \mathbb{R}, A\neq \emptyset, k \in \mathbb{R}$:
- $k=ínf(A) \Longleftrightarrow k \text{ es la cota inf de A más grande}$
- $k=sup(A) \Longleftrightarrow k \text{ es la cota sup de A más pequeña}$
La idea es que cuando tenemos un conjunto acotado, tenemos una serie de cotas inferiores, pero hay una que es mayor que todas las demás (ínfimo). Lo mismo aplica para la cotas superiores.

Completitud: $A \subset \mathbb{R}, A\neq \emptyset$
- Si A está acotado inferiormente, entonces tiene ínfimo.
- Si A está acotado superiormente, entonces tiene supremo.

Esto es el axioma de completitud, la propiedad más importante de los reales, puesto que define su textura. Esta propiedad establece que en $\mathbb{R}$ no hay agujeros, no faltan números (a diferencia de $\mathbb{Q}$).

# Razonamiento a menos de $\epsilon$
## Propiedad
Si $a\leq \text{ (o <) } b+ \epsilon \space (\forall \epsilon > 0)$, entonces $a\leq b$
La idea es agregar un "espacio" o "distancia" que nos facilita demostrar la desigualdad, puesto que el número mayor es un poco más grande al agregar $\epsilon$.

## Propiedad
Si $|a-b| \leq \text{ (o <) } \epsilon \space (\forall \epsilon > 0)$, entonces $a=b$
Si la distancia (valor absoluto) entre a y b es menor o igual (o menor), para todo $\epsilon$ positivo, entonces a=b.

A continuación, enunciaremos otras propiedades sobre los ínfimos y los supremos.

## Propiedad
Sea $A \subseteq \mathbb{R}, A \neq \emptyset$.
1. Si A tiene ínfimo (está acotado inferiormente, tiene cota inferior)
$\forall \epsilon > 0, \exists x \in A, \text{ ínf(A) } \leq x < \text{ ínf(A) + } \epsilon$
Básicamente, establece que siempre puede encontrar un elemento de A cuya distancia al ínfimo es menor que $\epsilon$, para cualquier $\epsilon$. Esto quiere decir que puedo aproximar el ínfimo por un elemento real de A, pero a distancia de $\epsilon$, y puedo elegir un $\epsilon$ cualquiera.
También existe una propiedad dual para el supremo:
![[Figura 1 - Propiedad ínfimo.png]]

2. Si A tiene supremo (está acotado superiormente, tiene cota superior)
$\forall \epsilon > 0, \exists x \in A, \text{ sup(A) - } \epsilon < x \leq \text{ sup(A)}$
Básicamente, se pone en espejo el dibujo anterior.

Vamos a demostrar las propiedades anteriores (solo la referente al ínfimo, ya que la otra es un espejo).
Aclarar que en el enunciado $\forall \epsilon > 0, \exists x \in A, \text{ ínf(A) } \leq x < \text{ ínf(A) + } \epsilon$, hay una desigualdad ($\text{ ínf(A) } \leq x$) que siempre se cumple. De esta forma, lo importante es demostrar la otra parte de la desigualdad.

Demostramos por el absurdo:
1. Por el absurdo, supongamos que
$\exists \epsilon > 0, \forall x \in A, x \geq \text{ ínf(A) + } \epsilon$ (negamos la desigualdad, sin incluir la parte que sabemos que se cumple).
Esto significa que $ínf(A) + \epsilon$ es una cota inferior de A, puesto que es menor o igual a todos los elementos de A. Pero ya sabemos que hay una cota inferior más grande que las otras, siendo el ínfimo.
Entonces: $ínf(A) + \epsilon \leq ínf(A)$. Si simplificamos, obtenemos que $\epsilon \leq 0$: contradicción
De esta forma, llegamos a una contradicción, puesto que habíamos partido de que $\epsilon > 0$

La demostración para el supremo es análoga.

Aquí tenemos prácticamente todas las herramientas que necesitamos conocer para utilizar el razonamiento "a menos de $\epsilon$" adecuadamente.
Continuamos analizando propiedades:

## Observación
Si $A \subset B \subset \mathbb{R}$, A y B acotados
¿Cómo se pueden relacionar los ínfimos y los supremos?
![[Figura 2 - Observación.png]]

Entonces: $ínf(B) \leq ínf(A) \leq sup(A) \leq sup(B)$

### Demostración
$ínf(B) \leq x \qquad \forall x \in B$.
La propiedad se cumple para todo x en B, y como A es un subconjunto de B, la propiedad aplica para todo x en A por inclusión.

entonces $ínf(B) \leq x \qquad \forall x \in A \text{ (por inclusión)}$
entonces $ínf(B) \text{ es cota inferior de } A$
Y como ínf(A) es la cota inferior de A más grande, tenemos que:

entonces $ínf(B) \leq ínf(A)$
Uso la propiedad de definición, que dice que el ínfimo de A, es la cota inferior más grande de A, estando a la derecha de el resto de las cotas inferiores de A.
De esta manera, demostramos la primer desigualdad. La última se demuestra de forma similar.
Cada vez que hacemos una demostración, una buena forma de trabajarla es entender cada paso de razonamiento realizado.

Por último, la igualdad central es obvia, puesto que aplica para todo conjunto (el ínfimo de conjunto siempre es menor o igual al supremo del mismo conjunto, siempre que el mismo sea no vacío).

Continuamos:

## Ejemplo
Sean $A,B \subset \mathbb{R}$ no vacíos y acotados. (A partir de estos, voy a definir la noción de suma de conjuntos). Se define:
$A+B=\{ x+y: x\in A, y \in B \}$
Conjunto resultante que incluye todas las combinaciones, sumas posibles, de elementos entre los conjuntos A y B.

Ejemplos:
$$
\begin{align}
&\{ a \} + \{ b \} = \{ a + b \} \text{ (cuando los dos conjuntos son reducidos a un punto)} \\
&\{ a, a' \} + \{ b, b' \} = \{ a + b, a + b', a' + b, a' + b' \}
\end{align}
$$
Por hipótesis, supusimos que los conjuntos son acotados. Se obtiene una cota superior, sumando dos cotas superiores. Si tomo una cota superior de A, y otra de B, su suma será cota superior de A + B. Lo mismo aplica para las cotas inferiores.

Entonces:
$$
\begin{align}
&ínf(A+B)=ínf(A)+ínf(B) \\
&sup(A+B)=sup(A)+sup(B)
\end{align}
$$
A continuación, demostramos la igualdad, buscando demostrar ambas desigualdades ($\leq$ y $\geq$):

### Demostración
Sea $z \in A+B$
existen $x \in A, y \in B$ tales que $z=x+y$
Tenemos que $ínf(A) \leq x, ínf(B) \leq y$
Entonces: $ínf(A) + ínf(B) \leq x+y = z$
Esta es una desigualdad que mostré para todo z, en el conjunto A+B. De esta forma, podemos deducir que la suma de los ínfimos es una cota inferior.

Entonces $ínf(A) + ínf(B) \text{ es cota inferior de } A + B$
Entonces $ínf(A) + ínf(B) \leq ínf(A + B)$

Logramos demostrar una desigualdad (la trivial, es la más sencilla de demostrar, simplemente siguiendo el desarrollo). Ahora debemos continuar con la otra.

Si intentamos proseguir directamente, nos encontramos con un problema:
$ínf(a+b) \leq x + y$
$x\geq ínf(A)$
$y\geq ínf(B)$
$ínf(a+b) \leq x + y \geq ínf(A) + ínf(B)$

¿Cómo podemos proseguir en este punto? Una solución puede ser agregar una distancia, razonando a menos de $\epsilon$:

Sea $\epsilon > 0$. Queremos mostrar que $ínf(A+B) \leq ínf(A) + ínf(B) + \epsilon$
La idea fundamental es que ya sabemos que podemos aproximar el ínfimo por un elemento de x a menos de $\epsilon$, de forma que ínf(A) es muy cercano a un elemento de A, y lo mismo para ínf(B) con un elemento de B, aunque no podemos decir que son iguales. Y el problema es que tenemos que usar un poco de distancia para ínf(A) y otro poco para ínf(B).
Entonces, lo que voy a hacer es dividir a $\epsilon$ en 2, para dar una parte a cada ínfimo.

- $\exists x \in A, x_{\epsilon} < ínf(A) + \frac{\epsilon}{2}$
- $\exists y \in B, y_{\epsilon} < ínf(B) + \frac{\epsilon}{2}$
Recordemos que esto funciona, puesto que $\epsilon$ puede tomar cualquier valor mayor que 0.

$ínf(A+B)\leq x_{\epsilon}+y_{\epsilon} < ínf(A) + ínf(B) + \epsilon$
Conclusión: $ínf(A+B)\leq ínf(A) + ínf(B)$

Necesitaba demostrar una desigualdad, y como la forma tradicional era demasiado complicada, utilicé el razonamiento a menos de $\epsilon$ para darme un poco de aire. Gracias a este espacio, pude reemplazar el ínfimo de A y B por una aproximación a menos de $\frac{\epsilon}{2}$.
Hay que entender lo que hicimos, puesto que trabajamos para todo $\epsilon$. El x e y manejados dependen de $\epsilon$, pues para cada $\epsilon$ encontré dos aproximaciones a menos de $\epsilon$ que dependían de $\epsilon$, una en A y otra en B.

También se puede demostrar sin $\epsilon$.

<u>Otra solución</u>:
Dado $x \in A:$
$$
\begin{align}
&ínf(A+B)\leq x+y \qquad (\forall y \in B) \\
&\implies ínf(A+B)-x\leq y \qquad (\forall y \in B) \\
&\text{De esta forma, podemos determinar que } ínf(A+B)-x \text{ es cota inferior de B, por lo que será menor o igual al ínfimo} \\
&\implies ínf(A+B)-x\leq ínf(B) \qquad (\forall x \in A) \\
&\implies ínf(A+B)-ínf(B)\leq x \qquad (\forall x \in B) \\
&\text{Por consecuente, podemos determinar que } ínf(A+B)-ínf(B) \text{ es cota inferior de A, por lo que será menor o igual al ínfimo} \\
&\implies ínf(A+B)-ínf(B)\leq ínf(A) \\
&\implies ínf(A+B)\leq ínf(A) + ínf(B)
\end{align}
$$
Esta es otra forma de demostrar lo anterior que no depende de $\epsilon$.

Para demostrar, es fundamental escribir los pasos de razonamiento, con el fin de comprender claramente cual es la lógica a seguir.

## Aplicación
<u>Existencia de la raíz cuadrada</u>.

<u>Teorema</u>: $\forall a \geq 0, \exists! b\geq_{0}, b^{2}=a$
(Todo número positivo o nulo tiene raíz cuadrada).

Nunca vimos ningún axioma para la raíz cuadrada, puesto que la raíz cuadrada no sale por argumentos algebraicos, sale por argumentos de completitud. Este teorema, muy general, nos da las raíces cuadradas de todos los números.
No demostraremos directamente el teorema, sino que vamos a demostrar dos lemas que sostienen el teorema.
Esta demostración no es trivial.

<u>Lema 1</u>: Dados $a,b > 0$
Si $b^{2} < a$, existe $\epsilon > 0$ tal que $(b+\epsilon)^{2}<a$. (Podemos agrandar b sumándole $\epsilon$, pero lo suficiente para que el cuadrado de $b+\epsilon$ siga siendo menor que a).

<u>Demostración</u>: Sea $\epsilon > 0$ tal que $\epsilon < b$ y $\epsilon < \frac{a-b^{2}}{3b}$
Verificamos que tal $\epsilon$ existe, y si, efectivamente existe un número menor que b y menor que $\frac{a-b^{2}}{3b}$.

Tenemos que
$$
\begin{align}
&(b+\epsilon)^{2}=b^{2}+2b\epsilon+\epsilon^{2} \\
&< b^{2}+2b\epsilon + b \epsilon \qquad (\text{pues } \epsilon < b) \\
&= b^{2}+3b \epsilon \\
&< b^{2} + \not 3b\left( \frac{a-b^{2}}{\not 3b} \right) \qquad (\text{pues } \epsilon < \frac{a-b^{2}}{\not 3b}) \\
&=b^{2}+(a-b^{2}) \\
&=a
\end{align}

$$
Logramos demostrar el lema 1, ya que llegamos al resultado $(b+\epsilon)^{2}<a$.

<u>Lema 2</u>: Dados $a,b > 0$
Si $b^{2}>a$, existe $\epsilon \in (0,b)$ tal que $(b-\epsilon)^{2}>a$.
Es decir, si el cuadrado de b es mayor que a, yo puedo reducir b sin perder la desigualdad.

<u>Demostración</u>: Sea $\epsilon=\frac{b^{2}-a}{2b}>0$
Por hipótesis, $b^{2}-a$ es positivo, y $2b$ también, por lo que $\epsilon > 0$.
Tenemos que verificar que $\epsilon = \frac{b^{2}-a}{2b} < b$

$$
\begin{align}
&\epsilon = \frac{b^{2}-a}{2b}< \frac{b^{2}}{2b} < \frac{2b^{2}}{2b} = b
\end{align}
$$
Aquí demostré dos cosas:
- $\epsilon > 0$
- $\epsilon < b$
De esta forma, es un buen candidato para la demostración.

$$
\begin{align}
&(b-\epsilon)^{2}=b^{2}-2b \epsilon + \epsilon^{2} \\
&=b^{2} - 2b \left(\frac{b^{2}-a}{2b} \right) + \epsilon^{2} \\
&=b^{2} - (b^{2}-a)+ \epsilon^{2} \\
&=\not b^{2} - \not b^{2} + a + \epsilon^{2} \\
&=a + \epsilon^{2} \\
&>a
\end{align}
$$
Logramos probar el lema 2, de forma que efectivamente $(b-\epsilon)^{2} > a$.

## Demostración del teorema
Yo quiero demostrar que existe y es único el b positivo o nulo, cuyo cuadrado es igual a a.

Sea $a \geq 0$

**(Unicidad)** Supongamos que $b, b' \geq 0 \text{ tal que } b^{2}=b'^{2} = a$
$(b+b')(b-b')=b^{2}-b'^{2}= a - a = 0$
Como el producto es nulo, uno de sus factores es nulo. Y si $b^{2}-b'^{2}$ es nulo, entonces $b^{2}$ y $b'^{2}$ son iguales.
Entonces, tenemos dos casos.

<u>2 casos</u>:
- $b+b' = 0 \implies b=b'=0$
- $b-b' = 0 \implies b=b'$
En ambos casos demostré que eran iguales. Si tengo dos números positivos o nulos que tienen el mismo cuadrado, entonces son iguales.

Ahora demostraremos la existencia por completitud.

**(Existencia)** Si $a=0$, basta con tomar $b=0$ (caso trivial)
Ahora, se supone que $a>0$.
Utilizando el teorema de completitud, la idea es construir un conjunto de aproximaciones de la raíz cuadrada.

Se define $B:=\{x>0;x^{2}<a\}$
De esta forma, podemos decir que el supremo de B es $\sqrt{ a }$, o lo que es lo mismo, $b$ (puesto que no hemos definido raíz cuadrada aún, evitaremos utilizarla). De esta forma, el límite de este conjunto a la derecha es la raíz cuadrada de a (o sea b).
Entonces, vamos a definir a la raíz cuadrada de a como el supremo de este conjunto.

Sin embargo, antes de proseguir tenemos que verificar dos cosas sobre este conjunto:
1. Que no es vacío ($B \neq \emptyset$)
2. Que tiene cota superior ($\exists y \in \mathbb{R}, \forall x \in B, x \leq y$)

- $B\neq 0$, pues: $\frac{a}{a+1}\in B$, ya que
$\left( \frac{a}{a+1} \right)^{2}=\frac{a^{2}}{a^{2}+2a+1 > a} < \frac{a^{2}}{a} = a$
Por inverso: $\frac{a^{2}}{a^{2}+2a+1 > a} < \frac{a^{2}}{a}$
Demostramos que  $\frac{a}{a+1}\in B$, así que nos queda demostrar que B tiene cota superior.

- B está acotado superiormente por $k:= máx(1,a)$
En efecto:
$$
\begin{align}
&x > máx(1,a) \\
&\implies x^{2}>1\times a = a \implies x \not \in B
\end{align}
$$
Como x es mayor que 1 y a a la vez, entonces el cuadrado de x es mayor que el producto de ambos elementos.

Por contrarrecíproco:
$$
x \in B \implies x \leq máx(1,a)
$$
De esta forma, determinamos que k es cota superior de B.
Ahora tenemos un conjunto no vacío y superiormente acotado.

Por completitud: Sea $b=sup(B)$
Queremos demostrar que $b^{2}=a$
Tenemos tres casos posibles, la idea es demostrar que únicamente el caso de igualdad es posible.

Tres casos posibles:
- $b^{2}<a$
- $b^{2}=a$
- $b^{2}>a$

**Caso $b^{2}<a$**
Por el lema 1, $\exists \epsilon > 0, (b+ \epsilon)^{2} < a$
$\implies b+\epsilon \in B \implies b+\epsilon \leq sup(B) = b$
$\implies \epsilon \leq 0: \text{contradicción}$
Caso imposible

**Caso $b^{2}>a$**
Por el lema 2, $\exists \epsilon \in (0,b) \text{ tal que } (b-\epsilon)^{2} > a$
Como $b=sup(B), \exists x \in B \text{ tal que}$
$$
\begin{align}
&x>sup(B)-\epsilon \\
&x>b-\epsilon \\
&a > x^{2}>(b-\epsilon)^{2} > a \\
&a \implies a
\end{align}
$$
Caso imposible, volvimos a llegar a una contradicción, pues $a \not \geq a$.

En conclusión, el único caso posible es $b^{2}=a$. Con esto, demostramos que la raíz cuadrada existe.

