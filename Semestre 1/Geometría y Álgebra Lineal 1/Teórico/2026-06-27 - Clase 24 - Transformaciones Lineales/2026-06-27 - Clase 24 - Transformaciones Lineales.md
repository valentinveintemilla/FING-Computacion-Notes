# Espacios vectoriales

Comenzamos repasando la suma de subespacios vectoriales (visto la clase anterior):
## Suma de subespacios vectoriales
$$
S, T \underset{sev} \subset V \qquad S + T = \{ v + w : v \in S, w \in T \}
$$
Hay que encenderla como una unión extendida con combinaciones lineales.

Si sumamos un espacio a si mismo, obtenemos el mismo espacio. Este es un "caso borde".

El otro caso borde es la suma de dos espacios vectoriales que no tienen nada en común (a excepción del vector nulo): suma directa.

Suma directa $S \oplus T$ cuando
$$
(A u \in S + T)(\exists! \space v \in S)(\exists! \space w \in T)(u = v + w)
$$

La operación es exactamente la misma, simplemente es una caracterización (un caso particular).

> [!Proposición]
> Una suma $S + T$ es directa $\Longleftrightarrow S \cap T = \{ \vec{0} \}$

Cuando sumamos espacios de diferentes dimensiones, tenemos varios casos posibles:
- Como mínimo se obtendrá un espacio que tenga dimensión como el espacio de mayor dimensión (en caso de que el de menor dimensión esté contenido dentro).
- Se obtendrá un espacio de dimensión igual a la suma entre las dimensiones de ambos, menos las dimensiones en común.
- Se obtendrá un espacio de dimensión igual a la suma entre las dimensiones de ambos (si no tienen nada en común aparte del vector nulo).

En base a esto, habíamos definido una proposición:

> [!Proposición]
> Si $A$ es una base de $S$ y $B$ es una base de $T$, entonces $A \cup B$ es una base de $S \oplus T$ (solo en caso de suma directa, pueso que cualquier par de bases elegido es disjunto).

También vimos que:

> [!Corolario]
> En caso de suma directa:
> $$
> dim(S \oplus T) = dim(S) + dim(T)
> $$
> Caso general:
> $$
> máx(dim(S), dim(T)) \leq dim(S + T) \leq dim(S) + dim(T)
> $$


Ahora, veremos un ejemplo:
### Ejemplo
$$
V = \mathcal{M}_{n \times n} \qquad (n \geq 1)
$$
$$
\begin{align}
&S = \{ A \in \mathcal{M}_{n \times n} : A^{t} = A \} \underset{sev} \subset V \\
&T = \{ A \in \mathcal{M}_{n \times n} : A^{t} = -A \} \underset{sev} \subset V
\end{align}
$$
Queremos determinar $S + T$. ¿La suma es directa?

Para deterimar si es directa o no, tenemos que considerar la intersección. Buscamos una matriz que sea a la vez simétrica y antisimétrica.

Sea $A \in S \cap T : A^{t} = A \text{ y } A^{t} = -A$
$$
\implies A = -A \implies 2A = O \implies A = O
$$
Entonces, determinamos que la suma es directa: $S \oplus T$.

Ahora, queremos saber cual es el espacio formado. Demostraremos que la suma $S + T$ compone todo el espacio de las matrices, lo que demuestra que cualquier matriz se puede conformar por combinación lineal de matrices simétricas y antisimétricas.

Queremos demostrar que:

Proposición:
$$
S \oplus T = \mathcal{M}_{n \times n}
$$

En efecto, si $A \in \mathcal{M}_{n \times n}$:
$$
A = \underbrace{ \frac{1}{2}(A + A^{t}) }_{ A^{+} } + \underbrace{ \frac{1}{2}(A - A^{t}) }_{ A^{-} }
$$
Se observa que
$$
(A^{+})^{t} = \left( \frac{1}{2}(A + A^{t}) \right)^{t} = \frac{1}{2}(A^{t} + A^{\cancel{ tt }}) = A^{+}
$$
Luego $A^{+} \in S$ (simétrica).
$$
(A^{-})^{t} = \left( \frac{1}{2}(A - A^{t}) \right)^{t} = \frac{1}{2}(A^{t} - A^{\cancel{ tt }}) = -A^{-}
$$
Luego $A^{-} \in S$ (antisimétrica).

Entonces, logramos demostrar que cualquier matriz se puede descomponer como la suma de una matriz simétrica y otra antisimétrica. Funciona para matrices de cualquier tamaño, ya que la demostración es genérica.

De esta forma:
$$
S \oplus T = \mathcal{M}_{n \times n}
$$

Sin embargo, es importante clarificar que este razonamiento no se cumple en $Z_{2}$, ya que al realizar $\frac{1}{2}$ dividimos entre 0 (recordemos que el nulo en $\mathbb{Z}_{2}$ es 0). En general, no funciona para ningun cuerpo con tal característica.

O sea, $S \oplus T$ cuando $2_{\mathbb{K}} \neq 0_{\mathbb{K}}$.

Incluso, en cualquier cuerpo donde $2 = 0$, se cumple que $1 = -1$, por lo que las matrices simétricas y las antisimétricas son iguales. En general, hay errores en cualquier lugar donde aparece el 2.

Entonces, el resultado no funciona para todos los cuerpos. A veces, es importante cuidar en que cuerpo se trabaja.

Los cuerpos finitos, como el mencionado, se utilizan mucho en criptografía.

---
Pasaremos a estudiar el último tema del curso:
# Transformaciones lineales
Ahora, veremos el verdadero potencial de los espacios vectoriales.

#Definición 
> [!Transformaciones lineales - Definición]
> Sean $V, W$ dos espacios vectoriales sobre el mismo cuerpo $\mathbb{K}$.
> 
> Una función $T : V \to W$ es una <u>transformación lineal</u> cuando
> $$
> \begin{align}
> &1. &&T(u +_{V} v) = T(u) +_{W} T(v) &&(u, v \in V) \\
> &2. &&T(\alpha \cdot_{V} u) = \alpha \cdot_{W} T(u) &&(\alpha \in \mathbb{K}, u \in V) \\
> \end{align}
> $$

Entonces, (1) transforma sumas de un primer espacio en sumas de un segundo espacio y (2) transforma productos por un escalar de un primer espacio en productos por un escalar de un segundo espacio (el escalar se mantiene constante, razón por la cual es necesario que los espacios compartan el mismo cuerpo).

Es fundamental, ya que corresponde a todos los fenómenos físicos sencillos. Se generaliza el comportamiento de transformación entre espacios diferentes que trabajan sobre el mismo contexto (cuerpo). Por ejemplo, si queremos calcular la transformación de una gran suma, podemos transformar cada componente y sumar los resultados.

Esto nos lleva a una proposición:

#Proposición 
> [!Proposición]
> Si $T : V \to W$ es una transformación lineal, entonces:
> $$
> T(\vec{0}) = \vec{0} \text{ y } T(-u) = -T(u)
> $$
> Más generalmente:
> $$
> T(\alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n}) = \alpha_{1} \cdot T(u_{1}) + \dots + \alpha_{n} \cdot T(u_{n})
> $$

Muchos fenómenos físicos son lineales, permitiendo pasar el comportamiento del nivel microscópico al nivel macroscópico, asegurando la estabilidad siempre.

Ahora, veremos algunos ejemplos de transformaciones (funciones) lineales:
## Ejemplos

1. $T : \mathbb{R}^{3} \to \mathbb{R}$ definida por $T(x, y, z) = 3x - 5y + 2z$
Verificamos que se trate de una transformación lineal (solo para la suma):
$$
\begin{align}
T((x, y, z) +_{\mathbb{R}^{3}} (x', y', z')) &= T(x + x', y + y', z + z') \\
&= 3(x + x') - 5(y + y') + 2(z + z') \\
&= \underbrace{ (3x - 5y + 2z) }_{ T(x, y, z) } + \underbrace{ (3x' - 5y' + 2z') }_{ T(x', y', z') }
\end{align}
$$
También funciona para el producto por un número: $T(\alpha \cdot u) = \alpha \cdot T(u)$.

Entonces, comprobamos que se trata de una transformación lineal.

En general las transformaciones lineales que estudiaremos tienen la forma anterior: una constante por la primera variable mas otra constante por la segunda variable, etc.

2. $T : \mathbb{R}^{3} \to \mathbb{R}$ definida por $T(x, y, z) = 2xyz$
Veremos que esta no es una transformación lineal:
$$
\begin{align}
&T(1, 1, 1) = 2 \\
&T(2, 2, 2) = 16 \neq 2T(1, 1, 1)
\end{align}
$$
Es así que, de una forma sencilla, demostramos que no es una transformación lineal. Muchas veces se puede ver mediante el producto.

Un ejemplo sencillo es la función cuadrado: un claro ejemplo de función lineal (al menos en $\mathbb{R}$):
$$
(x + y)^{2} = x^{2} + 2xy + y^{2} \neq x^{2} + y^{2}
$$
Sin embargo, es lineal en $\mathbb{Z}_{2}$.

3. $T : Der([a, b]) \to \mathbb{R}^{[a, b]}$.
La operación que definiremos es:
$$
f \mapsto f'
$$
(Transforma cada función derivable en su derivada).

Es fácilmente verificable que se trata de una transformación lineal, ya que $T(f + g) = f' + g'$ y $T(\alpha f) = \alpha T(f) = \alpha f'$.

$\mathbb{R}^{[a, b]}$ significa todas las funciones definidas como $f : [a, b] \to \mathbb{R}$.

4. $T : \mathcal{C}^{\circ}([a, b]) \to \mathbb{R}$
Definida por la operación:
$$
f \mapsto \int_{a}^{b} f
$$
La integral de una suma de funciones se puede expresar como la suma de las integrales, y la integral de una constante por una función permite extraer la constante de la integral.

De esta manera, vimos que la derivación y la integración son dos transformaciones lineales.

Normalmente, cuando trabajamos con integrales y derivadas, descomponemos en trozos y sumamos cada resultado. Entonces, aplicamos la propiedad de linealidad, ya que al tratarse de funciones lineales, nos podemos permitir dicha virtud.

5. $T : \mathcal{C}^{\circ}([0, 2]) \to \mathbb{R}$
$$
f \mapsto f(\sqrt{ 2 })
$$
$$
(f + g)(\sqrt{ 2 }) = f(\sqrt{ 2 }) + g(\sqrt{ 2 })
$$
$$
(\alpha \cdot f)(\sqrt{ 2 }) = \alpha \cdot f(\sqrt{ 2 })
$$

Entonces, es una transformación lineal.

Existen muchos más ejemplos tradicionales, pero proseguiremos con el tema. Ahora, estudiaremos una proposición fundamental:

#Proposición 
> [!Proposición]
> Una función $T : V \to W$ es una transformación lineal si y sólo si $\forall \alpha_{1}, \dots, \alpha_{n} \in \mathbb{K}, \forall u_{1}, \dots, u_{n} \in V$:
> $$
> T(\alpha_{1} \cdot u_{1} + \dots + \alpha_{n} \cdot u_{n}) = \alpha_{1} \cdot T(u_{1}) + \dots + \alpha_{n} \cdot T(u_{n})
> $$

Entonces, una transformación lineal es tal, si transforma cada combinación lineal de vectores del espacio $V$ en la misma combinación lineal de las imágenes de los vectores en el espacio de llegada.

Combina la suma y el producto en un único enunciado.

Entonces, tenemos dos opciones cuando consideramos funciones entre espacios vectoriales:
1. Preservan todas las combinaciones lineales, siendo transformaciones lineales.
2. Algunas combinaciones lineales no se preservan, perdiendo la propiedad de transformaciones lineales

Proseguiremos con algunos ejemplos, ahora con matrices:
## Ejemplos (continuación)

6. $(A \mapsto A^{t}) : \mathcal{M}_{n \times n} \to \mathcal{M}_{n \times n}$
En este caso, la traspuesta de una suma es igual a la suma de las traspuestas, y la traspuesta de una matriz por un número es el número por la traspuesta de la matriz. De esta forma, es una transformación lineal.

Si probáramos con la inversa, podremos ver que no está definida sobre el vector nulo, ya que no tiene inversa. De esta forma no es una transformación lineal.

7. $(A \mapsto \det(A)): \mathcal{M}_{n \times n} \to \mathbb{R}$
El determinante de la matriz nula es 0, por lo que se verifica dicha característica. Sin embargo, no podemos decir lo mismo para la suma: $\det(A + B) \neq \det(A) + \det(B)$.

Entonces, no es una transformación lineal.

---
Ahora, pasaremos a ver caracterizaciones de transformaciones lineales en una base:

## Proposición

#Proposición
> [!Proposición]
> Sean:
> - $V, W$ espacios vectoriales sobre $\mathbb{K}$
> - $S, T : V \to W$
> - $\{ v_{1}, \dots, v_{n} \} \subset V$ base de $V$
> 
> Entonces
> $$
> S(c_{1}) = T(v_{1}) \text{ y } \dots \text{ y } S(v_{n}) = T(v_{n}) \Longleftrightarrow S = T
> $$

Observamos que $S$ y $T$ coinciden con todos los vectores de base. De esta forma, se puede asumir que $S$ y $T$ son la misma función, ya que como cualquier vector del espacio se forma por combinación lineal de estos vectores, por combinación lineal la imagen de cualquier vector por la primer función será igual a la imagen del mismo vector por la segunda función. El recíproco es trivial, lo interesante es la implicación directa.

### Demostración
$(\impliedby)$: obvio

$(\implies)$: Supongamos que $S(v_{i}) = T(v_{i})$ para todo $i \in \{ 1, \dots, n \}$.

Sea $u \in V$ cualquiera. Existen $\alpha_{1}, \dots, \alpha_{n} \in \mathbb{K}$ tales que $u = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}$. Luego:
$$
\begin{align}
S(u) &= S(\alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}) \\
&= \alpha_{1} \cdot S(v_{1}) + \dots + \alpha_{n} \cdot S(v_{n}) \\
&= \alpha_{1} \cdot T(v_{1}) + \dots + \alpha_{n} \cdot T(v_{n}) \\
&= T(\alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}) \\
&= T(u)
\end{align}
$$

Entonces, para todo vector $u$, $S(u) = T(u)$. En conclusión: $S = T$.

La observación es que, aprovechamos la propiedad de generador de la base en la proposición, para demostrar que, como se puede generar todo el espacio con esos vectores y las transformaciones de ambas funciones son equivalentes, entonces son iguales. La parte libre de la base nunca fue mencionada.

La proposición anterior es interesante, ya que implícitamente enuncia que para conocer una transformación lineal sobre un espacio, simplemente tenemos que conocer la transformación lineal sobre una de sus bases, cosa que es muchísimo más sencilla. De esta forma, para determinar una función sobre un espacio vectorial de dimensión $n$, solo es necesario conocer $n$ valores.

No llegaremos a verlo en el curso, pero el objeto que se utiliza para representar cualquier transformación lineal es una matriz, a la cual le llamamos matriz asociada.

==Para conocer una transofmración lineal definida en un espacio vectorial de dimensión $n$, sólo hay que conocer $n$ valores (sobre una base)==. Entonces, las transformaciones lineales tienen información finita.

Ahora, pasaremos a ver otra propiedad

## Proposición (Caracterización de una transformación lineal en una base)

#Proposición 
> [!Proposición (Caracterización de una transformación lineal en una base)]
> Sean:
> - $V, W$ espacios vectoriales sobre $\mathbb{K}$
> - $\{ v_{1}, \dots, v_{n} \} \subset V$ base de $V$ ($dim(V) = n$)
> - $w_{1}, \dots, w_{n} \subset W$ vectores cualesquiera
> 
> Entonces, existe una única transformación lineal $T : V \to W$ tal que:
> $$
> T(v_{1}) = w_{1} \text{ y } \dots \text{ y } T(v_{n}) = w_{n}
> $$

Demostramos que existe una transformación lineal que transforma $v_{1}$ en $w_{1}$, $\dots$, $v_{n}$ en $w_{n}$, y dicha transformación lineal es única.

Entonces, solo fue necesario definir una cantidad finita de transformaciones para determinar una función, necesitando una base del primer espacio, y asociar a cada vector de la base un vector cualquiera del segundo espacio (podrían ser todos iguales, diferentes, no importa).

### Demostración
Sabemos que la transformación es única (unicidad), por la proposición anterior (si dos transformaciones lineales comparten las mismas transformaciones sobre una base, entonces son idénticas).

Unicidad: por la proposición anterior.

Ahora, pasamos a la existencia.

Existencia: sea $B = \{ v_{1}, \dots, v_{n} \}$ la base fijada de $V$.

Sea $v \in V$ cualquiera.
Sean $(\alpha_{1}, \dots, \alpha_{n}) = coord_{B}(v)$.

Tenemos que $v = \alpha_{1} \cdot v_{1} + \dots + \alpha_{n} \cdot v_{n}$

Se define $T(v) = \alpha_{1} \cdot w_{1} + \dots + \alpha_{n} \cdot w_{n} \qquad \in W$

Queda verificar que $T$ es una transformación lineal (Ejercicio).

---
Pasaremos a ver otros ejemplos de transformaciones lineales:
### Ejemplo
Sea $T : \mathbb{R}^{2} \to \mathbb{R}^{3}$ definida por
$$
T(1, 2) = (3, -1, 5) \text{ y } T(0,1) = (2, 1, -1)
$$
Los pares $(1, 2)$ y $(0, 1)$ forman una base de $\mathbb{R}^{2}$ ($\{ (1, 2), (0, 1) \}$ es base), por lo que la transformación lineal está bien definida.

Entonces, podemos hallar la formula general $T(x, y)$:
$$
\begin{align}
T(1, 0) &= T(1, 2) - 2T(0, 1) \\
&= (3, -1, 5) - 2(2, 1, -1) \\
&= (3, -1, 5) - (4, 2, -2) \\
&= (3 - 4, -1 - 2, 5 + 2) \\
&= (-1, -3, 7)
\end{align}
$$
Entonces, podemos definir a
$$
\begin{align}
T(x, y) &= xT(1, 0) + yT(0, 1) \\
&= x(-1, -3, 7) + y(2, 1, -1) \\
&= (-x, -3x, 7x) + (2y, y, -y) \\
&= (-x + 2y, -3x + y, 7x - y)
\end{align}
$$
En conclusión:
$$
T(x, y) = (-x + 2y, -3x + y, 7x - y)
$$

Aquí el método desarrollado por el docente:

De esta forma, lo que hicimos fue descomponer el vector $(x, y)$ en la base $B$;
$$
\begin{align}
(x, y) &= \alpha(1, 2) + \beta(0, 1) \\
&= (\alpha, 2\alpha + \beta)
\end{align}
$$
$$
\begin{cases}
\alpha = x \\
2\alpha + \beta = y
\end{cases}
$$
$$
\alpha = x \implies \beta = y - 2\alpha = y - 2x
$$

Entonces:
$$
(x, y) = x(1, 2) + (y - 2x)(0, 1)
$$
Ahora, podemos determinar $T(x, y)$:
$$
\begin{align}
T(x, y) &= T(x(1, 2) + (y - 2x)(0, 1)) \\
&= x(3, -1, 5) + (y - 2x)T(2, 1, -1) \\
&= (3x + 2y - 4x, -x + y - 2x, 5x - y + 2x) \\
&= (-x + 2y, -3x + y, 7x - y)
\end{align}
$$

Concluimos probando que, simplemente teniendo una base del primer espacio de la transformación lineal y las transformaciones de cada elemento, es posible determinar la forma general de la transformación.