Esta será la última clase del capítulo de números reales.
# Números reales
La vez pasada recordamos el axioma de completitud, viendo que es el motor de los números reales, el que define la textura. Además, vimos el razonamiento "a menos de épsilon" para demostrar igualdades y desigualdades.
También demostramos el siguiente teorema (asegurando la existencia y unicidad de la raiz cuadrada).

Teorema:
$$
\forall x \geq 0, \space
\exists! y \geq 0, \space y ^{2} = x
$$
Notación: $y:= \sqrt{ x }$
De esta forma, tenemos la raíz cuadrada de cualquier número real, y admitimos que la función existe ya que demostramos su existencia.
Para concluir con esto, tenemos (por construcción) que: $\sqrt{ x } \geq 0$ y $(\sqrt{ x })^{2} \geq x$

Continuamos con intervalos

# Los 10 tipos de intervalos

**Definición de Intervalo**
Un conjunto $I \subset \mathbb{R}$ es un <u>intervalo</u> si $\forall x, y \in I, \forall z \in \mathbb{R}, x \leq z \leq y \implies z \in I$
Es decir, cada vez que tomo dos puntos en un intervalo, todos los puntos intermedios también forman parte del intervalo. Es la definición más abstracta de intervalo.
Lo bueno es que en $\mathbb{R}$ ya sabemos categorizar todos los intervalos, y son los mismos que ya vimos antes, de forma que no hay otros tipos de intervalos.

## Teorema
Si $I \subset \mathbb{R}$ es un intervalo de $\mathbb{R}$, entonces o bien
$$
\begin{align}
&1. \space I \neq \emptyset \\
&2. \space I=[a,b], \text{ con } a \leq b \\
&3. \space I=[a,b), \text{ con } a < b \\
&4. \space I=(a,b], \text{ con } a < b \\
&5. \space I=(a,b), \text{ con } a < b \\
&6. \space I=(-\infty,a], \text{ con } a \in \mathbb{R} \\
&7. \space I=(-\infty,a), \text{ con } a \in \mathbb{R} \\
&8. \space I=[a,+\infty), \text{ con } a \in \mathbb{R} \\
&9. \space I=(a,+\infty), \text{ con } a \in \mathbb{R} \\
&10. \space I=(-\infty,+\infty) = \mathbb{R}
\end{align}
$$Si bien partimos de una definición abstracta, gracias al teorema anterior sabemos que un intervalo si o si pertenece a una de las formas anteriores, cosa que también se puede demostrar.
Lo primero que hay que mencionar es que la definición abstracta anterior se corresponde con los tipos establecidos.
Un detalle sobre la notación es que nosotros utilizamos la notación inglesa, la cual tiene un pequeño problema: la notación para intervalo abierto es la misma que para par ordenado: $(a,b) \text{ Intervalo } \neq (a,b) \text{ Par ordenado }$. Por esta razón, también se puede utilizar $<a,b>$ para designar un par ordenado, aunque no la utilizaremos.
La notación francesa soluciona este problema:
$$
\begin{align}
&[a,b] \text{ Notación inglesa } = [a,b] \text{ Notación francesa } \\
&[a,b) \text{ Notación inglesa } = [a,b[ \text{ Notación francesa }
\end{align}
$$
De esta forma, se utiliza el paréntesis recto al revés para designar un intervalo abierto.

Ahora demostraremos que si $I$ cumple la condición establecida en la definición, entonces tiene una de las 10 formas especificadas.

## Demostración
Se observa que $\emptyset$ es un intervalo. En este caso no hay nada que verificar, puesto que cuando especifico algo $\forall x, y \in \emptyset$, sabemos que se cumple. De esta forma, $\emptyset$ es un intervalo.
Ahora se supone que $I \neq \emptyset$. Ahora tenemos que demostrar que $I$ es de una de las nueve formas que quedan.
Se distinguen 4 casos:
La primera pregunta que puedo hacer es si $I$ esta acotado (ya sea superior o inferiormente).
1. $I$ está acotado inferior y superiormente.
2. $I$ está acotado superiormente, pero no inferiormente.
3. $I$ está acotado inferiormente, pero no superiormente.
4. $I$ no está acotado superiormente, ni inferiormente ni superiormente.

Esto nos divide el campo de investigación, de forma que las 10 categorías se separan en estos casos.

**Caso (1)**:
$I$ está acotado (si no se especifica nada más, significa que está acotado inferiormente y superiormente).
Sea $a := ínf(I)$ y $b := sup(I)$
Por construcción:
- $a \leq b$
- $I \subset [a,b]$ (no hay elementos de $I$ por debajo de a ni encima de b)

<u>Aclaración</u>: Nosotros usamos $\subset$ como si fuera $\subseteq$ (generalmente).

Demostraremos que como $I$ es un intervalo con una propiedad particular, contiene a todos sus elementos entre a y b excluidos.

Ahora, demostremos que $(a,b) = ]a,b[ \subset I (\subset [a,b])$.

Demostramos $(a,b) \subset I$
Sea $x \in (a,b)$ cualquiera
Por hipótesis: $a < x < b$

No sabemos si a y b pertenecen a $I$ o no, pues se trata del ínfimo y del supremo.
Para demostrar que x está en $I$, utilizaremos la propiedad del ínfimo, supremo y la propiedad de $I$.
A través de aproximación al ínfimo y supremo a menos de $\epsilon$.

- Como $a=ínf(I)$, existe $y \in I$ tal que $a = ínf(I) < y < x$ (Tomando $\epsilon = x-a > 0$).
Tomamos un x que no sabemos si pertenece a $I$, pero sabemos que y pertenece, ya que al utilizar la distancia $\epsilon$, estoy seguro de que el valor obtenido estará entre a y x.

De modo análogo, podemos realizar el mismo razonamiento para b:
- Como $b=sup(I)$, existe $y' \in I$ tal que $x < y' < b = sup(I)$ (Tomando $\epsilon' = b-x > 0$).

Al final, obtenemos que $y \in I < x < y' \in I$.
Por lo tanto: $x \in I$, pues $I$ es un intervalo por definición.

Conclusión:
$$
(a,b) \subset I \subset [a,b]
$$
De esta forma, los puntos dudosos son a y b, de forma que obtenemos los cuatro casos acotados de 2 al 5, cubriendo el caso 1 ($I$ está acotado inferior y superiormente).

La propiedad utilizada es la aproximación al ínfimo y supremo por $\epsilon$, la cual establece que si tengo un ínfimo o un supremo, puedo aproximar a menos de $\epsilon$ al mismo, quedándome dentro del conjunto.

Luego:
- o bien $I = [a,b]$
- o bien $I = [a,b) = [a,b[$
- o bien $I = (a,b] = ]a,b]$
- o bien $I = (a,b) = ]a,b[$

Las demostraciones para el resto de casos se realizan de forma similar. Sin embargo, el argumento sobre que un intervalo es no acotado es la negación de propiedad de estar acotado.

Para demostrar algo, es fundamental redactarlo, no solo escribir una sucesión de símbolos matemáticos. Si no se entiende cual es el razonamiento y lógica internos, la demostración no tiene sentido.

## Ejemplo
Sea $I = \{ x \in \mathbb{R}: x > 0 \land x^{2} < 2 \}$
Este conjunto es un intervalo, ya que si tomo dos puntos en este conjunto, todo punto entre esos dos puntos pertenecen a $I$.
Si $x,y \in I$ entonces $\forall z \in \mathbb{R}, x\leq z \leq y \implies z \in I$. Sabemos que como z se encuentra entre x e y, elementos que pertenecen a $I$, cumpliendo sus propiedades adecuadamente, entonces también aplican para z, por lo que también pertenece a $I$.

Tenemos que $I$ tendrá necesariamente una de las siguientes formas:
$$
\begin{align}
&I=[a,b] \\
&I=(a,b] \\
&I=[a,b) \\
&I=(a,b) \\
&\text{Con } a = ínf(I) = 0 \text{ y } b = sup(I) = \sqrt{ 2 } \\ \\

&\text{Si analizamos cuidadosamente las condiciones que definien a } I \text{, podemos llegar a la conclusión de que:} \\
&I=(0,\sqrt{ 2 })=]0,\sqrt{ 2 }[ \\
\end{align}
$$

¿Qué pasa si hubiésemos hecho lo mismo en $\mathbb{Q}$ en lugar de $\mathbb{R}$?
De esta forma $I$ sería un conjunto de racionales bien definidos, pero no entra en ninguna de las formas definidas anteriormente. ¿Por qué no se puede resolver? Porque no tenemos el supremo. Esto se llama un intervalo patológico (por que no entra en ninguna categoría).

Vamos a ver que pasaría si incluimos raíz de 2 en $I$.
$$
\begin{align}
&I_{0} = \{ x \in \mathbb{Q}: x > 0 \land x^{2} < 2 \} \\
&I_{1} = \{ x \in \mathbb{Q}: x > 0 \land x^{2} \leq 2 \} \\
&I_{0} = I_{1}
\end{align}
$$
Los dos conjuntos anteriores son iguales, puesto que no hay ningún racional cuyo cuadrado sea 2.
Sin embargo, si reemplazo $\mathbb{Q}$ por $\mathbb{R}$, ya no son más iguales, puesto que ahora $I_{2}$ tiene máximo y es $\sqrt{ 2 }$.
Como es un intervalo que no entra en ninguna de las categorías anteriores, no lo consideramos "correcto", de forma que solo se puede escribir en $\mathbb{R}$, y es en este sentido que se considera que $\mathbb{R}$ es una compleción de $\mathbb{Q}$.

# Consecuencias del axioma de completitud
Vamos a ver dos consecuencias importantes en esta sección.

**Definición (Sucesión)**: Una sucesión es una función $u: \mathbb{N} \to A$ escrita $u=(u_{n})_{n \in \mathbb{N}}$. Básicamente, es una función que tiene como dominio a $\mathbb{N}$.
Todas las cosas que se cumplen para las funciones, también se cumplen para las sucesiones (pues son funciones particulares).

<u>Notaciones</u>:
$$
\begin{align}
&u = (u_{n})_{n \in \mathbb{N}} \\
&u(n) = u_{n}
\end{align}
$$

## Teorema (Principio de los intervalos cerrados encajados)
Supongo que tengo una recta real, de la que tomo un primer intervalo $[a_{0},b_{0}]$, dentro del cual defino otro intervalo $[a_{1},b_{1}]$, y continuo de esta manera hasta infinito. De esta forma, tengo una sucesión infinita de intervalos encajados.
![[Principio de los intervalos cerrados encajados.png]]

Si $[a_{n}, b_{n}]_{n \in \mathbb{N}}$ es tal que $[a_{n+1}, b_{n+1}] \subset [a_{n}, b_{n}]$  $(\forall n \in \mathbb{N})$.
Entonces $\cap_{n \in \mathbb{N}} [a_{n}, b_{n}] \neq \emptyset$, de modo que existe al menos un punto adentro.

### Demostración
Por hipótesis
$a_{n} \leq a_{n+1} \leq b_{n+1} \leq b_{n} (\forall n \in \mathbb{N})$
$(a_{n})_{n \in \mathbb{N}}$ creciente, $(b_{n})_{n \in \mathbb{N}}$ decreciente

Más generalmente: $\forall n, m \in \mathbb{N}$
$a_{n} \leq a_{máx(n,m)} \leq b_{máx(n,m)} \leq b_{m}$
Esto establece que todos los $a_{n}$ son menores que todos los $b_{n}$. De esta forma, como cualquier termino de la sucesión $(a_{n})_{n \in \mathbb{N}}$ es menor o igual a cualquier termino de la sucesión $(b_{n})_{n \in \mathbb{N}}$, entonces todos los elementos de $(a_{n})_{n \in \mathbb{N}}$ son cota inferior de $(b_{n})_{n \in \mathbb{N}}$. De forma análoga, todos los elementos de $(b_{n})_{n \in \mathbb{N}}$ son cota superior de $(a_{n})_{n \in \mathbb{N}}$. Esto nos permite obtener el supremo e ínfimo de la intersección.

Sean
$$
\begin{align}
&a:= sup \{ a_{n}:n \in \mathbb{N} \} \\
&b:= ínf \{ b_{m}:m \in \mathbb{N} \}
\end{align}
$$
Podemos decir que a siempre es menor o igual a b.
Se demuestra de la siguiente forma:
- Tomo algún $a_{n}$
- Observo que $a_{n}$ es menor o igual a todos los $b_{m}$, entonces es una cota inferior del conjunto $\{ a_{n}:n \in \mathbb{N} \}$.
- De esta forma, $a_{n} \leq ínf \{ b_{m}:m \in \mathbb{N} \}$
- Pero esto se cumple para todos los n.
- Entonces, $ínf \{ b_{m}:m \in \mathbb{N} \}$ es una cota superior del conjunto $\{ b_{m}:m \in \mathbb{N} \}$.
- En conclusión, $sup \{ a_{n}:n \in \mathbb{N} \} \leq ínf \{ b_{m}:m \in \mathbb{N} \}$

Entonces, por construcción, tenemos que
$$
\begin{align}
&a_{n} \leq a = sup \{ a_{n}:n \in \mathbb{N} \} \leq b = ínf \{ b_{m}:m \in \mathbb{N} \} \leq b_{n} \text{, } \forall n \in \mathbb{N} \\
&[a,b] (\neq \emptyset) \subset [a_{n}, b_{n}] \\
&[a,b] (\neq \emptyset) \subset \cap_{n \in \mathbb{N}} [a_{n}, b_{n}] \neq \emptyset \\
&\forall n \in \mathbb{N}
\end{align}
$$
De esta forma, demostramos que la intersección no es vacía. Si tengo una sucesión finita de elementos que se reducen, al final me quedará al menos un punto.

Esta propiedad tampoco se cumple en $\mathbb{Q}$, demostrando la incompletitud del conjunto.

**Contraejemplo en $\mathbb{Q}$**
Sea $(a_{n})_{n\in \mathbb{N}}$ definida por:
$$
\begin{align}
&a_{0}:=1 \\
&a_{n+1}:= \frac{3a_{n} + 4}{2a_{n} + 3}
\end{align}
$$
Sea $(b_{n})_{n\in \mathbb{N}}$ definida por:
$$
\begin{align}
&b_{n}:= \frac{2}{a_{n}}
\end{align}
$$
Aunque no vamos a hacerlo, aquí se puede demostrar que la primera sucesión es creciente y la segunda decreciente, que la primera sucesión siempre es menor o igual a la segunda sucesión. Sin embargo, ambas tienen límite $\sqrt{ 2 }$ (una por defecto y la otra por exceso). Entonces, cuando yo considero la intersección de los intervalos en $\mathbb{Q}$, todo desaparece al infinito, puesto que lo único que nos queda entre todos los $a_{n}$ y $b_{n}$ es un número que no existe en $\mathbb{Q}$.
$$
\cap_{n \in \mathbb{N}} [a_{n}, b_{n}] \cap \mathbb{Q} = \emptyset
$$

## Teorema (Principio de Arquímedes)
El principio de Arquímedes establece que para cualquier número real, existe un natural mayor.
$$
\forall x \in \mathbb{R}, \exists n \in \mathbb{N}, n > x
$$
Esto quiere decir que al final, los enteros relativos están en toda la recta. No hay parte de la recta que no tenga enteros relativos.

### Demostración
Por el absurdo, supongamos que la propiedad no se cumple. De esta forma intentamos probar el opuesto:
Por el absurdo, supongamos que $\exists x \in \mathbb{R}, \forall n \in \mathbb{N}, n \leq x$
$\implies$ x es cota superior de $\mathbb{N}$ (existe un real superior a todos los naturales)

De esta forma, como $\mathbb{N}$ tiene elementos, podemos comparar x por el supremo:
Sea $s:= sup(\mathbb{N})$

Definimos un supremo de $\mathbb{N}$, así que puedo aproximar dicho supremo a un natural utilizando épsilon.
Tomando 
$$
\begin{align}
&\epsilon = 1, \exists n \in \mathbb{N} \\
&s - 1 < n \leq s \\
&\implies s < n + 1 \in \mathbb{N}
\end{align}
$$
De esta forma, obtuvimos que el supremo de $\mathbb{N}$ es menor que algún natural (cosa que sería imposible por el concepto de supremo). De esta manera demostramos el principio de Arquímedes, que puede parecer obvio, pero debe ser demostrado.
Podemos determinar que esta propiedad no cambia para $\mathbb{R}$ y $\mathbb{Q}$, se cumple en ambos. Es importante considerar esto, ya que podemos ver al axioma de completitud como la conjunción del principio de los intervalos cerrados encajados y el principio de Arquímedes. $\mathbb{R}$ cumple ambos principios, pero $\mathbb{Q}$ no cumple el principio de los intervalos cerrados encajados.

## Variante infinitesimal
$$
\forall \epsilon > 0, \exists n \in \mathbb{N}^{*}, \frac{1}{n} < \epsilon
$$
$\mathbb{N}^{*} \rightarrow \text{ Naturales no nulos}$
Esto quiere decir que puedo tomar un numero positivo, que sin importar lo pequeño que sea, siempre existe un inverso de natural antes.

La propiedad se demuestra:
1. Paso $\epsilon$ a $\frac{1}{\epsilon}$.
2. Existe un natural n mayor a $\epsilon$.
3. Paso n al inverso ($\frac{1}{n}$).
4. Obtengo que $\frac{1}{n} < \frac{1}{\epsilon}$

De esta forma, simplemente debemos aplicar el principio de Arquímedes a $\frac{1}{\epsilon}$.
El principio de Arquímedes dice que hay naturales tan grandes como yo quiero, mientras que la variante infinitesimal dice que hay inversos naturales tan pequeños como yo quiero (en valor absoluto).

Se volvió un tema de investigación hallar cuerpos que cumplan una propiedad pero no la otra, por ejemplo $\mathbb{Q}$ (no cumple el principio de los intervalos cerrados encajados).
Lo interesante es encontrar lo opuesto: un intervalo que cumpla el principio de los intervalos cerrados encajados, pero no el principio de Arquímedes.

Vamos a concluir la clase hablando de funciones monótonas.

# Funciones monótonas
Una funcion $f: I \to \mathbb{R}$ definida en un intervalo $I \subset \mathbb{R}$ es:
- monótona creciente si $\forall x, x' \in I, x \leq x' \implies f(x) \leq f(x')$
- monótona decreciente si $\forall x, x' \in I, x \leq x' \implies f(x) \geq f(x')$

Una función monótona creciente puede estacionar.
Una función constante es a la vez creciente y decreciente, y la única función que cumple esto.
En general, obviamos la palabra monótona, puesto que cuando hablamos de creciente o decreciente, nos referimos a monótona creciente y monótona decreciente.

También tenemos funciones estrictamente crecientes y estrictamente decrecientes:
- f es estrictamente creciente si $\forall x, x' \in I, x < x' \implies f(x) < f(x')$
Implica que la función tiene que crecer siempre entre dos valores.
- f es estrictamente decreciente si $\forall x, x' \in I, x < x' \implies f(x) > f(x')$

Cuando una función es estrictamente creciente, en particular es creciente. Ídem para funciones estrictamente decrecientes.
Aquí podemos aclarar que la función constante es monótona creciente y monótona decreciente, pero no estrictamente creciente ni estrictamente decreciente.

Algunos ejemplos:
- $f(x)=x \rightarrow$ estrictamente creciente
- $f(x)=x \rightarrow$ estrictamente creciente si consideramos $f:[0,+\infty)\to R$, y estrictamente decreciente si consideramos $f:(-\infty,0]\to R$

**Propiedad**: Sea $f: (a,b)\to \mathbb{R}$ monótona creciente, y $x_{0} \in (a,b)$
Consideramos los siguientes conjuntos:
$$
\begin{align}
&\{ f(x): x < x_{0} \} \\
&\{ f(x): x > x_{0} \}
\end{align}
$$
De ambos conjuntos, puedo concluir lo siguiente:
$$
\begin{align}
&sup\{ f(x): x < x_{0} \} \leq f(x_{0}) \leq ínf\{ f(x): x > x_{0} \}
\end{align}
$$
Sin embargo, vamos a mostrar un contraejemplo, que indica que la desigualdad puede ser estricta:
![[Contraejemplo funciones monótonas.png]]

Con el ejemplo anterior, entendemos que en las funciones monótonas pueden tener saltos de continuidad (la función es discontinua). Sin embargo, algo interesante es que una función monótona tiene que tener una cantidad finita o numerable de saltos, no puede tener más.
En general, la irregularidad mayor que se puede observar en una función monótona son los saltos de continuidad (que pueden no existir).

En la siguiente clase, comenzaremos con Integrales.